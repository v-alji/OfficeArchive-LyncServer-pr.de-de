---
title: 'Lync Server 2013: Testen der Gruppen-Chatfunktion'
description: 'Lync Server 2013: Testen der Fähigkeit, Gruppen-Chat zu durchführen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to do group IM
ms:assetid: ca5545bc-51ac-490f-b96b-917bb742ad04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743839(v=OCS.15)
ms:contentKeyID: 63969652
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f6988a0c1a7ba569f7b4da098ae741beab5e14fa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441102"
---
# <a name="testing-ability-to-do-group-im-in-lync-server-2013"></a><span data-ttu-id="cfa37-103">Testen der Fähigkeit zum Gruppieren von Chatnachrichten in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cfa37-103">Testing ability to do group IM in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cfa37-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cfa37-104">

<span> </span></span></span>

<span data-ttu-id="cfa37-105">_**Letztes Änderungsdatum des Themas:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="cfa37-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cfa37-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="cfa37-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="cfa37-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="cfa37-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cfa37-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="cfa37-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="cfa37-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="cfa37-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cfa37-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="cfa37-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="cfa37-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="cfa37-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="cfa37-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsGroupIM-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="cfa37-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsGroupIM cmdlet.</span></span> <span data-ttu-id="cfa37-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="cfa37-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsGroupIM&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="cfa37-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cfa37-114">Description</span></span>

<span data-ttu-id="cfa37-115">Das Test-CsGroupIM-Cmdlet überprüft, ob Benutzer in Ihrer Organisation Gruppen-Chatsitzungen durchführen können.</span><span class="sxs-lookup"><span data-stu-id="cfa37-115">The Test-CsGroupIM cmdlet verifies that users in your organization can conduct group instant messaging sessions.</span></span> <span data-ttu-id="cfa37-116">Wenn Sie Test-CsGroupIM ausführen, versucht das Cmdlet, ein paar Test Benutzer mit lync Server zu signieren.</span><span class="sxs-lookup"><span data-stu-id="cfa37-116">When you run Test-CsGroupIM, the cmdlet attempts to sign in a pair of test users to Lync Server.</span></span> <span data-ttu-id="cfa37-117">Wenn Sie erfolgreich sind, erstellt Test-CsGroupIM eine neue Konferenz mit dem ersten Testbenutzer und fordert den zweiten Benutzer auf, an der Konferenz teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="cfa37-117">If successful, Test-CsGroupIM creates a new conference using the first test user, then invites the second user to join the conference.</span></span> <span data-ttu-id="cfa37-118">Nach einem Austausch von Nachrichten werden beide Benutzer vom System getrennt.</span><span class="sxs-lookup"><span data-stu-id="cfa37-118">After an exchange of messages, both users are then disconnected from the system.</span></span> <span data-ttu-id="cfa37-119">Beachten Sie, dass dies alles ohne Benutzerinteraktion und ohne Auswirkungen auf tatsächliche Benutzer geschieht.</span><span class="sxs-lookup"><span data-stu-id="cfa37-119">Note that all of this happens without any user interaction, and without affecting any actual users.</span></span> <span data-ttu-id="cfa37-120">Nehmen wir beispielsweise an, dass das Test Konto SIP:kenmyer@litwareinc.com einem echten Benutzer entspricht, der ein echtes lync Server-Konto hat.</span><span class="sxs-lookup"><span data-stu-id="cfa37-120">For example, suppose that the test account sip:kenmyer@litwareinc.com corresponds to a real user who has a real Lync Server account.</span></span> <span data-ttu-id="cfa37-121">In diesem Fall wird der Test ohne Unterbrechung des echten Ken Myers durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="cfa37-121">In that case, the test will be conducted without any disruption to the real Ken Myer.</span></span> <span data-ttu-id="cfa37-122">Auch wenn sich das Ken Myers Test-Konto vom System abmeldet, bleibt die Person beispielsweise angemeldet.</span><span class="sxs-lookup"><span data-stu-id="cfa37-122">For example, even when the Ken Myer test account logs off from the system, Ken Myer the person will remain logged on.</span></span> <span data-ttu-id="cfa37-123">Ebenso erhält der wirkliche Ken Myers keine Einladung zur Teilnahme an der Konferenz.</span><span class="sxs-lookup"><span data-stu-id="cfa37-123">Likewise, the real Ken Myer won't receive an invitation to join the conference.</span></span> <span data-ttu-id="cfa37-124">Diese Einladung wird an das Testkonto gesendet und von diesem akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="cfa37-124">That invitation will be sent to, and accepted by, the test account.</span></span>

