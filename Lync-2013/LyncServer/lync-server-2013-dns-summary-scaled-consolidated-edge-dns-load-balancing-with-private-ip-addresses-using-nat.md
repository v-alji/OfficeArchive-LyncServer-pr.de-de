---
title: 'Lync Server 2013: DNS-Zusammenfassung für einen skalierten konsolidierten Edgeserver, DNS-Lastenausgleich mit privaten IP-Adressen und NAT'
description: 'Lync Server 2013: DNS-Zusammenfassung – skalierter konsolidierter Edge, DNS-Lastenausgleich mit privaten IP-Adressen mithilfe von NAT.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT
ms:assetid: 11bc7b84-91cf-48f9-ad0e-06ad30b46a2e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398201(v=OCS.15)
ms:contentKeyID: 48183447
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2eef3029323c1c2f798fddc721df832a932524c8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437707"
---
# <a name="dns-summary---scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="7519f-103">DNS-Zusammenfassung für einen skalierten konsolidierten Edgeserver, DNS-Lastenausgleich mit privaten IP-Adressen und NAT in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7519f-103">DNS summary - Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7519f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7519f-104">

<span> </span></span></span>

<span data-ttu-id="7519f-105">_**Letztes Änderungsdatum des Themas:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="7519f-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="7519f-106">Die Anforderungen für den DNS-Eintrag für den Remotezugriff auf lync Server 2013 sind im Vergleich zu Zertifikaten und Ports relativ einfach.</span><span class="sxs-lookup"><span data-stu-id="7519f-106">DNS record requirements for remote access to Lync Server 2013 are fairly straightforward compared to those for certificates and ports.</span></span> <span data-ttu-id="7519f-107">Darüber hinaus sind viele Datensätze optional, je nachdem, wie Sie Clients mit lync 2013 konfigurieren und ob Sie die Föderation aktivieren.</span><span class="sxs-lookup"><span data-stu-id="7519f-107">Also, many records are optional, depending on how you configure clients running Lync 2013 and whether you enable federation.</span></span>

<span data-ttu-id="7519f-108">Details zu den DNS-Anforderungen von lync 2013 finden Sie unter [Ermitteln der DNS-Anforderungen für lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7519f-108">For details about Lync 2013 DNS requirements, see [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="7519f-109">Ausführliche Informationen zum Konfigurieren der automatischen Konfiguration von lync 2013-Clients, wenn das Split-Brain-DNS nicht konfiguriert ist, finden Sie im Abschnitt "automatische Konfiguration ohne geteilten Brain-DNS" unter [Ermitteln der DNS-Anforderungen für lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="7519f-109">For details about configuring automatic configuration of Lync 2013 clients if split-brain DNS is not configured, see the "Automatic Configuration without Split Brain DNS" section in [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="7519f-110">Die folgende Tabelle enthält eine Zusammenfassung der DNS-Einträge, die für die Unterstützung der einzelnen konsolidierten Edge-Topologie erforderlich sind, die in der einzelnen konsolidierten Edge-Topologie-Abbildung dargestellt ist.</span><span class="sxs-lookup"><span data-stu-id="7519f-110">The following table contains a summary of the DNS records that are required to support the single consolidated edge topology shown in the Single Consolidated Edge Topology figure.</span></span> <span data-ttu-id="7519f-111">Beachten Sie, dass bestimmte DNS-Einträge nur für die automatische Konfiguration von lync 2013-Clients erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7519f-111">Note that certain DNS records are required only for automatic configuration of Lync 2013 clients.</span></span> <span data-ttu-id="7519f-112">Wenn Sie beabsichtigen, Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) zum Konfigurieren von lync-Clients zu verwenden, sind die zugehörigen Datensätze nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7519f-112">If you plan to use group policy objects (GPOs) to configure Lync clients, the associated records are not necessary.</span></span>

<div>

## <a name="important-edge-server-network-adapter-requirements"></a><span data-ttu-id="7519f-113">Wichtig: Anforderungen des Edge-Server-Netzwerkadapters</span><span class="sxs-lookup"><span data-stu-id="7519f-113">IMPORTANT: Edge Server Network Adapter Requirements</span></span>

