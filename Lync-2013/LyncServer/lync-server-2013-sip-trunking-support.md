---
title: 'Lync Server 2013: SIP-Trunking-Unterstützung'
description: Lync Server 2013 SIP-Trunking-Unterstützung.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SIP trunking support
ms:assetid: e3042831-e8d8-4ea2-baa2-1a697401ffa0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399005(v=OCS.15)
ms:contentKeyID: 48185714
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 427e573d88584ac8beb3bbcd54e68b13c4c42f0f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444630"
---
# <a name="sip-trunking-support-in-lync-server-2013"></a><span data-ttu-id="d08ca-103">SIP-Trunking-Unterstützung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d08ca-103">SIP trunking support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d08ca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d08ca-104">

<span> </span></span></span>

<span data-ttu-id="d08ca-105">_**Letztes Änderungsdatum des Themas:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="d08ca-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="d08ca-106">Wenn Sie Enterprise-VoIP mit SIP-Trunking verwenden möchten, müssen Sie einen Vermittlungs Server bereitstellen und sicherstellen, dass andere Infrastrukturen und Komponenten die für Ihr Bereitstellungsmodell geeigneten Supportanforderungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="d08ca-106">If you plan to use Enterprise Voice with SIP trunking, you must deploy a Mediation Server and make sure that other infrastructure and components meet the support requirements appropriate to your deployment model.</span></span> <span data-ttu-id="d08ca-107">Details zum ermitteln, ob SIP-Trunking implementiert werden soll, finden Sie unter [Übersicht über SIP-Trunking in lync Server 2013](lync-server-2013-overview-of-sip-trunking.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="d08ca-107">For details about determining whether to implement SIP trunking, see [Overview of SIP trunking in Lync Server 2013](lync-server-2013-overview-of-sip-trunking.md) in the Planning documentation.</span></span>

<span data-ttu-id="d08ca-108">Sie können das offene Interoperabilitäts Programm Microsoft Unified Communications für die Enterprise-Telefonie-Infrastruktur verwenden, um qualifizierte PSTN-Gateways (Public Switched Telephone Network), IP-PBX-Anlagen und SIP-Trunking-Dienste zu finden, einschließlich qualifizierter IP-Telefondienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d08ca-108">You can use the Microsoft Unified Communications Open Interoperability Program for enterprise telephony infrastructure to find qualified public switched telephone network (PSTN) gateways, IP-PBXs, and SIP trunking services, including qualified IP telephony service providers.</span></span> <span data-ttu-id="d08ca-109">Ausführliche Informationen finden Sie auf der Microsoft Unified Communications Open Interoperability Program-Website unter [https://go.microsoft.com/fwlink/p/?LinkId=203309](https://go.microsoft.com/fwlink/p/?linkid=203309) .</span><span class="sxs-lookup"><span data-stu-id="d08ca-109">For details, see the Microsoft Unified Communications Open Interoperability Program website at [https://go.microsoft.com/fwlink/p/?LinkId=203309](https://go.microsoft.com/fwlink/p/?linkid=203309).</span></span>

<div>

## <a name="mediation-server-support"></a><span data-ttu-id="d08ca-110">Vermittlungs Server Unterstützung</span><span class="sxs-lookup"><span data-stu-id="d08ca-110">Mediation Server Support</span></span>

<span data-ttu-id="d08ca-111">Um SIP-Trunking zu implementieren, müssen Sie die Verbindung über einen Vermittlungs Server weiterleiten, der als Proxy für Kommunikationssitzungen zwischen lync Server 2013-Clients und dem Dienstanbieter fungiert.</span><span class="sxs-lookup"><span data-stu-id="d08ca-111">To implement SIP trunking, you must route the connection through a Mediation Server, which acts as a proxy for communications sessions between Lync Server 2013 clients and the service provider.</span></span> <span data-ttu-id="d08ca-112">Der Vermittlungs Server dekodiert den Mediendatenverkehr von Clients und Servern und codiert ihn erneut, bevor er an den Dienstanbieter gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="d08ca-112">The Mediation Server decodes the media traffic from clients and servers and re-encodes it before sending it to the service provider.</span></span> <span data-ttu-id="d08ca-113">Die erneute Codierung ist erforderlich, da SIP-Trunks einige verwendete Codecs nicht unterstützen, wie etwa Echtzeit-Audio (RTA) oder Interaktions Einrichtung (ICE) Protocol Negotiation für die Firewall-Durchquerung.</span><span class="sxs-lookup"><span data-stu-id="d08ca-113">The re-encoding is needed because SIP trunks do not support some codecs used, such as Real Time Audio (RTA) or Interactive Connectivity Establishment (ICE) protocol negotiation for firewall traversal.</span></span>

