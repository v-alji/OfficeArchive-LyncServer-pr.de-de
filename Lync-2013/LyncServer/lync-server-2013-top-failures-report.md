---
title: 'Lync Server 2013: Bericht "Top-Fehler"'
description: 'Lync Server 2013: Bericht "Top-Fehler".'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Top Failures Report
ms:assetid: 438942e2-580a-4b67-9d42-f116111fb26a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558640(v=OCS.15)
ms:contentKeyID: 48184021
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 768c9a99916dece9eb76877b0cd65b057697ff95
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440913"
---
# <a name="top-failures-report-in-lync-server-2013"></a><span data-ttu-id="e8695-103">Bericht "Top-Fehler" in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e8695-103">Top Failures Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e8695-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e8695-104">

<span> </span></span></span>

<span data-ttu-id="e8695-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="e8695-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="e8695-p101">Der Bericht über häufigste Fehler bietet einen Überblick über die am häufigsten gemeldeten Fehler mit Trenddarstellung. Die Fehler basieren auf einer Kombination der folgenden zwei Metriken:</span><span class="sxs-lookup"><span data-stu-id="e8695-p101">The Top Failures Report provides a look at the most-commonly reported failures and their trends over time. Failures are based on a combination of the following two metrics:</span></span>

  - <span data-ttu-id="e8695-p102">**Diagnose-ID**. Eindeutige ID (in der Form eines Headers vom Typ „ms-diagnostics“), die an eine SIP-Nachricht angehängt wird und oft nützliche Informationen für die Fehlerbehebung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="e8695-p102">**Diagnostic ID**. Unique identifier (in the form of an ms-diagnostics header) that is attached to a SIP message. Diagnostic IDs provide information useful in troubleshooting call-related problems.</span></span>

  - <span data-ttu-id="e8695-111">**Antwortcode**.</span><span class="sxs-lookup"><span data-stu-id="e8695-111">**Response code**.</span></span> <span data-ttu-id="e8695-112">Antwortcodes werden in SIP-Kommunikationssitzungen verwendet, um auf SIP-Anforderungen zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="e8695-112">Response codes are used in SIP communication sessions to respond to SIP requests.</span></span> <span data-ttu-id="e8695-113">Angenommen, Ken sendet die INVITE-Anforderung an Pilar Ackerman (das heißt, Ken Myers ruft Pilar Ackerman an).</span><span class="sxs-lookup"><span data-stu-id="e8695-113">For example, suppose Ken sends the INVITE request to Pilar Ackerman (that is, suppose Ken Myer calls Pilar Ackerman).</span></span> <span data-ttu-id="e8695-114">Wenn Pilar antwortet, sendet Ihr Telefon den Antwortcode 200 (OK) und lässt Ken Telefon wissen, dass Pilar geantwortet hat.</span><span class="sxs-lookup"><span data-stu-id="e8695-114">If Pilar answers, her phone will send the response code 200 (OK), letting Ken's phone know that Pilar has answered.</span></span> <span data-ttu-id="e8695-115">Der Bericht "Top-Fehler" enthält nur Antwortcodes, die als Antwort auf einen Anruf Fehler gesendet wurden. Lync Server verfolgt nicht alle im Laufe eines Anrufs ausgestellten Antwortcodes.</span><span class="sxs-lookup"><span data-stu-id="e8695-115">The Top Failures Report only includes response codes that were sent in response to a call failure; Lync Server does not keep track of all the response codes issued during the course of a call.</span></span>

<span data-ttu-id="e8695-116">Informationen werden nicht nur für die Gesamtzahl an Sitzungen, in denen ein Fehler aufgetreten ist, gemeldet, sondern auch für die Gesamtzahl der Benutzer, die von den Fehlern betroffen waren.</span><span class="sxs-lookup"><span data-stu-id="e8695-116">Information is reported not only for the total number of sessions where a failure occurred but also for the total number of users who were impacted by the failure.</span></span>

<div>

## <a name="accessing-the-top-failures-report"></a><span data-ttu-id="e8695-117">Zugriff auf den Bericht über häufigste Fehler</span><span class="sxs-lookup"><span data-stu-id="e8695-117">Accessing the Top Failures Report</span></span>

<span data-ttu-id="e8695-118">Der Zugriff auf den Bericht über häufigste Fehler erfolgt von der Startseite für Überwachungsberichte aus.</span><span class="sxs-lookup"><span data-stu-id="e8695-118">The Top Failures Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="e8695-119">Wenn Sie auf die Metrik der gemeldeten Sitzungen klicken, gelangen Sie zum [Fehler Verteilungs Bericht in lync Server 2013](lync-server-2013-failure-distribution-report.md).</span><span class="sxs-lookup"><span data-stu-id="e8695-119">Clicking the Reported sessions metric will take you to the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md).</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-top-failures-report"></a><span data-ttu-id="e8695-120">Beste Nutzung des Berichts häufigster Fehler</span><span class="sxs-lookup"><span data-stu-id="e8695-120">Making the Best Use of the Top Failures Report</span></span>

