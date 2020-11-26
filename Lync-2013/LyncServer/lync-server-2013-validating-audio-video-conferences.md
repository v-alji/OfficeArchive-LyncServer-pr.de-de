---
title: 'Lync Server 2013: Überprüfen von Audio-und Videokonferenzen'
description: 'Lync Server 2013: Überprüfen von Audio-und Videokonferenzen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating audio/video conferences
ms:assetid: 6c8c422a-d501-42cb-820b-b002f9b2250b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720915(v=OCS.15)
ms:contentKeyID: 63969615
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad12611e928a64b934252ec21c18b98366e0912b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443489"
---
# <a name="validating-audiovideo-conferences-in-lync-server-2013"></a><span data-ttu-id="9a38b-103">Überprüfen von Audio-und Videokonferenzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9a38b-103">Validating audio/video conferences in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9a38b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9a38b-104">

<span> </span></span></span>

<span data-ttu-id="9a38b-105">_**Letztes Änderungsdatum des Themas:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="9a38b-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a38b-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="9a38b-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="9a38b-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="9a38b-107">Daily</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9a38b-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="9a38b-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="9a38b-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9a38b-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9a38b-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="9a38b-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="9a38b-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="9a38b-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="9a38b-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsAVConference-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="9a38b-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsAVConference cmdlet.</span></span> <span data-ttu-id="9a38b-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="9a38b-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsAVConference&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="9a38b-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9a38b-114">Description</span></span>

<span data-ttu-id="9a38b-115">Das Test-CsAVConference-Cmdlet überprüft, ob zwei Testbenutzer an einer Audio/Video-Konferenz (A/V) teilnehmen können.</span><span class="sxs-lookup"><span data-stu-id="9a38b-115">The Test-CsAVConference cmdlet checks whether two test users can participate in an audio/video (A/V) conference.</span></span> <span data-ttu-id="9a38b-116">Wenn das Cmdlet ausgeführt wird, sind die beiden Benutzer am System angemeldet.</span><span class="sxs-lookup"><span data-stu-id="9a38b-116">When the cmdlet runs, the two users are logged on to the system.</span></span> <span data-ttu-id="9a38b-117">Nachdem Sie sich erfolgreich angemeldet haben, erstellt der erste Benutzer eine A/V-Konferenz und wartet dann auf die Teilnahme des zweiten Benutzers an dieser Konferenz.</span><span class="sxs-lookup"><span data-stu-id="9a38b-117">After they face successfully logged on, the first user creates an A/V conference, and then waits for the second user to join that conference.</span></span> <span data-ttu-id="9a38b-118">Nach einem kurzen Datenaustausch wird die Konferenz gelöscht, und die beiden Testbenutzer werden abgemeldet.</span><span class="sxs-lookup"><span data-stu-id="9a38b-118">After a brief exchange of data, the conference is deleted and the two tests users are logged off.</span></span>

<span data-ttu-id="9a38b-119">Beachten Sie, dass Test-CsAVConference keine eigentliche A/V-Konferenz zwischen den beiden Testbenutzern durchführt.</span><span class="sxs-lookup"><span data-stu-id="9a38b-119">Note that Test-CsAVConference does not conduct an actual A/V conference between the two test users.</span></span> <span data-ttu-id="9a38b-120">Stattdessen überprüft das Cmdlet, ob die beiden Benutzer alle erforderlichen Verbindungen zum Durchführen einer solchen Konferenz vornehmen können.</span><span class="sxs-lookup"><span data-stu-id="9a38b-120">Instead, the cmdlet verifies that the two users can make all the connections necessary to conduct such a conference.</span></span>

<span data-ttu-id="9a38b-121">Weitere Beispiele für diesen Befehl finden Sie unter [Test-CsAVConference](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference).</span><span class="sxs-lookup"><span data-stu-id="9a38b-121">Further examples for this command can be found at [Test-CsAVConference](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference).</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="9a38b-122">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="9a38b-122">Running the test</span></span>

