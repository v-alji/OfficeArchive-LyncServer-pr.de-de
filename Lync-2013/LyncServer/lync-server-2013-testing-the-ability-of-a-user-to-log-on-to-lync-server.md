---
title: 'Lync Server 2013: Testen der Fähigkeit eines Benutzers zur Anmeldung bei lync Server'
description: 'Lync Server 2013: Testen der Fähigkeit eines Benutzers zur Anmeldung bei lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing the ability of a user to log on to Lync Server
ms:assetid: d9cd0f9b-6ef2-4050-a4ca-263c5afa93ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743841(v=OCS.15)
ms:contentKeyID: 63969655
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8b86ae3e490af0b361799ed5fb3f56ed4de42c82
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394338"
---
# <a name="testing-the-ability-of-a-user-to-log-on-to-lync-server-2013"></a><span data-ttu-id="87dc5-103">Testen der Fähigkeit eines Benutzers zur Anmeldung bei lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="87dc5-103">Testing the ability of a user to log on to Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="87dc5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="87dc5-104">

<span> </span></span></span>

<span data-ttu-id="87dc5-105">_**Letztes Änderungsdatum des Themas:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="87dc5-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="87dc5-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="87dc5-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="87dc5-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="87dc5-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="87dc5-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="87dc5-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="87dc5-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="87dc5-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="87dc5-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="87dc5-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="87dc5-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="87dc5-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="87dc5-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsRegistration-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="87dc5-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsRegistration cmdlet.</span></span> <span data-ttu-id="87dc5-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="87dc5-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsRegistration&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="87dc5-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="87dc5-114">Description</span></span>

<span data-ttu-id="87dc5-115">Mithilfe des Test-CsRegistration-Cmdlets können Sie überprüfen, ob sich die Benutzer in Ihrer Organisation bei lync Server anmelden können.</span><span class="sxs-lookup"><span data-stu-id="87dc5-115">The Test-CsRegistration cmdlet enables you to verify that users in your organization can log on to Lync Server.</span></span> <span data-ttu-id="87dc5-116">Wenn Sie Test-CsRegistration ausführen, versucht das Cmdlet, sich bei einem Testbenutzer bei lync Server anzumelden, und trennt dann, falls dies erfolgreich ist, den Testbenutzer vom System.</span><span class="sxs-lookup"><span data-stu-id="87dc5-116">When you run Test-CsRegistration, the cmdlet attempts to sign in a test user to Lync Server and then, if it is successful, disconnects that test user from the system.</span></span> <span data-ttu-id="87dc5-117">All dies geschieht ohne Benutzerinteraktion und ohne Auswirkungen auf tatsächliche Benutzer.</span><span class="sxs-lookup"><span data-stu-id="87dc5-117">All of this happens without any user interaction, and without affecting any actual users.</span></span> <span data-ttu-id="87dc5-118">Nehmen wir beispielsweise an, dass das Test Konto SIP:kenmyer@litwareinc.com einem echten Benutzer entspricht, der ein echtes lync Server-Konto hat.</span><span class="sxs-lookup"><span data-stu-id="87dc5-118">For example, suppose that the test account sip:kenmyer@litwareinc.com corresponds to a real user who has a real Lync Server account.</span></span> <span data-ttu-id="87dc5-119">In diesem Fall wird der Test ohne Unterbrechung des echten Ken Myers durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="87dc5-119">In that case, the test will be conducted without any disruption to the real Ken Myer.</span></span> <span data-ttu-id="87dc5-120">Wenn sich das Ken Myers Test-Konto vom System abmeldet, bleibt die Person angemeldet.</span><span class="sxs-lookup"><span data-stu-id="87dc5-120">When the Ken Myer test account logs off from the system, Ken Myer the person will remain logged on.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="87dc5-121">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="87dc5-121">Running the test</span></span>

