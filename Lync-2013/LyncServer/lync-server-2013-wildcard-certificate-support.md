---
title: 'Lync Server 2013: Unterstützung von Platzhalterzertifikaten'
description: Lync Server 2013-Platzhalterzertifikat-Unterstützung.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Wildcard certificate support
ms:assetid: 0bae2aa8-b6dc-46f5-a3be-3fe7581809d4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202161(v=OCS.15)
ms:contentKeyID: 48183382
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 46cc362eb925a86b5e90d51569db6d425ba88fa6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394470"
---
# <a name="wildcard-certificate-support-in-lync-server-2013"></a><span data-ttu-id="6fce9-103">Unterstützung von Platzhalterzertifikaten in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6fce9-103">Wildcard certificate support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6fce9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6fce9-104">

<span> </span></span></span>

<span data-ttu-id="6fce9-105">_**Letztes Änderungsdatum des Themas:** 2013-03-21_</span><span class="sxs-lookup"><span data-stu-id="6fce9-105">_**Topic Last Modified:** 2013-03-21_</span></span>

<span data-ttu-id="6fce9-106">Lync Server 2013 verwendet Zertifikate, um Kommunikationsverschlüsselung und Authentifizierung von Server Identitäten bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6fce9-106">Lync Server 2013 uses certificates to provide communications encryption and server identity authentication.</span></span> <span data-ttu-id="6fce9-107">In einigen Fällen, wie beispielsweise Web-Publishing über den Reverse-Proxy, ist ein starker Subject Alternative Name (San)-Eintrag, der dem vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Servers entspricht, der den Dienst darstellt, nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="6fce9-107">In some cases, such as web publishing through the reverse proxy, strong subject alternative name (SAN) entry matching to the fully qualified domain name (FQDN) of the server presenting the service is not required.</span></span> <span data-ttu-id="6fce9-108">In diesen Fällen können Sie Zertifikate mit Platzhalter-San-Einträgen (häufig als "Platzhalterzertifikate" bezeichnet) verwenden, um die Kosten für ein von einer öffentlichen Zertifizierungsstelle angefordertes Zertifikat zu verringern und die Komplexität des Planungsprozesses für Zertifikate zu verringern.</span><span class="sxs-lookup"><span data-stu-id="6fce9-108">In these cases, you can use certificates with wildcard SAN entries (commonly known as “wildcard certificates”) to reduce the cost of a certificate requested from a public certification authority and to reduce the complexity of the planning process for certificates.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="6fce9-109">Wenn Sie die Funktionalität von Unified Communications (UC)-Geräten (beispielsweise bei Tischtelefonen) beibehalten möchten, sollten Sie das bereitgestellte Zertifikat sorgfältig testen, um sicherzustellen, dass die Geräte ordnungsgemäß funktionieren, nachdem Sie ein Platzhalterzertifikat implementiert haben.</span><span class="sxs-lookup"><span data-stu-id="6fce9-109">To retain the functionality of unified communications (UC) devices (for example, desk phones), you should test the deployed certificate carefully to ensure that devices function properly after you implement a wildcard certificate.</span></span>



</div>

