---
title: 'Lync Server 2013: Abläufe für Reaktionsgruppen während des Ausfalls eines Pools'
description: Erfahrung mit der lync Server 2013-Reaktionsgruppe während eines Pool Fehlers.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Response group experience during pool failure
ms:assetid: 4e00fb38-64b1-4fd9-903d-7639177bc303
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204886(v=OCS.15)
ms:contentKeyID: 48184116
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d8d5904bc6934d4c330202bafa66d6dd8a16ff5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436244"
---
# <a name="response-group-experience-in-lync-server-2013-during-pool-failure"></a><span data-ttu-id="385ad-103">Abläufe für Reaktionsgruppen während des Ausfalls eines Pools in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="385ad-103">Response group experience in Lync Server 2013 during pool failure</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="385ad-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="385ad-104">

<span> </span></span></span>

<span data-ttu-id="385ad-105">_**Letztes Änderungsdatum des Themas:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="385ad-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="385ad-106">In diesem Abschnitt wird ausführlich beschrieben, wie Reaktionsgruppen Aktivitäten in den folgenden Phasen betroffen sind:</span><span class="sxs-lookup"><span data-stu-id="385ad-106">This section describes in detail how response group activity is affected in the following stages:</span></span>

  - <span data-ttu-id="385ad-107">Im primären Pool tritt ein Ausfall auf, aber noch kein Failover initiiert.</span><span class="sxs-lookup"><span data-stu-id="385ad-107">An outage occurs in the primary pool, but failover is not yet initiated.</span></span>

  - <span data-ttu-id="385ad-108">Der Dienst ist für den Sicherungspool nicht mehr möglich.</span><span class="sxs-lookup"><span data-stu-id="385ad-108">Service is failed over to the backup pool.</span></span>

  - <span data-ttu-id="385ad-109">Der Dienst ist nicht mehr im primären Pool zurück.</span><span class="sxs-lookup"><span data-stu-id="385ad-109">Service is failed back to the primary pool.</span></span>

<div>

## <a name="user-experience-when-outage-occurs"></a><span data-ttu-id="385ad-110">Benutzererfahrung bei einem Ausfall</span><span class="sxs-lookup"><span data-stu-id="385ad-110">User Experience When Outage Occurs</span></span>

