---
title: 'Lync Server 2013: Entwerfen des SIP-Trunks für E9-1-1'
description: 'Lync Server 2013: Entwerfen des SIP-Trunks für E9-1-1.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Designing the SIP trunk for E9-1-1
ms:assetid: 4f93b974-b460-45c7-a4a8-6f38e34840f5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398323(v=OCS.15)
ms:contentKeyID: 48184096
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ced3c92cb14739367c4e54da933a536cb66deb08
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429538"
---
# <a name="designing-the-sip-trunk-for-e9-1-1-in-lync-server-2013"></a><span data-ttu-id="81e18-103">Entwerfen des SIP-Trunks für E9-1-1 in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="81e18-103">Designing the SIP trunk for E9-1-1 in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="81e18-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="81e18-104">

<span> </span></span></span>

<span data-ttu-id="81e18-105">_**Letztes Änderungsdatum des Themas:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="81e18-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="81e18-106">Lync Server verwendet SIP-Trunks, um einen Notruf mit dem E9-1-1-Dienstanbieter zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="81e18-106">Lync Server uses SIP trunks to connect an emergency call to the E9-1-1 service provider.</span></span> <span data-ttu-id="81e18-107">Sie können Notrufdienst-SIP-Trunks für E9-1-1 an einem zentralen Standort, an mehreren zentralen Standorten oder an jeder Zweigstelle einrichten.</span><span class="sxs-lookup"><span data-stu-id="81e18-107">You can set up emergency service SIP trunks for E9-1-1 at one central site, at multiple central sites, or at each branch site.</span></span> <span data-ttu-id="81e18-108">Wenn jedoch die WAN-Verbindung zwischen dem Standort des Anrufers und dem Standort, an dem der Notfalldienst-SIP-Trunk gehostet wird, nicht verfügbar ist, ist für einen Anruf von einem Benutzer am nicht verbundenen Standort ein spezieller Telefonverwendungseintrag in der VoIP-Richtlinie des Benutzers erforderlich, der den Anruf über das lokale PSTN-Gateway an das ECRC weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="81e18-108">However, if the WAN link between the caller’s site and the site that hosts the emergency service SIP trunk is unavailable, then a call placed by a user at the disconnected site will need a special phone usage record in the user’s voice policy that will route the call to the ECRC through the local public switched telephone network (PSTN) gateway.</span></span> <span data-ttu-id="81e18-109">Das gleiche trifft zu, wenn in der Anrufsteuerung Begrenzungen für gleichzeitige Anrufe aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="81e18-109">The same is true if call admission control concurrent call limits are in effect.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="81e18-110">Es gibt zwei Möglichkeiten, einen SIP-Trunk in einer lync Server-Umgebung zu implementieren:</span><span class="sxs-lookup"><span data-stu-id="81e18-110">There are two ways to implement a SIP trunk in a Lync Server environment:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="81e18-111">Verwenden Sie mehrfach vernetzte Vermittlungsserver, die ihre nach außen gerichteten, öffentlich weitergeleiteten Schnittstellen verwenden, um mit dem SIP-Trunk-Anbieter zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="81e18-111">Use multihomed Mediation Servers that use their outward-facing publicly-routed interfaces to communicate with the SIP trunk provider.</span></span></P>
> <LI>
> <P><span data-ttu-id="81e18-112">Verwenden Sie einen lokalen Session Border Controller (SBC), um einen sicheren abgrenzungspunkt zwischen den Vermittlungsservern und den Diensten des SIP Trunk-Anbieters bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="81e18-112">Use an on-premises Session Border Controller (SBC) to provide a secure demarcation point between the Mediation Servers and the SIP trunk provider’s services.</span></span></P></LI></UL><span data-ttu-id="81e18-113">Wenn Sie sich für die zweite Methode entscheiden, stellen Sie sicher, dass die Marke/das Modell des von Ihnen ausgewählten SBC die Weitergabe von PIDF-LO (Presence Information Data Format Location Object)-Standortdaten als Teil der SIP INVITE unterstützt.</span><span class="sxs-lookup"><span data-stu-id="81e18-113">If you choose the latter method, be sure that the SBC make and model that you choose has been certified and supports passing Presence Information Data Format Location Object (PIDF-LO) location data as part of its SIP INVITE.</span></span> <span data-ttu-id="81e18-114">Andernfalls gehen die Anrufe ohne Standortinformationen beim Anbieter für die Notrufunterstützung ein.</span><span class="sxs-lookup"><span data-stu-id="81e18-114">Otherwise, the calls will arrive at the emergency services service provider stripped of their location information.</span></span> <span data-ttu-id="81e18-115">Ausführliche Informationen zu zertifizierten SBCS finden Sie unter "für Microsoft lync qualifizierte Infrastruktur" <A href="https://go.microsoft.com/fwlink/p/?linkid=248425">https://go.microsoft.com/fwlink/p/?LinkId=248425</A> .</span><span class="sxs-lookup"><span data-stu-id="81e18-115">For details about certified SBCs, see "Infrastructure Qualified for Microsoft Lync" at <A href="https://go.microsoft.com/fwlink/p/?linkid=248425">https://go.microsoft.com/fwlink/p/?LinkId=248425</A>.</span></span><BR><span data-ttu-id="81e18-116">Über E9-1-1-Dienstanbieter erhalten Sie Zugriff auf ein SBC-Paar, um Redundanz zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="81e18-116">E9-1-1 service providers supply you with access to a pair of SBCs for redundancy.</span></span> <span data-ttu-id="81e18-117">Sie müssen mehrere Entscheidungen bezüglich der Mediations Server Topologie und der Konfiguration des Anruf Routings treffen.</span><span class="sxs-lookup"><span data-stu-id="81e18-117">You need to make several decisions regarding the Mediation Server topology and call routing configuration.</span></span> <span data-ttu-id="81e18-118">Möchten Sie beide SBCs als gleichwertig behandeln und Roundrobinrouting für Anrufe zwischen ihnen verwenden oder werden Sie einen SBC als primären und den anderen als sekundären SBC festlegen?</span><span class="sxs-lookup"><span data-stu-id="81e18-118">Will you treat both SBCs as equal peers and use round-robin routing for calls between them, or will you designate one SBC as primary and the other as secondary?</span></span>



