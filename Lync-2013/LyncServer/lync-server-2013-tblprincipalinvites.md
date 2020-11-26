---
title: 'Lync Server 2013: tblPrincipalInvites'
description: 'Lync Server 2013: tblPrincipalInvites.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalInvites
ms:assetid: 548ec156-4d1a-469d-a804-62cff226e5c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558650(v=OCS.15)
ms:contentKeyID: 48184141
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d30d741864ed2a3cfbec8329215be33c21b3b262
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423505"
---
# <a name="tblprincipalinvites-in-lync-server-2013"></a><span data-ttu-id="d5f4f-103">tblPrincipalInvites in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d5f4f-103">tblPrincipalInvites in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d5f4f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d5f4f-104">

<span> </span></span></span>

<span data-ttu-id="d5f4f-105">_**Letztes Änderungsdatum des Themas:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="d5f4f-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="d5f4f-106">tblPrincipalInvites enthält Einladungen für alle bereitgestellten Benutzer für alle Knoten, bei denen die automatische Einladung aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-106">tblPrincipalInvites contains invitations for all provisioned users for all nodes with auto-invite on.</span></span>

### <a name="columns"></a><span data-ttu-id="d5f4f-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="d5f4f-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5f4f-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="d5f4f-108">Column</span></span></th>
<th><span data-ttu-id="d5f4f-109">Typ</span><span class="sxs-lookup"><span data-stu-id="d5f4f-109">Type</span></span></th>
<th><span data-ttu-id="d5f4f-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5f4f-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d5f4f-111">prinID</span><span class="sxs-lookup"><span data-stu-id="d5f4f-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="d5f4f-112">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="d5f4f-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="d5f4f-113">Prinzipal-ID.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f4f-114">invID</span><span class="sxs-lookup"><span data-stu-id="d5f4f-114">invID</span></span></p></td>
<td><p><span data-ttu-id="d5f4f-115">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="d5f4f-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="d5f4f-116">Eindeutige sequenzielle Zahl (pro Prinzipal-ID), die aus der tblLastInviteId-Tabelle generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-116">Unique sequential number (per principal ID) generated from tblLastInviteId table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5f4f-117">nodeID</span><span class="sxs-lookup"><span data-stu-id="d5f4f-117">nodeID</span></span></p></td>
<td><p><span data-ttu-id="d5f4f-118">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="d5f4f-118">int, not null</span></span></p></td>
<td><p><span data-ttu-id="d5f4f-119">Knoten-ID (nur Chatroom).</span><span class="sxs-lookup"><span data-stu-id="d5f4f-119">Node ID (chat room only).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f4f-120">createdOn</span><span class="sxs-lookup"><span data-stu-id="d5f4f-120">createdOn</span></span></p></td>
<td><p><span data-ttu-id="d5f4f-121">DateTime, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="d5f4f-121">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="d5f4f-122">Zeitpunkt der Erstellung.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-122">Time of creation.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="d5f4f-123">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="d5f4f-123">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d5f4f-124">Spalte</span><span class="sxs-lookup"><span data-stu-id="d5f4f-124">Column</span></span></th>
<th><span data-ttu-id="d5f4f-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d5f4f-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d5f4f-126">&lt;prinID, Knoten-Nr.&gt;</span><span class="sxs-lookup"><span data-stu-id="d5f4f-126">&lt;prinID, nodeID&gt;</span></span></p></td>
<td><p><span data-ttu-id="d5f4f-127">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="d5f4f-127">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d5f4f-128">prinID</span><span class="sxs-lookup"><span data-stu-id="d5f4f-128">prinID</span></span></p></td>
<td><p><span data-ttu-id="d5f4f-129">Fremdschlüssel mit Lookup in der tblPrincipal. prinID-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d5f4f-129">Foreign key with lookup in tblPrincipal.prinID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d5f4f-130">nodeID</span><span class="sxs-lookup"><span data-stu-id="d5f4f-130">nodeID</span></span></p></td>
<td><p><span data-ttu-id="d5f4f-131">Fremdschlüssel mit Lookup in der tblNode. Node-Tabelle</span><span class="sxs-lookup"><span data-stu-id="d5f4f-131">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d5f4f-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d5f4f-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

