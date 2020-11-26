---
title: 'Lync Server 2013: Testen des Replikat Diensts'
description: 'Lync Server 2013: Testen des Replikat Diensts.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing the replica service
ms:assetid: 4ff2cc91-0036-4c5a-9792-7bf43d8ce18d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727303(v=OCS.15)
ms:contentKeyID: 63969600
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a61751b95115da3d6519f20f52262b7159ffcbfe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440976"
---
# <a name="testing-the-replica-service-in-lync-server-2013"></a><span data-ttu-id="09d98-103">Testen des Replikat Diensts in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09d98-103">Testing the replica service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="09d98-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="09d98-104">

<span> </span></span></span>

<span data-ttu-id="09d98-105">_**Letztes Änderungsdatum des Themas:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="09d98-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="09d98-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="09d98-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="09d98-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="09d98-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="09d98-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="09d98-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="09d98-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="09d98-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="09d98-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="09d98-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="09d98-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="09d98-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="09d98-112">Beim Ausführen mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des <strong>Test-CsReplica-</strong> Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="09d98-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsReplica</strong> cmdlet.</span></span> <span data-ttu-id="09d98-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="09d98-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsReplica&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="09d98-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="09d98-114">Description</span></span>

<span data-ttu-id="09d98-115">Das Cmdlet **Test-CsReplica** überprüft, ob der lync Server 2013-Replikat Dienst auf dem lokalen Computer ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09d98-115">The **Test-CsReplica** cmdlet verifies that the Lync Server 2013 replica service is running on the local computer.</span></span> <span data-ttu-id="09d98-116">Das Cmdlet " **Test-CsReplica** " führt Aufgaben wie die folgenden aus:</span><span class="sxs-lookup"><span data-stu-id="09d98-116">The **Test-CsReplica** cmdlet performs such tasks as:</span></span>

  - <span data-ttu-id="09d98-117">Überprüfen des Status des Replicator-Agents und der Dienste für zentralisierte Protokollierungs-Agents</span><span class="sxs-lookup"><span data-stu-id="09d98-117">checking the status of the Replicator Agent and Centralized Logging Agent services</span></span>

  - <span data-ttu-id="09d98-118">Überprüfen, ob die erforderlichen Ports in der Windows-Firewall geöffnet wurden</span><span class="sxs-lookup"><span data-stu-id="09d98-118">verifying that the required ports were opened in the Windows Firewall</span></span>

  - <span data-ttu-id="09d98-119">sicherstellen, dass die erforderlichen Active Directory-und lokalen Computersicherheitsgruppen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="09d98-119">making sure that the necessary Active Directory and local computer security groups exist.</span></span>

<span data-ttu-id="09d98-120">Beachten Sie, dass dieses Cmdlet lokal ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="09d98-120">Note that this cmdlet must be run locally.</span></span> <span data-ttu-id="09d98-121">Das bedeutet, dass es auf dem Computer ausgeführt werden muss, auf dem der Replikat Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="09d98-121">That is, it must be run on the same computer where the replica service is running.</span></span> <span data-ttu-id="09d98-122">Es gibt keine Optionen für das Ausführen des **Test-CsReplica-** Cmdlets für einen Remoteserver.</span><span class="sxs-lookup"><span data-stu-id="09d98-122">There are no options for running the **Test-CsReplica** cmdlet against a remote server.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="09d98-123">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="09d98-123">Running the test</span></span>

<span data-ttu-id="09d98-124">Der in Beispiel 1 gezeigte Befehl testet den lync Server 2013-Replikat Dienst auf dem lokalen Computer.</span><span class="sxs-lookup"><span data-stu-id="09d98-124">The command shown in Example 1 tests the Lync Server 2013 replica service on the local computer.</span></span> <span data-ttu-id="09d98-125">In diesem Beispiel wird der Verbose-Parameter verwendet, um sicherzustellen, dass Informationen über den Test – einschließlich des eventuellen Fehlers oder des Erfolgs des Tests und der Position des vom Test generierten Berichts – auf dem Bildschirm angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="09d98-125">In this example the Verbose parameter is used to guarantee that information about the test – including the eventual failure or success of the test and the location of the report generated by the test – is displayed on screen.</span></span>

    Test-CsReplica -Verbose

