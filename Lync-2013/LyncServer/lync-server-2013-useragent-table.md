---
title: 'Lync Server 2013: UserAgent-Tabelle'
description: 'Lync Server 2013: UserAgent-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserAgent table
ms:assetid: d6bda1c0-b053-457a-9ffa-2ae859788775
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398939(v=OCS.15)
ms:contentKeyID: 48185582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b701d8384313d0267dd566e0c32242f6cc077472
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439128"
---
# <a name="useragent-table-in-lync-server-2013"></a><span data-ttu-id="2643b-103">UserAgent-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2643b-103">UserAgent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2643b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2643b-104">

<span> </span></span></span>

<span data-ttu-id="2643b-105">_**Letztes Änderungsdatum des Themas:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="2643b-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="2643b-106">Die UserAgent-Tabelle ist eine unterstützende Tabelle, in der eine Liste der verschiedenen Benutzer-Agents gespeichert ist, die an Sitzungen teilgenommen haben, die in der Datenbank aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="2643b-106">The UserAgent table is a supporting table that stores a list of the various user agents that have participated in sessions recorded in the database.</span></span> <span data-ttu-id="2643b-107">Jeder Datensatz in der Tabelle steht für einen Benutzer-Agent</span><span class="sxs-lookup"><span data-stu-id="2643b-107">Each record in the table represents one user agent</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2643b-108"><strong>Spalte</strong></span><span class="sxs-lookup"><span data-stu-id="2643b-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="2643b-109"><strong>Datentyp</strong></span><span class="sxs-lookup"><span data-stu-id="2643b-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="2643b-110"><strong>Schlüssel/Index</strong></span><span class="sxs-lookup"><span data-stu-id="2643b-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="2643b-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="2643b-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2643b-112"><strong>UserAgentKey</strong></span><span class="sxs-lookup"><span data-stu-id="2643b-112"><strong>UserAgentKey</strong></span></span></p></td>
<td><p><span data-ttu-id="2643b-113">int</span><span class="sxs-lookup"><span data-stu-id="2643b-113">int</span></span></p></td>
<td><p><span data-ttu-id="2643b-114">Primary</span><span class="sxs-lookup"><span data-stu-id="2643b-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="2643b-115">Eindeutige Nummer, die diesen Benutzer-Agent kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="2643b-115">Unique number identifying this user agent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2643b-116"><strong>UserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="2643b-116"><strong>UserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="2643b-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="2643b-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="2643b-118">Eindeutigen</span><span class="sxs-lookup"><span data-stu-id="2643b-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="2643b-119">Benutzer-Agent-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="2643b-119">User Agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2643b-120"><strong>UAType</strong></span><span class="sxs-lookup"><span data-stu-id="2643b-120"><strong>UAType</strong></span></span></p></td>
<td><p><span data-ttu-id="2643b-121">smallint</span><span class="sxs-lookup"><span data-stu-id="2643b-121">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="2643b-122">1 ist ein Vermittlungs Server.</span><span class="sxs-lookup"><span data-stu-id="2643b-122">1 is Mediation Server.</span></span></p>
<p><span data-ttu-id="2643b-123">2 ist ein/V-Konferenz Server.</span><span class="sxs-lookup"><span data-stu-id="2643b-123">2 is A/V Conferencing Server.</span></span></p>
<p><span data-ttu-id="2643b-124">4 ist lync.</span><span class="sxs-lookup"><span data-stu-id="2643b-124">4 is Lync.</span></span></p>
<p><span data-ttu-id="2643b-125">8 ist IP Phone.</span><span class="sxs-lookup"><span data-stu-id="2643b-125">8 is IP Phone.</span></span></p>
<p><span data-ttu-id="2643b-126">16 ist eine Live Meeting-Konsole.</span><span class="sxs-lookup"><span data-stu-id="2643b-126">16 is Live Meeting Console.</span></span></p>
<p><span data-ttu-id="2643b-127">32 ist ein Bereitstellungs Überprüfungs Tool (Thrombose).</span><span class="sxs-lookup"><span data-stu-id="2643b-127">32 is Deployment Validation Tool (DVT).</span></span></p>
<p><span data-ttu-id="2643b-128">64 ist lync auf Macintosh-Computern.</span><span class="sxs-lookup"><span data-stu-id="2643b-128">64 is Lync on Macintosh computers.</span></span></p>
<p><span data-ttu-id="2643b-129">128 ist Office Communications Server 2007 R2 Attendant.</span><span class="sxs-lookup"><span data-stu-id="2643b-129">128 is Office Communications Server 2007 R2 Attendant.</span></span></p>
<p><span data-ttu-id="2643b-130">256 ist ein Konferenzankündigungsdienst.</span><span class="sxs-lookup"><span data-stu-id="2643b-130">256 is Conferencing Announcement service.</span></span></p>
<p><span data-ttu-id="2643b-131">512 ist eine automatische Konferenzzentrale.</span><span class="sxs-lookup"><span data-stu-id="2643b-131">512 is Conferencing Auto Attendant.</span></span></p>
<p><span data-ttu-id="2643b-132">1024 ist eine reaktionsgruppenanwendung.</span><span class="sxs-lookup"><span data-stu-id="2643b-132">1024 is Response Group application.</span></span></p>
<p><span data-ttu-id="2643b-133">2048 ist außerhalb der Sprachsteuerung.</span><span class="sxs-lookup"><span data-stu-id="2643b-133">2048 is Outside Voice Control.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="2643b-134">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2643b-134">


</div>

<span> </span>

</div>

</div>

</span></span></div>

