---
title: 'Lync Server 2013: Gemeinsames Ausführen von Servern in einer Standard Edition-Serverbereitstellung'
description: Lync Server 2013-Server Zusammenstellung in einer Standard Edition-Server Bereitstellung.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server collocation in a Standard Edition server deployment
ms:assetid: 0763ffab-4fd6-463a-8e62-d97876b376d3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398131(v=OCS.15)
ms:contentKeyID: 48183314
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af44761d36c472de1a3da5cd3b3938dc1a130836
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441893"
---
# <a name="server-collocation-in-a-standard-edition-server-deployment-for-lync-server-2013"></a><span data-ttu-id="379ca-103">Gemeinsames Ausführen von Servern in einer Standard Edition-Serverbereitstellung für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="379ca-103">Server collocation in a Standard Edition server deployment for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="379ca-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="379ca-104">

<span> </span></span></span>

<span data-ttu-id="379ca-105">_**Letztes Änderungsdatum des Themas:** 2013-01-20_</span><span class="sxs-lookup"><span data-stu-id="379ca-105">_**Topic Last Modified:** 2013-01-20_</span></span>

<span data-ttu-id="379ca-106">In diesem Abschnitt werden die Serverrollen, Datenbanken und Dateifreigaben beschrieben, die Sie in einer lync Server 2013 Standard Edition-Server Bereitstellung collocate können.</span><span class="sxs-lookup"><span data-stu-id="379ca-106">This section describes the server roles, databases, and file shares that you can collocate in a Lync Server 2013 Standard Edition server deployment.</span></span>

<div>

## <a name="server-roles"></a><span data-ttu-id="379ca-107">Server Rollen</span><span class="sxs-lookup"><span data-stu-id="379ca-107">Server Roles</span></span>

<span data-ttu-id="379ca-108">In lync Server 2013 sind A/V-Konferenzdienst, Mediationsdienst, Überwachung und Archivierung auf dem Standard Edition-Server verfügbar, es ist jedoch eine zusätzliche Konfiguration erforderlich, um Sie zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="379ca-108">In Lync Server 2013, A/V Conferencing service, Mediation service, Monitoring, and Archiving are collocated on the Standard Edition Server, but additional configuration is required to enable them.</span></span> <span data-ttu-id="379ca-109">Sie können den Vermittlungsdienst auf separaten Servern bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="379ca-109">You can choose to deploy Mediation service on separate servers.</span></span>

<span data-ttu-id="379ca-110">Sie können einen vertrauenswürdigen Anwendungsserver mit einem Standard Edition-Server collocate.</span><span class="sxs-lookup"><span data-stu-id="379ca-110">You can collocate a trusted application server with a Standard Edition server.</span></span>

<span data-ttu-id="379ca-111">Die folgenden Serverrollen müssen jeweils auf einem separaten Computer bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="379ca-111">The following server roles must each be deployed on a separate computer:</span></span>

  - <span data-ttu-id="379ca-112">Director</span><span class="sxs-lookup"><span data-stu-id="379ca-112">Director</span></span>

  - <span data-ttu-id="379ca-113">Edgeserver</span><span class="sxs-lookup"><span data-stu-id="379ca-113">Edge Server</span></span>

  - <span data-ttu-id="379ca-114">Vermittlungsserver (wenn Sie nicht mit dem Standard Edition-Server ausgestattet sind)</span><span class="sxs-lookup"><span data-stu-id="379ca-114">Mediation Server (if not collocated with the Standard Edition server)</span></span>

  - <span data-ttu-id="379ca-115">Office Web Apps-Server</span><span class="sxs-lookup"><span data-stu-id="379ca-115">Office Web Apps Server</span></span>

</div>

<div>

## <a name="databases"></a><span data-ttu-id="379ca-116">Datenbanken</span><span class="sxs-lookup"><span data-stu-id="379ca-116">Databases</span></span>

<span data-ttu-id="379ca-117">Standardmäßig befindet sich die SQL Server Express-Back-End-Datenbank auf dem Standard Edition-Server.</span><span class="sxs-lookup"><span data-stu-id="379ca-117">By default, the SQL Server Express back-end database is collocated on the Standard Edition server.</span></span> <span data-ttu-id="379ca-118">Sie können Sie nicht auf einen anderen Computer verschieben.</span><span class="sxs-lookup"><span data-stu-id="379ca-118">You cannot move it to a separate computer.</span></span> <span data-ttu-id="379ca-119">Mit einer Ausnahme können Sie keine anderen Datenbanken auf dem Standard Edition-Server collocate.</span><span class="sxs-lookup"><span data-stu-id="379ca-119">With one exception, you cannot collocate other databases on the Standard Edition server.</span></span> <span data-ttu-id="379ca-120">Wenn Sie den Server für beständigen Chat auf einem Standard Edition-Server bereitstellen möchten, können Sie die Datenbank für beständigen Chat und die Compliance-Datenbank für beständigen Chat auf demselben Standard Edition-Server collocate.</span><span class="sxs-lookup"><span data-stu-id="379ca-120">If you choose to deploy Persistent Chat Server on a Standard Edition server, you can collocate the Persistent chat database and the Persistent Chat Compliance database on the same Standard Edition server.</span></span>

