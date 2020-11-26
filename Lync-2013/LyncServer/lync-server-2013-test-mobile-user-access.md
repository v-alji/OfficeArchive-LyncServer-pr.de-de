---
title: 'Lync Server 2013: Testen des Zugriffs auf mobile Benutzer'
description: 'Lync Server 2013: Testen des Zugriffs auf mobile Benutzer'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test mobile user access
ms:assetid: 81d97420-428b-41b7-91ef-185d572d3456
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767947(v=OCS.15)
ms:contentKeyID: 63969624
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e99a05e6ef9fe925126026452823e5edcc100ede
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441242"
---
# <a name="test-mobile-user-access-in-lync-server-2013"></a><span data-ttu-id="56bc1-103">Testen des Zugriffs von mobilen Benutzern in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="56bc1-103">Test mobile user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="56bc1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="56bc1-104">

<span> </span></span></span>

<span data-ttu-id="56bc1-105">_**Letztes Änderungsdatum des Themas:** 2014-06-07_</span><span class="sxs-lookup"><span data-stu-id="56bc1-105">_**Topic Last Modified:** 2014-06-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56bc1-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="56bc1-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="56bc1-107">Monatlich</span><span class="sxs-lookup"><span data-stu-id="56bc1-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56bc1-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="56bc1-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="56bc1-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="56bc1-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56bc1-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="56bc1-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="56bc1-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="56bc1-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="56bc1-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsMcxConference-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="56bc1-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsMcxConference cmdlet.</span></span> <span data-ttu-id="56bc1-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="56bc1-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsMcxConference&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="56bc1-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="56bc1-114">Description</span></span>

<span data-ttu-id="56bc1-115">Mit dem Mobilitätsdienst können Benutzer mobiler Geräte wie folgt vorgehen:</span><span class="sxs-lookup"><span data-stu-id="56bc1-115">The Mobility Service enables mobile device users to do such things as:</span></span>

1.  <span data-ttu-id="56bc1-116">Tauschen Sie Sofortnachrichten und Anwesenheitsinformationen aus.</span><span class="sxs-lookup"><span data-stu-id="56bc1-116">Exchange instant messages and presence information.</span></span>

2.  <span data-ttu-id="56bc1-117">Speichern und Abrufen von Voicemail intern und nicht mit Ihrem WLAN-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="56bc1-117">Store and retrieve voice mail internally instead of with their wireless provider.</span></span>

3.  <span data-ttu-id="56bc1-118">Nutzen Sie die Vorteile von lync-Server Funktionen wie Anruf über Arbeit und Einwahlkonferenzen.</span><span class="sxs-lookup"><span data-stu-id="56bc1-118">Take advantage of Lync Server capabilities such as Call via Work and dial-out conferencing.</span></span> <span data-ttu-id="56bc1-119">Das Test-CsMcxConference-Cmdlet bietet eine schnelle und einfache Möglichkeit, um zu überprüfen, ob Benutzer teilnehmen und an lync Server-Konferenzen teilnehmen können, indem Sie ein mobiles Gerät verwenden.</span><span class="sxs-lookup"><span data-stu-id="56bc1-119">The Test-CsMcxConference cmdlet provides a quick and easy way to verify that users can join and participate in Lync Server conferences by using a mobile device.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="56bc1-120">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="56bc1-120">Running the test</span></span>

<span data-ttu-id="56bc1-121">Zum Ausführen dieser Prüfung müssen Sie für jedes Konto drei Windows PowerShell-Anmeldeinformationsobjekte (Objekte, die den Kontonamen und das Kennwort enthalten) erstellen.</span><span class="sxs-lookup"><span data-stu-id="56bc1-121">To run this check, you must create three Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="56bc1-122">Sie müssen dann diese Anmeldeinformationsobjekte und die SIP-Adressen der beiden Konten einbeziehen, wenn Sie Test-CsMcxConference aufrufen, wie im folgenden Beispiel gezeigt:</span><span class="sxs-lookup"><span data-stu-id="56bc1-122">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsMcxConference as shown in the following example:</span></span>

    $organizerCred = Get-Credential "litwareinc\kenmyer"
    $user1Cred = Get-Credential "litwareinc\packerman"
    $user2Cred = Get-Credential "litwareinc\adelaney"
    
    Test-CsMcxConference -TargetFqdn "atl-cs-001.litwareinc.com" -Authentication Negotiate -OrganizerSipAddress "sip:kenmyer@litwareinc.com" -OrganizerCredential $organizerCred -UserSipAddress "sip:pilar@litwareinc.com" -UserCredential $user1Cred -User2SipAddress "sip:adelaney@litwareinc.com" -User2Credential $user2Cred

