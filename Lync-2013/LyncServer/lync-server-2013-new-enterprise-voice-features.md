---
title: 'Lync Server 2013: Neue Enterprise-VoIP-Funktionen'
description: 'Lync Server 2013: neue Enterprise-VoIP-Features.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New Enterprise Voice features
ms:assetid: db0ad7b9-e469-4c29-89d9-52fed018ef08
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398964(v=OCS.15)
ms:contentKeyID: 48185591
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1fc0c0970fe22fb6a56eaf0d950f1d49d210826
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445421"
---
# <a name="new-enterprise-voice-features-in-lync-server-2013"></a><span data-ttu-id="53f44-103">Neue Enterprise-VoIP-Funktionen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="53f44-103">New Enterprise Voice features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="53f44-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="53f44-104">

<span> </span></span></span>

<span data-ttu-id="53f44-105">_**Letztes Änderungsdatum des Themas:** 2013-05-01_</span><span class="sxs-lookup"><span data-stu-id="53f44-105">_**Topic Last Modified:** 2013-05-01_</span></span>

<span data-ttu-id="53f44-106">Lync Server 2013 führt verschiedene neue Routing-und Anruf Verwaltungsfeatures ein, die Enterprise-VoIP verbessern.</span><span class="sxs-lookup"><span data-stu-id="53f44-106">Lync Server 2013 introduces several new routing and call management features that enhance Enterprise Voice.</span></span>

<span data-ttu-id="53f44-107">Lync Server 2013 unterstützt mehrere Trunks zwischen Vermittlungsservern und Gateways.</span><span class="sxs-lookup"><span data-stu-id="53f44-107">Lync Server 2013 supports multiple trunks between Mediation Servers and gateways.</span></span> <span data-ttu-id="53f44-108">Ein *trunk* ist eine logische Zuordnung zwischen einer Portnummer und einem Vermittlungs Server mit einer Portnummer und einem Gateway.</span><span class="sxs-lookup"><span data-stu-id="53f44-108">A *trunk* is a logical association between a port number and Mediation Server with a port number and gateway.</span></span> <span data-ttu-id="53f44-109">Dies bedeutet, dass ein Vermittlungs Server mehrere Trunks für verschiedene Gateways aufweisen kann und ein Gateway mehrere Trunks zu verschiedenen Vermittlungsservern haben kann.</span><span class="sxs-lookup"><span data-stu-id="53f44-109">This means that a Mediation Server can have multiple trunks to different gateways, and a gateway can have multiple trunks to different Mediation Servers.</span></span> <span data-ttu-id="53f44-110">Das intertrunk-Routing ermöglicht es lync Server 2013, eine IP-Telefonanlage mit einem PSTN-Gateway (Public Switched Telephone Network) zu verbinden oder mehrere IP-PBX-Systeme miteinander zu verbinden.</span><span class="sxs-lookup"><span data-stu-id="53f44-110">Intertrunk routing makes it possible for Lync Server 2013 to interconnect an IP-PBX to a public switched telephone network (PSTN) gateway or to interconnect multiple IP-PBX systems.</span></span> <span data-ttu-id="53f44-111">Lync Server 2013 dient als Klebstoff (also die Verbindung) zwischen verschiedenen Telefonsystemen.</span><span class="sxs-lookup"><span data-stu-id="53f44-111">Lync Server 2013 serves as the glue (that is, the interconnection) between different telephony systems.</span></span>

<span data-ttu-id="53f44-112">Microsoft lync Server 2013 führt zu Verbesserungen in den Bereichen Anrufweiterleitung, gleichzeitiges Klingeln, Voicemail-Behandlung und Präsentation der Rufnummernanzeige.</span><span class="sxs-lookup"><span data-stu-id="53f44-112">Microsoft Lync Server 2013 makes improvements in the areas of call forwarding, simultaneous ringing, voice mail handling, and caller ID presentation.</span></span> <span data-ttu-id="53f44-113">Diese Features bereichern das Sprachanruf Erlebnis in Unternehmen.</span><span class="sxs-lookup"><span data-stu-id="53f44-113">These features enrich the Enterprise Voice call experience.</span></span>

<span data-ttu-id="53f44-114">Lync Server 2013 führt die folgenden neuen Verbesserungen für Enterprise-VoIP ein:</span><span class="sxs-lookup"><span data-stu-id="53f44-114">Lync Server 2013 introduces the following new enhancements to Enterprise Voice:</span></span>

  - [<span data-ttu-id="53f44-115">Neue Anruffunktionen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="53f44-115">New call features in Lync Server 2013</span></span>](lync-server-2013-new-call-features.md)

  - [<span data-ttu-id="53f44-116">Neue Funktion für die Anrufer-ID in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="53f44-116">New caller ID feature in Lync Server 2013</span></span>](lync-server-2013-new-caller-id-feature.md)

  - [<span data-ttu-id="53f44-117">Neue Voicemailfunktion in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="53f44-117">New voice mail feature in Lync Server 2013</span></span>](lync-server-2013-new-voice-mail-feature.md)

  - [<span data-ttu-id="53f44-118">Neue Trunkfunktion in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="53f44-118">New trunk feature in Lync Server 2013</span></span>](lync-server-2013-new-trunk-feature.md)

  - [<span data-ttu-id="53f44-119">Neue Funktion für das Routing zwischen Trunks in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="53f44-119">New intertrunk feature in Lync Server 2013</span></span>](lync-server-2013-new-intertrunk-feature.md)

  - [<span data-ttu-id="53f44-120">Neue Funktionen für die Anrufverwaltung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="53f44-120">New call management features in Lync Server 2013</span></span>](lync-server-2013-new-call-management-features.md)

<span data-ttu-id="53f44-121"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="53f44-121"></div>

<span> </span>

</div>

</div>

</span></span></div>

