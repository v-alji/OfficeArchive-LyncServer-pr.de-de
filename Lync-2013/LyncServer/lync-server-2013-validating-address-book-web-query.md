---
title: 'Lync Server 2013: Überprüfen der Adressbuch-Webabfrage'
description: 'Lync Server 2013: Überprüfen der Adressbuch-Webabfrage'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating address book web query
ms:assetid: e6ae0a5a-e131-4cfe-9a33-6e611831072d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720925(v=OCS.15)
ms:contentKeyID: 63969662
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e73c39fc33f8d1851fc89d277333a94aaa137790
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438904"
---
# <a name="validating-address-book-web-query-in-lync-server-2013"></a><span data-ttu-id="aa1ab-103">Überprüfen von Adressbuch-Webabfragen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aa1ab-103">Validating address book web query in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aa1ab-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aa1ab-104">

<span> </span></span></span>

<span data-ttu-id="aa1ab-105">_**Letztes Änderungsdatum des Themas:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="aa1ab-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="aa1ab-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="aa1ab-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="aa1ab-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="aa1ab-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="aa1ab-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="aa1ab-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="aa1ab-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="aa1ab-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="aa1ab-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="aa1ab-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="aa1ab-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="aa1ab-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsAddressBookWebQuery-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsAddressBookWebQuery cmdlet.</span></span> <span data-ttu-id="aa1ab-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="aa1ab-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsAddressBookWebQuery&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="aa1ab-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="aa1ab-114">Description</span></span>

<span data-ttu-id="aa1ab-115">Mithilfe des Test-CsAddressBookWebQuery-Cmdlets können Administratoren überprüfen, ob Benutzer den Adressbuch-Webabfrage Dienst verwenden können, um nach einem bestimmten Kontakt zu suchen.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-115">The Test-CsAddressBookWebQuery cmdlet enables administrators to verify that users can use the Address Book Web Query service to search for a specific contact.</span></span> <span data-ttu-id="aa1ab-116">Wenn Sie das Cmdlet ausführen, stellt Test-CsAddressBookWebQuery zunächst eine Verbindung mit dem Web-Ticket Dienst her, um authentifiziert zu werden.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-116">When you run the cmdlet, Test-CsAddressBookWebQuery will first connect to the Web Ticket service to be authenticated.</span></span> <span data-ttu-id="aa1ab-117">Wenn die Authentifizierung erfolgreich ist, stellt das Cmdlet eine Verbindung mit dem Adressbuch-Webabfrage Dienst her und sucht nach dem angegebenen Kontakt.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-117">If authentication is successful, the cmdlet will then connect to the Address Book Web Query service and search for the specified contact.</span></span> <span data-ttu-id="aa1ab-118">Wenn dieser Kontakt gefunden wird, versucht das Cmdlet, diese Informationen an den lokalen Computer zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-118">If that contact is found, the cmdlet will attempt to return that information to the local computer.</span></span> <span data-ttu-id="aa1ab-119">Der Test wird nur dann als erfolgreich markiert, wenn alle diese Schritte ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-119">The test will be marked a success only if all those steps can be completed.</span></span>

