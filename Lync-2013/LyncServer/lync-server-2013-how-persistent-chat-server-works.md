---
title: 'Lync Server 2013: Funktionsweise des beständigen Chat Servers'
description: 'Lync Server 2013: Funktionsweise des beständigen Chat Servers'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: How Persistent Chat Server works
ms:assetid: 3d04e9a1-3f0c-458e-bcbe-d27c8c464276
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ683096(v=OCS.15)
ms:contentKeyID: 49684643
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c65df6a13305f75a8a25b85a39688fadf64e476c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427476"
---
# <a name="how-persistent-chat-server-works-in-lync-server-2013"></a><span data-ttu-id="12128-103">Funktionsweise des beständigen Chat Servers in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="12128-103">How Persistent Chat Server works in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="12128-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="12128-104">

<span> </span></span></span>

<span data-ttu-id="12128-105">_**Letztes Änderungsdatum des Themas:** 2012-11-21_</span><span class="sxs-lookup"><span data-stu-id="12128-105">_**Topic Last Modified:** 2012-11-21_</span></span>

<span data-ttu-id="12128-106">Lync Server 2013, beständiger Chat Server ermöglicht Ihnen, an mehrteiligen, themenbasierten Konversationen teilzunehmen, die im Laufe der Zeit fortbestehen.</span><span class="sxs-lookup"><span data-stu-id="12128-106">Lync Server 2013, Persistent Chat Server enables you to participate in multiparty, topic-based conversations that persist over time.</span></span> <span data-ttu-id="12128-107">Der beständige Chat Server kann Ihrer Organisation helfen, Folgendes zu tun:</span><span class="sxs-lookup"><span data-stu-id="12128-107">Persistent Chat Server can help your organization do the following:</span></span>

  - <span data-ttu-id="12128-108">Verbessern der Kommunikation zwischen geografisch verteilten und funktionsübergreifenden Teams</span><span class="sxs-lookup"><span data-stu-id="12128-108">Improve communication between geographically dispersed and cross-functional teams</span></span>

  - <span data-ttu-id="12128-109">Erweitern des Informations Bewusstseins und der Teilnahme</span><span class="sxs-lookup"><span data-stu-id="12128-109">Broaden information awareness and participation</span></span>

  - <span data-ttu-id="12128-110">Verbessern der Kommunikation mit ihrer erweiterten Organisation</span><span class="sxs-lookup"><span data-stu-id="12128-110">Improve communication with your extended organization</span></span>

  - <span data-ttu-id="12128-111">Reduzieren der Informationsüberlastung</span><span class="sxs-lookup"><span data-stu-id="12128-111">Reduce information overload</span></span>

  - <span data-ttu-id="12128-112">Verbessern des Informations Bewusstseins</span><span class="sxs-lookup"><span data-stu-id="12128-112">Improve information awareness</span></span>

  - <span data-ttu-id="12128-113">Verbessern der Verbreitung wichtiger Kenntnisse und Informationen</span><span class="sxs-lookup"><span data-stu-id="12128-113">Increase dispersion of important knowledge and information</span></span>

<span data-ttu-id="12128-114">Sie können den Server für beständigen Chat als optionale Rolle in lync Server 2013 bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="12128-114">You can deploy Persistent Chat Server as an optional role with Lync Server 2013.</span></span> <span data-ttu-id="12128-115">Beständige Chat Dienste werden in einem dedizierten Pool ausgeführt, und ein beständiger Chat Serverpool hängt von einem lync Server-Pool ab, um Nachrichten an ihn weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="12128-115">Persistent Chat services run on a dedicated pool, and a Persistent Chat Server pool depends on a Lync Server pool to route messages to it.</span></span> <span data-ttu-id="12128-116">Clients verwenden eine erweiterbare Chat-Kommunikation über SIP (XCCOS).</span><span class="sxs-lookup"><span data-stu-id="12128-116">Clients use eXtensible Chat Communication Over SIP (XCCOS).</span></span> <span data-ttu-id="12128-117">Die lync Server-Front-End-Server sind so konfiguriert, dass Sie den Datenverkehr an einen beständigen Chat Server Pool weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="12128-117">The Lync Server Front End Servers are configured to route the traffic to a Persistent Chat Server pool.</span></span>

<div>

## <a name="high-level-architecture"></a><span data-ttu-id="12128-118">High-Level Architektur</span><span class="sxs-lookup"><span data-stu-id="12128-118">High-Level Architecture</span></span>

