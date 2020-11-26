---
title: 'Lync Server 2013: Serverrollen'
description: Lync Server 2013-Serverrollen.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server roles
ms:assetid: 7137fc06-fca2-4e5f-9db5-10c7c29a788c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398536(v=OCS.15)
ms:contentKeyID: 48184456
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7ee4636e602e5bfb8ce6eacdccb3d190f5728d1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441858"
---
# <a name="server-roles-in-lync-server-2013"></a><span data-ttu-id="8c51c-103">Serverrollen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c51c-103">Server roles in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8c51c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8c51c-104">

<span> </span></span></span>

<span data-ttu-id="8c51c-105">_**Letztes Änderungsdatum des Themas:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="8c51c-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="8c51c-106">Jeder Server, auf dem lync Server ausgeführt wird, führt mindestens eine *Serverrolle* aus.</span><span class="sxs-lookup"><span data-stu-id="8c51c-106">Each server running Lync Server runs one or more *server roles*.</span></span> <span data-ttu-id="8c51c-107">Eine Serverrolle ist ein definierter Satz von lync Server-Funktionen, die von diesem Server bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="8c51c-107">A server role is a defined set of Lync Server functionalities provided by that server.</span></span> <span data-ttu-id="8c51c-108">Sie müssen nicht alle verfügbaren Serverrollen in Ihrem Netzwerk bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8c51c-108">You do not need to deploy all available server roles in your network.</span></span> <span data-ttu-id="8c51c-109">Installieren Sie lediglich die Serverrollen, die die erforderliche Funktionalität enthalten.</span><span class="sxs-lookup"><span data-stu-id="8c51c-109">Install only the server roles that contain the functionality that you want.</span></span>

<span data-ttu-id="8c51c-110">Auch wenn Sie mit den Serverrollen in lync Server nicht vertraut sind, kann das Planungs Tool Sie auf der Grundlage der gewünschten Features zur besten Lösung für die Server führen, die Sie bereitstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="8c51c-110">Even if you are not familiar with server roles in Lync Server, the Planning Tool can guide you to the best solution for the servers that you need to deploy, based on the features that you want.</span></span> <span data-ttu-id="8c51c-111">Dieser Abschnitt enthält eine kurze Übersicht über die Serverrollen und die allgemeinen Features, die Sie bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="8c51c-111">This section provides a brief overview of the server roles and the general features that they provide:</span></span>

  - <span data-ttu-id="8c51c-112">Standard Edition-Server</span><span class="sxs-lookup"><span data-stu-id="8c51c-112">Standard Edition Server</span></span>

  - <span data-ttu-id="8c51c-113">Front-End-Server und Back-End-Server</span><span class="sxs-lookup"><span data-stu-id="8c51c-113">Front End Server and Back End Server</span></span>

  - <span data-ttu-id="8c51c-114">Edgeserver</span><span class="sxs-lookup"><span data-stu-id="8c51c-114">Edge Server</span></span>

  - <span data-ttu-id="8c51c-115">Vermittlungsserver</span><span class="sxs-lookup"><span data-stu-id="8c51c-115">Mediation Server</span></span>

  - <span data-ttu-id="8c51c-116">Director</span><span class="sxs-lookup"><span data-stu-id="8c51c-116">Director</span></span>

  - <span data-ttu-id="8c51c-117">Front-End-Server für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="8c51c-117">Persistent Chat Front End Server</span></span>

  - <span data-ttu-id="8c51c-118">Beständiger Chat Speicher (beständiger Chat-Back-End-Server)</span><span class="sxs-lookup"><span data-stu-id="8c51c-118">Persistent Chat Store (Persistent Chat Back End Server)</span></span>

  - <span data-ttu-id="8c51c-119">Kompatibilitäts Speicher für beständigen Chat (Kompatibilitäts-Compliance-Back-End-Server)</span><span class="sxs-lookup"><span data-stu-id="8c51c-119">Persistent Chat Compliance Store (Persistent Chat Compliance Back End Server)</span></span>

