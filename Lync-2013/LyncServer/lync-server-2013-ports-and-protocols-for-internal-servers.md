---
title: 'Lync Server 2013: Ports und Protokolle für interne Server'
description: 'Lync Server 2013: Ports und Protokolle für interne Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Ports and protocols for internal servers
ms:assetid: c94063f1-e802-4a61-be90-022fc185335e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398833(v=OCS.15)
ms:contentKeyID: 48185402
ms.date: 04/06/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d7d8f12c78c5dec5caacaeb1156f4d228b7cd591
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424247"
---
# <a name="ports-and-protocols-for-internal-servers-in-lync-server-2013"></a><span data-ttu-id="b8154-103">Ports und Protokolle für interne Server in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8154-103">Ports and protocols for internal servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b8154-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b8154-104">

<span> </span></span></span>

<span data-ttu-id="b8154-105">_**Letztes Änderungsdatum des Themas:** 2016-04-06_</span><span class="sxs-lookup"><span data-stu-id="b8154-105">_**Topic Last Modified:** 2016-04-06_</span></span>

<span data-ttu-id="b8154-106">In diesem Abschnitt werden die Ports und Protokolle zusammengefasst, die von Servern, Load-Balancern und Clients in einer lync Server-Bereitstellung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="b8154-106">This section summarizes the ports and protocols used by servers, load balancers, and clients in a Lync Server deployment.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b8154-107">Lync-und Communicator-Clients werden, wenn Sie an einer 1:1-Kommunikation beteiligt sind, häufig als Peer-to-Peer bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="b8154-107">Lync and Communicator clients when involved in a one to one communication, is often referred to as peer-to-peer.</span></span> <span data-ttu-id="b8154-108">Technisch gesehen kommunizieren die beiden Clients in einer 1:1-Konversation mit der Instant Messaging-Multipoint-Steuereinheit (IMMCU) in der Mitte.</span><span class="sxs-lookup"><span data-stu-id="b8154-108">Technically, the two clients are communicating in a one to one conversation, with the Instant Messaging multipoint control unit (IMMCU) in the middle.</span></span> <span data-ttu-id="b8154-109">Die IMMCU ist eine Komponente des Front-End-Servers.</span><span class="sxs-lookup"><span data-stu-id="b8154-109">The IMMCU is a component of Front End Server.</span></span> <span data-ttu-id="b8154-110">Wenn Sie den IMMCU in den erforderlichen Kommunikations Workflow einfügen, können Sie die Anrufdetailaufzeichnung und andere Features, die der Front-End-Server ermöglicht, aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="b8154-110">Placing the IMMCU in the required communication workflow allows call detail recording and other features that the Front End Server enables.</span></span> <span data-ttu-id="b8154-111">Die Kommunikation erfolgt von einem dynamischen Quell Port auf dem Client zum Front-End-Serverport TLS/TCP/5061 (unter der Voraussetzung, dass die empfohlene Transportschichtsicherheit verwendet wird).</span><span class="sxs-lookup"><span data-stu-id="b8154-111">Communication is from a dynamic source port on the client to the Front End Server port TLS/TCP/5061 (assuming the use of the recommended transport layer security).</span></span> <span data-ttu-id="b8154-112">Die Peer-to-Peer-Kommunikation (ebenso wie die Chat Unterhaltung mit mehreren Teilnehmern) ist im Entwurf nur möglich, wenn lync Server und IMMCU aktiv und verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="b8154-112">By design, peer-to-peer communication (as well as multi-party IM) is possible only when Lync Server and the IMMCU is active and available.</span></span>



</div>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="b8154-113">Port- und Protokolldetails</span><span class="sxs-lookup"><span data-stu-id="b8154-113">Port and Protocol Details</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b8154-114">Die Windows-Firewall muss ausgeführt werden, bevor Sie die lync Server-Dienste auf einem Server starten, weil dies der Fall ist, wenn lync Server die erforderlichen Ports in der Firewall öffnet.</span><span class="sxs-lookup"><span data-stu-id="b8154-114">Windows Firewall must be running before you start the Lync Server services on a server, because that is when Lync Server opens the required ports in the firewall.</span></span>



</div>

