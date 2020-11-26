---
title: 'Lync Server 2013: Überwachen des Gruppen-Chats'
description: 'Lync Server 2013: Überwachen des Gruppen-Chats.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring group chat
ms:assetid: bddcf0be-ebf3-46bc-90c7-2576877734fb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720924(v=OCS.15)
ms:contentKeyID: 63969648
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 625e45f455e8dba50a5fa64240b62cb010623d16
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425423"
---
# <a name="monitoring-group-chat-in-lync-server-2013"></a><span data-ttu-id="a64c7-103">Überwachen des Gruppen-Chats in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a64c7-103">Monitoring group chat in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a64c7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a64c7-104">

<span> </span></span></span>

<span data-ttu-id="a64c7-105">_**Letztes Änderungsdatum des Themas:** 2014-08-04_</span><span class="sxs-lookup"><span data-stu-id="a64c7-105">_**Topic Last Modified:** 2014-08-04_</span></span>

<span data-ttu-id="a64c7-106">Es wird dringend empfohlen, das neueste im Microsoft Download Center verfügbare [kumulative Server Update-Installationsprogramm](https://support.microsoft.com/kb/968802) zur Verbesserung der Leistung zu führen.</span><span class="sxs-lookup"><span data-stu-id="a64c7-106">We highly recommend running the most recent [Cumulative Server Update Installer](https://support.microsoft.com/kb/968802) available on the Microsoft Download Center for performance improvements.</span></span>

<span data-ttu-id="a64c7-107">Unter der Voraussetzung, dass Sie das neueste kumulative Update ausführen, verwenden Sie die folgende Belastungstest Tabelle für Metriken, um zu verstehen, ob Ihre Gruppen-Chat Server mit optimaler Integrität ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a64c7-107">Assuming you are running latest cumulative update, use the following stress test table for metrics to understand if your Group Chat Servers are running at optimal health.</span></span>

### <a name="test-environment-and-user-model"></a><span data-ttu-id="a64c7-108">Test Umgebung und Benutzermodell</span><span class="sxs-lookup"><span data-stu-id="a64c7-108">Test environment and user model</span></span>

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th> </th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a64c7-109">Drei Gruppen-Chat Server in einem Gruppen-Chat-Pool mit jeweils 8 GB Arbeitsspeicher und 8 Prozessoren.</span><span class="sxs-lookup"><span data-stu-id="a64c7-109">Three Group Chat Servers in a Group Chat pool, each with 8 GB memory and 8 processors.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a64c7-110">Zwei lync Server 2013-Front-Ends in Enterprise Edition</span><span class="sxs-lookup"><span data-stu-id="a64c7-110">Two Lync Server 2013 Front Ends in Enterprise Edition.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a64c7-111">60.000 gleichzeitige Benutzer in drei Gruppen Chat Servern.</span><span class="sxs-lookup"><span data-stu-id="a64c7-111">60,000 concurrent users across three Group Chat Servers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a64c7-112">25.000-Kanäle, die vom Gruppen-Chat-Pool gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="a64c7-112">25,000 channels hosted by Group Chat Pool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a64c7-113">Kanalgröße:</span><span class="sxs-lookup"><span data-stu-id="a64c7-113">Channel Size:</span></span></p>
<ul>
<li><p><span data-ttu-id="a64c7-114">Größe des kleinen Kanals: 30</span><span class="sxs-lookup"><span data-stu-id="a64c7-114">Small Channel Size: 30</span></span></p></li>
<li><p><span data-ttu-id="a64c7-115">Mittlere Kanalgröße: 150</span><span class="sxs-lookup"><span data-stu-id="a64c7-115">Medium Channel Size: 150</span></span></p></li>
<li><p><span data-ttu-id="a64c7-116">Größe des großen Kanals: 2500</span><span class="sxs-lookup"><span data-stu-id="a64c7-116">Large Channel Size: 2500</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a64c7-117">Kanalanzahl:</span><span class="sxs-lookup"><span data-stu-id="a64c7-117">Channel Count:</span></span></p>
<ul>
<li><p><span data-ttu-id="a64c7-118">Zahl kleine Kanäle: 24.000</span><span class="sxs-lookup"><span data-stu-id="a64c7-118">Number small channels: 24,000</span></span></p></li>
<li><p><span data-ttu-id="a64c7-119">Zahl Medium Kanäle 800</span><span class="sxs-lookup"><span data-stu-id="a64c7-119">Number medium channels 800</span></span></p></li>
<li><p><span data-ttu-id="a64c7-120">Zahl große Kanäle 24</span><span class="sxs-lookup"><span data-stu-id="a64c7-120">Number large channels 24</span></span></p></li>
<li><p><span data-ttu-id="a64c7-121">Gesamtzahl der Kanäle 24.824</span><span class="sxs-lookup"><span data-stu-id="a64c7-121">Total Channels 24,824</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a64c7-122">Kanäle einladen:</span><span class="sxs-lookup"><span data-stu-id="a64c7-122">Invite channels:</span></span></p>
<ul>
<li><p><span data-ttu-id="a64c7-123">Die Hälfte der Kanäle waren Einladungs Kanäle</span><span class="sxs-lookup"><span data-stu-id="a64c7-123">Half the channels were invite channels</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a64c7-124">Die Anzahl der Kanäle, die ein Benutzer verknüpft:</span><span class="sxs-lookup"><span data-stu-id="a64c7-124">Number of channels a user joins:</span></span></p>
<ul>
<li><p><span data-ttu-id="a64c7-125">Klein: 12</span><span class="sxs-lookup"><span data-stu-id="a64c7-125">Small: 12</span></span></p></li>
<li><p><span data-ttu-id="a64c7-126">Mittel: 2</span><span class="sxs-lookup"><span data-stu-id="a64c7-126">Medium: 2</span></span></p></li>
<li><p><span data-ttu-id="a64c7-127">Groß: 1</span><span class="sxs-lookup"><span data-stu-id="a64c7-127">Large: 1</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a64c7-128">Teilnahmegebühr:</span><span class="sxs-lookup"><span data-stu-id="a64c7-128">Join rate:</span></span></p>
<ul>
<li><p><span data-ttu-id="a64c7-129">10 Gesamt/Sekunde, 3.33/Sekunde pro Server</span><span class="sxs-lookup"><span data-stu-id="a64c7-129">10 total/second, 3.33/second per server</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a64c7-130">Abmelde Rate:</span><span class="sxs-lookup"><span data-stu-id="a64c7-130">Logout rate:</span></span></p>
<ul>
<li><p><span data-ttu-id="a64c7-131">10 Gesamt/Sekunde, 3.33/Sekunde pro Server</span><span class="sxs-lookup"><span data-stu-id="a64c7-131">10 total/second, 3.33/second per server</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a64c7-132">Chat-Gebühr:</span><span class="sxs-lookup"><span data-stu-id="a64c7-132">Chat rate:</span></span></p>
<ul>
<li><p><span data-ttu-id="a64c7-133">20 gesamt/Sekunde, 6.66/Sekunde pro Server</span><span class="sxs-lookup"><span data-stu-id="a64c7-133">20 total/second, 6.66/second per server</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <span data-ttu-id="a64c7-134">Die folgenden Leistungsindikator Nummern variieren wahrscheinlich, wenn verschiedene Hardwarespezifikationen oder Benutzerprofile verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a64c7-134">The following performance counter numbers will likely vary when different hardware specifications or user profiles are used.</span></span>



</div>

### <a name="performance-counter-to-be-monitored"></a><span data-ttu-id="a64c7-135">Zu überwachenden Leistungsindikator</span><span class="sxs-lookup"><span data-stu-id="a64c7-135">Performance counter to be monitored</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a64c7-136">Leistungsindikator</span><span class="sxs-lookup"><span data-stu-id="a64c7-136">Performance Counter</span></span></th>
<th><span data-ttu-id="a64c7-137">Schwellenwerte</span><span class="sxs-lookup"><span data-stu-id="a64c7-137">Thresholds</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a64c7-138">Prozess (Channelservice)- &gt; % Prozessorzeit</span><span class="sxs-lookup"><span data-stu-id="a64c7-138">Process(ChannelService)-&gt;%Processor Time</span></span></p></td>
<td><p><span data-ttu-id="a64c7-139">Min: 0</span><span class="sxs-lookup"><span data-stu-id="a64c7-139">Min: 0</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="a64c7-140">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a64c7-140">


</div>

<span> </span>

</div>

</div>

</span></span></div>

