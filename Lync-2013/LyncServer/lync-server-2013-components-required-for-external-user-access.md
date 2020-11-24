---
title: 'Lync Server 2013: Erforderliche Komponenten für den Zugriff durch externe Benutzer'
description: 'Lync Server 2013: Komponenten, die für den Zugriff durch externe Benutzer erforderlich sind.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components required for external user access
ms:assetid: 2d0f9817-14e7-4109-95dc-62420e3c29e2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425779(v=OCS.15)
ms:contentKeyID: 48183711
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d75ef0c7f2000353a35acefa0b177c90bdcc879b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394214"
---
# <a name="components-required-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="14403-103">Erforderliche Komponenten für den Zugriff durch externe Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14403-103">Components required for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="14403-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="14403-104">

<span> </span></span></span>

<span data-ttu-id="14403-105">_**Letztes Änderungsdatum des Themas:** 2014-05-29_</span><span class="sxs-lookup"><span data-stu-id="14403-105">_**Topic Last Modified:** 2014-05-29_</span></span>

<span data-ttu-id="14403-106">Die meisten Edgekomponenten werden in einem Umkreisnetzwerk bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="14403-106">Most Edge components are deployed in a perimeter network.</span></span> <span data-ttu-id="14403-107">Die folgenden Komponenten bilden die Edge-Topologie des Umkreisnetzwerks.</span><span class="sxs-lookup"><span data-stu-id="14403-107">The following components make up the edge topology of the perimeter network.</span></span> <span data-ttu-id="14403-108">Sofern nicht anders angegeben, sind die Komponenten Teil der [Szenarien für den Zugriff durch externe Benutzer in lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) und befinden sich im Umkreisnetzwerk.</span><span class="sxs-lookup"><span data-stu-id="14403-108">Except where noted, the components are part of the [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md) and are in the perimeter network.</span></span> <span data-ttu-id="14403-109">Zu den Edgekomponenten gehören:</span><span class="sxs-lookup"><span data-stu-id="14403-109">Edge components include the following:</span></span>

  - <span data-ttu-id="14403-110">Edge Servers</span><span class="sxs-lookup"><span data-stu-id="14403-110">Edge Servers</span></span>

  - <span data-ttu-id="14403-111">Reverse proxies</span><span class="sxs-lookup"><span data-stu-id="14403-111">Reverse proxies</span></span>

  - <span data-ttu-id="14403-112">Firewalls</span><span class="sxs-lookup"><span data-stu-id="14403-112">Firewalls</span></span>

  - <span data-ttu-id="14403-113">Directors (optional und logisch im internen Netzwerk angeordnet)</span><span class="sxs-lookup"><span data-stu-id="14403-113">Directors (optional, and logically located on the internal network)</span></span>

  - <span data-ttu-id="14403-114">Lastenausgleich für skalierte Edgetopologien (entweder DNS-Lastenausgleich oder Hardwaregerät zum Lastenausgleich)</span><span class="sxs-lookup"><span data-stu-id="14403-114">Load balancing for Scaled Edge Topologies (either DNS load balancing or a hardware load balancer)</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="14403-p102">Das Verfahren, für eine Schnittstelle den DNS-Lastenausgleich und für eine andere Schnittstelle ein Hardwaregerät zum Lastenausgleich zu verwenden, wird nicht unterstützt. Sie müssen entweder für beide Schnittstellen ein Hardwaregerät zum Lastenausgleich oder für beide Schnittstellen den DNS-Lastenausgleich verwenden.</span><span class="sxs-lookup"><span data-stu-id="14403-p102">Using DNS load balancing on one interface and hardware load balancing on the other is not supported. You must use hardware load balancing for both interfaces or DNS load balancing for both.</span></span>

    
    </div>

<div>

## <a name="edge-servers"></a><span data-ttu-id="14403-117">Edgeservers</span><span class="sxs-lookup"><span data-stu-id="14403-117">Edge Servers</span></span>

