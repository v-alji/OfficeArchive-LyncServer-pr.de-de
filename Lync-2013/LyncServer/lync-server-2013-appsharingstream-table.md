---
title: 'Lync Server 2013: AppSharingStream-Tabelle'
description: 'Lync Server 2013: AppSharingStream-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AppSharingStream table
ms:assetid: 391490cb-d7b8-44ca-b4d1-429600da909c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204808(v=OCS.15)
ms:contentKeyID: 48183852
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b530af5b489e090e5d0d00fbb01b2b950bafbe5a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440556"
---
# <a name="appsharingstream-table-in-lync-server-2013"></a><span data-ttu-id="23255-103">AppSharingStream-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="23255-103">AppSharingStream table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="23255-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="23255-104">

<span> </span></span></span>

<span data-ttu-id="23255-105">_**Letztes Änderungsdatum des Themas:** 2014-02-21_</span><span class="sxs-lookup"><span data-stu-id="23255-105">_**Topic Last Modified:** 2014-02-21_</span></span>

<span data-ttu-id="23255-106">Die AppSharingStream-Tabelle enthält die Qualität der Erfahrungswerte für die netzwerkdatenströme, die für die Anwendungsfreigabe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="23255-106">The AppSharingStream table contains Quality of Experience metrics for the network streams used for application sharing.</span></span> <span data-ttu-id="23255-107">Diese Tabelle wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="23255-107">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23255-108"><strong>Spalte</strong></span><span class="sxs-lookup"><span data-stu-id="23255-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="23255-109"><strong>Datentyp</strong></span><span class="sxs-lookup"><span data-stu-id="23255-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="23255-110"><strong>Schlüssel/Index</strong></span><span class="sxs-lookup"><span data-stu-id="23255-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="23255-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="23255-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23255-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="23255-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-113">DateTime</span><span class="sxs-lookup"><span data-stu-id="23255-113">dateTime</span></span></p></td>
<td><p><span data-ttu-id="23255-114">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="23255-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="23255-115">Das Datum und die Uhrzeit, zu der die Sitzung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-115">Date and time that the session started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="23255-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-117">int</span><span class="sxs-lookup"><span data-stu-id="23255-117">int</span></span></p></td>
<td><p><span data-ttu-id="23255-118">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="23255-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="23255-119">Sequenzielle Kennung, die verwendet wird, um zwischen Sitzungen zu unterscheiden, die am gleichen Datum und zur gleichen Zeit gestartet wurden.</span><span class="sxs-lookup"><span data-stu-id="23255-119">Sequential identifier used to distinguish between sessions that started on the same date and at the same time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="23255-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="23255-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="23255-122">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="23255-122">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="23255-123">Stellt den Typ der im Anruf verwendeten Videozeile dar.</span><span class="sxs-lookup"><span data-stu-id="23255-123">Represents the type of video line used in the call.</span></span> <span data-ttu-id="23255-124">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="23255-124">Allowed values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="23255-125">0 – Audio</span><span class="sxs-lookup"><span data-stu-id="23255-125">0 – Audio</span></span></p></li>
<li><p><span data-ttu-id="23255-126">1 – Video</span><span class="sxs-lookup"><span data-stu-id="23255-126">1 – Video</span></span></p></li>
<li><p><span data-ttu-id="23255-127">2 – Panorama Video</span><span class="sxs-lookup"><span data-stu-id="23255-127">2 – Panoramic video</span></span></p></li>
<li><p><span data-ttu-id="23255-128">3 – Anwendung/Desktop Freigabe</span><span class="sxs-lookup"><span data-stu-id="23255-128">3 –Application/Desktop Sharing</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-129"><strong>Datenstrom-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="23255-129"><strong>StreamID</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-130">int</span><span class="sxs-lookup"><span data-stu-id="23255-130">int</span></span></p></td>
<td><p><span data-ttu-id="23255-131">Primary</span><span class="sxs-lookup"><span data-stu-id="23255-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="23255-132">Eindeutiger Bezeichner des Anwendungsfreigabe Datenstroms.</span><span class="sxs-lookup"><span data-stu-id="23255-132">Unique identifier of the application sharing stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-133"><strong>JitterInterArrival</strong></span><span class="sxs-lookup"><span data-stu-id="23255-133"><strong>JitterInterArrival</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-134">int</span><span class="sxs-lookup"><span data-stu-id="23255-134">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-135">Der durchschnittliche Jitter, der zwischen dem Eintreffen von RTP-Paketen ermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-135">Average jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="23255-136">(Jitter ist ein Maß für die &quot; Zittern eines &quot; Anrufs.) Starke Jitterwerte werden in der Regel durch Überlastung oder einen überladenen Medienserver verursacht, was zu verzerrten oder verlorenen Audiodaten führt.</span><span class="sxs-lookup"><span data-stu-id="23255-136">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-137"><strong>JitterInterArrivalMax</strong></span><span class="sxs-lookup"><span data-stu-id="23255-137"><strong>JitterInterArrivalMax</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-138">int</span><span class="sxs-lookup"><span data-stu-id="23255-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-139">Maximaler Jitter zwischen den Ankünften des RTP-Pakets.</span><span class="sxs-lookup"><span data-stu-id="23255-139">Maximum jitter detected between RTP packet arrivals.</span></span> <span data-ttu-id="23255-140">(Jitter ist ein Maß für die &quot; Zittern eines &quot; Anrufs.) Starke Jitterwerte werden in der Regel durch Überlastung oder einen überladenen Medienserver verursacht, was zu verzerrten oder verlorenen Audiodaten führt.</span><span class="sxs-lookup"><span data-stu-id="23255-140">(Jitter is a measure of the &quot;shakiness&quot; of a call.) High jitter values are typically caused by congestion or an overloaded media server, and result in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-141"><strong>RoundTrip</strong></span><span class="sxs-lookup"><span data-stu-id="23255-141"><strong>RoundTrip</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-142">int</span><span class="sxs-lookup"><span data-stu-id="23255-142">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-p105">Die durchschnittliche Zeit (in Millisekunden), die ein RTP-Paket (Real-Time Transport-Protokoll) benötigt, um zu einem anderen Endpunkt und wieder zurück zu gelangen. Eine Roundtripzeit von 200 ms oder weniger gilt als akzeptable Qualität.</span><span class="sxs-lookup"><span data-stu-id="23255-p105">Average amount of (in milliseconds) required for a Real-Time Transport Protocol packet to travel to another endpoint and then back. Round-trip times of 200 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="23255-p106">Hohe Roundtripwerte können durch internationale Anrufweiterleitung, eine falsche Routingkonfiguration oder einen überlasteten Medienserver verursacht werden. Sie führen zu Problemen bei bidirektionalen Echtzeit-Audiounterhaltungen.</span><span class="sxs-lookup"><span data-stu-id="23255-p106">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-147"><strong>RoundTripMax</strong></span><span class="sxs-lookup"><span data-stu-id="23255-147"><strong>RoundTripMax</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-148">int</span><span class="sxs-lookup"><span data-stu-id="23255-148">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-149">Der Höchstbetrag (in Millisekunden), der für ein Real-Time Transport Protokoll Paket erforderlich ist, um zu einem anderen Endpunkt zu wechseln und dann zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="23255-149">Maximum amount of (in milliseconds) required for a Real-Time Transport Protocol packet to travel to another endpoint and then back.</span></span> <span data-ttu-id="23255-150">Eine Roundtripzeit von 200 ms oder weniger gilt als akzeptable Qualität.</span><span class="sxs-lookup"><span data-stu-id="23255-150">Round-trip times of 200 milliseconds or less are considered of acceptable quality.</span></span></p>
<p><span data-ttu-id="23255-p108">Hohe Roundtripwerte können durch internationale Anrufweiterleitung, eine falsche Routingkonfiguration oder einen überlasteten Medienserver verursacht werden. Sie führen zu Problemen bei bidirektionalen Echtzeit-Audiounterhaltungen.</span><span class="sxs-lookup"><span data-stu-id="23255-p108">High round-trip values can be caused by international call routing; a routing misconfiguration; or an overloaded media server. High round-trip times result in difficulties with two-way, real-time audio conversations.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-153"><strong>PacketLossRate</strong></span><span class="sxs-lookup"><span data-stu-id="23255-153"><strong>PacketLossRate</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-154">float</span><span class="sxs-lookup"><span data-stu-id="23255-154">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-p109">Die durchschnittliche Rate an RTP-Paketverlusten (Real-Time Transport-Protokoll; ein Protokoll für die Übertragung von Audio und Video über das Internet). Zu Paketverlusten kommt es, wenn RTP-Pakete ihr Ziel nicht erreichen. Hohe Verlustraten werden allgemein durch Überlastung, zu geringe Bandbreite, Funknetzüberlastung oder -interferenzen oder durch einen überlasteten Medienserver verursacht. Paketverluste führen in der Regel zu verzerrter oder unterbrochener Sprachübertragung.</span><span class="sxs-lookup"><span data-stu-id="23255-p109">Average rate of Real-Time Transport Protocol (RTP) packet loss. (Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server. Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-158"><strong>PacketLossRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="23255-158"><strong>PacketLossRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-159">float</span><span class="sxs-lookup"><span data-stu-id="23255-159">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-160">Maximale Rate des RTP-Paketverlusts (Real-Time Transport Protocol).</span><span class="sxs-lookup"><span data-stu-id="23255-160">Maximum rate of Real-Time Transport Protocol (RTP) packet loss.</span></span> <span data-ttu-id="23255-161">(Paketverlust tritt auf, wenn RTP-Pakete, ein Protokoll, das für die Übertragung von Audio und Video über das Internet verwendet wird, das Ziel nicht erreicht haben.) In der Regel sind die großen Verlustraten auf Engpässe zurückzuführen. mangelnde Bandbreite; WLAN-Überlastung oder Störungen; oder einen überladenen Medienserver.</span><span class="sxs-lookup"><span data-stu-id="23255-161">(Packet loss occurs when RTP packets, a protocol used for transmitting audio and video across the Internet, failed to reach their destination.) High loss rates are generally caused by congestion; lack of bandwidth; wireless congestion or interference; or an overloaded media server.</span></span> <span data-ttu-id="23255-162">Paketverluste führen in der Regel zu verzerrter oder unterbrochener Sprachübertragung.</span><span class="sxs-lookup"><span data-stu-id="23255-162">Packet loss typically results in distorted or lost audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-163"><strong>PacketUtilization</strong></span><span class="sxs-lookup"><span data-stu-id="23255-163"><strong>PacketUtilization</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-164">int</span><span class="sxs-lookup"><span data-stu-id="23255-164">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-165">Die Anzahl der gesendeten Pakete.</span><span class="sxs-lookup"><span data-stu-id="23255-165">Number of packets sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-166"><strong>Bandbreite</strong></span><span class="sxs-lookup"><span data-stu-id="23255-166"><strong>BandwidthEst</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-167">int</span><span class="sxs-lookup"><span data-stu-id="23255-167">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-168">Geschätzte einseitige Bandbreite, die am Ende der Sitzung zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="23255-168">Estimated one-way bandwidth available at the end of the session.</span></span> <span data-ttu-id="23255-169">In Bits pro Sekunde gemeldet.</span><span class="sxs-lookup"><span data-stu-id="23255-169">Reported in bits per second.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-170"><strong>AppSharingPayloadDescription</strong></span><span class="sxs-lookup"><span data-stu-id="23255-170"><strong>AppSharingPayloadDescription</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-171">int</span><span class="sxs-lookup"><span data-stu-id="23255-171">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-172">Beschreibung der Anwendungsfreigabe Nutzlast.</span><span class="sxs-lookup"><span data-stu-id="23255-172">Description of the application sharing payload.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-173"><strong>RelativeOneWayTotal</strong></span><span class="sxs-lookup"><span data-stu-id="23255-173"><strong>RelativeOneWayTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-174">float</span><span class="sxs-lookup"><span data-stu-id="23255-174">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-175">Gesamtzahl der unidirektionalen Latenzzeit.</span><span class="sxs-lookup"><span data-stu-id="23255-175">Total amount of one-way latency.</span></span> <span data-ttu-id="23255-176">Die relative unidirektionale Latenz misst die Verzögerung zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="23255-176">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-177"><strong>RelativeOneWayAverage</strong></span><span class="sxs-lookup"><span data-stu-id="23255-177"><strong>RelativeOneWayAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-178">float</span><span class="sxs-lookup"><span data-stu-id="23255-178">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-179">Durchschnittliche Anzahl der unidirektionalen Latenzzeit.</span><span class="sxs-lookup"><span data-stu-id="23255-179">Average amount of one-way latency.</span></span> <span data-ttu-id="23255-180">Die relative unidirektionale Latenz misst die Verzögerung zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="23255-180">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-181"><strong>RelativeOneWayMax</strong></span><span class="sxs-lookup"><span data-stu-id="23255-181"><strong>RelativeOneWayMax</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-182">float</span><span class="sxs-lookup"><span data-stu-id="23255-182">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-183">Maximale Anzahl von unidirektionalen Latenzzeiten.</span><span class="sxs-lookup"><span data-stu-id="23255-183">Maximum amount of one-way latency.</span></span> <span data-ttu-id="23255-184">Die relative unidirektionale Latenz misst die Verzögerung zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="23255-184">Relative one-way latency measures the delay between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-185"><strong>RelativeOneWayBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="23255-185"><strong>RelativeOneWayBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-186">int</span><span class="sxs-lookup"><span data-stu-id="23255-186">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-187">Gesamtzahl der einseitigen Burst-Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="23255-187">Total one-way burst occurrences.</span></span> <span data-ttu-id="23255-188">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen.</span><span class="sxs-lookup"><span data-stu-id="23255-188">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="23255-189">Diese Metrik misst den Datenfluss zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="23255-189">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-190"><strong>RelativeOneWayBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="23255-190"><strong>RelativeOneWayBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-191">float</span><span class="sxs-lookup"><span data-stu-id="23255-191">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-192">Totale unidirektionale Burst Dichte.</span><span class="sxs-lookup"><span data-stu-id="23255-192">Total one-way burst density.</span></span> <span data-ttu-id="23255-193">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen.</span><span class="sxs-lookup"><span data-stu-id="23255-193">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="23255-194">Diese Metrik misst den Datenfluss zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="23255-194">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-195"><strong>RelativeOneWayBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="23255-195"><strong>RelativeOneWayBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-196">float</span><span class="sxs-lookup"><span data-stu-id="23255-196">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-197">Gesamtdauer des einseitigen Bursts.</span><span class="sxs-lookup"><span data-stu-id="23255-197">Total one-way burst duration.</span></span> <span data-ttu-id="23255-198">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen.</span><span class="sxs-lookup"><span data-stu-id="23255-198">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span> <span data-ttu-id="23255-199">Diese Metrik misst den Datenfluss zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="23255-199">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-200"><strong>RelativeOneWayGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="23255-200"><strong>RelativeOneWayGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-201">int</span><span class="sxs-lookup"><span data-stu-id="23255-201">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-202">Gesamtanzahl der einseitigen Lücken.</span><span class="sxs-lookup"><span data-stu-id="23255-202">Total one-way gap occurrences.</span></span> <span data-ttu-id="23255-203">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen. Lücken deuten auf Verzögerungen zwischen diesen Bursts hin.</span><span class="sxs-lookup"><span data-stu-id="23255-203">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="23255-204">Diese Metrik misst den Datenfluss zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="23255-204">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-205"><strong>RelativeOneWayGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="23255-205"><strong>RelativeOneWayGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-206">float</span><span class="sxs-lookup"><span data-stu-id="23255-206">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-207">Gesamtdichte für einseitigen Abstand.</span><span class="sxs-lookup"><span data-stu-id="23255-207">Total one-way gap density.</span></span> <span data-ttu-id="23255-208">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen. Lücken deuten auf Verzögerungen zwischen diesen Bursts hin.</span><span class="sxs-lookup"><span data-stu-id="23255-208">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="23255-209">Diese Metrik misst den Datenfluss zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="23255-209">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-210"><strong>RelativeOneWayGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="23255-210"><strong>RelativeOneWayGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-211">float</span><span class="sxs-lookup"><span data-stu-id="23255-211">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-212">Gesamtdauer der einseitigen Lücke</span><span class="sxs-lookup"><span data-stu-id="23255-212">Total one-way gap duration.</span></span> <span data-ttu-id="23255-213">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen. Lücken deuten auf Verzögerungen zwischen diesen Bursts hin.</span><span class="sxs-lookup"><span data-stu-id="23255-213">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream; gaps indicate delays between these bursts.</span></span> <span data-ttu-id="23255-214">Diese Metrik misst den Datenfluss zwischen dem Client und dem Server.</span><span class="sxs-lookup"><span data-stu-id="23255-214">This metric measures data flow between the client and the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-215"><strong>ApplicationSharingType</strong></span><span class="sxs-lookup"><span data-stu-id="23255-215"><strong>ApplicationSharingType</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-216">varChar (256)</span><span class="sxs-lookup"><span data-stu-id="23255-216">varChar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-217">Anwendungsrolle (mitbenutzender oder Viewer) und Inhaltstyp.</span><span class="sxs-lookup"><span data-stu-id="23255-217">Application role (Sharer or Viewer) and content type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-218"><strong>RDPTileProcessingLatencyTotal</strong></span><span class="sxs-lookup"><span data-stu-id="23255-218"><strong>RDPTileProcessingLatencyTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-219">float</span><span class="sxs-lookup"><span data-stu-id="23255-219">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-220">Gesamtverarbeitungszeit für RDP-Kacheln (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="23255-220">Total processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="23255-221">Eine höhere Gesamtsumme entspricht einer längeren Verzögerung bei der Anzeige.</span><span class="sxs-lookup"><span data-stu-id="23255-221">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-222"><strong>RDPTileProcessingLatencyAverage</strong></span><span class="sxs-lookup"><span data-stu-id="23255-222"><strong>RDPTileProcessingLatencyAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-223">float</span><span class="sxs-lookup"><span data-stu-id="23255-223">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-224">Durchschnittliche Verarbeitungszeit für RDP-Kacheln (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="23255-224">Average processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="23255-225">Eine höhere Gesamtsumme entspricht einer längeren Verzögerung bei der Anzeige.</span><span class="sxs-lookup"><span data-stu-id="23255-225">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-226"><strong>RDPTileProcessingLatencyMax</strong></span><span class="sxs-lookup"><span data-stu-id="23255-226"><strong>RDPTileProcessingLatencyMax</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-227">float</span><span class="sxs-lookup"><span data-stu-id="23255-227">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-228">Maximale Verarbeitungszeit für RDP-Kacheln (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="23255-228">Maximum processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="23255-229">Eine höhere Gesamtsumme entspricht einer längeren Verzögerung bei der Anzeige.</span><span class="sxs-lookup"><span data-stu-id="23255-229">A higher total equates to a longer delay in the viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-230"><strong>RDPTileProcessingLatencyBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="23255-230"><strong>RDPTileProcessingLatencyBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-231">int</span><span class="sxs-lookup"><span data-stu-id="23255-231">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-232">Burst-Vorkommen in der Verarbeitungszeit für RDP-Kacheln (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="23255-232">Burst occurrences in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="23255-233">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen.</span><span class="sxs-lookup"><span data-stu-id="23255-233">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-234"><strong>RDPTileProcessingLatencyBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="23255-234"><strong>RDPTileProcessingLatencyBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-235">float</span><span class="sxs-lookup"><span data-stu-id="23255-235">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-236">Burst Dichte in der Verarbeitungszeit für RDP-Kacheln (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="23255-236">Burst density in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="23255-237">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen.</span><span class="sxs-lookup"><span data-stu-id="23255-237">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-238"><strong>RDPTileProcessingLatencyBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="23255-238"><strong>RDPTileProcessingLatencyBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-239">float</span><span class="sxs-lookup"><span data-stu-id="23255-239">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-240">Burst Dauer in der Verarbeitungszeit für RDP-Kacheln (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="23255-240">Burst duration in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="23255-241">Eine "bursty"-Übertragung ist eine Übertragung, bei der Daten in unvorhersehbaren Bursts im Gegensatz zu einem unveränderlichen Datenstrom fließen.</span><span class="sxs-lookup"><span data-stu-id="23255-241">A “bursty” transmission is a transmission where data flows in unpredictable bursts as opposed to a steady stream.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-242"><strong>RDPTileProcessingLatencyGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="23255-242"><strong>RDPTileProcessingLatencyGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-243">int</span><span class="sxs-lookup"><span data-stu-id="23255-243">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-244">Lücken Vorkommen in der Verarbeitungszeit für RDP-Kacheln (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="23255-244">Gap occurrences in the processing time for remote desktop protocol (RDP) tiles.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-245"><strong>RDPTileProcessingLatencyGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="23255-245"><strong>RDPTileProcessingLatencyGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-246">float</span><span class="sxs-lookup"><span data-stu-id="23255-246">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-247">Lücken Dichte in der Verarbeitungszeit für RDP-Kacheln (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="23255-247">Gap density in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="23255-248">Eine geringe Spalt Dichte entspricht einer besseren Anzeige Erfahrung.</span><span class="sxs-lookup"><span data-stu-id="23255-248">Low gap density equates to a better viewing experience.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-249"><strong>RDPTileProcessingLatencyGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="23255-249"><strong>RDPTileProcessingLatencyGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-250">float</span><span class="sxs-lookup"><span data-stu-id="23255-250">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-251">Lücken Dauer in der Verarbeitungszeit für RDP-Kacheln (Remote Desktop Protocol).</span><span class="sxs-lookup"><span data-stu-id="23255-251">Gap duration in the processing time for remote desktop protocol (RDP) tiles.</span></span> <span data-ttu-id="23255-252">Kurze Lücken dauern sind mit einer besseren Anzeige Erfahrung identisch.</span><span class="sxs-lookup"><span data-stu-id="23255-252">Short gap durations equate to a better viewing experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-253"><strong>CaptureTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="23255-253"><strong>CaptureTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-254">float</span><span class="sxs-lookup"><span data-stu-id="23255-254">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-255">Gesamtrate der erfassten Kacheln (in Kacheln pro Sekunde)</span><span class="sxs-lookup"><span data-stu-id="23255-255">Total rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-256"><strong>CaptureTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="23255-256"><strong>CaptureTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-257">float</span><span class="sxs-lookup"><span data-stu-id="23255-257">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-258">Durchschnittliche Rate der erfassten Kacheln (in Kacheln pro Sekunde)</span><span class="sxs-lookup"><span data-stu-id="23255-258">Average rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-259"><strong>CaptureTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="23255-259"><strong>CaptureTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-260">float</span><span class="sxs-lookup"><span data-stu-id="23255-260">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-261">Maximale Rate der erfassten Kacheln (in Kacheln pro Sekunde)</span><span class="sxs-lookup"><span data-stu-id="23255-261">Maximum rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-262"><strong>CaptureTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="23255-262"><strong>CaptureTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-263">in t</span><span class="sxs-lookup"><span data-stu-id="23255-263">in t</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-264">Burst-Vorkommen in der Rate der erfassten Kacheln (in Kacheln pro Sekunde)</span><span class="sxs-lookup"><span data-stu-id="23255-264">Burst occurrences in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-265"><strong>CaptureTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="23255-265"><strong>CaptureTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-266">float</span><span class="sxs-lookup"><span data-stu-id="23255-266">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-267">Burst Dichte in der Rate der aufgenommenen Kacheln (in Kacheln pro Sekunde)</span><span class="sxs-lookup"><span data-stu-id="23255-267">Burst density in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-268"><strong>CaptureTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="23255-268"><strong>CaptureTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-269">float</span><span class="sxs-lookup"><span data-stu-id="23255-269">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-270">Burst Dauer in der Rate der erfassten Kacheln (in Kacheln pro Sekunde)</span><span class="sxs-lookup"><span data-stu-id="23255-270">Burst duration in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-271"><strong>CaptureTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="23255-271"><strong>CaptureTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-272">int</span><span class="sxs-lookup"><span data-stu-id="23255-272">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-273">Lücken Vorkommen in der Rate der erfassten Kacheln (in Kacheln pro Sekunde)</span><span class="sxs-lookup"><span data-stu-id="23255-273">Gap occurrences in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-274"><strong>CaptureTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="23255-274"><strong>CaptureTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-275">float</span><span class="sxs-lookup"><span data-stu-id="23255-275">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-276">Spalt Dichte in der Rate der erfassten Kacheln (in Kacheln pro Sekunde)</span><span class="sxs-lookup"><span data-stu-id="23255-276">Gap density in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-277"><strong>CaptureTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="23255-277"><strong>CaptureTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-278">float</span><span class="sxs-lookup"><span data-stu-id="23255-278">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-279">Dauer der Lücke in der Rate der erfassten Kacheln (in Kacheln pro Sekunde)</span><span class="sxs-lookup"><span data-stu-id="23255-279">Gap duration in the rate of captured tiles (in tiles per second).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-280"><strong>SpoiledTilePercentTotal</strong></span><span class="sxs-lookup"><span data-stu-id="23255-280"><strong>SpoiledTilePercentTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-281">float</span><span class="sxs-lookup"><span data-stu-id="23255-281">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-282">Der Gesamtprozentsatz des Inhalts, der den Betrachter nicht erreicht hat, aber stattdessen von neuem Inhalt verworfen und überschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-282">Total percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-283"><strong>SpoiledTilePercentAverage</strong></span><span class="sxs-lookup"><span data-stu-id="23255-283"><strong>SpoiledTilePercentAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-284">float</span><span class="sxs-lookup"><span data-stu-id="23255-284">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-285">Der durchschnittliche Prozentsatz des Inhalts, der den Betrachter nicht erreicht hat, aber stattdessen von neuem Inhalt verworfen und überschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-285">Average percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-286"><strong>SpoiledTilePercentMax</strong></span><span class="sxs-lookup"><span data-stu-id="23255-286"><strong>SpoiledTilePercentMax</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-287">float</span><span class="sxs-lookup"><span data-stu-id="23255-287">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-288">Der maximale Prozentsatz des Inhalts, der den Betrachter nicht erreicht hat, aber stattdessen von neuem Inhalt verworfen und überschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-288">Maximum percentage of the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-289"><strong>SpoiledTilePercentBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="23255-289"><strong>SpoiledTilePercentBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-290">int</span><span class="sxs-lookup"><span data-stu-id="23255-290">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-291">Burst-Vorkommen für den Inhalt, der den Betrachter nicht erreicht hat, aber stattdessen von neuem Inhalt verworfen und überschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-291">Burst occurrences for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-292"><strong>SpoiledTilePercentBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="23255-292"><strong>SpoiledTilePercentBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-293">float</span><span class="sxs-lookup"><span data-stu-id="23255-293">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-294">Burst Dichte für den Inhalt, der den Betrachter nicht erreicht hat, aber stattdessen von neuem Inhalt verworfen und überschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-294">Burst density for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-295"><strong>SpoiledTilePercentBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="23255-295"><strong>SpoiledTilePercentBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-296">float</span><span class="sxs-lookup"><span data-stu-id="23255-296">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-297">Burst Dauer für den Inhalt, der den Betrachter nicht erreicht hat, aber stattdessen verworfen und durch neuen Inhalt überschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-297">Burst duration for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-298"><strong>SpoiledTilePercentGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="23255-298"><strong>SpoiledTilePercentGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-299">int</span><span class="sxs-lookup"><span data-stu-id="23255-299">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-300">Lücken auftreten für den Inhalt, der den Betrachter nicht erreicht hat, aber stattdessen von neuem Inhalt verworfen und überschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-300">Gap occurrences for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-301"><strong>SpoiledTilePercentGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="23255-301"><strong>SpoiledTilePercentGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-302">float</span><span class="sxs-lookup"><span data-stu-id="23255-302">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-303">Lücken Dichte für den Inhalt, der den Betrachter nicht erreicht hat, aber stattdessen von neuem Inhalt verworfen und überschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-303">Gap density for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-304"><strong>SpoiledTilePercentGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="23255-304"><strong>SpoiledTilePercentGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-305">float</span><span class="sxs-lookup"><span data-stu-id="23255-305">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-306">Abstands Dauer für den Inhalt, der den Betrachter nicht erreicht hat, aber stattdessen von neuem Inhalt verworfen und überschrieben wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-306">Gap duration for the content that did not reach the viewer but was instead discarded and overwritten by fresh content.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-307"><strong>ScrapingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="23255-307"><strong>ScrapingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-308">float</span><span class="sxs-lookup"><span data-stu-id="23255-308">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-309">Gesamtzahl der Frames, die aus der grafikquelle ausgekratzt wurden.</span><span class="sxs-lookup"><span data-stu-id="23255-309">Total number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-310"><strong>ScrapingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="23255-310"><strong>ScrapingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-311">float</span><span class="sxs-lookup"><span data-stu-id="23255-311">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-312">Die durchschnittliche Anzahl von Frames, die aus der grafikquelle ausgekratzt wurden.</span><span class="sxs-lookup"><span data-stu-id="23255-312">Average number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-313"><strong>ScrapingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="23255-313"><strong>ScrapingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-314">float</span><span class="sxs-lookup"><span data-stu-id="23255-314">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-315">Die maximale Anzahl von Frames, die aus der grafikquelle ausgekratzt wurden.</span><span class="sxs-lookup"><span data-stu-id="23255-315">Maximum number of frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-316"><strong>ScrapingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="23255-316"><strong>ScrapingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-317">int</span><span class="sxs-lookup"><span data-stu-id="23255-317">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-318">Burst-Vorkommen in den Frames, die aus der grafikquelle ausgekratzt wurden.</span><span class="sxs-lookup"><span data-stu-id="23255-318">Burst occurrences in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-319"><strong>ScrapingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="23255-319"><strong>ScrapingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-320">float</span><span class="sxs-lookup"><span data-stu-id="23255-320">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-321">Burst Dichte in den Frames, die aus der grafikquelle ausgekratzt wurden.</span><span class="sxs-lookup"><span data-stu-id="23255-321">Burst density in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-322"><strong>ScrapingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="23255-322"><strong>ScrapingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-323">float</span><span class="sxs-lookup"><span data-stu-id="23255-323">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-324">Burst Dauer in den Frames, die aus der grafikquelle ausgekratzt wurden.</span><span class="sxs-lookup"><span data-stu-id="23255-324">Burst duration in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-325"><strong>ScrapingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="23255-325"><strong>ScrapingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-326">int</span><span class="sxs-lookup"><span data-stu-id="23255-326">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-327">Lücken Vorkommen in den Frames, die aus der grafikquelle ausgekratzt wurden.</span><span class="sxs-lookup"><span data-stu-id="23255-327">Gap occurrences in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-328"><strong>ScrapingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="23255-328"><strong>ScrapingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-329">float</span><span class="sxs-lookup"><span data-stu-id="23255-329">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-330">Spalt Dichte in den Frames, die aus der grafikquelle ausgekratzt wurden.</span><span class="sxs-lookup"><span data-stu-id="23255-330">Gap density in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-331"><strong>ScrapingFrameRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="23255-331"><strong>ScrapingFrameRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-332">float</span><span class="sxs-lookup"><span data-stu-id="23255-332">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-333">Lücken Dauer in den Frames, die aus der grafikquelle ausgekratzt wurden.</span><span class="sxs-lookup"><span data-stu-id="23255-333">Gap duration in the frames scraped from the graphics source.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-334"><strong>IncomingTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="23255-334"><strong>IncomingTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-335">float</span><span class="sxs-lookup"><span data-stu-id="23255-335">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-336">Gesamtzahl der eingehenden Bilder, wie Sie vom Betrachter empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="23255-336">Total incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-337"><strong>IncomingTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="23255-337"><strong>IncomingTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-338">float</span><span class="sxs-lookup"><span data-stu-id="23255-338">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-339">Durchschnittliche eingehende Frame-Rate, wie Sie vom Betrachter empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-339">Average incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-340"><strong>IncomingTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="23255-340"><strong>IncomingTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-341">float</span><span class="sxs-lookup"><span data-stu-id="23255-341">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-342">Die maximale eingehende Kachel Rate, wie Sie vom Betrachter empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-342">Maximum incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-343"><strong>IncomingTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="23255-343"><strong>IncomingTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-344">int</span><span class="sxs-lookup"><span data-stu-id="23255-344">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-345">Burst-Vorkommen in der eingehenden Kachel Rate, wie Sie vom Betrachter empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="23255-345">Burst occurrences in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-346"><strong>IncomingTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="23255-346"><strong>IncomingTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-347">float</span><span class="sxs-lookup"><span data-stu-id="23255-347">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-348">Burst Dichte in der eingehenden Kachel Rate, wie Sie vom Betrachter empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-348">Burst density in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-349"><strong>IncomingTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="23255-349"><strong>IncomingTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-350">float</span><span class="sxs-lookup"><span data-stu-id="23255-350">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-351">Burst Dauer in der eingehenden Kachel Rate, wie Sie vom Betrachter empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-351">Burst duration in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-352"><strong>IncomingTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="23255-352"><strong>IncomingTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-353">int</span><span class="sxs-lookup"><span data-stu-id="23255-353">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-354">Lücken Vorkommen in der eingehenden Kachel Rate, wie Sie vom Betrachter empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="23255-354">Gap occurrences in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-355"><strong>IncomingTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="23255-355"><strong>IncomingTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-356">float</span><span class="sxs-lookup"><span data-stu-id="23255-356">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-357">Abstands Dichte in der eingehenden Kachel Rate, wie Sie vom Betrachter empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-357">Gap density in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-358"><strong>IncomingTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="23255-358"><strong>IncomingTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-359">float</span><span class="sxs-lookup"><span data-stu-id="23255-359">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-360">Lücken Dauer in der eingehenden Kachel Rate, wie Sie vom Betrachter empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-360">Gap duration in the incoming tile rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-361"><strong>IncomingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="23255-361"><strong>IncomingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-362">float</span><span class="sxs-lookup"><span data-stu-id="23255-362">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-363">Gesamtzahl der eingehenden Bilder, wie Sie vom Betrachter empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="23255-363">Total incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-364"><strong>IncomingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="23255-364"><strong>IncomingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-365">float</span><span class="sxs-lookup"><span data-stu-id="23255-365">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-366">Durchschnittliche eingehende Frame-Rate, wie Sie vom Betrachter empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-366">Average incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-367"><strong>IncomingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="23255-367"><strong>IncomingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-368">float</span><span class="sxs-lookup"><span data-stu-id="23255-368">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-369">Die maximale eingehende Frame-Rate, wie Sie vom Betrachter empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-369">Maximum incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-370"><strong>IncomingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="23255-370"><strong>IncomingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-371">int</span><span class="sxs-lookup"><span data-stu-id="23255-371">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-372">Burst-Vorkommen in der eingehenden Framerate, wie Sie vom Betrachter empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="23255-372">Burst occurrences in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-373"><strong>IncomingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="23255-373"><strong>IncomingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-374">float</span><span class="sxs-lookup"><span data-stu-id="23255-374">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-375">Burst Dichte in der eingehenden Framerate, wie Sie vom Betrachter empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-375">Burst density in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-376"><strong>IncomingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="23255-376"><strong>IncomingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-377">float</span><span class="sxs-lookup"><span data-stu-id="23255-377">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-378">Burst Dauer in der eingehenden Framerate, wie Sie vom Betrachter empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-378">Burst duration in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-379"><strong>IncomingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="23255-379"><strong>IncomingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-380">int</span><span class="sxs-lookup"><span data-stu-id="23255-380">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-381">Lücken Vorkommen in der eingehenden Framerate, wie Sie vom Betrachter empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="23255-381">Gap occurrences in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-382"><strong>IncomingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="23255-382"><strong>IncomingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-383">float</span><span class="sxs-lookup"><span data-stu-id="23255-383">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-384">Abstands Dichte in der eingehenden Framerate, wie Sie vom Betrachter empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-384">Gap density in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-385"><strong>IncomingFrameRateDuration</strong></span><span class="sxs-lookup"><span data-stu-id="23255-385"><strong>IncomingFrameRateDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-386">float</span><span class="sxs-lookup"><span data-stu-id="23255-386">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-387">Die Unterbrechungsdauer in der eingehenden Framerate, wie Sie vom Betrachter empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="23255-387">Gap duration in the incoming frame rate as received by the viewer.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-388"><strong>OutgoingTileRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="23255-388"><strong>OutgoingTileRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-389">float</span><span class="sxs-lookup"><span data-stu-id="23255-389">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-390">Gesamtanzahl der ausgehenden Kacheln für den Absender.</span><span class="sxs-lookup"><span data-stu-id="23255-390">Total outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-391"><strong>OutgoingTileRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="23255-391"><strong>OutgoingTileRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-392">float</span><span class="sxs-lookup"><span data-stu-id="23255-392">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-393">Durchschnittliche Ausgangs Kachel Rate für den Absender.</span><span class="sxs-lookup"><span data-stu-id="23255-393">Average outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-394"><strong>OutgoingTileRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="23255-394"><strong>OutgoingTileRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-395">float</span><span class="sxs-lookup"><span data-stu-id="23255-395">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-396">Maximale Anzahl der ausgehenden Kacheln für den Absender.</span><span class="sxs-lookup"><span data-stu-id="23255-396">Maximum outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-397"><strong>OutgoingTileRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="23255-397"><strong>OutgoingTileRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-398">int</span><span class="sxs-lookup"><span data-stu-id="23255-398">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-399">Burst-Vorkommen in der ausgehenden Kachel Rate für den Absender.</span><span class="sxs-lookup"><span data-stu-id="23255-399">Burst occurrences in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-400"><strong>OutgoingTileRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="23255-400"><strong>OutgoingTileRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-401">float</span><span class="sxs-lookup"><span data-stu-id="23255-401">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-402">Burst Dichte in der ausgehenden Kachel Rate für den Absender.</span><span class="sxs-lookup"><span data-stu-id="23255-402">Burst density in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-403"><strong>OutgoingTileRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="23255-403"><strong>OutgoingTileRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-404">float</span><span class="sxs-lookup"><span data-stu-id="23255-404">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-405">Burst Dauer in der ausgehenden Kachel Rate für den Absender.</span><span class="sxs-lookup"><span data-stu-id="23255-405">Burst duration in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-406"><strong>OutgoingTileRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="23255-406"><strong>OutgoingTileRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-407">int</span><span class="sxs-lookup"><span data-stu-id="23255-407">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-408">Lücken Vorkommen in der ausgehenden Kachel Rate für den Absender.</span><span class="sxs-lookup"><span data-stu-id="23255-408">Gap occurrences in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-409"><strong>OutgoingTileRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="23255-409"><strong>OutgoingTileRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-410">float</span><span class="sxs-lookup"><span data-stu-id="23255-410">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-411">Abstands Dichte in der ausgehenden Kachel Rate für den Absender.</span><span class="sxs-lookup"><span data-stu-id="23255-411">Gap density in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-412"><strong>OutgoingTileRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="23255-412"><strong>OutgoingTileRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-413">float</span><span class="sxs-lookup"><span data-stu-id="23255-413">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-414">Abstands Dauer in der ausgehenden Kachel Rate für den Absender.</span><span class="sxs-lookup"><span data-stu-id="23255-414">Gap duration in the outgoing tile rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-415"><strong>OutgoingFrameRateTotal</strong></span><span class="sxs-lookup"><span data-stu-id="23255-415"><strong>OutgoingFrameRateTotal</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-416">float</span><span class="sxs-lookup"><span data-stu-id="23255-416">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-417">Die gesamte Ausgangsbildrate für den Absender.</span><span class="sxs-lookup"><span data-stu-id="23255-417">Total outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-418"><strong>OutgoingFrameRateAverage</strong></span><span class="sxs-lookup"><span data-stu-id="23255-418"><strong>OutgoingFrameRateAverage</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-419">float</span><span class="sxs-lookup"><span data-stu-id="23255-419">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-420">durchschnittliche Ausgangsbildrate für den Absender.</span><span class="sxs-lookup"><span data-stu-id="23255-420">average outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-421"><strong>OutgoingFrameRateMax</strong></span><span class="sxs-lookup"><span data-stu-id="23255-421"><strong>OutgoingFrameRateMax</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-422">float</span><span class="sxs-lookup"><span data-stu-id="23255-422">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-423">Maximale Ausgangsbildrate für den Absender.</span><span class="sxs-lookup"><span data-stu-id="23255-423">Maximum outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-424"><strong>OutgoingFrameRateBurstOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="23255-424"><strong>OutgoingFrameRateBurstOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-425">int</span><span class="sxs-lookup"><span data-stu-id="23255-425">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-426">Burst-Vorkommen in der Ausgangsbildrate für den Absender.</span><span class="sxs-lookup"><span data-stu-id="23255-426">Burst occurrences in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-427"><strong>OutgoingFrameRateBurstDensity</strong></span><span class="sxs-lookup"><span data-stu-id="23255-427"><strong>OutgoingFrameRateBurstDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-428">float</span><span class="sxs-lookup"><span data-stu-id="23255-428">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-429">Burst Dichte in der Ausgangsbildrate für den Absender.</span><span class="sxs-lookup"><span data-stu-id="23255-429">Burst density in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-430"><strong>OutgoingFrameRateBurstDuration</strong></span><span class="sxs-lookup"><span data-stu-id="23255-430"><strong>OutgoingFrameRateBurstDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-431">float</span><span class="sxs-lookup"><span data-stu-id="23255-431">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-432">Burst Dauer in der Ausgangsbildrate für den Absender.</span><span class="sxs-lookup"><span data-stu-id="23255-432">Burst duration in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-433"><strong>OutgoingFrameRateGapOccurrences</strong></span><span class="sxs-lookup"><span data-stu-id="23255-433"><strong>OutgoingFrameRateGapOccurrences</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-434">int</span><span class="sxs-lookup"><span data-stu-id="23255-434">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-435">Lücken Vorkommen in der ausgehenden Framerate für den Absender.</span><span class="sxs-lookup"><span data-stu-id="23255-435">Gap occurrences in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-436"><strong>OutgoingFrameRateGapDensity</strong></span><span class="sxs-lookup"><span data-stu-id="23255-436"><strong>OutgoingFrameRateGapDensity</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-437">float</span><span class="sxs-lookup"><span data-stu-id="23255-437">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-438">Abstands Dichte in der Ausgangsbildrate für den Absender.</span><span class="sxs-lookup"><span data-stu-id="23255-438">Gap density in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-439"><strong>OutgoingFrameRateGapDuration</strong></span><span class="sxs-lookup"><span data-stu-id="23255-439"><strong>OutgoingFrameRateGapDuration</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-440">float</span><span class="sxs-lookup"><span data-stu-id="23255-440">float</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-441">Lücken Dauer in der ausgehenden Framerate für den Absender.</span><span class="sxs-lookup"><span data-stu-id="23255-441">Gap duration in the outgoing frame rate for the sender.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-442"><strong>AverageRectangleHeight</strong></span><span class="sxs-lookup"><span data-stu-id="23255-442"><strong>AverageRectangleHeight</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-443">int</span><span class="sxs-lookup"><span data-stu-id="23255-443">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-444">Durchschnittliche Höhe der Videoauflösung in Pixeln.</span><span class="sxs-lookup"><span data-stu-id="23255-444">Average video resolution height, in pixels.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-445"><strong>AverageRectangleWidth</strong></span><span class="sxs-lookup"><span data-stu-id="23255-445"><strong>AverageRectangleWidth</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-446">int</span><span class="sxs-lookup"><span data-stu-id="23255-446">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-447">Durchschnittliche Breite der Videoauflösung in Pixeln.</span><span class="sxs-lookup"><span data-stu-id="23255-447">Average video resolution width, in pixels.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-448"><strong>Inbound</strong></span><span class="sxs-lookup"><span data-stu-id="23255-448"><strong>Inbound</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-449">bit</span><span class="sxs-lookup"><span data-stu-id="23255-449">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-450">Durchschnittliche Bildwiederholrate (in Frames pro Sekunde) für eingehende Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="23255-450">Average frame rate (in frames per second) for inbound transmissions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23255-451"><strong>Ausgehend</strong></span><span class="sxs-lookup"><span data-stu-id="23255-451"><strong>Outbound</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-452">bit</span><span class="sxs-lookup"><span data-stu-id="23255-452">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-453">Durchschnittliche Bildwiederholrate (in Frames pro Sekunde) für ausgehende Übertragungen.</span><span class="sxs-lookup"><span data-stu-id="23255-453">Average frame rate (in frames per second) for outbound transmissions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23255-454"><strong>SenderIsCallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="23255-454"><strong>SenderIsCallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="23255-455">bit</span><span class="sxs-lookup"><span data-stu-id="23255-455">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="23255-456">1 bedeutet, dass die Datenstrom Richtung vom Aufrufer zu aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="23255-456">1 means the stream direction is from the caller to callee.</span></span></p>
<p><span data-ttu-id="23255-457">0 bedeutet, dass die Datenstrom Richtung vom aufgerufenen zum Aufrufer ist.</span><span class="sxs-lookup"><span data-stu-id="23255-457">0 means the stream direction is from the callee to the caller.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="23255-458">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="23255-458">


</div>

<span> </span>

</div>

</div>

</span></span></div>

