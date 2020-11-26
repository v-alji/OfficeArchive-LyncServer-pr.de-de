---
title: 'Lync Server 2013: Registration-Tabelle'
description: 'Lync Server 2013: Registrierungstabelle'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Registration table
ms:assetid: 05ff9dd3-1aaa-4af0-bd69-8789fb8eaeb3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398114(v=OCS.15)
ms:contentKeyID: 48183298
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 806e1a4e944c9bc04ebdd167c41c80a57fde3f29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436566"
---
# <a name="registration-table-in-lync-server-2013"></a><span data-ttu-id="b3a4a-103">Registration-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b3a4a-103">Registration table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b3a4a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b3a4a-104">

<span> </span></span></span>

<span data-ttu-id="b3a4a-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="b3a4a-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="b3a4a-106">Jeder Datensatz steht für ein Benutzer Registrierungs Ereignis.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-106">Each record represents one user registration event.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b3a4a-107">Spalte</span><span class="sxs-lookup"><span data-stu-id="b3a4a-107">Column</span></span></th>
<th><span data-ttu-id="b3a4a-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b3a4a-108">Data Type</span></span></th>
<th><span data-ttu-id="b3a4a-109">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="b3a4a-109">Key/Index</span></span></th>
<th><span data-ttu-id="b3a4a-110">Details</span><span class="sxs-lookup"><span data-stu-id="b3a4a-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b3a4a-111"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-112">datetime</span><span class="sxs-lookup"><span data-stu-id="b3a4a-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="b3a4a-113">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="b3a4a-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="b3a4a-114">Uhrzeit der Sitzungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-114">Time of session request.</span></span> <span data-ttu-id="b3a4a-115">Wird in Verbindung mit <strong>SessionIdSeq</strong> verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="b3a4a-116">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b3a4a-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3a4a-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-118">int</span><span class="sxs-lookup"><span data-stu-id="b3a4a-118">int</span></span></p></td>
<td><p><span data-ttu-id="b3a4a-119">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="b3a4a-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="b3a4a-120">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-120">ID number to identify the session.</span></span> <span data-ttu-id="b3a4a-121">Wird in Verbindung mit <strong>SessionID</strong> -Mal verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="b3a4a-122">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b3a4a-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3a4a-123"><strong>UserID</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-123"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-124">int</span><span class="sxs-lookup"><span data-stu-id="b3a4a-124">int</span></span></p></td>
<td><p><span data-ttu-id="b3a4a-125">Fremd</span><span class="sxs-lookup"><span data-stu-id="b3a4a-125">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b3a4a-126">Die Benutzer-ID.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-126">The user ID.</span></span> <span data-ttu-id="b3a4a-127">Weitere Informationen finden Sie <a href="lync-server-2013-users-table.md">in der Tabelle Benutzer in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b3a4a-127">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3a4a-128"><strong>EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-128"><strong>EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-129">uniqueidentifier</span><span class="sxs-lookup"><span data-stu-id="b3a4a-129">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b3a4a-130">Eine GUID, um einen Registrierungs Endpunkt zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-130">A GUID to identify a registration endpoint.</span></span> <span data-ttu-id="b3a4a-131">In der Regel verfügt das Register-Ereignis vom gleichen Computer desselben Benutzers über die gleiche Endpunkt-ID.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-131">Usually the register event from the same computer of the same user will have the same endpoint ID.</span></span> <span data-ttu-id="b3a4a-132">Unterschiedliche Computer verfügen über eine andere Endpunkt-ID.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-132">Different machines have a different endpoint ID.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3a4a-133"><strong>EndpointEra</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-133"><strong>EndpointEra</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-134">uniqueIdentifier</span><span class="sxs-lookup"><span data-stu-id="b3a4a-134">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b3a4a-135">Die ID, mit der Registrierungen unterschieden werden, die denselben Benutzer und denselben Endpunkt einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-135">ID used to differentiate registrations that involve the same user and the same endpoint.</span></span></p>
<p><span data-ttu-id="b3a4a-136">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-136">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3a4a-137"><strong>ClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-137"><strong>ClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-138">int</span><span class="sxs-lookup"><span data-stu-id="b3a4a-138">int</span></span></p></td>
<td><p><span data-ttu-id="b3a4a-139">Fremd</span><span class="sxs-lookup"><span data-stu-id="b3a4a-139">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b3a4a-140">Client Version des aktuellen Benutzers.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-140">Client version of current user.</span></span> <span data-ttu-id="b3a4a-141">Weitere Informationen finden Sie <a href="lync-server-2013-clientversions-table.md">in der ClientVersions-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b3a4a-141">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3a4a-142"><strong>Registrator</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-142"><strong>RegistrarId</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-143">int</span><span class="sxs-lookup"><span data-stu-id="b3a4a-143">int</span></span></p></td>
<td><p><span data-ttu-id="b3a4a-144">Fremd</span><span class="sxs-lookup"><span data-stu-id="b3a4a-144">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b3a4a-145">Die ID des Registrierungsservers, der für die Registrierung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-145">ID of the Registrar Server used for registration.</span></span> <span data-ttu-id="b3a4a-146">Weitere Informationen finden Sie <a href="lync-server-2013-servers-table.md">in der Tabelle Server in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b3a4a-146">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3a4a-147"><strong>Pool-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-147"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-148">int</span><span class="sxs-lookup"><span data-stu-id="b3a4a-148">int</span></span></p></td>
<td><p><span data-ttu-id="b3a4a-149">Fremd</span><span class="sxs-lookup"><span data-stu-id="b3a4a-149">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b3a4a-150">Die ID des Pools, in dem die Sitzung erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-150">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="b3a4a-151">Weitere Informationen finden Sie <a href="lync-server-2013-pools-table.md">in der Tabelle Pools in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b3a4a-151">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3a4a-152"><strong>EdgeServerId</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-152"><strong>EdgeServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-153">int</span><span class="sxs-lookup"><span data-stu-id="b3a4a-153">int</span></span></p></td>
<td><p><span data-ttu-id="b3a4a-154">Fremd</span><span class="sxs-lookup"><span data-stu-id="b3a4a-154">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b3a4a-155">Edge-Server die Registrierung wird durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-155">Edge Server the registration is going through.</span></span> <span data-ttu-id="b3a4a-156">Weitere Informationen finden Sie <a href="lync-server-2013-edgeservers-table.md">in der EdgeServers-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b3a4a-156">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3a4a-157"><strong>"IsInternal</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-157"><strong>IsInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-158">Bit</span><span class="sxs-lookup"><span data-stu-id="b3a4a-158">Bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b3a4a-159">Gibt an, ob der Benutzer intern angemeldet ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-159">Whether the user is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3a4a-160"><strong>IsUserServiceAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-160"><strong>IsUserServiceAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-161">bit</span><span class="sxs-lookup"><span data-stu-id="b3a4a-161">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b3a4a-162">Gibt an, ob die UserService verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-162">Whether the UserService is available or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3a4a-163"><strong>IsPrimaryRegistrar</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-163"><strong>IsPrimaryRegistrar</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-164">bit</span><span class="sxs-lookup"><span data-stu-id="b3a4a-164">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b3a4a-165">Ob Sie sich bei der primären Registrierungsstelle registrieren oder nicht.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-165">Whether register to the primary Registrar or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3a4a-166"><strong>IsPrimaryRegistrarCentral</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-166"><strong>IsPrimaryRegistrarCentral</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-167">bit</span><span class="sxs-lookup"><span data-stu-id="b3a4a-167">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b3a4a-168">Gibt an, ob der Benutzer bei einer Survivable Branch-Appliance registriert ist.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-168">Indicates whether or not the user is registered with a survivable branch appliance.</span></span></p>
<p><span data-ttu-id="b3a4a-169">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-169">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3a4a-170"><strong>Registrierung</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-170"><strong>RegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-171">datetime</span><span class="sxs-lookup"><span data-stu-id="b3a4a-171">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b3a4a-172">Registrierungszeit.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-172">Registration time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3a4a-173"><strong>Registrierung</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-173"><strong>DeRegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-174">datetime</span><span class="sxs-lookup"><span data-stu-id="b3a4a-174">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b3a4a-175">De-Registration Zeit.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-175">De-Registration time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3a4a-176"><strong>Response Code</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-176"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-177">int</span><span class="sxs-lookup"><span data-stu-id="b3a4a-177">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b3a4a-178">Antwortcode der Registrierungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-178">Response code of the register request.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3a4a-179"><strong>Diagnose-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-179"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-180">int</span><span class="sxs-lookup"><span data-stu-id="b3a4a-180">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b3a4a-181">Diagnose-ID der Registrierungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-181">Diagnostic ID of the register request.</span></span> <span data-ttu-id="b3a4a-182">Dies gibt an, dass der Typ der diagnostischen Informationen.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-182">This indicates that diagnostic information type.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3a4a-183"><strong>DeviceID</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-183"><strong>DeviceId</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-184">int</span><span class="sxs-lookup"><span data-stu-id="b3a4a-184">int</span></span></p></td>
<td><p><span data-ttu-id="b3a4a-185">Fremd</span><span class="sxs-lookup"><span data-stu-id="b3a4a-185">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b3a4a-186">Das Gerät, von dem die Registrierungsanforderung stammt.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-186">The device that the register request is coming from.</span></span> <span data-ttu-id="b3a4a-187">Weitere Informationen finden Sie <a href="lync-server-2013-devices-table.md">in der Tabelle Devices in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b3a4a-187">See the <a href="lync-server-2013-devices-table.md">Devices table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b3a4a-188"><strong>DeRegisterTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-188"><strong>DeRegisterTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-189">tinyint</span><span class="sxs-lookup"><span data-stu-id="b3a4a-189">tinyint</span></span></p></td>
<td><p><span data-ttu-id="b3a4a-190">Fremd</span><span class="sxs-lookup"><span data-stu-id="b3a4a-190">Foreign</span></span></p></td>
<td><p><span data-ttu-id="b3a4a-191">Der Grund für die Deregistrierung, wie "Benutzer initiiert", "Registrierung abgelaufen", "Client Fehler" und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-191">The reason of de-register, such as ‘user initiated’, ‘registration expired’, ‘client fail’, and more.</span></span> <span data-ttu-id="b3a4a-192">Weitere Informationen finden Sie <a href="lync-server-2013-deregistertype-table.md">in der Tabelle deregistertype in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b3a4a-192">See the <a href="lync-server-2013-deregistertype-table.md">DeRegisterType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b3a4a-193"><strong>IPAddress</strong></span><span class="sxs-lookup"><span data-stu-id="b3a4a-193"><strong>IPAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="b3a4a-194">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b3a4a-194">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="b3a4a-195">Die IP-Adresse des Endpunkts, bei dem der Benutzer registriert ist.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-195">IP address of the endpoint the user registered with.</span></span> <span data-ttu-id="b3a4a-196">Dies kann eine IPv4-Adresse oder eine IPv6-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-196">This can be an IPv4 address or an IPv6 address.</span></span></p>
<p><span data-ttu-id="b3a4a-197">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b3a4a-197">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b3a4a-198">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b3a4a-198">


</div>

<span> </span>

</div>

</div>

</span></span></div>

