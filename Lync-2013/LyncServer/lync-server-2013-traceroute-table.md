---
title: 'Lync Server 2013: traceroute-Tabelle'
description: 'Lync Server 2013: traceroute-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: TraceRoute table
ms:assetid: b9493cef-6ece-4f13-bf68-dbf132aab4f4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205205(v=OCS.15)
ms:contentKeyID: 48185242
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af33e572065fbab1eaaaef684997e7f95edaed9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440836"
---
# <a name="traceroute-table-in-lync-server-2013"></a><span data-ttu-id="14d1a-103">TraceRoute-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14d1a-103">TraceRoute table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="14d1a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="14d1a-104">

<span> </span></span></span>

<span data-ttu-id="14d1a-105">_**Letztes Änderungsdatum des Themas:** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="14d1a-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="14d1a-106">Die traceroute-Tabelle enthält Routinginformationen aus anrufen.</span><span class="sxs-lookup"><span data-stu-id="14d1a-106">The TraceRoute table contains routing information from calls.</span></span> <span data-ttu-id="14d1a-107">Diese Tabelle wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="14d1a-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="14d1a-108"><strong>Spalte</strong></span><span class="sxs-lookup"><span data-stu-id="14d1a-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="14d1a-109"><strong>Datentyp</strong></span><span class="sxs-lookup"><span data-stu-id="14d1a-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="14d1a-110"><strong>Schlüssel/Index</strong></span><span class="sxs-lookup"><span data-stu-id="14d1a-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="14d1a-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="14d1a-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="14d1a-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="14d1a-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="14d1a-113">datetime</span><span class="sxs-lookup"><span data-stu-id="14d1a-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="14d1a-114">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="14d1a-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="14d1a-115">Das Datum und die Uhrzeit, zu der der Anruf begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="14d1a-115">Date and time that the call began.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14d1a-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="14d1a-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="14d1a-117">int</span><span class="sxs-lookup"><span data-stu-id="14d1a-117">int</span></span></p></td>
<td><p><span data-ttu-id="14d1a-118">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="14d1a-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="14d1a-119">Eindeutiger Bezeichner, der verwendet wird, um zwischen mehreren Anrufen zu unterscheiden, die möglicherweise am gleichen Datum und zur gleichen Zeit begonnen haben.</span><span class="sxs-lookup"><span data-stu-id="14d1a-119">Unique identifier used to distinguish between multiple calls that might have begun on the same date and at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14d1a-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="14d1a-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="14d1a-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="14d1a-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="14d1a-122">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="14d1a-122">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="14d1a-123">Stellt den Typ der im Anruf verwendeten Videozeile dar.</span><span class="sxs-lookup"><span data-stu-id="14d1a-123">Represents the type of video line used in the call.</span></span> <span data-ttu-id="14d1a-124">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="14d1a-124">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="14d1a-125">0 – Audio</span><span class="sxs-lookup"><span data-stu-id="14d1a-125">0 – Audio</span></span></p></li>
<li><p><span data-ttu-id="14d1a-126">1 – Video</span><span class="sxs-lookup"><span data-stu-id="14d1a-126">1 – Video</span></span></p></li>
<li><p><span data-ttu-id="14d1a-127">2 – Panorama Video</span><span class="sxs-lookup"><span data-stu-id="14d1a-127">2 – Panoramic video</span></span></p></li>
<li><p><span data-ttu-id="14d1a-128">3 – Anwendung/Desktop Freigabe</span><span class="sxs-lookup"><span data-stu-id="14d1a-128">3 – Application/Desktop sharing</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14d1a-129"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="14d1a-129"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="14d1a-130">bit</span><span class="sxs-lookup"><span data-stu-id="14d1a-130">bit</span></span></p></td>
<td><p><span data-ttu-id="14d1a-131">Primary</span><span class="sxs-lookup"><span data-stu-id="14d1a-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="14d1a-132">Endpunkt, der den Anruf getätigt hat.</span><span class="sxs-lookup"><span data-stu-id="14d1a-132">Endpoint that placed the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14d1a-133"><strong>Hop</strong></span><span class="sxs-lookup"><span data-stu-id="14d1a-133"><strong>Hop</strong></span></span></p></td>
<td><p><span data-ttu-id="14d1a-134">int</span><span class="sxs-lookup"><span data-stu-id="14d1a-134">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="14d1a-135">Netzwerk-Hop/</span><span class="sxs-lookup"><span data-stu-id="14d1a-135">Network hop/</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="14d1a-136"><strong>IPAddressKey</strong></span><span class="sxs-lookup"><span data-stu-id="14d1a-136"><strong>IPAddressKey</strong></span></span></p></td>
<td><p><span data-ttu-id="14d1a-137">int</span><span class="sxs-lookup"><span data-stu-id="14d1a-137">int</span></span></p></td>
<td><p><span data-ttu-id="14d1a-138">Fremd</span><span class="sxs-lookup"><span data-stu-id="14d1a-138">Foreign</span></span></p></td>
<td><p><span data-ttu-id="14d1a-139">Eindeutiger Bezeichner für die IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="14d1a-139">Unique identifier for the IP address.</span></span> <span data-ttu-id="14d1a-140">IP-Adressinformationen werden in der <a href="lync-server-2013-ipaddress-table.md">Tabelle IPAddress in lync Server 2013</a>gespeichert.</span><span class="sxs-lookup"><span data-stu-id="14d1a-140">IP address information is stored in the <a href="lync-server-2013-ipaddress-table.md">IPAddress table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="14d1a-141"><strong>RTT</strong></span><span class="sxs-lookup"><span data-stu-id="14d1a-141"><strong>RTT</strong></span></span></p></td>
<td><p><span data-ttu-id="14d1a-142">int</span><span class="sxs-lookup"><span data-stu-id="14d1a-142">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="14d1a-143">Roundtrip-Zeit.</span><span class="sxs-lookup"><span data-stu-id="14d1a-143">Roundtrip time.</span></span> <span data-ttu-id="14d1a-144">Die Roundtrip-Zeit misst die Zeitdauer, die ein Sprachpaket benötigt, um sein Ziel zu erreichen, und sendet dann eine Benachrichtigung, dass es empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="14d1a-144">The roundtrip time measures the amount of time it takes for a voice packet to reach its destination and then send back notification that it was received.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="14d1a-145">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="14d1a-145">


</div>

<span> </span>

</div>

</div>

</span></span></div>

