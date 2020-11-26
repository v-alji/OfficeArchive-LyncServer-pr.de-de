---
title: 'Lync Server 2013: Testen der Fähigkeit, Gruppen Erweiterungen zu verwenden'
description: 'Lync Server 2013: Testen der Fähigkeit, Gruppen Erweiterungen zu verwenden.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing ability to employ group expansion
ms:assetid: 9b0fc954-6f9c-411a-ab32-94ebabc42de2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743836(v=OCS.15)
ms:contentKeyID: 63969634
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6267bc2099fc420c5c57e1ef80f4bf4491334938
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441109"
---
# <a name="testing-ability-to-employ-group-expansion-in-lync-server-2013"></a><span data-ttu-id="3daf4-103">Testen der Möglichkeit zur Verwendung der Gruppenerweiterung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3daf4-103">Testing ability to employ group expansion in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3daf4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3daf4-104">

<span> </span></span></span>

<span data-ttu-id="3daf4-105">_**Letztes Änderungsdatum des Themas:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="3daf4-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3daf4-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="3daf4-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="3daf4-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="3daf4-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3daf4-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="3daf4-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="3daf4-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="3daf4-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3daf4-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="3daf4-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="3daf4-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="3daf4-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="3daf4-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsGroupExpansion-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="3daf4-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsGroupExpansion cmdlet.</span></span> <span data-ttu-id="3daf4-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="3daf4-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsGroupExpansion&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="3daf4-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3daf4-114">Description</span></span>

<span data-ttu-id="3daf4-115">Mit dem Test-CsGroupExpansion-Cmdlet können Sie ermitteln, ob die Gruppenerweiterung in Ihrer Organisation funktioniert.</span><span class="sxs-lookup"><span data-stu-id="3daf4-115">The Test-CsGroupExpansion cmdlet lets you determine whether group expansion is working within your organization.</span></span> <span data-ttu-id="3daf4-116">Wenn die Gruppenerweiterung aktiviert ist, konfigurieren Benutzer Verteilergruppen als Kontakt.</span><span class="sxs-lookup"><span data-stu-id="3daf4-116">When group expansion is enabled, users configure distribution groups as a contact.</span></span> <span data-ttu-id="3daf4-117">Das bedeutet, dass diese Benutzer dann die gleiche Sofortnachricht an alle Gruppenmitglieder senden können, indem Sie die Nachricht an die Gruppe anstatt an einzelne Mitglieder dieser Gruppe adressieren.</span><span class="sxs-lookup"><span data-stu-id="3daf4-117">That means that those users can then send the same instant message to all the group members by addressing the message to the group instead of to individual members of that group.</span></span> <span data-ttu-id="3daf4-118">Mit der Gruppenerweiterung können Sie alle Gruppenmitglieder und deren aktuellen Status schnell und einfach anzeigen.</span><span class="sxs-lookup"><span data-stu-id="3daf4-118">Group expansion enables you to quickly and easily view all the group members and their current status.</span></span>

<span data-ttu-id="3daf4-119">Mit dem Test-CsGroupExpansion-Cmdlet geben Sie eine Active Directory-Verteilergruppe an, indem Sie die e-Mail-Adresse der Gruppe verwenden.</span><span class="sxs-lookup"><span data-stu-id="3daf4-119">With the Test-CsGroupExpansion cmdlet, you specify an Active Directory distribution group by using the group’s email address.</span></span> <span data-ttu-id="3daf4-120">Test-CsGroupExpansion verwendet dann die Gruppenerweiterung, um die Gruppenmitgliedschaft abzurufen, und vergleicht die abgerufene Liste mit der Mitgliedschaft der von Ihnen angegebenen Gruppen-e-Mail-Adresse.</span><span class="sxs-lookup"><span data-stu-id="3daf4-120">Test-CsGroupExpansion then uses group expansion to retrieve the group membership and compare the retrieved list to the membership of the group email address that you supplied.</span></span> <span data-ttu-id="3daf4-121">Wenn die beiden Listen übereinstimmen, funktioniert die Gruppenerweiterung ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="3daf4-121">If the two lists match, then group expansion is working correctly.</span></span> <span data-ttu-id="3daf4-122">Beachten Sie, dass Sie die Gruppenerweiterung auf zwei Arten testen können: durch Testen des Diensts selbst oder durch Testen des zugehörigen Webdiensts.</span><span class="sxs-lookup"><span data-stu-id="3daf4-122">Note that you can test group expansion in two ways: by testing the service itself or by testing the associated web service.</span></span>

