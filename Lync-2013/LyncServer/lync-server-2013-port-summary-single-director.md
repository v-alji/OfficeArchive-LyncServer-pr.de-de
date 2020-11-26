---
title: 'Lync Server 2013: Portzusammenfassung für einen einzelnen Director'
description: 'Lync Server 2013: Port Zusammenfassung – einzelner Director'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Single Director
ms:assetid: 079c1414-723f-4499-b7d4-a0d7121c1626
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204648(v=OCS.15)
ms:contentKeyID: 48183322
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a46e394121dbc7dd6158016d39511e9487cec1ff
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436979"
---
# <a name="port-summary---single-director-in-lync-server-2013"></a><span data-ttu-id="078f6-103">Portzusammenfassung für einen einzelnen Director in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="078f6-103">Port summary - Single Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="078f6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="078f6-104">

<span> </span></span></span>

<span data-ttu-id="078f6-105">_**Letztes Änderungsdatum des Themas:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="078f6-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="078f6-106">Die Firewall-Portanforderungen für einen einzelnen Director bestehen aus den Ports, die verwendet werden, um die Kommunikation mit dem Director aus der internen Schnittstelle oder dem internen Netzwerk des Reverse-Proxys herzustellen.</span><span class="sxs-lookup"><span data-stu-id="078f6-106">Firewall port requirements for a single Director consist of the ports that are used to establish communication with the Director from the internal interface or internal-facing network of the reverse proxy.</span></span> <span data-ttu-id="078f6-107">Microsoft lync Server 2013 erwartet standardmäßig, dass Ports http/TCP 8080 und HTTPS/TCP 4443 vom Reverse-Proxy an den Director sowie den Front-End-Pool und den Front-End-Server geöffnet werden.</span><span class="sxs-lookup"><span data-stu-id="078f6-107">Microsoft Lync Server 2013 by default expects ports HTTP/TCP 8080 and HTTPS/TCP 4443 to be open from the reverse proxy to the Director, as well as the Front End pool and Front End Server.</span></span> <span data-ttu-id="078f6-108">Darüber hinaus muss die SIP-Kommunikation (Session Initiation Protocol) von der internen Schnittstelle des Edge-Servers mit dem Director und dem Front-End-Pool und dem Front-End-Server erfolgen.</span><span class="sxs-lookup"><span data-stu-id="078f6-108">Additionally, there must be session initiation protocol (SIP) communication from the Edge Server internal interface to the Director and to the Front End pool and Front End Server.</span></span> <span data-ttu-id="078f6-109">Das SIP-Protokoll verwendet SIP/MTLS/TCP 5061 vom Edgeserver auf dem Front-End-Pool und dem Front-End-Server.</span><span class="sxs-lookup"><span data-stu-id="078f6-109">The SIP protocol uses SIP/MTLS/TCP 5061 from the Edge Server to the Front End pool and Front End Server.</span></span> <span data-ttu-id="078f6-110">Eine Regel, die die SIP/MTLS/TCP 5061-Kommunikation vom Director, Front-End-Pool und Front-End-Server zur internen Edge-Server-Schnittstelle ermöglicht, muss ebenfalls erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="078f6-110">A rule that allows SIP/MTLS/TCP 5061 communication from the Director, Front End pool and Front End Server to the Edge Server internal interface must be created as well.</span></span>