</div>

<span data-ttu-id="81e18-119">Details zum Bereitstellen eines SIP-Trunks in lync Server finden Sie unter [wie kann ich SIP-Trunking in lync Server 2013 implementieren?](lync-server-2013-how-do-i-implement-sip-trunking.md).</span><span class="sxs-lookup"><span data-stu-id="81e18-119">For details about deploying a SIP trunk in Lync Server, see [How do I implement SIP trunking in Lync Server 2013?](lync-server-2013-how-do-i-implement-sip-trunking.md).</span></span> <span data-ttu-id="81e18-120">Zur einfacheren Bereitstellung der SIP-Trunks für E9-1-1 sollten Sie zunächst die folgenden Fragen beantworten.</span><span class="sxs-lookup"><span data-stu-id="81e18-120">The following questions will help you decide how to deploy the SIP trunks for E9-1-1.</span></span>

  - <span data-ttu-id="81e18-121">**Soll der SIP-Trunk über eine dedizierte geleaste oder eine gemeinsam genutzte Internetverbindung bereitgestellt werden?**</span><span class="sxs-lookup"><span data-stu-id="81e18-121">**Should you deploy the SIP trunk over a dedicated leased or a shared internet connection?**</span></span>  
    <span data-ttu-id="81e18-p105">Es ist wichtig, dass jederzeit Notrufe getätigt werden können. Eine dedizierte Leitung bietet eine Verbindung, die nicht durch anderen Datenverkehr im Netzwerk belegt ist, und ermöglicht gleichzeitig die Implementierung von QoS. Denken Sie daran, dass eine IPSec-Verschlüsselung erforderlich ist, wenn Sie beim Herstellen einer Verbindung mit Anbietern für die Notrufunterstützung über das öffentliche Internet die Vertraulichkeit von Notrufen gewährleisten müssen.</span><span class="sxs-lookup"><span data-stu-id="81e18-p105">It is important that emergency calls always connect. A dedicated line provides a connection that will not be preempted by other traffic on the network, and gives you the ability to implement Quality of Service (QoS). Remember that if you are connecting to emergency services service providers over the public Internet and you need to guarantee the confidentiality of emergency calls, IPSec encryption is required.</span></span>

