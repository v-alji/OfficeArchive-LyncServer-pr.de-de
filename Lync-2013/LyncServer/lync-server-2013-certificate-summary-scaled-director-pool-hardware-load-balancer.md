---
title: Zertifikatzusammenfassung für einen skalierten Directorpool (Hardwarelastenausgleich)
description: Zertifikatzusammenfassung – skalierter Director-Pool, Hardware-Lastenausgleichsmodul
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Scaled Director pool, hardware load balancer
ms:assetid: 45940add-8027-418d-b79a-9033b494762f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204846(v=OCS.15)
ms:contentKeyID: 48183992
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 08abc37940cd41a29d6620cfc0a2a801de4a8e38
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394802"
---
# <a name="certificate-summary---scaled-director-pool-hardware-load-balancer-in-lync-server-2013"></a><span data-ttu-id="bff3d-103">Zertifikatzusammenfassung für einen skalierten Directorpool (Hardwarelastenausgleich) in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bff3d-103">Certificate summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bff3d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bff3d-104">

<span> </span></span></span>

<span data-ttu-id="bff3d-105">_**Letztes Änderungsdatum des Themas:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="bff3d-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="bff3d-106">Die Zertifikatanforderungen für einen Director mit einem Hardware Lastenausgleichsmodul verwenden ein Standardzertifikat, das einen Antragstellernamen und einen alternativen Betreff für Dienste enthält, die vom Director-Pool empfangen werden können.</span><span class="sxs-lookup"><span data-stu-id="bff3d-106">Certificate requirements for a Director with a hardware load balancer will use a default certificate that has a subject name and subject alternative names for services that the Director pool can receive.</span></span> <span data-ttu-id="bff3d-107">Für jeden Director im Pool wird ein Zertifikat angefordert.</span><span class="sxs-lookup"><span data-stu-id="bff3d-107">A certificate is requested for each Director in the pool.</span></span> <span data-ttu-id="bff3d-108">Darüber hinaus gibt es ein OAuth-Token Zertifikat für Server-zu-Server-Authentifizierungszwecke, das auf jedem Server installiert ist.</span><span class="sxs-lookup"><span data-stu-id="bff3d-108">Additionally there is an OAuth Token certificate for server to server authentication purposes that is installed on each server.</span></span>

### <a name="certificates-for-a-scaled-director-using-a-hardware-load-balancer"></a><span data-ttu-id="bff3d-109">Zertifikate für einen skalierten Director mit einem Hardware-Lastenausgleichsmodul</span><span class="sxs-lookup"><span data-stu-id="bff3d-109">Certificates for a Scaled Director Using a Hardware Load Balancer</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bff3d-110">Komponente</span><span class="sxs-lookup"><span data-stu-id="bff3d-110">Component</span></span></th>
<th><span data-ttu-id="bff3d-111">Antragstellername</span><span class="sxs-lookup"><span data-stu-id="bff3d-111">Subject name (SN)</span></span></th>
<th><span data-ttu-id="bff3d-112">Subject Alternative Names (San)</span><span class="sxs-lookup"><span data-stu-id="bff3d-112">Subject alternative names (SAN)</span></span></th>
<th><span data-ttu-id="bff3d-113">Kommentare</span><span class="sxs-lookup"><span data-stu-id="bff3d-113">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bff3d-114">Standard</span><span class="sxs-lookup"><span data-stu-id="bff3d-114">Default</span></span></p></td>
<td><p><span data-ttu-id="bff3d-115">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="bff3d-115">dirpool01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="bff3d-116">dirpool01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="bff3d-116">dirpool01.contoso.net</span></span></p>
<p><span data-ttu-id="bff3d-117">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="bff3d-117">dir01.contoso.net</span></span></p>
<p><span data-ttu-id="bff3d-118">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="bff3d-118">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="bff3d-119">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="bff3d-119">meet.contoso.com</span></span></p>
<p><span data-ttu-id="bff3d-120">lyncdiscoverinternal.contoso.com</span><span class="sxs-lookup"><span data-stu-id="bff3d-120">lyncdiscoverinternal.contoso.com</span></span></p>
<p><span data-ttu-id="bff3d-121">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="bff3d-121">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="bff3d-122">(Optional) \*. contoso.com</span><span class="sxs-lookup"><span data-stu-id="bff3d-122">(Optionally) \*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="bff3d-123">Director-Zertifikate können entweder von einer intern verwalteten Zertifizierungsstelle (Certification Authority, ca) oder von einer öffentlichen Zertifizierungsstelle angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="bff3d-123">Director certificates can be requested from either an internally managed certification authority (CA) or from a public CA.</span></span></p>
<p><span data-ttu-id="bff3d-124">Der Director antwortet auf Anforderungen vom Reverse-Proxy im Umkreis oder vom Edgeserver.</span><span class="sxs-lookup"><span data-stu-id="bff3d-124">The Director responds to requests from the reverse proxy in the perimeter or from the Edge Server.</span></span></p>
<p><span data-ttu-id="bff3d-125">Oder ein Platzhaltereintrag für die einfachen URLs</span><span class="sxs-lookup"><span data-stu-id="bff3d-125">Or, a wildcard entry for the simple URLs</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bff3d-126">OAuthTokenIssuer</span><span class="sxs-lookup"><span data-stu-id="bff3d-126">OAuthTokenIssuer</span></span></p></td>
<td><p><span data-ttu-id="bff3d-127">dir01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="bff3d-127">dir01.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="bff3d-128">Kein Eintrag</span><span class="sxs-lookup"><span data-stu-id="bff3d-128">No Entry</span></span></p></td>
<td>


> [!IMPORTANT]
> <span data-ttu-id="bff3d-129">Beachten Sie, dass die minimale Schlüssellänge 1024 ist, aber möglicherweise eine Warnung angezeigt wird, dass die empfohlene Mindestlänge von 2048 Bits beträgt.</span><span class="sxs-lookup"><span data-stu-id="bff3d-129">Note that the minimum key length is 1024, but you may receive a warning that the minimum recommended key length is 2048 bits.</span></span>


<p><span data-ttu-id="bff3d-130">Das OAuthTokenIssuer-Zertifikat ist ein Single-Purpose-Zertifikat zum Zweck der Authentifizierung von Servern in einer großen Umgebung und kann von einer internen Zertifizierungsstelle oder von einer öffentlichen Zertifizierungsstelle angefordert werden.</span><span class="sxs-lookup"><span data-stu-id="bff3d-130">The OAuthTokenIssuer certificate is a single-purpose certificate for the purpose of authenticating servers in a large-scale environment, and can be requested from an internal CA or from a public CA.</span></span> <span data-ttu-id="bff3d-131">Das Zertifikat ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bff3d-131">The certificate is required.</span></span></p><span data-ttu-id="bff3d-132"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bff3d-132"></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</span></span></div>

