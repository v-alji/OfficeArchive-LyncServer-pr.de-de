---
title: 'Lync Server 2013: Verwalten der Lync Server 2013-Netzwerkinfrastruktur'
description: 'Lync Server 2013: Verwalten der lync Server 2013-Netzwerkinfrastruktur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing the Lync Server 2013 network infrastructure
ms:assetid: cb13456a-8f66-4595-be21-8887f30ad4eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182585(v=OCS.15)
ms:contentKeyID: 48185638
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ab1b5c6fe52374b012063ac26640e9bb25496ad7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425857"
---
# <a name="managing-the-lync-server-2013-network-infrastructure"></a><span data-ttu-id="97f06-103">Verwalten der Lync Server 2013-Netzwerkinfrastruktur</span><span class="sxs-lookup"><span data-stu-id="97f06-103">Managing the Lync Server 2013 network infrastructure</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="97f06-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="97f06-104">

<span> </span></span></span>

<span data-ttu-id="97f06-105">_**Letztes Änderungsdatum des Themas:** 2014-02-11_</span><span class="sxs-lookup"><span data-stu-id="97f06-105">_**Topic Last Modified:** 2014-02-11_</span></span>

<span data-ttu-id="97f06-106">Microsoft lync Server 2013 umfasst die Unterstützung für die Anrufannahme Steuerung (CAC) und die medienumgehung.</span><span class="sxs-lookup"><span data-stu-id="97f06-106">Microsoft Lync Server 2013 includes support for call admission control (CAC) and media bypass.</span></span> <span data-ttu-id="97f06-107">Um diese Features zu implementieren, müssen Sie ein Netzwerk von Regionen, Websites, Subnets usw. konfigurieren, mit dem Sie die Bandbreite in Situationen verwalten können, in denen Audio-und Videoübertragungen eingeschränkt werden müssen.</span><span class="sxs-lookup"><span data-stu-id="97f06-107">To implement these features you must configure a network of regions, sites, subnets, and so on that will allow you to manage bandwidth in situations where audio and video transmissions need to be restricted.</span></span> <span data-ttu-id="97f06-108">Sie können auch die Quality of Service (QoS)-Netzwerktechnologie verwenden, um ein optimales Endbenutzererlebnis für Audio-und Videokommunikation zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="97f06-108">You can also use the Quality of Service (QoS) networking technology to help provide an optimal end-user experience for audio and video communications.</span></span>

<span data-ttu-id="97f06-109">Sie können die lync Server-Systemsteuerung verwenden, um CAC, medienumgehung und QoS einzurichten und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="97f06-109">You can use the Lync Server Control Panel to set up and manage CAC, media bypass, and QoS.</span></span> <span data-ttu-id="97f06-110">In den folgenden Themen finden Sie eine schrittweise Anleitung dazu.</span><span class="sxs-lookup"><span data-stu-id="97f06-110">The following topics provide steps for how to do this.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="97f06-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="97f06-111">In This Section</span></span>

  - [<span data-ttu-id="97f06-112">Verwalten von QoS (Quality of Service) in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97f06-112">Managing Quality of Service (QoS) in Lync Server 2013</span></span>](lync-server-2013-managing-quality-of-service-qos.md)

  - [<span data-ttu-id="97f06-113">Verwalten der Anruf Zulassungs Steuerung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97f06-113">Managing call admission control in Lync Server 2013</span></span>](lync-server-2013-managing-call-admission-control.md)

  - [<span data-ttu-id="97f06-114">Lync Server 2013-Netzwerkschnittstellen</span><span class="sxs-lookup"><span data-stu-id="97f06-114">Lync Server 2013 network interfaces</span></span>](lync-server-2013-lync-server-network-interfaces.md)

  - [<span data-ttu-id="97f06-115">Verhindern neuer Verbindungen mit lync Server 2013 für die Server Wartung</span><span class="sxs-lookup"><span data-stu-id="97f06-115">Prevent new connections to Lync Server 2013 for server maintenance</span></span>](lync-server-2013-prevent-new-connections-to-lync-server-for-server-maintenance.md)

  - [<span data-ttu-id="97f06-116">Methodik der lync-Anrufqualität in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97f06-116">Lync Call Quality Methodology in Lync Server 2013</span></span>](lync-server-2013-poster-lync-call-quality-methodology.md)

  - [<span data-ttu-id="97f06-117">Wichtige Integritätsindikatoren in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="97f06-117">Key Health Indicators in Lync Server 2013</span></span>](lync-server-2013-poster-key-health-indicators.md)

<span data-ttu-id="97f06-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="97f06-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

