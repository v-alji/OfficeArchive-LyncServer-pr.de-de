---
title: 'Lync Server 2013: Szenarien für Reverseproxys'
description: 'Lync Server 2013: Szenarien für Reverse-Proxy.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scenarios for reverse proxy
ms:assetid: 13108f59-a660-4ff1-8404-079d1cb646f2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204691(v=OCS.15)
ms:contentKeyID: 48183468
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cb714182fd13e42c6295e26ffd1edbb8b6041866
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394159"
---
# <a name="scenarios-for-reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="a3d86-103">Szenarien für Reverseproxys in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3d86-103">Scenarios for reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a3d86-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a3d86-104">

<span> </span></span></span>

<span data-ttu-id="a3d86-105">_**Letztes Änderungsdatum des Themas:** 2013-01-21_</span><span class="sxs-lookup"><span data-stu-id="a3d86-105">_**Topic Last Modified:** 2013-01-21_</span></span>

<span data-ttu-id="a3d86-106">Umgekehrte Proxys sind in lync Server 2013 für den Zugriff auf Dienste und Ressourcen wie die Besprechungs-und Einwahl einfachen URLs, das Adressbuch, den Besprechungsinhalt, die Erweiterung der Verteilerliste, Mobilitätsdienste und andere erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a3d86-106">Reverse proxies are required in Lync Server 2013 for providing access to services and resources such as the meeting and dial-in Simple URLs, address book, meeting content, distribution list expansion, mobility services, and others.</span></span> <span data-ttu-id="a3d86-107">Das typische Reverse-Proxy-Szenario in lync Server 2013 ist es, externen Clients (beispielsweise dem Desktop Client oder lync Web App-Client) Zugriff auf externe Webdienste des Director-oder Front-End-Servers zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="a3d86-107">The typical reverse proxy scenario in Lync Server 2013 is to allow external clients (for example, the desktop client or Lync Web App client) access to the Director or Front End Server external Web Services.</span></span>

<span data-ttu-id="a3d86-108">**Reverse-Proxy und externe Webdienste**</span><span class="sxs-lookup"><span data-stu-id="a3d86-108">**Reverse proxy and external web services**</span></span>

<span data-ttu-id="a3d86-109">![13142405-d5c9-45b7-a8b7-a8c89f09c97c](images/JJ204932.13142405-d5c9-45b7-a8b7-a8c89f09c97c(OCS.15).jpg "13142405-d5c9-45b7-a8b7-a8c89f09c97c")</span><span class="sxs-lookup"><span data-stu-id="a3d86-109">![13142405-d5c9-45b7-a8b7-a8c89f09c97c](images/JJ204932.13142405-d5c9-45b7-a8b7-a8c89f09c97c(OCS.15).jpg "13142405-d5c9-45b7-a8b7-a8c89f09c97c")</span></span>

<span data-ttu-id="a3d86-110">Während der Planungsphase definieren Sie die Anforderungen für den Reverse Proxy in einer lync Server 2013-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="a3d86-110">During the planning phase, you define the requirements for the reverse proxy in a Lync Server 2013 deployment.</span></span> <span data-ttu-id="a3d86-111">Der Reverse-Proxy ermöglicht den Zugriff auf Features für die folgenden externen Clients:</span><span class="sxs-lookup"><span data-stu-id="a3d86-111">The reverse proxy enables access to features for the following external clients:</span></span>

  - <span data-ttu-id="a3d86-112">Microsoft lync 2013-Desktop Client</span><span class="sxs-lookup"><span data-stu-id="a3d86-112">Microsoft Lync 2013 desktop client</span></span>

  - <span data-ttu-id="a3d86-113">Microsoft Lync Web App</span><span class="sxs-lookup"><span data-stu-id="a3d86-113">Microsoft Lync Web App</span></span>

  - <span data-ttu-id="a3d86-114">Microsoft Lync Mobile</span><span class="sxs-lookup"><span data-stu-id="a3d86-114">Microsoft Lync Mobile</span></span>

  - <span data-ttu-id="a3d86-115">Windows Store-App für Lync</span><span class="sxs-lookup"><span data-stu-id="a3d86-115">Lync Windows Store app</span></span>

