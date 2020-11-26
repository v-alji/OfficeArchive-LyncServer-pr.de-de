---
title: 'Lync Server 2013: Definieren der Edgetopologie'
description: 'Lync Server 2013: Definieren Ihrer Edge-Topologie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Define your edge topology
ms:assetid: 787b23f1-8fa0-4c37-abf2-c516c5dd66f0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398591(v=OCS.15)
ms:contentKeyID: 48184562
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bd4aa16ca23d24f0edd92189216030ef926fc841
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431036"
---
# <a name="define-your-edge-topology-in-lync-server-2013"></a><span data-ttu-id="db12c-103">Definieren der Edgetopologie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="db12c-103">Define your edge topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="db12c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="db12c-104">

<span> </span></span></span>

<span data-ttu-id="db12c-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="db12c-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="db12c-106">Sie müssen den Topologie-Generator verwenden, um Ihre Topologie zu erstellen, und Sie müssen mindestens einen internen Front-End-Pool oder Standard Edition-Server einrichten, bevor Sie den Edgeserver bereitstellen können.</span><span class="sxs-lookup"><span data-stu-id="db12c-106">You must use Topology Builder to build your topology and you must set up at least one internal Front End pool or Standard Edition server before you can deploy your Edge Server.</span></span> <span data-ttu-id="db12c-107">Gehen Sie wie folgt vor, um die Edge-Topologie für einen einzelnen Edgeserver zu definieren, und verwenden Sie dann die Verfahren unter [Veröffentlichen Ihrer Topologie in lync Server 2013](lync-server-2013-publish-your-topology.md) , und [exportieren Sie Ihre lync Server 2013-Topologie, und kopieren Sie Sie für die Edge-Installation auf externe Medien](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md) , um die Topologie zu veröffentlichen und für Ihren Edgeserver verfügbar zu machen.</span><span class="sxs-lookup"><span data-stu-id="db12c-107">Use the following procedure to define the edge topology for a single Edge Server, and then use the procedures in [Publish your topology in Lync Server 2013](lync-server-2013-publish-your-topology.md) and [Export your Lync Server 2013 topology and copy it to external media for edge installation](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md) to publish the topology and make it available to your Edge Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="db12c-108">Für die interne Edgeschnittstelle und die externe Edgeschnittstelle muss derselbe Typ von Lastenausgleich verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="db12c-108">The internal Edge interface and external Edge interface must use the same type of load balancing.</span></span> <span data-ttu-id="db12c-109">Es ist nicht möglich, für eine Edgeschnittstelle den DNS-Lastenausgleich und für die andere Edgeschnittstelle ein Hardwaregerät zum Lastenausgleich zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="db12c-109">You cannot use DNS load balancing on one Edge interface and hardware load balancing on the other Edge interface.</span></span>



</div>

<span data-ttu-id="db12c-110">Um eine Topologie beim Hinzufügen oder Entfernen einer Serverrolle erfolgreich zu veröffentlichen, zu aktivieren oder zu deaktivieren, müssen Sie als Benutzer angemeldet sein, der Mitglied der Gruppen RTCUniversalServerAdmins und Domänenadministratoren ist.</span><span class="sxs-lookup"><span data-stu-id="db12c-110">To successfully publish, enable, or disable a topology when adding or removing a server role, you must be logged in as a user who is a member of the RTCUniversalServerAdmins and Domain Admins groups.</span></span> <span data-ttu-id="db12c-111">Sie können auch die Administratorrechte und-Berechtigungen erteilen, die für das Hinzufügen von Serverrollen zu einem Benutzerkonto erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="db12c-111">You can also grant the administrator rights and permissions required for adding server roles to a user account.</span></span> <span data-ttu-id="db12c-112">Ausführliche Informationen finden Sie unter [Delegieren von Setup Berechtigungen in lync Server 2013](lync-server-2013-delegate-setup-permissions.md) in der Dokumentation zur Standard Edition-Server-oder Enterprise Edition-Server Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="db12c-112">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md) in the Standard Edition server or Enterprise Edition server Deployment documentation.</span></span> <span data-ttu-id="db12c-113">Bei anderen Konfigurationsänderungen ist nur die Mitgliedschaft in der RTCUniversalServerAdmins-Gruppe erforderlich.</span><span class="sxs-lookup"><span data-stu-id="db12c-113">For other configuration changes, only membership in the RTCUniversalServerAdmins group is required.</span></span>

<span data-ttu-id="db12c-114">Wenn Sie Ihre Edge-Topologie beim Definieren und Veröffentlichen Ihrer internen Topologie definiert haben und für die zuvor definierte Edge-Topologie keine Änderungen erforderlich sind, müssen Sie Sie nicht definieren und erneut veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="db12c-114">If you defined your edge topology when you defined and published your internal topology, and no changes are required to the edge topology that you previously defined, you do not need to do define it and publish it again.</span></span> <span data-ttu-id="db12c-115">Führen Sie das folgende Verfahren nur aus, wenn Sie Änderungen an ihrer Edge-Topologie vornehmen müssen.</span><span class="sxs-lookup"><span data-stu-id="db12c-115">Use the following procedure only if you need to make changes to your edge topology.</span></span> <span data-ttu-id="db12c-116">Sie müssen die zuvor definierte und veröffentlichte Topologie für Ihre Edgeserver verfügbar machen, indem Sie das Verfahren zum [Exportieren Ihrer lync Server 2013-Topologie verwenden und Sie für die Edge-Installation auf externe Medien kopieren](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md).</span><span class="sxs-lookup"><span data-stu-id="db12c-116">You must make the previously defined and published topology available to your Edge Servers, which you do by using the procedure in [Export your Lync Server 2013 topology and copy it to external media for edge installation](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="db12c-117">Sie können den Topology Builder nicht auf einem Edgeserver ausführen.</span><span class="sxs-lookup"><span data-stu-id="db12c-117">You cannot run Topology Builder from an Edge Server.</span></span> <span data-ttu-id="db12c-118">Sie müssen es auf dem Front-End-Server oder auf Standard Edition-Servern ausführen.</span><span class="sxs-lookup"><span data-stu-id="db12c-118">You must run it from your Front End Server or Standard Edition servers.</span></span>



</div>

<span data-ttu-id="db12c-119">Der Prozess zum Definieren Ihrer Edge-Server-Topologie erfolgt im Topologie-Generator.</span><span class="sxs-lookup"><span data-stu-id="db12c-119">The process to define your Edge Server topology is done in Topology Builder.</span></span> <span data-ttu-id="db12c-120">Die drei Haupttypen von Edge-Server-Topologien, die Sie planen und konfigurieren, sind nachfolgend aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="db12c-120">The three primary types of Edge Server topologies that you plan and configure are listed below:</span></span>

  - <span data-ttu-id="db12c-121">So definieren Sie die Topologie für einen einzelnen Edgeserver</span><span class="sxs-lookup"><span data-stu-id="db12c-121">To define the Topology for a Single Edge Server</span></span>

  - <span data-ttu-id="db12c-122">So definieren Sie die Topologie für einen Lastenausgleichs-Edge-Server Pool</span><span class="sxs-lookup"><span data-stu-id="db12c-122">To define the Topology for a Load Balanced Edge Server Pool</span></span>

  - <span data-ttu-id="db12c-123">So definieren Sie die Topologie für einen Hardware Lastenausgleich-Edge-Pool</span><span class="sxs-lookup"><span data-stu-id="db12c-123">To define the Topology for a Hardware Load Balanced Edge Pool</span></span>

<div>

## <a name="to-define-the-topology-for-a-single-edge-server"></a><span data-ttu-id="db12c-124">So definieren Sie die Topologie für einen einzelnen Edgeserver</span><span class="sxs-lookup"><span data-stu-id="db12c-124">To define the topology for a single Edge Server</span></span>

1.  <span data-ttu-id="db12c-125">Starten Sie den Topologie-Generator: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server Topology Builder**.</span><span class="sxs-lookup"><span data-stu-id="db12c-125">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="db12c-126">Erweitern Sie in der Konsolenstruktur die Website, auf der Sie einen Edgeserver bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="db12c-126">In the console tree, expand the site in which you want to deploy an Edge Server.</span></span>

3.  <span data-ttu-id="db12c-127">Klicken Sie mit der rechten Maustaste auf **Edge-Pools**, und klicken Sie dann auf **neuer Edge-Pool**.</span><span class="sxs-lookup"><span data-stu-id="db12c-127">Right-click **Edge pools**, and then click **New Edge Pool**.</span></span>

4.  <span data-ttu-id="db12c-128">Klicken Sie unter **neuen Edge-Pool definieren** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-128">In **Define the New Edge Pool**, click **Next**.</span></span>

5.  <span data-ttu-id="db12c-129">Gehen Sie unter **Definieren des FQDN des Edge-Pools** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="db12c-129">In **Define the Edge pool FQDN**, do the following:</span></span>
    
      - <span data-ttu-id="db12c-130">Geben Sie in **Pool FQDN** den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) der internen Schnittstelle für den Edgeserver ein.</span><span class="sxs-lookup"><span data-stu-id="db12c-130">In **Pool FQDN**, type the fully qualified domain name (FQDN) of the internal interface for the Edge Server.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="db12c-131">Der angegebene Name muss mit dem auf dem Server konfigurierten Computernamen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="db12c-131">The name you specify must be identical to the computer name configured on the server.</span></span> <span data-ttu-id="db12c-132">Standardmäßig ist der Computername eines Computers, der nicht zu einer Domäne gehört, ein kurzer Name und kein FQDN.</span><span class="sxs-lookup"><span data-stu-id="db12c-132">By default the computer name of a computer that is not joined to a domain is a short name, not an FQDN.</span></span> <span data-ttu-id="db12c-133">Der Topologie-Generator verwendet keine Kurznamen, sondern FQDNs.</span><span class="sxs-lookup"><span data-stu-id="db12c-133">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="db12c-134">Daher müssen Sie ein DNS-Suffix für den Namen des Computers konfigurieren, der als Edgeserver bereitgestellt werden soll und nicht Mitglied einer Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="db12c-134">So, you must configure a DNS suffix on the name of the computer to be deployed as an Edge Server that is not joined to a domain.</span></span> <span data-ttu-id="db12c-135">Verwenden Sie nur Standardzeichen (also A – Z, a – z, 0 – 9 und Bindestriche) beim Zuweisen von FQDNs der Server mit Lync Server, Edgeserver und Pools.</span><span class="sxs-lookup"><span data-stu-id="db12c-135">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="db12c-136">Verwenden Sie keine Unicode-Zeichen oder Unterstriche.</span><span class="sxs-lookup"><span data-stu-id="db12c-136">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="db12c-137">Nicht standardmäßige Zeichen in einem FQDN werden häufig nicht von externen DNS-und öffentlichen CAS unterstützt (wenn der FQDN dem SN im Zertifikat zugewiesen werden muss).</span><span class="sxs-lookup"><span data-stu-id="db12c-137">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span> <span data-ttu-id="db12c-138">Details zum Hinzufügen eines DNS-Suffix zu einem Computernamen finden Sie unter <A href="lync-server-2013-configure-dns-for-edge-support.md">Konfigurieren von DNS für die Edge-Unterstützung in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="db12c-138">For details about adding a DNS suffix to a computer name, see <A href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</A>.</span></span>

        
        </div>
    
      - <span data-ttu-id="db12c-139">Klicken Sie auf **Einzelcomputer Pool**, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-139">Click **Single computer pool**, and then click **Next**.</span></span>

