---
title: 'Lync Server 2013: Konferenz Detail Bericht'
description: 'Lync Server 2013: Konferenz Detail Bericht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Detail Report
ms:assetid: 1d61cd81-dcfe-40b4-9a41-a73b038bc216
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204728(v=OCS.15)
ms:contentKeyID: 48183565
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07c50b545f4a9ee3308a840fc2aa5a15e617a5bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394206"
---
# <a name="conference-detail-report-in-lync-server-2013"></a><span data-ttu-id="b161e-103">Konferenz Detail Bericht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b161e-103">Conference Detail Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b161e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b161e-104">

<span> </span></span></span>

<span data-ttu-id="b161e-105">_**Letztes Änderungsdatum des Themas:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="b161e-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="b161e-p101">Der detaillierte Konferenzbericht enthält ausführliche Informationen zu allen Benutzern, die an einer Konferenz teilgenommen haben. Sie können beispielsweise Informationen wie Datum und Uhrzeit, an dem bzw. zu der ein Benutzer einer Konferenz beigetreten ist und die Konferenz verlassen hat, sowie den Benutzer-Agent des Endpunkts anzeigen, mit dem der Benutzer mit der Konferenz verbunden wurde. Darüber hinaus können Sie Informationen zu der Rolle des Benutzers in den einzelnen Konferenzen (z. B. Referent oder Teilnehmer) anzeigen. Der vielleicht wichtigste Aspekt ist, dass Sie auf einen Blick erkennen können, welche Benutzer der Konferenz erfolgreich beigetreten und sie abgeschlossen haben und welche Benutzer der Konferenz nicht beitreten konnten und sie daher nicht abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="b161e-p101">The Conference Detail Report provides detailed information about all the users who participated in a conference. For example, you can see such information as the date and time that a user joined the conference, the date and time that the user left the conference, and the user agent of the endpoint that was used to connect that user to the conference. You can also see information the user's role in each conference (for example, Presenter or Attendee). Perhaps most important, you get quickly see which users successfully join and complete the conference, and which users were not able to successfully join and complete the conference.</span></span>

<div>

## <a name="accessing-the-conference-detail-report"></a><span data-ttu-id="b161e-110">Zugreifen auf den detaillierten Konferenzbericht</span><span class="sxs-lookup"><span data-stu-id="b161e-110">Accessing the Conference Detail Report</span></span>

<span data-ttu-id="b161e-111">Auf den detaillierten Konferenzbericht kann über die folgenden Berichte zugegriffen werden:</span><span class="sxs-lookup"><span data-stu-id="b161e-111">The Conference Detail Report can be accessed from the following reports:</span></span>

  - <span data-ttu-id="b161e-112">Der [Bericht zur Anruf Zulassungs Steuerung in lync Server 2013](lync-server-2013-call-admission-control-report.md) (durch Klicken auf die Detail Metrik für eine Konferenz)</span><span class="sxs-lookup"><span data-stu-id="b161e-112">The [Call Admission Control Report in Lync Server 2013](lync-server-2013-call-admission-control-report.md) (by clicking the Detail metric for a conference)</span></span>

  - <span data-ttu-id="b161e-113">Der [fehlerlistenbericht in lync Server 2013](lync-server-2013-failure-list-report.md) (durch Klicken auf die Konferenz Metrik)</span><span class="sxs-lookup"><span data-stu-id="b161e-113">The [Failure List Report in Lync Server 2013](lync-server-2013-failure-list-report.md) (by clicking the Conference metric)</span></span>

  - <span data-ttu-id="b161e-114">Der [Bericht "Benutzeraktivität" in lync Server 2013](lync-server-2013-user-activity-report.md) (durch Klicken auf die Konferenz-URI-Metrik)</span><span class="sxs-lookup"><span data-stu-id="b161e-114">The [User Activity Report in Lync Server 2013](lync-server-2013-user-activity-report.md) (by clicking the Conference URI metric)</span></span>

<span data-ttu-id="b161e-115">Im Konferenz Detail Bericht können Sie auf den [Diagnosebericht in lync Server 2013](lync-server-2013-diagnostic-report.md) zugreifen, indem Sie auf die Metrik für den Diagnosebericht (Detail) klicken.</span><span class="sxs-lookup"><span data-stu-id="b161e-115">From the Conference Detail Report you can access the [Diagnostic Report in Lync Server 2013](lync-server-2013-diagnostic-report.md) by clicking the Diagnostic Report (Detail) metric.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="b161e-116">Filter</span><span class="sxs-lookup"><span data-stu-id="b161e-116">Filters</span></span>

