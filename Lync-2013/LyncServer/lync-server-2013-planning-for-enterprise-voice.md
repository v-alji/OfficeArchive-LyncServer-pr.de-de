---
title: 'Lync Server 2013: Planung für Enterprise-VoIP'
description: 'Lync Server 2013: Planen von Enterprise-VoIP'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Enterprise Voice
ms:assetid: fd8d5867-0ac9-47f8-94f0-1c3ee5e25575
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413081(v=OCS.15)
ms:contentKeyID: 48185959
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4dfa0d91fe8270e49524d648ef403cd69ede2407
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424583"
---
# <a name="planning-for-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="74d07-103">Planen von Enterprise-VoIP in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74d07-103">Planning for Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="74d07-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="74d07-104">

<span> </span></span></span>

<span data-ttu-id="74d07-105">_**Letztes Änderungsdatum des Themas:** 2013-11-01_</span><span class="sxs-lookup"><span data-stu-id="74d07-105">_**Topic Last Modified:** 2013-11-01_</span></span>

<span data-ttu-id="74d07-106">Der Bereitstellungsprozess für Enterprise-VoIP hängt von Ihrer vorhandenen Topologie, Infrastruktur und der Enterprise-VoIP-Funktionalität ab, die Sie unterstützen möchten.</span><span class="sxs-lookup"><span data-stu-id="74d07-106">The deployment process for Enterprise Voice depends on your existing topology, infrastructure, and the Enterprise Voice functionality that you want to support.</span></span> <span data-ttu-id="74d07-107">Die erforderlichen Verfahren hängen von den von Ihnen ausgewählten Funktionen ab, aber Sie müssen weitere allgemeine Planungsentscheidungen treffen.</span><span class="sxs-lookup"><span data-stu-id="74d07-107">The required procedures will depend on what features you choose, but there are other planning considerations that you must make at a high level.</span></span>

<span data-ttu-id="74d07-108">In der Regel sollten Sie den Typ und die Anzahl der Websites, die Sie bereitstellen möchten, sowie deren geographische Standorte, das Anrufaufkommen an jedem Standort, die Typen von Netzwerkverbindungen, die Websites verbinden, angeben, ob Sie Redundanz und Failover für die Sprachfunktionalität für jede Website bereitstellen möchten und ob Sie vorhandene PBX-Anlagen verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="74d07-108">In general, consider the type and number of sites that you want to deploy and their geographical locations, the call volume at each site, the types of network links that connect sites, whether you want to provide redundancy and failover for voice functionality for each site, and whether you want to use existing PBX equipment.</span></span> <span data-ttu-id="74d07-109">Es gibt bestimmte Überlegungen, wie beispielsweise die Höchstverfügbarkeit, die Sie berücksichtigen sollten, wenn Sie die lync Server-Kommunikationssoftware als Ganzes planen.</span><span class="sxs-lookup"><span data-stu-id="74d07-109">There are certain considerations, such as high availability, that you should consider when you plan for Lync Server  communications software as a whole.</span></span> <span data-ttu-id="74d07-110">Diese Überlegungen werden nach Bedarf in den Themen in diesem Abschnitt erläutert.</span><span class="sxs-lookup"><span data-stu-id="74d07-110">These considerations are discussed in topics throughout this section, as needed.</span></span>

<div>

## <a name="planning-considerations"></a><span data-ttu-id="74d07-111">Planungsüberlegungen</span><span class="sxs-lookup"><span data-stu-id="74d07-111">Planning Considerations</span></span>

<span data-ttu-id="74d07-112">Informationen zu Planungsentscheidungen, die sich auf die Bereitstellung einer bestimmten Enterprise-VoIP-Funktion oder eines Bereitstellungsszenarios oder einer Komponente beziehen, finden Sie in den Themen in diesem Abschnitt.</span><span class="sxs-lookup"><span data-stu-id="74d07-112">For planning decisions that pertain to the deployment of a particular Enterprise Voice capability or deployment scenario or component, consult the topics in this section.</span></span>

  - [<span data-ttu-id="74d07-113">Definieren der Enterprise-VoIP-bezogenen Anforderungen für Ihr Unternehmen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74d07-113">Defining your requirements for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-enterprise-voice.md)

  - [<span data-ttu-id="74d07-114">Schätzen von VoIP-Nutzung und -Datenverkehr für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74d07-114">Estimating voice usage and traffic for Lync Server 2013</span></span>](lync-server-2013-estimating-voice-usage-and-traffic.md)

  - [<span data-ttu-id="74d07-115">Network settings for the advanced Enterprise Voice features in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74d07-115">Network settings for the advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md)

  - [<span data-ttu-id="74d07-116">Components required for Enterprise Voice in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74d07-116">Components required for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-components-required-for-enterprise-voice.md)

  - [<span data-ttu-id="74d07-117">Planen der Ausfallsicherheit für Enterprise-VoIP in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74d07-117">Planning for Enterprise Voice resiliency in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice-resiliency.md)

  - [<span data-ttu-id="74d07-118">Planen der Integration von Exchange Unified Messaging in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74d07-118">Planning for Exchange Unified Messaging integration in Lync Server 2013</span></span>](lync-server-2013-planning-for-exchange-unified-messaging-integration.md)

  - [<span data-ttu-id="74d07-119">Planen des Anrufsteuerungsdiensts in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74d07-119">Planning for call admission control in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-admission-control.md)

  - [<span data-ttu-id="74d07-120">Planen von Notrufdiensten (E9-1-1) in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74d07-120">Planning for emergency services (E9-1-1) in Lync Server 2013</span></span>](lync-server-2013-planning-for-emergency-services-e9-1-1.md)

  - [<span data-ttu-id="74d07-121">Planung der Medienumgehung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74d07-121">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)

  - [<span data-ttu-id="74d07-122">Planen privater Telefonleitungen mit lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74d07-122">Planning for private telephone lines with Lync Server 2013</span></span>](lync-server-2013-planning-for-private-telephone-lines.md)

  - [<span data-ttu-id="74d07-123">Planung des standortbasierten Routings in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74d07-123">Planning for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-planning-for-location-based-routing.md)

  - [<span data-ttu-id="74d07-124">Planen der Ausfallsicherheit für Enterprise-VoIP in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74d07-124">Planning for Enterprise Voice resiliency in Lync Server 2013</span></span>](lync-server-2013-planning-for-enterprise-voice-resiliency.md)

  - [<span data-ttu-id="74d07-125">Richtlinien für die Enterprise-VoIP-Bereitstellung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74d07-125">Deployment guidelines for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deployment-guidelines-for-enterprise-voice.md)

  - [<span data-ttu-id="74d07-126">Übersicht über den Bereitstellungsprozess für Enterprise-VoIP in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74d07-126">Deployment process overview for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deployment-process-overview-for-enterprise-voice.md)

  - [<span data-ttu-id="74d07-127">Verschieben von Benutzern zu Enterprise-VoIP in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74d07-127">Moving users to Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-moving-users-to-enterprise-voice.md)

  - [<span data-ttu-id="74d07-128">Lync-Tool für die voranruf Diagnose in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74d07-128">Lync PreCall Diagnostics Tool in Lync Server 2013</span></span>](lync-server-2013-lync-precall-diagnostics-tool.md)

<span data-ttu-id="74d07-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="74d07-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

