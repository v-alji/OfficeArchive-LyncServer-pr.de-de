---
title: 'Lync Server 2013: tblPrincipalMembers'
description: 'Lync Server 2013: tblPrincipalMembers.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalMembers
ms:assetid: 9a3e24cf-6ef7-4b82-99fc-50ba41800b6f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615022(v=OCS.15)
ms:contentKeyID: 48184965
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8bbb8be0b83d09b1bd54ea98655558581e6df834
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393934"
---
# <a name="tblprincipalmembers-in-lync-server-2013"></a><span data-ttu-id="88169-103">tblPrincipalMembers in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="88169-103">tblPrincipalMembers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="88169-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="88169-104">

<span> </span></span></span>

<span data-ttu-id="88169-105">_**Letztes Änderungsdatum des Themas:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="88169-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="88169-106">tblPrincipalMembers enthält Prinzipal Mitgliedschaften.</span><span class="sxs-lookup"><span data-stu-id="88169-106">tblPrincipalMembers contains principal memberships.</span></span>

### <a name="columns"></a><span data-ttu-id="88169-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="88169-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="88169-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="88169-108">Column</span></span></th>
<th><span data-ttu-id="88169-109">Typ</span><span class="sxs-lookup"><span data-stu-id="88169-109">Type</span></span></th>
<th><span data-ttu-id="88169-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88169-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88169-111">prinID</span><span class="sxs-lookup"><span data-stu-id="88169-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="88169-112">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="88169-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="88169-113">Prinzipal-ID.</span><span class="sxs-lookup"><span data-stu-id="88169-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88169-114">memberADPath</span><span class="sxs-lookup"><span data-stu-id="88169-114">memberADPath</span></span></p></td>
<td><p><span data-ttu-id="88169-115">nvarchar (384); nicht NULL</span><span class="sxs-lookup"><span data-stu-id="88169-115">nvarchar (384), not null</span></span></p></td>
<td><p><span data-ttu-id="88169-116">Distinguished Name eines Members.</span><span class="sxs-lookup"><span data-stu-id="88169-116">Distinguished name of a member.</span></span> <span data-ttu-id="88169-117">Ein Mitglied muss kein Prinzipal sein (in der tblPrincipal-Tabelle).</span><span class="sxs-lookup"><span data-stu-id="88169-117">A member does not have to be a principal (in tblPrincipal table).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="88169-118">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="88169-118">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="88169-119">Spalte</span><span class="sxs-lookup"><span data-stu-id="88169-119">Column</span></span></th>
<th><span data-ttu-id="88169-120">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="88169-120">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="88169-121">&lt;prinID, memberADPath&gt;</span><span class="sxs-lookup"><span data-stu-id="88169-121">&lt;prinID, memberADPath&gt;</span></span></p></td>
<td><p><span data-ttu-id="88169-122">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="88169-122">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="88169-123">prinID</span><span class="sxs-lookup"><span data-stu-id="88169-123">prinID</span></span></p></td>
<td><p><span data-ttu-id="88169-124">Fremdschlüssel mit Lookup in tblPrincipal. prinID.</span><span class="sxs-lookup"><span data-stu-id="88169-124">Foreign key with lookup in tblPrincipal.prinID.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="88169-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="88169-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

