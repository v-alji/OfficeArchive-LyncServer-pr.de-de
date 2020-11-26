---
title: 'Lync Server 2013: Topologien und Komponenten für Mobilität'
description: 'Lync Server 2013: Topologien und Komponenten für Mobilität.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Topologies and components for mobility
ms:assetid: be3cae7a-095d-4785-91ba-6fac99eba92a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690037(v=OCS.15)
ms:contentKeyID: 48185282
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 731991c3395bd3014270430483c6047dd5487185
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440867"
---
# <a name="topologies-and-components-for-mobility-in-lync-server-2013"></a><span data-ttu-id="f2386-103">Topologien und Komponenten für Mobilität in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2386-103">Topologies and components for mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f2386-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f2386-104">

<span> </span></span></span>

<span data-ttu-id="f2386-105">_**Letztes Änderungsdatum des Themas:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="f2386-105">_**Topic Last Modified:** 2013-02-17_</span></span>

    The information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="f2386-106">Zur Unterstützung von lync Mobile-Anwendungen auf mobilen Geräten bietet lync Server 2013 drei Dienste: lync Server 2013 MCX Mobility Service, lync Server 2013 AutoErmittlungsdienst und lync Server 2013-Push-Benachrichtigungsdienst.</span><span class="sxs-lookup"><span data-stu-id="f2386-106">To support Lync mobile applications on mobile devices, Lync Server 2013 provides three services: Lync Server 2013 Mcx Mobility Service, Lync Server 2013 Autodiscover Service, and Lync Server 2013 Push Notification Service.</span></span> <span data-ttu-id="f2386-107">Die kumulativen Updates für lync Server 2013: Februar 2013 fügt einen kostenlosen, aber erweiterten Dienst für lync 2013-Mobile Clients hinzu – Mobilitätsunterstützung durch die Verwendung der Unified Communications Web-API oder UCWA.</span><span class="sxs-lookup"><span data-stu-id="f2386-107">The Cumulative Updates for Lync Server 2013: February 2013 adds a complimentary, but advanced, service for Lync 2013 Mobile clients—mobility support through the use of the Unified Communications Web API, or UCWA.</span></span> <span data-ttu-id="f2386-108">In diesem Abschnitt werden diese Komponenten kurz beschrieben und die lync Server 2013-Topologien identifiziert, die die Mobilität unterstützen.</span><span class="sxs-lookup"><span data-stu-id="f2386-108">This section briefly describes these components and identifies the Lync Server 2013 topologies that support mobility.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f2386-109">Mobilitätsdienste stehen auch in hybridbereitstellungen zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="f2386-109">Mobility services are also available in hybrid deployments.</span></span> <span data-ttu-id="f2386-110">Sie müssen keine Dienste zur Unterstützung der Mobilität bereitstellen, wenn Ihre Benutzer online sind.</span><span class="sxs-lookup"><span data-stu-id="f2386-110">You are not required to deploy services for supporting mobility if your users are homed online.</span></span> <span data-ttu-id="f2386-111">Sie müssen eine Einstellung für den AutoErmittlungsdienst definieren, damit Mobile Benutzer ihre Online Identität finden können.</span><span class="sxs-lookup"><span data-stu-id="f2386-111">You do need to define a setting for the Autodiscover Service to enable mobile users to find their online identity.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="f2386-112">Wenn Sie eine externe Benutzerkonnektivität planen (beispielsweise Föderation, Zugriff auf externe Benutzer oder Mobilitätsfeatures), müssen Sie Edgeserver mit dem Standard Edition-Server und dem Front-End-Server oder dem Front-End-Pool verwenden.</span><span class="sxs-lookup"><span data-stu-id="f2386-112">If you are planning any external user connectivity (for example, federation, external user access, or mobility features), you must use Edge Servers with Standard Edition server and the Front End Server or Front End pool.</span></span> <span data-ttu-id="f2386-113">Der Standard Edition-Server und der Front-End-Server oder der Front-End-Pool verfügen nicht über die erforderlichen Komponenten, um externen Benutzern den Zugriff auf Ihre interne Bereitstellung zu ermöglichen, oder für die interne Bereitstellung, um mit Ihren externen Benutzern zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="f2386-113">The Standard Edition server and the Front End Server or Front End pool do not have the necessary components to enable external users to access your internal deployment, or for the internal deployment to communicate with your external users.</span></span> <span data-ttu-id="f2386-114">Für alle Szenarien, die externe Benutzer einbeziehen, die mit internen Benutzern zusammenarbeiten oder mit Ihnen kommunizieren, einschließlich Mobilität, müssen Sie mindestens einen Edgeserver und einen Reverse-Proxy bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f2386-114">For all scenarios that include external users collaborating or communicating with internal users, including mobility, you must deploy at least one Edge Server and one reverse proxy.</span></span><BR><span data-ttu-id="f2386-115">Bei der <EM>Push-Benachrichtigung</EM> wird ein Föderations für die lync Online-Dienste verwendet, die das Push Notification Clearing House (PNCH) hostet.</span><span class="sxs-lookup"><span data-stu-id="f2386-115"><EM>Push notification</EM> uses a type of federation to the Lync Online services, which hosts the Push Notification Clearing House (PNCH).</span></span> <span data-ttu-id="f2386-116">Die Push-Benachrichtigung bezieht sich auf die akustischen Benachrichtigungen, auf dem Bildschirm angezeigten Benachrichtigungen (Text) und auf Abzeichen, die von Anwendungen auf das Apple iPhone, iPad und Windows Phone übertragen werden, wenn das Mobile Gerät inaktiv ist.</span><span class="sxs-lookup"><span data-stu-id="f2386-116">Push notification refers to the sound alerts, on-screen alerts (text), and badges that are pushed by applications to the Apple iPhone, iPad, and Windows Phone, when the mobile device is inactive.</span></span> <span data-ttu-id="f2386-117">PNCH empfängt Push-Benachrichtigungen von lync Server.</span><span class="sxs-lookup"><span data-stu-id="f2386-117">PNCH receives push notifications from Lync Server.</span></span> <span data-ttu-id="f2386-118">Wenn PNCH eine Benachrichtigung über eine Nachricht erhält, leitet PNCH eine Benachrichtigung an mobile Clients über den Apple Push Notification Services oder den lync Server 2013-Push-Benachrichtigungsdienst weiter, der auf dem mobilen Client basiert, für den die Nachricht vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="f2386-118">When PNCH receives a notification of a message, PNCH forwards a notification to mobile clients through either the Apple Push Notification Services or Lync Server 2013 Push Notification Service, based on the mobile client that the message is intended for.</span></span> <span data-ttu-id="f2386-119">PNCH ist ein erforderlicher Dienst für diese mobilen Clients.</span><span class="sxs-lookup"><span data-stu-id="f2386-119">PNCH is a required service for these mobile clients.</span></span> <span data-ttu-id="f2386-120">Um eine Föderation zu lync online zu finden, verwendet PNCH Edgeserver und Zertifikate, um Vertraulichkeit und Authentifizierung, Richtlinien und ordnungsgemäß konfigurierte DNS-Einträge (Domain Name System) zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="f2386-120">To federate to Lync Online, PNCH uses Edge Servers and certificates to ensure confidentiality and authentication, policies, and correctly configured domain name system (DNS) records.</span></span> <span data-ttu-id="f2386-121">Die Nokia Symbian-und Android-basierten lync Mobile-Clients verwenden PNCH nicht.</span><span class="sxs-lookup"><span data-stu-id="f2386-121">Nokia Symbian and Android-based Lync Mobile clients do not use PNCH.</span></span> <span data-ttu-id="f2386-122">Details zum Planen und Bereitstellen von Edgeserver finden Sie unter <A href="lync-server-2013-planning-for-external-user-access.md">Planen des Zugriffs externer Benutzer in lync Server 2013</A> und <A href="lync-server-2013-deploying-external-user-access.md">Bereitstellen des Zugriffs externer Benutzer in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="f2386-122">For details about planning and deploying Edge Servers, see <A href="lync-server-2013-planning-for-external-user-access.md">Planning for external user access in Lync Server 2013</A> and <A href="lync-server-2013-deploying-external-user-access.md">Deploying external user access in Lync Server 2013</A>.</span></span><BR><span data-ttu-id="f2386-123">Die lync 2013-mobilen Clients für Apple-Geräte, die mit den kumulativen Updates für lync Server 2013 eingeführt wurden: Februar 2013 verwenden keine Push-Benachrichtigung mehr oder das Clearing House für Push-Benachrichtigungen (PNCH).</span><span class="sxs-lookup"><span data-stu-id="f2386-123">The Lync 2013 Mobile clients for Apple devices introduced with the Cumulative Updates for Lync Server 2013: February 2013 no longer use push notification or the push notification clearing house (PNCH).</span></span> <span data-ttu-id="f2386-124">Mobile lync 2013-Clients auf Windows Phone verwenden weiterhin die Push-Benachrichtigung und die (PNCH).</span><span class="sxs-lookup"><span data-stu-id="f2386-124">Lync 2013 Mobile clients on Windows Phone still use push notification and the (PNCH).</span></span>



