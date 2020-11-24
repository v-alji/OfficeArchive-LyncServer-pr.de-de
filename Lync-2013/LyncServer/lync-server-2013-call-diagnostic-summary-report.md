---
title: 'Lync Server 2013: Anruf Diagnose Zusammenfassungsbericht'
description: 'Lync Server 2013: Anruf Diagnose Zusammenfassungsbericht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Diagnostic Summary Report
ms:assetid: 9091de56-13e6-440e-9353-f57c10c906fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615016(v=OCS.15)
ms:contentKeyID: 48184789
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b444a176c06974a9eb9827006e078c17b54047a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393858"
---
# <a name="call-diagnostic-summary-report-in-lync-server-2013"></a><span data-ttu-id="e5690-103">Anruf Diagnose Zusammenfassungsbericht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e5690-103">Call Diagnostic Summary Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e5690-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e5690-104">

<span> </span></span></span>

<span data-ttu-id="e5690-105">_**Letztes Änderungsdatum des Themas:** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="e5690-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="e5690-p101">Der zusammenfassende Anrufdiagnosebericht bietet eine Gesamtübersicht zu fehlgeschlagenen Peer-to-Peer- und Konferenzsitzungen. Der Bericht zeigt die Gesamtfehlerrate für beide Sitzungstypen und detaillierte Fehlerinformationen nach Sitzungsmodalitätstyp:</span><span class="sxs-lookup"><span data-stu-id="e5690-p101">The Call Diagnostic Summary Report provides an overall look at failed peer-to-peer and conferencing sessions. The report shows the overall failure rate for both types of sessions, and further breaks the failure information down by session modality type:</span></span>

  - <span data-ttu-id="e5690-108">Sofortnachrichten</span><span class="sxs-lookup"><span data-stu-id="e5690-108">Instant messaging</span></span>

  - <span data-ttu-id="e5690-109">Anwendungsfreigabe</span><span class="sxs-lookup"><span data-stu-id="e5690-109">Application sharing</span></span>

  - <span data-ttu-id="e5690-110">Dateiübertragung</span><span class="sxs-lookup"><span data-stu-id="e5690-110">File transfer</span></span>

  - <span data-ttu-id="e5690-111">Audio</span><span class="sxs-lookup"><span data-stu-id="e5690-111">Audio</span></span>

  - <span data-ttu-id="e5690-112">Video</span><span class="sxs-lookup"><span data-stu-id="e5690-112">Video</span></span>

<div>

## <a name="accessing-the-call-diagnostic-summary-report"></a><span data-ttu-id="e5690-113">Zugriff auf den zusammenfassenden Anrufdiagnosebericht</span><span class="sxs-lookup"><span data-stu-id="e5690-113">Accessing the Call Diagnostic Summary Report</span></span>

<span data-ttu-id="e5690-114">Der Zugriff auf den zusammenfassenden Anrufdiagnosebericht erfolgt auf der Startseite für Überwachungsberichte.</span><span class="sxs-lookup"><span data-stu-id="e5690-114">The Call Diagnostic Summary Report is accessed from the Monitoring Reports Home page.</span></span> <span data-ttu-id="e5690-115">Im Bericht Anruf Diagnose Zusammenfassung können Sie auf den Bericht [Peer-to-Peer-Aktivitäts Diagnose in lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md) zugreifen, indem Sie im Abschnitt Peer-to-Peer-Sitzungszusammenfassung im Bericht auf die Fehlerrate-Metrik klicken.</span><span class="sxs-lookup"><span data-stu-id="e5690-115">From the Call Diagnostic Summary Report you can access the [Peer-to-Peer Activity Diagnostic Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md) by clicking the Failure rate metric under the Peer-to-Peer Session Summary section of the report.</span></span> <span data-ttu-id="e5690-116">Sie können auch auf den [Konferenz Diagnosebericht in lync Server 2013](lync-server-2013-conference-diagnostic-report.md) zugreifen, indem Sie auf eine der folgenden Konferenz Metriken klicken:</span><span class="sxs-lookup"><span data-stu-id="e5690-116">You can also access the [Conference Diagnostic Report in Lync Server 2013](lync-server-2013-conference-diagnostic-report.md) by clicking any of the following conference metrics:</span></span>

  - <span data-ttu-id="e5690-117">Sitzungsfehlerrate insgesamt</span><span class="sxs-lookup"><span data-stu-id="e5690-117">Overall session failure rate</span></span>

  - <span data-ttu-id="e5690-118">Fehlerrate für Konferenzzustandsobjekt</span><span class="sxs-lookup"><span data-stu-id="e5690-118">Focus failure rate</span></span>

  - <span data-ttu-id="e5690-119">MCU-Fehlerrate</span><span class="sxs-lookup"><span data-stu-id="e5690-119">MCU failure rate</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-diagnostic-summary-report"></a><span data-ttu-id="e5690-120">Optimale Verwendung des zusammenfassenden Anrufdiagnoseberichts</span><span class="sxs-lookup"><span data-stu-id="e5690-120">Making the Best Use of the Call Diagnostic Summary Report</span></span>

