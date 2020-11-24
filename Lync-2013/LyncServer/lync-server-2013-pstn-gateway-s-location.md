---
title: 'Lync Server 2013: Standort eines PSTN-Gateways'
description: 'Lync Server 2013: Standort des PSTN-Gateways.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN gateway's location
ms:assetid: 49693a35-fad3-49ee-a71e-c7e4537b79aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994031(v=OCS.15)
ms:contentKeyID: 51803940
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f793249908bd1f064f9038ddd90c7f5b01a61d5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394590"
---
# <a name="pstn-gateways-location-in-lync-server-2013"></a><span data-ttu-id="b2123-103">Standort eines PSTN-Gateways in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b2123-103">PSTN gateway's location in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b2123-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b2123-104">

<span> </span></span></span>

<span data-ttu-id="b2123-105">_**Letztes Änderungsdatum des Themas:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="b2123-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="b2123-106">Für Anrufe, die über PSTN-Gateways und PBX-Anlagen weitergeleitet werden, sind möglicherweise abhängig vom Standort solcher Systeme Location-Based Routing Einschränkungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b2123-106">Calls routed via PSTN gateways and PBXs might require Location-Based Routing restrictions depending on the location of such systems.</span></span> <span data-ttu-id="b2123-107">Location-Based-Routing kann pro trunk basierend auf Granularität aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="b2123-107">Location-Based Routing can be enabled at the granularity on a per trunk basis.</span></span>

<span data-ttu-id="b2123-108">Location-Based Routing führt die folgenden Regeln ein, wenn Sie in einem Trunk aktiviert sind:</span><span class="sxs-lookup"><span data-stu-id="b2123-108">Location-Based Routing introduces the following set of rules when enabled on a trunk:</span></span>

  - <span data-ttu-id="b2123-109">Wenn Location-Based Routing pro trunk aktiviert ist, werden die Regeln, die für diesen Trunk definiert sind, nur auf die durch diesen Trunk weitergeleiteten Anrufe angewendet.</span><span class="sxs-lookup"><span data-stu-id="b2123-109">When Location-Based Routing is enabled on a per trunk basis, the rules define on that trunk will be applied only to calls routed through that trunk.</span></span>

  - <span data-ttu-id="b2123-110">Um zu verhindern, dass PSTN-Mautgebühren für Anrufe von einer Netzwerk Website, die sich von der Netzwerk Website, auf der sich das PSTN-Gateway befindet, abweichen, wird Location-Based Routing die Zuordnung einer Netzwerk Website zu einem bestimmten trunk eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b2123-110">To prevent PSTN tolls bypass where calls originate from a network site different that the network site where the PSTN gateway is located, Location-Based Routing introduces the association of a network site to a given trunk.</span></span> <span data-ttu-id="b2123-111">Dadurch wird die Netzwerk Website definiert, die das Weiterleiten von Anrufen an einen bestimmten trunk ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="b2123-111">This defines the network site that allows calls to be routed to a given trunk.</span></span>

