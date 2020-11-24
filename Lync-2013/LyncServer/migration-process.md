---
title: Migrationsvorgang
description: Migrationsprozess.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migration process
ms:assetid: 13d71f4b-9d5e-4ea3-9e93-29fdad7ac68f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204696(v=OCS.15)
ms:contentKeyID: 48183474
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f363bd79a3d3be709d731d2ca4bffb4f83fe89ea
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394655"
---
# <a name="migration-process"></a><span data-ttu-id="e08ef-103">Migrationsvorgang</span><span class="sxs-lookup"><span data-stu-id="e08ef-103">Migration process</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e08ef-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e08ef-104">

<span> </span></span></span>

<span data-ttu-id="e08ef-105">_**Letztes Änderungsdatum des Themas:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="e08ef-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="e08ef-106">Das empfohlene und unterstützte Migrationsverfahren für lync Server 2013 ist eine parallele Migration.</span><span class="sxs-lookup"><span data-stu-id="e08ef-106">The recommended and supported migration procedure for Lync Server 2013 is side-by-side migration.</span></span> <span data-ttu-id="e08ef-107">In diesem Thema wird beschrieben, warum Sie die parallele Migration verwenden sollten, und Sie enthält auch Informationen zum Testen der Koexistenz.</span><span class="sxs-lookup"><span data-stu-id="e08ef-107">This topic describes why you should use side-by-side migration and also includes information about coexistence testing.</span></span>

<div>

## <a name="side-by-side-migration"></a><span data-ttu-id="e08ef-108">Parallele Migration</span><span class="sxs-lookup"><span data-stu-id="e08ef-108">Side-By-Side Migration</span></span>

<span data-ttu-id="e08ef-109">In fast jeder Migration sollten Sie den parallelen Migrationspfad verwenden.</span><span class="sxs-lookup"><span data-stu-id="e08ef-109">In nearly every migration, you should use the side-by-side migration path.</span></span> <span data-ttu-id="e08ef-110">Bei einer parallelen Migration stellen Sie einen neuen Server mit lync Server 2013 zusammen mit einem entsprechenden Server bereit, auf dem lync Server 2010 ausgeführt wird, und übertragen dann Vorgänge auf den neuen Server.</span><span class="sxs-lookup"><span data-stu-id="e08ef-110">In a side-by-side migration, you deploy a new server with Lync Server 2013 alongside a corresponding server that is running Lync Server 2010, and then transfer operations to the new server.</span></span> <span data-ttu-id="e08ef-111">Wenn ein Rollback zu lync Server 2010 erforderlich ist, müssen Sie die Vorgänge nur zurück zu den ursprünglichen Servern verschieben.</span><span class="sxs-lookup"><span data-stu-id="e08ef-111">If it becomes necessary to roll back to Lync Server 2010, you have only to shift operations back to the original servers.</span></span> <span data-ttu-id="e08ef-112">Beachten Sie, dass in dieser Situation alle neuen Besprechungen, die mit aktualisierten Clients geplant sind, nicht funktionieren, und die Clients müssten ebenfalls heruntergestuft werden.</span><span class="sxs-lookup"><span data-stu-id="e08ef-112">Be aware that in this situation any new meetings scheduled with upgraded clients will not work, and the clients would also need to be downgraded.</span></span>

</div>

<div>

## <a name="coexistence-testing"></a><span data-ttu-id="e08ef-113">Koexistenz testen</span><span class="sxs-lookup"><span data-stu-id="e08ef-113">Coexistence Testing</span></span>

<span data-ttu-id="e08ef-114">Nachdem Sie lync Server 2013 parallel mit lync Server 2010 bereitgestellt haben, stellt die Bereitstellung einen Teststatus für die Koexistenz von lync Server 2013 und lync Server 2010 dar.</span><span class="sxs-lookup"><span data-stu-id="e08ef-114">After you have deployed Lync Server 2013 in parallel with Lync Server 2010, the deployment represents a coexistence testing state of Lync Server 2013 and Lync Server 2010.</span></span> <span data-ttu-id="e08ef-115">In diesem Zustand ist es wichtig, zu testen und sicherzustellen, dass Dienste gestartet werden, jeder Standort verwaltet werden kann und Clients mit aktuellen und älteren Benutzern kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="e08ef-115">While in this state, it is important to test and ensure that services are started, each site can be administered, and clients can communicate with current and legacy users.</span></span> <span data-ttu-id="e08ef-116">Vor der Migration aller Benutzer ist es sehr wichtig, dass Sie den Zustand jeder Bereitstellung verstehen und sicherstellen, dass jede Bereitstellung funktionsfähig ist und ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="e08ef-116">Prior to the migration of all users, it is very important that you understand the state of each deployment and ensure that each deployment is functional and working properly.</span></span> <span data-ttu-id="e08ef-117">In der Regel ist die Koexistenz Testphase während des Pilottests von lync Server 2013 vorhanden.</span><span class="sxs-lookup"><span data-stu-id="e08ef-117">Typically, the coexistence testing phase exists throughout the pilot testing of Lync Server 2013.</span></span> <span data-ttu-id="e08ef-118">Ältere Benutzer werden für einen bestimmten Zeitraum nach lync Server 2013 verschoben, um sicherzustellen, dass die Anwendungskompatibilität und die Features und Funktionen ordnungsgemäß funktionieren.</span><span class="sxs-lookup"><span data-stu-id="e08ef-118">Legacy users are moved to Lync Server 2013 for a period of time to ensure that application compatibility and features and functions are working properly.</span></span> <span data-ttu-id="e08ef-119">Nach Pilottests werden Benutzer und Anwendungen in die Produktionsversion von lync Server 2013 verschoben, und die Legacy Pools und-Anwendungen von lync Server 2010 werden eingestellt.</span><span class="sxs-lookup"><span data-stu-id="e08ef-119">After pilot testing, users and applications are moved to the production version of Lync Server 2013, and the legacy pools and applications of Lync Server 2010 are retired.</span></span>

<span data-ttu-id="e08ef-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e08ef-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