6.  <span data-ttu-id="db12c-140">Gehen **Sie unter Features auswählen** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="db12c-140">In **Select features**, do the following:</span></span>
    
      - <span data-ttu-id="db12c-141">Wenn Sie einen einzelnen FQDN und eine IP-Adresse für den SIP-Zugriffsdienst, den lync Server 2013-Webkonferenzdienst und a/V-Edgedienst verwenden möchten, aktivieren Sie das Kontrollkästchen **einen einzelnen FQDN und eine IP-Adresse verwenden** .</span><span class="sxs-lookup"><span data-stu-id="db12c-141">If you plan to use a single FQDN and IP address for the SIP Access service, Lync Server 2013 Web Conferencing service, and A/V Edge services, select the **Use a single FQDN and IP Address** check box.</span></span>
    
      - <span data-ttu-id="db12c-142">Wenn Sie beabsichtigen, die Föderation zu aktivieren, aktivieren Sie das Kontrollkästchen **Föderation für diesen Edge-Pool aktivieren (Port 5061)** .</span><span class="sxs-lookup"><span data-stu-id="db12c-142">If you plan to enable federation select the **Enable federation for this Edge pool (Port 5061)** check box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="db12c-143">Sie können diese Option auswählen, aber nur ein Edge-Pool oder Edgeserver in Ihrer Organisation kann extern für den Verbund veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="db12c-143">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="db12c-144">Der gesamte Zugriff von Verbundbenutzern, einschließlich öffentlicher Chat-Benutzer, durchlaufen denselben Edge-Pool oder Single Edge-Server.</span><span class="sxs-lookup"><span data-stu-id="db12c-144">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="db12c-145">Wenn Ihre Bereitstellung beispielsweise einen Edge-Pool oder einen einzelnen Edgeserver umfasst, der in New York bereitgestellt und in London bereitgestellt wurde, und Sie die Föderations Unterstützung auf dem New York Edge-Pool oder Single Edge-Server aktivieren, wird der Signal Verkehr für verbundene Benutzer durch den New York Edge-Pool oder den Single Edge-Server durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="db12c-145">For example, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="db12c-146">Dies gilt auch für die Kommunikation mit Benutzern in London, wenngleich ein interner Benutzer in London, der einen Partnerbenutzer in London anruft, für den A/V-Datenverkehr den Pool oder Edgeserver in London verwendet.</span><span class="sxs-lookup"><span data-stu-id="db12c-146">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

        
        </div>
    
      - <span data-ttu-id="db12c-147">Wenn Sie beabsichtigen, das Extensible Messaging and Presence Protocol (XMPP) für Ihre Bereitstellung zu unterstützen, aktivieren Sie das Kontrollkästchen **XMPP-Föderation aktivieren (Port 5269)** .</span><span class="sxs-lookup"><span data-stu-id="db12c-147">If you plan to support the extensible messaging and presence protocol (XMPP) for your deployment, select the **Enable XMPP federation (port 5269)** check box</span></span>

7.  <span data-ttu-id="db12c-148">Gehen **Sie unter IP-Optionen auswählen** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="db12c-148">In **Select IP Options**, do the following:</span></span>
    
      - <span data-ttu-id="db12c-149">**Aktivieren von IPv4 auf interner Schnittstelle**: Aktivieren Sie das Kontrollkästchen, wenn Sie eine IPv4-Adresse auf die interne Schnittstelle des Edge-Servers oder des Edge-Pools anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="db12c-149">**Enable IPv4 on internal interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="db12c-150">**Aktivieren von IPv6 auf interner Schnittstelle**: Aktivieren Sie das Kontrollkästchen, wenn Sie eine IPv6-Adresse auf die interne Schnittstelle des Edge-Servers oder des Edge-Pools anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="db12c-150">**Enable IPv6 on internal interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="db12c-151">**Aktivieren von IPv4 auf externer Schnittstelle**: Aktivieren Sie das Kontrollkästchen, wenn Sie eine IPv4-Adresse auf die externe Schnittstelle des Edge-Servers oder des Edge-Pools anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="db12c-151">**Enable IPv4 on external interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool external interface</span></span>
    
      - <span data-ttu-id="db12c-152">**Aktivieren von IPv6 auf einer externen Schnittstelle**: Aktivieren Sie das Kontrollkästchen, wenn Sie eine IPv6-Adresse auf die externe Schnittstelle des Edge-Servers oder des Edge-Pools anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="db12c-152">**Enable IPv6 on external interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool external interface</span></span>
    
    <span data-ttu-id="db12c-153">Sie können auch den Edgeserver oder den Edge-Pool so konfigurieren, dass für die externen IP-Adressen eine Adresse für die Netzwerkadressübersetzung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db12c-153">You can also configure the Edge Server or Edge pool to use a network address translation address for the external IP addresses.</span></span> <span data-ttu-id="db12c-154">Aktivieren Sie dazu das Kontrollkästchen, um **die externe IP-Adresse dieses Edge-Pools von NAT zu übersetzen**.</span><span class="sxs-lookup"><span data-stu-id="db12c-154">You do this by selecting the check box **The external IP address of this Edge pool is translated by NAT**.</span></span>

8.  <span data-ttu-id="db12c-155">Führen Sie in **externen FQDNs** die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="db12c-155">In **External FQDNs**, do the following:</span></span>
    
      - <span data-ttu-id="db12c-156">Wenn Sie in **ausgewählte Features** einen einzelnen FQDN und eine IP-Adresse für den SIP-Zugriff, den Webkonferenzdienst und einen/V-Edgedienst verwenden möchten, geben Sie den externen FQDN in **SIP Access** ein.</span><span class="sxs-lookup"><span data-stu-id="db12c-156">If in **Select features** you chose to use a single FQDN and IP address for the SIP access, Web Conferencing service, and A/V Edge service, type the external FQDN in **SIP Access**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="db12c-157">Wenn Sie diese Option auswählen, müssen Sie für jeden Edgedienst eine andere Portnummer angeben (empfohlene Porteinstellungen: 5061 für Access-Edgedienst, 444 für Webkonferenz-Edgedienst und 443 für a/V-Edgedienst).</span><span class="sxs-lookup"><span data-stu-id="db12c-157">If you choose this option, you must specify a different port number for each of the edge services (recommended port settings: 5061 for Access Edge service, 444 for Web Conferencing Edge service, and 443 for A/V Edge service).</span></span> <span data-ttu-id="db12c-158">Wenn Sie diese Option auswählen, können Sie mögliche Verbindungsprobleme verhindern und die Konfiguration vereinfachen, da Sie dann dieselbe Portnummer (beispielsweise 443) für alle drei Dienste verwenden können.</span><span class="sxs-lookup"><span data-stu-id="db12c-158">Selecting this option can help prevent potential connectivity issues, and simplify the configuration because you can then use the same port number (for example, 443) for all three services.</span></span>

        
        </div>
    
      - <span data-ttu-id="db12c-159">Wenn Sie in **"Features auswählen"** nicht die Verwendung eines einzelnen FQDN und einer IP-Adresse gewählt haben, geben Sie die externen FQDNs für **SIP-Zugriff**, **Webkonferenz** und **Audiovideo** ein, wobei die Standardanschlüsse beizubehalten sind.</span><span class="sxs-lookup"><span data-stu-id="db12c-159">If in **Select features** you did not chose to use a single FQDN and IP Address, type the External FQDNs for **SIP Access**, **Web Conferencing** and **Audio Video**, keeping the default ports.</span></span>

