---
title: 'Lync Server 2013: Neue Funktionen für den Server für beständigen Chat'
description: 'Lync Server 2013: neue Funktionen für beständigen Chat Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New Persistent Chat Server features
ms:assetid: c3ec6f33-6261-4bf5-aa31-baa8ab2a87d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412965(v=OCS.15)
ms:contentKeyID: 48185341
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 549fa43e115467c373fe8df08f8568aa8715c29d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445351"
---
# <a name="new-persistent-chat-server-features-in-lync-server-2013"></a><span data-ttu-id="39eb2-103">Neue Funktionen für den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39eb2-103">New Persistent Chat Server features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39eb2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39eb2-104">

<span> </span></span></span>

<span data-ttu-id="39eb2-105">_**Letztes Änderungsdatum des Themas:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="39eb2-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="39eb2-106">Lync Server 2013, beständiger Chat Server ermöglicht Ihnen, an mehrteiligen, themenbasierten Konversationen teilzunehmen, die im Laufe der Zeit fortbestehen.</span><span class="sxs-lookup"><span data-stu-id="39eb2-106">Lync Server 2013, Persistent Chat Server enables you to participate in multiparty, topic-based conversations that persist over time.</span></span> <span data-ttu-id="39eb2-107">Der beständige Chat Server kann Ihrer Organisation helfen, Folgendes zu tun:</span><span class="sxs-lookup"><span data-stu-id="39eb2-107">Persistent Chat Server can help your organization do the following:</span></span>

  - <span data-ttu-id="39eb2-108">Verbessern der Kommunikation zwischen geografisch verteilten und funktionsübergreifenden Teams</span><span class="sxs-lookup"><span data-stu-id="39eb2-108">Improve communication between geographically dispersed and cross-functional teams</span></span>

  - <span data-ttu-id="39eb2-109">Erweitern des Informations Bewusstseins und der Teilnahme</span><span class="sxs-lookup"><span data-stu-id="39eb2-109">Broaden information awareness and participation</span></span>

  - <span data-ttu-id="39eb2-110">Verbessern der Kommunikation mit ihrer erweiterten Organisation</span><span class="sxs-lookup"><span data-stu-id="39eb2-110">Improve communication with your extended organization</span></span>

  - <span data-ttu-id="39eb2-111">Reduzieren der Informationsüberlastung</span><span class="sxs-lookup"><span data-stu-id="39eb2-111">Reduce information overload</span></span>

  - <span data-ttu-id="39eb2-112">Verbessern des Informations Bewusstseins</span><span class="sxs-lookup"><span data-stu-id="39eb2-112">Improve information awareness</span></span>

  - <span data-ttu-id="39eb2-113">Verbessern der Verbreitung wichtiger Kenntnisse und Informationen</span><span class="sxs-lookup"><span data-stu-id="39eb2-113">Increase dispersion of important knowledge and information</span></span>

<span data-ttu-id="39eb2-114">Lync Server 2013, beständiger Chat Server steht in Microsoft 365 oder Office 365 nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="39eb2-114">Lync Server 2013, Persistent Chat Server is not available in Microsoft 365 or Office 365.</span></span> <span data-ttu-id="39eb2-115">Zu diesem Zeitpunkt steht er nur für lokale lync 2013-Kunden zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="39eb2-115">At this time, it is available only to on-premise Lync 2013 customers.</span></span>

<span data-ttu-id="39eb2-116">In lync 2013 ist die Funktionalität des beständigen Chats in den lync 2013-Client integriert.</span><span class="sxs-lookup"><span data-stu-id="39eb2-116">In Lync 2013, Persistent Chat functionality is integrated into the Lync 2013 client.</span></span> <span data-ttu-id="39eb2-117">Daher haben Benutzer Zugriff auf Instant Messaging/Anwesenheit, Audio/Video, Konferenzen und beständigen Chat alle im lync 2013-Client.</span><span class="sxs-lookup"><span data-stu-id="39eb2-117">As a result, users have access to Instant Messaging/Presence, Audio/Video, Conferencing, and Persistent Chat all in the Lync 2013 client.</span></span> <span data-ttu-id="39eb2-118">Weitere Informationen zum lync 2013-Client finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=270877> .</span><span class="sxs-lookup"><span data-stu-id="39eb2-118">For more information about the Lync 2013 client, see <https://go.microsoft.com/fwlink/p/?linkid=270877>.</span></span>

