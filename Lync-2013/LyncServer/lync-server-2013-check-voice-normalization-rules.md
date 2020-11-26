---
title: 'Lync Server 2013: Überprüfen von Regeln für die sprach Normalisierung'
description: 'Lync Server 2013: Überprüfen der Normalisierungsregeln für die Sprachausgabe.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Check voice normalization rules
ms:assetid: bf71a218-71cd-4b64-b8e8-b3a98b6e87a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725212(v=OCS.15)
ms:contentKeyID: 63969649
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f68bbde24a3dc7d8e8214dcfe506d4b8112fbbb3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435005"
---
# <a name="check-voice-normalization-rules-in-lync-server-2013"></a><span data-ttu-id="b3ae8-103">Überprüfen von VoIP-Normalisierungsregeln in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3ae8-103">Check voice normalization rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b3ae8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b3ae8-104">

<span> </span></span></span>

<span data-ttu-id="b3ae8-105">_**Letztes Änderungsdatum des Themas:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="b3ae8-105">_**Topic Last Modified:** 2014-05-20_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3ae8-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="b3ae8-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="b3ae8-107">Monatlich</span><span class="sxs-lookup"><span data-stu-id="b3ae8-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3ae8-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="b3ae8-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="b3ae8-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="b3ae8-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3ae8-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="b3ae8-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="b3ae8-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="b3ae8-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsVoiceNormalizationRule-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsVoiceNormalizationRule cmdlet.</span></span> <span data-ttu-id="b3ae8-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="b3ae8-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsVoiceNormalizationRule&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="b3ae8-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b3ae8-114">Description</span></span>

<span data-ttu-id="b3ae8-115">Regeln für die sprach Normalisierung werden verwendet, um eine Telefonnummer zu konvertieren, die von einem Benutzer gewählt wurde (beispielsweise 2065551219), in das E. 164-Format, das von lync Server (+ 12065551219) verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-115">Voice normalization rules are used to convert a phone number dialed by a user (for example, 2065551219) to the E.164 format that is used by Lync Server (+12065551219).</span></span> <span data-ttu-id="b3ae8-116">Wenn Benutzer beispielsweise die Möglichkeit haben, eine Telefonnummer zu wählen, ohne die Landesvorwahl oder die Ortsvorwahl (z. b. 5551219) einzuschließen, müssen Sie über eine sprach Normalisierungsregel verfügen, mit der diese Zahl in das e. 164-Format konvertiert werden kann: + 12065551219.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-116">For example, if users are in the habit of dialing a phone number without including the country code or the area code (e.g., 5551219) then you must have a voice normalization rule that can convert that number to the E.164 format: +12065551219.</span></span> <span data-ttu-id="b3ae8-117">Ohne diese Regel ist der Benutzer nicht in der Lage, 555-1219 anzurufen.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-117">Without such a rule, the user won't be able to call 555-1219.</span></span>

<span data-ttu-id="b3ae8-118">Das Test-CsVoiceNormalizationRule-Cmdlet überprüft, ob eine bestimmte Telefonnummer durch eine angegebene VoIP-Normalisierungsregel erfolgreich konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-118">The Test-CsVoiceNormalizationRule cmdlet verifies that a specified voice normalization rule can successfully convert a specified phone number.</span></span> <span data-ttu-id="b3ae8-119">Mit diesem Befehl wird beispielsweise überprüft, ob die globale Normalisierungsregel NoAreaCode die Wählzeichenfolge 5551219 normalisieren und konvertieren kann.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-119">For example, this command checks whether the global normalization rule NoAreaCode can normalize and convert the dial string 5551219.</span></span>

`Get-CsVoiceNormalizationRule -Identity "global/NoAreaCode" | Test-CsVoiceNormalizationRule -DialedNumber "5551219"`

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="b3ae8-120">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="b3ae8-120">Running the test</span></span>

