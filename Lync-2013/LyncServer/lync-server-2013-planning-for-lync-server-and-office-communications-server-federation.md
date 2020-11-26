---
title: Planen der lync Server-und Office Communications Server-Föderation
description: Planen der lync Server-und Office Communications Server-Föderation
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Lync Server and Office Communications Server federation
ms:assetid: c9eaf06b-054f-41a4-ad0c-499400d6c4c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205335(v=OCS.15)
ms:contentKeyID: 48185640
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5d7385b8fde27446fb0648802544a8840a0f6276
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424541"
---
# <a name="planning-for-lync-server-2013-and-office-communications-server-federation"></a><span data-ttu-id="d6d0f-103">Planen der lync Server 2013-und Office Communications Server-Föderation</span><span class="sxs-lookup"><span data-stu-id="d6d0f-103">Planning for Lync Server 2013 and Office Communications Server federation</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d6d0f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d6d0f-104">

<span> </span></span></span>

<span data-ttu-id="d6d0f-105">_**Letztes Änderungsdatum des Themas:** 2013-02-13_</span><span class="sxs-lookup"><span data-stu-id="d6d0f-105">_**Topic Last Modified:** 2013-02-13_</span></span>

<span data-ttu-id="d6d0f-106">Der Verbund zwischen Microsoft lync Server 2013, lync Server 2010 und Office Communications Server unterstützt Peer-to-Peer-und Mehrparteienkommunikation.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-106">Federation between Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server supports peer-to-peer and multi-party communications.</span></span> <span data-ttu-id="d6d0f-107">Peer-to-Peer-Unterhaltungen können an mehr Parteien Unterhaltungen eskaliert werden, was zu Ad-hoc-Besprechungen führt.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-107">Peer-to-peer conversations can be escalated to multi-party conversations, allowing for ad hoc meetings.</span></span> <span data-ttu-id="d6d0f-108">Besprechungen – Webkonferenzen oder Audio/visuelle Konferenzen – können so geplant werden, dass Sie Kontakte innerhalb Ihrer Organisation sowie Kontakte in Partner einbeziehen, mit denen Sie eine Föderation aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-108">Meetings – Web conferencing or audio/visual conferences – can be scheduled to include contacts inside your organization as well as contacts in partners that you federate with.</span></span>

<span data-ttu-id="d6d0f-109">Federation erschien zunächst in Microsoft Office Live Communications Server 2005 und unterstützte eine Art von Föderation, direkte Föderation.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-109">Federation first appeared in Microsoft Office Live Communications Server 2005 and supported one kind of federation, Direct Federation.</span></span> <span data-ttu-id="d6d0f-110">Für den direkten Verbund mussten Sie die SIP-Domäne (Session Initiation Protocol) des Partner Verbandes und den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Edge-Servers des Partners kennen.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-110">Direct Federation required you to know the federation partner’s session initiation protocol (SIP) domain and the fully qualified domain name (FQDN) of the partner’s Edge Server.</span></span> <span data-ttu-id="d6d0f-111">Mit Live Communications Server 2005 mit SP1 wurden zusätzliche Föderations Typen eingeführt, die alle DNS-SRV-Einträge (Domain Name System) benötigten, die von dem Partnerverbund zum Auffinden des Edgeserver veröffentlicht wurden.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-111">Live Communications Server 2005 with SP1 introduced additional federation types, all of which required domain name system (DNS) SRV records to be published by the federated partner to locate their Edge Server.</span></span> <span data-ttu-id="d6d0f-112">Die Terminologie für diese Version lautete:</span><span class="sxs-lookup"><span data-stu-id="d6d0f-112">The terminology for that release was:</span></span>

  - <span data-ttu-id="d6d0f-113">*Erweiterte Föderation öffnen*: akzeptieren Sie einen beliebigen SIP-Domänennamen, und verwenden Sie DNS SRV zum Auffinden des Partner-Edge-Servers.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-113">*Open Enhanced Federation*: Accept any SIP domain name and use DNS SRV to locate the partner Edge Server</span></span>

  - <span data-ttu-id="d6d0f-114">*Erweiterte Föderation*: Konfigurieren Sie den SIP-Domänennamen des Partners als Verbundpartner für Ihre Organisation, und verwenden Sie DNS SRV zum Auffinden des Partner-Edge-Servers.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-114">*Enhanced Federation*: Configure the partner’s SIP domain name as a federation partner for your organization and use DNS SRV to find the partner Edge Server</span></span>

  - <span data-ttu-id="d6d0f-115">*Direkter Verbund*: Konfigurieren Sie den SIP-Domänennamen und den FQDN des Partners auf dem Edgeserver des Partners.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-115">*Direct Federation*: Configure the partner’s SIP domain name and the FQDN to the partner’s Edge Server</span></span>

  - <span data-ttu-id="d6d0f-116">*Server Zulassungsliste*: akzeptieren einer beliebigen Domäne, verwenden von DNS SRV zum Auffinden des Edgeserver eines Hostinganbieter oder eines öffentlichen Instant Messaging (im)-Verbindungs Anbieters</span><span class="sxs-lookup"><span data-stu-id="d6d0f-116">*Server Allow List*: Accept any domain, use DNS SRV to find the Edge Server of a hosting provider or a public instant messaging (IM) connectivity provider</span></span>

