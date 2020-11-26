---
title: 'Lync Server 2013: Peer-to-Peer-Sitzungs Detail Bericht'
description: 'Lync Server 2013: Peer-to-Peer-Sitzungs Detail Bericht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Peer-to-Peer Session Detail Report
ms:assetid: 6be1d676-68f7-4a53-a72a-de73296c5571
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558659(v=OCS.15)
ms:contentKeyID: 48184416
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e712225fddabb646cc3b862f59601857a7df8eff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445036"
---
# <a name="peer-to-peer-session-detail-report-in-lync-server-2013"></a><span data-ttu-id="431a1-103">Peer-zu-Peer-Sitzungs Detail Bericht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="431a1-103">Peer-to-Peer Session Detail Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="431a1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="431a1-104">

<span> </span></span></span>

<span data-ttu-id="431a1-105">_**Letztes Änderungsdatum des Themas:** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="431a1-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="431a1-p101">Der Detailbericht über Peer-to-Peer-Sitzungen gibt detaillierte Informationen über eine Peer-to-Peer-Sitzung zurück. Wenn Sie beispielsweise eine Sofortnachrichtensitzung auswählen, gibt der Bericht Ihnen die Anzahl an Nachrichten an, die jeweils von den beiden an der Sitzung beteiligten Benutzern gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="431a1-p101">The Peer-to-Peer Session Detail Report returns detailed information about a peer-to-peer session. For example, if you select an instant messaging session, the report will tell you the number of messages sent by each of the two users in the session.</span></span>

<div>

## <a name="accessing-the-peer-to-peer-session-detail-report"></a><span data-ttu-id="431a1-108">Zugriff auf den Detailbericht über Peer-to-Peer-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="431a1-108">Accessing the Peer-to-Peer Session Detail Report</span></span>

<span data-ttu-id="431a1-109">Sie können über die folgenden Berichte (die alle über die Startseite für Überwachungsberichte aufgerufen werden können) auf den Detailbericht über Peer-to-Peer-Sitzungen zugreifen:</span><span class="sxs-lookup"><span data-stu-id="431a1-109">The Peer-to-Peer Session Detail Report can be accessed from any of the following reports (all of which can be accessed from the Monitoring Reports home page):</span></span>

  - <span data-ttu-id="431a1-110">Inventurbericht über IP-Telefone</span><span class="sxs-lookup"><span data-stu-id="431a1-110">IP Phone Inventory Report</span></span>

  - <span data-ttu-id="431a1-111">Bericht über Benutzeraktivität</span><span class="sxs-lookup"><span data-stu-id="431a1-111">User Activity Report</span></span>

  - <span data-ttu-id="431a1-112">Bericht über Anrufsteuerung</span><span class="sxs-lookup"><span data-stu-id="431a1-112">Call Admission Control Report</span></span>

  - <span data-ttu-id="431a1-113">Fehlerlistenbericht</span><span class="sxs-lookup"><span data-stu-id="431a1-113">Failure List Report</span></span>

<span data-ttu-id="431a1-114">Im Bericht Peer-to-Peer-Sitzungsdetails können Sie auf den [Diagnosebericht in lync Server 2013](lync-server-2013-diagnostic-report.md) zugreifen, indem Sie auf die Metrik für den Diagnosebericht (Details) klicken.</span><span class="sxs-lookup"><span data-stu-id="431a1-114">From within the Peer-to-Peer Session Detail Report you can access the [Diagnostic Report in Lync Server 2013](lync-server-2013-diagnostic-report.md) by clicking the Diagnostic Report (Details) metric.</span></span> <span data-ttu-id="431a1-115">Sie können zudem auf den Bericht über häufigste Fehler zugreifen, indem Sie auf eine der folgenden beiden Metriken klicken:</span><span class="sxs-lookup"><span data-stu-id="431a1-115">You can also access the Top Failures Report by clicking either of these two metrics:</span></span>

  - <span data-ttu-id="431a1-116">Reaktion</span><span class="sxs-lookup"><span data-stu-id="431a1-116">Response</span></span>

  - <span data-ttu-id="431a1-117">Diagnose-ID</span><span class="sxs-lookup"><span data-stu-id="431a1-117">Diagnostic ID</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-peer-to-peer-session-detail-report"></a><span data-ttu-id="431a1-118">Optimale Verwendung des Detailberichts über Peer-to-Peer-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="431a1-118">Making the Best Use of the Peer-to-Peer session Detail Report</span></span>

