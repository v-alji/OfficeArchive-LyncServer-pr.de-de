---
title: 'Lync Server 2013: Sitzungsansicht'
description: 'Lync Server 2013: Sitzungsansicht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Session view
ms:assetid: 49e33f5b-45d0-4146-a5a4-76954d895a98
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688048(v=OCS.15)
ms:contentKeyID: 49733641
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ff4bc4abbd55e073006693d28f092f077698ef75
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444791"
---
# <a name="session-view-in-lync-server-2013"></a><span data-ttu-id="1275f-103">Sitzungsansicht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1275f-103">Session view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1275f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1275f-104">

<span> </span></span></span>

<span data-ttu-id="1275f-105">_**Letztes Änderungsdatum des Themas:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="1275f-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="1275f-106">Die Sitzungsansicht speichert Informationen zu Sitzungen mit Datensätzen in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="1275f-106">The Session View stores information about sessions that have records in the database.</span></span> <span data-ttu-id="1275f-107">Diese Ansicht wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1275f-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1275f-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="1275f-108">Column</span></span></th>
<th><span data-ttu-id="1275f-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1275f-109">Data Type</span></span></th>
<th><span data-ttu-id="1275f-110">Details</span><span class="sxs-lookup"><span data-stu-id="1275f-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1275f-111">ConferenceDateTime</span><span class="sxs-lookup"><span data-stu-id="1275f-111">ConferenceDateTime</span></span></p></td>
<td><p><span data-ttu-id="1275f-112">datetime</span><span class="sxs-lookup"><span data-stu-id="1275f-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="1275f-113">In der medialinie-Tabelle referenziert.</span><span class="sxs-lookup"><span data-stu-id="1275f-113">Referenced from the MediaLine Table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1275f-114">ConferenceURI</span><span class="sxs-lookup"><span data-stu-id="1275f-114">ConferenceURI</span></span></p></td>
<td><p><span data-ttu-id="1275f-115">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="1275f-115">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="1275f-116">Konferenz-URI, wenn es sich um eine Konferenz handelt, oder wenn es sich um eine Peer-to-Peer-Sitzung handelt.</span><span class="sxs-lookup"><span data-stu-id="1275f-116">Conference URI if this is a conference, or DialogID if this is a peer-to-peer session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1275f-117">Korrelation</span><span class="sxs-lookup"><span data-stu-id="1275f-117">Correlation</span></span></p></td>
<td><p><span data-ttu-id="1275f-118">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="1275f-118">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="1275f-119">Korrelations-ID der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="1275f-119">Correlation ID of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1275f-120">DialogCategory</span><span class="sxs-lookup"><span data-stu-id="1275f-120">DialogCategory</span></span></p></td>
<td><p><span data-ttu-id="1275f-121">bit</span><span class="sxs-lookup"><span data-stu-id="1275f-121">bit</span></span></p></td>
<td><p><span data-ttu-id="1275f-122">Dialog Feld Kategorie; 0 ist lync Server to Mediation Server Leg; 1 ist Vermittlungs Server für das PSTN-Gateway-Bein.</span><span class="sxs-lookup"><span data-stu-id="1275f-122">Dialog category; 0 is Lync Server to Mediation Server leg; 1 is Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1275f-123">MediationServerBypassFlag</span><span class="sxs-lookup"><span data-stu-id="1275f-123">MediationServerBypassFlag</span></span></p></td>
<td><p><span data-ttu-id="1275f-124">bit</span><span class="sxs-lookup"><span data-stu-id="1275f-124">bit</span></span></p></td>
<td><p><span data-ttu-id="1275f-125">Gibt an, ob der Anruf umgangen wurde.</span><span class="sxs-lookup"><span data-stu-id="1275f-125">Indicates whether or not the call was bypassed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1275f-126">MediaBypassWarningFlag</span><span class="sxs-lookup"><span data-stu-id="1275f-126">MediaBypassWarningFlag</span></span></p></td>
<td><p><span data-ttu-id="1275f-127">int</span><span class="sxs-lookup"><span data-stu-id="1275f-127">int</span></span></p></td>
<td><p><span data-ttu-id="1275f-128">Dieses Feld, falls vorhanden, gibt an, warum ein Anruf nicht umgangen wurde, auch wenn die Bypass-IDs übereinstimmten.</span><span class="sxs-lookup"><span data-stu-id="1275f-128">This field, if present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="1275f-129">Bei lync Server wird nur ein Wert definiert:</span><span class="sxs-lookup"><span data-stu-id="1275f-129">For Lync Server, only one value is defined:</span></span></p>
<p><span data-ttu-id="1275f-130">0x0001 – unbekannte Bypass-ID für den standardmäßigen Netzwerkadapter</span><span class="sxs-lookup"><span data-stu-id="1275f-130">0x0001 – Unknown bypass ID for Default network adapter</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1275f-131">StartTime</span><span class="sxs-lookup"><span data-stu-id="1275f-131">StartTime</span></span></p></td>
<td><p><span data-ttu-id="1275f-132">datetime</span><span class="sxs-lookup"><span data-stu-id="1275f-132">datetime</span></span></p></td>
<td><p><span data-ttu-id="1275f-133">Startzeit des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="1275f-133">Call start time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1275f-134">EndTime</span><span class="sxs-lookup"><span data-stu-id="1275f-134">EndTime</span></span></p></td>
<td><p><span data-ttu-id="1275f-135">datetime</span><span class="sxs-lookup"><span data-stu-id="1275f-135">datetime</span></span></p></td>
<td><p><span data-ttu-id="1275f-136">Endzeit des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="1275f-136">Call end time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1275f-137">CallerPool</span><span class="sxs-lookup"><span data-stu-id="1275f-137">CallerPool</span></span></p></td>
<td><p><span data-ttu-id="1275f-138">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1275f-138">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1275f-139">FQDN des anrufenden Pools.</span><span class="sxs-lookup"><span data-stu-id="1275f-139">Caller pool FQDN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1275f-140">CalleePool</span><span class="sxs-lookup"><span data-stu-id="1275f-140">CalleePool</span></span></p></td>
<td><p><span data-ttu-id="1275f-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1275f-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1275f-142">FQDN des aufgerufenen Pools.</span><span class="sxs-lookup"><span data-stu-id="1275f-142">Callee pool FQDN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1275f-143">CallerPAI</span><span class="sxs-lookup"><span data-stu-id="1275f-143">CallerPAI</span></span></p></td>
<td><p><span data-ttu-id="1275f-144">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="1275f-144">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="1275f-145">Identitäts-URI des Anrufers p-Assert</span><span class="sxs-lookup"><span data-stu-id="1275f-145">Caller’s p-asserted identity URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1275f-146">CalleePAI</span><span class="sxs-lookup"><span data-stu-id="1275f-146">CalleePAI</span></span></p></td>
<td><p><span data-ttu-id="1275f-147">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="1275f-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="1275f-148">P-Assert-Identitäts-URI des aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="1275f-148">Callee’s p-asserted identity URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1275f-149">CallerEndpoint</span><span class="sxs-lookup"><span data-stu-id="1275f-149">CallerEndpoint</span></span></p></td>
<td><p><span data-ttu-id="1275f-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1275f-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1275f-151">Der Endpunktname des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="1275f-151">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1275f-152">CalleeEndpoint</span><span class="sxs-lookup"><span data-stu-id="1275f-152">CalleeEndpoint</span></span></p></td>
<td><p><span data-ttu-id="1275f-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1275f-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1275f-154">Der Endpunktname des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="1275f-154">Caller’s endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1275f-155">CallerUserAgent</span><span class="sxs-lookup"><span data-stu-id="1275f-155">CallerUserAgent</span></span></p></td>
<td><p><span data-ttu-id="1275f-156">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1275f-156">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1275f-157">Benutzer-Agent-Zeichenfolge des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="1275f-157">Caller’s user agent string.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1275f-158">CallerUserAgentType</span><span class="sxs-lookup"><span data-stu-id="1275f-158">CallerUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="1275f-159">smallint</span><span class="sxs-lookup"><span data-stu-id="1275f-159">smallint</span></span></p></td>
<td><p><span data-ttu-id="1275f-160">Der Typ des Benutzer-Agents des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="1275f-160">Type of caller’s user agent.</span></span> <span data-ttu-id="1275f-161">Weitere Informationen finden Sie <a href="lync-server-2013-useragent-table.md">in der UserAgent-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="1275f-161">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1275f-162">CallerUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="1275f-162">CallerUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="1275f-163">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="1275f-163">nvarchar (64)</span></span></p></td>
<td><p><span data-ttu-id="1275f-164">Kategorie des Benutzer-Agents des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="1275f-164">Category of caller’s user agent.</span></span> <span data-ttu-id="1275f-165">Weitere Informationen finden Sie <a href="lync-server-2013-useragentdef-table-qoe.md">in der UserAgentDef-Tabelle (QoE) in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="1275f-165">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1275f-166">CalleeUserAgent</span><span class="sxs-lookup"><span data-stu-id="1275f-166">CalleeUserAgent</span></span></p></td>
<td><p><span data-ttu-id="1275f-167">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1275f-167">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="1275f-168">Benutzer-Agent-Zeichenfolge des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="1275f-168">Callee’s user agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1275f-169">CalleeUserAgentType</span><span class="sxs-lookup"><span data-stu-id="1275f-169">CalleeUserAgentType</span></span></p></td>
<td><p><span data-ttu-id="1275f-170">smallint</span><span class="sxs-lookup"><span data-stu-id="1275f-170">smallint</span></span></p></td>
<td><p><span data-ttu-id="1275f-171">Der Typ des Benutzer-Agents für den aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="1275f-171">Type of user agent for the callee.</span></span> <span data-ttu-id="1275f-172">Weitere Informationen finden Sie <a href="lync-server-2013-useragent-table.md">in der UserAgent-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="1275f-172">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1275f-173">CalleeUserAgentCategory</span><span class="sxs-lookup"><span data-stu-id="1275f-173">CalleeUserAgentCategory</span></span></p></td>
<td><p><span data-ttu-id="1275f-174">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="1275f-174">nvarchar (64)</span></span></p></td>
<td><p><span data-ttu-id="1275f-175">Benutzer-Agent-Kategorie für den aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="1275f-175">User agent category for the callee.</span></span> <span data-ttu-id="1275f-176">Weitere Informationen finden Sie <a href="lync-server-2013-useragentdef-table-qoe.md">in der UserAgentDef-Tabelle (QoE) in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="1275f-176">See the <a href="lync-server-2013-useragentdef-table-qoe.md">UserAgentDef table (QoE) in Lync Server 2013</a> for details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1275f-177">CallerURI</span><span class="sxs-lookup"><span data-stu-id="1275f-177">CallerURI</span></span></p></td>
<td><p><span data-ttu-id="1275f-178">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="1275f-178">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="1275f-179">URI des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="1275f-179">Caller’s URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1275f-180">CalleeURI</span><span class="sxs-lookup"><span data-stu-id="1275f-180">CalleeURI</span></span></p></td>
<td><p><span data-ttu-id="1275f-181">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="1275f-181">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="1275f-182">URI des aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="1275f-182">Callee’s URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1275f-183">CallPrioirty</span><span class="sxs-lookup"><span data-stu-id="1275f-183">CallPrioirty</span></span></p></td>
<td><p><span data-ttu-id="1275f-184">int</span><span class="sxs-lookup"><span data-stu-id="1275f-184">int</span></span></p></td>
<td><p><span data-ttu-id="1275f-185">Die Priorität des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="1275f-185">Priority of the call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="1275f-186">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1275f-186">


</div>

<span> </span>

</div>

</div>

</span></span></div>

