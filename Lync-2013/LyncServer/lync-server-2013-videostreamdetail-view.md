---
title: 'Lync Server 2013: VideoStreamDetail-Ansicht'
description: 'Lync Server 2013: VideoStreamDetail-Ansicht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VideoStreamDetail view
ms:assetid: ec8c45e1-307d-40ec-a75e-6083306105f2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721928(v=OCS.15)
ms:contentKeyID: 49733863
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3f420c292627d15fd0d54f2eba01c565a49a72d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443426"
---
# <a name="videostreamdetail-view-in-lync-server-2013"></a><span data-ttu-id="34555-103">VideoStreamDetail-Ansicht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="34555-103">VideoStreamDetail view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="34555-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="34555-104">

<span> </span></span></span>

<span data-ttu-id="34555-105">_**Letztes Änderungsdatum des Themas:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="34555-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="34555-106">In der VideoStreamDetail-Ansicht werden Informationen zu den einzelnen Videodatenströmen in der Datenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="34555-106">The VideoStreamDetail View stores information about each video stream in the database.</span></span> <span data-ttu-id="34555-107">Diese Ansicht wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="34555-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="34555-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="34555-108">Column</span></span></th>
<th><span data-ttu-id="34555-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="34555-109">Data Type</span></span></th>
<th><span data-ttu-id="34555-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="34555-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="34555-111">SessionTime</span><span class="sxs-lookup"><span data-stu-id="34555-111">SessionTime</span></span></p></td>
<td><p><span data-ttu-id="34555-112">datetime</span><span class="sxs-lookup"><span data-stu-id="34555-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="34555-113">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="34555-113">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-114">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="34555-114">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="34555-115">int</span><span class="sxs-lookup"><span data-stu-id="34555-115">int</span></span></p></td>
<td><p><span data-ttu-id="34555-116">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="34555-116">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-117">MediaLineLabel</span><span class="sxs-lookup"><span data-stu-id="34555-117">MediaLineLabel</span></span></p></td>
<td><p><span data-ttu-id="34555-118">tinyint</span><span class="sxs-lookup"><span data-stu-id="34555-118">tinyint</span></span></p></td>
<td><p><span data-ttu-id="34555-119">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="34555-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-120">Datenstrom-Nr</span><span class="sxs-lookup"><span data-stu-id="34555-120">StreamId</span></span></p></td>
<td><p><span data-ttu-id="34555-121">int</span><span class="sxs-lookup"><span data-stu-id="34555-121">int</span></span></p></td>
<td><p><span data-ttu-id="34555-122">Eindeutige ID innerhalb einer medienzeile</span><span class="sxs-lookup"><span data-stu-id="34555-122">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-123">StartTime</span><span class="sxs-lookup"><span data-stu-id="34555-123">StartTime</span></span></p></td>
<td><p><span data-ttu-id="34555-124">datetime</span><span class="sxs-lookup"><span data-stu-id="34555-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="34555-125">Startzeit der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="34555-125">Start time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-126">EndTime</span><span class="sxs-lookup"><span data-stu-id="34555-126">EndTime</span></span></p></td>
<td><p><span data-ttu-id="34555-127">datetime</span><span class="sxs-lookup"><span data-stu-id="34555-127">datetime</span></span></p></td>
<td><p><span data-ttu-id="34555-128">Endzeit der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="34555-128">End time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-129">CallPriority</span><span class="sxs-lookup"><span data-stu-id="34555-129">CallPriority</span></span></p></td>
<td><p><span data-ttu-id="34555-130">int</span><span class="sxs-lookup"><span data-stu-id="34555-130">int</span></span></p></td>
<td><p><span data-ttu-id="34555-131">Die Priorität des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="34555-131">Priority of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-132">CallerPool</span><span class="sxs-lookup"><span data-stu-id="34555-132">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="34555-133">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="34555-133">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34555-134">FQDN des anrufenden Pools.</span><span class="sxs-lookup"><span data-stu-id="34555-134">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-135">CalleePool</span><span class="sxs-lookup"><span data-stu-id="34555-135">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="34555-136">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="34555-136">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34555-137">FQDN des aufgerufenen Pools.</span><span class="sxs-lookup"><span data-stu-id="34555-137">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-138">Anrufer</span><span class="sxs-lookup"><span data-stu-id="34555-138">Caller</span></span></p></td>
<td><p><span data-ttu-id="34555-139">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="34555-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="34555-140">URI des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="34555-140">Caller’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-141">Callee</span><span class="sxs-lookup"><span data-stu-id="34555-141">Callee</span></span></p></td>
<td><p><span data-ttu-id="34555-142">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="34555-142">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="34555-143">URI des aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="34555-143">Callee’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-144">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="34555-144">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="34555-145">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="34555-145">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34555-146">Benutzer-Agent-Zeichenfolge des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="34555-146">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-147">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="34555-147">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="34555-148">smallint</span><span class="sxs-lookup"><span data-stu-id="34555-148">smallint</span></span></p></td>
<td><p><span data-ttu-id="34555-149">Der Typ des Benutzer-Agents des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="34555-149">Type of caller’s user agent.</span></span> <span data-ttu-id="34555-150">Weitere Informationen finden Sie <a href="lync-server-2013-useragent-table.md">in der UserAgent-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="34555-150">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-151">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="34555-151">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="34555-152">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="34555-152">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="34555-153">Kategorie des Benutzer-Agents des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="34555-153">Category of caller’s user agent.</span></span> <span data-ttu-id="34555-154">Weitere Informationen finden Sie <a href="lync-server-2013-useragentdef-table-qoe.md">in der UserAgentDef-Tabelle (QoE) in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="34555-154">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-155">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="34555-155">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="34555-156">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="34555-156">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34555-157">Benutzer-Agent-Zeichenfolge des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="34555-157">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-158">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="34555-158">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="34555-159">smallint</span><span class="sxs-lookup"><span data-stu-id="34555-159">smallint</span></span></p></td>
<td><p><span data-ttu-id="34555-160">Der Typ des Benutzer-Agents des anrufempfängers.</span><span class="sxs-lookup"><span data-stu-id="34555-160">Type of callee’s user agent.</span></span> <span data-ttu-id="34555-161">Informationen finden Sie <a href="lync-server-2013-useragent-table.md">in der UserAgent-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="34555-161">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-162">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="34555-162">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="34555-163">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="34555-163">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="34555-164">Kategorie des Benutzer-Agents des berufenen</span><span class="sxs-lookup"><span data-stu-id="34555-164">Category of callee’s user agent.</span></span> <span data-ttu-id="34555-165">Informationen hierzu finden Sie <a href="lync-server-2013-useragentdef-table-qoe.md">in der UserAgentDef-Tabelle (QoE) in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="34555-165">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-166">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="34555-166">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="34555-167">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="34555-167">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34555-168">Der Endpunktname des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="34555-168">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-169">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="34555-169">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="34555-170">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="34555-170">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34555-171">Endpunktname des angerufenen</span><span class="sxs-lookup"><span data-stu-id="34555-171">Callee’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-172">Anrufer</span><span class="sxs-lookup"><span data-stu-id="34555-172">CallerOS</span></span></p></td>
<td><p><span data-ttu-id="34555-173">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="34555-173">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="34555-174">Betriebssystem (OS) des Endpunkts des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="34555-174">Operating system (OS) of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-175">CalleeOS</span><span class="sxs-lookup"><span data-stu-id="34555-175">CalleeOS</span></span></p></td>
<td><p><span data-ttu-id="34555-176">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="34555-176">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="34555-177">Betriebssystem (OS) des Endpunkts des aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="34555-177">Operating system (OS) of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-178">CallerCPUName</span><span class="sxs-lookup"><span data-stu-id="34555-178">CallerCPUName</span></span></p></td>
<td><p><span data-ttu-id="34555-179">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="34555-179">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="34555-180">Der CPU-Name des Endpunkts des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="34555-180">CPU name of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-181">CalleeCPUName</span><span class="sxs-lookup"><span data-stu-id="34555-181">CalleeCPUName</span></span></p></td>
<td><p><span data-ttu-id="34555-182">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="34555-182">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="34555-183">Der CPU-Name des Endpunkts des aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="34555-183">CPU name of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-184">CallerCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="34555-184">CallerCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="34555-185">smallint</span><span class="sxs-lookup"><span data-stu-id="34555-185">smallint</span></span></p></td>
<td><p><span data-ttu-id="34555-186">Die Anzahl der CPU-Kerne des Endpunkts des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="34555-186">Number of CPU cores of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-187">CalleeCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="34555-187">CalleeCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="34555-188">smallint</span><span class="sxs-lookup"><span data-stu-id="34555-188">smallint</span></span></p></td>
<td><p><span data-ttu-id="34555-189">Die Anzahl von CPU-Kernen des Endpunkts des aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="34555-189">Number of CPU cores of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-190">CallerCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="34555-190">CallerCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="34555-191">int</span><span class="sxs-lookup"><span data-stu-id="34555-191">int</span></span></p></td>
<td><p><span data-ttu-id="34555-192">CPU-Prozessorgeschwindigkeit des Endpunkts des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="34555-192">CPU processor speed of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-193">CalleeCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="34555-193">CalleeCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="34555-194">int</span><span class="sxs-lookup"><span data-stu-id="34555-194">int</span></span></p></td>
<td><p><span data-ttu-id="34555-195">CPU-Prozessorgeschwindigkeit des Endpunkts des aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="34555-195">CPU processor speed of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-196">CallerVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="34555-196">CallerVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="34555-197">tinyint</span><span class="sxs-lookup"><span data-stu-id="34555-197">tinyint</span></span></p></td>
<td><p><span data-ttu-id="34555-198">Gibt an, ob das System des Anrufers in einer virtualisierten Umgebung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34555-198">Indicates whether the caller’s system is running in a virtualized environment.</span></span> <span data-ttu-id="34555-199">Weitere Informationen finden Sie <a href="lync-server-2013-endpoint-table.md">in der Endpunkt Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="34555-199">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-200">CalleeVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="34555-200">CalleeVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="34555-201">tinyint</span><span class="sxs-lookup"><span data-stu-id="34555-201">tinyint</span></span></p></td>
<td><p><span data-ttu-id="34555-202">Gibt an, ob das System des aufgerufenen in einer virtualisierten Umgebung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="34555-202">Indicates whether the callee’s system is running in a virtualized environment.</span></span> <span data-ttu-id="34555-203">Weitere Informationen finden Sie <a href="lync-server-2013-endpoint-table.md">in der Endpunkt Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="34555-203">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-204">ConnectivityIce</span><span class="sxs-lookup"><span data-stu-id="34555-204">ConnectivityIce</span></span></p></td>
<td><p><span data-ttu-id="34555-205">tinyint</span><span class="sxs-lookup"><span data-stu-id="34555-205">tinyint</span></span></p></td>
<td><p><span data-ttu-id="34555-206">Informationen zu Medien Pfaden, beispielsweise direkt oder weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="34555-206">Information about media path, such as direct or relayed.</span></span> <span data-ttu-id="34555-207">Weitere Informationen finden Sie <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="34555-207">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-208">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="34555-208">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="34555-209">int</span><span class="sxs-lookup"><span data-stu-id="34555-209">int</span></span></p></td>
<td><p><span data-ttu-id="34555-210">Informationen zum Prozess der interaktiven Verbindungseinrichtung (ICE), der unter Bits-Flags für den Aufrufer beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="34555-210">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="34555-211">Ausführliche Informationen finden Sie in der Quality of Experience Monitoring Server Protocol-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="34555-211">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-212">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="34555-212">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="34555-213">int</span><span class="sxs-lookup"><span data-stu-id="34555-213">int</span></span></p></td>
<td><p><span data-ttu-id="34555-214">Informationen zum Prozess der interaktiven Verbindungseinrichtung (ICE), der in den Bits-Flags für den aufgerufenen beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="34555-214">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="34555-215">Ausführliche Informationen finden Sie in der Quality of Experience Monitoring Server Protocol-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="34555-215">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-216">Transport</span><span class="sxs-lookup"><span data-stu-id="34555-216">Transport</span></span></p></td>
<td><p><span data-ttu-id="34555-217">int</span><span class="sxs-lookup"><span data-stu-id="34555-217">int</span></span></p></td>
<td><p><span data-ttu-id="34555-218">Transporttyp: 0 ist UDP, 1 ist TCP.</span><span class="sxs-lookup"><span data-stu-id="34555-218">Transport type: 0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-219">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="34555-219">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="34555-220">var (50)</span><span class="sxs-lookup"><span data-stu-id="34555-220">var(50)</span></span></p></td>
<td><p><span data-ttu-id="34555-221">Die IP-Adresse des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="34555-221">IP address of the caller.</span></span> <span data-ttu-id="34555-222">Hierbei kann es sich entweder um eine IPv4-oder eine IPv6-Adresse handeln.</span><span class="sxs-lookup"><span data-stu-id="34555-222">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-223">CallerPort</span><span class="sxs-lookup"><span data-stu-id="34555-223">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="34555-224">int</span><span class="sxs-lookup"><span data-stu-id="34555-224">int</span></span></p></td>
<td><p><span data-ttu-id="34555-225">Der vom Aufrufer verwendete Port.</span><span class="sxs-lookup"><span data-stu-id="34555-225">Port used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-226">CallerInside</span><span class="sxs-lookup"><span data-stu-id="34555-226">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="34555-227">bit</span><span class="sxs-lookup"><span data-stu-id="34555-227">bit</span></span></p></td>
<td><p><span data-ttu-id="34555-228">Gibt an, ob sich der Anrufer innerhalb des Organisationsnetzwerks befindet.</span><span class="sxs-lookup"><span data-stu-id="34555-228">Indicates whether the caller is inside the organization network.</span></span> <span data-ttu-id="34555-229">1 bedeutet, dass der Anrufer sich innerhalb des Unternehmensnetzwerks befindet, 0 bedeutet, dass sich der Anrufer außerhalb des Netzwerks befindet.</span><span class="sxs-lookup"><span data-stu-id="34555-229">1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-230">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="34555-230">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="34555-231">var (50)</span><span class="sxs-lookup"><span data-stu-id="34555-231">var(50)</span></span></p></td>
<td><p><span data-ttu-id="34555-232">Die IP-Adresse des aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="34555-232">IP address of the callee.</span></span> <span data-ttu-id="34555-233">Hierbei kann es sich entweder um eine IPv4-oder eine IPv6-Adresse handeln.</span><span class="sxs-lookup"><span data-stu-id="34555-233">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-234">CalleePort</span><span class="sxs-lookup"><span data-stu-id="34555-234">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="34555-235">int</span><span class="sxs-lookup"><span data-stu-id="34555-235">int</span></span></p></td>
<td><p><span data-ttu-id="34555-236">Port, der vom aufgerufenen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34555-236">Port used by the callee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-237">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="34555-237">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="34555-238">bit</span><span class="sxs-lookup"><span data-stu-id="34555-238">bit</span></span></p></td>
<td><p><span data-ttu-id="34555-239">Gibt an, ob sich der Aufrufer innerhalb des Organisationsnetzwerks befindet. 1 bedeutet, dass der Anrufer sich innerhalb des Unternehmensnetzwerks befindet, 0 bedeutet, dass der Anrufer sich außerhalb des Netzwerks befindet.</span><span class="sxs-lookup"><span data-stu-id="34555-239">Indicates whether the caller is inside the organization network.1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-240">CallerUserSite</span><span class="sxs-lookup"><span data-stu-id="34555-240">CallerUserSite</span></span></p></td>
<td><p><span data-ttu-id="34555-241">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="34555-241">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="34555-242">Der Name der Website des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="34555-242">Name of the caller’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-243">CallerRegion</span><span class="sxs-lookup"><span data-stu-id="34555-243">CallerRegion</span></span></p></td>
<td><p><span data-ttu-id="34555-244">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="34555-244">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="34555-245">Name des Landes/der Region der Website des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="34555-245">Name of the country/region of the caller’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-246">CalleeUserSite</span><span class="sxs-lookup"><span data-stu-id="34555-246">CalleeUserSite</span></span></p></td>
<td><p><span data-ttu-id="34555-247">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="34555-247">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="34555-248">Name der Website des aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="34555-248">Name of the callee’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-249">CalleeRegion</span><span class="sxs-lookup"><span data-stu-id="34555-249">CalleeRegion</span></span></p></td>
<td><p><span data-ttu-id="34555-250">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="34555-250">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="34555-251">Name des Landes/der Region der Website des berufenen.</span><span class="sxs-lookup"><span data-stu-id="34555-251">Name of the country/region of the callee’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-252">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="34555-252">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="34555-253">var (50)</span><span class="sxs-lookup"><span data-stu-id="34555-253">var(50)</span></span></p></td>
<td><p><span data-ttu-id="34555-254">Die IP-Adresse des A/V-Edgedienst, der vom Aufrufer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34555-254">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="34555-255">Weitere Informationen finden Sie <a href="lync-server-2013-ipaddress-table.md">in der Tabelle IPAddress in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="34555-255">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-256">CallerRelayPort</span><span class="sxs-lookup"><span data-stu-id="34555-256">CallerRelayPort</span></span></p></td>
<td><p><span data-ttu-id="34555-257">int</span><span class="sxs-lookup"><span data-stu-id="34555-257">int</span></span></p></td>
<td><p><span data-ttu-id="34555-258">Port des A/V-Edgedienst, der vom Anrufer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34555-258">Port on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-259">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="34555-259">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="34555-260">var (50)</span><span class="sxs-lookup"><span data-stu-id="34555-260">var(50)</span></span></p></td>
<td><p><span data-ttu-id="34555-261">Der IP-Adressen Schlüssel des A/V-Edgedienst, der vom aufgerufenen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34555-261">IP Address key of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="34555-262">Weitere Informationen finden Sie <a href="lync-server-2013-ipaddress-table.md">in der Tabelle IPAddress in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="34555-262">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-263">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="34555-263">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="34555-264">int</span><span class="sxs-lookup"><span data-stu-id="34555-264">int</span></span></p></td>
<td><p><span data-ttu-id="34555-265">Port auf dem A/V-Edgedienst, der vom aufgerufenen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="34555-265">Port on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-266">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="34555-266">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="34555-267">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="34555-267">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34555-268">Name des Aufnahmegeräts des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="34555-268">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-269">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="34555-269">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="34555-270">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="34555-270">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34555-271">Name des Render-Geräts des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="34555-271">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-272">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="34555-272">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="34555-273">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="34555-273">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34555-274">Name des Aufnahmegeräte Treibers des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="34555-274">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-275">CallerRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="34555-275">CallerRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="34555-276">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="34555-276">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34555-277">Name des Render-Gerätetreibers des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="34555-277">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-278">CalleeCaptureDev</span><span class="sxs-lookup"><span data-stu-id="34555-278">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="34555-279">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="34555-279">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34555-280">Der Name des Erfassungsgeräts des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="34555-280">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-281">CalleeRenderDev</span><span class="sxs-lookup"><span data-stu-id="34555-281">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="34555-282">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="34555-282">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34555-283">Name des Render-Geräts.</span><span class="sxs-lookup"><span data-stu-id="34555-283">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-284">CalleCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="34555-284">CalleCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="34555-285">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="34555-285">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34555-286">Der Name des Capture-Gerätetreibers des anrufempfängers.</span><span class="sxs-lookup"><span data-stu-id="34555-286">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-287">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="34555-287">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="34555-288">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="34555-288">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="34555-289">Der Name des Render-Gerätetreibers des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="34555-289">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-290">CallerNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="34555-290">CallerNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="34555-291">tinyint</span><span class="sxs-lookup"><span data-stu-id="34555-291">tinyint</span></span></p></td>
<td><p><span data-ttu-id="34555-292">Netzwerkverbindungstyp des Anrufers: 0 ist verkabelt, 1 ist drahtlos.</span><span class="sxs-lookup"><span data-stu-id="34555-292">Caller’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-293">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="34555-293">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="34555-294">bit</span><span class="sxs-lookup"><span data-stu-id="34555-294">bit</span></span></p></td>
<td><p><span data-ttu-id="34555-295">Gibt an, ob der Anrufer über ein virtuelles privates Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="34555-295">Indicates whether or not the caller connected over a virtual private network.</span></span> <span data-ttu-id="34555-296">1 ist ein VPN (virtuelles privates Netzwerk), 0 ist kein VPN.</span><span class="sxs-lookup"><span data-stu-id="34555-296">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-297">CallerLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="34555-297">CallerLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="34555-298">Decimal (18;)</span><span class="sxs-lookup"><span data-stu-id="34555-298">decimal(18,)</span></span></p></td>
<td><p><span data-ttu-id="34555-299">Netzwerkverbindungsgeschwindigkeit für den Endpunkt des Anrufers in BPS.</span><span class="sxs-lookup"><span data-stu-id="34555-299">Network link speed for the caller's endpoint in bps.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-300">CalleeNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="34555-300">CalleeNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="34555-301">tinyint</span><span class="sxs-lookup"><span data-stu-id="34555-301">tinyint</span></span></p></td>
<td><p><span data-ttu-id="34555-302">Netzwerkverbindungstyp des anrufempfängers: 0 ist verkabelt, 1 ist drahtlos.</span><span class="sxs-lookup"><span data-stu-id="34555-302">Callee’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-303">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="34555-303">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="34555-304">bit</span><span class="sxs-lookup"><span data-stu-id="34555-304">bit</span></span></p></td>
<td><p><span data-ttu-id="34555-305">Gibt an, ob der aufgerufene über ein virtuelles privates Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="34555-305">Indicates whether or not the callee connected over a virtual private network.</span></span> <span data-ttu-id="34555-306">1 ist ein VPN (virtuelles privates Netzwerk), 0 ist kein VPN.</span><span class="sxs-lookup"><span data-stu-id="34555-306">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-307">CalleeLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="34555-307">CalleeLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="34555-308">Decimal (18; 0)</span><span class="sxs-lookup"><span data-stu-id="34555-308">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="34555-309">Netzwerkverbindungsgeschwindigkeit für den Endpunkt des aufgerufenen (in BPS).</span><span class="sxs-lookup"><span data-stu-id="34555-309">Network link speed for the callee’s endpoint (in bps).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-310">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="34555-310">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="34555-311">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="34555-311">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="34555-312">Schmalband-Konversations-Mos der audiositzungen (basierend auf beiden Audiostreams).</span><span class="sxs-lookup"><span data-stu-id="34555-312">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-313">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="34555-313">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="34555-314">int</span><span class="sxs-lookup"><span data-stu-id="34555-314">int</span></span></p></td>
<td><p><span data-ttu-id="34555-315">Tatsächliche Bandbreite, die auf den angegebenen Send-Seitenstrom angewendet wurde, wenn verschiedene Richtlinieneinstellungen angegeben wurden (Turn, API, SDP, Richtlinien Server usw.).</span><span class="sxs-lookup"><span data-stu-id="34555-315">Actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="34555-316">Dies sollte nicht mit der effektiven Bandbreite verwechselt werden, da auf der Grundlage der Bandbreitenschätzung eine geringere effektive Bandbreite vorhanden sein kann.</span><span class="sxs-lookup"><span data-stu-id="34555-316">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="34555-317">Dies ist im Grunde die maximale Bandbreite, die der sendedatenstrom sperren kann, wenn die Bandbreite geschätzt wird.</span><span class="sxs-lookup"><span data-stu-id="34555-317">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-318">JitterInterArrival</span><span class="sxs-lookup"><span data-stu-id="34555-318">JitterInterArrival</span></span></p></td>
<td><p><span data-ttu-id="34555-319">int</span><span class="sxs-lookup"><span data-stu-id="34555-319">int</span></span></p></td>
<td><p><span data-ttu-id="34555-320">Durchschnittlicher Netzwerk-Jitter aus RTCP-Statistiken (Real Time Control Protocol).</span><span class="sxs-lookup"><span data-stu-id="34555-320">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-321">JitterInterArrivalMax</span><span class="sxs-lookup"><span data-stu-id="34555-321">JitterInterArrivalMax</span></span></p></td>
<td><p><span data-ttu-id="34555-322">int</span><span class="sxs-lookup"><span data-stu-id="34555-322">int</span></span></p></td>
<td><p><span data-ttu-id="34555-323">Maximaler Netzwerk Jitter während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="34555-323">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-324">RoundTrip</span><span class="sxs-lookup"><span data-stu-id="34555-324">RoundTrip</span></span></p></td>
<td><p><span data-ttu-id="34555-325">int</span><span class="sxs-lookup"><span data-stu-id="34555-325">int</span></span></p></td>
<td><p><span data-ttu-id="34555-326">Roundtrip-Zeit von RTCP-Statistiken</span><span class="sxs-lookup"><span data-stu-id="34555-326">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-327">RoundTripMax</span><span class="sxs-lookup"><span data-stu-id="34555-327">RoundTripMax</span></span></p></td>
<td><p><span data-ttu-id="34555-328">int</span><span class="sxs-lookup"><span data-stu-id="34555-328">int</span></span></p></td>
<td><p><span data-ttu-id="34555-329">Maximale Roundtrip-Zeit für den Audiostream.</span><span class="sxs-lookup"><span data-stu-id="34555-329">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-330">PacketLossRate</span><span class="sxs-lookup"><span data-stu-id="34555-330">PacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="34555-331">Dezimal (5; 4)</span><span class="sxs-lookup"><span data-stu-id="34555-331">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="34555-332">Durchschnittliche Paketverlustrate während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="34555-332">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-333">PacketLossRateMax</span><span class="sxs-lookup"><span data-stu-id="34555-333">PacketLossRateMax</span></span></p></td>
<td><p><span data-ttu-id="34555-334">Dezimal (5; 4)</span><span class="sxs-lookup"><span data-stu-id="34555-334">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="34555-335">Maximaler Paketverlust während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="34555-335">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-336">PacketUtilization</span><span class="sxs-lookup"><span data-stu-id="34555-336">PacketUtilization</span></span></p></td>
<td><p><span data-ttu-id="34555-337">int</span><span class="sxs-lookup"><span data-stu-id="34555-337">int</span></span></p></td>
<td><p><span data-ttu-id="34555-338">Paketanzahl für den Videostream (Echt Zeit Transport Protokoll, RTP).</span><span class="sxs-lookup"><span data-stu-id="34555-338">Packet count for the video stream (Real Time Transport Protocol, RTP).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-339">Bandbreite</span><span class="sxs-lookup"><span data-stu-id="34555-339">BandwidthEst</span></span></p></td>
<td><p><span data-ttu-id="34555-340">int</span><span class="sxs-lookup"><span data-stu-id="34555-340">int</span></span></p></td>
<td><p><span data-ttu-id="34555-341">Bandbreiten Schätzungen für den Audiostream.</span><span class="sxs-lookup"><span data-stu-id="34555-341">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-342">PayloadDescription</span><span class="sxs-lookup"><span data-stu-id="34555-342">PayloadDescription</span></span></p></td>
<td><p><span data-ttu-id="34555-343">int</span><span class="sxs-lookup"><span data-stu-id="34555-343">int</span></span></p></td>
<td><p><span data-ttu-id="34555-344">Für den Anruf verwendeter Audiocodec, auf den aus der <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription-Tabelle in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="34555-344">Audio codec used for the call, referenced from the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-345">VideoResolution</span><span class="sxs-lookup"><span data-stu-id="34555-345">VideoResolution</span></span></p></td>
<td><p><span data-ttu-id="34555-346">char (9)</span><span class="sxs-lookup"><span data-stu-id="34555-346">char(9)</span></span></p></td>
<td><p><span data-ttu-id="34555-347">Auflösung des Videos in Pixel Breite multipliziert mit Höhe des Pixels.</span><span class="sxs-lookup"><span data-stu-id="34555-347">Resolution of the video in pixels width multiplied by pixels height.</span></span> <span data-ttu-id="34555-348">Als Zeichenfolge gemeldet.</span><span class="sxs-lookup"><span data-stu-id="34555-348">Reported as a string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-349">VideoBitRateAvg</span><span class="sxs-lookup"><span data-stu-id="34555-349">VideoBitRateAvg</span></span></p></td>
<td><p><span data-ttu-id="34555-350">int</span><span class="sxs-lookup"><span data-stu-id="34555-350">int</span></span></p></td>
<td><p><span data-ttu-id="34555-351">Durchschnittliche Bitrate des Videodatenstroms.</span><span class="sxs-lookup"><span data-stu-id="34555-351">Average bit rate of the video stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-352">InboundVideoFrameRateAvg</span><span class="sxs-lookup"><span data-stu-id="34555-352">InboundVideoFrameRateAvg</span></span></p></td>
<td><p><span data-ttu-id="34555-353">Dezimal (9; 4)</span><span class="sxs-lookup"><span data-stu-id="34555-353">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="34555-354">Bildrate des empfangenen Videos.</span><span class="sxs-lookup"><span data-stu-id="34555-354">Frame rate of video received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-355">OutboundVideoFrameRateAvg</span><span class="sxs-lookup"><span data-stu-id="34555-355">OutboundVideoFrameRateAvg</span></span></p></td>
<td><p><span data-ttu-id="34555-356">Dezimal (9; 4)</span><span class="sxs-lookup"><span data-stu-id="34555-356">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="34555-357">Bildrate des gesendeten Videos.</span><span class="sxs-lookup"><span data-stu-id="34555-357">Frame rate of video sent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-358">ViideoBitRateMax</span><span class="sxs-lookup"><span data-stu-id="34555-358">ViideoBitRateMax</span></span></p></td>
<td><p><span data-ttu-id="34555-359">int</span><span class="sxs-lookup"><span data-stu-id="34555-359">int</span></span></p></td>
<td><p><span data-ttu-id="34555-360">Maximale Video Bitrate während der Videositzung.</span><span class="sxs-lookup"><span data-stu-id="34555-360">Maximum video bit rate during the video session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-361">VideoPacketLossRate</span><span class="sxs-lookup"><span data-stu-id="34555-361">VideoPacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="34555-362">Dezimal (9; 4)</span><span class="sxs-lookup"><span data-stu-id="34555-362">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="34555-363">Die Rate, mit der Videopakete verloren gegangen sind.</span><span class="sxs-lookup"><span data-stu-id="34555-363">Rate at which video packets were lost.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-364">VideoFrameLossRate</span><span class="sxs-lookup"><span data-stu-id="34555-364">VideoFrameLossRate</span></span></p></td>
<td><p><span data-ttu-id="34555-365">Decimal (9.4)</span><span class="sxs-lookup"><span data-stu-id="34555-365">decimal(9.4)</span></span></p></td>
<td><p><span data-ttu-id="34555-366">Der Prozentsatz der Gesamtzahl der Videoframes, die verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="34555-366">Percentage of total video frames that are lost.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-367">VideoFEC</span><span class="sxs-lookup"><span data-stu-id="34555-367">VideoFEC</span></span></p></td>
<td><p><span data-ttu-id="34555-368">bit</span><span class="sxs-lookup"><span data-stu-id="34555-368">bit</span></span></p></td>
<td><p><span data-ttu-id="34555-369">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="34555-369">Not used.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-370">VideoAllocateBWAvg</span><span class="sxs-lookup"><span data-stu-id="34555-370">VideoAllocateBWAvg</span></span></p></td>
<td><p><span data-ttu-id="34555-371">int</span><span class="sxs-lookup"><span data-stu-id="34555-371">int</span></span></p></td>
<td><p><span data-ttu-id="34555-372">Der durchschnittliche Umfang der für Video zugewiesenen Bandbreite.</span><span class="sxs-lookup"><span data-stu-id="34555-372">Average amount of bandwidth allocated for video.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="34555-373">VideoLocalFrameLossPercentageAvg</span><span class="sxs-lookup"><span data-stu-id="34555-373">VideoLocalFrameLossPercentageAvg</span></span></p></td>
<td><p><span data-ttu-id="34555-374">Decimal (9.4)</span><span class="sxs-lookup"><span data-stu-id="34555-374">decimal(9.4)</span></span></p></td>
<td><p><span data-ttu-id="34555-375">Der Prozentsatz der Gesamtzahl der Videoframes, die verloren gegangen sind.</span><span class="sxs-lookup"><span data-stu-id="34555-375">Percentage of total video frames that were lost.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="34555-376">SenderIsCallerPAI</span><span class="sxs-lookup"><span data-stu-id="34555-376">SenderIsCallerPAI</span></span></p></td>
<td><p><span data-ttu-id="34555-377">bit</span><span class="sxs-lookup"><span data-stu-id="34555-377">bit</span></span></p></td>
<td><p><span data-ttu-id="34555-378">Datenstrom Richtung für p-asserted Identity-Informationen.</span><span class="sxs-lookup"><span data-stu-id="34555-378">Stream direction for p-asserted identity information.</span></span> <span data-ttu-id="34555-379">1 bedeutet, dass die Datenstrom Richtung vom Anrufer an den aufgerufenen erfolgt; 0 bedeutet, dass die Datenstrom Richtung vom aufgerufenen zum Aufrufer ist.</span><span class="sxs-lookup"><span data-stu-id="34555-379">1 means the stream direction is from the caller to the callee; 0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="34555-380">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="34555-380">


</div>

<span> </span>

</div>

</div>

</span></span></div>

