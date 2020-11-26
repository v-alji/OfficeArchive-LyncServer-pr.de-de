---
title: 'Lync Server 2013: Trend Bericht zur Server Medienqualität'
description: 'Lync Server 2013: Trend Bericht zur Server Medienqualität'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server Media Quality Trend Report
ms:assetid: 8a51fd13-1487-4632-b5ec-f7ae2abe8ed4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205071(v=OCS.15)
ms:contentKeyID: 48184760
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7ac2482b967aab230c5522c2b6a76e10ced28e7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444903"
---
# <a name="server-media-quality-trend-report-in-lync-server-2013"></a><span data-ttu-id="d09ef-103">Trend Bericht zur Server Medienqualität in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d09ef-103">Server Media Quality Trend Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d09ef-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d09ef-104">

<span> </span></span></span>

<span data-ttu-id="d09ef-105">_**Letztes Änderungsdatum des Themas:** 2012-11-12_</span><span class="sxs-lookup"><span data-stu-id="d09ef-105">_**Topic Last Modified:** 2012-11-12_</span></span>

<span data-ttu-id="d09ef-106">Der Trend Bericht "Server Medienqualität" bietet eine Möglichkeit, bis zu 5 Server auf der Grundlage der Qualität von Erfahrungswerten wie Anruflautstärke, schlechtem Anruf Prozentsatz, Paketverlust und Jitter grafisch zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="d09ef-106">The Server Media Quality Trend Report provides a way for you to graphically compare up to 5 servers on Quality of Experience metrics such as call volume, poor call percentage, packet loss, and jitter.</span></span> <span data-ttu-id="d09ef-107">So ist es einfacher, die leistungsschwachen, nicht voll ausgelasteten oder die überbeanspruchten Server zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d09ef-107">This makes it easier to do such things as identify servers that are performing poorly, identify servers that are underutilized, or identify servers that are being overused.</span></span>

<div>

## <a name="accessing-the-server-media-quality-trend-report"></a><span data-ttu-id="d09ef-108">Zugreifen auf den „Trendbericht über Medienqualität des Servers“</span><span class="sxs-lookup"><span data-stu-id="d09ef-108">Accessing the Server Media Quality Trend Report</span></span>

<span data-ttu-id="d09ef-109">Auf den „Trendbericht über Medienqualität des Servers“ kann über einen der folgenden Berichte zugegriffen werden:</span><span class="sxs-lookup"><span data-stu-id="d09ef-109">The Server Media Quality Trend Report can be accessed from either one of the following report:</span></span>

  - <span data-ttu-id="d09ef-110">[Bericht zur Serverleistung in lync Server 2013](lync-server-2013-server-performance-report.md) (durch Klicken auf die Trend Metrik)</span><span class="sxs-lookup"><span data-stu-id="d09ef-110">[Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md) (by clicking the Trend metric)</span></span>

  - <span data-ttu-id="d09ef-111">[Anruf Detail Bericht in lync Server 2013](lync-server-2013-call-detail-report.md) (durch Klicken auf die Metrik A/V Edge Server.</span><span class="sxs-lookup"><span data-stu-id="d09ef-111">[Call Detail Report in Lync Server 2013](lync-server-2013-call-detail-report.md) (by clicking the A/V edge server metric.</span></span> <span data-ttu-id="d09ef-112">Wenn es sich bei dem Anrufer oder angerufenen um einen Server handelt, können Sie auch den Bericht "Server Quality Media Trend" erreichen, indem Sie auf den Endpunktnamen klicken.)</span><span class="sxs-lookup"><span data-stu-id="d09ef-112">If the caller or callee is a server, you can also reach the Server Quality Media Trend Report by clicking the endpoint name.)</span></span>

</div>

<div>

## <a name="making-the-best-use-of-server-media-quality-trend-report"></a><span data-ttu-id="d09ef-113">Optimale Nutzung des „Trendberichts über Medienqualität des Servers“</span><span class="sxs-lookup"><span data-stu-id="d09ef-113">Making the Best Use of Server Media Quality Trend Report</span></span>

