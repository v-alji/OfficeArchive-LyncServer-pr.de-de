---
title: 'Lync Server 2013: Unterstützte Datenbanksoftware'
description: Unterstützung der lync Server 2013-Datenbanksoftware.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Database software support
ms:assetid: e05d0032-bbea-4e61-987d-d07b1c045fd5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398990(v=OCS.15)
ms:contentKeyID: 48185517
ms.date: 12/02/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1c5d7b44e5febc4123dbcdf7072b98fcfd004609
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431225"
---
# <a name="database-software-support-in-lync-server-2013"></a><span data-ttu-id="87ad0-103">Unterstützte Datenbanksoftware in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="87ad0-103">Database software support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="87ad0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="87ad0-104">

<span> </span></span></span>

<span data-ttu-id="87ad0-105">_**Letztes Änderungsdatum des Themas:** 2014-12-01_</span><span class="sxs-lookup"><span data-stu-id="87ad0-105">_**Topic Last Modified:** 2014-12-01_</span></span>

<span data-ttu-id="87ad0-106">Lync Server 2013 unterstützt die folgenden Datenbank-Management Systeme:</span><span class="sxs-lookup"><span data-stu-id="87ad0-106">Lync Server 2013 supports the following database management systems:</span></span>

  - <span data-ttu-id="87ad0-107">**Back-End-Datenbank eines Front-End-Pools, Archivierungsdatenbank, Überwachungsdatenbank, Datenbank für beständigen Chat und Konformitätsdatenbank für beständigen Chat**</span><span class="sxs-lookup"><span data-stu-id="87ad0-107">**Back-end database of a Front End pool, Archiving database, Monitoring database, persistent chat database, and persistent chat compliance database**</span></span>
    
      - <span data-ttu-id="87ad0-p101">Microsoft SQL Server 2008 R2 Enterprise-Datenbanksoftware (64-Bit-Version). Darüber hinaus wird das neueste Service Pack empfohlen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-p101">Microsoft SQL Server 2008 R2 Enterprise database software (64-bit edition). Additionally running the latest service pack is recommended.</span></span>
    
      - <span data-ttu-id="87ad0-p102">Microsoft SQL Server 2008 R2 Standard (64-Bit-Version). Darüber hinaus wird das neueste Service Pack empfohlen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-p102">Microsoft SQL Server 2008 R2 Standard (64-bit edition). Additionally running the latest service pack is recommended.</span></span>
    
      - <span data-ttu-id="87ad0-p103">Microsoft SQL Server 2012 Enterprise (64-Bit-Version). Darüber hinaus wird das neueste Service Pack empfohlen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-p103">Microsoft SQL Server 2012 Enterprise (64-bit edition). Additionally running the latest service pack is recommended.</span></span>
    
      - <span data-ttu-id="87ad0-p104">Microsoft SQL Server 2012 Standard (64-Bit-Version). Darüber hinaus wird das neueste Service Pack empfohlen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-p104">Microsoft SQL Server 2012 Standard (64-bit edition). Additionally running the latest service pack is recommended.</span></span>

  - <span data-ttu-id="87ad0-116">**Standard Edition-Server Datenbank und Front-End-Server Datenbanken**</span><span class="sxs-lookup"><span data-stu-id="87ad0-116">**Standard Edition server database and Front End Server databases**</span></span>
    
      - <span data-ttu-id="87ad0-117">Microsoft SQL Server 2012 Express (64-Bit-Version).</span><span class="sxs-lookup"><span data-stu-id="87ad0-117">Microsoft SQL Server 2012 Express (64-bit edition).</span></span> <span data-ttu-id="87ad0-118">Darüber hinaus wird das neueste Service Pack empfohlen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-118">Additionally running the latest service pack is recommended.</span></span>
        
        <span data-ttu-id="87ad0-119">Wir unterstützen das Patchen und Aktualisieren von Microsoft SQL Server auf Front-End-Servern und Standard Edition-Servern.</span><span class="sxs-lookup"><span data-stu-id="87ad0-119">We support the patching and upgrade of Microsoft SQL Server on Front End Servers and Standard Edition servers.</span></span> <span data-ttu-id="87ad0-120">Wenn Sie jedoch auf Front-End-Servern jede Art von Upgrade oder Patch vornehmen, müssen Sie die Quorum Anforderungen berücksichtigen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-120">However, when you make any kind of upgrade or patch on Front End Servers, you must account for quorum requirements.</span></span> <span data-ttu-id="87ad0-121">Weitere Informationen finden Sie unter [Upgrade or update Front End Servers in Lync Server 2013](lync-server-2013-upgrade-or-update-front-end-servers.md) und [Topologies and components for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).</span><span class="sxs-lookup"><span data-stu-id="87ad0-121">For more information, see [Upgrade or update Front End Servers in Lync Server 2013](lync-server-2013-upgrade-or-update-front-end-servers.md) and [Topologies and components for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-topologies-and-components-for-front-end-servers-instant-messaging-and-presence.md).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="87ad0-122">Microsoft SQL Server 2012 Express (64-Bit Edition) wird von lync Server 2013 auf jedem Standard Edition-Server und jedem Front-End-Server automatisch installiert.</span><span class="sxs-lookup"><span data-stu-id="87ad0-122">Microsoft SQL Server 2012 Express (64-bit edition) is automatically installed by Lync Server 2013 on each Standard Edition server and each Front End Server server.</span></span>

    
    </div>

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="87ad0-123">Lync Server 2013 unterstützt nicht die 32-Bit-Edition von SQL Server.</span><span class="sxs-lookup"><span data-stu-id="87ad0-123">Lync Server 2013 does not support the 32-bit edition of SQL Server.</span></span> <span data-ttu-id="87ad0-124">Sie müssen die 64-Bit-Version verwenden.</span><span class="sxs-lookup"><span data-stu-id="87ad0-124">You must use the 64-bit edition.</span></span></P>
> <LI>
> <P><span data-ttu-id="87ad0-125">SQL Server Web Edition und SQL Server Arbeitsgruppe Edition werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="87ad0-125">SQL Server Web edition and SQL Server Workgroup edition are not supported.</span></span> <span data-ttu-id="87ad0-126">Sie können Sie nicht mit lync Server 2013 verwenden.</span><span class="sxs-lookup"><span data-stu-id="87ad0-126">You cannot use them with Lync Server 2013.</span></span></P>
> <LI>
> <P><span data-ttu-id="87ad0-127">Lync Server 2013 unterstützt die systemeigene Datenbankspiegelung.</span><span class="sxs-lookup"><span data-stu-id="87ad0-127">Lync Server 2013 does support native database mirroring.</span></span></P>
> <LI>
> <P><span data-ttu-id="87ad0-128">Wenn Sie die Monitoring Server-Rolle verwenden möchten, sollten Sie SQL Server Reporting Services installieren.</span><span class="sxs-lookup"><span data-stu-id="87ad0-128">To use the Monitoring Server role, you should install SQL Server Reporting Services.</span></span></P></LI></UL>



