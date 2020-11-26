---
title: 'Lync Server 2013: Richtlinien für die Integration lokaler Unified Messaging-Dienste'
description: 'Lync Server 2013: Richtlinien für die Integration von lokalen Unified Messaging.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Guidelines for integrating on-premises Unified Messaging and Lync Server
ms:assetid: 829ac017-6907-40f9-be22-787a28eae0ac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398656(v=OCS.15)
ms:contentKeyID: 48184681
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 814c927aa36199737712328d3b92c64a8e967a55
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427799"
---
# <a name="guidelines-for-integrating-on-premises-unified-messaging-and-lync-server-2013"></a><span data-ttu-id="a2f27-103">Richtlinien für die Integration lokaler Unified Messaging-Dienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a2f27-103">Guidelines for integrating on-premises Unified Messaging and Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a2f27-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a2f27-104">

<span> </span></span></span>

<span data-ttu-id="a2f27-105">_**Letztes Änderungsdatum des Themas:** 2012-09-25_</span><span class="sxs-lookup"><span data-stu-id="a2f27-105">_**Topic Last Modified:** 2012-09-25_</span></span>

<span data-ttu-id="a2f27-106">Im Folgenden sind Richtlinien und bewährte Methoden aufgeführt, die Sie beim Bereitstellen von Enterprise-VoIP berücksichtigen sollten:</span><span class="sxs-lookup"><span data-stu-id="a2f27-106">The following are guidelines and best practices to consider when you deploy Enterprise Voice:</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a2f27-107">Exchange Unified Messaging (um) unterstützt IPv6 nur, wenn Sie auch UCMA 4 verwenden.</span><span class="sxs-lookup"><span data-stu-id="a2f27-107">Exchange Unified Messaging (UM) supports IPv6 only if you are also using UCMA 4.</span></span>



