---
title: 'Lync Server 2013: Bereitstellen des Servers für beständigen Chat'
description: 'Lync Server 2013: Bereitstellen des beständigen Chat Servers'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Persistent Chat Server
ms:assetid: e3b930fb-6855-47f0-b6b3-7dfae386540d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205357(v=OCS.15)
ms:contentKeyID: 48185717
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b85c0070ab4bcd60d80d57738c25daac1de4faf1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429811"
---
# <a name="deploying-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="dc18f-103">Bereitstellen des Servers für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc18f-103">Deploying Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dc18f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dc18f-104">

<span> </span></span></span>

<span data-ttu-id="dc18f-105">_**Letztes Änderungsdatum des Themas:** 2014-03-31_</span><span class="sxs-lookup"><span data-stu-id="dc18f-105">_**Topic Last Modified:** 2014-03-31_</span></span>

<span data-ttu-id="dc18f-106">Lync Server 2013, beständiger Chat Server ist Teil der lync Server 2013-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="dc18f-106">Lync Server 2013, Persistent Chat Server is part of the Lync Server 2013 infrastructure.</span></span>

<span data-ttu-id="dc18f-107">Für die Bereitstellung des beständigen Chat Servers müssen Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="dc18f-107">Deploying Persistent Chat Server requires that you:</span></span>

  - <span data-ttu-id="dc18f-108">Verwenden Sie den Topologie-Generator, um Ihre Topologie und die Komponenten, die Sie bereitstellen möchten, zu definieren, zu importieren und anschließend zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="dc18f-108">Use Topology Builder to define, or import, and subsequently publish your topology and the components that you want to deploy.</span></span>

  - <span data-ttu-id="dc18f-109">Bereiten Sie Ihre Umgebung für die Bereitstellung beständiger Chat Server Komponenten vor.</span><span class="sxs-lookup"><span data-stu-id="dc18f-109">Prepare your environment for deploying Persistent Chat Server components.</span></span>

  - <span data-ttu-id="dc18f-110">Installieren und konfigurieren Sie Komponenten für beständigen Chat Server für Ihre Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="dc18f-110">Install and configure Persistent Chat Server components for your deployment.</span></span>

<span data-ttu-id="dc18f-111">Der Server für beständigen Chat steht in lync Server 2013 Enterprise Edition als separater Pool zur Verfügung (nicht mit den Enterprise Edition-Front-End-Servern).</span><span class="sxs-lookup"><span data-stu-id="dc18f-111">Persistent Chat Server is available with Lync Server 2013 Enterprise Edition as a separate pool (not collocated with the Enterprise Edition Front End Servers).</span></span> <span data-ttu-id="dc18f-112">Der Server für beständigen Chat erfordert einen SQL Server-Back-End-Server in Ihrem Enterprise Edition-Pool, um den Chatroom-Inhalt und andere relevante Metadaten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="dc18f-112">Persistent Chat Server requires a SQL Server Back End Server in your Enterprise Edition pool to store the chat room content and other relevant metadata.</span></span> <span data-ttu-id="dc18f-113">Wir empfehlen, dass Sie die **PersistentChatStore** auf einem dedizierten SQL Server-Back-End-Server installieren, obwohl abstimmen lync Server 2013-Back-End-Server und **PersistentChatStore** auf derselben SQL Server-Instanz unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="dc18f-113">We recommend that you install the **PersistentChatStore** on a dedicated SQL Server Back End Server, although collocating Lync Server 2013 Back End Server and **PersistentChatStore** on the same SQL Server instance is supported.</span></span>

<span data-ttu-id="dc18f-114">Der Server für beständigen Chat kann auch mit lync Server 2013 Standard Edition bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="dc18f-114">Persistent Chat Server can also be deployed with Lync Server 2013 Standard Edition.</span></span> <span data-ttu-id="dc18f-115">In diesem Fall befindet sich der **PersistentChatService** -Front-End-Server auf dem Standard Edition-Computer, und der **PersistentChatStore** -Back-End-Server kann auf der lokalen SQL Server Express-Instanz bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="dc18f-115">In this case, the **PersistentChatService** Front End Server is collocated on the Standard Edition computer, and the **PersistentChatStore** Back End Server can be deployed on the local SQL Server Express instance.</span></span>