<span data-ttu-id="09d98-126">Beispiel 2 ist eine Variation des Befehls, die in Beispiel 1 gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="09d98-126">Example 2 is a variation of the command shown in Example 1.</span></span> <span data-ttu-id="09d98-127">In diesem Fall ist der Berichtsparameter enthalten, um einen Ordnerpfad und einen Namen für den vom Test generierten Bericht anzugeben.</span><span class="sxs-lookup"><span data-stu-id="09d98-127">In this case, the Report parameter is included to specify a folder path and name for the report generated by the test.</span></span> <span data-ttu-id="09d98-128">Wenn Sie keinen Berichtspfad angeben, erhält der Bericht einen automatisch generierten Namen, der wie folgt lautet:</span><span class="sxs-lookup"><span data-stu-id="09d98-128">If you do not specify a report path the report will be given an auto-generated name similar to this:</span></span>

<span data-ttu-id="09d98-129">C: \\ Benutzer \\ Administrator. "litwareinc \\ AppData \\ lokal \\ Temp \\ 1 \\Test-Cs-Replica-3db40ee0-4b5d-4f58-8d3d-b1e61253129e.html</span><span class="sxs-lookup"><span data-stu-id="09d98-129">C:\\Users\\Administrator.Litwareinc\\AppData\\Local\\Temp\\1\\Test-Cs-Replica-3db40ee0-4b5d-4f58-8d3d-b1e61253129e.html</span></span>

    Test-CsReplica -Verbose -Report C:\Logs\ReplicaTest.html

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="09d98-130">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="09d98-130">Determining success or failure</span></span>

<span data-ttu-id="09d98-131">Abschnittstext hier einfügen.</span><span class="sxs-lookup"><span data-stu-id="09d98-131">Insert section body here.</span></span>

<span data-ttu-id="09d98-132">Ausführlich: Erstellen einer neuen Protokolldatei "C: \\ Benutzer, die \\ \\ AppData \\ Lokales \\ Temp \\ -Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml testen".</span><span class="sxs-lookup"><span data-stu-id="09d98-132">VERBOSE: Creating new log file "C:\\Users\\Testing\\AppData\\Local\\Temp\\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span></span>

<span data-ttu-id="09d98-133">Ausführlich: Erstellen einer neuen Protokolldatei "C: \\ Benutzer, die \\ \\ AppData \\ Lokales \\ Temp \\ -Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml testen".</span><span class="sxs-lookup"><span data-stu-id="09d98-133">VERBOSE: Creating new log file "C:\\Users\\Testing\\AppData\\Local\\Temp\\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span></span>

<span data-ttu-id="09d98-134">Ausführlich: die Verarbeitung von "Test-CsReplica" wurde erfolgreich abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="09d98-134">VERBOSE: "Test-CsReplica" processing has completed successfully.</span></span>

<span data-ttu-id="09d98-135">Ausführlich: detaillierte Ergebnisse finden Sie unter "C: \\ Benutzer \\ Testen \\ AppData \\ local \\ Temp \\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span><span class="sxs-lookup"><span data-stu-id="09d98-135">VERBOSE: Detailed results can be found at "C:\\Users\\Testing\\AppData\\Local\\Temp\\Test-CsReplica-3cb066b3-dd23-411a-8932-99f01c0f940c.xml".</span></span>

<span data-ttu-id="09d98-136">Ausführlich: Erstellen einer neuen Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="09d98-136">VERBOSE: Creating new log file</span></span>

<span data-ttu-id="09d98-137">"C: \\ Benutzer \\ Testen \\ AppData \\ local \\ Temp \\ 2 \\ Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span><span class="sxs-lookup"><span data-stu-id="09d98-137">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span></span>

<span data-ttu-id="09d98-138">d3bd0e4a083.xml ".</span><span class="sxs-lookup"><span data-stu-id="09d98-138">d3bd0e4a083.xml".</span></span>

<span data-ttu-id="09d98-139">Ausführlich: Erstellen einer neuen Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="09d98-139">VERBOSE: Creating new log file</span></span>

<span data-ttu-id="09d98-140">"C: \\ Benutzer \\ Testen \\ AppData \\ local \\ Temp \\ 2 \\ Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span><span class="sxs-lookup"><span data-stu-id="09d98-140">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span></span>

<span data-ttu-id="09d98-141">d3bd0e4a083.html ".</span><span class="sxs-lookup"><span data-stu-id="09d98-141">d3bd0e4a083.html".</span></span>

<span data-ttu-id="09d98-142">Warnung: Test-CsReplica fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="09d98-142">WARNING: Test-CsReplica failed.</span></span>

