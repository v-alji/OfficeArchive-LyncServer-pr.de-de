---
title: 'Lync Server 2013: Integration in gehostete Exchange Unified Messaging-Dienste'
description: 'Lync Server 2013: Hosted Exchange Unified Messaging-Integration.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted Exchange Unified Messaging integration
ms:assetid: f4de0165-da3b-499e-98fc-28ddd0db02d5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413027(v=OCS.15)
ms:contentKeyID: 48185829
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 980c0bc47258e9fae94ff623559342ca36eea145
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427530"
---
# <a name="hosted-exchange-unified-messaging-integration-in-lync-server-2013"></a><span data-ttu-id="c166d-103">Integration in gehostete Exchange Unified Messaging-Dienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c166d-103">Hosted Exchange Unified Messaging integration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c166d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c166d-104">

<span> </span></span></span>

<span data-ttu-id="c166d-105">_**Letztes Änderungsdatum des Themas:** 2012-09-20_</span><span class="sxs-lookup"><span data-stu-id="c166d-105">_**Topic Last Modified:** 2012-09-20_</span></span>

<span data-ttu-id="c166d-106">Zusätzlich zu der Unterstützung, die frühere lync Server 2013-Versionen für die Integration in *lokale* Bereitstellungen von Exchange Unified Messaging (um) bereitgestellt haben, stellt lync Server 2013 die Unterstützung für die Integration in *gehostete* Exchange um.</span><span class="sxs-lookup"><span data-stu-id="c166d-106">In addition to the support that previous Lync Server 2013 releases have provided for integration with *on-premises* deployments of Exchange Unified Messaging (UM), Lync Server 2013 introduces support for integration with *hosted* Exchange UM.</span></span> <span data-ttu-id="c166d-107">Hosted Exchange um ermöglicht es lync Server 2013, Ihren Benutzern Sprachnachrichten bereitzustellen, wenn Sie einige oder alle von Ihnen an einen gehosteten Exchange-Dienstanbieter wie Microsoft Exchange Online übertragen.</span><span class="sxs-lookup"><span data-stu-id="c166d-107">Hosted Exchange UM enables Lync Server 2013 to provide voice messaging to your users if you transfer some or all of them to a hosted Exchange service provider such as Microsoft Exchange Online.</span></span>

<span data-ttu-id="c166d-108">Lync Server 2013 Enterprise Voice verwendet die Exchange um-Infrastruktur für die Bereitstellung von Anrufannahme, Anrufbenachrichtigung, Sprachzugriff (einschließlich Voicemail) und automatischen Telefonzentralen Diensten.</span><span class="sxs-lookup"><span data-stu-id="c166d-108">Lync Server 2013 Enterprise Voice uses the Exchange UM infrastructure to provide call answering, call notification, voice access (including voice mail), and auto attendant services.</span></span> <span data-ttu-id="c166d-109">Ausführliche Informationen finden Sie unter [Features von Integrated Unified Messaging und lync Server 2013](lync-server-2013-features-of-integrated-unified-messaging.md).</span><span class="sxs-lookup"><span data-stu-id="c166d-109">For details, see [Features of integrated Unified Messaging and Lync Server 2013](lync-server-2013-features-of-integrated-unified-messaging.md).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c166d-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c166d-110">In This Section</span></span>

  - [<span data-ttu-id="c166d-111">Architektur und Routing für gehostete Exchange UM-Dienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c166d-111">Hosted Exchange UM architecture and routing in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-um-architecture-and-routing.md)

  - [<span data-ttu-id="c166d-112">Richtlinien für gehostete Voicemail in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c166d-112">Hosted voice mail policies in Lync Server 2013</span></span>](lync-server-2013-hosted-voice-mail-policies.md)

  - [<span data-ttu-id="c166d-113">Benutzerverwaltung für gehostete Exchange-Dienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c166d-113">Hosted Exchange user management in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-user-management.md)

  - [<span data-ttu-id="c166d-114">Kontaktobjektverwaltung für gehostete Exchange-Dienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c166d-114">Hosted Exchange Contact object management in Lync Server 2013</span></span>](lync-server-2013-hosted-exchange-contact-object-management.md)

  - [<span data-ttu-id="c166d-115">Bereitstellungsprozess für die Integration gehosteter Exchange UM-Dienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c166d-115">Deployment process for integrating hosted Exchange UM with Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-integrating-hosted-exchange-um.md)

<span data-ttu-id="c166d-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c166d-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

