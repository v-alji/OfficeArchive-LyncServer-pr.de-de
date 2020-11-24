---
title: 'Lync Server 2013: Überwachen der Back-End-Speicherleistung von lync Server'
description: 'Lync Server 2013: Überwachen der Back-End-Speicherleistung von lync Server'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring back end Lync Server 2013 storage performance
ms:assetid: 71627c70-1953-4ac2-afbe-f3ad85be0f44
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720917(v=OCS.15)
ms:contentKeyID: 63969619
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7501418d3589b941b7e92d2b414492c1d27a3ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394171"
---
# <a name="monitoring-back-end-lync-server-2013-storage-performance"></a><span data-ttu-id="48c30-103">Überwachen der Back-End-Speicherleistung von lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="48c30-103">Monitoring back end Lync Server 2013 storage performance</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="48c30-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="48c30-104">

<span> </span></span></span>

<span data-ttu-id="48c30-105">_**Letztes Änderungsdatum des Themas:** 2014-05-02_</span><span class="sxs-lookup"><span data-stu-id="48c30-105">_**Topic Last Modified:** 2014-05-02_</span></span>

<span data-ttu-id="48c30-106">Die lync Server 2013-Back-End-Datenbanken sind ein sehr wichtiger Bestandteil der lync Server 2013-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="48c30-106">The Lync Server 2013 back-end databases are a very important part of the Lync Server 2013 deployment.</span></span> <span data-ttu-id="48c30-107">Wir empfehlen, die Datenbanken und die jeweiligen Transaktionsprotokolle ständig zu überwachen, um sicherzustellen, dass das lync Server 2013-Back-End optimal ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="48c30-107">We recommend constantly monitoring the databases and respective transaction logs to help to make sure that the Lync Server 2013 back end is performing optimally.</span></span>

<span data-ttu-id="48c30-108">In der folgenden Tabelle sind Leistungsindikatoren aufgeführt, die überwacht werden sollten, um Informationen zur Speicherleistung zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="48c30-108">The following table identifies performance counters that should be monitored to learn information about Storage Performance.</span></span> <span data-ttu-id="48c30-109">Die Baselinewerte für diese Leistungsindikatoren müssen zuerst bestimmt werden (wenn das System die normale, erwartete Auslastung hat), um die Leistungsänderungen zu verstehen, wenn System beansprucht wird.</span><span class="sxs-lookup"><span data-stu-id="48c30-109">The baseline values for these counters must be determined first (when system is at its normal, expected load) to understand the performance changes when system is stressed.</span></span>

### <a name="performance-counters-to-be-monitored"></a><span data-ttu-id="48c30-110">Zu überwachenden Leistungsindikatoren</span><span class="sxs-lookup"><span data-stu-id="48c30-110">Performance counters to be monitored</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="48c30-111">Leistungsindikator</span><span class="sxs-lookup"><span data-stu-id="48c30-111">Performance Counter</span></span></th>
<th><span data-ttu-id="48c30-112">Baseline-Schwellenwerte</span><span class="sxs-lookup"><span data-stu-id="48c30-112">Baseline thresholds</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="48c30-113">Transaktionen/SEK (RTC)</span><span class="sxs-lookup"><span data-stu-id="48c30-113">Transactions/sec (RTC)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48c30-114">Transaktionen/SEK (RTCDyn)</span><span class="sxs-lookup"><span data-stu-id="48c30-114">Transactions/sec (rtcdyn)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48c30-115">Transaktionen/SEK (tempdb)</span><span class="sxs-lookup"><span data-stu-id="48c30-115">Transactions/sec (tempdb)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48c30-116">Protokollleerungen/SEK (RTC)</span><span class="sxs-lookup"><span data-stu-id="48c30-116">Log Flushes/sec (RTC)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48c30-117">Protokollleerungen/Sek. (RTCDyn)</span><span class="sxs-lookup"><span data-stu-id="48c30-117">Log Flushes/sec (rtcdyn)</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48c30-118">Protokollleerungen/SEK (tempdb)</span><span class="sxs-lookup"><span data-stu-id="48c30-118">Log Flushes/sec (tempdb)</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48c30-119">Datenträgerübertragungen/SEK (Read + Write)-RTC DB</span><span class="sxs-lookup"><span data-stu-id="48c30-119">Disk Transfers/sec (read+write) - RTC db</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48c30-120">Datenträgerübertragungen/SEK-RTC-Protokoll</span><span class="sxs-lookup"><span data-stu-id="48c30-120">Disk Transfers/sec - RTC log</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="48c30-121">Datenträgerübertragungen/SEK-RTCDyn DB</span><span class="sxs-lookup"><span data-stu-id="48c30-121">Disk Transfers/sec - rtcdyn db</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="48c30-122">Datenträgerübertragungen/SEK-RTCdyn-Protokoll</span><span class="sxs-lookup"><span data-stu-id="48c30-122">Disk Transfers/sec - rtcdyn log</span></span></p></td>
<td></td>
</tr>
</tbody>
</table><span data-ttu-id="48c30-123">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="48c30-123">


</div>

<span> </span>

</div>

</div>

</span></span></div>

