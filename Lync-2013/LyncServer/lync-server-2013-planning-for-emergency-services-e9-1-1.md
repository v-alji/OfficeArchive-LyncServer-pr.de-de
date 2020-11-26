---
title: 'Lync Server 2013: Planen von Notrufdiensten (E9-1-1)'
description: 'Lync Server 2013: Planen von Notfalldiensten (E9-1-1).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for emergency services (E9-1-1)
ms:assetid: 0a76f97b-474a-4bc1-8cd3-28c7e2bb57b9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398154(v=OCS.15)
ms:contentKeyID: 48183363
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba4113b2355db0b1aade0ab6766e8ba7a5972aee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424604"
---
# <a name="planning-for-emergency-services-e9-1-1-in-lync-server-2013"></a><span data-ttu-id="6b9e5-103">Planen von Notrufdiensten (E9-1-1) in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6b9e5-103">Planning for emergency services (E9-1-1) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6b9e5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6b9e5-104">

<span> </span></span></span>

<span data-ttu-id="6b9e5-105">_**Letztes Änderungsdatum des Themas:** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="6b9e5-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="6b9e5-106">Lync Server 2013 unterstützt erweiterte 9-1-1 (E9-1-1)-Dienste in den Vereinigten Staaten als Teil einer Enterprise-VoIP-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="6b9e5-106">Lync Server 2013 supports Enhanced 9-1-1 (E9-1-1) services within the United States as part of an Enterprise Voice deployment.</span></span> <span data-ttu-id="6b9e5-107">E9-1-1 ist ein Notfall-Dispatch-Feature, das einen 9-1-1-Anruf mit einem Emergency Response Location (ERL) verknüpft, der aus bürgerlichen (also Straßen-) Adressen und anderen spezifischeren Standortinformationen wie Floor-Nummern für Anrufe aus Bürogebäuden und anderen Multitenant-Einrichtungen besteht.</span><span class="sxs-lookup"><span data-stu-id="6b9e5-107">E9-1-1 is an emergency dispatch feature that associates a 9-1-1 call with an Emergency Response Location (ERL) that consists of civic (that is, street) addresses and other more specific location information, such as floor numbers, for calls from office buildings and other multitenant facilities.</span></span> <span data-ttu-id="6b9e5-108">Durch Verwendung des bereitgestellten Erl kann ein öffentlicher Sicherheits Beantwortungs Punkt (PSAP) sofort Antworten an den Anrufer in Seenot senden, wobei das Risiko verringert wird, dass der Responder versehentlich an eine falsche oder mehrdeutige Position geleitet wird.</span><span class="sxs-lookup"><span data-stu-id="6b9e5-108">By using the provided ERL, a Public Safety Answering Point (PSAP) can immediately dispatch first responders to the caller in distress with reduced risk of inadvertently directing the responder to an incorrect or ambiguous location.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6b9e5-109">Lync Server verfügt über drei erweiterte Enterprise-VoIP-Features: Anrufsteuerung, Notfalldienste (E9-1-1) und medienumgehung.</span><span class="sxs-lookup"><span data-stu-id="6b9e5-109">Lync Server has three advanced Enterprise Voice features: call admission control, emergency services (E9-1-1), and media bypass.</span></span> <span data-ttu-id="6b9e5-110">Eine Übersicht über die Planungsinformationen, die für alle drei Features üblich sind, finden Sie unter <A href="lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md">Netzwerkeinstellungen für die erweiterten Enterprise-VoIP-Features in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="6b9e5-110">For an overview of planning information that is common to all three of these features, see <A href="lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md">Network settings for the advanced Enterprise Voice features in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6b9e5-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6b9e5-111">In This Section</span></span>

  - [<span data-ttu-id="6b9e5-112">Übersicht über E9-1-1 in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6b9e5-112">Overview of E9-1-1 in Lync Server 2013</span></span>](lync-server-2013-overview-of-e9-1-1.md)

  - [<span data-ttu-id="6b9e5-113">Definieren der Anforderungen für Notrufe in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6b9e5-113">Defining your requirements for emergency calls in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-emergency-calls.md)

  - [<span data-ttu-id="6b9e5-114">Bereitstellungscheckliste für E9-1-1 in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6b9e5-114">Deployment checklist for E9-1-1 in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-e9-1-1.md)

<span data-ttu-id="6b9e5-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6b9e5-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