<span data-ttu-id="e8695-p105">Der Bericht häufigster Fehler ist in einer Hinsicht ungewöhnlich: Er ermöglicht Ihnen gleichzeitig, nach bis zu 5 Diagnose-IDs zu filtern (normalerweise kann nur nach einem Element gleichzeitig gefiltert werden, z. B. nach der SIP-Adresse des Benutzers). Um nach mehreren Diagnose-IDs zu filtern, geben Sie einfach alle IDs durch Kommas getrennt in das Feld „Diagnose-IDs“ ein (Sie können, müssen aber nicht nach jedem Komma ein Leerzeichen einfügen). Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e8695-p105">The Top Failures Report is unusual in one regard: it allows you to filter on as many as 5 diagnostic IDs at once. (Typically you can only filter on one item – such as one user SIP address – at a time.) To filter on multiple diagnostic IDs, simply enter each ID in the Diagnostic IDs box, separating the IDs by using commas. (If you want to, you can leave a blank space after each comma.) For example:</span></span>

<span data-ttu-id="e8695-124">1011, 2412, 1033, 52116, 1008</span><span class="sxs-lookup"><span data-stu-id="e8695-124">1011, 2412, 1033, 52116, 1008</span></span>

<span data-ttu-id="e8695-125">Wenn Sie dies tun, werden nur fehlerhafte Anrufe, die mindestens eine dieser fünf Diagnose-IDs gemeldet haben, angezeigt.</span><span class="sxs-lookup"><span data-stu-id="e8695-125">Do that, and only failed calls that reported at least one of those five diagnostic IDs will be displayed.</span></span>

<span data-ttu-id="e8695-p106">Wenn Sie Ihre Maus über einen Antwortcode bewegen, wird eine QuickInfo angezeigt, die Ihnen mitteilt, was der jeweilige Antwortcode bedeutet. Wenn Sie beispielsweise die Maus über den Antwortcode 486 bewegen, wird folgende Meldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="e8695-p106">If you hold your mouse over a Response code you'll see a tooltip that tells you what the Response code in question means. For example, if you hold the mouse over the Response code 486 you'll see this message:</span></span>

<span data-ttu-id="e8695-128">Ausgelastet.</span><span class="sxs-lookup"><span data-stu-id="e8695-128">Busy Here.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="e8695-129">Filter</span><span class="sxs-lookup"><span data-stu-id="e8695-129">Filters</span></span>

<span data-ttu-id="e8695-p107">Mithilfe von Filtern können Sie eine gezieltere Datenauswahl erreichen oder die zurückgegebenen Daten auf unterschiedliche Weise anzeigen. Beispielsweise können Sie die zurückgegebenen Daten im Bericht über häufigste Fehler nach Kriterien wie dem Aktivitätstyp (Peer-to-Peer-Sitzung oder Konferenzsitzung) oder dem SIP-Antwortcode für die fehlgeschlagene Sitzung filtern. Sie können außerdem festlegen, wie Daten gruppiert werden sollen. In diesem Fall werden die Ereignisse nach Stunde, Tag, Woche oder Monat zusammengefasst</span><span class="sxs-lookup"><span data-stu-id="e8695-p107">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Top Failures Report enables you to filter the returned data based on such things as the activity type (peer-to-peer session or conferencing session) or by the SIP response code that accompanied the failed session. You can also choose how data should be grouped. In this case, usages are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="e8695-134">In der folgenden Tabelle werden die Filter aufgelistet, die Sie im Bericht über häufigste Fehler verwenden können.</span><span class="sxs-lookup"><span data-stu-id="e8695-134">The following table lists the filters that you can use with the Top Failures Report.</span></span>