<span data-ttu-id="b161e-p102">Keine. Der detaillierte Konferenzbericht lässt sich nicht filtern.</span><span class="sxs-lookup"><span data-stu-id="b161e-p102">None. You cannot filter on the Conference Detail Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="b161e-119">Metriken</span><span class="sxs-lookup"><span data-stu-id="b161e-119">Metrics</span></span>

<span data-ttu-id="b161e-120">In der folgenden Tabelle werden die Informationen aus dem Abschnitt zu Konferenzinformationen des detaillierten Konferenzberichts aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b161e-120">The following table lists the information provided in the Conference Information section of the Conference Detail Report.</span></span>

### <a name="conference-information-metrics"></a><span data-ttu-id="b161e-121">Konferenzinformationen – Metriken</span><span class="sxs-lookup"><span data-stu-id="b161e-121">Conference Information Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b161e-122">Name</span><span class="sxs-lookup"><span data-stu-id="b161e-122">Name</span></span></th>
<th><span data-ttu-id="b161e-123">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="b161e-123">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="b161e-124">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b161e-124">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b161e-125"><strong>Konferenz-URI</strong></span><span class="sxs-lookup"><span data-stu-id="b161e-125"><strong>Conference URI</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b161e-p103">Der Konferenz zugewiesener URI. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b161e-p103">URI assigned to the conference. For example:</span></span></p>
<p><span data-ttu-id="b161e-128">sip:kmyer@litwareinc.com;gruu;opaque=app:conf:focus:id:drg2y8v4</span><span class="sxs-lookup"><span data-stu-id="b161e-128">sip:kmyer@litwareinc.com;gruu;opaque=app:conf:focus:id:drg2y8v4</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b161e-129"><strong>Pool-FQDN</strong></span><span class="sxs-lookup"><span data-stu-id="b161e-129"><strong>Pool FQDN</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b161e-130">Vollqualifizierter Domänenname des Registrierungspools oder Edgeservers in einer Sitzung.</span><span class="sxs-lookup"><span data-stu-id="b161e-130">Fully-qualified domain name of the Registrar pool or Edge Server involved in a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b161e-131"><strong>Startzeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="b161e-131"><strong>Start time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b161e-132">Datum und Uhrzeit, an dem bzw. zu der Konferenz begann.</span><span class="sxs-lookup"><span data-stu-id="b161e-132">Date and time that the conference started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b161e-133"><strong>Organisator</strong></span><span class="sxs-lookup"><span data-stu-id="b161e-133"><strong>Organizer</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b161e-134">SIP-Adresse des Benutzers, der die Sitzung organisiert hat.</span><span class="sxs-lookup"><span data-stu-id="b161e-134">SIP address of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b161e-135"><strong>Endzeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="b161e-135"><strong>End time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b161e-136">Datum und Uhrzeit, an dem bzw. zu der die Konferenz endete.</span><span class="sxs-lookup"><span data-stu-id="b161e-136">Date and time that the conference ended.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b161e-137">In der folgenden Tabelle werden die Informationen aus dem Abschnitt zur Konferenzteilnahme des detaillierten Konferenzberichts aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="b161e-137">The following table lists the information provided in the Conference Participation Section of the Conference Detail Report.</span></span>

