---
title: 'Lync Server 2013: Definieren eines Vermittlungsservers im Topologie-Generator'
description: 'Lync Server 2013: Definieren eines Vermittlungsservers im Topologie-Generator'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define a Mediation Server in Topology Builder
ms:assetid: 59d8f5ba-5064-4ea5-b4bf-2b9736e0fedd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398391(v=OCS.15)
ms:contentKeyID: 48184217
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2159b06c5587a17d24928febc11a883bc1520778
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431134"
---
# <a name="define-a-mediation-server-in-topology-builder-in-lync-server-2013"></a><span data-ttu-id="3ce92-103">Definieren eines Vermittlungsservers im Topologie-Generator in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3ce92-103">Define a Mediation Server in Topology Builder in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3ce92-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3ce92-104">

<span> </span></span></span>

<span data-ttu-id="3ce92-105">_**Letztes Änderungsdatum des Themas:** 2013-03-25_</span><span class="sxs-lookup"><span data-stu-id="3ce92-105">_**Topic Last Modified:** 2013-03-25_</span></span>

<span data-ttu-id="3ce92-106">Führen Sie die Schritte in diesem Thema aus, um mithilfe des Topologie-Generators einen eigenständigen Vermittlungs Server oder einen Pool mit einem Front-End-Pool an einer Website zu definieren, für die Sie Enterprise-VoIP zuvor nicht bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="3ce92-106">Follow the steps in this topic to use Topology Builder to define a stand-alone Mediation Server or a pool collocated with a Front End pool at a site for which you did not previously deploy Enterprise Voice.</span></span>

<span data-ttu-id="3ce92-107">Sie können eine Topologie mithilfe eines Kontos definieren, das Mitglied der Gruppe Administratoren ist.</span><span class="sxs-lookup"><span data-stu-id="3ce92-107">You can define a topology using an account that is a member of the Administrators group.</span></span>

<div>

## <a name="define-mediation-server-collocated-to-a-front-end-pool"></a><span data-ttu-id="3ce92-108">Definieren des Mediations Servers in einem Front-End-Pool</span><span class="sxs-lookup"><span data-stu-id="3ce92-108">Define Mediation Server collocated to a Front End pool</span></span>

<span data-ttu-id="3ce92-109">Führen Sie die Schritte in diesem Thema aus, um mithilfe des Topologie-Generators einen Vermittlungs Server zu definieren, der sich in einem Front-End-Pool an einer Website befindet, auf der Enterprise-VoIP nicht zuvor bereitgestellt wurde</span><span class="sxs-lookup"><span data-stu-id="3ce92-109">Follow the steps in this topic to use Topology Builder to define a Mediation Server collocated to a Front End pool in a site where Enterprise Voice has not been previously deployed.</span></span>

<div>

## <a name="to-add-a-mediation-server-to-a-front-end-pool"></a><span data-ttu-id="3ce92-110">So fügen Sie einen Vermittlungs Server zu einem Front-End-Pool hinzu</span><span class="sxs-lookup"><span data-stu-id="3ce92-110">To Add a Mediation Server to a Front End pool</span></span>

1.  <span data-ttu-id="3ce92-111">Starten Sie den Topologie-Generator: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server Topology Builder**.</span><span class="sxs-lookup"><span data-stu-id="3ce92-111">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="3ce92-112">Erweitern Sie im Topologie-Generator in der Konsolenstruktur den Namen der Website, für die Sie einen Front-End-Pool definieren möchten.</span><span class="sxs-lookup"><span data-stu-id="3ce92-112">In Topology Builder, in the console tree, expand the name of the site for which you want to define a Front End pool.</span></span>

3.  <span data-ttu-id="3ce92-113">Klicken Sie in der Konsolenstruktur mit der rechten Maustaste auf den Typ des gewünschten Front-End-Pools, und klicken Sie dann auf **neuer Front-End-Pool.**..</span><span class="sxs-lookup"><span data-stu-id="3ce92-113">In the console tree, right-click the type of Front End pool you want, and then click **New Front End pool..**.</span></span>

