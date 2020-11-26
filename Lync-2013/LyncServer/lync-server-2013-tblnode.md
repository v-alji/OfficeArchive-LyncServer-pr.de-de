---
title: 'Lync Server 2013: tblNode'
description: 'Lync Server 2013: tblNode.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblNode
ms:assetid: a31d2961-aa83-4286-a12e-15d279c95f19
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615024(v=OCS.15)
ms:contentKeyID: 48184960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d0a5d630621c32cbc54501249c7a679bf4023c60
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423519"
---
# <a name="tblnode-in-lync-server-2013"></a><span data-ttu-id="93256-103">tblNode in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="93256-103">tblNode in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="93256-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="93256-104">

<span> </span></span></span>

<span data-ttu-id="93256-105">_**Letztes Änderungsdatum des Themas:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="93256-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="93256-106">tblNode enthält die Objektstruktur (mit Kategorien-oder Chatroom-Knoten), wie Sie in der lync Server 2013-Systemsteuerung und den administrativen Cmdlets verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="93256-106">tblNode contains the object tree (with category or chat room nodes) as managed in the Lync Server 2013 Control Panel and administrative cmdlets.</span></span>

### <a name="columns"></a><span data-ttu-id="93256-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="93256-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93256-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="93256-108">Column</span></span></th>
<th><span data-ttu-id="93256-109">Typ</span><span class="sxs-lookup"><span data-stu-id="93256-109">Type</span></span></th>
<th><span data-ttu-id="93256-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93256-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93256-111">nodeID</span><span class="sxs-lookup"><span data-stu-id="93256-111">nodeID</span></span></p></td>
<td><p><span data-ttu-id="93256-112">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="93256-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="93256-113">Knoten-ID (eindeutige Nummer).</span><span class="sxs-lookup"><span data-stu-id="93256-113">Node ID (unique number).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93256-114">nodeGuid</span><span class="sxs-lookup"><span data-stu-id="93256-114">nodeGuid</span></span></p></td>
<td><p><span data-ttu-id="93256-115">GUID, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="93256-115">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="93256-116">Knoten-GUID.</span><span class="sxs-lookup"><span data-stu-id="93256-116">Node GUID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93256-117">parentID</span><span class="sxs-lookup"><span data-stu-id="93256-117">parentID</span></span></p></td>
<td><p><span data-ttu-id="93256-118">int</span><span class="sxs-lookup"><span data-stu-id="93256-118">int</span></span></p></td>
<td><p><span data-ttu-id="93256-119">Knoten-ID des übergeordneten Elements.</span><span class="sxs-lookup"><span data-stu-id="93256-119">Node ID of parent.</span></span> <span data-ttu-id="93256-120">Der Stammknoten (mit ID 1) schließt sich ebenfalls als übergeordnetes Element ein.</span><span class="sxs-lookup"><span data-stu-id="93256-120">The root node (with ID 1) includes itself as parent as well.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93256-121">NodeType</span><span class="sxs-lookup"><span data-stu-id="93256-121">nodeType</span></span></p></td>
<td><p><span data-ttu-id="93256-122">Bit, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="93256-122">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="93256-123">"True", wenn der Knoten eine Kategorie ist.</span><span class="sxs-lookup"><span data-stu-id="93256-123">True if the node is a category.</span></span></p>
<p><span data-ttu-id="93256-124">False, wenn es sich bei dem Knoten um einen Chatroom handelt.</span><span class="sxs-lookup"><span data-stu-id="93256-124">False if the node is a chat room.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93256-125">nodeName</span><span class="sxs-lookup"><span data-stu-id="93256-125">nodeName</span></span></p></td>
<td><p><span data-ttu-id="93256-126">nvarchar (256); nicht NULL</span><span class="sxs-lookup"><span data-stu-id="93256-126">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="93256-127">Knotenname</span><span class="sxs-lookup"><span data-stu-id="93256-127">Node name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93256-128">nodeDesc</span><span class="sxs-lookup"><span data-stu-id="93256-128">nodeDesc</span></span></p></td>
<td><p><span data-ttu-id="93256-129">nvarchar (256); nicht NULL</span><span class="sxs-lookup"><span data-stu-id="93256-129">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="93256-130">Knotenbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="93256-130">Node description.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93256-131">einladen</span><span class="sxs-lookup"><span data-stu-id="93256-131">invite</span></span></p></td>
<td><p><span data-ttu-id="93256-132">bit</span><span class="sxs-lookup"><span data-stu-id="93256-132">bit</span></span></p></td>
<td><p><span data-ttu-id="93256-133">Für Kategorien:</span><span class="sxs-lookup"><span data-stu-id="93256-133">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="93256-134">True, wenn Einladungen aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="93256-134">True if invites are on.</span></span></p></li>
<li><p><span data-ttu-id="93256-135">False, wenn Einladungen deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="93256-135">False if invites are off.</span></span></p></li>
</ul>
<p><span data-ttu-id="93256-136">Für Räume:</span><span class="sxs-lookup"><span data-stu-id="93256-136">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="93256-137">False, wenn Einladungen deaktiviert sind (überschreibt die übergeordnete Kategorie).</span><span class="sxs-lookup"><span data-stu-id="93256-137">False if invites are off (overrides the parent category).</span></span></p></li>
<li><p><span data-ttu-id="93256-138">NULL, wenn die invites-Einstellung von der übergeordneten Kategorie geerbt wird.</span><span class="sxs-lookup"><span data-stu-id="93256-138">Null if the invites setting is inherited from the parent category.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93256-139">angemeldet</span><span class="sxs-lookup"><span data-stu-id="93256-139">logged</span></span></p></td>
<td><p><span data-ttu-id="93256-140">bit</span><span class="sxs-lookup"><span data-stu-id="93256-140">bit</span></span></p></td>
<td><p><span data-ttu-id="93256-141">Für Kategorien:</span><span class="sxs-lookup"><span data-stu-id="93256-141">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="93256-142">"True", wenn das Chat-Protokoll aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="93256-142">True if chat history is on.</span></span></p></li>
<li><p><span data-ttu-id="93256-143">Falsch, wenn das Chat-Protokoll deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="93256-143">False if chat history is off.</span></span></p></li>
</ul>
<p><span data-ttu-id="93256-144">Für Räume:</span><span class="sxs-lookup"><span data-stu-id="93256-144">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="93256-145">NULL.</span><span class="sxs-lookup"><span data-stu-id="93256-145">Null.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93256-146">filePost</span><span class="sxs-lookup"><span data-stu-id="93256-146">filePost</span></span></p></td>
<td><p><span data-ttu-id="93256-147">bit</span><span class="sxs-lookup"><span data-stu-id="93256-147">bit</span></span></p></td>
<td><p><span data-ttu-id="93256-148">Für Kategorien:</span><span class="sxs-lookup"><span data-stu-id="93256-148">For categories:</span></span></p>
<ul>
<li><p><span data-ttu-id="93256-149">"True", wenn Dateiuploads zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="93256-149">True if file uploads are allowed.</span></span></p></li>
<li><p><span data-ttu-id="93256-150">False, wenn Dateiuploads nicht zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="93256-150">False if file uploads are disallowed.</span></span></p></li>
</ul>
<p><span data-ttu-id="93256-151">Für Räume:</span><span class="sxs-lookup"><span data-stu-id="93256-151">For rooms:</span></span></p>
<ul>
<li><p><span data-ttu-id="93256-152">NULL.</span><span class="sxs-lookup"><span data-stu-id="93256-152">Null.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93256-153">deaktiviert</span><span class="sxs-lookup"><span data-stu-id="93256-153">disabled</span></span></p></td>
<td><p><span data-ttu-id="93256-154">Bit, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="93256-154">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="93256-155">"True", wenn der Chatroom deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="93256-155">True if the chat room is disabled.</span></span> <span data-ttu-id="93256-156">Gilt nur für Chatrooms.</span><span class="sxs-lookup"><span data-stu-id="93256-156">Applies only to chat rooms.</span></span> <span data-ttu-id="93256-157">(Falsch für Kategorien.)</span><span class="sxs-lookup"><span data-stu-id="93256-157">(False for categories.)</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93256-158">Verhalten</span><span class="sxs-lookup"><span data-stu-id="93256-158">behavior</span></span></p></td>
<td><p><span data-ttu-id="93256-159">smallint, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="93256-159">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="93256-160">Verhalten (in der EnumValue-Tabelle nachgeschlagen):</span><span class="sxs-lookup"><span data-stu-id="93256-160">Behavior (looked up in EnumValue table):</span></span></p>
<ul>
<li><p><span data-ttu-id="93256-161">4: Normal (normale Chatrooms).</span><span class="sxs-lookup"><span data-stu-id="93256-161">4: Normal (normal chat rooms).</span></span></p></li>
<li><p><span data-ttu-id="93256-162">5: Auditorium (Auditorium-Chatrooms, nur Referenten können dazu beitragen).</span><span class="sxs-lookup"><span data-stu-id="93256-162">5: Auditorium (auditorium chat rooms, only presenters can contribute).</span></span></p></li>
</ul>
<p><span data-ttu-id="93256-163">Gilt nur für Chatrooms.</span><span class="sxs-lookup"><span data-stu-id="93256-163">Applies only to chat rooms.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93256-164">Sichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="93256-164">visibility</span></span></p></td>
<td><p><span data-ttu-id="93256-165">smallint, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="93256-165">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="93256-166">Sichtbarkeit (in der EnumValue-Tabelle nachgeschlagen):</span><span class="sxs-lookup"><span data-stu-id="93256-166">Visibility (looked up on EnumValue table):</span></span></p>
<ul>
<li><p><span data-ttu-id="93256-167">2: privat</span><span class="sxs-lookup"><span data-stu-id="93256-167">2: Private</span></span></p></li>
<li><p><span data-ttu-id="93256-168">3: Gültigkeitsbereich</span><span class="sxs-lookup"><span data-stu-id="93256-168">3: Scoped</span></span></p></li>
<li><p><span data-ttu-id="93256-169">6: Öffnen</span><span class="sxs-lookup"><span data-stu-id="93256-169">6: Open</span></span></p></li>
</ul>
<p><span data-ttu-id="93256-170">Gilt nur für Chatrooms.</span><span class="sxs-lookup"><span data-stu-id="93256-170">Applies only to chat rooms.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93256-171">siopID</span><span class="sxs-lookup"><span data-stu-id="93256-171">siopID</span></span></p></td>
<td><p><span data-ttu-id="93256-172">GUID</span><span class="sxs-lookup"><span data-stu-id="93256-172">GUID</span></span></p></td>
<td><p><span data-ttu-id="93256-173">Add-In GUID, wenn diesem Chatroom ein Add-in zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="93256-173">Add-In GUID if an add-in is associated with this chat room.</span></span> <span data-ttu-id="93256-174">(Kategorien verfügen nicht über Add-Ins.)</span><span class="sxs-lookup"><span data-stu-id="93256-174">(Categories do not have add-ins.)</span></span></p>
<p><span data-ttu-id="93256-175">Die Add-in-Informationen werden in der SiopWhiteList-Tabelle nachgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="93256-175">The add-in information is looked up in SiopWhiteList table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93256-176">nodeAddedBy</span><span class="sxs-lookup"><span data-stu-id="93256-176">nodeAddedBy</span></span></p></td>
<td><p><span data-ttu-id="93256-177">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="93256-177">int, not null</span></span></p></td>
<td><p><span data-ttu-id="93256-178">Die ID des Prinzipals, der diesen Knoten erstellt hat.</span><span class="sxs-lookup"><span data-stu-id="93256-178">ID of the principal that created this node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93256-179">nodeAddedOn</span><span class="sxs-lookup"><span data-stu-id="93256-179">nodeAddedOn</span></span></p></td>
<td><p><span data-ttu-id="93256-180">bigint, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="93256-180">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="93256-181">Zeitstempel der Knotenerstellung.</span><span class="sxs-lookup"><span data-stu-id="93256-181">Time stamp of the node creation.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93256-182">nodeUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="93256-182">nodeUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="93256-183">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="93256-183">int, not null</span></span></p></td>
<td><p><span data-ttu-id="93256-184">Die ID des Prinzipals, der das neueste Update dieses Knotens durchführte.</span><span class="sxs-lookup"><span data-stu-id="93256-184">ID of the principal that did the latest update of this node.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93256-185">nodeUpdatedOn</span><span class="sxs-lookup"><span data-stu-id="93256-185">nodeUpdatedOn</span></span></p></td>
<td><p><span data-ttu-id="93256-186">bigint, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="93256-186">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="93256-187">Zeitstempel der letzten Aktualisierung dieses Knotens.</span><span class="sxs-lookup"><span data-stu-id="93256-187">Time stamp of the latest update of this node.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93256-188">purgedOn</span><span class="sxs-lookup"><span data-stu-id="93256-188">purgedOn</span></span></p></td>
<td><p><span data-ttu-id="93256-189">datetime</span><span class="sxs-lookup"><span data-stu-id="93256-189">datetime</span></span></p></td>
<td><p><span data-ttu-id="93256-190">Zeitpunkt des letzten Aufräumvorgangs (Entfernen von Bereichen aus tblScopedPrincipal-Tabelle und Rollen aus der tblPrincipalRole-Tabelle), die diesen Knoten betroffen haben.</span><span class="sxs-lookup"><span data-stu-id="93256-190">Time of the latest purge operation (removal of scopes from tblScopedPrincipal table and roles from tblPrincipalRole table) that affected this node.</span></span> <span data-ttu-id="93256-191">Dieser wird vom internen Cache Aktualisierungsmechanismus des Chat Diensts verwendet.</span><span class="sxs-lookup"><span data-stu-id="93256-191">This is used by the Chat service’s internal cache update mechanism.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="93256-192">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="93256-192">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="93256-193">Spalte</span><span class="sxs-lookup"><span data-stu-id="93256-193">Column</span></span></th>
<th><span data-ttu-id="93256-194">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="93256-194">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="93256-195">nodeID</span><span class="sxs-lookup"><span data-stu-id="93256-195">nodeID</span></span></p></td>
<td><p><span data-ttu-id="93256-196">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="93256-196">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93256-197">Verhalten</span><span class="sxs-lookup"><span data-stu-id="93256-197">behavior</span></span></p></td>
<td><p><span data-ttu-id="93256-198">Fremdschlüssel mit Lookup in der Tabelle "tblEnumValue. Wert".</span><span class="sxs-lookup"><span data-stu-id="93256-198">Foreign key with lookup in tblEnumValue.valueID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93256-199">Sichtbarkeit</span><span class="sxs-lookup"><span data-stu-id="93256-199">visibility</span></span></p></td>
<td><p><span data-ttu-id="93256-200">Fremdschlüssel mit Lookup in der Tabelle "tblEnumValue. Wert".</span><span class="sxs-lookup"><span data-stu-id="93256-200">Foreign key with lookup in tblEnumValue.valueID table.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="93256-201">parentID</span><span class="sxs-lookup"><span data-stu-id="93256-201">parentID</span></span></p></td>
<td><p><span data-ttu-id="93256-202">Fremdschlüssel mit Lookup in der tblNode. Node-Tabelle</span><span class="sxs-lookup"><span data-stu-id="93256-202">Foreign key with lookup in tblNode.nodeID table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="93256-203">siopID</span><span class="sxs-lookup"><span data-stu-id="93256-203">siopID</span></span></p></td>
<td><p><span data-ttu-id="93256-204">Fremdschlüssel mit Lookup in der tblSiopWhiteList. siopId-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="93256-204">Foreign key with lookup in tblSiopWhiteList.siopId table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="93256-205">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="93256-205">


</div>

<span> </span>

</div>

</div>

</span></span></div>

