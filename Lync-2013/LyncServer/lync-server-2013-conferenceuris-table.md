---
title: 'Lync Server 2013: ConferenceUris-Tabelle'
description: 'Lync Server 2013: ConferenceUris-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceUris table
ms:assetid: b1721d52-3c65-45ea-8997-06af8fef93fc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412854(v=OCS.15)
ms:contentKeyID: 48185160
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a142aa9ad1fe4d3ae92aa3e21aa9eee505457cbe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434389"
---
# <a name="conferenceuris-table-in-lync-server-2013"></a><span data-ttu-id="294cb-103">ConferenceUris-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="294cb-103">ConferenceUris table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="294cb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="294cb-104">

<span> </span></span></span>

<span data-ttu-id="294cb-105">_**Letztes Änderungsdatum des Themas:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="294cb-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="294cb-106">Die Tabelle ConfereneUris ist eine unterstützende Tabelle, in der eine Liste der verschiedenen Konferenz-URIs gespeichert ist, die an Konferenzsitzungen teilgenommen haben, die in der Datenbank aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="294cb-106">The ConfereneUris table is a supporting table that stores a list of the various conference URIs that have participated in conference sessions recorded in the database.</span></span> <span data-ttu-id="294cb-107">Jeder Datensatz in der Tabelle steht für einen Konferenz-URI.</span><span class="sxs-lookup"><span data-stu-id="294cb-107">Each record in the table represents one conference URI.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="294cb-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="294cb-108">Column</span></span></th>
<th><span data-ttu-id="294cb-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="294cb-109">Data Type</span></span></th>
<th><span data-ttu-id="294cb-110">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="294cb-110">Key/Index</span></span></th>
<th><span data-ttu-id="294cb-111">Details</span><span class="sxs-lookup"><span data-stu-id="294cb-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="294cb-112"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="294cb-112"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="294cb-113">datetime</span><span class="sxs-lookup"><span data-stu-id="294cb-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="294cb-114">Primary</span><span class="sxs-lookup"><span data-stu-id="294cb-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="294cb-115">Zeitstempel, intern verwendet.</span><span class="sxs-lookup"><span data-stu-id="294cb-115">Time stamp, Internal used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="294cb-116"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="294cb-116"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="294cb-117">int</span><span class="sxs-lookup"><span data-stu-id="294cb-117">int</span></span></p></td>
<td><p><span data-ttu-id="294cb-118">Primary</span><span class="sxs-lookup"><span data-stu-id="294cb-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="294cb-119">Eindeutige Nummer, die diesen Konferenz-URI kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="294cb-119">Unique number identifying this conference URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="294cb-120"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="294cb-120"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="294cb-121">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="294cb-121">nvarchar(450)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="294cb-122">Konferenz-URI</span><span class="sxs-lookup"><span data-stu-id="294cb-122">Conference URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="294cb-123"><strong>Prüfsumme</strong></span><span class="sxs-lookup"><span data-stu-id="294cb-123"><strong>Checksum</strong></span></span></p></td>
<td><p><span data-ttu-id="294cb-124">int</span><span class="sxs-lookup"><span data-stu-id="294cb-124">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="294cb-125">Prüfsumme von ConferenceUri.</span><span class="sxs-lookup"><span data-stu-id="294cb-125">Checksum of ConferenceUri.</span></span> <span data-ttu-id="294cb-126">Wird verwendet, um die Geschwindigkeit von Datenbanksuchen zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="294cb-126">Used to increases the speed of database searches.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="294cb-127"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="294cb-127"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="294cb-128">int</span><span class="sxs-lookup"><span data-stu-id="294cb-128">int</span></span></p></td>
<td><p><span data-ttu-id="294cb-129">Fremd</span><span class="sxs-lookup"><span data-stu-id="294cb-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="294cb-130">URI-Typ wie conf: Chat für im-Konferenz oder conf: Audio-Video für Audio/Video-Konferenz.</span><span class="sxs-lookup"><span data-stu-id="294cb-130">URI type, such as conf:chat for IM conference, or conf:audio-video for audio/video conference.</span></span> <span data-ttu-id="294cb-131">Weitere Informationen finden Sie in der Tabelle <a href="lync-server-2013-uritypes-table.md">UriTypes in der lync Server 2013</a> -Tabelle.</span><span class="sxs-lookup"><span data-stu-id="294cb-131">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> table for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="294cb-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="294cb-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