<span data-ttu-id="d08ca-114">Jeder Vermittlungs Server kann über zwei Netzwerkadapter verfügen, die eine interne und eine externe Netzwerkschnittstelle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d08ca-114">Each Mediation Server can have two network adapters, which provide an internal and an external network interface.</span></span> <span data-ttu-id="d08ca-115">Die externe Schnittstelle wird gemeinhin als Gateway-Schnittstelle bezeichnet, da Sie üblicherweise für die Verbindung mit einem PSTN-Gateway oder einer IP-PBX-Anlage verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d08ca-115">The external interface is commonly called the gateway interface because, traditionally, it has been used to connect to a PSTN gateway or an IP-PBX.</span></span> <span data-ttu-id="d08ca-116">Um einen SIP-Trunk zu implementieren, verbinden Sie die externe Schnittstelle mit einem Session Border Controller (SBC) bei einem Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="d08ca-116">To implement a SIP trunk, you connect the external interface to a Session Border Controller (SBC) at a service provider.</span></span>

</div>

<div>

## <a name="centralized-vs-distributed-sip-trunking"></a><span data-ttu-id="d08ca-117">Zentralisiertes und verteiltes SIP-Trunking im Vergleich</span><span class="sxs-lookup"><span data-stu-id="d08ca-117">Centralized vs. Distributed SIP Trunking</span></span>

<span data-ttu-id="d08ca-118">*Zentralisiert* SIP-Trunking leitet den gesamten VoIP-Datenverkehr (einschließlich Zweigstellen-Websitedatenverkehr) über Ihr Rechenzentrum weiter.</span><span class="sxs-lookup"><span data-stu-id="d08ca-118">*Centralized* SIP trunking routes all Voice over Internet Protocol (VoIP) traffic, including branch site traffic, through your data center.</span></span> <span data-ttu-id="d08ca-119">Das zentralisierte Bereitstellungsmodell ist einfach, kostengünstig und im Allgemeinen der bevorzugte Ansatz für die Implementierung von SIP-Stämmen mit lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="d08ca-119">The centralized deployment model is simple, cost-effective, and is generally the preferred approach for implementing SIP trunks with Lync Server 2013.</span></span>

<span data-ttu-id="d08ca-120">Je nach Verwendungsmustern in Ihrem Unternehmen möchten Sie möglicherweise nicht alle Benutzer über den zentralisierten SIP-Stamm weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="d08ca-120">Depending on usage patterns within your enterprise, you may not want to route all users through the centralized SIP trunk.</span></span> <span data-ttu-id="d08ca-121">Beantworten Sie zur Analyse Ihrer Anforderungen die folgenden Fragen:</span><span class="sxs-lookup"><span data-stu-id="d08ca-121">To analyze your needs, answer the following questions:</span></span>

  - <span data-ttu-id="d08ca-122">Wie groß ist jede Website?</span><span class="sxs-lookup"><span data-stu-id="d08ca-122">How big is each site?</span></span> <span data-ttu-id="d08ca-123">Wie viele Benutzer?</span><span class="sxs-lookup"><span data-stu-id="d08ca-123">How many users?</span></span>

  - <span data-ttu-id="d08ca-124">Welche direkten Durchwahlnummern (DID) an jedem Standort erhalten die meisten Telefonanrufe?</span><span class="sxs-lookup"><span data-stu-id="d08ca-124">Which Direct Inward Dialing (DID) numbers at each site get the most phone calls?</span></span>