<span data-ttu-id="d09ef-114">Wenn Sie im [Serverleistungsbericht in lync Server 2013](lync-server-2013-server-performance-report.md) für einen bestimmten Server auf die Trend Metrik klicken, wird der Trendbericht "Server Medienqualität" geöffnet.</span><span class="sxs-lookup"><span data-stu-id="d09ef-114">When you click the Trend metric on the [Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md) for a specific server, the Server Media Quality Trend Report will open.</span></span> <span data-ttu-id="d09ef-115">Es wird jedoch nur eine leere Instanz dieses Berichts angezeigt. der auf dem Serverleistungsbericht ausgewählte Server wird nicht auf dem Bildschirm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d09ef-115">However, you will see only a blank instance of that report; the server you selected on the Server Performance Report will not be displayed onscreen.</span></span> <span data-ttu-id="d09ef-116">Stattdessen müssen Sie diesen Server aus der Dropdownliste Server auswählen.</span><span class="sxs-lookup"><span data-stu-id="d09ef-116">Instead, you will need to select that server from the Servers dropdown.</span></span> <span data-ttu-id="d09ef-117">Beachten Sie auch, dass die Dropdownliste "Server" eine Option "Alles auswählen" enthält.</span><span class="sxs-lookup"><span data-stu-id="d09ef-117">Note, too that the Servers dropdown includes a Select All option.</span></span> <span data-ttu-id="d09ef-118">Diese Option funktioniert nicht, wenn Sie mehr als 5 Server haben; im Trend Bericht zur Server Medienqualität können nur Daten für maximal 5 Server gleichzeitig angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d09ef-118">This option will not work if you have more than 5 servers; the Server Media Quality Trend Report can only display data for a maximum of 5 servers at a time.</span></span>

<span data-ttu-id="d09ef-119">In den Diagrammen, die mit dem Trend Bericht "Server Medienqualität" angezeigt werden, sind die Punkte mit der Bezeichnung Anrufvolumen und schlechter Anruf Prozentsatz Hotlinks; Wenn Sie auf einen Punkt im Diagramm klicken, wird eine Instanz des [Anruflisten Berichts in lync Server 2013](lync-server-2013-call-list-report.md) geöffnet, in dem die Gesamt Anrufe (oder schlechte Anrufe) für den angegebenen Zeitraum angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="d09ef-119">On the graphs displayed by the Server Media Quality Trend Report, the points labeled Call Volume and Poor Call Percentage are hotlinks; clicking a point on the graph will open an instance of the [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) showing the total calls (or poor calls) for the specified time period.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="d09ef-120">Filter</span><span class="sxs-lookup"><span data-stu-id="d09ef-120">Filters</span></span>

<span data-ttu-id="d09ef-p104">Mithilfe von Filtern können Sie eine gezieltere Datenauswahl erreichen oder die zurückgegebenen Daten auf unterschiedliche Weise anzeigen. In der folgenden Tabelle werden die Filter aufgelistet, die Sie im „Trendbericht über Medienqualität des Servers“ verwenden können.</span><span class="sxs-lookup"><span data-stu-id="d09ef-p104">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Server Media Quality Trend Report.</span></span>

