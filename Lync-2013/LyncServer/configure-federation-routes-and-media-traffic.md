---
title: Konfigurieren von Partnerverbundrouten und Mediendatenverkehr
description: Konfigurieren von Verbund Routen und Mediendatenverkehr
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Configure federation routes and media traffic
ms:assetid: 8b2f5f81-a955-4ad1-ad74-397322ff9521
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688121(v=OCS.15)
ms:contentKeyID: 49733720
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: de26f472bddc504ff79e427b5243587f27020c3d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394115"
---
# <a name="configure-federation-routes-and-media-traffic"></a><span data-ttu-id="0efb2-103">Konfigurieren von Partnerverbundrouten und Mediendatenverkehr</span><span class="sxs-lookup"><span data-stu-id="0efb2-103">Configure federation routes and media traffic</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0efb2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0efb2-104">

<span> </span></span></span>

<span data-ttu-id="0efb2-105">_**Letztes Änderungsdatum des Themas:** 2012-10-15_</span><span class="sxs-lookup"><span data-stu-id="0efb2-105">_**Topic Last Modified:** 2012-10-15_</span></span>

<span data-ttu-id="0efb2-106">Föderation ist eine Vertrauensstellung zwischen zwei oder mehr SIP-Domänen, die es Benutzern in separaten Organisationen ermöglicht, über Netzwerkgrenzen hinweg zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="0efb2-106">Federation is a trust relationship between two or more SIP domains that permits users in separate organizations to communicate across network boundaries.</span></span> <span data-ttu-id="0efb2-107">Nachdem Sie die Migration zu Ihrem lync Server 2013-Pilot Pool durchgeführt haben, müssen Sie von der Verbund Route ihrer lync Server 2010-Edgeserver zur Föderations Route ihrer lync Server 2013-Edgeserver wechseln.</span><span class="sxs-lookup"><span data-stu-id="0efb2-107">After you migrate to your Lync Server 2013 pilot pool, you need to transition from the federation route of your Lync Server 2010 Edge Servers to the federation route of your Lync Server 2013 Edge Servers.</span></span>

<span data-ttu-id="0efb2-108">Führen Sie die folgenden Verfahren aus, um die Föderations Route und die Medien Verkehrsroute vom lync Server 2010-Edgeserver und-Director auf Ihren lync Server 2013-Edgeserver für eine Bereitstellung mit einem einzelnen Standort umzustellen.</span><span class="sxs-lookup"><span data-stu-id="0efb2-108">Use the following procedures to transition the federation route and the media traffic route from your Lync Server 2010 Edge Server and Director to your Lync Server 2013 Edge Server, for a single-site deployment.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="0efb2-109">Für das Ändern der Route für die Verbund Route und den Mediendatenverkehr müssen Sie Wartungs Ausfälle für die Edgeserver lync Server 2013 und lync Server 2010 planen.</span><span class="sxs-lookup"><span data-stu-id="0efb2-109">Changing the federation route and media traffic route requires that you schedule maintenance downtime for the Lync Server 2013 and Lync Server 2010 Edge Servers.</span></span> <span data-ttu-id="0efb2-110">Dieser gesamte Übergangsprozess bedeutet auch, dass der Verbundzugriff für die Dauer des Ausfalls nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="0efb2-110">This entire transition process also means that federated access will be unavailable for the duration of the outage.</span></span> <span data-ttu-id="0efb2-111">Sie sollten die Downtime für eine Zeit planen, wenn Sie eine minimale Benutzeraktivität erwarten.</span><span class="sxs-lookup"><span data-stu-id="0efb2-111">You should schedule the downtime for a time when you expect minimal user activity.</span></span> <span data-ttu-id="0efb2-112">Darüber hinaus sollten Sie den Endbenutzern eine ausreichende Benachrichtigung senden.</span><span class="sxs-lookup"><span data-stu-id="0efb2-112">You should also provide sufficient notification to your end users.</span></span> <span data-ttu-id="0efb2-113">Planen Sie für diesen Ausfall entsprechend, und setzen Sie in Ihrer Organisation angemessene Erwartungen.</span><span class="sxs-lookup"><span data-stu-id="0efb2-113">Plan accordingly for this outage and set appropriate expectations within your organization.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="0efb2-114">Wenn Ihr Legacy lync Server 2010-Edgeserver so konfiguriert ist, dass derselbe FQDN für den Access-Edgedienst, den Webkonferenz-Edgedienst und den A/V-Edgedienst verwendet wird, werden die Verfahren in diesem Abschnitt nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0efb2-114">If your legacy Lync Server 2010 Edge Server is configured to use the same FQDN for the Access Edge service, Web Conferencing Edge service, and the A/V Edge service, the procedures in this section are not supported.</span></span> <span data-ttu-id="0efb2-115">Wenn die Legacy Edge-Dienste für die Verwendung desselben FQDN konfiguriert sind, müssen Sie zunächst alle Ihre Benutzer von lync Server 2010 zu lync Server 2013 migrieren und dann den lync Server 2010-Edgeserver außer Betrieb setzen, bevor Sie den Verbund auf dem lync Server 2013-Edgeserver aktivieren.</span><span class="sxs-lookup"><span data-stu-id="0efb2-115">If the legacy Edge services are configured to use the same FQDN, you must first migrate all your users from Lync Server 2010 to Lync Server 2013, then decommission the Lync Server 2010 Edge Server before enabling federation on the Lync Server 2013 Edge Server.</span></span>



