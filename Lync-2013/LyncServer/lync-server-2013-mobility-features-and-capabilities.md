---
title: 'Lync Server 2013: Mobilitätsfeatures und -funktionen'
description: 'Lync Server 2013: Mobilitätsfeatures und-Funktionen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Mobility features and capabilities
ms:assetid: 12517a88-2531-44a5-bea5-d8884aff53eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh689983(v=OCS.15)
ms:contentKeyID: 48183457
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20713145c18260f22d9635c34af291e9a7c5ea9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445953"
---
# <a name="mobility-features-and-capabilities-in-lync-server-2013"></a><span data-ttu-id="c8b58-103">Mobilitätsfeatures und -funktionen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c8b58-103">Mobility features and capabilities in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c8b58-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c8b58-104">

<span> </span></span></span>

<span data-ttu-id="c8b58-105">_**Letztes Änderungsdatum des Themas:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="c8b58-105">_**Topic Last Modified:** 2013-02-19_</span></span>

    The information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="c8b58-106">Das Mobilitätsfeature, das in den kumulativen Updates für lync Server 2013: Februar 2013 unterstützt die lync 2010 Mobile-und lync 2013-Funktionen für mobile Clients.</span><span class="sxs-lookup"><span data-stu-id="c8b58-106">The mobility feature introduced in the Cumulative Updates for Lync Server 2013: February 2013 supports Lync 2010 Mobile and Lync 2013 Mobile clients functionality.</span></span> <span data-ttu-id="c8b58-107">Wenn Sie den lync Server 2013-Mobilitätsdienst bereitstellen, können Benutzer unterstützte Apple IOS-, Android-und Windows Phone-oder Nokia Symbian-Mobilgeräte verwenden, um Aktivitäten wie das Senden und empfangen von Sofortnachrichten, das Anzeigen von Kontakten und das Anzeigen von Anwesenheitsfunktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="c8b58-107">When you deploy the Lync Server 2013 Mobility Service, users can use supported Apple iOS, Android, and Windows Phone, or Nokia Symbian mobile devices to perform activities such as sending and receiving instant messages, viewing contacts, and viewing presence.</span></span> <span data-ttu-id="c8b58-108">Darüber hinaus unterstützen Mobile Geräte einige Enterprise-VoIP-Features, wie beispielsweise klicken, um an einer Konferenz teilzunehmen, über Arbeit anzurufen, eine Rufnummer zu erreichen, Voicemail und verpasste Anrufe zu tätigen.</span><span class="sxs-lookup"><span data-stu-id="c8b58-108">In addition, mobile devices support some Enterprise Voice features, such as click to join a conference, Call via Work, single number reach, voice mail, and missed calls.</span></span> <span data-ttu-id="c8b58-109">Neue Features, die in den kumulativen Updates für lync Server 2013: Februar 2013 eingeführt wurden, umfassen VoIP-Funktionen und Video (H. 264) für Besprechungsteilnehmer.</span><span class="sxs-lookup"><span data-stu-id="c8b58-109">New features introduced in the Cumulative Updates for Lync Server 2013: February 2013 include Voice over IP (VoIP) capability and video (H.264) for meeting attendee.</span></span>