</div>

<span data-ttu-id="87ad0-129">In einem Front-End-Pool kann die Back-End-Datenbank ein einzelner SQL Server-Computer sein.</span><span class="sxs-lookup"><span data-stu-id="87ad0-129">In a Front End pool, the back-end database can be a single SQL Server computer.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="87ad0-130">Wenn Sie lync Server-Datenbanken mit anderen Datenbanken collocate, empfehlen wir dringend, alle Faktoren zu bewerten, die sich auf die Verfügbarkeit und Leistung auswirken können, und sicherzustellen, dass der verbleibende Knoten die Last verarbeiten kann, wenn ein Knoten fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="87ad0-130">If you collocate Lync Server databases with other databases, we highly recommend assessing all factors that might affect availability and performance, as well as ensuring that, if one node fails, the remaining node can handle the load.</span></span> <span data-ttu-id="87ad0-131">Zum Überprüfen von Failoverfunktionen empfiehlt es sich, alle Failover-Szenarien zu testen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-131">To verify failover capabilities, we recommend testing all failover scenarios.</span></span>



</div>

<div>

## <a name="using-sql-mirroring-and-sql-clustering"></a><span data-ttu-id="87ad0-132">Verwenden von SQL-Spiegelung und SQL-Clustering</span><span class="sxs-lookup"><span data-stu-id="87ad0-132">Using SQL Mirroring and SQL Clustering</span></span>

<span data-ttu-id="87ad0-133">Lync Server 2013 unterstützt die Verwendung von SQL-Spiegelung oder SQL-Clustering für jede lync Server-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="87ad0-133">Lync Server 2013 supports the use of either SQL mirroring or SQL clustering for each Lync Server database.</span></span> <span data-ttu-id="87ad0-134">Sie können die SQL-Spiegelung auf einfache Weise mit dem Tool Topologie-Generator in lync Server 2013 einrichten.</span><span class="sxs-lookup"><span data-stu-id="87ad0-134">You can easily set up SQL mirroring with the Topology Builder tool in Lync Server 2013.</span></span> <span data-ttu-id="87ad0-135">Zum Einrichten von SQL-Failoverclustering müssen Sie SQL Server verwenden.</span><span class="sxs-lookup"><span data-stu-id="87ad0-135">For SQL failover clustering, you must use SQL Server for setup.</span></span>