<span data-ttu-id="a3d86-116">Bei der Planung Ihrer lync Server 2013-Bereitstellung ordnen Sie die tatsächlichen Anforderungen für lync Server 2013 den Reverse-Proxy Features zu.</span><span class="sxs-lookup"><span data-stu-id="a3d86-116">When planning your Lync Server 2013 deployment, you map the actual requirements for Lync Server 2013 to the reverse proxy features.</span></span>

1.  <span data-ttu-id="a3d86-117">Externe Clients stellen eine Verbindung mit dem Reverse Proxy auf Port TCP 443 her und verwenden Secure Socket Layer (SSL) oder Transport Layer Security (TLS).</span><span class="sxs-lookup"><span data-stu-id="a3d86-117">External clients will connect to the reverse proxy on port TCP 443 and will use secure socket layer (SSL) or transport layer security (TLS).</span></span> <span data-ttu-id="a3d86-118">Microsoft lync Mobile-Clients können eine Verbindung mit Port TCP 80 herstellen, allerdings nur, wenn die erste Verbindung mit den lync Discover-Diensten hergestellt wird und der Administrator die richtigen DNS-Einträge (Domain Name System) konfiguriert hat, und akzeptiert, dass diese Kommunikation nicht verschlüsselt wird.</span><span class="sxs-lookup"><span data-stu-id="a3d86-118">Microsoft Lync Mobile clients can connect on port TCP 80, but only when performing the initial connection to the Lync discover services and the administrator has configured the proper domain name system (DNS) CNAME (or alias) records, and accepts that this communication will not be encrypted.</span></span>

2.  <span data-ttu-id="a3d86-119">Lync Server 2013-externe Webdienste (bereitgestellt auf dem Front-End-Server und/oder der Director) erwarten eine Verbindung von einem Reverseproxy auf Port TCP 4443, und es wird erwartet, dass die Verbindung SSL/TLS ist.</span><span class="sxs-lookup"><span data-stu-id="a3d86-119">Lync Server 2013 external web services (deployed on the Front End Server and/or the Director) expect a connection from a reverse proxy on port TCP 4443, and it expects that the connection will be SSL/TLS.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="a3d86-120">Die empfohlenen Standard Überwachungsanschlüsse für die externen Webdienste sind TCP 8080 für HTTP-Datenverkehr und TCP 4443 für HTTPS-Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="a3d86-120">The suggested default listening ports for the external web services are TCP 8080 for HTTP traffic, and TCP 4443 for HTTPS traffic.</span></span> <span data-ttu-id="a3d86-121">Der Topologie-Generator bietet die Möglichkeit, die Standardeinstellungen zu überschreiben und ihre eigenen Überwachungsanschlüsse für die externen Webdienste zu definieren.</span><span class="sxs-lookup"><span data-stu-id="a3d86-121">Topology Builder provides an opportunity to override the defaults and define your own listening ports for the external web services.</span></span> <span data-ttu-id="a3d86-122">Beachten Sie, dass der Reverse-Proxy mit den externen Webdiensten kommuniziert und die externen Clients mit dem Reverse-Proxy kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="a3d86-122">It’s important to note that the reverse proxy communicates with the external web services, and the external clients communicate with the reverse proxy.</span></span> <span data-ttu-id="a3d86-123">Der externe Client kommuniziert mit dem Reverseproxy auf Port TCP 443, aber Sie können neu definieren, welchen Port der Reverse-Proxy mit den externen Webdiensten kommuniziert.</span><span class="sxs-lookup"><span data-stu-id="a3d86-123">The external client communicates with the reverse proxy on port TCP 443, but you can redefine what port the reverse proxy communicates with the external web services on.</span></span> <span data-ttu-id="a3d86-124">Mit den Optionen im Topologie-Generator können Sie die standardmäßigen Überwachungsanschlüsse für die Webdienste überschreiben, um die Überwachung von Port Konflikten zu beheben, die in Ihrer Infrastruktur auftreten können.</span><span class="sxs-lookup"><span data-stu-id="a3d86-124">The options in Topology Builder to override the default listening ports for the web services allows you to resolve listening port conflicts that may arise in your infrastructure.</span></span>

    
    </div>

