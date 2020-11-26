---
title: 'Lync Server 2013: Definieren eines Gateways im Topologie-Generator'
description: 'Lync Server 2013: Definieren eines Gateways im Topologie-Generator'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define a gateway in Topology Builder
ms:assetid: 456e5a96-d9f6-42a6-862c-a69464391628
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425945(v=OCS.15)
ms:contentKeyID: 48184036
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1f8bf09f06f54d8988c8c9a9e385ef251a960bd6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431185"
---
# <a name="define-a-gateway-in-topology-builder-in-lync-server-2013"></a><span data-ttu-id="7b4f6-103">Definieren eines Gateways im Topologie-Generator in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7b4f6-103">Define a gateway in Topology Builder in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7b4f6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7b4f6-104">

<span> </span></span></span>

<span data-ttu-id="7b4f6-105">_**Letztes Änderungsdatum des Themas:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="7b4f6-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="7b4f6-106">Führen Sie die folgenden Schritte aus, um mithilfe des Topologie-Generators einen *Peer* zu definieren, dem Sie einen Vermittlungs Server zuordnen können, um Verbindungen mit dem öffentlichen Telefonnetz (PSTN) für Benutzer bereitzustellen, die für Enterprise-VoIP aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-106">Follow these steps to use Topology Builder to define a *peer* with which you can associate a Mediation Server to provide connectivity to the public switched telephone network (PSTN) for users enabled for Enterprise Voice.</span></span> <span data-ttu-id="7b4f6-107">Ein Peer-to-Mediation-Server kann ein PSTN-Gateway, eine IP-Telefonanlage oder ein Session Border Controller (SBC) für einen Internet-Telefoniedienstanbieter (ITSP) sein, mit dem Sie eine Verbindung herstellen, indem Sie einen SIP-Trunk konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-107">A peer to the Mediation Server can be a PSTN gateway, an IP-PBX, or a Session Border Controller (SBC) for an Internet Telephony Service Provider (ITSP) to which you connect by configuring a SIP trunk.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="7b4f6-108">In diesem Thema wird davon ausgegangen, dass Sie mindestens einen internen Front-End-Pool oder Standard Edition-Server an mindestens einem zentralen Standort mit einem zusammengefassten oder eigenständigen Vermittlungsserver eingerichtet haben, wie unter <A href="lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md">definieren und Konfigurieren eines Front-End-Pools oder Standard Edition-Servers in lync Server 2013</A> beschrieben und <A href="lync-server-2013-publish-the-topology.md">Veröffentlichen der Topologie in lync Server 2013</A> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-108">This topic assumes that you have set up at least one internal Front End pool or Standard Edition server in at least one central site with a collocated or stand-alone Mediation Server, as described in <A href="lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md">Define and configure a Front End pool or Standard Edition server in Lync Server 2013</A> and <A href="lync-server-2013-publish-the-topology.md">Publish the topology in Lync Server 2013</A> in the Deployment documentation.</span></span> <span data-ttu-id="7b4f6-109">In diesem Thema wird auch davon ausgegangen, dass Sie überprüft haben, dass Ihre Infrastruktur die Voraussetzungen erfüllt, die unter <A href="lync-server-2013-software-prerequisites-for-enterprise-voice.md">Software Voraussetzungen für Enterprise-VoIP in lync Server 2013</A> und <A href="lync-server-2013-security-and-configuration-prerequisites-for-enterprise-voice.md">Sicherheits-und Konfigurationsvoraussetzungen für Enterprise-VoIP in lync Server 2013</A>beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-109">This topic also assumes that you have verified that your infrastructure meets the prerequisites described in <A href="lync-server-2013-software-prerequisites-for-enterprise-voice.md">Software prerequisites for Enterprise Voice in Lync Server 2013</A> and <A href="lync-server-2013-security-and-configuration-prerequisites-for-enterprise-voice.md">Security and configuration prerequisites for Enterprise Voice in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-define-a-peer-for-the-mediation-server"></a><span data-ttu-id="7b4f6-110">So definieren Sie einen Peer für den Vermittlungs Server</span><span class="sxs-lookup"><span data-stu-id="7b4f6-110">To Define a Peer for the Mediation Server</span></span>

