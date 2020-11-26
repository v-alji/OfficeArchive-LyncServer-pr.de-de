---
title: 'Lync Server 2013: UserSite-Tabelle'
description: 'Lync Server 2013: UserSite-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserSite table
ms:assetid: 1c2a3cf2-dc05-472e-8097-a31f3a1aafcb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398256(v=OCS.15)
ms:contentKeyID: 48183552
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e0fb3149b9378bbfd3f14da8176eed226e4f57f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436111"
---
# <a name="usersite-table-in-lync-server-2013"></a><span data-ttu-id="9537f-103">UserSite-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9537f-103">UserSite table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9537f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9537f-104">

<span> </span></span></span>

<span data-ttu-id="9537f-105">_**Letztes Änderungsdatum des Themas:** 2010-11-09_</span><span class="sxs-lookup"><span data-stu-id="9537f-105">_**Topic Last Modified:** 2010-11-09_</span></span>

<span data-ttu-id="9537f-106">Die Tabelle UserSite ist eine unterstützende Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9537f-106">The UserSite table is a supporting table.</span></span> <span data-ttu-id="9537f-107">Jeder Datensatz steht für eine Benutzer Website, die in der Netzwerk Konfigurationseinstellung definiert ist.</span><span class="sxs-lookup"><span data-stu-id="9537f-107">Each record represents one user site defined in network configuration setting.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9537f-108"><strong>Spalte</strong></span><span class="sxs-lookup"><span data-stu-id="9537f-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="9537f-109"><strong>Datentyp</strong></span><span class="sxs-lookup"><span data-stu-id="9537f-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="9537f-110"><strong>Schlüssel/Index</strong></span><span class="sxs-lookup"><span data-stu-id="9537f-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="9537f-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="9537f-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9537f-112"><strong>UserSiteKey</strong></span><span class="sxs-lookup"><span data-stu-id="9537f-112"><strong>UserSiteKey</strong></span></span></p></td>
<td><p><span data-ttu-id="9537f-113">int</span><span class="sxs-lookup"><span data-stu-id="9537f-113">int</span></span></p></td>
<td><p><span data-ttu-id="9537f-114">Primary</span><span class="sxs-lookup"><span data-stu-id="9537f-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="9537f-115">Eindeutige Nummer, die die Benutzer Website kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="9537f-115">Unique number identifying the user site.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9537f-116"><strong>UserSiteName</strong></span><span class="sxs-lookup"><span data-stu-id="9537f-116"><strong>UserSiteName</strong></span></span></p></td>
<td><p><span data-ttu-id="9537f-117">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="9537f-117">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="9537f-118">Eindeutigen</span><span class="sxs-lookup"><span data-stu-id="9537f-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="9537f-119">Name der Benutzer Website.</span><span class="sxs-lookup"><span data-stu-id="9537f-119">User site’s name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9537f-120"><strong>RegionKey</strong></span><span class="sxs-lookup"><span data-stu-id="9537f-120"><strong>RegionKey</strong></span></span></p></td>
<td><p><span data-ttu-id="9537f-121">int</span><span class="sxs-lookup"><span data-stu-id="9537f-121">int</span></span></p></td>
<td><p><span data-ttu-id="9537f-122">Fremd</span><span class="sxs-lookup"><span data-stu-id="9537f-122">Foreign</span></span></p></td>
<td><p><span data-ttu-id="9537f-123">Referenziert aus der <a href="lync-server-2013-region-table.md">Regions Tabelle in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="9537f-123">Referenced from <a href="lync-server-2013-region-table.md">Region table in Lync Server 2013</a>.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9537f-124">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9537f-124">


</div>

<span> </span>

</div>

</div>

</span></span></div>

