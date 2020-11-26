---
title: 'Lync Server 2013: Konfigurieren von Firewalls und Ports für den externen Benutzerzugriff'
description: 'Lync Server 2013: Konfigurieren von Firewalls und Ports für den Zugriff durch externe Benutzer.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure firewalls and ports for external user access
ms:assetid: cacb3832-f8db-4009-bfcf-6f5c15c236ed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398848(v=OCS.15)
ms:contentKeyID: 48185430
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 68ccb382c3b3632b113b2b0a36846500700c1b9f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433969"
---
# <a name="configure-firewalls-and-ports-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="68984-103">Konfigurieren von Firewalls und Ports für den externen Benutzerzugriff in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68984-103">Configure firewalls and ports for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="68984-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="68984-104">

<span> </span></span></span>

<span data-ttu-id="68984-105">_**Letztes Änderungsdatum des Themas:** 2012-05-21_</span><span class="sxs-lookup"><span data-stu-id="68984-105">_**Topic Last Modified:** 2012-05-21_</span></span>

<span data-ttu-id="68984-106">Um Firewalls und Ports zu konfigurieren, müssen Sie Sie für Edgeserver, Reverse-Proxy Server und möglicherweise Hardwarelastenausgleichs (für eine skalierte Bereitstellung, die keinen DNS-Lastenausgleich verwendet) konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="68984-106">To configure firewalls and ports, you need to configure them for Edge Servers, reverse proxy servers, and possibly hardware load balancers (for a scaled deployment that does not use DNS load balancing).</span></span> <span data-ttu-id="68984-107">Dieser Abschnitt enthält Informationen über Firewall-und Portanforderungen für alle Edgeserver-Komponenten und die Konfiguration von Firewall-Ports für Edgeserver.</span><span class="sxs-lookup"><span data-stu-id="68984-107">This section provides information about firewall and port requirements for all Edge Server components and the configuration of firewall ports for Edge Servers.</span></span> <span data-ttu-id="68984-108">Weitere Informationen zum Konfigurieren von Ports für Reverse-Proxy Server finden Sie unter [Einrichten von Reverse-Proxyservern für lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md).</span><span class="sxs-lookup"><span data-stu-id="68984-108">For details about configuring ports for reverse proxy servers, see [Setting up reverse proxy servers for Lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md).</span></span> <span data-ttu-id="68984-109">Wenn Sie eine skalierte Edge-Topologie bereitstellen und anstelle des DNS-Lastenausgleichs den Hardwarelastenausgleich verwenden, finden Sie weitere Informationen zum Konfigurieren von Ports für Hardwarelastenausgleichs in der Planning-Dokumentation unter [skalierter konsolidierter Edge mit Hardwarelastenausgleichs in lync Server 2013](lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md) .</span><span class="sxs-lookup"><span data-stu-id="68984-109">If you are deploying a scaled edge topology and are using hardware load balancing instead of DNS load balancing, see [Scaled consolidated edge with hardware load balancers in Lync Server 2013](lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md) in the Planning documentation for details about configuring ports for hardware load balancers.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="68984-110">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="68984-110">See Also</span></span>


[<span data-ttu-id="68984-111">Ermitteln der Anforderungen für externe A/V-Firewalls und Ports für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68984-111">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  
  

<span data-ttu-id="68984-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="68984-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

