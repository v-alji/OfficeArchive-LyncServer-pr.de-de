---
title: DNS-Zusammenfassung – SIP, XMPP Federation und Public Instant Messaging
description: DNS Summary – SIP, XMPP Federation und Public Instant Messaging.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - SIP, XMPP federation, and public instant messaging
ms:assetid: 1ed24fb8-a849-44c0-a52e-7aef7527e644
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618369(v=OCS.15)
ms:contentKeyID: 49105656
ms.date: 03/09/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f40013b8346cc049f844a827b21bef81a66f6950
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393818"
---
# <a name="dns-summary---sip-xmpp-federation-and-public-instant-messaging-in-lync-server-2013"></a><span data-ttu-id="eebd4-103">DNS-Zusammenfassung – SIP, XMPP Federation und Public Instant Messaging in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eebd4-103">DNS summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eebd4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eebd4-104">

<span> </span></span></span>

<span data-ttu-id="eebd4-105">_**Letztes Änderungsdatum des Themas:** 2017-03-09_</span><span class="sxs-lookup"><span data-stu-id="eebd4-105">_**Topic Last Modified:** 2017-03-09_</span></span>

<span data-ttu-id="eebd4-106">Die DNS-Einträge (Domain Name System), die erforderlich sind, um einen Verbund mit Office Communications Server-oder lync Server-Partnern zu definieren, werden durch ihre Entscheidung bestimmt, die automatische DNS-Erkennung Ihrer Domäne durch andere Perspective-Partner zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="eebd4-106">The Domain Name System (DNS) records that will be required for defining a federation with Office Communications Server or Lync Server partners is determined by your decision to either allow automatic DNS discovery of your domain by other perspective partners.</span></span> <span data-ttu-id="eebd4-107">Wenn Sie die \_ sipfederationtls veröffentlichen. \_ TCP.</span><span class="sxs-lookup"><span data-stu-id="eebd4-107">If you publish the \_sipfederationtls.\_tcp.</span></span> <span data-ttu-id="eebd4-108">*\<SIP domain name\>* SRV-Eintrag, kann jede andere SIP-Verbunddomäne ihren Verbund "entdecken".</span><span class="sxs-lookup"><span data-stu-id="eebd4-108">*\<SIP domain name\>* SRV record, any other SIP federated domain will be able to “discover” your federation.</span></span> <span data-ttu-id="eebd4-109">Sie können steuern, welche Verbunddomänen mit Ihnen kommunizieren können, indem Sie die Einstellungen Domänen und Blockierte Domänen in der lync Server-Systemsteuerung zulassen oder die Konfiguration der zugelassenen oder blockierten Domänen mithilfe der lync Server-Verwaltungsshell und der PowerShell-Cmdlets **Get**, **Sets**, **New**, **Remove-CsAllowedDomain** und **-CsBlockedDomain** festlegen.</span><span class="sxs-lookup"><span data-stu-id="eebd4-109">You can control which federated domains can communicate with you by using the Allows domains and Blocked Domains settings in the Lync Server Control Panel, or by setting the allowed or blocked domains configuration using the Lync Server Management Shell and the **Get**, **Set**, **New**, **Remove-CsAllowedDomain** and **-CsBlockedDomain** PowerShell cmdlets.</span></span> <span data-ttu-id="eebd4-110">Weitere Informationen zum Konfigurieren dieser Einstellungen und zur Verwendung der PowerShell-Cmdlets finden Sie unter " **Verwandte Themen** " am Ende dieses Themas.</span><span class="sxs-lookup"><span data-stu-id="eebd4-110">For additional information on how to configure theses settings and the use of the PowerShell cmdlets, see **Related Topics** at the end of this topic.</span></span>

