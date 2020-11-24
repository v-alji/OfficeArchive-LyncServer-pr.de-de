---
title: 'Lync Server 2013: tblPrincipalRole'
description: 'Lync Server 2013: tblPrincipalRole.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalRole
ms:assetid: dcd16dc1-a66c-4720-a48f-ec8b28337383
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615039(v=OCS.15)
ms:contentKeyID: 48185597
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f58ffda3136c254ee77f14d33dcb42af5d172c4a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393918"
---
# <a name="tblprincipalrole-in-lync-server-2013"></a><span data-ttu-id="677fb-103">tblPrincipalRole in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="677fb-103">tblPrincipalRole in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="677fb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="677fb-104">

<span> </span></span></span>

<span data-ttu-id="677fb-105">_**Letztes Änderungsdatum des Themas:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="677fb-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="677fb-106">tblPrincipalRole enthält explizite Rollen, die Knoten zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="677fb-106">tblPrincipalRole contains explicit roles assigned to nodes.</span></span>

### <a name="columns"></a><span data-ttu-id="677fb-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="677fb-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="677fb-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="677fb-108">Column</span></span></th>
<th><span data-ttu-id="677fb-109">Typ</span><span class="sxs-lookup"><span data-stu-id="677fb-109">Type</span></span></th>
<th><span data-ttu-id="677fb-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="677fb-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="677fb-111">prinRoleNodeID</span><span class="sxs-lookup"><span data-stu-id="677fb-111">prinRoleNodeID</span></span></p></td>
<td><p><span data-ttu-id="677fb-112">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="677fb-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="677fb-113">Die Knoten-ID, auf die sich die Rolle bezieht.</span><span class="sxs-lookup"><span data-stu-id="677fb-113">Node ID that the role applies to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="677fb-114">prinRolePrinID</span><span class="sxs-lookup"><span data-stu-id="677fb-114">prinRolePrinID</span></span></p></td>
<td><p><span data-ttu-id="677fb-115">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="677fb-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="677fb-116">Prinzipal-ID.</span><span class="sxs-lookup"><span data-stu-id="677fb-116">Principal ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="677fb-117">prinRoleTypeID</span><span class="sxs-lookup"><span data-stu-id="677fb-117">prinRoleTypeID</span></span></p></td>
<td><p><span data-ttu-id="677fb-118">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="677fb-118">int, not null</span></span></p></td>
<td><p><span data-ttu-id="677fb-119">Rollentyp-ID (aus tblRoleType).</span><span class="sxs-lookup"><span data-stu-id="677fb-119">Role type ID (from tblRoleType).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="677fb-120">prinRoleUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="677fb-120">prinRoleUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="677fb-121">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="677fb-121">int, not null</span></span></p></td>
<td><p><span data-ttu-id="677fb-122">Die ID des Prinzipals, der diesen Eintrag zuletzt aktualisiert hat.</span><span class="sxs-lookup"><span data-stu-id="677fb-122">ID of the principal that last updated this entry.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="677fb-123">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="677fb-123">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="677fb-124">Spalte</span><span class="sxs-lookup"><span data-stu-id="677fb-124">Column</span></span></th>
<th><span data-ttu-id="677fb-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="677fb-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="677fb-126">&lt;prinRoleNodeID, prinRolePrinID, prinRoleTypeID&gt;</span><span class="sxs-lookup"><span data-stu-id="677fb-126">&lt;prinRoleNodeID, prinRolePrinID, prinRoleTypeID&gt;</span></span></p></td>
<td><p><span data-ttu-id="677fb-127">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="677fb-127">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="677fb-128">prinRoleNodeID</span><span class="sxs-lookup"><span data-stu-id="677fb-128">prinRoleNodeID</span></span></p></td>
<td><p><span data-ttu-id="677fb-129">Fremdschlüssel mit Lookup in der tblNode. Node-Tabelle</span><span class="sxs-lookup"><span data-stu-id="677fb-129">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="677fb-130">prinRolePrinID</span><span class="sxs-lookup"><span data-stu-id="677fb-130">prinRolePrinID</span></span></p></td>
<td><p><span data-ttu-id="677fb-131">Fremdschlüssel mit Lookup in der tblPrincipal. prinID-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="677fb-131">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="677fb-132">prinRoleTypeID</span><span class="sxs-lookup"><span data-stu-id="677fb-132">prinRoleTypeID</span></span></p></td>
<td><p><span data-ttu-id="677fb-133">Fremdschlüssel mit Lookup in der tblRoleType. rtypeID-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="677fb-133">Foreign key with lookup in tblRoleType.rtypeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="677fb-134">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="677fb-134">


</div>

<span> </span>

</div>

</div>

</span></span></div>

