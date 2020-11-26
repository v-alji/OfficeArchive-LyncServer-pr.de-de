---
title: 'Lync Server 2013: Planen von Konferenzen'
description: 'Lync Server 2013: Planen von Konferenzen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for conferencing
ms:assetid: 983a272a-e1b3-4d70-8f84-836b092fe526
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398781(v=OCS.15)
ms:contentKeyID: 48184937
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28e71d185b7be8971c451351aac60dcaaf7eaeda
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443020"
---
# <a name="planning-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="1dccd-103">Planen von Konferenzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1dccd-103">Planning for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1dccd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1dccd-104">

<span> </span></span></span>

<span data-ttu-id="1dccd-105">_**Letztes Änderungsdatum des Themas:** 2013-01-29_</span><span class="sxs-lookup"><span data-stu-id="1dccd-105">_**Topic Last Modified:** 2013-01-29_</span></span>

<span data-ttu-id="1dccd-106">Lync Server 2013 bietet eine Reihe umfassender Konferenzfunktionen:</span><span class="sxs-lookup"><span data-stu-id="1dccd-106">Lync Server 2013 offers a rich set of conferencing capabilities:</span></span>

  - <span data-ttu-id="1dccd-107">Webkonferenzen, einschließlich Dokument Zusammenarbeit, Anwendungsfreigabe und Desktopfreigabe.</span><span class="sxs-lookup"><span data-stu-id="1dccd-107">Web conferencing, which includes document collaboration, application sharing, and desktop sharing.</span></span> <span data-ttu-id="1dccd-108">In lync Server 2013 werden Office Web Apps und der Office Web Apps-Server verwendet, um die Freigabe und das Rendern von PowerPoint-Präsentationen zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="1dccd-108">Lync Server 2013 uses Office Web Apps and the Office Web Apps Server to handle sharing and rendering of PowerPoint presentations.</span></span> <span data-ttu-id="1dccd-109">Details zum Installieren und Konfigurieren des Office Web Apps-Servers finden Sie unter [Konfigurieren der Integration in Office Web Apps Server und lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="1dccd-109">For details about installing and configuring the Office Web Apps Server, see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

  - <span data-ttu-id="1dccd-110">Audio/Video-Konferenzen (A/V), die es Benutzern ermöglichen, Audio-oder Videokonferenzen in Echtzeit zu führen, ohne externe Dienste wie den Microsoft Live-Besprechungs Dienst oder eine Audiobrücke eines Drittanbieters zu benötigen.</span><span class="sxs-lookup"><span data-stu-id="1dccd-110">Audio/video (A/V) conferencing, which enables users to have real-time audio or video conferences without the need for external services such as the Microsoft Live Meeting service or a third-party audio bridge.</span></span>

  - <span data-ttu-id="1dccd-111">Einwahlkonferenzen, die Benutzern die Teilnahme am Audioteil einer lync Server 2013-Konferenz mithilfe eines PSTN-Telefons (Public Switched Telephone Network) ermöglichen, ohne dass ein Drittanbieter für Audiokonferenzen erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="1dccd-111">Dial-in conferencing, which allows users to join the audio portion of a Lync Server 2013 conference by using a public switched telephone network (PSTN) phone without requiring a third-party audio conferencing provider.</span></span>

  - <span data-ttu-id="1dccd-112">Instant Messaging (im)-Konferenzen, bei denen mehr als zwei Parteien in einer einzelnen Chatsitzung kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="1dccd-112">Instant messaging (IM) conferencing, in which more than two parties communicate in a single IM session.</span></span> <span data-ttu-id="1dccd-113">Details zu Chat Konferenzen finden Sie unter [Planen von Front-End-Servern, Sofortnachrichten und Anwesenheitsinformationen in lync Server 2013](lync-server-2013-planning-for-front-end-servers-instant-messaging-and-presence.md).</span><span class="sxs-lookup"><span data-stu-id="1dccd-113">For details about IM conferencing, see [Planning for Front End Servers, instant messaging, and presence in Lync Server 2013](lync-server-2013-planning-for-front-end-servers-instant-messaging-and-presence.md).</span></span>

<span data-ttu-id="1dccd-114">Lync Server 2013 unterstützt sowohl geplante Konferenzen als auch spontane Konferenzen.</span><span class="sxs-lookup"><span data-stu-id="1dccd-114">Lync Server 2013 supports both scheduled conferences and impromptu conferences.</span></span>

<span data-ttu-id="1dccd-115">Wenn Sie lync Server 2013, Front-End-Server, bereitstellen, können Sie auswählen, ob Sie auch Webkonferenzen, A/V-Konferenzen und Funktionen für Einwahlkonferenzen bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="1dccd-115">When you deploy Lync Server 2013, Front End Server, you can choose whether to also deploy the web conferencing, A/V conferencing, and dial-in conferencing capabilities.</span></span> <span data-ttu-id="1dccd-116">Chat-Konferenzfunktionen werden immer automatisch zusammen mit den Chat-Funktionen der Chat Unterhaltungen auf lync Server 2013-Front-End-Servern bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="1dccd-116">IM conferencing capabilities are always automatically deployed along with IM conversation capabilities on Lync Server 2013 Front End Servers.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1dccd-117">Wenn Ihre Bereitstellung Besprechungen umfasst, die mit Office Communicator 2007 R2-Clients (einschließlich der Live Meeting-Konsole oder des Konferenz-Add-Ins für Microsoft Office Outlook) organisiert sind, gelten für die Besprechungen nach der Migration zu lync Server 2013 die folgenden Einschränkungen:</span><span class="sxs-lookup"><span data-stu-id="1dccd-117">If your deployment includes meetings organized using Office Communicator 2007 R2 clients (including the Live Meeting console or Conferencing Add-in for Microsoft Office Outlook), the meetings will have the following limitations after they are migrated to Lync Server 2013:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="1dccd-118">Benutzer in der Besprechung können keine Daten Zusammenarbeitsfeatures verwenden, einschließlich der Zusammenarbeit von Dokumenten, der Anwendungsfreigabe und der Desktopfreigabe.</span><span class="sxs-lookup"><span data-stu-id="1dccd-118">Users in the meeting will not be able to use data collaboration features, including document collaboration, application sharing, and desktop sharing.</span></span></P>
> <LI>
> <P><span data-ttu-id="1dccd-119">Stabilitätsprobleme können auftreten, da Office Communicator 2007 R2-Clients mit lync Server 2013 nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="1dccd-119">Stability issues may arise since Office Communicator 2007 R2 clients are not supported with Lync Server 2013.</span></span></P></LI></UL><span data-ttu-id="1dccd-120">Um diese Probleme zu vermeiden, sollten Sie jede Besprechung, die mit Office Communicator 2007 R2-Clients mit Outlook 2010 oder Outlook 2013 organisiert ist, mithilfe des Online Besprechungs-Add-Ins für lync 2010 oder des Online Besprechungs-Add-Ins für lync 2013 neu planen.</span><span class="sxs-lookup"><span data-stu-id="1dccd-120">To avoid these issues, reschedule any meeting organized using Office Communicator 2007 R2 clients with Outlook 2010 or Outlook 2013 using either the Online Meeting Add-in for Lync 2010 or Online Meeting Add-in for Lync 2013.</span></span>



</div>

<span data-ttu-id="1dccd-121">In den folgenden Abschnitten wird beschrieben, was erforderlich ist, um die verschiedenen Arten von Konferenzfunktionen bereitzustellen, einschließlich des Planungsprozesses, der Komponenten, der Hardware-und Softwareanforderungen sowie des Bereitstellungsprozesses.</span><span class="sxs-lookup"><span data-stu-id="1dccd-121">The following sections describe what is required to deploy the various types of conferencing capabilities, including the planning process, components, hardware and software requirements, and the deployment process.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="1dccd-122">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="1dccd-122">In This Section</span></span>

  - [<span data-ttu-id="1dccd-123">Übersicht über Konferenzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1dccd-123">Overview of conferencing in Lync Server 2013</span></span>](lync-server-2013-overview-of-conferencing.md)

  - [<span data-ttu-id="1dccd-124">Definieren der Anforderungen für Konferenzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1dccd-124">Defining your requirements for conferencing in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-conferencing.md)

  - [<span data-ttu-id="1dccd-125">Komponenten und Topologien für Konferenzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1dccd-125">Components and topologies for conferencing in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-conferencing.md)

  - [<span data-ttu-id="1dccd-126">Technische Anforderungen für Konferenzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1dccd-126">Technical requirements for conferencing in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-conferencing.md)

  - [<span data-ttu-id="1dccd-127">Prüfliste zur Bereitstellung für Konferenzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1dccd-127">Deployment checklist for conferencing in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-conferencing.md)

  - [<span data-ttu-id="1dccd-128">Unterstützung für große Besprechungen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1dccd-128">Support for large meetings in Lync Server 2013</span></span>](lync-server-2013-support-for-large-meetings.md)

<span data-ttu-id="1dccd-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1dccd-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

