---
title: 'Lync Server 2013: tblRoleType'
description: 'Lync Server 2013: tblRoleType.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblRoleType
ms:assetid: 1eac3a54-656a-40ac-b771-edfc64d6e34b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558623(v=OCS.15)
ms:contentKeyID: 48183577
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f458259acaee7821d5f6a7339b993c70fe65f595
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393911"
---
# <a name="tblroletype-in-lync-server-2013"></a><span data-ttu-id="769fb-103">tblRoleType in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="769fb-103">tblRoleType in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="769fb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="769fb-104">

<span> </span></span></span>

<span data-ttu-id="769fb-105">_**Letztes Änderungsdatum des Themas:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="769fb-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="769fb-106">tblRoleType ist eine statische Nachschlagetabelle mit Rollentypen und zugehörigen Berechtigungssätzen.</span><span class="sxs-lookup"><span data-stu-id="769fb-106">tblRoleType is a static lookup table with role types and their associated permission sets.</span></span>

### <a name="columns"></a><span data-ttu-id="769fb-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="769fb-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="769fb-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="769fb-108">Column</span></span></th>
<th><span data-ttu-id="769fb-109">Typ</span><span class="sxs-lookup"><span data-stu-id="769fb-109">Type</span></span></th>
<th><span data-ttu-id="769fb-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="769fb-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="769fb-111">rtypeID</span><span class="sxs-lookup"><span data-stu-id="769fb-111">rtypeID</span></span></p></td>
<td><p><span data-ttu-id="769fb-112">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="769fb-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="769fb-113">ID des Rollentyps.</span><span class="sxs-lookup"><span data-stu-id="769fb-113">Role type ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="769fb-114">rtypeDesc</span><span class="sxs-lookup"><span data-stu-id="769fb-114">rtypeDesc</span></span></p></td>
<td><p><span data-ttu-id="769fb-115">nvarchar (256); nicht NULL</span><span class="sxs-lookup"><span data-stu-id="769fb-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="769fb-116">Beschreibung des Rollentyps.</span><span class="sxs-lookup"><span data-stu-id="769fb-116">Role type description.</span></span> <span data-ttu-id="769fb-117">Es gibt vier verfügbare Rollen:</span><span class="sxs-lookup"><span data-stu-id="769fb-117">There are four available roles:</span></span></p>
<ul>
<li><p><span data-ttu-id="769fb-118">Mitglied: Chatroom-Mitglied</span><span class="sxs-lookup"><span data-stu-id="769fb-118">Member: Chat room member</span></span></p></li>
<li><p><span data-ttu-id="769fb-119">Manager: Chat Room Manager</span><span class="sxs-lookup"><span data-stu-id="769fb-119">Manager: Chat room manager</span></span></p></li>
<li><p><span data-ttu-id="769fb-120">Geäußert: Referent für einen Chatroom für Auditorium</span><span class="sxs-lookup"><span data-stu-id="769fb-120">Voiced: Presenter for an auditorium chat room</span></span></p></li>
<li><p><span data-ttu-id="769fb-121">Creator: kann Chatrooms erstellen</span><span class="sxs-lookup"><span data-stu-id="769fb-121">Creator: Can create chat rooms</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="769fb-122">rtypeAllowedPermSet</span><span class="sxs-lookup"><span data-stu-id="769fb-122">rtypeAllowedPermSet</span></span></p></td>
<td><p><span data-ttu-id="769fb-123">bigint, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="769fb-123">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="769fb-124">Der Berechtigungssatz für die Rolle.</span><span class="sxs-lookup"><span data-stu-id="769fb-124">Permission set for the role.</span></span> <span data-ttu-id="769fb-125">Die verwendeten Bits sind:</span><span class="sxs-lookup"><span data-stu-id="769fb-125">The used bits are:</span></span></p>
<ul>
<li><p><span data-ttu-id="769fb-126">2: true, wenn die Rolle Knoten verwalten kann.</span><span class="sxs-lookup"><span data-stu-id="769fb-126">2: True if the role can manage nodes.</span></span></p></li>
<li><p><span data-ttu-id="769fb-127">4: true, wenn die Rolle untergeordnete Knoten erstellen kann.</span><span class="sxs-lookup"><span data-stu-id="769fb-127">4: True if the role can create children nodes.</span></span></p></li>
<li><p><span data-ttu-id="769fb-128">7: true, wenn die Rolle einem Chatroom (oder Chatrooms einer Kategorie) beitreten kann.</span><span class="sxs-lookup"><span data-stu-id="769fb-128">7: True if the role can join a chat room (or children chat rooms of a category).</span></span></p></li>
<li><p><span data-ttu-id="769fb-129">8: true, wenn die Rolle in einem Chatroom (oder in Chatrooms einer Kategorie) chatten kann.</span><span class="sxs-lookup"><span data-stu-id="769fb-129">8: True if the role can chat in a chat room (or in children chat rooms of a category).</span></span></p></li>
<li><p><span data-ttu-id="769fb-130">10: true, wenn die Rolle das Chat-Protokoll lesen kann, selbst wenn Sie nicht zu einem Chatroom gehört.</span><span class="sxs-lookup"><span data-stu-id="769fb-130">10: True if the role can read chat history even when not joined to a chat room.</span></span></p></li>
<li><p><span data-ttu-id="769fb-131">11: true, wenn die Rolle den Chatroom sehen kann.</span><span class="sxs-lookup"><span data-stu-id="769fb-131">11: True if the role can see the chat room.</span></span> <span data-ttu-id="769fb-132">(Dies wird durch Faktoren wie Bereich und Sichtbarkeit weiter verfeinert.)</span><span class="sxs-lookup"><span data-stu-id="769fb-132">(This is further refined by factors such as scope and visibility.)</span></span></p></li>
<li><p><span data-ttu-id="769fb-133">12: true, wenn die Rolle in einem Auditorium-Chatroom chatten kann.</span><span class="sxs-lookup"><span data-stu-id="769fb-133">12: True if the role can chat in an auditorium chat room.</span></span></p></li>
<li><p><span data-ttu-id="769fb-134">13: true, wenn die Rolle Sichtbarkeitsregeln beim Anzeigen von Knoten umgehen kann.</span><span class="sxs-lookup"><span data-stu-id="769fb-134">13: True if the role can bypass visibility rules when viewing nodes.</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="769fb-135">Key</span><span class="sxs-lookup"><span data-stu-id="769fb-135">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="769fb-136">Spalte</span><span class="sxs-lookup"><span data-stu-id="769fb-136">Column</span></span></th>
<th><span data-ttu-id="769fb-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="769fb-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="769fb-138">rtypeID</span><span class="sxs-lookup"><span data-stu-id="769fb-138">rtypeID</span></span></p></td>
<td><p><span data-ttu-id="769fb-139">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="769fb-139">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="769fb-140">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="769fb-140">


</div>

<span> </span>

</div>

</div>

</span></span></div>