</div>

<div>

## <a name="mobility-components"></a><span data-ttu-id="f2386-125">Mobilitätskomponenten</span><span class="sxs-lookup"><span data-stu-id="f2386-125">Mobility Components</span></span>

<span data-ttu-id="f2386-126">Die Dienste, die Mobilität unterstützen, sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f2386-126">The services that support mobility are as follows:</span></span>

  - <span data-ttu-id="f2386-127">**Lync Server 2013 Unified Communications Web-API (UCWA)**   Stellt Dienste für die Echtzeitkommunikation mit mobilen und Webclients in lync Server 2013 bereit.</span><span class="sxs-lookup"><span data-stu-id="f2386-127">**Lync Server 2013 Unified Communications Web API (UCWA)**   Provides services for real-time communications with mobile and web clients in Lync Server 2013.</span></span> <span data-ttu-id="f2386-128">Wenn Sie die kumulativen Updates für lync Server 2013: Februar 2013 auf dem Front-End-Server und Director bereitstellen, erstellt die Installation ein virtuelles Verzeichnis in den internen und externen Webdiensten (Ucwa).</span><span class="sxs-lookup"><span data-stu-id="f2386-128">When you deploy the Cumulative Updates for Lync Server 2013: February 2013 to the Front End Server and Director, the installation creates a virtual directory in the internal and external web services (Ucwa).</span></span> <span data-ttu-id="f2386-129">Eine Webkomponente, die Teil des virtuellen Verzeichnisses Ucwa ist, akzeptiert Anrufe von Ucwa-aktivierten Clients.</span><span class="sxs-lookup"><span data-stu-id="f2386-129">A web component that is part of the Ucwa virtual directory accepts calls from UCWA-enabled clients.</span></span> <span data-ttu-id="f2386-130">Die Client-apps kommunizieren über eine Ruhe-Schnittstelle für Anwesenheit, Kontakte, Instant Messaging, VoIP, Videokonferenzen und Zusammenarbeit.</span><span class="sxs-lookup"><span data-stu-id="f2386-130">The client apps communicate over a REST interface for presence, contacts, instant messaging, VoIP, video conferencing, and collaboration.</span></span> <span data-ttu-id="f2386-131">UCWA verwendet einen P-get-basierten Kanal, um Ereignisse wie einen eingehenden Anruf, eine eingehende Sofortnachricht oder eine Nachricht an die Client-App zu senden.</span><span class="sxs-lookup"><span data-stu-id="f2386-131">UCWA uses a P-GET based channel to send events, such as an incoming call, incoming instant message, or a message to the client app.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f2386-132"><EM>Ruhe</EM> Zustands-oder Repräsentations Statusübertragung, ist ein Software-Architekturstil für verteilte Systeme, der in vielen Formen weit verbreitet und für die Anforderungen von Webdiensten im Allgemeinen gut geeignet ist.</span><span class="sxs-lookup"><span data-stu-id="f2386-132"><EM>REST</EM> or representational state transfer, is a software architectural style for distributed systems that has been widely adopted in many forms and is well suited to the requirements of Web services in general.</span></span>

    
    </div>

  - <span data-ttu-id="f2386-133">**Lync Server 2013 Mobility Service (MCX)**   Dieser Dienst unterstützt lync-Funktionen wie Instant Messaging (im), Anwesenheitsinformationen und Kontakte auf mobilen Geräten.</span><span class="sxs-lookup"><span data-stu-id="f2386-133">**Lync Server 2013 Mobility Service (Mcx)**   This service supports Lync functionality, such as instant messaging (IM), presence, and contacts, on mobile devices.</span></span> <span data-ttu-id="f2386-134">Der Mobilitätsdienst ist auf jedem Front-End-Server in jedem Pool installiert, der die lync-Funktionalität auf mobilen Geräten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f2386-134">The Mobility Service is installed on every Front End Server in each pool that is to support Lync functionality on mobile devices.</span></span> <span data-ttu-id="f2386-135">Wenn Sie lync Server 2013 installieren, wird ein neues virtuelles Verzeichnis (MCX) sowohl auf der internen Website als auch auf der externen Website auf Ihren Front-End-Servern erstellt.</span><span class="sxs-lookup"><span data-stu-id="f2386-135">When you install Lync Server 2013, a new virtual directory (Mcx) is created under both the internal website and the external website on your Front End Servers.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="f2386-136">Lync Server 2013 mit den kumulierten Updates für lync Server 2013: Februar 2013 unterstützt sowohl den Mobilitätsdienst, der im kumulativen Update für lync Server 2010 eingeführt wurde: November 2011, allgemein bekannt als MCX, und die UCWA-Webkomponente.</span><span class="sxs-lookup"><span data-stu-id="f2386-136">Lync Server 2013 with the Cumulative Updates for Lync Server 2013: February 2013 supports both the Mobility service introduced in the Cumulative Update for Lync Server 2010: November 2011, commonly known as Mcx, and the UCWA web component.</span></span> <span data-ttu-id="f2386-137">Die Kombination dieser beiden Mobilitätsdienste bietet Interoperabilität und die Verwendung von Benutzern mit lync 2010 Mobile-und lync 2013-mobilen Clients auf lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="f2386-137">The combination of these two mobility services provides interoperability and use by users with Lync 2010 Mobile and Lync 2013 Mobile clients on Lync Server 2013.</span></span>

    
    </div>

  - <span data-ttu-id="f2386-138">**Lync Server 2013-AutoErmittlungsdienst**   Dieser Dienst identifiziert den Standort des Benutzers und ermöglicht es mobilen Geräten und anderen lync-Clients, Ressourcen zu finden, beispielsweise die internen und externen URLs für lync Server 2013-Webdienste und die URL für die MCX oder UCWA – unabhängig vom Netzwerkspeicherort.</span><span class="sxs-lookup"><span data-stu-id="f2386-138">**Lync Server 2013 Autodiscover Service**   This service identifies the location of the user and enables mobile devices and other Lync clients to locate resources—such as the internal and external URLs for Lync Server 2013 Web Services, and the URL for the Mcx or UCWA—regardless of network location.</span></span> <span data-ttu-id="f2386-139">Bei der automatischen Ermittlung werden hart codierte Host Namen (lyncdiscoverinternal für Benutzer im Netzwerk; lyncdiscover für Benutzer außerhalb des Netzwerks) und die SIP-Domäne des Benutzers verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2386-139">Automatic discovery uses hardcoded host names (lyncdiscoverinternal for users inside the network; lyncdiscover for users outside the network) and the SIP domain of the user.</span></span> <span data-ttu-id="f2386-140">Sowohl Clientverbindungen über HTTP als auch über HTTPS werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="f2386-140">It supports client connections that use either HTTP or HTTPS.</span></span>
    
    <span data-ttu-id="f2386-141">Der AutoErmittlungsdienst ist auf jedem Front-End-Server und auf jedem Director in jedem Pool installiert, der die lync-Funktionalität auf mobilen Geräten unterstützen soll.</span><span class="sxs-lookup"><span data-stu-id="f2386-141">The Autodiscover Service is installed on every Front End Server and on every Director in each pool that is to support Lync functionality on mobile devices.</span></span> <span data-ttu-id="f2386-142">Wenn Sie den AutoErmittlungsdienst installieren, wird ein neues virtuelles Verzeichnis (autodiscover) sowohl auf der internen Website als auch auf der externen Website sowohl auf Front-End-Servern als auch auf Directors erstellt.</span><span class="sxs-lookup"><span data-stu-id="f2386-142">When you install the Autodiscover Service, a new virtual directory (Autodiscover) is created under both the internal website and the external website, on both Front End Servers and Directors.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f2386-143">Der AutoErmittlungsdienst wird hier aufgelistet, da er bei der Bereitstellung von mobilen Clientdiensten eine wichtige Komponente bleibt.</span><span class="sxs-lookup"><span data-stu-id="f2386-143">The Autodiscover Service is listed here because it remains a critical component when providing mobile client services.</span></span> <span data-ttu-id="f2386-144">Die Rolle der AutoErmittlung in lync Server 2013 wurde erweitert, um Dienste für alle Clients bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f2386-144">The role of Autodiscover in Lync Server 2013 has been expanded to provide services for all clients.</span></span> <span data-ttu-id="f2386-145">Ausführliche Informationen zur Planung des AutoErmittlungsdiensts finden Sie unter <A href="lync-server-2013-planning-for-autodiscover.md">Planen der AutoErmittlung in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="f2386-145">For details about planning for the Autodiscover Service, see <A href="lync-server-2013-planning-for-autodiscover.md">Planning for Autodiscover in Lync Server 2013</A>.</span></span>

    
    </div>

  - <span data-ttu-id="f2386-146">**Push-Benachrichtigungsdienst**   Dieser Dienst ist ein Cloud-basierter Dienst, der sich im lync Online-Rechenzentrum befindet.</span><span class="sxs-lookup"><span data-stu-id="f2386-146">**Push Notification Service**   This service is a cloud-based service that is located in the Lync Online data center.</span></span> <span data-ttu-id="f2386-147">Wenn die lync Mobile-Anwendung auf einem unterstützten Apple IOS-Gerät oder Windows Phone inaktiv ist, kann Sie nicht auf neue Ereignisse reagieren, beispielsweise auf eine neue sofortnachrichteneinladung, eine verpasste Sofortnachricht, einen verpassten Anruf oder Voicemail, da diese Geräte keine mobilen Anwendungen unterstützen, die im Hintergrund ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f2386-147">When the Lync mobile application on a supported Apple iOS device or Windows Phone is inactive, it cannot respond to new events, such as a new instant messaging (IM) invitation, a missed instant message, a missed call, or voice mail, because these devices do not support mobile applications running in the background.</span></span> <span data-ttu-id="f2386-148">In diesen Fällen wird eine Benachrichtigung über das neue Ereignis – so genannte *Push-Benachrichtigung*– an das Mobile Gerät gesendet.</span><span class="sxs-lookup"><span data-stu-id="f2386-148">In these cases, a notification of the new event—called a *push notification*—is sent to the mobile device.</span></span> <span data-ttu-id="f2386-149">Der Mobilitätsdienst sendet die Benachrichtigung an den cloudbasierten Push-Benachrichtigungsdienst, der die Benachrichtigung entweder an den Apple Push Notification Service (APNS) (für unterstützte Apple IOS-Geräte) oder an den Microsoft Push Notification Service (MPNS) (für Windows Phone) sendet, der Sie dann an das Mobile Gerät sendet.</span><span class="sxs-lookup"><span data-stu-id="f2386-149">The Mobility Service sends the notification to the cloud-based Push Notification Service, which then sends the notification either to the Apple Push Notification Service (APNS) (for supported Apple iOS devices) or to the Microsoft Push Notification Service (MPNS) (for Windows Phone), which then sends it on to the mobile device.</span></span> <span data-ttu-id="f2386-150">Der Benutzer kann dann auf dem mobilen Gerät auf die Benachrichtigung Antworten, um die Anwendung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f2386-150">The user can then respond to the notification on the mobile device to activate the application.</span></span>
    
    <span data-ttu-id="f2386-151">Das lync 2010 Mobile auf Apple-und Windows Phone-Geräten verwendet Push-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="f2386-151">The Lync 2010 Mobile on Apple and Windows Phone devices use push notifications.</span></span> <span data-ttu-id="f2386-152">Der lync 2013-Mobile Client für Apple-Geräte, der mit den kumulativen Updates für lync Server 2013 eingeführt wurde: Februar 2013 verwendet keine Push-Benachrichtigung mehr oder das PNCH (Push Notification Clearing House).</span><span class="sxs-lookup"><span data-stu-id="f2386-152">The Lync 2013 Mobile client for Apple devices introduced with the Cumulative Updates for Lync Server 2013: February 2013 no longer uses push notification or the push notification clearing house (PNCH).</span></span>

