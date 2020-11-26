---
title: 'Lync Server 2013: Planung des standortbasierten Routings'
description: 'Lync Server 2013: Planen des Location-Based Routings'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Location-Based Routing
ms:assetid: bb035924-6b52-4f0f-8e05-b76864fb9ef3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994068(v=OCS.15)
ms:contentKeyID: 51803979
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 894a596e998fe07b97ad7911441eced670ba85b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442950"
---
# <a name="planning-for-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="bef7d-103">Planung des standortbasierten Routings in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bef7d-103">Planning for Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bef7d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bef7d-104">

<span> </span></span></span>

<span data-ttu-id="bef7d-105">_**Letztes Änderungsdatum des Themas:** 2013-07-31_</span><span class="sxs-lookup"><span data-stu-id="bef7d-105">_**Topic Last Modified:** 2013-07-31_</span></span>

<span data-ttu-id="bef7d-106">Die Informationen in diesem Thema beziehen sich auf kumulierte Updates für Lync Server 2013: February 2013.</span><span class="sxs-lookup"><span data-stu-id="bef7d-106">The information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.</span></span>

<span data-ttu-id="bef7d-107">Location-Based Routing ermöglicht es, das Routing von anrufen zwischen VoIP-Endpunkten und PSTN-Endpunkten basierend auf dem Standort der Gesprächspartner zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="bef7d-107">Location-Based Routing makes it possible to restrict the routing of calls between VoIP endpoints and PSTN endpoints based on the location of the parties in the call.</span></span> <span data-ttu-id="bef7d-108">Location-Based Routing ist Teil der lync Server 2013 Enterprise Voice-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="bef7d-108">Location-Based Routing is part of the Lync Server 2013 Enterprise Voice infrastructure.</span></span> <span data-ttu-id="bef7d-109">Location-Based Routing ist ein Anruf Verwaltungsfeature, das steuert, wie Anrufe von lync Server 2013 CU1 weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="bef7d-109">Location-Based Routing is a call management feature that controls how calls are routed by Lync Server 2013 CU1.</span></span> <span data-ttu-id="bef7d-110">Sie erzwingt Anruf Autorisierungsregeln, um festzulegen, ob Anrufe auf der Grundlage des geografischen Standorts des lync-Anrufers an PBX-oder PSTN-Endpunkte weitergeleitet werden können.</span><span class="sxs-lookup"><span data-stu-id="bef7d-110">It enforces call authorization rules on whether calls can be routed to PBX or PSTN endpoints based on the Lync caller’s geographic location.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="bef7d-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="bef7d-111">In This Section</span></span>

  - [<span data-ttu-id="bef7d-112">Übersicht über Location-Based-Routing in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bef7d-112">Overview of Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-overview-of-location-based-routing.md)

  - [<span data-ttu-id="bef7d-113">Anleitungen für das standortbasierte Routing in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bef7d-113">Guidance for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-guidance-for-location-based-routing.md)

  - [<span data-ttu-id="bef7d-114">Szenarien für das standortbasierte Routing in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bef7d-114">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)

  - [<span data-ttu-id="bef7d-115">Technische Überlegungen zum standortbasierten Routing in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bef7d-115">Technical considerations for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-technical-considerations-for-location-based-routing.md)

  - [<span data-ttu-id="bef7d-116">Client- und Serverunterstützung für standortbasiertes Routing in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bef7d-116">Client and server support for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-client-and-server-support-for-location-based-routing.md)

  - [<span data-ttu-id="bef7d-117">Vom standortbasierten Routing nicht unterstützte Funktionen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bef7d-117">Capabilities not supported by Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-capabilities-not-supported-by-location-based-routing.md)

  - [<span data-ttu-id="bef7d-118">Bereitstellungsvorgang beim standortbasierten Routing in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bef7d-118">Deployment process for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-location-based-routing.md)

  - [<span data-ttu-id="bef7d-119">Standortbasiertes Routing für Konferenzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bef7d-119">Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-location-based-routing-for-conferencing.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="bef7d-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bef7d-120">See Also</span></span>


[<span data-ttu-id="bef7d-121">Planen von Enterprise-VoIP in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bef7d-121">Planning for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice.md)  
  

<span data-ttu-id="bef7d-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bef7d-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

