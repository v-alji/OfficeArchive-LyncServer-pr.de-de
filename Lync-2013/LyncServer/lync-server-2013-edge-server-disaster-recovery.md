---
title: 'Lync Server 2013: Notfallwiederherstellung für Edgeserver'
description: 'Lync Server 2013: Edge Server Disaster Recovery.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Edge Server disaster recovery
ms:assetid: 05ec8d26-d167-4a6f-a966-a1f8873cf974
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687960(v=OCS.15)
ms:contentKeyID: 49733545
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: db084cae9b692ebc9d70660984275aa34096b7d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437679"
---
# <a name="edge-server-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="b15f6-103">Notfallwiederherstellung für Edgeserver in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b15f6-103">Edge Server disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b15f6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b15f6-104">

<span> </span></span></span>

<span data-ttu-id="b15f6-105">_**Letztes Änderungsdatum des Themas:** 2014-03-12_</span><span class="sxs-lookup"><span data-stu-id="b15f6-105">_**Topic Last Modified:** 2014-03-12_</span></span>

<span data-ttu-id="b15f6-106">Wie bei anderen Serverrollen besteht die beste Möglichkeit für Sie, eine höhere Verfügbarkeit für Ihre Edgeserver bereitzustellen, darin, mehrere Edgeserver in Pools auf jeder Website bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b15f6-106">As with other server roles, the best way for you to provide high availability for your Edge Servers is to deploy multiple Edge servers in pools in each site.</span></span> <span data-ttu-id="b15f6-107">Wenn ein Edge-Server ausfällt, werden die anderen Server im Pool weiterhin Edge-Dienste bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="b15f6-107">If one Edge Server goes down, the other servers in the pool will continue to provide Edge services.</span></span>

<span data-ttu-id="b15f6-108">Zum Aktivieren von Disaster Recovery-Verfahren müssen separate Edge-Server-Pools an verschiedenen Standorten bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="b15f6-108">To enable disaster recovery procedures, you must have separate Edge Server pools deployed at separate sites.</span></span> <span data-ttu-id="b15f6-109">Sie müssen die Edge-Pools nicht explizit mit den Front-End-Pools koppeln, aber mit mehreren Edge-Pools können Sie weiterhin die Verfügbarkeit durchführen, wenn ein ganzer Edge-Pool ausfällt.</span><span class="sxs-lookup"><span data-stu-id="b15f6-109">You do not need to explicitly pair Edge pools together as you do with Front End pools, but having multiple Edge pools still provides the availability to carry on if one entire Edge pool goes down.</span></span> <span data-ttu-id="b15f6-110">Die folgenden Abschnitte enthalten Details zur Disaster Recovery für die verschiedenen Funktionen von Edge-Servern.</span><span class="sxs-lookup"><span data-stu-id="b15f6-110">The following sections provide details on disaster recovery for the various functions of Edge Servers.</span></span>

<div>

## <a name="remote-access"></a><span data-ttu-id="b15f6-111">Remote Zugriff</span><span class="sxs-lookup"><span data-stu-id="b15f6-111">Remote Access</span></span>

<span data-ttu-id="b15f6-112">Wenn Sie über mehrere Websites verfügen, die jeweils einen Pool von Edge-Servern aufweisen und ein ganzer Edge-Pool ausfällt, funktionieren die RAS-Dienste weiterhin, ohne dass eine Administratoraktion erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b15f6-112">If you have multiple sites, each with a pool of Edge servers, and one entire Edge pool fails, the remote access services will continue to function without needing administrator action.</span></span> <span data-ttu-id="b15f6-113">Wenn Sie Edge-Pools in verschiedenen Websites erstellen, können Sie nicht den gleichen FQDN verwenden.</span><span class="sxs-lookup"><span data-stu-id="b15f6-113">When creating Edge pools in different sites, you cannot use the same FQDN.</span></span> <span data-ttu-id="b15f6-114">Jeder Edge-Pool muss eindeutige FQDNs (intern und extern) aufweisen.</span><span class="sxs-lookup"><span data-stu-id="b15f6-114">Each Edge pool must have unique FQDNs (internal and external).</span></span> <span data-ttu-id="b15f6-115">Die Edge-Pools verwenden keine Reverse Proxy-Veröffentlichungsregeln, um mit den Front-End-Servern zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="b15f6-115">The Edge pools do not use reverse proxy publishing rules to talk to the Front End servers.</span></span> <span data-ttu-id="b15f6-116">Automatisches Failover tritt auf, wenn der Client die RAS-DNS-Diensteinträge erneut abfragt und Remotebenutzer an die Edgeserver an einem anderen Standort weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="b15f6-116">Automatic failover occurs when the client re-queries the remote access DNS service records, and remote users are routed to the Edge servers in another site.</span></span> <span data-ttu-id="b15f6-117">Der Client versucht jeden externen Edge-FQDN entsprechend der Priorität der DNS-SRV-Einträge.</span><span class="sxs-lookup"><span data-stu-id="b15f6-117">The client attempts each external Edge FQDN according to the priority of the DNS SRV records.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b15f6-118">Damit ein Failover reibungslos funktioniert, müssen Sie sicherstellen, dass die Firewall den Front-End-Servern aus jedem Pool die Kommunikation mit allen Edge-Servern ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="b15f6-118">For failover to work smoothly, ensure that the firewall allows the Front End servers from every pool to communicate with all Edge servers.</span></span>



</div>

</div>

