---
title: Beispiel für die Erfassung Ihrer Anforderungen für die Anrufsteuerung
description: Beispiel für die Erfassung Ihrer Anforderungen für die Anrufsteuerung.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Example of gathering your requirements for call admission control
ms:assetid: 3363ac53-b7c4-4a59-aea1-b2f3ee016ae1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425827(v=OCS.15)
ms:contentKeyID: 48183820
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 25c0b450070bda62c2610d98cfff8c8cd16ad2af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428498"
---
# <a name="example-gathering-your-requirements-for-call-admission-control-in-lync-server-2013"></a><span data-ttu-id="c49f8-103">Beispiel: Erfassen Ihrer Anforderungen für die Anrufsteuerung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c49f8-103">Example: Gathering your requirements for call admission control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c49f8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c49f8-104">

<span> </span></span></span>

<span data-ttu-id="c49f8-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="c49f8-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="c49f8-p101">Dieses Beispiel führt Sie Schritt für Schritt durch die Planung und Implementierung des Anrufsteuerungsdiensts (Call Admission Control, CAC). Bei diesem Verfahren werden die folgenden allgemeinen Aufgaben ausgeführt:</span><span class="sxs-lookup"><span data-stu-id="c49f8-p101">This example shows you how to plan for and implement call admission control (CAC). At a high level, this consists of the following activities:</span></span>

1.  <span data-ttu-id="c49f8-108">Identifizieren aller Netzwerkhubs und Backbones (als *Netzwerkregionen* bezeichnet).</span><span class="sxs-lookup"><span data-stu-id="c49f8-108">Identify all of your network hubs and backbones (known as *network regions*).</span></span>

2.  <span data-ttu-id="c49f8-109">Ermitteln Sie die lync Server Central-Website, die die CAC für jede netzwerkregion verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c49f8-109">Identify the Lync Server central site that will manage CAC for each network region.</span></span>

3.  <span data-ttu-id="c49f8-110">Identifizieren und Definieren der *Netzwerkstandorte*, die mit jeder Netzwerkregion verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="c49f8-110">Identify and define the *network sites* that are connected to each network region.</span></span>

4.  <span data-ttu-id="c49f8-111">Beschreiben Sie für jede Netzwerk Website, deren Verbindung mit dem WAN von der Bandbreite abhängig ist, die Bandbreitenkapazität der WAN-Verbindung und die Bandbreitenbeschränkungen, die der Netzwerkadministrator für den lync Server-Mediendatenverkehr festgelegt hat (falls zutreffend).</span><span class="sxs-lookup"><span data-stu-id="c49f8-111">For each network site whose connection to the WAN is bandwidth-constrained, describe the bandwidth capacity of the WAN connection and the bandwidth limits that to the network administrator has set for Lync Server media traffic, if applicable.</span></span> <span data-ttu-id="c49f8-112">Standorte mit WAN-Verbindungen ohne Bandbreiteneinschränkung müssen nicht einbezogen werden.</span><span class="sxs-lookup"><span data-stu-id="c49f8-112">You do not need to include sites whose connection to the WAN is not bandwidth-constrained.</span></span>

5.  <span data-ttu-id="c49f8-113">Zuordnen der einzelnen Subnetze in Ihrem Netzwerk zu einem Netzwerkstandort.</span><span class="sxs-lookup"><span data-stu-id="c49f8-113">Associate each subnet in your network with a network site.</span></span>

6.  <span data-ttu-id="c49f8-114">Zuordnen der Verbindungen zwischen den Netzwerkregionen.</span><span class="sxs-lookup"><span data-stu-id="c49f8-114">Map the links between the network regions.</span></span> <span data-ttu-id="c49f8-115">Beschreiben Sie für jeden Link die Bandbreitenkapazität sowie alle Einschränkungen, die der Netzwerkadministrator für den Mediendatenverkehr in lync Server festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="c49f8-115">For each link, describe its bandwidth capacity and any limits that the network administrator has placed on Lync Server media traffic.</span></span>

7.  <span data-ttu-id="c49f8-116">Definieren einer Route zwischen jedem Netzwerkregionenpaar.</span><span class="sxs-lookup"><span data-stu-id="c49f8-116">Define a route between every pair of network regions.</span></span>

<div>

## <a name="gather-the-required-information"></a><span data-ttu-id="c49f8-117">Sammeln der erforderlichen Informationen</span><span class="sxs-lookup"><span data-stu-id="c49f8-117">Gather the Required Information</span></span>

<span data-ttu-id="c49f8-118">Zur Vorbereitung der Anrufsteuerung müssen Sie die in den folgenden Schritten beschriebenen Informationen sammeln:</span><span class="sxs-lookup"><span data-stu-id="c49f8-118">To prepare for call admission control, gather the information described in the following steps:</span></span>

1.  <span data-ttu-id="c49f8-p104">Identifizieren Sie Ihre Netzwerkregionen. Eine Netzwerkregion repräsentiert einen Netzwerkbackbone oder einen Netzwerkhub.</span><span class="sxs-lookup"><span data-stu-id="c49f8-p104">Identify your network regions. A network region represents a network backbone or a network hub.</span></span>
    
    <span data-ttu-id="c49f8-p105">Ein Netzwerkbackbone oder ein Netzwerkhub ist Bestandteil der Computernetzwerkinfrastruktur, die verschiedene Komponenten im Netzwerk verbindet und einen Pfad für den Austausch von Informationen zwischen unterschiedlichen LANs oder Subnetzen bereitstellt. Ein Backbone kann unterschiedliche Netzwerke miteinander verknüpfen, von kleinen Standorten bis hin zu einem geografisch weit verteilten Bereich. Die Kapazität des Backbones ist in der Regel höher als die der Netzwerke, die mit ihm verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="c49f8-p105">A network backbone or a network hub is a part of computer network infrastructure that interconnects various pieces of network, providing a path for the exchange of information between different LANs or subnets. A backbone can tie together diverse networks, from a small location to a wide geographic area. The backbone's capacity is typically greater than that of the networks connected to it.</span></span>
    
    <span data-ttu-id="c49f8-p106">Die hier vorgestellte Beispieltopologie umfasst drei Netzwerkregionen: Nordamerika, EMEA und APAC. Eine Netzwerkregion enthält verschiedene Netzwerkstandorte. Arbeiten Sie mit Ihrem Netzwerkadministrator zusammen, um die Netzwerkregionen für Ihr Unternehmen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="c49f8-p106">Our example topology has three network regions: North America, EMEA, and APAC. A network region contains a collection of network sites. Work with your network administrator to define the network regions for your enterprise.</span></span>