<span data-ttu-id="9a38b-123">Das Test-CsAVConference-Cmdlet kann entweder mit einem Paar vorkonfigurierter Testkonten ausgeführt werden (siehe Einrichten von Testkonten zum Ausführen von lync Server-Tests) oder der Konten von zwei Benutzern, die für lync Server aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="9a38b-123">The Test-CsAVConference cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="9a38b-124">Um diese Prüfung mit Testkonten auszuführen, müssen Sie lediglich den FQDN des zu testenden lync-Server Pools angeben.</span><span class="sxs-lookup"><span data-stu-id="9a38b-124">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="9a38b-125">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9a38b-125">For example:</span></span>

    Test-CsAVConference -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="9a38b-126">Damit diese Überprüfung mit tatsächlichen Benutzerkonten ausgeführt werden kann, müssen Sie für jedes Konto zwei Windows PowerShell-Anmeldeinformationsobjekte (Objekte, die den Kontonamen und das Kennwort enthalten) erstellen.</span><span class="sxs-lookup"><span data-stu-id="9a38b-126">To run this check using actual user accounts, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="9a38b-127">Sie müssen dann diese Anmeldeinformationsobjekte und die SIP-Adressen der beiden Konten einbeziehen, wenn Sie Test-CsAVConference aufrufen:</span><span class="sxs-lookup"><span data-stu-id="9a38b-127">You must then include those credentials objects and the SIP addresses of the two accounts when they call Test-CsAVConference:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsAVConference -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

