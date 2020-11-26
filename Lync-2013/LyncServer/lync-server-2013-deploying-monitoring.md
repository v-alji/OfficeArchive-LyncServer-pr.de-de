---
title: 'Lync Server 2013: Bereitstellen der Überwachung'
description: 'Lync Server 2013: Bereitstellen der Überwachung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying monitoring
ms:assetid: 117f4a3e-0670-4388-a553-b9854921145f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398199(v=OCS.15)
ms:contentKeyID: 48183442
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1821198ddd0b4164f6932122aa9cf00ac34aada
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429867"
---
# <a name="deploying-monitoring-in-lync-server-2013"></a><span data-ttu-id="3fa7f-103">Bereitstellen der Überwachung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3fa7f-103">Deploying monitoring in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3fa7f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3fa7f-104">

<span> </span></span></span>

<span data-ttu-id="3fa7f-105">_**Letztes Änderungsdatum des Themas:** 2013-12-17_</span><span class="sxs-lookup"><span data-stu-id="3fa7f-105">_**Topic Last Modified:** 2013-12-17_</span></span>

<span data-ttu-id="3fa7f-106">Wichtige Änderungen wurden an der Überwachungsinfrastruktur von Microsoft lync Server 2013 vorgenommen, beginnend mit der Tatsache, dass die Überwachungs Server Rolle veraltet ist.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-106">Major changes have been made to the Microsoft Lync Server 2013 monitoring infrastructure, beginning with the fact that the Monitoring Server role has been deprecated.</span></span> <span data-ttu-id="3fa7f-107">Anstelle von separaten Überwachungsserver Rollen (die in der Regel erforderlich sind, dass Organisationen dedizierte Computer einrichten, um als Überwachungsserver zu fungieren) sind die Überwachungsdienste nun auf jedem Front-End-Server angeordnet.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-107">Instead of separate Monitoring Server roles (which typically required organizations to set up dedicated computers to act as Monitoring servers) monitoring services are now collocated on each Front End server.</span></span> <span data-ttu-id="3fa7f-108">Diese Änderung unterstützt u. a.:</span><span class="sxs-lookup"><span data-stu-id="3fa7f-108">Among other things, this change helps to:</span></span>

  - <span data-ttu-id="3fa7f-109">Verringern Sie die Anzahl der Serverrollen, die bei der Implementierung von lync Server 2013 erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-109">Decrease the number of server roles required when implementing Lync Server 2013.</span></span> <span data-ttu-id="3fa7f-110">In diesem Fall hilft die Dekrementierung der Monitoring Server-Serverrolle auch, die Kosten zu senken, da keine dedizierten Server für die Überwachung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-110">In this case, decrementing the Monitoring Server server role also helps to reduce costs by eliminating the need to maintain dedicated servers for monitoring.</span></span>

  - <span data-ttu-id="3fa7f-111">Verringern Sie die Komplexität von lync Server-Setup und-Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-111">Reduce the complexity of Lync Server setup and administration.</span></span> <span data-ttu-id="3fa7f-112">Durch automatisches abstimmen der Überwachungsdienste auf jedem Front-End-Server müssen Sie die Monitoring Server-Rolle nicht mehr installieren, konfigurieren und verwalten.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-112">By automatically collocating the monitoring services on each Front End server you no longer have to install, configure, and manage the Monitoring Server role.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3fa7f-113">Die Rolle des Archivierungsservers wurde in lync Server 2013 ebenfalls als veraltet markiert.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-113">The Archiving Server role has also been deprecated in Lync Server 2013.</span></span> <span data-ttu-id="3fa7f-114">Wie die Überwachungsdienste sind die lync Server 2013-Archivierungsdienste nun auf jedem Front-End-Server angeordnet.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-114">Like the monitoring services, Lync Server 2013 archiving services are now collocated on each Front End server.</span></span> <span data-ttu-id="3fa7f-115">Dies ist wichtig, da die Überwachung und Archivierung häufig dieselbe SQL Server-Datenbankinstanz verwenden.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-115">This is important to note simply because monitoring and archiving often share the same SQL Server database instance.</span></span>



</div>

<span data-ttu-id="3fa7f-116">Wie Sie vielleicht erwarten, haben diese Änderungen einen großen Einfluss darauf, wie Überwachungsdienste installiert und verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-116">As you might expect, these changes have a major impact on how monitoring services are installed and managed.</span></span> <span data-ttu-id="3fa7f-117">Wenn beispielsweise die Monitoring Server-Rolle nicht mehr vorhanden ist, wurde der Monitoring Server-Knoten aus dem lync Server Topology Builder entfernt; Das bedeutet wiederum, dass Sie den neuen Monitoring Server-Assistenten von Topology Builder nicht mehr verwenden, um Ihrer Topologie einen neuen Monitoring Server hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-117">For example, because the Monitoring Server role no longer exists, the Monitoring Server node has been removed from the Lync Server Topology Builder; in turn, that means you no longer use Topology Builder's New Monitoring Server Wizard in order to add a new Monitoring Server to your topology.</span></span> <span data-ttu-id="3fa7f-118">(Dieser Assistent ist nicht mehr vorhanden.) Stattdessen implementieren Sie in der Regel Überwachungsdienste in Ihrer Topologie, indem Sie die beiden folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="3fa7f-118">(That wizard no longer exists.) Instead, you will typically implement monitoring services within your topology by completing the following two steps:</span></span>

