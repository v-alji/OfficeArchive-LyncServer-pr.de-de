---
title: 'Lync Server 2013: Bericht zur Anruf Zulassungs Steuerung'
description: 'Lync Server 2013: Bericht zur Anruf Zulassungs Steuerung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Admission Control Report
ms:assetid: ea4b0c9f-7f93-4b8a-b901-01e1636c44fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615043(v=OCS.15)
ms:contentKeyID: 48185933
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8764e51603e7097095894bc1230c2a2bb1126b9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435782"
---
# <a name="call-admission-control-report-in-lync-server-2013"></a><span data-ttu-id="f9c1f-103">Bericht zur Anruf Zulassungs Steuerung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9c1f-103">Call Admission Control Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f9c1f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f9c1f-104">

<span> </span></span></span>

<span data-ttu-id="f9c1f-105">_**Letztes Änderungsdatum des Themas:** 2012-06-29_</span><span class="sxs-lookup"><span data-stu-id="f9c1f-105">_**Topic Last Modified:** 2012-06-29_</span></span>

<span data-ttu-id="f9c1f-106">Der Bericht über Anrufsteuerung bietet Informationen über Peer-to-Peer- und Konferenzsitzungen, die unter Beschränkungen durchgeführt wurden, die über die Anrufsteuerung eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-106">The Call Admission Control Report provides information about peer-to-peer and conferencing sessions that were conducted under restrictions set in place by Call Admission Control.</span></span> <span data-ttu-id="f9c1f-107">Die in Microsoft lync Server 2010 eingeführte Anruf Zulassungs Steuerung bietet Administratoren die Möglichkeit, Kommunikationssitzungen basierend auf Bandbreiteneinschränkungen zuzulassen (oder nicht zulassen).</span><span class="sxs-lookup"><span data-stu-id="f9c1f-107">Call Admission Control, introduced in Microsoft Lync Server 2010, provides a way for administrators to allow (or not allow) communication sessions based on bandwidth constraints.</span></span> <span data-ttu-id="f9c1f-108">Beispielsweise kann ein Administrator Richtlinien erstellen, die die verfügbare Bandbreite für Sprach- und Videoanrufe beschränken.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-108">For example, administrators can create policies that impose a limit on the amount of bandwidth available for voice and video calls.</span></span> <span data-ttu-id="f9c1f-109">Sobald diese Bandbreitengrenze erreicht ist, können keine neuen Sprach- oder Videoanrufe mehr getätigt werden, bis einer der aktuellen Anrufe beendet worden ist und damit die erforderlichen Netzwerkressourcen freigegeben worden sind.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-109">If that bandwidth limit has been reached, then no new voice or video calls can be placed until one of the current calls has ended and freed up the required network resources.</span></span>

<div>

## <a name="accessing-the-call-admission-control-report"></a><span data-ttu-id="f9c1f-110">Öffnen des Berichts über Anrufsteuerung</span><span class="sxs-lookup"><span data-stu-id="f9c1f-110">Accessing the Call Admission Control Report</span></span>

<span data-ttu-id="f9c1f-p102">Auf den Bericht über Anrufsteuerung greifen Sie über die Startseite für Überwachungsberichte zu. Vom Bericht über Anrufsteuerung aus können Sie einen Drilldown zu einem der folgenden Berichte durchführen:</span><span class="sxs-lookup"><span data-stu-id="f9c1f-p102">The Call Admission Control Report is accessed from the Monitoring Reports home page. From the Call Admission Control Report you can drill down to either of the following reports:</span></span>

  - <span data-ttu-id="f9c1f-113">Konferenzdetailbericht – Zum Öffnen dieses Berichts klicken Sie auf die Metrik „Details“ einer Konferenzsitzung.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-113">Conference Detail Report – To access this report, click the Details metric from a conference session.</span></span>

  - <span data-ttu-id="f9c1f-114">Detailbericht über Peer-to-Peer-Sitzungen – Zum Öffnen dieses Berichts klicken Sie auf die Metrik „Details“ für eine Peer-to-Peer-Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-114">Peer-to-Peer Session Detail Report – To access this report, click the Details metric for a peer-to-peer session.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-admission-control-report"></a><span data-ttu-id="f9c1f-115">Optimales Nutzen des Berichts über Anrufsteuerung</span><span class="sxs-lookup"><span data-stu-id="f9c1f-115">Making the Best Use of the Call Admission Control Report</span></span>

