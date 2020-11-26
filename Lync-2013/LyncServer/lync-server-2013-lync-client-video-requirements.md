---
title: 'Lync Server 2013: Anforderungen für lync-Client Video'
description: 'Lync Server 2013: Video Anforderungen für lync-Clients.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Lync client video requirements
ms:assetid: 8f68f4c2-3194-487c-bd2f-fbe71ba8ad70
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688132(v=OCS.15)
ms:contentKeyID: 49733731
ms.date: 01/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ea1d4a993650ec8102d8b66ea5aa936ad1613f20
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426438"
---
# <a name="lync-client-video-requirements-for-lync-server-2013"></a><span data-ttu-id="7f28a-103">Video Anforderungen für lync-Clients für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f28a-103">Lync client video requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7f28a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7f28a-104">

<span> </span></span></span>

<span data-ttu-id="7f28a-105">_**Letztes Änderungsdatum des Themas:** 2016-01-29_</span><span class="sxs-lookup"><span data-stu-id="7f28a-105">_**Topic Last Modified:** 2016-01-29_</span></span>

<span data-ttu-id="7f28a-106">In diesem Abschnitt wird die Videohardware Unterstützung für lync 2013-Videoanrufe beschrieben und es wird beschrieben, wie Sie die erwartete Videoqualität für verschiedene Computer-, Tablet-und Mobile Gerätekonfigurationen ermitteln können.</span><span class="sxs-lookup"><span data-stu-id="7f28a-106">This section describes video hardware support for Lync 2013 video calls and describes how to determine the expected video quality for various computer, tablet, and mobile device configurations.</span></span>

<div>

## <a name="windows-desktop-and-tablet-video-requirements-and-capabilities"></a><span data-ttu-id="7f28a-107">Anforderungen und Funktionen für Windows-Desktop-und-Tablet-Video</span><span class="sxs-lookup"><span data-stu-id="7f28a-107">Windows Desktop and Tablet Video Requirements and Capabilities</span></span>

<span data-ttu-id="7f28a-108">Lync 2013 führt die Hardwarebeschleunigung für die Videocodierung und-Decodierung auf Grundlage des H. 264/MPEG-4 Part 10 Advanced Video Coding Standard ein.</span><span class="sxs-lookup"><span data-stu-id="7f28a-108">Lync 2013 introduces hardware acceleration for video encoding and decoding based on the H.264/MPEG-4 Part 10 Advanced Video Coding standard.</span></span> <span data-ttu-id="7f28a-109">Diese Funktion sorgt dafür, dass auch Computer mit geringeren CPU-Taktgeschwindigkeiten höher auflösende Videos codieren und decodieren können.</span><span class="sxs-lookup"><span data-stu-id="7f28a-109">This feature allows computers with lower CPU clock speeds to encode and decode higher resolution video.</span></span> <span data-ttu-id="7f28a-110">Die Anforderungen an die Videohardware hängen von der Computerkonfiguration und der gewünschten Videoauflösung ab.</span><span class="sxs-lookup"><span data-stu-id="7f28a-110">Video hardware requirements vary depending on the computer configuration and the video resolution wanted.</span></span>

<div>

## <a name="video-hardware-requirements"></a><span data-ttu-id="7f28a-111">Hardware Anforderungen für Video</span><span class="sxs-lookup"><span data-stu-id="7f28a-111">Video Hardware Requirements</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f28a-112">Funktion</span><span class="sxs-lookup"><span data-stu-id="7f28a-112">Feature</span></span></th>
<th><span data-ttu-id="7f28a-113">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f28a-113">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f28a-114">Hardwarebeschleunigte H.264-Decodierung mit DirectX Video Acceleration (DXVA)</span><span class="sxs-lookup"><span data-stu-id="7f28a-114">Hardware accelerated H.264 decoding using DirectX Video Acceleration (DXVA)</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="7f28a-115">Die Grafikkarte muss DirectX 9.0 unterstützen und den Decodierungsmodus DXVA2_ModeH264_VLD_NoFGT beherrschen.</span><span class="sxs-lookup"><span data-stu-id="7f28a-115">Graphics card must support DirectX 9.0 and must expose the DXVA2_ModeH264_VLD_NoFGT decoding mode.</span></span></p></li>
<li><p><span data-ttu-id="7f28a-116">Der aktuellste Grafikkartentreiber muss installiert sein.</span><span class="sxs-lookup"><span data-stu-id="7f28a-116">The latest graphics card driver must be installed.</span></span></p></li>
</ul>
<div>