</div>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="0efb2-116">Wenn Ihr XMPP-Verbund über einen lync Server 2013-Edgeserver weitergeleitet wird, können Legacy-lync Server 2010-Benutzer nicht mit dem XMPP-Verbundpartner kommunizieren, bis alle Benutzer in lync Server 2013, XMPP-Richtlinien und Zertifikate konfiguriert wurden, der XMPP-Verbundpartner auf lync Server 2013 konfiguriert wurde und zuletzt die DNS-Einträge aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="0efb2-116">If your XMPP federation is routed through a Lync Server 2013 Edge Server, legacy Lync Server 2010 users will not be able to communicate with the XMPP federated partner until all users have been moved to Lync Server 2013, XMPP policies and certificates have been configured, the XMPP federated partner has been configured on Lync Server 2013, and lastly the DNS entries have been updated.</span></span>



</div>

<div>

## <a name="to-remove-the-legacy-federation-association-from-lync-server-2013-sites"></a><span data-ttu-id="0efb2-117">So entfernen Sie die Legacy Verbund Zuordnung von lync Server 2013-Websites</span><span class="sxs-lookup"><span data-stu-id="0efb2-117">To remove the legacy federation association from Lync Server 2013 sites</span></span>

1.  <span data-ttu-id="0efb2-118">Öffnen Sie auf dem lync Server 2013-Front-End-Server die vorhandene Topologie im Topologie-Generator.</span><span class="sxs-lookup"><span data-stu-id="0efb2-118">On the Lync Server 2013 Front End server, open the existing topology in Topology Builder.</span></span>

2.  <span data-ttu-id="0efb2-119">Navigieren Sie im linken Bereich zu dem Websiteknoten, der sich direkt unter **lync Server** befindet.</span><span class="sxs-lookup"><span data-stu-id="0efb2-119">In the left pane, navigate to the site node, which is located directly below **Lync Server**.</span></span>

3.  <span data-ttu-id="0efb2-120">Klicken Sie mit der rechten Maustaste auf die Website, und klicken Sie dann auf **Eigenschaften bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="0efb2-120">Right-click the site and then click **Edit Properties**.</span></span>

4.  <span data-ttu-id="0efb2-121">Wählen Sie im linken Bereich **Föderations Route** aus.</span><span class="sxs-lookup"><span data-stu-id="0efb2-121">In the left pane, select **Federation route**.</span></span>

5.  <span data-ttu-id="0efb2-122">Deaktivieren Sie unter **Standort Verbund-Routen Zuweisung** das Kontrollkästchen **SIP-Verbund aktivieren** , um die Verbund Route über die Legacy-lync Server 2010-Umgebung zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="0efb2-122">Under **Site federation route assignment**, clear the **Enable SIP federation** check box to disable the federation route through the legacy Lync Server 2010 environment.</span></span>
    
    <span data-ttu-id="0efb2-123">![Dialogfeld "Eigenschaften bearbeiten", Seite "Verbund Route"](images/JJ688121.8d755ae0-fc7d-4253-b0db-0cf31b863c55(OCS.15).jpg "Dialogfeld "Eigenschaften bearbeiten", Seite "Verbund Route"")</span><span class="sxs-lookup"><span data-stu-id="0efb2-123">![Edit Properties dialog, Federation route page](images/JJ688121.8d755ae0-fc7d-4253-b0db-0cf31b863c55(OCS.15).jpg "Edit Properties dialog, Federation route page")</span></span>

6.  <span data-ttu-id="0efb2-124">Klicken Sie auf **OK** , um die Seite Eigenschaften bearbeiten zu schließen.</span><span class="sxs-lookup"><span data-stu-id="0efb2-124">Click **OK** to close the Edit Properties page.</span></span>

