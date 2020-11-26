---
title: 'Lync Server 2013: AppSharingMetricsThreshold-Tabelle'
description: 'Lync Server 2013: AppSharingMetricsThreshold-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AppSharingMetricsThreshold table
ms:assetid: 782cfab9-01a6-4843-aea1-28f47b0b51f7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205018(v=OCS.15)
ms:contentKeyID: 48184556
ms.date: 12/09/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 092c7d08026e6b736b81043a71b4ecaabc4d5f1b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439872"
---
# <a name="appsharingmetricsthreshold-table-in-lync-server-2013"></a><span data-ttu-id="3e0d2-103">AppSharingMetricsThreshold-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e0d2-103">AppSharingMetricsThreshold table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3e0d2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3e0d2-104">

<span> </span></span></span>

<span data-ttu-id="3e0d2-105">_**Letztes Änderungsdatum des Themas:** 2015-12-08_</span><span class="sxs-lookup"><span data-stu-id="3e0d2-105">_**Topic Last Modified:** 2015-12-08_</span></span>

<span data-ttu-id="3e0d2-106">Die AppSharingMetricsThreshold-Tabelle enthält optimale und akzeptable Werte für die Qualität der Erfahrungs Metrik, die bei der Anwendungsfreigabe verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-106">The AppSharingMetricsThreshold table contains optimal and acceptable values for the Quality of Experience metrics used with application sharing.</span></span> <span data-ttu-id="3e0d2-107">Diese Schwellenwerte werden verwendet, um festzustellen, ob die Anwendungsfreigabe Erfahrung als "schlecht" klassifiziert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-107">These thresholds are used to determine if the application sharing experience should be classified as poor.</span></span>

