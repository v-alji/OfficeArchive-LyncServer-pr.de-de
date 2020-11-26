---
title: 'Lync Server 2013: Zusätzliche Softwareanforderungen'
description: 'Lync Server 2013: zusätzliche Softwareanforderungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Additional software requirements
ms:assetid: 87b318e3-03ae-41f7-af5e-29bb294f6af0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398686(v=OCS.15)
ms:contentKeyID: 48184731
ms.date: 12/09/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fbc36f23a2246c9d653e47954064182c756f0dff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443153"
---
# <a name="additional-software-requirements-for-lync-server-2013"></a><span data-ttu-id="3e7aa-103">Zusätzliche Softwareanforderungen für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e7aa-103">Additional software requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3e7aa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3e7aa-104">

<span> </span></span></span>

<span data-ttu-id="3e7aa-105">_**Letztes Änderungsdatum des Themas:** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="3e7aa-105">_**Topic Last Modified:** 2016-12-08_</span></span>

<span data-ttu-id="3e7aa-106">Zusätzlich zu den Hardware-und Betriebssystemanforderungen für Serverplattformen erfordert lync Server 2013 die Installation zusätzlicher Software auf den von Ihnen bereitgestellten Servern.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-106">In addition to the hardware and operating system requirements for server platforms, Lync Server 2013 requires the installation of additional software on the servers that you deploy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3e7aa-107">Details zu den Plattformanforderungen für Server mit lync Server finden Sie unter <A href="lync-server-2013-server-hardware-platforms.md">Server-Hardwareplattformen für lync Server 2013</A> und <A href="lync-server-2013-server-and-tools-operating-system-support.md">Server-und Tools-Betriebssystemunterstützung in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-107">For details about the platform requirements for servers running Lync Server, see <A href="lync-server-2013-server-hardware-platforms.md">Server hardware platforms for Lync Server 2013</A> and <A href="lync-server-2013-server-and-tools-operating-system-support.md">Server and tools operating system support in Lync Server 2013</A>.</span></span> <span data-ttu-id="3e7aa-108">Ausführliche Informationen zu den Systemanforderungen für Clientcomputer und Geräte finden Sie unter <A href="lync-server-2013-planning-for-clients-and-devices.md">Planen von Clients und Geräten in lync Server 2013</A> in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-108">For details about system requirements for client computers and devices, see <A href="lync-server-2013-planning-for-clients-and-devices.md">Planning for clients and devices in Lync Server 2013</A> in the Planning documentation.</span></span> <span data-ttu-id="3e7aa-109">Details zu den Softwareanforderungen für Verwaltungstools finden Sie unter <A href="lync-server-2013-administrative-tools-software-requirements.md">Softwareanforderungen für Verwaltungstools in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-109">For details about software requirements for administrative tools, see <A href="lync-server-2013-administrative-tools-software-requirements.md">Administrative tools software requirements in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="additional-software-necessary-for-all-internal-server-roles"></a><span data-ttu-id="3e7aa-110">Zusätzliche Software, die für alle internen Server Rollen erforderlich ist</span><span class="sxs-lookup"><span data-stu-id="3e7aa-110">Additional Software Necessary for All Internal Server Roles</span></span>

<span data-ttu-id="3e7aa-111">Dieser Abschnitt listet Software auf, die für alle internen Serverrollen erforderlich ist, bei denen es sich um alle lync Server-Serverrollen mit Ausnahme von Edgeserver handelt.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-111">This section lists software necessary on all internal server roles, which are all Lync Server server roles except for Edge Server.</span></span> <span data-ttu-id="3e7aa-112">Die Anforderungen für die Edgeserver und Edge-Pools sind weiter unten in diesem Thema unter **zusätzliche Software für Edgeserver** aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-112">The requirements for the Edge Servers and Edge pools are listed later in this topic under **Additional Software for Edge Servers**.</span></span>

</div>

<div>

## <a name="windows-powershell-30"></a><span data-ttu-id="3e7aa-113">Windows PowerShell 3.0</span><span class="sxs-lookup"><span data-stu-id="3e7aa-113">Windows PowerShell 3.0</span></span>

