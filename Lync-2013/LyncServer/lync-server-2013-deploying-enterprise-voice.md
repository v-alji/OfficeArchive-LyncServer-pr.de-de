---
title: 'Lync Server 2013: Bereitstellen von Enterprise-VoIP'
description: 'Lync Server 2013: Bereitstellen von Enterprise-VoIP'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Enterprise Voice
ms:assetid: b5b593a6-ac30-461c-8c8c-0041e2c9ab04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412876(v=OCS.15)
ms:contentKeyID: 48185207
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5cc1c891d81db158c1d28e4a3e918a9dae37744c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430014"
---
# <a name="deploying-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="65de7-103">Bereitstellen von Enterprise-VoIP in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-103">Deploying Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="65de7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="65de7-104">

<span> </span></span></span>

<span data-ttu-id="65de7-105">_**Letztes Änderungsdatum des Themas:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="65de7-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="65de7-106">Lync Server 2013, Enterprise-VoIP ist Teil der lync Server 2013-Infrastruktur.</span><span class="sxs-lookup"><span data-stu-id="65de7-106">Lync Server 2013, Enterprise Voice is part of the Lync Server 2013 infrastructure.</span></span>

<span data-ttu-id="65de7-107">Zur Bereitstellung von Enterprise-VoIP müssen Sie Folgendes ausführen:</span><span class="sxs-lookup"><span data-stu-id="65de7-107">Deploying Enterprise Voice requires that you:</span></span>

<div id="sectionSection0" class="section">

1.  <span data-ttu-id="65de7-108">Lesen Sie den Abschnitt [Planning for Enterprise Voice in lync Server 2013](lync-server-2013-planning-for-enterprise-voice.md) der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="65de7-108">Review the [Planning for Enterprise Voice in Lync Server 2013](lync-server-2013-planning-for-enterprise-voice.md) section of the Planning documentation.</span></span>

2.  <span data-ttu-id="65de7-109">Abschließen von Plänen für Features und Komponenten, die mit dieser Arbeitsauslastung bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="65de7-109">Finalize plans for features and components to deploy with this workload.</span></span>

3.  <span data-ttu-id="65de7-110">Führen Sie das Planungs Tool aus, um eine Topologie zu entwerfen, die ihre Bereitstellungsentscheidungen widerspiegelt.</span><span class="sxs-lookup"><span data-stu-id="65de7-110">Run Planning Tool to design a topology that reflects your deployment decisions.</span></span>

4.  <span data-ttu-id="65de7-111">Öffnen Sie den Topologie-Entwurf im Topologie-Generator, wie unter [definieren und Konfigurieren der Topologie in lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md) in der Bereitstellungsdokumentation beschrieben.</span><span class="sxs-lookup"><span data-stu-id="65de7-111">Open the topology design in Topology Builder, as described in [Defining and configuring the topology in Lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md) in the Deployment documentation.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="65de7-112">Die Installation des Topologie-Generators ist Teil des Bereitstellungsprozesses für den internen Pool.</span><span class="sxs-lookup"><span data-stu-id="65de7-112">Installation of Topology Builder is part of the deployment process for the internal pool.</span></span> <span data-ttu-id="65de7-113">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-install-lync-server-administrative-tools.md">Installieren von lync Server 2013-Verwaltungstools</A> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="65de7-113">For details, see <A href="lync-server-2013-install-lync-server-administrative-tools.md">Install Lync Server 2013 administrative tools</A> in the Deployment documentation.</span></span>

    
    </div>