<span data-ttu-id="56bc1-123">Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Test-CsMcxConference](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxConference) .</span><span class="sxs-lookup"><span data-stu-id="56bc1-123">For more information, see the help topic for the [Test-CsMcxConference](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxConference) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="56bc1-124">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="56bc1-124">Determining success or failure</span></span>

<span data-ttu-id="56bc1-125">Wenn die Überprüfung erfolgreich ist, meldet Test-CsMcxConference ein Testergebnis, das erfolgreich ist:</span><span class="sxs-lookup"><span data-stu-id="56bc1-125">If the check succeeds, Test-CsMcxConference will report a test result of Success:</span></span>

<span data-ttu-id="56bc1-126">Ziel-FQDN: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="56bc1-126">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="56bc1-127">Ziel-URI: http://atl-cs-001.litwareinc.com:443/mcx</span><span class="sxs-lookup"><span data-stu-id="56bc1-127">Target Uri : http://atl-cs-001.litwareinc.com:443/mcx</span></span>

<span data-ttu-id="56bc1-128">Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="56bc1-128">Result : Success</span></span>

<span data-ttu-id="56bc1-129">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="56bc1-129">Latency : 00:00:00</span></span>

<span data-ttu-id="56bc1-130">Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="56bc1-130">Error Message :</span></span>

<span data-ttu-id="56bc1-131">Diagnose</span><span class="sxs-lookup"><span data-stu-id="56bc1-131">Diagnosis :</span></span>

<span data-ttu-id="56bc1-132">Wenn die Überprüfung nicht erfolgreich ist Test-CsMcxConference wird ein Testergebnis des Fehlers gemeldet.</span><span class="sxs-lookup"><span data-stu-id="56bc1-132">If the check is unsuccessful Test-CsMcxConference will report a test result of Failure.</span></span> <span data-ttu-id="56bc1-133">Dieses Testergebnis wird in der Regel von einer detaillierten Fehlermeldung und Diagnose begleitet.</span><span class="sxs-lookup"><span data-stu-id="56bc1-133">This test result will typically be accompanied by a detailed error message and diagnosis.</span></span> <span data-ttu-id="56bc1-134">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="56bc1-134">For example:</span></span>

<span data-ttu-id="56bc1-135">Ziel-FQDN: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="56bc1-135">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="56bc1-136">Ziel-URI: https://atl-cs-001.litwareinc.com:443/mcx</span><span class="sxs-lookup"><span data-stu-id="56bc1-136">Target Uri : https://atl-cs-001.litwareinc.com:443/mcx</span></span>

<span data-ttu-id="56bc1-137">Ergebnis: Fehler</span><span class="sxs-lookup"><span data-stu-id="56bc1-137">Result : Failure</span></span>

<span data-ttu-id="56bc1-138">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="56bc1-138">Latency : 00:00:00</span></span>

<span data-ttu-id="56bc1-139">Fehlermeldung: für Web-Ticket Dienst wurde keine Antwort empfangen.</span><span class="sxs-lookup"><span data-stu-id="56bc1-139">Error Message : No response received for Web-Ticket service.</span></span>

<span data-ttu-id="56bc1-140">Innere Ausnahme: die HHTP-Anforderung ist mit dem Client nicht autorisiert</span><span class="sxs-lookup"><span data-stu-id="56bc1-140">Inner Exception:The HHTP request is unauthorized with client</span></span>

<span data-ttu-id="56bc1-141">Aushandlungs Schema "NTLM".</span><span class="sxs-lookup"><span data-stu-id="56bc1-141">negotiation scheme 'Ntlm'.</span></span> <span data-ttu-id="56bc1-142">Der empfangene Authentifizierungsheader</span><span class="sxs-lookup"><span data-stu-id="56bc1-142">The authentication header received</span></span>

