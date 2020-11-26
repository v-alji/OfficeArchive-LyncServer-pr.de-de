---
title: 'Lync Server 2013: Konfigurieren einer Failoverroute'
description: 'Lync Server 2013: Konfigurieren einer Failover-Route'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a failover route
ms:assetid: 76e48df4-3b78-4fb7-b1f7-c1e604b81bad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398581(v=OCS.15)
ms:contentKeyID: 48184542
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7cfc45276931685a2d42103b1b7f1d5015dcd7e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433521"
---
# <a name="configuring-a-failover-route-in-lync-server-2013"></a><span data-ttu-id="7eb28-103">Konfigurieren einer Failoverroute in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7eb28-103">Configuring a failover route in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7eb28-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7eb28-104">

<span> </span></span></span>

<span data-ttu-id="7eb28-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="7eb28-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="7eb28-106">Im folgenden Beispiel wird gezeigt, wie ein Administrator eine Failover-Route für die Verwendung definieren kann, wenn der Dallas-GW1 für die Wartung ausgefallen ist oder anderweitig nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7eb28-106">The following example shows how an administrator can define a failover route for use if the Dallas-GW1 is down for maintenance or is otherwise unavailable.</span></span> <span data-ttu-id="7eb28-107">Die folgenden Tabellen veranschaulichen die erforderliche Konfigurationsänderung.</span><span class="sxs-lookup"><span data-stu-id="7eb28-107">The following tables illustrate the required configuration change.</span></span>

