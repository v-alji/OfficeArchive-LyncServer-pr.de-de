---
title: 'Lync Server 2013: AudioStreamDetail-Ansicht'
description: 'Lync Server 2013: AudioStreamDetail-Ansicht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioStreamDetail view
ms:assetid: b6a435b3-103c-41c4-96ed-33c3784534c0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721859(v=OCS.15)
ms:contentKeyID: 49733792
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 92c4c9bbb4f126e242e28d835222f6ba2af89d8b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438162"
---
# <a name="audiostreamdetail-view-in-lync-server-2013"></a><span data-ttu-id="61450-103">AudioStreamDetail-Ansicht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="61450-103">AudioStreamDetail view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="61450-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="61450-104">

<span> </span></span></span>

<span data-ttu-id="61450-105">_**Letztes Änderungsdatum des Themas:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="61450-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="61450-106">In der AudioStreamDetail-Ansicht werden Informationen zu jedem Audiostream in der Datenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="61450-106">The AudioStreamDetail View stores information about each audio stream in the database.</span></span> <span data-ttu-id="61450-107">Diese Ansicht wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="61450-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="61450-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="61450-108">Column</span></span></th>
<th><span data-ttu-id="61450-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="61450-109">Data Type</span></span></th>
<th><span data-ttu-id="61450-110">Details</span><span class="sxs-lookup"><span data-stu-id="61450-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="61450-111">SessionTime</span><span class="sxs-lookup"><span data-stu-id="61450-111">SessionTime</span></span></p></td>
<td><p><span data-ttu-id="61450-112">datetime</span><span class="sxs-lookup"><span data-stu-id="61450-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="61450-113">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="61450-113">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-114">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="61450-114">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="61450-115">int</span><span class="sxs-lookup"><span data-stu-id="61450-115">int</span></span></p></td>
<td><p><span data-ttu-id="61450-116">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="61450-116">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-117">Datenstrom-Nr</span><span class="sxs-lookup"><span data-stu-id="61450-117">StreamId</span></span></p></td>
<td><p><span data-ttu-id="61450-118">int</span><span class="sxs-lookup"><span data-stu-id="61450-118">int</span></span></p></td>
<td><p><span data-ttu-id="61450-119">Eindeutige ID innerhalb einer medienzeile</span><span class="sxs-lookup"><span data-stu-id="61450-119">Unique ID within a media line.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-120">StartTime</span><span class="sxs-lookup"><span data-stu-id="61450-120">StartTime</span></span></p></td>
<td><p><span data-ttu-id="61450-121">datetime</span><span class="sxs-lookup"><span data-stu-id="61450-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="61450-122">Startzeit der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="61450-122">Start time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-123">EndTime</span><span class="sxs-lookup"><span data-stu-id="61450-123">EndTime</span></span></p></td>
<td><p><span data-ttu-id="61450-124">datetime</span><span class="sxs-lookup"><span data-stu-id="61450-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="61450-125">Endzeit der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="61450-125">End time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-126">DialogCategory</span><span class="sxs-lookup"><span data-stu-id="61450-126">DialogCategory</span></span></p></td>
<td><p><span data-ttu-id="61450-127">bit</span><span class="sxs-lookup"><span data-stu-id="61450-127">bit</span></span></p></td>
<td><p><span data-ttu-id="61450-128">Dialog Feld Kategorie: 0 ist der lync Server to Mediation Server Leg; 1 ist der Vermittlungs Server für das PSTN-Gateway-Bein.</span><span class="sxs-lookup"><span data-stu-id="61450-128">Dialog category: 0 is the Lync Server to Mediation Server leg; 1 is the Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-129">MediationServerBypassFlag</span><span class="sxs-lookup"><span data-stu-id="61450-129">MediationServerBypassFlag</span></span></p></td>
<td><p><span data-ttu-id="61450-130">bit</span><span class="sxs-lookup"><span data-stu-id="61450-130">bit</span></span></p></td>
<td><p><span data-ttu-id="61450-131">Flag, das angibt, ob der Anruf umgangen wurde oder nicht.</span><span class="sxs-lookup"><span data-stu-id="61450-131">Flag indicating if the call was bypassed or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-132">MediaBypassWarningFlag</span><span class="sxs-lookup"><span data-stu-id="61450-132">MediaBypassWarningFlag</span></span></p></td>
<td><p><span data-ttu-id="61450-133">int</span><span class="sxs-lookup"><span data-stu-id="61450-133">int</span></span></p></td>
<td><p><span data-ttu-id="61450-134">Wenn vorhanden, gibt an, warum ein Anruf nicht umgangen wurde, auch wenn die Bypass-IDs zugeordnet wurden.</span><span class="sxs-lookup"><span data-stu-id="61450-134">If present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="61450-135">Es wird nur ein Wert definiert:</span><span class="sxs-lookup"><span data-stu-id="61450-135">Only one value is defined:</span></span></p>
<p><span data-ttu-id="61450-136">0x0001 – unbekannte Bypass-ID für den standardmäßigen Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="61450-136">0x0001 – Unknown bypass ID for Default network adapter.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-137">CallPriority</span><span class="sxs-lookup"><span data-stu-id="61450-137">CallPriority</span></span></p></td>
<td><p><span data-ttu-id="61450-138">int</span><span class="sxs-lookup"><span data-stu-id="61450-138">int</span></span></p></td>
<td><p><span data-ttu-id="61450-139">Die Priorität des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="61450-139">Priority of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-140">CallerPool</span><span class="sxs-lookup"><span data-stu-id="61450-140">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="61450-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="61450-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="61450-142">FQDN des anrufenden Pools.</span><span class="sxs-lookup"><span data-stu-id="61450-142">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-143">CalleePool</span><span class="sxs-lookup"><span data-stu-id="61450-143">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="61450-144">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="61450-144">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="61450-145">FQDN des aufgerufenen Pools.</span><span class="sxs-lookup"><span data-stu-id="61450-145">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-146">Anrufer</span><span class="sxs-lookup"><span data-stu-id="61450-146">Caller</span></span></p></td>
<td><p><span data-ttu-id="61450-147">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="61450-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="61450-148">URI des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-148">Caller’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-149">Callee</span><span class="sxs-lookup"><span data-stu-id="61450-149">Callee</span></span></p></td>
<td><p><span data-ttu-id="61450-150">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="61450-150">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="61450-151">URI des aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="61450-151">Callee’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-152">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="61450-152">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="61450-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="61450-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="61450-154">Benutzer-Agent-Zeichenfolge des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-154">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-155">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="61450-155">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="61450-156">smallint</span><span class="sxs-lookup"><span data-stu-id="61450-156">smallint</span></span></p></td>
<td><p><span data-ttu-id="61450-157">Der Typ des Benutzer-Agents des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-157">Type of the caller’s user agent.</span></span> <span data-ttu-id="61450-158">Weitere Informationen finden Sie <a href="lync-server-2013-useragent-table.md">in der UserAgent-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="61450-158">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-159">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="61450-159">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="61450-160">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="61450-160">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="61450-161">Kategorie des Benutzer-Agents des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-161">Category of the caller’s user agent.</span></span> <span data-ttu-id="61450-162">Weitere Informationen finden Sie <a href="lync-server-2013-useragentdef-table-qoe.md">in der UserAgentDef-Tabelle (QoE) in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="61450-162">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-163">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="61450-163">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="61450-164">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="61450-164">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="61450-165">Benutzer-Agent-Zeichenfolge des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="61450-165">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-166">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="61450-166">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="61450-167">smallint</span><span class="sxs-lookup"><span data-stu-id="61450-167">smallint</span></span></p></td>
<td><p><span data-ttu-id="61450-168">Der Typ des Benutzer-Agents des anrufempfängers.</span><span class="sxs-lookup"><span data-stu-id="61450-168">Type of callee’s user agent.</span></span> <span data-ttu-id="61450-169">Informationen finden Sie <a href="lync-server-2013-useragent-table.md">in der UserAgent-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="61450-169">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-170">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="61450-170">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="61450-171">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="61450-171">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="61450-172">Kategorie des Benutzer-Agents des berufenen</span><span class="sxs-lookup"><span data-stu-id="61450-172">Category of callee’s user agent.</span></span> <span data-ttu-id="61450-173">Informationen hierzu finden Sie <a href="lync-server-2013-useragentdef-table-qoe.md">in der UserAgentDef-Tabelle (QoE) in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="61450-173">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-174">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="61450-174">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="61450-175">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="61450-175">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="61450-176">Der Endpunktname des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-176">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-177">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="61450-177">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="61450-178">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="61450-178">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="61450-179">Endpunktname des angerufenen</span><span class="sxs-lookup"><span data-stu-id="61450-179">Callee’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-180">Anrufer</span><span class="sxs-lookup"><span data-stu-id="61450-180">CallerOS</span></span></p></td>
<td><p><span data-ttu-id="61450-181">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="61450-181">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="61450-182">Betriebssystem (OS) des Endpunkts des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-182">Operating system (OS) of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-183">CalleeOS</span><span class="sxs-lookup"><span data-stu-id="61450-183">CalleeOS</span></span></p></td>
<td><p><span data-ttu-id="61450-184">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="61450-184">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="61450-185">Betriebssystem (OS) des Endpunkts des aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="61450-185">Operating system (OS) of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-186">CallerCPUName</span><span class="sxs-lookup"><span data-stu-id="61450-186">CallerCPUName</span></span></p></td>
<td><p><span data-ttu-id="61450-187">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="61450-187">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="61450-188">Der CPU-Name des Endpunkts des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-188">CPU name of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-189">CalleeCPUName</span><span class="sxs-lookup"><span data-stu-id="61450-189">CalleeCPUName</span></span></p></td>
<td><p><span data-ttu-id="61450-190">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="61450-190">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="61450-191">Der CPU-Name des Endpunkts des aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="61450-191">CPU name of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-192">CallerCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="61450-192">CallerCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="61450-193">smallint</span><span class="sxs-lookup"><span data-stu-id="61450-193">smallint</span></span></p></td>
<td><p><span data-ttu-id="61450-194">Die Anzahl der CPU-Kerne im Endpunkt des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-194">Number of CPU cores in the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-195">CalleeCPUNumberOfCores</span><span class="sxs-lookup"><span data-stu-id="61450-195">CalleeCPUNumberOfCores</span></span></p></td>
<td><p><span data-ttu-id="61450-196">smallint</span><span class="sxs-lookup"><span data-stu-id="61450-196">smallint</span></span></p></td>
<td><p><span data-ttu-id="61450-197">Die Anzahl der CPU-Kerne im Endpunkt des aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="61450-197">Number of CPU cores in the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-198">CallerCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="61450-198">CallerCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="61450-199">int</span><span class="sxs-lookup"><span data-stu-id="61450-199">int</span></span></p></td>
<td><p><span data-ttu-id="61450-200">CPU-Prozessorgeschwindigkeit des Endpunkts des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-200">CPU processor speed of the caller’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-201">CalleeCPUProcessorSpeed</span><span class="sxs-lookup"><span data-stu-id="61450-201">CalleeCPUProcessorSpeed</span></span></p></td>
<td><p><span data-ttu-id="61450-202">int</span><span class="sxs-lookup"><span data-stu-id="61450-202">int</span></span></p></td>
<td><p><span data-ttu-id="61450-203">CPU-Prozessorgeschwindigkeit des Endpunkts des aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="61450-203">CPU processor speed of the callee’s endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-204">CallerVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="61450-204">CallerVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="61450-205">tinyint</span><span class="sxs-lookup"><span data-stu-id="61450-205">tinyint</span></span></p></td>
<td><p><span data-ttu-id="61450-206">Gibt an, ob das System des Anrufers in einer virtualisierten Umgebung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61450-206">Indicates whether the caller’s system is running in a virtualized environment.</span></span> <span data-ttu-id="61450-207">Weitere Informationen finden Sie <a href="lync-server-2013-endpoint-table.md">in der Endpunkt Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="61450-207">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-208">CalleeVirtualizationFlag</span><span class="sxs-lookup"><span data-stu-id="61450-208">CalleeVirtualizationFlag</span></span></p></td>
<td><p><span data-ttu-id="61450-209">tinyint</span><span class="sxs-lookup"><span data-stu-id="61450-209">tinyint</span></span></p></td>
<td><p><span data-ttu-id="61450-210">Gibt an, ob das System des aufgerufenen in einer virtualisierten Umgebung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="61450-210">Indicates whether the callee’s system is running in a virtualized environment.</span></span> <span data-ttu-id="61450-211">Weitere Informationen finden Sie <a href="lync-server-2013-endpoint-table.md">in der Endpunkt Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="61450-211">See the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-212">CorrelationKey</span><span class="sxs-lookup"><span data-stu-id="61450-212">CorrelationKey</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="61450-213">Korrelationsschlüssel</span><span class="sxs-lookup"><span data-stu-id="61450-213">Correlation key.</span></span> <span data-ttu-id="61450-214">Wird in der <a href="lync-server-2013-sessioncorrelation-table.md">SessionCorrelation-Tabelle in lync Server 2013</a>referenziert.</span><span class="sxs-lookup"><span data-stu-id="61450-214">Referenced from the <a href="lync-server-2013-sessioncorrelation-table.md">SessionCorrelation table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-215">ConnectivityIce</span><span class="sxs-lookup"><span data-stu-id="61450-215">ConnectivityIce</span></span></p></td>
<td><p><span data-ttu-id="61450-216">tinyint</span><span class="sxs-lookup"><span data-stu-id="61450-216">tinyint</span></span></p></td>
<td><p><span data-ttu-id="61450-217">Informationen zum Medienpfad, beispielsweise direkt oder weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="61450-217">Information about the media path, such as direct or relayed.</span></span> <span data-ttu-id="61450-218">Weitere Informationen finden Sie <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="61450-218">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-219">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="61450-219">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="61450-220">int</span><span class="sxs-lookup"><span data-stu-id="61450-220">int</span></span></p></td>
<td><p><span data-ttu-id="61450-221">Informationen zum Prozess der interaktiven Verbindungseinrichtung (ICE), der unter Bits-Flags für den Aufrufer beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="61450-221">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="61450-222">Ausführliche Informationen finden Sie in der Quality of Experience Monitoring Server Protocol-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="61450-222">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-223">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="61450-223">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="61450-224">int</span><span class="sxs-lookup"><span data-stu-id="61450-224">int</span></span></p></td>
<td><p><span data-ttu-id="61450-225">Informationen zum Prozess der interaktiven Verbindungseinrichtung (ICE), der in den Bits-Flags für den aufgerufenen beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="61450-225">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="61450-226">Ausführliche Informationen finden Sie in der Quality of Experience Monitoring Server Protocol-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="61450-226">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-227">Transport</span><span class="sxs-lookup"><span data-stu-id="61450-227">Transport</span></span></p></td>
<td><p><span data-ttu-id="61450-228">tinyint</span><span class="sxs-lookup"><span data-stu-id="61450-228">tinyint</span></span></p></td>
<td><p><span data-ttu-id="61450-229">Transporttyp: 0 ist UDP, 1 ist TCP.</span><span class="sxs-lookup"><span data-stu-id="61450-229">Transport type: 0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-230">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="61450-230">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="61450-231">var (50)</span><span class="sxs-lookup"><span data-stu-id="61450-231">var(50)</span></span></p></td>
<td><p><span data-ttu-id="61450-232">Die IP-Adresse des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-232">IP address of the caller.</span></span> <span data-ttu-id="61450-233">Hierbei kann es sich entweder um eine IPv4-oder eine IPv6-Adresse handeln.</span><span class="sxs-lookup"><span data-stu-id="61450-233">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-234">CallerPort</span><span class="sxs-lookup"><span data-stu-id="61450-234">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="61450-235">int</span><span class="sxs-lookup"><span data-stu-id="61450-235">int</span></span></p></td>
<td><p><span data-ttu-id="61450-236">Der vom Aufrufer verwendete Port.</span><span class="sxs-lookup"><span data-stu-id="61450-236">Port used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-237">CallerInside</span><span class="sxs-lookup"><span data-stu-id="61450-237">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="61450-238">bit</span><span class="sxs-lookup"><span data-stu-id="61450-238">bit</span></span></p></td>
<td><p><span data-ttu-id="61450-239">Gibt an, ob sich der Aufrufer innerhalb des Intervall Netzwerks befindet: 1 bedeutet, dass der Anrufer sich innerhalb des Unternehmensnetzwerks befindet, 0 bedeutet, dass sich der Anrufer außerhalb des Netzwerks befindet.</span><span class="sxs-lookup"><span data-stu-id="61450-239">Indicates whether the caller is inside the interval network: 1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-240">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="61450-240">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="61450-241">var (50)</span><span class="sxs-lookup"><span data-stu-id="61450-241">var(50)</span></span></p></td>
<td><p><span data-ttu-id="61450-242">Die IP-Adresse des aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="61450-242">IP address of the callee.</span></span> <span data-ttu-id="61450-243">Hierbei kann es sich entweder um eine IPv4-oder eine IPv6-Adresse handeln.</span><span class="sxs-lookup"><span data-stu-id="61450-243">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-244">CalleePort</span><span class="sxs-lookup"><span data-stu-id="61450-244">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="61450-245">int</span><span class="sxs-lookup"><span data-stu-id="61450-245">int</span></span></p></td>
<td><p><span data-ttu-id="61450-246">Port, der vom aufgerufenen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="61450-246">Port used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-247">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="61450-247">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="61450-248">bit</span><span class="sxs-lookup"><span data-stu-id="61450-248">bit</span></span></p></td>
<td><p><span data-ttu-id="61450-249">Gibt an, ob sich der aufgerufene innerhalb des Intervall Netzwerks befindet: 1 bedeutet, dass der Anrufer sich innerhalb des Unternehmensnetzwerks befindet, 0 bedeutet, dass der Anrufer sich außerhalb des Netzwerks befindet.</span><span class="sxs-lookup"><span data-stu-id="61450-249">Indicates whether the callee is inside the interval network: 1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-250">CallerUserSite</span><span class="sxs-lookup"><span data-stu-id="61450-250">CallerUserSite</span></span></p></td>
<td><p><span data-ttu-id="61450-251">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="61450-251">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="61450-252">Der Name der Website des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-252">Name of the caller’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-253">CallerRegion</span><span class="sxs-lookup"><span data-stu-id="61450-253">CallerRegion</span></span></p></td>
<td><p><span data-ttu-id="61450-254">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="61450-254">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="61450-255">Name des Landes/der Region der Website des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-255">Name of the country/region of the caller’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-256">CalleeUserSite</span><span class="sxs-lookup"><span data-stu-id="61450-256">CalleeUserSite</span></span></p></td>
<td><p><span data-ttu-id="61450-257">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="61450-257">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="61450-258">Name der Website des aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="61450-258">Name of the callee’s site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-259">CalleeRegion</span><span class="sxs-lookup"><span data-stu-id="61450-259">CalleeRegion</span></span></p></td>
<td><p><span data-ttu-id="61450-260">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="61450-260">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="61450-261">Name des Landes/der Region der Website des berufenen.</span><span class="sxs-lookup"><span data-stu-id="61450-261">Name of the country/region of the callee’s site.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-262">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="61450-262">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="61450-263">var (50)</span><span class="sxs-lookup"><span data-stu-id="61450-263">var(50)</span></span></p></td>
<td><p><span data-ttu-id="61450-264">Die IP-Adresse des A/V-Edgedienst, der vom Aufrufer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="61450-264">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="61450-265">Weitere Informationen finden Sie <a href="lync-server-2013-ipaddress-table.md">in der Tabelle IPAddress in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="61450-265">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-266">CallerRelayPort</span><span class="sxs-lookup"><span data-stu-id="61450-266">CallerRelayPort</span></span></p></td>
<td><p><span data-ttu-id="61450-267">int</span><span class="sxs-lookup"><span data-stu-id="61450-267">int</span></span></p></td>
<td><p><span data-ttu-id="61450-268">Der Port des A/V-Edgedienst, der vom Aufrufer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="61450-268">Port used on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-269">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="61450-269">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="61450-270">var (50)</span><span class="sxs-lookup"><span data-stu-id="61450-270">var(50)</span></span></p></td>
<td><p><span data-ttu-id="61450-271">Der IP-Adressen Schlüssel des A/V-Edgedienst, der vom aufgerufenen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="61450-271">IP Address key of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="61450-272">Weitere Informationen finden Sie <a href="lync-server-2013-ipaddress-table.md">in der Tabelle IPAddress in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="61450-272">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-273">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="61450-273">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="61450-274">int</span><span class="sxs-lookup"><span data-stu-id="61450-274">int</span></span></p></td>
<td><p><span data-ttu-id="61450-275">Port, der für den A/V-Edgedienst verwendet wird, der vom aufgerufenen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="61450-275">Port used on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-276">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="61450-276">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="61450-277">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="61450-277">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="61450-278">Name des Aufnahmegeräts des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-278">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-279">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="61450-279">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="61450-280">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="61450-280">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="61450-281">Name des Render-Geräts des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-281">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-282">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="61450-282">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="61450-283">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="61450-283">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="61450-284">Name des Aufnahmegeräte Treibers des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-284">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-285">CallerRenderDriver</span><span class="sxs-lookup"><span data-stu-id="61450-285">CallerRenderDriver</span></span></p></td>
<td><p><span data-ttu-id="61450-286">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="61450-286">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="61450-287">Name des Render-Gerätetreibers des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-287">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-288">CalleeCaptureDev</span><span class="sxs-lookup"><span data-stu-id="61450-288">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="61450-289">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="61450-289">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="61450-290">Der Name des Erfassungsgeräts des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-290">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-291">CalleeRenderDev</span><span class="sxs-lookup"><span data-stu-id="61450-291">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="61450-292">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="61450-292">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="61450-293">Name des Render-Geräts.</span><span class="sxs-lookup"><span data-stu-id="61450-293">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-294">CalleeCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="61450-294">CalleeCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="61450-295">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="61450-295">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="61450-296">Der Name des Capture-Gerätetreibers des anrufempfängers.</span><span class="sxs-lookup"><span data-stu-id="61450-296">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-297">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="61450-297">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="61450-298">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="61450-298">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="61450-299">Der Name des Render-Gerätetreibers des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="61450-299">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-300">CallerNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="61450-300">CallerNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="61450-301">tinyint</span><span class="sxs-lookup"><span data-stu-id="61450-301">tinyint</span></span></p></td>
<td><p><span data-ttu-id="61450-302">Netzwerkverbindungstyp des Anrufers: 0 ist verkabelt, 1 ist drahtlos.</span><span class="sxs-lookup"><span data-stu-id="61450-302">Caller’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-303">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="61450-303">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="61450-304">bit</span><span class="sxs-lookup"><span data-stu-id="61450-304">bit</span></span></p></td>
<td><p><span data-ttu-id="61450-305">Gibt an, ob der Anrufer über ein virtuelles privates Netzwerk verbunden ist: 1 ist ein VPN (virtuelles privates Netzwerk), 0 ist kein VPN.</span><span class="sxs-lookup"><span data-stu-id="61450-305">Indicates whether the caller connected over a virtual private network: 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-306">CallerLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="61450-306">CallerLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="61450-307">Decimal (18; 0)</span><span class="sxs-lookup"><span data-stu-id="61450-307">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="61450-308">Netzwerkverbindungsgeschwindigkeit für den Endpunkt des Anrufers in BPS.</span><span class="sxs-lookup"><span data-stu-id="61450-308">Network link speed for the caller's endpoint in bps.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-309">CalleeNetworkConnectionType</span><span class="sxs-lookup"><span data-stu-id="61450-309">CalleeNetworkConnectionType</span></span></p></td>
<td><p><span data-ttu-id="61450-310">tinyint</span><span class="sxs-lookup"><span data-stu-id="61450-310">tinyint</span></span></p></td>
<td><p><span data-ttu-id="61450-311">Netzwerkverbindungstyp des anrufempfängers: 0 ist verkabelt, 1 ist drahtlos.</span><span class="sxs-lookup"><span data-stu-id="61450-311">Callee’s network connection type: 0 is wired, 1 is wireless.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-312">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="61450-312">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="61450-313">bit</span><span class="sxs-lookup"><span data-stu-id="61450-313">bit</span></span></p></td>
<td><p><span data-ttu-id="61450-314">Gibt an, ob der Anrufer über ein virtuelles privates Netzwerk verbunden ist: 1 ist ein VPN (virtuelles privates Netzwerk), 0 ist kein VPN.</span><span class="sxs-lookup"><span data-stu-id="61450-314">Indicates whether the caller connected over a virtual private network: 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-315">CalleeLinkSpeed</span><span class="sxs-lookup"><span data-stu-id="61450-315">CalleeLinkSpeed</span></span></p></td>
<td><p><span data-ttu-id="61450-316">Decimal (18; 0)</span><span class="sxs-lookup"><span data-stu-id="61450-316">decimal(18,0)</span></span></p></td>
<td><p><span data-ttu-id="61450-317">Netzwerkverbindungsgeschwindigkeit für den Endpunkt des aufgerufenen in BPS.</span><span class="sxs-lookup"><span data-stu-id="61450-317">Network link speed for the callee's endpoint in bps.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-318">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="61450-318">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="61450-319">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-319">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-320">Schmalband-Konversations-Mos der audiositzungen (basierend auf beiden Audiostreams).</span><span class="sxs-lookup"><span data-stu-id="61450-320">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-321">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="61450-321">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="61450-322">int</span><span class="sxs-lookup"><span data-stu-id="61450-322">int</span></span></p></td>
<td><p><span data-ttu-id="61450-323">Tatsächliche Bandbreite, die auf den angegebenen Send-Seitenstrom angewendet wurde, wenn verschiedene Richtlinieneinstellungen angegeben wurden (Turn, API, SDP, Richtlinien Server usw.).</span><span class="sxs-lookup"><span data-stu-id="61450-323">Actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="61450-324">Dies sollte nicht mit der effektiven Bandbreite verwechselt werden, da auf der Grundlage der Bandbreitenschätzung eine geringere effektive Bandbreite vorhanden sein kann.</span><span class="sxs-lookup"><span data-stu-id="61450-324">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="61450-325">Dies ist im Grunde die maximale Bandbreite, die der sendedatenstrom sperren kann, wenn die Bandbreite geschätzt wird.</span><span class="sxs-lookup"><span data-stu-id="61450-325">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-326">JitterInterArrival</span><span class="sxs-lookup"><span data-stu-id="61450-326">JitterInterArrival</span></span></p></td>
<td><p><span data-ttu-id="61450-327">int</span><span class="sxs-lookup"><span data-stu-id="61450-327">int</span></span></p></td>
<td><p><span data-ttu-id="61450-328">Durchschnittlicher Netzwerk-Jitter aus RTCP-Statistiken (Real Time Control Protocol).</span><span class="sxs-lookup"><span data-stu-id="61450-328">Average network jitter from Real Time Control Protocol (RTCP) statistics.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-329">JitterInterArrivalMax</span><span class="sxs-lookup"><span data-stu-id="61450-329">JitterInterArrivalMax</span></span></p></td>
<td><p><span data-ttu-id="61450-330">int</span><span class="sxs-lookup"><span data-stu-id="61450-330">int</span></span></p></td>
<td><p><span data-ttu-id="61450-331">Maximaler Netzwerk Jitter während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="61450-331">Maximum network jitter during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-332">PacketLossRate</span><span class="sxs-lookup"><span data-stu-id="61450-332">PacketLossRate</span></span></p></td>
<td><p><span data-ttu-id="61450-333">Dezimal (5; 4)</span><span class="sxs-lookup"><span data-stu-id="61450-333">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="61450-334">Durchschnittliche Paketverlustrate während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="61450-334">Average packet loss rate during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-335">PacketLossRateMax</span><span class="sxs-lookup"><span data-stu-id="61450-335">PacketLossRateMax</span></span></p></td>
<td><p><span data-ttu-id="61450-336">Dezimal (5; 4)</span><span class="sxs-lookup"><span data-stu-id="61450-336">decimal(5,4)</span></span></p></td>
<td><p><span data-ttu-id="61450-337">Maximaler Paketverlust während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="61450-337">Maximum packet loss observed during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-338">BurstDensity</span><span class="sxs-lookup"><span data-stu-id="61450-338">BurstDensity</span></span></p></td>
<td><p><span data-ttu-id="61450-339">Dezimal (9; 4)</span><span class="sxs-lookup"><span data-stu-id="61450-339">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="61450-340">Durchschnittliche Dichte des Paketverlusts während des Ausbruchs von Verlusten während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="61450-340">Average density of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-341">BurstDuration</span><span class="sxs-lookup"><span data-stu-id="61450-341">BurstDuration</span></span></p></td>
<td><p><span data-ttu-id="61450-342">int</span><span class="sxs-lookup"><span data-stu-id="61450-342">int</span></span></p></td>
<td><p><span data-ttu-id="61450-343">Durchschnittliche Dauer des Paketverlusts während des Ausbruchs von Verlusten während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="61450-343">Average duration of packet loss during bursts of losses during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-344">BurstGapDensity</span><span class="sxs-lookup"><span data-stu-id="61450-344">BurstGapDensity</span></span></p></td>
<td><p><span data-ttu-id="61450-345">Dezimal (9; 4)</span><span class="sxs-lookup"><span data-stu-id="61450-345">decimal(9,4)</span></span></p></td>
<td><p><span data-ttu-id="61450-346">Durchschnittliche Dichte des Paketverlusts bei Lücken zwischen Bursts des Paketverlusts.</span><span class="sxs-lookup"><span data-stu-id="61450-346">Average density of packet loss during gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-347">BurstGapDuration</span><span class="sxs-lookup"><span data-stu-id="61450-347">BurstGapDuration</span></span></p></td>
<td><p><span data-ttu-id="61450-348">int</span><span class="sxs-lookup"><span data-stu-id="61450-348">int</span></span></p></td>
<td><p><span data-ttu-id="61450-349">Durchschnittliche Dauer von Lücken zwischen Bursts des Paketverlusts.</span><span class="sxs-lookup"><span data-stu-id="61450-349">Average duration of gaps between bursts of packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-350">PacketUtilization</span><span class="sxs-lookup"><span data-stu-id="61450-350">PacketUtilization</span></span></p></td>
<td><p><span data-ttu-id="61450-351">int</span><span class="sxs-lookup"><span data-stu-id="61450-351">int</span></span></p></td>
<td><p><span data-ttu-id="61450-352">Die Anzahl der Pakete für den Audiostream.</span><span class="sxs-lookup"><span data-stu-id="61450-352">Packet count for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-353">Bandbreite</span><span class="sxs-lookup"><span data-stu-id="61450-353">BandwidthEst</span></span></p></td>
<td><p><span data-ttu-id="61450-354">int</span><span class="sxs-lookup"><span data-stu-id="61450-354">int</span></span></p></td>
<td><p><span data-ttu-id="61450-355">Bandbreiten Schätzungen für den Audiostream.</span><span class="sxs-lookup"><span data-stu-id="61450-355">Bandwidth estimates for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-356">DegradationAvg</span><span class="sxs-lookup"><span data-stu-id="61450-356">DegradationAvg</span></span></p></td>
<td><p><span data-ttu-id="61450-357">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-357">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-358">Netzwerk-Mos-Verschlechterung für den gesamten Anruf.</span><span class="sxs-lookup"><span data-stu-id="61450-358">Network MOS Degradation for the whole call.</span></span> <span data-ttu-id="61450-359">Der Bereich ist 0,0 bis 5,0.</span><span class="sxs-lookup"><span data-stu-id="61450-359">Range is 0.0 to 5.0.</span></span> <span data-ttu-id="61450-360">Diese Metrik zeigt die Menge, die das Netzwerk Mos aufgrund von Jitter und Paketverlust reduziert wurde.</span><span class="sxs-lookup"><span data-stu-id="61450-360">This metric shows the amount the Network MOS was reduced because of jitter and packet loss.</span></span> <span data-ttu-id="61450-361">Für akzeptable Qualität sollte es weniger als 0,5.</span><span class="sxs-lookup"><span data-stu-id="61450-361">For acceptable quality it should less than 0.5.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-362">DegradationMax</span><span class="sxs-lookup"><span data-stu-id="61450-362">DegradationMax</span></span></p></td>
<td><p><span data-ttu-id="61450-363">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-363">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-364">Maximaler Netzwerk-Mos-Abbau während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="61450-364">Maximum Network MOS degradation during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-365">DegradationJitterAvg</span><span class="sxs-lookup"><span data-stu-id="61450-365">DegradationJitterAvg</span></span></p></td>
<td><p><span data-ttu-id="61450-366">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-366">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-367">Netzwerk-Mos-Beeinträchtigung durch Jitter.</span><span class="sxs-lookup"><span data-stu-id="61450-367">Network MOS degradation caused by jitter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-368">DegradationPacketLossAvg</span><span class="sxs-lookup"><span data-stu-id="61450-368">DegradationPacketLossAvg</span></span></p></td>
<td><p><span data-ttu-id="61450-369">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-369">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-370">Netzwerk-Mos-Beeinträchtigung durch Paketverlust.</span><span class="sxs-lookup"><span data-stu-id="61450-370">Network MOS degradation caused by packet loss.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-371">PayloadDescription</span><span class="sxs-lookup"><span data-stu-id="61450-371">PayloadDescription</span></span></p></td>
<td><p><span data-ttu-id="61450-372">int</span><span class="sxs-lookup"><span data-stu-id="61450-372">int</span></span></p></td>
<td><p><span data-ttu-id="61450-373">Der für den Anruf verwendete Audiocodec, auf den von der <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription-Tabelle in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="61450-373">The audio codec used for the call, referenced from the <a href="lync-server-2013-payloaddescription-table.md">PayloadDescription table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-374">AudioSampleRate</span><span class="sxs-lookup"><span data-stu-id="61450-374">AudioSampleRate</span></span></p></td>
<td><p><span data-ttu-id="61450-375">int</span><span class="sxs-lookup"><span data-stu-id="61450-375">int</span></span></p></td>
<td><p><span data-ttu-id="61450-376">Abtastrate für den Audiostream.</span><span class="sxs-lookup"><span data-stu-id="61450-376">Sampling rate for the audio stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-377">CallerSendSignalLevel</span><span class="sxs-lookup"><span data-stu-id="61450-377">CallerSendSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="61450-378">int</span><span class="sxs-lookup"><span data-stu-id="61450-378">int</span></span></p></td>
<td><p><span data-ttu-id="61450-379">Analoger Gain-Regler für Audio-Signalpegel für das Audiosignal, das der Anrufer gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="61450-379">Post-Analog Gain Control audio signal level for the audio the caller sent.</span></span> <span data-ttu-id="61450-380">Die Einheit für diese Metrik lautet dBmo.</span><span class="sxs-lookup"><span data-stu-id="61450-380">The unit for this metric is dBmo.</span></span> <span data-ttu-id="61450-381">Für akzeptable Qualität sollte es mindestens 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="61450-381">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="61450-382">Diese Metrik wird vom A/V-Konferenz Server oder von IP-Telefonen nicht gemeldet.</span><span class="sxs-lookup"><span data-stu-id="61450-382">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-383">CallerRecvSignalLevel</span><span class="sxs-lookup"><span data-stu-id="61450-383">CallerRecvSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="61450-384">int</span><span class="sxs-lookup"><span data-stu-id="61450-384">int</span></span></p></td>
<td><p><span data-ttu-id="61450-385">Audio-Signalpegel für das Audiosignal, das der Anrufer empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="61450-385">Audio signal level for the audio the caller received.</span></span> <span data-ttu-id="61450-386">Die Einheit für diese Metrik lautet dBmo.</span><span class="sxs-lookup"><span data-stu-id="61450-386">The unit for this metric is dBmo.</span></span> <span data-ttu-id="61450-387">Für akzeptable Qualität sollte es mindestens 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="61450-387">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="61450-388">Diese Metrik wird vom A/V-Konferenz Server oder von IP-Telefonen nicht gemeldet.</span><span class="sxs-lookup"><span data-stu-id="61450-388">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-389">CallerSendNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="61450-389">CallerSendNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="61450-390">int</span><span class="sxs-lookup"><span data-stu-id="61450-390">int</span></span></p></td>
<td><p><span data-ttu-id="61450-391">Nach analoger Gain-Regler Audio-Rauschpegel für das Audiosignal, das der Anrufer gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="61450-391">Post-Analog Gain Control audio noise level for the audio the caller sent.</span></span> <span data-ttu-id="61450-392">Die Einheit für diese Metrik lautet dBmo.</span><span class="sxs-lookup"><span data-stu-id="61450-392">The unit for this metric is dBmo.</span></span> <span data-ttu-id="61450-393">Für akzeptable Qualität sollte es weniger als 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="61450-393">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="61450-394">Diese Metrik wird vom A/V-Konferenz Server oder von IP-Telefonen nicht gemeldet.</span><span class="sxs-lookup"><span data-stu-id="61450-394">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-395">CallerRecvNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="61450-395">CallerRecvNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="61450-396">int</span><span class="sxs-lookup"><span data-stu-id="61450-396">int</span></span></p></td>
<td><p><span data-ttu-id="61450-397">Nach analoger Gain-Regler Audio-Rauschpegel für das Audiosignal, das der Anrufer empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="61450-397">Post-Analog Gain Control audio noise level for the audio the caller received.</span></span> <span data-ttu-id="61450-398">Die Einheit für diese Metrik lautet dBmo.</span><span class="sxs-lookup"><span data-stu-id="61450-398">The unit for this metric is dBmo.</span></span> <span data-ttu-id="61450-399">Für akzeptable Qualität sollte es weniger als 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="61450-399">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="61450-400">Diese Metrik wird vom A/V-Konferenz Server oder von IP-Telefonen nicht gemeldet.</span><span class="sxs-lookup"><span data-stu-id="61450-400">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-401">CallerEchoReturn</span><span class="sxs-lookup"><span data-stu-id="61450-401">CallerEchoReturn</span></span></p></td>
<td><p><span data-ttu-id="61450-402">int</span><span class="sxs-lookup"><span data-stu-id="61450-402">int</span></span></p></td>
<td><p><span data-ttu-id="61450-403">Verbesserung der Echo-Rückerstattung für den Anrufer.</span><span class="sxs-lookup"><span data-stu-id="61450-403">Echo Return Loss Enhancement for the caller.</span></span> <span data-ttu-id="61450-404">Die Einheit für diese Metrik ist DB.</span><span class="sxs-lookup"><span data-stu-id="61450-404">The unit for this metric is dB.</span></span> <span data-ttu-id="61450-405">Niedrigere Werte stellen weniger Echo dar.</span><span class="sxs-lookup"><span data-stu-id="61450-405">Lower values represent less echo.</span></span> <span data-ttu-id="61450-406">Diese Metrik wird vom A/V-Konferenz Server oder von IP-Telefonen nicht gemeldet.</span><span class="sxs-lookup"><span data-stu-id="61450-406">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-407">CallerSpeakerGlitchRate</span><span class="sxs-lookup"><span data-stu-id="61450-407">CallerSpeakerGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="61450-408">int</span><span class="sxs-lookup"><span data-stu-id="61450-408">int</span></span></p></td>
<td><p><span data-ttu-id="61450-409">Durchschnittliche Störimpulse pro fünf Minuten für die Lautsprecher-Wiedergabe des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-409">Average glitches per five minutes for the caller’s loudspeaker rendering.</span></span> <span data-ttu-id="61450-410">Für eine gute Qualität sollte dies weniger als eins pro fünf Minuten sein.</span><span class="sxs-lookup"><span data-stu-id="61450-410">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="61450-411">Nicht von A/V-Konferenzservern, Vermittlungsservern oder IP-Telefonen gemeldet.</span><span class="sxs-lookup"><span data-stu-id="61450-411">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-412">CallerMicGlitchRate</span><span class="sxs-lookup"><span data-stu-id="61450-412">CallerMicGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="61450-413">int</span><span class="sxs-lookup"><span data-stu-id="61450-413">int</span></span></p></td>
<td><p><span data-ttu-id="61450-414">Durchschnittliche Störimpulse pro fünf Minuten für die Mikrofonaufnahme des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-414">Average glitches per five minutes for the caller’s microphone capture.</span></span> <span data-ttu-id="61450-415">Für eine gute Qualität sollte dies weniger als eine pro fünf Minuten sein.</span><span class="sxs-lookup"><span data-stu-id="61450-415">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="61450-416">Nicht von A/V-Konferenzservern, Vermittlungsservern oder IP-Telefonen gemeldet.</span><span class="sxs-lookup"><span data-stu-id="61450-416">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-417">CallerTimestampDriftRateMic</span><span class="sxs-lookup"><span data-stu-id="61450-417">CallerTimestampDriftRateMic</span></span></p></td>
<td><p><span data-ttu-id="61450-418">Dezimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-418">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-419">Clock-Drift Rate des Anrufers im Verhältnis zur CPU-Uhr.</span><span class="sxs-lookup"><span data-stu-id="61450-419">Caller’s microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-420">CallerTimestampDriftRateSpk</span><span class="sxs-lookup"><span data-stu-id="61450-420">CallerTimestampDriftRateSpk</span></span></p></td>
<td><p><span data-ttu-id="61450-421">Dezimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-421">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-422">Clock-Drift Rate des Anrufers für das Lautsprecher Gerät relativ zur CPU-Uhr.</span><span class="sxs-lookup"><span data-stu-id="61450-422">Caller’s speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-423">CallerTimestampErrorMicMs</span><span class="sxs-lookup"><span data-stu-id="61450-423">CallerTimestampErrorMicMs</span></span></p></td>
<td><p><span data-ttu-id="61450-424">Dezimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-424">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-425">Durchschnittlicher Zeitstempel des Mikrofon-Datenstroms in Millisekunden in den letzten 20 Sekunden des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="61450-425">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-426">CallerTimestampErrorSpkMs</span><span class="sxs-lookup"><span data-stu-id="61450-426">CallerTimestampErrorSpkMs</span></span></p></td>
<td><p><span data-ttu-id="61450-427">Dezimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-427">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-428">Der Durchschnitt des Sprechers des Sprechers Render-Datenstrom Zeitstempel-Fehler in Millisekunden in den letzten 20 Sekunden des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="61450-428">Average of the caller’s speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-429">CallerVsEntryCauses</span><span class="sxs-lookup"><span data-stu-id="61450-429">CallerVsEntryCauses</span></span></p></td>
<td><p><span data-ttu-id="61450-430">smallint</span><span class="sxs-lookup"><span data-stu-id="61450-430">smallint</span></span></p></td>
<td><p><span data-ttu-id="61450-431">Voice-Switch ist ein Halbduplex-Modus mit verminderter Unterbrechungs Fähigkeit.</span><span class="sxs-lookup"><span data-stu-id="61450-431">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="61450-432">Weitere Informationen finden Sie <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="61450-432">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-433">CallerEchoEventCauses</span><span class="sxs-lookup"><span data-stu-id="61450-433">CallerEchoEventCauses</span></span></p></td>
<td><p><span data-ttu-id="61450-434">tinyint</span><span class="sxs-lookup"><span data-stu-id="61450-434">tinyint</span></span></p></td>
<td><p><span data-ttu-id="61450-435">Ursachen für ein Echo Ereignis für den Aufrufer.</span><span class="sxs-lookup"><span data-stu-id="61450-435">Causes of an echo event for the caller.</span></span> <span data-ttu-id="61450-436">Weitere Informationen finden Sie <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="61450-436">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-437">CallerEchoPercentMicIn</span><span class="sxs-lookup"><span data-stu-id="61450-437">CallerEchoPercentMicIn</span></span></p></td>
<td><p><span data-ttu-id="61450-438">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-438">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-439">Prozentsatz der Zeit, zu der ECHO im Mikrofonaufnahme Datenstrom des Anrufers erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="61450-439">Percentage of time when echo is detected in the caller’s microphone capture stream.</span></span> <span data-ttu-id="61450-440">Wenn Headset verwendet wird, sollte der Wert gering sein.</span><span class="sxs-lookup"><span data-stu-id="61450-440">If headset is used, the value should be low.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-441">CallerEchoPercentSend</span><span class="sxs-lookup"><span data-stu-id="61450-441">CallerEchoPercentSend</span></span></p></td>
<td><p><span data-ttu-id="61450-442">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-442">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-443">Prozentsatz der Zeit, zu der ECHO im gesendeten Datenstrom des Anrufers erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="61450-443">Percentage of time when echo is detected in the caller’s sent stream.</span></span> <span data-ttu-id="61450-444">Ein großer Prozentsatz des Echos in Send-Streams zeigt einen Hinweis auf Echo Verluste.</span><span class="sxs-lookup"><span data-stu-id="61450-444">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-445">CallerRxAGCSignalLevel</span><span class="sxs-lookup"><span data-stu-id="61450-445">CallerRxAGCSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="61450-446">int</span><span class="sxs-lookup"><span data-stu-id="61450-446">int</span></span></p></td>
<td><p><span data-ttu-id="61450-447">Empfangene Signalstufe auf dem Vermittlungs Server vom Gateway für das Audiosignal des Anrufers; Dies gilt nur für den Vermittlungs Server.</span><span class="sxs-lookup"><span data-stu-id="61450-447">Received signal level on the Mediation Server from the Gateway for the caller’s audio; this applies only to the Mediation Server.</span></span> <span data-ttu-id="61450-448">Die Einheit dieser Metrik ist dBoV.</span><span class="sxs-lookup"><span data-stu-id="61450-448">The unit of this metric is dBoV.</span></span> <span data-ttu-id="61450-449">Für eine gute Qualität sollte der zulässige Bereich-30 bis-18 dBoV sein.</span><span class="sxs-lookup"><span data-stu-id="61450-449">For good quality, the acceptable range should be -30 to -18 dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-450">CallerRxAGCNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="61450-450">CallerRxAGCNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="61450-451">int</span><span class="sxs-lookup"><span data-stu-id="61450-451">int</span></span></p></td>
<td><p><span data-ttu-id="61450-452">Empfangene Signalstufe auf dem Vermittlungs Server vom Gateway für das Audiosignal des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-452">Received signal level on the Mediation Server from the Gateway for the caller’s audio.</span></span> <span data-ttu-id="61450-453">Dies gilt nur für den Vermittlungs Server.</span><span class="sxs-lookup"><span data-stu-id="61450-453">This applies only to the Mediation Server.</span></span> <span data-ttu-id="61450-454">Die Einheit dieser Metrik ist dBoV.</span><span class="sxs-lookup"><span data-stu-id="61450-454">The unit of this metric is dBoV.</span></span> <span data-ttu-id="61450-455">Für eine gute Qualität sollte der zulässige Bereich kleiner als-50 dBoV sein.</span><span class="sxs-lookup"><span data-stu-id="61450-455">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-456">CallerRxAGCGain</span><span class="sxs-lookup"><span data-stu-id="61450-456">CallerRxAGCGain</span></span></p></td>
<td><p><span data-ttu-id="61450-457">int</span><span class="sxs-lookup"><span data-stu-id="61450-457">int</span></span></p></td>
<td><p><span data-ttu-id="61450-458">Automatische Gain-Steuerung (AGC) auf der Mediation Server-Seite, die auf das Audiosignal des Anrufers angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="61450-458">Automatic gain control (AGC) on the Mediation Server side applied to the caller’s audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-459">CallerInitialSignalLevelRMS</span><span class="sxs-lookup"><span data-stu-id="61450-459">CallerInitialSignalLevelRMS</span></span></p></td>
<td><p><span data-ttu-id="61450-460">float</span><span class="sxs-lookup"><span data-stu-id="61450-460">float</span></span></p></td>
<td><p><span data-ttu-id="61450-461">Root Mean Square (RMS) des eingehenden Signals an den Anrufer für bis zu den ersten 30 Sekunden des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="61450-461">Root mean square (RMS) of the incoming signal to the caller for up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-462">CalleeSendSignalLevel</span><span class="sxs-lookup"><span data-stu-id="61450-462">CalleeSendSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="61450-463">int</span><span class="sxs-lookup"><span data-stu-id="61450-463">int</span></span></p></td>
<td><p><span data-ttu-id="61450-464">Stellt die analogen Gain-Regler-Audiosignale für das Audiosignal dar, das der Anrufer gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="61450-464">Represents the Post-Analog Gain Control audio signal level for the audio the callee sent.</span></span> <span data-ttu-id="61450-465">Die Einheit für diese Metrik lautet dBmo.</span><span class="sxs-lookup"><span data-stu-id="61450-465">The unit for this metric is dBmo.</span></span> <span data-ttu-id="61450-466">Für akzeptable Qualität sollte es mindestens 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="61450-466">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="61450-467">Diese Metrik wird vom A/V-Konferenz Server oder von IP-Telefonen nicht gemeldet.</span><span class="sxs-lookup"><span data-stu-id="61450-467">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-468">CalleeRecvSignalLevel</span><span class="sxs-lookup"><span data-stu-id="61450-468">CalleeRecvSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="61450-469">int</span><span class="sxs-lookup"><span data-stu-id="61450-469">int</span></span></p></td>
<td><p><span data-ttu-id="61450-470">Audiosignal Pegel für das Audiosignal, das der Anrufer empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="61450-470">Audio signal level for the audio the callee received.</span></span> <span data-ttu-id="61450-471">Die Einheit für diese Metrik lautet dBmo.</span><span class="sxs-lookup"><span data-stu-id="61450-471">The unit for this metric is dBmo.</span></span> <span data-ttu-id="61450-472">Für akzeptable Qualität sollte es mindestens 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="61450-472">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="61450-473">Diese Metrik wird vom A/V-Konferenz Server oder von IP-Telefonen nicht gemeldet.</span><span class="sxs-lookup"><span data-stu-id="61450-473">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-474">CalleeSendNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="61450-474">CalleeSendNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="61450-475">int</span><span class="sxs-lookup"><span data-stu-id="61450-475">int</span></span></p></td>
<td><p><span data-ttu-id="61450-476">Post-Analog-Gain-Regler Audio-Rauschpegel für das Audiosignal, das der Anrufer gesendet hat.</span><span class="sxs-lookup"><span data-stu-id="61450-476">Post-Analog Gain Control audio noise level for the audio the callee sent.</span></span> <span data-ttu-id="61450-477">Die Einheit für diese Metrik lautet dBmo.</span><span class="sxs-lookup"><span data-stu-id="61450-477">The unit for this metric is dBmo.</span></span> <span data-ttu-id="61450-478">Für akzeptable Qualität sollte es weniger als 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="61450-478">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="61450-479">Diese Metrik wird vom A/V-Konferenz Server oder von IP-Telefonen nicht gemeldet.</span><span class="sxs-lookup"><span data-stu-id="61450-479">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-480">CalleeRecvNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="61450-480">CalleeRecvNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="61450-481">int</span><span class="sxs-lookup"><span data-stu-id="61450-481">int</span></span></p></td>
<td><p><span data-ttu-id="61450-482">Analoger Gain-Regler Audio-Rauschpegel für das Audiosignal, das der Anrufer empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="61450-482">Post-Analog Gain Control audio noise level for the audio the callee received.</span></span> <span data-ttu-id="61450-483">Die Einheit für diese Metrik lautet dBmo.</span><span class="sxs-lookup"><span data-stu-id="61450-483">The unit for this metric is dBmo.</span></span> <span data-ttu-id="61450-484">Für akzeptable Qualität sollte es weniger als 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="61450-484">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="61450-485">Diese Metrik wird vom A/V-Konferenz Server oder von IP-Telefonen nicht gemeldet.</span><span class="sxs-lookup"><span data-stu-id="61450-485">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-486">CalleeEchoReturn</span><span class="sxs-lookup"><span data-stu-id="61450-486">CalleeEchoReturn</span></span></p></td>
<td><p><span data-ttu-id="61450-487">int</span><span class="sxs-lookup"><span data-stu-id="61450-487">int</span></span></p></td>
<td><p><span data-ttu-id="61450-488">Verbesserung der Echo-Rückerstattung für den aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="61450-488">Echo Return Loss Enhancement for the callee.</span></span> <span data-ttu-id="61450-489">Die Einheit für diese Metrik ist DB.</span><span class="sxs-lookup"><span data-stu-id="61450-489">The unit for this metric is dB.</span></span> <span data-ttu-id="61450-490">Niedrigere Werte stellen weniger Echo dar.</span><span class="sxs-lookup"><span data-stu-id="61450-490">Lower values represent less echo.</span></span> <span data-ttu-id="61450-491">Diese Metrik wird vom A/V-Konferenz Server oder von IP-Telefonen nicht gemeldet.</span><span class="sxs-lookup"><span data-stu-id="61450-491">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-492">CalleeSpeakerGlitchRate</span><span class="sxs-lookup"><span data-stu-id="61450-492">CalleeSpeakerGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="61450-493">int</span><span class="sxs-lookup"><span data-stu-id="61450-493">int</span></span></p></td>
<td><p><span data-ttu-id="61450-494">Durchschnittliche Störgeräusche pro fünf Minuten für die Lautsprecher-Darstellung des anrufenden.</span><span class="sxs-lookup"><span data-stu-id="61450-494">Average glitches per five minutes for the callee’s loudspeaker rendering.</span></span> <span data-ttu-id="61450-495">Für eine gute Qualität sollte dies weniger als eins pro fünf Minuten sein.</span><span class="sxs-lookup"><span data-stu-id="61450-495">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="61450-496">Nicht von A/V-Konferenzservern, Vermittlungsservern oder IP-Telefonen gemeldet.</span><span class="sxs-lookup"><span data-stu-id="61450-496">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-497">CalleeMicGlitchRate</span><span class="sxs-lookup"><span data-stu-id="61450-497">CalleeMicGlitchRate</span></span></p></td>
<td><p><span data-ttu-id="61450-498">int</span><span class="sxs-lookup"><span data-stu-id="61450-498">int</span></span></p></td>
<td><p><span data-ttu-id="61450-499">Durchschnittliche Störimpulse pro fünf Minuten für die Mikrofonaufnahme des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="61450-499">Average glitches per five minutes for the callee’s microphone capture.</span></span> <span data-ttu-id="61450-500">Für eine gute Qualität sollte dies weniger als eine pro fünf Minuten sein.</span><span class="sxs-lookup"><span data-stu-id="61450-500">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="61450-501">Nicht von A/V-Konferenzservern, Vermittlungsservern oder IP-Telefonen gemeldet.</span><span class="sxs-lookup"><span data-stu-id="61450-501">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-502">CalleeTimestampDriftRateMic</span><span class="sxs-lookup"><span data-stu-id="61450-502">CalleeTimestampDriftRateMic</span></span></p></td>
<td><p><span data-ttu-id="61450-503">Dezimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-503">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-504">Abdriftrate des Mikrofon Geräts des Anrufers, relativ zu CPU-Takt.</span><span class="sxs-lookup"><span data-stu-id="61450-504">Callee’s microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-505">CalleeTimestampDriftRateSpk</span><span class="sxs-lookup"><span data-stu-id="61450-505">CalleeTimestampDriftRateSpk</span></span></p></td>
<td><p><span data-ttu-id="61450-506">Dezimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-506">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-507">Clock-Drift Rate des Anrufers für das Lautsprecher Gerät relativ zur CPU-Uhr.</span><span class="sxs-lookup"><span data-stu-id="61450-507">Callee’s speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-508">CalleeTimestampErrorMicMs</span><span class="sxs-lookup"><span data-stu-id="61450-508">CalleeTimestampErrorMicMs</span></span></p></td>
<td><p><span data-ttu-id="61450-509">Dezimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-509">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-510">Durchschnittlicher Zeitstempel des Mikrofon-Datenstroms in Millisekunden in den letzten 20 Sekunden des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="61450-510">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-511">CalleeTimestampErrorSpkMs</span><span class="sxs-lookup"><span data-stu-id="61450-511">CalleeTimestampErrorSpkMs</span></span></p></td>
<td><p><span data-ttu-id="61450-512">Dezimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-512">decimal(9,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-513">Der Durchschnitt des Sprechers des Speaker-Render-Datenstrom Zeitstempels in Millisekunden in den letzten 20 Sekunden des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="61450-513">Average of the callee’s speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-514">CalleeVsEntryCauses</span><span class="sxs-lookup"><span data-stu-id="61450-514">CalleeVsEntryCauses</span></span></p></td>
<td><p><span data-ttu-id="61450-515">smallint</span><span class="sxs-lookup"><span data-stu-id="61450-515">smallint</span></span></p></td>
<td><p><span data-ttu-id="61450-516">Voice-Switch ist ein Halbduplex-Modus mit verminderter Unterbrechungs Fähigkeit.</span><span class="sxs-lookup"><span data-stu-id="61450-516">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="61450-517">Weitere Informationen finden Sie <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="61450-517">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-518">CalleeEchoEventCauses</span><span class="sxs-lookup"><span data-stu-id="61450-518">CalleeEchoEventCauses</span></span></p></td>
<td><p><span data-ttu-id="61450-519">tinyint</span><span class="sxs-lookup"><span data-stu-id="61450-519">tinyint</span></span></p></td>
<td><p><span data-ttu-id="61450-520">Ursachen für ein Echo Ereignis für den aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="61450-520">Causes of an echo event for the callee.</span></span> <span data-ttu-id="61450-521">Weitere Informationen finden Sie <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="61450-521">See the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-522">CalleeEchoPercentMicIn</span><span class="sxs-lookup"><span data-stu-id="61450-522">CalleeEchoPercentMicIn</span></span></p></td>
<td><p><span data-ttu-id="61450-523">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-523">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-524">Prozentsatz der Zeit, zu der ECHO im Mikrofonaufnahme Datenstrom des berufenen erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="61450-524">Percentage of time when echo is detected in the callee’s microphone capture stream.</span></span> <span data-ttu-id="61450-525">Wenn Headset verwendet wird, sollte der Wert gering sein.</span><span class="sxs-lookup"><span data-stu-id="61450-525">If headset is used, the value should be low.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-526">CalleeEchoPercentSend</span><span class="sxs-lookup"><span data-stu-id="61450-526">CalleeEchoPercentSend</span></span></p></td>
<td><p><span data-ttu-id="61450-527">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-527">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-528">Der Prozentsatz der Zeit, zu der ECHO im gesendeten Datenstrom des aufgerufenen erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="61450-528">Percentage of time when echo is detected in the callee’s sent stream.</span></span> <span data-ttu-id="61450-529">Ein großer Prozentsatz des Echos in Send-Streams zeigt einen Hinweis auf Echo Verluste.</span><span class="sxs-lookup"><span data-stu-id="61450-529">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-530">CalleeRxAGCSignalLevel</span><span class="sxs-lookup"><span data-stu-id="61450-530">CalleeRxAGCSignalLevel</span></span></p></td>
<td><p><span data-ttu-id="61450-531">int</span><span class="sxs-lookup"><span data-stu-id="61450-531">int</span></span></p></td>
<td><p><span data-ttu-id="61450-532">Empfangene Signalstufe auf dem Vermittlungs Server vom Gateway für das Audio des berufenen; Dies gilt nur für den Vermittlungs Server.</span><span class="sxs-lookup"><span data-stu-id="61450-532">Received signal level on the Mediation Server from the Gateway for the callee’s audio; this applies only to the Mediation Server.</span></span> <span data-ttu-id="61450-533">Die Einheit dieser Metrik ist dBoV.</span><span class="sxs-lookup"><span data-stu-id="61450-533">The unit of this metric is dBoV.</span></span> <span data-ttu-id="61450-534">Für eine gute Qualität sollte der zulässige Bereich [-30 bis-18] dBoV sein.</span><span class="sxs-lookup"><span data-stu-id="61450-534">For good quality, the acceptable range should be [-30 to -18] dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-535">CalleeRxAGCNoiseLevel</span><span class="sxs-lookup"><span data-stu-id="61450-535">CalleeRxAGCNoiseLevel</span></span></p></td>
<td><p><span data-ttu-id="61450-536">int</span><span class="sxs-lookup"><span data-stu-id="61450-536">int</span></span></p></td>
<td><p><span data-ttu-id="61450-537">Empfangene Signalstufe auf dem Vermittlungs Server vom Gateway für das Audio des berufenen.</span><span class="sxs-lookup"><span data-stu-id="61450-537">Received signal level on the Mediation Server from the Gateway for the callee’s audio.</span></span> <span data-ttu-id="61450-538">Dies gilt nur für den Vermittlungs Server.</span><span class="sxs-lookup"><span data-stu-id="61450-538">This applies only to the Mediation Server.</span></span> <span data-ttu-id="61450-539">Die Einheit dieser Metrik ist dBoV.</span><span class="sxs-lookup"><span data-stu-id="61450-539">The unit of this metric is dBoV.</span></span> <span data-ttu-id="61450-540">Für eine gute Qualität sollte der zulässige Bereich kleiner als-50 dBoV sein.</span><span class="sxs-lookup"><span data-stu-id="61450-540">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-541">CalleeRxAGCGain</span><span class="sxs-lookup"><span data-stu-id="61450-541">CalleeRxAGCGain</span></span></p></td>
<td><p><span data-ttu-id="61450-542">int</span><span class="sxs-lookup"><span data-stu-id="61450-542">int</span></span></p></td>
<td><p><span data-ttu-id="61450-543">Automatische Gain-Steuerung (AGC) auf der Mediation Server-Seite, die auf die Audiofunktion des berufenen angewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="61450-543">Automatic gain control (AGC) on the Mediation Server side applied to the callee’s audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-544">CalleeInitialSignalLevelRMS</span><span class="sxs-lookup"><span data-stu-id="61450-544">CalleeInitialSignalLevelRMS</span></span></p></td>
<td><p><span data-ttu-id="61450-545">float</span><span class="sxs-lookup"><span data-stu-id="61450-545">float</span></span></p></td>
<td><p><span data-ttu-id="61450-546">Root Mean Square (RMS) des eingehenden Signals an den Anrufer für bis zu den ersten 30 Sekunden des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="61450-546">Root mean square (RMS) of the incoming signal to the callee for up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-547">RatioConcealedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="61450-547">RatioConcealedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="61450-548">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-548">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-549">Durchschnittliches Verhältnis der verborgenen Samples, die von der audioheilung an typische Samples generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="61450-549">Average ratio of concealed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-550">RatioStretchedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="61450-550">RatioStretchedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="61450-551">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-551">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-552">Durchschnittliches Verhältnis von gedehnten Samples, die von der audioheilung zu typischen Samples generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="61450-552">Average ratio of stretched samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-553">RatioCompressedSamplesAvg</span><span class="sxs-lookup"><span data-stu-id="61450-553">RatioCompressedSamplesAvg</span></span></p></td>
<td><p><span data-ttu-id="61450-554">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-554">decimal(5,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-555">Durchschnittliches Verhältnis von komprimierten Samples, die von der audioheilung zu typischen Samples generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="61450-555">Average ratio of compressed samples generated by audio healing to typical samples.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-556">RoundTrip</span><span class="sxs-lookup"><span data-stu-id="61450-556">RoundTrip</span></span></p></td>
<td><p><span data-ttu-id="61450-557">int</span><span class="sxs-lookup"><span data-stu-id="61450-557">int</span></span></p></td>
<td><p><span data-ttu-id="61450-558">Roundtrip-Zeit von RTCP-Statistiken</span><span class="sxs-lookup"><span data-stu-id="61450-558">Round trip time from RTCP statistics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-559">RoundTripMax</span><span class="sxs-lookup"><span data-stu-id="61450-559">RoundTripMax</span></span></p></td>
<td><p><span data-ttu-id="61450-560">int</span><span class="sxs-lookup"><span data-stu-id="61450-560">int</span></span></p></td>
<td><p><span data-ttu-id="61450-561">Maximale Roundtrip-Zeit für den Audiostream.</span><span class="sxs-lookup"><span data-stu-id="61450-561">Maximum round trip time for the audio stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-562">OverallAvgNetworkMOS</span><span class="sxs-lookup"><span data-stu-id="61450-562">OverallAvgNetworkMOS</span></span></p></td>
<td><p><span data-ttu-id="61450-563">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-563">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-564">Durchschnittliche Breitband-Netzwerk-Mos für den Anruf.</span><span class="sxs-lookup"><span data-stu-id="61450-564">Average wideband Network MOS for the call.</span></span> <span data-ttu-id="61450-565">Diese Metrik hängt vom verwendeten Paketverlust, Jitter und Codec ab.</span><span class="sxs-lookup"><span data-stu-id="61450-565">This metric depends on the packet loss, jitter, and codec used.</span></span> <span data-ttu-id="61450-566">Der Bereich ist 1,0 bis 5,0.</span><span class="sxs-lookup"><span data-stu-id="61450-566">Range is 1.0 to 5.0.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-567">OverallMinNetworkMOS</span><span class="sxs-lookup"><span data-stu-id="61450-567">OverallMinNetworkMOS</span></span></p></td>
<td><p><span data-ttu-id="61450-568">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-568">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-569">Minimale Breitband-Netzwerk-Mos für den Anruf.</span><span class="sxs-lookup"><span data-stu-id="61450-569">Minimum wideband Network MOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-570">SendListenMOS</span><span class="sxs-lookup"><span data-stu-id="61450-570">SendListenMOS</span></span></p></td>
<td><p><span data-ttu-id="61450-571">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-571">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-572">Durchschnittliche vorhergesagte Breitband-Abhör-Mos-Bewertung für gesendete Audiodaten, einschließlich Sprachniveau, Geräuschpegel und Aufnahmegeräte Eigenschaften.</span><span class="sxs-lookup"><span data-stu-id="61450-572">Average predicted wideband Listening MOS score for audio sent, including speech level, noise level and capture device characteristics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-573">SendListenMOSMin</span><span class="sxs-lookup"><span data-stu-id="61450-573">SendListenMOSMin</span></span></p></td>
<td><p><span data-ttu-id="61450-574">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-574">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-575">Minimale SendListenMOS für den Anruf.</span><span class="sxs-lookup"><span data-stu-id="61450-575">Minimum SendListenMOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-576">RecvListenMOS</span><span class="sxs-lookup"><span data-stu-id="61450-576">RecvListenMOS</span></span></p></td>
<td><p><span data-ttu-id="61450-577">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-577">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-578">Durchschnittlicher prognostizierter breitbandiger Abhör-Mos-Score für vom Netzwerk empfangene Audiosignale, einschließlich Sprachpegel, Geräuschpegel, Codec, Netzwerkbedingungen und Merkmale des Aufnahmegeräts.</span><span class="sxs-lookup"><span data-stu-id="61450-578">Average predicted wideband Listening MOS score for audio received from the network including speech level, noise level, codec, network conditions and capture device characteristics.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-579">RecvListenMOSMin</span><span class="sxs-lookup"><span data-stu-id="61450-579">RecvListenMOSMin</span></span></p></td>
<td><p><span data-ttu-id="61450-580">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="61450-580">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="61450-581">Minimale RecvListenMOS für den Anruf.</span><span class="sxs-lookup"><span data-stu-id="61450-581">Minimum RecvListenMOS for the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="61450-582">AudioFECUsed</span><span class="sxs-lookup"><span data-stu-id="61450-582">AudioFECUsed</span></span></p></td>
<td><p><span data-ttu-id="61450-583">bit</span><span class="sxs-lookup"><span data-stu-id="61450-583">bit</span></span></p></td>
<td><p><span data-ttu-id="61450-584">Gibt an, ob Audio FEC für den Anruf verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="61450-584">Indicates whether audio FEC was used for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="61450-585">SenderIsCallerPAI</span><span class="sxs-lookup"><span data-stu-id="61450-585">SenderIsCallerPAI</span></span></p></td>
<td><p><span data-ttu-id="61450-586">bit</span><span class="sxs-lookup"><span data-stu-id="61450-586">bit</span></span></p></td>
<td><p><span data-ttu-id="61450-587">Gibt die Richtung der p-Assert-identifizier Informationen an; 1 bedeutet, dass die Datenstrom Richtung vom Anrufer an den aufgerufenen erfolgt; 0 bedeutet, dass die Datenstrom Richtung vom aufgerufenen zum Aufrufer ist.</span><span class="sxs-lookup"><span data-stu-id="61450-587">Indicates direction of the p-asserted identify information; 1 means the stream direction is from the caller to the callee; 0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="61450-588">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="61450-588">


</div>

<span> </span>

</div>

</div>

</span></span></div>

