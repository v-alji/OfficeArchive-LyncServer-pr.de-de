---
title: 'Lync Server 2013: Bereitstellungsvorgang beim standortbasierten Routing'
description: 'Lync Server 2013: Bereitstellungsprozess für Location-Based Routing'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment process for Location-Based Routing
ms:assetid: 9e923e72-83fc-4a4f-8937-28a55739ed3e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994055(v=OCS.15)
ms:contentKeyID: 51803966
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2c321d9b0eada6e9501b2ded69120feae36be171
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394906"
---
# <a name="deployment-process-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="23649-103">Bereitstellungsvorgang beim standortbasierten Routing in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="23649-103">Deployment process for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="23649-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="23649-104">

<span> </span></span></span>

<span data-ttu-id="23649-105">_**Letztes Änderungsdatum des Themas:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="23649-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="23649-106">Dieses Thema bietet eine Übersicht über den Prozess, der beim Konfigurieren Location-Based Routings erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="23649-106">This topic provides an overview of the process involved in configuring Location-Based Routing.</span></span> <span data-ttu-id="23649-107">Sie müssen lync Server Enterprise Edition oder Standard Edition mit Enterprise-VoIP bereitstellen, bevor Sie Location-Based Routing konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="23649-107">You must deploy Lync Server Enterprise Edition or Standard Edition with Enterprise Voice before you configure Location-Based Routing.</span></span> <span data-ttu-id="23649-108">Die für Location-Based Routing erforderlichen Komponenten sind bereits bei der Bereitstellung von Enterprise-VoIP installiert und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="23649-108">The components required by Location-Based Routing are already installed and enabled when you deploy Enterprise Voice.</span></span>

