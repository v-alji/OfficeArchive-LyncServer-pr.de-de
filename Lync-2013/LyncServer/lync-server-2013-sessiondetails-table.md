---
title: 'Lync Server 2013: SessionDetails-Tabelle'
description: 'Lync Server 2013: SessionDetails-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionDetails table
ms:assetid: 783d2508-e31f-4b54-be0c-63aa5ec21c04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398589(v=OCS.15)
ms:contentKeyID: 48184559
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd927f784fb0f2a835c896824105fe8bb112c7a1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444777"
---
# <a name="sessiondetails-table-in-lync-server-2013"></a><span data-ttu-id="e7b1d-103">SessionDetails-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e7b1d-103">SessionDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e7b1d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e7b1d-104">

<span> </span></span></span>

<span data-ttu-id="e7b1d-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="e7b1d-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="e7b1d-106">Jeder Datensatz stellt eine Peer-to-Peer-Sitzung dar, bei der es sich um einen VoIP-VoIP Telefonanruf, eine Chatsitzung mit zwei Teilnehmern oder eine andere Art von Sitzung handeln kann.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-106">Each record represents one peer-to-peer session, which could be a VoIP-VoIP phone call, two-party IM session, or other type of session.</span></span> <span data-ttu-id="e7b1d-107">Sie können eine Tabellen Verknüpfung mit der [Medientabelle in lync Server 2013](lync-server-2013-media-table.md) ausführen, um die Details der einzelnen Medien zu finden, die an dieser Sitzung beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-107">You can perform a table join with the [Media table in Lync Server 2013](lync-server-2013-media-table.md) to find the details of each media involved in this session.</span></span>

