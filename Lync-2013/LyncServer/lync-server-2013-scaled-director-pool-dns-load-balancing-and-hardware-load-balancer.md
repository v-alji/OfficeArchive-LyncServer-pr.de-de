---
title: Skalierter Directorpool – DNS-Lastenausgleich und Hardwarelastenausgleich
description: Skalierter Director-Pool – DNS-Lastenausgleich und Hardwarelastenausgleich.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scaled Director pool - DNS load balancing and hardware load balancer
ms:assetid: a1f6ffc0-9e6e-4217-a923-025c9679e154
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205142(v=OCS.15)
ms:contentKeyID: 48185023
ms.date: 03/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b30dfcc3515420ffb34343e4653e9518b1b9c3ed
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442064"
---
# <a name="scaled-director-pool---dns-load-balancing-and-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="abc0e-103">Skalierter Directorpool – DNS-Lastenausgleich und Hardwarelastenausgleich in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abc0e-103">Scaled Director pool - DNS load balancing and hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="abc0e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="abc0e-104">

<span> </span></span></span>

<span data-ttu-id="abc0e-105">_**Letztes Änderungsdatum des Themas:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="abc0e-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="abc0e-106">Ein skalierten Director-Pool, in dem mehr als ein Director zur Behandlung zusätzlicher Kapazität bereitgestellt wird und eine hohe Verfügbarkeit bereitgestellt wird, erfordert Lastenausgleich, um die Client-und Server Kommunikation an alle Mitglieder des Pools zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="abc0e-106">A scaled Director pool, where there are more than one Director deployed to handle additional capacity and to provide high availability, requires load balancing to distribute client and server communication to all members of the pool.</span></span> <span data-ttu-id="abc0e-107">Ein Director hostet Webdienste ähnlich wie ein Front-End-Pool.</span><span class="sxs-lookup"><span data-stu-id="abc0e-107">A Director hosts web services much like a Front End pool.</span></span> <span data-ttu-id="abc0e-108">Um den Lastenausgleich bereitzustellen, können Sie entweder den Hardwarelastenausgleich oder den Lastenausgleich für DNS (Domain Name System) oder den Hardwarelastenausgleich verwenden.</span><span class="sxs-lookup"><span data-stu-id="abc0e-108">To provide the load balancing, you can use either hardware load balancing or domain name system (DNS) load balancing and hardware load balancing.</span></span> <span data-ttu-id="abc0e-109">Für die Webdienste ist ein Hardware Lastenausgleich erforderlich, und allein der DNS-Lastenausgleich bietet nicht die für die Webdienste erforderlichen Funktionen.</span><span class="sxs-lookup"><span data-stu-id="abc0e-109">Hardware load balancing is required for the web services, and DNS load balancing alone does not provide the capabilities required for the web services.</span></span>

<span data-ttu-id="abc0e-110">In den folgenden Themen werden die Planungsüberlegungen zum Bereitstellen eines Director-Pools mithilfe des DNS-Lastenausgleichs in Verbindung mit dem Hardwarelastenausgleich beschrieben.</span><span class="sxs-lookup"><span data-stu-id="abc0e-110">The following topics describe the planning considerations for deploying a Director pool using DNS load balancing in conjunction with hardware load balancing.</span></span> <span data-ttu-id="abc0e-111">Wenn Sie beabsichtigen, den Hardwarelastenausgleich, aber nicht den DNS-Lastenausgleich für den Director-Pool zu verwenden, lesen Sie das Thema [skalierten Director-Pool – Hardwarelastenausgleich in lync Server 2013, in](lync-server-2013-scaled-director-pool-hardware-load-balancer.md) dem die Planungsanforderungen für diese Topologie beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="abc0e-111">If you intend to use hardware load balancing, but not DNS load balancing for the Director pool, see the topic [Scaled Director pool - hardware load balancer in Lync Server 2013](lync-server-2013-scaled-director-pool-hardware-load-balancer.md) that describes the planning requirements for that topology.</span></span>

<span data-ttu-id="abc0e-112">![Skalierter Director-Pool](images/JJ205142.35a78a7a-b781-4c8f-951e-168451ba6a65(OCS.15).jpg "Skalierter Director-Pool")</span><span class="sxs-lookup"><span data-stu-id="abc0e-112">![Scaled Director Pool](images/JJ205142.35a78a7a-b781-4c8f-951e-168451ba6a65(OCS.15).jpg "Scaled Director Pool")</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="abc0e-113">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="abc0e-113">In This Section</span></span>

  - [<span data-ttu-id="abc0e-114">Zertifikatzusammenfassung für DNS- und Hardwarelastenausgleich in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abc0e-114">Certificate summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-dns-and-hlb-load-balanced.md)

  - [<span data-ttu-id="abc0e-115">Portzusammenfassung für DNS- und Hardwarelastenausgleich in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abc0e-115">Port summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-port-summary-dns-and-hlb-load-balanced.md)

  - [<span data-ttu-id="abc0e-116">DNS-Zusammenfassung für DNS- und Hardwarelastenausgleich in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="abc0e-116">DNS summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-dns-summary-dns-and-hlb-load-balanced.md)

<span data-ttu-id="abc0e-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="abc0e-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