### <a name="location-based-routing-deployment-process"></a><span data-ttu-id="23649-109">Location-Based Routing Bereitstellungsprozess</span><span class="sxs-lookup"><span data-stu-id="23649-109">Location-Based Routing Deployment Process</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23649-110">Phase</span><span class="sxs-lookup"><span data-stu-id="23649-110">Phase</span></span></th>
<th><span data-ttu-id="23649-111">Schritte</span><span class="sxs-lookup"><span data-stu-id="23649-111">Steps</span></span></th>
<th><span data-ttu-id="23649-112">Erforderliche Gruppen und Rollen</span><span class="sxs-lookup"><span data-stu-id="23649-112">Required groups and roles</span></span></th>
<th><span data-ttu-id="23649-113">Bereitstellungsdokumentation</span><span class="sxs-lookup"><span data-stu-id="23649-113">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23649-114">Bereitstellen von Enterprise-VoIP</span><span class="sxs-lookup"><span data-stu-id="23649-114">Deploy Enterprise Voice</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="23649-115">Konfigurieren von Trunks</span><span class="sxs-lookup"><span data-stu-id="23649-115">Configure Trunks</span></span></p></li>
<li><p><span data-ttu-id="23649-116">Erstellen von VoIP-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="23649-116">Create Voice Policies</span></span></p></li>
<li><p><span data-ttu-id="23649-117">Definieren von VoIP-Routen</span><span class="sxs-lookup"><span data-stu-id="23649-117">Define Voice Routes</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="23649-118">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="23649-118">CSVoiceAdmins</span></span><br />
<span data-ttu-id="23649-119">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="23649-119">CsAdministrator</span></span><br />
<span data-ttu-id="23649-120">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="23649-120">CsServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="23649-121">Bereitstellen von Enterprise-VoIP</span><span class="sxs-lookup"><span data-stu-id="23649-121">Deploying Enterprise Voice</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23649-122">Überprüfen Ihrer Enterprise-VoIP-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="23649-122">Verify your Enterprise Voice deployment</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23649-123">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="23649-123">CSVoiceAdmins</span></span><br />
<span data-ttu-id="23649-124">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="23649-124">CsAdministrator</span></span><br />
<span data-ttu-id="23649-125">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="23649-125">CsServerAdministrator</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23649-126">Konfigurieren von netzwerkregionen,-Websites und-Subnetzen</span><span class="sxs-lookup"><span data-stu-id="23649-126">Configure network regions, sites, and subnets</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="23649-127">Erstellen von netzwerkregionen</span><span class="sxs-lookup"><span data-stu-id="23649-127">Create network regions</span></span></p></li>
<li><p><span data-ttu-id="23649-128">Erstellen von Netzwerk Websites</span><span class="sxs-lookup"><span data-stu-id="23649-128">Create network sites</span></span></p></li>
<li><p><span data-ttu-id="23649-129">Ordnet Subnetze mit Netzwerkstandorten zu</span><span class="sxs-lookup"><span data-stu-id="23649-129">Associates subnets with network sites</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="23649-130">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="23649-130">CSVoiceAdmins</span></span><br />
<span data-ttu-id="23649-131">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="23649-131">CsAdministrator</span></span><br />
<span data-ttu-id="23649-132">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="23649-132">CsServerAdministrator</span></span></p></td>
<td><p><span data-ttu-id="23649-133">Informationen zu netzwerkregionen,-Websites und-Subnetzen</span><span class="sxs-lookup"><span data-stu-id="23649-133">About Network Regions, Sites, and Subnets</span></span><br />
<span data-ttu-id="23649-134">Erstellen oder Ändern eines Netzwerkbereichs</span><span class="sxs-lookup"><span data-stu-id="23649-134">Create or Modify a Network Region</span></span><br />
<span data-ttu-id="23649-135">Erstellen oder Ändern einer Netzwerk Website</span><span class="sxs-lookup"><span data-stu-id="23649-135">Create or Modify a Network Site</span></span><br />
<span data-ttu-id="23649-136">Zuordnen eines Subnetzes zu einer Netzwerk Website</span><span class="sxs-lookup"><span data-stu-id="23649-136">Associate a Subnet with a Network Site</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23649-137">Konfigurieren des Location-Based-Routings</span><span class="sxs-lookup"><span data-stu-id="23649-137">Configure Location-Based Routing</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="23649-138">Erstellen von VoIP-Routing Richtlinien</span><span class="sxs-lookup"><span data-stu-id="23649-138">Create voice routing policies</span></span></p></li>
<li><p><span data-ttu-id="23649-139">Separate trunk-Konfiguration pro trunk definieren</span><span class="sxs-lookup"><span data-stu-id="23649-139">Define separate trunk configuration per trunk</span></span></p></li>
<li><p><span data-ttu-id="23649-140">Ändern von VoIP-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="23649-140">Modify voice policies</span></span></p></li>
<li><p><span data-ttu-id="23649-141">Aktivieren Location-Based Routing Konfiguration</span><span class="sxs-lookup"><span data-stu-id="23649-141">Enable Location-Based Routing configuration</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="23649-142">CSVoiceAdmins</span><span class="sxs-lookup"><span data-stu-id="23649-142">CSVoiceAdmins</span></span><br />
<span data-ttu-id="23649-143">CsAdministrator</span><span class="sxs-lookup"><span data-stu-id="23649-143">CsAdministrator</span></span><br />
<span data-ttu-id="23649-144">CsServerAdministrator</span><span class="sxs-lookup"><span data-stu-id="23649-144">CsServerAdministrator</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>

## <a name="sample-deployment"></a><span data-ttu-id="23649-145">Beispielbereitstellung</span><span class="sxs-lookup"><span data-stu-id="23649-145">Sample Deployment</span></span>

<span data-ttu-id="23649-146">Die folgende Bereitstellung dient zur Veranschaulichung der Mechanismen, die durch Location-Based Routing aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="23649-146">The following deployment is used to illustrate further the mechanisms enabled by Location-Based Routing.</span></span>

<span data-ttu-id="23649-147">![e1bd2230-44da-4784-b359-24572b6ce02d](images/JJ994055.e1bd2230-44da-4784-b359-24572b6ce02d(OCS.15).png "e1bd2230-44da-4784-b359-24572b6ce02d")</span><span class="sxs-lookup"><span data-stu-id="23649-147">![e1bd2230-44da-4784-b359-24572b6ce02d](images/JJ994055.e1bd2230-44da-4784-b359-24572b6ce02d(OCS.15).png "e1bd2230-44da-4784-b359-24572b6ce02d")</span></span>