<span data-ttu-id="eebd4-111">In der Tabelle "Zusammenfassung der DNS-Einträge" werden die erforderlichen Einträge für eine offene oder auffindbare Föderation dargestellt.</span><span class="sxs-lookup"><span data-stu-id="eebd4-111">The DNS records summary table depicts the required entries for an open, or discoverable, federation.</span></span> <span data-ttu-id="eebd4-112">Wenn Sie die Verbund Ermittlung nicht implementieren möchten, können Sie sich entscheiden, die sipfederationtls nicht zu konfigurieren \_ . \_ TCP.</span><span class="sxs-lookup"><span data-stu-id="eebd4-112">If you do not want to implement Federation Discovery, You can decide to not configure the \_sipfederationtls.\_tcp.</span></span> <span data-ttu-id="eebd4-113">*\<SIP domain name\>* Eintrag.</span><span class="sxs-lookup"><span data-stu-id="eebd4-113">*\<SIP domain name\>* record.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="eebd4-114">Es gibt bestimmte Szenarien, in denen Sie über die _sipfederationtls. _tcp verfügen müssen.</span><span class="sxs-lookup"><span data-stu-id="eebd4-114">There are specific scenarios in which you must have the _sipfederationtls._tcp.</span></span> <span data-ttu-id="eebd4-115"><EM> &lt; SIP-Domänen &gt; Namen</EM> -SRV-Eintrag, aber Sie möchten keinen auffindbaren Verbund haben.</span><span class="sxs-lookup"><span data-stu-id="eebd4-115"><EM>&lt;SIP domain name&gt;</EM> SRV record, but you do not want to have a discoverable federation.</span></span> <span data-ttu-id="eebd4-116">In einem solchen Fall haben Sie die Mobilität für Ihre Benutzer bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="eebd4-116">One such instance is where you have deployed mobility for your users.</span></span> <span data-ttu-id="eebd4-117">Das Mobility Push Notification Clearing House (PNCH) ist ein spezieller Föderations, der für Microsoft lync Mobile-Clients auf Apple iPhone oder iPad mit dem lync 2010-Mobilclient oder Windows Phone mit den mobilen lync 2010 Mobile-oder lync 2013-Clients verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="eebd4-117">The mobility push notification clearinghouse (PNCH) is a special type of federation that is used for Microsoft Lync Mobile clients on Apple iPhone or iPad using the Lync 2010 Mobile client or Windows Phone using the Lync 2010 Mobile or Lync 2013 Mobile clients.</span></span> <span data-ttu-id="eebd4-118">Die _sipfederationtls. _tcp.</span><span class="sxs-lookup"><span data-stu-id="eebd4-118">The _sipfederationtls._tcp.</span></span> <span data-ttu-id="eebd4-119"><EM> &lt; SIP-Domänen &gt; Namen</EM> -SRV-Eintrag wird im Fall von Mobilität und Push-Benachrichtigung verwendet.</span><span class="sxs-lookup"><span data-stu-id="eebd4-119"><EM>&lt;SIP domain name&gt;</EM> SRV record is used in the case of mobility and push notification.</span></span> <span data-ttu-id="eebd4-120">Um dieses Problem zu vermeiden und ihre Auffindbarkeit zu kontrollieren, deaktivieren Sie die Einstellung <STRONG>enable Partner Domain Discovery</STRONG> , um Discovery zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="eebd4-120">To mitigate this issue and control your discoverability, clear the setting <STRONG>Enable partner domain discovery</STRONG> to turn off discovery.</span></span>



</div>

<span data-ttu-id="eebd4-121">Zum Konfigurieren von xmpp (Extensible Messaging and Presence Protocol) für Ihre Bereitstellung erstellen Sie zwei DNS-Einträge (Domain Name System) auf einem externen DNS-Server, die die Datensätze in den Access-Edgedienst Ihres Edge-Servers oder Edge-Pools auflösen.</span><span class="sxs-lookup"><span data-stu-id="eebd4-121">To configure extensible messaging and presence protocol (XMPP) for your deployment, you create two domain name system (DNS) records in an external DNS server that will resolve the records to the Access Edge service of your Edge Server or Edge pool.</span></span>

<span data-ttu-id="eebd4-122">Wenn Sie DNS (Domain Name System) für die öffentliche Instant Messaging-Konnektivität konfigurieren, werden Sie feststellen, dass die Konfiguration, die externe Benutzer unterstützt, öffentliche Chat Verbindungen unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eebd4-122">When you configure domain name system (DNS) for public instant messaging connectivity, you will find that the configuration that supports external users will support public IM connectivity.</span></span> <span data-ttu-id="eebd4-123">Wenn Sie Ihren Edge-Server oder Edge-Pool bereits konfiguriert haben, sollten Sie über die DNS-Einträge verfügen, die für die Unterstützung öffentlicher Chat Verbindungen erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="eebd4-123">If you have already configured your Edge Server or Edge pool, you should have the DNS records necessary to support public IM connectivity.</span></span>

