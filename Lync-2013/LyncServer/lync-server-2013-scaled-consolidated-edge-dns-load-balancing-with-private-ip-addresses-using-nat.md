---
title: 'Lync Server 2013: Skalierter konsolidierter Edgeserver, DNS-Lastenausgleich mit privaten IP-Adressen und NAT'
description: 'Lync Server 2013: skalierter konsolidierter Edge, DNS-Lastenausgleich mit privaten IP-Adressen mithilfe von NAT.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scaled consolidated edge, DNS load balancing with private IP addresses using NAT
ms:assetid: c7ca4ca8-c639-4d93-86d7-8891170cacbc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398823(v=OCS.15)
ms:contentKeyID: 48185369
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a1b668902059ef2680525b884d8b2c5e8486260
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394878"
---
# <a name="scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="cf434-103">Skalierter konsolidierter Edgeserver, DNS-Lastenausgleich mit privaten IP-Adressen und NAT in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf434-103">Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cf434-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cf434-104">

<span> </span></span></span>

<span data-ttu-id="cf434-105">_**Letztes Änderungsdatum des Themas:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="cf434-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="cf434-106">In der Edge-Server Pool-Topologie werden zwei oder mehr Edgeserver als Lastenausgleichspool im Umkreisnetzwerk des Rechenzentrums bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="cf434-106">In the Edge Server pool topology, two or more Edge Servers are deployed as a load-balanced pool in the perimeter network of the data center.</span></span> <span data-ttu-id="cf434-107">Der DNS-Lastenausgleich (Domain Name System) wird für den Datenverkehr sowohl an der externen als auch an der internen Edge-Schnittstelle verwendet.</span><span class="sxs-lookup"><span data-stu-id="cf434-107">Domain Name System (DNS) load balancing is used for traffic to both the external and internal Edge interfaces.</span></span>

<span data-ttu-id="cf434-108">Wenn Ihre Organisation Unterstützung für mehr als 15.000-Access-Edgedienst-Clientverbindungen, 1.000 Active lync Server-Webkonferenzdienst-Clientverbindungen oder 500 gleichzeitige A/V-Edge-Sitzungen und/oder eine große Verfügbarkeit des Edgeserver erfordert, bietet diese Topologie die Vorteile der Skalierbarkeit und der Failover-Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="cf434-108">If your organization requires support for more than 15,000 Access Edge service client connections, 1,000 active Lync Server Web Conferencing service client connections, or 500 concurrent A/V Edge sessions, and/or high availability of the Edge Server is important, this topology offers the advantages of scalability and failover support.</span></span>

<span data-ttu-id="cf434-109">Die Abbildung zeigt keine Directors, eine optionale Serverrolle, die im internen Netzwerk zwischen den Edgeserver und ihren Front-End-Pools oder-Servern bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="cf434-109">The figure does not show Directors, an optional server role deployed in the internal network between the Edge Servers and your Front End pools or server.</span></span> <span data-ttu-id="cf434-110">Details zur Topologie für Directors finden Sie unter [für den Director in lync Server 2013 erforderliche Komponenten](lync-server-2013-components-required-for-the-director.md).</span><span class="sxs-lookup"><span data-stu-id="cf434-110">For details about the topology for Directors, see [Components required for the Director in Lync Server 2013](lync-server-2013-components-required-for-the-director.md).</span></span> <span data-ttu-id="cf434-111">Die Abbildung stellt einen einzelnen Reverse-Proxy dar.</span><span class="sxs-lookup"><span data-stu-id="cf434-111">The figure represents a single reverse proxy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="cf434-112">Die angezeigte Abbildung dient zur Orientierung und zum Beispiel für die IP-Adressierung, beabsichtigt aber nicht, tatsächliche Kommunikationsflüsse mit dem korrekten ein-und ausgehenden Datenverkehr darzustellen.</span><span class="sxs-lookup"><span data-stu-id="cf434-112">The figure shown is for orientation and example IP addressing, but does not intend to represent actual communication flows with the correct incoming and outgoing traffic.</span></span> <span data-ttu-id="cf434-113">Die Abbildung stellt eine Ansicht des möglichen Datenverkehrs auf hoher Ebene dar.</span><span class="sxs-lookup"><span data-stu-id="cf434-113">The figure represents a high level view of possible traffic.</span></span> <span data-ttu-id="cf434-114">Details für den Datenverkehrs Fluss in Bezug auf eingehende (zu hörende Ports) und ausgehende (an Zielserver oder-Clients) werden in den einzelnen Szenarien im Diagramm Port Zusammenfassung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="cf434-114">Details for traffic flow as they pertain to incoming (to listening ports) and outgoing (to destination servers or clients) is represented in the Port Summary diagram in each scenario.</span></span> <span data-ttu-id="cf434-115">TCP 443 ist beispielsweise eigentlich nur eingehend (zum Edge-oder Reverse-Proxy) und ist nur ein bidirektionaler Fluss aus einer Protokoll (TCP)-Perspektive.</span><span class="sxs-lookup"><span data-stu-id="cf434-115">For example, TCP 443 is actually inbound (to the Edge or reverse proxy) only, and is only a two-way flow from a protocol (TCP) perspective.</span></span> <span data-ttu-id="cf434-116">Darüber hinaus zeigt die Abbildung die Art des Datenverkehrs an, wenn die NAT (Netzwerkadressübersetzung) Eintritt (die Zieladresse wird bei der eingehenden Änderung geändert, die Quelladresse wird beim ausgehen geändert).</span><span class="sxs-lookup"><span data-stu-id="cf434-116">Additionally, the figure shows the nature of traffic as it changes when NAT (network address translation) occurs (destination address is changed on inbound, source address is changed on outbound).</span></span> <span data-ttu-id="cf434-117">Beispiel für externe und interne Firewalls und Serverschnittstellen werden nur zu Referenzzwecken angezeigt.</span><span class="sxs-lookup"><span data-stu-id="cf434-117">Example external and internal firewall, and server interfaces are shown for reference purposes only.</span></span> <span data-ttu-id="cf434-118">Schließlich werden beispielsweise Standard-Gateway-und-Routen Beziehungen angezeigt, sofern zutreffend.</span><span class="sxs-lookup"><span data-stu-id="cf434-118">Finally, example default gateway and route relationships are shown, where applicable.</span></span> <span data-ttu-id="cf434-119">Beachten Sie auch, dass das Diagramm die DNS-Zone " <EM>. com</EM> " verwendet, um die externe DNS-Zone für Reverse-Proxy-und Edgeserver darzustellen, und die <EM>.net</EM> -DNS-Zone bezieht sich auf die interne DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="cf434-119">Note also that the diagram uses the <EM>.com</EM> DNS zone to represent the external DNS zone for both reverse proxy and Edge Servers, and the <EM>.net</EM> DNS zone refers to the internal DNS zone.</span></span>



