---
title: 'Lync Server 2013: Einrichten von Systemplattformen'
description: 'Lync Server 2013: Einrichten von Systemplattformen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set up system platforms
ms:assetid: 2e72e49d-2737-4b5b-8c0a-60f6ecb15bf1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204783(v=OCS.15)
ms:contentKeyID: 48183756
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bd02c519d5632b7aa5732fbd9b880f7d1084b50f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423970"
---
# <a name="set-up-system-platforms-in-lync-server-2013"></a><span data-ttu-id="9c0e4-103">Einrichten von Systemplattformen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c0e4-103">Set up system platforms in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9c0e4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9c0e4-104">

<span> </span></span></span>

<span data-ttu-id="9c0e4-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="9c0e4-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="9c0e4-106">Bevor Sie die Bereitstellung des beständigen Chat Servers starten, müssen Sie das erforderliche Betriebssystem auf Hardware installieren, die den Systemanforderungen auf Servern entspricht:</span><span class="sxs-lookup"><span data-stu-id="9c0e4-106">Before starting the deployment of Persistent Chat Server, you must install the required operating system on hardware that meets system requirements on servers:</span></span>

<span data-ttu-id="9c0e4-107">Details zur unterstützten Hardware für Server mit lync Server 2013, Datenbankservern und Dateiservern finden Sie unter [Unterstützte Hardware für lync Server 2013](lync-server-2013-supported-hardware.md) in der Dokumentation zur Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-107">For details about supported hardware for servers running Lync Server 2013, database servers, and file servers, see [Supported hardware for Lync Server 2013](lync-server-2013-supported-hardware.md) in the Supportability documentation.</span></span> <span data-ttu-id="9c0e4-108">Ausführliche Informationen zu unterstützten Betriebssystemen und Datenbanksoftware finden Sie unter Unterstützung für [Server Software und-Infrastruktur in lync Server 2013](lync-server-2013-server-software-and-infrastructure-support.md) in der Dokumentation zur Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-108">For details about supported operating systems and database software, see [Server software and infrastructure support in Lync Server 2013](lync-server-2013-server-software-and-infrastructure-support.md) in the Supportability documentation.</span></span> <span data-ttu-id="9c0e4-109">Details zu den Windows Update-Anforderungen finden Sie unter [zusätzliche Server Unterstützung und-Anforderungen in lync Server 2013](lync-server-2013-additional-server-support-and-requirements.md) in der Dokumentation zur Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-109">For details about Windows update requirements, see [Additional server support and requirements in Lync Server 2013](lync-server-2013-additional-server-support-and-requirements.md) in the Supportability documentation.</span></span>

<span data-ttu-id="9c0e4-110">Der beständige Chat Server-Front-End-Server, **PersistentChatService**, kann auf einem oder mehreren eigenständigen Computern in einem lync Server 2013 Enterprise Edition-Pool bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-110">The Persistent Chat Server Front End Server, **PersistentChatService**, can be deployed on one or more stand-alone computers in a Lync Server 2013 Enterprise Edition pool.</span></span> <span data-ttu-id="9c0e4-111">Sie können nicht auf den lync Server Enterprise Edition-Front-End-Servern zusammengestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-111">They cannot be collocated on the Lync Server Enterprise Edition Front End Servers.</span></span> <span data-ttu-id="9c0e4-112">Der Server für beständigen Chat kann vom Bootstrapper bereitgestellt werden, genau wie andere lync-Serverrollen.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-112">Persistent Chat Server can be deployed by the Bootstrapper, just like other Lync Server roles.</span></span> <span data-ttu-id="9c0e4-113">Die **beständigen Chat-Webdienste für Datei Upload/-Download** und **beständige Chat-Webdienste für die chatroomverwaltung** sind Webkomponenten, die auf den lync Server 2013-Front-End-Servern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-113">The **Persistent Chat Web Services for File Upload/Download**, and **Persistent Chat Web Services for Chat Room Management** are web components deployed on the Lync Server 2013 Front End Servers.</span></span>

<span data-ttu-id="9c0e4-114">Ein einzelner beständiger Chat Server-Front-End-Server kann 20.000-aktive Benutzer unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-114">A single Persistent Chat Server Front End Server can support 20,000 active users.</span></span> <span data-ttu-id="9c0e4-115">Sie können einen Server Pool für beständigen Chat mit bis zu vier aktiven Front-Ends haben, der insgesamt 80.000 gleichzeitige Benutzer unterstützt.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-115">You can have a Persistent Chat Server pool with up to 4 active front ends supporting a total of 80,000 concurrent users.</span></span> <span data-ttu-id="9c0e4-116">Der beständige Chat-Back-End-Server, **PersistentChatStore**, speichert die Chatrooms und Kategorien.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-116">The Persistent Chat Back End Server, **PersistentChatStore**, stores the chat rooms and categories.</span></span> <span data-ttu-id="9c0e4-117">Wir empfehlen, die **PersistentChatStore** auf einem dedizierten SQL Server-Back-End-Server in Ihrem Enterprise Edition-Pool zu installieren. Obwohl wir abstimmen lync Server 2013-Back-End-Server und- **PersistentChatStore** auf derselben SQL Server-Instanz unterstützen.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-117">We recommend that you install the **PersistentChatStore** on a dedicated SQL Server Back End Server in your Enterprise Edition pool; although we support collocating Lync Server 2013 Back End Server and **PersistentChatStore** on the same SQL Server instance.</span></span>