<span data-ttu-id="8c51c-120">Um Skalierbarkeit und hohe Verfügbarkeit zu bieten, können Sie für die meisten Serverrollen *Pools* mit mehreren Servern bereitstellen, auf denen dieselbe Serverrolle ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="8c51c-120">For most server roles, for scalability and high availability you can deploy *pools* of multiple servers all running the same server role.</span></span> <span data-ttu-id="8c51c-121">Auf allen Servern innerhalb eines Pools muss dieselbe Serverrolle ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8c51c-121">Each server in a pool must run an identical server role or roles.</span></span> <span data-ttu-id="8c51c-122">Bei den meisten Typen von Pools in lync Server müssen Sie ein Lastenausgleichsmodul bereitstellen, um den Datenverkehr zwischen den verschiedenen Servern im Pool zu verbreiten.</span><span class="sxs-lookup"><span data-stu-id="8c51c-122">For most types of pools in Lync Server, you must deploy a load balancer to spread traffic between the various servers in the pool.</span></span> <span data-ttu-id="8c51c-123">Lync Server unterstützt sowohl DNS (Domain Name System)-Lastenausgleich als auch Hardwarelastenausgleichs.</span><span class="sxs-lookup"><span data-stu-id="8c51c-123">Lync Server supports both Domain Name System (DNS) load balancing and hardware load balancers.</span></span>

<div>

## <a name="standard-edition-server"></a><span data-ttu-id="8c51c-124">Standard Edition-Server</span><span class="sxs-lookup"><span data-stu-id="8c51c-124">Standard Edition Server</span></span>

<span data-ttu-id="8c51c-125">Der Standard Edition-Server ist für kleine Organisationen und für Pilotprojekte großer Organisationen konzipiert.</span><span class="sxs-lookup"><span data-stu-id="8c51c-125">The Standard Edition server is designed for small organizations, and for pilot projects of large organizations.</span></span> <span data-ttu-id="8c51c-126">Damit können viele der Features von lync Server, einschließlich der erforderlichen Datenbanken, auf einem einzelnen Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8c51c-126">It enables many of the features of Lync Server, including the necessary databases, to run on a single server.</span></span> <span data-ttu-id="8c51c-127">Dies ermöglicht Ihnen, lync Server-Funktionen zu einem niedrigeren Preis zu nutzen, bietet jedoch keine echte Lösung mit hoher Verfügbarkeit.</span><span class="sxs-lookup"><span data-stu-id="8c51c-127">This enables you to have Lync Server functionality for a lower cost, but does not provide a true high-availability solution.</span></span>

<span data-ttu-id="8c51c-128">Der Standard Edition-Server ermöglicht Ihnen die Verwendung von Instant Messaging (im), Anwesenheitsfunktionen, Konferenzen und Enterprise-VoIP, die alle auf einem Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8c51c-128">Standard Edition server enables you to use instant messaging (IM), presence, conferencing, and Enterprise Voice, all running on one server.</span></span>

<span data-ttu-id="8c51c-129">Verwenden Sie für eine Lösung mit hoher Verfügbarkeit die lync Server Enterprise Edition.</span><span class="sxs-lookup"><span data-stu-id="8c51c-129">For a high-availability solution, use Lync Server Enterprise Edition.</span></span>

</div>

<div>

## <a name="front-end-server-and-back-end-server"></a><span data-ttu-id="8c51c-130">Front-End-Server und Back-End-Server</span><span class="sxs-lookup"><span data-stu-id="8c51c-130">Front End Server and Back End Server</span></span>

