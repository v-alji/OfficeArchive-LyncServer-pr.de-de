---
title: 'Lync Server 2013: Port Zusammenfassung – öffentliche Instant Messaging-Konnektivität'
description: 'Lync Server 2013: Port Zusammenfassung – öffentliche Instant Messaging-Konnektivität.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary - Public instant messaging connectivity
ms:assetid: f46756ec-1401-4ca2-a4a4-5cd28bcfdc7f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618376(v=OCS.15)
ms:contentKeyID: 49105663
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4137b5f92e043dc15dc9aa1f0b9593b4d9f7c2ca
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424275"
---
# <a name="port-summary---public-instant-messaging-connectivity-in-lync-server-2013"></a><span data-ttu-id="b1bc8-103">Port Zusammenfassung – öffentliche Instant Messaging-Konnektivität in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1bc8-103">Port summary - Public instant messaging connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b1bc8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b1bc8-104">

<span> </span></span></span>

<span data-ttu-id="b1bc8-105">_**Letztes Änderungsdatum des Themas:** 2013-02-16_</span><span class="sxs-lookup"><span data-stu-id="b1bc8-105">_**Topic Last Modified:** 2013-02-16_</span></span>

<span data-ttu-id="b1bc8-106">Wenn Sie Ihre Firewall für Ports und Protokolle konfigurieren möchten, die für die Unterstützung öffentlicher Instant Messaging-Konnektivität erforderlich sind, beachten Sie zunächst, dass SIP/MTLS/TCP 5061 bidirektional ist, um die Möglichkeit von Kontakten im öffentlichen Chat-Anbieter zu berücksichtigen, lync-Clients zu kontaktieren, oder dass lync Kontakte mit öffentlichen Chat Kontakten aufnehmen soll.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-106">To configure your firewall for ports and protocols necessary to support public instant messaging connectivity, first note that SIP/MTLS/TCP 5061 is bidirectional to account for the ability of contacts in the public IM provider to contact Lync clients, or for Lync to contact public IM contacts.</span></span>

<span data-ttu-id="b1bc8-107">Windows Live Messenger kann an der Audio-und Videokommunikation mit lync-Clients teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-107">Windows Live Messenger can participate in audio/video communications with Lync clients.</span></span> <span data-ttu-id="b1bc8-108">Damit wird die sehr ähnliche Firewall-Port-und-Protokollkonfiguration berücksichtigt, die Sie normalerweise auf der Firewall haben, um lync-Clients als externe Benutzer zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-108">This accounts for the very similar firewall port and protocol configuration that you would typically have on the firewall to support Lync clients as external users.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="b1bc8-109">Lync ist mehr denn je ein leistungsfähiges Tool für die Verbindung zwischen Organisationen und Personen in der ganzen Welt.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-109">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="b1bc8-110">Für den Verbund mit Windows Live Messenger sind keine weiteren Benutzer-und Gerätelizenzen außerhalb der lync-Standard Client Zugriffslizenz (CAL) erforderlich.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-110">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard Client Access License (CAL).</span></span> <span data-ttu-id="b1bc8-111">Skype Federation wird dieser Liste hinzugefügt und ermöglicht es lync-Benutzern, Hunderte von Millionen von Personen mit Chat und Sprache zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-111">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span><BR><span data-ttu-id="b1bc8-112">Die Föderation mit Messenger-Client Kontakten endet am 15. März 2013, mit Ausnahme des chinesischen Festlandes.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-112">Federation with Messenger client contacts will officially end on March 15, 2013, except for mainland China.</span></span> <span data-ttu-id="b1bc8-113">Skype wird zum Verbund Client für Föderationsbenutzer, die Messenger zuvor verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-113">Skype will become the federation client for federated users who previously used Messenger.</span></span>



</div>

<div>