4.  <span data-ttu-id="3ce92-114">Navigieren Sie durch den Assistenten **Neuen Front-End-Pool definieren**, bis Sie die Seite **Verbundene Serverrollen auswählen** erreichen.</span><span class="sxs-lookup"><span data-stu-id="3ce92-114">Navigate through the **Define New Front End Pool** wizard until you reach the **Select collocated server roles** page.</span></span>

5.  <span data-ttu-id="3ce92-115">Aktivieren Sie unter **ausgewählte Serverrollen auswählen** die Option **Collocate-Vermittlungsserver**.</span><span class="sxs-lookup"><span data-stu-id="3ce92-115">In **Select collocated server roles**, check the option **Collocate Mediation Server**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="3ce92-116">Wenn der Typ des ausgewählten Front-End-Pools die Enterprise-Edition ist, wird die Mediation Server-Komponente auf allen Front-End-Servern dieses Front-End-Pools installiert.</span><span class="sxs-lookup"><span data-stu-id="3ce92-116">If the type of Front End pool you selected is the Enterprise Edition, then the Mediation Server component will be installed on all the Front End Servers of that Front End pool.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="3ce92-117">Der vom Vermittlungsserver verwendete <STRONG>Next Hop-Pool</STRONG> ist der Front-End-Pool, in dem sich der Vermittlungsserver befindet.</span><span class="sxs-lookup"><span data-stu-id="3ce92-117">The <STRONG>Next hop pool</STRONG> used by the Mediation Server will be the Front End pool where the Mediation Server is collocated on.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="3ce92-118">Der vom Vermittlungsserver verwendete <STRONG>Edge-Pool</STRONG> ist derselbe Edge-Pool, der dem Front-End-Pool zugeordnet ist, in dem sich der Vermittlungsserver befindet.</span><span class="sxs-lookup"><span data-stu-id="3ce92-118">The <STRONG>Edge pool</STRONG> used by the Mediation Server will be the same Edge pool associated with the Front End pool where the Mediation Server is collocated on.</span></span></P></LI></UL>

    
    </div>

6.  <span data-ttu-id="3ce92-119">Klicken Sie auf **Standard festlegen** , um diesen Front-End-Pool zum Weiterleiten von Anrufen von Microsoft Office Communications Server 2007 R2 an das PSTN zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ce92-119">Click **Make Default** to use this Front End pool to route calls from Microsoft Office Communications Server 2007 R2 to the PSTN.</span></span>

7.  <span data-ttu-id="3ce92-120">Klicken Sie auf **Fertig stellen** , wenn Sie mit dem Verknüpfen eines oder mehrerer Peers mit dem Front-End-Pool fertig sind.</span><span class="sxs-lookup"><span data-stu-id="3ce92-120">Click **Finish** when you are finished associating one or more peers to the Front End pool.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3ce92-121">Bevor Sie mit dem nächsten Schritt des Enterprise-VoIP-Bereitstellungsprozesses fortfahren, stellen Sie sicher, dass der vermittlungsserverpool (also der Front-End-Pool mit der Mediationsserver Komponente) die von Ihnen angegebenen FQDNs verwendet.</span><span class="sxs-lookup"><span data-stu-id="3ce92-121">Before you proceed to the next step in the Enterprise Voice deployment process, make sure that the Mediation Server pool (i.e. Front End pool with the Mediation Server component collocated) is using the FQDNs that you specified.</span></span>

    
    </div>

