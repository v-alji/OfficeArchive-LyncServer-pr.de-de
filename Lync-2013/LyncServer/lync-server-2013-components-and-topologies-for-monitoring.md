---
title: 'Lync Server 2013: Komponenten und Topologien für die Überwachung'
description: 'Lync Server 2013: Komponenten und Topologien für die Überwachung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components and topologies for monitoring
ms:assetid: c1bb36b0-1fb8-4d8e-9cc9-9bef740fe3c6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412952(v=OCS.15)
ms:contentKeyID: 48185313
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8767a7eb16ca85e9606838606a6e86ee1296fc0e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434578"
---
# <a name="components-and-topologies-for-monitoring-in-lync-server-2013"></a><span data-ttu-id="10427-103">Komponenten und Topologien für die Überwachung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="10427-103">Components and topologies for monitoring in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="10427-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="10427-104">

<span> </span></span></span>

<span data-ttu-id="10427-105">_**Letztes Änderungsdatum des Themas:** 2012-09-05_</span><span class="sxs-lookup"><span data-stu-id="10427-105">_**Topic Last Modified:** 2012-09-05_</span></span>

<span data-ttu-id="10427-106">Da die Unified Data Collection-Agents automatisch auf jedem Front-End-Server installiert und aktiviert werden, müssen Sie keinen Server so konfigurieren, dass er als Monitoring Server fungiert. Jeder Front-End-Server fungiert bereits als Monitoring Server.</span><span class="sxs-lookup"><span data-stu-id="10427-106">Because the unified data collection agents are automatically installed and activated on each Front End server you do not need to configure a server to act as the Monitoring server; each Front End server already functions as a Monitoring server.</span></span> <span data-ttu-id="10427-107">Sie müssen jedoch eine Datenbank installieren und konfigurieren, damit Sie als Back-End-Datenspeicher für Ihre Überwachungsdaten fungieren kann.</span><span class="sxs-lookup"><span data-stu-id="10427-107">However, you will need to install and configure a database to act as the backend data store for your monitoring data.</span></span> <span data-ttu-id="10427-108">Microsoft lync Server 2013 kann eine der folgenden Datenbanken als Back-End-Speicher für die Überwachung verwenden:</span><span class="sxs-lookup"><span data-stu-id="10427-108">Microsoft Lync Server 2013 can use any of the following databases as the backend store for monitoring:</span></span>

  - <span data-ttu-id="10427-109">Microsoft SQL Server 2008 R2 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="10427-109">Microsoft SQL Server 2008 R2 Enterprise Edition</span></span>

  - <span data-ttu-id="10427-110">Microsoft SQL Server 2008 R2 Standard Edition</span><span class="sxs-lookup"><span data-stu-id="10427-110">Microsoft SQL Server 2008 R2 Standard Edition</span></span>

  - <span data-ttu-id="10427-111">Microsoft SQL Server 2012 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="10427-111">Microsoft SQL Server 2012 Enterprise Edition</span></span>

  - <span data-ttu-id="10427-112">Microsoft SQL Server 2012 Standard Edition</span><span class="sxs-lookup"><span data-stu-id="10427-112">Microsoft SQL Server 2012 Standard Edition</span></span>

<span data-ttu-id="10427-113">Beachten Sie, dass Sie die 64-Bit-Editionen dieser Datenbanken verwenden müssen. 32-Bit-Versionen von SQL Server können nicht als Back-End-Speicher zum Überwachen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="10427-113">Note that you must use the 64-bit editions of these databases; 32-bit versions of SQL Server cannot be used as the backend store for monitoring.</span></span> <span data-ttu-id="10427-114">Ebenso unterstützt lync Server 2013 die Express-Editionen von SQL Server 2008 oder SQL Server 2012 nicht.</span><span class="sxs-lookup"><span data-stu-id="10427-114">Likewise, Lync Server 2013 does not support the Express Editions of SQL Server 2008 or SQL Server 2012.</span></span> <span data-ttu-id="10427-115">Weitere Informationen zu den Datenbankanforderungen für lync Server 2013 finden Sie im Thema [Datenbanksoftware-Unterstützung in lync Server 2013](lync-server-2013-database-software-support.md) im lync Server 2013-Leitfaden zur Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="10427-115">For more information on database requirements for Lync Server 2013 see the topic [Database software support in Lync Server 2013](lync-server-2013-database-software-support.md) in the Lync Server 2013 Supportability guide.</span></span>