<span data-ttu-id="09d98-143">Warnung: detaillierte Ergebnisse finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="09d98-143">WARNING: Detailed results can be found at</span></span>

<span data-ttu-id="09d98-144">"C: \\ Benutzer \\ Testen \\ AppData \\ local \\ Temp \\ 2 \\ Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span><span class="sxs-lookup"><span data-stu-id="09d98-144">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsReplica-29fddb35-f56e-4e3c-8f4c-e</span></span>

<span data-ttu-id="09d98-145">d3bd0e4a083.html ".</span><span class="sxs-lookup"><span data-stu-id="09d98-145">d3bd0e4a083.html".</span></span>

<span data-ttu-id="09d98-146">Test-CsReplica: Fehler bei der Befehlsausführung: der angeforderte Registrierungszugriff ist nicht</span><span class="sxs-lookup"><span data-stu-id="09d98-146">Test-CsReplica : Command execution failed: Requested registry access is not</span></span>

<span data-ttu-id="09d98-147">zulässig.</span><span class="sxs-lookup"><span data-stu-id="09d98-147">allowed.</span></span>

<span data-ttu-id="09d98-148">Zeile: 1 Zeichen: 1</span><span class="sxs-lookup"><span data-stu-id="09d98-148">At line:1 char:1</span></span>

<span data-ttu-id="09d98-149">\+ Test-CsReplica-Verbose</span><span class="sxs-lookup"><span data-stu-id="09d98-149">\+ Test-CsReplica -Verbose</span></span>

\+ ~~~~~~~~~~~~~~~~~~~~~~~

<span data-ttu-id="09d98-150">\+ CategoryInfo: InvalidOperation: (:) \[ Test-CsReplica \] , Sicherheit</span><span class="sxs-lookup"><span data-stu-id="09d98-150">\+ CategoryInfo : InvalidOperation: (:) \[Test-CsReplica\], Security</span></span>

<span data-ttu-id="09d98-151">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="09d98-151">Exception</span></span>

<span data-ttu-id="09d98-152">\+ FullyQualifiedErrorId: ProcessingFailed, Microsoft. RTC. Management. deploy</span><span class="sxs-lookup"><span data-stu-id="09d98-152">\+ FullyQualifiedErrorId : ProcessingFailed,Microsoft.Rtc.Management.Deploy</span></span>

<span data-ttu-id="09d98-153">ment. TestReplicaCmdlet</span><span class="sxs-lookup"><span data-stu-id="09d98-153">ment.TestReplicaCmdlet</span></span>

<span data-ttu-id="09d98-154">PS C: \\ Testen der Benutzer \\\></span><span class="sxs-lookup"><span data-stu-id="09d98-154">PS C:\\Users\\Testing\></span></span>

<span data-ttu-id="09d98-155">PS C: \\ Benutzer, die \\ \> Test-CsUcwaConference-TargetFqdn "LyncTest. SelfHost. Corp. M testen</span><span class="sxs-lookup"><span data-stu-id="09d98-155">PS C:\\Users\\Testing\> Test-CsUcwaConference -TargetFqdn "LyncTest.SelfHost.Corp.M</span></span>

<span data-ttu-id="09d98-156">icrosoft.com "</span><span class="sxs-lookup"><span data-stu-id="09d98-156">icrosoft.com"</span></span>

<span data-ttu-id="09d98-157">Warnung: Fehler beim Lesen der Registrierungsstellen-Portnummer für die angegebene vollqualifizierte</span><span class="sxs-lookup"><span data-stu-id="09d98-157">WARNING: Failed to read Registrar port number for the given fully qualified</span></span>

<span data-ttu-id="09d98-158">Domänenname (FQDN).</span><span class="sxs-lookup"><span data-stu-id="09d98-158">domain name (FQDN).</span></span> <span data-ttu-id="09d98-159">Verwenden der standardmäßigen Registrierungs Portnummer</span><span class="sxs-lookup"><span data-stu-id="09d98-159">Using default Registrar port number.</span></span> <span data-ttu-id="09d98-160">Ausnahme</span><span class="sxs-lookup"><span data-stu-id="09d98-160">Exception:</span></span>

<span data-ttu-id="09d98-161">System. InvalidOperationException: kein übereinstimmender Cluster in der Topologie gefunden.</span><span class="sxs-lookup"><span data-stu-id="09d98-161">System.InvalidOperationException: No matching cluster found in topology.</span></span>

