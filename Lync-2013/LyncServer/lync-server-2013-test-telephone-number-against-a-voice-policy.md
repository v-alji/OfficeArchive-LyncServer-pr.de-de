---
title: 'Lync Server 2013: Testen einer Telefonnummer mit einer VoIP-Richtlinie'
description: 'Lync Server 2013: Testen Sie die Telefonnummer mit einer VoIP-Richtlinie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test telephone number against a voice policy
ms:assetid: 30c51700-17c6-4c57-891a-8d5ec30b50ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn725207(v=OCS.15)
ms:contentKeyID: 63969596
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5a6523e7657bd4c30c23909bb02e2569b6067298
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441221"
---
# <a name="test-telephone-number-against-a-voice-policy-in-lync-server-2013"></a><span data-ttu-id="7ea13-103">Testen einer Telefonnummer für eine VoIP-Richtlinie in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7ea13-103">Test telephone number against a voice policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7ea13-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7ea13-104">

<span> </span></span></span>

<span data-ttu-id="7ea13-105">_**Letztes Änderungsdatum des Themas:** 2014-05-20_</span><span class="sxs-lookup"><span data-stu-id="7ea13-105">_**Topic Last Modified:** 2014-05-20_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ea13-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="7ea13-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="7ea13-107">Monatlich</span><span class="sxs-lookup"><span data-stu-id="7ea13-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ea13-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="7ea13-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="7ea13-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7ea13-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ea13-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="7ea13-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="7ea13-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="7ea13-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="7ea13-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsVoicePolicy-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="7ea13-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsVoicePolicy cmdlet.</span></span> <span data-ttu-id="7ea13-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="7ea13-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<p><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsVoicePolicy&quot;}</code></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="7ea13-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7ea13-114">Description</span></span>

<span data-ttu-id="7ea13-115">Die Möglichkeit von Enterprise-VoIP-Benutzern, ausgehende Telefonanrufe über das öffentlich geschaltete Telefonnetz (PSTN) zu tätigen, hängt zu einem Großteil von drei Dingen ab:</span><span class="sxs-lookup"><span data-stu-id="7ea13-115">The ability of Enterprise Voice users to make outgoing phone calls over the Public Switched Telephone network (PSTN) hinges, in large part, on three things:</span></span>

  - <span data-ttu-id="7ea13-116">Die dem Benutzer zugewiesene VoIP-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="7ea13-116">The voice policy assigned to the user.</span></span>

  - <span data-ttu-id="7ea13-117">Die VoIP-Routen, die zum Weiterleiten von Anrufen von lync Server an das PSTN-Netzwerk verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="7ea13-117">The voice routes used to route calls from Lync Server to the PSTN network.</span></span>

  - <span data-ttu-id="7ea13-118">Die PSTN-Nutzung, eine lync Server-Eigenschaft, die eine VoIP-Richtlinie mit einer VoIP-Route verbindet.</span><span class="sxs-lookup"><span data-stu-id="7ea13-118">The PSTN usage, a Lync Server property that connects a voice policy to a voice route.</span></span>

<span data-ttu-id="7ea13-119">Die PSTN-Nutzung ist besonders wichtig: Es handelt sich um die Eigenschaft, die eine VoIP-Richtlinie mit einer VoIP-Route verbindet.</span><span class="sxs-lookup"><span data-stu-id="7ea13-119">The PSTN usage is especially important: it’s the property that connects a voice policy to a voice route.</span></span> <span data-ttu-id="7ea13-120">(Eine VoIP-Richtlinie und eine VoIP-Route werden als verbunden bezeichnet, wenn Sie mindestens eine PSTN-Nutzung gemeinsam haben.) VoIP-Richtlinien können ohne Angabe einer PSTN-Nutzung konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="7ea13-120">(A voice policy and a voice route are said to be connected if they have at least one PSTN usage in common.) Voice policies can be configured without specifying a PSTN usage.</span></span> <span data-ttu-id="7ea13-121">In diesem Fall können Benutzer, denen diese Richtlinie zugewiesen wurde, keine ausgehenden Anrufe über das PSTN-Netzwerk führen.</span><span class="sxs-lookup"><span data-stu-id="7ea13-121">In that case, users who were assigned that policy won't be able to make outgoing calls over the PSTN network.</span></span> <span data-ttu-id="7ea13-122">Ebenso können VoIP-Routen, die nicht über mindestens eine festgelegte PSTN-Nutzung verfügen, keine Anrufe an das PSTN-Netzwerk weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="7ea13-122">Likewise, voice routes that do not have at least one specified PSTN usage will be unable to route calls to the PSTN network.</span></span>

