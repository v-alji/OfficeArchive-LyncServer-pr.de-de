---
title: 'Lync Server 2013: Neue Funktionen für die Archivierung'
description: 'Lync Server 2013: neue Archivierungs Features'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New Archiving features
ms:assetid: c002e367-41ad-498d-9d23-8b117ac435b2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205225(v=OCS.15)
ms:contentKeyID: 48185288
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b5b69c90e62914284f178ae328375c6e350f5b3e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425163"
---
# <a name="new-archiving-features-in-lync-server-2013"></a><span data-ttu-id="efbca-103">Neue Funktionen für die Archivierung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="efbca-103">New Archiving features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="efbca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="efbca-104">

<span> </span></span></span>

<span data-ttu-id="efbca-105">_**Letztes Änderungsdatum des Themas:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="efbca-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="efbca-106">Bei der Archivierung in lync Server 2013 können die folgenden Arten von Inhalten archiviert werden:</span><span class="sxs-lookup"><span data-stu-id="efbca-106">Archiving in Lync Server 2013 can archive the following types of content:</span></span>

  - <span data-ttu-id="efbca-107">Peer-zu-Peer-Chatnachrichten</span><span class="sxs-lookup"><span data-stu-id="efbca-107">Peer-to-peer instant messages</span></span>

  - <span data-ttu-id="efbca-108">Konferenzen (Besprechungen), die mehr Parteien-Sofortnachrichten sind</span><span class="sxs-lookup"><span data-stu-id="efbca-108">Conferences (meetings) that are multi-party instant messages</span></span>

  - <span data-ttu-id="efbca-109">Konferenzinhalte, einschließlich hochgeladener Inhalte (z. B. Handzettel) sowie ereignisbezogener Inhalte (z. B. Beitritt zu/Verlassen einer Konferenz, Hochladen/Freigeben von Inhalten oder Änderungen in der Sichtbarkeit)</span><span class="sxs-lookup"><span data-stu-id="efbca-109">Conference content, including uploaded content (for example, handouts) and event-related content (for example, joining, leaving, uploading sharing, and changes in visibility)</span></span>