### <a name="single-director-ports-and-protocols-for-firewall-definitions"></a><span data-ttu-id="078f6-111">Single Director-Ports und-Protokolle für Firewall-Definitionen</span><span class="sxs-lookup"><span data-stu-id="078f6-111">Single Director Ports and Protocols for Firewall Definitions</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="078f6-112">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="078f6-112">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="078f6-113">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="078f6-113">Source IP address</span></span></th>
<th><span data-ttu-id="078f6-114">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="078f6-114">Destination IP address</span></span></th>
<th><span data-ttu-id="078f6-115">Hinweise</span><span class="sxs-lookup"><span data-stu-id="078f6-115">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="078f6-116">HTTP/TCP 8080</span><span class="sxs-lookup"><span data-stu-id="078f6-116">HTTP/TCP 8080</span></span></p></td>
<td><p><span data-ttu-id="078f6-117">Interne Proxy-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="078f6-117">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="078f6-118">Director</span><span class="sxs-lookup"><span data-stu-id="078f6-118">Director</span></span></p></td>
<td><p><span data-ttu-id="078f6-119">Zunächst von der externen Seite des Reverse-Proxys empfangen, wird die Kommunikation an den Director und die Front-End-Server-Webdienste gesendet.</span><span class="sxs-lookup"><span data-stu-id="078f6-119">Initially received by the external side of the reverse proxy, the communication is sent on to the Director and Front End Server web services</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="078f6-120">HTTPS/TCP 4443</span><span class="sxs-lookup"><span data-stu-id="078f6-120">HTTPS/TCP 4443</span></span></p></td>
<td><p><span data-ttu-id="078f6-121">Interne Proxy-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="078f6-121">Reverse proxy internal interface</span></span></p></td>
<td><p><span data-ttu-id="078f6-122">Director</span><span class="sxs-lookup"><span data-stu-id="078f6-122">Director</span></span></p></td>
<td><p><span data-ttu-id="078f6-123">Zunächst von der externen Seite des Reverse-Proxys empfangen, wird die Kommunikation an den Director und die Front-End-Server-Webdienste gesendet.</span><span class="sxs-lookup"><span data-stu-id="078f6-123">Initially received by the external side of the reverse proxy, the communication is sent on to the Director and Front End Server web services</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="078f6-124">HTTPS/TCP 444</span><span class="sxs-lookup"><span data-stu-id="078f6-124">HTTPS/TCP 444</span></span></p></td>
<td><p><span data-ttu-id="078f6-125">Director</span><span class="sxs-lookup"><span data-stu-id="078f6-125">Director</span></span></p></td>
<td><p><span data-ttu-id="078f6-126">Front-End-Server oder Front-End-Pool</span><span class="sxs-lookup"><span data-stu-id="078f6-126">Front End server or Front End pool</span></span></p></td>
<td><p><span data-ttu-id="078f6-127">Inter-Server-Kommunikation zwischen dem Director und dem Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="078f6-127">Inter-server communication between the Director and the Front End Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="078f6-128">HTTP/TCP 80</span><span class="sxs-lookup"><span data-stu-id="078f6-128">HTTP/TCP 80</span></span></p></td>
<td><p><span data-ttu-id="078f6-129">Interne Clients</span><span class="sxs-lookup"><span data-stu-id="078f6-129">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="078f6-130">Director-Webdienste</span><span class="sxs-lookup"><span data-stu-id="078f6-130">Director web services</span></span></p></td>
<td><p><span data-ttu-id="078f6-131">Der Director bietet Web Services für interne und externe Clients.</span><span class="sxs-lookup"><span data-stu-id="078f6-131">The Director provides web services to internal and external clients.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="078f6-132">HTTPS/TCP 443</span><span class="sxs-lookup"><span data-stu-id="078f6-132">HTTPS/TCP 443</span></span></p></td>
<td><p><span data-ttu-id="078f6-133">Interne Clients</span><span class="sxs-lookup"><span data-stu-id="078f6-133">Internal Clients</span></span></p></td>
<td><p><span data-ttu-id="078f6-134">Director-Webdienste</span><span class="sxs-lookup"><span data-stu-id="078f6-134">Director web services</span></span></p></td>
<td><p><span data-ttu-id="078f6-135">Der Director bietet Web Services für interne und externe Clients.</span><span class="sxs-lookup"><span data-stu-id="078f6-135">The Director provides web services to internal and external clients.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="078f6-136">SIP/MTLS/TCP 5061</span><span class="sxs-lookup"><span data-stu-id="078f6-136">SIP/MTLS/TCP 5061</span></span></p></td>
<td><p><span data-ttu-id="078f6-137">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="078f6-137">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="078f6-138">Director</span><span class="sxs-lookup"><span data-stu-id="078f6-138">Director</span></span></p></td>
<td><p><span data-ttu-id="078f6-139">SIP-Kommunikation vom Edgeserver an den Director und den Front-End-Server.</span><span class="sxs-lookup"><span data-stu-id="078f6-139">SIP communication from the Edge Server to the Director, and the Front End Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="078f6-140">MTLS/TCP/50001</span><span class="sxs-lookup"><span data-stu-id="078f6-140">MTLS/TCP/50001</span></span></p></td>
<td><p><span data-ttu-id="078f6-141">Beliebig</span><span class="sxs-lookup"><span data-stu-id="078f6-141">Any</span></span></p></td>
<td><p><span data-ttu-id="078f6-142">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="078f6-142">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="078f6-143">Zentralisierte Protokollierungsdienst Controller (ClsController.exe) oder Agent (ClasAgent.exe)-Befehle und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="078f6-143">Centralized Logging Service controller (ClsController.exe) or agent (ClasAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="078f6-144">MTLS/TCP/50002</span><span class="sxs-lookup"><span data-stu-id="078f6-144">MTLS/TCP/50002</span></span></p></td>
<td><p><span data-ttu-id="078f6-145">Beliebig</span><span class="sxs-lookup"><span data-stu-id="078f6-145">Any</span></span></p></td>
<td><p><span data-ttu-id="078f6-146">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="078f6-146">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="078f6-147">Zentralisierte Protokollierungsdienst Controller (ClsController.exe) oder Agent (ClasAgent.exe)-Befehle und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="078f6-147">Centralized Logging Service controller (ClsController.exe) or agent (ClasAgent.exe)commands and log collection</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="078f6-148">MTLS/TCP/50003</span><span class="sxs-lookup"><span data-stu-id="078f6-148">MTLS/TCP/50003</span></span></p></td>
<td><p><span data-ttu-id="078f6-149">Beliebig</span><span class="sxs-lookup"><span data-stu-id="078f6-149">Any</span></span></p></td>
<td><p><span data-ttu-id="078f6-150">Interne Edge-Server-Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="078f6-150">Edge Server internal interface</span></span></p></td>
<td><p><span data-ttu-id="078f6-151">Zentralisierte Protokollierungsdienst Controller (ClsController.exe) oder Agent (ClasAgent.exe)-Befehle und Protokollsammlung</span><span class="sxs-lookup"><span data-stu-id="078f6-151">Centralized Logging Service controller (ClsController.exe) or agent (ClasAgent.exe)commands and log collection</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="078f6-152">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="078f6-152">


</div>

<span> </span>

</div>

</div>

</span></span></div>

