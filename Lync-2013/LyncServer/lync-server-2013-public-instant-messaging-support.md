---
title: 'Lync Server 2013: Unterstützung von Funktionen für öffentlichen Chat'
description: 'Lync Server 2013: Unterstützung für öffentliche Sofortnachrichten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Public instant messaging support
ms:assetid: 1f45163b-52c6-4a78-b9c8-dfe3abe4e5eb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204732(v=OCS.15)
ms:contentKeyID: 48183582
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e071e8b79be82d865a85a9488e48dd0a4264c7f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394579"
---
# <a name="public-instant-messaging-support-in-lync-server-2013"></a><span data-ttu-id="8e953-103">Unterstützung von Funktionen für öffentlichen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8e953-103">Public instant messaging support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8e953-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8e953-104">

<span> </span></span></span>

<span data-ttu-id="8e953-105">_**Letztes Änderungsdatum des Themas:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="8e953-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="8e953-106">Lync Server 2013 unterstützt die Verwendung von lizenzierten öffentlichen Instant Messaging (im)-Verbindungs Anbietern sowie die Verwendung von Extensible Messaging and Presence Protocol (XMPP) zur Implementierung eines speziellen Föderations Typs, der einem lync-Server den Zugriff auf konfigurierte XMPP-Domänen Partner mithilfe des lync 2013-Clients ermöglicht.</span><span class="sxs-lookup"><span data-stu-id="8e953-106">Lync Server 2013 supports the use of licensed public instant messaging (IM) connectivity providers, as well as the use of eXtensible Messaging and Presence Protocol (XMPP) to implement a special type of federation that enables a Lync Server to access configured XMPP domain partners by using the Lync 2013 client.</span></span>

<div>

## <a name="public-im-connectivity-provider-support"></a><span data-ttu-id="8e953-107">Unterstützung für öffentliche Chat-Konnektivitäts-Anbieter</span><span class="sxs-lookup"><span data-stu-id="8e953-107">Public IM Connectivity Provider Support</span></span>

<span data-ttu-id="8e953-108">Die derzeit unterstützten öffentlichen Instant Messaging-Verbindungspartner sind:</span><span class="sxs-lookup"><span data-stu-id="8e953-108">The currently supported public instant messaging connectivity partners are:</span></span>

  - <span data-ttu-id="8e953-109">America Online</span><span class="sxs-lookup"><span data-stu-id="8e953-109">America Online</span></span>

  - <span data-ttu-id="8e953-110">Windows Live</span><span class="sxs-lookup"><span data-stu-id="8e953-110">Windows Live</span></span>

  - <span data-ttu-id="8e953-111">Yahoo\!</span><span class="sxs-lookup"><span data-stu-id="8e953-111">Yahoo\!</span></span>

<span data-ttu-id="8e953-112">Für die Kommunikation mit Windows Live-Benutzern unterstützt lync Server 2013 Peer-to-Peer-Chats sowie Audio-und Videoanrufe.</span><span class="sxs-lookup"><span data-stu-id="8e953-112">For communications with Windows Live users, Lync Server 2013 supports peer-to-peer IM and audio and video calls.</span></span> <span data-ttu-id="8e953-113">Für die Kommunikation mit AOL und Yahoo \! unterstützt lync Server 2013 Peer-to-Peer-Chats.</span><span class="sxs-lookup"><span data-stu-id="8e953-113">For communications with AOL and Yahoo\!, Lync Server 2013 supports peer-to-peer IM.</span></span> <span data-ttu-id="8e953-114">Möglicherweise ist eine separate Lizenz erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8e953-114">A separate license may be required.</span></span>

<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="8e953-115">Ab dem 1. September, 2012, ist die Microsoft lync Public im Connectivity-Benutzerabonnementlizenz ("PIC USL") nicht mehr für den Kauf von neuen oder erneuernden Vereinbarungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="8e953-115">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="8e953-116">Kunden mit aktiven Lizenzen sind in der Lage, weiterhin mit Yahoo! zu verbünden</span><span class="sxs-lookup"><span data-stu-id="8e953-116">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="8e953-117">Messenger, bis der Dienst das Datum beendet hat.</span><span class="sxs-lookup"><span data-stu-id="8e953-117">Messenger until the service shut down date.</span></span> <span data-ttu-id="8e953-118">Datum des Endes des Lebenszyklus von Juni 2014 für AOL und Yahoo!</span><span class="sxs-lookup"><span data-stu-id="8e953-118">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="8e953-119">wurde angekündigt.</span><span class="sxs-lookup"><span data-stu-id="8e953-119">has been announced.</span></span> <span data-ttu-id="8e953-120">Ausführliche Informationen finden Sie <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">unter Unterstützung für öffentliche Instant Messenger-Konnektivität in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="8e953-120">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="8e953-121">Bei der PIC-USL handelt es sich um eine Abonnementlizenz pro Benutzer pro Monat, die für die Föderation von lync Server oder Office Communications Server mit Yahoo! erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="8e953-121">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="8e953-122">Messenger.</span><span class="sxs-lookup"><span data-stu-id="8e953-122">Messenger.</span></span> <span data-ttu-id="8e953-123">Die Möglichkeit von Microsoft, diesen Dienst bereitzustellen, war von der Unterstützung durch Yahoo! abhängig, deren zugrunde liegende Vereinbarung abgewickelt wird.</span><span class="sxs-lookup"><span data-stu-id="8e953-123">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
> <LI>
> <P><span data-ttu-id="8e953-124">Lync ist mehr denn je ein leistungsfähiges Tool für die Verbindung zwischen Organisationen und Personen in der ganzen Welt.</span><span class="sxs-lookup"><span data-stu-id="8e953-124">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="8e953-125">Für den Verbund mit Windows Live Messenger sind keine zusätzlichen Benutzer-und Gerätelizenzen außerhalb der lync-Standard CAL erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8e953-125">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="8e953-126">Skype Federation wird dieser Liste hinzugefügt und ermöglicht es lync-Benutzern, Hunderte von Millionen von Personen mit Chat und Sprache zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="8e953-126">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>



</div>

</div>

<div>

## <a name="xmpp-federation-support"></a><span data-ttu-id="8e953-127">Unterstützung für XMPP-Föderation</span><span class="sxs-lookup"><span data-stu-id="8e953-127">XMPP Federation Support</span></span>

<span data-ttu-id="8e953-128">Die XMPP-Föderation unterstützt die Kommunikation von lync-Benutzern mit konfigurierten XMPP-Domänenbenutzern, die einen öffentlichen Anbieter wie GTalk verwenden.</span><span class="sxs-lookup"><span data-stu-id="8e953-128">XMPP federation supports Lync users communication with configured XMPP domain users who use a public provider, such as GTalk.</span></span> <span data-ttu-id="8e953-129">Die Kommunikation mit diesen Benutzern kann Folgendes umfassen:</span><span class="sxs-lookup"><span data-stu-id="8e953-129">Communications with these users can include the following:</span></span>

  - <span data-ttu-id="8e953-130">Peer-zu-Peer-Chat und Anwesenheit</span><span class="sxs-lookup"><span data-stu-id="8e953-130">Peer-to-peer IM and presence</span></span>

  - <span data-ttu-id="8e953-131">Erstellen von XMPP-verbundkontakten im lync-Client</span><span class="sxs-lookup"><span data-stu-id="8e953-131">Creation of XMPP federated contacts in the Lync client</span></span>

<span data-ttu-id="8e953-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8e953-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