<span data-ttu-id="b2123-112">Trunks können für Location-Based Routing auf zwei Arten aktiviert werden:</span><span class="sxs-lookup"><span data-stu-id="b2123-112">Trunks can be enabled for Location-Based Routing in two ways:</span></span>

  - <span data-ttu-id="b2123-p103">Der Trunk ist für ein PSTN-Gateway definiert, das Anrufe an das Telefonfestnetz weiterleitet. Eingehende Anrufe, die von einem Trunk dieses Typs weitergeleitet werden, werden nur an Endgeräte weitergeleitet, die sich am selben Netzwerkstandort befinden wie der Trunk.</span><span class="sxs-lookup"><span data-stu-id="b2123-p103">The trunk is defined for a PSTN gateway that egresses calls to the PSTN. Incoming calls routed by a trunk of this type will be routed only to endpoints located within the same network site as the trunk.</span></span>

  - <span data-ttu-id="b2123-115">Der trunk ist für einen Vermittlungs Server-Peer definiert, der keine Anrufe an das PSTN abgibt und Dienste für Benutzer mit älteren Telefonen an statischen Speicherorten (also Telefonanlagen) abruft.</span><span class="sxs-lookup"><span data-stu-id="b2123-115">The trunk is defined for a Mediation Server peer that doesn’t egress calls to the PSTN and services users with legacy phones in a static locations (i.e. PBX phones).</span></span> <span data-ttu-id="b2123-116">Für diese spezielle Konfiguration wird für alle eingehenden Anrufe, die von einem Trunk dieses Typs weitergeleitet werden, angenommen, dass sie vom selben Netzwerkstandort kommen wie der Trunk.</span><span class="sxs-lookup"><span data-stu-id="b2123-116">For this particular configuration, all incoming calls routed by a trunk of this type will be considered to be originating from the same network site as the trunk.</span></span> <span data-ttu-id="b2123-117">Anrufe von PBX-Benutzern haben dieselbe Location-Based Routing Erzwingung wie lync-Benutzer, die sich am gleichen Netzwerkstandort wie der Stamm befinden.</span><span class="sxs-lookup"><span data-stu-id="b2123-117">Calls from PBX users will have the same Location-Based Routing enforcement as Lync users who are located in the same network site as the trunk.</span></span> <span data-ttu-id="b2123-118">Wenn zwei PBX-Systeme, die sich auf separaten Netzwerkstandorten befinden, über lync Server verbunden sind, ermöglicht Location-Based Routing die Weiterleitung von einem PBX-Endpunkt in einer Netzwerk Website an einen anderen PBX-Endpunkt auf der anderen Netzwerk Website.</span><span class="sxs-lookup"><span data-stu-id="b2123-118">If two PBX systems located in separate network sites are connected through Lync Server, Location-Based Routing will allow routing from one PBX endpoint in one network site to another PBX endpoint in the other network site.</span></span> <span data-ttu-id="b2123-119">Dieses Szenario wird durch Location-Based Routing nicht blockiert.</span><span class="sxs-lookup"><span data-stu-id="b2123-119">This scenario will not be blocked by Location-Based Routing.</span></span> <span data-ttu-id="b2123-120">Zusätzlich zu diesem Szenario und auf ähnliche Weise wie ein lync-Benutzer am gleichen Speicherort können Endpunkte, die mit einem Vermittlungsserver-Peer mit dieser Konfiguration verbunden sind, Anrufe an und von einem anderen Vermittlungsserver-Peer durchführen oder empfangen, die keine Anrufe an das PSTN (also einen mit einer anderen Telefonanlage verbundenen Endpunkt) weiterleiten, und zwar unabhängig von der Netzwerk Website, der</span><span class="sxs-lookup"><span data-stu-id="b2123-120">In addition to this scenario and in a similar way as a Lync user in the same location, endpoints connected to a Mediation Server peer with this configuration will be able to make or receive calls to and from other Mediation Server peer that do not route calls to the PSTN (i.e. an endpoint connected to a different PBX) regardless of the network site to which the Mediation Server peer is associated.</span></span> <span data-ttu-id="b2123-121">Alle eingehenden Anrufe, ausgehenden Anrufe, Anruf Übertragungen und Anrufweiterleitung mit PSTN-Endpunkten unterliegen dem standortbasierten Routing, um nur PSTN-Gateways zu verwenden, die als lokal für diesen Vermittlungs Server-Peer definiert sind.</span><span class="sxs-lookup"><span data-stu-id="b2123-121">All inbound calls, outbound calls, call transfers and call forwards involving PSTN endpoints will be subject to Location Based Routing to use only PSTN gateways that are defined as local to such Mediation Server peer.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="b2123-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2123-122">See Also</span></span>


[<span data-ttu-id="b2123-123">Anleitungen für das standortbasierte Routing in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b2123-123">Guidance for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-guidance-for-location-based-routing.md)  
  

<span data-ttu-id="b2123-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b2123-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