> [!NOTE]  
> <span data-ttu-id="7f28a-117">Details zu den Decodierungs Modi finden Sie unter <A href="https://go.microsoft.com/fwlink/p/?linkid=268530">https://go.microsoft.com/fwlink/p/?LinkId=268530</A> .</span><span class="sxs-lookup"><span data-stu-id="7f28a-117">For details about decoding modes, see <A href="https://go.microsoft.com/fwlink/p/?linkid=268530">https://go.microsoft.com/fwlink/p/?LinkId=268530</A>.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f28a-118">Hardwarebeschleunigte H.264-Codierung: Chipsatzanforderungen</span><span class="sxs-lookup"><span data-stu-id="7f28a-118">Hardware accelerated H.264 encoding: Chipset Requirements</span></span></p></td>
<td><p><span data-ttu-id="7f28a-119">Folgende hardwarebeschleunigte Videocodierungslösungen von Intel werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="7f28a-119">The following Intel hardware accelerated video encoding solutions are supported:</span></span></p>
<ul>
<li><p><span data-ttu-id="7f28a-120">Intel HD-Grafik 2000, 2500, 3000 und 4000-Chipsätze (oder neuere Versionen) der zweiten und dritten Generation mit integrierten Hardware-Video-Encoder.</span><span class="sxs-lookup"><span data-stu-id="7f28a-120">Second and third generation Intel HD Graphics 2000, 2500, 3000, and 4000 chipsets (or later versions) with integrated hardware video encoders.</span></span> <span data-ttu-id="7f28a-121">Die Installation des Intel HD Graphics-Treibers 15.28.9.2884 oder des aktuellsten Treibers, der Folgendes enthält, ist erforderlich:</span><span class="sxs-lookup"><span data-stu-id="7f28a-121">Installation of the Intel HD Graphics driver 15.28.9.2884 or the latest driver containing the following is required:</span></span></p>
<ul>
<li><p><span data-ttu-id="7f28a-122">Grafiktreiber 9.17.10.2884 oder der aktuellster Treiber</span><span class="sxs-lookup"><span data-stu-id="7f28a-122">Display driver 9.17.10.2884 or the latest driver</span></span></p></li>
<li><p><span data-ttu-id="7f28a-123">HMFT (Hardware Media Foundation Transform), Version 3.12.10.31, oder der neueste HMFT</span><span class="sxs-lookup"><span data-stu-id="7f28a-123">Hardware media foundation transform (HMFT) version 3.12.10.31 or the latest HMFT</span></span></p></li>
</ul></li>
</ul>
<p><span data-ttu-id="7f28a-124">Die folgenden AMD Hardware Accelerated Video Encoding-Lösungen werden unterstützt (erfordert CU1-Updates für lync Server 2013):</span><span class="sxs-lookup"><span data-stu-id="7f28a-124">The following AMD hardware accelerated video encoding solutions are supported (requires CU1 Updates for Lync Server 2013):</span></span></p>
<ul>
<li><p><span data-ttu-id="7f28a-p103">AMD Video Codec Engine, die in einer Reihe diskreter Grafikkarten sowie in integrierten hardwarebeschleunigten CPUs der beschleunigten Prozessoren der Serie AMD A verfügbar ist. Der AMD Video Codec Engine-Treiber 9.12.0.0 oder höher muss installiert sein.</span><span class="sxs-lookup"><span data-stu-id="7f28a-p103">AMD Video Codec Engine, which is available in several discrete graphics cards and in integrated accelerated processing units of AMD A-Series Accelerated Processors. The AMD Video Codec Engine driver 9.12.0.0 or higher must be installed.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f28a-127">Hardwarebeschleunigte H.264-Codierung: Kameraanforderungen</span><span class="sxs-lookup"><span data-stu-id="7f28a-127">Hardware accelerated H.264 encoding: Camera Requirements</span></span></p></td>
<td><p><span data-ttu-id="7f28a-128">USB-Videokameras mit integrierter H.264-Hardwarecodierung entsprechend der USB Video Class (UVC-)Spezifikation Version 1.5.</span><span class="sxs-lookup"><span data-stu-id="7f28a-128">USB video cameras with integrated H.264 hardware encoder that conforms to the USB Video Class (UVC) specification version 1.5.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="7f28a-129">Lync 2013 unterstützt UVC 1,5-Kameras mit Windows 8 oder Windows 8,1, einschließlich Unterstützung für UVC 1,5.</span><span class="sxs-lookup"><span data-stu-id="7f28a-129">Lync 2013 supports UVC 1.5 cameras with Windows 8 or Windows 8.1, which includes support for UVC 1.5.</span></span> <span data-ttu-id="7f28a-130">Da Windows 7 keine Unterstützung für UVC 1,5 enthält, behandelt lync 2013 UVC 1,5-Kameras als normale Kameras ohne Unterstützung für die Hardware Codierung.</span><span class="sxs-lookup"><span data-stu-id="7f28a-130">Because Windows 7 does not include support for UVC 1.5, Lync 2013 treats UVC 1.5 cameras as regular cameras with no hardware encoding support.</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="determining-h264-video-encoding-and-decoding-capabilities"></a><span data-ttu-id="7f28a-131">Ermitteln von H. 264-Video Codierungs-und-Decodierungsfunktionen</span><span class="sxs-lookup"><span data-stu-id="7f28a-131">Determining H.264 Video Encoding and Decoding Capabilities</span></span>

