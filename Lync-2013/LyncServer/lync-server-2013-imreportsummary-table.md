---
title: 'Lync Server 2013: IMReportSummary-Tabelle'
description: 'Lync Server 2013: IMReportSummary-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IMReportSummary table
ms:assetid: 27ff9453-53f2-4fae-b637-70a086c9df96
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204753(v=OCS.15)
ms:contentKeyID: 48183673
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dfafa81d1605845b29a3627321fcbc0f72ca7ac7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427313"
---
# <a name="imreportsummary-table-in-lync-server-2013"></a><span data-ttu-id="d666d-103">IMReportSummary-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d666d-103">IMReportSummary table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d666d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d666d-104">

<span> </span></span></span>

<span data-ttu-id="d666d-105">_**Letztes Änderungsdatum des Themas:** 2012-08-20_</span><span class="sxs-lookup"><span data-stu-id="d666d-105">_**Topic Last Modified:** 2012-08-20_</span></span>

<span data-ttu-id="d666d-106">Der IMReportSummaryTable stellt einen Gesamtbericht zu den Chat-Sitzungen bereit, die in einer Organisation abgehalten werden.</span><span class="sxs-lookup"><span data-stu-id="d666d-106">The IMReportSummaryTable provides an overall report on the instant messaging sessions held in an organization.</span></span> <span data-ttu-id="d666d-107">Diese Tabelle wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d666d-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d666d-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="d666d-108">Column</span></span></th>
<th><span data-ttu-id="d666d-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d666d-109">Data Type</span></span></th>
<th><span data-ttu-id="d666d-110">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="d666d-110">Key/Index</span></span></th>
<th><span data-ttu-id="d666d-111">Details</span><span class="sxs-lookup"><span data-stu-id="d666d-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d666d-112"><strong>StartTime</strong></span><span class="sxs-lookup"><span data-stu-id="d666d-112"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d666d-113">datetime</span><span class="sxs-lookup"><span data-stu-id="d666d-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="d666d-114">Primary</span><span class="sxs-lookup"><span data-stu-id="d666d-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="d666d-115">Das Datum und die Uhrzeit, zu der die Sofortnachrichtensitzung begonnen hat.</span><span class="sxs-lookup"><span data-stu-id="d666d-115">Date and time that the instant messaging session began.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d666d-116"><strong>TimePeriod</strong></span><span class="sxs-lookup"><span data-stu-id="d666d-116"><strong>TimePeriod</strong></span></span></p></td>
<td><p><span data-ttu-id="d666d-117">Zeichen (1)</span><span class="sxs-lookup"><span data-stu-id="d666d-117">char(1)</span></span></p></td>
<td><p><span data-ttu-id="d666d-118">Primary</span><span class="sxs-lookup"><span data-stu-id="d666d-118">Primary</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d666d-119"><strong>PoolFQDN</strong></span><span class="sxs-lookup"><span data-stu-id="d666d-119"><strong>PoolFQDN</strong></span></span></p></td>
<td><p><span data-ttu-id="d666d-120">nvarchar (257)</span><span class="sxs-lookup"><span data-stu-id="d666d-120">nvarchar(257)</span></span></p></td>
<td><p><span data-ttu-id="d666d-121">Primary</span><span class="sxs-lookup"><span data-stu-id="d666d-121">Primary</span></span></p></td>
<td><p><span data-ttu-id="d666d-122">Vollständig qualifizierter Domänenname des Pools, der die Sitzung hostet.</span><span class="sxs-lookup"><span data-stu-id="d666d-122">Fully qualified domain name of the pool hosting the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d666d-123"><strong>AuthType</strong></span><span class="sxs-lookup"><span data-stu-id="d666d-123"><strong>AuthType</strong></span></span></p></td>
<td><p><span data-ttu-id="d666d-124">int</span><span class="sxs-lookup"><span data-stu-id="d666d-124">int</span></span></p></td>
<td><p><span data-ttu-id="d666d-125">Primary</span><span class="sxs-lookup"><span data-stu-id="d666d-125">Primary</span></span></p></td>
<td><p><span data-ttu-id="d666d-126">Priorität (beispielsweise dringende oder nicht dringende) des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="d666d-126">Priority (for example, urgent or non-urgent) of the call.</span></span> <span data-ttu-id="d666d-127">Prioritätsinformationen werden in der <a href="lync-server-2013-callpriorities-table.md">CallPriorities-Tabelle in lync Server 2013</a>gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d666d-127">Priority information is stored in the <a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d666d-128"><strong>SessionCount gespeichert</strong></span><span class="sxs-lookup"><span data-stu-id="d666d-128"><strong>SessionCount</strong></span></span></p></td>
<td><p><span data-ttu-id="d666d-129">bigint</span><span class="sxs-lookup"><span data-stu-id="d666d-129">bigint</span></span></p></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d666d-130"><strong>MsgCount</strong></span><span class="sxs-lookup"><span data-stu-id="d666d-130"><strong>MsgCount</strong></span></span></p></td>
<td><p><span data-ttu-id="d666d-131">bigint</span><span class="sxs-lookup"><span data-stu-id="d666d-131">bigint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="d666d-132">Die Gesamtzahl der während der Sitzung ausgetauschten Sofortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="d666d-132">Total number of instant messages exchanged during the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d666d-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d666d-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

