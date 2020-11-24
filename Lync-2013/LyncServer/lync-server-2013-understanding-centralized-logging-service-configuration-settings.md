---
title: Grundlegendes zu Konfigurationseinstellungen für den zentralisierten Protokollierungsdienst
description: Grundlegendes zu Konfigurationseinstellungen für den zentralisierten Protokollierungsdienst
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Understanding Centralized Logging Service configuration settings
ms:assetid: 3c34e600-0b91-43dc-b4cc-90b6a70ee12e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688029(v=OCS.15)
ms:contentKeyID: 49733619
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f99dbffe15c4b3f0dc13d231c3a2732a8554397
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394858"
---
# <a name="understanding-centralized-logging-service-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="d105f-103">Grundlegendes zu den Konfigurationseinstellungen für den zentralisierten Protokollierungsdienst in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d105f-103">Understanding Centralized Logging Service configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d105f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d105f-104">

<span> </span></span></span>

<span data-ttu-id="d105f-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="d105f-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="d105f-106">Der zentralisierte Protokollierungsdienst ist so konfiguriert, dass er definiert, was der Protokollierungsdienst sammeln soll, wie er erfasst, woher er sammelt und welche Protokolleinstellungen vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="d105f-106">The Centralized Logging Service is configured to define what the logging service is intended to collect, how it collects, where it will collect from, and what the log settings are.</span></span> <span data-ttu-id="d105f-107">Sie definieren diese Einstellungen global (d. h. für die gesamte Bereitstellung) oder für einen Standort (also einen benannten Standort in Ihrer Bereitstellung).</span><span class="sxs-lookup"><span data-stu-id="d105f-107">You define these settings globally (that is, for the entire deployment) or for a site (that is, a named site in your deployment).</span></span> <span data-ttu-id="d105f-108">Für jede Protokollierung, die Sie definieren, werden die Einstellungen verwendet, die jeweils für die von Ihnen für Befehle zum Starten, Beenden, Leeren und Durchsuchen von Protokollen verwendete Identität geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="d105f-108">Any logging that you define will use the settings that are appropriate for the identity that you use for commands to start, stop, flush, and search logs.</span></span>

<div>

## <a name="to-display-the-current-centralized-logging-service-configuration"></a><span data-ttu-id="d105f-109">So zeigen Sie die aktuelle Konfiguration für den zentralisierten Protokollierungsdienst an</span><span class="sxs-lookup"><span data-stu-id="d105f-109">To display the current Centralized Logging Service configuration</span></span>

