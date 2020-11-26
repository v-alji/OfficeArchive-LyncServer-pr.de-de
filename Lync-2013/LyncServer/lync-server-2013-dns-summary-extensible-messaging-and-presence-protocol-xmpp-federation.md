---
title: DNS Summary – Extensible Messaging and Presence Protocol (XMPP) Federation
description: DNS Summary – Extensible Messaging and Presence Protocol (XMPP) Federation.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS summary - Extensible messaging and presence protocol (XMPP) federation
ms:assetid: 0f720a2a-8ab5-43cc-882a-ab595ed3cec7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618368(v=OCS.15)
ms:contentKeyID: 49105655
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b8088e30c93faa52c575fefa97e572ed20b6ad9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437735"
---
# <a name="dns-summary---extensible-messaging-and-presence-protocol-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="e9ad1-103">DNS Summary – Extensible Messaging and Presence Protocol (XMPP) Federation in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e9ad1-103">DNS summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e9ad1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e9ad1-104">

<span> </span></span></span>

<span data-ttu-id="e9ad1-105">_**Letztes Änderungsdatum des Themas:** 2014-04-08_</span><span class="sxs-lookup"><span data-stu-id="e9ad1-105">_**Topic Last Modified:** 2014-04-08_</span></span>

<span data-ttu-id="e9ad1-106">Zum Konfigurieren von xmpp (Extensible Messaging and Presence Protocol) für Ihre Bereitstellung erstellen Sie zwei DNS-Einträge (Domain Name System) auf einem externen DNS-Server, die die Datensätze in den Access-Edgedienst Ihres Edge-Servers oder Edge-Pools auflösen.</span><span class="sxs-lookup"><span data-stu-id="e9ad1-106">To configure extensible messaging and presence protocol (XMPP) for your deployment, you create two Domain Name System (DNS) records in an external DNS server that will resolve the records to the Access Edge service of your Edge Server or Edge pool.</span></span>

<div>

## <a name="dns-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="e9ad1-107">DNS-Zusammenfassung für erweiterbares Messaging und Anwesenheits Protokoll</span><span class="sxs-lookup"><span data-stu-id="e9ad1-107">DNS Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e9ad1-108">Ort/Typ/Port</span><span class="sxs-lookup"><span data-stu-id="e9ad1-108">Location/TYPE/Port</span></span></th>
<th><span data-ttu-id="e9ad1-109">FQDN</span><span class="sxs-lookup"><span data-stu-id="e9ad1-109">FQDN</span></span></th>
<th><span data-ttu-id="e9ad1-110">IP-Adresse/FQDN-Hosteintrag</span><span class="sxs-lookup"><span data-stu-id="e9ad1-110">IP address/FQDN host record</span></span></th>
<th><span data-ttu-id="e9ad1-111">Karten/Kommentare</span><span class="sxs-lookup"><span data-stu-id="e9ad1-111">Maps to/Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9ad1-112">Externer DNS/SRV/5269</span><span class="sxs-lookup"><span data-stu-id="e9ad1-112">External DNS/SRV/5269</span></span></p></td>
<td><p><span data-ttu-id="e9ad1-113">_xmpp-server._tcp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="e9ad1-113">_xmpp-server._tcp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="e9ad1-114">xmpp.contoso.com</span><span class="sxs-lookup"><span data-stu-id="e9ad1-114">xmpp.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="e9ad1-115">XMPP-Proxy-externe Schnittstelle im Access Edge-Dienst oder Edge-Pool. Wiederholen Sie diese Schritte für alle internen SIP-Domänen mit lync-aktivierten Benutzern, bei denen der Kontakt mit XMPP-Kontakten über die Konfiguration der Richtlinie für den externen Zugriff über eine globale Richtlinie, eine Website Richtlinie, in der sich der Benutzer befindet, oder die Benutzerrichtlinie, die auf den lync-aktivierten Benutzer angewendet wurde, zulässig ist.</span><span class="sxs-lookup"><span data-stu-id="e9ad1-115">XMPP proxy external interface on the Access Edge service or Edge pool.Repeat as necessary for all internal SIP domains with Lync enabled users where contact with XMPP contacts is allowed through the configuration of the External Access Policy through a global policy, site policy where the user is located, or user policy applied to the Lync-enabled user.</span></span> <span data-ttu-id="e9ad1-116">Eine zulässige XMPP-Domäne muss auch in der XMPP-Föderationspartner-Richtlinie konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="e9ad1-116">An allowed XMPP domain must also be configured in the XMPP Federated Partners policy.</span></span> <span data-ttu-id="e9ad1-117">Weitere Informationen finden Sie in den Themen unter <strong>Siehe auch</strong> .</span><span class="sxs-lookup"><span data-stu-id="e9ad1-117">See topics in <strong>See Also</strong> for additional details</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9ad1-118">Externer DNS/A</span><span class="sxs-lookup"><span data-stu-id="e9ad1-118">External DNS/A</span></span></p></td>
<td><p><span data-ttu-id="e9ad1-119">xmpp.contoso.com (Beispiel)</span><span class="sxs-lookup"><span data-stu-id="e9ad1-119">xmpp.contoso.com (for example)</span></span></p></td>
<td><p><span data-ttu-id="e9ad1-120">IP-Adresse des Zugriffs-Edgedienst auf dem Edgeserver oder Edge-Pool, der XMPP-Proxy hostet</span><span class="sxs-lookup"><span data-stu-id="e9ad1-120">IP address of Access Edge service on your Edge Server or Edge pool hosting XMPP proxy</span></span></p></td>
<td><p><span data-ttu-id="e9ad1-121">Verweist auf den Access Edge-Dienst oder den Edge-Pool, der den XMPP-Proxydienst hostet.</span><span class="sxs-lookup"><span data-stu-id="e9ad1-121">Points to the Access Edge service or Edge pool that hosts the XMPP proxy service.</span></span> <span data-ttu-id="e9ad1-122">In der Regel verweist der von Ihnen erstellte SRV-Eintrag auf diesen Host-Eintrag (a oder AAAA).</span><span class="sxs-lookup"><span data-stu-id="e9ad1-122">Typically, the SRV record that you create will point to this host (A or AAAA) record</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e9ad1-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9ad1-123">See Also</span></span>


[<span data-ttu-id="e9ad1-124">Einrichten eines XMPP-Partnerverbunds in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e9ad1-124">Setting up XMPP federation in Lync Server 2013</span></span>](lync-server-2013-setting-up-xmpp-federation.md)  


[<span data-ttu-id="e9ad1-125">Ermitteln von DNS-Anforderungen für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e9ad1-125">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)  
  

<span data-ttu-id="e9ad1-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e9ad1-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

