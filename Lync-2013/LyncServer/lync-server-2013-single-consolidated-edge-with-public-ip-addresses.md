---
title: 'Lync Server 2013: Einzelner konsolidierter Edgeserver mit öffentlichen IP-Adressen'
description: 'Lync Server 2013: einzelner konsolidierter Edge mit öffentlichen IP-Adressen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Single consolidated edge with public IP addresses
ms:assetid: a92d1179-6a1f-4efe-908a-f8dfc5024f30
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205148(v=OCS.15)
ms:contentKeyID: 48185035
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ac829cd15a592a86d2ba5fdfe174703d0c933037
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423858"
---
# <a name="single-consolidated-edge-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="892d0-103">Einzelner konsolidierter Edgeserver mit öffentlichen IP-Adressen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="892d0-103">Single consolidated edge with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="892d0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="892d0-104">

<span> </span></span></span>

<span data-ttu-id="892d0-105">_**Letztes Änderungsdatum des Themas:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="892d0-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="892d0-106">Wenn Ihre Organisation Unterstützung für weniger als 15.000-Access-Edgedienst-Clientverbindungen, 1.000 Active lync Server-Webkonferenzdienst-Clientverbindungen und 500 gleichzeitige A/V-Edge-Sitzungen und eine höhere Verfügbarkeit des Edgeserver benötigt, bietet diese Topologie die Vorteile der niedrigeren Hardwarekosten und der einfacheren Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="892d0-106">If your organization needs support for fewer than 15,000 Access Edge service client connections, 1,000 active Lync Server Web Conferencing service client connections, and 500 concurrent A/V Edge sessions, and high availability of the Edge Server is not important, this topology offers the advantages of lower hardware cost and simpler deployment.</span></span> <span data-ttu-id="892d0-107">Wenn Sie eine größere Kapazität benötigen oder eine hohe Verfügbarkeit benötigen, sollten Sie eine skalierte konsolidierte Edgeserver-Topologie bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="892d0-107">If you need greater capacity or you require high availability, you should deploy a scaled consolidated Edge Server topology.</span></span>

  - <span></span>  
    [<span data-ttu-id="892d0-108">Skalierter konsolidierter Edgeserver, DNS-Lastenausgleich mit privaten IP-Adressen und NAT in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="892d0-108">Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md)

  - <span></span>  
    [<span data-ttu-id="892d0-109">Skalierter konsolidierter Edgeserver, DNS-Lastenausgleich mit öffentlichen IP-Adressen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="892d0-109">Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)

  - <span></span>  
    [<span data-ttu-id="892d0-110">Skalierter konsolidierter Edgeserver mit Hardwarelastenausgleich in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="892d0-110">Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md)

<div>


> [!IMPORTANT]  
> <span data-ttu-id="892d0-111">Wenn Sie die öffentliche IP-Adresse auf dem Edgeserver verwenden, ist das Standardgateway auf dem Edgeserver nicht mehr Ihre Firewall oder Ihr Router, sondern der Router oder die Firewall an Ihrem öffentlichen Perimeter-Rand – eine öffentliche Adresse.</span><span class="sxs-lookup"><span data-stu-id="892d0-111">When using public IP address on the Edge Server, the default gateway on the Edge Server is no longer your firewall or router, but the router or firewall at your public perimeter edge – which will be a public address.</span></span> <span data-ttu-id="892d0-112">Der Reverse-Proxy verwendet weiterhin den Router oder die Firewall, der dem äußersten Umkreisnetzwerk zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="892d0-112">The reverse proxy continues to use the router or firewall associated with the outermost perimeter network.</span></span> <span data-ttu-id="892d0-113">Der Unterschied zwischen dem Reverse-Proxy und dem Edgeserver mit öffentlichen IP-Adressen besteht darin, dass der Reverse-Proxy weiterhin NAT verwendet und der Edgeserver eine Routenbeziehung verwendet.</span><span class="sxs-lookup"><span data-stu-id="892d0-113">The difference between the reverse proxy and the Edge Server with public IP addresses is that the reverse proxy is still using NAT and the Edge Server is using a route relationship.</span></span>



</div>