<span data-ttu-id="3e7aa-114">Auf jedem Server, auf dem lync Server 2013 ausgeführt wird, muss die richtige Version von Windows PowerShell 3,0 installiert sein.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-114">Each server running Lync Server 2013 must have the correct release of Windows PowerShell 3.0 installed.</span></span> <span data-ttu-id="3e7aa-115">Ausführliche Informationen finden Sie unter [Installieren von Windows PowerShell 3,0 für lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="3e7aa-115">For details, see [Installing Windows PowerShell 3.0 for Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span></span>

</div>

<div>

## <a name="microsoft-net-framework-45"></a><span data-ttu-id="3e7aa-116">Microsoft .NET Framework 4.5</span><span class="sxs-lookup"><span data-stu-id="3e7aa-116">Microsoft .NET Framework 4.5</span></span>

<span data-ttu-id="3e7aa-117">Lync Server erfordert Microsoft .NET Framework 4,5 auf allen internen Server Rollen und auf allen Computern, auf denen Sie die lync Server-Verwaltungstools oder Microsoft lync Server 2013, Planungs Tool, ausführen werden.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-117">Lync Server requires Microsoft .NET Framework 4.5 on all internal server roles and on any computer where you will run the Lync Server administrative tools or Microsoft Lync Server 2013, Planning Tool.</span></span> <span data-ttu-id="3e7aa-118">Bei lync Server 2013 müssen Sie die 64-Bit-Version von Microsoft .NET Framework 4,5 auf dem Server manuell installieren, bevor Sie lync Server 2013 installieren.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-118">For Lync Server 2013, you must manually install the 64-bit edition of Microsoft .NET Framework 4.5 on the server prior to installing Lync Server 2013.</span></span> <span data-ttu-id="3e7aa-119">Wenn Sie die Datei manuell installieren möchten, laden Sie das Microsoft .NET 4,5-Framework aus dem Microsoft Download Center unter [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span><span class="sxs-lookup"><span data-stu-id="3e7aa-119">To manually install it, download the Microsoft .NET 4.5 Framework from the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span></span>

<div>

## <a name="installing-microsoft-net-framework-45-on-servers-running-windows-server-2012"></a><span data-ttu-id="3e7aa-120">Installieren von Microsoft .NET Framework 4,5 auf Servern mit Windows Server 2012</span><span class="sxs-lookup"><span data-stu-id="3e7aa-120">Installing Microsoft .NET Framework 4.5 on Servers Running Windows Server 2012</span></span>

<span data-ttu-id="3e7aa-121">Wenn Sie Microsoft .NET Framework 4,5 auf Servern installieren, auf denen lync Server 2013 und Windows Server 2012 ausgeführt wird, müssen Sie einen weiteren Schritt ausführen.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-121">When you install Microsoft .NET Framework 4.5 on servers that will run Lync Server 2013 and Windows Server 2012, you must perform one additional step.</span></span> <span data-ttu-id="3e7aa-122">Verwenden Sie nach der Installation von .NET Framework 4,5 den Server-Manager, um die HTTP-Aktivierung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-122">After .NET Framework 4.5 is installed, use Server Manager to install HTTP Activation.</span></span>

<span data-ttu-id="3e7aa-123">**So installieren Sie die .NET 4,5-HTTP-Aktivierung unter Windows Server 2012**</span><span class="sxs-lookup"><span data-stu-id="3e7aa-123">**To Install .NET 4.5 HTTP Activation on Windows Server 2012**</span></span>

1.  <span data-ttu-id="3e7aa-124">Klicken Sie im **Startmenü** auf **Programme** und dann auf **Verwaltung**, und klicken Sie dann auf **Server-Manager**.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-124">From the **Start** menu, click **Programs**, then click **Administrative Tools**, then click **Server Manager**.</span></span>

2.  <span data-ttu-id="3e7aa-125">Wählen Sie im Server-Manager unter **Zusammenfassung der Features** die Option **Features hinzufügen** aus.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-125">In Server Manager, under **Features Summary**, choose **Add Features**.</span></span>

3.  <span data-ttu-id="3e7aa-126">Erweitern Sie **.NET Framework 4,5**.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-126">Expand **.NET Framework 4.5**.</span></span>

4.  <span data-ttu-id="3e7aa-127">Wählen Sie **WCF-Aktivierung** aus, wenn Sie noch nicht ausgewählt ist.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-127">Select **WCF Activation** if it isn’t already selected.</span></span> <span data-ttu-id="3e7aa-128">Wählen Sie dann **http-Aktivierung** aus.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-128">Then select **HTTP Activation**.</span></span>

5.  <span data-ttu-id="3e7aa-129">Klicken Sie auf **weiter** , und folgen Sie den Anweisungen, um die Installation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-129">Click **Next** and follow the prompts to finish the installation.</span></span>

</div>

</div>

<div>

## <a name="windows-identity-foundation"></a><span data-ttu-id="3e7aa-130">Windows Identity Foundation</span><span class="sxs-lookup"><span data-stu-id="3e7aa-130">Windows Identity Foundation</span></span>

<span data-ttu-id="3e7aa-131">**WindowsIdentity Foundation** in lync Server 2013 erfordert die Installation von WindowsIdentity Foundation, um Server-zu-Server-Authentifizierungsszenarien zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-131">**Windows Identity Foundation** in Lync Server 2013 requires the installation of Windows Identity Foundation in order to support server to server authentication scenarios.</span></span> <span data-ttu-id="3e7aa-132">Windows Server 2008 R2 und Windows Server 2012 erfordern unterschiedliche Verfahren zum Installieren der Windows Identify Foundation.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-132">Windows Server 2008 R2 and Windows Server 2012 require different procedures to install the Windows Identify Foundation.</span></span> <span data-ttu-id="3e7aa-133">Wählen Sie das Betriebssystem Ihres Servers aus der folgenden Liste aus:</span><span class="sxs-lookup"><span data-stu-id="3e7aa-133">Select your server operating system from the following list:</span></span>

  - <span data-ttu-id="3e7aa-134">Windows Server 2008 R2 für Windows Server 2008 R2 überprüfen Sie, ob Sie bereits auf Ihrem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-134">Windows Server 2008 R2   For Windows Server 2008 R2, you check to see if it has already been installed on your computer.</span></span> <span data-ttu-id="3e7aa-135">Wechseln Sie dazu zu **Programme hinzufügen/entfernen**, **installierte Updates anzeigen**, und suchen Sie unter **Windows** nach dem Eintrag **Windows Identity Foundation (KB974405)**.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-135">To do this, go to **Add/Remove Programs**, **View Installed Updates**, and look under **Windows** for the entry **Windows Identity Foundation (KB974405)**.</span></span> <span data-ttu-id="3e7aa-136">Informationen zum Installieren von Windows Identity Foundation finden Sie unter [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657) .</span><span class="sxs-lookup"><span data-stu-id="3e7aa-136">For details about installing Windows Identity Foundation, see [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657).</span></span>

  - <span data-ttu-id="3e7aa-137">Windows Server 2012 für Windows Server 2012 verwenden Sie den **Server-Manager** , um die Windows Identity Foundation zu installieren.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-137">Windows Server 2012   For Windows Server 2012, you use **Server Manager** to install the Windows Identity Foundation.</span></span> <span data-ttu-id="3e7aa-138">Wählen Sie im **Assistenten zum Hinzufügen von Rollen und Features** des Server-Managers **Features** aus.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-138">In the Server Manager **Add Roles and Features Wizard**, select **Features**.</span></span> <span data-ttu-id="3e7aa-139">Wählen Sie **Windows Identity Foundation 3,5** aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-139">Select **Windows Identity Foundation 3.5** from the list.</span></span> <span data-ttu-id="3e7aa-140">Klicken Sie auf **weiter**, und klicken Sie dann auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-140">Click **Next**, then click **Install**.</span></span>

</div>

<div>

## <a name="additional-software-for-all-front-end-servers-and-standard-edition-servers"></a><span data-ttu-id="3e7aa-141">Zusätzliche Software für alle Front-End-Server und Standard Edition-Server</span><span class="sxs-lookup"><span data-stu-id="3e7aa-141">Additional Software for All Front End Servers and Standard Edition Servers</span></span>

<span data-ttu-id="3e7aa-142">Alle Front-End-Server und Standard Edition-Server müssen auch Internet Informationsdienste (IIS) mit bestimmten Modulen ausführen.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-142">All Front End Servers and Standard Edition servers must also run Internet Information Services (IIS) with certain modules.</span></span> <span data-ttu-id="3e7aa-143">Darüber hinaus müssen alle Front-End-Server und Standard Edition-Server, auf denen Konferenz-, Anruf Park-, Ankündigungs-oder Antwortgruppen bereitgestellt werden, die Windows Media-Format Laufzeit ausführen.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-143">Additionally, all Front End Servers and Standard Edition servers where conferencing, Call Park application, Announcement, or Response Groups are deployed must run Windows Media Format Runtime.</span></span>

<div>

## <a name="internet-information-services-iis"></a><span data-ttu-id="3e7aa-144">Internetinformationsdienste (Internet Information Services, IIS)</span><span class="sxs-lookup"><span data-stu-id="3e7aa-144">Internet Information Services (IIS)</span></span>

<span data-ttu-id="3e7aa-145">Front-End-Server und Standard Edition-Server müssen Internet Informationsdienste (IIS) mit den folgenden Modulen ausführen:</span><span class="sxs-lookup"><span data-stu-id="3e7aa-145">Front End Servers and Standard Edition servers must run Internet Information Services (IIS), with the following modules:</span></span>

  - <span data-ttu-id="3e7aa-146">Statischer Inhalt</span><span class="sxs-lookup"><span data-stu-id="3e7aa-146">Static Content</span></span>

  - <span data-ttu-id="3e7aa-147">Standarddokument</span><span class="sxs-lookup"><span data-stu-id="3e7aa-147">Default Document</span></span>

  - <span data-ttu-id="3e7aa-148">HTTP-Fehler</span><span class="sxs-lookup"><span data-stu-id="3e7aa-148">HTTP Errors</span></span>

  - <span data-ttu-id="3e7aa-149">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="3e7aa-149">ASP.NET</span></span>

  - <span data-ttu-id="3e7aa-150">.NET-Erweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="3e7aa-150">.NET Extensibility</span></span>

  - <span data-ttu-id="3e7aa-151">ISAPI-Erweiterungen (Internet Server API)</span><span class="sxs-lookup"><span data-stu-id="3e7aa-151">Internet Server API (ISAPI) Extensions</span></span>

  - <span data-ttu-id="3e7aa-152">ISAPI-Filter</span><span class="sxs-lookup"><span data-stu-id="3e7aa-152">ISAPI Filters</span></span>

  - <span data-ttu-id="3e7aa-153">HTTP-Protokollierung</span><span class="sxs-lookup"><span data-stu-id="3e7aa-153">HTTP Logging</span></span>

  - <span data-ttu-id="3e7aa-154">Protokollierungstools</span><span class="sxs-lookup"><span data-stu-id="3e7aa-154">Logging Tools</span></span>

  - <span data-ttu-id="3e7aa-155">Ablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="3e7aa-155">Tracing</span></span>

  - <span data-ttu-id="3e7aa-156">Windows-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="3e7aa-156">Windows Authentication</span></span>

  - <span data-ttu-id="3e7aa-157">Anforderungsfilterung</span><span class="sxs-lookup"><span data-stu-id="3e7aa-157">Request Filtering</span></span>

  - <span data-ttu-id="3e7aa-158">Komprimierung statischer Inhalte</span><span class="sxs-lookup"><span data-stu-id="3e7aa-158">Static Content Compression</span></span>

  - <span data-ttu-id="3e7aa-159">Komprimierung dynamischer Inhalte</span><span class="sxs-lookup"><span data-stu-id="3e7aa-159">Dynamic Content Compression</span></span>

  - <span data-ttu-id="3e7aa-160">IIS-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="3e7aa-160">IIS Management Console</span></span>

  - <span data-ttu-id="3e7aa-161">IIS-Verwaltungsskripts und -tools</span><span class="sxs-lookup"><span data-stu-id="3e7aa-161">IIS Management Scripts and Tools</span></span>

  - <span data-ttu-id="3e7aa-162">Anonyme Authentifizierung (standardmäßig installiert, wenn IIS installiert ist)</span><span class="sxs-lookup"><span data-stu-id="3e7aa-162">Anonymous Authentication (this is installed by default when IIS is installed.)</span></span>

  - <span data-ttu-id="3e7aa-163">Clientzertifikatzuordnungs-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="3e7aa-163">Client Certificate Mapping Authentication</span></span>

</div>

<div>

## <a name="windows-media-format-runtime-and-windows-desktop-experience"></a><span data-ttu-id="3e7aa-164">Windows Media Format-Laufzeit und Windows-Desktop Experience</span><span class="sxs-lookup"><span data-stu-id="3e7aa-164">Windows Media Format Runtime and Windows Desktop Experience</span></span>

<span data-ttu-id="3e7aa-165">**Windows-Desktop Umgebung** Auf allen Front-End-Servern und Standard Edition-Servern, auf denen Konferenzen bereitgestellt werden, muss die Windows Media-Format Laufzeit installiert sein, die, mit Ausnahme von Windows Server 2012, als Teil der Windows-Desktopumgebung installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-165">**Windows Desktop Experience** All Front End Servers and Standard Edition servers where conferencing will be deployed must have the Windows Media Format Runtime installed, which, except for Windows Server 2012 is installed as part of the Windows desktop experience.</span></span> <span data-ttu-id="3e7aa-166">Windows Server 2012 erfordert Microsoft Media Foundation.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-166">Windows Server 2012 requires Microsoft Media Foundation.</span></span> <span data-ttu-id="3e7aa-167">Die Windows Media-Format Laufzeit ist erforderlich, um die Windows Media-Audio-Dateien (WMA) auszuführen, die von den Anwendungen für die Anruf Park-, Ankündigungs-und Reaktionsgruppen für Ankündigungen und Musik abgespielt werden.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-167">The Windows Media Format Runtime is required to run the Windows Media Audio (.wma) files that the Call Park, Announcement, and Response Group applications play for announcements and music.</span></span>

<span data-ttu-id="3e7aa-168">Wir empfehlen, dass Sie die Windows-Desktopumgebung installieren, bevor Sie lync Server 2013 installieren.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-168">We recommend that you install Windows desktop experience before you install Lync Server 2013.</span></span> <span data-ttu-id="3e7aa-169">Wenn lync Server 2013 diese Software auf dem Server nicht findet, werden Sie aufgefordert, Sie zu installieren, und dann müssen Sie den Server neu starten, um die Installation abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-169">If Lync Server 2013 does not find this software on the server, it will prompt you to install it, and then you must restart the server to complete installation.</span></span>

</div>

</div>

<div>

## <a name="additional-software-for-front-end-servers-and-standard-edition-servers-running-on-windows-server-2012"></a><span data-ttu-id="3e7aa-170">Zusätzliche Software für Front-End-Server und Standard Edition-Server, die unter Windows Server 2012 ausgeführt werden</span><span class="sxs-lookup"><span data-stu-id="3e7aa-170">Additional Software for Front End Servers and Standard Edition Servers Running on Windows Server 2012</span></span>

<span data-ttu-id="3e7aa-171">Für Front-End-Server ist .NET 3,5 erforderlich, das unter Windows Server 2012 nicht standardmäßig installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-171">Front End Servers require .NET 3.5, which is not installed by default on Windows Server 2012.</span></span> <span data-ttu-id="3e7aa-172">Installieren Sie das Windows Server 2012-Installationsmedium auf Laufwerk D, und geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="3e7aa-172">To install it, put your Windows Server 2012 installation media in Drive D and type the following:</span></span>

    Add-WindowsFeature RSAT-ADDS, Web-Server, Web-Static-Content, Web-Default-Doc, Web-Http-Errors, Web-Asp-Net, Web-Net-Ext, Web-ISAPI-Ext, Web-ISAPI-Filter, Web-Http-Logging, Web-Log-Libraries, Web-Request-Monitor, Web-Http-Tracing, Web-Basic-Auth, Web-Windows-Auth, Web-Client-Auth, Web-Filtering, Web-Stat-Compression, Web-Dyn-Compression, NET-WCF-HTTP-Activation45, Web-Asp-Net45, Web-Mgmt-Tools, Web-Scripting-Tools, Web-Mgmt-Compat, Desktop-Experience, Telnet-Client, BITS -Source D:\sources\sxs

<span data-ttu-id="3e7aa-173">Details zur Installation von .NET 3,5 auf Servern mit Windows Server 2012 finden Sie unter "Microsoft .NET Framework 3,5-Bereitstellungsüberlegungen" unter <https://go.microsoft.com/fwlink/p/?linkid=275032> .</span><span class="sxs-lookup"><span data-stu-id="3e7aa-173">For details about installing .NET 3.5 on servers running Windows Server 2012, see "Microsoft .NET Framework 3.5 Deployment Considerations" at <https://go.microsoft.com/fwlink/p/?linkid=275032>.</span></span>

</div>

<div>

## <a name="additional-software-for-directors"></a><span data-ttu-id="3e7aa-174">Zusätzliche Software für Directors</span><span class="sxs-lookup"><span data-stu-id="3e7aa-174">Additional Software for Directors</span></span>

<span data-ttu-id="3e7aa-175">Directors müssen Internet Informationsdienste (IIS) mit den folgenden Modulen ausführen:</span><span class="sxs-lookup"><span data-stu-id="3e7aa-175">Directors must run Internet Information Services (IIS), with the following modules:</span></span>

  - <span data-ttu-id="3e7aa-176">Statischer Inhalt</span><span class="sxs-lookup"><span data-stu-id="3e7aa-176">Static Content</span></span>

  - <span data-ttu-id="3e7aa-177">Standarddokument</span><span class="sxs-lookup"><span data-stu-id="3e7aa-177">Default Document</span></span>

  - <span data-ttu-id="3e7aa-178">HTTP-Fehler</span><span class="sxs-lookup"><span data-stu-id="3e7aa-178">HTTP Errors</span></span>

  - <span data-ttu-id="3e7aa-179">ASP.NET</span><span class="sxs-lookup"><span data-stu-id="3e7aa-179">ASP.NET</span></span>

  - <span data-ttu-id="3e7aa-180">.NET-Erweiterbarkeit</span><span class="sxs-lookup"><span data-stu-id="3e7aa-180">.NET Extensibility</span></span>

  - <span data-ttu-id="3e7aa-181">ISAPI-Erweiterungen (Internet Server API)</span><span class="sxs-lookup"><span data-stu-id="3e7aa-181">Internet Server API (ISAPI) Extensions</span></span>

  - <span data-ttu-id="3e7aa-182">ISAPI-Filter</span><span class="sxs-lookup"><span data-stu-id="3e7aa-182">ISAPI Filters</span></span>

  - <span data-ttu-id="3e7aa-183">HTTP-Protokollierung</span><span class="sxs-lookup"><span data-stu-id="3e7aa-183">HTTP Logging</span></span>

  - <span data-ttu-id="3e7aa-184">Protokollierungstools</span><span class="sxs-lookup"><span data-stu-id="3e7aa-184">Logging Tools</span></span>

  - <span data-ttu-id="3e7aa-185">Ablaufverfolgung</span><span class="sxs-lookup"><span data-stu-id="3e7aa-185">Tracing</span></span>

  - <span data-ttu-id="3e7aa-186">Windows-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="3e7aa-186">Windows Authentication</span></span>

  - <span data-ttu-id="3e7aa-187">Anforderungsfilterung</span><span class="sxs-lookup"><span data-stu-id="3e7aa-187">Request Filtering</span></span>

  - <span data-ttu-id="3e7aa-188">Komprimierung statischer Inhalte</span><span class="sxs-lookup"><span data-stu-id="3e7aa-188">Static Content Compression</span></span>

  - <span data-ttu-id="3e7aa-189">IIS-Verwaltungskonsole</span><span class="sxs-lookup"><span data-stu-id="3e7aa-189">IIS Management Console</span></span>

  - <span data-ttu-id="3e7aa-190">IIS-Verwaltungsskripts und -tools</span><span class="sxs-lookup"><span data-stu-id="3e7aa-190">IIS Management Scripts and Tools</span></span>

  - <span data-ttu-id="3e7aa-191">Anonyme Authentifizierung (standardmäßig installiert, wenn IIS installiert ist)</span><span class="sxs-lookup"><span data-stu-id="3e7aa-191">Anonymous Authentication (This is installed by default when IIS is installed.)</span></span>

  - <span data-ttu-id="3e7aa-192">Clientzertifikatzuordnungs-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="3e7aa-192">Client Certificate Mapping Authentication</span></span>

</div>

<div>

## <a name="additional-software-for-persistent-chat-front-end-servers"></a><span data-ttu-id="3e7aa-193">Zusätzliche Software für beständige Chat-Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="3e7aa-193">Additional Software for Persistent Chat Front End Servers</span></span>

<span data-ttu-id="3e7aa-194">Beständige Chat-Front-End-Server müssen Message Queuing (auch als MSMQ bezeichnet) ausführen, einer Komponente von Windows Server.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-194">Persistent Chat Front End Servers must run Message Queuing (also known as MSMQ), which is a component of Windows Server.</span></span>

<span data-ttu-id="3e7aa-195">Informationen zum Aktivieren von MSMQ finden [Sie hier.](https://technet.microsoft.com/library/cc771474.aspx)</span><span class="sxs-lookup"><span data-stu-id="3e7aa-195">For information on enabling MSMQ, [click here.](https://technet.microsoft.com/library/cc771474.aspx)</span></span>

</div>

<div>

## <a name="additional-software-for-edge-servers"></a><span data-ttu-id="3e7aa-196">Zusätzliche Software für Edgeserver</span><span class="sxs-lookup"><span data-stu-id="3e7aa-196">Additional Software for Edge Servers</span></span>

<span data-ttu-id="3e7aa-197">Edgeserver erfordern die folgende Software:</span><span class="sxs-lookup"><span data-stu-id="3e7aa-197">Edge Servers require the following software:</span></span>

  - <span data-ttu-id="3e7aa-198">Auf jedem Server, auf dem lync Server 2013 ausgeführt wird, muss die richtige Version von Windows PowerShell 3,0 installiert sein.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-198">Each server running Lync Server 2013 must have the correct release of Windows PowerShell 3.0 installed.</span></span> <span data-ttu-id="3e7aa-199">Ausführliche Informationen finden Sie unter [Installieren von Windows PowerShell 3,0 für lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span><span class="sxs-lookup"><span data-stu-id="3e7aa-199">For details, see [Installing Windows PowerShell 3.0 for Lync Server 2013](lync-server-2013-installing-windows-powershell-3-0.md).</span></span>

  - <span data-ttu-id="3e7aa-200">Für lync Server ist Microsoft .NET Framework 4,5 erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-200">Lync Server requires Microsoft .NET Framework 4.5.</span></span> <span data-ttu-id="3e7aa-201">Für lync Server 2013, das unter Windows Server 2008 R2 installiert ist, müssen Sie die 64-Bit-Version von Microsoft .NET Framework 4,5 auf dem Server manuell installieren, bevor Sie lync Server 2013 installieren.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-201">For Lync Server 2013 installed on Windows Server 2008 R2, you must manually install the 64-bit edition of Microsoft .NET Framework 4.5 on the server prior to installing Lync Server 2013.</span></span> <span data-ttu-id="3e7aa-202">Wenn Sie die Datei manuell installieren möchten, laden Sie das Microsoft .NET 4,5-Framework aus dem Microsoft Download Center unter [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span><span class="sxs-lookup"><span data-stu-id="3e7aa-202">To manually install it, download the Microsoft .NET 4.5 Framework from the Microsoft Download Center at [https://go.microsoft.com/fwlink/p/?LinkId=268529](https://go.microsoft.com/fwlink/p/?linkid=268529)</span></span>

  - <span data-ttu-id="3e7aa-203">**WindowsIdentity Foundation** in lync Server 2013 erfordert die Installation von WindowsIdentity Foundation, um Server-zu-Server-Authentifizierungsszenarien zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-203">**Windows Identity Foundation** in Lync Server 2013 requires the installation of Windows Identity Foundation in order to support server to server authentication scenarios.</span></span> <span data-ttu-id="3e7aa-204">Windows Server 2008 R2 und Windows Server 2012 erfordern unterschiedliche Verfahren zum Installieren der Windows Identify Foundation.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-204">Windows Server 2008 R2 and Windows Server 2012 require different procedures to install the Windows Identify Foundation.</span></span> <span data-ttu-id="3e7aa-205">Wählen Sie das Betriebssystem Ihres Servers aus der folgenden Liste aus:</span><span class="sxs-lookup"><span data-stu-id="3e7aa-205">Select your server operating system from the following list:</span></span>
    
      - <span data-ttu-id="3e7aa-206">Windows Server 2008 R2 für Windows Server 2008 R2 überprüfen Sie, ob Sie bereits auf Ihrem Computer installiert ist.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-206">Windows Server 2008 R2   For Windows Server 2008 R2, you check to see if it has already been installed on your computer.</span></span> <span data-ttu-id="3e7aa-207">Wechseln Sie dazu zu **Programme hinzufügen/entfernen**, **installierte Updates anzeigen**, und suchen Sie unter **Windows** nach dem Eintrag **Windows Identity Foundation (KB974405)**.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-207">To do this, go to **Add/Remove Programs**, **View Installed Updates**, and look under **Windows** for the entry **Windows Identity Foundation (KB974405)**.</span></span> <span data-ttu-id="3e7aa-208">Informationen zum Installieren von Windows Identity Foundation finden Sie unter [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657) .</span><span class="sxs-lookup"><span data-stu-id="3e7aa-208">For details about installing Windows Identity Foundation, see [https://go.microsoft.com/fwlink/p/?linkId=204657](https://go.microsoft.com/fwlink/p/?linkid=204657).</span></span>
    
      - <span data-ttu-id="3e7aa-209">Windows Server 2012 für Windows Server 2012 verwenden Sie den **Server-Manager** , um die Windows Identity Foundation zu installieren.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-209">Windows Server 2012   For Windows Server 2012, you use **Server Manager** to install the Windows Identity Foundation.</span></span> <span data-ttu-id="3e7aa-210">Wählen Sie im **Assistenten zum Hinzufügen von Rollen und Features** des Server-Managers **Features** aus.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-210">In the Server Manager **Add Roles and Features Wizard**, select **Features**.</span></span> <span data-ttu-id="3e7aa-211">Wählen Sie **Windows Identity Foundation 3,5** aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-211">Select **Windows Identity Foundation 3.5** from the list.</span></span> <span data-ttu-id="3e7aa-212">Klicken Sie auf **weiter**, und klicken Sie dann auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-212">Click **Next**, then click **Install**.</span></span>

</div>

<div>

## <a name="do-not-install-layered-socket-providers-on-media-servers"></a><span data-ttu-id="3e7aa-213">Installieren Sie keine Layered Socket-Anbieter auf Medienservern.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-213">Do Not Install Layered Socket Providers on Media Servers</span></span>

<span data-ttu-id="3e7aa-214">Installieren Sie keine Microsoft Internet Security and Acceleration (ISA) Server-Client Software oder eine andere Winsock-Schicht Service Anbieter-Software (LSP) auf allen Front-End-Servern oder eigenständigen Vermittlungsservern.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-214">Do not install any Microsoft Internet Security and Acceleration (ISA) Server client software, or any other Winsock Layered Service Providers (LSP) software, on any Front End Servers or stand-alone Mediation Servers.</span></span> <span data-ttu-id="3e7aa-215">Die Installation dieser Software kann zu schlechter Leistung des Medien Verkehrs führen.</span><span class="sxs-lookup"><span data-stu-id="3e7aa-215">Installing this software could cause poor media traffic performance.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3e7aa-216">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e7aa-216">See Also</span></span>


[<span data-ttu-id="3e7aa-217">Softwareanforderungen für Verwaltungstools in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e7aa-217">Administrative tools software requirements in Lync Server 2013</span></span>](lync-server-2013-administrative-tools-software-requirements.md)  
  

<span data-ttu-id="3e7aa-218"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3e7aa-218"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