<div>

## <a name="incoming-pstn-calls"></a><span data-ttu-id="23649-148">Eingehende PSTN-Anrufe</span><span class="sxs-lookup"><span data-stu-id="23649-148">Incoming PSTN calls</span></span>

<span data-ttu-id="23649-149">Ein Administrator kann den trunk definieren, der zum Weiterleiten von Anrufen an "Standort 1 Gateway" für Location-Based Routing und zum Zuordnen des "Standort 1-Gateways" zu Website 1 definiert ist.</span><span class="sxs-lookup"><span data-stu-id="23649-149">An administrator can enable the trunk defined to route calls to “Site 1 Gateway” for Location-Based Routing and associate the “Site 1 Gateway” to site 1.</span></span> <span data-ttu-id="23649-150">Sobald die Option aktiviert ist, werden Anrufe, die über "Standort 1 Gateway" weitergeleitet werden, nur an Benutzer weitergeleitet, die sich in Standort 1 befinden.</span><span class="sxs-lookup"><span data-stu-id="23649-150">Once enabled, calls that are routed through “Site 1 Gateway“ will only be routed to users that are located in site 1.</span></span> <span data-ttu-id="23649-151">Alle Anrufe, die über den trunk "Standort 1 Gateway" geleitet werden, der für Benutzer an einer anderen Website bestimmt ist, wie etwa Standort 2, werden blockiert, um eine PSTN-Maut Umgehung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="23649-151">All calls routed through the “Site 1 Gateway” trunk destined to users in a different site, such as site 2 will be blocked to prevent PSTN toll bypass.</span></span>

<span data-ttu-id="23649-152">Alle eingehenden PSTN-Anrufe über "Standort 1 Gateway" dürfen nur an Endpunkte weitergeleitet werden, die sich in Standort 1 befinden.</span><span class="sxs-lookup"><span data-stu-id="23649-152">All incoming PSTN calls through “Site 1 Gateway” will only be allowed to route to endpoints located in site 1.</span></span> <span data-ttu-id="23649-153">Wenn beispielsweise "lync-Benutzer 1" zu Website 2 reist, werden alle eingehenden PSTN-Anrufe über "Standort 1 Gateway" nicht an die Endpunkte von "lync User 1" weitergeleitet, die sich in Standort 2 befinden.</span><span class="sxs-lookup"><span data-stu-id="23649-153">For example, when “Lync user 1” travels to site 2, all incoming PSTN calls through “Site 1 Gateway” will not be routed to “Lync user 1” endpoints located in site 2.</span></span> <span data-ttu-id="23649-154">Dieselbe Routingregel gilt, wenn "lync-Benutzer 1" zu einer unbekannten Netzwerk Website reist, in der der Standort des Benutzers nicht ermittelt werden kann.</span><span class="sxs-lookup"><span data-stu-id="23649-154">The same routing rule applies if “Lync user 1” travels to an unknown network site where the user’s location can’t be determined.</span></span>

<span data-ttu-id="23649-155">In der folgenden Tabelle wird die Benutzeroberfläche von "lync User 1" in diesem Kontext erläutert.</span><span class="sxs-lookup"><span data-stu-id="23649-155">The following table outlines the user experience of “Lync user 1” in this context.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="23649-156">Lync User 1-Endpunkte, die sich in Network Site 1 befinden</span><span class="sxs-lookup"><span data-stu-id="23649-156">Lync user 1 endpoints located in network site 1</span></span></th>
<th><span data-ttu-id="23649-157">Lync User 1-Endpunkte, die sich in Network Site 2 befinden</span><span class="sxs-lookup"><span data-stu-id="23649-157">Lync user 1 endpoints located in network site 2</span></span></th>
<th><span data-ttu-id="23649-158">Lync User 1-Endpunkte, die sich auf einer unbekannten Netzwerk Website befinden</span><span class="sxs-lookup"><span data-stu-id="23649-158">Lync user 1 endpoints located in unknown network site</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23649-159">Eingehende PSTN-Anrufe an lync-Benutzer 1</span><span class="sxs-lookup"><span data-stu-id="23649-159">Inbound PSTN calls to Lync user 1</span></span></p></td>
<td><p><span data-ttu-id="23649-160">Anrufe werden an Endpunkte an diesem Speicherort weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="23649-160">Calls are routed to endpoints in this location</span></span></p></td>
<td><p><span data-ttu-id="23649-161">Anrufe werden an diesem Standort nicht an Endpunkte weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="23649-161">Calls are not routed to endpoints in this location</span></span></p></td>
<td><p><span data-ttu-id="23649-162">Anrufe werden an diesem Standort nicht an Endpunkte weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="23649-162">Calls are not routed to endpoints in this location</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="outgoing-pstn-calls"></a><span data-ttu-id="23649-163">Ausgehende PSTN-Anrufe</span><span class="sxs-lookup"><span data-stu-id="23649-163">Outgoing PSTN calls</span></span>

