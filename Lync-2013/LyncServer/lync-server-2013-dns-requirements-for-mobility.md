---
title: 'Lync Server 2013: DNS-Anforderungen für Mobilität'
description: 'Lync Server 2013: DNS-Anforderungen für Mobilität.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for mobility
ms:assetid: df6962bc-2a16-440e-a333-022ebd14f957
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690040(v=OCS.15)
ms:contentKeyID: 48185624
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e2a8377dc7c856bb7250817cb3b8b66ed7789d3b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437805"
---
# <a name="dns-requirements-for-mobility-with-lync-server-2013"></a><span data-ttu-id="8d178-103">DNS-Anforderungen für Mobilität mit lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8d178-103">DNS requirements for mobility with Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8d178-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8d178-104">

<span> </span></span></span>

<span data-ttu-id="8d178-105">_**Letztes Änderungsdatum des Themas:** 2012-11-13_</span><span class="sxs-lookup"><span data-stu-id="8d178-105">_**Topic Last Modified:** 2012-11-13_</span></span>

<span data-ttu-id="8d178-106">Wenn Sie das Mobilitätsfeature von lync Server 2013 bereitstellen, können Sie die neuen URLs verwenden, die für den AutoErmittlungsdienst von Microsoft lync Server 2013 verfügbar sind, oder Sie können Ihre vorhandenen URLs für Webdienste verwenden.</span><span class="sxs-lookup"><span data-stu-id="8d178-106">When you deploy the Lync Server 2013 mobility feature, you can use the new URLs that are available with the Microsoft Lync Server 2013 Autodiscover Service, or you can use your existing Web Services URLs.</span></span> <span data-ttu-id="8d178-107">Wenn Sie Ihre vorhandenen URLs verwenden, müssen die Benutzer die URLs in Ihren Einstellungen für mobile Geräte manuell eingeben.</span><span class="sxs-lookup"><span data-stu-id="8d178-107">If you use your existing URLs, users need to manually enter the URLs in their mobile device settings.</span></span> <span data-ttu-id="8d178-108">Diese Option wird in der Regel für die Problembehandlung verwendet.</span><span class="sxs-lookup"><span data-stu-id="8d178-108">This option is typically used for troubleshooting.</span></span> <span data-ttu-id="8d178-109">Wenn Sie die neuen URLs verwenden, können mobile Clients die lync Server 2013-Ressourcen automatisch ermitteln.</span><span class="sxs-lookup"><span data-stu-id="8d178-109">When you use the new URLs, mobile clients can automatically discover Lync Server 2013 resources.</span></span> <span data-ttu-id="8d178-110">Wenn Sie die automatische Ermittlung unterstützen, müssen Sie neue DNS-Einträge (Domain Name System) hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8d178-110">When you support automatic discovery, you need to add new Domain Name System (DNS) records.</span></span> <span data-ttu-id="8d178-111">In diesem Abschnitt werden die DNS-Einträge beschrieben, die für die automatische Ermittlung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8d178-111">This section describes the DNS records that are required for automatic discovery.</span></span>

<span data-ttu-id="8d178-112">Zur Unterstützung der automatischen Ermittlung müssen Sie die folgenden DNS-Einträge für jede SIP-Domäne erstellen:</span><span class="sxs-lookup"><span data-stu-id="8d178-112">To support automatic discovery, you need to create the following DNS records for each SIP domain:</span></span>

  - <span data-ttu-id="8d178-113">Ein interner DNS-Eintrag zur Unterstützung von mobilen Benutzern, die innerhalb des Netzwerks Ihrer Organisation eine Verbindung herstellen</span><span class="sxs-lookup"><span data-stu-id="8d178-113">An internal DNS record to support mobile users who connect from within your organization's network</span></span>

  - <span data-ttu-id="8d178-114">Ein externer oder öffentlicher DNS-Eintrag zur Unterstützung von mobilen Benutzern, die eine Verbindung mit dem Internet herstellen</span><span class="sxs-lookup"><span data-stu-id="8d178-114">An external, or public, DNS record to support mobile users who connect from the Internet</span></span>

