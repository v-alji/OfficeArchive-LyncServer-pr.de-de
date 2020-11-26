---
title: Portzusammenfassung für einen einzelnen konsolidierten Edgeserver mit öffentlichen IP-Adressen
description: Port Zusammenfassung – einzelner konsolidierter Edge mit öffentlichen IP-Adressen.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single consolidated edge with public IP addresses
ms:assetid: 28407acc-8b92-4f78-875c-fd6b4323b602
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204756(v=OCS.15)
ms:contentKeyID: 48183685
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82ab2d89404fb174994d8e5b798f64bb68768326
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424264"
---
# <a name="port-summary---single-consolidated-edge-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="5ea27-103">Portzusammenfassung für einen einzelnen konsolidierten Edgeserver mit öffentlichen IP-Adressen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5ea27-103">Port summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5ea27-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5ea27-104">

<span> </span></span></span>

<span data-ttu-id="5ea27-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="5ea27-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="5ea27-106">Die in dieser Szenario-Architektur beschriebene lync Server 2013-Edgeserver-Funktionalität ähnelt dem, was in lync Server 2010 implementiert wurde.</span><span class="sxs-lookup"><span data-stu-id="5ea27-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="5ea27-107">Die bemerkenswerteste Ergänzung ist der Port **5269 over TCP** -Eintrag für das Extensible Messaging and Presence Protocol (XMPP).</span><span class="sxs-lookup"><span data-stu-id="5ea27-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="5ea27-108">Lync Server 2013 stellt optional einen XMPP-Proxy auf dem Edge-Server oder Edge-Pool und dem XMPP-Gatewayserver auf dem Front-End-Server oder Front-End-Pool bereit.</span><span class="sxs-lookup"><span data-stu-id="5ea27-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span> <span data-ttu-id="5ea27-109">Planungsinformationen für den Reverseproxy und die Föderation finden Sie in [Szenarien für den Reverse Proxy in lync Server 2013](lync-server-2013-scenarios-for-reverse-proxy.md) und [Planen für SIP, XMPP Federation und Public Instant Messaging in lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md) -Abschnitten.</span><span class="sxs-lookup"><span data-stu-id="5ea27-109">Planning information for the reverse proxy and federation are found in [Scenarios for reverse proxy in Lync Server 2013](lync-server-2013-scenarios-for-reverse-proxy.md) and [Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md) sections, respectively.</span></span>

<span data-ttu-id="5ea27-110">Neben IPv4 unterstützt der Edgeserver nun IPv6.</span><span class="sxs-lookup"><span data-stu-id="5ea27-110">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="5ea27-111">Aus Gründen der Übersichtlichkeit wird in den Szenarien nur IPv4 verwendet.</span><span class="sxs-lookup"><span data-stu-id="5ea27-111">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="5ea27-112">**Unternehmens Umkreisnetzwerk für einzelnen konsolidierten Edge mit öffentlicher IP-Adressierung**</span><span class="sxs-lookup"><span data-stu-id="5ea27-112">**Enterprise perimeter network for single consolidated edge with public IP addressing**</span></span>

<span data-ttu-id="5ea27-113">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span><span class="sxs-lookup"><span data-stu-id="5ea27-113">![f8c144c5-e5fb-498a-823e-eb39f26b6847](images/Gg425891.f8c144c5-e5fb-498a-823e-eb39f26b6847(OCS.15).jpg "f8c144c5-e5fb-498a-823e-eb39f26b6847")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="5ea27-114">Port- und Protokolldetails</span><span class="sxs-lookup"><span data-stu-id="5ea27-114">Port and Protocol Details</span></span>