<span data-ttu-id="7f28a-132">In der Regel werden die maximalen Codierungs- und Decodierungsmöglichkeiten einer konkreten Computerkonfiguration durch vier Hauptfaktoren bestimmt:</span><span class="sxs-lookup"><span data-stu-id="7f28a-132">Generally, there are four major factors that determine the maximum encoding and decoding capability of a particular computer configuration:</span></span>

  - <span data-ttu-id="7f28a-133">Unterstützung einer hardwarebeschleunigten Decodierung mittels DXVA</span><span class="sxs-lookup"><span data-stu-id="7f28a-133">Support for hardware accelerated decoding by using DXVA</span></span>

  - <span data-ttu-id="7f28a-134">Unterstützung einer hardwarebeschleunigten Codierung</span><span class="sxs-lookup"><span data-stu-id="7f28a-134">Support for hardware accelerated encoding</span></span>

  - <span data-ttu-id="7f28a-135">Anzahl der physischen Kerne</span><span class="sxs-lookup"><span data-stu-id="7f28a-135">Number of physical cores</span></span>

  - <span data-ttu-id="7f28a-136">Windows Experience Index (WEI)</span><span class="sxs-lookup"><span data-stu-id="7f28a-136">Windows Experience Index (WEI)</span></span>

<span data-ttu-id="7f28a-137">Das Windows System Assessment Tool (WinSAT) ermittelt den WEI-Wert.</span><span class="sxs-lookup"><span data-stu-id="7f28a-137">The Windows System Assessment Tool (WinSAT) determines the WEI.</span></span> <span data-ttu-id="7f28a-138">Wenn Sie das WinSAT-Tool ausführen, wird auf dem Computer im \\ \\ WinSAT- \\ DataStore-Verzeichnis von% windir% ein formales XML-Dokument für die Bewertung generiert.</span><span class="sxs-lookup"><span data-stu-id="7f28a-138">When you run the WinSAT tool, it generates a Formal.Assessment XML document on the computer in the %windir%\\Performance\\WinSAT\\DataStore directory.</span></span> <span data-ttu-id="7f28a-139">Diese XML-Datei enthält die beiden folgenden Bewertungen, die für die Ermittlung der Codierungs- und Decodierungsmöglichkeiten ausgesprochen wichtig sind:</span><span class="sxs-lookup"><span data-stu-id="7f28a-139">This XML file contains the following two scores that are of particular importance for determining encoding and decoding capabilities:</span></span>

  - <span data-ttu-id="7f28a-140">Der Wert „VideoEncodeScore“ gibt die softwarebasierte Viedeocodierungsfähigkeit des Computers an.</span><span class="sxs-lookup"><span data-stu-id="7f28a-140">The VideoEncodeScore indicates the software-based video encoding capability of the computer.</span></span>

  - <span data-ttu-id="7f28a-141">Der Wert „GraphicsScore“ gibt die hardwarebeschleunigte Codierungsfähigkeit des Computers an.</span><span class="sxs-lookup"><span data-stu-id="7f28a-141">The GraphicsScore value indicates the hardware accelerated encoding capability of the computer.</span></span>

