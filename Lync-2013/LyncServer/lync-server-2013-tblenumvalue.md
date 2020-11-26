---
title: 'Lync Server 2013: tblEnumValue'
description: 'Lync Server 2013: tblEnumValue.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblEnumValue
ms:assetid: a33df20c-d19d-4f5c-b012-29dab8fb9200
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615025(v=OCS.15)
ms:contentKeyID: 48185040
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 159f90bb96c367fcb3e11725a582a9993080d3fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444448"
---
# <a name="tblenumvalue-in-lync-server-2013"></a><span data-ttu-id="2b32d-103">tblEnumValue in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b32d-103">tblEnumValue in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2b32d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2b32d-104">

<span> </span></span></span>

<span data-ttu-id="2b32d-105">_**Letztes Änderungsdatum des Themas:** 2012-06-28_</span><span class="sxs-lookup"><span data-stu-id="2b32d-105">_**Topic Last Modified:** 2012-06-28_</span></span>

<span data-ttu-id="2b32d-106">tblEnumValue ist eine hart codierte Tabelle, die die Sichtbarkeits-und Verhaltens Werte der Attribute enthält, die in der Knoten Tabelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="2b32d-106">tblEnumValue is a hardcoded table that contains the Visibility and Behavior values of the attributes that are used in the Node table.</span></span>

### <a name="columns"></a><span data-ttu-id="2b32d-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="2b32d-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2b32d-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="2b32d-108">Column</span></span></th>
<th><span data-ttu-id="2b32d-109">Typ</span><span class="sxs-lookup"><span data-stu-id="2b32d-109">Type</span></span></th>
<th><span data-ttu-id="2b32d-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b32d-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b32d-111">Werttyp</span><span class="sxs-lookup"><span data-stu-id="2b32d-111">valueID</span></span></p></td>
<td><p><span data-ttu-id="2b32d-112">smallint, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="2b32d-112">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="2b32d-113">Die ID des Werts.</span><span class="sxs-lookup"><span data-stu-id="2b32d-113">ID of the value.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b32d-114">AttributeID</span><span class="sxs-lookup"><span data-stu-id="2b32d-114">attributeID</span></span></p></td>
<td><p><span data-ttu-id="2b32d-115">smallint, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="2b32d-115">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="2b32d-116">Die ID des Attributs.</span><span class="sxs-lookup"><span data-stu-id="2b32d-116">ID of the attribute.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b32d-117">AttributeValue</span><span class="sxs-lookup"><span data-stu-id="2b32d-117">attributeValue</span></span></p></td>
<td><p><span data-ttu-id="2b32d-118">nvarchar (256); nicht NULL</span><span class="sxs-lookup"><span data-stu-id="2b32d-118">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="2b32d-119">Der Name des Werts.</span><span class="sxs-lookup"><span data-stu-id="2b32d-119">Name of the value.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="2b32d-120">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="2b32d-120">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2b32d-121">Spalte</span><span class="sxs-lookup"><span data-stu-id="2b32d-121">Column</span></span></th>
<th><span data-ttu-id="2b32d-122">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2b32d-122">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b32d-123">Werttyp</span><span class="sxs-lookup"><span data-stu-id="2b32d-123">valueID</span></span></p></td>
<td><p><span data-ttu-id="2b32d-124">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="2b32d-124">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b32d-125">AttributeID</span><span class="sxs-lookup"><span data-stu-id="2b32d-125">attributeID</span></span></p></td>
<td><p><span data-ttu-id="2b32d-126">Fremdschlüssel mit Lookup in der tblEnumAttribute. AttributeCollection-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="2b32d-126">Foreign key with lookup in tblEnumAttribute.attributeID table.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="table-values"></a><span data-ttu-id="2b32d-127">Tabellenwerte</span><span class="sxs-lookup"><span data-stu-id="2b32d-127">Table Values</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2b32d-128">Werttyp</span><span class="sxs-lookup"><span data-stu-id="2b32d-128">valueID</span></span></th>
<th><span data-ttu-id="2b32d-129">AttributeID</span><span class="sxs-lookup"><span data-stu-id="2b32d-129">attributeID</span></span></th>
<th><span data-ttu-id="2b32d-130">AttributeValue</span><span class="sxs-lookup"><span data-stu-id="2b32d-130">attributeValue</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2b32d-131">2</span><span class="sxs-lookup"><span data-stu-id="2b32d-131">2</span></span></p></td>
<td><p><span data-ttu-id="2b32d-132">1</span><span class="sxs-lookup"><span data-stu-id="2b32d-132">1</span></span></p></td>
<td><p><span data-ttu-id="2b32d-133">privat</span><span class="sxs-lookup"><span data-stu-id="2b32d-133">private</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b32d-134">3</span><span class="sxs-lookup"><span data-stu-id="2b32d-134">3</span></span></p></td>
<td><p><span data-ttu-id="2b32d-135">1</span><span class="sxs-lookup"><span data-stu-id="2b32d-135">1</span></span></p></td>
<td><p><span data-ttu-id="2b32d-136">Bereich</span><span class="sxs-lookup"><span data-stu-id="2b32d-136">scope</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b32d-137">4</span><span class="sxs-lookup"><span data-stu-id="2b32d-137">4</span></span></p></td>
<td><p><span data-ttu-id="2b32d-138">2</span><span class="sxs-lookup"><span data-stu-id="2b32d-138">2</span></span></p></td>
<td><p><span data-ttu-id="2b32d-139">normal</span><span class="sxs-lookup"><span data-stu-id="2b32d-139">normal</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2b32d-140">5</span><span class="sxs-lookup"><span data-stu-id="2b32d-140">5</span></span></p></td>
<td><p><span data-ttu-id="2b32d-141">2</span><span class="sxs-lookup"><span data-stu-id="2b32d-141">2</span></span></p></td>
<td><p><span data-ttu-id="2b32d-142">Auditorium</span><span class="sxs-lookup"><span data-stu-id="2b32d-142">auditorium</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2b32d-143">6</span><span class="sxs-lookup"><span data-stu-id="2b32d-143">6</span></span></p></td>
<td><p><span data-ttu-id="2b32d-144">1</span><span class="sxs-lookup"><span data-stu-id="2b32d-144">1</span></span></p></td>
<td><p><span data-ttu-id="2b32d-145">Öffnen</span><span class="sxs-lookup"><span data-stu-id="2b32d-145">open</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="2b32d-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b32d-146">See Also</span></span>


[<span data-ttu-id="2b32d-147">tblNode in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b32d-147">tblNode in Lync Server 2013</span></span>](lync-server-2013-tblnode.md)  
  

<span data-ttu-id="2b32d-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2b32d-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

