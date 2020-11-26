---
title: 'Lync Server 2013: VideoStream-Tabelle'
description: 'Lync Server 2013: Videostream-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoStream table
ms:assetid: 4275ede7-5467-4a97-b8c8-a4b00917bf32
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425928(v=OCS.15)
ms:contentKeyID: 48184014
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d741478e1f6290685181bff471f143e41ce9ca1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444126"
---
# <a name="videostream-table-in-lync-server-2013"></a><span data-ttu-id="b7945-103">VideoStream-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7945-103">VideoStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b7945-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b7945-104">

<span> </span></span></span>

<span data-ttu-id="b7945-105">_**Letztes Änderungsdatum des Themas:** 2013-12-13_</span><span class="sxs-lookup"><span data-stu-id="b7945-105">_**Topic Last Modified:** 2013-12-13_</span></span>

<span data-ttu-id="b7945-106">Jeder Datensatz steht für einen Videostream.</span><span class="sxs-lookup"><span data-stu-id="b7945-106">Each record represents one video stream.</span></span> <span data-ttu-id="b7945-107">Eine Video medienzeile enthält in der Regel zwei Videostreams.</span><span class="sxs-lookup"><span data-stu-id="b7945-107">One video media line usually contains two video streams.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b7945-108"><strong>Spalte</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="b7945-109"><strong>Datentyp</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="b7945-110"><strong>Schlüssel/Index</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="b7945-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b7945-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-113">datetime</span><span class="sxs-lookup"><span data-stu-id="b7945-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="b7945-114">Primary</span><span class="sxs-lookup"><span data-stu-id="b7945-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="b7945-115">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b7945-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-117">int</span><span class="sxs-lookup"><span data-stu-id="b7945-117">int</span></span></p></td>
<td><p><span data-ttu-id="b7945-118">Primary</span><span class="sxs-lookup"><span data-stu-id="b7945-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="b7945-119">R, auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b7945-119">R Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="b7945-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="b7945-122">Primary</span><span class="sxs-lookup"><span data-stu-id="b7945-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="b7945-123">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="b7945-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-124"><strong>Datenstrom-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-124"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-125">int</span><span class="sxs-lookup"><span data-stu-id="b7945-125">int</span></span></p></td>
<td><p><span data-ttu-id="b7945-126">Primary</span><span class="sxs-lookup"><span data-stu-id="b7945-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="b7945-127">Eindeutige ID innerhalb einer medienzeile</span><span class="sxs-lookup"><span data-stu-id="b7945-127">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-128"><strong>VideoPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-128"><strong>VideoPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-129">smallint</span><span class="sxs-lookup"><span data-stu-id="b7945-129">smallint</span></span></p></td>
<td><p><span data-ttu-id="b7945-130">Fremd, primär</span><span class="sxs-lookup"><span data-stu-id="b7945-130">Foreign, Primary</span></span></p></td>
<td><p><span data-ttu-id="b7945-131">Nutzlast-Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="b7945-131">Payload description.</span></span> <span data-ttu-id="b7945-132">Weitere Informationen finden Sie <a href="lync-server-2013-payloaddescription-table.md">in der PayloadDescription-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b7945-132">See the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-133"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-133"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-134">int</span><span class="sxs-lookup"><span data-stu-id="b7945-134">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b7945-135">Durchschnittlicher Netzwerk-Jitter aus RTCP-Statistiken (Real Time Control Protocol).</span><span class="sxs-lookup"><span data-stu-id="b7945-135">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-136"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-136"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-137">int</span><span class="sxs-lookup"><span data-stu-id="b7945-137">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b7945-138">Maximaler Netzwerk Jitter während der Videositzung.</span><span class="sxs-lookup"><span data-stu-id="b7945-138">Maximum network jitter during the video session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-139"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-139"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-140">int</span><span class="sxs-lookup"><span data-stu-id="b7945-140">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b7945-141">Roundtrip-Zeit von RTCP-Statistiken</span><span class="sxs-lookup"><span data-stu-id="b7945-141">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-142"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-142"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-143">int</span><span class="sxs-lookup"><span data-stu-id="b7945-143">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b7945-144">Maximale Roundtrip-Zeit für den Videostream.</span><span class="sxs-lookup"><span data-stu-id="b7945-144">Maximum round trip time for the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-145"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-145"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-146">Dezimal (5; 4)</span><span class="sxs-lookup"><span data-stu-id="b7945-146">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b7945-147">Durchschnittliche Paketverlustrate während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="b7945-147">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-148"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-148"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-149">Dezimal (5; 4)</span><span class="sxs-lookup"><span data-stu-id="b7945-149">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b7945-150">Maximaler Paketverlust während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="b7945-150">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-151"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-151"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-152">int</span><span class="sxs-lookup"><span data-stu-id="b7945-152">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b7945-153">Paketanzahl für den Videostream (Echt Zeit Transport Protokoll, RTP).</span><span class="sxs-lookup"><span data-stu-id="b7945-153">Packet count for the video stream (Real Time Transport Protocol, RTP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-154"><strong>Bandbreite</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-154"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-155">int</span><span class="sxs-lookup"><span data-stu-id="b7945-155">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b7945-156">Bandbreiten Schätzungen für den Videostream.</span><span class="sxs-lookup"><span data-stu-id="b7945-156">Bandwidth estimates for the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-157"><strong>VideoResolution</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-157"><strong>VideoResolution</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-158">char (9)</span><span class="sxs-lookup"><span data-stu-id="b7945-158">char(9)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b7945-159">Auflösung des Videos in Pixel Breite multipliziert mit Höhe des Pixels.</span><span class="sxs-lookup"><span data-stu-id="b7945-159">Resolution of the video in pixels width multiplied by pixels height.</span></span> <span data-ttu-id="b7945-160">Als Zeichenfolge gemeldet.</span><span class="sxs-lookup"><span data-stu-id="b7945-160">Reported as a string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-161"><strong>VideoBitRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-161"><strong>VideoBitRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-162">int</span><span class="sxs-lookup"><span data-stu-id="b7945-162">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b7945-163">Durchschnittliche Bitrate des Videodatenstroms.</span><span class="sxs-lookup"><span data-stu-id="b7945-163">Average bit rate of the video stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-164"><strong>InboundVideoFrameRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-164"><strong>InboundVideoFrameRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-165">Dezimal (9; 4)</span><span class="sxs-lookup"><span data-stu-id="b7945-165">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b7945-166">Die empfangene Videobildrate.</span><span class="sxs-lookup"><span data-stu-id="b7945-166">The video frame rate received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-167"><strong>OutboundVideoFrameRateAvg</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-167"><strong>OutboundVideoFrameRateAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-168">Dezimal (9; 4)</span><span class="sxs-lookup"><span data-stu-id="b7945-168">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b7945-169">Die Videobildrate wird gesendet.</span><span class="sxs-lookup"><span data-stu-id="b7945-169">The video frame rate sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-170"><strong>VideoBitRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-170"><strong>VideoBitRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-171">int</span><span class="sxs-lookup"><span data-stu-id="b7945-171">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b7945-172">Die maximale Video-Bitrate während der Videositzung.</span><span class="sxs-lookup"><span data-stu-id="b7945-172">The maximum video bit rate during the video session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-173"><strong>VideoFrameLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-173"><strong>VideoFrameLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-174">Dezimal (9; 4)</span><span class="sxs-lookup"><span data-stu-id="b7945-174">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b7945-175">Der Prozentsatz der Gesamtzahl der Videoframes, die verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="b7945-175">The percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-176"><strong>VideoFEC</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-176"><strong>VideoFEC</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-177">bit</span><span class="sxs-lookup"><span data-stu-id="b7945-177">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b7945-178">Nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="b7945-178">Not available.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-179"><strong>VideoLocalFrameLossPercentageAvg</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-179"><strong>VideoLocalFrameLossPercentageAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-180">Dezimal (9; 4)</span><span class="sxs-lookup"><span data-stu-id="b7945-180">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-181">Der Prozentsatz der Gesamtzahl der Videoframes, die verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="b7945-181">The percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-182"><strong>CIFQualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-182"><strong>CIFQualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-183">tinyint</span><span class="sxs-lookup"><span data-stu-id="b7945-183">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-184">Der Prozentsatz des Anrufs, der sich in der CIF-Auflösung (Common Interchange Format) befand.</span><span class="sxs-lookup"><span data-stu-id="b7945-184">The percentage of the call that was at the Common Interchange Format (CIF) resolution.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-185"><strong>VGAQualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-185"><strong>VGAQualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-186">tinyint</span><span class="sxs-lookup"><span data-stu-id="b7945-186">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-187">Der Prozentsatz des Anrufs mit VGA-Auflösung.</span><span class="sxs-lookup"><span data-stu-id="b7945-187">The percentage of the call that was at VGA resolution.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-188"><strong>HD720QualityRatio</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-188"><strong>HD720QualityRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-189">tinyint</span><span class="sxs-lookup"><span data-stu-id="b7945-189">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-190">Der Prozentsatz des Anrufs, der mit der HD720-Auflösung erfolgte.</span><span class="sxs-lookup"><span data-stu-id="b7945-190">The percentage of the call that was at HD720 resolution.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-191"><strong>NoneDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-191"><strong>NoneDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-192">tinyint</span><span class="sxs-lookup"><span data-stu-id="b7945-192">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-193">Prozentsatz der Anrufdauer ohne Frame-Drop</span><span class="sxs-lookup"><span data-stu-id="b7945-193">Percentage of call duration with no frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-194"><strong>BDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-194"><strong>BDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-195">tinyint</span><span class="sxs-lookup"><span data-stu-id="b7945-195">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-196">Prozentsatz der Anrufdauer mit B-Frame-Abwurf.</span><span class="sxs-lookup"><span data-stu-id="b7945-196">Percentage of call duration with B frame drop.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-197"><strong>BPDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-197"><strong>BPDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-198">tinyint</span><span class="sxs-lookup"><span data-stu-id="b7945-198">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-199">Prozentsatz der Anrufdauer mit BP-Frame-Drop.</span><span class="sxs-lookup"><span data-stu-id="b7945-199">Percentage of call duration with BP frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-200"><strong>BPSPDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-200"><strong>BPSPDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-201">tinyint</span><span class="sxs-lookup"><span data-stu-id="b7945-201">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-202">Prozentsatz der Anrufdauer mit BPSP Frame Drop.</span><span class="sxs-lookup"><span data-stu-id="b7945-202">Percentage of call duration with BPSP frame drop.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-203"><strong>BPSPIDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-203"><strong>BPSPIDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-204">tinyint</span><span class="sxs-lookup"><span data-stu-id="b7945-204">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-205">Prozentsatz der Anrufdauer mit BPSPI Frame Drop.</span><span class="sxs-lookup"><span data-stu-id="b7945-205">Percentage of call duration with BPSPI frame drop.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-206"><strong>Inbound</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-206"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-207">bit</span><span class="sxs-lookup"><span data-stu-id="b7945-207">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b7945-208">Datenstrom auf Empfängerseite wird empfangen.</span><span class="sxs-lookup"><span data-stu-id="b7945-208">Stream data on receiver side is received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-209"><strong>Ausgehend</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-209"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-210">bit</span><span class="sxs-lookup"><span data-stu-id="b7945-210">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b7945-211">Datenstrom auf Absenderseite wird empfangen.</span><span class="sxs-lookup"><span data-stu-id="b7945-211">Stream data on sender side is received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-212"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-212"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-213">bit</span><span class="sxs-lookup"><span data-stu-id="b7945-213">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="b7945-214">1 bedeutet, dass die Datenstrom Richtung vom Aufrufer zu aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="b7945-214">1 means the stream direction is from the caller to callee.</span></span></p>
<p><span data-ttu-id="b7945-215">0 bedeutet, dass die Datenstrom Richtung vom aufgerufenen zum Aufrufer ist.</span><span class="sxs-lookup"><span data-stu-id="b7945-215">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-216"><strong>LossCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-216"><strong>LossCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-217">float</span><span class="sxs-lookup"><span data-stu-id="b7945-217">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-218">Gibt den Prozentsatz der Zeit an, zu der sich der Anruf in einem Engpass Zustand befand.</span><span class="sxs-lookup"><span data-stu-id="b7945-218">Indicates the percentage of the time when the call was in a loss congestion state.</span></span></p>
<p><span data-ttu-id="b7945-219">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-219">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-220"><strong>DelayCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-220"><strong>DelayCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-221">float</span><span class="sxs-lookup"><span data-stu-id="b7945-221">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-222">Gibt den Prozentsatz des Anrufs an, während dessen Überlastung durch das verspätete Eintreffen von Netzwerkpaketen verursacht wurde.</span><span class="sxs-lookup"><span data-stu-id="b7945-222">Indicates the percentage of the call during which congestion was caused by the delayed arrival of network packets.</span></span></p>
<p><span data-ttu-id="b7945-223">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-223">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-224"><strong>ContentionDetectedPercent</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-224"><strong>ContentionDetectedPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-225">float</span><span class="sxs-lookup"><span data-stu-id="b7945-225">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-226">Gibt den Prozentsatz der Zeit an, zu der der Anruf im Wettbewerb um Netzwerkressourcen erfolgte.</span><span class="sxs-lookup"><span data-stu-id="b7945-226">Indicates the percentage of the time when the call was competing for network resources.</span></span></p>
<p><span data-ttu-id="b7945-227">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-227">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-228"><strong>BandwidthEstMin</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-228"><strong>BandwidthEstMin</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-229">int</span><span class="sxs-lookup"><span data-stu-id="b7945-229">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-230">Minimaler Grad der Bandbreitenschätzung, gemessen während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="b7945-230">Minimum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="b7945-231">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-231">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-232"><strong>BandwidthEstMax</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-232"><strong>BandwidthEstMax</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-233">int</span><span class="sxs-lookup"><span data-stu-id="b7945-233">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-234">Maximale Menge an Bandbreitenschätzung, die während des Anrufs gemessen wurde.</span><span class="sxs-lookup"><span data-stu-id="b7945-234">Maximum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="b7945-235">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-235">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-236"><strong>BandwidthEstStdDev</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-236"><strong>BandwidthEstStdDev</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-237">int</span><span class="sxs-lookup"><span data-stu-id="b7945-237">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-238">Standard Abweichung der Bandbreitenschätzung, die während des Anrufs gemessen wurde.</span><span class="sxs-lookup"><span data-stu-id="b7945-238">Standard deviation of the bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="b7945-239">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-239">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-240"><strong>BandwidthEstAvge</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-240"><strong>BandwidthEstAvge</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-241">int</span><span class="sxs-lookup"><span data-stu-id="b7945-241">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-242">Durchschnittliche Menge an Bandbreitenschätzung, die während des Anrufs gemessen wurde.</span><span class="sxs-lookup"><span data-stu-id="b7945-242">Average amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="b7945-243">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-243">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-244"><strong>LowBandwidthForMultiview</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-244"><strong>LowBandwidthForMultiview</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-245">float</span><span class="sxs-lookup"><span data-stu-id="b7945-245">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-246">Prozentsatz des Anrufs, bei dem der Endpunkt festgestellt hat, dass die Netzwerkverbindung MultiView-Video nicht unterstützenkann.</span><span class="sxs-lookup"><span data-stu-id="b7945-246">Percentage of the call where the endpoint determined that the network connection could not support multiview video.</span></span></p>
<p><span data-ttu-id="b7945-247">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-247">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-248"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-248"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-249">float</span><span class="sxs-lookup"><span data-stu-id="b7945-249">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-250">Gesamtzahl der unidirektionalen Latenzzeit.</span><span class="sxs-lookup"><span data-stu-id="b7945-250">Total amount of one-way latency.</span></span> <span data-ttu-id="b7945-251">Die relative unidirektionale Latenz misst die Verzögerung zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="b7945-251">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="b7945-252">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-252">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-253"><strong>RelativeOneWayAverage</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-253"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-254">float</span><span class="sxs-lookup"><span data-stu-id="b7945-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-255">Durchschnittliche Anzahl der unidirektionalen Latenzzeit.</span><span class="sxs-lookup"><span data-stu-id="b7945-255">Average amount of one-way latency.</span></span> <span data-ttu-id="b7945-256">Die relative unidirektionale Latenz misst die Verzögerung zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="b7945-256">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="b7945-257">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-257">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-258"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-258"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-259">float</span><span class="sxs-lookup"><span data-stu-id="b7945-259">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-260">Maximale Anzahl von unidirektionalen Latenzzeiten.</span><span class="sxs-lookup"><span data-stu-id="b7945-260">Maximum amount of one-way latency.</span></span> <span data-ttu-id="b7945-261">Die relative unidirektionale Latenz misst die Verzögerung zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="b7945-261">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="b7945-262">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-262">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-263"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-263"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-264">int</span><span class="sxs-lookup"><span data-stu-id="b7945-264">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-265">Gesamtzahl der einseitigen Burst-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="b7945-265">Total one-way burst occurrences.</span></span> <span data-ttu-id="b7945-266">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen.</span><span class="sxs-lookup"><span data-stu-id="b7945-266">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="b7945-267">Diese Metrik misst den Datenfluss zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="b7945-267">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="b7945-268">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-268">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-269"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-269"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-270">int</span><span class="sxs-lookup"><span data-stu-id="b7945-270">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-271">Totale unidirektionale Burst Dichte.</span><span class="sxs-lookup"><span data-stu-id="b7945-271">Total one-way burst density.</span></span> <span data-ttu-id="b7945-272">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen.</span><span class="sxs-lookup"><span data-stu-id="b7945-272">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="b7945-273">Diese Metrik misst den Datenfluss zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="b7945-273">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="b7945-274">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-274">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-275"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-275"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-276">float</span><span class="sxs-lookup"><span data-stu-id="b7945-276">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-277">Gesamtdauer des einseitigen Bursts.</span><span class="sxs-lookup"><span data-stu-id="b7945-277">Total one-way burst duration.</span></span> <span data-ttu-id="b7945-278">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen.</span><span class="sxs-lookup"><span data-stu-id="b7945-278">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="b7945-279">Diese Metrik misst den Datenfluss zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="b7945-279">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="b7945-280">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-280">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-281"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-281"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-282">int</span><span class="sxs-lookup"><span data-stu-id="b7945-282">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-283">Gesamtanzahl der einseitigen Lücken.</span><span class="sxs-lookup"><span data-stu-id="b7945-283">Total one-way gap occurrences.</span></span> <span data-ttu-id="b7945-284">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen. Lücken deuten auf Verzögerungen zwischen diesen Bursts hin.</span><span class="sxs-lookup"><span data-stu-id="b7945-284">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="b7945-285">Diese Metrik misst den Datenfluss zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="b7945-285">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="b7945-286">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-286">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-287"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-287"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-288">float</span><span class="sxs-lookup"><span data-stu-id="b7945-288">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-289">Gesamtdichte für einseitigen Abstand.</span><span class="sxs-lookup"><span data-stu-id="b7945-289">Total one-way gap density.</span></span> <span data-ttu-id="b7945-290">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen. Lücken deuten auf Verzögerungen zwischen diesen Bursts hin.</span><span class="sxs-lookup"><span data-stu-id="b7945-290">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="b7945-291">Diese Metrik misst den Datenfluss zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="b7945-291">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="b7945-292">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-292">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-293"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-293"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-294">float</span><span class="sxs-lookup"><span data-stu-id="b7945-294">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-295">Gesamtdauer der einseitigen Lücke</span><span class="sxs-lookup"><span data-stu-id="b7945-295">Total one-way gap duration.</span></span> <span data-ttu-id="b7945-296">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen. Lücken deuten auf Verzögerungen zwischen diesen Bursts hin.</span><span class="sxs-lookup"><span data-stu-id="b7945-296">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="b7945-297">Diese Metrik misst den Datenfluss zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="b7945-297">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="b7945-298">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-298">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-299"><strong>VideoPacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-299"><strong>VideoPacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-300">Dezimal (9; 4)</span><span class="sxs-lookup"><span data-stu-id="b7945-300">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-301">Die Rate, mit der Videopakete verloren gegangen sind.</span><span class="sxs-lookup"><span data-stu-id="b7945-301">Rate at which video packets were lost.</span></span></p>
<p><span data-ttu-id="b7945-302">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-302">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-303"><strong>VideoAllocateBWAvg</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-303"><strong>VideoAllocateBWAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-304">int</span><span class="sxs-lookup"><span data-stu-id="b7945-304">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-305">Der durchschnittliche Umfang der für Video zugewiesenen Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="b7945-305">Average amount of bandwidth allocated for video.</span></span></p>
<p><span data-ttu-id="b7945-306">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-306">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-307"><strong>SendCodecTypes</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-307"><strong>SendCodecTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-308">smallint</span><span class="sxs-lookup"><span data-stu-id="b7945-308">smallint</span></span></p></td>
<td><p><span data-ttu-id="b7945-309">Fremd</span><span class="sxs-lookup"><span data-stu-id="b7945-309">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b7945-310">Der Typ der vom Absender verwendeten Video-Codecs.</span><span class="sxs-lookup"><span data-stu-id="b7945-310">Type of video codecs used by the sender.</span></span> <span data-ttu-id="b7945-311">Weitere Informationen finden Sie <a href="lync-server-2013-codecdescription-table.md">in der CodecDescription-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b7945-311">See the <a href="lync-server-2013-codecdescription-table.md">CodecDescription table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="b7945-312">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-312">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-313"><strong>SendResolutionWidth</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-313"><strong>SendResolutionWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-314">int</span><span class="sxs-lookup"><span data-stu-id="b7945-314">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-315">Vom Absender verwendete Auflösungsbreite.</span><span class="sxs-lookup"><span data-stu-id="b7945-315">Resolution width used by the sender.</span></span></p>
<p><span data-ttu-id="b7945-316">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-316">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-317"><strong>SendResolutionHeight</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-317"><strong>SendResolutionHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-318">int</span><span class="sxs-lookup"><span data-stu-id="b7945-318">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-319">Die vom Absender verwendete auflösungshöhe.</span><span class="sxs-lookup"><span data-stu-id="b7945-319">Resolution height used by the sender.</span></span></p>
<p><span data-ttu-id="b7945-320">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-320">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-321"><strong>SendFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-321"><strong>SendFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-322">float</span><span class="sxs-lookup"><span data-stu-id="b7945-322">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-323">Durchschnittliche Übertragungsrate für Video-Frames, die vom Absender verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b7945-323">Average video frame rate transmission used by the sender.</span></span></p>
<p><span data-ttu-id="b7945-324">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-324">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-325"><strong>SendBitRateMaximum</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-325"><strong>SendBitRateMaximum</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-326">int</span><span class="sxs-lookup"><span data-stu-id="b7945-326">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-327">Die maximale Bitrate für den Absender.</span><span class="sxs-lookup"><span data-stu-id="b7945-327">Maximum bit rate for the sender.</span></span></p>
<p><span data-ttu-id="b7945-328">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-328">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-329"><strong>SendBitRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-329"><strong>SendBitRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-330">int</span><span class="sxs-lookup"><span data-stu-id="b7945-330">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-331">Durchschnittliche Bitrate für den Absender.</span><span class="sxs-lookup"><span data-stu-id="b7945-331">Average bit rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-332"><strong>SendVideoStreamsMax</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-332"><strong>SendVideoStreamsMax</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-333">int</span><span class="sxs-lookup"><span data-stu-id="b7945-333">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-334">Maximale Anzahl der vom Absender verwendeten Videodatenströme.</span><span class="sxs-lookup"><span data-stu-id="b7945-334">Maximum number of video streams used by the sender.</span></span></p>
<p><span data-ttu-id="b7945-335">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-335">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-336"><strong>RecvCodecTypes</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-336"><strong>RecvCodecTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-337">smallint</span><span class="sxs-lookup"><span data-stu-id="b7945-337">smallint</span></span></p></td>
<td><p><span data-ttu-id="b7945-338">Fremd</span><span class="sxs-lookup"><span data-stu-id="b7945-338">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b7945-339">Vom Empfänger verwendete Video Codes.</span><span class="sxs-lookup"><span data-stu-id="b7945-339">Video codes used by the receiver.</span></span> <span data-ttu-id="b7945-340">Weitere Informationen finden Sie <a href="lync-server-2013-codecdescription-table.md">in der CodecDescription-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b7945-340">See the <a href="lync-server-2013-codecdescription-table.md">CodecDescription table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="b7945-341">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-341">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-342"><strong>RecvResolutionWidth</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-342"><strong>RecvResolutionWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-343">int</span><span class="sxs-lookup"><span data-stu-id="b7945-343">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-344">Vom Empfänger verwendete Auflösungsbreite.</span><span class="sxs-lookup"><span data-stu-id="b7945-344">Resolution width used by the receiver.</span></span></p>
<p><span data-ttu-id="b7945-345">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-345">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-346"><strong>RecvResolutionHeight</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-346"><strong>RecvResolutionHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-347">int</span><span class="sxs-lookup"><span data-stu-id="b7945-347">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-348">Vom Empfänger verwendete auflösungshöhe.</span><span class="sxs-lookup"><span data-stu-id="b7945-348">Resolution height used by the receiver.</span></span></p>
<p><span data-ttu-id="b7945-349">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-349">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-350"><strong>RecvFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-350"><strong>RecvFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-351">float</span><span class="sxs-lookup"><span data-stu-id="b7945-351">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-352">Durchschnittliche Videobildrate, die vom Empfänger verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b7945-352">Average video frame rate used by the receiver.</span></span></p>
<p><span data-ttu-id="b7945-353">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-353">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-354"><strong>RecvBitRateMaximum</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-354"><strong>RecvBitRateMaximum</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-355">int</span><span class="sxs-lookup"><span data-stu-id="b7945-355">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-356">Maximale Bitrate für den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="b7945-356">Maximum bit rate for the receiver.</span></span></p>
<p><span data-ttu-id="b7945-357">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-357">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-358"><strong>RecvBitRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-358"><strong>RecvBitRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-359">int</span><span class="sxs-lookup"><span data-stu-id="b7945-359">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-360">Durchschnittliche Bitrate für den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="b7945-360">Average bit rate for the receiver.</span></span></p>
<p><span data-ttu-id="b7945-361">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-361">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-362"><strong>RecvVideoStreamsMax</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-362"><strong>RecvVideoStreamsMax</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-363">int</span><span class="sxs-lookup"><span data-stu-id="b7945-363">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-364">Maximale Videodatenströme für den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="b7945-364">Maximum video streams for the receiver.</span></span></p>
<p><span data-ttu-id="b7945-365">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-365">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-366"><strong>RecvVideoStreamsMin</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-366"><strong>RecvVideoStreamsMin</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-367">int</span><span class="sxs-lookup"><span data-stu-id="b7945-367">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-368">Minimale Videodatenströme für den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="b7945-368">Minimum video streams for the receiver.</span></span></p>
<p><span data-ttu-id="b7945-369">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-369">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-370"><strong>RecvVideoStreamsMode</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-370"><strong>RecvVideoStreamsMode</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-371">int</span><span class="sxs-lookup"><span data-stu-id="b7945-371">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-372">Video Modus (beispielsweise Katalog oder einzelner Datenstrom) für den Empfänger.</span><span class="sxs-lookup"><span data-stu-id="b7945-372">Video mode (for example, gallery or single stream) for the receiver.</span></span></p>
<p><span data-ttu-id="b7945-373">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-373">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-374"><strong>VideoPostFECPLR</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-374"><strong>VideoPostFECPLR</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-375">float</span><span class="sxs-lookup"><span data-stu-id="b7945-375">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-376">Die Paketverlustrate, nachdem die weiter Leitungsfehler Korrektur angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="b7945-376">Packet loss rate after forward error correction has been applied.</span></span></p>
<p><span data-ttu-id="b7945-377">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-377">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-378"><strong>DynamicCapabilityPercent</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-378"><strong>DynamicCapabilityPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-379">float</span><span class="sxs-lookup"><span data-stu-id="b7945-379">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-380">Der Prozentsatz der Zeit, zu der das Flag für dynamische Funktionen aktiv war.</span><span class="sxs-lookup"><span data-stu-id="b7945-380">Percentage of time that the dynamic capability flag was active.</span></span></p>
<p><span data-ttu-id="b7945-381">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-381">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-382"><strong>ResolutionMin</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-382"><strong>ResolutionMin</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-383">char (9)</span><span class="sxs-lookup"><span data-stu-id="b7945-383">char(9)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-384">Minimale Auflösung während des Anrufs gemessen.</span><span class="sxs-lookup"><span data-stu-id="b7945-384">Minimum resolution measured during the call.</span></span></p>
<p><span data-ttu-id="b7945-385">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-385">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-386"><strong>LowBitRateCallPercent</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-386"><strong>LowBitRateCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-387">float</span><span class="sxs-lookup"><span data-stu-id="b7945-387">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-388">Der Prozentsatz des Anrufs unterhalb des Schwellenwerts für niedrige Bitraten (70 Kbit/s).</span><span class="sxs-lookup"><span data-stu-id="b7945-388">Percentage of the call below the low bit rate threshold (70 kilobits per second).</span></span></p>
<p><span data-ttu-id="b7945-389">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-389">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-390"><strong>Framerate (</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-390"><strong>LowFrameRateCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-391">float</span><span class="sxs-lookup"><span data-stu-id="b7945-391">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-392">Der Prozentsatz des Anrufs unterhalb des Schwellenwerts für niedrige Bildrate (7,5 Frames pro Sekunde, eingehend).</span><span class="sxs-lookup"><span data-stu-id="b7945-392">Percentage of the call below the low frame rate threshold (7.5 frames per second, inbound).</span></span></p>
<p><span data-ttu-id="b7945-393">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-393">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-394"><strong>LowResolutionCallPercent</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-394"><strong>LowResolutionCallPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-395">float</span><span class="sxs-lookup"><span data-stu-id="b7945-395">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-396">Der Prozentsatz des Anrufs, der mit der niedrigsten Auflösung erfolgte.</span><span class="sxs-lookup"><span data-stu-id="b7945-396">Percentage of the call that occurred at the lowest resolution.</span></span></p>
<p><span data-ttu-id="b7945-397">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-397">This column was introduced in Microsoft Lync Server 2013.</span></span></p>
<p><span data-ttu-id="b7945-398">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-398">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b7945-399"><strong>DurationSeconds</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-399"><strong>DurationSeconds</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-400">float</span><span class="sxs-lookup"><span data-stu-id="b7945-400">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-401">Die Länge des Anrufs in Sekunden.</span><span class="sxs-lookup"><span data-stu-id="b7945-401">Length of the call in seconds.</span></span></p>
<p><span data-ttu-id="b7945-402">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-402">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b7945-403"><strong>IsAggregatedData</strong></span><span class="sxs-lookup"><span data-stu-id="b7945-403"><strong>IsAggregatedData</strong></span></span></p></td>
<td><p><span data-ttu-id="b7945-404">bit</span><span class="sxs-lookup"><span data-stu-id="b7945-404">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b7945-405">Gibt an, ob die Daten aus mehreren anrufen aggregiert wurden.</span><span class="sxs-lookup"><span data-stu-id="b7945-405">Indicates whether the data has been aggregated from multiple calls.</span></span></p>
<p><span data-ttu-id="b7945-406">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b7945-406">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b7945-407">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b7945-407">


</div>

<span> </span>

</div>

</div>

</span></span></div>