<span data-ttu-id="f2386-153">Das folgende Diagramm zeigt, wie der Push-Benachrichtigungsdienst in eine lync Server 2013-Topologie passt, die UCWA-und lync 2013-Mobile Clients verwendet.</span><span class="sxs-lookup"><span data-stu-id="f2386-153">The following diagram illustrates how the Push Notification Service fits within a Lync Server 2013 topology that uses UCWA and Lync 2013 Mobile clients.</span></span>

<span data-ttu-id="f2386-154">![166d60fd-ff71-4ffe-9f66-3c8bbde0b5ae](images/Hh690037.166d60fd-ff71-4ffe-9f66-3c8bbde0b5ae(OCS.15).jpg "166d60fd-ff71-4ffe-9f66-3c8bbde0b5ae")</span><span class="sxs-lookup"><span data-stu-id="f2386-154">![166d60fd-ff71-4ffe-9f66-3c8bbde0b5ae](images/Hh690037.166d60fd-ff71-4ffe-9f66-3c8bbde0b5ae(OCS.15).jpg "166d60fd-ff71-4ffe-9f66-3c8bbde0b5ae")</span></span>

<span data-ttu-id="f2386-155">Der MCX-Dienst, der in das kumulative Update für lync Server 2010: November 2011 eingeführt wurde, bietet Dienste für lync 2010-Mobile Clients.</span><span class="sxs-lookup"><span data-stu-id="f2386-155">Introduced in Cumulative Update for Lync Server 2010: November 2011, the Mcx service provides services to Lync 2010 Mobile clients.</span></span> <span data-ttu-id="f2386-156">Das folgende Diagramm veranschaulicht den Push-Benachrichtigungsdienst für eine Topologie mit MCX-und lync 2010-mobilen Clients.</span><span class="sxs-lookup"><span data-stu-id="f2386-156">The following diagram illustrates the Push Notification Service as it applies to a topology using Mcx and Lync 2010 Mobile clients.</span></span>

