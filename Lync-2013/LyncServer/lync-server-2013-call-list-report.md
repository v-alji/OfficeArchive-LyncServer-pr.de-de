---
title: 'Lync Server 2013: Anruflistenbericht'
description: 'Lync Server 2013: Anruflistenbericht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call List Report
ms:assetid: 9739f9f0-7a37-4844-91d5-f089d2011013
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615020(v=OCS.15)
ms:contentKeyID: 48184921
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5b08d4c5f3011facc9cd8d4f6b2800638f3cc896
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435754"
---
# <a name="call-list-report-in-lync-server-2013"></a><span data-ttu-id="c0c73-103">Bericht zur Anrufliste in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c0c73-103">Call List Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c0c73-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c0c73-104">

<span> </span></span></span>

<span data-ttu-id="c0c73-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="c0c73-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="c0c73-106">Der Anruflistenbericht enthält QoE-Metriken (Quality of Experience) für einzelne Anrufe, die in Ihrer Organisation getätigt oder empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="c0c73-106">The Call List Report provides Quality of Experience (QoE) metrics for individual calls made and received in your organization.</span></span> <span data-ttu-id="c0c73-107">Beachten Sie, dass die tatsächlich im Bericht verzeichneten Metriken davon abhängen, wie Sie auf den Anruflistenbericht zugreifen.</span><span class="sxs-lookup"><span data-stu-id="c0c73-107">Note that the actual metrics reported will depend on how you access the Call List report.</span></span> <span data-ttu-id="c0c73-108">Wenn Sie beispielsweise den Bericht aus dem [gerätebericht in lync Server 2013](lync-server-2013-device-report.md)öffnen, werden Metriken wie die folgenden Metriken angezeigt, die auch im gerätebericht angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="c0c73-108">For example, if you open the report from the [Device Report in Lync Server 2013](lync-server-2013-device-report.md), you'll see metrics such as the following, metrics that are also reported on the Device Report:</span></span>

  - <span data-ttu-id="c0c73-109">Mikrofon des Anrufers</span><span class="sxs-lookup"><span data-stu-id="c0c73-109">Caller's microphone</span></span>

  - <span data-ttu-id="c0c73-110">Lautsprecher des Anrufers</span><span class="sxs-lookup"><span data-stu-id="c0c73-110">Caller's speaker</span></span>

  - <span data-ttu-id="c0c73-111">Mikrofon des Angerufenen</span><span class="sxs-lookup"><span data-stu-id="c0c73-111">Callee's microphone</span></span>

  - <span data-ttu-id="c0c73-112">Lautsprecher des Angerufenen</span><span class="sxs-lookup"><span data-stu-id="c0c73-112">Callee's speaker</span></span>

  - <span data-ttu-id="c0c73-113">Anteil Sprachumschaltzeit</span><span class="sxs-lookup"><span data-stu-id="c0c73-113">Ratio of voice switch time</span></span>

<span data-ttu-id="c0c73-114">Wenn Sie den Anruflistenbericht aber über den [Standortbericht in lync Server 2013](lync-server-2013-location-report.md)öffnen, werden keine dieser Metriken angezeigt. Stattdessen werden Metriken wie die folgenden angezeigt:</span><span class="sxs-lookup"><span data-stu-id="c0c73-114">However, if you open the Call List Report from the [Location Report in Lync Server 2013](lync-server-2013-location-report.md), you won't see any of those metrics; instead, you'll see metrics like these:</span></span>

  - <span data-ttu-id="c0c73-115">Roundtrip (ms)</span><span class="sxs-lookup"><span data-stu-id="c0c73-115">Round trip (ms)</span></span>

  - <span data-ttu-id="c0c73-116">Beeinträchtigung (MOS)</span><span class="sxs-lookup"><span data-stu-id="c0c73-116">Degradation (MOS)</span></span>

  - <span data-ttu-id="c0c73-117">Paketverlust</span><span class="sxs-lookup"><span data-stu-id="c0c73-117">Packet loss</span></span>

  - <span data-ttu-id="c0c73-118">Jitter (ms)</span><span class="sxs-lookup"><span data-stu-id="c0c73-118">Jitter (ms)</span></span>

<span data-ttu-id="c0c73-p102">Dies sind Metriken aus dem Standortbericht. Im Anruflistenbericht können Sie jedoch jederzeit auf die Metrikdetails klicken und zu allen Anrufen vollständige QoE-Informationen anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c0c73-p102">Those are the metrics reported on the Location Report. However, from the Call List Report you can always click the Detail metric to provide complete QoE information for any call.</span></span>