<div>

## <a name="dns-summary---sip-federation-including-public-instant-messaging-connectivity"></a><span data-ttu-id="eebd4-124">DNS-Zusammenfassung – SIP-Föderation einschließlich öffentlicher Instant Messaging-Konnektivität</span><span class="sxs-lookup"><span data-stu-id="eebd4-124">DNS Summary - SIP Federation including Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eebd4-125">Ort/Typ/Port</span><span class="sxs-lookup"><span data-stu-id="eebd4-125">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="eebd4-126">FQDN</span><span class="sxs-lookup"><span data-stu-id="eebd4-126">FQDN</span></span></th>
<th><span data-ttu-id="eebd4-127">IP-Adresse/FQDN-Hosteintrag</span><span class="sxs-lookup"><span data-stu-id="eebd4-127">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="eebd4-128">Karten/Kommentare</span><span class="sxs-lookup"><span data-stu-id="eebd4-128">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eebd4-129">Externer DNS/SRV/5061</span><span class="sxs-lookup"><span data-stu-id="eebd4-129">External DNS/SRV/5061</span></span></p></td>
<td><p><span data-ttu-id="eebd4-130">_sipfederationtls._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eebd4-130">_sipfederationtls._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eebd4-131">sip.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eebd4-131">sip.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eebd4-132">Die externe Schnittstelle für den Zugriff auf den Edgedienst ist für die automatische DNS-Erkennung Ihres Verbandes zu anderen potenziellen Verbundpartnern erforderlich und wird als "zugelassene SIP-Domänen" bezeichnet (genannt Enhanced Federation in früheren Versionen). Wiederholen Sie diese Schritte für alle SIP-Domänen mit lync-aktivierten Benutzern.</span><span class="sxs-lookup"><span data-stu-id="eebd4-132">Access Edge service external interface Required for automatic DNS discovery of your federation to other potential federation partners, and is known as “Allowed SIP Domains” (called enhanced federation in previous releases).Repeat as necessary for all SIP domains with Lync enabled users</span></span></p>



> [!IMPORTANT]
> <span data-ttu-id="eebd4-133">Dieser SRV-Eintrag ist für Mobilität und das Clearing House für die Push-Benachrichtigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="eebd4-133">This SRV record is required for mobility and the push notification clearing house.</span></span> <span data-ttu-id="eebd4-134">In Fällen, in denen mehrere SIP-Domänen vorhanden sind, erstellen und veröffentlichen Sie einen SRV-Eintrag für jede Domäne, die lync Mobile-Clients enthält.</span><span class="sxs-lookup"><span data-stu-id="eebd4-134">In cases where there is more than one SIP domain, create and publish an SRV record for each domain that will have Lync Mobile clients.</span></span> <span data-ttu-id="eebd4-135">Der Push-Benachrichtigungsdienst und der Apple Push-Benachrichtigungsdienst funktionieren möglicherweise nicht wie erwartet, wenn kein expliziter SRV-Eintrag für die einzelnen SIP-Domänen vorhanden ist, die die Bereitstellung unterstützt.</span><span class="sxs-lookup"><span data-stu-id="eebd4-135">The Push Notification Service and Apple Push Notification service may not operate as expected if there is not an explicit SRV record for each SIP domain that the deployment supports.</span></span>

