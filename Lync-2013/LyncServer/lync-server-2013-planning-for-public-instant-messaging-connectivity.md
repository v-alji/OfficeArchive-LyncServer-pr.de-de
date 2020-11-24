---
title: 'Lync Server 2013: Planen der öffentlichen Instant Messaging-Konnektivität'
description: 'Lync Server 2013: Planen der öffentlichen Instant Messaging-Konnektivität'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for public instant messaging connectivity
ms:assetid: e75e8884-05c7-414a-8014-bc9aa8126fb7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205349(v=OCS.15)
ms:contentKeyID: 48185698
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9a020a291a39d78aea9271926c99b508a8cd9827
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395338"
---
# <a name="planning-for-public-instant-messaging-connectivity-in-lync-server-2013"></a><span data-ttu-id="4f777-103">Planen der öffentlichen Instant Messaging-Konnektivität in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4f777-103">Planning for public instant messaging connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4f777-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4f777-104">

<span> </span></span></span>

<span data-ttu-id="4f777-105">_**Letztes Änderungsdatum des Themas:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="4f777-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="4f777-106">Die öffentliche Instant Messaging-Konnektivität ist eine Klasse des Föderations-und ist so konfiguriert, dass Ihre internen und externen lync Server 2013-Benutzer Kontakte aus einem der folgenden hinzufügen können:</span><span class="sxs-lookup"><span data-stu-id="4f777-106">Public Instant Messaging Connectivity is a class of federation, and is configured to allow your internal and external Lync Server 2013 users to add contacts from any of the following:</span></span>

  - <span data-ttu-id="4f777-107">Messenger-Kontakte</span><span class="sxs-lookup"><span data-stu-id="4f777-107">Messenger contacts</span></span>

  - <span data-ttu-id="4f777-108">Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="4f777-108">Yahoo\!</span></span> <span data-ttu-id="4f777-109">Kontakte</span><span class="sxs-lookup"><span data-stu-id="4f777-109">contacts</span></span>

  - <span data-ttu-id="4f777-110">America Online (AOL)-Kontakte</span><span class="sxs-lookup"><span data-stu-id="4f777-110">America Online (AOL) contacts</span></span>

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="4f777-111">Ab dem 1. September, 2012, ist die Microsoft lync Public Chat-Benutzerabonnementlizenz (PIC USL) nicht mehr für den Kauf für neue oder erneuernde Vereinbarungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="4f777-111">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (PIC USL) is no longer available for the purchase for new or renewing agreements.</span></span> <span data-ttu-id="4f777-112">Kunden mit aktiven Lizenzen sind in der Lage, weiterhin mit Yahoo! zu verbünden</span><span class="sxs-lookup"><span data-stu-id="4f777-112">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="4f777-113">Messenger bis zum Shutdown-Datum des Diensts.</span><span class="sxs-lookup"><span data-stu-id="4f777-113">Messenger until the service shutdown date.</span></span> <span data-ttu-id="4f777-114">Datum des Endes des Lebenszyklus von Juni 2014 für AOL und Yahoo!</span><span class="sxs-lookup"><span data-stu-id="4f777-114">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="4f777-115">wurde angekündigt.</span><span class="sxs-lookup"><span data-stu-id="4f777-115">has been announced.</span></span> <span data-ttu-id="4f777-116">Ausführliche Informationen finden Sie <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">unter Unterstützung für öffentliche Instant Messenger-Konnektivität in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="4f777-116">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="4f777-117">Bei der PIC-USL handelt es sich um eine pro Benutzer/Monat-Abonnementlizenz, die für lync Server oder Office Communications Server für die Föderation mit Yahoo! erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="4f777-117">The PIC USL is a per-user, per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="4f777-118">Messenger.</span><span class="sxs-lookup"><span data-stu-id="4f777-118">Messenger.</span></span> <span data-ttu-id="4f777-119">Die Möglichkeit von Microsoft, diesen Dienst bereitzustellen, war von der Unterstützung durch Yahoo! abhängig, deren zugrunde liegende Vereinbarung nicht verlängert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="4f777-119">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which will not be renewed.</span></span></P>
> <LI>
> <P><span data-ttu-id="4f777-120">Lync ist mehr denn je ein leistungsfähiges Tool für die Verbindung zwischen Organisationen und Personen in der ganzen Welt.</span><span class="sxs-lookup"><span data-stu-id="4f777-120">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="4f777-121">Für den Verbund mit Windows Live Messenger sind keine zusätzlichen Benutzer-und Gerätelizenzen außerhalb der lync-Standard CAL erforderlich.</span><span class="sxs-lookup"><span data-stu-id="4f777-121">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="4f777-122">Skype Federation wird dieser Liste hinzugefügt und ermöglicht es lync-Benutzern, Hunderte von Millionen von Personen über Chat und Sprache zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="4f777-122">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people through IM and voice.</span></span></P></LI></UL>



