---
title: 'Lync Server 2013: Ändern des einem Front-End-Pool zugeordneten Edgepools'
description: 'Lync Server 2013: Ändern des Edge-Pools, der einem Front-End-Pool zugeordnet ist.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changing the Edge pool associated with a Front End pool
ms:assetid: 369468c7-2c0b-48cc-bbc3-825dad7b85aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688023(v=OCS.15)
ms:contentKeyID: 49733613
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ab22ba35420341e291d51a1ff012459840e63a56
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435047"
---
# <a name="changing-the-edge-pool-associated-with-a-front-end-pool-in-lync-server-2013"></a><span data-ttu-id="1c1a9-103">Ändern des einem Front-End-Pool zugeordneten Edgepools in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1c1a9-103">Changing the Edge pool associated with a Front End pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1c1a9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1c1a9-104">

<span> </span></span></span>

<span data-ttu-id="1c1a9-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="1c1a9-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="1c1a9-106">Wenn ein Edge-Pool ausfällt, der Front-End-Pool am gleichen Standort aber noch ausgeführt wird, müssen Sie den Front-End-Pool so einrichten, dass ein Edge-Pool an einer anderen Website verwendet wird, bis der fehlerhafte Edge-Pool wiederhergestellt wird.</span><span class="sxs-lookup"><span data-stu-id="1c1a9-106">If an Edge pool goes down but the Front End pool at the same site is still running, you will need to set the Front End pool to use an Edge pool at a different site until the failed Edge pool is restored.</span></span>

<div>

## <a name="changing-the-edge-pool-associated-with-a-front-end-pool"></a><span data-ttu-id="1c1a9-107">Ändern des einem Front-End-Pool zugeordneten Edge-Pools</span><span class="sxs-lookup"><span data-stu-id="1c1a9-107">Changing the Edge Pool Associated with a Front End Pool</span></span>

1.  <span data-ttu-id="1c1a9-108">Navigieren Sie im Topologie-Generator zu dem Namen des Front-End-Pools, den Sie ändern müssen.</span><span class="sxs-lookup"><span data-stu-id="1c1a9-108">In Topology Builder, navigate to the name of the Front End pool you need to change.</span></span>

2.  <span data-ttu-id="1c1a9-109">Klicken Sie mit der rechten Maustaste auf den Pool, und klicken Sie dann auf **Eigenschaften bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="1c1a9-109">Right-click the pool, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="1c1a9-110">Verwenden Sie im Abschnitt **Zuordnungen** unter **Edge-Pool zuordnen (für Medienkomponenten)** das Dropdownfeld, um den Edge-Pool auszuwählen, dem Sie diesen Front-End-Pool zuordnen möchten.</span><span class="sxs-lookup"><span data-stu-id="1c1a9-110">In the **Associations** section, under **Associate Edge Pool (for media components)**, use the drop down box to select the Edge pool you want to associate this Front End pool with.</span></span>

4.  <span data-ttu-id="1c1a9-111">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="1c1a9-111">Click **OK**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="1c1a9-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c1a9-112">See Also</span></span>


[<span data-ttu-id="1c1a9-113">Notfallwiederherstellung für Edgeserver in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1c1a9-113">Edge Server disaster recovery in Lync Server 2013</span></span>](lync-server-2013-edge-server-disaster-recovery.md)  
  

<span data-ttu-id="1c1a9-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1c1a9-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

