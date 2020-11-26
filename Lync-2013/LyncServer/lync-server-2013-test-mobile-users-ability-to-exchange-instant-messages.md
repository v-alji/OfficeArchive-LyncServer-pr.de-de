---
title: 'Lync Server 2013: Testen der Fähigkeit von mobilen Benutzern zum Austauschen von Sofortnachrichten'
description: 'Lync Server 2013: Testen Sie die Fähigkeit von mobilen Benutzern, Sofortnachrichten auszutauschen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test mobile users' ability to exchange instant messages
ms:assetid: a78a048f-d413-4bee-8626-d62b8b74f811
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767950(v=OCS.15)
ms:contentKeyID: 63969638
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 675bbeff93fed374d950b2efbdf15b4ea246f861
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444259"
---
# <a name="test-mobile-users-ability-to-exchange-instant-messages-in-lync-server-2013"></a><span data-ttu-id="4c3f0-103">Testen der Fähigkeit von mobilen Benutzern zum Austauschen von Chatnachrichten in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4c3f0-103">Test mobile users' ability to exchange instant messages in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4c3f0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4c3f0-104">

<span> </span></span></span>

<span data-ttu-id="4c3f0-105">_**Letztes Änderungsdatum des Themas:** 2014-06-07_</span><span class="sxs-lookup"><span data-stu-id="4c3f0-105">_**Topic Last Modified:** 2014-06-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4c3f0-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="4c3f0-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="4c3f0-107">Monatlich</span><span class="sxs-lookup"><span data-stu-id="4c3f0-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4c3f0-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="4c3f0-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="4c3f0-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4c3f0-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4c3f0-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="4c3f0-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="4c3f0-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="4c3f0-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="4c3f0-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsMcxP2PIM-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="4c3f0-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsMcxP2PIM cmdlet.</span></span> <span data-ttu-id="4c3f0-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="4c3f0-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsMcxP2PIM&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="4c3f0-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4c3f0-114">Description</span></span>

<span data-ttu-id="4c3f0-115">Mit dem Mobilitätsdienst können Benutzer mobiler Geräte wie folgt vorgehen:</span><span class="sxs-lookup"><span data-stu-id="4c3f0-115">The Mobility Service enables mobile device users to do such things as:</span></span>

1.  <span data-ttu-id="4c3f0-116">Tauschen Sie Sofortnachrichten und Anwesenheitsinformationen aus.</span><span class="sxs-lookup"><span data-stu-id="4c3f0-116">Exchange instant messages and presence information.</span></span>

2.  <span data-ttu-id="4c3f0-117">Speichern und Abrufen von Voicemail intern und nicht mit Ihrem WLAN-Anbieter.</span><span class="sxs-lookup"><span data-stu-id="4c3f0-117">Store and retrieve voice mail internally instead of with their wireless provider.</span></span>

3.  <span data-ttu-id="4c3f0-118">Nutzen Sie die Vorteile von lync-Server Funktionen wie Anruf über Arbeit und Einwahlkonferenzen.</span><span class="sxs-lookup"><span data-stu-id="4c3f0-118">Take advantage of Lync Server capabilities such as Call via Work and dial-out conferencing.</span></span>

<span data-ttu-id="4c3f0-119">Das Test-CsMxcP2PIM-Cmdlet bietet eine schnelle und einfache Möglichkeit, um zu überprüfen, ob Benutzer den Mobilitätsdienst zum Austauschen von Sofortnachrichten verwenden können.</span><span class="sxs-lookup"><span data-stu-id="4c3f0-119">The Test-CsMxcP2PIM cmdlet provides a quick and easy way to verify that users can use the Mobility Service to exchange instant messages.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="4c3f0-120">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="4c3f0-120">Running the test</span></span>

<span data-ttu-id="4c3f0-121">Damit dieser Test ausgeführt werden kann, müssen Sie für jedes Konto zwei Windows PowerShell-Anmeldeinformationsobjekte (Objekte, die den Kontonamen und das Kennwort enthalten) erstellen.</span><span class="sxs-lookup"><span data-stu-id="4c3f0-121">To run this test, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="4c3f0-122">Sie müssen dann diese Anmeldeinformationsobjekte und die SIP-Adressen der beiden Konten einbeziehen, wenn Sie Test-CsMcxP2PIM aufrufen:</span><span class="sxs-lookup"><span data-stu-id="4c3f0-122">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsMcxP2PIM:</span></span>

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\pilar"
    
    Test-CsMcxP2PIM -TargetFqdn "atl-cs-001.litwareinc.com" -Authentication Negotiate -SenderSipAddres "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:packerman@litwareinc.com" -ReceiverCredential $credential2

