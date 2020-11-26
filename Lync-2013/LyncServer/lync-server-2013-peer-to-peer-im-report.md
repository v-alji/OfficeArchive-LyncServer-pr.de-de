---
title: 'Lync Server 2013: Peer-zu-Peer-Chat Bericht'
description: 'Lync Server 2013: Peer-to-Peer-Chat Bericht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Peer-to-Peer IM Report
ms:assetid: 19ec0145-2398-437b-8989-f780c179b798
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558620(v=OCS.15)
ms:contentKeyID: 48183533
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eac6291d0f099af8269ed15f7dc8c654ac944ed0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424685"
---
# <a name="peer-to-peer-im-report-in-lync-server-2013"></a><span data-ttu-id="bb6d7-103">Peer-zu-Peer-Chat Bericht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb6d7-103">Peer-to-Peer IM Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bb6d7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bb6d7-104">

<span> </span></span></span>

<span data-ttu-id="bb6d7-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="bb6d7-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="bb6d7-p101">Der Bericht über Peer-to-Peer-Sofortnachrichten enthält Trendinformationen zu den Peer-to-Peer-Sofortnachrichtensitzungen, aufgeschlüsselt nach Pool und Authentifizierungstyp. Der Bericht kann entweder die Gesamtanzahl der im angegebenen Zeitraum abgehaltenen Sitzungen (z. B. nach Tag oder nach Stunden) oder die Gesamtanzahl der in diesem Zeitraum gesendeten Sofortnachrichten anzeigen.</span><span class="sxs-lookup"><span data-stu-id="bb6d7-p101">The Peer-to-Peer IM Report provides trend information about peer-to-peer instant messaging (IM) sessions, broken down by pool and by authentication type. The report can show either the total number of sessions held during the specified time period (for example, day-by-day or hour-by-hour), or it can show the total number of instant messages sent during that time period.</span></span>

<div>

## <a name="accessing-the-peer-to-peer-im-report"></a><span data-ttu-id="bb6d7-108">Zugreifen auf den Bericht über Peer-to-Peer-Sofortnachrichten</span><span class="sxs-lookup"><span data-stu-id="bb6d7-108">Accessing the Peer-to-Peer IM Report</span></span>

<span data-ttu-id="bb6d7-109">Sie können nur auf den Chat-Chat Bericht zugreifen, indem Sie den [Bericht Peer-to-Peer-Aktivitätszusammenfassung in lync Server 2013](lync-server-2013-peer-to-peer-activity-summary-report.md) öffnen und dann auf eine der folgenden Metriken klicken:</span><span class="sxs-lookup"><span data-stu-id="bb6d7-109">You can access the Peer-to-Peer IM Report only by opening the [Peer-to-Peer Activity Summary Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-summary-report.md) and then clicking either of the following metrics:</span></span>

  - <span data-ttu-id="bb6d7-110">Peer-to-Peer-Chatsitzungen insgesamt</span><span class="sxs-lookup"><span data-stu-id="bb6d7-110">Total peer-to-peer IM sessions</span></span>

  - <span data-ttu-id="bb6d7-111">Peer-to-Peer-Chatnachrichten insgesamt</span><span class="sxs-lookup"><span data-stu-id="bb6d7-111">Total peer-to-peer IM messages</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-peer-to-peer-im-report"></a><span data-ttu-id="bb6d7-112">Optimales Verwenden des Berichts über Peer-to-Peer-Sofortnachrichten</span><span class="sxs-lookup"><span data-stu-id="bb6d7-112">Making the Best Use of the Peer-to-Peer IM Report</span></span>

<span data-ttu-id="bb6d7-p102">Standardmäßig wird im Bericht über Peer-to-Peer-Sofortnachrichten die Anzahl der Nachrichten pro Stunde (oder, abhängig von Ihren Einstellungen, pro Tag) angezeigt. Sie können jedoch auch den Tag nach Sitzungen pro Stunde anzeigen. Klicken Sie dazu rechts oben im Berichtfenster auf die Schaltfläche zum **Ein- und Ausblenden der Parameter** und klicken Sie dann in der Liste **Bericht nach** auf **Sitzungsanzahl**.</span><span class="sxs-lookup"><span data-stu-id="bb6d7-p102">By default, the Peer-to-Peer IM Report shows you the message count per-hour (or day, depending on your settings). However, you can also choose to view the day by sessions per hour. To do that, click **Hide/Show Parameters** in the upper-right corner of the Reports window, and then click **Session Count** from the **Report by** list.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="bb6d7-116">Filter</span><span class="sxs-lookup"><span data-stu-id="bb6d7-116">Filters</span></span>