</div>

<span data-ttu-id="cf434-120">Neu bei Microsoft lync Server 2013 ist die Unterstützung für die IPv6-Adressierung.</span><span class="sxs-lookup"><span data-stu-id="cf434-120">New to Microsoft Lync Server 2013 is support for IPv6 addressing.</span></span> <span data-ttu-id="cf434-121">Ähnlich wie bei der IPv4-Adressierung müssen IPv6-Adressen so zugewiesen werden, dass die Adressenteil des zugewiesenen IPv6-Adressraums sind.</span><span class="sxs-lookup"><span data-stu-id="cf434-121">Much like IPv4 addressing, IPv6 addresses must be assigned in such a way that the addresses are part of your assigned IPv6 address space.</span></span> <span data-ttu-id="cf434-122">Die Adressen in diesem Thema dienen nur zum Beispiel.</span><span class="sxs-lookup"><span data-stu-id="cf434-122">The addresses in this topic are for example only.</span></span> <span data-ttu-id="cf434-123">Sie müssen IPv6-Adressen erwerben, die in Ihrer Bereitstellung funktionieren, den korrekten Bereich bereitstellen und mit interner und externer Adressierung interagieren.</span><span class="sxs-lookup"><span data-stu-id="cf434-123">You must acquire IPv6 addresses that will function in your deployment, provide the correct scope and will interoperate with internal and external addressing.</span></span> <span data-ttu-id="cf434-124">Windows Server bietet ein Feature, das für den Übergangs-IPv6-Betrieb und die IPv4-zu-IPv6-Kommunikation, die so genannte *Dual Stack*, wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="cf434-124">Windows Server provides a feature that is important to transitional IPv6 operation and IPv4 to IPv6 communication called the *dual stack*.</span></span> <span data-ttu-id="cf434-125">Der Dual Stack ist ein separater und unterschiedlicher Netzwerkstapel für IPv4 und für IPv6.</span><span class="sxs-lookup"><span data-stu-id="cf434-125">The dual stack is a separate and distinct network stack for IPv4 and for IPv6.</span></span> <span data-ttu-id="cf434-126">Mit dem Dual Stack können Sie die Adressierung für IPv4 und IPv6 gleichzeitig zuweisen und dem Server die Kommunikation mit anderen Hosts und Clients auf der Grundlage Ihrer Anforderungen ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="cf434-126">The dual stack is what allows you to assign addressing for IPv4 and IPv6 concurrently, and allows the server to communicate with other hosts and clients based on what their requirements are.</span></span>

<span data-ttu-id="cf434-127">Typische Adresstypen, die Sie für die IPv6-Adressierung verwenden werden, sind die globalen IPv6-Adressen (ähnlich wie öffentliche IPv4-Adressen), eindeutige IPv6-lokale Adressen (ähnlich den privaten IPv4-Adressbereichen) und IPv6-Link-Local-Adressen (ähnlich wie automatische private IP-Adressen in Windows Server für IPv4).</span><span class="sxs-lookup"><span data-stu-id="cf434-127">Typical address types that you will use for IPv6 addressing will be the IPv6 global addresses (similar to public IPv4 addresses), IPv6 unique local addresses (similar to the private IPv4 address ranges) and IPv6 link-local addresses (similar to automatic private IP addresses in Windows Server for IPv4)</span></span>

