---
title: 'Lync Server 2013: Testen der Monitor Knoten Konfiguration'
description: 'Lync Server 2013: Test Watcher-Knoten Konfiguration.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing watcher node configuration
ms:assetid: f9ecd85c-0ae9-4906-b786-6b002b5a77c6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn751537(v=OCS.15)
ms:contentKeyID: 63969667
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1eeb141eee011d7e06f5dd49e483e026484d733
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440927"
---
# <a name="testing-watcher-node-configuration-in-lync-server-2013"></a><span data-ttu-id="30a64-103">Testen der Monitor Knoten Konfiguration in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="30a64-103">Testing watcher node configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="30a64-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="30a64-104">

<span> </span></span></span>

<span data-ttu-id="30a64-105">_**Letztes Änderungsdatum des Themas:** 2014-11-03_</span><span class="sxs-lookup"><span data-stu-id="30a64-105">_**Topic Last Modified:** 2014-11-03_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="30a64-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="30a64-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="30a64-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="30a64-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="30a64-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="30a64-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="30a64-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="30a64-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="30a64-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="30a64-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="30a64-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="30a64-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="30a64-112">Beim Ausführen mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des <strong>Test-CsWatcherNodeConfiguration-</strong> Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="30a64-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsWatcherNodeConfiguration</strong> cmdlet.</span></span> <span data-ttu-id="30a64-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="30a64-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot; Test-CsWatcherNodeConfiguration&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="30a64-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="30a64-114">Description</span></span>

<span data-ttu-id="30a64-115">Wenn Sie Microsoft System Center Operations Manager zum Überwachen von lync Server 2013 verwenden, haben Sie die Möglichkeit, "Watcher-Knoten" einzurichten: Computer, die regelmäßig und automatisch synthetische Transaktionen ausführen, um zu überprüfen, ob lync Server wie erwartet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="30a64-115">If you are using Microsoft System Center Operations Manager to monitor Lync Server 2013 then you have the option of setting up "watcher nodes": computers that periodically, and automatically, run synthetic transactions to verify that Lync Server is working as expected.</span></span> <span data-ttu-id="30a64-116">Watcher-Knoten werden Pools zugewiesen und mithilfe der **CsWatcherNodeConfiguration** -Cmdlets verwaltet.</span><span class="sxs-lookup"><span data-stu-id="30a64-116">Watcher nodes are assigned to pools, and are managed by using the **CsWatcherNodeConfiguration** cmdlets.</span></span> <span data-ttu-id="30a64-117">Beachten Sie, dass Sie keine Watcher-Knoten installieren müssen, wenn Sie System Center Operations Manager verwenden.</span><span class="sxs-lookup"><span data-stu-id="30a64-117">Note that you do not need to install watcher nodes if you are using System Center Operations Manager.</span></span> <span data-ttu-id="30a64-118">Sie können Ihr System weiterhin überwachen, ohne Watcher-Knoten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="30a64-118">You can still monitor your system without using watcher nodes.</span></span> <span data-ttu-id="30a64-119">Der einzige Unterschied besteht darin, dass alle synthetischen Transaktionen, die Sie ausführen möchten, manuell aufgerufen werden müssen, anstatt von Operations Manager automatisch aufgerufen zu werden.</span><span class="sxs-lookup"><span data-stu-id="30a64-119">The only difference is that any synthetic transactions that you want to run must be invoked manually instead of automatically invoked by Operations Manager.</span></span>

<span data-ttu-id="30a64-120">Mit dem Cmdlet **Test-CsWatcherNodeConfiguration** können Sie überprüfen, ob ein Watcher-Knoten ordnungsgemäß konfiguriert wurde und einem gültigen lync Server 2013-Pool zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="30a64-120">The **Test-CsWatcherNodeConfiguration** cmdlet enables you to verify that a watcher node was configured correctly and is assigned to a valid Lync Server 2013 pool.</span></span> <span data-ttu-id="30a64-121">Beachten Sie, dass das Cmdlet **Test-CsWatcherNodeConfiguration** auf dem Watcher-Knoten selbst ausgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="30a64-121">Note that the **Test-CsWatcherNodeConfiguration** cmdlet must be run on the watcher node itself.</span></span> <span data-ttu-id="30a64-122">Das Cmdlet kann nicht für Remotecomputer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="30a64-122">The cmdlet cannot be run against remote computers.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="30a64-123">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="30a64-123">Running the test</span></span>

