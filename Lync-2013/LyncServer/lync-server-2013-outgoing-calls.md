---
title: 'Lync Server 2013: Ausgehende Anrufe'
description: 'Lync Server 2013: ausgehende Anrufe.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Outgoing calls
ms:assetid: 885ffe6f-cd51-4f21-8d4f-a1ff8d818858
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994049(v=OCS.15)
ms:contentKeyID: 51803960
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e14f19dec35a6da47a2ddd62657d5d087a854f16
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424835"
---
# <a name="outgoing-calls-in-lync-server-2013"></a><span data-ttu-id="e616c-103">Ausgehende Anrufe in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e616c-103">Outgoing calls in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e616c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e616c-104">

<span> </span></span></span>

<span data-ttu-id="e616c-105">_**Letztes Änderungsdatum des Themas:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="e616c-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="e616c-106">Das Routing von ausgehenden Anrufen von Benutzern, die für Location-Based Routing aktiviert sind, ist vom Netzwerkspeicherort des Endpunkts des Benutzers betroffen.</span><span class="sxs-lookup"><span data-stu-id="e616c-106">The routing of outbound calls of users enabled for Location-Based Routing is affected by the network location of the user’s endpoint.</span></span> <span data-ttu-id="e616c-107">In der folgenden Tabelle wird gezeigt, wie sich Location-Based-Routing auf das Routing von ausgehenden Anrufen auswirkt, abhängig von der Position des Endpunkts des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="e616c-107">The following table illustrates how Location-Based Routing affects the routing of outbound calls depending on the location of the caller’s endpoint.</span></span>

### <a name="caller-placing-an-outbound-call-to-the-pstn"></a><span data-ttu-id="e616c-108">Der Anrufer tätigt einen ausgehenden Anruf in das öffentliche Telefonnetz</span><span class="sxs-lookup"><span data-stu-id="e616c-108">Caller placing an outbound call to the PSTN</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="e616c-109">Der Benutzerendpunkt befindet sich an einem Netzwerkstandort, der für standortbasiertes Routing aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="e616c-109">User endpoint located in a network site enabled for Location-Based Routing</span></span></th>
<th><span data-ttu-id="e616c-110">Der Benutzerendpunkt befindet sich an einem unbekannten Netzwerkstandort oder einem Standort, der nicht für standortbasiertes Routing aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="e616c-110">User endpoint located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e616c-111">Autorisierung ausgehender Anrufe</span><span class="sxs-lookup"><span data-stu-id="e616c-111">Authorization of outbound calls</span></span></p></td>
<td><p><span data-ttu-id="e616c-112">Der Anruf wird basierend auf der VoIP-Richtlinie des Benutzers autorisiert</span><span class="sxs-lookup"><span data-stu-id="e616c-112">Call is authorized based on user’s voice policy</span></span></p></td>
<td><p><span data-ttu-id="e616c-113">Der Anruf wird basierend auf der VoIP-Richtlinie des Benutzers autorisiert</span><span class="sxs-lookup"><span data-stu-id="e616c-113">Call is authorized based on user’s voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e616c-114">Routing ausgehender Anrufe</span><span class="sxs-lookup"><span data-stu-id="e616c-114">Routing of outbound call</span></span></p></td>
<td><p><span data-ttu-id="e616c-115">Das Routing des Anrufs erfolgt gemäß der VoIP-Routingrichtlinie des Netzwerkstandorts</span><span class="sxs-lookup"><span data-stu-id="e616c-115">Call is routed according to the network site’s voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="e616c-116">Der Anruf wird gemäß der VoIP-Richtlinie des Benutzers geroutet, jedoch nur durch Trunks, die nicht für standortbasiertes Routing aktiviert sind (sofern verfügbar)</span><span class="sxs-lookup"><span data-stu-id="e616c-116">Call is routed according to user’s voice policy and only through trunks not enabled for Location-Based Routing (if available)</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="e616c-117">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e616c-117">See Also</span></span>


[<span data-ttu-id="e616c-118">Szenarien für das standortbasierte Routing in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e616c-118">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="e616c-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e616c-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