<span data-ttu-id="d08ca-125">*Verteilte* SIP Trunking ist ein Bereitstellungsmodell, bei dem Sie einen lokalen SIP-Trunk an einer oder mehreren Zweigstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="d08ca-125">*Distributed* SIP trunking is a deployment model in which you implement a local SIP trunk at one or more branch sites.</span></span> <span data-ttu-id="d08ca-126">VoIP-Datenverkehr wird dann direkt von der Verzweigungs Website an Ihren Dienstanbieter weitergeleitet, ohne Ihr Rechenzentrum zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="d08ca-126">VoIP traffic is then routed from the branch site directly to their service provider, without going through your data center.</span></span>

<span data-ttu-id="d08ca-127">Ein verteiltes SIP-Trunking ist nur in den folgenden Fällen erforderlich:</span><span class="sxs-lookup"><span data-stu-id="d08ca-127">Distributed SIP trunking is required only in the following cases:</span></span>

  - <span data-ttu-id="d08ca-128">Die Verzweigungs Website erfordert eine überlebensfähige Telefonverbindung (beispielsweise, wenn das WAN ausfällt).</span><span class="sxs-lookup"><span data-stu-id="d08ca-128">The branch site requires survivable phone connectivity (for example, if the WAN goes down).</span></span> <span data-ttu-id="d08ca-129">Wenn für die Verzweigung Redundanz und Failover erforderlich sind, berechnet der Dienstanbieter mehr, und die Konfiguration wird länger dauern.</span><span class="sxs-lookup"><span data-stu-id="d08ca-129">If the branch does need redundancy and failover, the service provider will charge more and the configuration will take longer.</span></span> <span data-ttu-id="d08ca-130">Dies sollte für jede Verzweigungs Website analysiert werden.</span><span class="sxs-lookup"><span data-stu-id="d08ca-130">This should be analyzed for each branch site.</span></span> <span data-ttu-id="d08ca-131">Einige ihrer Zweigstellen erfordern möglicherweise Redundanz und Failover, während andere möglicherweise nicht.</span><span class="sxs-lookup"><span data-stu-id="d08ca-131">Some of your branches may require redundancy and failover, while others may not.</span></span>

  - <span data-ttu-id="d08ca-132">Die Verzweigungs Website und das Rechenzentrum befinden sich in verschiedenen Ländern/Regionen.</span><span class="sxs-lookup"><span data-stu-id="d08ca-132">The branch site and data center are in different countries/regions.</span></span> <span data-ttu-id="d08ca-133">Aus Kompatibilitäts-und rechtlichen Gründen benötigen Sie mindestens einen SIP-Trunk pro Land/Region.</span><span class="sxs-lookup"><span data-stu-id="d08ca-133">For compatibility and legal reasons, you need at least one SIP trunk per country/region.</span></span>

<span data-ttu-id="d08ca-134">Die Entscheidung, ob eine zentralisierte oder verteilte SIP-Trunkierung bereitgestellt werden soll, erfordert eine Kosten-Nutzen-Analyse.</span><span class="sxs-lookup"><span data-stu-id="d08ca-134">Deciding whether to deploy centralized or distributed SIP trunking requires a cost-benefit analysis.</span></span> <span data-ttu-id="d08ca-135">In einigen Fällen kann es vorteilhaft sein, den verteilten Bereitstellungsmodus zu wählen, auch wenn dies nicht erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="d08ca-135">In some cases, it may be advantageous to opt for the distributed deployment mode, even if it is not required.</span></span> <span data-ttu-id="d08ca-136">Bei einer vollständig zentralisierten Bereitstellung wird der gesamte Datenverkehr der Zweigstelle über WAN-Verbindungen weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="d08ca-136">In a completely centralized deployment, all branch site traffic is routed over WAN links.</span></span> <span data-ttu-id="d08ca-137">Statt für die erforderliche Bandbreite Gebühren für WAN-Verbindungen zu zahlen, können Sie das verteilte SIP-Trunking verwenden.</span><span class="sxs-lookup"><span data-stu-id="d08ca-137">Instead of paying for the bandwidth required for WAN linking, you may want to use distributed SIP trunking.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d08ca-138">Ausführliche Informationen dazu, warum und wie Sie das verteilte SIP-Trunking verwenden können, finden Sie unter <A href="lync-server-2013-branch-site-sip-trunking.md">SIP-Trunking in der Zweigstelle in lync Server 2013</A> in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="d08ca-138">For details about why and how you might use distributed SIP trunking, see <A href="lync-server-2013-branch-site-sip-trunking.md">Branch site SIP trunking in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

