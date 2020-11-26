---
title: 'Lync Server 2013: Zertifikatzusammenfassung für einen einzelnen konsolidierten Edgeserver mit privaten IP-Adressen und NAT'
description: 'Lync Server 2013: Zertifikatzusammenfassung – einzelner konsolidierter Edge mit privaten IP-Adressen mithilfe von NAT.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Single consolidated edge with private IP addresses using NAT
ms:assetid: 6de6680e-5f47-48e6-8e06-4994d710ea6d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398519(v=OCS.15)
ms:contentKeyID: 48184433
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 53c8fa23bd7d5a2faf91da956d363474095a09d7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435201"
---
# <a name="certificate-summary---single-consolidated-edge-with-private-ip-addresses-using-nat-in-lync-server-2013"></a><span data-ttu-id="a11aa-103">Zertifikatzusammenfassung für einen einzelnen konsolidierten Edgeserver mit privaten IP-Adressen und NAT in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a11aa-103">Certificate summary - Single consolidated edge with private IP addresses using NAT in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a11aa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a11aa-104">

<span> </span></span></span>

<span data-ttu-id="a11aa-105">_**Letztes Änderungsdatum des Themas:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="a11aa-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="a11aa-106">Microsoft lync Server 2013 verwendet Zertifikate zur gegenseitigen Authentifizierung anderer Server und zum Verschlüsseln von Daten von Server zu Server und Server auf dem Client.</span><span class="sxs-lookup"><span data-stu-id="a11aa-106">Microsoft Lync Server 2013 uses certificates to mutually authenticate other servers and to encrypt data from server to server and server to client.</span></span> <span data-ttu-id="a11aa-107">Für Zertifikate ist eine Namensübereinstimmung der DNS-Einträge (Domain Name System) erforderlich, die den Servern zugeordnet sind, sowie der Antragstellername (SN) und der Alternative Name (Subject Alternative Name, San) auf dem Zertifikat.</span><span class="sxs-lookup"><span data-stu-id="a11aa-107">Certificates require name matching of the domain name system (DNS) records associated with the servers and the subject name (SN) and subject alternative name (SAN) on the certificate.</span></span> <span data-ttu-id="a11aa-108">Damit Server, DNS-Einträge und Zertifikat Einträge erfolgreich zugeordnet werden können, müssen Sie die vollqualifizierten Domänennamen für den vorgesehenen Server sorgfältig planen, wie Sie in DNS und den Einträgen SN und San auf dem Zertifikat registriert sind.</span><span class="sxs-lookup"><span data-stu-id="a11aa-108">To successfully map servers, DNS records and certificate entries, you must carefully plan your intended server fully qualified domain names as registered in DNS and the SN and SAN entries on the certificate.</span></span>