<span data-ttu-id="4c3f0-123">Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Test-CsMcxP2PIM](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxP2PIM) .</span><span class="sxs-lookup"><span data-stu-id="4c3f0-123">For more information, see the help topic for the [Test-CsMcxP2PIM](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxP2PIM) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="4c3f0-124">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="4c3f0-124">Determining success or failure</span></span>

<span data-ttu-id="4c3f0-125">Wenn die beiden Testbenutzer Sofortnachrichten mithilfe des mobilitätsdiensts austauschen können, gibt Test-CsMcxP2PIM das Testergebnis erfolgreich zurück:</span><span class="sxs-lookup"><span data-stu-id="4c3f0-125">If the two test users can exchange instant messages by using the mobility service then Test-CsMcxP2PIM will return test result Success:</span></span>

<span data-ttu-id="4c3f0-126">Ziel-FQDN: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="4c3f0-126">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="4c3f0-127">Ziel-URI: http://atl-cs-001.litwareinc.com:443/mcx</span><span class="sxs-lookup"><span data-stu-id="4c3f0-127">Target Uri : http://atl-cs-001.litwareinc.com:443/mcx</span></span>

<span data-ttu-id="4c3f0-128">Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="4c3f0-128">Result : Success</span></span>

<span data-ttu-id="4c3f0-129">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4c3f0-129">Latency : 00:00:00</span></span>

<span data-ttu-id="4c3f0-130">Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="4c3f0-130">Error Message :</span></span>

<span data-ttu-id="4c3f0-131">Diagnose</span><span class="sxs-lookup"><span data-stu-id="4c3f0-131">Diagnosis :</span></span>

<span data-ttu-id="4c3f0-132">Wenn der Test fehlschlägt, wird das Ergebnis auf Failure gesetzt, und es wird eine detaillierte Fehlermeldung und Diagnose angezeigt:</span><span class="sxs-lookup"><span data-stu-id="4c3f0-132">If the test fails then the Result will be set to Failure and a detailed error message and diagnosis will be displayed:</span></span>

<span data-ttu-id="4c3f0-133">Ziel-FQDN: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="4c3f0-133">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="4c3f0-134">Ziel-URI: https://atl-cs-001.litwareinc.com:443/mcx</span><span class="sxs-lookup"><span data-stu-id="4c3f0-134">Target Uri : https://atl-cs-001.litwareinc.com:443/mcx</span></span>

<span data-ttu-id="4c3f0-135">Ergebnis: Fehler</span><span class="sxs-lookup"><span data-stu-id="4c3f0-135">Result : Failure</span></span>

<span data-ttu-id="4c3f0-136">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4c3f0-136">Latency : 00:00:00</span></span>

<span data-ttu-id="4c3f0-137">Fehlermeldung: für Web-Ticket Dienst wurde keine Antwort empfangen.</span><span class="sxs-lookup"><span data-stu-id="4c3f0-137">Error Message : No response received for Web-Ticket service.</span></span>

<span data-ttu-id="4c3f0-138">Innere Ausnahme: die HHTP-Anforderung ist nicht autorisiert mit</span><span class="sxs-lookup"><span data-stu-id="4c3f0-138">Inner Exception:The HHTP request is unauthorized with</span></span>

<span data-ttu-id="4c3f0-139">Client-Aushandlungs Schema "NTLM".</span><span class="sxs-lookup"><span data-stu-id="4c3f0-139">client negotiation scheme 'Ntlm'.</span></span> <span data-ttu-id="4c3f0-140">Die Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="4c3f0-140">The authentication</span></span>

<span data-ttu-id="4c3f0-141">der vom Server empfangene Header lautet "Negotiate, NTLM".</span><span class="sxs-lookup"><span data-stu-id="4c3f0-141">header received from the server was 'Negotiate,NTLM'.</span></span>