<span data-ttu-id="56bc1-143">vom Server war "Negotiate".</span><span class="sxs-lookup"><span data-stu-id="56bc1-143">from the server was 'Negotiate'.</span></span>

<span data-ttu-id="56bc1-144">Innere Ausnahme: der Remoteserver hat einen Fehler zurückgegeben: (401)</span><span class="sxs-lookup"><span data-stu-id="56bc1-144">Inner Exception:The remote server returned an error: (401)</span></span>

<span data-ttu-id="56bc1-145">Unbefugte.</span><span class="sxs-lookup"><span data-stu-id="56bc1-145">Unauthorized.</span></span>

<span data-ttu-id="56bc1-146">Diagnose</span><span class="sxs-lookup"><span data-stu-id="56bc1-146">Diagnosis :</span></span>

<span data-ttu-id="56bc1-147">Innere Diagnose: X-MS-Server-Fqdb: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="56bc1-147">Inner Diagnosis:X-MS-server-Fqdb : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="56bc1-148">Cache-Control: privat</span><span class="sxs-lookup"><span data-stu-id="56bc1-148">Cache-Control : private</span></span>

<span data-ttu-id="56bc1-149">Content-Type: Text/HTML; charset = UTF-8.</span><span class="sxs-lookup"><span data-stu-id="56bc1-149">Content-Type : text/html; charset=utf-8.</span></span>

<span data-ttu-id="56bc1-150">Server: Microsoft-IIS/8.5</span><span class="sxs-lookup"><span data-stu-id="56bc1-150">Server : Microsoft-IIS/8.5</span></span>

<span data-ttu-id="56bc1-151">WWW-Authenticate: Negotiate, NTLM</span><span class="sxs-lookup"><span data-stu-id="56bc1-151">WWW-Authenticate : Negotiate,NTLM</span></span>

<span data-ttu-id="56bc1-152">X-powered-by: ASP.net</span><span class="sxs-lookup"><span data-stu-id="56bc1-152">X-Powered-By : ASP.NET</span></span>

<span data-ttu-id="56bc1-153">X-Content-Type-Optionen: nosniff</span><span class="sxs-lookup"><span data-stu-id="56bc1-153">X-Content-Type-Options : nosniff</span></span>

<span data-ttu-id="56bc1-154">Datum: Wed, 28 May 2014 19:22:19 GMT</span><span class="sxs-lookup"><span data-stu-id="56bc1-154">Date : Wed, 28 May 2014 19:22:19 GMT</span></span>

<span data-ttu-id="56bc1-155">Content-length: 6305</span><span class="sxs-lookup"><span data-stu-id="56bc1-155">Content-Length : 6305</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="56bc1-156">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="56bc1-156">Reasons why the test might have failed</span></span>

<span data-ttu-id="56bc1-157">Wenn Test-CsMcxConference fehlschlägt, sollten Sie zunächst überprüfen, ob der Mobilitätsdienst ausgeführt wird und auf den Sie zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="56bc1-157">If Test-CsMcxConference fails you should begin by verifying that the mobility service is running and can be accessed.</span></span> <span data-ttu-id="56bc1-158">Dies kann mithilfe eines Webbrowsers erfolgen, um zu überprüfen, ob auf die Mobilitätsdienst-URL für Ihren lync Server-Pool zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="56bc1-158">That can be done by using a web browser to verify that the mobility service URL for your Lync Server pool can be accessed.</span></span> <span data-ttu-id="56bc1-159">Mit diesem Befehl wird beispielsweise die URL für den Pool ATL-CS-001.litwareinc.com überprüft:</span><span class="sxs-lookup"><span data-stu-id="56bc1-159">For example, this command verifies the URL for the pool atl-cs-001.litwareinc.com:</span></span>

`https://atl-cs-001.litwareinc.com/mcx/mcxservice.svc`

