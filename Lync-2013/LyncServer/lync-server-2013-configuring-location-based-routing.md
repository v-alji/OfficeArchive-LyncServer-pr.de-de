---
title: 'Lync Server 2013: Konfigurieren von standortbasiertem Routing'
description: 'Lync Server 2013: Konfigurieren Location-Based Routings'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Location-Based Routing
ms:assetid: 63cdc474-e80f-43b1-a237-9d9ed673300a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994036(v=OCS.15)
ms:contentKeyID: 51803946
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 080c2a3a82a8714fc35ce882b0c6cb1630552f27
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433048"
---
# <a name="configuring-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="4d8ee-103">Konfigurieren von standortbasiertem Routing in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4d8ee-103">Configuring Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4d8ee-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4d8ee-104">

<span> </span></span></span>

<span data-ttu-id="4d8ee-105">_**Letztes Änderungsdatum des Themas:** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="4d8ee-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="4d8ee-106">Lync Server 2013 CU1, Location-Based Routing ist eine Funktion von Enterprise-VoIP.</span><span class="sxs-lookup"><span data-stu-id="4d8ee-106">Lync Server 2013 CU1, Location-Based Routing is a feature of Enterprise Voice.</span></span> <span data-ttu-id="4d8ee-107">Location-Based Routing ist ein Anruf Verwaltungsfeature, das steuert, wie Anrufe von lync Server 2013 CU1 weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="4d8ee-107">Location-Based Routing is a call management feature that controls how calls are routed by Lync Server 2013 CU1.</span></span> <span data-ttu-id="4d8ee-108">Sie erzwingt Einschränkungen, ob Anrufe an PBX-oder PSTN-Ziele basierend auf dem Standort des lync-Anrufers weitergeleitet werden können.</span><span class="sxs-lookup"><span data-stu-id="4d8ee-108">It enforces restrictions on whether calls can be routed to PBX or PSTN destinations based on the Lync caller’s location.</span></span> <span data-ttu-id="4d8ee-109">Location-Based Routing wendet Anruf Autorisierungsregeln für PSTN-Anrufe auf der Grundlage des Netzwerkspeicherorts des Anrufers an.</span><span class="sxs-lookup"><span data-stu-id="4d8ee-109">Location-Based Routing applies call authorization rules to PSTN calls based on the caller’s network location.</span></span> <span data-ttu-id="4d8ee-110">Der Standort des Anrufers wird anhand der Netzwerk Website bestimmt, die dem Netzwerk-Subnetz zugeordnet ist, an dem der Anrufer angeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="4d8ee-110">The caller’s location is determined based on the network site associated with the network subnet the caller is connected on.</span></span> <span data-ttu-id="4d8ee-111">Für die Konfiguration Location-Based Routings müssen zuerst Enterprise-VoIP bereitgestellt und dann netzwerkregionen,-Standorte und-Subnetze konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="4d8ee-111">Configuring Location-Based Routing requires first deploying Enterprise Voice, then configuring network regions, sites and subnets.</span></span> <span data-ttu-id="4d8ee-112">Damit wird die Grundlage für die Aktivierung Location-Based Routings eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="4d8ee-112">This sets up the foundation for enabling Location-Based Routing.</span></span>

<span data-ttu-id="4d8ee-113">Bevor Sie Location-Based Routing bereitstellen, müssen Sie zuerst Enterprise-VoIP bereitstellen und netzwerkregionen,-Standorte und Netzwerk-Subnetze an Ihre Netzwerk Websites anschließen.</span><span class="sxs-lookup"><span data-stu-id="4d8ee-113">Before deploying Location-Based Routing, you must first deploy Enterprise Voice, and configure network regions, sites, and associate network subnets to your network sites.</span></span> <span data-ttu-id="4d8ee-114">Nach Abschluss des Vorgangs können Sie Location-Based Routing konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="4d8ee-114">Once completed, you can configure Location-Based Routing.</span></span> <span data-ttu-id="4d8ee-115">Eine schrittweise Anleitung zum Konfigurieren von netzwerkregionen,-Websites und-Subnetzen finden Sie unter [Bereitstellen von erweiterten Enterprise-VoIP-Features in lync Server 2013](lync-server-2013-deploying-advanced-enterprise-voice-features.md)</span><span class="sxs-lookup"><span data-stu-id="4d8ee-115">For steps on how to configure network regions, sites and subnets, see [Deploying advanced Enterprise Voice features in Lync Server 2013](lync-server-2013-deploying-advanced-enterprise-voice-features.md)</span></span>

