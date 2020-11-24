---
title: 'Lync Server 2013: VideoClientEvent-Tabelle'
description: 'Lync Server 2013: VideoClientEvent-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoClientEvent table
ms:assetid: e8ab963b-fe1d-45b3-b9bd-66a5f44c1629
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399039(v=OCS.15)
ms:contentKeyID: 48185891
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ae73ac2548e838241febe60a2d31f80983b01de5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395191"
---
# <a name="videoclientevent-table-in-lync-server-2013"></a><span data-ttu-id="5d084-103">VideoClientEvent-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d084-103">VideoClientEvent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5d084-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5d084-104">

<span> </span></span></span>

<span data-ttu-id="5d084-105">_**Letztes Änderungsdatum des Themas:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="5d084-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="5d084-106">Jeder Datensatz enthält ein Clientereignis für einen Endpunkt in einem Videoanruf.</span><span class="sxs-lookup"><span data-stu-id="5d084-106">Each record contains client event for one endpoint in a video call.</span></span> <span data-ttu-id="5d084-107">In der Regel verfügt ein Anruf über zwei Datensätze, einen für den Anrufer und einen für den aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="5d084-107">Usually, one call has two records, one for caller and one for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5d084-108"><strong>Spalte</strong></span><span class="sxs-lookup"><span data-stu-id="5d084-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="5d084-109"><strong>Datentyp</strong></span><span class="sxs-lookup"><span data-stu-id="5d084-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="5d084-110"><strong>Schlüssel/Index</strong></span><span class="sxs-lookup"><span data-stu-id="5d084-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="5d084-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="5d084-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d084-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="5d084-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5d084-113">datetime</span><span class="sxs-lookup"><span data-stu-id="5d084-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="5d084-114">Primary</span><span class="sxs-lookup"><span data-stu-id="5d084-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="5d084-115">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="5d084-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d084-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="5d084-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="5d084-117">int</span><span class="sxs-lookup"><span data-stu-id="5d084-117">int</span></span></p></td>
<td><p><span data-ttu-id="5d084-118">Primary</span><span class="sxs-lookup"><span data-stu-id="5d084-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="5d084-119">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="5d084-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d084-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="5d084-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="5d084-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="5d084-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="5d084-122">Primary</span><span class="sxs-lookup"><span data-stu-id="5d084-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="5d084-123">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="5d084-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d084-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="5d084-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="5d084-125">bit</span><span class="sxs-lookup"><span data-stu-id="5d084-125">bit</span></span></p></td>
<td><p><span data-ttu-id="5d084-126">Primary</span><span class="sxs-lookup"><span data-stu-id="5d084-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="5d084-127">0: Daten des angerufenen</span><span class="sxs-lookup"><span data-stu-id="5d084-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="5d084-128">1: Daten des Anrufers</span><span class="sxs-lookup"><span data-stu-id="5d084-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d084-129"><strong>NetworkBandwidthLowEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="5d084-129"><strong>NetworkBandwidthLowEventRatio</strong></span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5d084-130">Prozentsatz der Sitzung, für die das LowBandwidth-Ereignis für den Zustand "falsch" ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="5d084-130">Percentage of session the LowBandwidth event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="5d084-131">Die verfügbare Bandbreite reicht für ein akzeptables Spracherlebnis nicht aus.</span><span class="sxs-lookup"><span data-stu-id="5d084-131">The available bandwidth is insufficient for an acceptable voice experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d084-132"><strong>NetworkReceiveQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="5d084-132"><strong>NetworkReceiveQualityEventRatio</strong></span></span></p></td>
<td></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5d084-133">Prozentsatz der Sitzung, für die das ReceiveSendQuality-Ereignis für den Zustand "falsch" ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="5d084-133">Percentage of session the ReceiveSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="5d084-134">Die Netzwerkqualität in Bezug auf Jitter oder Paketverlust ist schwerwiegend und beeinträchtigt die Qualität des empfangenen Audiosignals.</span><span class="sxs-lookup"><span data-stu-id="5d084-134">Network quality in terms of jitter or packet loss is severe and impacts the quality of audio being received.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5d084-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5d084-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

