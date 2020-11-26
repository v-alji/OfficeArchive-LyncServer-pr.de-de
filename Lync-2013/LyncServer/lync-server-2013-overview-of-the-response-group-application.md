---
title: 'Lync Server 2013: Übersicht über die reaktionsgruppenanwendung'
description: 'Lync Server 2013: Übersicht über die reaktionsgruppenanwendung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of the Response Group application
ms:assetid: 6cc333e7-4029-4372-86b2-016040c415fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398513(v=OCS.15)
ms:contentKeyID: 48184453
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 763a64adcf0eaf43e8f98a49cd850882ca9c91c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424716"
---
# <a name="overview-of-the-response-group-application-in-lync-server-2013"></a><span data-ttu-id="85501-103">Übersicht über die reaktionsgruppenanwendung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85501-103">Overview of the Response Group application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="85501-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="85501-104">

<span> </span></span></span>

<span data-ttu-id="85501-105">_**Letztes Änderungsdatum des Themas:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="85501-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="85501-106">Wenn ein Anrufer eine Reaktionsgruppe anruft, wird der Anruf basierend auf einem Sammelanschluss oder den interaktiven Sprachantworten des Anrufers an einen Agent weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="85501-106">When a caller calls a response group, the call is routed to an agent based on a hunt group or the caller's answers to interactive voice response (IVR) questions.</span></span> <span data-ttu-id="85501-107">Die reaktionsgruppenanwendung verwendet standardmäßige Reaktionsgruppen-Routingmethoden, um den Anruf an den nächsten verfügbaren Agenten weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="85501-107">The Response Group application uses standard response group routing methods to route the call to the next available agent.</span></span> <span data-ttu-id="85501-108">Zu den Anruf Weiterleitungs Methoden gehören Serial-, Long-Idle-, parallel-, Round Robin-und Attendant-Routing (das heißt, alle Agents werden zur gleichen Zeit für jeden eingehenden Anruf aufgerufen, unabhängig von deren derzeitigem vorhanden sein).</span><span class="sxs-lookup"><span data-stu-id="85501-108">Call routing methods include serial, longest-idle, parallel, round robin, and Attendant routing (that is, all agents are called at the same time for every incoming call, regardless of their current presence).</span></span> <span data-ttu-id="85501-109">Wenn keine Agents verfügbar sind, wird der Anruf in einer Warteschleife platziert, bis ein Agent verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="85501-109">If no agents are available, the call is held in a queue until an agent is available.</span></span> <span data-ttu-id="85501-110">Wenn sich ein Anrufer in der Warteschleife befindet, wird Musik wiedergegeben, bis ein verfügbarer Agent den Anruf entgegennimmt.</span><span class="sxs-lookup"><span data-stu-id="85501-110">While in the queue, the caller hears music until an available agent accepts the call.</span></span> <span data-ttu-id="85501-111">Wenn es sich um eine vollständige Warteschlange handelt oder wenn der Anruf in der Warteschlange abläuft, hört der Anrufer möglicherweise eine Nachricht und wird dann entweder getrennt oder an ein anderes Ziel übertragen.</span><span class="sxs-lookup"><span data-stu-id="85501-111">If the queue is full, or if the call times out while in the queue, the caller might hear a message and then is either disconnected or transferred to a different destination.</span></span> <span data-ttu-id="85501-112">Wenn ein Agent den Anruf entgegennimmt, kann dem Anrufer abhängig davon, wie der Administrator die Reaktionsgruppe konfiguriert, die Identität des Agents angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="85501-112">When an agent accepts the call, the caller might or might not be able to see the agent's identity, depending on how the administrator configures the response group.</span></span> <span data-ttu-id="85501-113">Bei Agents kann es sich um formelle Agents handeln, die sich bei der Gruppe anmelden müssen, bevor sie Anrufe an die Gruppe entgegennehmen können, oder um informelle Agents, die sich nicht bei der Gruppe an- und abmelden müssen, um Anrufe zu beantworten.</span><span class="sxs-lookup"><span data-stu-id="85501-113">Agents can either be formal, which means that they must sign in to the group before they can accept calls routed to the group, or informal, which means that they do not sign into and out of the group to accept calls.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="85501-114">Nur lokale Benutzer können Agents sein.</span><span class="sxs-lookup"><span data-stu-id="85501-114">Only on-premises users can be agents.</span></span> <span data-ttu-id="85501-115">Wenn ein Agent von lokal in Online verschoben wird, werden keine Antwortgruppen Aufrufe an diesen Agenten weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="85501-115">If an agent is moved from on-premises to online, Response Group calls will not be routed to that agent.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="85501-116">Die Antwortgruppen Anwendung verwendet einen internen Dienst, der als Übereinstimmungs Erstellung bezeichnet wird, um Anrufe in die Warteschlange zu stellen und verfügbare Agents zu finden.</span><span class="sxs-lookup"><span data-stu-id="85501-116">The Response Group application uses an internal service, called Match Making, to queue calls and find available agents.</span></span> <span data-ttu-id="85501-117">Jeder Computer, auf dem die reaktionsgruppenanwendung ausgeführt wird, führt den Übereinstimmungs Dienst aus, aber es ist jeweils nur ein Übereinstimmungs Dienst pro lync-Server Pool aktiv – die anderen sind passiv.</span><span class="sxs-lookup"><span data-stu-id="85501-117">Each computer that runs the Response Group application runs the Match Making service, but only one Match Making service per Lync Server pool is active at a time--the others are passive.</span></span> <span data-ttu-id="85501-118">Wenn der aktive Übereinstimmungs Dienst während eines ungeplanten Ausfalls nicht mehr verfügbar ist, wird einer der passiven Übereinstimmungs Dienste aktiviert.</span><span class="sxs-lookup"><span data-stu-id="85501-118">If the active Match Making service becomes unavailable during an unplanned outage, one of the passive Match Making services becomes active.</span></span> <span data-ttu-id="85501-119">Die Response Group-Anwendung tut ihr Bestes, um sicherzustellen, dass Anrufweiterleitung und-Warteschlangen unterbrechungsfrei fortgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="85501-119">The Response Group application does its best to make sure that call routing and queuing continues uninterrupted.</span></span> <span data-ttu-id="85501-120">Wenn jedoch eine Übereinstimmung zum Dienst Übergang eintritt, gehen alle Anrufe, die zu diesem Zeitpunkt übertragen werden, verloren.</span><span class="sxs-lookup"><span data-stu-id="85501-120">However, when a Match Making service transition occurs, any calls that are in transfer at the time are lost.</span></span> <span data-ttu-id="85501-121">Wenn der Übergang beispielsweise auf den Ausfall des Front-End-Servers zurückzuführen ist, gehen alle Anrufe, die derzeit vom aktiven Übereinstimmungs Dienst auf dem Front-End-Server abgewickelt werden, ebenfalls verloren.</span><span class="sxs-lookup"><span data-stu-id="85501-121">For example, if the transition is due to the Front End Server going down, any calls currently being handled by the active Match Making service on that Front End Server are also lost.</span></span>



