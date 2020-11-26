---
title: Ausführen der Abwärtskompatibilität für den Server für beständigen Chat
description: Führen Sie die Abwärtskompatibilität für beständigen Chat Server aus.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Run backward compatibility for Persistent Chat Server
ms:assetid: 53f1a706-3104-4a94-8b4e-8badd9a066d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204901(v=OCS.15)
ms:contentKeyID: 48184175
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b0486992d44e6385559d3e9df9f9ffc2125120da
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423379"
---
# <a name="run-backward-compatibility-for-persistent-chat-server"></a><span data-ttu-id="28b1f-103">Ausführen der Abwärtskompatibilität für den Server für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="28b1f-103">Run backward compatibility for Persistent Chat Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="28b1f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="28b1f-104">

<span> </span></span></span>

<span data-ttu-id="28b1f-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="28b1f-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="28b1f-106">Der lync Server 2013, beständiger Chat Serverendpunkt bietet eine Möglichkeit zum Erstellen einer einfachen URL, die auf einen beständigen Chat Serverpool verweist.</span><span class="sxs-lookup"><span data-stu-id="28b1f-106">The Lync Server 2013, Persistent Chat Server endpoint provides a way to create a simple URL that points to a Persistent Chat Server pool.</span></span> <span data-ttu-id="28b1f-107">Dies ist nützlich für Legacy-Clients (Microsoft Office Communications Server 2007 R2-Gruppen-Chat Server oder lync Server 2010, Gruppen-Chat), da Benutzer in der manuellen Konfiguration eine einfache URL eingeben können, wenn Sie versuchen, den Legacyclient auf einen Computer mit lync 2013, beständigen Chat, zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="28b1f-107">This is useful for legacy clients (Microsoft Office Communications Server 2007 R2 Group Chat Server or Lync Server 2010, Group Chat) because users can enter a simple URL in the manual configuration when trying to point the legacy client to a computer running Lync 2013, Persistent Chat.</span></span> <span data-ttu-id="28b1f-108">Dieser Endpunkt wird nicht vom beständigen Chat verwendet und ist nur für Legacyclients erforderlich.</span><span class="sxs-lookup"><span data-stu-id="28b1f-108">This endpoint isn’t used by Persistent Chat, and is required for legacy clients only.</span></span> <span data-ttu-id="28b1f-109">Dies ist für den zwischen Zeitraum nützlich, in dem Räume migriert werden können, die lync 2013-Clients aber nicht in der gesamten Organisation bereitgestellt wurden.</span><span class="sxs-lookup"><span data-stu-id="28b1f-109">This is useful for the interim period where rooms may be migrated, but the Lync 2013 clients have not been deployed throughout the organization.</span></span> <span data-ttu-id="28b1f-110">Benutzer, die den lync 2010-Gruppen-Chat (Client) ausführen, können dann weiterhin eine Verbindung mit dem Server für beständigen Chat-Server herstellen.</span><span class="sxs-lookup"><span data-stu-id="28b1f-110">Users running Lync 2010 Group Chat (client) can then still connect to the Persistent Chat Server Back End Server.</span></span>

<span data-ttu-id="28b1f-111">Sie müssen nicht mehrere Endpunkte für beständigen Chat Server erstellen; Sie benötigen nur eine für jeden beständigen Chat Server Pool.</span><span class="sxs-lookup"><span data-stu-id="28b1f-111">You don’t need to create multiple Persistent Chat Server endpoints; you just need one for each Persistent Chat Server pool.</span></span> <span data-ttu-id="28b1f-112">Administratoren können mehrere Endpunkte (eine pro Pool) erstellen, ältere Clients können jedoch so konfiguriert werden, dass Sie nur mit einem Pool verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="28b1f-112">Administrators can create multiple endpoints (one per pool), but legacy clients can be configured to connect to only one pool at a time.</span></span> <span data-ttu-id="28b1f-113">Im normalen oder Mainstream-Szenario ist die Legacy Bereitstellung nur ein Pool.</span><span class="sxs-lookup"><span data-stu-id="28b1f-113">In the usual or mainstream scenario, the legacy deployment is one pool only.</span></span> <span data-ttu-id="28b1f-114">Eine neue Bereitstellung migriert in der Regel diesen Pool zu einem neuen lync Server 2013 und fügt möglicherweise einige neue Server Pools für beständigen Chat hinzu.</span><span class="sxs-lookup"><span data-stu-id="28b1f-114">A new deployment generally migrates that pool to a new Lync Server 2013 and might add some new additional Persistent Chat Server pools.</span></span>

