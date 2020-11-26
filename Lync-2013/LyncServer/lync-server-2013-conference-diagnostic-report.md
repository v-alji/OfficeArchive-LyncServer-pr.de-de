---
title: 'Lync Server 2013: Konferenz Diagnosebericht'
description: 'Lync Server 2013: Konferenz Diagnosebericht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Diagnostic Report
ms:assetid: e9edc23c-8ce8-4ab8-8786-9d22e1e51e14
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615042(v=OCS.15)
ms:contentKeyID: 48185901
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9d3ef3c78bc2145d907d5a40e1aed95a2f4cb4c4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434545"
---
# <a name="conference-diagnostic-report-in-lync-server-2013"></a><span data-ttu-id="a8311-103">Konferenz Diagnosebericht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a8311-103">Conference Diagnostic Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a8311-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a8311-104">

<span> </span></span></span>

<span data-ttu-id="a8311-105">_**Letztes Änderungsdatum des Themas:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="a8311-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="a8311-106">Der Diagnosebericht über die Konferenz enthält Informationen über erfolgreich durchgeführte Konferenzsitzungen und Fehler bei Konferenzsitzungen.</span><span class="sxs-lookup"><span data-stu-id="a8311-106">The Conference Diagnostic Report provides information about the success and failure of all conferencing sessions.</span></span> <span data-ttu-id="a8311-107">Beachten Sie, dass Microsoft lync Server zwischen verschiedenen Arten von Fehlern unterscheidet:</span><span class="sxs-lookup"><span data-stu-id="a8311-107">Note that Microsoft Lync Server distinguishes between different kinds of failure:</span></span>

  - <span data-ttu-id="a8311-p102">**Erwarteter Fehler**. Ein erwarteter Fehler ist typischerweise ein rein technischer Fehler. Ein Beispiel: Angenommen, eine Person startet eine Konferenz, legt aber auf, bevor andere Personen der Konferenz beigetreten sind. Das ist technisch gesehen ein Fehler: Die Konferenz wurde initiiert, aber nicht abgeschlossen. Allerdings wäre das ein Fehler, den Sie durchaus erwarten würden. Bricht nämlich der Organisator die Konferenz ab, bevor andere Personen teilnehmen können, würden Sie die Konferenz nicht als abgeschlossen betrachten.</span><span class="sxs-lookup"><span data-stu-id="a8311-p102">**Expected failure**. An expected failure is typically a failure only in the most technical sense. For example, suppose someone starts a conference but hangs up before anyone can join. Technically that's a failure: the conference was initiated, but not completed. However, that's a failure that you would expect to happen: if the organizer cancels the conference before anyone can join then you would not expect that conference to be completed.</span></span>

  - <span data-ttu-id="a8311-p103">**Unerwarteter Fehler**. Wie der Name schon sagt, ist ein unerwarteter Fehler ein Fehler, dessen Auftreten Sie unter gegebenen Umständen nicht erwarten würden. Ein Beispiel: Angenommen, eine Konferenz konnte nicht durchgeführt werden, weil die Besprechungsrichtlinie des Organisators nicht abgerufen werden konnte. Das ist ein unerwarteter Fehler, denn die Besprechungsrichtlinie eines Benutzers sollte grundsätzlich immer abgerufen werden können.</span><span class="sxs-lookup"><span data-stu-id="a8311-p103">**Unexpected failure**. An unexpected error is exactly what the name implies: an error that, based on the circumstances, you would not expect to occur. For example, suppose a conference could not be held because the organizer's meeting policy could not be retrieved. That's an unexpected error: after all, you should always be able to retrieve a user's meeting policy.</span></span>

