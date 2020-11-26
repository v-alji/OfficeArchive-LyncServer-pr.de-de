---
title: 'Lync Server 2013: Technische Anforderungen für Reaktionsgruppen'
description: 'Lync Server 2013: Technische Voraussetzungen für die Reaktionsgruppe.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for Response Group
ms:assetid: 477488bd-124f-437b-9327-732a0d7271ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204863(v=OCS.15)
ms:contentKeyID: 48184044
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f3125ed8c732960e23970229e99bf5a8487eb96a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441298"
---
# <a name="technical-requirements-for-response-group-in-lync-server-2013"></a><span data-ttu-id="3b6b5-103">Technische Anforderungen für Reaktionsgruppen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3b6b5-103">Technical requirements for Response Group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3b6b5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3b6b5-104">

<span> </span></span></span>

<span data-ttu-id="3b6b5-105">_**Letztes Änderungsdatum des Themas:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="3b6b5-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="3b6b5-106">In diesem Abschnitt werden die folgenden technischen Voraussetzungen für die reaktionsgruppenanwendung beschrieben:</span><span class="sxs-lookup"><span data-stu-id="3b6b5-106">This section describes the following technical requirements for the Response Group application:</span></span>

  - <span data-ttu-id="3b6b5-107">Hardwareanforderungen</span><span class="sxs-lookup"><span data-stu-id="3b6b5-107">Hardware requirements</span></span>

  - <span data-ttu-id="3b6b5-108">Softwareanforderungen</span><span class="sxs-lookup"><span data-stu-id="3b6b5-108">Software requirements</span></span>

  - <span data-ttu-id="3b6b5-109">Portanforderungen</span><span class="sxs-lookup"><span data-stu-id="3b6b5-109">Port requirements</span></span>

  - <span data-ttu-id="3b6b5-110">Audiodatei-Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b6b5-110">Audio file requirements</span></span>

  - <span data-ttu-id="3b6b5-111">Anforderungen für das Konfigurationstool für Reaktionsgruppen</span><span class="sxs-lookup"><span data-stu-id="3b6b5-111">Response Group configuration tool requirements</span></span>

<div>

## <a name="hardware-requirements"></a><span data-ttu-id="3b6b5-112">Hardware Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b6b5-112">Hardware Requirements</span></span>

<span data-ttu-id="3b6b5-113">Die Antwortgruppen Anwendung hat die gleichen Hardwareanforderungen wie Front-End-Server.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-113">The Response Group application has the same hardware requirements as Front End Servers.</span></span> <span data-ttu-id="3b6b5-114">Details zu den Hardwareanforderungen finden Sie unter [Server Hardwareplattformen für lync Server 2013](lync-server-2013-server-hardware-platforms.md) in der Dokumentation zur Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-114">For details about hardware requirements, see [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) in the Supportability documentation.</span></span>

</div>

<div>

## <a name="software-requirements"></a><span data-ttu-id="3b6b5-115">Software Anforderungen</span><span class="sxs-lookup"><span data-stu-id="3b6b5-115">Software Requirements</span></span>

<span data-ttu-id="3b6b5-116">Die reaktionsgruppenanwendung hat dieselben Betriebssystemanforderungen und Softwarevoraussetzungen wie Front-End-Server.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-116">The Response Group application has the same operating system requirements and software prerequisites as Front End Servers.</span></span> <span data-ttu-id="3b6b5-117">Ausführliche Informationen zu den Softwareanforderungen finden Sie unter unter [Stützung von Server-und Tools-Betriebssystemen in lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in der Dokumentation zur Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-117">For details about software requirements, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="3b6b5-118">Wenn Sie Windows Media Audio (WMA)-Dateien für die Musik und Ankündigungen von Reaktionsgruppen verwenden, muss für alle Front-End-Server oder Standard Edition-Server, auf denen die reaktionsgruppenanwendung ausgeführt wird, die Windows Media-Format Laufzeit für Server mit Windows Server 2008 R2 oder Microsoft Media Foundation für Server mit Windows Server 2012 oder Windows Server 2012 R2 installiert sein.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-118">If you use Windows Media Audio (.wma) files for Response Group music and announcements, all Front End Servers or Standard Editions servers that run the Response Group application must have the Windows Media Format Runtime installed for servers running Windows Server 2008 R2, or Microsoft Media Foundation for servers running Windows Server 2012 or Windows Server 2012 R2.</span></span> <span data-ttu-id="3b6b5-119">Für Windows Server 2008 R2 wird die Windows Media-Format Laufzeit als Teil der Windows-Desktop Oberfläche installiert.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-119">For Windows Server 2008 R2, Windows Media Format Runtime is installed as part of Windows Desktop Experience.</span></span>