<span data-ttu-id="f2386-157">![3081634e-60e7-4348-b24e-bbbf05a90f5f](images/Hh690037.3081634e-60e7-4348-b24e-bbbf05a90f5f(OCS.15).jpg "3081634e-60e7-4348-b24e-bbbf05a90f5f")</span><span class="sxs-lookup"><span data-stu-id="f2386-157">![3081634e-60e7-4348-b24e-bbbf05a90f5f](images/Hh690037.3081634e-60e7-4348-b24e-bbbf05a90f5f(OCS.15).jpg "3081634e-60e7-4348-b24e-bbbf05a90f5f")</span></span>

</div>

<div>

## <a name="supported-topologies"></a><span data-ttu-id="f2386-158">Unterstützte Topologien</span><span class="sxs-lookup"><span data-stu-id="f2386-158">Supported Topologies</span></span>

<span data-ttu-id="f2386-159">Durch Anwenden der kumulierten Updates für lync Server 2013: Februar 2013 werden die UCWA-Webkomponenten hinzugefügt, um die Mobilität für lync 2013-Mobile Clientfeatures in den folgenden Topologien zu unterstützen:</span><span class="sxs-lookup"><span data-stu-id="f2386-159">Applying the Cumulative Updates for Lync Server 2013: February 2013 adds the UCWA web components to support mobility for Lync 2013 Mobile client features in the following topologies:</span></span>

  - <span data-ttu-id="f2386-160">Lync Server 2013 Standard Edition</span><span class="sxs-lookup"><span data-stu-id="f2386-160">Lync Server 2013 Standard Edition</span></span>

  - <span data-ttu-id="f2386-161">Lync Server 2013 Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="f2386-161">Lync Server 2013 Enterprise Edition</span></span>

