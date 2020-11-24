---
title: 'Lync Server 2013: Überprüfen von Normalisierungsregeln für den Parken von Anrufen'
description: 'Lync Server 2013: Überprüfen der Normalisierungsregeln für den Parken von Anrufen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify normalization rules for Call Park
ms:assetid: deaa170f-041e-45cb-8eab-f02931ab541e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398981(v=OCS.15)
ms:contentKeyID: 48185646
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2ac4c15091141e3069e7b77533d0e4148459f570
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395034"
---
# <a name="verify-normalization-rules-for-call-park-in-lync-server-2013"></a><span data-ttu-id="f25f2-103">Überprüfen von Normalisierungsregeln für den Parken von Anrufen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f25f2-103">Verify normalization rules for Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f25f2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f25f2-104">

<span> </span></span></span>

<span data-ttu-id="f25f2-105">_**Letztes Änderungsdatum des Themas:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="f25f2-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="f25f2-106">Orbits für das Parken von anrufen dürfen nicht normalisiert werden.</span><span class="sxs-lookup"><span data-stu-id="f25f2-106">Call Park orbits must not be normalized.</span></span> <span data-ttu-id="f25f2-107">Überprüfen Sie Ihre Wählpläne, um sicherzustellen, dass Ihre Orbit-Nummern nicht normalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="f25f2-107">Check your dial plans to be sure that your orbit numbers are not normalized.</span></span> <span data-ttu-id="f25f2-108">Wenn Sie eine zusätzliche Normalisierungsregel erstellen müssen, um zu verhindern, dass ihre Umlaufbahnen normalisiert werden, führen Sie die Schritte unter [Erstellen eines Wählplans in lync Server 2013](lync-server-2013-create-a-dial-plan.md) aus, um eine neue Normalisierungsregel zu definieren, damit das **Übereinstimmungsmuster** den Umlaufbahn Bereich identifiziert und das **Übersetzungsmuster** **$1** ist.</span><span class="sxs-lookup"><span data-stu-id="f25f2-108">If you must create an additional normalization rule to prevent your orbits from being normalized, follow the procedure in [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md) to define a new normalization rule, so that **Pattern to match** identifies the orbit range and **Translation pattern** is **$1**.</span></span> <span data-ttu-id="f25f2-109">Wenn beispielsweise der Orbit-Bereich Ihres Anruf Parks 7000 – 7999 ist, ist das **Muster, das übereinstimmen** soll, **^ (7 \\ d {3} ) $** , und das **Übersetzungsmuster** ist **$1**.</span><span class="sxs-lookup"><span data-stu-id="f25f2-109">For example, if your Call Park orbit range is 7000 – 7999, the **Pattern to match** is **^(7\\d{3})$** and **Translation pattern** is **$1**.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="f25f2-110">Stellen Sie sicher, dass die standardmäßige Normalisierungsregel in Ihren Wählplänen nicht den Ausdruck <STRONG>^(\d\*)</STRONG> enthält.</span><span class="sxs-lookup"><span data-stu-id="f25f2-110">Be sure that the default normalization rule in your dial plans does not contain <STRONG>^(\d\*)</STRONG>.</span></span> <span data-ttu-id="f25f2-111">Andernfalls wird Ihre Normalisierungsregel für den Anruf Park nie ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="f25f2-111">Otherwise, your Call Park normalization rule will never run.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f25f2-112">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f25f2-112">See Also</span></span>


[<span data-ttu-id="f25f2-113">Erstellen eines Wählplans in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f25f2-113">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)  
  

<span data-ttu-id="f25f2-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f25f2-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

