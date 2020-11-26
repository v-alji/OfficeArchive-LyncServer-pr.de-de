---
title: Konfigurationsvoraussetzungen und -berechtigungen für Einwahlkonferenzen
description: Voraussetzungen und Berechtigungen für Einwahlkonferenzen
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dial-in conferencing configuration prerequisites and permissions
ms:assetid: b3b251e5-78ac-44a2-8c36-2a061c9b2314
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412865(v=OCS.15)
ms:contentKeyID: 48185165
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: eced67f33e35c711c4fcd31120480b6d5c2e41ce
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429265"
---
# <a name="dial-in-conferencing-configuration-prerequisites-and-permissions-in-lync-server-2013"></a><span data-ttu-id="dab0c-103">Konfigurationsvoraussetzungen und -berechtigungen für Einwahlkonferenzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dab0c-103">Dial-in conferencing configuration prerequisites and permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dab0c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dab0c-104">

<span> </span></span></span>

<span data-ttu-id="dab0c-105">_**Letztes Änderungsdatum des Themas:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="dab0c-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="dab0c-106">Einwahlkonferenzen ist eine optionale Komponente der lync Server 2013-Konferenz Arbeitsauslastung.</span><span class="sxs-lookup"><span data-stu-id="dab0c-106">Dial-in conferencing is an optional component of the Lync Server 2013 Conferencing workload.</span></span> <span data-ttu-id="dab0c-107">Die Komponenten, die Sie installieren müssen, bevor Sie Einwahlkonferenzen konfigurieren können, werden bereitgestellt, wenn Sie die Topologie mithilfe des Topologie-Generators entwerfen und dann Ihren Front-End-Pool oder Standard Edition-Server einrichten.</span><span class="sxs-lookup"><span data-stu-id="dab0c-107">The components you need to install before you can configure dial-in conferencing are deployed when you use the Topology Builder to design your topology and then set up your Front End pool or Standard Edition server.</span></span> <span data-ttu-id="dab0c-108">In diesem Thema wird beschrieben, welche Voraussetzungen erfüllt sein müssen, bevor Sie Einwahlkonferenzen konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="dab0c-108">This topic describes what you need to have accomplished before you can configure dial-in conferencing.</span></span>

<span data-ttu-id="dab0c-109">In diesem Abschnitt wird davon ausgegangen, dass Sie die Planungsabschnitte im Zusammenhang mit der Konferenz Arbeitsauslastung und insbesondere Einwahlkonferenzen gelesen haben.</span><span class="sxs-lookup"><span data-stu-id="dab0c-109">This section assumes that you have read the planning sections related to the Conferencing workload and dial-in conferencing in particular.</span></span>

<div>

## <a name="dial-in-conferencing-configuration-prerequisites"></a><span data-ttu-id="dab0c-110">Voraussetzungen für die Konfiguration von Einwahlkonferenzen</span><span class="sxs-lookup"><span data-stu-id="dab0c-110">Dial-in Conferencing Configuration Prerequisites</span></span>

<span data-ttu-id="dab0c-111">Für Einwahlkonferenzen sind die folgenden lync Server 2013-Komponenten erforderlich:</span><span class="sxs-lookup"><span data-stu-id="dab0c-111">Dial-in conferencing requires the following Lync Server 2013 components:</span></span>

  - <span data-ttu-id="dab0c-112">Unified Communications-Anwendungsdienst (auch nur *Anwendungsdienst* genannt)</span><span class="sxs-lookup"><span data-stu-id="dab0c-112">Unified Communications Application Service (UCAS) (called the *Application service*)</span></span>

  - <span data-ttu-id="dab0c-113">Konferenzzentrale</span><span class="sxs-lookup"><span data-stu-id="dab0c-113">Conferencing Attendant application</span></span>

  - <span data-ttu-id="dab0c-114">Konferenzankündigungsanwendung</span><span class="sxs-lookup"><span data-stu-id="dab0c-114">Conferencing Announcement application</span></span>

  - <span data-ttu-id="dab0c-115">Webseite mit Einstellungen für Einwahlkonferenzen</span><span class="sxs-lookup"><span data-stu-id="dab0c-115">Dial-in Conferencing Settings webpage</span></span>

  - <span data-ttu-id="dab0c-116">Mindestens ein lync Server 2013-Vermittlungsserver und mindestens ein PSTN-Gateway</span><span class="sxs-lookup"><span data-stu-id="dab0c-116">At least one Lync Server 2013 Mediation Server and at least one PSTN gateway</span></span>

