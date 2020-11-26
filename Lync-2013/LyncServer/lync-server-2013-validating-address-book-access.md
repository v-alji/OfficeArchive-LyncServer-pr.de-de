---
title: 'Lync Server 2013: Überprüfen des Zugriffs auf das Adressbuch'
description: 'Lync Server 2013: Überprüfen des Zugriffs auf das Adressbuch'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating address book access
ms:assetid: 630682c6-9262-46c5-9af1-6193db70374b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720916(v=OCS.15)
ms:contentKeyID: 63969611
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6da08e48be24b3325bc1f415b9baa3c9197717c3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438631"
---
# <a name="validating-address-book-access-in-lync-server-2013"></a><span data-ttu-id="7dd62-103">Überprüfen des Adressbuch Zugriffs in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7dd62-103">Validating address book access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7dd62-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7dd62-104">

<span> </span></span></span>

<span data-ttu-id="7dd62-105">_**Letztes Änderungsdatum des Themas:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="7dd62-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7dd62-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="7dd62-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="7dd62-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="7dd62-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7dd62-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="7dd62-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="7dd62-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="7dd62-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7dd62-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="7dd62-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="7dd62-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="7dd62-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="7dd62-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsAddressBookService-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="7dd62-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsAddressBookService cmdlet.</span></span> <span data-ttu-id="7dd62-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="7dd62-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsAddressBookService&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="7dd62-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="7dd62-114">Description</span></span>

<span data-ttu-id="7dd62-115">Das Test-CsAddressBookService-Cmdlet bietet eine Möglichkeit, um zu überprüfen, ob ein Benutzer eine Verbindung mit dem Adressbuch Download-Webdienst herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="7dd62-115">The Test-CsAddressBookService cmdlet provides a way for you to verify that a user can connect to the Address Book Download Web service.</span></span> <span data-ttu-id="7dd62-116">Wenn Sie das Cmdlet ausführen, stellt Test-CsAddressBookService eine Verbindung mit dem Adressbuch Download-Webdienst im angegebenen Pool her und fordert den Speicherort der Adressbuchdateien an.</span><span class="sxs-lookup"><span data-stu-id="7dd62-116">When you run the cmdlet, Test-CsAddressBookService connects to the Address Book Download Web service on the specified pool and requests the location of the Address Book files.</span></span> <span data-ttu-id="7dd62-117">Wenn das Adressbuch, das vom Webdienst heruntergeladen wird, diesen Speicherort bereitstellt, wird der Test als erfolgreich angesehen.</span><span class="sxs-lookup"><span data-stu-id="7dd62-117">If the Address Book Download Web service supplies that location, the test is considered successful.</span></span> <span data-ttu-id="7dd62-118">Wenn die Anforderung abgelehnt wird, wird der Test als Fehler gewertet.</span><span class="sxs-lookup"><span data-stu-id="7dd62-118">If the request is denied, then the test is considered a failure.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="7dd62-119">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="7dd62-119">Running the test</span></span>

<span data-ttu-id="7dd62-120">Das Test-CsAddressBookService-Cmdlet kann entweder mit einem vorkonfigurierten Test Konto ausgeführt werden (siehe Einrichten von Testkonten für die Ausführung von lync Server-Tests) oder dem Konto eines beliebigen Benutzers, der für lync Server aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="7dd62-120">The Test-CsAddressBookService cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who has been enabled for Lync Server.</span></span> <span data-ttu-id="7dd62-121">Um diese Überprüfung mit einem Testkonto auszuführen, müssen Sie lediglich den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des zu testenden lync-Server Pools angeben.</span><span class="sxs-lookup"><span data-stu-id="7dd62-121">To run this check using a test account, all you need to do is specify the fully qualified domain name (FQDN) of the Lync Server pool being tested.</span></span> <span data-ttu-id="7dd62-122">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="7dd62-122">For example:</span></span>

    Test-CsAddressBookService -TargetFqdn "atl-cs-001.litwareinc.com"

<span data-ttu-id="7dd62-123">Damit diese Überprüfung mit einem tatsächlichen Benutzerkonto ausgeführt werden kann, müssen Sie zuerst ein Windows PowerShell-Anmeldeinformationsobjekt erstellen, das den Kontonamen und das Kennwort enthält.</span><span class="sxs-lookup"><span data-stu-id="7dd62-123">To run this check using an actual user account, you must first create a Windows PowerShell credentials object that contains the account name and password.</span></span> <span data-ttu-id="7dd62-124">Sie müssen das Anmeldeinformationsobjekt und die SIP-Adresse, die dem Konto zugewiesen ist, beim Aufrufen von Test-CsAddressBookService einfügen:</span><span class="sxs-lookup"><span data-stu-id="7dd62-124">You must then include that credentials object and the SIP address assigned to the account when calling Test-CsAddressBookService:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsAddressBookService -TargetFqdn "atl-cs-001.litwareinc.com"-UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="7dd62-125">Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsAddressBookService](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookService) .</span><span class="sxs-lookup"><span data-stu-id="7dd62-125">For more information, see the Help documentation for the [Test-CsAddressBookService](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookService) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="7dd62-126">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="7dd62-126">Determining success or failure</span></span>