</div>

<span data-ttu-id="85501-122">In lync Server 2013 stehen zwei Verwaltungsrollen für die Verwaltung von Reaktionsgruppen zur Verfügung: Antwortgruppen-Manager und Antwortgruppen Administrator.</span><span class="sxs-lookup"><span data-stu-id="85501-122">In Lync Server 2013, two management roles are available for managing response groups: Response Group Manager and Response Group Administrator.</span></span> <span data-ttu-id="85501-123">Reaktionsgruppen Administratoren können alle Aspekte jeder Reaktionsgruppe verwalten.</span><span class="sxs-lookup"><span data-stu-id="85501-123">Response Group Administrators can manage any aspect of any response group.</span></span> <span data-ttu-id="85501-124">Antwortgruppen-Manager können nur bestimmte Aspekte verwalten, und zwar nur für die Antwortgruppen, die Sie besitzen.</span><span class="sxs-lookup"><span data-stu-id="85501-124">Response Group Managers can manage only certain aspects, and only for the response groups that they own.</span></span> <span data-ttu-id="85501-125">Die neue Manager-Rolle kann dazu beitragen, die Verwaltungskosten zu senken, da Sie für bestimmte Antwortgruppen begrenzte Zuständigkeiten an alle Benutzer delegieren können, die für Enterprise-VoIP aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="85501-125">The new Manager role can help reduce administration costs, because you can delegate limited responsibilities for specific response groups to any user who is enabled for Enterprise Voice.</span></span>

<span data-ttu-id="85501-126">Um der neuen Manager-Rolle gerecht zu werden, führt die lync Server 2013 Response Group-Anwendung einen **Workflowtyp** verwalteter oder nicht verwalteter Ressourcen ein.</span><span class="sxs-lookup"><span data-stu-id="85501-126">To accommodate the new Manager role, Lync Server 2013 Response Group application introduces a **Workflow Type** of Managed or Unmanaged.</span></span> <span data-ttu-id="85501-127">In der folgenden Tabelle werden die verwalteten und nicht verwalteten Reaktionsgruppen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="85501-127">The following table describes Managed and Unmanaged response groups.</span></span>

