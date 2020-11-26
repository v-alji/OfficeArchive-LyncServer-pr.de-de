---
title: 'Lync Server 2013: Routing für gehostete Exchange UM-Dienste'
description: 'Lync Server 2013: Hosted Exchange um-Routing.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted Exchange UM routing
ms:assetid: 6c90dc8b-6aef-4ce8-b483-37c7b5a553c2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398512(v=OCS.15)
ms:contentKeyID: 48184422
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 72fbdee5550ae53d5ff5e7513ea384cedad62c5a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427596"
---
# <a name="hosted-exchange-um-routing-in-lync-server-2013"></a><span data-ttu-id="01a79-103">Routing für gehostete Exchange UM-Dienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="01a79-103">Hosted Exchange UM routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="01a79-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="01a79-104">

<span> </span></span></span>

<span data-ttu-id="01a79-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="01a79-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="01a79-106">Die Exchange um-Routing Anwendung wird auf dem Front-End-Server ausgeführt, um Anrufe an eine lokale Microsoft Exchange Server Unified Messaging (um)-Bereitstellung oder an einen gehosteten Exchange um-Dienst weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="01a79-106">The Exchange UM Routing application runs on the Front End Server to route calls, either to an on-premises Microsoft Exchange Server Unified Messaging (UM) deployment or to hosted Exchange UM service.</span></span>

<div>

## <a name="the-exum-routing-application"></a><span data-ttu-id="01a79-107">Die ExUM-Routing Anwendung</span><span class="sxs-lookup"><span data-stu-id="01a79-107">The ExUM Routing Application</span></span>

<span data-ttu-id="01a79-108">Die lync Server 2013 Exchange um-Routing Anwendung verwendet Informationen aus den Einstellungen des Benutzerkontos und den Richtlinienparametern für gehostete Voicemail, um zu bestimmen, wie Anrufe für gehostete Voicemail weitergeleitet werden, wie im folgenden Diagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="01a79-108">The Lync Server 2013 Exchange UM Routing application uses information from user account settings and from hosted voice mail policy parameters to determine how to route calls for hosted voice messaging, as shown in the following diagram.</span></span>

<span data-ttu-id="01a79-109">**Beispiel für eine gemischte Bereitstellung Exchange um-Routing**</span><span class="sxs-lookup"><span data-stu-id="01a79-109">**Example of mixed deployment Exchange UM routing**</span></span>

<span data-ttu-id="01a79-110">![Lokale lync Server Exchange um-Bereitstellung](images/Gg398512.75258286-1f23-487b-bf46-d8538e7d540e(OCS.15).jpg "Lokale lync Server Exchange um-Bereitstellung")</span><span class="sxs-lookup"><span data-stu-id="01a79-110">![On-premises Lync Server Exchange UM deployment](images/Gg398512.75258286-1f23-487b-bf46-d8538e7d540e(OCS.15).jpg "On-premises Lync Server Exchange UM deployment")</span></span>

<span data-ttu-id="01a79-111">Das Exchange um-Routing kann so konfiguriert werden, dass Anrufe an Benutzer weitergeleitet werden, die für lokalen Exchange um aktiviert sind, für Benutzer, die für gehostete Exchange um aktiviert sind, oder für eine Kombination der beiden.</span><span class="sxs-lookup"><span data-stu-id="01a79-111">Exchange UM routing can be configured to route calls to users who are enabled for on-premises Exchange UM, to users who are enabled for hosted Exchange UM, or to a combination of the two.</span></span>

<span data-ttu-id="01a79-112">Nehmen wir beispielsweise an, dass das Postfach und der Exchange um-Dienst von Roy in einer lokalen Exchange-Bereitstellung verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="01a79-112">For example, suppose that Roy’s mailbox and Exchange UM service are homed in an on-premises Exchange deployment.</span></span>

  - <span data-ttu-id="01a79-113">Die Proxyadressinformationen des Benutzerkontos von Roy stellen die Informationen bereit, die von der ExUM-Routing Anwendung zum Weiterleiten von Anrufen an einen lokalen Exchange um-Server verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="01a79-113">The proxy address information from Roy’s user account provides the information that the ExUM Routing application uses to route his calls to an on-premises Exchange UM server.</span></span>