<span data-ttu-id="431a1-p103">Der Detailbericht über Peer-to-Peer-Sitzungen enthält zahlreiche Metriken, mit denen die Systemadministratoren möglicherweise zum Teil nicht vertraut sind. Häufig können Sie jedoch ein Tooltip mit einer kurzen Beschreibung der Metrik anzeigen, indem Sie den Mauszeiger über die Bezeichnung der jeweiligen Metrik bewegen.</span><span class="sxs-lookup"><span data-stu-id="431a1-p103">The Peer-to-Peer Session Detail Report includes a large number of metrics, many of which might not be familiar to system administrators. Often-times, however, you can view a tooltip that offers a brief description of that metric simply by holding your mouse over the metric label.</span></span>

<span data-ttu-id="431a1-p104">Beachten Sie, dass die tatsächlichen Metriken, die in einem bestimmten Bericht angezeigt werden, von der ausgewählten Peer-to-Peer-Sitzung abhängen. So wird für eine Audio-/Videositzung ein anderer Satz an Metriken ausgegeben als für eine Sofortnachrichtensitzung.</span><span class="sxs-lookup"><span data-stu-id="431a1-p104">Note that the actual metrics shown on a given report will depend on the type of peer-to-peer session you selected. An audio/video session will report a different set of metrics than an instant messaging session.</span></span>

<span data-ttu-id="431a1-123">Sie können den Mauszeiger auch über die Antwortcode- und Diagnose-ID-Metriken bewegen, um eine Beschreibung der folgenden Werte anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="431a1-123">You can also hold your mouse over the Response code and Diagnostic ID metrics in order to obtain a description of those values:</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="431a1-124">Filter</span><span class="sxs-lookup"><span data-stu-id="431a1-124">Filters</span></span>

<span data-ttu-id="431a1-p105">Keine. Der Detailbericht über Peer-to-Peer-Sitzungen kann nicht gefiltert werden.</span><span class="sxs-lookup"><span data-stu-id="431a1-p105">None. You cannot filter the Peer-to-Peer Session Detail Report.</span></span>

</div>

<div>

## <a name="session-information-metrics"></a><span data-ttu-id="431a1-127">Sitzungsinformationen - Metriken</span><span class="sxs-lookup"><span data-stu-id="431a1-127">Session Information Metrics</span></span>

<span data-ttu-id="431a1-128">In der folgenden Tabelle sind die Informationen aufgelistet, die im Detailbericht über Peer-to-Peer-Sitzungen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="431a1-128">The following table lists the information provided in the Peer-to-Peer Session Detail Report for each session.</span></span>