9.  <span data-ttu-id="db12c-160">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-160">Click **Next**.</span></span>

10. <span data-ttu-id="db12c-161">Geben Sie unter interne **IP-Adresse definieren** die IP-Adresse Ihres Edge-Servers unter **interner IPv4-Adresse** und **interner IPv6** -Adresse ein, wie dies für Ihre Anforderungen angemessen ist.</span><span class="sxs-lookup"><span data-stu-id="db12c-161">In **Define the Internal IP address**, type the IP address of your Edge Server in **Internal IPv4 address** and **Internal IPv6 address** as is appropriate for your requirements.</span></span> <span data-ttu-id="db12c-162">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-162">Click **Next**.</span></span>

11. <span data-ttu-id="db12c-163">Gehen Sie unter **externe IP-Adresse definieren** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="db12c-163">In **Define the External IP address**, do the following:</span></span>
    
      - <span data-ttu-id="db12c-164">Wenn Sie sich für die Verwendung eines einzelnen FQDN und einer IP-Adresse für den SIP Access-, Webkonferenzdienst und a/V-Edgedienst entschieden haben, geben Sie die externe IPv4-Adresse des Edgeserver in **SIP Access** ein, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-164">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv4 address of the Edge Server in **SIP Access**, and then, click **Next**.</span></span>
    
      - <span data-ttu-id="db12c-165">Wenn Sie sich für die Verwendung von IPv6-Adressen entschieden haben, geben Sie die externe IPv6-Adresse des Edge-Servers in **SIP Access** ein, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-165">If you chose to use IPv6 addresses, type the external IPv6 address of the Edge Server in **SIP Access**, and then, click **Next**.</span></span>
    
      - <span data-ttu-id="db12c-166">Wenn Sie keinen einzelnen FQDN und keine IP-Adresse für den SIP Access-, Webkonferenzdienst und einen/v-Edgedienst verwendet haben, geben Sie die externen IPv4-Adressen des Edgeserver in **SIP Access**, **Web Conferencing** und **a/v Conferencing ein**, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-166">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv4 addresses of the Edge Server in **SIP Access**, **Web Conferencing**, and **A/V Conferencing**, and then click **Next**.</span></span>
    
      - <span data-ttu-id="db12c-167">Wenn Sie sich für die Verwendung von IPv6-Adressen entschieden haben und sich nicht für die Verwendung eines einzelnen FQDN und einer IP-Adresse für den SIP-Zugriff, den Webkonferenzdienst und den a/v-Edgedienst entschieden haben, geben Sie die externen IPv6-Adressen des Edgeserver in **SIP Access**, **Web Conferencing** und **a/v Conferencing ein**, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-167">If you chose to use IPv6 addresses and did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv6 addresses of the Edge Server in **SIP Access**, **Web Conferencing**, and **A/V Conferencing**, and then click **Next**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="db12c-168">Wenn Sie sich nicht für die Aktivierung und Zuweisung von IPv6-Adressierung entschieden haben, wird dieses Dialogfeld nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db12c-168">If you did not choose to enable and assign IPv6 addressing, you will not see this dialog box.</span></span>

        
        </div>

12. <span data-ttu-id="db12c-169">Wenn Sie sich für die Verwendung von NAT entschieden haben, wird ein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db12c-169">If you chose to use NAT, a dialog box appears.</span></span> <span data-ttu-id="db12c-170">Geben Sie unter **öffentliche IPv4-Adresse für den A/V-Edgedienst** die öffentliche IPv4-Adresse ein, die von NAT übersetzt werden soll, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-170">In **Public IPv4 address for the A/V Edge service**, type the public IPv4 address to be translated by NAT, and then click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="db12c-171">Dies sollte die externe IP-Adresse des A/V-Edgedienst sein.</span><span class="sxs-lookup"><span data-stu-id="db12c-171">This should be the external IP address of the A/V Edge service.</span></span>

    
    </div>

13. <span data-ttu-id="db12c-172">Wenn Sie sich für die Verwendung von NAT-und IPv6-Adressen entschieden haben, wird ein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db12c-172">If you chose to use NAT and IPv6 addresses, a dialog box appears.</span></span> <span data-ttu-id="db12c-173">Geben Sie in **der öffentlichen IPv6-Adresse für den A/V-Edgedienst** die öffentliche IPv6-Adresse ein, die von NAT übersetzt werden soll, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-173">In **Public IPv6 address for the A/V Edge service**, type the public IPv6 address to be translated by NAT, and then click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="db12c-174">Dies sollte die externe IP-Adresse des A/V-Edgedienst sein.</span><span class="sxs-lookup"><span data-stu-id="db12c-174">This should be the external IP address of the A/V Edge service.</span></span>

    
    </div>

14. <span data-ttu-id="db12c-175">Wählen Sie im Bereich "nächsten Hop **definieren**" im Pool für den **nächsten Hop** den Namen des internen Pools aus, der entweder ein Front-End-Pool oder ein Standard Edition-Pool sein kann.</span><span class="sxs-lookup"><span data-stu-id="db12c-175">In **Define the next hop**, in **Next hop pool**, select the name of the internal pool, which can be either a Front End pool or a Standard Edition pool.</span></span> <span data-ttu-id="db12c-176">Wenn Ihre Bereitstellung einen Director umfasst, wählen Sie den Director aus.</span><span class="sxs-lookup"><span data-stu-id="db12c-176">Or, if your deployment includes a Director, select the Director.</span></span> <span data-ttu-id="db12c-177">Klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-177">Then, click **Next**.</span></span>

15. <span data-ttu-id="db12c-178">Geben Sie in **Front-End-Pools zuordnen** einen oder mehrere interne Pools an, die Front-End-Pools und Standard Edition-Server enthalten können, um diesem Edgeserver zugeordnet zu werden, indem Sie die Namen der internen Pools auswählen, die diesen Edgeserver für die Kommunikation mit unterstützten externen Benutzern verwenden sollen.</span><span class="sxs-lookup"><span data-stu-id="db12c-178">In **Associate Front End pools**, specify one or more internal pools, which can include Front End pools and Standard Edition servers, to be associated with this Edge Server, by selecting the names of the internal pools that are to use this Edge Server for communication with supported external users.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="db12c-179">Jedem internen Pool für A/V-Datenverkehr kann nur ein Edge-Pool mit Lastenausgleich oder ein einzelner Edgeserver zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="db12c-179">Only one load-balanced Edge pool or single Edge Server can be associated with each internal pool for A/V traffic.</span></span> <span data-ttu-id="db12c-180">Wenn Sie bereits über einen internen Pool verfügen, der einem Edge-Pool oder Edgeserver zugeordnet ist, wird eine Warnung angezeigt, die besagt, dass dem internen Pool bereits ein Edge-Pool oder ein Edgeserver zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="db12c-180">If you already have an internal pool associated with an Edge pool or Edge Server, a warning appears indicating that the internal pool is already associated an Edge pool or Edge Server.</span></span> <span data-ttu-id="db12c-181">Wenn Sie einen Pool auswählen, der bereits einem anderen Edgeserver zugeordnet ist, wird die Zuordnung geändert.</span><span class="sxs-lookup"><span data-stu-id="db12c-181">If you select a pool that is already associated with another Edge Server, it will change the association.</span></span>

    
    </div>

16. <span data-ttu-id="db12c-182">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="db12c-182">Click **Finish**.</span></span>

17. <span data-ttu-id="db12c-183">Veröffentlichen Sie Ihre Topologie.</span><span class="sxs-lookup"><span data-stu-id="db12c-183">Publish your topology.</span></span>

</div>

<div>

## <a name="to-define-the-topology-for-a-dns-load-balanced-edge-server-pool"></a><span data-ttu-id="db12c-184">So definieren Sie die Topologie für einen DNS Load Balancing Edge-Server Pool</span><span class="sxs-lookup"><span data-stu-id="db12c-184">To define the topology for a DNS load balanced Edge Server pool</span></span>

