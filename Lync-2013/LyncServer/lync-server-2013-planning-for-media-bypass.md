---
title: 'Lync Server 2013: Planung der Medienumgehung'
description: 'Lync Server 2013: Planen der medienumgehung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for media bypass
ms:assetid: 8ac732b6-8538-4d7b-b1a9-2035e419dac2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398703(v=OCS.15)
ms:contentKeyID: 48184768
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7d92a50d9d838b0f13fd6837cbfadee1c48712f0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424488"
---
# <a name="planning-for-media-bypass-in-lync-server-2013"></a><span data-ttu-id="9f8b3-103">Planung der Medienumgehung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f8b3-103">Planning for media bypass in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9f8b3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9f8b3-104">

<span> </span></span></span>

<span data-ttu-id="9f8b3-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="9f8b3-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="9f8b3-106">Medienumgehung bezieht sich auf das Entfernen des Vermittlungsservers aus dem Medienpfad, wenn möglich, für Anrufe, deren Signalisierung den Vermittlungsserver durchquert.</span><span class="sxs-lookup"><span data-stu-id="9f8b3-106">Media bypass refers to removing the Mediation Server from the media path whenever possible for calls whose signaling traverses the Mediation Server.</span></span>

<span data-ttu-id="9f8b3-107">Die Medienumgehung kann die Sprachqualität verbessern, indem die Latenz verringert, eine unnötige Übersetzung und Paketverluste verhindert sowie potenzielle Fehlerstellen minimiert werden.</span><span class="sxs-lookup"><span data-stu-id="9f8b3-107">Media bypass can improve voice quality by reducing latency, needless translation, possibility of packet loss, and the number of points of potential failure.</span></span> <span data-ttu-id="9f8b3-108">Die Skalierbarkeit kann verbessert werden, da durch die Eliminierung der Medienverarbeitung für Umgehungs Anrufe die Belastung des Vermittlungsservers verringert wird.</span><span class="sxs-lookup"><span data-stu-id="9f8b3-108">Scalability can be improved, because elimination of media processing for bypassed calls reduces the load on the Mediation Server.</span></span> <span data-ttu-id="9f8b3-109">Diese Verringerung der Auslastung ergänzt die Möglichkeit des Vermittlungsservers, mehrere Gateways zu steuern.</span><span class="sxs-lookup"><span data-stu-id="9f8b3-109">This reduction in load complements the ability of the Mediation Server to control multiple gateways.</span></span>

<span data-ttu-id="9f8b3-110">Wenn eine Verzweigungs Website ohne Vermittlungs Server über eine oder mehrere WAN-Links mit eingeschränkter Bandbreite mit einem zentralen Standort verbunden ist, verringert die medienumgehung die Bandbreitenanforderung, indem Medien von einem Client an einer Zweigstelle direkt an das lokale Gateway übermittelt werden können, ohne dass zuvor die WAN-Verbindung zu einem Vermittlungs Server am zentralen Standort und zurück durchlaufen werden muss.</span><span class="sxs-lookup"><span data-stu-id="9f8b3-110">Where a branch site without a Mediation Server is connected to a central site by one or more WAN links with constrained bandwidth, media bypass lowers the bandwidth requirement by allowing media from a client at a branch site to flow directly to its local gateway without first having to flow across the WAN link to a Mediation Server at the central site and back.</span></span>

<span data-ttu-id="9f8b3-111">Durch die Entlastung des Vermittlungsservers von der Medienverarbeitung kann die medienumgehung auch die Anzahl der Vermittlungsserver verringern, die für eine Enterprise-VoIP-Infrastruktur erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="9f8b3-111">By relieving the Mediation Server from media processing, media bypass may also reduce the number of Mediation Servers that an Enterprise Voice infrastructure requires.</span></span>

<span data-ttu-id="9f8b3-112">Die folgende Abbildung zeigt grundlegende Pfade für Medien- und Signaldatenverkehr in Topologien mit und ohne Umgehung.</span><span class="sxs-lookup"><span data-stu-id="9f8b3-112">The following figure shows basic media and signaling pathways in topologies with and without media bypass.</span></span>

<span data-ttu-id="9f8b3-113">**Pfade für Medien- und Signaldatenverkehr mit und ohne Medienumgehung**</span><span class="sxs-lookup"><span data-stu-id="9f8b3-113">**Media and signaling pathways with and without media bypass**</span></span>

<span data-ttu-id="9f8b3-114">![Voice CAC Media Bypass-Verbindungserzwingung](images/Gg398703.4d66d529-0912-4de1-abec-266f54272eb3(OCS.15).jpg "Voice CAC Media Bypass-Verbindungserzwingung")</span><span class="sxs-lookup"><span data-stu-id="9f8b3-114">![Voice CAC Media Bypass Connection Enforcement](images/Gg398703.4d66d529-0912-4de1-abec-266f54272eb3(OCS.15).jpg "Voice CAC Media Bypass Connection Enforcement")</span></span>

<span data-ttu-id="9f8b3-115">Generell gilt, dass die Medienumgehung möglichst immer aktiviert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="9f8b3-115">As a general rule, enable media bypass wherever possible.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="9f8b3-116">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="9f8b3-116">In This Section</span></span>

  - [<span data-ttu-id="9f8b3-117">Übersicht über die medienumgehung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f8b3-117">Overview of media bypass in Lync Server 2013</span></span>](lync-server-2013-overview-of-media-bypass.md)

  - [<span data-ttu-id="9f8b3-118">Modi für die Medienumgehung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f8b3-118">Media bypass modes in Lync Server 2013</span></span>](lync-server-2013-media-bypass-modes.md)

  - [<span data-ttu-id="9f8b3-119">Medienumgehung und Anrufsteuerung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f8b3-119">Media bypass and call admission control in Lync Server 2013</span></span>](lync-server-2013-media-bypass-and-call-admission-control.md)

  - [<span data-ttu-id="9f8b3-120">Technische Anforderungen für die Medienumgehung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f8b3-120">Technical requirements for media bypass in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-media-bypass.md)

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="9f8b3-121">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="9f8b3-121">Related Sections</span></span>

[<span data-ttu-id="9f8b3-122">Bereitstellen von erweiterten Enterprise-VoIP-Features in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f8b3-122">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-deploying-advanced-enterprise-voice-features.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9f8b3-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f8b3-123">See Also</span></span>


[<span data-ttu-id="9f8b3-124">Configure a trunk with media bypass in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f8b3-124">Configure a trunk with media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-a-trunk-with-media-bypass.md)  


[<span data-ttu-id="9f8b3-125">Globale Medien Umgehungs Optionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f8b3-125">Global media bypass options in Lync Server 2013</span></span>](lync-server-2013-global-media-bypass-options.md)  
  

<span data-ttu-id="9f8b3-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9f8b3-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

