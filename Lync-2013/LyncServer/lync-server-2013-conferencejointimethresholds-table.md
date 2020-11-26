---
title: 'Lync Server 2013: ConferenceJoinTimeThresholds-Tabelle'
description: 'Lync Server 2013: ConferenceJoinTimeThresholds-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceJoinTimeThresholds table
ms:assetid: 3944d724-bdd8-4d1c-a2af-933ee8141529
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204809(v=OCS.15)
ms:contentKeyID: 48183855
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5e38c8b99f444e16309882b6a8885d166fdceb9b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434459"
---
# <a name="conferencejointimethresholds-table-in-lync-server-2013"></a><span data-ttu-id="f70de-103">ConferenceJoinTimeThresholds-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f70de-103">ConferenceJoinTimeThresholds table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f70de-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f70de-104">

<span> </span></span></span>

<span data-ttu-id="f70de-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="f70de-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="f70de-106">Die Tabelle "ConferenceJoinTimeThresholds" enthält die Klassifizierungs Grenzen, die vom Zusammenfassungsbericht "Konferenzteilnahme Zeit" verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="f70de-106">The ConferenceJoinTimeThresholds table contains the classification boundaries used by the Conference Join Time Summary Report.</span></span> <span data-ttu-id="f70de-107">Der Bericht "Konferenz Teilzeit-Zusammenfassung" fasst die Zeitspanne zusammen, die der Benutzer für eine erfolgreiche Teilnahme an einer Konferenz benötigt. Diese Zeitwerte werden sowohl als Mittelwert als auch in einer der folgenden Kategorien angezeigt:</span><span class="sxs-lookup"><span data-stu-id="f70de-107">The Conference Join Time Summary Report summarizes the amount time required for users to successfully join a conference; these time values are reported both as an average and in one of the following categories:</span></span>

  - <span data-ttu-id="f70de-108">Weniger als 2 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="f70de-108">Less than 2 seconds.</span></span>

  - <span data-ttu-id="f70de-109">Zwischen 2 Sekunden und 5 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="f70de-109">Between 2 second and 5 seconds.</span></span>

  - <span data-ttu-id="f70de-110">Zwischen 5 Sekunden und 10 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="f70de-110">Between 5 seconds and 10 seconds.</span></span>

  - <span data-ttu-id="f70de-111">Mehr als 10 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="f70de-111">More than 10 seconds.</span></span>

<span data-ttu-id="f70de-112">Die Tabelle ConferenceJoinTimeThresholds enthält die Klassifizierungs Werte 2 Sekunden, 5 Sekunden und 10 Sekunden.</span><span class="sxs-lookup"><span data-stu-id="f70de-112">The ConferenceJoinTimeThresholds table contains the classification values 2 seconds, 5 seconds, and 10 seconds.</span></span>

<span data-ttu-id="f70de-113">Diese Tabelle wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f70de-113">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f70de-114">Spalte</span><span class="sxs-lookup"><span data-stu-id="f70de-114">Column</span></span></th>
<th><span data-ttu-id="f70de-115">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f70de-115">Data Type</span></span></th>
<th><span data-ttu-id="f70de-116">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="f70de-116">Key/Index</span></span></th>
<th><span data-ttu-id="f70de-117">Details</span><span class="sxs-lookup"><span data-stu-id="f70de-117">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f70de-118"><strong>Schwellenwert</strong></span><span class="sxs-lookup"><span data-stu-id="f70de-118"><strong>ThresholdId</strong></span></span></p></td>
<td><p><span data-ttu-id="f70de-119">int</span><span class="sxs-lookup"><span data-stu-id="f70de-119">int</span></span></p></td>
<td><p><span data-ttu-id="f70de-120">Primary</span><span class="sxs-lookup"><span data-stu-id="f70de-120">Primary</span></span></p></td>
<td><p><span data-ttu-id="f70de-121">Eindeutiger Bezeichner für die Klassifizierung.</span><span class="sxs-lookup"><span data-stu-id="f70de-121">Unique identifier for the classification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f70de-122"><strong>ThresholdValue</strong></span><span class="sxs-lookup"><span data-stu-id="f70de-122"><strong>ThresholdValue</strong></span></span></p></td>
<td><p><span data-ttu-id="f70de-123">int</span><span class="sxs-lookup"><span data-stu-id="f70de-123">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f70de-124">Obergrenze für die Klassifizierung.</span><span class="sxs-lookup"><span data-stu-id="f70de-124">Upper limit for the classification.</span></span> <span data-ttu-id="f70de-125">Gültige Werte sind:</span><span class="sxs-lookup"><span data-stu-id="f70de-125">Allowed values are:</span></span></p>
<ol>
<li><p><span data-ttu-id="f70de-126">2</span><span class="sxs-lookup"><span data-stu-id="f70de-126">2</span></span></p></li>
<li><p><span data-ttu-id="f70de-127">5</span><span class="sxs-lookup"><span data-stu-id="f70de-127">5</span></span></p></li>
<li><p><span data-ttu-id="f70de-128">10</span><span class="sxs-lookup"><span data-stu-id="f70de-128">10</span></span></p></li>
</ol></td>
</tr>
</tbody>
</table><span data-ttu-id="f70de-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f70de-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

