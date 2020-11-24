---
title: 'Lync Server 2013: Unterstützung für die Integration gehosteter Exchange UM-Dienste'
description: Lync Server 2013-Unterstützung für die gehostete Exchange um-Integration
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Support for hosted Exchange UM integration
ms:assetid: c7573ec3-013c-48d9-b59b-2a5427e6da35
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398821(v=OCS.15)
ms:contentKeyID: 48185376
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 88920667d703bc634921903e8e3995cb65db6873
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393939"
---
# <a name="support-for-hosted-exchange-um-integration-in-lync-server-2013"></a><span data-ttu-id="142ac-103">Unterstützung für die Integration gehosteter Exchange UM-Dienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="142ac-103">Support for hosted Exchange UM integration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="142ac-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="142ac-104">

<span> </span></span></span>

<span data-ttu-id="142ac-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="142ac-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="142ac-106">Die lync Server 2013 ExUM-Routing Anwendung unterstützt die Integration in Exchange Unified Messaging (um) in einer lokalen Umgebung, in der lync Server 2013 und Exchange um sowohl lokal innerhalb Ihres Unternehmens als auch in Exchange um von einem Dienstanbieter gehostet werden, wie in der folgenden Abbildung dargestellt.</span><span class="sxs-lookup"><span data-stu-id="142ac-106">The Lync Server 2013 ExUM Routing application supports integration with Exchange Unified Messaging (UM) in an on-premises environment, where Lync Server 2013 and Exchange UM are both installed locally within your enterprise, or in with Exchange UM hosted by a service provider, as shown in the following diagram.</span></span>

<span data-ttu-id="142ac-107">![Lokale lync Server Exchange um-Bereitstellung](images/Gg398821.d6498eb9-87ee-40f3-8ecd-852f91546590(OCS.15).jpg "Lokale lync Server Exchange um-Bereitstellung")</span><span class="sxs-lookup"><span data-stu-id="142ac-107">![On-premises Lync Server Exchange UM Deployment](images/Gg398821.d6498eb9-87ee-40f3-8ecd-852f91546590(OCS.15).jpg "On-premises Lync Server Exchange UM Deployment")</span></span>

<span data-ttu-id="142ac-108">Die folgenden Modi werden unterstützt:</span><span class="sxs-lookup"><span data-stu-id="142ac-108">The following modes are supported:</span></span>

  - <span data-ttu-id="142ac-109">**Lokal Modus**   Lync Server 2013 und Exchange um sind beide auf lokalen Servern innerhalb Ihres Unternehmens bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="142ac-109">**On-premises Mode**   Lync Server 2013 and Exchange UM are both deployed on local servers within your enterprise.</span></span>

  - <span data-ttu-id="142ac-110">**Standortübergreifender Modus**   Lync Server 2013 wird auf lokalen Servern innerhalb Ihres Unternehmens bereitgestellt, und Exchange um wird in der Einrichtung eines Onlinedienstanbieters, beispielsweise in einem Microsoft Exchange Online-Rechenzentrum, gehostet.</span><span class="sxs-lookup"><span data-stu-id="142ac-110">**Cross-premises Mode**   Lync Server 2013 is deployed on local servers within your enterprise and Exchange UM is hosted in an online service provider’s facility, such as a Microsoft Exchange Online data center.</span></span>

  - <span data-ttu-id="142ac-111">**Gemischter Modus**   Bei ihrer lync Server 2013-Bereitstellung sind einige Benutzerpostfächer auf lokalen Servern mit Microsoft Exchange Server innerhalb Ihres Unternehmens und einige Postfächer in einem gehosteten Exchange-Dienst-Rechenzentrum verwaltet.</span><span class="sxs-lookup"><span data-stu-id="142ac-111">**Mixed Mode**   Your Lync Server 2013 deployment has some user mailboxes homed on local servers running Microsoft Exchange Server within your enterprise and some mailboxes homed in a hosted Exchange service data center.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="142ac-112">Der gemischte Modus kann während der Evaluierung und schrittweisen Migration von Benutzern zu Hosted Exchange um als Übergangslösung verwendet werden, oder als dauerhafte Lösung, wenn Sie sich entscheiden, die Exchange um-Dienste einiger Benutzer nach der Migration anderer Personen lokal zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="142ac-112">Mixed mode can be used as a transitional solution during evaluation and stepwise migration of users to hosted Exchange UM, or as a permanent solution if you opt to keep some users’ Exchange UM services on-premises after migrating others.</span></span>

    
    </div>

<span data-ttu-id="142ac-113">Zum Integrieren von lync Server 2013 in gehostete Exchange um müssen Sie einen *freigegebenen SIP-Adressraum* (auch als *geteilte Domäne* bezeichnet) konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="142ac-113">To integrate Lync Server 2013 with hosted Exchange UM, you must configure a *shared SIP address space* (also called a *split domain*).</span></span> <span data-ttu-id="142ac-114">In dieser Konfiguration können sowohl lync Server 2013 als auch der von einem Drittanbieter gehostete Exchange um-Dienstanbieter auf denselben SIP-Domänen Adressraum zugreifen.</span><span class="sxs-lookup"><span data-stu-id="142ac-114">In this configuration, both Lync Server 2013 and the third-party hosted Exchange UM service provider can access the same SIP domain address space.</span></span> <span data-ttu-id="142ac-115">Ausführliche Informationen finden Sie unter [Hosted Exchange um-Integrationsarchitektur in lync Server 2013](lync-server-2013-hosted-exchange-um-integration-architecture.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="142ac-115">For details, see [Hosted Exchange UM integration architecture in Lync Server 2013](lync-server-2013-hosted-exchange-um-integration-architecture.md) in the Planning documentation.</span></span>

<span data-ttu-id="142ac-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="142ac-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