2.  <span data-ttu-id="c49f8-127">Identifizieren Sie den zentralen Standort, dem jede Netzwerkregion zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c49f8-127">Identify each network region’s associated central site.</span></span> <span data-ttu-id="c49f8-128">Eine zentrale Website enthält mindestens einen Front-End-Server und ist die lync Server-Bereitstellung, die CAC für den gesamten Mediendatenverkehr verwaltet, der die WAN-Verbindung des Netzwerkbereichs durchläuft.</span><span class="sxs-lookup"><span data-stu-id="c49f8-128">A central site contains at least one Front End Server and is the Lync Server deployment that will manage CAC for all media traffic that passes through the network region’s WAN connection.</span></span>
    
    <span data-ttu-id="c49f8-129">**Beispielunternehmensnetzwerk mit drei Netzwerkregionen**</span><span class="sxs-lookup"><span data-stu-id="c49f8-129">**An example enterprise network divided into three network regions**</span></span>
    
    <span data-ttu-id="c49f8-130">![Beispiel für eine Netzwerktopologie mit 3 netzwerkregionen](images/Gg425827.08937347-250f-488f-ba5f-c256e6afcd8b(OCS.15).jpg "Beispiel für eine Netzwerktopologie mit 3 netzwerkregionen")</span><span class="sxs-lookup"><span data-stu-id="c49f8-130">![Network Topology Example with 3 Network Regions](images/Gg425827.08937347-250f-488f-ba5f-c256e6afcd8b(OCS.15).jpg "Network Topology Example with 3 Network Regions")</span></span>  
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="c49f8-131">Ein MPLS-Netzwerk (Multiprotocol Label Switching) sollte als Netzwerkregion abgebildet werden, bei der jeder geografische Standort über einen entsprechenden Netzwerkstandort verfügt.</span><span class="sxs-lookup"><span data-stu-id="c49f8-131">A Multiprotocol Label Switching (MPLS) network should be represented as a network region in which each geographic location has a corresponding network site.</span></span> <span data-ttu-id="c49f8-132">Ausführliche Informationen finden Sie in der Planungsdokumentation unter dem Thema "<A href="lync-server-2013-call-admission-control-on-an-mpls-network.md">Anrufsteuerung in einem MPLS-Netzwerk mit lync Server 2013</A>".</span><span class="sxs-lookup"><span data-stu-id="c49f8-132">For details, see the “<A href="lync-server-2013-call-admission-control-on-an-mpls-network.md">Call admission control on an MPLS network with Lync Server 2013</A>” topic in the Planning documentation.</span></span>

    
    </div>
    
    <span data-ttu-id="c49f8-133">In der vorhergehenden Beispiel-Netzwerktopologie gibt es drei netzwerkregionen, die jeweils einen zentralen lync Server-Standort aufweisen, der CAC verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c49f8-133">In the preceding example network topology, there are three network regions, each with a Lync Server central site that manages CAC.</span></span> <span data-ttu-id="c49f8-134">Der geeignete zentrale Standort für eine Netzwerkregion wird nach geografischer Nähe ausgewählt.</span><span class="sxs-lookup"><span data-stu-id="c49f8-134">The appropriate central site for a network region is chosen by the geographic vicinity.</span></span> <span data-ttu-id="c49f8-135">Da innerhalb der Netzwerkregionen das Aufkommen an Mediendatenverkehr am höchsten ist, führt die Festlegung nach geografischer Nähe zu einer eigenständigen Konfiguration, die auch dann noch funktionsfähig ist, wenn andere zentrale Standorte ausfallen.</span><span class="sxs-lookup"><span data-stu-id="c49f8-135">Because media traffic will be heaviest within network regions, the ownership by geographic vicinity makes it self-contained and will continue to be functional even if other central sites become unavailable.</span></span>
    
    <span data-ttu-id="c49f8-136">In diesem Beispiel ist eine lync Server-Bereitstellung mit dem Namen Chicago der zentrale Standort für die Region Nordamerika.</span><span class="sxs-lookup"><span data-stu-id="c49f8-136">In this example, a Lync Server deployment named Chicago is the central site for the North America region.</span></span>
    
    <span data-ttu-id="c49f8-137">Alle lync-Benutzer in Nordamerika sind in der Chicago-Bereitstellung auf Servern verwaltet.</span><span class="sxs-lookup"><span data-stu-id="c49f8-137">All Lync users in North America are homed on servers in the Chicago deployment.</span></span> <span data-ttu-id="c49f8-138">Die folgende Tabelle zeigt die zentralen Standorte für alle drei Netzwerkregionen.</span><span class="sxs-lookup"><span data-stu-id="c49f8-138">The following table shows central sites for all three network regions.</span></span>
    
    ### <a name="network-regions-and-their-associated-central-sites"></a><span data-ttu-id="c49f8-139">Netzwerkregionen und zugeordnete zentrale Standorte</span><span class="sxs-lookup"><span data-stu-id="c49f8-139">Network Regions and their Associated Central Sites</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c49f8-140">Netzwerkregion</span><span class="sxs-lookup"><span data-stu-id="c49f8-140">Network Region</span></span></th>
    <th><span data-ttu-id="c49f8-141">Zentraler Standort</span><span class="sxs-lookup"><span data-stu-id="c49f8-141">Central Site</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="c49f8-142">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-142">North America</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-143">Chicago</span><span class="sxs-lookup"><span data-stu-id="c49f8-143">Chicago</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c49f8-144">EMEA</span><span class="sxs-lookup"><span data-stu-id="c49f8-144">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-145">London</span><span class="sxs-lookup"><span data-stu-id="c49f8-145">London</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="c49f8-146">APAC</span><span class="sxs-lookup"><span data-stu-id="c49f8-146">APAC</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-147">Peking</span><span class="sxs-lookup"><span data-stu-id="c49f8-147">Beijing</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="c49f8-148">Je nach lync Server-Topologie kann derselbe zentrale Standort mehreren netzwerkregionen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="c49f8-148">Depending on your Lync Server topology, the same central site can be assigned to multiple network regions.</span></span>

    
    </div>

3.  <span data-ttu-id="c49f8-p111">Identifizieren Sie für jede Netzwerkregion alle Netzwerkstandorte (Büros oder Zweigstellen), für deren WAN-Verbindungen keine Bandbreiteneinschränkungen gelten. Da diese Standorte keine Bandbreiteneinschränkungen aufweisen, müssen keine Richtlinien für die Anrufsteuerung auf sie angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="c49f8-p111">For each network region, identify all of the network sites (offices or locations) whose WAN connections are not bandwidth-constrained. Because these sites are not bandwidth constrained, you do not need to apply CAC bandwidth policies to them.</span></span>
    
    <span data-ttu-id="c49f8-151">Im Beispiel in der folgenden Tabelle gibt es drei Netzwerkstandorte, deren WAN-Verbindungen keine Bandbreiteneinschränkungen aufweisen: „New York“, „Chicago“ und „Detroit“.</span><span class="sxs-lookup"><span data-stu-id="c49f8-151">In the example shown in the following table, three network sites do not have bandwidth-constrained WAN links: New York, Chicago, and Detroit.</span></span>
    
    ### <a name="network-sites-not-constrained-by-wan-bandwidth"></a><span data-ttu-id="c49f8-152">Netzwerkstandorte ohne Einschränkungen in Bezug auf die WAN-Bandbreite</span><span class="sxs-lookup"><span data-stu-id="c49f8-152">Network Sites not Constrained by WAN Bandwidth</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c49f8-153">Netzwerkstandort</span><span class="sxs-lookup"><span data-stu-id="c49f8-153">Network Site</span></span></th>
    <th><span data-ttu-id="c49f8-154">Netzwerkregion</span><span class="sxs-lookup"><span data-stu-id="c49f8-154">Network Region</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="c49f8-155">New York</span><span class="sxs-lookup"><span data-stu-id="c49f8-155">New York</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-156">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-156">North America</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c49f8-157">Chicago</span><span class="sxs-lookup"><span data-stu-id="c49f8-157">Chicago</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-158">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-158">North America</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="c49f8-159">Detroit</span><span class="sxs-lookup"><span data-stu-id="c49f8-159">Detroit</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-160">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-160">North America</span></span></p></td>
    </tr>
    </tbody>
    </table>