<!-- end list -->

  - <span data-ttu-id="81e18-125">**Ist Ihre E9-1-1-Bereitstellung für die Notfalltoleranz konzipiert?**</span><span class="sxs-lookup"><span data-stu-id="81e18-125">**Is your E9-1-1 deployment designed for disaster tolerance?**</span></span>  
    <span data-ttu-id="81e18-126">Da es sich um eine Lösung für Notrufe handelt, ist die Ausfallsicherheit von grundlegender Bedeutung.</span><span class="sxs-lookup"><span data-stu-id="81e18-126">Because this is an emergency solution, resiliency is important.</span></span> <span data-ttu-id="81e18-127">Stellen Sie Ihre primären und sekundären Vermittlungsserver und SIP-Stämme in Disaster-toleranten Speicherorten bereit.</span><span class="sxs-lookup"><span data-stu-id="81e18-127">Deploy your primary and secondary Mediation Servers and SIP trunks in disaster tolerant locations.</span></span> <span data-ttu-id="81e18-128">Es empfiehlt sich, den primären Vermittlungsserver den Benutzern, die er unterstützt, am nächsten zu stellen und Failover-Anrufe über den sekundären Vermittlungsserver (an einem anderen geografischen Standort) weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="81e18-128">It is a good idea to deploy your primary Mediation Server closest to the users that it is supporting, and route failover calls through the secondary Mediation Server (located in a different geographic location).</span></span>

<!-- end list -->

  - <span data-ttu-id="81e18-129">**Sollten Sie einen separaten SIP-Trunk für jeden Zweigstellenstandort bereitstellen?**</span><span class="sxs-lookup"><span data-stu-id="81e18-129">**Should you deploy a separate SIP trunk for each branch office?**</span></span>  
    <span data-ttu-id="81e18-130">Lync Server bietet verschiedene Strategien für die Behandlung von VoIP-Flexibilität in Zweigniederlassungen, einschließlich: mit belastbaren Datennetzwerken, Bereitstellen eines SIP-Trunks an jeder Verzweigung oder durch Drücken von Anrufen an das lokale Gateway während Ausfällen.</span><span class="sxs-lookup"><span data-stu-id="81e18-130">Lync Server provides several strategies for handling voice resiliency in branch offices, including: having resilient data networks, deploying a SIP trunk at each branch, or pushing calls out to the local gateway during outages.</span></span> <span data-ttu-id="81e18-131">Ausführliche Informationen finden Sie unter [SIP-Trunking in der Zweigstelle in lync Server 2013](lync-server-2013-branch-site-sip-trunking.md).</span><span class="sxs-lookup"><span data-stu-id="81e18-131">For details, see [Branch site SIP trunking in Lync Server 2013](lync-server-2013-branch-site-sip-trunking.md).</span></span>

<!-- end list -->

  - <span data-ttu-id="81e18-132">**Ist die Anrufsteuerung aktiviert?**</span><span class="sxs-lookup"><span data-stu-id="81e18-132">**Is call admission control (CAC) enabled?**</span></span>  
    <span data-ttu-id="81e18-133">Lync Server behandelt keine Notrufe anders als normale Anrufe.</span><span class="sxs-lookup"><span data-stu-id="81e18-133">Lync Server does not handle emergency calls any differently than an ordinary call.</span></span> <span data-ttu-id="81e18-134">Aus diesem Grund kann sich die Bandbreitenverwaltung oder Anrufsteuerung negativ auf die E9-1-1-Konfiguration auswirken.</span><span class="sxs-lookup"><span data-stu-id="81e18-134">For this reason, bandwidth management, or call admission control (CAC), can have a negative impact on an E9-1-1 configuration.</span></span> <span data-ttu-id="81e18-135">Notrufe werden möglicherweise blockiert oder zum lokalen PSTN-Gateway geroutet, wenn die Anrufsteuerung aktiviert ist und der konfigurierte Grenzwert für die Verbindung überschritten wird, über die Notrufe geroutet werden.</span><span class="sxs-lookup"><span data-stu-id="81e18-135">Emergency calls will be blocked or routed to the local PSTN gateway if a CAC is enabled and the configured limit is exceeded on a link where emergency calls are being routed.</span></span> <span data-ttu-id="81e18-136">Wie bereits in diesem Thema besprochen verfügen solche Anrufe über keine Standortdaten und müssen manuell an das ECRC weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="81e18-136">As indicated earlier in this topic, such calls will not have location data and must be manually routed to the ECRC.</span></span>

<span data-ttu-id="81e18-137"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="81e18-137"></div>

<span> </span>

</div>

</div>

</span></span></div>