<span data-ttu-id="7f28a-p106">Die folgenden drei Tabellen erläutern die maximalen Codierungs- und Decodierungsfähigkeiten verschiedener PC-Typen in Abhängigkeit von der unterstützten Hardwarebeschleunigung. Für Auflösungen von 640 x 360 und darüber beträgt die maximal unterstützte Framerate 30 Frames pro Sekunde (fps). Für Auflösungen unter 640 x 360 beträgt die maximal unterstützte Framerate 15 fps.</span><span class="sxs-lookup"><span data-stu-id="7f28a-p106">The following three tables explain the maximum encoding and decoding capability for different PC types depending on what hardware acceleration they support. For resolutions of 640x360 and higher, the maximum supported frame rate is 30 frames per second (fps). For resolutions lower than 640x360, the maximum supported frame rate is 15 fps.</span></span>

### <a name="computer-without-dxva-and-without-hardware-accelerated-encoder"></a><span data-ttu-id="7f28a-145">Computer ohne DXVA und ohne hardwarebeschleunigten Codierer</span><span class="sxs-lookup"><span data-stu-id="7f28a-145">Computer Without DXVA And Without Hardware Accelerated Encoder</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f28a-146">Mögliche Codiererauflösung</span><span class="sxs-lookup"><span data-stu-id="7f28a-146">Capable Encoder Resolution</span></span></th>
<th><span data-ttu-id="7f28a-147">Mögliche Decodiererauflösung</span><span class="sxs-lookup"><span data-stu-id="7f28a-147">Capable Decoder Resolution</span></span></th>
<th><span data-ttu-id="7f28a-148">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f28a-148">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f28a-149">424 x 240</span><span class="sxs-lookup"><span data-stu-id="7f28a-149">424x240</span></span></p></td>
<td><p><span data-ttu-id="7f28a-150">424 x 240 (640 x 360 bei 15 fps für Szenarien, bei denen nur empfangen wird)</span><span class="sxs-lookup"><span data-stu-id="7f28a-150">424x240 (640x360 at 15fps for receive only scenarios)</span></span></p></td>
<td><p><span data-ttu-id="7f28a-151">1 Kern und VideoEncodeScore ≥ 4,0</span><span class="sxs-lookup"><span data-stu-id="7f28a-151">1 Core and VideoEncodeScore ≥ 4.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f28a-152">640 x 360</span><span class="sxs-lookup"><span data-stu-id="7f28a-152">640x360</span></span></p></td>
<td><p><span data-ttu-id="7f28a-153">640 x 360</span><span class="sxs-lookup"><span data-stu-id="7f28a-153">640x360</span></span></p></td>
<td><p><span data-ttu-id="7f28a-154">2 Kerne und VideoEncodeScore ≥ 4,5</span><span class="sxs-lookup"><span data-stu-id="7f28a-154">2 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f28a-155">640 x 360</span><span class="sxs-lookup"><span data-stu-id="7f28a-155">640x360</span></span></p></td>
<td><p><span data-ttu-id="7f28a-156">1280 x 720</span><span class="sxs-lookup"><span data-stu-id="7f28a-156">1280x720</span></span></p></td>
<td><p><span data-ttu-id="7f28a-157">2 Kerne und VideoEncodeScore ≥ 4,5</span><span class="sxs-lookup"><span data-stu-id="7f28a-157">2 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f28a-158">640 x 360</span><span class="sxs-lookup"><span data-stu-id="7f28a-158">640x360</span></span></p></td>
<td><p><span data-ttu-id="7f28a-159">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="7f28a-159">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="7f28a-160">4 Kerne und VideoEncodeScore ≥ 4,5</span><span class="sxs-lookup"><span data-stu-id="7f28a-160">4 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f28a-161">1280 x 720</span><span class="sxs-lookup"><span data-stu-id="7f28a-161">1280x720</span></span></p></td>
<td><p><span data-ttu-id="7f28a-162">1280 x 720</span><span class="sxs-lookup"><span data-stu-id="7f28a-162">1280x720</span></span></p></td>
<td><p><span data-ttu-id="7f28a-163">4 Kerne und VideoEncodeScore ≥ 7,3</span><span class="sxs-lookup"><span data-stu-id="7f28a-163">4 Cores and VideoEncodeScore ≥ 7.3</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f28a-164">1280 x 720</span><span class="sxs-lookup"><span data-stu-id="7f28a-164">1280x720</span></span></p></td>
<td><p><span data-ttu-id="7f28a-165">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="7f28a-165">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="7f28a-166">4 Kerne und VideoEncodeScore ≥ 7,3</span><span class="sxs-lookup"><span data-stu-id="7f28a-166">4 Cores and VideoEncodeScore ≥ 7.3</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f28a-167">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="7f28a-167">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="7f28a-168">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="7f28a-168">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="7f28a-169">-</span><span class="sxs-lookup"><span data-stu-id="7f28a-169">N/A</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="computer-with-dxva-but-without-hardware-accelerated-encoder"></a><span data-ttu-id="7f28a-170">Computer mit DXVA, aber ohne hardwarebeschleunigten Codierer</span><span class="sxs-lookup"><span data-stu-id="7f28a-170">Computer With DXVA But Without Hardware Accelerated Encoder</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f28a-171">Mögliche Codiererauflösung</span><span class="sxs-lookup"><span data-stu-id="7f28a-171">Capable Encoder Resolution</span></span></th>
<th><span data-ttu-id="7f28a-172">Mögliche Decodiererauflösung</span><span class="sxs-lookup"><span data-stu-id="7f28a-172">Capable Decoder Resolution</span></span></th>
<th><span data-ttu-id="7f28a-173">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f28a-173">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f28a-174">424 x 240</span><span class="sxs-lookup"><span data-stu-id="7f28a-174">424x240</span></span></p></td>
<td><p><span data-ttu-id="7f28a-175">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="7f28a-175">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="7f28a-176">1 Kern und VideoEncodeScore ≥ 3,0</span><span class="sxs-lookup"><span data-stu-id="7f28a-176">1 Core and VideoEncodeScore ≥ 3.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f28a-177">640 x 360</span><span class="sxs-lookup"><span data-stu-id="7f28a-177">640x360</span></span></p></td>
<td><p><span data-ttu-id="7f28a-178">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="7f28a-178">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="7f28a-179">2 Kerne und VideoEncodeScore ≥ 4,5</span><span class="sxs-lookup"><span data-stu-id="7f28a-179">2 Cores and VideoEncodeScore ≥ 4.5</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f28a-180">960 x 540</span><span class="sxs-lookup"><span data-stu-id="7f28a-180">960x540</span></span></p></td>
<td><p><span data-ttu-id="7f28a-181">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="7f28a-181">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="7f28a-182">2 Kerne und VideoEncodeScore ≥ 6,0</span><span class="sxs-lookup"><span data-stu-id="7f28a-182">2 Cores and VideoEncodeScore ≥ 6.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f28a-183">1280 x 720</span><span class="sxs-lookup"><span data-stu-id="7f28a-183">1280x720</span></span></p></td>
<td><p><span data-ttu-id="7f28a-184">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="7f28a-184">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="7f28a-185">4 Kerne und VideoEncodeScore ≥ 6,7</span><span class="sxs-lookup"><span data-stu-id="7f28a-185">4 Cores and VideoEncodeScore ≥ 6.7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7f28a-186">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="7f28a-186">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="7f28a-187">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="7f28a-187">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="7f28a-188">4 Kerne und VideoEncodeScore ≥ 8,2</span><span class="sxs-lookup"><span data-stu-id="7f28a-188">4 Cores and VideoEncodeScore ≥ 8.2</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="7f28a-p107">Die WinSAT-Bewertung ist unter Windows 7 auf maximal 7,9 beschränkt. Die maximale Codierungsfähigkeit für einen Computer ohne hardwarebeschleunigten Codierer kann daher nur unter Windows 8 oder Windows 8.1 erreicht werden, wo der maximale WinSAT-Wert bei 9,9 liegt.</span><span class="sxs-lookup"><span data-stu-id="7f28a-p107">The WinSAT score on Windows 7 is limited to a maximum of 7.9. Therefore, the encoding capability for a computer without a hardware accelerated encoder can only be achieved on Windows 8 or Windows 8.1, where the maximum WinSAT score is 9.9.</span></span>



