---
title: 'Lync Server 2013: Fehler Verteilungs Bericht'
description: 'Lync Server 2013: Fehler Verteilungs Bericht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failure Distribution Report
ms:assetid: 365c7beb-24d4-40f5-92e7-4978b9688916
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558635(v=OCS.15)
ms:contentKeyID: 48183849
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5a87f779f87d6b7002fa108f1969c33739eed9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428216"
---
# <a name="failure-distribution-report-in-lync-server-2013"></a><span data-ttu-id="5cc00-103">Bericht zur Fehlerverteilung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5cc00-103">Failure Distribution Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5cc00-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5cc00-104">

<span> </span></span></span>

<span data-ttu-id="5cc00-105">_**Letztes Änderungsdatum des Themas:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="5cc00-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="5cc00-106">Der Bericht über Fehlerverteilung ordnet Sitzungen, bei denen ein Fehler aufgetreten ist, in folgende Kategorien ein:</span><span class="sxs-lookup"><span data-stu-id="5cc00-106">The Failure Distribution Report ranks failed sessions in the following categories:</span></span>

  - <span data-ttu-id="5cc00-107">Häufigste Diagnosegründe</span><span class="sxs-lookup"><span data-stu-id="5cc00-107">Top diagnostic reasons</span></span>

  - <span data-ttu-id="5cc00-108">Häufigste Modalitäten</span><span class="sxs-lookup"><span data-stu-id="5cc00-108">Top modalities</span></span>

  - <span data-ttu-id="5cc00-109">Häufigste Pools</span><span class="sxs-lookup"><span data-stu-id="5cc00-109">Top pools</span></span>

  - <span data-ttu-id="5cc00-110">Häufigste Quellen</span><span class="sxs-lookup"><span data-stu-id="5cc00-110">Top sources</span></span>

  - <span data-ttu-id="5cc00-111">Häufigste Komponenten</span><span class="sxs-lookup"><span data-stu-id="5cc00-111">Top components</span></span>

  - <span data-ttu-id="5cc00-112">Häufigste Absenderbenutzer</span><span class="sxs-lookup"><span data-stu-id="5cc00-112">Top from users</span></span>

  - <span data-ttu-id="5cc00-113">Häufigste Empfängerbenutzer</span><span class="sxs-lookup"><span data-stu-id="5cc00-113">Top to users</span></span>

  - <span data-ttu-id="5cc00-114">Häufigste Absenderbenutzer-Agenten</span><span class="sxs-lookup"><span data-stu-id="5cc00-114">Top from user agents</span></span>

<span data-ttu-id="5cc00-p101">Anhand dieser Kategorien können Sie genau bestimmen, wo ein Problem aufgetreten ist und in einigen Fällen auch die Ursache feststellen. Angenommen, an einem Tag sind bei 242 Audio- und Videositzungen Fehler aufgetreten. Wenn Sie sich den Bericht über Fehlerverteilung ansehen, stellen Sie möglicherweise fest, dass 237 dieser gescheiterten Sitzungen im Dublin-Pool aufgetreten sind. Dies gibt Ihnen einen guten Ausgangspunkt zum Einkreisen der Ursache und Diagnostizieren dieser Fehler. Wenn Sie in der Kategorie **Häufigste Pools** auf den Dublin-Pool klicken, sehen Sie einen Bericht über Fehlerverteilung nur für diesen Pool. Sie können dann mit der Analyse des Dublin-Pools beginnen, um herauszufinden, warum es so viele Schwierigkeiten gab.</span><span class="sxs-lookup"><span data-stu-id="5cc00-p101">You can use these categories to determine exactly where a problem is occurring and, in some cases, why the problem is occurring. For example, suppose you recorded 242 failed audio/video sessions during a given day. If you look at the Failure Distribution Report, it might show that 237 of those failed sessions took place in your Dublin pool. That gives you a good place to start when it comes to tracking down and diagnosing the causes behind those failures. If you click on the Dublin pool under the **Top pools** category, you will see a Failure Distribution Report just for that pool. You can then begin analyzing why the Dublin pool was experiencing so many difficulties.</span></span>

<div>