<span data-ttu-id="a8311-p104">Beachten Sie, dass die Summe aus den Werten für Erfolge, erwartete Fehler und unerwartete Fehler nicht immer mit der Angabe für „Sitzungen insgesamt“ übereinstimmt. Beispielsweise können in dem Bericht folgende Werte angegeben werden:</span><span class="sxs-lookup"><span data-stu-id="a8311-p104">Note that the Success, Expected failure, and Unexpected failure metrics might not add up to the Total sessions metric. For example, you might see the following values in the Report:</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a8311-119">Erfolge</span><span class="sxs-lookup"><span data-stu-id="a8311-119">Successes</span></span></th>
<th><span data-ttu-id="a8311-120">Erwartete Fehler</span><span class="sxs-lookup"><span data-stu-id="a8311-120">Expected failures</span></span></th>
<th><span data-ttu-id="a8311-121">Unerwartete Fehler</span><span class="sxs-lookup"><span data-stu-id="a8311-121">Unexpected failures</span></span></th>
<th><span data-ttu-id="a8311-122">Sitzungen insgesamt</span><span class="sxs-lookup"><span data-stu-id="a8311-122">Total sessions</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8311-123">2024</span><span class="sxs-lookup"><span data-stu-id="a8311-123">2024</span></span></p></td>
<td><p><span data-ttu-id="a8311-124">469</span><span class="sxs-lookup"><span data-stu-id="a8311-124">469</span></span></p></td>
<td><p><span data-ttu-id="a8311-125">16</span><span class="sxs-lookup"><span data-stu-id="a8311-125">16</span></span></p></td>
<td><p><span data-ttu-id="a8311-126">2521</span><span class="sxs-lookup"><span data-stu-id="a8311-126">2521</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a8311-127">Wenn Sie 2.024 + 469 + 16 addieren, ergibt das insgesamt 2.509 Sitzungen, aber in der Spalte „Sitzungen insgesamt“ wird 2.521 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a8311-127">If you add 2024 + 469 + 16 you get a total of 2,509 sessions and yet, the Total sessions column shows a total of 2,521 sessions.</span></span> <span data-ttu-id="a8311-128">Die „fehlenden“ 12 Sitzungen sind Sitzungen, die vom System nicht als erfolgreich oder fehlerhaft kategorisiert werden konnten.</span><span class="sxs-lookup"><span data-stu-id="a8311-128">The "missing" 12 sessions for are sessions that the system was unable to categorize as successful or unsuccessful.</span></span> <span data-ttu-id="a8311-129">Dies ist manchmal der Fall, wenn ein Drittanbieterprodukt einen neuen Diagnosecode einführt, der für die Überwachung von Server unbekannt ist.</span><span class="sxs-lookup"><span data-stu-id="a8311-129">That will sometimes be the case when a third-party product introduces a new diagnostic code that is unfamiliar to Monitoring Server.</span></span> <span data-ttu-id="a8311-130">In einer solchen Situation können Aufrufe, die mit diesem Produkt ausgeführt werden und für die dieser Diagnosecode gemeldet wird, nicht immer eindeutig als Erfolg, erwarteter Fehler oder unerwarteter Fehler kategorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="a8311-130">When that happens, calls made using that product, and reporting that diagnostic code, cannot always be categorized as being a Success, an Expected failure, or an Unexpected failure.</span></span>

<div>

## <a name="accessing-the-conference-diagnostic-report"></a><span data-ttu-id="a8311-131">Öffnen des Diagnoseberichts über die Konferenz</span><span class="sxs-lookup"><span data-stu-id="a8311-131">Accessing the Conference Diagnostic Report</span></span>

<span data-ttu-id="a8311-132">Auf den Diagnosebericht über die Konferenz greifen Sie über die Startseite für Überwachungsberichte zu.</span><span class="sxs-lookup"><span data-stu-id="a8311-132">The Conference Diagnostic Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="a8311-133">Sie können auf den [Bericht Fehlerverteilung in lync Server 2013](lync-server-2013-failure-distribution-report.md) zugreifen, indem Sie auf eine der folgenden Metriken klicken:</span><span class="sxs-lookup"><span data-stu-id="a8311-133">You can access the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="a8311-134">Anzahl der unerwarteten Fehler</span><span class="sxs-lookup"><span data-stu-id="a8311-134">Unexpected failure volume</span></span>

  - <span data-ttu-id="a8311-135">Anzahl der erwarteten Fehler</span><span class="sxs-lookup"><span data-stu-id="a8311-135">Expected failure volume</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-conference-diagnostic-report"></a><span data-ttu-id="a8311-136">Optimales Nutzen des Diagnoseberichts über die Konferenz</span><span class="sxs-lookup"><span data-stu-id="a8311-136">Making the Best Use of the Conference Diagnostic Report</span></span>

