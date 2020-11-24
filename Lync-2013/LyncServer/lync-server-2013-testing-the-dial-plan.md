---
title: 'Lync Server 2013: Testen des Wählplans'
description: 'Lync Server 2013: Testen des Wählplans'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing the dial plan
ms:assetid: 70eec03c-aca3-4106-86a7-77ae96b53779
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690130(v=OCS.15)
ms:contentKeyID: 63969616
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a0ef2e3fce9d1fbbb0186b1b7aef608834145d3e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395307"
---
# <a name="testing-the-dial-plan-in-lync-server-2013"></a><span data-ttu-id="cacee-103">Testen des Wählplans in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cacee-103">Testing the dial plan in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cacee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cacee-104">

<span> </span></span></span>

<span data-ttu-id="cacee-105">_**Letztes Änderungsdatum des Themas:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="cacee-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cacee-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="cacee-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="cacee-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="cacee-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cacee-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="cacee-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="cacee-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="cacee-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cacee-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="cacee-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="cacee-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="cacee-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="cacee-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsDialPlan-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="cacee-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsDialPlan cmdlet.</span></span> <span data-ttu-id="cacee-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="cacee-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsDialPlan&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="cacee-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cacee-114">Description</span></span>

<span data-ttu-id="cacee-115">Mit dem Test-CsDialPlan-Cmdlet können Sie die Ergebnisse der Anwendung eines Wählplans auf eine bestimmte Telefonnummer anzeigen.</span><span class="sxs-lookup"><span data-stu-id="cacee-115">The Test-CsDialPlan cmdlet enables you to see the results of applying a dial plan to a given telephone number.</span></span> <span data-ttu-id="cacee-116">Wählpläne liefern Informationen, wie beispielsweise die Anwendung von Normalisierungsregeln, die erforderlich sind, damit Enterprise-VoIP-Benutzer Telefonanrufe tätigen können.</span><span class="sxs-lookup"><span data-stu-id="cacee-116">Dial plans provide information, such as how normalization rules are applied, required to enable Enterprise Voice users to make telephone calls.</span></span> <span data-ttu-id="cacee-117">Mit einer gewählten Nummer und einem Wählplan wird mit diesem Cmdlet überprüft, welche Normalisierungsregel innerhalb des Wählplans angewendet wird und welche übersetzte Nummer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cacee-117">Given a dialed number and a dial plan, this cmdlet will verify which normalization rule within the dial plan will be applied and what the translated number will be.</span></span>

<span data-ttu-id="cacee-118">Sie können dieses Cmdlet verwenden, um Probleme bei der Übersetzung von Zahlen zu beheben oder um zu überprüfen, wie Regeln für bestimmte Zahlen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="cacee-118">You can use this cmdlet for troubleshooting issues with number translations, or for verifying how to apply rules against certain numbers.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="cacee-119">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="cacee-119">Running the test</span></span>

<span data-ttu-id="cacee-120">Für das Test-CsDialPlan-Cmdlet müssen Sie zwei Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="cacee-120">The Test-CsDialPlan cmdlet requires you to do two things.</span></span> <span data-ttu-id="cacee-121">Zunächst müssen Sie eine Instanz des Wählplans abrufen, der getestet wird. Dies kann mithilfe des Get-CsDialPlan-Cmdlets erfolgen.</span><span class="sxs-lookup"><span data-stu-id="cacee-121">First, you must obtain an instance of the dial plan being tested; that can be done by using the Get-CsDialPlan cmdlet.</span></span> <span data-ttu-id="cacee-122">Als nächstes müssen Sie die Telefonnummer angeben, die normalisiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cacee-122">Second, you must specify the phone number that has to be normalized.</span></span> <span data-ttu-id="cacee-123">Das für die Telefonnummer verwendete Format sollte mit der Nummer übereinstimmen, die von einem Benutzer gewählt/eingegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="cacee-123">The format that is used for the phone number should match the number as dialed/entered by a user.</span></span> <span data-ttu-id="cacee-124">Mit diesem Befehl wird beispielsweise eine Instanz des Wählplans, redmonddialplan ", abgerufen, und es wird überprüft, ob die Telefonnummer 12065551219 normalisiert werden kann:</span><span class="sxs-lookup"><span data-stu-id="cacee-124">For example, this command retrieves an instance of the dial plan, RedmondDialPlan, and checks whether the phone number 12065551219 can be normalized:</span></span>

    Get-CsDialPlan -Identity "RedmondDialPlan" | Test-CsDialPlan -DialedNumber "12065551219" | Format-List