7.  <span data-ttu-id="0efb2-125">Wählen Sie im **Topologie-Generator** den **lync-Server** mit dem obersten Knoten aus.</span><span class="sxs-lookup"><span data-stu-id="0efb2-125">From **Topology Builder**, select the top node **Lync Server**.</span></span>

8.  <span data-ttu-id="0efb2-126">Klicken Sie im Menü **Aktion** auf **Topologie veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="0efb2-126">From the **Action** menu, click **Publish Topology**.</span></span>

9.  <span data-ttu-id="0efb2-127">Klicken Sie auf **weiter** , um den Veröffentlichungsvorgang abzuschließen, und klicken Sie dann auf **Fertig stellen** , wenn der Veröffentlichungsvorgang abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="0efb2-127">Click **Next** to complete the publishing process and then click **Finish** when the publishing process has completed.</span></span>

</div>

<div>

## <a name="to-configure-the-legacy-edge-server-as-a-non-federating-edge-server"></a><span data-ttu-id="0efb2-128">So konfigurieren Sie den Legacy-Edgeserver als nicht-Föderations-Edgeserver</span><span class="sxs-lookup"><span data-stu-id="0efb2-128">To configure the legacy Edge Server as a non-federating Edge Server</span></span>

1.  <span data-ttu-id="0efb2-129">Navigieren Sie im linken Bereich zum Knoten **lync Server 2010** und dann zum Knoten Edge- **Pools** .</span><span class="sxs-lookup"><span data-stu-id="0efb2-129">In the left pane, navigate to the **Lync Server 2010** node and then to the **Edge pools** node.</span></span>

2.  <span data-ttu-id="0efb2-130">Klicken Sie mit der rechten Maustaste auf den Edgeserver, und klicken Sie dann auf **Eigenschaften bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="0efb2-130">Right-click the Edge server, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="0efb2-131">Wählen Sie im linken Bereich die Option **Allgemein** aus.</span><span class="sxs-lookup"><span data-stu-id="0efb2-131">Select **General** in the left pane.</span></span>

4.  <span data-ttu-id="0efb2-132">Deaktivieren Sie das Kontrollkästchen Eintrag **Föderation für diesen Edge-Pool aktivieren (Port 5061)** , und wählen Sie **OK** aus, um die Seite zu schließen.</span><span class="sxs-lookup"><span data-stu-id="0efb2-132">Clear the **Enable federation for this Edge pool (port 5061)** check box entry and select **OK** to close the page.</span></span>
    
    <span data-ttu-id="0efb2-133">![Eigenschaften bearbeiten, allgemein, deaktivieren Föderation aktivieren](images/JJ688121.3be2c8c0-9ed9-4544-bafd-b7694271fafc(OCS.15).jpg "Eigenschaften bearbeiten, allgemein, deaktivieren Föderation aktivieren")</span><span class="sxs-lookup"><span data-stu-id="0efb2-133">![Edit Properties, General, clear Enable federation](images/JJ688121.3be2c8c0-9ed9-4544-bafd-b7694271fafc(OCS.15).jpg "Edit Properties, General, clear Enable federation")</span></span>

5.  <span data-ttu-id="0efb2-134">Wählen Sie im Menü **Aktion** die Option **Topologie veröffentlichen** aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="0efb2-134">From the **Action** menu, select **Publish Topology**, and then click **Next**.</span></span>

6.  <span data-ttu-id="0efb2-135">Klicken Sie nach Abschluss des **Veröffentlichungs-Assistenten** auf **Fertig stellen** , um den Assistenten zu schließen.</span><span class="sxs-lookup"><span data-stu-id="0efb2-135">When the **Publishing wizard** completes, click **Finish** to close the wizard.</span></span>

7.  <span data-ttu-id="0efb2-136">Überprüfen Sie, ob der Verbund für den Legacy-Edgeserver deaktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0efb2-136">Verify federation for the legacy Edge server is disabled.</span></span>
    
    <span data-ttu-id="0efb2-137">![Topologie-Generator, Edge-Pool, Verbund deaktiviert](images/JJ688121.a2948438-d51a-4aeb-9eaa-d899ca950758(OCS.15).jpg "Topologie-Generator, Edge-Pool, Verbund deaktiviert")</span><span class="sxs-lookup"><span data-stu-id="0efb2-137">![Topology Builder, Edge pool, federation disabled](images/JJ688121.a2948438-d51a-4aeb-9eaa-d899ca950758(OCS.15).jpg "Topology Builder, Edge pool, federation disabled")</span></span>

</div>

<div>

## <a name="to-configure-certificates-on-the-lync-server-2010-edge-server"></a><span data-ttu-id="0efb2-138">So konfigurieren Sie Zertifikate auf dem lync Server 2010-Edgeserver</span><span class="sxs-lookup"><span data-stu-id="0efb2-138">To configure certificates on the Lync Server 2010 Edge Server</span></span>