<span data-ttu-id="c8b58-110">Das Mobilitätsfeature in den kumulativen Updates für lync Server 2013: Februar 2013 unterstützt die lync 2013-Funktionalität für mobile Clients.</span><span class="sxs-lookup"><span data-stu-id="c8b58-110">The mobility feature introduced in the Cumulative Updates for Lync Server 2013: February 2013 supports Lync 2013 Mobile client functionality.</span></span> <span data-ttu-id="c8b58-111">Die kumulativen Updates für lync Server 2013: Februar 2013 Installieren der Unified Communications Web-API oder UCWA.</span><span class="sxs-lookup"><span data-stu-id="c8b58-111">The Cumulative Updates for Lync Server 2013: February 2013 install Unified Communications Web API, or UCWA.</span></span> <span data-ttu-id="c8b58-112">UCWA ist die Komponente, die für Mobile lync 2013-Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c8b58-112">UCWA is the component used for Lync 2013 Mobile clients.</span></span> <span data-ttu-id="c8b58-113">In lync Server 2013 wird MCX für Mobile lync 2010-Clients verwendet.</span><span class="sxs-lookup"><span data-stu-id="c8b58-113">In Lync Server 2013, Mcx is used for Lync 2010 Mobile clients.</span></span> <span data-ttu-id="c8b58-114">Kumulative Updates für lync Server 2013: Februar 2013 Einführung von UCWA als neuen Einstiegspunkt für Mobilitätsdienste.</span><span class="sxs-lookup"><span data-stu-id="c8b58-114">Cumulative Updates for Lync Server 2013: February 2013 introduce UCWA as the new entry point for mobility services.</span></span> <span data-ttu-id="c8b58-115">Lync Server 2013 implementiert gleichzeitig den Mobilitätsdienst (Mobility Service, MCX), der in den kumulativen Updates für lync Server 2010: November 2011 eingeführt wurde, und bietet Unterstützung für lync 2010 Mobile.</span><span class="sxs-lookup"><span data-stu-id="c8b58-115">Lync Server 2013 concurrently implements the Mobility Service (Mcx), introduced in the Cumulative Updates for Lync Server 2010: November 2011, and provides support for Lync 2010 Mobile.</span></span> <span data-ttu-id="c8b58-116">Wenn Sie die kumulativen Updates für lync Server 2013: Februar 2013 bereitstellen, können Benutzer unterstützte Apple IOS-, Android-und Windows Phone-Mobilgeräte verwenden, um folgende Aktionen auszuführen:</span><span class="sxs-lookup"><span data-stu-id="c8b58-116">When you deploy the Cumulative Updates for Lync Server 2013: February 2013, users can use supported Apple iOS, Android, and Windows Phone mobile devices to perform such activities as:</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c8b58-117">Vom Mobilitätsdienst unterstützte Features aus den kumulativen Updates für lync Server 2010: November 2011 sind mit (MCX) gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="c8b58-117">Features supported by the Mobility Service from the Cumulative Updates for Lync Server 2010: November 2011 are noted with (Mcx).</span></span> <span data-ttu-id="c8b58-118">Alle aufgelisteten Features werden vom UCWA unterstützt, das in den kumulativen Updates für lync Server 2013: Februar 2013 eingeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="c8b58-118">All listed features are supported by the UCWA, introduced in the Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

  - <span data-ttu-id="c8b58-119">Senden und empfangen von Sofortnachrichten (MCX)</span><span class="sxs-lookup"><span data-stu-id="c8b58-119">Send and receive instant messages (Mcx)</span></span>

  - <span data-ttu-id="c8b58-120">Anzeigen von Anwesenheitsinformationen (MCX)</span><span class="sxs-lookup"><span data-stu-id="c8b58-120">View presence (Mcx)</span></span>

  - <span data-ttu-id="c8b58-121">Anzeigen von Kontakten (MCX)</span><span class="sxs-lookup"><span data-stu-id="c8b58-121">View contacts (Mcx)</span></span>

  - <span data-ttu-id="c8b58-122">Klicken Sie, um an einer Konferenz teilzunehmen (MCX)</span><span class="sxs-lookup"><span data-stu-id="c8b58-122">Click to join a conference (Mcx)</span></span>

  - <span data-ttu-id="c8b58-123">Anruf über Arbeit (MCX)</span><span class="sxs-lookup"><span data-stu-id="c8b58-123">Call via work (Mcx)</span></span>

  - <span data-ttu-id="c8b58-124">Erreichbarkeit einer Rufnummer (MCX)</span><span class="sxs-lookup"><span data-stu-id="c8b58-124">Single number reach (Mcx)</span></span>

  - <span data-ttu-id="c8b58-125">Voicemail (MCX)</span><span class="sxs-lookup"><span data-stu-id="c8b58-125">Voice mail (Mcx)</span></span>

  - <span data-ttu-id="c8b58-126">Benachrichtigung über verpasste Anrufe (MCX)</span><span class="sxs-lookup"><span data-stu-id="c8b58-126">Missed call notification (Mcx)</span></span>

  - <span data-ttu-id="c8b58-127">Voice over IP (VoIP)</span><span class="sxs-lookup"><span data-stu-id="c8b58-127">Voice over IP (VoIP)</span></span>

  - <span data-ttu-id="c8b58-128">Teilnehmervideo (H.264)</span><span class="sxs-lookup"><span data-stu-id="c8b58-128">Attendee video (H.264)</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c8b58-129">Lync 2010 Mobile hat einen Client für Nokia Symbian-Geräte bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c8b58-129">Lync 2010 Mobile provided a client for Nokia Symbian devices.</span></span> <span data-ttu-id="c8b58-130">Lync 2013 Mobile hat keinen Client für Nokia Symbian-basierte Geräte.</span><span class="sxs-lookup"><span data-stu-id="c8b58-130">Lync 2013 Mobile will not have a client for Nokia Symbian-based devices.</span></span>