1.  <span data-ttu-id="7b4f6-111">Starten Sie den Topologie-Generator: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server Topology Builder**.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-111">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="7b4f6-112">Klicken Sie unter lync Server 2013, ihren Websitenamen, freigegebene Komponenten, mit der rechten Maustaste auf den Knoten **PSTN-Gateways** , und klicken Sie dann auf **Neues PSTN-Gateway**.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-112">Under Lync Server 2013, your site name, Shared Components, right-click the **PSTN Gateways** node, and then click **New PSTN Gateway**.</span></span>
    
    <span data-ttu-id="7b4f6-113">![d898c3c1-8798-4b74-8f02-b994ef3db4c1](images/Gg425945.d898c3c1-8798-4b74-8f02-b994ef3db4c1(OCS.15).png "d898c3c1-8798-4b74-8f02-b994ef3db4c1")</span><span class="sxs-lookup"><span data-stu-id="7b4f6-113">![d898c3c1-8798-4b74-8f02-b994ef3db4c1](images/Gg425945.d898c3c1-8798-4b74-8f02-b994ef3db4c1(OCS.15).png "d898c3c1-8798-4b74-8f02-b994ef3db4c1")</span></span>

3.  <span data-ttu-id="7b4f6-114">Geben Sie unter **Neues IP/PSTN-Gateway definieren** den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) oder die IP-Adresse des Peers ein und klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-114">In **Define New IP/PSTN Gateway**, type the fully qualified domain name (FQDN) or IP address of the peer, and click **Next**.</span></span>
    
    <span data-ttu-id="7b4f6-115">![8017ba5e-41bc-48d4-97d9-fd306cd322b8](images/Gg425945.8017ba5e-41bc-48d4-97d9-fd306cd322b8(OCS.15).png "8017ba5e-41bc-48d4-97d9-fd306cd322b8")</span><span class="sxs-lookup"><span data-stu-id="7b4f6-115">![8017ba5e-41bc-48d4-97d9-fd306cd322b8](images/Gg425945.8017ba5e-41bc-48d4-97d9-fd306cd322b8(OCS.15).png "8017ba5e-41bc-48d4-97d9-fd306cd322b8")</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7b4f6-116">Wenn Sie TLS (Transport Layer Security) als Transporttyp angeben, müssen Sie anstelle der IP-Adresse des Peers des Vermittlungsservers den FQDN angeben.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-116">If you specify Transport Layer Security (TLS) as the transport type, you must specify the FQDN instead of the IP address of the peer of the Mediation Server.</span></span>

    
    </div>

4.  <span data-ttu-id="7b4f6-117">Definieren Sie den Überwachungsmodus (IPv4 oder IPv6) für die IP-Adresse Ihres neuen PSTN-Gateways und klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-117">Define the listening mode (IPv4 or IPv6) of the IP address of your new PSTN gateway, and click **Next**.</span></span>
    
    <span data-ttu-id="7b4f6-118">![c7fc0d12-adc8-45a7-aca1-b376e1d2fcec](images/Gg425945.c7fc0d12-adc8-45a7-aca1-b376e1d2fcec(OCS.15).png "c7fc0d12-adc8-45a7-aca1-b376e1d2fcec")</span><span class="sxs-lookup"><span data-stu-id="7b4f6-118">![c7fc0d12-adc8-45a7-aca1-b376e1d2fcec](images/Gg425945.c7fc0d12-adc8-45a7-aca1-b376e1d2fcec(OCS.15).png "c7fc0d12-adc8-45a7-aca1-b376e1d2fcec")</span></span>