1.  <span data-ttu-id="0efb2-139">Exportieren Sie das Proxy Zertifikat für den externen Zugriff mit dem privaten Schlüssel vom Legacy lync Server 2010-Edgeserver.</span><span class="sxs-lookup"><span data-stu-id="0efb2-139">Export the external Access Proxy certificate, with the private key, from the legacy Lync Server 2010 Edge Server.</span></span>

2.  <span data-ttu-id="0efb2-140">Importieren Sie auf dem lync Server 2013-Edgeserver das externe Zugriffs Proxy Zertifikat aus dem vorherigen Schritt.</span><span class="sxs-lookup"><span data-stu-id="0efb2-140">On the Lync Server 2013 Edge Server, import the Access Proxy external certificate from the previous step.</span></span>

3.  <span data-ttu-id="0efb2-141">Weisen Sie das externe Zertifikat des Zugriffsproxys zur externen lync Server 2013-Schnittstelle des Edgeserver zu.</span><span class="sxs-lookup"><span data-stu-id="0efb2-141">Assign the Access Proxy external certificate to the Lync Server 2013 external interface of the Edge Server.</span></span>

4.  <span data-ttu-id="0efb2-142">Das interne Schnittstellen Zertifikat des lync Server 2013-Edge-Servers sollte von einer vertrauenswürdigen Zertifizierungsstelle angefordert und zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="0efb2-142">The internal interface certificate of the Lync Server 2013 Edge Server should be requested from a trusted CA and assigned.</span></span>

</div>

<div>

## <a name="to-change-lync-server-2010-federation-route-to-use-lync-server-2013-edge-server"></a><span data-ttu-id="0efb2-143">So ändern Sie die lync Server 2010-Verbund Route zur Verwendung des lync Server 2013 Edge-Servers</span><span class="sxs-lookup"><span data-stu-id="0efb2-143">To change Lync Server 2010 federation route to use Lync Server 2013 Edge Server</span></span>

1.  <span data-ttu-id="0efb2-144">Navigieren Sie vom Topologie-Generator im linken Bereich zum Knoten **lync Server 2013** und dann zum Knoten Edge- **Pools** .</span><span class="sxs-lookup"><span data-stu-id="0efb2-144">From Topology Builder, in the left pane, navigate to the **Lync Server 2013** node and then to the **Edge pools** node.</span></span>

2.  <span data-ttu-id="0efb2-145">Klicken Sie mit der rechten Maustaste auf den Edgeserver, und klicken Sie dann auf **Eigenschaften bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="0efb2-145">Right-click the Edge server, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="0efb2-146">Wählen Sie im linken Bereich die Option **Allgemein** aus.</span><span class="sxs-lookup"><span data-stu-id="0efb2-146">Select **General** in the left pane.</span></span>

4.  <span data-ttu-id="0efb2-147">Aktivieren Sie den Kontrollkästchen Eintrag für **enable Federation for this Edge Pool (Port 5061)** , und klicken Sie dann auf **OK** , um die Seite zu schließen.</span><span class="sxs-lookup"><span data-stu-id="0efb2-147">Select the check box entry for **Enable federation for this Edge pool (port 5061)** and then click **OK** to close the page.</span></span>
    
    <span data-ttu-id="0efb2-148">![Dialogfeld "Eigenschaften bearbeiten", Seite "Allgemein"](images/JJ688121.cc79a88c-cce4-4cab-80ad-4f70325dc7c4(OCS.15).jpg "Dialogfeld "Eigenschaften bearbeiten", Seite "Allgemein"")</span><span class="sxs-lookup"><span data-stu-id="0efb2-148">![Edit Properties dialog, General page](images/JJ688121.cc79a88c-cce4-4cab-80ad-4f70325dc7c4(OCS.15).jpg "Edit Properties dialog, General page")</span></span>

5.  <span data-ttu-id="0efb2-149">Wählen Sie im Menü **Aktion** die Option **Topologie veröffentlichen** aus, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="0efb2-149">From the **Action** menu, select **Publish Topology**, and then click **Next**.</span></span>

6.  <span data-ttu-id="0efb2-150">Klicken Sie nach Abschluss des **Veröffentlichungs-Assistenten** auf **Fertig stellen** , um den Assistenten zu schließen.</span><span class="sxs-lookup"><span data-stu-id="0efb2-150">When the **Publishing wizard** completes, click **Finish** to close the wizard.</span></span>

