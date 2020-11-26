---
title: 'Lync Server 2013: Definieren von Übersetzungsregeln'
description: 'Lync Server 2013: Definieren von Übersetzungsregeln.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining translation rules
ms:assetid: 4f6b975a-77e6-474c-9171-b139d84138c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398322(v=OCS.15)
ms:contentKeyID: 48184093
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c0c59225c8dc74d7d97bf3536c7b7073bc977925
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430910"
---
# <a name="defining-translation-rules-in-lync-server-2013"></a><span data-ttu-id="bf109-103">Definieren von Übersetzungsregeln in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf109-103">Defining translation rules in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bf109-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bf109-104">

<span> </span></span></span>

<span data-ttu-id="bf109-105">_**Letztes Änderungsdatum des Themas:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="bf109-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="bf109-106">Lync Server 2013 Enterprise-VoIP leitet Anrufe basierend auf Telefonnummern, die im E. 164-Format normalisiert wurden, weiter.</span><span class="sxs-lookup"><span data-stu-id="bf109-106">Lync Server 2013 Enterprise Voice routes calls based on phone numbers normalized to E.164 format.</span></span> <span data-ttu-id="bf109-107">Das bedeutet, dass alle gewählten Zeichenfolgen im E. 164-Format normalisiert werden müssen, um RNL (Reverse Number Lookup) durchzuführen, damit Sie in den entsprechenden SIP-URI übersetzt werden können.</span><span class="sxs-lookup"><span data-stu-id="bf109-107">This means that all dialed strings must be normalized to E.164 format for the purpose of performing reverse number lookup (RNL) so they can be translated to their matching SIP URI.</span></span> <span data-ttu-id="bf109-108">Lync Server 2013 bietet die Möglichkeit, die aufgerufene ID und die Rufnummernanzeige-Präsentation zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="bf109-108">Lync Server 2013 provides the ability to manipulate the called ID and the caller ID presentation.</span></span>

<span data-ttu-id="bf109-109">In diesem Abschnitt wird erläutert, wie die angerufene ID und die Rufnummernanzeige geändert werden.</span><span class="sxs-lookup"><span data-stu-id="bf109-109">This section discusses how to manipulate the called ID and caller ID.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="bf109-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="bf109-110">In This Section</span></span>

  - [<span data-ttu-id="bf109-111">Präsentation der Rufnummernanzeige in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf109-111">Caller ID presentation in Lync Server 2013</span></span>](lync-server-2013-caller-id-presentation.md)

  - [<span data-ttu-id="bf109-112">Aufgerufene ID-Präsentation in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf109-112">Called ID presentation in Lync Server 2013</span></span>](lync-server-2013-called-id-presentation.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="bf109-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf109-113">See Also</span></span>


[<span data-ttu-id="bf109-114">Definieren von Normalisierungsregeln in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf109-114">Defining normalization rules in Lync Server 2013</span></span>](lync-server-2013-defining-normalization-rules.md)  
  

<span data-ttu-id="bf109-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bf109-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