1.  <span data-ttu-id="db12c-185">Starten Sie den Topologie-Generator: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server Topology Builder**.</span><span class="sxs-lookup"><span data-stu-id="db12c-185">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="db12c-186">Erweitern Sie in der Konsolenstruktur die Website, auf der Sie Edgeserver bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="db12c-186">In the console tree, expand the site in which you want to deploy Edge Servers.</span></span>

3.  <span data-ttu-id="db12c-187">Klicken Sie mit der rechten Maustaste auf **Edge-Pools**, und klicken Sie dann auf **neuer Edge-Pool**.</span><span class="sxs-lookup"><span data-stu-id="db12c-187">Right-click **Edge Pools**, and then click **New Edge Pool**.</span></span>

4.  <span data-ttu-id="db12c-188">Klicken Sie unter **neuen Edge-Pool definieren** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-188">In **Define the New Edge Pool**, click **Next**.</span></span>

5.  <span data-ttu-id="db12c-189">Gehen Sie unter **Definieren des FQDN des Edge-Pools** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="db12c-189">In **Define the Edge pool FQDN**, do the following:</span></span>
    
      - <span data-ttu-id="db12c-190">Geben Sie in **Pool FQDN** den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) für die interne Verbindung des Edge-Pools ein.</span><span class="sxs-lookup"><span data-stu-id="db12c-190">In **Pool FQDN**, type the fully qualified domain name (FQDN) for the internal connection of the Edge pool.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="db12c-191">Der Name, den Sie für den Pool angeben, muss der Name des internen Edge-Pools sein.</span><span class="sxs-lookup"><span data-stu-id="db12c-191">The name you specify for the pool must be the internal edge pool name.</span></span> <span data-ttu-id="db12c-192">Dieser muss als FQDN definiert werden.</span><span class="sxs-lookup"><span data-stu-id="db12c-192">This must be defined as a FQDN.</span></span> <span data-ttu-id="db12c-193">Der Topologie-Generator verwendet keine Kurznamen, sondern FQDNs.</span><span class="sxs-lookup"><span data-stu-id="db12c-193">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="db12c-194">Verwenden Sie nur Standardzeichen (also A – Z, a – z, 0 – 9 und Bindestriche) beim Zuweisen von FQDNs der Server mit Lync Server, Edgeserver und Pools.</span><span class="sxs-lookup"><span data-stu-id="db12c-194">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="db12c-195">Verwenden Sie keine Unicode-Zeichen oder Unterstriche.</span><span class="sxs-lookup"><span data-stu-id="db12c-195">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="db12c-196">Nicht standardmäßige Zeichen in einem FQDN werden häufig nicht von externen DNS-und öffentlichen CAS unterstützt (wenn der FQDN dem SN im Zertifikat zugewiesen werden muss).</span><span class="sxs-lookup"><span data-stu-id="db12c-196">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span>

        
        </div>
    
      - <span data-ttu-id="db12c-197">Klicken Sie auf **Pool mit mehreren Computern**, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-197">Click **Multiple computer pool**, and then click **Next**.</span></span>

6.  <span data-ttu-id="db12c-198">Gehen **Sie unter Features auswählen** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="db12c-198">In **Select features**, do the following:</span></span>
    
      - <span data-ttu-id="db12c-199">Wenn Sie einen einzelnen FQDN und eine IP-Adresse für den SIP Access, lync Server 2013 Web Conferencing Service und a/V Edge Services verwenden möchten, aktivieren Sie das Kontrollkästchen **einen einzelnen FQDN und eine IP-Adresse verwenden** .</span><span class="sxs-lookup"><span data-stu-id="db12c-199">If you plan to use a single FQDN and IP address for the SIP access, Lync Server 2013 Web Conferencing service and A/V Edge services, select the **Use a single FQDN and IP Address** check box.</span></span>
    
      - <span data-ttu-id="db12c-200">Wenn Sie beabsichtigen, die Föderation zu aktivieren, aktivieren Sie das Kontrollkästchen **Föderation für diesen Edge-Pool aktivieren (Port 5061)** .</span><span class="sxs-lookup"><span data-stu-id="db12c-200">If you plan to enable federation, select the **Enable federation for this Edge pool (Port 5061)** check box.</span></span> <span data-ttu-id="db12c-201">Klicken Sie auf **weiter** .</span><span class="sxs-lookup"><span data-stu-id="db12c-201">Click **Next**</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="db12c-202">Sie können diese Option auswählen, aber nur ein Edge-Pool oder Edgeserver in Ihrer Organisation kann extern für den Verbund veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="db12c-202">You can select this option, but only one Edge pool or Edge Server in your organization can be published externally for federation.</span></span> <span data-ttu-id="db12c-203">Der gesamte Zugriff von Verbundbenutzern, einschließlich öffentlicher Chat-Benutzer, durchlaufen denselben Edge-Pool oder Single Edge-Server.</span><span class="sxs-lookup"><span data-stu-id="db12c-203">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="db12c-204">Wenn Ihre Bereitstellung beispielsweise je einen Edgepool oder einzelnen Edgeserver in New York und in London umfasst und Sie die Unterstützung des Partnerverbunds für den Edgepool oder den einzelnen Edgeserver in New York aktivieren, erfolgt der Signaldatenverkehr für Partnerbenutzer über den Edgepool oder den einzelnen Edgeserver in New York.</span><span class="sxs-lookup"><span data-stu-id="db12c-204">For instance, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="db12c-205">Dies gilt auch für die Kommunikation mit Benutzern in London, wenngleich ein interner Benutzer in London, der einen Partnerbenutzer in London anruft, für den A/V-Datenverkehr den Pool oder Edgeserver in London verwendet.</span><span class="sxs-lookup"><span data-stu-id="db12c-205">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

        
        </div>
    
      - <span data-ttu-id="db12c-206">Wenn Sie beabsichtigen, das Extensible Messaging and Presence Protocol (XMPP) für Ihre Bereitstellung zu unterstützen, aktivieren Sie das Kontrollkästchen **XMPP-Föderation aktivieren (Port 5269)** .</span><span class="sxs-lookup"><span data-stu-id="db12c-206">If you plan to support the extensible messaging and presence protocol (XMPP) for your deployment, select the **Enable XMPP federation (port 5269)** check box</span></span>

7.  <span data-ttu-id="db12c-207">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-207">Click **Next**.</span></span>

8.  <span data-ttu-id="db12c-208">Gehen **Sie unter IP-Optionen auswählen** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="db12c-208">In **Select IP Options**, do the following:</span></span>
    
      - <span data-ttu-id="db12c-209">**Aktivieren von IPv4 auf interner Schnittstelle**: Aktivieren Sie das Kontrollkästchen, wenn Sie eine IPv4-Adresse auf die interne Schnittstelle des Edge-Servers oder des Edge-Pools anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="db12c-209">**Enable IPv4 on internal interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="db12c-210">**Aktivieren von IPv6 auf interner Schnittstelle**: Aktivieren Sie das Kontrollkästchen, wenn Sie eine IPv6-Adresse auf die interne Schnittstelle des Edge-Servers oder des Edge-Pools anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="db12c-210">**Enable IPv6 on internal interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="db12c-211">**Aktivieren von IPv4 auf externer Schnittstelle**: Aktivieren Sie das Kontrollkästchen, wenn Sie eine IPv4-Adresse auf die externe Schnittstelle des Edge-Servers oder des Edge-Pools anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="db12c-211">**Enable IPv4 on external interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool external interface</span></span>
    
      - <span data-ttu-id="db12c-212">**Aktivieren von IPv6 auf einer externen Schnittstelle**: Aktivieren Sie das Kontrollkästchen, wenn Sie eine IPv6-Adresse auf die externe Schnittstelle des Edge-Servers oder des Edge-Pools anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="db12c-212">**Enable IPv6 on external interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool external interface</span></span>
    
    <span data-ttu-id="db12c-213">Sie können auch den Edgeserver oder den Edge-Pool so konfigurieren, dass für die externen IP-Adressen eine Adresse für die Netzwerkadressübersetzung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db12c-213">You can also configure the Edge Server or Edge pool to use a network address translation address for the external IP addresses.</span></span> <span data-ttu-id="db12c-214">Aktivieren Sie dazu das Kontrollkästchen, um **die externe IP-Adresse dieses Edge-Pools von NAT zu übersetzen**.</span><span class="sxs-lookup"><span data-stu-id="db12c-214">You do this by selecting the check box **The external IP address of this Edge pool is translated by NAT**.</span></span>

