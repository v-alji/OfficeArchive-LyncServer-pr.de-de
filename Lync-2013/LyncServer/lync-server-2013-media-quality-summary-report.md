---
title: 'Lync Server 2013: Zusammenfassungsbericht für Medienqualität'
description: 'Lync Server 2013: Zusammenfassungsbericht für Medienqualität.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media Quality Summary Report
ms:assetid: 8bd59ad6-3087-49c8-b692-5573fe2ffcd8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615012(v=OCS.15)
ms:contentKeyID: 48184776
ms.date: 06/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2616b7e3cdea9df7b004745a5c407188870903c7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446045"
---
# <a name="media-quality-summary-report-in-lync-server-2013"></a><span data-ttu-id="80be2-103">Zusammenfassungsbericht für Medienqualität in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="80be2-103">Media Quality Summary Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="80be2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="80be2-104">

<span> </span></span></span>

<span data-ttu-id="80be2-105">_**Letztes Änderungsdatum des Themas:** 2016-06-29_</span><span class="sxs-lookup"><span data-stu-id="80be2-105">_**Topic Last Modified:** 2016-06-29_</span></span>

<span data-ttu-id="80be2-106">Der „Zusammenfassende Bericht über Medienqualität“ ist möglicherweise die beste Option zum Analysieren der Anrufqualität in Ihrer Organisation: In diesem Bericht werden detailliert die QoE-Anrufmetriken (Quality of Experience, QoE) in den folgenden Kategorien aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="80be2-106">The Media Quality Summary Report is perhaps your best bet for analyzing call quality in your organization: this report provides detailed Quality of Experience (QoE) call metrics broken down into the following categories:</span></span>

  - <span data-ttu-id="80be2-107">UC-Peer-to-Peer-Anrufe (beispielsweise ein Microsoft lync 2013 zu Microsoft lync 2013-Anruf)</span><span class="sxs-lookup"><span data-stu-id="80be2-107">UC Peer to Peer Calls (such as a Microsoft Lync 2013 to Microsoft Lync 2013 call)</span></span>

  - <span data-ttu-id="80be2-108">UC-Konferenzsitzungen</span><span class="sxs-lookup"><span data-stu-id="80be2-108">UC Conference Sessions</span></span>

  - <span data-ttu-id="80be2-109">PSTN-Konferenzsitzungen</span><span class="sxs-lookup"><span data-stu-id="80be2-109">PSTN Conference Sessions</span></span>

  - <span data-ttu-id="80be2-110">PSTN-Anrufe: Medienumgehung</span><span class="sxs-lookup"><span data-stu-id="80be2-110">PSTN Calls: Media Bypass</span></span>

  - <span data-ttu-id="80be2-111">PSTN-Anrufe (keine Umgehung): UC-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="80be2-111">PSTN Calls (Non-Bypass): UC Leg</span></span>

  - <span data-ttu-id="80be2-112">PSTN-Anrufe (keine Umgehung): Gateway-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="80be2-112">PSTN Calls (Non-Bypass): Gateway Leg</span></span>

  - <span data-ttu-id="80be2-113">Andere Anruftypen</span><span class="sxs-lookup"><span data-stu-id="80be2-113">Other Call Types</span></span>

<span data-ttu-id="80be2-114">Beim ersten Öffnen des Berichts wird eine Zusammenfassung zu den einzelnen Kategorien angezeigt.</span><span class="sxs-lookup"><span data-stu-id="80be2-114">When you first open the report, you see summary information for each of these categories.</span></span> <span data-ttu-id="80be2-115">Ohne den Bericht zu verlassen, können Sie jede Kategorie erweitern, um Unterkategorien wie Anrufe von Office Communicator 2007 R2 zu lync 2013 zu sehen.</span><span class="sxs-lookup"><span data-stu-id="80be2-115">Without leaving the report, you can expand each category to look at subcategories such as calls made from Office Communicator 2007 R2 to Lync 2013.</span></span> <span data-ttu-id="80be2-116">Diese Unterkategorien können Sie anschließend erweitern, um Details zu jedem in diesen Unterkategorien getätigten Anruf anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="80be2-116">In turn, you can then drill down into these subcategories to see details about each call made within that subcategory.</span></span>