<span data-ttu-id="dc18f-116">Ausführliche Informationen zu unterstützten Colocation-Konfigurationen finden Sie unter [unterstützte Server setzungen in lync Server 2013](lync-server-2013-supported-server-collocation.md).</span><span class="sxs-lookup"><span data-stu-id="dc18f-116">For details about supported colocation configurations, see [Supported server collocation in Lync Server 2013](lync-server-2013-supported-server-collocation.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="dc18f-117">Wir unterstützen keine höhere Verfügbarkeit für die Standard Edition für beständigen Chat Server &nbsp; .</span><span class="sxs-lookup"><span data-stu-id="dc18f-117">We do not support high availability for Persistent Chat Server&nbsp;Standard Edition.</span></span> <span data-ttu-id="dc18f-118">Leistung und Skalierung sind limitiert.</span><span class="sxs-lookup"><span data-stu-id="dc18f-118">Performance and scale will be limited.</span></span> <span data-ttu-id="dc18f-119">Darüber hinaus unterstützen wir nur den neuen Server für beständigen Chat Server &nbsp; Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="dc18f-119">Furthermore, we support only new Persistent Chat Server&nbsp;Standard Edition server.</span></span> <span data-ttu-id="dc18f-120">Wir unterstützen nicht das Upgrade von lync Server 2010, Gruppen-Chat Server auf eine lync Server 2013 &nbsp; persistent Chat Server &nbsp; Standard Edition.</span><span class="sxs-lookup"><span data-stu-id="dc18f-120">We do not support upgrading Lync Server 2010, Group Chat Server to a Lync Server 2013&nbsp;Persistent Chat Server&nbsp;Standard Edition.</span></span>



</div>

<span data-ttu-id="dc18f-121">Wenn Ihre Organisation Compliance-Unterstützung erfordert, können Sie den beständigen Chat Server-Kompatibilitätsdienst auf dem Front-End-Server für beständigen Chat Server installieren.</span><span class="sxs-lookup"><span data-stu-id="dc18f-121">If your organization requires compliance support, you can install the Persistent Chat Server Compliance service on the Persistent Chat Server Front End Server.</span></span> <span data-ttu-id="dc18f-122">Für die Compliance ist eine separate Datenbank erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dc18f-122">A separate database is required for compliance.</span></span>

<span data-ttu-id="dc18f-123">Für jede Topologie ist mindestens ein Server mit lync Server 2013 und ein Server mit installierter SQL Server-Datenbanksoftware erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dc18f-123">At a minimum, each topology requires a server with Lync Server 2013 installed and a server with SQL Server database software installed.</span></span>

<span data-ttu-id="dc18f-124">Verwenden Sie den Topologie-Generator, um ihrer lync Server 2013-Bereitstellung beständigen Chat Server hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="dc18f-124">Use Topology Builder to add Persistent Chat Server to your Lync Server 2013 deployments.</span></span> <span data-ttu-id="dc18f-125">Mithilfe des Topologie-Generators können Sie einen oder mehrere beständige Chat Server Pools hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="dc18f-125">You can choose to add one or more Persistent Chat Server pools using Topology Builder.</span></span> <span data-ttu-id="dc18f-126">Befolgen Sie dieselben Bereitstellungsanweisungen für die Bereitstellung mehrerer beständiger Chat Server Pools, wie Sie dies für jeden Pool tun würden.</span><span class="sxs-lookup"><span data-stu-id="dc18f-126">Follow the same deployment instructions for deploying multiple Persistent Chat Server pools as you would for any pool.</span></span> <span data-ttu-id="dc18f-127">Ausführliche Informationen finden Sie unter [Bereitstellen von lync Server 2013](lync-server-2013-deploying-lync-server.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="dc18f-127">For details, see [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md) in the Deployment documentation.</span></span>

<span data-ttu-id="dc18f-128">Details zu verfügbaren Topologien sowie zu den technischen und Softwareanforderungen für die Installation von persistent Chat Server finden Sie unter [Planen des beständigen Chat Servers in lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in der Planungsdokumentation, [Funktionsweise des beständigen Chat 2013 Servers](lync-server-2013-how-persistent-chat-server-works.md) in der Planning-Dokumentation, Bereitstellungsdokumentation oder Betriebsdokumentation sowie [Unterstützte Hardware für lync Server 2013](lync-server-2013-supported-hardware.md) in der Dokumentation zur Unterstützung.</span><span class="sxs-lookup"><span data-stu-id="dc18f-128">For details about available topologies and the technical and software requirements for installing Persistent Chat Server, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation, [How Persistent Chat Server works in Lync Server 2013](lync-server-2013-how-persistent-chat-server-works.md) in the Planning documentation, Deployment documentation, or Operations documentation, and [Supported hardware for Lync Server 2013](lync-server-2013-supported-hardware.md) in the Supportability documentation.</span></span>

<span data-ttu-id="dc18f-129">Details zum Abrufen von Zertifikaten, zum Erstellen der SQL Server-Datenbank und zum Erstellen von Datei speichern finden Sie unter [Bereitstellen von lync Server 2013](lync-server-2013-deploying-lync-server.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="dc18f-129">For details about acquiring certificates, creating the SQL Server database, and creating file stores, see [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md) in the Deployment documentation.</span></span>

<span data-ttu-id="dc18f-130">Ein einzelner beständiger Chat Server-Front-End-Server kann 20.000-aktive Benutzer unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dc18f-130">A single Persistent Chat Server Front End Server can support 20,000 active users.</span></span> <span data-ttu-id="dc18f-131">Sie können einen Server Pool für beständigen Chat mit bis zu vier aktiven Front-End-Servern mit insgesamt 80.000 gleichzeitigen Benutzern unterstützen.</span><span class="sxs-lookup"><span data-stu-id="dc18f-131">You can have a Persistent Chat Server pool with up to 4 active Front End Servers supporting a total of 80,000 concurrent users.</span></span>

<span data-ttu-id="dc18f-132">Der Server für beständigen Chat wird auch auf einem virtuellen Server unterstützt.</span><span class="sxs-lookup"><span data-stu-id="dc18f-132">Persistent Chat Server is also supported on a virtual server.</span></span> <span data-ttu-id="dc18f-133">Der virtuelle Server kann bis zu 20.000 gleichzeitige Benutzer unterstützen, wenn er den Spezifikationen des physikalischen Servers entspricht.</span><span class="sxs-lookup"><span data-stu-id="dc18f-133">The virtual server can support up to 20,000 concurrent users if it matches the specifications of the physical server.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="dc18f-134">Der Server für beständigen Chat muss auf einem NTFS-Dateisystem installiert sein, um die Dateisystemsicherheit zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="dc18f-134">Persistent Chat Server must be installed on an NTFS file system to help enforce file system security.</span></span> <span data-ttu-id="dc18f-135">FAT32 ist kein unterstütztes Dateisystem für beständigen Chat Server.</span><span class="sxs-lookup"><span data-stu-id="dc18f-135">FAT32 is not a supported file system for Persistent Chat Server.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="dc18f-136">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="dc18f-136">In This Section</span></span>

  - [<span data-ttu-id="dc18f-137">Funktionsweise des beständigen Chat Servers in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc18f-137">How Persistent Chat Server works in Lync Server 2013</span></span>](lync-server-2013-how-persistent-chat-server-works.md)

  - [<span data-ttu-id="dc18f-138">Prüfliste zur Bereitstellung für den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc18f-138">Deployment checklist for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-persistent-chat-server.md)

  - [<span data-ttu-id="dc18f-139">Technische Anforderungen für den Server für beständigen Chat in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc18f-139">Technical requirements for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-persistent-chat-server.md)

  - [<span data-ttu-id="dc18f-140">Einrichten der Systeme und Infrastruktur für den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc18f-140">Setting up systems and infrastructure for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-setting-up-systems-and-infrastructure-for-persistent-chat-server.md)

  - [<span data-ttu-id="dc18f-141">Hinzufügen eines Servers für beständigen Chat zu einer Bereitstellung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc18f-141">Adding Persistent Chat Server to your deployment in Lync Server 2013</span></span>](lync-server-2013-adding-persistent-chat-server-to-your-deployment.md)

  - [<span data-ttu-id="dc18f-142">Installieren des Servers für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc18f-142">Installing Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-installing-persistent-chat-server.md)

  - [<span data-ttu-id="dc18f-143">Hinzufügen eines Administrators für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc18f-143">Adding a Persistent Chat administrator in Lync Server 2013</span></span>](lync-server-2013-adding-a-persistent-chat-administrator.md)

  - [<span data-ttu-id="dc18f-144">Konfigurieren des Servers für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc18f-144">Configuring Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-configuring-persistent-chat-server.md)

  - [<span data-ttu-id="dc18f-145">Konfigurieren des Servers für beständigen Chat mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="dc18f-145">Configuring Persistent Chat Server by using Windows PowerShell cmdlets</span></span>](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md)

  - [<span data-ttu-id="dc18f-146">Problembehandlung bei der Konfiguration des Servers für beständigen Chat mithilfe von Windows PowerShell-Cmdlets in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc18f-146">Troubleshooting Persistent Chat Server configuration using Windows PowerShell cmdlets in Lync Server 2013</span></span>](lync-server-2013-troubleshooting-persistent-chat-server-configuration-using-windows-powershell-cmdlets.md)

  - [<span data-ttu-id="dc18f-147">Konfigurieren der hohen Verfügbarkeit und der Notfallwiederherstellung für den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc18f-147">Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md)

  - [<span data-ttu-id="dc18f-148">Ausführen eines Failovers bzw. Failbacks für den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc18f-148">Failing over and failing back Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-failing-over-and-failing-back-persistent-chat-server.md)

<span data-ttu-id="dc18f-149"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dc18f-149"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

