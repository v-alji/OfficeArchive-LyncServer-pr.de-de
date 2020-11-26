---
title: 'Lync Server 2013: Konferenz Zusammenfassungs Unterbericht'
description: 'Lync Server 2013: Konferenz Zusammenfassung Unterbericht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conference Summary Subreport
ms:assetid: 2fc1d2bf-34f5-4093-a6e2-250ec1f1b004
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204779(v=OCS.15)
ms:contentKeyID: 48183742
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0612ce1adb8a6b0fdea5e3bf70b88346f7c08044
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434487"
---
# <a name="conference-summary-subreport-in-lync-server-2013"></a><span data-ttu-id="2182b-103">Konferenz Zusammenfassung Unterbericht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2182b-103">Conference Summary Subreport in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2182b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2182b-104">

<span> </span></span></span>

<span data-ttu-id="2182b-105">_**Letztes Änderungsdatum des Themas:** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="2182b-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="2182b-p101">Der zusammenfassende Konferenzunterbericht stellt eine Gesamtübersicht zu gescheiterten Konferenzsitzungen bereit, bei denen Fehler aufgetreten sind. Diese gescheiterten Sitzungen sind weiter nach Sitzungstyp unterteilt: Konferenzzustandsobjekt-Sitzungen und MCU-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="2182b-p101">The Conference Summary Subreport provides an overall view of failed conference sessions. These failed sessions are further broken down by session type: Focus sessions and MCU sessions.</span></span>

<div>

## <a name="filters"></a><span data-ttu-id="2182b-108">Filter</span><span class="sxs-lookup"><span data-stu-id="2182b-108">Filters</span></span>

<span data-ttu-id="2182b-p102">Mithilfe von Filtern können Sie eine gezieltere Datenauswahl erreichen oder die zurückgegebenen Daten auf unterschiedliche Weise anzeigen. In der folgenden Tabelle werden die Filter aufgelistet, die Sie im zusammenfassenden Konferenzunterbericht verwenden können.</span><span class="sxs-lookup"><span data-stu-id="2182b-p102">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the Conference Summary Subreport.</span></span>

### <a name="conference-summary-subreport-filters"></a><span data-ttu-id="2182b-111">Filter im zusammenfassenden Konferenzunterbericht</span><span class="sxs-lookup"><span data-stu-id="2182b-111">Conference Summary Subreport Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2182b-112">Name</span><span class="sxs-lookup"><span data-stu-id="2182b-112">Name</span></span></th>
<th><span data-ttu-id="2182b-113">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2182b-113">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2182b-114"><strong>Von</strong></span><span class="sxs-lookup"><span data-stu-id="2182b-114"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="2182b-p103">Anfangsdatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Anfangsdatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="2182b-p103">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="2182b-117">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="2182b-117">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="2182b-p104">Wenn Sie keinen Anfangszeitpunkt eingeben, beginnt der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="2182b-p104">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="2182b-120">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="2182b-120">7/7/2012</span></span></p>
<p><span data-ttu-id="2182b-121">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="2182b-121">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="2182b-122">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="2182b-122">7/3/2012</span></span></p>
<p><span data-ttu-id="2182b-123">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="2182b-123">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2182b-124"><strong>Bis</strong></span><span class="sxs-lookup"><span data-stu-id="2182b-124"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="2182b-p105">Enddatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Enddatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="2182b-p105">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="2182b-127">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="2182b-127">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="2182b-p106">Wenn Sie keinen Endzeitpunkt eingeben, endet der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="2182b-p106">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="2182b-130">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="2182b-130">7/7/2012</span></span></p>
<p><span data-ttu-id="2182b-131">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="2182b-131">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="2182b-132">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="2182b-132">7/3/2012</span></span></p>
<p><span data-ttu-id="2182b-133">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="2182b-133">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2182b-134"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="2182b-134"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="2182b-p107">Vollqualifizierter Domänenname (FQDN) des Registrierungspools oder Edgeservers. Sie können einen einzelnen Pool auswählen oder auf <strong>[Alle]</strong> klicken, um die Daten für alle Pools anzuzeigen. Diese Dropdownliste wird basierend auf den Datensätzen in der Datenbank automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="2182b-p107">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="2182b-138">Metriken</span><span class="sxs-lookup"><span data-stu-id="2182b-138">Metrics</span></span>

<span data-ttu-id="2182b-139">In der folgenden Tabelle sind die Metriken aufgelistet, die im zusammenfassenden Konferenzunterbericht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2182b-139">The following table lists the information provided in the Conference Summary Subreport.</span></span>