<span data-ttu-id="14403-118">Die Edgeserver senden und empfangen Netzwerkdatenverkehr für die Dienste, die von externen Benutzern bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="14403-118">The Edge Servers send and receive network traffic for the services offered by internal deployment by external users.</span></span> <span data-ttu-id="14403-119">Der Edgeserver führt die folgenden Dienste aus:</span><span class="sxs-lookup"><span data-stu-id="14403-119">The Edge Server runs the following services:</span></span>

  - <span data-ttu-id="14403-120">**Access-Edgedienst**   Der Access-Edgedienst stellt einen einzelnen vertrauenswürdigen Verbindungspunkt für ausgehende und eingehende SIP-Datenverkehr (Session Initiation Protocol) bereit.</span><span class="sxs-lookup"><span data-stu-id="14403-120">**Access Edge service**   The Access Edge service provides a single, trusted connection point for both outbound and inbound Session Initiation Protocol (SIP) traffic.</span></span>

  - <span data-ttu-id="14403-121">**Webkonferenz-Edgedienst**   Der Webkonferenz-Edgedienst ermöglicht externen Benutzern die Teilnahme an Besprechungen, die auf Ihrer internen lync Server 2013-Bereitstellung gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="14403-121">**Web Conferencing Edge service**   The Web Conferencing Edge service enables external users to join meetings that are hosted on your internal Lync Server 2013 deployment.</span></span>

  - <span data-ttu-id="14403-122">**A/V-Edgedienst**   Der A/V-Edgedienst ermöglicht externen Benutzern die Bereitstellung von Audio, Video, Anwendungsfreigabe und Dateiübertragung.</span><span class="sxs-lookup"><span data-stu-id="14403-122">**A/V Edge service**   The A/V Edge service makes audio, video, application sharing, and file transfer available to external users.</span></span> <span data-ttu-id="14403-123">Ihre Benutzer können Besprechungen mit externen Teilnehmern Audio und Video hinzufügen, und Sie können in Punkt-zu-Punkt-Sitzungen mithilfe von Audio und/oder Video direkt mit einem externen Benutzer kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="14403-123">Your users can add audio and video to meetings that include external participants, and they can communicate using audio and/or video directly with an external user in point-to-point sessions.</span></span> <span data-ttu-id="14403-124">Der A/V-Edgedienst bietet auch Unterstützung für die Desktopfreigabe und Dateiübertragung.</span><span class="sxs-lookup"><span data-stu-id="14403-124">The A/V Edge service also provides support for desktop sharing and file transfer.</span></span>

  - <span data-ttu-id="14403-125">**XMPP-Proxy Dienst**   Der XMPP-Proxy Dienst akzeptiert und sendet Nachrichten zu und von konfigurierten XMPP-Verbundpartnern.</span><span class="sxs-lookup"><span data-stu-id="14403-125">**XMPP Proxy service**   The XMPP Proxy service accepts and sends extensible messaging and presence protocol (XMPP) messages to and from configured XMPP Federated partners.</span></span>

<span data-ttu-id="14403-126">Autorisierte externe Benutzer können auf die Edgeserver zugreifen, um eine Verbindung mit ihrer internen lync Server 2013-Bereitstellung herzustellen, aber die Edgeserver bieten keine Möglichkeit für einen anderen Zugriff auf das interne Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="14403-126">Authorized external users can access the Edge Servers in order to connect to your internal Lync Server 2013 deployment, but the Edge Servers do not provide a means for any other access to the internal network.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="14403-127">Edgeserver werden für die Bereitstellung von Verbindungen für aktivierte lync-Clients und andere Microsoft Edge-Server bereitgestellt (wie in Verbundszenarien).</span><span class="sxs-lookup"><span data-stu-id="14403-127">Edge servers are deployed to provide connections for enabled Lync clients and other Microsoft Edge servers (as in federation scenarios).</span></span> <span data-ttu-id="14403-128">Sie sind nicht dafür vorgesehen, Verbindungen von anderen Endpunkt Client-oder Servertypen zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="14403-128">They are not designed to allow connections from other end point client or server types.</span></span> <span data-ttu-id="14403-129">Der XMPP-Gatewayserver kann bereitgestellt werden, um Verbindungen mit konfigurierten XMPP-Partnern zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="14403-129">The XMPP Gateway server can be deployed to allow connections with configured XMPP partners.</span></span> <span data-ttu-id="14403-130">Der Edge-Server und das XMPP-Gateway können nur Endpunkt Verbindungen von diesen Client-und Verbundtypen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="14403-130">The Edge server and XMPP Gateway can only support end point connections from these client and federation types.</span></span>



</div>

</div>

<div>

## <a name="reverse-proxy"></a><span data-ttu-id="14403-131">Reverseproxy</span><span class="sxs-lookup"><span data-stu-id="14403-131">Reverse Proxy</span></span>