<div>

## <a name="federation"></a><span data-ttu-id="b15f6-119">Partnerverbund</span><span class="sxs-lookup"><span data-stu-id="b15f6-119">Federation</span></span>

<span data-ttu-id="b15f6-120">Für Verbundbeziehungen mit anderen Organisationen, die lync Server ausführen, funktionieren eingehende Verbund Anforderungen weiterhin so lange, wie Sie Lösungen wie Geo-DNS-Unternehmen haben.</span><span class="sxs-lookup"><span data-stu-id="b15f6-120">For federation relationships with other organizations running Lync Server, inbound federation requests will continue to work as long as you have solutions like Geo-DNS GTM.</span></span> <span data-ttu-id="b15f6-121">Es ist wichtig zu wissen, dass Verbund Failover kein Failover mit Priorität in SRV-Einträgen bietet.</span><span class="sxs-lookup"><span data-stu-id="b15f6-121">It’s important to understand that federation failover does not provide failover with priority in SRV records.</span></span> <span data-ttu-id="b15f6-122">Eine zuvor bereitgestellte Lösung kann Ihnen bei der Bereitstellung von Disaster Recovery-Funktionen für eingehende Föderation helfen.</span><span class="sxs-lookup"><span data-stu-id="b15f6-122">A solution provided earlier can help you provide disaster recovery capabilities for inbound federation.</span></span>

<span data-ttu-id="b15f6-123">Ausgehende Föderationen werden immer über einen veröffentlichten Edge-Pool oder Edgeserver in der Organisation eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="b15f6-123">Outbound federation is always set up through one published Edge pool or Edge Server in the organization.</span></span> <span data-ttu-id="b15f6-124">Wenn dieser Edge-Pool nicht mehr vorhanden ist, müssen Sie den Topologie-Generator verwenden, um die ausgehende Föderations Route so zu ändern, dass ein noch ausgeführter Edge-Pool verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b15f6-124">If this Edge pool has gone down, you must use Topology Builder to change the outbound federation route to use an Edge pool which is still running.</span></span> <span data-ttu-id="b15f6-125">Ausführliche Informationen finden Sie unter [Failover des Edge-Pools, der für den lync Server-Verbund in lync Server 2013 verwendet wird](lync-server-2013-failing-over-the-edge-pool-used-for-lync-server-federation.md) .</span><span class="sxs-lookup"><span data-stu-id="b15f6-125">For details, see [Failing over the Edge pool used for Lync Server federation in Lync Server 2013](lync-server-2013-failing-over-the-edge-pool-used-for-lync-server-federation.md)</span></span>

</div>

<div>

## <a name="xmpp-federation"></a><span data-ttu-id="b15f6-126">XMPP-Föderation</span><span class="sxs-lookup"><span data-stu-id="b15f6-126">XMPP Federation</span></span>

<span data-ttu-id="b15f6-127">Bei der XMPP-Föderation schlägt der ausgehende und eingehende Datenverkehr fehl, wenn der als XMPP Federation Gateway bezeichnete Edge-Pool herunterfällt.</span><span class="sxs-lookup"><span data-stu-id="b15f6-127">For XMPP federation, both outbound and inbound traffic will fail if the Edge pool which is designated as the XMPP federation gateway goes down.</span></span> <span data-ttu-id="b15f6-128">Damit die XMPP-Föderation wieder funktioniert, müssen Sie die XMPP-Föderation ändern, um einen anderen Edge-Pool zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="b15f6-128">To make XMPP federation work again, you must change XMPP federation to use a different Edge pool.</span></span> <span data-ttu-id="b15f6-129">Ausführliche Informationen finden Sie unter [Failover des für die XMPP-Föderation in lync Server 2013 verwendeten Edge-Pools](lync-server-2013-failing-over-the-edge-pool-used-for-xmpp-federation.md).</span><span class="sxs-lookup"><span data-stu-id="b15f6-129">For details, see [Failing over the Edge pool used for XMPP federation in Lync Server 2013](lync-server-2013-failing-over-the-edge-pool-used-for-xmpp-federation.md).</span></span>

</div>

<div>

## <a name="edge-pool-fails-but-front-end-pool-is-still-running"></a><span data-ttu-id="b15f6-130">Der Edge-Pool schlägt fehl, aber der Front-End-Pool wird weiterhin ausgeführt</span><span class="sxs-lookup"><span data-stu-id="b15f6-130">Edge Pool Fails But Front End Pool Is Still Running</span></span>

<span data-ttu-id="b15f6-131">Wenn ein Edge-Pool an einer Website fehlschlägt, der Front-End-Pool dieser Website jedoch weiterhin ausgeführt wird, müssen Sie den Front-End-Pool so ändern, dass ein anderer Edge-Pool an einer anderen Website verwendet wird, während der erste Edge-Pool nicht mehr zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="b15f6-131">If an Edge pool fails at a site, but the Front End pool at that site is still running, you will need to change the Front End pool to use a different Edge pool at a different site while that first Edge pool is down.</span></span> <span data-ttu-id="b15f6-132">Weitere Informationen finden Sie unter [Ändern des Edge-Pools, der einem Front-End-Pool in lync Server 2013 zugeordnet](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md)ist.</span><span class="sxs-lookup"><span data-stu-id="b15f6-132">For more information, see [Changing the Edge pool associated with a Front End pool in Lync Server 2013](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md).</span></span>

<span data-ttu-id="b15f6-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b15f6-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