5.  <span data-ttu-id="7b4f6-119">Definieren Sie einen *Stammtrunk* für das PSTN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-119">Define a *root trunk* for the PSTN gateway.</span></span> <span data-ttu-id="7b4f6-120">Ein trunk ist eine logische Verbindung zwischen einem Vermittlungs Server und einem vom Tupel eindeutig identifizierten Gateway.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-120">A trunk is a logical connection between a Mediation Server and a gateway uniquely identified by the tuple.</span></span>
    
    <span data-ttu-id="7b4f6-121">{Vermittlungsserver-FQDN, Abhör Port für Mediationsserver (TLS oder TCP): Gateway-IP und-FQDN, Gateway-Überwachungs Port}</span><span class="sxs-lookup"><span data-stu-id="7b4f6-121">{Mediation Server FQDN, Mediation Server listening port (TLS or TCP) : gateway IP and FQDN, gateway listening port}</span></span>
    
      - <span data-ttu-id="7b4f6-122">Wenn Sie ein PSTN-Gateway im Topologie-Generator definieren, müssen Sie einen Stamm Stamm definieren, um das PSTN-Gateway erfolgreich zu Ihrer Topologie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-122">When defining a PSTN gateway in Topology Builder, you must define a root trunk to successfully add the PSTN gateway to your topology.</span></span>
    
      - <span data-ttu-id="7b4f6-123">Der Stammtrunk kann erst entfernt werden, nachdem das damit verbundene PSTN-Gateway entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-123">The root trunk cannot be removed until the associated PSTN gateway is removed.</span></span>
    
    <span data-ttu-id="7b4f6-124">![3b030757-eb35-4616-bb6b-74ee67507e3d](images/Gg425945.3b030757-eb35-4616-bb6b-74ee67507e3d(OCS.15).png "3b030757-eb35-4616-bb6b-74ee67507e3d")</span><span class="sxs-lookup"><span data-stu-id="7b4f6-124">![3b030757-eb35-4616-bb6b-74ee67507e3d](images/Gg425945.3b030757-eb35-4616-bb6b-74ee67507e3d(OCS.15).png "3b030757-eb35-4616-bb6b-74ee67507e3d")</span></span>

6.  <span data-ttu-id="7b4f6-125">Geben Sie unter **Abhör Port für IP/PSTN-Gateway** den Abhöranschluss ein, den das Gateway, die Telefonanlage oder SBC für SIP-Nachrichten vom Vermittlungs Server verwenden, die dem Stammverzeichnis des PSTN-Gateways zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-125">Under **Listening Port for IP/PSTN Gateway**, type the listening port that the gateway, PBX, or SBC will use for SIP messages from the Mediation Server that will be associated with the root trunk of the PSTN gateway.</span></span> <span data-ttu-id="7b4f6-126">(In der Standardeinstellung ist für ein PSTN-Gateway, eine Nebenstellenanlage oder einen SBC Port 5066 für TCP (Transmission Control Protocol) und Port 5067 für TLS (Transport Layer Security) festgelegt.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-126">(By default, the ports are 5066 for Transmission Control Protocol (TCP) and 5067 for Transport Layer Security (TLS) on a PSTN gateway, PBX or SBC.</span></span> <span data-ttu-id="7b4f6-127">Bei einer Survivable Branch-Appliance an einer Zweigstelle sind die Standardanschlüsse 5081 für TCP und 5082 für TLS.)</span><span class="sxs-lookup"><span data-stu-id="7b4f6-127">On a Survivable Branch Appliance at a branch site, the default ports are 5081 for TCP and 5082 for TLS.)</span></span>

7.  <span data-ttu-id="7b4f6-128">Klicken Sie unter **SIP-Transportprotokoll** auf das für den Peer zu verwendende Transportprotokoll und dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-128">Under **SIP Transport Protocol**, click the transport type that the peer uses, and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7b4f6-129">Aus Sicherheitsgründen empfehlen wir dringend, einen Peer auf dem Vermittlungs Server bereitzustellen, der TLS verwenden kann.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-129">For security reasons, we strongly recommend that you deploy a peer to the Mediation Server that can use TLS.</span></span>

    
    </div>

8.  <span data-ttu-id="7b4f6-130">Wählen Sie unter **zugeordneter Vermittlungsserver** den vermittlungsserverpool aus, der dem Stamm Stamm dieses PSTN-Gateways zugeordnet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-130">Under **Associated Mediation Server**, select the Mediation Server pool to associate with the root trunk of this PSTN Gateway.</span></span>