<span data-ttu-id="d6d0f-117">Microsoft Office Communications Server 2007 hat aktualisierte Namen für Verbundtypen eingeführt, um besser zu definieren, was die einzelnen Föderations Typen tatsächlich erreicht haben:</span><span class="sxs-lookup"><span data-stu-id="d6d0f-117">Microsoft Office Communications Server 2007 introduced updated naming for federation types to better define what each federation type actually accomplished:</span></span>

  - <span data-ttu-id="d6d0f-118">Open Enhanced Federation wurde als *erkannte Partner Domäne* bekannt</span><span class="sxs-lookup"><span data-stu-id="d6d0f-118">Open Enhanced Federation became known as *Discovered Partner Domain*</span></span>

  - <span data-ttu-id="d6d0f-119">Erweiterte Föderation wurde als *zugelassene Partner Domäne* bekannt</span><span class="sxs-lookup"><span data-stu-id="d6d0f-119">Enhanced Federation became known as *Allowed Partner Domain*</span></span>

  - <span data-ttu-id="d6d0f-120">Der direkte Verbund wurde als *zugelassener Partner Server* bekannt.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-120">Direct Federation became known as *Allowed Partner Server*</span></span>

  - <span data-ttu-id="d6d0f-121">Server Zulassungsliste wurde als *Hostinganbieter* und *Öffentlicher Chat Anbieter* bekannt.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-121">Server Allow List became known as *Hosting Provider* and *Public IM Provider*</span></span>

<span data-ttu-id="d6d0f-122">Microsoft lync Server 2010 hat eine schmalere Definition des Hostinganbieter-Anbieters in Übereinstimmung mit Microsoft lync Online 2010 und Microsoft Office 365 eingeführt und außerdem der gleichen zulässigen Liste unterzogen, die durch den Föderations zugelassene Partner Domäne definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-122">Microsoft Lync Server 2010 introduced a narrower definition of Hosting Provider in accordance with Microsoft Lync Online 2010 and Microsoft Office 365 and also made it subject to the same allowed list defined by the Allowed Partner Domain federation type.</span></span>

