---
title: 'Lync Server 2013: MediaLine-Tabelle'
description: 'Lync Server 2013: medialinie-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaLine table
ms:assetid: 414b1d63-ae97-4c27-bac0-c9ad0f808ff0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425920(v=OCS.15)
ms:contentKeyID: 48183956
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2acea8e14ba0608d9ebf72a48f888bfc4501fae3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425619"
---
# <a name="medialine-table-in-lync-server-2013"></a><span data-ttu-id="8c387-103">MediaLine-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c387-103">MediaLine table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8c387-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8c387-104">

<span> </span></span></span>

<span data-ttu-id="8c387-105">_**Letztes Änderungsdatum des Themas:** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="8c387-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="8c387-106">Jeder Datensatz stellt eine medienzeile dar.</span><span class="sxs-lookup"><span data-stu-id="8c387-106">Each record represents one media line.</span></span> <span data-ttu-id="8c387-107">(Eine Audiositzung enthält in der Regel eine Audio-medienzeile.</span><span class="sxs-lookup"><span data-stu-id="8c387-107">(One audio session usually contains one audio media line.</span></span> <span data-ttu-id="8c387-108">Eine Audio-und Video (A/V)-Sitzung enthält in der Regel eine Audio-Medien Linie und eine Video Medien Linie, obwohl die Sitzung zwei Video Medien Linien enthalten kann, wenn ein Konferenzgerät verwendet wird oder wenn die Katalogansicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c387-108">One audio and video (A/V) session usually contains one audio media line and one video media line, although the session might contain two video media lines if a conferencing device is used or if Gallery View is used.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8c387-109"><strong>Spalte</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="8c387-110"><strong>Datentyp</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="8c387-111"><strong>Schlüssel/Index</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="8c387-112"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8c387-113"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-113"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-114">datetime</span><span class="sxs-lookup"><span data-stu-id="8c387-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="8c387-115">Primary</span><span class="sxs-lookup"><span data-stu-id="8c387-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="8c387-116">Wird in der <a href="lync-server-2013-session-table.md">Session-Tabelle in lync Server 2013</a>referenziert.</span><span class="sxs-lookup"><span data-stu-id="8c387-116">Referenced from the <a href="lync-server-2013-session-table.md">Session table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-117"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-117"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-118">int</span><span class="sxs-lookup"><span data-stu-id="8c387-118">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-119">Primary</span><span class="sxs-lookup"><span data-stu-id="8c387-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="8c387-120">Wird in der <a href="lync-server-2013-session-table.md">Session-Tabelle in lync Server 2013</a>referenziert.</span><span class="sxs-lookup"><span data-stu-id="8c387-120">Referenced from the <a href="lync-server-2013-session-table.md">Session table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-121"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-121"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-122">tinyint</span><span class="sxs-lookup"><span data-stu-id="8c387-122">tinyint</span></span></p></td>
<td><p><span data-ttu-id="8c387-123">Primary</span><span class="sxs-lookup"><span data-stu-id="8c387-123">Primary</span></span></p></td>
<td><p><span data-ttu-id="8c387-124">0 ist Haupt-Audio, 1 ist das Hauptvideo, und 2 ist ein Panorama Video, 3 ist die Anwendung/Desktop-Freigabe.</span><span class="sxs-lookup"><span data-stu-id="8c387-124">0 is main audio, 1 is main video, and 2 is panoramic video, 3 is Application/Desktop Sharing.</span></span> <span data-ttu-id="8c387-125">Diese Bezeichnung muss innerhalb einer einzelnen Sitzung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="8c387-125">This label must be unique within a single session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-126"><strong>ConnectivityIce</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-126"><strong>ConnectivityIce</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-127">tinyint</span><span class="sxs-lookup"><span data-stu-id="8c387-127">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8c387-128">Diese Spalte ist vorhanden, wird aber in Microsoft lync Server 2013 nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c387-128">This column is present but not used in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="8c387-129">Informationen zur für eine medienzeile verwendeten Konnektivität werden in den Spalten CallerConnectivityICE und CalleeConnectivityICE erfasst.</span><span class="sxs-lookup"><span data-stu-id="8c387-129">Information about the connectivity used for a media line is captured in the CallerConnectivityICE and CalleeConnectivityICE columns.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-130"><strong>CallerIceWarningFlags</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-130"><strong>CallerIceWarningFlags</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-131">int</span><span class="sxs-lookup"><span data-stu-id="8c387-131">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8c387-132">Informationen über das in Bits-Flags beschriebene Verfahren zum interaktiven Verbindungsaufbau (ICE).</span><span class="sxs-lookup"><span data-stu-id="8c387-132">Information about Interactive Connectivity Establishment (ICE) process described in bits flags.</span></span> <span data-ttu-id="8c387-133">Ausführliche Informationen finden Sie in der <em>Spezifikation für Quality of Experience Monitoring Server Protocol</em>, die zum Download zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="8c387-133">For details, refer to the <em>Quality of Experience Monitoring Server Protocol Specification</em>, available for download.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-134"><strong>CalleeIceWarningFlags</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-134"><strong>CalleeIceWarningFlags</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-135">int</span><span class="sxs-lookup"><span data-stu-id="8c387-135">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8c387-136">Identisch mit CallerIceWarningFlags, aber auf der aufgerufenen Seite.</span><span class="sxs-lookup"><span data-stu-id="8c387-136">Same as CallerIceWarningFlags, but on the callee side.</span></span> <span data-ttu-id="8c387-137">Ausführliche Informationen finden Sie in der <em>Spezifikation für Quality of Experience Monitoring Server Protocol</em>, die zum Download zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="8c387-137">For details, refer to the <em>Quality of Experience Monitoring Server Protocol Specification</em>, available for download.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-138"><strong>Sicherheit</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-138"><strong>Security</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-139">tinyint</span><span class="sxs-lookup"><span data-stu-id="8c387-139">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8c387-140">Das verwendete Sicherheitsprofil.</span><span class="sxs-lookup"><span data-stu-id="8c387-140">The security profile in use.</span></span> <span data-ttu-id="8c387-141">0 ist None, 1 ist SRTP, 2 ist v1.</span><span class="sxs-lookup"><span data-stu-id="8c387-141">0 is NONE, 1 is SRTP, 2 is V1.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-142"><strong>Transport</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-142"><strong>Transport</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-143">tinyint</span><span class="sxs-lookup"><span data-stu-id="8c387-143">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8c387-144">0 ist UDP, 1 ist TCP.</span><span class="sxs-lookup"><span data-stu-id="8c387-144">0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-145"><strong>CallerIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-145"><strong>CallerIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-146">int</span><span class="sxs-lookup"><span data-stu-id="8c387-146">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-147">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-147">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-148">Die IP-Adresse des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="8c387-148">IP Address of the caller.</span></span> <span data-ttu-id="8c387-149">Weitere Informationen finden Sie <a href="lync-server-2013-ipaddress-table.md">in der Tabelle IPAddress in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8c387-149">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-150"><strong>CallerPort</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-150"><strong>CallerPort</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-151">int</span><span class="sxs-lookup"><span data-stu-id="8c387-151">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8c387-152">Der vom Aufrufer verwendete Port.</span><span class="sxs-lookup"><span data-stu-id="8c387-152">Port used by the caller.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-153"><strong>CallerSubnet</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-153"><strong>CallerSubnet</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-154">int</span><span class="sxs-lookup"><span data-stu-id="8c387-154">int</span></span></p></td>
<td><p> <span data-ttu-id="8c387-155">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-155">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-156">Das Subnetz des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="8c387-156">The subnet of the caller.</span></span> <span data-ttu-id="8c387-157">Weitere Informationen finden Sie <a href="lync-server-2013-ipaddress-table.md">in der Tabelle IPAddress in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8c387-157">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-158"><strong>CallerInside</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-158"><strong>CallerInside</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-159">bit</span><span class="sxs-lookup"><span data-stu-id="8c387-159">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8c387-160">1 bedeutet, dass der Anrufer sich innerhalb des Unternehmensnetzwerks befindet, 0 bedeutet, dass sich der Anrufer außerhalb des Netzwerks befindet.</span><span class="sxs-lookup"><span data-stu-id="8c387-160">1 means caller is inside the enterprise network, 0 means the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-161"><strong>CallerMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-161"><strong>CallerMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-162">int</span><span class="sxs-lookup"><span data-stu-id="8c387-162">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-163">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-163">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-164">Die Mac-Adresse des Anrufers, auf die von der <a href="lync-server-2013-macaddress-table.md">macaddress-Tabelle in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8c387-164">Caller’s mac address, referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-165"><strong>CallerRelayIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-165"><strong>CallerRelayIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-166">int</span><span class="sxs-lookup"><span data-stu-id="8c387-166">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-167">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-167">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-168">Die IP-Adresse des vom Aufrufer verwendeten lync Server A/V-Edgedienst.</span><span class="sxs-lookup"><span data-stu-id="8c387-168">IP Address of the Lync Server A/V Edge service used by the caller.</span></span> <span data-ttu-id="8c387-169">Weitere Informationen finden Sie <a href="lync-server-2013-ipaddress-table.md">in der Tabelle IPAddress in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8c387-169">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-170"><strong>CallerRelayPort</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-170"><strong>CallerRelayPort</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-171">int</span><span class="sxs-lookup"><span data-stu-id="8c387-171">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8c387-172">Port, der vom Anrufer für den A/V-Edgedienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c387-172">Port used on the A/V Edge service by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-173"><strong>CallerCaptureDev</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-173"><strong>CallerCaptureDev</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-174">int</span><span class="sxs-lookup"><span data-stu-id="8c387-174">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-175">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-176">Das vom Anrufer verwendete Aufnahmegerät.</span><span class="sxs-lookup"><span data-stu-id="8c387-176">Capture device used by the caller.</span></span> <span data-ttu-id="8c387-177">Wird in der <a href="lync-server-2013-device-table.md">Gerätetabelle in lync Server 2013</a>referenziert.</span><span class="sxs-lookup"><span data-stu-id="8c387-177">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-178"><strong>CallerRenderDev</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-178"><strong>CallerRenderDev</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-179">int</span><span class="sxs-lookup"><span data-stu-id="8c387-179">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-180">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-180">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-181">Vom Aufrufer verwendetes Render-Gerät.</span><span class="sxs-lookup"><span data-stu-id="8c387-181">Render device used by caller.</span></span> <span data-ttu-id="8c387-182">Wird in der <a href="lync-server-2013-device-table.md">Gerätetabelle in lync Server 2013</a>referenziert.</span><span class="sxs-lookup"><span data-stu-id="8c387-182">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-183"><strong>CallerCaptureDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-183"><strong>CallerCaptureDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-184">int</span><span class="sxs-lookup"><span data-stu-id="8c387-184">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-185">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-185">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-186">Treiber für das Aufnahmegerät des Anrufers, auf das von der <a href="lync-server-2013-devicedriver-table.md">ACPITreiber-Tabelle in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8c387-186">Driver for the caller’s capture device, referenced from the <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-187"><strong>CallerRenderDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-187"><strong>CallerRenderDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-188">int</span><span class="sxs-lookup"><span data-stu-id="8c387-188">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-189">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-189">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-190">Treiber für das Render-Gerät des Anrufers, auf das von der <a href="lync-server-2013-devicedriver-table.md">ACPITreiber-Tabelle in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="8c387-190">Driver for the caller’s render device, referenced from the <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-191"><strong>CallerNetworkConnectionType</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-191"><strong>CallerNetworkConnectionType</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-192">tinyint</span><span class="sxs-lookup"><span data-stu-id="8c387-192">tinyint</span></span></p></td>
<td><p><span data-ttu-id="8c387-193">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-194">Gibt an, wie der Anrufer mit dem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="8c387-194">Indicates how the caller connected to the network.</span></span> <span data-ttu-id="8c387-195">Werte werden <a href="lync-server-2013-networkconnectiondetail-table.md">in der NetworkConnectionDetail-Tabelle in lync Server 2013</a>abgerufen.</span><span class="sxs-lookup"><span data-stu-id="8c387-195">Values are obtained from the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a>.</span></span> <span data-ttu-id="8c387-196">Typische Werte sind 0 für eine kabelgebundene Verbindung "1 für eine WLAN-Verbindung; und 3 für eine Ethernet-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="8c387-196">Typical values are 0 for a wired connection’ 1 for a WiFi connection; and 3 for an Ethernet connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-197"><strong>CallerBssid</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-197"><strong>CallerBssid</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-198">int</span><span class="sxs-lookup"><span data-stu-id="8c387-198">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-199">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-199">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-200">BSSID des Anrufers, wenn Wireless verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c387-200">Caller’s BSSID if wireless is used.</span></span> <span data-ttu-id="8c387-201">Referenziert aus der <a href="lync-server-2013-macaddress-table.md">macaddress-Tabelle in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8c387-201">Referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-202"><strong>CallerVPN</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-202"><strong>CallerVPN</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-203">bit</span><span class="sxs-lookup"><span data-stu-id="8c387-203">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8c387-204">Der Link des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="8c387-204">The caller's link.</span></span> <span data-ttu-id="8c387-205">1 ist ein VPN (virtuelles privates Netzwerk), 0 ist kein VPN.</span><span class="sxs-lookup"><span data-stu-id="8c387-205">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-206"><strong>CallerLinkSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-206"><strong>CallerLinkSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-207">Decimal (18; 0)</span><span class="sxs-lookup"><span data-stu-id="8c387-207">decimal(18,0)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8c387-208">Die Netzwerkverbindungsgeschwindigkeit in BPS für den Endpunkt des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="8c387-208">The network link speed, in bps, for the caller's endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-209"><strong>CalleeIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-209"><strong>CalleeIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-210">int</span><span class="sxs-lookup"><span data-stu-id="8c387-210">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-211">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-211">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-212">Die IP-Adresse des anrufempfängers.</span><span class="sxs-lookup"><span data-stu-id="8c387-212">IP Address of the call receiver.</span></span> <span data-ttu-id="8c387-213">Weitere Informationen finden Sie <a href="lync-server-2013-ipaddress-table.md">in der Tabelle IPAddress in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8c387-213">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-214"><strong>CalleePort</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-214"><strong>CalleePort</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-215">bit</span><span class="sxs-lookup"><span data-stu-id="8c387-215">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8c387-216">Der vom Anrufempfänger verwendete Port.</span><span class="sxs-lookup"><span data-stu-id="8c387-216">Port used by the call receiver.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-217"><strong>CalleeSubnet</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-217"><strong>CalleeSubnet</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-218">int</span><span class="sxs-lookup"><span data-stu-id="8c387-218">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-219">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-219">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-220">Subnetz der aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="8c387-220">Subnet of callee.</span></span> <span data-ttu-id="8c387-221">Weitere Informationen finden Sie <a href="lync-server-2013-ipaddress-table.md">in der Tabelle IPAddress in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8c387-221">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-222"><strong>CalleeInside</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-222"><strong>CalleeInside</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-223">bit</span><span class="sxs-lookup"><span data-stu-id="8c387-223">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8c387-224">1 bedeutet, dass der Anrufempfänger sich innerhalb des Unternehmensnetzwerks befindet, 0 bedeutet, dass der Anrufempfänger sich außerhalb des Netzwerks befindet.</span><span class="sxs-lookup"><span data-stu-id="8c387-224">1 means call receiver is inside the enterprise network, 0 means the call receiver is outside the network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-225"><strong>CalleeMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-225"><strong>CalleeMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-226">int</span><span class="sxs-lookup"><span data-stu-id="8c387-226">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-227">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-227">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-228">Mac-Adresse des angerufenen</span><span class="sxs-lookup"><span data-stu-id="8c387-228">Callee Mac address.</span></span> <span data-ttu-id="8c387-229">Wird in der <a href="lync-server-2013-macaddress-table.md">macaddress-Tabelle in lync Server 2013</a>referenziert.</span><span class="sxs-lookup"><span data-stu-id="8c387-229">Referenced from the <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-230"><strong>CalleeRelayIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-230"><strong>CalleeRelayIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-231">int</span><span class="sxs-lookup"><span data-stu-id="8c387-231">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-232">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-232">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-233">Die IP-Adresse des A/V-Edgedienst, der vom Empfänger des Anrufs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c387-233">IP Address of the A/V Edge service used by the call receiver.</span></span> <span data-ttu-id="8c387-234">Weitere Informationen finden Sie <a href="lync-server-2013-ipaddress-table.md">in der Tabelle IPAddress in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8c387-234">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-235"><strong>CalleeRelayPort</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-235"><strong>CalleeRelayPort</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-236">int</span><span class="sxs-lookup"><span data-stu-id="8c387-236">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8c387-237">Port, der vom Anrufempfänger für den A/V-Edgedienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c387-237">Port used on the A/V Edge Service by the call receiver.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-238"><strong>CalleeCaptureDev</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-238"><strong>CalleeCaptureDev</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-239">int</span><span class="sxs-lookup"><span data-stu-id="8c387-239">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-240">fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-240">foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-241">Das vom Anrufempfänger verwendete Aufnahmegerät.</span><span class="sxs-lookup"><span data-stu-id="8c387-241">Capture device used by the call receiver.</span></span> <span data-ttu-id="8c387-242">Wird in der <a href="lync-server-2013-device-table.md">Gerätetabelle in lync Server 2013</a>referenziert.</span><span class="sxs-lookup"><span data-stu-id="8c387-242">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-243"><strong>CalleeRenderDev</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-243"><strong>CalleeRenderDev</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-244">int</span><span class="sxs-lookup"><span data-stu-id="8c387-244">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-245">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-245">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-246">Render-Gerät, das vom Empfänger des Anrufs verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c387-246">Render device used by the call receiver.</span></span> <span data-ttu-id="8c387-247">Wird in der <a href="lync-server-2013-device-table.md">Gerätetabelle in lync Server 2013</a>referenziert.</span><span class="sxs-lookup"><span data-stu-id="8c387-247">Referenced from the <a href="lync-server-2013-device-table.md">Device table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-248"><strong>CalleeCaptureDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-248"><strong>CalleeCaptureDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-249">int</span><span class="sxs-lookup"><span data-stu-id="8c387-249">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-250">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-250">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-251">Treiber für das Aufnahmegerät des anrufempfängers.</span><span class="sxs-lookup"><span data-stu-id="8c387-251">Driver for the call receiver’s capture device.</span></span> <span data-ttu-id="8c387-252">Referenziert aus der <a href="lync-server-2013-devicedriver-table.md">ACPITreiber-Tabelle in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8c387-252">Referenced from <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-253"><strong>CalleeRenderDevDriver</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-253"><strong>CalleeRenderDevDriver</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-254">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="8c387-254">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="8c387-255">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-255">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-256">Treiber für das Render-Gerät des anrufempfängers.</span><span class="sxs-lookup"><span data-stu-id="8c387-256">Driver for the call receiver’s render device.</span></span> <span data-ttu-id="8c387-257">Referenziert aus der <a href="lync-server-2013-devicedriver-table.md">ACPITreiber-Tabelle in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8c387-257">Referenced from <a href="lync-server-2013-devicedriver-table.md">DeviceDriver table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-258"><strong>CalleeNetworkConnectionType</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-258"><strong>CalleeNetworkConnectionType</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-259">tinyint</span><span class="sxs-lookup"><span data-stu-id="8c387-259">tinyint</span></span></p></td>
<td><p><span data-ttu-id="8c387-260">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-260">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-261">Gibt an, wie der aufgerufene mit dem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="8c387-261">Indicates how the callee connected to the network.</span></span> <span data-ttu-id="8c387-262">Werte werden <a href="lync-server-2013-networkconnectiondetail-table.md">in der NetworkConnectionDetail-Tabelle in lync Server 2013</a>abgerufen.</span><span class="sxs-lookup"><span data-stu-id="8c387-262">Values are obtained from the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a>.</span></span> <span data-ttu-id="8c387-263">Typische Werte sind 0 für eine kabelgebundene Verbindung "1 für eine WLAN-Verbindung; und 3 für eine Ethernet-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="8c387-263">Typical values are 0 for a wired connection’ 1 for a WiFi connection; and 3 for an Ethernet connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-264"><strong>CalleeBssid</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-264"><strong>CalleeBssid</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-265">int</span><span class="sxs-lookup"><span data-stu-id="8c387-265">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-266">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-266">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-267">BSSID des anrufempfängers, wenn Wireless verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8c387-267">Callee’s BSSID if wireless is used.</span></span> <span data-ttu-id="8c387-268">Referenziert aus der <a href="lync-server-2013-macaddress-table.md">macaddress-Tabelle in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8c387-268">Referenced from <a href="lync-server-2013-macaddress-table.md">MacAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-269"><strong>CalleeVPN</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-269"><strong>CalleeVPN</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-270">bit</span><span class="sxs-lookup"><span data-stu-id="8c387-270">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8c387-271">Link des anrufempfängers; 1 ist ein VPN (virtuelles privates Netzwerk), 0 ist kein VPN.</span><span class="sxs-lookup"><span data-stu-id="8c387-271">The call receiver’s link; 1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-272"><strong>CalleeLinkSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-272"><strong>CalleeLinkSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-273">Decimal (18; 0)</span><span class="sxs-lookup"><span data-stu-id="8c387-273">decimal(18,0)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8c387-274">Die Netzwerkverbindungsgeschwindigkeit in BPS für den Endpunkt des anrufempfängers.</span><span class="sxs-lookup"><span data-stu-id="8c387-274">The network link speed, in bps, for the call receiver’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-275"><strong>ConversationalMOS</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-275"><strong>ConversationalMOS</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-276">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="8c387-276">decimal(3,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8c387-277">Schmalband-Konversations-Mos der audiositzungen (basierend auf beiden Audiostreams).</span><span class="sxs-lookup"><span data-stu-id="8c387-277">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-278"><strong>AppliedBandwidthLimit</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-278"><strong>AppliedBandwidthLimit</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-279">int</span><span class="sxs-lookup"><span data-stu-id="8c387-279">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8c387-280">Hierbei handelt es sich um die tatsächliche Bandbreite, die auf den angegebenen Send-Seitenstrom angewendet wird, wobei verschiedene Richtlinieneinstellungen angegeben werden (Turn, API, SDP, Richtlinien Server usw.).</span><span class="sxs-lookup"><span data-stu-id="8c387-280">This is the actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, and so on).</span></span> <span data-ttu-id="8c387-281">Dies sollte nicht mit der effektiven Bandbreite verwechselt werden, da auf der Grundlage der Bandbreitenschätzung eine geringere effektive Bandbreite vorhanden sein kann.</span><span class="sxs-lookup"><span data-stu-id="8c387-281">This is not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="8c387-282">Dies ist im Grunde die maximale Bandbreite, die der sendedatenstrom sperren kann, wenn die Bandbreite geschätzt wird.</span><span class="sxs-lookup"><span data-stu-id="8c387-282">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-283"><strong>AppliedBandwidthSourceKey</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-283"><strong>AppliedBandwidthSourceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-284">smallint</span><span class="sxs-lookup"><span data-stu-id="8c387-284">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8c387-285">Hierbei handelt es sich um die Quelle des verhängten Bandbreitenlimits.</span><span class="sxs-lookup"><span data-stu-id="8c387-285">This is the source of the bandwidth cap being imposed.</span></span> <span data-ttu-id="8c387-286">Es wird beschrieben, woher die Bandbreitengrenze stammt ("Richtlinienserver", "Server umwandeln", "Modalität" usw.).</span><span class="sxs-lookup"><span data-stu-id="8c387-286">It describes where the bandwidth limit is coming from (“Policy Server”, “TURN Server”, “Modality”, and so on).</span></span> <span data-ttu-id="8c387-287">Wird in der <a href="lync-server-2013-appliedbandwidthsource-table.md">AppliedBandwidthSource-Tabelle in lync Server 2013</a>referenziert.</span><span class="sxs-lookup"><span data-stu-id="8c387-287">Referenced from the <a href="lync-server-2013-appliedbandwidthsource-table.md">AppliedBandwidthSource table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-288"><strong>Anrufer</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-288"><strong>Caller</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-289">bit</span><span class="sxs-lookup"><span data-stu-id="8c387-289">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8c387-290">Gibt an, ob Metriken des Anrufers empfangen wurden; 1 ist ja, ein NULL-Wert ist "Nein".</span><span class="sxs-lookup"><span data-stu-id="8c387-290">Indicates whether metrics from the caller were received; 1 is yes, a null value is no.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-291"><strong>Callee</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-291"><strong>Callee</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-292">bit</span><span class="sxs-lookup"><span data-stu-id="8c387-292">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="8c387-293">Gibt an, ob Metriken vom Anrufempfänger empfangen wurden; 1 ist ja, ein NULL-Wert ist "Nein".</span><span class="sxs-lookup"><span data-stu-id="8c387-293">Indicates whether metrics from the call receiver were received; 1 is yes, a null value is no.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-294"><strong>MidCallReport</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-294"><strong>MidCallReport</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-295">bit</span><span class="sxs-lookup"><span data-stu-id="8c387-295">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8c387-296">Gibt an, ob der Bericht für einen Teil der Sitzung oder für die vollständige Sitzung gilt.</span><span class="sxs-lookup"><span data-stu-id="8c387-296">Indicates whether the report is for a portion of the session or for the complete session.</span></span></p>
<p><span data-ttu-id="8c387-297">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8c387-297">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-298"><strong>ClassifiedPoorCall</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-298"><strong>ClassifiedPoorCall</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-299">bit</span><span class="sxs-lookup"><span data-stu-id="8c387-299">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8c387-300">Gibt an, ob ein Anruf als schlechter Anruf (Wert 1) oder als guter Anruf (0) klassifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="8c387-300">Indicates whether a call was classified as a poor call (value of 1) or as a good call (0).</span></span></p>
<p><span data-ttu-id="8c387-301">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8c387-301">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-302"><strong>CallerConnectivityICE</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-302"><strong>CallerConnectivityICE</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-303">tinyInt</span><span class="sxs-lookup"><span data-stu-id="8c387-303">tinyInt</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8c387-304">Gibt an, ob der Anrufer über das Ice-Protokoll (Internet Connectivity Establishment) mit dem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="8c387-304">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p>
<p><span data-ttu-id="8c387-305">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8c387-305">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-306"><strong>CalleeConnectivityICE</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-306"><strong>CalleeConnectivityICE</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-307">tinyint</span><span class="sxs-lookup"><span data-stu-id="8c387-307">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8c387-308">Gibt an, ob der Anrufer über das Ice-Protokoll (Internet Connectivity Establishment) mit dem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="8c387-308">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p>
<p><span data-ttu-id="8c387-309">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8c387-309">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-310"><strong>CallerReflexiveLocalIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-310"><strong>CallerReflexiveLocalIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-311">int</span><span class="sxs-lookup"><span data-stu-id="8c387-311">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-312">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-312">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-313">Reflexive IP-Adresse des Benutzers, der den Anruf getätigt hat.</span><span class="sxs-lookup"><span data-stu-id="8c387-313">Reflexive IP address of the user who placed the call.</span></span> <span data-ttu-id="8c387-314">In Organisationen, die NAT verwenden (Netzwerkadressübersetzung), ist die reflexive IP-Adresse die IP-Adresse des Proxyservers.</span><span class="sxs-lookup"><span data-stu-id="8c387-314">In organizations that use NAT (network address translation), the reflexive IP address is the IP address of the proxy server.</span></span></p>
<p><span data-ttu-id="8c387-315">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8c387-315">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-316"><strong>CallerWiFiDriverDevicesDesc</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-316"><strong>CallerWiFiDriverDevicesDesc</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-317">int</span><span class="sxs-lookup"><span data-stu-id="8c387-317">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-318">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-318">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-319">Gerätebeschreibung für den WiFi-Treiber des Benutzers, der den Anruf getätigt hat.</span><span class="sxs-lookup"><span data-stu-id="8c387-319">Device description for the WiFi driver employed by the user who placed the call.</span></span></p>
<p><span data-ttu-id="8c387-320">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8c387-320">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-321"><strong>CallerWiFiDriverVersion</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-321"><strong>CallerWiFiDriverVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-322">int</span><span class="sxs-lookup"><span data-stu-id="8c387-322">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-323">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-323">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-324">Die Versionsnummer des WLAN-Treibers, der vom Nutzer, der den Anruf getätigt hat, verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="8c387-324">Version number for the WiFi driver employed by the user who placed the call.</span></span></p>
<p><span data-ttu-id="8c387-325">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8c387-325">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-326"><strong>CalleReflexiveLocalIPAddr</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-326"><strong>CalleReflexiveLocalIPAddr</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-327">int</span><span class="sxs-lookup"><span data-stu-id="8c387-327">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-328">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-328">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-329">Reflexive IP-Adresse des Benutzers, der den Anruf erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="8c387-329">Reflexive IP address of the user who received the call.</span></span> <span data-ttu-id="8c387-330">In Organisationen, die NAT verwenden (Netzwerkadressübersetzung), ist die reflexive IP-Adresse die IP-Adresse des Proxyservers.</span><span class="sxs-lookup"><span data-stu-id="8c387-330">In organizations that use NAT (network address translation), the reflexive IP address is the IP address of the proxy server.</span></span></p>
<p><span data-ttu-id="8c387-331">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8c387-331">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8c387-332"><strong>CalleeWiFiDriverDevicesDesc</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-332"><strong>CalleeWiFiDriverDevicesDesc</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-333">int</span><span class="sxs-lookup"><span data-stu-id="8c387-333">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-334">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-334">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-335">Gerätebeschreibung für den WiFi-Treiber des Benutzers, der den Anruf erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="8c387-335">Device description for the WiFi driver employed by the user who received the call.</span></span></p>
<p><span data-ttu-id="8c387-336">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8c387-336">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8c387-337"><strong>CalleeWiFiDriverVersion</strong></span><span class="sxs-lookup"><span data-stu-id="8c387-337"><strong>CalleeWiFiDriverVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="8c387-338">int</span><span class="sxs-lookup"><span data-stu-id="8c387-338">int</span></span></p></td>
<td><p><span data-ttu-id="8c387-339">Fremd</span><span class="sxs-lookup"><span data-stu-id="8c387-339">Foreign</span></span></p></td>
<td><p><span data-ttu-id="8c387-340">Die Versionsnummer des WLAN-Treibers, der vom Nutzer, der den Anruf erhalten hat, verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="8c387-340">Version number for the WiFi driver employed by the user who received the call.</span></span></p>
<p><span data-ttu-id="8c387-341">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="8c387-341">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="8c387-342">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8c387-342">


</div>

<span> </span>

</div>

</div>

</span></span></div>

