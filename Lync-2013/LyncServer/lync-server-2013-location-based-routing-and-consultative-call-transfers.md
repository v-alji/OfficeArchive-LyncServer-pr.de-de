---
title: 'Lync Server 2013: Location-Based Routing und beratende Anruf Übertragungen'
description: 'Lync Server 2013: Location-Based Routing-und beratenden Anruf Übertragungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Location-Based Routing and consultative call transfers
ms:assetid: b12460c2-36c8-481f-b867-fe10dc1c0bdf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362836(v=OCS.15)
ms:contentKeyID: 56335089
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d07cf6a33ff4d6ad57f8913a798fac3bc393a00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426560"
---
# <a name="location-based-routing-and-consultative-call-transfers-in-lync-server-2013"></a><span data-ttu-id="940d3-103">Location-Based von Routing-und beratenden Anruf Übertragungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="940d3-103">Location-Based Routing and consultative call transfers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="940d3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="940d3-104">

<span> </span></span></span>

<span data-ttu-id="940d3-105">_**Letztes Änderungsdatum des Themas:** 2013-07-31_</span><span class="sxs-lookup"><span data-stu-id="940d3-105">_**Topic Last Modified:** 2013-07-31_</span></span>

<span data-ttu-id="940d3-106">Neben der Erzwingung Location-Based Routings zu lync-Besprechungen erzwingt die Location-Based Routing Konferenz Anwendung Location-Based Routing Einschränkungen bei Beratenden Anruf Übertragungen, die an PSTN-Endpunkte abtreten.</span><span class="sxs-lookup"><span data-stu-id="940d3-106">In addition to enforcing Location-Based Routing to Lync meetings, the Location-Based Routing Conferencing application enforces Location-Based Routing restrictions on consultative call transfers that egress to PSTN endpoints.</span></span> <span data-ttu-id="940d3-107">Bei einer beratenden Anrufübertragung handelt es sich um einen Anruf zwischen zwei Parteien, bei dem eine der Parteien den Anruf an einen neuen Nutzer übermittelt.</span><span class="sxs-lookup"><span data-stu-id="940d3-107">A consultative call transfer is a call established between two parties where one of the parties transfers the call to a new user.</span></span> <span data-ttu-id="940d3-108">Ein PSTN-Endpunkt ruft beispielsweise Benutzer a (lync-aufgerufener) auf.</span><span class="sxs-lookup"><span data-stu-id="940d3-108">For example, a PSTN endpoint calls user A (Lync callee).</span></span> <span data-ttu-id="940d3-109">Benutzer A bestimmt, dass der PSTN-Benutzer an Benutzer B weitergeleitet werden soll (lync-Benutzer).</span><span class="sxs-lookup"><span data-stu-id="940d3-109">User A determines the PSTN user should be forwarded to user B (Lync user).</span></span> <span data-ttu-id="940d3-110">Der Benutzer A platziert den Anruf mit dem PSTN-Benutzer in Wartestellung und ruft Benutzer b an, der sich mit dem PSTN-Benutzer unterhalten möchte.</span><span class="sxs-lookup"><span data-stu-id="940d3-110">User A places the call with the PSTN user on hold, and calls user B. User B agrees to talk to the PSTN user.</span></span> <span data-ttu-id="940d3-111">Benutzer a übergibt den Anruf in Wartestellung an Benutzer B.</span><span class="sxs-lookup"><span data-stu-id="940d3-111">User A transfers the call on-hold to user B.</span></span>

<span data-ttu-id="940d3-112">**Anruffluss bei einer Anrufdurchstellung mit Ankündigung**</span><span class="sxs-lookup"><span data-stu-id="940d3-112">**Consultative call transfer call flow**</span></span>

<span data-ttu-id="940d3-113">![Standortbasiertes Routing für Konferenzen (Diagramm)](images/Dn362836.e4d43d6f-23d2-49c9-b12b-15248a743f92(OCS.15).jpg "Standortbasiertes Routing für Konferenzen (Diagramm)")</span><span class="sxs-lookup"><span data-stu-id="940d3-113">![Location-based routing for conferencing diagram](images/Dn362836.e4d43d6f-23d2-49c9-b12b-15248a743f92(OCS.15).jpg "Location-based routing for conferencing diagram")</span></span>

