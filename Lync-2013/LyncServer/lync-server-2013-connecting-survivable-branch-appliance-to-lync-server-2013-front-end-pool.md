---
title: Verbinden einer Survivable Branch Appliance mit einem Lync Server 2013-Front-End-Pool
description: Verbinden einer Survival-Branch-Appliance mit dem lync Server 2013-Front-End-Pool
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Connecting Survivable Branch Appliance to Lync Server 2013 Front End pool
ms:assetid: 3c7ca33f-5295-4d82-9152-41d8bc6f35cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688026(v=OCS.15)
ms:contentKeyID: 49733616
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6ef917d3db6a1d653ac716d6c078e1df240fb31d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432261"
---
# <a name="connecting-survivable-branch-appliance-to-lync-server-2013-front-end-pool"></a><span data-ttu-id="6274a-103">Verbinden einer Survivable Branch Appliance mit einem Lync Server 2013-Front-End-Pool</span><span class="sxs-lookup"><span data-stu-id="6274a-103">Connecting Survivable Branch Appliance to Lync Server 2013 Front End pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6274a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6274a-104">

<span> </span></span></span>

<span data-ttu-id="6274a-105">_**Letztes Änderungsdatum des Themas:** 2012-10-05_</span><span class="sxs-lookup"><span data-stu-id="6274a-105">_**Topic Last Modified:** 2012-10-05_</span></span>

<span data-ttu-id="6274a-106">Jede Survivable Branch Appliance (SBA) ist mit einem Front-End-Pool verknüpft, der als Sicherungs Registrierungsstelle für die SBA fungiert.</span><span class="sxs-lookup"><span data-stu-id="6274a-106">Every Survivable Branch Appliance (SBA) is associated with a Front End pool, which serves as a backup Registrar for the SBA.</span></span> <span data-ttu-id="6274a-107">Wenn der Front-End-Pool auf lync Server 2013 aktualisiert wird, muss der SBA vom Front-End-Pool entfernt werden, während der Front-End-Pool aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="6274a-107">When the Front End pool is upgraded to Lync Server 2013, the SBA must be disassociated from the Front End pool while the Front End pool is upgraded.</span></span> <span data-ttu-id="6274a-108">Nach dem Upgrade des Front-End-Pools kann die SBA dem Front-End-Pool erneut zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="6274a-108">After the Front End pool is upgraded, the SBA can be reassociated with the Front End pool.</span></span> <span data-ttu-id="6274a-109">Dies umfasst das Löschen des SBA aus der Topologie im Topologie-Generator und das anschließende erneute Hinzufügen des SBA zu Topology Builder.</span><span class="sxs-lookup"><span data-stu-id="6274a-109">This involves deleting the SBA from the topology in Topology Builder and then adding the SBA, again, to Topology Builder.</span></span> <span data-ttu-id="6274a-110">Benutzer, die in der SBA verwaltet werden, müssen in einen anderen Front-End-Pool verschoben werden, bevor Sie die SBA aus der Topologie entfernen.</span><span class="sxs-lookup"><span data-stu-id="6274a-110">Users homed on the SBA must be moved to another Front End pool before removing the SBA from the topology.</span></span> <span data-ttu-id="6274a-111">Nachdem die SBA wieder zur Topologie hinzugefügt wurde, können diese Benutzer wieder in die SBA verschoben werden.</span><span class="sxs-lookup"><span data-stu-id="6274a-111">After the SBA is added back to the topology, those users can be moved back to the SBA.</span></span>

<span data-ttu-id="6274a-112">Nachfolgend werden die folgenden Schritte zusammengefasst:</span><span class="sxs-lookup"><span data-stu-id="6274a-112">These steps are summarized below:</span></span>

1.  <span data-ttu-id="6274a-113">Verschieben Sie Branch-Benutzer, die in SBA beheimatet sind, in einen anderen Front-End-Pool.</span><span class="sxs-lookup"><span data-stu-id="6274a-113">Move branch users homed on SBA to another Front End pool.</span></span>

2.  <span data-ttu-id="6274a-114">Entfernen Sie SBA aus Ihrer Topologie, um den vorhandenen Front-End-Pool als Sicherungs Registrierungsstelle zu trennen.</span><span class="sxs-lookup"><span data-stu-id="6274a-114">Remove SBA from your topology to disassociate the existing Front End pool as the backup Registrar.</span></span>

3.  <span data-ttu-id="6274a-115">Aktualisieren des Front-End-Pools auf Microsoft lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6274a-115">Upgrade Front End pool to Microsoft Lync Server 2013.</span></span>

4.  <span data-ttu-id="6274a-116">Fügen Sie SBA wieder in Ihre Topologie ein.</span><span class="sxs-lookup"><span data-stu-id="6274a-116">Add SBA back into your topology.</span></span>

5.  <span data-ttu-id="6274a-117">Ordnen Sie den neuen Front-End-Pool der SBA als Sicherungs Registrierungsstelle zu.</span><span class="sxs-lookup"><span data-stu-id="6274a-117">Associate the new Front End pool to the SBA as a backup Registrar.</span></span>

6.  <span data-ttu-id="6274a-118">Verschieben Sie Branch-Benutzer zurück in die SBA.</span><span class="sxs-lookup"><span data-stu-id="6274a-118">Move branch users back to the SBA.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6274a-119">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6274a-119">In This Section</span></span>

  - [<span data-ttu-id="6274a-120">Hinzufügen eines Zweigstellenstandorts mit einer Lync Server 2013 Survivable Branch Appliance zu einer Topologie</span><span class="sxs-lookup"><span data-stu-id="6274a-120">Add Lync Server 2013 Survivable Branch Appliance branch site to your topology</span></span>](lync-server-2013-add-lync-server-2013-survivable-branch-appliance-branch-site-to-your-topology.md)

  - [<span data-ttu-id="6274a-121">Hinzufügen eines Zweigstellenstandorts mit einer Lync Server 2010 Survivable Branch Appliance zu einer Topologie</span><span class="sxs-lookup"><span data-stu-id="6274a-121">Add Lync Server 2010 Survivable Branch Appliance branch site to your topology</span></span>](lync-server-2013-add-lync-server-2010-survivable-branch-appliance-branch-site-to-your-topology.md)

<span data-ttu-id="6274a-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6274a-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