### <a name="managed-and-unmanaged-response-groups"></a><span data-ttu-id="85501-128">Verwaltete und nicht verwaltete Reaktionsgruppen</span><span class="sxs-lookup"><span data-stu-id="85501-128">Managed and Unmanaged Response Groups</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85501-129">Reaktionsgruppentyp</span><span class="sxs-lookup"><span data-stu-id="85501-129">Response group type</span></span></th>
<th><span data-ttu-id="85501-130">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85501-130">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85501-131">Nicht verwaltet</span><span class="sxs-lookup"><span data-stu-id="85501-131">Unmanaged</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="85501-132">Nicht verwalteten Reaktionsgruppen ist kein Manager zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="85501-132">Unmanaged response groups have no assigned Managers.</span></span> <span data-ttu-id="85501-133">Diese Reaktionsgruppen können nur vom Administrator der Reaktionsgruppe konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="85501-133">Only the Response Group Administrator can configure these response groups.</span></span></p></li>
<li><p><span data-ttu-id="85501-134">Mehrere nicht verwaltete Reaktionsgruppen können eine Warteschleife oder Agentgruppe gemeinsam verwenden.</span><span class="sxs-lookup"><span data-stu-id="85501-134">Multiple unmanaged response groups can share a queue or agent group.</span></span></p></li>
<li><p><span data-ttu-id="85501-135">Wenn Sie Antwortgruppen von einer früheren Version zu lync Server 2013 migrieren, wird der Typ auf "nicht verwaltet" gesetzt.</span><span class="sxs-lookup"><span data-stu-id="85501-135">When you migrate response groups from a prior version to Lync Server 2013, the type is set to Unmanaged.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85501-136">Verwaltet</span><span class="sxs-lookup"><span data-stu-id="85501-136">Managed</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="85501-137">Reaktionsgruppen Administratoren können alle Aspekte von verwalteten Reaktionsgruppen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="85501-137">Response Group Administrators can configure any aspect of managed response groups.</span></span></p></li>
<li><p><span data-ttu-id="85501-138">Reaktionsgruppen-Manager können keine Antwortgruppen anzeigen oder ändern, die Ihnen nicht explizit zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="85501-138">Response Group Managers cannot view or modify response groups that are not explicitly assigned to them.</span></span></p></li>
<li><p><span data-ttu-id="85501-139">Reaktionsgruppen-Manager können nur einige Einstellungen für die Reaktionsgruppen konfigurieren, die Ihnen explizit zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="85501-139">Response Group Managers can configure only some settings for the response groups that are explicitly assigned to them.</span></span></p></li>
<li><p><span data-ttu-id="85501-140">Verwaltete Reaktionsgruppen können keine Warteschleifen oder Agentgruppen gemeinsam mit anderen Reaktionsgruppen, weder mit verwalteten noch nicht verwalteten, verwenden.</span><span class="sxs-lookup"><span data-stu-id="85501-140">Managed response groups can't share any queues or agent groups with any other response group, managed or unmanaged.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="85501-141">In der folgenden Tabelle werden die Aktionen beschrieben, die von Reaktionsgruppen-Managern für die Ihnen zugewiesenen Antwortgruppen ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="85501-141">The following table describes the actions that Response Group Managers can and cannot perform for the response groups assigned to them.</span></span>