### <a name="server-media-quality-trend-report-filters"></a><span data-ttu-id="d09ef-123">Filter im „Trendbericht über Medienqualität des Servers“</span><span class="sxs-lookup"><span data-stu-id="d09ef-123">Server Media Quality Trend Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d09ef-124">Name</span><span class="sxs-lookup"><span data-stu-id="d09ef-124">Name</span></span></th>
<th><span data-ttu-id="d09ef-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d09ef-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d09ef-126"><strong>Von</strong></span><span class="sxs-lookup"><span data-stu-id="d09ef-126"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="d09ef-p105">Anfangsdatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Anfangsdatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="d09ef-p105">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="d09ef-129">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="d09ef-129">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="d09ef-p106">Wenn Sie keinen Anfangszeitpunkt eingeben, beginnt der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="d09ef-p106">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="d09ef-132">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="d09ef-132">7/7/2012</span></span></p>
<p><span data-ttu-id="d09ef-133">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="d09ef-133">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="d09ef-134">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="d09ef-134">7/3/2012</span></span></p>
<p><span data-ttu-id="d09ef-135">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="d09ef-135">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09ef-136"><strong>Bis</strong></span><span class="sxs-lookup"><span data-stu-id="d09ef-136"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="d09ef-p107">Enddatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Enddatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="d09ef-p107">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="d09ef-139">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="d09ef-139">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="d09ef-p108">Wenn Sie keinen Endzeitpunkt eingeben, endet der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="d09ef-p108">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="d09ef-142">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="d09ef-142">7/7/2012</span></span></p>
<p><span data-ttu-id="d09ef-143">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="d09ef-143">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="d09ef-144">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="d09ef-144">7/3/2012</span></span></p>
<p><span data-ttu-id="d09ef-145">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="d09ef-145">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d09ef-146"><strong>Intervall</strong></span><span class="sxs-lookup"><span data-stu-id="d09ef-146"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="d09ef-p109">Zeitintervall. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="d09ef-p109">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="d09ef-149">Stündlich (maximal 25 Stunden können angezeigt werden)</span><span class="sxs-lookup"><span data-stu-id="d09ef-149">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="d09ef-150">Täglich (maximal 31 Tage können angezeigt werden)</span><span class="sxs-lookup"><span data-stu-id="d09ef-150">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="d09ef-151">Wöchentlich (maximal 12 Wochen können angezeigt werden)</span><span class="sxs-lookup"><span data-stu-id="d09ef-151">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="d09ef-152">Wenn mit dem angegebenen Start- und Endzeitpunkt die maximale Anzahl der zulässigen Werte für das ausgewählte Intervall überschritten wird, wird nur die maximale Anzahl an Werten (beginnend mit dem Startzeitpunkt) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d09ef-152">If the start and end dates exceed the maximum number of values allowed for the selected interval, only the maximum number of values (starting from the start date) is displayed.</span></span> <span data-ttu-id="d09ef-153">Wenn Sie beispielsweise das Tagesintervall mit einem Anfangstermin von 8/7/2012 und einem Enddatum von 9/28/2012 auswählen, werden die Daten für die Tage 8/7/2012 12:00 Uhr bis 9/7/2012 12:00 Uhr angezeigt (also insgesamt 31 Tage).</span><span class="sxs-lookup"><span data-stu-id="d09ef-153">For example, if you select the Daily interval with a start date of 8/7/2012 and an end date of 9/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09ef-154"><strong>Servertyp</strong></span><span class="sxs-lookup"><span data-stu-id="d09ef-154"><strong>Server type</strong></span></span></p></td>
<td><p><span data-ttu-id="d09ef-p111">Beim Anruf verwendeter Servertyp. Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d09ef-p111">Type of server involved in the call. Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="d09ef-157">Vermittlungsserver</span><span class="sxs-lookup"><span data-stu-id="d09ef-157">Mediation Server</span></span></p></li>
<li><p><span data-ttu-id="d09ef-158">A/V-Konferenzserver</span><span class="sxs-lookup"><span data-stu-id="d09ef-158">A/V Conferencing Server</span></span></p></li>
<li><p><span data-ttu-id="d09ef-159">A/V-Edgeserver</span><span class="sxs-lookup"><span data-stu-id="d09ef-159">A/V Edge Server</span></span></p></li>
<li><p><span data-ttu-id="d09ef-160">Gateway (Vermittlungsserver)</span><span class="sxs-lookup"><span data-stu-id="d09ef-160">Gateway (Mediation Server)</span></span></p></li>
<li><p><span data-ttu-id="d09ef-161">Gateway (Umgehung des Vermittlungsservers)</span><span class="sxs-lookup"><span data-stu-id="d09ef-161">Gateway (Mediation Server Bypass)</span></span></p></li>
<li><p><span data-ttu-id="d09ef-162">AS-Konferenzserver</span><span class="sxs-lookup"><span data-stu-id="d09ef-162">AS Conferencing Server</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d09ef-163"><strong>Server</strong></span><span class="sxs-lookup"><span data-stu-id="d09ef-163"><strong>Servers</strong></span></span></p></td>
<td><p><span data-ttu-id="d09ef-p112">Name des in der Sitzung verwendeten Servers. Diese Dropdownliste wird automatisch anhand des Werts des Servertypfilters aufgefüllt. Sie können bei der Erstellung eines Berichts bis zu 5 verschiedene Server auswählen.</span><span class="sxs-lookup"><span data-stu-id="d09ef-p112">Name of the server involved in the session; this dropdown list is automatically populated for you based on the value of the Server type filter. You can select up to 5 different servers when compiling a report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09ef-166"><strong>Zugriffstyp</strong></span><span class="sxs-lookup"><span data-stu-id="d09ef-166"><strong>Access type</strong></span></span></p></td>
<td><p><span data-ttu-id="d09ef-p113">Gibt an, ob der Teilnehmer am internen oder am externen Netzwerk angemeldet wurde. Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d09ef-p113">Indicates whether the participant was logged on to the internal network or from the external network. Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="d09ef-169">[Alle]</span><span class="sxs-lookup"><span data-stu-id="d09ef-169">[All]</span></span></p></li>
<li><p><span data-ttu-id="d09ef-170">Intern</span><span class="sxs-lookup"><span data-stu-id="d09ef-170">Internal</span></span></p></li>
<li><p><span data-ttu-id="d09ef-171">Extern</span><span class="sxs-lookup"><span data-stu-id="d09ef-171">External</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d09ef-172"><strong>Netzwerktyp</strong></span><span class="sxs-lookup"><span data-stu-id="d09ef-172"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="d09ef-p114">Gibt den Typ des Netzwerks an, mit dem der Teilnehmer verbunden wurde. Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d09ef-p114">Indicates the type of network the participant was connected to. Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="d09ef-175">[Alle]</span><span class="sxs-lookup"><span data-stu-id="d09ef-175">[All]</span></span></p></li>
<li><p><span data-ttu-id="d09ef-176">Verkabelt</span><span class="sxs-lookup"><span data-stu-id="d09ef-176">Wired</span></span></p></li>
<li><p><span data-ttu-id="d09ef-177">Funk</span><span class="sxs-lookup"><span data-stu-id="d09ef-177">Wireless</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09ef-178"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="d09ef-178"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="d09ef-p115">Gibt an, ob ein externer Teilnehmer während der Sitzung eine VPN-Verbindung (Virtual Private Network) verwendete. Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="d09ef-p115">Indicates whether an external participant was using a virtual private network (VPN) connection during the session. Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="d09ef-181">[Alle]</span><span class="sxs-lookup"><span data-stu-id="d09ef-181">[All]</span></span></p></li>
<li><p><span data-ttu-id="d09ef-182">VPN</span><span class="sxs-lookup"><span data-stu-id="d09ef-182">VPN</span></span></p></li>
<li><p><span data-ttu-id="d09ef-183">Nicht-VPN</span><span class="sxs-lookup"><span data-stu-id="d09ef-183">Non-VPN</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="d09ef-184">Metriken</span><span class="sxs-lookup"><span data-stu-id="d09ef-184">Metrics</span></span>

