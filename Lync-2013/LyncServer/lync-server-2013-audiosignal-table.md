---
title: 'Lync Server 2013: AudioSignal-Tabelle'
description: 'Lync Server 2013: AudioSignal-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioSignal table
ms:assetid: 0013c8c6-cdf9-4d70-bc2a-cddd1560f66b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398064(v=OCS.15)
ms:contentKeyID: 48183217
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82f3b3119eaccfe56c4706cff07469bc3434461f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438206"
---
# <a name="audiosignal-table-in-lync-server-2013"></a><span data-ttu-id="7da0b-103">AudioSignal-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7da0b-103">AudioSignal table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7da0b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7da0b-104">

<span> </span></span></span>

<span data-ttu-id="7da0b-105">_**Letztes Änderungsdatum des Themas:** 2013-11-12_</span><span class="sxs-lookup"><span data-stu-id="7da0b-105">_**Topic Last Modified:** 2013-11-12_</span></span>

<span data-ttu-id="7da0b-106">Jeder Datensatz stellt die Metriken des Audiosignals für einen Endpunkt dar.</span><span class="sxs-lookup"><span data-stu-id="7da0b-106">Each record represents audio signal metrics for one endpoint.</span></span> <span data-ttu-id="7da0b-107">In der Regel hat jeder Anruf zwei Datensätze, einer für den Anrufer und einer für den aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="7da0b-107">Usually, each call has two records, one is for caller, and one is for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7da0b-108"><strong>Spalte</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="7da0b-109"><strong>Datentyp</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="7da0b-110"><strong>Schlüssel/Index</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="7da0b-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7da0b-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-113">datetime</span><span class="sxs-lookup"><span data-stu-id="7da0b-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="7da0b-114">Primary</span><span class="sxs-lookup"><span data-stu-id="7da0b-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="7da0b-115">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7da0b-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da0b-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-117">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-117">int</span></span></p></td>
<td><p><span data-ttu-id="7da0b-118">Primary</span><span class="sxs-lookup"><span data-stu-id="7da0b-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="7da0b-119">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7da0b-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da0b-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="7da0b-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="7da0b-122">Primary</span><span class="sxs-lookup"><span data-stu-id="7da0b-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="7da0b-123">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="7da0b-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da0b-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-125">bit</span><span class="sxs-lookup"><span data-stu-id="7da0b-125">bit</span></span></p></td>
<td><p><span data-ttu-id="7da0b-126">Primary</span><span class="sxs-lookup"><span data-stu-id="7da0b-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="7da0b-127">0: Daten des angerufenen</span><span class="sxs-lookup"><span data-stu-id="7da0b-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="7da0b-128">1: Daten des Anrufers</span><span class="sxs-lookup"><span data-stu-id="7da0b-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da0b-129"><strong>SendSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-129"><strong>SendSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-130">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-130">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7da0b-131">Stellt den Pegel des Audiosignals nach analoger Gain-Steuerung dar.</span><span class="sxs-lookup"><span data-stu-id="7da0b-131">Represents the Post-Analog Gain Control audio signal level.</span></span> <span data-ttu-id="7da0b-132">Die Einheit für diese Metrik lautet dBmo.</span><span class="sxs-lookup"><span data-stu-id="7da0b-132">The unit for this metric is dBmo.</span></span> <span data-ttu-id="7da0b-133">Für akzeptable Qualität sollte es mindestens 30 dBmo.</span><span class="sxs-lookup"><span data-stu-id="7da0b-133">For acceptable quality, it should be at least 30 dBmo.</span></span> <span data-ttu-id="7da0b-134">Diese Metrik wird vom A/V-Konferenz Server oder von IP-Telefonen nicht gemeldet.</span><span class="sxs-lookup"><span data-stu-id="7da0b-134">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da0b-135"><strong>RecvSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-135"><strong>RecvSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-136">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-136">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7da0b-137">Siehe SendSignalLevel.</span><span class="sxs-lookup"><span data-stu-id="7da0b-137">See SendSignalLevel.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da0b-138"><strong>SendNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-138"><strong>SendNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-139">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-139">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7da0b-140">Stellt den Audio-Rauschpegel nach analoger Gain-Steuerung dar.</span><span class="sxs-lookup"><span data-stu-id="7da0b-140">Represents the Post-Analog Gain Control audio noise level.</span></span> <span data-ttu-id="7da0b-141">Die Einheit für diese Metrik lautet dBmo.</span><span class="sxs-lookup"><span data-stu-id="7da0b-141">The unit for this metric is dBmo.</span></span> <span data-ttu-id="7da0b-142">Für akzeptable Qualität sollte es weniger als 35 dBmo.</span><span class="sxs-lookup"><span data-stu-id="7da0b-142">For acceptable quality, it should be less than 35 dBmo.</span></span> <span data-ttu-id="7da0b-143">Diese Metrik wird vom A/V-Konferenz Server oder von IP-Telefonen nicht gemeldet.</span><span class="sxs-lookup"><span data-stu-id="7da0b-143">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da0b-144"><strong>RecvNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-144"><strong>RecvNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-145">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-145">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7da0b-146">Siehe SendNoiseLevel.</span><span class="sxs-lookup"><span data-stu-id="7da0b-146">See SendNoiseLevel.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da0b-147"><strong>EchoReturn</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-147"><strong>EchoReturn</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-148">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-148">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7da0b-149">Verbesserungs Metrik für ECHO-Rückerstattungs Verluste.</span><span class="sxs-lookup"><span data-stu-id="7da0b-149">Echo Return Loss Enhancement metric.</span></span> <span data-ttu-id="7da0b-150">Die Einheit für diese Metrik ist DB.</span><span class="sxs-lookup"><span data-stu-id="7da0b-150">The unit for this metric is dB.</span></span> <span data-ttu-id="7da0b-151">Niedrigere Werte stellen weniger Echo dar.</span><span class="sxs-lookup"><span data-stu-id="7da0b-151">Lower values represent less echo.</span></span> <span data-ttu-id="7da0b-152">Diese Metrik wird vom A/V-Konferenz Server oder von IP-Telefonen nicht gemeldet.</span><span class="sxs-lookup"><span data-stu-id="7da0b-152">This metric is not reported by the A/V Conferencing Server or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da0b-153"><strong>AudioSpeakerGlitchRate</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-153"><strong>AudioSpeakerGlitchRate</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-154">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-154">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7da0b-155">Durchschnittliche Störimpulse pro fünf Minuten für die Lautsprecher-Wiedergabe.</span><span class="sxs-lookup"><span data-stu-id="7da0b-155">Average glitches per five minutes for the loudspeaker rendering.</span></span> <span data-ttu-id="7da0b-156">Für eine gute Qualität sollte dies weniger als eins pro fünf Minuten sein.</span><span class="sxs-lookup"><span data-stu-id="7da0b-156">For good quality, this should be less than one per five minutes.</span></span> <span data-ttu-id="7da0b-157">Nicht von A/V-Konferenzservern, Vermittlungsservern oder IP-Telefonen gemeldet.</span><span class="sxs-lookup"><span data-stu-id="7da0b-157">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da0b-158"><strong>AudioMicGlitchRate</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-158"><strong>AudioMicGlitchRate</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-159">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-159">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7da0b-160">Durchschnittliche Störimpulse pro fünf Minuten für die Aufnahme des Mikrofons.</span><span class="sxs-lookup"><span data-stu-id="7da0b-160">Average glitches per five minutes for the microphone capture.</span></span> <span data-ttu-id="7da0b-161">Für eine gute Qualität sollte dies weniger als eine pro fünf Minuten sein.</span><span class="sxs-lookup"><span data-stu-id="7da0b-161">For good quality this should be less than one per five minutes.</span></span> <span data-ttu-id="7da0b-162">Nicht von A/V-Konferenzservern, Vermittlungsservern oder IP-Telefonen gemeldet.</span><span class="sxs-lookup"><span data-stu-id="7da0b-162">Not reported by A/V Conferencing Servers, Mediation Servers, or IP phones.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da0b-163"><strong>AudioTimestampDriftRateMic</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-163"><strong>AudioTimestampDriftRateMic</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-164">Dezimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="7da0b-164">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7da0b-165">Clock-Drift Rate des Mikrofon Geräts relativ zur CPU-Uhr.</span><span class="sxs-lookup"><span data-stu-id="7da0b-165">Microphone device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da0b-166"><strong>AudioTimestampDriftRateSpk</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-166"><strong>AudioTimestampDriftRateSpk</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-167">Dezimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="7da0b-167">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7da0b-168">Clock-Drift Rate des Lautsprecher Geräts relativ zur CPU-Uhr.</span><span class="sxs-lookup"><span data-stu-id="7da0b-168">Speaker device clock drift rate, relative to CPU clock.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da0b-169"><strong>AudioTimestampErrorMicMs</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-169"><strong>AudioTimestampErrorMicMs</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-170">Dezimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="7da0b-170">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7da0b-171">Clock-Drift Rate des Lautsprecher Geräts relativ zur CPU-Uhr.</span><span class="sxs-lookup"><span data-stu-id="7da0b-171">Speaker device clock drift rate, relative to CPU clock.</span></span></p>
<p><span data-ttu-id="7da0b-172">Durchschnittlicher Zeitstempel des Mikrofon-Datenstroms in Millisekunden in den letzten 20 Sekunden des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="7da0b-172">Average microphone capture stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da0b-173"><strong>AudioTimestampErrorSpkMs</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-173"><strong>AudioTimestampErrorSpkMs</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-174">Dezimal (9; 2)</span><span class="sxs-lookup"><span data-stu-id="7da0b-174">decimal(9,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7da0b-175">Durchschnittlicher Render-Datenstrom-Zeitstempel Fehler in Millisekunden in den letzten 20 Sekunden des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="7da0b-175">Average speaker render stream time stamp error, in milliseconds, in the last 20 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da0b-176"><strong>VsEntryCauses</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-176"><strong>VsEntryCauses</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-177">smallint</span><span class="sxs-lookup"><span data-stu-id="7da0b-177">smallint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7da0b-178">Voice-Switch ist ein Halbduplex-Modus mit verminderter Unterbrechungs Fähigkeit.</span><span class="sxs-lookup"><span data-stu-id="7da0b-178">Voice switch is a half-duplex mode with reduced interruption ability.</span></span> <span data-ttu-id="7da0b-179">Ursachen für den Sprachwechsel Eintrag:</span><span class="sxs-lookup"><span data-stu-id="7da0b-179">Causes of voice switch entry:</span></span></p>
<p><span data-ttu-id="7da0b-180">ENTER_VS_BADTS 0x01</span><span class="sxs-lookup"><span data-stu-id="7da0b-180">ENTER_VS_BADTS 0x01</span></span></p>
<p><span data-ttu-id="7da0b-181">ENTER_VS_ECHO 0x02</span><span class="sxs-lookup"><span data-stu-id="7da0b-181">ENTER_VS_ECHO 0x02</span></span></p>
<p><span data-ttu-id="7da0b-182">ENTER_VS_FORCEORCONVERGENCE 0x04</span><span class="sxs-lookup"><span data-stu-id="7da0b-182">ENTER_VS_FORCEORCONVERGENCE 0x04</span></span></p>
<p><span data-ttu-id="7da0b-183">ENTER_VS_DNLP 0x08</span><span class="sxs-lookup"><span data-stu-id="7da0b-183">ENTER_VS_DNLP 0x08</span></span></p>
<p><span data-ttu-id="7da0b-184">Die Ursache kann eine Kombination dieser einzelnen Ursachen sein.</span><span class="sxs-lookup"><span data-stu-id="7da0b-184">The cause can be a combination of those individual causes.</span></span> <span data-ttu-id="7da0b-185">ENTER_VS_FORCEORCONVERGENCE können nur von der Registrierungsschlüssel für Testzwecke aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="7da0b-185">ENTER_VS_FORCEORCONVERGENCE can only be enabled by regkey for test purpose.</span></span></p>
<p><span data-ttu-id="7da0b-186">Der Datentyp für diese Spalte wurde in Microsoft lync Server 2013 geändert.</span><span class="sxs-lookup"><span data-stu-id="7da0b-186">The data type for this column was changed in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da0b-187"><strong>EchoEventCauses</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-187"><strong>EchoEventCauses</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-188">tinyint</span><span class="sxs-lookup"><span data-stu-id="7da0b-188">tinyint</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7da0b-189">Ursachen für ein Echo-Ereignis:</span><span class="sxs-lookup"><span data-stu-id="7da0b-189">Causes of an echo event:</span></span></p>
<p><span data-ttu-id="7da0b-190">ECHO_EVENT_BAD_TIMESTAMP 0x01</span><span class="sxs-lookup"><span data-stu-id="7da0b-190">ECHO_EVENT_BAD_TIMESTAMP 0x01</span></span></p>
<p><span data-ttu-id="7da0b-191">ECHO_EVENT_POSTAEC_ECHO 0x02</span><span class="sxs-lookup"><span data-stu-id="7da0b-191">ECHO_EVENT_POSTAEC_ECHO 0x02</span></span></p>
<p><span data-ttu-id="7da0b-192">ECHO_EVENT_ANLP 0x04</span><span class="sxs-lookup"><span data-stu-id="7da0b-192">ECHO_EVENT_ANLP 0x04</span></span></p>
<p><span data-ttu-id="7da0b-193">ECHO_EVENT_DNLP 0x08</span><span class="sxs-lookup"><span data-stu-id="7da0b-193">ECHO_EVENT_DNLP 0x08</span></span></p>
<p><span data-ttu-id="7da0b-194">ECHO_EVENT_MIC_CLIPPING 0x10</span><span class="sxs-lookup"><span data-stu-id="7da0b-194">ECHO_EVENT_MIC_CLIPPING 0x10</span></span></p>
<p><span data-ttu-id="7da0b-195">ECHO_EVENT_BAD_STATE 0x20</span><span class="sxs-lookup"><span data-stu-id="7da0b-195">ECHO_EVENT_BAD_STATE 0x20</span></span></p>
<p><span data-ttu-id="7da0b-196">Die Ursache kann eine Kombination dieser einzelnen Ursachen sein.</span><span class="sxs-lookup"><span data-stu-id="7da0b-196">The cause can be a combination of those individual causes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da0b-197"><strong>EchoPercentMicIn</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-197"><strong>EchoPercentMicIn</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-198">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="7da0b-198">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7da0b-p109">Prozentsatz der Zeit, in der im Mikrofonaufnahme-Datenstrom Echo festgestellt wurde. In der Regel weisen Headsets oder Hörer niedrige Werte und Freisprechvorrichtungen oder eigenständige Lautsprecher höhere Werte auf. Bei Geräten, die eine integrierte akustische Echounterdrückung unterstützen, weisen hohe Werte auf eine Echoausbreitung hin. Für andere Geräte sollte diese Metrik nicht verwendet werden, um die Gerätequalität zu evaluieren.</span><span class="sxs-lookup"><span data-stu-id="7da0b-p109">Percentage of time when echo was detected in the microphone capture stream. Typically, values are low for headsets or handsets, and higher for speaker phones or stand-alone speakers. For devices that support on-board acoustic echo cancellation, high values indicate echo leak. For other devices, this metric should not be used to evaluate device quality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da0b-203"><strong>EchoPercentSend</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-203"><strong>EchoPercentSend</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-204">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="7da0b-204">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7da0b-205">Prozentsatz der Zeit, zu der Echo in gesendetem Datenstrom erkannt wird.</span><span class="sxs-lookup"><span data-stu-id="7da0b-205">Percentage of time when echo is detected in sent stream.</span></span> <span data-ttu-id="7da0b-206">Ein großer Prozentsatz des Echos in Send-Streams zeigt einen Hinweis auf Echo Verluste.</span><span class="sxs-lookup"><span data-stu-id="7da0b-206">High echo percentage in send streams an indication of echo leak.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da0b-207"><strong>RxAGCSignalLevel</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-207"><strong>RxAGCSignalLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-208">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-208">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7da0b-209">Empfangene Signalstufe auf dem Vermittlungs Server vom Gateway; Dies gilt nur für den Vermittlungs Server.</span><span class="sxs-lookup"><span data-stu-id="7da0b-209">Received signal level on the Mediation Server from the Gateway; this applies only to the Mediation Server.</span></span> <span data-ttu-id="7da0b-210">Die Einheit dieser Metrik ist dBoV.</span><span class="sxs-lookup"><span data-stu-id="7da0b-210">The unit of this metric is dBoV.</span></span> <span data-ttu-id="7da0b-211">Für eine gute Qualität sollte der zulässige Bereich [-30 bis-18] dBoV sein.</span><span class="sxs-lookup"><span data-stu-id="7da0b-211">For good quality, the acceptable range should be [-30 to -18] dBoV.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da0b-212"><strong>RxAGCNoiseLevel</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-212"><strong>RxAGCNoiseLevel</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-213">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-213">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7da0b-214">Empfangene Signalstufe auf dem Vermittlungs Server vom Gateway.</span><span class="sxs-lookup"><span data-stu-id="7da0b-214">Received signal level on the Mediation Server from the Gateway.</span></span> <span data-ttu-id="7da0b-215">Dies gilt nur für den Vermittlungs Server.</span><span class="sxs-lookup"><span data-stu-id="7da0b-215">This applies only to the Mediation Server.</span></span> <span data-ttu-id="7da0b-216">Die Einheit dieser Metrik ist dBoV.</span><span class="sxs-lookup"><span data-stu-id="7da0b-216">The unit of this metric is dBoV.</span></span> <span data-ttu-id="7da0b-217">Für eine gute Qualität sollte der zulässige Bereich kleiner als-50 dBoV sein.</span><span class="sxs-lookup"><span data-stu-id="7da0b-217">For good quality, the acceptable range should be less than -50 dBoV.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da0b-218"><strong>RxAvgAGCGain</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-218"><strong>RxAvgAGCGain</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-219">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-219">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7da0b-220">Automatische Gain-Steuerung (AGC) auf der Mediation Server-Seite.</span><span class="sxs-lookup"><span data-stu-id="7da0b-220">Automatic gain control (AGC) on the Mediation Server side.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da0b-221"><strong>InitialSignalLevelRMS</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-221"><strong>InitialSignalLevelRMS</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-222">float</span><span class="sxs-lookup"><span data-stu-id="7da0b-222">float</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="7da0b-223">Das Stamm mittelquadrat (RMS) des eingehenden Signals von bis zu den ersten 30 Sekunden des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="7da0b-223">The root mean square (RMS) of the incoming signal of up to the first 30 seconds of the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da0b-224"><strong>RecvSignalLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-224"><strong>RecvSignalLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-225">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-225">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7da0b-226">Signal Pegel, wie er auf Kanal 1 empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="7da0b-226">Signal level as received on channel 1.</span></span></p>
<p><span data-ttu-id="7da0b-227">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7da0b-227">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da0b-228"><strong>RecvSignalLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-228"><strong>RecvSignalLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-229">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-229">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7da0b-230">Signal Pegel, wie er auf Kanal 2 empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="7da0b-230">Signal level as received on channel 2.</span></span></p>
<p><span data-ttu-id="7da0b-231">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7da0b-231">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da0b-232"><strong>RecvNoiseLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-232"><strong>RecvNoiseLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-233">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-233">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7da0b-234">Geräuschpegel, wie er auf Kanal 1 empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="7da0b-234">Noise level as received on channel 1.</span></span></p>
<p><span data-ttu-id="7da0b-235">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7da0b-235">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da0b-236"><strong>RecvNoiseLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-236"><strong>RecvNoiseLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-237">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-237">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7da0b-238">Rauschpegel, wie er auf Kanal 2 empfangen wurde.</span><span class="sxs-lookup"><span data-stu-id="7da0b-238">Noise level as received on channel 2.</span></span></p>
<p><span data-ttu-id="7da0b-239">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7da0b-239">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da0b-240"><strong>SendSignalLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-240"><strong>SendSignalLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-241">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-241">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7da0b-242">Signal Pegel, wie er auf Kanal 1 gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7da0b-242">Signal level as sent on channel 1.</span></span></p>
<p><span data-ttu-id="7da0b-243">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7da0b-243">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da0b-244"><strong>SendSignalLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-244"><strong>SendSignalLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-245">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-245">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7da0b-246">Signal Pegel, wie er auf Kanal 2 gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7da0b-246">Signal level as sent on channel 2.</span></span></p>
<p><span data-ttu-id="7da0b-247">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7da0b-247">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7da0b-248"><strong>SendNoiseLevelCh1</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-248"><strong>SendNoiseLevelCh1</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-249">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-249">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7da0b-250">Rauschpegel, wie er auf Kanal 1 gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7da0b-250">Noise level as sent on channel 1.</span></span></p>
<p><span data-ttu-id="7da0b-251">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7da0b-251">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7da0b-252"><strong>SendNoiseLevelCh2</strong></span><span class="sxs-lookup"><span data-stu-id="7da0b-252"><strong>SendNoiseLevelCh2</strong></span></span></p></td>
<td><p><span data-ttu-id="7da0b-253">int</span><span class="sxs-lookup"><span data-stu-id="7da0b-253">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="7da0b-254">Rauschpegel, wie er auf Kanal 2 gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="7da0b-254">Noise level as sent on channel 2.</span></span></p>
<p><span data-ttu-id="7da0b-255">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="7da0b-255">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7da0b-256">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7da0b-256">


</div>

<span> </span>

</div>

</div>

</span></span></div>