<span data-ttu-id="8d178-115">Die interne automatische Erkennungs-URL sollte nicht von außerhalb Ihres Netzwerks adressierbar sein.</span><span class="sxs-lookup"><span data-stu-id="8d178-115">The internal automatic discovery URL should not be addressable from outside your network.</span></span> <span data-ttu-id="8d178-116">Die URL für die externe automatische Suche sollte in Ihrem Netzwerk nicht adressierbar sein.</span><span class="sxs-lookup"><span data-stu-id="8d178-116">The external automatic discovery URL should not be addressable from within your network.</span></span> <span data-ttu-id="8d178-117">Wenn Sie diese Voraussetzungen für die externe URL nicht erfüllen können, sollte der Mobile Client jedoch nicht beeinträchtigt werden.</span><span class="sxs-lookup"><span data-stu-id="8d178-117">However, if you cannot meet this requirement for the external URL, mobile client functionally should not be affected.</span></span>

<span data-ttu-id="8d178-118">Bei den DNS-Einträgen kann es sich entweder um CNAME-Einträge oder einen (Host-) Eintrag handeln.</span><span class="sxs-lookup"><span data-stu-id="8d178-118">The DNS records can be either CNAME records or A (host) records.</span></span>

<span data-ttu-id="8d178-119">**Interne DNS-Einträge**</span><span class="sxs-lookup"><span data-stu-id="8d178-119">**Internal DNS records**</span></span>

<span data-ttu-id="8d178-120">Sie müssen einen der folgenden internen DNS-Einträge erstellen:</span><span class="sxs-lookup"><span data-stu-id="8d178-120">You need to create one of the following internal DNS records:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8d178-121">Eintragstyp</span><span class="sxs-lookup"><span data-stu-id="8d178-121">Record type</span></span></th>
<th><span data-ttu-id="8d178-122">Hostname oder SRV-Definition</span><span class="sxs-lookup"><span data-stu-id="8d178-122">Host name or SRV definition</span></span></th>
<th><span data-ttu-id="8d178-123">Auflösung in</span><span class="sxs-lookup"><span data-stu-id="8d178-123">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d178-124">CNAME</span><span class="sxs-lookup"><span data-stu-id="8d178-124">CNAME</span></span></p></td>
<td><p><span data-ttu-id="8d178-125">lyncdiscoverinternal. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="8d178-125">lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="8d178-126">Interner Webdienste (Fully Qualified Domain Name, FQDN) für Ihren Director-Pool, falls vorhanden, oder für Ihren Front-End-Pool, wenn Sie keinen Director haben</span><span class="sxs-lookup"><span data-stu-id="8d178-126">Internal Web Services fully qualified domain name (FQDN) for your Director pool, if you have one, or for your Front End pool if you do not have a Director</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d178-127">A (Host)</span><span class="sxs-lookup"><span data-stu-id="8d178-127">A (host)</span></span></p></td>
<td><p><span data-ttu-id="8d178-128">lyncdiscoverinternal. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="8d178-128">lyncdiscoverinternal.&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="8d178-129">Interne Web Services-IP-Adresse (virtuelle IP-Adresse (VIP-Adresse), wenn Sie ein Lastenausgleichsmodul verwenden) Ihres Director-Pools, falls vorhanden, oder des Front-End-Pools, wenn Sie keinen Director haben</span><span class="sxs-lookup"><span data-stu-id="8d178-129">Internal Web Services IP address (virtual IP (VIP) address if you use a load balancer) of your Director pool, if you have one, or of your Front End pool if you do not have a Director</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="8d178-130">**Externe DNS-Einträge**</span><span class="sxs-lookup"><span data-stu-id="8d178-130">**External DNS records**</span></span>