<span data-ttu-id="3daf4-123">Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) .</span><span class="sxs-lookup"><span data-stu-id="3daf4-123">For more information, see the Help documentation for the [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) cmdlet.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="3daf4-124">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="3daf4-124">Running the test</span></span>

<span data-ttu-id="3daf4-125">Das Test-CsGroupExpansion-Cmdlet kann entweder mit einem vorkonfigurierten Test Konto ausgeführt werden (siehe Einrichten von Testkonten zum Ausführen von lync Server-Tests) oder dem Konto eines beliebigen Benutzers, der für lync Server aktiviert war.</span><span class="sxs-lookup"><span data-stu-id="3daf4-125">The Test-CsGroupExpansion cmdlet can be run using either a preconfigured test account (see Setting Up Test Accounts for Running Lync Server Tests) or the account of any user who was enabled for Lync Server.</span></span> <span data-ttu-id="3daf4-126">Um diese Überprüfung mit einem Testkonto auszuführen, müssen Sie lediglich den FQDN des zu testenden lync-Server Pools und die e-Mail-Adresse für eine gültige Verteilergruppe angeben.</span><span class="sxs-lookup"><span data-stu-id="3daf4-126">To run this check using a test account, you just have to specify the FQDN of the Lync Server pool being tested and the email address for a valid distribution group.</span></span> <span data-ttu-id="3daf4-127">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="3daf4-127">For example:</span></span>

    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com"

<span data-ttu-id="3daf4-128">Damit diese Überprüfung mit einem tatsächlichen Benutzerkonto ausgeführt werden kann, müssen Sie zuerst ein lync Server-Anmeldeinformationsobjekt erstellen, das den Kontonamen und das Kennwort enthält.</span><span class="sxs-lookup"><span data-stu-id="3daf4-128">To run this check using an actual user account, you must first create a Lync Server credentials object that contains the account name and password.</span></span> <span data-ttu-id="3daf4-129">Sie müssen dann das Anmeldeinformationsobjekt und die SIP-Adresse einbeziehen, die dem Konto zugewiesen ist, wenn das System Test-CsGroupExpansion aufruft:</span><span class="sxs-lookup"><span data-stu-id="3daf4-129">You must then include that credentials object and the SIP address assigned to the account when the system calls Test-CsGroupExpansion:</span></span>

    $credential = Get-Credential "litwareinc\kenmyer"
    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com" -UserSipAddress "sip:kenmyer@litwareinc.com" -UserCredential $credential

