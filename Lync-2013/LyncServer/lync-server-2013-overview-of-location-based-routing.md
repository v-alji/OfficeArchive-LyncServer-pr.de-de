---
title: 'Lync Server 2013: Übersicht über Location-Based Routing'
description: 'Lync Server 2013: Übersicht über Location-Based-Routing.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Location-Based Routing
ms:assetid: 4aa494bd-0d66-4335-b9e8-f758d44a7202
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994032(v=OCS.15)
ms:contentKeyID: 51803941
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b1e026791a8562629231b91b58d7e7eff569ffa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394979"
---
# <a name="overview-of-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="ddb86-103">Übersicht über Location-Based-Routing in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ddb86-103">Overview of Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ddb86-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ddb86-104">

<span> </span></span></span>

<span data-ttu-id="ddb86-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="ddb86-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="ddb86-p101">Das standortbasierte Routing stellt einen neuen Regelsatz zur Verfügung, mit dem das Routing nationaler und internationaler PSTN-Anrufe modifiziert werden kann, um eine Gebührenumgehung zu verhindern. Beim standortbasierten Routing lassen sich die Regeln flexibel auf bestimmte Regionen und Gateways und sogar auf bestimmte Benutzergruppen beschränken.</span><span class="sxs-lookup"><span data-stu-id="ddb86-p101">Location-Based Routing introduces a new set of rules that modifies the routing of national and international PSTN calls to prevent toll bypass. Location-Based Routing provides the flexibility to scope these rules to specific regions, specific gateways or to specific set of users only.</span></span>

<span data-ttu-id="ddb86-108">Die folgenden Szenarien veranschaulichen die wichtigsten Arten von Einschränkungen, die Location-Based Routing erzwingen kann:</span><span class="sxs-lookup"><span data-stu-id="ddb86-108">The following scenarios illustrate the main types of restrictions Location-Based Routing can enforce:</span></span>

  - <span data-ttu-id="ddb86-109">Ausstiegs Anrufe – Location-Based Routing kann ausgehende Aufrufe von einem PSTN-Gateway erzwingen, das sich in der gleichen Region befindet wie der Aufrufer, um die PSTN-Maut Umgehung zu verhindern, wodurch Anrufe von einem PSTN-Gateway in einer anderen Region als der Aufrufer verhindert werden.</span><span class="sxs-lookup"><span data-stu-id="ddb86-109">Egress calls – Location-Based Routing can enforce outgoing calls to egress from a PSTN gateway that is located in the same region as where the caller is to prevent PSTN toll bypass, which prevents calls to egress from a PSTN gateway located in a different region as the caller.</span></span>

  - <span data-ttu-id="ddb86-110">Ingress-Anrufe – Location-Based Routing kann verhindern, dass eingehende PSTN-Anrufe lync-Endpunkte anrufen, wenn sich das PSTN-Gateway, in dem sich der eingehende Anruf befindet, nicht in derselben Region wie der angerufene lync-Benutzer befindet.</span><span class="sxs-lookup"><span data-stu-id="ddb86-110">Ingress calls – Location-Based Routing can prevent incoming PSTN calls to ring Lync endpoints if the PSTN gateway routing the incoming call is not located in the same region as the called Lync user.</span></span>

  - <span data-ttu-id="ddb86-111">Unbekannte Regionen – Location-Based Routing schränkt eingehende und ausgehende PSTN-Anrufe von und zu Benutzern ein, die sich an unbestimmten Speicherorten befinden (also Remotebenutzer, die eine Verbindung mit dem Internet herstellen oder sich in unbekannten Regionen befinden).</span><span class="sxs-lookup"><span data-stu-id="ddb86-111">Unknown regions – Location-Based Routing restricts incoming and outgoing PSTN calls to and from users that are located in undetermined locations (i.e. remote users connecting from the Internet or located in unknown regions).</span></span>

  - <span data-ttu-id="ddb86-112">Internationale Regionen – Location-Based Routing erzwingt die Weiterleitung von ausgehenden Anrufen über internationale PSTN-Gateways, wenn ein Gateway lokal zum Standort des Benutzers nicht gefunden werden kann.</span><span class="sxs-lookup"><span data-stu-id="ddb86-112">International regions – Location-Based Routing enforces routing of outgoing calls through international PSTN gateways if a gateway local to the user’s location cannot be found.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="ddb86-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ddb86-113">See Also</span></span>


[<span data-ttu-id="ddb86-114">Planung des standortbasierten Routings in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ddb86-114">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="ddb86-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ddb86-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

