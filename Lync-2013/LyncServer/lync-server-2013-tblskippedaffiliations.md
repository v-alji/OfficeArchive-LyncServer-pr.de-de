---
title: 'Lync Server 2013: tblSkippedAffiliations'
description: 'Lync Server 2013: tblSkippedAffiliations.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblSkippedAffiliations
ms:assetid: 0b129b54-a7a8-42a6-9279-0e08410c06ec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558611(v=OCS.15)
ms:contentKeyID: 48183373
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31746cee7302d34a1d19b3059ca1da6beab9345d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395063"
---
# <a name="tblskippedaffiliations-in-lync-server-2013"></a><span data-ttu-id="6cee0-103">tblSkippedAffiliations in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6cee0-103">tblSkippedAffiliations in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6cee0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6cee0-104">

<span> </span></span></span>

<span data-ttu-id="6cee0-105">_**Letztes Änderungsdatum des Themas:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="6cee0-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="6cee0-106">tblSkippedAffiliations enthält die Zuordnungen, die nicht gelesen werden konnten (in der Regel aufgrund von Zugriffsfehlern in Active Directory-Domänendiensten).</span><span class="sxs-lookup"><span data-stu-id="6cee0-106">tblSkippedAffiliations contains the affiliations that could not be read (usually due to Active Directory Domain Services access errors).</span></span>

### <a name="columns"></a><span data-ttu-id="6cee0-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="6cee0-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6cee0-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="6cee0-108">Column</span></span></th>
<th><span data-ttu-id="6cee0-109">Typ</span><span class="sxs-lookup"><span data-stu-id="6cee0-109">Type</span></span></th>
<th><span data-ttu-id="6cee0-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cee0-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cee0-111">prinID</span><span class="sxs-lookup"><span data-stu-id="6cee0-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="6cee0-112">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="6cee0-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="6cee0-113">Prinzipal-ID.</span><span class="sxs-lookup"><span data-stu-id="6cee0-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cee0-114">affDescription</span><span class="sxs-lookup"><span data-stu-id="6cee0-114">affDescription</span></span></p></td>
<td><p><span data-ttu-id="6cee0-115">nvarchar (256); nicht NULL</span><span class="sxs-lookup"><span data-stu-id="6cee0-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="6cee0-116">Eine Zeichenfolge, die die Zuordnung kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="6cee0-116">A string identifying the affiliation.</span></span></p>
<p><span data-ttu-id="6cee0-117">Das Format lautet: GUID: {0} URI: {1} &gt; ID:{2}</span><span class="sxs-lookup"><span data-stu-id="6cee0-117">The format is: guid: {0} uri: {1}&gt; id: {2}</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6cee0-118">updatedBy</span><span class="sxs-lookup"><span data-stu-id="6cee0-118">updatedBy</span></span></p></td>
<td><p><span data-ttu-id="6cee0-119">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="6cee0-119">int, not null</span></span></p></td>
<td><p><span data-ttu-id="6cee0-120">Die ID des Prinzipals, der diese Zeile aktualisiert hat.</span><span class="sxs-lookup"><span data-stu-id="6cee0-120">ID of the principal that updated this row.</span></span> <span data-ttu-id="6cee0-121">Es ist immer 1 (Systembenutzer), da die Active Directory-Synchronisierung die einzige Quelle für diese Einträge ist.</span><span class="sxs-lookup"><span data-stu-id="6cee0-121">It is always 1 (system user) because Active Directory Sync is the only source for these entries.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="6cee0-122">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="6cee0-122">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6cee0-123">Spalte (n)</span><span class="sxs-lookup"><span data-stu-id="6cee0-123">Column(s)</span></span></th>
<th><span data-ttu-id="6cee0-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6cee0-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6cee0-125">&lt;prinID, affDescription&gt;</span><span class="sxs-lookup"><span data-stu-id="6cee0-125">&lt;prinID, affDescription&gt;</span></span></p></td>
<td><p><span data-ttu-id="6cee0-126">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="6cee0-126">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6cee0-127">prinID</span><span class="sxs-lookup"><span data-stu-id="6cee0-127">prinID</span></span></p></td>
<td><p><span data-ttu-id="6cee0-128">Fremdschlüssel mit Lookup in der tblPrincipal. prinID-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="6cee0-128">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6cee0-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6cee0-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