<span data-ttu-id="cf434-128">Netzwerkadressübersetzung-Technologien (NAT) für IPv6 sind vorhanden, die für NAT IPv6 zu IPv4 (gemeinhin als NAT64 bezeichnet) und für NAT IPv6 zu IPv6 (gemeinhin als NAT66 bezeichnet) zugelassen sind.</span><span class="sxs-lookup"><span data-stu-id="cf434-128">Network address translation technologies (NAT) for IPv6 exist that will allow for NAT IPv6 to IPv4 (commonly referred to as NAT64) and for NAT IPv6 to IPv6 (commonly referred to as NAT66).</span></span> <span data-ttu-id="cf434-129">Das vorhanden sein von NAT-Technologien bedeutet, dass die fünf Szenarien, die für lync Server-Edgeserver bereitgestellt werden, weiterhin gültig sind.</span><span class="sxs-lookup"><span data-stu-id="cf434-129">The existence of NAT technologies means that the five scenarios presented for Lync Server Edge Servers are still valid.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="cf434-130">IPv6 ist ein komplexes Thema und erfordert eine sorgfältige Planung mit Ihrem Netzwerkteam und Ihrem Internet Anbieter, um sicherzustellen, dass die Adressen, die Sie auf der Windows-Serverebene und auf der lync Server 2013-Ebene zuweisen, wie erwartet funktionieren.</span><span class="sxs-lookup"><span data-stu-id="cf434-130">IPv6 is a complex topic and requires careful planning with your networking team and your Internet provider to ensure that the addresses you assign at the Windows server level and at the Lync Server 2013 level will work as expected.</span></span> <span data-ttu-id="cf434-131">Zusätzliche Informationen zur IPv6-Adressierung und -Planung finden Sie über die Links am Ende dieses Themas.</span><span class="sxs-lookup"><span data-stu-id="cf434-131">See the links at the end of this topic for additional resources on IPv6 addressing and planning.</span></span>



</div>

<span data-ttu-id="cf434-132">![899546d4-2eef-44d2-8317-51c5f699cd2a](images/Gg398823.899546d4-2eef-44d2-8317-51c5f699cd2a(OCS.15).jpg "899546d4-2eef-44d2-8317-51c5f699cd2a")</span><span class="sxs-lookup"><span data-stu-id="cf434-132">![899546d4-2eef-44d2-8317-51c5f699cd2a](images/Gg398823.899546d4-2eef-44d2-8317-51c5f699cd2a(OCS.15).jpg "899546d4-2eef-44d2-8317-51c5f699cd2a")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="cf434-133">Wenn Sie die Anrufsteuerung (Call Admission Control, CAC) verwenden, müssen Sie der Edge-Server-internen Schnittstelle weiterhin IPv4-Adressen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="cf434-133">If you are using Call Admission Control (CAC), you still must assign IPv4 addresses to the Edge Server internal interface.</span></span> <span data-ttu-id="cf434-134">CAC verwendet IPv4-Adressen und muss für den Betrieb zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="cf434-134">CAC uses IPv4 addresses and must have them available to operate.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="cf434-135">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="cf434-135">In This Section</span></span>

  - [<span data-ttu-id="cf434-136">Zertifikatzusammenfassung für einen skalierten konsolidierten Edgeserver, DNS-Lastenausgleich mit privaten IP-Adressen und NAT in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf434-136">Certificate summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-consolidated-edge-dns-load-balancing-private-ip.md)

  - [<span data-ttu-id="cf434-137">Portzusammenfassung für einen skalierten konsolidierten Edgeserver, DNS-Lastenausgleich mit privaten IP-Adressen und NAT in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf434-137">Port summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-port-summary-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md)

  - [<span data-ttu-id="cf434-138">DNS-Zusammenfassung für einen skalierten konsolidierten Edgeserver, DNS-Lastenausgleich mit privaten IP-Adressen und NAT in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cf434-138">DNS summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-dns-summary-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="cf434-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cf434-139">See Also</span></span>


[<span data-ttu-id="cf434-140">IP Version 6-Adressierungs Architektur</span><span class="sxs-lookup"><span data-stu-id="cf434-140">IP Version 6 Addressing Architecture</span></span>](https://tools.ietf.org/html/rfc4291)  
[<span data-ttu-id="cf434-141">Globales IPv6-Unicast-Adress Format</span><span class="sxs-lookup"><span data-stu-id="cf434-141">IPv6 Global Unicast Address Format</span></span>](https://tools.ietf.org/html/rfc3587)  
[<span data-ttu-id="cf434-142">Eindeutige lokale IPv6-Unicast-Adressen</span><span class="sxs-lookup"><span data-stu-id="cf434-142">Unique Local IPv6 Unicast Addresses</span></span>](https://tools.ietf.org/html/rfc4193)  
  

<span data-ttu-id="cf434-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cf434-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