<span data-ttu-id="3b6b5-120">Weitere Informationen zu Audioanforderungen finden Sie unter "Anforderungen an die Audiodateien" weiter unten in diesem Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-120">For more details about audio requirements, see "Audio File Requirements" later in this section.</span></span>

</div>

<div>

## <a name="port-requirements"></a><span data-ttu-id="3b6b5-121">Portanforderungen</span><span class="sxs-lookup"><span data-stu-id="3b6b5-121">Port Requirements</span></span>

<span data-ttu-id="3b6b5-122">Die Antwortgruppen Anwendung verwendet die folgenden Ports:</span><span class="sxs-lookup"><span data-stu-id="3b6b5-122">The Response Group application uses the following ports:</span></span>

  - <span data-ttu-id="3b6b5-123">**Port 5071** Wird für SIP-Überwachungsanforderungen verwendet</span><span class="sxs-lookup"><span data-stu-id="3b6b5-123">**Port 5071**   Used for SIP listening requests</span></span>

  - <span data-ttu-id="3b6b5-124">**Port 8404** Dieser Port wird für die Kommunikation zwischen Servern verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-124">**Port 8404**   Used for interserver communications</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3b6b5-125">Dieser Port wird für den Übereinstimmungs Dienst verwendet und ist erforderlich, wenn die reaktionsgruppenanwendung in einem Pool mit mehr als einem Front-End-Server bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-125">This port is used for the Match Making service and is required when the Response Group application is deployed in a pool that has more than one Front End Server.</span></span>

    
    </div>

<div>


> [!NOTE]  
> <span data-ttu-id="3b6b5-126">Diese Ports sind Standardeinstellungen, die Sie mit dem Cmdlet <STRONG>Set-CsApplicationServer</STRONG> ändern können.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-126">These ports are default settings that you can change by using the <STRONG>Set-CsApplicationServer</STRONG> cmdlet.</span></span> <span data-ttu-id="3b6b5-127">Details zu diesem Cmdlet finden Sie in der Dokumentation zur lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-127">For details about this cmdlet, see the Lync Server Management Shell documentation.</span></span>



</div>

</div>

<div>

## <a name="audio-file-requirements"></a><span data-ttu-id="3b6b5-128">Anforderungen für Audiodateien</span><span class="sxs-lookup"><span data-stu-id="3b6b5-128">Audio File Requirements</span></span>

<span data-ttu-id="3b6b5-129">Die Antwortgruppen Anwendung unterstützt das Wave-Dateiformat (WAV) und das Windows Media Audio-Dateiformat (WMA) für Reaktionsgruppen Nachrichten, Warteschleife-Musik oder IVR-Fragen (Interactive Voice Response).</span><span class="sxs-lookup"><span data-stu-id="3b6b5-129">The Response Group application supports wave (.wav) file format and Windows Media audio (.wma) file format for Response Group messages, on-hold music, or interactive voice response (IVR) questions.</span></span>

<span data-ttu-id="3b6b5-130">Das Windows Media-Audiodateiformat setzt voraus, dass die Windows Media-Format Laufzeit auf Front-End-Servern mit Windows Server 2008 R2 und Windows Server 2008 installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-130">The Windows Media audio file format requires that the Windows Media Format Runtime is installed on Front End Servers running Windows Server 2008 R2 and Windows Server 2008.</span></span> <span data-ttu-id="3b6b5-131">Nähere Informationen dazu finden Sie weiter oben in diesem Abschnitt unter „Softwareanforderungen“.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-131">For more details, see "Software Requirements" earlier in this section.</span></span>