### <a name="top-failures-report-filters"></a><span data-ttu-id="e8695-135">Filter im Bericht über häufigste Fehler</span><span class="sxs-lookup"><span data-stu-id="e8695-135">Top Failures Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8695-136">Name</span><span class="sxs-lookup"><span data-stu-id="e8695-136">Name</span></span></th>
<th><span data-ttu-id="e8695-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8695-137">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8695-138"><strong>Von</strong></span><span class="sxs-lookup"><span data-stu-id="e8695-138"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="e8695-p108">Anfangsdatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Anfangsdatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="e8695-p108">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="e8695-141">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="e8695-141">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="e8695-p109">Wenn Sie keinen Anfangszeitpunkt eingeben, beginnt der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="e8695-p109">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="e8695-144">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="e8695-144">7/7/2012</span></span></p>
<p><span data-ttu-id="e8695-145">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="e8695-145">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="e8695-146">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="e8695-146">7/3/2012</span></span></p>
<p><span data-ttu-id="e8695-147">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="e8695-147">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8695-148"><strong>Bis</strong></span><span class="sxs-lookup"><span data-stu-id="e8695-148"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="e8695-p110">Enddatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Enddatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="e8695-p110">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="e8695-151">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="e8695-151">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="e8695-p111">Wenn Sie keinen Endzeitpunkt eingeben, endet der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="e8695-p111">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="e8695-154">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="e8695-154">7/7/2012</span></span></p>
<p><span data-ttu-id="e8695-155">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="e8695-155">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="e8695-156">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="e8695-156">7/3/2012</span></span></p>
<p><span data-ttu-id="e8695-157">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="e8695-157">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8695-158"><strong>Aktivitätstyp</strong></span><span class="sxs-lookup"><span data-stu-id="e8695-158"><strong>Activity type</strong></span></span></p></td>
<td><p><span data-ttu-id="e8695-p112">Aktivitätstyp. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="e8695-p112">Type of activity. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="e8695-161">[Alle]</span><span class="sxs-lookup"><span data-stu-id="e8695-161">[All]</span></span></p></li>
<li><p><span data-ttu-id="e8695-162">Peer-to-Peer</span><span class="sxs-lookup"><span data-stu-id="e8695-162">Peer-to-peer</span></span></p></li>
<li><p><span data-ttu-id="e8695-163">Konferenz</span><span class="sxs-lookup"><span data-stu-id="e8695-163">Conference</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8695-164"><strong>Modalität</strong></span><span class="sxs-lookup"><span data-stu-id="e8695-164"><strong>Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="e8695-165">Derzeit ist nur die Option <strong>[Alle]</strong> verfügbar.</span><span class="sxs-lookup"><span data-stu-id="e8695-165">At this time the only option available is <strong>[All]</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8695-166"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="e8695-166"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="e8695-p113">Vollqualifizierter Domänenname (FQDN) des Registrierungspools oder Edgeservers. Sie können einen einzelnen Pool auswählen oder auf <strong>[Alle]</strong> klicken, um die Daten für alle Pools anzuzeigen. Diese Dropdownliste wird basierend auf den Datensätzen in der Datenbank automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="e8695-p113">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8695-170"><strong>Kategorie</strong></span><span class="sxs-lookup"><span data-stu-id="e8695-170"><strong>Category</strong></span></span></p></td>
<td><p><span data-ttu-id="e8695-p114">Der Typ des aufgetretenen Fehlers. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="e8695-p114">Type of failure experienced. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="e8695-173">Erwartete und unerwartete Fehler</span><span class="sxs-lookup"><span data-stu-id="e8695-173">Both expected and unexpected failure</span></span></p></li>
<li><p><span data-ttu-id="e8695-174">Unerwarteter Fehler</span><span class="sxs-lookup"><span data-stu-id="e8695-174">Unexpected failure</span></span></p></li>
</ul>
<p><span data-ttu-id="e8695-175">&quot;Bei einem erwarteten Fehler handelt es sich &quot; um einen Fehler, der erwartet wird.</span><span class="sxs-lookup"><span data-stu-id="e8695-175">An &quot;expected failure&quot; is a failure that is expected to happen.</span></span> <span data-ttu-id="e8695-176">Hat beispielsweise ein Benutzer seinen Status auf „Nicht stören“ gesetzt, ist zu erwarten, dass alle Anrufe an diesen Benutzer fehlschlagen.</span><span class="sxs-lookup"><span data-stu-id="e8695-176">For example, if a user has set his or her status to Do Not Disturb you would expect any call to that user to fail.</span></span> <span data-ttu-id="e8695-177">&quot;Bei einem unerwarteten Fehler &quot; handelt es sich um einen Fehler, der in einem ansonsten fehlerhaften System auftreten kann.</span><span class="sxs-lookup"><span data-stu-id="e8695-177">An &quot;unexpected failure&quot; is a failure that occurs in what would appear to be an otherwise healthy system.</span></span> <span data-ttu-id="e8695-178">Beispielsweise sollte ein Anruf nicht abgebrochen werden, während der Anrufer sich in der Warteschleife befindet.</span><span class="sxs-lookup"><span data-stu-id="e8695-178">For example, a call should not be terminated if the caller is placed on hold.</span></span> <span data-ttu-id="e8695-179">In diesem Fall würde der Fehler als „unerwartet“ gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="e8695-179">If that occurs, that would be flagged as an unexpected failure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8695-180"><strong>Antwortcode</strong></span><span class="sxs-lookup"><span data-stu-id="e8695-180"><strong>Response code</strong></span></span></p></td>
<td><p><span data-ttu-id="e8695-p116">Der SIP-Antwortcode, der gesendet wird, wenn die Konferenz fehlschlägt. Geben Sie den vollständigen Antwortcode ein. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="e8695-p116">SIP response code sent when the conference failed. Enter the entire response code For example:</span></span></p>
<p><span data-ttu-id="e8695-183">400</span><span class="sxs-lookup"><span data-stu-id="e8695-183">400</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8695-184"><strong>Diagnose-ID</strong></span><span class="sxs-lookup"><span data-stu-id="e8695-184"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="e8695-p117">Eindeutige ID (in der Form eines Headers vom Typ „ms-diagnostics“), die an eine SIP-Nachricht angehängt wird und oft nützliche Informationen für die Fehlerbehebung bereitstellt. Diagnostics-Header sind optional (SIP-Sitzungen ohne diese Header sind möglich) und Diagnose-IDs werden nur für Sitzungen berichtet, bei denen Probleme aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="e8695-p117">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors. Diagnostics headers are optional (it is possible to have SIP sessions that do not include these headers), and diagnostic IDs are reported only for sessions that experienced problems of some kind.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="e8695-187">Metriken</span><span class="sxs-lookup"><span data-stu-id="e8695-187">Metrics</span></span>

