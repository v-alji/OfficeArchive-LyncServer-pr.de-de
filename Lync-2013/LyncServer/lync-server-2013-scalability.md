---
title: 'Lync Server 2013: Skalierbarkeit'
description: Lync Server 2013-Skalierbarkeit.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scalability
ms:assetid: 46fa0cb5-1507-4a12-ad3f-ba64585e2dc4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg417160(v=OCS.15)
ms:contentKeyID: 48183995
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28cd5820755ffd1eb863ed6f2369b5756a7ae3f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442117"
---
# <a name="scalability-with-lync-server-2013"></a><span data-ttu-id="5d7ba-103">Skalierbarkeit mit Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d7ba-103">Scalability with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5d7ba-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5d7ba-104">

<span> </span></span></span>

<span data-ttu-id="5d7ba-105">_**Letztes Änderungsdatum des Themas:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="5d7ba-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="5d7ba-106">Lync Server wird in zwei Editionen, Enterprise Edition und Standard Edition angeboten.</span><span class="sxs-lookup"><span data-stu-id="5d7ba-106">Lync Server is offered in two editions, Enterprise Edition and Standard Edition.</span></span> <span data-ttu-id="5d7ba-107">Die verschiedenen Editionen sind in erster Linie für unterschiedliche Größen von Organisationen vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="5d7ba-107">The different editions are intended primarily for different sizes of organizations.</span></span> <span data-ttu-id="5d7ba-108">Wie in der folgenden Tabelle dargestellt, unterstützen beide Editionen alle Funktionen in allen Arbeitsauslastungen, mit Ausnahme von höchst Verfügbarkeit und Disaster Recovery.</span><span class="sxs-lookup"><span data-stu-id="5d7ba-108">As shown in the following table, both editions support all functionality in all workloads, except for high availability and disaster recovery.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5d7ba-109">Feature</span><span class="sxs-lookup"><span data-stu-id="5d7ba-109">Feature</span></span></th>
<th><span data-ttu-id="5d7ba-110">In Enterprise Edition unterstützt?</span><span class="sxs-lookup"><span data-stu-id="5d7ba-110">Supported in Enterprise Edition?</span></span></th>
<th><span data-ttu-id="5d7ba-111">In der Standard Edition unterstützt?</span><span class="sxs-lookup"><span data-stu-id="5d7ba-111">Supported in Standard Edition?</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5d7ba-112">Instant Messaging (im) und Anwesenheitsinformationen</span><span class="sxs-lookup"><span data-stu-id="5d7ba-112">Instant messaging (IM) and presence</span></span></p></td>
<td><p><span data-ttu-id="5d7ba-113">Ja</span><span class="sxs-lookup"><span data-stu-id="5d7ba-113">Yes</span></span></p></td>
<td><p><span data-ttu-id="5d7ba-114">Ja</span><span class="sxs-lookup"><span data-stu-id="5d7ba-114">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d7ba-115">Konferenzen</span><span class="sxs-lookup"><span data-stu-id="5d7ba-115">Conferencing</span></span></p></td>
<td><p><span data-ttu-id="5d7ba-116">Ja</span><span class="sxs-lookup"><span data-stu-id="5d7ba-116">Yes</span></span></p></td>
<td><p><span data-ttu-id="5d7ba-117">Ja</span><span class="sxs-lookup"><span data-stu-id="5d7ba-117">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d7ba-118">A/V-Konferenzen</span><span class="sxs-lookup"><span data-stu-id="5d7ba-118">A/V conferencing</span></span></p></td>
<td><p><span data-ttu-id="5d7ba-119">Ja</span><span class="sxs-lookup"><span data-stu-id="5d7ba-119">Yes</span></span></p></td>
<td><p><span data-ttu-id="5d7ba-120">Ja</span><span class="sxs-lookup"><span data-stu-id="5d7ba-120">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d7ba-121">Einwahlkonferenzen</span><span class="sxs-lookup"><span data-stu-id="5d7ba-121">Dial-in conferencing</span></span></p></td>
<td><p><span data-ttu-id="5d7ba-122">Ja</span><span class="sxs-lookup"><span data-stu-id="5d7ba-122">Yes</span></span></p></td>
<td><p><span data-ttu-id="5d7ba-123">Ja</span><span class="sxs-lookup"><span data-stu-id="5d7ba-123">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d7ba-124">Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="5d7ba-124">Enterprise Voice</span></span></p></td>
<td><p><span data-ttu-id="5d7ba-125">Ja</span><span class="sxs-lookup"><span data-stu-id="5d7ba-125">Yes</span></span></p></td>
<td><p><span data-ttu-id="5d7ba-126">Ja</span><span class="sxs-lookup"><span data-stu-id="5d7ba-126">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5d7ba-127">Virtualisierung</span><span class="sxs-lookup"><span data-stu-id="5d7ba-127">Virtualization</span></span></p></td>
<td><p><span data-ttu-id="5d7ba-128">Ja</span><span class="sxs-lookup"><span data-stu-id="5d7ba-128">Yes</span></span></p></td>
<td><p><span data-ttu-id="5d7ba-129">Ja</span><span class="sxs-lookup"><span data-stu-id="5d7ba-129">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5d7ba-130">Hochgradige Verfügbarkeit, Failover und Disaster Recovery</span><span class="sxs-lookup"><span data-stu-id="5d7ba-130">High availability, failover, and disaster recovery</span></span></p></td>
<td><p><span data-ttu-id="5d7ba-131">Ja</span><span class="sxs-lookup"><span data-stu-id="5d7ba-131">Yes</span></span></p></td>
<td><p><span data-ttu-id="5d7ba-132">Nein</span><span class="sxs-lookup"><span data-stu-id="5d7ba-132">No</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5d7ba-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5d7ba-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

