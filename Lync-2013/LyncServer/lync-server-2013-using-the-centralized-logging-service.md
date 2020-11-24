---
title: 'Lync Server 2013: Verwenden des zentralen Protokollierungsdiensts'
description: 'Lync Server 2013: Verwenden des zentralisierten Protokollierungsdiensts.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using the Centralized Logging Service
ms:assetid: 7b05aaef-f0ea-4649-ba8a-02e68b0cdf23
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688101(v=OCS.15)
ms:contentKeyID: 49733700
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f8b9edf839de889e9f0b01c10311f6b5c70ced8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395295"
---
# <a name="using-the-centralized-logging-service-in-lync-server-2013"></a><span data-ttu-id="d094f-103">Verwenden des zentralisierten Protokollierungsdiensts in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d094f-103">Using the Centralized Logging Service in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d094f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d094f-104">

<span> </span></span></span>

<span data-ttu-id="d094f-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="d094f-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="d094f-106">Der zentralisierte Protokollierungsdienst ist ein neues Feature in lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d094f-106">The Centralized Logging Service is a new feature in Lync Server 2013.</span></span> <span data-ttu-id="d094f-107">Es handelt sich um einen verbesserten Ersatz für die **OCSLogger** -und **OCSTracer** -Tools, die in früheren Versionen bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="d094f-107">It is an enhanced replacement for the **OCSLogger** and **OCSTracer** tools that were provided in previous releases.</span></span> <span data-ttu-id="d094f-108">Sie können den zentralisierten Protokollierungsdienst verwenden, um die folgenden Aufgaben auszuführen:</span><span class="sxs-lookup"><span data-stu-id="d094f-108">You can use the Centralized Logging Service to perform the following tasks:</span></span>

  - <span data-ttu-id="d094f-109">Starten Sie die Protokollierung an einem oder mehreren Computern und Pools von einem einzelnen Standort und Befehl aus.</span><span class="sxs-lookup"><span data-stu-id="d094f-109">Start logging on one or more computers and pools from a single location and command.</span></span>

  - <span data-ttu-id="d094f-110">Beenden Sie die Protokollierung an einem oder mehreren Computern und Pools an einem einzigen Speicherort und Befehl.</span><span class="sxs-lookup"><span data-stu-id="d094f-110">Stop logging on one or more computers and pools from a single location and command.</span></span>

  - <span data-ttu-id="d094f-111">Durchsuchen von Protokollen auf einem oder mehreren Computern und Pools für einen einzelnen Standort und Befehl.</span><span class="sxs-lookup"><span data-stu-id="d094f-111">Search logs on one or more computers and pools for a single location and command.</span></span> <span data-ttu-id="d094f-112">Sie können den Suchbefehl so anpassen, dass die gesamte Aggregation von Protokollen zurückgegeben wird, die auf allen Computern erfasst und gespeichert wurden, oder Sie können ein gekürztes Ergebnis zurückgeben, in dem bestimmte Daten erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="d094f-112">You can tailor the search command to return the entire aggregation of logs that were captured and stored on all machines, or return a trimmed-down result that captures specific data.</span></span>

  - <span data-ttu-id="d094f-113">Konfigurieren Sie die Protokollierungssitzungen wie folgt:</span><span class="sxs-lookup"><span data-stu-id="d094f-113">Configure logging sessions as follows:</span></span>
    
      - <span data-ttu-id="d094f-114">Definieren Sie ein **Szenario** oder verwenden Sie ein Standardszenario.</span><span class="sxs-lookup"><span data-stu-id="d094f-114">Define a **Scenario**, or use a default scenario.</span></span> <span data-ttu-id="d094f-115">Ein *Szenario* im zentralisierten Protokollierungsdienst besteht aus dem Bereich (Global oder Website), einem Szenarionamen zur Identifizierung des Zwecks des Szenarios und einem oder mehreren Anbietern.</span><span class="sxs-lookup"><span data-stu-id="d094f-115">A *scenario* in Centralized Logging Service is made up of scope (global or site), a scenario name to identify the purpose of the scenario, and one or more providers.</span></span> <span data-ttu-id="d094f-116">Sie können zwei Szenarios zu einem beliebigen Zeitpunkt auf einem Computer ausführen.</span><span class="sxs-lookup"><span data-stu-id="d094f-116">You can run two scenarios at any given time on a computer.</span></span>
    
      - <span data-ttu-id="d094f-p104">Sie können einen vorhandenen *Anbieter* verwenden oder einen neuen Anbieter erstellen. Der *Anbieter* definiert, was bei der Protokollierungssitzung erfasst wird, welche Detailebene gilt, welche Komponenten nachverfolgt werden und welche Flags angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="d094f-p104">Use an existing *provider* or create a new provider. A *provider* defines what the logging session collects, what level of detail, what components to trace, and what flags are applied.</span></span>
        
        <div>
        

        > [!TIP]  
        > <span data-ttu-id="d094f-119">Wenn Sie mit der Verwendung von OCSLogger vertraut sind: Der Begriff <EM>Anbieter</EM> bezieht sich auf die Sammlung der <STRONG>Komponenten</STRONG> (z. B. S4, SIPStack), einen <STRONG>Protokollierungstyp</STRONG> (z. B. WPP, EventLog oder IIS logfile), eine <STRONG>Ablaufverfolgungsstufe</STRONG> (z. B. All, verbose, debug) sowie <STRONG>Flags</STRONG> (z. B. TF_COMPONENT, TF_DIAG).</span><span class="sxs-lookup"><span data-stu-id="d094f-119">If you are familiar with OCSLogger, the term <EM>providers</EM> refers to the collection of <STRONG>components</STRONG> (for example, S4, SIPStack), a <STRONG>logging type</STRONG> (for example, WPP, EventLog, or IIS logfile), a <STRONG>tracing level</STRONG> (for example, All, verbose, debug), and <STRONG>flags</STRONG> (for example, TF_COMPONENT, TF_DIAG).</span></span> <span data-ttu-id="d094f-120">Diese Elemente werden im Anbieter (eine Windows PowerShell-Variable) definiert und an den Befehl "zentralisierter Protokollierungsdienst" übergeben.</span><span class="sxs-lookup"><span data-stu-id="d094f-120">These items are defined in the provider (a Windows PowerShell variable) and passed into the Centralized Logging Service command.</span></span>

        
        </div>
    
      - <span data-ttu-id="d094f-121">Konfigurieren Sie die Computer und Pools, aus denen Sie Protokolle sammeln möchten.</span><span class="sxs-lookup"><span data-stu-id="d094f-121">Configure the computers and pools that you want to collect logs from.</span></span>
    
      - <span data-ttu-id="d094f-122">Definieren Sie den Bereich für die Protokollierungssitzung auf der **Seite** "Optionen" (nur Protokollierungs Aufzeichnungen auf Computern auf dieser Website) oder **Global** (Ausführen der Protokollierungs Aufzeichnung auf allen Computern in der Bereitstellung).</span><span class="sxs-lookup"><span data-stu-id="d094f-122">Define the scope for the logging session from the options **Site** (run logging captures on computers in that site only), or **Global** (run logging capture on all computers in the deployment).</span></span>

