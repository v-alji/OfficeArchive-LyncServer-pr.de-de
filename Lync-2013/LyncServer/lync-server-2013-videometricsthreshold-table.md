---
title: 'Lync Server 2013: VideoMetricsThreshold-Tabelle'
description: 'Lync Server 2013: VideoMetricsThreshold-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoMetricsThreshold table
ms:assetid: 2e2f4711-35ba-48c6-b15b-5aba61c4eb75
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204778(v=OCS.15)
ms:contentKeyID: 48183736
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 93cdd6fb4c3c54ac1470499490f36fee87ba283d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438869"
---
# <a name="videometricsthreshold-table-in-lync-server-2013"></a><span data-ttu-id="7abaf-103">VideoMetricsThreshold-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7abaf-103">VideoMetricsThreshold table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7abaf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7abaf-104">

<span> </span></span></span>

<span data-ttu-id="7abaf-105">_**Letztes Änderungsdatum des Themas:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="7abaf-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="7abaf-106">Die VideoMetricsThreshold-Tabelle enthält die optimalen und akzeptablen Werte für die Qualität der bei Videoanrufen verwendeten Metriken für die Erfahrung.</span><span class="sxs-lookup"><span data-stu-id="7abaf-106">The VideoMetricsThreshold table contains optimal and acceptable values for the Quality of Experience metrics used with video calls.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7abaf-107"><strong>Spalte</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-107"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="7abaf-108"><strong>Datentyp</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-108"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="7abaf-109"><strong>Schlüssel/Index</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-109"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="7abaf-110"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-110"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7abaf-111"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-111"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="7abaf-112">int</span><span class="sxs-lookup"><span data-stu-id="7abaf-112">int</span></span></p></td>
<td><p><span data-ttu-id="7abaf-113">Primary</span><span class="sxs-lookup"><span data-stu-id="7abaf-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="7abaf-114">Der Typ des Anrufs, der getätigt wurde.</span><span class="sxs-lookup"><span data-stu-id="7abaf-114">Type of call that was placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7abaf-115"><strong>VideoPostFECPLROptimal</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-115"><strong>VideoPostFECPLROptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="7abaf-116">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="7abaf-116">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7abaf-117">Der Standardwert ist 0,05.</span><span class="sxs-lookup"><span data-stu-id="7abaf-117">The default value is 0.05.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7abaf-118"><strong>VideoPostFECPLRAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-118"><strong>VideoPostFECPLRAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="7abaf-119">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="7abaf-119">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7abaf-120">Der Standardwert ist 0,10.</span><span class="sxs-lookup"><span data-stu-id="7abaf-120">The default value is 0.10.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7abaf-121"><strong>VideoLocalFrameLostPercentageAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-121"><strong>VideoLocalFrameLostPercentageAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="7abaf-122">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="7abaf-122">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7abaf-123">Der Standardwert ist 5,0.</span><span class="sxs-lookup"><span data-stu-id="7abaf-123">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7abaf-124"><strong>VideoLocalFrameLostPercentageAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-124"><strong>VideoLocalFrameLostPercentageAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="7abaf-125">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="7abaf-125">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7abaf-126">Der Standardwert ist 10,0.</span><span class="sxs-lookup"><span data-stu-id="7abaf-126">The default value is 10.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7abaf-127"><strong>RecvFrameRateAverageOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-127"><strong>RecvFrameRateAverageOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="7abaf-128">Dezimal (9; 4)</span><span class="sxs-lookup"><span data-stu-id="7abaf-128">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7abaf-129">Der Standardwert ist 12,0000.</span><span class="sxs-lookup"><span data-stu-id="7abaf-129">The default value is 12.0000.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7abaf-130"><strong>RecvFramerateAverageAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-130"><strong>RecvFramerateAverageAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="7abaf-131">Dezimal (9; 4)</span><span class="sxs-lookup"><span data-stu-id="7abaf-131">decimal(9,4)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7abaf-132">Der Standardwert ist 7,0000.</span><span class="sxs-lookup"><span data-stu-id="7abaf-132">The default value is 7.0000.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7abaf-133"><strong>LowFrameRateCallPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-133"><strong>LowFrameRateCallPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="7abaf-134">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="7abaf-134">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7abaf-135">Der Standardwert ist 5,0.</span><span class="sxs-lookup"><span data-stu-id="7abaf-135">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7abaf-136"><strong>LowFrameRateCallPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-136"><strong>LowFrameRateCallPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="7abaf-137">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="7abaf-137">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7abaf-138">Der Standardwert ist 10.0/</span><span class="sxs-lookup"><span data-stu-id="7abaf-138">The default value is 10.0/</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7abaf-139"><strong>LowResolutionCallPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-139"><strong>LowResolutionCallPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="7abaf-140">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="7abaf-140">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7abaf-141">Der Standardwert ist 5,0.</span><span class="sxs-lookup"><span data-stu-id="7abaf-141">The default value is 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7abaf-142"><strong>LowResolutionCallPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-142"><strong>LowResolutionCallPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="7abaf-143">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="7abaf-143">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7abaf-144">Der Standardwert ist 10,0.</span><span class="sxs-lookup"><span data-stu-id="7abaf-144">The default value is 10.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7abaf-145"><strong>VideoPacketLossRateOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-145"><strong>VideoPacketLossRateOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="7abaf-146">foat</span><span class="sxs-lookup"><span data-stu-id="7abaf-146">foat</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7abaf-147">Der Standardwert ist 0,05.</span><span class="sxs-lookup"><span data-stu-id="7abaf-147">The default value is 0.05.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7abaf-148"><strong>VideoPacketLossRateAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-148"><strong>VideoPacketLossRateAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="7abaf-149">float</span><span class="sxs-lookup"><span data-stu-id="7abaf-149">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7abaf-150">Der Standardwert ist 0,10.</span><span class="sxs-lookup"><span data-stu-id="7abaf-150">The default value is 0.10.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7abaf-151"><strong>VideoFrameRateAvgOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-151"><strong>VideoFrameRateAvgOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="7abaf-152">float</span><span class="sxs-lookup"><span data-stu-id="7abaf-152">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7abaf-153">Der Standardwert ist 12.</span><span class="sxs-lookup"><span data-stu-id="7abaf-153">The default value is 12.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7abaf-154"><strong>VideoFrameRateAvgAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-154"><strong>VideoFrameRateAvgAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="7abaf-155">float</span><span class="sxs-lookup"><span data-stu-id="7abaf-155">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7abaf-156">Der Standardwert ist 7.</span><span class="sxs-lookup"><span data-stu-id="7abaf-156">The default value is 7.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7abaf-157"><strong>DynamicCapabilityPercentOptimal</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-157"><strong>DynamicCapabilityPercentOptimal</strong></span></span></p></td>
<td><p><span data-ttu-id="7abaf-158">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="7abaf-158">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7abaf-159">Der Standardwert ist 5,00.</span><span class="sxs-lookup"><span data-stu-id="7abaf-159">The default value is 5.00.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7abaf-160"><strong>DynamicCapabilityPercentAcceptable</strong></span><span class="sxs-lookup"><span data-stu-id="7abaf-160"><strong>DynamicCapabilityPercentAcceptable</strong></span></span></p></td>
<td><p><span data-ttu-id="7abaf-161">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="7abaf-161">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7abaf-162">Der Standardwert ist 10,00.</span><span class="sxs-lookup"><span data-stu-id="7abaf-162">The default value is 10.00.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7abaf-163">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7abaf-163">


</div>

<span> </span>

</div>

</div>

</span></span></div>