<span data-ttu-id="4d8ee-116">Dieser Abschnitt führt Sie durch die Konfiguration von Location-Based Routing mithilfe des folgenden Beispiels als Abbildung.</span><span class="sxs-lookup"><span data-stu-id="4d8ee-116">This section guides you through the configuration of Location-Based Routing using the following example as illustration.</span></span>

<span data-ttu-id="4d8ee-117">![Beispiel für standortbasiertes Routing für Enterprise-VoIP](images/JJ994036.b6ef5afc-36ac-406f-8ec2-a87532b20612(OCS.15).png "Beispiel für standortbasiertes Routing für Enterprise-VoIP")</span><span class="sxs-lookup"><span data-stu-id="4d8ee-117">![Enterprise Voice location-based routing example](images/JJ994036.b6ef5afc-36ac-406f-8ec2-a87532b20612(OCS.15).png "Enterprise Voice location-based routing example")</span></span>

  
<span data-ttu-id="4d8ee-118">In der folgenden Tabelle sind die in diesem Beispiel definierten Benutzer dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4d8ee-118">The following table represents the users defined in this example.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d8ee-119">Endpunkttyp</span><span class="sxs-lookup"><span data-stu-id="4d8ee-119">Endpoint type</span></span></th>
<th><span data-ttu-id="4d8ee-120">Ort</span><span class="sxs-lookup"><span data-stu-id="4d8ee-120">Location</span></span></th>
<th><span data-ttu-id="4d8ee-121">Benutzer</span><span class="sxs-lookup"><span data-stu-id="4d8ee-121">Users</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d8ee-122">Lync</span><span class="sxs-lookup"><span data-stu-id="4d8ee-122">Lync</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-123">Firmensitz in Delhi</span><span class="sxs-lookup"><span data-stu-id="4d8ee-123">Delhi corporate office</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-124">Del-lync-1, del-lync-2, del-lync-3</span><span class="sxs-lookup"><span data-stu-id="4d8ee-124">DEL-LYNC-1,DEL-LYNC-2,DEL-LYNC-3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d8ee-125">Lync</span><span class="sxs-lookup"><span data-stu-id="4d8ee-125">Lync</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-126">Firmensitz in Hyderabad</span><span class="sxs-lookup"><span data-stu-id="4d8ee-126">Hyderabad corporate office</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-127">Hyd-lync-1, Hyd-lync-2, Hyd-lync-3</span><span class="sxs-lookup"><span data-stu-id="4d8ee-127">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d8ee-128">Lync</span><span class="sxs-lookup"><span data-stu-id="4d8ee-128">Lync</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-129">Unbekannt (z.b. Hotel)</span><span class="sxs-lookup"><span data-stu-id="4d8ee-129">Unknown (i.e. hotel)</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-130">Unk-LYNC-1</span><span class="sxs-lookup"><span data-stu-id="4d8ee-130">UNK-LYNC-1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d8ee-131">PBX</span><span class="sxs-lookup"><span data-stu-id="4d8ee-131">PBX</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-132">Firmensitz in Delhi</span><span class="sxs-lookup"><span data-stu-id="4d8ee-132">Delhi corporate office</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-133">Del-PBX-1, del-PBX-2</span><span class="sxs-lookup"><span data-stu-id="4d8ee-133">DEL-PBX-1, DEL-PBX-2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d8ee-134">PBX</span><span class="sxs-lookup"><span data-stu-id="4d8ee-134">PBX</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-135">Firmensitz in Hyderabad</span><span class="sxs-lookup"><span data-stu-id="4d8ee-135">Hyderabad corporate office</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-136">Hyd-PBX-1, Hyd-PBX-2</span><span class="sxs-lookup"><span data-stu-id="4d8ee-136">HYD-PBX-1, HYD-PBX-2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d8ee-137">Telefonfestnetz (PSTN)</span><span class="sxs-lookup"><span data-stu-id="4d8ee-137">PSTN</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-138">Unbekannten</span><span class="sxs-lookup"><span data-stu-id="4d8ee-138">Unknown</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-139">PSTN-1, PSTN-2, PSTN-3</span><span class="sxs-lookup"><span data-stu-id="4d8ee-139">PSTN-1, PSTN-2, PSTN-3</span></span></p></td>
</tr>
</tbody>
</table>

  

