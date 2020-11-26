---
title: 'Lync Server 2013: DNS-Zusammenfassung für Reverseproxy'
description: 'Lync Server 2013: DNS Summary – Reverse Proxy.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Reverse proxy
ms:assetid: 3073affa-4d92-4453-9974-3a82ca0c6445
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204781(v=OCS.15)
ms:contentKeyID: 48183755
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dc2d806893786a11317be1eff9bfdc08c9230bf3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437721"
---
# <a name="dns-summary---reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="f33b3-103">DNS-Zusammenfassung für Reverseproxy in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f33b3-103">DNS summary - Reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f33b3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f33b3-104">

<span> </span></span></span>

<span data-ttu-id="f33b3-105">_**Letztes Änderungsdatum des Themas:** 2013-03-22_</span><span class="sxs-lookup"><span data-stu-id="f33b3-105">_**Topic Last Modified:** 2013-03-22_</span></span>

<span data-ttu-id="f33b3-106">Sie konfigurieren zwei Netzwerkadapter in Ihrem Reverse-Proxy wie folgt:</span><span class="sxs-lookup"><span data-stu-id="f33b3-106">You configure two network adapters in your reverse proxy as follows:</span></span>

<div>

## <a name="reverse-proxy-network-adapter-requirements"></a><span data-ttu-id="f33b3-107">Anforderungen des Reverse Proxy-Netzwerkadapters</span><span class="sxs-lookup"><span data-stu-id="f33b3-107">Reverse Proxy Network Adapter Requirements</span></span>

  - <span data-ttu-id="f33b3-108">Beispiel für **einen Netzwerkadapter 1 (interne Schnittstelle)**</span><span class="sxs-lookup"><span data-stu-id="f33b3-108">**Network adapter 1 (Internal Interface)** example</span></span>
    
    <span data-ttu-id="f33b3-109">Interne Schnittstelle mit zugewiesenem 172.25.33.40</span><span class="sxs-lookup"><span data-stu-id="f33b3-109">Internal interface with 172.25.33.40 assigned.</span></span>
    
    <span data-ttu-id="f33b3-110">Es wurde kein Standardgateway definiert.</span><span class="sxs-lookup"><span data-stu-id="f33b3-110">No default gateway is defined.</span></span>
    
    <span data-ttu-id="f33b3-111">Stellen Sie sicher, dass eine Route aus dem Netzwerk mit der internen Reverse Proxy-Schnittstelle zu allen Netzwerken vorhanden ist, die lync Server-Front-End-Pool Server enthalten (beispielsweise von 172.25.33.0 zu 192.168.10.0).</span><span class="sxs-lookup"><span data-stu-id="f33b3-111">Ensure there is a route from the network containing the reverse proxy internal interface to any networks that contain Lync Server Front End pool servers (for example, from 172.25.33.0 to 192.168.10.0).</span></span>

  - <span data-ttu-id="f33b3-112">Beispiel für **Netzwerkadapter 2 (externe Schnittstelle)**</span><span class="sxs-lookup"><span data-stu-id="f33b3-112">**Network adapter 2 (External Interface)** example</span></span>
    
    <span data-ttu-id="f33b3-113">Diesem Netzwerkadapter wird mindestens eine öffentliche IP-Adresse zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="f33b3-113">A minimum of one public IP address is assigned to this network adapter.</span></span>
    
    <span data-ttu-id="f33b3-114">Gateway wird definiert, um auf den Router oder die integrierte Firewall im äußeren Umkreis zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="f33b3-114">Gateway is defined to point to the router or integrated firewall in your outer perimeter.</span></span> <span data-ttu-id="f33b3-115">(10.45.16.1 in den Szenario-Beispielen)</span><span class="sxs-lookup"><span data-stu-id="f33b3-115">(10.45.16.1 in the scenario examples)</span></span>

