---
title: 'Lync Server 2013: Session-Tabelle'
description: 'Lync Server 2013: Sitzungstabelle'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Session table
ms:assetid: 7f05529c-794d-41ed-bca4-2e85b87b2dec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398635(v=OCS.15)
ms:contentKeyID: 48184626
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e1a52813dfea808253cc934f71a9d4c846c2dbbd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441816"
---
# <a name="session-table-in-lync-server-2013"></a><span data-ttu-id="f0f74-103">Session-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0f74-103">Session table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f0f74-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f0f74-104">

<span> </span></span></span>

<span data-ttu-id="f0f74-105">_**Letztes Änderungsdatum des Themas:** 2013-09-09_</span><span class="sxs-lookup"><span data-stu-id="f0f74-105">_**Topic Last Modified:** 2013-09-09_</span></span>

<span data-ttu-id="f0f74-106">Jeder Eintrag stellt eine Sitzung dar, die Audio-oder Audio-und Videodaten beinhaltet.</span><span class="sxs-lookup"><span data-stu-id="f0f74-106">Each record represents one session which involves audio or audio and video.</span></span> <span data-ttu-id="f0f74-107">Sie enthält allgemeine Informationen zur Sitzung.</span><span class="sxs-lookup"><span data-stu-id="f0f74-107">It contains overall information about the session.</span></span> <span data-ttu-id="f0f74-108">Eine Sitzung ist als SIP-Dialog (Audio-oder Video Session Initiation Protocol) zwischen zwei Endpunkten definiert.</span><span class="sxs-lookup"><span data-stu-id="f0f74-108">A session is defined as an audio or video Session Initiation Protocol (SIP) dialog between two endpoints.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f0f74-109"><strong>Spalte</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-109"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="f0f74-110"><strong>Datentyp</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-110"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="f0f74-111"><strong>Schlüssel/Index</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-111"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="f0f74-112"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-112"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f0f74-113"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-113"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-114">datetime</span><span class="sxs-lookup"><span data-stu-id="f0f74-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="f0f74-115">Primary</span><span class="sxs-lookup"><span data-stu-id="f0f74-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="f0f74-116">Wird in der <a href="lync-server-2013-dialog-table.md">Dialog Feld Tabelle in lync Server 2013</a>referenziert.</span><span class="sxs-lookup"><span data-stu-id="f0f74-116">Referenced from the <a href="lync-server-2013-dialog-table.md">Dialog table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0f74-117"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-117"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-118">int</span><span class="sxs-lookup"><span data-stu-id="f0f74-118">int</span></span></p></td>
<td><p><span data-ttu-id="f0f74-119">Primary</span><span class="sxs-lookup"><span data-stu-id="f0f74-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="f0f74-120">Wird in der <a href="lync-server-2013-dialog-table.md">Dialog Feld Tabelle in lync Server 2013</a>referenziert.</span><span class="sxs-lookup"><span data-stu-id="f0f74-120">Referenced from the <a href="lync-server-2013-dialog-table.md">Dialog table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0f74-121"><strong>ConferenceKey</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-121"><strong>ConferenceKey</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-122">int</span><span class="sxs-lookup"><span data-stu-id="f0f74-122">int</span></span></p></td>
<td><p><span data-ttu-id="f0f74-123">Fremd</span><span class="sxs-lookup"><span data-stu-id="f0f74-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f0f74-124">Konferenz Taste.</span><span class="sxs-lookup"><span data-stu-id="f0f74-124">Conference key.</span></span> <span data-ttu-id="f0f74-125">Wird aus der <a href="lync-server-2013-conference-table.md">Konferenz Tabelle in lync Server 2013</a>referenziert.</span><span class="sxs-lookup"><span data-stu-id="f0f74-125">Referenced from the <a href="lync-server-2013-conference-table.md">Conference table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0f74-126"><strong>CorrelationKey</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-126"><strong>CorrelationKey</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-127">int</span><span class="sxs-lookup"><span data-stu-id="f0f74-127">int</span></span></p></td>
<td><p><span data-ttu-id="f0f74-128">Fremd</span><span class="sxs-lookup"><span data-stu-id="f0f74-128">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f0f74-129">Korrelationsschlüssel</span><span class="sxs-lookup"><span data-stu-id="f0f74-129">Correlation key.</span></span> <span data-ttu-id="f0f74-130">Wird in der <a href="lync-server-2013-sessioncorrelation-table.md">SessionCorrelation-Tabelle in lync Server 2013</a>referenziert.</span><span class="sxs-lookup"><span data-stu-id="f0f74-130">Referenced from the <a href="lync-server-2013-sessioncorrelation-table.md">SessionCorrelation table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0f74-131"><strong>DialogCategory</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-131"><strong>DialogCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-132">bit</span><span class="sxs-lookup"><span data-stu-id="f0f74-132">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f0f74-133">Dialog Feld Kategorie; 0 ist lync Server to Mediation Server Leg; 1 ist Vermittlungs Server für das PSTN-Gateway-Bein.</span><span class="sxs-lookup"><span data-stu-id="f0f74-133">Dialog category; 0 is Lync Server to Mediation Server leg; 1 is Mediation Server to PSTN gateway leg.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0f74-134"><strong>MediationServerBypassFlag</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-134"><strong>MediationServerBypassFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-135">bit</span><span class="sxs-lookup"><span data-stu-id="f0f74-135">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f0f74-136">Flag, das angibt, ob der Anruf umgangen wurde oder nicht.</span><span class="sxs-lookup"><span data-stu-id="f0f74-136">Flag indicating if the call was bypassed or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0f74-137"><strong>MediaBypassWarningFlag</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-137"><strong>MediaBypassWarningFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-138">int</span><span class="sxs-lookup"><span data-stu-id="f0f74-138">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f0f74-139">Dieses Feld, falls vorhanden, gibt an, warum ein Anruf nicht umgangen wurde, auch wenn die Bypass-IDs übereinstimmten.</span><span class="sxs-lookup"><span data-stu-id="f0f74-139">This field, if present, indicates why a call was not bypassed even if the bypass IDs matched.</span></span> <span data-ttu-id="f0f74-140">Bei lync Server ist nur ein Wert definiert.</span><span class="sxs-lookup"><span data-stu-id="f0f74-140">For Lync Server, only one value is defined.</span></span></p>
<p><span data-ttu-id="f0f74-141">0x0001 – unbekannte Bypass-ID für den standardmäßigen Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="f0f74-141">0x0001 – Unknown bypass ID for Default network adapter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0f74-142"><strong>StartTime</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-142"><strong>StartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-143">datetime</span><span class="sxs-lookup"><span data-stu-id="f0f74-143">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f0f74-144">Startzeit des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="f0f74-144">Call start time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0f74-145"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-145"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-146">datetime</span><span class="sxs-lookup"><span data-stu-id="f0f74-146">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="f0f74-147">Endzeit des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="f0f74-147">Call end time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0f74-148"><strong>CallerPool</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-148"><strong>CallerPool</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-149">int</span><span class="sxs-lookup"><span data-stu-id="f0f74-149">int</span></span></p></td>
<td><p><span data-ttu-id="f0f74-150">Fremd</span><span class="sxs-lookup"><span data-stu-id="f0f74-150">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f0f74-151">Der Pool des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="f0f74-151">The pool of the caller.</span></span> <span data-ttu-id="f0f74-152">Referenziert aus der <a href="lync-server-2013-pool-table.md">Pool Tabelle in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f0f74-152">Referenced from the <a href="lync-server-2013-pool-table.md">Pool table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0f74-153"><strong>CalleePool</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-153"><strong>CalleePool</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-154">int</span><span class="sxs-lookup"><span data-stu-id="f0f74-154">int</span></span></p></td>
<td><p><span data-ttu-id="f0f74-155">Fremd</span><span class="sxs-lookup"><span data-stu-id="f0f74-155">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f0f74-156">Der Pool des anrufempfängers.</span><span class="sxs-lookup"><span data-stu-id="f0f74-156">The pool of the call receiver.</span></span> <span data-ttu-id="f0f74-157">Referenziert aus der <a href="lync-server-2013-pool-table.md">Pool Tabelle in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="f0f74-157">Referenced from the <a href="lync-server-2013-pool-table.md">Pool table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0f74-158"><strong>CalleePAI</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-158"><strong>CalleePAI</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-159">int</span><span class="sxs-lookup"><span data-stu-id="f0f74-159">int</span></span></p></td>
<td><p><span data-ttu-id="f0f74-160">Fremd</span><span class="sxs-lookup"><span data-stu-id="f0f74-160">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f0f74-161">SIP-URI in der SIP p-asserted Identity (Pai) des empfangenden Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="f0f74-161">SIP URI in the SIP p-asserted identity (PAI) of the receiving endpoint.</span></span> <span data-ttu-id="f0f74-162">Wird in der <a href="lync-server-2013-user-table.md">Tabelle "Benutzer" in lync Server 2013</a>referenziert.</span><span class="sxs-lookup"><span data-stu-id="f0f74-162">Referenced from the <a href="lync-server-2013-user-table.md">User table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0f74-163"><strong>CallerURI</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-163"><strong>CallerURI</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-164">int</span><span class="sxs-lookup"><span data-stu-id="f0f74-164">int</span></span></p></td>
<td><p><span data-ttu-id="f0f74-165">Fremd</span><span class="sxs-lookup"><span data-stu-id="f0f74-165">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f0f74-166">URI des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="f0f74-166">Caller’s URI.</span></span> <span data-ttu-id="f0f74-167">Wird in der <a href="lync-server-2013-user-table.md">Tabelle "Benutzer" in lync Server 2013</a>referenziert.</span><span class="sxs-lookup"><span data-stu-id="f0f74-167">Referenced from the <a href="lync-server-2013-user-table.md">User table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0f74-168"><strong>CallerEndpoint</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-168"><strong>CallerEndpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-169">int</span><span class="sxs-lookup"><span data-stu-id="f0f74-169">int</span></span></p></td>
<td><p><span data-ttu-id="f0f74-170">Fremd</span><span class="sxs-lookup"><span data-stu-id="f0f74-170">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f0f74-171">Endpunkt des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="f0f74-171">Caller’s endpoint.</span></span> <span data-ttu-id="f0f74-172">Wird von der <a href="lync-server-2013-endpoint-table.md">Endpunkt Tabelle in lync Server 2013</a>referenziert.</span><span class="sxs-lookup"><span data-stu-id="f0f74-172">Referenced from the <a href="lync-server-2013-endpoint-table.md">Endpoint table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0f74-173"><strong>CallerUserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-173"><strong>CallerUserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-174">bit</span><span class="sxs-lookup"><span data-stu-id="f0f74-174">bit</span></span></p></td>
<td><p><span data-ttu-id="f0f74-175">Fremd</span><span class="sxs-lookup"><span data-stu-id="f0f74-175">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f0f74-176">Benutzer-Agent des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="f0f74-176">Caller’s user agent.</span></span> <span data-ttu-id="f0f74-177">Wird in der <a href="lync-server-2013-useragent-table.md">userAgent-Tabelle in lync Server 2013</a>referenziert.</span><span class="sxs-lookup"><span data-stu-id="f0f74-177">Referenced from the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0f74-178"><strong>CallPriority</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-178"><strong>CallPriority</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-179">smallint</span><span class="sxs-lookup"><span data-stu-id="f0f74-179">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f0f74-180">Die Priorität dieses Anrufs.</span><span class="sxs-lookup"><span data-stu-id="f0f74-180">The priority of this call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0f74-181"><strong>ClassifiedPoorCall</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-181"><strong>ClassifiedPoorCall</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-182">bit</span><span class="sxs-lookup"><span data-stu-id="f0f74-182">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f0f74-183">Diese Spalte wurde als veraltet markiert und wird in Microsoft lync Server 2013 nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="f0f74-183">This column has been deprecated and is not used in Microsoft Lync Server 2013.</span></span> <span data-ttu-id="f0f74-184">Stattdessen werden diese Informationen auf Basis einer einzelnen medienzeile gemeldet.</span><span class="sxs-lookup"><span data-stu-id="f0f74-184">Instead, this information is reported on a per-media line bases.</span></span> <span data-ttu-id="f0f74-185">Weitere Informationen finden Sie <a href="lync-server-2013-medialine-table.md">in der Tabelle medialinie in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f0f74-185">Refer to the <a href="lync-server-2013-medialine-table.md">MediaLine table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0f74-186"><strong>CallerPAI</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-186"><strong>CallerPAI</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-187">int</span><span class="sxs-lookup"><span data-stu-id="f0f74-187">int</span></span></p></td>
<td><p><span data-ttu-id="f0f74-188">Fremd</span><span class="sxs-lookup"><span data-stu-id="f0f74-188">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f0f74-189">P-bestätigt – Identität des Benutzers, der den Anruf getätigt hat.</span><span class="sxs-lookup"><span data-stu-id="f0f74-189">P-Asserted-Identity of the user who placed the call.</span></span> <span data-ttu-id="f0f74-190">Die P-Asserted-Identity (Pai) wird verwendet, um die wahre Identität des Benutzers zu vermitteln, der den Anruf getätigt hat.</span><span class="sxs-lookup"><span data-stu-id="f0f74-190">The P-Asserted-Identity (PAI) is used to convey the true identity of the user who placed the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0f74-191"><strong>CalleeEndpoint</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-191"><strong>CalleeEndpoint</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-192">int</span><span class="sxs-lookup"><span data-stu-id="f0f74-192">int</span></span></p></td>
<td><p><span data-ttu-id="f0f74-193">Fremd</span><span class="sxs-lookup"><span data-stu-id="f0f74-193">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f0f74-194">Endpunkt, der den Anruf empfangen hat.</span><span class="sxs-lookup"><span data-stu-id="f0f74-194">Endpoint that received the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f0f74-195"><strong>CalleeUserAgent</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-195"><strong>CalleeUserAgent</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-196">int</span><span class="sxs-lookup"><span data-stu-id="f0f74-196">int</span></span></p></td>
<td><p><span data-ttu-id="f0f74-197">Fremd</span><span class="sxs-lookup"><span data-stu-id="f0f74-197">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f0f74-198">Benutzer-Agent des Benutzers, der den Anruf erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="f0f74-198">User agent employed by the user who received the call.</span></span> <span data-ttu-id="f0f74-199">Benutzer-Agents stellen das Clientendpunkt Gerät dar.</span><span class="sxs-lookup"><span data-stu-id="f0f74-199">User agents represent the client endpoint device.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f0f74-200"><strong>CalleeUri</strong></span><span class="sxs-lookup"><span data-stu-id="f0f74-200"><strong>CalleeUri</strong></span></span></p></td>
<td><p><span data-ttu-id="f0f74-201">int</span><span class="sxs-lookup"><span data-stu-id="f0f74-201">int</span></span></p></td>
<td><p><span data-ttu-id="f0f74-202">Fremd</span><span class="sxs-lookup"><span data-stu-id="f0f74-202">Foreign</span></span></p></td>
<td><p><span data-ttu-id="f0f74-203">SIP-URI des Benutzers, der den Anruf erhalten hat.</span><span class="sxs-lookup"><span data-stu-id="f0f74-203">SIP URI of the user who received the call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f0f74-204">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f0f74-204">


</div>

<span> </span>

</div>

</div>

</span></span></div>