<span data-ttu-id="23649-164">Auf VoIP-Routen wird in beiden VoIP-Richtlinien verwiesen, die Benutzern direkt zugewiesen sind, und für VoIP-Routing Richtlinien, die Netzwerk Websites zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="23649-164">Voice routes are referenced in both Voice Policies assigned directly to users, and Voice Routing Policies assigned to network sites.</span></span> <span data-ttu-id="23649-165">Beide Richtlinien enthalten Verweise auf Routen, die verwendet werden können, um einen Anruf anders weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="23649-165">Both policies contain references to routes, which can be used to route a call differently.</span></span> <span data-ttu-id="23649-166">Beispielsweise kann ein Administrator eine VoIP-Routing Richtlinie für alle Benutzer definieren, die sich auf der Netzwerk Website 1 befinden, um alle ausgehenden Anrufe über das "Standort 1 Gateway" weiterzuleiten, während die VoIP-Richtlinie einiger Benutzer eine Route für alle ausgehenden Anrufe über das "Standort-2-Gateway" definiert.</span><span class="sxs-lookup"><span data-stu-id="23649-166">For example, an administrator can define a Voice Routing Policy for all users located in network site 1 to route all outbound calls through the “Site 1 Gateway” while the Voice Policy of some users define a route for all outbound calls through the “Site 2 Gateway”.</span></span> <span data-ttu-id="23649-167">Während sich diese Benutzer auf der Netzwerk Website 1 befinden, werden Ihre ausgehenden Anrufe über das "Standort 1 Gateway" weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="23649-167">While these users are located in network site 1, their outbound calls will be routed through the “Site 1 Gateway”.</span></span>

<span data-ttu-id="23649-168">Wenn sich ein Benutzer in einer für Location-Based Routing konfigurierten Netzwerk Website befindet, überschreibt die VoIP-Routing Richtlinien Route des Netzwerkstandorts die VoIP-Richtlinien Route des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="23649-168">When a user is located in a network site configured for Location-Based Routing, the network site’s Voice Routing Policy route overrides the user’s Voice Policy route.</span></span> <span data-ttu-id="23649-169">Diese Regel eignet sich besonders für Benutzer, die temporär zu einer anderen Website wechseln.</span><span class="sxs-lookup"><span data-stu-id="23649-169">This rule is particularly useful for users that temporarily move to a different site.</span></span> <span data-ttu-id="23649-170">In diesem speziellen Fall wird ein Nutzer immer ein Gateway verwenden, das lokal an seinem Standort liegt; Wenn sich "lync User 3" auf "Website 2" befindet, werden alle ausgehenden Anrufe über "Standort 2-Gateway" weitergeleitet, aber wenn er zu Site 1 reist, werden alle ausgehenden Anrufe, die Sie bei Standort 1 getätigt haben, durch "Standort 1 Gateway" weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="23649-170">In this particular case a user will always use a gateway that is local to his location; if “Lync user 3” is located at “Site 2”, all his outbound calls will be routed via “Site 2 Gateway”, but if he travels to site 1, all his outbound calls placed while he’s at site 1 will be routed through “Site 1 Gateway”.</span></span>