<span data-ttu-id="f2386-162">Der Edgeserver kann ein lync Server 2010 Edge-Server sein.</span><span class="sxs-lookup"><span data-stu-id="f2386-162">The Edge Server can be a Lync Server 2010 Edge Server.</span></span>

<span data-ttu-id="f2386-163">Eine lync Server 2013-Bereitstellung ohne die kumulativen Updates für lync Server 2013: Februar 2013 verwendet den MCX-Mobilitätsdienst und kann nur Dienste für lync 2010 Mobile bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="f2386-163">A Lync Server 2013 deployment without the Cumulative Updates for Lync Server 2013: February 2013 will use the Mcx Mobility Service and can provide services only for Lync 2010 Mobile.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="f2386-164">Der Mobilitätsdienst wird auf Front-End-Servern unterstützt, die mit der Vermittlungs Server Rolle mit zwei Netzwerkschnittstellen verbunden sind, Sie müssen jedoch die erforderlichen Schritte zum Konfigurieren der Schnittstellen ausführen.</span><span class="sxs-lookup"><span data-stu-id="f2386-164">The Mobility Service is supported on Front End Servers that is collocated with the Mediation Server role with two network interfaces, but you must take appropriate steps to configure the interfaces.</span></span> <span data-ttu-id="f2386-165">Sie müssen die IP-Adressen der jeweiligen Schnittstelle zuweisen, die als Vermittlungsserver kommuniziert, und die Netzwerkschnittstellen-IP-Adresse, die als Front-End-Server kommunizieren soll.</span><span class="sxs-lookup"><span data-stu-id="f2386-165">You must assign the IP addresses to the specific interface that will communicate as the Mediation Server, and the network interface IP that will communicate as the Front End Server.</span></span> <span data-ttu-id="f2386-166">Sie können dies in Topology Builder durchführen, indem Sie die richtige IP-Adresse für jeden Dienst auswählen, anstatt die standardmäßig <STRONG>alle konfigurierten IP-Adressen zu verwenden</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="f2386-166">You can do this in Topology Builder by selecting the correct IP address for each service, instead of using the default <STRONG>Use all configured IP addresses</STRONG>.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f2386-167">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2386-167">See Also</span></span>


[<span data-ttu-id="f2386-168">Planen des Zugriffs externer Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2386-168">Planning for external user access in Lync Server 2013</span></span>](lync-server-2013-planning-for-external-user-access.md)  
[<span data-ttu-id="f2386-169">Bereitstellen des Zugriffs durch externe Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2386-169">Deploying external user access in Lync Server 2013</span></span>](lync-server-2013-deploying-external-user-access.md)  
[<span data-ttu-id="f2386-170">Planen der AutoErmittlung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f2386-170">Planning for Autodiscover in Lync Server 2013</span></span>](lync-server-2013-planning-for-autodiscover.md)  
  

<span data-ttu-id="f2386-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f2386-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