<span data-ttu-id="01a79-114">Alices Postfach und Exchange um-Dienst befinden sich im Rechenzentrum eines gehosteten Exchange-Dienstanbieters.</span><span class="sxs-lookup"><span data-stu-id="01a79-114">Alice’s mailbox and Exchange UM service are located at a hosted Exchange service provider’s data center.</span></span> <span data-ttu-id="01a79-115">Das Routing für Ihre Exchange um-Anrufe ist wie folgt konfiguriert:</span><span class="sxs-lookup"><span data-stu-id="01a79-115">Routing for her Exchange UM calls is configured as follows:</span></span>

  - <span data-ttu-id="01a79-116">Die Werte, die im msExchUCVoiceMailSettings-Attribut des Benutzerkontos von Alice festgesetzt sind, weisen die ExUM-Routing Anwendung an, auf Routing Details in einer gehosteten Voicemail-Richtlinie zu überprüfen.</span><span class="sxs-lookup"><span data-stu-id="01a79-116">The values set in the msExchUCVoiceMailSettings attribute of Alice’s user account tell the ExUM Routing application to check for routing details in a hosted voice mail policy.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="01a79-117">Der Wert des Attributs msExchUCVoiceMailSettings kann entweder vom Exchange-Dienstanbieter oder vom lync Server 2013-Administrator eingestellt werden.</span><span class="sxs-lookup"><span data-stu-id="01a79-117">The value of the msExchUCVoiceMailSettings attribute can be set by either the Exchange service provider or the Lync Server 2013 administrator.</span></span> <span data-ttu-id="01a79-118">In dem im vorherigen Diagramm gezeigten Beispiel wurde der Wert (CsHostedVoiceMail = 1) vom lync Server 2013-Administrator so eingerichtet, dass die gehostete Voicemail für Alice aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="01a79-118">In the example shown in the preceding diagram, the value (CsHostedVoiceMail=1) was set by the Lync Server 2013 administrator to enable hosted voice mail for Alice.</span></span> <span data-ttu-id="01a79-119">Details zu diesem Attribut finden Sie unter <A href="lync-server-2013-hosted-exchange-user-management.md">gehostete Exchange-Benutzerverwaltung in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="01a79-119">For details about this attribute, see <A href="lync-server-2013-hosted-exchange-user-management.md">Hosted Exchange user management in Lync Server 2013</A>.</span></span>

    
    </div>

  - <span data-ttu-id="01a79-120">Die Hosted Voicemail-Richtlinie, die dem Benutzerkonto von Alice zugewiesen ist, bietet Routing Details:</span><span class="sxs-lookup"><span data-stu-id="01a79-120">The hosted voice mail policy that is assigned to Alice’s user account provides routing details:</span></span>
    
      - <span data-ttu-id="01a79-121">Ziel ist der gehostete Exchange um-Dienstanbieter (LS). ExUm. \<hostedExchangeServer\> com in diesem Beispiel).</span><span class="sxs-lookup"><span data-stu-id="01a79-121">Destination is the hosted Exchange UM service provider (ls.ExUm.\<hostedExchangeServer\>.com in this example).</span></span>
    
      - <span data-ttu-id="01a79-122">Organisationen werden durch die Mandanten-IDs identifiziert, bei denen es sich um die Routing-FQDNs für SIP-Nachrichten für Exchange Server-Mandanten handelt, die sich auf LS befinden. ExUm. \<hostedExchangeServer\> com (Corp.contoso.com und Corp.litwareinc.com in diesem Beispiel).</span><span class="sxs-lookup"><span data-stu-id="01a79-122">Organizations are identified by the tenant IDs, which are the routing FQDNs for SIP messages for Exchange Server tenants that are located on ls.ExUm.\<hostedExchangeServer\>.com (corp.contoso.com and corp.litwareinc.com in this example).</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="01a79-123">Der FQDN für Exchange Online lautet exap.um.Outlook.com.</span><span class="sxs-lookup"><span data-stu-id="01a79-123">The FQDN for Exchange Online is exap.um.outlook.com.</span></span>

        
        </div>
        
        <span data-ttu-id="01a79-124">Ausführliche Informationen finden Sie unter [Richtlinien für gehostete Voicemail in lync Server 2013](lync-server-2013-hosted-voice-mail-policies.md).</span><span class="sxs-lookup"><span data-stu-id="01a79-124">For details, see [Hosted voice mail policies in Lync Server 2013](lync-server-2013-hosted-voice-mail-policies.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="01a79-125">Wenn in einem Benutzerkonto sowohl das msExchUCVoiceMailSettings-Attribut als auch die um-Proxy Adresseinstellungen vorhanden sind, hat das msExchUCVoiceMailSettings-Attribut Vorrang.</span><span class="sxs-lookup"><span data-stu-id="01a79-125">If both the msExchUCVoiceMailSettings attribute and the UM proxy address settings are present in a user account, the msExchUCVoiceMailSettings attribute takes precedence.</span></span>



<span data-ttu-id="01a79-126"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="01a79-126"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