<span data-ttu-id="b3ae8-121">Zum Ausführen des Test-CsVoiceNormalizationRule-Cmdlets müssen Sie zuerst das Get-CsVoiceNormalizationRule-Cmdlet verwenden, um eine Instanz der getesteten Regel abzurufen, und diese Instanz dann an Test-CsVoiceNormalizationRule.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-121">To run the Test-CsVoiceNormalizationRule cmdlet, you must first use the Get-CsVoiceNormalizationRule cmdlet to retrieve an instance of the rule being tested, and then pipe that instance to Test-CsVoiceNormalizationRule.</span></span> <span data-ttu-id="b3ae8-122">Eine ähnliche Syntax wie diese funktioniert nicht:</span><span class="sxs-lookup"><span data-stu-id="b3ae8-122">Syntax similar to this won't work:</span></span>

<span data-ttu-id="b3ae8-123">Test-CsVoiceNormalizationRule-DialedNumber "12065551219" – NormalizationRule "Global/Prefix all"</span><span class="sxs-lookup"><span data-stu-id="b3ae8-123">Test-CsVoiceNormalizationRule -DialedNumber "12065551219" –NormalizationRule "global/Prefix All"</span></span>

<span data-ttu-id="b3ae8-124">Verwenden Sie stattdessen Syntax wie die folgende, die sowohl die Get-CsVoiceNormalizationRule als auch die Test-CsVoiceNormalizationRule-Cmdlets kombiniert:</span><span class="sxs-lookup"><span data-stu-id="b3ae8-124">Instead, use syntax such as the following, which combines both the Get-CsVoiceNormalizationRule and the Test-CsVoiceNormalizationRule cmdlets:</span></span>

<span data-ttu-id="b3ae8-125">Get-CsVoiceNormalizationRule-Identity "Global/Prefix all" | Test-CsVoiceNormalizationRule-DialedNumber "12065551219"</span><span class="sxs-lookup"><span data-stu-id="b3ae8-125">Get-CsVoiceNormalizationRule -Identity "global/Prefix All" | Test-CsVoiceNormalizationRule -DialedNumber "12065551219"</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b3ae8-126">.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-126">.</span></span> <span data-ttu-id="b3ae8-127">Sie können auch diesen Ansatz verwenden, um eine Instanz einer Regel abzurufen und diese Regel dann mit einer angegebenen Telefonnummer zu testen:</span><span class="sxs-lookup"><span data-stu-id="b3ae8-127">Or, you can also use this approach to retrieve an instance of a rule and then test that rule against a specified phone number:</span></span>



</div>

`$x = Get-CsVoiceNormalizationRule -Identity "global/Prefix All"`

`Test-CsVoiceNormalizationRule -DialedNumber "12065551219" -NormalizationRule $x`

<span data-ttu-id="b3ae8-128">Geben Sie den Wert für den DialedNumber-Parameter genau so ein, wie Sie erwarten, dass die Nummer gewählt wird.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-128">Enter the value for the DialedNumber parameter exactly as you expect that number to be dialed.</span></span> <span data-ttu-id="b3ae8-129">Wenn beispielsweise die angegebene sprach Normalisierungsregel die Landesvorwahl (die Initiale 1 im Wert 12065551219) automatisch hinzufügen soll, sollten Sie die Landesvorwahl nicht angeben:</span><span class="sxs-lookup"><span data-stu-id="b3ae8-129">For example, if the specified voice normalization rule is supposed to automatically add the country code (the initial 1 in the value 12065551219) then you should leave off the country code:</span></span>

`-DialedNumber "2065551219"`

<span data-ttu-id="b3ae8-130">Wenn die Regel ordnungsgemäß konfiguriert ist, wird beim Übersetzen der Nummer automatisch die Landesvorwahl in das von lync Server verwendete E. 164-Format hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-130">If the rule is configured correctly, it will automatically add the country code when translating the number to the E.164 format that is used by Lync Server.</span></span>

<span data-ttu-id="b3ae8-131">Weitere Informationen finden Sie in der Hilfedokumentation für das Cmdlet "Test-CsVoiceNormalizationRule".</span><span class="sxs-lookup"><span data-stu-id="b3ae8-131">For more information, see the Help documentation for the Test-CsVoiceNormalizationRule cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="b3ae8-132">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="b3ae8-132">Determining success or failure</span></span>

<span data-ttu-id="b3ae8-133">Wenn die angegebene sprach Normalisierungsregel die angegebene Nummer übersetzen kann, wird die übersetzte Nummer auf dem Bildschirm angezeigt:</span><span class="sxs-lookup"><span data-stu-id="b3ae8-133">If the specified voice normalization rule can translate the supplied number then the translated number will be displayed on-screen:</span></span>