<span data-ttu-id="892d0-114">Die Abbildung zeigt keine Directors, eine optionale Serverrolle, die im internen Netzwerk zwischen den Edgeserver und ihren Front-End-Pools oder-Servern bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="892d0-114">The figure does not show Directors, an optional server role deployed in the internal network between the Edge Servers and your Front End pools or server.</span></span> <span data-ttu-id="892d0-115">Details zur Topologie für Directors finden Sie unter [für den Director in lync Server 2013 erforderliche Komponenten](lync-server-2013-components-required-for-the-director.md).</span><span class="sxs-lookup"><span data-stu-id="892d0-115">For details about the topology for Directors, see [Components required for the Director in Lync Server 2013](lync-server-2013-components-required-for-the-director.md).</span></span> <span data-ttu-id="892d0-116">Die Abbildung stellt einen einzelnen Reverse-Proxy dar.</span><span class="sxs-lookup"><span data-stu-id="892d0-116">The figure represents a single reverse proxy.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="892d0-117">Die angezeigte Abbildung dient zur Orientierung und zum Beispiel für die IP-Adressierung, beabsichtigt aber nicht, tatsächliche Kommunikationsflüsse mit dem korrekten ein-und ausgehenden Datenverkehr darzustellen.</span><span class="sxs-lookup"><span data-stu-id="892d0-117">The figure shown is for orientation and example IP addressing, but does not intend to represent actual communication flows with the correct incoming and outgoing traffic.</span></span> <span data-ttu-id="892d0-118">Die Abbildung stellt eine Ansicht des möglichen Datenverkehrs auf hoher Ebene dar.</span><span class="sxs-lookup"><span data-stu-id="892d0-118">The figure represents a high level view of possible traffic.</span></span> <span data-ttu-id="892d0-119">Details für den Datenverkehrs Fluss in Bezug auf eingehende (zu hörende Ports) und ausgehende (an Zielserver oder-Clients) werden in den einzelnen Szenarien im Diagramm Port Zusammenfassung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="892d0-119">Details for traffic flow as they pertain to incoming (to listening ports) and outgoing (to destination servers or clients) is represented in the Port Summary diagram in each scenario.</span></span> <span data-ttu-id="892d0-120">TCP 443 ist beispielsweise eigentlich nur eingehend (zum Edge-oder Reverse-Proxy) und ist nur ein bidirektionaler Fluss aus einer Protokoll (TCP)-Perspektive.</span><span class="sxs-lookup"><span data-stu-id="892d0-120">For example, TCP 443 is actually inbound (to the Edge or reverse proxy) only, and is only a two-way flow from a protocol (TCP) perspective.</span></span> <span data-ttu-id="892d0-121">Darüber hinaus zeigt die Abbildung die Art des Datenverkehrs an, wenn die NAT (Netzwerkadressübersetzung) Eintritt (die Zieladresse wird bei der eingehenden Änderung geändert, die Quelladresse wird beim ausgehen geändert).</span><span class="sxs-lookup"><span data-stu-id="892d0-121">Additionally, the figure shows the nature of traffic as it changes when NAT (network address translation) occurs (destination address is changed on inbound, source address is changed on outbound).</span></span> <span data-ttu-id="892d0-122">Beispiel für externe und interne Firewalls und Serverschnittstellen werden nur zu Referenzzwecken angezeigt.</span><span class="sxs-lookup"><span data-stu-id="892d0-122">Example external and internal firewall, and server interfaces are shown for reference purposes only.</span></span> <span data-ttu-id="892d0-123">Schließlich werden beispielsweise Standard-Gateway-und-Routen Beziehungen angezeigt, sofern zutreffend.</span><span class="sxs-lookup"><span data-stu-id="892d0-123">Finally, example default gateway and route relationships are shown, where applicable.</span></span> <span data-ttu-id="892d0-124">Beachten Sie auch, dass das Diagramm die DNS-Zone " <EM>. com</EM> " verwendet, um die externe DNS-Zone für Reverse-Proxy-und Edgeserver darzustellen, und die <EM>.net</EM> -DNS-Zone bezieht sich auf die interne DNS-Zone.</span><span class="sxs-lookup"><span data-stu-id="892d0-124">Note also that the diagram uses the <EM>.com</EM> DNS zone to represent the external DNS zone for both reverse proxy and Edge Servers, and the <EM>.net</EM> DNS zone refers to the internal DNS zone.</span></span>



</div>

