---
title: 'Lync Server 2013: QoE-Berichte'
description: 'Lync Server 2013: QoE-Berichte.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: QoE reports
ms:assetid: 49c827af-b8dd-4c6e-b0dc-b4bc6d60e9a3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720913(v=OCS.15)
ms:contentKeyID: 63969601
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 55965d246b7f0ddd71eaeeec99d218eaf8819c2e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394526"
---
# <a name="qoe-reports-in-lync-server-2013"></a><span data-ttu-id="3bc0a-103">QoE-Berichte in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3bc0a-103">QoE reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3bc0a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3bc0a-104">

<span> </span></span></span>

<span data-ttu-id="3bc0a-105">_**Letztes Änderungsdatum des Themas:** 2014-05-01_</span><span class="sxs-lookup"><span data-stu-id="3bc0a-105">_**Topic Last Modified:** 2014-05-01_</span></span>

<div>

## <a name="qoe-summarytrend-reports"></a><span data-ttu-id="3bc0a-106">QoE-Zusammenfassung/Trendberichte</span><span class="sxs-lookup"><span data-stu-id="3bc0a-106">QoE summary/trend reports</span></span>

<span data-ttu-id="3bc0a-107">Die Berichte QoE-Zusammenfassung/Trends sind hilfreich, um die Spitzenzeiten für die Nutzung zu ermitteln und die Medienqualität in diesen Zeiten zu untersuchen, um sicherzustellen, dass die Netzwerkressourcen Ihrer Organisation ausreichend sind.</span><span class="sxs-lookup"><span data-stu-id="3bc0a-107">The QoE summary/trends reports are useful for finding the peak usage times of day and examining the media quality during those times to help assure that your organization's network resources are sufficient.</span></span> <span data-ttu-id="3bc0a-108">Ihre Organisation kann auch die zahlreichen im Bericht verfügbaren Filter verwenden, um Leistungsnummern für bestimmte Speicherorte, Client-und Gerätetypen und Server zu isolieren.</span><span class="sxs-lookup"><span data-stu-id="3bc0a-108">Your organization can also use the many filters available in the report to isolate performance numbers for certain locations, client and device types, and servers.</span></span>

<span data-ttu-id="3bc0a-109">QoE-Zusammenfassung/Trendberichte bestehen aus:</span><span class="sxs-lookup"><span data-stu-id="3bc0a-109">QoE summary/trend reports consist of:</span></span>

  - <span data-ttu-id="3bc0a-110">UC-zu-UC-Zusammenfassung/Trend Bericht</span><span class="sxs-lookup"><span data-stu-id="3bc0a-110">UC-to-UC Summary/Trend Report</span></span>

  - <span data-ttu-id="3bc0a-111">PSTN-Zusammenfassung/Trend Bericht</span><span class="sxs-lookup"><span data-stu-id="3bc0a-111">PSTN Summary/Trend Report</span></span>

  - <span data-ttu-id="3bc0a-112">Konferenz Zusammenfassung/Trend Bericht</span><span class="sxs-lookup"><span data-stu-id="3bc0a-112">Conference Summary/Trend Report</span></span>

</div>

<div>

## <a name="qoe-performance-reports"></a><span data-ttu-id="3bc0a-113">QoE-Leistungsberichte</span><span class="sxs-lookup"><span data-stu-id="3bc0a-113">QoE performance reports</span></span>

<span data-ttu-id="3bc0a-114">QoE-Leistungsberichte bieten Details zu den drei Berichten, die sich auf die QoE-Leistung von Mediations Servern, A/V-Konferenzservern und Endpunkt Speicherorten konzentrieren.</span><span class="sxs-lookup"><span data-stu-id="3bc0a-114">QoE performance reports provide details about the three reports that concentrate on the QoE performance of Mediation Servers, A/V Conferencing Servers, and endpoint locations.</span></span>

</div>

<div>

## <a name="mediation-server-performance-report"></a><span data-ttu-id="3bc0a-115">Bericht zur Vermittlungsserver Leistung</span><span class="sxs-lookup"><span data-stu-id="3bc0a-115">Mediation server performance report</span></span>

<span data-ttu-id="3bc0a-116">Im Bericht "Vermittlungs Server Leistung" werden die Metriken aufgelistet, die von einer oder mehreren Mediation während des angegebenen Zeitraums erreicht wurden.</span><span class="sxs-lookup"><span data-stu-id="3bc0a-116">The Mediation Server Performance report lists the metrics achieved by one or more Mediation during the specified time period.</span></span> <span data-ttu-id="3bc0a-117">Die Metriken für das Unified Communications (UC)-to-Mediation-Server Bein und das Vermittlungsserver-zu-Gateway-Bein jedes Anrufs werden separat gemeldet.</span><span class="sxs-lookup"><span data-stu-id="3bc0a-117">The metrics for the unified communications (UC)-to-Mediation Server leg and the Mediation Server-to-Gateway leg of each call are reported separately.</span></span> <span data-ttu-id="3bc0a-118">Mit diesem Bericht können Sie die Lautstärke und Leistung der verschiedenen Vermittlungsserver Ihrer Organisation vergleichen.</span><span class="sxs-lookup"><span data-stu-id="3bc0a-118">Use this report to compare the volume and performance of your organization's various Mediation Servers.</span></span>