<span data-ttu-id="d6d0f-123">Wenn Sie den Verbund zwischen Microsoft lync Server 2013, lync Server 2010 und Office Communications Server aktivieren, werden die Edgeserver und Reverse Proxys verwendet, um die von Ihnen definierten Regeln und zulässigen Partnerdomänen zu erzwingen.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-123">Enabling federation between Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server uses the Edge Servers and reverse proxies to enforce the rules and allowed partner domains that you define.</span></span> <span data-ttu-id="d6d0f-124">Aus Planungssicht erfordert die Zusammenarbeit mit anderen lync-Servern in Office Communications Server Folgendes:</span><span class="sxs-lookup"><span data-stu-id="d6d0f-124">From a planning perspective, federating with other Lync Server, Office Communications Server requires the following:</span></span>

  - <span data-ttu-id="d6d0f-125">Aktivieren der Föderation im Topologie-Generator</span><span class="sxs-lookup"><span data-stu-id="d6d0f-125">Enable federation in Topology Builder.</span></span> <span data-ttu-id="d6d0f-126">Ausführliche Informationen finden Sie im Bereitstellungs Thema [Konfigurieren von SIP Federation, XMPP Federation und Public Instant Messaging in lync Server 2013](lync-server-2013-configuring-sip-federation-xmpp-federation-and-public-instant-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="d6d0f-126">For details, see the Deployment topic [Configuring SIP federation, XMPP federation and public instant messaging in Lync Server 2013](lync-server-2013-configuring-sip-federation-xmpp-federation-and-public-instant-messaging.md).</span></span>

  - <span data-ttu-id="d6d0f-127">Ermitteln Sie Ihre Anforderungen für die Föderationsdomänen Ermittlung:</span><span class="sxs-lookup"><span data-stu-id="d6d0f-127">Determine your requirements for federated domain discovery:</span></span>
    
      - <span></span>  
        <span data-ttu-id="d6d0f-128">Für die manuelle Konfiguration von Federation müssen Sie über den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Edge-Servers des Partners und des Domänennamens oder des Online Domänennamens verfügen, der in der lync Server-Systemsteuerung, in der **Föderation und im externen Zugriff**, **SIP-Verbunddomänen** eingegeben wird.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-128">For manual configuration of federation, you must have the fully qualified domain name (FQDN) of the partner’s Edge Server and domain name, or online domain name, which is entered in the Lync Server Control Panel, **Federation and External Access**, **SIP Federated Domains**.</span></span> <span data-ttu-id="d6d0f-129">Erstellen Sie eine **neue** Richtlinie, oder **Bearbeiten** Sie eine vorhandene Richtlinie, damit Domänen nach FQDN zugelassen oder blockiert werden.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-129">Create a **New** policy or **Edit** an existing policy to either allow or block domains by FQDN.</span></span>
        
        <div>
        

        > [!WARNING]
        > <span data-ttu-id="d6d0f-130">Die manuelle Konfiguration des Edge-Servers eines Verbundpartners ist für den Fall anfällig, dass der Partner die IP-Adresse seines Edge-Servers ändert.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-130">Manual configuration of a federation partner’s Edge Server is prone to failure in the event that the partner changes the IP address of their Edge Server.</span></span>

        
        </div>
        
        <div>
        

        > [!NOTE]
        > <span data-ttu-id="d6d0f-131">Für <STRONG>neue SIP-Verbunddomänen</STRONG>müssen Sie den <STRONG>Domänennamen (oder den FQDN)</STRONG> für Microsoft lync Online und Microsoft 365 oder Office 365 angeben.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-131">For <STRONG>New SIP Federated Domains</STRONG>, you must provide the <STRONG>Domain name (or FQDN)</STRONG> for Microsoft Lync Online and Microsoft 365 or Office 365.</span></span> <span data-ttu-id="d6d0f-132">Für Microsoft lync Server 2013, lync Server 2010 und Office Communications Server müssen Sie auch einen <STRONG>Access Edge Service (FQDN)</STRONG> bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-132">For Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server you must also provide an <STRONG>Access Edge service (FQDN)</STRONG></span></span>

        
        </div>
    
      - <span></span>  
        <span data-ttu-id="d6d0f-133">Für entdeckten Partnerverbund, in dem Partner ihren Edgeserver entdecken können, erstellen Sie einen SRV-Eintrag in Ihrem externen DNS- \_ sipfederationtls. \_ TCP.contoso.com – verweist auf den Port 5061 und den Host (A)-Eintrag Ihres Edge-Servers</span><span class="sxs-lookup"><span data-stu-id="d6d0f-133">For discovered partner federation, where partners can discover your Edge Server, you create an SRV record in your external DNS - \_sipfederationtls.\_tcp.contoso.com – which points to the port 5061 and the host (A) record of your Edge Server</span></span>
        
        <div>
        

        > [!IMPORTANT]
        > <span data-ttu-id="d6d0f-134">Wenn Sie Microsoft lync Mobile-Clients auf Windows Phone oder Apple iPhone, iPad oder anderen Apple-Geräten unterstützen und den Push-Benachrichtigungsdienst oder den Push-Benachrichtigungsdienst verwenden, müssen Sie _sipfederationtls. _tcp planen.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-134">If you are supporting Microsoft Lync Mobile clients on either Windows Phone or Apple iPhone, iPad, or other Apple devices and are using the Push Notification Service or Push Notification Service, you must plan for _sipfederationtls._tcp.</span></span> <span data-ttu-id="d6d0f-135">&lt;SIP-Domänen- &gt; SRV-Einträge für jede SIP-Domäne, auf der Sie lync Mobile-Clients haben.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-135">&lt;SIP domain&gt; SRV records for each SIP domain that you have Lync Mobile clients.</span></span> <span data-ttu-id="d6d0f-136">Android und Nokia Symbian lync Mobile verwenden keine Push-Benachrichtigung und unterliegen nicht dieser Anforderung.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-136">Android and Nokia Symbian Lync Mobile do not use push notification and are not subject to this requirement.</span></span>

        
        </div>

  - <span data-ttu-id="d6d0f-137">Konfigurieren von Richtlinien für den externen Benutzer Zugriff zur Unterstützung von Verbunddomänen</span><span class="sxs-lookup"><span data-stu-id="d6d0f-137">Configure external user access policies to support federated domains</span></span>

  - <span data-ttu-id="d6d0f-138">Öffnen Sie die Firewall-Ports für SIP (Session Initiation Protocol), Webkonferenzen und Audio/visuell, um die von Ihnen aktivierte Föderation oder Kontakte aufnehmen zu können.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-138">Open firewall ports for session initiation protocol (SIP), web conferencing and audio/visual to accommodate the federation or contacts that you are enabling.</span></span> <span data-ttu-id="d6d0f-139">Ausführliche Informationen finden Sie unter: [ermitteln externer A/V-Firewall-und Portanforderungen für lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)</span><span class="sxs-lookup"><span data-stu-id="d6d0f-139">For details, see: [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)</span></span>

<span data-ttu-id="d6d0f-140">Die folgenden Informationen unterstützen Sie bei der Definition der Zertifikat-, Port/Protokoll-und DNS-Anforderungen für den Verbund mit Microsoft lync Server 2013 und lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-140">The following information will aid you in defining the certificate, port/protocol and DNS requirements for federation with Microsoft Lync Server 2013 and Lync Server 2010.</span></span>

<span data-ttu-id="d6d0f-141">Die Planung für Zertifikate, Firewall-und Port/Protocol-Anforderungen und DNS-Anforderungen ist in der Regel ein geradliniger Prozess, wenn Sie Ihre Microsoft lync Server 2013-Edgeserver geplant oder bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-141">Planning for certificates, firewall and port/protocol requirements and DNS requirements is generally a straight forward process if you have planned or deployed your Microsoft Lync Server 2013 Edge Servers.</span></span> <span data-ttu-id="d6d0f-142">Da es sich bei der Föderation um ein zusätzliches Feature handelt, das den vorhandenen Edgeserver verwendet, werden die Planungsanforderungen in der Regel von der Planung und Bereitstellung des Edge-Servers erfüllt.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-142">Because federation is an additional feature that uses the existing Edge Server, the planning requirements are generally met by the Edge Server planning and deployment.</span></span> <span data-ttu-id="d6d0f-143">Verwenden Sie die folgenden Tabellen, um festzustellen, ob Ihre Anforderungen erfüllt sind, und nehmen Sie dementsprechend Änderungen an Port/Protokoll und DNS vor.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-143">You should use the following tables to determine that your requirements are met and make changes in port/protocol and DNS accordingly.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="d6d0f-144">Wenn Sie über einen Pool von Edge-Servern verfügen und mit lync Server 2013-oder lync Server 2010-Partnern zusammenarbeiten, können Sie entweder den DNS-Lastenausgleich oder Hardwarelastenausgleichs auf der internen und externen Seite der Edgeserver verwenden.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-144">If you have a pool of Edge Servers and are federating with Lync Server 2013 or Lync Server 2010 partners, then you can use either DNS load balancing or hardware load balancers on the internal and external facing sides of the Edge Servers.</span></span> <span data-ttu-id="d6d0f-145">Wenn Sie mit Office Communications Server 2007 oder Office Communications Server 2007 R2 eine Föderation durchführen, bietet der Hardwarelastenausgleich eine Failover-Unterstützung für den Fall eines Edgeserver.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-145">If you are federating with Office Communications Server 2007 or Office Communications Server 2007 R2, hardware load balancing will provide failover support in the event of an Edge Server.</span></span> <span data-ttu-id="d6d0f-146">Office Communications Server 2007 und Office Communications Server 2007 R2 sind nicht für den DNS-Lastenausgleich bekannt.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-146">Office Communications Server 2007 and Office Communications Server 2007 R2 are not DNS load balancing aware.</span></span> <span data-ttu-id="d6d0f-147">Die Partner-Edgeserver richten die Kommunikation mit dem ersten Edgeserver in Ihrem Pool ein, der antwortet.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-147">The partner Edge Servers will establish communication with the first Edge Server in your pool that responds.</span></span> <span data-ttu-id="d6d0f-148">Wenn dieser Edge-Server ausfällt, wird die Kommunikation nicht automatisch Failover.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-148">If that Edge Server fails, communication does not automatically failover.</span></span>



</div>

<span data-ttu-id="d6d0f-149">Die Zertifikatanforderungen werden in der Regel durch die Planung von Zertifikaten für den ausgewählten Edgeserver oder den Pooled Edge Server-Plan erfüllt.</span><span class="sxs-lookup"><span data-stu-id="d6d0f-149">Certificate requirements are typically met through the planning of certificates for your chosen Edge Server or pooled Edge Server plan.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d6d0f-150">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d6d0f-150">In This Section</span></span>

  - [<span data-ttu-id="d6d0f-151">Zusammenfassung des Zertifikats – SIP, XMPP Federation und Public Instant Messaging in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d6d0f-151">Certificate summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-sip-xmpp-federation-and-public-instant-messaging.md)

  - [<span data-ttu-id="d6d0f-152">Port Zusammenfassung – SIP, XMPP Federation und Public Instant Messaging in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d6d0f-152">Port summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-port-summary-sip-xmpp-federation-and-public-instant-messaging.md)

  - [<span data-ttu-id="d6d0f-153">DNS-Zusammenfassung – SIP, XMPP Federation und Public Instant Messaging in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d6d0f-153">DNS summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-dns-summary-sip-xmpp-federation-and-public-instant-messaging.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d6d0f-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6d0f-154">See Also</span></span>


[<span data-ttu-id="d6d0f-155">Konfigurieren von Richtlinien zur Steuerung des Partnerbenutzerzugriffs in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d6d0f-155">Configure policies to control federated user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-federated-user-access.md)  


[<span data-ttu-id="d6d0f-156">Szenarien für den Zugriff durch externe Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d6d0f-156">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="d6d0f-157">Ermitteln der Anforderungen für externe A/V-Firewalls und Ports für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d6d0f-157">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  
[<span data-ttu-id="d6d0f-158">Ermitteln von DNS-Anforderungen für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d6d0f-158">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)  


[<span data-ttu-id="d6d0f-159">Verwalten der Konfiguration des Zugriffsedge für Ihre Organisation in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d6d0f-159">Manage Access Edge Configuration for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-access-edge-configuration-for-your-organization.md)  
[<span data-ttu-id="d6d0f-160">Verwalten von SIP-Partnerdomänen für eine Organisation in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d6d0f-160">Manage SIP federated domains for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-domains-for-your-organization.md)  
[<span data-ttu-id="d6d0f-161">Verwalten von SIP-Partnerverbundanbietern für eine Organisation in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d6d0f-161">Manage SIP federated providers for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-providers-for-your-organization.md)  
  

<span data-ttu-id="d6d0f-162"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d6d0f-162"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