3.  <span data-ttu-id="a3d86-125">Lync Server 2013-externe Webdienste erwarten einen unveränderten Host Header vom Client, um zu ermitteln, welches Dienst-und Webserververzeichnis der Client verwenden möchte.</span><span class="sxs-lookup"><span data-stu-id="a3d86-125">Lync Server 2013 external web services expect an unmodified Host Header from the client to identify what service and web server directory the client is attempting to use.</span></span> <span data-ttu-id="a3d86-126">Anforderungen sollten so aussehen, als ob Sie vom Reverse-Proxy stammen</span><span class="sxs-lookup"><span data-stu-id="a3d86-126">Requests should appear as if they came from the reverse proxy</span></span>

4.  <span data-ttu-id="a3d86-127">Die externen Webdienste verwenden definierte Webserver Virtual Directories (vDir), die die für Clients angebotenen Dienste bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a3d86-127">The external web services use defined web server virtual directories (vDir) that provide the services offered to clients.</span></span> <span data-ttu-id="a3d86-128">Bestimmte extern identifizierbare Webdienste sind:</span><span class="sxs-lookup"><span data-stu-id="a3d86-128">Specific externally identifiable web services are:</span></span>
    
      - <span data-ttu-id="a3d86-129">Die "Besprechung"-vDir für Webkonferenzbesprechungen</span><span class="sxs-lookup"><span data-stu-id="a3d86-129">The “Meet” vDir for web conference meetings</span></span>
    
      - <span data-ttu-id="a3d86-130">"Dialin"-vDir für Telefon-und Telefonkonferenzen</span><span class="sxs-lookup"><span data-stu-id="a3d86-130">The “Dialin” vDir for phone access and phone conferencing</span></span>
    
      - <span data-ttu-id="a3d86-131">Der "Auto Ermittlungs-vDir" für die lync Windows Store-App, lync Mobile und den Desktop Client lync 2013.</span><span class="sxs-lookup"><span data-stu-id="a3d86-131">The “Autodiscover” vDir for Lync Windows Store app, Lync Mobile, and the desktop client Lync 2013.</span></span> <span data-ttu-id="a3d86-132">Die AutoErmittlung in lync Server 2013 ist unter dem DNS-Namen "lyncdiscover" bekannt.</span><span class="sxs-lookup"><span data-stu-id="a3d86-132">Autodiscover in Lync Server 2013 is known by the DNS name “lyncdiscover”</span></span>
    
      - <span data-ttu-id="a3d86-133">Auf Dienste, die nicht definiert sind, wird vom externen Client durch direkte Anrufe an die externen Webdienste zugegriffen.</span><span class="sxs-lookup"><span data-stu-id="a3d86-133">Services not defined are accessed by the external client by direct calls to the external web services.</span></span> <span data-ttu-id="a3d86-134">So können Sie beispielsweisedurch direkte Anrufe an externe Webdienste und zugeordnete vDirs auf die Expansion von Verteilergruppen (dlx) und den Adressbuchdienst (ABS) zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a3d86-134">For example, distribution group expansion (DLX) and the address book service (ABS) are accessed by direct calls to the external web services and associated vDirs.</span></span> <span data-ttu-id="a3d86-135">Der Client kennt den tatsächlichen Pfad zum vDir und erstellt basierend auf diesen Informationen einen Uniform Record Locator (URL).</span><span class="sxs-lookup"><span data-stu-id="a3d86-135">The client knows the actual path to the vDir and constructs a uniform record locator (URL) based on this information.</span></span> <span data-ttu-id="a3d86-136">Der Clientzugriff auf den Adressbuchdienst mit einer URL ähnlich wie `https://externalweb.contoso.com/abs/handler`</span><span class="sxs-lookup"><span data-stu-id="a3d86-136">The client would access the address book service using a URL similar to `https://externalweb.contoso.com/abs/handler`</span></span>
    
      - <span data-ttu-id="a3d86-137">Der Office Web Apps-Server, wenn Konferenzen als Teil der lync Server-Topologie definiert und konfiguriert sind</span><span class="sxs-lookup"><span data-stu-id="a3d86-137">The Office Web Apps Server when conferencing is defined and configured as part of the Lync Server topology</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="a3d86-138">Der Office Web Apps-Server ist ein separater Rollen Server und nicht als Teil der externen Webdienste konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="a3d86-138">The Office Web Apps Server is a separate role server and is not configured as part of the external web services.</span></span> <span data-ttu-id="a3d86-139">Dieser Server wird separat für den Clientzugriff veröffentlicht.</span><span class="sxs-lookup"><span data-stu-id="a3d86-139">This server is separately published for client access.</span></span>

        
        </div>

