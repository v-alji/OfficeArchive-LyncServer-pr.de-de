---
title: 'Lync Server 2013: Planen der Integration von Exchange Unified Messaging'
description: 'Lync Server 2013: Planen der Integration von Exchange Unified Messaging'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Exchange Unified Messaging integration
ms:assetid: e7c63a71-2d99-4aa9-b649-36c1a431bdf1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399031(v=OCS.15)
ms:contentKeyID: 48185880
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31296444d21a86a7837da3e29fc2152f3ca96ccc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442999"
---
# <a name="planning-for-exchange-unified-messaging-integration-in-lync-server-2013"></a><span data-ttu-id="dc976-103">Planen der Integration von Exchange Unified Messaging in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc976-103">Planning for Exchange Unified Messaging integration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dc976-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dc976-104">

<span> </span></span></span>

<span data-ttu-id="dc976-105">_**Letztes Änderungsdatum des Themas:** 2012-10-13_</span><span class="sxs-lookup"><span data-stu-id="dc976-105">_**Topic Last Modified:** 2012-10-13_</span></span>

<span data-ttu-id="dc976-106">Lync Server 2013 unterstützt die Integration in Exchange Unified Messaging (um) zum Kombinieren von Voicemail und e-Mail-Messaging in einer einzelnen Messaginginfrastruktur.</span><span class="sxs-lookup"><span data-stu-id="dc976-106">Lync Server 2013 supports integration with Exchange Unified Messaging (UM) for combining voice messaging and email messaging into a single messaging infrastructure.</span></span> <span data-ttu-id="dc976-107">In Microsoft Exchange Server 2007 Service Pack 1 (SP1) und Microsoft Exchange Server 2010 ist Exchange Unified Messaging (um) eine von mehreren Exchange-Serverfunktionen, die Sie installieren und konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="dc976-107">In Microsoft Exchange Server 2007 Service Pack 1 (SP1) and Microsoft Exchange Server 2010, Exchange Unified Messaging (UM) is one of several Exchange server roles that you can install and configure.</span></span>

<span data-ttu-id="dc976-108">In Microsoft Exchange Server 2013 wird Exchange um als Dienst auf einem Exchange-Post Fach Server ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="dc976-108">In Microsoft Exchange Server 2013, Exchange UM runs as a service on an Exchange Mailbox server.</span></span> <span data-ttu-id="dc976-109">Bei lync Server 2013 Enterprise-VoIP-Bereitstellungen kombiniert Unified Messaging Voicemail und e-Mail-Nachrichten in einem einzigen Speicher, der über ein Telefon (Outlook Voice Access) oder einen Computer zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="dc976-109">For Lync Server 2013 Enterprise Voice deployments, Unified Messaging combines voice messaging and email messaging into a single store that is available from a telephone (Outlook Voice Access) or a computer.</span></span> <span data-ttu-id="dc976-110">Unified Messaging und lync Server 2013 arbeiten gemeinsam an der Bereitstellung von Anrufbeantwortung, Outlook Voice Access und automatischen Telefonzentralen Diensten für Benutzer von Enterprise-VoIP.</span><span class="sxs-lookup"><span data-stu-id="dc976-110">Unified Messaging and Lync Server 2013 work together to provide call answering, Outlook Voice Access, and auto-attendant services to users of Enterprise Voice.</span></span>

<span data-ttu-id="dc976-111">Weitere Informationen zu den Architekturänderungen in Microsoft Exchange Server 2013 finden Sie unter "Änderungen der Spracharchitektur" in der Microsoft Exchange Server 2013-Dokumentation unter [https://go.microsoft.com/fwlink/p/?LinkId=266730](https://go.microsoft.com/fwlink/p/?linkid=266730) .</span><span class="sxs-lookup"><span data-stu-id="dc976-111">For more information about the architecture changes in Microsoft Exchange Server 2013, see “Voice Architecture Changes” in the Microsoft Exchange Server 2013 documentation at [https://go.microsoft.com/fwlink/p/?LinkId=266730](https://go.microsoft.com/fwlink/p/?linkid=266730).</span></span>

<span data-ttu-id="dc976-112">Damit diese Features in einer lokalen Exchange um-Bereitstellung unterstützt werden, müssen Sie eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="dc976-112">For these features to be supported in an on-premises Exchange UM deployment, you must be running one of the following:</span></span>

  - <span data-ttu-id="dc976-113">Microsoft Exchange Server 2007 Service Pack 1 (SP1) oder neuestes Service Pack</span><span class="sxs-lookup"><span data-stu-id="dc976-113">Microsoft Exchange Server 2007 Service Pack 1 (SP1) or latest service pack</span></span>

  - <span data-ttu-id="dc976-114">Microsoft Exchange Server 2010 oder neuestes Service Pack</span><span class="sxs-lookup"><span data-stu-id="dc976-114">Microsoft Exchange Server 2010 or latest service pack</span></span>

  - <span data-ttu-id="dc976-115">Microsoft Exchange Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc976-115">Microsoft Exchange Server 2013</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="dc976-116">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="dc976-116">In This Section</span></span>

  - [<span data-ttu-id="dc976-117">Features von integriertem Unified Messaging und Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc976-117">Features of integrated Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-features-of-integrated-unified-messaging.md)

  - [<span data-ttu-id="dc976-118">Komponenten und Topologien für lokales Unified Messaging in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc976-118">Components and topologies for on-premises Unified Messaging in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-on-premises-unified-messaging.md)

  - [<span data-ttu-id="dc976-119">Richtlinien für die Integration lokaler Unified Messaging-Dienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc976-119">Guidelines for integrating on-premises Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-guidelines-for-integrating-on-premises-unified-messaging.md)

  - [<span data-ttu-id="dc976-120">Bereitstellungsprozess für die Integration von lokalen Unified Messaging-Diensten und Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc976-120">Deployment process for integrating on-premises Unified Messaging and Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-integrating-on-premises-unified-messaging.md)

<span data-ttu-id="dc976-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dc976-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

