---
title: 'Lync Server 2013: Medienumgehung und Vermittlungsserver'
description: 'Lync Server 2013: medienumgehung und Vermittlungsserver.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media bypass and Mediation Server
ms:assetid: 8ed35f95-05cd-4b5d-8470-442d2323df71
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398719(v=OCS.15)
ms:contentKeyID: 48184774
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ebb005d3d52fa9e5a38fdf56a65dfcbd73616d87
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425703"
---
# <a name="media-bypass-and-mediation-server-in-lync-server-2013"></a><span data-ttu-id="a5fe0-103">Medienumgehung und Vermittlungsserver in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a5fe0-103">Media bypass and Mediation Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a5fe0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a5fe0-104">

<span> </span></span></span>

<span data-ttu-id="a5fe0-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="a5fe0-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="a5fe0-106">Bei der medienumgehung handelt es sich um eine lync-Server Funktion, mit der ein Administrator das Anrufrouting so konfigurieren kann, dass es direkt zwischen dem Benutzer Endpunkt und dem PSTN-Gateway (Public Switched Telephone Network) erfolgt, ohne den Vermittlungs Server zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="a5fe0-106">Media bypass is a Lync Server capability that enables an administrator to configure call routing to flow directly between the user endpoint and the public switched telephone network (PSTN) gateway without traversing the Mediation Server.</span></span> <span data-ttu-id="a5fe0-107">Die medienumgehung verbessert die Anrufqualität, indem Latenz, unnötige Übersetzung, Möglichkeit des Paketverlusts und die Anzahl potenzieller Fehlerpunkte reduziert werden.</span><span class="sxs-lookup"><span data-stu-id="a5fe0-107">Media bypass improves call quality by reducing latency, unnecessary translation, possibility of packet loss, and the number of potential points of failure.</span></span> <span data-ttu-id="a5fe0-108">Wenn ein Remotestandort ohne Vermittlungs Server über eine oder mehrere WAN-Links mit eingeschränkter Bandbreite mit einem zentralen Standort verbunden ist, senkt die medienumgehung die Bandbreitenanforderung, indem Medien von einem Client an einem Remotestandort direkt an sein lokales Gateway übermittelt werden können, ohne dass zuvor über die WAN-Verbindung zu einem Vermittlungs Server am zentralen Standort und zurück weiter fließen muss. Diese Verringerung der Medienverarbeitung ergänzt auch die Möglichkeit des Vermittlungsservers, mehrere Gateways zu steuern.</span><span class="sxs-lookup"><span data-stu-id="a5fe0-108">Where a remote site without a Mediation Server is connected to a central site by one or more WAN links with constrained bandwidth, media bypass lowers the bandwidth requirement by enabling media from a client at a remote site to flow directly to its local gateway without first having to flow across the WAN link to a Mediation Server at the central site and back.This reduction in media processing also complements the Mediation Server’s ability to control multiple gateways.</span></span>

<span data-ttu-id="a5fe0-p102">Die Medienumgehung und die Anrufsteuerung schließen sich gegenseitig aus. Wenn für einen Anruf die Medienumgehung implementiert wird, wird für diesen Anruf keine Anrufsteuerung ausgeführt. Es wird davon ausgegangen, dass für den Anruf keine Verbindungen mit beschränkter Bandbreite verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a5fe0-p102">Media bypass and call admission control (CAC) are mutually exclusive. If media bypass is employed for a call, CAC is not performed for that call. The assumption is that there are no links with constrained bandwidth involved in the call.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="a5fe0-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a5fe0-112">See Also</span></span>


[<span data-ttu-id="a5fe0-113">Anrufsteuerung und Vermittlungsserver in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a5fe0-113">Call admission control and Mediation Server in Lync Server 2013</span></span>](lync-server-2013-call-admission-control-and-mediation-server.md)  


[<span data-ttu-id="a5fe0-114">Planung der Medienumgehung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a5fe0-114">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
  

<span data-ttu-id="a5fe0-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a5fe0-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

