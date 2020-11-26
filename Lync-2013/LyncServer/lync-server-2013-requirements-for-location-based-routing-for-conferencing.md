---
title: 'Lync Server 2013: Anforderungen für Location-Based Routing für Konferenzen'
description: 'Lync Server 2013: Anforderungen für Location-Based Routing für Konferenzen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Requirements for Location-Based Routing for conferencing
ms:assetid: 766d9286-2c34-4faf-bb3e-f0ca478a70cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362806(v=OCS.15)
ms:contentKeyID: 56335085
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbaa1af2690c3148d2ecfb173b13be288a21d80f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442663"
---
# <a name="requirements-for-location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="ae24a-103">Voraussetzungen für Location-Based Routing für Konferenzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ae24a-103">Requirements for Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ae24a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ae24a-104">

<span> </span></span></span>

<span data-ttu-id="ae24a-105">_**Letztes Änderungsdatum des Themas:** 2013-07-19_</span><span class="sxs-lookup"><span data-stu-id="ae24a-105">_**Topic Last Modified:** 2013-07-19_</span></span>

<span data-ttu-id="ae24a-106">Im folgenden werden die Anforderungen für die Installation und Konfiguration der Location-Based Routing Konferenz Anwendung benötigt:</span><span class="sxs-lookup"><span data-stu-id="ae24a-106">The following are the requirements needed for the installation and configuration of the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="ae24a-107">Das kumulative Update 2 von lync Server 2013 muss auf allen Servern oder Pools in Ihrer Topologie bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="ae24a-107">Lync Server 2013 Cumulative Update 2 must be deployed on all servers or pools in your topology.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ae24a-108">Wenn auf einem lync-Server oder-Pool in Ihrer Topologie lync Server 2013 Kumulatives Update 2 oder höher nicht installiert ist, kann die Erzwingung Location-Based Routings von lync-Besprechungen nicht garantiert werden.</span><span class="sxs-lookup"><span data-stu-id="ae24a-108">If a Lync server or pool in your topology does not have Lync Server 2013 Cumulative Update 2 or higher installed, then enforcement of Location-Based Routing of Lync meetings cannot be guaranteed.</span></span>



