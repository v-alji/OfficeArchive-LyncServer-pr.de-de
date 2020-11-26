---
title: 'Lync Server 2013: Portzusammenfassung für DNS- und Hardwarelastenausgleich'
description: 'Lync Server 2013: Port Zusammenfassung – DNS und HLB Load Balanced.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - DNS and HLB load balanced
ms:assetid: b07c37e4-820e-46ee-a678-1da95d1b87af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205179(v=OCS.15)
ms:contentKeyID: 48185149
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be2e8204e792fd9c4718cb9171e90784af2d0104
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424338"
---
# <a name="port-summary---dns-and-hlb-load-balanced-in-lync-server-2013"></a><span data-ttu-id="9c620-103">Portzusammenfassung für DNS- und Hardwarelastenausgleich in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9c620-103">Port summary - DNS and HLB load balanced in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9c620-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9c620-104">

<span> </span></span></span>

<span data-ttu-id="9c620-105">_**Letztes Änderungsdatum des Themas:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="9c620-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="9c620-106">Die Firewall-Portanforderungen für einen einzelnen Director bestehen aus den Ports, die verwendet werden, um die Kommunikation mit dem Director aus der internen Schnittstelle oder dem internen Netzwerk des Reverse-Proxys herzustellen.</span><span class="sxs-lookup"><span data-stu-id="9c620-106">Firewall port requirements for a single Director consist of the ports that are used to establish communication with the Director from the internal interface or internal-facing network of the reverse proxy.</span></span> <span data-ttu-id="9c620-107">Microsoft lync Server 2013 erwartet standardmäßig, dass Ports http/TCP 8080 und HTTPS/TCP 4443 vom Reverse-Proxy an den Director sowie den Front-End-Pool und den Front-End-Server geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="9c620-107">Microsoft Lync Server 2013 by default expects ports HTTP/TCP 8080 and HTTPS/TCP 4443 to be open from the reverse proxy to the Director, as well as the Front End pool and Front End Server.</span></span> <span data-ttu-id="9c620-108">Darüber hinaus muss die SIP-Kommunikation (Session Initiation Protocol) von der internen Schnittstelle des Edge-Servers mit dem Director und dem Front-End-Pool und dem Front-End-Server erfolgen.</span><span class="sxs-lookup"><span data-stu-id="9c620-108">Additionally, there must be session initiation protocol (SIP) communication from the Edge Server internal interface to the Director and to the Front End pool and Front End Server.</span></span> <span data-ttu-id="9c620-109">Das SIP-Protokoll verwendet SIP/MTLS/TCP 5061 vom Edgeserver auf dem Front-End-Pool und dem Front-End-Server.</span><span class="sxs-lookup"><span data-stu-id="9c620-109">The SIP protocol uses SIP/MTLS/TCP 5061 from the Edge Server to the Front End pool and Front End Server.</span></span> <span data-ttu-id="9c620-110">Eine Regel, die die SIP/MTLS/TCP 5061-Kommunikation vom Director, Front-End-Pool und Front-End-Server zur internen Edge-Server-Schnittstelle ermöglicht, muss ebenfalls erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="9c620-110">A rule that allows SIP/MTLS/TCP 5061 communication from the Director, Front End pool and Front End Server to the Edge Server internal interface must be created as well.</span></span>