<span data-ttu-id="7dd62-127">Wenn der angegebene Benutzer in der Lage ist, eine Verbindung mit dem Adressbuchdienst herzustellen, erhalten Sie eine ähnliche Ausgabe wie diese, wobei die Eigenschaft Ergebnis als **erfolgreich** markiert ist:</span><span class="sxs-lookup"><span data-stu-id="7dd62-127">If the specified user is able to connect to the Address Book Service you will get back output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="7dd62-128">TargetUri https://lync-se.fabrikam.com:443/abs/handler</span><span class="sxs-lookup"><span data-stu-id="7dd62-128">TargetUri : https://lync-se.fabrikam.com:443/abs/handler</span></span>

<span data-ttu-id="7dd62-129">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="7dd62-129">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="7dd62-130">Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="7dd62-130">Result : Success</span></span>

<span data-ttu-id="7dd62-131">Latenz: 00:00:06.2260399</span><span class="sxs-lookup"><span data-stu-id="7dd62-131">Latency : 00:00:06.2260399</span></span>

<span data-ttu-id="7dd62-132">Fehler</span><span class="sxs-lookup"><span data-stu-id="7dd62-132">Error :</span></span>

<span data-ttu-id="7dd62-133">Diagnose</span><span class="sxs-lookup"><span data-stu-id="7dd62-133">Diagnosis :</span></span>

<span data-ttu-id="7dd62-134">Wenn der angegebene Benutzer diese Verbindung nicht herstellen kann, wird das Ergebnis als Fehler angezeigt, und weitere Informationen werden in den Eigenschaften Fehler und Diagnose aufgezeichnet:</span><span class="sxs-lookup"><span data-stu-id="7dd62-134">If the specified user is not able to make this connection, the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="7dd62-135">TargetUri</span><span class="sxs-lookup"><span data-stu-id="7dd62-135">TargetUri :</span></span>

<span data-ttu-id="7dd62-136">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="7dd62-136">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="7dd62-137">Ergebnis: Fehler</span><span class="sxs-lookup"><span data-stu-id="7dd62-137">Result : Failure</span></span>

<span data-ttu-id="7dd62-138">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="7dd62-138">Latency : 00:00:00</span></span>

<span data-ttu-id="7dd62-139">Diagnose: errorCode = 4005, Source = ATL-CS-001.litwareinc.com,</span><span class="sxs-lookup"><span data-stu-id="7dd62-139">Diagnosis : ErrorCode=4005,Source=atl-cs-001.litwareinc.com,</span></span>

<span data-ttu-id="7dd62-140">Reason = Ziel-URI ist entweder für SIP nicht aktiviert oder nicht</span><span class="sxs-lookup"><span data-stu-id="7dd62-140">Reason=Destination URI either not enabled for SIP or does not</span></span>

<span data-ttu-id="7dd62-141">existieren.</span><span class="sxs-lookup"><span data-stu-id="7dd62-141">exist.</span></span>

<span data-ttu-id="7dd62-142">Microsoft. RTC. Signalisierungs-DiagnosticHeader</span><span class="sxs-lookup"><span data-stu-id="7dd62-142">Microsoft.Rtc.Signaling.DiagnosticHeader</span></span>

<span data-ttu-id="7dd62-143">In der vorhergehenden Ausgabe wird beispielsweise festgestellt, dass der Test fehlgeschlagen ist, weil der angegebene Benutzer (also der "Ziel-URI") entweder nicht vorhanden ist oder für lync Server nicht aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="7dd62-143">For example, the preceding output states that the test failed because the specified user (that is, the “Destination URI”) either does not exist or has not been enabled for Lync Server.</span></span> <span data-ttu-id="7dd62-144">Sie können überprüfen, ob ein Benutzerkonto gültig ist, und sicherstellen, dass Sie die richtige SIP-Adresse angegeben haben, indem Sie einen Befehl wie den folgenden ausführen:</span><span class="sxs-lookup"><span data-stu-id="7dd62-144">You can verify whether or not a user account is valid, and verify that you supplied the correct SIP address, by running a command like this one:</span></span>

<span data-ttu-id="7dd62-145">Get-CsUser-Identity "SIP:kenmyer@litwareinc.com" | Select-Object SipAddress, aktiviert</span><span class="sxs-lookup"><span data-stu-id="7dd62-145">Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, Enabled</span></span>