<span data-ttu-id="efbca-110">Darüber hinaus bietet die Archivierung in lync Server 2013 neue Funktionen, die die Bereitstellung und die Effizienz des Betriebs verbessern.</span><span class="sxs-lookup"><span data-stu-id="efbca-110">Additionally, Archiving in Lync Server 2013 provides new features that improve deployment and operations efficiency.</span></span> <span data-ttu-id="efbca-111">Diese neuen Features bestehen aus:</span><span class="sxs-lookup"><span data-stu-id="efbca-111">These new features consist of:</span></span>

  - <span data-ttu-id="efbca-112">**Übersetzung der Archivierung auf Front-End-Servern.**</span><span class="sxs-lookup"><span data-stu-id="efbca-112">**Collocation of Archiving on Front End Servers.**</span></span>   <span data-ttu-id="efbca-113">Lync Server 2013 verfügt nicht über eine separate Archivierungs Server Rolle.</span><span class="sxs-lookup"><span data-stu-id="efbca-113">Lync Server 2013 does not have a separate Archiving Server role.</span></span> <span data-ttu-id="efbca-114">Die Archivierung ist ein optionales Feature, das auf allen Front-End-Servern in einer Enterprise Edition-Bereitstellung und auf Standard Edition-Servern zur Verfügung steht, die für einen Pool oder eine Website konfiguriert werden können.</span><span class="sxs-lookup"><span data-stu-id="efbca-114">Archiving is an optional feature available on all Front End Servers in an Enterprise Edition deployment, and on Standard Edition servers, that can be implemented configured for a pool or a site.</span></span>

  - <span data-ttu-id="efbca-115">**Integration von Microsoft Exchange.**</span><span class="sxs-lookup"><span data-stu-id="efbca-115">**Microsoft Exchange integration.**</span></span>   <span data-ttu-id="efbca-116">Wenn Sie die Archivierung bereitstellen, können Sie den Datenspeicher für die Archivierung mit Ihrem vorhandenen Exchange 2013-Speicher für alle Benutzer integrieren, die sich in Exchange 2013 befinden und deren Postfächer In-Place halten, sodass Sie keine separaten SQL Server-Datenbanken zum Archivieren von lync-Daten bereitstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="efbca-116">When you deploy Archiving, you can integrate data storage for Archiving with your existing Exchange 2013 storage for all users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold, so you don’t need to deploy separate SQL Server databases to archive Lync data.</span></span> <span data-ttu-id="efbca-117">Wenn Sie keine Exchange 2013-Bereitstellung haben, oder wenn Sie es vorziehen, Sie nicht zu integrieren, oder wenn Sie lync 2013-Benutzer haben, die sich nicht in Exchange 2013 befinden und ihre Postfächer in In-Place halten, können Sie separate Archivierungsdatenbanken bereitstellen, indem Sie SQL Server verwenden, um archivierte Daten aus lync Communications zu speichern.</span><span class="sxs-lookup"><span data-stu-id="efbca-117">If you do not have an Exchange 2013 deployment, or if you prefer not to integrate with it, or if you have any Lync 2013 users who are not homed on Exchange 2013 with their mailboxes put on In-Place Hold, you can deploy separate Archiving databases by using SQL Server to store archived data from Lync communications.</span></span> <span data-ttu-id="efbca-118">Sie können sowohl die Microsoft Exchange-Integration als auch die lync Server 2013-Archivierungsdatenbanken verwenden, wenn Sie die Microsoft Exchange-Integration für einige, aber nicht für alle Benutzer in Ihrer Bereitstellung verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="efbca-118">You can use both Microsoft Exchange integration and Lync Server 2013 Archiving databases if you want to use Microsoft Exchange integration for some but not all users in your deployment.</span></span> <span data-ttu-id="efbca-119">Details zu In-Place Haltebereich finden Sie unter "in-situ-Speicher" unter [https://go.microsoft.com/fwlink/p/?LinkId=267500](https://go.microsoft.com/fwlink/p/?linkid=267500) .</span><span class="sxs-lookup"><span data-stu-id="efbca-119">For details about In-Place Hold, see “In-Place Hold” at [https://go.microsoft.com/fwlink/p/?LinkId=267500](https://go.microsoft.com/fwlink/p/?linkid=267500).</span></span>

  - <span data-ttu-id="efbca-120">**SQL Store-Spiegelung.**</span><span class="sxs-lookup"><span data-stu-id="efbca-120">**SQL Store Mirroring.**</span></span>   <span data-ttu-id="efbca-121">Wenn Sie die Archivierung bereitstellen, können Sie die SQL Server-Datenbankspiegelung für Ihre Archivierungsdatenbank aktivieren.</span><span class="sxs-lookup"><span data-stu-id="efbca-121">When you deploy Archiving, you can enable SQL Server database mirroring for your Archiving database.</span></span>

  - <span data-ttu-id="efbca-122">**Archivierung von Whiteboards und Umfragen.**</span><span class="sxs-lookup"><span data-stu-id="efbca-122">**Archiving of Whiteboards and Polls.**</span></span>   <span data-ttu-id="efbca-123">Archivierte Konferenzinhalte enthalten nun Whiteboards und Umfragen, die während der Besprechung freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="efbca-123">Archived conference content now includes whiteboards and polls that are shared during the meeting.</span></span>

<span data-ttu-id="efbca-124">Die folgenden Inhaltstypen werden nicht archiviert:</span><span class="sxs-lookup"><span data-stu-id="efbca-124">The following types of content are not archived:</span></span>

  - <span data-ttu-id="efbca-125">Peer-to-Peer-Dateiübertragungen</span><span class="sxs-lookup"><span data-stu-id="efbca-125">Peer-to-peer file transfers</span></span>

  - <span data-ttu-id="efbca-126">Audio-/Videoinhalte für Peer-zu-Peer-Chatnachrichten und -konferenzen</span><span class="sxs-lookup"><span data-stu-id="efbca-126">Audio/video for peer-to-peer instant messages and conferences</span></span>

  - <span data-ttu-id="efbca-127">Anwendungsfreigabe für Peer-to-Peer-Sofortnachrichten und-Konferenzen</span><span class="sxs-lookup"><span data-stu-id="efbca-127">Application sharing for peer-to-peer instant messages and conferences</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="efbca-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="efbca-128">See Also</span></span>


[<span data-ttu-id="efbca-129">Planen der Archivierung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="efbca-129">Planning for Archiving in Lync Server 2013</span></span>](lync-server-2013-planning-for-archiving.md)  
  

<span data-ttu-id="efbca-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="efbca-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

