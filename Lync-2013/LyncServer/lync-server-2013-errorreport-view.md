---
title: 'Lync Server 2013: errorreport-Ansicht'
description: 'Lync Server 2013: errorreport-Ansicht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorReport view
ms:assetid: ca873f7e-b18b-4eaf-8db0-5f9d5a9b60a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721887(v=OCS.15)
ms:contentKeyID: 49733821
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 50fb0a362c71d8dfb5873157e7b1ed3d3eb680ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428524"
---
# <a name="errorreport-view-in-lync-server-2013"></a><span data-ttu-id="71664-103">ErrorReport-Ansicht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="71664-103">ErrorReport view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="71664-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="71664-104">

<span> </span></span></span>

<span data-ttu-id="71664-105">_**Letztes Änderungsdatum des Themas:** 2013-01-22_</span><span class="sxs-lookup"><span data-stu-id="71664-105">_**Topic Last Modified:** 2013-01-22_</span></span>

<span data-ttu-id="71664-106">In der errorreport-Ansicht werden Informationen zu den gemeldeten Fehlern gespeichert.</span><span class="sxs-lookup"><span data-stu-id="71664-106">The ErrorReport view stores information about errors reported.</span></span> <span data-ttu-id="71664-107">Bei jedem Datensatz handelt es sich um ein Fehlerereignis.</span><span class="sxs-lookup"><span data-stu-id="71664-107">Each record is one error occurrence.</span></span> <span data-ttu-id="71664-108">Die Fehler werden entweder vom CDR-Agent, der auf dem Front-End-Server ausgeführt wird, erfasst oder vom Client gesendet.</span><span class="sxs-lookup"><span data-stu-id="71664-108">The errors are captured either by the CDR agent running on the front-end server or sent from the client.</span></span> <span data-ttu-id="71664-109">Diese Ansicht wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="71664-109">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="71664-110">Spalte</span><span class="sxs-lookup"><span data-stu-id="71664-110">Column</span></span></th>
<th><span data-ttu-id="71664-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="71664-111">Data Type</span></span></th>
<th><span data-ttu-id="71664-112">Details</span><span class="sxs-lookup"><span data-stu-id="71664-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="71664-113"><strong>Fehlerzeit</strong></span><span class="sxs-lookup"><span data-stu-id="71664-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-114">datetime</span><span class="sxs-lookup"><span data-stu-id="71664-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="71664-115">Zeitpunkt des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="71664-115">Time of error occurred.</span></span> <span data-ttu-id="71664-116">Wird in Verbindung mit ErrorReportSeq verwendet, um einen Fehler eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="71664-116">Used in conjunction with ErrorReportSeq to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71664-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="71664-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-118">int</span><span class="sxs-lookup"><span data-stu-id="71664-118">int</span></span></p></td>
<td><p><span data-ttu-id="71664-119">Die ID-Nummer, um den Fehler zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="71664-119">ID number to identify the error.</span></span> <span data-ttu-id="71664-120">Wird in Verbindung mit Fehlerzeit verwendet, um einen Fehler eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="71664-120">Used in conjunction with ErrorTime to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71664-121"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="71664-121"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-122">int</span><span class="sxs-lookup"><span data-stu-id="71664-122">int</span></span></p></td>
<td><p><span data-ttu-id="71664-123">Diagnose-ID für den Fehlerbericht.</span><span class="sxs-lookup"><span data-stu-id="71664-123">Diagnostic ID for the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71664-124"><strong>FromUri</strong></span><span class="sxs-lookup"><span data-stu-id="71664-124"><strong>FromUri</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-125">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="71664-125">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="71664-126">Der URI des Benutzers, der den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="71664-126">URI of the user who originated the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71664-127"><strong>FromUriType</strong></span><span class="sxs-lookup"><span data-stu-id="71664-127"><strong>FromUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="71664-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="71664-129">Der Typ des URIs des Benutzers, der den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="71664-129">Type of URI of the user who originated the error.</span></span> <span data-ttu-id="71664-130">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="71664-130">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71664-131"><strong>FromTenant</strong></span><span class="sxs-lookup"><span data-stu-id="71664-131"><strong>FromTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="71664-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="71664-133">Der Mandant des Benutzers, der den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="71664-133">Tenant of the user who originated the error.</span></span> <span data-ttu-id="71664-134">Weitere Informationen finden Sie <a href="lync-server-2013-tenants-table.md">in der Tabelle Mandanten in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="71664-134">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71664-135"><strong>Touri</strong></span><span class="sxs-lookup"><span data-stu-id="71664-135"><strong>ToUri</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-136">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="71664-136">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="71664-137">Der URI des Benutzers, der das Ziel des Fehlerberichts war.</span><span class="sxs-lookup"><span data-stu-id="71664-137">URI of the user who was the target of the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71664-138"><strong>ToUriType</strong></span><span class="sxs-lookup"><span data-stu-id="71664-138"><strong>ToUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-139">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="71664-139">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="71664-140">Der Typ des URIs des Benutzers, der auf den Fehlerbericht ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="71664-140">Type of URI of the user who target of the error report.</span></span> <span data-ttu-id="71664-141">Weitere Informationen finden Sie in der UriTypes-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="71664-141">See the UriTypes Table for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71664-142"><strong>Totenant</strong></span><span class="sxs-lookup"><span data-stu-id="71664-142"><strong>ToTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-143">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="71664-143">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="71664-144">Der Mandant des Benutzers, der auf den Fehlerbericht abzielt.</span><span class="sxs-lookup"><span data-stu-id="71664-144">Tenant of the user who target of the error report.</span></span> <span data-ttu-id="71664-145">Weitere Informationen finden Sie <a href="lync-server-2013-tenants-table.md">in der Tabelle Mandanten in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="71664-145">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71664-146"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="71664-146"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-147">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="71664-147">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="71664-148">Der URI der Konferenz, die das Ziel des Fehlerberichts war.</span><span class="sxs-lookup"><span data-stu-id="71664-148">URI of the conference that was the target of the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71664-149"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="71664-149"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="71664-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="71664-151">Der URI-Typ der Konferenz, die das Ziel des Fehlerberichts war.</span><span class="sxs-lookup"><span data-stu-id="71664-151">URI type of the conference that was the target of the error report.</span></span> <span data-ttu-id="71664-152">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="71664-152">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71664-153"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="71664-153"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-154">datetime</span><span class="sxs-lookup"><span data-stu-id="71664-154">datetime</span></span></p></td>
<td><p><span data-ttu-id="71664-155">Die Uhrzeit der Sitzungsanforderung, von der der Fehlerbericht stammt.</span><span class="sxs-lookup"><span data-stu-id="71664-155">Time of session request that originated the error report.</span></span> <span data-ttu-id="71664-156">Wird in Verbindung mit SessionIdSeq verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="71664-156">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="71664-157">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="71664-157">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71664-158"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="71664-158"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-159">int</span><span class="sxs-lookup"><span data-stu-id="71664-159">int</span></span></p></td>
<td><p><span data-ttu-id="71664-160">Die ID-Nummer, mit der die Sitzungsanforderung identifiziert wird, von der der Fehlerbericht stammt.</span><span class="sxs-lookup"><span data-stu-id="71664-160">ID number to identify the session request that originated the error report.</span></span> <span data-ttu-id="71664-161">Wird in Verbindung mit SessionID-Mal verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="71664-161">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="71664-162">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="71664-162">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71664-163"><strong>Dialogfeld-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="71664-163"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-164">varstring (775)</span><span class="sxs-lookup"><span data-stu-id="71664-164">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="71664-165">SIP-Dialogfeld-ID der Sitzung, die den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="71664-165">SIP dialog ID of session that originated the error.</span></span> <span data-ttu-id="71664-166">Das Format lautet:</span><span class="sxs-lookup"><span data-stu-id="71664-166">The format is:</span></span></p>
<p><span data-ttu-id="71664-167">Dialogfeld; from-Tag; to-Tag</span><span class="sxs-lookup"><span data-stu-id="71664-167">dialog;from-tag;to-tag</span></span></p>
<p><span data-ttu-id="71664-168">Diese Daten können mithilfe der folgenden Syntax in das Text Format konvertiert werden:</span><span class="sxs-lookup"><span data-stu-id="71664-168">This data can be converted to text format by using this syntax:</span></span></p>
<p><span data-ttu-id="71664-169">Umwandlung (Umwandlung (extern-als varbinary (max)) als varchar (max))</span><span class="sxs-lookup"><span data-stu-id="71664-169">cast(cast(ExternalId as varbinary(max)) as varchar(max))</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71664-170"><strong>ClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="71664-170"><strong>ClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-171">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="71664-171">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="71664-172">Die Version des Clients, die von dem Benutzer verwendet wird, der den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="71664-172">Version of client used by the user who originated the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71664-173"><strong>Clienttyp</strong></span><span class="sxs-lookup"><span data-stu-id="71664-173"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-174">int</span><span class="sxs-lookup"><span data-stu-id="71664-174">int</span></span></p></td>
<td><p><span data-ttu-id="71664-175">Der Client, der vom Benutzer verwendet wird, der den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="71664-175">Client used by the user who originated the error.</span></span> <span data-ttu-id="71664-176">Weitere Informationen finden Sie <a href="lync-server-2013-useragentdef-table.md">in der UserAgentDef-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="71664-176">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71664-177"><strong>ClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="71664-177"><strong>ClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-178">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="71664-178">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="71664-179">Der Name der Kategorie des Clients, der vom Benutzer verwendet wird, der den Fehler ausgelöst hat.</span><span class="sxs-lookup"><span data-stu-id="71664-179">Name of the category of the client used by the user who originated the error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71664-180"><strong>Quelle</strong></span><span class="sxs-lookup"><span data-stu-id="71664-180"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-181">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="71664-181">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="71664-182">Name des Servers, der den Fehler verursacht hat (wenn der Bericht von einer Serverkomponente gesendet wurde).</span><span class="sxs-lookup"><span data-stu-id="71664-182">Name of server that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71664-183"><strong>Anwendung</strong></span><span class="sxs-lookup"><span data-stu-id="71664-183"><strong>Application</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-184">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="71664-184">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="71664-185">Der Name der Anwendung, die den Fehler verursacht hat (wenn der Bericht von einer Serverkomponente gesendet wurde).</span><span class="sxs-lookup"><span data-stu-id="71664-185">Name of application that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71664-186"><strong>Response Code</strong></span><span class="sxs-lookup"><span data-stu-id="71664-186"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-187">int</span><span class="sxs-lookup"><span data-stu-id="71664-187">int</span></span></p></td>
<td><p><span data-ttu-id="71664-188">SIP-Antwortcode für die Sitzung der SIP-Nachricht, die den Fehlerbericht enthält.</span><span class="sxs-lookup"><span data-stu-id="71664-188">SIP response code to the session of the SIP message containing the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71664-189"><strong>RequestType</strong></span><span class="sxs-lookup"><span data-stu-id="71664-189"><strong>RequestType</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-190">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="71664-190">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="71664-191">Der Typ der fehlgeschlagenen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="71664-191">Type of request that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71664-192"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="71664-192"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-193">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="71664-193">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="71664-194">Inhaltstyp der fehlgeschlagenen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="71664-194">Content type of the request that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71664-195"><strong>CallType</strong></span><span class="sxs-lookup"><span data-stu-id="71664-195"><strong>CallType</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="71664-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="71664-197">Der Sitzungstyp.</span><span class="sxs-lookup"><span data-stu-id="71664-197">Type of session.</span></span> <span data-ttu-id="71664-198">Weitere Informationen finden Sie <a href="lync-server-2013-calltype-table.md">in der Tabelle "CallType" in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="71664-198">See the <a href="lync-server-2013-calltype-table.md">CallType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71664-199"><strong>Telemetrie</strong></span><span class="sxs-lookup"><span data-stu-id="71664-199"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-200">uniqueidentifier</span><span class="sxs-lookup"><span data-stu-id="71664-200">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="71664-201">Eindeutiger Bezeichner, in dem die Verknüpfungszeit Informationen für die verschiedenen an einer Konferenz beteiligten Komponenten korreliert werden.</span><span class="sxs-lookup"><span data-stu-id="71664-201">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71664-202"><strong>Rüstzeit</strong></span><span class="sxs-lookup"><span data-stu-id="71664-202"><strong>SetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-203">int</span><span class="sxs-lookup"><span data-stu-id="71664-203">int</span></span></p></td>
<td><p><span data-ttu-id="71664-204">Zeit (in Millisekunden), die für eine bestimmte Komponente erforderlich ist, um an einer Konferenz teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="71664-204">Time (in milliseconds) required for a specific component to join a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71664-205"><strong>IsCapturedByServer</strong></span><span class="sxs-lookup"><span data-stu-id="71664-205"><strong>IsCapturedByServer</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-206">bit</span><span class="sxs-lookup"><span data-stu-id="71664-206">bit</span></span></p></td>
<td><p><span data-ttu-id="71664-207">Gibt an, ob der Fehlerbericht vom auf dem Front-End-Server ausgeführten CDR-Agent erfasst oder vom Client gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="71664-207">Indicates whether the error report was captured by the CDR agent running on the Front End server, or sent by the client.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71664-208"><strong>Kennzeichnen</strong></span><span class="sxs-lookup"><span data-stu-id="71664-208"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-209">smallint</span><span class="sxs-lookup"><span data-stu-id="71664-209">smallint</span></span></p></td>
<td><p><span data-ttu-id="71664-210">Für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="71664-210">Reserved for future use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71664-211"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="71664-211"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-212">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="71664-212">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="71664-213">Weitere Informationen zum Fehler.</span><span class="sxs-lookup"><span data-stu-id="71664-213">Additional information about the error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="71664-214"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="71664-214"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-215">nvarchar</span><span class="sxs-lookup"><span data-stu-id="71664-215">nvarchar</span></span></p></td>
<td><p><span data-ttu-id="71664-216">Vollständig qualifizierter Domänenname des Front-End-Servers, der den Bericht übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="71664-216">Fully qualified domain name of the Front End server that submitted the report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="71664-217"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="71664-217"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="71664-218">nvarchar</span><span class="sxs-lookup"><span data-stu-id="71664-218">nvarchar</span></span></p></td>
<td><p><span data-ttu-id="71664-219">Vollständig qualifizierter Domänenname des Pools, der den Front-End-Server enthält, der den Bericht übermittelt hat.</span><span class="sxs-lookup"><span data-stu-id="71664-219">Fully qualified domain name of the pool containing the Front End server that submitted the report.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="71664-220">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="71664-220">


</div>

<span> </span>

</div>

</div>

</span></span></div>