<span data-ttu-id="8c51c-131">In lync Server Enterprise Edition ist der Front-End-Server die Hauptserver Rolle und führt viele grundlegende lync-Serverfunktionen aus.</span><span class="sxs-lookup"><span data-stu-id="8c51c-131">In Lync Server Enterprise Edition, the Front End Server is the core server role, and runs many basic Lync Server functions.</span></span> <span data-ttu-id="8c51c-132">Der Front-End-Server ist zusammen mit den Back-End-Servern die einzige Server Rolle, die für eine lync Server Enterprise Edition-Bereitstellung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8c51c-132">The Front End Server, along with the Back End Servers, are the only server roles required to be in any Lync Server Enterprise Edition deployment.</span></span>

<span data-ttu-id="8c51c-133">Bei einem *Front-End-Pool* handelt es sich um einen Satz von Front-End-Servern, die identisch konfiguriert sind und zusammenarbeiten, um Dienste für eine gemeinsame Gruppe von Benutzern bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8c51c-133">A *Front End pool* is a set of Front End Servers, configured identically, that work together to provide services for a common group of users.</span></span> <span data-ttu-id="8c51c-134">Ein Pool mit mehreren Servern, auf denen dieselbe Rolle ausgeführt wird, bietet Skalierbarkeit und Failoverfunktionen.</span><span class="sxs-lookup"><span data-stu-id="8c51c-134">A pool of multiple servers running the same role provides scalability and failover capability.</span></span>

