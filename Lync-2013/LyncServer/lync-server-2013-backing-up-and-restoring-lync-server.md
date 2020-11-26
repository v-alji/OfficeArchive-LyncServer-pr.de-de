---
title: 'Lync Server 2013: Sichern und Wiederherstellen von lync Server'
description: 'Lync Server 2013: Sichern und Wiederherstellen von lync Server'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up and restoring Lync Server 2013
ms:assetid: 07dc1f5e-af66-4e18-bf39-881dceff8bc3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202160(v=OCS.15)
ms:contentKeyID: 51541443
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c1a7024b2264fb895d1562a6da0775f9397644b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438141"
---
# <a name="backing-up-and-restoring-lync-server-2013"></a><span data-ttu-id="5f436-103">Sichern und Wiederherstellen von lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f436-103">Backing up and restoring Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5f436-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5f436-104">

<span> </span></span></span>

<span data-ttu-id="5f436-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="5f436-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="5f436-106">In diesem Abschnitt finden Sie die bewährten Methoden zum Sichern Ihrer lync Server 2013-Daten sowie zum Wiederherstellen bei einem Fehler.</span><span class="sxs-lookup"><span data-stu-id="5f436-106">In this section, you’ll find the best practices for backing up your Lync Server 2013 data, and for restoring it if you have a failure.</span></span> <span data-ttu-id="5f436-107">Diese bewährten Methoden gelten für die folgenden Situationen:</span><span class="sxs-lookup"><span data-stu-id="5f436-107">These best practices apply to the following situations:</span></span>

  - <span data-ttu-id="5f436-108">Ein gesamter lync Server-Pool eines beliebigen Typs (Front-End-Server, Edgeserver, Vermittlungsserver, beständiger Chat Server oder Director) oder ein einzelner Server in einem dieser Pools.</span><span class="sxs-lookup"><span data-stu-id="5f436-108">An entire Lync Server pool of any type (Front End Server, Edge Server, Mediation Server, Persistent Chat Server, or Director), or an individual server in one of these pools.</span></span>

  - <span data-ttu-id="5f436-109">Der zentrale Verwaltungs Server</span><span class="sxs-lookup"><span data-stu-id="5f436-109">The Central Management Server</span></span>

  - <span data-ttu-id="5f436-110">Ein Standard Edition-Server</span><span class="sxs-lookup"><span data-stu-id="5f436-110">A Standard Edition server</span></span>

  - <span data-ttu-id="5f436-111">Ein Enterprise Edition-Back-End-Server</span><span class="sxs-lookup"><span data-stu-id="5f436-111">An Enterprise Edition Back End Server</span></span>

  - <span data-ttu-id="5f436-112">Ein Dateispeicher</span><span class="sxs-lookup"><span data-stu-id="5f436-112">A File Store</span></span>

  - <span data-ttu-id="5f436-113">Eine Archivierungsdatenbank, eine Überwachungsdatenbank oder eine persistente Chat Datenbank</span><span class="sxs-lookup"><span data-stu-id="5f436-113">An Archiving database, Monitoring database, or Persistent Chat database</span></span>

<span data-ttu-id="5f436-114">Dieser Abschnitt enthält keine Informationen zum Wiederherstellen einer gesamten Website oder zur Entwicklung einer Standby-Website.</span><span class="sxs-lookup"><span data-stu-id="5f436-114">This section does not include information about restoring an entire site or for developing a standby site.</span></span> <span data-ttu-id="5f436-115">Details zur Entwicklung einer Disaster Recovery-Lösung mit gekoppelten Front-End-Pools finden Sie unter [Planen von Hochverfügbarkeits-und Disaster Recovery in lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="5f436-115">For details about developing a disaster recovery solution with paired Front End pools, see [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span> <span data-ttu-id="5f436-116">Dies ist die empfohlene Methode für die Planung der Notfallwiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="5f436-116">This is the recommended method for planning for disaster recovery.</span></span>

<span data-ttu-id="5f436-117">Wenn Sie gekoppelte Front-End-Pools bereitgestellt haben, können Sie diesen Pool mit einem neuen vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) aus dem gekoppelten Pool wiederherstellen, wenn eines dieser Pools ausfällt und nicht wiederhergestellt werden kann.</span><span class="sxs-lookup"><span data-stu-id="5f436-117">If you have deployed paired Front End pools, if one of these pools fails and becomes unrecoverable, you can restore this pool with a new fully qualified domain name (FQDN) from its paired pool.</span></span> <span data-ttu-id="5f436-118">Ausführliche Informationen zu den Schritten zum Durchführen dieser Wiederherstellung finden Sie unter [Failover eines Pools in lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span><span class="sxs-lookup"><span data-stu-id="5f436-118">For details on the steps to perform this recovery, see [Failing over a pool in Lync Server 2013](lync-server-2013-failing-over-a-pool.md).</span></span> <span data-ttu-id="5f436-119">Wenn Sie später einen fehlerhaften und nicht behebbaren Pool erstellen möchten, der Teil eines Front-End-Paars war, können Sie die Schritte unter [Durchführen eines Failovers des ABC-Front-End-Pools in lync Server 2013](lync-server-2013-performing-an-abc-front-end-pool-failover.md)verwenden.</span><span class="sxs-lookup"><span data-stu-id="5f436-119">Additionally, if you later want to recreate a failed and unrecoverable pool that was part of a Front End pair, you can use the steps in [Performing an ABC Front End pool failover in Lync Server 2013](lync-server-2013-performing-an-abc-front-end-pool-failover.md).</span></span>

<span data-ttu-id="5f436-120">Die in diesem Dokument beschriebene Methodik umfasst besondere Aspekte in der Planungsphase.</span><span class="sxs-lookup"><span data-stu-id="5f436-120">The methodology described in this document involves special considerations during the planning phase.</span></span> <span data-ttu-id="5f436-121">Ausführliche Informationen finden Sie unter [Einrichten eines Sicherungs-und Wiederherstellungsplans für lync Server 2013](lync-server-2013-establishing-a-backup-and-restoration-plan.md).</span><span class="sxs-lookup"><span data-stu-id="5f436-121">For details, see [Establishing a backup and restoration plan for Lync Server 2013](lync-server-2013-establishing-a-backup-and-restoration-plan.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5f436-122">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="5f436-122">In This Section</span></span>

  - [<span data-ttu-id="5f436-123">Vorbereiten der Sicherung und Wiederherstellung von lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f436-123">Preparing for Lync Server 2013 backup and restoration</span></span>](lync-server-2013-preparing-for-lync-server-backup-and-restoration.md)

  - [<span data-ttu-id="5f436-124">Sichern von Daten und Einstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f436-124">Backing up data and settings in Lync Server 2013</span></span>](lync-server-2013-backing-up-data-and-settings.md)

  - [<span data-ttu-id="5f436-125">Wiederherstellen von Daten und Einstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f436-125">Restoring data and settings in Lync Server 2013</span></span>](lync-server-2013-restoring-data-and-settings.md)

  - [<span data-ttu-id="5f436-126">Arbeitsblätter zum Sichern und Wiederherstellen für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f436-126">Backup and restoration worksheets for Lync Server 2013</span></span>](lync-server-2013-backup-and-restoration-worksheets.md)

<span data-ttu-id="5f436-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5f436-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