<span data-ttu-id="bb6d7-p103">Mithilfe von Filtern können Sie eine gezieltere Datenauswahl erreichen oder die zurückgegebenen Daten auf unterschiedliche Weise anzeigen. In der folgenden Tabelle werden die Filter aufgelistet, die Sie im Bericht über Peer-to-Peer-Sofortnachrichten verwenden können.</span><span class="sxs-lookup"><span data-stu-id="bb6d7-p103">Filters provide a way for you to return a more finely targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Peer-to-Peer IM Report.</span></span>

### <a name="peer-to-peer-im-report-filters"></a><span data-ttu-id="bb6d7-119">Filter im Bericht über Peer-to-Peer-Sofortnachrichten</span><span class="sxs-lookup"><span data-stu-id="bb6d7-119">Peer-to-Peer IM Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb6d7-120">Name</span><span class="sxs-lookup"><span data-stu-id="bb6d7-120">Name</span></span></th>
<th><span data-ttu-id="bb6d7-121">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb6d7-121">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb6d7-122"><strong>Von</strong></span><span class="sxs-lookup"><span data-stu-id="bb6d7-122"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="bb6d7-p104">Anfangsdatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Anfangsdatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="bb6d7-p104">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="bb6d7-125">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="bb6d7-125">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="bb6d7-p105">Wenn Sie keinen Anfangszeitpunkt eingeben, beginnt der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="bb6d7-p105">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="bb6d7-128">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="bb6d7-128">7/7/2012</span></span></p>
<p><span data-ttu-id="bb6d7-129">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die Woche oder den Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="bb6d7-129">To view by week or by month, enter a date that falls anywhere within the week or month (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="bb6d7-130">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="bb6d7-130">7/3/2012</span></span></p>
<p><span data-ttu-id="bb6d7-131">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="bb6d7-131">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb6d7-132"><strong>Bis</strong></span><span class="sxs-lookup"><span data-stu-id="bb6d7-132"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="bb6d7-p106">Enddatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Enddatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="bb6d7-p106">End date and time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="bb6d7-135">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="bb6d7-135">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="bb6d7-p107">Wenn Sie keinen Endzeitpunkt eingeben, endet der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="bb6d7-p107">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="bb6d7-138">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="bb6d7-138">7/7/2012</span></span></p>
<p><span data-ttu-id="bb6d7-139">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="bb6d7-139">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="bb6d7-140">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="bb6d7-140">7/3/2012</span></span></p>
<p><span data-ttu-id="bb6d7-141">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="bb6d7-141">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb6d7-142"><strong>Intervall</strong></span><span class="sxs-lookup"><span data-stu-id="bb6d7-142"><strong>Interval</strong></span></span></p></td>
<td><p><span data-ttu-id="bb6d7-p108">Zeitintervall. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="bb6d7-p108">Time interval. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="bb6d7-145">Stündlich (maximal 25 Stunden können angezeigt werden)</span><span class="sxs-lookup"><span data-stu-id="bb6d7-145">Hourly (a maximum of 25 hours can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="bb6d7-146">Täglich (maximal 31 Tage können angezeigt werden)</span><span class="sxs-lookup"><span data-stu-id="bb6d7-146">Daily (a maximum of 31 days can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="bb6d7-147">Wöchentlich (maximal 12 Wochen können angezeigt werden)</span><span class="sxs-lookup"><span data-stu-id="bb6d7-147">Weekly (a maximum of 12 weeks can be displayed)</span></span></p></li>
<li><p><span data-ttu-id="bb6d7-148">Monatlich (maximal 12 Monate können angezeigt werden)</span><span class="sxs-lookup"><span data-stu-id="bb6d7-148">Monthly (a maximum of 12 months can be displayed)</span></span></p></li>
</ul>
<p><span data-ttu-id="bb6d7-149">Wenn mit dem angegebenen Start- und Endzeitpunkt die maximale Anzahl der zulässigen Werte für das ausgewählte Intervall überschritten wird, wird nur die maximale Anzahl an Werten (beginnend mit dem Startzeitpunkt) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="bb6d7-149">If the start and end dates exceed the maximum number of values allowed for the selected interval then only the maximum number of values (starting from the start date) are displayed.</span></span> <span data-ttu-id="bb6d7-150">Wenn Sie beispielsweise das Tagesintervall mit einem Anfangstermin von 7/7/2012 und einem Enddatum von 2/28/2012 auswählen, werden die Daten für die Tage 8/7/2012 12:00 Uhr bis 9/7/2012 12:00 Uhr angezeigt (also insgesamt 31 Tage).</span><span class="sxs-lookup"><span data-stu-id="bb6d7-150">For example, if you select the Daily interval with a start date of 7/7/2012 and an end date of 2/28/2012, data is displayed for the days 8/7/2012 12:00 AM to 9/7/2012 12:00 AM (that is, a total of 31 days' worth of data).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb6d7-151"><strong>Bericht nach</strong></span><span class="sxs-lookup"><span data-stu-id="bb6d7-151"><strong>Report by</strong></span></span></p></td>
<td><p><span data-ttu-id="bb6d7-p110">Gibt die Werte an, die in dem Bericht verwendet werden sollen. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="bb6d7-p110">Indicates the values to be used in the report. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="bb6d7-154">Sitzungsanzahl</span><span class="sxs-lookup"><span data-stu-id="bb6d7-154">Session count</span></span></p></li>
<li><p><span data-ttu-id="bb6d7-155">Nachrichtenanzahl</span><span class="sxs-lookup"><span data-stu-id="bb6d7-155">Message count</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-im-session-by-pool"></a><span data-ttu-id="bb6d7-156">Metriken für den Bericht über Peer-to-Peer-Sofortnachrichtensitzungen nach Pool</span><span class="sxs-lookup"><span data-stu-id="bb6d7-156">Metrics for Peer-to-Peer IM Session by Pool</span></span>

<span data-ttu-id="bb6d7-157">In der folgenden Tabelle werden die Metriken aufgelistet, die im Bericht über Peer-to-Peer-Sofortnachrichten enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="bb6d7-157">The following table lists the information provided in the Peer-to-Peer IM Report.</span></span>

### <a name="metrics-for-peer-to-peer-im-session-by-pool"></a><span data-ttu-id="bb6d7-158">Metriken für den Bericht über Peer-to-Peer-Sofortnachrichtensitzungen nach Pool</span><span class="sxs-lookup"><span data-stu-id="bb6d7-158">Metrics for Peer-to-Peer IM Session by Pool</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb6d7-159">Name</span><span class="sxs-lookup"><span data-stu-id="bb6d7-159">Name</span></span></th>
<th><span data-ttu-id="bb6d7-160">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="bb6d7-160">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="bb6d7-161">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb6d7-161">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb6d7-162"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="bb6d7-162"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="bb6d7-163">Nein</span><span class="sxs-lookup"><span data-stu-id="bb6d7-163">No</span></span></p></td>
<td><p><span data-ttu-id="bb6d7-164">Der Name des registrierungspools oder des Edge-Servers.</span><span class="sxs-lookup"><span data-stu-id="bb6d7-164">Name of the Registrar pool or Edge Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb6d7-165"><strong>Datum/Uhrzeit</strong></span><span class="sxs-lookup"><span data-stu-id="bb6d7-165"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="bb6d7-166">Nein</span><span class="sxs-lookup"><span data-stu-id="bb6d7-166">No</span></span></p></td>
<td><p><span data-ttu-id="bb6d7-167">Zeitpunkt (Datum und Uhrzeit), zu dem die Sitzungen stattfanden.</span><span class="sxs-lookup"><span data-stu-id="bb6d7-167">Date and time that the sessions took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb6d7-168"><strong>Gesamt</strong></span><span class="sxs-lookup"><span data-stu-id="bb6d7-168"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="bb6d7-169">Nein</span><span class="sxs-lookup"><span data-stu-id="bb6d7-169">No</span></span></p></td>
<td><p><span data-ttu-id="bb6d7-170">Gesamtzahl der Sitzungen bzw. Gesamtzahl der Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="bb6d7-170">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-peer-to-peer-im-session-by-authentication-type"></a><span data-ttu-id="bb6d7-171">Metriken für den Bericht über Peer-to-Peer-Sofortnachrichtensitzungen nach Authentifizierungstyp</span><span class="sxs-lookup"><span data-stu-id="bb6d7-171">Metrics for Peer-to-Peer IM Session by Authentication Type</span></span>

<span data-ttu-id="bb6d7-172">In der folgenden Tabelle werden die Metriken aufgelistet, die im Bericht über Peer-to-Peer-Sofortnachrichten für die einzelnen von den Teilnehmern in einer Peer-to-Peer-Sitzung verwendeten Authentifizierungstypen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="bb6d7-172">The following table lists the information provided in the Peer-to-Peer IM Report for each type of authentication used by the participants in a peer-to-peer session.</span></span>

### <a name="metrics-for-peer-to-peer-im-session-by-authentication-type"></a><span data-ttu-id="bb6d7-173">Metriken für den Bericht über Peer-to-Peer-Sofortnachrichtensitzungen nach Authentifizierungstyp</span><span class="sxs-lookup"><span data-stu-id="bb6d7-173">Metrics for Peer-to-Peer IM Session by Authentication Type</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bb6d7-174">Name</span><span class="sxs-lookup"><span data-stu-id="bb6d7-174">Name</span></span></th>
<th><span data-ttu-id="bb6d7-175">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="bb6d7-175">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="bb6d7-176">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bb6d7-176">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bb6d7-177"><strong>Authentifizierungstyp</strong></span><span class="sxs-lookup"><span data-stu-id="bb6d7-177"><strong>Authentication type</strong></span></span></p></td>
<td><p><span data-ttu-id="bb6d7-178">Nein</span><span class="sxs-lookup"><span data-stu-id="bb6d7-178">No</span></span></p></td>
<td><p><span data-ttu-id="bb6d7-p111">Der von den Sitzungsteilnehmern verwendete Authentifizierungstyp. Folgende Werte sind möglich:</span><span class="sxs-lookup"><span data-stu-id="bb6d7-p111">Type of authentication used by the session participants. Values are typically one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="bb6d7-181">Enterprise</span><span class="sxs-lookup"><span data-stu-id="bb6d7-181">Enterprise</span></span></p></li>
<li><p><span data-ttu-id="bb6d7-182">Federated</span><span class="sxs-lookup"><span data-stu-id="bb6d7-182">Federated</span></span></p></li>
<li><p><span data-ttu-id="bb6d7-183">PIC</span><span class="sxs-lookup"><span data-stu-id="bb6d7-183">PIC</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bb6d7-184"><strong>Datum/Uhrzeit</strong></span><span class="sxs-lookup"><span data-stu-id="bb6d7-184"><strong>Date/Time</strong></span></span></p></td>
<td><p><span data-ttu-id="bb6d7-185">Nein</span><span class="sxs-lookup"><span data-stu-id="bb6d7-185">No</span></span></p></td>
<td><p><span data-ttu-id="bb6d7-186">Zeitpunkt (Datum und Uhrzeit), zu dem die Sitzungen stattfanden.</span><span class="sxs-lookup"><span data-stu-id="bb6d7-186">Date and time that the sessions took place.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bb6d7-187"><strong>Gesamt</strong></span><span class="sxs-lookup"><span data-stu-id="bb6d7-187"><strong>Total</strong></span></span></p></td>
<td><p><span data-ttu-id="bb6d7-188">Nein</span><span class="sxs-lookup"><span data-stu-id="bb6d7-188">No</span></span></p></td>
<td><p><span data-ttu-id="bb6d7-189">Gesamtzahl der Sitzungen bzw. Gesamtzahl der Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="bb6d7-189">Total number of sessions or total message count.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="bb6d7-190">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bb6d7-190">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