<span data-ttu-id="7ea13-123">Das Test-CsVoicePolicy-Cmdlet überprüft, ob eine bestimmte VoIP-Richtlinie über eine PSTN-Nutzung verfügt und dass die Nutzung von mindestens einer VoIP-Route freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="7ea13-123">The Test-CsVoicePolicy cmdlet verifies that a given voice policy has a PSTN usage and that the usage is shared by at least one voice route.</span></span> <span data-ttu-id="7ea13-124">Wenn die Überprüfung, die von Test-CsVoicePolicy ausgeführt wird, erfolgreich ist, meldet das Cmdlet den Namen der ersten gültigen VoIP-Route sowie den Namen der PSTN-Nutzung, die die Richtlinie mit der Route verbindet, zurück.</span><span class="sxs-lookup"><span data-stu-id="7ea13-124">If the verification run by Test-CsVoicePolicy succeeds, the cmdlet will report back the name of the first valid voice route it finds, and also the name of the PSTN usage that connects the policy to the route.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="7ea13-125">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="7ea13-125">Running the test</span></span>

<span data-ttu-id="7ea13-126">Zum Ausführen des Test-CsVoicePolicy-Cmdlets müssen Sie zuerst das Cmdlet Get-CsVoicePolicy verwenden, um eine Instanz der VoIP-Richtlinie abzurufen, die getestet werden soll. Diese Instanz muss dann zu Test-CsVoicePolicy umgeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="7ea13-126">To run the Test-CsVoicePolicy cmdlet you must first use the Get-CsVoicePolicy cmdlet retrieve an instance of the voice policy to be tested; that instance must then be piped to Test-CsVoicePolicy.</span></span> <span data-ttu-id="7ea13-127">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7ea13-127">For example:</span></span>

`Get-CsVoicePolicy -Identity "Global" | Test-CsVoicePolicy -TargetNumber "+12065551219"`

<span data-ttu-id="7ea13-128">Beachten Sie, dass dieser Befehl, der keine Get-CsVoicePolicy zum Abrufen einer VoIP-Richtlinieninstanz verwendet, fehlerhaft ist:</span><span class="sxs-lookup"><span data-stu-id="7ea13-128">Note that this command, which does not use Get-CsVoicePolicy to retrieve a voice policy instance, will fail:</span></span>

`Test-CsVoicePolicy -TargetNumber "+12065551219" -VoicePolicy "Global"`

<span data-ttu-id="7ea13-129">Wenn Sie alle VoIP-Richtlinien für eine bestimmte Telefonnummer überprüfen möchten, verwenden Sie einen ähnlichen Befehl wie den folgenden:</span><span class="sxs-lookup"><span data-stu-id="7ea13-129">If you want to check all the voice policies against a specified phone number then use a command similar to this:</span></span>

`Get-CsVoicePolicy | Test-CsVoicePolicy -TargetNumber "+12065551219"`

<span data-ttu-id="7ea13-130">Beachten Sie, dass der TargetNumber mit dem E. 164-Format angegeben werden muss.</span><span class="sxs-lookup"><span data-stu-id="7ea13-130">Note that the TargetNumber must be specified by using the E.164 format.</span></span> <span data-ttu-id="7ea13-131">Test-CsVoicePolicy versucht nicht, Telefonnummern in das E. 164-Format zu normalisieren oder zu übersetzen.</span><span class="sxs-lookup"><span data-stu-id="7ea13-131">Test-CsVoicePolicy won't attempt to normalize or translate phone numbers into the E.164 format.</span></span>

<span data-ttu-id="7ea13-132">Weitere Informationen finden Sie in der Hilfedokumentation für das Cmdlet "Test-CsVoicePolicy".</span><span class="sxs-lookup"><span data-stu-id="7ea13-132">For more information, see the Help documentation for the Test-CsVoicePolicy cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="7ea13-133">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="7ea13-133">Determining success or failure</span></span>

