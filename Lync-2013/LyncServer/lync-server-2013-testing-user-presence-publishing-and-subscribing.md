---
title: 'Lync Server 2013: Testen der Benutzer Anwesenheits Veröffentlichung und-Anmeldung'
description: 'Lync Server 2013: Testen der Benutzer Anwesenheits Veröffentlichung und-Anmeldung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing user presence publishing and subscribing
ms:assetid: 27694c71-8e63-4aa4-b49f-fa06ccb81949
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743832(v=OCS.15)
ms:contentKeyID: 63969587
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 90913f270fbd034ca4d2ea7cf3b93c255fc95c66
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439712"
---
# <a name="testing-user-presence-publishing-and-subscribing-in-lync-server-2013"></a><span data-ttu-id="4b5a1-103">Testen der Veröffentlichung und des Abonnierens von Benutzeranwesenheitsinformationen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4b5a1-103">Testing user presence publishing and subscribing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4b5a1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4b5a1-104">

<span> </span></span></span>

<span data-ttu-id="4b5a1-105">_**Letztes Änderungsdatum des Themas:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="4b5a1-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b5a1-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="4b5a1-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="4b5a1-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="4b5a1-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b5a1-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="4b5a1-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="4b5a1-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4b5a1-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b5a1-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="4b5a1-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="4b5a1-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="4b5a1-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsPresence-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsPresence cmdlet.</span></span> <span data-ttu-id="4b5a1-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="4b5a1-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsPresence&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="4b5a1-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b5a1-114">Description</span></span>

<span data-ttu-id="4b5a1-115">Test-CsPresence wird verwendet, um zu ermitteln, ob ein paar Testbenutzer sich bei lync Server anmelden und dann Anwesenheitsinformationen austauschen können.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-115">Test-CsPresence is used to determine whether a pair of test users can log on to Lync Server and then exchange presence information.</span></span> <span data-ttu-id="4b5a1-116">Dazu protokolliert das Cmdlet zunächst die beiden Benutzer am System.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-116">To do this, the cmdlet first logs the two users on to the system.</span></span> <span data-ttu-id="4b5a1-117">Wenn beide Anmeldungen erfolgreich sind, werden Sie vom ersten Testbenutzer aufgefordert, Anwesenheitsinformationen des zweiten Benutzers zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-117">If both logons succeed, the first test user then asks to receive presence information from the second user.</span></span> <span data-ttu-id="4b5a1-118">Der zweite Benutzer veröffentlicht diese Informationen, und Test-CsPresence überprüft, ob die Informationen erfolgreich an den ersten Benutzer übertragen wurden.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-118">The second user publishes this information, and Test-CsPresence verifies that the information was successfully transmitted to the first user.</span></span> <span data-ttu-id="4b5a1-119">Nach dem Austausch von Anwesenheitsinformationen werden die beiden Testbenutzer dann von lync Server abgemeldet.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-119">After the exchange of presence information, the two test users are then logged off from Lync Server.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="4b5a1-120">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="4b5a1-120">Running the test</span></span>

<span data-ttu-id="4b5a1-121">Das Test-CsPresence-Cmdlet kann entweder mit einem Paar vorkonfigurierter Testkonten ausgeführt werden (siehe Einrichten von Testkonten zum Ausführen von lync Server-Tests) oder der Konten von zwei Benutzern, die für lync Server aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-121">The Test-CsPresence cmdlet can be run using either a pair of preconfigured test accounts (see Setting Up Test Accounts for Running Lync Server Tests) or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="4b5a1-122">Um diese Prüfung mit Testkonten auszuführen, müssen Sie lediglich den FQDN des zu testenden lync-Server Pools angeben.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-122">To run this check using test accounts, you just have to specify the FQDN of the Lync Server pool being tested.</span></span> <span data-ttu-id="4b5a1-123">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4b5a1-123">For example:</span></span>

    Test-CsPresence -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="4b5a1-124">Damit diese Überprüfung mit tatsächlichen Benutzerkonten ausgeführt werden kann, müssen Sie für jedes Konto zwei Windows PowerShell-Anmeldeinformationsobjekte (Objekte, die den Kontonamen und das Kennwort enthalten) erstellen.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-124">To run this check using actual user accounts, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="4b5a1-125">Sie müssen dann diese Anmeldeinformationsobjekte und die SIP-Adressen der beiden Konten einbeziehen, wenn Sie Test-CsPresence aufrufen:</span><span class="sxs-lookup"><span data-stu-id="4b5a1-125">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsPresence:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsPresence -TargetFqdn "atl-cs-001.litwareinc.com" -PublisherSipAddress "sip:kenmyer@litwareinc.com" -PublisherCredential $credential1 -SubscriberSipAddress "sip:davidlongmire@litwareinc.com" -SubscriberCredential $credential2