<div>

## <a name="supported-wave-file-formats"></a><span data-ttu-id="3b6b5-132">Unterstützte WAV-Dateiformate</span><span class="sxs-lookup"><span data-stu-id="3b6b5-132">Supported Wave File Formats</span></span>

<span data-ttu-id="3b6b5-133">WAV-Dateien müssen folgenden Anforderungen entsprechen:</span><span class="sxs-lookup"><span data-stu-id="3b6b5-133">All wave files must meet the following requirements:</span></span>

  - <span data-ttu-id="3b6b5-134">8- oder 16-Bit-Datei</span><span class="sxs-lookup"><span data-stu-id="3b6b5-134">8-bit or 16-bit file</span></span>

  - <span data-ttu-id="3b6b5-135">LPCM- (Linear Pulse Code Modulation), A-Law- oder µ-Law-Format</span><span class="sxs-lookup"><span data-stu-id="3b6b5-135">Linear pulse code modulation (LPCM), A-Law, or mu-Law format</span></span>

  - <span data-ttu-id="3b6b5-136">Mono oder Stereo</span><span class="sxs-lookup"><span data-stu-id="3b6b5-136">Mono or stereo</span></span>

  - <span data-ttu-id="3b6b5-137">Maximal 4 MB</span><span class="sxs-lookup"><span data-stu-id="3b6b5-137">4MB or less</span></span>

<span data-ttu-id="3b6b5-138">Um die beste Leistung zu erzielen, wird eine WAV-Datei mit den Werten 16 kHz, Mono, 16 Bit empfohlen.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-138">For the best performance of wave files, a 16 kHz, mono, 16-bit Wave file is recommended.</span></span>

</div>

<div>

## <a name="supported-windows-media-audio-file-formats"></a><span data-ttu-id="3b6b5-139">Unterstützte WMA-Dateiformate</span><span class="sxs-lookup"><span data-stu-id="3b6b5-139">Supported Windows Media Audio File Formats</span></span>

<span data-ttu-id="3b6b5-140">Bei Verwendung einer WMA-Datei sollten Sie niedrige Bitraten verwenden und die Leistung Ihres Systems überprüfen, wenn dieses ausgelastet ist.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-140">If you use a Windows Media audio file, consider using low bit rates, and verify the performance of your system under load.</span></span>

<span data-ttu-id="3b6b5-141">Sie können Microsoft Expression Encoder 4 verwenden, um eine Datei in das WMA-Format zu konvertieren.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-141">You can use the Microsoft Expression Encoder 4 to convert a file to the Windows Media Audio format.</span></span> <span data-ttu-id="3b6b5-142">Informationen zum Herunterladen von Expression Encoder 4 finden Sie unter [https://go.microsoft.com/fwlink/p/?linkId=202843](https://go.microsoft.com/fwlink/p/?linkid=202843) .</span><span class="sxs-lookup"><span data-stu-id="3b6b5-142">To download Expression Encoder 4, see [https://go.microsoft.com/fwlink/p/?linkId=202843](https://go.microsoft.com/fwlink/p/?linkid=202843).</span></span>

</div>

</div>

<div>

## <a name="response-group-configuration-tool-requirements"></a><span data-ttu-id="3b6b5-143">Anforderungen des Konfigurationstools für Reaktionsgruppen</span><span class="sxs-lookup"><span data-stu-id="3b6b5-143">Response Group Configuration Tool Requirements</span></span>

<span data-ttu-id="3b6b5-144">Das Reaktionsgruppen-Konfigurations Tool unterstützt die in der folgenden Tabelle beschriebenen Kombinationen aus Betriebssystemen und Webbrowsern.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-144">The Response Group Configuration Tool supports the combinations of operating systems and web browsers described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3b6b5-p107">32-Bit- und 64-Bit-Versionen des jeweiligen Betriebssystems werden unterstützt. Für Internet Explorer werden nur 32-Bit-Versionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-p107">32-bit or 64-bit versions of the operating systems are supported. Only 32-bit versions of Internet Explorer are supported.</span></span>



</div>