4.  <span data-ttu-id="c49f8-161">Identifizieren Sie für jede Netzwerkregion alle Netzwerkstandorte, die über WAN-Verbindungen mit Bandbreiteneinschränkungen eine Verbindung mit der Netzwerkregion herstellen.</span><span class="sxs-lookup"><span data-stu-id="c49f8-161">For each network region, identify all of the network sites that connect to the network region through bandwidth-constrained WAN links.</span></span>
    
    <span data-ttu-id="c49f8-162">Um die Audio- und Videoqualität besser sicherstellen zu können, wird für diese Netzwerkstandorte mit Bandbreiteneinschränkungen empfohlen, die WAN-Verbindungen zu überwachen und Richtlinien für die Anrufsteuerung anzuwenden, um den Mediendatenverkehr (Sprache oder Video) von und zu der Netzwerkregion zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="c49f8-162">To help ensure audio and video quality, we recommend that these bandwidth-constrained network sites have their WANs monitored and CAC bandwidth policies that limit media (voice or video) traffic flow to and from the network region.</span></span>
    
    <span data-ttu-id="c49f8-163">Im Beispiel in der folgenden Tabelle sind drei Netzwerkstandorte vorhanden, deren WAN-Bandbreite eingeschränkt ist: „Portland“, „Reno“ und „Albuquerque“.</span><span class="sxs-lookup"><span data-stu-id="c49f8-163">In the example shown in the following table, there are three network sites that are constrained by WAN bandwidth: Portland, Reno and Albuquerque.</span></span>
    
    ### <a name="network-sites-constrained-by-wan-bandwidth"></a><span data-ttu-id="c49f8-164">Netzwerkstandorte mit Einschränkungen in Bezug auf die WAN-Bandbreite</span><span class="sxs-lookup"><span data-stu-id="c49f8-164">Network Sites Constrained by WAN Bandwidth</span></span>
    
    <table>
    <colgroup>
    <col style="width: 50%" />
    <col style="width: 50%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c49f8-165">Netzwerkstandort</span><span class="sxs-lookup"><span data-stu-id="c49f8-165">Network Site</span></span></th>
    <th><span data-ttu-id="c49f8-166">Netzwerkregion</span><span class="sxs-lookup"><span data-stu-id="c49f8-166">Network Region</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="c49f8-167">Albuquerque</span><span class="sxs-lookup"><span data-stu-id="c49f8-167">Albuquerque</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-168">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-168">North America</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c49f8-169">Reno</span><span class="sxs-lookup"><span data-stu-id="c49f8-169">Reno</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-170">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-170">North America</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="c49f8-171">Portland</span><span class="sxs-lookup"><span data-stu-id="c49f8-171">Portland</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-172">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-172">North America</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
    <span data-ttu-id="c49f8-173">**Anrufsteuerung in der Netzwerkregion „Nordamerika“ mit drei Netzwerkstandorten, die keine Bandbreiteneinschränkung aufweisen (Chicago, New York und Detroit), und drei Netzwerkstandorten mit eingeschränkter WAN-Bandbreite (Portland, Reno und Albuquerque)**</span><span class="sxs-lookup"><span data-stu-id="c49f8-173">**CAC network region North America with three network sites that are unconstrained by bandwidth (Chicago, New York, and Detroit) and three network sites that are constrained by WAN bandwidth (Portland, Reno, and Albuquerque)**</span></span>
    
    <span data-ttu-id="c49f8-174">![Beispiel für Netzwerk Websites, die durch WAN-Bandbreite beschränkt sind](images/Gg425827.d9d1f231-db4d-4dd7-8fbc-eb0b6d1e705d(OCS.15).jpg "Beispiel für Netzwerk Websites, die durch WAN-Bandbreite beschränkt sind")</span><span class="sxs-lookup"><span data-stu-id="c49f8-174">![Example network sites constrained by WAN bandwidth](images/Gg425827.d9d1f231-db4d-4dd7-8fbc-eb0b6d1e705d(OCS.15).jpg "Example network sites constrained by WAN bandwidth")</span></span>  