<span data-ttu-id="5ea27-115">Wir empfehlen, nur die Ports zu öffnen, die erforderlich sind, um die Funktionalität zu unterstützen, für die Sie externen Zugriff bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="5ea27-115">We recommend that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="5ea27-116">Damit der Remotezugriff für jeden Edgedienst funktionieren kann, ist es zwingend erforderlich, dass der SIP-Datenverkehr bidirektional erfolgt, wie in der Abbildung für eingehende/ausgehende Edge-Datenverkehr dargestellt.</span><span class="sxs-lookup"><span data-stu-id="5ea27-116">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bidirectionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="5ea27-117">Anders ausgedrückt: das SIP-Messaging zum und vom Access-Edgedienst ist an Instant Messaging (im), Anwesenheitsinformationen, Webkonferenzen, Audio/Video (A/V) und Föderation beteiligt.</span><span class="sxs-lookup"><span data-stu-id="5ea27-117">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-single-consolidated-edge-with-public-ip-addresses-external-interface"></a><span data-ttu-id="5ea27-118">Zusammenfassung der Firewall für einzelne konsolidierte Edges mit öffentlichen IP-Adressen: externe Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5ea27-118">Firewall Summary for Single Consolidated Edge with Public IP Addresses: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ea27-119">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="5ea27-119">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="5ea27-120">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5ea27-120">Source IP address</span></span></th>
<th><span data-ttu-id="5ea27-121">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5ea27-121">Destination IP address</span></span></th>
<th><span data-ttu-id="5ea27-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5ea27-122">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-123">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="5ea27-123">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="5ea27-124">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-124">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-125">XMPP-Proxy Dienst (Freigabe der IP-Adresse mit Access Edge Service)</span><span class="sxs-lookup"><span data-stu-id="5ea27-125">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="5ea27-126">Der XMPP-Proxy Dienst akzeptiert Datenverkehr von XMPP-Kontakten in definierten XMPP-Föderationen</span><span class="sxs-lookup"><span data-stu-id="5ea27-126">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea27-127">Access/http/TCP/80</span><span class="sxs-lookup"><span data-stu-id="5ea27-127">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="5ea27-128">Öffentliche IP-Adresse des Edge-Server-Zugriffs-Edge-Diensts</span><span class="sxs-lookup"><span data-stu-id="5ea27-128">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="5ea27-129">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-129">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-130">Zertifikatsperrung/CRL-Prüfung und-Abruf</span><span class="sxs-lookup"><span data-stu-id="5ea27-130">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-131">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="5ea27-131">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="5ea27-132">Öffentliche IP-Adresse des Edge-Server-Zugriffs-Edge-Diensts</span><span class="sxs-lookup"><span data-stu-id="5ea27-132">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="5ea27-133">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-133">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-134">DNS-Abfrage über TCP</span><span class="sxs-lookup"><span data-stu-id="5ea27-134">DNS query over TCP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea27-135">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="5ea27-135">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="5ea27-136">Öffentliche IP-Adresse des Edge-Server-Zugriffs-Edge-Diensts</span><span class="sxs-lookup"><span data-stu-id="5ea27-136">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="5ea27-137">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-137">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-138">DNS-Abfrage über UDP</span><span class="sxs-lookup"><span data-stu-id="5ea27-138">DNS query over UDP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-139">Access/SIP (TLS)-/TCP/443</span><span class="sxs-lookup"><span data-stu-id="5ea27-139">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="5ea27-140">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-140">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-141">Öffentliche IP-Adresse des Edge-Server-Zugriffs-Edge-Diensts</span><span class="sxs-lookup"><span data-stu-id="5ea27-141">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="5ea27-142">Client-zu-Server-SIP-Datenverkehr für den Zugriff durch externe Benutzer</span><span class="sxs-lookup"><span data-stu-id="5ea27-142">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea27-143">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="5ea27-143">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="5ea27-144">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-144">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-145">Öffentliche IP-Adresse des Edge-Server-Zugriffs-Edge-Diensts</span><span class="sxs-lookup"><span data-stu-id="5ea27-145">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="5ea27-146">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="5ea27-146">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-147">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="5ea27-147">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="5ea27-148">Öffentliche IP-Adresse des Edge-Server-Zugriffs-Edge-Diensts</span><span class="sxs-lookup"><span data-stu-id="5ea27-148">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="5ea27-149">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-149">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-150">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="5ea27-150">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea27-151">Web Conferencing/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="5ea27-151">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="5ea27-152">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-152">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-153">Edge-Server-Webkonferenz-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5ea27-153">Edge Server Web Conferencing Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="5ea27-154">Web-Konferenzmedien</span><span class="sxs-lookup"><span data-stu-id="5ea27-154">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-155">A/V/RTP/TCP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="5ea27-155">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="5ea27-156">Öffentliche IP-Adresse des Edge-Server-Zugriffs-Edge-Diensts</span><span class="sxs-lookup"><span data-stu-id="5ea27-156">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="5ea27-157">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-157">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-158">Erforderlich für die Föderation mit Partnern, die Office Communications Server 2007, Office Communications Server 2007 R2, lync Server 2010 und lync Server 2013 ausführen.</span><span class="sxs-lookup"><span data-stu-id="5ea27-158">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea27-159">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="5ea27-159">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="5ea27-160">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5ea27-160">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="5ea27-161">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-161">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-162">Nur für den Verbund mit Partnern erforderlich, die Office Communications Server 2007 ausführen</span><span class="sxs-lookup"><span data-stu-id="5ea27-162">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-163">A/V/RTP/TCP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="5ea27-163">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="5ea27-164">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-164">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-165">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5ea27-165">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="5ea27-166">Nur für den Verbund mit Partnern erforderlich, auf denen Office Communications Server 2007 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5ea27-166">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea27-167">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="5ea27-167">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="5ea27-168">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-168">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-169">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5ea27-169">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="5ea27-170">Nur für den Verbund mit Partnern erforderlich, auf denen Office Communications Server 2007 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5ea27-170">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-171">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="5ea27-171">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="5ea27-172">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5ea27-172">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="5ea27-173">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-173">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-174">3478 Outbound wird verwendet, um die Version von Edgeserver zu ermitteln, mit der lync Server kommuniziert, sowie für Mediendatenverkehr vom Edge-Server-zu-Edge-Server.</span><span class="sxs-lookup"><span data-stu-id="5ea27-174">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="5ea27-175">Erforderlich für den Verbund mit lync Server 2010, Windows Live Messenger und Office Communications Server 2007 R2 und auch, wenn mehrere Edge-Pools in einem Unternehmen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="5ea27-175">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea27-176">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="5ea27-176">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="5ea27-177">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-177">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-178">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5ea27-178">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="5ea27-179">Betäubung/Turn Verhandlung von Kandidaten über UDP/3478</span><span class="sxs-lookup"><span data-stu-id="5ea27-179">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-180">A/V/Stun, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="5ea27-180">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="5ea27-181">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-181">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-182">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5ea27-182">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="5ea27-183">Betäubung/Turn Verhandlung von Kandidaten über TCP/443</span><span class="sxs-lookup"><span data-stu-id="5ea27-183">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea27-184">A/V/Stun, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="5ea27-184">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="5ea27-185">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5ea27-185">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="5ea27-186">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-186">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-187">Betäubung/Turn Verhandlung von Kandidaten über TCP/443</span><span class="sxs-lookup"><span data-stu-id="5ea27-187">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-single-consolidated-edge-with-public-ip-addresses-internal-interface"></a><span data-ttu-id="5ea27-188">Zusammenfassung der Firewall für einzelne konsolidierte Edges mit öffentlichen IP-Adressen: interne Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5ea27-188">Firewall Summary for Single Consolidated Edge with Public IP Addresses: Internal Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ea27-189">Protokoll/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="5ea27-189">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="5ea27-190">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5ea27-190">Source IP address</span></span></th>
<th><span data-ttu-id="5ea27-191">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5ea27-191">Destination IP address</span></span></th>
<th><span data-ttu-id="5ea27-192">Kommentare</span><span class="sxs-lookup"><span data-stu-id="5ea27-192">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-193">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="5ea27-193">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="5ea27-194">Any (kann als Standard Edition Server IP, Standard Edition Server-IP-Adresse oder Pool-IP-Adresse mit dem XMPP-Gatewayserver definiert werden)</span><span class="sxs-lookup"><span data-stu-id="5ea27-194">Any (can be defined as Standard Edition server IP, Standard Edition server IP address, or pool IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="5ea27-195">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5ea27-195">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="5ea27-196">Ausgehender XMPP-Datenverkehr vom XMPP-Gatewayserver auf dem Front-End-Server oder Front-End-Pool</span><span class="sxs-lookup"><span data-stu-id="5ea27-196">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea27-197">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="5ea27-197">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="5ea27-198">Any (kann als Director, IP-Adresse des Director-Pools, Front-End-Server oder IP-Adresse des Front-End-Pools definiert werden)</span><span class="sxs-lookup"><span data-stu-id="5ea27-198">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool IP address)</span></span></p></td>
<td><p><span data-ttu-id="5ea27-199">Edge-Server-IP oder Pool, der die interne Schnittstelle enthält</span><span class="sxs-lookup"><span data-stu-id="5ea27-199">Edge Server IP, or pool that holds the internal interface</span></span></p></td>
<td><p><span data-ttu-id="5ea27-200">Ausgehender SIP-Datenverkehr (von Director, Director-Pool-IP-Adresse, Front-End-Server oder IP-Adresse des Front-End-Pools) zu einer internen Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5ea27-200">Outbound SIP traffic (from Director, Director pool IP address, Front End Server or Front End pool IP address) to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-201">SIP/MTLS/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="5ea27-201">SIP/MTLS/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="5ea27-202">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5ea27-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="5ea27-203">Any (kann als Director, IP-Adresse des Director-Pools, Front-End-Server oder Adresse des Front-End-Pools definiert werden)</span><span class="sxs-lookup"><span data-stu-id="5ea27-203">Any (can be defined as Director, Director pool IP address, Front End Server or Front End pool address)</span></span></p></td>
<td><p><span data-ttu-id="5ea27-204">Eingehende SIP-Datenverkehr (an Director, IP-Adresse des Director-Pools, Front-End-Server oder IP-Adresse des Front-End-Pools) aus der internen Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5ea27-204">Inbound SIP traffic (to Director, Director pool IP address, Front End Server or Front End pool IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea27-205">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="5ea27-205">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="5ea27-206">Any (kann als Front-End-Server-IP-Adresse oder jede IP-Adresse eines Front-End-Servers in einem Front-End-Pool definiert werden)</span><span class="sxs-lookup"><span data-stu-id="5ea27-206">Any (can be defined as Front End Server IP address, or each Front End Server IP address in a Front End pool)</span></span></p></td>
<td><p><span data-ttu-id="5ea27-207">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5ea27-207">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="5ea27-208">Webkonferenzen-Datenverkehr vom Front-End-Server oder jedem Front-End-Server, falls in einem Pool, zu einer internen Schnittstelle des Edge-Servers</span><span class="sxs-lookup"><span data-stu-id="5ea27-208">Web conferencing traffic from Front End Server or each Front End Server if in a pool, to Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-209">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="5ea27-209">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="5ea27-210">Any (kann als Front-End-Server-IP-Adresse oder IP-Adresse des Front-End-Pools oder einer überlebensfähigen Branch-Appliance oder eines Überlebenden Branch-Servers mit diesem Edgeserver definiert werden)</span><span class="sxs-lookup"><span data-stu-id="5ea27-210">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="5ea27-211">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5ea27-211">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="5ea27-212">Authentifizierung von a/v-Benutzern (a/v-Authentifizierungsdienst) vom Front-End-Server oder der IP-Adresse des Front-End-Pools oder von einer Überlebenden Branch-Appliance oder einem Überlebenden Branch-Server mit diesem Edgeserver</span><span class="sxs-lookup"><span data-stu-id="5ea27-212">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea27-213">Stun/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="5ea27-213">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="5ea27-214">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-214">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-215">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5ea27-215">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="5ea27-216">Bevorzugter Pfad für die A/V-Medienübertragung zwischen internen und externen Benutzern, Survivable Branch Appliance oder Survivable Branch Server</span><span class="sxs-lookup"><span data-stu-id="5ea27-216">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-217">Stun/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="5ea27-217">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="5ea27-218">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-218">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-219">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5ea27-219">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="5ea27-220">Fall Back Pfad für die A/V-Medienübertragung zwischen internen und externen Benutzern, Survival-Branch-Appliance oder einem Überlebenden Branch-Server wenn die UDP-Kommunikation nicht hergestellt werden kann, wird TCP für Dateiübertragung und Desktopfreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="5ea27-220">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea27-221">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="5ea27-221">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="5ea27-222">Any (kann als die IP-Adresse des Front-End-Servers oder-Pools definiert werden, der den zentralen Verwaltungsspeicher enthält)</span><span class="sxs-lookup"><span data-stu-id="5ea27-222">Any (can be defined as the Front End Server IP address, or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="5ea27-223">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5ea27-223">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="5ea27-224">Replikation von Änderungen vom zentralen Verwaltungsspeicher auf den Edgeserver</span><span class="sxs-lookup"><span data-stu-id="5ea27-224">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-225">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="5ea27-225">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="5ea27-226">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-226">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-227">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5ea27-227">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="5ea27-228">Zentralisierter Protokollierungsdienst Controller mit lync Server-Verwaltungsshell und zentralen Protokolldienst-Cmdlets, Befehlszeilen-ClsController (ClsController.exe) oder Agent (ClsAgent.exe)-Befehlen und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="5ea27-228">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea27-229">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="5ea27-229">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="5ea27-230">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-230">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-231">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5ea27-231">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="5ea27-232">Zentralisierter Protokollierungsdienst Controller mit lync Server-Verwaltungsshell und zentralen Protokolldienst-Cmdlets, Befehlszeilen-ClsController (ClsController.exe) oder Agent (ClsAgent.exe)-Befehlen und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="5ea27-232">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-233">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="5ea27-233">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="5ea27-234">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-234">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-235">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="5ea27-235">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="5ea27-236">Zentralisierter Protokollierungsdienst Controller mit lync Server-Verwaltungsshell und zentralen Protokolldienst-Cmdlets, Befehlszeilen-ClsController (ClsController.exe) oder Agent (ClsAgent.exe)-Befehlen und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="5ea27-236">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-federation"></a><span data-ttu-id="5ea27-237">Zusammenfassung der Firewall für den Verbund</span><span class="sxs-lookup"><span data-stu-id="5ea27-237">Firewall Summary for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ea27-238">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="5ea27-238">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="5ea27-239">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5ea27-239">Source IP address</span></span></th>
<th><span data-ttu-id="5ea27-240">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5ea27-240">Destination IP address</span></span></th>
<th><span data-ttu-id="5ea27-241">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5ea27-241">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-242">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="5ea27-242">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="5ea27-243">Access Edge Service (öffentliche IP-Adresse)</span><span class="sxs-lookup"><span data-stu-id="5ea27-243">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="5ea27-244">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-244">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-245">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="5ea27-245">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="5ea27-246">Zusammenfassung der Firewall – öffentliche Instant Messaging-Konnektivität</span><span class="sxs-lookup"><span data-stu-id="5ea27-246">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ea27-247">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="5ea27-247">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="5ea27-248">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5ea27-248">Source IP address</span></span></th>
<th><span data-ttu-id="5ea27-249">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="5ea27-249">Destination IP address</span></span></th>
<th><span data-ttu-id="5ea27-250">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5ea27-250">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-251">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="5ea27-251">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="5ea27-252">Verbindungspartner für öffentliche Chats</span><span class="sxs-lookup"><span data-stu-id="5ea27-252">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="5ea27-253">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="5ea27-253">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="5ea27-254">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="5ea27-254">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea27-255">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="5ea27-255">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="5ea27-256">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="5ea27-256">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="5ea27-257">Verbindungspartner für öffentliche Chats</span><span class="sxs-lookup"><span data-stu-id="5ea27-257">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="5ea27-258">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="5ea27-258">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-259">Access/SIP (TLS)-/TCP/443</span><span class="sxs-lookup"><span data-stu-id="5ea27-259">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="5ea27-260">Clients</span><span class="sxs-lookup"><span data-stu-id="5ea27-260">Clients</span></span></p></td>
<td><p><span data-ttu-id="5ea27-261">Edge-Server-Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="5ea27-261">Edge Server Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="5ea27-262">Client-zu-Server-SIP-Datenverkehr für den Zugriff durch externe Benutzer</span><span class="sxs-lookup"><span data-stu-id="5ea27-262">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea27-263">A/V/RTP/TCP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="5ea27-263">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="5ea27-264">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="5ea27-264">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="5ea27-265">Live Messenger-Clients</span><span class="sxs-lookup"><span data-stu-id="5ea27-265">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="5ea27-266">Wird für A/V-Sitzungen mit Windows Live Messenger verwendet, wenn die Konnektivität für öffentliche Chats konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="5ea27-266">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-267">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="5ea27-267">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="5ea27-268">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="5ea27-268">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="5ea27-269">Live Messenger-Clients</span><span class="sxs-lookup"><span data-stu-id="5ea27-269">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="5ea27-270">Erforderlich für öffentliche Chat Verbindungen mit Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="5ea27-270">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea27-271">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="5ea27-271">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="5ea27-272">Live Messenger-Clients</span><span class="sxs-lookup"><span data-stu-id="5ea27-272">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="5ea27-273">Edge-Server A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="5ea27-273">Edge Server A/V Edge service</span></span></p></td>
<td><p><span data-ttu-id="5ea27-274">Erforderlich für öffentliche Chat Verbindungen mit Windows Live Messenger</span><span class="sxs-lookup"><span data-stu-id="5ea27-274">Required for public IM connectivity with Windows Live Messenger</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="5ea27-275">Zusammenfassung der Firewall für erweiterbares Messaging und Anwesenheits Protokoll</span><span class="sxs-lookup"><span data-stu-id="5ea27-275">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5ea27-276">Protokoll/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="5ea27-276">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="5ea27-277">Quelle (IP-Adresse)</span><span class="sxs-lookup"><span data-stu-id="5ea27-277">Source (IP address)</span></span></th>
<th><span data-ttu-id="5ea27-278">Ziel (IP-Adresse)</span><span class="sxs-lookup"><span data-stu-id="5ea27-278">Destination (IP address)</span></span></th>
<th><span data-ttu-id="5ea27-279">Kommentare</span><span class="sxs-lookup"><span data-stu-id="5ea27-279">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-280">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="5ea27-280">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="5ea27-281">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-281">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-282">IP-Adresse des Edge-Server-Access-Edge-Service-Interfaces</span><span class="sxs-lookup"><span data-stu-id="5ea27-282">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="5ea27-283">Standard mäßiger Server-zu-Server-Kommunikationsanschluss für XMPP.</span><span class="sxs-lookup"><span data-stu-id="5ea27-283">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="5ea27-284">Ermöglicht die Kommunikation mit dem Edge-Server-XMPP-Proxy von Federated XMPP-Partnern</span><span class="sxs-lookup"><span data-stu-id="5ea27-284">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5ea27-285">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="5ea27-285">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="5ea27-286">IP-Adresse des Edge-Server-Access-Edge-Service-Interfaces</span><span class="sxs-lookup"><span data-stu-id="5ea27-286">Edge Server Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="5ea27-287">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-287">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-288">Standard mäßiger Server-zu-Server-Kommunikationsanschluss für XMPP.</span><span class="sxs-lookup"><span data-stu-id="5ea27-288">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="5ea27-289">Ermöglicht die Kommunikation vom Edge Server XMPP-Proxy an Federated XMPP-Partner</span><span class="sxs-lookup"><span data-stu-id="5ea27-289">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5ea27-290">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="5ea27-290">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="5ea27-291">Beliebig</span><span class="sxs-lookup"><span data-stu-id="5ea27-291">Any</span></span></p></td>
<td><p><span data-ttu-id="5ea27-292">Jede interne Edge-Server-Schnittstellen-IP</span><span class="sxs-lookup"><span data-stu-id="5ea27-292">Each internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="5ea27-293">Interner XMPP-Datenverkehr vom XMPP-Gateway auf dem Front-End-Server oder Front-End-Pool zur internen IP-Adresse des Edge-Servers oder zur internen IP-Adresse jedes Edge-Pools</span><span class="sxs-lookup"><span data-stu-id="5ea27-293">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server internal IP address or each Edge pool member’s internal IP address</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5ea27-294">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5ea27-294">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