7.  <span data-ttu-id="0efb2-151">Überprüfen Sie, ob der **Verbund (Port 5061)** auf **aktiviert** festgesetzt ist.</span><span class="sxs-lookup"><span data-stu-id="0efb2-151">Verify **Federation (port 5061)** is set to **Enabled**.</span></span>
    
    <span data-ttu-id="0efb2-152">![Topologie-Generator, Edge-Pool, Verbund aktiviert](images/JJ688121.e8ccdada-23f4-47e5-a99d-5bf795fefc48(OCS.15).jpg "Topologie-Generator, Edge-Pool, Verbund aktiviert")</span><span class="sxs-lookup"><span data-stu-id="0efb2-152">![Topology Builder, Edge pool, Federation enabled](images/JJ688121.e8ccdada-23f4-47e5-a99d-5bf795fefc48(OCS.15).jpg "Topology Builder, Edge pool, Federation enabled")</span></span>

</div>

<div>

## <a name="to-update-lync-server-2013-edge-server-federation-next-hop"></a><span data-ttu-id="0efb2-153">So aktualisieren Sie den nächsten Hop von lync Server 2013 Edge Server Federation</span><span class="sxs-lookup"><span data-stu-id="0efb2-153">To update Lync Server 2013 Edge Server federation next hop</span></span>

1.  <span data-ttu-id="0efb2-154">Navigieren Sie vom Topologie-Generator im linken Bereich zum Knoten **lync Server 2013** und dann zum Knoten Edge- **Pools** .</span><span class="sxs-lookup"><span data-stu-id="0efb2-154">From Topology Builder, in the left pane, navigate to the **Lync Server 2013** node and then to the **Edge pools** node.</span></span>

2.  <span data-ttu-id="0efb2-155">Erweitern Sie den Knoten, klicken Sie mit der rechten Maustaste auf den aufgelisteten Edgeserver, und klicken Sie dann auf **Eigenschaften bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="0efb2-155">Expand the node, right-click the Edge Server listed, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="0efb2-156">Wählen Sie auf der Seite **Allgemein** unter Auswahl für den **nächsten Hop** in der Dropdownliste den lync Server 2013-Pool aus.</span><span class="sxs-lookup"><span data-stu-id="0efb2-156">On the **General** page, under **Next hop selection**, select from the drop-down list the Lync Server 2013  pool.</span></span>
    
    <span data-ttu-id="0efb2-157">![Dialogfeld ' Eigenschaften bearbeiten ', Seite ' nächster Hop '](images/JJ688121.5741b9a8-e729-4457-9f62-38f08a2c5b02(OCS.15).jpg "Dialogfeld ' Eigenschaften bearbeiten ', Seite ' nächster Hop '")</span><span class="sxs-lookup"><span data-stu-id="0efb2-157">![Edit Properties dialog, Next hop page](images/JJ688121.5741b9a8-e729-4457-9f62-38f08a2c5b02(OCS.15).jpg "Edit Properties dialog, Next hop page")</span></span>

4.  <span data-ttu-id="0efb2-158">Klicken Sie auf **OK** , um die Seite Eigenschaften bearbeiten zu schließen.</span><span class="sxs-lookup"><span data-stu-id="0efb2-158">Click **OK** to close the Edit Properties page.</span></span>

5.  <span data-ttu-id="0efb2-159">Wählen Sie im **Topologie-Generator** den **lync-Server** mit dem obersten Knoten aus.</span><span class="sxs-lookup"><span data-stu-id="0efb2-159">From **Topology Builder**, select the top node **Lync Server** .</span></span>

6.  <span data-ttu-id="0efb2-160">Klicken Sie im Menü **Aktion** auf **Topologie veröffentlichen** , und schließen Sie den Assistenten ab.</span><span class="sxs-lookup"><span data-stu-id="0efb2-160">From the **Action** menu, click **Publish Topology** and complete the wizard.</span></span>

</div>

<div>

## <a name="to-configure-lync-server-2013-edge-server-outbound-media-path"></a><span data-ttu-id="0efb2-161">So konfigurieren Sie den ausgehenden Medienpfad von lync Server 2013 Edge Server</span><span class="sxs-lookup"><span data-stu-id="0efb2-161">To configure Lync Server 2013 Edge Server outbound media path</span></span>

1.  <span data-ttu-id="0efb2-162">Navigieren Sie vom Topologie-Generator im linken Bereich zu dem **lync Server 2013** -Knoten, und klicken Sie dann auf den Pool unter **Standard Edition-Front-End-Server** oder **Enterprise Edition-Front-End-Pools**.</span><span class="sxs-lookup"><span data-stu-id="0efb2-162">From Topology Builder, in the left pane, navigate to the **Lync Server 2013** node and then to the pool below **Standard Edition Front End Servers** or **Enterprise Edition Front End pools**.</span></span>

