---
title: 'Lync Server 2013: Planen der PSTN-Konnektivität'
description: 'Lync Server 2013: Planen der PSTN-Konnektivität'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for PSTN connectivity
ms:assetid: 280f684a-740a-443d-8ecf-574241382a42
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425749(v=OCS.15)
ms:contentKeyID: 48183684
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 45c0df6aa6dc9d9cc8522223056f1834849e6ddb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424436"
---
# <a name="planning-for-pstn-connectivity-in-lync-server-2013"></a><span data-ttu-id="b7596-103">Planen der PSTN-Konnektivität in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7596-103">Planning for PSTN connectivity in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b7596-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b7596-104">

<span> </span></span></span>

<span data-ttu-id="b7596-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="b7596-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="b7596-106">Eine VoIP-Lösung für Unternehmen muss ein- und ausgehende PSTN-Anrufe (Public Switched Telephone Network, Telefonfestnetz) ermöglichen, ohne dass die Dienstqualität (Quality of Service, QoS) in irgendeiner Weise beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="b7596-106">An enterprise-grade VoIP solution must provide for calls to and from the public switched telephone network (PSTN) without any decline in Quality of Service (QoS).</span></span> <span data-ttu-id="b7596-107">Benutzer, die Anrufe tätigen und empfangen, sollten sich der zugrunde liegenden Technologie nicht bewusst sein: ein Anruf zwischen der Enterprise-VoIP-Infrastruktur und dem PSTN sollte aus Sicht des Benutzers wie nur ein weiterer Telefonanruf aussehen.</span><span class="sxs-lookup"><span data-stu-id="b7596-107">Users who place and receive calls should not be aware of the underlying technology: from the user's perspective, a call between the Enterprise Voice infrastructure and the PSTN should seem like just another phone call.</span></span>

<span data-ttu-id="b7596-108">Lync Server 2013 bietet zuverlässige, skalierbare PSTN-Konnektivität mithilfe der folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="b7596-108">Lync Server 2013 provides reliable, scalable PSTN connectivity by using the following options:</span></span>

  - <span data-ttu-id="b7596-109">**SIP-Trunks** mit einem Anbieter von Internettelefoniediensten (Internet Telephony Service Provider, ITSP)</span><span class="sxs-lookup"><span data-stu-id="b7596-109">**SIP trunks** to an Internet telephony service provider (ITSP)</span></span>

  - <span data-ttu-id="b7596-110">**Direkte SIP-Verbindungen** mit einem PSTN-Gateway</span><span class="sxs-lookup"><span data-stu-id="b7596-110">**Direct SIP connections** to a PSTN gateway</span></span>

  - <span data-ttu-id="b7596-111">**Direkte SIP-Verbindungen** mit einer Nebenstellenanlage</span><span class="sxs-lookup"><span data-stu-id="b7596-111">**Direct SIP connections** to a PBX</span></span>

<span data-ttu-id="b7596-112">Je nach Größe, geographischer Abdeckung und vorhandener VoIP-Infrastruktur können Unternehmen eine, zwei oder sogar alle drei Optionen an verschiedenen Speicherorten verwenden.</span><span class="sxs-lookup"><span data-stu-id="b7596-112">Depending on its size, geographic coverage, and existing voice infrastructure, an enterprise may use one, two, or even all three of these options at various locations.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="b7596-113">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="b7596-113">In This Section</span></span>

  - [<span data-ttu-id="b7596-114">SIP-Trunking in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7596-114">SIP trunking in Lync Server 2013</span></span>](lync-server-2013-sip-trunking.md)

  - [<span data-ttu-id="b7596-115">Direkte SIP-Verbindungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7596-115">Direct SIP connections in Lync Server 2013</span></span>](lync-server-2013-direct-sip-connections.md)

  - [<span data-ttu-id="b7596-116">M:N trunk in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7596-116">M:N trunk in Lync Server 2013</span></span>](lync-server-2013-m-n-trunk.md)

  - [<span data-ttu-id="b7596-117">Übersetzungsregeln in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7596-117">Translation rules in Lync Server 2013</span></span>](lync-server-2013-translation-rules.md)

  - [<span data-ttu-id="b7596-118">Planen des VoIP-Routings für ausgehende Anrufe in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7596-118">Planning outbound voice routing in Lync Server 2013</span></span>](lync-server-2013-planning-outbound-voice-routing.md)

<span data-ttu-id="b7596-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b7596-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

