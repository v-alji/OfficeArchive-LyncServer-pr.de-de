---
title: 'Lync Server 2013: Kapazitätsplanung für das Parken von Anrufen'
description: 'Lync Server 2013: Kapazitätsplanung für den Park für Anrufe.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity planning for Call Park
ms:assetid: 75520310-760a-4b1b-bcc1-4d724d13f87a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg416493(v=OCS.15)
ms:contentKeyID: 48184529
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 053a6dabad9d10540e84e9e4f43de09057c295f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395162"
---
# <a name="capacity-planning-for-call-park-in-lync-server-2013"></a><span data-ttu-id="ec056-103">Kapazitätsplanung für das Parken von Anrufen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ec056-103">Capacity planning for Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ec056-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ec056-104">

<span> </span></span></span>

<span data-ttu-id="ec056-105">_**Letztes Änderungsdatum des Themas:** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="ec056-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<div id="sectionSection0" class="section">

<span data-ttu-id="ec056-106">In der folgenden Tabelle wird das Benutzermodell des Anruf Parks beschrieben, das Sie als Grundlage für die Kapazitäts Planungsanforderungen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="ec056-106">The following table describes the Call Park user model that you can use as the basis for capacity planning requirements.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="ec056-107">Beachten Sie, dass für die Planung von Disaster Recovery-Kapazität jeder Pool eines gekoppelten Pools in der Lage sein sollte, die Arbeitslasten für die Dienste des Anruf Parks in beiden Pools zu behandeln.</span><span class="sxs-lookup"><span data-stu-id="ec056-107">Keep in mind that, for disaster recovery capacity planning, each pool of a paired pool should be able to handle the workloads for Call Park services in both pools.</span></span>



</div>

### <a name="call-park-user-model"></a><span data-ttu-id="ec056-108">Benutzermodell der Funktion zum Parken von Anrufen</span><span class="sxs-lookup"><span data-stu-id="ec056-108">Call Park User Model</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ec056-109">Metrik</span><span class="sxs-lookup"><span data-stu-id="ec056-109">Metric</span></span></th>
<th><span data-ttu-id="ec056-110">Pro Front-End-Pool (mit 8 Front-End-Servern)</span><span class="sxs-lookup"><span data-stu-id="ec056-110">Per Front End pool (with 8 Front End Servers)</span></span></th>
<th><span data-ttu-id="ec056-111">Pro Standard Edition-Server</span><span class="sxs-lookup"><span data-stu-id="ec056-111">Per Standard Edition server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ec056-112">Rate für das Parken von Anrufen</span><span class="sxs-lookup"><span data-stu-id="ec056-112">Park rate</span></span></p></td>
<td><p><span data-ttu-id="ec056-113">8 pro Minute</span><span class="sxs-lookup"><span data-stu-id="ec056-113">8 per minute</span></span></p></td>
<td><p><span data-ttu-id="ec056-114">1 pro Minute</span><span class="sxs-lookup"><span data-stu-id="ec056-114">1 per minute</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ec056-115">Rate für das Abrufen geparkter Anrufe</span><span class="sxs-lookup"><span data-stu-id="ec056-115">Retrieve parked call rate</span></span></p></td>
<td><p><span data-ttu-id="ec056-116">8 pro Minute</span><span class="sxs-lookup"><span data-stu-id="ec056-116">8 per minute</span></span></p></td>
<td><p><span data-ttu-id="ec056-117">1 pro Minute</span><span class="sxs-lookup"><span data-stu-id="ec056-117">1 per minute</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ec056-118">Durchschnittliche Parkdauer</span><span class="sxs-lookup"><span data-stu-id="ec056-118">Average park duration</span></span></p></td>
<td><p><span data-ttu-id="ec056-119">60 Sekunden</span><span class="sxs-lookup"><span data-stu-id="ec056-119">60 seconds</span></span></p></td>
<td><p><span data-ttu-id="ec056-120">60 Sekunden</span><span class="sxs-lookup"><span data-stu-id="ec056-120">60 seconds</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="ec056-121">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ec056-121">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