<span data-ttu-id="8c51c-135">Der Front-End-Server enthält Folgendes:</span><span class="sxs-lookup"><span data-stu-id="8c51c-135">The Front End Server includes the following:</span></span>

  - <span data-ttu-id="8c51c-136">Benutzerauthentifizierung und-Registrierung</span><span class="sxs-lookup"><span data-stu-id="8c51c-136">User authentication and registration</span></span>

  - <span data-ttu-id="8c51c-137">Anwesenheitsinformationen und Kontaktkarten Austausch</span><span class="sxs-lookup"><span data-stu-id="8c51c-137">Presence information and contact card exchange</span></span>

  - <span data-ttu-id="8c51c-138">Erweiterung von Adressbuchdiensten und Verteilerlisten</span><span class="sxs-lookup"><span data-stu-id="8c51c-138">Address book services and distribution list expansion</span></span>

  - <span data-ttu-id="8c51c-139">Chat-Funktionen, einschließlich mehrteiliger Chat Konferenzen</span><span class="sxs-lookup"><span data-stu-id="8c51c-139">IM functionality, including multiparty IM conferences</span></span>

  - <span data-ttu-id="8c51c-140">Webkonferenzen, PSTN-Einwahlkonferenzen und a/V-Konferenzen (falls bereitgestellt)</span><span class="sxs-lookup"><span data-stu-id="8c51c-140">Web conferencing, PSTN Dial-in conferencing and A/V conferencing (if deployed)</span></span>

  - <span data-ttu-id="8c51c-141">Anwendungshosting, für beide Anwendungen, die in lync Server enthalten sind (beispielsweise Konferenzzentrale und reaktionsgruppenanwendung) und Anwendungen von Drittanbietern</span><span class="sxs-lookup"><span data-stu-id="8c51c-141">Application hosting, for both applications included with Lync Server (for example, Conferencing Attendant and Response Group application), and third-party applications</span></span>

  - <span data-ttu-id="8c51c-142">Optional eine Überwachungsfunktion, um Nutzungsinformationen in Form von Kommunikationsdatensätzen und Daten zu Anruffehlern zu erfassen.</span><span class="sxs-lookup"><span data-stu-id="8c51c-142">Optionally, Monitoring, to collect usage information in the form of call detail records (CDRs) and call error records (CERs).</span></span> <span data-ttu-id="8c51c-143">Diese Informationen enthalten Metriken zur Qualität der Medien (Audio und Video), die in Ihrem Netzwerk für Enterprise-Sprachanrufe und A/V-Konferenzen durchlaufen werden.</span><span class="sxs-lookup"><span data-stu-id="8c51c-143">This information provides metrics about the quality of the media (audio and video) traversing your network for both Enterprise Voice calls and A/V conferences.</span></span>

  - <span data-ttu-id="8c51c-144">Webkomponenten zu unterstützten webbasierten Aufgaben wie Webplaner und Join Launcher.</span><span class="sxs-lookup"><span data-stu-id="8c51c-144">Web components to supported web-based tasks such as web scheduler and join launcher.</span></span>

  - <span data-ttu-id="8c51c-145">Optional eine Archivierung der Chatnachrichtenkommunikation und Besprechungsinhalte, um rechtliche Vorgaben einzuhalten.</span><span class="sxs-lookup"><span data-stu-id="8c51c-145">Optionally, Archiving, to archive IM communications and meeting content for compliance reasons.</span></span> <span data-ttu-id="8c51c-146">Ausführliche Informationen finden Sie unter [Planen der Archivierung in lync Server 2013](lync-server-2013-planning-for-archiving.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="8c51c-146">For details, see [Planning for Archiving in Lync Server 2013](lync-server-2013-planning-for-archiving.md) in the Planning documentation.</span></span>
    
    <span data-ttu-id="8c51c-147">In lync Server 2010 und früheren Versionen waren Überwachung und Archivierung getrennte Server Rollen, nicht auf dem Front-End-Server.</span><span class="sxs-lookup"><span data-stu-id="8c51c-147">In Lync Server 2010 and prior versions, Monitoring and Archiving were separate server roles, not collocated on Front End Server.</span></span>

  - <span data-ttu-id="8c51c-148">Optional, sofern der beständige Chat aktiviert ist, Webdienste für den beständigen Chat für die Chatroom-Verwaltung und Webdienste für den beständigen Chat für das Hochladen/Herunterladen von Dateien.</span><span class="sxs-lookup"><span data-stu-id="8c51c-148">Optionally, if Persistent chat is enabled, Persistent Chat Web Services for Chat Room Management and Persistent Chat Web Services for File Upload/Download.</span></span>

<span data-ttu-id="8c51c-p109">Front-End-Pools bilden außerdem den primären Speicher für Benutzer- und Konferenzdaten. Die Informationen zu den einzelnen Benutzern werden auf drei Front-End-Servern im Pool repliziert und auf den Back-End-Servern gesichert.</span><span class="sxs-lookup"><span data-stu-id="8c51c-p109">Front End Pools are also the primary store for user and conference data. Information about each user is replicated among three Front End Servers in the pool, and backed up on the Back End Servers.</span></span>

<span data-ttu-id="8c51c-151">Darüber hinaus führt ein Front-End-Pool in der Bereitstellung auch den *zentralen Verwaltungs Server* aus, der grundlegende Konfigurationsdaten für alle Server mit lync Server verwaltet und bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="8c51c-151">Additionally, one Front End pool in the deployment also runs the *Central Management Server*, which manages and deploys basic configuration data to all servers running Lync Server.</span></span> <span data-ttu-id="8c51c-152">Der zentrale Verwaltungs Server bietet auch die lync Server-Verwaltungsshell und die Dateiübertragungsfunktionen.</span><span class="sxs-lookup"><span data-stu-id="8c51c-152">The Central Management Server also provides Lync Server Management Shell and file transfer capabilities.</span></span>

<span data-ttu-id="8c51c-153">Die Back-End-Server sind Datenbankserver mit Microsoft SQL Server, die die Datenbankdienste für den Front-End-Pool bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8c51c-153">The Back End Servers are database servers running Microsoft SQL Server that provide the database services for the Front End pool.</span></span> <span data-ttu-id="8c51c-154">Die Back-End-Server dienen als Sicherungsspeicher für die Benutzer-und Konferenzdaten des Pools und sind die primären Speicher für andere Datenbanken wie die Datenbank der Reaktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="8c51c-154">The Back End Servers serve as backup stores for the pool’s user and conference data, and are the primary stores for other databases such as the Response Group database.</span></span> <span data-ttu-id="8c51c-155">Sie können einen einzelnen Back-End-Server verwenden, aber für Failover empfiehlt sich eine Lösung, die die SQL Server-Spiegelung verwendet.</span><span class="sxs-lookup"><span data-stu-id="8c51c-155">You can have a single Back End Server, but a solution that uses SQL Server mirroring is recommended for failover.</span></span> <span data-ttu-id="8c51c-156">Back-End-Server führen keine lync Server-Software aus.</span><span class="sxs-lookup"><span data-stu-id="8c51c-156">Back End Servers do not run any Lync Server software.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="8c51c-157">Es wird nicht empfohlen, abstimmen lync Server-Datenbanken mit anderen Datenbanken zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8c51c-157">We do not recommend collocating Lync Server databases with other databases.</span></span> <span data-ttu-id="8c51c-158">Andernfalls können Verfügbarkeit und Leistung beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="8c51c-158">If you do so, availability and performance may be affected.</span></span>



</div>

<span data-ttu-id="8c51c-159">Die in den Datenbanken auf einem Back-End-Server gespeicherten Daten umfassen Anwesenheitsinformationen, die Kontaktlisten der Benutzer, Konferenzdaten (einschließlich dauerhafter Daten zum Zustand aller aktuellen Konferenzen) sowie Konferenzplanungsdaten.</span><span class="sxs-lookup"><span data-stu-id="8c51c-159">Information stored in the Back End Server databases includes presence information, users' Contacts lists, conferencing data, including persistent data about the state of all current conferences, and conference scheduling data.</span></span>

</div>

<div>

## <a name="edge-server"></a><span data-ttu-id="8c51c-160">Edgeserver</span><span class="sxs-lookup"><span data-stu-id="8c51c-160">Edge Server</span></span>

<span data-ttu-id="8c51c-161">Edge-Server ermöglicht Ihren Benutzern die Kommunikation und Zusammenarbeit mit Benutzern außerhalb der Firewalls der Organisation.</span><span class="sxs-lookup"><span data-stu-id="8c51c-161">Edge Server enables your users to communicate and collaborate with users outside the organization’s firewalls.</span></span> <span data-ttu-id="8c51c-162">Diese externen Benutzer können die eigenen Benutzer der Organisation einbeziehen, die derzeit an einem externen Standort arbeiten, Benutzer aus Föderationspartner Organisationen und externe Benutzer, die eingeladen wurden, an Konferenzen teilzunehmen, die in ihrer lync Server-Bereitstellung gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="8c51c-162">These external users can include the organization’s own users who are currently working offsite, users from federated partner organizations, and outside users who have been invited to join conferences hosted on your Lync Server deployment.</span></span> <span data-ttu-id="8c51c-163">Edge-Server ermöglicht auch die Konnektivität mit öffentlichen Chat Diensten wie Windows Live, AOL, Yahoo \! und Google Talk.</span><span class="sxs-lookup"><span data-stu-id="8c51c-163">Edge Server also enables connectivity to public IM connectivity services, including Windows Live, AOL, Yahoo\!, and Google Talk.</span></span>

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="8c51c-164">Ab dem 1. September, 2012, ist die Microsoft lync Public im Connectivity-Benutzerabonnementlizenz ("PIC USL") nicht mehr für den Kauf von neuen oder erneuernden Vereinbarungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8c51c-164">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="8c51c-165">Kunden mit aktiven Lizenzen sind in der Lage, weiterhin mit Yahoo! zu verbünden</span><span class="sxs-lookup"><span data-stu-id="8c51c-165">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="8c51c-166">Messenger, bis der Dienst das Datum beendet hat.</span><span class="sxs-lookup"><span data-stu-id="8c51c-166">Messenger until the service shut down date.</span></span> <span data-ttu-id="8c51c-167">Datum des Endes des Lebenszyklus von Juni 2014 für AOL und Yahoo!</span><span class="sxs-lookup"><span data-stu-id="8c51c-167">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="8c51c-168">wurde angekündigt.</span><span class="sxs-lookup"><span data-stu-id="8c51c-168">has been announced.</span></span> <span data-ttu-id="8c51c-169">Ausführliche Informationen finden Sie <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">unter Unterstützung für öffentliche Instant Messenger-Konnektivität in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="8c51c-169">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="8c51c-170">Bei der PIC-USL handelt es sich um eine Abonnementlizenz pro Benutzer pro Monat, die für die Föderation von lync Server oder Office Communications Server mit Yahoo! erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8c51c-170">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="8c51c-171">Messenger.</span><span class="sxs-lookup"><span data-stu-id="8c51c-171">Messenger.</span></span> <span data-ttu-id="8c51c-172">Die Möglichkeit von Microsoft, diesen Dienst bereitzustellen, war von der Unterstützung durch Yahoo! abhängig, deren zugrunde liegende Vereinbarung abgewickelt wird.</span><span class="sxs-lookup"><span data-stu-id="8c51c-172">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
> <LI>
> <P><span data-ttu-id="8c51c-173">Lync ist mehr denn je ein leistungsfähiges Tool für die Verbindung zwischen Organisationen und Personen in der ganzen Welt.</span><span class="sxs-lookup"><span data-stu-id="8c51c-173">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="8c51c-174">Für den Verbund mit Windows Live Messenger sind keine zusätzlichen Benutzer-und Gerätelizenzen außerhalb der lync-Standard CAL erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8c51c-174">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="8c51c-175">Skype Federation wird dieser Liste hinzugefügt und ermöglicht es lync-Benutzern, Hunderte von Millionen von Personen mit Chat und Sprache zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="8c51c-175">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>



</div>

<span data-ttu-id="8c51c-176">Durch die Bereitstellung von Edge Server werden auch Mobilitätsdienste aktiviert, die die lync-Funktionalität auf mobilen Geräten unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8c51c-176">Deploying Edge Server also enables mobility services, which supports Lync functionality on mobile devices.</span></span> <span data-ttu-id="8c51c-177">Benutzer können mit unterstützten mobilen Geräten (Apple iOS, Android, Windows Phone oder Nokia) Aktionen wie Senden und Empfangen von Chatnachrichten, Anzeigen von Kontakten und Anzeigen der Anwesenheit ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c51c-177">Users can use supported Apple iOS, Android, Windows Phone, or Nokia mobile devices to perform activities such as sending and receiving instant messages, viewing contacts, and viewing presence.</span></span> <span data-ttu-id="8c51c-178">Darüber hinaus unterstützen Mobile Geräte einige Enterprise-VoIP-Features, wie beispielsweise klicken, um an einer Konferenz teilzunehmen, über Arbeit anzurufen, eine Rufnummer zu erreichen, Voicemail und verpasste Anrufe zu tätigen.</span><span class="sxs-lookup"><span data-stu-id="8c51c-178">In addition, mobile devices support some Enterprise Voice features, such as click to join a conference, Call via Work, single number reach, voice mail, and missed calls.</span></span> <span data-ttu-id="8c51c-179">Die Mobilitätsfunktion unterstützt auch *Pushbenachrichtigungen* für mobile Geräte, die das Ausführen von Anwendungen im Hintergrund nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="8c51c-179">The mobility feature also supports *push notifications* for mobile devices that do not support applications running in the background.</span></span> <span data-ttu-id="8c51c-180">Eine Pushbenachrichtigung ist eine an ein mobiles Gerät gesendete Benachrichtigung über ein Ereignis, das auftritt, wenn eine mobile Anwendung inaktiv ist.</span><span class="sxs-lookup"><span data-stu-id="8c51c-180">A push notification is a notification that is sent to a mobile device about an event that occurs while a mobile application is inactive.</span></span>

<span data-ttu-id="8c51c-181">Die Edgeserver umfassen außerdem einen vollständig integrierten XMPP-Proxy (Extensible Messaging and Presence Protocol), wobei das XMPP-Gateway auf den Front-End-Servern integriert ist.</span><span class="sxs-lookup"><span data-stu-id="8c51c-181">Edge Servers also include a fully-integrated Extensible Messaging and Presence Protocol (XMPP) proxy, with an XMPP gateway included on Front End Servers.</span></span> <span data-ttu-id="8c51c-182">Sie können diese XMPP-Komponenten so konfigurieren, dass Ihre lync Server 2013-Benutzer Kontakte aus XMPP-basierten Partnern (wie Google Talk) für Sofortnachrichten und Anwesenheitsinformationen hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="8c51c-182">You can configure these XMPP components to enable your Lync Server 2013 users to add contacts from XMPP-based partners (such as Google Talk) for instant messaging and presence.</span></span>

<span data-ttu-id="8c51c-183">Ausführliche Informationen finden Sie unter [Planen des Zugriffs externer Benutzer in lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="8c51c-183">For details, see [Planning for external user access in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="mediation-server"></a><span data-ttu-id="8c51c-184">Vermittlungsserver</span><span class="sxs-lookup"><span data-stu-id="8c51c-184">Mediation Server</span></span>

<span data-ttu-id="8c51c-185">Mediation Server ist eine notwendige Komponente für die Implementierung von Enterprise-VoIP und Einwahlkonferenzen.</span><span class="sxs-lookup"><span data-stu-id="8c51c-185">Mediation Server is a necessary component for implementing Enterprise Voice and dial-in conferencing.</span></span> <span data-ttu-id="8c51c-186">Der Vermittlungs Server übersetzt Signalisierungen und in einigen Konfigurationen Medien zwischen Ihrer internen lync Server-Infrastruktur und einem PSTN-Gateway (Public Switched Telephone Network), IP-PBX oder einem SIP-Trunk (Session Initiation Protocol).</span><span class="sxs-lookup"><span data-stu-id="8c51c-186">Mediation Server translates signaling, and, in some configurations, media between your internal Lync Server infrastructure and a public switched telephone network (PSTN) gateway, IP-PBX, or a Session Initiation Protocol (SIP) trunk.</span></span> <span data-ttu-id="8c51c-187">Sie können den Vermittlungsserver auf dem gleichen Server wie dem Front-End-Server ausführen oder in einen eigenständigen vermittlungsserverpool unterteilt.</span><span class="sxs-lookup"><span data-stu-id="8c51c-187">You can run Mediation Server collocated on the same server as Front End Server, or separated into a stand-alone Mediation Server pool.</span></span>

<span data-ttu-id="8c51c-188">Ausführliche Informationen finden Sie in der Planning-Dokumentation unter [Mediation Server Component in lync Server 2013](lync-server-2013-mediation-server-component.md) .</span><span class="sxs-lookup"><span data-stu-id="8c51c-188">For details, see [Mediation Server component in Lync Server 2013](lync-server-2013-mediation-server-component.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="director"></a><span data-ttu-id="8c51c-189">Director</span><span class="sxs-lookup"><span data-stu-id="8c51c-189">Director</span></span>

<span data-ttu-id="8c51c-190">Directors können lync Server-Benutzeranforderungen authentifizieren, jedoch keine Benutzerkonten oder Anwesenheits-oder Konferenzdienste.</span><span class="sxs-lookup"><span data-stu-id="8c51c-190">Directors can authenticate Lync Server user requests, but they do not home user accounts or provide presence or conferencing services.</span></span> <span data-ttu-id="8c51c-191">Directors sind zur Verbesserung der Sicherheit insbesondere in Bereitstellungen nützlich, in denen der Zugriff durch externe Benutzer aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="8c51c-191">Directors are most useful to enhance security in deployments that enable external user access.</span></span> <span data-ttu-id="8c51c-192">Der Director kann Anforderungen authentifizieren, bevor sie an interne Server weitergeleitet werden.</span><span class="sxs-lookup"><span data-stu-id="8c51c-192">The Director can authenticate requests before sending them on to internal servers.</span></span> <span data-ttu-id="8c51c-193">Bei Denial-of-Service-Angriffen enden die Angriffe beim Director und erreichen nicht die Front-End-Server.</span><span class="sxs-lookup"><span data-stu-id="8c51c-193">In the case of a denial-of-service attack, the attack ends with the Director and does not reach the Front End servers.</span></span> <span data-ttu-id="8c51c-194">Ausführliche Informationen finden Sie unter [Szenarien für den Director in lync Server 2013](lync-server-2013-scenarios-for-the-director.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="8c51c-194">For details, see [Scenarios for the Director in Lync Server 2013](lync-server-2013-scenarios-for-the-director.md) in the Planning documentation.</span></span>

</div>

<div>

## <a name="persistent-chat-server-roles"></a><span data-ttu-id="8c51c-195">Server Rollen für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="8c51c-195">Persistent Chat Server Roles</span></span>

<span data-ttu-id="8c51c-p121">Durch den beständigen Chat können Benutzer an themenbasierten Unterhaltungen mit mehreren Teilnehmern teilnehmen, die langfristig erhalten bleiben. Auf dem Front-End-Server für beständigen Chat wird der beständige Chatdienst ausgeführt. Auf dem Back-End-Server für beständigen Chat werden die Chatverlaufsdaten sowie Informationen zu Kategorien und Chatrooms gespeichert. Auf dem optionalen Back-End-Server zur Kompatibilität für den beständigen Chat können Chatinhalte sowie Kompatibilitätsereignisse zum Zweck der Einhaltung von Bestimmungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="8c51c-p121">Persistent chat enables users to participate in multiparty, topic-based conversations that persist over time. The Persistent Chat Front End Server runs the persistent chat service. The Persistent Chat Back End Server stores the chat history data, and information about categories and chat rooms. The optional Persistent Chat Compliance Back End Server can store the chat content and compliance events for the purpose of compliance.</span></span>

<span data-ttu-id="8c51c-200">Auf Servern mit lync Server Standard Edition kann auch beständiger Chat auf demselben Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8c51c-200">Servers running Lync Server Standard Edition can also run Persistent chat collocated on the same server.</span></span> <span data-ttu-id="8c51c-201">Der Front-End-Server für beständigen Chat mit Enterprise Edition-Front-End-Server kann nicht collocate werden.</span><span class="sxs-lookup"><span data-stu-id="8c51c-201">You cannot collocate the Persistent Chat Front End Server with Enterprise Edition Front End Server.</span></span>

<span data-ttu-id="8c51c-202">Ausführliche Informationen finden Sie unter [Planen des beständigen Chat Servers in lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="8c51c-202">For details, see [Planning for Persistent Chat Server in Lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8c51c-203">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c51c-203">See Also</span></span>


[<span data-ttu-id="8c51c-204">Vermittlungsserver Komponente in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c51c-204">Mediation Server component in Lync Server 2013</span></span>](lync-server-2013-mediation-server-component.md)  


[<span data-ttu-id="8c51c-205">Planen der Archivierung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c51c-205">Planning for Archiving in Lync Server 2013</span></span>](lync-server-2013-planning-for-archiving.md)  
[<span data-ttu-id="8c51c-206">Planen des Zugriffs externer Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c51c-206">Planning for external user access in Lync Server 2013</span></span>](lync-server-2013-planning-for-external-user-access.md)  
[<span data-ttu-id="8c51c-207">Szenarien für den Director in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c51c-207">Scenarios for the Director in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-the-director.md)  
[<span data-ttu-id="8c51c-208">Planen für den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c51c-208">Planning for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-planning-for-persistent-chat-server.md)  
  

<span data-ttu-id="8c51c-209"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8c51c-209"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

