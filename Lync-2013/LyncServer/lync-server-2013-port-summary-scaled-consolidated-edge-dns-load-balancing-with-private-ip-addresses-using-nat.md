---
title: 'Lync Server 2013: Portzusammenfassung für einen skalierten konsolidierten Edgeserver, DNS-Lastenausgleich mit privaten IP-Adressen und NAT'
description: 'Lync Server 2013: Port Zusammenfassung – skalierter konsolidierter Edge, DNS-Lastenausgleich mit privaten IP-Adressen mithilfe von NAT.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT
ms:assetid: a296c2af-54d4-4b4f-9795-9191baf688cb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412756(v=OCS.15)
ms:contentKeyID: 48184955
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e0402b6682e86e5edf263fca78dfbe0f8fa070b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424292"
---
# <a name="port-summary---scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="51950-103">Portzusammenfassung für einen skalierten konsolidierten Edgeserver, DNS-Lastenausgleich mit privaten IP-Adressen und NAT in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="51950-103">Port summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="51950-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="51950-104">

<span> </span></span></span>

<span data-ttu-id="51950-105">_**Letztes Änderungsdatum des Themas:** 2012-12-04_</span><span class="sxs-lookup"><span data-stu-id="51950-105">_**Topic Last Modified:** 2012-12-04_</span></span>

<span data-ttu-id="51950-106">Die in dieser Szenario-Architektur beschriebene lync Server 2013-Edgeserver-Funktionalität ähnelt dem, was in lync Server 2010 implementiert wurde.</span><span class="sxs-lookup"><span data-stu-id="51950-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="51950-107">Die bemerkenswerteste Ergänzung ist der Port **5269 over TCP** -Eintrag für das Extensible Messaging and Presence Protocol (XMPP).</span><span class="sxs-lookup"><span data-stu-id="51950-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="51950-108">Lync Server 2013 stellt optional einen XMPP-Proxy auf dem Edge-Server oder Edge-Pool und dem XMPP-Gatewayserver auf dem Front-End-Server oder Front-End-Pool bereit.</span><span class="sxs-lookup"><span data-stu-id="51950-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="51950-109">Neben IPv4 unterstützt der Edgeserver nun IPv6.</span><span class="sxs-lookup"><span data-stu-id="51950-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="51950-110">Aus Gründen der Übersichtlichkeit wird in den Szenarien nur IPv4 verwendet.</span><span class="sxs-lookup"><span data-stu-id="51950-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="51950-111">**Unternehmens Umkreisnetzwerk für skalierten konsolidierten Edge mit privaten IP-Adressen mithilfe von NAT**</span><span class="sxs-lookup"><span data-stu-id="51950-111">**Enterprise perimeter network for scaled consolidated edge with private IP addresses using NAT**</span></span>

<span data-ttu-id="51950-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span><span class="sxs-lookup"><span data-stu-id="51950-112">![96f5a8f5-16d2-464d-b86e-7c7ecfc89ead](images/JJ205394.96f5a8f5-16d2-464d-b86e-7c7ecfc89ead(OCS.15).jpg "96f5a8f5-16d2-464d-b86e-7c7ecfc89ead")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="51950-113">Port- und Protokolldetails</span><span class="sxs-lookup"><span data-stu-id="51950-113">Port and Protocol Details</span></span>

