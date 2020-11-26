---
title: 'Lync Server 2013: Definieren der Anforderungen für Front-End-Server, Chat und Anwesenheit'
description: 'Lync Server 2013: Definieren Ihrer Anforderungen für Front-End-Server, Instant Messaging und Anwesenheitsinformationen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining your requirements for Front End Servers, instant messaging, and presence
ms:assetid: c21198bc-520c-4d17-8b84-7ff1475b9b0a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412956(v=OCS.15)
ms:contentKeyID: 48185319
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 923132b32d5aef80191b19a7b85c3f17276e5946
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430812"
---
# <a name="defining-your-requirements-for-front-end-servers-instant-messaging-and-presence-in-lync-server-2013"></a><span data-ttu-id="22df9-103">Definieren der Anforderungen für Front-End-Server, Chat und Anwesenheit in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22df9-103">Defining your requirements for Front End Servers, instant messaging, and presence in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="22df9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="22df9-104">

<span> </span></span></span>

<span data-ttu-id="22df9-105">_**Letztes Änderungsdatum des Themas:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="22df9-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="22df9-106">Die wichtigste Aufgabe bei der Planung von Instant Messaging (im) und Anwesenheitsfunktionen besteht darin, sicherzustellen, dass Sie über genügend Front-End-Server für Ihre Benutzer verfügen.</span><span class="sxs-lookup"><span data-stu-id="22df9-106">The main task of planning for instant messaging (IM) and presence is ensuring that you have enough Front End Servers for your users.</span></span>

<div>

## <a name="enabling-communication-with-external-users"></a><span data-ttu-id="22df9-107">Aktivieren der Kommunikation mit externen Benutzern</span><span class="sxs-lookup"><span data-stu-id="22df9-107">Enabling Communication with External Users</span></span>

<span data-ttu-id="22df9-108">Sie können die Vorteile Ihrer Investition in lync Server erheblich steigern, indem Sie es Ihren Benutzern ermöglichen, mit externen Benutzern zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="22df9-108">You can greatly increase the benefits of your investment in Lync Server by enabling your users to communicate with external users.</span></span> <span data-ttu-id="22df9-109">Bei externen Benutzern sind unter anderem folgende Kategorien möglich:</span><span class="sxs-lookup"><span data-stu-id="22df9-109">External users can include:</span></span>

  - <span data-ttu-id="22df9-110">**Remote Benutzer**   Die eigenen Benutzer Ihrer Organisation, wenn diese außerhalb Ihrer Firewalls arbeiten und ihre Laptops oder andere lync Server-Geräte verwenden.</span><span class="sxs-lookup"><span data-stu-id="22df9-110">**Remote users**   Your organization’s own users, when they are working outside your firewalls and are using their laptops or other Lync Server devices.</span></span>

  - <span data-ttu-id="22df9-111">**Federated-Benutzer**   Benutzer von Unternehmen, mit denen Sie zusammenarbeiten, die ebenfalls lync Server ausführen.</span><span class="sxs-lookup"><span data-stu-id="22df9-111">**Federated users**   Users from companies you work with who also run Lync Server.</span></span> <span data-ttu-id="22df9-112">Damit Ihre Benutzer problemlos Kontakt zu diesen Benutzern aufnehmen können, erstellen Sie Partnerverbundbeziehungen mit diesen Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="22df9-112">To enable your users to easily contact these users, you create federated relationships with these companies.</span></span>

  - <span data-ttu-id="22df9-113">**Öffentliche Benutzer**   Benutzer von öffentlichen Chat Diensten, beispielsweise Chat Dienste, die vom Windows Live-Netzwerk von Internet Diensten, Yahoo \! und AOL bereitgestellt werden, sowie Benutzer von Anbietern und Servern, die das Extensible Messaging and Presence Protocol (XMPP) verwenden, wie etwa Google Talk.</span><span class="sxs-lookup"><span data-stu-id="22df9-113">**Public users**   Users of public IM services, such as IM services provided by the Windows Live network of Internet services, Yahoo\!, and AOL, and users of providers and servers that use Extensible Messaging and Presence Protocol (XMPP), such as Google Talk.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="22df9-114">Beachten Sie, dass für öffentliche Chat Verbindungen mit Windows Live, AOL und Yahoo! möglicherweise eine separate Lizenz erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="22df9-114">Note that a separate license might be required for public IM connectivity with Windows Live, AOL, and Yahoo!</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="22df9-115">Ab dem 1. September, 2012, ist die Microsoft lync Public im Connectivity-Benutzerabonnementlizenz ("PIC USL") nicht mehr für den Kauf von neuen oder erneuernden Vereinbarungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="22df9-115">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="22df9-116">Kunden mit aktiven Lizenzen sind in der Lage, weiterhin mit Yahoo! zu verbünden</span><span class="sxs-lookup"><span data-stu-id="22df9-116">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="22df9-117">Messenger, bis der Dienst das Datum beendet hat.</span><span class="sxs-lookup"><span data-stu-id="22df9-117">Messenger until the service shut down date.</span></span> <span data-ttu-id="22df9-118">Datum des Endes des Lebenszyklus von Juni 2014 für AOL und Yahoo!</span><span class="sxs-lookup"><span data-stu-id="22df9-118">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="22df9-119">wurde angekündigt.</span><span class="sxs-lookup"><span data-stu-id="22df9-119">has been announced.</span></span> <span data-ttu-id="22df9-120">Ausführliche Informationen finden Sie <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">unter Unterstützung für öffentliche Instant Messenger-Konnektivität in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="22df9-120">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="22df9-121">Bei der PIC-USL handelt es sich um eine Abonnementlizenz pro Benutzer pro Monat, die für die Föderation von lync Server oder Office Communications Server mit Yahoo! erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="22df9-121">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="22df9-122">Messenger.</span><span class="sxs-lookup"><span data-stu-id="22df9-122">Messenger.</span></span> <span data-ttu-id="22df9-123">Die Möglichkeit von Microsoft, diesen Dienst bereitzustellen, war von der Unterstützung durch Yahoo! abhängig, deren zugrunde liegende Vereinbarung abgewickelt wird.</span><span class="sxs-lookup"><span data-stu-id="22df9-123">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="22df9-124">Lync ist mehr denn je ein leistungsfähiges Tool für die Verbindung zwischen Organisationen und Personen in der ganzen Welt.</span><span class="sxs-lookup"><span data-stu-id="22df9-124">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="22df9-125">Für den Verbund mit Windows Live Messenger sind keine zusätzlichen Benutzer-und Gerätelizenzen außerhalb der lync-Standard CAL erforderlich.</span><span class="sxs-lookup"><span data-stu-id="22df9-125">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="22df9-126">Skype Federation wird dieser Liste hinzugefügt und ermöglicht es lync-Benutzern, Hunderte von Millionen von Personen mit Chat und Sprache zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="22df9-126">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>

    
    </div>

