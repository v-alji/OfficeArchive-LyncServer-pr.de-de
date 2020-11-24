---
title: 'Lync Server 2013: Technische Anforderungen für Konferenzen'
description: Technische Anforderungen von lync Server 2013 für Konferenzen
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for conferencing
ms:assetid: 3c0d89e1-53e6-46d7-bf8c-491260b292ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425889(v=OCS.15)
ms:contentKeyID: 48183923
ms.date: 06/26/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b3b787d84288d789cd0d824081439004f19327e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394678"
---
# <a name="technical-requirements-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="fbeb7-103">Technische Anforderungen für Konferenzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fbeb7-103">Technical requirements for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fbeb7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fbeb7-104">

<span> </span></span></span>

<span data-ttu-id="fbeb7-105">_**Letztes Änderungsdatum des Themas:** 2014-06-25_</span><span class="sxs-lookup"><span data-stu-id="fbeb7-105">_**Topic Last Modified:** 2014-06-25_</span></span>

<span data-ttu-id="fbeb7-106">Für lync Server 2013 können Einwahlkonferenzen, A/V-Konferenzen, Sofortnachrichten (im)-Konferenzen und Webkonferenzfunktionen immer auf Front-End-Servern ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-106">For Lync Server 2013, dial-in conferencing, A/V conferencing, instant messaging (IM) conferencing and web conferencing capabilities always run on Front End Servers.</span></span>

<span data-ttu-id="fbeb7-107">In diesem Abschnitt werden die Hardware-und Softwareanforderungen für diese Server sowie die unterstützte Zusammensetzung erläutert.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-107">This section details the hardware and software requirements for these servers, along with the supported collocation.</span></span>

<span data-ttu-id="fbeb7-108">Einwahlkonferenzen sind eine Funktion, die eine Vielzahl von Komponenten umfasst.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-108">Dial-in conferencing is a feature that includes a variety of components.</span></span> <span data-ttu-id="fbeb7-109">Einige der Komponenten gelten speziell für Einwahlkonferenzen und einige sind Enterprise-VoIP-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-109">Some of the components are specific to dial-in conferencing and some are Enterprise Voice components.</span></span> <span data-ttu-id="fbeb7-110">In diesem Abschnitt werden die Anforderungen für die Komponenten beschrieben, die für Einwahlkonferenzen spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-110">This section describes the requirements for the components that are specific to dial-in conferencing.</span></span> <span data-ttu-id="fbeb7-111">Details zu den Anforderungen des Vermittlungsservers und des PSTN-Gateways (Public Switched Telephone Network) finden Sie in der Planning-Dokumentation unter [Mediation Server-Komponente in lync Server 2013](lync-server-2013-mediation-server-component.md) und [Komponenten und Topologien für Mediation Server in lync Server 2013](lync-server-2013-components-and-topologies-for-mediation-server.md) .</span><span class="sxs-lookup"><span data-stu-id="fbeb7-111">For details about Mediation Server and public switched telephone network (PSTN) gateway requirements, see [Mediation Server component in Lync Server 2013](lync-server-2013-mediation-server-component.md) and [Components and topologies for Mediation Server in Lync Server 2013](lync-server-2013-components-and-topologies-for-mediation-server.md) in the Planning documentation.</span></span>

<div>

## <a name="hardware-requirements"></a><span data-ttu-id="fbeb7-112">Hardware Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbeb7-112">Hardware Requirements</span></span>

<span data-ttu-id="fbeb7-113">Da Webkonferenzen und A/V-Konferenzen mit dem Front-End-Server kombiniert werden, sind die Server Hardwareanforderungen identisch mit den Front-End-Servern.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-113">Because web conferencing and A/V conferencing are collocated with the Front End Server, the server hardware requirements are the same as for the Front End Servers.</span></span> <span data-ttu-id="fbeb7-114">Details zu den Hardwareanforderungen finden Sie unter [Server Hardwareplattformen für lync Server 2013](lync-server-2013-server-hardware-platforms.md) in der Dokumentation zur Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-114">For details about hardware requirements, see [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) in the Supportability documentation.</span></span> <span data-ttu-id="fbeb7-115">Die folgenden für Einwahlkonferenzen erforderlichen Komponenten haben auch die gleichen Hardwareanforderungen wie Front-End-Server:</span><span class="sxs-lookup"><span data-stu-id="fbeb7-115">The following components required for dial-in conferencing also have the same hardware requirements as Front End Servers:</span></span>

  - <span data-ttu-id="fbeb7-116">Anwendungsdienst</span><span class="sxs-lookup"><span data-stu-id="fbeb7-116">Application service</span></span>

  - <span data-ttu-id="fbeb7-117">Konferenzzentrale</span><span class="sxs-lookup"><span data-stu-id="fbeb7-117">Conferencing Attendant application</span></span>

  - <span data-ttu-id="fbeb7-118">Konferenzankündigungsanwendung</span><span class="sxs-lookup"><span data-stu-id="fbeb7-118">Conferencing Announcement application</span></span>