<span data-ttu-id="80be2-117">In Microsoft lync Server 2013 werden die Daten im Zusammenfassungsbericht für Medienqualität weiter in drei Anruftypen unterteilt: Audioanrufe, Videoanrufe und Anwendungsfreigabe Anrufe.</span><span class="sxs-lookup"><span data-stu-id="80be2-117">In Microsoft Lync Server 2013 the Media Quality Summary Report further breaks the data down into three call types: audio calls, video calls, and application sharing calls.</span></span> <span data-ttu-id="80be2-118">Für jeden Anruftyp gibt es im Bericht einen eigenen Bereich und eigenen benutzerdefinierten Satz von Anrufmetriken.</span><span class="sxs-lookup"><span data-stu-id="80be2-118">Each call type has its own section in the report, and its own custom set of call metrics.</span></span>

<span data-ttu-id="80be2-119">Im „Zusammenfassenden Bericht über Medienqualität“ können Sie Filter anwenden, mit denen Sie die Anrufqualität zwischen verkabelten und drahtlosen Anrufen, internen und externen Anrufen sowie VPN- und Nicht-VPN-Anrufen vergleichen können.</span><span class="sxs-lookup"><span data-stu-id="80be2-119">The Media Quality Summary Report also allows you to apply filters that enable you to compare the call quality of wired calls vs. wireless calls, internal calls vs. external calls, and VPN calls vs. non-VPN calls.</span></span>

<div>

## <a name="accessing-the-media-quality-summary-report"></a><span data-ttu-id="80be2-120">Zugreifen auf den „Zusammenfassenden Bericht über Medienqualität“</span><span class="sxs-lookup"><span data-stu-id="80be2-120">Accessing the Media Quality Summary Report</span></span>