9.  <span data-ttu-id="db12c-215">Führen Sie in **externen FQDNs** die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="db12c-215">In **External FQDNs**, do the following:</span></span>
    
      - <span data-ttu-id="db12c-216">Wenn Sie in **ausgewählte Features** einen einzelnen FQDN und eine IP-Adresse für den SIP-Zugriff, den Webkonferenzdienst und einen/V-Edgedienst verwenden möchten, geben Sie den externen FQDN in **SIP Access** ein.</span><span class="sxs-lookup"><span data-stu-id="db12c-216">If in **Select features** you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external FQDN in **SIP Access**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="db12c-217">Wenn Sie diese Option auswählen, müssen Sie für jeden Edgedienst eine andere Portnummer angeben (empfohlene Porteinstellungen: 5061 für Access-Edgedienst, 444 für Webkonferenz-Edgedienst und 443 für a/V-Edgedienst).</span><span class="sxs-lookup"><span data-stu-id="db12c-217">If you choose this option, you must specify a different port number for each of the Edge services (recommended port settings: 5061 for Access Edge service, 444 for Web Conferencing Edge service, and 443 for A/V Edge service).</span></span> <span data-ttu-id="db12c-218">Wenn Sie diese Option auswählen, können Sie mögliche Verbindungsprobleme verhindern und die Konfiguration vereinfachen, da Sie dann dieselbe Portnummer (beispielsweise 443) für alle drei Dienste verwenden können.</span><span class="sxs-lookup"><span data-stu-id="db12c-218">By selecting this option, you can help prevent potential connectivity issues and simplify the configuration because you can then use the same port number (for example, 443) for all three services.</span></span>

        
        </div>
    
      - <span data-ttu-id="db12c-219">Wenn Sie in **"Features auswählen"** nicht die Verwendung eines einzelnen FQDN und einer IP-Adresse gewählt haben, geben Sie den FQDN ein, den Sie für die öffentliche Seite des Edge-Pools für den **SIP-Zugriff** ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-219">If in **Select features** you did not chose to use a single FQDN and IP Address, type the FQDN that you have chosen for your public facing side of the edge pool for in **SIP Access**.</span></span> <span data-ttu-id="db12c-220">Geben Sie in **Webkonferenzen** den FQDN ein, den Sie für die öffentlich zugängliche Seite des Edge-Pools ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-220">In **Web Conferencing**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="db12c-221">Geben Sie in **Audio/Video** den FQDN ein, den Sie für die öffentliche Seite des Edge-Pools ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-221">In **Audio/Video**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="db12c-222">Verwenden Sie die Standardanschlüsse.</span><span class="sxs-lookup"><span data-stu-id="db12c-222">Use the default ports.</span></span>

10. <span data-ttu-id="db12c-223">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-223">Click **Next**.</span></span>

11. <span data-ttu-id="db12c-224">Klicken Sie unter **Computer in diesem Pool definieren** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="db12c-224">In **Define the computers in this pool**, click **Add**.</span></span>

12. <span data-ttu-id="db12c-225">Gehen Sie unter **Interner FQDN und IP-Adresse** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="db12c-225">In **Internal FQDN and IP address**, do the following:</span></span>
    
      - <span data-ttu-id="db12c-226">Geben Sie unter **interne IPv4-Adresse** die IPv4-Adresse und die **interne IPv6-Adresse** ein, die für Ihre Anforderungen für den ersten Edgeserver, den Sie in diesem Pool erstellen möchten, geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="db12c-226">In **Internal IPv4 address**, type the IPv4 address and **Internal IPv6 address** as is appropriate for your requirements for the first Edge Server that you want to create in this pool.</span></span>
    
      - <span data-ttu-id="db12c-227">Geben Sie im **internen FQDN** den FQDN des ersten Edge-Servers ein, den Sie in diesem Pool erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="db12c-227">In **Internal FQDN**, type the FQDN of the first Edge Server that you want to create in this pool.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="db12c-228">Der angegebene Name muss mit dem auf dem Server konfigurierten Computernamen übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="db12c-228">The name you specify must be identical to the computer name configured on the server.</span></span> <span data-ttu-id="db12c-229">Der Name eines Computers, der nicht Mitglied einer Domäne ist, ist standardmäßig kein FQDN, sondern ein Kurzname.</span><span class="sxs-lookup"><span data-stu-id="db12c-229">By default, the computer name of a computer that is not joined to a domain is a short name, not an FQDN.</span></span> <span data-ttu-id="db12c-230">Der Topologie-Generator verwendet keine Kurznamen, sondern FQDNs.</span><span class="sxs-lookup"><span data-stu-id="db12c-230">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="db12c-231">Daher müssen Sie ein DNS-Suffix für den Namen des Computers konfigurieren, der als Edgeserver bereitgestellt werden soll und nicht Mitglied einer Domäne ist.</span><span class="sxs-lookup"><span data-stu-id="db12c-231">So, you must configure a DNS suffix on the name of the computer to be deployed as an Edge Server that is not joined to a domain.</span></span> <span data-ttu-id="db12c-232">Verwenden Sie beim Zuweisen von FQDNs ihrer lync-Server,-Edgeserver,-Pools und-Arrays nur Standardzeichen (einschließlich a – z, a – z, 0 – 9 und Bindestriche).</span><span class="sxs-lookup"><span data-stu-id="db12c-232">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, pools, and arrays.</span></span> <span data-ttu-id="db12c-233">Verwenden Sie keine Unicode-Zeichen oder Unterstriche.</span><span class="sxs-lookup"><span data-stu-id="db12c-233">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="db12c-234">Nicht standardmäßige Zeichen in einem FQDN werden häufig nicht von externen DNS-und öffentlichen CAS unterstützt (wenn der FQDN dem SN im Zertifikat zugewiesen werden muss).</span><span class="sxs-lookup"><span data-stu-id="db12c-234">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span> <span data-ttu-id="db12c-235">Details zum Hinzufügen eines DNS-Suffix zu einem Computernamen finden Sie unter <A href="lync-server-2013-configure-dns-for-edge-support.md">Konfigurieren von DNS für die Edge-Unterstützung in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="db12c-235">For details about adding a DNS suffix to a computer name, see <A href="lync-server-2013-configure-dns-for-edge-support.md">Configure DNS for edge support in Lync Server 2013</A>.</span></span>

        
        </div>

13. <span data-ttu-id="db12c-236">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-236">Click **Next**.</span></span>

14. <span data-ttu-id="db12c-237">Gehen Sie unter **externe IP-Adressen definieren** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="db12c-237">In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="db12c-238">Wenn Sie sich für die Verwendung eines einzelnen FQDN und einer IP-Adresse für den SIP Access-, Webkonferenz-und a/V-Edgedienst entschieden haben, geben Sie die externe IP-Adresse des Edgeserver in **SIP Access** ein.</span><span class="sxs-lookup"><span data-stu-id="db12c-238">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IP address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="db12c-239">Wenn Sie nicht entschieden haben, einen einzelnen FQDN und eine IP-Adresse für den SIP Access-, Webkonferenz-und a/V-Konferenzdienst zu verwenden, geben Sie die IP-Adresse ein, die Sie für die öffentliche Seite des Edge-Pool-Servers für den **SIP-Zugriff** ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-239">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IP address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="db12c-240">Geben Sie in **Webkonferenzen** die IP-Adresse ein, die Sie für die öffentliche Seite des Edge-Pool-Servers gewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-240">In **Web Conferencing**, type the IP address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="db12c-241">Geben Sie in **A/V-Konferenzen** die IP-Adresse ein, die Sie für die öffentliche Seite des Edge-Pool-Servers gewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-241">In **A/V Conferencing**, type the IP address you have chosen for your public facing side of this Edge pool server.</span></span>

15. <span data-ttu-id="db12c-242">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-242">Click **Next**.</span></span>

16. <span data-ttu-id="db12c-243">Wenn Sie sich für die Aktivierung von IPv6-Adressen entschieden haben, gehen Sie unter **definieren externer IP-Adressen** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="db12c-243">If you chose to enable IPv6 addresses, In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="db12c-244">Wenn Sie sich für die Verwendung eines einzelnen FQDN und einer IP-Adresse für den SIP Access-, Webkonferenz-und a/V-Edgedienst entschieden haben, geben Sie die externe IPv6-Adresse des Edgeserver in **SIP Access** ein.</span><span class="sxs-lookup"><span data-stu-id="db12c-244">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv6 address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="db12c-245">Wenn Sie nicht entschieden haben, einen einzelnen FQDN und eine IP-Adresse für den SIP Access-, Webkonferenz-und a/V-Konferenzdienst zu verwenden, geben Sie die IPv6-Adresse ein, die Sie für die öffentliche Seite des Edge-Pool-Servers für den **SIP-Zugriff** ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-245">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IPv6 address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="db12c-246">Geben Sie in **Webkonferenzen** die IPv6-Adresse ein, die Sie für die öffentliche Seite des Edge-Pool-Servers gewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-246">In **Web Conferencing**, type the IPv6 address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="db12c-247">Geben Sie in **A/V-Konferenzen** die IPv6-Adresse ein, die Sie für die öffentliche Seite des Edge-Pool-Servers gewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-247">In **A/V Conferencing**, type the IPv6 address you have chosen for your public facing side of this Edge pool server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="db12c-248">Wenn Sie sich nicht für die Aktivierung und Zuweisung von IPv6-Adressierung entschieden haben, wird dieses Dialogfeld nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db12c-248">If you did not choose to enable and assign IPv6 addressing, you will not see this dialog box.</span></span>

    
    </div>

