---
title: Port Zusammenfassung – Extensible Messaging and Presence Protocol (XMPP) Federation
description: Port Zusammenfassung – Extensible Messaging and Presence Protocol (XMPP) Federation.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Port summary -  Extensible messaging and presence protocol (XMPP) federation
ms:assetid: 62e98fab-7add-4983-a3fa-dbe74e1c3849
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ618371(v=OCS.15)
ms:contentKeyID: 49105658
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9508bc8b9fbcca6fb6a37478def258a9fa52c373
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442803"
---
# <a name="port-summary---extensible-messaging-and-presence-protocol-xmpp-federation-in-lync-server-2013"></a><span data-ttu-id="810e4-103">Port Zusammenfassung – Extensible Messaging and Presence Protocol (XMPP) Federation in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="810e4-103">Port summary - Extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="810e4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="810e4-104">

<span> </span></span></span>

<span data-ttu-id="810e4-105">_**Letztes Änderungsdatum des Themas:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="810e4-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="810e4-106">Die Ports und Protokolle, die für den auf dem Edgeserver bereitgestellten XMPP-Proxy (Extensible Messaging and Presence Protocol) definiert sind, ermöglichen die Kommunikation zwischen dem XMPP-Partner und dem Edgeserver sowie die Kommunikation zwischen dem Edgeserver und dem XMPP-Partner.</span><span class="sxs-lookup"><span data-stu-id="810e4-106">The ports and protocols defined for the extensible messaging and presence protocol (XMPP) proxy deployed on the Edge Server allow communications from the XMPP federated partner to the Edge Server, and also allows communication from your Edge Server to the XMPP federated partner.</span></span> <span data-ttu-id="810e4-107">Eine Regel wird auch für die interne Firewall vom Front-End-Server oder Front-End-Pool für den Edge-Server oder den Edge-Pool definiert.</span><span class="sxs-lookup"><span data-stu-id="810e4-107">A rule is also defined on the internal-facing firewall from the Front End Server or Front End pool to the Edge Server or Edge pool.</span></span>

<div>

## <a name="firewall-summary-for-extensible-messaging-and-presence-protocol"></a><span data-ttu-id="810e4-108">Zusammenfassung der Firewall für erweiterbares Messaging und Anwesenheits Protokoll</span><span class="sxs-lookup"><span data-stu-id="810e4-108">Firewall Summary for Extensible Messaging and Presence Protocol</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="810e4-109">Protokoll/TCP oder UDP/Port</span><span class="sxs-lookup"><span data-stu-id="810e4-109">Protocol/TCP or UDP/Port</span></span></th>
<th><span data-ttu-id="810e4-110">Quelle (IP-Adresse)</span><span class="sxs-lookup"><span data-stu-id="810e4-110">Source (IP address)</span></span></th>
<th><span data-ttu-id="810e4-111">Ziel (IP-Adresse)</span><span class="sxs-lookup"><span data-stu-id="810e4-111">Destination (IP address)</span></span></th>
<th><span data-ttu-id="810e4-112">Kommentare</span><span class="sxs-lookup"><span data-stu-id="810e4-112">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="810e4-113">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="810e4-113">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="810e4-114">Beliebig</span><span class="sxs-lookup"><span data-stu-id="810e4-114">Any</span></span></p></td>
<td><p><span data-ttu-id="810e4-115">Access Edge Service Interface-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="810e4-115">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="810e4-116">Standard mäßiger Server-zu-Server-Kommunikationsanschluss für XMPP.</span><span class="sxs-lookup"><span data-stu-id="810e4-116">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="810e4-117">Ermöglicht die Kommunikation mit dem Edge-Server-XMPP-Proxy von Federated XMPP-Partnern</span><span class="sxs-lookup"><span data-stu-id="810e4-117">Allows communication to the Edge Server XMPP proxy from federated XMPP partners</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="810e4-118">XMPP/TCP/5269</span><span class="sxs-lookup"><span data-stu-id="810e4-118">XMPP/TCP/5269</span></span></p></td>
<td><p><span data-ttu-id="810e4-119">Access Edge Service Interface-IP-Adresse</span><span class="sxs-lookup"><span data-stu-id="810e4-119">Access Edge service interface IP address</span></span></p></td>
<td><p><span data-ttu-id="810e4-120">Beliebig</span><span class="sxs-lookup"><span data-stu-id="810e4-120">Any</span></span></p></td>
<td><p><span data-ttu-id="810e4-121">Standard mäßiger Server-zu-Server-Kommunikationsanschluss für XMPP.</span><span class="sxs-lookup"><span data-stu-id="810e4-121">Standard server-to-server communication port for XMPP.</span></span> <span data-ttu-id="810e4-122">Ermöglicht die Kommunikation vom Edge Server XMPP-Proxy an Federated XMPP-Partner</span><span class="sxs-lookup"><span data-stu-id="810e4-122">Allows communication from the Edge Server XMPP proxy to federated XMPP partners</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="810e4-123">XMPP/MTLS/23456</span><span class="sxs-lookup"><span data-stu-id="810e4-123">XMPP/MTLS/23456</span></span></p></td>
<td><p><span data-ttu-id="810e4-124">Beliebig</span><span class="sxs-lookup"><span data-stu-id="810e4-124">Any</span></span></p></td>
<td><p><span data-ttu-id="810e4-125">Interne Edge-Server-Schnittstellen-IP</span><span class="sxs-lookup"><span data-stu-id="810e4-125">Internal Edge Server Interface IP</span></span></p></td>
<td><p><span data-ttu-id="810e4-126">Interner XMPP-Datenverkehr vom XMPP-Gateway auf dem Front-End-Server oder Front-End-Pool zum Edgeserver</span><span class="sxs-lookup"><span data-stu-id="810e4-126">Internal XMPP traffic from the XMPP Gateway on the Front End Server or Front End pool to the Edge Server</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="810e4-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="810e4-127">See Also</span></span>


[<span data-ttu-id="810e4-128">Beispiel für eine XMPP-Konfiguration in Lync Server 2013 – XMPP-Partnerverbund mit Google Talk</span><span class="sxs-lookup"><span data-stu-id="810e4-128">Example XMPP configuration in Lync Server 2013 – XMPP federation with Google Talk</span></span>](lync-server-2013-example-xmpp-configuration-–-xmpp-federation-with-google-talk.md)  


[<span data-ttu-id="810e4-129">Verwalten von XMPP-Verbundpartnern für Ihre Organisation in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="810e4-129">Manage XMPP federated partners in Lync Server 2013</span></span>](lync-server-2013-manage-xmpp-federated-partners-for-your-organization.md)  
  

<span data-ttu-id="810e4-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="810e4-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