</div>

  - <span data-ttu-id="a2f27-108">Bereitstellen eines lync Server 2013 Standard Edition-Servers oder eines Front-End-Pools</span><span class="sxs-lookup"><span data-stu-id="a2f27-108">Deploy a Lync Server 2013 Standard Edition server or a Front End pool.</span></span> <span data-ttu-id="a2f27-109">Details zur Installation finden Sie unter [Bereitstellen von lync Server 2013](lync-server-2013-deploying-lync-server.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="a2f27-109">For details about installation, see [Deploying Lync Server 2013](lync-server-2013-deploying-lync-server.md) in the Deployment documentation.</span></span>

  - <span data-ttu-id="a2f27-110">Besprechen Sie mit den Exchange-Administratoren, wer welche Aufgaben ausführt, um eine reibungslose und erfolgreiche Integration sicherzustellen.</span><span class="sxs-lookup"><span data-stu-id="a2f27-110">Work with Exchange administrators to confirm which tasks each of you will perform to assure a smooth and successful integration.</span></span>

  - <span data-ttu-id="a2f27-111">Stellen Sie die Exchange-Postfachserverrollen in jeder Exchange Unified Messaging (um)-Gesamtstruktur bereit, in der Sie die Benutzer für Exchange um aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="a2f27-111">Deploy the Exchange Mailbox server roles in each Exchange Unified Messaging (UM) forest where you want to enable users for Exchange UM.</span></span> <span data-ttu-id="a2f27-112">Ausführliche Informationen zum Installieren von Exchange-Serverrollen finden Sie in der Dokumentation zu Microsoft Exchange Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a2f27-112">For details about installing Exchange server roles, see the Microsoft Exchange Server 2013 documentation.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="a2f27-113">Wenn Exchange Unified Messaging (um) installiert ist, ist es für die Verwendung eines selbstsignierten Zertifikats konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="a2f27-113">When Exchange Unified Messaging (UM) is installed, it is configured to use a self-signed certificate.</span></span><BR><span data-ttu-id="a2f27-114">Das selbstsignierte Zertifikat ermöglicht lync Server 2013 und Exchange um jedoch nicht, sich gegenseitig zu vertrauen, weshalb es notwendig ist, ein separates Zertifikat von einer Zertifizierungsstelle anzufordern, der beide Server Vertrauen.</span><span class="sxs-lookup"><span data-stu-id="a2f27-114">The self-signed certificate, however, does not enable Lync Server 2013 and Exchange UM to trust each other, which is why it is necessary to request a separate certificate from a certification authority that both servers trust.</span></span>

    
    </div>

  - <span data-ttu-id="a2f27-115">Wenn lync Server 2013 und Exchange um in verschiedenen Gesamtstrukturen installiert sind, konfigurieren Sie jede Exchange-Gesamtstruktur so, dass Sie der lync Server 2013-Gesamtstruktur und der lync Server 2013-Gesamtstruktur vertrauen, um jeder Exchange-Gesamtstruktur zu vertrauen.</span><span class="sxs-lookup"><span data-stu-id="a2f27-115">If Lync Server 2013 and Exchange UM are installed in different forests, configure each Exchange forest to trust the Lync Server 2013 forest and the Lync Server 2013 forest to trust each Exchange forest.</span></span> <span data-ttu-id="a2f27-116">Darüber hinaus können Sie die Exchange um-Einstellungen der Benutzer für die Benutzerobjekte in der lync Server 2013-Gesamtstruktur festlegen, indem Sie in der Regel ein Skript oder ein Gesamtstrukturübergreifendes Tool verwenden, beispielsweise Identity Lifecycle Manager (ILM).</span><span class="sxs-lookup"><span data-stu-id="a2f27-116">Also, set the users’ Exchange UM settings on the user objects in the Lync Server 2013 forest, typically by using a script or a cross-forest tool, such as Identity Lifecycle Manager (ILM).</span></span>

  - <span data-ttu-id="a2f27-117">Installieren Sie bei Bedarf die Exchange-Verwaltungskonsole zur Verwaltung Ihrer Unified Messaging-Server.</span><span class="sxs-lookup"><span data-stu-id="a2f27-117">If necessary, install the Exchange Management Console to manage your Unified Messaging servers.</span></span>

  - <span data-ttu-id="a2f27-118">Beziehen Sie gültige Rufnummern für Outlook Voice Access und für die automatische Telefonzentrale.</span><span class="sxs-lookup"><span data-stu-id="a2f27-118">Obtain valid phone numbers for Outlook Voice Access and auto attendant.</span></span>

  - <span data-ttu-id="a2f27-119">Wenn Sie eine frühere Exchange-Version als Microsoft Exchange Server 2010 Service Pack 1 (SP1) verwenden, koordinieren Sie die Namen für Exchange um SIP-URI-Wählpläne und Enterprise-VoIP-Wählpläne.</span><span class="sxs-lookup"><span data-stu-id="a2f27-119">If you are using a version of Exchange UM earlier than Microsoft Exchange Server 2010 Service Pack 1 (SP1), coordinate names for Exchange UM SIP URI dial plans and Enterprise Voice dial plans.</span></span>

<div>

## <a name="deploying-redundant-exchange-um-servers"></a><span data-ttu-id="a2f27-120">Bereitstellen redundanter Exchange UM-Server</span><span class="sxs-lookup"><span data-stu-id="a2f27-120">Deploying Redundant Exchange UM Servers</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a2f27-121">Wir empfehlen, dass Sie mindestens zwei Server bereitstellen, auf denen Exchange um-Dienste für jeden Exchange um-SIP-URI-Wählplan ausgeführt wird, den Sie für Ihre Organisation konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="a2f27-121">We recommend that you deploy a minimum of two servers on which Exchange UM services is running for each Exchange UM SIP URI dial plan that you configure for your organization.</span></span> <span data-ttu-id="a2f27-122">Zusätzlich zu einer höheren Kapazität bietet die Bereitstellung redundanter Server eine hohe Verfügbarkeit.</span><span class="sxs-lookup"><span data-stu-id="a2f27-122">In addition to providing expanded capacity, deploying redundant servers provides high availability.</span></span> <span data-ttu-id="a2f27-123">Bei einem Serverfehler kann lync Server 2013 so konfiguriert werden, dass ein Failover zu einem anderen Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a2f27-123">In the event of an server failure, Lync Server 2013 can be configured to fail over to another server.</span></span>



</div>

<span data-ttu-id="a2f27-124">Die folgenden Beispielkonfigurationen bieten Ausfallsicherheit für Exchange UM.</span><span class="sxs-lookup"><span data-stu-id="a2f27-124">The following example configurations provide Exchange UM resiliency.</span></span>

<span data-ttu-id="a2f27-125">**Beispiel 1: Exchange UM-Ausfallsicherheit**</span><span class="sxs-lookup"><span data-stu-id="a2f27-125">**Example 1: Exchange UM Resiliency**</span></span>

<span data-ttu-id="a2f27-126">![Exchange um-Beispiel 1](images/Gg398656.3644b847-0847-4550-a989-e3fc51de5c4b(OCS.15).jpg "Exchange um-Beispiel 1")</span><span class="sxs-lookup"><span data-stu-id="a2f27-126">![Exchange UM Example 1](images/Gg398656.3644b847-0847-4550-a989-e3fc51de5c4b(OCS.15).jpg "Exchange UM Example 1")</span></span>

<span data-ttu-id="a2f27-p105">In Beispiel 1 sind die Exchange UM-Server 1 und 2 im Rechenzentrum "Tukwila" aktiviert, die Exchange UM-Server 3 und 4 im Rechenzentrum "Dublin". Bei einem Exchange UM-Ausfall in Tukwila sollten die DNS-A-Einträge für die Server 1 und 2 so konfiguriert sein, dass sie auf den Server 3 bzw. 4 zeigen. Bei einem Exchange UM-Ausfall in Dublin sollten die DNS-A-Einträge für die Server 3 und 4 so konfiguriert sein, dass sie auf den Server 1 bzw. 2 zeigen.</span><span class="sxs-lookup"><span data-stu-id="a2f27-p105">In Example 1, Exchange UM servers 1 and 2 are enabled in the Tukwila data center, and Exchange UM servers 3 and 4 are enabled in the Dublin data center. In the event of an Exchange UM outage in Tukwila, the Domain Name System (DNS) A records for servers 1 and 2 should be configured to point to servers 3 and 4, respectively. In the event of an Exchange UM outage in Dublin, the DNS A records for servers 3 and 4 should be configured to point to servers 1 and 2, respectively.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a2f27-130">In Beispiel 1 sollten Sie zudem auf jedem Exchange UM-Server eins der folgenden Zertifikate zuweisen:</span><span class="sxs-lookup"><span data-stu-id="a2f27-130">For Example 1, you should also assign one of following certificate on each Exchange UM server:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="a2f27-131">Verwenden Sie ein Zertifikat mit einem Platzhalter im alternativen Antragstellernamen.</span><span class="sxs-lookup"><span data-stu-id="a2f27-131">Use a certificate with a wildcard in the Subject Alternative Name (SAN).</span></span></P>
> <LI>
> <P><span data-ttu-id="a2f27-132">Tragen Sie die vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) der einzelnen Exchange UM-Server als alternativen Antragstellernamen ein.</span><span class="sxs-lookup"><span data-stu-id="a2f27-132">Put the fully qualified domain name (FQDN) of each of the four Exchange UM servers in the SAN.</span></span></P></LI></UL>