8.  <span data-ttu-id="3ce92-122">Führen Sie als nächstes die Verfahren unter [Veröffentlichen der Topologie in lync Server 2013](lync-server-2013-publish-the-topology.md) im Bereitstellungshandbuch aus, um den Vermittlungsserver Ihrer Topologie hinzuzufügen, bevor Sie mit dem nächsten Schritt zum Ändern der Abhör Anschlüsse des Vermittlungsservers bei Bedarf fortfahren.</span><span class="sxs-lookup"><span data-stu-id="3ce92-122">Next, follow the procedures in [Publish the topology in Lync Server 2013](lync-server-2013-publish-the-topology.md) in the Deployment Guide documentation to add the Mediation Server to your topology before proceeding to the next step of modifying the listening ports of the Mediation Server if needed.</span></span> <span data-ttu-id="3ce92-123">Sie müssen Ihre Topologie jedes Mal veröffentlichen, wenn Sie den Topologie-Generator verwenden, um Ihre Topologie zu definieren oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3ce92-123">You must publish your topology each time you use Topology Builder to define or modify your topology.</span></span>

</div>

</div>

<div>

## <a name="define-stand-alone-mediation-server"></a><span data-ttu-id="3ce92-124">Eigenständigen Vermittlungs Server definieren</span><span class="sxs-lookup"><span data-stu-id="3ce92-124">Define stand-alone Mediation Server</span></span>

<span data-ttu-id="3ce92-125">Führen Sie die Schritte in diesem Thema aus, um mithilfe des Topologie-Generators einen eigenständigen Vermittlungs Server oder Pool an einer Website zu definieren, auf der Enterprise-VoIP nicht zuvor bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="3ce92-125">Follow the steps in this topic to use Topology Builder to define a stand-alone Mediation Server or pool at a site where Enterprise Voice has not been previously deployed.</span></span>

