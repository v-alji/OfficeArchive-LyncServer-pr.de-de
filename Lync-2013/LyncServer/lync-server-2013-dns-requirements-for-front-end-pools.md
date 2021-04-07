---
title: 'Lync Server 2013: DNS-Anforderungen für Front -End-Pools'
description: 'Lync Server 2013: DNS-Anforderungen für Front -End-Pools.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pools
ms:assetid: ba28919c-fbbe-4c54-8bf9-2b0cd3fa39c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412910(v=OCS.15)
ms:contentKeyID: 48185228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c0369e82bd8ed2ea63e2156728b41f9942b0148
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429070"
---
# <a name="dns-requirements-for-front-end-pools-in-lync-server-2013"></a><span data-ttu-id="4ce91-103">DNS-Anforderungen für Front -End-Pools in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4ce91-103">DNS requirements for Front End pools in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4ce91-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4ce91-104">

<span> </span></span></span>

<span data-ttu-id="4ce91-105">_**Thema Letzte Änderung:** 11.11.2012_</span><span class="sxs-lookup"><span data-stu-id="4ce91-105">_**Topic Last Modified:** 2012-11-07_</span></span>

<span data-ttu-id="4ce91-106">In diesem Abschnitt werden die DNS-Einträge (Domain Name System) beschrieben, die für die Bereitstellung von Front -End-Pools erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4ce91-106">This section describes the Domain Name System (DNS) records that are required for deployment of Front End pools.</span></span>

<div>

## <a name="dns-records-for-front-end-pools"></a><span data-ttu-id="4ce91-107">DNS-Einträge für Front -End-Pools</span><span class="sxs-lookup"><span data-stu-id="4ce91-107">DNS Records for Front End Pools</span></span>

<span data-ttu-id="4ce91-108">In der folgenden Tabelle sind die DNS-Anforderungen für eine Lync Server 2013-Front-End-Poolbereitstellung angegeben.</span><span class="sxs-lookup"><span data-stu-id="4ce91-108">The following table specifies DNS requirements for a Lync Server 2013 Front End pool deployment.</span></span>

### <a name="dns-requirements-for-a-front-end-pool"></a><span data-ttu-id="4ce91-109">DNS-Anforderungen für einen Front -End-Pool</span><span class="sxs-lookup"><span data-stu-id="4ce91-109">DNS Requirements for a Front End Pool</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4ce91-110">Bereitstellungsszenario</span><span class="sxs-lookup"><span data-stu-id="4ce91-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="4ce91-111">DNS-Anforderung</span><span class="sxs-lookup"><span data-stu-id="4ce91-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ce91-112">Front -End-Pool mit mehreren Front -End-Servern und einem Hardwareladeausgleich (unabhängig davon, ob der DNS-Lastenausgleich auch in diesem Pool bereitgestellt wird)</span><span class="sxs-lookup"><span data-stu-id="4ce91-112">Front End pool with multiple Front End Servers and a hardware load balancer (whether or not DNS load balancing is also deployed on that pool)</span></span></p></td>
<td><p><span data-ttu-id="4ce91-113">Wenn Sie sowohl den DNS-Lastenausgleich als auch einen Hardwareladeausgleich verwenden, müssen Sie A-Einträge hosten.</span><span class="sxs-lookup"><span data-stu-id="4ce91-113">When using both DNS load balancing and a hardware load balancer, you need to Host (A) records.</span></span> <span data-ttu-id="4ce91-114">Erstellen Sie einen internen A-Eintrag, der den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Front -End-Pools für den DNS-Lastenausgleich aufhebt.</span><span class="sxs-lookup"><span data-stu-id="4ce91-114">Create an internal A record that resolves the fully qualified domain name (FQDN) of the Front End pool for DNS load balancing.</span></span> <span data-ttu-id="4ce91-115">Erstellen Sie einen internen Hostdatensatz (A) für die internen Webdienste an die virtuelle IP-Adresse (VIP) des Load Balancers.</span><span class="sxs-lookup"><span data-stu-id="4ce91-115">Create an internal host (A) record for the internal Web services to the virtual IP (VIP) address of the load balancer.</span></span> <span data-ttu-id="4ce91-116">Sie müssen den internen Webdienstnamen wie im Topologie-Generator definiert verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ce91-116">You must use the internal Web services name as defined in Topology Builder.</span></span></p>
<p><span data-ttu-id="4ce91-117">Wenn Sie z. B. sowohl den DNS-Lastenausgleich als auch den Hardwarelastausgleich verwenden, verfügen Sie über einen A-Eintrag für jeden Front End Server in einem Pool für den DNS-Lastenausgleich und einen A-Eintrag für die internen Webdienste, der auf die virtuelle IP des Hardwareladeausgleichs zeigt:</span><span class="sxs-lookup"><span data-stu-id="4ce91-117">For example, if you use both DNS load balancing and hardware load balancing, you would have an A record for each Front End Server in a pool for DNS load balancing, and an A record for the internal Web services pointing to the virtual IP of the hardware load balancer:</span></span></p>
<ul>
<li><p><span data-ttu-id="4ce91-118">DNS-Lastenausgleich: Pool01.contoso.net -IP-Adresse des Pools 10.10.10.5</span><span class="sxs-lookup"><span data-stu-id="4ce91-118">DNS load balancing:   Pool01.contoso.net   IP Address of pool   10.10.10.5</span></span></p>
<div>