<span data-ttu-id="23649-171">In der folgenden Tabelle wird die Benutzeroberfläche von lync User 1 veranschaulicht, die einen ausgehenden Anruf von den folgenden Netzwerkstandorten aus durchführen.</span><span class="sxs-lookup"><span data-stu-id="23649-171">The following table illustrates the user experience of Lync user 1 placing an outbound call from the following network sites.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="23649-172">Netzwerk Website 1</span><span class="sxs-lookup"><span data-stu-id="23649-172">Network site 1</span></span></th>
<th><span data-ttu-id="23649-173">Netzwerk Website 2</span><span class="sxs-lookup"><span data-stu-id="23649-173">Network site 2</span></span></th>
<th><span data-ttu-id="23649-174">Unbekannte Netzwerk Website oder für Location-Based Routing nicht aktiviert</span><span class="sxs-lookup"><span data-stu-id="23649-174">Unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23649-175">Autorisierung ausgehender Anrufe</span><span class="sxs-lookup"><span data-stu-id="23649-175">Authorization of outbound calls</span></span></p></td>
<td><p><span data-ttu-id="23649-176">Lync-Benutzer-1-VoIP-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="23649-176">Lync user 1 voice policy</span></span></p></td>
<td><p><span data-ttu-id="23649-177">Lync-Benutzer-1-VoIP-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="23649-177">Lync user 1 voice policy</span></span></p></td>
<td><p><span data-ttu-id="23649-178">Lync-Benutzer-1-VoIP-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="23649-178">Lync user 1 voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23649-179">Weiterleiten von ausgehenden Anrufen</span><span class="sxs-lookup"><span data-stu-id="23649-179">Routing of outbound calls</span></span></p></td>
<td><p><span data-ttu-id="23649-180">Website 1 – VoIP-Routing Richtlinie</span><span class="sxs-lookup"><span data-stu-id="23649-180">Site 1 voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="23649-181">Website 2 – VoIP-Routing Richtlinie</span><span class="sxs-lookup"><span data-stu-id="23649-181">Site 2 voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="23649-182">VoIP-Richtlinie des Benutzers und nur für Systeme, die für Location-Based Routing nicht aktiviert sind</span><span class="sxs-lookup"><span data-stu-id="23649-182">User’s voice policy and only to systems not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="call-transfers-and-forwards"></a><span data-ttu-id="23649-183">Anruf Übertragungen und Weiterleitungen</span><span class="sxs-lookup"><span data-stu-id="23649-183">Call transfers and forwards</span></span>

<span data-ttu-id="23649-184">Wenn Anrufe übertragen oder weitergeleitet werden, wird das Routing von Anrufen von Location-Based Routing beeinflusst.</span><span class="sxs-lookup"><span data-stu-id="23649-184">When calls are transferred or forwarded, the routing of calls is affected by Location-Based Routing.</span></span>

