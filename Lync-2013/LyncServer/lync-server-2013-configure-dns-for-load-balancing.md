---
title: 'Lync Server 2013: Konfigurieren von DNS für den Lastenausgleich'
description: 'Lync Server 2013: Konfigurieren von DNS für den Lastenausgleich'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS for load balancing
ms:assetid: 1b2e8414-8676-4872-8ecf-ea07196f74de
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398251(v=OCS.15)
ms:contentKeyID: 48183540
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4b13db22d65ee67723ebc0a31544137d467d5c6b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395123"
---
# <a name="configure-dns-for-load-balancing-in-lync-server-2013"></a><span data-ttu-id="46c6f-103">Konfigurieren von DNS für den Lastenausgleich in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46c6f-103">Configure DNS for load balancing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="46c6f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="46c6f-104">

<span> </span></span></span>

<span data-ttu-id="46c6f-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="46c6f-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="46c6f-106">Um dieses Verfahren erfolgreich durchführen zu können, sollten Sie am Server oder in der Domäne minimal als Mitglied der Gruppe der Domänenadministratoren oder als Mitglied der DnsAdmins-Gruppe angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="46c6f-106">To successfully complete this procedure, you should be logged on to the server or domain minimally as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="46c6f-107">Der DNS-Lastenausgleich (Domain Name System) balanciert den Netzwerkdatenverkehr aus, der für lync Server 2013 eindeutig ist, wie etwa SIP-Datenverkehr und Mediendatenverkehr.</span><span class="sxs-lookup"><span data-stu-id="46c6f-107">Domain Name System (DNS) Load Balancing balances the network traffic that is unique to Lync Server 2013, such as SIP traffic and media traffic.</span></span> <span data-ttu-id="46c6f-108">Der DNS-Lastenausgleich wird für Front-End-Pools, Edge-Pools, Director-Pools und eigenständige Vermittlungs Pools unterstützt.</span><span class="sxs-lookup"><span data-stu-id="46c6f-108">DNS load balancing is supported for Front End pools, Edge pools, Director pools, and stand-alone Mediation pools.</span></span> <span data-ttu-id="46c6f-109">Für einen Pool, der für die Verwendung des DNS-Lastenausgleichs konfiguriert ist, müssen zwei vollqualifizierte Domänennamen (FQDNs) definiert sein: der reguläre Pool-FQDN, der vom DNS-Lastenausgleich verwendet wird (beispielsweise pool1.contoso.com), der zu den physikalischen IPS der Server im Pool aufgelöst wird, und ein anderer FQDN für die Webdienste des Pools (beispielsweise web1.contoso.net), der in die virtuelle IP-Adresse des Pools aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="46c6f-109">A pool that is configured to use DNS load balancing must have two fully qualified domain names (FQDNs) defined: the regular pool FQDN that is used by DNS load balancing (for example, pool1.contoso.com) and that resolves to the physical IPs of the servers in the pool, and another FQDN for the pool’s Web Services (for example, web1.contoso.net), which resolves to the virtual IP address of the pool.</span></span> <span data-ttu-id="46c6f-110">Details zum DNS-Lastenausgleich finden Sie unter [DNS-Lastenausgleich in lync Server 2013](lync-server-2013-dns-load-balancing.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="46c6f-110">For details about DNS Load Balancing, see [DNS load balancing in Lync Server 2013](lync-server-2013-dns-load-balancing.md) in the Planning documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="46c6f-111">Für den HTTPS-Datenverkehr zwischen Client und Server ist weiterhin Hardware Lastenausgleich erforderlich.</span><span class="sxs-lookup"><span data-stu-id="46c6f-111">Hardware load balancing is still required for client to server HTTPS traffic.</span></span>



</div>

<span data-ttu-id="46c6f-112">Bevor Sie den DNS-Lastenausgleich verwenden können, müssen Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="46c6f-112">Before you can use DNS load balancing, you must do the following:</span></span>

1.  <span data-ttu-id="46c6f-113">Überschreiben Sie den internen FQDN des Webdienste-Pools.</span><span class="sxs-lookup"><span data-stu-id="46c6f-113">Override the internal Web Services pool FQDN.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="46c6f-114">Wenn Sie beschließen, die internen Webdienste mit einem selbst definierten FQDN zu überschreiben, muss jeder FQDN für jeden anderen Front-End-Pool, Director oder Director-Pool eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="46c6f-114">If decide to override the Internal web services with a self-defined FQDN, each FQDN must be unique from any other Front End pool, Director or a Director pool.</span></span>

    
    </div>

2.  <span data-ttu-id="46c6f-115">Erstellen Sie DNS-A-Hosteinträge, um den FQDN des Pools in die IP-Adressen aller Server im Pool aufzulösen.</span><span class="sxs-lookup"><span data-stu-id="46c6f-115">Create DNS A host records to resolve the pool FQDN to the IP addresses of all the servers in the pool.</span></span>

3.  <span data-ttu-id="46c6f-116">Aktivieren Sie die zufällige IP-Adresse, oder aktivieren Sie für Windows Server-DNS Round Robin.</span><span class="sxs-lookup"><span data-stu-id="46c6f-116">Enable IP Address randomization or, for Windows Server DNS, enable round robin.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="46c6f-117">Round Robin sollte standardmäßig aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="46c6f-117">Round robin should be enabled by default.</span></span>

    
    </div>

<div>

## <a name="to-override-internal-web-services-fqdn"></a><span data-ttu-id="46c6f-118">So heben Sie den internen FQDN von Webdiensten auf</span><span class="sxs-lookup"><span data-stu-id="46c6f-118">To override internal Web services FQDN</span></span>

1.  <span data-ttu-id="46c6f-119">Starten Sie den Topologie-Generator: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server Topology Builder**.</span><span class="sxs-lookup"><span data-stu-id="46c6f-119">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="46c6f-120">Erweitern Sie in der Konsolenstruktur den Knoten Enterprise Edition-Front-End-Pools.</span><span class="sxs-lookup"><span data-stu-id="46c6f-120">From the console tree, expand the Enterprise Edition Front End pools node.</span></span>

3.  <span data-ttu-id="46c6f-121">Klicken Sie mit der rechten Maustaste auf den Pool, klicken Sie auf **Eigenschaften bearbeiten**, und klicken Sie dann auf **Webdienste**.</span><span class="sxs-lookup"><span data-stu-id="46c6f-121">Right-click the pool, click **Edit Properties**, and then click **Web Services**.</span></span>

4.  <span data-ttu-id="46c6f-122">Aktivieren Sie unter **interne Webdienste** das Kontrollkästchen **FQDN überschreiben** .</span><span class="sxs-lookup"><span data-stu-id="46c6f-122">Below **Internal web services**, select the **Override FQDN** check box.</span></span>

5.  <span data-ttu-id="46c6f-123">Geben Sie den FQDN des Pools ein, der in die physischen IP-Adressen der Server im Pool aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="46c6f-123">Type the pool FQDN that resolves to the physical IP addresses of the servers in the pool.</span></span>

6.  <span data-ttu-id="46c6f-124">Geben Sie unter **externe Webdienste** den FQDN des externen Pools ein, der in die virtuellen IP-Adressen des Pools aufgelöst wird, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="46c6f-124">Below **External web services**, type the external pool FQDN that resolves to the virtual IP addresses of the pool, and then click **OK**.</span></span>

7.  <span data-ttu-id="46c6f-125">Klicken Sie in der Konsolenstruktur auf **lync Server 2013**, und klicken Sie dann im Bereich **Aktionen** auf **Topologie veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="46c6f-125">From the console tree, click **Lync Server 2013**, and then in the **Actions** pane, click **Publish Topology**.</span></span>

</div>

<div>

## <a name="to-create-dns-host-a-records-for-all-internal-pool-servers"></a><span data-ttu-id="46c6f-126">So erstellen Sie DNS-Host Einträge (A) für alle internen Pool Server</span><span class="sxs-lookup"><span data-stu-id="46c6f-126">To create DNS Host (A) Records for all internal pool servers</span></span>

1.  <span data-ttu-id="46c6f-127">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **DNS**.</span><span class="sxs-lookup"><span data-stu-id="46c6f-127">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="46c6f-128">Klicken Sie im **DNS-Manager** auf den DNS-Server, der Ihre Datensätze verwaltet, um Sie zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="46c6f-128">In **DNS Manager**, click the DNS Server that manages your records to expand it.</span></span>

3.  <span data-ttu-id="46c6f-129">Klicken Sie auf **Forward-Lookupzonen** , um Sie zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="46c6f-129">Click **Forward Lookup Zones** to expand it.</span></span>

4.  <span data-ttu-id="46c6f-130">Klicken Sie mit der rechten Maustaste auf die DNS-Domäne, der Sie Datensätze hinzufügen müssen, und klicken Sie dann auf **neuer Host (A oder AAAA)**.</span><span class="sxs-lookup"><span data-stu-id="46c6f-130">Right-click the DNS domain that you need to add records to, and then click **New Host (A or AAAA)**.</span></span>

5.  <span data-ttu-id="46c6f-131">Geben Sie im Feld **Name** den Namen des Hosteintrags ein (der Domänenname wird automatisch angehängt).</span><span class="sxs-lookup"><span data-stu-id="46c6f-131">In the **Name** box, type the name of the host record (the domain name will be automatically appended).</span></span>

6.  <span data-ttu-id="46c6f-132">Geben Sie im Feld IP-Adresse die IP-Adresse des einzelnen Front-End-Servers ein, und wählen Sie dann **zugehörigen Zeigereintrag erstellen** aus, oder **ermöglichen Sie es jedem authentifizierten Benutzer, DNS-Einträge mit demselben Besitzernamen zu aktualisieren**, sofern zutreffend.</span><span class="sxs-lookup"><span data-stu-id="46c6f-132">In the IP Address box, type the IP address of the individual Front End Server and then select **Create associated pointer (PTR) record** or **Allow any authenticated user to update DNS records with the same owner name**, if applicable.</span></span>

7.  <span data-ttu-id="46c6f-133">Erstellen Sie weiterhin Datensätze für alle Member-Front-End-Server, die am DNS-Lastenausgleich beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="46c6f-133">Continue creating records for all member Front End Servers that will participate in DNS Load Balancing.</span></span>
    
    <span data-ttu-id="46c6f-134">Wenn Sie beispielsweise über einen Pool mit dem Namen pool1.contoso.com und drei Front-End-Server verfügen, erstellen Sie die folgenden DNS-Einträge:</span><span class="sxs-lookup"><span data-stu-id="46c6f-134">For example, if you had a pool named pool1.contoso.com and three Front End Servers, you would create the following DNS entries:</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="46c6f-135">FQDN</span><span class="sxs-lookup"><span data-stu-id="46c6f-135">FQDN</span></span></th>
    <th><span data-ttu-id="46c6f-136">Typ</span><span class="sxs-lookup"><span data-stu-id="46c6f-136">Type</span></span></th>
    <th><span data-ttu-id="46c6f-137">Daten</span><span class="sxs-lookup"><span data-stu-id="46c6f-137">Data</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="46c6f-138">Pool1.contoso.com</span><span class="sxs-lookup"><span data-stu-id="46c6f-138">Pool1.contoso.com</span></span></p></td>
    <td><p><span data-ttu-id="46c6f-139">Host (A)</span><span class="sxs-lookup"><span data-stu-id="46c6f-139">Host (A)</span></span></p></td>
    <td><p><span data-ttu-id="46c6f-140">192.168.1.1</span><span class="sxs-lookup"><span data-stu-id="46c6f-140">192.168.1.1</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="46c6f-141">Pool1.contoso.com</span><span class="sxs-lookup"><span data-stu-id="46c6f-141">Pool1.contoso.com</span></span></p></td>
    <td><p><span data-ttu-id="46c6f-142">Host (A)</span><span class="sxs-lookup"><span data-stu-id="46c6f-142">Host (A)</span></span></p></td>
    <td><p><span data-ttu-id="46c6f-143">192.168.1.2</span><span class="sxs-lookup"><span data-stu-id="46c6f-143">192.168.1.2</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="46c6f-144">Pool1.contoso.com</span><span class="sxs-lookup"><span data-stu-id="46c6f-144">Pool1.contoso.com</span></span></p></td>
    <td><p><span data-ttu-id="46c6f-145">Host (A)</span><span class="sxs-lookup"><span data-stu-id="46c6f-145">Host (A)</span></span></p></td>
    <td><p><span data-ttu-id="46c6f-146">192.168.1.3</span><span class="sxs-lookup"><span data-stu-id="46c6f-146">192.168.1.3</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
    <span data-ttu-id="46c6f-147">Details zum Erstellen von DNS-Hosteinträgen (A) finden Sie unter [Konfigurieren von DNS-Hosteinträgen für lync Server 2013](lync-server-2013-configure-dns-host-records.md).</span><span class="sxs-lookup"><span data-stu-id="46c6f-147">For details about creating DNS Host (A) records, see [Configure DNS Host records for Lync Server 2013](lync-server-2013-configure-dns-host-records.md).</span></span>

</div>

<div>

## <a name="to-enable-round-robin-for-windows-server"></a><span data-ttu-id="46c6f-148">So aktivieren Sie Round Robin für Windows Server</span><span class="sxs-lookup"><span data-stu-id="46c6f-148">To enable round robin for Windows Server</span></span>

1.  <span data-ttu-id="46c6f-149">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **DNS**.</span><span class="sxs-lookup"><span data-stu-id="46c6f-149">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="46c6f-150">Erweitern Sie **DNS**, klicken Sie mit der rechten Maustaste auf den DNS-Server, den Sie konfigurieren möchten, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="46c6f-150">Expand **DNS**, right-click the DNS server you want to configure, and then click **Properties**.</span></span>

3.  <span data-ttu-id="46c6f-151">Klicken Sie auf die Registerkarte **erweitert** , wählen Sie **Round Robin aktivieren** und **Netzmaske aktivieren** aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="46c6f-151">Click the **Advanced** tab, select **Enable round robin** and **Enable netmask ordering**, and then click **OK**.</span></span>
    
    <span data-ttu-id="46c6f-152">![DNS Round Robin (Dialogfeld)](images/Gg398251.e7bf6125-8d78-4460-8401-0a8e7e21d305(OCS.15).jpg "DNS Round Robin (Dialogfeld)")</span><span class="sxs-lookup"><span data-stu-id="46c6f-152">![DNS Round Robin dialog box](images/Gg398251.e7bf6125-8d78-4460-8401-0a8e7e21d305(OCS.15).jpg "DNS Round Robin dialog box")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="46c6f-153">Dieses Feature sollte standardmäßig aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="46c6f-153">This feature should be enabled by default.</span></span>



</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="46c6f-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46c6f-154">See Also</span></span>


[<span data-ttu-id="46c6f-155">DNS-Lastenausgleich in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="46c6f-155">DNS load balancing in Lync Server 2013</span></span>](lync-server-2013-dns-load-balancing.md)  
  

<span data-ttu-id="46c6f-156"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="46c6f-156"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

