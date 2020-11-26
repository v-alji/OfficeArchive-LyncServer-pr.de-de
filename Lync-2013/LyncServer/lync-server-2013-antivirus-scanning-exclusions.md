---
title: 'Lync Server 2013: Ausnahmen in Virenschutzprogrammen'
description: 'Lync Server 2013: Ausschlüsse für Antivirus-Scans.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Antivirus scanning exclusions for Lync Server 2013
ms:assetid: 71e1f1cc-2d16-4111-9864-9276bf24dfe0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn440138(v=OCS.15)
ms:contentKeyID: 57793042
ms.date: 11/03/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20c395f529cad91993d003efdeb231bd66f4b9bc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440661"
---
# <a name="antivirus-scanning-exclusions-for-lync-server-2013"></a><span data-ttu-id="33389-103">Ausnahmen in Virenschutzprogrammen für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="33389-103">Antivirus scanning exclusions for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="33389-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="33389-104">

<span> </span></span></span>

<span data-ttu-id="33389-105">_**Letztes Änderungsdatum des Themas:** 2015-11-02_</span><span class="sxs-lookup"><span data-stu-id="33389-105">_**Topic Last Modified:** 2015-11-02_</span></span>

<span data-ttu-id="33389-106">Wenn Sie sicherstellen möchten, dass der Virenscanner den Betrieb von lync Server 2013 nicht stört, müssen Sie bestimmte Prozesse und Verzeichnisse für jeden lync Server 2013-Server oder die Serverrolle ausschließen, auf der Sie einen Antivirus-Scanner ausführen.</span><span class="sxs-lookup"><span data-stu-id="33389-106">To ensure that the antivirus scanner does not interfere with the operation of Lync Server 2013, you must exclude specific processes and directories for each Lync Server 2013 server or server role on which you run an antivirus scanner.</span></span> <span data-ttu-id="33389-107">Die folgenden Prozesse und Verzeichnisse sollten ausgeschlossen werden:</span><span class="sxs-lookup"><span data-stu-id="33389-107">The following processes and directories should be excluded:</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="33389-108">Die nachstehend aufgeführten Ordner-und Dateispeicherorte sind die Standardspeicherorte für lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="33389-108">Folder and file locations listed below are the default locations for Lync Server 2013.</span></span> <span data-ttu-id="33389-109">Falls Sie andere Speicherorte als die Standardspeicherorte verwendet haben, schließen Sie statt der hier aufgeführten Standardspeicherorte die Speicherorte aus, die Sie für Ihre Organisation angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="33389-109">For any locations for which you did not use the default, exclude the locations you specified for your organization instead of the default locations specified in this topic.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="33389-110">Beachten Sie, dass einige Virenschutzprogramme für ihre Ausschlussliste anstelle von relativen möglicherweise absolute Pfade benötigen.</span><span class="sxs-lookup"><span data-stu-id="33389-110">Please note that some antivirus programs may need absolute, not relative paths, for their exclusion list.</span></span>