<span data-ttu-id="28b1f-115">Dieses Mainstream-Szenario folgt in der Regel diesem Muster:</span><span class="sxs-lookup"><span data-stu-id="28b1f-115">This mainstream scenario generally follows this pattern:</span></span>

  - <span data-ttu-id="28b1f-116">Sie verwalten Benutzer mit einem lync Server 2010, Gruppen-Chat-Pool und ihren lync 2010-Gruppen-Chat-Clients, die eine Verbindung mit diesem Pool herstellen, indem Sie einen bekannten Benutzer verwenden (entweder standardmäßig SIP: OCSChat@ \<domainName\> . com oder eine ähnliche).</span><span class="sxs-lookup"><span data-stu-id="28b1f-116">You administer users with one Lync Server 2010, Group Chat pool, and your Lync 2010 Group Chat clients connect to that pool by using some well-known user (either default sip:ocschat@\<domainName\>.com, or a similar one).</span></span> <span data-ttu-id="28b1f-117">Die Benutzer sind SIP-fähige Active Directory-Domänendienste, und der Suchdienst registriert sich, um eingehende Anforderungen zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="28b1f-117">The users are SIP-enabled Active Directory Domain Services, and the Lookup service registers with them to receive incoming requests.</span></span>

  - <span data-ttu-id="28b1f-118">Anschließend installieren Sie einen lync Server 2013-beständigen Chat Server und einen beständigen Chat Serverpool.</span><span class="sxs-lookup"><span data-stu-id="28b1f-118">Subsequently, you install a Lync Server 2013 Persistent Chat Server and Persistent Chat Server pool.</span></span>

  - <span data-ttu-id="28b1f-119">In einer Zeit, in der Benutzer im allgemeinen offline sind (beispielsweise ein Wochenende):</span><span class="sxs-lookup"><span data-stu-id="28b1f-119">During a time when users are generally offline (for example, a weekend):</span></span>
    
      - <span data-ttu-id="28b1f-120">Deaktivieren Sie lync Server 2010, Gruppen-Chat.</span><span class="sxs-lookup"><span data-stu-id="28b1f-120">Turn off Lync Server 2010, Group Chat.</span></span>
    
      - <span data-ttu-id="28b1f-121">Migrieren Sie Daten aus dem lync Server 2010, Gruppen-Chat-Pool, in den lync Server 2013-Serverpool für beständigen Chat.</span><span class="sxs-lookup"><span data-stu-id="28b1f-121">Migrate data from the Lync Server 2010, Group Chat pool to the Lync Server 2013 Persistent Chat Server pool.</span></span>
    
      - <span data-ttu-id="28b1f-122">Löschen Sie den bekannten Benutzer aus den Active Directory-Domänendiensten.</span><span class="sxs-lookup"><span data-stu-id="28b1f-122">Delete the well-known user from the Active Directory Domain Services.</span></span>
    
      - <span data-ttu-id="28b1f-123">Erstellen Sie einen neuen *Legacy Endpunkt* mit dem gleichen SIP-URI wie der zuvor gelöschte bekannte Benutzer.</span><span class="sxs-lookup"><span data-stu-id="28b1f-123">Create a new *legacy endpoint* with the same SIP URI as the previously deleted well-known user.</span></span>
    
      - <span data-ttu-id="28b1f-124">Starten Sie die lync Server 2013, persistent Chat Server.</span><span class="sxs-lookup"><span data-stu-id="28b1f-124">Start the Lync Server 2013, Persistent Chat Servers.</span></span>

  - <span data-ttu-id="28b1f-125">Benutzer melden sich mit Ihrem lync 2010-Gruppen-Chat (Client) wieder an und stellen eine Verbindung mit Ihren Daten her, ohne dass eine Konfiguration geändert werden muss.</span><span class="sxs-lookup"><span data-stu-id="28b1f-125">Users log back on by using their Lync 2010 Group Chat (client) and connect to their data without needing to change any configuration.</span></span>

  - <span data-ttu-id="28b1f-126">Zu einem späteren Zeitpunkt können Sie den lync Server 2010, Gruppen-Chat, außer Betrieb nehmen.</span><span class="sxs-lookup"><span data-stu-id="28b1f-126">At a later time, you can decommission the Lync Server 2010, Group Chat.</span></span> <span data-ttu-id="28b1f-127">Anschließend können Sie lync Server 2013, beständiger Chat Server und neue lync Server 2013-Server Pools für beständige Chats installieren.</span><span class="sxs-lookup"><span data-stu-id="28b1f-127">Subsequently, you can deploy Lync Server 2013, Persistent Chat Server, and install new Lync Server 2013 Persistent Chat Server pools.</span></span>

