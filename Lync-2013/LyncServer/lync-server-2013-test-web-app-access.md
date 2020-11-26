---
title: 'Lync Server 2013: Testen des Web App-Zugriffs'
description: 'Lync Server 2013: Testen des Web App-Zugriffs'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test Web App access
ms:assetid: 17d67ea3-f74d-4952-ac2b-92c0dacc8014
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767944(v=OCS.15)
ms:contentKeyID: 63969584
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fc3bbc8008df4fe47fc5a39571356383fe5a6035
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441130"
---
# <a name="test-web-app-access-in-lync-server-2013"></a><span data-ttu-id="9c585-103">Testen des Web App-Zugriffs in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c585-103">Test Web App access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9c585-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9c585-104">

<span> </span></span></span>

<span data-ttu-id="9c585-105">_**Letztes Änderungsdatum des Themas:** 2014-06-07_</span><span class="sxs-lookup"><span data-stu-id="9c585-105">_**Topic Last Modified:** 2014-06-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c585-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="9c585-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="9c585-107">Monatlich</span><span class="sxs-lookup"><span data-stu-id="9c585-107">Monthly</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c585-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="9c585-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="9c585-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="9c585-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c585-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="9c585-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="9c585-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="9c585-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="9c585-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsWebApp-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="9c585-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsWebApp cmdlet.</span></span> <span data-ttu-id="9c585-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="9c585-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsWebApp&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="9c585-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c585-114">Description</span></span>

<span data-ttu-id="9c585-115">Das Test-CsWebApp-Cmdlet überprüft, ob authentifizierte Benutzer mit lync Web App an lync Server-Konferenzen teilnehmen können.</span><span class="sxs-lookup"><span data-stu-id="9c585-115">The Test-CsWebApp cmdlet verifies that authenticated users can join Lync Server conferences by using the Lync Web App.</span></span> <span data-ttu-id="9c585-116">Wenn Sie das Cmdlet ausführen, Test-CsWebApp Kontakt mit dem Web Ticket-Dienst, um Web-Tickets für die angegebenen Benutzer zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="9c585-116">When you run the cmdlet, Test-CsWebApp contacts the Web Ticket service to obtain web tickets for the specified users.</span></span> <span data-ttu-id="9c585-117">Diese Tickets fungieren effektiv als "Eintrittskarten" für die lync Server-Konferenz.</span><span class="sxs-lookup"><span data-stu-id="9c585-117">These tickets effectively act as ‘admission tickets” to the Lync Server conference.</span></span> <span data-ttu-id="9c585-118">Wenn die Tickets abgerufen werden können und die Benutzer authentifiziert werden können, wenden sich Test-CsWebApp an den lync-Server und versuchen, getrennte Konferenzen für Chats, Anwendungsfreigabe und Datenzusammenarbeit einzurichten.</span><span class="sxs-lookup"><span data-stu-id="9c585-118">If the tickets can be retrieved, and if the users can be authenticated, Test-CsWebApp will then contact Lync Server and attempt to establish separate conferences for instant messaging, application sharing, and data collaboration.</span></span>

<span data-ttu-id="9c585-119">Beachten Sie, dass Test-CsWebApp nur die APIs und Verbindungen überprüft, die zum Erstellen dieser Konferenzen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9c585-119">Note that Test-CsWebApp just verifies the APIs and connections used to create these conferences.</span></span> <span data-ttu-id="9c585-120">Mit dem Cmdlet soll überprüft werden, ob lync Web App zum Erstellen und teilnehmen an Konferenzen verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="9c585-120">The cmdlet is designed to verify that Lync Web App could be used to create and join conferences.</span></span> <span data-ttu-id="9c585-121">Es wird jedoch nicht tatsächlich eine Konferenz erstellt und durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="9c585-121">However,, it does not actually create and conduct a conference.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="9c585-122">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="9c585-122">Running the test</span></span>

<span data-ttu-id="9c585-123">Das Test-CsWebApp-Cmdlet kann entweder mit einem Paar vorkonfigurierter Testkonten oder mit den Konten zweier Benutzer ausgeführt werden, die für lync Server aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="9c585-123">The Test-CsWebApp cmdlet can be run using either a pair of preconfigured test accounts or the accounts of any two users who are enabled for Lync Server.</span></span> <span data-ttu-id="9c585-124">Um diese Prüfung mit Testkonten auszuführen, müssen Sie lediglich den vollqualifizierten Domänennamen des lync-Server Pools angeben, der getestet wird.</span><span class="sxs-lookup"><span data-stu-id="9c585-124">To run this check using test accounts, you just have to specify the fully qualified domain name of the Lync Server pool being tested.</span></span> <span data-ttu-id="9c585-125">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9c585-125">For example:</span></span>

    Test-CsWebApp -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="9c585-126">Damit diese Überprüfung mit tatsächlichen Benutzerkonten ausgeführt werden kann, müssen Sie für jedes Konto zwei Windows PowerShell-Anmeldeinformationsobjekte (Objekte, die den Kontonamen und das Kennwort enthalten) erstellen.</span><span class="sxs-lookup"><span data-stu-id="9c585-126">To run this check using actual user accounts, you must create two Windows PowerShell credentials objects (objects that contain the account name and password) for each account.</span></span> <span data-ttu-id="9c585-127">Sie müssen dann diese Anmeldeinformationsobjekte und die SIP-Adressen der beiden Konten einbeziehen, wenn Sie Test-CsWebApp aufrufen:</span><span class="sxs-lookup"><span data-stu-id="9c585-127">You must then include those credentials objects and the SIP addresses of the two accounts when you call Test-CsWebApp:</span></span>

    $cred1 = Get-Credential "litwareinc\kenmyer"
    $cred2 = Get-Credential "litwareinc\pilar"
    
    Test-CsWebApp -TargetFqdn atl-cs-001.litwareinc.com -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $cred1 -User2SipAddress "sip:pilar@litwareinc.com" -User2Credential $cred2