5.  <span data-ttu-id="c49f8-175">Ermitteln Sie für jede WAN-Verbindung mit eingeschränkter Bandbreite die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="c49f8-175">For each bandwidth-constrained WAN link, determine the following:</span></span>
    
      - <span data-ttu-id="c49f8-176">Die gesamte Bandbreiteneinschränkung, die Sie für alle gleichzeitigen Audiositzungen festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="c49f8-176">Overall bandwidth limit that you want to set for all concurrent audio sessions.</span></span> <span data-ttu-id="c49f8-177">Wenn diese Grenze durch eine neue Audiositzung überschritten wird, lässt Lync Server den Start der Sitzung nicht zu.</span><span class="sxs-lookup"><span data-stu-id="c49f8-177">If a new audio session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="c49f8-p113">Die Bandbreiteneinschränkung, die Sie für jede einzelne Audiositzung festlegen möchten. Die standardmäßige Bandbreiteneinschränkung bei der Anrufsteuerung ist auf 175 KBit/s festgelegt, sie kann jedoch vom Administrator geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c49f8-p113">Bandwidth limit that you want to set for each individual audio session. The default CAC bandwidth limit is 175 kbps, but it can be modified by the administrator.</span></span>
    
      - <span data-ttu-id="c49f8-180">Die gesamte Bandbreiteneinschränkung, die Sie für alle gleichzeitigen Videositzungen festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="c49f8-180">Overall bandwidth limit that you want to set for all concurrent video sessions.</span></span> <span data-ttu-id="c49f8-181">Wenn diese Grenze durch eine neue Videositzung überschritten wird, lässt Lync Server den Start der Sitzung nicht zu.</span><span class="sxs-lookup"><span data-stu-id="c49f8-181">If a new video session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="c49f8-p115">Die Bandbreiteneinschränkung, die Sie für jede einzelne Videositzung festlegen möchten. Die standardmäßige Bandbreiteneinschränkung bei der Anrufsteuerung ist auf 700 KBit/s festgelegt, sie kann jedoch vom Administrator geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c49f8-p115">Bandwidth limit that you want to set for each individual video session. The default CAC bandwidth limit is 700 kbps, but it can be modified by the administrator.</span></span>
    
    ### <a name="network-sites-with-wan-bandwidth-constraint-information-bandwidth-in-kbps"></a><span data-ttu-id="c49f8-184">Netzwerkstandorte mit Informationen zur WAN-Bandbreiteneinschränkung (Bandbreite in KBit/s)</span><span class="sxs-lookup"><span data-stu-id="c49f8-184">Network Sites with WAN Bandwidth Constraint Information (Bandwidth in kbps)</span></span>
    
    <table style="width:100%;">
    <colgroup>
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    <col style="width: 14%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c49f8-185">Netzwerkstandort</span><span class="sxs-lookup"><span data-stu-id="c49f8-185">Network Site</span></span></th>
    <th><span data-ttu-id="c49f8-186">Netzwerkregion</span><span class="sxs-lookup"><span data-stu-id="c49f8-186">Network Region</span></span></th>
    <th><span data-ttu-id="c49f8-187">Grenzwert für Bandbreite</span><span class="sxs-lookup"><span data-stu-id="c49f8-187">BW Limit</span></span></th>
    <th><span data-ttu-id="c49f8-188">Grenzwert für Audio</span><span class="sxs-lookup"><span data-stu-id="c49f8-188">Audio Limit</span></span></th>
    <th><span data-ttu-id="c49f8-189">Grenzwert für Audiositzung</span><span class="sxs-lookup"><span data-stu-id="c49f8-189">Audio Session Limit</span></span></th>
    <th><span data-ttu-id="c49f8-190">Grenzwert für Video</span><span class="sxs-lookup"><span data-stu-id="c49f8-190">Video Limit</span></span></th>
    <th><span data-ttu-id="c49f8-191">Grenzwert für Videositzung</span><span class="sxs-lookup"><span data-stu-id="c49f8-191">Video Session Limit</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="c49f8-192">Albuquerque</span><span class="sxs-lookup"><span data-stu-id="c49f8-192">Albuquerque</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-193">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-193">North America</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-194">5.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-194">5,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-195">2.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-195">2,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-196">175</span><span class="sxs-lookup"><span data-stu-id="c49f8-196">175</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-197">1.400</span><span class="sxs-lookup"><span data-stu-id="c49f8-197">1,400</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-198">700</span><span class="sxs-lookup"><span data-stu-id="c49f8-198">700</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c49f8-199">Reno</span><span class="sxs-lookup"><span data-stu-id="c49f8-199">Reno</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-200">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-200">North America</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-201">10.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-201">10,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-202">4.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-202">4,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-203">175</span><span class="sxs-lookup"><span data-stu-id="c49f8-203">175</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-204">2.800</span><span class="sxs-lookup"><span data-stu-id="c49f8-204">2,800</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-205">700</span><span class="sxs-lookup"><span data-stu-id="c49f8-205">700</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="c49f8-206">Portland</span><span class="sxs-lookup"><span data-stu-id="c49f8-206">Portland</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-207">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-207">North America</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-208">5.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-208">5,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-209">4.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-209">4,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-210">175</span><span class="sxs-lookup"><span data-stu-id="c49f8-210">175</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-211">2.800</span><span class="sxs-lookup"><span data-stu-id="c49f8-211">2,800</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-212">700</span><span class="sxs-lookup"><span data-stu-id="c49f8-212">700</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c49f8-213">New York</span><span class="sxs-lookup"><span data-stu-id="c49f8-213">New York</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-214">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-214">North America</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-215">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-215">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-216">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-216">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-217">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-217">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-218">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-218">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-219">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-219">(no limit)</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="c49f8-220">Chicago</span><span class="sxs-lookup"><span data-stu-id="c49f8-220">Chicago</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-221">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-221">North America</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-222">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-222">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-223">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-223">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-224">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-224">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-225">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-225">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-226">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-226">(no limit)</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c49f8-227">Detroit</span><span class="sxs-lookup"><span data-stu-id="c49f8-227">Detroit</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-228">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-228">North America</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-229">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-229">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-230">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-230">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-231">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-231">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-232">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-232">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-233">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-233">(no limit)</span></span></p></td>
    </tr>
    </tbody>
    </table>


