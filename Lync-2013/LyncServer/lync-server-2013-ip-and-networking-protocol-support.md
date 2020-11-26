---
title: 'Lync Server 2013: IP- und Netzwerkprotokollunterstützung'
description: 'Lync Server 2013: Unterstützung für IP-und Netzwerkprotokoll.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IP and networking protocol support
ms:assetid: b0cffb10-3478-445c-89c7-8cb8b5027424
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412848(v=OCS.15)
ms:contentKeyID: 48185128
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dbd8022dd7197524334e0c70ea0ad875a30446de
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426746"
---
# <a name="ip-and-networking-protocol-support-in-lync-server-2013"></a><span data-ttu-id="81ad3-103">IP- und Netzwerkprotokollunterstützung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="81ad3-103">IP and networking protocol support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="81ad3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="81ad3-104">

<span> </span></span></span>

<span data-ttu-id="81ad3-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="81ad3-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="81ad3-106">Lync Server 2013 unterstützt die folgenden IP-und Netzwerkprotokolle:</span><span class="sxs-lookup"><span data-stu-id="81ad3-106">Lync Server 2013 supports the following IP and networking protocols:</span></span>

  - <span data-ttu-id="81ad3-107">**IP-Protokolle.**</span><span class="sxs-lookup"><span data-stu-id="81ad3-107">**IP Protocols.**</span></span>   <span data-ttu-id="81ad3-108">Lync Server 2013 unterstützt entweder IP Version 4 (IPv4) oder IP Version 6 (IPv6) für das Server Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="81ad3-108">Lync Server 2013 supports either IP version 4 (IPv4) or IP version 6 (IPv6) for the server network.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="81ad3-109">Lync Server 2013 kann in einem Netzwerk mit aktiviertem Dual IP Stack funktionieren.</span><span class="sxs-lookup"><span data-stu-id="81ad3-109">Lync Server 2013 can function in a network with dual IP stack enabled.</span></span>

    
    </div>

  - <span data-ttu-id="81ad3-110">**SIP-Transport Protokolle.**</span><span class="sxs-lookup"><span data-stu-id="81ad3-110">**SIP Transport Protocols.**</span></span>   <span data-ttu-id="81ad3-111">Im Allgemeinen kann SIP mindestens drei Transporttypen verwenden: User Datagram Protocol (UDP), Transmission Control Protocol (TCP) und Transport Layer Security (TLS).</span><span class="sxs-lookup"><span data-stu-id="81ad3-111">Generically, SIP can use at least three transport types: User Datagram Protocol (UDP), Transmission Control Protocol (TCP), and Transport Layer Security (TLS).</span></span> <span data-ttu-id="81ad3-112">In der standardmäßigen SIP-Transportkonfiguration wird TLS über TCP ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="81ad3-112">In the default SIP transport configuration, TLS runs over TCP.</span></span> <span data-ttu-id="81ad3-113">TLS wird im lync Server 2013-Netzwerk verwendet.</span><span class="sxs-lookup"><span data-stu-id="81ad3-113">TLS is used within the Lync Server 2013 network.</span></span> <span data-ttu-id="81ad3-114">Am Rand des Netzwerks kann lync Server 2013 über TCP interagieren.</span><span class="sxs-lookup"><span data-stu-id="81ad3-114">At the edge of the network, Lync Server 2013 can interoperate over TCP.</span></span> <span data-ttu-id="81ad3-115">Lync Server 2013 unterstützt UDP für den SIP-Transport nicht, da es die Mindestanforderungen für die Sicherheit, Zuverlässigkeit und Skalierbarkeit von Unternehmenskommunikation nicht erfüllt.</span><span class="sxs-lookup"><span data-stu-id="81ad3-115">Lync Server 2013 does not support UDP for SIP transport because it doesn’t meet the minimum standards for enterprise communications security, reliability, and scalability.</span></span> <span data-ttu-id="81ad3-116">Ausführliche Informationen finden Sie im NextHop-Blog Artikel "zu UDP oder nicht zu UDP, das ist die Frage" [https://go.microsoft.com/fwlink/p/?linkId=185369](https://go.microsoft.com/fwlink/p/?linkid=185369) .</span><span class="sxs-lookup"><span data-stu-id="81ad3-116">For details, see the NextHop blog article, "To UDP, or not to UDP, that is the question," at [https://go.microsoft.com/fwlink/p/?linkId=185369](https://go.microsoft.com/fwlink/p/?linkid=185369).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="81ad3-117">Die Inhalte der Blogs und die zugehörige URL können ohne vorherige Ankündigung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="81ad3-117">The content of each blog and its URL are subject to change without notice.</span></span>

    
    <span data-ttu-id="81ad3-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="81ad3-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