<span data-ttu-id="a8311-137">Der Diagnosebericht über die Konferenz enthält eine Reihe von Diagrammen.</span><span class="sxs-lookup"><span data-stu-id="a8311-137">The Conference Diagnostic Report includes a series of graphs.</span></span> <span data-ttu-id="a8311-138">Jede der Spalten in einem Diagramm ist ein Hyperlink.</span><span class="sxs-lookup"><span data-stu-id="a8311-138">Each of the columns shown in the graph is actually a hyperlink.</span></span> <span data-ttu-id="a8311-139">Wenn Sie auf eine Spalte klicken, führen Sie einen Drilldown zum [Fehler Verteilungs Bericht in lync Server 2013](lync-server-2013-failure-distribution-report.md) für diesen Zeitraum und diesen Konferenztyp durch.</span><span class="sxs-lookup"><span data-stu-id="a8311-139">If you click a column, you'll drill down to the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md) for that time period and that conference type.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="a8311-140">Filter</span><span class="sxs-lookup"><span data-stu-id="a8311-140">Filters</span></span>

<span data-ttu-id="a8311-p108">Mithilfe von Filtern können Sie eine gezieltere Datenauswahl erreichen oder die zurückgegebenen Daten auf unterschiedliche Weise anzeigen. Beispielsweise können Sie die Daten im Diagnosebericht über Konferenzen nach Kriterien wie etwa dem Konferenztyp (z. B. Konferenzzustandsobjekt-Sitzung) oder dem für die Konferenz verwendeten Edgeserver filtern. Sie können außerdem festlegen, wie Daten gruppiert werden sollen. In diesem Fall werden Konferenzen nach Stunde, Tag, Woche oder Monat zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="a8311-p108">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Conference Diagnostic Report enables you to filter on such things as the type of conference being conducted (for example, a Focus-based conference) or by the Edge Server used in the conference. You can also choose how data should be grouped. In this case, conferences are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="a8311-145">In der folgenden Tabelle werden die Filter aufgelistet, die Sie im Diagnosebericht über die Konferenz verwenden können.</span><span class="sxs-lookup"><span data-stu-id="a8311-145">The following table lists the filters that you can use with the Conference Diagnostic Report.</span></span>

### <a name="conference-diagnostic-report-filters"></a><span data-ttu-id="a8311-146">Filter im Diagnosebericht über die Konferenz</span><span class="sxs-lookup"><span data-stu-id="a8311-146">Conference Diagnostic Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a8311-147">Name</span><span class="sxs-lookup"><span data-stu-id="a8311-147">Name</span></span></th>
<th><span data-ttu-id="a8311-148">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8311-148">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8311-149"><strong>Von</strong></span><span class="sxs-lookup"><span data-stu-id="a8311-149"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="a8311-p109">Anfangsdatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Anfangsdatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="a8311-p109">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="a8311-152">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="a8311-152">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="a8311-p110">Wenn Sie keinen Anfangszeitpunkt eingeben, beginnt der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="a8311-p110">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="a8311-155">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="a8311-155">7/7/2012</span></span></p>
<p><span data-ttu-id="a8311-156">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="a8311-156">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="a8311-157">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="a8311-157">7/3/2012</span></span></p>
<p><span data-ttu-id="a8311-158">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="a8311-158">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8311-159"><strong>Bis</strong></span><span class="sxs-lookup"><span data-stu-id="a8311-159"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="a8311-p111">Enddatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Enddatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="a8311-p111">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="a8311-162">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="a8311-162">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="a8311-p112">Wenn Sie keinen Endzeitpunkt eingeben, endet der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="a8311-p112">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="a8311-165">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="a8311-165">7/7/2012</span></span></p>
<p><span data-ttu-id="a8311-166">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="a8311-166">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="a8311-167">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="a8311-167">7/3/2012</span></span></p>
<p><span data-ttu-id="a8311-168">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="a8311-168">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8311-169"><strong>Intervall</strong></span><span class="sxs-lookup"><span data-stu-id="a8311-169"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="a8311-p113">Zeitintervall. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="a8311-p113">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="a8311-172">Stündlich (maximal 25 Stunden können angezeigt werden)</span><span class="sxs-lookup"><span data-stu-id="a8311-172">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="a8311-173">Täglich (maximal 31 Tage können angezeigt werden)</span><span class="sxs-lookup"><span data-stu-id="a8311-173">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="a8311-174">Wöchentlich (maximal 12 Wochen können angezeigt werden)</span><span class="sxs-lookup"><span data-stu-id="a8311-174">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="a8311-175">Monatlich (maximal 12 Monate können angezeigt werden)</span><span class="sxs-lookup"><span data-stu-id="a8311-175">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="a8311-176">Wenn mit dem angegebenen Start- und Endzeitpunkt die maximale Anzahl der zulässigen Werte für das ausgewählte Intervall überschritten wird, wird nur die maximale Anzahl an Werten (beginnend mit dem Startzeitpunkt) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a8311-176">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="a8311-177">Wenn Sie beispielsweise das Tagesintervall mit einem Anfangstermin von 7/7/2012 und einem Enddatum von 2/28/2012 auswählen, werden die Daten für die Tage 8/7/2012 12:00 Uhr bis 9/7/2012 12:00 Uhr angezeigt (also insgesamt 31 Tage).</span><span class="sxs-lookup"><span data-stu-id="a8311-177">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8311-178"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="a8311-178"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="a8311-p115">Vollqualifizierter Domänenname (FQDN) des Registrierungspools oder Edgeservers. Sie können einen einzelnen Pool auswählen oder auf <strong>[Alle]</strong> klicken, um die Daten für alle Pools anzuzeigen. Diese Dropdownliste wird basierend auf den Datensätzen in der Datenbank automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="a8311-p115">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8311-182"><strong>Konferenzsitzungen</strong></span><span class="sxs-lookup"><span data-stu-id="a8311-182"><strong>Conference sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="a8311-p116">Gibt den Typ der Konferenzsitzung an. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="a8311-p116">Indicates the type of conferencing session. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="a8311-185">[Alle]</span><span class="sxs-lookup"><span data-stu-id="a8311-185">[All]</span></span></p></li>
<li><p><span data-ttu-id="a8311-186">Konferenzzustandsobjekt-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="a8311-186">Focus sessions</span></span></p></li>
<li><p><span data-ttu-id="a8311-187">Alle MCU-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="a8311-187">All MCU sessions</span></span></p></li>
<li><p><span data-ttu-id="a8311-188">Sofortnachrichtenkonferenzen</span><span class="sxs-lookup"><span data-stu-id="a8311-188">IM conferencing</span></span></p></li>
<li><p><span data-ttu-id="a8311-189">Anwendungsfreigabe</span><span class="sxs-lookup"><span data-stu-id="a8311-189">Application sharing</span></span></p></li>
<li><p><span data-ttu-id="a8311-190">A/V-Konferenzen</span><span class="sxs-lookup"><span data-stu-id="a8311-190">A/V conferencing</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="a8311-191">Metriken</span><span class="sxs-lookup"><span data-stu-id="a8311-191">Metrics</span></span>