<span data-ttu-id="65de7-114">Darüber hinaus müssen Sie lync Server, Enterprise Edition, auf zentralen Websites und Zweigstellen bereitgestellt haben, die der von Ihnen bereitzustellenden Referenztopologie entsprechen.</span><span class="sxs-lookup"><span data-stu-id="65de7-114">Additionally, you must have already deployed Lync Server, Enterprise Edition at central sites and branch sites that correspond to the reference topology that you choose to deploy.</span></span> <span data-ttu-id="65de7-115">Sie können Enterprise-VoIP-Komponenten erst bereitstellen, nachdem Sie Dateien für mindestens einen internen Pool definiert, veröffentlicht und installiert haben, und Sie müssen den Topologie-Generator verwenden, um einen internen Pool zu definieren und zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="65de7-115">You can’t deploy Enterprise Voice components until you have defined, published, and installed files for at least one internal pool, and you must use Topology Builder to define and publish an internal pool.</span></span>

</div>

<div id="sectionSection1" class="section">

<div class="subSection">

<span data-ttu-id="65de7-116">Informationen zum Anzeigen von Referenz Topologien mit Beispielen für die Bereitstellung von Enterprise-VoIP-Serverrollen (und deren Beziehung zu einem anderen und anderen lync Server 2013-Serverrollen) finden Sie unter [Referenz Topologien in lync Server 2013](lync-server-2013-reference-topologies.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="65de7-116">To view reference topologies with examples of where Enterprise Voice server roles can be deployed (and their relationship to one another and other Lync Server 2013 server roles), see [Reference topologies in Lync Server 2013](lync-server-2013-reference-topologies.md) in the Planning documentation.</span></span>

<span data-ttu-id="65de7-117">Informationen zum Anzeigen einer Referenztopologie, die eine Beispielbereitstellung für die Anrufsteuerung, einschließlich netzwerkregionen, Netzwerk Websites und Subnetzen, veranschaulicht und erläutert, finden Sie unter [Beispiel: Sammeln Ihrer Anforderungen für die Anrufsteuerung in lync Server 2013](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="65de7-117">To view a reference topology that illustrates and explains a sample call admission control deployment, including network regions, network sites, and subnets, see [Example: Gathering your requirements for call admission control in Lync Server 2013](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md) in the Planning documentation.</span></span>

</div>

</div>

<div id="sectionSection2" class="section">

<div>


> [!IMPORTANT]  
> <span data-ttu-id="65de7-118">Wenn Sie Enterprise-VoIP an einem zentralen Standort bereitstellen möchten, lesen Sie die Themen in diesem Abschnitt weiter.</span><span class="sxs-lookup"><span data-stu-id="65de7-118">To deploy Enterprise Voice at a central site, continue reading the topics in this section.</span></span> <span data-ttu-id="65de7-119">Wenn Sie Enterprise-VoIP an einer Zweigstelle bereitstellen möchten, wechseln Sie zum bereit <A href="lync-server-2013-deploying-branch-sites.md">Stellen von Zweigstellen in lync Server 2013</A> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="65de7-119">To deploy Enterprise Voice at a branch site, skip to <A href="lync-server-2013-deploying-branch-sites.md">Deploying branch sites in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<span data-ttu-id="65de7-120">Dieser Abschnitt enthält Verfahren für Bereitstellungen, in denen ein Vermittlungsserver wie empfohlen auf jedem Front-End-Server oder Standard Edition-Server gemeinsam ausgeführt wird und auch für Bereitstellungen mit einem eigenständigen Vermittlungsserverpool.</span><span class="sxs-lookup"><span data-stu-id="65de7-120">This section includes procedures for deployments in which a Mediation Server is collocated on each Front End Server or Standard Edition server, as recommended, and also for deployments with a stand-alone Mediation Server pool.</span></span>

<span data-ttu-id="65de7-121">Sie können den folgenden Inhalt überspringen, wenn Sie mithilfe des Topologie-Generators eine Topologie definiert und veröffentlicht haben, die einen Vermittlungsserver auf jedem Front-End-Server oder Standard Edition-Server Kollokatoren, da der Bereitstellungs-Assistent die Dateien für den Vermittlungsserver bereits bei der Installation von Dateien für den Front-End-Serverpool oder Standard Edition-Server automatisch installiert hat:</span><span class="sxs-lookup"><span data-stu-id="65de7-121">You can skip the following content if you used Topology Builder to define and publish a topology that collocates a Mediation Server on each Front End Server or Standard Edition server, because Deployment Wizard already automatically installed the files for Mediation Server when you installed files for your Front End Server pool or Standard Edition server:</span></span>

  - [<span data-ttu-id="65de7-122">Konfigurieren von Trunks in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-122">Configuring trunks in Lync Server 2013</span></span>](lync-server-2013-configuring-trunks.md)

<span data-ttu-id="65de7-123">Wenn Sie den Topologie-Generator zum Definieren und Veröffentlichen eines Vermittlungsservers in einem eigenständigen Pool verwendet haben, können Sie den folgenden Inhalt verwenden:</span><span class="sxs-lookup"><span data-stu-id="65de7-123">If you used Topology Builder to define and publish a Mediation Server in a stand-alone pool, you can use the following content:</span></span>

  - <span data-ttu-id="65de7-124">Überprüfen Sie, ob Ihre Topologie die erforderlichen Software-und Umgebungsvoraussetzungen erfüllt, wie in [Enterprise-VoIP-Voraussetzungen für lync Server 2013](lync-server-2013-enterprise-voice-prerequisites.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="65de7-124">Verify that your topology meets the software and environment prerequisites, as described in [Enterprise Voice prerequisites for Lync Server 2013](lync-server-2013-enterprise-voice-prerequisites.md).</span></span>

</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="65de7-125">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="65de7-125">In This Section</span></span>

  - <span></span>  
    [<span data-ttu-id="65de7-126">Voraussetzungen für Enterprise-VoIP für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-126">Enterprise Voice prerequisites for Lync Server 2013</span></span>](lync-server-2013-enterprise-voice-prerequisites.md)

  - <span></span>  
    [<span data-ttu-id="65de7-127">Bereitstellen von Vermittlungsservern und Definieren von Peers in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-127">Deploying Mediation Servers and defining peers in Lync Server 2013</span></span>](lync-server-2013-deploying-mediation-servers-and-defining-peers.md)

  - <span></span>  
    [<span data-ttu-id="65de7-128">Konfigurieren von Trunks in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-128">Configuring trunks in Lync Server 2013</span></span>](lync-server-2013-configuring-trunks.md)

  - <span></span>  
    [<span data-ttu-id="65de7-129">Konfigurieren von Wählplänen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-129">Configuring dial plans in Lync Server 2013</span></span>](lync-server-2013-configuring-dial-plans.md)

  - <span></span>  
    [<span data-ttu-id="65de7-130">Konfigurieren von VoIP-Richtlinien, PSTN-Verwendungsdatensätzen und VoIP-Routen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-130">Configuring voice policies, PSTN usage records, and voice routes in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md)

  - <span></span>  
    [<span data-ttu-id="65de7-131">Exportieren und Importieren einer VoIP-Routingkonfiguration in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-131">Exporting and importing voice routing configuration in Lync Server 2013</span></span>](lync-server-2013-exporting-and-importing-voice-routing-configuration.md)

  - <span></span>  
    [<span data-ttu-id="65de7-132">Testen des VoIP-Routings in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-132">Test voice routing in Lync Server 2013</span></span>](lync-server-2013-test-voice-routing.md)

  - <span></span>  
    [<span data-ttu-id="65de7-133">Veröffentlichen ausstehender Änderungen an der VoIP-Routingkonfiguration in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-133">Publish pending changes to the voice routing configuration in Lync Server 2013</span></span>](lync-server-2013-publish-pending-changes-to-the-voice-routing-configuration.md)

  - <span></span>  
    [<span data-ttu-id="65de7-134">Bereitstellen lokaler Exchange Unified Messaging-Dienste zur Unterstützung von Lync Server 2013-Voicemail</span><span class="sxs-lookup"><span data-stu-id="65de7-134">Deploying on-premises Exchange UM to provide Lync Server 2013 voice mail</span></span>](lync-server-2013-deploying-on-premises-exchange-um-to-provide-lync-server-2013-voice-mail.md)

  - <span></span>  
    [<span data-ttu-id="65de7-135">Bereitstellen von Voicemail für Benutzer von Lync Server 2013 für gehostete Exchange Unified Messaging-Dienste</span><span class="sxs-lookup"><span data-stu-id="65de7-135">Providing Lync Server 2013 users voice mail on hosted Exchange UM</span></span>](lync-server-2013-providing-lync-server-users-voice-mail-on-hosted-exchange-um.md)

  - <span></span>  
    [<span data-ttu-id="65de7-136">Konfigurieren der lokalen lync Server 2013-Integration in Exchange Online</span><span class="sxs-lookup"><span data-stu-id="65de7-136">Configuring on-premises Lync Server 2013 integration with Exchange Online</span></span>](lync-server-2013-configuring-on-premises-lync-server-integration-with-exchange-online.md)

  - <span></span>  
    [<span data-ttu-id="65de7-137">Bereitstellen von erweiterten Enterprise-VoIP-Features in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-137">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-deploying-advanced-enterprise-voice-features.md)
    
      - [<span data-ttu-id="65de7-138">Informationen zu Netzwerkregionen, Standorten und Subnetzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-138">About network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-about-network-regions-sites-and-subnets.md)
    
      - [<span data-ttu-id="65de7-139">Erstellen oder Ändern eines Netzwerkbereichs in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-139">Create or modify a network region in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-region.md)
    
      - [<span data-ttu-id="65de7-140">Erstellen oder Ändern eines Netzwerkstandorts in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-140">Create or modify a network site in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-site.md)
    
      - [<span data-ttu-id="65de7-141">Zuordnen eines Subnetzes zu einem Netzwerkstandort in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-141">Associate a subnet with a network site in Lync Server 2013</span></span>](lync-server-2013-associate-a-subnet-with-a-network-site.md)
    
      - [<span data-ttu-id="65de7-142">Konfigurieren der Anrufsteuerung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-142">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)
    
      - [<span data-ttu-id="65de7-143">Konfigurieren von E9-1-1 in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-143">Configure Enhanced 9-1-1 in Lync Server 2013</span></span>](lync-server-2013-configure-enhanced-9-1-1.md)
    
      - [<span data-ttu-id="65de7-144">Konfigurieren der Medienumgehung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-144">Configure media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-media-bypass.md)

  - <span></span>  
    [<span data-ttu-id="65de7-145">Aktivieren von Benutzern für Enterprise-VoIP in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-145">Enable users for Enterprise Voice in Lync Server 2013</span></span>](lync-server-2013-enable-users-for-enterprise-voice.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="65de7-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="65de7-146">See Also</span></span>


[<span data-ttu-id="65de7-147">Bereitstellen von Zweigstellen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-147">Deploying branch sites in Lync Server 2013</span></span>](lync-server-2013-deploying-branch-sites.md)  
[<span data-ttu-id="65de7-148">Konfigurieren von Einwahlkonferenzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-148">Configuring dial-in conferencing in Lync Server 2013</span></span>](lync-server-2013-configuring-dial-in-conferencing.md)  
[<span data-ttu-id="65de7-149">Konfigurieren des Parkens von Anrufen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-149">Configuring Call Park in Lync Server 2013</span></span>](lync-server-2013-configuring-call-park.md)  
[<span data-ttu-id="65de7-150">Konfigurieren von Ansagen für nicht zugewiesene Nummern in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-150">Configuring announcements for unassigned numbers in Lync Server 2013</span></span>](lync-server-2013-configuring-announcements-for-unassigned-numbers.md)  
[<span data-ttu-id="65de7-151">Bereitstellen der Überwachung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65de7-151">Deploying monitoring in Lync Server 2013</span></span>](lync-server-2013-deploying-monitoring.md)  
  

<span data-ttu-id="65de7-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="65de7-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

