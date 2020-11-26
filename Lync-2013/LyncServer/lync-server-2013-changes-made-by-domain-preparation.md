---
title: 'Lync Server 2013: von der Domänenvorbereitung vorgenommene Änderungen'
description: 'Lync Server 2013: Änderungen, die von der Domänenvorbereitung vorgenommen wurden.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by domain preparation
ms:assetid: 9191221e-6166-4c2b-837e-fa73d90fdf80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398742(v=OCS.15)
ms:contentKeyID: 48184845
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 26400bd1c72c6ae3b8dc1f2d2d8f6c6906b80595
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435117"
---
# <a name="changes-made-by-domain-preparation-in-lync-server-2013"></a><span data-ttu-id="3fcf9-103">Von der Domänenvorbereitung in lync Server 2013 vorgenommene Änderungen</span><span class="sxs-lookup"><span data-stu-id="3fcf9-103">Changes made by domain preparation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3fcf9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3fcf9-104">

<span> </span></span></span>

<span data-ttu-id="3fcf9-105">_**Letztes Änderungsdatum des Themas:** 2010-10-18_</span><span class="sxs-lookup"><span data-stu-id="3fcf9-105">_**Topic Last Modified:** 2010-10-18_</span></span>

<span data-ttu-id="3fcf9-106">In der folgenden Tabelle sind die Zugriffssteuerungseinträge (ACEs) aufgeführt, die von der Domänenvorbereitung für den Domänenstamm erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="3fcf9-106">The following table lists the access control entries (ACEs) that domain preparation creates on the domain root.</span></span> <span data-ttu-id="3fcf9-107">Alle ACEs werden geerbt, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="3fcf9-107">All ACEs are inherited unless otherwise noted.</span></span>

<div id="sectionSection0" class="section">

### <a name="aces-added-to-domain-root"></a><span data-ttu-id="3fcf9-108">ACEs, die dem Domänenstamm hinzugefügt wurden</span><span class="sxs-lookup"><span data-stu-id="3fcf9-108">ACEs Added to Domain Root</span></span>

