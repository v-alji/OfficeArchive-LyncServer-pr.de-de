---
title: 'Lync Server 2013: AudioStream-Tabelle'
description: 'Lync Server 2013: AudioStream-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioStream table
ms:assetid: 49ccbbc3-2f73-45fc-80a6-e612535cbc10
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425961(v=OCS.15)
ms:contentKeyID: 48184077
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af2e622e14c54fa4f9a6313e1b0dae8f2483132
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438176"
---
# <a name="audiostream-table-in-lync-server-2013"></a><span data-ttu-id="0af91-103">AudioStream-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0af91-103">AudioStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0af91-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0af91-104">

<span> </span></span></span>

<span data-ttu-id="0af91-105">_**Letztes Änderungsdatum des Themas:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="0af91-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="0af91-106">Jeder Datensatz steht für einen Audiostream.</span><span class="sxs-lookup"><span data-stu-id="0af91-106">Each record represents one audio stream.</span></span> <span data-ttu-id="0af91-107">Eine Audio-Media-Zeile enthält in der Regel zwei Audiostreams.</span><span class="sxs-lookup"><span data-stu-id="0af91-107">One audio media line usually contains two audio streams.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0af91-108"><strong>Spalte</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="0af91-109"><strong>Datentyp</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="0af91-110"><strong>Schlüssel/Index</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="0af91-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0af91-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-113">datetime</span><span class="sxs-lookup"><span data-stu-id="0af91-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="0af91-114">Primary</span><span class="sxs-lookup"><span data-stu-id="0af91-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="0af91-115">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0af91-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-117">int</span><span class="sxs-lookup"><span data-stu-id="0af91-117">int</span></span></p></td>
<td><p><span data-ttu-id="0af91-118">Primary</span><span class="sxs-lookup"><span data-stu-id="0af91-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="0af91-119">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0af91-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="0af91-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="0af91-122">Primary</span><span class="sxs-lookup"><span data-stu-id="0af91-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="0af91-123">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0af91-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-124"><strong>Datenstrom-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-124"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-125">int</span><span class="sxs-lookup"><span data-stu-id="0af91-125">int</span></span></p></td>
<td><p><span data-ttu-id="0af91-126">Primary</span><span class="sxs-lookup"><span data-stu-id="0af91-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="0af91-127">Eindeutige ID innerhalb einer medienzeile</span><span class="sxs-lookup"><span data-stu-id="0af91-127">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-128"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-128"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-129">int</span><span class="sxs-lookup"><span data-stu-id="0af91-129">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-130">Durchschnittlicher Netzwerk-Jitter aus RTCP-Statistiken (Real Time Control Protocol).</span><span class="sxs-lookup"><span data-stu-id="0af91-130">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-131"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-131"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-132">int</span><span class="sxs-lookup"><span data-stu-id="0af91-132">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-133">Maximaler Netzwerk Jitter während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="0af91-133">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-134"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-134"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-135">Dezimal (5; 4)</span><span class="sxs-lookup"><span data-stu-id="0af91-135">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-136">Durchschnittliche Paketverlustrate während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="0af91-136">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-137"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-137"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-138">Dezimal (5; 4)</span><span class="sxs-lookup"><span data-stu-id="0af91-138">decimal(5,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-139">Maximaler Paketverlust während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="0af91-139">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-140"><strong>BurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-140"><strong>BurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-141">Dezimal (9; 4)</span><span class="sxs-lookup"><span data-stu-id="0af91-141">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-142">Durchschnittliche Dichte des Paketverlusts während des Ausbruchs von Verlusten während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="0af91-142">Average density of packet Loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-143"><strong>BurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-143"><strong>BurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-144">int</span><span class="sxs-lookup"><span data-stu-id="0af91-144">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-145">Durchschnittliche Dauer des Paketverlusts während des Ausbruchs von Verlusten während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="0af91-145">Average duration of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-146"><strong>BurstGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-146"><strong>BurstGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-147">Dezimal (9; 4)</span><span class="sxs-lookup"><span data-stu-id="0af91-147">decimal(9,4)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-148">Durchschnittliche Dichte des Paketverlusts bei Lücken zwischen Bursts des Paketverlusts.</span><span class="sxs-lookup"><span data-stu-id="0af91-148">Average density of packet loss during gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-149"><strong>BurstGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-149"><strong>BurstGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-150">int</span><span class="sxs-lookup"><span data-stu-id="0af91-150">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-151">Durchschnittliche Dauer von Lücken zwischen Bursts des Paketverlusts.</span><span class="sxs-lookup"><span data-stu-id="0af91-151">Average duration of gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-152"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-152"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-153">Int</span><span class="sxs-lookup"><span data-stu-id="0af91-153">Int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-154">Die Anzahl der Pakete für den Audiostream.</span><span class="sxs-lookup"><span data-stu-id="0af91-154">Packet count for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-155"><strong>Bandbreite</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-155"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-156">Int</span><span class="sxs-lookup"><span data-stu-id="0af91-156">Int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-157">Bandbreiten Schätzungen für den Audiostream.</span><span class="sxs-lookup"><span data-stu-id="0af91-157">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-158"><strong>DegradationAvg</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-158"><strong>DegradationAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-159">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="0af91-159">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-160">Netzwerk-Mos-Verschlechterung für den gesamten Anruf.</span><span class="sxs-lookup"><span data-stu-id="0af91-160">Network MOS Degradation for the whole call.</span></span> <span data-ttu-id="0af91-161">Der Bereich ist 0,0 bis 5,0.</span><span class="sxs-lookup"><span data-stu-id="0af91-161">Range is 0.0 to 5.0.</span></span> <span data-ttu-id="0af91-162">Diese Metrik zeigt die Menge, die das Netzwerk Mos aufgrund von Jitter und Paketverlust reduziert wurde.</span><span class="sxs-lookup"><span data-stu-id="0af91-162">This metric shows the amount the Network MOS was reduced because of jitter and packet loss.</span></span> <span data-ttu-id="0af91-163">Für akzeptable Qualität sollte es weniger als 0,5.</span><span class="sxs-lookup"><span data-stu-id="0af91-163">For acceptable quality it should less than 0.5.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-164"><strong>DegradationMax</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-164"><strong>DegradationMax</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-165">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="0af91-165">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-166">Maximaler Netzwerk-Mos-Abbau während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="0af91-166">Maximum Network MOS degradation during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-167"><strong>DegradationJitterAvg</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-167"><strong>DegradationJitterAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-168">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="0af91-168">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-169">Netzwerk-Mos-Beeinträchtigung durch Jitter.</span><span class="sxs-lookup"><span data-stu-id="0af91-169">Network MOS degradation caused by jitter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-170"><strong>DegradationPacketLossAvg</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-170"><strong>DegradationPacketLossAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-171">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="0af91-171">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-172">Netzwerk-Mos-Beeinträchtigung durch Paketverlust.</span><span class="sxs-lookup"><span data-stu-id="0af91-172">Network MOS degradation caused by packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-173"><strong>AudioPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-173"><strong>AudioPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-174">int</span><span class="sxs-lookup"><span data-stu-id="0af91-174">int</span></span></p></td>
<td><p><span data-ttu-id="0af91-175">Fremd</span><span class="sxs-lookup"><span data-stu-id="0af91-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0af91-176">Der für den Anruf verwendete Audiocodec, auf den von der PayloadDescription-Tabelle verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="0af91-176">The audio Codec used for the call, referenced from PayloadDescription Table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-177"><strong>AudioSampleRate</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-177"><strong>AudioSampleRate</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-178">int</span><span class="sxs-lookup"><span data-stu-id="0af91-178">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-179">Abtastrate für den Audiostream.</span><span class="sxs-lookup"><span data-stu-id="0af91-179">Sampling rate for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-180"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-180"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-181">int</span><span class="sxs-lookup"><span data-stu-id="0af91-181">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-182">Roundtrip-Zeit von RTCP-Statistiken</span><span class="sxs-lookup"><span data-stu-id="0af91-182">Round trip time from RTCP statistics.</span></span> <span data-ttu-id="0af91-183">Bei akzeptabler Qualität sollte dies weniger als 100M betragen.</span><span class="sxs-lookup"><span data-stu-id="0af91-183">For acceptable quality this should be less than 100ms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-184"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-184"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-185">int</span><span class="sxs-lookup"><span data-stu-id="0af91-185">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-186">Maximale Roundtrip-Zeit für den Audiostream.</span><span class="sxs-lookup"><span data-stu-id="0af91-186">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-187"><strong>OverallAvgNetworkMOS</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-187"><strong>OverallAvgNetworkMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-188">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="0af91-188">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-189">Durchschnittliche Breitband-Netzwerk-Mos für den Anruf.</span><span class="sxs-lookup"><span data-stu-id="0af91-189">Average wideband Network MOS for the call.</span></span> <span data-ttu-id="0af91-190">Diese Metrik hängt vom verwendeten Paketverlust, Jitter und Codec ab.</span><span class="sxs-lookup"><span data-stu-id="0af91-190">This metric depends on the packet loss, jitter, and codec used.</span></span> <span data-ttu-id="0af91-191">Bereich ist [1,0 bis 5,0].</span><span class="sxs-lookup"><span data-stu-id="0af91-191">Range is [1.0 to 5.0].</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-192"><strong>OverallMinNetworkMOS</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-192"><strong>OverallMinNetworkMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-193">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="0af91-193">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-194">Das Mindest-Breitband-Netzwerk Mos für den Anruf.</span><span class="sxs-lookup"><span data-stu-id="0af91-194">The minimum wideband Network MOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-195"><strong>SendListenMOS</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-195"><strong>SendListenMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-196">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="0af91-196">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-197">Der durchschnittliche prognostizierte Breitband-Abhör-Mos-Score für gesendete Audiodaten, einschließlich der Eigenschaften für Sprachpegel, Geräuschpegel und Aufnahmegeräte.</span><span class="sxs-lookup"><span data-stu-id="0af91-197">The average predicted wideband Listening MOS score for audio sent, including speech level, noise level and capture device characteristics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-198"><strong>SendListenMOSMin</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-198"><strong>SendListenMOSMin</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-199">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="0af91-199">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-200">Die Mindest-SendListenMOS für den Anruf.</span><span class="sxs-lookup"><span data-stu-id="0af91-200">The minimum SendListenMOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-201"><strong>RecvListenMOS</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-201"><strong>RecvListenMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-202">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="0af91-202">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-203">Der durchschnittliche prognostizierte Breitband-Abhör-Mos-Score für vom Netzwerk empfangene Audiosignale, einschließlich Sprachpegel, Geräuschpegel, Codec, Netzwerkbedingungen und Merkmale des Aufnahmegeräts.</span><span class="sxs-lookup"><span data-stu-id="0af91-203">The average predicted wideband Listening MOS score for audio received from the network including speech level, noise level, codec, network conditions and capture device characteristics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-204"><strong>RecvListenMOSMin</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-204"><strong>RecvListenMOSMin</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-205">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="0af91-205">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-206">Die Mindest-RecvListenMOS für den Anruf.</span><span class="sxs-lookup"><span data-stu-id="0af91-206">The minimum RecvListenMOS for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-207"><strong>AudioFECUsed</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-207"><strong>AudioFECUsed</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-208">bit</span><span class="sxs-lookup"><span data-stu-id="0af91-208">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-209">Flag, das angibt, ob Audio FEC für den Anruf verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0af91-209">Flag indicating if audio FEC was used for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-210"><strong>RatioConcealedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-210"><strong>RatioConcealedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-211">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="0af91-211">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-212">Durchschnittliches Verhältnis der verborgenen Samples, die von der audioheilung an typische Samples generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0af91-212">Average ratio of concealed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-213"><strong>RatioStretchedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-213"><strong>RatioStretchedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-214">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="0af91-214">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-215">Durchschnittliches Verhältnis von gedehnten Samples, die von der audioheilung zu typischen Samples generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0af91-215">Average ratio of stretched samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-216"><strong>RatioCompressedSamplesAvg</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-216"><strong>RatioCompressedSamplesAvg</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-217">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="0af91-217">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-218">Durchschnittliches Verhältnis von komprimierten Samples, die von der audioheilung zu typischen Samples generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0af91-218">Average ratio of compressed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-219"><strong>Inbound</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-219"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-220">bit</span><span class="sxs-lookup"><span data-stu-id="0af91-220">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-221">Datenstrom auf Empfängerseite wird empfangen.</span><span class="sxs-lookup"><span data-stu-id="0af91-221">Stream data on receiver side is received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-222"><strong>Ausgehend</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-222"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-223">bit</span><span class="sxs-lookup"><span data-stu-id="0af91-223">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-224">Datenstrom auf Absenderseite wird empfangen.</span><span class="sxs-lookup"><span data-stu-id="0af91-224">Stream data on sender side is received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-225"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-225"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-226">bit</span><span class="sxs-lookup"><span data-stu-id="0af91-226">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="0af91-227">1 bedeutet, dass die Datenstrom Richtung vom Aufrufer an den aufgerufenen gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="0af91-227">1 means the stream direction is from the caller to the callee.</span></span></p>
<p><span data-ttu-id="0af91-228">0 bedeutet, dass die Datenstrom Richtung vom aufgerufenen zum Aufrufer ist.</span><span class="sxs-lookup"><span data-stu-id="0af91-228">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-229"><strong>JitterInterArrivalSD</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-229"><strong>JitterInterArrivalSD</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-230">float</span><span class="sxs-lookup"><span data-stu-id="0af91-230">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-231">Standard Abweichung für Jitter-Ankunftszeiten.</span><span class="sxs-lookup"><span data-stu-id="0af91-231">Standard deviation for jitter arrival times.</span></span></p>
<p><span data-ttu-id="0af91-232">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-232">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-233"><strong>ConcealRatioMax</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-233"><strong>ConcealRatioMax</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-234">float</span><span class="sxs-lookup"><span data-stu-id="0af91-234">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-235">Maximales Verhältnis von Paketen, die vom Heiler verborgen sind.</span><span class="sxs-lookup"><span data-stu-id="0af91-235">Maximum ratio of packets concealed by the healer.</span></span></p>
<p><span data-ttu-id="0af91-236">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-236">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-237"><strong>ConcealRatioSD</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-237"><strong>ConcealRatioSD</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-238">float</span><span class="sxs-lookup"><span data-stu-id="0af91-238">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-239">Standard Abweichung für das Verhältnis von Paketen, die vom Heiler verborgen sind.</span><span class="sxs-lookup"><span data-stu-id="0af91-239">Standard deviation for the ratio of packets concealed by the healer.</span></span></p>
<p><span data-ttu-id="0af91-240">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-240">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-241"><strong>HealerPacketDropRatio</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-241"><strong>HealerPacketDropRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-242">float</span><span class="sxs-lookup"><span data-stu-id="0af91-242">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-243">Das Verhältnis der vom Heiler abgegebenen Pakete im Vergleich zur Gesamtzahl der empfangenen Pakete.</span><span class="sxs-lookup"><span data-stu-id="0af91-243">Ratio of packets dropped by the healer compared to the total number of packets received.</span></span></p>
<p><span data-ttu-id="0af91-244">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-244">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-245"><strong>HealerFECPacketUsedRatio</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-245"><strong>HealerFECPacketUsedRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-246">float</span><span class="sxs-lookup"><span data-stu-id="0af91-246">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-247">Verhältnis der verwendeten Forward-Fehlerkorrektur Pakete im Vergleich zur Gesamtzahl der empfangenen Pakete.</span><span class="sxs-lookup"><span data-stu-id="0af91-247">Ratio of used forward error correction packets compared to the total number of packets received.</span></span></p>
<p><span data-ttu-id="0af91-248">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-248">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-249"><strong>MaxCompressedSamples</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-249"><strong>MaxCompressedSamples</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-250">float</span><span class="sxs-lookup"><span data-stu-id="0af91-250">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-251">Die maximale Anzahl von Audiopaketen, die vom Heiler komprimiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0af91-251">Maximum number of audio packets that were compressed by the healer.</span></span></p>
<p><span data-ttu-id="0af91-252">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-252">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-253"><strong>LossCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-253"><strong>LossCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-254">float</span><span class="sxs-lookup"><span data-stu-id="0af91-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-255">Gibt den Prozentsatz der Zeit an, zu der sich der Anruf in einem Engpass Zustand befand.</span><span class="sxs-lookup"><span data-stu-id="0af91-255">Indicates the percentage of the time when the call was in a loss congestion state.</span></span></p>
<p><span data-ttu-id="0af91-256">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-256">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-257"><strong>DelayCongestionPercent</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-257"><strong>DelayCongestionPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-258">float</span><span class="sxs-lookup"><span data-stu-id="0af91-258">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-259">Gibt den Prozentsatz des Anrufs an, während dessen Überlastung durch das verspätete Eintreffen von Netzwerkpaketen verursacht wurde.</span><span class="sxs-lookup"><span data-stu-id="0af91-259">Indicates the percentage of the call during which congestion was caused by the delayed arrival of network packets.</span></span></p>
<p><span data-ttu-id="0af91-260">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-260">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-261"><strong>ContentionDetectedPercent</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-261"><strong>ContentionDetectedPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-262">float</span><span class="sxs-lookup"><span data-stu-id="0af91-262">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-263">Gibt den Prozentsatz der Zeit an, zu der der Anruf im Wettbewerb um Netzwerkressourcen erfolgte.</span><span class="sxs-lookup"><span data-stu-id="0af91-263">Indicates the percentage of the time when the call was competing for network resources.</span></span></p>
<p><span data-ttu-id="0af91-264">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-264">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-265"><strong>BandwidthEstMin</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-265"><strong>BandwidthEstMin</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-266">int</span><span class="sxs-lookup"><span data-stu-id="0af91-266">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-267">Minimaler Grad der Bandbreitenschätzung, gemessen während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="0af91-267">Minimum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="0af91-268">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-268">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-269"><strong>BandwidthEstMax</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-269"><strong>BandwidthEstMax</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-270">int</span><span class="sxs-lookup"><span data-stu-id="0af91-270">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-271">Maximale Menge an Bandbreitenschätzung, die während des Anrufs gemessen wurde.</span><span class="sxs-lookup"><span data-stu-id="0af91-271">Maximum amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="0af91-272">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-272">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-273"><strong>BandwidthEstStdDev</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-273"><strong>BandwidthEstStdDev</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-274">int</span><span class="sxs-lookup"><span data-stu-id="0af91-274">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-275">Standard Abweichung der Bandbreitenschätzung, die während des Anrufs gemessen wurde.</span><span class="sxs-lookup"><span data-stu-id="0af91-275">Standard deviation of the bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="0af91-276">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-276">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-277"><strong>BandwidthEstAvge</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-277"><strong>BandwidthEstAvge</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-278">int</span><span class="sxs-lookup"><span data-stu-id="0af91-278">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-279">Durchschnittliche Menge an Bandbreitenschätzung, die während des Anrufs gemessen wurde.</span><span class="sxs-lookup"><span data-stu-id="0af91-279">Average amount of bandwidth estimation measured during the call.</span></span></p>
<p><span data-ttu-id="0af91-280">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-280">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-281"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-281"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-282">float</span><span class="sxs-lookup"><span data-stu-id="0af91-282">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-283">Gesamtzahl der unidirektionalen Latenzzeit.</span><span class="sxs-lookup"><span data-stu-id="0af91-283">Total amount of one-way latency.</span></span> <span data-ttu-id="0af91-284">Die relative unidirektionale Latenz misst die Verzögerung zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="0af91-284">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="0af91-285">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-285">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-286"><strong>RelativeOneWayAverage</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-286"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-287">float</span><span class="sxs-lookup"><span data-stu-id="0af91-287">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-288">Durchschnittliche Anzahl der unidirektionalen Latenzzeit.</span><span class="sxs-lookup"><span data-stu-id="0af91-288">Average amount of one-way latency.</span></span> <span data-ttu-id="0af91-289">Die relative unidirektionale Latenz misst die Verzögerung zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="0af91-289">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="0af91-290">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-290">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-291"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-291"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-292">float</span><span class="sxs-lookup"><span data-stu-id="0af91-292">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-293">Maximale Anzahl von unidirektionalen Latenzzeiten.</span><span class="sxs-lookup"><span data-stu-id="0af91-293">Maximum amount of one-way latency.</span></span> <span data-ttu-id="0af91-294">Die relative unidirektionale Latenz misst die Verzögerung zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="0af91-294">Relative one-way latency measures the delay between the client and the server.</span></span></p>
<p><span data-ttu-id="0af91-295">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-295">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-296"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-296"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-297">int</span><span class="sxs-lookup"><span data-stu-id="0af91-297">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-298">Gesamtzahl der einseitigen Burst-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="0af91-298">Total one-way burst occurrences.</span></span> <span data-ttu-id="0af91-299">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen.</span><span class="sxs-lookup"><span data-stu-id="0af91-299">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="0af91-300">Diese Metrik misst den Datenfluss zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="0af91-300">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="0af91-301">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-301">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-302"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-302"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-303">float</span><span class="sxs-lookup"><span data-stu-id="0af91-303">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-304">Totale unidirektionale Burst Dichte.</span><span class="sxs-lookup"><span data-stu-id="0af91-304">Total one-way burst density.</span></span> <span data-ttu-id="0af91-305">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen.</span><span class="sxs-lookup"><span data-stu-id="0af91-305">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="0af91-306">Diese Metrik misst den Datenfluss zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="0af91-306">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="0af91-307">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-307">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-308"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-308"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-309">float</span><span class="sxs-lookup"><span data-stu-id="0af91-309">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-310">Gesamtdauer des einseitigen Bursts.</span><span class="sxs-lookup"><span data-stu-id="0af91-310">Total one-way burst duration.</span></span> <span data-ttu-id="0af91-311">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen.</span><span class="sxs-lookup"><span data-stu-id="0af91-311">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="0af91-312">Diese Metrik misst den Datenfluss zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="0af91-312">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="0af91-313">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-313">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-314"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-314"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-315">int</span><span class="sxs-lookup"><span data-stu-id="0af91-315">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-316">Gesamtanzahl der einseitigen Lücken.</span><span class="sxs-lookup"><span data-stu-id="0af91-316">Total one-way gap occurrences.</span></span> <span data-ttu-id="0af91-317">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen. Lücken deuten auf Verzögerungen zwischen diesen Bursts hin.</span><span class="sxs-lookup"><span data-stu-id="0af91-317">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="0af91-318">Diese Metrik misst den Datenfluss zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="0af91-318">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="0af91-319">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-319">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-320"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-320"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-321">float</span><span class="sxs-lookup"><span data-stu-id="0af91-321">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-322">Gesamtdichte für einseitigen Abstand.</span><span class="sxs-lookup"><span data-stu-id="0af91-322">Total one-way gap density.</span></span> <span data-ttu-id="0af91-323">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen. Lücken deuten auf Verzögerungen zwischen diesen Bursts hin.</span><span class="sxs-lookup"><span data-stu-id="0af91-323">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="0af91-324">Diese Metrik misst den Datenfluss zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="0af91-324">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="0af91-325">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-325">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-326"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-326"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-327">float</span><span class="sxs-lookup"><span data-stu-id="0af91-327">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-328">Gesamtdauer der einseitigen Lücke</span><span class="sxs-lookup"><span data-stu-id="0af91-328">Total one-way gap duration.</span></span> <span data-ttu-id="0af91-329">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen. Lücken deuten auf Verzögerungen zwischen diesen Bursts hin.</span><span class="sxs-lookup"><span data-stu-id="0af91-329">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="0af91-330">Diese Metrik misst den Datenfluss zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="0af91-330">This metric measures data flow between the client and the server.</span></span></p>
<p><span data-ttu-id="0af91-331">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-331">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-332"><strong>DecodeStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-332"><strong>DecodeStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-333">float</span><span class="sxs-lookup"><span data-stu-id="0af91-333">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-334">Prozentsatz des Anrufs, der als Stereo decodiert wurde.</span><span class="sxs-lookup"><span data-stu-id="0af91-334">Percentage of the call decoded as stereo.</span></span></p>
<p><span data-ttu-id="0af91-335">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-335">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-336"><strong>AecRenderStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-336"><strong>AecRenderStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-337">float</span><span class="sxs-lookup"><span data-stu-id="0af91-337">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-338">Prozentsatz des Anrufs, der von der akustischen Echounterdrückung als Stereo gerendert wird.</span><span class="sxs-lookup"><span data-stu-id="0af91-338">Percentage of the call rendered as stereo by the acoustic echo canceller.</span></span></p>
<p><span data-ttu-id="0af91-339">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-339">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-340"><strong>AudioPostFECPLR</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-340"><strong>AudioPostFECPLR</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-341">float</span><span class="sxs-lookup"><span data-stu-id="0af91-341">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-342">Die Paketverlustrate, nachdem die weiter Leitungsfehler Korrektur angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="0af91-342">Packet loss rate after forward error correction has been applied.</span></span></p>
<p><span data-ttu-id="0af91-343">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-343">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0af91-344"><strong>EncodeStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-344"><strong>EncodeStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-345">float</span><span class="sxs-lookup"><span data-stu-id="0af91-345">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-346">Prozentsatz des als Stereo codierten Anrufs.</span><span class="sxs-lookup"><span data-stu-id="0af91-346">Percentage of the call encoded as stereo.</span></span></p>
<p><span data-ttu-id="0af91-347">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-347">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0af91-348"><strong>AecCaptureStereoPercent</strong></span><span class="sxs-lookup"><span data-stu-id="0af91-348"><strong>AecCaptureStereoPercent</strong></span></span></p></td>
<td><p><span data-ttu-id="0af91-349">float</span><span class="sxs-lookup"><span data-stu-id="0af91-349">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0af91-350">Prozentsatz des Anrufs, der von der akustischen Echounterdrückung als Stereo aufgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="0af91-350">Percentage of the call captured as stereo by the acoustic echo canceller.</span></span></p>
<p><span data-ttu-id="0af91-351">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0af91-351">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0af91-352">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0af91-352">


</div>

<span> </span>

</div>

</div>

</span></span></div>