<span data-ttu-id="39eb2-119">In diesem Thema werden die Funktionsänderungen zwischen der neuen Version von lync Server 2013, dem beständigen Chat Server und der vorherigen Version (Microsoft lync Server 2010, Gruppen Chat) beschrieben, einschließlich:</span><span class="sxs-lookup"><span data-stu-id="39eb2-119">This topic describes feature changes between the new version of Lync Server 2013, Persistent Chat Server and the previous version (Microsoft Lync Server 2010, Group Chat), including:</span></span>

  - <span data-ttu-id="39eb2-120">Bereitstelleneiner administrativen Funktionalität in der lync Server-Systemsteuerung und eliminieren des Administrator Tools für Gruppenchats</span><span class="sxs-lookup"><span data-stu-id="39eb2-120">Provide an administrative experience in Lync Server Control Panel, and eliminate the Group Chat Admin Tool</span></span>

  - <span data-ttu-id="39eb2-121">Integrieren von Konfigurationseinstellungen für beständigen Chat Server in den Topologie-Generator durch Eliminierung des Gruppen-Chat-Konfigurationstools</span><span class="sxs-lookup"><span data-stu-id="39eb2-121">Integrate configuration settings for Persistent Chat Server into Topology Builder by eliminating the Group Chat Configuration tool</span></span>

  - <span data-ttu-id="39eb2-122">Einfache Migration und Upgrade von vorherigen Versionen des beständigen Chat Servers</span><span class="sxs-lookup"><span data-stu-id="39eb2-122">Ease migration and upgrade from previous versions of Persistent Chat Server</span></span>

  - <span data-ttu-id="39eb2-123">Bereitstellen von Hochverfügbarkeits-und Disaster Recovery-Lösungen</span><span class="sxs-lookup"><span data-stu-id="39eb2-123">Provide high availability and disaster recovery solutions</span></span>

