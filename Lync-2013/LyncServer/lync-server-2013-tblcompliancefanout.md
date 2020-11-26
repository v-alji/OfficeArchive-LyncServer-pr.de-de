---
title: 'Lync Server 2013: tblComplianceFanout'
description: 'Lync Server 2013: tblComplianceFanout.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceFanout
ms:assetid: f5d9f342-a7cb-4b54-baa6-e656256b75ad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615050(v=OCS.15)
ms:contentKeyID: 48185828
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0cb94fff579c504598f027c8c68c7dde00a5a516
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423528"
---
# <a name="tblcompliancefanout-in-lync-server-2013"></a><span data-ttu-id="9c6d5-103">tblComplianceFanout in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c6d5-103">tblComplianceFanout in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9c6d5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9c6d5-104">

<span> </span></span></span>

<span data-ttu-id="9c6d5-105">_**Letztes Änderungsdatum des Themas:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="9c6d5-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="9c6d5-106">tblComplianceFanout enthält alle Server, die ein Compliance-Ereignis verarbeitet haben.</span><span class="sxs-lookup"><span data-stu-id="9c6d5-106">tblComplianceFanout contains all servers that processed a compliance event.</span></span>

### <a name="columns"></a><span data-ttu-id="9c6d5-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="9c6d5-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c6d5-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="9c6d5-108">Column</span></span></th>
<th><span data-ttu-id="9c6d5-109">Typ</span><span class="sxs-lookup"><span data-stu-id="9c6d5-109">Type</span></span></th>
<th><span data-ttu-id="9c6d5-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c6d5-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c6d5-111">fanoutEventID</span><span class="sxs-lookup"><span data-stu-id="9c6d5-111">fanoutEventID</span></span></p></td>
<td><p><span data-ttu-id="9c6d5-112">int</span><span class="sxs-lookup"><span data-stu-id="9c6d5-112">int</span></span></p></td>
<td><p><span data-ttu-id="9c6d5-113">Ereignis-ID.</span><span class="sxs-lookup"><span data-stu-id="9c6d5-113">Event ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c6d5-114">fanoutServerID</span><span class="sxs-lookup"><span data-stu-id="9c6d5-114">fanoutServerID</span></span></p></td>
<td><p><span data-ttu-id="9c6d5-115">int</span><span class="sxs-lookup"><span data-stu-id="9c6d5-115">int</span></span></p></td>
<td><p><span data-ttu-id="9c6d5-116">Serveridentität (entsprechend der Tabelle "tblServerIdentity. Serverkennung").</span><span class="sxs-lookup"><span data-stu-id="9c6d5-116">Server identity (corresponding to tblServerIdentity.serverID table).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="9c6d5-117">Key</span><span class="sxs-lookup"><span data-stu-id="9c6d5-117">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c6d5-118">Spalte</span><span class="sxs-lookup"><span data-stu-id="9c6d5-118">Column</span></span></th>
<th><span data-ttu-id="9c6d5-119">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="9c6d5-119">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c6d5-120">fanoutEventID</span><span class="sxs-lookup"><span data-stu-id="9c6d5-120">fanoutEventID</span></span></p></td>
<td><p><span data-ttu-id="9c6d5-121">Fremdschlüssel mit Lookup in der tblComplianceData. cmplEventID-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="9c6d5-121">Foreign key with lookup in tblComplianceData.cmplEventID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9c6d5-122">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9c6d5-122">


</div>

<span> </span>

</div>

</div>

</span></span></div>