<span data-ttu-id="e8695-188">In der folgenden Tabelle werden die Metriken aufgelistet, die im Bericht über häufigste Fehler angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e8695-188">The following table lists the information provided in the Top Failures Report.</span></span>

### <a name="top-failures-report-metrics"></a><span data-ttu-id="e8695-189">Metriken im Bericht über häufigste Fehler</span><span class="sxs-lookup"><span data-stu-id="e8695-189">Top Failures Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e8695-190">Name</span><span class="sxs-lookup"><span data-stu-id="e8695-190">Name</span></span></th>
<th><span data-ttu-id="e8695-191">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="e8695-191">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="e8695-192">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e8695-192">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e8695-193"><strong>Rang</strong></span><span class="sxs-lookup"><span data-stu-id="e8695-193"><strong>Rank</strong></span></span></p></td>
<td><p><span data-ttu-id="e8695-194">Ja</span><span class="sxs-lookup"><span data-stu-id="e8695-194">Yes</span></span></p></td>
<td><p><span data-ttu-id="e8695-195">Der relative Rang basierend auf der Anzahl der gemeldeten Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="e8695-195">Relative rank based on the number of reported sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8695-196"><strong>Gemeldete Sitzungen</strong></span><span class="sxs-lookup"><span data-stu-id="e8695-196"><strong>Reported sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="e8695-197">Ja</span><span class="sxs-lookup"><span data-stu-id="e8695-197">Yes</span></span></p></td>
<td><p><span data-ttu-id="e8695-198">Die Gesamtzahl der fehlerhaften Sitzungen basierend auf der Diagnose-ID und dem SIP-Antwortcode.</span><span class="sxs-lookup"><span data-stu-id="e8695-198">Total number of failed sessions based on diagnostic ID and SIP response code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8695-199"><strong>Betroffene Benutzer</strong></span><span class="sxs-lookup"><span data-stu-id="e8695-199"><strong>Users impacted</strong></span></span></p></td>
<td><p><span data-ttu-id="e8695-200">Ja</span><span class="sxs-lookup"><span data-stu-id="e8695-200">Yes</span></span></p></td>
<td><p><span data-ttu-id="e8695-201">Die Gesamtzahl der Benutzer, die von der fehlerhaften Sitzung betroffen waren.</span><span class="sxs-lookup"><span data-stu-id="e8695-201">Total number of users affected by the failed session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e8695-202"><strong>Fehlerinformationen</strong></span><span class="sxs-lookup"><span data-stu-id="e8695-202"><strong>Failure information</strong></span></span></p></td>
<td><p><span data-ttu-id="e8695-203">Nein</span><span class="sxs-lookup"><span data-stu-id="e8695-203">No</span></span></p></td>
<td><p><span data-ttu-id="e8695-204">Genaue Angaben zu dem Fehler, u. a. die Diagnose-ID, der SIP-Antwortcode und eine Beschreibung der Ursache des Sitzungsfehlers.</span><span class="sxs-lookup"><span data-stu-id="e8695-204">Detailed information about the failure, including diagnostic ID, SIP response code, and description of why the session failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e8695-205"><strong>Trend in der Vergangenheit</strong></span><span class="sxs-lookup"><span data-stu-id="e8695-205"><strong>Trend in the past</strong></span></span></p></td>
<td><p><span data-ttu-id="e8695-206">Nein</span><span class="sxs-lookup"><span data-stu-id="e8695-206">No</span></span></p></td>
<td><p><span data-ttu-id="e8695-207">Eine grafische Darstellung der fehlerhaften Sitzungen über einen bestimmten Zeitraum.</span><span class="sxs-lookup"><span data-stu-id="e8695-207">Graphs failed sessions over time.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e8695-208">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e8695-208">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