### <a name="session-information-metrics"></a><span data-ttu-id="431a1-129">Sitzungsinformationen - Metriken</span><span class="sxs-lookup"><span data-stu-id="431a1-129">Session Information Metrics</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="431a1-130">Name</span><span class="sxs-lookup"><span data-stu-id="431a1-130">Name</span></span></th>
<th><span data-ttu-id="431a1-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="431a1-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="431a1-132"><strong>Pool-FQDN</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-132"><strong>Pool FQDN</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-133">Vollqualifizierter Domänenname (FQDN) des Registrar-Pools oder Edgeservers in der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="431a1-133">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server involved in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a1-134"><strong>Einladungszeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-134"><strong>Invite time</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-135">Datum und Uhrzeit, an dem bzw. zu der die Sitzungseinladung ursprünglich gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="431a1-135">Date and time the session invitation was originally sent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a1-136"><strong>Antwortzeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-136"><strong>Response time</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-137">Datum und Uhrzeit, an dem bzw. zu der die Annahme der Einladung empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="431a1-137">Date and time that the invitation acceptance was received.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a1-138"><strong>Absenderbenutzer</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-138"><strong>From user</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-139">SIP-Adresse des Benutzers, der die Sitzung initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="431a1-139">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a1-140"><strong>Von Benutzeragent</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-140"><strong>From user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-141">Software, die vom Endpunkt des Benutzers, der die Sitzung initiiert hat, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="431a1-141">Software used by the endpoint of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a1-142"><strong>Interner Absenderbenutzer</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-142"><strong>Is From user internal</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-143">Gibt an, ob der Benutzer, der die Sitzung initiiert hat, am internen Netzwerk angemeldet war.</span><span class="sxs-lookup"><span data-stu-id="431a1-143">Indicates whether the user who initiated the session was logged on to the internal network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a1-144"><strong>Absenderbenutzer mit Telefonapparat</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-144"><strong>Is From user integrated with desk phone</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-145">Gibt an, ob der Endpunkt des Benutzers, der die Sitzung initiiert hat, mit seinem Desktoptelefon integriert ist.</span><span class="sxs-lookup"><span data-stu-id="431a1-145">Indicates whether the endpoint used by the user who initiated the session is integrated with his or her desktop phone.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a1-146"><strong>Sitzungspriorität</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-146"><strong>Session Priority</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-p106">Die der Sitzung zugewiesene Priorität. Gültige Prioritäten sind „Unbekannt“, „Nicht dringend“, „Normal“, „Dringend“ und „Notfall“.</span><span class="sxs-lookup"><span data-stu-id="431a1-p106">Priority assigned to the session. Valid priorities are: Unknown; Non-Urgent; Normal; Urgent; and Emergency.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a1-149"><strong>Antwortcode</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-149"><strong>Response code</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-150">SIP-Antwortcode, der bei einem Sitzungsfehler gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="431a1-150">SIP response code sent when the session failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a1-151"><strong>Front-End</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-151"><strong>Front end</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-152">Name des in der Konferenz verwendeten Front-End-Servers.</span><span class="sxs-lookup"><span data-stu-id="431a1-152">Name of the Front End Server used in the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a1-153"><strong>Erfassungszeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-153"><strong>Capture time</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-154">Datum und Uhrzeit, an dem bzw. zu der die Sitzungsinformationen erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="431a1-154">Date and time that the session information was recorded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a1-155"><strong>Endzeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-155"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-156">Datum und Uhrzeit, an dem bzw. zu der die Sitzung endete.</span><span class="sxs-lookup"><span data-stu-id="431a1-156">Date and time the session ended.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a1-157"><strong>An Benutzer</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-157"><strong>To user</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-158">SIP-Adresse des Benutzers, der zur Sitzung eingeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="431a1-158">SIP address of the user who was invited to the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a1-159"><strong>Empfängerbenutzeragent</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-159"><strong>To user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-160">Die vom Endpunkt des Benutzers verwendete Software, der zur Teilnahme an der Sitzung eingeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="431a1-160">Software used by the endpoint of the user who was invited to the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a1-161"><strong>Interner Empfängerbenutzer</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-161"><strong>Is To user internal</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-162">Gibt an, ob der Benutzer, der zur Teilnahme an der Sitzung eingeladen wurde, am internen Netzwerk angemeldet war.</span><span class="sxs-lookup"><span data-stu-id="431a1-162">Indicates whether the user who was invited to the session was logged on to the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a1-163"><strong>Empfängerbenutzer mit Telefonapparat</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-163"><strong>Is To user integrated with desk phone</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-164">Gibt an, ob der Endpunkt des Benutzers, der zur Teilnahme an der Sitzung eingeladen wurde, mit seinem Desktoptelefon integriert ist.</span><span class="sxs-lookup"><span data-stu-id="431a1-164">Indicates whether the endpoint used by the user who was invited to the session is integrated with his or her desktop phone.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a1-165"><strong>Wiederholungsversuch der Sitzung</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-165"><strong>Is retried session</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-166">Gibt an, ob die Sitzung ein Wiederholungsversuch einer zuvor fehlgeschlagenen Sitzung ist.</span><span class="sxs-lookup"><span data-stu-id="431a1-166">Indicates whether the session is an attempt to retry a session that previously failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a1-167"><strong>Diagnose-ID</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-167"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-p107">Eindeutige ID (in der Form eines Headers vom Typ „ms-diagnostics“), die an eine SIP-Nachricht angehängt wird und oft nützliche Informationen für die Fehlerbehebung bereitstellt. Halten Sie den Mauszeiger über die ID-Nummer, um zusätzliche Information zu dieser ID anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="431a1-p107">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Hold the mouse over the ID number to view additional information about that ID.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-modalities"></a><span data-ttu-id="431a1-170">Metriken für Modalitäten</span><span class="sxs-lookup"><span data-stu-id="431a1-170">Metrics for Modalities</span></span>

<span data-ttu-id="431a1-171">In der folgenden Tabelle sind die Informationen aufgelistet, die im Detailbericht über Peer-to-Peer-Sitzungen zu jeder Sitzungsmodalität angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="431a1-171">The following table lists the information provided in the Peer-to-Peer Session Detail Report for each session modality.</span></span>

### <a name="metrics-for-modalities"></a><span data-ttu-id="431a1-172">Metriken für Modalitäten</span><span class="sxs-lookup"><span data-stu-id="431a1-172">Metrics for Modalities</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="431a1-173">Name</span><span class="sxs-lookup"><span data-stu-id="431a1-173">Name</span></span></th>
<th><span data-ttu-id="431a1-174">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="431a1-174">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="431a1-175">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="431a1-175">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="431a1-176"><strong>Modalitäten</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-176"><strong>Modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-177">Nein</span><span class="sxs-lookup"><span data-stu-id="431a1-177">No</span></span></p></td>
<td><p><span data-ttu-id="431a1-p108">In der Sitzung verwendete Modalitäten, z. B. Chat, Audio oder Dateiübertragung.</span><span class="sxs-lookup"><span data-stu-id="431a1-p108">Modalities used in the session. For example, instant messaging (IM) or file transfer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a1-180"><strong>Nachrichten von Absenderbenutzer</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-180"><strong>From user messages</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-181">Nein</span><span class="sxs-lookup"><span data-stu-id="431a1-181">No</span></span></p></td>
<td><p><span data-ttu-id="431a1-182">Anzahl der gesendeten Nachrichten des Benutzers, der die Sitzung initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="431a1-182">Number of messages sent by the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a1-183"><strong>Nachrichten an Empfängerbenutzer</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-183"><strong>To user messages</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-184">Nein</span><span class="sxs-lookup"><span data-stu-id="431a1-184">No</span></span></p></td>
<td><p><span data-ttu-id="431a1-185">Anzahl der gesendeten Nachrichten des Benutzers, der zur Teilnahme an der Sitzung eingeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="431a1-185">Number of messages sent by the user who was invited to join the session.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-diagnostic-reports"></a><span data-ttu-id="431a1-186">Metriken für Diagnoseberichte</span><span class="sxs-lookup"><span data-stu-id="431a1-186">Metrics for Diagnostic Reports</span></span>

