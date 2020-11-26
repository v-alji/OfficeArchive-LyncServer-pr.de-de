---
title: 'Lync Server 2013: Bereitstellungsrichtlinien für den Vermittlungsserver'
description: 'Lync Server 2013: Bereitstellungsrichtlinien für Mediation Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment guidelines for Mediation Server
ms:assetid: 7cc22b87-18d9-45e6-8402-015abd20f2e5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398622(v=OCS.15)
ms:contentKeyID: 48184606
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8198431b24714666c9411029aecd12835014fef4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429685"
---
# <a name="deployment-guidelines-for-mediation-server-in-lync-server-2013"></a><span data-ttu-id="d90c5-103">Bereitstellungsrichtlinien für den Vermittlungsserver in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d90c5-103">Deployment guidelines for Mediation Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d90c5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d90c5-104">

<span> </span></span></span>

<span data-ttu-id="d90c5-105">_**Letztes Änderungsdatum des Themas:** 2012-10-12_</span><span class="sxs-lookup"><span data-stu-id="d90c5-105">_**Topic Last Modified:** 2012-10-12_</span></span>

<span data-ttu-id="d90c5-106">In diesem Thema werden Planungsrichtlinien für die Vermittlungs Server Bereitstellung beschrieben.</span><span class="sxs-lookup"><span data-stu-id="d90c5-106">This topic describes planning guidelines for Mediation Server deployment.</span></span> <span data-ttu-id="d90c5-107">Nachdem Sie diese Richtlinien überprüft haben, empfehlen wir, dass Sie das Planungs Tool verwenden, um mögliche Alternative Topologien zu erstellen und anzuzeigen, die als Modelle dafür dienen können, wie die endgültige, von Ihnen bereitzustellende Topologie aussehen würde.</span><span class="sxs-lookup"><span data-stu-id="d90c5-107">After reviewing these guidelines, we recommend that you use the Planning Tool to create and view possible alternative topologies, which can serve as models for what the final tailored topology that you decide to deploy would look like.</span></span>

<div>

## <a name="collocated-or-stand-alone-mediation-server"></a><span data-ttu-id="d90c5-108">Oder eigenständigen Vermittlungs Server?</span><span class="sxs-lookup"><span data-stu-id="d90c5-108">Collocated or Stand-alone Mediation Server?</span></span>

<span data-ttu-id="d90c5-109">Der Vermittlungsserver befindet sich standardmäßig auf dem Standard Edition-Server oder Front-End-Server in einem Front-End-Pool an zentralen Standorten.</span><span class="sxs-lookup"><span data-stu-id="d90c5-109">Mediation Server is by default collocated on the Standard Edition server or Front End Server in a Front End pool at central sites.</span></span> <span data-ttu-id="d90c5-110">Die Anzahl von Anrufen über das Telefonfestnetz (Public Switched Telephone Network, PSTN), die verarbeitet werden können, und die Anzahl erforderlicher Computer im Pool hängt von folgenden Faktoren ab:</span><span class="sxs-lookup"><span data-stu-id="d90c5-110">The number of public switched telephone network (PSTN) calls that can be handled and the number of machines required in the pool will depend on the following:</span></span>

  - <span data-ttu-id="d90c5-111">Die Anzahl der Gateway-Peers, die vom Vermittlungs Server Pool gesteuert werden</span><span class="sxs-lookup"><span data-stu-id="d90c5-111">The number of gateway peers that the Mediation Server pool controls</span></span>

  - <span data-ttu-id="d90c5-112">Datenverkehr zu Spitzenzeiten, der über diese Gateways verarbeitet wird</span><span class="sxs-lookup"><span data-stu-id="d90c5-112">The high-volume traffic periods through those gateways</span></span>

  - <span data-ttu-id="d90c5-113">Der Prozentsatz der Anrufe, deren Medien den Vermittlungs Server umgehen</span><span class="sxs-lookup"><span data-stu-id="d90c5-113">The percentage of calls that are calls whose media bypass the Mediation Server</span></span>

