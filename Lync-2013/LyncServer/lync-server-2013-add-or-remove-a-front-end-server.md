---
title: 'Lync Server 2013: Hinzufügen oder Entfernen eines Front-End-Servers'
description: 'Lync Server 2013: Hinzufügen oder Entfernen eines Front-End-Servers'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add or remove a Front End Server
ms:assetid: ab748733-6bad-4c93-8dda-db8d5271653d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205153(v=OCS.15)
ms:contentKeyID: 48185050
ms.date: 01/21/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 297bbf42dbba3d4f9926fd5ab9e0d7ed79349dc4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439275"
---
# <a name="add-or-remove-a-front-end-server-in-lync-server-2013"></a><span data-ttu-id="f1396-103">Add or remove a Front End Server in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f1396-103">Add or remove a Front End Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f1396-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f1396-104">

<span> </span></span></span>

<span data-ttu-id="f1396-105">_**Letztes Änderungsdatum des Themas:** 2016-01-21_</span><span class="sxs-lookup"><span data-stu-id="f1396-105">_**Topic Last Modified:** 2016-01-21_</span></span>

<span data-ttu-id="f1396-106">Wenn Sie einen Front-End-Server zu einem Pool hinzufügen oder einen Front-End-Server aus einem Pool entfernen, müssen Sie den Pool erneut starten.</span><span class="sxs-lookup"><span data-stu-id="f1396-106">When you add a Front End Server to a pool, or remove a Front End Server from a pool, you then need to restart the pool.</span></span> <span data-ttu-id="f1396-107">Gehen Sie beim Hinzufügen oder Entfernen eines Front-End-Servers wie folgt vor, um eine Unterbrechung des Diensts für Benutzer zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="f1396-107">To prevent any interruption of service to users, use the following procedure when adding or removing a Front End Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f1396-108">Wenn Sie neue Server zum Pool hinzufügen, aktualisieren Sie Ihre neuen Poolserver, sodass diese im Hinblick auf das kumulative Update auf demselben Stand sind wie die bereits bestehenden Server in dem Pool.</span><span class="sxs-lookup"><span data-stu-id="f1396-108">If you're adding new servers to the pool, update your new pool servers to be at the same Cumulative Update level as the existing servers in the Pool.</span></span>



</div>

<div>

## <a name="to-add-or-remove-front-end-servers"></a><span data-ttu-id="f1396-109">So können Sie Front-End-Server hinzufügen oder entfernen</span><span class="sxs-lookup"><span data-stu-id="f1396-109">To add or remove Front End servers</span></span>

1.  <span data-ttu-id="f1396-110">Wenn Sie alle Front-End-Server entfernen, beenden Sie zunächst neue Verbindungen mit diesen Servern.</span><span class="sxs-lookup"><span data-stu-id="f1396-110">If you are removing any Front End Servers, first stop new connections to those servers.</span></span> <span data-ttu-id="f1396-111">Dazu können Sie das folgende Cmdlet verwenden:</span><span class="sxs-lookup"><span data-stu-id="f1396-111">To do so, you can use the following cmdlet:</span></span>
    
        Stop-CsWindowsServices -Graceful

2.  <span data-ttu-id="f1396-112">Wenn die entfernten Server keine aktuellen Sitzungen haben, beenden Sie die lync Server-Dienste.</span><span class="sxs-lookup"><span data-stu-id="f1396-112">When the servers being removed have no current sessions, stop Lync Server services on them.</span></span>

3.  <span data-ttu-id="f1396-113">Öffnen Sie den Topologie-Generator, und fügen Sie die erforderlichen Server hinzu, oder entfernen Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="f1396-113">Open Topology Builder, and add or remove the necessary servers.</span></span>

4.  <span data-ttu-id="f1396-114">Veröffentlichen Sie die Topologie.</span><span class="sxs-lookup"><span data-stu-id="f1396-114">Publish the topology.</span></span>

5.  <span data-ttu-id="f1396-115">Wenn der Pool von zwei Front-End-Servern auf mehr als zwei oder von mehr als zwei Servern auf genau zwei hinausgegangen ist, müssen Sie das folgende Cmdlet eingeben:</span><span class="sxs-lookup"><span data-stu-id="f1396-115">If the pool has gone from having two Front End Servers to more than two, or gone from more than two servers to exactly two, you need to type the following cmdlet:</span></span>
    
        Reset-CsPoolRegistrarState-ResetType FullReset -PoolFqdn <PoolFqdn>
    
    <span data-ttu-id="f1396-116">Wenn der Pool über drei oder mehr Server verfügt, müssen mindestens drei dieser Server ausgeführt werden, wenn Sie dieses Cmdlet eingeben.</span><span class="sxs-lookup"><span data-stu-id="f1396-116">If the pool has three or more servers, then at least three of those servers must be running when you type this cmdlet.</span></span>

6.  <span data-ttu-id="f1396-117">Starten Sie alle Front-End-Server im Pool einzeln neu.</span><span class="sxs-lookup"><span data-stu-id="f1396-117">Restart all Front End Servers in the pool, one at a time.</span></span>

<span data-ttu-id="f1396-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f1396-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

