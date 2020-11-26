---
title: 'Lync Server 2013: Testen von UCWA-Konferenzen'
description: 'Lync Server 2013: Testen von UCWA-Konferenzen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing UCWA conferencing
ms:assetid: 62b3866a-0759-4b1f-99ec-5a68d6a74f00
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727306(v=OCS.15)
ms:contentKeyID: 63969610
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37f88a683abb67d55211422fc4dcf45fc1d5c966
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439737"
---
# <a name="testing-ucwa-conferencing-in-lync-server-2013"></a><span data-ttu-id="bc308-103">Testen von UCWA-Konferenzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc308-103">Testing UCWA conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bc308-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bc308-104">

<span> </span></span></span>

<span data-ttu-id="bc308-105">_**Letztes Änderungsdatum des Themas:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="bc308-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bc308-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="bc308-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="bc308-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="bc308-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bc308-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="bc308-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="bc308-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="bc308-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bc308-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="bc308-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="bc308-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="bc308-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="bc308-112">Beim Ausführen mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des <strong>Test-CsUcwaConference-</strong> Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="bc308-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsUcwaConference</strong> cmdlet.</span></span> <span data-ttu-id="bc308-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="bc308-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsUcwaConference&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="bc308-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bc308-114">Description</span></span>

<span data-ttu-id="bc308-115">Das Cmdlet **Test-CsUcwaConference** überprüft, ob ein paar Testbenutzer mithilfe der Unified Communications Web-API (UCWA) eine Onlinekonferenz planen, daran teilnehmen und dann eine Onlinekonferenz durchführen können.</span><span class="sxs-lookup"><span data-stu-id="bc308-115">The **Test-CsUcwaConference** cmdlet verifies that a pair of test users can schedule, join, and then conduct an online conference using the Unified Communications Web API (UCWA).</span></span> <span data-ttu-id="bc308-116">Dazu verwendet das Cmdlet den lync Server Web Ticket-Dienst, um die beiden Testbenutzer zu authentifizieren und bei lync Server zu registrieren.</span><span class="sxs-lookup"><span data-stu-id="bc308-116">To do this, the cmdlet uses the Lync Server web ticket service to authenticate the two test users and register them with Lync Server.</span></span> <span data-ttu-id="bc308-117">Das Cmdlet startet dann eine Konferenz mit den Anmeldeinformationen des Organisators und fordert den Teilnehmer auf, an der Besprechung teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="bc308-117">The cmdlet then starts a conference using the organizer credentials and invites the participant to join the meeting.</span></span> <span data-ttu-id="bc308-118">Nachdem die Besprechung beigetreten ist, überprüft das Cmdlet " **Test-CsUcwaConference** ", ob die Benutzer die folgenden Aktionen ausführen können: Exchange-Sofortnachrichten und leiten von Pools, trennt die Konferenz und hebt die Registrierung der beiden Testbenutzer auf.</span><span class="sxs-lookup"><span data-stu-id="bc308-118">After the meeting is joined, the **Test-CsUcwaConference** cmdlet verifies that the users can do such things as exchange instant message and conduct pools, then disconnects the conference and unregisters the two test users.</span></span> <span data-ttu-id="bc308-119">Die geplante Konferenz wird auch nach Abschluss des Tests gelöscht.</span><span class="sxs-lookup"><span data-stu-id="bc308-119">The scheduled conference will also be deleted when the test is finished.</span></span>

<span data-ttu-id="bc308-120">Das Cmdlet **Test-CsUcwaConference** kann auch verwendet werden, um zu ermitteln, ob anonyme Benutzer an Online Konferenzen teilnehmen können.</span><span class="sxs-lookup"><span data-stu-id="bc308-120">The **Test-CsUcwaConference** cmdlet can also be used to determine whether anonymous users can join online conferences.</span></span>

<span data-ttu-id="bc308-121">Beachten Sie, dass das Cmdlet **Test-CsUcwaConference** nicht für einen Microsoft lync Server 2010-Pool ausgeführt werden sollte, es sei denn, UCWA wurde in diesem Pool installiert.</span><span class="sxs-lookup"><span data-stu-id="bc308-121">Note that the **Test-CsUcwaConference** cmdlet should not be run against a Microsoft Lync Server 2010 pool unless UCWA was installed on that pool.</span></span> <span data-ttu-id="bc308-122">Wenn UCWA nicht installiert wurde, tritt beim Aufruf des **Test-CsUcwaConference-** Cmdlets ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="bc308-122">If UCWA has not been installed then the call to the **Test-CsUcwaConference** cmdlet will fail.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="bc308-123">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="bc308-123">Running the test</span></span>