<span data-ttu-id="f9c1f-p103">Zum Abrufen einer Liste der Anrufe, bei denen wegen nicht ausreichender Bandbreite ein Fehler auftrat, wählen Sie in der Dropdownliste „Anrufkategorie“ den Eintrag „Anrufe, die aufgrund der Anrufsteuerung abgelehnt werden“ aus. Die meisten der zurückgegebenen Anrufe haben wahrscheinlich die Diagnose-ID 5:</span><span class="sxs-lookup"><span data-stu-id="f9c1f-p103">To get a list of calls that failed because of insufficient bandwidth, select Calls rejected because of call admission control from the Call category dropdown list. Most of the returned calls will likely have a diagnostic ID of 5:</span></span>

<span data-ttu-id="f9c1f-p104">Nicht genügend Bandbreite zum Herstellen der Sitzung. PSTN-Umleitung wird versucht.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-p104">Insufficient bandwidth to establish session. Attempt PSTN re-route.</span></span>

<span data-ttu-id="f9c1f-120">Dies weist darauf hin, dass Beschränkungen der Anrufsteuerung verhindert haben, dass der Anruf im VoIP-Netzwerk ausgeführt werden konnte.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-120">That indicates that Call Admission Control limitations were preventing the call from being made on the VoIP network.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="f9c1f-121">Filter</span><span class="sxs-lookup"><span data-stu-id="f9c1f-121">Filters</span></span>

<span data-ttu-id="f9c1f-p105">Mithilfe von Filtern können Sie eine gezieltere Datenauswahl zurückgeben oder die zurückgegebenen Daten auf unterschiedliche Weise anzeigen. Der Anrufsteuerungsbericht ermöglicht Ihnen beispielsweise das Filtern von Anrufen nach dem Benutzer, der den Anruf initiiert hat oder nach dem angerufenen Benutzer. Sie können außerdem festlegen, wie Daten gruppiert werden sollen. In diesem Fall werden die Anrufe nach Stunde, Tag, Woche oder Monat zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-p105">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Call Admission Control Report enables you to filter calls by the user who initiated the call or by the user who was being called. You can also choose how data should be grouped. In this case, calls are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="f9c1f-126">In der folgenden Tabelle werden die Filter aufgelistet, die Sie im Anrufsteuerungsbericht verwenden können.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-126">The following table lists the filters that you can use with the Call Admission Control Report.</span></span>