<table style="width:100%;">
<colgroup>
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
<col style="width: 16%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3fcf9-109">ACE</span><span class="sxs-lookup"><span data-stu-id="3fcf9-109">ACE</span></span></th>
<th><span data-ttu-id="3fcf9-110">RTCUniversal-UserReadOnly-Gruppe</span><span class="sxs-lookup"><span data-stu-id="3fcf9-110">RTCUniversal-UserReadOnly-Group</span></span></th>
<th><span data-ttu-id="3fcf9-111">RTCUniversal-ServerReadOnly-Gruppe</span><span class="sxs-lookup"><span data-stu-id="3fcf9-111">RTCUniversal-ServerReadOnly-Group</span></span></th>
<th><span data-ttu-id="3fcf9-112">RTCUniversal-UserAdmins</span><span class="sxs-lookup"><span data-stu-id="3fcf9-112">RTCUniversal-UserAdmins</span></span></th>
<th><span data-ttu-id="3fcf9-113">RTCHSUniversal-Services</span><span class="sxs-lookup"><span data-stu-id="3fcf9-113">RTCHSUniversal-Services</span></span></th>
<th><span data-ttu-id="3fcf9-114">Authenticated-Users</span><span class="sxs-lookup"><span data-stu-id="3fcf9-114">Authenticated-Users</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3fcf9-115">Read-Container (nicht geerbt)</span><span class="sxs-lookup"><span data-stu-id="3fcf9-115">Read Container (not inherited)</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-116"><strong>Ja</strong></span><span class="sxs-lookup"><span data-stu-id="3fcf9-116"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcf9-117"><strong>Ja</strong></span><span class="sxs-lookup"><span data-stu-id="3fcf9-117"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcf9-118">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-118">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-119">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-119">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-120">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-120">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcf9-121">Lesen der Benutzer-PropertySet-Benutzerkonto Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="3fcf9-121">Read User PropertySet User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-122"><strong>Ja</strong></span><span class="sxs-lookup"><span data-stu-id="3fcf9-122"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcf9-123">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-123">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-124">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-124">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-125">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-125">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-126">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-126">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcf9-127">Lesen von User PropertySet Personal-Information</span><span class="sxs-lookup"><span data-stu-id="3fcf9-127">Read User PropertySet Personal-Information</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-128"><strong>Ja</strong></span><span class="sxs-lookup"><span data-stu-id="3fcf9-128"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcf9-129">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-129">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-130">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-130">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-131">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-131">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-132">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-132">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcf9-133">Lesen von User PropertySet General-Information</span><span class="sxs-lookup"><span data-stu-id="3fcf9-133">Read User PropertySet General-Information</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-134"><strong>Ja</strong></span><span class="sxs-lookup"><span data-stu-id="3fcf9-134"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcf9-135">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-135">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-136">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-136">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-137">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-137">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-138">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-138">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcf9-139">Lesen von User PropertySet Public-Information</span><span class="sxs-lookup"><span data-stu-id="3fcf9-139">Read User PropertySet Public-Information</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-140"><strong>Ja</strong></span><span class="sxs-lookup"><span data-stu-id="3fcf9-140"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcf9-141">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-141">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-142">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-142">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-143">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-143">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-144">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-144">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcf9-145">Lesen von User PropertySet RTCUserSearchProperty-Set</span><span class="sxs-lookup"><span data-stu-id="3fcf9-145">Read User PropertySet RTCUserSearchProperty-Set</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-146"><strong>Ja</strong></span><span class="sxs-lookup"><span data-stu-id="3fcf9-146"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcf9-147">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-147">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-148">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-148">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-149">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-149">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-150"><strong>Ja</strong></span><span class="sxs-lookup"><span data-stu-id="3fcf9-150"><strong>Yes</strong></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcf9-151">Read User PropertySet RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="3fcf9-151">Read User PropertySet RTCPropertySet</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-152"><strong>Ja</strong></span><span class="sxs-lookup"><span data-stu-id="3fcf9-152"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcf9-153">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-153">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-154">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-154">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-155">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-155">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-156">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-156">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcf9-157">Benutzereigenschaft schreiben Proxy-Addresses</span><span class="sxs-lookup"><span data-stu-id="3fcf9-157">Write User Property Proxy-Addresses</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-158">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-158">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-159">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-159">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-160"><strong>Ja</strong></span><span class="sxs-lookup"><span data-stu-id="3fcf9-160"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcf9-161">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-161">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-162">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-162">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcf9-163">Schreiben von Benutzer Eigenschafts RTCUserSearchProperty-Set</span><span class="sxs-lookup"><span data-stu-id="3fcf9-163">Write User PropertySet RTCUserSearchProperty-Set</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-164">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-164">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-165">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-165">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-166"><strong>Ja</strong></span><span class="sxs-lookup"><span data-stu-id="3fcf9-166"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcf9-167">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-167">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-168">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-168">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3fcf9-169">Schreiben von Benutzer-PropertySet-RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="3fcf9-169">Write User PropertySet RTCPropertySet</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-170">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-170">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-171">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-171">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-172"><strong>Ja</strong></span><span class="sxs-lookup"><span data-stu-id="3fcf9-172"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcf9-173">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-173">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-174">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-174">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3fcf9-175">Lesen von PropertySet DS-Replikation-abrufen – Änderungen aller Active Directory-Objekte</span><span class="sxs-lookup"><span data-stu-id="3fcf9-175">Read PropertySet DS-Replication-Get-Changes of all Active Directory objects</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-176">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-176">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-177">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-177">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-178">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-178">No</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-179"><strong>Ja</strong></span><span class="sxs-lookup"><span data-stu-id="3fcf9-179"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcf9-180">Nein</span><span class="sxs-lookup"><span data-stu-id="3fcf9-180">No</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3fcf9-181">In der folgenden Tabelle sind die ACEs aufgeführt, die von der Domänenvorbereitung in den drei integrierten Containern erstellt werden: Benutzer, Computer und Domänencontroller.</span><span class="sxs-lookup"><span data-stu-id="3fcf9-181">The following table lists the ACEs that domain preparation creates in the three built-in containers: Users, Computers, and Domain Controllers.</span></span> <span data-ttu-id="3fcf9-182">Alle ACEs werden geerbt, sofern nicht anders angegeben.</span><span class="sxs-lookup"><span data-stu-id="3fcf9-182">All ACEs are inherited unless otherwise noted.</span></span>

### <a name="aces-added-to-built-in-containers"></a><span data-ttu-id="3fcf9-183">ACEs, die zu integrierten Containern hinzugefügt wurden</span><span class="sxs-lookup"><span data-stu-id="3fcf9-183">ACEs Added to Built-in Containers</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3fcf9-184">ACE</span><span class="sxs-lookup"><span data-stu-id="3fcf9-184">ACE</span></span></th>
<th><span data-ttu-id="3fcf9-185">RTCUniversal-UserReadOnly-Gruppe</span><span class="sxs-lookup"><span data-stu-id="3fcf9-185">RTCUniversal-UserReadOnly-Group</span></span></th>
<th><span data-ttu-id="3fcf9-186">RTCUniversal-ServerReadOnly-Gruppe</span><span class="sxs-lookup"><span data-stu-id="3fcf9-186">RTCUniversal-ServerReadOnly-Group</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3fcf9-187">Read-Container (nicht geerbt)</span><span class="sxs-lookup"><span data-stu-id="3fcf9-187">Read Container (not inherited)</span></span></p></td>
<td><p><span data-ttu-id="3fcf9-188"><strong>Ja</strong></span><span class="sxs-lookup"><span data-stu-id="3fcf9-188"><strong>Yes</strong></span></span></p></td>
<td><p><span data-ttu-id="3fcf9-189"><strong>Ja</strong></span><span class="sxs-lookup"><span data-stu-id="3fcf9-189"><strong>Yes</strong></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3fcf9-190">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3fcf9-190">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

