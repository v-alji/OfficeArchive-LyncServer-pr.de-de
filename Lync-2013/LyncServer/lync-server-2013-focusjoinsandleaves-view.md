---
title: 'Lync Server 2013: FocusJoinsAndLeaves-Ansicht'
description: 'Lync Server 2013: FocusJoinsAndLeaves-Ansicht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FocusJoinsAndLeaves view
ms:assetid: 226460ef-766f-4d61-80cb-f332b65a210d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687992(v=OCS.15)
ms:contentKeyID: 49733582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c6f68c44461e378e9ebedce1305ee6b384a7a8a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428108"
---
# <a name="focusjoinsandleaves-view-in-lync-server-2013"></a><span data-ttu-id="b5e1c-103">FocusJoinsAndLeaves-Ansicht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b5e1c-103">FocusJoinsAndLeaves view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b5e1c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b5e1c-104">

<span> </span></span></span>

<span data-ttu-id="b5e1c-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="b5e1c-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="b5e1c-106">In der FocusJoinsAndLeaves-Ansicht werden Informationen zu Join-und Leave-Informationen für eine Konferenz gespeichert.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-106">The FocusJoinsAndLeaves view stores information about join and leave information for one conference.</span></span> <span data-ttu-id="b5e1c-107">Jede Konferenz wird in dieser Ansicht durch einen Datensatz dargestellt, der jedes Mal geschrieben wird, wenn ein Benutzer eine Konferenz anschließt und verlässt.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-107">Each conference is represented in this view by a record written each time a user joins and leaves the conference.</span></span> <span data-ttu-id="b5e1c-108">Diese Ansicht wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b5e1c-109">Spalte</span><span class="sxs-lookup"><span data-stu-id="b5e1c-109">Column</span></span></th>
<th><span data-ttu-id="b5e1c-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b5e1c-110">Data Type</span></span></th>
<th><span data-ttu-id="b5e1c-111">Details</span><span class="sxs-lookup"><span data-stu-id="b5e1c-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b5e1c-112"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="b5e1c-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e1c-113">datetime</span><span class="sxs-lookup"><span data-stu-id="b5e1c-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="b5e1c-114">Uhrzeit der Konferenz Instanz.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-114">Time of conference instance.</span></span> <span data-ttu-id="b5e1c-115">Wird in Verbindung mit SessionIdSeq verwendet, um eine Konferenz Instanz eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-115">Used in conjunction with SessionIdSeq to uniquely identify a conference instance.</span></span> <span data-ttu-id="b5e1c-116">Weitere Informationen finden Sie <a href="lync-server-2013-conferences-table.md">in der Tabelle "Konferenzen" in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b5e1c-116">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e1c-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="b5e1c-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e1c-118">int</span><span class="sxs-lookup"><span data-stu-id="b5e1c-118">int</span></span></p></td>
<td><p><span data-ttu-id="b5e1c-119">Die ID-Nummer zum Identifizieren der Konferenz Instanz.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-119">ID number to identify the conference instance.</span></span> <span data-ttu-id="b5e1c-120">Wird in Verbindung mit SessionID-Mal verwendet, um eine Konferenz Instanz eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-120">Used in conjunction with SessionIdTime to uniquely identify a conference instance.</span></span> <span data-ttu-id="b5e1c-121">Weitere Informationen finden Sie <a href="lync-server-2013-conferences-table.md">in der Tabelle "Konferenzen" in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b5e1c-121">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e1c-122"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="b5e1c-122"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e1c-123">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="b5e1c-123">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="b5e1c-124">Der URI des Benutzers, dessen Konferenz beitreten/Leave-Informationen erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-124">URI of the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e1c-125"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="b5e1c-125"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e1c-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b5e1c-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b5e1c-127">Der Typ des URIs des Benutzers, dessen Konferenz beitreten/Leave-Informationen erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-127">Type of URI of the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="b5e1c-128">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b5e1c-128">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e1c-129"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="b5e1c-129"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e1c-130">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b5e1c-130">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b5e1c-131">Der Mandant des Benutzers, dessen Konferenz beitreten/Leave-Informationen erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-131">Tenant of the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="b5e1c-132">Weitere Informationen finden Sie <a href="lync-server-2013-tenants-table.md">in der Tabelle Mandanten in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b5e1c-132">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e1c-133"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="b5e1c-133"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e1c-134">uniqueidentifier</span><span class="sxs-lookup"><span data-stu-id="b5e1c-134">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="b5e1c-135">Eindeutiger Bezeichner des Benutzers, dessen Konferenz beitreten/Leave-Informationen erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-135">Unique identifier of the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e1c-136"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="b5e1c-136"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e1c-137">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b5e1c-137">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b5e1c-138">Die Version des Clients, die von dem Benutzer verwendet wurde, dessen Konferenz beitreten/Leave-Informationen erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-138">Version of client used by the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e1c-139"><strong>UserClientType</strong></span><span class="sxs-lookup"><span data-stu-id="b5e1c-139"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e1c-140">int</span><span class="sxs-lookup"><span data-stu-id="b5e1c-140">int</span></span></p></td>
<td><p><span data-ttu-id="b5e1c-141">Der Client, der von dem Benutzer verwendet wird, dessen Konferenz beitreten/Leave-Informationen erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-141">Client used by the user whose conference join/leave information was captured.</span></span> <span data-ttu-id="b5e1c-142">Weitere Informationen finden Sie unter <a href="lync-server-2013-useragentdef-table.md">UserAgentDef-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b5e1c-142">See <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e1c-143"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="b5e1c-143"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e1c-144">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="b5e1c-144">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="b5e1c-145">Name der Kategorie des Clients, die von dem Benutzer verwendet wird, dessen Konferenz teilnehmen/-Abwesenheitsinformationen erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-145">Name of the category of the client used by the user whose conference join/leave information was captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e1c-146"><strong>FocusUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="b5e1c-146"><strong>FocusUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e1c-147">int</span><span class="sxs-lookup"><span data-stu-id="b5e1c-147">int</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e1c-148"><strong>IsuserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="b5e1c-148"><strong>IsuserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e1c-149">bit</span><span class="sxs-lookup"><span data-stu-id="b5e1c-149">bit</span></span></p></td>
<td><p><span data-ttu-id="b5e1c-150">Bit, das darstellt, ob der Benutzer ein interner Benutzer ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-150">Bit that represents whether the user is an internal user or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e1c-151"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="b5e1c-151"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e1c-152">datetime</span><span class="sxs-lookup"><span data-stu-id="b5e1c-152">datetime</span></span></p></td>
<td><p><span data-ttu-id="b5e1c-153">Uhrzeit der Sitzungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-153">Time of session request.</span></span> <span data-ttu-id="b5e1c-154">Wird in Verbindung mit SessionIdSeq verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-154">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="b5e1c-155">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b5e1c-155">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e1c-156"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="b5e1c-156"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e1c-157">int</span><span class="sxs-lookup"><span data-stu-id="b5e1c-157">int</span></span></p></td>
<td><p><span data-ttu-id="b5e1c-158">Wenn ein Benutzer gleichzeitig an mehreren Computern oder Geräten angemeldet ist, wird UserInstance verwendet, um die Kombination aus Benutzer und Gerät eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-158">If a user is logged on at multiple computers or devices at the same time, UserInstance is used to uniquely identify the user/device combination.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e1c-159"><strong>Dialogfeld-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="b5e1c-159"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e1c-160">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="b5e1c-160">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="b5e1c-161">SIP-Dialogfeld-ID der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-161">SIP dialog ID of the session.</span></span> <span data-ttu-id="b5e1c-162">Das Format lautet: Dialogfeld; from-Tag; to-Tag.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-162">The format is: dialog;from-tag;to-tag.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e1c-163"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="b5e1c-163"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e1c-164">datetime</span><span class="sxs-lookup"><span data-stu-id="b5e1c-164">datetime</span></span></p></td>
<td><p><span data-ttu-id="b5e1c-165">Uhrzeit, zu der der Benutzer der Konferenz beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-165">Time that the user joined the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b5e1c-166"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="b5e1c-166"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e1c-167">datetime</span><span class="sxs-lookup"><span data-stu-id="b5e1c-167">datetime</span></span></p></td>
<td><p><span data-ttu-id="b5e1c-168">Der Zeitpunkt, zu dem der Benutzer die Konferenz verlassen hat.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-168">Time that the user left the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b5e1c-169"><strong>UserRole</strong></span><span class="sxs-lookup"><span data-stu-id="b5e1c-169"><strong>UserRole</strong></span></span></p></td>
<td><p><span data-ttu-id="b5e1c-170">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b5e1c-170">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b5e1c-171">Rolle des Benutzers in der Konferenz, beispielsweise Referent oder Teilnehmer.</span><span class="sxs-lookup"><span data-stu-id="b5e1c-171">User’s role in the conference, such as Presenter or Attendee.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b5e1c-172">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b5e1c-172">


</div>

<span> </span>

</div>

</div>

</span></span></div>