### <a name="call-admission-control-report-filters"></a><span data-ttu-id="f9c1f-127">Anrufsteuerungsbericht - Filter</span><span class="sxs-lookup"><span data-stu-id="f9c1f-127">Call Admission Control Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9c1f-128">Name</span><span class="sxs-lookup"><span data-stu-id="f9c1f-128">Name</span></span></th>
<th><span data-ttu-id="f9c1f-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9c1f-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9c1f-130"><strong>Von</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-130"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-p106">Anfangsdatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Anfangsdatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="f9c1f-p106">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="f9c1f-133">7/17/12012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="f9c1f-133">7/17/12012 1:00 PM</span></span></p>
<p><span data-ttu-id="f9c1f-p107">Wenn Sie keinen Anfangszeitpunkt eingeben, beginnt der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="f9c1f-p107">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="f9c1f-136">7/17/12012</span><span class="sxs-lookup"><span data-stu-id="f9c1f-136">7/17/12012</span></span></p>
<p><span data-ttu-id="f9c1f-137">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="f9c1f-137">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="f9c1f-138">7/13/2012</span><span class="sxs-lookup"><span data-stu-id="f9c1f-138">7/13/2012</span></span></p>
<p><span data-ttu-id="f9c1f-139">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-139">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c1f-140"><strong>Bis</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-140"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-p108">Enddatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Enddatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="f9c1f-p108">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="f9c1f-143">7/17/12012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="f9c1f-143">7/17/12012 1:00 PM</span></span></p>
<p><span data-ttu-id="f9c1f-p109">Wenn Sie keinen Endzeitpunkt eingeben, endet der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="f9c1f-p109">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="f9c1f-146">7/17/12012</span><span class="sxs-lookup"><span data-stu-id="f9c1f-146">7/17/12012</span></span></p>
<p><span data-ttu-id="f9c1f-147">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="f9c1f-147">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="f9c1f-148">7/13/2012</span><span class="sxs-lookup"><span data-stu-id="f9c1f-148">7/13/2012</span></span></p>
<p><span data-ttu-id="f9c1f-149">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-149">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c1f-150"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-150"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-p110">Vollqualifizierter Domänenname (FQDN) des Registrierungspools oder Edgeservers. Sie können einen einzelnen Pool auswählen oder auf <strong>[Alle]</strong> klicken, um die Daten für alle Pools anzuzeigen. Diese Dropdownliste wird basierend auf den Datensätzen in der Datenbank automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-p110">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c1f-154"><strong>Aktivitätstyp</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-154"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-p111">Aktivitätstyp. Wählen Sie eine der folgenden Aktivitäten aus:</span><span class="sxs-lookup"><span data-stu-id="f9c1f-p111">Type of activity. Select one of the following activities:</span></span></p>
<ul>
<li><p><span data-ttu-id="f9c1f-157">[Alle]</span><span class="sxs-lookup"><span data-stu-id="f9c1f-157">[All]</span></span></p></li>
<li><p><span data-ttu-id="f9c1f-158">Peer-to-Peer</span><span class="sxs-lookup"><span data-stu-id="f9c1f-158">Peer-to-Peer</span></span></p></li>
<li><p><span data-ttu-id="f9c1f-159">Konferenz</span><span class="sxs-lookup"><span data-stu-id="f9c1f-159">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c1f-160"><strong>Anrufkategorie</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-160"><strong>Call category</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-p112">Gibt den Grund für die Verwendung der Anrufsteuerung bei einem Anruf an. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="f9c1f-p112">Indicates the reason that CAC was used for the call. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="f9c1f-163">[Alle]</span><span class="sxs-lookup"><span data-stu-id="f9c1f-163">[All]</span></span></p></li>
<li><p><span data-ttu-id="f9c1f-164">Anruf durch Anrufsteuerung abgelehnt</span><span class="sxs-lookup"><span data-stu-id="f9c1f-164">Call rejected because of call admission control</span></span></p></li>
<li><p><span data-ttu-id="f9c1f-165">Anrufe durch Anrufsteuerung über PSTN umgeleitet</span><span class="sxs-lookup"><span data-stu-id="f9c1f-165">Calls rerouted through PSTN because of call admission control</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="f9c1f-166">Metriken für Peer-to-Peer-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="f9c1f-166">Metrics for Peer-to-Peer Sessions</span></span>

<span data-ttu-id="f9c1f-167">In der folgenden Tabelle sind die im Anrufsteuerungsbericht für Peer-to-Peer-Sitzungen (d. h. Sitzungen mit nur zwei Teilnehmern) enthaltenen Informationen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-167">The following table lists the information provided in the Call Admission Control Report for peer-to-peer sessions (that is, sessions involving just two participants).</span></span>

