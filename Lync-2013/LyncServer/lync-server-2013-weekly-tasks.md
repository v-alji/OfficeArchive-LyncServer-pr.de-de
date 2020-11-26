---
title: 'Lync Server 2013: Wöchentliche Aufgaben'
description: 'Lync Server 2013: wöchentliche Aufgaben.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Weekly tasks
ms:assetid: d564839b-b49d-4c5d-b67e-dc5abb0f6980
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn722432(v=OCS.15)
ms:contentKeyID: 63969650
ms.date: 08/20/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d818e1140141a470bb57a1471bb04931f505a6bd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443846"
---
# <a name="weekly-tasks-in-lync-server-2013"></a><span data-ttu-id="f7138-103">Wöchentliche Aufgaben in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f7138-103">Weekly tasks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f7138-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f7138-104">

<span> </span></span></span>

<span data-ttu-id="f7138-105">_**Letztes Änderungsdatum des Themas:** 2015-08-17_</span><span class="sxs-lookup"><span data-stu-id="f7138-105">_**Topic Last Modified:** 2015-08-17_</span></span>

<span data-ttu-id="f7138-106">Wöchentliche Aufgaben sind im Allgemeinen mit dem sammeln und Analysieren von Protokollen und Berichten verbunden.</span><span class="sxs-lookup"><span data-stu-id="f7138-106">Weekly tasks are generally related to collecting and analyzing logs and reports.</span></span>

<div>

## <a name="archive-event-logs"></a><span data-ttu-id="f7138-107">Archivieren von Ereignisprotokollen</span><span class="sxs-lookup"><span data-stu-id="f7138-107">Archive event logs</span></span>

<span data-ttu-id="f7138-108">Wenn Ereignisprotokolle nicht so konfiguriert sind, dass Ereignisse nach Bedarf überschrieben werden, müssen Sie regelmäßig archiviert und gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="f7138-108">If event logs are not configured to overwrite events as required, they must be regularly archived and deleted.</span></span> <span data-ttu-id="f7138-109">Diese Aktion ist besonders wichtig für Sicherheitsprotokolle, die möglicherweise bei der Untersuchung von Sicherheitsverstößen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="f7138-109">This action is especially important for security logs, which may be required when investigating attempted security breaches.</span></span>

<span data-ttu-id="f7138-110">In Ihrer Organisation müssen Richtlinien und Verfahren für die Protokoll Archivierung definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f7138-110">Your organization will have to define policies and procedures for log archiving.</span></span>

</div>

<div>

## <a name="create-reports"></a><span data-ttu-id="f7138-111">Berichte erstellen</span><span class="sxs-lookup"><span data-stu-id="f7138-111">Create reports</span></span>

<span data-ttu-id="f7138-112">Erstellen Sie Statusberichte, die Ihnen bei der Kapazitätsplanung, SLA-Bewertungen und Leistungsanalyse helfen.</span><span class="sxs-lookup"><span data-stu-id="f7138-112">Create status reports to help with capacity planning, SLA reviews, and performance analysis.</span></span> <span data-ttu-id="f7138-113">Verwenden Sie tägliche Daten aus dem Ereignisprotokoll und dem System Monitor, um Berichte auf Datenträger, Arbeitsspeicher und CPU-Auslastung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7138-113">Use daily data from event log and System Monitor to create reports on disk, memory, and CPU usage.</span></span> <span data-ttu-id="f7138-114">Verwenden Sie System Center Operations Manager, um Verfügbarkeits-und Verfügbarkeitsberichte zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="f7138-114">Use System Center Operations Manager to generate uptime and availability reports.</span></span>

<span data-ttu-id="f7138-115">In Ihrer Organisation müssen Richtlinien und Verfahren für Statusberichte definiert werden.</span><span class="sxs-lookup"><span data-stu-id="f7138-115">Your organization will have to define policies and procedures for status reports.</span></span>

</div>

<div>

## <a name="incident-reports"></a><span data-ttu-id="f7138-116">Vorfallberichte</span><span class="sxs-lookup"><span data-stu-id="f7138-116">Incident reports</span></span>