<span data-ttu-id="b8154-115">Details zur Firewall-Konfiguration für Edge-Komponenten finden Sie unter [ermitteln externer A/V-Firewall-und Portanforderungen für lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="b8154-115">For details about firewall configuration for edge components, see [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span></span>

<span data-ttu-id="b8154-116">In der folgenden Tabelle werden alle Ports aufgeführt, die auf jeder internen Serverrolle geöffnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b8154-116">The following table lists the ports that need to be open on each internal server role.</span></span>

### <a name="required-server-ports-by-server-role"></a><span data-ttu-id="b8154-117">Erforderliche Serverports (nach Serverrolle)</span><span class="sxs-lookup"><span data-stu-id="b8154-117">Required Server Ports (by Server Role)</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8154-118">Serverrolle</span><span class="sxs-lookup"><span data-stu-id="b8154-118">Server role</span></span></th>
<th><span data-ttu-id="b8154-119">Name des Diensts</span><span class="sxs-lookup"><span data-stu-id="b8154-119">Service name</span></span></th>
<th><span data-ttu-id="b8154-120">Port</span><span class="sxs-lookup"><span data-stu-id="b8154-120">Port</span></span></th>
<th><span data-ttu-id="b8154-121">Protokoll</span><span class="sxs-lookup"><span data-stu-id="b8154-121">Protocol</span></span></th>
<th><span data-ttu-id="b8154-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b8154-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8154-123">Alle Server</span><span class="sxs-lookup"><span data-stu-id="b8154-123">All Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-124">SQL-Browser</span><span class="sxs-lookup"><span data-stu-id="b8154-124">SQL Browser</span></span></p></td>
<td><p><span data-ttu-id="b8154-125">1434</span><span class="sxs-lookup"><span data-stu-id="b8154-125">1434</span></span></p></td>
<td><p><span data-ttu-id="b8154-126">UDP</span><span class="sxs-lookup"><span data-stu-id="b8154-126">UDP</span></span></p></td>
<td><p><span data-ttu-id="b8154-127">SQL-Browser für die lokale replizierte Kopie der Datenbank des zentralen Verwaltungsspeichers.</span><span class="sxs-lookup"><span data-stu-id="b8154-127">SQL Browser for the local replicated copy of the Central Management Store database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-128">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-128">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-129">Lync Server-Front-End Dienst</span><span class="sxs-lookup"><span data-stu-id="b8154-129">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b8154-130">5060</span><span class="sxs-lookup"><span data-stu-id="b8154-130">5060</span></span></p></td>
<td><p><span data-ttu-id="b8154-131">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-131">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-132">Wird optional von Standard Edition- und Front-End-Servern für statische Routen zu vertrauenswürdigen Diensten wie z. B. Servern für die Remoteanrufsteuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-132">Optionally used by Standard Edition servers and Front End Servers for static routes to trusted services, such as remote call control servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-133">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-133">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-134">Lync Server-Front-End Dienst</span><span class="sxs-lookup"><span data-stu-id="b8154-134">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b8154-135">5061</span><span class="sxs-lookup"><span data-stu-id="b8154-135">5061</span></span></p></td>
<td><p><span data-ttu-id="b8154-136">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-136">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b8154-137">Wird von Standard Edition-Servern und Front-End-Pools für die gesamte interne SIP-Kommunikation zwischen Servern (MTLS), für die SIP-Kommunikation zwischen Server und Client (TLS) und für die SIP-Kommunikation zwischen Front-End- und Vermittlungsservern (MTLS) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-137">Used by Standard Edition servers and Front End pools for all internal SIP communications between servers (MTLS), for SIP communications between Server and Client (TLS) and for SIP communications between Front End Servers and Mediation Servers (MTLS).</span></span> <span data-ttu-id="b8154-138">Wird auch für die Kommunikation mit Monitoring Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-138">Also used for communications with Monitoring Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-139">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-139">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-140">Lync Server-Front-End Dienst</span><span class="sxs-lookup"><span data-stu-id="b8154-140">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b8154-141">444</span><span class="sxs-lookup"><span data-stu-id="b8154-141">444</span></span></p></td>
<td><p><span data-ttu-id="b8154-142">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b8154-142">HTTPS</span></span></p>
<p><span data-ttu-id="b8154-143">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-143">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-144">Wird für die HTTPS-Kommunikation zwischen dem Fokus (der lync-Server Komponente, die den Konferenzstatus verwaltet) und den einzelnen Servern verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-144">Used for HTTPS communication between the Focus (the Lync Server component that manages conference state) and the individual servers.</span></span></p>
<p><span data-ttu-id="b8154-145">Dieser Port wird auch für die TCP-Kommunikation zwischen Überlebenden Branch-Appliances und Front-End-Servern verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-145">This port is also used for TCP communication between Survivable Branch Appliances and Front End Servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-146">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-146">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-147">Lync Server-Front-End Dienst</span><span class="sxs-lookup"><span data-stu-id="b8154-147">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b8154-148">135</span><span class="sxs-lookup"><span data-stu-id="b8154-148">135</span></span></p></td>
<td><p><span data-ttu-id="b8154-149">DCOM und Remoteprozeduraufruf (RPC)</span><span class="sxs-lookup"><span data-stu-id="b8154-149">DCOM and remote procedure call (RPC)</span></span></p></td>
<td><p><span data-ttu-id="b8154-150">Wird für DCOM-basierte Vorgänge wie z. B. das Verschieben von Benutzern, die Synchronisierung des Benutzerreplikationsdiensts und die Synchronisierung von Adressbüchern verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-150">Used for DCOM based operations such as Moving Users, User Replicator Synchronization, and Address Book Synchronization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-151">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-151">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-152">Lync Server im-Konferenzdienst</span><span class="sxs-lookup"><span data-stu-id="b8154-152">Lync Server IM Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="b8154-153">5062</span><span class="sxs-lookup"><span data-stu-id="b8154-153">5062</span></span></p></td>
<td><p><span data-ttu-id="b8154-154">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-154">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-155">Wird für eingehende SIP-Anforderungen für Instant Messaging-Konferenzen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-155">Used for incoming SIP requests for instant messaging (IM) conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-156">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-156">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-157">Lync Server-Webkonferenzdienst</span><span class="sxs-lookup"><span data-stu-id="b8154-157">Lync Server Web Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="b8154-158">8057</span><span class="sxs-lookup"><span data-stu-id="b8154-158">8057</span></span></p></td>
<td><p><span data-ttu-id="b8154-159">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-159">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b8154-160">Wird zum Überwachen von PSOM-Verbindungen (Persistent Shared Object Model) vom Client verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-160">Used to listen for Persistent Shared Object Model (PSOM) connections from client.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-161">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-161">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-162">Lync Server-Webkonferenz-Kompatibilitätsdienst</span><span class="sxs-lookup"><span data-stu-id="b8154-162">Lync Server Web Conferencing Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="b8154-163">8058</span><span class="sxs-lookup"><span data-stu-id="b8154-163">8058</span></span></p></td>
<td><p><span data-ttu-id="b8154-164">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-164">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b8154-165">Wird verwendet, um auf Persistent Shared Object Model (PSOM)-Verbindungen vom Live Meeting-Client und früheren Versionen von lync Server zu lauschen.</span><span class="sxs-lookup"><span data-stu-id="b8154-165">Used to listen for Persistent Shared Object Model (PSOM) connections from the Live Meeting client and previous versions of Lync Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-166">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-166">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-167">Lync Server-Audio/Video Konferenzdienst</span><span class="sxs-lookup"><span data-stu-id="b8154-167">Lync Server Audio/Video Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="b8154-168">5063</span><span class="sxs-lookup"><span data-stu-id="b8154-168">5063</span></span></p></td>
<td><p><span data-ttu-id="b8154-169">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-169">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-170">Wird für eingehende SIP-Anforderungen für A/V-Konferenzen (Audio/Video) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-170">Used for incoming SIP requests for audio/video (A/V) conferencing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-171">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-171">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-172">Lync Server-Audio/Video Konferenzdienst</span><span class="sxs-lookup"><span data-stu-id="b8154-172">Lync Server Audio/Video Conferencing service</span></span></p></td>
<td><p><span data-ttu-id="b8154-173">57501-65535</span><span class="sxs-lookup"><span data-stu-id="b8154-173">57501-65535</span></span></p></td>
<td><p><span data-ttu-id="b8154-174">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="b8154-174">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="b8154-175">Für Videokonferenzen verwendeter Medienportbereich.</span><span class="sxs-lookup"><span data-stu-id="b8154-175">Media port range used for video conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-176">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-176">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-177">Lync Server-webkompatibilitäts Dienst</span><span class="sxs-lookup"><span data-stu-id="b8154-177">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="b8154-178">80</span><span class="sxs-lookup"><span data-stu-id="b8154-178">80</span></span></p></td>
<td><p><span data-ttu-id="b8154-179">HTTP</span><span class="sxs-lookup"><span data-stu-id="b8154-179">HTTP</span></span></p></td>
<td><p><span data-ttu-id="b8154-180">Wird für die Kommunikation von den Front-End-Servern mit den FQDNs der Webfarm (von IIS-Webkomponenten genutzte URLs) verwendet, wenn kein HTTPS verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b8154-180">Used for communication from Front End Servers to the web farm FQDNs (the URLs used by IIS web components) when HTTPS is not used.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-181">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-181">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-182">Lync Server-webkompatibilitäts Dienst</span><span class="sxs-lookup"><span data-stu-id="b8154-182">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="b8154-183">443</span><span class="sxs-lookup"><span data-stu-id="b8154-183">443</span></span></p></td>
<td><p><span data-ttu-id="b8154-184">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b8154-184">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="b8154-185">Wird für die Kommunikation von den Front-End-Servern mit den FQDNs der Webfarm (von IIS-Webkomponenten genutzte URLs) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-185">Used for communication from Front End Servers to the web farm FQDNs (the URLs used by IIS web components).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-186">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-186">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-187">Lync Server-webkompatibilitäts Dienst</span><span class="sxs-lookup"><span data-stu-id="b8154-187">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="b8154-188">8080</span><span class="sxs-lookup"><span data-stu-id="b8154-188">8080</span></span></p></td>
<td><p><span data-ttu-id="b8154-189">TCP und HTTP</span><span class="sxs-lookup"><span data-stu-id="b8154-189">TCP and HTTP</span></span></p></td>
<td><p><span data-ttu-id="b8154-190">Wird von Webkomponenten für den externen Zugriff verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-190">Used by web components for external access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-191">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-191">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-192">Webserverkomponente</span><span class="sxs-lookup"><span data-stu-id="b8154-192">Web server component</span></span></p></td>
<td><p><span data-ttu-id="b8154-193">4443</span><span class="sxs-lookup"><span data-stu-id="b8154-193">4443</span></span></p></td>
<td><p><span data-ttu-id="b8154-194">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b8154-194">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="b8154-195">HTTPS (vom Reverseproxy) und HTTPS-Front-End-Kommunikation zwischen Servern für die AutoErmittlungsanmeldung.</span><span class="sxs-lookup"><span data-stu-id="b8154-195">HTTPS (from Reverse Proxy) and HTTPS Front End inter-pool communications for Autodiscover sign-in.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-196">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-196">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-197">Webserverkomponente</span><span class="sxs-lookup"><span data-stu-id="b8154-197">Web server component</span></span></p></td>
<td><p><span data-ttu-id="b8154-198">8060</span><span class="sxs-lookup"><span data-stu-id="b8154-198">8060</span></span></p></td>
<td><p><span data-ttu-id="b8154-199">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-199">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-200">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-200">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-201">Webserverkomponente</span><span class="sxs-lookup"><span data-stu-id="b8154-201">Web server component</span></span></p></td>
<td><p><span data-ttu-id="b8154-202">8061</span><span class="sxs-lookup"><span data-stu-id="b8154-202">8061</span></span></p></td>
<td><p><span data-ttu-id="b8154-203">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-203">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-204">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-204">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-205">Mobilitätsdienstekomponente</span><span class="sxs-lookup"><span data-stu-id="b8154-205">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="b8154-206">5086</span><span class="sxs-lookup"><span data-stu-id="b8154-206">5086</span></span></p></td>
<td><p><span data-ttu-id="b8154-207">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-207">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="b8154-208">Der von internen Prozessen der Mobilitätsdienste verwendete SIP-Port</span><span class="sxs-lookup"><span data-stu-id="b8154-208">SIP port used by Mobility Services internal processes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-209">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-209">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-210">Mobilitätsdienstekomponente</span><span class="sxs-lookup"><span data-stu-id="b8154-210">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="b8154-211">5087</span><span class="sxs-lookup"><span data-stu-id="b8154-211">5087</span></span></p></td>
<td><p><span data-ttu-id="b8154-212">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-212">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="b8154-213">Der von internen Prozessen der Mobilitätsdienste verwendete SIP-Port</span><span class="sxs-lookup"><span data-stu-id="b8154-213">SIP port used by Mobility Services internal processes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-214">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-214">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-215">Mobilitätsdienstekomponente</span><span class="sxs-lookup"><span data-stu-id="b8154-215">Mobility Services component</span></span></p></td>
<td><p><span data-ttu-id="b8154-216">443</span><span class="sxs-lookup"><span data-stu-id="b8154-216">443</span></span></p></td>
<td><p><span data-ttu-id="b8154-217">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b8154-217">HTTPS</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-218">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-218">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-219">Lync Server Conferencing Attendant-Dienst (Einwahlkonferenzen)</span><span class="sxs-lookup"><span data-stu-id="b8154-219">Lync Server Conferencing Attendant service (dial-in conferencing)</span></span></p></td>
<td><p><span data-ttu-id="b8154-220">5064</span><span class="sxs-lookup"><span data-stu-id="b8154-220">5064</span></span></p></td>
<td><p><span data-ttu-id="b8154-221">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-221">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-222">Wird für eingehende SIP-Anforderungen für Einwahlkonferenzen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-222">Used for incoming SIP requests for dial-in conferencing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-223">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-223">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-224">Lync Server Conferencing Attendant-Dienst (Einwahlkonferenzen)</span><span class="sxs-lookup"><span data-stu-id="b8154-224">Lync Server Conferencing Attendant service (dial-in conferencing)</span></span></p></td>
<td><p><span data-ttu-id="b8154-225">5072</span><span class="sxs-lookup"><span data-stu-id="b8154-225">5072</span></span></p></td>
<td><p><span data-ttu-id="b8154-226">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-226">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-227">Wird für eingehende SIP-Anforderungen für Attendant (Dial in Conferencing) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-227">Used for incoming SIP requests for Attendant (dial in conferencing).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-228">Front-End-Server, auf denen auch ein verbundener Vermittlungsserver ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="b8154-228">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="b8154-229">Lync Server-Vermittlungsdienst</span><span class="sxs-lookup"><span data-stu-id="b8154-229">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b8154-230">5070</span><span class="sxs-lookup"><span data-stu-id="b8154-230">5070</span></span></p></td>
<td><p><span data-ttu-id="b8154-231">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-231">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-232">Wird vom Vermittlungsserver für eingehende Anforderungen vom Front-End-Server an den Vermittlungsserver verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-232">Used by the Mediation Server for incoming requests from the Front End Server to the Mediation Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-233">Front-End-Server, auf denen auch ein verbundener Vermittlungsserver ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="b8154-233">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="b8154-234">Lync Server-Vermittlungsdienst</span><span class="sxs-lookup"><span data-stu-id="b8154-234">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b8154-235">5067</span><span class="sxs-lookup"><span data-stu-id="b8154-235">5067</span></span></p></td>
<td><p><span data-ttu-id="b8154-236">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-236">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b8154-237">Wird für eingehende SIP-Anforderungen vom PSTN-Gateway an den Vermittlungsserver verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-237">Used for incoming SIP requests from the PSTN gateway to the Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-238">Front-End-Server, auf denen auch ein verbundener Vermittlungsserver ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="b8154-238">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="b8154-239">Lync Server-Vermittlungsdienst</span><span class="sxs-lookup"><span data-stu-id="b8154-239">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b8154-240">5068</span><span class="sxs-lookup"><span data-stu-id="b8154-240">5068</span></span></p></td>
<td><p><span data-ttu-id="b8154-241">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-241">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-242">Wird für eingehende SIP-Anforderungen vom PSTN-Gateway an den Vermittlungsserver verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-242">Used for incoming SIP requests from the PSTN gateway to the Mediation Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-243">Front-End-Server, auf denen auch ein verbundener Vermittlungsserver ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="b8154-243">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="b8154-244">Lync Server-Vermittlungsdienst</span><span class="sxs-lookup"><span data-stu-id="b8154-244">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b8154-245">5081</span><span class="sxs-lookup"><span data-stu-id="b8154-245">5081</span></span></p></td>
<td><p><span data-ttu-id="b8154-246">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-246">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-247">Wird für ausgehende SIP-Anforderungen vom Vermittlungsserver an das PSTN-Gateway verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-247">Used for outgoing SIP requests from the Mediation Server to the PSTN gateway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-248">Front-End-Server, auf denen auch ein verbundener Vermittlungsserver ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="b8154-248">Front End Servers that also run a Collocated Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="b8154-249">Lync Server-Vermittlungsdienst</span><span class="sxs-lookup"><span data-stu-id="b8154-249">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b8154-250">5082</span><span class="sxs-lookup"><span data-stu-id="b8154-250">5082</span></span></p></td>
<td><p><span data-ttu-id="b8154-251">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-251">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b8154-252">Wird für ausgehende SIP-Anforderungen vom Vermittlungsserver an das PSTN-Gateway verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-252">Used for outgoing SIP requests from the Mediation Server to the PSTN gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-253">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-253">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-254">Lync Server-Anwendungsfreigabe Dienst</span><span class="sxs-lookup"><span data-stu-id="b8154-254">Lync Server Application Sharing service</span></span></p></td>
<td><p><span data-ttu-id="b8154-255">5065</span><span class="sxs-lookup"><span data-stu-id="b8154-255">5065</span></span></p></td>
<td><p><span data-ttu-id="b8154-256">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-256">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-257">Wird für eingehende SIP-Überwachungsanforderungen für die Anwendungsfreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-257">Used for incoming SIP listening requests for application sharing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-258">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-258">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-259">Lync Server-Anwendungsfreigabe Dienst</span><span class="sxs-lookup"><span data-stu-id="b8154-259">Lync Server Application Sharing service</span></span></p></td>
<td><p><span data-ttu-id="b8154-260">49152-65535</span><span class="sxs-lookup"><span data-stu-id="b8154-260">49152-65535</span></span></p></td>
<td><p><span data-ttu-id="b8154-261">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-261">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-262">Für die Anwendungsfreigabe verwendeter Medienportbereich.</span><span class="sxs-lookup"><span data-stu-id="b8154-262">Media port range used for application sharing.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-263">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-263">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-264">Ankündigungsdienst für lync Server-Konferenzen</span><span class="sxs-lookup"><span data-stu-id="b8154-264">Lync Server Conferencing Announcement service</span></span></p></td>
<td><p><span data-ttu-id="b8154-265">5073</span><span class="sxs-lookup"><span data-stu-id="b8154-265">5073</span></span></p></td>
<td><p><span data-ttu-id="b8154-266">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-266">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-267">Wird für eingehende SIP-Anforderungen für den lync Server Conferencing-Ankündigungsdienst (also für Einwahlkonferenzen) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-267">Used for incoming SIP requests for the Lync Server Conferencing Announcement service (that is, for dial-in conferencing).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-268">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-268">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-269">Lync Server-Dienst zum Parken von Anrufen</span><span class="sxs-lookup"><span data-stu-id="b8154-269">Lync Server Call Park service</span></span></p></td>
<td><p><span data-ttu-id="b8154-270">5075</span><span class="sxs-lookup"><span data-stu-id="b8154-270">5075</span></span></p></td>
<td><p><span data-ttu-id="b8154-271">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-271">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-272">Wird für eingehende SIP-Anforderungen für die Anwendung zum Parken von Anrufen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-272">Used for incoming SIP requests for the Call Park application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-273">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-273">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-274">Lync Server-audiotestdienst</span><span class="sxs-lookup"><span data-stu-id="b8154-274">Lync Server Audio Test service</span></span></p></td>
<td><p><span data-ttu-id="b8154-275">5076</span><span class="sxs-lookup"><span data-stu-id="b8154-275">5076</span></span></p></td>
<td><p><span data-ttu-id="b8154-276">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-276">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-277">Wird für eingehende SIP-Anforderungen für den Audiotestdienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-277">Used for incoming SIP requests for the Audio Test service.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-278">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-278">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-279">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="b8154-279">Not applicable</span></span></p></td>
<td><p><span data-ttu-id="b8154-280">5066</span><span class="sxs-lookup"><span data-stu-id="b8154-280">5066</span></span></p></td>
<td><p><span data-ttu-id="b8154-281">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-281">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-282">Wird für das ausgehende E9-1-1-Gateway (9-1-1 [erweitert]) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-282">Used for outbound Enhanced 9-1-1 (E9-1-1) gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-283">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-283">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-284">Lync Server-Reaktionsgruppendienst</span><span class="sxs-lookup"><span data-stu-id="b8154-284">Lync Server Response Group service</span></span></p></td>
<td><p><span data-ttu-id="b8154-285">5071</span><span class="sxs-lookup"><span data-stu-id="b8154-285">5071</span></span></p></td>
<td><p><span data-ttu-id="b8154-286">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-286">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-287">Wird für eingehende SIP-Anforderungen für die Reaktionsgruppenanwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-287">Used for incoming SIP requests for the Response Group application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-288">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-288">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-289">Lync Server-Reaktionsgruppendienst</span><span class="sxs-lookup"><span data-stu-id="b8154-289">Lync Server Response Group service</span></span></p></td>
<td><p><span data-ttu-id="b8154-290">8404</span><span class="sxs-lookup"><span data-stu-id="b8154-290">8404</span></span></p></td>
<td><p><span data-ttu-id="b8154-291">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-291">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="b8154-292">Wird für eingehende SIP-Anforderungen für die Reaktionsgruppenanwendung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-292">Used for incoming SIP requests for the Response Group application.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-293">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-293">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-294">Lync Server-bandbreitenrichtliniendienst</span><span class="sxs-lookup"><span data-stu-id="b8154-294">Lync Server Bandwidth Policy Service</span></span></p></td>
<td><p><span data-ttu-id="b8154-295">5080</span><span class="sxs-lookup"><span data-stu-id="b8154-295">5080</span></span></p></td>
<td><p><span data-ttu-id="b8154-296">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-296">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-297">Wird für die Anrufsteuerung durch den Bandbreitenrichtliniendienst für TURN-Datenverkehr vom A/V-Edgeserver verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-297">Used for call admission control by the Bandwidth Policy service for A/V Edge TURN traffic.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-298">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-298">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-299">Lync Server-bandbreitenrichtliniendienst</span><span class="sxs-lookup"><span data-stu-id="b8154-299">Lync Server Bandwidth Policy Service</span></span></p></td>
<td><p><span data-ttu-id="b8154-300">448</span><span class="sxs-lookup"><span data-stu-id="b8154-300">448</span></span></p></td>
<td><p><span data-ttu-id="b8154-301">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-301">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-302">Wird für die Anrufsteuerung vom lync Server-bandbreitenrichtliniendienst verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-302">Used for call admission control by the Lync Server Bandwidth Policy Service.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-303">Front-End-Server, auf denen sich der zentrale Verwaltungsspeicher befindet</span><span class="sxs-lookup"><span data-stu-id="b8154-303">Front End Servers where the Central Management store resides</span></span></p></td>
<td><p><span data-ttu-id="b8154-304">Lync Server-Master-Replicator-Agent-Dienst</span><span class="sxs-lookup"><span data-stu-id="b8154-304">Lync Server Master Replicator Agent service</span></span></p></td>
<td><p><span data-ttu-id="b8154-305">445</span><span class="sxs-lookup"><span data-stu-id="b8154-305">445</span></span></p></td>
<td><p><span data-ttu-id="b8154-306">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-306">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-307">Wird verwendet, um Konfigurationsdaten aus dem zentralen Verwaltungsspeicher auf Server mit lync Server zu übertragen.</span><span class="sxs-lookup"><span data-stu-id="b8154-307">Used to push configuration data from the Central Management store to servers running Lync Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-308">Alle Server</span><span class="sxs-lookup"><span data-stu-id="b8154-308">All Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-309">SQL-Browser</span><span class="sxs-lookup"><span data-stu-id="b8154-309">SQL Browser</span></span></p></td>
<td><p><span data-ttu-id="b8154-310">1434</span><span class="sxs-lookup"><span data-stu-id="b8154-310">1434</span></span></p></td>
<td><p><span data-ttu-id="b8154-311">UDP</span><span class="sxs-lookup"><span data-stu-id="b8154-311">UDP</span></span></p></td>
<td><p><span data-ttu-id="b8154-312">SQL-Browser für lokale replizierte Kopie von Daten des zentralen Verwaltungsspeichers in einer lokalen SQL Server-Instanz</span><span class="sxs-lookup"><span data-stu-id="b8154-312">SQL Browser for local replicated copy of Central Management store data in local SQL Server instance</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-313">Alle internen Server</span><span class="sxs-lookup"><span data-stu-id="b8154-313">All internal servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-314">Verschiedene</span><span class="sxs-lookup"><span data-stu-id="b8154-314">Various</span></span></p></td>
<td><p><span data-ttu-id="b8154-315">49152-57500</span><span class="sxs-lookup"><span data-stu-id="b8154-315">49152-57500</span></span></p></td>
<td><p><span data-ttu-id="b8154-316">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="b8154-316">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="b8154-317">Für Audiokonferenzen auf allen internen Servern verwendeter Medienportbereich.</span><span class="sxs-lookup"><span data-stu-id="b8154-317">Media port range used for audio conferencing on all internal servers.</span></span> <span data-ttu-id="b8154-318">Wird von allen Servern verwendet, die Audio beenden: Front-End-Server (für den lync Server Conferencing Attendant-Dienst, lync Server Conferencing Announcement Service und lync Server-Audio/Video Konferenzdienst) und Vermittlungsserver.</span><span class="sxs-lookup"><span data-stu-id="b8154-318">Used by all servers that terminate audio: Front End Servers (for Lync Server Conferencing Attendant service, Lync Server Conferencing Announcement service, and Lync Server Audio/Video Conferencing service), and Mediation Server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-319">Office Web Apps-Server</span><span class="sxs-lookup"><span data-stu-id="b8154-319">Office Web Apps Servers</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b8154-320">443</span><span class="sxs-lookup"><span data-stu-id="b8154-320">443</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b8154-321">Wird von lync Server 2013 zum Herstellen einer Verbindung mit Office Web Apps Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-321">Used by Lync Server 2013 to connect to Office Web Apps Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-322">Directors</span><span class="sxs-lookup"><span data-stu-id="b8154-322">Directors</span></span></p></td>
<td><p><span data-ttu-id="b8154-323">Lync Server-Front-End Dienst</span><span class="sxs-lookup"><span data-stu-id="b8154-323">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b8154-324">5060</span><span class="sxs-lookup"><span data-stu-id="b8154-324">5060</span></span></p></td>
<td><p><span data-ttu-id="b8154-325">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-325">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-326">Wird optional für statische Routen zu vertrauenswürdigen Diensten wie z. B. Servern für die Remoteanrufsteuerung verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-326">Optionally used for static routes to trusted services, such as remote call control servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-327">Directors</span><span class="sxs-lookup"><span data-stu-id="b8154-327">Directors</span></span></p></td>
<td><p><span data-ttu-id="b8154-328">Lync Server-Front-End Dienst</span><span class="sxs-lookup"><span data-stu-id="b8154-328">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b8154-329">444</span><span class="sxs-lookup"><span data-stu-id="b8154-329">444</span></span></p></td>
<td><p><span data-ttu-id="b8154-330">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b8154-330">HTTPS</span></span></p>
<p><span data-ttu-id="b8154-331">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-331">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-332">Serverübergreifende Kommunikation zwischen Front-End und Director.</span><span class="sxs-lookup"><span data-stu-id="b8154-332">Inter-server communication between Front End and Director.</span></span> <span data-ttu-id="b8154-333">Darüber hinaus veröffentlichen Clientzertifikate (auf Front-End-Servern) oder überprüfen, ob das Clientzertifikat bereits veröffentlicht wurde.</span><span class="sxs-lookup"><span data-stu-id="b8154-333">Additionally, client certificate publish (to Front End Servers) or validate if the client certificate has already been published.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-334">Directors</span><span class="sxs-lookup"><span data-stu-id="b8154-334">Directors</span></span></p></td>
<td><p><span data-ttu-id="b8154-335">Lync Server-webkompatibilitäts Dienst</span><span class="sxs-lookup"><span data-stu-id="b8154-335">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="b8154-336">80</span><span class="sxs-lookup"><span data-stu-id="b8154-336">80</span></span></p></td>
<td><p><span data-ttu-id="b8154-337">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-337">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-p105">Wird für die anfängliche Kommunikation von Directors zu den FQDNs der Webfarm (den von den IIS-Webkomponenten genutzten URLs) verwendet. Im Normalbetrieb wird auf HTTPS-Datenverkehr mit Port 443 und Protokolltyp TCP umgeschaltet.</span><span class="sxs-lookup"><span data-stu-id="b8154-p105">Used for initial communication from Directors to the web farm FQDNs (the URLs used by IIS web components). In normal operation, will switch to HTTPS traffic, using port 443 and protocol type TCP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-340">Directors</span><span class="sxs-lookup"><span data-stu-id="b8154-340">Directors</span></span></p></td>
<td><p><span data-ttu-id="b8154-341">Lync Server-webkompatibilitäts Dienst</span><span class="sxs-lookup"><span data-stu-id="b8154-341">Lync Server Web Compatibility service</span></span></p></td>
<td><p><span data-ttu-id="b8154-342">443</span><span class="sxs-lookup"><span data-stu-id="b8154-342">443</span></span></p></td>
<td><p><span data-ttu-id="b8154-343">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b8154-343">HTTPS</span></span></p></td>
<td><p><span data-ttu-id="b8154-344">Wird für die Kommunikation von Directors zu den FQDNs der Webfarm (den von den IIS-Webkomponenten genutzten URLs) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-344">Used for communication from Directors to the web farm FQDNs (the URLs used by IIS web components).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-345">Directors</span><span class="sxs-lookup"><span data-stu-id="b8154-345">Directors</span></span></p></td>
<td><p><span data-ttu-id="b8154-346">Lync Server-Front-End Dienst</span><span class="sxs-lookup"><span data-stu-id="b8154-346">Lync Server Front-End service</span></span></p></td>
<td><p><span data-ttu-id="b8154-347">5061</span><span class="sxs-lookup"><span data-stu-id="b8154-347">5061</span></span></p></td>
<td><p><span data-ttu-id="b8154-348">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-348">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-349">Wird für die interne Kommunikation zwischen Servern und für Clientverbindungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-349">Used for internal communications between servers and for client connections.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-350">Vermittlungsserver</span><span class="sxs-lookup"><span data-stu-id="b8154-350">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-351">Lync Server-Vermittlungsdienst</span><span class="sxs-lookup"><span data-stu-id="b8154-351">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b8154-352">5070</span><span class="sxs-lookup"><span data-stu-id="b8154-352">5070</span></span></p></td>
<td><p><span data-ttu-id="b8154-353">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-353">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-354">Wird vom Vermittlungsserver für eingehende Anforderungen vom Front-End-Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-354">Used by the Mediation Server for incoming requests from the Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-355">Vermittlungsserver</span><span class="sxs-lookup"><span data-stu-id="b8154-355">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-356">Lync Server-Vermittlungsdienst</span><span class="sxs-lookup"><span data-stu-id="b8154-356">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b8154-357">5067</span><span class="sxs-lookup"><span data-stu-id="b8154-357">5067</span></span></p></td>
<td><p><span data-ttu-id="b8154-358">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-358">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b8154-359">Wird für eingehende SIP-Anforderungen vom PSTN-Gateway verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-359">Used for incoming SIP requests from the PSTN gateway.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-360">Vermittlungsserver</span><span class="sxs-lookup"><span data-stu-id="b8154-360">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-361">Lync Server-Vermittlungsdienst</span><span class="sxs-lookup"><span data-stu-id="b8154-361">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b8154-362">5068</span><span class="sxs-lookup"><span data-stu-id="b8154-362">5068</span></span></p></td>
<td><p><span data-ttu-id="b8154-363">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-363">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-364">Wird für eingehende SIP-Anforderungen vom PSTN-Gateway verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-364">Used for incoming SIP requests from the PSTN gateway.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-365">Vermittlungsserver</span><span class="sxs-lookup"><span data-stu-id="b8154-365">Mediation Servers</span></span></p></td>
<td><p><span data-ttu-id="b8154-366">Lync Server-Vermittlungsdienst</span><span class="sxs-lookup"><span data-stu-id="b8154-366">Lync Server Mediation service</span></span></p></td>
<td><p><span data-ttu-id="b8154-367">5070</span><span class="sxs-lookup"><span data-stu-id="b8154-367">5070</span></span></p></td>
<td><p><span data-ttu-id="b8154-368">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-368">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="b8154-369">Wird für SIP-Anforderungen von den Front-End-Servern verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-369">Used for SIP requests from the Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-370">Front-End-Server für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="b8154-370">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="b8154-371">SIP für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="b8154-371">Persistent Chat SIP</span></span></p></td>
<td><p><span data-ttu-id="b8154-372">5041</span><span class="sxs-lookup"><span data-stu-id="b8154-372">5041</span></span></p></td>
<td><p><span data-ttu-id="b8154-373">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-373">TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-374">Front-End-Server für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="b8154-374">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="b8154-375">Windows Communication Foundation (WCF) für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="b8154-375">Persistent Chat Windows Communication Foundation (WCF)</span></span></p></td>
<td><p><span data-ttu-id="b8154-376">881</span><span class="sxs-lookup"><span data-stu-id="b8154-376">881</span></span></p></td>
<td><p><span data-ttu-id="b8154-377">TCP (TLS) und TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-377">TCP (TLS) and TCP (MTLS)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-378">Front-End-Server für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="b8154-378">Persistent Chat Front End Server</span></span></p></td>
<td><p><span data-ttu-id="b8154-379">Dateiübertragungsdienst für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="b8154-379">Persistent Chat File Transfer Service</span></span></p></td>
<td><p><span data-ttu-id="b8154-380">443</span><span class="sxs-lookup"><span data-stu-id="b8154-380">443</span></span></p></td>
<td><p><span data-ttu-id="b8154-381">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-381">TCP (TLS)</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="b8154-382">In einigen Szenarien mit Remoteanrufsteuerung ist eine TCP-Verbindung zwischen dem Front-End-Server oder dem Director und der Nebenstellenanlage erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b8154-382">Some remote call control scenarios require a TCP connection between the Front End Server or Director and the PBX.</span></span> <span data-ttu-id="b8154-383">Obwohl der TCP-Port 5060 von lync Server nicht mehr verwendet wird, erstellen Sie während der Remoteanrufsteuerung eine vertrauenswürdige Serverkonfiguration, die den FQDN des RCC-Leitungs Servers dem TCP-Port zuordnet, den der Front-End-Server oder Director für die Verbindung mit dem PBX-System verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-383">Although Lync Server no longer uses TCP port 5060, during remote call control deployment you create a trusted server configuration, which associates the RCC Line Server FQDN with the TCP port that the Front End Server or Director will use to connect to the PBX system.</span></span> <span data-ttu-id="b8154-384">Ausführliche Informationen finden Sie im <STRONG>CsTrustedApplicationComputer</STRONG> -Cmdlet in der Dokumentation zur lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="b8154-384">For details, see the <STRONG>CsTrustedApplicationComputer</STRONG> cmdlet in the Lync Server Management Shell documentation.</span></span>



</div>

<span data-ttu-id="b8154-385">Für Pools, in denen nur Hardwaregeräte zum Lastenausgleich (kein DNS-Lastenausgleich) verwendet werden, zeigen die folgenden Tabellen die Ports, die für die Hardwaregeräte zum Lastenausgleich geöffnet werden müssen.</span><span class="sxs-lookup"><span data-stu-id="b8154-385">For your pools that use only hardware load balancing (not DNS load balancing), the following table shows the ports that need to open the hardware load balancers.</span></span>

### <a name="hardware-load-balancer-ports-if-using-only-hardware-load-balancing"></a><span data-ttu-id="b8154-386">Ports für Hardwaregeräte zum Lastenausgleich, wenn nur ein Hardwarelastenausgleich verwendet wird</span><span class="sxs-lookup"><span data-stu-id="b8154-386">Hardware Load Balancer Ports if Using Only Hardware Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8154-387">Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-387">Load Balancer</span></span></th>
<th><span data-ttu-id="b8154-388">Port</span><span class="sxs-lookup"><span data-stu-id="b8154-388">Port</span></span></th>
<th><span data-ttu-id="b8154-389">Protokoll</span><span class="sxs-lookup"><span data-stu-id="b8154-389">Protocol</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8154-390">Front-End-Server-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-390">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-391">5061</span><span class="sxs-lookup"><span data-stu-id="b8154-391">5061</span></span></p></td>
<td><p><span data-ttu-id="b8154-392">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-392">TCP (TLS)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-393">Front-End-Server-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-393">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-394">444</span><span class="sxs-lookup"><span data-stu-id="b8154-394">444</span></span></p></td>
<td><p><span data-ttu-id="b8154-395">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b8154-395">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-396">Front-End-Server-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-396">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-397">135</span><span class="sxs-lookup"><span data-stu-id="b8154-397">135</span></span></p></td>
<td><p><span data-ttu-id="b8154-398">DCOM und Remoteprozeduraufruf (RPC)</span><span class="sxs-lookup"><span data-stu-id="b8154-398">DCOM and remote procedure call (RPC)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-399">Front-End-Server-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-399">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-400">80</span><span class="sxs-lookup"><span data-stu-id="b8154-400">80</span></span></p></td>
<td><p><span data-ttu-id="b8154-401">HTTP</span><span class="sxs-lookup"><span data-stu-id="b8154-401">HTTP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-402">Front-End-Server-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-402">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-403">8080</span><span class="sxs-lookup"><span data-stu-id="b8154-403">8080</span></span></p></td>
<td><p><span data-ttu-id="b8154-404">TCP – Abruf des Stammzertifikats für Clients und Geräte über den Front-End-Server – NTLM-Authentifizierung der Clients und Geräte</span><span class="sxs-lookup"><span data-stu-id="b8154-404">TCP - Client and device retrieval of root certificate from Front End Server – clients and devices authenticated by NTLM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-405">Front-End-Server-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-405">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-406">443</span><span class="sxs-lookup"><span data-stu-id="b8154-406">443</span></span></p></td>
<td><p><span data-ttu-id="b8154-407">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b8154-407">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-408">Front-End-Server-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-408">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-409">4443</span><span class="sxs-lookup"><span data-stu-id="b8154-409">4443</span></span></p></td>
<td><p><span data-ttu-id="b8154-410">HTTPS (vom Reverseproxy)</span><span class="sxs-lookup"><span data-stu-id="b8154-410">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-411">Front-End-Server-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-411">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-412">5072</span><span class="sxs-lookup"><span data-stu-id="b8154-412">5072</span></span></p></td>
<td><p><span data-ttu-id="b8154-413">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-413">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-414">Front-End-Server-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-414">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-415">5073</span><span class="sxs-lookup"><span data-stu-id="b8154-415">5073</span></span></p></td>
<td><p><span data-ttu-id="b8154-416">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-416">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-417">Front-End-Server-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-417">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-418">5075</span><span class="sxs-lookup"><span data-stu-id="b8154-418">5075</span></span></p></td>
<td><p><span data-ttu-id="b8154-419">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-419">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-420">Front-End-Server-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-420">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-421">5076</span><span class="sxs-lookup"><span data-stu-id="b8154-421">5076</span></span></p></td>
<td><p><span data-ttu-id="b8154-422">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-422">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-423">Front-End-Server-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-423">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-424">5071</span><span class="sxs-lookup"><span data-stu-id="b8154-424">5071</span></span></p></td>
<td><p><span data-ttu-id="b8154-425">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-425">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-426">Front-End-Server-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-426">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-427">5080</span><span class="sxs-lookup"><span data-stu-id="b8154-427">5080</span></span></p></td>
<td><p><span data-ttu-id="b8154-428">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-428">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-429">Front-End-Server-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-429">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-430">448</span><span class="sxs-lookup"><span data-stu-id="b8154-430">448</span></span></p></td>
<td><p><span data-ttu-id="b8154-431">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-431">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-432">Vermittlungsserver-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-432">Mediation Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-433">5070</span><span class="sxs-lookup"><span data-stu-id="b8154-433">5070</span></span></p></td>
<td><p><span data-ttu-id="b8154-434">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-434">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-435">Front-End-Server-Lastenausgleichssystem (wenn im Pool auch ein Vermittlungsserver ausgeführt wird)</span><span class="sxs-lookup"><span data-stu-id="b8154-435">Front End Server load balancer (if the pool also runs Mediation Server)</span></span></p></td>
<td><p><span data-ttu-id="b8154-436">5070</span><span class="sxs-lookup"><span data-stu-id="b8154-436">5070</span></span></p></td>
<td><p><span data-ttu-id="b8154-437">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-437">TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-438">Director-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-438">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-439">443</span><span class="sxs-lookup"><span data-stu-id="b8154-439">443</span></span></p></td>
<td><p><span data-ttu-id="b8154-440">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b8154-440">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-441">Director-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-441">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-442">444</span><span class="sxs-lookup"><span data-stu-id="b8154-442">444</span></span></p></td>
<td><p><span data-ttu-id="b8154-443">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b8154-443">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-444">Director-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-444">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-445">5061</span><span class="sxs-lookup"><span data-stu-id="b8154-445">5061</span></span></p></td>
<td><p><span data-ttu-id="b8154-446">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-446">TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-447">Director-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-447">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-448">4443</span><span class="sxs-lookup"><span data-stu-id="b8154-448">4443</span></span></p></td>
<td><p><span data-ttu-id="b8154-449">HTTPS (vom Reverseproxy)</span><span class="sxs-lookup"><span data-stu-id="b8154-449">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b8154-p107">Für die Front-End- und Director-Pools, die DNS-Lastenausgleich verwenden, muss auch ein Hardwaregerät zum Lastenausgleich bereitgestellt werden. In der folgenden Tabelle werden die Ports aufgeführt, die auf diesen Hardwaregeräten geöffnet sein müssen.</span><span class="sxs-lookup"><span data-stu-id="b8154-p107">Your Front End pools and Director pools that use DNS load balancing also must have a hardware load balancer deployed. The following table shows the ports that need to be open on these hardware load balancers.</span></span>

### <a name="hardware-load-balancer-ports-if-using-dns-load-balancing"></a><span data-ttu-id="b8154-452">Ports für Hardwaregeräte zum Lastenausgleich, wenn DNS-Lastenausgleich verwendet wird</span><span class="sxs-lookup"><span data-stu-id="b8154-452">Hardware Load Balancer Ports if Using DNS Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8154-453">Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-453">Load Balancer</span></span></th>
<th><span data-ttu-id="b8154-454">Port</span><span class="sxs-lookup"><span data-stu-id="b8154-454">Port</span></span></th>
<th><span data-ttu-id="b8154-455">Protokoll</span><span class="sxs-lookup"><span data-stu-id="b8154-455">Protocol</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8154-456">Front-End-Server-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-456">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-457">80</span><span class="sxs-lookup"><span data-stu-id="b8154-457">80</span></span></p></td>
<td><p><span data-ttu-id="b8154-458">HTTP</span><span class="sxs-lookup"><span data-stu-id="b8154-458">HTTP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-459">Front-End-Server-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-459">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-460">443</span><span class="sxs-lookup"><span data-stu-id="b8154-460">443</span></span></p></td>
<td><p><span data-ttu-id="b8154-461">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b8154-461">HTTPS</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-462">Front-End-Server-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-462">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-463">8080</span><span class="sxs-lookup"><span data-stu-id="b8154-463">8080</span></span></p></td>
<td><p><span data-ttu-id="b8154-464">TCP – Abruf des Stammzertifikats für Clients und Geräte über den Front-End-Server – NTLM-Authentifizierung der Clients und Geräte</span><span class="sxs-lookup"><span data-stu-id="b8154-464">TCP - Client and device retrieval of root certificate from Front End Server – clients and devices authenticated by NTLM</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-465">Front-End-Server-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-465">Front End Server load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-466">4443</span><span class="sxs-lookup"><span data-stu-id="b8154-466">4443</span></span></p></td>
<td><p><span data-ttu-id="b8154-467">HTTPS (vom Reverseproxy)</span><span class="sxs-lookup"><span data-stu-id="b8154-467">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-468">Director-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-468">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-469">443</span><span class="sxs-lookup"><span data-stu-id="b8154-469">443</span></span></p></td>
<td><p><span data-ttu-id="b8154-470">HTTPS</span><span class="sxs-lookup"><span data-stu-id="b8154-470">HTTPS</span></span></p></td>
</tr>
<tr class="even">
<td> </td>
<td> </td>
<td> </td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-471">Director-Lastenausgleichssystem</span><span class="sxs-lookup"><span data-stu-id="b8154-471">Director load balancer</span></span></p></td>
<td><p><span data-ttu-id="b8154-472">4443</span><span class="sxs-lookup"><span data-stu-id="b8154-472">4443</span></span></p></td>
<td><p><span data-ttu-id="b8154-473">HTTPS (vom Reverseproxy)</span><span class="sxs-lookup"><span data-stu-id="b8154-473">HTTPS (from reverse proxy)</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="required-client-ports"></a><span data-ttu-id="b8154-474">Erforderliche Clientports</span><span class="sxs-lookup"><span data-stu-id="b8154-474">Required Client Ports</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8154-475">Komponente</span><span class="sxs-lookup"><span data-stu-id="b8154-475">Component</span></span></th>
<th><span data-ttu-id="b8154-476">Port</span><span class="sxs-lookup"><span data-stu-id="b8154-476">Port</span></span></th>
<th><span data-ttu-id="b8154-477">Protokoll</span><span class="sxs-lookup"><span data-stu-id="b8154-477">Protocol</span></span></th>
<th><span data-ttu-id="b8154-478">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b8154-478">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8154-479">Clients</span><span class="sxs-lookup"><span data-stu-id="b8154-479">Clients</span></span></p></td>
<td><p><span data-ttu-id="b8154-480">67/68</span><span class="sxs-lookup"><span data-stu-id="b8154-480">67/68</span></span></p></td>
<td><p><span data-ttu-id="b8154-481">DHCP</span><span class="sxs-lookup"><span data-stu-id="b8154-481">DHCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-482">Wird von lync Server verwendet, um den FQDN der Registrierungsstelle zu finden (das heißt, wenn DNS SRV fehlschlägt und manuelle Einstellungen nicht konfiguriert sind).</span><span class="sxs-lookup"><span data-stu-id="b8154-482">Used by Lync Server to find the Registrar FQDN (that is, if DNS SRV fails and manual settings are not configured).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-483">Clients</span><span class="sxs-lookup"><span data-stu-id="b8154-483">Clients</span></span></p></td>
<td><p><span data-ttu-id="b8154-484">443</span><span class="sxs-lookup"><span data-stu-id="b8154-484">443</span></span></p></td>
<td><p><span data-ttu-id="b8154-485">TCP (TLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-485">TCP (TLS)</span></span></p></td>
<td><p><span data-ttu-id="b8154-486">Wird bei externem Benutzerzugriff für SIP-Datenverkehr vom Client zum Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-486">Used for client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-487">Clients</span><span class="sxs-lookup"><span data-stu-id="b8154-487">Clients</span></span></p></td>
<td><p><span data-ttu-id="b8154-488">443</span><span class="sxs-lookup"><span data-stu-id="b8154-488">443</span></span></p></td>
<td><p><span data-ttu-id="b8154-489">TCP (PSOM/TLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-489">TCP (PSOM/TLS)</span></span></p></td>
<td><p><span data-ttu-id="b8154-490">Wird für externen Benutzerzugriff auf Webkonferenzsitzungen verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-490">Used for external user access to web conferencing sessions.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-491">Clients</span><span class="sxs-lookup"><span data-stu-id="b8154-491">Clients</span></span></p></td>
<td><p><span data-ttu-id="b8154-492">443</span><span class="sxs-lookup"><span data-stu-id="b8154-492">443</span></span></p></td>
<td><p><span data-ttu-id="b8154-493">TCP (STUN/MSTURN)</span><span class="sxs-lookup"><span data-stu-id="b8154-493">TCP (STUN/MSTURN)</span></span></p></td>
<td><p><span data-ttu-id="b8154-494">Wird für externen Benutzerzugriff auf A/V-Sitzungen und -Mediendaten verwendet (TCP).</span><span class="sxs-lookup"><span data-stu-id="b8154-494">Used for external user access to A/V sessions and media (TCP)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-495">Clients</span><span class="sxs-lookup"><span data-stu-id="b8154-495">Clients</span></span></p></td>
<td><p><span data-ttu-id="b8154-496">3478</span><span class="sxs-lookup"><span data-stu-id="b8154-496">3478</span></span></p></td>
<td><p><span data-ttu-id="b8154-497">UDP (STUN/MSTURN)</span><span class="sxs-lookup"><span data-stu-id="b8154-497">UDP (STUN/MSTURN)</span></span></p></td>
<td><p><span data-ttu-id="b8154-498">Wird für externen Benutzerzugriff auf A/V-Sitzungen und -Mediendaten verwendet (UDP).</span><span class="sxs-lookup"><span data-stu-id="b8154-498">Used for external user access to A/V sessions and media (UDP)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-499">Clients</span><span class="sxs-lookup"><span data-stu-id="b8154-499">Clients</span></span></p></td>
<td><p><span data-ttu-id="b8154-500">5061</span><span class="sxs-lookup"><span data-stu-id="b8154-500">5061</span></span></p></td>
<td><p><span data-ttu-id="b8154-501">TCP (MTLS)</span><span class="sxs-lookup"><span data-stu-id="b8154-501">TCP (MTLS)</span></span></p></td>
<td><p><span data-ttu-id="b8154-502">Wird bei externem Benutzerzugriff für SIP-Datenverkehr vom Client zum Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-502">Used for client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-503">Clients</span><span class="sxs-lookup"><span data-stu-id="b8154-503">Clients</span></span></p></td>
<td><p><span data-ttu-id="b8154-504">6891-6901</span><span class="sxs-lookup"><span data-stu-id="b8154-504">6891-6901</span></span></p></td>
<td><p><span data-ttu-id="b8154-505">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-505">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-506">Wird für die Dateiübertragung zwischen lync-Clients und vorherigen Clients (Clients von Microsoft Office Communications Server 2007 R2, Microsoft Office Communications Server 2007 und Live Communications Server 2005) verwendet.</span><span class="sxs-lookup"><span data-stu-id="b8154-506">Used for file transfer between Lync clients and previous clients (clients of Microsoft Office Communications Server 2007 R2, Microsoft Office Communications Server 2007, and Live Communications Server 2005).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-507">Clients</span><span class="sxs-lookup"><span data-stu-id="b8154-507">Clients</span></span></p></td>
<td><p><span data-ttu-id="b8154-508">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="b8154-508">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="b8154-509">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="b8154-509">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="b8154-510">Audioportbereich (mindestens 20 Ports erforderlich).</span><span class="sxs-lookup"><span data-stu-id="b8154-510">Audio port range (minimum of 20 ports required)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-511">Clients</span><span class="sxs-lookup"><span data-stu-id="b8154-511">Clients</span></span></p></td>
<td><p><span data-ttu-id="b8154-512">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="b8154-512">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="b8154-513">TCP/UDP</span><span class="sxs-lookup"><span data-stu-id="b8154-513">TCP/UDP</span></span></p></td>
<td><p><span data-ttu-id="b8154-514">Videoportbereich (mindestens 20 Ports erforderlich).</span><span class="sxs-lookup"><span data-stu-id="b8154-514">Video port range (minimum of 20 ports required).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-515">Clients</span><span class="sxs-lookup"><span data-stu-id="b8154-515">Clients</span></span></p></td>
<td><p><span data-ttu-id="b8154-516">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="b8154-516">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="b8154-517">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-517">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-518">Peer-zu-Peer-Dateiübertragungen (zur Übertragung von Konferenzdateien verwenden Clients PSOM-Verbindungen).</span><span class="sxs-lookup"><span data-stu-id="b8154-518">Peer-to-peer file transfer (for conferencing file transfer, clients use PSOM).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8154-519">Clients</span><span class="sxs-lookup"><span data-stu-id="b8154-519">Clients</span></span></p></td>
<td><p><span data-ttu-id="b8154-520">1024-65535 \*</span><span class="sxs-lookup"><span data-stu-id="b8154-520">1024-65535 \*</span></span></p></td>
<td><p><span data-ttu-id="b8154-521">TCP</span><span class="sxs-lookup"><span data-stu-id="b8154-521">TCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-522">Anwendungsfreigabe.</span><span class="sxs-lookup"><span data-stu-id="b8154-522">Application sharing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8154-523">Aastra 6721ip (Telefon für öffentliche Bereiche)</span><span class="sxs-lookup"><span data-stu-id="b8154-523">Aastra 6721ip common area phone</span></span></p>
<p><span data-ttu-id="b8154-524">Telefonapparat Aastra 6725ip</span><span class="sxs-lookup"><span data-stu-id="b8154-524">Aastra 6725ip desk phone</span></span></p>
<p><span data-ttu-id="b8154-525">IP-Telefon HP 4110 (Telefon für öffentliche Bereiche)</span><span class="sxs-lookup"><span data-stu-id="b8154-525">HP 4110 IP Phone (common area phone)</span></span></p>
<p><span data-ttu-id="b8154-526">IP-Telefon HP 4120 (Telefonapparat)</span><span class="sxs-lookup"><span data-stu-id="b8154-526">HP 4120 IP Phone (desk phone)</span></span></p>
<p><span data-ttu-id="b8154-527">IP-Telefon Polycom CX500 (Telefon für öffentliche Bereiche)</span><span class="sxs-lookup"><span data-stu-id="b8154-527">Polycom CX500 IP common area phone</span></span></p>
<p><span data-ttu-id="b8154-528">IP-Telefonapparat Polycom CX600</span><span class="sxs-lookup"><span data-stu-id="b8154-528">Polycom CX600 IP desk phone</span></span></p>
<p><span data-ttu-id="b8154-529">IP-Telefonapparat Polycom CX700</span><span class="sxs-lookup"><span data-stu-id="b8154-529">Polycom CX700 IP desk phone</span></span></p>
<p><span data-ttu-id="b8154-530">IP-Konferenztelefon Polycom CX3000</span><span class="sxs-lookup"><span data-stu-id="b8154-530">Polycom CX3000 IP conference phone</span></span></p></td>
<td><p><span data-ttu-id="b8154-531">67/68</span><span class="sxs-lookup"><span data-stu-id="b8154-531">67/68</span></span></p></td>
<td><p><span data-ttu-id="b8154-532">DHCP</span><span class="sxs-lookup"><span data-stu-id="b8154-532">DHCP</span></span></p></td>
<td><p><span data-ttu-id="b8154-533">Wird von den aufgelisteten Geräten verwendet, um das lync Server-Zertifikat, den Bereitstellungs-FQDN und den FQDN der Registrierungsstelle zu finden.</span><span class="sxs-lookup"><span data-stu-id="b8154-533">Used by the listed devices to find the Lync Server certificate, provisioning FQDN, and Registrar FQDN.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b8154-534">**\*** Wenn Sie bestimmte Ports für diese Medientypen konfigurieren möchten, verwenden Sie das CsConferencingConfiguration-Cmdlet (ClientMediaPortRangeEnabled-, ClientMediaPort-und ClientMediaPortRange-Parameter).</span><span class="sxs-lookup"><span data-stu-id="b8154-534">**\*** To configure specific ports for these media types, use the CsConferencingConfiguration cmdlet (ClientMediaPortRangeEnabled, ClientMediaPort, and ClientMediaPortRange parameters).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b8154-535">Mit den Einstellungen für lync-Clients werden die erforderlichen Ausnahmen für das Betriebssystem auf dem Clientcomputer automatisch erstellt.</span><span class="sxs-lookup"><span data-stu-id="b8154-535">The set programs for Lync clients automatically create the required operating-system firewall exceptions on the client computer.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="b8154-536">Die für den externen Benutzerzugriff verwendeten Ports werden für jedes Szenario benötigt, in dem der Client die Firewall der Organisation durchqueren muss (z. B. bei externer Kommunikation oder bei Besprechungen, die von anderen Organisationen gehostet werden).</span><span class="sxs-lookup"><span data-stu-id="b8154-536">The ports that are used for external user access are required for any scenario in which the client must traverse the organization’s firewall (for example, any external communications or meetings hosted by other organizations).</span></span>



<span data-ttu-id="b8154-537"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b8154-537"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