<span data-ttu-id="cfa37-125">Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) .</span><span class="sxs-lookup"><span data-stu-id="cfa37-125">For more information, see the Help documentation for the [Test-CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="cfa37-126">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="cfa37-126">Running the test</span></span>

<span data-ttu-id="cfa37-127">Das Test-CsGroupIM-Cmdlet kann entweder mit einem Paar vorkonfigurierter Testkonten ausgeführt werden (siehe Einrichten von Testkonten zum Ausführen von lync Server-Tests) oder der Konten von zwei Benutzern, die für lync Server aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="cfa37-127">The Test-CsGroupIM cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="cfa37-128">Um diese Prüfung mit Testkonten auszuführen, müssen Sie lediglich den FQDN des zu testenden lync-Server Pools angeben.</span><span class="sxs-lookup"><span data-stu-id="cfa37-128">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="cfa37-129">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="cfa37-129">For example:</span></span>

    Test-CsGroupIM -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="cfa37-130">Damit diese Überprüfung mit tatsächlichen Benutzerkonten ausgeführt werden kann, müssen Sie für jedes Konto zwei Anmeldedaten Objekte der lync Server-Verwaltungsshell (Objekte, die den Kontonamen und das Kennwort enthalten) erstellen.</span><span class="sxs-lookup"><span data-stu-id="cfa37-130">To run this check using actual user accounts, you must create two Lync Server Management Shell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="cfa37-131">Sie müssen dann diese Anmeldeinformationsobjekte und die SIP-Adressen der beiden Konten einbeziehen, wenn Sie Test-CsGroupIM aufrufen:</span><span class="sxs-lookup"><span data-stu-id="cfa37-131">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsGroupIM:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsGroupIm -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

<span data-ttu-id="cfa37-132">Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) .</span><span class="sxs-lookup"><span data-stu-id="cfa37-132">For more information, see the Help documentation for the [Test-CsGroupIM](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupIM) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="cfa37-133">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="cfa37-133">Determining Success or Failure</span></span>

<span data-ttu-id="cfa37-134">Wenn die beiden Benutzer eine Gruppen-Chatsitzung durchführen können, erhalten Sie eine ähnliche Ausgabe, wobei die Ergebniseigenschaft als erfolgreich markiert ist **:**</span><span class="sxs-lookup"><span data-stu-id="cfa37-134">If the two users can complete a group instant messaging session, you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="cfa37-135">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="cfa37-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="cfa37-136">Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="cfa37-136">Result : Success</span></span>

<span data-ttu-id="cfa37-137">Latenz: 00:00:06.3812203</span><span class="sxs-lookup"><span data-stu-id="cfa37-137">Latency : 00:00:06.3812203</span></span>

<span data-ttu-id="cfa37-138">Fehler</span><span class="sxs-lookup"><span data-stu-id="cfa37-138">Error :</span></span>

<span data-ttu-id="cfa37-139">Diagnose</span><span class="sxs-lookup"><span data-stu-id="cfa37-139">Diagnosis :</span></span>

<span data-ttu-id="cfa37-140">Wenn die beiden Benutzer nicht in der Lage sind, die Chat-Sitzung abzuschließen, wird das Ergebnis als Fehler angezeigt, und weitere Informationen werden in den Eigenschaften Fehler und Diagnose aufgezeichnet:</span><span class="sxs-lookup"><span data-stu-id="cfa37-140">If the two users can't able to complete the instant messaging session, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="cfa37-141">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="cfa37-141">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="cfa37-142">Ergebnis: Fehler</span><span class="sxs-lookup"><span data-stu-id="cfa37-142">Result : Failure</span></span>

<span data-ttu-id="cfa37-143">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="cfa37-143">Latency : 00:00:00</span></span>

<span data-ttu-id="cfa37-144">Fehler: 404, nicht gefunden</span><span class="sxs-lookup"><span data-stu-id="cfa37-144">Error : 404, Not Found</span></span>