<span data-ttu-id="6fce9-110">Es gibt keine Unterstützung für einen Platzhaltereintrag als Antragstellernamen (auch als "allgemeiner Name" oder "CN" bezeichnet) für eine beliebige Rolle.</span><span class="sxs-lookup"><span data-stu-id="6fce9-110">There is no support for a wildcard entry as the subject name (also referred to as the common name or CN) for any role.</span></span> <span data-ttu-id="6fce9-111">Die folgenden Serverrollen werden bei Verwendung von Platzhaltereinträgen im San unterstützt:</span><span class="sxs-lookup"><span data-stu-id="6fce9-111">The following server roles are supported when using wildcard entries in the SAN:</span></span>

  - <span></span>  
    <span data-ttu-id="6fce9-112">**Reverseproxy**</span><span class="sxs-lookup"><span data-stu-id="6fce9-112">**Reverse proxy.**</span></span>   <span data-ttu-id="6fce9-113">Platzhalter-San-Eintrag wird für ein einfaches URL-Veröffentlichungs Zertifikat unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6fce9-113">Wildcard SAN entry is supported for Simple URL (meet and dialin) publishing certificate.</span></span>

  - <span></span>  
    <span data-ttu-id="6fce9-114">**Reverseproxy**</span><span class="sxs-lookup"><span data-stu-id="6fce9-114">**Reverse proxy.**</span></span>   <span data-ttu-id="6fce9-115">Platzhalter-San-Eintrag wird für die San-Einträge für LyncDiscover auf dem Veröffentlichungs Zertifikat unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6fce9-115">Wildcard SAN entry is supported for the SAN entries for LyncDiscover on the publishing certificate.</span></span>

  - <span></span>  
    <span data-ttu-id="6fce9-116">**Direktor.**</span><span class="sxs-lookup"><span data-stu-id="6fce9-116">**Director.**</span></span>   <span data-ttu-id="6fce9-117">Platzhalter-San-Eintrag wird für einfache URLs (Meet und Dialin) sowie für San-Einträge für LyncDiscover und LyncDiscoverInternal in Director Web Components unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6fce9-117">Wildcard SAN entry is supported for Simple URLs (meet and dialin) and for SAN entries for LyncDiscover and LyncDiscoverInternal in Director web components.</span></span>

  - <span></span>  
    <span data-ttu-id="6fce9-118">**Front-End-Server (Standard Edition) und Front-End-Pool (Enterprise Edition).**</span><span class="sxs-lookup"><span data-stu-id="6fce9-118">**Front End Server (Standard Edition) and Front End pool (Enterprise Edition).**</span></span> <span data-ttu-id="6fce9-119">Platzhalter-San-Eintrag wird für einfache URLs (Meet und Dialin) sowie für San-Einträge für LyncDiscover und LyncDiscoverInternal in Front-End-Webkomponenten unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6fce9-119">Wildcard SAN entry is supported for Simple URLs (meet and dialin) and for SAN entries for LyncDiscover and LyncDiscoverInternal in Front End web components.</span></span>

  - <span></span>  
    <span data-ttu-id="6fce9-120">**Exchange Unified Messaging (um).**</span><span class="sxs-lookup"><span data-stu-id="6fce9-120">**Exchange Unified Messaging (UM).**</span></span>   <span data-ttu-id="6fce9-121">Der Server verwendet keine San-Einträge, wenn er als eigenständiger Server bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="6fce9-121">The server does not use SAN entries when deployed as a stand-alone server.</span></span>

  - <span></span>  
    <span data-ttu-id="6fce9-122">**Microsoft Exchange Server-Client Zugriffsserver**</span><span class="sxs-lookup"><span data-stu-id="6fce9-122">**Microsoft Exchange Server Client Access server.**</span></span>   <span data-ttu-id="6fce9-123">Platzhaltereinträge im San werden für interne und externe Clients unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6fce9-123">Wildcard entries in the SAN are supported for internal and external clients.</span></span>

  - <span></span>  
    <span data-ttu-id="6fce9-124">**Exchange Unified Messaging (um) und Microsoft Exchange Server-Client Zugriffsserver auf demselben Server.**</span><span class="sxs-lookup"><span data-stu-id="6fce9-124">**Exchange Unified Messaging (UM) and Microsoft Exchange Server Client Access server on same server.**</span></span>   <span data-ttu-id="6fce9-125">Platzhalter-San-Einträge werden unterstützt.</span><span class="sxs-lookup"><span data-stu-id="6fce9-125">Wildcard SAN entries are supported.</span></span>