<span data-ttu-id="7dd62-146">Wenn Test-CsAddressBookService fehlschlägt, möchten Sie möglicherweise den Test erneut ausführen, wobei dieser Zeitpunkt einschließlich des Verbose-Parameters lautet:</span><span class="sxs-lookup"><span data-stu-id="7dd62-146">If Test-CsAddressBookService fails then you might want to rerun the test, this time including the Verbose parameter:</span></span>

<span data-ttu-id="7dd62-147">Test-CsAddressBookService-TargetFqdn "ATL-CS-001.litwareinc.com"-Verbose</span><span class="sxs-lookup"><span data-stu-id="7dd62-147">Test-CsAddressBookService -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose</span></span>

<span data-ttu-id="7dd62-148">Wenn der Verbose-Parameter enthalten ist Test-CsAddressBookService gibt eine Schritt-für-Schritt-Konto für jede Aktion zurück, die beim Überprüfen der Fähigkeit des angegebenen Benutzers zur Anmeldung bei lync Server versucht wurde.</span><span class="sxs-lookup"><span data-stu-id="7dd62-148">When the Verbose parameter is included Test-CsAddressBookService will return a step-by-step account of each action it attempted when checking the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="7dd62-149">Diese Beispielausgabe zeigt beispielsweise, dass Test-CsAddressBookService, zumindest in diesem Beispiel, die Adressbuchdatei herunterladen konnte:</span><span class="sxs-lookup"><span data-stu-id="7dd62-149">For example, this sample output shows that Test-CsAddressBookService, at least in this example, was able to download the Address Book file:</span></span>

<span data-ttu-id="7dd62-150">Sendet eine HTTP GET-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="7dd62-150">Sending Http GET Request.</span></span>

<span data-ttu-id="7dd62-151">Dateipfad = https://atl-cs-001.litwareinc.com:443/abs/handler/f-1299.lsabs</span><span class="sxs-lookup"><span data-stu-id="7dd62-151">File Path = https://atl-cs-001.litwareinc.com:443/abs/handler/f-1299.lsabs</span></span>

<span data-ttu-id="7dd62-152">Nummer des Versuchs = 1</span><span class="sxs-lookup"><span data-stu-id="7dd62-152">Attempt Number = 1</span></span>

<span data-ttu-id="7dd62-153">Timeout (MS) = 60000</span><span class="sxs-lookup"><span data-stu-id="7dd62-153">TimeOut (msec) = 60000</span></span>

<span data-ttu-id="7dd62-154">Die ABS-Datei wurde erfolgreich heruntergeladen https://atl-cs-001.litwareinc.com:443/abs/handler/f-1299.lsabs</span><span class="sxs-lookup"><span data-stu-id="7dd62-154">Successfully Downloaded the ABS file https://atl-cs-001.litwareinc.com:443/abs/handler/f-1299.lsabs</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="7dd62-155">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="7dd62-155">Reasons why the test might have failed</span></span>

<span data-ttu-id="7dd62-156">Im folgenden finden Sie einige häufige Gründe, warum Test-CsAddressBookService fehlschlagen kann:</span><span class="sxs-lookup"><span data-stu-id="7dd62-156">Here are some common reasons why Test-CsAddressBookService might fail:</span></span>

  - <span data-ttu-id="7dd62-157">Sie haben ein ungültiges Benutzerkonto angegeben.</span><span class="sxs-lookup"><span data-stu-id="7dd62-157">You specified an invalid user account.</span></span> <span data-ttu-id="7dd62-158">Sie können überprüfen, ob ein Benutzerkonto vorhanden ist, indem Sie einen Befehl wie den folgenden ausführen:</span><span class="sxs-lookup"><span data-stu-id="7dd62-158">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="7dd62-159">Das Benutzerkonto ist gültig, aber das Konto ist derzeit nicht für lync Server aktiviert.</span><span class="sxs-lookup"><span data-stu-id="7dd62-159">The user account is valid, but the account is not currently enabled for Lync Server.</span></span> <span data-ttu-id="7dd62-160">Führen Sie einen Befehl ähnlich der folgenden aus, um zu überprüfen, ob ein Benutzerkonto für lync Server aktiviert wurde:</span><span class="sxs-lookup"><span data-stu-id="7dd62-160">To verify that a user account has been enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="7dd62-161">Wenn die Enabled-Eigenschaft auf false festgelegt ist, bedeutet dies, dass der Benutzer zurzeit nicht für lync Server aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="7dd62-161">If the Enabled property is set to False that means that the user is not currently enabled for Lync Server.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7dd62-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7dd62-162">See Also</span></span>


[<span data-ttu-id="7dd62-163">Test-CsAddressBookService</span><span class="sxs-lookup"><span data-stu-id="7dd62-163">Test-CsAddressBookService</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookService)  
  

<span data-ttu-id="7dd62-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7dd62-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

