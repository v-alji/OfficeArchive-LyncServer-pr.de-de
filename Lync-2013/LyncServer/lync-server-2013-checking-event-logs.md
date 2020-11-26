---
title: 'Lync Server 2013: Überprüfen von Ereignisprotokollen'
description: 'Lync Server 2013: Überprüfen von Ereignisprotokollen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Checking event logs
ms:assetid: 5500720d-c628-4dbd-84bc-a5becc39b99c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720914(v=OCS.15)
ms:contentKeyID: 63969602
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6617bde846fd38ab3282fd023b16e0a921f48920
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434928"
---
# <a name="checking-event-logs-in-lync-server-2013"></a><span data-ttu-id="a8250-103">Überprüfen von Ereignisprotokollen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a8250-103">Checking event logs in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a8250-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a8250-104">

<span> </span></span></span>

<span data-ttu-id="a8250-105">_**Letztes Änderungsdatum des Themas:** 2014-08-06_</span><span class="sxs-lookup"><span data-stu-id="a8250-105">_**Topic Last Modified:** 2014-08-06_</span></span>

<span data-ttu-id="a8250-106">Sie können die [Windows-Ereignisanzeige](https://go.microsoft.com/fwlink/p/?linkid=314067) verwenden, um Ereignisprotokolle anzuzeigen und Informationen zu Dienstfehlern, Replikationsfehlern in AD DS sowie Warnungen zu Systemressourcen wie virtuellem Arbeitsspeicher und Speicherplatz zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="a8250-106">You can use [Windows Event Viewer](https://go.microsoft.com/fwlink/p/?linkid=314067) to view event logs and obtain information about service failures, replication errors in the AD DS, and warnings about system resources such as virtual memory and disk space.</span></span> <span data-ttu-id="a8250-107">Die Ereignisanzeige ist im Lieferumfang von Windows Server 2008 und 2012 enthalten.</span><span class="sxs-lookup"><span data-stu-id="a8250-107">Event Viewer is included with Windows Server 2008 and 2012.</span></span>

<span data-ttu-id="a8250-108">Klicken Sie im lync Server 2013-Protokollierungstool beim Beenden der Debugsitzung auf **Protokolldateien analysieren** , um die Protokolldateien mithilfe des Snooper-Tools anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a8250-108">In the Lync Server 2013 Logging Tool, when you end the debug session, click **Analyze Log Files** to view the log files by using the Snooper tool.</span></span>

<span data-ttu-id="a8250-109">Die Ereignisanzeige verwaltet Protokolle zu Anwendungs-, Sicherheits-und Systemereignissen auf dem Computer.</span><span class="sxs-lookup"><span data-stu-id="a8250-109">Event Viewer maintains logs about application, security, and system events on the computer.</span></span> <span data-ttu-id="a8250-110">Sowohl lync Server 2013 als auch Windows melden Warnungen und Fehlerbedingungen für die Ereignisprotokolle.</span><span class="sxs-lookup"><span data-stu-id="a8250-110">Both Lync Server 2013 and Windows report warnings and error conditions to the event logs.</span></span> <span data-ttu-id="a8250-111">Überprüfen Sie daher die Ereignisprotokolle täglich.</span><span class="sxs-lookup"><span data-stu-id="a8250-111">Therefore, review event logs daily.</span></span>

<span data-ttu-id="a8250-112">Verwenden Sie die Ereignisanzeige für folgende Zwecke:</span><span class="sxs-lookup"><span data-stu-id="a8250-112">Use Event Viewer to:</span></span>

  - <span data-ttu-id="a8250-113">Anzeigen und Verwalten von Ereignisprotokollen</span><span class="sxs-lookup"><span data-stu-id="a8250-113">View and manage event logs.</span></span>

  - <span data-ttu-id="a8250-114">Abrufen von Informationen zu Hardware-, Software-und Systemproblemen, die aufgelöst werden müssen.</span><span class="sxs-lookup"><span data-stu-id="a8250-114">Obtain information about hardware, software, and system issues that must be resolved.</span></span>

  - <span data-ttu-id="a8250-115">Erkennen von Trends, die eine zukünftige Aktion erfordern</span><span class="sxs-lookup"><span data-stu-id="a8250-115">Identify trends that require future action.</span></span>

<span data-ttu-id="a8250-116">Ein Server, auf dem lync Server unter einem Windows Server-Betriebssystem ausgeführt wird, zeichnet Ereignisse in vier Typen von Protokollen auf:</span><span class="sxs-lookup"><span data-stu-id="a8250-116">A server that is running Lync Server on a Windows Server operating system records events in four types of logs:</span></span>

  - <span data-ttu-id="a8250-117">**Anwendungsprotokolle**   Das Anwendungsprotokoll enthält Ereignisse, die von Anwendungen oder Programmen protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="a8250-117">**Application logs**   The Application log contains events logged by applications or programs.</span></span> <span data-ttu-id="a8250-118">Entwickler legen fest, welche Ereignisse protokolliert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a8250-118">Developers determine which events to log.</span></span> <span data-ttu-id="a8250-119">Beispielsweise kann ein Datenbankprogramm einen Datei Fehler im Anwendungsprotokoll aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="a8250-119">For example, a database program might record a file error in the Application log.</span></span> <span data-ttu-id="a8250-120">Die meisten Ereignisse im Zusammenhang mit lync Server 2013 werden im Anwendungsprotokoll angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a8250-120">Most Lync Server 2013-related events appear in the Application log.</span></span>

  - <span data-ttu-id="a8250-121">**Sicherheitsprotokolle**   Das Sicherheitsprotokoll zeichnet Ereignisse wie gültige und ungültige Anmeldeversuche zusätzlich zu Ereignissen auf, die sich auf die Ressourcennutzung beziehen, wie das Erstellen, öffnen oder Löschen von Dateien oder anderen Objekten.</span><span class="sxs-lookup"><span data-stu-id="a8250-121">**Security logs**   The Security log records events such as valid and not valid logon tries in addition to events related to resource use such as creating, opening, or deleting files or other objects.</span></span> <span data-ttu-id="a8250-122">Wenn beispielsweise die Anmeldeüberwachung aktiviert ist, werden Versuche zur Anmeldung am System im Sicherheitsprotokoll aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a8250-122">For example, if logon auditing is enabled, attempts to log on to the system are recorded in the Security log.</span></span>

  - <span data-ttu-id="a8250-123">**System Protokolle**   Das Systemprotokoll enthält Ereignisse, die von Windows-Systemkomponenten protokolliert werden.</span><span class="sxs-lookup"><span data-stu-id="a8250-123">**System logs**   The System log contains events logged by Windows system components.</span></span> <span data-ttu-id="a8250-124">Beispielsweise wird der Fehler eines Treibers oder einer anderen Systemkomponente zum Laden während des Starts im Systemprotokoll aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="a8250-124">For example, the failure of a driver or other system component to load during startup is recorded in the System log.</span></span> <span data-ttu-id="a8250-125">Die von Systemkomponenten protokollierten Ereignistypen sind vom Server vorgegeben.</span><span class="sxs-lookup"><span data-stu-id="a8250-125">The event types logged by system components are predetermined by the server.</span></span>

  - <span data-ttu-id="a8250-126">**Lync Server 2013**   Das Protokollierungstool zeichnet wichtige Ereignisse auf, die sich auf Authentifizierung, Verbindungen und Benutzeraktionen beziehen.</span><span class="sxs-lookup"><span data-stu-id="a8250-126">**Lync Server 2013**   The logging tool records significant events related to authentication, connections, and user actions.</span></span> <span data-ttu-id="a8250-127">Nachdem Sie die Diagnoseprotokollierung aktiviert haben, können Sie die Protokolleinträge in der Ereignisanzeige anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a8250-127">After enabling diagnostic logging, you can view the log entries in Event Viewer.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a8250-128">Es wird nicht empfohlen, die maximalen Protokollierungseinstellungen zu verwenden, es sei denn, Sie werden von den Microsoft-Kundendienst angewiesen.</span><span class="sxs-lookup"><span data-stu-id="a8250-128">We do not recommend that you use the maximum logging settings unless you are instructed to do this by Microsoft Customer Support Services.</span></span> <span data-ttu-id="a8250-129">Die maximale Protokollierung führt zu erheblichen Ressourcen und kann viele "falsch positive" geben, das heißt, Fehler, die nur bei maximaler Protokollierung protokolliert werden, aber wirklich erwartet werden und keine Besorgnis erregend sind.</span><span class="sxs-lookup"><span data-stu-id="a8250-129">Maximum logging drains significant resources and can give many “false positives,” that is, errors that get logged only at maximum logging but are really expected and are not a cause of concern.</span></span> <span data-ttu-id="a8250-130">Wir empfehlen außerdem, die Diagnoseprotokollierung nicht dauerhaft zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a8250-130">We also recommend that you do not enable diagnostic logging permanently.</span></span> <span data-ttu-id="a8250-131">Verwenden Sie es nur bei der Problembehandlung.</span><span class="sxs-lookup"><span data-stu-id="a8250-131">Use it only when troubleshooting.</span></span>



</div>

<span data-ttu-id="a8250-132">In jedem Ereignisanzeigeprotokoll zeichnet lync Server 2013 Informations-, Warnungs-und Fehlerereignisse auf.</span><span class="sxs-lookup"><span data-stu-id="a8250-132">Within each Event Viewer log, Lync Server 2013 records informational, warning, and error events.</span></span> <span data-ttu-id="a8250-133">Überwachen Sie diese Protokolle genau, um die Typen von Transaktionen zu verfolgen, die auf den lync Server 2013-Servern durchgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a8250-133">Monitor these logs closely to track the types of transactions being conducted on the Lync Server 2013 servers.</span></span> <span data-ttu-id="a8250-134">Sie sollten die Protokolle in regelmäßigen Abständen archivieren oder das automatische Rollover verwenden, um nicht genügend Speicherplatz zu schaffen.</span><span class="sxs-lookup"><span data-stu-id="a8250-134">You should periodically archive the logs or use automatic rollover to avoid running out of space.</span></span> <span data-ttu-id="a8250-135">Da Protokolldateien eine begrenzte Menge an Speicherplatz belegen können, erhöhen Sie die Protokollgröße (beispielsweise auf 50 MB), und legen Sie Sie auf Overwrite fest, damit der lync Server 2013-Server weiterhin neue Ereignisse schreiben kann.</span><span class="sxs-lookup"><span data-stu-id="a8250-135">Because log files can occupy a finite amount of space, increase the log size (for example, to 50 MB) and set it to overwrite so that the Lync Server 2013 Server can continue to write new events.</span></span>

<span data-ttu-id="a8250-136">Sie können die Ereignisprotokollverwaltung auch mithilfe der folgenden Tools und Technologien automatisieren:</span><span class="sxs-lookup"><span data-stu-id="a8250-136">You can also automate event log administration by using the following tools and technologies:</span></span>

  - <span data-ttu-id="a8250-137">System Center Operations Manager überwacht den Zustand und die Verwendung von lync Server 2013-Servern.</span><span class="sxs-lookup"><span data-stu-id="a8250-137">System Center Operations Manager monitors the health and use of Lync Server 2013 servers.</span></span> <span data-ttu-id="a8250-138">Das lync Server 2013 Management Pack für Operations Manager erweitert Operations Manager durch die Bereitstellung spezieller Überwachung für Server, auf denen lync Server 2013 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a8250-138">Lync Server 2013 Management Pack for Operations Manager extends Operations Manager by providing specialized monitoring for servers that are running Lync Server 2013.</span></span>

  - <span data-ttu-id="a8250-139">Das lync Server 2013-Management Pack für Operations Manager überwacht die Standard-und Enterprise-Edition von lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a8250-139">The Lync Server 2013 Management Pack for Operations Manager monitors Standard and Enterprise Edition of Lync Server 2013.</span></span> <span data-ttu-id="a8250-140">Diese Version enthält auch das QoE-Management Pack (Quality of Experience), das zuvor ein separates Management Pack war.</span><span class="sxs-lookup"><span data-stu-id="a8250-140">This release also incorporates the Quality of Experience (QoE) Management Pack which was previously a separate management pack.</span></span>

<span data-ttu-id="a8250-141">Überwachte Typen sind Ereignisprotokolleinträge, Leistungsindikatoren und statusbehaftete Überwachung von QoE.</span><span class="sxs-lookup"><span data-stu-id="a8250-141">Monitored types are event log entries, performance counters and stateful monitoring of QoE.</span></span> <span data-ttu-id="a8250-142">Diese Version des Management Packs überwacht nur lync Server 2013 und 2010 und kann nicht zum Überwachen von Office Communications Server 2007 verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a8250-142">This version of the management pack only monitors Lync Server 2013 and 2010, and cannot be used to monitor Office Communications Server 2007.</span></span>

<span data-ttu-id="a8250-143">Das Management Pack bietet die folgenden Features:</span><span class="sxs-lookup"><span data-stu-id="a8250-143">The management pack provides the following features:</span></span>

  - <span data-ttu-id="a8250-144">Benachrichtigungen, die darauf hindeuten, dass der Dienst Auswirkungen auf Ereignisse hat</span><span class="sxs-lookup"><span data-stu-id="a8250-144">Alerts indicating service affecting events</span></span>

  - <span data-ttu-id="a8250-145">Warnungen, die die Konfiguration angeben, und andere Probleme, die sich nicht auf Dienste auswirken</span><span class="sxs-lookup"><span data-stu-id="a8250-145">Alerts indicating configuration, and other non-service impacting issues</span></span>

  - <span data-ttu-id="a8250-146">Statusüberwachung der lync Server-Dienste</span><span class="sxs-lookup"><span data-stu-id="a8250-146">State monitoring of Lync Server services</span></span>

  - <span data-ttu-id="a8250-147">Produkt wissen: Ursache und Lösung identifizierter Probleme</span><span class="sxs-lookup"><span data-stu-id="a8250-147">Product knowledge: Cause and resolution of identified issues</span></span>

<span data-ttu-id="a8250-148">Weitere Informationen zum lync Server 2013 Management Pack finden Sie unter über [Wachen von lync Server 2013 mit System Center Operations Manager](lync-server-2013-monitoring-lync-server-with-system-center-operations-manager.md).</span><span class="sxs-lookup"><span data-stu-id="a8250-148">For more information about Lync Server 2013 Management Pack, refer to [Monitoring Lync Server 2013 with System Center Operations Manager](lync-server-2013-monitoring-lync-server-with-system-center-operations-manager.md).</span></span>

<span data-ttu-id="a8250-149">**Ereignis Kamm**   Das Event Comb-Tool sammelt bestimmte Ereignisse aus den Ereignisprotokollen mehrerer Computer an einem zentralen Speicherort.</span><span class="sxs-lookup"><span data-stu-id="a8250-149">**Event Comb**   The Event Comb tool collects specific events from the event logs of several computers to one central location.</span></span> <span data-ttu-id="a8250-150">Damit können Sie nur die Ereignis-IDs oder Ereignisquellen melden, die Sie angeben.</span><span class="sxs-lookup"><span data-stu-id="a8250-150">It lets you report on only the event IDs or event sources it specifies.</span></span> <span data-ttu-id="a8250-151">Weitere Informationen zum Event Comb finden Sie auf der Website [Kontosperrung und Verwaltungs Tools](https://go.microsoft.com/fwlink/?linkid=35607) .</span><span class="sxs-lookup"><span data-stu-id="a8250-151">For more information about Event Comb, see the [Account Lockout and Management Tools](https://go.microsoft.com/fwlink/?linkid=35607) website.</span></span>

<span data-ttu-id="a8250-152">**Ereignisauslöser**   In Windows Server 2012 können Sie in der Windows-Ereignisanzeige eine Aufgabe an dieses Ereignis anfügen, in der ein Administrator entweder ein Programm ausführen, eine e-Mail-Nachricht senden oder eine auf dem Bildschirm angezeigte Nachricht anzeigen kann.</span><span class="sxs-lookup"><span data-stu-id="a8250-152">**Event triggers**   In Windows Server 2012 you can "Attach a Task to This Event" within the Windows Event Viewer—where an administrator can either run a program, send an email message or display an on-screen message.</span></span> <span data-ttu-id="a8250-153">Weitere Informationen zu diesem Feature finden Sie unter Windows Server 2008 R2-Thema [Ausführen einer Aufgabe als Antwort auf ein bestimmtes Ereignis](https://technet.microsoft.com/library/cc748900.aspx).</span><span class="sxs-lookup"><span data-stu-id="a8250-153">For more information about this feature, see the Windows Server 2008 R2 topic [Run a Task in Response to a Given Event](https://technet.microsoft.com/library/cc748900.aspx).</span></span> <span data-ttu-id="a8250-154">Sie können auch Befehlszeilentools wie "Eventtrigger.exe" verwenden, um Ereignisprotokolle zu erstellen und zu Abfragen und Programme mit bestimmten protokollierten Ereignissen zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="a8250-154">You can also use command-line tools such as ‘Eventtrigger.exe’ to create and query event logs and associate programs with particular logged events.</span></span> <span data-ttu-id="a8250-155">Mithilfe von Eventtriggers.exe können Sie Ereignisauslöser erstellen, die Programme ausführen, wenn bestimmte Ereignisse auftreten.</span><span class="sxs-lookup"><span data-stu-id="a8250-155">By using Eventtriggers.exe, you can create event triggers that run programs when specific events occur.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="a8250-156">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8250-156">See Also</span></span>


[<span data-ttu-id="a8250-157">Windows-Ereignisanzeige</span><span class="sxs-lookup"><span data-stu-id="a8250-157">Windows Event Viewer</span></span>](https://go.microsoft.com/fwlink/p/?linkid=314067)  
  

<span data-ttu-id="a8250-158"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a8250-158"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

