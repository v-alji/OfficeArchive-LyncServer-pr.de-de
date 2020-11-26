---
title: 'Lync Server 2013: Hybrid-und Split-Domain-AutoErmittlung'
description: 'Lync Server 2013: Hybrid-und Split-Domain-AutoErmittlung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hybrid and split-domain - Autodiscover
ms:assetid: c855bcc5-b656-4d2d-92d6-f016f2797d3a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945652(v=OCS.15)
ms:contentKeyID: 51541520
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 972233fd10d2b68a002d2d3a203f61bb0bd29574
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427439"
---
# <a name="hybrid-and-split-domain---autodiscover-in-lync-server-2013"></a><span data-ttu-id="89802-103">Hybrid-und Split-Domain-AutoErmittlung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="89802-103">Hybrid and split-domain - Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="89802-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="89802-104">

<span> </span></span></span>

<span data-ttu-id="89802-105">_**Letztes Änderungsdatum des Themas:** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="89802-105">_**Topic Last Modified:** 2013-02-14_</span></span>

<span data-ttu-id="89802-106">Ein freigegebener SIP-Adressraum, auch bekannt als " *Split-Domain-* Bereitstellung" oder eine *Hybrid* Bereitstellung, ist eine Konfiguration, in der Benutzer über eine lokale Bereitstellung und eine Online Umgebung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="89802-106">A shared SIP address space, also known as a *split-domain* deployment, or a *hybrid* deployment, is a configuration where users are deployed across an on-premise deployment and an online environment.</span></span> <span data-ttu-id="89802-107">Das gewünschte Ergebnis besteht darin, dass Sie einen Benutzer haben, unabhängig davon, wo sich der Stammserver befindet (lokal oder Online), sich bei der Bereitstellung anmelden und an den Standort Ihres Home-Servers weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="89802-107">The desired outcome is to have a user, regardless of where their home server is located (on-premise or online), log into the deployment and be redirected to their home server location.</span></span> <span data-ttu-id="89802-108">Um dies zu erreichen, wird das Auto Ermittlungs Feature von lync Server 2013 verwendet, um den Online Benutzer zur Online Topologie umzuleiten.</span><span class="sxs-lookup"><span data-stu-id="89802-108">To accomplish this, the Autodiscover feature of Lync Server 2013 is used to redirect the online user to the online topology.</span></span> <span data-ttu-id="89802-109">Dazu können Sie den Uniform Resource Locator (URL) für die AutoErmittlung mithilfe der lync Server-Verwaltungsshell, dem Cmdlet " **Get-CsHostingProvider** " und dem Cmdlet " **Satz-CsHostingProvider** " konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="89802-109">You can do this by configuring the Autodiscover uniform resource locator (URL) by using the Lync Server Management Shell, the **Get-CsHostingProvider** cmdlet, and the **Set-CsHostingProvider** cmdlet.</span></span>

<div>

## <a name="mobility-for-the-split-domain-deployment"></a><span data-ttu-id="89802-110">Mobilität für die Bereitstellung von geteilten Domänen</span><span class="sxs-lookup"><span data-stu-id="89802-110">Mobility for the Split Domain Deployment</span></span>

<span data-ttu-id="89802-111">Sie müssen die folgenden bereitgestellten Attribute sammeln und aufzeichnen:</span><span class="sxs-lookup"><span data-stu-id="89802-111">You will need to collect and record the following deployed attributes:</span></span>

  - <span data-ttu-id="89802-112">Geben Sie in der lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="89802-112">From the Lync Server Management Shell, type</span></span>
    
        Get-CsHostingProvider

  - <span data-ttu-id="89802-113">Suchen Sie in den Ergebnissen den Onlineanbieter mit dem Attribut **ProxyFQDN**.</span><span class="sxs-lookup"><span data-stu-id="89802-113">In the results, find the online provider with the attribute **ProxyFQDN**.</span></span> <span data-ttu-id="89802-114">Beispiel: sipfed.online.lync.com.</span><span class="sxs-lookup"><span data-stu-id="89802-114">For example, sipfed.online.lync.com.</span></span>

  - <span data-ttu-id="89802-115">Notieren Sie sich den Wert des ProxyFQDN.</span><span class="sxs-lookup"><span data-stu-id="89802-115">Record the value of the ProxyFQDN.</span></span>

  - <span data-ttu-id="89802-116">Aktivieren Sie die Föderation in der lokalen lync Server-Systemsteuerung, wodurch die Föderation mit dem Onlineanbieter zugelassen wird.</span><span class="sxs-lookup"><span data-stu-id="89802-116">Enable federation in the on-premise Lync Server Control Panel, allowing federation with the online provider.</span></span>

  - <span data-ttu-id="89802-117">Aktivieren Sie den Verbund für den Onlineanbieter.</span><span class="sxs-lookup"><span data-stu-id="89802-117">Enable federation for the online provider.</span></span> <span data-ttu-id="89802-118">Standardmäßig sind alle Online Benutzer für den Domänen Verbund aktiviert und können mit allen Domänen kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="89802-118">By default, all online users are enabled for domain federation and can communicate with all domains.</span></span>

  - <span data-ttu-id="89802-119">Wenn Sie blockierte und zulässige Domänen definieren, ermitteln Sie die Domänen, die explizit zugelassen oder explizit blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="89802-119">If you will define blocked and allowed domains, determine the domains that you will explicitly allow or explicitly block.</span></span>

  - <span data-ttu-id="89802-120">Für die Online-Föderation müssen Sie Firewall-Ausnahmen, Zertifikate und DNS-Host (A oder AAAA, wenn Sie IPv6 verwenden) planen.</span><span class="sxs-lookup"><span data-stu-id="89802-120">For online federation, you must plan for firewall exceptions, certificates, and DNS host (A or AAAA, if using IPv6) records.</span></span> <span data-ttu-id="89802-121">Darüber hinaus müssen Sie Verbund Richtlinien konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="89802-121">Additionally, you must configure federation policies.</span></span> <span data-ttu-id="89802-122">Ausführliche Informationen finden Sie unter [Planen von lync Server 2013 und Office Communications Server Federation](lync-server-2013-planning-for-lync-server-and-office-communications-server-federation.md).</span><span class="sxs-lookup"><span data-stu-id="89802-122">For details, see [Planning for Lync Server 2013 and Office Communications Server federation](lync-server-2013-planning-for-lync-server-and-office-communications-server-federation.md).</span></span>

<span data-ttu-id="89802-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="89802-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