<span data-ttu-id="87ad0-136">Lync Server 2013 unterstützt sowohl SQL-Spiegelungs-als auch SQL-Cluster-Topologien für alle Bereitstellungen, einschließlich Greenfield-Bereitstellungen und Organisationen, die von früheren Versionen von lync Server aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="87ad0-136">Lync Server 2013 supports both SQL mirroring and SQL clustering topologies for all deployments, including greenfield deployments and organizations that have upgraded from previous versions of Lync Server.</span></span>

<span data-ttu-id="87ad0-p111">Die SQL-Clusteringunterstützung bezieht sich auf eine Aktiv/Passiv-Konfiguration. Aus Leistungsgründen sollte der passive Knoten von keiner anderen SQL-Instanz verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="87ad0-p111">SQL Clustering support is for an active/passive configuration. For performance reasons, the passive node should not be shared by any other SQL instance.</span></span>

<span data-ttu-id="87ad0-139">Die folgende Unterstützung wird geboten:</span><span class="sxs-lookup"><span data-stu-id="87ad0-139">The following support is included:</span></span>

  - <span data-ttu-id="87ad0-140">Zwei-Knoten-Failoverclustering für:</span><span class="sxs-lookup"><span data-stu-id="87ad0-140">Two-node failover clustering for the following:</span></span>
    
      - <span data-ttu-id="87ad0-p112">Microsoft SQL Server 2012 Standard (64-Bit-Version). Darüber hinaus wird das neueste Service Pack empfohlen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-p112">Microsoft SQL Server 2012 Standard (64-bit edition). Additionally running the latest service pack is recommended.</span></span>
    
      - <span data-ttu-id="87ad0-p113">Microsoft SQL Server 2008 R2 Standard (64-Bit-Version). Darüber hinaus wird das neueste Service Pack empfohlen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-p113">Microsoft SQL Server 2008 R2 Standard (64-bit edition). Additionally running the latest service pack is recommended.</span></span>

  - <span data-ttu-id="87ad0-145">Failoverclustering mit bis zu sechzehn Knoten für:</span><span class="sxs-lookup"><span data-stu-id="87ad0-145">Up to sixteen-node failover clustering for the following:</span></span>
    
      - <span data-ttu-id="87ad0-p114">Microsoft SQL Server 2012 Enterprise (64-Bit-Version). Darüber hinaus wird das neueste Service Pack empfohlen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-p114">Microsoft SQL Server 2012 Enterprise (64-bit edition). Additionally running the latest service pack is recommended.</span></span>
    
      - <span data-ttu-id="87ad0-p115">Microsoft SQL Server 2008 R2 Enterprise-Datenbanksoftware (64-Bit-Version). Darüber hinaus wird das neueste Service Pack empfohlen.</span><span class="sxs-lookup"><span data-stu-id="87ad0-p115">Microsoft SQL Server 2008 R2 Enterprise database software (64-bit edition). Additionally running the latest service pack is recommended.</span></span>

<span data-ttu-id="87ad0-150">Weitere Informationen zur SQL-Spiegelung finden Sie unter [Back-End-Server – höhere Verfügbarkeit in lync Server 2013](lync-server-2013-back-end-server-high-availability.md).</span><span class="sxs-lookup"><span data-stu-id="87ad0-150">For more information about SQL mirroring, see [Back End Server high availability in Lync Server 2013](lync-server-2013-back-end-server-high-availability.md).</span></span> <span data-ttu-id="87ad0-151">Details zum Bereitstellen von SQL-Clustering finden Sie unter [Konfigurieren des SQL Server-Clusters für lync Server 2013](lync-server-2013-configure-sql-server-clustering.md).</span><span class="sxs-lookup"><span data-stu-id="87ad0-151">For details on how to deploy SQL clustering, see [Configure SQL Server clustering for Lync Server 2013](lync-server-2013-configure-sql-server-clustering.md).</span></span>

<span data-ttu-id="87ad0-152">Weitere Informationen und bewährte Methoden für die Failover-Clusterunterstützung in SQL Server 2012 finden Sie unter <https://technet.microsoft.com/library/hh231721.aspx> .</span><span class="sxs-lookup"><span data-stu-id="87ad0-152">For more information and best practices for failover clustering in SQL Server 2012, see <https://technet.microsoft.com/library/hh231721.aspx>.</span></span> <span data-ttu-id="87ad0-153">Informationen zum Failover-Clustering in SQL Server 2008 finden Sie unter <https://technet.microsoft.com/library/ms189134(v=sql.105).aspx> .</span><span class="sxs-lookup"><span data-stu-id="87ad0-153">For failover clustering in SQL Server 2008, see <https://technet.microsoft.com/library/ms189134(v=sql.105).aspx>.</span></span>

<span data-ttu-id="87ad0-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="87ad0-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