<span data-ttu-id="a11aa-109">Das Zertifikat, das den externen Schnittstellen des Edge-Servers zugewiesen ist, wird von einer öffentlichen Zertifizierungsstelle angefordert.</span><span class="sxs-lookup"><span data-stu-id="a11aa-109">The certificate assigned to the external interfaces of the Edge Server is requested from a public certification authority (CA).</span></span> <span data-ttu-id="a11aa-110">Öffentliche CAS, die bei der Bereitstellung von Zertifikaten für die Zwecke der Unified Communications erfolgreich sind, sind im folgenden Artikel aufgeführt: [https://go.microsoft.com/fwlink/p/?linkid=3052\&kbid=929395](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=929395) .</span><span class="sxs-lookup"><span data-stu-id="a11aa-110">Public CAs that have demonstrated success in supplying certificates for the purposes of Unified Communications are listed in the following article: [https://go.microsoft.com/fwlink/p/?linkid=3052\&kbid=929395](https://go.microsoft.com/fwlink/p/?linkid=3052%26kbid=929395).</span></span> <span data-ttu-id="a11aa-111">Wenn Sie das Zertifikat anfordern, können Sie die vom lync Server-Bereitstellungs-Assistenten generierte Zertifikatanforderung verwenden oder die Anforderung manuell mithilfe der lync Server-Verwaltungsshell-Cmdlets oder durch einen Prozess erstellen, der von einer öffentlichen Zertifizierungsstelle bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="a11aa-111">When requesting the certificate, you can use the certificate request generated by the Lync Server Deployment Wizard or create the request manually using Lync Server Management Shell cmdlets or by a process provided by a public CA.</span></span> <span data-ttu-id="a11aa-112">Ausführliche Informationen zu Cmdlets der lync Server-Verwaltungsshell für die Zertifikatverwaltung finden Sie unter [Zertifikats-und Authentifizierungs-Cmdlets in lync Server 2013](https://docs.microsoft.com/powershell/module/skype/) bei der Zuweisung des Zertifikats wird das Zertifikat der Access-Edgedienst-Schnittstelle, der Edgedienst-Schnittstelle für Webkonferenzen und dem Audio/Video-Authentifizierungsdienst zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a11aa-112">For details on Lync Server Management Shell cmdlets for certificate management, see [Certificate and authentication cmdlets in Lync Server 2013](https://docs.microsoft.com/powershell/module/skype/) When assigning the certificate, the certificate is assigned to the Access Edge service interface, the Web Conferencing Edge service interface, and the Audio/Video Authentication service.</span></span> <span data-ttu-id="a11aa-113">Der Audio-und Video Authentifizierungsdienst sollte nicht mit dem a/V-Edgedienst verwechselt werden, der kein Zertifikat zum Verschlüsseln der Audio-und Videodatenströme verwendet.</span><span class="sxs-lookup"><span data-stu-id="a11aa-113">The Audio/Video Authentication service should not be confused with the A/V Edge service which does not use a certificate to encrypt the audio and video streams.</span></span> <span data-ttu-id="a11aa-114">Die Schnittstelle für den internen Edgeserver kann ein Zertifikat von einer internen Zertifizierungsstelle (in Ihrer Organisation) oder einem Zertifikat einer öffentlichen Zertifizierungsstelle verwenden.</span><span class="sxs-lookup"><span data-stu-id="a11aa-114">The internal Edge Server interface can use a certificate from an internal (to your organization) CA or a certificate from a public CA.</span></span> <span data-ttu-id="a11aa-115">Das interne Schnittstellen Zertifikat verwendet nur SN und benötigt keine San-Einträge.</span><span class="sxs-lookup"><span data-stu-id="a11aa-115">The internal interface certificate uses only the SN and does not need or use SAN entries.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a11aa-116">Die folgende Tabelle zeigt einen zweiten SIP-Eintrag (SIP.fabrikam.com) in der Liste Betreff-alternativer Name als Referenz.</span><span class="sxs-lookup"><span data-stu-id="a11aa-116">The following table shows a second SIP entry (sip.fabrikam.com) in the subject alternative name list for reference.</span></span> <span data-ttu-id="a11aa-117">Für jede SIP-Domäne in Ihrer Organisation müssen Sie einen entsprechenden FQDN hinzufügen, der in der Liste Zertifikat Antragsteller-alternativer Name aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="a11aa-117">For each SIP domain in your organization, you need to add a corresponding FQDN listed in the certificate subject alternative name list.</span></span>



</div>

<div>

## <a name="certificates-required-for-single-consolidated-edge-with-private-ip-addresses-using-nat"></a><span data-ttu-id="a11aa-118">Zertifikate, die für einen einzelnen konsolidierten Edge mit privaten IP-Adressen mithilfe von NAT erforderlich sind</span><span class="sxs-lookup"><span data-stu-id="a11aa-118">Certificates Required for Single Consolidated Edge with Private IP Addresses using NAT</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a11aa-119">Komponente</span><span class="sxs-lookup"><span data-stu-id="a11aa-119">Component</span></span></th>
<th><span data-ttu-id="a11aa-120">Antragstellername</span><span class="sxs-lookup"><span data-stu-id="a11aa-120">Subject name (SN)</span></span></th>
<th><span data-ttu-id="a11aa-121">Subject Alternative Names (San)/Order</span><span class="sxs-lookup"><span data-stu-id="a11aa-121">Subject alternative names (SAN)/Order</span></span></th>
<th><span data-ttu-id="a11aa-122">Kommentare</span><span class="sxs-lookup"><span data-stu-id="a11aa-122">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a11aa-123">Einzelner konsolidierter Rand (externer Rand)</span><span class="sxs-lookup"><span data-stu-id="a11aa-123">Single consolidated Edge (External Edge)</span></span></p></td>
<td><p><span data-ttu-id="a11aa-124">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a11aa-124">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a11aa-125">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a11aa-125">webcon.contoso.com</span></span></p>
<p><span data-ttu-id="a11aa-126">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a11aa-126">sip.contoso.com</span></span></p>
<p><span data-ttu-id="a11aa-127">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="a11aa-127">sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="a11aa-128">Das Zertifikat muss von einer öffentlichen Zertifizierungsstelle sein und muss über die Server-EKU und den Client-EKU verfügen, wenn öffentliche Chat Verbindungen mit AOL bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a11aa-128">Certificate must be from a Public CA, and must have the server EKU and client EKU if public IM connectivity with AOL is to be deployed.</span></span> <span data-ttu-id="a11aa-129">Das Zertifikat wird den externen Edge-Schnittstellen für Folgendes zugewiesen:</span><span class="sxs-lookup"><span data-stu-id="a11aa-129">The certificate is assigned to the external Edge interfaces for:</span></span></p>
<ul>
<li><p><span data-ttu-id="a11aa-130">Zugriffs-Edge</span><span class="sxs-lookup"><span data-stu-id="a11aa-130">Access Edge</span></span></p></li>
<li><p><span data-ttu-id="a11aa-131">Konferenz Kante</span><span class="sxs-lookup"><span data-stu-id="a11aa-131">Conferencing Edge</span></span></p></li>
<li><p><span data-ttu-id="a11aa-132">A/V-Edge</span><span class="sxs-lookup"><span data-stu-id="a11aa-132">A/V Edge</span></span></p></li>
</ul>
<p><span data-ttu-id="a11aa-133">Beachten Sie, dass Sans automatisch dem Zertifikat basierend auf ihren Definitionen im Topologie-Generator hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a11aa-133">Note that SANs are automatically added to the certificate based on your definitions in Topology Builder.</span></span> <span data-ttu-id="a11aa-134">Für zusätzliche SIP-Domänen und andere Einträge, die Sie unterstützen müssen, fügen Sie nach Bedarf San-Einträge hinzu.</span><span class="sxs-lookup"><span data-stu-id="a11aa-134">You add SAN entries as needed for additional SIP domains and other entries that you need to support.</span></span> <span data-ttu-id="a11aa-135">Der Antragstellername wird im San repliziert und muss für den korrekten Betrieb vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="a11aa-135">The subject name is replicated in the SAN and must be present for correct operation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a11aa-136">Einzelner konsolidierter Rand (interner Rand)</span><span class="sxs-lookup"><span data-stu-id="a11aa-136">Single consolidated Edge (Internal Edge)</span></span></p></td>
<td><p><span data-ttu-id="a11aa-137">lsedge.contoso.net</span><span class="sxs-lookup"><span data-stu-id="a11aa-137">lsedge.contoso.net</span></span></p></td>
<td><p><span data-ttu-id="a11aa-138">Kein San erforderlich</span><span class="sxs-lookup"><span data-stu-id="a11aa-138">No SAN required</span></span></p></td>
<td><p><span data-ttu-id="a11aa-139">Das Zertifikat kann von einer öffentlichen oder privaten Zertifizierungsstelle ausgestellt werden und muss die Server-EKU enthalten.</span><span class="sxs-lookup"><span data-stu-id="a11aa-139">Certificate can be issued by a public or private CA, and must contain the server EKU.</span></span> <span data-ttu-id="a11aa-140">Das Zertifikat wird der Schnittstelle für den internen Rand zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="a11aa-140">The certificate is assigned to the internal Edge interface.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="certificate-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="a11aa-141">Zusammenfassung des Zertifikats – öffentliche Instant Messaging-Konnektivität</span><span class="sxs-lookup"><span data-stu-id="a11aa-141">Certificate Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a11aa-142">Komponente</span><span class="sxs-lookup"><span data-stu-id="a11aa-142">Component</span></span></th>
<th><span data-ttu-id="a11aa-143">Name des Antragstellers</span><span class="sxs-lookup"><span data-stu-id="a11aa-143">Subject name</span></span></th>
<th><span data-ttu-id="a11aa-144">Subject Alternative Names (San)/Order</span><span class="sxs-lookup"><span data-stu-id="a11aa-144">Subject alternative names (SAN)/Order</span></span></th>
<th><span data-ttu-id="a11aa-145">Kommentare</span><span class="sxs-lookup"><span data-stu-id="a11aa-145">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a11aa-146">Extern/Access-Edge</span><span class="sxs-lookup"><span data-stu-id="a11aa-146">External/Access Edge</span></span></p></td>
<td><p><span data-ttu-id="a11aa-147">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a11aa-147">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a11aa-148">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a11aa-148">sip.contoso.com</span></span></p>
<p><span data-ttu-id="a11aa-149">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a11aa-149">webcon.contoso.com</span></span></p>
<p><span data-ttu-id="a11aa-150">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="a11aa-150">sip.fabrikam.com</span></span></p></td>
<td><p><span data-ttu-id="a11aa-151">Das Zertifikat muss von einer öffentlichen Zertifizierungsstelle sein und muss über die Server-EKU und den Client-EKU verfügen, wenn öffentliche Chat Verbindungen mit AOL bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="a11aa-151">Certificate must be from a Public CA, and must have the server EKU and client EKU if public IM connectivity with AOL is to be deployed.</span></span> <span data-ttu-id="a11aa-152">Das Zertifikat wird den externen Edge-Schnittstellen für Folgendes zugewiesen:</span><span class="sxs-lookup"><span data-stu-id="a11aa-152">The certificate is assigned to the external Edge interfaces for:</span></span></p>
<ul>
<li><p><span data-ttu-id="a11aa-153">Zugriffs-Edge</span><span class="sxs-lookup"><span data-stu-id="a11aa-153">Access Edge</span></span></p></li>
<li><p><span data-ttu-id="a11aa-154">Konferenz Kante</span><span class="sxs-lookup"><span data-stu-id="a11aa-154">Conferencing Edge</span></span></p></li>
<li><p><span data-ttu-id="a11aa-155">A/V-Edge</span><span class="sxs-lookup"><span data-stu-id="a11aa-155">A/V Edge</span></span></p></li>
</ul>
<p><span data-ttu-id="a11aa-156">Beachten Sie, dass Sans automatisch dem Zertifikat basierend auf ihren Definitionen im Topologie-Generator hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="a11aa-156">Note that SANs are automatically added to the certificate based on your definitions in Topology Builder.</span></span> <span data-ttu-id="a11aa-157">Für zusätzliche SIP-Domänen und andere Einträge, die Sie unterstützen müssen, fügen Sie nach Bedarf San-Einträge hinzu.</span><span class="sxs-lookup"><span data-stu-id="a11aa-157">You add SAN entries as needed for additional SIP domains and other entries that you need to support.</span></span> <span data-ttu-id="a11aa-158">Der Antragstellername wird im San repliziert und muss für den korrekten Betrieb vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="a11aa-158">The subject name is replicated in the SAN and must be present for correct operation.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="certificate-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="a11aa-159">Zertifikatzusammenfassung für erweiterbares Messaging und Anwesenheits Protokoll</span><span class="sxs-lookup"><span data-stu-id="a11aa-159">Certificate Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a11aa-160">Komponente</span><span class="sxs-lookup"><span data-stu-id="a11aa-160">Component</span></span></th>
<th><span data-ttu-id="a11aa-161">Name des Antragstellers</span><span class="sxs-lookup"><span data-stu-id="a11aa-161">Subject name</span></span></th>
<th><span data-ttu-id="a11aa-162">Subject Alternative Names (San)/Order</span><span class="sxs-lookup"><span data-stu-id="a11aa-162">Subject alternative names (SAN)/Order</span></span></th>
<th><span data-ttu-id="a11aa-163">Kommentare</span><span class="sxs-lookup"><span data-stu-id="a11aa-163">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a11aa-164">Zuweisen des Zugriffs-Edgedienst des Edge-Servers oder Edge-Pools</span><span class="sxs-lookup"><span data-stu-id="a11aa-164">Assign to Access Edge service of Edge Server or Edge pool</span></span></p></td>
<td><p><span data-ttu-id="a11aa-165">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a11aa-165">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="a11aa-166">webcon.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a11aa-166">webcon.contoso.com</span></span></p>
<p><span data-ttu-id="a11aa-167">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a11aa-167">sip.contoso.com</span></span></p>
<p><span data-ttu-id="a11aa-168">sip.fabrikam.com</span><span class="sxs-lookup"><span data-stu-id="a11aa-168">sip.fabrikam.com</span></span></p>
<p><span data-ttu-id="a11aa-169">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="a11aa-169">xmpp.contoso.com</span></span></p>
<p><span data-ttu-id="a11aa-170"><strong>\*.contoso.com</strong></span><span class="sxs-lookup"><span data-stu-id="a11aa-170"><strong>\*.contoso.com</strong></span></span></p></td>
<td><p><span data-ttu-id="a11aa-171">Die ersten drei San-Einträge sind die normalen San-Einträge für einen Full Edge-Server.</span><span class="sxs-lookup"><span data-stu-id="a11aa-171">The first three SAN entries are the normal SAN entries for a full Edge Server.</span></span> <span data-ttu-id="a11aa-172">Der contoso.com ist der Eintrag, der für den Verbund mit dem XMPP-Partner auf der Stammdomänen Ebene erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a11aa-172">The contoso.com is the entry required for federation with the XMPP partner at the root domain level.</span></span> <span data-ttu-id="a11aa-173">Dieser Eintrag ermöglicht XMPP für alle Domänen mit dem Suffix \*. contoso.com.</span><span class="sxs-lookup"><span data-stu-id="a11aa-173">This entry will allow XMPP for all domains with the suffix \*.contoso.com.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a11aa-174">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a11aa-174">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