## <a name="viewing-the-failure-distribution-report"></a><span data-ttu-id="5cc00-121">Anzeigen des Berichts über Fehlerverteilung</span><span class="sxs-lookup"><span data-stu-id="5cc00-121">Viewing the Failure Distribution Report</span></span>

<span data-ttu-id="5cc00-122">Sie können auf den Bericht über Fehlerverteilung von einem der folgenden Berichte zugreifen, indem Sie entweder auf die Metrik **Anzahl der erwarteten Fehler** oder **Anzahl der unerwarteten Fehler** klicken:</span><span class="sxs-lookup"><span data-stu-id="5cc00-122">You can access the Failure Distribution Report from any of the following reports by clicking either the **Expected failure volume** or the **Unexpected failure volume** metric:</span></span>

  - [<span data-ttu-id="5cc00-123">Bericht "Top-Fehler" in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5cc00-123">Top Failures Report in Lync Server 2013</span></span>](lync-server-2013-top-failures-report.md)

  - [<span data-ttu-id="5cc00-124">Konferenz Diagnosebericht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5cc00-124">Conference Diagnostic Report in Lync Server 2013</span></span>](lync-server-2013-conference-diagnostic-report.md)

  - [<span data-ttu-id="5cc00-125">Diagnosebericht zur Peer-to-Peer-Aktivität in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5cc00-125">Peer-to-Peer Activity Diagnostic Report in Lync Server 2013</span></span>](lync-server-2013-peer-to-peer-activity-diagnostic-report.md)

<span data-ttu-id="5cc00-126">Im Bericht Fehlerverteilung können Sie auf eine der folgenden Metriken klicken, um den [fehlerlistenbericht in lync Server 2013](lync-server-2013-failure-list-report.md)anzuzeigen:</span><span class="sxs-lookup"><span data-stu-id="5cc00-126">From the Failure Distribution Report, you can click any of the following metrics to view the [Failure List Report in Lync Server 2013](lync-server-2013-failure-list-report.md):</span></span>

  - <span data-ttu-id="5cc00-127">Wichtigste Diagnosegründe (Sitzungen)</span><span class="sxs-lookup"><span data-stu-id="5cc00-127">Top diagnostic reasons (sessions)</span></span>

  - <span data-ttu-id="5cc00-128">Wichtigste Modalitäten (Sitzungen)</span><span class="sxs-lookup"><span data-stu-id="5cc00-128">Top modalities (sessions)</span></span>

  - <span data-ttu-id="5cc00-129">Wichtigste Pools (Sitzungen)</span><span class="sxs-lookup"><span data-stu-id="5cc00-129">Top pools (sessions)</span></span>

  - <span data-ttu-id="5cc00-130">Wichtigste Quellen (Sitzungen)</span><span class="sxs-lookup"><span data-stu-id="5cc00-130">Top sources (sessions)</span></span>

  - <span data-ttu-id="5cc00-131">Wichtigste Komponenten (Sitzungen)</span><span class="sxs-lookup"><span data-stu-id="5cc00-131">Top components (sessions)</span></span>

  - <span data-ttu-id="5cc00-132">Wichtigste Absenderbenutzer (Sitzungen)</span><span class="sxs-lookup"><span data-stu-id="5cc00-132">Top from users (sessions)</span></span>

  - <span data-ttu-id="5cc00-133">Wichtigste Empfängerbenutzer (Sitzungen)</span><span class="sxs-lookup"><span data-stu-id="5cc00-133">Top to users (sessions)</span></span>

  - <span data-ttu-id="5cc00-134">Wichtigste Absenderbenutzer-Agenten (Sitzungen)</span><span class="sxs-lookup"><span data-stu-id="5cc00-134">Top from user agents (sessions)</span></span>

</div>

<div>

## <a name="using-the-failure-distribution-report"></a><span data-ttu-id="5cc00-135">Verwenden des Berichts über Fehlerverteilung</span><span class="sxs-lookup"><span data-stu-id="5cc00-135">Using the Failure Distribution Report</span></span>

<span data-ttu-id="5cc00-p102">Je nach Ihrer Monitorgröße und Bildschirmauflösung werden einige Daten im Bericht über Fehlerverteilung möglicherweise abgeschnitten, wenn Sie auf dem Bildschirm angezeigt werden. Dies ist insbesondere bei Agent-Benutzern der Fall, die sehr lange Bezeichnungen haben können. Auf dem Bildschirm wird ein Benutzer-Agent mit dem Namen „UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Lync 2013)“ z. B. nur teilweise angezeigt:</span><span class="sxs-lookup"><span data-stu-id="5cc00-p102">Depending on your monitor size and screen resolution, it's possible that some of the data shown in the Failure Distribution Report might be truncated when you view it onscreen. This is especially true for metrics such as user agents, which can have very long labels. For example, a user agent with a name like "UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Lync 2013)" might only partially appear onscreen:</span></span>

<span data-ttu-id="5cc00-139">UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Ly...</span><span class="sxs-lookup"><span data-stu-id="5cc00-139">UCCAPI/4.0.7400.0 OC/4.0.7400.0 (Microsoft Ly...</span></span>

<span data-ttu-id="5cc00-140">Sie können aber die gesamte Bezeichnung anzeigen, indem Sie die Maus über den gekürzten Wert halten.</span><span class="sxs-lookup"><span data-stu-id="5cc00-140">Fortunately, you can see the entire label simply by holding your mouse over the truncated value.</span></span>

<span data-ttu-id="5cc00-p103">Eine interessante Metrik, nach der Sie im Bericht über Fehlerverteilung filtern können, ist die Diagnose-ID. Wenn Sie dieselbe Diagnose-ID auch in anderen Berichten sehen, können Sie nach dieser ID im Bericht über Fehlerverteilung filtern. Sie erhalten dann einen sehr detaillierten Einblick darüber, wo genau und wie oft diese ID in einer gescheiterten Sitzung gemeldet wurde.</span><span class="sxs-lookup"><span data-stu-id="5cc00-p103">One interesting metric that you can filter on by using the Failure Distribution Report is Diagnostic ID. If you see the same Diagnostic ID cropping up in other reports you can filter on that ID in the Failure Distribution Report and get a very detailed look at exactly where, and how often, that ID has been reported during a failed session.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="5cc00-143">Filter</span><span class="sxs-lookup"><span data-stu-id="5cc00-143">Filters</span></span>

<span data-ttu-id="5cc00-p104">Mithilfe von Filtern können Sie eine gezieltere Datenauswahl zurückgeben oder die zurückgegebenen Daten auf unterschiedliche Weise anzeigen. Mit dem Bericht über Fehlerverteilung können Sie beispielsweise nach Kriterien wie dem Aktivitätstyp (Peer-to-Peer-Sitzung oder Konferenzsitzung) oder nach der Diagnose-ID der jeweiligen fehlgeschlagenen Sitzung filtern.</span><span class="sxs-lookup"><span data-stu-id="5cc00-p104">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Failed Distribution Report enables you to filter on such things as the activity type (peer-to-peer session or conferencing session) or by the diagnostic ID that accompanied each failed session.</span></span>

<span data-ttu-id="5cc00-146">In der folgenden Tabelle sind die Filter aufgeführt, die Sie im Bericht über Fehlerverteilung verwenden können.</span><span class="sxs-lookup"><span data-stu-id="5cc00-146">The following table lists the filters that you can use with the Failure Distribution Report.</span></span>

### <a name="failure-distribution-report-filters"></a><span data-ttu-id="5cc00-147">Bericht über Fehlerverteilung - Filter</span><span class="sxs-lookup"><span data-stu-id="5cc00-147">Failure Distribution Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5cc00-148">Name</span><span class="sxs-lookup"><span data-stu-id="5cc00-148">Name</span></span></th>
<th><span data-ttu-id="5cc00-149">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cc00-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-150"><strong>Von</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-150"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-p105">Anfangsdatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Anfangsdatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="5cc00-p105">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="5cc00-153">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="5cc00-153">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="5cc00-p106">Wenn Sie keinen Anfangszeitpunkt eingeben, beginnt der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="5cc00-p106">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="5cc00-156">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="5cc00-156">7/7/2012</span></span></p>
<p><span data-ttu-id="5cc00-157">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="5cc00-157">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="5cc00-158">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="5cc00-158">7/3/2012</span></span></p>
<p><span data-ttu-id="5cc00-159">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="5cc00-159">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cc00-160"><strong>Bis</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-160"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-p107">Enddatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Enddatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="5cc00-p107">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="5cc00-163">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="5cc00-163">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="5cc00-p108">Wenn Sie keinen Endzeitpunkt eingeben, endet der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="5cc00-p108">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="5cc00-166">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="5cc00-166">7/7/2012</span></span></p>
<p><span data-ttu-id="5cc00-167">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="5cc00-167">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="5cc00-168">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="5cc00-168">7/3/2012</span></span></p>
<p><span data-ttu-id="5cc00-169">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="5cc00-169">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-170"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-170"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-p109">Vollqualifizierter Domänenname (FQDN) des Registrierungspools oder Edgeservers. Sie können einen einzelnen Pool auswählen oder auf <strong>[Alle]</strong> klicken, um die Daten für alle Pools anzuzeigen. Diese Dropdownliste wird basierend auf den Datensätzen in der Datenbank automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="5cc00-p109">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cc00-174"><strong>Aktivitätstyp</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-174"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-p110">Aktivitätstyp, nach dem gefiltert wird. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="5cc00-p110">Type of activity to filter on. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="5cc00-177">[Alle]</span><span class="sxs-lookup"><span data-stu-id="5cc00-177">[All]</span></span></p></li>
<li><p><span data-ttu-id="5cc00-178">Peer-to-Peer</span><span class="sxs-lookup"><span data-stu-id="5cc00-178">Peer-to-peer</span></span></p></li>
<li><p><span data-ttu-id="5cc00-179">Konferenz</span><span class="sxs-lookup"><span data-stu-id="5cc00-179">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-180"><strong>Sitzungskategorie</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-180"><strong>Session category</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-p111">Gibt an, ob die betreffende Aktivität erfolgreich war oder nicht. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="5cc00-p111">Indicates whether the activity in question succeeded or failed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="5cc00-183">[Alle]</span><span class="sxs-lookup"><span data-stu-id="5cc00-183">[All]</span></span></p></li>
<li><p><span data-ttu-id="5cc00-184">Erfolg</span><span class="sxs-lookup"><span data-stu-id="5cc00-184">Success</span></span></p></li>
<li><p><span data-ttu-id="5cc00-185">Erwarteter Fehler</span><span class="sxs-lookup"><span data-stu-id="5cc00-185">Expected failure</span></span></p></li>
<li><p><span data-ttu-id="5cc00-186">Unerwarteter Fehler</span><span class="sxs-lookup"><span data-stu-id="5cc00-186">Unexpected failure</span></span></p></li>
</ul>
<p><span data-ttu-id="5cc00-187">&quot;Bei einem erwarteten Fehler handelt es sich &quot; um einen Fehler, der erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="5cc00-187">An &quot;expected failure&quot; is a failure that is expected to happen.</span></span> <span data-ttu-id="5cc00-188">Hat beispielsweise ein Benutzer seinen Status auf „Nicht stören“ gesetzt, ist zu erwarten, dass alle Anrufe an diesen Benutzer fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="5cc00-188">For example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span> <span data-ttu-id="5cc00-189">&quot;Bei einem unerwarteten Fehler &quot; handelt es sich um einen Fehler, der in einem ansonsten fehlerhaften System auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="5cc00-189">An &quot;unexpected failure&quot; is a failure that occurs in what would appear to be an otherwise healthy system.</span></span> <span data-ttu-id="5cc00-190">Beispielsweise sollte ein Anruf nicht abgebrochen werden, während der Anrufer sich in der Warteschleife befindet.</span><span class="sxs-lookup"><span data-stu-id="5cc00-190">For example, a call should not be terminated if the caller is placed on hold.</span></span> <span data-ttu-id="5cc00-191">In diesem Fall würde der Fehler als „unerwartet“ gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="5cc00-191">If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cc00-192"><strong>Diagnose-ID</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-192"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-p113">Eindeutige ID (in der Form eines Headers vom Typ „ms-diagnostics“), die an eine SIP-Nachricht angehängt wird und oft nützliche Informationen für die Fehlerbehebung bereitstellt. Diagnostics-Header sind optional (SIP-Sitzungen ohne diese Header sind möglich) und Diagnose-IDs werden nur für Sitzungen berichtet, bei denen Probleme aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="5cc00-p113">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-diagnostic-reasons"></a><span data-ttu-id="5cc00-195">Metriken für die wichtigsten Diagnosegründe</span><span class="sxs-lookup"><span data-stu-id="5cc00-195">Metrics for Top Diagnostic Reasons</span></span>

<span data-ttu-id="5cc00-196">In der folgenden Tabelle sind die im Bericht über Fehlerverteilung enthaltenen Informationen aufgeführt, basierend auf der am häufigsten berichteten Diagnose-ID.</span><span class="sxs-lookup"><span data-stu-id="5cc00-196">The following table lists the information provided in the Failure Distribution Report based on the most frequently reported diagnostic ID.</span></span>

### <a name="metrics-for-top-diagnostic-reasons"></a><span data-ttu-id="5cc00-197">Metriken für die wichtigsten Diagnosegründe</span><span class="sxs-lookup"><span data-stu-id="5cc00-197">Metrics for Top Diagnostic Reasons</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5cc00-198">Name</span><span class="sxs-lookup"><span data-stu-id="5cc00-198">Name</span></span></th>
<th><span data-ttu-id="5cc00-199">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="5cc00-199">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="5cc00-200">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cc00-200">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-201"><strong>Rang</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-201"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-202">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-202">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-p114">Relative Rangordnung der fehlgeschlagenen Sitzungen basierend auf Diagnose-IDs. Die Diagnose-ID ist eine eindeutige ID (in der Form eines Headers vom Typ „ms-diagnostics“), die an eine SIP-Nachricht angehängt wird und oft nützliche Informationen für die Fehlerbehebung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="5cc00-p114">Relative ranking of failed sessions based on diagnostic IDs. The diagnostic ID is a unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cc00-205"><strong>Häufigste Diagnosegründe</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-205"><strong>Top diagnostic reasons</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-206">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-206">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-207">In einer Sitzung generierte Diagnose-ID.</span><span class="sxs-lookup"><span data-stu-id="5cc00-207">Diagnostic ID generated in a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-208"><strong>Sitzungen</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-208"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-209">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-209">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-210">Gesamtanzahl der fehlgeschlagenen Sitzungen, für die die angegebene Diagnose-ID generiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5cc00-210">Total number of failed sessions where the specified diagnostic ID was generated.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-modalities"></a><span data-ttu-id="5cc00-211">Metriken für die wichtigsten Modalitäten</span><span class="sxs-lookup"><span data-stu-id="5cc00-211">Metrics for Top Modalities</span></span>

<span data-ttu-id="5cc00-212">In der folgenden Tabelle sind die im Bericht über Fehlerverteilung enthaltenen Informationen aufgeführt, basierend auf den Sitzungsmodalitäten, bei denen die meisten Fehler auftraten.</span><span class="sxs-lookup"><span data-stu-id="5cc00-212">The following table lists the information provided in the Failure Distribution Report based on the session modalities that experienced the most failures.</span></span>

### <a name="metrics-for-top-modalities"></a><span data-ttu-id="5cc00-213">Metriken für die wichtigsten Modalitäten</span><span class="sxs-lookup"><span data-stu-id="5cc00-213">Metrics for Top Modalities</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5cc00-214">Name</span><span class="sxs-lookup"><span data-stu-id="5cc00-214">Name</span></span></th>
<th><span data-ttu-id="5cc00-215">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="5cc00-215">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="5cc00-216">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cc00-216">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-217"><strong>Rang</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-217"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-218">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-218">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-219">Relative Rangordnung basierend auf der gescheiterten Sitzung und auf dem Sitzungstyp (z. B. Audio-/Video-Konferenz oder Peer-to-Peer-Dateiübertragungssitzung).</span><span class="sxs-lookup"><span data-stu-id="5cc00-219">Relative ranking based of failed session based on session type (for example, an audio/video conference or a peer-to-peer file transfer session).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cc00-220"><strong>Häufigste Modalitäten</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-220"><strong>Top modalities</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-221">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-221">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-222">Sitzungstyp</span><span class="sxs-lookup"><span data-stu-id="5cc00-222">Session type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-223"><strong>Sitzungen</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-223"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-224">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-224">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-225">Gesamtanzahl der fehlgeschlagenen Sitzungen mit der angegebenen Modalität.</span><span class="sxs-lookup"><span data-stu-id="5cc00-225">Total number of failed sessions involving the specified modality.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-pools"></a><span data-ttu-id="5cc00-226">Metriken für die wichtigsten Pools</span><span class="sxs-lookup"><span data-stu-id="5cc00-226">Metrics for Top Pools</span></span>

<span data-ttu-id="5cc00-227">In der folgenden Tabelle sind die im Bericht über Fehlerverteilung enthaltenen Informationen aufgeführt, basierend auf den Pools, bei denen die meisten Fehler auftraten.</span><span class="sxs-lookup"><span data-stu-id="5cc00-227">The following table lists the information provided in the Failure Distribution Report based on the pools that experienced the most failures.</span></span>

### <a name="metrics-for-top-pools"></a><span data-ttu-id="5cc00-228">Metriken für die wichtigsten Pools</span><span class="sxs-lookup"><span data-stu-id="5cc00-228">Metrics for Top Pools</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5cc00-229">Name</span><span class="sxs-lookup"><span data-stu-id="5cc00-229">Name</span></span></th>
<th><span data-ttu-id="5cc00-230">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="5cc00-230">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="5cc00-231">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cc00-231">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-232"><strong>Rang</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-232"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-233">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-233">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-234">Relative Rangfolge der fehlgeschlagenen Sitzungen auf Grundlage des registrierungspools oder des Edge-Servers, auf dem die Sitzung ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="5cc00-234">Relative ranking of failed sessions based on the Registrar pool or Edge Server where the session was conducted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cc00-235"><strong>Häufigste Pools</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-235"><strong>Top pools</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-236">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-236">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-237">Der Name des registrierungspools oder des Edge-Servers.</span><span class="sxs-lookup"><span data-stu-id="5cc00-237">Name of the Registrar pool or Edge Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-238"><strong>Sitzungen</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-238"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-239">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-239">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-240">Die Gesamtzahl der fehlgeschlagenen Sitzungen pro Registrierungspool oder Edgeserver.</span><span class="sxs-lookup"><span data-stu-id="5cc00-240">Total number of failed sessions per Registrar pool or Edge Server.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-sources"></a><span data-ttu-id="5cc00-241">Metriken für die wichtigsten Quellen</span><span class="sxs-lookup"><span data-stu-id="5cc00-241">Metrics for Top Sources</span></span>

<span data-ttu-id="5cc00-242">In der folgenden Tabelle sind die im Bericht über Fehlerverteilung enthaltenen Informationen aufgeführt, basierend auf den Computern, bei denen die meisten Fehler auftraten.</span><span class="sxs-lookup"><span data-stu-id="5cc00-242">The following table lists the information provided in the Failure Distribution Report based on the computers that experienced the most failures.</span></span>

### <a name="metrics-for-top-sources"></a><span data-ttu-id="5cc00-243">Metriken für die wichtigsten Quellen</span><span class="sxs-lookup"><span data-stu-id="5cc00-243">Metrics for Top Sources</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5cc00-244">Name</span><span class="sxs-lookup"><span data-stu-id="5cc00-244">Name</span></span></th>
<th><span data-ttu-id="5cc00-245">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="5cc00-245">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="5cc00-246">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cc00-246">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-247"><strong>Rang</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-247"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-248">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-248">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-249">Relative Rangordnung der fehlgeschlagenen Sitzungen pro Computer.</span><span class="sxs-lookup"><span data-stu-id="5cc00-249">Relative ranking failed sessions per computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cc00-250"><strong>Häufigste Quellen</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-250"><strong>Top sources</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-251">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-251">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-252">Name des Computers, auf dem die Sitzung fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="5cc00-252">Name of the computer involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-253"><strong>Sitzungen</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-253"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-254">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-254">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-255">Gesamtanzahl der fehlgeschlagenen Sitzungen pro Computer.</span><span class="sxs-lookup"><span data-stu-id="5cc00-255">Total number of failed sessions per computer.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-components"></a><span data-ttu-id="5cc00-256">Metriken für die wichtigsten Komponenten</span><span class="sxs-lookup"><span data-stu-id="5cc00-256">Metrics for Top Components</span></span>

<span data-ttu-id="5cc00-257">In der folgenden Tabelle sind die Informationen aufgeführt, die im Fehler Verteilungs Bericht basierend auf den Microsoft lync Server 2010-Komponenten bereitgestellt werden, bei denen die meisten Fehler aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="5cc00-257">The following table lists the information provided in the Failure Distribution Report based on the Microsoft Lync Server 2010 components that experienced the most failures.</span></span>

### <a name="metrics-for-top-components"></a><span data-ttu-id="5cc00-258">Metriken für die wichtigsten Komponenten</span><span class="sxs-lookup"><span data-stu-id="5cc00-258">Metrics for Top Components</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5cc00-259">Name</span><span class="sxs-lookup"><span data-stu-id="5cc00-259">Name</span></span></th>
<th><span data-ttu-id="5cc00-260">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="5cc00-260">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="5cc00-261">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cc00-261">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-262"><strong>Rang</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-262"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-263">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-263">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-264">Relative Rangfolge fehlerhafter Sitzungen basierend auf der lync Server 2010-Komponente (beispielsweise ExumRouting, GroupChat oder MediationServer).</span><span class="sxs-lookup"><span data-stu-id="5cc00-264">Relative ranking of failed sessions based on Lync Server 2010 component (for example, ExumRouting, GroupChat, or MediationServer).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cc00-265"><strong>Häufigste Komponenten</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-265"><strong>Top components</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-266">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-266">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-267">Name der für die fehlgeschlagene Sitzung verwendeten Komponente.</span><span class="sxs-lookup"><span data-stu-id="5cc00-267">Name of the component involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-268"><strong>Sitzungen</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-268"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-269">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-269">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-270">Gesamtanzahl der fehlgeschlagenen Sitzungen pro Komponente.</span><span class="sxs-lookup"><span data-stu-id="5cc00-270">Total number of failed sessions per component.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-from-users"></a><span data-ttu-id="5cc00-271">Metriken für die wichtigsten Absenderbenutzer</span><span class="sxs-lookup"><span data-stu-id="5cc00-271">Metrics for Top From Users</span></span>

<span data-ttu-id="5cc00-272">In der folgenden Tabelle sind die im Bericht über Fehlerverteilung enthaltenen Informationen aufgeführt, basierend auf den Benutzern, bei denen beim Versuch, jemanden anzurufen, die meisten Fehler auftraten (als Absenderbenutzer bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="5cc00-272">The following table lists the information provided in the Failure Distribution Report based on users who experienced the most failures when they tried to call someone else (known as "From" users).</span></span>

### <a name="metrics-for-top-from-users"></a><span data-ttu-id="5cc00-273">Metriken für die wichtigsten Absenderbenutzer</span><span class="sxs-lookup"><span data-stu-id="5cc00-273">Metrics for Top From Users</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5cc00-274">Name</span><span class="sxs-lookup"><span data-stu-id="5cc00-274">Name</span></span></th>
<th><span data-ttu-id="5cc00-275">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="5cc00-275">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="5cc00-276">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cc00-276">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-277"><strong>Rang</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-277"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-278">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-278">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-279">Relative Rangordnung der fehlgeschlagenen Sitzungen basierend auf dem Benutzer, der zur Teilnahme an der Sitzung eingeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="5cc00-279">Relative ranking of failed sessions based on the user who was invited to join the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cc00-280"><strong>Häufigste Absenderbenutzer</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-280"><strong>Top from users</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-281">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-281">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-282">SIP-Adresse des Benutzers, der zur Teilnahme an der Sitzung eingeladen wurde.</span><span class="sxs-lookup"><span data-stu-id="5cc00-282">SIP address of the user invited to join the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-283"><strong>Sitzungen</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-283"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-284">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-284">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-285">Gesamtanzahl der fehlgeschlagenen Sitzungen pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="5cc00-285">Total number of failed sessions per user.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-to-users"></a><span data-ttu-id="5cc00-286">Metriken für die wichtigsten Empfängerbenutzer</span><span class="sxs-lookup"><span data-stu-id="5cc00-286">Metrics for Top To Users</span></span>

<span data-ttu-id="5cc00-287">In der folgenden Tabelle sind die im Bericht über Fehlerverteilung enthaltenen Informationen aufgeführt, basierend auf den Benutzern, bei denen die meisten Fehler auftraten, wenn sie von einem anderen Benutzer angerufen wurden (als Empfängerbenutzer bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="5cc00-287">The following table lists the information provided in the Failure Distribution Report based on the users who experienced the most failures when another user tried to call them (known as "To" users).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5cc00-288">Name</span><span class="sxs-lookup"><span data-stu-id="5cc00-288">Name</span></span></th>
<th><span data-ttu-id="5cc00-289">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="5cc00-289">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="5cc00-290">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cc00-290">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-291"><strong>Rang</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-291"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-292">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-292">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-293">Relative Rangordnung der fehlgeschlagenen Sitzungen basierend auf dem Benutzer, der die Sitzung initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="5cc00-293">Relative ranking of failed sessions based on the user who initiated the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cc00-294"><strong>Häufigste Empfängerbenutzer</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-294"><strong>Top to users</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-295">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-295">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-296">SIP-Adresse des Benutzers, der die Sitzung initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="5cc00-296">SIP address of the user who initiated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-297"><strong>Sitzungen</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-297"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-298">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-298">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-299">Gesamtanzahl der fehlgeschlagenen Sitzungen pro Benutzer.</span><span class="sxs-lookup"><span data-stu-id="5cc00-299">Total number of failed sessions per user.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics-for-top-user-agents"></a><span data-ttu-id="5cc00-300">Metriken für die wichtigsten Benutzer-Agenten</span><span class="sxs-lookup"><span data-stu-id="5cc00-300">Metrics for Top User Agents</span></span>

<span data-ttu-id="5cc00-301">In der folgenden Tabelle sind die im Bericht über Fehlerverteilung enthaltenen Informationen aufgeführt, basierend auf der Endpunktsoftware, bei der die meisten Fehler auftraten.</span><span class="sxs-lookup"><span data-stu-id="5cc00-301">The following table lists the information provided in the Failure Distribution Report based on the endpoint software that experienced the most failures.</span></span>

### <a name="metrics-for-top-user-agents"></a><span data-ttu-id="5cc00-302">Metriken für die wichtigsten Benutzer-Agenten</span><span class="sxs-lookup"><span data-stu-id="5cc00-302">Metrics for Top User Agents</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5cc00-303">Name</span><span class="sxs-lookup"><span data-stu-id="5cc00-303">Name</span></span></th>
<th><span data-ttu-id="5cc00-304">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="5cc00-304">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="5cc00-305">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="5cc00-305">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-306"><strong>Rang</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-306"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-307">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-307">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-p115">Relative Rangordnung der fehlgeschlagenen Sitzungen basierend auf dem in der Sitzung verwendeten Benutzer-Agent (Software), z. B. RTCC/4.0.0.0 Inbound Routing/4.0.0.0.</span><span class="sxs-lookup"><span data-stu-id="5cc00-p115">Relative ranking of failed sessions based on the user agent (software) involved in the session. For example: RTCC/4.0.0.0 Inbound Routing/4.0.0.0.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5cc00-310"><strong>Wichtigste Benutzer-Agenten</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-310"><strong>Top user agents</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-311">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-311">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-312">Name des in der fehlgeschlagenen Sitzung verwendeten Benutzer-Agent.</span><span class="sxs-lookup"><span data-stu-id="5cc00-312">Name of the user agent involved in the failed session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5cc00-313"><strong>Sitzungen</strong></span><span class="sxs-lookup"><span data-stu-id="5cc00-313"><strong>Sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="5cc00-314">Nein</span><span class="sxs-lookup"><span data-stu-id="5cc00-314">No</span></span></p></td>
<td><p><span data-ttu-id="5cc00-315">Gesamtanzahl der fehlgeschlagenen Sitzungen pro Benutzer-Agent.</span><span class="sxs-lookup"><span data-stu-id="5cc00-315">Total number of failed sessions per user agent.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5cc00-316">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5cc00-316">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

