---
title: 'Lync Server 2013: Installieren einer optionalen Software'
description: 'Lync Server 2013: Installieren optionaler Software.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing optional software
ms:assetid: b95b3301-fa1e-4b96-9af4-05b43d39db8d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615032(v=OCS.15)
ms:contentKeyID: 51541509
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7423c0d54b762fb4af7cedc8d7ba8745fd94bdf7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427026"
---
# <a name="installing-optional-software-in-lync-server-2013"></a><span data-ttu-id="6f8a7-103">Installieren von optionaler Software in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f8a7-103">Installing optional software in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6f8a7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6f8a7-104">

<span> </span></span></span>

<span data-ttu-id="6f8a7-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="6f8a7-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="6f8a7-106">Das Planungs Tool für Microsoft lync Server 2013 ist für den Export nach Microsoft Excel und Microsoft Visio vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="6f8a7-106">The Microsoft Lync Server 2013, Planning Tool is designed to export to Microsoft Excel and Microsoft Visio.</span></span> <span data-ttu-id="6f8a7-107">Obwohl diese Anwendungen nicht für den Betrieb des Planungstools erforderlich sind, fügen Sie der Bereitstellung und Dokumentation Ihres Entwurfs einen erheblichen Mehrwert hinzu.</span><span class="sxs-lookup"><span data-stu-id="6f8a7-107">While these applications are not required for the operation of the Planning Tool, they do add significant value to the deployment and documentation of your design.</span></span>

<div>

## <a name="optional-software"></a><span data-ttu-id="6f8a7-108">Optionale Software</span><span class="sxs-lookup"><span data-stu-id="6f8a7-108">Optional Software</span></span>

<div>

## <a name="microsoft-excel"></a><span data-ttu-id="6f8a7-109">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="6f8a7-109">Microsoft Excel</span></span>

<span data-ttu-id="6f8a7-110">Beim Exportieren Ihres Entwurfs nach Microsoft Excel wird ein Bericht in Form einer Tabelle mit sieben Registerkarten erstellt:</span><span class="sxs-lookup"><span data-stu-id="6f8a7-110">Exporting your design to Microsoft Excel creates a report that displays seven tabs in the spreadsheet:</span></span>

  - <span data-ttu-id="6f8a7-111">Zusammenfassung - Zeigt Informationen zur Standortkonfiguration an, u. a. Benutzeranzahl, Kapazitätseinstellungen und Serverprofilinformationen.</span><span class="sxs-lookup"><span data-stu-id="6f8a7-111">Summary – Displays information on site configuration, including user count, capacity settings, and server profile information.</span></span>

  - <span data-ttu-id="6f8a7-p102">Hardwareprofil - Zeigt einen Bericht zu den empfohlenen Hardwarekonfigurationen für Server an, die in der Topologie angegeben sind (einschließlich CPU, Arbeitsspeicher, Datenträger und Netzwerkschnittstelle). Die Anzahl und die empfohlenen Spezifikationen für die Serverkomponenten sind auch enthalten. Darüber hinaus ist jeder Server nach Standort definiert, um eine vollständige Darstellung der Serveranforderungen nach Standort bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6f8a7-p102">Hardware Profile – Displays a report on the recommended hardware configurations for servers that are specified in the topology, including CPU, memory, disk, and network interface. The quantity and recommended specifications for the server components are also included. In addition, each server is defined by site to provide a complete representation of server requirements by site.</span></span>

  - <span data-ttu-id="6f8a7-p103">Portanforderungen - Zeigt einen Bericht zu allen aktivierten Ports sowie die Zuordnung zum Domain Name System-Lastenausgleich (DNS-LB) und zu Hardwaregeräten zum Lastenausgleich (HLB) an. Sie sollten diesen Bericht zum Planen der Konfiguration von Firewall sowie DNS-Lastenausgleich und Hardwaregeräten zum Lastenausgleich verwenden.</span><span class="sxs-lookup"><span data-stu-id="6f8a7-p103">Ports Requirements – Displays a report of all ports that are enabled, and the association to Domain Name System load balancing (DNS LB) and hardware load balancers (HLB). You should use this report to plan your firewall and DNS LB and HLB configurations.</span></span>

  - <span data-ttu-id="6f8a7-117">Zusammenfassungsbericht – zeigt die allgemeine Zusammenfassung der Einstellungen an, die zum Einrichten Ihres Edge-Server-Netzwerks erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6f8a7-117">Summary Report – Displays the general summary of the settings that are required to set up your Edge Server network.</span></span>

  - <span data-ttu-id="6f8a7-118">Zertifikat Bericht – zeigt den Namen des Antragstellers und des Subjekts an, die für die erforderlichen Zertifikate erforderlich sind, damit die Edgeserver ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="6f8a7-118">Certificates Report – Displays the subject name and subject alternate names that are required for the certificates needed to get the Edge Servers running.</span></span>

  - <span data-ttu-id="6f8a7-119">Firewallbericht - Zeigt die Quell- und Zielports und die IP-Adressen für sowohl externe als auch interne Schnittstellten an.</span><span class="sxs-lookup"><span data-stu-id="6f8a7-119">Firewall Report – Displays the source and destination ports and IP addresses for both External and Internal interfaces.</span></span>

  - <span data-ttu-id="6f8a7-120">DNS-Bericht - Zeigt den vollqualifizierten Domänennamen (FQDN) und die IP/VIP-Adressen an, die für jeden von Ihnen erstellten DNS-Eintrag erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6f8a7-120">DNS Report – Displays the fully qualified domain name (FQDN) and IP/VIP addresses required for each DNS entry that you create.</span></span>

