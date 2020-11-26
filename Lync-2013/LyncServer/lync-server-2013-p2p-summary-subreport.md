---
title: 'Lync Server 2013: P2P-Zusammenfassungs Unterbericht'
description: 'Lync Server 2013: P2P-Zusammenfassungs Unterbericht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: P2P Summary Subreport
ms:assetid: fc36185a-3cc5-4167-8c93-8a755fa75ac7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205416(v=OCS.15)
ms:contentKeyID: 48185950
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eda51e76c4ed7b62535a2a2e4ab52982aa6381f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424702"
---
# <a name="p2p-summary-subreport-in-lync-server-2013"></a><span data-ttu-id="39e6c-103">P2P-Zusammenfassungs Unterbericht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39e6c-103">P2P Summary Subreport in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39e6c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39e6c-104">

<span> </span></span></span>

<span data-ttu-id="39e6c-105">_**Letztes Änderungsdatum des Themas:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="39e6c-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="39e6c-106">Der Zusammenfassende Unterbericht über Peer-to-Peer-Sitzungen bietet eine allgemeine Übersicht über fehlerhafte Peer-to-Peer-Kommunikationssitzungen.</span><span class="sxs-lookup"><span data-stu-id="39e6c-106">The P2P Summary Subreport provides an overall view of your failed peer-to-peer communication sessions.</span></span>

<div>

## <a name="filters"></a><span data-ttu-id="39e6c-107">Filter</span><span class="sxs-lookup"><span data-stu-id="39e6c-107">Filters</span></span>

<span data-ttu-id="39e6c-p101">Mithilfe von Filtern können Sie eine gezieltere Datenauswahl erreichen oder die zurückgegebenen Daten auf unterschiedliche Weise anzeigen. In der folgenden Tabelle werden die Filter aufgelistet, die Sie im Zusammenfassenden Unterbericht über Peer-to-Peer-Sitzungen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="39e6c-p101">Filters provide a way for you to return a more finely targeted set of data or to view the returned data in different ways. The following table lists the filters that you can use with the P2P Summary Subreport.</span></span>

### <a name="p2p-summary-subreport-filters"></a><span data-ttu-id="39e6c-110">Filter im Zusammenfassenden Unterbericht über Peer-to-Peer-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="39e6c-110">P2P Summary Subreport Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39e6c-111">Name</span><span class="sxs-lookup"><span data-stu-id="39e6c-111">Name</span></span></th>
<th><span data-ttu-id="39e6c-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39e6c-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39e6c-113"><strong>Von</strong></span><span class="sxs-lookup"><span data-stu-id="39e6c-113"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="39e6c-p102">Anfangsdatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Anfangsdatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="39e6c-p102">Start date and time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="39e6c-116">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="39e6c-116">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="39e6c-p103">Wenn Sie keinen Anfangszeitpunkt eingeben, beginnt der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="39e6c-p103">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="39e6c-119">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="39e6c-119">7/7/2012</span></span></p>
<p><span data-ttu-id="39e6c-120">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="39e6c-120">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="39e6c-121">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="39e6c-121">7/3/2012</span></span></p>
<p><span data-ttu-id="39e6c-122">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="39e6c-122">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39e6c-123"><strong>Bis</strong></span><span class="sxs-lookup"><span data-stu-id="39e6c-123"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="39e6c-p104">Enddatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Enddatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="39e6c-p104">End date and time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="39e6c-126">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="39e6c-126">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="39e6c-p105">Wenn Sie keinen Endzeitpunkt eingeben, endet der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="39e6c-p105">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="39e6c-129">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="39e6c-129">7/7/2012</span></span></p>
<p><span data-ttu-id="39e6c-130">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="39e6c-130">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="39e6c-131">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="39e6c-131">7/3/2012</span></span></p>
<p><span data-ttu-id="39e6c-132">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="39e6c-132">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39e6c-133"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="39e6c-133"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="39e6c-p106">Vollqualifizierter Domänenname (FQDN) des Registrierungspools oder Edgeservers. Sie können einen einzelnen Pool auswählen oder auf <strong>[Alle]</strong> klicken, um die Daten für alle Pools anzuzeigen. Diese Dropdownliste wird basierend auf den Datensätzen in der Datenbank automatisch ausgefüllt.</span><span class="sxs-lookup"><span data-stu-id="39e6c-p106">Fully qualified domain name (FQDN) of the Registrar pool or Edge Server. You can either select an individual pool or click <strong>[All]</strong> to view data for all the pools. This drop-down list is automatically populated for you based on the records in the database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="39e6c-137">Metriken</span><span class="sxs-lookup"><span data-stu-id="39e6c-137">Metrics</span></span>