<span data-ttu-id="9a38b-128">Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsAVConference](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference) .</span><span class="sxs-lookup"><span data-stu-id="9a38b-128">For more information, see the Help documentation for the [Test-CsAVConference](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="9a38b-129">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="9a38b-129">Determining Success or Failure</span></span>

<span data-ttu-id="9a38b-130">Wenn die angegebenen Benutzer eine A/V-Konferenz erfolgreich abschließen können, erhalten Sie eine ähnliche Ausgabe, wobei die Eigenschaft Ergebnis als erfolgreich markiert ist **:**</span><span class="sxs-lookup"><span data-stu-id="9a38b-130">If the specified users can successfully complete an A/V conference, you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="9a38b-131">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="9a38b-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="9a38b-132">Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="9a38b-132">Result : Success</span></span>

<span data-ttu-id="9a38b-133">Latenz: 00:00:02.6841765</span><span class="sxs-lookup"><span data-stu-id="9a38b-133">Latency : 00:00:02.6841765</span></span>

<span data-ttu-id="9a38b-134">Fehler</span><span class="sxs-lookup"><span data-stu-id="9a38b-134">Error :</span></span>

<span data-ttu-id="9a38b-135">Diagnose</span><span class="sxs-lookup"><span data-stu-id="9a38b-135">Diagnosis :</span></span>

<span data-ttu-id="9a38b-136">Wenn die Benutzer die Konferenz nicht abschließen können, wird das Ergebnis als Fehler angezeigt, und weitere Informationen werden in den Eigenschaften Fehler und Diagnose aufgezeichnet:</span><span class="sxs-lookup"><span data-stu-id="9a38b-136">If the users can not complete the conference, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="9a38b-137">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="9a38b-137">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="9a38b-138">Ergebnis: Fehler</span><span class="sxs-lookup"><span data-stu-id="9a38b-138">Result : Failure</span></span>

<span data-ttu-id="9a38b-139">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9a38b-139">Latency : 00:00:00</span></span>

<span data-ttu-id="9a38b-140">Fehler: 404, nicht gefunden</span><span class="sxs-lookup"><span data-stu-id="9a38b-140">Error : 404, Not Found</span></span>

<span data-ttu-id="9a38b-141">Diagnose: errorCode = 4005, Source = ATL-CS-001.litwareinc.com,</span><span class="sxs-lookup"><span data-stu-id="9a38b-141">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="9a38b-142">Reason = Ziel-URI ist entweder für SIP nicht aktiviert oder nicht</span><span class="sxs-lookup"><span data-stu-id="9a38b-142">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="9a38b-143">existieren.</span><span class="sxs-lookup"><span data-stu-id="9a38b-143">exist.</span></span>

<span data-ttu-id="9a38b-144">Microsoft. RTC. Signalisierungs-DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="9a38b-144">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="9a38b-145">In der vorherigen Ausgabe wird beispielsweise festgestellt, dass der Test fehlgeschlagen ist, weil mindestens eines der beiden Benutzerkonten ungültig war, weil das Konto nicht vorhanden ist oder weil das Konto für lync Server nicht aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="9a38b-145">For example, the previous output states that the test failed because at least one of the two user accounts was not valid, either because the account does not exist or because the account has not been enabled for Lync Server.</span></span> <span data-ttu-id="9a38b-146">Sie können überprüfen, ob die beiden Testkonten vorhanden sind und ob Sie für lync Server aktiviert wurden, indem Sie einen Befehl wie den folgenden ausführen:</span><span class="sxs-lookup"><span data-stu-id="9a38b-146">You can verify the existence of the two test accounts, and whether they were enabled for Lync Server, by running a command similar to the following:</span></span>

    "sip:kenmyer@litwareinc.com","sip:davidlongmire@litwareinc.com" | Get-CsUser | Select-Object SipAddress, enabled

<span data-ttu-id="9a38b-147">Wenn Test-CsAVConference fehlschlägt, möchten Sie möglicherweise den Test erneut ausführen, wobei dieser Zeitpunkt einschließlich des Verbose-Parameters lautet:</span><span class="sxs-lookup"><span data-stu-id="9a38b-147">If Test-CsAVConference fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsAVConference -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="9a38b-148">Wenn der Verbose-Parameter enthalten ist Test-CsAVConference gibt eine Schritt-für-Schritt-Konto für jede Aktion zurück, die versucht wurde, als die Möglichkeit der angegebenen Benutzer zur Teilnahme an einer AV-Konferenz geprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="9a38b-148">When the Verbose parameter is included Test-CsAVConference will return a step-by-step account of each action it tried when it checked the ability of the specified users to participate in an AV conference.</span></span> <span data-ttu-id="9a38b-149">Nehmen wir beispielsweise an, dass Ihr Test fehlschlägt und Sie die folgende Diagnose erhalten:</span><span class="sxs-lookup"><span data-stu-id="9a38b-149">For example, suppose that your test fails and you receive the following Diagnosis:</span></span>

<span data-ttu-id="9a38b-150">ErrorCode = 1008, Source = accessproxy. "litwareinc. com; Reason = DNS-SRV-Eintrag konnte nicht aufgelöst werden</span><span class="sxs-lookup"><span data-stu-id="9a38b-150">ErrorCode=1008,Source=accessproxy.litwareinc.com,Reason=Unable to resolve DNS SRV record</span></span>

<span data-ttu-id="9a38b-151">Wenn Sie den Test mit dem Verbose-Parameter erneut ausführen, beinhalten die zurückgegebenen schrittweisen Informationen eine Ausgabe, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="9a38b-151">If you rerun the test using the Verbose parameter, the step-by-step information returned will include output similar to this:</span></span>

<span data-ttu-id="9a38b-152">Ausführlich: die Aktivität "registrieren" wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="9a38b-152">VERBOSE: 'Register' activity started.</span></span>

<span data-ttu-id="9a38b-153">Registrierungsanfrage wird gesendet:</span><span class="sxs-lookup"><span data-stu-id="9a38b-153">Sending Registration request:</span></span>

<span data-ttu-id="9a38b-154">Ziel-FQDN = ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="9a38b-154">Target Fqdn = atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="9a38b-155">SIP-Adresse des Benutzers = SIP:davidlongmire@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="9a38b-155">User Sip Address = sip:davidlongmire@litwareinc.com</span></span>

<span data-ttu-id="9a38b-156">Registrar Port = 5061.</span><span class="sxs-lookup"><span data-stu-id="9a38b-156">Registrar Port = 5061.</span></span>

<span data-ttu-id="9a38b-157">Auth-Typ "vertrauenswürdig" ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="9a38b-157">Auth Type 'Trusted' is selected.</span></span>

<span data-ttu-id="9a38b-158">Die Aktivität "registrieren" wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="9a38b-158">'Register' activity started.</span></span>

<span data-ttu-id="9a38b-159">Registrierungsanfrage wird gesendet:</span><span class="sxs-lookup"><span data-stu-id="9a38b-159">Sending Registration request:</span></span>

<span data-ttu-id="9a38b-160">Ziel-FQDN = ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="9a38b-160">Target Fqdn = atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="9a38b-161">SIP-Adresse des Benutzers = SIP:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="9a38b-161">User Sip Address = sip:kenmyer@litwareinc.com</span></span>

<span data-ttu-id="9a38b-162">Registrar Port = 5061.</span><span class="sxs-lookup"><span data-stu-id="9a38b-162">Registrar Port = 5061.</span></span>

<span data-ttu-id="9a38b-163">Auth-Typ "vertrauenswürdig" ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="9a38b-163">Auth Type 'Trusted' is selected.</span></span>

<span data-ttu-id="9a38b-164">Eine Ausnahme "der Endpunkt konnte nicht registriert werden.</span><span class="sxs-lookup"><span data-stu-id="9a38b-164">An exception 'The endpoint was unable to register.</span></span> <span data-ttu-id="9a38b-165">Lesen Sie den ErrorCode aus bestimmten Gründen.</span><span class="sxs-lookup"><span data-stu-id="9a38b-165">See the ErrorCode for specific reason.'</span></span> <span data-ttu-id="9a38b-166">während des Workflows aufgetreten</span><span class="sxs-lookup"><span data-stu-id="9a38b-166">occurred during Workflow</span></span>

<span data-ttu-id="9a38b-167">Die letzte Zeile in dieser Ausgabe gibt an, dass der Benutzer SIP:kenmyer@litwareinc.com sich nicht bei lync Server registrieren konnte.</span><span class="sxs-lookup"><span data-stu-id="9a38b-167">The last line in that output indicates that the user sip:kenmyer@litwareinc.com was unable to register with Lync Server.</span></span> <span data-ttu-id="9a38b-168">Das bedeutet, dass Sie überprüfen sollten, ob die SIP-Adresse SIP:kenmyer@litwareinc.com gültig ist und dass der zugeordnete Benutzer für lync Server aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9a38b-168">That means that you should verify that the SIP address sip:kenmyer@litwareinc.com is valid, and that the associated user is enabled for Lync Server.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="9a38b-169">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="9a38b-169">Reasons why the test might have failed</span></span>

<span data-ttu-id="9a38b-170">Im folgenden finden Sie einige häufige Gründe, warum Test-CsAVConference fehlschlagen kann:</span><span class="sxs-lookup"><span data-stu-id="9a38b-170">Here are some common reasons why Test-CsAVConference might fail:</span></span>

  - <span data-ttu-id="9a38b-171">Sie haben ein ungültiges Benutzerkonto angegeben.</span><span class="sxs-lookup"><span data-stu-id="9a38b-171">You specified a user account that is not valid.</span></span> <span data-ttu-id="9a38b-172">Sie können überprüfen, ob ein Benutzerkonto vorhanden ist, indem Sie einen Befehl wie den folgenden ausführen:</span><span class="sxs-lookup"><span data-stu-id="9a38b-172">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="9a38b-173">Das Benutzerkonto ist gültig, das Konto ist derzeit aber für lync Server nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="9a38b-173">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="9a38b-174">Führen Sie einen Befehl ähnlich der folgenden aus, um zu überprüfen, ob ein Benutzerkonto für lync Server aktiviert ist:</span><span class="sxs-lookup"><span data-stu-id="9a38b-174">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="9a38b-175">Wenn die Enabled-Eigenschaft auf false festgelegt ist, bedeutet dies, dass der Benutzer zurzeit nicht für lync Server aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="9a38b-175">If the Enabled property is set to False that means that the user is currently not enabled for Lync Server.</span></span>

<span data-ttu-id="9a38b-176"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9a38b-176"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