<span data-ttu-id="cfa37-145">Diagnose: errorCode = 4005, Source = ATL-CS-001.litwareinc.com,</span><span class="sxs-lookup"><span data-stu-id="cfa37-145">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="cfa37-146">Reason = Ziel-URI ist entweder für SIP nicht aktiviert oder nicht</span><span class="sxs-lookup"><span data-stu-id="cfa37-146">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="cfa37-147">existieren.</span><span class="sxs-lookup"><span data-stu-id="cfa37-147">exist.</span></span>

<span data-ttu-id="cfa37-148">Microsoft. RTC. Signalisierungs-DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="cfa37-148">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="cfa37-149">In der vorherigen Ausgabe wird angegeben, dass der Test fehlgeschlagen ist, weil mindestens eines der Testkonten ungültig war, weil das Konto nicht vorhanden ist oder der Benutzer nicht für lync Server aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="cfa37-149">The previous output states that the test failed because at least one of the test accounts was not valid, either because the account does not exist or because the user has not been enabled for Lync Server.</span></span> <span data-ttu-id="cfa37-150">Sie können überprüfen, ob das Konto vorhanden ist, und ob das Konto für nm-OCS-14-3rd aktiviert wurde, indem Sie einen ähnlichen Befehl wie den folgenden ausführen:</span><span class="sxs-lookup"><span data-stu-id="cfa37-150">You can verify the account exists, and whether or not the account has been enabled for nm-ocs-14-3rd by running a command similar to this:</span></span>

    "Ken Myer", "David Longmire" | Get-CsUser | Select-Object SipAddress, Enabled

<span data-ttu-id="cfa37-151">Wenn Test-CsGroupIM fehlschlägt, möchten Sie möglicherweise den Test erneut ausführen, wobei dieser Zeitpunkt einschließlich des Verbose-Parameters lautet:</span><span class="sxs-lookup"><span data-stu-id="cfa37-151">If Test-CsGroupIM fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsGroupIM -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="cfa37-152">Wenn der Verbose-Parameter enthalten ist, gibt Test-CsGroupIM eine Schritt-für-Schritt-Konto für jede Aktion zurück, die versucht wurde, als Sie die Möglichkeit der angegebenen Benutzer zur Teilnahme an einer Gruppen-Chatsitzung überprüft hat.</span><span class="sxs-lookup"><span data-stu-id="cfa37-152">When the Verbose parameter is included, Test-CsGroupIM will return a step-by-step account of each action it tried when it checked the ability of the specified users to participate in a group instant messaging sessions.</span></span> <span data-ttu-id="cfa37-153">Wenn Ihr Test beispielsweise fehlschlägt und Ihnen mitgeteilt wird, dass ein oder mehrere Benutzerkonten ungültig sind, können Sie den Test mit dem Verbose-Parameter erneut ausführen und feststellen, welches Benutzerkonto ungültig ist:</span><span class="sxs-lookup"><span data-stu-id="cfa37-153">For example, if your test fails and you are told that one or more of the user accounts is not valid, you can rerun the test using the Verbose parameter and determine which user account is not valid:</span></span>

<span data-ttu-id="cfa37-154">Registrierungsanfrage wird gesendet:</span><span class="sxs-lookup"><span data-stu-id="cfa37-154">Sending Registration request:</span></span>

 <span data-ttu-id="cfa37-155">Ziel-FQDN = ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="cfa37-155">Target Fqdn      = atl-cs-001.litwareinc.com</span></span>

 <span data-ttu-id="cfa37-156">SIP-Adresse des Benutzers = SIP:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="cfa37-156">User SIP Address = sip:kenmyer@litwareinc.com</span></span>

 <span data-ttu-id="cfa37-157">Port registrieren = 5061</span><span class="sxs-lookup"><span data-stu-id="cfa37-157">Register Port    = 5061</span></span>

<span data-ttu-id="cfa37-158">Auth-Typ "IWA" ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="cfa37-158">Auth type 'IWA' is selected.</span></span>

<span data-ttu-id="cfa37-159">Eine Ausnahme "die Anmeldung wurde abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="cfa37-159">An exception 'The log on was denied.</span></span> <span data-ttu-id="cfa37-160">Überprüfen Sie, ob die richtigen Anmeldeinformationen verwendet werden und das Konto aktiv ist. "</span><span class="sxs-lookup"><span data-stu-id="cfa37-160">Check that the correct credentials are being used and the account is active'</span></span>