<span data-ttu-id="aa1ab-120">Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsAddressBookWebQuery](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery) .</span><span class="sxs-lookup"><span data-stu-id="aa1ab-120">For more information, see the Help documentation for the [Test-CsAddressBookWebQuery](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="aa1ab-121">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="aa1ab-121">Running the test</span></span>

<span data-ttu-id="aa1ab-122">Das Test-CsAddressBookWebQuery-Cmdlet kann entweder mit einem vorkonfigurierten Test Konto ausgeführt werden (siehe Einrichten von Testkonten zum Ausführen von lync Server-Tests) oder dem Konto eines beliebigen Benutzers, der für lync Server aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-122">The Test-CsAddressBookWebQuery cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who is enabled for Lync Server.</span></span> <span data-ttu-id="aa1ab-123">Damit diese Überprüfung mit einem Testkonto ausgeführt werden kann, müssen Sie lediglich den FQDN des lync Server-Pools und die SIP-Adresse des Benutzers angeben, der als Ziel für die Suche fungiert.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-123">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool and the SIP address of the user acting as the target of the search.</span></span> <span data-ttu-id="aa1ab-124">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="aa1ab-124">For example:</span></span>

    Test-CsAddressBookWebQuery -TargetFqdn "atl-cs-001.litwareinc.com" -TargetSipAddress "sip:davidlongmire@litwareinc.com"

<span data-ttu-id="aa1ab-125">Damit diese Überprüfung mit einem tatsächlichen Benutzerkonto ausgeführt werden kann, müssen Sie ein Windows PowerShell-Anmeldeinformationsobjekt erstellen, das einen gültigen Benutzernamen und ein Kennwort enthält.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-125">To run this check using an actual user account, you must create a Windows PowerShell credentials object that contains a valid user name and password.</span></span> <span data-ttu-id="aa1ab-126">Sie müssen dann das Anmeldeinformationsobjekt und die SIP-Adresse einbeziehen, die dem Konto zugewiesen ist, wenn der Code Test-CsAddressBookWebQuery aufruft:</span><span class="sxs-lookup"><span data-stu-id="aa1ab-126">You must then include that credentials object and the SIP address assigned to the account when the code calls Test-CsAddressBookWebQuery:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsAddressBookWebQuery -TargetFqdn "atl-cs-001.litwareinc.com" -TargetSipAddress "sip:davidlongmire@litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="aa1ab-127">Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsAddressBookWebQuery](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery) .</span><span class="sxs-lookup"><span data-stu-id="aa1ab-127">For more information, see the Help documentation for the [Test-CsAddressBookWebQuery](https://docs.microsoft.com/powershell/module/skype/Test-CsAddressBookWebQuery) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="aa1ab-128">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="aa1ab-128">Determining success or failure</span></span>

<span data-ttu-id="aa1ab-129">Wenn der angegebene Benutzer eine Verbindung mit dem Adressbuchdienst herstellen und die Zieladresse des Benutzers abrufen kann, geben Sie eine ähnliche Ausgabe zurück, wobei die Ergebniseigenschaft als erfolgreich markiert ist:</span><span class="sxs-lookup"><span data-stu-id="aa1ab-129">If the specified user can connect to the Address Book Service and retrieve the targeted user address, you'll return output similar to this with the Result property marked as Success:</span></span>

<span data-ttu-id="aa1ab-130">TargetUri https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="aa1ab-130">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="aa1ab-131">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="aa1ab-131">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="aa1ab-132">Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="aa1ab-132">Result : Success</span></span>

<span data-ttu-id="aa1ab-133">Latenz: 00:00:06.2611356</span><span class="sxs-lookup"><span data-stu-id="aa1ab-133">Latency : 00:00:06.2611356</span></span>

<span data-ttu-id="aa1ab-134">Fehler</span><span class="sxs-lookup"><span data-stu-id="aa1ab-134">Error :</span></span>

<span data-ttu-id="aa1ab-135">Diagnose</span><span class="sxs-lookup"><span data-stu-id="aa1ab-135">Diagnosis :</span></span>

<span data-ttu-id="aa1ab-136">Wenn der angegebene Benutzer keine Verbindung herstellen kann oder wenn die Zielbenutzer Adresse nicht abgerufen werden kann, wird das Ergebnis als Fehler angezeigt, und weitere Informationen werden in den Eigenschaften Fehler und Diagnose aufgezeichnet:</span><span class="sxs-lookup"><span data-stu-id="aa1ab-136">If the specified user can't connect or if the target user address cannot be retrieved, then the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="aa1ab-137">TargetUri https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="aa1ab-137">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="aa1ab-138">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="aa1ab-138">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="aa1ab-139">Ergebnis: Fehler</span><span class="sxs-lookup"><span data-stu-id="aa1ab-139">Result : Failure</span></span>

<span data-ttu-id="aa1ab-140">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="aa1ab-140">Latency : 00:00:00</span></span>

<span data-ttu-id="aa1ab-141">Fehler: die Adressbuch-Webdienstanforderung ist mit dem Antwortcode fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-141">Error : Address Book Web service request has failed with response code</span></span>

<span data-ttu-id="aa1ab-142">NoEntryFound.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-142">NoEntryFound.</span></span>

<span data-ttu-id="aa1ab-143">Diagnose</span><span class="sxs-lookup"><span data-stu-id="aa1ab-143">Diagnosis :</span></span>

<span data-ttu-id="aa1ab-144">In der vorherigen Ausgabe wird angegeben, dass der Test fehlgeschlagen ist, weil der Zielbenutzer nicht gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-144">The previous output states that the test failed because the target user couldn't be found.</span></span> <span data-ttu-id="aa1ab-145">Sie können feststellen, ob eine gültige SIP-Adresse an Test-CsAddressBookWebQuery übergeben wurde, indem Sie einen Befehl wie den folgenden ausführen:</span><span class="sxs-lookup"><span data-stu-id="aa1ab-145">You can determine whether or not a valid SIP address was passed to Test-CsAddressBookWebQuery by running a command similar to the following:</span></span>

    Get-CsUser | Where-Object {$_.SipAddress -eq "sip:davidlongmire@litwareinc.com"

<span data-ttu-id="aa1ab-146">Wenn Test-CsAddressBookWebQuery fehlschlägt, möchten Sie möglicherweise den Test erneut ausführen, wobei dieser Zeitpunkt einschließlich des Verbose-Parameters lautet:</span><span class="sxs-lookup"><span data-stu-id="aa1ab-146">If Test-CsAddressBookWebQuery fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsAddressBookWebQuery -TargetFqdn "atl-cs-001.litwareinc.com" -TargetSipAddress "sip:davidlongmire@litwareinc.com" -Verbose

<span data-ttu-id="aa1ab-147">Wenn der Parameter Verbose enthalten ist, gibt Test-CsAddressBookWebQuery ein schrittweises Konto für jede Aktion zurück, die versucht wurde, während die Möglichkeit des angegebenen Benutzers zur Anmeldung bei lync Server überprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-147">When the Verbose parameter is included, Test-CsAddressBookWebQuery will return a step-by-step account of each action it tried while checking the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="aa1ab-148">Diese Ausgabe zeigt beispielsweise an, dass Test-CsAddressBookWebQuery eine Verbindung mit dem Adressbuchdienst herstellen konnte, aber die Ziel-SIP-Adresse nicht finden konnte:</span><span class="sxs-lookup"><span data-stu-id="aa1ab-148">For example, this output indicates that Test-CsAddressBookWebQuery was able to connect to the Address Book Service, but was not able to locate the target SIP address:</span></span>

<span data-ttu-id="aa1ab-149">Die Aktivität "QueryAddressBookWebService" wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-149">'QueryAddressBookWebService' activity started.</span></span>

<span data-ttu-id="aa1ab-150">Aufruf des Adressbuch-Webabfrage Diensts.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-150">Calling Address Book Web Query Service.</span></span> <span data-ttu-id="aa1ab-151">ABWS URL =</span><span class="sxs-lookup"><span data-stu-id="aa1ab-151">ABWS URL =</span></span>

https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc

<span data-ttu-id="aa1ab-152">Ausnahme für Adressbuch Abfragen: die Adressbuch-Webdienstanforderung ist mit dem Antwortcode NoEntryFound fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-152">Address book query exception : Address Book Web service request has failed with response code NoEntryFound.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="aa1ab-153">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="aa1ab-153">Reasons Why the Test Might Have Failed</span></span>

<span data-ttu-id="aa1ab-154">Im folgenden finden Sie einige häufige Gründe, warum Test-CsAddressBookWebQuery fehlschlagen kann:</span><span class="sxs-lookup"><span data-stu-id="aa1ab-154">Here are some common reasons why Test-CsAddressBookWebQuery might fail:</span></span>

  - <span data-ttu-id="aa1ab-155">Sie haben ein ungültiges Benutzerkonto angegeben.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-155">You specified an invalid user account.</span></span> <span data-ttu-id="aa1ab-156">Sie können überprüfen, ob ein Benutzerkonto vorhanden ist, indem Sie einen Befehl wie den folgenden ausführen:</span><span class="sxs-lookup"><span data-stu-id="aa1ab-156">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="aa1ab-157">Das Benutzerkonto ist gültig, aber das Konto ist derzeit nicht für lync Server aktiviert.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-157">The user account is valid, but the account is not currently enabled for Lync Server.</span></span> <span data-ttu-id="aa1ab-158">Führen Sie einen Befehl ähnlich der folgenden aus, um zu überprüfen, ob ein Benutzerkonto für lync Server aktiviert wurde:</span><span class="sxs-lookup"><span data-stu-id="aa1ab-158">To verify that a user account has been enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="aa1ab-159">Wenn die Enabled-Eigenschaft auf false festgelegt ist, bedeutet dies, dass der Benutzer zurzeit nicht für lync Server aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-159">If the Enabled property is set to False that means that the user is not currently enabled for Lync Server.</span></span>

  - <span data-ttu-id="aa1ab-160">Der Zielbenutzer befindet sich möglicherweise nicht im Adressbuch.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-160">The target user might not be in the Address Book.</span></span>

  - <span data-ttu-id="aa1ab-161">Das Adressbuch wurde möglicherweise nicht vollständig aktualisiert und repliziert.</span><span class="sxs-lookup"><span data-stu-id="aa1ab-161">The Address Book might not have fully updated and replicated.</span></span> <span data-ttu-id="aa1ab-162">Sie können eine Aktualisierung aller Adressbuchserver in Ihrer Organisation erzwingen, indem Sie den folgenden Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="aa1ab-162">You can force an update of all the Address Book Servers in your organization by running the following command:</span></span>
    
        Update-CsAddressBook

<span data-ttu-id="aa1ab-163"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aa1ab-163"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

