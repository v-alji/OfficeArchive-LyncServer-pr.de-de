---
title: 'Lync Server 2013: Anruf Detail Bericht'
description: 'Lync Server 2013: Anruf Detail Bericht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Detail Report
ms:assetid: 38862e35-3fec-41b9-a035-0b301942d446
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558637(v=OCS.15)
ms:contentKeyID: 48183843
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d72ae6c1c1ec869041eee5b0dc35941c33609710
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394806"
---
# <a name="call-detail-report-in-lync-server-2013"></a><span data-ttu-id="15041-103">Anruf Detail Bericht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="15041-103">Call Detail Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="15041-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="15041-104">

<span> </span></span></span>

<span data-ttu-id="15041-105">_**Letztes Änderungsdatum des Themas:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="15041-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="15041-106">Der Anruf Detailbericht bietet einen detaillierten Überblick über einen einzelnen Anruf. der Bericht enthält nahezu alle von lync Server gesammelten Metriken für die Qualität der Benutzerfreundlichkeit und die in Berichtsabschnitte unterteilten Statistiken, wie beispielsweise:</span><span class="sxs-lookup"><span data-stu-id="15041-106">The Call Detail Report provides a detailed look at an individual call; the report includes nearly all the Quality of Experience metrics and statistics collected by Lync Server, divided into report sections such as:</span></span>

  - <span data-ttu-id="15041-107">Anrufinformationen</span><span class="sxs-lookup"><span data-stu-id="15041-107">Call Information</span></span>

  - <span data-ttu-id="15041-108">Gerät und Signalmetrik des Anrufers</span><span class="sxs-lookup"><span data-stu-id="15041-108">Caller Device and Signal Metrics</span></span>

  - <span data-ttu-id="15041-109">Gerät und Signalmetrik des Angerufenen</span><span class="sxs-lookup"><span data-stu-id="15041-109">Callee Device and Signal metrics</span></span>

  - <span data-ttu-id="15041-110">Clientereignis des Anrufers</span><span class="sxs-lookup"><span data-stu-id="15041-110">Caller Client Event</span></span>

  - <span data-ttu-id="15041-111">Clientereignis des Angerufenen</span><span class="sxs-lookup"><span data-stu-id="15041-111">Callee Client Event</span></span>

  - <span data-ttu-id="15041-112">Audiodatenstrom (Anrufer zum Angerufenen)</span><span class="sxs-lookup"><span data-stu-id="15041-112">Audio Stream (Caller to Callee)</span></span>

  - <span data-ttu-id="15041-113">Videodatenstrom (Anrufer zum Angerufenen)</span><span class="sxs-lookup"><span data-stu-id="15041-113">Video Stream (Caller to Callee)</span></span>

  - <span data-ttu-id="15041-114">Audiodatenstrom (Angerufener zum Anrufer)</span><span class="sxs-lookup"><span data-stu-id="15041-114">Audio Stream (Callee to Caller)</span></span>

  - <span data-ttu-id="15041-115">Videodatenstrom (Angerufener zum Anrufer)</span><span class="sxs-lookup"><span data-stu-id="15041-115">Video Stream (Callee to Caller)</span></span>

<span data-ttu-id="15041-p101">Beachten Sie, dass die Kategorien und Metriken in einem bestimmten Bericht zum einen vom Typ der Sitzung und zum anderen vom Typ der Endpunkte abhängen, die in der Sitzung verwendet werden. Bei einem reinen Audioanruf werden keine Metriken für Videodatenströme gemeldet, da der Anruf keinen Videodatenstrom beinhaltete. Entsprechend werden in einem Bericht ggf. zwar Anruferstatistiken, aber keine Statistiken zum Angerufen angezeigt. Dies liegt normalerweise daran, dass der Angerufene kein SIP-kompatibles Gerät verwendet. Endpunkte sind für das Melden von Statistiken am Ende des Anrufs verantwortlich. Ein Mobiltelefon (das SIP oder SIP-Statistiken nicht unterstützt) kann diese Informationen jedoch nicht melden. Wenn Sie jemanden anrufen und diese Person den Anruf auf einem Mobiltelefon entgegennimmt, erhalten Sie keinen Bericht von diesem Mobiltelefon, wenn der Anruf beendet wird.</span><span class="sxs-lookup"><span data-stu-id="15041-p101">Keep in mind that the categories and the metrics you see on a given report depend on two things: the type of session and the type of endpoints used in the session. For example, an audio-only call will not report metrics for video streams; that's because the call didn't have a video stream. Likewise, you might have a report that lists caller statistics but not callee statistics. That's typically because the callee was not using a SIP-compliant device. Endpoints are responsible for reporting statistics at the end of a call; however, a cell phone (which knows nothing about SIP or SIP statistics) is unable to report that kind of information. If you call someone and they answer you on their cell phone, you will not get a report from that cell phone when the call ends.</span></span>