> [!WARNING]  
> <span data-ttu-id="4ce91-119">Jeder Front End Server verfügt auch über einen eindeutigen A-Eintrag:</span><span class="sxs-lookup"><span data-stu-id="4ce91-119">Each Front End Server will also have a distinct A record:</span></span>


</div>
<ol>
<li><p><span data-ttu-id="4ce91-120">FE01.contoso.net 10.10.10.1</span><span class="sxs-lookup"><span data-stu-id="4ce91-120">FE01.contoso.net    10.10.10.1</span></span></p></li>
<li><p><span data-ttu-id="4ce91-121">FE02.contoso.net 10.10.10.2</span><span class="sxs-lookup"><span data-stu-id="4ce91-121">FE02.contoso.net    10.10.10.2</span></span></p></li>
<li><p><span data-ttu-id="4ce91-122">FE03.contoso.net 10.10.10.3</span><span class="sxs-lookup"><span data-stu-id="4ce91-122">FE03.contoso.net    10.10.10.3</span></span></p></li>
<li><p><span data-ttu-id="4ce91-123">FE04.contoso.net 10.10.10.4</span><span class="sxs-lookup"><span data-stu-id="4ce91-123">FE04.contoso.net    10.10.10.4</span></span></p></li>
</ol></li>
<li><p><span data-ttu-id="4ce91-124">Hardwarelastausgleich: WebInternal.contoso.net #A0 von HLB VIP 192.168.10.5</span><span class="sxs-lookup"><span data-stu-id="4ce91-124">Hardware load balancing:   WebInternal.contoso.net   IP Address of HLB VIP   192.168.10.5</span></span></p></li>
</ul>
<p><span data-ttu-id="4ce91-125">Für den ganzen Datenverkehr mit Ausnahme von HTTP/HTTPS-Datenverkehr wird der Pool01.contoso.net verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ce91-125">All traffic except for HTTP/HTTPS traffic will use the Pool01.contoso.net record.</span></span> <span data-ttu-id="4ce91-126">FÜR HTTP/HTTPS-Datenverkehr wird die definierte interne Webdienstadresse von 192.168.10.5 verwendet.</span><span class="sxs-lookup"><span data-stu-id="4ce91-126">HTTP/HTTPS traffic will use the defined internal Web services address of 192.168.10.5</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ce91-127">Front -End-Pool mit bereitgestellter DNS-Lastenverteilung</span><span class="sxs-lookup"><span data-stu-id="4ce91-127">Front End pool with DNS load balancing deployed</span></span></p></td>
<td><p><span data-ttu-id="4ce91-128">Eine Gruppe interner A-Datensätze, die den FQDN des Pools auf die IP-Adresse jedes Servers im Pool auflösen.</span><span class="sxs-lookup"><span data-stu-id="4ce91-128">A set of internal A records that resolve the FQDN of the pool to the IP address of each server in the pool.</span></span> <span data-ttu-id="4ce91-129">Für jeden Server im Pool muss ein A-Eintrag vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="4ce91-129">There must one A record for each server in the pool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ce91-130">Front -End-Pool mit bereitgestellter DNS-Lastenverteilung</span><span class="sxs-lookup"><span data-stu-id="4ce91-130">Front End pool with DNS load balancing deployed</span></span></p></td>
<td><p><span data-ttu-id="4ce91-131">Eine Reihe interner A-Einträge, die den FQDN jedes Servers im Pool an die IP-Adresse des Servers auflösen.</span><span class="sxs-lookup"><span data-stu-id="4ce91-131">A set of internal A records that resolve the FQDN of each server in the pool to the IP address of that server.</span></span> <span data-ttu-id="4ce91-132">Ausführliche Informationen finden Sie unter <a href="lync-server-2013-dns-load-balancing.md">DNS-Lastenausgleich in Lync Server 2013</a> in der Dokumentation zur Planung.</span><span class="sxs-lookup"><span data-stu-id="4ce91-132">For details, see <a href="lync-server-2013-dns-load-balancing.md">DNS load balancing in Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ce91-133">Front -End-Pool mit einem einzelnen Front End Server und einer dedizierten Back-End-Datenbank, aber ohne Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="4ce91-133">Front End pool with a single Front End Server and a dedicated back-end database but no load balancer</span></span></p></td>
<td><p><span data-ttu-id="4ce91-134">Ein interner A-Eintrag, der den FQDN des Front -End-Pools auf die IP-Adresse des einzelnen Enterprise Edition Front End Servers aufhebt.</span><span class="sxs-lookup"><span data-stu-id="4ce91-134">An internal A record that resolves the FQDN of the Front End pool to the IP address of the single Enterprise Edition Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ce91-135">Automatische Client-Anmeldung</span><span class="sxs-lookup"><span data-stu-id="4ce91-135">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="4ce91-136">Für jede unterstützte SIP-Domäne einen SRV-Eintrag für _sipinternaltls._tcp. &lt; Domäne &gt; über Port 5061, der dem FQDN des Front -End-Pools zu ordnet, der Clientanforderungen für die Anmeldung authentifiziert und umleitt.</span><span class="sxs-lookup"><span data-stu-id="4ce91-136">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Front End pool that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="4ce91-137">Details finden Sie unter <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS-Anforderungen für die automatische Client-Anmeldung in Lync Server 2013.</a></span><span class="sxs-lookup"><span data-stu-id="4ce91-137">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ce91-138">Device Update Web Service Discovery by Unified Communications (UC)-Geräte</span><span class="sxs-lookup"><span data-stu-id="4ce91-138">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="4ce91-139">Ein interner A-Eintrag mit dem Namen ucupdates-r2. &lt; SIP-Domäne, die auf die IP-Adresse des &gt; Front -End-Pools aufgelöst wird, der den Geräteupdatewebdienst hostet.</span><span class="sxs-lookup"><span data-stu-id="4ce91-139">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Front End pool that hosts the Device Update Web service.</span></span> <span data-ttu-id="4ce91-140">In der Situation, in der ein UC-Gerät aktiviert ist, sich ein Benutzer aber noch nie beim Gerät angemeldet hat, ermöglicht der A-Eintrag dem Gerät, den Front -End-Pool-Hostinggeräteupdate-Webdienst zu ermitteln und Updates zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="4ce91-140">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the Front End pool hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="4ce91-141">Andernfalls erhalten Geräte diese Informationen, obwohl sie bei der ersten Benutzeranmeldezeit in der Bandbereitstellung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="4ce91-141">Otherwise, devices obtain this information though in-band provisioning the first time a user logs in.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="4ce91-142">Wenn Sie in Lync Server 2010 über eine Bereitstellung des Geräteupdatewebdiensts verfügen, haben Sie bereits einen internen A-Eintrag mit dem Namen ucupdates erstellt. &lt; SIP-Domäne &gt; .</span><span class="sxs-lookup"><span data-stu-id="4ce91-142">If you have an existing deployment of Device Update Web service in Lync Server 2010, you have already created an internal A record with the name ucupdates.&lt;SIP domain&gt;.</span></span> <span data-ttu-id="4ce91-143">Für Microsoft Office Communications Server 2007 R2 müssen Sie einen zusätzlichen DNS A-Eintrag mit dem Namen ucupdates-r2 erstellen. &lt; SIP-Domäne &gt; .</span><span class="sxs-lookup"><span data-stu-id="4ce91-143">For Microsoft Office Communications Server 2007 R2, you must create an additional DNS A record with the name ucupdates-r2.&lt;SIP domain&gt;.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4ce91-144">Ein Reverseproxy zur Unterstützung von HTTP-Datenverkehr</span><span class="sxs-lookup"><span data-stu-id="4ce91-144">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="4ce91-145">Ein externer A-Eintrag, der den FQDN der externen Webfarm in die externe IP-Adresse des Reverseproxys aufhebt.</span><span class="sxs-lookup"><span data-stu-id="4ce91-145">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="4ce91-146">Clients und UC-Geräte verwenden diesen Eintrag, um eine Verbindung mit dem Reverseproxy herzustellen.</span><span class="sxs-lookup"><span data-stu-id="4ce91-146">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="4ce91-147">Ausführliche Informationen finden Sie <a href="lync-server-2013-determine-dns-requirements.md">unter Ermitteln der DNS-Anforderungen für Lync Server 2013</a> in der Dokumentation "Planung".</span><span class="sxs-lookup"><span data-stu-id="4ce91-147">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="4ce91-148">Die folgende Tabelle zeigt ein Beispiel für die dns-Einträge, die für die interne Webfarm FQDN erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="4ce91-148">The following table shows an example of the DNS records required for the internal web farm FQDN.</span></span>