</div>

<div>

## <a name="microsoft-visio"></a><span data-ttu-id="6f8a7-121">Microsoft Visio</span><span class="sxs-lookup"><span data-stu-id="6f8a7-121">Microsoft Visio</span></span>

<span data-ttu-id="6f8a7-p104">Beim Exportieren Ihres Entwurfs nach Microsoft Visio wird ein Diagramm erstellt, das Sie zur Dokumentation Ihrer konfigurierten Topologie und Infrastruktur verwenden können. Das importierte Diagramm kann bearbeitet und neu angeordnet werden, um Ihre Dokumentationsanforderungen zu erfüllen. Das typische Visio-Diagramm umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="6f8a7-p104">Exporting your design to Microsoft Visio creates a diagram for use in your documentation purposes of your configured topology and infrastructure. The imported diagram can be edited and rearranged to meet your documentation needs. The typical Visio diagram will include:</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6f8a7-125">Wenn Ihr Entwurf groß genug ist, um mehr als drei Front-End-Server zu erfordern, wird eine zusätzliche Seite für den Front-End-Pool, Front-End-Server, den Computer mit SQL Server, IP-Adressen und FQDNs erstellt.</span><span class="sxs-lookup"><span data-stu-id="6f8a7-125">If your design is large enough to require more than three Front End Servers, an additional page will be created for the Front End pool, Front End Servers, the computer running SQL Server, IP addresses, and FQDNs.</span></span>



</div>

  - <span data-ttu-id="6f8a7-126">Globale Topologie – Diagramm der konfigurierten lync Server 2013-Websites.</span><span class="sxs-lookup"><span data-stu-id="6f8a7-126">Global Topology – Diagram of configured Lync Server 2013 sites.</span></span>

  - <span data-ttu-id="6f8a7-127">Registerkarte "Website Name" – zeigt die Topologie der Websitekonfiguration mit Edgeserver, Firewall, PSTN (Public Switched Telephone Network) mit Gateways und der internen Server Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="6f8a7-127">Site Name tab – Displays the site configuration topology with Edge Server, firewall, public switched telephone network (PSTN) with gateways, and the internal server deployment.</span></span> <span data-ttu-id="6f8a7-128">Die interne Bereitstellung besteht aus konfigurierten Servern und Pools, einschließlich der Front-End-Pools, SQL Server-basierten Servern, Active Directory-Domänendiensten, Directors, Exchange Unified Messaging (um)-Servern, Exchange-Postfachservern, Office Web Apps-Servern, Vermittlungsservern und beständigen Chat Servern.</span><span class="sxs-lookup"><span data-stu-id="6f8a7-128">Internal deployment consists of configured servers and pools, including the Front End pools, SQL Server-based servers, Active Directory Domain Services, Directors, Exchange Unified Messaging (UM) servers, Exchange Mailbox Servers, Office Web Apps Servers, Mediation Servers, and Persistent Chat Servers.</span></span>

  - <span data-ttu-id="6f8a7-129">Edge-Netzwerkdiagramm – Diagramm, in dem die Edgeserver-Konfiguration mit zugehörigen IP-Adressen und FQDNs erläutert wird.</span><span class="sxs-lookup"><span data-stu-id="6f8a7-129">Edge Network Diagram – Diagram detailing the Edge Server configuration with associated IP addresses and FQDNs.</span></span> <span data-ttu-id="6f8a7-130">DNS-Lastenausgleich und Hardwarelastenausgleich sind ebenfalls enthalten.</span><span class="sxs-lookup"><span data-stu-id="6f8a7-130">DNS load balancing and hardware load balancers are also included.</span></span> <span data-ttu-id="6f8a7-131">Darüber hinaus werden Directors und der Front-End-Server oder der Front-End-Pool mit zugeordneter DNS lb oder HLB und der zugewiesenen IP-Adresse (das Planungs Tool unterstützt IPv4-und IPv6-Adressen) und dem FQDN angezeigt.</span><span class="sxs-lookup"><span data-stu-id="6f8a7-131">Additionally, Directors and the Front End Server or Front End pool are displayed, with associated DNS LB or HLB and the assigned IP address (the Planning Tool supports both IPv4 and IPv6 addresses) and FQDN.</span></span>

</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6f8a7-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6f8a7-132">See Also</span></span>


[<span data-ttu-id="6f8a7-133">Installieren des Planungstools in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6f8a7-133">Installing the Planning Tool in Lync Server 2013</span></span>](lync-server-2013-installing-the-planning-tool.md)  
  

<span data-ttu-id="6f8a7-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6f8a7-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