<span data-ttu-id="d90c5-114">Berücksichtigen Sie bei der Planung unbedingt die Medienverarbeitungsanforderungen für PSTN-Anrufe und für A/V-Konferenzen, die nicht für eine Medienumgehung konfiguriert sind, sowie die erforderliche Leistung zur Verarbeitung von Signalinteraktionen für die Anzahl von Anrufen zu Spitzenzeiten, die unterstützt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d90c5-114">When planning, be sure to take into account the media processing requirements for PSTN calls and A/V conferences that are not configured for media bypass, as well as the processing needed to handle signaling interactions for the number of busy-hour calls that need to be supported.</span></span> <span data-ttu-id="d90c5-115">Wenn nicht genügend CPU vorhanden ist, müssen Sie einen eigenständigen Pool von Vermittlungsservern bereitstellen. und PSTN-Gateways, IP-PBX-Anlagen und SBCS müssen in Teilmengen aufgeteilt werden, die von den zusammengefassten Vermittlungsservern in einem Pool und den eigenständigen Vermittlungsservern in einem oder mehreren eigenständigen Pools gesteuert werden.</span><span class="sxs-lookup"><span data-stu-id="d90c5-115">If there is not enough CPU, then you must deploy a stand-alone pool of Mediation Servers; and PSTN gateways, IP-PBXs, and SBCs will need to be split into subsets that are controlled by the collocated Mediation Servers in one pool and the stand-alone Mediation Servers in one or more stand-alone pools.</span></span>

<span data-ttu-id="d90c5-116">Wenn Sie PSTN-Gateways, IP-PBX-Anlagen oder SBCS (Session Border Controllers) bereitgestellt haben, die nicht die richtigen Funktionen für die Interaktion mit einem Pool von Vermittlungsservern, einschließlich der folgenden, unterstützen, müssen Sie einem eigenständigen Pool zugeordnet werden, der aus einem einzigen Vermittlungsserver besteht:</span><span class="sxs-lookup"><span data-stu-id="d90c5-116">If you deployed PSTN gateways, IP-PBXs, or Session Border Controllers (SBCs) that do not support the correct capabilities to interact with a pool of Mediation Servers, including the following, then they will need to be associated with a stand-alone pool consisting of a single Mediation Server:</span></span>

  - <span data-ttu-id="d90c5-117">Durchführen von DNS (Domain Name System)-Lastenausgleich auf Netzwerkebene über Vermittlungsserver in einem Pool (oder anderweitiges Weiterleiten des Datenverkehrs an alle Vermittlungsserver in einem Pool)</span><span class="sxs-lookup"><span data-stu-id="d90c5-117">Perform network layer Domain Name System (DNS) load balancing across Mediation Servers in a pool (or otherwise route traffic uniformly to all Mediation Servers in a pool)</span></span>

  - <span data-ttu-id="d90c5-118">Akzeptieren von Datenverkehr von einem beliebigen Vermittlungs Server in einem Pool</span><span class="sxs-lookup"><span data-stu-id="d90c5-118">Accept traffic from any Mediation Server in a pool</span></span>

<span data-ttu-id="d90c5-119">Sie können das Planungs Tool Microsoft lync Server 2013 verwenden, um zu evaluieren, ob abstimmen dem Vermittlungsserver mit dem Front-End-Pool die Last verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="d90c5-119">You can use the Microsoft Lync Server 2013, Planning Tool to evaluate whether collocating the Mediation Server with your Front End pool can handle the load.</span></span> <span data-ttu-id="d90c5-120">Wenn Ihre Umgebung diese Anforderungen nicht erfüllen kann, müssen Sie einen eigenständigen Vermittlungs Server Pool bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d90c5-120">If your environment cannot meet these requirements, then you must deploy a stand-alone Mediation Server pool.</span></span>

</div>

<div>

## <a name="central-site-and-branch-site-considerations"></a><span data-ttu-id="d90c5-121">Überlegungen zum zentralen Standort und Zweigstellenstandort</span><span class="sxs-lookup"><span data-stu-id="d90c5-121">Central Site and Branch Site Considerations</span></span>