<span data-ttu-id="fbeb7-119">Die Hardwareanforderungen für den Front-End-Server entsprechen denen für viele andere Serverrollen in lync Server 2013, die in der folgenden Tabelle beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-119">The hardware requirements for Front End Server are the same as for many other server roles in Lync Server 2013 are outlined in the following table.</span></span>

</div>

<div>

## <a name="software-requirements"></a><span data-ttu-id="fbeb7-120">Software Anforderungen</span><span class="sxs-lookup"><span data-stu-id="fbeb7-120">Software Requirements</span></span>

<span data-ttu-id="fbeb7-121">Da Webkonferenzen und A/V-Konferenzen mit dem Front-End-Server kombiniert werden, sind die Server Softwareanforderungen identisch mit den Front-End-Servern.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-121">Because web conferencing and A/V conferencing are collocated with the Front End Server, the server software requirements are the same as for the Front End Servers.</span></span> <span data-ttu-id="fbeb7-122">Ausführliche Informationen zu den Softwareanforderungen finden Sie unter unter [Stützung von Server-und Tools-Betriebssystemen in lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in der Dokumentation zur Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-122">For details about software requirements, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="fbeb7-123">Für Webkonferenzen erfordert lync Server 2013 auch Office Web Apps und den Office Web Apps-Server (vormals als "The-Server" bezeichnet), um PowerPoint-Präsentationen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-123">For web conferencing, Lync Server 2013 also requires Office Web Apps and the Office Web Apps Server (formerly known as WAC Server) to handle PowerPoint presentations.</span></span> <span data-ttu-id="fbeb7-124">Ausführliche Informationen finden Sie unter [Konfigurieren der Integration in Office Web Apps Server und lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="fbeb7-124">For details, see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

<span data-ttu-id="fbeb7-125">Für Einwahlkonferenzen, Anwendungsdienst, Konferenz Aufsichts Anwendung und Konferenz Ankündigungs Anwendung gelten dieselben Betriebssystemanforderungen wie für Front-End-Server.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-125">For dial-in conferencing, Application service, Conferencing Attendant application, and Conferencing Announcement application have the same operating system requirements as Front End Servers.</span></span> <span data-ttu-id="fbeb7-126">Ausführliche Informationen zu den Softwareanforderungen finden Sie unter unter [Stützung von Server-und Tools-Betriebssystemen in lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in der Dokumentation zur Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-126">For details about software requirements, see [Server and tools operating system support in Lync Server 2013](lync-server-2013-server-and-tools-operating-system-support.md) in the Supportability documentation.</span></span>

<span data-ttu-id="fbeb7-127">Die Anwendung für die Conferencing Attendant-Anwendung und die Konferenzankündigung erfordern, dass Windows Media Format Runtime auf Front-End-Servern installiert ist.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-127">Conferencing Attendant application and Conferencing Announcement application require that Windows Media Format Runtime is installed on Front End Servers.</span></span> <span data-ttu-id="fbeb7-128">Die Windows Media-Format Laufzeit ist erforderlich, um WMA-Dateien (Windows Media Audio) wiederzugeben, die für Musik in Wartestellung, aufgezeichnete Namen und Eingabeaufforderungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-128">The Windows Media Format Runtime is required to play Windows Media audio (WMA) files that are used for music on hold, recorded names, and prompts.</span></span> <span data-ttu-id="fbeb7-129">Mit Ausnahme von Windows Server 2012 und Windows Server 2012 R2 wird die Windows Media-Format Laufzeit automatisch als Teil der Windows-Desktop Umgebung installiert, wenn Sie Setup ausführen, aber möglicherweise müssen Sie den Computer neu starten.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-129">Except for Windows Server 2012 and Windows Server 2012 R2, the Windows Media Format Runtime is installed automatically as part of the Windows Desktop Experience when you run Setup, but you might need to restart the computer.</span></span> <span data-ttu-id="fbeb7-130">Daher empfiehlt es sich, die Installation als Teil der Windows-Desktop Umgebung zu installieren, die Windows Media Format Runtime umfasst, bevor Sie Setup ausführen.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-130">Therefore, we recommend that you install as part of the Windows Desktop Experience, which includes Windows Media Format Runtime before you run Setup.</span></span> <span data-ttu-id="fbeb7-131">Für Windows Server 2012 und Windows Server 2012 R2 ist Microsoft Media Foundation erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-131">Windows Server 2012 and Windows Server 2012 R2 requires Microsoft Media Foundation.</span></span>