</div>

<span data-ttu-id="a2f27-133">**Beispiel 2: Exchange UM-Ausfallsicherheit**</span><span class="sxs-lookup"><span data-stu-id="a2f27-133">**Example 2: Exchange UM Resiliency**</span></span>

<span data-ttu-id="a2f27-134">![Exchange um-Beispiel 2](images/Gg398656.15754273-306e-448d-b258-84bc2936a2e8(OCS.15).jpg "Exchange um-Beispiel 2")</span><span class="sxs-lookup"><span data-stu-id="a2f27-134">![Exchange UM Example 2](images/Gg398656.15754273-306e-448d-b258-84bc2936a2e8(OCS.15).jpg "Exchange UM Example 2")</span></span>

<span data-ttu-id="a2f27-p106">In Beispiel 2 sind die Exchange UM-Server 1 und 2 bei normalen Betriebsbedingungen im Rechenzentrum "Tukwila" aktiviert, die Exchange UM-Server 3 und 4 im Rechenzentrum "Dublin". Alle vier Server sind in den SIP-URI-Wähleinstellungen der Benutzer in Tukwila enthalten, die Server 3 und 4 sind deaktiviert. Wenn Exchange UM z. B. in Tukwila ausfällt, sollten die Exchange UM-Server 1 und 2 deaktiviert und die Exchange UM-Server 3 und 4 aktiviert werden, damit der Exchange UM-Datenverkehr in Tukwila an die Server in Dublin geroutet wird.</span><span class="sxs-lookup"><span data-stu-id="a2f27-p106">In Example 2, under ordinary operating conditions Exchange UM servers 1 and 2 are enabled in the Tukwila data center, and Exchange UM servers 3 and 4 are enabled in the Dublin data center. All four servers are included in the Tukwila users' SIP URI dial plan; however, servers 3 and 4 are disabled. In the event of an Exchange UM outage in Tukwila, for example, Exchange UM servers 1 and 2 should be disabled and Exchange UM servers 3 and 4 should be enabled so the Tukwila Exchange UM traffic will be routed to the servers in Dublin.</span></span>