<span data-ttu-id="431a1-187">In der folgenden Tabelle sind die Informationen aufgelistet, die im Detailbericht über Peer-to-Peer-Sitzungen zu jeden Diagnosebericht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="431a1-187">The following table lists the information provided in the Peer-to-Peer Session Detail Report for each diagnostic report.</span></span>

### <a name="metrics-for-diagnostic-reports"></a><span data-ttu-id="431a1-188">Metriken für Diagnoseberichte</span><span class="sxs-lookup"><span data-stu-id="431a1-188">Metrics for Diagnostic Reports</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="431a1-189">Name</span><span class="sxs-lookup"><span data-stu-id="431a1-189">Name</span></span></th>
<th><span data-ttu-id="431a1-190">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="431a1-190">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="431a1-191">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="431a1-191">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="431a1-192"><strong>Detail</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-192"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-193">Nein</span><span class="sxs-lookup"><span data-stu-id="431a1-193">No</span></span></p></td>
<td><p><span data-ttu-id="431a1-194">Klicken Sie auf dieses Element, um den Diagnosebericht für die Sitzung anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="431a1-194">When you click this item, the report shows the Diagnostic Report for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a1-195"><strong>Berichtszeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-195"><strong>Report time</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-196">Nein</span><span class="sxs-lookup"><span data-stu-id="431a1-196">No</span></span></p></td>
<td><p><span data-ttu-id="431a1-197">Datum und Uhrzeit der Aufzeichnung des Berichts.</span><span class="sxs-lookup"><span data-stu-id="431a1-197">Date and time the report was recorded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a1-198"><strong>Anforderung</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-198"><strong>Request</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-199">Nein</span><span class="sxs-lookup"><span data-stu-id="431a1-199">No</span></span></p></td>
<td><p><span data-ttu-id="431a1-p109">SIP-Anforderungstyp, z. B. INVITE oder BYE.</span><span class="sxs-lookup"><span data-stu-id="431a1-p109">SIP request type. For example, INVITE or BYE.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a1-202"><strong>Diagnose-ID</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-202"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-203">Nein</span><span class="sxs-lookup"><span data-stu-id="431a1-203">No</span></span></p></td>
<td><p><span data-ttu-id="431a1-204">Eindeutige ID (in der Form eines Headers vom Typ „ms-diagnostics“), die an eine SIP-Nachricht angehängt wird und oft nützliche Informationen für die Fehlerbehebung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="431a1-204">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="431a1-205"><strong>Inhaltstyp</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-205"><strong>Content type</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-206">Nein</span><span class="sxs-lookup"><span data-stu-id="431a1-206">No</span></span></p></td>
<td><p><span data-ttu-id="431a1-p110">In der Konferenz verwendeter Medieninhaltstyp. Ein gängiger Inhaltstyp ist beispielsweise „Application/sdp“. SDP (Session Description Protocol) ist ein Standardinternetprotokoll, das für Sitzungsankündigungen, Sitzungseinladungen und andere Formen des Multimediasitzungsaufbaus verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="431a1-p110">Type of media content used in the conference. For example, a common content type is Application/sdp. Session Description Protocol (SDP) is a standard Internet protocol used for session announcements, session invitations, and other forms of multimedia session initiation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="431a1-210"><strong>Berichtet von</strong></span><span class="sxs-lookup"><span data-stu-id="431a1-210"><strong>Reported by</strong></span></span></p></td>
<td><p><span data-ttu-id="431a1-211">Nein</span><span class="sxs-lookup"><span data-stu-id="431a1-211">No</span></span></p></td>
<td><p><span data-ttu-id="431a1-212">Computer (d. h. Client oder Server), der das Problem berichtet hat.</span><span class="sxs-lookup"><span data-stu-id="431a1-212">Computer (that is, client or server) that reported the problem.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="431a1-213">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="431a1-213">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