<span data-ttu-id="a8311-192">In der folgenden Tabelle werden die Metriken aufgelistet, die im Diagnosebericht über die Konferenz für jeden Konferenzsitzungstyp angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a8311-192">The following table lists the information provided in the Conference Diagnostic Report for each type of conferencing session.</span></span>

### <a name="conference-diagnostic-report-metrics"></a><span data-ttu-id="a8311-193">Metriken im Diagnosebericht über die Konferenz</span><span class="sxs-lookup"><span data-stu-id="a8311-193">Conference Diagnostic Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a8311-194">Name</span><span class="sxs-lookup"><span data-stu-id="a8311-194">Name</span></span></th>
<th><span data-ttu-id="a8311-195">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="a8311-195">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="a8311-196">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="a8311-196">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a8311-197"><strong>Anzahl der erfolgreichen Sitzungen</strong></span><span class="sxs-lookup"><span data-stu-id="a8311-197"><strong>Success volume</strong></span></span></p></td>
<td><p><span data-ttu-id="a8311-198">Nein</span><span class="sxs-lookup"><span data-stu-id="a8311-198">No</span></span></p></td>
<td><p><span data-ttu-id="a8311-199">Die Gesamtzahl der erfolgreich durchgeführten Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="a8311-199">Total number of successful conferences.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8311-200"><strong>Prozentsatz der erfolgreichen Sitzungen</strong></span><span class="sxs-lookup"><span data-stu-id="a8311-200"><strong>Success percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="a8311-201">Nein</span><span class="sxs-lookup"><span data-stu-id="a8311-201">No</span></span></p></td>
<td><p><span data-ttu-id="a8311-p117">Der Prozentsatz der Konferenzen, die ohne nennenswerte Probleme ausgeführt wurden. Errechnet sich durch Dividieren der Anzahl der erfolgreichen Sitzungen durch die Gesamtzahl der Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="a8311-p117">Percentage of conferences that completed with significant problems. Calculated by dividing the Success volume by the Total sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8311-204"><strong>Anzahl der erwarteten Fehler</strong></span><span class="sxs-lookup"><span data-stu-id="a8311-204"><strong>Expected failure volume</strong></span></span></p></td>
<td><p><span data-ttu-id="a8311-205">Nein</span><span class="sxs-lookup"><span data-stu-id="a8311-205">No</span></span></p></td>
<td><p><span data-ttu-id="a8311-206">Die Gesamtzahl der Konferenzen, bei denen ein &quot; Erwarteter Fehler &quot; aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a8311-206">Total number of conferences where an &quot;expected failure&quot; occurred.</span></span></p>
<p><span data-ttu-id="a8311-p118">Ein erwarteter Fehler ist ein Fehler, der zu erwarten ist. Wenn beispielsweise ein Benutzer seinen Status auf „Nicht stören“ festgelegt hat, ist zu erwarten, dass jeder Anruf an diesen Benutzer fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="a8311-p118">An expected failure is a failure that is expected to happen. For example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8311-209"><strong>Prozentsatz der erwarteten Fehler</strong></span><span class="sxs-lookup"><span data-stu-id="a8311-209"><strong>Expected failure percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="a8311-210">Nein</span><span class="sxs-lookup"><span data-stu-id="a8311-210">No</span></span></p></td>
<td><p><span data-ttu-id="a8311-p119">Der Prozentsatz der Konferenzen, bei denen ein erwarteter Fehler aufgetreten ist. Errechnet sich durch Dividieren der Anzahl der erwarteten Fehler durch die Gesamtzahl der Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="a8311-p119">Percentage of conferences that experienced an expected error. Calculated by dividing the Expected failure volume by the Total sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8311-213"><strong>Anzahl der unerwarteten Fehler</strong></span><span class="sxs-lookup"><span data-stu-id="a8311-213"><strong>Unexpected failure volume</strong></span></span></p></td>
<td><p><span data-ttu-id="a8311-214">Nein</span><span class="sxs-lookup"><span data-stu-id="a8311-214">No</span></span></p></td>
<td><p><span data-ttu-id="a8311-215">Die Gesamtzahl der Konferenzen, bei denen ein &quot; unerwarteter Fehler &quot; aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="a8311-215">Total number of conferences where an &quot;unexpected failure&quot; occurred.</span></span></p>
<p><span data-ttu-id="a8311-p120">Ein unerwarteter Fehler ist ein Fehler, der in einem System auftritt, das abgesehen davon anscheinend intakt ist. Beispielsweise sollte ein Anruf nicht beendet werden, wenn der Anrufer in der Warteschleife platziert ist. Geschieht dies jedoch, würde dieser Vorgang als unerwarteter Fehler gekennzeichnet werden.</span><span class="sxs-lookup"><span data-stu-id="a8311-p120">An unexpected failure is a failure that occurs in what would appear to be an otherwise healthy system. For example, a call should not be terminated if the caller is placed on hold. If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a8311-219"><strong>Prozentsatz der unerwarteten Fehler</strong></span><span class="sxs-lookup"><span data-stu-id="a8311-219"><strong>Unexpected failure percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="a8311-220">Nein</span><span class="sxs-lookup"><span data-stu-id="a8311-220">No</span></span></p></td>
<td><p><span data-ttu-id="a8311-p121">Der Prozentsatz der Konferenzen, bei denen ein unerwarteter Fehler aufgetreten ist. Errechnet sich durch Dividieren der Anzahl der unerwarteten Fehler durch die Gesamtzahl der Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="a8311-p121">Percentage of conferences that experienced an unexpected error. Calculated by dividing the Unexpected failure volume by the Total sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a8311-223"><strong>Sitzungen insgesamt</strong></span><span class="sxs-lookup"><span data-stu-id="a8311-223"><strong>Total sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="a8311-224">Nein</span><span class="sxs-lookup"><span data-stu-id="a8311-224">No</span></span></p></td>
<td><p><span data-ttu-id="a8311-225">Die Gesamtzahl der Konferenzen, einschließlich Konferenzen ohne Fehler, Konferenzen mit Fehlern (sowohl erwarteten als auch unerwarteten) und nicht kategorisierten Konferenzen.</span><span class="sxs-lookup"><span data-stu-id="a8311-225">Total number of conferences, including successful conferences, failed conferences (both expected failures and unexpected failures), and uncategorized conferences.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a8311-226">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a8311-226">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