17. <span data-ttu-id="db12c-249">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="db12c-249">Click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="db12c-250">Der erste Edge-Server, den Sie in Ihrem Pool erstellt haben, wird nun im Dialogfeld <STRONG>Computer in diesem Pool definieren</STRONG> angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db12c-250">You will now see the first Edge Server you created in your pool in the <STRONG>Define the computers in this pool</STRONG> dialog box.</span></span>

    
    </div>

18. <span data-ttu-id="db12c-251">Klicken Sie unter **Computer in diesem Pool definieren** auf **Hinzufügen**, und wiederholen Sie dann die Schritte 11 bis 14 für den zweiten Edgeserver, den Sie dem Edge-Pool hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="db12c-251">In **Define the computers in this pool**, click **Add**, and then repeat steps 11 through 14 for the second Edge Server that you want to add to you Edge pool.</span></span>

19. <span data-ttu-id="db12c-252">Nachdem Sie die Schritte 11 bis 14 wiederholt haben, klicken Sie unter **Definieren der Computer in diesem Pool** auf **weiter** .</span><span class="sxs-lookup"><span data-stu-id="db12c-252">After you repeat steps 11 through 14, click **Next** in **Define the computers in this pool**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="db12c-253">An dieser Stelle können Sie die beiden Edgeserver in Ihrem Pool sehen.</span><span class="sxs-lookup"><span data-stu-id="db12c-253">At this point, you can see both of the Edge Servers in your pool.</span></span>

    
    </div>

20. <span data-ttu-id="db12c-254">Wenn Sie sich für die Verwendung von NAT entschieden haben, wird ein Dialogfeld angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db12c-254">If you chose to use NAT, a dialog box appears.</span></span> <span data-ttu-id="db12c-255">Geben Sie unter **öffentliche IP-Adresse** die öffentlichen IPv4-und IPv6-Adressen (sofern erforderlich) ein, die von NAT übersetzt werden sollen, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-255">In **Public IP address**, type the public IPv4 and IPv6 (as appropriate) addresses to be translated by NAT, and then click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="db12c-256">Dies sollte die externe IP-Adresse der A/V-Kante sein.</span><span class="sxs-lookup"><span data-stu-id="db12c-256">This should be the external IP Address of the A/V Edge.</span></span>

    
    </div>

21. <span data-ttu-id="db12c-257">Wählen Sie im **Feld nächsten Hop definieren** in der Liste **Nächster Hop-Pool** den Namen des internen Pools aus, der entweder ein Front-End-Pool oder ein Standard Edition-Pool sein kann.</span><span class="sxs-lookup"><span data-stu-id="db12c-257">In **Define the next hop**, in the **Next hop pool** list, select the name of the internal pool, which can be either a Front End pool or a Standard Edition pool.</span></span> <span data-ttu-id="db12c-258">Wenn Ihre Bereitstellung einen Director umfasst, wählen Sie den Namen des Directors aus.</span><span class="sxs-lookup"><span data-stu-id="db12c-258">Or, if your deployment includes a Director, select the name of the Director.</span></span> <span data-ttu-id="db12c-259">Klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-259">Then, click **Next**.</span></span>

22. <span data-ttu-id="db12c-260">Geben Sie in **Front-End-Pools zuordnen** einen oder mehrere interne Pools an, die Front-End-Pools und Standard Edition-Server enthalten können, die diesem Edgeserver zugeordnet werden sollen, indem Sie die Namen der internen Pools auswählen, die diesen Edgeserver für die Kommunikation mit unterstützten externen Benutzern verwenden sollen.</span><span class="sxs-lookup"><span data-stu-id="db12c-260">In **Associate Front End pools**, specify one or more internal pools, which can include Front End pools and Standard Edition servers, to be associated with this Edge Server, by selecting the names of the internal pool(s) that is to use this Edge Server for communication with supported external users.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="db12c-261">Jedem internen Pool für A/V-Datenverkehr kann nur ein Edge-Pool mit Lastenausgleich oder ein einzelner Edgeserver zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="db12c-261">Only one load-balanced Edge pool or single Edge Server can be associated with each internal pool for A/V traffic.</span></span> <span data-ttu-id="db12c-262">Wenn Sie bereits über einen internen Pool verfügen, der einem Edge-Pool oder Edgeserver zugeordnet ist, wird eine Warnung angezeigt, die besagt, dass dem internen Pool bereits ein Edge-Pool oder ein Edgeserver zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="db12c-262">If you already have an internal pool associated with an Edge pool or Edge Server, a warning appears indicating that the internal pool is already associated an Edge pool or Edge Server.</span></span> <span data-ttu-id="db12c-263">Wenn Sie einen Pool auswählen, der bereits einem anderen Edgeserver zugeordnet ist, wird die Zuordnung geändert.</span><span class="sxs-lookup"><span data-stu-id="db12c-263">If you select a pool that is already associated with another Edge Server, it will change the association.</span></span>

    
    </div>

23. <span data-ttu-id="db12c-264">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="db12c-264">Click **Finish**.</span></span>

24. <span data-ttu-id="db12c-265">Veröffentlichen Sie Ihre Topologie.</span><span class="sxs-lookup"><span data-stu-id="db12c-265">Publish your topology.</span></span>

</div>

<div>

## <a name="to-define-the-topology-for-a-hardware-load-balanced-edge-server-pool"></a><span data-ttu-id="db12c-266">So definieren Sie die Topologie für einen Hardwarelastenausgleich-Edgeserver-Pool</span><span class="sxs-lookup"><span data-stu-id="db12c-266">To define the topology for a hardware load balanced Edge Server pool</span></span>

1.  <span data-ttu-id="db12c-267">Starten Sie den Topologie-Generator: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server Topology Builder**.</span><span class="sxs-lookup"><span data-stu-id="db12c-267">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="db12c-268">Erweitern Sie in der Konsolenstruktur die Website, auf der Sie Edgeserver bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="db12c-268">In the console tree, expand the site in which you want to deploy Edge Servers.</span></span>

3.  <span data-ttu-id="db12c-269">Klicken Sie mit der rechten Maustaste auf **Edge-Pools**, und wählen Sie dann **neuer Edge-Pool** aus.</span><span class="sxs-lookup"><span data-stu-id="db12c-269">Right-click **Edge Pools**, and then select **New Edge Pool**.</span></span>

4.  <span data-ttu-id="db12c-270">Klicken Sie unter **neuen Edge-Pool definieren** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-270">In **Define the New Edge Pool**, click **Next**.</span></span>

5.  <span data-ttu-id="db12c-271">Gehen Sie unter **Definieren des FQDN des Edge-Pools** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="db12c-271">In **Define the Edge pool FQDN**, do the following:</span></span>
    
      - <span data-ttu-id="db12c-272">Geben Sie in **FQDN** den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) ein, den Sie für die interne Seite des Edge-Pools ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-272">In **FQDN**, type the fully qualified domain name (FQDN) you have chosen for the internal side of the Edge pool.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="db12c-273">Der Name, den Sie für den Pool angeben, muss der Name des internen Edge-Pools sein.</span><span class="sxs-lookup"><span data-stu-id="db12c-273">The name you specify for the pool must be the internal edge pool name.</span></span> <span data-ttu-id="db12c-274">Dieser muss als FQDN definiert werden.</span><span class="sxs-lookup"><span data-stu-id="db12c-274">This must be defined as a FQDN.</span></span> <span data-ttu-id="db12c-275">Der Topologie-Generator verwendet keine Kurznamen, sondern FQDNs.</span><span class="sxs-lookup"><span data-stu-id="db12c-275">Topology Builder uses FQDNs, not short names.</span></span> <span data-ttu-id="db12c-276">Verwenden Sie nur Standardzeichen (also A – Z, a – z, 0 – 9 und Bindestriche) beim Zuweisen von FQDNs der Server mit Lync Server, Edgeserver und Pools.</span><span class="sxs-lookup"><span data-stu-id="db12c-276">Use only standard characters (including A–Z, a–z, 0–9, and hyphens) when assigning FQDNs of your Lync Servers, Edge Servers, and pools.</span></span> <span data-ttu-id="db12c-277">Verwenden Sie keine Unicode-Zeichen oder Unterstriche.</span><span class="sxs-lookup"><span data-stu-id="db12c-277">Do not use Unicode characters or underscores.</span></span> <span data-ttu-id="db12c-278">Nicht standardmäßige Zeichen in einem FQDN werden häufig nicht von externen DNS-und öffentlichen CAS unterstützt (wenn der FQDN dem SN im Zertifikat zugewiesen werden muss).</span><span class="sxs-lookup"><span data-stu-id="db12c-278">Nonstandard characters in an FQDN are often not supported by external DNS and public CAs (when the FQDN must be assigned to the SN in the certificate).</span></span>

        
        </div>
    
    <!-- end list -->
    
      - <span data-ttu-id="db12c-279">Klicken Sie auf **Pool für mehrere Computer** und dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-279">Click **Multiple computer pool**, and then **Next**.</span></span>