1.  <span data-ttu-id="3fa7f-119">Aktivieren der Überwachung zur gleichen Zeit beim Einrichten eines neuen lync Server-Pools.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-119">Enabling monitoring at the same time you set up a new Lync Server pool.</span></span> <span data-ttu-id="3fa7f-120">(In lync Server 2013 ist die Überwachung in Pool-by-Pool-Basis aktiviert oder deaktiviert.) Beachten Sie, dass Sie die Überwachung für einen Pool aktivieren können, ohne tatsächlich Überwachungsdaten zu sammeln, was im Abschnitt Konfigurieren der Aufzeichnung von Anrufdetails und der Einstellungen für die Qualität der Benutzerfreundlichkeit dieser Dokumentation erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-120">(In Lync Server 2013, monitoring is enabled or disabled on a pool-by-pool basis.) Note that you can enable monitoring for a pool without actually collecting monitoring data, a process explained in the Configuring Call Detail Recording and Quality of Experience Settings section of this documentation.</span></span>

2.  <span data-ttu-id="3fa7f-p107">Zuordnen eines Überwachungsspeichers (d. h. einer Überwachungsdatenbank) zum neuen Pool. Ein einzelner Überwachungsspeicher kann mehreren Pools zugeordnet werden. Abhängig von der Anzahl von Benutzern, die in Ihren Registrierungsstellenpools verwaltet werden, bedeutet dies, dass Sie keine separate Überwachungsdatenbank für jeden Pool einrichten müssen. Stattdessen können einzelne Überwachungsspeicher von mehreren Pools verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-p107">Associating a monitoring store (that is, a monitoring database) with the new pool. Note that a single monitoring store can be associated with multiple pools. Depending on the number of users homed on your Registrar pools, that means that you do not have to set up a separate monitoring database for each of your pools. Instead, single monitoring store can be used by multiple pools.</span></span>

<span data-ttu-id="3fa7f-125">Zwar ist es oft einfacher, die Überwachung zur gleichen Zeit zu aktivieren, in der Sie einen neuen Pool erstellen, aber es ist auch möglich, einen neuen Pool mit deaktivierter Überwachung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-125">Although it's often easier to enable monitoring at the same time that you create a new pool, it's also possible to create a new pool with monitoring disabled.</span></span> <span data-ttu-id="3fa7f-126">In diesem Fall können Sie später mithilfe des Topologie-Generators den Dienst aktivieren: Topologie-Generator bietet eine Möglichkeit zum Aktivieren oder Deaktivieren der Überwachung für einen Pool oder zum Zuordnen eines Pools zu einem anderen Überwachungsspeicher.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-126">If you do that, you can later use Topology Builder to enable the service: Topology Builder provides a way to enable or disable monitoring for a pool, or to associate a pool with a different monitoring store.</span></span> <span data-ttu-id="3fa7f-127">Beachten Sie, dass Sie zwar nicht mehr über eine Überwachungs Server Rolle verfügen, aber dennoch mindestens einen Überwachungsspeicher erstellen müssen: Back-End-Datenbanken, die zum Speichern der vom Überwachungsdienst gesammelten Daten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-127">Keep in mind that even though there is no longer a Monitoring Server role you will still need to create one or more monitoring stores: backend databases used to store the data gathered by the monitoring service.</span></span> <span data-ttu-id="3fa7f-128">Diese Back-End-Datenbankenkönnen entweder mit Microsoft SQL Server 2008 R2 oder mit Microsoft SQL Server 2012 erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-128">These backend databases can be created using either Microsoft SQL Server 2008 R2 or Microsoft SQL Server 2012.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3fa7f-129">Wenn die Überwachung für einen Pool aktiviert wurde, können Sie den Prozess des Sammelns von Überwachungsdaten deaktivieren, ohne Ihre Topologie ändern zu müssen: die lync Server-Verwaltungsshell bietet eine Möglichkeit, die Datensammlung zur Anrufdetailaufzeichnung (CDR) oder zur Quality of Experience (QoE) zu deaktivieren (und später erneut zu aktivieren).</span><span class="sxs-lookup"><span data-stu-id="3fa7f-129">If monitoring has been enabled for a pool you can disable the process of collecting monitoring data without having to change your topology: Lync Server Management Shell provides a way for you to disable (and then later re-enable) call detail recording (CDR) or Quality of Experience (QoE) data collection.</span></span> <span data-ttu-id="3fa7f-130">Weitere Informationen finden Sie in diesem Dokument im Abschnitt „Konfigurieren von KDS (Aufzeichnung von Kommunikationsdatensätzen)“ und „QoE (Quality of Experience)-Einstellungen“.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-130">For more information, see the Configuring Call Detail Recording and Quality of Experience Settings section of this document.</span></span>