<span data-ttu-id="dab0c-117">Diese Komponenten werden bereitgestellt, wenn Sie den Topologie-Generator verwenden, um Ihre Topologie zu definieren und zu veröffentlichen und dann einen Front-End-Pool oder einen Standard Edition-Server bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="dab0c-117">You deploy these components when you use the Topology Builder to define and publish your topology and then deploy a Front End pool or a Standard Edition server.</span></span> <span data-ttu-id="dab0c-118">Wenn Sie Enterprise-VoIP bereitstellen, sollten Sie es bereitstellen, bevor Sie Einwahlkonferenzen konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="dab0c-118">If you are deploying Enterprise Voice, you should deploy it before you configure dial-in conferencing.</span></span> <span data-ttu-id="dab0c-119">Wenn Sie Enterprise-VoIP nicht bereitstellen, können Sie einen Vermittlungs Server und ein PSTN-Gateway (Public Switched Telephone Network) bereitstellen, wenn Sie den Front-End-Pool oder den Standard Edition-Server bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="dab0c-119">If you are not deploying Enterprise Voice, you can deploy a Mediation Server and a public switched telephone network (PSTN) gateway when you deploy your Front End pool or Standard Edition server.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="dab0c-120">Wenn Sie ein Upgrade von Office Communications Server 2007 R2 auf lync Server 2013 durchführen, stellen Sie Einwahlkonferenzen in jedem Pool bereit, den Sie zum Hosten von lync Server 2013-Konferenzen verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="dab0c-120">If you are upgrading from Office Communications Server 2007 R2 to Lync Server 2013, deploy dial-in conferencing in every pool that you plan to use to host Lync Server 2013 conferences.</span></span> <span data-ttu-id="dab0c-121">Details zum Migrieren von Einwahlkonferenzen finden Sie unter <A href="migration-from-office-communications-server-2007-r2-to-lync-server-2013.md">Migration von Office Communications Server 2007 R2 zu lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="dab0c-121">For details about migrating dial-in conferencing, see <A href="migration-from-office-communications-server-2007-r2-to-lync-server-2013.md">Migration from Office Communications Server 2007 R2 to Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="dab0c-122">In diesem Abschnitt wird davon ausgegangen, dass Sie die folgenden Schritte ausgeführt haben:</span><span class="sxs-lookup"><span data-stu-id="dab0c-122">This section assumes that you have done the following:</span></span>

  - <span data-ttu-id="dab0c-123">Sie haben die neuesten Updates für Ihre Office Communications Server 2007 R2-Umgebung angewendet, wenn Sie zu lync Server 2013 migrieren.</span><span class="sxs-lookup"><span data-stu-id="dab0c-123">Applied the latest updates to your Office Communications Server 2007 R2 environment, if you are migrating to Lync Server 2013.</span></span>

  - <span data-ttu-id="dab0c-124">Mithilfe des Topologie-Generators können Sie Ihre Topologie entwerfen und konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="dab0c-124">Used Topology Builder to design and configure your topology.</span></span> <span data-ttu-id="dab0c-125">Wenn Sie die Konferenz Arbeitsauslastung angeben, haben Sie die Option Einwahlkonferenzen ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="dab0c-125">While specifying the Conferencing workload, you selected the dial-in conferencing option.</span></span> <span data-ttu-id="dab0c-126">Details zum Definieren Ihrer Topologie finden Sie unter [definieren und Konfigurieren der Topologie in lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="dab0c-126">For details about defining your topology, see [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md) in the Deployment documentation.</span></span>

  - <span data-ttu-id="dab0c-127">Haben Sie Ihre Topologie veröffentlicht, und richten Sie den Front-End-Pool oder den Standard Edition-Server ein.</span><span class="sxs-lookup"><span data-stu-id="dab0c-127">Published your topology, and set up the Front End pool or Standard Edition server.</span></span> <span data-ttu-id="dab0c-128">Details zum Veröffentlichen der Topologie und zur Installation von lync Server 2013 finden Sie unter [Bereitstellen von lync Server 2013](lync-server-2013-deploying-lync-server.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="dab0c-128">For details about publishing the topology and installing Lync Server 2013, see [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md) in the Deployment documentation.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="dab0c-129">Wenn Sie Ihre veröffentlichte Topologie installieren, wird die Seite Einwahlkonferenzeinstellungen auf dem Front-End-Server oder Standard Edition-Server als Teil von Webdiensten installiert.</span><span class="sxs-lookup"><span data-stu-id="dab0c-129">When you install your published topology, the Dial-in Conferencing Settings webpage is installed on the Front End Server or Standard Edition server as part of Web Services.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="dab0c-130">Wenn Sie den Pfad für den Dateispeicher in Topology Builder nach der Bereitstellung von lync Server 2013 ändern, müssen Sie die Anwendungen für Konferenzzentrale und Konferenz Ankündigungen neu starten, um den neuen Pfad zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="dab0c-130">If you change the path for the File Store in Topology Builder after you deploy Lync Server 2013, you need to restart the Conferencing Attendant and Conferencing Announcement applications to use the new path.</span></span>

    
    </div>

  - <span data-ttu-id="dab0c-131">Enterprise-VoIP bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="dab0c-131">Deployed Enterprise Voice.</span></span> <span data-ttu-id="dab0c-132">Wenn Sie Enterprise-VoIP nicht bereitstellen, haben Sie entweder einen Vermittlungsserver auf dem Enterprise Edition-Front-End-Server oder auf dem Standard Edition-Server zusammengestellt, oder Sie haben einen eigenständigen Vermittlungsserver bereitgestellt, und Sie haben ein PSTN-Gateway bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="dab0c-132">If you are not deploying Enterprise Voice, you either collocated a Mediation Server on the Enterprise Edition Front End Server or the Standard Edition server, or you deployed a stand-alone Mediation Server, and you deployed a PSTN gateway.</span></span> <span data-ttu-id="dab0c-133">Details zur Bereitstellung von Enterprise-VoIP finden Sie unter [Bereitstellen von Enterprise-VoIP in lync Server 2013](lync-server-2013-deploying-enterprise-voice.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="dab0c-133">For details about deploying Enterprise Voice, see [Deploying Enterprise Voice in Lync Server 2013](lync-server-2013-deploying-enterprise-voice.md) in the Deployment documentation.</span></span> <span data-ttu-id="dab0c-134">Details zum Installieren eines eigenständigen Vermittlungsservers und eines PSTN-Gateways finden Sie unter [Bereitstellen von Vermittlungsservern und Definieren von Peers in lync Server 2013](lync-server-2013-deploying-mediation-servers-and-defining-peers.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="dab0c-134">For details about installing a stand-alone Mediation Server and PSTN gateway, see [Deploying Mediation Servers and defining peers in Lync Server 2013](lync-server-2013-deploying-mediation-servers-and-defining-peers.md) in the Deployment documentation.</span></span>

<span data-ttu-id="dab0c-135">Das folgende Flussdiagramm zeigt die Schritte, die Sie ausführen müssen, bevor Sie Einwahlkonferenzen und die Schritte konfigurieren können, die Sie zum Konfigurieren von Einwahlkonferenzen durchführen.</span><span class="sxs-lookup"><span data-stu-id="dab0c-135">The following flowchart shows the steps that you must perform before you can configure dial-in conferencing and the steps that you perform to configure dial-in conferencing.</span></span>

<span data-ttu-id="dab0c-136">**Bereitstellen von Einwahlkonferenzen**</span><span class="sxs-lookup"><span data-stu-id="dab0c-136">**Deploying dial-in conferencing**</span></span>

<span data-ttu-id="dab0c-137">![Bereitstellungs Flussdiagramm für Einwahlkonferenzen](images/Gg412865.fde8c246-b5ed-4323-a6e7-af1983a5ec86(OCS.15).jpg "Bereitstellungs Flussdiagramm für Einwahlkonferenzen")</span><span class="sxs-lookup"><span data-stu-id="dab0c-137">![Dial-in Conferencing Deployment flowchart](images/Gg412865.fde8c246-b5ed-4323-a6e7-af1983a5ec86(OCS.15).jpg "Dial-in Conferencing Deployment flowchart")</span></span>

</div>

<div>

## <a name="dial-in-conferencing-permissions"></a><span data-ttu-id="dab0c-138">Berechtigungen für Einwahlkonferenzen</span><span class="sxs-lookup"><span data-stu-id="dab0c-138">Dial-in Conferencing Permissions</span></span>

<span data-ttu-id="dab0c-139">Zum Konfigurieren von Einwahlkonferenzen müssen Sie die folgenden Verwaltungstools verwenden:</span><span class="sxs-lookup"><span data-stu-id="dab0c-139">To configure dial-in conferencing, you need to use the following administrative tools:</span></span>

  - <span data-ttu-id="dab0c-140">Systemsteuerung für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dab0c-140">Lync Server 2013 Control Panel</span></span>

  - <span data-ttu-id="dab0c-141">Lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="dab0c-141">Lync Server Management Shell</span></span>

<span data-ttu-id="dab0c-142">Sie verwenden diese Verwaltungstools, um Einstellungen für Einwahlkonferenzen und die Wählpläne, Richtlinien und andere Einstellungen zu konfigurieren, die für Einwahlkonferenzen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="dab0c-142">You use these administrative tools to configure dial-in conferencing settings, and the dial plans, policies, and other settings that dial-in conferencing requires.</span></span>

<span data-ttu-id="dab0c-143">Für die Konfiguration von Einwahlkonferenzen sind je nach Aufgabe eine der folgenden Administratorrollen erforderlich:</span><span class="sxs-lookup"><span data-stu-id="dab0c-143">Configuring dial-in conferencing requires any of the following administrative roles, depending on the task:</span></span>

  - <span data-ttu-id="dab0c-144">**CsVoiceAdministrator**   Diese Administratorrolle kann sprachbezogene Einstellungen und Richtlinien erstellen, konfigurieren und verwalten.</span><span class="sxs-lookup"><span data-stu-id="dab0c-144">**CsVoiceAdministrator**   This administrator role can create, configure, and manage voice-related settings and policies.</span></span>

  - <span data-ttu-id="dab0c-145">**CsUserAdministrator**   Diese Administratorrolle kann Benutzer für lync Server aktivieren und deaktivieren und Benutzern vorhandene Richtlinien wie Konferenzrichtlinien und PIN-Richtlinien zuweisen.</span><span class="sxs-lookup"><span data-stu-id="dab0c-145">**CsUserAdministrator**   This administrator role can enable and disable users for Lync Server and assign existing policies, such as conferencing policies and PIN policies, to users.</span></span>

  - <span data-ttu-id="dab0c-146">**CsAdministrator**   Diese Administratorrolle kann alle Aufgaben von CsVoiceAdministrator und CsUserAdministrator ausführen.</span><span class="sxs-lookup"><span data-stu-id="dab0c-146">**CsAdministrator**   This administrator role can perform all of the tasks of CsVoiceAdministrator and CsUserAdministrator.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="dab0c-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dab0c-147">See Also</span></span>


[<span data-ttu-id="dab0c-148">Bereitstellen von Enterprise-VoIP in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dab0c-148">Deploying Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-deploying-enterprise-voice.md)  
  

<span data-ttu-id="dab0c-149"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dab0c-149"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