### <a name="example-dns-records-for-internal-web-farm-fqdn"></a><span data-ttu-id="4ce91-149">Beispiel-DNS-Einträge für FQDN der internen Webfarm</span><span class="sxs-lookup"><span data-stu-id="4ce91-149">Example DNS Records for Internal Web Farm FQDN</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4ce91-150">FQDN für interne Webfarmen</span><span class="sxs-lookup"><span data-stu-id="4ce91-150">Internal web farm FQDN</span></span></th>
<th><span data-ttu-id="4ce91-151">Pool-FQDN</span><span class="sxs-lookup"><span data-stu-id="4ce91-151">Pool FQDN</span></span></th>
<th><span data-ttu-id="4ce91-152">DNS A-Einträge</span><span class="sxs-lookup"><span data-stu-id="4ce91-152">DNS A record(s)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4ce91-153">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="4ce91-153">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="4ce91-154">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="4ce91-154">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="4ce91-155">DNS Ein Eintrag für die ee-pool.contoso.com, der in die VIP-Adresse des Load Balancers aufgelöst wird, der von den Front -End-Servern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4ce91-155">DNS A record for the ee-pool.contoso.com that resolves to the VIP address of the load balancer used by the Front End Servers.</span></span></p>
<p><span data-ttu-id="4ce91-156">DNS Ein Eintrag für webcon.contoso.com, der in die VIP-Adresse des Load Balancers aufgelöst wird, der von den Front -End-Servern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4ce91-156">DNS A record for webcon.contoso.com that resolves to the VIP address of the load balancer used by the Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4ce91-157">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="4ce91-157">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="4ce91-158">ee-pool.contoso.com</span><span class="sxs-lookup"><span data-stu-id="4ce91-158">ee-pool.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="4ce91-159">DNS Ein Eintrag für ee-pool.contoso.com, der in die virtuelle IP-Adresse (VIP) des Load Balancers aufgelöst wird, der von den Enterprise Edition Front End-Servern im Front -End-Pool verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="4ce91-159">DNS A record for ee-pool.contoso.com that resolves to the virtual IP (VIP) address of the load balancer used by the Enterprise Edition Front End Servers in the Front End pool.</span></span></p>
<p><span data-ttu-id="4ce91-160">Beachten Sie, dass ihr Front -End-Pool und die interne Webfarm nicht über denselben FQDN verfügen können, wenn Sie den DNS-Lastenausgleich für diesen Pool verwenden.</span><span class="sxs-lookup"><span data-stu-id="4ce91-160">Note that if you are using DNS load balancing on this pool, your Front End pool and internal web farm cannot have the same FQDN.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="4ce91-161">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4ce91-161">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