<span data-ttu-id="d90c5-122">Vermittlungsserver am zentralen Standort können verwendet werden, um Anrufe für IP-PBXs-oder PSTN-Gateways an Zweigstellen zu leiten.</span><span class="sxs-lookup"><span data-stu-id="d90c5-122">Mediation Servers at the central site can be used to route calls for IP-PBXs or PSTN gateways at branch sites.</span></span> <span data-ttu-id="d90c5-123">Wenn Sie jedoch SIP-Trunks bereitstellen, müssen Sie einen Vermittlungs Server an der Website bereitstellen, auf der jeder trunk beendet wird.</span><span class="sxs-lookup"><span data-stu-id="d90c5-123">If you deploy SIP trunks, however, you must deploy a Mediation Server at the site where each trunk terminates.</span></span> <span data-ttu-id="d90c5-124">Die Verwendung eines Vermittlungsservers an der zentralen Standort Route für Anrufe an ein IP-PBX-oder PSTN-Gateway an einer Zweigstelle erfordert keine medienumgehung.</span><span class="sxs-lookup"><span data-stu-id="d90c5-124">Having a Mediation Server at the central site route calls for an IP-PBX or PSTN gateway at a branch site does not require the use of media bypass.</span></span> <span data-ttu-id="d90c5-125">Wenn Sie jedoch die medienumgehung aktivieren können, wird dadurch die Latenz des Medien Pfads verringert und dadurch die Medienqualität verbessert, da der Medienpfad nicht mehr dem Signalisierungs Pfad folgen muss.</span><span class="sxs-lookup"><span data-stu-id="d90c5-125">However, if you can enable media bypass, doing so will reduce media path latency and, consequently, result in improved media quality because the media path is no longer required to follow the signaling path.</span></span> <span data-ttu-id="d90c5-126">Zudem wird durch die Medienumgehung die Verarbeitungslast des Pools verringert.</span><span class="sxs-lookup"><span data-stu-id="d90c5-126">Media bypass will also decrease the processing load on the pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d90c5-127">Die Medienumgehung funktioniert nicht mit allen PSTN-Gateways, IP-Nebenstellenanlagen oder SBCs.</span><span class="sxs-lookup"><span data-stu-id="d90c5-127">Media bypass will not interoperate with every PSTN gateway, IP-PBX, and SBC.</span></span> <span data-ttu-id="d90c5-128">Microsoft hat eine Reihe von PSTN-Gateways und SBCs mit zertifizierten Partnern getestet und einige Tests mit IP-Nebenstellenanlagen von Cisco durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="d90c5-128">Microsoft has tested a set of PSTN gateways and SBCs with certified partners and has done some testing with Cisco IP-PBXs.</span></span> <span data-ttu-id="d90c5-129">Die medienumgehung wird nur mit Produkten und Versionen unterstützt, die unter Unified Communications Open Interoperability Program – lync Server unter aufgeführt sind <A href="https://go.microsoft.com/fwlink/p/?linkid=268730">https://go.microsoft.com/fwlink/p/?LinkId=268730</A> .</span><span class="sxs-lookup"><span data-stu-id="d90c5-129">Media bypass is supported only with products and versions listed on Unified Communications Open Interoperability Program – Lync Server at <A href="https://go.microsoft.com/fwlink/p/?linkid=268730">https://go.microsoft.com/fwlink/p/?LinkId=268730</A>.</span></span>



</div>

<span data-ttu-id="d90c5-130">Wenn die Stabilität des Zweigstellen Standorts erforderlich ist, muss eine Survivable Branch-Appliance oder eine Kombination aus einem Front-End-Server, einem Vermittlungsserver und einem Gateway an der Zweigstelle bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="d90c5-130">If branch site resiliency is required, a Survivable Branch Appliance or combination of a Front End Server, a Mediation Server, and a gateway must be deployed at the branch site.</span></span> <span data-ttu-id="d90c5-131">(Die Annahme, dass die Stabilität des Zweigstellen Standorts davon ausgeht, dass Anwesenheit und Konferenzen auf der Website nicht belastbar sind.) Anleitungen zur Planung von Zweigstellen für Sprachanrufe finden Sie unter [Planen der sprach Sicherheit in der Zweigstelle in lync Server 2013](lync-server-2013-planning-for-branch-site-voice-resiliency.md).</span><span class="sxs-lookup"><span data-stu-id="d90c5-131">(The assumption with branch site resiliency is that presence and conferencing are not resilient at the site.) For guidance on branch site planning for voice, see [Planning for branch-site voice resiliency in Lync Server 2013](lync-server-2013-planning-for-branch-site-voice-resiliency.md).</span></span>

