---
title: 'Lync Server 2013: Branch Site SIP Trunking'
description: 'Lync Server 2013: Branch Site SIP Trunking.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Branch site SIP trunking
ms:assetid: c4d9dfcd-8baa-41ea-9677-48b0e429429d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412974(v=OCS.15)
ms:contentKeyID: 48185350
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 33e408a462c21ffa6df6e6a2aee50d7b87dca1f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435943"
---
# <a name="branch-site-sip-trunking-in-lync-server-2013"></a><span data-ttu-id="89999-103">Branch site SIP trunking in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89999-103">Branch site SIP trunking in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="89999-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="89999-104">

<span> </span></span></span>

<span data-ttu-id="89999-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="89999-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="89999-106">In einigen Fällen müssen Sie möglicherweise verteilte SIP-Trunking an ausgewählten Zweigstellen implementieren.</span><span class="sxs-lookup"><span data-stu-id="89999-106">In some cases, you may need to implement distributed SIP trunking at selected branch sites.</span></span> <span data-ttu-id="89999-107">Wenn Sie feststellen möchten, ob ein SIP-Trunk für eine Zweigstelle benötigt wird, lesen Sie die Informationen unter [wie kann ich SIP-Trunking in lync Server 2013 implementieren?](lync-server-2013-how-do-i-implement-sip-trunking.md).</span><span class="sxs-lookup"><span data-stu-id="89999-107">To determine whether a SIP trunk is needed for a branch site, review the information in [How do I implement SIP trunking in Lync Server 2013?](lync-server-2013-how-do-i-implement-sip-trunking.md).</span></span>

<span data-ttu-id="89999-108">Details zu den unterstützten Topologie-Optionen für die Bereitstellung von SIP-Stämmen in Zweigstellen finden Sie unter Lösungen für die [Standort Stabilität in lync Server 2013](lync-server-2013-branch-site-resiliency-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="89999-108">For details about the supported topology options for deploying SIP trunks in branch sites, see [Branch-site resiliency solutions in Lync Server 2013](lync-server-2013-branch-site-resiliency-solutions.md).</span></span>

<div>

## <a name="example-branch-site-sip-trunk-requirements-analysis"></a><span data-ttu-id="89999-109">Beispielanalyse für die SIP-Trunkanforderungen an einer Zweigniederlassung</span><span class="sxs-lookup"><span data-stu-id="89999-109">Example Branch Site SIP Trunk Requirements Analysis</span></span>

<span data-ttu-id="89999-110">Wenn Sie sich für die Bereitstellung einer Zweigstelle SIP Trunk entscheiden, müssen Sie eine Website spezifische Kostenanalyse durchführen.</span><span class="sxs-lookup"><span data-stu-id="89999-110">When you decide to deploy a branch site SIP trunk, you need to perform a site-specific cost analysis.</span></span> <span data-ttu-id="89999-111">Beispielsweise sollte ein Unternehmen mit einem zentralen Standort in Redmond, Washington und einer Zweigstelle in New York eine Analyse durchführen, um zu ermitteln, ob ein SIP-Trunk vom Standort New York zu einem lokalen Dienstanbieter implementiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="89999-111">For example, an enterprise that has a central site in Redmond, Washington, and a branch site in New York, should do an analysis to determine whether to implement a SIP trunk from the New York site to a local service provider.</span></span>

<span data-ttu-id="89999-112">Wenn Sie feststellen möchten, ob ein verteilter SIP-Trunk in New York kostengünstig ist, ermitteln Sie, welche Direktwahlnummern (DID) den SIP-Stamm verwenden, und analysieren Sie die Anzahl der Anrufe, die in New York an andere Bereiche als Redmond (425) vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="89999-112">To determine whether a distributed SIP trunk in New York is cost-effective, identify which Direct Inward Dialing (DID) numbers will use the SIP trunk, and analyze the number of calls New York makes to areas other than Redmond (425).</span></span> <span data-ttu-id="89999-113">Sie können für die Verzweigungs Website am zentralen Standort beendet haben.</span><span class="sxs-lookup"><span data-stu-id="89999-113">You can have DID termination for the branch site at the central site.</span></span> <span data-ttu-id="89999-114">So kann beispielsweise auf der zentralen Website von Redmond die Nummer für die Niederlassung in der New York Branch-Website gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="89999-114">For example, the Redmond central site can host DID numbers for the New York branch site.</span></span> <span data-ttu-id="89999-115">Wenn die Kosten für die Implementierung eines verteilten SIP-Trunks kleiner als die Kosten dieser Anrufe sind, sollten Sie einen SIP-Trunk an der New York Branch-Website implementieren.</span><span class="sxs-lookup"><span data-stu-id="89999-115">If the cost of implementing a distributed SIP trunk is less than the cost of those calls, consider implementing a SIP trunk at the New York branch site.</span></span>

</div>

<div>

## <a name="other-branch-site-sip-trunk-requirements"></a><span data-ttu-id="89999-116">Weitere SIP-Trunkanforderungen für Zweigniederlassungen</span><span class="sxs-lookup"><span data-stu-id="89999-116">Other Branch Site SIP Trunk Requirements</span></span>

<span data-ttu-id="89999-117">Die Entscheidung, ob anstelle eines Gateways ein SIP-Trunk bereitgestellt werden sollte, hängt von der Kostendifferenz bei Ferngesprächen der einzelnen Optionen ab.</span><span class="sxs-lookup"><span data-stu-id="89999-117">The choice between a deploying a SIP trunk instead of a gateway is based on the difference between the public switched telephone network (PSTN) long distance toll charges of each option.</span></span> <span data-ttu-id="89999-118">Wenn Sie eine Verzweigungs Website SIP-Trunk bereitstellen, müssen Sie auch ihre Stabilitäts-und Bandbreitenanforderungen ermitteln.</span><span class="sxs-lookup"><span data-stu-id="89999-118">If you deploy a branch site SIP trunk, you also need to determine your resiliency and bandwidth requirements.</span></span> <span data-ttu-id="89999-119">Wenn der Link zwischen Ihrer Zweigstelle und dem zentralen Standort widerstandsfähig ist und über genügend Bandbreite verfügt, können Sie einen SIP-Trunk oder ein Gateway bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="89999-119">If the link between your branch site and central site is resilient and has sufficient bandwidth, you can deploy a SIP trunk or a gateway.</span></span> <span data-ttu-id="89999-120">Sie müssen keine Survivable Branch-Appliance an der Zweigstelle bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="89999-120">You do not need to deploy a Survivable Branch Appliance at the branch site.</span></span> <span data-ttu-id="89999-121">Wenn der Link zwischen Ihrer Verzweigungs Website und dem zentralen Standort nicht belastbar ist, stellen Sie eine Survivable Branch-Appliance bereit, oder stellen Sie einen überlebensfähigen Verzweigungs Server mit einem Gateway oder SIP-Trunk an der Zweigstelle bereit.</span><span class="sxs-lookup"><span data-stu-id="89999-121">If the link between your branch site and central site is not resilient, deploy a Survivable Branch Appliance, or deploy a Survivable Branch Server with either a gateway or SIP trunk at the branch site.</span></span>

<span data-ttu-id="89999-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="89999-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

