---
title: 'Lync Server 2013: Wiederherstellen von Daten und Einstellungen'
description: 'Lync Server 2013: Wiederherstellen von Daten und Einstellungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring data and settings
ms:assetid: b07f5dd7-7bed-4819-8cb5-617f5acd478e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202185(v=OCS.15)
ms:contentKeyID: 51541503
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 694b1e362d729d354b08367d31c47e8ca866dd91
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442530"
---
# <a name="restoring-data-and-settings-in-lync-server-2013"></a><span data-ttu-id="7f0d1-103">Wiederherstellen von Daten und Einstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f0d1-103">Restoring data and settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7f0d1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7f0d1-104">

<span> </span></span></span>

<span data-ttu-id="7f0d1-105">_**Letztes Änderungsdatum des Themas:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="7f0d1-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="7f0d1-106">Wenn Sie eine Disaster Recovery-Topologie mit gekoppelten Pools implementiert haben und einer dieser Front-End-Pools nach unten gegangen ist und Sie den Dienst schnell für Ihre Benutzer wiederherstellen müssen, lesen Sie [Failover eines Pools in lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span><span class="sxs-lookup"><span data-stu-id="7f0d1-106">If you have implemented a disaster recovery topology with paired pools, and one of those Front End pools has gone down and you need to quickly restore service to your users, see [Failing over a pool in Lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span></span> <span data-ttu-id="7f0d1-107">Verwenden Sie andernfalls die Informationen in den folgenden Themen zusammen mit den Arbeitsblättern in [Arbeitsblättern für die Sicherung und Wiederherstellung für lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md), um lync Server nach einem Ausfall oder Ausfall wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="7f0d1-107">Otherwise, use the information in the following topics, along with the worksheets in [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md), to restore Lync Server after a failure or outage.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7f0d1-108">Um Ausfallzeiten und potenzielle Datenverluste zu verringern, führen Sie die in diesem Dokument beschriebenen Wiederherstellungsverfahren nur aus, wenn die Problembehandlung bei der Identifizierung und Behebung des Problems nicht wirksam ist.</span><span class="sxs-lookup"><span data-stu-id="7f0d1-108">To reduce downtime and potential data loss, perform the restoration procedures described in this document only if troubleshooting procedures are not effective in identifying and correcting the problem.</span></span> <span data-ttu-id="7f0d1-109">Versuchen Sie während der Problembehandlung, die Auswirkungen auf andere Server und Komponenten zu minimieren, während Sie die Server herunterfahren und neu starten.</span><span class="sxs-lookup"><span data-stu-id="7f0d1-109">During troubleshooting, try to minimize the impact on other servers and components as you shut down and restart servers.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7f0d1-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="7f0d1-110">In This Section</span></span>

  - [<span data-ttu-id="7f0d1-111">Vorbereiten der Wiederherstellung von lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f0d1-111">Preparing to restore Lync Server 2013</span></span>](lync-server-2013-preparing-to-restore-lync-server.md)

  - [<span data-ttu-id="7f0d1-112">Wiederherstellen eines Standard Edition-Servers in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f0d1-112">Restoring a Standard Edition server in Lync Server 2013</span></span>](lync-server-2013-restoring-a-standard-edition-server.md)

  - [<span data-ttu-id="7f0d1-113">Wiederherstellen des Servers, auf dem der zentrale Verwaltungsspeicher in lync Server 2013 gehostet wird</span><span class="sxs-lookup"><span data-stu-id="7f0d1-113">Restoring the server hosting the Central Management store in Lync Server 2013</span></span>](lync-server-2013-restoring-the-server-hosting-the-central-management-store.md)

  - [<span data-ttu-id="7f0d1-114">Wiederherstellen eines Enterprise Edition-Back-End-Servers in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f0d1-114">Restoring an Enterprise Edition Back End Server in Lync Server 2013</span></span>](lync-server-2013-restoring-an-enterprise-edition-back-end-server.md)

  - [<span data-ttu-id="7f0d1-115">Wiederherstellen eines Enterprise Edition-Mitgliedsservers in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f0d1-115">Restoring an Enterprise Edition member server in Lync Server 2013</span></span>](lync-server-2013-restoring-an-enterprise-edition-member-server.md)

  - [<span data-ttu-id="7f0d1-116">Wiederherstellen eines lync Server-Pools in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f0d1-116">Restoring a Lync Server pool in Lync Server 2013</span></span>](lync-server-2013-restoring-a-lync-server-pool.md)

  - [<span data-ttu-id="7f0d1-117">Durchführen eines ABC-Front-End-Pool-Failovers in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f0d1-117">Performing an ABC Front End pool failover in Lync Server 2013</span></span>](lync-server-2013-performing-an-abc-front-end-pool-failover.md)

  - [<span data-ttu-id="7f0d1-118">Wiederherstellen eines Dateispeichers in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f0d1-118">Restoring a file store in Lync Server 2013</span></span>](lync-server-2013-restoring-a-file-store.md)

  - [<span data-ttu-id="7f0d1-119">Wiederherstellen von Überwachungs-oder Archivierungsdaten in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f0d1-119">Restoring monitoring or archiving data in Lync Server 2013</span></span>](lync-server-2013-restoring-monitoring-or-archiving-data.md)

  - [<span data-ttu-id="7f0d1-120">Wiederherstellen beständiger Chat-Daten in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7f0d1-120">Restoring Persistent Chat data in Lync Server 2013</span></span>](lync-server-2013-restoring-persistent-chat-data.md)

<span data-ttu-id="7f0d1-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7f0d1-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