<span data-ttu-id="22df9-127">Wenn Sie ein oder alle dieser Szenarien aktivieren möchten, müssen Sie einen Edgeserver bereitstellen, um die sichere Kommunikation zwischen Ihrer lync Server-Bereitstellung und externen Benutzern zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="22df9-127">To enable any or all of these scenarios, you need to deploy an Edge Server to help enable secure communications between your Lync Server deployment and external users.</span></span> <span data-ttu-id="22df9-128">Remotebenutzer Ihrer Organisation und Benutzer in Partnerorganisationen können ihre Anwesenheitsinformationen sehen und über Chat miteinander kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="22df9-128">Your organization’s remote users and users at federated organizations will be able to see each other’s presence and communicate using IM.</span></span> <span data-ttu-id="22df9-129">Details zum Aktivieren der Kommunikation mit externen Benutzern finden Sie unter [Planen des Zugriffs externer Benutzer in lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="22df9-129">For details about enabling communication with external users, see [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="archiving-im-content"></a><span data-ttu-id="22df9-130">Archivieren von Chat Inhalten</span><span class="sxs-lookup"><span data-stu-id="22df9-130">Archiving IM Content</span></span>

<span data-ttu-id="22df9-131">Lync Server bietet Funktionen, die Sie verwenden können, wenn Ihre Organisation Konformitätsrichtlinien beachten muss.</span><span class="sxs-lookup"><span data-stu-id="22df9-131">Lync Server provides features you can use if your organization must follow compliance regulations.</span></span> <span data-ttu-id="22df9-132">Mithilfe der Archivierung können Sie Chatinhalte für alle Benutzer in Ihrer Organisation oder nur für bestimmte Benutzer archivieren.</span><span class="sxs-lookup"><span data-stu-id="22df9-132">You can use Archiving to archive the content of IM messages for all users in your organization or for only certain users that you specify.</span></span> <span data-ttu-id="22df9-133">Ausführliche Informationen finden Sie unter [Planen der Archivierung in lync Server 2013](lync-server-2013-planning-for-archiving.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="22df9-133">For details, see [Planning for Archiving in Lync Server 2013](lync-server-2013-planning-for-archiving.md) in the Planning documentation.</span></span>

<span data-ttu-id="22df9-134">Wenn Sie auch Microsoft Exchange Server 2013 bereitgestellt haben, können Sie die Archivierung von Exchange-Daten mit der Archivierung von lync Server-Daten integrieren und ein einzelnes Tool verwenden, um beide Arten von archivierten Daten zu durchsuchen.</span><span class="sxs-lookup"><span data-stu-id="22df9-134">If you also have Microsoft Exchange Server 2013 deployed, you can integrate the archiving of Exchange data with the archiving of Lync Server data, and use a single tool to search both types of archived data.</span></span> <span data-ttu-id="22df9-135">Weitere Informationen finden Sie unter [Konfigurieren von Microsoft lync Server 2013 für die Verwendung von Microsoft Exchange Server 2013-Archivierung](configuring-lync-server-2013-to-use-microsoft-exchange-server-2013-archiving.md).</span><span class="sxs-lookup"><span data-stu-id="22df9-135">For more information, see [Configuring Microsoft Lync Server 2013 to use Microsoft Exchange Server 2013 archiving](configuring-lync-server-2013-to-use-microsoft-exchange-server-2013-archiving.md).</span></span>

<span data-ttu-id="22df9-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="22df9-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