<span data-ttu-id="28b1f-128">Details zur Migration von lync Server 2010, Gruppen-Chat zu lync Server 2013, beständiger Chat Server, finden Sie unter [Migration von lync Server 2010, Gruppen-Chat oder Office Communications Server 2007 R2-Gruppenchat zu lync Server 2013, beständiger Chat Server](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="28b1f-128">For details about migrating from Lync Server 2010, Group Chat to Lync Server 2013, Persistent Chat Server, see [Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md).</span></span>

<span data-ttu-id="28b1f-129">So führen Sie Abwärtskompatibilität aus (zum Erstellen eines beständigen Chat Server-Endpunkts, der auf einen beständigen Chat Serverpool verweist, der von Legacy-Gruppen-Chat Pool-Clients verwendet werden kann):</span><span class="sxs-lookup"><span data-stu-id="28b1f-129">To run backward compatibility (to create a Persistent Chat Server endpoint that points to a Persistent Chat Server pool, which can be used by legacy Group Chat pool clients):</span></span>

    New-CsPersistentChatEndpoint -SipAddress <CO name, ex. persistentchat@contoso.com> -PersistentChatPoolFqdn <pool FQDN, like pcpool.contoso.com>

<span data-ttu-id="28b1f-130">Konfigurieren Sie als nächstes Clients für beständigen Chat, um diese SIP-Adresse als Kontaktobjekt zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="28b1f-130">Next, configure Persistent Chat clients to use that SIP address as their contact object.</span></span> <span data-ttu-id="28b1f-131">Die SIP-Adresse wird mit dem Cmdlet **New-CsPersistentChatEndpoint** für einen bestimmten beständigen Chat Server Pool erstellt.</span><span class="sxs-lookup"><span data-stu-id="28b1f-131">The SIP address is created with the **New-CsPersistentChatEndpoint** cmdlet for a specific Persistent Chat Server pool.</span></span>

<span data-ttu-id="28b1f-132">Wenn Sie den beständigen Chat-Server Endpunkt mithilfe der Windows PowerShell-Befehlszeilenschnittstelle hinzufügen möchten, sollten Sie das folgende Beispiel Bedenken.</span><span class="sxs-lookup"><span data-stu-id="28b1f-132">To add the Persistent Chat Server endpoint by using Windows PowerShell command-line interface, consider the following example.</span></span> <span data-ttu-id="28b1f-133">In diesem Fall konfigurieren Sie das Kontaktobjekt mit dem Namen "persistentchat" in der Topologie "contoso.com", wobei der vollqualifizierte Domänenname (Fully Qualified Domain Name, FQDN) des Pools "pcpool.contoso.com" lautet:</span><span class="sxs-lookup"><span data-stu-id="28b1f-133">In this case, you are configuring the contact object to be named "persistentchat" on the "contoso.com" topology, where the pool fully qualified domain name (FQDN) is "pcpool.contoso.com":</span></span>

    New-CsPersistentChatEndpoint -SipAddress sip:persistentchat@contoso.com -PersistentChatPoolFqdn pcpool.contoso.com

<div>

## <a name="see-also"></a><span data-ttu-id="28b1f-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28b1f-134">See Also</span></span>


[<span data-ttu-id="28b1f-135">Migration von Lync Server 2010-Gruppenchat oder Office Communications Server 2007 R2-Gruppenchat zu Lync Server 2013 Persistent Chat Server</span><span class="sxs-lookup"><span data-stu-id="28b1f-135">Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server</span></span>](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md)  
  

<span data-ttu-id="28b1f-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="28b1f-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