</div>

<span data-ttu-id="c8b58-131">Apple iPad-Benutzer erhalten Zugriff auf Erweiterte Funktionen.</span><span class="sxs-lookup"><span data-stu-id="c8b58-131">Apple iPad users will have access to enhanced capabilities.</span></span> <span data-ttu-id="c8b58-132">Nach dem teilnehmen an einer Besprechung mithilfe des audiorückrufs kann ein iPad-Benutzer hochgeladene Microsoft PowerPoint-Präsentationen in einer Besprechung anzeigen, Anwendungen und Desktops freigeben, die Teilnehmerliste der Besprechung anzeigen und Benachrichtigungen zu anderen Inhaltstypen empfangen, die in der Besprechung freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c8b58-132">After joining a meeting by using audio call back, an iPad user will be able to view uploaded Microsoft PowerPoint presentations within a meeting, share applications and desktops, view the meeting participant list, and receive notifications of other content types that are being shared within the meeting.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="c8b58-133">Mit einer einzelnen Rufnummer erhält ein Nutzer Anrufe auf einem Mobiltelefon, das in die geschäftliche Rufnummer gewählt wurde.</span><span class="sxs-lookup"><span data-stu-id="c8b58-133">With single number reach, a user receives calls on a mobile phone that were dialed to the work number.</span></span> <span data-ttu-id="c8b58-134">Bei Anrufen über Arbeit platziert der Benutzer einen ausgehenden Anruf vom lync Mobile-Client unter Verwendung einer geschäftlichen Telefonnummer anstelle der Mobiltelefonnummer.</span><span class="sxs-lookup"><span data-stu-id="c8b58-134">With Call via Work, the user places an outbound call from the Lync Mobile client by using a work phone number instead of the mobile phone number.</span></span> <span data-ttu-id="c8b58-135">Beim Einwählen sendet der Client eine Anforderung an MCX oder UCWA (basierend auf der lync Mobile-Version), um den Anruf zu tätigen.</span><span class="sxs-lookup"><span data-stu-id="c8b58-135">With dial-out, the client sends a request to Mcx or UCWA (based on the Lync Mobile version) to make the call for them.</span></span> <span data-ttu-id="c8b58-136">Der Server initiiert den Anruf und ruft den Benutzer dann wieder auf dem Mobiltelefon an.</span><span class="sxs-lookup"><span data-stu-id="c8b58-136">The server initiates the call and then calls the user back on the mobile phone.</span></span> <span data-ttu-id="c8b58-137">Wenn der Benutzer antwortet, schließt der Server den Anruf ab, indem er die andere Partei anwählt.</span><span class="sxs-lookup"><span data-stu-id="c8b58-137">When the user answers, the server completes the call by dialing the other party.</span></span> <span data-ttu-id="c8b58-138">Durch die Verwendung von Anruf über die Arbeit können Benutzer Ihre geschäftliche Identität während eines Anrufs aufrecht erhalten, was bedeutet, dass der Anrufempfänger die Handynummer des Anrufers nicht sieht, und der Anrufer die Gebühren für ausgehende Anrufe vermeidet.</span><span class="sxs-lookup"><span data-stu-id="c8b58-138">By using Call via Work, users can maintain their work identity during a call, which means that the call recipient does not see the caller's mobile number, and the caller avoids incurring outbound calling charges.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="c8b58-139">Nicht alle Features funktionieren auf allen mobilen Geräten genau gleich.</span><span class="sxs-lookup"><span data-stu-id="c8b58-139">Not all features work exactly the same on all mobile devices.</span></span> <span data-ttu-id="c8b58-140">Details zu den auf mobilen Geräten unterstützten Features finden Sie in den Vergleichstabellen für mobile Clients unter <A href="https://go.microsoft.com/fwlink/p/?linkid=234777">https://go.microsoft.com/fwlink/p/?LinkId=234777</A> .</span><span class="sxs-lookup"><span data-stu-id="c8b58-140">For details about features supported on mobile devices, see the Mobile Client Comparison Tables at <A href="https://go.microsoft.com/fwlink/p/?linkid=234777">https://go.microsoft.com/fwlink/p/?LinkId=234777</A>.</span></span> <span data-ttu-id="c8b58-141">Ausführliche Informationen zu unterstützten Geräten und Betriebssystemen finden Sie in den Anforderungs Themen unter <A href="lync-server-2013-planning-for-mobile-clients.md">Planen für mobile Clients in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="c8b58-141">For details about supported devices and operating systems, see the requirements topics under <A href="lync-server-2013-planning-for-mobile-clients.md">Planning for mobile clients in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="c8b58-142">Wenn Sie das Feature für die AutoErmittlung in lync Server 2013 verwenden, können mobile Anwendungen lync Server 2013-Webdienste automatisch finden, ohne dass die Benutzer die URLs manuell in Ihre Geräteeinstellungen eingeben müssen.</span><span class="sxs-lookup"><span data-stu-id="c8b58-142">When you use the Lync Server 2013 Autodiscover feature, mobile applications can automatically locate Lync Server 2013 Web Services without requiring users to manually enter the URLs in their device settings.</span></span> <span data-ttu-id="c8b58-143">Die manuelle Eingabe von URLs in Einstellungen für mobile Geräte wird ebenfalls unterstützt, hauptsächlich zur Problembehandlung.</span><span class="sxs-lookup"><span data-stu-id="c8b58-143">Manually entering URLs in mobile device settings is also supported, primarily for troubleshooting purposes.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="c8b58-144">MCX und UCWA sind ﻿kostenlose Dienste, die beide zur Unterstützung von lync 2010 Mobile-und lync 2013-mobilen Clients bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="c8b58-144">The Mcx and UCWA are complimentary services and both are deployed to support Lync 2010 Mobile and Lync 2013 Mobile clients.</span></span> <span data-ttu-id="c8b58-145">Lync 2013 Mobile kann sich bei lync Server 2010-Bereitstellungen nicht anmelden.</span><span class="sxs-lookup"><span data-stu-id="c8b58-145">Lync 2013 Mobile will not be able to sign in to Lync Server 2010 deployments.</span></span> <span data-ttu-id="c8b58-146">Lync 2010 Mobile und lync 2013 Mobile können eine lync Server 2013-Bereitstellung mit den kumulierten Updates für lync Server 2013 verwenden: Februar 2013 angewendet.</span><span class="sxs-lookup"><span data-stu-id="c8b58-146">Lync 2010 Mobile and Lync 2013 Mobile will be able to use a Lync Server 2013 deployment with the Cumulative Updates for Lync Server 2013: February 2013 applied.</span></span>



