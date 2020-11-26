---
title: 'Lync Server 2013: Standort des Benutzers'
description: 'Lync Server 2013: Standort des Benutzers.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User's location
ms:assetid: ce57941d-086b-448e-8ada-c7d636a2a1c9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994073(v=OCS.15)
ms:contentKeyID: 51803984
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a92ec780809cdb3e1ee582ce6c348c884bbb5890
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439170"
---
# <a name="users-location-in-lync-server-2013"></a><span data-ttu-id="20929-103">Standort des Benutzers in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20929-103">User's location in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="20929-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="20929-104">

<span> </span></span></span>

<span data-ttu-id="20929-105">_**Letztes Änderungsdatum des Themas:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="20929-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="20929-106">Location-Based-Routing nutzt dieselben netzwerkregionen,-Standorte und-Subnetze, wie Sie in lync Server von E9-1-1, CAC und medienumgehung definiert sind, um Anruf Weiterleitungs Einschränkungen anzuwenden, um die PSTN-Maut Umgehung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="20929-106">Location-Based Routing leverages the same network regions, sites and subnets as defined in Lync Server used by E9-1-1, CAC and Media Bypass to apply call routing restrictions to prevent PSTN toll bypass.</span></span> <span data-ttu-id="20929-107">Der Standort eines Benutzers wird durch das IP-Subnetz der lync-Endpunkte des Benutzers bestimmt, von dem die Verbindung hergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="20929-107">A user’s location is determined by the IP subnet of the user’s Lync endpoint(s) are connected from.</span></span> <span data-ttu-id="20929-108">Jedes IP-Subnetz ist einem Netzwerkstandort zugeordnet, von denen mehrere zu vom Administrator definierten Netzwerkbereichen zusammengefasst sind.</span><span class="sxs-lookup"><span data-stu-id="20929-108">Each IP subnet is associated to a network site, which are aggregated into network regions defined by the administrator.</span></span> <span data-ttu-id="20929-109">Das standortbasierte Routing wird auf Grundlage des Netzwerkstandorts des Benutzers durchgesetzt.</span><span class="sxs-lookup"><span data-stu-id="20929-109">Location-Based Routing is enforced based on the user’s network site.</span></span>

<span data-ttu-id="20929-110">Location-Based Routingregeln werden pro Netzwerk Website angewendet, was bedeutet, dass ein bestimmter Regelsatz auf alle Endpunkte angewendet wird, die für Location-Based Routing aktiviert sind, die sich innerhalb desselben Netzwerkstandorts befinden.</span><span class="sxs-lookup"><span data-stu-id="20929-110">Location-Based Routing rules are applied on a per network site basis, meaning that a given set of rules will be applied to all endpoints enabled for Location-Based Routing that are located within the same network site.</span></span> <span data-ttu-id="20929-111">Administratoren können das standortbasierte Routing auf Netzwerkstandorte anwenden, die dies erfordern.</span><span class="sxs-lookup"><span data-stu-id="20929-111">Administrators can apply Location-Based Routing to network sites that require it.</span></span>

<span data-ttu-id="20929-112">Richtlinien für das VoIP-Routing können auf Grundlage von Netzwerkstandorten definiert werden, um ein bestimmtes Gateway in das öffentliche Telefonnetz zu definieren, das dann von allen Benutzern, die sich am gleichen Netzwerkstandort befinden, für Verbindungen mit Rufnummern im öffentlichen Telefonnetz verwendet werden muss.</span><span class="sxs-lookup"><span data-stu-id="20929-112">Voice routing policies can be defined on a per network site basis to define a particular PSTN gateway that should be used by all users located in the network site to call PSTN phone numbers.</span></span> <span data-ttu-id="20929-113">Solche VoIP-Routing Richtlinien haben Vorrang vor dem Routing, das durch die VoIP-Richtlinie des Benutzers definiert wird, wenn sich der Benutzer in einer Netzwerk Website befindet, die für Location-Based Routing aktiviert ist, und er verhindert das Routing von Anrufen über andere PSTN-Gateways, die für Location-Based Routing aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="20929-113">Such voice routing policies will take precedence over the routing defined by the user’s voice policy when the user is located in a network site enabled for Location-Based Routing, and it will prevent the routing of calls via other PSTN gateways that are enabled for Location-Based Routing.</span></span> <span data-ttu-id="20929-114">Wenn ein lync-Benutzer einen PSTN-Anruf anlegt, bestimmt die VoIP-Richtlinie des Benutzers, ob der Benutzer zum tätigen des Anrufs autorisiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="20929-114">When a Lync user places a PSTN call, the user’s voice policy determines whether the user can be authorized to place the call.</span></span> <span data-ttu-id="20929-115">Wenn die VoIP-Richtlinie des Benutzers es dem Benutzer ermöglicht, den Anruf zu tätigen, bestimmt Location-Based Routing, von welchem PSTN-Gateway der Anruf ausgehen soll.</span><span class="sxs-lookup"><span data-stu-id="20929-115">If the user’s voice policy allows the user to place the call, Location-Based Routing determines which PSTN gateway the call should egress from.</span></span> <span data-ttu-id="20929-116">Location-Based Routing macht diese Ermittlung auf Grundlage des Standorts des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="20929-116">Location-Based Routing makes this determination based on the user’s location.</span></span>

