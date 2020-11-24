---
title: 'Lync Server 2013: Übersicht über den Zugriff durch externe Benutzer'
description: 'Lync Server 2013: Übersicht über den Zugriff durch externe Benutzer.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of external user access
ms:assetid: 97aded6c-5fa3-4225-95a6-9ad094d61654
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398775(v=OCS.15)
ms:contentKeyID: 48184934
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d2900dde457da34c4438892878ae7ddb4f74723a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394894"
---
# <a name="overview-of-external-user-access-in-lync-server-2013"></a><span data-ttu-id="1264a-103">Übersicht über den Zugriff durch externe Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1264a-103">Overview of external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1264a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1264a-104">

<span> </span></span></span>

<span data-ttu-id="1264a-105">_**Letztes Änderungsdatum des Themas:** 2013-11-07_</span><span class="sxs-lookup"><span data-stu-id="1264a-105">_**Topic Last Modified:** 2013-11-07_</span></span>

<span data-ttu-id="1264a-106">In dieser Dokumentation verwenden wir den Begriff *externer Benutzer* , um eine große Kategorie von Benutzern zu definieren, die von außerhalb der Firewall mit ihren lync Server 2013-und lync 2013-Benutzern kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="1264a-106">In this documentation, we use the term *external user* to define a large category of users who communicate with your Lync Server 2013 and Lync 2013 users from outside the firewall.</span></span> <span data-ttu-id="1264a-107">Externe Benutzer, die Sie für die Kommunikation mit lync Server 2013 mit internen Benutzern autorisieren können (das heißt, Benutzer, die sich bei lync Server innerhalb der Firewall anmelden), können Folgendes umfassen:</span><span class="sxs-lookup"><span data-stu-id="1264a-107">External users that you can authorize to communicate Lync Server 2013 with internal users (that is, users who sign in to Lync Server from inside the firewall) can include the following:</span></span>

  - <span data-ttu-id="1264a-108">**Remote Benutzer**   Benutzer Ihrer Organisation, die sich von außerhalb der Firewall bei lync Server anmelden.</span><span class="sxs-lookup"><span data-stu-id="1264a-108">**Remote users**   Users of your organization who sign in to Lync Server from outside the firewall.</span></span>

  - <span data-ttu-id="1264a-109">**Federated-Benutzer**   Benutzer, die über ein Konto bei einem vertrauenswürdigen Kunden oder einer Partnerorganisation wie lync Server 2010, lync Server 2013 oder Office Communications Server 2007 R2 verfügen</span><span class="sxs-lookup"><span data-stu-id="1264a-109">**Federated users**   Users who have an account with a trusted customer or partner organization, such as Lync Server 2010, Lync Server 2013 or Office Communications Server 2007 R2.</span></span> <span data-ttu-id="1264a-110">Federated-Benutzer können auch Mitglieder von definierten Partnerorganisationen sein, die mithilfe des XMPP-Proxys auf dem Edge-Server und dem XMPP-Gateway auf dem Front-End-Server oder-Pool über den XMPP-Proxy und das Presence-Protokoll (XMPP) verfügen.</span><span class="sxs-lookup"><span data-stu-id="1264a-110">Federated users can also be members of defined partner organizations using extensible messaging and presence protocol (XMPP) by way of the XMPP proxy on the Edge Server and XMPP gateway on the Front End Server or pool.</span></span> <span data-ttu-id="1264a-111">Eine definierte Vertrauensstellung, die so genannte Föderation, bezieht sich nicht auf eine Vertrauensstellung von Active Directory-Domänendiensten und hängt nicht davon ab.</span><span class="sxs-lookup"><span data-stu-id="1264a-111">A defined trust relationship, called a federation, is not related to or dependent upon an Active Directory Domain Services trust relationship.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1264a-112">Datum des Endes des Lebenszyklus von Juni 2014 für AOL und Yahoo!</span><span class="sxs-lookup"><span data-stu-id="1264a-112">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="1264a-113">wurde angekündigt.</span><span class="sxs-lookup"><span data-stu-id="1264a-113">has been announced.</span></span> <span data-ttu-id="1264a-114">Ausführliche Informationen finden Sie <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">unter Unterstützung für öffentliche Instant Messenger-Konnektivität in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="1264a-114">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span>

    
    </div>

  - <span data-ttu-id="1264a-115">**Benutzer von öffentlichen Instant Messaging-Verbindungen**   Kontakte, die Ihre Benutzer über öffentliche Instant Messaging-Verbindungsdienste einrichten (Windows Live, Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="1264a-115">**Public Instant Messaging Connectivity users**   Contacts that your users establish through public instant messaging connectivity services (Windows Live, Yahoo\!</span></span> <span data-ttu-id="1264a-116">und AOL).</span><span class="sxs-lookup"><span data-stu-id="1264a-116">and AOL).</span></span>

  - <span data-ttu-id="1264a-117">**Mobile Benutzer**   Benutzer, die Mitglieder Ihrer Organisation sind, die ein Smartphone oder ein Tablet mit einem lync Mobile-Client verwenden, werden bei ihrer internen Bereitstellung angemeldet und können mit den anderen Benutzergruppen kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="1264a-117">**Mobile users**   Users that are members of your organization that use a smart phone or tablet running a Lync Mobile client sign in to your internal deployment and are able to communicate with the other classes of users.</span></span> <span data-ttu-id="1264a-118">Der Mobile Benutzer verwendet Mobilitätsdienste, die über den Reverse Proxy veröffentlicht werden, um auf die interne Bereitstellung zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="1264a-118">The mobile user uses mobility services that are published through the reverse proxy to access the internal deployment.</span></span> <span data-ttu-id="1264a-119">Details zu den Features und Funktionen, die für lync Mobile verfügbar sind, finden Sie in den Vergleichstabellen für mobile Clients unter [https://go.microsoft.com/fwlink/p/?LinkID=234777](https://go.microsoft.com/fwlink/p/?linkid=234777) .</span><span class="sxs-lookup"><span data-stu-id="1264a-119">For details on features and capabilities available to Lync Mobile , see the Mobile Client Comparison Tables at [https://go.microsoft.com/fwlink/p/?LinkID=234777](https://go.microsoft.com/fwlink/p/?linkid=234777).</span></span>

  - <span data-ttu-id="1264a-120">**Anonyme Benutzer**   Benutzer, die nicht über ein Benutzerkonto in den Active Directory-Domänendiensten Ihrer Organisation oder in einer unterstützten Föderationsdomäne verfügen, aber Einladungen zur Remote Teilnahme an einer lokalen Konferenz erhalten haben.</span><span class="sxs-lookup"><span data-stu-id="1264a-120">**Anonymous users**   Users who do not have a user account in your organization's Active Directory Domain Services or in a supported federated domain, but who have received invitations to participate remotely in an on-premises conference.</span></span>

<span data-ttu-id="1264a-121">Ihre Edge-Bereitstellung bietet externen Zugriff für die folgenden Kommunikationsarten:</span><span class="sxs-lookup"><span data-stu-id="1264a-121">Your edge deployment provides external access for the following types of communication:</span></span>

  - <span data-ttu-id="1264a-122">**Chat und Anwesenheit**   Autorisierte externe Benutzer können an Chat Unterhaltungen und Konferenzen teilnehmen, und Sie können Informationen über den Anwesenheitsstatus einer anderen Person erhalten.</span><span class="sxs-lookup"><span data-stu-id="1264a-122">**IM and presence**   Authorized external users can participate in IM conversations and conferences, and they can get information about one another’s presence status.</span></span> <span data-ttu-id="1264a-123">Benutzer von öffentlichen Chat Dienstanbietern können an Chat Unterhaltungen mit einzelnen lync Server-Benutzern in Ihrer Organisation teilnehmen und auf Anwesenheitsinformationen zugreifen, aber Sie können mit lync Server nicht an Chat Konferenzen teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="1264a-123">Users of public IM service providers can participate in IM conversations with individual Lync Server users in your organization and access presence information, but they cannot participate in IM multiparty conferences using Lync Server.</span></span> <span data-ttu-id="1264a-124">Es handelt sich um eine strikte Peer-to-Peer-Kommunikation.</span><span class="sxs-lookup"><span data-stu-id="1264a-124">It is strictly peer-to-peer communication.</span></span> <span data-ttu-id="1264a-125">Die Dateiübertragung wird für Benutzer von öffentlichen Chat Dienstanbietern nicht unterstützt, und Audio/Video in Peer-zu-Peer-Kommunikation wird für Windows Messenger 2011-Benutzer, aber nicht für andere Benutzer von öffentlichen Chatdienst Anbietern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1264a-125">File transfer is not supported for users of public IM service providers, and audio/video in peer-to-peer communications is supported for Windows Messenger 2011 users, but not other users of public IM service providers.</span></span>
    
    <span data-ttu-id="1264a-126">Sowohl SIP-als auch XMPP-Protokolle werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1264a-126">Both SIP and XMPP protocols are supported.</span></span> <span data-ttu-id="1264a-127">Informationen zum Bereitstellen von Diensten für XMPP finden Sie unter [Planen von SIP, XMPP Federation und Public Instant Messaging in lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="1264a-127">To provide services for XMPP, see [Planning for SIP, XMPP federation, and public instant messaging in Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md).</span></span>

  - <span data-ttu-id="1264a-128">**Web-Konferenzen**   Autorisierte externe Benutzer können an Konferenzen teilnehmen, die in ihrer lync Server-Bereitstellung gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="1264a-128">**Web conferencing**   Authorized external users can participate in conferences that are hosted on your Lync Server deployment.</span></span> <span data-ttu-id="1264a-129">Remote Benutzer, verbundene Benutzer und anonyme Benutzer können für die Teilnahme an Webkonferenzen aktiviert werden, aber öffentliche Chat-Benutzer können nicht an Konferenzen teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="1264a-129">Remote users, federated users, and anonymous users can be enabled for participation in web conferencing, but public IM users cannot participate in conferences.</span></span> <span data-ttu-id="1264a-130">Je nach den von Ihnen ausgewählten Optionen können Webkonferenzen aktivierte Benutzer an der Desktop-und Anwendungsfreigabe teilnehmen und als Besprechungsorganisatoren oder Referenten fungieren.</span><span class="sxs-lookup"><span data-stu-id="1264a-130">Depending on the options that you select, web conferencing-enabled users can participate in desktop and application sharing and can act as meeting organizers or presenters.</span></span>

  - <span data-ttu-id="1264a-131">**A/V-Konferenzen**   Autorisierte externe Benutzer können an Audio-und Videokonferenzen teilnehmen, die ihre lync Server-Bereitstellung hostet.</span><span class="sxs-lookup"><span data-stu-id="1264a-131">**A/V conferencing**   Authorized external users can participate in audio and video conferences that your Lync Server deployment hosts.</span></span> <span data-ttu-id="1264a-132">Audio/Video in der Peer-to-Peer-Kommunikation wird für Windows Messenger 2011-Benutzer, aber nicht für andere Benutzer von öffentlichen Chat Dienstanbietern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="1264a-132">Audio/video in peer-to-peer communications is supported for Windows Messenger 2011 users, but not for other users of public IM service providers.</span></span>

<span data-ttu-id="1264a-133">Um die Kommunikation zu steuern, können Sie eine oder mehrere Richtlinien konfigurieren, die definieren, wie Benutzer innerhalb und außerhalb Ihrer Organisation miteinander kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="1264a-133">In order to control communications, you can configure one or more policies that define how users inside and outside your organization communicate with each other.</span></span> <span data-ttu-id="1264a-134">Sie können auch Einstellungen konfigurieren und Richtlinien für einzelne interne Benutzer oder bestimmte Typen externer Benutzer anwenden, um die Kommunikation mit externen Benutzern zu steuern.</span><span class="sxs-lookup"><span data-stu-id="1264a-134">You can also configure settings and apply policies for individual internal users or for specific types of external users to control communications with external users.</span></span>

<span data-ttu-id="1264a-135">Lync Server 2013-Rollen, die für den externen Zugriff verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="1264a-135">Lync Server 2013 roles that are used to provide external access:</span></span>

<span data-ttu-id="1264a-136">**Edgeserver**   Beim Edgeserver handelt es sich um einen Server oder einen Pool von Servern, auf denen die Dienste ausgeführt werden, die externen Zugriff auf Chat und Anwesenheitsinformationen, Konferenzen, Audio/Video und andere Medien (beispielsweise Dateiübertragungsdienste) ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="1264a-136">**Edge Server**   The Edge Server is a server or a pool of servers that run the services that allow external access to IM and presence, conferencing, audio/video, and other media (for example, file transfer) services.</span></span> <span data-ttu-id="1264a-137">Optional können Sie den Edgeserver für die Föderation mit anderen lync Server-oder Office Communications Server 2007 R2-Bereitstellungen und anderen XMPP-Bereitstellungen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="1264a-137">Optionally, you can configure the Edge Server to federate with other Lync Server or Office Communications Server 2007 R2 deployments, and other XMPP deployments.</span></span> <span data-ttu-id="1264a-138">Das optionale Feature für die öffentliche Chat Verbindung wird über den Edgeserver aktiviert und konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="1264a-138">The optional public IM connectivity feature is enabled and configured through the Edge Server.</span></span>

<span data-ttu-id="1264a-139">**Direktor**   Der Director ist ein optionaler Server-oder Serverpool, auf dem die lync Server 2013 Director-Rolle ausgeführt wird, mit der Benutzeranforderungen vorab authentifiziert und Anforderungen an den Start-Front-End-Server oder Front-End-Pool der Benutzer weitergeleitet werden, jedoch keine Benutzerkonten zu Hause sind.</span><span class="sxs-lookup"><span data-stu-id="1264a-139">**Director**   The Director is an optional server or server pool running the Lync Server 2013 Director role that pre-authenticates user requests and routes requests to the users’ home Front End Server or Front End pool, but does not home any user accounts.</span></span>

<span data-ttu-id="1264a-140">**Reverseproxy**   Bei einem Reverse-Proxy handelt es sich um einen allgemeinen Ausdruck für spezialisierte Server, die im internen Netzwerk verfügbare Ressourcen veröffentlichen und Informationen für Clients aus der veröffentlichten Ressource abrufen.</span><span class="sxs-lookup"><span data-stu-id="1264a-140">**Reverse Proxy**   A reverse proxy is a general term for specialized servers that publish resources available on the internal network and retrieve information for clients from the published resource.</span></span> <span data-ttu-id="1264a-141">Lync Server 2013 verwendet den Reverseproxy zum Veröffentlichen einer Reihe von Features, wie Konferenz Besprechungen, Konferenz-Join-Speicherorte, Adressbuch, Erweiterung der Verteilerliste, Herunterladen von Besprechungsinhalten, Geräte Updates, Mobilitätsdienste und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="1264a-141">Lync Server 2013 uses the reverse proxy to publish a number of features, such as conferencing meetings, conference join locations, the address book, distribution list expansion, downloading meeting content, device updates, Mobility services, and more.</span></span> <span data-ttu-id="1264a-142">Alle Reverse-Proxys, die die Anforderungen für die Veröffentlichung der erforderlichen Ressourcenspeicherorte erfüllen können, können verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="1264a-142">Any reverse proxy that can meet the requirements for publishing the necessary resource locations can be used.</span></span> <span data-ttu-id="1264a-143">Microsoft Forefront Threat Management Gateway (TMG) 2010 wird als Beispiel verwendet, um die Veröffentlichungsregeln zu illustrieren, aber Forefront TMG 2010 ist nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1264a-143">Microsoft Forefront Threat Management Gateway (TMG) 2010 is used as an example for the purposes of illustrating the publishing rules necessary, but Forefront TMG 2010 is not required.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="1264a-144">Lync Server 2013 unterstützt IPv4 und IPv6.</span><span class="sxs-lookup"><span data-stu-id="1264a-144">Lync Server 2013 supports both IPv4 and IPv6.</span></span> <span data-ttu-id="1264a-145">Windows Server &nbsp; 2008 &nbsp; R2, Windows Server 2012 und Windows Server 2012 R2 verwenden einen dualen Stapel, der gleichzeitig IPv4 und IPv6 verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="1264a-145">Windows Server&nbsp;2008&nbsp;R2, Windows Server 2012, and Windows Server 2012 R2 use a dual stack that can use both IPv4 and IPv6 concurrently.</span></span> <span data-ttu-id="1264a-146">Dies ist wichtig, da eine Bereitstellung, die von IPv4 zu IPv6 wechselt, übergangsweise ist.</span><span class="sxs-lookup"><span data-stu-id="1264a-146">This is important because of the transitional nature of a deployment moving from IPv4 to IPv6.</span></span> <span data-ttu-id="1264a-147">IPv4 kann in einigen Bereichen unterstützt werden, in denen in anderen Bereichen der Bereitstellung IPv6 verwendet werden kann.</span><span class="sxs-lookup"><span data-stu-id="1264a-147">IPv4 can be supported in some areas, where in other areas of the deployment, IPv6 can be used.</span></span> <span data-ttu-id="1264a-148">Dies ist besonders wichtig, wenn es um das Internet und interne Bereitstellungen geht.</span><span class="sxs-lookup"><span data-stu-id="1264a-148">This is especially important where the Internet and internal deployments are concerned.</span></span> <span data-ttu-id="1264a-149">Externe Clients müssen über den Reverse-Proxy kommunizieren, um Dienste wie Mobilität, Besprechungen, Adressbuch Download und andere zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="1264a-149">External clients must communicate through the reverse proxy to use services such as mobility, meetings, address book download, and others.</span></span> <span data-ttu-id="1264a-150">Derzeit unterstützen Forefront Threat Management Gateway 2010 und Internet Security and Acceleration Server 2006 keine IPv6-Adressierung, unabhängig von der Betriebssystemversion, auf der Sie bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="1264a-150">Currently, Forefront Threat Management Gateway 2010 and Internet Security and Acceleration Server 2006 do not support IPv6 addressing, regardless of the operating system version that they are deployed on.</span></span> <span data-ttu-id="1264a-151">Sie müssen in Bezug auf ihre Verwendung von IPv6 und IPv4 entsprechend planen, während Sie sich auf externe Clients beziehen.</span><span class="sxs-lookup"><span data-stu-id="1264a-151">You must plan accordingly in relation to your use of IPv6 and IPv4 as they relate to external clients.</span></span>



<span data-ttu-id="1264a-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1264a-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

