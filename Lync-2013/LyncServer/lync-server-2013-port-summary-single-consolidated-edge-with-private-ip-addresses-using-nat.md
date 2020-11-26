---
title: Portzusammenfassung für einen einzelnen konsolidierten Edgeserver mit privaten IP-Adressen und NAT
description: Port Zusammenfassung – einzelner konsolidierter Edge mit privaten IP-Adressen mithilfe von NAT.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single consolidated edge with private IP addresses using NAT
ms:assetid: 3c1a389f-5f42-4719-a05b-e0b84aa3eb9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425891(v=OCS.15)
ms:contentKeyID: 48183877
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3fc182b9fbbd24d589feb7f73e3c0086fa23152
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424296"
---
# <a name="port-summary---single-consolidated-edge-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="6e12f-103">Portzusammenfassung für einen einzelnen konsolidierten Edgeserver mit privaten IP-Adressen und NAT in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6e12f-103">Port summary - Single consolidated edge with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6e12f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6e12f-104">

<span> </span></span></span>

<span data-ttu-id="6e12f-105">_**Letztes Änderungsdatum des Themas:** 2013-04-03_</span><span class="sxs-lookup"><span data-stu-id="6e12f-105">_**Topic Last Modified:** 2013-04-03_</span></span>

<span data-ttu-id="6e12f-106">Die in dieser Szenario-Architektur beschriebene lync Server 2013-Edgeserver-Funktionalität ähnelt dem, was in lync Server 2010 implementiert wurde.</span><span class="sxs-lookup"><span data-stu-id="6e12f-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="6e12f-107">Die bemerkenswerteste Ergänzung ist der Port **5269 over TCP** -Eintrag für das Extensible Messaging and Presence Protocol (XMPP).</span><span class="sxs-lookup"><span data-stu-id="6e12f-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="6e12f-108">Lync Server 2013 stellt optional einen XMPP-Proxy auf dem Edge-Server oder Edge-Pool und dem XMPP-Gatewayserver auf dem Front-End-Server oder Front-End-Pool bereit.</span><span class="sxs-lookup"><span data-stu-id="6e12f-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="6e12f-109">Neben IPv4 unterstützt der Edgeserver nun IPv6.</span><span class="sxs-lookup"><span data-stu-id="6e12f-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="6e12f-110">Aus Gründen der Übersichtlichkeit wird in den Szenarien nur IPv4 verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e12f-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="6e12f-111">**Netzwerk Perimeter für einen einzelnen konsolidierten Edgeserver mit privater IP-Adressierung mithilfe von NAT**</span><span class="sxs-lookup"><span data-stu-id="6e12f-111">**Network Perimeter for a Single Consolidated Edge Server with Private IP Addressing Using NAT**</span></span>

<span data-ttu-id="6e12f-112">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span><span class="sxs-lookup"><span data-stu-id="6e12f-112">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="6e12f-113">Port- und Protokolldetails</span><span class="sxs-lookup"><span data-stu-id="6e12f-113">Port and Protocol Details</span></span>

<span data-ttu-id="6e12f-114">Wir empfehlen, nur die Ports zu öffnen, die erforderlich sind, um die Funktionalität zu unterstützen, für die Sie externen Zugriff bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6e12f-114">We recommend that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="6e12f-115">Damit der Remotezugriff für jeden Edgedienst funktionieren kann, ist es zwingend erforderlich, dass der SIP-Datenverkehr bidirektional wie in der Abbildung des eingehenden/ausgehenden Edge-Traffics durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="6e12f-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="6e12f-116">Anders ausgedrückt: das SIP-Messaging zum und vom Access-Edgedienst ist an Instant Messaging (im), Anwesenheitsinformationen, Webkonferenzen, Audio/Video (A/V) und Föderation beteiligt.</span><span class="sxs-lookup"><span data-stu-id="6e12f-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V), and federation.</span></span>

