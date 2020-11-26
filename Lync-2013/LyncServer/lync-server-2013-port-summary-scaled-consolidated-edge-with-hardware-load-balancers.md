---
title: Portzusammenfassung für skalierte konsolidierte Edgetopologie mit Hardwareastenausgleich
description: Port Zusammenfassung – skalierter konsolidierter Edge mit Hardware-Lastenausgleichsgeräten.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Scaled consolidated edge with hardware load balancers
ms:assetid: 91213b1e-f875-464b-83e8-fe3a351595a4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398739(v=OCS.15)
ms:contentKeyID: 48184841
ms.date: 04/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1a03acb3644d83669bcf0065ebb20c526ef5fa32
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424313"
---
# <a name="port-summary---scaled-consolidated-edge-with-hardware-load-balancers-in-lync-server-2013"></a><span data-ttu-id="9dd65-103">Portzusammenfassung für skalierte konsolidierte Edgetopologie mit Hardwareastenausgleich in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9dd65-103">Port summary - Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9dd65-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9dd65-104">

<span> </span></span></span>

<span data-ttu-id="9dd65-105">_**Letztes Änderungsdatum des Themas:** 2015-04-27_</span><span class="sxs-lookup"><span data-stu-id="9dd65-105">_**Topic Last Modified:** 2015-04-27_</span></span>

<span data-ttu-id="9dd65-106">Die in dieser Szenario-Architektur beschriebene lync Server 2013-Edgeserver-Funktionalität ähnelt dem, was in lync Server 2010 implementiert wurde.</span><span class="sxs-lookup"><span data-stu-id="9dd65-106">The Lync Server 2013, Edge Server functionality described in this scenario architecture is very similar to what was implemented in Lync Server 2010.</span></span> <span data-ttu-id="9dd65-107">Die bemerkenswerteste Ergänzung ist der Port **5269 over TCP** -Eintrag für das Extensible Messaging and Presence Protocol (XMPP).</span><span class="sxs-lookup"><span data-stu-id="9dd65-107">The most noticeable addition is the port **5269 over TCP** entry for the extensible messaging and presence protocol (XMPP).</span></span> <span data-ttu-id="9dd65-108">Lync Server 2013 stellt optional einen XMPP-Proxy auf dem Edge-Server oder Edge-Pool und dem XMPP-Gatewayserver auf dem Front-End-Server oder Front-End-Pool bereit.</span><span class="sxs-lookup"><span data-stu-id="9dd65-108">Lync Server 2013 optionally deploys an XMPP proxy on the Edge Server or Edge pool and the XMPP gateway server on the Front End Server or Front End pool.</span></span>

<span data-ttu-id="9dd65-109">Neben IPv4 unterstützt der Edgeserver nun IPv6.</span><span class="sxs-lookup"><span data-stu-id="9dd65-109">In addition to IPv4, the Edge Server now supports IPv6.</span></span> <span data-ttu-id="9dd65-110">Aus Gründen der Übersichtlichkeit wird in den Szenarien nur IPv4 verwendet.</span><span class="sxs-lookup"><span data-stu-id="9dd65-110">For clarity, only IPv4 is used in the scenarios.</span></span>

<span data-ttu-id="9dd65-111">**Skalierter konsolidierter Edge mithilfe des Hardware Lastenausgleichs**</span><span class="sxs-lookup"><span data-stu-id="9dd65-111">**Scaled Consolidated Edge using Hardware Load Balancing**</span></span>

<span data-ttu-id="9dd65-112">![Edge-Server-Umkreisnetzwerk-Ports und-Protokolle](images/Gg398739.063f7dd1-16db-4cc7-8708-bca9bc41184d(OCS.15).jpg "Edge-Server-Umkreisnetzwerk-Ports und-Protokolle")</span><span class="sxs-lookup"><span data-stu-id="9dd65-112">![Edge Server Perimeter Network ports and protocols](images/Gg398739.063f7dd1-16db-4cc7-8708-bca9bc41184d(OCS.15).jpg "Edge Server Perimeter Network ports and protocols")</span></span>

<div>

## <a name="port-and-protocol-details"></a><span data-ttu-id="9dd65-113">Port- und Protokolldetails</span><span class="sxs-lookup"><span data-stu-id="9dd65-113">Port and Protocol Details</span></span>

<span data-ttu-id="9dd65-114">Es wird empfohlen, nur die Ports zu öffnen, die erforderlich sind, um die Funktionalität zu unterstützen, für die Sie externen Zugriff bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9dd65-114">It is recommended that you open only the ports required to support the functionality for which you are providing external access.</span></span>

