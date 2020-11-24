---
title: 'Lync Server 2013: PurgeSettings-Tabelle (QoE)'
description: 'Lync Server 2013: PurgeSettings-Tabelle (QoE)'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PurgeSettings table (QoE)
ms:assetid: 31b85d1c-3f32-4f67-94bf-9389cdd282c5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204788(v=OCS.15)
ms:contentKeyID: 48183777
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d515d799a7cc442dc6d34f2ece1a968de51cdad6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394538"
---
# <a name="purgesettings-table-qoe-in-lync-server-2013"></a><span data-ttu-id="5311d-103">PurgeSettings-Tabelle (QoE) in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5311d-103">PurgeSettings table (QoE) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5311d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5311d-104">

<span> </span></span></span>

<span data-ttu-id="5311d-105">_**Letztes Änderungsdatum des Themas:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="5311d-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="5311d-106">Die PurgeSettings-Tabelle enthält Informationen, die angeben, ob (und wann) veraltete Quality of Experience-Datensätze automatisch aus der QoE-Datenbank gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="5311d-106">The PurgeSettings table contains information that specifies if (and when) outdated Quality of Experience records will automatically be deleted from the QoE database.</span></span> <span data-ttu-id="5311d-107">Beachten Sie, dass Bereinigungs bezogene Informationen auch in der Microsoft lync Server 2013-Verwaltungsshell abgerufen werden können, indem Sie den folgenden Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="5311d-107">Note that purging-related information can also be obtained from within the Microsoft Lync Server 2013 Management Shell by running the following command:</span></span>

    Get-CsQoEConfiguration

