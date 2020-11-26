---
title: 'Lync Server 2013: Von Reaktionsgruppen verwendete Komponenten'
description: 'Lync Server 2013: von der Reaktionsgruppe verwendete Komponenten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Response Group
ms:assetid: 2b058785-47ca-43b7-b3de-6928a60dc685
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425768(v=OCS.15)
ms:contentKeyID: 48183693
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a1e916d9e4bf986bf0337a6f1f1dd918ff2772e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434557"
---
# <a name="components-used-by-response-group-in-lync-server-2013"></a><span data-ttu-id="be401-103">Von Reaktionsgruppen verwendete Komponenten in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="be401-103">Components used by Response Group in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="be401-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="be401-104">

<span> </span></span></span>

<span data-ttu-id="be401-105">_**Letztes Änderungsdatum des Themas:** 2012-09-11_</span><span class="sxs-lookup"><span data-stu-id="be401-105">_**Topic Last Modified:** 2012-09-11_</span></span>

<span data-ttu-id="be401-106">Die reaktionsgruppenanwendung wird automatisch aktiviert, wenn Sie Enterprise-VoIP bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="be401-106">The Response Group application is automatically enabled when you deploy Enterprise Voice.</span></span> <span data-ttu-id="be401-107">In diesem Abschnitt werden die Komponenten beschrieben, die die reaktionsgruppenanwendung unterstützen.</span><span class="sxs-lookup"><span data-stu-id="be401-107">This section describes the components that support the Response Group application.</span></span>

<div>

## <a name="response-group-components"></a><span data-ttu-id="be401-108">Komponenten der Reaktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="be401-108">Response Group Components</span></span>

