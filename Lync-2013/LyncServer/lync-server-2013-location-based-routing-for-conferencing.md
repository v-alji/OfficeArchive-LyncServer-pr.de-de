---
title: 'Lync Server 2013: Location-Based Routing für Konferenzen'
description: 'Lync Server 2013: Location-Based Routing für Konferenzen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Location-Based Routing for conferencing
ms:assetid: e1acb1ba-0ed2-4abf-8a7b-1ca3049e95e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362849(v=OCS.15)
ms:contentKeyID: 56335087
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 979c835e03bbf87c9a9bf86b030cb9a8f4e138e0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426543"
---
# <a name="location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="65005-103">Location-Based Routing für Konferenzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65005-103">Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="65005-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="65005-104">

<span> </span></span></span>

<span data-ttu-id="65005-105">_**Letztes Änderungsdatum des Themas:** 2013-07-31_</span><span class="sxs-lookup"><span data-stu-id="65005-105">_**Topic Last Modified:** 2013-07-31_</span></span>

<span data-ttu-id="65005-106">Location-Based Routing ermöglicht es, das Routing von anrufen zwischen VoIP-Endpunkten und PSTN-Endpunkten basierend auf dem Standort der Gesprächspartner zu beschränken.</span><span class="sxs-lookup"><span data-stu-id="65005-106">Location-Based Routing makes it possible to restrict the routing of calls between VoIP endpoints and PSTN endpoints based on the location of the parties in the call.</span></span> <span data-ttu-id="65005-107">Mit dem kumulativen Update 2 von lync Server 2013 können Location-Based Routing Regeln in lync-Besprechungen (also Konferenzen) erzwungen werden, um eine PSTN-Maut Umgehung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="65005-107">With Cumulative Update 2 of Lync Server 2013, Location-Based Routing rules can be enforced on Lync meetings (i.e. conferences) to prevent PSTN toll bypass.</span></span> <span data-ttu-id="65005-108">Die Anwendung überwacht eine aktive Konferenz und erzwingt Location-Based Routing Einschränkungen basierend auf dem Standort der teilnehmenden Benutzer.</span><span class="sxs-lookup"><span data-stu-id="65005-108">The application monitors an active conference and enforces Location-Based Routing restrictions based on the location of users participating.</span></span> <span data-ttu-id="65005-109">Die Location-Based Routing Konferenz Anwendung ermöglicht darüber hinaus die Erzwingung von Location-Based Routing Einschränkungen für beratende Übertragungen, die PSTN-Endpunkte umfassen.</span><span class="sxs-lookup"><span data-stu-id="65005-109">The Location-Based Routing Conferencing application additionally enables the enforcement of Location-Based Routing restrictions to consultative transfers involving PSTN endpoints.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="65005-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="65005-110">In This Section</span></span>

  - [<span data-ttu-id="65005-111">Übersicht über Location-Based Routing für Konferenzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65005-111">Overview of Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-overview-of-location-based-routing-for-conferencing.md)

  - [<span data-ttu-id="65005-112">Übertragungen von standortbasierten Routing-und beratenden anrufen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65005-112">Location-Based Routing and consultative call transfers in Lync Server 2013</span></span>](lync-server-2013-location-based-routing-and-consultative-call-transfers.md)

  - [<span data-ttu-id="65005-113">Voraussetzungen für Location-Based Routing für Konferenzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65005-113">Requirements for Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-requirements-for-location-based-routing-for-conferencing.md)

  - [<span data-ttu-id="65005-114">Konfiguration von standortbasiertem Routing für Konferenzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65005-114">Configuration of Location-Based Routing for conferencing in Lync Server 2013</span></span>](lync-server-2013-configuration-of-location-based-routing-for-conferencing.md)

<span data-ttu-id="65005-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="65005-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

