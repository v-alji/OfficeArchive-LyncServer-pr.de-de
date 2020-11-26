---
title: 'Lync Server 2013: Betriebs Abhängigkeiten'
description: 'Lync Server 2013: Betriebs Abhängigkeiten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Operational dependencies
ms:assetid: 450b6be2-7fb3-47d7-8b0b-c05faa331e14
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720559(v=OCS.15)
ms:contentKeyID: 63969597
ms.date: 05/16/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e240981f5dfded7c27f123c8483794ea3ffedff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445295"
---
# <a name="operational-dependencies-in-lync-server-2013"></a><span data-ttu-id="69596-103">Betriebs Abhängigkeiten in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="69596-103">Operational dependencies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="69596-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="69596-104">

<span> </span></span></span>

<span data-ttu-id="69596-105">_**Letztes Änderungsdatum des Themas:** 2015-05-15_</span><span class="sxs-lookup"><span data-stu-id="69596-105">_**Topic Last Modified:** 2015-05-15_</span></span>

<span data-ttu-id="69596-106">Die in diesem Dokument beschriebene Referenzarchitektur wird Ihnen dabei helfen sicherzustellen, dass Sie über eine lync Server 2013-Bereitstellung verfügen, die nicht nur auf die Anforderungen der Organisation skaliert, sondern nach den bewährten Microsoft-Methoden entworfen wurde.</span><span class="sxs-lookup"><span data-stu-id="69596-106">The Reference Architecture discussed in this document will help ensure that you have a Lync Server 2013 deployment that not only scales to the organization’s requirements but is architected as per Microsoft best practices.</span></span> <span data-ttu-id="69596-107">Es kann sein, dass die lync Server 2013-Implementierung ein dynamischer Dienst ist und wie jeder andere Dienst im Unternehmen weiterhin Überwachungs-und proaktives Management erfordert, um dem Unternehmen ein hohes Maß an Serviceverfügbarkeit und Servicequalität zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="69596-107">Be that as it may the Lync Server 2013 implementation is a dynamic service and like any other service in the enterprise still requires monitoring and proactive management to maintain high level of service availability and service quality to the business.</span></span>

<span data-ttu-id="69596-108">Da lync Server 2013 in der täglichen Geschäftstätigkeit des Unternehmens tief verwurzelt ist, ist es wichtig, dass der Dienst durch ein genaues und greifbares Service Level-Management verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="69596-108">As Lync Server 2013 becomes deeply ingrained in the organization’s everyday business it is important that the service be managed by accurate and tangible service level management.</span></span> <span data-ttu-id="69596-109">Die lync-Systemarchitektur kann komplex und sehr integriert werden, und um ein effektives Service Level-Management zu gewährleisten und SLAs für lync Server 2013 festzulegen, wird es entscheidend, die Abhängigkeiten des Systems auf anderen Plattformen und Servern zu verstehen.</span><span class="sxs-lookup"><span data-stu-id="69596-109">The Lync system architecture can become complex and very integrated and in order to maintain effective service level management and establish SLAs for Lync Server 2013 it becomes critical to understand the system’s dependencies on other platforms and servers.</span></span> <span data-ttu-id="69596-110">Ebenso wichtig ist, zu beachten, welche Unternehmensdienste wie Sprach-und UC-integrierte Anwendungen von lync abhängig werden.</span><span class="sxs-lookup"><span data-stu-id="69596-110">Equally important is to note which business services, such as voice and UC integrated applications, become dependent on Lync.</span></span>

<span data-ttu-id="69596-111">Lync Server 2013 muss eingerichtet werden, wobei alle genannten Abhängigkeiten berücksichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="69596-111">Lync Server 2013 must be established noting all the said dependencies.</span></span> <span data-ttu-id="69596-112">Die Dienstzuordnung ermöglicht es Ihnen, eine SLA zwischen lync und dem abhängigen Dienst zu formulieren und einen Ausgangspunkt für die SLA-Aushandlung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="69596-112">The service map will allow you to formulate a SLA between Lync and its dependent service and provide a starting place for SLA negotiation.</span></span>