<span data-ttu-id="892d0-125">Neu bei Microsoft lync Server 2013 ist die Unterstützung für die IPv6-Adressierung.</span><span class="sxs-lookup"><span data-stu-id="892d0-125">New to Microsoft Lync Server 2013 is support for IPv6 addressing.</span></span> <span data-ttu-id="892d0-126">Ähnlich wie bei der IPv4-Adressierung müssen IPv6-Adressen so zugewiesen werden, dass die Adressenteil des zugewiesenen IPv6-Adressraums sind.</span><span class="sxs-lookup"><span data-stu-id="892d0-126">Much like IPv4 addressing, IPv6 addresses must be assigned in such a way that the addresses are part of your assigned IPv6 address space.</span></span> <span data-ttu-id="892d0-127">Die Adressen in diesem Thema dienen nur zum Beispiel.</span><span class="sxs-lookup"><span data-stu-id="892d0-127">The addresses in this topic are for example only.</span></span> <span data-ttu-id="892d0-128">Sie müssen IPv6-Adressen erwerben, die in Ihrer Bereitstellung funktionieren, den korrekten Bereich bereitstellen und mit interner und externer Adressierung interagieren.</span><span class="sxs-lookup"><span data-stu-id="892d0-128">You must acquire IPv6 addresses that will function in your deployment, provide the correct scope and will interoperate with internal and external addressing.</span></span> <span data-ttu-id="892d0-129">Windows Server bietet ein Feature, das für den Übergangs-IPv6-Betrieb und die IPv4-zu-IPv6-Kommunikation, die so genannte *Dual Stack*, wichtig ist.</span><span class="sxs-lookup"><span data-stu-id="892d0-129">Windows Server provides a feature that is important to transitional IPv6 operation and IPv4 to IPv6 communication called the *dual stack*.</span></span> <span data-ttu-id="892d0-130">Der Dual Stack ist ein separater und unterschiedlicher Netzwerkstapel für IPv4 und für IPv6.</span><span class="sxs-lookup"><span data-stu-id="892d0-130">The dual stack is a separate and distinct network stack for IPv4 and for IPv6.</span></span> <span data-ttu-id="892d0-131">Mit dem Dual Stack können Sie die Adressierung für IPv4 und IPv6 gleichzeitig zuweisen und dem Server die Kommunikation mit anderen Hosts und Clients auf der Grundlage Ihrer Anforderungen ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="892d0-131">The dual stack is what allows you to assign addressing for IPv4 and IPv6 concurrently, and allows the server to communicate with other hosts and clients based on what their requirements are.</span></span>

<span data-ttu-id="892d0-132">Typische Adresstypen, die Sie für die IPv6-Adressierung verwenden werden, sind die globalen IPv6-Adressen (ähnlich wie öffentliche IPv4-Adressen), eindeutige IPv6-lokale Adressen (ähnlich den privaten IPv4-Adressbereichen) und IPv6-Link-Local-Adressen (ähnlich wie automatische private IP-Adressen in Windows Server für IPv4).</span><span class="sxs-lookup"><span data-stu-id="892d0-132">Typical address types that you will use for IPv6 addressing will be the IPv6 global addresses (similar to public IPv4 addresses), IPv6 unique local addresses (similar to the private IPv4 address ranges) and IPv6 link-local addresses (similar to automatic private IP addresses in Windows Server for IPv4)</span></span>

<span data-ttu-id="892d0-133">Netzwerkadressübersetzung-Technologien (NAT) für IPv6 sind vorhanden, die für NAT IPv6 zu IPv4 (gemeinhin als NAT64 bezeichnet) und für NAT IPv6 zu IPv6 (gemeinhin als NAT66 bezeichnet) zugelassen sind.</span><span class="sxs-lookup"><span data-stu-id="892d0-133">Network address translation technologies (NAT) for IPv6 exist that will allow for NAT IPv6 to IPv4 (commonly referred to as NAT64) and for NAT IPv6 to IPv6 (commonly referred to as NAT66).</span></span> <span data-ttu-id="892d0-134">Das vorhanden sein von NAT-Technologien bedeutet, dass die fünf Szenarien, die für lync Server-Edgeserver bereitgestellt werden, weiterhin gültig sind.</span><span class="sxs-lookup"><span data-stu-id="892d0-134">The existence of NAT technologies means that the five scenarios presented for Lync Server Edge Servers are still valid.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="892d0-135">IPv6 ist ein komplexes Thema und erfordert eine sorgfältige Planung mit Ihrem Netzwerkteam und Ihrem Internet Anbieter, um sicherzustellen, dass die Adressen, die Sie auf der Windows-Serverebene und auf der lync Server 2013-Ebene zuweisen, wie erwartet funktionieren.</span><span class="sxs-lookup"><span data-stu-id="892d0-135">IPv6 is a complex topic and requires careful planning with your networking team and your Internet provider to ensure that the addresses you assign at the Windows server level and at the Lync Server 2013 level will work as expected.</span></span> <span data-ttu-id="892d0-136">Zusätzliche Informationen zur IPv6-Adressierung und -Planung finden Sie über die Links am Ende dieses Themas.</span><span class="sxs-lookup"><span data-stu-id="892d0-136">See the links at the end of this topic for additional resources on IPv6 addressing and planning.</span></span>