<span data-ttu-id="379ca-121">Sie können jede der folgenden Datenbanken auf einem einzelnen Datenbankserver collocate:</span><span class="sxs-lookup"><span data-stu-id="379ca-121">You can collocate each of the following databases on a single database server:</span></span>

  - <span data-ttu-id="379ca-122">Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="379ca-122">Monitoring database</span></span>

  - <span data-ttu-id="379ca-123">Archivierungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="379ca-123">Archiving database</span></span>

  - <span data-ttu-id="379ca-124">Eine Back-End-Datenbank für einen Enterprise Edition-Front-End-Pool</span><span class="sxs-lookup"><span data-stu-id="379ca-124">A back-end database for an Enterprise Edition Front End pool</span></span>

<span data-ttu-id="379ca-125">Sie können eine beliebige oder eine beliebige oder alle dieser Datenbanken in einer einzelnen SQL-Instanz collocate oder für jede einzelne SQL-Instanzen verwenden, wobei die folgenden Einschränkungen gelten:</span><span class="sxs-lookup"><span data-stu-id="379ca-125">You can collocate any or any or all of these databases in a single SQL instance or use a separate SQL instances for each, with the following limitations:</span></span>

  - <span data-ttu-id="379ca-126">Jede SQL-Instanz kann nur eine einzige Back-End-Datenbank (für einen Enterprise Edition-Front-End-Pool), eine einzige Überwachungsdatenbank, eine einzelne Archivierungsdatenbank, eine einzelne persistent Chat-Datenbank und eine einzelne beständige Chat-Kompatibilitätsdatenbank enthalten.</span><span class="sxs-lookup"><span data-stu-id="379ca-126">Each SQL instance can contain only a single back-end database (for an Enterprise Edition Front End pool), single Monitoring database, single Archiving database, single persistent chat database, and single persistent chat compliance database.</span></span>

  - <span data-ttu-id="379ca-127">Der Datenbankserver kann nicht mehr als einen Enterprise Edition-Front-End-Pool, einen Server, auf dem die Archivierung ausgeführt wird, einen Server mit Überwachung, eine einzige persistente Chat-Datenbank und eine einzelne beständige Chat-Kompatibilitätsdatenbank unterstützen, doch er kann einen der beiden unterstützen, unabhängig davon, ob die Datenbanken dieselbe Instanz von SQL Server oder separate Instanzen von</span><span class="sxs-lookup"><span data-stu-id="379ca-127">The database server cannot support more than one Enterprise Edition Front End pool, one server running Archiving, one server running Monitoring, single Persistent Chat database, and single Persistent Chat compliance database, but it can support one of each, regardless of whether the databases use the same instance of SQL Server or separate instances of SQL Server.</span></span>

<span data-ttu-id="379ca-128">Sie können eine Dateifreigabe für die Datenbanken collocate, wie weiter unten in diesem Abschnitt beschrieben.</span><span class="sxs-lookup"><span data-stu-id="379ca-128">You can collocate a file share with the databases, as described later in this section.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="379ca-129">In lync Server 2013 haben Sie die Möglichkeit, den Überwachungs-und Archivierungsspeicher mit Exchange 2013-Speicher für einige oder alle Benutzer in Ihrer Bereitstellung zu integrieren.</span><span class="sxs-lookup"><span data-stu-id="379ca-129">In Lync Server 2013, you have the option of integrating Monitoring and Archiving storage with Exchange 2013 storage for some or all users in your deployment.</span></span> <span data-ttu-id="379ca-130">Sie können keine Server mit lync Server oder Komponenten auf denselben Servern wie dem Exchange-Speicher bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="379ca-130">You cannot deploy any servers running Lync Server or components on the same servers as the Exchange storage.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="379ca-131">Obwohl die Daten Bank Zusammenstellung unterstützt wird, kann die Größe der Datenbanken schnell zunehmen.</span><span class="sxs-lookup"><span data-stu-id="379ca-131">Although collocation of databases is supported, the size of the databases can grow quickly.</span></span> <span data-ttu-id="379ca-132">Wenn Sie beispielsweise die Archivierungsdatenbank mit anderen Datenbanken abstimmen, beachten Sie Folgendes: Wenn Sie die Nachrichten von mehr als wenigen Benutzern archivieren, kann der von der Archivierungsdatenbank benötigte Speicherplatz sehr groß werden.</span><span class="sxs-lookup"><span data-stu-id="379ca-132">For example, when you consider collocating the Archiving database with other databases, be aware that if you are archiving the messages of more than a few users, the disk space needed by the Archiving database can grow very large.</span></span> <span data-ttu-id="379ca-133">Aus diesem Grund raten wir davon ab, abstimmen mehrere Datenbanken, insbesondere die Archivierungsdatenbank, die persistente Chat-Datenbank und die beständige Chat-Kompatibilitätsdatenbank, mit der Back-End-Datenbank eines Enterprise-Pools zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="379ca-133">For this reason, we do not recommend collocating multiple databases, especially the Archiving database, Persistent Chat database, and Persistent Chat compliance database with the back-end database of an Enterprise pool.</span></span>