<span data-ttu-id="39eb2-124">Weitere Informationen zur neuesten Version des beständigen Chat Servers finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="39eb2-124">For additional details about the latest version of Persistent Chat Server, see the following:</span></span>

  - <span data-ttu-id="39eb2-125">In der Hilfe für beständigen Chat <https://go.microsoft.com/fwlink/p/?linkid=270945> finden Sie eine detaillierte Liste der beständigen Chat Features, ihre Funktionsweise und ihre Verwendung während des beständigen Chat Servers.</span><span class="sxs-lookup"><span data-stu-id="39eb2-125">The Persistent Chat Help at <https://go.microsoft.com/fwlink/p/?linkid=270945> which provides a detailed list of Persistent Chat features, how they work, and how to use them while running Persistent Chat Server.</span></span>

  - <span data-ttu-id="39eb2-126">Der [Server für die Planung des beständigen Chats in lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in der Planungsdokumentation [Bereitstellen des beständigen Chat Servers in lync Server 2013](lync-server-2013-deploying-persistent-chat-server.md) in der Bereitstellungsdokumentation, [Migration von lync Server 2010, Gruppen-Chat oder Office Communications Server 2007 R2-Gruppenchat zu lync Server 2013, beständiger Chat Server](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md) in der Migrationsdokumentation und [Verwalten von lync Server 2013, beständiger Chat Server](managing-lync-server-2013-persistent-chat-server.md) in der Betriebsdokumentation, die alle Anweisungen zum Einrichten des beständigen Chat Servers bieten</span><span class="sxs-lookup"><span data-stu-id="39eb2-126">The [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in the Planning documentation, [Deploying Persistent Chat Server in Lync Server 2013](lync-server-2013-deploying-persistent-chat-server.md) in the Deployment documentation, [Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md) in the Migration documentation, and [Managing Lync Server 2013, Persistent Chat Server](managing-lync-server-2013-persistent-chat-server.md) in the Operations documentation, all of which provide instructions for setting up Persistent Chat Server.</span></span>

  - <span data-ttu-id="39eb2-127">Der beständige Chat Server Documentation.msi-Datei (Windows Installer-Datei) ermöglicht Benutzern den Zugriff auf eine umfassende offlinedokumentation zu beständigen Chatservern.</span><span class="sxs-lookup"><span data-stu-id="39eb2-127">The Persistent Chat Server Documentation.msi file (Windows Installer file) lets users access comprehensive offline documentation about Persistent Chat Server.</span></span>

<div>

## <a name="key-topology-changes-for-persistent-chat-server"></a><span data-ttu-id="39eb2-128">Änderungen an wichtigen Topologien für beständigen Chat Server</span><span class="sxs-lookup"><span data-stu-id="39eb2-128">Key Topology Changes for Persistent Chat Server</span></span>

<span data-ttu-id="39eb2-129">Die folgenden allgemeinen Änderungen für beständigen Chat Server sind:</span><span class="sxs-lookup"><span data-stu-id="39eb2-129">The following high-level changes for Persistent Chat Server include:</span></span>

<span data-ttu-id="39eb2-130">Der beständige Chat Server ist nun eine Serverrolle.</span><span class="sxs-lookup"><span data-stu-id="39eb2-130">Persistent Chat Server is now a server role.</span></span> <span data-ttu-id="39eb2-131">In Microsoft lync Server 2010 war der Gruppen-Chat Server eine vertrauenswürdige Anwendung eines Drittanbieters für Microsoft lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="39eb2-131">In Microsoft Lync Server 2010, Group Chat Server was a third-party trusted application for Microsoft Lync Server 2010.</span></span> <span data-ttu-id="39eb2-132">Beständiger Chat kann ihrer lync Server 2013-Topologie mithilfe des Topologie-Generators hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="39eb2-132">Persistent Chat can be added to your Lync Server 2013 topology by using Topology Builder.</span></span> <span data-ttu-id="39eb2-133">In lync Server 2013 wird die Funktion des beständigen Chat Servers mithilfe von drei neuen Serverrollen implementiert:</span><span class="sxs-lookup"><span data-stu-id="39eb2-133">In Lync Server 2013, Persistent Chat Server functionality is implemented by using three new server roles:</span></span>

  - <span data-ttu-id="39eb2-134">**PersistentChatService:** Dies ist die Front-End-Rolle für beständigen Chat.</span><span class="sxs-lookup"><span data-stu-id="39eb2-134">**PersistentChatService:** This is the front end role for Persistent Chat.</span></span> <span data-ttu-id="39eb2-135">In Standard Edition-Bereitstellungen wird die Server Dienst Rolle des beständigen Chats auf dem Standard Edition-Server, der von Bootstrapper bereitgestellt wird, wie jede andere lync-Serverrolle verwendet.</span><span class="sxs-lookup"><span data-stu-id="39eb2-135">In Standard Edition deployments, Persistent Chat Server Service Role is collocated on the Standard Edition server deployed by Bootstrapper, like any other Lync Server role.</span></span> <span data-ttu-id="39eb2-136">In Enterprise Edition-Bereitstellungen wird die Funktion des beständigen Chats auf eigenständigen Computern nach Bootstrapper wie jede andere lync-Server Rolle bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="39eb2-136">In Enterprise Edition deployments, Persistent Chat Service Role is deployed on stand-alone computers by Bootstrapper, like any other Lync Server role.</span></span>

  - <span data-ttu-id="39eb2-137">**PersistentChatStore:** Back-End-Server, der der Inhaltsdatenbank für beständigen Chat entspricht, in der alle Chatinhalte gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="39eb2-137">**PersistentChatStore:** Back End Server that corresponds to the Persistent Chat content database, where all the chat content is stored.</span></span>

  - <span data-ttu-id="39eb2-138">**PersistentChatComplianceStore:** Back-End-Server Rolle, die der Compliance-Datenbank für beständigen Chat entspricht, in der alle Compliance-Ereignisse gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="39eb2-138">**PersistentChatComplianceStore:** Back End Server role that corresponds to the Persistent Chat Compliance database, where all compliance events are stored.</span></span>

<span data-ttu-id="39eb2-139">Diese Serverrollen für beständigen Chat sind optional und werden nur von Kunden installiert, die umfassende Funktionen für den beständigen Chat Server wünschen.</span><span class="sxs-lookup"><span data-stu-id="39eb2-139">These Persistent Chat Server roles are optional, and are installed only by customers who want comprehensive Persistent Chat Server functionality.</span></span> <span data-ttu-id="39eb2-140">Die Rolle **PersistentChatComplianceStore** ist nur erforderlich, wenn Sie die Compliance für beständigen Chat bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="39eb2-140">The **PersistentChatComplianceStore** role is needed only if you choose to deploy Persistent Chat Compliance.</span></span>

<span data-ttu-id="39eb2-141">Die **PersistentChatService** -Rolle führt zwei Dienste aus:</span><span class="sxs-lookup"><span data-stu-id="39eb2-141">The **PersistentChatService** role runs two services:</span></span>

  - <span data-ttu-id="39eb2-142">Beständiger Chat Dienst</span><span class="sxs-lookup"><span data-stu-id="39eb2-142">Persistent Chat service</span></span>

  - <span data-ttu-id="39eb2-143">Kompatibilitätsdienst für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="39eb2-143">Persistent Chat Compliance service</span></span>

<span data-ttu-id="39eb2-144">Wenn diese Dienste auf jedem beständigen Chat Server ausgeführt werden, bietet diese Dienste in einem persistenten Chat Serverpool eine höhere Verfügbarkeit.</span><span class="sxs-lookup"><span data-stu-id="39eb2-144">Having these services run on each Persistent Chat Server provides high availability for these services in a multiserver Persistent Chat Server pool.</span></span>

<span data-ttu-id="39eb2-145">Um den Dateiupload und-Download in beständige Chatrooms zu unterstützen, enthält der beständige Chat Server zudem einen Webdienst.</span><span class="sxs-lookup"><span data-stu-id="39eb2-145">Additionally, to support the file upload and download in Persistent Chat rooms, Persistent Chat Server includes a web service.</span></span> <span data-ttu-id="39eb2-146">Zuvor war dieser Dienst auf dem Server für beständigen Chat, dem Front-End-Server und den erforderlichen Internet Informationsdiensten (IIS) installiert, um als Voraussetzung zu installieren.</span><span class="sxs-lookup"><span data-stu-id="39eb2-146">Previously, this service was collocated on the Persistent Chat Server, Front End Server and required Internet Information Services (IIS) to be installed as a prerequisite.</span></span> <span data-ttu-id="39eb2-147">Im lync Server 2013-Server für beständigen Chat befindet sich der Web Servicedatei Upload/-Download mit dem lync Server 2013-Front-End-Server.</span><span class="sxs-lookup"><span data-stu-id="39eb2-147">In Lync Server 2013 Persistent Chat Server, the File Upload/Download web service is collocated with the Lync Server 2013 Front End Server.</span></span> <span data-ttu-id="39eb2-148">Als Nebeneffekt ist Internet Information Services (IIS) nicht mehr eine Voraussetzung für beständigen Chat Server.</span><span class="sxs-lookup"><span data-stu-id="39eb2-148">As a side effect, Internet Information Services (IIS) is no longer a prerequisite for Persistent Chat Server.</span></span> <span data-ttu-id="39eb2-149">Der Webdienst für Datei Upload/-Download wird im Internet Informationsdienste (IIS)-Manager als **PersistentChat** identifiziert.</span><span class="sxs-lookup"><span data-stu-id="39eb2-149">The File Upload/Download web service is identified as **PersistentChat** in the Internet Information Services (IIS) Manager.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="39eb2-150">Die <STRONG>PersistentChatService</STRONG> -Rolle kann nur auf dem gleichen Server wie ein lync Server 2013 &nbsp; -Front-End-Server ausgeführt werden, wenn der Front-End-Server ein Standard Edition &nbsp; -Front-End-Server ist.</span><span class="sxs-lookup"><span data-stu-id="39eb2-150">The <STRONG>PersistentChatService</STRONG> role can run on the same server as a Lync Server 2013&nbsp;Front End Server only if that Front End Server is a Standard Edition&nbsp;Front End Server.</span></span> <span data-ttu-id="39eb2-151">Die <STRONG>PersistentChatService</STRONG> -Rolle kann nicht unabhängig von einem lync Server 2013 &nbsp; -Front-End-Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="39eb2-151">The <STRONG>PersistentChatService</STRONG> role cannot run independently of a Lync Server 2013&nbsp;Front End Server.</span></span> <span data-ttu-id="39eb2-152">Sie kann nur im Kontext einer lync Server 2013-Bereitstellung installiert werden.</span><span class="sxs-lookup"><span data-stu-id="39eb2-152">It can be installed only in the context of a Lync Server 2013 deployment.</span></span>



</div>

<span data-ttu-id="39eb2-153">Im beständigen Chat Server wurde der Suchdienst eliminiert.</span><span class="sxs-lookup"><span data-stu-id="39eb2-153">In Persistent Chat Server, Lookup service has been eliminated.</span></span> <span data-ttu-id="39eb2-154">In lync Server 2010, Gruppen-Chat, wurde der Nachschlage Dienst auf jedem Front-End-Server des Gruppen-Chat Servers ausgeführt und auf einen der Kanalserver geroutet.</span><span class="sxs-lookup"><span data-stu-id="39eb2-154">In Lync Server 2010, Group Chat, the Lookup service ran on every Group Chat Server Front End Server, and performed routing to one of the Channel Servers.</span></span> <span data-ttu-id="39eb2-155">Lync Server 2013 basiert auf dem Routing mithilfe von Kontaktobjekten, wobei jeder beständige Chat Serverpool durch ein Kontaktobjekt dargestellt wird, das von den lync Server-Front-End-Servern verwendet wird, um Anforderungen zu identifizieren und an einen entsprechenden beständigen Chat Serverpool weiterzuleiten, und an einen der Computer, auf dem der beständige Chat Server im Pool ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39eb2-155">Lync Server 2013 relies on routing by using contact objects, where each Persistent Chat Server pool is represented by a contact object that is used by the Lync Server Front End Servers to identify and route requests to an appropriate Persistent Chat Server pool, and to one of the computers running Persistent Chat Server in the pool.</span></span>

<span data-ttu-id="39eb2-156">In lync Server 2013 sind Kompatibilitätsdienst Änderungen vorhanden:</span><span class="sxs-lookup"><span data-stu-id="39eb2-156">In Lync Server 2013, there are Compliance service modifications:</span></span>

  - <span data-ttu-id="39eb2-157">In lync Server 2010 wurde der Kompatibilitätsdienst eigenständig (nicht in der Lage) und nur auf einem einzelnen Server ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="39eb2-157">In Lync Server 2010, the Compliance service ran stand-alone (non-collocated), and only on a single server.</span></span> <span data-ttu-id="39eb2-158">Der Kompatibilitätsdienst wird nun neben dem beständigen Chatdienst auf allen Front-End-Servern des beständigen Chats ausgeführt und bietet dadurch eine höhere Verfügbarkeit in einem persistenten Chat Serverpool.</span><span class="sxs-lookup"><span data-stu-id="39eb2-158">The Compliance service now runs on all the Persistent Chat Server Front End Servers, alongside the Persistent Chat service, and thereby provides high availability in a multiserver Persistent Chat Server pool.</span></span> <span data-ttu-id="39eb2-159">Ein einzelner Kompatibilitätsadapter kann so konfiguriert werden, dass Daten aus der Kompatibilitätsdatenbank und einem anderen System (XML-Datei, Exchange-gehostete Archive usw.) extrahiert werden.</span><span class="sxs-lookup"><span data-stu-id="39eb2-159">A single compliance adapter can be configured to extract data from the compliance database and into one of the other systems (XML file, Exchange-hosted archives, and so on).</span></span> <span data-ttu-id="39eb2-160">Der beständige Chat Server enthält einen XML-Adapter.</span><span class="sxs-lookup"><span data-stu-id="39eb2-160">Persistent Chat Server includes an XML adapter.</span></span>

  - <span data-ttu-id="39eb2-161">Die Warteschlange für Message Queuing (auch als MSMQ bezeichnet), die vom beständigen Chatdienst und dem Kompatibilitätsdienst auf jedem beständigen Chat Server-Front-End-Server freigegeben wird, ist jetzt eine private Warteschlange, die nur von den beiden Diensten freigegeben wird.</span><span class="sxs-lookup"><span data-stu-id="39eb2-161">The Message Queuing (also known as MSMQ) queue that is shared by the Persistent Chat service and the Compliance service on each Persistent Chat Server Front End Server is now a private queue shared only by the two services.</span></span> <span data-ttu-id="39eb2-162">Alle Konformitäts Dienste schreiben in dieselbe Compliance-Back-End-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="39eb2-162">All compliance services write to the same Compliance Back End database.</span></span> <span data-ttu-id="39eb2-163">Sie haben auch alle aus dieser Datenbank gelesen, um die Daten an Ihre Instanz des Adapters zu senden.</span><span class="sxs-lookup"><span data-stu-id="39eb2-163">They also all read from that database, for the purpose of sending the data to their instance of the adapter.</span></span> <span data-ttu-id="39eb2-164">Der Compliance-Back-End-Server wird als neue Back-End-Serverrolle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="39eb2-164">The Compliance Back End Server is represented as a new Back End Server role.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="39eb2-165">Wie in früheren Versionen werden alle Kompatibilitätsdaten nur einmal verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="39eb2-165">As in previous versions, all compliance data is processed only once.</span></span> <span data-ttu-id="39eb2-166">Die Daten können von allen Adapter Instanzen verarbeitet werden, die vom Kompatibilitätsdienst aufgerufen werden, der auf den verschiedenen lync Server 2013-, persistent Chat Server-Computern ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39eb2-166">The data may be processed by any of the adapter instances invoked by the compliance service running on the various Lync Server 2013, Persistent Chat Server computers.</span></span> <span data-ttu-id="39eb2-167">In einem beständigen Chat Server können alle Adapter Instanzen die Daten verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="39eb2-167">In Persistent Chat Server, any one of the adapter instances could process the data.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="39eb2-168">Informationen zum Installieren von Message Queuing finden Sie unter <A href="lync-server-2013-install-operating-systems-and-prerequisite-software-on-servers.md">Installieren von Betriebssystemen und der erforderlichen Software auf Servern für lync Server 2013</A> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="39eb2-168">For information about installing Message Queuing, see <A href="lync-server-2013-install-operating-systems-and-prerequisite-software-on-servers.md">Install operating systems and prerequisite software on servers for Lync Server 2013</A> in the Deployment documentation.</span></span>

    
    </div>

<span data-ttu-id="39eb2-169">In lync Server 2013 gibt es Verbesserungen bei der Hochverfügbarkeits-und Disaster Recovery:</span><span class="sxs-lookup"><span data-stu-id="39eb2-169">In Lync Server 2013, there are improvements in both high availability and disaster recovery:</span></span>

  - <span data-ttu-id="39eb2-170">Verbesserungen bei hoher Verfügbarkeit: die SQL Server-Spiegelung wird verwendet, um eine höhere Verfügbarkeit für die Inhaltsdatenbank des beständigen Chat Servers und die Datenbank für beständigen Chat in einem Rechenzentrum (in-Site) bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="39eb2-170">High availability improvements: SQL Server mirroring is used to provide high availability for the Persistent Chat Server content database and Persistent Chat compliance database within a data center (in-site).</span></span>

  - <span data-ttu-id="39eb2-171">Verbesserungen bei der Disaster Recovery: der beständige Chat Server unterstützt eine ausgestreckte Pool Architektur, die es ermöglicht, einen einzelnen beständigen Chat Serverpool über zwei Standorte (also einen einzelnen logischen Pool in der Topologie) zu dehnen, wobei sich die Server im Pool physisch über zwei Standorte befinden.</span><span class="sxs-lookup"><span data-stu-id="39eb2-171">Disaster recovery improvements: Persistent Chat Server supports a stretched pool architecture that enables a single Persistent Chat Server pool to be stretched across two sites (that is, a single logical pool in the topology, with servers in the pool physically located across two sites).</span></span> <span data-ttu-id="39eb2-172">Der SQL Server-Protokollversand wird für die websiteübergreifende Notfallwiederherstellung verwendet.</span><span class="sxs-lookup"><span data-stu-id="39eb2-172">SQL Server Log Shipping is used for cross-site disaster recovery.</span></span>

<span data-ttu-id="39eb2-173">Weitere Informationen zu Hochverfügbarkeits-und Disaster Recovery finden Sie unter [Konfigurieren des beständigen Chat Servers für Hochverfügbarkeits-und Disaster Recovery in lync Server 2013](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="39eb2-173">For more information about high availability and disaster recovery, see [Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md) in the Deployment documentation.</span></span>

</div>

<div>

## <a name="key-administration-and-management-changes-for-persistent-chat-server"></a><span data-ttu-id="39eb2-174">Wichtige Änderungen bei der Verwaltung und Verwaltung für beständigen Chat Server</span><span class="sxs-lookup"><span data-stu-id="39eb2-174">Key Administration and Management Changes for Persistent Chat Server</span></span>

<span data-ttu-id="39eb2-175">Lync Server 2013 hat das Verwalten und Verwalten von beständigen Chat Servern vereinfacht, indem Sie Folgendes bereitgestellt haben:</span><span class="sxs-lookup"><span data-stu-id="39eb2-175">Lync Server 2013 has made it easier to administer and manage Persistent Chat Server by providing:</span></span>

  - <span data-ttu-id="39eb2-176">Einheitliche Verwaltung und Verwaltung</span><span class="sxs-lookup"><span data-stu-id="39eb2-176">Unified administration and management.</span></span> <span data-ttu-id="39eb2-177">Lync Server 2013 vereinfacht das Verwalten und Verwalten des beständigen Chat Servers mithilfe von Tools, die lync-Administratoren bereits vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="39eb2-177">Lync Server 2013 makes it easier to manage and administer Persistent Chat Server by using tools that are already familiar to Lync administrators.</span></span> <span data-ttu-id="39eb2-178">Der Server für beständigen Chat umfasst eine Benutzeroberflächen-Administratoroberfläche, die in die lync Server-Systemsteuerung integriert ist und Leistungsprobleme mit den vorherigen Versionen der Benutzeroberfläche des Gruppen-Chat Servers behebt.</span><span class="sxs-lookup"><span data-stu-id="39eb2-178">Persistent Chat Server includes an administrative user interface experience that is integrated with the Lync Server Control Panel, which addresses performance issues with the previous versions of the Group Chat Server user interface.</span></span> <span data-ttu-id="39eb2-179">Darüber hinaus enthält der Server für beständigen Chat eine Sammlung von Windows PowerShell-Cmdlets zum Verwalten und verwalten beständiger Chat Server Kategorien, beständiger Chatrooms (einschließlich Löschen von Räumen und bereinigen veralteter Inhalte) sowie Add-Ins.</span><span class="sxs-lookup"><span data-stu-id="39eb2-179">Also, Persistent Chat Server includes a collection of Windows PowerShell cmdlets to administer and manage Persistent Chat Server categories, Persistent Chat Server rooms (including deleting rooms and purging obsolete content), and add-ins.</span></span>

  - <span data-ttu-id="39eb2-180">Vereinfachtes Verwaltungsmodell</span><span class="sxs-lookup"><span data-stu-id="39eb2-180">Simplified administration model.</span></span> <span data-ttu-id="39eb2-181">Lync Server 2013 hat das Server Modell für beständigen Chat geändert und vereinfacht, indem es die folgenden wichtigen Kundenanforderungen erfüllt:</span><span class="sxs-lookup"><span data-stu-id="39eb2-181">Lync Server 2013 has changed and simplified the Persistent Chat Server model by addressing the following key customer requirements:</span></span>
    
      - <span data-ttu-id="39eb2-182">Entfernen Sie die komplexen geschachtelten Hierarchien von Bereichen und Kategorien.</span><span class="sxs-lookup"><span data-stu-id="39eb2-182">Remove the complex nested hierarchies of scopes and categories.</span></span>
    
      - <span data-ttu-id="39eb2-183">Unterstützung zum Definieren von Verweigerungslisten sowie zulässiger Listen (Bereiche) für aktuelle MindAlign-Kunden, die beabsichtigen, zum Server für beständigen Chat zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="39eb2-183">Support to define deny lists as well as allowed lists (scopes) for current MindAlign customers who are planning to migrate to Persistent Chat Server.</span></span>

</div>

<div>

## <a name="whats-different-about-user-roles-from-previous-group-chat-server-versions"></a><span data-ttu-id="39eb2-184">Worin unterscheiden sich die Benutzerrollen aus früheren Gruppen-Chat Server Versionen?</span><span class="sxs-lookup"><span data-stu-id="39eb2-184">What’s Different about User Roles from Previous Group Chat Server Versions?</span></span>

<span data-ttu-id="39eb2-185">Lync Server 2010, Gruppen-Chat hatte eine Benutzeradministratorrolle, eine Chatroom-Administratorrolle und eine lync Server-Administratorrolle, die Add-Ins verwalten konnte. Der Server für beständigen Chat stellt einfach eine Administrator Rolle für beständigen Chat bereit (ähnlich wie bei anderen rollenbasierten Zugriffssteuerungsfunktionen (Role-Based Access Control, RBAC)).</span><span class="sxs-lookup"><span data-stu-id="39eb2-185">Lync Server 2010, Group Chat had a user administrator role, a chat room administrator role and a Lync Server administrator role that could manage add-ins. Persistent Chat Server simply provides a Persistent Chat Administrator role (which is similar to other Lync Server role-based access control (RBAC) roles).</span></span> <span data-ttu-id="39eb2-186">Jeder, der Mitglied dieser RBAC-Rolle ist, kann Chatrooms, Add-Ins und Kategorien verwalten (und dadurch den Benutzer Zugriff für diese Kategorien gewinnen) und die Konfiguration des beständigen Chat Server Pools.</span><span class="sxs-lookup"><span data-stu-id="39eb2-186">Anyone who is a member of this RBAC role can manage chat rooms, add-ins, and categories (and therefore gain user access for these categories), and configuration of the Persistent Chat Server pool.</span></span>

</div>

<div>

## <a name="whats-different-about-chat-room-categories-from-previous-group-chat-server-versions"></a><span data-ttu-id="39eb2-187">Welche Unterschiede gibt es zu Chatroom-Kategorien aus früheren Gruppen-Chat Server Versionen?</span><span class="sxs-lookup"><span data-stu-id="39eb2-187">What’s Different about Chat Room Categories from Previous Group Chat Server Versions?</span></span>

<span data-ttu-id="39eb2-188">Chatroom-Kategorien können nicht mehr geschachtelt werden, und die Stammkategorie kann nicht mehr geändert werden.</span><span class="sxs-lookup"><span data-stu-id="39eb2-188">Chat room categories can no longer be nested, and the root category can no longer be modified.</span></span> <span data-ttu-id="39eb2-189">AllowedMembers/DeniedMembers enthalten einen Bereich, der in Legacy Gruppen-Chat Server Versionen verwendet wurde (mit der Ausnahme, dass die Angabe einer verweigerten Liste nicht unterstützt wurde).</span><span class="sxs-lookup"><span data-stu-id="39eb2-189">AllowedMembers/DeniedMembers comprise what a scope used to be in legacy Group Chat Server versions (except that it didn’t support specifying a Denied list).</span></span> <span data-ttu-id="39eb2-190">Bereiche können nicht mehr überschrieben werden, da es keine geschachtelten Kategorien gibt.</span><span class="sxs-lookup"><span data-stu-id="39eb2-190">Scopes can no longer be overridden, because there are no nested categories.</span></span> <span data-ttu-id="39eb2-191">Ein Administrator für beständigen Chat in lync Server 2013 kann Chatroom-Kategorien erstellen und verwalten.</span><span class="sxs-lookup"><span data-stu-id="39eb2-191">A Persistent Chat Administrator in Lync Server 2013 can create and manage chat room categories.</span></span> <span data-ttu-id="39eb2-192">Im Rahmen des Erstellens und Verwaltens von Chatroom-Kategorien kann ein beständiger Chat-Administrator Prinzipale (Active Directory-Gruppen/-Container/-Benutzer) konfigurieren, die Zugriff auf Mitglieder/Ersteller von Chatrooms einer bestimmten Kategorie haben.</span><span class="sxs-lookup"><span data-stu-id="39eb2-192">As part of creating and managing chat room categories, a Persistent Chat Administrator can configure principals (Active Directory groups/containers/users) that have access to be members/creators of chat rooms of a particular category.</span></span> <span data-ttu-id="39eb2-193">Ein Administrator des beständigen Chats kann auch DeniedMembers zu einer Kategorie hinzufügen, und diese werden explizite Ausnahmen für die zulässige Liste.</span><span class="sxs-lookup"><span data-stu-id="39eb2-193">A Persistent Chat Administrator can also add DeniedMembers to a category, and these become explicit exclusions to the allowed list.</span></span> <span data-ttu-id="39eb2-194">Einträge unter „DeniedMembers“ haben Vorrang vor Einträgen unter „AllowedMembers“.</span><span class="sxs-lookup"><span data-stu-id="39eb2-194">DeniedMembers override what’s in AllowedMembers.</span></span>

</div>

<div>

## <a name="whats-different-about-chat-room-properties-from-previous-group-chat-server-versions"></a><span data-ttu-id="39eb2-195">Was unterscheidet sich von den Chatroom-Eigenschaften aus früheren Gruppen-Chat Server Versionen?</span><span class="sxs-lookup"><span data-stu-id="39eb2-195">What’s Different about Chat Room Properties from Previous Group Chat Server Versions?</span></span>

<span data-ttu-id="39eb2-196">Ein neues Konzept offener Chatrooms ist in lync Server 2013, beständiger Chat Server, vorhanden.</span><span class="sxs-lookup"><span data-stu-id="39eb2-196">A new concept of open chat rooms exists in Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="39eb2-197">Alle zulässigen Mitglieder können dem Chatroom beitreten, ohne eine exklusive Mitgliedschaft zu haben.</span><span class="sxs-lookup"><span data-stu-id="39eb2-197">All allowed members can join the chat room, without exclusive membership.</span></span>

<span data-ttu-id="39eb2-198">Die folgenden Chatroom-Eigenschaften, die in früheren Versionen des beständigen Chat Servers enthalten waren, wurden eliminiert:</span><span class="sxs-lookup"><span data-stu-id="39eb2-198">The following chat room properties that were included in previous versions of Persistent Chat Server have been eliminated:</span></span>

  - <span data-ttu-id="39eb2-199">Thema: ein Raum hat jetzt nur eine Beschreibung.</span><span class="sxs-lookup"><span data-stu-id="39eb2-199">Topic: A Room now only has a Description.</span></span>

  - <span data-ttu-id="39eb2-200">Neue Mitgliederliste erstellen: auf dem Server für beständigen Chat beginnen alle Chatrooms mit einer leeren Mitgliedschaft (und können eine Mitgliedschaft maximieren, die den zulässigen Mitgliedern entspricht).</span><span class="sxs-lookup"><span data-stu-id="39eb2-200">Create New Member list: In Persistent Chat Server, all chat rooms start with empty membership (and can maximize to a membership equaling the Allowed Members).</span></span>

  - <span data-ttu-id="39eb2-201">Dateiupload: verwendet als eine Einstellung pro Chatroom, um zu steuern, ob Dateiupload/-Downloads zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="39eb2-201">File Upload: Used to be a setting per chat room to control whether file upload/downloads were allowed.</span></span> <span data-ttu-id="39eb2-202">Damit wird nun nur die Kategorieebene festgesetzt und gilt für alle Räume in dieser Kategorie.</span><span class="sxs-lookup"><span data-stu-id="39eb2-202">This is now set only the category level and applies to all rooms in that category.</span></span>

  - <span data-ttu-id="39eb2-203">Chat-Protokoll: verwendet als eine Einstellung pro Chatroom, um zu steuern, ob das Chat-Protokoll aktiviert wurde, aber jetzt nur auf der Kategorieebene festgelegt ist und für alle Räume in dieser Kategorie gilt.</span><span class="sxs-lookup"><span data-stu-id="39eb2-203">Chat History: Used to be a setting per chat room to control if Chat History was enabled, but is now set only at the category level and applies to all rooms in that category.</span></span>

  - <span data-ttu-id="39eb2-204">Einladungen: ein Raum erbt immer die Einstellung Einladungen für die Kategorie; oder es kann auf dem Raum ausgeschaltet werden.</span><span class="sxs-lookup"><span data-stu-id="39eb2-204">Invites: A room always inherits the Invites setting for the category; or it can be turned off on the room.</span></span> <span data-ttu-id="39eb2-205">Ein Raum kann Einladungen nicht aktivieren, wenn die Kategorie zuvor auf Einladungen aus eingestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="39eb2-205">A room cannot turn on Invites if the category was previously set to Invites off.</span></span>

</div>

<div>

## <a name="whats-different-about-policies-from-previous-group-chat-server-versions"></a><span data-ttu-id="39eb2-206">Was unterscheidet sich von den Richtlinien aus früheren Gruppen-Chat Server Versionen?</span><span class="sxs-lookup"><span data-stu-id="39eb2-206">What’s Different about Policies from Previous Group Chat Server Versions?</span></span>

<span data-ttu-id="39eb2-207">Der Server für beständigen Chat hat eine neue lync-Richtlinie mit beständigem Chat, pro Benutzer/Pool/Website/globale Einstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="39eb2-207">Persistent Chat Server has a new Lync policy enabled with Persistent Chat, per user/pool/site/global settings.</span></span> <span data-ttu-id="39eb2-208">Im lync 2013-Client ist die Umgebung für beständigen Chat nur für Benutzer verfügbar, die durch Richtlinie für beständigen Chat aktiviert sind (entweder direkt oder über die Einstellung Pool/Website/Global).</span><span class="sxs-lookup"><span data-stu-id="39eb2-208">In the Lync 2013 client, the Persistent Chat environment is available only for users who are enabled by policy for Persistent Chat (either directly or through the pool/site/global setting).</span></span>

<span data-ttu-id="39eb2-209">In früheren Versionen des Gruppen Chat Servers wurden keine Richtlinien in die lync-Server Richtlinien integriert.</span><span class="sxs-lookup"><span data-stu-id="39eb2-209">Previous versions of Group Chat Server did not have any policies integrated into the Lync Server policies.</span></span> <span data-ttu-id="39eb2-210">Auf der Basis pro Benutzer und pro Kategorie/Raum können Sie mithilfe des Features "Dateien pro Benutzer **hochladen** " einen Benutzer Administrator, einen Chatroom-Administrator oder die Möglichkeit zum Hochladen von Dateien durch den Benutzer festlegen.</span><span class="sxs-lookup"><span data-stu-id="39eb2-210">On a per user and per category/room basis, by using the **Can Upload Files** per user feature, you could make the user a User administrator, a chat room administrator, or configure the user’s ability to upload files.</span></span> <span data-ttu-id="39eb2-211">Die **Datei Upload** -Funktion des beständigen Chat Servers ist nur pro Kategorie.</span><span class="sxs-lookup"><span data-stu-id="39eb2-211">The Persistent Chat Server **File Upload** feature is just per category.</span></span>

</div>

<div>

## <a name="logging"></a><span data-ttu-id="39eb2-212">Protokollierung</span><span class="sxs-lookup"><span data-stu-id="39eb2-212">Logging</span></span>

<span data-ttu-id="39eb2-213">Die Protokollierung für den Server für beständigen Chat und System Center Operations Manager ist in die lync Server 2013-Ablaufverfolgungsprotokollierung integriert.</span><span class="sxs-lookup"><span data-stu-id="39eb2-213">Logging for Persistent Chat Server and System Center Operations Manager is integrated into the Lync Server 2013 trace logging.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="39eb2-214">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="39eb2-214">See Also</span></span>


[<span data-ttu-id="39eb2-215">Planen für den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39eb2-215">Planning for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-planning-for-persistent-chat-server.md)  
  

<span data-ttu-id="39eb2-216"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39eb2-216"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