<span data-ttu-id="f7138-117">Führen Sie eine wöchentliche Überprüfung der vorfallberichte Ihrer Organisation durch, die sich auf lync Server beziehen.</span><span class="sxs-lookup"><span data-stu-id="f7138-117">Perform a weekly audit of your organization’s incident reports that relate to Lync Server.</span></span> <span data-ttu-id="f7138-118">Diese Überprüfung sollte Folgendes umfassen:</span><span class="sxs-lookup"><span data-stu-id="f7138-118">This audit should include the following:</span></span>

  - <span data-ttu-id="f7138-119">Die am häufigsten generierten, behobenen und ausstehenden Vorfälle.</span><span class="sxs-lookup"><span data-stu-id="f7138-119">The top generated, resolved, and pending incidents.</span></span>

  - <span data-ttu-id="f7138-120">Lösungen für ungelöste Vorfälle.</span><span class="sxs-lookup"><span data-stu-id="f7138-120">Solutions for unresolved incidents.</span></span>

  - <span data-ttu-id="f7138-121">Aktualisieren von Berichten, um neue Trouble-Tickets einzubeziehen.</span><span class="sxs-lookup"><span data-stu-id="f7138-121">Updating reports to include new trouble tickets.</span></span>

  - <span data-ttu-id="f7138-122">Aktualisieren eines Dokument-Repositorys zur Fehlerbehebung und zur Obduktion über Ausfälle</span><span class="sxs-lookup"><span data-stu-id="f7138-122">Updating a document repository for troubleshooting guides and post mortems about outages.</span></span>

<span data-ttu-id="f7138-123">Da das Vorfall Überwachungssystem Ihrer Organisation eine Wahl ist, die von lync Server unabhängig ist, sind bestimmte Anweisungen oder Zeiger nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f7138-123">Since your organization’s incident tracking system is a choice independent of Lync Server, specific instructions or pointers are not available.</span></span> <span data-ttu-id="f7138-124">Konsultieren Sie die Dokumentation für das System, das Ihre Organisation ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="f7138-124">Consult the documentation for the system your organization chose.</span></span>

</div>

<div>

## <a name="check-iis-logs-and-performance"></a><span data-ttu-id="f7138-125">Überprüfen von IIS-Protokollen und-Leistung</span><span class="sxs-lookup"><span data-stu-id="f7138-125">Check IIS logs and performance</span></span>