<span data-ttu-id="3ce92-126">Wenn Sie bereits Vermittlungsserver an Front-End-Pools auf dieser Website bereitgestellt haben, können Sie diesen Abschnitt überspringen und [die Dateien für den Vermittlungsserver in lync Server 2013 installieren](lync-server-2013-install-the-files-for-mediation-server.md) , bevor Sie mit der [Konfiguration von Trunks in lync Server 2013](lync-server-2013-configuring-trunks.md)fortfahren.</span><span class="sxs-lookup"><span data-stu-id="3ce92-126">If you already deployed Mediation Servers collocated to Front End pools at this site, you can skip this section and [Install the files for Mediation Server in Lync Server 2013](lync-server-2013-install-the-files-for-mediation-server.md) before proceeding to [Configuring trunks in Lync Server 2013](lync-server-2013-configuring-trunks.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3ce92-127">In diesem Abschnitt wird davon ausgegangen, dass Sie bereits mindestens einen Front-End-Pool eingerichtet haben, wie unter <A href="lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md">definieren und Konfigurieren eines Front-End-Pools oder Standard Edition-Servers in lync Server 2013</A> und <A href="lync-server-2013-publish-the-topology.md">Veröffentlichen der Topologie in lync Server 2013</A> in der Bereitstellungshandbuch-Dokumentation beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="3ce92-127">This section assumes that you have already setup at least one Front End pool, as described in <A href="lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md">Define and configure a Front End pool or Standard Edition server in Lync Server 2013</A> and <A href="lync-server-2013-publish-the-topology.md">Publish the topology in Lync Server 2013</A> in the Deployment Guide documentation.</span></span>



</div>

<div>

## <a name="to-add-a-mediation-server"></a><span data-ttu-id="3ce92-128">So fügen Sie einen Vermittlungs Server hinzu</span><span class="sxs-lookup"><span data-stu-id="3ce92-128">To Add a Mediation Server</span></span>

1.  <span data-ttu-id="3ce92-129">Starten Sie den Topologie-Generator: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server Topology Builder**.</span><span class="sxs-lookup"><span data-stu-id="3ce92-129">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="3ce92-130">Erweitern Sie im Topologie-Generator in der Konsolenstruktur den Namen der Website, für die Sie einen Vermittlungs Server definieren möchten.</span><span class="sxs-lookup"><span data-stu-id="3ce92-130">In Topology Builder, in the console tree, expand the name of the site for which you want to define a Mediation Server.</span></span>

3.  <span data-ttu-id="3ce92-131">Klicken Sie in der Konsolenstruktur mit der rechten Maustaste auf den Knoten **Mediations Pools** , und klicken Sie dann auf **Vermittlungs Server Pool**.</span><span class="sxs-lookup"><span data-stu-id="3ce92-131">In the console tree, right-click the **Mediation pools** node, and then click **Mediation Server pool**.</span></span>

4.  <span data-ttu-id="3ce92-132">Geben Sie unter **neuen Mediations Pool definieren** den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Mediation Server Pools ein.</span><span class="sxs-lookup"><span data-stu-id="3ce92-132">In **Define New Mediation Pool**, type the Mediation Server pool fully qualified domain name (FQDN).</span></span>

5.  <span data-ttu-id="3ce92-133">Führen Sie anschließend eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="3ce92-133">Next, do one of the following:</span></span>
    
      - <span data-ttu-id="3ce92-134">Wenn Sie mehrere Vermittlungsserver im Pool bereitstellen möchten, um eine höhere Verfügbarkeit zu gewährleisten, wählen Sie den **Pool für mehrere Computer** aus.</span><span class="sxs-lookup"><span data-stu-id="3ce92-134">If you want to deploy multiple Mediation Servers in the pool to provide high availability, then select **Multiple computer pool**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="3ce92-135">Sie müssen den DNS-Lastenausgleich bereitstellen, um Vermittlungsserver Pools mit mehreren Vermittlungsservern zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="3ce92-135">You must deploy DNS load balancing to support Mediation Server pools that have multiple Mediation Servers.</span></span> <span data-ttu-id="3ce92-136">Ausführliche Informationen finden Sie im Abschnitt Verwenden des DNS-Lastenausgleichs für Mediationsserver Pools des <A href="lync-server-2013-dns-load-balancing.md">DNS-Lastenausgleichs in lync Server 2013</A> in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="3ce92-136">For details, see the Using DNS Load Balancing on Mediation Server Pools section of <A href="lync-server-2013-dns-load-balancing.md">DNS load balancing in Lync Server 2013</A> in the Planning documentation.</span></span>

        
        </div>
    
      - <span data-ttu-id="3ce92-137">Wenn Sie nur einen Vermittlungs Server im Pool bereitstellen möchten, weil Sie keine höhere Verfügbarkeit benötigen, wählen Sie den **Pool für einzelne Computer** aus.</span><span class="sxs-lookup"><span data-stu-id="3ce92-137">If you want to deploy only one Mediation Server in the pool because you do not require high availability, then select **Single computer pool**.</span></span> <span data-ttu-id="3ce92-138">Überspringen Sie den folgenden Schritt.</span><span class="sxs-lookup"><span data-stu-id="3ce92-138">Skip the following step.</span></span>

6.  <span data-ttu-id="3ce92-139">Wenn Sie im vorherigen Schritt **Pool mit mehreren Computern** ausgewählt haben, klicken Sie in **Computer in diesem Pool definieren** auf **Computer-FQDN**, geben Sie die FQDNs der einzelnen Server innerhalb des Pools ein und klicken Sie anschließend auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="3ce92-139">If you selected **Multiple computer pool** in the previous step, on the **Define the computers in this pool** item, click **Computer FQDN**, type the FQDN of each server in the pool, and then click **Add**.</span></span> <span data-ttu-id="3ce92-140">Wiederholen Sie diesen Schritt für alle anderen Vermittlungsserver, die Sie dem Pool hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="3ce92-140">Repeat this step for all other Mediation Servers that you want to add to the pool.</span></span> <span data-ttu-id="3ce92-141">Nachdem Sie alle Computer im Pool definiert haben, klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="3ce92-141">When you have defined all the computers in the pool, click **Next**.</span></span>

7.  <span data-ttu-id="3ce92-142">Klicken Sie auf der Seite **Nächster Hop auswählen** auf **Nächster Hop-Pool**, klicken Sie auf den FQDN des Front-End-Pools, in dem dieser Vermittlungs Server Pool verwendet wird, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3ce92-142">On the **Select the next hop** page, click **Next hop pool**, click the FQDN of the Front End pool that will use this Mediation Server pool, and then click **Next**.</span></span>

8.  <span data-ttu-id="3ce92-143">Führen Sie auf der Seite **Edgeserver auswählen** einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="3ce92-143">On the **Select an Edge Server** page, do one of the following:</span></span>
    
      - <span data-ttu-id="3ce92-144">Wenn Sie die PSTN-Konnektivität für externe Benutzer bereitstellen möchten, die für Enterprise-VoIP aktiviert sind, klicken Sie unter Wählen Sie den **von diesem Vermittlungsserver verwendeten Edge-Pool** aus auf den FQDN des Edgeserver-Pools, der diesen vermittlungsserverpool verwendet, um PSTN-Konnektivität für diese externen Benutzer bereitzustellen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3ce92-144">If you want to provide PSTN connectivity to external users enabled for Enterprise Voice, under **Select Edge Pool used by this Mediation Server**, click the FQDN of the Edge Server pool that will use this Mediation Server pool to provide PSTN connectivity to those external users, and then click **Next**.</span></span>
    
      - <span data-ttu-id="3ce92-145">Wenn Sie nicht beabsichtigen, externe Benutzer für Enterprise-VoIP zu aktivieren, oder wenn Sie keine PSTN-Konnektivität für Benutzer bereitstellen möchten, wenn diese sich außerhalb des internen Netzwerks befinden, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="3ce92-145">If you do not plan to enable external users for Enterprise Voice, or if you do not want to provide PSTN connectivity to users when they are outside the internal network, click **Next**.</span></span>

9.  <span data-ttu-id="3ce92-146">Führen Sie als nächstes die Verfahren unter [Veröffentlichen der Topologie in lync Server 2013](lync-server-2013-publish-the-topology.md) in der Bereitstellungsdokumentation aus, um den Vermittlungs Server zur Topologie hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="3ce92-146">Next, follow the procedures in [Publish the topology in Lync Server 2013](lync-server-2013-publish-the-topology.md) in the Deployment documentation to add the Mediation Server to the topology.</span></span> <span data-ttu-id="3ce92-147">Sie müssen Ihre Topologie jedes Mal veröffentlichen, wenn Sie den Topologie-Generator verwenden, um Ihre Topologie zu erstellen oder zu ändern, damit die Daten zum Installieren der Dateien für Server verwendet werden können, auf denen lync Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3ce92-147">You must publish your topology each time you use Topology Builder to build or modify your topology so that the data can be used to install the files for servers that are running Lync Server.</span></span> <span data-ttu-id="3ce92-148">Fahren Sie dann mit den nächsten Schritten fort, um die Abhör Anschlüsse auf dem Vermittlungs Server bei Bedarf zu ändern.</span><span class="sxs-lookup"><span data-stu-id="3ce92-148">Then continue to the next steps to modify the listening ports on the Mediation Server, if necessary.</span></span>

</div>

</div>

<div>

## <a name="define-the-mediation-server-listening-ports"></a><span data-ttu-id="3ce92-149">Definieren der Abhör Anschlüsse des Vermittlungsservers</span><span class="sxs-lookup"><span data-stu-id="3ce92-149">Define the Mediation Server Listening Ports</span></span>

<span data-ttu-id="3ce92-150">Führen Sie die Schritte in diesem Thema aus, um mithilfe des Topologie-Generators die Abhör Anschlüsse zu definieren, die von einem Vermittlungs Server oder-Pool eingehende Verbindungen von einem Gateway-Peer akzeptiert werden.</span><span class="sxs-lookup"><span data-stu-id="3ce92-150">Follow the steps in this topic to use Topology Builder to define the listening ports a Mediation Server or pool will accept incoming connections from a gateway peer.</span></span>

<div>

## <a name="to-modify-the-mediation-server-listening-ports"></a><span data-ttu-id="3ce92-151">So ändern Sie die Abhör Anschlüsse des Vermittlungsservers</span><span class="sxs-lookup"><span data-stu-id="3ce92-151">To Modify the Mediation Server Listening Ports</span></span>

1.  <span data-ttu-id="3ce92-152">Starten Sie den Topologie-Generator: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server Topology Builder**.</span><span class="sxs-lookup"><span data-stu-id="3ce92-152">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="3ce92-153">Erweitern Sie im Topologie-Generator in der Konsolenstruktur den Knoten **Mediations Pools** , und klicken Sie mit der rechten Maustaste auf den zuvor erstellten Mediations Server.</span><span class="sxs-lookup"><span data-stu-id="3ce92-153">In Topology Builder, in the console tree, expand the **Mediation pools** node, and right-click the Mediation Server previously created.</span></span>

3.  <span data-ttu-id="3ce92-154">Standardmäßig sind die SIP-Abhör Anschlüsse auf dem Vermittlungsserver 5070 für den TLS-Datenverkehr von lync Server, 5067 für TLS-Datenverkehr von Peers (Gateways, TK oder SBCS).</span><span class="sxs-lookup"><span data-stu-id="3ce92-154">By default, the SIP listening ports on the Mediation Server are 5070 for TLS traffic from Lync Server, 5067 for TLS traffic from peers (gateways, PBXes, or SBCs).</span></span> <span data-ttu-id="3ce92-155">Der TCP-Port ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="3ce92-155">TCP port is disabled by default.</span></span> <span data-ttu-id="3ce92-156">Wenn Sie über Gateways verfügen, die TLS nicht unterstützen, müssen Sie den TCP-Port aktivieren.</span><span class="sxs-lookup"><span data-stu-id="3ce92-156">You must enable TCP port if you have gateways that do not support TLS.</span></span>

4.  <span data-ttu-id="3ce92-157">Geben Sie den gewünschten TLS-oder TCP-Überwachungs Portbereich an der Vermittlungs Server akzeptiert eingehende Verbindungen von PSTN-Gateways.</span><span class="sxs-lookup"><span data-stu-id="3ce92-157">Specify the desired TLS or TCP listening port range the Mediation Server will accept incoming connections from PSTN gateways.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="3ce92-158">Wenn die Option <STRONG>TCP-Port aktivieren</STRONG> nicht ausgewählt wird, ist die Eingabe des TCP-Portbereichs nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="3ce92-158">Entering a TCP port range is not required if <STRONG>Enable TCP port</STRONG> is not checked.</span></span> <span data-ttu-id="3ce92-159">Diese Einstellung ist optional.</span><span class="sxs-lookup"><span data-stu-id="3ce92-159">This setting is optional.</span></span>

    
    </div>

<span data-ttu-id="3ce92-160">Definieren Sie als nächstes [ein Gateway im Topologie-Generator in lync Server 2013](lync-server-2013-define-a-gateway-in-topology-builder.md) , und installieren Sie die Dateien auf jedem Vermittlungsserver im Pool, indem Sie die Verfahren unter [Installieren der Dateien für Mediation Server in lync Server 2013](lync-server-2013-install-the-files-for-mediation-server.md)befolgen.</span><span class="sxs-lookup"><span data-stu-id="3ce92-160">Next, [Define a gateway in Topology Builder in Lync Server 2013](lync-server-2013-define-a-gateway-in-topology-builder.md) and install the files on each Mediation Server in the pool by following the procedures in [Install the files for Mediation Server in Lync Server 2013](lync-server-2013-install-the-files-for-mediation-server.md).</span></span>

<span data-ttu-id="3ce92-161"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3ce92-161"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

