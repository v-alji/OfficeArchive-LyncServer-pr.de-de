---
title: 'Lync Server 2013: tblADUpdates'
description: 'Lync Server 2013: tblADUpdates.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblADUpdates
ms:assetid: ba19fa16-4d2d-4635-ac32-f93e09469546
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615033(v=OCS.15)
ms:contentKeyID: 48185227
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7ab4418a10eac283d0f39d09b1c1fe15a32b2e68
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444483"
---
# <a name="tbladupdates-in-lync-server-2013"></a><span data-ttu-id="c68c5-103">tblADUpdates in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c68c5-103">tblADUpdates in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c68c5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c68c5-104">

<span> </span></span></span>

<span data-ttu-id="c68c5-105">_**Letztes Änderungsdatum des Themas:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="c68c5-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="c68c5-106">tblADUpdates enthält Änderungen an Active Directory-Domänendiensten, die noch nicht von den späteren Active Directory-Synchronisierungs Schritten verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="c68c5-106">tblADUpdates contains Active Directory Domain Services changes that have not yet been processed by the later Active Directory Sync steps.</span></span>

### <a name="columns"></a><span data-ttu-id="c68c5-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="c68c5-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c68c5-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="c68c5-108">Column</span></span></th>
<th><span data-ttu-id="c68c5-109">Typ</span><span class="sxs-lookup"><span data-stu-id="c68c5-109">Type</span></span></th>
<th><span data-ttu-id="c68c5-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c68c5-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c68c5-111">prinGuid</span><span class="sxs-lookup"><span data-stu-id="c68c5-111">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="c68c5-112">GUID, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="c68c5-112">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="c68c5-113">Prinzipal-GUID des geänderten Objekts.</span><span class="sxs-lookup"><span data-stu-id="c68c5-113">Principal GUID of the object that changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c68c5-114">prinADPath</span><span class="sxs-lookup"><span data-stu-id="c68c5-114">prinADPath</span></span></p></td>
<td><p><span data-ttu-id="c68c5-115">nvarchar (384); nicht NULL</span><span class="sxs-lookup"><span data-stu-id="c68c5-115">nvarchar (384), not null</span></span></p></td>
<td><p><span data-ttu-id="c68c5-116">Distinguished Name des Objekts.</span><span class="sxs-lookup"><span data-stu-id="c68c5-116">Distinguished name of the object.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c68c5-117">prinAttributesChanged</span><span class="sxs-lookup"><span data-stu-id="c68c5-117">prinAttributesChanged</span></span></p></td>
<td><p><span data-ttu-id="c68c5-118">Bit, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="c68c5-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="c68c5-119">"True", wenn mindestens ein Attribut des Objekts geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="c68c5-119">True if at least one attribute of the object changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c68c5-120">prinMembersChanged</span><span class="sxs-lookup"><span data-stu-id="c68c5-120">prinMembersChanged</span></span></p></td>
<td><p><span data-ttu-id="c68c5-121">Bit, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="c68c5-121">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="c68c5-122">"True", wenn die Mitgliedschaft geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="c68c5-122">True if the membership changed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c68c5-123">prinAffiliationsChanged</span><span class="sxs-lookup"><span data-stu-id="c68c5-123">prinAffiliationsChanged</span></span></p></td>
<td><p><span data-ttu-id="c68c5-124">Bit, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="c68c5-124">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="c68c5-125">Nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c68c5-125">Not used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c68c5-126">prinDeleted</span><span class="sxs-lookup"><span data-stu-id="c68c5-126">prinDeleted</span></span></p></td>
<td><p><span data-ttu-id="c68c5-127">Bit, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="c68c5-127">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="c68c5-128">"True", wenn das Objekt gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="c68c5-128">True if the object was deleted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c68c5-129">lastUpdated</span><span class="sxs-lookup"><span data-stu-id="c68c5-129">lastUpdated</span></span></p></td>
<td><p><span data-ttu-id="c68c5-130">DateTime, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="c68c5-130">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="c68c5-131">Zeitstempel, wann die Zeile eingefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="c68c5-131">Time stamp of when the row was inserted.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="c68c5-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c68c5-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

