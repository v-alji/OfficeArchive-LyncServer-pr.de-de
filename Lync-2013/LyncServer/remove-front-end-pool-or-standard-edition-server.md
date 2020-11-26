---
title: Entfernen eines Front-End-Pools oder Standard Edition-Servers
description: Entfernen Sie den Front-End-Pool oder den Standard Edition-Server.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Remove Front End pool or Standard Edition server
ms:assetid: 83c39a36-49a1-4ac6-9cc5-b0e441b1fdec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688115(v=OCS.15)
ms:contentKeyID: 49733713
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c878d56b073558f4f4b50f31b6742fd581c80241
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440276"
---
# <a name="remove-front-end-pool-or-standard-edition-server"></a><span data-ttu-id="91b1b-103">Entfernen eines Front-End-Pools oder Standard Edition-Servers</span><span class="sxs-lookup"><span data-stu-id="91b1b-103">Remove Front End pool or Standard Edition server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="91b1b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="91b1b-104">

<span> </span></span></span>

<span data-ttu-id="91b1b-105">_**Letztes Änderungsdatum des Themas:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="91b1b-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="91b1b-106">Dieses Thema führt Sie durch den Vorgang zum Entfernen eines Front-End-Pools oder eines Front-End-Servers der Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="91b1b-106">This topic guides you through the process of removing a Front End pool or a Standard Edition Front End Server.</span></span> <span data-ttu-id="91b1b-107">Wenn Sie einen Front-End-Pool entfernen, entfernen Sie jeden Front-End-Server, der zum Pool gehört, als Teil des Prozesses zum Entfernen des Pools.</span><span class="sxs-lookup"><span data-stu-id="91b1b-107">When you remove a Front End pool, you remove each Front End Server that belongs to the pool as a part of the pool removal process.</span></span> <span data-ttu-id="91b1b-108">Wenn Sie einen Standard Edition-Front-End-Server entfernen, müssen Sie die SQL Store-Definition aus dem Topology Builder entfernen.</span><span class="sxs-lookup"><span data-stu-id="91b1b-108">When you remove a Standard Edition Front End Server, you must remove the SQL Store definition from Topology Builder.</span></span>

<div>

## <a name="to-remove-a-front-end-server-pool"></a><span data-ttu-id="91b1b-109">So entfernen Sie einen Front-End-Server Pool</span><span class="sxs-lookup"><span data-stu-id="91b1b-109">To remove a Front End Server pool</span></span>

1.  <span data-ttu-id="91b1b-110">Öffnen Sie den Topologie-Generator.</span><span class="sxs-lookup"><span data-stu-id="91b1b-110">Open Topology Builder.</span></span>

2.  <span data-ttu-id="91b1b-111">Navigieren Sie zum lync Server 2010-Knoten.</span><span class="sxs-lookup"><span data-stu-id="91b1b-111">Navigate to the Lync Server 2010 node.</span></span>

3.  <span data-ttu-id="91b1b-112">Erweitern Sie **Enterprise Edition-Front-End-Pools**, erweitern Sie den Front-End-Pool, klicken Sie mit der rechten Maustaste auf den zu entfernenden Frontend-Pool, und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="91b1b-112">Expand **Enterprise Edition Front End pools**, expand the Front End pool, right-click the Front End pool that you want to remove, and then click **Delete**.</span></span>

4.  <span data-ttu-id="91b1b-113">Veröffentlichen Sie die Topologie, überprüfen Sie den Replikationsstatus, und führen Sie dann den lync Server-Bereitstellungs-Assistenten nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="91b1b-113">Publish the topology, check replication status, and then run the Lync Server Deployment Wizard as needed.</span></span>

</div>

<div>

## <a name="to-remove-a-standard-edition-front-end-server"></a><span data-ttu-id="91b1b-114">So entfernen Sie einen Front-End-Server der Standard Edition</span><span class="sxs-lookup"><span data-stu-id="91b1b-114">To remove a Standard Edition Front End server</span></span>

1.  <span data-ttu-id="91b1b-115">Öffnen Sie den Topologie-Generator.</span><span class="sxs-lookup"><span data-stu-id="91b1b-115">Open Topology Builder.</span></span>

2.  <span data-ttu-id="91b1b-116">Navigieren Sie zum lync Server 2010-Knoten.</span><span class="sxs-lookup"><span data-stu-id="91b1b-116">Navigate to the Lync Server 2010 node.</span></span>

3.  <span data-ttu-id="91b1b-117">Erweitern Sie die **Standard Edition-Front-End-Server**, klicken Sie mit der rechten Maustaste auf den Front-End-Server, den Sie entfernen möchten, und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="91b1b-117">Expand **Standard Edition Front End servers**, right-click the Front End Server that you want to remove, and then click **Delete**.</span></span>

4.  <span data-ttu-id="91b1b-118">Erweitern Sie **SQL Stores**, klicken Sie mit der rechten Maustaste auf die SQL Server-Datenbank, die dem Front-End-Server der Standard Edition zugeordnet ist, und klicken Sie dann auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="91b1b-118">Expand **SQL stores**, right-click the SQL Server database that is associated with the Standard Edition Front End Server, and then click **Delete**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="91b1b-119">Sie müssen die Definition der SQL Server-Datenbanken vom Standard Edition-Front-End-Server entfernen.</span><span class="sxs-lookup"><span data-stu-id="91b1b-119">You must remove the definition of the collocated SQL Server databases from the Standard Edition Front End Server.</span></span>

    
    </div>

5.  <span data-ttu-id="91b1b-120">Veröffentlichen Sie die Topologie, überprüfen Sie den Replikationsstatus, und führen Sie dann den lync Server-Bereitstellungs-Assistenten nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="91b1b-120">Publish the topology, check replication status, and then run the Lync Server Deployment Wizard as needed.</span></span>

<span data-ttu-id="91b1b-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="91b1b-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

