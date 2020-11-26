---
title: Lync Server 2013 IPsec-Ausnahmen
description: Lync Server 2013 IPsec-Ausnahmen.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: IPsec exceptions
ms:assetid: 241f1eca-6f2f-44de-90b1-2cb659cbe27c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425719(v=OCS.15)
ms:contentKeyID: 48183627
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b01264171592ec352b778e1aa7eee5861801991
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426725"
---
# <a name="ipsec-exceptions-in-lync-server-2013"></a><span data-ttu-id="9e44c-103">IPsec-Ausnahmen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e44c-103">IPsec exceptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9e44c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9e44c-104">

<span> </span></span></span>

<span data-ttu-id="9e44c-105">_**Letztes Änderungsdatum des Themas:** 2012-06-27_</span><span class="sxs-lookup"><span data-stu-id="9e44c-105">_**Topic Last Modified:** 2012-06-27_</span></span>

<span data-ttu-id="9e44c-106">Für Unternehmensnetzwerke, in denen IPSec (Internet Protocol Security) (siehe IETF-RFC 4301-4309) bereitgestellt wurde, muss IPsec über den Portbereich deaktiviert werden, der für die Bereitstellung von Audio-, Video-und Panorama Video verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9e44c-106">For enterprise networks where Internet Protocol security (IPsec) (see IETF RFC 4301-4309) has been deployed, IPsec must be disabled over the range of ports used for the delivery of audio, video, and panorama video.</span></span> <span data-ttu-id="9e44c-107">Mit dieser Empfehlung sollen Verzögerungen in der Zuweisung von Medienports vermieden werden, die sich aus dem IPsec-Aushandlungsvorgang ergeben könnten.</span><span class="sxs-lookup"><span data-stu-id="9e44c-107">The recommendation is motivated by the need to avoid any delay in the allocation of media ports due to IPsec negotiation.</span></span>

<span data-ttu-id="9e44c-108">In der folgenden Tabelle werden die empfohlenen Einstellungen für IPsec-Ausnahmen erläutert.</span><span class="sxs-lookup"><span data-stu-id="9e44c-108">The following table explains the recommended IPsec exception settings.</span></span>