<span data-ttu-id="15041-122">Der Anrufdetailbericht ist sehr nützlich, wenn Sie genau feststellen möchten, warum bei einem bestimmten Anruf Probleme in Bezug auf die Medienqualität aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="15041-122">The Call Detail Report is most useful when you are trying to determine exactly why a given call experienced media quality problems.</span></span>

<div>

## <a name="accessing-the-call-detail-report"></a><span data-ttu-id="15041-123">Zugreifen auf den Anrufdetailbericht</span><span class="sxs-lookup"><span data-stu-id="15041-123">Accessing the Call Detail Report</span></span>

<span data-ttu-id="15041-124">Auf den Anrufdetailbericht kann von einem der folgenden Berichte aus zugegriffen werden:</span><span class="sxs-lookup"><span data-stu-id="15041-124">The Call Detail Report can be accessed from any of the following reports:</span></span>

  - <span data-ttu-id="15041-125">Der [Standortbericht in lync Server 2013](lync-server-2013-location-report.md) (durch Klicken auf das Anrufvolumen oder den Prozentsatz für den schlechten Anruf)</span><span class="sxs-lookup"><span data-stu-id="15041-125">The [Location Report in Lync Server 2013](lync-server-2013-location-report.md) (by clicking either the Call volume or the Poor call percentage metric)</span></span>

  - <span data-ttu-id="15041-126">Der [Bericht zur Zusammenfassung der Medienqualität in lync Server 2013](lync-server-2013-media-quality-summary-report.md) (durch Klicken auf den Prozentsatz der Anruflautstärke oder die schlechte Anruf Rate)</span><span class="sxs-lookup"><span data-stu-id="15041-126">The [Media Quality Summary Report in Lync Server 2013](lync-server-2013-media-quality-summary-report.md) (by clicking either the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="15041-127">Der [Bericht zum Vergleich der Medienqualität in lync Server 2013](lync-server-2013-media-quality-comparison-report.md) (durch Klicken auf den [Bericht Anrufliste in lync Server 2013](lync-server-2013-call-list-report.md) und anschließendes Klicken auf die Detail Metrik).</span><span class="sxs-lookup"><span data-stu-id="15041-127">The [Media Quality Comparison Report in Lync Server 2013](lync-server-2013-media-quality-comparison-report.md) (by clicking the [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) and then clicking the Detail metric).</span></span>

  - <span data-ttu-id="15041-128">Der [Bericht zur Serverleistung in lync Server 2013](lync-server-2013-server-performance-report.md) (durch Klicken auf den Prozentsatz der Anruflautstärke oder des schlechten Anrufs)</span><span class="sxs-lookup"><span data-stu-id="15041-128">The [Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md) (by clicking either the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="15041-129">Der [Anruflistenbericht in lync Server 2013](lync-server-2013-call-list-report.md) (durch Klicken auf die Detail Metrik)</span><span class="sxs-lookup"><span data-stu-id="15041-129">The [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) (by clicking the Detail metric)</span></span>

<span data-ttu-id="15041-130">Innerhalb des Anruf Detail Berichts können Sie auf den [gerätebericht in lync Server 2013](lync-server-2013-device-report.md) zugreifen, indem Sie auf eine der folgenden Metriken klicken:</span><span class="sxs-lookup"><span data-stu-id="15041-130">From within the Call Detail Report you can access the [Device Report in Lync Server 2013](lync-server-2013-device-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="15041-131">Aufnahmegerät</span><span class="sxs-lookup"><span data-stu-id="15041-131">Capture device</span></span>

  - <span data-ttu-id="15041-132">Darstellungsgerät</span><span class="sxs-lookup"><span data-stu-id="15041-132">Render device</span></span>

<span data-ttu-id="15041-133">Sie können auch auf den Trendbericht über Medienqualität des Servers zugreifen, indem Sie auf die Metrik „A/V-Edgeserver“ klicken.</span><span class="sxs-lookup"><span data-stu-id="15041-133">You can also access the Server Media Quality Trend Report by clicking the A/V edge server metric.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-detail-report"></a><span data-ttu-id="15041-134">Optimale Verwendung des Anrufdetailberichts</span><span class="sxs-lookup"><span data-stu-id="15041-134">Making the Best Use of the Call Detail Report</span></span>

<span data-ttu-id="15041-p102">Der Anrufdetailbericht umfasst normalerweise 250 verschiedene Metriken. Hierzu gehören „Zeitstempelabweichung des Mikrofons“, „Geringer Rauschabstand, Zeit“ und „Nahes Ende zu Echo, Zeit“. Wenn Sie nicht genau wissen, was mit diesen Metriken gemessen wird, können Sie mit der Maus auf die Bezeichnung der Metrik zeigen. In den meisten Fällen erscheint dann eine QuickInfo mit einer Metrikbeschreibung.</span><span class="sxs-lookup"><span data-stu-id="15041-p102">The Call Detail Report typically includes over 250 different metrics, including such items as Microphone timestamp drift, Low SNR time, and Near end to echo time. If you can't remember what all of these metrics actually measure, try holding your mouse over the metric label; often-times, a tooltip will appear describing that metric.</span></span>

<span data-ttu-id="15041-137">Wenn Sie Probleme beim Auffinden einer Metrik haben, geben Sie einen Teil der metrischen Beschriftung im Suchfeld ein, und klicken Sie dann auf suchen.</span><span class="sxs-lookup"><span data-stu-id="15041-137">If you have problems locating a metric, type part of the metric label in the search box and then click Find.</span></span> <span data-ttu-id="15041-138">Wenn Sie beispielsweise die niedrige SNR-Zeit Metrik nicht finden können, geben Sie im Suchfeld SNR ein, und klicken Sie dann auf suchen.</span><span class="sxs-lookup"><span data-stu-id="15041-138">For example, if you can't find the Low SNR time metric, type SNR in the search box and then click Find.</span></span>

<span data-ttu-id="15041-p104">Beachten Sie, dass im Bericht nur Informationen zu einem Anruf verfolgt werden. Der Anruf selbst wird nicht aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="15041-p104">Note that the report only tracks information about a call. The call itself is not recorded.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="15041-141">Filter</span><span class="sxs-lookup"><span data-stu-id="15041-141">Filters</span></span>

<span data-ttu-id="15041-p105">Keine. Der Anrufdetailbericht lässt sich nicht filtern.</span><span class="sxs-lookup"><span data-stu-id="15041-p105">None. You cannot filter the Call Detail Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="15041-144">Metriken</span><span class="sxs-lookup"><span data-stu-id="15041-144">Metrics</span></span>

<span data-ttu-id="15041-145">In der folgenden Tabelle werden die Metriken aufgelistet, die im Anrufdetailbericht für jeden Anruf angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="15041-145">The following table lists the information provided in the Call Detail Report for each call.</span></span>

### <a name="call-detail-report-metrics"></a><span data-ttu-id="15041-146">Metriken im Anrufdetailbericht</span><span class="sxs-lookup"><span data-stu-id="15041-146">Call Detail Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="15041-147">Name</span><span class="sxs-lookup"><span data-stu-id="15041-147">Name</span></span></th>
<th><span data-ttu-id="15041-148">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="15041-148">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="15041-149">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="15041-149">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="15041-150"><strong>PAI des Anrufers</strong></span><span class="sxs-lookup"><span data-stu-id="15041-150"><strong>Caller PAI</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-151">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-151">No</span></span></p></td>
<td><p><span data-ttu-id="15041-p106">Die P-Asserted-Identity (P-Asserted-ID) des Benutzers, der den Anruf initiiert hat. Diese dient zur Übermittlung der nachgewiesenen Identität eines Benutzers innerhalb eines vertrauenswürdigen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="15041-p106">P-Asserted-Identity of the user who initiated the call. The P-Asserted-Identity is used to convey the proven identity of a user within a trusted network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15041-154"><strong>URI des Anrufers</strong></span><span class="sxs-lookup"><span data-stu-id="15041-154"><strong>Caller URI</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-155">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-155">No</span></span></p></td>
<td><p><span data-ttu-id="15041-156">Die SIP-Adresse des Benutzers, der den Anruf initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="15041-156">SIP address of the user who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15041-157"><strong>Endpunkt des Anrufers</strong></span><span class="sxs-lookup"><span data-stu-id="15041-157"><strong>Caller endpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-158">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-158">No</span></span></p></td>
<td><p><span data-ttu-id="15041-159">Das Gerät, mit dem der Anruf ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="15041-159">Device used to make the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15041-160"><strong>Benutzer-Agent des Anrufers</strong></span><span class="sxs-lookup"><span data-stu-id="15041-160"><strong>Caller user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-161">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-161">No</span></span></p></td>
<td><p><span data-ttu-id="15041-162">Die Software, die auf dem Gerät verwendet wird, mit dem der Anruf ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="15041-162">Software used on the device that made the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15041-163"><strong>Startzeit des Anrufs</strong></span><span class="sxs-lookup"><span data-stu-id="15041-163"><strong>Call start</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-164">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-164">No</span></span></p></td>
<td><p><span data-ttu-id="15041-165">Der Zeitpunkt (Datum und Uhrzeit), zu dem der Anruf ursprünglich getätigt wurde.</span><span class="sxs-lookup"><span data-stu-id="15041-165">Date and time that the call was initially placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15041-166"><strong>Vermittlungsserver-Umgehungsanruf</strong></span><span class="sxs-lookup"><span data-stu-id="15041-166"><strong>Mediation Server bypass call</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-167">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-167">No</span></span></p></td>
<td><p><span data-ttu-id="15041-168">Gibt an, ob der Anruf mit einem PSTN-VoIP-Gateway oder einer qualifizierten IP-Nebenstellenanlage verbunden wurde, ohne dass er über den Vermittlungsserver geleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="15041-168">Indicates whether the call connected to a PSTN voice gateway or qualified IP-PBX without passing through the Mediation Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15041-169"><strong>Betriebssystem des Anrufers</strong></span><span class="sxs-lookup"><span data-stu-id="15041-169"><strong>Caller OS</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-170">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-170">No</span></span></p></td>
<td><p><span data-ttu-id="15041-171">Das Betriebssystem auf dem Computer des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="15041-171">Operating system of the caller's computer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15041-172"><strong>CPU des Anrufers</strong></span><span class="sxs-lookup"><span data-stu-id="15041-172"><strong>Caller CPU</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-173">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-173">No</span></span></p></td>
<td><p><span data-ttu-id="15041-174">Die CPU, die im Computer des Benutzers installiert ist, der den Anruf initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="15041-174">CPU installed in the computer of the user who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15041-175"><strong>CPU-Kernnummer des Anrufers</strong></span><span class="sxs-lookup"><span data-stu-id="15041-175"><strong>Caller CPU core number</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-176">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-176">No</span></span></p></td>
<td><p><span data-ttu-id="15041-177">Die Nummer des Prozessors in dem Computer des Benutzers, der den Anruf initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="15041-177">Processor number in the computer used by the person who initiated the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15041-178"><strong>CPU-Geschwindigkeit des Anrufers</strong></span><span class="sxs-lookup"><span data-stu-id="15041-178"><strong>Caller CPU speed</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-179">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-179">No</span></span></p></td>
<td><p><span data-ttu-id="15041-180">Die Taktfrequenz der CPU des Computers des Benutzers, der den Anruf initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="15041-180">Clock speed of the CPU of the computer used by the person who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15041-181"><strong>CPU-Virtualisierung des Anrufers</strong></span><span class="sxs-lookup"><span data-stu-id="15041-181"><strong>Caller CPU virtualization</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-182">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-182">No</span></span></p></td>
<td><p><span data-ttu-id="15041-183">Ggf. die Virtualisierung, die auf dem Computer des Benutzers implementiert ist, der den Anruf initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="15041-183">Virtualization (if any) used on the computer used by the person who initiated the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15041-184"><strong>PAI des Angerufenen</strong></span><span class="sxs-lookup"><span data-stu-id="15041-184"><strong>Callee PAI</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-185">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-185">No</span></span></p></td>
<td><p><span data-ttu-id="15041-p107">Die P-Asserted-Identity (P-Asserted-ID) des Benutzers, der zur Teilnahme an dem Anruf eingeladen wurde. Diese dient zur Übermittlung der nachgewiesenen Identität eines Benutzers innerhalb eines vertrauenswürdigen Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="15041-p107">P-Asserted-Identity of the user who was invited to join the call. The P-Asserted-Identity is used to convey the proven identity of a user within a trusted network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15041-188"><strong>URI des Angerufenen</strong></span><span class="sxs-lookup"><span data-stu-id="15041-188"><strong>Callee URI</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-189">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-189">No</span></span></p></td>
<td><p><span data-ttu-id="15041-190">Die SIP-Adresse des Benutzers, der angerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="15041-190">SIP address of the user who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15041-191"><strong>Endpunkt des Angerufenen</strong></span><span class="sxs-lookup"><span data-stu-id="15041-191"><strong>Callee endpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-192">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-192">No</span></span></p></td>
<td><p><span data-ttu-id="15041-193">Das Gerät, mit dem der Anruf angenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="15041-193">Device used to receive the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15041-194"><strong>Benutzer-Agent des Angerufenen</strong></span><span class="sxs-lookup"><span data-stu-id="15041-194"><strong>Callee user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-195">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-195">No</span></span></p></td>
<td><p><span data-ttu-id="15041-196">Die Software, die auf dem Gerät verwendet wird, mit dem der Anruf angenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="15041-196">Software used on the device that received the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15041-197"><strong>Dauer</strong></span><span class="sxs-lookup"><span data-stu-id="15041-197"><strong>Duration</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-198">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-198">No</span></span></p></td>
<td><p><span data-ttu-id="15041-199">Die Dauer des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="15041-199">Length of time for the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15041-200"><strong>Vermittlungsserver-Umgehungswarnung</strong></span><span class="sxs-lookup"><span data-stu-id="15041-200"><strong>Media bypass warning flag</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-201">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-201">No</span></span></p></td>
<td><p><span data-ttu-id="15041-202">Eine Warnung, die ausgegeben wird, wenn der Vermittlungsserver umgangen wurde.</span><span class="sxs-lookup"><span data-stu-id="15041-202">Warning issued when the Mediation Server was bypassed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15041-203"><strong>Betriebssystem des Angerufenen</strong></span><span class="sxs-lookup"><span data-stu-id="15041-203"><strong>Callee OS</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-204">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-204">No</span></span></p></td>
<td><p><span data-ttu-id="15041-205">Das Betriebssystem auf dem Computer des Benutzers, der angerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="15041-205">Operating system of the computer for the user who was called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15041-206"><strong>CPU des Angerufenen</strong></span><span class="sxs-lookup"><span data-stu-id="15041-206"><strong>Callee CPU</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-207">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-207">No</span></span></p></td>
<td><p><span data-ttu-id="15041-208">Die CPU, die im Computer des Benutzers installiert ist, der angerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="15041-208">CPU installed in the computer of the user who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15041-209"><strong>CPU-Kernnummer des Angerufenen</strong></span><span class="sxs-lookup"><span data-stu-id="15041-209"><strong>Callee core number</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-210">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-210">No</span></span></p></td>
<td><p><span data-ttu-id="15041-211">Die Nummer des Prozessors in dem Computer des Benutzers, der angerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="15041-211">Processor number in the computer used by the person who was called.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="15041-212"><strong>CPU-Geschwindigkeit des Angerufenen</strong></span><span class="sxs-lookup"><span data-stu-id="15041-212"><strong>Callee CPU speed</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-213">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-213">No</span></span></p></td>
<td><p><span data-ttu-id="15041-214">Die Taktfrequenz der CPU des Computers des Benutzers, der angerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="15041-214">Clock speed of the CPU of the computer used by the person who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="15041-215"><strong>CPU-Virtualisierung des Angerufenen</strong></span><span class="sxs-lookup"><span data-stu-id="15041-215"><strong>Callee CPU virtualization</strong></span></span></p></td>
<td><p><span data-ttu-id="15041-216">Nein</span><span class="sxs-lookup"><span data-stu-id="15041-216">No</span></span></p></td>
<td><p><span data-ttu-id="15041-217">Ggf. die Virtualisierung, die auf dem Computer des Benutzers implementiert ist, der angerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="15041-217">Virtualization (if any) used on the computer used by the person who was called.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="15041-218">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="15041-218">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

