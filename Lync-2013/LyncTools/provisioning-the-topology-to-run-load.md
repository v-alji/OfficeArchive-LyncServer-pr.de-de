---
title: Bereitstellen der Topologie zum Ausführen der Auslastung
description: Bereitstellen der Topologie zum Ausführen der Auslastung
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Provisioning the Topology to Run Load
ms:assetid: 6fba03df-3914-4d2a-8208-e252ad993aff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945598(v=OCS.15)
ms:contentKeyID: 51541424
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: da482fde949675acc1722305433b95b7a6a6b523
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446423"
---
# <a name="provisioning-the-topology-to-run-load"></a><span data-ttu-id="aed00-103">Bereitstellen der Topologie zum Ausführen der Auslastung</span><span class="sxs-lookup"><span data-stu-id="aed00-103">Provisioning the Topology to Run Load</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aed00-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aed00-104">

<span> </span></span></span>

<span data-ttu-id="aed00-105">_**Letztes Änderungsdatum des Themas:** 2013-02-04_</span><span class="sxs-lookup"><span data-stu-id="aed00-105">_**Topic Last Modified:** 2013-02-04_</span></span>

<div>

<span data-ttu-id="aed00-106">Je nach den vorhandenen Einstellungen und der Konfiguration von lync Server 2013 müssen Sie möglicherweise die folgenden Änderungen in Ihrer Umgebung vornehmen:</span><span class="sxs-lookup"><span data-stu-id="aed00-106">Depending on your existing settings and configuration of Lync Server 2013, you may need to make the following changes in your environment:</span></span>

1.  <span data-ttu-id="aed00-107">Setzen Sie die Windows PowerShell-Ausführungsrichtlinie auf Unrestricted.</span><span class="sxs-lookup"><span data-stu-id="aed00-107">Set the Windows PowerShell execution policy to Unrestricted.</span></span> <span data-ttu-id="aed00-108">Um die Einstellungen für die Ausführungsrichtlinie zu überprüfen, öffnen Sie die lync Server-Verwaltungsshell, und führen Sie den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="aed00-108">To check your execution policy settings, open the Lync Server Management Shell and run the following command:</span></span>

    ``` powershell
        Get-ExecutionPolicy
    ```        

    <span data-ttu-id="aed00-109">Wenn dieser Befehl nicht den Wert Unrestricted zurückgibt, führen Sie diesen Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="aed00-109">If this command does not return the value Unrestricted, run this command:</span></span>

    ``` powershell
        Set-ExecutionPolicy -Unrestricted
    ```

2.  <span data-ttu-id="aed00-110">Um lync Server 2013 effektiv zu konfigurieren, müssen Sie Folgendes tun:</span><span class="sxs-lookup"><span data-stu-id="aed00-110">To effectively configure Lync Server 2013, you will need to:</span></span>
    
      - <span data-ttu-id="aed00-111">Mit der lync Server 2013-Topologie vertraut sein (beispielsweise Computernamen, Dienstinstanzen, Websitenamen und Richtlinien).</span><span class="sxs-lookup"><span data-stu-id="aed00-111">Be familiar with Lync Server 2013 topology (for example, computer names, service instances, site names, and policies).</span></span>
    
      - <span data-ttu-id="aed00-112">Weisen Sie einige der Benutzer zu, die Gruppen erstellt wurden, wie etwa Gruppen-Sammelanschlüsse (beispielsweise SIP-URIs).</span><span class="sxs-lookup"><span data-stu-id="aed00-112">Assign some of the users that were created to groups, such as Response Group hunt groups (for example, SIP URIs).</span></span>

3.  <span data-ttu-id="aed00-113">Wenn Sie das Skript über die Befehlszeile ausführen möchten, können Sie Folgendes verwenden:</span><span class="sxs-lookup"><span data-stu-id="aed00-113">To run the script from the command line, you may use:</span></span>

    ``` powershell
        Powershell.exe -file <path to the file>
    ```
    
4.  <span data-ttu-id="aed00-114">In der Regel wird nach einem der Skripts in diesem Paket die resultierenden Ablaufverfolgungen aus dem Skript in einer Datei im gleichen Pfad gespeichert, aus dem das Skript aufgerufen wurde, mit dem Namen \<scriptname\> $h $ m $s.txt.</span><span class="sxs-lookup"><span data-stu-id="aed00-114">Typically, after one of the scripts in this package runs, the resulting traces from the script will be stored in a file in the same path from which the script was invoked, named \<scriptname\>$h$m$s.txt.</span></span> <span data-ttu-id="aed00-115">Beispiel: Ausführen von ArchivingPolicy.ps1 um 12:15 Uhr</span><span class="sxs-lookup"><span data-stu-id="aed00-115">For example, running ArchivingPolicy.ps1 at 12:15 P.M.</span></span> <span data-ttu-id="aed00-116">wird eine Protokolldatei wie ArchivingPolicy121500.txt generiert.</span><span class="sxs-lookup"><span data-stu-id="aed00-116">will generate a log file such as ArchivingPolicy121500.txt.</span></span>

5.  <span data-ttu-id="aed00-117">Beachten Sie abschließend, dass Sie zwar Beispiele für die Konfiguration des Servers bereitgestellt haben, Sie aber für das ändern oder Löschen der Konfiguration verantwortlich sind, nachdem Sie die Auslastung ausgeführt haben.</span><span class="sxs-lookup"><span data-stu-id="aed00-117">Finally, note that although we have provided examples to configure the server, you are responsible for modifying or deleting the configuration after you have finished running the load.</span></span>

<span data-ttu-id="aed00-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aed00-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

