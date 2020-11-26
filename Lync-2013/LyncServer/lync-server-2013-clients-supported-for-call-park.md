---
title: 'Lync Server 2013: Unterstützte Clients für das Parken von Anrufen'
description: 'Lync Server 2013: für den Parken von Anrufen unterstützte Clients.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Clients supported for Call Park
ms:assetid: c236d2ba-9d83-418c-9cbc-92541f115fb0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412958(v=OCS.15)
ms:contentKeyID: 48185320
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a923f0e62c246a12b811628d578ab571f4f13e36
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434781"
---
# <a name="clients-supported-for-call-park-in-lync-server-2013"></a><span data-ttu-id="6cfa3-103">Unterstützte Clients für das Parken von Anrufen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6cfa3-103">Clients supported for Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6cfa3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6cfa3-104">

<span> </span></span></span>

<span data-ttu-id="6cfa3-105">_**Letztes Änderungsdatum des Themas:** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="6cfa3-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<span data-ttu-id="6cfa3-106">In diesem Abschnitt werden die Clients identifiziert, die zum Parken von Anrufen und der Clients verwendet werden können, die zum Abrufen von geparkten Anrufen verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="6cfa3-106">This section identifies the clients that can be used to park calls and the clients that can be used to retrieve parked calls.</span></span>

<div>

## <a name="clients-supported-for-parking-calls"></a><span data-ttu-id="6cfa3-107">Für das Parken von Anrufen unterstützte Clients</span><span class="sxs-lookup"><span data-stu-id="6cfa3-107">Clients Supported for Parking Calls</span></span>

<span data-ttu-id="6cfa3-108">Anrufe von IP-, Nebenstellen-, Festnetz- oder Mobiltelefonen können geparkt werden.</span><span class="sxs-lookup"><span data-stu-id="6cfa3-108">Calls from any IP, private branch exchange (PBX), public switched telephone network (PSTN), or mobile phone can be parked.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6cfa3-p101">Nur Audioanrufe können geparkt werden. Das Parken von Chatnachrichten und Konferenzen ist nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="6cfa3-p101">Only audio calls can be parked. Instant messages and conferences cannot be parked.</span></span>



</div>

<span data-ttu-id="6cfa3-111">Die folgenden Clients können den Anruf Park zum Parken von Anrufen verwenden:</span><span class="sxs-lookup"><span data-stu-id="6cfa3-111">The following clients can use Call Park to park calls:</span></span>

  - <span data-ttu-id="6cfa3-112">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="6cfa3-112">Lync 2013</span></span>

  - <span data-ttu-id="6cfa3-113">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="6cfa3-113">Lync 2010</span></span>

  - <span data-ttu-id="6cfa3-114">Lync 2010 Attendant</span><span class="sxs-lookup"><span data-stu-id="6cfa3-114">Lync 2010 Attendant</span></span>

  - <span data-ttu-id="6cfa3-115">Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="6cfa3-115">Lync Phone Edition</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6cfa3-116">Mobiltelefone können den Anruf Park nicht zum Parken von Anrufen verwenden.</span><span class="sxs-lookup"><span data-stu-id="6cfa3-116">Mobile phones cannot use Call Park to park calls.</span></span>



</div>

</div>

<div>

## <a name="clients-supported-for-retrieving-calls"></a><span data-ttu-id="6cfa3-117">Für das Wiederaufnehmen geparkter Anrufe unterstützte Clients</span><span class="sxs-lookup"><span data-stu-id="6cfa3-117">Clients Supported for Retrieving Calls</span></span>

<span data-ttu-id="6cfa3-p102">Orbitbereiche werden als Blöcke virtueller Durchwahlnummern (Durchwahlnummern, denen kein Benutzer oder Telefon zugewiesen ist) konfiguriert. Wenn Sie Orbits als virtuelle Durchwahlnummern konfigurieren, können Mobil- und Festnetztelefone keine geparkten Anrufe wiederaufnehmen.</span><span class="sxs-lookup"><span data-stu-id="6cfa3-p102">Orbit ranges are configured as blocks of virtual extensions (extensions without an assigned user or phone). When you configure orbits as virtual extensions, mobile phones and PSTN phones cannot retrieve parked calls.</span></span>

<span data-ttu-id="6cfa3-120">Das Wiederaufnehmen geparkter Anrufe durch Partnerbenutzer ist nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="6cfa3-120">Federated users cannot retrieve parked calls.</span></span>

<span data-ttu-id="6cfa3-121">Die folgenden Clients können Anrufe abrufen, die im Park des Anrufs abgestellt sind:</span><span class="sxs-lookup"><span data-stu-id="6cfa3-121">The following clients can retrieve calls that are parked on Call Park:</span></span>

  - <span data-ttu-id="6cfa3-122">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="6cfa3-122">Lync 2013</span></span>

  - <span data-ttu-id="6cfa3-123">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="6cfa3-123">Lync 2010</span></span>

  - <span data-ttu-id="6cfa3-124">Lync 2010 Attendant</span><span class="sxs-lookup"><span data-stu-id="6cfa3-124">Lync 2010 Attendant</span></span>

  - <span data-ttu-id="6cfa3-125">Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="6cfa3-125">Lync Phone Edition</span></span>

  - <span data-ttu-id="6cfa3-126">IP-Telefone in öffentlichen Bereichen</span><span class="sxs-lookup"><span data-stu-id="6cfa3-126">IP common area phones</span></span>

  - <span data-ttu-id="6cfa3-127">Nicht-IP-Telefone, die mit der lync Server 2013-Infrastruktur verbunden sind, einschließlich Telefone im öffentlichen Bereich und Private Branch Exchange (PBX)-Telefone</span><span class="sxs-lookup"><span data-stu-id="6cfa3-127">Non-IP phones that are connected to the Lync Server 2013 infrastructure, including common area phones and private branch exchange (PBX) phones</span></span>

<span data-ttu-id="6cfa3-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6cfa3-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