5.  <span data-ttu-id="a3d86-140">Definieren Sie SSL-Bridging für jeden Dienst.</span><span class="sxs-lookup"><span data-stu-id="a3d86-140">Define SSL bridging for each service.</span></span> <span data-ttu-id="a3d86-141">Der externe Port TCP 443 wird dem external Web Services-Port von TCP 4443 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a3d86-141">The external port TCP 443 is mapped to the external web services port of TCP 4443.</span></span> <span data-ttu-id="a3d86-142">Für unverschlüsselte http wird Port TCP 80 dem externen Webdienste-Port TCP 8080 zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="a3d86-142">For unencrypted HTTP, port TCP 80 is mapped to the external web services port TCP 8080</span></span>

6.  <span data-ttu-id="a3d86-143">Planen von Reverse Proxy-Listenern zum Veröffentlichen von Webserverressourcen</span><span class="sxs-lookup"><span data-stu-id="a3d86-143">Plan for reverse proxy listeners to publish web server resources</span></span>

7.  <span data-ttu-id="a3d86-144">Sie können das Zertifikat für den Reverse-Proxy basierend auf den angebotenen Diensten anfordern und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a3d86-144">Request and configure the certificate for the reverse proxy based on the services that will be offered.</span></span> <span data-ttu-id="a3d86-145">Wenn dieses Zertifikat mit dem richtigen Alternativen Betreff-Namen konfiguriert wurde, kann es von allen konfigurierten Listener auf dem Reverse-Proxy Server freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="a3d86-145">If configured with the correct subject alternative names, this certificate can be shared by all configured listeners on the reverse proxy server</span></span>

<span data-ttu-id="a3d86-146">Ressourcen, die für die Planung der Reverse-Proxybereitstellung verfügbar sind:</span><span class="sxs-lookup"><span data-stu-id="a3d86-146">Resources available for planning your reverse proxy deployment:</span></span>

  - [<span data-ttu-id="a3d86-147">Datenerfassung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3d86-147">Data collection in Lync Server 2013</span></span>](lync-server-2013-data-collection.md)

  - [<span data-ttu-id="a3d86-148">Zertifikatzusammenfassung für Reverseproxy in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3d86-148">Certificate summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-reverse-proxy.md)

  - [<span data-ttu-id="a3d86-149">Portzusammenfassung für Reverseproxy in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3d86-149">Port summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-port-summary-reverse-proxy.md)

  - [<span data-ttu-id="a3d86-150">DNS-Zusammenfassung für Reverseproxy in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a3d86-150">DNS summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-dns-summary-reverse-proxy.md)

<span data-ttu-id="a3d86-151"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a3d86-151"></div>

<span> </span>

</div>

</div>

</span></span></div>