6.  <span data-ttu-id="c49f8-234">Geben Sie für jedes Subnetz in Ihrem Netzwerk den zugeordneten Netzwerkstandort an.</span><span class="sxs-lookup"><span data-stu-id="c49f8-234">For every subnet in your network, specify its associated network site.</span></span>
    
    <div>
    

    > [!IMPORTANT]
    > <span data-ttu-id="c49f8-p116">Jedes Subnetz in Ihrem Netzwerk muss einem Netzwerkstandort zugeordnet sein - selbst dann, wenn für den Netzwerkstandort keine Bandbreiteneinschränkungen gelten. Diese Anforderung gilt, da die Anrufsteuerung mithilfe von Subnetzinformationen ermittelt, an welchem Netzwerkstandort sich ein Endpunkt befindet. Wenn die Standorte beider Sitzungsteilnehmer ermittelt wurden, kann über die Anrufsteuerung festgestellt werden, ob genügend Bandbreite für einen Anruf vorhanden ist. Wird eine Sitzung über eine Verbindung ohne Bandbreiteneinschränkungen hergestellt, wird eine Warnung generiert.</span><span class="sxs-lookup"><span data-stu-id="c49f8-p116">Every subnet in your network must be associated with a network site, even if the network site is not bandwidth constrained. This is because call admission control uses subnet information to determine at which network site an endpoint is located. When the locations of both parties in the session are determined, call admission control can determine if there is sufficient bandwidth to establish a call. When a session is established over a link that has no bandwidth limits, an alert is generated.</span></span><BR><span data-ttu-id="c49f8-239">Wenn Sie A/V-Edgeserver (Audio/Video) bereitstellen, müssen die öffentlichen IP-Adressen der jeweiligen Edgeserver dem Netzwerkstandort zugeordnet werden, in dem der Edgeserver bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c49f8-239">If you deploy Audio/Video Edge Servers, the public IP addresses of each Edge Server must be associated with the network site where the Edge Server is deployed.</span></span> <span data-ttu-id="c49f8-240">Jede öffentliche IP-Adresse des A/V-Edgeservers muss in den Netzwerkkonfigurationseinstellungen als Subnetz mit der Subnetzmaske 32 hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="c49f8-240">Each public IP address of the A/V Edge Server must be added to your network configuration settings as a subnet with a subnet mask of 32.</span></span> <span data-ttu-id="c49f8-241">Wenn Sie beispielsweise A/V-Edgeserver in Chicago bereitstellen, müssen Sie für jede externe IP-Adresse dieser Server ein Subnetz mit der Subnetzmaske 32 erstellen und den Netzwerkstandort „Chicago“ diesen Subnetzen zuordnen.</span><span class="sxs-lookup"><span data-stu-id="c49f8-241">For example, if you deploy A/V Edge Servers in Chicago, then for each external IP address of those servers create a subnet with a subnet mask of 32 and associate network site Chicago with those subnets.</span></span> <span data-ttu-id="c49f8-242">Details zu öffentlichen IP-Adressen finden Sie unter <A href="lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md">Ermitteln der externen A/V-Firewall und Portanforderungen für lync Server 2013</A> in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="c49f8-242">For details about public IP addresses, see <A href="lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md">Determine external A/V firewall and port requirements for Lync Server 2013</A> in the Planning documentation.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="c49f8-p118">Es wird eine KHI-Warnung (Key Health Indicator) ausgegeben. Diese enthält eine Liste der IP-Adressen, die in Ihrem Netzwerk vorhanden, aber keinem Subnetz zugeordnet sind, oder gibt das Subnetz an, das die IP-Adressen enthält, jedoch keinem Netzwerkstandort zugeordnet ist. Diese Warnung wird innerhalb von 8 Stunden nur einmal angezeigt. Nachfolgend finden Sie die relevanten Warnungsinformationen und ein Beispiel:</span><span class="sxs-lookup"><span data-stu-id="c49f8-p118">A Key Health Indicator (KHI) alert is raised, specifying a list of IP addresses that are present in your network but are either not associated with a subnet, or the subnet that includes the IP addresses is not associated with a network site. This alert will not be raised more than once within an 8 hour period. The relevant alert information and an example are as follows:</span></span><BR><span data-ttu-id="c49f8-246"><STRONG>Quelle:</STRONG> CS-bandbreitenrichtliniendienst (Core)</span><span class="sxs-lookup"><span data-stu-id="c49f8-246"><STRONG>Source:</STRONG> CS Bandwidth Policy Service (Core)</span></span><BR><span data-ttu-id="c49f8-247"><STRONG>Ereignisnummer:</STRONG> 36034</span><span class="sxs-lookup"><span data-stu-id="c49f8-247"><STRONG>Event number:</STRONG> 36034</span></span><BR><span data-ttu-id="c49f8-248"><STRONG>Stufe:</STRONG> 2</span><span class="sxs-lookup"><span data-stu-id="c49f8-248"><STRONG>Level:</STRONG> 2</span></span><BR><span data-ttu-id="c49f8-249"><STRONG>Beschreibung:</STRONG> Die Subnetze für die folgenden IP-Adressen: die &lt; Liste der IP-Adressen &gt; ist entweder nicht konfiguriert, oder die Subnetze sind nicht mit einer Netzwerk Website verbunden.</span><span class="sxs-lookup"><span data-stu-id="c49f8-249"><STRONG>Description:</STRONG> The subnets for the following IP Addresses: &lt;List of IP Addresses&gt; are either not configured or the subnets are not associated to a network site.</span></span><BR><span data-ttu-id="c49f8-250"><STRONG>Ursache:</STRONG> Die Subnetze für die entsprechenden IP-Adressen fehlen in den Netzwerkkonfigurationseinstellungen, oder die Subnetze sind nicht mit einer Netzwerk Website verbunden.</span><span class="sxs-lookup"><span data-stu-id="c49f8-250"><STRONG>Cause:</STRONG> The subnets for the corresponding IP addresses are missing from the network configuration settings or the subnets are not associated to a network site.</span></span><BR><span data-ttu-id="c49f8-251"><STRONG>Auflösung:</STRONG> Fügen Sie den Netzwerkkonfigurationseinstellungen Subnetze hinzu, die der vorhergehenden Liste der IP-Adressen entsprechen, und ordnen Sie jedes Subnetz einer Netzwerk Website zu.</span><span class="sxs-lookup"><span data-stu-id="c49f8-251"><STRONG>Resolution:</STRONG> Add subnets corresponding to the preceding list of IP addresses into the network configuration settings and associate every subnet to a network site.</span></span><BR><span data-ttu-id="c49f8-p119">Wenn die Liste der IP-Adressen beispielsweise die Einträge 10.121.248.226 und 10.121.249.20 enthält, sind diese IP-Adressen entweder keinem Subnetz zugeordnet oder das zugeordnete Subnetz gehört keinem Netzwerkstandort an. Wenn die zugehörigen Subnetze für diese Adressen 10.121.248.0/24 und 10.121.249.0/24 lauten, können Sie das Problem wie folgt lösen:</span><span class="sxs-lookup"><span data-stu-id="c49f8-p119">For example, if the IP address list in the alert specifies 10.121.248.226 and 10.121.249.20, either these IP addresses are not associated with a subnet, or the subnet that they are associated with does not belong to a network site. If 10.121.248.0/24 and 10.121.249.0/24 are the corresponding subnets for these addresses, you can resolve this issue as follows:</span></span> 
    > <OL>
    > <LI>
    > <P><span data-ttu-id="c49f8-254">Stellen Sie sicher, dass die IP-Adresse 10.121.248.226 dem Subnetz 10.121.248.0/24 und die IP-Adresse 10.121.249.20 dem Subnetz 10.121.249.0/24 zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="c49f8-254">Be sure that IP address 10.121.248.226 is associated with the 10.121.248.0/24 subnet and IP address 10.121.249.20 is associated with the 10.121.249.0/24 subnet.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="c49f8-255">Stellen Sie sicher, dass die Subnetze 10.121.248.0/24 und 10.121.249.0/24 jeweils einem Netzwerkstandort zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="c49f8-255">Be sure that the 10.121.248.0/24 and 10.121.249.0/24 subnets are each associated with a network site.</span></span></P></LI></OL>

    
    </div>
    
    ### <a name="network-sites-and-associated-subnets-bandwidth-in-kbps"></a><span data-ttu-id="c49f8-256">Netzwerkstandorte und zugeordnete Subnetze (Bandbreite in KBit/s)</span><span class="sxs-lookup"><span data-stu-id="c49f8-256">Network Sites and Associated Subnets (Bandwidth in kbps)</span></span>
    
    <table>
    <colgroup>
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c49f8-257">Netzwerkstandort</span><span class="sxs-lookup"><span data-stu-id="c49f8-257">Network Site</span></span></th>
    <th><span data-ttu-id="c49f8-258">Netzwerkregion</span><span class="sxs-lookup"><span data-stu-id="c49f8-258">Network Region</span></span></th>
    <th><span data-ttu-id="c49f8-259">Grenzwert für Bandbreite</span><span class="sxs-lookup"><span data-stu-id="c49f8-259">BW Limit</span></span></th>
    <th><span data-ttu-id="c49f8-260">Grenzwert für Audio</span><span class="sxs-lookup"><span data-stu-id="c49f8-260">Audio Limit</span></span></th>
    <th><span data-ttu-id="c49f8-261">Grenzwert für Audiositzung</span><span class="sxs-lookup"><span data-stu-id="c49f8-261">Audio Session Limit</span></span></th>
    <th><span data-ttu-id="c49f8-262">Grenzwert für Video</span><span class="sxs-lookup"><span data-stu-id="c49f8-262">Video Limit</span></span></th>
    <th><span data-ttu-id="c49f8-263">Grenzwert für Videositzung</span><span class="sxs-lookup"><span data-stu-id="c49f8-263">Video Session Limit</span></span></th>
    <th><span data-ttu-id="c49f8-264">Subnetze</span><span class="sxs-lookup"><span data-stu-id="c49f8-264">Subnets</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="c49f8-265">Albuquerque</span><span class="sxs-lookup"><span data-stu-id="c49f8-265">Albuquerque</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-266">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-266">North America</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-267">5.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-267">5,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-268">2.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-268">2,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-269">175</span><span class="sxs-lookup"><span data-stu-id="c49f8-269">175</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-270">1.400</span><span class="sxs-lookup"><span data-stu-id="c49f8-270">1,400</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-271">700</span><span class="sxs-lookup"><span data-stu-id="c49f8-271">700</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-272">172.29.79.0/23, 157.57.215.0/25, 172.29.90.0/23, 172.29.80.0/24</span><span class="sxs-lookup"><span data-stu-id="c49f8-272">172.29.79.0/23, 157.57.215.0/25, 172.29.90.0/23, 172.29.80.0/24</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c49f8-273">Reno</span><span class="sxs-lookup"><span data-stu-id="c49f8-273">Reno</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-274">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-274">North America</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-275">10.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-275">10,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-276">4.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-276">4,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-277">175</span><span class="sxs-lookup"><span data-stu-id="c49f8-277">175</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-278">2.800</span><span class="sxs-lookup"><span data-stu-id="c49f8-278">2,800</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-279">700</span><span class="sxs-lookup"><span data-stu-id="c49f8-279">700</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-280">157.57.210.0/23, 172.28.151.128/25</span><span class="sxs-lookup"><span data-stu-id="c49f8-280">157.57.210.0/23, 172.28.151.128/25</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="c49f8-281">Portland</span><span class="sxs-lookup"><span data-stu-id="c49f8-281">Portland</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-282">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-282">North America</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-283">5.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-283">5,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-284">4.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-284">4,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-285">175</span><span class="sxs-lookup"><span data-stu-id="c49f8-285">175</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-286">2.800</span><span class="sxs-lookup"><span data-stu-id="c49f8-286">2,800</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-287">700</span><span class="sxs-lookup"><span data-stu-id="c49f8-287">700</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-288">172.29.77.0/24 10.71.108.0/24, 157.57.208.0/23</span><span class="sxs-lookup"><span data-stu-id="c49f8-288">172.29.77.0/24 10.71.108.0/24, 157.57.208.0/23</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c49f8-289">New York</span><span class="sxs-lookup"><span data-stu-id="c49f8-289">New York</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-290">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-290">North America</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-291">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-291">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-292">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-292">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-293">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-293">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-294">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-294">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-295">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-295">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-296">172.29.80.0/23, 157.57.216.0/25, 172.29.91.0/23, 172.29.81.0/24</span><span class="sxs-lookup"><span data-stu-id="c49f8-296">172.29.80.0/23, 157.57.216.0/25, 172.29.91.0/23, 172.29.81.0/24</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="c49f8-297">Chicago</span><span class="sxs-lookup"><span data-stu-id="c49f8-297">Chicago</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-298">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-298">North America</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-299">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-299">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-300">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-300">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-301">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-301">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-302">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-302">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-303">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-303">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-304">157.57.211.0/23, 172.28.152.128/25</span><span class="sxs-lookup"><span data-stu-id="c49f8-304">157.57.211.0/23, 172.28.152.128/25</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c49f8-305">Detroit</span><span class="sxs-lookup"><span data-stu-id="c49f8-305">Detroit</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-306">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-306">North America</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-307">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-307">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-308">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-308">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-309">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-309">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-310">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-310">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-311">(keine Begrenzung)</span><span class="sxs-lookup"><span data-stu-id="c49f8-311">(no limit)</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-312">172.29.78.0/24 10.71.109.0/24, 157.57.209.0/23</span><span class="sxs-lookup"><span data-stu-id="c49f8-312">172.29.78.0/24 10.71.109.0/24, 157.57.209.0/23</span></span></p></td>
    </tr>
    </tbody>
    </table>