<span data-ttu-id="9dd65-115">Damit der Remotezugriff für jeden Edgedienst funktionieren kann, ist es zwingend erforderlich, dass der SIP-Datenverkehr bidirektional wie in der Abbildung des eingehenden/ausgehenden Edge-Traffics durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="9dd65-115">For remote access to work for any edge service, it is mandatory that SIP traffic is allowed to flow bi-directionally as shown in the Inbound/Outbound edge traffic figure.</span></span> <span data-ttu-id="9dd65-116">Anders ausgedrückt: das SIP-Messaging zum und vom Access-Edgedienst ist an Instant Messaging (im), Anwesenheitsinformationen, Webkonferenzen, Audio/Video (A/V) und Föderation beteiligt.</span><span class="sxs-lookup"><span data-stu-id="9dd65-116">Stated another way, the SIP messaging to and from the Access Edge service is involved in instant messaging (IM), presence, web conferencing, audio/video (A/V) and federation.</span></span>

### <a name="firewall-summary-for-scaled-consolidated-edge-hardware-load-balanced-external-interface--node-1-and-node-2-example"></a><span data-ttu-id="9dd65-117">Zusammenfassung der Firewall für den skalierten konsolidierten Edge, Hardware Lastenausgleich: externe Schnittstelle – Knoten 1 und Knoten 2 (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="9dd65-117">Firewall Summary for Scaled Consolidated Edge, Hardware Load Balanced: External Interface – Node 1 and Node 2 (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9dd65-118">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="9dd65-118">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="9dd65-119">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-119">Source IP address</span></span></th>
<th><span data-ttu-id="9dd65-120">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-120">Destination IP address</span></span></th>
<th><span data-ttu-id="9dd65-121">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9dd65-121">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9dd65-122">Access/http/TCP/80</span><span class="sxs-lookup"><span data-stu-id="9dd65-122">Access/HTTP/TCP/80</span></span></p></td>
<td><p><span data-ttu-id="9dd65-123">Öffentliche IP-Adresse des Edge-Server-Zugriffs-Edge-Diensts</span><span class="sxs-lookup"><span data-stu-id="9dd65-123">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9dd65-124">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-124">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-125">Zertifikatsperrung/CRL-Prüfung und-Abruf</span><span class="sxs-lookup"><span data-stu-id="9dd65-125">Certificate revocation/CRL check and retrieval</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dd65-126">Access/DNS/TCP/53</span><span class="sxs-lookup"><span data-stu-id="9dd65-126">Access/DNS/TCP/53</span></span></p></td>
<td><p><span data-ttu-id="9dd65-127">Öffentliche IP-Adresse des Edge-Server-Zugriffs-Edge-Diensts</span><span class="sxs-lookup"><span data-stu-id="9dd65-127">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9dd65-128">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-128">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-129">DNS-Abfrage über TCP</span><span class="sxs-lookup"><span data-stu-id="9dd65-129">DNS query over TCP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dd65-130">Access/DNS/UDP/53</span><span class="sxs-lookup"><span data-stu-id="9dd65-130">Access/DNS/UDP/53</span></span></p></td>
<td><p><span data-ttu-id="9dd65-131">Öffentliche IP-Adresse des Edge-Server-Zugriffs-Edge-Diensts</span><span class="sxs-lookup"><span data-stu-id="9dd65-131">Edge Server Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9dd65-132">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-132">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-133">DNS-Abfrage über UDP</span><span class="sxs-lookup"><span data-stu-id="9dd65-133">DNS query over UDP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dd65-134">A/V/RTP/TCP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="9dd65-134">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="9dd65-135">Edge-Server-A/V-Edgedienst-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-135">Edge Server A/V Edge service IP address</span></span></p></td>
<td><p><span data-ttu-id="9dd65-136">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-136">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-137">Erforderlich für die Föderation mit Partnern, die Office Communications Server 2007, Office Communications Server 2007 R2, lync Server 2010 und lync Server 2013 ausführen.</span><span class="sxs-lookup"><span data-stu-id="9dd65-137">Required for federating with partners running Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 and Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dd65-138">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="9dd65-138">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="9dd65-139">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-139">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9dd65-140">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-140">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-141">Nur für den Verbund mit Partnern erforderlich, auf denen Office Communications Server 2007 ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="9dd65-141">Required only for federation with partners running Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dd65-142">A/V/RTP/TCP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="9dd65-142">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="9dd65-143">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-143">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-144">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-144">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9dd65-145">Nur für den Verbund mit Partnern erforderlich, die Office Communications Server 2007 ausführen</span><span class="sxs-lookup"><span data-stu-id="9dd65-145">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dd65-146">A/V/RTP/UDP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="9dd65-146">A/V/RTP/UDP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="9dd65-147">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-147">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-148">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-148">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9dd65-149">Nur für den Verbund mit Partnern erforderlich, die Office Communications Server 2007 ausführen</span><span class="sxs-lookup"><span data-stu-id="9dd65-149">Required only for federation with partners running Office Communications Server 2007</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dd65-150">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9dd65-150">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="9dd65-151">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-151">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9dd65-152">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-152">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-153">3478 Outbound wird verwendet, um die Version von Edgeserver zu ermitteln, mit der lync Server kommuniziert, sowie für Mediendatenverkehr vom Edge-Server-zu-Edge-Server.</span><span class="sxs-lookup"><span data-stu-id="9dd65-153">3478 outbound is used to determine the version of Edge Server that Lync Server is communicating with and also for media traffic from Edge Server-to-Edge Server.</span></span> <span data-ttu-id="9dd65-154">Erforderlich für den Verbund mit lync Server 2010, Windows Live Messenger und Office Communications Server 2007 R2 und auch, wenn mehrere Edge-Pools in einem Unternehmen bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9dd65-154">Required for federation with Lync Server 2010, Windows Live Messenger, and Office Communications Server 2007 R2, and also if multiple Edge pools are deployed within a company.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dd65-155">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9dd65-155">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="9dd65-156">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-156">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-157">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-157">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9dd65-158">Betäubung/Turn Verhandlung von Kandidaten über UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9dd65-158">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dd65-159">A/V/Stun, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9dd65-159">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9dd65-160">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-160">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-161">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-161">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9dd65-162">Betäubung/Turn Verhandlung von Kandidaten über TCP/443</span><span class="sxs-lookup"><span data-stu-id="9dd65-162">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dd65-163">A/V/Stun, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9dd65-163">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9dd65-164">Edge-Server-A/V-Edgedienst, öffentliche IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-164">Edge Server A/V Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="9dd65-165">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-165">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-166">Betäubung/Turn Verhandlung von Kandidaten über TCP/443</span><span class="sxs-lookup"><span data-stu-id="9dd65-166">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-hardware-load-balanced-internal-interface-node-1-and-node-2"></a><span data-ttu-id="9dd65-167">Zusammenfassung der Firewall für den skalierten konsolidierten Edge, Hardware Lastenausgleich: internes Interface, Knoten 1 und Knoten 2</span><span class="sxs-lookup"><span data-stu-id="9dd65-167">Firewall Summary for Scaled Consolidated Edge, Hardware Load Balanced: Internal Interface Node 1 and Node 2</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9dd65-168">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="9dd65-168">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="9dd65-169">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-169">Source IP address</span></span></th>
<th><span data-ttu-id="9dd65-170">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-170">Destination IP address</span></span></th>
<th><span data-ttu-id="9dd65-171">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9dd65-171">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9dd65-172">XMPP/MTLS/TCP/23456</span><span class="sxs-lookup"><span data-stu-id="9dd65-172">XMPP/MTLS/TCP/23456</span></span></p></td>
<td><p><span data-ttu-id="9dd65-173">Any (kann als Front-End-Server Adresse oder virtuelle IP-Adresse des Front-End-Pools definiert werden, auf der der XMPP-Gatewayserver ausgeführt wird)</span><span class="sxs-lookup"><span data-stu-id="9dd65-173">Any (can be defined as Front End Server address, or Front End pool virtual IP address running the XMPP Gateway service)</span></span></p></td>
<td><p><span data-ttu-id="9dd65-174">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9dd65-174">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9dd65-175">Ausgehender XMPP-Datenverkehr vom XMPP-Gatewayserver auf dem Front-End-Server oder Front-End-Pool</span><span class="sxs-lookup"><span data-stu-id="9dd65-175">Outbound XMPP traffic from XMPP Gateway service running on Front End Server or Front End pool</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dd65-176">HTTPS/TCP/4443</span><span class="sxs-lookup"><span data-stu-id="9dd65-176">HTTPS/TCP/4443</span></span></p></td>
<td><p><span data-ttu-id="9dd65-177">Any (kann als Front-End-Server-IP oder-Pool definiert werden, der den zentralen Verwaltungsspeicher enthält)</span><span class="sxs-lookup"><span data-stu-id="9dd65-177">Any (can be defined as the Front End Server server IP or pool that holds the Central Management store)</span></span></p></td>
<td><p><span data-ttu-id="9dd65-178">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9dd65-178">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="9dd65-179">Replikation von Änderungen vom zentralen Verwaltungsspeicher auf den Edgeserver</span><span class="sxs-lookup"><span data-stu-id="9dd65-179">Replication of changes from the Central Management store to the Edge Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dd65-180">PSOM/MTLS/TCP/8057</span><span class="sxs-lookup"><span data-stu-id="9dd65-180">PSOM/MTLS/TCP/8057</span></span></p></td>
<td><p><span data-ttu-id="9dd65-181">Any (kann als Director-IP, IP-Front-End-Server oder virtuelle Pool-IP-Adresse definiert werden)</span><span class="sxs-lookup"><span data-stu-id="9dd65-181">Any (can be defined as Director IP, Front End Server IP or Pool virtual IP)</span></span></p></td>
<td><p><span data-ttu-id="9dd65-182">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9dd65-182">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="9dd65-183">Webkonferenzen-Datenverkehr von interner Bereitstellung zu interner Edge-Server Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9dd65-183">Web conferencing traffic from Internal deployment to Internal Edge Server interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dd65-184">Stun/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9dd65-184">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="9dd65-185">Any (kann als Director-IP, IP-Front-End-Server oder virtuelle Pool-IP-Adresse definiert werden)</span><span class="sxs-lookup"><span data-stu-id="9dd65-185">Any (can be defined as Director IP, Front End Server IP or Pool virtual IP)</span></span></p></td>
<td><p><span data-ttu-id="9dd65-186">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9dd65-186">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="9dd65-187">Bevorzugter Pfad für die A/V-Medienübertragung zwischen internen und externen Benutzern, Survivable Branch Appliance oder Survivable Branch Server</span><span class="sxs-lookup"><span data-stu-id="9dd65-187">Preferred path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dd65-188">Stun/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9dd65-188">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9dd65-189">Any (kann als Director-IP, IP-Front-End-Server oder virtuelle Pool-IP-Adresse definiert werden)</span><span class="sxs-lookup"><span data-stu-id="9dd65-189">Any (can be defined as Director IP, Front End Server IP or Pool virtual IP)</span></span></p></td>
<td><p><span data-ttu-id="9dd65-190">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9dd65-190">Edge Server Internal interface</span></span></p></td>
<td><p><span data-ttu-id="9dd65-191">Fall Back Pfad für die A/V-Medienübertragung zwischen internen und externen Benutzern, Survival-Branch-Appliance oder einem Überlebenden Branch-Server wenn die UDP-Kommunikation nicht hergestellt werden kann, wird TCP für Dateiübertragung und Desktopfreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="9dd65-191">Fallback path for A/V media transfer between internal and external users, Survivable Branch Appliance or Survivable Branch Server if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dd65-192">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="9dd65-192">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="9dd65-193">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-193">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-194">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9dd65-194">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9dd65-195">Zentralisierter Protokollierungsdienst Controller mit lync Server-Verwaltungsshell und zentralen Protokolldienst-Cmdlets, Befehlszeilen-ClsController (ClsController.exe) oder Agent (ClsAgent.exe)-Befehlen und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="9dd65-195">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dd65-196">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="9dd65-196">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="9dd65-197">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-197">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-198">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9dd65-198">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9dd65-199">Zentralisierter Protokollierungsdienst Controller mit lync Server-Verwaltungsshell und zentralen Protokolldienst-Cmdlets, Befehlszeilen-ClsController (ClsController.exe) oder Agent (ClsAgent.exe)-Befehlen und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="9dd65-199">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dd65-200">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="9dd65-200">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="9dd65-201">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-201">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-202">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9dd65-202">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9dd65-203">Zentralisierter Protokollierungsdienst Controller mit lync Server-Verwaltungsshell und zentralen Protokolldienst-Cmdlets, Befehlszeilen-ClsController (ClsController.exe) oder Agent (ClsAgent.exe)-Befehlen und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="9dd65-203">Centralized Logging Service controller using Lync Server Management Shell and Centralized Logging Service cmdlets, ClsController command line (ClsController.exe) or agent (ClsAgent.exe) commands and log collection</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="9dd65-204">Hardware Lastenausgleichs haben bestimmte Anforderungen, wenn Sie bereitgestellt werden, um Verfügbarkeit und Lastenausgleich für lync Server bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9dd65-204">Hardware load balancers have specific requirements when deployed to provide availability and load balancing for Lync Server.</span></span> <span data-ttu-id="9dd65-205">Die Anforderungen sind in der folgenden Abbildung und in den Tabellen definiert.</span><span class="sxs-lookup"><span data-stu-id="9dd65-205">The requirements are defined in the following figure and tables.</span></span> <span data-ttu-id="9dd65-206">Drittanbieter verwenden möglicherweise unterschiedliche Terminologie für die hier festgelegten Anforderungen.</span><span class="sxs-lookup"><span data-stu-id="9dd65-206">Third party vendors may use different terminology for the requirements defined here.</span></span> <span data-ttu-id="9dd65-207">Es ist erforderlich, die Anforderungen von lync Server den Features und Konfigurationsoptionen zuzuordnen, die vom Hersteller Ihres Hardwarelastenausgleichs bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9dd65-207">It will be necessary to map the requirements of Lync Server to the features and configuration options provided by your hardware load balancer vendor.</span></span>