6.  <span data-ttu-id="db12c-280">Gehen **Sie unter Features auswählen** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="db12c-280">In **Select features** do the following:</span></span>
    
      - <span data-ttu-id="db12c-281">Wenn Sie einen einzelnen FQDN und eine IP-Adresse für den SIP-Zugriffsdienst, den lync Server-Webkonferenzdienst und den a/V-Edgedienst verwenden möchten, aktivieren Sie das Kontrollkästchen **einen einzelnen FQDN & IP-Adresse verwenden** .</span><span class="sxs-lookup"><span data-stu-id="db12c-281">If you plan to use a single FQDN and IP address for the SIP access service, Lync Server Web Conferencing service, and A/V Edge service, select the **Use a single FQDN & IP Address** check box.</span></span>
    
      - <span data-ttu-id="db12c-282">Wenn Sie beabsichtigen, die Föderation zu aktivieren, aktivieren Sie das Kontrollkästchen **Föderation für diesen Edge-Pool aktivieren (Port 5061)** .</span><span class="sxs-lookup"><span data-stu-id="db12c-282">If you plan to enable federation, select the **Enable federation for this Edge pool (Port 5061)** check box.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="db12c-283">Sie können diese Option auswählen, es kann jedoch nur ein Edge-Pool oder ein Edgeserver in Ihrer Organisation extern für den Verbund veröffentlicht werden.</span><span class="sxs-lookup"><span data-stu-id="db12c-283">You can select this option, but only one Edge pool or Edge Server in your organization may be published externally for federation.</span></span> <span data-ttu-id="db12c-284">Der gesamte Zugriff von Verbundbenutzern, einschließlich öffentlicher Chat-Benutzer, durchlaufen denselben Edge-Pool oder Single Edge-Server.</span><span class="sxs-lookup"><span data-stu-id="db12c-284">All access by federated users, including public instant messaging (IM) users, go through the same Edge pool or single Edge Server.</span></span> <span data-ttu-id="db12c-285">Wenn Ihre Bereitstellung beispielsweise je einen Edgepool oder einzelnen Edgeserver in New York und in London umfasst und Sie die Unterstützung des Partnerverbunds für den Edgepool oder den einzelnen Edgeserver in New York aktivieren, erfolgt der Signaldatenverkehr für Partnerbenutzer über den Edgepool oder den einzelnen Edgeserver in New York.</span><span class="sxs-lookup"><span data-stu-id="db12c-285">For instance, if your deployment includes an Edge pool or single Edge Server deployed in New York and one deployed in London and you enable federation support on the New York Edge pool or single Edge Server, signal traffic for federated users will go through the New York Edge pool or single Edge Server.</span></span> <span data-ttu-id="db12c-286">Dies gilt auch für die Kommunikation mit Benutzern in London, wenngleich ein interner Benutzer in London, der einen Partnerbenutzer in London anruft, für den A/V-Datenverkehr den Pool oder Edgeserver in London verwendet.</span><span class="sxs-lookup"><span data-stu-id="db12c-286">This is true even for communications with London users, although a London internal user calling a London federated user uses the London pool or Edge Server for A/V traffic.</span></span>

        
        </div>
    
      - <span data-ttu-id="db12c-287">Wenn Sie beabsichtigen, das Extensible Messaging and Presence Protocol (XMPP) für Ihre Bereitstellung zu unterstützen, aktivieren Sie das Kontrollkästchen **XMPP-Föderation aktivieren (Port 5269)** .</span><span class="sxs-lookup"><span data-stu-id="db12c-287">If you plan to support the extensible messaging and presence protocol (XMPP) for your deployment, select the **Enable XMPP federation (port 5269)** check box</span></span>

7.  <span data-ttu-id="db12c-288">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-288">Click **Next**.</span></span>

8.  <span data-ttu-id="db12c-289">Gehen **Sie unter IP-Optionen auswählen** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="db12c-289">In **Select IP Options**, do the following:</span></span>
    
      - <span data-ttu-id="db12c-290">**Aktivieren von IPv4 auf interner Schnittstelle**: Aktivieren Sie das Kontrollkästchen, wenn Sie eine IPv4-Adresse auf die interne Schnittstelle des Edge-Servers oder des Edge-Pools anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="db12c-290">**Enable IPv4 on internal interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="db12c-291">**Aktivieren von IPv6 auf interner Schnittstelle**: Aktivieren Sie das Kontrollkästchen, wenn Sie eine IPv6-Adresse auf die interne Schnittstelle des Edge-Servers oder des Edge-Pools anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="db12c-291">**Enable IPv6 on internal interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool internal interface</span></span>
    
      - <span data-ttu-id="db12c-292">**Aktivieren von IPv4 auf externer Schnittstelle**: Aktivieren Sie das Kontrollkästchen, wenn Sie eine IPv4-Adresse auf die externe Schnittstelle des Edge-Servers oder des Edge-Pools anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="db12c-292">**Enable IPv4 on external interface**: Select the check box if you want to apply an IPv4 address to the Edge Server or Edge pool external interface</span></span>
    
      - <span data-ttu-id="db12c-293">**Aktivieren von IPv6 auf einer externen Schnittstelle**: Aktivieren Sie das Kontrollkästchen, wenn Sie eine IPv6-Adresse auf die externe Schnittstelle des Edge-Servers oder des Edge-Pools anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="db12c-293">**Enable IPv6 on external interface**: Select the check box if you want to apply an IPv6 address to the Edge Server or Edge pool external interface</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="db12c-294">Aktivieren Sie <STRONG>nicht</STRONG> das Kontrollkästchen <STRONG>externe IP-Adresse des Edge-Pools, der von NAT übersetzt wird</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="db12c-294"><STRONG>Do Not</STRONG> select the <STRONG>The external IP address of the Edge pool is translated by NAT</STRONG> check box.</span></span> <span data-ttu-id="db12c-295">Netzwerkadressübersetzung (Network Address Translation, NAT) wird nicht unterstützt, wenn Sie den Hardwarelastenausgleich verwenden.</span><span class="sxs-lookup"><span data-stu-id="db12c-295">Network address translation (NAT) is not supported when you are using hardware load balancing.</span></span>

    
    </div>

9.  <span data-ttu-id="db12c-296">Führen Sie in **externen FQDNs** die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="db12c-296">In **External FQDNs**, do the following:</span></span>
    
      - <span data-ttu-id="db12c-297">Wenn Sie in **ausgewählte Features** einen einzelnen FQDN und eine IP-Adresse für den SIP-Zugriff, den Webkonferenzdienst und einen/V-Edgedienst verwenden möchten, geben Sie den externen FQDN in **SIP Access** ein.</span><span class="sxs-lookup"><span data-stu-id="db12c-297">If in **Select features** you chose to use a single FQDN and IP address for the SIP access, Web Conferencing service, and A/V Edge service, type the external FQDN in **SIP Access**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="db12c-298">Wenn Sie diese Option auswählen, müssen Sie für jeden Edgedienst eine andere Portnummer angeben (empfohlene Porteinstellungen: 5061 für Access-Edgedienst, 444 für Webkonferenz-Edgedienst und 443 für a/V-Edgedienst).</span><span class="sxs-lookup"><span data-stu-id="db12c-298">If you choose to select this option, you must specify a different port number for each of the Edge services (recommended port settings: 5061 for Access Edge service, 444 for Web Conferencing Edge service, and 443 for A/V Edge service).</span></span> <span data-ttu-id="db12c-299">Wenn Sie diese Option auswählen, können Sie mögliche Verbindungsprobleme verhindern und die Konfiguration vereinfachen, da Sie dann dieselbe Portnummer (beispielsweise 443) für alle drei Dienste verwenden können.</span><span class="sxs-lookup"><span data-stu-id="db12c-299">By selecting this option, you can help prevent potential connectivity issues and simplify the configuration because you can then use the same port number (for example, 443) for all three services.</span></span>

        
        </div>
    
      - <span data-ttu-id="db12c-300">Wenn Sie in **"Features auswählen"** nicht die Verwendung eines einzelnen FQDN und einer IP-Adresse gewählt haben, geben Sie den FQDN ein, den Sie für die öffentliche Seite des Edge-Pools für den **SIP-Zugriff** ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-300">If in **Select features** you did not chose to use a single FQDN and IP address, type the FQDN that you have chosen for your public facing side of the edge pool for in **SIP Access**.</span></span> <span data-ttu-id="db12c-301">Geben Sie in **Webkonferenzen** den FQDN ein, den Sie für die öffentlich zugängliche Seite des Edge-Pools ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-301">In **Web Conferencing**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="db12c-302">Geben Sie in **Audio/Video** den FQDN ein, den Sie für die öffentliche Seite des Edge-Pools ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-302">In **Audio/Video**, type the FQDN you have chosen for your public facing side of the Edge pool.</span></span> <span data-ttu-id="db12c-303">Verwenden Sie die Standardanschlüsse.</span><span class="sxs-lookup"><span data-stu-id="db12c-303">Use the default ports.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="db12c-304">Hierbei handelt es sich um die öffentlich zugänglichen VIP-FQDNs (Virtual IP) für den Pool.</span><span class="sxs-lookup"><span data-stu-id="db12c-304">These will be the publicly facing virtual IP (VIP) FQDNs for the pool.</span></span>

        
        </div>

