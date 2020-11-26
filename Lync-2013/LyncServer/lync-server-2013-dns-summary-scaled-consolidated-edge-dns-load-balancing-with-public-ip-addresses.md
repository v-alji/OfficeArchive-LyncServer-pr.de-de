---
title: 'Lync Server 2013: DNS-Zusammenfassung für einen skalierten konsolidierten Edgeserver, DNS-Lastenausgleich mit öffentlichen IP-Adressen'
description: 'Lync Server 2013: DNS-Zusammenfassung – skalierter konsolidierter Edge, DNS-Lastenausgleich mit öffentlichen IP-Adressen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Scaled consolidated edge, DNS load balancing with public IP addresses
ms:assetid: dc8f096a-a0a4-4f71-8930-88ff8fc089d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205319(v=OCS.15)
ms:contentKeyID: 48185594
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ca88043b76365508ea00ca840e9a9fdcb0e270be
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429014"
---
# <a name="dns-summary---scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-in-lync-server-2013"></a><span data-ttu-id="64981-103">DNS-Zusammenfassung für einen skalierten konsolidierten Edgeserver, DNS-Lastenausgleich mit öffentlichen IP-Adressen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="64981-103">DNS summary - Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="64981-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="64981-104">

<span> </span></span></span>

<span data-ttu-id="64981-105">_**Letztes Änderungsdatum des Themas:** 2017-03-09_</span><span class="sxs-lookup"><span data-stu-id="64981-105">_**Topic Last Modified:** 2017-03-09_</span></span>

<span data-ttu-id="64981-106">Die Anforderungen für den DNS-Eintrag für den Remotezugriff auf lync Server 2013 sind im Vergleich zu Zertifikaten und Ports relativ einfach.</span><span class="sxs-lookup"><span data-stu-id="64981-106">DNS record requirements for remote access to Lync Server 2013 are fairly straightforward compared to those for certificates and ports.</span></span> <span data-ttu-id="64981-107">Darüber hinaus sind viele Datensätze optional, je nachdem, wie Sie Clients mit lync 2013 konfigurieren und ob Sie die Föderation aktivieren.</span><span class="sxs-lookup"><span data-stu-id="64981-107">Also, many records are optional, depending on how you configure clients running Lync 2013 and whether you enable federation.</span></span>