</div>

<span data-ttu-id="c8b58-147">Die Mobilitätsfunktion unterstützt auch *Pushbenachrichtigungen* für mobile Geräte, die das Ausführen von Anwendungen im Hintergrund nicht unterstützen.</span><span class="sxs-lookup"><span data-stu-id="c8b58-147">The mobility feature also supports *push notifications* for mobile devices that do not support applications running in the background.</span></span> <span data-ttu-id="c8b58-148">Eine Pushbenachrichtigung ist eine an ein mobiles Gerät gesendete Benachrichtigung über ein Ereignis, das auftritt, wenn eine mobile Anwendung inaktiv ist.</span><span class="sxs-lookup"><span data-stu-id="c8b58-148">A push notification is a notification that is sent to a mobile device about an event that occurs while a mobile application is inactive.</span></span> <span data-ttu-id="c8b58-149">So kann beispielsweise eine verpasste sofortnachrichteneinladung zu einer Push-Benachrichtigung führen.</span><span class="sxs-lookup"><span data-stu-id="c8b58-149">For example, a missed instant messaging (IM) invitation can result in a push notification.</span></span>

<span data-ttu-id="c8b58-150">MCX, UCWA, AutoErmittlungsdienst und Support für Push-Benachrichtigungen werden in lync Server 2013 bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="c8b58-150">Mcx, UCWA, Autodiscover Service, and support for push notifications are provided in Lync Server 2013.</span></span> <span data-ttu-id="c8b58-151">Aktualisierte Clientfeatures, Funktionen und die Verwendung von UCWA als Mobilitäts Einstiegspunkt werden in den kumulativen Updates für lync Server 2013: Februar 2013 vorgestellt.</span><span class="sxs-lookup"><span data-stu-id="c8b58-151">Updated client features, capabilities, and the use of UCWA as the mobility entry point are introduced in the Cumulative Updates for Lync Server 2013: February 2013.</span></span>

<span data-ttu-id="c8b58-152"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c8b58-152"></div>

<span> </span>

</div>

</div>

</span></span></div>