<span data-ttu-id="3bc0a-119">Für jeden Vermittlungs Server (und für jedes Anruf Bein) wird im Bericht Folgendes angezeigt:</span><span class="sxs-lookup"><span data-stu-id="3bc0a-119">For each Mediation Server (and for each call leg), the report displays the following:</span></span>

  - <span data-ttu-id="3bc0a-120">Anzahl der Anrufe</span><span class="sxs-lookup"><span data-stu-id="3bc0a-120">Number of calls</span></span>

  - <span data-ttu-id="3bc0a-121">Paketverlust</span><span class="sxs-lookup"><span data-stu-id="3bc0a-121">Packet Loss</span></span>

  - <span data-ttu-id="3bc0a-122">Round-Trip-Zeit</span><span class="sxs-lookup"><span data-stu-id="3bc0a-122">Round Trip Time</span></span>

  - <span data-ttu-id="3bc0a-123">Jitter</span><span class="sxs-lookup"><span data-stu-id="3bc0a-123">Jitter</span></span>

  - <span data-ttu-id="3bc0a-124">Conversational Mean Opinion Score (MOS)</span><span class="sxs-lookup"><span data-stu-id="3bc0a-124">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="3bc0a-125">Senden von MOS</span><span class="sxs-lookup"><span data-stu-id="3bc0a-125">Sending MOS</span></span>

  - <span data-ttu-id="3bc0a-126">Anhören von MOS</span><span class="sxs-lookup"><span data-stu-id="3bc0a-126">Listening MOS</span></span>

  - <span data-ttu-id="3bc0a-127">Netzwerk-Mos</span><span class="sxs-lookup"><span data-stu-id="3bc0a-127">Network MOS</span></span>

  - <span data-ttu-id="3bc0a-128">Netzwerk-Mos-Verschlechterung</span><span class="sxs-lookup"><span data-stu-id="3bc0a-128">Network MOS Degradation</span></span>

  - <span data-ttu-id="3bc0a-129">Echo-Rückgabe</span><span class="sxs-lookup"><span data-stu-id="3bc0a-129">Echo Return</span></span>

  - <span data-ttu-id="3bc0a-130">Signal Pegel</span><span class="sxs-lookup"><span data-stu-id="3bc0a-130">Signal Level</span></span>

</div>

<div>

## <a name="av-conferencing-server-performance-report"></a><span data-ttu-id="3bc0a-131">A/V-Konferenzserver-Leistungsbericht</span><span class="sxs-lookup"><span data-stu-id="3bc0a-131">A/V conferencing server performance report</span></span>

<span data-ttu-id="3bc0a-132">Der Leistungsbericht a/v Conferencing Server bietet Listen mit Metriken, die von einem oder mehreren a/v-Konferenzservern während des angegebenen Zeitraums erreicht wurden.</span><span class="sxs-lookup"><span data-stu-id="3bc0a-132">The A/V Conferencing Server Performance report provides lists of metrics achieved by one or more A/V Conferencing Servers during the specified time period.</span></span> <span data-ttu-id="3bc0a-133">Dieser Bericht kann verwendet werden, um die Lautstärke und Leistung der verschiedenen A/V-Konferenzserver Ihrer Organisation zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="3bc0a-133">This report can be used to compare the volume and performance of your organization’s various A/V Conferencing Servers.</span></span> <span data-ttu-id="3bc0a-134">Ihre Organisation kann den Bericht auch isolieren, um nur die Benutzeroberfläche für bestimmte Clienttypen wie lync-Clients oder PSTN-Clients anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="3bc0a-134">Your organization can also isolate the report to show only the experience for specific client types, such as Lync clients or PSTN clients.</span></span>