</div>

<div>

## <a name="port-requirements-for-dial-in-conferencing"></a><span data-ttu-id="fbeb7-132">Port Anforderungen für Einwahlkonferenzen</span><span class="sxs-lookup"><span data-stu-id="fbeb7-132">Port Requirements for dial-in conferencing</span></span>

<span data-ttu-id="fbeb7-133">In der folgenden Tabelle werden die Ports beschrieben, die von Einwahlkonferenzen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-133">The following table describes the ports that are used by dial-in conferencing.</span></span> <span data-ttu-id="fbeb7-134">Wenn Sie ein Lastenausgleichsmodul verwenden, stellen Sie sicher, dass das Load Balancer für die Ports konfiguriert ist, die von allen Anwendungen verwendet werden, die im Pool ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-134">If you use a load balancer, ensure that the load balancer is configured for the ports used by any applications that will run in the pool.</span></span>

<span data-ttu-id="fbeb7-135">Diese Ports sind Standardeinstellungen, die Sie mit dem Cmdlet **Set-CsApplicationServer** ändern können.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-135">These ports are default settings that you can change by using the **Set-CsApplicationServer** cmdlet.</span></span> <span data-ttu-id="fbeb7-136">Details zu diesem Cmdlet finden Sie in der Dokumentation zur lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-136">For details about this cmdlet, see the Lync Server Management Shell documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fbeb7-137">Alle Instanzen der gleichen Anwendung in einem Pool verwenden denselben SIP-Abhör-Port.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-137">All instances of the same application in a pool use the same SIP listening port.</span></span>



</div>

### <a name="ports-used-by-dial-in-conferencing"></a><span data-ttu-id="fbeb7-138">Ports, die von Einwahlkonferenzen verwendet werden</span><span class="sxs-lookup"><span data-stu-id="fbeb7-138">Ports used by dial-in conferencing</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fbeb7-139">Portnummer</span><span class="sxs-lookup"><span data-stu-id="fbeb7-139">Port number</span></span></th>
<th><span data-ttu-id="fbeb7-140">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="fbeb7-140">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fbeb7-141">5072</span><span class="sxs-lookup"><span data-stu-id="fbeb7-141">5072</span></span></p></td>
<td><p><span data-ttu-id="fbeb7-142">Wird von der Konferenz Aufsichts Anwendung für SIP-Überwachungsanforderungen verwendet</span><span class="sxs-lookup"><span data-stu-id="fbeb7-142">Used by Conferencing Attendant application for SIP listening requests</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbeb7-143">5073</span><span class="sxs-lookup"><span data-stu-id="fbeb7-143">5073</span></span></p></td>
<td><p><span data-ttu-id="fbeb7-144">Wird von der Konferenz Ankündigungs Anwendung für SIP-Überwachungsanforderungen verwendet</span><span class="sxs-lookup"><span data-stu-id="fbeb7-144">Used by Conferencing Announcement application for SIP listening requests</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="supported-clients-for-dial-in-conferencing"></a><span data-ttu-id="fbeb7-145">Unterstützte Clients für Einwahlkonferenzen</span><span class="sxs-lookup"><span data-stu-id="fbeb7-145">Supported Clients for Dial-In Conferencing</span></span>

<span data-ttu-id="fbeb7-146">Sie können den folgenden Client verwenden, um lokale Konferenzen zu planen, die Einwahlzugriff unterstützen:</span><span class="sxs-lookup"><span data-stu-id="fbeb7-146">You can use the following client to schedule on-premises conferences that support dial-in access:</span></span>

  - <span data-ttu-id="fbeb7-147">Online Besprechungs-Add-in für lync 2013 (automatisch installiert, wenn Sie lync 2013 oder Teilnehmer installieren)</span><span class="sxs-lookup"><span data-stu-id="fbeb7-147">Online Meeting Add-in for Lync 2013 (installed automatically when you install Lync 2013 or Attendee)</span></span>

