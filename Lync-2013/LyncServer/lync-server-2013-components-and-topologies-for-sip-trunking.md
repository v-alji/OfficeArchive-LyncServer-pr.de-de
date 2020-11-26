---
title: 'Lync Server 2013: Komponenten und Topologien für das SIP-Trunking'
description: 'Lync Server 2013: Komponenten und Topologien für SIP-Trunking.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components and topologies for SIP trunking
ms:assetid: 8ed9a9d0-517e-4f36-a131-22cdafa257fa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398720(v=OCS.15)
ms:contentKeyID: 48184775
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f9d9c826539084a539d3efe7f143c335ec6d8f62
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434574"
---
# <a name="components-and-topologies-for-sip-trunking-in-lync-server-2013"></a><span data-ttu-id="ab56d-103">Komponenten und Topologien für das SIP-Trunking in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ab56d-103">Components and topologies for SIP trunking in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ab56d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ab56d-104">

<span> </span></span></span>

<span data-ttu-id="ab56d-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="ab56d-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="ab56d-106">Die folgende Abbildung zeigt die SIP-Trunking-Topologie in lync Server.</span><span class="sxs-lookup"><span data-stu-id="ab56d-106">The following figure depicts the SIP trunking topology in Lync Server.</span></span>

<span data-ttu-id="ab56d-107">**SIP-Trunking-Topologie**</span><span class="sxs-lookup"><span data-stu-id="ab56d-107">**SIP trunking topology**</span></span>

<span data-ttu-id="ab56d-108">![Topologie für das SIP-Trunking](images/Gg398720.669fb55d-7c81-4e21-9421-fabc43d6e064(OCS.15).jpg "Topologie für das SIP-Trunking")</span><span class="sxs-lookup"><span data-stu-id="ab56d-108">![SIP Trunking Topology](images/Gg398720.669fb55d-7c81-4e21-9421-fabc43d6e064(OCS.15).jpg "SIP Trunking Topology")</span></span>

<span data-ttu-id="ab56d-p101">Wie in der Abbildung gezeigt wird das virtuelle private IP-Netzwerk (IP-VPN) für die Verbindungen zwischen dem Unternehmensnetzwerk und dem PSTN (Public Switched Telephone Network, Telefonfestnetz)-Dienstanbieter verwendet. Mit diesem privaten Netzwerk sollen IP-Verbindungen, erweiterte Sicherheit und (optional) Garantien für die Dienstqualität (Quality of Service, QoS) geboten werden. Aufgrund der Merkmale eines VPNs ist es nicht erforderlich, Transport Layer Security (TLS) für den SIP-Signaldatenverkehr oder Secure Real-Time Transport Protocol (SRTP) für den Mediendatenverkehr zu verwenden. Die Verbindungen zwischen dem Unternehmen und dem Dienstanbieter bestehen deshalb aus einfachen TCP-Verbindungen für SIP-Datenverkehr und einfachen Real-Time Transport Protocol (RTP)-Verbindungen (über UDP) für Mediendatenverkehr, der durch ein IP-VPN getunnelt werden kann. Stellen Sie sicher, dass alle Firewalls zwischen den VPN-Routern offene Ports aufweisen, damit die VPN-Router kommunizieren können. Zudem müssen die IP-Adressen der externen Edgeschnittstellen der VPN-Router öffentlich routingfähig sein.</span><span class="sxs-lookup"><span data-stu-id="ab56d-p101">As shown in the diagram, an IP virtual private network (VPN) is used for connectivity between the enterprise network and the public switched telephone network (PSTN) service provider. The purpose of this private network is to provide IP connectivity, enhance security, and (optionally) obtain Quality of Service (QoS) guarantees. Because of the nature of a VPN, you do not need to use Transport Layer Security (TLS) for SIP signaling traffic or secure real-time transport protocol (SRTP) for the media traffic. Connections between the enterprise and the service provider therefore consist of plain TCP connections for SIP and plain real-time transport protocol (RTP) (over UDP) for media tunneled through an IP VPN. Ensure that all firewalls between the VPN routers have ports open to allow the VPN routers to communicate, and that the IP addresses on the external edges of the VPN routers are publicly routable.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ab56d-114">Kontaktieren Sie Ihren Dienstanbieter, um zu ermitteln, ob er Unterstützung für hohe Verfügbarkeit (einschließlich Failover) bietet.</span><span class="sxs-lookup"><span data-stu-id="ab56d-114">Contact your service provider to determine whether it provides support for high availability, including failover.</span></span> <span data-ttu-id="ab56d-115">Wenn ja, müssen Sie die erforderlichen Vorgehensweisen zum Einrichten von hoher Verfügbarkeit ermitteln.</span><span class="sxs-lookup"><span data-stu-id="ab56d-115">If so, you will need to determine the procedures for setting it up.</span></span> <span data-ttu-id="ab56d-116">Müssen Sie beispielsweise nur eine IP-Adresse und einen SIP-Trunk auf jedem Vermittlungsserver konfigurieren, oder müssen mehrere SIP-Stämme auf jedem Vermittlungsserver konfiguriert werden?</span><span class="sxs-lookup"><span data-stu-id="ab56d-116">For example, do you need to configure only one IP address and one SIP trunk on each Mediation Server, or do you need to configure multiple SIP trunks on each Mediation Server?</span></span><BR><span data-ttu-id="ab56d-117">Wenn Sie über mehrere zentrale Websites verfügen, Fragen Sie auch, ob der Dienstanbieter Verbindungen zu und von einem anderen zentralen Standort aus aktivieren kann.</span><span class="sxs-lookup"><span data-stu-id="ab56d-117">If you have multiple central sites, also ask whether the service provider has the ability to enable connections to and from another central site.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="ab56d-118">Für SIP-Trunking empfehlen wir dringend, eigenständige Vermittlungsserver bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="ab56d-118">For SIP trunking, we strongly recommend that you deploy stand-alone Mediation Servers.</span></span> <span data-ttu-id="ab56d-119">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-deploying-mediation-servers-and-defining-peers.md">Bereitstellen von Vermittlungsservern und Definieren von Peers in lync Server 2013</A> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="ab56d-119">For details, see <A href="lync-server-2013-deploying-mediation-servers-and-defining-peers.md">Deploying Mediation Servers and defining peers in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="securing-the-mediation-server-for-sip-trunking"></a><span data-ttu-id="ab56d-120">Schützen des Vermittlungsservers für das SIP-Trunking</span><span class="sxs-lookup"><span data-stu-id="ab56d-120">Securing the Mediation Server for SIP Trunking</span></span>

