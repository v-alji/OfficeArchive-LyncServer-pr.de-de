---
title: 'Lync Server 2013: IPAddress-Tabelle'
description: 'Lync Server 2013: IPAddress-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IPAddress table
ms:assetid: 8ec018b9-158e-4bbe-ad46-869e60315555
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205077(v=OCS.15)
ms:contentKeyID: 48184771
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6d987281fc310a3a179fa99f2aae51b0764349dd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394694"
---
# <a name="ipaddress-table-in-lync-server-2013"></a><span data-ttu-id="959af-103">IPAddress-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="959af-103">IPAddress table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="959af-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="959af-104">

<span> </span></span></span>

<span data-ttu-id="959af-105">_**Letztes Änderungsdatum des Themas:** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="959af-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="959af-106">Die IPAddress-Tabelle ordnet IP-Adressen den eindeutigen IP-Adress Bezeichnern zu, die an anderer Stelle in der Datenbank für die Qualität der Erfahrung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="959af-106">The IPAddress table maps IP addresses to the unique IP address identifiers used elsewhere in the Quality of Experience database.</span></span> <span data-ttu-id="959af-107">Diese Tabelle wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="959af-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="959af-108"><strong>Spalte</strong></span><span class="sxs-lookup"><span data-stu-id="959af-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="959af-109"><strong>Datentyp</strong></span><span class="sxs-lookup"><span data-stu-id="959af-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="959af-110"><strong>Schlüssel/Index</strong></span><span class="sxs-lookup"><span data-stu-id="959af-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="959af-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="959af-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="959af-112"><strong>IPAddressKey</strong></span><span class="sxs-lookup"><span data-stu-id="959af-112"><strong>IPAddressKey</strong></span></span></p></td>
<td><p><span data-ttu-id="959af-113">int</span><span class="sxs-lookup"><span data-stu-id="959af-113">int</span></span></p></td>
<td><p><span data-ttu-id="959af-114">Primary</span><span class="sxs-lookup"><span data-stu-id="959af-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="959af-115">Eindeutiger Bezeichner für die angegebene IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="959af-115">Unique identifier for the specified IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="959af-116"><strong>IPAddress</strong></span><span class="sxs-lookup"><span data-stu-id="959af-116"><strong>IPAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="959af-117">varchar(50)</span><span class="sxs-lookup"><span data-stu-id="959af-117">varchar(50)</span></span></p></td>
<td><p><span data-ttu-id="959af-118">Eindeutigen</span><span class="sxs-lookup"><span data-stu-id="959af-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="959af-119">Eindeutige IP-Adresse (beispielsweise 189.168.1.1), die dem IpAddressKey zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="959af-119">Unique IP address (for example, 189.168.1.1) that maps to the IpAddressKey.</span></span> <span data-ttu-id="959af-120">Hierbei kann es sich entweder um eine IPv4-oder eine IPv6-Adresse handeln.</span><span class="sxs-lookup"><span data-stu-id="959af-120">This may be either an IPv4 or an IPv6 address.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="959af-121">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="959af-121">


</div>

<span> </span>

</div>

</div>

</span></span></div>

