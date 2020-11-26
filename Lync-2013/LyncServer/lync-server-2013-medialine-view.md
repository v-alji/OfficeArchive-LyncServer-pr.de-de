---
title: 'Lync Server 2013: Medienansicht'
description: 'Lync Server 2013: medialinie-Ansicht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaLine view
ms:assetid: 132eca13-8913-4218-9eff-4960ced8c3dc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687972(v=OCS.15)
ms:contentKeyID: 49733560
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c61fcc15b46958622e6cddd66427255a6def154
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445946"
---
# <a name="medialine-view-in-lync-server-2013"></a><span data-ttu-id="14aa0-103">Medienansicht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14aa0-103">MediaLine view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="14aa0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="14aa0-104">

<span> </span></span></span>

<span data-ttu-id="14aa0-105">_**Letztes Änderungsdatum des Themas:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="14aa0-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="14aa0-106">In der medialinie-Ansicht werden Informationen zu jeder medienzeile in der Datenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14aa0-106">The MediaLine View stores information about each media line in the database.</span></span> <span data-ttu-id="14aa0-107">Eine Audiositzung enthält in der Regel eine Audio-medienzeile.</span><span class="sxs-lookup"><span data-stu-id="14aa0-107">One audio session typically contains one audio media line.</span></span> <span data-ttu-id="14aa0-108">Eine Audio-und Video (A/V)-Sitzung enthält in der Regel eine Audio-medienzeile und eine Video medienzeile. die Sitzung kann jedoch zwei Video Medien Linien enthalten, wenn ein Konferenzgerät verwendet wird oder wenn die Katalogansicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="14aa0-108">One audio and video (A/V) session typically contains one audio media line and one video media line; however, the session might contain two video media lines if a conferencing device is used or if Gallery View is used.</span></span> <span data-ttu-id="14aa0-109">Diese Ansicht wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="14aa0-109">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="14aa0-110">Spalte</span><span class="sxs-lookup"><span data-stu-id="14aa0-110">Column</span></span></th>
<th><span data-ttu-id="14aa0-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="14aa0-111">Data Type</span></span></th>
<th><span data-ttu-id="14aa0-112">Details</span><span class="sxs-lookup"><span data-stu-id="14aa0-112">details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-113">ConferenceDateTime</span><span class="sxs-lookup"><span data-stu-id="14aa0-113">ConferenceDateTime</span></span></p></td>
<td><p><span data-ttu-id="14aa0-114">datetime</span><span class="sxs-lookup"><span data-stu-id="14aa0-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="14aa0-115">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="14aa0-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-116">SessionSeq</span><span class="sxs-lookup"><span data-stu-id="14aa0-116">SessionSeq</span></span></p></td>
<td><p><span data-ttu-id="14aa0-117">int</span><span class="sxs-lookup"><span data-stu-id="14aa0-117">int</span></span></p></td>
<td><p><span data-ttu-id="14aa0-118">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="14aa0-118">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-119">MediaLineLabel</span><span class="sxs-lookup"><span data-stu-id="14aa0-119">MediaLineLabel</span></span></p></td>
<td><p><span data-ttu-id="14aa0-120">tinyint</span><span class="sxs-lookup"><span data-stu-id="14aa0-120">tinyint</span></span></p></td>
<td><p><span data-ttu-id="14aa0-121">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="14aa0-121">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-122">CallerIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="14aa0-122">CallerIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="14aa0-123">int</span><span class="sxs-lookup"><span data-stu-id="14aa0-123">int</span></span></p></td>
<td><p><span data-ttu-id="14aa0-124">Informationen zum Prozess der interaktiven Verbindungseinrichtung (ICE), der unter Bits-Flags für den Aufrufer beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="14aa0-124">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the caller.</span></span> <span data-ttu-id="14aa0-125">Ausführliche Informationen finden Sie in der Quality of Experience Monitoring Server Protocol-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="14aa0-125">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-126">CalleeIceWarningFlags</span><span class="sxs-lookup"><span data-stu-id="14aa0-126">CalleeIceWarningFlags</span></span></p></td>
<td><p><span data-ttu-id="14aa0-127">int</span><span class="sxs-lookup"><span data-stu-id="14aa0-127">int</span></span></p></td>
<td><p><span data-ttu-id="14aa0-128">Informationen zum Prozess der interaktiven Verbindungseinrichtung (ICE), der in den Bits-Flags für den aufgerufenen beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="14aa0-128">Information about Interactive Connectivity Establishment (ICE) process described in bits flags for the callee.</span></span> <span data-ttu-id="14aa0-129">Ausführliche Informationen finden Sie in der Quality of Experience Monitoring Server Protocol-Spezifikation.</span><span class="sxs-lookup"><span data-stu-id="14aa0-129">For details, refer to the Quality of Experience Monitoring Server Protocol Specification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-130">Sicherheit</span><span class="sxs-lookup"><span data-stu-id="14aa0-130">Security</span></span></p></td>
<td><p><span data-ttu-id="14aa0-131">tinyint</span><span class="sxs-lookup"><span data-stu-id="14aa0-131">tinyint</span></span></p></td>
<td><p><span data-ttu-id="14aa0-132">Verwendetes Sicherheitsprofil</span><span class="sxs-lookup"><span data-stu-id="14aa0-132">Security profile in use.</span></span> <span data-ttu-id="14aa0-133">0 ist None, 1 ist SRTP, 2 ist v1.</span><span class="sxs-lookup"><span data-stu-id="14aa0-133">0 is NONE, 1 is SRTP, 2 is V1.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-134">Transport</span><span class="sxs-lookup"><span data-stu-id="14aa0-134">Transport</span></span></p></td>
<td><p><span data-ttu-id="14aa0-135">tinyint</span><span class="sxs-lookup"><span data-stu-id="14aa0-135">tinyint</span></span></p></td>
<td><p><span data-ttu-id="14aa0-136">Transporttyp.</span><span class="sxs-lookup"><span data-stu-id="14aa0-136">Transport type.</span></span> <span data-ttu-id="14aa0-137">0 ist UDP, 1 ist TCP.</span><span class="sxs-lookup"><span data-stu-id="14aa0-137">0 is UDP, 1 is TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-138">CallerIPAddr</span><span class="sxs-lookup"><span data-stu-id="14aa0-138">CallerIPAddr</span></span></p></td>
<td><p><span data-ttu-id="14aa0-139">var (50)</span><span class="sxs-lookup"><span data-stu-id="14aa0-139">var(50)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-140">Die IP-Adresse des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="14aa0-140">IP address of the caller.</span></span> <span data-ttu-id="14aa0-141">Dies kann eine IPv4-oder IPv6-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="14aa0-141">This can be either an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-142">CallerPort</span><span class="sxs-lookup"><span data-stu-id="14aa0-142">CallerPort</span></span></p></td>
<td><p><span data-ttu-id="14aa0-143">int</span><span class="sxs-lookup"><span data-stu-id="14aa0-143">int</span></span></p></td>
<td><p><span data-ttu-id="14aa0-144">Der vom Aufrufer verwendete Port.</span><span class="sxs-lookup"><span data-stu-id="14aa0-144">Port used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-145">CallerInside</span><span class="sxs-lookup"><span data-stu-id="14aa0-145">CallerInside</span></span></p></td>
<td><p><span data-ttu-id="14aa0-146">bit</span><span class="sxs-lookup"><span data-stu-id="14aa0-146">bit</span></span></p></td>
<td><p><span data-ttu-id="14aa0-147">Gibt an, ob sich der Anrufer innerhalb des Organisationsnetzwerks befindet.</span><span class="sxs-lookup"><span data-stu-id="14aa0-147">Indicates whether or not the caller is inside the organization network.</span></span> <span data-ttu-id="14aa0-148">1 bedeutet, dass sich der Anrufer innerhalb des Unternehmensnetzwerks befindet.</span><span class="sxs-lookup"><span data-stu-id="14aa0-148">1 means that the caller is inside the enterprise network.</span></span> <span data-ttu-id="14aa0-149">0 bedeutet, dass sich der Anrufer außerhalb des Netzwerks befindet.</span><span class="sxs-lookup"><span data-stu-id="14aa0-149">0 means that the caller is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-150">CallerMacAddress</span><span class="sxs-lookup"><span data-stu-id="14aa0-150">CallerMacAddress</span></span></p></td>
<td><p><span data-ttu-id="14aa0-151">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="14aa0-151">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-152">Mac-Adresse der vom Anrufer verwendeten Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="14aa0-152">MAC address of network interface used by caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-153">CallerRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="14aa0-153">CallerRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="14aa0-154">var (50)</span><span class="sxs-lookup"><span data-stu-id="14aa0-154">var(50)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-155">Die IP-Adresse des A/V-Edgedienst, der vom Aufrufer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="14aa0-155">IP Address of the A/V Edge service used by the caller.</span></span> <span data-ttu-id="14aa0-156">Weitere Informationen finden Sie <a href="lync-server-2013-ipaddress-table.md">in der Tabelle IPAddress in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="14aa0-156">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-157">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="14aa0-157">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="14aa0-158">int</span><span class="sxs-lookup"><span data-stu-id="14aa0-158">int</span></span></p></td>
<td><p><span data-ttu-id="14aa0-159">Der Port des A/V-Edgedienst, der vom Aufrufer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="14aa0-159">Port used on the A/V Edge service used by the caller.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-160">CallerReflexiveIPAddr</span><span class="sxs-lookup"><span data-stu-id="14aa0-160">CallerReflexiveIPAddr</span></span></p></td>
<td><p><span data-ttu-id="14aa0-161">var (50)</span><span class="sxs-lookup"><span data-stu-id="14aa0-161">var(50)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-162">Die IP-Adresse des Anrufers, wie er vom A/V-Edgedienst gemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="14aa0-162">Caller’s IP address as reported by the A/V Edge service.</span></span> <span data-ttu-id="14aa0-163">Diese Adresse kann sich von der CallerIPAddr unterscheiden, wenn sich der Client beispielsweise hinter einem NAT befindet.</span><span class="sxs-lookup"><span data-stu-id="14aa0-163">This address may be different that the CallerIPAddr if the client is located behind a NAT for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-164">CallerCaptureDev</span><span class="sxs-lookup"><span data-stu-id="14aa0-164">CallerCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="14aa0-165">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="14aa0-165">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-166">Name des Aufnahmegeräts des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="14aa0-166">Caller’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-167">CallerRenderDev</span><span class="sxs-lookup"><span data-stu-id="14aa0-167">CallerRenderDev</span></span></p></td>
<td><p><span data-ttu-id="14aa0-168">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="14aa0-168">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-169">Name des Render-Geräts des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="14aa0-169">Caller’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-170">CallerCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="14aa0-170">CallerCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="14aa0-171">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="14aa0-171">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-172">Name des Aufnahmegeräte Treibers des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="14aa0-172">Caller’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-173">CallerRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="14aa0-173">CallerRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="14aa0-174">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="14aa0-174">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-175">Name des Render-Gerätetreibers des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="14aa0-175">Caller’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-176">CallerWifiDriverDeviceDesc</span><span class="sxs-lookup"><span data-stu-id="14aa0-176">CallerWifiDriverDeviceDesc</span></span></p></td>
<td><p><span data-ttu-id="14aa0-177">varchar (256</span><span class="sxs-lookup"><span data-stu-id="14aa0-177">varchar(256</span></span></p></td>
<td><p><span data-ttu-id="14aa0-178">Beschreibung des WLAN-Treibers des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="14aa0-178">Caller’s Wifi driver description.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-179">CallerWifiDriverVersion</span><span class="sxs-lookup"><span data-stu-id="14aa0-179">CallerWifiDriverVersion</span></span></p></td>
<td><p><span data-ttu-id="14aa0-180">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="14aa0-180">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-181">WLAN-Treiberversion des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="14aa0-181">Caller’s Wifi driver version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-182">CalleeNetworkConnectionDetail</span><span class="sxs-lookup"><span data-stu-id="14aa0-182">CalleeNetworkConnectionDetail</span></span></p></td>
<td><p><span data-ttu-id="14aa0-183">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="14aa0-183">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-184">Details zur Netzwerkverbindung des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="14aa0-184">Details of caller’s network connection.</span></span> <span data-ttu-id="14aa0-185">Weitere Informationen finden Sie <a href="lync-server-2013-networkconnectiondetail-table.md">in der NetworkConnectionDetail-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="14aa0-185">See the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-186">CallerBssid</span><span class="sxs-lookup"><span data-stu-id="14aa0-186">CallerBssid</span></span></p></td>
<td><p><span data-ttu-id="14aa0-187">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="14aa0-187">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-188">Grundlegende Dienst Satzkennung, die von der WLAN-Verbindung der Anrufer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="14aa0-188">Basic Service Set Identifier used by callers WiFi connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-189">CallerVPN</span><span class="sxs-lookup"><span data-stu-id="14aa0-189">CallerVPN</span></span></p></td>
<td><p><span data-ttu-id="14aa0-190">bit</span><span class="sxs-lookup"><span data-stu-id="14aa0-190">bit</span></span></p></td>
<td><p><span data-ttu-id="14aa0-191">Gibt an, ob der Anrufer über ein virtuelles privates Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="14aa0-191">Indicates whether the caller connected over a virtual private network.</span></span> <span data-ttu-id="14aa0-192">1 ist ein VPN (virtuelles privates Netzwerk), 0 ist kein VPN.</span><span class="sxs-lookup"><span data-stu-id="14aa0-192">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-193">CalleeIPAddr</span><span class="sxs-lookup"><span data-stu-id="14aa0-193">CalleeIPAddr</span></span></p></td>
<td><p><span data-ttu-id="14aa0-194">var (50)</span><span class="sxs-lookup"><span data-stu-id="14aa0-194">var(50)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-195">Die IP-Adresse des aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="14aa0-195">IP address of the callee.</span></span> <span data-ttu-id="14aa0-196">Dies kann eine IPv4-oder IPv6-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="14aa0-196">This can be either an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-197">CalleePort</span><span class="sxs-lookup"><span data-stu-id="14aa0-197">CalleePort</span></span></p></td>
<td><p><span data-ttu-id="14aa0-198">int</span><span class="sxs-lookup"><span data-stu-id="14aa0-198">int</span></span></p></td>
<td><p><span data-ttu-id="14aa0-199">Port, der vom aufgerufenen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="14aa0-199">Port used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-200">CalleeInside</span><span class="sxs-lookup"><span data-stu-id="14aa0-200">CalleeInside</span></span></p></td>
<td><p><span data-ttu-id="14aa0-201">bit</span><span class="sxs-lookup"><span data-stu-id="14aa0-201">bit</span></span></p></td>
<td><p><span data-ttu-id="14aa0-202">Gibt an, ob sich der aufgerufene innerhalb des Unternehmensnetzwerks befindet.</span><span class="sxs-lookup"><span data-stu-id="14aa0-202">Indicates whether the callee is inside the enterprise network.</span></span> <span data-ttu-id="14aa0-203">1 bedeutet, dass der Anrufer sich innerhalb des Unternehmensnetzwerks befindet, 0 bedeutet, dass der Anrufer sich außerhalb des Netzwerks befindet.</span><span class="sxs-lookup"><span data-stu-id="14aa0-203">1 means callee is inside the enterprise network, 0 means the callee is outside the network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-204">CalleeMacAddress</span><span class="sxs-lookup"><span data-stu-id="14aa0-204">CalleeMacAddress</span></span></p></td>
<td><p><span data-ttu-id="14aa0-205">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="14aa0-205">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-206">Mac-Adresse der vom aufgerufenen verwendeten Netzwerkschnittstelle.</span><span class="sxs-lookup"><span data-stu-id="14aa0-206">MAC address of network interface used by callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-207">CalleeRelayIPAddr</span><span class="sxs-lookup"><span data-stu-id="14aa0-207">CalleeRelayIPAddr</span></span></p></td>
<td><p><span data-ttu-id="14aa0-208">var (50)</span><span class="sxs-lookup"><span data-stu-id="14aa0-208">var(50)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-209">Die IP-Adresse des A/V-Edgedienst, der vom aufgerufenen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="14aa0-209">IP Address of the A/V Edge service used by the callee.</span></span> <span data-ttu-id="14aa0-210">Weitere Informationen finden Sie <a href="lync-server-2013-ipaddress-table.md">in der Tabelle IPAddress in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="14aa0-210">See the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-211">CalleeRelayPort</span><span class="sxs-lookup"><span data-stu-id="14aa0-211">CalleeRelayPort</span></span></p></td>
<td><p><span data-ttu-id="14aa0-212">int</span><span class="sxs-lookup"><span data-stu-id="14aa0-212">int</span></span></p></td>
<td><p><span data-ttu-id="14aa0-213">Port, der für den A/V-Edgedienst verwendet wird, der vom aufgerufenen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="14aa0-213">Port used on the A/V Edge service used by the callee.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-214">CalleeReflexiveIPAddr</span><span class="sxs-lookup"><span data-stu-id="14aa0-214">CalleeReflexiveIPAddr</span></span></p></td>
<td><p><span data-ttu-id="14aa0-215">var (50)</span><span class="sxs-lookup"><span data-stu-id="14aa0-215">var(50)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-216">Die IP-Adresse des Betreibers, wie vom A/V-Edgedienst gemeldet.</span><span class="sxs-lookup"><span data-stu-id="14aa0-216">Callee’s IP address as reported by the A/V Edge service.</span></span> <span data-ttu-id="14aa0-217">Diese Adresse kann sich von der CalleeIPAddr unterscheiden, wenn sich der Client beispielsweise hinter einem NAT befindet.</span><span class="sxs-lookup"><span data-stu-id="14aa0-217">This address may be different that the CalleeIPAddr if the client is located behind a NAT for example.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-218">CalleeCaptureDev</span><span class="sxs-lookup"><span data-stu-id="14aa0-218">CalleeCaptureDev</span></span></p></td>
<td><p><span data-ttu-id="14aa0-219">var (50)</span><span class="sxs-lookup"><span data-stu-id="14aa0-219">var(50)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-220">Der Name des Erfassungsgeräts des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="14aa0-220">Callee’s capture device name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-221">CalleeRenderDev</span><span class="sxs-lookup"><span data-stu-id="14aa0-221">CalleeRenderDev</span></span></p></td>
<td><p><span data-ttu-id="14aa0-222">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="14aa0-222">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-223">Name des Render-Geräts.</span><span class="sxs-lookup"><span data-stu-id="14aa0-223">Callee’s render device name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-224">CalleeCaptureDevDriver</span><span class="sxs-lookup"><span data-stu-id="14aa0-224">CalleeCaptureDevDriver</span></span></p></td>
<td><p><span data-ttu-id="14aa0-225">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="14aa0-225">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-226">Der Name des Capture-Gerätetreibers des anrufempfängers.</span><span class="sxs-lookup"><span data-stu-id="14aa0-226">Callee’s capture device driver name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-227">CalleeRenderDevDriver</span><span class="sxs-lookup"><span data-stu-id="14aa0-227">CalleeRenderDevDriver</span></span></p></td>
<td><p><span data-ttu-id="14aa0-228">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="14aa0-228">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-229">Der Name des Render-Gerätetreibers des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="14aa0-229">Callee’s render device driver name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-230">CalleeWifiDriverDeviceDesc</span><span class="sxs-lookup"><span data-stu-id="14aa0-230">CalleeWifiDriverDeviceDesc</span></span></p></td>
<td><p><span data-ttu-id="14aa0-231">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="14aa0-231">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-232">Beschreibung des WLAN-Treibers des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="14aa0-232">Callee’s Wifi driver description.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-233">CalleeWifiDriverVersion</span><span class="sxs-lookup"><span data-stu-id="14aa0-233">CalleeWifiDriverVersion</span></span></p></td>
<td><p><span data-ttu-id="14aa0-234">varchar (256</span><span class="sxs-lookup"><span data-stu-id="14aa0-234">varchar(256</span></span></p></td>
<td><p><span data-ttu-id="14aa0-235">WLAN-Treiberversion des anrufempfängers.</span><span class="sxs-lookup"><span data-stu-id="14aa0-235">Callee’s Wifi driver version.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-236">CalleeNetworkConnectionDetail</span><span class="sxs-lookup"><span data-stu-id="14aa0-236">CalleeNetworkConnectionDetail</span></span></p></td>
<td><p><span data-ttu-id="14aa0-237">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="14aa0-237">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-238">Details zur Netzwerkverbindung des berufenen.</span><span class="sxs-lookup"><span data-stu-id="14aa0-238">Details of callee’s network connection.</span></span> <span data-ttu-id="14aa0-239">Weitere Informationen finden Sie <a href="lync-server-2013-networkconnectiondetail-table.md">in der NetworkConnectionDetail-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="14aa0-239">See the <a href="lync-server-2013-networkconnectiondetail-table.md">NetworkConnectionDetail table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-240">CalleeBssid</span><span class="sxs-lookup"><span data-stu-id="14aa0-240">CalleeBssid</span></span></p></td>
<td><p><span data-ttu-id="14aa0-241">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="14aa0-241">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-242">Grundlegende Dienst Satz-ID, die von der WLAN-Verbindung des berufenen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="14aa0-242">Basic Service Set Identifier used by callee’s WiFi connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-243">CalleeVPN</span><span class="sxs-lookup"><span data-stu-id="14aa0-243">CalleeVPN</span></span></p></td>
<td><p><span data-ttu-id="14aa0-244">bit</span><span class="sxs-lookup"><span data-stu-id="14aa0-244">bit</span></span></p></td>
<td><p><span data-ttu-id="14aa0-245">Gibt an, ob der aufgerufene über ein virtuelles privates Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="14aa0-245">Indicates whether the callee connected over a virtual private network.</span></span> <span data-ttu-id="14aa0-246">1 ist ein VPN (virtuelles privates Netzwerk), 0 ist kein VPN.</span><span class="sxs-lookup"><span data-stu-id="14aa0-246">1 is virtual private network (VPN), 0 is non-VPN.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-247">ConversationalMOS</span><span class="sxs-lookup"><span data-stu-id="14aa0-247">ConversationalMOS</span></span></p></td>
<td><p><span data-ttu-id="14aa0-248">Dezimal (3; 2)</span><span class="sxs-lookup"><span data-stu-id="14aa0-248">decimal(3,2)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-249">Schmalband-Konversations-Mos der audiositzungen (basierend auf beiden Audiostreams).</span><span class="sxs-lookup"><span data-stu-id="14aa0-249">Narrowband Conversational MOS of the audio sessions (based on both audio streams).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-250">AppliedBandwidthLimit</span><span class="sxs-lookup"><span data-stu-id="14aa0-250">AppliedBandwidthLimit</span></span></p></td>
<td><p><span data-ttu-id="14aa0-251">int</span><span class="sxs-lookup"><span data-stu-id="14aa0-251">int</span></span></p></td>
<td><p><span data-ttu-id="14aa0-252">Hierbei handelt es sich um die tatsächliche Bandbreite, die auf den angegebenen Send-Seitenstrom angewendet wird, wobei verschiedene Richtlinieneinstellungen angegeben werden (Turn, API, SDP, Richtlinien Server usw.).</span><span class="sxs-lookup"><span data-stu-id="14aa0-252">This is the actual bandwidth applied to the given send side stream given various policy settings (TURN, API, SDP, Policy Server, etc.).</span></span> <span data-ttu-id="14aa0-253">Dies sollte nicht mit der effektiven Bandbreite verwechselt werden, da auf der Grundlage der Bandbreitenschätzung eine geringere effektive Bandbreite vorhanden sein kann.</span><span class="sxs-lookup"><span data-stu-id="14aa0-253">This should not to be confused with the effective bandwidth because there can be a lower effective bandwidth based on the bandwidth estimate.</span></span> <span data-ttu-id="14aa0-254">Dies ist im Grunde die maximale Bandbreite, die der sendedatenstrom sperren kann, wenn die Bandbreite geschätzt wird.</span><span class="sxs-lookup"><span data-stu-id="14aa0-254">This is basically the maximum bandwidth the send stream can take barring limits imposed by the bandwidth estimate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-255">AppliedBandwidthSource</span><span class="sxs-lookup"><span data-stu-id="14aa0-255">AppliedBandwidthSource</span></span></p></td>
<td><p><span data-ttu-id="14aa0-256">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="14aa0-256">varchar(256)</span></span></p></td>
<td><p><span data-ttu-id="14aa0-257">Die Quelle des verhängten Bandbreitenlimits.</span><span class="sxs-lookup"><span data-stu-id="14aa0-257">Source of the bandwidth cap being imposed.</span></span> <span data-ttu-id="14aa0-258">Es wird beschrieben, woher die Bandbreitengrenze stammt (beispielsweise "Richtlinienserver", "Server umwandeln" oder "Modalität").</span><span class="sxs-lookup"><span data-stu-id="14aa0-258">It describes where the bandwidth limit is coming from (for example, “Policy Server”, “TURN Server”, or “Modality”).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-259">Anrufer</span><span class="sxs-lookup"><span data-stu-id="14aa0-259">Caller</span></span></p></td>
<td><p><span data-ttu-id="14aa0-260">bit</span><span class="sxs-lookup"><span data-stu-id="14aa0-260">bit</span></span></p></td>
<td><p><span data-ttu-id="14aa0-261">Gibt an, ob Metriken des Anrufers empfangen wurden; 1 ist ja, 0 ist Nein.</span><span class="sxs-lookup"><span data-stu-id="14aa0-261">Indicates whether metrics from the caller were received; 1 is yes, 0 is no.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-262">Callee</span><span class="sxs-lookup"><span data-stu-id="14aa0-262">Callee</span></span></p></td>
<td><p><span data-ttu-id="14aa0-263">bit</span><span class="sxs-lookup"><span data-stu-id="14aa0-263">bit</span></span></p></td>
<td><p><span data-ttu-id="14aa0-264">Gibt an, ob Metriken vom Anrufempfänger empfangen wurden; 1 ist ja, 0 ist Nein.</span><span class="sxs-lookup"><span data-stu-id="14aa0-264">Indicates whether metrics from the call receiver were received; 1 is yes, 0 is no.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-265">MidCallReport</span><span class="sxs-lookup"><span data-stu-id="14aa0-265">MidCallReport</span></span></p></td>
<td><p><span data-ttu-id="14aa0-266">bit</span><span class="sxs-lookup"><span data-stu-id="14aa0-266">bit</span></span></p></td>
<td><p><span data-ttu-id="14aa0-267">Gibt an, ob es sich bei dem Bericht um einen Teil des Anrufs oder um einen vollständigen Anruf handelt.</span><span class="sxs-lookup"><span data-stu-id="14aa0-267">Indicates whether the report is for a portion of the call or for the complete call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-268">ClassifiedPoorCall</span><span class="sxs-lookup"><span data-stu-id="14aa0-268">ClassifiedPoorCall</span></span></p></td>
<td><p><span data-ttu-id="14aa0-269">bit</span><span class="sxs-lookup"><span data-stu-id="14aa0-269">bit</span></span></p></td>
<td><p><span data-ttu-id="14aa0-270">Gibt an, ob ein Anruf als schlechter Anruf (1) oder als guter Anruf (0) klassifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="14aa0-270">Indicates whether a call was classified as a poor call (1) or as a good call (0).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14aa0-271">CallerConnectivityICE</span><span class="sxs-lookup"><span data-stu-id="14aa0-271">CallerConnectivityICE</span></span></p></td>
<td><p><span data-ttu-id="14aa0-272">tinyint</span><span class="sxs-lookup"><span data-stu-id="14aa0-272">tinyint</span></span></p></td>
<td><p><span data-ttu-id="14aa0-273">Gibt an, ob der Anrufer über das Ice-Protokoll (Internet Connectivity Establishment) mit dem Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="14aa0-273">Indicates whether the caller connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14aa0-274">CalleeConnectivityICE</span><span class="sxs-lookup"><span data-stu-id="14aa0-274">CalleeConnectivityICE</span></span></p></td>
<td><p><span data-ttu-id="14aa0-275">tinyint</span><span class="sxs-lookup"><span data-stu-id="14aa0-275">tinyint</span></span></p></td>
<td><p><span data-ttu-id="14aa0-276">Gibt an, ob der Benutzer die Verbindung mit dem Netzwerk mit dem ICE-Protokoll (Internet Connectivity Establishment) aufgerufen hat.</span><span class="sxs-lookup"><span data-stu-id="14aa0-276">Indicates whether the user called connected to the network using the ICE protocol (Internet Connectivity Establishment).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="14aa0-277">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="14aa0-277">


</div>

<span> </span>

</div>

</div>

</span></span></div>