<span data-ttu-id="7ea13-134">Wenn die VoIP-Richtlinie sowohl eine übereinstimmende VoIP-Route als auch eine übereinstimmende PSTN-Nutzung finden kann, werden sowohl die Route als auch die Verwendung auf dem Bildschirm angezeigt:</span><span class="sxs-lookup"><span data-stu-id="7ea13-134">If the voice policy can find both a matching voice route and a matching PSTN usage, then both the route and the usage will be displayed on-screen:</span></span>

<span data-ttu-id="7ea13-135">FirstMatchingRoute MatchingUsage</span><span class="sxs-lookup"><span data-stu-id="7ea13-135">FirstMatchingRoute MatchingUsage</span></span>

<span data-ttu-id="7ea13-136">\------------------ -------------</span><span class="sxs-lookup"><span data-stu-id="7ea13-136">\------------------ -------------</span></span>

<span data-ttu-id="7ea13-137">RedmondVoiceRoute RedmondPstnUsage</span><span class="sxs-lookup"><span data-stu-id="7ea13-137">RedmondVoiceRoute RedmondPstnUsage</span></span>

<span data-ttu-id="7ea13-138">Wenn entweder eine geeignete VoIP-Route oder eine entsprechende PSTN-Nutzung gefunden werden kann, werden leere Eigenschaftswerte auf dem Bildschirm angezeigt:</span><span class="sxs-lookup"><span data-stu-id="7ea13-138">If either an appropriate voice route or an appropriate PSTN usage cannot be found then blank property values will be displayed on-screen:</span></span>

<span data-ttu-id="7ea13-139">FirstMatchingRoute MatchingUsage</span><span class="sxs-lookup"><span data-stu-id="7ea13-139">FirstMatchingRoute MatchingUsage</span></span>

<span data-ttu-id="7ea13-140">\------------------ -------------</span><span class="sxs-lookup"><span data-stu-id="7ea13-140">\------------------ -------------</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="7ea13-141">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="7ea13-141">Reasons why the test might have failed</span></span>

<span data-ttu-id="7ea13-142">Wenn Test-CsVoicePolicy keine Übereinstimmung zurückgibt, kann dies bedeuten, dass die VoIP-Richtlinie keine PSTN-Nutzung mit einer VoIP-Route teilt.</span><span class="sxs-lookup"><span data-stu-id="7ea13-142">If Test-CsVoicePolicy does not return a match that could mean that the voice policy does not share a PSTN usage with a voice route.</span></span> <span data-ttu-id="7ea13-143">Um dies zu überprüfen, verwenden Sie ein Cmdlet ähnlich dem folgenden, um zu überprüfen, ob PSTN-Nutzungen der VoIP-Richtlinie zugewiesen sind:</span><span class="sxs-lookup"><span data-stu-id="7ea13-143">To verify that, use a cmdlet similar to the following to verify that PSTN usages assigned to the voice policy:</span></span>

`Get-CsVoicePolicy -Identity "Global" | Select-Object PstnUsages | Format-List`

<span data-ttu-id="7ea13-144">Führen Sie als nächstes diesen Befehl aus, um festzustellen, welche PSTN-Nutzungen für Ihre VoIP-Routen zuzuweisen sind:</span><span class="sxs-lookup"><span data-stu-id="7ea13-144">Next, run this command to determine the PSTN usages assign to each of your voice routes:</span></span>

`Get-CsVoiceRoute | Select-Object Identity, PstnUsages`

<span data-ttu-id="7ea13-145">Wenn Sie Übereinstimmungen sehen (das heißt, wenn Sie eine oder mehrere VoIP-Routen sehen, die mindestens eine PSTN-Nutzung mit Ihrer VoIP-Richtlinie aufweisen), sollten Sie das Test-CsVoiceRoute-Cmdlet ausführen, um zu überprüfen, ob die VoIP-Route die angegebene Telefonnummer wählen kann.</span><span class="sxs-lookup"><span data-stu-id="7ea13-145">If you see any matches (that is, if you see one or more voice routes that share at least one PSTN usage with your voice policy), you should then run the Test-CsVoiceRoute cmdlet to verify that the voice route can dial the supplied phone number.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7ea13-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7ea13-146">See Also</span></span>


[<span data-ttu-id="7ea13-147">Test-CsVoicePolicy</span><span class="sxs-lookup"><span data-stu-id="7ea13-147">Test-CsVoicePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsVoicePolicy)  
  

<span data-ttu-id="7ea13-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7ea13-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

