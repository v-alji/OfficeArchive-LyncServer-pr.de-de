---
title: 'Lync Server 2013: höchst verfügbare Dateifreigabe'
description: 'Lync Server 2013: Dateifreigabe, höchste Verfügbarkeit.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: File sharing high availability
ms:assetid: b8c8d5ec-9397-4128-8d1e-8ec6c30fade7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205203(v=OCS.15)
ms:contentKeyID: 48185238
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 29b0a77d2d03460c640c66b8e8ce2a551edf2d73
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428188"
---
# <a name="file-sharing-high-availability-in-lync-server-2013"></a><span data-ttu-id="feae5-103">Höhere Verfügbarkeit von Dateien in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="feae5-103">File sharing high availability in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="feae5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="feae5-104">

<span> </span></span></span>

<span data-ttu-id="feae5-105">_**Letztes Änderungsdatum des Themas:** 2012-03-30_</span><span class="sxs-lookup"><span data-stu-id="feae5-105">_**Topic Last Modified:** 2012-03-30_</span></span>

<span data-ttu-id="feae5-106">Wenn Sie eine höhere Verfügbarkeit der lync Server-Dateifreigabe in einem einzigen Rechenzentrum sicherstellen möchten, können Sie das verteilte Datei System (Distributed File System, DFS) verwenden.</span><span class="sxs-lookup"><span data-stu-id="feae5-106">To ensure high availability for Lync Server file sharing within a single data center, you can use the Distributed File System (DFS).</span></span> <span data-ttu-id="feae5-107">DFS unterstützt Failover von einem Dateiserver auf einen anderen innerhalb desselben Rechenzentrums.</span><span class="sxs-lookup"><span data-stu-id="feae5-107">DFS supports failover from one file server to another within the same data center.</span></span> <span data-ttu-id="feae5-108">Bei einer umfassenden Bereitstellung empfehlen wir Ihnen die Verwendung von dedizierten Dateiservern, die mithilfe von DFS kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="feae5-108">For a large scale deployment, we recommend that you use dedicated file servers that are paired using DFS.</span></span>

<span data-ttu-id="feae5-109">Je nach Größe Ihres Netzwerks und dem gewünschten Maß an Flexibilität können Sie mit einem Serverpaar alle Dateifreigaben auf einer Website hosten oder ein paar pro Front-End-Pool verwenden.</span><span class="sxs-lookup"><span data-stu-id="feae5-109">Depending on your network's size, and the amount of resiliency you want, you can use one pair of servers to host all file shares in a site, or use one pair per Front End pool.</span></span>

<span data-ttu-id="feae5-110">Bei DFS handelt es sich um einen Best Effort-Datei Replikationsmechanismus, bei dem keine RTO-oder Recovery Point Objective (RPO)-Zusicherungen veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="feae5-110">DFS is a best effort file replication mechanism, with no published recovery time objective (RTO) or recovery point objective (RPO) commitment.</span></span> <span data-ttu-id="feae5-111">Das Failover zwischen den DFS-Servern sollte schnell abgeschlossen sein, aber die Daten Replikationsverzögerung kann verhindern, dass Benutzer die Arbeit in Bearbeitung fortsetzen können, wenn das Failover erfolgt.</span><span class="sxs-lookup"><span data-stu-id="feae5-111">The failover between the DFS servers should be completed quickly, but data replication delay may prevent users from being able to continue work in progress when the failover happens.</span></span>

<span data-ttu-id="feae5-112">Wenn Sie DFS verwenden und der Datenspeicher in der FileShare-Datei wichtig ist, sollten Sie die Dateifreigaben häufig sichern, beispielsweise alle 4 bis 8 Stunden.</span><span class="sxs-lookup"><span data-stu-id="feae5-112">If you use DFS and data store on the fileshare is critical, you should back up the file shares frequently, such as every 4 to 8 hours.</span></span> <span data-ttu-id="feae5-113">Wenn eine Dateifreigabe ausfällt und die Replikation nicht auf dem neuesten Stand ist, können Sie die Sicherung verwenden, um den Inhalt des ausgefallenen Servers auf dem anderen Server wiederherzustellen, der mit dem jetzt nicht mehr verfügbaren Server kombiniert ist.</span><span class="sxs-lookup"><span data-stu-id="feae5-113">When one file share goes down and replication is not up to date, you can use the backup to restore the content on the failed server to the other server that is paired with the server that is now unavailable.</span></span>

<span data-ttu-id="feae5-114"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="feae5-114"></div>

<span> </span>

</div>

</div>

</span></span></div>

