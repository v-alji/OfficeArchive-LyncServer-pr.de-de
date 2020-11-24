---
title: 'Lync Server 2013: tblScopePrincipal'
description: 'Lync Server 2013: tblScopePrincipal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblScopePrincipal
ms:assetid: 422d6c7f-7ba7-4dd4-bacc-95ace47959ff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558639(v=OCS.15)
ms:contentKeyID: 48184009
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 63315f8525e5c2f05fe54a0f9ed9e8a97b9e8bce
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393906"
---
# <a name="tblscopeprincipal-in-lync-server-2013"></a><span data-ttu-id="cd774-103">tblScopePrincipal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cd774-103">tblScopePrincipal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cd774-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cd774-104">

<span> </span></span></span>

<span data-ttu-id="cd774-105">_**Letztes Änderungsdatum des Themas:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="cd774-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="cd774-106">tblScopePrincipal enthält Bereiche, die Knoten zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="cd774-106">tblScopePrincipal contains scopes assigned to nodes.</span></span>

### <a name="columns"></a><span data-ttu-id="cd774-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="cd774-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cd774-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="cd774-108">Column</span></span></th>
<th><span data-ttu-id="cd774-109">Typ</span><span class="sxs-lookup"><span data-stu-id="cd774-109">Type</span></span></th>
<th><span data-ttu-id="cd774-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd774-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd774-111">scopeNodeID</span><span class="sxs-lookup"><span data-stu-id="cd774-111">scopeNodeID</span></span></p></td>
<td><p><span data-ttu-id="cd774-112">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="cd774-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="cd774-113">Knoten-ID, auf die sich der Bereich bezieht.</span><span class="sxs-lookup"><span data-stu-id="cd774-113">Node ID that the scope applies to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd774-114">scopePrinID</span><span class="sxs-lookup"><span data-stu-id="cd774-114">scopePrinID</span></span></p></td>
<td><p><span data-ttu-id="cd774-115">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="cd774-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="cd774-116">Prinzipal-ID.</span><span class="sxs-lookup"><span data-stu-id="cd774-116">Principal ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd774-117">scopeIsDenied</span><span class="sxs-lookup"><span data-stu-id="cd774-117">scopeIsDenied</span></span></p></td>
<td><p><span data-ttu-id="cd774-118">Bit, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="cd774-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="cd774-119">"True", wenn der Typ des Bereichs "verweigern" lautet. False, wenn allow.</span><span class="sxs-lookup"><span data-stu-id="cd774-119">True if type of scope is Deny; False if Allow.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd774-120">scopeUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="cd774-120">scopeUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="cd774-121">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="cd774-121">int, not null</span></span></p></td>
<td><p><span data-ttu-id="cd774-122">Die ID des Prinzipals, der diesen Eintrag zuletzt aktualisiert hat.</span><span class="sxs-lookup"><span data-stu-id="cd774-122">ID of the principal that last updated this entry.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="cd774-123">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="cd774-123">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cd774-124">Spalte</span><span class="sxs-lookup"><span data-stu-id="cd774-124">Column</span></span></th>
<th><span data-ttu-id="cd774-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cd774-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cd774-126">&lt;scopeNodeID, scopePrinID&gt;</span><span class="sxs-lookup"><span data-stu-id="cd774-126">&lt;scopeNodeID, scopePrinID&gt;</span></span></p></td>
<td><p><span data-ttu-id="cd774-127">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="cd774-127">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cd774-128">scopeNodeID</span><span class="sxs-lookup"><span data-stu-id="cd774-128">scopeNodeID</span></span></p></td>
<td><p><span data-ttu-id="cd774-129">Fremdschlüssel mit Lookup in der tblNode. Node-Tabelle</span><span class="sxs-lookup"><span data-stu-id="cd774-129">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cd774-130">scopePrinID</span><span class="sxs-lookup"><span data-stu-id="cd774-130">scopePrinID</span></span></p></td>
<td><p><span data-ttu-id="cd774-131">Fremdschlüssel mit Lookup in der tblPrincipal. prinID-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="cd774-131">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="cd774-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cd774-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