<div>

## <a name="accessing-the-call-list-report"></a><span data-ttu-id="c0c73-121">Zugriff auf den Anruflistenbericht</span><span class="sxs-lookup"><span data-stu-id="c0c73-121">Accessing the Call List Report</span></span>

<span data-ttu-id="c0c73-122">Auf den Anruflistenbericht kann über alle folgenden Berichte zugegriffen werden:</span><span class="sxs-lookup"><span data-stu-id="c0c73-122">The Call List Report can be accessed from any of the following reports:</span></span>

  - <span data-ttu-id="c0c73-123">Der [Standortbericht in lync Server 2013](lync-server-2013-location-report.md) (durch Klicken auf die Lautstärke des Anrufs oder die prozentuale Kennzahl für schlechten Anruf)</span><span class="sxs-lookup"><span data-stu-id="c0c73-123">The [Location Report in Lync Server 2013](lync-server-2013-location-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="c0c73-124">Der [gerätebericht in lync Server 2013](lync-server-2013-device-report.md) (durch Klicken auf die Lautstärke des Anrufs oder die prozentuale Kennzahl für schlechten Anruf)</span><span class="sxs-lookup"><span data-stu-id="c0c73-124">The [Device Report in Lync Server 2013](lync-server-2013-device-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="c0c73-125">Der [Bericht zur Zusammenfassung der Medienqualität in lync Server 2013](lync-server-2013-media-quality-summary-report.md) (durch Klicken auf das Anrufvolumen oder die prozentuale Kennzahl für schlechten Anruf)</span><span class="sxs-lookup"><span data-stu-id="c0c73-125">The [Media Quality Summary Report in Lync Server 2013](lync-server-2013-media-quality-summary-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

  - <span data-ttu-id="c0c73-126">Der [Server Leistungsbericht in lync Server 2013](lync-server-2013-server-performance-report.md) (durch Klicken auf das Anrufvolumen oder die prozentuale Kennzahl für schlechten Anruf)</span><span class="sxs-lookup"><span data-stu-id="c0c73-126">The [Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md) (by clicking the Call volume or Poor call percentage metric)</span></span>

<span data-ttu-id="c0c73-127">Innerhalb des Anruflisten Berichts können Sie auf den [Anruf Detailbericht in lync Server 2013](lync-server-2013-call-detail-report.md) zugreifen, indem Sie auf die Detail Metrik klicken.</span><span class="sxs-lookup"><span data-stu-id="c0c73-127">From within the Call List Report you can access the [Call Detail Report in Lync Server 2013](lync-server-2013-call-detail-report.md) by clicking the Detail metric.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-call-list-report"></a><span data-ttu-id="c0c73-128">Optimale Verwendung des Anruflistenberichts</span><span class="sxs-lookup"><span data-stu-id="c0c73-128">Making the Best Use of the Call List Report</span></span>

<span data-ttu-id="c0c73-129">Wenn Sie vergessen haben, wofür einige der Anruflistenberichtsmetriken stehen (z. B. der Anteil Sprachumschaltzeit), bewegen Sie den Mauszeiger über die Beschriftung der Metrik, damit eine QuickInfo mit einer kurzen Beschreibung der Metrik angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="c0c73-129">If you can't remember what some of the Call List Report metrics (such as Ratio voice switch time) actually measure, hold your mouse over the metric label; a tool tip will then appear giving you a brief description of the metric.</span></span>

</div>

<div>

## <a name="filters"></a><span data-ttu-id="c0c73-130">Filter</span><span class="sxs-lookup"><span data-stu-id="c0c73-130">Filters</span></span>

<span data-ttu-id="c0c73-p103">Keine. Sie können den Anruflistenbericht nicht filtern.</span><span class="sxs-lookup"><span data-stu-id="c0c73-p103">None. You cannot filter the Call List Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="c0c73-133">Metriken</span><span class="sxs-lookup"><span data-stu-id="c0c73-133">Metrics</span></span>

<span data-ttu-id="c0c73-134">In der folgenden Tabelle sind die im Anruflistenbericht enthaltenen Informationen für jeden Anruf aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="c0c73-134">The following table lists the information provided in the Call List Report for each call.</span></span>

### <a name="call-list-report-metrics"></a><span data-ttu-id="c0c73-135">Anruflistenbericht-Metriken</span><span class="sxs-lookup"><span data-stu-id="c0c73-135">Call List Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c0c73-136">Name</span><span class="sxs-lookup"><span data-stu-id="c0c73-136">Name</span></span></th>
<th><span data-ttu-id="c0c73-137">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="c0c73-137">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="c0c73-138">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c0c73-138">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c0c73-139"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="c0c73-139"><strong>Details</strong></span></span></p></td>
<td><p><span data-ttu-id="c0c73-140">Nein</span><span class="sxs-lookup"><span data-stu-id="c0c73-140">No</span></span></p></td>
<td><p><span data-ttu-id="c0c73-141">Wenn Sie auf dieses Element klicken, werden zusätzliche Informationen über den Anruf angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c0c73-141">When you click this item, the report shows additional information on the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0c73-142"><strong>Anrufer</strong></span><span class="sxs-lookup"><span data-stu-id="c0c73-142"><strong>Caller</strong></span></span></p></td>
<td><p><span data-ttu-id="c0c73-143">Ja</span><span class="sxs-lookup"><span data-stu-id="c0c73-143">Yes</span></span></p></td>
<td><p><span data-ttu-id="c0c73-144">SIP-Adresse der Person, die den Anruf initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="c0c73-144">SIP address of the person who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0c73-145"><strong>Callee</strong></span><span class="sxs-lookup"><span data-stu-id="c0c73-145"><strong>Callee</strong></span></span></p></td>
<td><p><span data-ttu-id="c0c73-146">Ja</span><span class="sxs-lookup"><span data-stu-id="c0c73-146">Yes</span></span></p></td>
<td><p><span data-ttu-id="c0c73-147">SIP-Adresse der Person, die angerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="c0c73-147">SIP address of the person who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0c73-148"><strong>Startzeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="c0c73-148"><strong>Start time</strong></span></span></p></td>
<td><p><span data-ttu-id="c0c73-149">Ja</span><span class="sxs-lookup"><span data-stu-id="c0c73-149">Yes</span></span></p></td>
<td><p><span data-ttu-id="c0c73-150">Datum und Uhrzeit des Beginns des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="c0c73-150">Date and time that the call started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0c73-151"><strong>Endzeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="c0c73-151"><strong>End time</strong></span></span></p></td>
<td><p><span data-ttu-id="c0c73-152">Ja</span><span class="sxs-lookup"><span data-stu-id="c0c73-152">Yes</span></span></p></td>
<td><p><span data-ttu-id="c0c73-153">Datum und Uhrzeit des Endes des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="c0c73-153">Date and time that the call ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0c73-154"><strong>Benutzer-Agent des Anrufers</strong></span><span class="sxs-lookup"><span data-stu-id="c0c73-154"><strong>Caller user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="c0c73-155">Ja</span><span class="sxs-lookup"><span data-stu-id="c0c73-155">Yes</span></span></p></td>
<td><p><span data-ttu-id="c0c73-156">Software, die vom Endpunkt der Person, die den Anruf initiiert hat, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c0c73-156">Software used by the endpoint of the person who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0c73-157"><strong>Benutzer-Agent des Angerufenen</strong></span><span class="sxs-lookup"><span data-stu-id="c0c73-157"><strong>Callee user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="c0c73-158">Ja</span><span class="sxs-lookup"><span data-stu-id="c0c73-158">Yes</span></span></p></td>
<td><p><span data-ttu-id="c0c73-159">Software, die vom Endpunkt der Person, die angerufen wurde, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c0c73-159">Software used by the endpoint of the person who was called.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0c73-160"><strong>Roundtrip (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="c0c73-160"><strong>Round trip (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="c0c73-161">Ja</span><span class="sxs-lookup"><span data-stu-id="c0c73-161">Yes</span></span></p></td>
<td><p><span data-ttu-id="c0c73-p104">Die durchschnittliche Zeit (in Millisekunden), die ein RTP-Paket (Real-time Transport Protocol) benötigt, um zu einem anderen Endpunkt und wieder zurück zu gelangen. Eine Roundtripzeit von 100 ms oder weniger gilt als akzeptable Qualität.</span><span class="sxs-lookup"><span data-stu-id="c0c73-p104">Average amount of (in milliseconds) required for a real-time transport protocol (RTP) packet to travel to another endpoint and then back. Round-trip times of 100 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="c0c73-p105">Hohe Roundtripwerte können durch internationale Anrufweiterleitung, eine falsche Routingkonfiguration oder einen überlasteten Medienserver verursacht werden. Sie führen zu Problemen bei bidirektionalen Echtzeit-Audiounterhaltungen.</span><span class="sxs-lookup"><span data-stu-id="c0c73-p105">High round-trip values can be caused by international call routing, a routing misconfiguration, or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0c73-166"><strong>Beeinträchtigung (MOS)</strong></span><span class="sxs-lookup"><span data-stu-id="c0c73-166"><strong>Degradation (MOS)</strong></span></span></p></td>
<td><p><span data-ttu-id="c0c73-167">Ja</span><span class="sxs-lookup"><span data-stu-id="c0c73-167">Yes</span></span></p></td>
<td><p><span data-ttu-id="c0c73-168">Die durchschnittliche Beeinträchtigung der Qualität, die gemäß Mean Opinion Score (MOS) während eines Anrufs auftrat.</span><span class="sxs-lookup"><span data-stu-id="c0c73-168">Average amount of mean opinion score (MOS) degradation experienced during a call.</span></span> <span data-ttu-id="c0c73-169">Die Beeinträchtigungswerte liegen zwischen 0,0 (schlecht) und 5,0 (gut).</span><span class="sxs-lookup"><span data-stu-id="c0c73-169">Degradation values can range from a low of 0.0 to a high of 5.0.</span></span> <span data-ttu-id="c0c73-170">Ein Wert von 0,5 oder weniger gilt als akzeptable Beeinträchtigung.</span><span class="sxs-lookup"><span data-stu-id="c0c73-170">A value of 0.5 or less represents acceptable degradation.</span></span> <span data-ttu-id="c0c73-171">Früher wurden Mean Opinion Scores berechnet, indem man Benutzer die Qualität eines Telefongesprächs auf einer Skala von 1 bis 5 bewerten ließ.</span><span class="sxs-lookup"><span data-stu-id="c0c73-171">Historically, mean options scores were calculated by having users rate the quality of a call on a scale of 1-to-5.</span></span> <span data-ttu-id="c0c73-172">In lync Server verwendet lync Server einen Satz von Algorithmen, um vorherzusagen, wie Benutzer einen Anruf bewertet hätten.</span><span class="sxs-lookup"><span data-stu-id="c0c73-172">In Lync Server, Lync Server uses a set of algorithms to predict how users would have rated a call.</span></span></p>
<p><span data-ttu-id="c0c73-p107">Hohe Beeinträchtigungswerte können durch Überlastung, zu geringe Bandbreite, Funknetzüberlastung oder -interferenzen oder durch einen überlasteten Medienserver oder Endpunkt verursacht werden. Eine hohe Beeinträchtigung führt zu verzerrter oder unterbrochener Sprachübertragung.</span><span class="sxs-lookup"><span data-stu-id="c0c73-p107">High degradation values can be caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server or endpoint. High degradation results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0c73-175"><strong>Paketverlust</strong></span><span class="sxs-lookup"><span data-stu-id="c0c73-175"><strong>Packet loss</strong></span></span></p></td>
<td><p><span data-ttu-id="c0c73-176">Ja</span><span class="sxs-lookup"><span data-stu-id="c0c73-176">Yes</span></span></p></td>
<td><p><span data-ttu-id="c0c73-p108">Die durchschnittliche Rate an RTP-Paketverlusten. Zu Paketverlusten kommt es, wenn RTP-Pakete (RTP ist ein Protokoll für die Übertragung von Audio und Video über das Internet) ihr Ziel nicht erreichen. Hohe Verlustraten werden allgemein durch Überlastung, zu geringe Bandbreite, Funknetzüberlastung oder -interferenzen oder durch einen überlasteten Medienserver verursacht. Paketverluste führen in der Regel zu verzerrter oder unterbrochener Sprachübertragung.</span><span class="sxs-lookup"><span data-stu-id="c0c73-p108">Average rate of RTP packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion, lack of bandwidth, wireless congestion or interference, or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0c73-180"><strong>Jitter</strong></span><span class="sxs-lookup"><span data-stu-id="c0c73-180"><strong>Jitter</strong></span></span></p></td>
<td><p><span data-ttu-id="c0c73-181">Ja</span><span class="sxs-lookup"><span data-stu-id="c0c73-181">Yes</span></span></p></td>
<td><p><span data-ttu-id="c0c73-182">Der durchschnittliche Jitter, der zwischen dem Eintreffen von RTP-Paketen ermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="c0c73-182">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="c0c73-183">(Jitter ist ein Maß für die &quot; Zittern eines &quot; Anrufs.) Starke Jitterwerte werden in der Regel durch Überlastung oder einen überladenen Medienserver verursacht, was zu verzerrten oder verlorenen Audiodaten führt.</span><span class="sxs-lookup"><span data-stu-id="c0c73-183">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0c73-184"><strong>Ausblendungsverhältnis der Reparatur</strong></span><span class="sxs-lookup"><span data-stu-id="c0c73-184"><strong>Healer concealed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="c0c73-185">Ja</span><span class="sxs-lookup"><span data-stu-id="c0c73-185">Yes</span></span></p></td>
<td><p><span data-ttu-id="c0c73-p110">Das durchschnittliche Verhältnis zwischen ausgeblendeten Audiosamples und der Gesamtzahl der Samples. (Ausgeblendete Audiosamples sind ein Verfahren zum „Glätten“ der „holprigen“ Übertragung, die normalerweise von verworfenen Netzwerkpaketen verursacht wird.) Ein hoher Wert gibt an, dass wegen Paketverlusten oder Jitters Verlustausblendung in großem Umfang angewendet wurde und führt zu verzerrter oder unterbrochener Sprachübertragung.</span><span class="sxs-lookup"><span data-stu-id="c0c73-p110">Average ratio of concealed audio samples to the total to the total number of samples. (A concealed audio sample is a technique used to smooth out the abrupt transition that would usually be caused by dropped network packets.) High values indicate significant levels of loss concealment applied caused by packet loss or jitter, and results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0c73-188"><strong>Streckungsverhältnis der Reparatur</strong></span><span class="sxs-lookup"><span data-stu-id="c0c73-188"><strong>Healer stretched ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="c0c73-189">Ja</span><span class="sxs-lookup"><span data-stu-id="c0c73-189">Yes</span></span></p></td>
<td><p><span data-ttu-id="c0c73-p111">Das durchschnittliche Verhältnis zwischen gestreckten Audiosamples und der Gesamtzahl der Samples. (Gestrecktes Audio ist ein Verfahren zum Dehnen von Audiodaten, um die Gesprächsqualität aufrechtzuerhalten, wenn ein verworfenes Netzwerkpaket festgestellt wurde.) Ein hoher Wert gibt an, dass wegen Jitters Samplestreckung in hohem Umfang aufgetreten ist und führt zu roboterhafter oder verzerrter Sprachqualität.</span><span class="sxs-lookup"><span data-stu-id="c0c73-p111">Average ratio of stretched audio samples to the total to the total number of samples. (Stretched audio is audio that has been expanded to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample stretching caused by jitter, and result in audio sounding robotic or distorted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c0c73-192"><strong>Komprimierungsverhältnis der Reparatur</strong></span><span class="sxs-lookup"><span data-stu-id="c0c73-192"><strong>Healer compressed ratio</strong></span></span></p></td>
<td><p><span data-ttu-id="c0c73-193">Ja</span><span class="sxs-lookup"><span data-stu-id="c0c73-193">Yes</span></span></p></td>
<td><p><span data-ttu-id="c0c73-p112">Das durchschnittliche Verhältnis zwischen komprimierten Audiosamples und der Gesamtzahl der Samples. (Komprimiertes Audio sind Audiodaten, die komprimiert wurden, um die Gesprächsqualität aufrechtzuerhalten, wenn ein verworfenes Netzwerkpaket festgestellt wurde.) Ein hoher Wert gibt an, dass wegen Jitters Samplekomprimierung in hohem Umfang angewendet wurde und führt zu einer zu schnellen Sprachwiedergabe oder zu verzerrter Sprachqualität.</span><span class="sxs-lookup"><span data-stu-id="c0c73-p112">Average ratio of compressed audio samples to the total number of samples. (Compressed audio is audio that has been compressed to help maintain call quality when a dropped network packet has been detected.) High values indicate significant levels of sample compression caused by jitter, and result in audio sounding accelerated or distorted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c0c73-196"><strong>Verbindung</strong></span><span class="sxs-lookup"><span data-stu-id="c0c73-196"><strong>Connectivity</strong></span></span></p></td>
<td><p><span data-ttu-id="c0c73-197">Ja</span><span class="sxs-lookup"><span data-stu-id="c0c73-197">Yes</span></span></p></td>
<td><p><span data-ttu-id="c0c73-p113">Typ einer Kommunikationsverbindung über Funk. In der Regel wird damit einer der folgenden Typen bezeichnet:</span><span class="sxs-lookup"><span data-stu-id="c0c73-p113">Type of wireless communication link. Typically, this is one of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="c0c73-200">Vermittelt</span><span class="sxs-lookup"><span data-stu-id="c0c73-200">Relay</span></span></p></li>
<li><p><span data-ttu-id="c0c73-201">Direkt</span><span class="sxs-lookup"><span data-stu-id="c0c73-201">Direct</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="c0c73-202">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c0c73-202">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