<span data-ttu-id="12128-119">Die folgenden Diagramme bieten allgemeine Perspektiven auf die Architektur und Dienste des beständigen Chat Servers.</span><span class="sxs-lookup"><span data-stu-id="12128-119">The following diagrams provide high-level perspectives of the Persistent Chat Server architecture and services.</span></span>

<span data-ttu-id="12128-120">**Allgemeine Architektur der permanenten Chatserver**</span><span class="sxs-lookup"><span data-stu-id="12128-120">**Persistent Chat Server High-Level Architecture**</span></span>

<span data-ttu-id="12128-121">![Server Architektur für beständigen Chat](images/JJ683096.5db6f36f-4461-4d87-ba77-463b7ffe609b(OCS.15).jpg "Server Architektur für beständigen Chat")</span><span class="sxs-lookup"><span data-stu-id="12128-121">![Persistent Chat Server architecture.](images/JJ683096.5db6f36f-4461-4d87-ba77-463b7ffe609b(OCS.15).jpg "Persistent Chat Server architecture.")</span></span>

<span data-ttu-id="12128-122">**Allgemeine Dienste der permanenten Chatserver**</span><span class="sxs-lookup"><span data-stu-id="12128-122">**Persistent Chat Server High-Level Services**</span></span>

<span data-ttu-id="12128-123">![Server Komponenten für beständigen Chat](images/JJ683096.b6d743aa-3a86-4081-aaef-4fe3257db4e7(OCS.15).jpg "Server Komponenten für beständigen Chat")</span><span class="sxs-lookup"><span data-stu-id="12128-123">![Persistent Chat Server components.](images/JJ683096.b6d743aa-3a86-4081-aaef-4fe3257db4e7(OCS.15).jpg "Persistent Chat Server components.")</span></span>

<span data-ttu-id="12128-124">Auf den Server-Front-End-Servern des beständigen Chats werden zwei Dienste ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="12128-124">Two services run on the Persistent Chat Server Front End Servers:</span></span>

  - <span data-ttu-id="12128-125">Beständiger Chat (Kanal)</span><span class="sxs-lookup"><span data-stu-id="12128-125">Persistent Chat (Channel)</span></span>

  - <span data-ttu-id="12128-126">Compliance</span><span class="sxs-lookup"><span data-stu-id="12128-126">Compliance</span></span>

<div>

## <a name="persistent-chat-channel-service"></a><span data-ttu-id="12128-127">Beständiger Chat (Kanal)-Dienst</span><span class="sxs-lookup"><span data-stu-id="12128-127">Persistent Chat (Channel) Service</span></span>

<span data-ttu-id="12128-128">Der Dienst für beständigen Chat (Kanal) ist der Hauptdienst, der für den persistenten Chat Server verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="12128-128">The Persistent Chat (Channel) service is the core service responsible for Persistent Chat Server.</span></span> <span data-ttu-id="12128-129">Dieser Dienst bietet die folgenden Funktionen:</span><span class="sxs-lookup"><span data-stu-id="12128-129">This service provides the following functions:</span></span>

  - <span data-ttu-id="12128-130">Annahme eingehender Nachrichten</span><span class="sxs-lookup"><span data-stu-id="12128-130">Accepts incoming messages</span></span>

  - <span data-ttu-id="12128-131">Registrierung und Auflistung der Online-Teilnehmer in einem Chatroom für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="12128-131">Registers and lists online participants within a Persistent Chat room</span></span>

  - <span data-ttu-id="12128-132">Neuübermittlung von Nachrichten an andere Abonnenten des Kanals</span><span class="sxs-lookup"><span data-stu-id="12128-132">Retransmits messages to other channel subscribers</span></span>

  - <span data-ttu-id="12128-133">Implementiert die Logik für die Kanalverwaltung, die Einladung zu Chatrooms, die Suche und neue Inhalts Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="12128-133">Implements logic for channel management, chat room invitation, search, and new content notifications</span></span>

<span data-ttu-id="12128-134">Der Dienst für beständigen Chat (Kanal) speichert und greift auf Chatroom-Inhalte und andere Systemmetadaten (Autorisierungsregeln usw.) mithilfe des beständigen Chat Speichers zu.</span><span class="sxs-lookup"><span data-stu-id="12128-134">The Persistent Chat (Channel) service stores and accesses chat room content and other system metadata (authorization rules, and so on) by using the Persistent Chat Store.</span></span> <span data-ttu-id="12128-135">Dieser Dienst speichert Dateien, die in Chatrooms im persistenten Chat-Dateispeicher hochgeladen werden.</span><span class="sxs-lookup"><span data-stu-id="12128-135">This service stores files that are uploaded into chat rooms in the Persistent Chat File Store.</span></span>

</div>

<div>