<span data-ttu-id="5311d-108">Diese Tabelle wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5311d-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5311d-109"><strong>Spalte</strong></span><span class="sxs-lookup"><span data-stu-id="5311d-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="5311d-110"><strong>Datentyp</strong></span><span class="sxs-lookup"><span data-stu-id="5311d-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="5311d-111"><strong>Schlüssel/Index</strong></span><span class="sxs-lookup"><span data-stu-id="5311d-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="5311d-112"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="5311d-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5311d-113"><strong>ID</strong></span><span class="sxs-lookup"><span data-stu-id="5311d-113"><strong>ID</strong></span></span></p></td>
<td><p><span data-ttu-id="5311d-114">int</span><span class="sxs-lookup"><span data-stu-id="5311d-114">int</span></span></p></td>
<td><p><span data-ttu-id="5311d-115">Primary</span><span class="sxs-lookup"><span data-stu-id="5311d-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="5311d-116">Eindeutiger Bezeichner für die Sammlung von QoE-Bereinigungseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="5311d-116">Unique identifier for the collection of QoE purge settings.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5311d-117"><strong>EnablePurge</strong></span><span class="sxs-lookup"><span data-stu-id="5311d-117"><strong>EnablePurge</strong></span></span></p></td>
<td><p><span data-ttu-id="5311d-118">bit</span><span class="sxs-lookup"><span data-stu-id="5311d-118">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5311d-119">Bei Festlegung auf true (1) bereinigen Microsoft lync Server 2013 in regelmäßigen Abständen veraltete Datensätze aus der QoE-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="5311d-119">When set to True (1) Microsoft Lync Server 2013 will periodically purge outdated records from the QoE database.</span></span> <span data-ttu-id="5311d-120">Das Bereinigen erfolgt täglich im Wälzer, der durch die Einstellung PurgeHour angegeben wird.</span><span class="sxs-lookup"><span data-stu-id="5311d-120">Purging will take place each day at the tome specified by the PurgeHour setting.</span></span> <span data-ttu-id="5311d-121">Bei Festlegung auf "false" (0) werden Datensätze nicht automatisch aus der Datenbank bereinigt.</span><span class="sxs-lookup"><span data-stu-id="5311d-121">If set to False (0) then records will not be automatically purged from the database.</span></span> <span data-ttu-id="5311d-122">Der Standardwert lautet „True“.</span><span class="sxs-lookup"><span data-stu-id="5311d-122">The default value is True.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5311d-123"><strong>KeepQoEDataForDays</strong></span><span class="sxs-lookup"><span data-stu-id="5311d-123"><strong>KeepQoEDataForDays</strong></span></span></p></td>
<td><p><span data-ttu-id="5311d-124">int</span><span class="sxs-lookup"><span data-stu-id="5311d-124">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5311d-125">Gibt das Alter von QoE-Datensätzen (in Tagen) an, die aus der Datenbank gelöscht werden: Wenn die Bereinigung aktiviert ist, werden QoE-Datensätze, die älter als dieser Wert sind, aus der Datenbank entfernt.</span><span class="sxs-lookup"><span data-stu-id="5311d-125">Specifies the age of QoE records (in days) that will be purged from the database: if purging is enabled, QoE records older than this value will be removed from the database.</span></span> <span data-ttu-id="5311d-126">Der Standardwert ist 60 Tage.</span><span class="sxs-lookup"><span data-stu-id="5311d-126">The default value is 60 days.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5311d-127"><strong>PurgeHour</strong></span><span class="sxs-lookup"><span data-stu-id="5311d-127"><strong>PurgeHour</strong></span></span></p></td>
<td><p><span data-ttu-id="5311d-128">int</span><span class="sxs-lookup"><span data-stu-id="5311d-128">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5311d-129">Gibt die lokale Tageszeit an, zu der eine Datenbankbereinigung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5311d-129">Specifies the local time of day when database purging will take place.</span></span> <span data-ttu-id="5311d-130">Die Uhrzeit wird im 24-Stunden-Format angegeben, wobei Mitternacht (12:00 AM) durch 0 und 11:00 PM durch 23 dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5311d-130">The time of day is specified using a 24-hour clock, with 0 representing midnight (12:00 AM) and 23 representing 11:00 PM.</span></span> <span data-ttu-id="5311d-131">Beachten Sie, dass Sie nur die Stunde des Tages angeben können: der Wert 10 (mit der Angabe von 10:00 Uhr) ist zulässig, aber der Wert 10:30 von 10,5 (mit der Angabe 10:30 Uhr) ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="5311d-131">Note that you can only specify the hour of the day: a value of 10 (indicating 10:00 AM) is allowed, but a value of 10:30 of 10.5 (indicating 10:30 AM) is not allowed.</span></span> <span data-ttu-id="5311d-132">Der Standardwert ist 1 (1:00 am).</span><span class="sxs-lookup"><span data-stu-id="5311d-132">The default value is 1 (1:00 AM).</span></span> <span data-ttu-id="5311d-133">Gibt die lokale Tageszeit an, zu der eine Datenbankbereinigung durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="5311d-133">Specifies the local time of day when database purging will take place.</span></span> <span data-ttu-id="5311d-134">Die Uhrzeit wird im 24-Stunden-Format angegeben, wobei Mitternacht (12:00 AM) durch 0 und 11:00 PM durch 23 dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="5311d-134">The time of day is specified using a 24-hour clock, with 0 representing midnight (12:00 AM) and 23 representing 11:00 PM.</span></span> <span data-ttu-id="5311d-135">Beachten Sie, dass Sie nur die Stunde des Tages angeben können: der Wert 10 (mit der Angabe von 10:00 Uhr) ist zulässig, aber der Wert 10:30 von 10,5 (mit der Angabe 10:30 Uhr) ist nicht zulässig.</span><span class="sxs-lookup"><span data-stu-id="5311d-135">Note that you can only specify the hour of the day: a value of 10 (indicating 10:00 AM) is allowed, but a value of 10:30 of 10.5 (indicating 10:30 AM) is not allowed.</span></span> <span data-ttu-id="5311d-136">Der Standardwert ist 1 (1:00 am).</span><span class="sxs-lookup"><span data-stu-id="5311d-136">The default value is 1 (1:00 AM).</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="5311d-137">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5311d-137">


</div>

<span> </span>

</div>

</div>

</span></span></div>