<span data-ttu-id="f7138-126">Führen Sie eine wöchentliche Überprüfung der Internet Informationsdienste (IIS)-Protokolle und-Leistung durch.</span><span class="sxs-lookup"><span data-stu-id="f7138-126">Perform a weekly review of Internet Information Services (IIS) logs and performance.</span></span> <span data-ttu-id="f7138-127">Weitere Informationen zum Überwachen von IIS-Protokollen und-Leistung finden Sie unter [Übersicht über die Ereignisprotokollierung in Windows Server 2003 (IIS)](https://go.microsoft.com/fwlink/?linkid=36077).</span><span class="sxs-lookup"><span data-stu-id="f7138-127">For more information about how to monitor IIS logs and performance, see [Windows Server 2003 Internet Information Services (IIS) Event Logging Overview](https://go.microsoft.com/fwlink/?linkid=36077).</span></span> <span data-ttu-id="f7138-128">Die Überprüfung sollte Folgendes umfassen:</span><span class="sxs-lookup"><span data-stu-id="f7138-128">The review should include the following:</span></span>

  - <span data-ttu-id="f7138-129">Webdienst-Cache-Leistungsindikatoren zum Überwachen des WWW-Dienst Caches.</span><span class="sxs-lookup"><span data-stu-id="f7138-129">Web Service Cache counters to monitor the WWW service cache.</span></span>

  - <span data-ttu-id="f7138-130">ASP-Leistungsindikatoren (Active Server Pages) zum Überwachen von Anwendungen, die als ASP ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f7138-130">Active Server Pages (ASPs) counters to monitor applications that run as ASPs.</span></span>

</div>

<div>

## <a name="generate-database-reports"></a><span data-ttu-id="f7138-131">Generieren von Datenbankberichten</span><span class="sxs-lookup"><span data-stu-id="f7138-131">Generate database reports</span></span>

<span data-ttu-id="f7138-132">**So generieren Sie Berichte für die SQL-Datenbank**</span><span class="sxs-lookup"><span data-stu-id="f7138-132">**To generate reports on the SQL Database**</span></span>

1.  <span data-ttu-id="f7138-133">Öffnen Sie lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f7138-133">Open Lync Server 2013.</span></span>

2.  <span data-ttu-id="f7138-134">Erweitern Sie in der Konsolenstruktur den Knoten Gesamtstruktur, erweitern Sie **Enterprise-Pools**, und klicken Sie dann auf den Pool, für den Sie einen Datenbankbericht generieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f7138-134">In the console tree, expand the forest node, expand **Enterprise pools**, and then click the pool for which you want to generate a database report.</span></span>

3.  <span data-ttu-id="f7138-135">Klicken Sie im Detailbereich auf die Registerkarte **Datenbank** .</span><span class="sxs-lookup"><span data-stu-id="f7138-135">In the details pane, click the **Database** tab.</span></span>

4.  <span data-ttu-id="f7138-136">Führen Sie auf der Registerkarte **Datenbank** die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="f7138-136">On the **Database** tab, do the following:</span></span>
    
    1.  <span data-ttu-id="f7138-137">Wenn Sie den Namen der Datenbank anzeigen möchten, erweitern Sie **Allgemeine Einstellungen**, und zeigen Sie den Datenbanknamen an.</span><span class="sxs-lookup"><span data-stu-id="f7138-137">To view the name of the database, expand **General Settings**, and view the database name.</span></span>
    
    2.  <span data-ttu-id="f7138-138">Wenn Sie die aktuellen Benutzer Zusammenfassungs Statistiken für den Pool abrufen möchten, erweitern Sie **Benutzer Zusammenfassungsberichte**, klicken Sie auf **Gehe** zu, und zeigen Sie die Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="f7138-138">To retrieve current user summary statistics for the pool, expand **User Summary Reports**, click **Go**, and view the results.</span></span>
    
    3.  <span data-ttu-id="f7138-139">Wenn Sie aktuelle Daten pro Benutzer für einen einzelnen Benutzer des Pools abrufen möchten, erweitern Sie **Benutzer Berichte**, geben Sie den SIP-URI des Benutzers ein, klicken Sie auf **Gehe** zu, und zeigen Sie die Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="f7138-139">To retrieve current per-user data for a single user of the pool, expand **Per-User Reports**, type the user’s SIP URI, click **Go**, and view the results.</span></span>

<span data-ttu-id="f7138-140">Wenn Sie aktuelle Konferenz Zusammenfassungs Statistiken für den Pool abrufen möchten, erweitern Sie **Konferenz Zusammenfassungsberichte**, klicken Sie auf **Gehe** zu, und zeigen Sie die Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="f7138-140">To retrieve current conference summary statistics for the pool, expand **Conference Summary Reports**, click **Go**, and view the results.</span></span>

</div>

<div>

## <a name="check-for-security-and-lync-server-updates"></a><span data-ttu-id="f7138-141">Überprüfen auf Sicherheits-und lync Server-Updates</span><span class="sxs-lookup"><span data-stu-id="f7138-141">Check for security and Lync Server updates</span></span>

<span data-ttu-id="f7138-142">Identifizieren Sie alle neuen Service Packs, Hotfixes oder Updates.</span><span class="sxs-lookup"><span data-stu-id="f7138-142">Identify any new service packs, hotfixes, or updates.</span></span> <span data-ttu-id="f7138-143">Testen Sie diese gegebenenfalls in einem Testlabor, und verwenden Sie die Änderungskontrollverfahren, um die Bereitstellung auf den Produktionsservern zu arrangieren.</span><span class="sxs-lookup"><span data-stu-id="f7138-143">If appropriate, test these in a test lab, and use the change control procedures to arrange for deployment to the production servers.</span></span> <span data-ttu-id="f7138-144">Außerdem sind Updates für lync Server-Komponenten jetzt als Teil von Windows Update verfügbar.</span><span class="sxs-lookup"><span data-stu-id="f7138-144">Also, Lync Server component updates are now available as part of Windows update.</span></span> <span data-ttu-id="f7138-145">Alle lync Server-Komponenten Updates müssen gleichzeitig auf allen Servern mit lync Server aktualisiert werden, für die die Updates gelten.</span><span class="sxs-lookup"><span data-stu-id="f7138-145">All Lync Server component updates must be updated at the same time on all of the servers that are running Lync Server for which the updates are applicable.</span></span>

</div>

<div>

## <a name="run-the-lync-server-2013-best-practice-analyzer"></a><span data-ttu-id="f7138-146">Ausführen des lync Server 2013 Best Practice Analyzer</span><span class="sxs-lookup"><span data-stu-id="f7138-146">Run the Lync Server 2013 Best Practice Analyzer</span></span>

<span data-ttu-id="f7138-147">Das lync Server 2013 Best Practices Analyzer-Tool ist ein Diagnosetool, das Konfigurationsinformationen sammelt und bestimmt, ob die Konfiguration gemäß den bewährten Methoden von Microsoft festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="f7138-147">The Lync Server 2013 Best Practices Analyzer Tool is a diagnostic tool that collects configuration information and determines whether the configuration is set according to Microsoft best practices.</span></span> <span data-ttu-id="f7138-148">Die Dokumentation für dieses Tool finden Sie unter [lync Server 2013 Best Practices Analyzer](lync-server-2013-lync-server-best-practices-analyzer.md).</span><span class="sxs-lookup"><span data-stu-id="f7138-148">Documentation for this tool is at [Lync Server 2013 Best Practices Analyzer](lync-server-2013-lync-server-best-practices-analyzer.md).</span></span>

<span data-ttu-id="f7138-149">Das Tool vergleicht die Konfigurationsdaten Ihrer Bereitstellung mit einer Reihe vordefinierter Regeln für lync Server und meldet potenzielle Probleme.</span><span class="sxs-lookup"><span data-stu-id="f7138-149">The tool compares your deployment’s configuration data against a set of pre-defined rules for Lync Server, and reports potential issues.</span></span> <span data-ttu-id="f7138-150">Für jedes gemeldete Problem bietet das Tool die aktuelle Konfiguration in der lync Server-Umgebung und die empfohlene Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="f7138-150">For every issue reported, the tool provides the current configuration in the Lync Server environment, and the recommended configuration.</span></span>

<span data-ttu-id="f7138-151">Mit dem richtigen Netzwerkzugriff kann das Tool Ihre AD DS und Server untersuchen, auf denen lync Server 2013 ausgeführt wird, um folgende Aktionen auszuführen:</span><span class="sxs-lookup"><span data-stu-id="f7138-151">With the correct network access, the tool can examine your AD DS and servers that are running Lync Server 2013 to do the following:</span></span>

  - <span data-ttu-id="f7138-152">Proaktive Durchführung von Integritätsprüfungen und überprüfen, ob die Konfiguration gemäß den empfohlenen bewährten Methoden festzulegen ist</span><span class="sxs-lookup"><span data-stu-id="f7138-152">Proactively perform health checks, verifying that the configuration is set according to recommended best practices</span></span>

  - <span data-ttu-id="f7138-153">Erstellen einer Liste von Problemen, beispielsweise suboptimal-Konfigurationseinstellungen oder nicht unterstützte oder nicht empfohlene Optionen</span><span class="sxs-lookup"><span data-stu-id="f7138-153">Generate a list of issues, such as suboptimal configuration settings or unsupported or not recommended options</span></span>

  - <span data-ttu-id="f7138-154">Beurteilen des allgemeinen Zustands eines Systems</span><span class="sxs-lookup"><span data-stu-id="f7138-154">Judge the general health of a system</span></span>

  - <span data-ttu-id="f7138-155">Hilfe zur Problembehandlung bei bestimmten Problemen</span><span class="sxs-lookup"><span data-stu-id="f7138-155">Help troubleshoot specific issues</span></span>

  - <span data-ttu-id="f7138-156">Aufforderung zum Herunterladen von Updates, wenn diese verfügbar sind</span><span class="sxs-lookup"><span data-stu-id="f7138-156">Prompt you to download updates if they are available</span></span>

  - <span data-ttu-id="f7138-157">Bereitstellen von Online-und lokalen Dokumentation zu gemeldeten Problemen und einbeziehen von Tipps zur Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="f7138-157">Provide online and local documentation about reported issues, and include troubleshooting tips</span></span>

  - <span data-ttu-id="f7138-158">Generieren von Konfigurationsinformationen, die zur späteren Überprüfung erfasst werden können</span><span class="sxs-lookup"><span data-stu-id="f7138-158">Generate configuration information that can be captured for later review</span></span>

<span data-ttu-id="f7138-159">Stellen Sie sicher, dass die RTCBPA.msi auf allen lync Server 2013-Servern installiert ist, und erstellen Sie einen wöchentlichen Status Prüfbericht.</span><span class="sxs-lookup"><span data-stu-id="f7138-159">Ensure that the RTCBPA.msi is installed on all Lync Server 2013 servers, and generate a weekly Health Check Report.</span></span> <span data-ttu-id="f7138-160">Notieren Sie sich die Ergebnisse, und korrigieren Sie, falls erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f7138-160">Note the results and correct, if necessary.</span></span>

</div>

<div>

## <a name="review-sla-performance-figures"></a><span data-ttu-id="f7138-161">Überprüfen der SLA-Leistungskennzahlen</span><span class="sxs-lookup"><span data-stu-id="f7138-161">Review SLA performance figures</span></span>

<span data-ttu-id="f7138-162">Überprüfen Sie die wichtigsten Leistungsdaten für die vorherige Woche.</span><span class="sxs-lookup"><span data-stu-id="f7138-162">Check the key performance data for the previous week.</span></span> <span data-ttu-id="f7138-163">Überprüfen Sie die Leistung mit den Anforderungen der SLA.</span><span class="sxs-lookup"><span data-stu-id="f7138-163">Review performance against the requirements of the SLA.</span></span> <span data-ttu-id="f7138-164">Erkennen von Trends und Elementen, die ihre Ziele nicht erreicht haben</span><span class="sxs-lookup"><span data-stu-id="f7138-164">Identify trends and items that have not met their targets.</span></span>

</div>

<div>

## <a name="review-system-center-operations-manager-management-pack-and-quality-of-experience-reports"></a><span data-ttu-id="f7138-165">Überprüfen von System Center Operations Manager-Management Pack und Berichte zur Qualität der Erfahrung</span><span class="sxs-lookup"><span data-stu-id="f7138-165">Review System Center Operations Manager Management Pack and quality of experience reports</span></span>

<span data-ttu-id="f7138-166">Beziehen und überprüfen Sie das lync Server 2013-Management Pack und die Qualität der Erfahrungsberichte.</span><span class="sxs-lookup"><span data-stu-id="f7138-166">Obtain and review Lync Server 2013 Management Pack and Quality of Experience reports.</span></span>

</div>

<div>

## <a name="generating-and-viewing-database-reports-for-enterprise-pools"></a><span data-ttu-id="f7138-167">Generieren und Anzeigen von Datenbankberichten für Enterprise-Pools</span><span class="sxs-lookup"><span data-stu-id="f7138-167">Generating and viewing database reports for enterprise pools</span></span>

<span data-ttu-id="f7138-168">**So generieren Sie Pool Berichte**</span><span class="sxs-lookup"><span data-stu-id="f7138-168">**To generate pool reports**</span></span>

1.  <span data-ttu-id="f7138-169">Öffnen Sie lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f7138-169">Open Lync Server 2013.</span></span>

2.  <span data-ttu-id="f7138-170">Erweitern Sie in der Konsolenstruktur den Knoten Gesamtstruktur, erweitern Sie **Enterprise-Pools**, und klicken Sie dann auf den Pool, für den Sie einen Datenbankbericht generieren möchten.</span><span class="sxs-lookup"><span data-stu-id="f7138-170">In the console tree, expand the forest node, expand **Enterprise pools**, and then click the pool for which you want to generate a database report.</span></span>

3.  <span data-ttu-id="f7138-171">Klicken Sie im Detailbereich auf die Registerkarte **Datenbank** .</span><span class="sxs-lookup"><span data-stu-id="f7138-171">In the details pane, click the **Database** tab.</span></span>

4.  <span data-ttu-id="f7138-172">Führen Sie auf der Registerkarte **Datenbank** die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="f7138-172">On the **Database** tab, do the following:</span></span>
    
    1.  <span data-ttu-id="f7138-173">Wenn Sie den Namen der Datenbank anzeigen möchten, erweitern Sie **Allgemeine Einstellungen**, und zeigen Sie den Datenbanknamen an.</span><span class="sxs-lookup"><span data-stu-id="f7138-173">To view the name of the database, expand **General Settings**, and view the database name.</span></span>
    
    2.  <span data-ttu-id="f7138-174">Wenn Sie die aktuellen Benutzer Zusammenfassungs Statistiken für den Pool abrufen möchten, erweitern Sie **Benutzer Zusammenfassungsberichte**, klicken Sie auf **Gehe** zu, und zeigen Sie die Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="f7138-174">To retrieve current user summary statistics for the pool, expand **User Summary Reports**, click **Go**, and view the results.</span></span>
    
    3.  <span data-ttu-id="f7138-175">Wenn Sie aktuelle Daten pro Benutzer für einen einzelnen Benutzer des Pools abrufen möchten, erweitern Sie **Benutzer Berichte**, geben Sie den SIP-URI des Benutzers ein, klicken Sie auf **Gehe** zu, und zeigen Sie die Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="f7138-175">To retrieve current per-user data for a single user of the pool, expand **Per-User Reports**, type the user’s SIP URI, click **Go**, and view the results.</span></span>

<span data-ttu-id="f7138-176">Wenn Sie aktuelle Konferenz Zusammenfassungs Statistiken für den Pool abrufen möchten, erweitern Sie **Konferenz Zusammenfassungsberichte**, klicken Sie auf **Gehe** zu, und zeigen Sie die Ergebnisse an.</span><span class="sxs-lookup"><span data-stu-id="f7138-176">To retrieve current conference summary statistics for the pool, expand **Conference Summary Reports**, click **Go**, and view the results.</span></span>

<span data-ttu-id="f7138-177">Für jeden Enterprise-Pool können Administratoren die Registerkarte **Datenbank** verwenden, um den Datenbanknamen anzuzeigen und Berichte aus der Datenbank abzurufen und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="f7138-177">For each Enterprise Pool, administrators can use the **Database** tab to view the database name and retrieve and view reports from the database.</span></span>

### <a name="database-reports-and-descriptions"></a><span data-ttu-id="f7138-178">Datenbankberichte und Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="f7138-178">Database Reports and Descriptions</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f7138-179">Abschnittsüberschrift</span><span class="sxs-lookup"><span data-stu-id="f7138-179">Section</span></span></th>
<th><span data-ttu-id="f7138-180">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="f7138-180">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f7138-181">Benutzer Zusammenfassungsberichte</span><span class="sxs-lookup"><span data-stu-id="f7138-181">User Summary Reports</span></span></p></td>
<td><p><span data-ttu-id="f7138-182">Dbanalyze/v/Report: diag [/SQLServer: Wert]</span><span class="sxs-lookup"><span data-stu-id="f7138-182">Dbanalyze /v /report:diag [/sqlserver:value]</span></span></p>
<p><span data-ttu-id="f7138-183">In diesem Abschnitt werden aggregierte Informationen zu Benutzern in einem Pool angezeigt, beispielsweise die Anzahl der aktivierten Benutzer, die durchschnittliche Anzahl der Kontakte pro Benutzer und die Anzahl der Benutzer für bestimmte Features.</span><span class="sxs-lookup"><span data-stu-id="f7138-183">This section displays aggregate information about users in a pool, such as the number of enabled users, the average number of contacts per user, and the number of users for specific features.</span></span></p>
<p><span data-ttu-id="f7138-184">Wenn Sie diese Berichte verwenden, können die folgenden Informationen hilfreich sein:</span><span class="sxs-lookup"><span data-stu-id="f7138-184">When using these reports, the following information may be helpful:</span></span></p>
<ul>
<li><p><span data-ttu-id="f7138-185">Ein aktivierter Benutzer ist ein Benutzer, der mit dem Snap-in Active Directory-Benutzer und-Computer für lync Server 2013 aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="f7138-185">An enabled user is a user who is enabled for Lync Server 2013 by using the Active Directory Users and Computers Snap-in.</span></span></p></li>
<li><p><span data-ttu-id="f7138-186">Ein aktiver Benutzer ist ein Benutzer, der sich angemeldet oder registriert hat.</span><span class="sxs-lookup"><span data-stu-id="f7138-186">An active user is a user who has logged on or registered.</span></span></p></li>
<li><p><span data-ttu-id="f7138-187">Die Zusammenfassungsberichte bieten auch eine Reihe von statistischen Informationen zu Kontakten.</span><span class="sxs-lookup"><span data-stu-id="f7138-187">The summary reports also offer a set of statistical information about contacts.</span></span> <span data-ttu-id="f7138-188">Diese Statistiken gelten nur für die Bevölkerung von Benutzern, die sich mindestens einmal angemeldet haben und die mindestens einen Kontakt haben.</span><span class="sxs-lookup"><span data-stu-id="f7138-188">These statistics are only valid for the population of users who have logged on at least one time, and who have at least one contact.</span></span> <span data-ttu-id="f7138-189">Daher wird normalerweise keine minimale Anzahl von Kontakten von 0 angezeigt.</span><span class="sxs-lookup"><span data-stu-id="f7138-189">Consequently, you'll typically not see a minimum number of contacts of 0.</span></span> <span data-ttu-id="f7138-190">Wenn ein Benutzer über keine Kontakte verfügt (aber aktiv ist, in dem sich der Benutzer registriert hat), wird möglicherweise &lt; &gt; für einige Statistikfelder leer angezeigt:</span><span class="sxs-lookup"><span data-stu-id="f7138-190">Because of this behavior, if a user has no contacts (but is active, in that the user has registered), you may see: &lt;empty&gt; for some statistics fields.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f7138-191">Per-User Berichte</span><span class="sxs-lookup"><span data-stu-id="f7138-191">Per-User Reports</span></span></p></td>
<td><p><span data-ttu-id="f7138-192">Dbanalyze/v/Report: Datenträger [/SQLServer: Wert]</span><span class="sxs-lookup"><span data-stu-id="f7138-192">Dbanalyze /v /report:disk [/sqlserver:value]</span></span></p>
<p><span data-ttu-id="f7138-193">Im Gegensatz zu den Zusammenfassungsberichten, die über eine Benutzerpopulation berechnet werden, handelt es sich um Berichte über einen bestimmten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="f7138-193">Unlike the summary reports, which are calculated over a user population, these are reports about a specific user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f7138-194">Konferenz Zusammenfassungsberichte</span><span class="sxs-lookup"><span data-stu-id="f7138-194">Conference Summary Reports</span></span></p></td>
<td><p><span data-ttu-id="f7138-195">Dbanalyze/v/Report: conf [/SQLServer: Wert]</span><span class="sxs-lookup"><span data-stu-id="f7138-195">Dbanalyze /v /report:conf [/sqlserver:value]</span></span></p>
<p><span data-ttu-id="f7138-196">In diesem Abschnitt werden aggregierte Informationen zu Konferenz Zusammenfassungs Statistiken für den Pool angezeigt, beispielsweise die Anzahl aktiver Konferenzen und die Gesamtzahl der Teilnehmer.</span><span class="sxs-lookup"><span data-stu-id="f7138-196">This section displays aggregate information about conference summary statistics for the pool, such as the number of active conferences and total number of participants.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="running-bandwidth-utilization-analyzer"></a><span data-ttu-id="f7138-197">Ausführen von Bandbreiten Auslastungsanalyse</span><span class="sxs-lookup"><span data-stu-id="f7138-197">Running Bandwidth Utilization Analyzer</span></span>

<span data-ttu-id="f7138-198">Bandwidth Utilization Analyzer ist ein Tool, das Berichte über verschiedene Ansichten des Bandbreitenverbrauchs durch die UC-Endpunkte über WAN-Verbindungen im Unternehmensnetzwerk erstellt.</span><span class="sxs-lookup"><span data-stu-id="f7138-198">Bandwidth Utilization Analyzer is a tool that creates reports about various views of bandwidth consumption by the UC endpoints across WAN links in the enterprise network.</span></span> <span data-ttu-id="f7138-199">Diese Berichte können verwendet werden, um das aktuelle Muster der Bandbreitennutzung zu verstehen und bei der Planung der Bandbreitenkapazität zu helfen.</span><span class="sxs-lookup"><span data-stu-id="f7138-199">These reports can be used to understand the current bandwidth consumption pattern and to help with bandwidth capacity planning.</span></span> <span data-ttu-id="f7138-200">Das Tool durchläuft außerdem die Bandbreitenkapazität, die verschiedenen Verbindungen zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="f7138-200">It also iterates on the bandwidth capacity that is assigned to various links.</span></span>

<span data-ttu-id="f7138-201">Das Tool bietet folgende Funktionen:</span><span class="sxs-lookup"><span data-stu-id="f7138-201">This tool does the following:</span></span>

  - <span data-ttu-id="f7138-202">Generiert bestimmte Berichte für die audionutzung über das Netzwerk</span><span class="sxs-lookup"><span data-stu-id="f7138-202">Generates specific reports for audio usage over the network</span></span>

  - <span data-ttu-id="f7138-203">Hilfe bei einer effektiveren Kapazitätsplanung und Iteration der Bandbreitenkapazität, die verschiedenen Verbindungen zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="f7138-203">Helps with more effective capacity planning and iteration on the bandwidth capacity that is assigned to various links</span></span>

<span data-ttu-id="f7138-204">Der Bandbreiten Auslastungs Analysator kann grafische Plots von Bandbreiten Kapazitäts-und Nutzungsberichten generieren.</span><span class="sxs-lookup"><span data-stu-id="f7138-204">Bandwidth Utilization Analyzer can generate graphical plots of bandwidth capacity and usage reports.</span></span> <span data-ttu-id="f7138-205">Sie sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f7138-205">They are as follows:</span></span>

  - <span data-ttu-id="f7138-206">Alle WAN-Verbindungen im Unternehmensnetzwerk</span><span class="sxs-lookup"><span data-stu-id="f7138-206">All the WAN links in the enterprise network</span></span>

  - <span data-ttu-id="f7138-207">Gefiltert nach ausgewählten WAN-Links, die ausgewählt wurden</span><span class="sxs-lookup"><span data-stu-id="f7138-207">Filtered by selected WAN links that were chosen</span></span>

  - <span data-ttu-id="f7138-208">Gefiltert nach WAN-Verbindungen, die die Verbindungskapazität überschritten haben</span><span class="sxs-lookup"><span data-stu-id="f7138-208">Filtered by WAN links that have exceeded link capacity</span></span>

  - <span data-ttu-id="f7138-209">Gefiltert nach WAN-Links, die die bereitgestellte Bandbreite unter Verwenden</span><span class="sxs-lookup"><span data-stu-id="f7138-209">Filtered by WAN links that were under-using the provisioned bandwidth</span></span>

  - <span data-ttu-id="f7138-210">Filtern nach WAN-Links, die kritische Ebenen erreichen (eine Bandbreitennutzung, die größer als 90 Prozent der Bandbreitenkapazität der WAN-Verbindung ist)</span><span class="sxs-lookup"><span data-stu-id="f7138-210">Filter by WAN links that were reaching critical levels (a bandwidth usage that is greater than 90 percent of bandwidth capacity of the WAN link)</span></span>

  - <span data-ttu-id="f7138-211">Nach WAN-Verknüpfungstyp gefiltert – Netzwerk-Standort-Links, interregionale Links und Links innerhalb einer Website</span><span class="sxs-lookup"><span data-stu-id="f7138-211">Filtered by WAN link type—network-site links, interregional links, and links inside a site</span></span>

  - <span data-ttu-id="f7138-212">Gefiltert nach Netzwerkregion</span><span class="sxs-lookup"><span data-stu-id="f7138-212">Filtered by network region</span></span>

<span data-ttu-id="f7138-213">Die Dokumentation zu diesem Tool finden Sie in der [Dokumentation zur lync Server 2013 Resource Kit-Tools](https://go.microsoft.com/fwlink/?linkid=623245).</span><span class="sxs-lookup"><span data-stu-id="f7138-213">Documentation for this tool is available at [Lync Server 2013 Resource Kit Tools Documentation](https://go.microsoft.com/fwlink/?linkid=623245).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f7138-214">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f7138-214">See Also</span></span>


[<span data-ttu-id="f7138-215">Checkliste für wöchentliche Aufgaben</span><span class="sxs-lookup"><span data-stu-id="f7138-215">Weekly task checklist</span></span>](lync-server-2013-operations-checklists.md)  
  

<span data-ttu-id="f7138-216"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f7138-216"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