### <a name="dns-records-required-for-reverse-proxy"></a><span data-ttu-id="f33b3-116">Für Reverse-Proxy erforderliche DNS-Einträge</span><span class="sxs-lookup"><span data-stu-id="f33b3-116">DNS Records Required for Reverse Proxy</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f33b3-117">Ort/Typ/Port</span><span class="sxs-lookup"><span data-stu-id="f33b3-117">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="f33b3-118">FQDN</span><span class="sxs-lookup"><span data-stu-id="f33b3-118">FQDN</span></span></th>
<th><span data-ttu-id="f33b3-119">IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="f33b3-119">IP address</span></span></th>
<th><span data-ttu-id="f33b3-120">Karten/Kommentare</span><span class="sxs-lookup"><span data-stu-id="f33b3-120">Maps to/comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f33b3-121">Externer DNS/A</span><span class="sxs-lookup"><span data-stu-id="f33b3-121">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="f33b3-122">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f33b3-122">webext.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f33b3-123">Zugewiesener Listener für extern veröffentlichte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f33b3-123">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="f33b3-124">Externe Webdienste aus der internen Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="f33b3-124">External web services from the internal deployment.</span></span> <span data-ttu-id="f33b3-125">Zusätzliche Datensätze können für alle Pools und Einzelserver für alle SIP-Domänen definiert und erstellt werden, die diesen Reverseproxy verwenden, und hat externe Webdienste definiert.</span><span class="sxs-lookup"><span data-stu-id="f33b3-125">Additional records can be defined and created for all pools and single servers for any SIP domain that will use this reverse proxy, and has defined external web services.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33b3-126">Externer DNS/A</span><span class="sxs-lookup"><span data-stu-id="f33b3-126">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="f33b3-127">webdirext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f33b3-127">webdirext.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f33b3-128">Zugewiesener Listener für extern veröffentlichte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f33b3-128">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="f33b3-129">Externe Webdienste für die Directors-oder Director-Pools in Ihrer Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="f33b3-129">External web services for the Directors or Director pools in your deployment.</span></span> <span data-ttu-id="f33b3-130">Sie können beliebig viele Directors definieren, da es verschiedene Directors gibt, die möglicherweise anderen SIP-Domänen zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="f33b3-130">You can define as many Directors as there are distinct Directors, of which may be associated with other SIP domains.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="f33b3-131">Das Definieren der DNS-Einträge für und die Veröffentlichung der Directors ist weder der Front-End-Pool noch die Entscheidung des Regisseurs.</span><span class="sxs-lookup"><span data-stu-id="f33b3-131">Defining the DNS records for and publishing the Directors is not an either the Front End pool or the Director decision.</span></span> <span data-ttu-id="f33b3-132">Sie müssen sowohl den Director als auch den Front-End-Pool externer Webdienste definieren und veröffentlichen, wenn Sie Directors verwenden.</span><span class="sxs-lookup"><span data-stu-id="f33b3-132">You must define and publish both the Director and the Front End pool external web services if you are using Directors.</span></span> <span data-ttu-id="f33b3-133">Bestimmte Datenverkehrstypen (für Authentifizierung und andere Verwendungszwecke) werden zuerst an den Director gesendet, wenn er in der Topologie definiert ist.</span><span class="sxs-lookup"><span data-stu-id="f33b3-133">Specific traffic types (for authentication and other uses) will be sent to the Director first, if it is defined in the topology.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33b3-134">Externer DNS/A</span><span class="sxs-lookup"><span data-stu-id="f33b3-134">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="f33b3-135">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f33b3-135">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f33b3-136">Zugewiesener Listener für extern veröffentlichte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f33b3-136">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="f33b3-137">Extern veröffentlichte Einwahlkonferenzen</span><span class="sxs-lookup"><span data-stu-id="f33b3-137">Dial-in conferencing published externally</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33b3-138">Externer DNS/A</span><span class="sxs-lookup"><span data-stu-id="f33b3-138">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="f33b3-139">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f33b3-139">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f33b3-140">Zugewiesener Listener für extern veröffentlichte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f33b3-140">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="f33b3-141">Extern veröffentlichte Konferenzen</span><span class="sxs-lookup"><span data-stu-id="f33b3-141">Conferences published externally</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f33b3-142">Externer DNS/A</span><span class="sxs-lookup"><span data-stu-id="f33b3-142">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="f33b3-143">officewebapps01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f33b3-143">officewebapps01.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f33b3-144">Zugeordneter Listener für Office Web Apps Server</span><span class="sxs-lookup"><span data-stu-id="f33b3-144">Assigned listener for Office Web Apps Server</span></span></p></td>
<td><p><span data-ttu-id="f33b3-145">Office Web Apps Server wird intern oder im Umkreis bereitgestellt und für den Zugriff auf externe Clients veröffentlicht</span><span class="sxs-lookup"><span data-stu-id="f33b3-145">Office Web Apps Server deployed internally or in the perimeter, and published for external client access</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f33b3-146">Externer DNS/A</span><span class="sxs-lookup"><span data-stu-id="f33b3-146">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="f33b3-147">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="f33b3-147">lyncdiscover.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="f33b3-148">Zugewiesener Listener für extern veröffentlichte Ressourcen</span><span class="sxs-lookup"><span data-stu-id="f33b3-148">Assigned listener for externally published resources</span></span></p></td>
<td><p><span data-ttu-id="f33b3-149">Lync erkennt externen Eintrag für extern veröffentlichte AutoErmittlung und umfasst Mobilität, Microsoft lync Web App und Scheduler Web App</span><span class="sxs-lookup"><span data-stu-id="f33b3-149">Lync Discover External record for externally published AutoDiscover, and includes Mobility, Microsoft Lync Web App, and scheduler Web app</span></span></p></td>
</tr><span data-ttu-id="f33b3-150">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f33b3-150">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

