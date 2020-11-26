---
title: 'Lync Server 2013: tblPrincipal'
description: 'Lync Server 2013: tblPrincipal.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipal
ms:assetid: 79a24502-b4ce-41f0-8979-8caddf535338
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558667(v=OCS.15)
ms:contentKeyID: 48184571
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f07b37ac4c8ceed5c044b5c263eeee6370adfdc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444413"
---
# <a name="tblprincipal-in-lync-server-2013"></a><span data-ttu-id="faa28-103">tblPrincipal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="faa28-103">tblPrincipal in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="faa28-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="faa28-104">

<span> </span></span></span>

<span data-ttu-id="faa28-105">_**Letztes Änderungsdatum des Themas:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="faa28-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="faa28-106">tblPrincipal enthält alle Prinzipale, einschließlich Benutzern, Ordnern und Gruppen.</span><span class="sxs-lookup"><span data-stu-id="faa28-106">tblPrincipal contains all principals, including users, folders, and groups.</span></span>

### <a name="columns"></a><span data-ttu-id="faa28-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="faa28-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="faa28-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="faa28-108">Column</span></span></th>
<th><span data-ttu-id="faa28-109">Typ</span><span class="sxs-lookup"><span data-stu-id="faa28-109">Type</span></span></th>
<th><span data-ttu-id="faa28-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="faa28-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa28-111">prinID</span><span class="sxs-lookup"><span data-stu-id="faa28-111">prinID</span></span></p></td>
<td><p><span data-ttu-id="faa28-112">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="faa28-112">int, not null</span></span></p></td>
<td><p><span data-ttu-id="faa28-113">Prinzipal-ID.</span><span class="sxs-lookup"><span data-stu-id="faa28-113">Principal ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa28-114">prinGuid</span><span class="sxs-lookup"><span data-stu-id="faa28-114">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="faa28-115">GUID, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="faa28-115">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="faa28-116">Prinzipal-GUID.</span><span class="sxs-lookup"><span data-stu-id="faa28-116">Principal GUID.</span></span> <span data-ttu-id="faa28-117">Dies wird im Allgemeinen als alternativer Primärschlüssel verwendet, da dessen Bedeutung in den Bereich der Active Directory-Domänendienste überschritten wird.</span><span class="sxs-lookup"><span data-stu-id="faa28-117">This is broadly used as an alternate primary key because its meaning crosses over into the Active Directory Domain Services space.</span></span> <span data-ttu-id="faa28-118">(Die GUID für einen zwischengespeicherten Prinzipal entspricht der entsprechenden GUID des Active Directory-Objekts.)</span><span class="sxs-lookup"><span data-stu-id="faa28-118">(The GUID for a cached principal is equal to the corresponding Active Directory object GUID.)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa28-119">prinUri</span><span class="sxs-lookup"><span data-stu-id="faa28-119">prinUri</span></span></p></td>
<td><p><span data-ttu-id="faa28-120">nvarchar (256); nicht NULL</span><span class="sxs-lookup"><span data-stu-id="faa28-120">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="faa28-121">Prinzipal-URI.</span><span class="sxs-lookup"><span data-stu-id="faa28-121">Principal URI.</span></span> <span data-ttu-id="faa28-122">Das SIP-Schema wird für Benutzer verwendet, und MA-GRP wird für fast alles andere verwendet.</span><span class="sxs-lookup"><span data-stu-id="faa28-122">The SIP scheme is used for users, and ma-grp is used for almost everything else.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa28-123">prinName</span><span class="sxs-lookup"><span data-stu-id="faa28-123">prinName</span></span></p></td>
<td><p><span data-ttu-id="faa28-124">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="faa28-124">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="faa28-125">Allgemeiner Name</span><span class="sxs-lookup"><span data-stu-id="faa28-125">Common name.</span></span> <span data-ttu-id="faa28-126">Wird nur von Benutzertypen verwendet.</span><span class="sxs-lookup"><span data-stu-id="faa28-126">Used only by user types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa28-127">prinDisplayName</span><span class="sxs-lookup"><span data-stu-id="faa28-127">prinDisplayName</span></span></p></td>
<td><p><span data-ttu-id="faa28-128">Nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="faa28-128">Nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="faa28-129">Anzeigename</span><span class="sxs-lookup"><span data-stu-id="faa28-129">Display name.</span></span> <span data-ttu-id="faa28-130">Wird nur von Benutzertypen verwendet.</span><span class="sxs-lookup"><span data-stu-id="faa28-130">Used only by user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa28-131">prinCompanyName</span><span class="sxs-lookup"><span data-stu-id="faa28-131">prinCompanyName</span></span></p></td>
<td><p><span data-ttu-id="faa28-132">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="faa28-132">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="faa28-133">Name des Unternehmens.</span><span class="sxs-lookup"><span data-stu-id="faa28-133">Company name.</span></span> <span data-ttu-id="faa28-134">Wird nur von Benutzertypen verwendet.</span><span class="sxs-lookup"><span data-stu-id="faa28-134">Used only by user types.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa28-135">prinEmail</span><span class="sxs-lookup"><span data-stu-id="faa28-135">prinEmail</span></span></p></td>
<td><p><span data-ttu-id="faa28-136">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="faa28-136">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="faa28-137">E-Mail.</span><span class="sxs-lookup"><span data-stu-id="faa28-137">Email.</span></span> <span data-ttu-id="faa28-138">Wird nur von Benutzertypen verwendet.</span><span class="sxs-lookup"><span data-stu-id="faa28-138">Used only by user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa28-139">prinADPath</span><span class="sxs-lookup"><span data-stu-id="faa28-139">prinADPath</span></span></p></td>
<td><p><span data-ttu-id="faa28-140">nvarchar (384)</span><span class="sxs-lookup"><span data-stu-id="faa28-140">nvarchar (384)</span></span></p></td>
<td><p><span data-ttu-id="faa28-141">Der Domänenname des Active Directory-Objekts, in dem der Prinzipal eine zwischengespeicherte Version von ist.</span><span class="sxs-lookup"><span data-stu-id="faa28-141">Domain name of the Active Directory object that the principal is a cached version of.</span></span> <span data-ttu-id="faa28-142">Kann NULL für Typen sein, die keine Active Directory-Objekte (wie Systembenutzer) sind.</span><span class="sxs-lookup"><span data-stu-id="faa28-142">Can be Null for types that are not Active Directory objects (such as system users).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa28-143">prinADUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="faa28-143">prinADUserPrincipalName</span></span></p></td>
<td><p><span data-ttu-id="faa28-144">nvarchar (256)</span><span class="sxs-lookup"><span data-stu-id="faa28-144">nvarchar (256)</span></span></p></td>
<td><p><span data-ttu-id="faa28-145">Benutzerprinzipalname (User Principal Name, UPN) des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="faa28-145">User’s user principal name (UPN).</span></span> <span data-ttu-id="faa28-146">Wird nur von normalen Benutzertypen verwendet.</span><span class="sxs-lookup"><span data-stu-id="faa28-146">Used only by regular user types.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa28-147">prinDisabled</span><span class="sxs-lookup"><span data-stu-id="faa28-147">prinDisabled</span></span></p></td>
<td><p><span data-ttu-id="faa28-148">smallint, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="faa28-148">smallint, not null</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="faa28-149">0: Principal ist aktiv.</span><span class="sxs-lookup"><span data-stu-id="faa28-149">0: Principal is active.</span></span></p></li>
<li><p><span data-ttu-id="faa28-150">1: Principal ist deaktiviert, da die SIP-Funktionen des Benutzers deaktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="faa28-150">1: Principal is disabled because user’s SIP capabilities are disabled.</span></span></p></li>
<li><p><span data-ttu-id="faa28-151">2: Principal wird gelöscht, weil das zugeordnete anzeigen Objekt gelöscht wurde.</span><span class="sxs-lookup"><span data-stu-id="faa28-151">2: Principal is deleted because associated AD object has been deleted.</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa28-152">prinTypeID</span><span class="sxs-lookup"><span data-stu-id="faa28-152">prinTypeID</span></span></p></td>
<td><p><span data-ttu-id="faa28-153">smallint, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="faa28-153">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="faa28-154">Principal Type (aus tblPrincipalType-Tabelle).</span><span class="sxs-lookup"><span data-stu-id="faa28-154">Principal type (from tblPrincipalType table).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa28-155">prinPoolID</span><span class="sxs-lookup"><span data-stu-id="faa28-155">prinPoolID</span></span></p></td>
<td><p><span data-ttu-id="faa28-156">Int</span><span class="sxs-lookup"><span data-stu-id="faa28-156">Int</span></span></p></td>
<td><p><span data-ttu-id="faa28-157">Lync-Pool Aufgabe für den Prinzipal.</span><span class="sxs-lookup"><span data-stu-id="faa28-157">Lync pool assignment for the principal.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa28-158">prinPolicyID</span><span class="sxs-lookup"><span data-stu-id="faa28-158">prinPolicyID</span></span></p></td>
<td><p><span data-ttu-id="faa28-159">Int</span><span class="sxs-lookup"><span data-stu-id="faa28-159">Int</span></span></p></td>
<td><p><span data-ttu-id="faa28-160">Server Richtlinienwert des beständigen Chats für Benutzer, wenn die Kategorie-typrichtlinie vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="faa28-160">Persistent Chat Server policy value for user, if tag type policy is present.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa28-161">prinAddedBy</span><span class="sxs-lookup"><span data-stu-id="faa28-161">prinAddedBy</span></span></p></td>
<td><p><span data-ttu-id="faa28-162">int</span><span class="sxs-lookup"><span data-stu-id="faa28-162">int</span></span></p></td>
<td><p><span data-ttu-id="faa28-163">Prinzipal-ID des Erstellers.</span><span class="sxs-lookup"><span data-stu-id="faa28-163">Principal ID of the creator.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa28-164">prinAddedOn</span><span class="sxs-lookup"><span data-stu-id="faa28-164">prinAddedOn</span></span></p></td>
<td><p><span data-ttu-id="faa28-165">bigint, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="faa28-165">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="faa28-166">Zeitstempel für die Erstellungszeit.</span><span class="sxs-lookup"><span data-stu-id="faa28-166">Time stamp for the creation time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa28-167">prinUpdatedBy</span><span class="sxs-lookup"><span data-stu-id="faa28-167">prinUpdatedBy</span></span></p></td>
<td><p><span data-ttu-id="faa28-168">int</span><span class="sxs-lookup"><span data-stu-id="faa28-168">int</span></span></p></td>
<td><p><span data-ttu-id="faa28-169">Die ID des Prinzipals, der diesen zuletzt aktualisiert hat.</span><span class="sxs-lookup"><span data-stu-id="faa28-169">ID of the principal that last updated this.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="faa28-170">prinUpdatedOn</span><span class="sxs-lookup"><span data-stu-id="faa28-170">prinUpdatedOn</span></span></p></td>
<td><p><span data-ttu-id="faa28-171">bigint, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="faa28-171">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="faa28-172">Zeitstempel für das letzte Update.</span><span class="sxs-lookup"><span data-stu-id="faa28-172">Time stamp for the last update.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa28-173">prinVerifiedOn</span><span class="sxs-lookup"><span data-stu-id="faa28-173">prinVerifiedOn</span></span></p></td>
<td><p><span data-ttu-id="faa28-174">DateTime, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="faa28-174">datetime, not null</span></span></p></td>
<td><p><span data-ttu-id="faa28-175">Datum und Uhrzeit der letzten Aktualisierung der Active Directory-Synchronisierung für den Prinzipal.</span><span class="sxs-lookup"><span data-stu-id="faa28-175">Date and time of the last Active Directory Sync refresh for the principal.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="faa28-176">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="faa28-176">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="faa28-177">Spalte</span><span class="sxs-lookup"><span data-stu-id="faa28-177">Column</span></span></th>
<th><span data-ttu-id="faa28-178">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="faa28-178">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="faa28-179">prinID</span><span class="sxs-lookup"><span data-stu-id="faa28-179">prinID</span></span></p></td>
<td><p><span data-ttu-id="faa28-180">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="faa28-180">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="faa28-181">prinTypeID</span><span class="sxs-lookup"><span data-stu-id="faa28-181">prinTypeID</span></span></p></td>
<td><p><span data-ttu-id="faa28-182">Fremdschlüssel mit Lookup in der tblPrincipalType. ptypeID-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="faa28-182">Foreign key with lookup in tblPrincipalType.ptypeID table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="faa28-183">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="faa28-183">


</div>

<span> </span>

</div>

</div>

</span></span></div>