<span data-ttu-id="e5690-121">Der Bericht zur Anruf Diagnose Zusammenfassung enthält Diagramme, die Fehlerraten für die verschiedenen in Microsoft lync Server 2013 verwendeten Methoden vergleichen.</span><span class="sxs-lookup"><span data-stu-id="e5690-121">The Call Diagnostic Summary Report includes graphs that compare failure rates for the various modalities used in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="e5690-122">Die Spalten in diesen Diagrammen sind tatsächlich Hotlinks; Wenn Sie beispielsweise auf die Spalte Instant Messaging für Peer-to-Peer-Sitzungen klicken, führen Sie einen Drilldown zu einer Instanz des [Diagnoseberichts zur Peer-to-Peer-Aktivität in lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md)durch, in der zusätzliche Details zu allen Chatsitzungen enthalten sind, die im Zusammenfassungsbericht zur Anruf Diagnose enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="e5690-122">The columns in these graphs are actually hotlinks; for example, if you click the Instant messaging column for peer-to-peer sessions, you'll drill down to an instance of the [Peer-to-Peer Activity Diagnostic Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md), a report that provides additional details about all the instant messaging sessions included in the Call Diagnostic Summary Report.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="e5690-123">Filter</span><span class="sxs-lookup"><span data-stu-id="e5690-123">Filters</span></span>

<span data-ttu-id="e5690-p104">Mithilfe von Filtern können Sie eine gezieltere Datenauswahl erreichen oder die zurückgegebenen Daten auf unterschiedliche Weise anzeigen. Beispielsweise können Sie im Zusammenfassenden Anrufdiagnosebericht nach Kriterien wie dem Registrierungspool oder den in der Sitzung verwendeten Edgeserver filtern. Sie können außerdem festlegen, wie Daten gruppiert werden sollen. In diesem Fall werden Anrufe nach Stunde, Tag, Woche oder Monat zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="e5690-p104">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Call Diagnostic Summary Report enables you to filter on such things as the Registrar pool or Edge Server used in the session. You can also choose how data should be grouped. In this case, calls are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="e5690-128">In der folgenden Tabelle werden die Filter aufgelistet, die Sie im Zusammenfassenden Anrufdiagnosebericht verwenden können.</span><span class="sxs-lookup"><span data-stu-id="e5690-128">The following table lists the filters that you can use with the Call Diagnostic Summary Report.</span></span>