<span data-ttu-id="bc308-124">Der in Beispiel 1 gezeigte Befehl überprüft, ob ein paar Testbenutzer an einer UCWA-Konferenz im Pool-ATL-CS-001.litwareinc.com teilnehmen können.</span><span class="sxs-lookup"><span data-stu-id="bc308-124">The command shown in Example 1 verifies that a pair of test users can participate in an UCWA conference on the pool atl-cs-001.litwareinc.com.</span></span> <span data-ttu-id="bc308-125">Beachten Sie, dass dieser Befehl fehlschlägt, wenn Sie für ATL-CS-001.litwareinc.com keine Konfigurationstest Benutzer für die Integritätsüberwachung vordefiniert haben.</span><span class="sxs-lookup"><span data-stu-id="bc308-125">Note that this command will fail if you have not predefined a pair of health monitoring configuration test users for atl-cs-001.litwareinc.com.</span></span>

    Test-CsUcwaConference -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="bc308-126">Die in Beispiel 2 gezeigten Befehle testen die Möglichkeit eines Paars von Benutzern ("litwareinc \\ Pilar und" litwareinc \\ kenmyer), an einer UCWA Konferenz teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="bc308-126">The commands shown in Example 2 test the ability of a pair of users (litwareinc\\pilar and litwareinc\\kenmyer) to participate in an UCWA conference.</span></span> <span data-ttu-id="bc308-127">Dazu wird im ersten Befehl im Beispiel das Get-Credential-Cmdlet verwendet, um ein Windows PowerShell-Befehlszeilen-Schnittstellen Anmeldeinformationsobjekt zu erstellen, das den Namen und das Kennwort des Benutzers Pilar Ackerman enthält.</span><span class="sxs-lookup"><span data-stu-id="bc308-127">To do this, the first command in the example uses the Get-Credential cmdlet to create a Windows PowerShell command-line interface credential object that contains the name and password of the user Pilar Ackerman.</span></span> <span data-ttu-id="bc308-128">(Da der Anmeldename, "litwareinc \\ Pilar, als Parameter enthalten war, erfordert das Dialogfeld Windows PowerShell-Anmeldeinformationen nur, dass der Administrator das Kennwort für das Pilar Ackerman-Konto eingegeben hat.) Das resultierende Credentials-Objekt wird dann in einer Variablen mit dem Namen $cred 1 gespeichert.</span><span class="sxs-lookup"><span data-stu-id="bc308-128">(Because the logon name, litwareinc\\pilar, was included as a parameter, the Windows PowerShell Credential Request dialog box only requires the administrator to enter the password for the Pilar Ackerman account.) The resulting credentials object is then stored in a variable named $cred1.</span></span> <span data-ttu-id="bc308-129">Der zweite Befehl führt dieselbe Aufgabe aus, wobei dieses Mal ein Anmeldeinformationsobjekt für das Ken Myers-Konto zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="bc308-129">The second command does the same thing, this time returning a credential object for the Ken Myer account.</span></span>

<span data-ttu-id="bc308-130">Wenn die beiden Anmeldeinformationsobjekte in der Hand sind, bestimmt der dritte Befehl im Beispiel, ob die beiden Benutzer an einer UCWA-Konferenz teilnehmen können.</span><span class="sxs-lookup"><span data-stu-id="bc308-130">With the two credential objects in hand, the third command in the example determines whether the two users can participate in an UCWA conference.</span></span> <span data-ttu-id="bc308-131">Zum Ausführen dieser Aufgabe wird das Cmdlet **Test-CsUcwaConference** zusammen mit den folgenden Parametern aufgerufen: TargetFqdn (der FQDN des registrierungspools); OrganizerSipAddress (die SIP-Adresse für den Besprechungsorganisator); OrganizerCredential (das Windows PowerShell-Objekt, das die Anmeldeinformationen für denselben Benutzer enthält); ParticipantSipAddress (die SIP-Adresse des anderen Testbenutzers); und ParticipantCredential (das Windows PowerShell-Befehlszeilen-Schnittstellenobjekt, das die Anmeldeinformationen für den anderen Benutzer enthält).</span><span class="sxs-lookup"><span data-stu-id="bc308-131">To run this task, the **Test-CsUcwaConference** cmdlet is called, together with the following parameters: TargetFqdn (the FQDN of the Registrar pool); OrganizerSipAddress (the SIP address for the meeting organizer); OrganizerCredential (the Windows PowerShell object that contains the credentials for this same user); ParticipantSipAddress (the SIP address for the other test user); and ParticipantCredential (the Windows PowerShell command-line interface object that contains the credentials for the other user).</span></span>

    $cred1 = Get-Credential "litwareinc\pilar"
    $cred2 = Get-Credential "litwareinc\kenmyer"
    Test-CsUcwaConference -TargetFqdn atl-cs-001.litwareinc.com -OrganizerSipAddress "sip:pilar@litwareinc.com" -OrganizerCredential $cred1 -ParticipantSipAddress "sip:kenmyer@litwareinc.com" -ParticipantCredential $cred2

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="bc308-132">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="bc308-132">Determining success or failure</span></span>

<span data-ttu-id="bc308-133">Wenn Conferencing richtig konfiguriert ist, erhalten Sie eine ähnliche Ausgabe, wobei die Eigenschaft Ergebnis als erfolgreich markiert ist **:**</span><span class="sxs-lookup"><span data-stu-id="bc308-133">If conferencing is correctly configured, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="bc308-134">Ziel-FQDN: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="bc308-134">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="bc308-135">Ziel-URI: https://LyncTest-SE. LyncTest. SelfHost. Corp.</span><span class="sxs-lookup"><span data-stu-id="bc308-135">Target Uri : https:// LyncTest-SE.LyncTest.SelfHost.Corp.</span></span>

<span data-ttu-id="bc308-136">Microsoft.com:443/CertProv/CertProvisiongService.svc</span><span class="sxs-lookup"><span data-stu-id="bc308-136">Microsoft.com:443/CertProv/CertProvisiongService.svc</span></span>

<span data-ttu-id="bc308-137">Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="bc308-137">Result : Success</span></span>

<span data-ttu-id="bc308-138">Latenz: 00:00:14.9862716</span><span class="sxs-lookup"><span data-stu-id="bc308-138">Latency : 00:00:14.9862716</span></span>

<span data-ttu-id="bc308-139">Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="bc308-139">Error Message :</span></span>

<span data-ttu-id="bc308-140">Diagnose</span><span class="sxs-lookup"><span data-stu-id="bc308-140">Diagnosis :</span></span>

<span data-ttu-id="bc308-141">Wenn die angegebenen Benutzer keine Konferenz verwenden können, wird das Ergebnis als **Fehler** angezeigt, und weitere Informationen werden in den Eigenschaften Fehler und Diagnose aufgezeichnet:</span><span class="sxs-lookup"><span data-stu-id="bc308-141">If the specified users can't use conferencing, the Result will be shown as **Failure**, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="bc308-142">Warnung: Fehler beim Lesen der Registrierungsstellen-Portnummer für die angegebene vollqualifizierte</span><span class="sxs-lookup"><span data-stu-id="bc308-142">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="bc308-143">Domänenname (FQDN).</span><span class="sxs-lookup"><span data-stu-id="bc308-143">domain name (FQDN).</span></span> <span data-ttu-id="bc308-144">Verwenden der standardmäßigen Registrierungs Portnummer</span><span class="sxs-lookup"><span data-stu-id="bc308-144">Using default Registrar port number.</span></span> <span data-ttu-id="bc308-145">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="bc308-145">Exception:</span></span>

<span data-ttu-id="bc308-146">System. InvalidOperationException: kein übereinstimmender Cluster in der Topologie gefunden.</span><span class="sxs-lookup"><span data-stu-id="bc308-146">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="bc308-147">am</span><span class="sxs-lookup"><span data-stu-id="bc308-147">at</span></span>

<span data-ttu-id="bc308-148">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="bc308-148">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="bc308-149">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="bc308-149">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="bc308-150">Test-CsUcwaConference: Es wurde kein Testbenutzer zugewiesen</span><span class="sxs-lookup"><span data-stu-id="bc308-150">Test-CsUcwaConference : There is no test user assigned for</span></span>

<span data-ttu-id="bc308-151">\[LyncTest.SelfHost.Corp.Microsoft.com \] .</span><span class="sxs-lookup"><span data-stu-id="bc308-151">\[LyncTest.SelfHost.Corp.Microsoft.com\].</span></span> <span data-ttu-id="bc308-152">Überprüfen Sie die Benutzerkonfiguration testen.</span><span class="sxs-lookup"><span data-stu-id="bc308-152">Verify test user configuration.</span></span>

<span data-ttu-id="bc308-153">Zeile: 1 Zeichen: 1</span><span class="sxs-lookup"><span data-stu-id="bc308-153">At line:1 char:1</span></span>

<span data-ttu-id="bc308-154">\+ Test-CsUcwaConference-TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="bc308-154">\+ Test-CsUcwaConference -TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"</span></span>

\+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

<span data-ttu-id="bc308-155">\+ CategoryInfo: ResourceUnavailable: (:) \[ Test-CsUcwaConference\]</span><span class="sxs-lookup"><span data-stu-id="bc308-155">\+ CategoryInfo : ResourceUnavailable: (:) \[Test-CsUcwaConference\]</span></span>

<span data-ttu-id="bc308-156">, InvalidOperationException</span><span class="sxs-lookup"><span data-stu-id="bc308-156">, InvalidOperationException</span></span>

<span data-ttu-id="bc308-157">\+ FullyQualifiedErrorId: NotFoundTestUsers, Microsoft. RTC. Management. Synth</span><span class="sxs-lookup"><span data-stu-id="bc308-157">\+ FullyQualifiedErrorId : NotFoundTestUsers,Microsoft.Rtc.Management.Synth</span></span>

<span data-ttu-id="bc308-158">eticTransactions.TestUcwaConferenceCmdlet</span><span class="sxs-lookup"><span data-stu-id="bc308-158">eticTransactions.TestUcwaConferenceCmdlet</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="bc308-159">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="bc308-159">Reasons why the test might have failed</span></span>

<span data-ttu-id="bc308-160">Nachfolgend finden Sie einige häufige Gründe, warum **Test-CsUcwaConference** möglicherweise fehlschlägt:</span><span class="sxs-lookup"><span data-stu-id="bc308-160">Here are some common reasons why **Test-CsUcwaConference** might fail:</span></span>

  - <span data-ttu-id="bc308-161">Es wurde ein falscher Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="bc308-161">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="bc308-162">Wenn die optionalen Parameter verwendet werden, müssen Sie ordnungsgemäß konfiguriert sein, oder der Test schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="bc308-162">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="bc308-163">Führen Sie den Befehl ohne die optionalen Parameter erneut aus, und überprüfen Sie, ob dies erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="bc308-163">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="bc308-164">Die Möglichkeit zum Durchführen einer Konferenz hängt von der konferenzrichtlinie ab, die dem Benutzer zugewiesen wurde, der die Konferenz organisiert hat (im Fall des **Test-CsUcwaConference-** Cmdlets, bei dem es sich um den Absender handelt).</span><span class="sxs-lookup"><span data-stu-id="bc308-164">The ability to conduct a conference depends on the conferencing policy that has been assigned to the user who organized the conference (in the case of the **Test-CsUcwaConference** cmdlet, that is the "sender").</span></span> <span data-ttu-id="bc308-165">Wenn es dem Organisator nicht gestattet ist, in seiner Besprechung kollaborative Aktivitäten einzubeziehen (Wenn beispielsweise die EnableDataCollaboration-Eigenschaft der konferenzrichtlinie auf "false" festgelegt ist), schlägt das **Test-CsUcwaConference-** Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="bc308-165">If the organizer is not allowed to include collaborative activities in his or her meeting (for example, if his or her conferencing policy has the EnableDataCollaboration property set to False) then the **Test-CsUcwaConference** cmdlet will fail.</span></span>

  - <span data-ttu-id="bc308-166">Dieser Befehl schlägt fehl, wenn der Edgeserver falsch konfiguriert oder noch nicht bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="bc308-166">This command will fail if the Edge Server is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="bc308-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc308-167">See Also</span></span>


[<span data-ttu-id="bc308-168">Test-CsASConference</span><span class="sxs-lookup"><span data-stu-id="bc308-168">Test-CsASConference</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsASConference)  
[<span data-ttu-id="bc308-169">Test-CsDataConference</span><span class="sxs-lookup"><span data-stu-id="bc308-169">Test-CsDataConference</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsDataConference)  
[<span data-ttu-id="bc308-170">Test-CsAVConference</span><span class="sxs-lookup"><span data-stu-id="bc308-170">Test-CsAVConference</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference)  
  

<span data-ttu-id="bc308-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bc308-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