<span data-ttu-id="39e6c-138">In der folgenden Tabelle werden die Metriken aufgelistet, die im Zusammenfassenden Unterbericht über Peer-to-Peer-Sitzungen angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="39e6c-138">The following table lists the information provided in the P2P Summary Subreport.</span></span>

### <a name="p2p-summary-subreport-metrics"></a><span data-ttu-id="39e6c-139">Metriken im Zusammenfassenden Unterbericht über Peer-to-Peer-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="39e6c-139">P2P Summary Subreport Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="39e6c-140">Name</span><span class="sxs-lookup"><span data-stu-id="39e6c-140">Name</span></span></th>
<th><span data-ttu-id="39e6c-141">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="39e6c-141">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="39e6c-142">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="39e6c-142">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="39e6c-143"><strong>Sitzungen insgesamt</strong></span><span class="sxs-lookup"><span data-stu-id="39e6c-143"><strong>Total sessions</strong></span></span></p></td>
<td><p><span data-ttu-id="39e6c-144">Nein</span><span class="sxs-lookup"><span data-stu-id="39e6c-144">No</span></span></p></td>
<td><p><span data-ttu-id="39e6c-145">Die Gesamtzahl der Sitzungen, einschließlich Sitzungen ohne Fehler, Sitzungen mit Fehlern (sowohl erwarteten als auch unerwarteten) und nicht kategorisierten Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="39e6c-145">Total number of sessions, including successful sessions, failed sessions (both expected failures and unexpected failures), and uncategorized sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39e6c-146"><strong>Fehlerrate</strong></span><span class="sxs-lookup"><span data-stu-id="39e6c-146"><strong>Failure rate</strong></span></span></p></td>
<td><p><span data-ttu-id="39e6c-147">Nein</span><span class="sxs-lookup"><span data-stu-id="39e6c-147">No</span></span></p></td>
<td><p><span data-ttu-id="39e6c-148">Der Prozentsatz der Peer-to-Peer-Sitzungen, bei denen ein Fehler aufgetreten ist.</span><span class="sxs-lookup"><span data-stu-id="39e6c-148">Percentage of peer-to-peer sessions that failed.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="39e6c-149"><strong>Sitzungen nach Modalität</strong></span><span class="sxs-lookup"><span data-stu-id="39e6c-149"><strong>Sessions by Modality</strong></span></span></p></td>
<td><p><span data-ttu-id="39e6c-150">Nein</span><span class="sxs-lookup"><span data-stu-id="39e6c-150">No</span></span></p></td>
<td><p><span data-ttu-id="39e6c-151">Gesamtzahl der Sitzungen, gruppiert nach Modalität (z. B. Instant Messaging).</span><span class="sxs-lookup"><span data-stu-id="39e6c-151">Total number of sessions grouped by modality (for example, instant messaging).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="39e6c-152"><strong>Fehlerrate nach Modalität</strong></span><span class="sxs-lookup"><span data-stu-id="39e6c-152"><strong>Failure rate by modality</strong></span></span></p></td>
<td><p><span data-ttu-id="39e6c-153">Nein</span><span class="sxs-lookup"><span data-stu-id="39e6c-153">No</span></span></p></td>
<td><p><span data-ttu-id="39e6c-154">Gesamtzahl der fehlerhaften Sitzungen, gruppiert nach Modalität (z. B. Instant Messaging).</span><span class="sxs-lookup"><span data-stu-id="39e6c-154">Total number of failed sessions grouped by modality (for example, instant messaging).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="39e6c-155">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39e6c-155">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