</div>

<div>

## <a name="dial-in-conferencing-settings-page-requirements"></a><span data-ttu-id="fbeb7-148">Einstellungen für Einwahlkonferenzen, Seitenanforderungen</span><span class="sxs-lookup"><span data-stu-id="fbeb7-148">Dial-in Conferencing Settings page Requirements</span></span>

<span data-ttu-id="fbeb7-149">Auf der Seite Einstellungen für Einwahlkonferenzen werden die in der folgenden Tabelle beschriebenen Kombinationen aus Betriebssystemen und Webbrowsern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-149">The Dial-in Conferencing Settings page supports the combinations of operating systems and web browsers described in the following table.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="fbeb7-150">32-Bit-und 64-Bit-Versionen der Betriebssysteme werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-150">32-bit and 64-bit versions of the operating systems are supported.</span></span>



</div>

### <a name="supported-operating-systems-and-web-browsers"></a><span data-ttu-id="fbeb7-151">Unterstützte Betriebssysteme und Webbrowser</span><span class="sxs-lookup"><span data-stu-id="fbeb7-151">Supported Operating Systems and Web Browsers</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fbeb7-152">Betriebssystem</span><span class="sxs-lookup"><span data-stu-id="fbeb7-152">Operating system</span></span></th>
<th><span data-ttu-id="fbeb7-153">Webbrowser</span><span class="sxs-lookup"><span data-stu-id="fbeb7-153">Web browser</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fbeb7-154">Windows 7</span><span class="sxs-lookup"><span data-stu-id="fbeb7-154">Windows 7</span></span></p></td>
<td><p><span data-ttu-id="fbeb7-155">Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="fbeb7-155">Internet Explorer 9</span></span></p>
<p><span data-ttu-id="fbeb7-156">Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="fbeb7-156">Internet Explorer 8</span></span></p>
<p><span data-ttu-id="fbeb7-157">Firefox</span><span class="sxs-lookup"><span data-stu-id="fbeb7-157">Firefox</span></span></p></td>
</tr>
<tr class="even">
<td> </td>
<td> </td>
</tr>
<tr class="odd">
<td> </td>
<td> </td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fbeb7-158">Windows Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="fbeb7-158">Windows Server 2008 R2</span></span></p></td>
<td><p><span data-ttu-id="fbeb7-159">Internet Explorer 9</span><span class="sxs-lookup"><span data-stu-id="fbeb7-159">Internet Explorer 9</span></span></p>
<p><span data-ttu-id="fbeb7-160">Internet Explorer 8</span><span class="sxs-lookup"><span data-stu-id="fbeb7-160">Internet Explorer 8</span></span></p>
<p><span data-ttu-id="fbeb7-161">Internet Explorer 7</span><span class="sxs-lookup"><span data-stu-id="fbeb7-161">Internet Explorer 7</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fbeb7-162">Mac OS</span><span class="sxs-lookup"><span data-stu-id="fbeb7-162">Mac OS</span></span></p></td>
<td><p><span data-ttu-id="fbeb7-163">Firefox</span><span class="sxs-lookup"><span data-stu-id="fbeb7-163">Firefox</span></span></p>
<p><span data-ttu-id="fbeb7-164">Safari</span><span class="sxs-lookup"><span data-stu-id="fbeb7-164">Safari</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="audio-file-requirements-for-dial-in-conferencing"></a><span data-ttu-id="fbeb7-165">Audio-Dateianforderungen für Einwahlkonferenzen</span><span class="sxs-lookup"><span data-stu-id="fbeb7-165">Audio File Requirements for dial-in conferencing</span></span>

<span data-ttu-id="fbeb7-166">Lync Server 2013 unterstützt keine Anpassung von Sprachansagen und Musik für Einwahlkonferenzen.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-166">Lync Server 2013 does not support customization of voice prompts and music for dial-in conferencing.</span></span> <span data-ttu-id="fbeb7-167">Wenn Sie jedoch eine starke geschäftliche Anforderung haben, die erfordert, dass Sie die standardmäßigen Audiodateien ändern, lesen Sie den Microsoft Knowledge Base-Artikel 961177, [Anleitung zum Anpassen von Sprachansagen oder Musikdateien für Einwahlkonferenzen in Microsoft Office Communications Server 2007 R2](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=961177).</span><span class="sxs-lookup"><span data-stu-id="fbeb7-167">However, if you have a strong business need that requires you to change the default audio files, see Microsoft Knowledge Base article 961177, [How to customize voice prompts or music files for dial-in audio conferencing in Microsoft Office Communications Server 2007 R2](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=961177).</span></span>

