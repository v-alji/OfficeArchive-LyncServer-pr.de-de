---
title: Lync Server 2013-Referenztopologie für kleine Organisationen
description: Lync Server 2013-Referenztopologie für kleine Organisationen
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reference topology for small organizations
ms:assetid: 0453aeee-c41f-44e6-a6e0-aaace526ca08
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398095(v=OCS.15)
ms:contentKeyID: 48183272
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7f2f23a963543c303e54f8f2773d499e8317a63a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436611"
---
# <a name="reference-topology-for-lync-server-2013-in-small-organizations"></a><span data-ttu-id="fb143-103">Referenztopologie für lync Server 2013 in kleinen Organisationen</span><span class="sxs-lookup"><span data-stu-id="fb143-103">Reference topology for Lync Server 2013 in small organizations</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fb143-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fb143-104">

<span> </span></span></span>

<span data-ttu-id="fb143-105">_**Letztes Änderungsdatum des Themas:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="fb143-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="fb143-106">Die Referenztopologie für kleine Organisationen zeigt, wie Sie eine robuste, hoch verfügbare Lösung bereitstellen können, indem Sie nur drei Server mit lync Server bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="fb143-106">The reference topology for small organizations shows how you can deploy a robust, highly available solution by deploying only three servers running Lync Server.</span></span>

<span data-ttu-id="fb143-107">**Referenztopologie für kleine Organisationen**</span><span class="sxs-lookup"><span data-stu-id="fb143-107">**Reference topology for small organizations**</span></span>

