---
title: 'Lync Server 2013: DNS-Übersicht für skalierten Directorpool (Hardwarelastenausgleich)'
description: 'Lync Server 2013: DNS-Zusammenfassung – skalierter Director-Pool, Hardware-Lastenausgleichsmodul.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Scaled Director pool, hardware load balancer
ms:assetid: 08ba48e6-bfa1-4ab0-bc89-d58ddb9c20af
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204655(v=OCS.15)
ms:contentKeyID: 48183340
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7198e6a97feed8ce70cb16753ad1f21d58ef246c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428993"
---
# <a name="dns-summary---scaled-director-pool-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="78383-103">DNS-Übersicht für skalierten Directorpool (Hardwarelastenausgleich) in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="78383-103">DNS summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="78383-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="78383-104">

<span> </span></span></span>

<span data-ttu-id="78383-105">_**Letztes Änderungsdatum des Themas:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="78383-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="78383-106">Die folgende Tabelle enthält eine Zusammenfassung der DNS-Einträge, die für die Unterstützung des Directors Hardware Load Balanced erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="78383-106">The following table contains a summary of the DNS records that are required to support the hardware load balanced Director.</span></span> <span data-ttu-id="78383-107">Die Rolle des Directors erfordert ähnliche DNS-Einträge wie der Front-End-Server.</span><span class="sxs-lookup"><span data-stu-id="78383-107">The role of the Director requires similar DNS records as the Front End Server.</span></span> <span data-ttu-id="78383-108">Die Anzahl der benötigten Datensätze wird in den für das Director-Zertifikat erforderlichen Alternativen Betreff-Namen widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="78383-108">The number of records needed is reflected in the subject alternative names required on the Director certificate.</span></span> <span data-ttu-id="78383-109">Anders als der Front-End-Server hostet der Director-Pool keine Benutzerkonten oder hostet die Mobilitätsdienste.</span><span class="sxs-lookup"><span data-stu-id="78383-109">Different from the Front End Server, the Director pool does not host user accounts or host the Mobility Services.</span></span>

### <a name="dns-records-required-for-the-director-pool-using-a-hardware-load-balancer-and-dns-load-balancing"></a><span data-ttu-id="78383-110">Für den Director-Pool erforderliche DNS-Einträge unter Verwendung eines Hardware Lastenausgleichs und des DNS-Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="78383-110">DNS Records Required for the Director pool using a Hardware Load Balancer and DNS Load Balancing</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78383-111">Ort/Typ/Port</span><span class="sxs-lookup"><span data-stu-id="78383-111">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="78383-112">FQDN/DNS-Eintrag</span><span class="sxs-lookup"><span data-stu-id="78383-112">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="78383-113">IP-Adresse/FQDN</span><span class="sxs-lookup"><span data-stu-id="78383-113">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="78383-114">Karten/Kommentare</span><span class="sxs-lookup"><span data-stu-id="78383-114">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78383-115">Internes DNS/A</span><span class="sxs-lookup"><span data-stu-id="78383-115">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="78383-116">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="78383-116">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="78383-117">Director</span><span class="sxs-lookup"><span data-stu-id="78383-117">Director</span></span></p></td>
<td><p><span data-ttu-id="78383-118">Director-Hosteintrag für Replikation und Server-zu-Server-Kommunikation</span><span class="sxs-lookup"><span data-stu-id="78383-118">Director host record used for replication and server to server communication</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78383-119">Internes DNS/A</span><span class="sxs-lookup"><span data-stu-id="78383-119">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="78383-120">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="78383-120">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="78383-121">Director Pool HLB VIP</span><span class="sxs-lookup"><span data-stu-id="78383-121">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="78383-122">Host-Eintrag für den Director-Pool für DNS Load Balancing</span><span class="sxs-lookup"><span data-stu-id="78383-122">Host record for the DNS load balanced Director pool</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78383-123">Internes DNS/A</span><span class="sxs-lookup"><span data-stu-id="78383-123">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="78383-124">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="78383-124">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="78383-125">Director Pool HLB VIP</span><span class="sxs-lookup"><span data-stu-id="78383-125">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="78383-126">SIP (Inbound Session Initiation Protocol) von der internen Schnittstelle des Edge-Servers</span><span class="sxs-lookup"><span data-stu-id="78383-126">Inbound session initiation protocol (SIP) from the internal interface of the Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78383-127">Internes DNS/A</span><span class="sxs-lookup"><span data-stu-id="78383-127">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="78383-128">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="78383-128">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="78383-129">Director Pool HLB VIP</span><span class="sxs-lookup"><span data-stu-id="78383-129">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="78383-130">Hardware Load Balanced veröffentlichte Dialin-Webdienste vom Reverse-Proxy</span><span class="sxs-lookup"><span data-stu-id="78383-130">Hardware load balanced published dialin web services from reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78383-131">Internes DNS/A</span><span class="sxs-lookup"><span data-stu-id="78383-131">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="78383-132">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="78383-132">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="78383-133">Director Pool HLB VIP</span><span class="sxs-lookup"><span data-stu-id="78383-133">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="78383-134">Hardware Load Balanced veröffentlicht Meet Web Services from Reverse Proxy</span><span class="sxs-lookup"><span data-stu-id="78383-134">Hardware load balanced published meet web services from reverse proxy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78383-135">Internes DNS/A</span><span class="sxs-lookup"><span data-stu-id="78383-135">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="78383-136">webdirexternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="78383-136">webdirexternal.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="78383-137">Director Pool HLB VIP</span><span class="sxs-lookup"><span data-stu-id="78383-137">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="78383-138">Vom Reverse Proxy Web-Ticket externe Webdienste für den Director-Pool veröffentlichte und definierte Hardware Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="78383-138">Hardware load balanced published and defined by the reverse proxy Web Ticket external web services for the Director pool</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="78383-139">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="78383-139">


</div>

<span> </span>

</div>

</div>

</span></span></div>

