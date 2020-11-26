---
title: Lync Server 2013 unterstützte Pool-Kopplungs Optionen und bewährte Methoden
description: Lync Server 2013 unterstützte Pool-Kopplungs Optionen und bewährte Methoden.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported pool pairing options and best practices
ms:assetid: 142caf34-0f20-47f3-9d32-ce25ab622fad
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204697(v=OCS.15)
ms:contentKeyID: 48183478
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 76d0f8331c0b6998008efff8af70ae3c4b43a9c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441417"
---
# <a name="supported-pool-pairing-options-and-best-practices-for-lync-server-2013"></a><span data-ttu-id="cc9dc-103">Unterstützte Pool-Kopplungs Optionen und bewährte Methoden für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cc9dc-103">Supported pool pairing options and best practices for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cc9dc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cc9dc-104">

<span> </span></span></span>

<span data-ttu-id="cc9dc-105">_**Letztes Änderungsdatum des Themas:** 2017-03-09_</span><span class="sxs-lookup"><span data-stu-id="cc9dc-105">_**Topic Last Modified:** 2017-03-09_</span></span>

<span data-ttu-id="cc9dc-106">Es gibt keine Einschränkung für den Abstand zwischen zwei Rechenzentren, in denen Front-End-Pools miteinander kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="cc9dc-106">There is no restriction on the distance between two data centers that are to include Front End pools paired with each other.</span></span> <span data-ttu-id="cc9dc-107">Wir empfehlen, dass Sie zwei Rechenzentren in der gleichen Weltregion verwenden, mit Hochgeschwindigkeits-Links zwischen Ihnen.</span><span class="sxs-lookup"><span data-stu-id="cc9dc-107">We recommend that you use two data centers in the same world region, with high-speed links between them.</span></span> <span data-ttu-id="cc9dc-108">Am besten ist es, wenn die beiden Rechenzentren voneinander getrennt sind, um zu verhindern, dass ein einzelner Notfall gleichzeitig anschlägt.</span><span class="sxs-lookup"><span data-stu-id="cc9dc-108">It is best if the two data centers are separated enough to avoid a single disaster hitting both at the same time.</span></span>

<span data-ttu-id="cc9dc-109">Die Möglichkeit, zwei Rechenzentren in verschiedenen Weltregionen zu nutzen, kann aufgrund der Latenz bei der Datenreplikation zu einem höheren Datenverlust führen.</span><span class="sxs-lookup"><span data-stu-id="cc9dc-109">Having two data centers across world regions is possible, but could incur higher data loss due to latency in data replication.</span></span>

<span data-ttu-id="cc9dc-110">Beachten Sie bei der Planung, welche Pools als Paar bereitgestellt werden, dass nur die folgenden Paarungen unterstützt werden:</span><span class="sxs-lookup"><span data-stu-id="cc9dc-110">When you plan which pools to pair, you must keep in mind that only the following pairings are supported:</span></span>

  - <span data-ttu-id="cc9dc-111">Enterprise Edition-Pools können nur mit anderen Enterprise Edition-Pools gepaart werden.</span><span class="sxs-lookup"><span data-stu-id="cc9dc-111">Enterprise Edition pools can be paired only with other Enterprise Edition pools.</span></span> <span data-ttu-id="cc9dc-112">Entsprechend können Standard Edition-Pools nur mit anderen Standard Edition-Pools gepaart werden.</span><span class="sxs-lookup"><span data-stu-id="cc9dc-112">Similarly, Standard Edition pools can be paired only with other Standard Edition pools.</span></span>

  - <span data-ttu-id="cc9dc-113">Physische Pools können nur mit anderen physischen Pools gepaart werden.</span><span class="sxs-lookup"><span data-stu-id="cc9dc-113">Physical pools can be paired only with other physical pools.</span></span> <span data-ttu-id="cc9dc-114">Entsprechend können virtuelle Pools nur mit anderen virtuellen Pools gepaart werden.</span><span class="sxs-lookup"><span data-stu-id="cc9dc-114">Similarly, virtual pools can be paired only with other virtual pools.</span></span>

  - <span data-ttu-id="cc9dc-115">Für Pools, die zusammen gekoppelt sind, muss dasselbe Betriebssystem ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="cc9dc-115">Pools that are paired together must be running the same operating system.</span></span>

<span data-ttu-id="cc9dc-p104">Eine Paarung zweier Pools, die nicht diesen Empfehlungen entspricht, wird weder durch den Topologie-Generator noch durch die Topologieüberprüfung verhindert. Der Topologie-Generator lässt z. B. die Paarung eines Enterprise Edition-Pools mit einem Standard Edition-Pool zu. Diese Art von Paarung wird jedoch nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="cc9dc-p104">Neither Topology Builder nor topology validation will prohibit pairing two pools in a way that does not follow these recommendations. For example, Topology Builder allows you to pair an Enterprise Edition pool with a Standard Edition pool. However, these types of pairings are not supported.</span></span>

<span data-ttu-id="cc9dc-119">Jeder Pool in einem Paar sollte in der Lage sein, alle Benutzer aus beiden Pools im Fall eines Notfalls zu bedienen.</span><span class="sxs-lookup"><span data-stu-id="cc9dc-119">Each pool in a pair should have the capacity to serve all users from both pools in the event of a disaster.</span></span>

<span data-ttu-id="cc9dc-120">Wenn Sie Enterprise Edition-Pools koppeln, können Sie auch eine höhere Verfügbarkeit auf den Back-End-Servern implementieren, bei Paaren von Standard Edition-Pools sind jedoch nur die Wiederherstellungsmaßnahmen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="cc9dc-120">If you pair Enterprise Edition pools, you can also implement high availability on the Back End Servers, but for pairs of Standard Edition pools only the disaster recovery measures are available.</span></span>

<span data-ttu-id="cc9dc-121"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cc9dc-121"></div>

<span> </span>

</div>

</div>

</span></span></div>