</div>

  - <span data-ttu-id="33389-111">Lync Server 2013-Prozesse:</span><span class="sxs-lookup"><span data-stu-id="33389-111">Lync Server 2013 processes:</span></span>
    
      - <span data-ttu-id="33389-112">ABServer.exe</span><span class="sxs-lookup"><span data-stu-id="33389-112">ABServer.exe</span></span>
    
      - <span data-ttu-id="33389-113">AcpMcuSvc.exe</span><span class="sxs-lookup"><span data-stu-id="33389-113">AcpMcuSvc.exe</span></span>
    
      - <span data-ttu-id="33389-114">ASMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="33389-114">ASMCUSvc.exe</span></span>
    
      - <span data-ttu-id="33389-115">AVMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="33389-115">AVMCUSvc.exe</span></span>
    
      - <span data-ttu-id="33389-116">ChannelService.exe</span><span class="sxs-lookup"><span data-stu-id="33389-116">ChannelService.exe</span></span>
    
      - <span data-ttu-id="33389-117">ClsAgent.exe</span><span class="sxs-lookup"><span data-stu-id="33389-117">ClsAgent.exe</span></span>
    
      - <span data-ttu-id="33389-118">ComplianceService.exe</span><span class="sxs-lookup"><span data-stu-id="33389-118">ComplianceService.exe</span></span>
    
      - <span data-ttu-id="33389-119">DataMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="33389-119">DataMCUSvc.exe</span></span>
    
      - <span data-ttu-id="33389-120">DataProxy.exe</span><span class="sxs-lookup"><span data-stu-id="33389-120">DataProxy.exe</span></span>
    
      - <span data-ttu-id="33389-121">FileTransferAgent.exe</span><span class="sxs-lookup"><span data-stu-id="33389-121">FileTransferAgent.exe</span></span>
    
      - <span data-ttu-id="33389-122">IMMCUSvc.exe</span><span class="sxs-lookup"><span data-stu-id="33389-122">IMMCUSvc.exe</span></span>
    
      - <span data-ttu-id="33389-123">LysSvc.exe</span><span class="sxs-lookup"><span data-stu-id="33389-123">LysSvc.exe</span></span>
    
      - <span data-ttu-id="33389-124">MasterReplicatorAgent.exe</span><span class="sxs-lookup"><span data-stu-id="33389-124">MasterReplicatorAgent.exe</span></span>
    
      - <span data-ttu-id="33389-125">MediaRelaySvc.exe</span><span class="sxs-lookup"><span data-stu-id="33389-125">MediaRelaySvc.exe</span></span>
    
      - <span data-ttu-id="33389-126">MediationServerSvc.exe</span><span class="sxs-lookup"><span data-stu-id="33389-126">MediationServerSvc.exe</span></span>
    
      - <span data-ttu-id="33389-127">MRASSvc.exe</span><span class="sxs-lookup"><span data-stu-id="33389-127">MRASSvc.exe</span></span>
    
      - <span data-ttu-id="33389-128">OcsAppServerHost.exe</span><span class="sxs-lookup"><span data-stu-id="33389-128">OcsAppServerHost.exe</span></span>
    
      - <span data-ttu-id="33389-129">ReplicaReplicatorAgent.exe</span><span class="sxs-lookup"><span data-stu-id="33389-129">ReplicaReplicatorAgent.exe</span></span>
    
      - <span data-ttu-id="33389-130">ReplicationApp.exe</span><span class="sxs-lookup"><span data-stu-id="33389-130">ReplicationApp.exe</span></span>
    
      - <span data-ttu-id="33389-131">RtcHost.exe</span><span class="sxs-lookup"><span data-stu-id="33389-131">RtcHost.exe</span></span>
    
      - <span data-ttu-id="33389-132">RTCSrv.exe</span><span class="sxs-lookup"><span data-stu-id="33389-132">RTCSrv.exe</span></span>
    
      - <span data-ttu-id="33389-133">XmppProxy.exe</span><span class="sxs-lookup"><span data-stu-id="33389-133">XmppProxy.exe</span></span>
    
      - <span data-ttu-id="33389-134">XmppTGW.exe</span><span class="sxs-lookup"><span data-stu-id="33389-134">XmppTGW.exe</span></span>

  - <span data-ttu-id="33389-135">Windows Fabric-Hostdienst-Prozesse:</span><span class="sxs-lookup"><span data-stu-id="33389-135">Windows Fabric Host Service processes:</span></span>
    
      - <span data-ttu-id="33389-136">Fabric.exe</span><span class="sxs-lookup"><span data-stu-id="33389-136">Fabric.exe</span></span>
    
      - <span data-ttu-id="33389-137">FabricDCA.exe</span><span class="sxs-lookup"><span data-stu-id="33389-137">FabricDCA.exe</span></span>
    
      - <span data-ttu-id="33389-138">FabricHost.exe</span><span class="sxs-lookup"><span data-stu-id="33389-138">FabricHost.exe</span></span>

  - <span data-ttu-id="33389-139">IIS-Prozesse:</span><span class="sxs-lookup"><span data-stu-id="33389-139">IIS processes:</span></span>
    
      - <span data-ttu-id="33389-140">% systemroot% \\ system32 \\ inetsrv \\w3wp.exe</span><span class="sxs-lookup"><span data-stu-id="33389-140">%systemroot%\\system32\\inetsrv\\w3wp.exe</span></span>
    
      - <span data-ttu-id="33389-141">% systemroot% \\ syswow64 \\ inetsrv \\w3wp.exe</span><span class="sxs-lookup"><span data-stu-id="33389-141">%systemroot%\\SysWOW64\\inetsrv\\w3wp.exe</span></span>

  - <span data-ttu-id="33389-142">SQL Server Back-End-Prozesse:</span><span class="sxs-lookup"><span data-stu-id="33389-142">SQL Server Back-End processes:</span></span>
    
      - <span data-ttu-id="33389-143">% Programme% \\ Microsoft SQL Server \\ MSSQL11. MSSQLSERVER \\ MSSQL \\ Binn \\SQLServr.exe</span><span class="sxs-lookup"><span data-stu-id="33389-143">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.MSSQLSERVER\\MSSQL\\Binn\\SQLServr.exe</span></span>
    
      - <span data-ttu-id="33389-144">% Programme% \\ Microsoft SQL Server \\ MSRS11. MSSQLSERVER \\ Reporting Services \\ Report Server \\ bin \\ReportingServicesService.exe</span><span class="sxs-lookup"><span data-stu-id="33389-144">%ProgramFiles%\\Microsoft SQL Server\\MSRS11.MSSQLSERVER\\Reporting Services\\ReportServer\\Bin\\ReportingServicesService.exe</span></span>
    
      - <span data-ttu-id="33389-145">% Programme% \\ Microsoft SQL Server \\ MSAS11. MSSQLSERVER \\ OLAP \\ bin \\MSMDSrv.exe</span><span class="sxs-lookup"><span data-stu-id="33389-145">%ProgramFiles%\\Microsoft SQL Server\\MSAS11.MSSQLSERVER\\OLAP\\Bin\\MSMDSrv.exe</span></span>

  - <span data-ttu-id="33389-146">SQL Server Front-End-Prozesse:</span><span class="sxs-lookup"><span data-stu-id="33389-146">SQL Server Front-End processes:</span></span>
    
      - <span data-ttu-id="33389-147">% Programme% \\ Microsoft SQL Server \\ MSSQL11. LYNCLOCAL \\ MSSQL \\ Binn \\SQLServr.exe</span><span class="sxs-lookup"><span data-stu-id="33389-147">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.LYNCLOCAL\\MSSQL\\Binn\\SQLServr.exe</span></span>
    
      - <span data-ttu-id="33389-148">% Programme% \\ Microsoft SQL Server \\ MSSQL11. RTCLOCAL \\ MSSQL \\ Binn \\SQLServr.exe</span><span class="sxs-lookup"><span data-stu-id="33389-148">%ProgramFiles%\\Microsoft SQL Server\\MSSQL11.RTCLOCAL\\MSSQL\\Binn\\SQLServr.exe</span></span>

  - <span data-ttu-id="33389-149">Verzeichnisse und Dateien:</span><span class="sxs-lookup"><span data-stu-id="33389-149">Directories and files:</span></span>
    
      - <span data-ttu-id="33389-150">% systemroot% \\ system32- \\ Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="33389-150">%systemroot%\\System32\\LogFiles</span></span>
    
      - <span data-ttu-id="33389-151">% systemroot% \\ syswow64- \\ Protokolldateien</span><span class="sxs-lookup"><span data-stu-id="33389-151">%systemroot%\\SysWow64\\LogFiles</span></span>
    
      - <span data-ttu-id="33389-152">% systemroot% \\ Microsoft.net \\ Assembly \\ GAC \_ MSIL</span><span class="sxs-lookup"><span data-stu-id="33389-152">%systemroot%\\Microsoft.NET\\assembly\\GAC\_MSIL</span></span>
    
      - <span data-ttu-id="33389-153">% Programme% \\ Microsoft lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="33389-153">%programfiles%\\Microsoft Lync Server 2013</span></span>
    
      - <span data-ttu-id="33389-154">% Programme% \\ Common Files \\ Microsoft lync Server 2013 \\ Watcher-Knoten</span><span class="sxs-lookup"><span data-stu-id="33389-154">%programfiles%\\Common Files\\Microsoft Lync Server 2013\\Watcher Node</span></span>
    
      - <span data-ttu-id="33389-155">% Programme% \\ Allgemeine Dateien \\ Microsoft lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="33389-155">%programfiles%\\Common Files\\Microsoft Lync Server 2013</span></span>
    
      - <span data-ttu-id="33389-156">% SystemDrive% \\ RtcReplicaRoot</span><span class="sxs-lookup"><span data-stu-id="33389-156">%SystemDrive%\\RtcReplicaRoot</span></span>
    
      - <span data-ttu-id="33389-157">Dateifreigabespeicher (im Topologie-Generator angegeben).</span><span class="sxs-lookup"><span data-stu-id="33389-157">File share store (specified in Topology Builder).</span></span> <span data-ttu-id="33389-158">Dateispeicher werden im Topologie-Generator angegeben.</span><span class="sxs-lookup"><span data-stu-id="33389-158">File stores are specified in Topology Builder.</span></span>
    
      - <span data-ttu-id="33389-159">SQL Server-Daten-und-Protokolldateien, einschließlich derer für die Back-End-Datenbank, den Benutzerspeicher, den Archivierungsspeicher, den Überwachungsspeicher und den Anwendungsspeicher.</span><span class="sxs-lookup"><span data-stu-id="33389-159">SQL Server data and log files, including those for the back-end database, user store, archiving store, monitoring store, and application store.</span></span> <span data-ttu-id="33389-160">In Topology Builder können Datenbank-und Protokolldateien angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="33389-160">Database and log files can be specified in Topology Builder.</span></span> <span data-ttu-id="33389-161">Details zu den Daten-und Protokolldateien für jede Datenbank, einschließlich Standardnamen, finden Sie unter [SQL Server-Daten-und Protokolldatei Platzierung für lync Server 2013](lync-server-2013-sql-server-data-and-log-file-placement.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="33389-161">For details about the data and log files for each database, including default names, see [SQL Server data and log file placement for Lync Server 2013](lync-server-2013-sql-server-data-and-log-file-placement.md) in the Deployment documentation.</span></span>
    
      - <span data-ttu-id="33389-162">SQL Server-Daten-und-Protokolldateien, einschließlich derer für die Front-End-Datenbank, den lync-Store und den RtcDatabase-Speicher.</span><span class="sxs-lookup"><span data-stu-id="33389-162">SQL Server data and log files, including those for the Front-end database, Lync store, and RtcDatabase store.</span></span> <span data-ttu-id="33389-163">Sie befinden sich normalerweise unter% LokalesLaufwerk% \\ CSData.</span><span class="sxs-lookup"><span data-stu-id="33389-163">They are normally under %localdrive%\\CSData.</span></span>

<span data-ttu-id="33389-164"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="33389-164"></div>

<span> </span>

</div>

</div>

</span></span></div>