10. <span data-ttu-id="db12c-305">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-305">Click **Next**.</span></span>

11. <span data-ttu-id="db12c-306">Klicken Sie unter **Computer in diesem Pool definieren** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="db12c-306">In **Define the computers in this pool**, click **Add**.</span></span>

12. <span data-ttu-id="db12c-307">Gehen Sie unter **externe IP-Adressen definieren** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="db12c-307">In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="db12c-308">Wenn Sie sich für die Verwendung eines einzelnen FQDN und einer IP-Adresse für den SIP Access-, Webkonferenzdienst und a/V-Edgedienst entschieden haben, geben Sie die externe IPv4-Adresse des Edgeserver in **SIP Access** ein. externe IP-Adresse des Edge-Servers in **SIP Access**.</span><span class="sxs-lookup"><span data-stu-id="db12c-308">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv4 address of the Edge Server in **SIP Access**.external IP address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="db12c-309">Wenn Sie nicht entschieden haben, einen einzelnen FQDN und eine IP-Adresse für den SIP Access-, Webkonferenz-und a/V-Konferenzdienst zu verwenden, geben Sie die IP-Adresse ein, die Sie für die öffentliche Seite des Edge-Pool-Servers für den **SIP-Zugriff** ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-309">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IP address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="db12c-310">Geben Sie in **Webkonferenzen** die IP-Adresse ein, die Sie für die öffentliche Seite des Edge-Pool-Servers gewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-310">In **Web Conferencing**, type the IP address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="db12c-311">Geben Sie in **A/V-Konferenzen** die IP-Adresse ein, die Sie für die öffentliche Seite des Edge-Pool-Servers gewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-311">In **A/V Conferencing**, type the IP address you have chosen for your public facing side of this Edge pool server.</span></span>

13. <span data-ttu-id="db12c-312">Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-312">Click **Next**.</span></span>

14. <span data-ttu-id="db12c-313">Wenn Sie sich für die Aktivierung von IPv6-Adressen entschieden haben, gehen Sie unter **definieren externer IP-Adressen** wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="db12c-313">If you chose to enable IPv6 addresses, In **Define the external IP addresses**, do the following:</span></span>
    
      - <span data-ttu-id="db12c-314">Wenn Sie sich für die Verwendung eines einzelnen FQDN und einer IP-Adresse für den SIP Access-, Webkonferenz-und a/V-Edgedienst entschieden haben, geben Sie die externe IPv6-Adresse des Edgeserver in **SIP Access** ein.</span><span class="sxs-lookup"><span data-stu-id="db12c-314">If you chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Edge service, type the external IPv6 address of the Edge Server in **SIP Access**.</span></span>
    
      - <span data-ttu-id="db12c-315">Wenn Sie nicht entschieden haben, einen einzelnen FQDN und eine IP-Adresse für den SIP Access-, Webkonferenz-und a/V-Konferenzdienst zu verwenden, geben Sie die IPv6-Adresse ein, die Sie für die öffentliche Seite des Edge-Pool-Servers für den **SIP-Zugriff** ausgewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-315">If you did not chose to use a single FQDN and IP Address for the SIP access, Web Conferencing service, and A/V Conferencing service, type the IPv6 address that you have chosen for your public facing side of this Edge pool server for **SIP Access**.</span></span> <span data-ttu-id="db12c-316">Geben Sie in **Webkonferenzen** die IPv6-Adresse ein, die Sie für die öffentliche Seite des Edge-Pool-Servers gewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-316">In **Web Conferencing**, type the IPv6 address that you have chosen for your public facing side of this Edge pool server.</span></span> <span data-ttu-id="db12c-317">Geben Sie in **A/V-Konferenzen** die IPv6-Adresse ein, die Sie für die öffentliche Seite des Edge-Pool-Servers gewählt haben.</span><span class="sxs-lookup"><span data-stu-id="db12c-317">In **A/V Conferencing**, type the IPv6 address you have chosen for your public facing side of this Edge pool server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="db12c-318">Wenn Sie sich nicht für die Aktivierung und Zuweisung von IPv6-Adressierung entschieden haben, wird dieses Dialogfeld nicht angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db12c-318">If you did not choose to enable and assign IPv6 addressing, you will not see this dialog box.</span></span>

    
    </div>

15. <span data-ttu-id="db12c-319">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="db12c-319">Click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="db12c-320">Der erste Edge-Server, den Sie in Ihrem Pool erstellt haben, wird nun im Dialogfeld <STRONG>Computer in diesem Pool definieren</STRONG> angezeigt.</span><span class="sxs-lookup"><span data-stu-id="db12c-320">You will now see the first Edge Server you created in your pool in the <STRONG>Define the computers in this pool</STRONG> dialog box.</span></span>

    
    </div>

16. <span data-ttu-id="db12c-321">Klicken Sie unter **Computer in diesem Pool definieren** auf **Hinzufügen**, und wiederholen Sie dann die Schritte 11 bis 14 für den zweiten Edgeserver, den Sie Ihrem Edge-Pool hinzufügen möchten.</span><span class="sxs-lookup"><span data-stu-id="db12c-321">In **Define the computers in this pool**, click **Add**, and then repeat steps 11 through 14 for the second Edge Server that you want to add to your Edge pool.</span></span>

17. <span data-ttu-id="db12c-322">Nachdem Sie die Schritte 11 bis 14 wiederholt haben, klicken Sie unter **Definieren der Computer in diesem Pool** auf **weiter** .</span><span class="sxs-lookup"><span data-stu-id="db12c-322">After you repeat steps 11 through 14, click **Next** in **Define the computers in this pool**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="db12c-323">An dieser Stelle können Sie die beiden Edgeserver in Ihrem Pool sehen.</span><span class="sxs-lookup"><span data-stu-id="db12c-323">At this point, you can see both of the Edge Servers in your pool.</span></span>

    
    </div>

18. <span data-ttu-id="db12c-324">Wählen Sie im **Feld nächsten Hop definieren** in der Liste **Nächster Hop-Pool** den Namen des internen Pools aus, der entweder ein Front-End-Pool oder ein Standard Edition-Pool sein kann.</span><span class="sxs-lookup"><span data-stu-id="db12c-324">In **Define the next hop**, in the **Next hop pool** list, select the name of the internal pool, which can be either a Front End pool or a Standard Edition pool.</span></span> <span data-ttu-id="db12c-325">Wenn Ihre Bereitstellung einen Director umfasst, wählen Sie den Namen des Directors aus.</span><span class="sxs-lookup"><span data-stu-id="db12c-325">Or, if your deployment includes a Director, select the name of the Director.</span></span> <span data-ttu-id="db12c-326">Klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="db12c-326">Then, click **Next**.</span></span>

19. <span data-ttu-id="db12c-327">Geben Sie in **Front-End-Pools zuordnen** einen oder mehrere interne Pools an, die Front-End-Pools und Standard Edition-Server enthalten können, die diesem Edgeserver zugeordnet werden sollen, indem Sie die Namen der internen Pools auswählen, die diesen Edgeserver für die Kommunikation mit unterstützten externen Benutzern verwenden sollen.</span><span class="sxs-lookup"><span data-stu-id="db12c-327">In **Associate Front End pools**, specify one or more internal pools, which can include Front End pools and Standard Edition servers, to be associated with this Edge Server, by selecting the names of the internal pool(s) that is to use this Edge Server for communication with supported external users.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="db12c-328">Jedem internen Pool für A/V-Datenverkehr kann nur ein Edge-Pool mit Lastenausgleich oder ein einzelner Edgeserver zugeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="db12c-328">Only one load-balanced Edge pool or single Edge Server can be associated with each internal pool for A/V traffic.</span></span> <span data-ttu-id="db12c-329">Wenn Sie bereits über einen internen Pool verfügen, der einem Edge-Pool oder Edgeserver zugeordnet ist, wird eine Warnung angezeigt, die besagt, dass dem internen Pool bereits ein Edge-Pool oder ein Edgeserver zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="db12c-329">If you already have an internal pool associated with an Edge pool or Edge Server, a warning appears indicating that the internal pool is already associated an Edge pool or Edge Server.</span></span> <span data-ttu-id="db12c-330">Wenn Sie einen Pool auswählen, der bereits einem anderen Edgeserver zugeordnet ist, wird die Zuordnung geändert.</span><span class="sxs-lookup"><span data-stu-id="db12c-330">If you select a pool that is already associated with another Edge Server, it will change the association.</span></span>

    
    </div>

20. <span data-ttu-id="db12c-331">Klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="db12c-331">Click **Finish**.</span></span>

21. <span data-ttu-id="db12c-332">Veröffentlichen Sie Ihre Topologie.</span><span class="sxs-lookup"><span data-stu-id="db12c-332">Publish your topology.</span></span>

<span data-ttu-id="db12c-333"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="db12c-333"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