<span data-ttu-id="56bc1-160">Wenn Sie auf den Mobilitätsdienst zugreifen können, sollten Sie sicherstellen, dass die Testbenutzer über gültige lync Server-Konten verfügen.</span><span class="sxs-lookup"><span data-stu-id="56bc1-160">If the mobility service can be accessed you should then verify that your test users have valid Lync Server accounts.</span></span> <span data-ttu-id="56bc1-161">Sie können Kontoinformationen abrufen, indem Sie einen Befehl wie den folgenden verwenden:</span><span class="sxs-lookup"><span data-stu-id="56bc1-161">You can retrieve account information by using a command similar to this:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

<span data-ttu-id="56bc1-162">Wenn die Enabled-Eigenschaft nicht gleich true ist oder der Befehl fehlschlägt, bedeutet dies, dass der Benutzer kein gültiges lync Server-Konto hat. Sie sollten auch sicherstellen, dass jedes Benutzerkonto für Mobilität aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="56bc1-162">If the Enabled property is not equal to True or if the command fails, that means that the user does not have a valid Lync Server account.You should also verify that each user account is enabled for mobility.</span></span> <span data-ttu-id="56bc1-163">Ermitteln Sie dazu zunächst die Mobilitätsrichtlinie, die dem Konto zugewiesen ist:</span><span class="sxs-lookup"><span data-stu-id="56bc1-163">To do that, first determine the mobility policy that is assigned to the account:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object MobilityPolicy

<span data-ttu-id="56bc1-164">Nachdem Sie den Richtliniennamen bekannt haben, verwenden Sie das Get-CsMobilityPolicy-Cmdlet, um zu überprüfen, ob die EnableMobility-Eigenschaft auf die betreffende Richtlinie (beispielsweise RedmondMobilityPolicy) auf true festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="56bc1-164">After you know the policy name, use the Get-CsMobilityPolicy cmdlet to verify that the policy in question (for example, RedmondMobilityPolicy) has the EnableMobility property set to True:</span></span>

    Get-CsMobilityPolicy -Identity "RedmondMobilityPolicy"

<span data-ttu-id="56bc1-165">Wenn Sie eine Fehlermeldung "Authentifizierungsheader" erhalten, wenn Sie Test-CsMcxConference ausführen, die häufig bedeutet, dass Sie kein gültiges Benutzerkonto angegeben haben, überprüfen Sie den Benutzernamen und das Kennwort, und versuchen Sie dann erneut, den Test zu testen.</span><span class="sxs-lookup"><span data-stu-id="56bc1-165">If you receive an “authentication header” error message when you run Test-CsMcxConference that often means that you have not specified a valid user account, Verify the user name and password and then try the test again.</span></span> <span data-ttu-id="56bc1-166">Wenn Sie davon überzeugt sind, dass das Benutzerkonto gültig ist, verwenden Sie das Get-CsWebServiceConfiguration-Cmdlet, und überprüfen Sie den Wert der UseWindowsAuth-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="56bc1-166">If you are convinced that the user account is valid, then use the Get-CsWebServiceConfiguration cmdlet and check the value of the UseWindowsAuth property.</span></span> <span data-ttu-id="56bc1-167">Damit erfahren Sie, welche Authentifizierungsmethoden in Ihrer Organisation aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="56bc1-167">That will tell you which authentication methods are enabled in your organization.</span></span>

<span data-ttu-id="56bc1-168">Weitere Tipps zur Problembehandlung beim Mobilitätsdienst finden Sie im Blogbeitrag zur [Problembehandlung von externen lync-Mobilitäts Verbindungsproblemen Schritt-für-Schritt](https://blogs.technet.com/b/nexthop/archive/2012/02/21/troubleshooting-external-lync-mobility-connectivity-issues-step-by-step.aspx).</span><span class="sxs-lookup"><span data-stu-id="56bc1-168">For more tips about how to troubleshoot the mobility service, see the blog post [Troubleshooting External Lync Mobility Connectivity Issues Step-by-Step](https://blogs.technet.com/b/nexthop/archive/2012/02/21/troubleshooting-external-lync-mobility-connectivity-issues-step-by-step.aspx).</span></span>

<span data-ttu-id="56bc1-169"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="56bc1-169"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

