---
title: 'Lync Server 2013: McuJoinsAndLeaves-Ansicht'
description: 'Lync Server 2013: McuJoinsAndLeaves-Ansicht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: McuJoinsAndLeaves view
ms:assetid: 6f00b8e7-b8b6-4657-ac5e-d8a571806ae2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688088(v=OCS.15)
ms:contentKeyID: 49733687
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f7f2f51c340d5bd4824a6e8eff1a0da172a758c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425731"
---
# <a name="mcujoinsandleaves-view-in-lync-server-2013"></a><span data-ttu-id="bdb55-103">McuJoinsAndLeaves-Ansicht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bdb55-103">McuJoinsAndLeaves view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bdb55-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bdb55-104">

<span> </span></span></span>

<span data-ttu-id="bdb55-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="bdb55-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="bdb55-106">Die McuJoinsAndLeaves-Ansicht speichert Informationen zu Benutzern, die an einem Konferenzserver teilnehmen und Informationen hinterlassen.</span><span class="sxs-lookup"><span data-stu-id="bdb55-106">The McuJoinsAndLeaves view stores information about users join and leave information for one conference server.</span></span> <span data-ttu-id="bdb55-107">Jeder Datensatz in dieser Ansicht enthält Anrufdetails zu einer Kombination aus einem Benutzer-Join oder Leave-und Konferenzserver.</span><span class="sxs-lookup"><span data-stu-id="bdb55-107">Each record in this view contains call details about one combination of a user join or leave and conferencing server.</span></span> <span data-ttu-id="bdb55-108">Diese Ansicht wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bdb55-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bdb55-109">Spalte</span><span class="sxs-lookup"><span data-stu-id="bdb55-109">Column</span></span></th>
<th><span data-ttu-id="bdb55-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bdb55-110">Data Type</span></span></th>
<th><span data-ttu-id="bdb55-111">Details</span><span class="sxs-lookup"><span data-stu-id="bdb55-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bdb55-112"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="bdb55-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="bdb55-113">datetime</span><span class="sxs-lookup"><span data-stu-id="bdb55-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="bdb55-114">Uhrzeit der Konferenz Instanz.</span><span class="sxs-lookup"><span data-stu-id="bdb55-114">Time of conference instance.</span></span> <span data-ttu-id="bdb55-115">Wird in Verbindung mit SessionIdSeq verwendet, um eine Konferenz Instanz eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bdb55-115">Used in conjunction with SessionIdSeq to uniquely identify a conference instance.</span></span> <span data-ttu-id="bdb55-116">Weitere Informationen finden Sie <a href="lync-server-2013-conferences-table.md">in der Tabelle "Konferenzen" in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="bdb55-116">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdb55-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="bdb55-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="bdb55-118">int</span><span class="sxs-lookup"><span data-stu-id="bdb55-118">int</span></span></p></td>
<td><p><span data-ttu-id="bdb55-119">Die ID-Nummer zum Identifizieren der Konferenz Instanz.</span><span class="sxs-lookup"><span data-stu-id="bdb55-119">ID number to identify the conference instance.</span></span> <span data-ttu-id="bdb55-120">Wird in Verbindung mit SessionID-Mal verwendet, um eine Konferenz Instanz eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bdb55-120">Used in conjunction with SessionIdTime to uniquely identify a conference instance.</span></span> <span data-ttu-id="bdb55-121">Weitere Informationen finden Sie <a href="lync-server-2013-conferences-table.md">in der Tabelle "Konferenzen" in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="bdb55-121">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdb55-122"><strong>McuUri</strong></span><span class="sxs-lookup"><span data-stu-id="bdb55-122"><strong>McuUri</strong></span></span></p></td>
<td><p><span data-ttu-id="bdb55-123">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="bdb55-123">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="bdb55-124">Der URI des Konferenzservers, mit dem der Benutzer eine Verbindung hergestellt hat.</span><span class="sxs-lookup"><span data-stu-id="bdb55-124">The URI of the conferencing server that the user connected to.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdb55-125"><strong>McuUriType</strong></span><span class="sxs-lookup"><span data-stu-id="bdb55-125"><strong>McuUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="bdb55-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="bdb55-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="bdb55-127">Der URI des Konferenzservers, mit dem der Benutzer eine Verbindung hergestellt hat.</span><span class="sxs-lookup"><span data-stu-id="bdb55-127">The URI of the conferencing server that the user connected to.</span></span> <span data-ttu-id="bdb55-128">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="bdb55-128">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdb55-129"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="bdb55-129"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="bdb55-130">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="bdb55-130">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="bdb55-131">Der URI des Benutzers, dessen Konferenzserver teilnehmen/Leave-Informationen erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="bdb55-131">The URI of the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdb55-132"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="bdb55-132"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="bdb55-133">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="bdb55-133">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="bdb55-134">Der Typ des URIs des Benutzers, dessen Konferenzserver teilnehmen/Leave-Informationen erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="bdb55-134">The type of URI of the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="bdb55-135">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="bdb55-135">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdb55-136"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="bdb55-136"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="bdb55-137">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="bdb55-137">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="bdb55-138">Der Mandant des Benutzers, dessen Konferenzserver teilnehmen/Leave-Informationen erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="bdb55-138">The tenant of the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="bdb55-139">Weitere Informationen finden Sie <a href="lync-server-2013-tenants-table.md">in der Tabelle Mandanten in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="bdb55-139">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdb55-140"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="bdb55-140"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="bdb55-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="bdb55-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="bdb55-142">Die Version des Clients, die von dem Benutzer verwendet wird, dessen Konferenzserver-Informationen aufgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="bdb55-142">The version of client used by the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdb55-143"><strong>UserClientType</strong></span><span class="sxs-lookup"><span data-stu-id="bdb55-143"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="bdb55-144">int</span><span class="sxs-lookup"><span data-stu-id="bdb55-144">int</span></span></p></td>
<td><p><span data-ttu-id="bdb55-145">Der Client, der von dem Benutzer verwendet wird, dessen Konferenzserver an-und Abgangs Informationen erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="bdb55-145">The client used by the user whose conferencing server join/leave information was captured.</span></span> <span data-ttu-id="bdb55-146">Weitere Informationen finden Sie <a href="lync-server-2013-useragentdef-table.md">in der UserAgentDef-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="bdb55-146">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdb55-147"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="bdb55-147"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="bdb55-148">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="bdb55-148">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="bdb55-149">Der Name der Kategorie des Clients, die von dem Benutzer verwendet wird, dessen Konferenzserver-Informationen aufgenommen wurden.</span><span class="sxs-lookup"><span data-stu-id="bdb55-149">The name of the category of the client used by the user whose conferencing server join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdb55-150"><strong>McuUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="bdb55-150"><strong>McuUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="bdb55-151">int</span><span class="sxs-lookup"><span data-stu-id="bdb55-151">int</span></span></p></td>
<td><p><span data-ttu-id="bdb55-152">Kennzeichnet die Kombination von Benutzern/Geräten für Benutzer, die gleichzeitig an mehreren Geräten angemeldet sind.</span><span class="sxs-lookup"><span data-stu-id="bdb55-152">Uniquely identifies the user/device combination for users simultaneously logged on to multiple devices.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdb55-153"><strong>IsUserFromPstn</strong></span><span class="sxs-lookup"><span data-stu-id="bdb55-153"><strong>IsUserFromPstn</strong></span></span></p></td>
<td><p><span data-ttu-id="bdb55-154">bit</span><span class="sxs-lookup"><span data-stu-id="bdb55-154">bit</span></span></p></td>
<td><p><span data-ttu-id="bdb55-155">Bit, das darstellt, ob der Benutzer ein interner Benutzer ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="bdb55-155">Bit that represents whether the user is an internal user or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdb55-156"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="bdb55-156"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="bdb55-157">datetime</span><span class="sxs-lookup"><span data-stu-id="bdb55-157">datetime</span></span></p></td>
<td><p><span data-ttu-id="bdb55-158">Uhrzeit der Sitzungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="bdb55-158">Time of session request.</span></span> <span data-ttu-id="bdb55-159">Wird in Verbindung mit SessionIdSeq verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bdb55-159">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="bdb55-160">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="bdb55-160">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdb55-161"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="bdb55-161"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="bdb55-162">int</span><span class="sxs-lookup"><span data-stu-id="bdb55-162">int</span></span></p></td>
<td><p><span data-ttu-id="bdb55-163">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bdb55-163">ID number to identify the session.</span></span> <span data-ttu-id="bdb55-164">Wird in Verbindung mit SessionID-Mal verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bdb55-164">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="bdb55-165">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="bdb55-165">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdb55-166"><strong>Dialogfeld-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="bdb55-166"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="bdb55-167">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="bdb55-167">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="bdb55-168">SIP-Dialogfeld-ID der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="bdb55-168">SIP dialog ID of the session.</span></span> <span data-ttu-id="bdb55-169">Das Format lautet: Dialogfeld; from-Tag; to-Tag.</span><span class="sxs-lookup"><span data-stu-id="bdb55-169">The format is: dialog;from-tag;to-tag.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bdb55-170"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="bdb55-170"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="bdb55-171">datetime</span><span class="sxs-lookup"><span data-stu-id="bdb55-171">datetime</span></span></p></td>
<td><p><span data-ttu-id="bdb55-172">Zeitpunkt, zu dem der Benutzer dem Konferenzserver beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="bdb55-172">Time the user joined the conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bdb55-173"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="bdb55-173"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="bdb55-174">datetime</span><span class="sxs-lookup"><span data-stu-id="bdb55-174">datetime</span></span></p></td>
<td><p><span data-ttu-id="bdb55-175">Zeitpunkt, zu dem der Benutzer den Konferenzserver verlassen hat.</span><span class="sxs-lookup"><span data-stu-id="bdb55-175">Time the user left the conferencing server.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="bdb55-176">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bdb55-176">


</div>

<span> </span>

</div>

</div>

</span></span></div>

