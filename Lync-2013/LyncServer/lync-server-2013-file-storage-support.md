---
title: 'Lync Server 2013: Dateispeicherunterstützung'
description: Unterstützung für den lync Server 2013-Dateispeicher.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: File storage support
ms:assetid: ed66430d-3c19-4267-938c-956a51005073
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399073(v=OCS.15)
ms:contentKeyID: 48185743
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 03b7c3379c6aad6283f6a55b991ebaec50044bda
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428181"
---
# <a name="file-storage-support-in-lync-server-2013"></a><span data-ttu-id="a2ec3-103">Dateispeicherunterstützung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a2ec3-103">File storage support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a2ec3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a2ec3-104">

<span> </span></span></span>

<span data-ttu-id="a2ec3-105">_**Letztes Änderungsdatum des Themas:** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="a2ec3-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="a2ec3-106">Lync Server 2013 verwendet denselben Dateispeicher für alle Dateispeicher.</span><span class="sxs-lookup"><span data-stu-id="a2ec3-106">Lync Server 2013 uses the same file store for all file storage.</span></span> <span data-ttu-id="a2ec3-107">Die Unterstützung für Dateispeicher umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="a2ec3-107">File storage support includes the following:</span></span>

  - <span data-ttu-id="a2ec3-108">Eine Dateifreigabe entweder in Direct Attached Storage (das) oder in einem SAN (Storage Area Network), einschließlich DFS (Distributed File System), und auf einem redundanten Array von unabhängigen Datenträgern (RAID) für Dateispeicher.</span><span class="sxs-lookup"><span data-stu-id="a2ec3-108">A file share on either direct attached storage (DAS) or a storage area network (SAN), including Distributed File System (DFS), and on a redundant array of independent disks (RAID) for file stores.</span></span> <span data-ttu-id="a2ec3-109">Details zu den Speicheranforderungen finden Sie unter [Technische Voraussetzungen für Front-End-Server, Instant Messaging und Anwesenheitsinformationen in lync Server 2013](lync-server-2013-technical-requirements-for-front-end-servers-instant-messaging-and-presence.md) sowie [Hardware-und Softwareanforderungen für den Director in lync Server 2013](lync-server-2013-hardware-and-software-requirements-for-the-director.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="a2ec3-109">For details about storage requirements, see [Technical requirements for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-technical-requirements-for-front-end-servers-instant-messaging-and-presence.md) and [Hardware and software requirements for the Director in Lync Server 2013](lync-server-2013-hardware-and-software-requirements-for-the-director.md) in the Planning documentation.</span></span> <span data-ttu-id="a2ec3-110">Ausführliche Informationen zum Betriebssystem DFS für Windows Server 2008 finden Sie in der schrittweisen Anleitung zu DFS für Windows Server 2008 unter [https://go.microsoft.com/fwlink/p/?linkId=202835](https://go.microsoft.com/fwlink/p/?linkid=202835) .</span><span class="sxs-lookup"><span data-stu-id="a2ec3-110">For details about DFS for Windows Server 2008 operating system, see the DFS Step-by-Step Guide for Windows Server 2008 at [https://go.microsoft.com/fwlink/p/?linkId=202835](https://go.microsoft.com/fwlink/p/?linkid=202835).</span></span>

  - <span data-ttu-id="a2ec3-111">Ein freigegebener Cluster für die Dateifreigabe.</span><span class="sxs-lookup"><span data-stu-id="a2ec3-111">A shared cluster for the file share.</span></span> <span data-ttu-id="a2ec3-112">Wenn Sie einen freigegebenen Cluster verwenden, sollten Sie Cluster Server mit Windows Server 2008 oder Windows Server 2008 R2 verwenden.</span><span class="sxs-lookup"><span data-stu-id="a2ec3-112">If you use a shared cluster, you should use cluster servers running Windows Server 2008 or Windows Server 2008 R2.</span></span> <span data-ttu-id="a2ec3-113">Die Verwendung von Clusterservern, auf denen eine ältere Version von Windows ausgeführt wird, kann zu Berechtigungsproblemen führen, die verhindern, dass einige Features verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="a2ec3-113">Using cluster servers running an older version of Windows may result in permission issues that prevent some features from being available.</span></span> <span data-ttu-id="a2ec3-114">Verwenden Sie die Cluster Verwaltung, um die Dateifreigaben zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="a2ec3-114">Use the Cluster Administrator to create the file shares.</span></span> <span data-ttu-id="a2ec3-115">Details zur Verwendung des Cluster Administrators finden Sie im Microsoft Knowledge Base-Artikel 284838, "So erstellen Sie eine Server Cluster-Dateifreigabe mit Cluster.exe" [https://go.microsoft.com/fwlink/p/?linkId=140899](https://go.microsoft.com/fwlink/p/?linkid=140899) .</span><span class="sxs-lookup"><span data-stu-id="a2ec3-115">For details about using the Cluster Administrator, see Microsoft Knowledge Base article 284838, "How to Create a Server Cluster File Share with Cluster.exe" at [https://go.microsoft.com/fwlink/p/?linkId=140899](https://go.microsoft.com/fwlink/p/?linkid=140899).</span></span>

<span data-ttu-id="a2ec3-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a2ec3-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