<span data-ttu-id="d094f-123">Der zentralisierte Protokollierungsdienst ist äußerst leistungsstark und kann nahezu alle Anforderungen für die Problembehandlung erfüllen – groß oder klein.</span><span class="sxs-lookup"><span data-stu-id="d094f-123">The Centralized Logging Service is extremely powerful and can meet nearly all of the needs for troubleshooting problems—large or small.</span></span> <span data-ttu-id="d094f-124">Von der Ursachenanalyse bis zu Leistungsproblemen kann der zentralisierte Protokollierungsdienst ein wichtiges Tool für jeden Administrator sein.</span><span class="sxs-lookup"><span data-stu-id="d094f-124">From root cause analysis to performance problems, the Centralized Logging Service can be an important tool for any administrator.</span></span> <span data-ttu-id="d094f-125">Alle Beispiele werden mithilfe der lync Server-Verwaltungsshell angezeigt.</span><span class="sxs-lookup"><span data-stu-id="d094f-125">All examples are shown using the Lync Server Management Shell.</span></span> <span data-ttu-id="d094f-126">Es gibt eine Befehlszeilenkomponente für den zentralisierten Protokollierungsdienst namens " **CLSController.exe**".</span><span class="sxs-lookup"><span data-stu-id="d094f-126">There is a command-line component for the Centralized Logging Service called **CLSController.exe**.</span></span> <span data-ttu-id="d094f-127">Hilfe wird für das Befehlszeilentool über das Tool selbst bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="d094f-127">Help is provided for the command-line tool through the tool itself.</span></span> <span data-ttu-id="d094f-128">Es gibt jedoch eine begrenzte Anzahl von Funktionen, die Sie über die Befehlszeile ausführen können.</span><span class="sxs-lookup"><span data-stu-id="d094f-128">However, there is a limited set of functions that you can execute from the command line.</span></span> <span data-ttu-id="d094f-129">Mithilfe der lync Server-Verwaltungsshell haben Sie Zugriff auf eine viel größere und viel mehr konfigurierbare Gruppe von Features.</span><span class="sxs-lookup"><span data-stu-id="d094f-129">By using Lync Server Management Shell, you have access to a much larger and much more configurable set of features.</span></span> <span data-ttu-id="d094f-130">Wenn Sie den zentralisierten Protokollierungsdienst verwenden, sollten Sie die lync Server-Verwaltungsshell immer als die erste und wichtigste Methode beachten.</span><span class="sxs-lookup"><span data-stu-id="d094f-130">You should always consider Lync Server Management Shell as the first and foremost method when using the Centralized Logging Service.</span></span>