7.  <span data-ttu-id="c49f8-313">In der lync Server-Anruf Zulassungs Steuerung werden die Verbindungen zwischen netzwerkregionen als *Regions Verknüpfungen* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c49f8-313">In Lync Server call admission control, the connections between network regions are called *region links*.</span></span> <span data-ttu-id="c49f8-314">Ermitteln Sie für jede Regionenverbindung, ebenso wie für die Netzwerkstandorte, die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="c49f8-314">For each region link, determine the following, just as you did for the network sites:</span></span>
    
      - <span data-ttu-id="c49f8-315">Die gesamte Bandbreiteneinschränkung, die Sie für alle gleichzeitigen Audiositzungen festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="c49f8-315">Overall bandwidth limit that you want to set for all concurrent audio sessions.</span></span> <span data-ttu-id="c49f8-316">Wenn diese Grenze durch eine neue Audiositzung überschritten wird, lässt Lync Server den Start der Sitzung nicht zu.</span><span class="sxs-lookup"><span data-stu-id="c49f8-316">If a new audio session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="c49f8-p122">Die Bandbreiteneinschränkung, die Sie für jede einzelne Audiositzung festlegen möchten. Die standardmäßige Bandbreiteneinschränkung bei der Anrufsteuerung ist auf 175 KBit/s festgelegt, sie kann jedoch vom Administrator geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c49f8-p122">Bandwidth limit that you want to set for each individual audio session. The default CAC bandwidth limit is 175 kbps, but it can be modified by the administrator.</span></span>
    
      - <span data-ttu-id="c49f8-319">Die gesamte Bandbreiteneinschränkung, die Sie für alle gleichzeitigen Videositzungen festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="c49f8-319">Overall bandwidth limit that you want to set for all concurrent video sessions.</span></span> <span data-ttu-id="c49f8-320">Wenn diese Grenze durch eine neue Videositzung überschritten wird, lässt Lync Server den Start der Sitzung nicht zu.</span><span class="sxs-lookup"><span data-stu-id="c49f8-320">If a new video session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="c49f8-p124">Die Bandbreiteneinschränkung, die Sie für jede einzelne Videositzung festlegen möchten. Die standardmäßige Bandbreiteneinschränkung bei der Anrufsteuerung ist auf 700 KBit/s festgelegt, sie kann jedoch vom Administrator geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c49f8-p124">Bandwidth limit that you want to set for each individual video session. The default CAC bandwidth limit is 700 kbps, but it can be modified by the administrator.</span></span>
    
    <span data-ttu-id="c49f8-323">**Netzwerkregionenverbindungen mit zugehörigen Bandbreiteneinschränkungen**</span><span class="sxs-lookup"><span data-stu-id="c49f8-323">**Network Region links with associated bandwidth limits**</span></span>
    
    <span data-ttu-id="c49f8-324">![Beispiel für Einschränkungen zwischen drei Regionen](images/Gg425827.25259afa-ee7c-4d26-bc41-92ba9cb56dec(OCS.15).jpg "Beispiel für Einschränkungen zwischen drei Regionen")</span><span class="sxs-lookup"><span data-stu-id="c49f8-324">![Example of Limitations between 3 Regions](images/Gg425827.25259afa-ee7c-4d26-bc41-92ba9cb56dec(OCS.15).jpg "Example of Limitations between 3 Regions")</span></span>  
    
    ### <a name="region-link-bandwidth-information-bandwidth-in-kbps"></a><span data-ttu-id="c49f8-325">Bandbreiteninformationen zu Regionenverbindungen (Bandbreite in KBit/s)</span><span class="sxs-lookup"><span data-stu-id="c49f8-325">Region Link Bandwidth Information (Bandwidth in kbps)</span></span>
    
    <table>
    <colgroup>
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c49f8-326">Name der Regionenverbindung</span><span class="sxs-lookup"><span data-stu-id="c49f8-326">Region Link Name</span></span></th>
    <th><span data-ttu-id="c49f8-327">Erste Region</span><span class="sxs-lookup"><span data-stu-id="c49f8-327">First Region</span></span></th>
    <th><span data-ttu-id="c49f8-328">Zweite Region</span><span class="sxs-lookup"><span data-stu-id="c49f8-328">Second Region</span></span></th>
    <th><span data-ttu-id="c49f8-329">Grenzwert für Bandbreite</span><span class="sxs-lookup"><span data-stu-id="c49f8-329">BW Limit</span></span></th>
    <th><span data-ttu-id="c49f8-330">Grenzwert für Audio</span><span class="sxs-lookup"><span data-stu-id="c49f8-330">Audio Limit</span></span></th>
    <th><span data-ttu-id="c49f8-331">Grenzwert für Audiositzung</span><span class="sxs-lookup"><span data-stu-id="c49f8-331">Audio Session Limit</span></span></th>
    <th><span data-ttu-id="c49f8-332">Grenzwert für Video</span><span class="sxs-lookup"><span data-stu-id="c49f8-332">Video Limit</span></span></th>
    <th><span data-ttu-id="c49f8-333">Grenzwert für Videositzung</span><span class="sxs-lookup"><span data-stu-id="c49f8-333">Video Session Limit</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="c49f8-334">NA-EMEA-LINK</span><span class="sxs-lookup"><span data-stu-id="c49f8-334">NA-EMEA-LINK</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-335">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-335">North America</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-336">EMEA</span><span class="sxs-lookup"><span data-stu-id="c49f8-336">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-337">50.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-337">50,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-338">20.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-338">20,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-339">175</span><span class="sxs-lookup"><span data-stu-id="c49f8-339">175</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-340">14.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-340">14,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-341">700</span><span class="sxs-lookup"><span data-stu-id="c49f8-341">700</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c49f8-342">EMEA-APAC-LINK</span><span class="sxs-lookup"><span data-stu-id="c49f8-342">EMEA-APAC-LINK</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-343">EMEA</span><span class="sxs-lookup"><span data-stu-id="c49f8-343">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-344">APAC</span><span class="sxs-lookup"><span data-stu-id="c49f8-344">APAC</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-345">25.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-345">25,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-346">10.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-346">10,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-347">175</span><span class="sxs-lookup"><span data-stu-id="c49f8-347">175</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-348">7.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-348">7,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-349">700</span><span class="sxs-lookup"><span data-stu-id="c49f8-349">700</span></span></p></td>
    </tr>
    </tbody>
    </table>


