---
title: 'Lync Server 2013: Anforderungen an Zertifikate für interne Server'
description: 'Lync Server 2013: Zertifikatanforderungen für interne Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate requirements for internal servers
ms:assetid: 0444cdbd-538c-43b1-b9a1-9d7d6cf818d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398094(v=OCS.15)
ms:contentKeyID: 48183270
ms.date: 02/17/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dc1a627dd762c849b848087a96e00e19d320ef01
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435355"
---
# <a name="certificate-requirements-for-internal-servers-in-lync-server-2013"></a><span data-ttu-id="91aed-103">Anforderungen an Zertifikate für interne Server in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="91aed-103">Certificate requirements for internal servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="91aed-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="91aed-104">

<span> </span></span></span>

<span data-ttu-id="91aed-105">_**Letztes Änderungsdatum des Themas:** 2017-02-17_</span><span class="sxs-lookup"><span data-stu-id="91aed-105">_**Topic Last Modified:** 2017-02-17_</span></span>

<span data-ttu-id="91aed-106">Zu den internen Servern, auf denen lync Server ausgeführt wird und für die Zertifikate erforderlich sind, gehören Standard Edition-Server, Enterprise Edition-Front-End-Server, Vermittlungsserver und Director.</span><span class="sxs-lookup"><span data-stu-id="91aed-106">Internal servers that are running Lync Server and that require certificates include Standard Edition server, Enterprise Edition Front End Server, Mediation Server, and Director.</span></span> <span data-ttu-id="91aed-107">In der folgenden Tabelle sind die Zertifikatanforderungen für diese Server aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="91aed-107">The following table shows the certificate requirements for these servers.</span></span> <span data-ttu-id="91aed-108">Sie können den lync Server-Zertifikat-Assistenten verwenden, um diese Zertifikate anzufordern.</span><span class="sxs-lookup"><span data-stu-id="91aed-108">You can use the Lync Server certificate wizard to request these certificates.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="91aed-109">Platzhalterzertifikate werden für die alternativen Subjektnamen unterstützt, die mit den einfachen URLs im Front-End-Pool, Front-End-Server oder Director verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="91aed-109">Wildcard certificates are supported for the subject alternative names associated with the simple URLs on the Front End pool, Front End Server, or Director.</span></span> <span data-ttu-id="91aed-110">Details zur Unterstützung von Platzhalterzertifikaten finden Sie unter <A href="lync-server-2013-wildcard-certificate-support.md">Unterstützung für Platzhalterzertifikate in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="91aed-110">For details about wildcard certificate support, see <A href="lync-server-2013-wildcard-certificate-support.md">Wildcard certificate support in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="91aed-111">Obwohl eine interne Unternehmenszertifizierungsstelle für interne Server empfohlen wird, können Sie auch eine öffentliche Zertifizierungsstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="91aed-111">Although an internal enterprise certification authority (CA) is recommended for internal servers, you can also use a public CA.</span></span> <span data-ttu-id="91aed-112">Eine Liste der öffentlichen Zertifizierungsstellen, die Zertifikate zur Verfügung stellen, die bestimmte Anforderungen für Unified Communications (UC)-Zertifikate erfüllen und mit Microsoft zusammenarbeiten, um sicherzustellen, dass Sie mit dem lync Server-Zertifikat-Assistenten funktionieren, finden Sie im Artikel Microsoft Knowledge Base 929395, "Unified Communications Certificate Partners für Exchange Server und für Communications Server" unter [https://go.microsoft.com/fwlink/p/?linkId=202834](https://go.microsoft.com/fwlink/p/?linkid=202834) .</span><span class="sxs-lookup"><span data-stu-id="91aed-112">For a list of public CAs that provide certificates that comply with specific requirements for unified communications (UC) certificates and have partnered with Microsoft to ensure they work with the Lync Server Certificate Wizard, see article Microsoft Knowledge Base 929395, "Unified Communications Certificate Partners for Exchange Server and for Communications Server," at [https://go.microsoft.com/fwlink/p/?linkId=202834](https://go.microsoft.com/fwlink/p/?linkid=202834).</span></span>

<span data-ttu-id="91aed-113">Die Kommunikation mit anderen Anwendungen und Servern, wie etwa Exchange 2013, erfordert ein Zertifikat, das von den anderen Anwendungen und Produkten unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="91aed-113">Communication with other applications and servers, such as Exchange 2013, requires a certificate that is supported by the other applications and products.</span></span> <span data-ttu-id="91aed-114">Für die 2013-Version unterstützen lync Server 2013 und andere Microsoft-Serverprodukte, einschließlich Exchange 2013 und SharePoint Server, das Open Authorization (OAuth)-Protokoll für die Server-zu-Server-Authentifizierung und-Autorisierung.</span><span class="sxs-lookup"><span data-stu-id="91aed-114">For the 2013 release, Lync Server 2013 and other Microsoft server products, including Exchange 2013 and SharePoint Server, support the Open Authorization (OAuth) protocol for server-to-server authentication and authorization.</span></span> <span data-ttu-id="91aed-115">Ausführliche Informationen finden Sie unter [Verwalten der Server-zu-Server-Authentifizierung (OAuth) und der Partneranwendungen in lync Server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) in der Bereitstellungsdokumentation oder in der Betriebsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="91aed-115">For details, see [Managing server-to-server authentication (OAuth) and partner applications in Lync Server 2013](lync-server-2013-managing-server-to-server-authentication-oauth-and-partner-applications.md) in the Deployment documentation or the Operations documentation.</span></span>

<span data-ttu-id="91aed-116">Für Verbindungen von Clients unter dem BetriebssystemWindows 7, dem BetriebssystemWindows Server 2008, dem BetriebssystemWindows Server 2008 R2, dem BetriebssystemWindows Vista und Microsoft lync Phone Edition bietet lync Server 2013 Unterstützung für (aber nicht erforderliche) Zertifikate, die mit der SHA-256-kryptografischen Hashfunktion signiert wurden.</span><span class="sxs-lookup"><span data-stu-id="91aed-116">For connections from clients running Windows 7 operating system, Windows Server 2008 operating system, Windows Server 2008 R2 operating system, Windows Vista operating system, and Microsoft Lync Phone Edition, Lync Server 2013 includes support for (but does not require) certificates signed using the SHA-256 cryptographic hash function.</span></span> <span data-ttu-id="91aed-117">Um den externen Zugriff mithilfe von SHA-256 zu unterstützen, wird das externe Zertifikat von einer öffentlichen Zertifizierungsstelle mithilfe von SHA-256 ausgestellt.</span><span class="sxs-lookup"><span data-stu-id="91aed-117">To support external access using SHA-256, the external certificate is issued by a public CA using SHA-256.</span></span>

<span data-ttu-id="91aed-118">In den folgenden Tabellen werden die Zertifikatanforderungen nach Serverrolle für Front-End-Pools und Standard Edition-Server angezeigt.</span><span class="sxs-lookup"><span data-stu-id="91aed-118">The following tables show certificate requirements by server role for Front End pools and Standard Edition servers.</span></span> <span data-ttu-id="91aed-119">Dies sind standardmäßige Webserverzertifikate, privater Schlüssel, nicht exportierbarer Server.</span><span class="sxs-lookup"><span data-stu-id="91aed-119">All these are standard web server certificates, private key, non-exportable.</span></span>

<span data-ttu-id="91aed-120">Beachten Sie, dass die erweiterte Schlüsselverwendung von Server automatisch konfiguriert wird, wenn Sie mit dem Zertifikat-Assistenten Zertifikate anfordern.</span><span class="sxs-lookup"><span data-stu-id="91aed-120">Note that server enhanced key usage (EKU) is automatically configured when you use the certificate wizard to request certificates.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="91aed-121">Jeder Zertifikatsanzeige Name muss im Computerspeicher eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="91aed-121">Each certificate Friendly Name must be unique in the computer store.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="91aed-122">Wenn Sie sipinternal.contoso.com oder sipexternal.contoso.com in Ihrem DNS konfiguriert haben, müssen Sie diese im alternativen Antragstellernamen des Zertifikats hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="91aed-122">If you have configured sipinternal.contoso.com or sipexternal.contoso.com in your DNS, you will need to add them in the certificate’s Subject Alternative Name.</span></span>



</div>

### <a name="certificates-for-standard-edition-server"></a><span data-ttu-id="91aed-123">Zertifikate für den Standard Edition-Server</span><span class="sxs-lookup"><span data-stu-id="91aed-123">Certificates for Standard Edition Server</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91aed-124">Zertifikat</span><span class="sxs-lookup"><span data-stu-id="91aed-124">Certificate</span></span></th>
<th><span data-ttu-id="91aed-125">Name des Antragstellers/gebräuchlicher Name</span><span class="sxs-lookup"><span data-stu-id="91aed-125">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="91aed-126">Alternativer Antragstellername</span><span class="sxs-lookup"><span data-stu-id="91aed-126">Subject alternative name</span></span></th>
<th><span data-ttu-id="91aed-127">Beispiel</span><span class="sxs-lookup"><span data-stu-id="91aed-127">Example</span></span></th>
<th><span data-ttu-id="91aed-128">Kommentare</span><span class="sxs-lookup"><span data-stu-id="91aed-128">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91aed-129">Standard</span><span class="sxs-lookup"><span data-stu-id="91aed-129">Default</span></span></p></td>
<td><p><span data-ttu-id="91aed-130">Vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Pools</span><span class="sxs-lookup"><span data-stu-id="91aed-130">Fully qualified domain name (FQDN) of the pool</span></span></p></td>
<td><p><span data-ttu-id="91aed-131">FQDN des Pools und der FQDN des Servers</span><span class="sxs-lookup"><span data-stu-id="91aed-131">FQDN of the pool and the FQDN of the server</span></span></p>
<p><span data-ttu-id="91aed-132">Wenn mehrere SIP-Domänen vorhanden sind und die automatische Clientkonfiguration aktiviert wurde, erkennt der Zertifikat-Assistent die unterstützten FQDNs für SIP-Domänen und fügt diese hinzu.</span><span class="sxs-lookup"><span data-stu-id="91aed-132">If you have multiple SIP domains and have enabled automatic client configuration, the certificate wizard detects and adds each supported SIP domain FQDNs.</span></span></p>
<p><span data-ttu-id="91aed-133">Wenn es sich bei diesem Pool um den Server für die automatische Anmeldung für Clients handelt und in den Gruppenrichtlinien der exakte DNS-Abgleich (Domain Name System) festgelegt ist, benötigen Sie auch Einträge für „sip.sipDomäne“ (für jede vorhandene SIP-Domäne).</span><span class="sxs-lookup"><span data-stu-id="91aed-133">If this pool is the auto-logon server for clients and strict Domain Name System (DNS) matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="91aed-134">SN=se01.contoso.com; SAN=se01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="91aed-134">SN=se01.contoso.com; SAN=se01.contoso.com</span></span></p>
<p><span data-ttu-id="91aed-135">Wenn es sich bei diesem Pool um den Server für die automatische Anmeldung für Clients handelt und in den Gruppenrichtlinien der exakte DNS-Abgleich festgelegt ist, benötigen Sie auch „SAN=sip.contoso.com; SAN=sip.fabrikam.com“.</span><span class="sxs-lookup"><span data-stu-id="91aed-135">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="91aed-136">Auf dem Standard Edition-Server entspricht der Server-FQDN dem FQDN des Pools.</span><span class="sxs-lookup"><span data-stu-id="91aed-136">On Standard Edition server, the server FQDN is the same as the pool FQDN.</span></span></p>
<p><span data-ttu-id="91aed-137">Der Assistent erkennt alle SIP-Domänen, die Sie während der Installation angegeben haben, und fügt sie automatisch zum alternativen Antragstellernamen (SAN) hinzu.</span><span class="sxs-lookup"><span data-stu-id="91aed-137">The wizard detects any SIP domains you specified during setup and automatically adds them to the subject alternative name.</span></span></p>
<p><span data-ttu-id="91aed-138">Sie können dieses Zertifikat auch für die Server-zu-Server-Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="91aed-138">You can also use this certificate for Server-to-Server Authentication.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91aed-139">Web, intern</span><span class="sxs-lookup"><span data-stu-id="91aed-139">Web internal</span></span></p></td>
<td><p><span data-ttu-id="91aed-140">FQDN des Servers</span><span class="sxs-lookup"><span data-stu-id="91aed-140">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="91aed-141">Jeder der folgenden:</span><span class="sxs-lookup"><span data-stu-id="91aed-141">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="91aed-142">Interner Web-FQDN (entspricht dem FQDN des Servers)</span><span class="sxs-lookup"><span data-stu-id="91aed-142">Internal web FQDN (which is the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="91aed-143">Einfache Besprechungs-URLs</span><span class="sxs-lookup"><span data-stu-id="91aed-143">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="91aed-144">Einfache URLs vom Typ „Dialin“</span><span class="sxs-lookup"><span data-stu-id="91aed-144">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="91aed-145">Einfache URLs vom Typ „Admin“</span><span class="sxs-lookup"><span data-stu-id="91aed-145">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="91aed-146">Oder ein Platzhaltereintrag für die einfachen URLs</span><span class="sxs-lookup"><span data-stu-id="91aed-146">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="91aed-147">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="91aed-147">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="91aed-148">Mit einem Platzhalterzertifikat:</span><span class="sxs-lookup"><span data-stu-id="91aed-148">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="91aed-149">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="91aed-149">SN=se01.contoso.com; SAN=se01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="91aed-150">Sie können den internen Web-FQDN im Topologie-Generator nicht außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="91aed-150">You cannot override the Internal web FQDN in Topology Builder.</span></span></p>
<p><span data-ttu-id="91aed-151">Wenn Sie über mehrere einfache URLs für Besprechungen verfügen, müssen Sie diese als Alternativen Betreff-Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="91aed-151">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="91aed-152">Platzhaltereinträge werden für die Einträge für einfache URLs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91aed-152">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91aed-153">Web, extern</span><span class="sxs-lookup"><span data-stu-id="91aed-153">Web external</span></span></p></td>
<td><p><span data-ttu-id="91aed-154">FQDN des Servers</span><span class="sxs-lookup"><span data-stu-id="91aed-154">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="91aed-155">Jeder der folgenden:</span><span class="sxs-lookup"><span data-stu-id="91aed-155">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="91aed-156">Externer Web-FQDN</span><span class="sxs-lookup"><span data-stu-id="91aed-156">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="91aed-157">Einfache URLs vom Typ „Dialin“</span><span class="sxs-lookup"><span data-stu-id="91aed-157">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="91aed-158">Einfache Besprechungs-URLs pro SIP-Domäne</span><span class="sxs-lookup"><span data-stu-id="91aed-158">Meet simple URLs per SIP domain</span></span></p></li>
<li><p><span data-ttu-id="91aed-159">Oder ein Platzhaltereintrag für die einfachen URLs</span><span class="sxs-lookup"><span data-stu-id="91aed-159">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="91aed-160">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="91aed-160">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="91aed-161">Mit einem Platzhalterzertifikat:</span><span class="sxs-lookup"><span data-stu-id="91aed-161">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="91aed-162">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="91aed-162">SN=se01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="91aed-163">Wenn Sie über mehrere einfache URLs für Besprechungen verfügen, müssen Sie diese als Alternativen Betreff-Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="91aed-163">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="91aed-164">Platzhaltereinträge werden für die Einträge für einfache URLs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91aed-164">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-front-end-server-in-a-front-end-pool"></a><span data-ttu-id="91aed-165">Zertifikate für den Front-End-Server in einem Front-End-Pool</span><span class="sxs-lookup"><span data-stu-id="91aed-165">Certificates for Front End Server in a Front End Pool</span></span>

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91aed-166">Zertifikat</span><span class="sxs-lookup"><span data-stu-id="91aed-166">Certificate</span></span></th>
<th><span data-ttu-id="91aed-167">Name des Antragstellers/gebräuchlicher Name</span><span class="sxs-lookup"><span data-stu-id="91aed-167">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="91aed-168">Alternativer Antragstellername</span><span class="sxs-lookup"><span data-stu-id="91aed-168">Subject alternative name</span></span></th>
<th><span data-ttu-id="91aed-169">Beispiel</span><span class="sxs-lookup"><span data-stu-id="91aed-169">Example</span></span></th>
<th><span data-ttu-id="91aed-170">Kommentare</span><span class="sxs-lookup"><span data-stu-id="91aed-170">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91aed-171">Standard</span><span class="sxs-lookup"><span data-stu-id="91aed-171">Default</span></span></p></td>
<td><p><span data-ttu-id="91aed-172">FQDN des Pools</span><span class="sxs-lookup"><span data-stu-id="91aed-172">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="91aed-173">FQDN des Pools und FQDN des Servers.</span><span class="sxs-lookup"><span data-stu-id="91aed-173">FQDN of the pool and FQDN of the server.</span></span></p>
<p><span data-ttu-id="91aed-174">Wenn mehrere SIP-Domänen vorhanden sind und die automatische Clientkonfiguration aktiviert wurde, erkennt der Zertifikat-Assistent die unterstützten FQDNs für SIP-Domänen und fügt diese hinzu.</span><span class="sxs-lookup"><span data-stu-id="91aed-174">If you have multiple SIP domains and have enabled automatic client configuration, the certificate wizard detects and adds each supported SIP domain FQDNs.</span></span></p>
<p><span data-ttu-id="91aed-175">Wenn dieser Pool der Server für die automatische Anmeldung für Clients ist und in Gruppenrichtlinien strikter DNS-Abgleich erforderlich ist, benötigen Sie auch Einträge für SIP. sipdomain (für jede SIP-Domäne, die Sie haben).</span><span class="sxs-lookup"><span data-stu-id="91aed-175">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="91aed-176">SN=eepool.contoso.com; SAN=eepool.contoso.com; SAN=ee01.contoso.com </span><span class="sxs-lookup"><span data-stu-id="91aed-176">SN=eepool.contoso.com; SAN=eepool.contoso.com; SAN=ee01.contoso.com</span></span></p>
<p><span data-ttu-id="91aed-177">Wenn es sich bei diesem Pool um den Server für die automatische Anmeldung für Clients handelt und in den Gruppenrichtlinien der exakte DNS-Abgleich festgelegt ist, benötigen Sie auch „SAN=sip.contoso.com; SAN=sip.fabrikam.com“.</span><span class="sxs-lookup"><span data-stu-id="91aed-177">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="91aed-178">Der Assistent erkennt alle SIP-Domänen, die Sie während der Installation angegeben haben, und fügt sie automatisch zum alternativen Antragstellernamen (SAN) hinzu.</span><span class="sxs-lookup"><span data-stu-id="91aed-178">The wizard detects any SIP domains you specified during setup and automatically adds them to the subject alternative name.</span></span></p>
<p><span data-ttu-id="91aed-179">Sie können dieses Zertifikat auch für die Server-zu-Server-Authentifizierung verwenden.</span><span class="sxs-lookup"><span data-stu-id="91aed-179">You can also use this certificate for Server-to-Server Authentication.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91aed-180">Web-intern</span><span class="sxs-lookup"><span data-stu-id="91aed-180">Web Internal</span></span></p></td>
<td><p><span data-ttu-id="91aed-181">FQDN des Pools</span><span class="sxs-lookup"><span data-stu-id="91aed-181">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="91aed-182">Jeder der folgenden:</span><span class="sxs-lookup"><span data-stu-id="91aed-182">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="91aed-183">Interner Web-FQDN (entspricht NICHT dem FQDN des Servers)</span><span class="sxs-lookup"><span data-stu-id="91aed-183">Internal web FQDN (which is NOT the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="91aed-184">Server-FQDN</span><span class="sxs-lookup"><span data-stu-id="91aed-184">Server FQDN</span></span></p></li>
<li><p><span data-ttu-id="91aed-185">Lync-Pool-FQDN</span><span class="sxs-lookup"><span data-stu-id="91aed-185">Lync pool FQDN</span></span></p></li>
<li><p><span data-ttu-id="91aed-186">Einfache Besprechungs-URLs</span><span class="sxs-lookup"><span data-stu-id="91aed-186">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="91aed-187">Einfache URLs vom Typ „Dialin“</span><span class="sxs-lookup"><span data-stu-id="91aed-187">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="91aed-188">Einfache URLs vom Typ „Admin“</span><span class="sxs-lookup"><span data-stu-id="91aed-188">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="91aed-189">Oder ein Platzhaltereintrag für die einfachen URLs</span><span class="sxs-lookup"><span data-stu-id="91aed-189">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="91aed-190">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="91aed-190">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="91aed-191">Mit einem Platzhalterzertifikat:</span><span class="sxs-lookup"><span data-stu-id="91aed-191">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="91aed-192">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="91aed-192">SN=ee01.contoso.com; SAN=ee01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="91aed-193">Wenn Sie über mehrere einfache URLs für Besprechungen verfügen, müssen Sie diese als Alternativen Betreff-Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="91aed-193">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="91aed-194">Platzhaltereinträge werden für die Einträge für einfache URLs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91aed-194">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91aed-195">Web, extern</span><span class="sxs-lookup"><span data-stu-id="91aed-195">Web external</span></span></p></td>
<td><p><span data-ttu-id="91aed-196">FQDN des Pools</span><span class="sxs-lookup"><span data-stu-id="91aed-196">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="91aed-197">Jeder der folgenden:</span><span class="sxs-lookup"><span data-stu-id="91aed-197">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="91aed-198">Externer Web-FQDN</span><span class="sxs-lookup"><span data-stu-id="91aed-198">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="91aed-199">Einfache URLs vom Typ „Dialin“</span><span class="sxs-lookup"><span data-stu-id="91aed-199">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="91aed-200">Einfache URLs vom Typ „Admin“</span><span class="sxs-lookup"><span data-stu-id="91aed-200">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="91aed-201">Oder ein Platzhaltereintrag für die einfachen URLs</span><span class="sxs-lookup"><span data-stu-id="91aed-201">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="91aed-202">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="91aed-202">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="91aed-203">Mit einem Platzhalterzertifikat:</span><span class="sxs-lookup"><span data-stu-id="91aed-203">Using a wildcard certificate:</span></span></p>
<p><span data-ttu-id="91aed-204">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="91aed-204">SN=ee01.contoso.com; SAN=webcon01.contoso.com; SAN=\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="91aed-205">Wenn Sie über mehrere einfache URLs für Besprechungen verfügen, müssen Sie diese als Alternativen Betreff-Namen angeben.</span><span class="sxs-lookup"><span data-stu-id="91aed-205">If you have multiple Meet simple URLs, you must include all of them as subject alternative names.</span></span></p>
<p><span data-ttu-id="91aed-206">Platzhaltereinträge werden für die Einträge für einfache URLs unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91aed-206">Wildcard entries are supported for the simple URL entries.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-director"></a><span data-ttu-id="91aed-207">Zertifikate für Director</span><span class="sxs-lookup"><span data-stu-id="91aed-207">Certificates for Director</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91aed-208">Zertifikat</span><span class="sxs-lookup"><span data-stu-id="91aed-208">Certificate</span></span></th>
<th><span data-ttu-id="91aed-209">Name des Antragstellers/gebräuchlicher Name</span><span class="sxs-lookup"><span data-stu-id="91aed-209">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="91aed-210">Alternativer Antragstellername</span><span class="sxs-lookup"><span data-stu-id="91aed-210">Subject alternative name</span></span></th>
<th><span data-ttu-id="91aed-211">Beispiel</span><span class="sxs-lookup"><span data-stu-id="91aed-211">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91aed-212">Standard</span><span class="sxs-lookup"><span data-stu-id="91aed-212">Default</span></span></p></td>
<td><p><span data-ttu-id="91aed-213">FQDN des Director-Pools</span><span class="sxs-lookup"><span data-stu-id="91aed-213">FQDN of the Director pool</span></span></p></td>
<td><p><span data-ttu-id="91aed-214">FQDN des Directors, FQDN des Director-Pools</span><span class="sxs-lookup"><span data-stu-id="91aed-214">FQDN of the Director, FQDN of the Director pool</span></span></p>
<p><span data-ttu-id="91aed-215">Wenn dieser Pool der Server für die automatische Anmeldung für Clients ist und in Gruppenrichtlinien strikter DNS-Abgleich erforderlich ist, benötigen Sie auch Einträge für SIP. sipdomain (für jede SIP-Domäne, die Sie haben).</span><span class="sxs-lookup"><span data-stu-id="91aed-215">If this pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need entries for sip.sipdomain (for each SIP domain you have).</span></span></p></td>
<td><p><span data-ttu-id="91aed-216">SN = dir-Pool.contoso.com; San = dir-Pool.contoso.com; San = dir01. contoso. com</span><span class="sxs-lookup"><span data-stu-id="91aed-216">SN=dir-pool.contoso.com; SAN=dir-pool.contoso.com; SAN=dir01.contoso.com</span></span></p>
<p><span data-ttu-id="91aed-217">Wenn dieser Director-Pool der Server für die automatische Anmeldung für Clients ist und in Gruppenrichtlinien strikter DNS-Abgleich erforderlich ist, benötigen Sie auch San = SIP. contoso. com; San = SIP. fabrikam. com</span><span class="sxs-lookup"><span data-stu-id="91aed-217">If this Director pool is the auto-logon server for clients and strict DNS matching is required in group policy, you also need SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="91aed-218">Web-intern</span><span class="sxs-lookup"><span data-stu-id="91aed-218">Web Internal</span></span></p></td>
<td><p><span data-ttu-id="91aed-219">FQDN des Servers</span><span class="sxs-lookup"><span data-stu-id="91aed-219">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="91aed-220">Jeder der folgenden:</span><span class="sxs-lookup"><span data-stu-id="91aed-220">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="91aed-221">Interner Web-FQDN (entspricht dem FQDN des Servers)</span><span class="sxs-lookup"><span data-stu-id="91aed-221">Internal web FQDN (which is the same as the FQDN of the server)</span></span></p></li>
<li><p><span data-ttu-id="91aed-222">Server-FQDN</span><span class="sxs-lookup"><span data-stu-id="91aed-222">Server FQDN</span></span></p></li>
<li><p><span data-ttu-id="91aed-223">Lync-Pool-FQDN</span><span class="sxs-lookup"><span data-stu-id="91aed-223">Lync pool FQDN</span></span></p></li>
<li><p><span data-ttu-id="91aed-224">Einfache Besprechungs-URLs</span><span class="sxs-lookup"><span data-stu-id="91aed-224">Meet simple URLs</span></span></p></li>
<li><p><span data-ttu-id="91aed-225">Einfache URLs vom Typ „Dialin“</span><span class="sxs-lookup"><span data-stu-id="91aed-225">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="91aed-226">Einfache URLs vom Typ „Admin“</span><span class="sxs-lookup"><span data-stu-id="91aed-226">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="91aed-227">Oder ein Platzhaltereintrag für die einfachen URLs</span><span class="sxs-lookup"><span data-stu-id="91aed-227">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="91aed-228">SN=dir01.contoso.com; SAN=dir01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="91aed-228">SN=dir01.contoso.com; SAN=dir01.contoso.com; SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com; SAN=admin.contoso.com</span></span></p>
<p><span data-ttu-id="91aed-229">SN=dir01.contoso.com; SAN=dir01.contoso.com SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="91aed-229">SN=dir01.contoso.com; SAN=dir01.contoso.com SAN=\*.contoso.com</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="91aed-230">Web, extern</span><span class="sxs-lookup"><span data-stu-id="91aed-230">Web external</span></span></p></td>
<td><p><span data-ttu-id="91aed-231">FQDN des Servers</span><span class="sxs-lookup"><span data-stu-id="91aed-231">FQDN of the server</span></span></p></td>
<td><p><span data-ttu-id="91aed-232">Jeder der folgenden:</span><span class="sxs-lookup"><span data-stu-id="91aed-232">Each of the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="91aed-233">Externer Web-FQDN</span><span class="sxs-lookup"><span data-stu-id="91aed-233">External web FQDN</span></span></p></li>
<li><p><span data-ttu-id="91aed-234">Einfache URLs vom Typ „Dialin“</span><span class="sxs-lookup"><span data-stu-id="91aed-234">Dial-in simple URL</span></span></p></li>
<li><p><span data-ttu-id="91aed-235">Einfache URLs vom Typ „Admin“</span><span class="sxs-lookup"><span data-stu-id="91aed-235">Admin simple URL</span></span></p></li>
<li><p><span data-ttu-id="91aed-236">Oder ein Platzhaltereintrag für die einfachen URLs</span><span class="sxs-lookup"><span data-stu-id="91aed-236">Or, a wildcard entry for the simple URLs</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="91aed-237">Der FQDN des Director External Web muss vom Front-End-Pool oder Front-End-Server abweichen.</span><span class="sxs-lookup"><span data-stu-id="91aed-237">The Director external web FQDN must be different from the Front End pool or Front End Server.</span></span></p>
<p><span data-ttu-id="91aed-238">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="91aed-238">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=meet.contoso.com; SAN=meet.fabrikam.com; SAN=dialin.contoso.com</span></span></p>
<p><span data-ttu-id="91aed-239">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=\*.contoso.com</span><span class="sxs-lookup"><span data-stu-id="91aed-239">SN=dir01.contoso.com; SAN=directorwebcon01.contoso.com SAN=\*.contoso.com</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="91aed-240">Wenn Sie über einen eigenständigen vermittlungsserverpool verfügen, benötigen die Vermittlungsserver jeweils die in der folgenden Tabelle aufgelisteten Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="91aed-240">If you have a stand-alone Mediation Server pool, the Mediation Servers in it each need the certificates listed in the following table.</span></span> <span data-ttu-id="91aed-241">Wenn Sie den Vermittlungs Server mit den Front-End-Servern collocate, genügen die Zertifikate, die in der Tabelle "Zertifikate für Front-End-Server im Front-End-Pool" weiter oben in diesem Thema aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="91aed-241">If you collocate Mediation Server with the Front End Servers, the certificates listed in the “Certificates for Front End Server in Front End Pool” table earlier in this topic are sufficient.</span></span>

### <a name="certificates-for-stand-alone-mediation-server"></a><span data-ttu-id="91aed-242">Zertifikate für eigenständigen Vermittlungs Server</span><span class="sxs-lookup"><span data-stu-id="91aed-242">Certificates for Stand-alone Mediation Server</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91aed-243">Zertifikat</span><span class="sxs-lookup"><span data-stu-id="91aed-243">Certificate</span></span></th>
<th><span data-ttu-id="91aed-244">Name des Antragstellers/gebräuchlicher Name</span><span class="sxs-lookup"><span data-stu-id="91aed-244">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="91aed-245">Alternativer Antragstellername</span><span class="sxs-lookup"><span data-stu-id="91aed-245">Subject alternative name</span></span></th>
<th><span data-ttu-id="91aed-246">Beispiel</span><span class="sxs-lookup"><span data-stu-id="91aed-246">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91aed-247">Standard</span><span class="sxs-lookup"><span data-stu-id="91aed-247">Default</span></span></p></td>
<td><p><span data-ttu-id="91aed-248">FQDN des Pools</span><span class="sxs-lookup"><span data-stu-id="91aed-248">FQDN of the pool</span></span></p></td>
<td><p><span data-ttu-id="91aed-249">FQDN des Pools</span><span class="sxs-lookup"><span data-stu-id="91aed-249">FQDN of the pool</span></span></p>
<p><span data-ttu-id="91aed-250">FQDN des Pool Mitgliedsservers</span><span class="sxs-lookup"><span data-stu-id="91aed-250">FQDN of pool member server</span></span></p></td>
<td><p><span data-ttu-id="91aed-251">SN=medsvr-pool.contoso.net; SAN=medsvr-pool.contoso.net; SAN=medsvr01.contoso.net</span><span class="sxs-lookup"><span data-stu-id="91aed-251">SN=medsvr-pool.contoso.net; SAN=medsvr-pool.contoso.net; SAN=medsvr01.contoso.net</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="certificates-for-survivable-branch-appliance"></a><span data-ttu-id="91aed-252">Zertifikate für Survivable Branch Appliance</span><span class="sxs-lookup"><span data-stu-id="91aed-252">Certificates for Survivable Branch Appliance</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="91aed-253">Zertifikat</span><span class="sxs-lookup"><span data-stu-id="91aed-253">Certificate</span></span></th>
<th><span data-ttu-id="91aed-254">Name des Antragstellers/gebräuchlicher Name</span><span class="sxs-lookup"><span data-stu-id="91aed-254">Subject name/ Common name</span></span></th>
<th><span data-ttu-id="91aed-255">Alternativer Antragstellername</span><span class="sxs-lookup"><span data-stu-id="91aed-255">Subject alternative name</span></span></th>
<th><span data-ttu-id="91aed-256">Beispiel</span><span class="sxs-lookup"><span data-stu-id="91aed-256">Example</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="91aed-257">Standard</span><span class="sxs-lookup"><span data-stu-id="91aed-257">Default</span></span></p></td>
<td><p><span data-ttu-id="91aed-258">FQDN der Anwendung</span><span class="sxs-lookup"><span data-stu-id="91aed-258">FQDN of the appliance</span></span></p></td>
<td><p><span data-ttu-id="91aed-259">SIP. &lt; sipdomain &gt; (benötigt einen Eintrag pro SIP-Domäne)</span><span class="sxs-lookup"><span data-stu-id="91aed-259">SIP.&lt;sipdomain&gt; (need one entry per SIP domain)</span></span></p></td>
<td><p><span data-ttu-id="91aed-260">SN=sba01.contoso.net; SAN=sip.contoso.com; SAN=sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="91aed-260">SN=sba01.contoso.net; SAN=sip.contoso.com; SAN=sip.fabrikam.com</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="91aed-261">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91aed-261">See Also</span></span>


[<span data-ttu-id="91aed-262">Unterstützung von Platzhalterzertifikaten in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="91aed-262">Wildcard certificate support in Lync Server 2013</span></span>](lync-server-2013-wildcard-certificate-support.md)  
  

<span data-ttu-id="91aed-263"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="91aed-263"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

