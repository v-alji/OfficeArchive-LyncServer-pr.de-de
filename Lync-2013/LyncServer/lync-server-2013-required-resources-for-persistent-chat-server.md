---
title: 'Lync Server 2013: Erforderliche Ressourcen für den Server für beständigen Chat'
description: 'Lync Server 2013: erforderliche Ressourcen für beständigen Chat Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Required resources
ms:assetid: bce50b95-f3c8-407e-963a-d8896ee77fbc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205211(v=OCS.15)
ms:contentKeyID: 48185255
ms.date: 02/05/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 18c81f0017428e4305e46fbcf5580a83af38accf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442701"
---
# <a name="required-resources-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="7d241-103">Erforderliche Ressourcen für den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d241-103">Required resources for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7d241-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7d241-104">

<span> </span></span></span>

<span data-ttu-id="7d241-105">_**Letztes Änderungsdatum des Themas:** 2016-02-05_</span><span class="sxs-lookup"><span data-stu-id="7d241-105">_**Topic Last Modified:** 2016-02-05_</span></span>

<span data-ttu-id="7d241-106">Hochverfügbarkeit und Disaster Recovery für beständigen Chat Server erfordern zusätzliche Ressourcen, die über das hinausgehen, was in der Regel für den vollständigen Betrieb benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="7d241-106">High availability and disaster recovery for Persistent Chat Server requires additional resources beyond what is typically needed for full operation.</span></span> <span data-ttu-id="7d241-107">Bevor Sie den beständigen Chat Server für Hochverfügbarkeit und Disaster Recovery konfigurieren, stellen Sie sicher, dass Sie über die folgenden Ressourcen verfügen, die für den standardmäßigen Serverbetrieb des beständigen Chats erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7d241-107">Before configuring Persistent Chat Server for high availability and disaster recovery, ensure that you have the following resources in addition to what is required for standard Persistent Chat Server operation.</span></span> <span data-ttu-id="7d241-108">Weitere Konfigurationsinformationen finden Sie unter [Konfigurieren des beständigen Chat Servers in lync Server 2013](lync-server-2013-configuring-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="7d241-108">For additional configuration information, see [Configuring Persistent Chat Server in Lync Server 2013](lync-server-2013-configuring-persistent-chat-server.md).</span></span>

  - <span data-ttu-id="7d241-109">Eine dedizierte Datenbankinstanz, die sich im gleichen physikalischen Rechenzentrum befindet, in dem sich das Home-Front-End des Server Diensts für beständigen Chat befindet.</span><span class="sxs-lookup"><span data-stu-id="7d241-109">One dedicated database instance located in the same physical data center in which the home front end of the Persistent Chat Server service is located.</span></span> <span data-ttu-id="7d241-110">Diese Datenbank dient als SQL Server-Spiegelung für die primäre Datenbank für beständigen Chat.</span><span class="sxs-lookup"><span data-stu-id="7d241-110">This database will serve as the SQL Server mirror for the primary Persistent Chat database.</span></span> <span data-ttu-id="7d241-111">Optional können Sie einen zusätzlichen SQL-Server als Spiegelungs Zeuge festlegen, wenn Sie ein automatisches Failover zur Spiegeldatenbank durch stellen möchten.</span><span class="sxs-lookup"><span data-stu-id="7d241-111">Optionally, designate an additional SQL Server to serve as the mirroring witness if you want an automated failover to the mirror database.</span></span>

  - <span data-ttu-id="7d241-112">Eine dedizierte Datenbankinstanz in dem anderen physischen Rechenzentrum.</span><span class="sxs-lookup"><span data-stu-id="7d241-112">One dedicated database instance located in the other physical data center.</span></span> <span data-ttu-id="7d241-113">Diese Datenbank dient als SQL Server-Protokollversand-sekundäre Datenbank für die Datenbank im primären Rechenzentrum.</span><span class="sxs-lookup"><span data-stu-id="7d241-113">This database will serve as the SQL Server Log Shipping secondary database for the database in the primary data center.</span></span>

  - <span data-ttu-id="7d241-114">Eine dedizierte Datenbankinstanz, die als SQL Server-Spiegelung für die sekundäre Datenbank fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="7d241-114">One dedicated database instance to serve as the SQL Server mirror for the secondary database.</span></span> <span data-ttu-id="7d241-115">Optional können Sie einen zusätzlichen SQL Server als Spiegelungs Zeuge auf dem Server angeben.</span><span class="sxs-lookup"><span data-stu-id="7d241-115">Optionally, designate an additional SQL Server to server as the mirroring witness.</span></span> <span data-ttu-id="7d241-116">Beide Instanzen müssen sich im selben physischen Rechenzentrum wie die sekundäre Datenbank befinden.</span><span class="sxs-lookup"><span data-stu-id="7d241-116">Both of these must be located in the same physical data center as the secondary database.</span></span>

  - <span data-ttu-id="7d241-117">Wenn die Kompatibilität des beständigen Chat Servers aktiviert ist, sind zusätzliche drei dedizierte Datenbankinstanzen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7d241-117">If Persistent Chat Server compliance is enabled, an additional three dedicated database instances are required.</span></span> <span data-ttu-id="7d241-118">Ihre Verteilung ist mit denen identisch, die zuvor für die persistente Chat-Datenbank beschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="7d241-118">Their distribution is the same as those previously outlined for the Persistent Chat database.</span></span> <span data-ttu-id="7d241-119">Es ist zwar möglich, dass die Compliance-Datenbank dieselbe SQL Server-Instanz wie die persistente Chat-Datenbank hat, wir empfehlen jedoch eigenständige Instanzen für eine höhere Verfügbarkeit und Disaster Recovery.</span><span class="sxs-lookup"><span data-stu-id="7d241-119">While it is possible for the compliance database to share the same SQL Server instance as the Persistent Chat database, we recommend standalone instances for high availability and disaster recovery.</span></span>

  - <span data-ttu-id="7d241-120">Es muss eine Dateifreigabe erstellt und für die Transaktionsprotokolle des SQL Server-Protokollversands festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="7d241-120">A file share must be created and designated for the SQL Server Log Shipping transaction logs.</span></span> <span data-ttu-id="7d241-121">Alle SQL-Server in beiden Rechenzentren, in denen persistente Chat Datenbanken ausgeführt werden, müssen über Lese-/Schreibzugriff auf diese Dateifreigabe verfügen.</span><span class="sxs-lookup"><span data-stu-id="7d241-121">All SQL Servers in both data centers that run Persistent Chat databases must have read/write access to this file share.</span></span> <span data-ttu-id="7d241-122">Diese Freigabe wird nicht als Teil einer FileStore-Rolle definiert.</span><span class="sxs-lookup"><span data-stu-id="7d241-122">This share is not defined as part of a FileStore role.</span></span>

  - <span data-ttu-id="7d241-123">Eine Dateifreigabe auf dem sekundären Datenbankserver, die als Zielordner für die SQL Server-Transaktionsprotokolle fungieren soll, die aus der Dateifreigabe des primären Servers kopiert werden.</span><span class="sxs-lookup"><span data-stu-id="7d241-123">A file share on the secondary database server to serve as the destination folder for the SQL Server transaction logs that are copied from the primary server file share.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7d241-124">Aktive beständige Chat Server in einem beständigen Chat Serverpool müssen sich in derselben Zeitzone befinden wie der lync-Pool für den nächsten Hop, der in der Topologie definiert ist.</span><span class="sxs-lookup"><span data-stu-id="7d241-124">Active Persistent Chat servers in a Persistent Chat Server pool MUST reside in the same time zone as the next hop Lync Pool defined in the topology.</span></span>