</div>

<span data-ttu-id="4f777-123">Für diese Föderations Klasse sind die folgenden Planungsüberlegungen erforderlich:</span><span class="sxs-lookup"><span data-stu-id="4f777-123">This class of federation requires the following planning considerations:</span></span>

  - <span data-ttu-id="4f777-124">Benutzer von Windows Live Messenger können neben Instant Messaging auch eine Peer-to-Peer-Audio/visuelle Kommunikation mit lync Server 2013-Benutzern führen.</span><span class="sxs-lookup"><span data-stu-id="4f777-124">Windows Live Messenger users can have peer-to-peer audio/visual communication with Lync Server 2013 users, in addition to instant messaging.</span></span> <span data-ttu-id="4f777-125">Ihre Edgeserver müssen bestimmte Port-und Protokollanforderungen erfüllen.</span><span class="sxs-lookup"><span data-stu-id="4f777-125">Your Edge Servers must meet specific port and protocol requirements.</span></span> <span data-ttu-id="4f777-126">Ausführliche Informationen finden Sie unter [ermitteln externer A/V-Firewall-und Portanforderungen für lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span><span class="sxs-lookup"><span data-stu-id="4f777-126">For details, see [Determine external A/V firewall and port requirements for Lync Server 2013](lync-server-2013-determine-external-a-v-firewall-and-port-requirements.md).</span></span>

  - <span data-ttu-id="4f777-127">Yahoo Instant Messaging hat keine eindeutigen Anforderungen, außer denen, die normalerweise bei der Planung und Bereitstellung des typischen Edgeserver verwendet werden, der Föderation bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="4f777-127">Yahoo instant messaging has no unique requirements, other than those typically used in the planning and deployment of the typical Edge Server that is providing federation.</span></span>

  - <span data-ttu-id="4f777-128">Für America Online ist es erforderlich, dass Ihr Edge-Server-Zertifikat, das dem Access-Edgedienst zugewiesen ist, über eine erweiterte Client-Schlüsselverwendung verfügt.</span><span class="sxs-lookup"><span data-stu-id="4f777-128">America Online requires that your Edge Server certificate assigned to the Access Edge service has a client enhanced key usage (EKU).</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="4f777-129">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="4f777-129">In This Section</span></span>

  - [<span data-ttu-id="4f777-130">Zertifikats Zusammenfassung – öffentliche Instant Messaging-Konnektivität in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4f777-130">Certificate summary - Public instant messaging connectivity in Lync Server 2013</span></span>](lync-server-2013-certificate-summary-public-instant-messaging-connectivity.md)

  - [<span data-ttu-id="4f777-131">Port Zusammenfassung – öffentliche Instant Messaging-Konnektivität in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4f777-131">Port summary - Public instant messaging connectivity in Lync Server 2013</span></span>](lync-server-2013-port-summary-public-instant-messaging-connectivity.md)

  - <span data-ttu-id="4f777-132">[DNS-Zusammenfassung – öffentliche Instant Messaging-Konnektivität in lync Server 2013](https://technet.microsoft.com/library/jj618375\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="4f777-132">[DNS summary - Public instant messaging connectivity in Lync Server 2013](https://technet.microsoft.com/library/jj618375\(v=ocs.15\))</span></span>

<span data-ttu-id="4f777-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4f777-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

