---
title: Vorbereiten der Installation von Servern im Umkreisnetzwerk
description: Vorbereiten der Installation von Servern im Umkreisnetzwerk
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing for installation of servers in the perimeter network
ms:assetid: 5e6c457a-f964-4ef7-a709-97abda9c673a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398416(v=OCS.15)
ms:contentKeyID: 48184292
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5689d7990cc1ddf91ad6487d8abed08f40cd3db5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424135"
---
# <a name="preparing-for-installation-of-servers-in-the-perimeter-network-for-lync-server-2013"></a><span data-ttu-id="7450e-103">Vorbereiten der Installation von Servern im Umkreisnetzwerk für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7450e-103">Preparing for installation of servers in the perimeter network for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7450e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7450e-104">

<span> </span></span></span>

<span data-ttu-id="7450e-105">_**Letztes Änderungsdatum des Themas:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="7450e-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="7450e-106">Bevor Sie Edgeserver-Komponenten einrichten, müssen Sie sicherstellen, dass die Computer, die Sie einrichten, die Systemanforderungen erfüllen und andere erforderliche Schritte für die Bereitstellung von Edgeserver-Komponenten ausführen.</span><span class="sxs-lookup"><span data-stu-id="7450e-106">Before you set up Edge Server components, you need to ensure that computers that you are setting up meet system requirements and complete other prerequisite steps required for deployment of Edge Server components.</span></span>

<span data-ttu-id="7450e-107">Bevor Sie beginnen, überprüfen Sie die Details in den folgenden Themen in der Planungsdokumentation für die Referenzarchitektur, die Sie bereitstellen möchten:</span><span class="sxs-lookup"><span data-stu-id="7450e-107">Before you begin, review the details in the following topics in the Planning documentation for the reference architecture that you want to deploy:</span></span>

  - [<span data-ttu-id="7450e-108">Einzelner konsolidierter Edgeserver mit privaten IP-Adressen und NAT in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7450e-108">Single consolidated edge with private IP addresses and NAT in Lync Server 2013</span></span>](lync-server-2013-single-consolidated-edge-with-private-ip-addresses-and-nat.md)

  - [<span data-ttu-id="7450e-109">Einzelner konsolidierter Edgeserver mit öffentlichen IP-Adressen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7450e-109">Single consolidated edge with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-single-consolidated-edge-with-public-ip-addresses.md)

  - [<span data-ttu-id="7450e-110">Skalierter konsolidierter Edgeserver, DNS-Lastenausgleich mit privaten IP-Adressen und NAT in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7450e-110">Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md)

  - [<span data-ttu-id="7450e-111">Skalierter konsolidierter Edgeserver, DNS-Lastenausgleich mit öffentlichen IP-Adressen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7450e-111">Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md)

  - [<span data-ttu-id="7450e-112">Skalierter konsolidierter Edgeserver mit Hardwarelastenausgleich in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7450e-112">Scaled consolidated edge with hardware load balancers in Lync Server 2013</span></span>](lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md)

<div>

## <a name="in-this-section"></a><span data-ttu-id="7450e-113">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="7450e-113">In This Section</span></span>

  - [<span data-ttu-id="7450e-114">Konfigurieren von DNS für die Edgeunterstützung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7450e-114">Configure DNS for edge support in Lync Server 2013</span></span>](lync-server-2013-configure-dns-for-edge-support.md)

  - [<span data-ttu-id="7450e-115">Einrichten von Hardwaregeräten zum Lastenausgleich für skalierte Edgetopologien in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7450e-115">Set up hardware load balancers for scaled edge topologies in Lync Server 2013</span></span>](lync-server-2013-set-up-hardware-load-balancers-for-scaled-edge-topologies.md)

  - [<span data-ttu-id="7450e-116">Konfigurieren von Firewalls und Ports für den externen Benutzerzugriff in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7450e-116">Configure firewalls and ports for external user access in Lync Server 2013</span></span>](lync-server-2013-configure-firewalls-and-ports-for-external-user-access.md)

  - [<span data-ttu-id="7450e-117">Ermitteln der Anforderungen für externe A/V-Firewalls und Ports für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7450e-117">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)

  - [<span data-ttu-id="7450e-118">Anfordern von Zertifikaten für Edgekomponenten in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7450e-118">Request certificates for edge components in Lync Server 2013</span></span>](lync-server-2013-request-certificates-for-edge-components.md)

<span data-ttu-id="7450e-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7450e-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