<span data-ttu-id="9dd65-208">Bei der Konfiguration von Hardware-Lastenausgleichsgeräten sollten Sie die folgenden Anforderungen erfüllen:</span><span class="sxs-lookup"><span data-stu-id="9dd65-208">When configuring hardware load balancers, consider the following requirements:</span></span>

  - <span data-ttu-id="9dd65-209">Quell-Netzwerkadressübersetzung (SNAT) kann auf dem Hardware Load Balancer (HLB) für Access Edge Service und Web Conferencing Edge Service konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="9dd65-209">Source Network Address Translation (SNAT) can be configured on the hardware load balancer (HLB) for Access Edge service and Web Conferencing Edge service</span></span>

  - <span data-ttu-id="9dd65-210">SNAT kann nicht auf dem a/v-Edgedienst konfiguriert werden – der a/v-Edgedienst muss mit der Adresse des realen Servers und nicht mit der virtuellen HLB-IP (VIP) Antworten, um eine einfache Durchquerung von UDP über NAT (Stun)-/Traversal mit Relay-NAT (Turn)/Federation Turn (FTURN) zu verwenden, um ordnungsgemäß zu funktionieren</span><span class="sxs-lookup"><span data-stu-id="9dd65-210">SNAT cannot be configured on the A/V Edge service– the A/V Edge service must respond with the real server address, not the HLB virtual IP (VIP), for simple traversal of UDP over NAT (STUN)/traversal using relay NAT (TURN)/federation TURN (FTURN) to work properly</span></span>
    
      - <span data-ttu-id="9dd65-211">Wenn der Client eine Anforderung an die HLB sendet, muss die Antwort vom HLB-VIP zurückkehren.</span><span class="sxs-lookup"><span data-stu-id="9dd65-211">If the client sends a request to the HLB, the response must come back from the HLB VIP</span></span>
    
      - <span data-ttu-id="9dd65-212">Wenn der Client eine Anforderung an den Edge sendet, muss die Antwort von der Edge-IP zurückkommen.</span><span class="sxs-lookup"><span data-stu-id="9dd65-212">If the client sends a request to the Edge, the response must come back from the Edge IP</span></span>

  - <span data-ttu-id="9dd65-213">Öffentliche IP-Adressen werden auf jeder Server Schnittstelle und auf den VIPs der HLB verwendet, und Ihre Anforderungen an die öffentliche IP-Adresse sind N + 1, wobei für jede echte Server Schnittstelle eine öffentliche IP-Adresse und eine für jedes HLB-VIP vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="9dd65-213">Public IP addresses are used on each server interface and on the VIPs of the HLB, and your public IP address requirements are N+1, where there is a public IP address for each real server interface and one for each HLB VIP.</span></span> <span data-ttu-id="9dd65-214">Wenn im Pool zwei Edgeserver vorhanden sind, werden in 9 öffentliche IP-Adressen, wobei 3 für die HLB-VIPs und eine für jede Edgeserver-Schnittstelle verwendet werden (insgesamt sechs für die Server) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="9dd65-214">Where you have 2 Edge servers in the pool, this results in 9 public IP addresses, where 3 are used for the HLB VIPs, and one for each Edge server interface (a total of six for the servers)</span></span>

  - <span data-ttu-id="9dd65-215">Bei Access Edge Service und Web Conferencing Edge Service (und Verwendung von NAT auf der HLB) kontaktiert der Client den VIP, der VIP ändert die Quell-IP-Adresse vom Client in seine eigene IP-Adresse.</span><span class="sxs-lookup"><span data-stu-id="9dd65-215">For the Access Edge service and Web Conferencing Edge service, (and using NAT on the HLB) the client contacts the VIP, the VIP changes the source IP address from the client to its own IP address.</span></span> <span data-ttu-id="9dd65-216">Die Server Schnittstelle adressiert die Absenderadresse an den VIP, der VIP ändert die Quelladresse von der IP-Adresse der Server Schnittstelle und sendet das Paket an den Client.</span><span class="sxs-lookup"><span data-stu-id="9dd65-216">The server interface addresses the return address to the VIP, the VIP changes the source address from the server interface IP address and sends the packet to the client</span></span>

  - <span data-ttu-id="9dd65-217">Für den A/V-Edgedienst darf der VIP die Quell-IP-Adresse nicht ändern, und die Adresse des realen Servers wird direkt an den Client zurückgegeben – Sie können NAT auf der HLB für AV-Datenverkehr nicht konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="9dd65-217">For the A/V Edge service, the VIP must NOT change the source IP address, and the real server address is returned to the client directly – you cannot configure NAT on the HLB for AV traffic</span></span>
    
      - <span data-ttu-id="9dd65-218">Wenn der Client eine Anfrage an das HLB-VIP sendet, muss die Antwort vom HLB-VIP zurückkommen.</span><span class="sxs-lookup"><span data-stu-id="9dd65-218">If the client sends a request to the HLB VIP, the response must come back from the HLB VIP</span></span>
    
      - <span data-ttu-id="9dd65-219">Wenn der Client eine Anforderung an die Edge-IP-Adresse sendet, muss die Antwort von der Edge-IP-Adresse zurückgeliefert werden.</span><span class="sxs-lookup"><span data-stu-id="9dd65-219">If the client sends a request to the Edge IP, the response must come back from the Edge IP</span></span>

  - <span data-ttu-id="9dd65-220">Bei AV behält die externe Firewall die öffentliche IP-Adresse des realen Servers für alle Pakete bei.</span><span class="sxs-lookup"><span data-stu-id="9dd65-220">For AV, the external firewall will retain the real server public IP address for all packets</span></span>

  - <span data-ttu-id="9dd65-221">Nach der festgelegten Kommunikation des Client-zu-A/V-Edge-Diensts erfolgt die Kommunikation mit dem echten Server und nicht mit der HLB</span><span class="sxs-lookup"><span data-stu-id="9dd65-221">Once established, client to A/V Edge service communication is to the real server, not the HLB</span></span>

  - <span data-ttu-id="9dd65-222">Interner Edge-Server und-Clients müssen weitergeleitet werden, und für alle internen Netzwerke, die Server oder Clients hosten, werden permanente Routen festgesetzt.</span><span class="sxs-lookup"><span data-stu-id="9dd65-222">Internal edge to internal servers and clients must be routed, and persistent routes are set for all internal networks that host servers or clients</span></span>

  - <span data-ttu-id="9dd65-223">Der HLB Access Edge Service VIP fungiert als Standardgateway für jede Edge-Server-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="9dd65-223">The HLB Access Edge service VIP will act as the default gateway for each Edge server interface</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="9dd65-224">Weitere Informationen zur NAT-Planung und-Funktionalität finden Sie unter <A href="lync-server-2013-hardware-load-balancer-requirements.md">Hardware Load Balancer Requirements for lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="9dd65-224">For further information on NAT planning and functionality, please refer to <A href="lync-server-2013-hardware-load-balancer-requirements.md">Hardware load balancer requirements for Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="9dd65-225">![Details zu Edge-Server-Ports und-Protokollen](images/Gg398739.1c193b80-98ab-4d59-a854-dbfdb5e209e2(OCS.15).jpg "Details zu Edge-Server-Ports und-Protokollen")</span><span class="sxs-lookup"><span data-stu-id="9dd65-225">![Edge Server ports and protocols details](images/Gg398739.1c193b80-98ab-4d59-a854-dbfdb5e209e2(OCS.15).jpg "Edge Server ports and protocols details")</span></span>