<span data-ttu-id="ab56d-p104">Aus Sicherheitsgründen sollten Sie ein virtuelles LAN (VLAN) für jede Verbindung zwischen den zwei VPN-Routern einrichten. Die tatsächliche Vorgehensweise zum Einrichten eines VLANs variiert abhängig vom Routerhersteller. Ausführliche Informationen erhalten Sie von Ihrem Routeranbieter.</span><span class="sxs-lookup"><span data-stu-id="ab56d-p104">For security purposes, you should set up a virtual LAN (VLAN) for each connection between the two VPN routers. The actual process for setting up a VLAN varies from one router manufacturer to another. For details, contact your router vendor.</span></span>

<span data-ttu-id="ab56d-124">Sie sollten die folgenden Richtlinie befolgen:</span><span class="sxs-lookup"><span data-stu-id="ab56d-124">We recommend that you follow these guidelines:</span></span>

  - <span data-ttu-id="ab56d-125">Einrichten eines virtuellen LANs (VLAN) zwischen dem Vermittlungs Server und dem VPN-Router im Umkreisnetzwerk (auch bekannt als DMZ, demilitarisierte Zone und geschirmtes Subnetz).</span><span class="sxs-lookup"><span data-stu-id="ab56d-125">Set up a virtual LAN (VLAN) between the Mediation Server and the VPN router in the perimeter network (also known as DMZ, demilitarized zone, and screened subnet).</span></span>

  - <span data-ttu-id="ab56d-126">Lassen Sie keine Übertragung von Broadcast- oder Multicastpaketen vom Router in das VLAN zu.</span><span class="sxs-lookup"><span data-stu-id="ab56d-126">Do not allow broadcast or multicast packets to be transferred from the router to the VLAN.</span></span>

  - <span data-ttu-id="ab56d-127">Blockieren Sie Routingregeln, die den Datenverkehr vom Router an eine beliebige Stelle, aber auf den Vermittlungs Server weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="ab56d-127">Block any routing rules that route traffic from the router to anywhere but the Mediation Server.</span></span>

<span data-ttu-id="ab56d-128">Bei Verwendung eines VPN-Servers sollten Sie die folgenden Richtlinien befolgen:</span><span class="sxs-lookup"><span data-stu-id="ab56d-128">If you use a VPN server, we recommend that you follow these guidelines:</span></span>

  - <span data-ttu-id="ab56d-129">Einrichten eines VLAN zwischen dem VPN-Server und dem Vermittlungsserver</span><span class="sxs-lookup"><span data-stu-id="ab56d-129">Set up a VLAN between the VPN server and the Mediation Server.</span></span>

  - <span data-ttu-id="ab56d-130">Lassen Sie keine Übertragung von Broadcast- oder Multicastpaketen vom VPN-Server in das VLAN zu.</span><span class="sxs-lookup"><span data-stu-id="ab56d-130">Do not allow broadcast or multicast packets to be transmitted from the VPN server to the VLAN.</span></span>

  - <span data-ttu-id="ab56d-131">Blockieren Sie jede Routingregel, die den VPN-Server Datenverkehr an eine beliebige Stelle, aber den Vermittlungsserver weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="ab56d-131">Block any routing rule that routes VPN server traffic to anywhere but the Mediation Server.</span></span>

  - <span data-ttu-id="ab56d-132">Verschlüsseln Sie Daten im VPN mithilfe von GRE (Generic Routing Encapsulation).</span><span class="sxs-lookup"><span data-stu-id="ab56d-132">Encrypt data on the VPN by using generic routing encapsulation (GRE).</span></span>

<span data-ttu-id="ab56d-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ab56d-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

