---
title: 'Lync Server 2013: Devices-Tabelle'
description: 'Lync Server 2013: Devices-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Devices table
ms:assetid: 532e2280-4bbc-4a6c-93da-45d9f80a30a0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398351(v=OCS.15)
ms:contentKeyID: 48184169
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 763e1788e2874f9f9831c089ffe8fa077621b030
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429339"
---
# <a name="devices-table-in-lync-server-2013"></a><span data-ttu-id="c4045-103">Devices-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c4045-103">Devices table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c4045-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c4045-104">

<span> </span></span></span>

<span data-ttu-id="c4045-105">_**Letztes Änderungsdatum des Themas:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="c4045-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="c4045-106">Die Tabelle Devices ist eine unterstützende Tabelle.</span><span class="sxs-lookup"><span data-stu-id="c4045-106">The Devices table is a supporting table.</span></span> <span data-ttu-id="c4045-107">Jeder Datensatz speichert Informationen zu einem Gerät (Tischtelefon).</span><span class="sxs-lookup"><span data-stu-id="c4045-107">Each record stores information about one device (desk phone).</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c4045-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="c4045-108">Column</span></span></th>
<th><span data-ttu-id="c4045-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="c4045-109">Data Type</span></span></th>
<th><span data-ttu-id="c4045-110">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="c4045-110">Key/Index</span></span></th>
<th><span data-ttu-id="c4045-111">Details</span><span class="sxs-lookup"><span data-stu-id="c4045-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c4045-112"><strong>DeviceID</strong></span><span class="sxs-lookup"><span data-stu-id="c4045-112"><strong>DeviceId</strong></span></span></p></td>
<td><p><span data-ttu-id="c4045-113">int</span><span class="sxs-lookup"><span data-stu-id="c4045-113">int</span></span></p></td>
<td><p><span data-ttu-id="c4045-114">Primary</span><span class="sxs-lookup"><span data-stu-id="c4045-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="c4045-115">Eindeutige Nummer, die diese Hardware Version kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="c4045-115">Unique number identifying this hardware version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4045-116"><strong>ManufacturerId</strong></span><span class="sxs-lookup"><span data-stu-id="c4045-116"><strong>ManufacturerId</strong></span></span></p></td>
<td><p><span data-ttu-id="c4045-117">int</span><span class="sxs-lookup"><span data-stu-id="c4045-117">int</span></span></p></td>
<td><p><span data-ttu-id="c4045-118">Fremd</span><span class="sxs-lookup"><span data-stu-id="c4045-118">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c4045-119">Hersteller des Geräts.</span><span class="sxs-lookup"><span data-stu-id="c4045-119">Manufacturer of this device.</span></span> <span data-ttu-id="c4045-120">Weitere Informationen finden Sie <a href="lync-server-2013-manufacturers-table.md">in der Tabelle "Hersteller" in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="c4045-120">See the <a href="lync-server-2013-manufacturers-table.md">Manufacturers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c4045-121"><strong>HardwareVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="c4045-121"><strong>HardwareVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="c4045-122">int</span><span class="sxs-lookup"><span data-stu-id="c4045-122">int</span></span></p></td>
<td><p><span data-ttu-id="c4045-123">Fremd</span><span class="sxs-lookup"><span data-stu-id="c4045-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="c4045-124">Hardware Version dieses Geräts.</span><span class="sxs-lookup"><span data-stu-id="c4045-124">Hardware version of this device.</span></span> <span data-ttu-id="c4045-125">Weitere Informationen finden Sie <a href="lync-server-2013-hardwareversions-table.md">in der HardwareVersions-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="c4045-125">See the <a href="lync-server-2013-hardwareversions-table.md">HardwareVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c4045-126"><strong>MacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="c4045-126"><strong>MacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="c4045-127">bigint</span><span class="sxs-lookup"><span data-stu-id="c4045-127">bigint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="c4045-128">Mac-Adresse</span><span class="sxs-lookup"><span data-stu-id="c4045-128">MAC Address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c4045-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c4045-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

