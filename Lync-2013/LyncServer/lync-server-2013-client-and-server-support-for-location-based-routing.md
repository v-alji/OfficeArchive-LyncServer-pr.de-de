---
title: 'Lync Server 2013: Client- und Serverunterstützung für standortbasiertes Routing'
description: 'Lync Server 2013: Client-und Server Unterstützung für Location-Based Routing'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Client and server support for Location-Based Routing
ms:assetid: 26c2ca3d-026d-4dd7-94fa-15ebb4406953
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994024(v=OCS.15)
ms:contentKeyID: 51803933
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20dca7444f58ee62dbc36edbb7d9e1c976a97807
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434900"
---
# <a name="client-and-server-support-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="d56bc-103">Client- und Serverunterstützung für standortbasiertes Routing in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d56bc-103">Client and server support for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d56bc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d56bc-104">

<span> </span></span></span>

<span data-ttu-id="d56bc-105">_**Letztes Änderungsdatum des Themas:** 2013-06-18_</span><span class="sxs-lookup"><span data-stu-id="d56bc-105">_**Topic Last Modified:** 2013-06-18_</span></span>

<span data-ttu-id="d56bc-106">Location-Based Routing wird von lync Server erzwungen.</span><span class="sxs-lookup"><span data-stu-id="d56bc-106">Location-Based Routing is enforced by Lync Server.</span></span> <span data-ttu-id="d56bc-107">Lync Server kann die Netzwerk Websites identifizieren, über die Benutzer im Unternehmensnetzwerk eine Verbindung herstellen.</span><span class="sxs-lookup"><span data-stu-id="d56bc-107">Lync Server can identify the network sites where users are connecting from within the corporate network.</span></span> <span data-ttu-id="d56bc-108">Da sich Remotebenutzer außerhalb des Unternehmensnetzwerks befinden, werden deren Positionen als unbekannt angesehen.</span><span class="sxs-lookup"><span data-stu-id="d56bc-108">Since remote users are outside the corporate network, their location is considered to be unknown.</span></span>

<div>

## <a name="lync-server-support"></a><span data-ttu-id="d56bc-109">Lync Server-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="d56bc-109">Lync Server Support</span></span>

<span data-ttu-id="d56bc-110">Für Location-Based Routing muss lync Server 2013 CU1 auf allen Front-End-Pools und Standard Edition-Servern in einer bestimmten Topologie bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d56bc-110">Location-Based Routing requires that Lync Server 2013 CU1 is deployed on all Front End pools and Standard Edition servers in a given topology.</span></span> <span data-ttu-id="d56bc-111">Wenn lync Server 2013 CU1 nicht auf bestimmten lync-Komponenten in der Topologie installiert ist, können Location-Based Routing Einschränkungen nicht vollständig erzwungen werden.</span><span class="sxs-lookup"><span data-stu-id="d56bc-111">If Lync Server 2013 CU1 is not installed on certain Lync components in the topology, Location-Based Routing restrictions cannot be fully enforced.</span></span>

<span data-ttu-id="d56bc-112">In der folgenden Tabelle wird die Kombination aus Serverrollen und Versionen aufgeführt, die für Location-Based Routing unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d56bc-112">The following table identifies the combination of server roles and versions that is supported for Location-Based Routing.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d56bc-113">Poolversion</span><span class="sxs-lookup"><span data-stu-id="d56bc-113">Pool version</span></span></th>
<th><span data-ttu-id="d56bc-114">Mediation Server-Version</span><span class="sxs-lookup"><span data-stu-id="d56bc-114">Mediation Server version</span></span></th>
<th><span data-ttu-id="d56bc-115">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d56bc-115">Supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d56bc-116">Lync Server 2013 Februar 2013 Kumulatives Update</span><span class="sxs-lookup"><span data-stu-id="d56bc-116">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="d56bc-117">Lync Server 2013 Februar 2013 Kumulatives Update</span><span class="sxs-lookup"><span data-stu-id="d56bc-117">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="d56bc-118">ja</span><span class="sxs-lookup"><span data-stu-id="d56bc-118">yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d56bc-119">Lync Server 2013 Februar 2013 Kumulatives Update</span><span class="sxs-lookup"><span data-stu-id="d56bc-119">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="d56bc-120">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d56bc-120">Lync Server 2013</span></span></p></td>
<td><p><span data-ttu-id="d56bc-121">nein</span><span class="sxs-lookup"><span data-stu-id="d56bc-121">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d56bc-122">Lync Server 2013 Februar 2013 Kumulatives Update</span><span class="sxs-lookup"><span data-stu-id="d56bc-122">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="d56bc-123">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="d56bc-123">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="d56bc-124">nein</span><span class="sxs-lookup"><span data-stu-id="d56bc-124">no</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d56bc-125">Lync Server 2013 Februar 2013 Kumulatives Update</span><span class="sxs-lookup"><span data-stu-id="d56bc-125">Lync Server 2013 February 2013 Cumulative Update</span></span></p></td>
<td><p><span data-ttu-id="d56bc-126">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="d56bc-126">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="d56bc-127">nein</span><span class="sxs-lookup"><span data-stu-id="d56bc-127">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d56bc-128">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d56bc-128">Lync Server 2013</span></span></p></td>
<td><p><span data-ttu-id="d56bc-129">Beliebig</span><span class="sxs-lookup"><span data-stu-id="d56bc-129">any</span></span></p></td>
<td><p><span data-ttu-id="d56bc-130">nein</span><span class="sxs-lookup"><span data-stu-id="d56bc-130">no</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d56bc-131">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="d56bc-131">Lync Server 2010</span></span></p></td>
<td><p><span data-ttu-id="d56bc-132">Beliebig</span><span class="sxs-lookup"><span data-stu-id="d56bc-132">any</span></span></p></td>
<td><p><span data-ttu-id="d56bc-133">nein</span><span class="sxs-lookup"><span data-stu-id="d56bc-133">no</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d56bc-134">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="d56bc-134">Office Communications Server 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="d56bc-135">Beliebig</span><span class="sxs-lookup"><span data-stu-id="d56bc-135">any</span></span></p></td>
<td><p><span data-ttu-id="d56bc-136">nein</span><span class="sxs-lookup"><span data-stu-id="d56bc-136">no</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="lync-client-support"></a><span data-ttu-id="d56bc-137">Lync-Client Unterstützung</span><span class="sxs-lookup"><span data-stu-id="d56bc-137">Lync Client Support</span></span>