8.  <span data-ttu-id="c49f8-350">Definieren einer Route zwischen jedem Netzwerkregionenpaar.</span><span class="sxs-lookup"><span data-stu-id="c49f8-350">Define a route between every pair of network regions.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="c49f8-351">Für die Route zwischen den Regionen „Nordamerika“ und „APAC“ sind zwei Verbindungen erforderlich, da keine Region vorhanden ist, die die Regionen direkt miteinander verbindet.</span><span class="sxs-lookup"><span data-stu-id="c49f8-351">Two links are required for the route between the North America and APAC regions because there is no region link that directly connects them.</span></span>

    
    </div>
    
    ### <a name="region-routes"></a><span data-ttu-id="c49f8-352">Routen zwischen Regionen</span><span class="sxs-lookup"><span data-stu-id="c49f8-352">Region Routes</span></span>
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c49f8-353">Name der Regionenroute</span><span class="sxs-lookup"><span data-stu-id="c49f8-353">Region Route Name</span></span></th>
    <th><span data-ttu-id="c49f8-354">Erste Region</span><span class="sxs-lookup"><span data-stu-id="c49f8-354">First Region</span></span></th>
    <th><span data-ttu-id="c49f8-355">Zweite Region</span><span class="sxs-lookup"><span data-stu-id="c49f8-355">Second Region</span></span></th>
    <th><span data-ttu-id="c49f8-356">Regionenverbindungen</span><span class="sxs-lookup"><span data-stu-id="c49f8-356">Region Links</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="c49f8-357">NA-EMEA-ROUTE</span><span class="sxs-lookup"><span data-stu-id="c49f8-357">NA-EMEA-ROUTE</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-358">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-358">North America</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-359">EMEA</span><span class="sxs-lookup"><span data-stu-id="c49f8-359">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-360">NA-EMEA-LINK</span><span class="sxs-lookup"><span data-stu-id="c49f8-360">NA-EMEA-LINK</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="c49f8-361">EMEA-APAC-ROUTE</span><span class="sxs-lookup"><span data-stu-id="c49f8-361">EMEA-APAC-ROUTE</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-362">EMEA</span><span class="sxs-lookup"><span data-stu-id="c49f8-362">EMEA</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-363">APAC</span><span class="sxs-lookup"><span data-stu-id="c49f8-363">APAC</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-364">EMEA-APAC-LINK</span><span class="sxs-lookup"><span data-stu-id="c49f8-364">EMEA-APAC-LINK</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="c49f8-365">NA-APAC-ROUTE</span><span class="sxs-lookup"><span data-stu-id="c49f8-365">NA-APAC-ROUTE</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-366">Nordamerika</span><span class="sxs-lookup"><span data-stu-id="c49f8-366">North America</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-367">APAC</span><span class="sxs-lookup"><span data-stu-id="c49f8-367">APAC</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-368">NA-EMEA-LINK, EMEA-APAC-LINK</span><span class="sxs-lookup"><span data-stu-id="c49f8-368">NA-EMEA-LINK, EMEA-APAC-LINK</span></span></p></td>
    </tr>
    </tbody>
    </table>


