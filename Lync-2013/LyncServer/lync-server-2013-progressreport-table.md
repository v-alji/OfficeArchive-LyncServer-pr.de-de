---
title: 'Lync Server 2013: ProgressReport-Tabelle'
description: 'Lync Server 2013: ProgressReport-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ProgressReport table
ms:assetid: 38e5f060-5e9b-4185-87b2-7ef61c4bb75f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425864(v=OCS.15)
ms:contentKeyID: 48183847
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d36ee2ab75410ea2462da4b647ef5b45afefb1bb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436867"
---
# <a name="progressreport-table-in-lync-server-2013"></a><span data-ttu-id="0e06c-103">ProgressReport-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0e06c-103">ProgressReport table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0e06c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0e06c-104">

<span> </span></span></span>

<span data-ttu-id="0e06c-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="0e06c-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="0e06c-106">Statusberichte basieren auf Daten, die vom Client nach Abschluss eines Anrufs oder einer Sitzung an die Datenbank hochgeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="0e06c-106">Progress reports are based on data uploaded by the client to the database after a call or session is completed.</span></span> <span data-ttu-id="0e06c-107">Fortschrittsberichte werden nur für Anrufe und Sitzungen geschrieben, die von lync Server 2013 für diagnostische Zwecke nützlich sein können.</span><span class="sxs-lookup"><span data-stu-id="0e06c-107">Progress reports will be written only for calls and sessions that Lync Server 2013 determines might be useful for diagnostic purposes.</span></span>