### <a name="table-1-user-policy"></a><span data-ttu-id="7eb28-108">Tabelle 1</span><span class="sxs-lookup"><span data-stu-id="7eb28-108">Table 1.</span></span> <span data-ttu-id="7eb28-109">Benutzerrichtlinien</span><span class="sxs-lookup"><span data-stu-id="7eb28-109">User Policy</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7eb28-110">Benutzerrichtlinie</span><span class="sxs-lookup"><span data-stu-id="7eb28-110">User policy</span></span></th>
<th><span data-ttu-id="7eb28-111">Telefonnutzung</span><span class="sxs-lookup"><span data-stu-id="7eb28-111">Phone usage</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7eb28-112">Standardanrufrichtlinie</span><span class="sxs-lookup"><span data-stu-id="7eb28-112">Default Calling Policy</span></span></p></td>
<td><p><span data-ttu-id="7eb28-113">Local</span><span class="sxs-lookup"><span data-stu-id="7eb28-113">Local</span></span></p>
<p><span data-ttu-id="7eb28-114">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="7eb28-114">GlobalPSTNHopoff</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb28-115">Lokale Redmond-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="7eb28-115">Redmond Local Policy</span></span></p></td>
<td><p><span data-ttu-id="7eb28-116">RedmondLocal</span><span class="sxs-lookup"><span data-stu-id="7eb28-116">RedmondLocal</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb28-117">Dallas-Anrufrichtlinie</span><span class="sxs-lookup"><span data-stu-id="7eb28-117">Dallas Calling Policy</span></span></p></td>
<td><p><span data-ttu-id="7eb28-118">DallasUsers</span><span class="sxs-lookup"><span data-stu-id="7eb28-118">DallasUsers</span></span></p>
<p><span data-ttu-id="7eb28-119">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="7eb28-119">GlobalPSTNHopoff</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="table-2-routes"></a><span data-ttu-id="7eb28-120">Tabelle 2.</span><span class="sxs-lookup"><span data-stu-id="7eb28-120">Table 2.</span></span> <span data-ttu-id="7eb28-121">Routen</span><span class="sxs-lookup"><span data-stu-id="7eb28-121">Routes</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7eb28-122">Routenname</span><span class="sxs-lookup"><span data-stu-id="7eb28-122">Route name</span></span></th>
<th><span data-ttu-id="7eb28-123">Nummernmuster</span><span class="sxs-lookup"><span data-stu-id="7eb28-123">Number pattern</span></span></th>
<th><span data-ttu-id="7eb28-124">Telefonnutzung</span><span class="sxs-lookup"><span data-stu-id="7eb28-124">Phone usage</span></span></th>
<th><span data-ttu-id="7eb28-125">Stamm</span><span class="sxs-lookup"><span data-stu-id="7eb28-125">Trunk</span></span></th>
<th><span data-ttu-id="7eb28-126">Gateway</span><span class="sxs-lookup"><span data-stu-id="7eb28-126">Gateway</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7eb28-127">Lokale Redmond-Route</span><span class="sxs-lookup"><span data-stu-id="7eb28-127">Redmond Local Route</span></span></p></td>
<td><p><span data-ttu-id="7eb28-128">^\+1 (425 | 206 | 253) (\d {7} ) $</span><span class="sxs-lookup"><span data-stu-id="7eb28-128">^\+1(425|206|253)(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="7eb28-129">Local</span><span class="sxs-lookup"><span data-stu-id="7eb28-129">Local</span></span></p>
<p><span data-ttu-id="7eb28-130">RedmondLocal</span><span class="sxs-lookup"><span data-stu-id="7eb28-130">RedmondLocal</span></span></p></td>
<td><p><span data-ttu-id="7eb28-131">Trunk1</span><span class="sxs-lookup"><span data-stu-id="7eb28-131">Trunk1</span></span></p>
<p><span data-ttu-id="7eb28-132">Trunk2</span><span class="sxs-lookup"><span data-stu-id="7eb28-132">Trunk2</span></span></p></td>
<td><p><span data-ttu-id="7eb28-133">Rot-GW1</span><span class="sxs-lookup"><span data-stu-id="7eb28-133">Red-GW1</span></span></p>
<p><span data-ttu-id="7eb28-134">Rot-GW2</span><span class="sxs-lookup"><span data-stu-id="7eb28-134">Red-GW2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb28-135">Lokale Route für Dallas</span><span class="sxs-lookup"><span data-stu-id="7eb28-135">Dallas Local Route</span></span></p></td>
<td><p><span data-ttu-id="7eb28-136">^\+1 (972 | 214 | 469) (\d {7} ) $</span><span class="sxs-lookup"><span data-stu-id="7eb28-136">^\+1(972|214|469)(\d{7})$</span></span></p></td>
<td><p><span data-ttu-id="7eb28-137">Local</span><span class="sxs-lookup"><span data-stu-id="7eb28-137">Local</span></span></p></td>
<td><p><span data-ttu-id="7eb28-138">Trunk3</span><span class="sxs-lookup"><span data-stu-id="7eb28-138">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="7eb28-139">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="7eb28-139">Dallas-GW1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7eb28-140">Universelle Route</span><span class="sxs-lookup"><span data-stu-id="7eb28-140">Universal Route</span></span></p></td>
<td><p><span data-ttu-id="7eb28-141">^\+? (\d \*) $</span><span class="sxs-lookup"><span data-stu-id="7eb28-141">^\+?(\d\*)$</span></span></p></td>
<td><p><span data-ttu-id="7eb28-142">GlobalPSTNHopoff</span><span class="sxs-lookup"><span data-stu-id="7eb28-142">GlobalPSTNHopoff</span></span></p></td>
<td><p><span data-ttu-id="7eb28-143">Trunk1</span><span class="sxs-lookup"><span data-stu-id="7eb28-143">Trunk1</span></span></p>
<p><span data-ttu-id="7eb28-144">Trunk2</span><span class="sxs-lookup"><span data-stu-id="7eb28-144">Trunk2</span></span></p>
<p><span data-ttu-id="7eb28-145">Trunk3</span><span class="sxs-lookup"><span data-stu-id="7eb28-145">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="7eb28-146">Rot-GW1</span><span class="sxs-lookup"><span data-stu-id="7eb28-146">Red-GW1</span></span></p>
<p><span data-ttu-id="7eb28-147">Rot-GW2</span><span class="sxs-lookup"><span data-stu-id="7eb28-147">Red-GW2</span></span></p>
<p><span data-ttu-id="7eb28-148">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="7eb28-148">Dallas-GW1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7eb28-149">Route für Dallas-Benutzer</span><span class="sxs-lookup"><span data-stu-id="7eb28-149">Dallas Users Route</span></span></p></td>
<td><p><span data-ttu-id="7eb28-150">^\+? (\d \*) $</span><span class="sxs-lookup"><span data-stu-id="7eb28-150">^\+?(\d\*)$</span></span></p></td>
<td><p><span data-ttu-id="7eb28-151">DallasUsers</span><span class="sxs-lookup"><span data-stu-id="7eb28-151">DallasUsers</span></span></p></td>
<td><p><span data-ttu-id="7eb28-152">Trunk3</span><span class="sxs-lookup"><span data-stu-id="7eb28-152">Trunk3</span></span></p></td>
<td><p><span data-ttu-id="7eb28-153">Dallas-GW1</span><span class="sxs-lookup"><span data-stu-id="7eb28-153">Dallas-GW1</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="7eb28-154">In Tabelle 1 wird nach der DallasUsers-Telefonnutzung in der Dallas-Anrufrichtlinie eine Telefonverwendung von GlobalPSTNHopoff hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="7eb28-154">In Table 1, a phone usage of GlobalPSTNHopoff is added after the DallasUsers phone usage in the Dallas Calling Policy.</span></span> <span data-ttu-id="7eb28-155">Dies ermöglicht es anrufen mit der Dallas-Anrufrichtlinie, Routen zu verwenden, die für die GlobalPSTNHopoff-Telefonverwendung konfiguriert sind, wenn eine Route für die DallasUsers-Telefonnutzung nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="7eb28-155">This enables calls with the Dallas Calling policy to use routes that are configured for the GlobalPSTNHopoff phone usage if a route for the DallasUsers phone usage is unavailable.</span></span>

<span data-ttu-id="7eb28-156"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7eb28-156"></div>

<span> </span>

</div>

</div>

</span></span></div>