<span data-ttu-id="385ad-111">Wenn ein Pool-oder Website Ausfall auftritt, der Administrator aber noch kein Failover initiiert hat, wird die Aktivität der Reaktionsgruppe wie in der folgenden Tabelle beschrieben behandelt.</span><span class="sxs-lookup"><span data-stu-id="385ad-111">When a pool or site outage occurs, but the administrator has not yet initiated failover, response group activity is handled as described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="385ad-112">Während der Disaster Recovery Verhalten sich Anrufe anders, je nachdem, ob die primären Pool Antwortgruppen während der Wiederherstellung in den Backup-Pool importiert wurden.</span><span class="sxs-lookup"><span data-stu-id="385ad-112">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="385ad-113">In der folgenden Tabelle sind Verweise auf importierte Antwortgruppen darauf hinweisen, dass primäre Pool Antwortgruppen während des Disaster Recovery-Modus in den Sicherungspool importiert wurden.</span><span class="sxs-lookup"><span data-stu-id="385ad-113">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="outage-occurs"></a><span data-ttu-id="385ad-114">Ausfall eintritt</span><span class="sxs-lookup"><span data-stu-id="385ad-114">Outage Occurs</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="385ad-115">Art des Anrufs oder der Benutzeraktion</span><span class="sxs-lookup"><span data-stu-id="385ad-115">Type of call or user action</span></span></th>
<th><span data-ttu-id="385ad-116">Bei einem Ausfall</span><span class="sxs-lookup"><span data-stu-id="385ad-116">During outage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="385ad-117">Anrufe, die mit einem Agenten verbunden sind</span><span class="sxs-lookup"><span data-stu-id="385ad-117">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="385ad-118">Reguläre Anrufe bleiben verbunden.</span><span class="sxs-lookup"><span data-stu-id="385ad-118">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="385ad-119">Anonyme Anrufe werden getrennt.</span><span class="sxs-lookup"><span data-stu-id="385ad-119">Anonymous calls are disconnected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="385ad-120">In Bearbeitung befindliche Anrufe, die noch nicht mit einem Agenten verbunden sind</span><span class="sxs-lookup"><span data-stu-id="385ad-120">In progress calls not yet connected to an agent</span></span></p></td>
<td><p><span data-ttu-id="385ad-121">Anrufe werden getrennt.</span><span class="sxs-lookup"><span data-stu-id="385ad-121">Calls are disconnected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="385ad-122">Neue Anrufe</span><span class="sxs-lookup"><span data-stu-id="385ad-122">New calls</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="385ad-123">Anrufe werden getrennt.</span><span class="sxs-lookup"><span data-stu-id="385ad-123">Calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="385ad-124">Wenn Reaktionsgruppen importiert wurden, werden die Verbindungen mit dem Sicherungspool verbunden, aber im primären Pool verwaltete Agents sind nicht erreichbar.</span><span class="sxs-lookup"><span data-stu-id="385ad-124">If response groups were imported, calls connect to backup pool, but agents homed in primary pool are unreachable.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="385ad-125">Agenten Anrufe im Namen der Reaktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="385ad-125">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="385ad-126">Das Feature ist in dieser Phase deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="385ad-126">Feature is disabled during this stage.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="385ad-127">Informationen zu Anmelde-und Agent-Agents</span><span class="sxs-lookup"><span data-stu-id="385ad-127">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="385ad-128">Agentengruppen, die im Besitz des primären Pools sind, können auf der Agentenkonsole angezeigt werden, aber die Agents können sich nicht anmelden.</span><span class="sxs-lookup"><span data-stu-id="385ad-128">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="385ad-129">Agentengruppen, die im Besitz des Sicherungs Pools sind, können auf der Agentenkonsole angezeigt werden, und die Agents können sich anmelden.</span><span class="sxs-lookup"><span data-stu-id="385ad-129">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="385ad-130">Importierte Agentengruppen werden auf der Agentenkonsole nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="385ad-130">Imported agent groups are not displayed on agent console.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="385ad-131">Reaktionsgruppen Konfiguration</span><span class="sxs-lookup"><span data-stu-id="385ad-131">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="385ad-132">Antwortgruppen, die im Besitz des primären Pools sind, können je nach Verfügbarkeit der Back-End-Datenbank des primären Pools angezeigt, aber nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="385ad-132">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="385ad-133">Antwortgruppen, die im Besitz des Sicherungs Pools sind, können angezeigt und geändert werden.</span><span class="sxs-lookup"><span data-stu-id="385ad-133">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="385ad-134">Importierte Antwortgruppen können nicht mit der lync Server-Systemsteuerung oder dem Reaktionsgruppen-Konfigurations Tool angezeigt werden, können aber mithilfe der lync Server-Verwaltungsshell-Cmdlets konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="385ad-134">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-experience-during-failover"></a><span data-ttu-id="385ad-135">Benutzerfreundlichkeit während eines Failovers</span><span class="sxs-lookup"><span data-stu-id="385ad-135">User Experience During Failover</span></span>