</div>

### <a name="computer-with-dxva-and-with-intel-hd-graphics-hardware-accelerated-encoder"></a><span data-ttu-id="7f28a-191">Computer mit DXVA und mit durch Intel HD Graphics hardwarebeschleunigtem Codierer</span><span class="sxs-lookup"><span data-stu-id="7f28a-191">Computer With DXVA And With Intel HD Graphics Hardware Accelerated Encoder</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f28a-192">Mögliche Codiererauflösung</span><span class="sxs-lookup"><span data-stu-id="7f28a-192">Capable Encoder Resolution</span></span></th>
<th><span data-ttu-id="7f28a-193">Mögliche Decodiererauflösung</span><span class="sxs-lookup"><span data-stu-id="7f28a-193">Capable Decoder Resolution</span></span></th>
<th><span data-ttu-id="7f28a-194">Anforderung</span><span class="sxs-lookup"><span data-stu-id="7f28a-194">Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f28a-195">1280 x 720</span><span class="sxs-lookup"><span data-stu-id="7f28a-195">1280x720</span></span></p></td>
<td><p><span data-ttu-id="7f28a-196">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="7f28a-196">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="7f28a-197">Alle Intel HD Graphics-Modelle der 2. und 3. Generation</span><span class="sxs-lookup"><span data-stu-id="7f28a-197">All 2nd and 3rd generation Intel HD Graphics</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f28a-198">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="7f28a-198">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="7f28a-199">1920 x 1080</span><span class="sxs-lookup"><span data-stu-id="7f28a-199">1920x1080</span></span></p></td>
<td><p><span data-ttu-id="7f28a-200">Intel HD Graphics-Modelle der 2. und 3. Generation und GraphicsScore ≥ 5,0</span><span class="sxs-lookup"><span data-stu-id="7f28a-200">2nd and 3rd generation Intel HD Graphics and GraphicsScore ≥ 5.0</span></span></p></td>
</tr>
</tbody>
</table>