<span data-ttu-id="9c0e4-118">Wenn Ihre Organisation Compliance-Unterstützung erfordert, können Sie Sie mithilfe des Topologie-Generators installieren.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-118">If your organization requires compliance support, you can install it by using Topology Builder.</span></span> <span data-ttu-id="9c0e4-119">Der beständige Chat Server-Kompatibilitätsdienst ist auf demselben Computer wie der Front-End-Server des beständigen Chat Servers installiert.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-119">The Persistent Chat Server Compliance service is installed on the same computer as the Persistent Chat Server Front End Server.</span></span> <span data-ttu-id="9c0e4-120">Für die Compliance ist eine separate Datenbank erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-120">A separate database is required for compliance.</span></span> <span data-ttu-id="9c0e4-121">Ausführliche Informationen zu den Konformitätsanforderungen für den Server für beständigen Chat finden Sie unter [Planen des beständigen Chat Servers in lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-121">For details about compliance requirements for Persistent Chat Server, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation.</span></span>

<span data-ttu-id="9c0e4-122">Für jede Topologie ist mindestens ein Server mit lync Server 2013 und ein Server mit installierter SQL Server-Datenbanksoftware erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-122">At a minimum, each topology requires a server with Lync Server 2013 installed and a server with SQL Server database software installed.</span></span> <span data-ttu-id="9c0e4-123">Der Topologie-Generator unterstützt mehrere beständige Chat Server Pools.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-123">Topology Builder supports multiple Persistent Chat Server pools.</span></span> <span data-ttu-id="9c0e4-124">Befolgen Sie die gleichen Bereitstellungsanweisungen für die Bereitstellung mehrerer beständiger Chat Server Pools wie für jeden Pool, wenn Sie [lync Server 2013](lync-server-2013-deploying-lync-server.md) in der Bereitstellungsdokumentation bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-124">Follow the same deployment instructions for deploying multiple Persistent Chat Server pools as you would for any pool from [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md) in the Deployment documentation.</span></span>

<span data-ttu-id="9c0e4-125">Sie können den Server für beständigen Chat auch mit lync Server 2013 Standard Edition bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-125">You can also deploy Persistent Chat Server with Lync Server 2013 Standard Edition.</span></span> <span data-ttu-id="9c0e4-126">In diesem Fall befindet sich der **PersistentChatService** -Front-End-Server auf dem Standard Edition-Server, und Sie können den **PersistentChatStore** -Back-End-Server auf der lokalen SQL Server Express-Instanz bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-126">In this case, the **PersistentChatService** Front End Server is collocated on the Standard Edition server, and you can deploy the **PersistentChatStore** Back End Server on the local SQL Server Express instance.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="9c0e4-127">Wir unterstützen keine persistent Chat Server &nbsp; Standard Edition für eine höhere Verfügbarkeit.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-127">We do not support Persistent Chat Server&nbsp;Standard Edition for high availability.</span></span> <span data-ttu-id="9c0e4-128">Leistung und Skalierung sind limitiert.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-128">Performance and scale will be limited.</span></span> <span data-ttu-id="9c0e4-129">Darüber hinaus unterstützen wir nur neue Server Bereitstellungen für beständigen Chat Server- &nbsp; Standard Editionen.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-129">Furthermore, we support only new Persistent Chat Server&nbsp;Standard Edition server deployments.</span></span> <span data-ttu-id="9c0e4-130">Wir unterstützen kein Upgrade von lync Server 2010, Gruppen-Chat Server auf eine lync Server 2013 &nbsp; persistent Chat Server &nbsp; Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="9c0e4-130">We do not support an upgrade of Lync Server 2010, Group Chat Server to a Lync Server 2013&nbsp;Persistent Chat Server&nbsp;Standard Edition.</span></span>



</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9c0e4-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9c0e4-131">See Also</span></span>


[<span data-ttu-id="9c0e4-132">Zusätzliche Serverunterstützung und Anforderungen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c0e4-132">Additional server support and requirements in Lync Server 2013</span></span>](lync-server-2013-additional-server-support-and-requirements.md)  


[<span data-ttu-id="9c0e4-133">Unterstützte Hardware für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c0e4-133">Supported hardware for Lync Server 2013</span></span>](lync-server-2013-supported-hardware.md)  
[<span data-ttu-id="9c0e4-134">Serversoftware- und Infrastrukturunterstützung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c0e4-134">Server software and infrastructure support in Lync Server 2013</span></span>](lync-server-2013-server-software-and-infrastructure-support.md)  
[<span data-ttu-id="9c0e4-135">Planen für den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c0e4-135">Planning for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-planning-for-persistent-chat-server.md)  
[<span data-ttu-id="9c0e4-136">Bereitstellen von Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c0e4-136">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)  
  

<span data-ttu-id="9c0e4-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9c0e4-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

