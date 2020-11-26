---
title: 'Lync Server 2013: Vom standortbasierten Routing nicht unterstützte Funktionen'
description: 'Lync Server 2013: Funktionen, die von Location-Based Routing nicht unterstützt werden.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capabilities not supported by Location-Based Routing
ms:assetid: c3d54953-a7d6-4465-a6c3-ae411b2d8ea9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994071(v=OCS.15)
ms:contentKeyID: 51803982
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf9cd03a8cbdd50e136605c4f172598b2ad3f523
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435607"
---
# <a name="capabilities-not-supported-by-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="90c8e-103">Vom standortbasierten Routing nicht unterstützte Funktionen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="90c8e-103">Capabilities not supported by Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="90c8e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="90c8e-104">

<span> </span></span></span>

<span data-ttu-id="90c8e-105">_**Letztes Änderungsdatum des Themas:** 2014-03-12_</span><span class="sxs-lookup"><span data-stu-id="90c8e-105">_**Topic Last Modified:** 2014-03-12_</span></span>

<span data-ttu-id="90c8e-106">Location-Based Routing gilt nicht für die folgenden Arten von Interaktionen.</span><span class="sxs-lookup"><span data-stu-id="90c8e-106">Location-Based Routing does not apply to the following types of interactions.</span></span> <span data-ttu-id="90c8e-107">Location-Based Routing wird nicht erzwungen, wenn lync-Endpunkte mithilfe dieser Funktionen mit PSTN-Endpunkten interagieren.</span><span class="sxs-lookup"><span data-stu-id="90c8e-107">Location-Based Routing is not enforced when Lync endpoints interact with PSTN endpoints using these capabilities.</span></span>

  - <span data-ttu-id="90c8e-108">PSTN-Einwahl bei Konferenzen</span><span class="sxs-lookup"><span data-stu-id="90c8e-108">PSTN dial-in to conferences</span></span>

  - <span data-ttu-id="90c8e-109">Eingehende und ausgehende PSTN-Anrufe über die Reaktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="90c8e-109">Incoming and outgoing PSTN calls through Response Group</span></span>

  - <span data-ttu-id="90c8e-110">Parken von Anrufen oder Abrufen von PSTN-Anrufen über das Parken von Anrufen</span><span class="sxs-lookup"><span data-stu-id="90c8e-110">Call park or retrieval of PSTN calls through Call Park</span></span>

  - <span data-ttu-id="90c8e-111">Eingehende PSTN-Anrufe an den Ankündigungsdienst</span><span class="sxs-lookup"><span data-stu-id="90c8e-111">Incoming PSTN calls to Announcement Service</span></span>

  - <span data-ttu-id="90c8e-112">Eingehende PSTN-Anrufe, die über die Gruppenanrufannahme abgerufen werden</span><span class="sxs-lookup"><span data-stu-id="90c8e-112">Incoming PSTN calls retrieved via Group Call Pickup</span></span>

<span data-ttu-id="90c8e-113">Wenn Sie Location-Based Routingregeln für die Typen von Interaktionen in der folgenden Liste erzwingen möchten, müssen Sie Location-Based Routing für Konferenzen aktivieren:</span><span class="sxs-lookup"><span data-stu-id="90c8e-113">To enforce Location-Based Routing rules to the types of interactions in the following list, you must enable Location-Based Routing for Conferencing:</span></span>

  - <span data-ttu-id="90c8e-114">PSTN-Einwahl von Konferenzen</span><span class="sxs-lookup"><span data-stu-id="90c8e-114">PSTN dial-out from conferences</span></span>

  - <span data-ttu-id="90c8e-115">Eskalationen von Peer-zu-Peer-Audiounterhaltungen in Konferenzen unter Beteiligung von PSTN-Endpunkten</span><span class="sxs-lookup"><span data-stu-id="90c8e-115">Escalations from peer-to-peer audio conversations to conferencing involving PSTN endpoints</span></span>

  - <span data-ttu-id="90c8e-116">Anrufdurchstellung nach Rücksprache unter Beteiligung von PSTN-Endpunkten</span><span class="sxs-lookup"><span data-stu-id="90c8e-116">Consultative transfers involving PSTN endpoints</span></span>

<span data-ttu-id="90c8e-117">Informationen zum Aktivieren von Location-Based Routing für Konferenzen finden Sie unter [standortbasiertes Routing für Konferenzen in lync Server 2013](lync-server-2013-location-based-routing-for-conferencing.md).</span><span class="sxs-lookup"><span data-stu-id="90c8e-117">To enable Location-Based Routing for Conferencing, see [Location-Based Routing for conferencing in Lync Server 2013](lync-server-2013-location-based-routing-for-conferencing.md).</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="90c8e-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="90c8e-118">See Also</span></span>


[<span data-ttu-id="90c8e-119">Planung des standortbasierten Routings in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="90c8e-119">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)  
  

<span data-ttu-id="90c8e-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="90c8e-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

