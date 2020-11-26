---
title: 'Lync Server 2013: Technische Anforderungen für die Medienumgehung'
description: 'Lync Server 2013: Technische Voraussetzungen für die medienumgehung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for media bypass
ms:assetid: 6162a204-0e7c-460a-8eb2-e592c6590a8a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398435(v=OCS.15)
ms:contentKeyID: 48184321
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dee594139031966342fcec2bc1296a603055b4cc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423435"
---
# <a name="technical-requirements-for-media-bypass-in-lync-server-2013"></a><span data-ttu-id="5c8ea-103">Technische Anforderungen für die Medienumgehung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c8ea-103">Technical requirements for media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5c8ea-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5c8ea-104">

<span> </span></span></span>

<span data-ttu-id="5c8ea-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="5c8ea-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="5c8ea-106">Für jeden Anruf an das PSTN ermittelt der Vermittlungsserver, ob Medien vom lync-Endpunkt des Ursprungs direkt an einen Vermittlungsserver-Peer gesendet werden können, ohne den Vermittlungsserver zu durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="5c8ea-106">For each call to the PSTN, the Mediation Server determines whether media from the Lync endpoint of origin can be sent directly to a Mediation Server peer without traversing the Mediation Server.</span></span> <span data-ttu-id="5c8ea-107">Der Peer kann ein PSTN-Gateway, eine IP-Nebenstellenanlage oder ein SBC (Session Border Controller) bei einem Anbieter von Internettelefoniediensten sein, der zu der Leitung zwischen dem Vermittlungsserver gehört, bei dem der Anruf weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="5c8ea-107">The peer can be a PSTN gateway, IP-PBX, or Session Border Controller (SBC) at an Internet telephony service provider (ITSP) that is associated with the trunk between the Mediation Server where the call is routed.</span></span>

<span data-ttu-id="5c8ea-108">Die Medienumgehung kann implementiert werden, wenn die folgenden Voraussetzungen erfüllt sind:</span><span class="sxs-lookup"><span data-stu-id="5c8ea-108">Media bypass can be employed when the following requirements are met:</span></span>

  - <span data-ttu-id="5c8ea-109">Ein Vermittlungs Server-Peer muss die erforderlichen Funktionen für die medienumgehung unterstützen, wobei das wichtigste die Möglichkeit ist, mehrere gegabelte Antworten (so genannte "frühe Dialogfelder") zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="5c8ea-109">A Mediation Server peer must support the necessary capabilities for media bypass, the most important being the ability to handle multiple forked responses (known as “early dialogs”).</span></span> <span data-ttu-id="5c8ea-110">Wenden Sie sich an den Hersteller Ihres Gateways oder Ihrer Telefonanlage oder Ihres ITSP, um den Wert für die maximale Anzahl der frühen Dialogfelder abzurufen, die das Gateway, die Telefonanlage oder SBC akzeptieren können.</span><span class="sxs-lookup"><span data-stu-id="5c8ea-110">Contact the manufacturer of your gateway or PBX, or your ITSP, to obtain the value for the maximum number of early dialogs that the gateway, PBX, or SBC can accept.</span></span>

  - <span data-ttu-id="5c8ea-111">Der Vermittlungs Server-Peer muss Mediendatenverkehr direkt von lync-Endpunkten akzeptieren.</span><span class="sxs-lookup"><span data-stu-id="5c8ea-111">The Mediation Server peer must accept media traffic directly from Lync endpoints.</span></span> <span data-ttu-id="5c8ea-112">Mit vielen ITSPs können Ihre SBC nur Datenverkehr vom Vermittlungs Server empfangen.</span><span class="sxs-lookup"><span data-stu-id="5c8ea-112">Many ITSPs allow their SBC to receive traffic only from the Mediation Server.</span></span> <span data-ttu-id="5c8ea-113">Wenden Sie sich an Ihren ITSP, um festzustellen, ob der SBC Mediendatenverkehr direkt von lync-Endpunkten akzeptiert.</span><span class="sxs-lookup"><span data-stu-id="5c8ea-113">Contact your ITSP to determine whether its SBC accepts media traffic directly from Lync endpoints.</span></span>

  - <span data-ttu-id="5c8ea-114">Lync-Clients und ein Vermittlungs Server-Peer müssen gut verbunden sein, d. h., Sie befinden sich entweder im gleichen Netzwerkbereich oder auf Netzwerkstandorten, die eine Verbindung mit der Region über WAN-Links herstellen, die keine Bandbreiteneinschränkungen aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5c8ea-114">Lync clients and a Mediation Server peer must be well connected, meaning that they are either located in the same network region or at network sites that connect to the region over WAN links that have no bandwidth constraints</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="5c8ea-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5c8ea-115">See Also</span></span>


[<span data-ttu-id="5c8ea-116">Modi für die Medienumgehung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c8ea-116">Media bypass modes in Lync Server 2013</span></span>](lync-server-2013-media-bypass-modes.md)  
[<span data-ttu-id="5c8ea-117">Medienumgehung und Anrufsteuerung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c8ea-117">Media bypass and call admission control in Lync Server 2013</span></span>](lync-server-2013-media-bypass-and-call-admission-control.md)  
  

<span data-ttu-id="5c8ea-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5c8ea-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