### <a name="recommended-ipsec-exceptions"></a><span data-ttu-id="9e44c-109">Empfohlene IPsec-Ausnahmen</span><span class="sxs-lookup"><span data-stu-id="9e44c-109">Recommended IPsec Exceptions</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9e44c-110">Regelname</span><span class="sxs-lookup"><span data-stu-id="9e44c-110">Rule name</span></span></th>
<th><span data-ttu-id="9e44c-111">Quell-IP</span><span class="sxs-lookup"><span data-stu-id="9e44c-111">Source IP</span></span></th>
<th><span data-ttu-id="9e44c-112">Ziel-IP</span><span class="sxs-lookup"><span data-stu-id="9e44c-112">Destination IP</span></span></th>
<th><span data-ttu-id="9e44c-113">Protokoll</span><span class="sxs-lookup"><span data-stu-id="9e44c-113">Protocol</span></span></th>
<th><span data-ttu-id="9e44c-114">Quellport</span><span class="sxs-lookup"><span data-stu-id="9e44c-114">Source port</span></span></th>
<th><span data-ttu-id="9e44c-115">Zielport</span><span class="sxs-lookup"><span data-stu-id="9e44c-115">Destination port</span></span></th>
<th><span data-ttu-id="9e44c-116">Authentifizierungsanforderung</span><span class="sxs-lookup"><span data-stu-id="9e44c-116">Authentication Requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9e44c-117">A/V-Edgeserver, intern eingehend</span><span class="sxs-lookup"><span data-stu-id="9e44c-117">A/V Edge Server Internal Inbound</span></span></p></td>
<td><p><span data-ttu-id="9e44c-118">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-118">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-119">A/V-Edgeserver, intern</span><span class="sxs-lookup"><span data-stu-id="9e44c-119">A/V Edge Server Internal</span></span></p></td>
<td><p><span data-ttu-id="9e44c-120">UDP und TCP</span><span class="sxs-lookup"><span data-stu-id="9e44c-120">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="9e44c-121">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-121">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-122">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-122">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-123">Nicht authentifizieren</span><span class="sxs-lookup"><span data-stu-id="9e44c-123">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e44c-124">A/V-Edgeserver, extern eingehend</span><span class="sxs-lookup"><span data-stu-id="9e44c-124">A/V Edge Server External Inbound</span></span></p></td>
<td><p><span data-ttu-id="9e44c-125">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-125">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-126">A/V-Edgeserver, extern</span><span class="sxs-lookup"><span data-stu-id="9e44c-126">A/V Edge Server External</span></span></p></td>
<td><p><span data-ttu-id="9e44c-127">UDP und TCP</span><span class="sxs-lookup"><span data-stu-id="9e44c-127">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="9e44c-128">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-128">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-129">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-129">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-130">Nicht authentifizieren</span><span class="sxs-lookup"><span data-stu-id="9e44c-130">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e44c-131">A/V-Edgeserver, intern ausgehend</span><span class="sxs-lookup"><span data-stu-id="9e44c-131">A/V Edge Server Internal Outbound</span></span></p></td>
<td><p><span data-ttu-id="9e44c-132">A/V-Edgeserver, intern</span><span class="sxs-lookup"><span data-stu-id="9e44c-132">A/V Edge Server Internal</span></span></p></td>
<td><p><span data-ttu-id="9e44c-133">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-133">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-134">UDP- &amp; TCP</span><span class="sxs-lookup"><span data-stu-id="9e44c-134">UDP &amp; TCP</span></span></p></td>
<td><p><span data-ttu-id="9e44c-135">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-135">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-136">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-136">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-137">Nicht authentifizieren</span><span class="sxs-lookup"><span data-stu-id="9e44c-137">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e44c-138">A/V-Edgeserver, extern ausgehend</span><span class="sxs-lookup"><span data-stu-id="9e44c-138">A/V Edge Server External Outbound</span></span></p></td>
<td><p><span data-ttu-id="9e44c-139">A/V-Edgeserver, extern</span><span class="sxs-lookup"><span data-stu-id="9e44c-139">A/V Edge Server External</span></span></p></td>
<td><p><span data-ttu-id="9e44c-140">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-140">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-141">UDP und TCP</span><span class="sxs-lookup"><span data-stu-id="9e44c-141">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="9e44c-142">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-142">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-143">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-143">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-144">Nicht authentifizieren</span><span class="sxs-lookup"><span data-stu-id="9e44c-144">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e44c-145">Vermittlungsserver, eingehend</span><span class="sxs-lookup"><span data-stu-id="9e44c-145">Mediation Server Inbound</span></span></p></td>
<td><p><span data-ttu-id="9e44c-146">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-146">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-147">Vermittlungs-</span><span class="sxs-lookup"><span data-stu-id="9e44c-147">Mediation</span></span></p>
<p><span data-ttu-id="9e44c-148">server</span><span class="sxs-lookup"><span data-stu-id="9e44c-148">Server(s)</span></span></p></td>
<td><p><span data-ttu-id="9e44c-149">UDP und TCP</span><span class="sxs-lookup"><span data-stu-id="9e44c-149">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="9e44c-150">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-150">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-151">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-151">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-152">Nicht authentifizieren</span><span class="sxs-lookup"><span data-stu-id="9e44c-152">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e44c-153">Vermittlungsserver, ausgehend</span><span class="sxs-lookup"><span data-stu-id="9e44c-153">Mediation Server Outbound</span></span></p></td>
<td><p><span data-ttu-id="9e44c-154">Vermittlungs-</span><span class="sxs-lookup"><span data-stu-id="9e44c-154">Mediation</span></span></p>
<p><span data-ttu-id="9e44c-155">server</span><span class="sxs-lookup"><span data-stu-id="9e44c-155">Server(s)</span></span></p></td>
<td><p><span data-ttu-id="9e44c-156">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-156">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-157">UDP und TCP</span><span class="sxs-lookup"><span data-stu-id="9e44c-157">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="9e44c-158">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-158">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-159">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-159">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-160">Nicht authentifizieren</span><span class="sxs-lookup"><span data-stu-id="9e44c-160">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e44c-161">Konferenzzentrale, eingehend</span><span class="sxs-lookup"><span data-stu-id="9e44c-161">Conferencing Attendant Inbound</span></span></p></td>
<td><p><span data-ttu-id="9e44c-162">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-162">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-163">Front-End-Server, auf dem die Konferenzzentrale ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="9e44c-163">Front End Server running Conferencing Attendant</span></span></p></td>
<td><p><span data-ttu-id="9e44c-164">UDP und TCP</span><span class="sxs-lookup"><span data-stu-id="9e44c-164">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="9e44c-165">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-165">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-166">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-166">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-167">Nicht authentifizieren</span><span class="sxs-lookup"><span data-stu-id="9e44c-167">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e44c-168">Konferenzzentrale (ausgehend)</span><span class="sxs-lookup"><span data-stu-id="9e44c-168">Conferencing Attendant Outbound</span></span></p></td>
<td><p><span data-ttu-id="9e44c-169">Front-End-Server, auf dem die Konferenzzentrale ausgeführt wird</span><span class="sxs-lookup"><span data-stu-id="9e44c-169">Front End Server running Conferencing Attendant</span></span></p></td>
<td><p><span data-ttu-id="9e44c-170">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-170">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-171">UDP und TCP</span><span class="sxs-lookup"><span data-stu-id="9e44c-171">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="9e44c-172">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-172">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-173">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-173">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-174">Nicht authentifizieren</span><span class="sxs-lookup"><span data-stu-id="9e44c-174">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e44c-175">A/V-Konferenzserver, eingehend</span><span class="sxs-lookup"><span data-stu-id="9e44c-175">A/V Conferencing Inbound</span></span></p></td>
<td><p><span data-ttu-id="9e44c-176">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-176">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-177">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="9e44c-177">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="9e44c-178">UDP und TCP</span><span class="sxs-lookup"><span data-stu-id="9e44c-178">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="9e44c-179">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-179">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-180">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-180">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-181">Nicht authentifizieren</span><span class="sxs-lookup"><span data-stu-id="9e44c-181">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e44c-182">A/V-Konferenzen, ausgehend</span><span class="sxs-lookup"><span data-stu-id="9e44c-182">A/V Conferencing Outbound</span></span></p></td>
<td><p><span data-ttu-id="9e44c-183">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="9e44c-183">Front End Servers</span></span></p></td>
<td><p><span data-ttu-id="9e44c-184">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-184">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-185">UDP und TCP</span><span class="sxs-lookup"><span data-stu-id="9e44c-185">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="9e44c-186">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-186">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-187">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-187">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-188">Nicht authentifizieren</span><span class="sxs-lookup"><span data-stu-id="9e44c-188">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e44c-189">Exchange, eingehend</span><span class="sxs-lookup"><span data-stu-id="9e44c-189">Exchange Inbound</span></span></p></td>
<td><p><span data-ttu-id="9e44c-190">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-190">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-191">Exchange Unified Messaging</span><span class="sxs-lookup"><span data-stu-id="9e44c-191">Exchange Unified Messaging</span></span></p></td>
<td><p><span data-ttu-id="9e44c-192">UDP und TCP</span><span class="sxs-lookup"><span data-stu-id="9e44c-192">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="9e44c-193">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-193">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-194">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-194">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-195">Nicht authentifizieren</span><span class="sxs-lookup"><span data-stu-id="9e44c-195">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e44c-196">Anwendungsfreigabeserver, eingehend</span><span class="sxs-lookup"><span data-stu-id="9e44c-196">Application Sharing Servers Inbound</span></span></p></td>
<td><p><span data-ttu-id="9e44c-197">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-197">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-198">Anwendungsfreigabeserver</span><span class="sxs-lookup"><span data-stu-id="9e44c-198">Application Sharing Servers</span></span></p></td>
<td><p><span data-ttu-id="9e44c-199">TCP</span><span class="sxs-lookup"><span data-stu-id="9e44c-199">TCP</span></span></p></td>
<td><p><span data-ttu-id="9e44c-200">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-200">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-201">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-201">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-202">Nicht authentifizieren</span><span class="sxs-lookup"><span data-stu-id="9e44c-202">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e44c-203">Anwendungsfreigabeserver, ausgehend</span><span class="sxs-lookup"><span data-stu-id="9e44c-203">Application Sharing Server Outbound</span></span></p></td>
<td><p><span data-ttu-id="9e44c-204">Anwendungsfreigabeserver</span><span class="sxs-lookup"><span data-stu-id="9e44c-204">Application Sharing Servers</span></span></p></td>
<td><p><span data-ttu-id="9e44c-205">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-205">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-206">TCP</span><span class="sxs-lookup"><span data-stu-id="9e44c-206">TCP</span></span></p></td>
<td><p><span data-ttu-id="9e44c-207">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-207">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-208">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-208">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-209">Nicht authentifizieren</span><span class="sxs-lookup"><span data-stu-id="9e44c-209">Do not authenticate</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9e44c-210">Exchange, ausgehend</span><span class="sxs-lookup"><span data-stu-id="9e44c-210">Exchange Outbound</span></span></p></td>
<td><p><span data-ttu-id="9e44c-211">Exchange Unified Messaging</span><span class="sxs-lookup"><span data-stu-id="9e44c-211">Exchange Unified Messaging</span></span></p></td>
<td><p><span data-ttu-id="9e44c-212">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-212">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-213">UDP und TCP</span><span class="sxs-lookup"><span data-stu-id="9e44c-213">UDP and TCP</span></span></p></td>
<td><p><span data-ttu-id="9e44c-214">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-214">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-215">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-215">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-216">Nicht authentifizieren</span><span class="sxs-lookup"><span data-stu-id="9e44c-216">Do not authenticate</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9e44c-217">Clients</span><span class="sxs-lookup"><span data-stu-id="9e44c-217">Clients</span></span></p></td>
<td><p><span data-ttu-id="9e44c-218">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-218">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-219">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-219">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-220">UDP</span><span class="sxs-lookup"><span data-stu-id="9e44c-220">UDP</span></span></p></td>
<td><p><span data-ttu-id="9e44c-221">Angegebener Medienportbereich</span><span class="sxs-lookup"><span data-stu-id="9e44c-221">Specified media port range</span></span></p></td>
<td><p><span data-ttu-id="9e44c-222">Beliebig</span><span class="sxs-lookup"><span data-stu-id="9e44c-222">Any</span></span></p></td>
<td><p><span data-ttu-id="9e44c-223">Nicht authentifizieren</span><span class="sxs-lookup"><span data-stu-id="9e44c-223">Do not authenticate</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="9e44c-224">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9e44c-224">


</div>

<span> </span>

</div>

</div>

</span></span></div>