1.  <span data-ttu-id="d105f-110">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="d105f-110">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="d105f-111">Geben Sie den folgenden Befehl an der Eingabeaufforderung ein:</span><span class="sxs-lookup"><span data-stu-id="d105f-111">Type the following at a command-line prompt:</span></span>
    
        Get-CsClsConfiguration
    
    <div>
    

    > [!TIP]
    > <span data-ttu-id="d105f-112">Sie können den Umfang der Konfigurationseinstellungen einschränken oder erweitern, die durch definieren <CODE>-Identity</CODE> und einen Bereich wie "Website: Redmond" zurückgegeben werden, um nur den CsClsConfiguration für die Website Redmond zurückzugeben.</span><span class="sxs-lookup"><span data-stu-id="d105f-112">You can narrow or expand the scope of the configuration settings that are returned by defining <CODE>-Identity</CODE> and a scope, such as "Site:Redmond" to return only the CsClsConfiguration for the site Redmond.</span></span> <span data-ttu-id="d105f-113">Wenn Sie Details zu einem bestimmten Teil der Konfiguration wünschen, können Sie die Ausgabe in ein anderes Windows PowerShell-Cmdlet übertragen.</span><span class="sxs-lookup"><span data-stu-id="d105f-113">If you want details about a given portion of the configuration, you can pipe the output into another Windows PowerShell cmdlet.</span></span> <span data-ttu-id="d105f-114">Wenn Sie beispielsweise Details zu den Szenarien erhalten möchten, die in der Konfiguration für die Website "Redmond" definiert sind, geben Sie Folgendes ein: <CODE>Get-CsClsConfiguration -Identity "site:Redmond" | Select-Object -ExpandPropery Scenarios</CODE></span><span class="sxs-lookup"><span data-stu-id="d105f-114">For example, to get details about the scenarios defined in the configuration for site "Redmond", type: <CODE>Get-CsClsConfiguration -Identity "site:Redmond" | Select-Object -ExpandPropery Scenarios</CODE></span></span>

    
    </div>
    
    <span data-ttu-id="d105f-115">![Beispielausgabe von Get-CsClsConfiguration](images/JJ688029.23f98ddc-fc48-499a-b6c5-752611f2a0b0(OCS.15).jpg "Beispielausgabe von Get-CsClsConfiguration")</span><span class="sxs-lookup"><span data-stu-id="d105f-115">![Sample output from Get-CsClsConfiguration.](images/JJ688029.23f98ddc-fc48-499a-b6c5-752611f2a0b0(OCS.15).jpg "Sample output from Get-CsClsConfiguration.")</span></span>
    
    <span data-ttu-id="d105f-116">Das Ergebnis des Cmdlets zeigt die aktuelle Konfiguration des zentralen Protokollierungsdiensts an.</span><span class="sxs-lookup"><span data-stu-id="d105f-116">The result from the cmdlet displays the current configuration of the Centralized Logging Service.</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="d105f-117">Konfigurationseinstellung</span><span class="sxs-lookup"><span data-stu-id="d105f-117">Configuration Setting</span></span></th>
    <th><span data-ttu-id="d105f-118">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="d105f-118">Description</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="d105f-119"><strong>Identity</strong></span><span class="sxs-lookup"><span data-stu-id="d105f-119"><strong>Identity</strong></span></span></p></td>
    <td><p><span data-ttu-id="d105f-p103">Identifiziert den Bereich und den Namen dieser Konfiguration. Es gibt nur eine globale Konfiguration sowie eine Konfiguration pro Standort.</span><span class="sxs-lookup"><span data-stu-id="d105f-p103">Identifies the scope and name for this configuration. There is only one Global configuration, and one configuration per site.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d105f-122"><strong>Scenarios</strong></span><span class="sxs-lookup"><span data-stu-id="d105f-122"><strong>Scenarios</strong></span></span></p></td>
    <td><p><span data-ttu-id="d105f-123">Auflistung aller Szenarien, die für diese Konfiguration definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d105f-123">Listing of all scenarios that are defined for this configuration.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="d105f-124"><strong>SearchTerms</strong></span><span class="sxs-lookup"><span data-stu-id="d105f-124"><strong>SearchTerms</strong></span></span></p></td>
    <td><p><span data-ttu-id="d105f-125">Definierte Suchbegriffe für die Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d105f-125">Defined search terms for the configuration.</span></span> <span data-ttu-id="d105f-126">Office 365 oder Microsoft 365, keine lokalen Bereitstellungen.</span><span class="sxs-lookup"><span data-stu-id="d105f-126">Office 365 or Microsoft 365, not on-premises deployments.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d105f-127"><strong>SecurityGroups</strong></span><span class="sxs-lookup"><span data-stu-id="d105f-127"><strong>SecurityGroups</strong></span></span></p></td>
    <td><p><span data-ttu-id="d105f-128">Definierte Sicherheitsgruppen, die steuern, welche Mitglieder von Sicherheitsgruppen Computer basierend auf dem Standort, an dem sie sich befinden, anzeigen können.</span><span class="sxs-lookup"><span data-stu-id="d105f-128">Defined security groups that control who (that is, members of the security groups) can see computers based on the site they are located in.</span></span> <span data-ttu-id="d105f-129">Website ist in diesem Kontext die Website, wie Sie im Topologie-Generator definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d105f-129">Site, in this context, is the site as defined in Topology Builder.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="d105f-130"><strong>Regions</strong></span><span class="sxs-lookup"><span data-stu-id="d105f-130"><strong>Regions</strong></span></span></p></td>
    <td><p><span data-ttu-id="d105f-131">Definierte Regionen werden verwendet, um Sicherheitsgruppen zu einer Region zusammenzufassen, beispielsweise EMEA.</span><span class="sxs-lookup"><span data-stu-id="d105f-131">Defined regions are used to collect SecurityGroups into a region, for example EMEA.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d105f-132"><strong>EtlFileFolder</strong></span><span class="sxs-lookup"><span data-stu-id="d105f-132"><strong>EtlFileFolder</strong></span></span></p></td>
    <td><p><span data-ttu-id="d105f-133">Definierter Pfad zu dem Speicherort, an dem Protokolldateien auf Computern geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="d105f-133">Defined path to the location where log files are written on computers.</span></span> <span data-ttu-id="d105f-134">CLSAgent schreibt die Protokolldateien und wird im Kontext des Netzwerkdiensts ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d105f-134">CLSAgent writes the log files and runs under the context of the Network Service.</span></span> <span data-ttu-id="d105f-135">In diesem Fall expandiert% Temp% zu%windir%\ServiceProfiles\NetworkService\AppData\Local</span><span class="sxs-lookup"><span data-stu-id="d105f-135">In this case, %TEMP% expands to %WINDIR%\ServiceProfiles\NetworkService\AppData\Local</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="d105f-136"><strong>EtlFileRolloverSizeMB</strong></span><span class="sxs-lookup"><span data-stu-id="d105f-136"><strong>EtlFileRolloverSizeMB</strong></span></span></p></td>
    <td><p><span data-ttu-id="d105f-p107">Dieser Parameter gibt die maximale Größe der Protokolldatei vor der Erstellung einer neuen ETL-Datei (Event Trace Log, Ereignis-Ablaufverfolgungsprotokoll) an. Wenn die definierte Größe erreicht ist, wird eine neue Protokolldatei erstellt, auch wenn die in EtlFileRolloverMinutes festgelegte maximale Zeit noch nicht erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="d105f-p107">The parameter indicates the maximum size of the log file before a new event trace log (.etl) file is created. A new log file is created when the defined size is reached even if the maximum time set in EtlFileRolloverMinutes has not yet been reached.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d105f-139"><strong>EtlFileRolloverMinutes</strong></span><span class="sxs-lookup"><span data-stu-id="d105f-139"><strong>EtlFileRolloverMinutes</strong></span></span></p></td>
    <td><p><span data-ttu-id="d105f-p108">Die definierte maximale Zeitspanne in Minuten, die für ein Protokoll verstreichen kann, bevor eine neue ETL-Datei erstellt wird. Wenn der Timer abläuft, wird eine neue Protokolldatei erstellt, auch wenn die in EtlFileRolloverSizeMB festgelegte maximale Größe noch nicht erreicht wurde.</span><span class="sxs-lookup"><span data-stu-id="d105f-p108">Defined maximum amount of time, in minutes, that a log can elapse before a new .etl file is created. A new log file is created when the timer expires even if the maximum size set in EtlFileRolloverSizeMB has not yet been reached.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="d105f-142"><strong>TmfFileSearchPath</strong></span><span class="sxs-lookup"><span data-stu-id="d105f-142"><strong>TmfFileSearchPath</strong></span></span></p></td>
    <td><p><span data-ttu-id="d105f-143">Speicherort, an dem nach den Formatdateien für Ablaufverfolgungsmeldungen gesucht wird.</span><span class="sxs-lookup"><span data-stu-id="d105f-143">Location to search for the trace message format files.</span></span> <span data-ttu-id="d105f-144">Die Dateien für das Trace-Nachrichtenformat werden verwendet, um die Binärdateien in ein menschlich lesbares Format umzuwandeln.</span><span class="sxs-lookup"><span data-stu-id="d105f-144">The trace message format files are used to convert the binary files into a human readable format.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d105f-145"><strong>CacheFileLocalFolders</strong></span><span class="sxs-lookup"><span data-stu-id="d105f-145"><strong>CacheFileLocalFolders</strong></span></span></p></td>
    <td><p><span data-ttu-id="d105f-p110">Definierter Pfad zu dem Speicherort, an dem Cachedateien auf Computer geschrieben werden. CLSAgent schreibt die Cachedatei und wird im Kontext des Netzwerkdiensts ausgeführt. In diesem Fall wird %TEMP% zu %WINDIR%\ServiceProfiles\NetworkService\AppData\Local erweitert. Standardmäßig werden Cache- und Protokolldateien in dasselbe Verzeichnis geschrieben.</span><span class="sxs-lookup"><span data-stu-id="d105f-p110">Defined path to the location where cache files are written on computers. CLSAgent writes the cache files and runs under the context of the Network Service. In this case, %TEMP% expands to %WINDIR%\ServiceProfiles\NetworkService\AppData\Local. By default, cache files and log files are written to the same directory.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="d105f-150"><strong>CacheFileNetworkFolder</strong></span><span class="sxs-lookup"><span data-stu-id="d105f-150"><strong>CacheFileNetworkFolder</strong></span></span></p></td>
    <td><p><span data-ttu-id="d105f-151">Sie können einen UNC-Pfad (Universal Naming Convention) definieren, um die Cachedateien während Protokollierungsvorgängen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="d105f-151">You can define a universal naming convention (UNC) path to receive the cache files during logging operations.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d105f-152"><strong>CacheFileLocalRetentionPeriod</strong></span><span class="sxs-lookup"><span data-stu-id="d105f-152"><strong>CacheFileLocalRetentionPeriod</strong></span></span></p></td>
    <td><p><span data-ttu-id="d105f-153">Definiert als die Höchstdauer in Tagen, für die Cachedateien beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="d105f-153">Defined as the maximum time, in days, that cache files are retained.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="d105f-154"><strong>CacheFileMaxDiskUsage</strong></span><span class="sxs-lookup"><span data-stu-id="d105f-154"><strong>CacheFileMaxDiskUsage</strong></span></span></p></td>
    <td><p><span data-ttu-id="d105f-155">Definiert als der prozentuale Anteil des Speicherplatzes, der von den Cachedateien verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="d105f-155">Defined as the percentage of disk space that can be used by the cache files.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d105f-156"><strong>ComponentThrottleLimit</strong></span><span class="sxs-lookup"><span data-stu-id="d105f-156"><strong>ComponentThrottleLimit</strong></span></span></p></td>
    <td><p><span data-ttu-id="d105f-157">Definiert als die Höchstzahl an Ablaufverfolgungen pro Sekunde, die eine Komponente erzeugen kann, bevor der automatische Drosselbegrenzer ausgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="d105f-157">Defined as the maximum number of traces per second that a component can produce before the automatic throttle limiter is triggered.</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="d105f-158"><strong>ComponentThrottleSample</strong></span><span class="sxs-lookup"><span data-stu-id="d105f-158"><strong>ComponentThrottleSample</strong></span></span></p></td>
    <td><p><span data-ttu-id="d105f-159">Anzahl der möglichen Überschreitungen von ComponentThrottleLimit in 60 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="d105f-159">Number of times in 60 seconds that the ComponentThrottleLimit can be exceeded.</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="d105f-160"><strong>MinimumClsAgentServiceVersion</strong></span><span class="sxs-lookup"><span data-stu-id="d105f-160"><strong>MinimumClsAgentServiceVersion</strong></span></span></p></td>
    <td><p><span data-ttu-id="d105f-161">Die mindestens erforderliche Version des CLSAgent, die ausgeführt werden kann.</span><span class="sxs-lookup"><span data-stu-id="d105f-161">The minimum version of the CLSAgent allowed to run.</span></span> <span data-ttu-id="d105f-162">Dieses Element ist für Office 365 oder Microsoft 365 vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="d105f-162">This element is intended for Office 365 or Microsoft 365.</span></span></p></td>
    </tr>
    </tbody>
    </table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d105f-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d105f-163">See Also</span></span>