### <a name="conference-summary-subreport-metrics"></a><span data-ttu-id="2182b-140">Metriken im zusammenfassenden Konferenzunterbericht</span><span class="sxs-lookup"><span data-stu-id="2182b-140">Conference Summary Subreport Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2182b-141">Name</span><span class="sxs-lookup"><span data-stu-id="2182b-141">Name</span></span></th>
<th><span data-ttu-id="2182b-142">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="2182b-142">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="2182b-143">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2182b-143">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2182b-144"><strong>Konferenzen insgesamt</strong></span><span class="sxs-lookup"><span data-stu-id="2182b-144"><strong>Total conferences</strong></span></span></p></td>
<td><p><span data-ttu-id="2182b-145">Nein</span><span class="sxs-lookup"><span data-stu-id="2182b-145">No</span></span></p></td>
<td><p><span data-ttu-id="2182b-146">Gesamtzahl der Konferenzen, die durchgeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="2182b-146">Total number of conferences held.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2182b-147"><strong>Konferenzsitzungen insgesamt</strong></span><span class="sxs-lookup"><span data-stu-id="2182b-147"><strong>Total conference sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="2182b-148">Nein</span><span class="sxs-lookup"><span data-stu-id="2182b-148">No</span></span></p></td>
<td><p><span data-ttu-id="2182b-p108">Gesamtzahl der Konferenzsitzungen. Eine einzelne Konferenz kann mehrere Sitzungen haben. Beispielsweise kann eine Konferenz sowohl eine Konferenzzustandsobjekt-Sitzung als auch eine MCU-Sitzung umfassen.</span><span class="sxs-lookup"><span data-stu-id="2182b-p108">Total number of conference sessions. A single conference can have multiple sessions; for example, a conference might include both a Focus session and an MCU session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2182b-151"><strong>Sitzungsfehlerrate insgesamt</strong></span><span class="sxs-lookup"><span data-stu-id="2182b-151"><strong>Overall session failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="2182b-152">Nein</span><span class="sxs-lookup"><span data-stu-id="2182b-152">No</span></span></p></td>
<td><p><span data-ttu-id="2182b-153">Prozentsatz aller gescheiterten Konferenzen.</span><span class="sxs-lookup"><span data-stu-id="2182b-153">Percentage of all conferences that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2182b-154"><strong>Konferenzzustandsobjekt-Sitzungen</strong></span><span class="sxs-lookup"><span data-stu-id="2182b-154"><strong>Focus sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="2182b-155">Nein</span><span class="sxs-lookup"><span data-stu-id="2182b-155">No</span></span></p></td>
<td><p><span data-ttu-id="2182b-156">Gesamtanzahl der Konferenzzustandsobjekt-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="2182b-156">Total number of Focus sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2182b-157"><strong>Fehlerrate für Konferenzzustandsobjekt</strong></span><span class="sxs-lookup"><span data-stu-id="2182b-157"><strong>Focus failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="2182b-158">Nein</span><span class="sxs-lookup"><span data-stu-id="2182b-158">No</span></span></p></td>
<td><p><span data-ttu-id="2182b-159">Prozentsatz der gescheiterten Konferenzzustandsobjekt-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="2182b-159">Percentage of Focus sessions that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2182b-160">MCU-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="2182b-160">MCU sessions</span></span></p></td>
<td><p><span data-ttu-id="2182b-161">Nein</span><span class="sxs-lookup"><span data-stu-id="2182b-161">No</span></span></p></td>
<td><p><span data-ttu-id="2182b-162">Gesamtanzahl der MCU-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="2182b-162">Total number of MCU sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2182b-163"><strong>MCU-Fehlerrate</strong></span><span class="sxs-lookup"><span data-stu-id="2182b-163"><strong>MCU failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="2182b-164">Nein</span><span class="sxs-lookup"><span data-stu-id="2182b-164">No</span></span></p></td>
<td><p><span data-ttu-id="2182b-165">Prozentsatz der gescheiterten MCU-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="2182b-165">Percentage of MCU sessions that failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2182b-166"><strong>MCU-Sitzungen nach Modalität</strong></span><span class="sxs-lookup"><span data-stu-id="2182b-166"><strong>MCU sessions by modality</strong></span></span></p></td>
<td><p><span data-ttu-id="2182b-167">Nein</span><span class="sxs-lookup"><span data-stu-id="2182b-167">No</span></span></p></td>
<td><p><span data-ttu-id="2182b-168">Gesamtanzahl der MCU-Sitzungen, gruppiert nach Modalität (z. B. Chatkonferenz).</span><span class="sxs-lookup"><span data-stu-id="2182b-168">Total number of MCU sessions, grouped by modality (for example, IM conferencing).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2182b-169"><strong>Fehlerrate nach Modalität</strong></span><span class="sxs-lookup"><span data-stu-id="2182b-169"><strong>Failure rate by modality</strong></span></span></p></td>
<td><p><span data-ttu-id="2182b-170">Nein</span><span class="sxs-lookup"><span data-stu-id="2182b-170">No</span></span></p></td>
<td><p><span data-ttu-id="2182b-171">Prozentsatz der gescheiterten MCU-Sitzungen, gruppiert nach Modalität (z. B. Chatkonferenz).</span><span class="sxs-lookup"><span data-stu-id="2182b-171">Percentage of MCU sessions that failed, grouped by modality (for example, IM conferencing).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="2182b-172">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2182b-172">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

