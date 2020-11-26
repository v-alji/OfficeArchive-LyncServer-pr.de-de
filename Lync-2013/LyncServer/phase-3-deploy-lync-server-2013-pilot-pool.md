---
title: 'Phase 3: Bereitstellen des lync Server 2013-pilotpools'
description: 'Phase 3: Bereitstellen des lync Server 2013-pilotpools.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Phase 3: Deploy Lync Server 2013 pilot pool'
ms:assetid: f12b1517-fb56-4ded-8323-57aa9fc9ea48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205367(v=OCS.15)
ms:contentKeyID: 48185778
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f72f0cdd2e7d3b9e29891a4adc0ab0551539f465
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438456"
---
# <a name="phase-3-deploy-lync-server-2013-pilot-pool"></a><span data-ttu-id="ffe7f-103">Phase 3: Bereitstellen des lync Server 2013-pilotpools</span><span class="sxs-lookup"><span data-stu-id="ffe7f-103">Phase 3: Deploy Lync Server 2013 pilot pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ffe7f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ffe7f-104">

<span> </span></span></span>

<span data-ttu-id="ffe7f-105">_**Letztes Änderungsdatum des Themas:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="ffe7f-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="ffe7f-106">In diesem Abschnitt werden die erforderlichen Schritte zum Bereitstellen eines pilotpools von lync Server 2013 beschrieben.</span><span class="sxs-lookup"><span data-stu-id="ffe7f-106">This section covers the steps required to deploy a pilot pool of Lync Server 2013.</span></span> <span data-ttu-id="ffe7f-107">Die Bereitstellung von lync Server 2013 erfordert die Verwendung des Topologie-Generators zum Definieren Ihrer Topologie und der Komponenten, die Sie bereitstellen möchten, Vorbereiten der Umgebung für die Bereitstellung der lync Server 2013-Komponenten, Veröffentlichen des Topologie-Designs auf dem ersten Front-End-Server und anschließendes Installieren und Konfigurieren der lync Server 2013-Software für die Komponenten für Ihre Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="ffe7f-107">The deployment of Lync Server 2013 requires using Topology Builder to define your topology and the components you want to deploy, preparing your environment for deployment of the Lync Server 2013 components, publishing your topology design on the first Front End Server, and then installing and configuring Lync Server 2013 software for the components for your deployment.</span></span> <span data-ttu-id="ffe7f-108">Wenn Sie fertig sind, wird die Bereitstellung Ihres lync Server 2013-pilotpools mit einem vorhandenen lync Server 2010-Pool koexistieren.</span><span class="sxs-lookup"><span data-stu-id="ffe7f-108">When completed, your Lync Server 2013 pilot pool deployment will coexist with an existing Lync Server 2010 pool.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ffe7f-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ffe7f-109">In This Section</span></span>

  - [<span data-ttu-id="ffe7f-110">Vorbereiten von Active Directory für Lync Server</span><span class="sxs-lookup"><span data-stu-id="ffe7f-110">Prepare Active Directory for Lync Server</span></span>](prepare-active-directory-for-lync-server.md)

  - [<span data-ttu-id="ffe7f-111">Herunterladen der Topologie aus einer vorhandenen Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="ffe7f-111">Download topology from existing deployment</span></span>](download-topology-from-existing-deployment.md)

  - [<span data-ttu-id="ffe7f-112">Bereitstellen des lync Server 2013-pilotpools</span><span class="sxs-lookup"><span data-stu-id="ffe7f-112">Deploy Lync Server 2013 pilot pool</span></span>](deploy-lync-server-2013-pilot-pool.md)

  - [<span data-ttu-id="ffe7f-113">Überprüfen der Koexistenz der Pilotinstallation mit Pools der Vorversion</span><span class="sxs-lookup"><span data-stu-id="ffe7f-113">Verify pilot pool coexistence with legacy pool</span></span>](verify-pilot-pool-coexistence-with-legacy-pool.md)

  - [<span data-ttu-id="ffe7f-114">Verbinden des Pilotpools mit Edgeservern der Vorversion</span><span class="sxs-lookup"><span data-stu-id="ffe7f-114">Connect pilot pool to legacy Edge Servers</span></span>](connect-pilot-pool-to-legacy-edge-servers.md)

  - [<span data-ttu-id="ffe7f-115">Konfigurieren von Zugriffsrichtlinien und Zertifikaten für XMPP-Gateways</span><span class="sxs-lookup"><span data-stu-id="ffe7f-115">Configure XMPP gateway access policies and certificates</span></span>](configure-xmpp-gateway-access-policies-and-certificates.md)

<span data-ttu-id="ffe7f-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ffe7f-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

