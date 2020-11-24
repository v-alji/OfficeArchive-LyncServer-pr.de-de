---
title: 'Lync Server 2013: Planen von VoIP-Ausfallsicherheit für Zweigstellen'
description: 'Lync Server 2013: Planen der sprach Stabilität von Branch-Site.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for branch-site voice resiliency
ms:assetid: 67713f57-3ded-4127-ac37-57d8099bf384
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398477(v=OCS.15)
ms:contentKeyID: 48184351
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9ce7eb25e1d3078cd2114fc26428f4c8c2ff6508
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394886"
---
# <a name="planning-for-branch-site-voice-resiliency-in-lync-server-2013"></a><span data-ttu-id="5114f-103">Planen von VoIP-Ausfallsicherheit für Zweigstellen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5114f-103">Planning for branch-site voice resiliency in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5114f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5114f-104">

<span> </span></span></span>

<span data-ttu-id="5114f-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="5114f-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="5114f-106">Wenn Sie eine Ausfallsicherheit für Zweigstellen, also den Enterprise-VoIP-Dienst mit hoher Verfügbarkeit, bereitstellen möchten, stehen Ihnen drei Möglichkeiten zur Verfügung:</span><span class="sxs-lookup"><span data-stu-id="5114f-106">If you want to provide branch-site resiliency, that is, high-availability Enterprise Voice service, you have three options for doing so:</span></span>

  - <span data-ttu-id="5114f-107">Survivable Branch Appliance</span><span class="sxs-lookup"><span data-stu-id="5114f-107">Survivable Branch Appliance</span></span>

  - <span data-ttu-id="5114f-108">Survivable Branch Server</span><span class="sxs-lookup"><span data-stu-id="5114f-108">Survivable Branch Server</span></span>

  - <span data-ttu-id="5114f-109">Eine vollständige lync Server-Bereitstellung auf der Zweigstelle</span><span class="sxs-lookup"><span data-stu-id="5114f-109">A full Lync Server deployment at the branch site</span></span>

<span data-ttu-id="5114f-110">Dieser Leitfaden hilft Ihnen bei der Beurteilung, welche Stabilitäts Lösung für Ihre Organisation am besten geeignet ist und welche PSTN-Konnektivitäts-Lösung auf der Grundlage ihrer Resilienz-Lösung zu verwenden ist.</span><span class="sxs-lookup"><span data-stu-id="5114f-110">This guide will help you evaluate which resiliency solution is best for your organization and, based on your resiliency solution, which PSTN-connectivity solution to use.</span></span> <span data-ttu-id="5114f-111">Darüber hinaus können Sie die Bereitstellung der von Ihnen ausgewählten Lösung vorbereiten, indem Sie Voraussetzungen und andere Planungsüberlegungen beschreiben.</span><span class="sxs-lookup"><span data-stu-id="5114f-111">It will also help you prepare to deploy the solution that you choose by describing prerequisites and other planning considerations.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5114f-112">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="5114f-112">In This Section</span></span>

  - [<span data-ttu-id="5114f-113">Ausfallsicherheitsfunktionen für Zweigstellenstandorte in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5114f-113">Branch-site resiliency features in Lync Server 2013</span></span>](lync-server-2013-branch-site-resiliency-features.md)

  - [<span data-ttu-id="5114f-114">Ausfallsicherheitslösungen für Zweigstellenstandorte in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5114f-114">Branch-site resiliency solutions in Lync Server 2013</span></span>](lync-server-2013-branch-site-resiliency-solutions.md)

  - [<span data-ttu-id="5114f-115">Anforderungen für die Ausfallsicherheit an Zweigstellenstandorten für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5114f-115">Branch-site resiliency requirements for Lync Server 2013</span></span>](lync-server-2013-branch-site-resiliency-requirements.md)

<span data-ttu-id="5114f-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5114f-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

