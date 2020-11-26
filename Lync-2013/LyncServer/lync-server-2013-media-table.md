---
title: 'Lync Server 2013: Media-Tabelle'
description: 'Lync Server 2013: Medientabelle'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media table
ms:assetid: 1e1b427f-59b5-4564-bde5-1002a80439ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398268(v=OCS.15)
ms:contentKeyID: 48183568
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31e30d1f91c59b8e3aa7915fc0d513618d0f709f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425675"
---
# <a name="media-table-in-lync-server-2013"></a><span data-ttu-id="cb056-103">Media-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cb056-103">Media table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cb056-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cb056-104">

<span> </span></span></span>

<span data-ttu-id="cb056-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="cb056-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="cb056-106">Jeder Datensatz steht für einen in einer Peer-to-Peer-Sitzung verwendeten Medientyp.</span><span class="sxs-lookup"><span data-stu-id="cb056-106">Each record represents one media type used in a peer-to-peer session.</span></span> <span data-ttu-id="cb056-107">Eine Sitzung wird von mehreren Datensätzen in der Tabelle dargestellt, wenn mehr als ein Medientyp verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="cb056-107">One session would be represented by multiple records in the table, if more than one media type is used.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="cb056-108">Die Medientabelle sollte nicht verwendet werden, um die Mediendauer einer Sitzung zu berechnen.</span><span class="sxs-lookup"><span data-stu-id="cb056-108">The Media table should not be used to calculate the media duration for a session.</span></span> <span data-ttu-id="cb056-109">Diese Tabelle enthält die Signalisierungs Details von Medienaustausch in einer Sitzung.</span><span class="sxs-lookup"><span data-stu-id="cb056-109">This table contains the signaling details of media exchange in a session.</span></span> <span data-ttu-id="cb056-110">Der Medienaustausch erfolgt über die Einladungs Anfrage, und Startzeit gibt an, wie lange die Einladung gesendet wurde. Die Einladungs Zeit bedeutet nicht unbedingt die Startzeit des Mediums, da Medien erst gestartet werden, nachdem der Sitzungs nehmer die Sitzung akzeptiert hat.</span><span class="sxs-lookup"><span data-stu-id="cb056-110">Media exchange is done by the INVITE request, and StartTime indicates the time that the INVITE was sent out. The invite time does not necessarily mean the media start time, because media starts only after the sessionee accepts the session.</span></span> <span data-ttu-id="cb056-111">Die EndTime bedeutet normalerweise die Endzeit dieser Sitzung.</span><span class="sxs-lookup"><span data-stu-id="cb056-111">The EndTime usually means the end time of this session.</span></span>



</div>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cb056-112">Spalte</span><span class="sxs-lookup"><span data-stu-id="cb056-112">Column</span></span></th>
<th><span data-ttu-id="cb056-113">Datentyp</span><span class="sxs-lookup"><span data-stu-id="cb056-113">Data Type</span></span></th>
<th><span data-ttu-id="cb056-114">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="cb056-114">Key/Index</span></span></th>
<th><span data-ttu-id="cb056-115">Details</span><span class="sxs-lookup"><span data-stu-id="cb056-115">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cb056-116"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="cb056-116"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="cb056-117">datetime</span><span class="sxs-lookup"><span data-stu-id="cb056-117">datetime</span></span></p></td>
<td><p><span data-ttu-id="cb056-118">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="cb056-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="cb056-119">Uhrzeit der Sitzungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="cb056-119">Time of session request.</span></span> <span data-ttu-id="cb056-120">Wird in Verbindung mit <strong>SessionIdSeq</strong> verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cb056-120">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="cb056-121">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cb056-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb056-122"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="cb056-122"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="cb056-123">int</span><span class="sxs-lookup"><span data-stu-id="cb056-123">int</span></span></p></td>
<td><p><span data-ttu-id="cb056-124">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="cb056-124">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="cb056-125">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cb056-125">ID number to identify the session.</span></span> <span data-ttu-id="cb056-126">Wird in Verbindung mit <strong>SessionID</strong> -Mal verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="cb056-126">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="cb056-127">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cb056-127">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb056-128"><strong>MediaId</strong></span><span class="sxs-lookup"><span data-stu-id="cb056-128"><strong>MediaId</strong></span></span></p></td>
<td><p><span data-ttu-id="cb056-129">tinyint</span><span class="sxs-lookup"><span data-stu-id="cb056-129">tinyint</span></span></p></td>
<td><p><span data-ttu-id="cb056-130">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="cb056-130">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="cb056-131">Eindeutige Nummer, die diesen Medientyp kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="cb056-131">Unique number identifying this media type.</span></span> <span data-ttu-id="cb056-132">Weitere Informationen finden Sie <a href="lync-server-2013-medialist-table.md">in der Tabelle medialist in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="cb056-132">See the <a href="lync-server-2013-medialist-table.md">MediaList table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cb056-133"><strong>StartTime</strong></span><span class="sxs-lookup"><span data-stu-id="cb056-133"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="cb056-134">datetime</span><span class="sxs-lookup"><span data-stu-id="cb056-134">datetime</span></span></p></td>
<td><p><span data-ttu-id="cb056-135">Primary</span><span class="sxs-lookup"><span data-stu-id="cb056-135">Primary</span></span></p></td>
<td><p><span data-ttu-id="cb056-136">Dies ist der Zeitpunkt, zu dem eine Medienanfrage gesendet wurde, nicht die Startzeit des realen Mediums.</span><span class="sxs-lookup"><span data-stu-id="cb056-136">This is the time that a media request was sent out, not the real media start time.</span></span> <span data-ttu-id="cb056-137"><strong>Startzeit</strong> umfasst die Rüstzeit für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="cb056-137"><strong>StartTime</strong> includes the session setup time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cb056-138"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="cb056-138"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="cb056-139">datetime</span><span class="sxs-lookup"><span data-stu-id="cb056-139">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="cb056-140">Dies ist die Endzeit der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="cb056-140">This is the end time of the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="cb056-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cb056-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