<span data-ttu-id="4b5a1-126">Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsPresence](https://docs.microsoft.com/powershell/module/skype/Test-CsPresence) .</span><span class="sxs-lookup"><span data-stu-id="4b5a1-126">For more information, see the Help documentation for the [Test-CsPresence](https://docs.microsoft.com/powershell/module/skype/Test-CsPresence) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="4b5a1-127">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="4b5a1-127">Determining success or failure</span></span>

<span data-ttu-id="4b5a1-128">Wenn die angegebenen Benutzeranwesenheitsinformationen austauschen können, erhalten Sie eine ähnliche Ausgabe, wobei die Eigenschaft Ergebnis als erfolgreich markiert ist **:**</span><span class="sxs-lookup"><span data-stu-id="4b5a1-128">If the specified users can exchange presence information, then you'll receive output similar to this, with the Result property marked as **Success:**</span></span>

<span data-ttu-id="4b5a1-129">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="4b5a1-129">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="4b5a1-130">Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="4b5a1-130">Result : Success</span></span>

<span data-ttu-id="4b5a1-131">Latenz: 00:00:06.3280315</span><span class="sxs-lookup"><span data-stu-id="4b5a1-131">Latency : 00:00:06.3280315</span></span>

<span data-ttu-id="4b5a1-132">Fehler</span><span class="sxs-lookup"><span data-stu-id="4b5a1-132">Error :</span></span>

<span data-ttu-id="4b5a1-133">Diagnose</span><span class="sxs-lookup"><span data-stu-id="4b5a1-133">Diagnosis :</span></span>

<span data-ttu-id="4b5a1-134">Wenn die beiden Benutzer keine Anwesenheitsinformationen austauschen können, wird das Ergebnis als Fehler angezeigt, und weitere Informationen werden in den Eigenschaften Fehler und Diagnose aufgezeichnet:</span><span class="sxs-lookup"><span data-stu-id="4b5a1-134">If the two users can't exchange presence information, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="4b5a1-135">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="4b5a1-135">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="4b5a1-136">Ergebnis: Fehler</span><span class="sxs-lookup"><span data-stu-id="4b5a1-136">Result : Failure</span></span>

<span data-ttu-id="4b5a1-137">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4b5a1-137">Latency : 00:00:00</span></span>

<span data-ttu-id="4b5a1-138">Fehler: 404, nicht gefunden</span><span class="sxs-lookup"><span data-stu-id="4b5a1-138">Error : 404, Not Found</span></span>

<span data-ttu-id="4b5a1-139">Diagnose: errorCode = 4005, Source = ATL-CS-001.litwareinc.com,</span><span class="sxs-lookup"><span data-stu-id="4b5a1-139">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="4b5a1-140">Reason = Ziel-URI ist entweder für SIP nicht aktiviert oder nicht</span><span class="sxs-lookup"><span data-stu-id="4b5a1-140">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="4b5a1-141">existieren.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-141">exist.</span></span>

<span data-ttu-id="4b5a1-142">Microsoft. RTC. Signalisierungs-DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="4b5a1-142">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="4b5a1-143">In der vorherigen Ausgabe wird beispielsweise festgestellt, dass der Test fehlgeschlagen ist, da mindestens eines der beiden Benutzerkonten ungültig ist: entweder ist das Konto nicht vorhanden, oder es wurde nicht für lync Server aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-143">For example, the previous output states that the test failed because at least one of the two user accounts is not valid: either the account does not exist or it has not been enabled for Lync Server.</span></span> <span data-ttu-id="4b5a1-144">Sie können überprüfen, ob die Konten vorhanden sind, und ermitteln, ob Sie für lync Server aktiviert sind, indem Sie einen Befehl wie den folgenden ausführen:</span><span class="sxs-lookup"><span data-stu-id="4b5a1-144">You can verify that the accounts exist, and determine whether they are enabled for Lync Server, by running a command similar to this:</span></span>

    "sip:kenmyer@litwareinc.com", "sip:davidlongmire@litwareinc.com" | Get-CsUser | Select-Object SipAddress, Enabled

<span data-ttu-id="4b5a1-145">Wenn Test-CsPresence fehlschlägt, möchten Sie möglicherweise den Test erneut ausführen, wobei dieser Zeitpunkt einschließlich des Verbose-Parameters lautet:</span><span class="sxs-lookup"><span data-stu-id="4b5a1-145">If Test-CsPresence fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsPresence -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="4b5a1-146">Wenn der Verbose-Parameter enthalten ist, gibt Test-CsPresence eine Schritt-für-Schritt-Konto für jede Aktion zurück, die versucht wurde, als die Möglichkeit des angegebenen Benutzers zur Anmeldung bei lync Server geprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-146">When the Verbose parameter is included, Test-CsPresence will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="4b5a1-147">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="4b5a1-147">For example:</span></span>

<span data-ttu-id="4b5a1-148">Anmeldungsanfrage gegen unbekannt getroffen</span><span class="sxs-lookup"><span data-stu-id="4b5a1-148">Registration Request hit against Unknown</span></span>

<span data-ttu-id="4b5a1-149">' Registrieren '-Aktivität abgeschlossen in ' 0,0345791 ' Sek.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-149">'Register' activity completed in '0.0345791' secs.</span></span>

<span data-ttu-id="4b5a1-150">Die Aktivität "SelfSubscribeActivity" wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-150">'SelfSubscribeActivity' activity started.</span></span>

<span data-ttu-id="4b5a1-151">"SelfSubscribeActivity"-Aktivität wurde in "0,0041174" Sek. abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-151">'SelfSubscribeActivity' activity completed in '0.0041174' secs.</span></span>

<span data-ttu-id="4b5a1-152">Die Aktivität "SubscribePresence" wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-152">'SubscribePresence' activity started.</span></span>

<span data-ttu-id="4b5a1-153">"SubscribePresence"-Aktivität wurde in "0,0038764" Sek. abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-153">'SubscribePresence' activity completed in '0.0038764' secs.</span></span>

<span data-ttu-id="4b5a1-154">Die Aktivität "PublishPresence" wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-154">'PublishPresence' activity started.</span></span>

<span data-ttu-id="4b5a1-155">Die Anwesenheits Benachrichtigung einer Ausnahme wird nicht innerhalb von 25 Sekunden empfangen.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-155">An exception 'Presence notification is not received within 25 secs.'</span></span> <span data-ttu-id="4b5a1-156">bereut-Workflow Microsoft. RTC. SyntheticTransactions. Workflows. STPresenceWorkflow-Ausführung aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-156">occurred ruing Workflow Microsoft.Rtc.SyntheticTransactions.Workflows.STPresenceWorkflow execution.</span></span>

<span data-ttu-id="4b5a1-157">Die Tatsache, dass die Anwesenheits Benachrichtigung nicht innerhalb von 25 Sekunden empfangen wurde, kann darauf hindeuten, dass Netzwerkprobleme das Austauschen von Informationen verhindern.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-157">The fact that the presence notification was not received within 25 seconds might indicate that network issues are preventing information from being exchanged.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="4b5a1-158">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="4b5a1-158">Reasons why the test might have failed</span></span>

<span data-ttu-id="4b5a1-159">Im folgenden finden Sie einige häufige Gründe, warum Test-CsPresence fehlschlagen kann:</span><span class="sxs-lookup"><span data-stu-id="4b5a1-159">Here are some common reasons why Test-CsPresence might fail:</span></span>

  - <span data-ttu-id="4b5a1-160">Sie haben ein falsches Benutzerkonto angegeben.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-160">You specified an incorrect user account.</span></span> <span data-ttu-id="4b5a1-161">Sie können überprüfen, ob ein Benutzerkonto vorhanden ist, indem Sie einen Befehl wie den folgenden ausführen:</span><span class="sxs-lookup"><span data-stu-id="4b5a1-161">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="4b5a1-162">Das Benutzerkonto ist gültig, das Konto ist derzeit aber für lync Server nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-162">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="4b5a1-163">Führen Sie einen Befehl ähnlich der folgenden aus, um zu überprüfen, ob ein Benutzerkonto für lync Server aktiviert ist:</span><span class="sxs-lookup"><span data-stu-id="4b5a1-163">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="4b5a1-164">Wenn die Enabled-Eigenschaft auf false festgelegt ist, bedeutet dies, dass der Benutzer zurzeit nicht für lync Server aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4b5a1-164">If the Enabled property is set to False that means that the user is currently not enabled for Lync Server.</span></span>

<span data-ttu-id="4b5a1-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4b5a1-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