### <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="f9c1f-168">Metriken für Peer-to-Peer-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="f9c1f-168">Metrics for Peer-to-Peer Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9c1f-169">Name</span><span class="sxs-lookup"><span data-stu-id="f9c1f-169">Name</span></span></th>
<th><span data-ttu-id="f9c1f-170">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="f9c1f-170">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="f9c1f-171">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9c1f-171">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9c1f-172"><strong>Detail</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-172"><strong>Detail</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-173">Nein</span><span class="sxs-lookup"><span data-stu-id="f9c1f-173">No</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-174">Wenn Sie auf dieses Element klicken, zeigt der Bericht einen detaillierten Peer-to-Peer-Sitzungsbericht für die angegebene Sitzung an.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-174">When you click this item, the report shows you a Peer-to-Peer Session Detail Report for the specified session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c1f-175"><strong>Absenderbenutzer</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-175"><strong>From user</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-176">Ja</span><span class="sxs-lookup"><span data-stu-id="f9c1f-176">Yes</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-177">SIP-Adresse des Benutzers, der die Sitzung initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-177">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c1f-178"><strong>An Benutzer</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-178"><strong>To user</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-179">Ja</span><span class="sxs-lookup"><span data-stu-id="f9c1f-179">Yes</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-180">SIP-Adresse des Benutzers, der zur Teilnahme an der Sitzung eingeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-180">SIP address of the user who was invited to join the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c1f-181"><strong>Modalitäten</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-181"><strong>Modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-182">Ja</span><span class="sxs-lookup"><span data-stu-id="f9c1f-182">Yes</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-183">Kommunikationsmodalitäten (z. B. Audio und Video), die bei der Sitzung verwendet wurden.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-183">Communication modalities (such as audio and video) that were used during the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c1f-184"><strong>Einladungszeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-184"><strong>Invite time</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-185">Ja</span><span class="sxs-lookup"><span data-stu-id="f9c1f-185">Yes</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-186">Datum und Uhrzeit, an dem bzw. zu der die ursprüngliche Sitzungseinladung an den Benutzer gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-186">Date and time the initial session invitation was sent to the From user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c1f-187"><strong>Antwortzeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-187"><strong>Response time</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-188">Ja</span><span class="sxs-lookup"><span data-stu-id="f9c1f-188">Yes</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-189">Datum und Uhrzeit, an dem bzw. zu der die Annahme der Einladung empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-189">Date and time that the invitation acceptance was received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c1f-190"><strong>Endzeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-190"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-191">Ja</span><span class="sxs-lookup"><span data-stu-id="f9c1f-191">Yes</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-192">Datum und Uhrzeit, an dem bzw. zu der die Sitzung endete.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-192">Date and time that the session ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c1f-193"><strong>Diagnose-ID</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-193"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-194">Ja</span><span class="sxs-lookup"><span data-stu-id="f9c1f-194">Yes</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-p113">Eindeutige ID (in der Form eines Headers vom Typ „ms-diagnostics“), die an eine SIP-Nachricht angehängt wird und oft nützliche Informationen für die Fehlerbehebung bereitstellt. Diagnostics-Header sind optional (SIP-Sitzungen ohne diese Header sind möglich) und Diagnose-IDs werden nur für Sitzungen berichtet, bei denen Probleme aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-p113">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="f9c1f-197">Metriken für Konferenzsitzungen</span><span class="sxs-lookup"><span data-stu-id="f9c1f-197">Metrics for Conferencing Sessions</span></span>

<span data-ttu-id="f9c1f-198">In der folgenden Tabelle sind die im Anrufsteuerungsbericht für Konferenzsitzungen (d. h. Sitzungen mit mindestens drei Teilnehmern) enthaltenen Informationen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-198">The following table lists the information provided in the Call Admission Control Report for conferencing sessions (that is, sessions involving three or more participants).</span></span>

### <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="f9c1f-199">Metriken für Konferenzsitzungen</span><span class="sxs-lookup"><span data-stu-id="f9c1f-199">Metrics for Conferencing Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9c1f-200">Name</span><span class="sxs-lookup"><span data-stu-id="f9c1f-200">Name</span></span></th>
<th><span data-ttu-id="f9c1f-201">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="f9c1f-201">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="f9c1f-202">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9c1f-202">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9c1f-203"><strong>Konferenz-URI</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-203"><strong>Conference URI</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-204">Ja</span><span class="sxs-lookup"><span data-stu-id="f9c1f-204">Yes</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-p114">Eindeutige ID für die Konferenz. Wenn Sie auf dieses Element klicken, zeigt der Bericht die einzelnen Konferenzteilnehmer an.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-p114">Unique identifier for the conference. When you click this item, the report shows the individual conference participants.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c1f-207"><strong>Organisator</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-207"><strong>Organizer</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-208">Ja</span><span class="sxs-lookup"><span data-stu-id="f9c1f-208">Yes</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-209">SIP-Adresse des Benutzers, der die Sitzung organisiert hat.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-209">SIP address of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c1f-210"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-210"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-211">Ja</span><span class="sxs-lookup"><span data-stu-id="f9c1f-211">Yes</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-212">In der Konferenz verwendeter Edgeserver.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-212">Edge Server used in the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c1f-213"><strong>Startzeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-213"><strong>Start time</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-214">Ja</span><span class="sxs-lookup"><span data-stu-id="f9c1f-214">Yes</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-215">Datum und Uhrzeit, an dem bzw. zu der Konferenz begann.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-215">Date and time that the conference started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c1f-216"><strong>Endzeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-216"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-217">Ja</span><span class="sxs-lookup"><span data-stu-id="f9c1f-217">Yes</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-218">Datum und Uhrzeit, an dem bzw. zu der die Konferenz endete.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-218">Date and time that the conference ended.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-individual-conference-participants"></a><span data-ttu-id="f9c1f-219">Metriken für einzelne Konferenzteilnehmer</span><span class="sxs-lookup"><span data-stu-id="f9c1f-219">Metrics for Individual Conference Participants</span></span>