</div>

<span data-ttu-id="7d241-125">Die folgenden Abbildungen enthalten Beispiele dafür, wie der gesamte Server Pool für beständigen Chat in den beiden unterschiedlichen gedehnten Pool Topologien konfiguriert werden kann:</span><span class="sxs-lookup"><span data-stu-id="7d241-125">The following figures provide examples about how the entire Persistent Chat Server pool can be configured in the two different stretched pool topologies:</span></span>

  - <span data-ttu-id="7d241-126">Gedehnter beständiger Chat Server Pool, wenn Rechenzentren mit hoher Bandbreite/geringer Latenz geographisch lokalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="7d241-126">Stretched Persistent Chat Server pool when data centers are geo-located with high bandwidth/low latency.</span></span>

  - <span data-ttu-id="7d241-127">Gedehnter beständiger Chat Server Pool, wenn Rechenzentren mit niedriger Bandbreite/hoher Latenz geografischer Standort sind.</span><span class="sxs-lookup"><span data-stu-id="7d241-127">Stretched Persistent Chat Server pool when data centers are geo-located with low bandwidth/high latency.</span></span>

<span data-ttu-id="7d241-128">Die folgende Abbildung zeigt eine gedehnte Server Pooltopologie mit beständigem Chat, in der Rechenzentren mit hoher Bandbreite/geringer Latenz geographisch lokalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="7d241-128">The following figure shows a stretched Persistent Chat Server pool topology where data centers are geo-located with high bandwidth/low latency.</span></span>