### <a name="firewall-summary-for-single-consolidated-edge-with-private-ip-addresses-using-nat-external-interface"></a><span data-ttu-id="6e12f-117">Zusammenfassung der Firewall für einen einzelnen konsolidierten Edge mit privaten IP-Adressen mithilfe von NAT: externe Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6e12f-117">Firewall Summary for Single Consolidated Edge with Private IP Addresses using NAT: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6e12f-118">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="6e12f-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="6e12f-119">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="6e12f-119">Source IP address</span></span></th>
<th><span data-ttu-id="6e12f-120">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="6e12f-120">Destination IP address</span></span></th>
<th><span data-ttu-id="6e12f-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6e12f-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-122">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="6e12f-122">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="6e12f-123">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-123">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-124">XMPP-Proxy Dienst (Freigabe der IP-Adresse mit Access Edge Service)</span><span class="sxs-lookup"><span data-stu-id="6e12f-124">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="6e12f-125">Der XMPP-Proxy Dienst akzeptiert Datenverkehr von XMPP-Kontakten in definierten XMPP-Föderationen</span><span class="sxs-lookup"><span data-stu-id="6e12f-125">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e12f-126">Access/http/TCP/80</span><span class="sxs-lookup"><span data-stu-id="6e12f-126">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="6e12f-127">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-127">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-128">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-128">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-129">Zertifikatsperrung/CRL-Prüfung und-Abruf</span><span class="sxs-lookup"><span data-stu-id="6e12f-129">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-130">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="6e12f-130">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="6e12f-131">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-131">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-132">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-132">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-133">DNS-Abfrage über TCP</span><span class="sxs-lookup"><span data-stu-id="6e12f-133">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e12f-134">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="6e12f-134">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="6e12f-135">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-135">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-136">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-136">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-137">DNS-Abfrage über UDP</span><span class="sxs-lookup"><span data-stu-id="6e12f-137">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-138">Access/SIP (TLS)-/TCP/443</span><span class="sxs-lookup"><span data-stu-id="6e12f-138">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="6e12f-139">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-139">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-140">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-140">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-141">Client-zu-Server-SIP-Datenverkehr für den Zugriff durch externe Benutzer</span><span class="sxs-lookup"><span data-stu-id="6e12f-141">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e12f-142">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="6e12f-142">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="6e12f-143">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-143">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-144">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-144">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-145">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="6e12f-145">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-146">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="6e12f-146">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="6e12f-147">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-147">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-148">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-148">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-149">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="6e12f-149">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e12f-150">Web Conferencing/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="6e12f-150">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="6e12f-151">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-151">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-152">Edge-Server-Webkonferenz-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-152">Edge Server Web Conferencing Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-153">Web-Konferenzmedien</span><span class="sxs-lookup"><span data-stu-id="6e12f-153">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-154">A/V/RTP/TCP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="6e12f-154">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="6e12f-155">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-155">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-156">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-156">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-157">Erforderlich für die Föderation mit Partnern, die Office Communications Server 2007, Office Communications Server 2007 R2, lync Server 2010 und lync Server 2013 ausführen.</span><span class="sxs-lookup"><span data-stu-id="6e12f-157">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e12f-158">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="6e12f-158">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="6e12f-159">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-159">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-160">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-160">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-161">Nur für den Verbund mit Partnern erforderlich, auf denen Office Communications Server 2007 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="6e12f-161">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-162">A/V/RTP/TCP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="6e12f-162">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="6e12f-163">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-163">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-164">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-164">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-165">Nur für den Verbund mit Partnern erforderlich, die Office Communications Server 2007 ausführen</span><span class="sxs-lookup"><span data-stu-id="6e12f-165">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e12f-166">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="6e12f-166">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="6e12f-167">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-167">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-168">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-168">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-169">Nur für den Verbund mit Partnern erforderlich, die Office Communications Server 2007 ausführen</span><span class="sxs-lookup"><span data-stu-id="6e12f-169">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-170">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="6e12f-170">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="6e12f-171">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-171">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-172">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-172">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-173">3478 Outbound wird verwendet, um die Version von Edgeserver zu ermitteln, mit der lync Server kommuniziert, sowie für Mediendatenverkehr vom Edge-Server-zu-Edge-Server.</span><span class="sxs-lookup"><span data-stu-id="6e12f-173">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="6e12f-174">Erforderlich für den Verbund mit lync Server 2010, Windows Live Messenger und Office Communications Server 2007 R2 und auch, wenn mehrere Edge-Pools in einem Unternehmen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="6e12f-174">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e12f-175">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="6e12f-175">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="6e12f-176">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-176">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-177">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-177">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-178">Betäubung/Turn Verhandlung von Kandidaten über UDP/3478</span><span class="sxs-lookup"><span data-stu-id="6e12f-178">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-179">A/V/Stun, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="6e12f-179">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="6e12f-180">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-180">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-181">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-181">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-182">Betäubung/Turn Verhandlung von Kandidaten über TCP/443</span><span class="sxs-lookup"><span data-stu-id="6e12f-182">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e12f-183">A/V/Stun, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="6e12f-183">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="6e12f-184">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-184">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-185">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-185">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-186">Betäubung/Turn Verhandlung von Kandidaten über TCP/443</span><span class="sxs-lookup"><span data-stu-id="6e12f-186">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-single-consolidated-edge-with-private-ip-addresses-using-nat-internal-interface"></a><span data-ttu-id="6e12f-187">Zusammenfassung der Firewall für einen einzelnen konsolidierten Edge mit privaten IP-Adressen mithilfe von NAT: interne Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6e12f-187">Firewall Summary for Single Consolidated Edge with Private IP Addresses Using NAT: Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6e12f-188">Protokoll/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="6e12f-188">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="6e12f-189">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="6e12f-189">Source IP address</span></span></th>
<th><span data-ttu-id="6e12f-190">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="6e12f-190">Destination IP address</span></span></th>
<th><span data-ttu-id="6e12f-191">Kommentare</span><span class="sxs-lookup"><span data-stu-id="6e12f-191">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-192">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="6e12f-192">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="6e12f-193">Any (kann als Standard Edition Server IP, Standard Edition Server-IP-Adresse oder Pool-IP-Adresse mit dem XMPP-Gatewayserver definiert werden)</span><span class="sxs-lookup"><span data-stu-id="6e12f-193">Any (can be defined as Standard Edition server IP, Standard Edition server IP address, or pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="6e12f-194">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6e12f-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6e12f-195">Ausgehender XMPP-Datenverkehr vom XMPP-Gatewayserver auf dem Front-End-Server oder Front-End-Pool</span><span class="sxs-lookup"><span data-stu-id="6e12f-195">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e12f-196">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="6e12f-196">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="6e12f-197">Any (kann als Director, IP-Adresse des Director-Pools, Front-End-Server oder IP-Adresse des Front-End-Pools definiert werden)</span><span class="sxs-lookup"><span data-stu-id="6e12f-197">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="6e12f-198">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6e12f-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6e12f-199">Ausgehender SIP-Datenverkehr (von Director, Director-Pool-IP-Adresse, Front-End-Server oder IP-Adresse des Front-End-Pools) zu einer internen Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6e12f-199">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-200">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="6e12f-200">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="6e12f-201">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6e12f-201">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6e12f-202">Any (kann als Director, IP-Adresse des Director-Pools, Front-End-Server oder IP-Adresse des Front-End-Pools definiert werden)</span><span class="sxs-lookup"><span data-stu-id="6e12f-202">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="6e12f-203">Eingehende SIP-Datenverkehr (an Director, IP-Adresse des Director-Pools, Front-End-Server oder IP-Adresse des Front-End-Pools) aus der internen Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6e12f-203">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e12f-204">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="6e12f-204">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="6e12f-205">Any (kann als Front-End-Server-IP-Adresse oder jede IP-Adresse eines Front-End-Servers in einem Front-End-Pool definiert werden)</span><span class="sxs-lookup"><span data-stu-id="6e12f-205">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="6e12f-206">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6e12f-206">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6e12f-207">Webkonferenzen-Datenverkehr vom Front-End-Server oder jedem Front-End-Server, falls in einem Pool, zu einer internen Schnittstelle des Edge-Servers</span><span class="sxs-lookup"><span data-stu-id="6e12f-207">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-208">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="6e12f-208">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="6e12f-209">Any (kann als Front-End-Server-IP-Adresse oder IP-Adresse des Front-End-Pools oder einer überlebensfähigen Branch-Appliance oder eines Überlebenden Branch-Servers mit diesem Edgeserver definiert werden)</span><span class="sxs-lookup"><span data-stu-id="6e12f-209">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="6e12f-210">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6e12f-210">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6e12f-211">Authentifizierung von a/v-Benutzern (a/v-Authentifizierungsdienst) vom Front-End-Server oder der IP-Adresse des Front-End-Pools oder von einer Überlebenden Branch-Appliance oder einem Überlebenden Branch-Server mit diesem Edgeserver</span><span class="sxs-lookup"><span data-stu-id="6e12f-211">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e12f-212">Stun/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="6e12f-212">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="6e12f-213">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-213">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-214">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6e12f-214">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6e12f-215">Bevorzugter Pfad für die A/V-Medienübertragung zwischen internen und externen Benutzern, Survivable Branch Appliance oder Survivable Branch Server</span><span class="sxs-lookup"><span data-stu-id="6e12f-215">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-216">Stun/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="6e12f-216">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="6e12f-217">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-217">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-218">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6e12f-218">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6e12f-219">Fall Back Pfad für die A/V-Medienübertragung zwischen internen und externen Benutzern, Survival-Branch-Appliance oder einem Überlebenden Branch-Server wenn die UDP-Kommunikation nicht hergestellt werden kann, wird TCP für Dateiübertragung und Desktopfreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="6e12f-219">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e12f-220">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="6e12f-220">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="6e12f-221">Any (kann als die IP-Adresse des Front-End-Servers oder-Pools definiert werden, der den zentralen Verwaltungsspeicher enthält)</span><span class="sxs-lookup"><span data-stu-id="6e12f-221">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="6e12f-222">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6e12f-222">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6e12f-223">Replikation von Änderungen vom zentralen Verwaltungsspeicher auf den Edgeserver</span><span class="sxs-lookup"><span data-stu-id="6e12f-223">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-224">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="6e12f-224">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="6e12f-225">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-225">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-226">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6e12f-226">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6e12f-227">Zentralisierter Protokollierungsdienst Controller mit lync Server-Verwaltungsshell und zentralen Protokolldienst-Cmdlets, Befehlszeilen-ClsController (ClsController.exe) oder Agent (ClsAgent.exe)-Befehlen und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="6e12f-227">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e12f-228">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="6e12f-228">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="6e12f-229">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-229">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-230">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6e12f-230">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6e12f-231">Zentralisierter Protokollierungsdienst Controller mit lync Server-Verwaltungsshell und zentralen Protokolldienst-Cmdlets, Befehlszeilen-ClsController (ClsController.exe) oder Agent (ClsAgent.exe)-Befehlen und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="6e12f-231">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-232">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="6e12f-232">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="6e12f-233">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-233">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-234">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="6e12f-234">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="6e12f-235">Zentralisierter Protokollierungsdienst Controller mit lync Server-Verwaltungsshell und zentralen Protokolldienst-Cmdlets, Befehlszeilen-ClsController (ClsController.exe) oder Agent (ClsAgent.exe)-Befehlen und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="6e12f-235">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="6e12f-236">Zusammenfassung der Firewall für den Verbund</span><span class="sxs-lookup"><span data-stu-id="6e12f-236">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6e12f-237">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="6e12f-237">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="6e12f-238">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="6e12f-238">Source IP address</span></span></th>
<th><span data-ttu-id="6e12f-239">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="6e12f-239">Destination IP address</span></span></th>
<th><span data-ttu-id="6e12f-240">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6e12f-240">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-241">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="6e12f-241">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="6e12f-242">Access Edge Service (öffentliche IP-Adresse)</span><span class="sxs-lookup"><span data-stu-id="6e12f-242">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="6e12f-243">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-243">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-244">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="6e12f-244">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="6e12f-245">Zusammenfassung der Firewall – öffentliche Instant Messaging-Konnektivität</span><span class="sxs-lookup"><span data-stu-id="6e12f-245">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6e12f-246">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="6e12f-246">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="6e12f-247">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="6e12f-247">Source IP address</span></span></th>
<th><span data-ttu-id="6e12f-248">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="6e12f-248">Destination IP address</span></span></th>
<th><span data-ttu-id="6e12f-249">Hinweise</span><span class="sxs-lookup"><span data-stu-id="6e12f-249">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-250">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="6e12f-250">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="6e12f-251">Verbindungspartner für öffentliche Chats</span><span class="sxs-lookup"><span data-stu-id="6e12f-251">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="6e12f-252">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-252">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-253">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="6e12f-253">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e12f-254">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="6e12f-254">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="6e12f-255">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-255">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-256">Verbindungspartner für öffentliche Chats</span><span class="sxs-lookup"><span data-stu-id="6e12f-256">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="6e12f-257">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="6e12f-257">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-258">Access/SIP (TLS)-/TCP/443</span><span class="sxs-lookup"><span data-stu-id="6e12f-258">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="6e12f-259">Clients</span><span class="sxs-lookup"><span data-stu-id="6e12f-259">Clients</span></span></p></td>
<td><p><span data-ttu-id="6e12f-260">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-260">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-261">Client-zu-Server-SIP-Datenverkehr für den Zugriff durch externe Benutzer</span><span class="sxs-lookup"><span data-stu-id="6e12f-261">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e12f-262">A/V/RTP/TCP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="6e12f-262">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="6e12f-263">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-263">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-264">Live Messenger-Clients</span><span class="sxs-lookup"><span data-stu-id="6e12f-264">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="6e12f-265">Wird für A/V-Sitzungen mit Windows Live Messenger verwendet, wenn die Konnektivität für öffentliche Chats konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="6e12f-265">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-266">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="6e12f-266">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="6e12f-267">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-267">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-268">Live Messenger-Clients</span><span class="sxs-lookup"><span data-stu-id="6e12f-268">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="6e12f-269">Erforderlich für öffentliche Chat Verbindungen mit Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="6e12f-269">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e12f-270">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="6e12f-270">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="6e12f-271">Live Messenger-Clients</span><span class="sxs-lookup"><span data-stu-id="6e12f-271">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="6e12f-272">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="6e12f-272">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="6e12f-273">Erforderlich für öffentliche Chat Verbindungen mit Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="6e12f-273">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="6e12f-274">Zusammenfassung der Firewall für erweiterbares Messaging und Anwesenheits Protokoll</span><span class="sxs-lookup"><span data-stu-id="6e12f-274">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6e12f-275">Protokoll/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="6e12f-275">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="6e12f-276">Quelle (IP-Adresse)</span><span class="sxs-lookup"><span data-stu-id="6e12f-276">Source (IP address)</span></span></th>
<th><span data-ttu-id="6e12f-277">Ziel (IP-Adresse)</span><span class="sxs-lookup"><span data-stu-id="6e12f-277">Destination (IP address)</span></span></th>
<th><span data-ttu-id="6e12f-278">Kommentare</span><span class="sxs-lookup"><span data-stu-id="6e12f-278">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-279">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="6e12f-279">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="6e12f-280">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-280">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-281">IP-Adresse des Edge-Server-Access-Edge-Service-Interfaces</span><span class="sxs-lookup"><span data-stu-id="6e12f-281">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="6e12f-282">Standard mäßiger Server-zu-Server-Kommunikationsanschluss für XMPP.</span><span class="sxs-lookup"><span data-stu-id="6e12f-282">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="6e12f-283">Ermöglicht die Kommunikation mit dem Edge-Server-XMPP-Proxy von Federated XMPP-Partnern</span><span class="sxs-lookup"><span data-stu-id="6e12f-283">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6e12f-284">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="6e12f-284">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="6e12f-285">IP-Adresse des Edge-Server-Access-Edge-Service-Interfaces</span><span class="sxs-lookup"><span data-stu-id="6e12f-285">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="6e12f-286">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-286">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-287">Standard mäßiger Server-zu-Server-Kommunikationsanschluss für XMPP.</span><span class="sxs-lookup"><span data-stu-id="6e12f-287">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="6e12f-288">Ermöglicht die Kommunikation vom Edge Server XMPP-Proxy an Federated XMPP-Partner</span><span class="sxs-lookup"><span data-stu-id="6e12f-288">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6e12f-289">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="6e12f-289">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="6e12f-290">Beliebig</span><span class="sxs-lookup"><span data-stu-id="6e12f-290">Any</span></span></p></td>
<td><p><span data-ttu-id="6e12f-291">Jede interne Edge-Server-Schnittstellen-IP</span><span class="sxs-lookup"><span data-stu-id="6e12f-291">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="6e12f-292">Interner XMPP-Datenverkehr vom XMPP-Gateway auf dem Front-End-Server oder Front-End-Pool zur internen IP-Adresse des Edge-Servers oder zur internen IP-Adresse jedes Edge-Pools</span><span class="sxs-lookup"><span data-stu-id="6e12f-292">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6e12f-293">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6e12f-293">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