</div>

  - <span data-ttu-id="ae24a-109">Lync Server 2013 Location-Based-Routing ist eine Voraussetzung für Location-Based Routing Konferenz Anwendung.</span><span class="sxs-lookup"><span data-stu-id="ae24a-109">Lync Server 2013 Location-Based Routing is a pre-requisite for Location-Based Routing Conferencing application.</span></span> <span data-ttu-id="ae24a-110">Weitere Informationen zum Konfigurieren von lync Server 2013 Location-Based-Routing finden Sie unter [Konfigurieren von Location-Based-Routing](lync-server-2013-configuring-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="ae24a-110">For further information on configuring Lync Server 2013 Location-Based Routing, please refer to [Configuring Location-Based Routing](lync-server-2013-configuring-location-based-routing.md).</span></span>

  - <span data-ttu-id="ae24a-111">Die Anforderungen für Location-Based Routing Konferenz Anwendung entsprechen den Anforderungen für lync Server 2013 Location-Based-Routing.</span><span class="sxs-lookup"><span data-stu-id="ae24a-111">Requirements of Location-Based Routing Conferencing application are the same as the requirements for Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="ae24a-112">Weitere Informationen finden Sie unter [Planen von Location-Based-Routing](lync-server-2013-planning-for-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="ae24a-112">For more information, please refer to [Planning for Location-Based Routing](lync-server-2013-planning-for-location-based-routing.md).</span></span>

<div>

## <a name="supported-servers"></a><span data-ttu-id="ae24a-113">Unterstützte Server</span><span class="sxs-lookup"><span data-stu-id="ae24a-113">Supported Servers</span></span>

<span data-ttu-id="ae24a-114">Die Location-Based Routing Konferenz Anwendung erfordert, dass das kumulative Update 2 von lync Server 2013 auf allen Front-End Pools und Standard Edition-Servern in Ihrer Topologie bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="ae24a-114">The Location-Based Routing Conferencing application requires that Lync Server 2013 Cumulative Update 2 is deployed on all Front-End pools and Standard Edition Servers in your topology.</span></span> <span data-ttu-id="ae24a-115">Wenn das kumulative Update 2 von lync Server 2013 auf einigen lync-Servern in Ihrer Topologie nicht installiert ist, können Location-Based Routing Einschränkungen nicht vollständig in lync-Besprechungen und beratenden Anruf Übertragungen erzwungen werden.</span><span class="sxs-lookup"><span data-stu-id="ae24a-115">If Lync Server 2013 Cumulative Update 2 is not installed on some Lync Servers in your topology, Location-Based Routing restrictions cannot be fully enforced on Lync meetings and consultative call transfers.</span></span>

<span data-ttu-id="ae24a-116">In der folgenden Tabelle sind die Kombinationen aus Serverrollen und Versionen aufgeführt, die Location-Based Routing unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ae24a-116">The following table identifies the combination of server roles and versions that support Location-Based Routing.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ae24a-117">Version des Front-End Pools</span><span class="sxs-lookup"><span data-stu-id="ae24a-117">Front-End Pool version</span></span></p></td>
<td><p><span data-ttu-id="ae24a-118">Mediation Server-Version</span><span class="sxs-lookup"><span data-stu-id="ae24a-118">Mediation Server version</span></span></p></td>
<td><p><span data-ttu-id="ae24a-119">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ae24a-119">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae24a-120">Lync Server 2013 Kumulatives Update 2</span><span class="sxs-lookup"><span data-stu-id="ae24a-120">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="ae24a-121">Lync Server 2013 Kumulatives Update 2</span><span class="sxs-lookup"><span data-stu-id="ae24a-121">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="ae24a-122">Ja</span><span class="sxs-lookup"><span data-stu-id="ae24a-122">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae24a-123">Lync Server 2013 Kumulatives Update 2</span><span class="sxs-lookup"><span data-stu-id="ae24a-123">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="ae24a-124">Lync Server 2013 Kumulatives Update 1</span><span class="sxs-lookup"><span data-stu-id="ae24a-124">Lync Server 2013 Cumulative Update 1</span></span></p></td>
<td><p><span data-ttu-id="ae24a-125">Nein</span><span class="sxs-lookup"><span data-stu-id="ae24a-125">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae24a-126">Lync Server 2013 Kumulatives Update 2</span><span class="sxs-lookup"><span data-stu-id="ae24a-126">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="ae24a-127">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="ae24a-127">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="ae24a-128">Nein</span><span class="sxs-lookup"><span data-stu-id="ae24a-128">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae24a-129">Lync Server 2013 Kumulatives Update 2</span><span class="sxs-lookup"><span data-stu-id="ae24a-129">Lync Server 2013 Cumulative Update 2</span></span></p></td>
<td><p><span data-ttu-id="ae24a-130">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="ae24a-130">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="ae24a-131">Nein</span><span class="sxs-lookup"><span data-stu-id="ae24a-131">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae24a-132">Lync Server 2013 Kumulatives Update 1</span><span class="sxs-lookup"><span data-stu-id="ae24a-132">Lync Server 2013 Cumulative Update 1</span></span></p></td>
<td><p><span data-ttu-id="ae24a-133">Beliebig</span><span class="sxs-lookup"><span data-stu-id="ae24a-133">Any</span></span></p></td>
<td><p><span data-ttu-id="ae24a-134">Nein</span><span class="sxs-lookup"><span data-stu-id="ae24a-134">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ae24a-135">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="ae24a-135">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="ae24a-136">Beliebig</span><span class="sxs-lookup"><span data-stu-id="ae24a-136">Any</span></span></p></td>
<td><p><span data-ttu-id="ae24a-137">Nein</span><span class="sxs-lookup"><span data-stu-id="ae24a-137">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ae24a-138">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="ae24a-138">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="ae24a-139">Beliebig</span><span class="sxs-lookup"><span data-stu-id="ae24a-139">Any</span></span></p></td>
<td><p><span data-ttu-id="ae24a-140">Nein</span><span class="sxs-lookup"><span data-stu-id="ae24a-140">No</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="supported-clients"></a><span data-ttu-id="ae24a-141">Unterstützte Clients</span><span class="sxs-lookup"><span data-stu-id="ae24a-141">Supported Clients</span></span>

<span data-ttu-id="ae24a-142">Die lync-Clients, die Location-Based Routing von lync-Besprechungen unterstützen, sind dieselben Clients, die lync Server 2013 Location-Based Routing unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ae24a-142">The Lync clients that support Location-Based Routing of Lync meetings are the same clients that support Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="ae24a-143">Weitere Informationen finden Sie [unter Support für Client und Server für Location-Based Routing](lync-server-2013-client-and-server-support-for-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="ae24a-143">For more information, please refer to [Client and Server Support for Location-Based Routing](lync-server-2013-client-and-server-support-for-location-based-routing.md).</span></span>

</div>

<div>

## <a name="mediation-server-requirements-for-consultative-call-transfers"></a><span data-ttu-id="ae24a-144">Vermittlungs Server Anforderungen für beratende Anruf Übertragungen</span><span class="sxs-lookup"><span data-stu-id="ae24a-144">Mediation Server Requirements for Consultative Call Transfers</span></span>

<span data-ttu-id="ae24a-145">Für die Location-Based-Routing Konferenz Anwendung müssen eigenständige Vermittlungsserver bereitgestellt werden, um Location-Based Routing Einschränkungen bei Beratenden Anruf Übertragungen durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="ae24a-145">The Location-Based Routing Conferencing application requires deploying stand-alone Mediation Servers in order to enforce Location-Based Routing restrictions on consultative call transfers.</span></span>

<span data-ttu-id="ae24a-146">Um Location-Based Routing von beratenden Anruf Übertragungen durchzusetzen, muss der Vermittlungsserver nur einem Vermittlungsserver-Peer (also einer Telefonanlage, einem SIP-Gateway usw.) in netzwerkregionen zugeordnet sein, in denen Location-Based Routing erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ae24a-146">To enforce Location-Based Routing of consultative call transfers, the Mediation Server must be associated with only one Mediation Server peer (i.e. PBX, SIP gateway, etc) in network regions where Location-Based Routing is required.</span></span> <span data-ttu-id="ae24a-147">Wenn weitere Vermittlungsserver-Peers im gleichen Netzwerkbereich bereitgestellt werden, muss der Vermittlungsserver-Peer einem anderen Vermittlungsserver zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="ae24a-147">If additional Mediation Server peers are deployed in the same network region, the Mediation Server peer must be associated with a different Mediation Server .</span></span> <span data-ttu-id="ae24a-148">Diese Anforderung wird wie folgt erläutert:</span><span class="sxs-lookup"><span data-stu-id="ae24a-148">This Requirement is detailed as follows:</span></span>

  - <span data-ttu-id="ae24a-149">Einzelner Vermittlungsserver pro mehrere Vermittlungsserver-Peers, wenn eine beratende Anrufübertragung an einen Vermittlungsserver-Peer über einen Vermittlungsserver weitergeleitet wird, der mit mehreren SIP-Stämmen für mehrere Peers konfiguriert ist (d. h. PBX-Anlagen und Gateways) wird die Anrufumleitung blockiert, um eine PSTN-Maut Umgehung zu verhindern, wenn die Anrufumleitung über einige SIP-Stämme zugelassen, aber über andere SIP-Stämme nicht zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="ae24a-149">Single Mediation Server per multiple Mediation Server peers When a consultative call transfer is routed to a Mediation Server peer through a Mediation Server that’s configured with multiple SIP trunks to multiple peers (i.e. PBXs and gateways), the consultative call transfer is blocked to prevent PSTN toll bypass if the consultative call transfer is permitted through some SIP trunks but disallowed through other SIP trunks.</span></span>
    
    <span data-ttu-id="ae24a-150">Wenn beispielsweise ein einzelner Vermittlungsserver einen Vermittlungsserver-Peer des PSTN-Gateways und einen PBX-Vermittlungsserver-Peer bedient, wird das folgende Verhalten beobachtet:</span><span class="sxs-lookup"><span data-stu-id="ae24a-150">For example, in the case of a single Mediation Server servicing a PSTN Gateway Mediation Server Peer and a PBX Mediation Server Peer, the following behavior will be observed:</span></span>
    
      - <span data-ttu-id="ae24a-151">Wenn ein lync-Benutzer von einer bestimmten Website (also Website 1) versucht, einen Anruf mit einem PSTN-Endpunkt an einen lync-Benutzer von einer anderen Website (also Standort 2) über eine beratende Übertragung zu übertragen, wird der Anruf nicht zugelassen, um die PSTN-Maut Umgehung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="ae24a-151">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PSTN endpoint to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed to prevent PSTN toll bypass.</span></span>
    
      - <span data-ttu-id="ae24a-152">Wenn ein lync-Benutzer von einer bestimmten Website (also Website 1) versucht, einen Anruf mit einem PBX-Endpunkt am gleichen Standort (Standort 1) an einen lync-Benutzer von einer anderen Website (d. h. Standort 2) über eine beratende Übertragung zu übertragen, wird der Anruf nicht zugelassen, auch wenn er nicht in potenzieller Umgehung des PSTN-Mautbereichs fällt.</span><span class="sxs-lookup"><span data-stu-id="ae24a-152">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PBX endpoint in the same site (site 1) to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed even if it doesn’t incur in potential PSTN toll bypassing.</span></span>

  - <span data-ttu-id="ae24a-153">Separate Vermittlungsserver pro Vermittlungsserver-Peer</span><span class="sxs-lookup"><span data-stu-id="ae24a-153">Separate Mediation Servers per Mediation Server peer</span></span>
    
    <span data-ttu-id="ae24a-154">Wenn eine beratende Übertragung auf einen Vermittlungsserver-Peer ausgerichtet ist, wird die beratende Übertragung mit dem einzelnen Mediation Server-Peer bewertet, der vom Vermittlungsserver gewartet wird.</span><span class="sxs-lookup"><span data-stu-id="ae24a-154">When a consultative transfer is targeted at a Mediation Server Peer, the consultative transfer will be evaluated against the single Mediation Server Peer serviced by the Mediation Server.</span></span> <span data-ttu-id="ae24a-155">Der Anruf wird aufgrund seines Potenzials, in der PSTN-Maut Umgehung zu entstehen, ungeachtet aller anderen Vermittlungsserver-Peers in der Website, die von separaten Vermittlungsservern gewartet werden, nicht zugelassen oder zulässig.</span><span class="sxs-lookup"><span data-stu-id="ae24a-155">The call will be disallowed or allowed based in its potential to incur in PSTN toll bypass regardless of all other Mediations Server Peers in the site as they’re serviced by separate Mediation Servers.</span></span>
    
    <span data-ttu-id="ae24a-156">Bei einem separaten Vermittlungsserver, der einen Vermittlungsserver-Peer des PSTN-Gateways und einen PBX-Vermittlungsserver-Peer bedient, wird beispielsweise folgendes Verhalten beobachtet:</span><span class="sxs-lookup"><span data-stu-id="ae24a-156">For example, in the case of a separate Mediation Servers servicing a PSTN Gateway Mediation Server Peer and a PBX Mediation Server Peer, the following behavior will be observed:</span></span>
    
      - <span data-ttu-id="ae24a-157">Wenn ein lync-Benutzer von einer bestimmten Website (also Website 1) versucht, einen Anruf mit einem PSTN-Endpunkt an einen lync-Benutzer von einer anderen Website (also Standort 2) über eine beratende Übertragung zu übertragen, wird der Anruf nicht zugelassen, um die PSTN-Maut Umgehung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="ae24a-157">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PSTN endpoint to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be disallowed to prevent PSTN toll bypass.</span></span>
    
      - <span data-ttu-id="ae24a-158">Wenn ein lync-Benutzer von einer bestimmten Website (also Website 1) versucht, einen Anruf mit einem PBX-Endpunkt am gleichen Standort (Standort 1) an einen lync-Benutzer von einer anderen Website (also Standort 2) über eine beratende Übertragung zu übertragen, wird der Anruf zugelassen, da er nicht in potenzielle Umgehung von PSTN-Gebühren fällt.</span><span class="sxs-lookup"><span data-stu-id="ae24a-158">When a Lync user from a given site (i.e. site 1) attempts to transfer a call with a PBX endpoint in the same site (site 1) to a Lync user from a different site (i.e. site 2) via consultative transfer, the call will be allowed as it doesn’t incur in potential PSTN toll bypassing.</span></span>

</div>

<div>

## <a name="capabilities-not-supported-by-the-location-based-routing-conferencing-application"></a><span data-ttu-id="ae24a-159">Funktionen, die von der Location-Based Routing Konferenz Anwendung nicht unterstützt werden</span><span class="sxs-lookup"><span data-stu-id="ae24a-159">Capabilities Not Supported by the Location-Based Routing Conferencing Application</span></span>

<span data-ttu-id="ae24a-160">Die folgenden Funktionen werden von der Location-Based Routing Konferenz Anwendung nicht unterstützt:</span><span class="sxs-lookup"><span data-stu-id="ae24a-160">The following capabilities are not supported by the Location-Based Routing Conferencing application:</span></span>

  - <span data-ttu-id="ae24a-161">Einwahlkonferenzen.</span><span class="sxs-lookup"><span data-stu-id="ae24a-161">Dial-in conferencing.</span></span> <span data-ttu-id="ae24a-162">Location-Based-Routing kann für Einwahlkonferenzen nicht erzwungen werden.</span><span class="sxs-lookup"><span data-stu-id="ae24a-162">Location-Based Routing cannot be enforced for Dial-in conferencing.</span></span> <span data-ttu-id="ae24a-163">Alle Einwahl Anforderungen an eine bestimmte Konferenz werden nicht durch Location-Based Routing eingeschränkt, auch wenn der Konferenzorganisator ein lync-Benutzer ist, der für Location-Based Routing aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="ae24a-163">Any dial-in request to a given conference will not be restricted by Location-Based Routing even if the conference organizer is a Lync user enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="ae24a-164">Es wird empfohlen, keine Konferenz Zugriffsnummern in Regionen bereitzustellen, in denen Location-Based Routing Einschränkungen erzwungen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="ae24a-164">It’s recommended not to provision conferencing access numbers in regions where Location-Based Routing restrictions need to be enforced.</span></span>

<span data-ttu-id="ae24a-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ae24a-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