### <a name="external-port-settings-required-for-scaled-consolidated-edge-hardware-load-balanced-external-interface-virtual-ips"></a><span data-ttu-id="9dd65-226">Externe Port Einstellungen für skalierten konsolidierten Edge, Hardware Lastenausgleich: externe Schnittstelle, Virtuelles IPS</span><span class="sxs-lookup"><span data-stu-id="9dd65-226">External Port Settings Required for Scaled Consolidated Edge, Hardware Load Balanced: External Interface Virtual IPs</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9dd65-227">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="9dd65-227">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="9dd65-228">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-228">Source IP address</span></span></th>
<th><span data-ttu-id="9dd65-229">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-229">Destination IP address</span></span></th>
<th><span data-ttu-id="9dd65-230">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9dd65-230">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9dd65-231">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="9dd65-231">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="9dd65-232">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-232">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-233">XMPP-Proxy Dienst (Freigabe der IP-Adresse mit Access Edge Service)</span><span class="sxs-lookup"><span data-stu-id="9dd65-233">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="9dd65-234">Der XMPP-Proxy Dienst akzeptiert Datenverkehr von XMPP-Kontakten in definierten XMPP-Föderationen</span><span class="sxs-lookup"><span data-stu-id="9dd65-234">XMPP Proxy service accepts traffic from XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dd65-235">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="9dd65-235">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="9dd65-236">XMPP-Proxy Dienst (Freigabe der IP-Adresse mit Access Edge Service)</span><span class="sxs-lookup"><span data-stu-id="9dd65-236">XMPP Proxy service (shares IP address with Access Edge service)</span></span></p></td>
<td><p><span data-ttu-id="9dd65-237">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-237">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-238">Der XMPP-Proxy Dienst sendet Datenverkehr an XMPP-Kontakte in definierten XMPP-Föderationen</span><span class="sxs-lookup"><span data-stu-id="9dd65-238">XMPP Proxy service sends traffic to XMPP contacts in defined XMPP federations</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dd65-239">Access/SIP (TLS)-/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9dd65-239">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9dd65-240">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-240">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-241">Access Edge Service Public VIP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-241">Access Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="9dd65-242">Client-zu-Server-SIP-Datenverkehr für den Zugriff durch externe Benutzer</span><span class="sxs-lookup"><span data-stu-id="9dd65-242">Client-to-server SIP traffic for external user access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dd65-243">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="9dd65-243">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="9dd65-244">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-244">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-245">Access Edge Service Public VIP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-245">Access Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="9dd65-246">SIP-Signalisierungs-, Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="9dd65-246">SIP signaling, federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dd65-247">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="9dd65-247">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="9dd65-248">Access Edge Service Public VIP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-248">Access Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="9dd65-249">Partnerverbund</span><span class="sxs-lookup"><span data-stu-id="9dd65-249">Federated partner</span></span></p></td>
<td><p><span data-ttu-id="9dd65-250">SIP-Signalisierungs-, Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="9dd65-250">SIP signaling, federated and public IM connectivity using SIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dd65-251">Web Conferencing/PSOM (TLS)/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9dd65-251">Web Conferencing/PSOM(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9dd65-252">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-252">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-253">Edge-Server-Webkonferenz-Edgedienst, öffentliche VIP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-253">Edge Server Web Conferencing Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="9dd65-254">Web-Konferenzmedien</span><span class="sxs-lookup"><span data-stu-id="9dd65-254">Web Conferencing media</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dd65-255">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9dd65-255">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="9dd65-256">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-256">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-257">Edge-Server A/V Edge Service Public VIP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-257">Edge Server A/V Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="9dd65-258">Betäubung/Turn Verhandlung von Kandidaten über UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9dd65-258">STUN/TURN negotiation of candidates over UDP/3478</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dd65-259">A/V/Stun, MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9dd65-259">A/V/STUN,MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9dd65-260">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-260">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-261">Edge-Server A/V Edge Service Public VIP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-261">Edge Server A/V Edge service public VIP address</span></span></p></td>
<td><p><span data-ttu-id="9dd65-262">Betäubung/Turn Verhandlung von Kandidaten über TCP/443</span><span class="sxs-lookup"><span data-stu-id="9dd65-262">STUN/TURN negotiation of candidates over TCP/443</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="firewall-summary-for-scaled-consolidated-edge-hardware-load-balanced-internal-interface-virtual-ips"></a><span data-ttu-id="9dd65-263">Zusammenfassung der Firewall für den skalierten konsolidierten Edge, Hardware Lastenausgleich: internes Interface, Virtuelles IPS</span><span class="sxs-lookup"><span data-stu-id="9dd65-263">Firewall Summary for Scaled Consolidated Edge, Hardware Load Balanced: Internal Interface Virtual IPs</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9dd65-264">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="9dd65-264">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="9dd65-265">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-265">Source IP address</span></span></th>
<th><span data-ttu-id="9dd65-266">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9dd65-266">Destination IP address</span></span></th>
<th><span data-ttu-id="9dd65-267">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9dd65-267">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9dd65-268">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="9dd65-268">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="9dd65-269">Any (kann als Director, Virtual IP address des Director-Pools, Front-End-Server oder virtuelle IP-Adresse des Front-End-Pools definiert werden)</span><span class="sxs-lookup"><span data-stu-id="9dd65-269">Any (can be defined as Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address)</span></span></p></td>
<td><p><span data-ttu-id="9dd65-270">Edge-Server-interne VIP-Oberfläche</span><span class="sxs-lookup"><span data-stu-id="9dd65-270">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="9dd65-271">Ausgehender SIP-Datenverkehr (von Director, Virtual IP address des Director-Pools, Front-End-Server oder virtuelle IP-Adresse des Front-End-Pools) zu interner Edge-VIP</span><span class="sxs-lookup"><span data-stu-id="9dd65-271">Outbound SIP traffic (from Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address)to Internal Edge VIP</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dd65-272">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="9dd65-272">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="9dd65-273">Edge-Server-interne VIP-Oberfläche</span><span class="sxs-lookup"><span data-stu-id="9dd65-273">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="9dd65-274">Any (kann als Director, Virtual IP address des Director-Pools, Front-End-Server oder virtuelle IP-Adresse des Front-End-Pools definiert werden)</span><span class="sxs-lookup"><span data-stu-id="9dd65-274">Any (can be defined as Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address)</span></span></p></td>
<td><p><span data-ttu-id="9dd65-275">Eingehende SIP-Datenverkehr (an Director, Virtual IP address des Director-Pools, virtuelle IP-Adresse des Front-End-Servers oder virtuelle IP-Adresse des Front-End-Pools) aus der internen</span><span class="sxs-lookup"><span data-stu-id="9dd65-275">Inbound SIP traffic (to Director, Director pool virtual IP address, Front End Server or Front End pool virtual IP address) from Edge Server internal interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dd65-276">SIP/MTLS/TCP/5062</span><span class="sxs-lookup"><span data-stu-id="9dd65-276">SIP/MTLS/TCP/5062</span></span></p></td>
<td><p><span data-ttu-id="9dd65-277">Any (kann als Front-End-Server-IP-Adresse oder IP-Adresse des Front-End-Pools oder einer überlebensfähigen Branch-Appliance oder eines Überlebenden Branch-Servers mit diesem Edgeserver definiert werden)</span><span class="sxs-lookup"><span data-stu-id="9dd65-277">Any (can be defined as Front End Server IP address, or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server)</span></span></p></td>
<td><p><span data-ttu-id="9dd65-278">Edge-Server-interne VIP-Oberfläche</span><span class="sxs-lookup"><span data-stu-id="9dd65-278">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="9dd65-279">Authentifizierung von a/v-Benutzern (a/v-Authentifizierungsdienst) vom Front-End-Server oder der IP-Adresse des Front-End-Pools oder von einer Überlebenden Branch-Appliance oder einem Überlebenden Branch-Server mit diesem Edgeserver</span><span class="sxs-lookup"><span data-stu-id="9dd65-279">Authentication of A/V users (A/V authentication service) from Front End Server or Front End pool IP address or any Survivable Branch Appliance or Survivable Branch Server using this Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dd65-280">Stun/MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="9dd65-280">STUN/MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="9dd65-281">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-281">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-282">Edge-Server-interne VIP-Oberfläche</span><span class="sxs-lookup"><span data-stu-id="9dd65-282">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="9dd65-283">Bevorzugter Pfad für die A/V-Medienübertragung zwischen internen und externen Benutzern</span><span class="sxs-lookup"><span data-stu-id="9dd65-283">Preferred path for A/V media transfer between internal and external users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9dd65-284">Stun/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9dd65-284">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9dd65-285">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-285">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-286">Edge-Server-interne VIP-Oberfläche</span><span class="sxs-lookup"><span data-stu-id="9dd65-286">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="9dd65-287">Fall Back Pfad für die A/V-Medienübertragung zwischen internen und externen Benutzern wenn keine UDP-Kommunikation eingerichtet werden kann, wird TCP für Dateiübertragung und Desktopfreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="9dd65-287">Fallback path for A/V media transfer between internal and external users if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9dd65-288">Stun/MSTURN/TCP/443</span><span class="sxs-lookup"><span data-stu-id="9dd65-288">STUN/MSTURN/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="9dd65-289">Edge-Server-interne VIP-Oberfläche</span><span class="sxs-lookup"><span data-stu-id="9dd65-289">Edge Server Internal VIP interface</span></span></p></td>
<td><p><span data-ttu-id="9dd65-290">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9dd65-290">Any</span></span></p></td>
<td><p><span data-ttu-id="9dd65-291">Fall Back Pfad für die A/V-Medienübertragung zwischen internen und externen Benutzern wenn keine UDP-Kommunikation eingerichtet werden kann, wird TCP für Dateiübertragung und Desktopfreigabe verwendet.</span><span class="sxs-lookup"><span data-stu-id="9dd65-291">Fallback path for A/V media transfer between internal and external users if UDP communication cannot be established, TCP is used for file transfer and desktop sharing</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9dd65-292">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9dd65-292">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

