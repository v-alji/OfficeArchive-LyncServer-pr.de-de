---
title: 'Lync Server 2013: tblPrincipalAffiliations'
description: 'Lync Server 2013: tblPrincipalAffiliations.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalAffiliations
ms:assetid: 45fd8484-5837-44d2-85bb-45c83546607c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558642(v=OCS.15)
ms:contentKeyID: 48183993
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 01c373147a58300e64f22e60e989a777c59b2653
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441368"
---
# <a name="tblprincipalaffiliations-in-lync-server-2013"></a><span data-ttu-id="040b4-103">tblPrincipalAffiliations in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="040b4-103">tblPrincipalAffiliations in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="040b4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="040b4-104">

<span> </span></span></span>

<span data-ttu-id="040b4-105">_**Letztes Änderungsdatum des Themas:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="040b4-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="040b4-106">tblPrincipalAffiliations enthält die Haupt Zuordnungen, die Mitgliedschaften an Speicherorten beschreiben, einschließlich Sicherheitsgruppen für Active Directory-Domänendienste, in Active Directory-Containern in Domänen.</span><span class="sxs-lookup"><span data-stu-id="040b4-106">tblPrincipalAffiliations contains the principal affiliations that describe memberships in locations, including Active Directory Domain Services security groups, in Active Directory containers, in domains.</span></span>

### <a name="columns"></a><span data-ttu-id="040b4-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="040b4-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="040b4-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="040b4-108">Column</span></span></th>
<th><span data-ttu-id="040b4-109">Typ</span><span class="sxs-lookup"><span data-stu-id="040b4-109">Type</span></span></th>
<th><span data-ttu-id="040b4-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="040b4-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="040b4-111">Prinzipal-Nr</span><span class="sxs-lookup"><span data-stu-id="040b4-111">principalID</span></span></p></td>
<td><p><span data-ttu-id="040b4-112">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="040b4-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="040b4-113">Die ID des verbundenen Prinzipals.</span><span class="sxs-lookup"><span data-stu-id="040b4-113">ID of the affiliated principal.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="040b4-114">affiliationID</span><span class="sxs-lookup"><span data-stu-id="040b4-114">affiliationID</span></span></p></td>
<td><p><span data-ttu-id="040b4-115">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="040b4-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="040b4-116">Die ID des Prinzipals, der die Zuordnung darstellt.</span><span class="sxs-lookup"><span data-stu-id="040b4-116">ID of the principal representing the affiliation.</span></span> <span data-ttu-id="040b4-117">Jeder Prinzipal (mit Ausnahme von System-User-Typen) hat ebenfalls eine Selbstzuordnung.</span><span class="sxs-lookup"><span data-stu-id="040b4-117">Each principal (except system-user-types) has a self-affiliation as well.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="040b4-118">Index</span><span class="sxs-lookup"><span data-stu-id="040b4-118">index</span></span></p></td>
<td><p><span data-ttu-id="040b4-119">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="040b4-119">int, not null</span></span></p></td>
<td><p><span data-ttu-id="040b4-120">Index.</span><span class="sxs-lookup"><span data-stu-id="040b4-120">Index.</span></span> <span data-ttu-id="040b4-121">Der Wert für Self-Affiliations ist-1, und für die anderen Zuordnungen wird er sequenziell von 1 innerhalb der einzelnen &lt; Prinzipal-affiliationId- &gt; Buckets erhöht.</span><span class="sxs-lookup"><span data-stu-id="040b4-121">The value for self-affiliations is -1, and for the other affiliations it increases sequentially from 1 within each &lt;principalID, affiliationId&gt; bucket.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="040b4-122">updatedBy</span><span class="sxs-lookup"><span data-stu-id="040b4-122">updatedBy</span></span></p></td>
<td><p><span data-ttu-id="040b4-123">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="040b4-123">int, not null</span></span></p></td>
<td><p><span data-ttu-id="040b4-124">Prinzipal, der das neueste Update durchführte.</span><span class="sxs-lookup"><span data-stu-id="040b4-124">Principal that did the latest update.</span></span> <span data-ttu-id="040b4-125">Dies ist normalerweise 1, was bedeutet, dass die Active Directory-Synchronisierung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="040b4-125">This is usually 1, which means Active Directory Sync.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="040b4-126">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="040b4-126">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="040b4-127">Spalten</span><span class="sxs-lookup"><span data-stu-id="040b4-127">Columns</span></span></th>
<th><span data-ttu-id="040b4-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="040b4-128">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="040b4-129">&lt;Prinzipal-, Index-, affiliationID&gt;</span><span class="sxs-lookup"><span data-stu-id="040b4-129">&lt;principalID, index, affiliationID&gt;</span></span></p></td>
<td><p><span data-ttu-id="040b4-130">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="040b4-130">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="040b4-131">Prinzipal-Nr</span><span class="sxs-lookup"><span data-stu-id="040b4-131">principalID</span></span></p></td>
<td><p><span data-ttu-id="040b4-132">Fremdschlüssel mit Lookup in der tblPrincipal. prinID-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="040b4-132">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="040b4-133">affiliationID</span><span class="sxs-lookup"><span data-stu-id="040b4-133">affiliationID</span></span></p></td>
<td><p><span data-ttu-id="040b4-134">Fremdschlüssel mit Lookup in der tblPrincipal. prinID-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="040b4-134">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="040b4-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="040b4-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