<span data-ttu-id="4c3f0-142">Innere Ausnahme: der Remoteserver hat einen Fehler zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="4c3f0-142">Inner Exception:The remote server returned an error:</span></span>

<span data-ttu-id="4c3f0-143">(401) nicht autorisiert.</span><span class="sxs-lookup"><span data-stu-id="4c3f0-143">(401) Unauthorized.</span></span>

<span data-ttu-id="4c3f0-144">Diagnose</span><span class="sxs-lookup"><span data-stu-id="4c3f0-144">Diagnosis :</span></span>

<span data-ttu-id="4c3f0-145">Innere Diagnose: X-MS-Server-Fqdb: ATL-CS-</span><span class="sxs-lookup"><span data-stu-id="4c3f0-145">Inner Diagnosis:X-MS-server-Fqdb : atl-cs-</span></span>

<span data-ttu-id="4c3f0-146">001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="4c3f0-146">001.litwareinc.com</span></span>

<span data-ttu-id="4c3f0-147">Cache-Control: privat</span><span class="sxs-lookup"><span data-stu-id="4c3f0-147">Cache-Control : private</span></span>

<span data-ttu-id="4c3f0-148">Content-Type: Text/HTML; charset = UTF-8.</span><span class="sxs-lookup"><span data-stu-id="4c3f0-148">Content-Type : text/html; charset=utf-8.</span></span>

<span data-ttu-id="4c3f0-149">Server: Microsoft-IIS/8.5</span><span class="sxs-lookup"><span data-stu-id="4c3f0-149">Server : Microsoft-IIS/8.5</span></span>

<span data-ttu-id="4c3f0-150">WWW-Authenticate: Negotiate, NTLM</span><span class="sxs-lookup"><span data-stu-id="4c3f0-150">WWW-Authenticate : Negotiate,NTLM</span></span>

<span data-ttu-id="4c3f0-151">X-powered-by: ASP.net</span><span class="sxs-lookup"><span data-stu-id="4c3f0-151">X-Powered-By : ASP.NET</span></span>

<span data-ttu-id="4c3f0-152">X-Content-Type-Optionen: nosniff</span><span class="sxs-lookup"><span data-stu-id="4c3f0-152">X-Content-Type-Options : nosniff</span></span>

<span data-ttu-id="4c3f0-153">Datum: Wed, 28 May 2014 19:16:05 GMT</span><span class="sxs-lookup"><span data-stu-id="4c3f0-153">Date : Wed, 28 May 2014 19:16:05 GMT</span></span>

<span data-ttu-id="4c3f0-154">Content-length: 6305</span><span class="sxs-lookup"><span data-stu-id="4c3f0-154">Content-Length : 6305</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="4c3f0-155">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="4c3f0-155">Reasons why the test might have failed</span></span>

<span data-ttu-id="4c3f0-156">Wenn Test-CsMcxP2PIM fehlschlägt, sollte der erste Schritt darin liegen, zu überprüfen, ob der Mobilitätsdienst eingerichtet ist und ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="4c3f0-156">If Test-CsMcxP2PIM fails your first step should be to verify that the mobility service is up and running.</span></span> <span data-ttu-id="4c3f0-157">Dies kann mithilfe eines Webbrowsers erfolgen, um zu überprüfen, ob auf die Mobilitätsdienst-URL für Ihren lync Server-Pool zugegriffen werden kann.</span><span class="sxs-lookup"><span data-stu-id="4c3f0-157">That can be done by using a web browser to verify that the mobility service URL for your Lync Server pool can be accessed.</span></span> <span data-ttu-id="4c3f0-158">Mit diesem Befehl wird beispielsweise die URL für den Pool ATL-CS-001.litwareinc.com überprüft:</span><span class="sxs-lookup"><span data-stu-id="4c3f0-158">For example, this command verifies the URL for the pool atl-cs-001.litwareinc.com:</span></span>

    https://atl-cs-001.litwareinc.com/mcx/mcxservice.svc