<span data-ttu-id="f9c1f-220">In der folgenden Tabelle sind die im Anrufsteuerungsbericht für einzelne Konferenzteilnehmer enthaltenen Informationen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-220">The following table lists the information provided in the Call Admission Control Report for individual conference participants.</span></span>

### <a name="metrics-for-individual-conference-participants"></a><span data-ttu-id="f9c1f-221">Metriken für einzelne Konferenzteilnehmer</span><span class="sxs-lookup"><span data-stu-id="f9c1f-221">Metrics for Individual Conference Participants</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f9c1f-222">Name</span><span class="sxs-lookup"><span data-stu-id="f9c1f-222">Name</span></span></th>
<th><span data-ttu-id="f9c1f-223">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="f9c1f-223">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="f9c1f-224">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f9c1f-224">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9c1f-225"><strong>Rolle</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-225"><strong>Role</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-226">Nein</span><span class="sxs-lookup"><span data-stu-id="f9c1f-226">No</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-227">Rolle (z. B. Referent) des Konferenzteilnehmers.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-227">Role (for example, Presenter) played by the conference participant.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c1f-228"><strong>Teilnehmer</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-228"><strong>Participant</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-229">Nein</span><span class="sxs-lookup"><span data-stu-id="f9c1f-229">No</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-230">SIP-Adresse des Konferenzteilnehmers.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-230">SIP address of the conference participant.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c1f-231"><strong>Verbindung</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-231"><strong>Connectivity</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-232">Nein</span><span class="sxs-lookup"><span data-stu-id="f9c1f-232">No</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-233">Netzwerkverbindungen (in der Regel „From Internal“ oder „From External“) des Teilnehmers.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-233">Network connectivity (typically From Internal or From External) for the participant.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c1f-234"><strong>Modalität</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-234"><strong>Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-235">Nein</span><span class="sxs-lookup"><span data-stu-id="f9c1f-235">No</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-236">Konferenztyp (z. B. A/V-Konferenzen).</span><span class="sxs-lookup"><span data-stu-id="f9c1f-236">Conference type (for example, A/V conferencing).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c1f-237"><strong>Beitrittszeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-237"><strong>Join time</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-238">Nein</span><span class="sxs-lookup"><span data-stu-id="f9c1f-238">No</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-239">Datum und Uhrzeit, an dem bzw. zu der der Teilnehmer der Konferenz beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-239">Date and time that the participant joined the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9c1f-240"><strong>Beendigungszeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-240"><strong>Leave time</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-241">Nein</span><span class="sxs-lookup"><span data-stu-id="f9c1f-241">No</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-242">Datum und Uhrzeit, an dem bzw. zu der der Teilnehmer die Konferenz verlassen hat.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-242">Date and time that the participant left the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9c1f-243"><strong>Diagnose-ID</strong></span><span class="sxs-lookup"><span data-stu-id="f9c1f-243"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="f9c1f-244">Nein</span><span class="sxs-lookup"><span data-stu-id="f9c1f-244">No</span></span></p></td>
<td><p><span data-ttu-id="f9c1f-p115">Eindeutige ID (in der Form eines Headers vom Typ „ms-diagnostics“), die an eine SIP-Nachricht angehängt wird und oft nützliche Informationen für die Fehlerbehebung bereitstellt. Diagnostics-Header sind optional (SIP-Sitzungen ohne diese Header sind möglich) und Diagnose-IDs werden nur für Sitzungen berichtet, bei denen Probleme aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="f9c1f-p115">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f9c1f-247">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f9c1f-247">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