<span data-ttu-id="d09ef-185">In der folgenden Tabelle werden Metriken aufgelistet, die im „Trendbericht über Medienqualität des Servers“ angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="d09ef-185">The following table lists the information provided in the Server Media Quality Trend Report.</span></span>

### <a name="server-media-quality-trend-report-metrics"></a><span data-ttu-id="d09ef-186">Metriken im „Trendbericht über Medienqualität des Servers“</span><span class="sxs-lookup"><span data-stu-id="d09ef-186">Server Media Quality Trend Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d09ef-187">Name</span><span class="sxs-lookup"><span data-stu-id="d09ef-187">Name</span></span></th>
<th><span data-ttu-id="d09ef-188">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="d09ef-188">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="d09ef-189">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d09ef-189">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d09ef-190"><strong>Anruflautstärke</strong></span><span class="sxs-lookup"><span data-stu-id="d09ef-190"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="d09ef-191">Nein</span><span class="sxs-lookup"><span data-stu-id="d09ef-191">No</span></span></p></td>
<td><p><span data-ttu-id="d09ef-192">Die Gesamtzahl der Anrufe.</span><span class="sxs-lookup"><span data-stu-id="d09ef-192">Total number of calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09ef-193"><strong>Beeinträchtigung (MOS)</strong></span><span class="sxs-lookup"><span data-stu-id="d09ef-193"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="d09ef-194">Nein</span><span class="sxs-lookup"><span data-stu-id="d09ef-194">No</span></span></p></td>
<td><p><span data-ttu-id="d09ef-195">Durchschnittliche Anzahl von MOS (Mean Option Score) Verschlechterung während eines Anrufs.</span><span class="sxs-lookup"><span data-stu-id="d09ef-195">Average amount of MOS (mean option score) degradation experienced during a call.</span></span> <span data-ttu-id="d09ef-196">Die Werte für die Verschlechterung können von einem Tiefstwert von 0,0 bis zu einem Höchstwert von 5,0 liegen. ein Wert von 0,5 oder einer kleineren stellt eine akzeptable Verschlechterung dar.</span><span class="sxs-lookup"><span data-stu-id="d09ef-196">Degradation values can range from a low of 0.0 to a high of 5.0; a value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="d09ef-197">Früher wurden Mean Opinion Scores berechnet, indem man Benutzer die Qualität eines Telefongesprächs auf einer Skala von 1 bis 5 bewerten ließ.</span><span class="sxs-lookup"><span data-stu-id="d09ef-197">Historically, mean options scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="d09ef-198">Lync Server verwendet eine Reihe von Algorithmen, um vorherzusagen, wie Benutzer einen Anruf bewertet hätten.</span><span class="sxs-lookup"><span data-stu-id="d09ef-198">Lync Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="d09ef-p117">Hohe Beeinträchtigungswerte können durch Überlastung, zu geringe Bandbreite, Funknetzüberlastung oder -interferenzen oder durch einen überlasteten Medienserver oder Endpunkt verursacht werden. Eine hohe Beeinträchtigung führt zu verzerrter oder unterbrochener Sprachübertragung.</span><span class="sxs-lookup"><span data-stu-id="d09ef-p117">High degradation values can be caused by congestion; lack of bandwidth; wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d09ef-201"><strong>Prozentsatz der Anrufe schlechter Qualität</strong></span><span class="sxs-lookup"><span data-stu-id="d09ef-201"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="d09ef-202">Nein</span><span class="sxs-lookup"><span data-stu-id="d09ef-202">No</span></span></p></td>
<td><p><span data-ttu-id="d09ef-p118">Die Gesamtzahl der Anrufe, die als Anrufe schlechter Qualität klassifiziert werden. Dies sind Anrufe, bei denen für mindestens eine der gemessenen Metriken der zulässige Wert überschritten wurde (z. B. ein Anruf mit übermäßigem Jitter).</span><span class="sxs-lookup"><span data-stu-id="d09ef-p118">The total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09ef-205"><strong>Roundtrip (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="d09ef-205"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="d09ef-206">Nein</span><span class="sxs-lookup"><span data-stu-id="d09ef-206">No</span></span></p></td>
<td><p><span data-ttu-id="d09ef-p119">Die durchschnittliche Zeit (in Millisekunden), die ein Real-Time Transport Protocol-Paket (RTP) benötigt, um zu einem Endpunkt und wieder zurück zu gelangen. Eine Roundtripzeit von 200 ms oder weniger gilt als akzeptable Qualität.</span><span class="sxs-lookup"><span data-stu-id="d09ef-p119">Average amount of time (in milliseconds) required for a Real-Time Transport Protocol packet to travel to one endpoint and then back. Round-trip times of 200 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="d09ef-p120">Hohe Roundtripwerte können durch internationale Anrufweiterleitung, eine falsche Routingkonfiguration oder einen überlasteten Medienserver verursacht werden. Sie führen zu Problemen bei bidirektionalen Echtzeit-Audiounterhaltungen.</span><span class="sxs-lookup"><span data-stu-id="d09ef-p120">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d09ef-211"><strong>Paketverlust</strong></span><span class="sxs-lookup"><span data-stu-id="d09ef-211"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="d09ef-212">Nein</span><span class="sxs-lookup"><span data-stu-id="d09ef-212">No</span></span></p></td>
<td><p><span data-ttu-id="d09ef-p121">Die durchschnittliche Rate an RTP-Paketverlusten (Real-Time Transport-Protokoll; ein Protokoll für die Übertragung von Audio und Video über das Internet). Zu Paketverlusten kommt es, wenn RTP-Pakete ihr Ziel nicht erreichen. Hohe Verlustraten werden allgemein durch Überlastung, zu geringe Bandbreite, Funknetzüberlastung oder -interferenzen oder durch einen überlasteten Medienserver verursacht. Paketverluste führen in der Regel zu verzerrter oder unterbrochener Sprachübertragung.</span><span class="sxs-lookup"><span data-stu-id="d09ef-p121">Average rate of Real-Time Transport Protocol (RTP) packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09ef-216"><strong>Jitter (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="d09ef-216"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="d09ef-217">Nein</span><span class="sxs-lookup"><span data-stu-id="d09ef-217">No</span></span></p></td>
<td><p><span data-ttu-id="d09ef-218">Der durchschnittliche Jitter, der zwischen dem Eintreffen von RTP-Paketen ermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="d09ef-218">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="d09ef-219">(Jitter ist ein Maß für die &quot; Zittern eines &quot; Anrufs.) Starke Jitterwerte werden in der Regel durch Überlastung oder einen überladenen Medienserver verursacht, was zu verzerrten oder verlorenen Audiodaten führt.</span><span class="sxs-lookup"><span data-stu-id="d09ef-219">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d09ef-220"><strong>Ausblendungsverhältnis der Reparatur</strong></span><span class="sxs-lookup"><span data-stu-id="d09ef-220"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09ef-221">Nein</span><span class="sxs-lookup"><span data-stu-id="d09ef-221">No</span></span></p></td>
<td><p><span data-ttu-id="d09ef-p123">Das durchschnittliche Verhältnis zwischen ausgeblendeten Audiosamples und der Gesamtzahl der Samples. (Ausgeblendete Audiosamples sind ein Verfahren zum „Glätten“ der „holprigen“ Übertragung, die normalerweise von verworfenen Netzwerkpaketen verursacht wird.) Ein hoher Wert gibt an, dass wegen Paketverlusten oder Jitters Verlustausblendung in großem Umfang angewendet wurde und führt zu verzerrter oder unterbrochener Sprachübertragung.</span><span class="sxs-lookup"><span data-stu-id="d09ef-p123">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d09ef-224"><strong>Streckungsverhältnis der Reparatur</strong></span><span class="sxs-lookup"><span data-stu-id="d09ef-224"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09ef-225">Nein</span><span class="sxs-lookup"><span data-stu-id="d09ef-225">No</span></span></p></td>
<td><p><span data-ttu-id="d09ef-p124">Das durchschnittliche Verhältnis zwischen gestreckten Audiosamples und der Gesamtzahl der Samples. (Gestrecktes Audio ist ein Verfahren zum Dehnen von Audiodaten, um die Gesprächsqualität aufrechtzuerhalten, wenn ein verworfenes Netzwerkpaket festgestellt wurde.) Ein hoher Wert gibt an, dass wegen Jitters Samplestreckung in hohem Umfang aufgetreten ist und führt zu roboterhafter oder verzerrter Sprachqualität.</span><span class="sxs-lookup"><span data-stu-id="d09ef-p124">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d09ef-228"><strong>Komprimierungsverhältnis der Reparatur</strong></span><span class="sxs-lookup"><span data-stu-id="d09ef-228"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="d09ef-229">Nein</span><span class="sxs-lookup"><span data-stu-id="d09ef-229">No</span></span></p></td>
<td><p><span data-ttu-id="d09ef-p125">Das durchschnittliche Verhältnis zwischen komprimierten Audiosamples und der Gesamtzahl der Samples. (Komprimiertes Audio sind Audiodaten, die komprimiert wurden, um die Gesprächsqualität aufrechtzuerhalten, wenn ein verworfenes Netzwerkpaket festgestellt wurde.) Ein hoher Wert gibt an, dass wegen Jitters Samplekomprimierung in hohem Umfang angewendet wurde und führt zu einer zu schnellen Sprachwiedergabe oder zu verzerrter Sprachqualität.</span><span class="sxs-lookup"><span data-stu-id="d09ef-p125">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="d09ef-232">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d09ef-232">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

