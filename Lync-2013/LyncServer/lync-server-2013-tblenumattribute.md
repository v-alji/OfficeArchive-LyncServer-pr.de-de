---
title: 'Lync Server 2013: tblEnumAttribute'
description: 'Lync Server 2013: tblEnumAttribute.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblEnumAttribute
ms:assetid: 17f8b87e-36a6-4f6a-8630-7c76b61a7595
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558617(v=OCS.15)
ms:contentKeyID: 48183523
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ca979a68e758ad47b691ac704f24c68c1841938a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423540"
---
# <a name="tblenumattribute-in-lync-server-2013"></a><span data-ttu-id="cdc62-103">tblEnumAttribute in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cdc62-103">tblEnumAttribute in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cdc62-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cdc62-104">

<span> </span></span></span>

<span data-ttu-id="cdc62-105">_**Letztes Änderungsdatum des Themas:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="cdc62-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="cdc62-106">tblEnumAttribute ist eine hart codierte Tabelle, die die Sichtbarkeits-und Verhaltensattribute enthält, die in der Knoten Tabelle verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="cdc62-106">tblEnumAttribute is a hardcoded table that contains the Visibility and Behavior attributes that are used in the Node table.</span></span>

### <a name="columns"></a><span data-ttu-id="cdc62-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="cdc62-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cdc62-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="cdc62-108">Column</span></span></th>
<th><span data-ttu-id="cdc62-109">Typ</span><span class="sxs-lookup"><span data-stu-id="cdc62-109">Type</span></span></th>
<th><span data-ttu-id="cdc62-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cdc62-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdc62-111">AttributeID</span><span class="sxs-lookup"><span data-stu-id="cdc62-111">attributeID</span></span></p></td>
<td><p><span data-ttu-id="cdc62-112">smallint, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="cdc62-112">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="cdc62-113">Die ID des Attributs.</span><span class="sxs-lookup"><span data-stu-id="cdc62-113">ID of the attribute.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdc62-114">AttributeName</span><span class="sxs-lookup"><span data-stu-id="cdc62-114">attributeName</span></span></p></td>
<td><p><span data-ttu-id="cdc62-115">nvarchar (256); nicht NULL</span><span class="sxs-lookup"><span data-stu-id="cdc62-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="cdc62-116">Name des Attributs.</span><span class="sxs-lookup"><span data-stu-id="cdc62-116">Name of the attribute.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="cdc62-117">Key</span><span class="sxs-lookup"><span data-stu-id="cdc62-117">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cdc62-118">Spalte</span><span class="sxs-lookup"><span data-stu-id="cdc62-118">Column</span></span></th>
<th><span data-ttu-id="cdc62-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cdc62-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdc62-120">AttributeID</span><span class="sxs-lookup"><span data-stu-id="cdc62-120">attributeID</span></span></p></td>
<td><p><span data-ttu-id="cdc62-121">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="cdc62-121">Primary key.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="table-values"></a><span data-ttu-id="cdc62-122">Tabellenwerte</span><span class="sxs-lookup"><span data-stu-id="cdc62-122">Table Values</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cdc62-123">AttributeID</span><span class="sxs-lookup"><span data-stu-id="cdc62-123">attributeID</span></span></th>
<th><span data-ttu-id="cdc62-124">AttributeName</span><span class="sxs-lookup"><span data-stu-id="cdc62-124">attributeName</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cdc62-125">1</span><span class="sxs-lookup"><span data-stu-id="cdc62-125">1</span></span></p></td>
<td><p><span data-ttu-id="cdc62-126">Sichtbarkeit.</span><span class="sxs-lookup"><span data-stu-id="cdc62-126">Visibility.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cdc62-127">2</span><span class="sxs-lookup"><span data-stu-id="cdc62-127">2</span></span></p></td>
<td><p><span data-ttu-id="cdc62-128">Verhalten.</span><span class="sxs-lookup"><span data-stu-id="cdc62-128">Behavior.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="cdc62-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cdc62-129">See Also</span></span>


[<span data-ttu-id="cdc62-130">tblNode in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cdc62-130">tblNode in Lync Server 2013</span></span>](lync-server-2013-tblnode.md)  
  

<span data-ttu-id="cdc62-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cdc62-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

