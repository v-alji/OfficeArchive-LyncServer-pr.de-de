---
title: 'Lync Server 2013: Zertifikatzusammenfassung – AutoErmittlung'
description: 'Lync Server 2013: Zertifikatzusammenfassung – AutoErmittlung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Autodiscover
ms:assetid: 16ac96bb-882a-4141-b75c-9530637548d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945616(v=OCS.15)
ms:contentKeyID: 51541451
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ae421401421434a4c4069c1d90ee287dfb016997
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435349"
---
# <a name="certificate-summary---autodiscover-in-lync-server-2013"></a><span data-ttu-id="85156-103">Zertifikatzusammenfassung – AutoErmittlung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85156-103">Certificate summary - Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="85156-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="85156-104">

<span> </span></span></span>

<span data-ttu-id="85156-105">_**Letztes Änderungsdatum des Themas:** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="85156-105">_**Topic Last Modified:** 2013-02-14_</span></span>

<span data-ttu-id="85156-106">Der lync Server 2013-AutoErmittlungsdienst wird auf den Director-und Front-End-Pool Servern ausgeführt und kann bei Veröffentlichung in DNS von lync-Clients zum Auffinden von Server-und Benutzerdiensten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85156-106">The Lync Server 2013 Autodiscover Service runs on the Director and Front End pool servers, and when published in DNS, can be used by Lync clients to locate server and user services.</span></span> <span data-ttu-id="85156-107">Wenn Sie ein Upgrade von lync Server 2010 durchführen und keine Mobilität bereitstellen, bevor Clients die automatische Ermittlung verwenden können, müssen Sie die Listen für alternative Namen für Zertifikats Subjekte auf jedem Director-und Front-End-Server ändern, auf dem der AutoErmittlungsdienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="85156-107">If you are upgrading from Lync Server 2010 and did not deploy Mobility, before clients can use automatic discovery, you must modify certificate subject alternative name lists on any Director and Front End Server running the Autodiscover Service.</span></span> <span data-ttu-id="85156-108">Darüber hinaus ist es möglicherweise erforderlich, die Listen Betreff alternativer Name auf Zertifikaten zu ändern, die für externe Webdienst Veröffentlichungsregeln für umgekehrte Proxys verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="85156-108">In addition, it may be necessary to modify the subject alternative name lists on certificates used for external web service publishing rules on reverse proxies.</span></span>