<span data-ttu-id="09d98-162">am</span><span class="sxs-lookup"><span data-stu-id="09d98-162">at</span></span>

<span data-ttu-id="09d98-163">Microsoft. RTC. Management. SyntheticTransactions. SipSyntheticTransaction. TryRetri</span><span class="sxs-lookup"><span data-stu-id="09d98-163">Microsoft.Rtc.Management.SyntheticTransactions.SipSyntheticTransaction.TryRetri</span></span>

<span data-ttu-id="09d98-164">eveRegistrarPortFromTopology (Int32& registrarPortNumber)</span><span class="sxs-lookup"><span data-stu-id="09d98-164">eveRegistrarPortFromTopology(Int32& registrarPortNumber)</span></span>

<span data-ttu-id="09d98-165">Test-CsUcwaConference: Es wurde kein Testbenutzer zugewiesen</span><span class="sxs-lookup"><span data-stu-id="09d98-165">Test-CsUcwaConference : There is no test user assigned for</span></span>

<span data-ttu-id="09d98-166">\[LyncTest.SelfHost.Corp.Microsoft.com \] .</span><span class="sxs-lookup"><span data-stu-id="09d98-166">\[LyncTest.SelfHost.Corp.Microsoft.com\].</span></span> <span data-ttu-id="09d98-167">Überprüfen Sie die Benutzerkonfiguration testen.</span><span class="sxs-lookup"><span data-stu-id="09d98-167">Verify test user configuration.</span></span>

<span data-ttu-id="09d98-168">Zeile: 1 Zeichen: 1</span><span class="sxs-lookup"><span data-stu-id="09d98-168">At line:1 char:1</span></span>

<span data-ttu-id="09d98-169">\+ Test-CsUcwaConference-TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"</span><span class="sxs-lookup"><span data-stu-id="09d98-169">\+ Test-CsUcwaConference -TargetFqdn "LyncTest.SelfHost.Corp.Microsoft.com"</span></span>

\+ ~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~~

<span data-ttu-id="09d98-170">\+ CategoryInfo: ResourceUnavailable: (:) \[ Test-CsUcwaConference\]</span><span class="sxs-lookup"><span data-stu-id="09d98-170">\+ CategoryInfo : ResourceUnavailable: (:) \[Test-CsUcwaConference\]</span></span>

<span data-ttu-id="09d98-171">, InvalidOperationException</span><span class="sxs-lookup"><span data-stu-id="09d98-171">, InvalidOperationException</span></span>

<span data-ttu-id="09d98-172">\+ FullyQualifiedErrorId: NotFoundTestUsers, Microsoft. RTC. Management. Synth</span><span class="sxs-lookup"><span data-stu-id="09d98-172">\+ FullyQualifiedErrorId : NotFoundTestUsers,Microsoft.Rtc.Management.Synth</span></span>

<span data-ttu-id="09d98-173">eticTransactions.TestUcwaConferenceCmdlet</span><span class="sxs-lookup"><span data-stu-id="09d98-173">eticTransactions.TestUcwaConferenceCmdlet</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="09d98-174">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="09d98-174">Reasons why the test might have failed</span></span>

<span data-ttu-id="09d98-175">Nachfolgend finden Sie einige häufige Gründe, warum **Test-CsReplica** möglicherweise fehlschlägt:</span><span class="sxs-lookup"><span data-stu-id="09d98-175">Here are some common reasons why **Test-CsReplica** might fail:</span></span>

  - <span data-ttu-id="09d98-176">Möglicherweise liegt ein größeres Problem mit dem Replicator-Agent und den zentralen Protokollierungs-Agent-Diensten vor.</span><span class="sxs-lookup"><span data-stu-id="09d98-176">There may be a larger problem with the Replicator Agent and Centralized Logging Agent services</span></span>

  - <span data-ttu-id="09d98-177">Die erforderlichen Ports sind möglicherweise nicht in der Windows-Firewall geöffnet.</span><span class="sxs-lookup"><span data-stu-id="09d98-177">The required ports may not be open in the Windows Firewall</span></span>

  - <span data-ttu-id="09d98-178">Die erforderlichen Active Directory-und lokalen Computersicherheitsgruppen sind möglicherweise nicht vorhanden</span><span class="sxs-lookup"><span data-stu-id="09d98-178">The necessary Active Directory and local computer security groups may not exist</span></span>

<span data-ttu-id="09d98-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="09d98-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