<span data-ttu-id="8d178-131">Sie müssen einen der folgenden externen DNS-Einträge erstellen:</span><span class="sxs-lookup"><span data-stu-id="8d178-131">You need to create one of the following external DNS records:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8d178-132">Eintragstyp</span><span class="sxs-lookup"><span data-stu-id="8d178-132">Record type</span></span></th>
<th><span data-ttu-id="8d178-133">Hostname</span><span class="sxs-lookup"><span data-stu-id="8d178-133">Host name</span></span></th>
<th><span data-ttu-id="8d178-134">Auflösung in</span><span class="sxs-lookup"><span data-stu-id="8d178-134">Resolves to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8d178-135">CNAME</span><span class="sxs-lookup"><span data-stu-id="8d178-135">CNAME</span></span></p></td>
<td><p><span data-ttu-id="8d178-136">lyncdiscover.</span><span class="sxs-lookup"><span data-stu-id="8d178-136">lyncdiscover.</span></span> <span data-ttu-id="8d178-137">&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="8d178-137">&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="8d178-138">FQDN externer Webdienste für Ihren Director-Pool, falls vorhanden, oder für Ihren Front-End-Pool, wenn Sie keinen Director haben</span><span class="sxs-lookup"><span data-stu-id="8d178-138">External Web Services FQDN for your Director pool, if you have one, or for your Front End pool if you do not have a Director</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8d178-139">A (Host)</span><span class="sxs-lookup"><span data-stu-id="8d178-139">A (host)</span></span></p></td>
<td><p><span data-ttu-id="8d178-140">lyncdiscover.</span><span class="sxs-lookup"><span data-stu-id="8d178-140">lyncdiscover.</span></span> <span data-ttu-id="8d178-141">&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="8d178-141">&lt;sipdomain&gt;</span></span></p></td>
<td><p><span data-ttu-id="8d178-142">Externe oder öffentliche IP-Adresse (VIP-Adresse, wenn Sie ein Lastenausgleichsmodul verwenden) des Reverse-Proxys</span><span class="sxs-lookup"><span data-stu-id="8d178-142">External or public IP address (VIP address if you use a load balancer) of the reverse proxy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8d178-143">SRV</span><span class="sxs-lookup"><span data-stu-id="8d178-143">SRV</span></span></p></td>
<td><p><span data-ttu-id="8d178-144">_sipfederationtls._tcp.</span><span class="sxs-lookup"><span data-stu-id="8d178-144">_sipfederationtls._tcp.</span></span> <span data-ttu-id="8d178-145">&lt;sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="8d178-145">&lt;sipdomain&gt;</span></span></p>
<p><span data-ttu-id="8d178-146">Behebt einen Host-Eintrag (A oder AAAA) für den Access-Edgedienst</span><span class="sxs-lookup"><span data-stu-id="8d178-146">Resolves to host (A or AAAA) record for the Access Edge service</span></span></p></td>
<td><p><span data-ttu-id="8d178-147">Um den Push-Benachrichtigungsdienst und den Apple Push-Benachrichtigungsdienst zu unterstützen, erstellen Sie für jede SIP-Domäne mit Microsoft lync Mobile-Clients einen SRV-Eintrag.</span><span class="sxs-lookup"><span data-stu-id="8d178-147">To support Push Notification Service and Apple Push Notification service, you create one SRV record for each SIP domain that has Microsoft Lync Mobile clients.</span></span></p>
<div>

> [!IMPORTANT]  
> <span data-ttu-id="8d178-148">Diese Anforderung gilt nur für Microsoft lync Mobile-Clients auf mobilen Apple-oder Microsoft-basierten Geräten.</span><span class="sxs-lookup"><span data-stu-id="8d178-148">This requirement applies only to Microsoft Lync Mobile clients on Apple or Microsoft based mobile devices.</span></span> <span data-ttu-id="8d178-149">Android und Nokia Symbian-Geräte verwenden keine Push-Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="8d178-149">Andriod and Nokia Symbian devices do not use push notification.</span></span>


</div></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="8d178-150">Lyncdiscover, auch als AutoErmittlung bekannt, verkehrt durch den Reverseproxy.</span><span class="sxs-lookup"><span data-stu-id="8d178-150">Lyncdiscover, also known as autodiscover, traffic goes through the reverse proxy.</span></span> <span data-ttu-id="8d178-151">Der SRV-Eintrag verweist auf einen Datensatz, der über den Access-Edgedienst aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="8d178-151">SRV record points to a record that resolves through the Access Edge service.</span></span>



<span data-ttu-id="8d178-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8d178-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