<span data-ttu-id="cacee-125">Wenn Sie über eine Normalisierungsregel verfügen, die die Landesvorwahl (in diesem Beispiel 1) und die Ortsvorwahl (206) automatisch hinzufügt, sollten Sie die Telefonnummer 5551219 wie folgt überprüfen:</span><span class="sxs-lookup"><span data-stu-id="cacee-125">If you have a normalization rule that automatically adds the country code (in this example, 1) and the area code (206), then you might want to check the phone number 5551219, as follows:</span></span>

    Get-CsDialPlan -Identity "RedmondDialPlan" | Test-CsDialPlan -DialedNumber "5551219" | Format-List

<span data-ttu-id="cacee-126">Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsDialPlan](https://docs.microsoft.com/powershell/module/skype/Test-CsDialPlan) .</span><span class="sxs-lookup"><span data-stu-id="cacee-126">For more information, see the Help documentation for the [Test-CsDialPlan](https://docs.microsoft.com/powershell/module/skype/Test-CsDialPlan) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="cacee-127">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="cacee-127">Determining success or failure</span></span>

<span data-ttu-id="cacee-128">Test-CsDialPlan weicht von vielen der lync Server-Test-Cmdlets ab, da Sie nur indirekt angibt, ob ein Test erfolgreich war oder fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="cacee-128">Test-CsDialPlan differs from many of the Lync Server test cmdlets because it only indirectly indicates whether a test succeeded or failed.</span></span> <span data-ttu-id="cacee-129">Wenn Sie Test-CsDialPlan verwenden, erhalten Sie keine ähnliche Ausgabe wie diese, wobei das Ergebnis deutlich gekennzeichnet ist:</span><span class="sxs-lookup"><span data-stu-id="cacee-129">When using Test-CsDialPlan you do not receive back output similar to this with the Result clearly labeled:</span></span>

<span data-ttu-id="cacee-130">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="cacee-130">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="cacee-131">Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="cacee-131">Result : Success</span></span>

<span data-ttu-id="cacee-132">Latenz: 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="cacee-132">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="cacee-133">Fehler</span><span class="sxs-lookup"><span data-stu-id="cacee-133">Error :</span></span>

<span data-ttu-id="cacee-134">Diagnose</span><span class="sxs-lookup"><span data-stu-id="cacee-134">Diagnosis :</span></span>

<span data-ttu-id="cacee-135">Wenn Test-CsDialPlan erfolgreich ist, erhalten Sie stattdessen Informationen zur Normalisierungsregel, die die angegebene Telefonnummer erfolgreich übersetzen und verwenden konnte:</span><span class="sxs-lookup"><span data-stu-id="cacee-135">Instead, if Test-CsDialPlan succeeds, then you'll receive information about the normalization rule that was able to successfully translate and use the specified phone number:</span></span>

<span data-ttu-id="cacee-136">TranslatedNumber: + 12065551219</span><span class="sxs-lookup"><span data-stu-id="cacee-136">TranslatedNumber : +12065551219</span></span>

<span data-ttu-id="cacee-137">MatchingRule: Description =; Muster = ^ ( \\ d (11)) $; Übersetzung = + $1;</span><span class="sxs-lookup"><span data-stu-id="cacee-137">MatchingRule : Description=;Pattern=^(\\d(11))$;Translation=+$1;</span></span>

<span data-ttu-id="cacee-138">Name = Präfix alle; IsInternalExtension = falsch</span><span class="sxs-lookup"><span data-stu-id="cacee-138">Name=Prefix All; IsInternalExtension=False</span></span>

<span data-ttu-id="cacee-139">Wenn Test-CsDialPlan fehlschlägt (das heißt, wenn der Wählplan nicht über eine Normalisierungsregel verfügt, die die angegebene Telefonnummer übersetzen kann), erhalten Sie einfach die "leere" Ausgabe wie folgt:</span><span class="sxs-lookup"><span data-stu-id="cacee-139">If Test-CsDialPlan fails (that is, if the dial plan does not have a normalization rule that can translate the specified phone number), you'll just receive “empty” output as follows:</span></span>

<span data-ttu-id="cacee-140">TranslatedNumber :</span><span class="sxs-lookup"><span data-stu-id="cacee-140">TranslatedNumber :</span></span>

<span data-ttu-id="cacee-141">MatchingRule</span><span class="sxs-lookup"><span data-stu-id="cacee-141">MatchingRule :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="cacee-142">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="cacee-142">Reasons why the test might have failed</span></span>

<span data-ttu-id="cacee-143">Im folgenden finden Sie einige häufige Gründe, warum Test-CsDialPlan fehlschlagen kann:</span><span class="sxs-lookup"><span data-stu-id="cacee-143">Here are some common reasons why Test-CsDialPlan might fail:</span></span>

  - <span data-ttu-id="cacee-144">Möglicherweise haben Sie bei der Angabe der Telefonnummer ein falsches Format verwendet.</span><span class="sxs-lookup"><span data-stu-id="cacee-144">You might have used an incorrect format when specifying the phone number.</span></span> <span data-ttu-id="cacee-145">Zu den Wählplänen gehören Normalisierungsregeln, mit denen lync Server die von einem Benutzer gewählten oder eingegebenen Telefonnummern übersetzen kann.</span><span class="sxs-lookup"><span data-stu-id="cacee-145">Dial plans include normalization rules that enable Lync Server to translate the phone numbers dialed or entered by a user.</span></span> <span data-ttu-id="cacee-146">Daher sollten ihre Wähleinstellungen die Normalisierungsregeln aufweisen, die den Zahlen entsprechen, die Benutzer wahrscheinlich wählen.</span><span class="sxs-lookup"><span data-stu-id="cacee-146">Therefore, your dial plan should have normalization rules that match the numbers users are likely to dial.</span></span> <span data-ttu-id="cacee-147">Wenn Benutzer beispielsweise die Landesvorwahl, Ortsvorwahl und dann die Telefonnummer selbst wählen, bedeutet dies, dass Ihr Wählplan über eine Normalisierungsregel zur Behandlung von Telefonnummern wie diesen verfügt:</span><span class="sxs-lookup"><span data-stu-id="cacee-147">For example, if users might dial the country code, area code, and then the phone number itself, that means that your dial plan should have a normalization rule to handle phone numbers such as this:</span></span>
    
    <span data-ttu-id="cacee-148">12065551219</span><span class="sxs-lookup"><span data-stu-id="cacee-148">12065551219</span></span>
    
    <span data-ttu-id="cacee-149">Wenn Sie jedoch eine falsche Telefonnummer eingeben (beispielsweise wenn Sie die letzte Ziffer verlassen), schlägt Test-CsDialPlan fehl.</span><span class="sxs-lookup"><span data-stu-id="cacee-149">However, if you enter an incorrect phone number (for example, leaving off the final digit), then Test-CsDialPlan will fail.</span></span> <span data-ttu-id="cacee-150">Das liegt nicht daran, dass die Wähleinstellungen fehlerhaft sind, sondern weil Sie eine Telefonnummer eingegeben haben, als nicht interpretiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="cacee-150">That’s not because the dial plan is faulty but because you have entered a phone number than can’t be interpreted.</span></span>

<span data-ttu-id="cacee-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cacee-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