<span data-ttu-id="3bc0a-135">Für jeden A/V-Konferenz Server wird im Bericht Folgendes angezeigt:</span><span class="sxs-lookup"><span data-stu-id="3bc0a-135">For each A/V Conferencing Server, the report displays the following:</span></span>

  - <span data-ttu-id="3bc0a-136">Anzahl von Konferenzen</span><span class="sxs-lookup"><span data-stu-id="3bc0a-136">Number of conferences</span></span>

  - <span data-ttu-id="3bc0a-137">Paketverlust</span><span class="sxs-lookup"><span data-stu-id="3bc0a-137">Packet Loss</span></span>

  - <span data-ttu-id="3bc0a-138">Round-Trip-Zeit</span><span class="sxs-lookup"><span data-stu-id="3bc0a-138">Round Trip Time</span></span>

  - <span data-ttu-id="3bc0a-139">Jitter</span><span class="sxs-lookup"><span data-stu-id="3bc0a-139">Jitter</span></span>

  - <span data-ttu-id="3bc0a-140">Conversational Mean Opinion Score (MOS)</span><span class="sxs-lookup"><span data-stu-id="3bc0a-140">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="3bc0a-141">Senden von MOS</span><span class="sxs-lookup"><span data-stu-id="3bc0a-141">Sending MOS</span></span>

  - <span data-ttu-id="3bc0a-142">Anhören von MOS</span><span class="sxs-lookup"><span data-stu-id="3bc0a-142">Listening MOS</span></span>

  - <span data-ttu-id="3bc0a-143">Netzwerk-Mos</span><span class="sxs-lookup"><span data-stu-id="3bc0a-143">Network MOS</span></span>

  - <span data-ttu-id="3bc0a-144">Netzwerk-Mos-Verschlechterung</span><span class="sxs-lookup"><span data-stu-id="3bc0a-144">Network MOS Degradation</span></span>

  - <span data-ttu-id="3bc0a-145">Echo-Rückgabe</span><span class="sxs-lookup"><span data-stu-id="3bc0a-145">Echo Return</span></span>

  - <span data-ttu-id="3bc0a-146">Signal Pegel</span><span class="sxs-lookup"><span data-stu-id="3bc0a-146">Signal Level</span></span>

</div>

<div>

## <a name="location-based-performance-report"></a><span data-ttu-id="3bc0a-147">Bericht zur standortbasierten Leistung</span><span class="sxs-lookup"><span data-stu-id="3bc0a-147">Location-based performance report</span></span>

<span data-ttu-id="3bc0a-148">Der Location-Based Leistungsbericht enthält eine Liste der Netzwerkspeicherorte, und für jeden Standort wird die Anzahl der Anrufe in jedem zuvor festgelegten Qualitätsbereich angezeigt.</span><span class="sxs-lookup"><span data-stu-id="3bc0a-148">The Location-Based Performance report provides a list of network locations and for each location shows the number of calls in each pre-determined range of quality.</span></span> <span data-ttu-id="3bc0a-149">Ziel dieses Berichts ist es, Einblicke in die Medienqualität des Großteils der Telefonanrufe Ihrer Organisation an verschiedenen Standorten zu geben, damit Sie schlecht darstellende Standorte erkennen und die unterschiedlichen Grade der Medienqualität in den verschiedenen Speicherorten Ihrer Organisation sehen können.</span><span class="sxs-lookup"><span data-stu-id="3bc0a-149">The goal of this report is to provide insight into the media quality of the bulk of your organization’s telephone calls for various locations so that you can identify poorly performing locations, and see the different grades of media quality in your organization’s different locations.</span></span>

<span data-ttu-id="3bc0a-150">Beim Anzeigen des Berichts werden unterschiedliche Tabellen mit Metriken angezeigt – eine Tabelle für jede Metrik, über die Ihre Organisation berichten möchte.</span><span class="sxs-lookup"><span data-stu-id="3bc0a-150">When displaying the report, different tables of metrics appear—one table for each metric your organization decides to report on.</span></span> <span data-ttu-id="3bc0a-151">Sie können aus den folgenden Metriken für diesen Bericht wählen:</span><span class="sxs-lookup"><span data-stu-id="3bc0a-151">You can choose from the following metrics for this report:</span></span>

  - <span data-ttu-id="3bc0a-152">Conversational Mean Opinion Score (MOS)</span><span class="sxs-lookup"><span data-stu-id="3bc0a-152">Conversational mean opinion score (MOS)</span></span>

  - <span data-ttu-id="3bc0a-153">Netzwerk-Mos</span><span class="sxs-lookup"><span data-stu-id="3bc0a-153">Network MOS</span></span>

  - <span data-ttu-id="3bc0a-154">Netzwerk-Mos-Verschlechterung</span><span class="sxs-lookup"><span data-stu-id="3bc0a-154">Network MOS Degradation</span></span>

  - <span data-ttu-id="3bc0a-155">Senden von MOS</span><span class="sxs-lookup"><span data-stu-id="3bc0a-155">Sending MOS</span></span>

  - <span data-ttu-id="3bc0a-156">Anhören von MOS</span><span class="sxs-lookup"><span data-stu-id="3bc0a-156">Listening MOS</span></span>

  - <span data-ttu-id="3bc0a-157">Paketverlust</span><span class="sxs-lookup"><span data-stu-id="3bc0a-157">Packet Loss</span></span>

  - <span data-ttu-id="3bc0a-158">Jitter</span><span class="sxs-lookup"><span data-stu-id="3bc0a-158">Jitter</span></span>

  - <span data-ttu-id="3bc0a-159">Latenz</span><span class="sxs-lookup"><span data-stu-id="3bc0a-159">Latency</span></span>

<span data-ttu-id="3bc0a-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3bc0a-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

