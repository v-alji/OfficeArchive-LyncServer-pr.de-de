---
title: 'Lync Server 2013: SessionDetails-Ansicht'
description: 'Lync Server 2013: SessionDetails-Ansicht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SessionDetails view
ms:assetid: ea328c6f-cf22-48dd-8f7f-f1666c9148c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721924(v=OCS.15)
ms:contentKeyID: 49733859
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c9f657257e54389defb805919be61adbdecad74
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424030"
---
# <a name="sessiondetails-view-in-lync-server-2013"></a><span data-ttu-id="d46ba-103">SessionDetails-Ansicht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d46ba-103">SessionDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d46ba-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d46ba-104">

<span> </span></span></span>

<span data-ttu-id="d46ba-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="d46ba-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="d46ba-106">In der SessionDetails-Ansicht werden Informationen zu Peer-to-Peer-Sitzungen gespeichert, bei denen es sich um einen VoIP-VoIP Telefonanruf, eine Chatsitzung mit zwei Teilnehmern oder eine andere Art von Sitzung handeln kann.</span><span class="sxs-lookup"><span data-stu-id="d46ba-106">The SessionDetails view stores information about peer-to-peer sessions, which could be a VoIP-VoIP phone call, two-party IM session, or other type of session.</span></span> <span data-ttu-id="d46ba-107">Diese Ansicht wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d46ba-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d46ba-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="d46ba-108">Column</span></span></th>
<th><span data-ttu-id="d46ba-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="d46ba-109">Data Type</span></span></th>
<th><span data-ttu-id="d46ba-110">Details</span><span class="sxs-lookup"><span data-stu-id="d46ba-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-111"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-112">datetime</span><span class="sxs-lookup"><span data-stu-id="d46ba-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="d46ba-113">Uhrzeit der Sitzungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="d46ba-113">Time of session request.</span></span> <span data-ttu-id="d46ba-114">Wird in Verbindung mit SessionIdSeq verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d46ba-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="d46ba-115">Weitere Informationen finden Sie in der Tabelle <a href="lync-server-2013-dialogs-table.md">Dialogfelder in der lync Server 2013</a> -Tabelle.</span><span class="sxs-lookup"><span data-stu-id="d46ba-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> Table for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-117">int</span><span class="sxs-lookup"><span data-stu-id="d46ba-117">int</span></span></p></td>
<td><p><span data-ttu-id="d46ba-118">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d46ba-118">ID number to identify the session.</span></span> <span data-ttu-id="d46ba-119">Wird in Verbindung mit SessionID-Mal verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d46ba-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="d46ba-120">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d46ba-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-121"><strong>Einladen</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-121"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-122">datetime</span><span class="sxs-lookup"><span data-stu-id="d46ba-122">datetime</span></span></p></td>
<td><p><span data-ttu-id="d46ba-123">Uhrzeit der ersten INVITE-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d46ba-123">Time of the first INVITE request.</span></span> <span data-ttu-id="d46ba-124">Dieses Feld wird in der Regel von Daten ausgefüllt, die aus der anfänglichen Einladungsnachricht in der Sitzung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d46ba-124">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="d46ba-125">Wenn keine Einladungsnachricht vorhanden ist, wird das Feld mit dem Datum und der Uhrzeit der ersten relevanten SIP-Nachricht gefüllt (Bye, Cancel, Nachricht oder info).</span><span class="sxs-lookup"><span data-stu-id="d46ba-125">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span> <span data-ttu-id="d46ba-126">Dieses Feld wird in der Regel von Daten ausgefüllt, die aus der anfänglichen Einladungsnachricht in der Sitzung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d46ba-126">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="d46ba-127">Wenn keine Einladungsnachricht vorhanden ist, wird das Feld mit dem Datum und der Uhrzeit der ersten relevanten SIP-Nachricht gefüllt (Bye, Cancel, Nachricht oder info).</span><span class="sxs-lookup"><span data-stu-id="d46ba-127">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-128"><strong>FromUri</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-128"><strong>FromUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-129">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d46ba-129">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-130">Der URI des Benutzers, der die Sitzung gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="d46ba-130">URI of the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-131"><strong>Touri</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-131"><strong>ToUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-132">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d46ba-132">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-133">Der URI des Benutzers, der der Sitzung beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d46ba-133">URI of the user who joined the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-134"><strong>FromUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-134"><strong>FromUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-135">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d46ba-135">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-136">Der Typ des URIs des Benutzers, der die Sitzung gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="d46ba-136">Type of URI of the user who started the session.</span></span> <span data-ttu-id="d46ba-137">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d46ba-137">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-138"><strong>ToUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-138"><strong>ToUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-139">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d46ba-139">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-140">Der Typ des URIs des Benutzers, der der Sitzung beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d46ba-140">Type of URI of the user who joined the session.</span></span> <span data-ttu-id="d46ba-141">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d46ba-141">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-142"><strong>FromTenant</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-142"><strong>FromTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-143">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d46ba-143">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-144">Der Mandant des Benutzers, der die Sitzung gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="d46ba-144">Tenant of the user who started the session.</span></span> <span data-ttu-id="d46ba-145">Weitere Informationen finden Sie <a href="lync-server-2013-tenants-table.md">in der Tabelle Mandanten in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d46ba-145">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-146"><strong>Totenant</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-146"><strong>ToTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-147">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d46ba-147">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-148">Der Mandant des Benutzers, der der Sitzung beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d46ba-148">The tenant of the user who joined the session.</span></span> <span data-ttu-id="d46ba-149">Weitere Informationen finden Sie <a href="lync-server-2013-tenants-table.md">in der Tabelle Mandanten in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d46ba-149">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-150"><strong>FromEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-150"><strong>FromEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-151">uniqueidentifier</span><span class="sxs-lookup"><span data-stu-id="d46ba-151">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="d46ba-152">Eindeutiger Bezeichner des Endpunkts des Benutzers, der die Sitzung gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="d46ba-152">Unique identifier of the endpoint of the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-153"><strong>Endpunkt-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-153"><strong>ToEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-154">uniqueidentifier</span><span class="sxs-lookup"><span data-stu-id="d46ba-154">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="d46ba-155">Eindeutiger Bezeichner des Endpunkts des Benutzers, der der Sitzung beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d46ba-155">Unique identifier of the endpoint of the user who joined the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-156"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-156"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-157">datetime</span><span class="sxs-lookup"><span data-stu-id="d46ba-157">datetime</span></span></p></td>
<td><p><span data-ttu-id="d46ba-158">Endzeit der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="d46ba-158">End time of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-159"><strong>FromMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-159"><strong>FromMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-160">int</span><span class="sxs-lookup"><span data-stu-id="d46ba-160">int</span></span></p></td>
<td><p><span data-ttu-id="d46ba-161">Die Anzahl der Nachrichten, die von dem Benutzer gesendet wurden, der die Sitzung gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="d46ba-161">Number of messages sent by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-162"><strong>ToMessageCount</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-162"><strong>ToMessageCount</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-163">int</span><span class="sxs-lookup"><span data-stu-id="d46ba-163">int</span></span></p></td>
<td><p><span data-ttu-id="d46ba-164">Die Anzahl der Nachrichten, die von dem Benutzer gesendet wurden, der der Sitzung beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d46ba-164">Number of messages sent by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-165"><strong>FromClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-165"><strong>FromClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-166">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d46ba-166">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-167">Die Version des Clients, die von dem Benutzer verwendet wird, der die Sitzung gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="d46ba-167">Version of client used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-168"><strong>FromClientType</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-168"><strong>FromClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-169">int</span><span class="sxs-lookup"><span data-stu-id="d46ba-169">int</span></span></p></td>
<td><p><span data-ttu-id="d46ba-170">Der Client, der von dem Benutzer verwendet wird, der die Sitzung gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="d46ba-170">Client used by the user who started the session.</span></span> <span data-ttu-id="d46ba-171">Weitere Informationen finden Sie <a href="lync-server-2013-useragentdef-table.md">in der UserAgentDef-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d46ba-171">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-172"><strong>FromClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-172"><strong>FromClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-173">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="d46ba-173">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-174">Der Name der Kategorie des Clients, der vom Benutzer verwendet wird, der die Sitzung gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="d46ba-174">Name of the category of the client used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-175"><strong>ToClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-175"><strong>ToClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-176">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d46ba-176">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-177">Die Version des Clients, die von dem Benutzer verwendet wird, der der Sitzung beigetreten ist</span><span class="sxs-lookup"><span data-stu-id="d46ba-177">Version of client used by the user who joined the session</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-178"><strong>Toclienttype</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-178"><strong>ToClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-179">int</span><span class="sxs-lookup"><span data-stu-id="d46ba-179">int</span></span></p></td>
<td><p><span data-ttu-id="d46ba-180">Der Client, der von dem Benutzer verwendet wird, der der Sitzung beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d46ba-180">Client used by the user who joined the session.</span></span> <span data-ttu-id="d46ba-181">Weitere Informationen finden Sie <a href="lync-server-2013-useragentdef-table.md">in der UserAgentDef-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d46ba-181">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-182"><strong>ToClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-182"><strong>ToClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-183">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="d46ba-183">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-184">Der Name der Kategorie des Clients, der von dem Benutzer verwendet wird, der der Sitzung beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="d46ba-184">Name of the category of the client used by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-185"><strong>TargetUri</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-185"><strong>TargetUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-186">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d46ba-186">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-187">Der URI des Zielbenutzers der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="d46ba-187">URI of the target user of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-188"><strong>TargetUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-188"><strong>TargetUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-189">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d46ba-189">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-190">Der Typ des URIs des Zielbenutzers für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="d46ba-190">Type of URI of the target user for the session.</span></span> <span data-ttu-id="d46ba-191">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d46ba-191">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-192"><strong>OnBehalfOfUri</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-192"><strong>OnBehalfOfUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-193">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d46ba-193">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-194">Der URI des Benutzers, in dessen Auftrag die Sitzung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="d46ba-194">URI of the user on whose behalf the session was started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-195"><strong>OnnnBehalfOfUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-195"><strong>OnnnBehalfOfUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d46ba-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-197">Der Typ des URIs des Benutzers, in dessen Auftrag die Sitzung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="d46ba-197">Type of URI of the user on whose behalf the session was started.</span></span> <span data-ttu-id="d46ba-198">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d46ba-198">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-199"><strong>OnBehalfOfTenant</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-199"><strong>OnBehalfOfTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-200">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d46ba-200">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-201">Der Mandant des Benutzers, dessen Namen für die Sitzung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="d46ba-201">Tenant of the user whose on behalf the session was started.</span></span> <span data-ttu-id="d46ba-202">Weitere Informationen finden Sie <a href="lync-server-2013-tenants-table.md">in der Tabelle Mandanten in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d46ba-202">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-203"><strong>ReferredByUri</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-203"><strong>ReferredByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-204">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="d46ba-204">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-205">Der URI des Benutzers, der die Sitzung angewiesen hat.</span><span class="sxs-lookup"><span data-stu-id="d46ba-205">URI of the user who referred the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-206"><strong>ReferredByUriType</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-206"><strong>ReferredByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-207">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d46ba-207">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-208">Der Typ des URIs des Benutzers, der die Sitzung angewiesen hat.</span><span class="sxs-lookup"><span data-stu-id="d46ba-208">Type of URI of the user who referred the session.</span></span> <span data-ttu-id="d46ba-209">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d46ba-209">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-210"><strong>ReferredByTenant</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-210"><strong>ReferredByTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-211">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d46ba-211">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-212">Der Mandant des Benutzers, der die Sitzung angewiesen hat.</span><span class="sxs-lookup"><span data-stu-id="d46ba-212">Tenant of the user who referred the session.</span></span> <span data-ttu-id="d46ba-213">Weitere Informationen finden Sie <a href="lync-server-2013-tenants-table.md">in der Tabelle Mandanten in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d46ba-213">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-214"><strong>Dialogfeld-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-214"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-215">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="d46ba-215">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-216">SIP-Dialogfeld-ID.</span><span class="sxs-lookup"><span data-stu-id="d46ba-216">SIP dialog ID.</span></span> <span data-ttu-id="d46ba-217">Das Format lautet:</span><span class="sxs-lookup"><span data-stu-id="d46ba-217">The format is:</span></span></p>
<p><span data-ttu-id="d46ba-218">Dialogfeld; from-Tag; to-Tag</span><span class="sxs-lookup"><span data-stu-id="d46ba-218">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-219"><strong>CorrelationId</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-219"><strong>CorrelationId</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-220">uniqueidentifier</span><span class="sxs-lookup"><span data-stu-id="d46ba-220">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="d46ba-221">GUID, die verwendet wird, um mehrere Sitzungen zu korrelieren.</span><span class="sxs-lookup"><span data-stu-id="d46ba-221">GUID used to correlate multiple sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-222"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-222"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-223">datetime</span><span class="sxs-lookup"><span data-stu-id="d46ba-223">datetime</span></span></p></td>
<td><p><span data-ttu-id="d46ba-224">Uhrzeit des Dialogs, der durch die Sitzung ersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="d46ba-224">Time of the dialog which was replaced by the session.</span></span> <span data-ttu-id="d46ba-225">Wird in Verbindung mit ReplaceDialogIdSeq verwendet, um ein durch die Sitzung Ersetztes Dialogfeld eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d46ba-225">Used in conjunction with ReplaceDialogIdSeq to uniquely identify a dialog that is replaced by the session.</span></span> <span data-ttu-id="d46ba-226">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d46ba-226">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-227"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-227"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-228">int</span><span class="sxs-lookup"><span data-stu-id="d46ba-228">int</span></span></p></td>
<td><p><span data-ttu-id="d46ba-229">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d46ba-229">ID number to identify the session.</span></span> <span data-ttu-id="d46ba-230">Wird in Verbindung mit ReplaceDialogIdTime verwendet, um ein durch die Sitzung Ersetztes Dialogfeld eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d46ba-230">Used in conjunction with ReplaceDialogIdTime to uniquely identify a dialog that is replaced by the session.</span></span> <span data-ttu-id="d46ba-231">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="d46ba-231">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-232"><strong>ReplacesDialogId</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-232"><strong>ReplacesDialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-233">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="d46ba-233">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-234">SIP-Dialog-ID, die die Sitzung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="d46ba-234">SIP dialog ID the session replaces.</span></span> <span data-ttu-id="d46ba-235">Das Format lautet:</span><span class="sxs-lookup"><span data-stu-id="d46ba-235">The format is:</span></span></p>
<p><span data-ttu-id="d46ba-236">Dialogfeld; from-Tag; to-Tag</span><span class="sxs-lookup"><span data-stu-id="d46ba-236">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-237"><strong>Webantworten</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-237"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-238">datetime</span><span class="sxs-lookup"><span data-stu-id="d46ba-238">datetime</span></span></p></td>
<td><p><span data-ttu-id="d46ba-239">Zeitpunkt der Antwort auf die erste Einladungsnachricht.</span><span class="sxs-lookup"><span data-stu-id="d46ba-239">Time of the response to the first INVITE message.</span></span> <span data-ttu-id="d46ba-240">Dieses Feld wird in der Regel von Daten ausgefüllt, die aus der anfänglichen Einladungsnachricht in der Sitzung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d46ba-240">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="d46ba-241">Wenn keine Einladungsnachricht vorhanden ist, wird das Feld mit dem Datum und der Uhrzeit der ersten relevanten SIP-Nachricht gefüllt (Bye, Cancel, Nachricht oder info).</span><span class="sxs-lookup"><span data-stu-id="d46ba-241">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-242"><strong>Response Code</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-242"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-243">int</span><span class="sxs-lookup"><span data-stu-id="d46ba-243">int</span></span></p></td>
<td><p><span data-ttu-id="d46ba-244">SIP-Antwortcode für die Sitzungseinladung</span><span class="sxs-lookup"><span data-stu-id="d46ba-244">SIP response code to the session invitation.</span></span> <span data-ttu-id="d46ba-245">Dieses Feld wird in der Regel von Daten ausgefüllt, die aus der anfänglichen Einladungsnachricht in der Sitzung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="d46ba-245">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="d46ba-246">Wenn keine Einladungsnachricht vorhanden ist, wird das Feld mit dem Datum und der Uhrzeit der ersten relevanten SIP-Nachricht gefüllt (Bye, Cancel, Nachricht oder info).</span><span class="sxs-lookup"><span data-stu-id="d46ba-246">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-247"><strong>Diagnose-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-247"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-248">int</span><span class="sxs-lookup"><span data-stu-id="d46ba-248">int</span></span></p></td>
<td><p><span data-ttu-id="d46ba-249">Von SIP-Headern erfasste Diagnose-ID.</span><span class="sxs-lookup"><span data-stu-id="d46ba-249">Diagnostic ID captured from SIP headers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-250"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-250"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-251">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d46ba-251">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-252">Der Typ des Inhalts für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="d46ba-252">Type of content for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-253"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-253"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-254">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d46ba-254">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-255">FQDN des Front-End-Servers, der die Daten für die Sitzung erfasst hat.</span><span class="sxs-lookup"><span data-stu-id="d46ba-255">FQDN of the Front End server that captured the data for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-256"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-256"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-257">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d46ba-257">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-258">Der FQDN des Pools, in dem die Daten für die Sitzung erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="d46ba-258">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-259"><strong>FromEdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-259"><strong>FromEdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-260">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d46ba-260">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-261">Der FQDN des Edge-Servers, der vom Benutzer verwendet wird, der die Sitzung gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="d46ba-261">FQDN of the Edge server used by the user who started the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-262"><strong>ToEdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-262"><strong>ToEdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-263">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d46ba-263">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-264">FQDN des Edge-Servers, der vom Benutzer verwendet wird, der die Sitzung gestartet hat</span><span class="sxs-lookup"><span data-stu-id="d46ba-264">FQDN of the Edge server used by the user who started the session</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-265"><strong>IsFromInternal</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-265"><strong>IsFromInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-266">bit</span><span class="sxs-lookup"><span data-stu-id="d46ba-266">bit</span></span></p></td>
<td><p><span data-ttu-id="d46ba-267">Gibt an, ob der Benutzer, der die Sitzung gestartet hat, sich über das interne Netzwerk angemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="d46ba-267">Indicates whether the user who started the session logged on from the internal network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-268"><strong>IsToInternal</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-268"><strong>IsToInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-269">bit</span><span class="sxs-lookup"><span data-stu-id="d46ba-269">bit</span></span></p></td>
<td><p><span data-ttu-id="d46ba-270">Gibt an, ob der Benutzer, der der Sitzung beigetreten ist, aus dem internen Netzwerk angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="d46ba-270">Indicates whether the user who joined the session logged on from the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-271"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-271"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-272">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="d46ba-272">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-273">Anrufpriorität der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="d46ba-273">Call priority of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-274"><strong>FromUserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-274"><strong>FromUserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-275">smallint</span><span class="sxs-lookup"><span data-stu-id="d46ba-275">smallint</span></span></p></td>
<td><p><span data-ttu-id="d46ba-276">Gibt die Attribute des Benutzers an, der die Sitzung gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="d46ba-276">Indicates the attributes of the user who started the session.</span></span> <span data-ttu-id="d46ba-277">Die folgenden Attributdefinitionen sind zulässig:</span><span class="sxs-lookup"><span data-stu-id="d46ba-277">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="d46ba-278">0x01-integriert mit dem Desktoptelefon</span><span class="sxs-lookup"><span data-stu-id="d46ba-278">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-279"><strong>ToUserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-279"><strong>ToUserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-280">smallint</span><span class="sxs-lookup"><span data-stu-id="d46ba-280">smallint</span></span></p></td>
<td><p><span data-ttu-id="d46ba-281">Gibt die Attribute des Benutzers an, der die Sitzung gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="d46ba-281">Indicates the attributes of the user who started the session.</span></span> <span data-ttu-id="d46ba-282">Die folgenden Attributdefinitionen sind zulässig:</span><span class="sxs-lookup"><span data-stu-id="d46ba-282">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="d46ba-283">0x01-integriert mit dem Desktoptelefon</span><span class="sxs-lookup"><span data-stu-id="d46ba-283">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d46ba-284"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-284"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-285">smallint</span><span class="sxs-lookup"><span data-stu-id="d46ba-285">smallint</span></span></p></td>
<td><p><span data-ttu-id="d46ba-286">Gibt die anrufattribute an.</span><span class="sxs-lookup"><span data-stu-id="d46ba-286">Indicates the call attributes.</span></span> <span data-ttu-id="d46ba-287">Die folgenden Attributdefinitionen sind zulässig:</span><span class="sxs-lookup"><span data-stu-id="d46ba-287">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="d46ba-288">0x01-wiederholte Sitzung</span><span class="sxs-lookup"><span data-stu-id="d46ba-288">0x01 - Retried Session</span></span></p>
<p><span data-ttu-id="d46ba-289">0x02 – ein Anruf, der von einem Agenten im Auftrag einer Reaktionsgruppe durchgeführt wurde</span><span class="sxs-lookup"><span data-stu-id="d46ba-289">0x02 - A call made by agent on behalf of a Response Group</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d46ba-290"><strong>Standort</strong></span><span class="sxs-lookup"><span data-stu-id="d46ba-290"><strong>Location</strong></span></span></p></td>
<td><p><span data-ttu-id="d46ba-291">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="d46ba-291">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="d46ba-292">Ort des Notrufs.</span><span class="sxs-lookup"><span data-stu-id="d46ba-292">Location of emergency call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d46ba-293">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d46ba-293">


</div>

<span> </span>

</div>

</div>

</span></span></div>