### <a name="call-diagnostic-summary-report-filters"></a><span data-ttu-id="e5690-129">Filter im Zusammenfassenden Anrufdiagnosebericht</span><span class="sxs-lookup"><span data-stu-id="e5690-129">Call Diagnostic Summary Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5690-130">Name</span><span class="sxs-lookup"><span data-stu-id="e5690-130">Name</span></span></th>
<th><span data-ttu-id="e5690-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5690-131">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e5690-132"><strong>Von</strong></span><span class="sxs-lookup"><span data-stu-id="e5690-132"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="e5690-p105">Anfangsdatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Anfangsdatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="e5690-p105">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="e5690-135">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="e5690-135">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="e5690-p106">Wenn Sie keinen Anfangszeitpunkt eingeben, beginnt der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="e5690-p106">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="e5690-138">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="e5690-138">7/7/2012</span></span></p>
<p><span data-ttu-id="e5690-139">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="e5690-139">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="e5690-140">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="e5690-140">7/3/2012</span></span></p>
<p><span data-ttu-id="e5690-141">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="e5690-141">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5690-142"><strong>Bis</strong></span><span class="sxs-lookup"><span data-stu-id="e5690-142"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="e5690-p107">Enddatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Enddatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="e5690-p107">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="e5690-145">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="e5690-145">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="e5690-p108">Wenn Sie keinen Endzeitpunkt eingeben, endet der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="e5690-p108">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="e5690-148">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="e5690-148">7/7/2012</span></span></p>
<p><span data-ttu-id="e5690-149">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="e5690-149">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="e5690-150">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="e5690-150">7/3/2012</span></span></p>
<p><span data-ttu-id="e5690-151">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="e5690-151">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5690-152"><strong>Intervall</strong></span><span class="sxs-lookup"><span data-stu-id="e5690-152"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="e5690-p109">Zeitintervall. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="e5690-p109">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="e5690-155">Stündlich (maximal 25 Stunden können angezeigt werden)</span><span class="sxs-lookup"><span data-stu-id="e5690-155">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="e5690-156">Täglich (maximal 31 Tage können angezeigt werden)</span><span class="sxs-lookup"><span data-stu-id="e5690-156">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="e5690-157">Wöchentlich (maximal 12 Wochen können angezeigt werden)</span><span class="sxs-lookup"><span data-stu-id="e5690-157">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="e5690-158">Monatlich (maximal 12 Monate können angezeigt werden)</span><span class="sxs-lookup"><span data-stu-id="e5690-158">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="e5690-159">Wenn mit dem angegebenen Start- und Endzeitpunkt die maximale Anzahl der zulässigen Werte für das ausgewählte Intervall überschritten wird, wird nur die maximale Anzahl an Werten (beginnend mit dem Startzeitpunkt) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e5690-159">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="e5690-160">Wenn Sie beispielsweise das Tagesintervall mit einem Anfangstermin von 7/7/2012 und einem Enddatum von 2/28/2012 auswählen, werden die Daten für die Tage 8/7/2012 12:00 Uhr bis 9/7/2012 12:00 Uhr angezeigt (also insgesamt 31 Tage).</span><span class="sxs-lookup"><span data-stu-id="e5690-160">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5690-161"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="e5690-161"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="e5690-p111">Vollqualifizierter Domänenname (FQDN) des Registrar-Pools oder Edgeservers. Sie können einen einzelnen Pool auswählen oder auf <strong>[Alle]</strong> klicken, um die Daten für alle Pools anzuzeigen. Diese Dropdownliste wird basierend auf den Datensätzen in der Datenbank automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="e5690-p111">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="e5690-165">Metriken für Peer-to-Peer-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="e5690-165">Metrics for Peer-to-Peer Sessions</span></span>

<span data-ttu-id="e5690-166">In der folgenden Tabelle werden die Metriken aufgelistet, die im Zusammenfassenden Anrufdiagnosebericht für Peer-to-Peer-Sitzungen (d. h. für Sitzungen mit nur zwei Teilnehmern) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e5690-166">The following table lists the information provided in the Call Diagnostic Summary Report for peer-to-peer sessions (that is, sessions involving just two participants).</span></span>

### <a name="metrics-for-peer-to-peer-sessions"></a><span data-ttu-id="e5690-167">Metriken für Peer-to-Peer-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="e5690-167">Metrics for Peer-to-Peer Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5690-168">Name</span><span class="sxs-lookup"><span data-stu-id="e5690-168">Name</span></span></th>
<th><span data-ttu-id="e5690-169">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="e5690-169">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e5690-170">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5690-170">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e5690-171"><strong>Sitzungen insgesamt</strong></span><span class="sxs-lookup"><span data-stu-id="e5690-171"><strong>Total sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="e5690-172">Nein</span><span class="sxs-lookup"><span data-stu-id="e5690-172">No</span></span></p></td>
<td><p><span data-ttu-id="e5690-173">Die Gesamtzahl der Peer-to-Peer-Sitzungen, die stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="e5690-173">Total number of peer-to-peer sessions conducted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5690-174"><strong>Fehlerrate</strong></span><span class="sxs-lookup"><span data-stu-id="e5690-174"><strong>Failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="e5690-175">Nein</span><span class="sxs-lookup"><span data-stu-id="e5690-175">No</span></span></p></td>
<td><p><span data-ttu-id="e5690-p112">Der Prozentsatz der Peer-to-Peer-Sitzungen, bei denen ein Fehler aufgetreten ist. Wenn Sie auf dieses Element klicken, wird der Diagnosebericht über Peer-to-Peer-Aktivitäten angezeigt, der detailliertere Angaben zu den fehlgeschlagenen Peer-to-Peer-Sitzungen enthält.</span><span class="sxs-lookup"><span data-stu-id="e5690-p112">Percentage of peer-to-peer sessions that failed. When you click this item, the report shows the Peer-to-Peer Activity Diagnostic report, which displays more detailed information about the failed peer-to-peer sessions.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="e5690-178">Metriken für Konferenzsitzungen</span><span class="sxs-lookup"><span data-stu-id="e5690-178">Metrics for Conferencing Sessions</span></span>