</div>

<div>

## <a name="supported-sip-trunking-connection-types"></a><span data-ttu-id="d08ca-139">Unterstützte Verbindungstypen für das SIP-Trunking</span><span class="sxs-lookup"><span data-stu-id="d08ca-139">Supported SIP Trunking Connection Types</span></span>

<span data-ttu-id="d08ca-140">Lync Server 2013 unterstützt die folgenden Verbindungstypen für SIP-Trunking:</span><span class="sxs-lookup"><span data-stu-id="d08ca-140">Lync Server 2013 supports the following connection types for SIP trunking:</span></span>

  - <span data-ttu-id="d08ca-141">Multiprotocol Label Switching (MPLS) ist ein privates Netzwerk, das Daten von einem Netzwerkknoten an einen anderen weiterleitet und übertragt.</span><span class="sxs-lookup"><span data-stu-id="d08ca-141">Multiprotocol Label Switching (MPLS) is a private network that directs and carries data from one network node to the next.</span></span> <span data-ttu-id="d08ca-142">Die Bandbreite in einem MPLS-Netzwerk wird gemeinsam mit anderen Teilnehmern verwendet und jedem Datenpaket wird eine Bezeichnung zugewiesen, um die Daten der einzelnen Teilnehmer voneinander zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="d08ca-142">The bandwidth in an MPLS network is shared with other subscribers, and each data packet is assigned a label to distinguish one subscriber’s data from another’s.</span></span> <span data-ttu-id="d08ca-143">Für diesen Verbindungstyp ist kein VPN erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d08ca-143">This connection type does not require VPN.</span></span> <span data-ttu-id="d08ca-144">Ein potenzieller Nachteil ist, dass übermäßiger IP-Datenverkehr zu Konflikten mit VoIP-Operationen führen kann, wenn dem VoIP-Datenverkehr keine Priorität eingeräumt wird.</span><span class="sxs-lookup"><span data-stu-id="d08ca-144">A potential drawback is that excessive IP traffic can interfere with VoIP operation unless VoIP traffic is given priority.</span></span>

  - <span data-ttu-id="d08ca-145">Eine private Verbindung ohne anderen Datenverkehr ist in der Regel der zuverlässigste und sicherste Verbindungstyp (beispielsweise eine geleaste Glasfaser-oder T1-Verbindung).</span><span class="sxs-lookup"><span data-stu-id="d08ca-145">A private connection with no other traffic is typically the most reliable and secure connection type (for example, a leased fiber-optic connection or T1 line).</span></span> <span data-ttu-id="d08ca-146">Dieser Verbindungstyp bietet die höchste Anrufkapazität, ist aber in der Regel am teuersten.</span><span class="sxs-lookup"><span data-stu-id="d08ca-146">This connection type provides the highest call-carrying capacity, but is typically the most expensive.</span></span> <span data-ttu-id="d08ca-147">Ein VPN ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d08ca-147">VPN is not required.</span></span> <span data-ttu-id="d08ca-148">Private Verbindungen sind geeignet für Organisationen mit hohem Anrufaufkommen oder strikten Sicherheits- und Verfügbarkeitsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="d08ca-148">Private connections are appropriate for organizations with high call volumes or stringent security and availability requirements.</span></span>

  - <span data-ttu-id="d08ca-149">Das öffentliche Internet ist der kostengünstigste Verbindungstyp, aber auch der am wenigsten zuverlässige, und der mit der niedrigsten Anruf Tragfähigkeit.</span><span class="sxs-lookup"><span data-stu-id="d08ca-149">The public Internet is the least expensive connection type, but also the least reliable, and the one with the lowest call-carrying capacity.</span></span> <span data-ttu-id="d08ca-150">Ihr Internet-Telefoniedienstanbieter (ITSP) kann diesen SIP Trunk-Verbindungstyp schützen, wenn er TLS (Transport Layer Security) und SRTP (Secure Real-Time Transport Protocol) unterstützt, um Signalisierungs-und Mediendatenverkehr zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="d08ca-150">Your Internet Telephony Service Provider (ITSP) can help secure this SIP trunk connection type if it supports Transport Layer Security (TLS) and Secure Real-Time Transport Protocol (SRTP) to encrypt signaling and media traffic.</span></span> <span data-ttu-id="d08ca-151">Wenn Sie keine SIP Trunk-Verbindung über das Internet für die Verwendung von TLS und SRTP konfigurieren können, wird dringend empfohlen, einen VPN-Tunnel zu verwenden, um eine sicherere Verbindung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="d08ca-151">If you cannot configure a SIP trunk connection through the Internet to use TLS and SRTP, we strongly recommend that you use a VPN tunnel to provide a more secure connection.</span></span> <span data-ttu-id="d08ca-152">Wenden Sie sich an Ihren ITSP, um zu ermitteln, ob er TLS mit SRTP unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d08ca-152">Contact your ITSP to determine whether it provides support for TLS with SRTP.</span></span>