## <a name="compliance-service"></a><span data-ttu-id="12128-136">Kompatibilitätsdienst</span><span class="sxs-lookup"><span data-stu-id="12128-136">Compliance Service</span></span>

<span data-ttu-id="12128-137">Der Kompatibilitätsdienst ist eine optionale Komponente des Servers für beständigen Chat und ist für das Archivieren von Chat Inhalten und Ereignissen im Compliance Store für beständigen Chat verantwortlich.</span><span class="sxs-lookup"><span data-stu-id="12128-137">The Compliance service is an optional component of Persistent Chat Server and is responsible for archiving chat content and events to the Persistent Chat Compliance Store.</span></span> <span data-ttu-id="12128-138">Wenn es in Ihrer Organisation Vorschriften gibt, nach denen Aktivitäten des beständigen Chats zu archivieren sind, können Sie den optionalen Kompatibilitätsdienst für beständigen Chat bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="12128-138">If your organization has regulations that require Persistent Chat activity to be archived, you can deploy the optional Persistent Chat Compliance service.</span></span> <span data-ttu-id="12128-139">Der Kompatibilitätsdienst wird auf jedem beständigen Chat Server in einem beständigen Chat-Pool installiert.</span><span class="sxs-lookup"><span data-stu-id="12128-139">The Compliance service is installed on each Persistent Chat Server in a Persistent Chat pool.</span></span> <span data-ttu-id="12128-140">Nach der Konfiguration zeichnet die beständige Chat Server-Compliance Benutzeraktivitäten auf, beispielsweise das beitreten und verlassen von Räumen sowie das Posten und Lesen von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="12128-140">When configured, Persistent Chat Server compliance records user activity such as joining and leaving rooms, and posting and reading of messages.</span></span> <span data-ttu-id="12128-141">Der Kompatibilitätsdienst speichert Dateien, die im beständigen Chat-Kompatibilitätsdatei Speicher archiviert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="12128-141">The Compliance service stores files that need to be archived in the Persistent Chat Compliance File Store.</span></span>

</div>

<div>

## <a name="persistent-chat-web-services"></a><span data-ttu-id="12128-142">Beständige Chat-Webdienste</span><span class="sxs-lookup"><span data-stu-id="12128-142">Persistent Chat Web Services</span></span>

<span data-ttu-id="12128-143">Auf den lync Server-Front-End-Servern werden zwei Dienste ausgeführt, die von Internet Informationsdiensten (IIS) abhängen und als Webkomponenten implementiert sind:</span><span class="sxs-lookup"><span data-stu-id="12128-143">On the Lync Server Front End Servers, two services run that depend on Internet Information Services (IIS), and are implemented as web components:</span></span>

  - <span data-ttu-id="12128-144">**Beständige Chat-Webdienste für Datei Upload/-Download** Verantwortlich für das Posten und Abrufen von Dateien aus Chatrooms.</span><span class="sxs-lookup"><span data-stu-id="12128-144">**Persistent Chat Web Services for File Upload/Download** Responsible for posting and retrieving files from chat rooms.</span></span>

  - <span data-ttu-id="12128-145">**Beständige Chat-Webdienste für die Chat Raumverwaltung** Verantwortlich dafür, dass Benutzer die Möglichkeit haben, ihre Chatrooms zu verwalten und neue Chatrooms zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="12128-145">**Persistent Chat Web Services for Chat Room Management** Responsible for providing users the ability to manage their chat rooms, and create new chat rooms.</span></span>

</div>

</div>

<div>

## <a name="how-do-i-start-using-persistent-chat-server"></a><span data-ttu-id="12128-146">Wie beginne ich mit der Verwendung des beständigen Chat Servers?</span><span class="sxs-lookup"><span data-stu-id="12128-146">How Do I Start Using Persistent Chat Server?</span></span>

<span data-ttu-id="12128-147">Der beständige Chat Server ist eine optionale Serverrolle innerhalb der lync Server 2013-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="12128-147">Persistent Chat Server is an optional server role within the Lync Server 2013 infrastructure.</span></span> <span data-ttu-id="12128-148">Wenn Sie die Server Funktion "beständiger Chat" installieren, können alle Benutzer, die über eine Richtlinie von einem Administrator aktiviert wurden, beständigen Chat mit dem lync 2013-Client verwenden.</span><span class="sxs-lookup"><span data-stu-id="12128-148">If you install the Persistent Chat Server role, any users who have been enabled through policy by an administrator can use Persistent Chat with the Lync 2013 client.</span></span>

