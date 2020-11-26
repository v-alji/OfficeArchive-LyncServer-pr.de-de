---
title: 'Lync Server 2013: Planen des Anrufsteuerungsdiensts'
description: 'Lync Server 2013: Planen der Anrufsteuerung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for call admission control (CAC)
ms:assetid: ca367138-adf5-4119-bc40-5ddf335ed22f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398842(v=OCS.15)
ms:contentKeyID: 48185652
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: afbc3ca411fcf0a3a1c869a23cddccdb87f09ed6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437042"
---
# <a name="planning-for-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="7c163-103">Planen des Anrufsteuerungsdiensts in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7c163-103">Planning for call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7c163-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7c163-104">

<span> </span></span></span>

<span data-ttu-id="7c163-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="7c163-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="7c163-106">Für UC-Anwendungen (Unified Communications), die IP-basiert sind, wie Telefonie, Video und Anwendungsfreigabe, wird die verfügbare Bandbreite von Unternehmensnetzwerken im Allgemeinen nicht als limitierender Faktor in LAN-Umgebungen angesehen.</span><span class="sxs-lookup"><span data-stu-id="7c163-106">For unified communications (UC) applications that are IP-based, such as telephony, video, and application sharing, the available bandwidth of enterprise networks is not generally considered to be a limiting factor within LAN environments.</span></span> <span data-ttu-id="7c163-107">Wenn Standorte jedoch über ein WAN verbunden sind, kann die Bandbreite eingeschränkt sein.</span><span class="sxs-lookup"><span data-stu-id="7c163-107">However, on WAN links that interconnect sites, network bandwidth can be limited.</span></span> <span data-ttu-id="7c163-108">Wenn ein Zustrom von Netzwerkdatenverkehr eine WAN-Verbindung überzeichnet, werden aktuelle Mechanismen wie Warteschlangen, Pufferung und Paket Abwurf verwendet, um die Überlastung zu beheben.</span><span class="sxs-lookup"><span data-stu-id="7c163-108">When an influx of network traffic oversubscribes a WAN link, current mechanisms such as queuing, buffering, and packet dropping are used to resolve the congestion.</span></span> <span data-ttu-id="7c163-109">Der zusätzliche Datenverkehr wird üblicherweise verzögert, bis die Überlastung aufgehoben ist, oder gegebenenfalls verworfen.</span><span class="sxs-lookup"><span data-stu-id="7c163-109">The extra traffic is typically delayed until the network congestion eases or, if necessary, the traffic is dropped.</span></span> <span data-ttu-id="7c163-110">Bei herkömmlichem Datenverkehr kann der Empfängerclient die Daten in solchen Situationen wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="7c163-110">For conventional data traffic in such situations, the receiving client can recover.</span></span> <span data-ttu-id="7c163-111">Für echtzeitdatenverkehr wie Unified Communications kann die Netzwerküberlastung auf diese Weise nicht aufgelöst werden, da der Unified Communications-Datenverkehr sowohl auf Latenz als auch auf Paketverluste reagiert.</span><span class="sxs-lookup"><span data-stu-id="7c163-111">For real-time traffic such as unified communications, network congestion cannot be resolved in this manner, because the unified communications traffic is sensitive to both latency and packet loss.</span></span> <span data-ttu-id="7c163-112">Eine Überlastung des WAN kann zu einer unzureichenden Erlebnisqualität für Benutzer führen.</span><span class="sxs-lookup"><span data-stu-id="7c163-112">Congestion on the WAN can result in a poor Quality of Experience (QoE) for users.</span></span> <span data-ttu-id="7c163-113">Für Echtzeitverkehr in überlasteten Situationen ist es besser, Anrufe zu verweigern, als Verbindungen mit schlechter Qualität bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="7c163-113">For real-time traffic in congested conditions, it is better to deny calls than to provide connections with poor quality.</span></span>

<span data-ttu-id="7c163-114">Die Anrufsteuerung (Call Admission Control, CAC) ermittelt, ob ausreichend Netzwerkbandbreite für eine Echtzeitsitzung in akzeptabler Qualität vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="7c163-114">Call admission control (CAC) determines whether there is sufficient network bandwidth to establish a real-time session of acceptable quality.</span></span> <span data-ttu-id="7c163-115">In lync Server 2013 steuert CAC den Echtzeitverkehr nur für Audio und Video, hat aber keinen Einfluss auf den Datenverkehr.</span><span class="sxs-lookup"><span data-stu-id="7c163-115">In Lync Server 2013, CAC controls real-time traffic only for audio and video, but it does not affect data traffic.</span></span> <span data-ttu-id="7c163-116">Wenn der WAN-Standardpfad nicht die erforderliche Bandbreite aufweist, kann die Anrufsteuerung versuchen, den Anruf über einen Internetpfad oder das Festnetz zu leiten.</span><span class="sxs-lookup"><span data-stu-id="7c163-116">If the default WAN path does not have the required bandwidth, CAC can attempt to route the call through an Internet path or the public switched telephone network (PSTN).</span></span> <span data-ttu-id="7c163-117">CAC steht nur in lync Server zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="7c163-117">CAC is available only in Lync Server.</span></span>

<span data-ttu-id="7c163-118">In diesem Abschnitt wird die Funktionsweise der Anrufsteuerung beschrieben und es wird erläutert, wie die Anrufsteuerung geplant werden kann.</span><span class="sxs-lookup"><span data-stu-id="7c163-118">This section describes the call admission control functionality and explains how to plan for CAC.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7c163-119">Lync Server verfügt über drei erweiterte Enterprise-VoIP-Features: Anrufannahme Steuerung (CAC), Notfalldienste (E9-1-1) und medienumgehung.</span><span class="sxs-lookup"><span data-stu-id="7c163-119">Lync Server has three advanced Enterprise Voice features: call admission control (CAC), emergency services (E9-1-1), and media bypass.</span></span> <span data-ttu-id="7c163-120">Eine Übersicht über die Planungsinformationen, die für alle drei Features üblich sind, finden Sie unter <A href="lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md">Netzwerkeinstellungen für die erweiterten Enterprise-VoIP-Features in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="7c163-120">For an overview of planning information that is common to all three of these features, see <A href="lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md">Network settings for the advanced Enterprise Voice features in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7c163-121">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="7c163-121">In This Section</span></span>

  - [<span data-ttu-id="7c163-122">Übersicht über die Anrufsteuerung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7c163-122">Overview of call admission control in Lync Server 2013</span></span>](lync-server-2013-overview-of-call-admission-control.md)

  - [<span data-ttu-id="7c163-123">Definieren der Anforderungen Ihrer Organisation für die Anrufsteuerung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7c163-123">Defining your requirements for call admission control in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-call-admission-control.md)

  - [<span data-ttu-id="7c163-124">Beispiel: Erfassen Ihrer Anforderungen für die Anrufsteuerung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7c163-124">Example: Gathering your requirements for call admission control in Lync Server 2013</span></span>](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md)

  - [<span data-ttu-id="7c163-125">Komponenten und Topologien für die Anrufsteuerung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7c163-125">Components and topologies for CAC in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-cac.md)

  - [<span data-ttu-id="7c163-126">Bewährte Methoden für die Anrufsteuerung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7c163-126">Best practices for call admission control in Lync Server 2013</span></span>](lync-server-2013-best-practices-for-call-admission-control.md)

  - [<span data-ttu-id="7c163-127">Prüfliste für die Bereitstellung der Anrufsteuerung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7c163-127">Deployment checklist for call admission control in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-call-admission-control.md)

<span data-ttu-id="7c163-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7c163-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