### <a name="conference-participation-metrics"></a><span data-ttu-id="b161e-138">Konferenzteilnahme – Metriken</span><span class="sxs-lookup"><span data-stu-id="b161e-138">Conference Participation Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b161e-139">Name</span><span class="sxs-lookup"><span data-stu-id="b161e-139">Name</span></span></th>
<th><span data-ttu-id="b161e-140">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="b161e-140">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="b161e-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b161e-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b161e-142"><strong>User</strong></span><span class="sxs-lookup"><span data-stu-id="b161e-142"><strong>User</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b161e-143">SIP-Adresse des Benutzers, der an der Konferenz teilgenommen hat.</span><span class="sxs-lookup"><span data-stu-id="b161e-143">SIP address of the user who participated in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b161e-144"><strong>Rolle</strong></span><span class="sxs-lookup"><span data-stu-id="b161e-144"><strong>Role</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b161e-145">Rolle (z. B. Referent) des Konferenzteilnehmers.</span><span class="sxs-lookup"><span data-stu-id="b161e-145">Role (for example, Presenter) played by the conference participant.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b161e-146"><strong>Verbindung</strong></span><span class="sxs-lookup"><span data-stu-id="b161e-146"><strong>Connectivity</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b161e-147">Netzwerkverbindungen (in der Regel „From Internal“ oder „From External“) des Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="b161e-147">Network connectivity (typically From Internal or From External) for the participant.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b161e-148">Beitrittszeitpunkt</span><span class="sxs-lookup"><span data-stu-id="b161e-148">Join time</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b161e-149">Datum und Uhrzeit, an dem bzw. zu der der Teilnehmer der Konferenz beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b161e-149">Date and time that the participant joined the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b161e-150"><strong>Beendigungszeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="b161e-150"><strong>Leave time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b161e-151">Datum und Uhrzeit, an dem bzw. zu der der Teilnehmer die Konferenz verlassen hat.</span><span class="sxs-lookup"><span data-stu-id="b161e-151">Date and time that the participant left the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b161e-152"><strong>Benutzer-Agent</strong></span><span class="sxs-lookup"><span data-stu-id="b161e-152"><strong>User agent</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b161e-153">ID für die vom Endpunkt des Teilnehmers verwendete Software.</span><span class="sxs-lookup"><span data-stu-id="b161e-153">Identifier for the software used by the participant’s endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b161e-154"><strong>Diagnoseberichte</strong></span><span class="sxs-lookup"><span data-stu-id="b161e-154"><strong>Diagnostic reports</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b161e-p104">Enthält Diagnose- und Problembehandlungsinformationen, einschließlich SIP-Antwortcodes, Diagnoseheader, Zeitpunkt des Konferenzbeitritts und Diagnose-IDs für fehlgeschlagene Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="b161e-p104">Provides diagnostic and troubleshooting information. Including SIP response codes, diagnostic headers, conference join times, and diagnostic IDs for failed sessions.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b161e-157">In der folgenden Tabelle sind die Informationen aufgeführt, die im Abschnitt Konferenz Modalitäten des Konferenz Detail Berichts bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b161e-157">The following table lists the information provided in the Conference Modalities section of the Conference Detail Report.</span></span>

### <a name="conference-modalities-metrics"></a><span data-ttu-id="b161e-158">Konferenzmodalitäten – Metriken</span><span class="sxs-lookup"><span data-stu-id="b161e-158">Conference Modalities Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b161e-159">Name</span><span class="sxs-lookup"><span data-stu-id="b161e-159">Name</span></span></th>
<th><span data-ttu-id="b161e-160">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="b161e-160">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="b161e-161">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b161e-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b161e-162"><strong>User</strong></span><span class="sxs-lookup"><span data-stu-id="b161e-162"><strong>User</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b161e-163">SIP-Adresse des Benutzers, der an der Konferenz teilgenommen hat.</span><span class="sxs-lookup"><span data-stu-id="b161e-163">SIP address of the user who participated in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b161e-164"><strong>Beitrittszeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="b161e-164"><strong>Join time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b161e-165">Datum und Uhrzeit, an dem bzw. zu der der Teilnehmer der Konferenz beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b161e-165">Date and time that the participant joined the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b161e-166"><strong>Beendigungszeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="b161e-166"><strong>Leave time</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b161e-167">Datum und Uhrzeit, an dem bzw. zu der ein Teilnehmer die Konferenz verlassen hat.</span><span class="sxs-lookup"><span data-stu-id="b161e-167">Date and time that a participant left the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b161e-168"><strong>Konferenzserver-URI</strong></span><span class="sxs-lookup"><span data-stu-id="b161e-168"><strong>Conferencing server URI</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b161e-169">URI für den in der Konferenz verwendeten Konferenzserver.</span><span class="sxs-lookup"><span data-stu-id="b161e-169">URI for the Conferencing server used in the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b161e-170"><strong>Diagnoseberichte</strong></span><span class="sxs-lookup"><span data-stu-id="b161e-170"><strong>Diagnostic reports</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b161e-p105">Enthält Diagnose- und Problembehandlungsinformationen, einschließlich SIP-Antwortcodes, Diagnoseheader, Zeitpunkt des Konferenzbeitritts und Diagnose-IDs für fehlgeschlagene Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="b161e-p105">Provides diagnostic and troubleshooting information. Including SIP response codes, diagnostic headers, conference join times, and diagnostic IDs for failed sessions.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b161e-173">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b161e-173">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