<span data-ttu-id="d90c5-132">Für Interaktionen mit einer IP-PBX-Anlage, wenn die IP-Telefonanlage nicht ordnungsgemäß frühe Medien Interaktionen mit mehreren frühen Dialogfeldern und RFC 3960-Interaktionen unterstützt, können die ersten Wörter der Ansage für eingehende Anrufe von der IP-PBX zu lync-Endpunkten abgeschnitten werden.</span><span class="sxs-lookup"><span data-stu-id="d90c5-132">For interactions with an IP-PBX, if the IP-PBX does not correctly support early media interactions with multiple early dialogs and RFC 3960 interactions, there can be clipping of the first few words of the greeting for incoming calls from the IP-PBX to Lync endpoints.</span></span> <span data-ttu-id="d90c5-133">Dieses Verhalten kann gravierender sein, wenn ein Vermittlungs Server an einem zentralen Standort Routing Anrufe für eine IP-PBX-Anlage durchführt, bei der die Route an einer Zweigstelle beendet wird, da für die Signalisierungs Ausführung mehr Zeit benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="d90c5-133">This behavior can be more severe if a Mediation Server at a central site is routing calls for an IP-PBX where the route terminates at a branch site, because more time is needed for signaling to complete.</span></span> <span data-ttu-id="d90c5-134">Wenn dieses Verhalten auftritt, ist die Bereitstellungeines Vermittlungsservers auf der Verzweigungs Website die einzige Möglichkeit, das Clipping der ersten Wörter zu reduzieren.</span><span class="sxs-lookup"><span data-stu-id="d90c5-134">If you experience this behavior, deploying a Mediation Server at the branch site is the only way to reduce clipping of the first few words.</span></span>

<span data-ttu-id="d90c5-135">Wenn Ihre zentrale Website über eine TDM-Telefonanlage verfügt oder wenn Ihre IP-Telefonanlage nicht die Notwendigkeit eines PSTN-Gateways beseitigt, müssen Sie ein Gateway auf der Anrufroute bereitstellen, die den Vermittlungs Server und die Telefonanlage verbindet.</span><span class="sxs-lookup"><span data-stu-id="d90c5-135">Finally, if your central site has a TDM PBX, or if your IP-PBX does not eliminate the need for a PSTN gateway, then you must deploy a gateway on the call route connecting Mediation Server and the PBX.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d90c5-136">Um die Medienqualität von eigenständigen Vermittlungsservern zu verbessern, sollten Sie RSS (Receive-Side Scaling) für die Netzwerkadapter dieser Server aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d90c5-136">To improve the media performance of standalone Mediation Server, you should enable receive-side scaling (RSS) on the network adapters on these servers.</span></span> <span data-ttu-id="d90c5-137">Mit RSS können eingehende Pakete gleichzeitig von mehreren Prozessoren auf dem Server verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="d90c5-137">RSS enables incoming packets to be handled in parallel by multiple processors on the server.</span></span> <span data-ttu-id="d90c5-138">Ausführliche Informationen finden Sie unter "Verbesserungen bei der Empfangs seitigen Skalierung in Windows Server" unter <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?LinkId=268731</A> .</span><span class="sxs-lookup"><span data-stu-id="d90c5-138">For details, see "Receive-Side Scaling Enhancements in Windows Server" at <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?LinkId=268731</A>.</span></span> <span data-ttu-id="d90c5-139">Weitere Informationen zum Aktivieren von RSS finden Sie in der Dokumentation zu Ihrem Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="d90c5-139">For details about how to enable RSS, see your network adapter documentation.</span></span>



<span data-ttu-id="d90c5-140"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d90c5-140"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