<span data-ttu-id="30a64-124">Mit dem folgenden Befehl werden die Konfigurationseinstellungen für jeden Watcher-Knoten überprüft, der in der Organisation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="30a64-124">The following command verifies the configuration settings for each watcher node that is being used in the organization.</span></span>

    Test-CsWatcherNodeConfiguration

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="30a64-125">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="30a64-125">Determining success or failure</span></span>

<span data-ttu-id="30a64-126">Die folgende erfolgreiche Beispielausgabe zeigt ein System mit vier Edge-Servern.</span><span class="sxs-lookup"><span data-stu-id="30a64-126">The following successful sample output shows a system with four edge servers.</span></span>

<span data-ttu-id="30a64-127">Überprüfen des ATL-CS-001.litwareinc.com des Ziel Pools gegen Topologie.</span><span class="sxs-lookup"><span data-stu-id="30a64-127">Validating target pool atl-cs-001.litwareinc.com against topology.</span></span>

<span data-ttu-id="30a64-128">Erfolg: Ziel Pool-ATL-CS-001.litwareinc.com ist in der Topologie vorhanden.</span><span class="sxs-lookup"><span data-stu-id="30a64-128">Success: Target pool atl-cs-001.litwareinc.com exists in topology.</span></span>

<span data-ttu-id="30a64-129">Erfolg: Ziel Pool ATL-CS-001.litwareinc.com hat die Registrierungsstelle Rolle installiert.</span><span class="sxs-lookup"><span data-stu-id="30a64-129">Success: Target pool atl-cs-001.litwareinc.com has Registrar role installed.</span></span>

<span data-ttu-id="30a64-130">Erfolg: Ziel Pool-ATL-CS-001.litwareinc.com wird unterstützt.</span><span class="sxs-lookup"><span data-stu-id="30a64-130">Success: Target pool atl-cs-001.litwareinc.com is supported version.</span></span>

<span data-ttu-id="30a64-131">Erfolgreich: Port Nummer für 5061 Ziel Pool ATL-CS-001.litwareinc.com ist richtig.</span><span class="sxs-lookup"><span data-stu-id="30a64-131">Success: Port number for 5061 Target pool atl-cs-001.litwareinc.com is correct.</span></span>

<span data-ttu-id="30a64-132">Das Überprüfen auf fehlende Pools in Watcher-Knoten Konfiguration wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="30a64-132">Checking for missing pools in watcher node configuration is started.</span></span> <span data-ttu-id="30a64-133">Wenn ein Fehler erkannt wird, wird er gedruckt.</span><span class="sxs-lookup"><span data-stu-id="30a64-133">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="30a64-134">Das Überprüfen auf fehlende Pools in Watcher-Knoten Konfiguration ist nicht mehr erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="30a64-134">Checking for missing pools in watcher node configuration is finished.</span></span>

<span data-ttu-id="30a64-135">Die Überprüfung auf die Registrierungsschlüssel für Watcher-Knoten, die von Watcher-Knoten Installation erstellt wurden, wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="30a64-135">Checking for watcher node registry keys created by watcher node installation, is started.</span></span> <span data-ttu-id="30a64-136">Wenn ein Fehler erkannt wird, wird er gedruckt.</span><span class="sxs-lookup"><span data-stu-id="30a64-136">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="30a64-137">Die Überprüfung der Registrierungsschlüssel für Watcher-Knoten, die von Watcher-Knoten Installation erstellt wurden, ist zu Ende.</span><span class="sxs-lookup"><span data-stu-id="30a64-137">Checking for watcher node registry keys created by watcher node installation, is finished.</span></span> <span data-ttu-id="30a64-138">Der erkannte Authentifizierungstyp ist Negotiate.</span><span class="sxs-lookup"><span data-stu-id="30a64-138">Detected authentication type is Negotiate.</span></span>

<span data-ttu-id="30a64-139">Das vorhanden sein der Anmeldeinformationen des Testbenutzers wurde erfolgreich überprüft SIP: user1@ ATL-CS-001.litwareinc.com im Anmelde Informations Verwaltungsspeicher.</span><span class="sxs-lookup"><span data-stu-id="30a64-139">Successfully validated existence of test user’s credential sip:user1@ atl-cs-001.litwareinc.com in credential management store.</span></span>