<span data-ttu-id="7d241-129">**Gedehnter beständiger Chat Server Pool, wenn Rechenzentren mit hoher Bandbreite/geringer Latenz geographisch lokalisiert sind.**</span><span class="sxs-lookup"><span data-stu-id="7d241-129">**Stretched Persistent Chat Server pool when data centers are geo-located with high bandwidth/low latency.**</span></span>

<span data-ttu-id="7d241-130">![Beständiger Chat Server Pool HBW-Konfigurationsprüfung](images/JJ205211.55d10910-c824-41e6-bed2-08d13a2abd65(OCS.15).jpg "Beständiger Chat Server Pool HBW-Konfigurationsprüfung")</span><span class="sxs-lookup"><span data-stu-id="7d241-130">![Persistent Chat Server pool HBW configuration exam](images/JJ205211.55d10910-c824-41e6-bed2-08d13a2abd65(OCS.15).jpg "Persistent Chat Server pool HBW configuration exam")</span></span>

<span data-ttu-id="7d241-131">Die folgende Abbildung zeigt eine gedehnte Server Pooltopologie mit beständigem Chat, in der Rechenzentren mit niedriger Bandbreite/hoher Latenz geografisch lokalisiert sind.</span><span class="sxs-lookup"><span data-stu-id="7d241-131">The following figure shows a stretched Persistent Chat Server pool topology where data centers are geo-located with low bandwidth/high latency.</span></span>

<span data-ttu-id="7d241-132">**Gedehnter beständiger Chat Server Pool, wenn Rechenzentren mit niedriger Bandbreite/hoher Latenz geografischer Standort sind.**</span><span class="sxs-lookup"><span data-stu-id="7d241-132">**Stretched Persistent Chat Server pool when data centers are geo-located with low bandwidth/high latency.**</span></span>

<span data-ttu-id="7d241-133">![Beständiger Chat Server Pool LBW-Konfigurationsprüfung](images/JJ205211.586b0a3a-3767-4991-944f-ee54389512aa(OCS.15).jpg "Beständiger Chat Server Pool LBW-Konfigurationsprüfung")</span><span class="sxs-lookup"><span data-stu-id="7d241-133">![Persistent Chat Server pool LBW configuration exam](images/JJ205211.586b0a3a-3767-4991-944f-ee54389512aa(OCS.15).jpg "Persistent Chat Server pool LBW configuration exam")</span></span>

<span data-ttu-id="7d241-134"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7d241-134"></div>

<span> </span>

</div>

</div>

</span></span></div>