2.  <span data-ttu-id="0efb2-163">Klicken Sie mit der rechten Maustaste auf den Pool, und klicken Sie dann auf **Eigenschaften bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="0efb2-163">Right-click the pool, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="0efb2-164">Aktivieren Sie im Abschnitt **Zuordnungen** das Kontrollkästchen **Edge-Pool zuordnen (für Medienkomponenten)** .</span><span class="sxs-lookup"><span data-stu-id="0efb2-164">In the **Associations** section, select the **Associate Edge pool (for media components)** check box.</span></span>
    
    <span data-ttu-id="0efb2-165">![Bearbeiten von Eigenschaften, allgemein, Verknüpfen des Edge-Pools](images/JJ688121.fd9b18ca-fda2-4764-9bf0-726bf39f6a12(OCS.15).jpg "Bearbeiten von Eigenschaften, allgemein, Verknüpfen des Edge-Pools")</span><span class="sxs-lookup"><span data-stu-id="0efb2-165">![Edit Properties, General, Associate Edge pool](images/JJ688121.fd9b18ca-fda2-4764-9bf0-726bf39f6a12(OCS.15).jpg "Edit Properties, General, Associate Edge pool")</span></span>

4.  <span data-ttu-id="0efb2-166">Wählen Sie im Dropdownfeld den lync Server 2013-Edgeserver aus.</span><span class="sxs-lookup"><span data-stu-id="0efb2-166">From the drop down box, select the Lync Server 2013 Edge Server.</span></span>

5.  <span data-ttu-id="0efb2-167">Klicken Sie auf **OK** , um die Seite **Eigenschaften bearbeiten** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="0efb2-167">Click **OK** to close the **Edit Properties** page.</span></span>

</div>

<div>

## <a name="to-turn-on-lync-server-2013-edge-server-federation"></a><span data-ttu-id="0efb2-168">So aktivieren Sie den lync Server 2013-Edgeserver-Verbund</span><span class="sxs-lookup"><span data-stu-id="0efb2-168">To turn on Lync Server 2013 Edge Server federation</span></span>

1.  <span data-ttu-id="0efb2-169">Navigieren Sie vom Topologie-Generator im linken Bereich zum Knoten **lync Server 2013** und dann zum Knoten Edge- **Pools** .</span><span class="sxs-lookup"><span data-stu-id="0efb2-169">From Topology Builder, in the left pane, navigate to the **Lync Server 2013** node and then to the **Edge pools** node.</span></span>

2.  <span data-ttu-id="0efb2-170">Erweitern Sie den Knoten, klicken Sie mit der rechten Maustaste auf den aufgelisteten Edgeserver, und klicken Sie dann auf **Eigenschaften bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="0efb2-170">Expand the node, right-click the Edge Server listed, and then click **Edit Properties**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0efb2-171">Der Verbund kann nur für einen einzelnen Edge-Pool aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="0efb2-171">Federation can only be enabled for a single Edge pool.</span></span> <span data-ttu-id="0efb2-172">Wenn Sie über mehrere Edge-Pools verfügen, wählen Sie eine aus, die Sie als Föderations-Edge-Pool verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="0efb2-172">If you have multiple Edge pools, select one to use as the federating Edge pool.</span></span>

    
    </div>

3.  <span data-ttu-id="0efb2-173">Überprüfen Sie auf der Seite **Allgemein** , ob die Einstellung **Föderation für diesen Edge-Pool aktivieren (Port 5061)** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0efb2-173">On the **General** page, verify the **Enable federation for this Edge pool (Port 5061)** setting is checked.</span></span>
    
    <span data-ttu-id="0efb2-174">![Dialogfeld "Eigenschaften bearbeiten", Seite "Allgemein"](images/JJ688121.cc79a88c-cce4-4cab-80ad-4f70325dc7c4(OCS.15).jpg "Dialogfeld "Eigenschaften bearbeiten", Seite "Allgemein"")</span><span class="sxs-lookup"><span data-stu-id="0efb2-174">![Edit Properties dialog, General page](images/JJ688121.cc79a88c-cce4-4cab-80ad-4f70325dc7c4(OCS.15).jpg "Edit Properties dialog, General page")</span></span>

4.  <span data-ttu-id="0efb2-175">Klicken Sie auf **OK** , um die Seite Eigenschaften bearbeiten zu schließen.</span><span class="sxs-lookup"><span data-stu-id="0efb2-175">Click **OK** to close the Edit Properties page.</span></span>