<span data-ttu-id="87dc5-122">Das Test-CsRegistration-Cmdlet kann entweder mit einem vorkonfigurierten Test Konto ausgeführt werden (siehe Einrichten von Testkonten zum Ausführen von lync Server-Tests) oder dem Konto eines beliebigen Benutzers, der für lync Server aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="87dc5-122">The Test-CsRegistration cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="87dc5-123">Um diese Überprüfung mit einem Testkonto auszuführen, müssen Sie lediglich den FQDN des zu testenden lync Server-registrierungspools angeben.</span><span class="sxs-lookup"><span data-stu-id="87dc5-123">To run this check using a test account, you just have to specify the FQDN of the Lync Server Registrar pool being tested.</span></span> <span data-ttu-id="87dc5-124">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="87dc5-124">For example:</span></span>

    Test-CsRegistration -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="87dc5-125">Damit diese Überprüfung mit einem tatsächlichen Benutzerkonto ausgeführt werden kann, müssen Sie zuerst ein Windows PowerShell-Anmeldeinformationsobjekt erstellen, das den Kontonamen und das Kennwort enthält.</span><span class="sxs-lookup"><span data-stu-id="87dc5-125">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="87dc5-126">Sie müssen das Anmeldeinformationen-Objekt und die SIP-Adresse, die dem Konto zugewiesen ist, beim Aufrufen von Test-CsRegistration einfügen:</span><span class="sxs-lookup"><span data-stu-id="87dc5-126">You must then include that credentials object and the SIP address assigned to the account when you call Test-CsRegistration:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsRegistration -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="87dc5-127">Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsRegistration](https://docs.microsoft.com/powershell/module/skype/Test-CsRegistration) .</span><span class="sxs-lookup"><span data-stu-id="87dc5-127">For more information, see the Help documentation for the [Test-CsRegistration](https://docs.microsoft.com/powershell/module/skype/Test-CsRegistration) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="87dc5-128">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="87dc5-128">Determining success or failure</span></span>

<span data-ttu-id="87dc5-129">Wenn sich der angegebene Benutzer bei lync Server anmelden (und dann abmelden kann), erhalten Sie eine ähnliche Ausgabe, wobei die Ergebniseigenschaft als erfolgreich markiert ist **:**</span><span class="sxs-lookup"><span data-stu-id="87dc5-129">If the specified user can log on to (and then log off from) Lync Server, you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="87dc5-130">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="87dc5-130">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="87dc5-131">Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="87dc5-131">Result : Success</span></span>

<span data-ttu-id="87dc5-132">Latenz: 00:00:06.8630376</span><span class="sxs-lookup"><span data-stu-id="87dc5-132">Latency : 00:00:06.8630376</span></span>

<span data-ttu-id="87dc5-133">Fehler</span><span class="sxs-lookup"><span data-stu-id="87dc5-133">Error :</span></span>

<span data-ttu-id="87dc5-134">Diagnose</span><span class="sxs-lookup"><span data-stu-id="87dc5-134">Diagnosis :</span></span>

<span data-ttu-id="87dc5-135">Wenn sich der angegebene Benutzer nicht anmelden oder abmelden kann, wird das Ergebnis als Fehler angezeigt, und zusätzliche Informationen werden in den Eigenschaften Fehler und Diagnose aufgezeichnet:</span><span class="sxs-lookup"><span data-stu-id="87dc5-135">If the specified user can't log in or log out, the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="87dc5-136">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="87dc5-136">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="87dc5-137">Ergebnis: Fehler</span><span class="sxs-lookup"><span data-stu-id="87dc5-137">Result : Failure</span></span>

<span data-ttu-id="87dc5-138">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="87dc5-138">Latency : 00:00:00</span></span>

<span data-ttu-id="87dc5-139">Fehler: 404, nicht gefunden</span><span class="sxs-lookup"><span data-stu-id="87dc5-139">Error : 404, Not Found</span></span>

<span data-ttu-id="87dc5-140">Diagnose: errorCode = 1003, Source = ATL-CS-001. "litwareinc. com, Reason = User</span><span class="sxs-lookup"><span data-stu-id="87dc5-140">Diagnosis : ErrorCode=1003,source=atl-cs-001.litwareinc.com,Reason=User does</span></span>

<span data-ttu-id="87dc5-141">nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="87dc5-141">not exist</span></span>

<span data-ttu-id="87dc5-142">Microsoft. RTC. Signalisierungs-DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="87dc5-142">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="87dc5-143">Die vorherige Ausgabe besagt beispielsweise, dass der Test fehlgeschlagen ist, weil der angegebene Benutzer nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="87dc5-143">For example, the previous output states that the test failed because the specified user couldn't be found.</span></span> <span data-ttu-id="87dc5-144">Sie können feststellen, ob eine SIP-Adresse gültig ist (und ob der Benutzer, der diese SIP-Adresse zugewiesen hat, für lync Server aktiviert ist), indem Sie den folgenden Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="87dc5-144">You can determine whether or not a SIP address is valid (and whether the user assigned that SIP address is enabled for Lync Server) by running this command:</span></span>

    Get-CsUser "sip:kenmyer@litwareinc.com"

<span data-ttu-id="87dc5-145">Wenn Test-CsRegistration fehlschlägt, möchten Sie möglicherweise den Test erneut ausführen, wobei dieser Zeitpunkt einschließlich des Verbose-Parameters lautet:</span><span class="sxs-lookup"><span data-stu-id="87dc5-145">If Test-CsRegistration fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsRegistration -UserSipAddress "sip:kenmyer@litwareinc.com" -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

<span data-ttu-id="87dc5-146">Wenn der Verbose-Parameter enthalten ist, gibt Test-CsRegistration eine Schritt-für-Schritt-Konto für jede Aktion zurück, die versucht wurde, als die Möglichkeit des angegebenen Benutzers zur Anmeldung bei lync Server geprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="87dc5-146">When the Verbose parameter is included, Test-CsRegistration will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="87dc5-147">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="87dc5-147">For example:</span></span>

<span data-ttu-id="87dc5-148">Ausführlich: die Aktivität "registrieren" wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="87dc5-148">VERBOSE: 'Register' activity started.</span></span>

<span data-ttu-id="87dc5-149">Registrierungsanfrage wird gesendet:</span><span class="sxs-lookup"><span data-stu-id="87dc5-149">Sending Registration request:</span></span>

<span data-ttu-id="87dc5-150">Ziel-FQDN = ATL-CS-011.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="87dc5-150">Target Fqdn = atl-cs-011.litwareinc.com</span></span>

<span data-ttu-id="87dc5-151">SIP-Adresse des Benutzers = SIP:kenmyer@litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="87dc5-151">User Sip Address = sip:kenmyer@litwareinc.com</span></span>

<span data-ttu-id="87dc5-152">Registrar Port = 5061.</span><span class="sxs-lookup"><span data-stu-id="87dc5-152">Registrar Port = 5061.</span></span>

<span data-ttu-id="87dc5-153">Auth-Typ "vertrauenswürdig" ist ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="87dc5-153">Auth Type 'Trusted' is selected.</span></span>

<span data-ttu-id="87dc5-154">Eine Ausnahme "der Endpunkt kann nicht registriert werden.</span><span class="sxs-lookup"><span data-stu-id="87dc5-154">An exception 'The endpoint is unable to register.</span></span> <span data-ttu-id="87dc5-155">Informationen dazu finden Sie unter Fehler begründete Fehler während der Workflow-Ausführung "Microsoft. RTC. SyntheticTransactions. Workflow. STRegistrerWorkflow".</span><span class="sxs-lookup"><span data-stu-id="87dc5-155">See the ErrorCode for specific reason' occurred during Workflow Microsoft.Rtc.SyntheticTransactions.Workflow.STRegistrerWorkflow execution.</span></span>

<span data-ttu-id="87dc5-156">Ausnahmeaufrufliste: unter Microsoft. RTC. Signalisierungs-SipAsyncResult'1. throwiffailedplatform ()</span><span class="sxs-lookup"><span data-stu-id="87dc5-156">Exception Call Stack: at Microsoft.Rtc.Signaling.SipAsyncResult'1.ThrowIfFailed()</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="87dc5-157">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="87dc5-157">Reasons why the test might have failed</span></span>

<span data-ttu-id="87dc5-158">Im folgenden finden Sie einige häufige Gründe, warum Test-CsRegistration fehlschlagen kann:</span><span class="sxs-lookup"><span data-stu-id="87dc5-158">Here are some common reasons why Test-CsRegistration might fail:</span></span>

  - <span data-ttu-id="87dc5-159">Sie haben ein falsches Benutzerkonto angegeben.</span><span class="sxs-lookup"><span data-stu-id="87dc5-159">You specified an incorrect user account.</span></span> <span data-ttu-id="87dc5-160">Sie können überprüfen, ob ein Benutzerkonto vorhanden ist, indem Sie einen Befehl wie den folgenden ausführen:</span><span class="sxs-lookup"><span data-stu-id="87dc5-160">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="87dc5-161">Das Benutzerkonto ist gültig, das Konto ist derzeit aber für lync Server nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="87dc5-161">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="87dc5-162">Führen Sie einen Befehl ähnlich der folgenden aus, um zu überprüfen, ob ein Benutzerkonto für lync Server aktiviert ist:</span><span class="sxs-lookup"><span data-stu-id="87dc5-162">To verify that a user account is enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="87dc5-163">Wenn die Enabled-Eigenschaft auf false festgelegt ist, bedeutet dies, dass der Benutzer zurzeit nicht für lync Server aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="87dc5-163">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="87dc5-164">Sie haben einen falschen Registrierungspool angegeben.</span><span class="sxs-lookup"><span data-stu-id="87dc5-164">You specified an incorrect Registrar pool.</span></span> <span data-ttu-id="87dc5-165">Mit diesem Befehl können Sie die FQDNs ihrer registrierungspools zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="87dc5-165">You can return the FQDNs of your Registrar pools by using this command:</span></span>
    
        Get-CsService -Registrar | Select-Object PoolFqdn

  - <span data-ttu-id="87dc5-166">Der Registrierungspool steht zurzeit nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="87dc5-166">The Registrar pool is currently not available.</span></span> <span data-ttu-id="87dc5-167">Versuchen Sie, den Pool zu pingen, um zu sehen, ob er antwortet:</span><span class="sxs-lookup"><span data-stu-id="87dc5-167">Try pinging the pool to see whether it responds:</span></span>
    
        ping atl-cs-001.litwareinc.com

<span data-ttu-id="87dc5-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="87dc5-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