<span data-ttu-id="12128-149">Ausführliche Informationen zum Bereitstellen eines beständigen Chat Servers und zur Nutzung der Funktionen durch Richtlinien finden Sie unter [Bereitstellen eines beständigen Chat Servers in lync Server 2013](lync-server-2013-deploying-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="12128-149">For details about how to deploy Persistent Chat Server and enable users to leverage the capabilities by policy, see [Deploying Persistent Chat Server in Lync Server 2013](lync-server-2013-deploying-persistent-chat-server.md).</span></span>

<span data-ttu-id="12128-150">Weitere Informationen zum Konfigurieren von Einstellungen für die Bereitstellung von beständigen Chatservern finden Sie unter [Bereitstellen eines beständigen Chat Servers in lync Server 2013](lync-server-2013-deploying-persistent-chat-server.md) und [Verwalten von lync Server 2013, beständiger Chat Server](managing-lync-server-2013-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="12128-150">For details about how to configure settings on your Persistent Chat Server deployment, see [Deploying Persistent Chat Server in Lync Server 2013](lync-server-2013-deploying-persistent-chat-server.md) and [Managing Lync Server 2013, Persistent Chat Server](managing-lync-server-2013-persistent-chat-server.md).</span></span>

<span data-ttu-id="12128-151">Ausführliche Informationen dazu, wie Sie Benutzer nach Richtlinie so aktivieren können, dass Sie die Funktionalität des beständigen Chats in lync 2013-Client nutzen können, finden Sie unter [Bereitstellen eines persistenten Chat Servers in lync Server 2013](lync-server-2013-deploying-persistent-chat-server.md) und [Verwalten von lync Server 2013, beständiger Chat Server](managing-lync-server-2013-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="12128-151">For details about how to enable users by policy such that they can leverage Persistent Chat functionality in Lync 2013 client, see [Deploying Persistent Chat Server in Lync Server 2013](lync-server-2013-deploying-persistent-chat-server.md) and [Managing Lync Server 2013, Persistent Chat Server](managing-lync-server-2013-persistent-chat-server.md).</span></span>

<span data-ttu-id="12128-152">Wenn Sie die Compliance für beständigen Chat bereitgestellt haben, finden Sie weitere Informationen zum Konfigurieren von Einstellungen für die Kompatibilität unter [Verwalten von lync Server 2013, beständiger Chat Server](managing-lync-server-2013-persistent-chat-server.md) .</span><span class="sxs-lookup"><span data-stu-id="12128-152">If you deployed Persistent Chat compliance, see [Managing Lync Server 2013, Persistent Chat Server](managing-lync-server-2013-persistent-chat-server.md) for details about how to configure settings for compliance.</span></span>

</div>

<div>

## <a name="persistent-chat-call-flows"></a><span data-ttu-id="12128-153">Beständige Chat-Anruf Flüsse</span><span class="sxs-lookup"><span data-stu-id="12128-153">Persistent Chat Call Flows</span></span>

<span data-ttu-id="12128-154">Der beständige Chat-Client kommuniziert mit dem beständigen Chatdienst mithilfe von XCCOS.</span><span class="sxs-lookup"><span data-stu-id="12128-154">The Persistent Chat client communicates with the Persistent Chat service by using XCCOS.</span></span> <span data-ttu-id="12128-155">In den folgenden Sequenzen werden der Anmeldevorgang und ein typisches Raum Abonnement und ein Nachrichten Post Szenario beschrieben.</span><span class="sxs-lookup"><span data-stu-id="12128-155">The following sequences describe the sign-in process and a typical room subscription and message post scenario.</span></span>

<div>

## <a name="sign-in"></a><span data-ttu-id="12128-156">Anmeldung</span><span class="sxs-lookup"><span data-stu-id="12128-156">Sign-in</span></span>

<span data-ttu-id="12128-157">Das folgende Anruffluss Diagramm und die folgenden Schritte beschreiben den Anmeldeprozess.</span><span class="sxs-lookup"><span data-stu-id="12128-157">The following call flow diagram and steps describe the sign-in process.</span></span>

<span data-ttu-id="12128-158">**Beständiger Chat-Client-Anmelde Anruffluss**</span><span class="sxs-lookup"><span data-stu-id="12128-158">**Persistent Chat Client Sign-in Call Flow**</span></span>

<span data-ttu-id="12128-159">![Anruffluss Diagramm für beständigen Chat Server](images/JJ683096.9b3b3c61-caca-42b6-853c-6a09e6ff5c44(OCS.15).jpg "Anruffluss Diagramm für beständigen Chat Server")</span><span class="sxs-lookup"><span data-stu-id="12128-159">![Persistent Chat Server call flow diagram.](images/JJ683096.9b3b3c61-caca-42b6-853c-6a09e6ff5c44(OCS.15).jpg "Persistent Chat Server call flow diagram.")</span></span>

1.  <span data-ttu-id="12128-160">Der beständige Chat-Client sendet zunächst ein SIP-Abonnement, um das in-Band-Bereitstellungs Dokument vom Server abzurufen.</span><span class="sxs-lookup"><span data-stu-id="12128-160">The Persistent Chat client first sends a SIP SUBSCRIBE to retrieve the in-band provisioning document from the server.</span></span> <span data-ttu-id="12128-161">Dieses Dokument zeigt an, ob der beständige Chat für den Benutzer aktiviert oder deaktiviert ist, und die Liste der SIP-URIs für den Server Pool des beständigen Chats.</span><span class="sxs-lookup"><span data-stu-id="12128-161">This document indicates if Persistent Chat is enabled or disabled for the user and the list of SIP URIs for the Persistent Chat Server pool.</span></span>

2.  <span data-ttu-id="12128-162">Der beständige Chat-Client sendet eine SIP-Einladungsnachricht an den SIP-URI des beständigen Chat Servers, der im vorherigen Schritt abgerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="12128-162">The Persistent Chat client sends a SIP INVITE message to the SIP URI of the Persistent Chat Server that it obtained in the previous step.</span></span> <span data-ttu-id="12128-163">Auf die Einladungs Sequenz folgt 200 OK und ACK, und der beständige Chat-Client hat nun eine SIP-Sitzung mit einem beständigen Chat Server-Endpunkt geöffnet.</span><span class="sxs-lookup"><span data-stu-id="12128-163">The INVITE sequence is followed by 200 OK and ACK, and the Persistent Chat client has now opened a SIP session with a Persistent Chat Server endpoint.</span></span> <span data-ttu-id="12128-164">Infolgedessen kommuniziert der beständige Chat-Client mit dem beständigen Chat Server durch Senden von SIP-Info-Nachrichten, die entweder Chat Nachrichten oder Befehle enthalten, die den Server zum Ausführen einer Aktion anfordern.</span><span class="sxs-lookup"><span data-stu-id="12128-164">Consequently, the Persistent Chat client communicates with Persistent Chat Server by sending SIP INFO messages that contain either chat messages or commands requesting the server to take an action.</span></span> <span data-ttu-id="12128-165">Alle diese Nachrichten werden bestätigt, wenn der 200 OK-oder 503-Dienst nicht verfügbar ist (im Fall einer starken Serverauslastung).</span><span class="sxs-lookup"><span data-stu-id="12128-165">All of these messages are acknowledged with either 200 OK or 503 Service Unavailable (that is, in the event of heavy server load).</span></span> <span data-ttu-id="12128-166">Wenn der Client eine 503-Antwort erhält, wird die Nachricht erneut versucht.</span><span class="sxs-lookup"><span data-stu-id="12128-166">If the client receives a 503 response, it will retry the message.</span></span> <span data-ttu-id="12128-167">(In diesem Beispiel ist keine 503-Antwort eingeschlossen.) Wenn der Server die Nachricht oder den Befehl akzeptiert und 200 OK sendet, stellt er eine Antwort an den Client in Form einer separaten SIP-INFO Nachricht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="12128-167">(This example does not include a 503 response.) If the server accepts the message or command and sends 200 OK, it provides a response to the client in the form of a separate SIP INFO message.</span></span> <span data-ttu-id="12128-168">Diese Antwort enthält einen Verweis auf den ursprünglichen Befehl.</span><span class="sxs-lookup"><span data-stu-id="12128-168">This response includes a reference to the originating command.</span></span>

3.  <span data-ttu-id="12128-169">Der beständige Chat-Client sendet eine SIP-INFO-Nachricht mit dem Befehl XCCOS **getServerInfo** .</span><span class="sxs-lookup"><span data-stu-id="12128-169">The Persistent Chat client sends a SIP INFO message that contains the XCCOS **getserverinfo** command.</span></span> <span data-ttu-id="12128-170">Der beständige Chat Server antwortet mit einer neuen SIP-INFO Nachricht, die Informationen zur Konfiguration des beständigen Chats enthält.</span><span class="sxs-lookup"><span data-stu-id="12128-170">Persistent Chat Server replies with a new SIP INFO message that contains information about the Persistent Chat service configuration.</span></span>

4.  <span data-ttu-id="12128-171">Der beständige Chat-Client sendet eine SIP-INFO-Nachricht, die den Befehl XCCOS **GetAssociations** enthält.</span><span class="sxs-lookup"><span data-stu-id="12128-171">The Persistent Chat client sends a SIP INFO message that contains the XCCOS **getassociations** command.</span></span> <span data-ttu-id="12128-172">Der beständige Chat Server antwortet mit einer neuen SIP-INFO Nachricht, die die Liste der Chatrooms enthält, in denen der Benutzer Mitglied ist.</span><span class="sxs-lookup"><span data-stu-id="12128-172">Persistent Chat Server replies with a new SIP INFO message that contains the list of rooms of which the user is a member.</span></span> <span data-ttu-id="12128-173">Der beständige Chat-Client wiederholt den Befehl, um die Liste der Räume abzurufen, deren Manager der Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="12128-173">The Persistent Chat client repeats the command to retrieve the list of rooms of which the user is a manager.</span></span>

5.  <span data-ttu-id="12128-174">Der beständige Chat-Client ruft die Liste der befolgten Räume aus dem Dokument "Anwesenheit" ab, in dem jeder befolgte Raum durch eine Kategorie "roomSetting" dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="12128-174">The Persistent Chat client gets the list of followed rooms from the "presence" document, where each followed room is represented by a "roomSetting" category.</span></span> <span data-ttu-id="12128-175">Alle folgenden Chatrooms werden durch eine einzelne SIP-INFO Nachricht verbunden, die den Befehl XCCOS **btreten** enthält, der die Liste der Raum-URIs enthält.</span><span class="sxs-lookup"><span data-stu-id="12128-175">All followed rooms are joined by a single SIP INFO message that contains the XCCOS **bjoin** command that contains the list of room URIs.</span></span> <span data-ttu-id="12128-176">Da die Liste der nachverfolgten Räume auf dem Server gespeichert wird, verfügt jeder Client auf einem Computer über die gleiche Liste der folgenden Chatrooms für den angegebenen Benutzer-URI.</span><span class="sxs-lookup"><span data-stu-id="12128-176">Because the list of followed rooms is kept on the server, any client on any computer has the same list of followed rooms for the specified user URI.</span></span> <span data-ttu-id="12128-177">Der beständige Chat-Client speichert auch die Liste der geöffneten Chatrooms (wenn diese Option vom Benutzer aktiviert ist) in der Registrierung des lokalen Computers und verknüpft jeden dieser Chatrooms bei der Anmeldung durch Senden einer SIP-INFO Nachricht, die den XCCOS- **Join** -Befehl für jeden geöffneten Chatroom enthält.</span><span class="sxs-lookup"><span data-stu-id="12128-177">The Persistent Chat client also keeps the list of opened rooms (if this option is enabled by the user) in the local computer registry, and joins each of these rooms at sign-in by sending a SIP INFO message that contains the XCCOS **join** command for each opened room.</span></span> <span data-ttu-id="12128-178">Da diese Liste in der Registrierung aufbewahrt wird, kann Sie bei zwei beständigen Chat-Clients unterschiedlich sein, die auf unterschiedlichen Computern ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="12128-178">Because this list is kept in the registry, it can be different on two Persistent Chat clients running on different computers.</span></span>

6.  <span data-ttu-id="12128-179">Für jeden beige tretenen Chatroom sendet der beständige Chat-Client eine SIP-INFO-Nachricht, die den Befehl XCCOS **bccontext** enthält.</span><span class="sxs-lookup"><span data-stu-id="12128-179">For each room joined, the Persistent Chat client sends a SIP INFO message that contains the XCCOS **bccontext** command.</span></span> <span data-ttu-id="12128-180">Der beständige Chat Server antwortet mit einer neuen SIP-INFO Nachricht, die die neueste Chatnachricht im Chatroom enthält.</span><span class="sxs-lookup"><span data-stu-id="12128-180">Persistent Chat Server replies with a new SIP INFO message that contains the most recent chat message in the room.</span></span>

7.  <span data-ttu-id="12128-181">Der beständige Chat-Client sendet eine SIP-INFO-Nachricht, die eine XCCOS- **GetInv** (also Einladung) enthält, um neue Raum Einladungen anzufordern, die der Kunde noch nicht gesehen hat.</span><span class="sxs-lookup"><span data-stu-id="12128-181">The Persistent Chat client sends a SIP INFO message that contains a XCCOS **getinv** (that is, get invitation) command to request any new room invitations that the client has not yet seen.</span></span> <span data-ttu-id="12128-182">In einer separaten SIP-INFO Nachricht gibt der beständige Chat Server eine Liste dieser Chatrooms zurück.</span><span class="sxs-lookup"><span data-stu-id="12128-182">In a separate SIP INFO message, Persistent Chat Server returns a list of those rooms.</span></span>

</div>

<div>

## <a name="subscribe-to-a-room-and-post-a-message"></a><span data-ttu-id="12128-183">Abonnieren eines Chatrooms und Posten einer Nachricht</span><span class="sxs-lookup"><span data-stu-id="12128-183">Subscribe to a Room and Post a Message</span></span>

<span data-ttu-id="12128-184">Das folgende Anruffluss Diagramm und die folgenden Schritte beschreiben ein typisches Raum Abonnement und ein Nachrichten Post Szenario.</span><span class="sxs-lookup"><span data-stu-id="12128-184">The following call flow diagram and steps describe a typical room subscription and message post scenario.</span></span>

<span data-ttu-id="12128-185">**Beständiger Chat-Client Raum-Abonnement und Nachrichten Buchung-Anruffluss**</span><span class="sxs-lookup"><span data-stu-id="12128-185">**Persistent Chat Client Room Subscription and Message Posting Call Flow**</span></span>

<span data-ttu-id="12128-186">![Szenario für Raum Abonnements und Nachrichten](images/JJ683096.2d3c417e-c91b-42bd-964e-285b72bb2e44(OCS.15).jpg "Szenario für Raum Abonnements und Nachrichten")</span><span class="sxs-lookup"><span data-stu-id="12128-186">![Room subscription and message post scenario.](images/JJ683096.2d3c417e-c91b-42bd-964e-285b72bb2e44(OCS.15).jpg "Room subscription and message post scenario.")</span></span>

1.  <span data-ttu-id="12128-187">Im beständigen Chat-Client klickt Benutzer1 auf **an einem Chatroom teilnehmen**, klickt auf **Suchen** und gibt dann einige Suchkriterien ein.</span><span class="sxs-lookup"><span data-stu-id="12128-187">From the Persistent Chat client, User1 clicks **Join a Chat Room**, clicks **Search**, and then enters some search criteria.</span></span> <span data-ttu-id="12128-188">Der beständige Chat-Client sendet eine SIP-INFO-Nachricht, die den Befehl XCCOS **chansrch** (Raum Suche) zusammen mit den Suchkriterien enthält.</span><span class="sxs-lookup"><span data-stu-id="12128-188">The Persistent Chat client sends a SIP INFO message that contains the XCCOS **chansrch** (room search) command, along with the search criteria.</span></span> <span data-ttu-id="12128-189">Der beständige Chat Server fragt die Back-End-Datenbank ab und antwortet in einer neuen SIP-INFO Nachricht, die eine Liste der verfügbaren Räume enthält, die den Suchkriterien entsprechen.</span><span class="sxs-lookup"><span data-stu-id="12128-189">Persistent Chat Server queries the back-end database and replies in a new SIP INFO message that contains a list of available rooms that meet the search criteria.</span></span>

2.  <span data-ttu-id="12128-190">Benutzer1 wählt den Chatroom aus, dem er beitreten möchte, und klickt dann auf **diesem Chatroom folgen**.</span><span class="sxs-lookup"><span data-stu-id="12128-190">User1 selects the chat room that he or she wants to join, and then clicks **Follow this room**.</span></span> <span data-ttu-id="12128-191">Der beständige Chat-Client sendet beständigen Chat Server eine SIP-INFO-Nachricht, die den XCCOS- **Join** -Befehl und die Raum-ID des Chatrooms enthält, den der Benutzer ausgewählt hat.</span><span class="sxs-lookup"><span data-stu-id="12128-191">The Persistent Chat client sends Persistent Chat Server a SIP INFO message that contains the XCCOS **join** command and the room ID of the chat room that the user selected.</span></span> <span data-ttu-id="12128-192">Der beständige Chat Server antwortet mit einer SIP-INFO Nachricht, die die Bereitstellungsdaten enthält.</span><span class="sxs-lookup"><span data-stu-id="12128-192">Persistent Chat Server replies with a SIP INFO message that contains the provisioning data.</span></span>

3.  <span data-ttu-id="12128-193">Der beständige Chat-Client sendet beständigen Chat Server eine SIP-INFO-Nachricht, die den Befehl XCCOS **bccontext** (Backchat-Kontext) enthält.</span><span class="sxs-lookup"><span data-stu-id="12128-193">The Persistent Chat client sends Persistent Chat Server a SIP INFO message that contains the XCCOS **bccontext** (backchat context) command.</span></span> <span data-ttu-id="12128-194">Der beständige Chat Server Ruft das Chat-Protokoll ab und gibt es in einer separaten SIP-INFO-Nachricht an den beständigen Chat-Client zurück.</span><span class="sxs-lookup"><span data-stu-id="12128-194">Persistent Chat Server retrieves the chat history, and returns it to the Persistent Chat client in a separate SIP INFO message.</span></span> <span data-ttu-id="12128-195">An diesem Punkt wechselt der Benutzer in den Chatroom und kann teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="12128-195">At this point, the user enters the chat room and is ready to participate.</span></span>

4.  <span data-ttu-id="12128-196">Benutzer1 gibt eine neue Nachricht ein und klickt dann auf **senden**.</span><span class="sxs-lookup"><span data-stu-id="12128-196">User1 enters a new message, and then clicks **Send**.</span></span> <span data-ttu-id="12128-197">Der beständige Chat-Client Bucht die Nachricht in einem Chatroom in einem SIP-Info-XCCOS **grpchat** Befehl.</span><span class="sxs-lookup"><span data-stu-id="12128-197">The Persistent Chat client posts the message to the chat room in a SIP INFO XCCOS **grpchat** command.</span></span> <span data-ttu-id="12128-198">Der beständige Chat Server speichert eine Kopie dieser neuen Nachricht in der Back-End-Datenbank des beständigen Chats.</span><span class="sxs-lookup"><span data-stu-id="12128-198">Persistent Chat Server stores a copy of this new message in the Persistent Chat back-end database.</span></span>

5.  <span data-ttu-id="12128-199">Der beständige Chat Server sendet eine separate Kopie der SIP-Info-XCCOS **grpchat** -Nachricht an User2, der den Chatroom bereits betreten hat.</span><span class="sxs-lookup"><span data-stu-id="12128-199">Persistent Chat Server sends a separate copy of the SIP INFO XCCOS **grpchat** message to User2, who has already entered the chat room.</span></span>

</div>

</div>

<div>

## <a name="persistent-chat-compliance-call-flows"></a><span data-ttu-id="12128-200">Compliance-Anruf Flüsse für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="12128-200">Persistent Chat Compliance Call Flows</span></span>

<span data-ttu-id="12128-201">Der Server für beständigen Chat verwendet Message Queuing (auch als MSMQ bezeichnet) und eine zusätzliche Kompatibilitätsdatenbank (mgccomp), um Kompatibilitätsdaten zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="12128-201">Persistent Chat Server uses Message Queuing (also known as MSMQ) and an additional compliance database (mgccomp) to process compliance data.</span></span> <span data-ttu-id="12128-202">Als Beispiel für die Verarbeitung von Kompatibilitäts Ereignissen beschreibt die folgende Abfolge von Ereignissen, wie ein Nachrichten Post-Ereignis verarbeitet wird.</span><span class="sxs-lookup"><span data-stu-id="12128-202">As an example of how compliance events are processed, the following sequence of events describes how a message post event is processed.</span></span>

1.  <span data-ttu-id="12128-203">Ein Benutzer Bucht eine Nachricht in einem Raum.</span><span class="sxs-lookup"><span data-stu-id="12128-203">A user posts a message to a room.</span></span>

2.  <span data-ttu-id="12128-204">Der Server für beständigen Chat platziert Informationen, die sich auf das Ereignis beziehen, in einer privaten Message Queuing-Warteschlange.</span><span class="sxs-lookup"><span data-stu-id="12128-204">Persistent Chat Server places information pertaining to the event in a private Message Queuing queue.</span></span>

3.  <span data-ttu-id="12128-205">Der beständige Chat-Kompatibilitätsserver liest dieses Ereignis aus der Warteschlange und platziert es zur späteren Verarbeitung in der mgccomp-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="12128-205">Persistent Chat Compliance server reads this event from the queue, and places it into the mgccomp database for processing later.</span></span>

4.  <span data-ttu-id="12128-206">Der beständige Chat-Kompatibilitätsserver verarbeitet in regelmäßigen Abständen eine Reihe von Ereignissen in der Datenbank und sendet Sie zur Verarbeitung an den Compliance-Adapter für beständigen Chat.</span><span class="sxs-lookup"><span data-stu-id="12128-206">Periodically, the Persistent Chat Compliance server processes a set of events in the database, and sends them to the Persistent Chat Compliance adapter for processing.</span></span>

5.  <span data-ttu-id="12128-207">Wenn der Adapter die Daten erfolgreich verarbeitet, löscht der beständige Chat-Kompatibilitätsserver die Ereignisse aus der mgccomp-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="12128-207">If the adapter successfully processes the data, Persistent Chat Compliance server deletes the events from the mgccomp database.</span></span>

<span data-ttu-id="12128-208"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="12128-208"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