<span data-ttu-id="64981-108">Details zu den DNS-Anforderungen von lync 2013 finden Sie unter [Ermitteln der DNS-Anforderungen für lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="64981-108">For details about Lync 2013 DNS requirements, see [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="64981-109">Ausführliche Informationen zum Konfigurieren der automatischen Konfiguration von lync 2013-Clients, wenn das Split-Brain-DNS nicht konfiguriert ist, finden Sie im Abschnitt "automatische Konfiguration ohne geteilten Brain-DNS" unter [Ermitteln der DNS-Anforderungen für lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="64981-109">For details about configuring automatic configuration of Lync 2013 clients if split-brain DNS is not configured, see the "Automatic Configuration without Split Brain DNS" section in [Determine DNS requirements for Lync Server 2013](lync-server-2013-determine-dns-requirements.md).</span></span>

<span data-ttu-id="64981-110">Die folgende Tabelle enthält eine Zusammenfassung der DNS-Einträge, die für die Unterstützung der einzelnen konsolidierten Edge-Topologie erforderlich sind, die in der einzelnen konsolidierten Edge-Topologie-Abbildung dargestellt ist.</span><span class="sxs-lookup"><span data-stu-id="64981-110">The following table contains a summary of the DNS records that are required to support the single consolidated edge topology shown in the Single Consolidated Edge Topology figure.</span></span> <span data-ttu-id="64981-111">Beachten Sie, dass bestimmte DNS-Einträge nur für die automatische Konfiguration von lync 2013-Clients erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="64981-111">Note that certain DNS records are required only for automatic configuration of Lync 2013 clients.</span></span> <span data-ttu-id="64981-112">Wenn Sie beabsichtigen, Gruppenrichtlinienobjekte (Group Policy Objects, GPOs) zum Konfigurieren von lync-Clients zu verwenden, sind die zugehörigen Datensätze nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="64981-112">If you plan to use group policy objects (GPOs) to configure Lync clients, the associated records are not necessary.</span></span>

<div>

## <a name="important-edge-server-network-adapter-requirements"></a><span data-ttu-id="64981-113">Wichtig: Anforderungen des Edge-Server-Netzwerkadapters</span><span class="sxs-lookup"><span data-stu-id="64981-113">IMPORTANT: Edge Server Network Adapter Requirements</span></span>

<span data-ttu-id="64981-114">Um Routingprobleme zu vermeiden, stellen Sie sicher, dass Ihre Edgeserver mindestens zwei Netzwerkadapter aufweisen und dass das Standardgateway nur auf dem Netzwerkadapter festgesetzt ist, der der externen Schnittstelle zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="64981-114">To avoid routing issues, verify that there are at least two network adapters in your Edge Servers and that the default gateway is set only on the network adapter associated with the external interface.</span></span> <span data-ttu-id="64981-115">Beispielsweise würde das Standardgateway auf die externe Firewall verweisen, wie es in der Szenariogröße des skalierten konsolidierten Rands in der [skalierten konsolidierten Kante, dem DNS-Lastenausgleich mit öffentlichen IP-Adressen in lync Server 2013](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md) gezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="64981-115">For example, as shown in the Scaled Consolidated Edge Scenario figure in [Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013](lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md) , the default gateway would point to the external firewall.</span></span>

<span data-ttu-id="64981-116">Sie können zwei Netzwerkadapter auf jedem Edgeserver wie folgt konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="64981-116">You can configure two network adapters in each of your Edge Server as follows:</span></span>

  - <span data-ttu-id="64981-117">**Netzwerkadapter 1 – Knoten 1 (interne Schnittstelle)**</span><span class="sxs-lookup"><span data-stu-id="64981-117">**Network adapter 1 - Node 1 (Internal Interface)**</span></span>
    
    <span data-ttu-id="64981-118">Interne Schnittstelle mit zugewiesenem 172.25.33.10</span><span class="sxs-lookup"><span data-stu-id="64981-118">Internal interface with 172.25.33.10 assigned.</span></span>
    
    <span data-ttu-id="64981-119">Es wurde kein Standardgateway definiert.</span><span class="sxs-lookup"><span data-stu-id="64981-119">No default gateway is defined.</span></span>
    
    <span data-ttu-id="64981-120">Stellen Sie sicher, dass eine Route vom Netzwerk mit der Edge-internen Schnittstelle zu allen Netzwerken vorhanden ist, die Server mit lync Server 2013-oder lync Server 2013-Clients enthalten (beispielsweise von 172.25.33.0 bis 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="64981-120">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="64981-121">**Netzwerkadapter 1 – Knoten 2 (interne Schnittstelle)**</span><span class="sxs-lookup"><span data-stu-id="64981-121">**Network adapter 1 - Node 2 (Internal Interface)**</span></span>
    
    <span data-ttu-id="64981-122">Interne Schnittstelle mit zugewiesenem 172.25.33.11</span><span class="sxs-lookup"><span data-stu-id="64981-122">Internal interface with 172.25.33.11 assigned.</span></span>
    
    <span data-ttu-id="64981-123">Es wurde kein Standardgateway definiert.</span><span class="sxs-lookup"><span data-stu-id="64981-123">No default gateway is defined.</span></span>
    
    <span data-ttu-id="64981-124">Stellen Sie sicher, dass eine Route vom Netzwerk mit der Edge-internen Schnittstelle zu allen Netzwerken vorhanden ist, die Server mit lync Server 2013-oder lync Server 2013-Clients enthalten (beispielsweise von 172.25.33.0 bis 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="64981-124">Ensure that there is a route from the network containing the Edge internal interface to any networks that contain servers running Lync Server 2013 or Lync Server 2013 clients (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="64981-125">**Netzwerkadapter 2 Knoten 1 (externe Schnittstelle)**</span><span class="sxs-lookup"><span data-stu-id="64981-125">**Network adapter 2 Node 1 (External Interface)**</span></span>
    
    <span data-ttu-id="64981-126">Diesem Netzwerkadapter werden drei private IP-Adressen zugewiesen, beispielsweise 131.107.155.10 für Access Edge Service, 131.107.155.20 for Web Conferencing Edge Service, 131.107.155.30 für A/V-Edgedienst.</span><span class="sxs-lookup"><span data-stu-id="64981-126">Three private IP addresses are assigned to this network adapter, for example 131.107.155.10 for Access Edge service, 131.107.155.20 for Web Conferencing Edge service, 131.107.155.30 for A/V Edge service.</span></span>
    
    <span data-ttu-id="64981-127">Die öffentliche IP-Adresse des Zugriffs-Edge-Diensts ist primär mit dem Standardgateway auf den öffentlichen Router (131.107.155.1) eingestellt.</span><span class="sxs-lookup"><span data-stu-id="64981-127">The Access Edge service public IP address is primary with default gateway set to the public router (131.107.155.1).</span></span>
    
    <span data-ttu-id="64981-128">Web Conferencing Edge Service und A/V Edge Service private IP-Adressen sind zusätzliche IP-Adressen im **erweiterten** Abschnitt der Eigenschaften von **Internet Protocol Version 4 (TCP/IPv4)** und **Internet Protocol Version 6 (TCP/IPv6)** der **Eigenschaften der LAN-Verbindung** in Windows Server.</span><span class="sxs-lookup"><span data-stu-id="64981-128">Web Conferencing Edge service and A/V Edge service private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="64981-129">Es ist jedoch möglich, eine einzige IP-Adresse für alle drei Edge-Service-Interfaces zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="64981-129">It is possible, though not recommended, to use a single IP address for all three Edge service interfaces.</span></span> <span data-ttu-id="64981-130">Obwohl dadurch IP-Adressen gespeichert werden, sind für jeden Dienst unterschiedliche Portnummern erforderlich.</span><span class="sxs-lookup"><span data-stu-id="64981-130">Though this does save IP addresses, it requires different port numbers for each service.</span></span> <span data-ttu-id="64981-131">Die Standardportnummer ist 443/TCP, wodurch sichergestellt wird, dass die meisten Remote Firewalls den Datenverkehr zulassen.</span><span class="sxs-lookup"><span data-stu-id="64981-131">The default port number is 443/TCP, which ensures that most remote firewalls will allow the traffic.</span></span> <span data-ttu-id="64981-132">Das Ändern der Portwerte in (zum Beispiel) 5061/TCP für den Access-Edgedienst, 444/TCP für den Webkonferenz-Edgedienst und 443/TCP für den A/V-Edgedienst kann zu Problemen bei Remotebenutzern führen, bei denen eine Firewall, die Sie behindern, den Datenverkehr über 5061/TCP und 444/TCP nicht zulässt.</span><span class="sxs-lookup"><span data-stu-id="64981-132">Changing the port values to (for example) 5061/TCP for the Access Edge service, 444/TCP for the Web Conferencing Edge service and 443/TCP for the A/V Edge service might cause problems for remote users where a firewall that they are behind does not allow the traffic over 5061/TCP and 444/TCP.</span></span> <span data-ttu-id="64981-133">Darüber hinaus erleichtern drei unterschiedliche IP-Adressen die Problembehandlung, da Sie nach IP-Adressen filtern können.</span><span class="sxs-lookup"><span data-stu-id="64981-133">Additionally, three distinct IP addresses makes troubleshooting easier due to being able to filter on IP address.</span></span>

    
    </div>

  - <span data-ttu-id="64981-134">**Netzwerkadapter 2 Knoten 2 (externe Schnittstelle)**</span><span class="sxs-lookup"><span data-stu-id="64981-134">**Network adapter 2 Node 2 (External Interface)**</span></span>
    
    <span data-ttu-id="64981-135">Diesem Netzwerkadapter werden drei private IP-Adressen zugewiesen, beispielsweise 131.107.155.11 für Access Edge Service, 131.107.155.21 for Web Conferencing Edge Service, 131.107.155.31 für A/V-Edgedienst.</span><span class="sxs-lookup"><span data-stu-id="64981-135">Three private IP addresses are assigned to this network adapter, for example 131.107.155.11 for Access Edge service, 131.107.155.21 for Web Conferencing Edge service, 131.107.155.31 for A/V Edge service.</span></span>
    
    <span data-ttu-id="64981-136">Die öffentliche IP-Adresse des Zugriffs-Edge-Diensts ist primär mit dem Standardgateway auf den öffentlichen Router (131.107.155.1) eingestellt.</span><span class="sxs-lookup"><span data-stu-id="64981-136">The Access Edge service public IP address is primary with default gateway set to the public router (131.107.155.1).</span></span>
    
    <span data-ttu-id="64981-137">Web Conferencing Edge Service und A/V Edge Service private IP-Adressen sind zusätzliche IP-Adressen im **erweiterten** Abschnitt der Eigenschaften von **Internet Protocol Version 4 (TCP/IPv4)** und **Internet Protocol Version 6 (TCP/IPv6)** der **Eigenschaften der LAN-Verbindung** in Windows Server.</span><span class="sxs-lookup"><span data-stu-id="64981-137">Web Conferencing Edge service and A/V Edge service private IP addresses are additional IP addresses in the **Advanced** section of the properties of **Internet Protocol Version 4 (TCP/IPv4)** and **Internet Protocol Version 6 (TCP/IPv6)** of the **Local Area Connection Properties** in Windows Server.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="64981-138">Die Konfiguration des Edge-Servers mit zwei Netzwerkadaptern ist eine von zwei Optionen.</span><span class="sxs-lookup"><span data-stu-id="64981-138">Configuring the Edge Server with two network adapters is one of two options.</span></span> <span data-ttu-id="64981-139">Die andere Option besteht darin, einen Netzwerkadapter für die interne Seite und drei Netzwerkadapter für die externe Seite des Edge-Servers zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="64981-139">The other option is to use one network adapter for the internal side and three network adapters for the external side of the Edge Server.</span></span> <span data-ttu-id="64981-140">Der Hauptvorteil dieser Option ist ein eindeutiger Netzwerkadapter pro Edgeserver und eine potenziell genauere Datensammlung, wenn eine Problembehandlung erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="64981-140">The main benefit of this option is a distinct network adapter per Edge Server service, and potentially more concise data collection when troubleshooting is necessary</span></span>



</div>

### <a name="dns-records-required-for-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses-example"></a><span data-ttu-id="64981-141">DNS-Einträge, die für den skalierten konsolidierten Edge erforderlich sind, DNS-Lastenausgleich mit öffentlichen IP-Adressen (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="64981-141">DNS Records Required for Scaled Consolidated Edge, DNS Load Balancing with Public IP Addresses (Example)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="64981-142">Ort/Typ/Port</span><span class="sxs-lookup"><span data-stu-id="64981-142">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="64981-143">FQDN/DNS-Eintrag</span><span class="sxs-lookup"><span data-stu-id="64981-143">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="64981-144">IP-Adresse/FQDN</span><span class="sxs-lookup"><span data-stu-id="64981-144">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="64981-145">Karten/Kommentare</span><span class="sxs-lookup"><span data-stu-id="64981-145">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64981-146">Externer DNS/A</span><span class="sxs-lookup"><span data-stu-id="64981-146">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="64981-147">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="64981-147">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="64981-148">131.107.155.10 und 131.107.155.11</span><span class="sxs-lookup"><span data-stu-id="64981-148">131.107.155.10 and 131.107.155.11</span></span></p></td>
<td><p><span data-ttu-id="64981-149">Access Edge Service External Interface (Contoso) wiederholen Sie diese nach Bedarf für alle SIP-Domänen mit lync-aktivierten Benutzern.</span><span class="sxs-lookup"><span data-stu-id="64981-149">Access Edge service external interface (Contoso) Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64981-150">Externer DNS/A</span><span class="sxs-lookup"><span data-stu-id="64981-150">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="64981-151">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="64981-151">webcon.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="64981-152">131.107.155.20 und 131.107.155.21</span><span class="sxs-lookup"><span data-stu-id="64981-152">131.107.155.20 and 131.107.155.21</span></span></p></td>
<td><p><span data-ttu-id="64981-153">Web Conferencing Edge Service-externe Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="64981-153">Web Conferencing Edge service external interface</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64981-154">Externer DNS/A</span><span class="sxs-lookup"><span data-stu-id="64981-154">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="64981-155">av.contoso.com</span><span class="sxs-lookup"><span data-stu-id="64981-155">av.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="64981-156">131.107.155.30 und 131.107.155.31</span><span class="sxs-lookup"><span data-stu-id="64981-156">131.107.155.30 and 131.107.155.31</span></span></p></td>
<td><p><span data-ttu-id="64981-157">Externe Schnittstelle A/V Edge Service</span><span class="sxs-lookup"><span data-stu-id="64981-157">A/V Edge service external interface</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64981-158">Externer DNS/SRV/443</span><span class="sxs-lookup"><span data-stu-id="64981-158">External DNS/SRV/443</span></span></p></td>
<td><p><span data-ttu-id="64981-159">_sip._tls.contoso.com</span><span class="sxs-lookup"><span data-stu-id="64981-159">_sip._tls.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="64981-160">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="64981-160">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="64981-161">Access Edge Service-externe Schnittstelle.</span><span class="sxs-lookup"><span data-stu-id="64981-161">Access Edge service external interface.</span></span> <span data-ttu-id="64981-162">Erforderlich für die automatische Konfiguration von lync 2013-und lync 2010-Clients, um extern zu arbeiten.</span><span class="sxs-lookup"><span data-stu-id="64981-162">Required for automatic configuration of Lync 2013 and Lync 2010 clients to work externally.</span></span> <span data-ttu-id="64981-163">Wiederholen Sie diese Schritte für alle SIP-Domänen mit lync-aktivierten Benutzern.</span><span class="sxs-lookup"><span data-stu-id="64981-163">Repeat as necessary for all SIP domains with Lync enabled users.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="64981-164">Externer DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="64981-164">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="64981-165">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="64981-165">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="64981-166">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="64981-166">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="64981-167">Für die automatische DNS-Ermittlung von Verbundpartnern, die als "zugelassene SIP-Domäne" bezeichnet werden (genannt Enhanced Federation in früheren Versionen), ist die externe Schnittstelle des Zugriffs-Edge-Diensts erforderlich.</span><span class="sxs-lookup"><span data-stu-id="64981-167">Access Edge service external interface Required for automatic DNS discovery of federated partners known as “Allowed SIP Domain” (called enhanced federation in previous releases).</span></span> <span data-ttu-id="64981-168">Wiederholen Sie diese Schritte für alle SIP-Domänen mit lync-aktivierten Benutzern.</span><span class="sxs-lookup"><span data-stu-id="64981-168">Repeat as necessary for all SIP domains with Lync enabled users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64981-169">Internes DNS/A</span><span class="sxs-lookup"><span data-stu-id="64981-169">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="64981-170">lsedge.contoso.net</span><span class="sxs-lookup"><span data-stu-id="64981-170">lsedge.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="64981-171">172.25.33.10 und 172.25.33.11</span><span class="sxs-lookup"><span data-stu-id="64981-171">172.25.33.10 and 172.25.33.11</span></span></p></td>
<td><p><span data-ttu-id="64981-172">Konsolidierte Edge-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="64981-172">Consolidated Edge internal interface</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="records-required-for-federation"></a><span data-ttu-id="64981-173">Für den Verbund erforderliche Datensätze</span><span class="sxs-lookup"><span data-stu-id="64981-173">Records Required for Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="64981-174">Ort/Typ/Port</span><span class="sxs-lookup"><span data-stu-id="64981-174">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="64981-175">FQDN</span><span class="sxs-lookup"><span data-stu-id="64981-175">FQDN</span></span></th>
<th><span data-ttu-id="64981-176">IP-Adresse/FQDN-Hosteintrag</span><span class="sxs-lookup"><span data-stu-id="64981-176">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="64981-177">Karten/Kommentare</span><span class="sxs-lookup"><span data-stu-id="64981-177">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64981-178">Externer DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="64981-178">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="64981-179">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="64981-179">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="64981-180">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="64981-180">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="64981-181">Die externe Schnittstelle für den SIP-Zugriffs-Edgedienst ist für die automatische DNS-Erkennung Ihres Verbandes zu anderen potenziellen Verbundpartnern erforderlich und wird als "zugelassene SIP-Domänen" bezeichnet (genannt Enhanced Federation in früheren Versionen).</span><span class="sxs-lookup"><span data-stu-id="64981-181">SIP Access Edge service external interface Required for automatic DNS discovery of your federation to other potential federation partners, and is known as “Allowed SIP Domains” (called enhanced federation in previous releases).</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="64981-182">Wiederholen Sie diese Schritte für alle SIP-Domänen mit lync-aktivierten Benutzern und Microsoft lync Mobile-Clients, die entweder den Push-Benachrichtigungsdienst oder den Apple Push-Benachrichtigungsdienst verwenden.</span><span class="sxs-lookup"><span data-stu-id="64981-182">Repeat as necessary for all SIP domains with Lync enabled users and Microsoft Lync Mobile clients that use either the Push Notification Service or the Apple Push Notification service</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="64981-183">DNS-Zusammenfassung für erweiterbares Messaging und Anwesenheits Protokoll</span><span class="sxs-lookup"><span data-stu-id="64981-183">DNS Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="64981-184">Ort/Typ/Port</span><span class="sxs-lookup"><span data-stu-id="64981-184">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="64981-185">FQDN</span><span class="sxs-lookup"><span data-stu-id="64981-185">FQDN</span></span></th>
<th><span data-ttu-id="64981-186">IP-Adresse/FQDN-Hosteintrag</span><span class="sxs-lookup"><span data-stu-id="64981-186">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="64981-187">Karten/Kommentare</span><span class="sxs-lookup"><span data-stu-id="64981-187">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="64981-188">Externer DNS/SRV/5269</span><span class="sxs-lookup"><span data-stu-id="64981-188">External DNS/SRV/5269</span></span></p></td>
<td><p><span data-ttu-id="64981-189">_xmpp-server._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="64981-189">_xmpp-server._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="64981-190">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="64981-190">xmpp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="64981-191">XMPP-Proxy-externe Schnittstelle im Access Edge-Dienst oder Edge-Pool. Wiederholen Sie diese Schritte für alle internen SIP-Domänen mit lync-aktivierten Benutzern, bei denen der Kontakt mit XMPP-Kontakten über die Konfiguration der Richtlinie für den externen Zugriff über eine globale Richtlinie, eine Website Richtlinie, in der sich der Benutzer befindet, oder die Benutzerrichtlinie, die auf den lync-aktivierten Benutzer angewendet wurde, zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="64981-191">XMPP proxy external interface on the Access Edge service or Edge pool.Repeat as necessary for all internal SIP domains with Lync enabled users where contact with XMPP contacts is allowed through the configuration of the External Access Policy through a global policy, site policy where the user is located, or user policy applied to the Lync-enabled user.</span></span> <span data-ttu-id="64981-192">Eine zulässige XMPP-Domäne muss auch in der XMPP-Föderationspartner-Richtlinie konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="64981-192">An allowed XMPP domain must also be configured in the XMPP Federated Partners policy.</span></span> <span data-ttu-id="64981-193">Weitere Informationen finden Sie in den Themen unter <strong>Siehe auch</strong> .</span><span class="sxs-lookup"><span data-stu-id="64981-193">See topics in <strong>See Also</strong> for additional details</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="64981-194">Externer DNS/A</span><span class="sxs-lookup"><span data-stu-id="64981-194">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="64981-195">xmpp.contoso.com (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="64981-195">xmpp.contoso.com (for example)</span></span></p></td>
<td><p><span data-ttu-id="64981-196">IP-Adresse des Zugriffs-Edgedienst auf dem Edgeserver oder Edge-Pool, der XMPP-Proxy hostet</span><span class="sxs-lookup"><span data-stu-id="64981-196">IP address of Access Edge service on your Edge Server or Edge pool hosting XMPP proxy</span></span></p></td>
<td><p><span data-ttu-id="64981-197">Verweist auf den Access Edge-Dienst oder den Edge-Pool, der den XMPP-Proxydienst hostet.</span><span class="sxs-lookup"><span data-stu-id="64981-197">Points to the Access Edge service or Edge pool that hosts the XMPP proxy service.</span></span> <span data-ttu-id="64981-198">In der Regel verweist der von Ihnen erstellte SRV-Eintrag auf diesen Host-Eintrag (a oder AAAA).</span><span class="sxs-lookup"><span data-stu-id="64981-198">Typically, the SRV record that you create will point to this host (A or AAAA) record</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="64981-199">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="64981-199">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