<span data-ttu-id="6fce9-126">Server Rollen, die in diesem Thema nicht behandelt werden:</span><span class="sxs-lookup"><span data-stu-id="6fce9-126">Server roles that are not addressed in this topic:</span></span>

  - <span data-ttu-id="6fce9-127">Interne Serverrollen (einschließlich, aber nicht nur auf den Vermittlungsserver, den Archivierungs-und Überwachungsserver, die Survivable Branch-Appliance oder den Survivable Branch-Server)</span><span class="sxs-lookup"><span data-stu-id="6fce9-127">Internal server roles (including, but not limited to the Mediation Server, Archiving and Monitoring Server, Survivable Branch Appliance, or Survivable Branch Server)</span></span>

  - <span data-ttu-id="6fce9-128">Externe Edgeserver-Schnittstellen</span><span class="sxs-lookup"><span data-stu-id="6fce9-128">External Edge Server interfaces</span></span>

  - <span data-ttu-id="6fce9-129">Interner Edgeserver</span><span class="sxs-lookup"><span data-stu-id="6fce9-129">Internal Edge Server</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="6fce9-130">Für die interne Edge-Server Schnittstelle kann dem San ein Platzhaltereintrag zugewiesen und unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="6fce9-130">For the internal Edge Server interface, a wildcard entry can be assigned to the SAN, and is supported.</span></span> <span data-ttu-id="6fce9-131">Das San auf dem internen Edgeserver wird nicht abgefragt, und ein Platzhalter-San-Eintrag hat einen geringen Wert.</span><span class="sxs-lookup"><span data-stu-id="6fce9-131">The SAN on the internal Edge Server is not queried, and a wildcard SAN entry is of limited value.</span></span>

    
    </div>

<span data-ttu-id="6fce9-132">Details zu Zertifikat Konfigurationen, einschließlich der Verwendung von Platzhaltern in Zertifikaten, finden Sie unter den folgenden Themen:</span><span class="sxs-lookup"><span data-stu-id="6fce9-132">For details about certificate configurations, including the use of wildcards in certificates, see the following topics:</span></span>

  - [<span data-ttu-id="6fce9-133">Anforderungen an Zertifikate für interne Server in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6fce9-133">Certificate requirements for internal servers in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-internal-servers.md)

  - [<span data-ttu-id="6fce9-134">Zertifikatanforderungen für den Zugriff durch externe Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6fce9-134">Certificate requirements for external user access in Lync Server 2013</span></span>](lync-server-2013-certificate-requirements-for-external-user-access.md)

  - [<span data-ttu-id="6fce9-135">Zertifikatzusammenfassung für DNS- und Hardwarelastenausgleich in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6fce9-135">Certificate summary - DNS and HLB load balanced in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-dns-and-hlb-load-balanced.md)

  - [<span data-ttu-id="6fce9-136">Zertifikatzusammenfassung für einen einzelnen Director in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6fce9-136">Certificate summary - Single Director in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-single-director.md)

  - [<span data-ttu-id="6fce9-137">Zertifikatzusammenfassung für einen skalierten Directorpool (Hardwarelastenausgleich) in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6fce9-137">Certificate summary - Scaled Director pool, hardware load balancer in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-scaled-director-pool-hardware-load-balancer.md)

  - [<span data-ttu-id="6fce9-138">Zertifikatzusammenfassung für Reverseproxy in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6fce9-138">Certificate summary - Reverse proxy in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-reverse-proxy.md)

  - [<span data-ttu-id="6fce9-139">Richtlinien für die Integration lokaler Unified Messaging-Dienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6fce9-139">Guidelines for integrating on-premises Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-guidelines-for-integrating-on-premises-unified-messaging.md)

<span data-ttu-id="6fce9-140">Details zum Konfigurieren von Zertifikaten für Exchange, einschließlich der Verwendung von Platzhaltern, finden Sie in der Exchange 2013-Produktdokumentation.</span><span class="sxs-lookup"><span data-stu-id="6fce9-140">For details about configuring certificates for Exchange, including the use of wildcards, see the Exchange 2013 product documentation.</span></span>

<span data-ttu-id="6fce9-141"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6fce9-141"></div>

<span> </span>

</div>

</div>

</span></span></div>