</div>

</div>

<div>

## <a name="mobile-device-video-capabilities"></a><span data-ttu-id="7f28a-201">Video Funktionen für mobile Geräte</span><span class="sxs-lookup"><span data-stu-id="7f28a-201">Mobile Device Video Capabilities</span></span>

<span data-ttu-id="7f28a-202">In der folgenden Tabelle werden die maximalen Videofunktionen der unterstützten mobilen Geräte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7f28a-202">The following table describes the maximum video capabilities for supported mobile devices.</span></span> <span data-ttu-id="7f28a-203">Weitere Informationen zur Unterstützung mobiler Geräte finden Sie unter [Planen mobiler Clients in lync Server 2013](lync-server-2013-planning-for-mobile-clients.md).</span><span class="sxs-lookup"><span data-stu-id="7f28a-203">For more information about mobile device support, see [Planning for mobile clients in Lync Server 2013](lync-server-2013-planning-for-mobile-clients.md).</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7f28a-204">Funktion</span><span class="sxs-lookup"><span data-stu-id="7f28a-204">Feature</span></span></th>
<th><span data-ttu-id="7f28a-205">Windows Phone</span><span class="sxs-lookup"><span data-stu-id="7f28a-205">Windows Phone</span></span></th>
<th><span data-ttu-id="7f28a-206">iPhone</span><span class="sxs-lookup"><span data-stu-id="7f28a-206">iPhone</span></span></th>
<th><span data-ttu-id="7f28a-207">iPad</span><span class="sxs-lookup"><span data-stu-id="7f28a-207">iPad</span></span></th>
<th><span data-ttu-id="7f28a-208">Android</span><span class="sxs-lookup"><span data-stu-id="7f28a-208">Android</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7f28a-209">Maximale Auflösung der H.264-Codierung</span><span class="sxs-lookup"><span data-stu-id="7f28a-209">H.264 encoding maximum resolution</span></span></p></td>
<td><p><span data-ttu-id="7f28a-210">VGA</span><span class="sxs-lookup"><span data-stu-id="7f28a-210">VGA</span></span></p></td>
<td><p><span data-ttu-id="7f28a-211">QVGA: iPhone 4S</span><span class="sxs-lookup"><span data-stu-id="7f28a-211">QVGA: iPhone 4S</span></span></p>
<p><span data-ttu-id="7f28a-212">VGA: iPhone 5</span><span class="sxs-lookup"><span data-stu-id="7f28a-212">VGA: iPhone 5</span></span></p>
<p><span data-ttu-id="7f28a-213">720p: iPhone 5S und höher</span><span class="sxs-lookup"><span data-stu-id="7f28a-213">720p: iPhone 5S and later</span></span></p></td>
<td><p><span data-ttu-id="7f28a-214">VGA: iPad 2 und höher/iPad mini 1 und höher</span><span class="sxs-lookup"><span data-stu-id="7f28a-214">VGA: iPad 2 and later/iPad mini 1 and later</span></span></p>
<p><span data-ttu-id="7f28a-215">720p: iPad Air/iPad mini 2/iPad Pro und höher</span><span class="sxs-lookup"><span data-stu-id="7f28a-215">720p: iPad Air/iPad mini 2/iPad Pro and later</span></span></p></td>
<td><p><span data-ttu-id="7f28a-216">Bis zu VGA je nach Gerätemodell</span><span class="sxs-lookup"><span data-stu-id="7f28a-216">Up to VGA depending on device model</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7f28a-217">Maximale Auflösung der H.264-Decodierung</span><span class="sxs-lookup"><span data-stu-id="7f28a-217">H.264 decoding maximum resolution</span></span></p></td>
<td><p><span data-ttu-id="7f28a-218">VGA</span><span class="sxs-lookup"><span data-stu-id="7f28a-218">VGA</span></span></p></td>
<td><p><span data-ttu-id="7f28a-219">QVGA: iPhone 4S</span><span class="sxs-lookup"><span data-stu-id="7f28a-219">QVGA: iPhone 4S</span></span></p>
<p><span data-ttu-id="7f28a-220">VGA: iPhone 5</span><span class="sxs-lookup"><span data-stu-id="7f28a-220">VGA: iPhone 5</span></span></p>
<p><span data-ttu-id="7f28a-221">720p: iPhone 5S und höher</span><span class="sxs-lookup"><span data-stu-id="7f28a-221">720p: iPhone 5S and later</span></span></p></td>
<td><p><span data-ttu-id="7f28a-222">VGA: iPad 2 und höher/iPad mini 1 und höher</span><span class="sxs-lookup"><span data-stu-id="7f28a-222">VGA: iPad 2 and later/iPad mini 1 and later</span></span></p>
<p><span data-ttu-id="7f28a-223">720p: iPad Air/iPad mini 2/iPad Pro und höher</span><span class="sxs-lookup"><span data-stu-id="7f28a-223">720p: iPad Air/iPad mini 2/iPad Pro and later</span></span></p></td>
<td><p><span data-ttu-id="7f28a-224">Bis zu VGA je nach Gerätemodell</span><span class="sxs-lookup"><span data-stu-id="7f28a-224">Up to VGA depending on device model</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7f28a-225">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7f28a-225">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