</div>

</div>

<div>

## <a name="file-shares"></a><span data-ttu-id="379ca-134">Dateifreigaben</span><span class="sxs-lookup"><span data-stu-id="379ca-134">File Shares</span></span>

<span data-ttu-id="379ca-135">Die Dateifreigabe kann ein separater Server sein oder sich auf dem gleichen Server wie die folgenden befinden:</span><span class="sxs-lookup"><span data-stu-id="379ca-135">The file share can be a separate server or can be collocated on the same server as any or all of the following:</span></span>

  - <span data-ttu-id="379ca-136">Datenbankserver, einschließlich des Back-End-Servers eines Enterprise Edition-Front-End-Pools</span><span class="sxs-lookup"><span data-stu-id="379ca-136">Database server, including the Back End Server of an Enterprise Edition Front End pool</span></span>

  - <span data-ttu-id="379ca-137">Archivierungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="379ca-137">Archiving database</span></span>

  - <span data-ttu-id="379ca-138">Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="379ca-138">Monitoring database</span></span>

  - <span data-ttu-id="379ca-139">Datenbank für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="379ca-139">Persistent Chat database</span></span>

  - <span data-ttu-id="379ca-140">Kompatibilitätsdatenbank für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="379ca-140">Persistent Chat compliance database</span></span>

<span data-ttu-id="379ca-141">Eine einzelne Dateifreigabe kann für mehrere Front-End-Pools, Standard Edition-Server (alle auf der gleichen Website), verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="379ca-141">A single file share can be used for multiple Front End pools, Standard Edition servers (all in the same site).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="379ca-142">In lync Server 2013 verwenden die Überwachung und Archivierung die lync Server-Dateifreigabe als Standard Edition-Server.</span><span class="sxs-lookup"><span data-stu-id="379ca-142">In Lync Server 2013, Monitoring and Archiving use the Lync Server file share as the Standard Edition server.</span></span>



</div>

</div>

<div>

## <a name="other-components"></a><span data-ttu-id="379ca-143">Andere Komponenten</span><span class="sxs-lookup"><span data-stu-id="379ca-143">Other Components</span></span>

<span data-ttu-id="379ca-144">Sie können keinen Reverseproxy-Server collocate, bei dem es sich nicht um eine lync Server 2013-Komponente handelt, aber für Ihre Bereitstellung erforderlich ist, wenn Sie die Freigabe von Webinhalten für Verbundbenutzer mit einer beliebigen lync Server 2013-Serverrolle unterstützen möchten.</span><span class="sxs-lookup"><span data-stu-id="379ca-144">You cannot collocate a reverse proxy server, which is not a Lync Server 2013 component, but is required in your deployment if you want to support sharing of web content for federated users with any Lync Server 2013 server role.</span></span> <span data-ttu-id="379ca-145">Sie können jedoch eine Reverse-Proxy-Unterstützung für eine lync Server 2013-Bereitstellung implementieren, indem Sie die Unterstützung für einen vorhandenen Reverse-Proxy Server in Ihrer Organisation konfigurieren, der für andere Anwendungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="379ca-145">You can, however, implement reverse proxy support for a Lync Server 2013 deployment by configuring the support on an existing reverse proxy server in your organization that is used for other applications.</span></span>

<span data-ttu-id="379ca-146">Sie können keine Exchange um-Komponente oder SharePoint-Komponente mit einer lync Server 2013-Rolle collocate.</span><span class="sxs-lookup"><span data-stu-id="379ca-146">You cannot collocate any Exchange UM component or SharePoint component with any Lync Server 2013 role.</span></span>

<span data-ttu-id="379ca-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="379ca-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

