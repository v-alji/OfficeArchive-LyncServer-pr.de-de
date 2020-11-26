---
title: 'Lync Server 2013: tblComplianceParticipant'
description: 'Lync Server 2013: tblComplianceParticipant.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceParticipant
ms:assetid: 5d7e0dea-74f7-46d1-badf-b94abc8f066d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558655(v=OCS.15)
ms:contentKeyID: 48184262
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1385b0a635f003a72de93f10f72642314ad7ebd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444455"
---
# <a name="tblcomplianceparticipant-in-lync-server-2013"></a><span data-ttu-id="314d9-103">tblComplianceParticipant in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="314d9-103">tblComplianceParticipant in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="314d9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="314d9-104">

<span> </span></span></span>

<span data-ttu-id="314d9-105">_**Letztes Änderungsdatum des Themas:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="314d9-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="314d9-106">tblComplianceParticipant enthält die aktuellen Teilnehmer pro Kanal und pro Server.</span><span class="sxs-lookup"><span data-stu-id="314d9-106">tblComplianceParticipant contains the current participants per channel and per server.</span></span>

### <a name="columns"></a><span data-ttu-id="314d9-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="314d9-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="314d9-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="314d9-108">Column</span></span></th>
<th><span data-ttu-id="314d9-109">Typ</span><span class="sxs-lookup"><span data-stu-id="314d9-109">Type</span></span></th>
<th><span data-ttu-id="314d9-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="314d9-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="314d9-111">channelUri</span><span class="sxs-lookup"><span data-stu-id="314d9-111">channelUri</span></span></p></td>
<td><p><span data-ttu-id="314d9-112">nvarchar (255); nicht NULL</span><span class="sxs-lookup"><span data-stu-id="314d9-112">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="314d9-113">Kanal Uniform Resource Identifier (URI).</span><span class="sxs-lookup"><span data-stu-id="314d9-113">Channel Uniform Resource Identifier (URI).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="314d9-114">UserID</span><span class="sxs-lookup"><span data-stu-id="314d9-114">userId</span></span></p></td>
<td><p><span data-ttu-id="314d9-115">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="314d9-115">int, not null</span></span></p></td>
<td><p><span data-ttu-id="314d9-116">Prinzipal-ID des Teilnehmers (entsprechend der Tabelle tblPrincipal. prinID).</span><span class="sxs-lookup"><span data-stu-id="314d9-116">Principal ID of the participant (corresponding to tblPrincipal.prinID table).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="314d9-117">joinedAt</span><span class="sxs-lookup"><span data-stu-id="314d9-117">joinedAt</span></span></p></td>
<td><p><span data-ttu-id="314d9-118">bigint, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="314d9-118">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="314d9-119">Zeitstempel des Joining-Ereignisses</span><span class="sxs-lookup"><span data-stu-id="314d9-119">Time stamp of the joining event.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="314d9-120">partedAt</span><span class="sxs-lookup"><span data-stu-id="314d9-120">partedAt</span></span></p></td>
<td><p><span data-ttu-id="314d9-121">bigint</span><span class="sxs-lookup"><span data-stu-id="314d9-121">bigint</span></span></p></td>
<td><p><span data-ttu-id="314d9-122">NULL, wenn der Teilnehmer noch verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="314d9-122">Null if participant is still joined.</span></span> <span data-ttu-id="314d9-123">Der Zeitstempel des Kanals, der das Ereignis verlässt, wenn nicht NULL.</span><span class="sxs-lookup"><span data-stu-id="314d9-123">The time stamp of the channel leaving event if not null.</span></span></p>
<p><span data-ttu-id="314d9-124">Diese Einträge werden schließlich entfernt, wenn alle Übersetzer das Ereignis verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="314d9-124">These entries are eventually removed when all translators process the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="314d9-125">userUri</span><span class="sxs-lookup"><span data-stu-id="314d9-125">userUri</span></span></p></td>
<td><p><span data-ttu-id="314d9-126">nvarchar (255); nicht NULL</span><span class="sxs-lookup"><span data-stu-id="314d9-126">nvarchar(255), not null</span></span></p></td>
<td><p><span data-ttu-id="314d9-127">Benutzer-URI.</span><span class="sxs-lookup"><span data-stu-id="314d9-127">User URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="314d9-128">ServerID</span><span class="sxs-lookup"><span data-stu-id="314d9-128">serverID</span></span></p></td>
<td><p><span data-ttu-id="314d9-129">int</span><span class="sxs-lookup"><span data-stu-id="314d9-129">int</span></span></p></td>
<td><p><span data-ttu-id="314d9-130">Serveridentität (wie in der Tabelle tblServerIdentity. Server-ID).</span><span class="sxs-lookup"><span data-stu-id="314d9-130">Server identity (as in tblServerIdentity.serverID table).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="314d9-131">SessionID</span><span class="sxs-lookup"><span data-stu-id="314d9-131">sessionId</span></span></p></td>
<td><p><span data-ttu-id="314d9-132">bigint</span><span class="sxs-lookup"><span data-stu-id="314d9-132">bigint</span></span></p></td>
<td><p><span data-ttu-id="314d9-133">Server Sitzung.</span><span class="sxs-lookup"><span data-stu-id="314d9-133">Server session.</span></span> <span data-ttu-id="314d9-134">Hierbei handelt es sich um eine Zufallszahl, die bei jedem Start eines Chat-Diensts generiert wird.</span><span class="sxs-lookup"><span data-stu-id="314d9-134">This is a random number generated each time a Chat service starts.</span></span> <span data-ttu-id="314d9-135">Sie wird zur Unterscheidung von Sitzungen zum Zweck der Identifizierung verwaister Teilnehmer verwendet.</span><span class="sxs-lookup"><span data-stu-id="314d9-135">It is used to differentiate sessions for the purpose of identifying orphaned participants.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="314d9-136">Key</span><span class="sxs-lookup"><span data-stu-id="314d9-136">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="314d9-137">Spalte</span><span class="sxs-lookup"><span data-stu-id="314d9-137">Column</span></span></th>
<th><span data-ttu-id="314d9-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="314d9-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="314d9-139">&lt;channelUri, UserID, joinedAt&gt;</span><span class="sxs-lookup"><span data-stu-id="314d9-139">&lt;channelUri, userId, joinedAt&gt;</span></span></p></td>
<td><p><span data-ttu-id="314d9-140">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="314d9-140">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="314d9-141">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="314d9-141">


</div>

<span> </span>

</div>

</div>

</span></span></div>