<span data-ttu-id="385ad-136">Wenn ein Administrator ein Failover zu einem Sicherungspool aufruft, werden die Reaktionsgruppen Aktivitäten während und nach dem Failover verarbeitet, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="385ad-136">When an administrator invokes failover to a backup pool, response group activity is handled during and after the failover as described in the following table.</span></span> <span data-ttu-id="385ad-137">Die erste Spalte beschreibt die Art der Aktivität, die möglicherweise stattfindet.</span><span class="sxs-lookup"><span data-stu-id="385ad-137">The first column describes the type of activity that might be taking place.</span></span> <span data-ttu-id="385ad-138">In der mittleren Spalte wird beschrieben, wie die einzelnen Aktivitäten während der kurzen Zeit behandelt werden, die für ein Failover zum Sicherungspool erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="385ad-138">The middle column describes how each activity is handled during the brief time that it takes to fail over to the backup pool.</span></span> <span data-ttu-id="385ad-139">In der letzten Spalte wird beschrieben, wie die Aktivität für die Dauer verarbeitet wird, nachdem der Failoverprozess abgeschlossen ist und der Sicherungspool für den primären Pool bereit steht.</span><span class="sxs-lookup"><span data-stu-id="385ad-139">The last column describes how the activity is handled for the duration, after the failover process is complete and the backup pool is standing in for the primary pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="385ad-140">Während der Disaster Recovery Verhalten sich Anrufe anders, je nachdem, ob die primären Pool Antwortgruppen während der Wiederherstellung in den Backup-Pool importiert wurden.</span><span class="sxs-lookup"><span data-stu-id="385ad-140">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="385ad-141">In der folgenden Tabelle sind Verweise auf importierte Antwortgruppen darauf hinweisen, dass primäre Pool Antwortgruppen während des Disaster Recovery-Modus in den Sicherungspool importiert wurden.</span><span class="sxs-lookup"><span data-stu-id="385ad-141">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="failover-is-initiated"></a><span data-ttu-id="385ad-142">Failover wird initiiert</span><span class="sxs-lookup"><span data-stu-id="385ad-142">Failover Is Initiated</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="385ad-143">Art des Anrufs oder der Benutzeraktion</span><span class="sxs-lookup"><span data-stu-id="385ad-143">Type of call or user action</span></span></th>
<th><span data-ttu-id="385ad-144">Während des Failovers</span><span class="sxs-lookup"><span data-stu-id="385ad-144">During Failover</span></span></th>
<th><span data-ttu-id="385ad-145">Nach Abschluss des Failovers</span><span class="sxs-lookup"><span data-stu-id="385ad-145">After Failover Completes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="385ad-146">Anrufe, die mit einem Agenten verbunden sind</span><span class="sxs-lookup"><span data-stu-id="385ad-146">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="385ad-147">Reguläre Anrufe bleiben verbunden.</span><span class="sxs-lookup"><span data-stu-id="385ad-147">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="385ad-148">Anonyme Anrufe werden getrennt.</span><span class="sxs-lookup"><span data-stu-id="385ad-148">Anonymous calls are disconnected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="385ad-149">Reguläre Anrufe bleiben verbunden.</span><span class="sxs-lookup"><span data-stu-id="385ad-149">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="385ad-150">Bei importierten Antwortgruppen bleiben anonyme Anrufe, die den Sicherungspool erreicht haben, verbunden.</span><span class="sxs-lookup"><span data-stu-id="385ad-150">For imported response groups, anonymous calls that have reached the backup pool remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="385ad-151">In Bearbeitung befindliche Anrufe, die noch nicht mit einem Agenten verbunden sind</span><span class="sxs-lookup"><span data-stu-id="385ad-151">In progress calls not yet connected to an agent</span></span></p></td>
<td><p><span data-ttu-id="385ad-152">Anrufe werden getrennt.</span><span class="sxs-lookup"><span data-stu-id="385ad-152">Calls are disconnected.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="385ad-153">Wenn Reaktionsgruppen nicht importiert wurden, befinden sich in diesem Status keine Anrufe.</span><span class="sxs-lookup"><span data-stu-id="385ad-153">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="385ad-154">Bei importierten Antwortgruppen bleiben Anrufe, die den Sicherungspool erreicht haben, verbunden.</span><span class="sxs-lookup"><span data-stu-id="385ad-154">For imported response groups, calls that have reached the backup pool remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="385ad-155">Neue Anrufe</span><span class="sxs-lookup"><span data-stu-id="385ad-155">New calls</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="385ad-156">Anrufe werden getrennt.</span><span class="sxs-lookup"><span data-stu-id="385ad-156">Calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="385ad-157">Bei importierten Antwortgruppen wird die Verbindung mit dem Sicherungspool hergestellt, aber im primären Pool verwaltete Agents sind nicht erreichbar.</span><span class="sxs-lookup"><span data-stu-id="385ad-157">For imported response groups, calls connect to the backup pool, but agents homed in the primary pool are unreachable.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="385ad-158">Wenn Reaktionsgruppen nicht importiert wurden, werden Anrufe getrennt.</span><span class="sxs-lookup"><span data-stu-id="385ad-158">If response groups were not imported, calls are disconnected.</span></span></p></li>
<li><p><span data-ttu-id="385ad-159">Bei importierten Antwortgruppen werden Anrufe mit dem Sicherungspool verbunden.</span><span class="sxs-lookup"><span data-stu-id="385ad-159">For imported response groups, calls connect to the backup pool.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="385ad-160">Agenten Anrufe im Namen der Reaktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="385ad-160">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="385ad-161">Feature ist in dieser Phase deaktiviert</span><span class="sxs-lookup"><span data-stu-id="385ad-161">Feature is disabled during this stage</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="385ad-162">Wenn Reaktionsgruppen nicht importiert wurden, schlagen Aufrufe fehl.</span><span class="sxs-lookup"><span data-stu-id="385ad-162">If response groups were not imported, calls fail.</span></span></p></li>
<li><p><span data-ttu-id="385ad-163">Bei importierten Antwortgruppen werden Aufrufe erfolgreich ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="385ad-163">For imported response groups, calls succeed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="385ad-164">Informationen zu Anmelde-und Agent-Agents</span><span class="sxs-lookup"><span data-stu-id="385ad-164">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="385ad-165">Agentengruppen, die im Besitz des primären Pools sind, können auf der Agentenkonsole angezeigt werden, aber die Agents können sich nicht anmelden.</span><span class="sxs-lookup"><span data-stu-id="385ad-165">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="385ad-166">Agentengruppen, die im Besitz des Sicherungs Pools sind, können auf der Agentenkonsole angezeigt werden, und die Agents können sich anmelden.</span><span class="sxs-lookup"><span data-stu-id="385ad-166">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="385ad-167">Importierte Agentengruppen werden auf der Agentenkonsole angezeigt, und die Agents können sich anmelden.</span><span class="sxs-lookup"><span data-stu-id="385ad-167">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="385ad-168">Agentengruppen, die im Besitz des primären Pools sind, können auf der Agentenkonsole angezeigt werden, aber die Agents können sich nicht anmelden.</span><span class="sxs-lookup"><span data-stu-id="385ad-168">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="385ad-169">Agentengruppen, die im Besitz des Sicherungs Pools sind, können auf der Agentenkonsole angezeigt werden, und die Agents können sich anmelden.</span><span class="sxs-lookup"><span data-stu-id="385ad-169">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="385ad-170">Importierte Agentengruppen werden auf der Agentenkonsole angezeigt, und die Agents können sich anmelden.</span><span class="sxs-lookup"><span data-stu-id="385ad-170">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="385ad-171">Reaktionsgruppen Konfiguration</span><span class="sxs-lookup"><span data-stu-id="385ad-171">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="385ad-172">Antwortgruppen, die im Besitz des primären Pools sind, können je nach Verfügbarkeit der Back-End-Datenbank des primären Pools angezeigt, aber nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="385ad-172">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="385ad-173">Antwortgruppen, die im Besitz des Sicherungs Pools sind, können angezeigt und geändert werden.</span><span class="sxs-lookup"><span data-stu-id="385ad-173">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="385ad-174">Importierte Antwortgruppen können nicht mit der lync Server-Systemsteuerung oder dem Reaktionsgruppen-Konfigurations Tool angezeigt werden, können aber mithilfe der lync Server-Verwaltungsshell-Cmdlets konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="385ad-174">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="385ad-175">Antwortgruppen, die dem primären Pool gehören, können abhängig von der Verfügbarkeit der Back-End-Datenbank angezeigt, aber nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="385ad-175">Response groups owned by the primary pool can be viewed, depending on the availability of the back end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="385ad-176">Antwortgruppen, die im Besitz des Sicherungs Pools sind, können angezeigt und geändert werden.</span><span class="sxs-lookup"><span data-stu-id="385ad-176">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="385ad-177">Importierte Antwortgruppen können nicht mit der lync Server-Systemsteuerung oder dem Reaktionsgruppen-Konfigurations Tool angezeigt werden, können aber mithilfe der lync Server-Verwaltungsshell-Cmdlets konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="385ad-177">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-experience-during-failback"></a><span data-ttu-id="385ad-178">Benutzerfreundlichkeit während des Failback</span><span class="sxs-lookup"><span data-stu-id="385ad-178">User Experience During Failback</span></span>