<span data-ttu-id="e5690-179">In der folgenden Tabelle werden die Metriken aufgelistet, die im Zusammenfassenden Anrufdiagnosebericht für Konferenzsitzungen (d. h. für Sitzungen mit mindestens drei Teilnehmern) angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e5690-179">The following table lists the information provided in the Call Diagnostic Report for conferencing sessions (that is, sessions involving three or more participants).</span></span>

### <a name="metrics-for-conferencing-sessions"></a><span data-ttu-id="e5690-180">Metriken für Konferenzsitzungen</span><span class="sxs-lookup"><span data-stu-id="e5690-180">Metrics for Conferencing Sessions</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e5690-181">Name</span><span class="sxs-lookup"><span data-stu-id="e5690-181">Name</span></span></th>
<th><span data-ttu-id="e5690-182">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="e5690-182">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e5690-183">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e5690-183">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e5690-184"><strong>Konferenzen insgesamt</strong></span><span class="sxs-lookup"><span data-stu-id="e5690-184"><strong>Total conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="e5690-185">Nein</span><span class="sxs-lookup"><span data-stu-id="e5690-185">No</span></span></p></td>
<td><p><span data-ttu-id="e5690-186">Die Gesamtzahl der Konferenzen, die stattgefunden haben.</span><span class="sxs-lookup"><span data-stu-id="e5690-186">Total number of conferences conducted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5690-187"><strong>Konferenzsitzungen insgesamt</strong></span><span class="sxs-lookup"><span data-stu-id="e5690-187"><strong>Total conference sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="e5690-188">Nein</span><span class="sxs-lookup"><span data-stu-id="e5690-188">No</span></span></p></td>
<td><p><span data-ttu-id="e5690-189">Die Gesamtzahl der Konferenzsitzungen, die durchgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="e5690-189">Total number of conferencing sessions conducted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5690-190"><strong>Sitzungsfehlerrate insgesamt</strong></span><span class="sxs-lookup"><span data-stu-id="e5690-190"><strong>Overall session failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="e5690-191">Nein</span><span class="sxs-lookup"><span data-stu-id="e5690-191">No</span></span></p></td>
<td><p><span data-ttu-id="e5690-192">Der Prozentsatz der Konferenzsitzungen, bei denen ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e5690-192">Percentage of the total conferencing sessions that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5690-193"><strong>Konferenzzustandsobjekt-Sitzungen</strong></span><span class="sxs-lookup"><span data-stu-id="e5690-193"><strong>Focus sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="e5690-194">Nein</span><span class="sxs-lookup"><span data-stu-id="e5690-194">No</span></span></p></td>
<td><p><span data-ttu-id="e5690-195">Die Anzahl der auf Konferenzzustandsobjekten basierenden Sitzungen, bei denen Fehler aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="e5690-195">Total number of Focus-based conferencing sessions that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5690-196"><strong>Fehlerrate für Konferenzzustandsobjekt</strong></span><span class="sxs-lookup"><span data-stu-id="e5690-196"><strong>Focus failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="e5690-197">Nein</span><span class="sxs-lookup"><span data-stu-id="e5690-197">No</span></span></p></td>
<td><p><span data-ttu-id="e5690-198">Der Prozentsatz der auf Konferenzzustandsobjekten basierenden Konferenzsitzungen, bei denen ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e5690-198">Percentage of the Focus-based conferencing sessions that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e5690-199"><strong>MCU-Sitzungen</strong></span><span class="sxs-lookup"><span data-stu-id="e5690-199"><strong>MCU sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="e5690-200">Nein</span><span class="sxs-lookup"><span data-stu-id="e5690-200">No</span></span></p></td>
<td><p><span data-ttu-id="e5690-201">Die Gesamtzahl der auf Konferenzservern basierenden Konferenzen (früher als MCU-Konferenzen bezeichnet [Multipoint Control Unit]), bei denen ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e5690-201">Total number of conferencing server-based (formerly known as Multipoint Control Unit or MCU) conferences that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e5690-202"><strong>MCU-Fehlerrate</strong></span><span class="sxs-lookup"><span data-stu-id="e5690-202"><strong>MCU failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="e5690-203">Nein</span><span class="sxs-lookup"><span data-stu-id="e5690-203">No</span></span></p></td>
<td><p><span data-ttu-id="e5690-204">Der Prozentsatz der auf Konferenzservern basierenden Konferenzen (früher als MCU-Konferenzen bezeichnet [Multipoint Control Unit]), bei denen ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="e5690-204">Percentage of the conferencing server-based (formerly known as Multipoint Control Unit or MCU) conferences that failed.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e5690-205">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e5690-205">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