<span data-ttu-id="a2f27-138">Details zum Aktivieren oder Deaktivieren von Unified Messaging auf Exchange 2013 finden Sie unter "Integration von Exchange 2013 um mit lync Server" unter [https://go.microsoft.com/fwlink/p/?LinkId=265372](https://go.microsoft.com/fwlink/p/?linkid=265372) .</span><span class="sxs-lookup"><span data-stu-id="a2f27-138">For details about how to enable or disable Unified Messaging on Exchange 2013, see “Integrate Exchange 2013 UM with Lync Server” at [https://go.microsoft.com/fwlink/p/?LinkId=265372](https://go.microsoft.com/fwlink/p/?linkid=265372).</span></span>

<span data-ttu-id="a2f27-139">Details zum Aktivieren oder Deaktivieren von Unified Messaging auf Microsoft Exchange Server 2010 finden Sie unter:</span><span class="sxs-lookup"><span data-stu-id="a2f27-139">For details about how to enable or disable Unified Messaging on Microsoft Exchange Server 2010, see:</span></span>

  - <span data-ttu-id="a2f27-140">"Unified Messaging auf Exchange 2010 aktivieren" unter [https://go.microsoft.com/fwlink/p/?LinkId=204418](https://go.microsoft.com/fwlink/p/?linkid=204418) .</span><span class="sxs-lookup"><span data-stu-id="a2f27-140">"Enable Unified Messaging on Exchange 2010" at [https://go.microsoft.com/fwlink/p/?LinkId=204418](https://go.microsoft.com/fwlink/p/?linkid=204418).</span></span>

  - <span data-ttu-id="a2f27-141">"Unified Messaging auf Exchange 2010 deaktivieren" unter [https://go.microsoft.com/fwlink/p/?LinkId=204416](https://go.microsoft.com/fwlink/p/?linkid=204416) .</span><span class="sxs-lookup"><span data-stu-id="a2f27-141">"Disable Unified Messaging on Exchange 2010" at [https://go.microsoft.com/fwlink/p/?LinkId=204416](https://go.microsoft.com/fwlink/p/?linkid=204416).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a2f27-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2f27-142">See Also</span></span>


[<span data-ttu-id="a2f27-143">Bereitstellungsprozess für die Integration von lokalen Unified Messaging-Diensten und Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a2f27-143">Deployment process for integrating on-premises Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md)  
  

<span data-ttu-id="a2f27-144"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a2f27-144"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