<span data-ttu-id="69596-113">In der folgenden Tabelle sind die typischen Abhängigkeitsdienste für eine lync-Infrastruktur aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="69596-113">The following table lists the typical dependency services for a Lync infrastructure.</span></span> <span data-ttu-id="69596-114">Jede dieser Technologien sollte eine eigene proaktive Überwachung aufweisen.</span><span class="sxs-lookup"><span data-stu-id="69596-114">Each of these technologies should have its own proactive monitoring.</span></span>

### <a name="typical-dependency-services"></a><span data-ttu-id="69596-115">Typische Abhängigkeitsdienste</span><span class="sxs-lookup"><span data-stu-id="69596-115">Typical dependency services</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="69596-116">Abhängigkeitsdienst</span><span class="sxs-lookup"><span data-stu-id="69596-116">Dependency Service</span></span></th>
<th></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69596-117">Betriebssysteme</span><span class="sxs-lookup"><span data-stu-id="69596-117">Operating systems</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69596-118">Server Hardware</span><span class="sxs-lookup"><span data-stu-id="69596-118">Server Hardware</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69596-119">Active Directory</span><span class="sxs-lookup"><span data-stu-id="69596-119">Active Directory</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69596-120">Infrastruktur öffentlicher Schlüssel</span><span class="sxs-lookup"><span data-stu-id="69596-120">Public Key Infrastructure</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69596-121">Domain Naming Service</span><span class="sxs-lookup"><span data-stu-id="69596-121">Domain Naming Service</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69596-122">Datenbankdienste</span><span class="sxs-lookup"><span data-stu-id="69596-122">Database Services</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69596-123">Speicherdienste</span><span class="sxs-lookup"><span data-stu-id="69596-123">Storage Services</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69596-124">System Verwaltung – Überwachung und Verteilung</span><span class="sxs-lookup"><span data-stu-id="69596-124">System Management – Monitoring and distribution</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69596-125">Security Services – Antivirus</span><span class="sxs-lookup"><span data-stu-id="69596-125">Security Services - Antivirus</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69596-126">Netzwerkinfrastruktur – Internet</span><span class="sxs-lookup"><span data-stu-id="69596-126">Network Infrastructure - Internet</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69596-127">Netzwerkinfrastruktur – intern (LAN/WAN)</span><span class="sxs-lookup"><span data-stu-id="69596-127">Network Infrastructure – Internal (LAN/WAN)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69596-128">Telefonie-Infrastruktur – IP-PBX und Gateways</span><span class="sxs-lookup"><span data-stu-id="69596-128">Telephony Infrastructure – IP-PBX and Gateways</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69596-129">Cloud-Dienste</span><span class="sxs-lookup"><span data-stu-id="69596-129">Cloud Services</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="69596-130">Es wird davon ausgegangen, dass die Organisation in der Lage ist, grundlegende Service Level-Verwaltungsfunktionen wie Change-, Incident-und Release-Management gemäß dem MOF-Verfahren zu entwickeln.</span><span class="sxs-lookup"><span data-stu-id="69596-130">It is assumed that the organization is operationally mature in exercising basic service level management functions such as change, incident and release management as prescribed by the MOF.</span></span> <span data-ttu-id="69596-131">Die lync-Lösung sollte von diesen Funktionen übernommen werden und den gleichen operativen Verwaltungsprozessen unterworfen werden.</span><span class="sxs-lookup"><span data-stu-id="69596-131">The Lync solution should be adopted by these functions and become subject to the same operational management processes.</span></span>

<span data-ttu-id="69596-132">Aufbauend auf den obigen Informationen haben wir jetzt ein größeres Verständnis darüber, was sich auf den lync-Dienst im Unternehmen auswirken kann.</span><span class="sxs-lookup"><span data-stu-id="69596-132">Building on the information obtained above we now have a greater understanding of what can impact the Lync service in the enterprise.</span></span> <span data-ttu-id="69596-133">Um die Verfügbarkeit und Qualität von lync Server 2013 zu gewährleisten, müssen die folgenden Überwachungstools mit der Bereitstellung der Referenzarchitektur einhergehen:</span><span class="sxs-lookup"><span data-stu-id="69596-133">To help ensure Lync Server 2013 service availability and quality, the following monitoring tools must accompany the reference architecture deployment:</span></span>