## <a name="firewall-summary--public-instant-messaging-connectivity"></a><span data-ttu-id="b1bc8-114">Zusammenfassung der Firewall – öffentliche Instant Messaging-Konnektivität</span><span class="sxs-lookup"><span data-stu-id="b1bc8-114">Firewall Summary – Public Instant Messaging Connectivity</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b1bc8-115">Role/Protocol/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="b1bc8-115">Role/Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="b1bc8-116">Quell-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="b1bc8-116">Source IP address</span></span></th>
<th><span data-ttu-id="b1bc8-117">Ziel-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="b1bc8-117">Destination IP address</span></span></th>
<th><span data-ttu-id="b1bc8-118">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b1bc8-118">Notes</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1bc8-119">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="b1bc8-119">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="b1bc8-120">Verbindungspartner für öffentliche Chats</span><span class="sxs-lookup"><span data-stu-id="b1bc8-120">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="b1bc8-121">Edge-Server-Zugriffs Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b1bc8-121">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="b1bc8-122">Für Verbund-und öffentliche Chat Verbindungen, die SIP verwenden.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-122">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1bc8-123">Access/SIP (MTLS)-/TCP/5061</span><span class="sxs-lookup"><span data-stu-id="b1bc8-123">Access/SIP(MTLS)/TCP/5061</span></span></p></td>
<td><p><span data-ttu-id="b1bc8-124">Edge-Server-Zugriffs Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b1bc8-124">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="b1bc8-125">Verbindungspartner für öffentliche Chats</span><span class="sxs-lookup"><span data-stu-id="b1bc8-125">Public IM connectivity partners</span></span></p></td>
<td><p><span data-ttu-id="b1bc8-126">Für Verbund-und öffentliche Chat Verbindungen, die SIP verwenden.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-126">For federated and public IM connectivity that use SIP.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1bc8-127">Access/SIP (TLS)-/TCP/443</span><span class="sxs-lookup"><span data-stu-id="b1bc8-127">Access/SIP(TLS)/TCP/443</span></span></p></td>
<td><p><span data-ttu-id="b1bc8-128">Clients</span><span class="sxs-lookup"><span data-stu-id="b1bc8-128">Clients</span></span></p></td>
<td><p><span data-ttu-id="b1bc8-129">Edge-Server-Zugriffs Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b1bc8-129">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="b1bc8-130">Client-zu-Server-SIP-Datenverkehr für den externen Benutzerzugriff</span><span class="sxs-lookup"><span data-stu-id="b1bc8-130">Client-to-server SIP traffic for external user access.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1bc8-131">A/V/RTP/TCP/50000-59.999</span><span class="sxs-lookup"><span data-stu-id="b1bc8-131">A/V/RTP/TCP/50,000-59,999</span></span></p></td>
<td><p><span data-ttu-id="b1bc8-132">Edge-Server-Zugriffs Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b1bc8-132">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="b1bc8-133">Live Messenger-Clients</span><span class="sxs-lookup"><span data-stu-id="b1bc8-133">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="b1bc8-134">Wird für A/V-Sitzungen mit Windows Live Messenger verwendet, wenn die Konnektivität für öffentliche Chats konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-134">Used for A/V sessions with Windows Live Messenger if public IM connectivity is configured.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1bc8-135">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="b1bc8-135">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="b1bc8-136">Edge-Server-Zugriffs Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b1bc8-136">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="b1bc8-137">Live Messenger-Clients</span><span class="sxs-lookup"><span data-stu-id="b1bc8-137">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="b1bc8-138">Erforderlich für öffentliche Chat Verbindungen mit Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-138">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1bc8-139">A/V/Stun, MSTURN/UDP/3478</span><span class="sxs-lookup"><span data-stu-id="b1bc8-139">A/V/STUN,MSTURN/UDP/3478</span></span></p></td>
<td><p><span data-ttu-id="b1bc8-140">Live Messenger-Clients</span><span class="sxs-lookup"><span data-stu-id="b1bc8-140">Live Messenger clients</span></span></p></td>
<td><p><span data-ttu-id="b1bc8-141">Edge-Server-Zugriffs Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="b1bc8-141">Edge Server Access interface</span></span></p></td>
<td><p><span data-ttu-id="b1bc8-142">Erforderlich für öffentliche Chat Verbindungen mit Windows Live Messenger.</span><span class="sxs-lookup"><span data-stu-id="b1bc8-142">Required for public IM connectivity with Windows Live Messenger.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b1bc8-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b1bc8-143">See Also</span></span>


[<span data-ttu-id="b1bc8-144">Szenarien für den Zugriff durch externe Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1bc8-144">Scenarios for external user access in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-external-user-access.md)  
[<span data-ttu-id="b1bc8-145">Ermitteln der Anforderungen für externe A/V-Firewalls und Ports für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1bc8-145">Determine external A/V firewall and port requirements for Lync Server 2013</span></span>](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md)  
  

<span data-ttu-id="b1bc8-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b1bc8-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