<span data-ttu-id="940d3-114">Wenn ein für Location-Based Routing aktivierter Benutzer eine beratende Anrufübertragung eines PSTN-Endpunkts initiiert (wie in der vorhergehenden Abbildung dargestellt), werden zwei aktive Anrufe, ein Anruf zwischen dem PSTN-Benutzer und dem lync-Benutzer a und der andere zwischen lync-Benutzer a und lync-Benutzer B erstellt. das folgende Verhalten wird von der Location-Based Routing Konferenz Anwendung erzwungen:</span><span class="sxs-lookup"><span data-stu-id="940d3-114">When a user enabled for Location-Based Routing initiates a consultative call transfer of a PSTN endpoint (as shown in the preceding figure), this creates two active calls, one call between the PSTN user and Lync user A, and the other between Lync user A and Lync user B. the following behavior is enforced by the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="940d3-115">Wenn das SIP Trunk-Routing des PSTN-Anrufs autorisiert ist, den PSTN-Anruf an die Netzwerk Website weiterzuleiten, auf der sich der lync-Benutzer B (also das Übertragungsziel) befindet, wird die Anrufübertragung zugelassen. Andernfalls wird die Übertragung von beratenden anrufen blockiert.</span><span class="sxs-lookup"><span data-stu-id="940d3-115">If the SIP trunk routing the PSTN call is authorized to re-route the PSTN call to the network site where Lync user B (i.e. transfer target) is located,, then the call transfer will be allowed; otherwise, the consultative call transfer will be blocked.</span></span> <span data-ttu-id="940d3-116">Diese Autorisierung erfolgt auf der Grundlage des Standorts der übertragenen Partei, die sich am gleichen Netzwerkstandort wie der SIP-Stamm befindet, der den aktiven Anruf an den PSTN-Endpunkt weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="940d3-116">This authorization is performed based on the transferred party’s location being in the same network site as the SIP trunk that is routing the active call to the PSTN endpoint.</span></span>

  - <span data-ttu-id="940d3-117">Wenn der SIP-Trunk-Routing der eingehende PSTN-Anruf nicht autorisiert ist, Anrufe an die Netzwerk Website weiterzuleiten, auf der sich die übertragene Partei (lync-Benutzer B) befindet oder sich die übertragene Partei in einer unbekannten Netzwerk Website befindet, wird die beratende Anrufübertragung an den PSTN-Endpunkt (dh Anrufübergabe Ziel) blockiert.</span><span class="sxs-lookup"><span data-stu-id="940d3-117">If the SIP trunk routing the inbound PSTN call is not authorized to route calls to the network site where the transferred party (Lync user B) is located or the transferred party is located in an unknown network site, then the consultative call transfer to the PSTN endpoint (i.e. call transfer target) will be blocked.</span></span>