<span data-ttu-id="23649-185">Die folgende Tabelle zeigt, wie lync-Benutzer 1 einen PSTN-Anruf an einen anderen lync-Benutzer übertragen oder weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="23649-185">The following table depicts Lync user 1 transferring or forwarding a PSTN call to another Lync user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23649-186">Benutzer initiiert Anrufübertragung oder Weiterleitung</span><span class="sxs-lookup"><span data-stu-id="23649-186">User initiating call transfer or forward</span></span></th>
<th><span data-ttu-id="23649-187">Lync-Benutzer 2</span><span class="sxs-lookup"><span data-stu-id="23649-187">Lync user 2</span></span></th>
<th><span data-ttu-id="23649-188">Lync-Benutzer 4</span><span class="sxs-lookup"><span data-stu-id="23649-188">Lync user 4</span></span></th>
<th><span data-ttu-id="23649-189">Lync-Benutzer auf der Netzwerk Website für Location-Based Routing nicht aktiviert</span><span class="sxs-lookup"><span data-stu-id="23649-189">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23649-190">Lync-Benutzer 1</span><span class="sxs-lookup"><span data-stu-id="23649-190">Lync user 1</span></span></p></td>
<td><p><span data-ttu-id="23649-191">Anrufweiterleitung oder -durchstellung ist erlaubt</span><span class="sxs-lookup"><span data-stu-id="23649-191">Call forward or transfer is allowed</span></span></p></td>
<td><p><span data-ttu-id="23649-192">Anrufweiterleitung oder -durchstellung ist nicht erlaubt</span><span class="sxs-lookup"><span data-stu-id="23649-192">Call forward or transfer is not allowed</span></span></p></td>
<td><p><span data-ttu-id="23649-193">Anrufweiterleitung oder -durchstellung ist nicht erlaubt</span><span class="sxs-lookup"><span data-stu-id="23649-193">Call forward or transfer is not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="23649-194">In der folgenden Tabelle wird gezeigt, wie sich Location-Based Routing auf die Weiterleitung des Anrufs auswirkt, basierend auf dem Standort des lync-Benutzers, der übertragen wird (lync User 2, lync User 4 usw.) an einen PSTN-Endpunkt</span><span class="sxs-lookup"><span data-stu-id="23649-194">The following table illustrates how Location-Based Routing affects how the call is routed based on the location of the Lync user being transferred (Lync user 2, Lync user 4, etc) to a PSTN endpoint</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23649-195">Endpunkt, an den der Anruf übertragen oder weitergeleitet wird</span><span class="sxs-lookup"><span data-stu-id="23649-195">Endpoint where call is transferred or forwarded to</span></span></th>
<th><span data-ttu-id="23649-196">Lync-Benutzer 2</span><span class="sxs-lookup"><span data-stu-id="23649-196">Lync user 2</span></span></th>
<th><span data-ttu-id="23649-197">Lync-Benutzer 4</span><span class="sxs-lookup"><span data-stu-id="23649-197">Lync user 4</span></span></th>
<th><span data-ttu-id="23649-198">Lync-Benutzer auf der Netzwerk Website für Location-Based Routing nicht aktiviert</span><span class="sxs-lookup"><span data-stu-id="23649-198">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23649-199">Endpunkt im öffentlichen Telefonnetz</span><span class="sxs-lookup"><span data-stu-id="23649-199">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="23649-200">Anrufweiterleitung oder-Übertragung wird über Website 1-VoIP-Routing Richtlinie und-Ausstieg über das Website 1-Gateway weitergeleitet</span><span class="sxs-lookup"><span data-stu-id="23649-200">Call forward or transfer is routed through site 1 voice routing policy and egress via Site 1 Gateway</span></span></p></td>
<td><p><span data-ttu-id="23649-201">Anrufweiterleitung oder-Übertragung wird über die Website 2-VoIP-Routing Richtlinie und den Ausstieg über das Standort-2-Gateway weitergeleitet</span><span class="sxs-lookup"><span data-stu-id="23649-201">Call forward or transfer is routed through site 2 voice routing policy and egress via Site 2 Gateway</span></span></p></td>
<td><p><span data-ttu-id="23649-202">Anrufweiterleitung oder-Übertragung wird über die lync-Benutzer VoIP-Richtlinie und den Ausstieg über ein Gateway weitergeleitet, das für standortbasiertes Routing nicht aktiviert ist (sofern verfügbar)</span><span class="sxs-lookup"><span data-stu-id="23649-202">Call forward or transfer is routed through the Lync user voice policy and egress via a gateway not enabled for location-based routing (if available)</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="simultaneous-ringing"></a><span data-ttu-id="23649-203">Paralleles Anrufen</span><span class="sxs-lookup"><span data-stu-id="23649-203">Simultaneous ringing</span></span>

<span data-ttu-id="23649-204">Sobald standortbasiertes Routing in der Beispieltopologie konfiguriert ist, werden die folgenden Interaktionen erzwungen.</span><span class="sxs-lookup"><span data-stu-id="23649-204">Once location-based routing is configured in the sample topology, the following interactions are enforced.</span></span>

