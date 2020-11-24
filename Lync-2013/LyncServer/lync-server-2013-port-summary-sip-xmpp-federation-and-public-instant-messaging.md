---
title: Port Zusammenfassung – SIP, XMPP Federation und Public Instant Messaging
description: Port Zusammenfassung – SIP, XMPP Federation und Public Instant Messaging.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - SIP, XMPP federation, and public instant messaging
ms:assetid: ab05bdd6-e9b0-4b1b-9dd9-29ab88e8befe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618373(v=OCS.15)
ms:contentKeyID: 49105660
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7c58dbf7bdd56b4678d56f96a11332219bb40c17
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393975"
---
# <a name="port-summary---sip-xmpp-federation-and-public-instant-messaging-in-lync-server-2013"></a><span data-ttu-id="b8029-103">Port Zusammenfassung – SIP, XMPP Federation und Public Instant Messaging in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8029-103">Port summary - SIP, XMPP federation, and public instant messaging in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b8029-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b8029-104">

<span> </span></span></span>

<span data-ttu-id="b8029-105">_**Letztes Änderungsdatum des Themas:** 2013-03-15_</span><span class="sxs-lookup"><span data-stu-id="b8029-105">_**Topic Last Modified:** 2013-03-15_</span></span>

<span data-ttu-id="b8029-106">Port-, Protokoll-und Firewall-Anforderungen für den Verbund mit Microsoft lync Server 2013, lync Server 2010 und Office Communications Server ähneln denen für den bereitgestellten Edgeserver.</span><span class="sxs-lookup"><span data-stu-id="b8029-106">Port, protocol and firewall requirements for federation with Microsoft Lync Server 2013, Lync Server 2010 and Office Communications Server are similar to those for the deployed Edge Server.</span></span> <span data-ttu-id="b8029-107">Clients initiieren die Kommunikation mit dem Access Edge Service über TLS/SIP/TCP 443.</span><span class="sxs-lookup"><span data-stu-id="b8029-107">Clients initiate communication with the Access Edge service over TLS/SIP/TCP 443.</span></span> <span data-ttu-id="b8029-108">Föderationspartner initiieren jedoch die Kommunikation mit dem Access Edge-Dienst über MTLS/SIP/TCP 5061.</span><span class="sxs-lookup"><span data-stu-id="b8029-108">Federated partners however, will initiate communications to the Access Edge service over MTLS/SIP/TCP 5061.</span></span>

<span data-ttu-id="b8029-109">Wenn Sie Ihre Firewall für Ports und Protokolle konfigurieren möchten, die für die Unterstützung öffentlicher Instant Messaging-Konnektivität erforderlich sind, beachten Sie zunächst, dass SIP/MTLS/TCP 5061 bidirektional ist, um die Möglichkeit von Kontakten im öffentlichen Chat-Anbieter zu berücksichtigen, lync-Clients zu kontaktieren, oder dass lync Kontakte mit öffentlichen Chat Kontakten aufnehmen soll.</span><span class="sxs-lookup"><span data-stu-id="b8029-109">To configure your firewall for ports and protocols necessary to support public instant messaging connectivity, first note that SIP/MTLS/TCP 5061 is bidirectional to account for the ability of contacts in the public IM provider to contact Lync clients, or for Lync to contact public IM contacts.</span></span>

<span data-ttu-id="b8029-110">Windows Live Messenger kann an der Audio-und Videokommunikation mit lync-Clients teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="b8029-110">Windows Live Messenger can participate in audio/video communications with Lync clients.</span></span> <span data-ttu-id="b8029-111">Damit wird die sehr ähnliche Firewall-Port-und-Protokollkonfiguration berücksichtigt, die Sie normalerweise auf der Firewall haben, um lync-Clients als externe Benutzer zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b8029-111">This accounts for the very similar firewall port and protocol configuration that you would typically have on the firewall to support Lync clients as external users.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="b8029-112">Lync ist mehr denn je ein leistungsfähiges Tool für die Verbindung zwischen Organisationen und Personen in der ganzen Welt.</span><span class="sxs-lookup"><span data-stu-id="b8029-112">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="b8029-113">Für den Verbund mit Windows Live Messenger sind keine weiteren Benutzer-und Gerätelizenzen außerhalb der lync-Standard Client Zugriffslizenz (CAL) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b8029-113">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard Client Access License (CAL).</span></span> <span data-ttu-id="b8029-114">Skype Federation wird dieser Liste hinzugefügt und ermöglicht es lync-Benutzern, Hunderte von Millionen von Personen mit Chat und Sprache zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="b8029-114">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span><BR><span data-ttu-id="b8029-115">Die Föderation mit Messenger-Client Kontakten endet am 15. März 2013, mit Ausnahme des chinesischen Festlandes.</span><span class="sxs-lookup"><span data-stu-id="b8029-115">Federation with Messenger client contacts will officially end on March 15, 2013, except for mainland China.</span></span> <span data-ttu-id="b8029-116">Skype wird zum Verbund Client für Föderationsbenutzer, die Messenger zuvor verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="b8029-116">Skype will become the federation client for federated users who previously used Messenger.</span></span>