5.  <span data-ttu-id="0efb2-176">Navigieren Sie als nächstes zum Websiteknoten.</span><span class="sxs-lookup"><span data-stu-id="0efb2-176">Next, navigate to the site node.</span></span>

6.  <span data-ttu-id="0efb2-177">Klicken Sie mit der rechten Maustaste auf die Website, und klicken Sie dann auf **Eigenschaften bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="0efb2-177">Right-click the site, and then click **Edit Properties**.</span></span>

7.  <span data-ttu-id="0efb2-178">Klicken Sie im linken Bereich auf **Föderations Route**.</span><span class="sxs-lookup"><span data-stu-id="0efb2-178">In the left pane, click **Federation route**.</span></span>

8.  <span data-ttu-id="0efb2-179">Wählen Sie unter **Website Verbund-Routenzuordnung** die Option **SIP-Verbund aktivieren** aus, und wählen Sie dann in der Liste den Eintrag lync Server 2013 Edge Server aus.</span><span class="sxs-lookup"><span data-stu-id="0efb2-179">Under **Site federation route assignment**, select **Enable SIP federation**, and then from the list select the Lync Server 2013 Edge Server listed.</span></span>
    
    <span data-ttu-id="0efb2-180">![Eigenschaften bearbeiten, Seite "Verbund Route"](images/JJ688121.c50c13b8-0859-4e3e-8793-45c431a5b4b5(OCS.15).jpg "Eigenschaften bearbeiten, Seite "Verbund Route"")</span><span class="sxs-lookup"><span data-stu-id="0efb2-180">![Edit Properties, Federation route page](images/JJ688121.c50c13b8-0859-4e3e-8793-45c431a5b4b5(OCS.15).jpg "Edit Properties, Federation route page")</span></span>

9.  <span data-ttu-id="0efb2-181">Klicken Sie auf **OK** , um die Seite **Eigenschaften bearbeiten** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="0efb2-181">Click **OK** to close the **Edit Properties** page.</span></span>
    
    <span data-ttu-id="0efb2-182">Führen Sie für die Bereitstellung mehrerer Websites dieses Verfahren an jedem Standort aus.</span><span class="sxs-lookup"><span data-stu-id="0efb2-182">For multi-site deployments, complete this procedure at each site.</span></span>

</div>

<div>

## <a name="to-publish-edge-server-configuration-changes"></a><span data-ttu-id="0efb2-183">So veröffentlichen Sie Änderungen an Edge-Server-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="0efb2-183">To publish Edge Server configuration changes</span></span>

1.  <span data-ttu-id="0efb2-184">Wählen Sie im **Topologie-Generator** den **lync-Server** mit dem obersten Knoten aus.</span><span class="sxs-lookup"><span data-stu-id="0efb2-184">From **Topology Builder**, select the top node **Lync Server** .</span></span>

2.  <span data-ttu-id="0efb2-185">Wählen Sie im Menü **Aktion** die Option **Topologie veröffentlichen** aus, und schließen Sie den Assistenten ab.</span><span class="sxs-lookup"><span data-stu-id="0efb2-185">From the **Action** menu, select **Publish Topology** and complete the wizard.</span></span>

3.  <span data-ttu-id="0efb2-186">Warten Sie, bis die Active Directory-Replikation für alle Pools in der Bereitstellung erfolgt.</span><span class="sxs-lookup"><span data-stu-id="0efb2-186">Wait for Active Directory replication to occur to all pools in the deployment.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0efb2-187">Möglicherweise wird die folgende Meldung angezeigt:</span><span class="sxs-lookup"><span data-stu-id="0efb2-187">You may see the following message:</span></span><BR><span data-ttu-id="0efb2-188"><STRONG>Warnung: die Topologie enthält mehr als einen Federated-Edgeserver. Dies kann während der Migration zu einer neueren Version des Produkts auftreten. In diesem Fall würde nur ein Edgeserver für den Verbund aktiv verwendet. Überprüfen Sie, ob der externe DNS-SRV-Eintrag auf den richtigen Edgeserver verweist. Wenn Sie mehrere Verbund-Edgeserver bereitstellen möchten, um gleichzeitig aktiv zu sein (also kein Migrationsszenario), stellen Sie sicher, dass alle Verbundpartner lync Server verwenden. Überprüfen Sie, ob der externe DNS-SRV-Eintrag alle Verbund fähigen Edgeserver auflistet.</STRONG></span><span class="sxs-lookup"><span data-stu-id="0efb2-188"><STRONG>Warning: The topology contains more than one Federated Edge Server. This can occur during migration to a more recent version of the product. In that case, only one Edge Server would be actively used for federation. Verify that the external DNS SRV record points to the correct Edge Server. If you want to deploy multiple federation Edge Server to be active concurrently (that is, not a migration scenario), verify that all federated partners are using Lync Server. Verify that the external DNS SRV record lists all federation enabled Edge Servers.</STRONG></span></span><BR><span data-ttu-id="0efb2-189">Diese Warnung wird erwartet und kann bedenkenlos ignoriert werden.</span><span class="sxs-lookup"><span data-stu-id="0efb2-189">This warning is expected and can be safely ignored.</span></span>

    
    </div>