<span data-ttu-id="4d8ee-140">In der folgenden Tabelle sind die in dieser Beispielumgebung dargestellten Systeme dargestellt.</span><span class="sxs-lookup"><span data-stu-id="4d8ee-140">The following table represents the systems illustrated in this example environment.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4d8ee-141">System</span><span class="sxs-lookup"><span data-stu-id="4d8ee-141">System</span></span></th>
<th><span data-ttu-id="4d8ee-142">Ort</span><span class="sxs-lookup"><span data-stu-id="4d8ee-142">Location</span></span></th>
<th><span data-ttu-id="4d8ee-143">Name</span><span class="sxs-lookup"><span data-stu-id="4d8ee-143">Name</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4d8ee-144">Lync Server 2013 CU1-Pool</span><span class="sxs-lookup"><span data-stu-id="4d8ee-144">Lync Server 2013 CU1 pool</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-145">Beliebig</span><span class="sxs-lookup"><span data-stu-id="4d8ee-145">any</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-146">LS-PL1</span><span class="sxs-lookup"><span data-stu-id="4d8ee-146">LS-PL1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d8ee-147">Lync Server 2013 CU1, Vermittlungsserver</span><span class="sxs-lookup"><span data-stu-id="4d8ee-147">Lync Server 2013 CU1, Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-148">Beliebig</span><span class="sxs-lookup"><span data-stu-id="4d8ee-148">any</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-149">MS-PL1</span><span class="sxs-lookup"><span data-stu-id="4d8ee-149">MS-PL1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d8ee-150">PSTN-Gateway 1</span><span class="sxs-lookup"><span data-stu-id="4d8ee-150">PSTN gateway 1</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-151">Delhi</span><span class="sxs-lookup"><span data-stu-id="4d8ee-151">Delhi</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-152">DEL-GW</span><span class="sxs-lookup"><span data-stu-id="4d8ee-152">DEL-GW</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d8ee-153">PSTN-Gateway 2</span><span class="sxs-lookup"><span data-stu-id="4d8ee-153">PSTN gateway 2</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-154">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="4d8ee-154">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-155">Hyd-GW</span><span class="sxs-lookup"><span data-stu-id="4d8ee-155">HYD-GW</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4d8ee-156">Telefonanlage 1</span><span class="sxs-lookup"><span data-stu-id="4d8ee-156">PBX 1</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-157">Delhi</span><span class="sxs-lookup"><span data-stu-id="4d8ee-157">Delhi</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-158">DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="4d8ee-158">DEL-PBX</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4d8ee-159">PBX 2</span><span class="sxs-lookup"><span data-stu-id="4d8ee-159">PBX 2</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-160">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="4d8ee-160">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="4d8ee-161">Red-PBX</span><span class="sxs-lookup"><span data-stu-id="4d8ee-161">RED-PBX</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="in-this-section"></a><span data-ttu-id="4d8ee-162">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="4d8ee-162">In This Section</span></span>

  - [<span data-ttu-id="4d8ee-163">Konfigurieren von Enterprise-VoIP in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4d8ee-163">Configuring Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-configuring-enterprise-voice.md)

  - [<span data-ttu-id="4d8ee-164">Bereitstellen von netzwerkregionen,-Websites und-Subnetzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4d8ee-164">Deploying network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-deploying-network-regions-sites-and-subnets.md)

  - [<span data-ttu-id="4d8ee-165">Aktivieren von Location-Based-Routing in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4d8ee-165">Enabling Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-enabling-location-based-routing.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4d8ee-166">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4d8ee-166">See Also</span></span>


[<span data-ttu-id="4d8ee-167">Bereitstellen von erweiterten Enterprise-VoIP-Features in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4d8ee-167">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-deploying-advanced-enterprise-voice-features.md)  
  

<span data-ttu-id="4d8ee-168"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4d8ee-168"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

