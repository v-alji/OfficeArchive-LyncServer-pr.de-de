---
title: 'Lync Server 2013: Endpoint-Tabelle'
description: 'Lync Server 2013: Endpunkt Tabelle'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Endpoint table
ms:assetid: 500f330d-4d7d-4e88-b1cc-fef9a9de6b5c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398327(v=OCS.15)
ms:contentKeyID: 48184098
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 614872eee41b5d8e56da4b96cf5bbe3a4a1cf4d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428678"
---
# <a name="endpoint-table-in-lync-server-2013"></a><span data-ttu-id="cb934-103">Endpoint-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cb934-103">Endpoint table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cb934-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cb934-104">

<span> </span></span></span>

<span data-ttu-id="cb934-105">_**Letztes Änderungsdatum des Themas:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="cb934-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="cb934-106">Die Endpunkt Tabelle ist eine unterstützende Tabelle, in der Informationen zu den Endpunkten gespeichert werden, die an Sitzungen teilgenommen haben, die in der Datenbank aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="cb934-106">The Endpoint table is a supporting table that stores information about the endpoints that have participated in sessions recorded in the database.</span></span> <span data-ttu-id="cb934-107">Jeder Datensatz in der Tabelle steht für einen Endpunkt.</span><span class="sxs-lookup"><span data-stu-id="cb934-107">Each record in the table represents one endpoint.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb934-108"><strong>Spalte</strong></span><span class="sxs-lookup"><span data-stu-id="cb934-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="cb934-109"><strong>Datentyp</strong></span><span class="sxs-lookup"><span data-stu-id="cb934-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="cb934-110"><strong>Schlüssel/Index</strong></span><span class="sxs-lookup"><span data-stu-id="cb934-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="cb934-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="cb934-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb934-112"><strong>EndpointKey</strong></span><span class="sxs-lookup"><span data-stu-id="cb934-112"><strong>EndpointKey</strong></span></span></p></td>
<td><p><span data-ttu-id="cb934-113">int</span><span class="sxs-lookup"><span data-stu-id="cb934-113">int</span></span></p></td>
<td><p><span data-ttu-id="cb934-114">Primary</span><span class="sxs-lookup"><span data-stu-id="cb934-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="cb934-115">Eindeutige Zahl, die diesen Endpunkt kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cb934-115">Unique number identifying this endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb934-116"><strong>Name</strong></span><span class="sxs-lookup"><span data-stu-id="cb934-116"><strong>Name</strong></span></span></p></td>
<td><p><span data-ttu-id="cb934-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="cb934-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="cb934-118">Eindeutigen</span><span class="sxs-lookup"><span data-stu-id="cb934-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="cb934-119">Endpunktname</span><span class="sxs-lookup"><span data-stu-id="cb934-119">Endpoint name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb934-120"><strong>OS</strong></span><span class="sxs-lookup"><span data-stu-id="cb934-120"><strong>OS</strong></span></span></p></td>
<td><p><span data-ttu-id="cb934-121">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="cb934-121">nvarchar(128)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="cb934-122">Betriebssystem (OS) des Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="cb934-122">Operating system (OS) of the endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb934-123"><strong>CPUName</strong></span><span class="sxs-lookup"><span data-stu-id="cb934-123"><strong>CPUName</strong></span></span></p></td>
<td><p><span data-ttu-id="cb934-124">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="cb934-124">nvarchar(128)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="cb934-125">Der CPU-Name des Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="cb934-125">CPU name of the endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb934-126"><strong>CPUNumberOfCores</strong></span><span class="sxs-lookup"><span data-stu-id="cb934-126"><strong>CPUNumberOfCores</strong></span></span></p></td>
<td><p><span data-ttu-id="cb934-127">smallint</span><span class="sxs-lookup"><span data-stu-id="cb934-127">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="cb934-128">Die Anzahl von CPU-Kernen des Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="cb934-128">Number of CPU cores of the endpoint.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb934-129"><strong>CPUProcessorSpeed</strong></span><span class="sxs-lookup"><span data-stu-id="cb934-129"><strong>CPUProcessorSpeed</strong></span></span></p></td>
<td><p><span data-ttu-id="cb934-130">int</span><span class="sxs-lookup"><span data-stu-id="cb934-130">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="cb934-131">CPU-Prozessorgeschwindigkeit des Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="cb934-131">CPU processor speed of the endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb934-132"><strong>VirtualizationFlag</strong></span><span class="sxs-lookup"><span data-stu-id="cb934-132"><strong>VirtualizationFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="cb934-133">tinyint</span><span class="sxs-lookup"><span data-stu-id="cb934-133">tinyint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="cb934-134">Bit-Flag, das angibt, ob das System in einer virtualisierten Umgebung ausgeführt wird:</span><span class="sxs-lookup"><span data-stu-id="cb934-134">Bit flag that indicates if the system is running in a virtualized environment:</span></span></p>
<ul>
<li><p><span data-ttu-id="cb934-135">0x0000 – keine</span><span class="sxs-lookup"><span data-stu-id="cb934-135">0x0000 – None</span></span></p></li>
<li><p><span data-ttu-id="cb934-136">0x0001 – HyperV</span><span class="sxs-lookup"><span data-stu-id="cb934-136">0x0001 – HyperV</span></span></p></li>
<li><p><span data-ttu-id="cb934-137">0x0002 – VMware</span><span class="sxs-lookup"><span data-stu-id="cb934-137">0x0002 – VMWare</span></span></p></li>
<li><p><span data-ttu-id="cb934-138">0x0004 – virtueller PC</span><span class="sxs-lookup"><span data-stu-id="cb934-138">0x0004 – Virtual PC</span></span></p></li>
<li><p><span data-ttu-id="cb934-139">0x0008 – xen-PC</span><span class="sxs-lookup"><span data-stu-id="cb934-139">0x0008 – Xen PC</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="cb934-140">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cb934-140">


</div>

<span> </span>

</div>

</div>

</span></span></div>