<span data-ttu-id="d56bc-138">In der folgenden Tabelle sind die Clients aufgeführt, die von Location-Based Routing unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="d56bc-138">The following table identifies the clients that Location-Based Routing supports.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d56bc-139">Clienttyp</span><span class="sxs-lookup"><span data-stu-id="d56bc-139">Client type</span></span></th>
<th><span data-ttu-id="d56bc-140">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="d56bc-140">Supported</span></span></th>
<th><span data-ttu-id="d56bc-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d56bc-141">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d56bc-142">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="d56bc-142">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="d56bc-143">ja</span><span class="sxs-lookup"><span data-stu-id="d56bc-143">yes</span></span></p></td>
<td><p><span data-ttu-id="d56bc-144">Einschließlich lync 2013 Februar 2013 Kumulatives Update</span><span class="sxs-lookup"><span data-stu-id="d56bc-144">Including Lync 2013 February 2013 Cumulative Update</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d56bc-145">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="d56bc-145">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="d56bc-146">ja</span><span class="sxs-lookup"><span data-stu-id="d56bc-146">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d56bc-147">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="d56bc-147">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="d56bc-148">nein</span><span class="sxs-lookup"><span data-stu-id="d56bc-148">no</span></span></p></td>
<td> </td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d56bc-149">Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="d56bc-149">Lync Phone Edition</span></span></p></td>
<td><p><span data-ttu-id="d56bc-150">ja</span><span class="sxs-lookup"><span data-stu-id="d56bc-150">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d56bc-151">Lync Attendant</span><span class="sxs-lookup"><span data-stu-id="d56bc-151">Lync Attendant</span></span></p></td>
<td><p><span data-ttu-id="d56bc-152">ja</span><span class="sxs-lookup"><span data-stu-id="d56bc-152">yes</span></span></p></td>
<td> </td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d56bc-153">Lync für Windows 8</span><span class="sxs-lookup"><span data-stu-id="d56bc-153">Lync for Windows 8</span></span></p></td>
<td><p><span data-ttu-id="d56bc-154">nein</span><span class="sxs-lookup"><span data-stu-id="d56bc-154">no</span></span></p></td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d56bc-155">Lync Mobile 2013</span><span class="sxs-lookup"><span data-stu-id="d56bc-155">Lync Mobile 2013</span></span></p></td>
<td><p><span data-ttu-id="d56bc-156">nein</span><span class="sxs-lookup"><span data-stu-id="d56bc-156">no</span></span></p></td>
<td><p><span data-ttu-id="d56bc-157">VoIP muss für lync Mobile 2013-Clients deaktiviert sein, wenn Sie von Benutzern mit aktiviertem Location-Based Routing verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d56bc-157">VoIP must be disabled for Lync Mobile 2013 clients if used by users with Location-Based Routing enabled.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d56bc-158">Lync Mobile 2010</span><span class="sxs-lookup"><span data-stu-id="d56bc-158">Lync Mobile 2010</span></span></p></td>
<td><p><span data-ttu-id="d56bc-159">ja</span><span class="sxs-lookup"><span data-stu-id="d56bc-159">yes</span></span></p></td>
<td> </td>
</tr>
</tbody>
</table>

  

<div>


> [!NOTE]  
> <span data-ttu-id="d56bc-160">Wenn Sie VoIP für lync Mobile 2013-Clients deaktivieren möchten, weisen Sie der Einstellung "IP Audio/Video" eine Mobilitätsrichtlinie zu, die für alle Benutzer deaktiviert ist, die für standortbasiertes Routing aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="d56bc-160">To disable VoIP for Lync Mobile 2013 clients, assign a mobility policy with the setting, IP Audio/Video, disabled for all users enabled for Location Based Routing.</span></span> <span data-ttu-id="d56bc-161">Ausführlichere Informationen zu Mobilitätsrichtlinien finden Sie unter <A href="https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy">New-CsMobilityPolicy</A>.</span><span class="sxs-lookup"><span data-stu-id="d56bc-161">For more details about mobility policy, see <A href="https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy">New-CsMobilityPolicy</A>.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d56bc-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d56bc-162">See Also</span></span>


[<span data-ttu-id="d56bc-163">Planung des standortbasierten Routings in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d56bc-163">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="d56bc-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d56bc-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

