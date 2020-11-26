---
title: 'Lync Server 2013: MediaList-Tabelle'
description: 'Lync Server 2013: medialist-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: MediaList table
ms:assetid: 1f440590-c1bc-483e-b7bc-6cc763847768
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398279(v=OCS.15)
ms:contentKeyID: 48183579
ms.date: 07/12/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e54535cd4a081657e7dcd59446cf65aaa3af7cd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445925"
---
# <a name="medialist-table-in-lync-server-2013"></a><span data-ttu-id="1d602-103">MediaList-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1d602-103">MediaList table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1d602-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1d602-104">

<span> </span></span></span>

<span data-ttu-id="1d602-105">_**Letztes Änderungsdatum des Themas:** 2016-07-12_</span><span class="sxs-lookup"><span data-stu-id="1d602-105">_**Topic Last Modified:** 2016-07-12_</span></span>

<span data-ttu-id="1d602-106">Die MediaList-Tabelle ist eine statische Tabelle, in der die Liste der verschiedenen Medientypen gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="1d602-106">The MediaList table is a static table that stores the list of various media types.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1d602-107">Spalte</span><span class="sxs-lookup"><span data-stu-id="1d602-107">Column</span></span></th>
<th><span data-ttu-id="1d602-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="1d602-108">Data Type</span></span></th>
<th><span data-ttu-id="1d602-109">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="1d602-109">Key/Index</span></span></th>
<th><span data-ttu-id="1d602-110">Details</span><span class="sxs-lookup"><span data-stu-id="1d602-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1d602-111"><strong>MediaId</strong></span><span class="sxs-lookup"><span data-stu-id="1d602-111"><strong>MediaId</strong></span></span></p></td>
<td><p><span data-ttu-id="1d602-112">tinyint</span><span class="sxs-lookup"><span data-stu-id="1d602-112">tinyint</span></span></p></td>
<td><p><span data-ttu-id="1d602-113">Primary</span><span class="sxs-lookup"><span data-stu-id="1d602-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="1d602-114">Werte: 1-7</span><span class="sxs-lookup"><span data-stu-id="1d602-114">Values: 1-7</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1d602-115"><strong>Media</strong></span><span class="sxs-lookup"><span data-stu-id="1d602-115"><strong>Media</strong></span></span></p></td>
<td><p><span data-ttu-id="1d602-116">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="1d602-116">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="1d602-117">Statische Zuordnung von MediaID- und Media-Werten</span><span class="sxs-lookup"><span data-stu-id="1d602-117">Static mapping of MediaID and Media values:</span></span></p>
<ul>
<li><p><span data-ttu-id="1d602-118">1 – im</span><span class="sxs-lookup"><span data-stu-id="1d602-118">1 – IM</span></span></p></li>
<li><p><span data-ttu-id="1d602-119">2 - Dateiübertragung</span><span class="sxs-lookup"><span data-stu-id="1d602-119">2 – File Transfer</span></span></p></li>
<li><p><span data-ttu-id="1d602-120">3 – Remoteunterstützung</span><span class="sxs-lookup"><span data-stu-id="1d602-120">3 – Remote Assistance</span></span></p></li>
<li><p><span data-ttu-id="1d602-121">4 – Anwendungsfreigabe</span><span class="sxs-lookup"><span data-stu-id="1d602-121">4 – Application Sharing</span></span></p></li>
<li><p><span data-ttu-id="1d602-122">5 – Audio</span><span class="sxs-lookup"><span data-stu-id="1d602-122">5 – Audio</span></span></p></li>
<li><p><span data-ttu-id="1d602-123">6 – Video</span><span class="sxs-lookup"><span data-stu-id="1d602-123">6 – Video</span></span></p></li>
<li><p><span data-ttu-id="1d602-124">7 – Anwendungseinladung</span><span class="sxs-lookup"><span data-stu-id="1d602-124">7 – App Invite</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="1d602-125">Wenn Sie versuchen, den Modalitätstyp für die Werte in LcsCDR.SessionDetailsView.MediaTypes zu bestimmen, müssen Sie das folgende Join-Snippet verwenden: </span><span class="sxs-lookup"><span data-stu-id="1d602-125">If you are trying to determine the modality type for the values in LcsCDR.SessionDetailsView.MediaTypes, then you need to use the following Join snippet:</span></span>

    LEFT JOIN on Media.MediaId = MediaList.MediaId

<span data-ttu-id="1d602-126"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1d602-126"></div>

<span> </span>

</div>

</div>

</span></span></div>

