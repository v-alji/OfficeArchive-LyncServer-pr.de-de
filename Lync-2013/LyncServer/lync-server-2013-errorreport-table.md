---
title: 'Lync Server 2013: ErrorReport-Tabelle'
description: 'Lync Server 2013: errorreport-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorReport table
ms:assetid: ae0287b4-e8ca-4f8c-84ef-502897dcaa2a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412826(v=OCS.15)
ms:contentKeyID: 48185129
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c1cc65c396c16dc137255438f7ef7c32b2d0b78
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428517"
---
# <a name="errorreport-table-in-lync-server-2013"></a><span data-ttu-id="e7711-103">ErrorReport-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e7711-103">ErrorReport table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e7711-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e7711-104">

<span> </span></span></span>

<span data-ttu-id="e7711-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="e7711-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="e7711-106">In der errorreport-Tabelle werden Informationen zu Fehlern gespeichert, die aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="e7711-106">The ErrorReport table stores information about errors that have occurred.</span></span> <span data-ttu-id="e7711-107">Bei jedem Datensatz handelt es sich um ein Fehlerereignis.</span><span class="sxs-lookup"><span data-stu-id="e7711-107">Each record is one error occurrence.</span></span> <span data-ttu-id="e7711-108">Die Fehler werden entweder vom CDR-Agent, der auf dem Front-End-Server ausgeführt wird, erfasst oder vom Client gesendet.</span><span class="sxs-lookup"><span data-stu-id="e7711-108">The errors are captured either by the CDR agent running on the front-end server or sent from the client.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e7711-109">Spalte</span><span class="sxs-lookup"><span data-stu-id="e7711-109">Column</span></span></th>
<th><span data-ttu-id="e7711-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e7711-110">Data Type</span></span></th>
<th><span data-ttu-id="e7711-111">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="e7711-111">Key/Index</span></span></th>
<th><span data-ttu-id="e7711-112">Details</span><span class="sxs-lookup"><span data-stu-id="e7711-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e7711-113"><strong>Fehlerzeit</strong></span><span class="sxs-lookup"><span data-stu-id="e7711-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e7711-114">datetime</span><span class="sxs-lookup"><span data-stu-id="e7711-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="e7711-115">Primary</span><span class="sxs-lookup"><span data-stu-id="e7711-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="e7711-116">Das Datum und die Uhrzeit, zu der der Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e7711-116">Date and time the error occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7711-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="e7711-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="e7711-118">int</span><span class="sxs-lookup"><span data-stu-id="e7711-118">int</span></span></p></td>
<td><p><span data-ttu-id="e7711-119">Primary</span><span class="sxs-lookup"><span data-stu-id="e7711-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="e7711-120">Die ID-Nummer, um den Fehlerbericht zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e7711-120">ID number to identify the error report.</span></span> <span data-ttu-id="e7711-121">Wird in Verbindung mit <strong>Fehler</strong> Zeit verwendet, um einen Fehlerbericht eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e7711-121">Used in conjunction with <strong>ErrorTime</strong> to uniquely identify an error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7711-122"><strong>ErrorID</strong></span><span class="sxs-lookup"><span data-stu-id="e7711-122"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7711-123">int</span><span class="sxs-lookup"><span data-stu-id="e7711-123">int</span></span></p></td>
<td><p><span data-ttu-id="e7711-124">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7711-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7711-125">Eindeutige ID des Fehlertyps.</span><span class="sxs-lookup"><span data-stu-id="e7711-125">Unique ID of the error type.</span></span> <span data-ttu-id="e7711-126">Weitere Informationen finden Sie <a href="lync-server-2013-errordef-table.md">in der ErrorDef-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7711-126">See the <a href="lync-server-2013-errordef-table.md">ErrorDef table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7711-127"><strong>FromUserId</strong></span><span class="sxs-lookup"><span data-stu-id="e7711-127"><strong>FromUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7711-128">int</span><span class="sxs-lookup"><span data-stu-id="e7711-128">int</span></span></p></td>
<td><p><span data-ttu-id="e7711-129">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7711-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7711-130">Der Benutzer, der die Anforderung initiiert hat, die den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="e7711-130">User who originated the request that caused the error.</span></span> <span data-ttu-id="e7711-131">Weitere Informationen finden Sie <a href="lync-server-2013-users-table.md">in der Tabelle Benutzer in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7711-131">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7711-132"><strong>Touser-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="e7711-132"><strong>ToUserId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7711-133">int</span><span class="sxs-lookup"><span data-stu-id="e7711-133">int</span></span></p></td>
<td><p><span data-ttu-id="e7711-134">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7711-134">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7711-135">Der Zielbenutzer für die Anforderung, die den Fehler verursacht hat.</span><span class="sxs-lookup"><span data-stu-id="e7711-135">Destination user for the request that caused the error.</span></span> <span data-ttu-id="e7711-136">Weitere Informationen finden Sie <a href="lync-server-2013-users-table.md">in der Tabelle Benutzer in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7711-136">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7711-137"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="e7711-137"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7711-138">int</span><span class="sxs-lookup"><span data-stu-id="e7711-138">int</span></span></p></td>
<td><p><span data-ttu-id="e7711-139">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7711-139">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7711-140">Konferenz-URI im Zusammenhang mit dem Fehler.</span><span class="sxs-lookup"><span data-stu-id="e7711-140">Conference URI related to the error.</span></span> <span data-ttu-id="e7711-141">Weitere Informationen finden Sie <a href="lync-server-2013-conferenceuris-table.md">in der ConferenceUris-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7711-141">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="e7711-142">Wenn ConferenceUriId nicht NULL ist, ist in der Regel entweder FromUserId oder touser-Wert NULL.</span><span class="sxs-lookup"><span data-stu-id="e7711-142">Typically, if ConferenceUriId is not null, then either FromUserId or ToUserId will be null.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7711-143"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="e7711-143"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e7711-144">datetime</span><span class="sxs-lookup"><span data-stu-id="e7711-144">datetime</span></span></p></td>
<td><p><span data-ttu-id="e7711-145">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7711-145">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7711-146">Wird in Verbindung mit <strong>SessionIdSeq</strong> verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e7711-146">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="e7711-147">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7711-147">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7711-148"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="e7711-148"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="e7711-149">int</span><span class="sxs-lookup"><span data-stu-id="e7711-149">int</span></span></p></td>
<td><p><span data-ttu-id="e7711-150">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7711-150">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7711-151">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e7711-151">ID number to identify the session.</span></span> <span data-ttu-id="e7711-152">Wird in Verbindung mit <strong>SessionID</strong> -Mal verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="e7711-152">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="e7711-153">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7711-153">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7711-154"><strong>SourceID</strong></span><span class="sxs-lookup"><span data-stu-id="e7711-154"><strong>SourceId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7711-155">int</span><span class="sxs-lookup"><span data-stu-id="e7711-155">int</span></span></p></td>
<td><p><span data-ttu-id="e7711-156">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7711-156">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7711-157">Der Server, der den Fehlerbericht gesendet hat (wenn der Bericht von einer Serverkomponente gesendet wird).</span><span class="sxs-lookup"><span data-stu-id="e7711-157">Server that sent the error report (if the report is being sent from a server component).</span></span> <span data-ttu-id="e7711-158">Weitere Informationen finden Sie <a href="lync-server-2013-servers-table.md">in der Tabelle Server in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7711-158">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="e7711-159">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e7711-159">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7711-160"><strong>ApplicationId</strong></span><span class="sxs-lookup"><span data-stu-id="e7711-160"><strong>ApplicationId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7711-161">int</span><span class="sxs-lookup"><span data-stu-id="e7711-161">int</span></span></p></td>
<td><p><span data-ttu-id="e7711-162">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7711-162">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7711-163">Der Server, der den Fehlerbericht gesendet hat (wenn der Bericht von einer Serverkomponente gesendet wird).</span><span class="sxs-lookup"><span data-stu-id="e7711-163">Server that sent the error report (if the report is being sent from a server component).</span></span> <span data-ttu-id="e7711-164">Weitere Informationen finden Sie <a href="lync-server-2013-application-table.md">in der Anwendungstabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7711-164">See the <a href="lync-server-2013-application-table.md">Application table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="e7711-165">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e7711-165">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7711-166"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="e7711-166"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="e7711-167">Bild</span><span class="sxs-lookup"><span data-stu-id="e7711-167">image</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="e7711-168">Weitere Informationen zum Fehler.</span><span class="sxs-lookup"><span data-stu-id="e7711-168">More information about the error.</span></span></p>
<p><span data-ttu-id="e7711-169">Diese Daten können mithilfe der folgenden Syntax in das Text Format konvertiert werden:</span><span class="sxs-lookup"><span data-stu-id="e7711-169">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(Detail as varbinary(max)) as varchar(max)) </code></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7711-170"><strong>ClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="e7711-170"><strong>ClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7711-171">int</span><span class="sxs-lookup"><span data-stu-id="e7711-171">int</span></span></p></td>
<td><p><span data-ttu-id="e7711-172">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7711-172">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7711-173">Die Client Version des Endpunkts, der den Fehlerbericht sendet.</span><span class="sxs-lookup"><span data-stu-id="e7711-173">The client version of endpoint that sends the error report.</span></span> <span data-ttu-id="e7711-174">Weitere Informationen finden Sie <a href="lync-server-2013-clientversions-table.md">in der ClientVersions-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="e7711-174">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7711-175"><strong>IsCapturedByServer</strong></span><span class="sxs-lookup"><span data-stu-id="e7711-175"><strong>IsCapturedByServer</strong></span></span></p></td>
<td><p><span data-ttu-id="e7711-176">bit</span><span class="sxs-lookup"><span data-stu-id="e7711-176">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7711-177">Der Fehlerbericht, der vom auf dem Front-End-Server ausgeführten CDR-Agent erfasst oder vom Client gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="e7711-177">Is the error report captured by the CDR agent running on the front-end server, or sent by the client.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7711-178"><strong>Kennzeichnen</strong></span><span class="sxs-lookup"><span data-stu-id="e7711-178"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="e7711-179">smallint</span><span class="sxs-lookup"><span data-stu-id="e7711-179">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7711-180">Für die spätere Verwendung reserviert.</span><span class="sxs-lookup"><span data-stu-id="e7711-180">Reserved for future use.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7711-181"><strong>Telemetrie</strong></span><span class="sxs-lookup"><span data-stu-id="e7711-181"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7711-182">uniqueIdentifier</span><span class="sxs-lookup"><span data-stu-id="e7711-182">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7711-183">Eindeutiger Bezeichner, in dem die Verknüpfungszeit Informationen für die verschiedenen an einer Konferenz beteiligten Komponenten korreliert werden.</span><span class="sxs-lookup"><span data-stu-id="e7711-183">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p>
<p><span data-ttu-id="e7711-184">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e7711-184">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7711-185"><strong>SessionSetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="e7711-185"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="e7711-186">int</span><span class="sxs-lookup"><span data-stu-id="e7711-186">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e7711-187">Zeit (in Millisekunden), die für eine bestimmte Komponente erforderlich ist, um an einer Konferenz teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="e7711-187">Time (in milliseconds) required for a specific component to join a conference.</span></span></p>
<p><span data-ttu-id="e7711-188">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e7711-188">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e7711-189"><strong>ServerID</strong></span><span class="sxs-lookup"><span data-stu-id="e7711-189"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7711-190">int</span><span class="sxs-lookup"><span data-stu-id="e7711-190">int</span></span></p></td>
<td><p><span data-ttu-id="e7711-191">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7711-191">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7711-192">Stellt den vollqualifizierten Domänennamen des Servers dar, der den Fehlerbericht generiert hat.</span><span class="sxs-lookup"><span data-stu-id="e7711-192">Represents the fully qualified domain name of the server that generated the error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e7711-193"><strong>Pool-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="e7711-193"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="e7711-194">int</span><span class="sxs-lookup"><span data-stu-id="e7711-194">int</span></span></p></td>
<td><p><span data-ttu-id="e7711-195">Fremd</span><span class="sxs-lookup"><span data-stu-id="e7711-195">Foreign</span></span></p></td>
<td><p><span data-ttu-id="e7711-196">Stellt den vollqualifizierten Domänennamen des Pools dar, in dem der Fehlerbericht generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="e7711-196">Represents the fully qualified domain name of the pool where the error report was generated.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e7711-197">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e7711-197">


</div>

<span> </span>

</div>

</div>

</span></span></div>