<span data-ttu-id="fb143-108">![Referenztopologie mit drei Servern (Diagramm)](images/Gg398095.25196d0d-dd07-451b-83ba-94c0ddf59030(OCS.15).jpg "Referenztopologie mit drei Servern (Diagramm)")</span><span class="sxs-lookup"><span data-stu-id="fb143-108">![Reference topology deploying three servers diagram](images/Gg398095.25196d0d-dd07-451b-83ba-94c0ddf59030(OCS.15).jpg "Reference topology deploying three servers diagram")</span></span>

  - <span data-ttu-id="fb143-109">**Paar von Standard Edition-Servern bereitgestellt**    Diese Organisation hat 4.000-Benutzer an Ihrem zentralen Standort.</span><span class="sxs-lookup"><span data-stu-id="fb143-109">**Pair of Standard Edition Servers Deployed**    This organization has 4,000 users at their central site.</span></span> <span data-ttu-id="fb143-110">Die Organisation hat zwei Standard Edition-Server bereitgestellt und kombiniert, um eine höhere Verfügbarkeit und Disaster Recovery zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="fb143-110">The organization has deployed two Standard Edition servers and paired them together to enable high availability and disaster recovery.</span></span> <span data-ttu-id="fb143-111">Jeder Server verfügt über 2.000-Benutzer, aber Informationen zu allen Benutzern werden zwischen den beiden Servern synchronisiert.</span><span class="sxs-lookup"><span data-stu-id="fb143-111">Each server homes 2,000 users, but information about all users is synchronized between the two servers.</span></span> <span data-ttu-id="fb143-112">Wenn einer ausfällt, kann ein Administrator für diese Benutzer einen Failover durchführen, um von dem anderen Server bedient zu werden, mit einem mindestunterbrechungs Intervall für die Benutzer.</span><span class="sxs-lookup"><span data-stu-id="fb143-112">If one goes down, an administrator can fail over those users to be served by the other server, with a minimum of disruption to users.</span></span> <span data-ttu-id="fb143-113">Weitere Informationen zu Funktionen für die Hochverfügbarkeits-und Disaster Recovery in lync Server 2013 finden Sie unter [Planen von Hochverfügbarkeits-und Disaster Recovery in lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span><span class="sxs-lookup"><span data-stu-id="fb143-113">For more information about high availability and disaster recovery features in Lync Server 2013, see [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span>

  - <span data-ttu-id="fb143-114">**Empfehlung der Bereitstellung eines Edgeservers.**</span><span class="sxs-lookup"><span data-stu-id="fb143-114">**Edge Server deployment is recommended.**</span></span>   <span data-ttu-id="fb143-115">Auch wenn die Bereitstellung eines Edgeservers für interne Chats, für Anwesenheitsinformationen und für Konferenzen nicht erforderlich ist, wird sie selbst für kleine Bereitstellungen empfohlen.</span><span class="sxs-lookup"><span data-stu-id="fb143-115">Although deploying an Edge Server is not required for internal IM, presence and conferencing, we recommend it even for small deployments.</span></span> <span data-ttu-id="fb143-116">Sie können Ihre lync Server-Investition maximieren, indem Sie einen Edgeserver bereitstellen, um die Dienste für Benutzer bereitzustellen, die sich derzeit außerhalb der Firewalls Ihrer Organisation befinden.</span><span class="sxs-lookup"><span data-stu-id="fb143-116">You can maximize your Lync Server investment by deploying an Edge Server to provide service to users currently outside your organization’s firewalls.</span></span> <span data-ttu-id="fb143-117">Dies bietet folgende Vorteile:</span><span class="sxs-lookup"><span data-stu-id="fb143-117">The benefits include the following:</span></span>
    
      - <span data-ttu-id="fb143-118">Die eigenen Benutzer Ihrer Organisation können die lync-Server Funktionalität verwenden, wenn Sie von zu Hause aus arbeiten oder unterwegs sind.</span><span class="sxs-lookup"><span data-stu-id="fb143-118">Your organization’s own users can use Lync Server functionality, if they are working from home or are out on the road.</span></span>
    
      - <span data-ttu-id="fb143-119">Ihre Benutzer können externe Benutzer zur Teilnahme an Besprechungen einladen.</span><span class="sxs-lookup"><span data-stu-id="fb143-119">Your users can invite outside users to participate in meetings.</span></span>
    
      - <span data-ttu-id="fb143-120">Wenn Sie über einen Partner, einen Kreditor oder eine Kundenorganisation verfügen, die ebenfalls lync Server verwendet, können Sie eine *Verbundbeziehung* mit dieser Organisation bilden.</span><span class="sxs-lookup"><span data-stu-id="fb143-120">If you have a partner, vendor or customer organization that also uses Lync Server, you can form a *federated relationship* with that organization.</span></span> <span data-ttu-id="fb143-121">Ihre lync Server-Bereitstellung erkennt dann Benutzer aus dieser Verbundorganisation, was zu einer besseren Zusammenarbeit führt.</span><span class="sxs-lookup"><span data-stu-id="fb143-121">Your Lync Server deployment would then recognize users from that federated organization, leading to better collaboration.</span></span>
    
      - <span data-ttu-id="fb143-122">Ihre Benutzer können Sofortnachrichten mit Benutzern von öffentlichen Chat Diensten austauschen, einschließlich einer oder aller der folgenden: Windows Live, AOL, Yahoo \! und Google Talk.</span><span class="sxs-lookup"><span data-stu-id="fb143-122">Your users can exchange instant messages with users of public IM services, including any or all of the following: Windows Live, AOL, Yahoo\!, and Google Talk.</span></span> <span data-ttu-id="fb143-123">Für die Konnektivität öffentlicher Chats mit diesen Diensten ist möglicherweise eine separate Lizenz erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fb143-123">A separate license might be required for public IM connectivity with these services.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <UL>
        > <LI>
        > <P><span data-ttu-id="fb143-124">Ab dem 1. September, 2012, ist die Microsoft lync Public im Connectivity-Benutzerabonnementlizenz ("PIC USL") nicht mehr für den Kauf von neuen oder erneuernden Vereinbarungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="fb143-124">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="fb143-125">Kunden mit aktiven Lizenzen sind in der Lage, weiterhin mit Yahoo! zu verbünden</span><span class="sxs-lookup"><span data-stu-id="fb143-125">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="fb143-126">Messenger, bis der Dienst das Datum beendet hat.</span><span class="sxs-lookup"><span data-stu-id="fb143-126">Messenger until the service shut down date.</span></span> <span data-ttu-id="fb143-127">Datum des Endes des Lebenszyklus von Juni 2014 für AOL und Yahoo!</span><span class="sxs-lookup"><span data-stu-id="fb143-127">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="fb143-128">wurde angekündigt.</span><span class="sxs-lookup"><span data-stu-id="fb143-128">has been announced.</span></span> <span data-ttu-id="fb143-129">Ausführliche Informationen finden Sie <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">unter Unterstützung für öffentliche Instant Messenger-Konnektivität in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="fb143-129">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
        > <LI>
        > <P><span data-ttu-id="fb143-130">Bei der PIC-USL handelt es sich um eine Abonnementlizenz pro Benutzer pro Monat, die für die Föderation von lync Server oder Office Communications Server mit Yahoo! erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="fb143-130">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="fb143-131">Messenger.</span><span class="sxs-lookup"><span data-stu-id="fb143-131">Messenger.</span></span> <span data-ttu-id="fb143-132">Die Möglichkeit von Microsoft, diesen Dienst bereitzustellen, war von der Unterstützung durch Yahoo! abhängig, deren zugrunde liegende Vereinbarung abgewickelt wird.</span><span class="sxs-lookup"><span data-stu-id="fb143-132">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
        > <LI>
        > <P><span data-ttu-id="fb143-133">Lync ist mehr denn je ein leistungsfähiges Tool für die Verbindung zwischen Organisationen und Personen in der ganzen Welt.</span><span class="sxs-lookup"><span data-stu-id="fb143-133">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="fb143-134">Für den Verbund mit Windows Live Messenger sind keine zusätzlichen Benutzer-und Gerätelizenzen außerhalb der lync-Standard CAL erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fb143-134">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="fb143-135">Skype Federation wird dieser Liste hinzugefügt und ermöglicht es lync-Benutzern, Hunderte von Millionen von Personen mit Chat und Sprache zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="fb143-135">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>

        
        </div>

  - <span data-ttu-id="fb143-136">**Ausfallsicherheit für Zweigstellen.**</span><span class="sxs-lookup"><span data-stu-id="fb143-136">**Branch site survivability.**</span></span>   <span data-ttu-id="fb143-137">In dieser Organisation wird ein Pilotprogramm des Enterprise-VoIP-Features von lync Server ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="fb143-137">This organization is running a pilot program of the Enterprise Voice feature of Lync Server.</span></span> <span data-ttu-id="fb143-138">Einige Benutzer verwenden lync Server als einzige Sprachlösung.</span><span class="sxs-lookup"><span data-stu-id="fb143-138">Some users are using Lync Server as their sole voice solution.</span></span> <span data-ttu-id="fb143-139">Einige dieser sprach Pilotbenutzer befinden sich auf der Zweigstelle.</span><span class="sxs-lookup"><span data-stu-id="fb143-139">Some of these Voice pilot users are located at the branch site.</span></span> <span data-ttu-id="fb143-140">Die Verzweigungs Website verfügt nicht über einen zuverlässigen WAN-Link (Wide Area Network) mit dem zentralen Standort, daher wird eine Survivable Branch-Appliance dort bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="fb143-140">The branch site does not have a reliable wide area network (WAN) link to the central site, so a Survivable Branch Appliance is deployed there.</span></span> <span data-ttu-id="fb143-141">Dank der Survivable Branch-Anwendung können die Benutzer in der Zweigstelle bei Ausfall der WAN-Verbindung weiterhin Anrufe tätigen und entgegennehmen (sowohl innerhalb der Organisation als auch über das Festnetz), die Voicemailfunktion nutzen und per Chat kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="fb143-141">With this deployed, if the WAN link goes down, users at the branch site can still make and receive calls (both calls within the organization and PSTN calls), have voice mail functionality, and communicate with two-party instant messaging (IM).</span></span> <span data-ttu-id="fb143-142">Benutzer können darüber hinaus auch dann authentifiziert werden, wenn die WAN-Verbindung nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="fb143-142">Users can also be authenticated when the WAN link is unavailable as well.</span></span>

  - <span data-ttu-id="fb143-143">**Exchange UM-Bereitstellung.**</span><span class="sxs-lookup"><span data-stu-id="fb143-143">**Exchange UM deployment.**</span></span> <span data-ttu-id="fb143-144">Diese Referenztopologie umfasst einen Exchange Unified Messaging (um)-Server, auf dem Microsoft Exchange Server ausgeführt wird, nicht lync Server.</span><span class="sxs-lookup"><span data-stu-id="fb143-144">This reference topology includes an Exchange Unified Messaging (UM) Server, which runs Microsoft Exchange Server, not Lync Server.</span></span>
    
    <span data-ttu-id="fb143-145">Ausführliche Informationen zu Exchange um finden Sie unter [Planen der Exchange Unified Messaging-Integration in lync Server 2013](lync-server-2013-planning-for-exchange-unified-messaging-integration.md) und [gehostete Exchange Unified Messaging-Integration in lync Server 2013](lync-server-2013-hosted-exchange-unified-messaging-integration.md) in der Planning-Dokumentation.</span><span class="sxs-lookup"><span data-stu-id="fb143-145">For details about Exchange UM, see [Planning for Exchange Unified Messaging integration in Lync Server 2013](lync-server-2013-planning-for-exchange-unified-messaging-integration.md) and [Hosted Exchange Unified Messaging integration in Lync Server 2013](lync-server-2013-hosted-exchange-unified-messaging-integration.md) in the Planning documentation.</span></span>

  - <span data-ttu-id="fb143-146">**Office Web Apps Server.**</span><span class="sxs-lookup"><span data-stu-id="fb143-146">**Office Web Apps Server.**</span></span> <span data-ttu-id="fb143-147">Es wird empfohlen, in jeder Organisation, in der der Webkonferenzdienst verwendet wird, einen Office Web Apps Server oder eine Office Web Apps-Serverfarm bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="fb143-147">We recommend deploying an Office Web Apps Server or Office Web Apps Server farm in every organization that uses web conferencing.</span></span> <span data-ttu-id="fb143-148">Mit Office Web Apps Server können PowerPoint-Folien in Webkonferenzen präsentiert werden.</span><span class="sxs-lookup"><span data-stu-id="fb143-148">Office Web Apps Server makes it possible for PowerPoint slides to be presented in web conferences.</span></span> <span data-ttu-id="fb143-149">Weitere Informationen finden Sie unter [Konfigurieren der Integration in Office Web Apps Server und lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="fb143-149">For more information, see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

<span data-ttu-id="fb143-150"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fb143-150"></div>

<span> </span>

</div>

</div>

</span></span></div>