[<span data-ttu-id="d105f-164">Übersicht über den zentralisierten Protokollierungsdienst in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d105f-164">Overview of the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-overview-of-the-centralized-logging-service.md)  


<span data-ttu-id="d105f-165">[Set-CsClsConfiguration](https://technet.microsoft.com/library/JJ619182(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d105f-165">[Set-CsClsConfiguration](https://technet.microsoft.com/library/JJ619182(v=OCS.15))</span></span>  
<span data-ttu-id="d105f-166">[Remove-CsClsConfiguration](https://technet.microsoft.com/library/JJ619191(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d105f-166">[Remove-CsClsConfiguration](https://technet.microsoft.com/library/JJ619191(v=OCS.15))</span></span>  
<span data-ttu-id="d105f-167">[New-CsClsConfiguration](https://technet.microsoft.com/library/JJ619177(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d105f-167">[New-CsClsConfiguration](https://technet.microsoft.com/library/JJ619177(v=OCS.15))</span></span>  
<span data-ttu-id="d105f-168">[Get-CsClsConfiguration](https://technet.microsoft.com/library/JJ619179(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="d105f-168">[Get-CsClsConfiguration](https://technet.microsoft.com/library/JJ619179(v=OCS.15))</span></span>  
  

<span data-ttu-id="d105f-169"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d105f-169"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

