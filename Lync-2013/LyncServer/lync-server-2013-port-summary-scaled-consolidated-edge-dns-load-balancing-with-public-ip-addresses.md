---
title: 'Lync Server 2013: Portzusammenfassung für einen skalierten konsolidierten Edgeserver, DNS-Lastenausgleich mit öffentlichen IP-Adressen'
description: 'Lync Server 2013: Port Zusammenfassung – skalierter konsolidierter Edge, DNS-Lastenausgleich mit öffentlichen IP-Adressen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge, DNS load balancing with public IP addresses
ms:assetid: f7cbd0f1-841d-4116-8d17-e9d991daa4a8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205394(v=OCS.15)
ms:contentKeyID: 48185865
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8090435485b4b6a183702a608b139cec91ae26a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446339"
---
# <a name="port-summary---scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="3b5ec-103">Portzusammenfassung für einen skalierten konsolidierten Edgeserver, DNS-Lastenausgleich mit öffentlichen IP-Adressen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3b5ec-103">Port summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3b5ec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3b5ec-104">

<span> </span></span></span>

<span data-ttu-id="3b5ec-105">_**Letztes Änderungsdatum des Themas:** 2013-04-03_</span><span class="sxs-lookup"><span data-stu-id="3b5ec-105">_**Topic Last Modified:** 2013-04-03_</span></span>

<span data-ttu-id="3b5ec-106">Die in dieser Szenario-Architektur beschriebene lync Server 2013-Edgeserver-Funktionalität ähnelt dem, was in lync Server 2010 implementiert wurde.</span><span class="sxs-lookup"><span data-stu-id="3b5ec-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="3b5ec-107">Die bemerkenswerteste Ergänzung ist der Port **5269 over TCP** -Eintrag für das Extensible Messaging and Presence Protocol (XMPP).</span><span class="sxs-lookup"><span data-stu-id="3b5ec-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="3b5ec-108">Lync Server 2013 stellt optional einen XMPP-Proxy auf dem Edge-Server oder Edge-Pool und dem XMPP-Gatewayserver auf dem Front-End-Server oder Front-End-Pool bereit.</span><span class="sxs-lookup"><span data-stu-id="3b5ec-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="3b5ec-109">Neben IPv4 unterstützt der Edgeserver nun IPv6.</span><span class="sxs-lookup"><span data-stu-id="3b5ec-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="3b5ec-110">Aus Gründen der Übersichtlichkeit wird in den Szenarien nur IPv4 verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b5ec-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="3b5ec-111">**Unternehmens Umkreisnetzwerk für skalierten konsolidierten Edge, DNS-Lastenausgleich mit öffentlichen IP-Adressen**</span><span class="sxs-lookup"><span data-stu-id="3b5ec-111">**Enterprise perimeter network for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses**</span></span>

<span data-ttu-id="3b5ec-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span><span class="sxs-lookup"><span data-stu-id="3b5ec-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="3b5ec-113">Port- und Protokolldetails</span><span class="sxs-lookup"><span data-stu-id="3b5ec-113">Port and Protocol Details</span></span>