<span data-ttu-id="4c3f0-159">Wenn der Mobilitätsdienst anscheinend ausgeführt wird, überprüfen Sie, ob die beiden Testbenutzer über gültige lync Server-Konten verfügen.</span><span class="sxs-lookup"><span data-stu-id="4c3f0-159">If the mobility service seems to be running then verify that your two test users have valid Lync Server accounts.</span></span> <span data-ttu-id="4c3f0-160">Sie können Kontoinformationen abrufen, indem Sie einen Befehl wie den folgenden verwenden:</span><span class="sxs-lookup"><span data-stu-id="4c3f0-160">You can retrieve account information by using a command similar to this:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

<span data-ttu-id="4c3f0-161">Wenn die Enabled-Eigenschaft nicht gleich true ist oder der Befehl fehlschlägt, bedeutet dies, dass der Benutzer kein gültiges lync Server-Konto hat.</span><span class="sxs-lookup"><span data-stu-id="4c3f0-161">If the Enabled property is not equal to True or if the command fails, that means that the user does not have a valid Lync Server account.</span></span>

<span data-ttu-id="4c3f0-162">Sie sollten auch sicherstellen, dass der Benutzer für Mobilität aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="4c3f0-162">You should also verify that the user is enabled for mobility.</span></span> <span data-ttu-id="4c3f0-163">Ermitteln Sie dazu zunächst die Mobilitätsrichtlinie, die dem Konto zugewiesen ist:</span><span class="sxs-lookup"><span data-stu-id="4c3f0-163">To do that, first determine the mobility policy that is assigned to the account:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object MobilityPolicy

<span data-ttu-id="4c3f0-164">Nachdem Sie den Richtliniennamen bekannt haben, verwenden Sie das Get-CsMobilityPolicy-Cmdlet, um zu überprüfen, ob die EnableMobility-Eigenschaft auf die betreffende Richtlinie (beispielsweise RedmondMobilityPolicy) auf true festgelegt ist:</span><span class="sxs-lookup"><span data-stu-id="4c3f0-164">After you know the policy name, use the Get-CsMobilityPolicy cmdlet to verify that the policy in question (for example, RedmondMobilityPolicy) has the EnableMobility property set to True:</span></span>

    Get-CsMobilityPolicy -Identity "RedmondMobilityPolicy"

<span data-ttu-id="4c3f0-165">Wenn Sie eine Fehlermeldung mit Authentifizierungs Headern erhalten, bedeutet dies häufig, dass Sie kein gültiges Benutzerkonto angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="4c3f0-165">If you receive an error message with authentication headers, that often means that you have not specified a valid user account.</span></span> <span data-ttu-id="4c3f0-166">Überprüfen Sie den Benutzernamen und das Kennwort, und versuchen Sie dann erneut, den Test zu testen.</span><span class="sxs-lookup"><span data-stu-id="4c3f0-166">Verify the user name and password and then try the test again.</span></span> <span data-ttu-id="4c3f0-167">Wenn Sie davon überzeugt sind, dass das Benutzerkonto gültig ist, verwenden Sie das Get-CsWebServiceConfiguration-Cmdlet, und überprüfen Sie den Wert der UseWindowsAuth-Eigenschaft.</span><span class="sxs-lookup"><span data-stu-id="4c3f0-167">If you are convinced that the user account is valid, then use the Get-CsWebServiceConfiguration cmdlet and check the value of the UseWindowsAuth property.</span></span> <span data-ttu-id="4c3f0-168">Damit erfahren Sie, welche Authentifizierungsmethoden in Ihrer Organisation aktiviert sind. Weitere Tipps zur Problembehandlung beim Mobilitätsdienst finden Sie im Blogbeitrag zur [Problembehandlung von externen lync-Mobilitäts Verbindungsproblemen Schritt-für-Schritt](https://blogs.technet.com/b/nexthop/archive/2012/02/21/troubleshooting-external-lync-mobility-connectivity-issues-step-by-step.aspx).</span><span class="sxs-lookup"><span data-stu-id="4c3f0-168">That will tell you which authentication methods are enabled in your organization.For more tips about how to troubleshoot the mobility service, see the blog post [Troubleshooting External Lync Mobility Connectivity Issues Step-by-Step](https://blogs.technet.com/b/nexthop/archive/2012/02/21/troubleshooting-external-lync-mobility-connectivity-issues-step-by-step.aspx).</span></span>

<span data-ttu-id="4c3f0-169"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4c3f0-169"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