<span data-ttu-id="385ad-179">Wenn ein Administrator Failback für den primären Pool aufruft, werden die Reaktionsgruppen Aktivitäten während und nach dem Failback verarbeitet, wie in der folgenden Tabelle beschrieben.</span><span class="sxs-lookup"><span data-stu-id="385ad-179">When an administrator invokes failback to the primary pool, response group activity is handled during and after the failback as described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="385ad-180">Während der Disaster Recovery Verhalten sich Anrufe anders, je nachdem, ob die primären Pool Antwortgruppen während der Wiederherstellung in den Backup-Pool importiert wurden.</span><span class="sxs-lookup"><span data-stu-id="385ad-180">During disaster recovery, calls behave differently depending on whether the primary pool response groups were imported to the backup pool during recovery.</span></span> <span data-ttu-id="385ad-181">In der folgenden Tabelle sind Verweise auf importierte Antwortgruppen darauf hinweisen, dass primäre Pool Antwortgruppen während des Disaster Recovery-Modus in den Sicherungspool importiert wurden.</span><span class="sxs-lookup"><span data-stu-id="385ad-181">In the following table, references to imported response groups mean that primary pool response groups were imported to the backup pool during disaster recovery mode.</span></span>



</div>

### <a name="call-handling-in-failback"></a><span data-ttu-id="385ad-182">Anrufbehandlung in Failback</span><span class="sxs-lookup"><span data-stu-id="385ad-182">Call Handling in Failback</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="385ad-183">Art des Anrufs oder der Benutzeraktion</span><span class="sxs-lookup"><span data-stu-id="385ad-183">Type of call or user action</span></span></th>
<th><span data-ttu-id="385ad-184">Während des Failback</span><span class="sxs-lookup"><span data-stu-id="385ad-184">During Failback</span></span></th>
<th><span data-ttu-id="385ad-185">Nach Abschluss des Failback</span><span class="sxs-lookup"><span data-stu-id="385ad-185">After Failback Completes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="385ad-186">Anrufe, die mit einem Agenten verbunden sind</span><span class="sxs-lookup"><span data-stu-id="385ad-186">Calls connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="385ad-187">Reguläre Anrufe bleiben verbunden.</span><span class="sxs-lookup"><span data-stu-id="385ad-187">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="385ad-188">Wenn Reaktionsgruppen nicht importiert wurden, befinden sich in diesem Status keine anonymen Anrufe.</span><span class="sxs-lookup"><span data-stu-id="385ad-188">If response groups were not imported, no anonymous calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="385ad-189">Bei importierten Antwortgruppen bleiben anonyme Anrufe verbunden.</span><span class="sxs-lookup"><span data-stu-id="385ad-189">For imported response groups, anonymous calls remain connected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="385ad-190">Reguläre Anrufe bleiben verbunden.</span><span class="sxs-lookup"><span data-stu-id="385ad-190">Regular calls remain connected.</span></span></p></li>
<li><p><span data-ttu-id="385ad-191">Wenn Reaktionsgruppen nicht importiert wurden, befinden sich in diesem Status keine anonymen Anrufe.</span><span class="sxs-lookup"><span data-stu-id="385ad-191">If response groups were not imported, no anonymous calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="385ad-192">Bei importierten Antwortgruppen bleiben anonyme Anrufe verbunden.</span><span class="sxs-lookup"><span data-stu-id="385ad-192">For imported response groups, anonymous calls remain connected.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="385ad-193">In Bearbeitung befindliche Anrufe, die noch nicht mit einem Agenten verbunden sind</span><span class="sxs-lookup"><span data-stu-id="385ad-193">In progress calls not yet connected to an agent</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="385ad-194">Wenn Reaktionsgruppen nicht importiert wurden, befinden sich in diesem Status keine Anrufe.</span><span class="sxs-lookup"><span data-stu-id="385ad-194">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="385ad-195">Bei importierten Antwortgruppen werden Anrufe getrennt.</span><span class="sxs-lookup"><span data-stu-id="385ad-195">For imported response groups, calls will be disconnected.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="385ad-196">Wenn Reaktionsgruppen nicht importiert wurden, befinden sich in diesem Status keine Anrufe.</span><span class="sxs-lookup"><span data-stu-id="385ad-196">If response groups were not imported, no calls are in this status.</span></span></p></li>
<li><p><span data-ttu-id="385ad-197">Bei importierten Antwortgruppen werden Anrufe getrennt.</span><span class="sxs-lookup"><span data-stu-id="385ad-197">For imported response groups, calls will be disconnected.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="385ad-198">Neue Anrufe</span><span class="sxs-lookup"><span data-stu-id="385ad-198">New calls</span></span></p></td>
<td><p><span data-ttu-id="385ad-199">Anrufe stellen eine Verbindung mit dem primären Pool her, aber die im primären Pool verwalteten Agents sind nicht erreichbar.</span><span class="sxs-lookup"><span data-stu-id="385ad-199">Calls connect to the primary pool, but agents homed in the primary pool are unreachable.</span></span></p></td>
<td><p><span data-ttu-id="385ad-200">Anrufe stellen eine Verbindung mit dem primären Pool her.</span><span class="sxs-lookup"><span data-stu-id="385ad-200">Calls connect to the primary pool.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="385ad-201">Agenten Anrufe im Namen der Reaktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="385ad-201">Agent calls on behalf of response group</span></span></p></td>
<td><p><span data-ttu-id="385ad-202">Das Feature ist in dieser Phase deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="385ad-202">Feature is disabled during this stage.</span></span></p></td>
<td><p><span data-ttu-id="385ad-203">Anrufe erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="385ad-203">Calls succeed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="385ad-204">Informationen zu Anmelde-und Agent-Agents</span><span class="sxs-lookup"><span data-stu-id="385ad-204">Agent sign-in and agent information</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="385ad-205">Agentengruppen, die im Besitz des primären Pools sind, können auf der Agentenkonsole angezeigt werden, aber die Agents können sich nicht anmelden.</span><span class="sxs-lookup"><span data-stu-id="385ad-205">Agent groups owned by the primary pool can be viewed on agent console but agents cannot sign in.</span></span></p></li>
<li><p><span data-ttu-id="385ad-206">Agentengruppen, die im Besitz des Sicherungs Pools sind, können auf der Agentenkonsole angezeigt werden, und die Agents können sich anmelden.</span><span class="sxs-lookup"><span data-stu-id="385ad-206">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="385ad-207">Importierte Agentengruppen werden auf der Agentenkonsole angezeigt, und die Agents können sich anmelden.</span><span class="sxs-lookup"><span data-stu-id="385ad-207">Imported agent groups are displayed on agent console and agents can sign in.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="385ad-208">Agentengruppen, die im Besitz des primären Pools sind, können auf der Agentenkonsole angezeigt werden, und die Agents können sich anmelden.</span><span class="sxs-lookup"><span data-stu-id="385ad-208">Agent groups owned by the primary pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="385ad-209">Agentengruppen, die im Besitz des Sicherungs Pools sind, können auf der Agentenkonsole angezeigt werden, und die Agents können sich anmelden.</span><span class="sxs-lookup"><span data-stu-id="385ad-209">Agent groups owned by the backup pool can be viewed on agent console and agents can sign in.</span></span></p></li>
<li><p><span data-ttu-id="385ad-210">Importierte Agentengruppen werden auf der Agentenkonsole nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="385ad-210">Imported agent groups are not displayed on agent console.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="385ad-211">Reaktionsgruppen Konfiguration</span><span class="sxs-lookup"><span data-stu-id="385ad-211">Response group configuration</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="385ad-212">Antwortgruppen, die im Besitz des primären Pools sind, können je nach Verfügbarkeit der Back-End-Datenbank des primären Pools angezeigt, aber nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="385ad-212">Response groups owned by the primary pool can be viewed, depending on the availability of the primary pool’s back-end database, but cannot be modified.</span></span></p></li>
<li><p><span data-ttu-id="385ad-213">Antwortgruppen, die im Besitz des Sicherungs Pools sind, können angezeigt und geändert werden.</span><span class="sxs-lookup"><span data-stu-id="385ad-213">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="385ad-214">Importierte Antwortgruppen können nicht mit der lync Server-Systemsteuerung oder dem Reaktionsgruppen-Konfigurations Tool angezeigt werden, können aber mithilfe der lync Server-Verwaltungsshell-Cmdlets konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="385ad-214">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="385ad-215">Antwortgruppen, die im Besitz des primären Pools sind, können angezeigt und geändert werden.</span><span class="sxs-lookup"><span data-stu-id="385ad-215">Response groups owned by the primary pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="385ad-216">Antwortgruppen, die im Besitz des Sicherungs Pools sind, können angezeigt und geändert werden.</span><span class="sxs-lookup"><span data-stu-id="385ad-216">Response groups owned by the backup pool can be viewed and modified.</span></span></p></li>
<li><p><span data-ttu-id="385ad-217">Importierte Antwortgruppen können nicht mit der lync Server-Systemsteuerung oder dem Reaktionsgruppen-Konfigurations Tool angezeigt werden, können aber mithilfe der lync Server-Verwaltungsshell-Cmdlets konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="385ad-217">Imported response groups cannot be viewed with Lync Server Control Panel or the Response Group Configuration Tool, but can be configured by using Lync Server Management Shell cmdlets.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="385ad-218">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="385ad-218">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