<span data-ttu-id="14403-132">Der Reverseproxy ist für Folgendes erforderlich:</span><span class="sxs-lookup"><span data-stu-id="14403-132">The reverse proxy is required for the following:</span></span>

  - <span data-ttu-id="14403-133">So ermöglichen Sie Benutzern das Herstellen einer Verbindung mit Besprechungen oder Einwahlkonferenzen mithilfe einfacher URLs</span><span class="sxs-lookup"><span data-stu-id="14403-133">To allow users to connect to meetings or dial-in conferences using simple URLs</span></span>

  - <span data-ttu-id="14403-134">So aktivieren Sie externe Benutzer zum Herunterladen von Besprechungsinhalten</span><span class="sxs-lookup"><span data-stu-id="14403-134">To enable external users to download meeting content</span></span>

  - <span data-ttu-id="14403-135">So aktivieren Sie externe Benutzer zum Erweitern von Verteilergruppen</span><span class="sxs-lookup"><span data-stu-id="14403-135">To enable external users to expand distribution groups</span></span>

  - <span data-ttu-id="14403-136">So ermöglichen Sie Benutzern das Abrufen eines benutzerbasierten Zertifikats für die Clientzertifikat basierte Authentifizierung</span><span class="sxs-lookup"><span data-stu-id="14403-136">To allow the user to obtain a user-based certificate for client certificate based authentication</span></span>

  - <span data-ttu-id="14403-137">So aktivieren Sie Remotebenutzer zum Herunterladen von Dateien vom Adressbuch Server oder zum Übermitteln von Abfragen an den Adressbuch-Webabfrage Dienst</span><span class="sxs-lookup"><span data-stu-id="14403-137">To enable remote users to download files from the Address Book Server or to submit queries to the Address Book Web Query service</span></span>

  - <span data-ttu-id="14403-138">So ermöglichen Sie es Remotebenutzern, Updates für Client-und Geräte Software zu erhalten</span><span class="sxs-lookup"><span data-stu-id="14403-138">To enable remote users to obtain updates to client and device software</span></span>

  - <span data-ttu-id="14403-139">So aktivieren Sie mobile Geräte, um Front-End-Server, die Mobilitätsdienste anbieten, automatisch zu erkennen</span><span class="sxs-lookup"><span data-stu-id="14403-139">To enable mobile devices to automatically discover Front End Servers offering mobility services</span></span>

  - <span data-ttu-id="14403-140">So aktivieren Sie Push-Benachrichtigungen auf mobilen Geräten von Microsoft 365, Office 365 oder Apple Push Notification Services</span><span class="sxs-lookup"><span data-stu-id="14403-140">To enable push notifications to mobile devices from the Microsoft 365, Office 365, or Apple push notification services</span></span>