<span data-ttu-id="10427-116">Beachten Sie, dass SQL Server installiert und konfiguriert werden muss, bevor Sie die Überwachung bereitstellen und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="10427-116">Keep in mind that SQL Server must be installed and configured before you deploy and configure monitoring.</span></span> <span data-ttu-id="10427-117">Sie müssen jedoch nur SQL Server selbst bereitstellen. Sie müssen die Überwachungsdatenbanken nicht im Voraus einrichten.</span><span class="sxs-lookup"><span data-stu-id="10427-117">However, you only need to deploy SQL Server itself; you do not have to setup the monitoring databases in advance.</span></span> <span data-ttu-id="10427-118">Stattdessen werden diese Datenbankenautomatisch für Sie erstellt, wenn Sie Ihre lync Server-Topologie veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="10427-118">Instead, those databases will automatically be created for you when you publish your Lync Server topology.</span></span>

<span data-ttu-id="10427-p104">Überwachungsdaten können eine SQL Server-Instanz gemeinsam mit anderen Datentypen verwenden. In der Regel verwenden die Datenbank für die Aufzeichnung von Kommunikationsdatensätzen (LcsCdr) und die Quality of Experience-Datenbank (QoEMetrics) dieselbe SQL-Instanz. Häufig sind die beiden Überwachungsdatenbanken auch in derselben SQL-Instanz wie die Archivierungsdatenbank (LcsLog) vorhanden. Die einzige echte Anforderung für SQL Server-Instanzen besteht darin, dass jede Instanz von SQL Server auf Folgendes beschränkt ist:</span><span class="sxs-lookup"><span data-stu-id="10427-p104">Monitoring data can share a SQL Server instance with other types of data. Typically, the call detail recording database (LcsCdr) and the Quality of Experience database (QoEMetrics) share the same SQL instance; it is also common for the two monitoring databases to be in the same SQL instance as the archiving database (LcsLog). About the only real requirement with SQL Server instances is that any one instance of SQL Server is limited to the following:</span></span>

  - <span data-ttu-id="10427-122">Eine Instanz der lync Server 2013-Back-End-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="10427-122">One instance of the Lync Server 2013 backend database.</span></span> <span data-ttu-id="10427-123">(Im Allgemeinen wird davon abgeraten, die Überwachungsdatenbank in derselben SQL-Instanz oder sogar auf demselben Computer wie die Back-End-Datenbank zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="10427-123">(As a general rule, it is not recommended that your monitoring database be collocated in the same SQL instance, or even on the same computer, as the backend database.</span></span> <span data-ttu-id="10427-124">Dies ist zwar technisch möglich, aber es besteht das Risiko, dass die Überwachungsdatenbank Speicherplatz belegt, der für die Back-End-Datenbank benötigt wird.)</span><span class="sxs-lookup"><span data-stu-id="10427-124">Although technically possible, you run the risk of the monitoring database using up disk space needed by the backend database.)</span></span>

  - <span data-ttu-id="10427-125">Eine Instanz der Datenbank für die Aufzeichnung von Kommunikationsdatensätzen.</span><span class="sxs-lookup"><span data-stu-id="10427-125">One instance of the call detail recording database.</span></span>

  - <span data-ttu-id="10427-126">Eine Instanz der Quality of Experience-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="10427-126">One instance of the Quality of Experience database.</span></span>

  - <span data-ttu-id="10427-127">Eine Instanz der Archivierungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="10427-127">One instance of the archiving database.</span></span>

<span data-ttu-id="10427-128">Anders ausgedrückt: Sie können nicht zwei Instanzen der LcsCdr-Datenbank in der gleichen Instanz von SQL Server haben.</span><span class="sxs-lookup"><span data-stu-id="10427-128">In other words, you cannot have two instances of the LcsCdr database in the same instance of SQL Server.</span></span> <span data-ttu-id="10427-129">Wenn Sie mehrere Instanzen der LcsCdr-Datenbank benötigen, müssen Sie mehrere Instanzen von SQL Server konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="10427-129">If you need multiple instances of the LcsCdr database then you will need to configure multiple instances of SQL Server.</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="10427-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="10427-130">See Also</span></span>


[<span data-ttu-id="10427-131">Bereitstellen der Überwachung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="10427-131">Deploying monitoring in Lync Server 2013</span></span>](lync-server-2013-deploying-monitoring.md)  
  

<span data-ttu-id="10427-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="10427-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

