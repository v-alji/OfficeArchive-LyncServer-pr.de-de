---
title: 'Lync Server 2013: AudioClientEvent-Tabelle'
description: 'Lync Server 2013: AudioClientEvent-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: AudioClientEvent table
ms:assetid: fef73d8f-7261-4e5b-9769-82435b007979
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413086(v=OCS.15)
ms:contentKeyID: 48185967
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2200cd9567bdd10ac4ad8f5c269062c2f5614dcb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438210"
---
# <a name="audioclientevent-table-in-lync-server-2013"></a><span data-ttu-id="6b7bc-103">AudioClientEvent-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6b7bc-103">AudioClientEvent table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6b7bc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6b7bc-104">

<span> </span></span></span>

<span data-ttu-id="6b7bc-105">_**Letztes Änderungsdatum des Themas:** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="6b7bc-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="6b7bc-106">Jeder Datensatz enthält ein Clientereignis für einen Endpunkt in einem Audioanruf.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-106">Each record contains a client event for one endpoint in an audio call.</span></span> <span data-ttu-id="6b7bc-107">In der Regel verfügt ein Anruf über zwei Datensätze, einen für den Anrufer und einen für den aufgerufenen.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-107">Usually, one call has two records, one for caller and one for callee.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6b7bc-108"><strong>Spalte</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="6b7bc-109"><strong>Datentyp</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="6b7bc-110"><strong>Schlüssel/Index</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="6b7bc-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6b7bc-112"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-112"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-113">datetime</span><span class="sxs-lookup"><span data-stu-id="6b7bc-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="6b7bc-114">Primary</span><span class="sxs-lookup"><span data-stu-id="6b7bc-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="6b7bc-115">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-115">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7bc-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-117">int</span><span class="sxs-lookup"><span data-stu-id="6b7bc-117">int</span></span></p></td>
<td><p><span data-ttu-id="6b7bc-118">Primary</span><span class="sxs-lookup"><span data-stu-id="6b7bc-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="6b7bc-119">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-119">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7bc-120"><strong>MediaLineLabel</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-120"><strong>MediaLineLabel</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-121">tinyint</span><span class="sxs-lookup"><span data-stu-id="6b7bc-121">tinyint</span></span></p></td>
<td><p><span data-ttu-id="6b7bc-122">Primary</span><span class="sxs-lookup"><span data-stu-id="6b7bc-122">Primary</span></span></p></td>
<td><p><span data-ttu-id="6b7bc-123">Auf die <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-123">Referenced from the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7bc-124"><strong>FromCaller</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-124"><strong>FromCaller</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-125">bit</span><span class="sxs-lookup"><span data-stu-id="6b7bc-125">bit</span></span></p></td>
<td><p><span data-ttu-id="6b7bc-126">Primary</span><span class="sxs-lookup"><span data-stu-id="6b7bc-126">Primary</span></span></p></td>
<td><p><span data-ttu-id="6b7bc-127">0: Daten des angerufenen</span><span class="sxs-lookup"><span data-stu-id="6b7bc-127">0: Callee’s data</span></span></p>
<p><span data-ttu-id="6b7bc-128">1: Daten des Anrufers</span><span class="sxs-lookup"><span data-stu-id="6b7bc-128">1: Caller’s data</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7bc-129"><strong>NetworkSendQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-129"><strong>NetworkSendQualityEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-130">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6b7bc-130">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6b7bc-131">Prozentsatz der Sitzung, für die das NetworkSendQuality-Ereignis für den Zustand "falsch" ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-131">Percentage of session the NetworkSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="6b7bc-132">Die Netzwerkqualität in Bezug auf Jitter oder Paketverlust ist schwerwiegend und beeinträchtigt die Qualität des gesendeten Audiosignals.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-132">Network quality in terms of jitter or packet loss is severe and impacting the quality of audio being sent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7bc-133"><strong>NetworkReceiveQualityEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-133"><strong>NetworkReceiveQualityEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-134">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6b7bc-134">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6b7bc-135">Prozentsatz der Sitzung, für die das ReceiveSendQuality-Ereignis für den Zustand "falsch" ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-135">Percentage of session the ReceiveSendQuality event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="6b7bc-136">Die Netzwerkqualität in Bezug auf Jitter oder Paketverlust ist schwerwiegend und beeinträchtigt die Qualität des empfangenen Audiosignals.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-136">Network quality in terms of jitter or packet loss is severe and impacting the quality of audio being received.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7bc-137"><strong>NetworkDelayEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-137"><strong>NetworkDelayEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-138">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6b7bc-138">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6b7bc-139">Prozentsatz der Sitzung, für die das Delay-Ereignis für den Zustand "falsch" ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-139">Percentage of session the Delay event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="6b7bc-140">Die Netzwerklatenz ist schwerwiegend und beeinträchtigt die Erfahrung, indem Sie die interaktive Kommunikation verhindert.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-140">Network latency is severe and impacting the experience by preventing interactive communication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7bc-141"><strong>NetworkBandwidthLowEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-141"><strong>NetworkBandwidthLowEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-142">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6b7bc-142">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6b7bc-143">Prozentsatz der Sitzung, für die das LowBandwidth-Ereignis für den Zustand "falsch" ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-143">Percentage of session the LowBandwidth event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="6b7bc-144">Die verfügbare Bandbreite reicht für ein akzeptables Spracherlebnis nicht aus.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-144">The available bandwidth is insufficient for an acceptable voice experience.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7bc-145"><strong>CPUInsufficientEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-145"><strong>CPUInsufficientEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-146">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6b7bc-146">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6b7bc-147">Prozentsatz der Sitzung das unzureichende CPU-Ereignis wurde für den Zustand "falsch" ausgelöst.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-147">Percentage of session the insufficient CPU event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="6b7bc-148">Es gibt unzureichende CPU-Zyklen für die Verarbeitung mit den aktuellen Modalitäten und Anwendungen, die verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-148">There are insufficient CPU cycles for processing with the current modalities and applications in use.</span></span> <span data-ttu-id="6b7bc-149">Dies verursacht Verzerrungen beim Audiokanal.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-149">This causes distortions with the audio channel.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7bc-150"><strong>DeviceHalfDuplexAECEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-150"><strong>DeviceHalfDuplexAECEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-151">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6b7bc-151">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6b7bc-152">Prozentsatz der Sitzung, für die das DeviceHalfDuplexAEC-Ereignis für den Zustand "falsch" ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-152">Percentage of session the DeviceHalfDuplexAEC event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="6b7bc-153">Um Echo zu verhindern, hat das System die Eingabe Hälfte Duplex.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-153">In order to prevent echo, the system has enter half duplex.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7bc-154"><strong>DeviceRenderNotFunctioningEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-154"><strong>DeviceRenderNotFunctioningEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-155">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6b7bc-155">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6b7bc-156">Prozentsatz der Sitzung, für die das DeviceRenderNotFunctioning-Ereignis für den Zustand "falsch" ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-156">Percentage of session the DeviceRenderNotFunctioning event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="6b7bc-157">Das Rendering-Gerät, das derzeit für die Sitzung verwendet wird, funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-157">The render device currently being used for the session is not functioning correctly.</span></span> <span data-ttu-id="6b7bc-158">Dies kann zu einseitigen Audioproblemen führen.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-158">This can cause one-way audio issues.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7bc-159"><strong>DeviceCaptureNotFunctioningEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-159"><strong>DeviceCaptureNotFunctioningEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-160">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6b7bc-160">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6b7bc-161">Prozentsatz der Sitzung, für die das DeviceCaptureNotFunctioning-Ereignis für den Zustand "falsch" ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-161">Percentage of session the DeviceCaptureNotFunctioning event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="6b7bc-162">Das Aufnahmegerät, das derzeit für die Sitzung verwendet wird, funktioniert nicht ordnungsgemäß.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-162">The capture device currently being used for the session is not functioning correctly.</span></span> <span data-ttu-id="6b7bc-163">Dies kann zu einseitigen Audioproblemen führen.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-163">This can cause one-way audio issues.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7bc-164"><strong>DeviceGlitchesEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-164"><strong>DeviceGlitchesEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-165">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6b7bc-165">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6b7bc-166">Prozentsatz der Sitzung, für die das DeviceGlitches-Ereignis für den Zustand "falsch" ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-166">Percentage of session the DeviceGlitches event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="6b7bc-167">Bei der Wiedergabe von Audio, die zu Verzerrungen führt, gibt es schwere Störungen.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-167">There are severe glitches in the rendering of audio which is causing distortions.</span></span> <span data-ttu-id="6b7bc-168">Diese Störungen können durch Treiber Probleme, verzögerte Prozeduraufrufe (DPC) Storm (Treiber) und eine höhere CPU-Auslastung verursacht werden.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-168">These glitches can be caused by driver issues, deferred procedure calls (DPC) storm (drivers), and high CPU usage.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7bc-169"><strong>DeviceLowSNREventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-169"><strong>DeviceLowSNREventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-170">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6b7bc-170">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6b7bc-171">Prozentsatz der Sitzung, für die das DeviceLowSNR-Ereignis für den Zustand "falsch" ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-171">Percentage of session the DeviceLowSNR event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="6b7bc-172">Die Aufnahmequalität ist sehr schlecht, entweder sehr laut oder der Nutzer spricht zu weit vom Mikrofon entfernt.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-172">The capture quality is very poor, either very noisy or user is talking too far away from the microphone.</span></span> <span data-ttu-id="6b7bc-173">Dies führt zu Verzerrungen.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-173">This will cause distortions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7bc-174"><strong>DeviceLowSpeechLevelEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-174"><strong>DeviceLowSpeechLevelEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-175">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6b7bc-175">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6b7bc-176">Prozentsatz der Sitzung, für die das DeviceLowSpeechLevel-Ereignis für den Zustand "falsch" ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-176">Percentage of session the DeviceLowSpeechLevel event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="6b7bc-177">Der Sprachpegel des Benutzers ist zu gering, und das System kann ihn nicht weiter erhöhen.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-177">User‘s speech level is too low and the system cannot increase it any further.</span></span> <span data-ttu-id="6b7bc-178">Dies kann entweder zu Verzerrungen führen oder als unidirektionale Audiowiedergabe wahrgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-178">This can either cause distortions or perceived as one-way audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7bc-179"><strong>DeviceClippingEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-179"><strong>DeviceClippingEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-180">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6b7bc-180">Decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6b7bc-181">Prozentsatz der Sitzung, für die das DeviceClipping-Ereignis für den Zustand "falsch" ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-181">Percentage of session the DeviceClipping event was fired for ‘Bad’ state.</span></span></p>
<p><span data-ttu-id="6b7bc-182">Wenn das Mikrofon in der Nähe von Sprachausgabe Clips abgespielt wird, hören Sie Verzerrungen durch Clipping.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-182">When near-end speech clips the microphone, far-end hears distortion due to clipping.</span></span> <span data-ttu-id="6b7bc-183">Es ist wichtig, das Mikrofon-Clipping in der Nähe zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-183">It is important to avoid near-end microphone clipping.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7bc-184"><strong>DeviceEchoEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-184"><strong>DeviceEchoEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-185">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6b7bc-185">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6b7bc-186">Prozentsatz der Sitzung, für die das DeviceEchoEvent-Ereignis für den Zustand "falsch" ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-186">Percentage of session the DeviceEchoEvent event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="6b7bc-187">Gerät oder Setup verursacht Echo über die Fähigkeit des Systems hinaus, dies zu kompensieren.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-187">Device or setup is causing echo beyond the ability of the system to compensate.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7bc-188"><strong>DeviceNearEndToEchoRatioEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-188"><strong>DeviceNearEndToEchoRatioEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-189">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6b7bc-189">decimal(5,2)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6b7bc-190">Prozentsatz der Sitzung, für die das DeviceNearEndToEchoRatio-Ereignis für den Zustand "falsch" ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-190">Percentage of session the DeviceNearEndToEchoRatio event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="6b7bc-191">Die Sprache des Benutzers ist im Vergleich zu dem aufgenommenen Echo zu gering, was sich auf die Benutzererfahrung auswirkt, weil dadurch die Benutzerfreundlichkeit eingeschränkt wird.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-191">The user’s speech is too low compared to the echo being captured which impacts the users experience because it limits how easy it is to interrupt a user.</span></span> <span data-ttu-id="6b7bc-192">Verringern Sie die Lautstärke des Mikrofons, und bewegen Sie das Mikrofon näher an den Redner.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-192">Reduce speaker volume, move the microphone closer to the talker.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7bc-193"><strong>DeviceMultipleEndpointsEventCount</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-193"><strong>DeviceMultipleEndpointsEventCount</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-194">int</span><span class="sxs-lookup"><span data-stu-id="6b7bc-194">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6b7bc-195">Häufigkeit, mit der während der Sitzung das DeviceMultipleEndpoints-Ereignis für den Zustand "falsch" ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-195">Number of times during session the DeviceMultipleEndpoints event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="6b7bc-196">Mehrere Audio-Endpunkte in derselben Sitzung wurden erkannt, und das System hat durch Reduzieren der rendermenge kompensiert.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-196">Multiple audio endpoints in the same session detected and the system has compensated by reducing render volume.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7bc-197"><strong>DeviceHowlingEventCount</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-197"><strong>DeviceHowlingEventCount</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-198">int</span><span class="sxs-lookup"><span data-stu-id="6b7bc-198">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="6b7bc-199">Häufigkeit, mit der während der Sitzung das DeviceHowlingEvent-Ereignis für den Zustand "falsch" ausgelöst wurde.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-199">Number of times during session the DeviceHowlingEvent event was fired for ‘Bad’ state.</span></span> <span data-ttu-id="6b7bc-200">Audiofeedback-Schleife erkannt (verursacht durch mehrere Endpunkte, die einen Audiopfad freigeben).</span><span class="sxs-lookup"><span data-stu-id="6b7bc-200">Audio feedback loop detected (caused by multiple endpoints sharing audio path).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6b7bc-201"><strong>DeviceRenderZeroVolumeEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-201"><strong>DeviceRenderZeroVolumeEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-202">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6b7bc-202">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6b7bc-203">Der Prozentsatz der Sitzung, für die das DeviceRenderZeroVolume-Ereignis ausgelöst wurde, weil es sich im Zustand "ungültig" befand.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-203">Percentage of session the DeviceRenderZeroVolume event was fired for being in the “Bad’ state.</span></span> <span data-ttu-id="6b7bc-204">Das Render-Gerät wurde auf NULL Lautstärke eingestellt.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-204">The render device was set to zero volume.</span></span></p>
<p><span data-ttu-id="6b7bc-205">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-205">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6b7bc-206"><strong>DeviceRenderMuteEventRatio</strong></span><span class="sxs-lookup"><span data-stu-id="6b7bc-206"><strong>DeviceRenderMuteEventRatio</strong></span></span></p></td>
<td><p><span data-ttu-id="6b7bc-207">Dezimal (5; 2)</span><span class="sxs-lookup"><span data-stu-id="6b7bc-207">decimal(5,2)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="6b7bc-208">Der Prozentsatz der Sitzung, für die das DeviceRenderMute-Ereignis ausgelöst wurde, weil es sich im Zustand "ungültig" befand.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-208">Percentage of session the DeviceRenderMute event was fired for being in the “Bad’ state.</span></span> <span data-ttu-id="6b7bc-209">Das Render-Gerät war stumm geschaltet.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-209">The render device was muted.</span></span></p>
<p><span data-ttu-id="6b7bc-210">Diese Spalte wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="6b7bc-210">This column was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6b7bc-211">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6b7bc-211">


</div>

<span> </span>

</div>

</div>

</span></span></div>