<span data-ttu-id="9c585-128">Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Test-CsWebApp](https://docs.microsoft.com/powershell/module/skype/Test-CsWebApp) .</span><span class="sxs-lookup"><span data-stu-id="9c585-128">For more information, see the help topic for the [Test-CsWebApp](https://docs.microsoft.com/powershell/module/skype/Test-CsWebApp) cmdlet.</span></span> <span data-ttu-id="9c585-129">Beachten Sie, dass Test-CsWebApp für die Verwendung in lync Server 2013 als veraltet markiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9c585-129">Note that Test-CsWebApp was deprecated for use on Lync Server 2013.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="9c585-130">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="9c585-130">Determining success or failure</span></span>

<span data-ttu-id="9c585-131">Wenn Test-CsWebApp die Benutzer an Ihren Konferenzen teilnehmen können, gibt das Cmdlet den Erfolg des Testergebnisses zurück:</span><span class="sxs-lookup"><span data-stu-id="9c585-131">If Test-CsWebApp can join the users to their conferences, the cmdlet will return the test result Success:</span></span>

<span data-ttu-id="9c585-132">Ziel-FQDN:</span><span class="sxs-lookup"><span data-stu-id="9c585-132">Target Fqdn :</span></span>

<span data-ttu-id="9c585-133">Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="9c585-133">Result : Success</span></span>

<span data-ttu-id="9c585-134">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9c585-134">Latency : 00:00:00</span></span>

<span data-ttu-id="9c585-135">Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="9c585-135">Error Message :</span></span>

<span data-ttu-id="9c585-136">Diagnose</span><span class="sxs-lookup"><span data-stu-id="9c585-136">Diagnosis :</span></span>

<span data-ttu-id="9c585-137">Wenn die Benutzer nicht an den erforderlichen Konferenzen teilnehmen können, wird das Testergebnis als Fehler gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="9c585-137">If the users cannot join the necessary conferences then the test result will be marked as Failure.</span></span> <span data-ttu-id="9c585-138">In der Regel werden Test-CsWebApp auch eine detaillierte Fehlermeldung und Diagnose zurückmelden:</span><span class="sxs-lookup"><span data-stu-id="9c585-138">Typically Test-CsWebApp will also report back a detailed error message and diagnosis:</span></span>

<span data-ttu-id="9c585-139">Ziel-FQDN: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="9c585-139">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="9c585-140">Ergebnis: Fehler</span><span class="sxs-lookup"><span data-stu-id="9c585-140">Result : Failure</span></span>

<span data-ttu-id="9c585-141">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="9c585-141">Latency : 00:00:00</span></span>

<span data-ttu-id="9c585-142">Fehlermeldung: keine Antwort für Web-Ticket Dienst empfangen</span><span class="sxs-lookup"><span data-stu-id="9c585-142">Error Message : No response received for Web-Ticket service</span></span>

<span data-ttu-id="9c585-143">Diagnose: die HTTP-Anforderung ist mit dem Client nicht autorisiert</span><span class="sxs-lookup"><span data-stu-id="9c585-143">Diagnosis : The HTTP request is unauthorized with client</span></span>

<span data-ttu-id="9c585-144">Authentifizierungsschema "NTLM".</span><span class="sxs-lookup"><span data-stu-id="9c585-144">authentication scheme 'Ntlm'.</span></span> <span data-ttu-id="9c585-145">Die Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="9c585-145">The authentication</span></span>

<span data-ttu-id="9c585-146">der vom Server empfangene Header lautet "Negotiate, NTLM".</span><span class="sxs-lookup"><span data-stu-id="9c585-146">header received from the server was 'Negotiate,NTLM'.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="9c585-147">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="9c585-147">Reasons why the test might have failed</span></span>

<span data-ttu-id="9c585-148">Test-CsWebApp Ausfälle beinhalten in der Regelfehler bei der Benutzerauthentifizierung.</span><span class="sxs-lookup"><span data-stu-id="9c585-148">Test-CsWebApp failures typically involve user authentication errors.</span></span> <span data-ttu-id="9c585-149">Wenn Test-CsWebApp fehlschlägt, sollten Sie zuerst überprüfen, ob die angegebenen Benutzer über gültige Benutzerkonten verfügen und für lync Server aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="9c585-149">If Test-CsWebApp fails, you should first verify that the specified users have valid user accounts and are enabled for Lync Server.</span></span> <span data-ttu-id="9c585-150">Sie können Kontoinformationen abrufen, indem Sie einen Befehl wie den folgenden verwenden:</span><span class="sxs-lookup"><span data-stu-id="9c585-150">You can retrieve account information by using a command similar to this:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

<span data-ttu-id="9c585-151">Wenn die Enabled-Eigenschaft nicht gleich true ist oder der Befehl fehlschlägt, bedeutet dies, dass der Benutzer kein gültiges lync Server-Konto hat. Sie sollten auch sicherstellen, dass die für das Cmdlet angegebenen Kennwörter gültig sind.</span><span class="sxs-lookup"><span data-stu-id="9c585-151">If the Enabled property is not equal to True or if the command fails, that means that the user does not have a valid Lync Server account.You should also verify that the passwords that you supplied to the cmdlet are valid.</span></span>

<span data-ttu-id="9c585-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9c585-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