### <a name="monitoring-tools"></a><span data-ttu-id="69596-134">Überwachungstools</span><span class="sxs-lookup"><span data-stu-id="69596-134">Monitoring tools</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="69596-135">Komponente</span><span class="sxs-lookup"><span data-stu-id="69596-135">Component</span></span></th>
<th><span data-ttu-id="69596-136">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="69596-136">Description</span></span></th>
<th><span data-ttu-id="69596-137">Anwendbare Website</span><span class="sxs-lookup"><span data-stu-id="69596-137">Applicable Site</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69596-138">Lync Server 2013-Überwachungs Server</span><span class="sxs-lookup"><span data-stu-id="69596-138">Lync Server 2013 Monitoring Server</span></span></p></td>
<td><p><span data-ttu-id="69596-139">Stellen Sie mindestens eine lync Server 2013 Monitoring Server-Rolle pro zentralen Standort bereit, und konfigurieren Sie das QoE-Berichterstattungs Paket (Quality of Experience).</span><span class="sxs-lookup"><span data-stu-id="69596-139">Deploy at least one Lync Server 2013 Monitoring Server role per Central site and configure Quality of Experience (QoE) Reporting Pack.</span></span></p>
<p><span data-ttu-id="69596-140">Weitere Informationen finden Sie in der Dokumentation zur lync Server 2013-Bereitstellung:</span><span class="sxs-lookup"><span data-stu-id="69596-140">Refer to the Lync Server 2013 Deployment documentation for further details:</span></span></p>
<p><span data-ttu-id="69596-141"><a href="lync-server-2013-deploying-monitoring.md">Bereitstellen der Überwachung in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="69596-141"><a href="lync-server-2013-deploying-monitoring.md">Deploying monitoring in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="69596-142">Zentrale Websites</span><span class="sxs-lookup"><span data-stu-id="69596-142">Central sites</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="69596-143">Binden Sie die einzelnen Pools an die nächstgelegene Instanz der Monitoring Server-Rolle.</span><span class="sxs-lookup"><span data-stu-id="69596-143">Tether each pool to its nearest instance of the Monitoring Server role.</span></span></p></td>
<td><p><span data-ttu-id="69596-144">Zentrale Websites</span><span class="sxs-lookup"><span data-stu-id="69596-144">Central sites</span></span></p>
<p><span data-ttu-id="69596-145">Zweigstellen</span><span class="sxs-lookup"><span data-stu-id="69596-145">Branch sites</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69596-146">System Center Operations Manager 2012</span><span class="sxs-lookup"><span data-stu-id="69596-146">System Center Operations Manager 2012</span></span></p></td>
<td><p><span data-ttu-id="69596-147">System Center Operations Manager 2012 mit importiertem Microsoft lync Server 2013 Management Pack (MP).</span><span class="sxs-lookup"><span data-stu-id="69596-147">System Center Operations Manager 2012 with the Microsoft Lync Server 2013 Management Pack (MP) imported.</span></span></p>
<p><span data-ttu-id="69596-148">Das Management Pack implementiert herkömmliches Ereignisprotokoll und Leistungsindikator basierte Instrumentation sowie die Aktivierung der neu verfügbaren Instrumentation in lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="69596-148">The Management Pack implements traditional Event Log and Performance counter based instrumentation is utilized as well as enabling newly available instrumentation in Lync Server 2013.</span></span></p></td>
<td><p><span data-ttu-id="69596-149">Zentrale Websites</span><span class="sxs-lookup"><span data-stu-id="69596-149">Central sites</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="69596-150">Stellen Sie sicher, dass die zentrale Ermittlung zur Erkennung von Rollen und Komponenten, die überwacht werden müssen, automatisch auf Grundlage eines zentralen Ermittlungsskripts abgeschlossen wird, das das in der zentralen Verwaltungsdatenbank veröffentlichte Topologie-Dokument liest.</span><span class="sxs-lookup"><span data-stu-id="69596-150">Make sure that Central Discovery to discovery of roles and components that need to be monitored are automatically completed based on a central discovery script that reads the topology document published in Central Management Database.</span></span></p></td>
<td><p><span data-ttu-id="69596-151">Zentraler Standort</span><span class="sxs-lookup"><span data-stu-id="69596-151">Central Site</span></span></p>
<p><span data-ttu-id="69596-152">Verzweigungs Website</span><span class="sxs-lookup"><span data-stu-id="69596-152">Branch Site</span></span></p>
<p><span data-ttu-id="69596-153">Edge-Website</span><span class="sxs-lookup"><span data-stu-id="69596-153">Edge Site</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="69596-154">Bereitstellen von System Center Operations Manager 2007-Agents für alle bereitgestellten Server mit lync Server</span><span class="sxs-lookup"><span data-stu-id="69596-154">Deploy System Centre Operations Manager 2007 agents to all deployed servers running Lync Server.</span></span></p></td>
<td><p><span data-ttu-id="69596-155">Zentraler Standort</span><span class="sxs-lookup"><span data-stu-id="69596-155">Central Site</span></span></p>
<p><span data-ttu-id="69596-156">Verzweigungs Website</span><span class="sxs-lookup"><span data-stu-id="69596-156">Branch Site</span></span></p>
<p><span data-ttu-id="69596-157">Edge-Website</span><span class="sxs-lookup"><span data-stu-id="69596-157">Edge Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="69596-158">Stellen Sie sicher, dass priorisierte Benachrichtigungen für Benachrichtigungen konfiguriert sind:</span><span class="sxs-lookup"><span data-stu-id="69596-158">Make sure Prioritized Alerts are configured for notification:</span></span></p>
<p><span data-ttu-id="69596-159">Benachrichtigungen mit höherer Priorität</span><span class="sxs-lookup"><span data-stu-id="69596-159">High Priority Alerts</span></span></p>
<p><span data-ttu-id="69596-160">Warnungen mittlerer Priorität</span><span class="sxs-lookup"><span data-stu-id="69596-160">Medium Priority Alerts</span></span></p>
<p><span data-ttu-id="69596-161">Andere Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="69596-161">Other Alerts.</span></span></p></td>
<td><p><span data-ttu-id="69596-162">Zentraler Standort</span><span class="sxs-lookup"><span data-stu-id="69596-162">Central Site</span></span></p>
<p><span data-ttu-id="69596-163">Verzweigungs Website</span><span class="sxs-lookup"><span data-stu-id="69596-163">Branch Site</span></span></p>
<p><span data-ttu-id="69596-164">Edge-Website</span><span class="sxs-lookup"><span data-stu-id="69596-164">Edge Site</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="69596-165">Konfigurieren Sie die Port Überwachung für Ihre Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="69596-165">Configure Port monitoring for your deployment.</span></span></p></td>
<td><p><span data-ttu-id="69596-166">Zentraler Standort</span><span class="sxs-lookup"><span data-stu-id="69596-166">Central Site</span></span></p>
<p><span data-ttu-id="69596-167">Verzweigungs Website</span><span class="sxs-lookup"><span data-stu-id="69596-167">Branch Site</span></span></p>
<p><span data-ttu-id="69596-168">Edge-Website</span><span class="sxs-lookup"><span data-stu-id="69596-168">Edge Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="69596-169">Konfigurieren der URL-Überwachung für Ihre Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="69596-169">Configure URL monitoring for your deployment</span></span></p></td>
<td><p><span data-ttu-id="69596-170">Zentraler Standort</span><span class="sxs-lookup"><span data-stu-id="69596-170">Central Site</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69596-171">Integration von lync und System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="69596-171">Lync and System Center Operations Manager integration</span></span></p></td>
<td><p><span data-ttu-id="69596-172">Bereitstellen von Anruf Zuverlässigkeit und Medienqualität MonitoringCall Zuverlässigkeit und Überwachung der Medienqualität verwenden Sie den Monitoring Server-Computer als Watcher-Knoten, um die Anruf Zuverlässigkeit und Medienqualität von lync Server zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="69596-172">Deploy Call Reliability and Media Quality MonitoringCall reliability and media quality monitoring use the Monitoring Server computer as their watcher node to monitor call reliability and media quality of Lync Server.</span></span> <span data-ttu-id="69596-173">Beide Features Abfragen die Monitoring Server-Datenbanken, um die Analyse durchführen zu können.</span><span class="sxs-lookup"><span data-stu-id="69596-173">Both of these features query the Monitoring Server databases to do analysis.</span></span></p></td>
<td><p><span data-ttu-id="69596-174">Zentraler Standort</span><span class="sxs-lookup"><span data-stu-id="69596-174">Central Site</span></span></p>
<p><span data-ttu-id="69596-175">Verzweigungs Website</span><span class="sxs-lookup"><span data-stu-id="69596-175">Branch Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="69596-176">Stellen Sie sicher, dass die Warnungsschwellenwerte für Medienqualität genau konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="69596-176">Ensure Media Quality warning thresholds are accurately configured.</span></span> <span data-ttu-id="69596-177">In der folgenden Tabelle ist die maximale Anzahl von Netzwerk Mittelwerten nach Codec angegeben.</span><span class="sxs-lookup"><span data-stu-id="69596-177">The following table indicates the maximum Network Mean Opinion Scores by Codec.</span></span> <span data-ttu-id="69596-178">In der Produktion sollten diese Bewertungen für einen festgelegten Zeitraum überwacht werden, und es müssen akzeptable Schwellenwerte basierend auf den organisationsspezifischen NMOS-Ergebnissen festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="69596-178">In production these scores should be monitored for a set period and acceptable thresholds must be established based on the organization specific NMOS scores.</span></span></p></td>
<td><p><span data-ttu-id="69596-179">Zentraler Standort</span><span class="sxs-lookup"><span data-stu-id="69596-179">Central Site</span></span></p>
<p><span data-ttu-id="69596-180">Verzweigungs Website</span><span class="sxs-lookup"><span data-stu-id="69596-180">Branch Site</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69596-181">Lync Server 2013, synthetischer Transaktionsmonitor</span><span class="sxs-lookup"><span data-stu-id="69596-181">Lync Server 2013 Synthetic Transaction Watcher</span></span></p></td>
<td><p><span data-ttu-id="69596-182">Bereitstellen eines dedizierten lync-Servers als synthetischer Transaktionsmonitor</span><span class="sxs-lookup"><span data-stu-id="69596-182">Deploy a dedicated Lync Server to be a synthetic transaction watcher.</span></span></p>
<p><span data-ttu-id="69596-183">Synthetische Transaktionen sind lync Server 2013 Windows PowerShell-Cmdlets, die vom Management Pack automatisch in einem vordefinierten Intervall ausgelöst werden.</span><span class="sxs-lookup"><span data-stu-id="69596-183">Synthetic transactions are Lync Server 2013 Windows PowerShell cmdlets that are automatically triggered by the management pack on a predefined interval.</span></span> <span data-ttu-id="69596-184">Diese werden auf einem synthetischen Transaktions Überwachungsknoten ausgeführt, bei dem es sich um einen vom Administrator benannten Server handelt, der für die Ermittlung und Ausführung von STS für jeden Pool verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="69596-184">These are executed on a synthetic transaction watcher node which is an administrator designated server responsible for discovery and execution of STs for each pool.</span></span></p>
<p><span data-ttu-id="69596-185">Es wird nicht empfohlen, einen vorhandenen Microsoft lync Server 2013-Server als synthetischer Transaktions Überwachungsknoten zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="69596-185">We do not recommend that you use an existing Microsoft Lync Server 2013 server as a synthetic transaction watcher node.</span></span> <span data-ttu-id="69596-186">Dies liegt an den Anforderungen an die CPU/Arbeitsspeichernutzung für die Ausführung von STS.</span><span class="sxs-lookup"><span data-stu-id="69596-186">This is due to the high CPU/memory usage requirements for running STs.</span></span> <span data-ttu-id="69596-187">Verwenden Sie einen neuen Server Computer (oder einen virtuellen Server) für den synthetischen Transaktions Überwachungsknoten.</span><span class="sxs-lookup"><span data-stu-id="69596-187">Use a new server computer (or a virtual server) for the synthetic transaction watcher node.</span></span></p></td>
<td><p><span data-ttu-id="69596-188">Zentraler Standort</span><span class="sxs-lookup"><span data-stu-id="69596-188">Central Site</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td><p><span data-ttu-id="69596-189">Bereitstellen des Überwachungs Knotens für synthetische Transaktionen</span><span class="sxs-lookup"><span data-stu-id="69596-189">Deploying synthetic transactions watcher node.</span></span></p>
<p><span data-ttu-id="69596-190">Weitere Informationen finden Sie im MonitoringCS_withSCOM.docx Dokument in der UCTAP Connect-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="69596-190">Refer to the MonitoringCS_withSCOM.docx document from UCTAP connect documentation.</span></span></p></td>
<td><p><span data-ttu-id="69596-191">Zentraler Standort</span><span class="sxs-lookup"><span data-stu-id="69596-191">Central Site</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="maximum-network-mos-scores-per-codec"></a><span data-ttu-id="69596-192">Maximale Anzahl von Netzwerk-Mos-Bewertungen Pro Codec</span><span class="sxs-lookup"><span data-stu-id="69596-192">Maximum Network MOS scores per codec</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="69596-193">Szenario</span><span class="sxs-lookup"><span data-stu-id="69596-193">Scenario</span></span></th>
<th><span data-ttu-id="69596-194">Codec</span><span class="sxs-lookup"><span data-stu-id="69596-194">Codec</span></span></th>
<th><span data-ttu-id="69596-195">Max NMOS</span><span class="sxs-lookup"><span data-stu-id="69596-195">Max NMOS</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="69596-196">UC-UC-Anruf</span><span class="sxs-lookup"><span data-stu-id="69596-196">UC-UC call</span></span></p></td>
<td><p><span data-ttu-id="69596-197">RTAudio WB</span><span class="sxs-lookup"><span data-stu-id="69596-197">RTAudio WB</span></span></p></td>
<td><p><span data-ttu-id="69596-198">4,10</span><span class="sxs-lookup"><span data-stu-id="69596-198">4.10</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69596-199">UC-UC-Anruf</span><span class="sxs-lookup"><span data-stu-id="69596-199">UC-UC call</span></span></p></td>
<td><p><span data-ttu-id="69596-200">RTAudio NB</span><span class="sxs-lookup"><span data-stu-id="69596-200">RTAudio NB</span></span></p></td>
<td><p><span data-ttu-id="69596-201">2,95</span><span class="sxs-lookup"><span data-stu-id="69596-201">2.95</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69596-202">Telefonkonferenz</span><span class="sxs-lookup"><span data-stu-id="69596-202">Conference call</span></span></p></td>
<td><p><span data-ttu-id="69596-203">Siren</span><span class="sxs-lookup"><span data-stu-id="69596-203">Siren</span></span></p></td>
<td><p><span data-ttu-id="69596-204">3,72</span><span class="sxs-lookup"><span data-stu-id="69596-204">3.72</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="69596-205">UC – PSTN-Anruf</span><span class="sxs-lookup"><span data-stu-id="69596-205">UC-PSTN call</span></span></p></td>
<td><p><span data-ttu-id="69596-206">RTAudio NB</span><span class="sxs-lookup"><span data-stu-id="69596-206">RTAudio NB</span></span></p></td>
<td><p><span data-ttu-id="69596-207">2,95</span><span class="sxs-lookup"><span data-stu-id="69596-207">2.95</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="69596-208">UC – PSTN-Anruf</span><span class="sxs-lookup"><span data-stu-id="69596-208">UC-PSTN call</span></span></p></td>
<td><p><span data-ttu-id="69596-209">G-711</span><span class="sxs-lookup"><span data-stu-id="69596-209">G-711</span></span></p></td>
<td><p><span data-ttu-id="69596-210">3,61</span><span class="sxs-lookup"><span data-stu-id="69596-210">3.61</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="69596-211">Über die vorherigen proaktiven Überwachungsaktivitäten hinaus sollten Wartungsaufgaben für zentral-, Edge-und Verzweigungs Standorte regelmäßig täglich, wöchentlich und monatlich ausgeführt werden, wie im lync RA-Betriebshandbuch definiert.</span><span class="sxs-lookup"><span data-stu-id="69596-211">Over and above the previous pro-active monitoring activities, maintenance tasks should be executed for Central, Edge and Branch sites on a recurring daily, weekly and monthly basis as defined in the Lync RA Operations Guide.</span></span>

<span data-ttu-id="69596-212"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="69596-212"></div>

<span> </span>

</div>

</div>

</span></span></div>