<span data-ttu-id="3daf4-130">Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) .</span><span class="sxs-lookup"><span data-stu-id="3daf4-130">For more information, see the Help documentation for the [Test-CsGroupExpansion](https://docs.microsoft.com/powershell/module/skype/Test-CsGroupExpansion) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="3daf4-131">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="3daf4-131">Determining success or failure</span></span>

<span data-ttu-id="3daf4-132">Wenn der angegebene Benutzer die Gruppenerweiterung verwenden kann, erhalten Sie eine ähnliche Ausgabe, wobei die Ergebniseigenschaft als erfolgreich markiert ist **:**</span><span class="sxs-lookup"><span data-stu-id="3daf4-132">If the specified user can use group expansion, you'll receive output similar to this with the Result property marked as **Success:**</span></span>

<span data-ttu-id="3daf4-133">TargetUri https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="3daf4-133">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="3daf4-134">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="3daf4-134">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="3daf4-135">Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="3daf4-135">Result : Success</span></span>

<span data-ttu-id="3daf4-136">Latenz: 00:00:01.1234976</span><span class="sxs-lookup"><span data-stu-id="3daf4-136">Latency : 00:00:01.1234976</span></span>

<span data-ttu-id="3daf4-137">Fehler</span><span class="sxs-lookup"><span data-stu-id="3daf4-137">Error :</span></span>

<span data-ttu-id="3daf4-138">Diagnose</span><span class="sxs-lookup"><span data-stu-id="3daf4-138">Diagnosis :</span></span>

<span data-ttu-id="3daf4-139">Wenn der angegebene Benutzer keine Gruppenerweiterung verwenden kann, wird das Ergebnis als Fehler angezeigt, und zusätzliche Informationen werden in den Eigenschaften Fehler und Diagnose aufgezeichnet:</span><span class="sxs-lookup"><span data-stu-id="3daf4-139">If the specified user can't use group expansion, then the Result will be shown as Failure and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="3daf4-140">TargetUri https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span><span class="sxs-lookup"><span data-stu-id="3daf4-140">TargetUri : https://atl-cs-001.litwareinc.com:443/groupexpansion/service.svc</span></span>

<span data-ttu-id="3daf4-141">TargetFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="3daf4-141">TargetFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="3daf4-142">Ergebnis: Fehler</span><span class="sxs-lookup"><span data-stu-id="3daf4-142">Result : Failure</span></span>

<span data-ttu-id="3daf4-143">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="3daf4-143">Latency : 00:00:00</span></span>

<span data-ttu-id="3daf4-144">Fehler</span><span class="sxs-lookup"><span data-stu-id="3daf4-144">Error :</span></span>

<span data-ttu-id="3daf4-145">Diagnose</span><span class="sxs-lookup"><span data-stu-id="3daf4-145">Diagnosis :</span></span>

<span data-ttu-id="3daf4-146">Test-CsGroupExpansion: der Endpunkt konnte nicht registriert werden.</span><span class="sxs-lookup"><span data-stu-id="3daf4-146">Test-CsGroupExpansion : The endpoint was unable to register.</span></span> <span data-ttu-id="3daf4-147">Lesen Sie den ErrorCode aus bestimmten Gründen.</span><span class="sxs-lookup"><span data-stu-id="3daf4-147">See the ErrorCode for specific reason.</span></span>

<span data-ttu-id="3daf4-148">In der vorherigen Ausgabe wird angegeben, dass der Test fehlgeschlagen ist, weil der angegebene Benutzer sich nicht bei lync Server registrieren konnte.</span><span class="sxs-lookup"><span data-stu-id="3daf4-148">The previous output states that the test failed because the specified user was unable to register with Lync Server.</span></span> <span data-ttu-id="3daf4-149">Dies erfolgt in der Regel, wenn das Testkonto nicht vorhanden ist oder für lync Server nicht aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3daf4-149">This will typically occur if the test account does not exist or has not enabled for Lync Server.</span></span> <span data-ttu-id="3daf4-150">Sie können überprüfen, ob das Konto vorhanden ist, und ermitteln, ob das Konto für nm-OCS-14-3rd aktiviert wurde, indem Sie einen Befehl wie den folgenden ausführen:</span><span class="sxs-lookup"><span data-stu-id="3daf4-150">You can verify that the account exists, and determine whether or not the account has been enabled for nm-ocs-14-3rd by running a command similar to the following:</span></span>

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object SipAddress, Enabled

<span data-ttu-id="3daf4-151">Wenn Test-CsGroupExpansion fehlschlägt, möchten Sie möglicherweise den Test erneut ausführen, wobei dieser Zeitpunkt einschließlich des Verbose-Parameters lautet:</span><span class="sxs-lookup"><span data-stu-id="3daf4-151">If Test-CsGroupExpansion fails, then you might want to rerun the test, this time including the Verbose parameter:</span></span>

    Test-CsGroupExpansion -TargetFqdn "atl-cs-001.litwareinc.com" -GroupEmailAddress "Sales@litwareinc.com" -Verbose

<span data-ttu-id="3daf4-152">Wenn der Verbose-Parameter enthalten ist Test-CsGroupExpansion gibt eine Schritt-für-Schritt-Konto für jede Aktion zurück, die versucht wurde, als die Möglichkeit des angegebenen Benutzers zur Anmeldung bei lync Server geprüft wurde.</span><span class="sxs-lookup"><span data-stu-id="3daf4-152">When the Verbose parameter is included Test-CsGroupExpansion will return a step-by-step account of each action it tried when it checked the ability of the specified user to log on to Lync Server.</span></span> <span data-ttu-id="3daf4-153">Diese Ausgabe gibt beispielsweise an, dass die angegebene Verteilergruppe nicht gefunden wurde:</span><span class="sxs-lookup"><span data-stu-id="3daf4-153">For example, this output indicates that the specified distribution group couldn't be found:</span></span>

<span data-ttu-id="3daf4-154">Sie versuchen, Web-Ticket zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3daf4-154">Trying to get web ticket.</span></span>

<span data-ttu-id="3daf4-155">Webdienst-URL: https://atl-cs-001.litwareinc.com:443/WebTicket/WebTicketService.svc</span><span class="sxs-lookup"><span data-stu-id="3daf4-155">Web Service url : https://atl-cs-001.litwareinc.com:443/WebTicket/WebTicketService.svc</span></span>

<span data-ttu-id="3daf4-156">Verwenden von NTLM/Kerb auth</span><span class="sxs-lookup"><span data-stu-id="3daf4-156">Using NTLM/Kerb auth.</span></span>

<span data-ttu-id="3daf4-157">GetWebTicketActivity abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="3daf4-157">GetWebTicketActivity completed.</span></span>

<span data-ttu-id="3daf4-158">Die Aktivität "VerifyDistributionList" wurde gestartet.</span><span class="sxs-lookup"><span data-stu-id="3daf4-158">'VerifyDistributionList' activity started.</span></span>

<span data-ttu-id="3daf4-159">Der Antwort Status des dlx-Webdiensts lautet: NotFound.</span><span class="sxs-lookup"><span data-stu-id="3daf4-159">DLX Web Service Response Status is: NotFound.</span></span>

<span data-ttu-id="3daf4-160">"VerifyDistributionList"-Aktivität wurde in "0,2597923" Sek. abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="3daf4-160">'VerifyDistributionList' activity completed in '0.2597923' secs.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="3daf4-161">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="3daf4-161">Reasons why the test might have failed</span></span>

<span data-ttu-id="3daf4-162">Im folgenden finden Sie einige häufige Gründe, warum Test-CsGroupExpansion fehlschlagen kann:</span><span class="sxs-lookup"><span data-stu-id="3daf4-162">Here are some common reasons why Test-CsGroupExpansion might fail:</span></span>

  - <span data-ttu-id="3daf4-163">Sie haben ein ungültiges Benutzerkonto angegeben.</span><span class="sxs-lookup"><span data-stu-id="3daf4-163">You specified an invalid user account.</span></span> <span data-ttu-id="3daf4-164">Sie können überprüfen, ob ein Benutzerkonto vorhanden ist, indem Sie einen Befehl wie den folgenden ausführen:</span><span class="sxs-lookup"><span data-stu-id="3daf4-164">You can verify that a user account exists by running a command similar to this:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - <span data-ttu-id="3daf4-165">Das Benutzerkonto ist gültig, das Konto ist derzeit aber für lync Server nicht aktiviert.</span><span class="sxs-lookup"><span data-stu-id="3daf4-165">The user account is valid, but the account is currently not enabled for Lync Server.</span></span> <span data-ttu-id="3daf4-166">Um zu überprüfen, ob ein Benutzerkonto für lync Server aktiviert war, führen Sie einen Befehl ähnlich der folgenden aus:</span><span class="sxs-lookup"><span data-stu-id="3daf4-166">To verify that a user account was enabled for Lync Server, run a command similar to the following:</span></span>
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    <span data-ttu-id="3daf4-167">Wenn die Enabled-Eigenschaft auf false festgelegt ist, bedeutet dies, dass der Benutzer zurzeit nicht für lync Server aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3daf4-167">If the Enabled property is set to False, that means that the user is currently not enabled for Lync Server.</span></span>

  - <span data-ttu-id="3daf4-168">Die Gruppenerweiterung ist möglicherweise deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3daf4-168">Group expansion might be disabled.</span></span> <span data-ttu-id="3daf4-169">Es ist möglich, die Gruppenerweiterung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="3daf4-169">It is possible to turn off group expansion.</span></span> <span data-ttu-id="3daf4-170">Wenn die Gruppenerweiterung deaktiviert wurde, schlägt das Test-CsGroupExpansion-Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="3daf4-170">If group expansion was disabled then the Test-CsGroupExpansion cmdlet will fail.</span></span> <span data-ttu-id="3daf4-171">Wenn Sie feststellen möchten, ob die Gruppenerweiterung aktiviert ist, verwenden Sie einen Befehl wie den folgenden:</span><span class="sxs-lookup"><span data-stu-id="3daf4-171">To determine whether group expansion is enabled, use a command similar to this:</span></span>
    
        Get-CsWebServiceConfiguration | Select-Object Identity, EnableGroupExpansion

<span data-ttu-id="3daf4-172"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3daf4-172"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