<span data-ttu-id="940d3-118">In der folgenden Tabelle wird beschrieben, wie Location-Based Routing Einschränkungen von der Location-Based Routing Konferenz Anwendung für beratende Anruf Übertragungen angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="940d3-118">The following table describes how Location-Based Routing restrictions are applied by the Location-Based Routing Conferencing application for consultative call transfers.</span></span> <span data-ttu-id="940d3-119">Zwar sind Nebenstellenanlagenendgeräte nicht direkt einem Netzwerkstandort zugewiesen, aber die SIP-Vermittlungsleitung, an die die jeweilige Nebenstellenanlage angeschlossen ist, kann einem Netzwerkstandort zugewiesen sein.</span><span class="sxs-lookup"><span data-stu-id="940d3-119">Although PBX endpoints are not directly associated with a network site, the SIP trunk the PBX is connected to can be assigned a network site.</span></span> <span data-ttu-id="940d3-120">Daher kann ein Nebenstellenanlagenendgerät indirekt einem Netzwerkstandort zugewiesen sein.</span><span class="sxs-lookup"><span data-stu-id="940d3-120">Therefore, the PBX endpoint can be indirectly associated with a network site.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="940d3-121">Netzwerkstandort des Teilnehmers, dessen Anruf durchgestellt wird</span><span class="sxs-lookup"><span data-stu-id="940d3-121">Network site of call transferred party</span></span></p></td>
<td><p><span data-ttu-id="940d3-122">Netzwerk Website des Anruf Weiterleitungs Ziels</span><span class="sxs-lookup"><span data-stu-id="940d3-122">Network site of call transfer target</span></span></p></td>
<td><p><span data-ttu-id="940d3-123">Verhalten</span><span class="sxs-lookup"><span data-stu-id="940d3-123">Behavior</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940d3-124">Endpunkt im öffentlichen Telefonnetz</span><span class="sxs-lookup"><span data-stu-id="940d3-124">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="940d3-125">Lync-Benutzer an derselben Netzwerk Website (also Website 1)</span><span class="sxs-lookup"><span data-stu-id="940d3-125">Lync user in the same network site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="940d3-126">Eine beratende Übertragung ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="940d3-126">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940d3-127">Endpunkt im öffentlichen Telefonnetz</span><span class="sxs-lookup"><span data-stu-id="940d3-127">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="940d3-128">Lync-Benutzer an verschiedenen Netzwerkstandorten (also Standort 2)</span><span class="sxs-lookup"><span data-stu-id="940d3-128">Lync user in different network sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="940d3-129">Eine beratende Übertragung ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="940d3-129">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940d3-130">Endpunkt im öffentlichen Telefonnetz</span><span class="sxs-lookup"><span data-stu-id="940d3-130">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="940d3-131">Lync-Benutzer in einer unbekannten Netzwerk Website</span><span class="sxs-lookup"><span data-stu-id="940d3-131">Lync user in an unknown network site</span></span></p></td>
<td><p><span data-ttu-id="940d3-132">Eine beratende Übertragung ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="940d3-132">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940d3-133">Endpunkt im öffentlichen Telefonnetz</span><span class="sxs-lookup"><span data-stu-id="940d3-133">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="940d3-134">Federated lync-Benutzer</span><span class="sxs-lookup"><span data-stu-id="940d3-134">Federated Lync user</span></span></p></td>
<td><p><span data-ttu-id="940d3-135">Eine beratende Übertragung ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="940d3-135">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940d3-136">Endpunkt im öffentlichen Telefonnetz</span><span class="sxs-lookup"><span data-stu-id="940d3-136">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="940d3-137">PBX-Endpunkt am gleichen Standort (also Standort 1)</span><span class="sxs-lookup"><span data-stu-id="940d3-137">PBX endpoint in the same site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="940d3-138">Eine beratende Übertragung ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="940d3-138">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940d3-139">Endpunkt im öffentlichen Telefonnetz</span><span class="sxs-lookup"><span data-stu-id="940d3-139">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="940d3-140">PBX-Endpunkt an verschiedenen Standorten (also Standort 2)</span><span class="sxs-lookup"><span data-stu-id="940d3-140">PBX endpoint in a different sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="940d3-141">Eine beratende Übertragung ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="940d3-141">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940d3-142">PBX-Endpunkt am gleichen Standort (also Standort 1)</span><span class="sxs-lookup"><span data-stu-id="940d3-142">PBX endpoint in the same site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="940d3-143">Endpunkt im öffentlichen Telefonnetz</span><span class="sxs-lookup"><span data-stu-id="940d3-143">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="940d3-144">Eine beratende Übertragung ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="940d3-144">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940d3-145">PBX-Endpunkt an einer anderen Website (also Standort 2)</span><span class="sxs-lookup"><span data-stu-id="940d3-145">PBX endpoint in a different site (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="940d3-146">Endpunkt im öffentlichen Telefonnetz</span><span class="sxs-lookup"><span data-stu-id="940d3-146">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="940d3-147">Eine beratende Übertragung ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="940d3-147">Consultative transfer will be disallowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940d3-148">PBX-Endpunkt auf einer beliebigen Website</span><span class="sxs-lookup"><span data-stu-id="940d3-148">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="940d3-149">Lync-Benutzer an derselben Netzwerk Website (also Website 1)</span><span class="sxs-lookup"><span data-stu-id="940d3-149">Lync user in the same network site (i.e. site 1)</span></span></p></td>
<td><p><span data-ttu-id="940d3-150">Eine beratende Übertragung ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="940d3-150">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940d3-151">PBX-Endpunkt auf einer beliebigen Website</span><span class="sxs-lookup"><span data-stu-id="940d3-151">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="940d3-152">Lync-Benutzer an verschiedenen Netzwerkstandorten (also Standort 2)</span><span class="sxs-lookup"><span data-stu-id="940d3-152">Lync user in different network sites (i.e. site 2)</span></span></p></td>
<td><p><span data-ttu-id="940d3-153">Eine beratende Übertragung ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="940d3-153">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="940d3-154">PBX-Endpunkt auf einer beliebigen Website</span><span class="sxs-lookup"><span data-stu-id="940d3-154">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="940d3-155">Lync-Benutzer in einer unbekannten Netzwerk Website</span><span class="sxs-lookup"><span data-stu-id="940d3-155">Lync user in an unknown network site</span></span></p></td>
<td><p><span data-ttu-id="940d3-156">Eine beratende Übertragung ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="940d3-156">Consultative transfer will be allowed</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="940d3-157">PBX-Endpunkt auf einer beliebigen Website</span><span class="sxs-lookup"><span data-stu-id="940d3-157">PBX endpoint in any site</span></span></p></td>
<td><p><span data-ttu-id="940d3-158">Federated lync-Benutzer</span><span class="sxs-lookup"><span data-stu-id="940d3-158">Federated Lync user</span></span></p></td>
<td><p><span data-ttu-id="940d3-159">Eine beratende Übertragung ist zulässig.</span><span class="sxs-lookup"><span data-stu-id="940d3-159">Consultative transfer will be allowed</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="940d3-160">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="940d3-160">


</div>

<span> </span>

</div>

</div>

</span></span></div>