9.  <span data-ttu-id="7b4f6-131">Geben Sie unter **zugeordneter Vermittlungsserver-Port** den Abhör Port ein, der vom Vermittlungsserver für SIP-Nachrichten vom Gateway verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-131">Under **Associated Mediation Server port**, type the listening port that the Mediation Server will use for SIP messages from the gateway.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7b4f6-132">Mit mehreren trunk-Unterstützung in lync Server 2013 können mehrere SIP-Signalisierungs Anschlüsse auf dem Vermittlungsserver definiert werden, um für die Kommunikation mit mehreren PSTN-Gateways verwendet zu werden.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-132">With multiple trunk support in Lync Server 2013, multiple SIP signaling ports can be defined on the Mediation Server to be used for communication with multiple PSTN gateways.</span></span> <span data-ttu-id="7b4f6-133">Wenn Sie einen trunk definieren, muss sich der <STRONG>zugeordnete Vermittlungsserver-Port</STRONG> innerhalb des Bereichs der Abhör Anschlüsse für das jeweilige vom Vermittlungsserver zugelassene Protokoll befinden.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-133">When defining a trunk, the <STRONG>Associated Mediation Server port</STRONG> must be within the range of the listening ports for the respective protocol allowed by the Mediation Server.</span></span> <span data-ttu-id="7b4f6-134">Dieser Portbereich wird unter lync Server 2013 und Mediations Pools definiert.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-134">This port range is defined under Lync Server 2013 and Mediation Pools.</span></span> <span data-ttu-id="7b4f6-135">Klicken Sie mit der rechten Maustaste auf den Interessenbereich des Mediation Server-Pools, und wählen Sie <STRONG>Eigenschaften bearbeiten</STRONG>aus.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-135">Right-click the Mediation Server pool of interest, and select <STRONG>Edit Properties</STRONG>.</span></span> <span data-ttu-id="7b4f6-136">Geben Sie den Portbereich im Feld <STRONG>Abhör-Ports</STRONG> an.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-136">Specify the port range in the <STRONG>Listening ports</STRONG> field.</span></span>

    
    </div>

10. <span data-ttu-id="7b4f6-137">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-137">Click **Finish**.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="7b4f6-138">Bevor Sie diesen Schritt abgeschlossen haben, müssen Sie sicherstellen, dass der von Ihnen definierte Peer ausgeführt wird und den von Ihnen angegebenen FQDN oder die IP-Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-138">Before you finish this step, be sure that the peer that you defined is running and using the FQDN or IP address that you specified.</span></span>



</div>

<span data-ttu-id="7b4f6-139">Führen Sie als nächstes zum Hinzufügen des Peers zur Topologie die Verfahren unter [Veröffentlichen der Topologie in lync Server 2013](lync-server-2013-publish-the-topology.md) in der Bereitstellungsdokumentation aus.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-139">Next, to add the peer to the topology, follow the procedures in [Publish the topology in Lync Server 2013](lync-server-2013-publish-the-topology.md) in the Deployment documentation.</span></span> <span data-ttu-id="7b4f6-140">Sie müssen Ihre Topologie jedes Mal veröffentlichen, wenn Sie den Topologie-Generator verwenden, um Ihre Topologie zu erstellen oder zu ändern, damit die Daten zum Installieren der Dateien für Server verwendet werden können, auf denen lync Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b4f6-140">You must publish your topology each time that you use Topology Builder to build or modify your topology, so that the data can be used to install the files for servers that are running Lync Server.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="7b4f6-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b4f6-141">See Also</span></span>


[<span data-ttu-id="7b4f6-142">Ändern eines Trunks im Topologie-Generator in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7b4f6-142">Modify a trunk in Topology Builder in Lync Server 2013</span></span>](lync-server-2013-modify-a-trunk-in-topology-builder.md)  
  

<span data-ttu-id="7b4f6-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7b4f6-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