### <a name="supported-operating-systems-and-web-browsers"></a><span data-ttu-id="3b6b5-147">Unterstützte Betriebssysteme und Webbrowser</span><span class="sxs-lookup"><span data-stu-id="3b6b5-147">Supported Operating Systems and Web Browsers</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b6b5-148">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="3b6b5-148">Operating system</span></span></th>
<th><span data-ttu-id="3b6b5-149">Webbrowser</span><span class="sxs-lookup"><span data-stu-id="3b6b5-149">Web browser</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b6b5-150">Windows Vista mit Service Pack (SP) 2</span><span class="sxs-lookup"><span data-stu-id="3b6b5-150">Windows Vista with Service Pack (SP) 2</span></span></p></td>
<td><p><span data-ttu-id="3b6b5-151">Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="3b6b5-151">Internet Explorer 7</span></span></p>
<p><span data-ttu-id="3b6b5-152">Internet Explorer 8 (einheitlicher Modus)</span><span class="sxs-lookup"><span data-stu-id="3b6b5-152">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="3b6b5-153">Internet Explorer 9 (einheitlicher Modus)</span><span class="sxs-lookup"><span data-stu-id="3b6b5-153">Internet Explorer 9 (native mode)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b6b5-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3b6b5-154">Windows 7</span></span></p>
<p><span data-ttu-id="3b6b5-155">Windows 7 mit Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="3b6b5-155">Windows 7 with Service Pack 1</span></span></p></td>
<td><p><span data-ttu-id="3b6b5-156">Internet Explorer 8 (einheitlicher Modus)</span><span class="sxs-lookup"><span data-stu-id="3b6b5-156">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="3b6b5-157">Internet Explorer 9 (einheitlicher Modus)</span><span class="sxs-lookup"><span data-stu-id="3b6b5-157">Internet Explorer 9 (native mode)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b6b5-158">Windows Server 2008 mit Service Pack 2</span><span class="sxs-lookup"><span data-stu-id="3b6b5-158">Windows Server 2008 with Service Pack 2</span></span></p></td>
<td><p><span data-ttu-id="3b6b5-159">Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="3b6b5-159">Internet Explorer 7</span></span></p>
<p><span data-ttu-id="3b6b5-160">Internet Explorer 8 (einheitlicher Modus)</span><span class="sxs-lookup"><span data-stu-id="3b6b5-160">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="3b6b5-161">Internet Explorer 9 (einheitlicher Modus)</span><span class="sxs-lookup"><span data-stu-id="3b6b5-161">Internet Explorer 9 (native mode)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b6b5-162">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3b6b5-162">Windows Server 2008 R2</span></span></p>
<p><span data-ttu-id="3b6b5-163">Windows Server 2008 R2 mit Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="3b6b5-163">Windows Server 2008 R2 with Service Pack 1</span></span></p></td>
<td><p><span data-ttu-id="3b6b5-164">Internet Explorer 8 (einheitlicher Modus)</span><span class="sxs-lookup"><span data-stu-id="3b6b5-164">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="3b6b5-165">Internet Explorer 9 (einheitlicher Modus)</span><span class="sxs-lookup"><span data-stu-id="3b6b5-165">Internet Explorer 9 (native mode)</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="response-group-agent-console"></a><span data-ttu-id="3b6b5-166">Agentkonsole für Reaktionsgruppen</span><span class="sxs-lookup"><span data-stu-id="3b6b5-166">Response Group Agent Console</span></span>

<span data-ttu-id="3b6b5-167">Die Agentkonsole unterstützt die in der folgenden Tabelle aufgeführten Kombinationen aus Betriebssystemen und Webbrowsern.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-167">The agent console supports the combinations of operating systems and web browsers described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3b6b5-p108">32-Bit- und 64-Bit-Versionen des jeweiligen Betriebssystems werden unterstützt. Für Internet Explorer werden nur 32-Bit-Versionen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="3b6b5-p108">32-bit or 64-bit versions of the operating systems are supported. Only 32-bit versions of Internet Explorer are supported.</span></span>



</div>