<span data-ttu-id="85156-109">Die Entscheidung darüber, ob die Listen Betreff alternativer Namen in umgekehrten Proxys verwendet werden, basiert darauf, ob Sie den AutoErmittlungsdienst auf Port 80 oder auf Port 443 veröffentlichen:</span><span class="sxs-lookup"><span data-stu-id="85156-109">The decision about whether to use subject alternative name lists on reverse proxies is based on whether you publish the Autodiscover Service on port 80 or on port 443:</span></span>

  - <span data-ttu-id="85156-110">**Veröffentlicht auf Port 80**   Wenn die ursprüngliche Abfrage des AutoErmittlungsdiensts über Port 80 erfolgt, sind keine Zertifikat Änderungen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="85156-110">**Published on port 80**   No certificate changes are required if the initial query to the Autodiscover Service occurs over port 80.</span></span> <span data-ttu-id="85156-111">Dies liegt daran, dass Mobile Geräte, auf denen lync ausgeführt wird, auf den Reverseproxy auf Port 80 extern zugreifen und dann intern mit einem Director oder Front-End-Server auf Port 8080 überbrückt werden.</span><span class="sxs-lookup"><span data-stu-id="85156-111">This is because mobile devices running Lync will access the reverse proxy on port 80 externally and then be bridged to a Director or Front End Server on port 8080 internally.</span></span> <span data-ttu-id="85156-112">Ausführliche Informationen finden Sie im Abschnitt "ursprünglicher Auto Ermittlungsprozess mit Port 80" unter [Technische Voraussetzungen für Mobilität in lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="85156-112">For details, see the "Initial Autodiscover Process Using Port 80" section [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span></span>

  - <span data-ttu-id="85156-113">**Veröffentlicht auf Port 443**   Die Liste Subject Alternative Name für Zertifikate, die von der externen Webdienste-Veröffentlichungsregel verwendet werden, muss eine *lyncdiscover enthalten. \<sipdomain\>*</span><span class="sxs-lookup"><span data-stu-id="85156-113">**Published on port 443**   The subject alternative name list on certificates used by the external web services publishing rule must contain a *lyncdiscover.\<sipdomain\>*</span></span> <span data-ttu-id="85156-114">Eintrag für jede SIP-Domäne innerhalb Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="85156-114">entry for each SIP domain within your organization.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="85156-115">Es wird dringend empfohlen, HTTPS über HTTP zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="85156-115">We highly recommend using HTTPS over HTTP.</span></span> <span data-ttu-id="85156-116">HTTPS verwendet Zertifikate, um den Datenverkehr zu verschlüsseln.</span><span class="sxs-lookup"><span data-stu-id="85156-116">HTTPS uses certificates to encrypt traffic.</span></span> <span data-ttu-id="85156-117">HTTP bietet keine Verschlüsselung, und die gesendeten Daten sind nur Text.</span><span class="sxs-lookup"><span data-stu-id="85156-117">HTTP does not provide for encryption, and any data sent will be plain text.</span></span>

    
    </div>

<span data-ttu-id="85156-118">Das erneute ausgeben von Zertifikaten mithilfe einer internen Zertifizierungsstelle ist in der Regel ein einfacher Prozess.</span><span class="sxs-lookup"><span data-stu-id="85156-118">Reissuing certificates by using an internal certificate authority is typically a simple process.</span></span> <span data-ttu-id="85156-119">Bei öffentlichen Zertifikaten, die für die Veröffentlichungsregel des Webdiensts verwendet werden, kann das Hinzufügen von Einträgen mit mehreren Alternativen Subjekten teuer werden.</span><span class="sxs-lookup"><span data-stu-id="85156-119">But for public certificates used on the web service publishing rule, adding multiple subject alternative name entries can become expensive.</span></span> <span data-ttu-id="85156-120">Um dieses Problem zu umgehen, unterstützen wir die anfängliche automatische Ermittlungs Verbindung über Port 80, die dann auf Port 8080 auf dem Director-oder Front-End-Server umgeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="85156-120">To work around this issue, we support the initial automatic discovery connection over port 80, which is then redirected to port 8080 on the Director or Front End Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="85156-121">Wenn Ihre lync Server 2013-Infrastruktur interne Zertifikate verwendet, die von einer internen Zertifizierungsstelle (Certification Authority, ca) ausgestellt wurden, und Sie beabsichtigen, Mobile Geräte drahtlos zu unterstützen, muss entweder die Stammzertifikatkette von der internen Zertifizierungsstelle auf den mobilen Geräten installiert sein, oder Sie müssen zu einem öffentlichen Zertifikat in ihrer lync Server 2013-Infrastruktur wechseln.</span><span class="sxs-lookup"><span data-stu-id="85156-121">If your Lync Server 2013 infrastructure uses internal certificates that are issued from an internal certification authority (CA) and you plan to support mobile devices connecting wirelessly, either the root certificate chain from the internal CA must be installed on the mobile devices or you must change to a public certificate on your Lync Server 2013 infrastructure.</span></span>



</div>

<span data-ttu-id="85156-122">In diesem Thema werden die für Director, Front-End-Server und Reverse Proxy erforderlichen zusätzlichen alternativen Namen für Subjekte beschrieben.</span><span class="sxs-lookup"><span data-stu-id="85156-122">This topic describes the added subject alternative names required for the Director, Front End Server and reverse proxy.</span></span> <span data-ttu-id="85156-123">Es werden nur die zusätzlichen alternativen Namen (Subject Alternative Names, San) referenziert.</span><span class="sxs-lookup"><span data-stu-id="85156-123">Only the added subject alternative names (SAN) are referenced.</span></span> <span data-ttu-id="85156-124">In den Planungs Abschnitten finden Sie Anleitungen zu den anderen Einträgen auf Zertifikaten.</span><span class="sxs-lookup"><span data-stu-id="85156-124">Refer to the planning sections for guidance on the other entries on certificates.</span></span> <span data-ttu-id="85156-125">Ausführliche Informationen finden Sie unter [Szenarien für den Director in lync Server 2013](lync-server-2013-scenarios-for-the-director.md), [Szenarien für den Zugriff durch externe Benutzer in lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md)und [Szenarien für den Reverse Proxy in lync Server 2013](lync-server-2013-scenarios-for-reverse-proxy.md).</span><span class="sxs-lookup"><span data-stu-id="85156-125">For details, see [Scenarios for the Director in Lync Server 2013](lync-server-2013-scenarios-for-the-director.md), [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md), and [Scenarios for reverse proxy in Lync Server 2013](lync-server-2013-scenarios-for-reverse-proxy.md).</span></span>

<span data-ttu-id="85156-126">In den folgenden Tabellen werden die San-Einträge für die AutoErmittlung für den Director-Pool, den Front-End-Pool und den Reverse-Proxy definiert:</span><span class="sxs-lookup"><span data-stu-id="85156-126">The following tables define the Autodiscover SAN entries for the Director pool, the Front End pool, and the reverse proxy:</span></span>

### <a name="director-pool-certificate-requirements"></a><span data-ttu-id="85156-127">Anforderungen des Director-Pool Zertifikats</span><span class="sxs-lookup"><span data-stu-id="85156-127">Director Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85156-128">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85156-128">Description</span></span></th>
<th><span data-ttu-id="85156-129">Eintrag für den alternativen Antragstellernamen</span><span class="sxs-lookup"><span data-stu-id="85156-129">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85156-130">URL des internen AutoErmittlungsdiensts</span><span class="sxs-lookup"><span data-stu-id="85156-130">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="85156-131">San = lyncdiscoverinternal. &lt; Interner Domänenname&gt;</span><span class="sxs-lookup"><span data-stu-id="85156-131">SAN=lyncdiscoverinternal.&lt;internal domain name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85156-132">URL des externen AutoErmittlungsdiensts</span><span class="sxs-lookup"><span data-stu-id="85156-132">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="85156-133">San = lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="85156-133">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="85156-134">Sie weisen das neu aktualisierte Zertifikat mit dem neuen San-Eintrag dem Standardzertifikat zu.</span><span class="sxs-lookup"><span data-stu-id="85156-134">You assign the newly updated certificate with the new SAN entry to the Default certificate.</span></span> <span data-ttu-id="85156-135">Sie können auch San = \* verwenden. &lt; sipdomain &gt; .</span><span class="sxs-lookup"><span data-stu-id="85156-135">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;.</span></span>



</div>

### <a name="front-end-pool-certificate-requirements"></a><span data-ttu-id="85156-136">Anforderungen für das Front-End-Pool Zertifikat</span><span class="sxs-lookup"><span data-stu-id="85156-136">Front End Pool Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85156-137">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85156-137">Description</span></span></th>
<th><span data-ttu-id="85156-138">Eintrag für den alternativen Antragstellernamen</span><span class="sxs-lookup"><span data-stu-id="85156-138">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85156-139">URL des internen AutoErmittlungsdiensts</span><span class="sxs-lookup"><span data-stu-id="85156-139">Internal Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="85156-140">San = lyncdiscoverinternal. &lt; Interner Domänenname&gt;</span><span class="sxs-lookup"><span data-stu-id="85156-140">SAN=lyncdiscoverinternal.&lt;internal domain name&gt;</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="85156-141">URL des externen AutoErmittlungsdiensts</span><span class="sxs-lookup"><span data-stu-id="85156-141">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="85156-142">San = lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="85156-142">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="85156-143">Sie weisen das neu aktualisierte Zertifikat mit dem neuen San-Eintrag dem Standardzertifikat zu.</span><span class="sxs-lookup"><span data-stu-id="85156-143">You assign the newly updated certificate with the new SAN entry to the Default certificate.</span></span> <span data-ttu-id="85156-144">Sie können auch San = \* verwenden. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="85156-144">Alternatively, you can use SAN=\*.&lt;sipdomain&gt;</span></span>



</div>

### <a name="reverse-proxy-public-ca-certificate-requirements"></a><span data-ttu-id="85156-145">Zertifikatanforderungen für Reverse Proxy (öffentliche Zertifizierungsstelle)</span><span class="sxs-lookup"><span data-stu-id="85156-145">Reverse Proxy (Public CA) Certificate Requirements</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="85156-146">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="85156-146">Description</span></span></th>
<th><span data-ttu-id="85156-147">Eintrag für den alternativen Antragstellernamen</span><span class="sxs-lookup"><span data-stu-id="85156-147">Subject alternative name entry</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="85156-148">URL des externen AutoErmittlungsdiensts</span><span class="sxs-lookup"><span data-stu-id="85156-148">External Autodiscover Service URL</span></span></p></td>
<td><p><span data-ttu-id="85156-149">San = lyncdiscover. &lt; sipdomain&gt;</span><span class="sxs-lookup"><span data-stu-id="85156-149">SAN=lyncdiscover.&lt;sipdomain&gt;</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="85156-150">Sie weisen das neu aktualisierte Zertifikat dem SSL-Listener auf dem Reverse-Proxy mit dem neuen San-Eintrag zu.</span><span class="sxs-lookup"><span data-stu-id="85156-150">You assign the newly updated certificate with the new SAN entry to the SSL Listener on the reverse proxy.</span></span>



<span data-ttu-id="85156-151"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="85156-151"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