</div>

<span data-ttu-id="b8029-117">Die Ports und Protokolle, die für den auf dem Edgeserver bereitgestellten XMPP-Proxy (Extensible Messaging and Presence Protocol) definiert sind, ermöglichen die Kommunikation zwischen dem XMPP-Partner und dem Edgeserver sowie die Kommunikation zwischen dem Edgeserver und dem XMPP-Partner.</span><span class="sxs-lookup"><span data-stu-id="b8029-117">The ports and protocols defined for the extensible messaging and presence protocol (XMPP) proxy deployed on the Edge Server allow communications from the XMPP federated partner to the Edge Server, and also allows communication from your Edge Server to the XMPP federated partner.</span></span> <span data-ttu-id="b8029-118">Eine Regel wird auch für die interne Firewall vom Front-End-Server oder Front-End-Pool für den Edge-Server oder den Edge-Pool definiert.</span><span class="sxs-lookup"><span data-stu-id="b8029-118">A rule is also defined on the internal-facing firewall from the Front End Server or Front End pool to the Edge Server or Edge pool.</span></span>

<div>

## <a name="firewall-summary---sip-federation"></a><span data-ttu-id="b8029-119">Zusammenfassung der Firewall – SIP-Föderation</span><span class="sxs-lookup"><span data-stu-id="b8029-119">Firewall Summary - SIP Federation</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8029-120">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="b8029-120">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="b8029-121">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="b8029-121">Source IP address</span></span></th>
<th><span data-ttu-id="b8029-122">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="b8029-122">Destination IP address</span></span></th>
<th><span data-ttu-id="b8029-123">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b8029-123">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8029-124">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="b8029-124">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="b8029-125">Access Edge Service (öffentliche IP-Adresse)</span><span class="sxs-lookup"><span data-stu-id="b8029-125">Access Edge service public IP address</span></span></p></td>
<td><p><span data-ttu-id="b8029-126">Beliebig</span><span class="sxs-lookup"><span data-stu-id="b8029-126">Any</span></span></p></td>
<td><p><span data-ttu-id="b8029-127">Für Verbund-und öffentliche Chat Verbindungen mit SIP</span><span class="sxs-lookup"><span data-stu-id="b8029-127">For federated and public IM connectivity using SIP</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="b8029-128">Zusammenfassung der Firewall – öffentliche Instant Messaging-Konnektivität</span><span class="sxs-lookup"><span data-stu-id="b8029-128">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8029-129">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="b8029-129">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="b8029-130">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="b8029-130">Source IP address</span></span></th>
<th><span data-ttu-id="b8029-131">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="b8029-131">Destination IP address</span></span></th>
<th><span data-ttu-id="b8029-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b8029-132">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8029-133">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="b8029-133">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="b8029-134">Verbindungspartner für öffentliche Chats</span><span class="sxs-lookup"><span data-stu-id="b8029-134">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="b8029-135">Edge-Server-Zugriffs Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b8029-135">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="b8029-136">Für Verbund-und öffentliche Chat Verbindungen, die SIP verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8029-136">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8029-137">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="b8029-137">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="b8029-138">Edge-Server-Zugriffs Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b8029-138">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="b8029-139">Verbindungspartner für öffentliche Chats</span><span class="sxs-lookup"><span data-stu-id="b8029-139">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="b8029-140">Für Verbund-und öffentliche Chat Verbindungen, die SIP verwenden.</span><span class="sxs-lookup"><span data-stu-id="b8029-140">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8029-141">Access/SIP (TLS)-/TCP/443</span><span class="sxs-lookup"><span data-stu-id="b8029-141">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="b8029-142">Clients</span><span class="sxs-lookup"><span data-stu-id="b8029-142">Clients</span></span></p></td>
<td><p><span data-ttu-id="b8029-143">Edge-Server-Zugriffs Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b8029-143">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="b8029-144">Client-zu-Server-SIP-Datenverkehr für den externen Benutzerzugriff</span><span class="sxs-lookup"><span data-stu-id="b8029-144">Client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8029-145">A/V/RTP/TCP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="b8029-145">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="b8029-146">Edge-Server-Zugriffs Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b8029-146">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="b8029-147">Live Messenger-Clients</span><span class="sxs-lookup"><span data-stu-id="b8029-147">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="b8029-148">Wird für A/V-Sitzungen mit Windows Live Messenger verwendet, wenn die Konnektivität für öffentliche Chats konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="b8029-148">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8029-149">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="b8029-149">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="b8029-150">Edge-Server-Zugriffs Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b8029-150">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="b8029-151">Live Messenger-Clients</span><span class="sxs-lookup"><span data-stu-id="b8029-151">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="b8029-152">Erforderlich für öffentliche Chat Verbindungen mit Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="b8029-152">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8029-153">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="b8029-153">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="b8029-154">Live Messenger-Clients</span><span class="sxs-lookup"><span data-stu-id="b8029-154">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="b8029-155">Edge-Server-Zugriffs Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b8029-155">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="b8029-156">Erforderlich für öffentliche Chat Verbindungen mit Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="b8029-156">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="firewall-summary---extensible-messaging-and-presence-protocol-xmpp"></a><span data-ttu-id="b8029-157">Zusammenfassung der Firewall – erweiterbares Messaging und Anwesenheits Protokoll (XMPP)</span><span class="sxs-lookup"><span data-stu-id="b8029-157">Firewall Summary - Extensible Messaging and Presence Protocol (XMPP)</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b8029-158">Protokoll/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="b8029-158">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="b8029-159">Quelle (IP-Adresse)</span><span class="sxs-lookup"><span data-stu-id="b8029-159">Source (IP address)</span></span></th>
<th><span data-ttu-id="b8029-160">Ziel (IP-Adresse)</span><span class="sxs-lookup"><span data-stu-id="b8029-160">Destination (IP address)</span></span></th>
<th><span data-ttu-id="b8029-161">Kommentare</span><span class="sxs-lookup"><span data-stu-id="b8029-161">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b8029-162">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="b8029-162">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="b8029-163">Beliebig</span><span class="sxs-lookup"><span data-stu-id="b8029-163">Any</span></span></p></td>
<td><p><span data-ttu-id="b8029-164">Access Edge Service Interface-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="b8029-164">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="b8029-165">Standard mäßiger Server-zu-Server-Kommunikationsanschluss für XMPP.</span><span class="sxs-lookup"><span data-stu-id="b8029-165">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="b8029-166">Ermöglicht die Kommunikation mit dem Edge-Server-XMPP-Proxy von Federated XMPP-Partnern</span><span class="sxs-lookup"><span data-stu-id="b8029-166">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b8029-167">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="b8029-167">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="b8029-168">Access Edge Service Interface-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="b8029-168">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="b8029-169">Beliebig</span><span class="sxs-lookup"><span data-stu-id="b8029-169">Any</span></span></p></td>
<td><p><span data-ttu-id="b8029-170">Standard mäßiger Server-zu-Server-Kommunikationsanschluss für XMPP.</span><span class="sxs-lookup"><span data-stu-id="b8029-170">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="b8029-171">Ermöglicht die Kommunikation vom Edge Server XMPP-Proxy an Federated XMPP-Partner</span><span class="sxs-lookup"><span data-stu-id="b8029-171">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b8029-172">XMPP/MTLS/23456</span><span class="sxs-lookup"><span data-stu-id="b8029-172">XMPP/MTLS/23456</span></span></p></td>
<td><p><span data-ttu-id="b8029-173">Beliebig</span><span class="sxs-lookup"><span data-stu-id="b8029-173">Any</span></span></p></td>
<td><p><span data-ttu-id="b8029-174">Interne Edge-Server-Schnittstellen-IP</span><span class="sxs-lookup"><span data-stu-id="b8029-174">Internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="b8029-175">Interner XMPP-Datenverkehr vom XMPP-Gateway auf dem Front-End-Server oder Front-End-Pool zum Edgeserver</span><span class="sxs-lookup"><span data-stu-id="b8029-175">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b8029-176">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b8029-176">See Also</span></span>


[<span data-ttu-id="b8029-177">Szenarien für den Zugriff durch externe Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8029-177">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="b8029-178">Ermitteln der Anforderungen für externe A/V-Firewalls und Ports für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8029-178">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  


[<span data-ttu-id="b8029-179">Verwalten von XMPP-Verbundpartnern für Ihre Organisation in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b8029-179">Manage XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md)  
  

<span data-ttu-id="b8029-180"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b8029-180"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