### <a name="supported-operating-systems-and-web-browsers"></a><span data-ttu-id="3b6b5-170">Unterstützte Betriebssysteme und Webbrowser</span><span class="sxs-lookup"><span data-stu-id="3b6b5-170">Supported Operating Systems and Web Browsers</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b6b5-171">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="3b6b5-171">Operating system</span></span></th>
<th><span data-ttu-id="3b6b5-172">Webbrowser</span><span class="sxs-lookup"><span data-stu-id="3b6b5-172">Web browser</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b6b5-173">Windows Vista mit Service Pack (SP) 2</span><span class="sxs-lookup"><span data-stu-id="3b6b5-173">Windows Vista with Service Pack (SP) 2</span></span></p></td>
<td><p><span data-ttu-id="3b6b5-174">Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="3b6b5-174">Internet Explorer 7</span></span></p>
<p><span data-ttu-id="3b6b5-175">Internet Explorer 8 (einheitlicher Modus)</span><span class="sxs-lookup"><span data-stu-id="3b6b5-175">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="3b6b5-176">Internet Explorer 9 (einheitlicher Modus)</span><span class="sxs-lookup"><span data-stu-id="3b6b5-176">Internet Explorer 9 (native mode)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b6b5-177">Windows 7</span><span class="sxs-lookup"><span data-stu-id="3b6b5-177">Windows 7</span></span></p>
<p><span data-ttu-id="3b6b5-178">Windows 7 mit Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="3b6b5-178">Windows 7 with Service Pack 1</span></span></p></td>
<td><p><span data-ttu-id="3b6b5-179">Internet Explorer 8 (einheitlicher Modus)</span><span class="sxs-lookup"><span data-stu-id="3b6b5-179">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="3b6b5-180">Internet Explorer 9 (einheitlicher Modus)</span><span class="sxs-lookup"><span data-stu-id="3b6b5-180">Internet Explorer 9 (native mode)</span></span></p>
<p><span data-ttu-id="3b6b5-181">Firefox 10.0</span><span class="sxs-lookup"><span data-stu-id="3b6b5-181">Firefox 10.0</span></span></p>
<p><span data-ttu-id="3b6b5-182">Chrome 18.0</span><span class="sxs-lookup"><span data-stu-id="3b6b5-182">Chrome 18.0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b6b5-183">Windows Server 2008 mit Service Pack 2</span><span class="sxs-lookup"><span data-stu-id="3b6b5-183">Windows Server 2008 with Service Pack 2</span></span></p></td>
<td><p><span data-ttu-id="3b6b5-184">Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="3b6b5-184">Internet Explorer 7</span></span></p>
<p><span data-ttu-id="3b6b5-185">Internet Explorer 8 (einheitlicher Modus)</span><span class="sxs-lookup"><span data-stu-id="3b6b5-185">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="3b6b5-186">Internet Explorer 9 (einheitlicher Modus)</span><span class="sxs-lookup"><span data-stu-id="3b6b5-186">Internet Explorer 9 (native mode)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b6b5-187">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="3b6b5-187">Windows Server 2008 R2</span></span></p>
<p><span data-ttu-id="3b6b5-188">Windows Server 2008 R2 mit Service Pack 1</span><span class="sxs-lookup"><span data-stu-id="3b6b5-188">Windows Server 2008 R2 with Service Pack 1</span></span></p></td>
<td><p><span data-ttu-id="3b6b5-189">Internet Explorer 8 (einheitlicher Modus)</span><span class="sxs-lookup"><span data-stu-id="3b6b5-189">Internet Explorer 8 (native mode)</span></span></p>
<p><span data-ttu-id="3b6b5-190">Internet Explorer 9 (einheitlicher Modus)</span><span class="sxs-lookup"><span data-stu-id="3b6b5-190">Internet Explorer 9 (native mode)</span></span></p>
<p><span data-ttu-id="3b6b5-191">Firefox 10.0</span><span class="sxs-lookup"><span data-stu-id="3b6b5-191">Firefox 10.0</span></span></p>
<p><span data-ttu-id="3b6b5-192">Chrome 18.0</span><span class="sxs-lookup"><span data-stu-id="3b6b5-192">Chrome 18.0</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
</tr>
</tbody>
</table><span data-ttu-id="3b6b5-193">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3b6b5-193">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