</div>

<div>

## <a name="to-configure-lync-server-2013-edge-server"></a><span data-ttu-id="0efb2-190">So konfigurieren Sie den lync Server 2013-Edgeserver</span><span class="sxs-lookup"><span data-stu-id="0efb2-190">To configure Lync Server 2013 Edge Server</span></span>

1.  <span data-ttu-id="0efb2-191">Bringen Sie alle lync Server 2013-Edgeserver online.</span><span class="sxs-lookup"><span data-stu-id="0efb2-191">Bring all of the Lync Server 2013 Edge Servers online.</span></span>

2.  <span data-ttu-id="0efb2-192">Aktualisieren Sie die Routingregeln für externe Firewalls oder die Einstellungen für das Hardwarelastenausgleich, um SIP-Datenverkehr für externen Zugriff (normalerweise Port 443) und Föderation (in der Regel Port 5061) an den lync Server 2013-Edgeserver anstelle des Legacy-Edgeserver zu senden.</span><span class="sxs-lookup"><span data-stu-id="0efb2-192">Update the external firewall routing rules or the hardware load balancer settings to send SIP traffic for external access (usually port 443) and federation (usually port 5061) to the Lync Server 2013 Edge Server, instead of the legacy Edge Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0efb2-193">Wenn Sie nicht über ein Hardware-Lastenausgleichsmodul verfügen, müssen Sie den DNS-a-Eintrag für die Föderation aktualisieren, damit er auf den neuen lync Server Access-Edgeserver aufgelöst werden kann.</span><span class="sxs-lookup"><span data-stu-id="0efb2-193">If you do not have a hardware load balancer, you need to update the DNS A record for federation to resolve to the new Lync Server Access Edge server.</span></span> <span data-ttu-id="0efb2-194">Um dies bei minimaler Unterbrechung zu erreichen, verringern Sie den TLL-Wert für den externen lync Server Access-Edge-FQDN, sodass beim Aktualisieren von DNS auf den neuen lync Server Access-Edge die Föderation und der Remotezugriff schnell aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0efb2-194">To accomplish this with minimum disruption, reduce the TLL value for the external Lync Server Access Edge FQDN so that when DNS is updated to point to the new Lync Server Access Edge, federation and remote access will be updated quickly.</span></span>

    
    </div>

3.  <span data-ttu-id="0efb2-195">Beenden Sie als nächstes den **lync Server Access-Edge** von jedem Edgeserver-Computer.</span><span class="sxs-lookup"><span data-stu-id="0efb2-195">Next, stop the **Lync Server Access Edge** from each Edge Server computer.</span></span>

4.  <span data-ttu-id="0efb2-196">Öffnen Sie auf jedem Legacy-Edgeserver-Computer das Applet **Dienste** in den **Verwaltungs Tools**.</span><span class="sxs-lookup"><span data-stu-id="0efb2-196">From each legacy Edge Server computer, open the **Services** applet from the **Administrative Tools**.</span></span>

5.  <span data-ttu-id="0efb2-197">Suchen Sie in der Liste Dienste nach **lync Server Access Edge**.</span><span class="sxs-lookup"><span data-stu-id="0efb2-197">In the services list, find **Lync Server Access Edge**.</span></span>

6.  <span data-ttu-id="0efb2-198">Klicken Sie mit der rechten Maustaste auf den Namen der Dienste, und wählen Sie dann **Beenden** aus, um den Dienst zu beenden.</span><span class="sxs-lookup"><span data-stu-id="0efb2-198">Right-click the services name, and then select **Stop** to stop the service.</span></span>

7.  <span data-ttu-id="0efb2-199">Setzen Sie den Starttyp auf **disabled**.</span><span class="sxs-lookup"><span data-stu-id="0efb2-199">Set the Startup type to **Disabled**.</span></span>

8.  <span data-ttu-id="0efb2-200">Klicken Sie auf **OK** , um das **Eigenschaften** Fenster zu schließen.</span><span class="sxs-lookup"><span data-stu-id="0efb2-200">Click **OK** to close the **Properties** window.</span></span>

<span data-ttu-id="0efb2-201"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0efb2-201"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