<div>

## <a name="selecting-a-connection-type"></a><span data-ttu-id="d08ca-153">Auswählen eines Verbindungstyps</span><span class="sxs-lookup"><span data-stu-id="d08ca-153">Selecting a Connection Type</span></span>

<span data-ttu-id="d08ca-154">Der für Ihr Unternehmen geeignete Verbindungstyp für das SIP-Trunking richtet sich nach Ihren Anforderungen und Ihrem Budget.</span><span class="sxs-lookup"><span data-stu-id="d08ca-154">The most appropriate SIP trunking connection type for your enterprise depends on your needs and your budget.</span></span>

  - <span data-ttu-id="d08ca-155">Für ein mittelständisches oder größeres Unternehmen bietet ein MPLS-Netzwerk im Allgemeinen den größten Wert.</span><span class="sxs-lookup"><span data-stu-id="d08ca-155">For a mid-size or larger enterprise, an MPLS network generally provides the most value.</span></span> <span data-ttu-id="d08ca-156">Dieser Netzwerktyp bietet die erforderliche Bandbreite zu einem günstigeren Preis als ein dediziertes privates Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="d08ca-156">It can provide the necessary bandwidth at a cheaper rate than a specialized private network.</span></span>

  - <span data-ttu-id="d08ca-157">Große Unternehmen benötigen möglicherweise eine private Fiber-Optic-oder T1-Verbindung.</span><span class="sxs-lookup"><span data-stu-id="d08ca-157">Large enterprises may require a private fiber-optic or T1 connection.</span></span>

  - <span data-ttu-id="d08ca-158">Für ein kleines Unternehmen oder eine Zweigstelle mit geringem Anrufaufkommen kann die SIP-Trunkierung über das Internet die beste Wahl sein.</span><span class="sxs-lookup"><span data-stu-id="d08ca-158">For a small enterprise or branch site with low call volume, SIP trunking through the Internet may be the best choice.</span></span> <span data-ttu-id="d08ca-159">Dieser Verbindungstyp wird jedoch für mittelgroße oder größere Websites nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="d08ca-159">However, this connection type is not recommended for mid-size or larger sites.</span></span>

</div>

</div>

<div>

## <a name="codec-support"></a><span data-ttu-id="d08ca-160">Codec-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="d08ca-160">Codec Support</span></span>

<span data-ttu-id="d08ca-161">Der Dienstanbieter Proxy muss die folgenden Codecs unterstützen:</span><span class="sxs-lookup"><span data-stu-id="d08ca-161">The service provider proxy must support the following codecs:</span></span>

  - <span data-ttu-id="d08ca-162">G.711 A-Law (wird hauptsächlich außerhalb von Nordamerika eingesetzt)</span><span class="sxs-lookup"><span data-stu-id="d08ca-162">G.711 a-law (used primarily outside North America)</span></span>

  - <span data-ttu-id="d08ca-163">G.711 µ-Law (wird in Nordamerika eingesetzt)</span><span class="sxs-lookup"><span data-stu-id="d08ca-163">G.711 µ-law (used in North America)</span></span>

<span data-ttu-id="d08ca-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d08ca-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