### <a name="single-director-ports-and-protocols-for-firewall-definitions"></a><span data-ttu-id="9c620-111">Single Director-Ports und-Protokolle für Firewall-Definitionen</span><span class="sxs-lookup"><span data-stu-id="9c620-111">Single Director Ports and Protocols for Firewall Definitions</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9c620-112">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="9c620-112">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="9c620-113">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9c620-113">Source IP address</span></span></th>
<th><span data-ttu-id="9c620-114">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="9c620-114">Destination IP address</span></span></th>
<th><span data-ttu-id="9c620-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9c620-115">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9c620-116">HTTP/TCP 8080</span><span class="sxs-lookup"><span data-stu-id="9c620-116">HTTP/TCP 8080</span></span></p></td>
<td><p><span data-ttu-id="9c620-117">Interne Proxy-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9c620-117">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="9c620-118">Director Hardware Load Balancer VIP</span><span class="sxs-lookup"><span data-stu-id="9c620-118">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="9c620-119">Zunächst von der externen Seite des Reverse-Proxys empfangen, wird die Kommunikation an den Director HLB VIP-und Front-End-Server-Webdienste gesendet.</span><span class="sxs-lookup"><span data-stu-id="9c620-119">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Server web services.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c620-120">HTTPS/TCP 4443</span><span class="sxs-lookup"><span data-stu-id="9c620-120">HTTPS/TCP 4443</span></span></p></td>
<td><p><span data-ttu-id="9c620-121">Interne Proxy-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9c620-121">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="9c620-122">Director Hardware Load Balancer VIP</span><span class="sxs-lookup"><span data-stu-id="9c620-122">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="9c620-123">Zunächst von der externen Seite des Reverse-Proxys empfangen, wird die Kommunikation an den Director HLB VIP-und Front-End-Server-Webdienste gesendet.</span><span class="sxs-lookup"><span data-stu-id="9c620-123">Initially received by the external side of the reverse proxy, the communication is sent on to the Director HLB VIP and Front End Server web services.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c620-124">HTTPS/TCP 444</span><span class="sxs-lookup"><span data-stu-id="9c620-124">HTTPS/TCP 444</span></span></p></td>
<td><p><span data-ttu-id="9c620-125">Director</span><span class="sxs-lookup"><span data-stu-id="9c620-125">Director</span></span></p></td>
<td><p><span data-ttu-id="9c620-126">Front-End-Pool oder Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="9c620-126">Front End pool or Front End Server</span></span></p></td>
<td><p><span data-ttu-id="9c620-127">Kommunikation zwischen Servern zwischen dem Director HLB VIP und dem Front-End-Server oder den Front-End-Servern.</span><span class="sxs-lookup"><span data-stu-id="9c620-127">Inter-server communication between the Director HLB VIP and the Front End Server or Front End Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c620-128">HTTP/TCP 80</span><span class="sxs-lookup"><span data-stu-id="9c620-128">HTTP/TCP 80</span></span></p></td>
<td><p><span data-ttu-id="9c620-129">Interne Clients</span><span class="sxs-lookup"><span data-stu-id="9c620-129">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="9c620-130">Director Hardware Load Balancer VIP</span><span class="sxs-lookup"><span data-stu-id="9c620-130">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="9c620-131">Der Director stellt Webdienste sowohl internen als auch externen Clients zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9c620-131">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c620-132">HTTPS/TCP 443</span><span class="sxs-lookup"><span data-stu-id="9c620-132">HTTPS/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="9c620-133">Interne Clients</span><span class="sxs-lookup"><span data-stu-id="9c620-133">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="9c620-134">Director Hardware Load Balancer VIP</span><span class="sxs-lookup"><span data-stu-id="9c620-134">Director Hardware Load Balancer VIP</span></span></p></td>
<td><p><span data-ttu-id="9c620-135">Der Director stellt Webdienste sowohl internen als auch externen Clients zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="9c620-135">The Director provides web services to internal as well as external clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c620-136">SIP/MTLS/TCP 5061</span><span class="sxs-lookup"><span data-stu-id="9c620-136">SIP/MTLS/TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="9c620-137">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="9c620-137">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="9c620-138">Director</span><span class="sxs-lookup"><span data-stu-id="9c620-138">Director</span></span></p></td>
<td><p><span data-ttu-id="9c620-139">SIP-Kommunikation vom Edgeserver an den Director und die Front-End-Server.</span><span class="sxs-lookup"><span data-stu-id="9c620-139">SIP communication from the Edge Server to the Director, as well as the Front End Servers.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c620-140">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="9c620-140">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="9c620-141">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9c620-141">Any</span></span></p></td>
<td><p><span data-ttu-id="9c620-142">Director</span><span class="sxs-lookup"><span data-stu-id="9c620-142">Director</span></span></p></td>
<td><p><span data-ttu-id="9c620-143">Zentralisierte Protokollierungsdienst Controller (ClsController.exe) oder Agent (ClsAgent.exe)-Befehle und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="9c620-143">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9c620-144">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="9c620-144">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="9c620-145">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9c620-145">Any</span></span></p></td>
<td><p><span data-ttu-id="9c620-146">Director</span><span class="sxs-lookup"><span data-stu-id="9c620-146">Director</span></span></p></td>
<td><p><span data-ttu-id="9c620-147">Zentralisierte Protokollierungsdienst Controller (ClsController.exe) oder Agent (ClsAgent.exe)-Befehle und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="9c620-147">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9c620-148">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="9c620-148">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="9c620-149">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9c620-149">Any</span></span></p></td>
<td><p><span data-ttu-id="9c620-150">Director</span><span class="sxs-lookup"><span data-stu-id="9c620-150">Director</span></span></p></td>
<td><p><span data-ttu-id="9c620-151">Zentralisierte Protokollierungsdienst Controller (ClsController.exe) oder Agent (ClsAgent.exe)-Befehle und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="9c620-151">Centralized Logging Service controller (ClsController.exe) or agent (ClsAgent.exe)commands and log collection</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9c620-152">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9c620-152">


</div>

<span> </span>

</div>

</div>

</span></span></div>