</td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="dns-summary---extensible-messaging-and-presence-protocol-xmpp"></a><span data-ttu-id="eebd4-136">DNS Summary – Extensible Messaging and Presence Protocol (XMPP)</span><span class="sxs-lookup"><span data-stu-id="eebd4-136">DNS Summary - Extensible Messaging and Presence Protocol (XMPP)</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="eebd4-137">Ort/Typ/Port</span><span class="sxs-lookup"><span data-stu-id="eebd4-137">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="eebd4-138">FQDN</span><span class="sxs-lookup"><span data-stu-id="eebd4-138">FQDN</span></span></th>
<th><span data-ttu-id="eebd4-139">IP-Adresse/FQDN-Hosteintrag</span><span class="sxs-lookup"><span data-stu-id="eebd4-139">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="eebd4-140">Karten/Kommentare</span><span class="sxs-lookup"><span data-stu-id="eebd4-140">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="eebd4-141">Externer DNS/SRV/5269</span><span class="sxs-lookup"><span data-stu-id="eebd4-141">External DNS/SRV/5269</span></span></p></td>
<td><p><span data-ttu-id="eebd4-142">_xmpp-server._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eebd4-142">_xmpp-server._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eebd4-143">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="eebd4-143">xmpp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="eebd4-144">XMPP-Proxy-externe Schnittstelle im Access Edge-Dienst oder Edge-Pool. Wiederholen Sie diese Schritte für alle internen SIP-Domänen mit lync-aktivierten Benutzern, bei denen der Kontakt mit XMPP-Kontakten über die Konfiguration der Richtlinie für den externen Zugriff über eine globale Richtlinie, eine Website Richtlinie, in der sich der Benutzer befindet, oder die Benutzerrichtlinie, die auf den lync-aktivierten Benutzer angewendet wurde, zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="eebd4-144">XMPP proxy external interface on the Access Edge service or Edge pool.Repeat as necessary for all internal SIP domains with Lync enabled users where contact with XMPP contacts is allowed through the configuration of the External Access Policy through a global policy, site policy where the user is located, or user policy applied to the Lync-enabled user.</span></span> <span data-ttu-id="eebd4-145">Eine zulässige XMPP-Domäne muss auch in der XMPP-Föderationspartner-Richtlinie konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="eebd4-145">An allowed XMPP domain must also be configured in the XMPP Federated Partners policy.</span></span> <span data-ttu-id="eebd4-146">Weitere Informationen finden Sie in den Themen unter <strong>Siehe auch</strong> .</span><span class="sxs-lookup"><span data-stu-id="eebd4-146">See topics in <strong>See Also</strong> for additional details</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="eebd4-147">Externer DNS/A</span><span class="sxs-lookup"><span data-stu-id="eebd4-147">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="eebd4-148">xmpp.contoso.com (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="eebd4-148">xmpp.contoso.com (for example)</span></span></p></td>
<td><p><span data-ttu-id="eebd4-149">IP-Adresse des Zugriffs-Edgedienst auf dem Edgeserver oder Edge-Pool, der XMPP-Proxy hostet</span><span class="sxs-lookup"><span data-stu-id="eebd4-149">IP address of Access Edge service on your Edge Server or Edge pool hosting XMPP proxy</span></span></p></td>
<td><p><span data-ttu-id="eebd4-150">Verweist auf den Access Edge-Dienst oder den Edge-Pool, der den XMPP-Proxydienst hostet.</span><span class="sxs-lookup"><span data-stu-id="eebd4-150">Points to the Access Edge service or Edge pool that hosts the XMPP proxy service.</span></span> <span data-ttu-id="eebd4-151">In der Regel verweist der von Ihnen erstellte SRV-Eintrag auf diesen Host-Eintrag (a oder AAAA).</span><span class="sxs-lookup"><span data-stu-id="eebd4-151">Typically, the SRV record that you create will point to this host (A or AAAA) record</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="eebd4-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eebd4-152">See Also</span></span>


[<span data-ttu-id="eebd4-153">Einrichten eines XMPP-Partnerverbunds in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eebd4-153">Setting up XMPP federation in Lync Server 2013</span></span>](lync-server-2013-setting-up-xmpp-federation.md)  
[<span data-ttu-id="eebd4-154">Konfigurieren von Pushbenachrichtigungen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eebd4-154">Configuring for push notifications in Lync Server 2013</span></span>](lync-server-2013-configuring-for-push-notifications.md)  
[<span data-ttu-id="eebd4-155">Aktivieren oder Deaktivieren der Suche von Verbundpartnern in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eebd4-155">Enable or disable discovery of federation partners in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-discovery-of-federation-partners.md)  


[<span data-ttu-id="eebd4-156">Szenarien für den Zugriff durch externe Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eebd4-156">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="eebd4-157">Ermitteln von DNS-Anforderungen für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eebd4-157">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)  


[<span data-ttu-id="eebd4-158">Verwalten von SIP-Partnerdomänen für eine Organisation in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eebd4-158">Manage SIP federated domains for your organization in Lync Server 2013</span></span>](lync-server-2013-manage-sip-federated-domains-for-your-organization.md)  
  

<span data-ttu-id="eebd4-159"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eebd4-159"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