<span data-ttu-id="3b5ec-114">Es wird empfohlen, nur die Ports zu öffnen, die erforderlich sind, um die Funktionalität zu unterstützen, für die Sie externen Zugriff bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="3b5ec-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="3b5ec-115">Damit der Remotezugriff für jeden Edgedienst funktionieren kann, ist es zwingend erforderlich, dass der SIP-Datenverkehr bidirektional wie in der Abbildung des eingehenden/ausgehenden Edge-Traffics durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="3b5ec-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="3b5ec-116">Anders ausgedrückt: das SIP-Messaging zum und vom Access-Edgedienst ist an Instant Messaging (im), Anwesenheitsinformationen, Webkonferenzen, Audio/Video (A/V) und Föderation beteiligt.</span><span class="sxs-lookup"><span data-stu-id="3b5ec-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="3b5ec-117">Zusammenfassung der Firewall für den konsolidierten skalierten Edge, DNS-Lastenausgleich mit öffentlichen IP-Adressen: externe Schnittstelle – Knoten 1 und Knoten 2 (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="3b5ec-117">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b5ec-118">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="3b5ec-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="3b5ec-119">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="3b5ec-119">Source IP address</span></span></th>
<th><span data-ttu-id="3b5ec-120">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="3b5ec-120">Destination IP address</span></span></th>
<th><span data-ttu-id="3b5ec-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3b5ec-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="3b5ec-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-123">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-123">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-124">XMPP-Proxy Dienst (Freigabe der IP-Adresse mit Access Edge Service)</span><span class="sxs-lookup"><span data-stu-id="3b5ec-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-125">Der XMPP-Proxy Dienst akzeptiert Datenverkehr von XMPP-Kontakten in definierten XMPP-Föderationen</span><span class="sxs-lookup"><span data-stu-id="3b5ec-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5ec-126">Access/http/TCP/80</span><span class="sxs-lookup"><span data-stu-id="3b5ec-126">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-127">Öffentliche IP-Adresse des Edge-Server-Zugriffs-Edge-Diensts</span><span class="sxs-lookup"><span data-stu-id="3b5ec-127">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-128">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-128">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-129">Zertifikatsperrung/CRL-Prüfung und-Abruf</span><span class="sxs-lookup"><span data-stu-id="3b5ec-129">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-130">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="3b5ec-130">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-131">Öffentliche IP-Adresse des Edge-Server-Zugriffs-Edge-Diensts</span><span class="sxs-lookup"><span data-stu-id="3b5ec-131">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-132">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-132">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-133">DNS-Abfrage über TCP</span><span class="sxs-lookup"><span data-stu-id="3b5ec-133">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5ec-134">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="3b5ec-134">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-135">Öffentliche IP-Adresse des Edge-Server-Zugriffs-Edge-Diensts</span><span class="sxs-lookup"><span data-stu-id="3b5ec-135">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-136">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-136">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-137">DNS-Abfrage über UDP</span><span class="sxs-lookup"><span data-stu-id="3b5ec-137">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-138">Access/SIP (TLS)-/TCP/443</span><span class="sxs-lookup"><span data-stu-id="3b5ec-138">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-139">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-139">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-140">Öffentliche IP-Adresse des Edge-Server-Zugriffs-Edge-Diensts</span><span class="sxs-lookup"><span data-stu-id="3b5ec-140">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-141">Client-zu-Server-SIP-Datenverkehr für den Zugriff durch externe Benutzer</span><span class="sxs-lookup"><span data-stu-id="3b5ec-141">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5ec-142">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="3b5ec-142">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-143">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-143">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-144">Öffentliche IP-Adresse des Edge-Server-Zugriffs-Edge-Diensts</span><span class="sxs-lookup"><span data-stu-id="3b5ec-144">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-145">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="3b5ec-145">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-146">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="3b5ec-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-147">Öffentliche IP-Adresse des Edge-Server-Zugriffs-Edge-Diensts</span><span class="sxs-lookup"><span data-stu-id="3b5ec-147">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-148">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-148">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-149">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="3b5ec-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5ec-150">Web Conferencing/PSOM (TLS) TCP/443</span><span class="sxs-lookup"><span data-stu-id="3b5ec-150">Web Conferencing/PSOM(TLS)TCP/443</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-151">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-151">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-152">Edge-Server-Webkonferenz-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="3b5ec-152">Edge Server Web Conferencing Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-153">Web-Konferenzmedien</span><span class="sxs-lookup"><span data-stu-id="3b5ec-153">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-154">A/V/RTP/TCP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="3b5ec-154">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-155">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="3b5ec-155">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-156">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-156">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-157">Erforderlich für die Föderation mit Partnern, die Office Communications Server 2007, Office Communications Server 2007 R2, lync Server 2010 und lync Server 2013 ausführen.</span><span class="sxs-lookup"><span data-stu-id="3b5ec-157">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5ec-158">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="3b5ec-158">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-159">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="3b5ec-159">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-160">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-160">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-161">Nur für den Verbund mit Partnern erforderlich, auf denen Office Communications Server 2007 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3b5ec-161">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-162">A/V/RTP/TCP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="3b5ec-162">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-163">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-163">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-164">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="3b5ec-164">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-165">Nur für den Verbund mit Partnern erforderlich, die Office Communications Server 2007 ausführen</span><span class="sxs-lookup"><span data-stu-id="3b5ec-165">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5ec-166">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="3b5ec-166">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-167">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-167">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-168">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="3b5ec-168">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-169">Nur für den Verbund mit Partnern erforderlich, die Office Communications Server 2007 ausführen</span><span class="sxs-lookup"><span data-stu-id="3b5ec-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-170">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="3b5ec-170">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-171">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="3b5ec-171">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-172">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-172">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-173">3478 Outbound wird verwendet, um die Version von Edgeserver zu ermitteln, mit der lync Server kommuniziert, sowie für Mediendatenverkehr vom Edge-Server-zu-Edge-Server.</span><span class="sxs-lookup"><span data-stu-id="3b5ec-173">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="3b5ec-174">Erforderlich für den Verbund mit lync Server 2010, Windows Live Messenger und Office Communications Server 2007 R2 und auch, wenn mehrere Edge-Pools in einem Unternehmen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3b5ec-174">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5ec-175">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="3b5ec-175">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-176">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-176">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-177">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="3b5ec-177">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-178">Betäubung/Turn Verhandlung von Kandidaten über UDP/3478</span><span class="sxs-lookup"><span data-stu-id="3b5ec-178">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-179">A/V/Stun, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="3b5ec-179">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-180">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-180">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-181">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="3b5ec-181">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-182">Betäubung/Turn Verhandlung von Kandidaten über TCP/443</span><span class="sxs-lookup"><span data-stu-id="3b5ec-182">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5ec-183">A/V/Stun, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="3b5ec-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-184">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="3b5ec-184">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-185">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-185">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-186">Betäubung/Turn Verhandlung von Kandidaten über TCP/443</span><span class="sxs-lookup"><span data-stu-id="3b5ec-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-internal-interface--node-1-and-node-2-example"></a><span data-ttu-id="3b5ec-187">Zusammenfassung der Firewall für den konsolidierten skalierten Edge, DNS-Lastenausgleich mit öffentlichen IP-Adressen: interne Schnittstelle – Knoten 1 und Knoten 2 (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="3b5ec-187">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses: Internal Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b5ec-188">Protokoll/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="3b5ec-188">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="3b5ec-189">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="3b5ec-189">Source IP address</span></span></th>
<th><span data-ttu-id="3b5ec-190">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="3b5ec-190">Destination IP address</span></span></th>
<th><span data-ttu-id="3b5ec-191">Kommentare</span><span class="sxs-lookup"><span data-stu-id="3b5ec-191">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-192">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="3b5ec-192">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-193">Any (kann als Front-End-Server Adresse oder IP-Adresse des Front-End-Pools definiert werden, auf der der XMPP-Gatewayserver ausgeführt wird)</span><span class="sxs-lookup"><span data-stu-id="3b5ec-193">Any (can be defined as Front End Server address, or Front End pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-194">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3b5ec-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-195">Ausgehender XMPP-Datenverkehr vom XMPP-Gatewayserver auf dem Front-End-Server oder Front-End-Pool</span><span class="sxs-lookup"><span data-stu-id="3b5ec-195">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5ec-196">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="3b5ec-196">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-197">Any (kann als Director, IP-Adresse des Director-Pools, Front-End-Server oder IP-Adresse des Front-End-Pools definiert werden)</span><span class="sxs-lookup"><span data-stu-id="3b5ec-197">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-198">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3b5ec-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-199">Ausgehender SIP-Datenverkehr (von Director, Director-Pool-IP-Adresse, Front-End-Server oder IP-Adresse des Front-End-Pools) zu einer internen Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3b5ec-199">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="3b5ec-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-201">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3b5ec-201">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-202">Any (kann als Director, IP-Adresse des Director-Pools, Front-End-Server oder IP-Adresse des Front-End-Pools definiert werden)</span><span class="sxs-lookup"><span data-stu-id="3b5ec-202">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-203">Eingehende SIP-Datenverkehr (an Director, IP-Adresse des Director-Pools, Front-End-Server oder IP-Adresse des Front-End-Pools) aus der internen Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3b5ec-203">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5ec-204">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="3b5ec-204">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-205">Any (kann als Front-End-Server-IP-Adresse oder jede IP-Adresse eines Front-End-Servers in einem Front-End-Pool definiert werden)</span><span class="sxs-lookup"><span data-stu-id="3b5ec-205">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-206">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3b5ec-206">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-207">Webkonferenzen-Datenverkehr vom Front-End-Server oder jedem Front-End-Server, falls in einem Pool, zu einer internen Schnittstelle des Edge-Servers</span><span class="sxs-lookup"><span data-stu-id="3b5ec-207">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-208">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="3b5ec-208">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-209">Any (kann als Front-End-Server-IP-Adresse oder IP-Adresse des Front-End-Pools oder einer überlebensfähigen Branch-Appliance oder eines Überlebenden Branch-Servers mit diesem Edgeserver definiert werden)</span><span class="sxs-lookup"><span data-stu-id="3b5ec-209">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-210">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3b5ec-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-211">Authentifizierung von a/v-Benutzern (a/v-Authentifizierungsdienst) vom Front-End-Server oder der IP-Adresse des Front-End-Pools oder von einer Überlebenden Branch-Appliance oder einem Überlebenden Branch-Server mit diesem Edgeserver</span><span class="sxs-lookup"><span data-stu-id="3b5ec-211">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5ec-212">Stun/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="3b5ec-212">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-213">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-213">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-214">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3b5ec-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-215">Bevorzugter Pfad für die A/V-Medienübertragung zwischen internen und externen Benutzern, Survivable Branch Appliance oder Survivable Branch Server</span><span class="sxs-lookup"><span data-stu-id="3b5ec-215">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-216">Stun/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="3b5ec-216">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-217">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-217">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-218">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3b5ec-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-219">Fall Back Pfad für die A/V-Medienübertragung zwischen internen und externen Benutzern, Survival-Branch-Appliance oder einem Überlebenden Branch-Server wenn die UDP-Kommunikation nicht hergestellt werden kann, wird TCP für Dateiübertragung und Desktopfreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="3b5ec-219">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5ec-220">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="3b5ec-220">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-221">Any (kann als die IP-Adresse des Front-End-Servers oder-Pools definiert werden, der den zentralen Verwaltungsspeicher enthält)</span><span class="sxs-lookup"><span data-stu-id="3b5ec-221">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-222">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3b5ec-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-223">Replikation von Änderungen vom zentralen Verwaltungsspeicher auf den Edgeserver</span><span class="sxs-lookup"><span data-stu-id="3b5ec-223">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-224">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="3b5ec-224">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-225">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-225">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-226">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3b5ec-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-227">Zentralisierter Protokollierungsdienst Controller mit lync Server-Verwaltungsshell und zentralen Protokolldienst-Cmdlets, Befehlszeilen-ClsController (ClsController.exe) oder Agent (ClsAgent.exe)-Befehlen und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="3b5ec-227">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5ec-228">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="3b5ec-228">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-229">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-229">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-230">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3b5ec-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-231">Zentralisierter Protokollierungsdienst Controller mit lync Server-Verwaltungsshell und zentralen Protokolldienst-Cmdlets, Befehlszeilen-ClsController (ClsController.exe) oder Agent (ClsAgent.exe)-Befehlen und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="3b5ec-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-232">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="3b5ec-232">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-233">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-233">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-234">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3b5ec-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-235">Zentralisierter Protokollierungsdienst Controller mit lync Server-Verwaltungsshell und zentralen Protokolldienst-Cmdlets, Befehlszeilen-ClsController (ClsController.exe) oder Agent (ClsAgent.exe)-Befehlen und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="3b5ec-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="3b5ec-236">Zusammenfassung der Firewall für den Verbund</span><span class="sxs-lookup"><span data-stu-id="3b5ec-236">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b5ec-237">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="3b5ec-237">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="3b5ec-238">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="3b5ec-238">Source IP address</span></span></th>
<th><span data-ttu-id="3b5ec-239">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="3b5ec-239">Destination IP address</span></span></th>
<th><span data-ttu-id="3b5ec-240">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3b5ec-240">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-241">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="3b5ec-241">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-242">Access Edge Service (öffentliche IP-Adresse)</span><span class="sxs-lookup"><span data-stu-id="3b5ec-242">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-243">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-243">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-244">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="3b5ec-244">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="3b5ec-245">Zusammenfassung der Firewall – öffentliche Instant Messaging-Konnektivität</span><span class="sxs-lookup"><span data-stu-id="3b5ec-245">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b5ec-246">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="3b5ec-246">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="3b5ec-247">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="3b5ec-247">Source IP address</span></span></th>
<th><span data-ttu-id="3b5ec-248">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="3b5ec-248">Destination IP address</span></span></th>
<th><span data-ttu-id="3b5ec-249">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3b5ec-249">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-250">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="3b5ec-250">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-251">Verbindungspartner für öffentliche Chats</span><span class="sxs-lookup"><span data-stu-id="3b5ec-251">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-252">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="3b5ec-252">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-253">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="3b5ec-253">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5ec-254">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="3b5ec-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-255">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="3b5ec-255">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-256">Verbindungspartner für öffentliche Chats</span><span class="sxs-lookup"><span data-stu-id="3b5ec-256">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-257">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="3b5ec-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-258">Access/SIP (TLS)-/TCP/443</span><span class="sxs-lookup"><span data-stu-id="3b5ec-258">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-259">Clients</span><span class="sxs-lookup"><span data-stu-id="3b5ec-259">Clients</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-260">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="3b5ec-260">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-261">Client-zu-Server-SIP-Datenverkehr für den Zugriff durch externe Benutzer</span><span class="sxs-lookup"><span data-stu-id="3b5ec-261">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5ec-262">A/V/RTP/TCP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="3b5ec-262">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-263">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="3b5ec-263">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-264">Live Messenger-Clients</span><span class="sxs-lookup"><span data-stu-id="3b5ec-264">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-265">Wird für A/V-Sitzungen mit Windows Live Messenger verwendet, wenn die Konnektivität für öffentliche Chats konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="3b5ec-265">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-266">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="3b5ec-266">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-267">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="3b5ec-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-268">Live Messenger-Clients</span><span class="sxs-lookup"><span data-stu-id="3b5ec-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-269">Erforderlich für öffentliche Chat Verbindungen mit Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="3b5ec-269">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5ec-270">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="3b5ec-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-271">Live Messenger-Clients</span><span class="sxs-lookup"><span data-stu-id="3b5ec-271">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-272">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="3b5ec-272">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-273">Erforderlich für öffentliche Chat Verbindungen mit Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="3b5ec-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="3b5ec-274">Zusammenfassung der Firewall für erweiterbares Messaging und Anwesenheits Protokoll</span><span class="sxs-lookup"><span data-stu-id="3b5ec-274">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b5ec-275">Protokoll/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="3b5ec-275">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="3b5ec-276">Quelle (IP-Adresse)</span><span class="sxs-lookup"><span data-stu-id="3b5ec-276">Source (IP address)</span></span></th>
<th><span data-ttu-id="3b5ec-277">Ziel (IP-Adresse)</span><span class="sxs-lookup"><span data-stu-id="3b5ec-277">Destination (IP address)</span></span></th>
<th><span data-ttu-id="3b5ec-278">Kommentare</span><span class="sxs-lookup"><span data-stu-id="3b5ec-278">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-279">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="3b5ec-279">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-280">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-280">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-281">IP-Adresse des Edge-Server-Access-Edge-Service-Interfaces</span><span class="sxs-lookup"><span data-stu-id="3b5ec-281">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-282">Standard mäßiger Server-zu-Server-Kommunikationsanschluss für XMPP.</span><span class="sxs-lookup"><span data-stu-id="3b5ec-282">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="3b5ec-283">Ermöglicht die Kommunikation mit dem Edge-Server-XMPP-Proxy von Federated XMPP-Partnern</span><span class="sxs-lookup"><span data-stu-id="3b5ec-283">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b5ec-284">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="3b5ec-284">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-285">IP-Adresse des Edge-Server-Access-Edge-Service-Interfaces</span><span class="sxs-lookup"><span data-stu-id="3b5ec-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-286">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-286">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-287">Standard mäßiger Server-zu-Server-Kommunikationsanschluss für XMPP.</span><span class="sxs-lookup"><span data-stu-id="3b5ec-287">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="3b5ec-288">Ermöglicht die Kommunikation vom Edge Server XMPP-Proxy an Federated XMPP-Partner</span><span class="sxs-lookup"><span data-stu-id="3b5ec-288">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b5ec-289">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="3b5ec-289">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-290">Beliebig</span><span class="sxs-lookup"><span data-stu-id="3b5ec-290">Any</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-291">Jede interne Edge-Server-Schnittstellen-IP</span><span class="sxs-lookup"><span data-stu-id="3b5ec-291">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="3b5ec-292">Interner XMPP-Datenverkehr vom XMPP-Gateway auf dem Front-End-Server oder Front-End-Pool zur internen IP-Adresse des Edge-Servers oder zur internen IP-Adresse jedes Edge-Pools</span><span class="sxs-lookup"><span data-stu-id="3b5ec-292">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3b5ec-293">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3b5ec-293">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