<span data-ttu-id="51950-114">Es wird empfohlen, nur die Ports zu öffnen, die erforderlich sind, um die Funktionalität zu unterstützen, für die Sie externen Zugriff bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="51950-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="51950-115">Damit der Remotezugriff für jeden Edgedienst funktionieren kann, ist es zwingend erforderlich, dass der SIP-Datenverkehr bidirektional wie in der Abbildung des eingehenden/ausgehenden Edge-Traffics durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="51950-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="51950-116">Anders ausgedrückt: das SIP-Messaging zum und vom Access-Edgedienst ist an Instant Messaging (im), Anwesenheitsinformationen, Webkonferenzen, Audio/Video (A/V) und Föderation beteiligt.</span><span class="sxs-lookup"><span data-stu-id="51950-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="51950-117">Zusammenfassung der Firewall für den konsolidierten skalierten Edge, DNS-Lastenausgleich mit privaten IP-Adressen mithilfe von NAT: externe Schnittstelle – Knoten 1 und Knoten 2 (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="51950-117">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Private IP Addresses Using NAT: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="51950-118">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="51950-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="51950-119">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="51950-119">Source IP address</span></span></th>
<th><span data-ttu-id="51950-120">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="51950-120">Destination IP address</span></span></th>
<th><span data-ttu-id="51950-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="51950-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51950-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="51950-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="51950-123">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-123">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-124">XMPP-Proxy Dienst (Freigabe der IP-Adresse mit Access Edge Service)</span><span class="sxs-lookup"><span data-stu-id="51950-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="51950-125">Der XMPP-Proxy Dienst akzeptiert Datenverkehr von XMPP-Kontakten in definierten XMPP-Föderationen</span><span class="sxs-lookup"><span data-stu-id="51950-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51950-126">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="51950-126">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="51950-127">XMPP-Proxy Dienst (Freigabe der IP-Adresse mit Access Edge Service)</span><span class="sxs-lookup"><span data-stu-id="51950-127">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="51950-128">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-128">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-129">Der XMPP-Proxy Dienst sendet Datenverkehr an XMPP-Kontakte in definierten XMPP-Föderationen</span><span class="sxs-lookup"><span data-stu-id="51950-129">XMPP Proxy service sends traffic to XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51950-130">Access/http/TCP/80</span><span class="sxs-lookup"><span data-stu-id="51950-130">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="51950-131">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-131">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-132">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-132">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-133">Zertifikatsperrung/CRL-Prüfung und-Abruf</span><span class="sxs-lookup"><span data-stu-id="51950-133">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51950-134">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="51950-134">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="51950-135">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-135">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-136">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-136">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-137">DNS-Abfrage über TCP</span><span class="sxs-lookup"><span data-stu-id="51950-137">DNS query over TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51950-138">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="51950-138">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="51950-139">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-139">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-140">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-140">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-141">DNS-Abfrage über UDP</span><span class="sxs-lookup"><span data-stu-id="51950-141">DNS query over UDP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51950-142">Access/SIP (TLS)-/TCP/443</span><span class="sxs-lookup"><span data-stu-id="51950-142">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="51950-143">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-143">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-144">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-144">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-145">Client-zu-Server-SIP-Datenverkehr für den Zugriff durch externe Benutzer</span><span class="sxs-lookup"><span data-stu-id="51950-145">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51950-146">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="51950-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="51950-147">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-147">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-148">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-148">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-149">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="51950-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51950-150">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="51950-150">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="51950-151">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-151">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-152">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-152">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-153">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="51950-153">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51950-154">Web Conferencing/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="51950-154">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="51950-155">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-155">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-156">Edge-Server-Webkonferenz-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-156">Edge Server Web Conferencing Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-157">Web-Konferenzmedien</span><span class="sxs-lookup"><span data-stu-id="51950-157">Web Conferencing media</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51950-158">A/V/RTP/TCP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="51950-158">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="51950-159">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-159">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-160">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-160">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-161">Erforderlich für die Föderation mit Partnern, die Office Communications Server 2007, Office Communications Server 2007 R2, lync Server 2010 und lync Server 2013 ausführen.</span><span class="sxs-lookup"><span data-stu-id="51950-161">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51950-162">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="51950-162">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="51950-163">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-163">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-164">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-164">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-165">Nur für den Verbund mit Partnern erforderlich, auf denen Office Communications Server 2007 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="51950-165">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51950-166">A/V/RTP/TCP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="51950-166">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="51950-167">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-167">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-168">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-168">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-169">Nur für den Verbund mit Partnern erforderlich, die Office Communications Server 2007 ausführen</span><span class="sxs-lookup"><span data-stu-id="51950-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51950-170">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="51950-170">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="51950-171">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-171">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-172">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-172">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-173">Nur für den Verbund mit Partnern erforderlich, die Office Communications Server 2007 ausführen</span><span class="sxs-lookup"><span data-stu-id="51950-173">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51950-174">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="51950-174">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="51950-175">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-175">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-176">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-176">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-177">3478 Outbound wird verwendet, um die Version von Edgeserver zu ermitteln, mit der lync Server kommuniziert, sowie für Mediendatenverkehr vom Edge-Server-zu-Edge-Server.</span><span class="sxs-lookup"><span data-stu-id="51950-177">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="51950-178">Erforderlich für den Verbund mit lync Server 2010, Windows Live Messenger und Office Communications Server 2007 R2 und auch, wenn mehrere Edge-Pools in einem Unternehmen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="51950-178">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51950-179">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="51950-179">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="51950-180">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-180">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-181">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-181">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-182">Betäubung/Turn Verhandlung von Kandidaten über UDP/3478</span><span class="sxs-lookup"><span data-stu-id="51950-182">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51950-183">A/V/Stun, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="51950-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="51950-184">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-184">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-185">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-185">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-186">Betäubung/Turn Verhandlung von Kandidaten über TCP/443</span><span class="sxs-lookup"><span data-stu-id="51950-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51950-187">A/V/Stun, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="51950-187">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="51950-188">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-188">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-189">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-189">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-190">Betäubung/Turn Verhandlung von Kandidaten über TCP/443</span><span class="sxs-lookup"><span data-stu-id="51950-190">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-internal-interface--node-1-and-node-2-example"></a><span data-ttu-id="51950-191">Zusammenfassung der Firewall für den konsolidierten skalierten Edge, DNS-Lastenausgleich mit privaten IP-Adressen mithilfe von NAT: interne Schnittstelle – Knoten 1 und Knoten 2 (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="51950-191">Firewall Summary for Scaled Consolidated Edge, DNS Load Balancing with Private IP Addresses Using NAT: Internal Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="51950-192">Protokoll/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="51950-192">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="51950-193">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="51950-193">Source IP address</span></span></th>
<th><span data-ttu-id="51950-194">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="51950-194">Destination IP address</span></span></th>
<th><span data-ttu-id="51950-195">Kommentare</span><span class="sxs-lookup"><span data-stu-id="51950-195">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51950-196">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="51950-196">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="51950-197">Any (kann als Front-End-Server Adresse oder IP-Adresse des Front-End-Pools definiert werden, auf der der XMPP-Gatewayserver ausgeführt wird)</span><span class="sxs-lookup"><span data-stu-id="51950-197">Any (can be defined as Front End Server address, or Front End pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="51950-198">IP-Adresse des Edge-Server-internen Interfaces</span><span class="sxs-lookup"><span data-stu-id="51950-198">Edge Server internal interface IP address</span></span></p></td>
<td><p><span data-ttu-id="51950-199">Ausgehender XMPP-Datenverkehr vom XMPP-Gatewayserver auf dem Front-End-Server oder Front-End-Pool</span><span class="sxs-lookup"><span data-stu-id="51950-199">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51950-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="51950-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="51950-201">Any (kann als Director, IP-Adresse des Director-Pools, Front-End-Server oder IP-Adresse des Front-End-Pools definiert werden)</span><span class="sxs-lookup"><span data-stu-id="51950-201">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="51950-202">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="51950-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="51950-203">Ausgehender SIP-Datenverkehr (von Director, Director-Pool-IP-Adresse, Front-End-Server oder IP-Adresse des Front-End-Pools) zu einer internen Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="51950-203">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51950-204">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="51950-204">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="51950-205">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="51950-205">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="51950-206">Any (kann als Director, IP-Adresse des Director-Pools, Front-End-Server oder IP-Adresse des Front-End-Pools definiert werden)</span><span class="sxs-lookup"><span data-stu-id="51950-206">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="51950-207">Eingehende SIP-Datenverkehr (an Director, IP-Adresse des Director-Pools, Front-End-Server oder IP-Adresse des Front-End-Pools) aus der internen Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="51950-207">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51950-208">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="51950-208">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="51950-209">Any (kann als Front-End-Server-IP-Adresse oder jede IP-Adresse eines Front-End-Servers in einem Front-End-Pool definiert werden)</span><span class="sxs-lookup"><span data-stu-id="51950-209">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="51950-210">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="51950-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="51950-211">Webkonferenzen-Datenverkehr vom Front-End-Server oder jedem Front-End-Server, falls in einem Pool, zu einer internen Schnittstelle des Edge-Servers</span><span class="sxs-lookup"><span data-stu-id="51950-211">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51950-212">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="51950-212">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="51950-213">Any (kann als Front-End-Server-IP-Adresse oder IP-Adresse des Front-End-Pools oder einer überlebensfähigen Branch-Appliance oder eines Überlebenden Branch-Servers mit diesem Edgeserver definiert werden)</span><span class="sxs-lookup"><span data-stu-id="51950-213">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="51950-214">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="51950-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="51950-215">Authentifizierung von a/v-Benutzern (a/v-Authentifizierungsdienst) vom Front-End-Server oder der IP-Adresse des Front-End-Pools oder von einer Überlebenden Branch-Appliance oder einem Überlebenden Branch-Server mit diesem Edgeserver</span><span class="sxs-lookup"><span data-stu-id="51950-215">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51950-216">Stun/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="51950-216">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="51950-217">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-217">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-218">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="51950-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="51950-219">Bevorzugter Pfad für die A/V-Medienübertragung zwischen internen und externen Benutzern, Survivable Branch Appliance oder Survivable Branch Server</span><span class="sxs-lookup"><span data-stu-id="51950-219">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51950-220">Stun/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="51950-220">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="51950-221">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-221">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-222">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="51950-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="51950-223">Fall Back Pfad für die A/V-Medienübertragung zwischen internen und externen Benutzern, Survival-Branch-Appliance oder einem Überlebenden Branch-Server wenn die UDP-Kommunikation nicht hergestellt werden kann, wird TCP für Dateiübertragung und Desktopfreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="51950-223">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51950-224">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="51950-224">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="51950-225">Any (kann als die IP-Adresse des Front-End-Servers oder-Pools definiert werden, der den zentralen Verwaltungsspeicher enthält)</span><span class="sxs-lookup"><span data-stu-id="51950-225">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="51950-226">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="51950-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="51950-227">Replikation von Änderungen vom zentralen Verwaltungsspeicher auf den Edgeserver</span><span class="sxs-lookup"><span data-stu-id="51950-227">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51950-228">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="51950-228">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="51950-229">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-229">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-230">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="51950-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="51950-231">Zentralisierter Protokollierungsdienst Controller mit lync Server-Verwaltungsshell und zentralen Protokolldienst-Cmdlets, Befehlszeilen-ClsController (ClsController.exe) oder Agent (ClsAgent.exe)-Befehlen und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="51950-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51950-232">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="51950-232">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="51950-233">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-233">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-234">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="51950-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="51950-235">Zentralisierter Protokollierungsdienst Controller mit lync Server-Verwaltungsshell und zentralen Protokolldienst-Cmdlets, Befehlszeilen-ClsController (ClsController.exe) oder Agent (ClsAgent.exe)-Befehlen und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="51950-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51950-236">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="51950-236">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="51950-237">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-237">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-238">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="51950-238">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="51950-239">Zentralisierter Protokollierungsdienst Controller mit lync Server-Verwaltungsshell und zentralen Protokolldienst-Cmdlets, Befehlszeilen-ClsController (ClsController.exe) oder Agent (ClsAgent.exe)-Befehlen und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="51950-239">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="51950-240">Zusammenfassung der Firewall für den Verbund</span><span class="sxs-lookup"><span data-stu-id="51950-240">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="51950-241">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="51950-241">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="51950-242">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="51950-242">Source IP address</span></span></th>
<th><span data-ttu-id="51950-243">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="51950-243">Destination IP address</span></span></th>
<th><span data-ttu-id="51950-244">Hinweise</span><span class="sxs-lookup"><span data-stu-id="51950-244">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51950-245">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="51950-245">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="51950-246">Access Edge Service (öffentliche IP-Adresse)</span><span class="sxs-lookup"><span data-stu-id="51950-246">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="51950-247">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-247">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-248">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="51950-248">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="51950-249">Zusammenfassung der Firewall – öffentliche Instant Messaging-Konnektivität</span><span class="sxs-lookup"><span data-stu-id="51950-249">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="51950-250">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="51950-250">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="51950-251">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="51950-251">Source IP address</span></span></th>
<th><span data-ttu-id="51950-252">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="51950-252">Destination IP address</span></span></th>
<th><span data-ttu-id="51950-253">Hinweise</span><span class="sxs-lookup"><span data-stu-id="51950-253">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51950-254">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="51950-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="51950-255">Verbindungspartner für öffentliche Chats</span><span class="sxs-lookup"><span data-stu-id="51950-255">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="51950-256">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-256">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-257">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="51950-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51950-258">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="51950-258">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="51950-259">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-259">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-260">Verbindungspartner für öffentliche Chats</span><span class="sxs-lookup"><span data-stu-id="51950-260">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="51950-261">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="51950-261">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51950-262">Access/SIP (TLS)-/TCP/443</span><span class="sxs-lookup"><span data-stu-id="51950-262">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="51950-263">Clients</span><span class="sxs-lookup"><span data-stu-id="51950-263">Clients</span></span></p></td>
<td><p><span data-ttu-id="51950-264">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-264">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-265">Client-zu-Server-SIP-Datenverkehr für den Zugriff durch externe Benutzer</span><span class="sxs-lookup"><span data-stu-id="51950-265">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51950-266">A/V/RTP/TCP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="51950-266">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="51950-267">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-268">Live Messenger-Clients</span><span class="sxs-lookup"><span data-stu-id="51950-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="51950-269">Wird für A/V-Sitzungen mit Windows Live Messenger verwendet, wenn die Konnektivität für öffentliche Chats konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="51950-269">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51950-270">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="51950-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="51950-271">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-271">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-272">Live Messenger-Clients</span><span class="sxs-lookup"><span data-stu-id="51950-272">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="51950-273">Erforderlich für öffentliche Chat Verbindungen mit Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="51950-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51950-274">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="51950-274">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="51950-275">Live Messenger-Clients</span><span class="sxs-lookup"><span data-stu-id="51950-275">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="51950-276">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="51950-276">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="51950-277">Erforderlich für öffentliche Chat Verbindungen mit Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="51950-277">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="51950-278">Zusammenfassung der Firewall für erweiterbares Messaging und Anwesenheits Protokoll</span><span class="sxs-lookup"><span data-stu-id="51950-278">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="51950-279">Protokoll/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="51950-279">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="51950-280">Quelle (IP-Adresse)</span><span class="sxs-lookup"><span data-stu-id="51950-280">Source (IP address)</span></span></th>
<th><span data-ttu-id="51950-281">Ziel (IP-Adresse)</span><span class="sxs-lookup"><span data-stu-id="51950-281">Destination (IP address)</span></span></th>
<th><span data-ttu-id="51950-282">Kommentare</span><span class="sxs-lookup"><span data-stu-id="51950-282">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="51950-283">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="51950-283">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="51950-284">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-284">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-285">IP-Adresse des Edge-Server-Access-Edge-Service-Interfaces</span><span class="sxs-lookup"><span data-stu-id="51950-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="51950-286">Standard mäßiger Server-zu-Server-Kommunikationsanschluss für XMPP.</span><span class="sxs-lookup"><span data-stu-id="51950-286">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="51950-287">Ermöglicht die Kommunikation mit dem Edge-Server-XMPP-Proxy von Federated XMPP-Partnern</span><span class="sxs-lookup"><span data-stu-id="51950-287">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="51950-288">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="51950-288">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="51950-289">IP-Adresse des Edge-Server-Access-Edge-Service-Interfaces</span><span class="sxs-lookup"><span data-stu-id="51950-289">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="51950-290">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-290">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-291">Standard mäßiger Server-zu-Server-Kommunikationsanschluss für XMPP.</span><span class="sxs-lookup"><span data-stu-id="51950-291">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="51950-292">Ermöglicht die Kommunikation vom Edge Server XMPP-Proxy an Federated XMPP-Partner</span><span class="sxs-lookup"><span data-stu-id="51950-292">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="51950-293">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="51950-293">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="51950-294">Beliebig</span><span class="sxs-lookup"><span data-stu-id="51950-294">Any</span></span></p></td>
<td><p><span data-ttu-id="51950-295">Jede interne Edge-Server-Schnittstellen-IP</span><span class="sxs-lookup"><span data-stu-id="51950-295">Each internal Edge Server interface IP</span></span></p></td>
<td><p><span data-ttu-id="51950-296">Interner XMPP-Datenverkehr vom XMPP-Gateway auf dem Front-End-Server oder Front-End-Pool zur internen IP-Adresse des Edge-Servers oder zur internen IP-Adresse jedes Edge-Pools</span><span class="sxs-lookup"><span data-stu-id="51950-296">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="51950-297">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="51950-297">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