<span data-ttu-id="7519f-114">Um Routingprobleme zu vermeiden, stellen Sie sicher, dass Ihre Edgeserver mindestens zwei Netzwerkadapter aufweisen und dass das Standardgateway nur auf dem Netzwerkadapter festgesetzt ist, der der externen Schnittstelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="7519f-114">To avoid routing issues, verify that there are at least two network adapters in your Edge Servers and that the default gateway is set only on the network adapter associated with the external interface.</span></span> <span data-ttu-id="7519f-115">Beispielsweise würde das Standardgateway auf die externe Firewall verweisen, wie es in der Szenariogröße des skalierten konsolidierten Rands in der [skalierten konsolidierten Kante, dem DNS-Lastenausgleich mit privaten IP-Adressen mithilfe von NAT in lync Server 2013](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md)gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="7519f-115">For example, as shown in the Scaled Consolidated Edge Scenario figure in [Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md), the default gateway would point to the external firewall.</span></span>

<span data-ttu-id="7519f-116">Sie können zwei Netzwerkadapter auf jedem Edgeserver wie folgt konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="7519f-116">You can configure two network adapters in each of your Edge Server as follows:</span></span>

  - <span data-ttu-id="7519f-117">**Netzwerkadapter 1 – Knoten 1 (interne Schnittstelle)**</span><span class="sxs-lookup"><span data-stu-id="7519f-117">**Network adapter 1 - Node 1 (Internal Interface)**</span></span>
    
    <span data-ttu-id="7519f-118">Interne Schnittstelle mit zugewiesenem 172.25.33.10</span><span class="sxs-lookup"><span data-stu-id="7519f-118">Internal interface with 172.25.33.10 assigned.</span></span>
    
    <span data-ttu-id="7519f-119">Es wurde kein Standardgateway definiert.</span><span class="sxs-lookup"><span data-stu-id="7519f-119">No default gateway is defined.</span></span>
    
    <span data-ttu-id="7519f-120">Stellen Sie sicher, dass eine Route vom Netzwerk mit der Edge-internen Schnittstelle zu allen Netzwerken vorhanden ist, die Server mit lync Server 2013-oder lync Server 2013-Clients enthalten (beispielsweise von 172.25.33.0 bis 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="7519f-120">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="7519f-121">**Netzwerkadapter 1 – Knoten 2 (interne Schnittstelle)**</span><span class="sxs-lookup"><span data-stu-id="7519f-121">**Network adapter 1 - Node 2 (Internal Interface)**</span></span>
    
    <span data-ttu-id="7519f-122">Interne Schnittstelle mit zugewiesenem 172.25.33.11</span><span class="sxs-lookup"><span data-stu-id="7519f-122">Internal interface with 172.25.33.11 assigned.</span></span>
    
    <span data-ttu-id="7519f-123">Es wurde kein Standardgateway definiert.</span><span class="sxs-lookup"><span data-stu-id="7519f-123">No default gateway is defined.</span></span>
    
    <span data-ttu-id="7519f-124">Stellen Sie sicher, dass eine Route vom Netzwerk mit der Edge-internen Schnittstelle zu allen Netzwerken vorhanden ist, die Server mit lync Server 2013-oder lync Server 2013-Clients enthalten (beispielsweise von 172.25.33.0 bis 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="7519f-124">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="7519f-125">**Netzwerkadapter 2 Knoten 1 (externe Schnittstelle)**</span><span class="sxs-lookup"><span data-stu-id="7519f-125">**Network adapter 2 Node 1 (External Interface)**</span></span>
    
    <span data-ttu-id="7519f-126">Diesem Netzwerkadapter werden drei private IP-Adressen zugewiesen, beispielsweise 10.45.16.10 für Access Edge, 10.45.16.20 for Web Conferencing Edge, 10.45.16.30 für AV Edge.</span><span class="sxs-lookup"><span data-stu-id="7519f-126">Three private IP addresses are assigned to this network adapter, for example 10.45.16.10 for Access Edge, 10.45.16.20 for Web Conferencing Edge, 10.45.16.30 for AV Edge.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="7519f-127">Es ist jedoch möglich, eine einzige IP-Adresse für alle drei Edge-Service-Interfaces zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7519f-127">It is possible, though not recommended, to use a single IP address for all three Edge service interfaces.</span></span> <span data-ttu-id="7519f-128">Obwohl dadurch IP-Adressen gespeichert werden, sind für jeden Dienst unterschiedliche Portnummern erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7519f-128">Though this does save IP addresses, it requires different port numbers for each service.</span></span> <span data-ttu-id="7519f-129">Die Standardportnummer ist 443/TCP, wodurch sichergestellt wird, dass die meisten Remote Firewalls den Datenverkehr zulassen.</span><span class="sxs-lookup"><span data-stu-id="7519f-129">The default port number is 443/TCP, which ensures that most remote firewalls will allow the traffic.</span></span> <span data-ttu-id="7519f-130">Das Ändern der Portwerte in (zum Beispiel) 5061/TCP für den Access-Edge, 444/TCP für den Webkonferenz-Edge und 443/TCP für den AV-Edge kann zu Problemen bei Remotebenutzern führen, bei denen eine Firewall, die Sie behindern, den Datenverkehr über 5061/TCP und 444/TCP nicht zulässt.</span><span class="sxs-lookup"><span data-stu-id="7519f-130">Changing the port values to (for example) 5061/TCP for the Access Edge, 444/TCP for the Web Conferencing Edge and 443/TCP for the AV Edge might cause problems for remote users where a firewall that they are behind does not allow the traffic over 5061/TCP and 444/TCP.</span></span> <span data-ttu-id="7519f-131">Darüber hinaus erleichtern drei unterschiedliche IP-Adressen die Problembehandlung, da Sie nach IP-Adressen filtern können.</span><span class="sxs-lookup"><span data-stu-id="7519f-131">Additionally, three distinct IP addresses makes troubleshooting easier due to being able to filter on IP address.</span></span>

    
    </div>
    
    <span data-ttu-id="7519f-132">Die öffentliche IP-Adresse des Zugriffs Rands ist primär mit dem Standardgateway auf den integrierten Router (10.45.16.1) eingestellt.</span><span class="sxs-lookup"><span data-stu-id="7519f-132">The Access Edge public IP address is primary with default gateway set to the integrated router (10.45.16.1).</span></span>
    
    <span data-ttu-id="7519f-133">Private IP-Adressen für Webkonferenzen und A/V-Edge sind zusätzliche IP-Adressen im Abschnitt **erweitert** der Eigenschaften von **Internet Protocol Version 4 (TCP/IPv4)** und **Internet Protocol Version 6 (TCP/IPv6)** der Eigenschaften für den **lokalen Verbindungsbereich** in Windows Server.</span><span class="sxs-lookup"><span data-stu-id="7519f-133">Web conferencing and A/V Edge private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>

  - <span data-ttu-id="7519f-134">**Netzwerkadapter 2 Knoten 2 (externe Schnittstelle)**</span><span class="sxs-lookup"><span data-stu-id="7519f-134">**Network adapter 2 Node 2 (External Interface)**</span></span>
    
    <span data-ttu-id="7519f-135">Diesem Netzwerkadapter werden drei private IP-Adressen zugewiesen, beispielsweise 10.45.16.11 für Access Edge, 10.45.16.21 for Web Conferencing Edge, 10.45.16.31 für AV Edge.</span><span class="sxs-lookup"><span data-stu-id="7519f-135">Three private IP addresses are assigned to this network adapter, for example 10.45.16.11 for Access Edge, 10.45.16.21 for Web Conferencing Edge, 10.45.16.31 for AV Edge.</span></span>
    
    <span data-ttu-id="7519f-136">Die öffentliche IP-Adresse des Zugriffs Rands ist primär mit dem Standardgateway auf den integrierten Router (10.45.16.1) eingestellt.</span><span class="sxs-lookup"><span data-stu-id="7519f-136">The Access Edge public IP address is primary with default gateway set to the integrated router (10.45.16.1).</span></span>
    
    <span data-ttu-id="7519f-137">Private IP-Adressen für Webkonferenzen und A/V-Edge sind zusätzliche IP-Adressen im Abschnitt **erweitert** der Eigenschaften von **Internet Protocol Version 4 (TCP/IPv4)** und **Internet Protocol Version 6 (TCP/IPv6)** der Eigenschaften für den **lokalen Verbindungsbereich** in Windows Server.</span><span class="sxs-lookup"><span data-stu-id="7519f-137">Web conferencing and A/V Edge private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="7519f-138">Die Konfiguration des Edge-Servers mit zwei Netzwerkadaptern ist eine von zwei Optionen.</span><span class="sxs-lookup"><span data-stu-id="7519f-138">Configuring the Edge Server with two network adapters is one of two options.</span></span> <span data-ttu-id="7519f-139">Die andere Option besteht darin, einen Netzwerkadapter für die interne Seite und drei Netzwerkadapter für die externe Seite des Edge-Servers zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="7519f-139">The other option is to use one network adapter for the internal side and three network adapters for the external side of the Edge Server.</span></span> <span data-ttu-id="7519f-140">Der Hauptvorteil dieser Option ist ein eindeutiger Netzwerkadapter pro Edgeserver und eine potenziell genauere Datensammlung, wenn eine Problembehandlung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="7519f-140">The main benefit of this option is a distinct network adapter per Edge Server service, and potentially more concise data collection when troubleshooting is necessary</span></span>



</div>

### <a name="dns-records-required-for-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat-example"></a><span data-ttu-id="7519f-141">DNS-Einträge für den skalierten konsolidierten Edge, DNS-Lastenausgleich mit privaten IP-Adressen mithilfe von NAT (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="7519f-141">DNS Records Required for Scaled Consolidated Edge, DNS Load Balancing with Private IP Addresses Using NAT (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7519f-142">Ort/Typ/Port</span><span class="sxs-lookup"><span data-stu-id="7519f-142">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="7519f-143">FQDN/DNS-Eintrag</span><span class="sxs-lookup"><span data-stu-id="7519f-143">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="7519f-144">IP-Adresse/FQDN</span><span class="sxs-lookup"><span data-stu-id="7519f-144">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="7519f-145">Karten/Kommentare</span><span class="sxs-lookup"><span data-stu-id="7519f-145">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7519f-146">Externer DNS/A</span><span class="sxs-lookup"><span data-stu-id="7519f-146">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="7519f-147">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7519f-147">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7519f-148">131.107.155.10 und 131.107.155.11</span><span class="sxs-lookup"><span data-stu-id="7519f-148">131.107.155.10 and 131.107.155.11</span></span></p></td>
<td><p><span data-ttu-id="7519f-149">Access Edge External Interface (Contoso) wiederholen Sie diese nach Bedarf für alle SIP-Domänen mit lync-aktivierten Benutzern.</span><span class="sxs-lookup"><span data-stu-id="7519f-149">Access Edge external interface (Contoso) Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7519f-150">Externer DNS/A</span><span class="sxs-lookup"><span data-stu-id="7519f-150">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="7519f-151">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7519f-151">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7519f-152">131.107.155.20 und 131.107.155.21</span><span class="sxs-lookup"><span data-stu-id="7519f-152">131.107.155.20 and 131.107.155.21</span></span></p></td>
<td><p><span data-ttu-id="7519f-153">Externe Schnittstelle für Webkonferenz-Edge</span><span class="sxs-lookup"><span data-stu-id="7519f-153">Web Conferencing Edge external interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7519f-154">Externer DNS/A</span><span class="sxs-lookup"><span data-stu-id="7519f-154">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="7519f-155">av.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7519f-155">av.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7519f-156">131.107.155.30 und 131.107.155.31</span><span class="sxs-lookup"><span data-stu-id="7519f-156">131.107.155.30 and 131.107.155.31</span></span></p></td>
<td><p><span data-ttu-id="7519f-157">Externe Schnittstelle A/V Edge</span><span class="sxs-lookup"><span data-stu-id="7519f-157">A/V Edge external interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7519f-158">Externer DNS/SRV/443</span><span class="sxs-lookup"><span data-stu-id="7519f-158">External DNS/SRV/443</span></span></p></td>
<td><p><span data-ttu-id="7519f-159">_sip._tls.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7519f-159">_sip._tls.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7519f-160">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7519f-160">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7519f-161">Access Edge-externe Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7519f-161">Access Edge external interface.</span></span> <span data-ttu-id="7519f-162">Erforderlich für die automatische Konfiguration von lync 2013-und lync 2010-Clients, um extern zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="7519f-162">Required for automatic configuration of Lync 2013 and Lync 2010 clients to work externally.</span></span> <span data-ttu-id="7519f-163">Wiederholen Sie diese Schritte für alle SIP-Domänen mit lync-aktivierten Benutzern.</span><span class="sxs-lookup"><span data-stu-id="7519f-163">Repeat as necessary for all SIP domains with Lync enabled users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7519f-164">Externer DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="7519f-164">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="7519f-165">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7519f-165">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7519f-166">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7519f-166">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7519f-167">Externe SIP-Access-Edge-Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="7519f-167">SIP Access Edge external interface.</span></span> <span data-ttu-id="7519f-168">Erforderlich für die automatische DNS-Ermittlung von Verbundpartnern, die als "zugelassene SIP-Domäne" bezeichnet werden (genannt Enhanced Federation in früheren Versionen).</span><span class="sxs-lookup"><span data-stu-id="7519f-168">Required for automatic DNS discovery of federated partners known as “Allowed SIP Domain” (called enhanced federation in previous releases).</span></span> <span data-ttu-id="7519f-169">Wiederholen Sie diese Schritte für alle SIP-Domänen mit lync-aktivierten Benutzern.</span><span class="sxs-lookup"><span data-stu-id="7519f-169">Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7519f-170">Internes DNS/A</span><span class="sxs-lookup"><span data-stu-id="7519f-170">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="7519f-171">lsedge.contoso.net</span><span class="sxs-lookup"><span data-stu-id="7519f-171">lsedge.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="7519f-172">172.25.33.10 und 172.25.33.11</span><span class="sxs-lookup"><span data-stu-id="7519f-172">172.25.33.10 and 172.25.33.11</span></span></p></td>
<td><p><span data-ttu-id="7519f-173">Konsolidierte Edge-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7519f-173">Consolidated Edge internal interface</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="records-required-for-federation"></a><span data-ttu-id="7519f-174">Für den Verbund erforderliche Datensätze</span><span class="sxs-lookup"><span data-stu-id="7519f-174">Records Required for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7519f-175">Ort/Typ/Port</span><span class="sxs-lookup"><span data-stu-id="7519f-175">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="7519f-176">FQDN</span><span class="sxs-lookup"><span data-stu-id="7519f-176">FQDN</span></span></th>
<th><span data-ttu-id="7519f-177">IP-Adresse/FQDN-Hosteintrag</span><span class="sxs-lookup"><span data-stu-id="7519f-177">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="7519f-178">Karten/Kommentare</span><span class="sxs-lookup"><span data-stu-id="7519f-178">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7519f-179">Externer DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="7519f-179">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="7519f-180">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7519f-180">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7519f-181">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7519f-181">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7519f-182">Die externe SIP-Schnittstelle für die automatische DNS-Erkennung Ihres Verbandes zu anderen potenziellen Verbundpartnern ist erforderlich und wird als "zugelassene SIP-Domänen" bezeichnet (so genannte erweiterte Föderation in früheren Versionen). Wiederholen Sie diese Schritte für alle SIP-Domänen mit lync-aktivierten Benutzern.</span><span class="sxs-lookup"><span data-stu-id="7519f-182">SIP Access Edge external interface Required for automatic DNS discovery of your federation to other potential federation partners, and is known as “Allowed SIP Domains” (called enhanced federation in previous releases).Repeat as necessary for all SIP domains with Lync enabled users</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="7519f-183">Dieser SRV-Eintrag ist für Mobilität und das Clearinghaus für Push-Benachrichtigungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="7519f-183">This SRV record is required for mobility and the push notification clearing house</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="7519f-184">DNS-Zusammenfassung – öffentliche Instant Messaging-Konnektivität</span><span class="sxs-lookup"><span data-stu-id="7519f-184">DNS Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7519f-185">Ort/Typ/Port</span><span class="sxs-lookup"><span data-stu-id="7519f-185">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="7519f-186">FQDN/DNS-Eintrag</span><span class="sxs-lookup"><span data-stu-id="7519f-186">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="7519f-187">IP-Adresse/FQDN</span><span class="sxs-lookup"><span data-stu-id="7519f-187">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="7519f-188">Karten/Kommentare</span><span class="sxs-lookup"><span data-stu-id="7519f-188">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7519f-189">Externer DNS/A</span><span class="sxs-lookup"><span data-stu-id="7519f-189">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="7519f-190">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7519f-190">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7519f-191">Access Edge Service-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="7519f-191">Access Edge service interface</span></span></p></td>
<td><p><span data-ttu-id="7519f-192">Access Edge External Interface (Contoso) wiederholen Sie diese nach Bedarf für alle SIP-Domänen mit lync-aktivierten Benutzern.</span><span class="sxs-lookup"><span data-stu-id="7519f-192">Access Edge external interface (Contoso)Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="7519f-193">DNS-Zusammenfassung für erweiterbares Messaging und Anwesenheits Protokoll</span><span class="sxs-lookup"><span data-stu-id="7519f-193">DNS Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7519f-194">Ort/Typ/Port</span><span class="sxs-lookup"><span data-stu-id="7519f-194">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="7519f-195">FQDN</span><span class="sxs-lookup"><span data-stu-id="7519f-195">FQDN</span></span></th>
<th><span data-ttu-id="7519f-196">IP-Adresse/FQDN-Hosteintrag</span><span class="sxs-lookup"><span data-stu-id="7519f-196">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="7519f-197">Karten/Kommentare</span><span class="sxs-lookup"><span data-stu-id="7519f-197">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7519f-198">Externer DNS/SRV/5269</span><span class="sxs-lookup"><span data-stu-id="7519f-198">External DNS/SRV/5269</span></span></p></td>
<td><p><span data-ttu-id="7519f-199">_xmpp-server._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7519f-199">_xmpp-server._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7519f-200">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="7519f-200">xmpp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="7519f-201">XMPP-Proxy-externe Schnittstelle im Access Edge-Dienst oder Edge-Pool. Wiederholen Sie diese Schritte für alle internen SIP-Domänen mit lync-aktivierten Benutzern, bei denen der Kontakt mit XMPP-Kontakten über die Konfiguration der Richtlinie für den externen Zugriff über eine globale Richtlinie, eine Website Richtlinie, in der sich der Benutzer befindet, oder die Benutzerrichtlinie, die auf den lync-aktivierten Benutzer angewendet wurde, zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="7519f-201">XMPP proxy external interface on the Access Edge service or Edge pool.Repeat as necessary for all internal SIP domains with Lync enabled users where contact with XMPP contacts is allowed through the configuration of the External Access Policy through a global policy, site policy where the user is located, or user policy applied to the Lync-enabled user.</span></span> <span data-ttu-id="7519f-202">Eine zulässige XMPP-Domäne muss auch in der XMPP-Föderationspartner-Richtlinie konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="7519f-202">An allowed XMPP domain must also be configured in the XMPP Federated Partners policy.</span></span> <span data-ttu-id="7519f-203">Weitere Informationen finden Sie in den Themen unter <strong>Siehe auch</strong> .</span><span class="sxs-lookup"><span data-stu-id="7519f-203">See topics in <strong>See Also</strong> for additional details</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7519f-204">Externer DNS/A</span><span class="sxs-lookup"><span data-stu-id="7519f-204">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="7519f-205">xmpp.contoso.com (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="7519f-205">xmpp.contoso.com (for example)</span></span></p></td>
<td><p><span data-ttu-id="7519f-206">IP-Adresse des Zugriffs-Edgedienst auf dem Edgeserver oder Edge-Pool, der XMPP-Proxy hostet</span><span class="sxs-lookup"><span data-stu-id="7519f-206">IP address of Access Edge service on your Edge Server or Edge pool hosting XMPP proxy</span></span></p></td>
<td><p><span data-ttu-id="7519f-207">Verweist auf den Access Edge-Dienst oder den Edge-Pool, der den XMPP-Proxydienst hostet.</span><span class="sxs-lookup"><span data-stu-id="7519f-207">Points to the Access Edge service or Edge pool that hosts the XMPP proxy service.</span></span> <span data-ttu-id="7519f-208">In der Regel verweist der von Ihnen erstellte SRV-Eintrag auf diesen Host-Eintrag (a oder AAAA).</span><span class="sxs-lookup"><span data-stu-id="7519f-208">Typically, the SRV record that you create will point to this host (A or AAAA) record</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7519f-209">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7519f-209">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