9.  <span data-ttu-id="c49f8-369">Ermitteln Sie für jedes Netzwerkstandortpaar, das durch eine einzelne Verbindung direkt miteinander verbunden wird (als *standortübergreifende* Verbindung bezeichnet), die folgenden Informationen:</span><span class="sxs-lookup"><span data-stu-id="c49f8-369">For every pair of network sites that are directly connected by a single link (called an *inter-site* link), determine the following:</span></span>
    
      - <span data-ttu-id="c49f8-370">Die gesamte Bandbreiteneinschränkung, die Sie für alle gleichzeitigen Audiositzungen festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="c49f8-370">Overall bandwidth limit that you want to set for all concurrent audio sessions.</span></span> <span data-ttu-id="c49f8-371">Wenn diese Grenze durch eine neue Audiositzung überschritten wird, lässt Lync Server den Start der Sitzung nicht zu.</span><span class="sxs-lookup"><span data-stu-id="c49f8-371">If a new audio session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="c49f8-p126">Die Bandbreiteneinschränkung, die Sie für jede einzelne Audiositzung festlegen möchten. Die standardmäßige Bandbreiteneinschränkung bei der Anrufsteuerung ist auf 175 KBit/s festgelegt, sie kann jedoch vom Administrator geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c49f8-p126">Bandwidth limit that you want to set for each individual audio session. The default CAC bandwidth limit is 175 kbps, but it can be modified by the administrator.</span></span>
    
      - <span data-ttu-id="c49f8-374">Die gesamte Bandbreiteneinschränkung, die Sie für alle gleichzeitigen Videositzungen festlegen möchten.</span><span class="sxs-lookup"><span data-stu-id="c49f8-374">Overall bandwidth limit that you want to set for all concurrent video sessions.</span></span> <span data-ttu-id="c49f8-375">Wenn diese Grenze durch eine neue Videositzung überschritten wird, lässt Lync Server den Start der Sitzung nicht zu.</span><span class="sxs-lookup"><span data-stu-id="c49f8-375">If a new video session will cause this limit to be exceeded, Lync Server does not allow the session to start.</span></span>
    
      - <span data-ttu-id="c49f8-p128">Die Bandbreiteneinschränkung, die Sie für jede einzelne Videositzung festlegen möchten. Die standardmäßige Bandbreiteneinschränkung bei der Anrufsteuerung ist auf 700 KBit/s festgelegt, sie kann jedoch vom Administrator geändert werden.</span><span class="sxs-lookup"><span data-stu-id="c49f8-p128">Bandwidth limit that you want to set for each individual video session. The default CAC bandwidth limit is 700 kbps, but it can be modified by the administrator.</span></span>
    
    <span data-ttu-id="c49f8-378">**Anrufsteuerung in der Netzwerkregion „Nordamerika“ mit Anzeige der Bandbreitenkapazitäten und -einschränkungen für die standortübergreifende Verbindung zwischen Reno und Albuquerque**</span><span class="sxs-lookup"><span data-stu-id="c49f8-378">**CAC network region North America showing the bandwidth capacities and bandwidth limits for the inter-site link between Reno and Albuquerque**</span></span>
    
    <span data-ttu-id="c49f8-379">![Netzwerk Websites, die durch das WAN-Bandbreite-Beispiel beschränkt sind](images/Gg425827.063e5e1d-b6c8-4e8c-98db-c227c78f671d(OCS.15).jpg "Netzwerk Websites, die durch das WAN-Bandbreite-Beispiel beschränkt sind")</span><span class="sxs-lookup"><span data-stu-id="c49f8-379">![Network Sites Constrained by WAN Bandwidth example](images/Gg425827.063e5e1d-b6c8-4e8c-98db-c227c78f671d(OCS.15).jpg "Network Sites Constrained by WAN Bandwidth example")</span></span>  
    
    ### <a name="bandwidth-information-for-an-inter-site-link-between-two-network-sites-bandwidth-in-kbps"></a><span data-ttu-id="c49f8-380">Bandbreiteninformationen für eine standortübergreifende Verbindung zwischen zwei Netzwerkstandorten (Bandbreite in KBit/s)</span><span class="sxs-lookup"><span data-stu-id="c49f8-380">Bandwidth Information for an Inter-Site Link between Two Network Sites (Bandwidth in kbps)</span></span>
    
    <table>
    <colgroup>
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    <col style="width: 12%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="c49f8-381">Name der standortübergreifenden Verbindung</span><span class="sxs-lookup"><span data-stu-id="c49f8-381">Inter-Site Link Name</span></span></th>
    <th><span data-ttu-id="c49f8-382">Erster Standort</span><span class="sxs-lookup"><span data-stu-id="c49f8-382">First Site</span></span></th>
    <th><span data-ttu-id="c49f8-383">Zweiter Standort</span><span class="sxs-lookup"><span data-stu-id="c49f8-383">Second Site</span></span></th>
    <th><span data-ttu-id="c49f8-384">Grenzwert für Bandbreite</span><span class="sxs-lookup"><span data-stu-id="c49f8-384">BW Limit</span></span></th>
    <th><span data-ttu-id="c49f8-385">Grenzwert für Audio</span><span class="sxs-lookup"><span data-stu-id="c49f8-385">Audio Limit</span></span></th>
    <th><span data-ttu-id="c49f8-386">Grenzwert für Audiositzung</span><span class="sxs-lookup"><span data-stu-id="c49f8-386">Audio Session Limit</span></span></th>
    <th><span data-ttu-id="c49f8-387">Grenzwert für Video</span><span class="sxs-lookup"><span data-stu-id="c49f8-387">Video Limit</span></span></th>
    <th><span data-ttu-id="c49f8-388">Grenzwert für Videositzung</span><span class="sxs-lookup"><span data-stu-id="c49f8-388">Video Session Limit</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="c49f8-389">Reno-Albu-Intersite-Link</span><span class="sxs-lookup"><span data-stu-id="c49f8-389">Reno-Albu-Intersite-Link</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-390">Reno</span><span class="sxs-lookup"><span data-stu-id="c49f8-390">Reno</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-391">Albuquerque</span><span class="sxs-lookup"><span data-stu-id="c49f8-391">Albuquerque</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-392">20.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-392">20,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-393">12.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-393">12,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-394">175</span><span class="sxs-lookup"><span data-stu-id="c49f8-394">175</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-395">5.000</span><span class="sxs-lookup"><span data-stu-id="c49f8-395">5,000</span></span></p></td>
    <td><p><span data-ttu-id="c49f8-396">700</span><span class="sxs-lookup"><span data-stu-id="c49f8-396">700</span></span></p></td>
    </tr>
    </tbody>
    </table>


<div>

## <a name="next-steps"></a><span data-ttu-id="c49f8-397">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="c49f8-397">Next Steps</span></span>

<span data-ttu-id="c49f8-398">Nachdem Sie die erforderlichen Informationen gesammelt haben, können Sie die CAC-Bereitstellung entweder mithilfe der lync Server-Verwaltungsshell oder der lync Server-Systemsteuerung durchführen.</span><span class="sxs-lookup"><span data-stu-id="c49f8-398">After you have gathered the required information, you can perform CAC deployment either by using the Lync Server Management Shell or Lync Server Control Panel.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="c49f8-399">Obwohl Sie die meisten Netzwerk Konfigurationsaufgaben mithilfe der lync Server-Systemsteuerung ausführen können, müssen Sie zum Erstellen von Subnetzen und standortübergreifenden Links die lync Server-Verwaltungsshell verwenden.</span><span class="sxs-lookup"><span data-stu-id="c49f8-399">Although you can perform most network configuration tasks by using Lync Server Control Panel, to create subnets and intersite links, you must use Lync Server Management Shell.</span></span> <span data-ttu-id="c49f8-400">Ausführliche Informationen finden Sie in der Dokumentation zur lync Server-Verwaltungsshell für das Cmdlet <STRONG>New-CsNetworkSubnet</STRONG> und das Cmdlet <STRONG>New-CsNetworkIntersitePolicy</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="c49f8-400">For details, see the Lync Server Management Shell documentation for the <STRONG>New-CsNetworkSubnet</STRONG> cmdlet and the <STRONG>New-CsNetworkIntersitePolicy</STRONG> cmdlet.</span></span>



<span data-ttu-id="c49f8-401"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c49f8-401"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

