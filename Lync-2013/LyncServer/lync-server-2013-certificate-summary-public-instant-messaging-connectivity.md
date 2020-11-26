---
title: 'Lync Server 2013: Zertifikats Zusammenfassung – öffentliche Instant Messaging-Konnektivität'
description: 'Lync Server 2013: Zertifikats Zusammenfassung – öffentliche Instant Messaging-Konnektivität.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Public instant messaging connectivity
ms:assetid: 2b3687ee-50c2-4c1c-880e-8dcf8bd4f309
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618370(v=OCS.15)
ms:contentKeyID: 49105657
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: abf5a01bdeb03da158e221c623417a1b42cc82f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435292"
---
# <a name="certificate-summary---public-instant-messaging-connectivity-in-lync-server-2013"></a><span data-ttu-id="df57d-103">Zertifikats Zusammenfassung – öffentliche Instant Messaging-Konnektivität in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df57d-103">Certificate summary - Public instant messaging connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="df57d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="df57d-104">

<span> </span></span></span>

<span data-ttu-id="df57d-105">_**Letztes Änderungsdatum des Themas:** 2013-02-19_</span><span class="sxs-lookup"><span data-stu-id="df57d-105">_**Topic Last Modified:** 2013-02-19_</span></span>

<span data-ttu-id="df57d-106">Wenn Sie Zertifikate für die öffentliche Instant Messaging-Konnektivität konfigurieren möchten, sollten Sie zuerst feststellen, dass sich nichts von anderen SIP Federation-Typen oder sogar Standard-Edgeserver-Zertifikaten unterscheidet, es sei denn, dass America Online (AOL) eine eindeutige Zertifikatkonfiguration erfordert.</span><span class="sxs-lookup"><span data-stu-id="df57d-106">To configure certificates for public Instant Messaging connectivity, you should first notice that there is nothing different from other SIP federation types or even standard Edge Server certificates, except that America Online (AOL) requires a unique certificate configuration.</span></span> <span data-ttu-id="df57d-107">Neben der üblichen Server-Erweiterte Schlüsselverwendung (EKU) erfordert America Online, dass das Zertifikat oder die Zertifikate (im Fall eines Edge-Pools) auch die Client-EKU enthalten.</span><span class="sxs-lookup"><span data-stu-id="df57d-107">In addition to the usual server enhanced key usage (EKU), America Online requires the certificate or certificates (in the case of an Edge pool) to also contain the client EKU.</span></span> <span data-ttu-id="df57d-108">Die Client-EKU ist eine Ergänzung zum Zertifikat und Teil des externen öffentlichen Zertifikats, das Ihrem Edgeserver zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="df57d-108">The client EKU is an addition to the certificate, and is part of the external public certificate that is assigned to your Edge Server.</span></span>

<div>

## <a name="certificate-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="df57d-109">Zusammenfassung des Zertifikats – öffentliche Instant Messaging-Konnektivität</span><span class="sxs-lookup"><span data-stu-id="df57d-109">Certificate Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="df57d-110">Komponente</span><span class="sxs-lookup"><span data-stu-id="df57d-110">Component</span></span></th>
<th><span data-ttu-id="df57d-111">Name des Antragstellers</span><span class="sxs-lookup"><span data-stu-id="df57d-111">Subject name</span></span></th>
<th><span data-ttu-id="df57d-112">Subject Alternative Names (San)/Order</span><span class="sxs-lookup"><span data-stu-id="df57d-112">Subject alternative names (SAN)/Order</span></span></th>
<th><span data-ttu-id="df57d-113">Kommentare</span><span class="sxs-lookup"><span data-stu-id="df57d-113">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="df57d-114">Extern/Access-Edge</span><span class="sxs-lookup"><span data-stu-id="df57d-114">External/Access Edge</span></span></p></td>
<td><p><span data-ttu-id="df57d-115">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="df57d-115">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="df57d-116">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="df57d-116">sip.contoso.com</span></span></p>
<p><span data-ttu-id="df57d-117">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="df57d-117">webcon.contoso.com</span></span></p>
<p><span data-ttu-id="df57d-118">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="df57d-118">sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="df57d-119">Das Zertifikat muss von einer öffentlichen Zertifizierungsstelle sein und über die Server-EKU und den Client-EKU verfügen, wenn öffentliche Chat Verbindungen mit AOL bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="df57d-119">The certificate must be from a Public CA, and must have the server EKU and client EKU if public IM connectivity with AOL is to be deployed.</span></span> <span data-ttu-id="df57d-120">Das Zertifikat wird den externen Edgeserver-Schnittstellen für Folgendes zugewiesen:</span><span class="sxs-lookup"><span data-stu-id="df57d-120">The certificate is assigned to the external Edge Server interfaces for:</span></span></p>
<ul>
<li><p><span data-ttu-id="df57d-121">Zugriffs-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="df57d-121">Access Edge service</span></span></p></li>
<li><p><span data-ttu-id="df57d-122">Webkonferenz-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="df57d-122">Web Conferencing Edge service</span></span></p></li>
<li><p><span data-ttu-id="df57d-123">A/V-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="df57d-123">A/V Edge service</span></span></p></li>
</ul>
<p><span data-ttu-id="df57d-124">Beachten Sie, dass Sans automatisch dem Zertifikat basierend auf ihren Definitionen im Topologie-Generator hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="df57d-124">Note that SANs are automatically added to the certificate based on your definitions in Topology Builder.</span></span> <span data-ttu-id="df57d-125">Für zusätzliche SIP-Domänen und andere Einträge, die Sie unterstützen müssen, fügen Sie nach Bedarf San-Einträge hinzu.</span><span class="sxs-lookup"><span data-stu-id="df57d-125">You add SAN entries as needed for additional SIP domains and other entries that you need to support.</span></span> <span data-ttu-id="df57d-126">Der Antragstellername wird im San repliziert und muss für den korrekten Betrieb vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="df57d-126">The subject name is replicated in the SAN and must be present for correct operation.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="df57d-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df57d-127">See Also</span></span>


[<span data-ttu-id="df57d-128">Szenarien für den Zugriff durch externe Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="df57d-128">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
  

<span data-ttu-id="df57d-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="df57d-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

