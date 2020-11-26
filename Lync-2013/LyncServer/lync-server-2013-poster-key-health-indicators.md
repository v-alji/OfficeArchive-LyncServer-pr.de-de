---
title: 'Lync Server 2013: Poster: wichtige Integritätsindikatoren'
description: 'Lync Server 2013: Poster: wichtige Integritätsindikatoren.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Poster: Key Health Indicators'
ms:assetid: 8367dccf-adaa-4a0b-a4ed-bc9570cc5e24
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn593599(v=OCS.15)
ms:contentKeyID: 61084873
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9962d1764d5d2c664bb8415261344d9b48c81149
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424243"
---
# <a name="key-health-indicators-in-lync-server-2013"></a><span data-ttu-id="3b2a0-103">Wichtige Integritätsindikatoren in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3b2a0-103">Key Health Indicators in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3b2a0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3b2a0-104">

<span> </span></span></span>

<span data-ttu-id="3b2a0-105">_**Letztes Änderungsdatum des Themas:** 2014-02-10_</span><span class="sxs-lookup"><span data-stu-id="3b2a0-105">_**Topic Last Modified:** 2014-02-10_</span></span>

<span data-ttu-id="3b2a0-106">Dieser Artikel ist ein Begleiter zu den [wichtigsten Integritätsindikatoren: die Grundlage für die Verwaltung eines fehlerfreien lync Servers](https://go.microsoft.com/fwlink/?linkid=391838) -Plakats, das Sie aus dem Download Center herunterladen können.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-106">This article is a companion to the [Key Health Indicators: The Foundation for Maintaining Healthy Lync Servers](https://go.microsoft.com/fwlink/?linkid=391838) poster, which you can download from the Download Center.</span></span>

<span data-ttu-id="3b2a0-107">![Poster, das die Problembehandlung mithilfe von KHI-Daten beschreibt](images/Dn594589.b6fe82bd-d70f-4c1f-a812-b615ac5fa7d7(OCS.15).jpg "Poster, das die Problembehandlung mithilfe von KHI-Daten beschreibt")</span><span class="sxs-lookup"><span data-stu-id="3b2a0-107">![Poster describing troubleshooting using KHI data](images/Dn594589.b6fe82bd-d70f-4c1f-a812-b615ac5fa7d7(OCS.15).jpg "Poster describing troubleshooting using KHI data")</span></span>

<span data-ttu-id="3b2a0-108">Sie können dieses Poster verwenden, um Informationen zu wichtigen Integritätsindikatoren (KHIs), Leistungsindikatoren mit Schwellenwerten für die Anzeige von Problemen mit der Benutzeroberfläche zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-108">You can use this poster to learn about Key Health Indicators (KHIs), performance counters with thresholds aimed at revealing user experience issues.</span></span> <span data-ttu-id="3b2a0-109">Das Sammeln von KHI-Daten ist in der Regel der erste Schritt zur Implementierung der Methode für die Anrufqualität (Call Quality Method, CQM), die auf die Gewährleistung einer Audioqualität für lync-Benutzer ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-109">Gathering KHI data is usually the first step to implementing the Call Quality Methodology (CQM), which is focused on ensuring a quality audio experience for Lync users.</span></span>

<span data-ttu-id="3b2a0-110">Wenn Sie Fragen zur Verwendung von CQM haben, können Sie Ihre Fragen an cqmfeedback@Microsoft.com senden.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-110">If you have questions about how to use CQM, you can submit your questions to cqmfeedback@microsoft.com.</span></span>

<span data-ttu-id="3b2a0-111">Das Poster erläutert die folgenden Bereiche:</span><span class="sxs-lookup"><span data-stu-id="3b2a0-111">The poster explains the following areas:</span></span>

  - <span data-ttu-id="3b2a0-112">Was sind die wichtigsten Statusindikatoren?</span><span class="sxs-lookup"><span data-stu-id="3b2a0-112">What are Key Health Indicators?</span></span>

  - <span data-ttu-id="3b2a0-113">So erfassen Sie KHI-Daten</span><span class="sxs-lookup"><span data-stu-id="3b2a0-113">To Collect KHI Data</span></span>

  - <span data-ttu-id="3b2a0-114">Korrektur Fluss für alle Server Rollen</span><span class="sxs-lookup"><span data-stu-id="3b2a0-114">Remediation Flow for all Server Roles</span></span>

  - <span data-ttu-id="3b2a0-115">Glossar</span><span class="sxs-lookup"><span data-stu-id="3b2a0-115">Glossary</span></span>

  - <span data-ttu-id="3b2a0-116">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="3b2a0-116">Front-end Servers</span></span>

  - <span data-ttu-id="3b2a0-117">Back-End-SQL-Server</span><span class="sxs-lookup"><span data-stu-id="3b2a0-117">Backend SQL Servers</span></span>

  - <span data-ttu-id="3b2a0-118">Vermittlungsserver</span><span class="sxs-lookup"><span data-stu-id="3b2a0-118">Mediation Servers</span></span>

  - <span data-ttu-id="3b2a0-119">Edgeservers</span><span class="sxs-lookup"><span data-stu-id="3b2a0-119">Edge Servers</span></span>

<span id="WhatIs"></span>

<div>

## <a name="what-are-key-health-indicators"></a><span data-ttu-id="3b2a0-120">Was sind die wichtigsten Statusindikatoren?</span><span class="sxs-lookup"><span data-stu-id="3b2a0-120">What are Key Health Indicators?</span></span>

<span data-ttu-id="3b2a0-121">Zu den wichtigsten Integritätsindikatoren zählen Leistungsindikatoren mit Schwellenwerten, die darauf abzielen, Probleme mit der Benutzeroberfläche zu erkennen.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-121">Key Health Indicators are performance counters with thresholds aimed at revealing user experience issues.</span></span> <span data-ttu-id="3b2a0-122">Das Sammeln von KHI-Daten ist in der Regel der erste Schritt zur Implementierung der Methode für die Anrufqualität (Call Quality Method, CQM), die auf die Gewährleistung einer Audioqualität für lync-Benutzer ausgerichtet ist.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-122">Gathering KHI data is usually the first step to implementing the Call Quality Methodology (CQM), which is focused on ensuring a quality audio experience for Lync users.</span></span>

<span data-ttu-id="3b2a0-123">KHIs werden zusätzlich zu den standardmäßigen lync-Überwachungslösungen (z. b. System Center Operations Manager, synthetische Transaktionen, Monitoring Server) und nicht anstelle dieser Lösungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-123">KHIs are used in addition to standard Lync Monitoring Solutions (e.g. System Center Operations Manager, Synthetic Transactions, Monitoring Server) and not instead of those solutions.</span></span>

<span data-ttu-id="3b2a0-124">Sammeln Sie die KHI-Leistungsindikatoren, und füllen Sie die KHI-Kalkulationstabelle mit dem Netzwerk Leit Faden aus, um eine Scorecard zu erstellen, mit der Sie den Serverzustand einer lync-Bereitstellung ermitteln können.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-124">Collect the KHI performance counters and populate the KHI spreadsheet accompanying the Networking Guide to produce a scorecard that will help you determine the server health of a Lync deployment.</span></span> <span data-ttu-id="3b2a0-125">Sobald die Datei ausgefüllt ist, führt Sie Sie bei der Reparatur der Umgebung und gibt weiteren Einblick in andere Stakeholder.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-125">Once populated, it guides you in repairing the environment and gives additional insight to other stakeholders.</span></span> <span data-ttu-id="3b2a0-126">Bewerten Sie KHIs monatlich, und fügen Sie Sie in die laufenden operativen Prozesse der Bereitstellung ein.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-126">Evaluate KHIs on a monthly basis and incorporate them into any deployment’s ongoing operational processes.</span></span>

<span data-ttu-id="3b2a0-127">Laden Sie den [lync Server-Netzwerk Leit Faden](https://go.microsoft.com/fwlink/p/?linkid=390677) herunter, um die vollständige Liste der KHIs anzuzeigen und die zugehörigen Kalkulationstabellen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-127">Download the [Lync Server Networking Guide](https://go.microsoft.com/fwlink/p/?linkid=390677) to see the full list of KHIs and to get the related spreadsheets.</span></span>

</div>

<span id="ToCollect"></span>

<div>

## <a name="to-collect-khi-data"></a><span data-ttu-id="3b2a0-128">So erfassen Sie KHI-Daten</span><span class="sxs-lookup"><span data-stu-id="3b2a0-128">To Collect KHI Data</span></span>

1.  <span data-ttu-id="3b2a0-129">Führen Sie das KHI-Skript aus, das im lync Server-Netzwerk Leit Faden auf jedem lync-Server enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-129">Run the KHI script included with the Lync Server Networking Guide on each Lync Server.</span></span> <span data-ttu-id="3b2a0-130">Dadurch wird ein Datenauflister innerhalb des Systemmonitors erstellt und der Name khi.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-130">This will create a Data Collector inside of Performance Monitor and name it KHI.</span></span> <span data-ttu-id="3b2a0-131">Standardmäßig werden Daten alle 15 Sekunden abgefragt.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-131">By default, data will be polled every 15 seconds.</span></span>

2.  <span data-ttu-id="3b2a0-132">Wechseln Sie vor dem Beginn des Geschäftstages des Unternehmens zu jedem lync-Server, und starten Sie den KHI-Datensammler.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-132">Before the start of your company's business day, go to each Lync Server and start the KHI Data Collector.</span></span>

3.  <span data-ttu-id="3b2a0-133">Beenden Sie am Ende dieses Tages den KHI-Datenauflister, und kopieren Sie die Daten an eine zentrale Position.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-133">At the end of that day, stop the KHI Data Collector and copy the data to a central location.</span></span>

4.  <span data-ttu-id="3b2a0-134">Nachdem Sie die mit dem lync Server Networking Guide-Download enthaltene KHI-Kalkulationstabelle mit dem System Monitor gefüllt haben, vergleichen Sie die Ergebnisse mit den empfohlenen Zielen.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-134">After using Performance Monitor to fill in the KHI spreadsheet included with the Lync Server Networking Guide download, compare the results to the recommended targets.</span></span>

</div>

<span id="Remidiation"></span>

<div>

## <a name="remediation-flow-for-all-server-roles"></a><span data-ttu-id="3b2a0-135">Korrektur Fluss für alle Server Rollen</span><span class="sxs-lookup"><span data-stu-id="3b2a0-135">Remediation Flow for all Server Roles</span></span>

<span data-ttu-id="3b2a0-136">Stellen Sie für jeden Server in ihrer lync-Implementierung zunächst sicher, dass die komponentenintegrität und Systemleistung des Servers auf oder über dem gewünschten Wert liegen.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-136">For each server in your Lync implementation, begin by verifying that the server’s component health and system performance is at or above the desired level.</span></span> <span data-ttu-id="3b2a0-137">Erst danach sollten Sie sich die Indikatoren in Bezug auf die Rolle des Servers in der gesamten lync-Implementierung anschauen.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-137">Only after that should you look at the indicators relating to the server’s role in the overall Lync implementation.</span></span>

<span data-ttu-id="3b2a0-138">Beginnen Sie mit dem Sammeln von KHI-Leistungsdaten für alle Server.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-138">Begin by collecting KHI Performance Data for all servers.</span></span> <span data-ttu-id="3b2a0-139">Für jede Systemrolle (Details, die weiter unten in diesem Dokument erläutert werden) ermitteln Sie, ob die grundlegenden Systemkomponenten die empfohlenen Ziele erfüllen.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-139">For each of the system roles (details discussed later in this document) determine whether the basic system components meet the recommended targets.</span></span> <span data-ttu-id="3b2a0-140">Wenn dies nicht der Fall ist, beheben Sie die Systemleistung, und sammeln Sie dann KHI-Daten erneut, und stellen Sie die Systemintegrität sicher, bevor Sie sich die Metriken ansehen, die für die Rolle des Servers in der lync-Implementierung spezifisch sind.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-140">If they do not, remediate the system performance then re-collect KHI data and ensure system health before looking at the metrics specific to the server’s role in the Lync implementation.</span></span> <span data-ttu-id="3b2a0-141">Der Komponentenstatus für alle Rollen ist wie folgt definiert:</span><span class="sxs-lookup"><span data-stu-id="3b2a0-141">Component health for all roles is defined as:</span></span>

  - <span data-ttu-id="3b2a0-142">CPU-Auslastung \< 80%</span><span class="sxs-lookup"><span data-stu-id="3b2a0-142">CPU Utilization \< 80%</span></span>

  - <span data-ttu-id="3b2a0-143">AVG. Disk schreibt \< 10 ms</span><span class="sxs-lookup"><span data-stu-id="3b2a0-143">Avg. Disk Write \< 10 ms</span></span>

  - <span data-ttu-id="3b2a0-144">AVG. Disk Lesen Sie \< 10 ms</span><span class="sxs-lookup"><span data-stu-id="3b2a0-144">Avg. Disk Read \< 10 ms</span></span>

  - <span data-ttu-id="3b2a0-145">Verfügbarer Arbeitsspeicher \> 20% System gesamt MB</span><span class="sxs-lookup"><span data-stu-id="3b2a0-145">Available memory \>20% System Total MB</span></span>

  - <span data-ttu-id="3b2a0-146">Netzwerk-Warteschlangenlänge \< 2</span><span class="sxs-lookup"><span data-stu-id="3b2a0-146">Network Queue Length \< 2</span></span>

  - <span data-ttu-id="3b2a0-147">Verworfene Pakete (in/out) = 0</span><span class="sxs-lookup"><span data-stu-id="3b2a0-147">Discarded Packets (in / out) = 0</span></span>

</div>

<span id="Glossary"></span>

<div>

## <a name="glossary"></a><span data-ttu-id="3b2a0-148">Glossar</span><span class="sxs-lookup"><span data-stu-id="3b2a0-148">Glossary</span></span>

<span data-ttu-id="3b2a0-149">Die folgenden Begriffe und Akronyme werden in diesem Poster verwendet:</span><span class="sxs-lookup"><span data-stu-id="3b2a0-149">The following terms and acronyms are used in this poster:</span></span>

<span data-ttu-id="3b2a0-150">Als MCU = Application Sharing Multi-Punkt-Steuereinheit</span><span class="sxs-lookup"><span data-stu-id="3b2a0-150">AS MCU = Application Sharing Multi-point Control Unit</span></span>

<span data-ttu-id="3b2a0-151">AV MCU = Audio/Video-MCU</span><span class="sxs-lookup"><span data-stu-id="3b2a0-151">AV MCU = Audio/Video MCU</span></span>

<span data-ttu-id="3b2a0-152">IM MCU = Instant Messaging-MCU</span><span class="sxs-lookup"><span data-stu-id="3b2a0-152">IM MCU = Instant Messaging MCU</span></span>

<span data-ttu-id="3b2a0-153">UCWA = Unified Communications Web-API</span><span class="sxs-lookup"><span data-stu-id="3b2a0-153">UCWA = Unified Communications Web API</span></span>

<span data-ttu-id="3b2a0-154">AV Edge = durchlaufen von Audio/Video über Edge</span><span class="sxs-lookup"><span data-stu-id="3b2a0-154">AV Edge = Traversal of audio/video via edge</span></span>

<span data-ttu-id="3b2a0-155">AV auth = Audio/Video-Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="3b2a0-155">AV Auth = Audio/Video Authentication</span></span>

<span data-ttu-id="3b2a0-156">SIP Stack = enthält die zentrale SIP-Implementierung von lync</span><span class="sxs-lookup"><span data-stu-id="3b2a0-156">SIP Stack = Contains Lync’s core SIP implementation</span></span>

<span data-ttu-id="3b2a0-157">Data Proxy = wird für Edge-Konferenzen verwendet</span><span class="sxs-lookup"><span data-stu-id="3b2a0-157">Data Proxy = Used for edge conferencing</span></span>

<span data-ttu-id="3b2a0-158">LySS = lync-Speicherdienst</span><span class="sxs-lookup"><span data-stu-id="3b2a0-158">LySS = Lync Storage Service</span></span>

</div>

<span id="Front"></span>

<div>

## <a name="front-end-servers"></a><span data-ttu-id="3b2a0-159">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="3b2a0-159">Front-end Servers</span></span>

<span data-ttu-id="3b2a0-160">Die folgenden empfohlenen KHI-Ziele sind für Front-End-Server zusätzlich zu den grundlegenden Komponentenstatus spezifisch:</span><span class="sxs-lookup"><span data-stu-id="3b2a0-160">The following recommended KHI targets are specific to front-end servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b2a0-161">Funktionsbereich</span><span class="sxs-lookup"><span data-stu-id="3b2a0-161">Functional area</span></span></th>
<th><span data-ttu-id="3b2a0-162">Ziel Metriken</span><span class="sxs-lookup"><span data-stu-id="3b2a0-162">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b2a0-163">AS/AV/im-MCU</span><span class="sxs-lookup"><span data-stu-id="3b2a0-163">AS/AV/IM MCU</span></span></p></td>
<td><p><span data-ttu-id="3b2a0-164">MCU-Integritätsstatus &lt; 2</span><span class="sxs-lookup"><span data-stu-id="3b2a0-164">MCU Health State &lt;2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2a0-165">Web-Komponenten</span><span class="sxs-lookup"><span data-stu-id="3b2a0-165">Web Components</span></span></p></td>
<td><p><span data-ttu-id="3b2a0-166">Erweiterung der Verteilerliste anzeigen Timeouts &lt; 0</span><span class="sxs-lookup"><span data-stu-id="3b2a0-166">Distribution List expansion AD timeouts &lt;0</span></span></p>
<p><span data-ttu-id="3b2a0-167">ABWQ-Fehler = 0</span><span class="sxs-lookup"><span data-stu-id="3b2a0-167">ABWQ failures = 0</span></span></p>
<p><span data-ttu-id="3b2a0-168">LIS-Fehler = 0</span><span class="sxs-lookup"><span data-stu-id="3b2a0-168">LIS failures = 0</span></span></p>
<p><span data-ttu-id="3b2a0-169">Authentifizierungsfehler &lt; 1/Sek.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-169">Authentication Errors &lt; 1/sec</span></span></p>
<p><span data-ttu-id="3b2a0-170">ASP.net V4-Anforderungen abgelehnt = 0</span><span class="sxs-lookup"><span data-stu-id="3b2a0-170">ASP.NET v4 Requests Rejected = 0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b2a0-171">SIP-Stack</span><span class="sxs-lookup"><span data-stu-id="3b2a0-171">SIP Stack</span></span></p></td>
<td><p><span data-ttu-id="3b2a0-172">Verarbeitung von eingehenden Nachrichten &lt; 1 Sek.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-172">Avg. Incoming Message Processing &lt; 1 sec</span></span></p>
<p><span data-ttu-id="3b2a0-173">Eingehende Antworten sanken &lt; 1/sec eingehende Anforderungen sanken &lt; 1/Sek.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-173">Incoming Responses Dropped &lt; 1/sec Incoming Requests Dropped &lt; 1/sec</span></span></p>
<p><span data-ttu-id="3b2a0-174">Warteschlangen Wartezeit &lt; 100 MS</span><span class="sxs-lookup"><span data-stu-id="3b2a0-174">Queue Latency &lt; 100 ms</span></span></p>
<p><span data-ttu-id="3b2a0-175">Latenz Wartezeit &lt; 100 MS</span><span class="sxs-lookup"><span data-stu-id="3b2a0-175">Sproc Latency &lt; 100 ms</span></span></p>
<p><span data-ttu-id="3b2a0-176">Gedrosselte Anforderungen = 0</span><span class="sxs-lookup"><span data-stu-id="3b2a0-176">Throttled Requests = 0</span></span></p>
<p><span data-ttu-id="3b2a0-177">Authentifizierungsfehler &lt; 1/Sek.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-177">Authentication Errors &lt; 1/sec</span></span></p>
<p><span data-ttu-id="3b2a0-178">Timeout für eingehende Nachrichten &lt; 2</span><span class="sxs-lookup"><span data-stu-id="3b2a0-178">Incoming Messages Timed Out &lt; 2</span></span></p>
<p><span data-ttu-id="3b2a0-179">Eingehende Nachrichten: &lt; 1 Sek.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-179">Avg. Incoming Message Hold &lt; 1 sec</span></span></p>
<p><span data-ttu-id="3b2a0-180">Durchflussgesteuerte Verbindungen &lt; 2</span><span class="sxs-lookup"><span data-stu-id="3b2a0-180">Flow Controlled Connections &lt; 2</span></span></p>
<p><span data-ttu-id="3b2a0-181">Verzögerung von AVG. Out-Warteschlange &lt; 2 Sek.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-181">Avg. Out Queue Delay &lt; 2 sec</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2a0-182">LySS</span><span class="sxs-lookup"><span data-stu-id="3b2a0-182">LySS</span></span></p></td>
<td><p><span data-ttu-id="3b2a0-183">% des vom Speicherdienst DB 80 verwendeten Speicherplatzes &lt;</span><span class="sxs-lookup"><span data-stu-id="3b2a0-183">% of space used by Storage Service DB &lt; 80</span></span></p>
<p><span data-ttu-id="3b2a0-184"># Replikat Replikationsfehler = 0</span><span class="sxs-lookup"><span data-stu-id="3b2a0-184"># of replica replication failures = 0</span></span></p>
<p><span data-ttu-id="3b2a0-185"># von Datenverlust Ereignissen = 0</span><span class="sxs-lookup"><span data-stu-id="3b2a0-185"># of data loss events = 0</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b2a0-186">SQL</span><span class="sxs-lookup"><span data-stu-id="3b2a0-186">SQL</span></span></p></td>
<td><p><span data-ttu-id="3b2a0-187">Lebenserwartung der Seite &gt; 300 Sek.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-187">Page life expectancy &gt; 300 Sec.</span></span></p>
<p><span data-ttu-id="3b2a0-188">Batch Anforderungen/Sek &lt; 2500</span><span class="sxs-lookup"><span data-stu-id="3b2a0-188">Batch requests / sec &lt; 2500</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<span id="BackEnd"></span>

<div>

## <a name="backend-sql-servers"></a><span data-ttu-id="3b2a0-189">Back-End-SQL-Server</span><span class="sxs-lookup"><span data-stu-id="3b2a0-189">Backend SQL Servers</span></span>

<span data-ttu-id="3b2a0-190">Die folgenden empfohlenen KHI-Ziele gelten zusätzlich zu den grundlegenden Komponenten Integritäts Merkmalen für SQL-Server:</span><span class="sxs-lookup"><span data-stu-id="3b2a0-190">The following recommended KHI targets are specific to SQL servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b2a0-191">Funktionsbereich</span><span class="sxs-lookup"><span data-stu-id="3b2a0-191">Functional area</span></span></th>
<th><span data-ttu-id="3b2a0-192">Ziel Metriken</span><span class="sxs-lookup"><span data-stu-id="3b2a0-192">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b2a0-193">SQL</span><span class="sxs-lookup"><span data-stu-id="3b2a0-193">SQL</span></span></p></td>
<td><p><span data-ttu-id="3b2a0-194">Lebenserwartung der Seite &gt; 300 Sek.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-194">Page life expectancy &gt; 300 Sec.</span></span></p>
<p><span data-ttu-id="3b2a0-195">Batch Anforderungen/Sek &lt; 2500</span><span class="sxs-lookup"><span data-stu-id="3b2a0-195">Batch requests / sec &lt; 2500</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<span id="Mediation"></span>

<div>

## <a name="mediation-servers"></a><span data-ttu-id="3b2a0-196">Vermittlungsserver</span><span class="sxs-lookup"><span data-stu-id="3b2a0-196">Mediation Servers</span></span>

<span data-ttu-id="3b2a0-197">Die folgenden empfohlenen KHI-Ziele gelten speziell für Vermittlungsserver sowie für die grundlegende komponentenintegrität:</span><span class="sxs-lookup"><span data-stu-id="3b2a0-197">The following recommended KHI targets are specific to mediation servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b2a0-198">Funktionsbereich</span><span class="sxs-lookup"><span data-stu-id="3b2a0-198">Functional area</span></span></th>
<th><span data-ttu-id="3b2a0-199">Ziel Metriken</span><span class="sxs-lookup"><span data-stu-id="3b2a0-199">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b2a0-200">Vermittlungs Server Dienst</span><span class="sxs-lookup"><span data-stu-id="3b2a0-200">Mediation Server Service</span></span></p></td>
<td><p><span data-ttu-id="3b2a0-201">Fehler beim Laden des Anrufs Index = 0</span><span class="sxs-lookup"><span data-stu-id="3b2a0-201">Load Call Failure Index = 0</span></span></p>
<p><span data-ttu-id="3b2a0-202">Fehlgeschlagene Anrufe wegen Proxy &lt; 10</span><span class="sxs-lookup"><span data-stu-id="3b2a0-202">Failed Calls due to Proxy &lt;10</span></span></p>
<p><span data-ttu-id="3b2a0-203">Fehlgeschlagene Anrufe wegen Gateway &lt; 10</span><span class="sxs-lookup"><span data-stu-id="3b2a0-203">Failed Calls due to Gateway &lt;10</span></span></p>
<p><span data-ttu-id="3b2a0-204">Anrufe (in oder aus) abgelehnt = 0</span><span class="sxs-lookup"><span data-stu-id="3b2a0-204">Calls (in or out) rejected = 0</span></span></p>
<p><span data-ttu-id="3b2a0-205">Medien Kandidaten fehlen = 0</span><span class="sxs-lookup"><span data-stu-id="3b2a0-205">Media Candidates missing = 0</span></span></p>
<p><span data-ttu-id="3b2a0-206">Fehler bei der Medien Verbindungsüberprüfung = 0</span><span class="sxs-lookup"><span data-stu-id="3b2a0-206">Media Connectivity Check Failures = 0</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<span id="Edge"></span>

<div>

## <a name="edge-servers"></a><span data-ttu-id="3b2a0-207">Edgeservers</span><span class="sxs-lookup"><span data-stu-id="3b2a0-207">Edge Servers</span></span>

<span data-ttu-id="3b2a0-208">Die folgenden empfohlenen KHI-Ziele gelten zusätzlich zu den grundlegenden Komponentenstatus speziell für Edge-Server:</span><span class="sxs-lookup"><span data-stu-id="3b2a0-208">The following recommended KHI targets are specific to edge servers in addition to basic component health:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b2a0-209">Funktionsbereich</span><span class="sxs-lookup"><span data-stu-id="3b2a0-209">Functional area</span></span></th>
<th><span data-ttu-id="3b2a0-210">Ziel Metriken</span><span class="sxs-lookup"><span data-stu-id="3b2a0-210">Target Metrics</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b2a0-211">AV-auth</span><span class="sxs-lookup"><span data-stu-id="3b2a0-211">AV Auth</span></span></p></td>
<td><p><span data-ttu-id="3b2a0-212">Ungültige Anforderungen &lt; 20/Sek.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-212">Bad Requests &lt; 20/sec</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2a0-213">AV-Edge</span><span class="sxs-lookup"><span data-stu-id="3b2a0-213">AV Edge</span></span></p></td>
<td><p><span data-ttu-id="3b2a0-214">Auth. Fehler &lt; 20/Sek.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-214">Auth. Failures &lt;20/sec</span></span></p>
<p><span data-ttu-id="3b2a0-215">Zuordnungsfehler &lt; 20/Sek.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-215">Allocation Failures &lt;20/sec</span></span></p>
<p><span data-ttu-id="3b2a0-216">Pakete, die &lt; 300/Sek. gelöscht wurden</span><span class="sxs-lookup"><span data-stu-id="3b2a0-216">Packets Dropped &lt;300/sec</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b2a0-217">Daten Proxy</span><span class="sxs-lookup"><span data-stu-id="3b2a0-217">Data Proxy</span></span></p></td>
<td><p><span data-ttu-id="3b2a0-218">Gedrosselte Server Verbindungen &lt; 3</span><span class="sxs-lookup"><span data-stu-id="3b2a0-218">Throttled Server connections &lt; 3</span></span></p>
<p><span data-ttu-id="3b2a0-219">System Drosselung &lt; 1</span><span class="sxs-lookup"><span data-stu-id="3b2a0-219">System is Throttling &lt;1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b2a0-220">SIP-Stack</span><span class="sxs-lookup"><span data-stu-id="3b2a0-220">SIP Stack</span></span></p></td>
<td><p><span data-ttu-id="3b2a0-221">Verbindungen über Grenze sanken &lt; 1</span><span class="sxs-lookup"><span data-stu-id="3b2a0-221">Connections over limit dropped &lt; 1</span></span></p>
<p><span data-ttu-id="3b2a0-222">Zeitüberschreitung bei Sends &lt; 10</span><span class="sxs-lookup"><span data-stu-id="3b2a0-222">Sends timed out &lt;10</span></span></p>
<p><span data-ttu-id="3b2a0-223">Durchflussgesteuerte Verbindungen &lt; 100</span><span class="sxs-lookup"><span data-stu-id="3b2a0-223">Flow Controlled Connections &lt;100</span></span></p>
<p><span data-ttu-id="3b2a0-224">Eingehende Anforderungen sanken auf &lt; 1/Sek.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-224">Incoming requests dropped &lt; 1/sec</span></span></p>
<p><span data-ttu-id="3b2a0-225">AVG. Nachrichtenverarbeitung &lt; 3 Sek.</span><span class="sxs-lookup"><span data-stu-id="3b2a0-225">Avg. Message Processing &lt; 3 sec</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3b2a0-226">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b2a0-226">See Also</span></span>


[<span data-ttu-id="3b2a0-227">Lync Server-Netzwerkhandbuch</span><span class="sxs-lookup"><span data-stu-id="3b2a0-227">Lync Server Networking Guide</span></span>](https://go.microsoft.com/fwlink/p/?linkid=390677)  
[<span data-ttu-id="3b2a0-228">Wichtige Integritätsindikatoren: die Grundlage für die Verwaltung von fehlerfreien lync-Servern</span><span class="sxs-lookup"><span data-stu-id="3b2a0-228">Key Health Indicators: The Foundation for Maintaining Healthy Lync Servers</span></span>](https://go.microsoft.com/fwlink/?linkid=391838)  
[<span data-ttu-id="3b2a0-229">Methodik der lync-Anrufqualität</span><span class="sxs-lookup"><span data-stu-id="3b2a0-229">Lync Call Quality Methodology</span></span>](https://go.microsoft.com/fwlink/?linkid=391841)  
  

<span data-ttu-id="3b2a0-230"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3b2a0-230"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

