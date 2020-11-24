---
title: Überlegungen zur Koexistenz
description: Überlegungen zur Koexistenz
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Coexistence considerations
ms:assetid: 9d1a3c0f-492a-4e37-bc2f-63509e328785
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205131(v=OCS.15)
ms:contentKeyID: 48184990
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fd1f9525b37bdee3249e0e47352fdea1bc7f012f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394647"
---
# <a name="coexistence-considerations"></a><span data-ttu-id="ab3db-103">Überlegungen zur Koexistenz</span><span class="sxs-lookup"><span data-stu-id="ab3db-103">Coexistence considerations</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ab3db-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ab3db-104">

<span> </span></span></span>

<span data-ttu-id="ab3db-105">_**Letztes Änderungsdatum des Themas:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="ab3db-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="ab3db-106">Nach der Migration wird nur ein lync Server 2013, beständiger Chat Serverpool vorhanden sein, und Sie können Ihre Legacy Bereitstellung außer Betrieb halten.</span><span class="sxs-lookup"><span data-stu-id="ab3db-106">After migration, only a Lync Server 2013, Persistent Chat Server pool will exist, and you can decommission your legacy deployment.</span></span>

<span data-ttu-id="ab3db-107">Bevor die Migration abgeschlossen ist und Sie Ihre aktuelle Gruppen-Chat Server-Bereitstellung vollständig außer Betrieb genommen haben, verfügen Sie möglicherweise über eine der folgenden Bereitstellungen:</span><span class="sxs-lookup"><span data-stu-id="ab3db-107">Before migration completes and before you have decommissioned your current Group Chat Server deployment completely, you may have any of the following deployments:</span></span>

  - <span data-ttu-id="ab3db-108">Lync Server 2013, Serverpool für beständigen Chat, der in einem lync Server 2013-Pool verwaltet werden muss.</span><span class="sxs-lookup"><span data-stu-id="ab3db-108">Lync Server 2013, Persistent Chat Server pool, which must be homed on a Lync Server 2013 pool.</span></span>

  - <span data-ttu-id="ab3db-109">Lync Server 2010, Gruppen-Chat Pool, der in einem lync Server 2010-Pool verwaltet werden muss.</span><span class="sxs-lookup"><span data-stu-id="ab3db-109">Lync Server 2010, Group Chat pool, which must be homed on a Lync Server 2010 pool.</span></span>

  - <span data-ttu-id="ab3db-110">Office Communications Server 2007 R2-Gruppen-Chat-Pool, der in einem Office Communications Server 2007 R2-Pool verwaltet werden muss.</span><span class="sxs-lookup"><span data-stu-id="ab3db-110">Office Communications Server 2007 R2 Group Chat pool, which must be homed on an Office Communications Server 2007 R2 pool.</span></span>

<span data-ttu-id="ab3db-111">Diese Bereitstellungen können nebeneinander vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="ab3db-111">These deployments can exist side by side.</span></span> <span data-ttu-id="ab3db-112">Die Kategorien, Räume und Add-Ins in einer Bereitstellung interagieren jedoch nicht mit denen in der zugehörigen Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="ab3db-112">However the categories, rooms, and add-ins in one deployment do not interact with those in the accompanying deployment.</span></span>

<span data-ttu-id="ab3db-113">Mithilfe der manuellen Konfiguration kann ein Legacyclient (Gruppen-Chat-Client) eine Verbindung zu einem Pool für Office Communications Server 2007 R2, lync Server 2010, Gruppen-Chat oder lync Server 2013 herstellen.</span><span class="sxs-lookup"><span data-stu-id="ab3db-113">Using manual configuration, a legacy client (Group Chat client) can connect to one pool at a time for Office Communications Server 2007 R2, Lync Server 2010, Group Chat, or Lync Server 2013.</span></span>

<span data-ttu-id="ab3db-114">Lync 2013 (Client) kann nur mit dem lync Server 2013, beständigen Chat Serverpool und nicht mit Legacy-Gruppen Chat Server-Pools interagieren.</span><span class="sxs-lookup"><span data-stu-id="ab3db-114">The Lync 2013 (client) can interact only with the Lync Server 2013, Persistent Chat Server pool, not with legacy Group Chat Server pools.</span></span> <span data-ttu-id="ab3db-115">Zur Verwendung des beständigen Chats in einem lync 2013 (-Client) muss der Benutzer in lync 2013 gehostet und durch Richtlinie aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="ab3db-115">To use Persistent Chat in a Lync 2013 (client), the user must be homed on Lync 2013 and enabled by policy.</span></span>

<span data-ttu-id="ab3db-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ab3db-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