<span data-ttu-id="fbeb7-168">Sie können auch das Verwaltungsdienstprogramm für [benutzerdefinierte Sprachansagen der Microsoft lync Server-Konferenzzentrale](https://go.microsoft.com/fwlink/p/?linkid=396880) verwenden, das es Administratoren ermöglicht, die standardmäßigen Sprachaufforderungen zu ersetzen, die verwendet werden, wenn ein Telefon Anrufer eine lync-Besprechung mit benutzerdefinierten Ansagen annimmt, um eine andere Besprechungs Eingabe zu ermöglichen</span><span class="sxs-lookup"><span data-stu-id="fbeb7-168">You can also use the [Microsoft Lync Server Conferencing Attendant Custom Voice Prompts](https://go.microsoft.com/fwlink/p/?linkid=396880) management utility, which enables administrators to replace the default voice prompts used when a phone caller joins a Lync meeting with custom prompts to provide a different meeting entry experience.</span></span> <span data-ttu-id="fbeb7-169">Die benutzerdefinierten Sprachansagen können auf einem Server mit lync Server 2010 oder lync Server 2013, entweder Enterprise oder Standard Edition, installiert werden.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-169">The custom voice prompts can be installed on a server that is running Lync Server 2010 or Lync Server 2013, either Enterprise or Standard Edition.</span></span>

<span data-ttu-id="fbeb7-170">Anwendung für die Conferencing Attendant-Anwendung und Konferenzankündigung gelten für die folgenden Voraussetzungen für Musik in Wartestellung, aufgezeichnete Namen und Audio-Ansagedateien:</span><span class="sxs-lookup"><span data-stu-id="fbeb7-170">Conferencing Attendant application and Conferencing Announcement application have the following requirements for music on hold, recorded name, and audio prompt files:</span></span>

  - <span data-ttu-id="fbeb7-171">WMA-Dateiformat (Windows Media Audio)</span><span class="sxs-lookup"><span data-stu-id="fbeb7-171">Windows Media Audio (WMA) file format</span></span>

  - <span data-ttu-id="fbeb7-172">16-Bit mono</span><span class="sxs-lookup"><span data-stu-id="fbeb7-172">16-bit mono</span></span>

  - <span data-ttu-id="fbeb7-173">Konstante Bitrate (Constant Bit Rate), 48 KBit/s, 2 Durchläufe</span><span class="sxs-lookup"><span data-stu-id="fbeb7-173">48 kbps 2-pass CBR (constant bit rate)</span></span>

  - <span data-ttu-id="fbeb7-174">Sprachpegel: -24 dB</span><span class="sxs-lookup"><span data-stu-id="fbeb7-174">Speech level at -24DB</span></span>

</div>

<div>

## <a name="user-requirements-for-dial-in-conferencing"></a><span data-ttu-id="fbeb7-175">Benutzeranforderungen für Einwahlkonferenzen</span><span class="sxs-lookup"><span data-stu-id="fbeb7-175">User Requirements for Dial-In Conferencing</span></span>

<span data-ttu-id="fbeb7-176">Dem Konto eines Einwahlkonferenzbenutzers muss eine eindeutige Rufnummer oder Durchwahl zugewiesen sein.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-176">Dial-in conferencing users must have a unique phone number or extension assigned to their account.</span></span> <span data-ttu-id="fbeb7-177">Diese Anforderung unterstützt die Authentifizierung während der Einwahlkonferenz.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-177">This requirement supports authentication during dial-in conferencing.</span></span> <span data-ttu-id="fbeb7-178">Enterprise-Benutzer (also Benutzer mit Anmeldeinformationen für Active Directory-Domänendienste und lync-Server Konten in Ihrer Organisation) geben Ihre Telefonnummer (oder Durchwahl) und eine persönliche Identifikationsnummer (PIN) ein, um sich als authentifizierter Benutzer in Konferenzen einzuwählen.</span><span class="sxs-lookup"><span data-stu-id="fbeb7-178">Enterprise users (that is, users who have Active Directory Domain Services credentials and Lync Server accounts within your organization) enter their phone number (or extension) and a personal identification number (PIN) to dial in to conferences as an authenticated user.</span></span>

<span data-ttu-id="fbeb7-179"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fbeb7-179"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