<span data-ttu-id="0e06c-108">Die Felder "Fehler", "ErrorReportSeq" und "ProgressReportSeq" beziehen sich nicht unbedingt auf Fehler, sondern auf Nachrichten, die den Status von anrufen oder Nachrichten angeben.</span><span class="sxs-lookup"><span data-stu-id="0e06c-108">The ErrorTime, ErrorReportSeq and ProgressReportSeq fields don’t necessarily refer to errors but to messages that indicate the status of calls or messages.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0e06c-109">Spalte</span><span class="sxs-lookup"><span data-stu-id="0e06c-109">Column</span></span></th>
<th><span data-ttu-id="0e06c-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="0e06c-110">Data Type</span></span></th>
<th><span data-ttu-id="0e06c-111">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="0e06c-111">Key/Index</span></span></th>
<th><span data-ttu-id="0e06c-112">Details</span><span class="sxs-lookup"><span data-stu-id="0e06c-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0e06c-113"><strong>Fehlerzeit</strong></span><span class="sxs-lookup"><span data-stu-id="0e06c-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="0e06c-114">datetime</span><span class="sxs-lookup"><span data-stu-id="0e06c-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="0e06c-115">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="0e06c-115">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="0e06c-116">Datum und Uhrzeit des Status Fehlerberichts, der diesen Statusbericht enthält.</span><span class="sxs-lookup"><span data-stu-id="0e06c-116">Date and time of the progress error report that contains this progress report.</span></span> <span data-ttu-id="0e06c-117">Weitere Informationen finden Sie <a href="lync-server-2013-errorreport-table.md">in der errorreport-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0e06c-117">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e06c-118"><strong>ErrorID</strong></span><span class="sxs-lookup"><span data-stu-id="0e06c-118"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="0e06c-119">int</span><span class="sxs-lookup"><span data-stu-id="0e06c-119">int</span></span></p></td>
<td><p><span data-ttu-id="0e06c-120">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="0e06c-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="0e06c-121">ID-Nummer, die in Verbindung mit Fehlerzeit verwendet wird, ProgressReportSeq, um einen Statusbericht eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0e06c-121">ID number used in conjunction with ErrorTime, ProgressReportSeq to uniquely identify a progress report.</span></span> <span data-ttu-id="0e06c-122">Weitere Informationen finden Sie <a href="lync-server-2013-errorreport-table.md">in der errorreport-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0e06c-122">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e06c-123"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="0e06c-123"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="0e06c-124">int</span><span class="sxs-lookup"><span data-stu-id="0e06c-124">int</span></span></p></td>
<td><p><span data-ttu-id="0e06c-125">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="0e06c-125">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="0e06c-126">Die ID-Nummer, die den Fehlerbericht identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0e06c-126">ID number that identifies the error report.</span></span> <span data-ttu-id="0e06c-127">ErrorReporSeq wird in Verbindung mit Fehlerzeit verwendet, um einen Fehlerbericht eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0e06c-127">ErrorReporSeq is used in conjunction with ErrorTime to uniquely identify an error report.</span></span> <span data-ttu-id="0e06c-128">Weitere Informationen finden Sie <a href="lync-server-2013-errorreport-table.md">in der errorreport-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="0e06c-128">See the <a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a> for more information</span></span></p>
<p><span data-ttu-id="0e06c-129">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0e06c-129">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e06c-130"><strong>ProgressReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="0e06c-130"><strong>ProgressReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="0e06c-131">int</span><span class="sxs-lookup"><span data-stu-id="0e06c-131">int</span></span></p></td>
<td><p><span data-ttu-id="0e06c-132">Primary</span><span class="sxs-lookup"><span data-stu-id="0e06c-132">Primary</span></span></p></td>
<td><p><span data-ttu-id="0e06c-133">Die ID-Nummer zur Identifizierung des Statusberichts.</span><span class="sxs-lookup"><span data-stu-id="0e06c-133">ID number to identify the progress report.</span></span> <span data-ttu-id="0e06c-134">Wird in Verbindung mit Fehlerzeit und ErrorReportSeq verwendet, um einen Statusbericht eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="0e06c-134">Used in conjunction with ErrorTime and ErrorReportSeq to uniquely identify a progress report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e06c-135"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="0e06c-135"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="0e06c-136">int</span><span class="sxs-lookup"><span data-stu-id="0e06c-136">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0e06c-137">Diagnose-ID des Statusberichts</span><span class="sxs-lookup"><span data-stu-id="0e06c-137">Diagnostic ID of the progress report.</span></span></p>
<p><span data-ttu-id="0e06c-138">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0e06c-138">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e06c-139"><strong>SourceID</strong></span><span class="sxs-lookup"><span data-stu-id="0e06c-139"><strong>SourceId</strong></span></span></p></td>
<td><p><span data-ttu-id="0e06c-140">int</span><span class="sxs-lookup"><span data-stu-id="0e06c-140">int</span></span></p></td>
<td><p><span data-ttu-id="0e06c-141">Fremd</span><span class="sxs-lookup"><span data-stu-id="0e06c-141">Foreign</span></span></p></td>
<td><p><span data-ttu-id="0e06c-142">Der Server, der den Fehlerbericht gesendet hat (wenn der Bericht von einer Serverkomponente gesendet wurde).</span><span class="sxs-lookup"><span data-stu-id="0e06c-142">Server that sent the error report (if the report was sent from a server component).</span></span> <span data-ttu-id="0e06c-143">Weitere Informationen finden Sie <a href="lync-server-2013-servers-table.md">in der Tabelle Server in lync Server 2013</a> . Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0e06c-143">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e06c-144"><strong>ApplicationId</strong></span><span class="sxs-lookup"><span data-stu-id="0e06c-144"><strong>ApplicationId</strong></span></span></p></td>
<td><p><span data-ttu-id="0e06c-145">int</span><span class="sxs-lookup"><span data-stu-id="0e06c-145">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0e06c-146">Der lync-Server Prozess, zu dem der Bericht gehört.</span><span class="sxs-lookup"><span data-stu-id="0e06c-146">The Lync Server process that the report is about.</span></span> <span data-ttu-id="0e06c-147">Weitere Informationen finden Sie in der Anwendungstabelle.</span><span class="sxs-lookup"><span data-stu-id="0e06c-147">See the Application Table for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e06c-148"><strong>Detail</strong></span><span class="sxs-lookup"><span data-stu-id="0e06c-148"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="0e06c-149">Bild</span><span class="sxs-lookup"><span data-stu-id="0e06c-149">image</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0e06c-150">Details des Statusberichts, die im Binärformat gespeichert werden, um Platz zu sparen. Diese Daten können mit dieser Syntax in das Text Format konvertiert werden:</span><span class="sxs-lookup"><span data-stu-id="0e06c-150">Progress report details, stored in binary format to save space.This data can be converted to text format using this syntax:</span></span></p>
<p><span data-ttu-id="0e06c-151">Umwandlung (Umwandlung (Detail als varbinary (max)) als varchar (max))</span><span class="sxs-lookup"><span data-stu-id="0e06c-151">cast(cast(Detail as varbinary(max)) as varchar(max))</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0e06c-152"><strong>Telemetrie</strong></span><span class="sxs-lookup"><span data-stu-id="0e06c-152"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="0e06c-153">uniqueIdentifier</span><span class="sxs-lookup"><span data-stu-id="0e06c-153">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0e06c-154">Eindeutiger Bezeichner, der die Verknüpfungszeit Informationen für die verschiedenen an einer Konferenz beteiligten Komponenten korreliert.</span><span class="sxs-lookup"><span data-stu-id="0e06c-154">Unique identifier that correlates join time information for the different components involved in a conference.</span></span></p>
<p><span data-ttu-id="0e06c-155">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0e06c-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0e06c-156"><strong>SessionSetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="0e06c-156"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="0e06c-157">int</span><span class="sxs-lookup"><span data-stu-id="0e06c-157">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="0e06c-158">Zeit (in Millisekunden) für eine bestimmte Komponente, um an einer Konferenz teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="0e06c-158">Time (in milliseconds) for a specific component to join a conference.</span></span></p>
<p><span data-ttu-id="0e06c-159">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="0e06c-159">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0e06c-160">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0e06c-160">


</div>

<span> </span>

</div>

</div>

</span></span></div>

