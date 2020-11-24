---
title: 'Lync Server 2013: tblServerIdentity'
description: 'Lync Server 2013: tblServerIdentity.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblServerIdentity
ms:assetid: 5411c9bc-b0b3-41fc-8b7e-fa71cccd770b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558648(v=OCS.15)
ms:contentKeyID: 48184125
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e954618cb373f2cf4f1b7ed929c3aaf6d8875e92
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393903"
---
# <a name="tblserveridentity-in-lync-server-2013"></a><span data-ttu-id="dd501-103">tblServerIdentity in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dd501-103">tblServerIdentity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dd501-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dd501-104">

<span> </span></span></span>

<span data-ttu-id="dd501-105">_**Letztes Änderungsdatum des Themas:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="dd501-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="dd501-106">tblServerIdentity enthält die aktiven Chat Server im persistent Chat Serverpool.</span><span class="sxs-lookup"><span data-stu-id="dd501-106">tblServerIdentity contains the active chat servers in the Persistent Chat Server pool.</span></span>

### <a name="columns"></a><span data-ttu-id="dd501-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="dd501-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dd501-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="dd501-108">Column</span></span></th>
<th><span data-ttu-id="dd501-109">Typ</span><span class="sxs-lookup"><span data-stu-id="dd501-109">Type</span></span></th>
<th><span data-ttu-id="dd501-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd501-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd501-111">ServerID</span><span class="sxs-lookup"><span data-stu-id="dd501-111">serverID</span></span></p></td>
<td><p><span data-ttu-id="dd501-112">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="dd501-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="dd501-113">Server-ID.</span><span class="sxs-lookup"><span data-stu-id="dd501-113">Server ID.</span></span> <span data-ttu-id="dd501-114">Entspricht der Instanz-ID des zentralen Verwaltungsspeichers.</span><span class="sxs-lookup"><span data-stu-id="dd501-114">Corresponds to the instance ID from Central Management store.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="dd501-115">ServerAddress</span><span class="sxs-lookup"><span data-stu-id="dd501-115">serverAddress</span></span></p></td>
<td><p><span data-ttu-id="dd501-116">nvarchar (256); nicht NULL</span><span class="sxs-lookup"><span data-stu-id="dd501-116">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="dd501-117">Server Adresse unter Verwendung der Windows Communication Foundation-Adresse.</span><span class="sxs-lookup"><span data-stu-id="dd501-117">Server address using the Windows Communication Foundation address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="dd501-118">serverLastPingTime</span><span class="sxs-lookup"><span data-stu-id="dd501-118">serverLastPingTime</span></span></p></td>
<td><p><span data-ttu-id="dd501-119">datetime</span><span class="sxs-lookup"><span data-stu-id="dd501-119">datetime</span></span></p></td>
<td><p><span data-ttu-id="dd501-120">Der letzte Zeitpunkt, zu dem der Kanal Server diese Zeile aktualisiert hat, um zu beweisen, dass er ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="dd501-120">The latest time that the Channel Server updated this row to give evidence that it is running.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="dd501-121">Key</span><span class="sxs-lookup"><span data-stu-id="dd501-121">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="dd501-122">Spalte</span><span class="sxs-lookup"><span data-stu-id="dd501-122">Column</span></span></th>
<th><span data-ttu-id="dd501-123">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="dd501-123">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="dd501-124">ServerID</span><span class="sxs-lookup"><span data-stu-id="dd501-124">serverID</span></span></p></td>
<td><p><span data-ttu-id="dd501-125">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="dd501-125">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="dd501-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dd501-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