### <a name="response-group-manager-capabilities"></a><span data-ttu-id="85501-142">Funktionen der Reaktionsgruppenmanager</span><span class="sxs-lookup"><span data-stu-id="85501-142">Response Group Manager Capabilities</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85501-143">Konfiguration von:</span><span class="sxs-lookup"><span data-stu-id="85501-143">Can configure:</span></span></th>
<th><span data-ttu-id="85501-144">Erstellen, Löschen, Konfigurieren von:</span><span class="sxs-lookup"><span data-stu-id="85501-144">Can create, delete, or configure:</span></span></th>
<th><span data-ttu-id="85501-145">Nicht möglich:</span><span class="sxs-lookup"><span data-stu-id="85501-145">Cannot:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><ul>
<li><p><span data-ttu-id="85501-146">Agents</span><span class="sxs-lookup"><span data-stu-id="85501-146">Agents</span></span></p></li>
<li><p><span data-ttu-id="85501-147">Willkommensnachrichten</span><span class="sxs-lookup"><span data-stu-id="85501-147">Welcome message</span></span></p></li>
<li><p><span data-ttu-id="85501-148">Name der Reaktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="85501-148">Response Group name</span></span></p></li>
<li><p><span data-ttu-id="85501-149">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85501-149">Description</span></span></p></li>
<li><p><span data-ttu-id="85501-150">Anzeigenummer</span><span class="sxs-lookup"><span data-stu-id="85501-150">Display number</span></span></p></li>
<li><p><span data-ttu-id="85501-151">Geschäftszeiten</span><span class="sxs-lookup"><span data-stu-id="85501-151">Business hours</span></span></p></li>
<li><p><span data-ttu-id="85501-152">Wartemusik</span><span class="sxs-lookup"><span data-stu-id="85501-152">Music on hold</span></span></p></li>
<li><p><span data-ttu-id="85501-153">Status (aktiv/inaktiv)</span><span class="sxs-lookup"><span data-stu-id="85501-153">Status (active/inactive)</span></span></p></li>
<li><p><span data-ttu-id="85501-154">Workflows für Sammelanschlüsse oder für Interaktive Sprachantwort (Interactive Voice Response, IVR)</span><span class="sxs-lookup"><span data-stu-id="85501-154">Hunt group workflows or Interactive voice response (IVR) workflows</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="85501-155">Agentgruppen</span><span class="sxs-lookup"><span data-stu-id="85501-155">Agent Groups</span></span></p></li>
<li><p><span data-ttu-id="85501-156">Warteschleifen</span><span class="sxs-lookup"><span data-stu-id="85501-156">Queues</span></span></p></li>
<li><p><span data-ttu-id="85501-157">Feiertagssätze</span><span class="sxs-lookup"><span data-stu-id="85501-157">Holiday sets</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="85501-158">Erstellen oder Löschen beliebiger Workflowtypen</span><span class="sxs-lookup"><span data-stu-id="85501-158">Create or delete any type of workflow</span></span></p></li>
<li><p><span data-ttu-id="85501-159">Ändern grundlegender Reaktionsgruppeneinstellungen wie <strong>SIP-URI</strong>, <strong>Telefonnummer</strong> oder <strong>Workflowtyp</strong>.</span><span class="sxs-lookup"><span data-stu-id="85501-159">Modify core response group settings, such as: <strong>SIP URI</strong>, <strong>Telephone Number</strong>, or <strong>Workflow Type</strong>.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="85501-160">Antwortgruppen-Manager können die folgenden Tools verwenden, um Ihre vorgesehenen Antwortgruppen zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="85501-160">Response Group Managers can use the following tools to manage their designated response groups.</span></span>

  - <span data-ttu-id="85501-161">Lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="85501-161">Lync Server Control Panel</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="85501-162">Antwortgruppen-Manager können mit diesem Tool nur Einstellungen für die Reaktionsgruppe verwalten.</span><span class="sxs-lookup"><span data-stu-id="85501-162">Response Group Managers can only manage Response Group settings with this tool.</span></span> <span data-ttu-id="85501-163">Andere lync-Server Einstellungen stehen Managern nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="85501-163">Other Lync Server settings are not available to Managers.</span></span>

    
    </div>

  - <span data-ttu-id="85501-164">Konfigurationstool für Reaktionsgruppen</span><span class="sxs-lookup"><span data-stu-id="85501-164">Response Group Configuration Tool</span></span>

  - <span data-ttu-id="85501-165">Lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="85501-165">Lync Server Management Shell</span></span>

<span data-ttu-id="85501-166">Die Reaktionsgruppe eignet sich gut für Abteilungs-oder Arbeitsgruppenumgebungen (Details finden Sie unter [Kapazitätsplanung für die Reaktionsgruppe in lync Server 2013](lync-server-2013-capacity-planning-for-response-group.md)) und kann in völlig neuen Telefonieanlagen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="85501-166">Response Group scales well to departmental or workgroup environments (for details, see [Capacity planning for Response Group in Lync Server 2013](lync-server-2013-capacity-planning-for-response-group.md)) and can be deployed in entirely new telephony installations.</span></span> <span data-ttu-id="85501-167">Sie unterstützt eingehende Anrufe von der Enterprise-VoIP-Bereitstellung und vom lokalen Netzbetreiber Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="85501-167">It supports incoming calls from the Enterprise Voice deployment and from the local carrier network.</span></span> <span data-ttu-id="85501-168">Agents können lync 2013, lync 2010, lync 2010 Attendant oder lync Phone Edition verwenden, um die an Sie weitergeleiteten Anrufe zu übernehmen.</span><span class="sxs-lookup"><span data-stu-id="85501-168">Agents can use Lync 2013, Lync 2010, Lync 2010 Attendant, or Lync Phone Edition to take the calls routed to them.</span></span>

<span data-ttu-id="85501-169">Die Response Group-Anwendung ist eine Komponente von Enterprise-VoIP.</span><span class="sxs-lookup"><span data-stu-id="85501-169">The Response Group application is a component of Enterprise Voice.</span></span> <span data-ttu-id="85501-170">Wenn Sie Enterprise-VoIP bereitstellen, wird die reaktionsgruppenanwendung automatisch installiert und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="85501-170">When you deploy Enterprise Voice, the Response Group application is installed and activated automatically.</span></span>

<span data-ttu-id="85501-171"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="85501-171"></div>

<span> </span>

</div>

</div>

</span></span></div>

