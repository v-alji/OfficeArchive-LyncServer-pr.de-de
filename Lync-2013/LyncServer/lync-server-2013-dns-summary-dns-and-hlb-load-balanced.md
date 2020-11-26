---
title: 'Lync Server 2013: DNS-Zusammenfassung für DNS- und Hardwarelastenausgleich'
description: 'Lync Server 2013: DNS Summary – DNS und HLB Load Balanced.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - DNS and HLB load balanced
ms:assetid: d2132695-1956-4190-a98e-cd7255cbded6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205273(v=OCS.15)
ms:contentKeyID: 48185447
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 81c191d653ce4025618e135b4c69bc673f79a6d9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437742"
---
# <a name="dns-summary---dns-and-hlb-load-balanced-in-lync-server-2013"></a><span data-ttu-id="98635-103">DNS-Zusammenfassung für DNS- und Hardwarelastenausgleich in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="98635-103">DNS summary - DNS and HLB load balanced in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="98635-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="98635-104">

<span> </span></span></span>

<span data-ttu-id="98635-105">_**Letztes Änderungsdatum des Themas:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="98635-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="98635-106">Die folgende Tabelle enthält eine Zusammenfassung der DNS-Einträge, die erforderlich sind, um den Director für DNS-Lastenausgleich und Hardwarelastenausgleich zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="98635-106">The following table contains a summary of the DNS records that are required to support the DNS load balanced and hardware load balanced Director.</span></span> <span data-ttu-id="98635-107">Die Rolle des Directors erfordert ähnliche DNS-Einträge wie der Front-End-Server.</span><span class="sxs-lookup"><span data-stu-id="98635-107">The role of the Director requires similar DNS records as the Front End Server.</span></span> <span data-ttu-id="98635-108">Die Anzahl der benötigten Datensätze wird in den für das Director-Zertifikat erforderlichen Alternativen Betreff-Namen widergespiegelt.</span><span class="sxs-lookup"><span data-stu-id="98635-108">The number of records needed is reflected in the subject alternative names required on the Director certificate.</span></span> <span data-ttu-id="98635-109">Anders als der Front-End-Server hostet der Director-Pool keine Benutzerkonten oder hostet die Mobilitätsdienste.</span><span class="sxs-lookup"><span data-stu-id="98635-109">Different from the Front End Server, the Director pool does not host user accounts or host the Mobility Services.</span></span>

### <a name="dns-records-required-for-the-director-pool-using-dns-load-balancing-and-hardware-load-balancer"></a><span data-ttu-id="98635-110">Für den Director-Pool erforderliche DNS-Einträge mithilfe des DNS-Lastenausgleichs und des Hardware Lastenausgleichs</span><span class="sxs-lookup"><span data-stu-id="98635-110">DNS Records Required for the Director Pool using DNS Load Balancing and Hardware Load Balancer</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="98635-111">Ort/Typ/Port</span><span class="sxs-lookup"><span data-stu-id="98635-111">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="98635-112">FQDN/DNS-Eintrag</span><span class="sxs-lookup"><span data-stu-id="98635-112">FQDN/DNS Record</span></span></th>
<th><span data-ttu-id="98635-113">IP-Adresse/FQDN</span><span class="sxs-lookup"><span data-stu-id="98635-113">IP Address/FQDN</span></span></th>
<th><span data-ttu-id="98635-114">Karten/Kommentare</span><span class="sxs-lookup"><span data-stu-id="98635-114">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="98635-115">Internes DNS/A</span><span class="sxs-lookup"><span data-stu-id="98635-115">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="98635-116">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="98635-116">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="98635-117">Director</span><span class="sxs-lookup"><span data-stu-id="98635-117">Director</span></span></p></td>
<td><p><span data-ttu-id="98635-118">Director-Hosteintrag für Replikation und Server-zu-Server</span><span class="sxs-lookup"><span data-stu-id="98635-118">Director host record used for replication and server to server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98635-119">Internes DNS/A</span><span class="sxs-lookup"><span data-stu-id="98635-119">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="98635-120">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="98635-120">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="98635-121">Directorpool</span><span class="sxs-lookup"><span data-stu-id="98635-121">Director pool</span></span></p></td>
<td><p><span data-ttu-id="98635-122">Host-Eintrag für den DNS Load Balancing Director-Pool für Server-zu-Server</span><span class="sxs-lookup"><span data-stu-id="98635-122">Host record for the DNS load balanced Director pool for server to server</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98635-123">Internes DNS/A</span><span class="sxs-lookup"><span data-stu-id="98635-123">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="98635-124">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="98635-124">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="98635-125">Directorpool</span><span class="sxs-lookup"><span data-stu-id="98635-125">Director pool</span></span></p></td>
<td><p><span data-ttu-id="98635-126">SIP (Inbound Session Initiation Protocol) von der internen Schnittstelle des Edge-Servers</span><span class="sxs-lookup"><span data-stu-id="98635-126">Inbound session initiation protocol (SIP) from the internal interface of the Edge Server</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98635-127">Internes DNS/A</span><span class="sxs-lookup"><span data-stu-id="98635-127">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="98635-128">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="98635-128">dialin.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="98635-129">Director Pool HLB VIP</span><span class="sxs-lookup"><span data-stu-id="98635-129">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="98635-130">Hardware Load Balanced veröffentlichte Dialin-Webdienste vom Reverse-Proxy</span><span class="sxs-lookup"><span data-stu-id="98635-130">Hardware load balanced published dialin web services from reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="98635-131">Internes DNS/A</span><span class="sxs-lookup"><span data-stu-id="98635-131">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="98635-132">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="98635-132">meet.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="98635-133">Director Pool HLB VIP</span><span class="sxs-lookup"><span data-stu-id="98635-133">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="98635-134">Hardware Load Balanced veröffentlicht Meet Web Services from Reverse Proxy</span><span class="sxs-lookup"><span data-stu-id="98635-134">Hardware load balanced published meet web services from reverse proxy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="98635-135">Internes DNS/A</span><span class="sxs-lookup"><span data-stu-id="98635-135">Internal DNS/A</span></span></p></td>
<td><p><span data-ttu-id="98635-136">webdirexternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="98635-136">webdirexternal.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="98635-137">Director Pool HLB VIP</span><span class="sxs-lookup"><span data-stu-id="98635-137">Director pool HLB VIP</span></span></p></td>
<td><p><span data-ttu-id="98635-138">Vom Reverse Proxy Web-Ticket externe Webdienste für den Director-Pool veröffentlichte und definierte Hardware Lastenausgleich</span><span class="sxs-lookup"><span data-stu-id="98635-138">Hardware load balanced published and defined by the reverse proxy Web Ticket external web services for the Director pool</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="98635-139">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="98635-139">


</div>

<span> </span>

</div>

</div>

</span></span></div>