<span data-ttu-id="30a64-140">Das vorhanden sein der Anmeldeinformationen des Testbenutzers wurde erfolgreich überprüft SIP: User2@ ATL-CS-001.litwareinc.com im Anmelde Informations Verwaltungsspeicher.</span><span class="sxs-lookup"><span data-stu-id="30a64-140">Successfully validated existence of test user’s credential sip:user2@ atl-cs-001.litwareinc.com in credential management store.</span></span>

<span data-ttu-id="30a64-141">Das Überprüfen auf fehlende Pools in Watcher-Knoten Konfiguration wird gestartet.</span><span class="sxs-lookup"><span data-stu-id="30a64-141">Checking for missing pools in watcher node configuration is started.</span></span> <span data-ttu-id="30a64-142">Wenn ein Fehler erkannt wird, wird er gedruckt.</span><span class="sxs-lookup"><span data-stu-id="30a64-142">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="30a64-143">Warnung: Pool ATL-CS-001.litwareinc.com hat die Registrierungsstelle</span><span class="sxs-lookup"><span data-stu-id="30a64-143">WARNING: Pool atl-cs-001.litwareinc.com has Registrar</span></span>

<span data-ttu-id="30a64-144">Rolle installiert, aber es sind keine Testbenutzer konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="30a64-144">role installed, but there are no test users configured for it.</span></span>

<span data-ttu-id="30a64-145">Das Überprüfen auf fehlende Pools in Watcher-Knoten Konfiguration ist nicht mehr erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="30a64-145">Checking for missing pools in watcher node configuration is finished.</span></span>

<span data-ttu-id="30a64-146">Überprüfen der Registrierungsschlüssel für Watcher-Knoten, die von Watcher-Knoten Installation erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="30a64-146">Checking for watcher node registry keys created by watcher node installation, is</span></span>

<span data-ttu-id="30a64-147">begann.</span><span class="sxs-lookup"><span data-stu-id="30a64-147">started.</span></span> <span data-ttu-id="30a64-148">Wenn ein Fehler erkannt wird, wird er gedruckt.</span><span class="sxs-lookup"><span data-stu-id="30a64-148">If any error is detected, it will be printed.</span></span>

<span data-ttu-id="30a64-149">Test-CsWatcherNodeConfiguration: der Integritäts Registrierungsschlüssel kann nicht gefunden werden</span><span class="sxs-lookup"><span data-stu-id="30a64-149">Test-CsWatcherNodeConfiguration : Cannot find Health registry key in</span></span>

<span data-ttu-id="30a64-150">Software \\ Microsoft \\ -Echtzeitkommunikation.</span><span class="sxs-lookup"><span data-stu-id="30a64-150">Software\\Microsoft\\Real-Time Communications.</span></span> <span data-ttu-id="30a64-151">Stellen Sie sicher, dass Watcher Node. msi</span><span class="sxs-lookup"><span data-stu-id="30a64-151">Make sure watcher node .msi is</span></span>

<span data-ttu-id="30a64-152">ordnungsgemäß installiert.</span><span class="sxs-lookup"><span data-stu-id="30a64-152">installed properly.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="30a64-153">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="30a64-153">Reasons why the test might have failed</span></span>

<span data-ttu-id="30a64-154">Nachfolgend finden Sie einige häufige Gründe, warum **Test-CsWatcherNodeConfiguration** möglicherweise fehlschlägt:</span><span class="sxs-lookup"><span data-stu-id="30a64-154">Here are some common reasons why **Test-CsWatcherNodeConfiguration** might fail:</span></span>

  - <span data-ttu-id="30a64-155">Watcher-Knoten ist nicht ordnungsgemäß installiert.</span><span class="sxs-lookup"><span data-stu-id="30a64-155">Watcher node is not correctly installed.</span></span>

  - <span data-ttu-id="30a64-156">Es sind keine Testbenutzer konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="30a64-156">No test users are configured.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="30a64-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="30a64-157">See Also</span></span>


[<span data-ttu-id="30a64-158">Get-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="30a64-158">Get-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsWatcherNodeConfiguration)  
[<span data-ttu-id="30a64-159">New-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="30a64-159">New-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsWatcherNodeConfiguration)  
[<span data-ttu-id="30a64-160">Remove-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="30a64-160">Remove-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsWatcherNodeConfiguration)  
[<span data-ttu-id="30a64-161">Set-CsWatcherNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="30a64-161">Set-CsWatcherNodeConfiguration</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsWatcherNodeConfiguration)  
  

<span data-ttu-id="30a64-162"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="30a64-162"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