<span data-ttu-id="80be2-121">Auf den „Zusammenfassenden Bericht über Medienqualität“ kann auf der Startseite „Überwachungsberichte“ zugegriffen werden.</span><span class="sxs-lookup"><span data-stu-id="80be2-121">The Media Quality Summary Report is accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="80be2-122">Sie können einen Drilldown zum [Bericht Anrufliste in lync Server 2013](lync-server-2013-call-list-report.md) durchführen, indem Sie auf eine der folgenden Metriken klicken:</span><span class="sxs-lookup"><span data-stu-id="80be2-122">You can drill down to the [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="80be2-123">Anruflautstärke</span><span class="sxs-lookup"><span data-stu-id="80be2-123">Call volume</span></span>

  - <span data-ttu-id="80be2-124">Prozentsatz der Anrufe schlechter Qualität</span><span class="sxs-lookup"><span data-stu-id="80be2-124">Poor call percentage</span></span>

<span data-ttu-id="80be2-125">Auf den „Zusammenfassenden Bericht über Medienqualität“ können Sie auch zugreifen, indem Sie auf eine beliebige der folgenden Audioanrufmetriken klicken:</span><span class="sxs-lookup"><span data-stu-id="80be2-125">In addition, you can access the Media Quality Metrics Distribution Report by clicking any of the following audio call metrics:</span></span>

  - <span data-ttu-id="80be2-126">Roundtrip (ms)</span><span class="sxs-lookup"><span data-stu-id="80be2-126">Round trip (ms)</span></span>

  - <span data-ttu-id="80be2-127">Beeinträchtigung (MOS)</span><span class="sxs-lookup"><span data-stu-id="80be2-127">Degradation (MOS)</span></span>

  - <span data-ttu-id="80be2-128">Paketverlust</span><span class="sxs-lookup"><span data-stu-id="80be2-128">Packet loss</span></span>

  - <span data-ttu-id="80be2-129">Jitter (ms)</span><span class="sxs-lookup"><span data-stu-id="80be2-129">Jitter (ms)</span></span>

  - <span data-ttu-id="80be2-130">Ausblendungsverhältnis der Reparatur</span><span class="sxs-lookup"><span data-stu-id="80be2-130">Healer concealed ratio</span></span>

  - <span data-ttu-id="80be2-131">Streckungsverhältnis der Reparatur</span><span class="sxs-lookup"><span data-stu-id="80be2-131">Healer stretched ratio</span></span>

  - <span data-ttu-id="80be2-132">Komprimierungsverhältnis der Reparatur</span><span class="sxs-lookup"><span data-stu-id="80be2-132">Healer compressed ratio</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="80be2-133">Filter</span><span class="sxs-lookup"><span data-stu-id="80be2-133">Filters</span></span>

<span data-ttu-id="80be2-p104">Mithilfe von Filtern können Sie eine gezieltere Datenauswahl zurückgeben oder die zurückgegebenen Daten auf unterschiedliche Weise anzeigen. Beispielsweise können Sie im zusammenfassenden Bericht über Medienqualität die zurückgegebenen Daten nach Zugriffstyp (d. h. interner oder externer Zugriff) oder nach Netzwerkverbindung (Kabel- oder Funkverbindung) filtern. Sie können außerdem festlegen, wie Daten gruppiert werden sollen. In diesem Fall werden die Anrufe nach Stunde, Tag, Woche oder Monat zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="80be2-p104">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Media Quality Summary Report enables you to filter the returned data by such things as access type (that is, interval access vs. external access) or by wired/wireless network connection. You can also choose how data should be grouped. In this case, calls are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="80be2-138">In der folgenden Tabelle werden die Filter aufgelistet, die Sie im „Zusammenfassenden Bericht über Medienqualität“ verwenden können.</span><span class="sxs-lookup"><span data-stu-id="80be2-138">The following table lists the filters that you can use with the Media Quality Summary Report.</span></span>

### <a name="media-quality-summary-report-filters"></a><span data-ttu-id="80be2-139">Filter im „Zusammenfassenden Bericht über Medienqualität“</span><span class="sxs-lookup"><span data-stu-id="80be2-139">Media Quality Summary Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80be2-140">Name</span><span class="sxs-lookup"><span data-stu-id="80be2-140">Name</span></span></th>
<th><span data-ttu-id="80be2-141">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80be2-141">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80be2-142"><strong>Von</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-142"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-p105">Anfangsdatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Anfangsdatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="80be2-p105">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="80be2-145">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="80be2-145">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="80be2-p106">Wenn Sie keinen Anfangszeitpunkt eingeben, beginnt der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="80be2-p106">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="80be2-148">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="80be2-148">7/7/2012</span></span></p>
<p><span data-ttu-id="80be2-149">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="80be2-149">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="80be2-150">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="80be2-150">7/3/2012</span></span></p>
<p><span data-ttu-id="80be2-151">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="80be2-151">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-152"><strong>Bis</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-152"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-p107">Enddatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Enddatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="80be2-p107">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="80be2-155">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="80be2-155">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="80be2-p108">Wenn Sie keinen Endzeitpunkt eingeben, endet der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="80be2-p108">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="80be2-158">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="80be2-158">7/7/2012</span></span></p>
<p><span data-ttu-id="80be2-159">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="80be2-159">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="80be2-160">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="80be2-160">7/3/2012</span></span></p>
<p><span data-ttu-id="80be2-161">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="80be2-161">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80be2-162"><strong>Zugriffstyp</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-162"><strong>Access type</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-p109">Gibt an, ob der Client am internen oder am externen Netzwerk angemeldet wurde, als der Anruf getätigt wurde. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="80be2-p109">Indicates whether the client was logged on to the internal network or the external network when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="80be2-165">[Alle]</span><span class="sxs-lookup"><span data-stu-id="80be2-165">[All]</span></span></p></li>
<li><p><span data-ttu-id="80be2-166">Intern</span><span class="sxs-lookup"><span data-stu-id="80be2-166">Internal</span></span></p></li>
<li><p><span data-ttu-id="80be2-167">Extern</span><span class="sxs-lookup"><span data-stu-id="80be2-167">External</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-168"><strong>Netzwerktyp</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-168"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-p110">Gibt den Typ des Netzwerks an, mit dem der Client verbunden wurde, als der Anruf erfolgte. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="80be2-p110">Indicates the type of network the client was connected to when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="80be2-171">[Alle]</span><span class="sxs-lookup"><span data-stu-id="80be2-171">[All]</span></span></p></li>
<li><p><span data-ttu-id="80be2-172">Verkabelt</span><span class="sxs-lookup"><span data-stu-id="80be2-172">Wired</span></span></p></li>
<li><p><span data-ttu-id="80be2-173">Funk</span><span class="sxs-lookup"><span data-stu-id="80be2-173">Wireless</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80be2-174"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-174"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-p111">Gibt an, ob ein externer Client eine VPN-Verbindung (Virtual Private Network) verwendete, als der Anruf getätigt wurde. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="80be2-p111">Indicates whether an external client was using a virtual private network (VPN) connection when the call was placed. Select one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="80be2-177">[Alle]</span><span class="sxs-lookup"><span data-stu-id="80be2-177">[All]</span></span></p></li>
<li><p><span data-ttu-id="80be2-178">VPN</span><span class="sxs-lookup"><span data-stu-id="80be2-178">VPN</span></span></p></li>
<li><p><span data-ttu-id="80be2-179">Nicht-VPN</span><span class="sxs-lookup"><span data-stu-id="80be2-179">Non-VPN</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="80be2-180">Metriken</span><span class="sxs-lookup"><span data-stu-id="80be2-180">Metrics</span></span>

<span data-ttu-id="80be2-181">In der folgenden Tabelle werden Metriken aufgelistet, die im Zusammenfassenden Bericht über Medienqualität angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="80be2-181">The following table lists the information provided in the Media Quality Summary Report.</span></span>

### <a name="media-quality-summary-report-metrics-audio-call-summary"></a><span data-ttu-id="80be2-182">Metriken im „Zusammenfassenden Bericht über Medienqualität“: Zusammenfassung der Audioanrufe</span><span class="sxs-lookup"><span data-stu-id="80be2-182">Media Quality Summary Report Metrics: Audio Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80be2-183">Name</span><span class="sxs-lookup"><span data-stu-id="80be2-183">Name</span></span></th>
<th><span data-ttu-id="80be2-184">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="80be2-184">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="80be2-185">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80be2-185">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80be2-186"><strong>Anruftyp/Endpunkttyp</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-186"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-187">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-187">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-p112">Wenn Sie auf dieses Element klicken, zeigt der Bericht Details zu den auf diesem Typ basierenden Anrufen. Es gibt folgende Anruftypen:</span><span class="sxs-lookup"><span data-stu-id="80be2-p112">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="80be2-190">UC-Peer-to-Peer-Anrufe</span><span class="sxs-lookup"><span data-stu-id="80be2-190">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="80be2-191">UC-Konferenzsitzungen</span><span class="sxs-lookup"><span data-stu-id="80be2-191">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="80be2-192">PSTN-Konferenzsitzungen</span><span class="sxs-lookup"><span data-stu-id="80be2-192">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="80be2-193">PSTN-Anrufe: Medienumgehung</span><span class="sxs-lookup"><span data-stu-id="80be2-193">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="80be2-194">PSTN-Anrufe (keine Umgehung): UC-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="80be2-194">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="80be2-195">PSTN-Anrufe (keine Umgehung): Gateway-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="80be2-195">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="80be2-196">Andere Anruftypen</span><span class="sxs-lookup"><span data-stu-id="80be2-196">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-197"><strong>Anruflautstärke</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-197"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-198">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-198">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-199">Die Gesamtzahl der Anrufe pro Anruftyp.</span><span class="sxs-lookup"><span data-stu-id="80be2-199">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80be2-200"><strong>Prozentsatz der Anrufe schlechter Qualität</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-200"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-201">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-201">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-p113">Die Gesamtzahl der Anrufe, die als Anrufe schlechter Qualität klassifiziert werden. Dies sind Anrufe, bei denen für mindestens eine der gemessenen Metriken der zulässige Wert überschritten wurde (z. B. ein Anruf mit übermäßigem Jitter).</span><span class="sxs-lookup"><span data-stu-id="80be2-p113">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-204"><strong>Anruflautstärke (Funkanruf)</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-204"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-205">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-205">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-206">Die Gesamtzahl der Anrufe, für die eine Funkverbindung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="80be2-206">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80be2-207"><strong>Anruflautstärke (VPN-Anruf)</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-207"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-208">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-208">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-209">Die Gesamtzahl der Anrufe, für die eine VPN-Verbindung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="80be2-209">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-210"><strong>Anruflautstärke (externer Anruf)</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-210"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-211">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-211">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-212">Die Gesamtzahl der Anrufe, für die eine externe Verbindung verwendet wurde (d. h. eine Verbindung außerhalb des internen Netzwerks).</span><span class="sxs-lookup"><span data-stu-id="80be2-212">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80be2-213"><strong>Roundtrip (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-213"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-214">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-214">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-p114">Die durchschnittliche Zeit (in Millisekunden), die ein RTP-Paket (Real-time Transport Protocol) benötigt, um zu einem anderen Endpunkt und wieder zurück zu gelangen. Eine Roundtripzeit von 100 ms oder weniger gilt als akzeptable Qualität.</span><span class="sxs-lookup"><span data-stu-id="80be2-p114">Average amount of (in milliseconds) required for a real-time transport protocol (RTP) packet to travel to another endpoint and then back. Round-trip times of 100 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="80be2-p115">Hohe Roundtripwerte können durch internationale Anrufweiterleitung, eine falsche Routingkonfiguration oder einen überlasteten Medienserver verursacht werden. Sie führen zu Problemen bei bidirektionalen Echtzeit-Audiounterhaltungen.</span><span class="sxs-lookup"><span data-stu-id="80be2-p115">High round-trip values can be caused by international call routing, a routing misconfiguration, or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-219"><strong>Beeinträchtigung (MOS)</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-219"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-220">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-220">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-221">Die durchschnittliche Beeinträchtigung der Qualität, die gemäß Mean Opinion Score (MOS) während eines Anrufs auftrat.</span><span class="sxs-lookup"><span data-stu-id="80be2-221">Average amount of mean opinion score (MOS) degradation experienced during a call.</span></span> <span data-ttu-id="80be2-222">Die Beeinträchtigungswerte liegen zwischen 0,0 (schlecht) und 5,0 (gut).</span><span class="sxs-lookup"><span data-stu-id="80be2-222">Degradation values can range from a low of 0.0 to a high of 5.0.</span></span> <span data-ttu-id="80be2-223">Ein Wert von 0,5 oder weniger gilt als akzeptable Beeinträchtigung.</span><span class="sxs-lookup"><span data-stu-id="80be2-223">A value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="80be2-224">Früher wurden Mean Opinion Scores berechnet, indem man Benutzer die Qualität eines Telefongesprächs auf einer Skala von 1 bis 5 bewerten ließ.</span><span class="sxs-lookup"><span data-stu-id="80be2-224">Historically, mean options scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="80be2-225">In lync Server verwendet lync Server einen Satz von Algorithmen, um vorherzusagen, wie Benutzer einen Anruf bewertet hätten.</span><span class="sxs-lookup"><span data-stu-id="80be2-225">In Lync Server, Lync Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="80be2-p117">Hohe Beeinträchtigungswerte können durch Überlastung, zu geringe Bandbreite, Funknetzüberlastung oder -interferenzen oder durch einen überlasteten Medienserver oder Endpunkt verursacht werden. Eine hohe Beeinträchtigung führt zu verzerrter oder unterbrochener Sprachübertragung.</span><span class="sxs-lookup"><span data-stu-id="80be2-p117">High degradation values can be caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80be2-228"><strong>Paketverlust</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-228"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-229">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-229">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-p118">Die durchschnittliche Rate an RTP-Paketverlusten. Zu Paketverlusten kommt es, wenn RTP-Pakete (RTP ist ein Protokoll für die Übertragung von Audio und Video über das Internet) ihr Ziel nicht erreichen. Hohe Verlustraten werden allgemein durch Überlastung, zu geringe Bandbreite, Funknetzüberlastung oder -interferenzen oder durch einen überlasteten Medienserver verursacht. Paketverluste führen in der Regel zu verzerrter oder unterbrochener Sprachübertragung.</span><span class="sxs-lookup"><span data-stu-id="80be2-p118">Average rate of RTP packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-233"><strong>Jitter (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-233"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-234">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-234">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-235">Der durchschnittliche Jitter, der zwischen dem Eintreffen von RTP-Paketen ermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="80be2-235">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="80be2-236">(Jitter ist ein Maß für die &quot; Zittern eines &quot; Anrufs.) Starke Jitterwerte werden in der Regel durch Überlastung oder einen überladenen Medienserver verursacht, was zu verzerrten oder verlorenen Audiodaten führt.</span><span class="sxs-lookup"><span data-stu-id="80be2-236">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80be2-237"><strong>Ausblendungsverhältnis der Reparatur</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-237"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-238">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-238">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-p120">Das durchschnittliche Verhältnis zwischen ausgeblendeten Audiosamples und der Gesamtzahl der Samples. (Ausgeblendete Audiosamples sind ein Verfahren zum „Glätten“ der „holprigen“ Übertragung, die normalerweise von verworfenen Netzwerkpaketen verursacht wird.) Ein hoher Wert gibt an, dass wegen Paketverlusten oder Jitters Verlustausblendung in großem Umfang angewendet wurde und führt zu verzerrter oder unterbrochener Sprachübertragung.</span><span class="sxs-lookup"><span data-stu-id="80be2-p120">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-241"><strong>Streckungsverhältnis der Reparatur</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-241"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-242">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-242">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-p121">Das durchschnittliche Verhältnis zwischen gestreckten Audiosamples und der Gesamtzahl der Samples. (Gestrecktes Audio ist ein Verfahren zum Dehnen von Audiodaten, um die Gesprächsqualität aufrechtzuerhalten, wenn ein verworfenes Netzwerkpaket festgestellt wurde.) Ein hoher Wert gibt an, dass wegen Jitters Samplestreckung in hohem Umfang aufgetreten ist und führt zu roboterhafter oder verzerrter Sprachqualität.</span><span class="sxs-lookup"><span data-stu-id="80be2-p121">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80be2-245"><strong>Komprimierungsverhältnis der Reparatur</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-245"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-246">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-246">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-p122">Das durchschnittliche Verhältnis zwischen komprimierten Audiosamples und der Gesamtzahl der Samples. (Komprimiertes Audio sind Audiodaten, die komprimiert wurden, um die Gesprächsqualität aufrechtzuerhalten, wenn ein verworfenes Netzwerkpaket festgestellt wurde.) Ein hoher Wert gibt an, dass wegen Jitters Samplekomprimierung in hohem Umfang angewendet wurde und führt zu einer zu schnellen Sprachwiedergabe oder zu verzerrter Sprachqualität.</span><span class="sxs-lookup"><span data-stu-id="80be2-p122">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="media-quality-summary-report-metrics-video-call-summary"></a><span data-ttu-id="80be2-249">Metriken im „Zusammenfassenden Bericht über Medienqualität“: Zusammenfassung der Videoanrufe</span><span class="sxs-lookup"><span data-stu-id="80be2-249">Media Quality Summary Report Metrics: Video Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80be2-250">Name</span><span class="sxs-lookup"><span data-stu-id="80be2-250">Name</span></span></th>
<th><span data-ttu-id="80be2-251">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="80be2-251">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="80be2-252">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80be2-252">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80be2-253"><strong>Anruftyp/Endpunkttyp</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-253"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-254">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-254">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-p123">Wenn Sie auf dieses Element klicken, zeigt der Bericht Details zu den auf diesem Typ basierenden Anrufen. Es gibt folgende Anruftypen:</span><span class="sxs-lookup"><span data-stu-id="80be2-p123">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="80be2-257">UC-Peer-to-Peer-Anrufe</span><span class="sxs-lookup"><span data-stu-id="80be2-257">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="80be2-258">UC-Konferenzsitzungen</span><span class="sxs-lookup"><span data-stu-id="80be2-258">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="80be2-259">PSTN-Konferenzsitzungen</span><span class="sxs-lookup"><span data-stu-id="80be2-259">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="80be2-260">PSTN-Anrufe: Medienumgehung</span><span class="sxs-lookup"><span data-stu-id="80be2-260">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="80be2-261">PSTN-Anrufe (keine Umgehung): UC-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="80be2-261">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="80be2-262">PSTN-Anrufe (keine Umgehung): Gateway-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="80be2-262">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="80be2-263">Andere Anruftypen</span><span class="sxs-lookup"><span data-stu-id="80be2-263">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-264"><strong>Anruflautstärke</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-264"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-265">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-265">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-266">Die Gesamtzahl der Anrufe pro Anruftyp.</span><span class="sxs-lookup"><span data-stu-id="80be2-266">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80be2-267"><strong>Prozentsatz der Anrufe schlechter Qualität</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-267"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-268">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-268">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-p124">Die Gesamtzahl der Anrufe, die als Anrufe schlechter Qualität klassifiziert werden. Dies sind Anrufe, bei denen für mindestens eine der gemessenen Metriken der zulässige Wert überschritten wurde (z. B. ein Anruf mit übermäßigem Jitter).</span><span class="sxs-lookup"><span data-stu-id="80be2-p124">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-271"><strong>Anruflautstärke (Funkanruf)</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-271"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-272">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-272">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-273">Die Gesamtzahl der Anrufe, für die eine Funkverbindung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="80be2-273">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80be2-274"><strong>Anruflautstärke (VPN-Anruf)</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-274"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-275">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-275">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-276">Die Gesamtzahl der Anrufe, für die eine VPN-Verbindung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="80be2-276">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-277"><strong>Anruflautstärke (externer Anruf)</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-277"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-278">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-278">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-279">Die Gesamtzahl der Anrufe, für die eine externe Verbindung verwendet wurde (d. h. eine Verbindung außerhalb des internen Netzwerks).</span><span class="sxs-lookup"><span data-stu-id="80be2-279">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80be2-280"><strong>Durchschnittliche Bitrate (KBit/s)</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-280"><strong>Avg bit-rate (Kbits/s)</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-281">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-281">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-282">Durchschnittliche Video-Bitrate (in Kilobit pro Sekunde).</span><span class="sxs-lookup"><span data-stu-id="80be2-282">Average video bit rate (in kilobits per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-283"><strong>Niedrige Bitrate %</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-283"><strong>Low bit-rate %</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-284">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-284">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-285">Prozentsatz aller Anrufe, bei denen die Bitrate niedrig war.</span><span class="sxs-lookup"><span data-stu-id="80be2-285">Percentage of the call where the bit rate was low.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80be2-286"><strong>Verlust ausgehender Pakete</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-286"><strong>Outbound packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-287">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-287">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-p125">RTP-Paketverluste (Real-Time Transport Protocol) bei ausgehenden Paketen. (Zu Paketverlusten kommt es, wenn RTP-Pakete (ein Protokoll für die Übertragung von Audio und Video über das Internet) ihr Ziel nicht erreichen.) Hohe Verlustraten werden allgemein durch Überlastung, zu geringe Bandbreite, Funknetzüberlastung oder -interferenzen oder durch einen überlasteten Medienserver verursacht. Paketverluste führen in der Regel zu verzerrter oder unterbrochener Sprachübertragung.</span><span class="sxs-lookup"><span data-stu-id="80be2-p125">Real-Time Transport Protocol (RTP) packet loss for outbound packets. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-291"><strong>Eingefrorene Frames %</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-291"><strong>Frozen frame %</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-292">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-292">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-p126">Prozentsatz der „eingefrorenen“ Frames. In einem eingefrorenen Frame wird das Video nicht fortgesetzt, während der Audioteil des Anrufs weitergeht.</span><span class="sxs-lookup"><span data-stu-id="80be2-p126">Percentage of “frozen” frames. In a frozen frame, the video stops advancing while the audio portion of the call continues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80be2-295"><strong>Durchschnittliche ausgehende Framerate</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-295"><strong>Outbound avg frame rate</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-296">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-296">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-297">Durchschnittliche Framerate für ausgehende Übertragungen während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="80be2-297">Average frame rate for outbound transmissions during the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-298"><strong>Durchschnittliche eingehende Framerate</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-298"><strong>Inbound avg frame rate</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-299">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-299">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-300">Durchschnittliche Framerate für eingehende Übertragungen während des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="80be2-300">Average frame rate for incoming transmissions during the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80be2-301"><strong>Niedrige eingehende Framerate %</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-301"><strong>Inbound low frame rate %</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-302">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-302">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-303">Prozentsatz aller Anrufe, bei denen die Bitrate für eingehende Videodaten niedrig war.</span><span class="sxs-lookup"><span data-stu-id="80be2-303">Percentage of the call where the bit rate for incoming video was low.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-304"><strong>Clientintegrität %</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-304"><strong>Client health %</strong></span></span></p></td>
<td></td>
<td><p><span data-ttu-id="80be2-305">Zeigt die relative Integrität des Clientgeräts während des Anrufs an.</span><span class="sxs-lookup"><span data-stu-id="80be2-305">Indicates the relative health of the client device during the call.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="media-quality-summary-report-metrics-application-sharing-call-summary"></a><span data-ttu-id="80be2-306">Metriken im „Zusammenfassenden Bericht über Medienqualität“: Zusammenfassung der Anwendungsfreigabeanrufe</span><span class="sxs-lookup"><span data-stu-id="80be2-306">Media Quality Summary Report Metrics: Application Sharing Call Summary</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="80be2-307">Name</span><span class="sxs-lookup"><span data-stu-id="80be2-307">Name</span></span></th>
<th><span data-ttu-id="80be2-308">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="80be2-308">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="80be2-309">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="80be2-309">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="80be2-310"><strong>Anruftyp/Endpunkttyp</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-310"><strong>Call type/Endpoint type</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-311">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-311">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-p127">Wenn Sie auf dieses Element klicken, zeigt der Bericht Details zu den auf diesem Typ basierenden Anrufen. Es gibt folgende Anruftypen:</span><span class="sxs-lookup"><span data-stu-id="80be2-p127">When you click this item, the report shows detailed information about calls based on that type. Call types include:</span></span></p>
<ul>
<li><p><span data-ttu-id="80be2-314">UC-Peer-to-Peer-Anrufe</span><span class="sxs-lookup"><span data-stu-id="80be2-314">UC Peer-to-Peer Calls</span></span></p></li>
<li><p><span data-ttu-id="80be2-315">UC-Konferenzsitzungen</span><span class="sxs-lookup"><span data-stu-id="80be2-315">UC Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="80be2-316">PSTN-Konferenzsitzungen</span><span class="sxs-lookup"><span data-stu-id="80be2-316">PSTN Conference Sessions</span></span></p></li>
<li><p><span data-ttu-id="80be2-317">PSTN-Anrufe: Medienumgehung</span><span class="sxs-lookup"><span data-stu-id="80be2-317">PSTN Calls: Media Bypass</span></span></p></li>
<li><p><span data-ttu-id="80be2-318">PSTN-Anrufe (keine Umgehung): UC-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="80be2-318">PSTN Calls (Non-Bypass): UC Leg</span></span></p></li>
<li><p><span data-ttu-id="80be2-319">PSTN-Anrufe (keine Umgehung): Gateway-Abschnitt</span><span class="sxs-lookup"><span data-stu-id="80be2-319">PSTN Calls (Non-Bypass): Gateway Leg</span></span></p></li>
<li><p><span data-ttu-id="80be2-320">Andere Anruftypen</span><span class="sxs-lookup"><span data-stu-id="80be2-320">Other Call Types</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-321"><strong>Anruflautstärke</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-321"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-322">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-322">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-323">Die Gesamtzahl der Anrufe pro Anruftyp.</span><span class="sxs-lookup"><span data-stu-id="80be2-323">Total number of calls per call type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80be2-324"><strong>Prozentsatz der Anrufe schlechter Qualität</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-324"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-325">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-325">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-p128">Die Gesamtzahl der Anrufe, die als Anrufe schlechter Qualität klassifiziert werden. Dies sind Anrufe, bei denen für mindestens eine der gemessenen Metriken der zulässige Wert überschritten wurde (z. B. ein Anruf mit übermäßigem Jitter).</span><span class="sxs-lookup"><span data-stu-id="80be2-p128">Total number of calls classified as poor. A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-328"><strong>Anruflautstärke (Funkanruf)</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-328"><strong>Call volume (wireless call)</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-329">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-329">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-330">Die Gesamtzahl der Anrufe, für die eine Funkverbindung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="80be2-330">Total number of calls that used a wireless connection.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80be2-331"><strong>Anruflautstärke (VPN-Anruf)</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-331"><strong>Call volume (VPN call)</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-332">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-332">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-333">Die Gesamtzahl der Anrufe, für die eine VPN-Verbindung verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="80be2-333">Total number of calls that used a VPN connection.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-334"><strong>Anruflautstärke (externer Anruf)</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-334"><strong>Call volume (external call)</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-335">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-335">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-336">Die Gesamtzahl der Anrufe, für die eine externe Verbindung verwendet wurde (d. h. eine Verbindung außerhalb des internen Netzwerks).</span><span class="sxs-lookup"><span data-stu-id="80be2-336">Number of calls that used an external connection (that is, a connection outside the internal network).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80be2-337"><strong>Jitter (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-337"><strong>Jitter (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-338">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-338">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-339">Der durchschnittliche Jitter, der zwischen dem Eintreffen von RTP-Paketen ermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="80be2-339">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="80be2-340">(Jitter ist ein Maß für die &quot; Zittern eines &quot; Anrufs.) Starke Jitterwerte werden in der Regel durch Überlastung oder einen überladenen Medienserver verursacht, was zu verzerrten oder verlorenen Audiodaten führt.</span><span class="sxs-lookup"><span data-stu-id="80be2-340">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-341"><strong>Durchschnittliche relative unidirektionale Verzögerung</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-341"><strong>Avg. relative one way</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-342">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-342">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-p130">Durchschnittliche relative unidirektionale Verzögerung zwischen zwei Medienendpunkten. Dies ist ein Single-Hop-Latenzmaß.</span><span class="sxs-lookup"><span data-stu-id="80be2-p130">Average relative one-way delay between two media endpoints. This is a single-hop latency measure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="80be2-345"><strong>Durchschnittliche Latenz der RDP-Kachelverarbeitung</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-345"><strong>Avg. RDP tile processing latency</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-346">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-346">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-p131">Die durchschnittliche Latenz der RDP-Kachelverarbeitung im AS-Konferenzserver über die Dauer der Anzeigesitzung. Ein hoher Durchschnitt zeigt eine längere Verzögerung bei der Anzeige an und bezieht Netzwerklatenz mit ein. Ein überlasteter Konferenzserver weist gegebenenfalls höhere durchschnittliche Verzögerungen auf.</span><span class="sxs-lookup"><span data-stu-id="80be2-p131">The average RDP tile processing latency in the AS Conferencing Server over the duration of the viewing session. A high average reflects a longer delay in the viewing experience, and includes network latency. An overloaded conferencing server may experience higher average delays.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="80be2-350"><strong>Ungültige Kacheln insgesamt %</strong></span><span class="sxs-lookup"><span data-stu-id="80be2-350"><strong>Total spoiled tile %</strong></span></span></p></td>
<td><p><span data-ttu-id="80be2-351">Nein</span><span class="sxs-lookup"><span data-stu-id="80be2-351">No</span></span></p></td>
<td><p><span data-ttu-id="80be2-352">Gesamtprozentsatz schlechter RDP-Kacheln.</span><span class="sxs-lookup"><span data-stu-id="80be2-352">Total percentage of spoiled RDP tiles.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="80be2-353">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="80be2-353">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