<span data-ttu-id="cfa37-161">Wie Sie sehen können, war in diesem Beispiel der Benutzer, der die SIP-Adresse SIP:kenmyer@litwareinc.com, nicht in der Lage, sich anzumelden.</span><span class="sxs-lookup"><span data-stu-id="cfa37-161">As you can see, in this example the user who has the SIP address sip:kenmyer@litwareinc.com was not able to log on.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="cfa37-162">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="cfa37-162">Reasons why the test might have failed</span></span>

<span data-ttu-id="cfa37-163">Im folgenden finden Sie einige häufige Gründe, warum Test-CsGroupIM fehlschlagen kann:</span><span class="sxs-lookup"><span data-stu-id="cfa37-163">Here are some common reasons why Test-CsGroupIM might fail:</span></span>

  - <span data-ttu-id="cfa37-164">Sie haben ein falsches Benutzerkonto angegeben.</span><span class="sxs-lookup"><span data-stu-id="cfa37-164">You specified an incorrect user account.</span></span> <span data-ttu-id="cfa37-165">Sie können überprüfen, ob ein Benutzerkonto vorhanden ist, indem Sie einen Befehl wie den folgenden ausführen:</span><span class="sxs-lookup"><span data-stu-id="cfa37-165">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="cfa37-166">Das Benutzerkonto ist gültig, das Konto ist derzeit aber für lync Server nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cfa37-166">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="cfa37-167">Um zu überprüfen, ob ein Benutzerkonto für lync Server aktiviert war, führen Sie einen Befehl ähnlich der folgenden aus:</span><span class="sxs-lookup"><span data-stu-id="cfa37-167">To verify that a user account was enabled for Lync Server, run a command similar to the following:</span></span>
    
    <span data-ttu-id="cfa37-168">Get-CsUser "SIP:kenmyer@litwareinc.com" | Select-Object aktiviert</span><span class="sxs-lookup"><span data-stu-id="cfa37-168">Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled</span></span>
    
    <span data-ttu-id="cfa37-169">Wenn die Enabled-Eigenschaft auf false festgelegt ist, bedeutet dies, dass der Benutzer zurzeit nicht für lync Server aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="cfa37-169">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="cfa37-170">Der Instant Messaging-Dienst ist möglicherweise nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cfa37-170">The instant messaging service might not be available.</span></span> <span data-ttu-id="cfa37-171">Mit lync Server können Sie das System so konfigurieren, dass Sofortnachrichten nicht verfügbar sind, wenn auf die Archivierungsdatenbank nicht zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="cfa37-171">With Lync Server, you can configure the system so that instant messaging is not available if the archiving database cannot be accessed.</span></span> <span data-ttu-id="cfa37-172">Sie können dies überprüfen, indem Sie einen Befehl wie den folgenden ausführen:</span><span class="sxs-lookup"><span data-stu-id="cfa37-172">You can verify that by running a command similar to the following:</span></span>
    
        Get-CsArchivingConfiguration -Identity "atl-cs-001.litwareinc.com" | Select-Object BlockOnArchiveFailure
    
    <span data-ttu-id="cfa37-173">Wenn BlockOnArchiveFailure auf "true" festgelegt ist, sollten Sie ermitteln, ob die Archivierungsdatenbank verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="cfa37-173">If BlockOnArchiveFailure is set to True, then you should determine whether or not the archiving database is available.</span></span> <span data-ttu-id="cfa37-174">Sie können die Speicherorte ihrer Archivierungsdatenbanken mithilfe des folgenden Befehls zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="cfa37-174">You can return the locations of your archiving databases by using the following command:</span></span>
    
        Get-CsService -ArchivingDatabase

  - <span data-ttu-id="cfa37-175">Der Archivierungs Server steht möglicherweise nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="cfa37-175">The Archiving Server might not be available.</span></span> <span data-ttu-id="cfa37-176">Mit diesem Befehl können Sie den FQDN ihrer Archivierungsserver abrufen:</span><span class="sxs-lookup"><span data-stu-id="cfa37-176">You can retrieve the FQDN of your Archiving Servers by using this command:</span></span>
    
        Get-CsService -ArchivingServer
    
    <span data-ttu-id="cfa37-177">Sie können dann den entsprechenden Server anpingen, um zu überprüfen, ob er verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="cfa37-177">You can then ping the appropriate server to verify that it is available.</span></span> <span data-ttu-id="cfa37-178">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="cfa37-178">For example:</span></span>
    
        ping atl-archiving-001.litwareinc.com

<span data-ttu-id="cfa37-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cfa37-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