<span data-ttu-id="d094f-131">In den Themen in diesem Abschnitt wird erläutert, wie der zentralisierte Protokollierungsdienst und Beispiele für die Verwendung der zahlreichen Features verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d094f-131">The topics in this section explain how to use the Centralized Logging Service and examples of how to use its many features.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d094f-132">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d094f-132">In This Section</span></span>

  - [<span data-ttu-id="d094f-133">Übersicht über den zentralisierten Protokollierungsdienst in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d094f-133">Overview of the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-overview-of-the-centralized-logging-service.md)

  - [<span data-ttu-id="d094f-134">Verwalten der Konfigurationseinstellungen für den zentralisierten Protokollierungsdienst in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d094f-134">Managing the Centralized Logging Service configuration settings in Lync Server 2013</span></span>](lync-server-2013-managing-the-centralized-logging-service-configuration-settings.md)

  - [<span data-ttu-id="d094f-135">Grundlegendes zu den Konfigurationseinstellungen für den zentralisierten Protokollierungsdienst in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d094f-135">Understanding Centralized Logging Service configuration settings in Lync Server 2013</span></span>](lync-server-2013-understanding-centralized-logging-service-configuration-settings.md)

  - [<span data-ttu-id="d094f-136">Verwenden von "Start" für den zentralisierten Protokollierungsdienst zum Aufzeichnen von Protokollen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d094f-136">Using Start for the Centralized Logging Service to capture logs in Lync Server 2013</span></span>](lync-server-2013-using-start-for-the-centralized-logging-service-to-capture-logs.md)

  - [<span data-ttu-id="d094f-137">Verwenden von "beenden" für den zentralisierten Protokollierungsdienst in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d094f-137">Using Stop for the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-using-stop-for-the-centralized-logging-service.md)

  - [<span data-ttu-id="d094f-138">Verwenden der Suche in Aufzeichnungs Protokollen, die vom zentralisierten Protokollierungsdienst in lync Server 2013 erstellt wurden</span><span class="sxs-lookup"><span data-stu-id="d094f-138">Using search on capture logs created by the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-using-search-on-capture-logs-created-by-the-centralized-logging-service.md)

  - [<span data-ttu-id="d094f-139">Lesen von Aufnahme Protokollen vom zentralisierten Protokollierungsdienst in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d094f-139">Reading capture logs from the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-reading-capture-logs-from-the-centralized-logging-service.md)

<span data-ttu-id="d094f-140"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d094f-140"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

