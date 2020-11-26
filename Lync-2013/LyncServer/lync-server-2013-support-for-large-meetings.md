---
title: 'Lync Server 2013: Unterstützung für große Besprechungen'
description: Lync Server 2013-Unterstützung für umfangreiche Besprechungen
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Support for large meetings
ms:assetid: 8f0446d5-1ed9-4ea0-bb97-6c062a98a1eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205090(v=OCS.15)
ms:contentKeyID: 48184820
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bb37cbfb95e36b9a07604eb4fbbc548e4d7ce9a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423666"
---
# <a name="support-for-large-meetings-in-lync-server-2013"></a><span data-ttu-id="7faf1-103">Unterstützung für große Besprechungen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7faf1-103">Support for large meetings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7faf1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7faf1-104">

<span> </span></span></span>

<span data-ttu-id="7faf1-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="7faf1-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="7faf1-106">Lync Server 2013 kann Besprechungen mit bis zu 1000 Teilnehmern mithilfe von Audio/Video-Konferenzen (A/V) unterstützen, einschließlich der Freigabe von PowerPoint-Präsentationen.</span><span class="sxs-lookup"><span data-stu-id="7faf1-106">Lync Server 2013 can support meetings with up to 1000 participants using audio/video (A/V) conferencing, including sharing PowerPoint presentations.</span></span> <span data-ttu-id="7faf1-107">Hierzu muss ein dedizierter Pool konfiguriert werden, der große Besprechungen unterstützt und so verwaltet wird, dass er das Hosten einer einzigen großen Besprechung sicherstellt.</span><span class="sxs-lookup"><span data-stu-id="7faf1-107">This support requires a dedicated pool configured to support large meetings and managed in a way that ensures hosting of only a single large meeting at a time.</span></span>

<span data-ttu-id="7faf1-108">In diesem Abschnitt wird beschrieben, wie Sie große Besprechungen mithilfe eines dedizierten lync Server 2013-Pools unterstützen.</span><span class="sxs-lookup"><span data-stu-id="7faf1-108">This section describes how to support large meetings using a dedicated Lync Server 2013 pool.</span></span> <span data-ttu-id="7faf1-109">Er beschreibt Skalierbarkeits Überlegungen und die Implementierungsanforderungen für einen dedizierten Pool, einschließlich Topologie-, Hardware-, Software-und Konfigurationsanforderungen.</span><span class="sxs-lookup"><span data-stu-id="7faf1-109">It describes scalability considerations and the implementation requirements for a dedicated pool, including topology, hardware, software, and configuration requirements.</span></span> <span data-ttu-id="7faf1-110">Darüber hinaus bietet es eine Reihe bewährter Methoden zur Unterstützung großer Besprechungen, eine Zusammenfassung der Testmethoden und Ergebnisse der Server Skalierbarkeitstests, die vom lync Server Engineering-Team durchgeführt wurden, und die Antworten auf häufig gestellte Fragen zum Support für große Besprechungen.</span><span class="sxs-lookup"><span data-stu-id="7faf1-110">It also provides a set of best practice recommendations for supporting large meetings, a summary of the test methods and results of server scalability testing conducted by the Lync Server engineering team, and the answers to frequently asked questions about support for large meetings.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7faf1-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="7faf1-111">In This Section</span></span>

  - [<span data-ttu-id="7faf1-112">Übersicht über die Skalierbarkeit von Konferenzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7faf1-112">Overview of conferencing scalability in Lync Server 2013</span></span>](lync-server-2013-conferencing-scalability-overview.md)

  - [<span data-ttu-id="7faf1-113">Unterstützen von umfangreichen Besprechungen mit lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7faf1-113">Supporting large meetings using Lync Server 2013</span></span>](lync-server-2013-supporting-large-meetings.md)

  - [<span data-ttu-id="7faf1-114">Häufig gestellte Fragen zu Besprechungs Support für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7faf1-114">Large meeting support FAQ for Lync Server 2013</span></span>](lync-server-2013-large-meeting-support-faq.md)

<span data-ttu-id="7faf1-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7faf1-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

