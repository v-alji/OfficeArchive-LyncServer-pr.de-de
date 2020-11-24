---
title: 'Lync Server 2013: tblPrincipalMemberDifference'
description: 'Lync Server 2013: tblPrincipalMemberDifference.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalMemberDifference
ms:assetid: 0b94f555-6888-4fe0-a048-4660a2513276
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558612(v=OCS.15)
ms:contentKeyID: 48183379
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ce7c770a6fed02dc27d2493816fae58943d391a6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393938"
---
# <a name="tblprincipalmemberdifference-in-lync-server-2013"></a><span data-ttu-id="b0dbc-103">tblPrincipalMemberDifference in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b0dbc-103">tblPrincipalMemberDifference in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b0dbc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b0dbc-104">

<span> </span></span></span>

<span data-ttu-id="b0dbc-105">_**Letztes Änderungsdatum des Themas:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="b0dbc-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="b0dbc-106">tblPrincipalMemberDifference enthält Gruppenmitgliedschaftsänderungen (sowohl hinzugefügte als auch entfernte Mitglieder), die noch nicht von den späteren Synchronisierungs Schritten von Active Directory-Domänendiensten verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="b0dbc-106">tblPrincipalMemberDifference contains group membership changes (both added and removed members) that have not yet been processed by the later Active Directory Domain Services Sync steps.</span></span>

### <a name="columns"></a><span data-ttu-id="b0dbc-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="b0dbc-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b0dbc-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="b0dbc-108">Column</span></span></th>
<th><span data-ttu-id="b0dbc-109">Typ</span><span class="sxs-lookup"><span data-stu-id="b0dbc-109">Type</span></span></th>
<th><span data-ttu-id="b0dbc-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0dbc-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0dbc-111">prinGuid</span><span class="sxs-lookup"><span data-stu-id="b0dbc-111">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="b0dbc-112">GUID, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="b0dbc-112">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="b0dbc-113">Prinzipal-GUID der geänderten Gruppe.</span><span class="sxs-lookup"><span data-stu-id="b0dbc-113">Principal GUID of the group that changed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b0dbc-114">memberADPath</span><span class="sxs-lookup"><span data-stu-id="b0dbc-114">memberADPath</span></span></p></td>
<td><p><span data-ttu-id="b0dbc-115">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="b0dbc-115">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="b0dbc-116">Distinguished Name des Members.</span><span class="sxs-lookup"><span data-stu-id="b0dbc-116">Distinguished name of the member.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b0dbc-117">memberRemoved</span><span class="sxs-lookup"><span data-stu-id="b0dbc-117">memberRemoved</span></span></p></td>
<td><p><span data-ttu-id="b0dbc-118">Bit, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="b0dbc-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="b0dbc-119">False, wenn das Mitglied hinzugefügt wurde.</span><span class="sxs-lookup"><span data-stu-id="b0dbc-119">False if the member was added.</span></span> <span data-ttu-id="b0dbc-120">"True", wenn das Element entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="b0dbc-120">True if the member was removed.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="b0dbc-121">Key</span><span class="sxs-lookup"><span data-stu-id="b0dbc-121">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b0dbc-122">Spalte</span><span class="sxs-lookup"><span data-stu-id="b0dbc-122">Column</span></span></th>
<th><span data-ttu-id="b0dbc-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b0dbc-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b0dbc-124">&lt;prinGuid, memberADPath&gt;</span><span class="sxs-lookup"><span data-stu-id="b0dbc-124">&lt;prinGuid, memberADPath&gt;</span></span></p></td>
<td><p><span data-ttu-id="b0dbc-125">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="b0dbc-125">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b0dbc-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b0dbc-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

