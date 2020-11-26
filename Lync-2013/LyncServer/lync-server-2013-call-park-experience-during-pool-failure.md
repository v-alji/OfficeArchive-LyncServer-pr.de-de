---
title: 'Lync Server 2013: Abläufe für das Parken von Anrufen während des Ausfalls eines Pools'
description: 'Lync Server 2013: Anruf parken während eines Pool Fehlers.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Park experience during pool failure
ms:assetid: f6303e69-8771-492a-9e8b-c3d7ba231309
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205383(v=OCS.15)
ms:contentKeyID: 48185831
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b97a0af13d378b0753979c32b6d5ffe7a525cf0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435698"
---
# <a name="call-park-experience-in-lync-server-2013-during-pool-failure"></a><span data-ttu-id="6d634-103">Abläufe für das Parken von Anrufen in Lync Server 2013 während des Ausfalls eines Pools</span><span class="sxs-lookup"><span data-stu-id="6d634-103">Call Park experience in Lync Server 2013 during pool failure</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6d634-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6d634-104">

<span> </span></span></span>

<span data-ttu-id="6d634-105">_**Letztes Änderungsdatum des Themas:** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="6d634-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="6d634-106">Wenn ein Front-End-Pool aufgrund eines ungeplanten Vorfalls nicht mehr zur Verfügung steht, werden Anrufe, die geparkt, aber noch nicht abgerufen wurden, getrennt.</span><span class="sxs-lookup"><span data-stu-id="6d634-106">When a Front End pool becomes unavailable due an unplanned incident, calls that have been parked but not yet retrieved are disconnected.</span></span> <span data-ttu-id="6d634-107">Beim Failover zu einem Sicherungspool werden die Benutzer in den Sicherungspool umgeleitet und befinden sich im Widerstands Modus.</span><span class="sxs-lookup"><span data-stu-id="6d634-107">During failover to a backup pool, users are redirected to the backup pool and are in resiliency mode.</span></span> <span data-ttu-id="6d634-108">Im Resilienz-Modus können Benutzer keine Anrufe parken, aber Sie können Anrufe in Wartestellung setzen und übertragen.</span><span class="sxs-lookup"><span data-stu-id="6d634-108">While in resiliency mode, users cannot park calls, but they can place calls on hold and transfer them.</span></span> <span data-ttu-id="6d634-109">Nach Abschluss des Failovers können Anrufe wieder wie gewohnt abgestellt und abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6d634-109">When failover is complete, calls can again be parked and retrieved as usual.</span></span> <span data-ttu-id="6d634-110">Während des Failback können Benutzer Anrufe erst dann Parken, wenn Sie den Stabilitäts Modus verlassen.</span><span class="sxs-lookup"><span data-stu-id="6d634-110">During failback, users cannot park calls until they are out of resiliency mode.</span></span>

<span data-ttu-id="6d634-111">Während der Disaster Recovery verwenden Benutzer, die im Rahmen des Failovers an den Backup-Pool umgeleitet wurden, die Anwendung Parken, die im Backup-Pool bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6d634-111">During disaster recovery, users who have been redirected to the backup pool as part of the failover process use the Call Park application that is deployed in the backup pool.</span></span> <span data-ttu-id="6d634-112">Daher verwenden Benutzer, die an den Sicherungspool umgeleitet werden, die Einstellungen für den Anruf Park, die für die Anwendung "Parken" im Sicherungspool konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="6d634-112">Therefore, users who are redirected to the backup pool use the call park settings that are configured for the Call Park application in the backup pool.</span></span>

<span data-ttu-id="6d634-113">In der folgenden Tabelle sind die Erfahrungen des Anruf Parks in den Phasen der Disaster Recovery zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="6d634-113">The following table summarizes the Call Park experience through the phases of disaster recovery.</span></span>

### <a name="user-experience-during-disaster-recovery"></a><span data-ttu-id="6d634-114">Benutzererfahrung bei der Disaster Recovery</span><span class="sxs-lookup"><span data-stu-id="6d634-114">User Experience During Disaster Recovery</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6d634-115">Anruf Zustand</span><span class="sxs-lookup"><span data-stu-id="6d634-115">Call state</span></span></th>
<th><span data-ttu-id="6d634-116">Wenn ein Ausfall eintritt</span><span class="sxs-lookup"><span data-stu-id="6d634-116">When outage occurs</span></span></th>
<th><span data-ttu-id="6d634-117">Während des Failovers</span><span class="sxs-lookup"><span data-stu-id="6d634-117">During failover</span></span></th>
<th><span data-ttu-id="6d634-118">Während des Failbacks</span><span class="sxs-lookup"><span data-stu-id="6d634-118">During failback</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d634-119">Noch nicht geparkter Anruf</span><span class="sxs-lookup"><span data-stu-id="6d634-119">Call not yet parked</span></span></p></td>
<td><p><span data-ttu-id="6d634-120">Der Anruf bleibt verbunden, kann aber nicht abgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6d634-120">Call remains connected, but cannot be parked.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="6d634-121">Während des Failovers kann der Anruf nicht abgestellt werden, während sich die Benutzer im Resilienz-Modus befinden, können aber in Wartestellung gesetzt und übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="6d634-121">During failover, call cannot be parked while users are in resiliency mode, but can be put on hold and transferred.</span></span></p></li>
<li><p><span data-ttu-id="6d634-122">Nach Abschluss des Failovers kann der Anruf abgestellt und abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6d634-122">When failover completes, call can be parked and retrieved.</span></span></p></li>
</ul></td>
<td><ul>
<li><p><span data-ttu-id="6d634-123">Während des Failback kann der Anruf nicht abgestellt werden, während sich die Benutzer im Resilienz-Modus befinden, können aber in Wartestellung gesetzt und übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="6d634-123">During failback, call cannot be parked while users are in resiliency mode, but can be put on hold and transferred.</span></span></p></li>
<li><p><span data-ttu-id="6d634-124">Nach Abschluss des Failback kann der Anruf abgestellt und abgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="6d634-124">When failback completes, call can be parked and retrieved.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d634-125">Anruf abgestellt, aber noch nicht abgerufen</span><span class="sxs-lookup"><span data-stu-id="6d634-125">Call parked, but not yet retrieved</span></span></p></td>
<td><p><span data-ttu-id="6d634-126">Der Anruf wird getrennt.</span><span class="sxs-lookup"><span data-stu-id="6d634-126">Call is disconnected.</span></span></p></td>
<td><p><span data-ttu-id="6d634-127">Keine Anrufe in diesem Zustand.</span><span class="sxs-lookup"><span data-stu-id="6d634-127">No calls in this state.</span></span></p></td>
<td><p><span data-ttu-id="6d634-128">Der Anruf bleibt geparkt.</span><span class="sxs-lookup"><span data-stu-id="6d634-128">Call remains parked.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d634-129">Geparkten Anruf bereits abgerufen</span><span class="sxs-lookup"><span data-stu-id="6d634-129">Parked call already retrieved</span></span></p></td>
<td><p><span data-ttu-id="6d634-130">Der Anruf bleibt verbunden.</span><span class="sxs-lookup"><span data-stu-id="6d634-130">Call remains connected.</span></span></p></td>
<td><p><span data-ttu-id="6d634-131">Der Anruf bleibt verbunden.</span><span class="sxs-lookup"><span data-stu-id="6d634-131">Call remains connected.</span></span></p></td>
<td><p><span data-ttu-id="6d634-132">Der Anruf bleibt verbunden.</span><span class="sxs-lookup"><span data-stu-id="6d634-132">Call remains connected.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6d634-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6d634-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