<span data-ttu-id="20929-117">Der Standort eines Benutzers kann auf folgende Weise kategorisiert werden:</span><span class="sxs-lookup"><span data-stu-id="20929-117">A user location can be categorized in the following ways:</span></span>

  - <span data-ttu-id="20929-118">Der Benutzer befindet sich in einer bekannten Netzwerk Website, die für Location-Based Routing aktiviert ist, und seine DID-Nummer (Direktwahl) wird auf einem PSTN-Gateway beendet, das sich auf demselben Netzwerkstandort befindet (also Office).</span><span class="sxs-lookup"><span data-stu-id="20929-118">The user is located in a known network site enabled for Location-Based Routing and his DID (Direct Inward Dial) number terminates on a PSTN gateway placed in the same network site (i.e. office).</span></span> <span data-ttu-id="20929-119">Das Routing ausgehender Anrufe erfolgt anhand der VoIP-Routingrichtlinie des Netzwerkstandorts, an dem sich der Benutzer befindet.</span><span class="sxs-lookup"><span data-stu-id="20929-119">The routing of outbound calls will be through the voice routing policy of the network site in which the user is located.</span></span> <span data-ttu-id="20929-120">Aus dem öffentlichen Telefonnetz für den Benutzer eingehende Anrufe werden an Endpunkte geroutet, die sich am gleichen Netzwerkstandort wie das Gateway in das öffentliche Telefonnetz befinden.</span><span class="sxs-lookup"><span data-stu-id="20929-120">Incoming PSTN calls to the user are routed to endpoints that are located in the same network site as the PSTN gateway.</span></span>

  - <span data-ttu-id="20929-p105">Der Benutzer befindet sich an einem bekannten Netzwerkstandort, der sich von dem Netzwerkstandort unterscheidet, an dem sich das Gateway in das öffentliche Telefonnetz befindet (d. h., der Benutzer ist zu einem anderen Unternehmensstandort gereist). Das Routing ausgehender Anrufe erfolgt anhand der VoIP-Routingrichtlinie des Netzwerkstandorts, an dem sich der Benutzer befindet. Für den Benutzer aus dem öffentlichen Telefonnetz eingehende Anrufe werden nicht an Endpunkte geroutet, die sich an anderen Standorten befinden als das Gateway in das öffentliche Telefonnetz, um das Umgehen von Gebühren im öffentlichen Telefonnetz zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="20929-p105">The user is located in a known network site that is in different from the network site where the PSTN gateway is located. (i.e. the user traveled to another corporate office). The routing of outbound calls will be using the voice routing policy of the network site in which the user is located. Incoming PSTN calls to the user will not be routed to endpoints that are located in different sites than the PSTN gateway to prevent PSTN toll bypassing.</span></span>

  - <span data-ttu-id="20929-125">Wenn sich ein Benutzer in einer Netzwerk Website befindet, die der lync Server-Bereitstellung unbekannt ist, basiert das Routing von ausgehenden Anrufen auf der VoIP-Richtlinie, die dem Benutzer für PSTN-Gateways zugewiesen ist, die nicht an Location-Based Routing Einschränkungen gebunden sind.</span><span class="sxs-lookup"><span data-stu-id="20929-125">When a user is located in a network site that is unknown to the Lync Server deployment, the routing of outbound calls will be based on the voice policy assigned to the user to PSTN gateways not bound to Location-Based Routing restrictions.</span></span> <span data-ttu-id="20929-126">Eingehende Anrufe aus dem öffentlichen Telefonnetz werden nicht an Endpunkte geroutet, die sich an unbekannten Netzwerkstandorten befinden, um das Umgehen von Gebühren im öffentlichen Telefonnetz zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="20929-126">Incoming PSTN calls will not be routed to endpoints that are located in unknown network sites to prevent PSTN toll bypassing.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="20929-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="20929-127">See Also</span></span>


[<span data-ttu-id="20929-128">Anleitungen für das standortbasierte Routing in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="20929-128">Guidance for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-guidance-for-location-based-routing.md)  
  

<span data-ttu-id="20929-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="20929-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

