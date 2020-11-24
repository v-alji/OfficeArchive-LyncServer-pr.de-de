---
title: 'Lync Server 2013: Konfigurieren von Gruppennummern für die Anruf Abholung'
description: 'Lync Server 2013: Konfigurieren von Gruppennummern für die Anruf Abholung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure call pickup group numbers
ms:assetid: 5cc67f0b-d70d-446a-8db1-befda8671121
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945631(v=OCS.15)
ms:contentKeyID: 51541479
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ddffae2e385ce6c3fd7a700a9b94a89b1b6679f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393834"
---
# <a name="configure-call-pickup-group-numbers-in-lync-server-2013"></a><span data-ttu-id="3af1d-103">Konfigurieren von Gruppennummern für die Anruf Abholung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3af1d-103">Configure call pickup group numbers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3af1d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3af1d-104">

<span> </span></span></span>

<span data-ttu-id="3af1d-105">_**Letztes Änderungsdatum des Themas:** 2013-01-30_</span><span class="sxs-lookup"><span data-stu-id="3af1d-105">_**Topic Last Modified:** 2013-01-30_</span></span>

<span data-ttu-id="3af1d-106">Die Abholung von Gruppen anrufen basiert auf der Anwendung "Parken".</span><span class="sxs-lookup"><span data-stu-id="3af1d-106">Group Call Pickup is based on the Call Park application.</span></span> <span data-ttu-id="3af1d-107">Wenn Sie die Gruppenanruf Abholung bereitstellen, konfigurieren Sie die Orbit-Tabelle des Anruf Parks mit Bereichen von Telefonnummern, die als Gruppennummern für die Anruf Abholung festgelegt sind.</span><span class="sxs-lookup"><span data-stu-id="3af1d-107">When you deploy Group Call Pickup, you configure the call park orbit table with ranges of phone numbers that are designated as call pickup group numbers.</span></span> <span data-ttu-id="3af1d-108">Bei diesen Gruppennummern handelt es sich um Nummern, die Benutzer wählen, um Anrufe anzunehmen, die an einen Benutzer eingehen.</span><span class="sxs-lookup"><span data-stu-id="3af1d-108">These group numbers are the numbers that users dial to pick up calls that are ringing for another user.</span></span>

<span data-ttu-id="3af1d-109">Wie bei Orbitnummern zum Parken von Anrufen muss es sich auch bei Nummern für die Gruppenanrufannahme um virtuelle Durchwahlen handeln, denen kein Benutzer oder Telefon zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="3af1d-109">Like call park orbit numbers, call pickup group numbers need to be virtual extensions that have no user or phone assigned to them.</span></span> <span data-ttu-id="3af1d-110">Jeder Front-End-Pool, in dem Sie die Gruppenanruf Abholung bereitstellen, kann über einen oder mehrere Bereiche der Gruppennummern für die Anruf Abholung verfügen.</span><span class="sxs-lookup"><span data-stu-id="3af1d-110">Each Front End pool where you deploy Group Call Pickup can have one or more ranges of call pickup group numbers.</span></span> <span data-ttu-id="3af1d-111">Die Gruppennummern Bereiche müssen in der lync Server-Bereitstellung global eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="3af1d-111">The group number ranges must be globally unique across the Lync Server deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="3af1d-112">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="3af1d-112">In This Section</span></span>

[<span data-ttu-id="3af1d-113">Create or modify a Group Call Pickup number range in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3af1d-113">Create or modify a Group Call Pickup number range in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-group-call-pickup-number-range.md)

<span data-ttu-id="3af1d-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3af1d-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