<span data-ttu-id="23649-205">In der folgenden Tabelle wird gezeigt, ob Location-Based Routing das gleichzeitige Klingeln für verschiedene lync-Benutzer ermöglicht (also lync-Benutzer 2, lync-Benutzer 4 usw.).</span><span class="sxs-lookup"><span data-stu-id="23649-205">The following table illustrates whether Location-Based Routing allows simultaneous ringing for different Lync users (i.e. Lync user 2, Lync user 4, etc).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23649-206">Eingehendes PSTN-Anruf Ziel</span><span class="sxs-lookup"><span data-stu-id="23649-206">Incoming PSTN call target</span></span></th>
<th><span data-ttu-id="23649-207">Lync-Benutzer 2</span><span class="sxs-lookup"><span data-stu-id="23649-207">Lync user 2</span></span></th>
<th><span data-ttu-id="23649-208">Lync-Benutzer 4</span><span class="sxs-lookup"><span data-stu-id="23649-208">Lync user 4</span></span></th>
<th><span data-ttu-id="23649-209">Lync-Benutzer auf der Netzwerk Website für Location-Based Routing nicht aktiviert</span><span class="sxs-lookup"><span data-stu-id="23649-209">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23649-210">Lync-Benutzer 1</span><span class="sxs-lookup"><span data-stu-id="23649-210">Lync user 1</span></span></p></td>
<td><p><span data-ttu-id="23649-211">Gleichzeitiges Klingeln ist zulässig</span><span class="sxs-lookup"><span data-stu-id="23649-211">Simultaneous ring is allowed</span></span></p></td>
<td><p><span data-ttu-id="23649-212">Gleichzeitiges Klingeln ist nicht zulässig</span><span class="sxs-lookup"><span data-stu-id="23649-212">Simultaneous ring is not allowed</span></span></p></td>
<td><p><span data-ttu-id="23649-213">Gleichzeitiges Klingeln ist nicht zulässig</span><span class="sxs-lookup"><span data-stu-id="23649-213">Simultaneous ring is not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="23649-214">In der folgenden Tabelle wird gezeigt, ob Location-Based Routing das gleichzeitige Klingeln an einen PSTN-Endpunkt von unterschiedlichen lync-Benutzern ermöglicht (also lync-Benutzer 2, lync-Benutzer 4 usw.).</span><span class="sxs-lookup"><span data-stu-id="23649-214">The following table illustrates whether Location-Based Routing allows simultaneous ringing to a PSTN endpoint from different Lync users (i.e. Lync user 2, Lync user 4, etc).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23649-215">Ziel für paralleles Anrufen</span><span class="sxs-lookup"><span data-stu-id="23649-215">Simultaneous ring target</span></span></th>
<th><span data-ttu-id="23649-216">Lync-Benutzer 2</span><span class="sxs-lookup"><span data-stu-id="23649-216">Lync user 2</span></span></th>
<th><span data-ttu-id="23649-217">Lync-Benutzer 4</span><span class="sxs-lookup"><span data-stu-id="23649-217">Lync user 4</span></span></th>
<th><span data-ttu-id="23649-218">Lync-Benutzer auf der Netzwerk Website für Location-Based Routing nicht aktiviert</span><span class="sxs-lookup"><span data-stu-id="23649-218">Lync user in network site not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23649-219">Lync-Benutzer 1-Mobiltelefon (PSTN-Endpunkt)</span><span class="sxs-lookup"><span data-stu-id="23649-219">Lync user 1 mobile phone (PSTN endpoint)</span></span></p></td>
<td><p><span data-ttu-id="23649-220">Anrufweiterleitung über die VoIP-Routing Richtlinie des Netzwerkstandorts und den Ausstieg über das Website 1-Gateway</span><span class="sxs-lookup"><span data-stu-id="23649-220">Call routed through network site 1’s voice routing policy and egress via site 1 gateway</span></span></p></td>
<td><p><span data-ttu-id="23649-221">Anrufweiterleitung über die VoIP-Routing Richtlinie des Netzwerkstandorts und den Ausstieg über das Gateway des Standorts 2</span><span class="sxs-lookup"><span data-stu-id="23649-221">Call routed through network site 2’s voice routing policy and egress via site 2 gateway</span></span></p></td>
<td><p><span data-ttu-id="23649-222">Anrufweiterleitung über die Richtlinie für Anrufer-VoIP und wird über ein PSTN-Gateway ablaufen, das für Location-Based Routing nicht aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="23649-222">Call routed through the caller voice policy and will egress via a PSTN gateway not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="23649-223">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23649-223">See Also</span></span>


[<span data-ttu-id="23649-224">Planung des standortbasierten Routings in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="23649-224">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="23649-225"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="23649-225"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