<span data-ttu-id="3e0d2-108">Diese Tabelle wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e0d2-109"><strong>Spalte</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="3e0d2-110"><strong>Datentyp</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="3e0d2-111"><strong>Schlüssel/Index</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="3e0d2-112"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e0d2-113"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-113"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="3e0d2-114">int</span><span class="sxs-lookup"><span data-stu-id="3e0d2-114">int</span></span></p></td>
<td><p><span data-ttu-id="3e0d2-115">Primary</span><span class="sxs-lookup"><span data-stu-id="3e0d2-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="3e0d2-116">Der Typ des Anrufs, der getätigt wurde.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-116">Type of call that was placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e0d2-117"><strong>AppliedBandwidthLimitOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-117"><strong>AppliedBandwidthLimitOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="3e0d2-118">int</span><span class="sxs-lookup"><span data-stu-id="3e0d2-118">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3e0d2-119">Optimale Bandbreitenbeschränkung bei der Anwendungsfreigabe.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-119">Optimal bandwidth limitation for application sharing.</span></span> <span data-ttu-id="3e0d2-120">Der Standardwert ist 1 Million.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-120">The default value is 1000000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e0d2-121"><strong>AppliedBandwidthLimitAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-121"><strong>AppliedBandwidthLimitAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="3e0d2-122">int</span><span class="sxs-lookup"><span data-stu-id="3e0d2-122">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3e0d2-123">Zulässige Bandbreitenbeschränkung für die Anwendungsfreigabe.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-123">Acceptable bandwidth limitation for application sharing.</span></span> <span data-ttu-id="3e0d2-124">Der Standardwert ist 500000.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-124">The default value is 500000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e0d2-125"><strong>SpoiledTilePercentTotalOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-125"><strong>SpoiledTilePercentTotalOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="3e0d2-126">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="3e0d2-126">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3e0d2-127">Optimaler Prozentsatz für "verwöhnte" Kacheln für die Klassifizierung einer Anwendungsfreigabe Qualität.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-127">Optimal percentage rate for “spoiled” tiles for classifying an Application Sharing quality.</span></span> <span data-ttu-id="3e0d2-128">Dieser Wert ist der Prozentsatz des Inhalts des mitbenutzenden, der den Betrachter nicht erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-128">This value is the percentage of the content from the sharer that did not reach the viewer.</span></span> <span data-ttu-id="3e0d2-129">Inhalte werden möglicherweise verworfen (oder verdorben), wenn der mitbenutzende die Kacheln aus der grafikquelle abwirft oder die ASMCU-Kacheln Kacheln von Sharer abwirft.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-129">Content may be discarded (or spoiled) when the sharer discards tiles from the graphics source or the ASMCU tiles discards tiles from Sharer respectively.</span></span> <span data-ttu-id="3e0d2-130">Der Standardwert ist 11 Prozent.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-130">The default value is 11 percent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e0d2-131"><strong>SpoiledTilePercentTotalAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-131"><strong>SpoiledTilePercentTotalAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="3e0d2-132">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="3e0d2-132">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3e0d2-133">cceptable-Prozentsatz für "verdorbene" Kacheln für die Klassifizierung einer Anwendungsfreigabe Qualität.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-133">cceptable percentage rate for “spoiled” tiles for classifying an Application Sharing quality.</span></span> <span data-ttu-id="3e0d2-134">Dieser Wert ist der Prozentsatz des Inhalts des mitbenutzenden, der den Betrachter nicht erreicht hat.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-134">This value is the percentage of the content from the sharer that did not reach the viewer.</span></span> <span data-ttu-id="3e0d2-135">Inhalte werden möglicherweise verworfen (oder verdorben), wenn der mitbenutzende die Kacheln aus der grafikquelle abwirft oder die ASMCU-Kacheln Kacheln von Sharer abwirft.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-135">Content may be discarded (or spoiled) when the sharer discards tiles from the graphics source or the ASMCU tiles discards tiles from Sharer respectively.</span></span> <span data-ttu-id="3e0d2-136">Der Standardwert ist 36 Prozent.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-136">The default value is 36 percent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e0d2-137"><strong>JitterInterArrivalOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-137"><strong>JitterInterArrivalOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="3e0d2-138">int</span><span class="sxs-lookup"><span data-stu-id="3e0d2-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3e0d2-139">Diese Spalte wird in Microsoft lync Server 2013 nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-139">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e0d2-140"><strong>JitterInterArrivalAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-140"><strong>JitterInterArrivalAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="3e0d2-141">int</span><span class="sxs-lookup"><span data-stu-id="3e0d2-141">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3e0d2-142">Diese Spalte wird in Microsoft lync Server 2013 nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-142">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e0d2-143"><strong>RelativeOneWayBurstDensityOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-143"><strong>RelativeOneWayBurstDensityOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="3e0d2-144">float</span><span class="sxs-lookup"><span data-stu-id="3e0d2-144">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3e0d2-145">Diese Spalte wird in Microsoft lync Server 2013 nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-145">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e0d2-146"><strong>RelativeOneWayBurstDensityAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-146"><strong>RelativeOneWayBurstDensityAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="3e0d2-147">float</span><span class="sxs-lookup"><span data-stu-id="3e0d2-147">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3e0d2-148">Diese Spalte wird in Microsoft lync Server 2013 nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-148">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e0d2-149"><strong>RDPTileProcessingLatencyBurstDensityOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-149"><strong>RDPTileProcessingLatencyBurstDensityOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="3e0d2-150">float</span><span class="sxs-lookup"><span data-stu-id="3e0d2-150">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3e0d2-151">Diese Spalte wird in Microsoft lync Server 2013 nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-151">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e0d2-152"><strong>RDPTileProcessingLatencyBurstDensityAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-152"><strong>RDPTileProcessingLatencyBurstDensityAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="3e0d2-153">float</span><span class="sxs-lookup"><span data-stu-id="3e0d2-153">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3e0d2-154">Diese Spalte wird in Microsoft lync Server 2013 nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-154">This column is not used in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e0d2-155"><strong>RelativeOneWayAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-155"><strong>RelativeOneWayAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="3e0d2-156">float</span><span class="sxs-lookup"><span data-stu-id="3e0d2-156">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3e0d2-157">Optimaler Wert für die relative unidirektionale Verzögerung zwischen den beiden Medien Endpunkten, die an der Anwendungsfreigabe beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-157">Optimal value for the relative one-way delay between the two media endpoints involved in the application sharing.</span></span> <span data-ttu-id="3e0d2-158">Dies ist ein Single-Hop-Latenzmaß.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-158">This is a single-hop latency measure.</span></span> <span data-ttu-id="3e0d2-159">Der Standardwert ist 1,0 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-159">The default value is 1.0 seconds.</span></span></p>
<p><span data-ttu-id="3e0d2-160">Die Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-160">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e0d2-161"><strong>RelativeOneWayAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-161"><strong>RelativeOneWayAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="3e0d2-162">float</span><span class="sxs-lookup"><span data-stu-id="3e0d2-162">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3e0d2-163">Optimaler Wert für die relative unidirektionale Verzögerung zwischen den beiden Medien Endpunkten, die an der Anwendungsfreigabe beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-163">Optimal value for the relative one-way delay between the two media endpoints involved in the application sharing.</span></span> <span data-ttu-id="3e0d2-164">Dies ist ein Single-Hop-Latenzmaß.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-164">This is a single-hop latency measure.</span></span> <span data-ttu-id="3e0d2-165">Der Standardwert ist 1,75 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-165">The default value is 1.75 seconds.</span></span></p>
<p><span data-ttu-id="3e0d2-166">Die Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-166">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e0d2-167"><strong>RDPTileProcessingLatencyAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-167"><strong>RDPTileProcessingLatencyAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="3e0d2-168">float</span><span class="sxs-lookup"><span data-stu-id="3e0d2-168">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3e0d2-169">Optimaler Wert der durchschnittlichen Verarbeitungs Wartezeit für RDP-Kacheln auf dem AS-Konferenz Server über die Dauer der Anzeige Sitzung.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-169">Optimal value of the average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session.</span></span> <span data-ttu-id="3e0d2-170">Latenz ist der Zeitunterschied zwischen dem Codieren des Start Frames auf dem Server (Sharer oder MCU, je nach Szenario) und dem gleichen Start Frame im Viewer.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-170">Latency is the time difference between when the Start Frame is encoded on the server (sharer or MCU depending on the scenario) and the same Start Frame is decoded on the viewer.</span></span></p>
<p><span data-ttu-id="3e0d2-171">Ein hoher Durchschnitt zeigt eine längere Verzögerung bei der Anzeige an.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-171">A high average reflects a longer delay in the viewing experience.</span></span> <span data-ttu-id="3e0d2-172">Ein überlasteter Konferenzserver zeigt gegebenenfalls höhere durchschnittliche Verzögerungen an.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-172">An overloaded conferencing server may experience higher average delays.</span></span> <span data-ttu-id="3e0d2-173">Der Standardwert ist 200M.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-173">The default value is 200ms.</span></span></p>
<p><span data-ttu-id="3e0d2-174">Die Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-174">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e0d2-175"><strong>RDPTileProcessingLatencyAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="3e0d2-175"><strong>RDPTileProcessingLatencyAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="3e0d2-176">float</span><span class="sxs-lookup"><span data-stu-id="3e0d2-176">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3e0d2-177">Akzeptabler Wert der durchschnittlichen Verarbeitungs Wartezeit für RDP-Kacheln auf dem AS-Konferenz Server über die Dauer der Anzeige Sitzung.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-177">Acceptable value of the average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session.</span></span> <span data-ttu-id="3e0d2-178">Latenz ist der Zeitunterschied zwischen dem Codieren des Start Frames auf dem Server (Sharer oder MCU, je nach Szenario) und dem gleichen Start Frame im Viewer.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-178">Latency is the time difference between when the Start Frame is encoded on the server (sharer or MCU depending on the scenario) and the same Start Frame is decoded on the viewer.</span></span></p>
<p><span data-ttu-id="3e0d2-179">Ein hoher Durchschnitt zeigt eine längere Verzögerung bei der Anzeige an.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-179">A high average reflects a longer delay in the viewing experience.</span></span> <span data-ttu-id="3e0d2-180">Ein überlasteter Konferenzserver zeigt gegebenenfalls höhere durchschnittliche Verzögerungen an.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-180">An overloaded conferencing server may experience higher average delays.</span></span> <span data-ttu-id="3e0d2-181">Der Standardwert ist 200M.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-181">The default value is 200ms.</span></span></p>
<p><span data-ttu-id="3e0d2-182">Die Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="3e0d2-182">The column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3e0d2-183">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3e0d2-183">


</div>

<span> </span>

</div>

</div>

</span></span></div>

