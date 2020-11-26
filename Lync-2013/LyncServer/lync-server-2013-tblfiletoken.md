---
title: 'Lync Server 2013: tblFileToken'
description: 'Lync Server 2013: tblFileToken.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblFileToken
ms:assetid: 49e7dd79-1607-443c-818a-88c160e4ed06
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558646(v=OCS.15)
ms:contentKeyID: 48184073
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c0a0465bd769cff5c23c00a98f79e2346232175
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423533"
---
# <a name="tblfiletoken-in-lync-server-2013"></a><span data-ttu-id="b1ef6-103">tblFileToken in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1ef6-103">tblFileToken in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b1ef6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b1ef6-104">

<span> </span></span></span>

<span data-ttu-id="b1ef6-105">_**Letztes Änderungsdatum des Themas:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="b1ef6-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="b1ef6-106">tblFileToken enthält temporäre Token für Datei Übertragungs Zwecke.</span><span class="sxs-lookup"><span data-stu-id="b1ef6-106">tblFileToken contains temporary tokens for file transfer purposes.</span></span>

### <a name="columns"></a><span data-ttu-id="b1ef6-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="b1ef6-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b1ef6-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="b1ef6-108">Column</span></span></th>
<th><span data-ttu-id="b1ef6-109">Typ</span><span class="sxs-lookup"><span data-stu-id="b1ef6-109">Type</span></span></th>
<th><span data-ttu-id="b1ef6-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1ef6-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1ef6-111">FileToken</span><span class="sxs-lookup"><span data-stu-id="b1ef6-111">fileToken</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-112">nvarchar (50); nicht NULL</span><span class="sxs-lookup"><span data-stu-id="b1ef6-112">nvarchar (50), not null</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-113">Eindeutiges Token (eine GUID).</span><span class="sxs-lookup"><span data-stu-id="b1ef6-113">Unique token (a GUID).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1ef6-114">fileTokenUserID</span><span class="sxs-lookup"><span data-stu-id="b1ef6-114">fileTokenUserID</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-115">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="b1ef6-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-116">Die ID des Prinzipals, der die Datei übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="b1ef6-116">ID of the principal that is transferring the file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1ef6-117">fileTokenChannelID</span><span class="sxs-lookup"><span data-stu-id="b1ef6-117">fileTokenChannelID</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-118">GUID, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="b1ef6-118">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-119">GUID des Chatroom-Knotens.</span><span class="sxs-lookup"><span data-stu-id="b1ef6-119">GUID of the chat room node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1ef6-120">fileTokenExpireDate</span><span class="sxs-lookup"><span data-stu-id="b1ef6-120">fileTokenExpireDate</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-121">DateTime, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="b1ef6-121">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-122">Ablaufzeit.</span><span class="sxs-lookup"><span data-stu-id="b1ef6-122">Expiration time.</span></span> <span data-ttu-id="b1ef6-123">(Token werden nach 30 Minuten ablaufen, es sei denn, angeheftet (siehe die folgenden Beschreibungen in dieser Spalte).</span><span class="sxs-lookup"><span data-stu-id="b1ef6-123">(Tokens expire after 30 minutes, unless pinned (see the following descriptions in this column).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1ef6-124">fileTokenComplianceFileUrl</span><span class="sxs-lookup"><span data-stu-id="b1ef6-124">fileTokenComplianceFileUrl</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-125">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b1ef6-125">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-126">Die URL der übertragenen Datei (für die Verwendung des Kompatibilitätsdiensts).</span><span class="sxs-lookup"><span data-stu-id="b1ef6-126">URL of the transferred file (for Compliance service use).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1ef6-127">fileTokenComplianceThumbnailUrl</span><span class="sxs-lookup"><span data-stu-id="b1ef6-127">fileTokenComplianceThumbnailUrl</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b1ef6-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-129">Die URL der Miniaturansicht für die übertragene Datei (für die Verwendung des Kompatibilitätsdiensts).</span><span class="sxs-lookup"><span data-stu-id="b1ef6-129">URL of the thumbnail for the transferred file (for Compliance service use).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1ef6-130">fileTokenComplianceTime</span><span class="sxs-lookup"><span data-stu-id="b1ef6-130">fileTokenComplianceTime</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-131">datetime2</span><span class="sxs-lookup"><span data-stu-id="b1ef6-131">datetime2</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-132">Timestamp für den eigentlichen Dateiübertragungsvorgang (für die Verwendung des Kompatibilitätsdiensts).</span><span class="sxs-lookup"><span data-stu-id="b1ef6-132">Timestamp for the actual file transfer operation (for Compliance service use).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1ef6-133">fileTokenComplianceIsUpload</span><span class="sxs-lookup"><span data-stu-id="b1ef6-133">fileTokenComplianceIsUpload</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-134">bit</span><span class="sxs-lookup"><span data-stu-id="b1ef6-134">bit</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-135">True, wenn Upload; False, wenn Download (für Compliance-Dienstnutzung).</span><span class="sxs-lookup"><span data-stu-id="b1ef6-135">True if upload; False if download (for Compliance service use).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1ef6-136">fileTokenCompliancePinned</span><span class="sxs-lookup"><span data-stu-id="b1ef6-136">fileTokenCompliancePinned</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-137">Bit, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="b1ef6-137">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-138">True, wenn Token angeheftet ist.</span><span class="sxs-lookup"><span data-stu-id="b1ef6-138">True if token is pinned.</span></span> <span data-ttu-id="b1ef6-139">Sie wird verwendet, um das Token in der Tabelle beizubehalten, bis der Kompatibilitätsdienst die entsprechenden Felder aus ihm abrufen kann.</span><span class="sxs-lookup"><span data-stu-id="b1ef6-139">It’s used to keep the token in the table until Compliance service has a chance to retrieve the relevant fields from it.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="b1ef6-140">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="b1ef6-140">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b1ef6-141">Spalte</span><span class="sxs-lookup"><span data-stu-id="b1ef6-141">Column</span></span></th>
<th><span data-ttu-id="b1ef6-142">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1ef6-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1ef6-143">FileToken</span><span class="sxs-lookup"><span data-stu-id="b1ef6-143">fileToken</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-144">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="b1ef6-144">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1ef6-145">fileTokenChannelID</span><span class="sxs-lookup"><span data-stu-id="b1ef6-145">fileTokenChannelID</span></span></p></td>
<td><p><span data-ttu-id="b1ef6-146">Fremdschlüssel mit Lookup in der tblNode. nodeGuid-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="b1ef6-146">Foreign key with lookup in tblNode.nodeGuid table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b1ef6-147">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b1ef6-147">


</div>

<span> </span>

</div>

</div>

</span></span></div>