<span data-ttu-id="e7b1d-108">Beachten Sie, dass die IsUser1IntegratedWithDeskPhone-und IsUser2IntegratedWithDeskPhone-Felder aus der SessionDetails-Tabelle gelöscht wurden, die in Microsoft lync Server 2013 verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-108">Note that the IsUser1IntegratedWithDeskPhone and the IsUser2IntegratedWithDeskPhone fields have been dropped from the SessionDetails table used in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7b1d-109">Spalte</span><span class="sxs-lookup"><span data-stu-id="e7b1d-109">Column</span></span></th>
<th><span data-ttu-id="e7b1d-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e7b1d-110">Data Type</span></span></th>
<th><span data-ttu-id="e7b1d-111">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="e7b1d-111">Key/Index</span></span></th>
<th><span data-ttu-id="e7b1d-112">Details</span><span class="sxs-lookup"><span data-stu-id="e7b1d-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-113"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-113"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-114">datetime</span><span class="sxs-lookup"><span data-stu-id="e7b1d-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-115">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="e7b1d-115">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-116">Uhrzeit der Sitzungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-116">Time of session request.</span></span> <span data-ttu-id="e7b1d-117">Wird in Verbindung mit <strong>SessionIdSeq</strong> verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-117">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="e7b1d-118">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7b1d-118">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-119"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-119"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-120">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-120">int</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-121">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="e7b1d-121">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-122">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-122">ID number to identify the session.</span></span> <span data-ttu-id="e7b1d-123">Wird in Verbindung mit <strong>SessionID</strong> -Mal verwendet, um eine Sitzung eindeutig zu identifizieren. \* Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7b1d-123">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.\* See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-124"><strong>CorrelationId</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-124"><strong>CorrelationId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-125">uniqueidentifier</span><span class="sxs-lookup"><span data-stu-id="e7b1d-125">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7b1d-126">Eine GUID zum Korrelieren mehrerer Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-126">A GUID to correlate multiple sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-127"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-127"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-128">datetime</span><span class="sxs-lookup"><span data-stu-id="e7b1d-128">datetime</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-129">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7b1d-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-130">Die ID-Nummer, die das Dialogfeld identifiziert, das durch die aktuelle Sitzung ersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-130">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="e7b1d-131">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7b1d-131">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-132"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-132"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-133">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-133">int</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-134">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7b1d-134">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-135">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-135">ID number to identify the session.</span></span> <span data-ttu-id="e7b1d-136">Wird in Verbindung mit <strong>ReplacesDialogIdTime</strong> verwendet, um eine Sitzung, die durch diese Sitzung ersetzt wird, eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-136">Used in conjunction with <strong>ReplacesDialogIdTime</strong> to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="e7b1d-137">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7b1d-137">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-138"><strong>Benutzer1</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-138"><strong>User1Id</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-139">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-139">int</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-140">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7b1d-140">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-141">Die ID eines Benutzers in der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-141">ID of one user in the session.</span></span> <span data-ttu-id="e7b1d-142">Weitere Informationen finden Sie <a href="lync-server-2013-users-table.md">in der Tabelle Benutzer in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7b1d-142">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-143"><strong>User2Id</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-143"><strong>User2Id</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-144">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-144">int</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-145">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7b1d-145">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-146">Die ID des anderen Benutzers in der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-146">ID of the other user in the session.</span></span> <span data-ttu-id="e7b1d-147">Weitere Informationen finden Sie <a href="lync-server-2013-users-table.md">in der Tabelle Benutzer in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7b1d-147">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-148"><strong>User1EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-148"><strong>User1EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-149">uniqueIdentifier</span><span class="sxs-lookup"><span data-stu-id="e7b1d-149">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7b1d-150">GUID, die den vom ersten Benutzer in der Sitzung verwendeten Endpunkt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-150">GUID that identifies the endpoint used by the first user in the session.</span></span></p>
<p><span data-ttu-id="e7b1d-151">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-151">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-152"><strong>User2EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-152"><strong>User2EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-153">uniqueIdentifier</span><span class="sxs-lookup"><span data-stu-id="e7b1d-153">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7b1d-154">GUID, die den vom zweiten Benutzer in der Sitzung verwendeten Endpunkt identifiziert.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-154">GUID that identifies the endpoint used by the second user in the session.</span></span></p>
<p><span data-ttu-id="e7b1d-155">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-156"><strong>TargetUserId</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-156"><strong>TargetUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-157">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-157">int</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-158">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7b1d-158">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-159">Das Original für Benutzer-URI in der SIP-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-159">The original To user URI in the SIP request.</span></span> <span data-ttu-id="e7b1d-160">Weitere Informationen finden Sie <a href="lync-server-2013-users-table.md">in der Tabelle Benutzer in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7b1d-160">see the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-161"><strong>SessionStartedById</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-161"><strong>SessionStartedById</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-162">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-162">int</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-163">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7b1d-163">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-164">Die ID des Benutzers, der die Sitzung gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-164">ID of the user who started the session.</span></span> <span data-ttu-id="e7b1d-165">Weitere Informationen finden Sie <a href="lync-server-2013-users-table.md">in der Tabelle Benutzer in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7b1d-165">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-166"><strong>OnBehalfOfId</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-166"><strong>OnBehalfOfId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-167">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-167">int</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-168">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7b1d-168">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-169">Gibt die ID des Benutzers an, der der Anrufer im Auftrag ist.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-169">Indicates the ID of the user of who the caller is on behalf.</span></span> <span data-ttu-id="e7b1d-170">Weitere Informationen finden Sie <a href="lync-server-2013-users-table.md">in der Tabelle Benutzer in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7b1d-170">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-171"><strong>ReferredById</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-171"><strong>ReferredById</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-172">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-172">int</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-173">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7b1d-173">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-174">Die ID des Benutzers, auf den der Anruf verweist.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-174">ID of the user by who the call is referred.</span></span> <span data-ttu-id="e7b1d-175">Weitere Informationen finden Sie <a href="lync-server-2013-users-table.md">in der Tabelle Benutzer in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7b1d-175">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-176"><strong>ServerID</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-176"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-177">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-177">int</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-178">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7b1d-178">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-179">Die ID des für diese Sitzung verwendeten Front-End-Servers.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-179">ID of the front-end server used for this session.</span></span> <span data-ttu-id="e7b1d-180">Weitere Informationen finden Sie <a href="lync-server-2013-servers-table.md">in der Tabelle Server in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7b1d-180">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-181"><strong>Pool-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-181"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-182">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-182">int</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-183">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7b1d-183">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-184">Die ID des Pools, in dem die Sitzung erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-184">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="e7b1d-185">Weitere Informationen finden Sie <a href="lync-server-2013-pools-table.md">in der Tabelle Pools in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7b1d-185">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-186"><strong>ContentTypeID</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-186"><strong>ContentTypeID</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-187">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-187">int</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-188">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7b1d-188">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-189">Inhaltstyp, der in der Sitzung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-189">Content type used in the session.</span></span> <span data-ttu-id="e7b1d-190">Weitere Informationen finden Sie <a href="lync-server-2013-contenttypes-table.md">in der Tabelle "ContentTypes" in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7b1d-190">See the <a href="lync-server-2013-contenttypes-table.md">ContentTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-191"><strong>User1ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-191"><strong>User1ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-192">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-192">int</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-193">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7b1d-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-194">Von Benutzer1 verwendete Client Version.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-194">Client version used by User1.</span></span> <span data-ttu-id="e7b1d-195">Weitere Informationen finden Sie <a href="lync-server-2013-clientversions-table.md">in der ClientVersions-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7b1d-195">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-196"><strong>User2ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-196"><strong>User2ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-197">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-197">int</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-198">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7b1d-198">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-199">Von User2 verwendete Client Version.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-199">Client version used by User2.</span></span> <span data-ttu-id="e7b1d-200">Weitere Informationen finden Sie <a href="lync-server-2013-clientversions-table.md">in der ClientVersions-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7b1d-200">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-201"><strong>User1EdgeServerid</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-201"><strong>User1EdgeServerid</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-202">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-202">int</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-203">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7b1d-203">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-204">Von Benutzer1 verwendeter Edgeserver</span><span class="sxs-lookup"><span data-stu-id="e7b1d-204">Edge Server used by User1.</span></span> <span data-ttu-id="e7b1d-205">Weitere Informationen finden Sie <a href="lync-server-2013-edgeservers-table.md">in der EdgeServers-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7b1d-205">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-206"><strong>User2EdgeServerid</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-206"><strong>User2EdgeServerid</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-207">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-207">int</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-208">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7b1d-208">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-209">Von User2 verwendeter Edgeserver.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-209">Edge Server used by User2.</span></span> <span data-ttu-id="e7b1d-210">Weitere Informationen finden Sie <a href="lync-server-2013-edgeservers-table.md">in der EdgeServers-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7b1d-210">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-211"><strong>IsUser1Internal</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-211"><strong>IsUser1Internal</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-212">bit</span><span class="sxs-lookup"><span data-stu-id="e7b1d-212">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7b1d-213">Gibt an, ob Benutzer1 intern angemeldet ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-213">Whether User1 is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-214"><strong>IsUser2Internal</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-214"><strong>IsUser2Internal</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-215">bit</span><span class="sxs-lookup"><span data-stu-id="e7b1d-215">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7b1d-216">Gibt an, ob User2 intern angemeldet ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-216">Whether User2 is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-217"><strong>Einladen</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-217"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-218">datetime</span><span class="sxs-lookup"><span data-stu-id="e7b1d-218">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7b1d-219">Der Zeitpunkt der ersten INVITE-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-219">The time of the first INVITE request.</span></span> <span data-ttu-id="e7b1d-220">Dieses Feld wird in der Regel von Daten ausgefüllt, die aus der anfänglichen Einladungsnachricht in der Sitzung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-220">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="e7b1d-221">Wenn keine Einladungsnachricht vorhanden ist, wird das Feld mit dem Datum und der Uhrzeit der ersten relevanten SIP-Nachricht gefüllt (Bye, Cancel, Nachricht oder info).</span><span class="sxs-lookup"><span data-stu-id="e7b1d-221">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span> <span data-ttu-id="e7b1d-222">Dieses Feld wird in der Regel von Daten ausgefüllt, die aus der anfänglichen Einladungsnachricht in der Sitzung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-222">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="e7b1d-223">Wenn keine Einladungsnachricht vorhanden ist, wird das Feld mit dem Datum und der Uhrzeit der ersten relevanten SIP-Nachricht gefüllt (Bye, Cancel, Nachricht oder info).</span><span class="sxs-lookup"><span data-stu-id="e7b1d-223">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-224"><strong>Webantworten</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-224"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-225">datetime</span><span class="sxs-lookup"><span data-stu-id="e7b1d-225">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7b1d-226">Der Zeitpunkt der Antwort auf die erste Einladungsnachricht.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-226">The time of the response to the first INVITE message.</span></span> <span data-ttu-id="e7b1d-227">Dieses Feld wird in der Regel von Daten ausgefüllt, die aus der anfänglichen Einladungsnachricht in der Sitzung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-227">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="e7b1d-228">Wenn keine Einladungsnachricht vorhanden ist, wird das Feld mit dem Datum und der Uhrzeit der ersten relevanten SIP-Nachricht gefüllt (Bye, Cancel, Nachricht oder info).</span><span class="sxs-lookup"><span data-stu-id="e7b1d-228">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-229"><strong>Response Code</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-229"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-230">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-230">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7b1d-231">SIP-Antwortcode für die Sitzungseinladung</span><span class="sxs-lookup"><span data-stu-id="e7b1d-231">SIP response code to the session invitation.</span></span> <span data-ttu-id="e7b1d-232">Dieses Feld wird in der Regel von Daten ausgefüllt, die aus der anfänglichen Einladungsnachricht in der Sitzung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-232">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="e7b1d-233">Wenn keine Einladungsnachricht vorhanden ist, wird das Feld mit dem Datum und der Uhrzeit der ersten relevanten SIP-Nachricht gefüllt (Bye, Cancel, Nachricht oder info).</span><span class="sxs-lookup"><span data-stu-id="e7b1d-233">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-234"><strong>Diagnose-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-234"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-235">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-235">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7b1d-236">Vom SIP-Header erfasste Diagnose-ID.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-236">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-237"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-237"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-238">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-238">int</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-239">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7b1d-239">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-240">Anrufpriorität.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-240">Call priority.</span></span> <span data-ttu-id="e7b1d-241">Weitere Informationen finden Sie <a href="lync-server-2013-callpriorities-table.md">in der CallPriorities-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7b1d-241">See the <a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-242"><strong>User1MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-242"><strong>User1MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-243">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-243">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7b1d-244">Die Anzahl der Nachrichten, die von Benutzer1 während der Sitzung gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-244">Number of messages sent by User1 during the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-245"><strong>User2MessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-245"><strong>User2MessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-246">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-246">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7b1d-247">Die Anzahl der Nachrichten, die von User2 während der Sitzung gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-247">Number of messages sent by User2 during the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-248"><strong>SessionEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-248"><strong>SessionEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-249">datetime</span><span class="sxs-lookup"><span data-stu-id="e7b1d-249">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7b1d-250">Uhrzeit am Ende der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-250">Time at the end of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-251"><strong>MediaTypes</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-251"><strong>MediaTypes</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-252">int</span><span class="sxs-lookup"><span data-stu-id="e7b1d-252">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7b1d-253">Ein Bit-Satz, der den Medientyp dieser Sitzung angibt.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-253">A bit set that indicates the media type of this session.</span></span> <span data-ttu-id="e7b1d-254">Aufgelistet sind die Definitionen der Typen:</span><span class="sxs-lookup"><span data-stu-id="e7b1d-254">Listed are the definitions of the types:</span></span></p>
<h3 id="section-1"> </h3>
<div>
<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-255">Chat</span><span class="sxs-lookup"><span data-stu-id="e7b1d-255">IM</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-256">1</span><span class="sxs-lookup"><span data-stu-id="e7b1d-256">1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-257">FILE_TRANSFER</span><span class="sxs-lookup"><span data-stu-id="e7b1d-257">FILE_TRANSFER</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-258">2</span><span class="sxs-lookup"><span data-stu-id="e7b1d-258">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-259">REMOTE_ASSISTANCE</span><span class="sxs-lookup"><span data-stu-id="e7b1d-259">REMOTE_ASSISTANCE</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-260">4</span><span class="sxs-lookup"><span data-stu-id="e7b1d-260">4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-261">APP_SHARING</span><span class="sxs-lookup"><span data-stu-id="e7b1d-261">APP_SHARING</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-262">8</span><span class="sxs-lookup"><span data-stu-id="e7b1d-262">8</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-263">Audio</span><span class="sxs-lookup"><span data-stu-id="e7b1d-263">AUDIO</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-264">16</span><span class="sxs-lookup"><span data-stu-id="e7b1d-264">16</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-265">Video</span><span class="sxs-lookup"><span data-stu-id="e7b1d-265">VIDEO</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-266">32</span><span class="sxs-lookup"><span data-stu-id="e7b1d-266">32</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-267">APP_INVITE</span><span class="sxs-lookup"><span data-stu-id="e7b1d-267">APP_INVITE</span></span></p></td>
<td><p><span data-ttu-id="e7b1d-268">64</span><span class="sxs-lookup"><span data-stu-id="e7b1d-268">64</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-269"><strong>User1Flag</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-269"><strong>User1Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-270">smallint</span><span class="sxs-lookup"><span data-stu-id="e7b1d-270">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7b1d-271">Ein Bit-Satz, der die Benutzer1-Attribute angibt.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-271">A bit set that indicates the User1 attributes.</span></span> <span data-ttu-id="e7b1d-272">Die folgenden Attributdefinitionen werden aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="e7b1d-272">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="e7b1d-273">0x01-integriert mit dem Desktoptelefon</span><span class="sxs-lookup"><span data-stu-id="e7b1d-273">0x01 - Integrated with desktop phone</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-274"><strong>User2Flag</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-274"><strong>User2Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-275">smallint</span><span class="sxs-lookup"><span data-stu-id="e7b1d-275">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7b1d-276">Ein Bit-Satz, der die User2-Attribute angibt.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-276">A bit set that indicates the User2 attributes.</span></span> <span data-ttu-id="e7b1d-277">Die folgenden Attributdefinitionen werden aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="e7b1d-277">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="e7b1d-278">0x01-integriert mit dem Desktoptelefon</span><span class="sxs-lookup"><span data-stu-id="e7b1d-278">0x01 - Integrated with desktop phone</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7b1d-279"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-279"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-280">smallint</span><span class="sxs-lookup"><span data-stu-id="e7b1d-280">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7b1d-281">Ein Bit-Satz, der die anrufattribute angibt.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-281">A bit set that indicates the call attributes.</span></span> <span data-ttu-id="e7b1d-282">Die folgenden Attributdefinitionen werden aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="e7b1d-282">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="e7b1d-283">0x01-wiederholte Sitzung</span><span class="sxs-lookup"><span data-stu-id="e7b1d-283">0x01 - Retried Session</span></span></p></li>
<li><p><span data-ttu-id="e7b1d-284">0x02 – ein Anruf, der von einem Agenten im Auftrag einer Reaktionsgruppe durchgeführt wurde</span><span class="sxs-lookup"><span data-stu-id="e7b1d-284">0x02 - A call made by agent on behalf of a response group</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7b1d-285"><strong>Verarbeitet</strong></span><span class="sxs-lookup"><span data-stu-id="e7b1d-285"><strong>Processed</strong></span></span></p></td>
<td><p><span data-ttu-id="e7b1d-286">bit</span><span class="sxs-lookup"><span data-stu-id="e7b1d-286">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7b1d-287">Für die interne Verwendung durch den Überwachungsdienst.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-287">For internal use by the Monitoring service.</span></span></p>
<p><span data-ttu-id="e7b1d-288">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-288">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="e7b1d-289">\* Bei den meisten Sitzungen erhält SessionIdSeq den Wert 1.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-289">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="e7b1d-290">Wenn mehrere Sitzungen genau zur gleichen Zeit beginnen, ist der SessionIdSeq für einen 1, für einen anderen wird 2 usw.</span><span class="sxs-lookup"><span data-stu-id="e7b1d-290">If multiple sessions start at exactly the same time, the SessionIdSeq for one will be 1, for another will be 2, and so on.</span></span>

<span data-ttu-id="e7b1d-291"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e7b1d-291"></div>

<span> </span>

</div>

</div>

</span></span></div>