<span data-ttu-id="14403-141">Weitere Informationen zu Reverse-Proxys und den Anforderungen, die umgekehrte Proxys erfüllen müssen, finden Sie in den Details unter [Konfigurationsanforderungen für Reverse Proxy in lync Server 2013](lync-server-2013-configuration-requirements-for-reverse-proxy.md).</span><span class="sxs-lookup"><span data-stu-id="14403-141">For additional information related to reverse proxies and the requirements that reverse proxies must meet, see the details in [Configuration requirements for reverse proxy in Lync Server 2013](lync-server-2013-configuration-requirements-for-reverse-proxy.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="14403-142">Externe Benutzer benötigen keine VPN-Verbindung (virtuelles privates Netzwerk) mit Ihrer Organisation, um an der Kommunikation mit lync Server 2013 teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="14403-142">External users do not need a virtual private network (VPN) connection to your organization in order to participate in communications using Lync Server 2013.</span></span> <span data-ttu-id="14403-143">Wenn Sie in Ihrer Organisation VPN-Technologie implementiert haben und Ihre Benutzer das VPN für lync verwenden, können Mediendatenverkehr (wie Videokonferenzen) beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="14403-143">If you have implemented VPN technology in your organization and your users use the VPN for Lync, media traffic (such as video conferencing) can be adversely affected.</span></span> <span data-ttu-id="14403-144">Sie sollten die Bereitstellungeines Mediums für Mediendatenverkehr in Frage stellen, um die Verbindung mit dem AV Edge-Dienst direkt herzustellen und das VPN zu umgehen.</span><span class="sxs-lookup"><span data-stu-id="14403-144">You should consider providing a means for media traffic to connect to the AV Edge service directly and bypass the VPN.</span></span> <span data-ttu-id="14403-145">Ausführliche Informationen finden Sie im NextHop-Blog Artikel "Aktivieren von lync Media zur Umgehung eines VPN-Tunnels" unter <A href="https://go.microsoft.com/fwlink/p/?linkid=256532">https://go.microsoft.com/fwlink/p/?LinkId=256532</A> .</span><span class="sxs-lookup"><span data-stu-id="14403-145">For details, see the NextHop Blog article, “Enabling Lync Media to Bypass a VPN Tunnel,” at <A href="https://go.microsoft.com/fwlink/p/?linkid=256532">https://go.microsoft.com/fwlink/p/?LinkId=256532</A>.</span></span>



</div>

</div>

<div>

## <a name="firewall"></a><span data-ttu-id="14403-146">Firewall</span><span class="sxs-lookup"><span data-stu-id="14403-146">Firewall</span></span>

<span data-ttu-id="14403-147">Sie können Ihre Edge-Topologie nur mit einer externen Firewall oder mit externen und internen Firewalls bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="14403-147">You can deploy your edge topology with only an external firewall or both external and internal firewalls.</span></span> <span data-ttu-id="14403-148">Zu den Szenarien-Architekturen gehören zwei Firewalls.</span><span class="sxs-lookup"><span data-stu-id="14403-148">The scenario architectures include two firewalls.</span></span> <span data-ttu-id="14403-149">Die Verwendung von zwei Firewalls ist die empfohlene Vorgehensweise, da Sie ein striktes Routing von einem Netzwerkrand zum anderen gewährleistet und ihre interne Bereitstellung hinter zwei Firewall-Ebenen schützt.</span><span class="sxs-lookup"><span data-stu-id="14403-149">Using two firewalls is the recommended approach because it ensures strict routing from one network edge to the other, and it protects your internal deployment behind two levels of firewall.</span></span>

</div>

<div>

## <a name="director"></a><span data-ttu-id="14403-150">Director</span><span class="sxs-lookup"><span data-stu-id="14403-150">Director</span></span>

<span data-ttu-id="14403-151">Bei einem Director handelt es sich um eine separate, optionale Serverrolle in lync Server 2013, in der keine Benutzerkonten zu Hause sind, oder Anwesenheits-oder Konferenzdienste bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="14403-151">A Director is a separate, optional server role in Lync Server 2013 that does not home user accounts, or provide presence or conferencing services.</span></span> <span data-ttu-id="14403-152">Sie fungiert als interner Server für den nächsten Hop, auf dem ein Edgeserver eingehenden SIP-Datenverkehr für interne Server weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="14403-152">It serves as an internal next hop server to which an Edge Server routes inbound SIP traffic destined for internal servers.</span></span> <span data-ttu-id="14403-153">Der Director authentifiziert eingehende Anforderungen und leitet Sie an den privaten Pool oder Server des Benutzers weiter.</span><span class="sxs-lookup"><span data-stu-id="14403-153">The Director preauthenticates inbound requests and redirects them to the user’s home pool or server.</span></span> <span data-ttu-id="14403-154">Durch die Vorauthentifizierung beim Director können Sie Anforderungen aus Benutzerkonten, die für die Bereitstellung unbekannt sind, ablegen.</span><span class="sxs-lookup"><span data-stu-id="14403-154">By preauthenticating at the Director, you can drop requests from user accounts that are unknown to the deployment.</span></span>

<span data-ttu-id="14403-155">Ein Director hilft beim Isolieren von Standard Edition-Servern und Front-End-Servern in Enterprise Edition-Front-End-Pools vor böswilligem Datenverkehr wie DOS-Attacken (Denial-of-Service).</span><span class="sxs-lookup"><span data-stu-id="14403-155">A Director helps insulate Standard Edition servers and Front End Servers in Enterprise Edition Front End pools from malicious traffic such as denial-of-service (DoS) attacks.</span></span> <span data-ttu-id="14403-156">Wenn das Netzwerk bei einem solchen Angriff mit einem ungültigen externen Datenverkehr überflutet wird, endet der Datenverkehr beim Director.</span><span class="sxs-lookup"><span data-stu-id="14403-156">If the network is flooded with invalid external traffic in such an attack, the traffic ends at the Director.</span></span> <span data-ttu-id="14403-157">Ausführliche Informationen zur Verwendung von Directors finden Sie unter [Szenarien für den Director in lync Server 2013](lync-server-2013-scenarios-for-the-director.md).</span><span class="sxs-lookup"><span data-stu-id="14403-157">For details about the use of Directors, see [Scenarios for the Director in Lync Server 2013](lync-server-2013-scenarios-for-the-director.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="14403-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="14403-158">See Also</span></span>


[<span data-ttu-id="14403-159">Anforderungen an das Hardwaregerät zum Lastenausgleich für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="14403-159">Hardware load balancer requirements for Lync Server 2013</span></span>](lync-server-2013-hardware-load-balancer-requirements.md)  
  

<span data-ttu-id="14403-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="14403-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