<span data-ttu-id="be401-109">Die folgenden Microsoft lync Server 2013-Komponenten unterstützen die reaktionsgruppenanwendung:</span><span class="sxs-lookup"><span data-stu-id="be401-109">The following Microsoft Lync Server 2013 components support the Response Group application:</span></span>

  - <span data-ttu-id="be401-110">**Anwendungsdienst**   Der Anwendungsdienst bietet eine Plattform zum Bereitstellen, hosten und Verwalten von Unified Communications-Anwendungen wie der Reaktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="be401-110">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications applications, such as Response Group.</span></span> <span data-ttu-id="be401-111">Der Anwendungsdienst wird automatisch auf jedem Front-End-Server in einem Front-End-Pool und auf jedem Standard Edition-Server installiert.</span><span class="sxs-lookup"><span data-stu-id="be401-111">The Application service is automatically installed on every Front End Server in a Front End pool and on every Standard Edition server.</span></span>

  - <span data-ttu-id="be401-112">**Reaktionsgruppenanwendung**   Die Antwortgruppen Anwendung ist eine der Unified Communications-Anwendungen, die vom Anwendungsdienst gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="be401-112">**Response Group application**   The Response Group application is one of the unified communications applications that are hosted by Application service.</span></span> <span data-ttu-id="be401-113">Sie wird automatisch einbezogen, wenn Sie die Reaktionsgruppe bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="be401-113">It is included automatically when you deploy Response Group.</span></span> <span data-ttu-id="be401-114">Die Antwortgruppen Anwendung leitet eingehende Anrufe an Gruppen von Agents weiter und Warteschlangen.</span><span class="sxs-lookup"><span data-stu-id="be401-114">The Response Group application routes and queues incoming calls to groups of agents.</span></span>

  - <span data-ttu-id="be401-115">**Sprachpaket**   Für die Unterstützung von Text-zu-Sprache-und Spracherkennung ist ein Sprachpaket erforderlich.</span><span class="sxs-lookup"><span data-stu-id="be401-115">**Language pack**   A language pack is required to support text-to-speech and speech recognition.</span></span> <span data-ttu-id="be401-116">Diese Sprachtechnologien werden zum Konfigurieren von Nachrichten verwendet, beispielsweise für die Willkommensnachricht oder für andere Ansagen sowie für Fragen und Antworten der interaktiven Sprachantwort (Interactive Voice Response, IVR).</span><span class="sxs-lookup"><span data-stu-id="be401-116">These speech technologies are used when you configure messages, such as the welcome message and other prompts, and interactive voice response (IVR) questions and answers.</span></span> <span data-ttu-id="be401-117">Standardmäßig werden die 26 unterstützten Sprachpakete installiert, wenn Sie lync Server 2013 bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="be401-117">By default, the 26 supported language packs are installed when you deploy Lync Server 2013.</span></span>

  - <span data-ttu-id="be401-118">**Audiodateien**   Audiodateien werden für Nachrichten und Musik im Wartebereich verwendet.</span><span class="sxs-lookup"><span data-stu-id="be401-118">**Audio files**   Audio files are used for messages and on-hold music.</span></span>

  - <span data-ttu-id="be401-119">**Dateispeicher**   Die Reaktionsgruppe verwendet den Dateispeicher zum Speichern von Audiodateien.</span><span class="sxs-lookup"><span data-stu-id="be401-119">**File Store**   Response Group uses File store to store audio files.</span></span> <span data-ttu-id="be401-120">Mehrere Antwortgruppen Pools können dieselbe Instanz des Dateispeichers verwenden.</span><span class="sxs-lookup"><span data-stu-id="be401-120">Multiple Response Group pools can use the same instance of File store.</span></span>

  - <span data-ttu-id="be401-121">**Reaktionsgruppen-Konfigurations Tool**   Das Tool für die Reaktionsgruppen-Konfiguration ist ein webbasiertes Tool, das zum Erstellen und Konfigurieren von Reaktionsgruppen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="be401-121">**Response Group Configuration Tool**   The Response Group Configuration Tool is a web-based tool that is used to create and configure response groups.</span></span> <span data-ttu-id="be401-122">Beim Installieren von Webdiensten ist das Tool für die Reaktionsgruppen Konfiguration enthalten.</span><span class="sxs-lookup"><span data-stu-id="be401-122">The Response Group Configuration Tool is included when you install Web Services.</span></span>

  - <span data-ttu-id="be401-123">**Microsoft lync Server 2013-System**   Steuerung   Mit der lync Server-Systemsteuerung können Sie Agentengruppen und-Warteschlangen für Reaktionsgruppen einrichten und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="be401-123">**Microsoft Lync Server 2013 Control Panel**   You can use Lync Server Control Panel to setup and configure agent groups and queues for response groups.</span></span>

  - <span data-ttu-id="be401-124">**Lync Server-Verwaltungsshell**   Alle Einstellungen der Reaktionsgruppe können mithilfe der lync Server-Verwaltungsshell-Cmdlets konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="be401-124">**Lync Server Management Shell**   All Response Group settings can be configured by using Lync Server Management Shell cmdlets.</span></span>

  - <span data-ttu-id="be401-125">**Microsoft lync 2013**   Formelle Agents (Agents, die sich bei der Gruppe anmelden müssen, bevor Sie Anrufe für die Gruppe annehmen können) verwenden Sie lync 2013, um sich bei der Gruppe anzumelden und sich abzumelden.</span><span class="sxs-lookup"><span data-stu-id="be401-125">**Microsoft Lync 2013**   Formal agents (agents who are required to sign in to the group before they can accept calls for the group) use Lync 2013 to sign in to and sign out from the group.</span></span> <span data-ttu-id="be401-126">Wenn eine Agentengruppe für formelle Agents konfiguriert ist, klicken die Agents auf ein Menüelement in lync 2013, um Internet Explorer zu öffnen und eine Webseite-Konsole für die Anmeldung bei der Gruppe anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="be401-126">If an agent group is configured for formal agents, the agents click a menu item in Lync 2013 to open Internet Explorer and display a webpage console for signing in and out of the group.</span></span>

  - <span data-ttu-id="be401-127">**Web Services**   Webdienste sind für das Reaktionsgruppen-Konfigurations Tool, die Anmelde-und Abmelde Konsole des Agents, die lync Server-Systemsteuerung und den Client-Webdienst der Reaktionsgruppe erforderlich.</span><span class="sxs-lookup"><span data-stu-id="be401-127">**Web Services**   Web Services is required for Response Group Configuration Tool, the agents’ sign-in and sign-out console, Lync Server Control Panel, and Response Group client web service.</span></span>

  - <span data-ttu-id="be401-128">**Client-Webdienst für Reaktionsgruppen**   Die Antwortgruppen Anwendung bietet einen Client-Webdienst, der von Drittanbieteranwendungen verwendet werden kann, um Informationen zu Agents, Agentengruppen Mitgliedschaft, Agent-Anmeldestatus, Anrufstatus für Gruppen und die Gruppen abzurufen, die anonyme Anrufe unterstützen.</span><span class="sxs-lookup"><span data-stu-id="be401-128">**Response Group Client Web Service**   Response Group application provides a client web service, which can be used by third-party applications to retrieve information about agents, agent group membership, agent sign-in status, call status for groups, and the groups that support anonymous calls.</span></span> <span data-ttu-id="be401-129">Lync 2013 und lync 2010 Attendant verwenden den Client-Webdienst der Reaktionsgruppe, um die Liste der Antwortgruppen abzurufen, die von Agents für anonyme Anrufe verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="be401-129">Lync 2013 and Lync 2010 Attendant use Response Group Client Web service to retrieve the list of response groups that agents can use to make anonymous calls.</span></span> <span data-ttu-id="be401-130">Der Client-Webdienst ist bei der Installation von Webdiensten enthalten.</span><span class="sxs-lookup"><span data-stu-id="be401-130">The client web service is included when you install Web Services.</span></span>

<span data-ttu-id="be401-131"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="be401-131"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