<span data-ttu-id="b3ae8-134">TranslatedNumber</span><span class="sxs-lookup"><span data-stu-id="b3ae8-134">TranslatedNumber</span></span>

\----------------

<span data-ttu-id="b3ae8-135">\+12065551219</span><span class="sxs-lookup"><span data-stu-id="b3ae8-135">\+12065551219</span></span>

<span data-ttu-id="b3ae8-136">Wenn der Test fehlschlägt, wird eine leere übersetzte Zahl zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="b3ae8-136">If the test fails then a blank translated number will be returned:</span></span>

<span data-ttu-id="b3ae8-137">TranslatedNumber</span><span class="sxs-lookup"><span data-stu-id="b3ae8-137">TranslatedNumber</span></span>

\----------------

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="b3ae8-138">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="b3ae8-138">Reasons why the test might have failed</span></span>

<span data-ttu-id="b3ae8-139">Wenn die Test-CsVoiceNormalizationRule eine übersetzte Zahl zurückgibt, bedeutet dies, dass die angegebene sprach Normalisierungsregel die angegebene Telefonnummer nicht in das von lync Server verwendete E. 164-Format übersetzen konnte.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-139">If the Test-CsVoiceNormalizationRule does return a translated number that means that the specified voice normalization rule was unable to translate the supplied telephone number into the E.164 format that is used by Lync Server.</span></span> <span data-ttu-id="b3ae8-140">Um dies zu überprüfen, stellen Sie zuerst sicher, dass Sie die Telefonnummer richtig eingegeben haben.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-140">To verify that, first make sure that you typed the telephone number in correctly.</span></span> <span data-ttu-id="b3ae8-141">Sie würden beispielsweise davon ausgehen, dass die Regel für die sprach Normalisierung Probleme hat, eine Zahl zu übersetzen, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="b3ae8-141">For example, you would expect your voice normalization rule to have problems translating a number similar to this:</span></span>

`-DialedNumber "1"`

<span data-ttu-id="b3ae8-142">Wenn die Nummer richtig eingegeben wurde, sollte der nächste Schritt darin liegen, zu überprüfen, ob die angegebene Normalisierungsregel für die Behandlung dieser Telefonnummer vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-142">Assuming the number was entered correctly, your next step should be to verify that the specified normalization rule is designed to handle that phone number.</span></span> <span data-ttu-id="b3ae8-143">Beispielsweise kann eine Normalisierungsregel zur Behandlung des Formats 12065551219 entwickelt werden, aber eine zweite Regel kann für die Behandlung der Zahl 2065551219 entworfen werden.</span><span class="sxs-lookup"><span data-stu-id="b3ae8-143">For example, one normalization rule might be designed to handle the format 12065551219, but a second rule might be designed to handle the number 2065551219.</span></span> <span data-ttu-id="b3ae8-144">(Das ist die gleiche Telefonnummer, abzüglich der Landesvorwahl 1 am Anfang.) Wenn Sie detaillierte Informationen zu einer Regel für die sprach Normalisierung zurückgeben möchten, führen Sie einen Befehl wie den folgenden aus:</span><span class="sxs-lookup"><span data-stu-id="b3ae8-144">(That’s the same phone number, minus the country code 1 at the very beginning.) To return detailed information about a voice normalization rule, run a command similar to this:</span></span>

`Get-CsVoiceNormalizationRule -Identity "global/Prefix All" | Format-List`

<span data-ttu-id="b3ae8-145">Führen Sie stattdessen diesen Befehl aus, um detaillierte Informationen zu allen Regeln für die sprach Normalisierung zurückzugeben:</span><span class="sxs-lookup"><span data-stu-id="b3ae8-145">To return detailed information about all the voice normalization rules, run this command instead:</span></span>

`Get-CsVoiceNormalizationRule | Format-List`

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b3ae8-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b3ae8-146">See Also</span></span>


[<span data-ttu-id="b3ae8-147">Test-CsVoiceNormalizationRule</span><span class="sxs-lookup"><span data-stu-id="b3ae8-147">Test-CsVoiceNormalizationRule</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsVoiceNormalizationRule)  
  

<span data-ttu-id="b3ae8-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b3ae8-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