</div>

<span data-ttu-id="892d0-137">**Einzelner konsolidierter Edge mit Topologie öffentlicher IP-Adressen**</span><span class="sxs-lookup"><span data-stu-id="892d0-137">**Single Consolidated Edge with Public IP Addresses topology**</span></span>

<span data-ttu-id="892d0-138">![2db9f9e1-75aa-4de0-ab3f-c6effddb4f4d](images/JJ205148.2db9f9e1-75aa-4de0-ab3f-c6effddb4f4d(OCS.15).jpg "2db9f9e1-75aa-4de0-ab3f-c6effddb4f4d")</span><span class="sxs-lookup"><span data-stu-id="892d0-138">![2db9f9e1-75aa-4de0-ab3f-c6effddb4f4d](images/JJ205148.2db9f9e1-75aa-4de0-ab3f-c6effddb4f4d(OCS.15).jpg "2db9f9e1-75aa-4de0-ab3f-c6effddb4f4d")</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="892d0-139">Wenn Sie die Anrufsteuerung (Call Admission Control, CAC) verwenden, müssen Sie der Edge-Server-internen Schnittstelle weiterhin IPv4-Adressen zuweisen.</span><span class="sxs-lookup"><span data-stu-id="892d0-139">If you are using Call Admission Control (CAC), you still must assign IPv4 addresses to the Edge Server internal interface.</span></span> <span data-ttu-id="892d0-140">CAC verwendet IPv4-Adressen und muss für den Betrieb zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="892d0-140">CAC uses IPv4 addresses and must have them available to operate.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="892d0-141">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="892d0-141">In This Section</span></span>

  - [<span data-ttu-id="892d0-142">Zertifikatzusammenfassung für einen einzelnen konsolidierten Edgeserver mit öffentlichen IP-Adressen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="892d0-142">Certificate summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-single-consolidated-edge-with-public-ip-addresses.md)

  - [<span data-ttu-id="892d0-143">Portzusammenfassung für einen einzelnen konsolidierten Edgeserver mit öffentlichen IP-Adressen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="892d0-143">Port summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-port-summary-single-consolidated-edge-with-public-ip-addresses.md)

  - [<span data-ttu-id="892d0-144">DNS-Zusammenfassung für einen einzelnen konsolidierten Edgeserver mit öffentlichen IP-Adressen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="892d0-144">DNS summary - Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-dns-summary-single-consolidated-edge-with-public-ip-addresses.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="892d0-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="892d0-145">See Also</span></span>


[<span data-ttu-id="892d0-146">IP Version 6-Adressierungs Architektur</span><span class="sxs-lookup"><span data-stu-id="892d0-146">IP Version 6 Addressing Architecture</span></span>](https://tools.ietf.org/html/rfc4291)  
[<span data-ttu-id="892d0-147">Globales IPv6-Unicast-Adress Format</span><span class="sxs-lookup"><span data-stu-id="892d0-147">IPv6 Global Unicast Address Format</span></span>](https://tools.ietf.org/html/rfc3587)  
[<span data-ttu-id="892d0-148">Eindeutige lokale IPv6-Unicast-Adressen</span><span class="sxs-lookup"><span data-stu-id="892d0-148">Unique Local IPv6 Unicast Addresses</span></span>](https://tools.ietf.org/html/rfc4193)  
  

<span data-ttu-id="892d0-149"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="892d0-149"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