</div>

<span data-ttu-id="3fa7f-131">Eine weitere wichtige Verbesserung der Überwachung in lync Server 2013 ist die Tatsache, dass die lync Server-Überwachungsberichte nun IPv6 unterstützen: Berichte, die das Feld IP-Adresse verwenden, werden je nach: 1) der verwendeten SQL-Abfrage entweder IPv4-oder IPv6-Adressen angezeigt. und 2) Wenn die IPv6-Adresse in der Überwachungsdatenbank gespeichert ist.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-131">One other important enhancement to monitoring in Lync Server 2013 is the fact that Lync Server Monitoring Reports now support IPv6: reports that use the IP Address field will display either IPv4 or IPv6 addresses depending on : 1) the SQL query being used; and, 2) where or not the IPv6 address is stored in the monitoring database.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3fa7f-132">Vergewissern Sie sich, dass der Starttyp des SQL Server-Agent-Diensts „Automatisch“ ist und der SQL Server-Agent-Dienst für die SQL-Instanz mit den Überwachungsdatenbanken ausgeführt wird, damit die SQL Server-Wartungsaufträge für die Standardüberwachung plangemäß unter der Kontrolle des SQL Server-Agent-Diensts ausgeführt werden können.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-132">Ensure that the SQL Server Agent Service Startup Type is Automatic and the SQL Server Agent Service is running for the SQL Instance which is holding the Monitoring databases, so that the Default Monitoring SQL Server Maintenance Jobs can run on their scheduled basis under the control of the SQL Server Agent Service.</span></span>



</div>

<span data-ttu-id="3fa7f-133">Diese Dokumentation führt Sie durch den Vorgang zum Installieren und Konfigurieren von Überwachungs-und Überwachungsberichten für lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-133">This documentation walks you through the process of installing and configuring monitoring and Monitoring Reports for Lync Server 2013.</span></span> <span data-ttu-id="3fa7f-134">Die Dokumentation enthält Schritt-für-Schritt-Anleitungen für Folgendes:</span><span class="sxs-lookup"><span data-stu-id="3fa7f-134">The documentation provides step-by-step instructions that will help you to:</span></span>

  - <span data-ttu-id="3fa7f-135">Aktivieren der Überwachung in Ihrer Topologie und Zuordnen eines Überwachungsspeichers zu einem Front-End-Pool.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-135">Enable monitoring in your topology and associate a monitoring store with a Front End pool.</span></span>

  - <span data-ttu-id="3fa7f-136">Installieren Sie SQL Server Reporting Services und die lync Server-Überwachungsberichte.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-136">Install SQL Server Reporting Services and the Lync Server Monitoring Reports.</span></span> <span data-ttu-id="3fa7f-137">Überwachungsberichte sind vorkonfigurierte Berichte, die verschiedene Einsichten in die in einer Überwachungsdatenbank gespeicherten Informationen bieten.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-137">Monitoring Reports are preconfigured reports that provide different views into the information stored in a monitoring database.</span></span>

  - <span data-ttu-id="3fa7f-138">Konfigurieren Sie die Datensammlung zur Anrufdetailaufzeichnung (CDR) und zur Quality of Experience (QoE).</span><span class="sxs-lookup"><span data-stu-id="3fa7f-138">Configure call detail recording (CDR) and Quality of Experience (QoE) data collection.</span></span> <span data-ttu-id="3fa7f-139">Die Aufzeichnung von Anrufdetails bietet eine Möglichkeit, die Nutzung von lync-Server Funktionen wie VoIP-Telefon anrufen (Voice over IP) nachvollziehen zu können. Instant Messaging (im) Dateiübertragungen; Audio/Video-Konferenzen (A/V); und Anwendungsfreigabesitzungen.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-139">Call detail recording provides a way for you to track usage of Lync Server capabilities such as Voice over IP (VoIP) phone calls; instant messaging (IM); file transfers; audio/video (A/V) conferencing; and application sharing sessions.</span></span> <span data-ttu-id="3fa7f-140">QoE-Metriken dienen zur Überwachung der Qualität von Audio- und Videoanrufen in Ihrer Organisation, z. B. der Anzahl der verloren gegangenen Netzwerkpakete, von Hintergrundgeräuschen und der Unterschiede bei der Paketverzögerung (Jitter).</span><span class="sxs-lookup"><span data-stu-id="3fa7f-140">QoE metrics track the quality of audio and video calls made in your organization, including such things as the number of network packets lost, background noise, and the amount of "jitter" (differences in packet delay).</span></span>

  - <span data-ttu-id="3fa7f-141">Manuelles Löschen von KDS und/oder QoE-Datensätzen aus der Überwachungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="3fa7f-141">Manually purge CDR and/or QoE records from the monitoring database.</span></span>

<span data-ttu-id="3fa7f-142"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3fa7f-142"></div>

<span> </span>

</div>

</div>

</span></span></div>

