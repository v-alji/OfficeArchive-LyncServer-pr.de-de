---
title: 'Lync Server 2013: Für den Director erforderliche Komponenten'
description: 'Lync Server 2013: für den Director erforderliche Komponenten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components required for the Director
ms:assetid: 15c7c8d4-b93f-4386-b2d1-d76dab8f801e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398228(v=OCS.15)
ms:contentKeyID: 48183502
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 57f717b9ddb9557f212321cdab075713a4b85c2d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394019"
---
# <a name="components-required-for-the-director-in-lync-server-2013"></a><span data-ttu-id="31d4d-103">Für den Director erforderliche Komponenten in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31d4d-103">Components required for the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="31d4d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="31d4d-104">

<span> </span></span></span>

<span data-ttu-id="31d4d-105">_**Letztes Änderungsdatum des Themas:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="31d4d-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="31d4d-106">Die einzige Komponente, die zum Erstellen und Konfigurieren eines Directors erforderlich ist, besteht darin, die Director-Serverrolle bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="31d4d-106">The only component required to create and configure a Director is to deploy the Director server role.</span></span> <span data-ttu-id="31d4d-107">Dazu verwenden Sie den Topologie-Generator und definieren entweder einen einzelnen Computerpool oder einen Pool mit mehreren Computern im Director-Pool-Knoten.</span><span class="sxs-lookup"><span data-stu-id="31d4d-107">You do this by using Topology Builder and define either a single computer pool or a multiple computer pool in the Director pool node.</span></span> <span data-ttu-id="31d4d-108">Nachdem Sie den Director-oder Director-Pool definiert haben, führen Sie den lync Server-Bereitstellungs-Assistenten auf dem Computer aus, der als Director ausgeführt werden soll.</span><span class="sxs-lookup"><span data-stu-id="31d4d-108">After you have defined the Director or Director pool, run the Lync Server Deployment Wizard on the computer that will be a Director.</span></span> <span data-ttu-id="31d4d-109">Im Fall eines Director-Pools führen Sie den lync Server-Bereitstellungs-Assistenten auf jedem Server aus, der Mitglied des Pools sein soll.</span><span class="sxs-lookup"><span data-stu-id="31d4d-109">In the case of a Director pool, you run the Lync Server Deployment Wizard on each server that will be a member of the pool.</span></span>

<div>

## <a name="topologies"></a><span data-ttu-id="31d4d-110">Topologien verfügen</span><span class="sxs-lookup"><span data-stu-id="31d4d-110">Topologies</span></span>

<span data-ttu-id="31d4d-111">Sie können einen einzelnen Director-Server oder einen Director-Pool implementieren.</span><span class="sxs-lookup"><span data-stu-id="31d4d-111">You can implement a single Director server or a Director pool.</span></span> <span data-ttu-id="31d4d-112">Der Director ist immer ein separater Server oder Pool, nicht mit einer anderen Serverrolle in lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="31d4d-112">The Director is always a separate server or pool, not collocated with any other server role in Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="31d4d-113">Wenn Sie Directors nicht bereitstellen, übernimmt der Front-End-Server oder der Front-End-Pool die Director-Rolle.</span><span class="sxs-lookup"><span data-stu-id="31d4d-113">If you do not deploy Directors, the Front End Server or Front End pool will assume the Director role.</span></span>



</div>

<span data-ttu-id="31d4d-114">Ein Pool von Directors muss Load Balanced sein.</span><span class="sxs-lookup"><span data-stu-id="31d4d-114">A pool of Directors must be load balanced.</span></span> <span data-ttu-id="31d4d-115">Sie können eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="31d4d-115">You can do one of the following:</span></span>

  - <span data-ttu-id="31d4d-116">Erstellen Sie eine Topologie, die ein Hardwarelastenausgleich für Webdienste und DNS (Domain Name System)-Lastenausgleich für die anderen Datenverkehrstypen verwendet.</span><span class="sxs-lookup"><span data-stu-id="31d4d-116">Create a topology that uses a hardware load balancer for web services and Domain Name System (DNS) load balancing for the other traffic types.</span></span>
    
    [<span data-ttu-id="31d4d-117">Skalierter Directorpool – DNS-Lastenausgleich und Hardwarelastenausgleich in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31d4d-117">Scaled Director pool - DNS load balancing and hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-scaled-director-pool-dns-load-balancing-and-hardware-load-balancer.md)

  - <span data-ttu-id="31d4d-118">Erstellen Sie eine Topologie, die ein Hardware-Lastenausgleichsmodul für den für den Director-Pool erforderlichen Lastenausgleich verwendet.</span><span class="sxs-lookup"><span data-stu-id="31d4d-118">Create a topology that uses a hardware load balancer for load balancing needed for the Director pool.</span></span>
    
    [<span data-ttu-id="31d4d-119">Skalierter Directorpool (Hardwarelastenausgleich) in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="31d4d-119">Scaled Director pool - hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-scaled-director-pool-hardware-load-balancer.md)

<span data-ttu-id="31d4d-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="31d4d-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

