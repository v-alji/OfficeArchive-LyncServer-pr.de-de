---
title: 'Lync Server 2013: von Grant-CsOUPermission vorgenommene Änderungen'
description: 'Lync Server 2013: von Grant-CsOUPermission vorgenommene Änderungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by Grant-CsOUPermission
ms:assetid: d744d352-1ad9-4447-8e2b-28e768d2ed1b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205310(v=OCS.15)
ms:contentKeyID: 48185564
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 10d3db0e9dde380628690bc016e2b4bd2ec85b54
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435054"
---
# <a name="changes-made-by-grant-csoupermission-in-lync-server-2013"></a><span data-ttu-id="56514-103">Von Grant-CsOUPermission in lync Server 2013 vorgenommene Änderungen</span><span class="sxs-lookup"><span data-stu-id="56514-103">Changes made by Grant-CsOUPermission in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="56514-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="56514-104">

<span> </span></span></span>

<span data-ttu-id="56514-105">_**Letztes Änderungsdatum des Themas:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="56514-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="56514-106">Wenn Sie die Verwaltung von lync Server 2013 delegieren möchten, können Sie den angegebenen Organisationseinheiten Berechtigungen hinzufügen, sodass Mitglieder der von der Gesamtstrukturvorbereitung erstellten RTC universelle Gruppen auf die OUs zugreifen können, ohne Mitglieder der Gruppe der Domänenadministratoren zu sein.</span><span class="sxs-lookup"><span data-stu-id="56514-106">To delegate Lync Server 2013 administration, you can add permissions to specified organizational units (OUs) so that members of the RTC universal groups created by forest preparation can access the OUs without being members of the Domain Admins group.</span></span>

<span data-ttu-id="56514-107">Das Cmdlet **Grant-CsOuPermission** gewährt den Objekten in der angegebenen OU Berechtigungen, wie in den folgenden Tabellen angegeben.</span><span class="sxs-lookup"><span data-stu-id="56514-107">The **Grant-CsOuPermission** cmdlet grants permissions to objects in the specified OU as specified in the following tables.</span></span>

<div>

## <a name="granting-permission-for-user-objects"></a><span data-ttu-id="56514-108">Erteilen der Berechtigung für Benutzerobjekte</span><span class="sxs-lookup"><span data-stu-id="56514-108">Granting Permission for User Objects</span></span>

<span data-ttu-id="56514-109">Wenn Sie das **Grant-CsOuPermission-** Cmdlet für Benutzerobjekte in einer OU ausführen, werden Gruppen Berechtigungen gewährt, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="56514-109">When you run the **Grant-CsOuPermission** cmdlet for User objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-user-objects"></a><span data-ttu-id="56514-110">Für Benutzerobjekte gewährte Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="56514-110">Permissions Granted for User Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="56514-111">Gruppe</span><span class="sxs-lookup"><span data-stu-id="56514-111">Group</span></span></th>
<th><span data-ttu-id="56514-112">Berechtigungs</span><span class="sxs-lookup"><span data-stu-id="56514-112">Permission</span></span></th>
<th><span data-ttu-id="56514-113">Gilt für</span><span class="sxs-lookup"><span data-stu-id="56514-113">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56514-114">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="56514-114">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="56514-115">Replizieren von Verzeichnisänderungen</span><span class="sxs-lookup"><span data-stu-id="56514-115">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="56514-116">Nur dieses Objekt</span><span class="sxs-lookup"><span data-stu-id="56514-116">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56514-117">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="56514-117">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="56514-118">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="56514-118">List contents</span></span></p>
<p><span data-ttu-id="56514-119">Alle Eigenschaften lesen</span><span class="sxs-lookup"><span data-stu-id="56514-119">Read all properties</span></span></p>
<p><span data-ttu-id="56514-120">Leseberechtigungen</span><span class="sxs-lookup"><span data-stu-id="56514-120">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="56514-121">Nur dieses Objekt</span><span class="sxs-lookup"><span data-stu-id="56514-121">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56514-122">RTCUniversalUserReadOnlyGroup hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="56514-122">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="56514-123">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="56514-123">List contents</span></span></p>
<p><span data-ttu-id="56514-124">Alle Eigenschaften lesen</span><span class="sxs-lookup"><span data-stu-id="56514-124">Read all properties</span></span></p>
<p><span data-ttu-id="56514-125">Leseberechtigungen</span><span class="sxs-lookup"><span data-stu-id="56514-125">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="56514-126">Nur dieses Objekt</span><span class="sxs-lookup"><span data-stu-id="56514-126">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56514-127">RTCUniversalUserReadOnlyGroup hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="56514-127">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="56514-128">Lesen von RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-128">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="56514-129">Lesen von RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-129">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="56514-130">Lesen von RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-130">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="56514-131">Lesen Public-Information</span><span class="sxs-lookup"><span data-stu-id="56514-131">Read Public-Information</span></span></p>
<p><span data-ttu-id="56514-132">Lesen General-Information</span><span class="sxs-lookup"><span data-stu-id="56514-132">Read General-Information</span></span></p>
<p><span data-ttu-id="56514-133">Lesen von Benutzerkonto Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="56514-133">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="56514-134">Nachfolger Benutzerobjekte</span><span class="sxs-lookup"><span data-stu-id="56514-134">Descendant User objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56514-135">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="56514-135">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="56514-136">Schreiben von RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-136">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="56514-137">Schreiben von msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="56514-137">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="56514-138">Schreiben von RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-138">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="56514-139">Schreiben von RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-139">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="56514-140">Schreiben von proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="56514-140">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="56514-141">Nachfolger Benutzerobjekte</span><span class="sxs-lookup"><span data-stu-id="56514-141">Descendant User objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-computer-objects"></a><span data-ttu-id="56514-142">Erteilen der Berechtigung für Computer Objekte</span><span class="sxs-lookup"><span data-stu-id="56514-142">Granting Permission for Computer Objects</span></span>

<span data-ttu-id="56514-143">Wenn Sie das **Grant-CsOuPermission-** Cmdlet für Computer Objekte in einer OU ausführen, werden Gruppen Berechtigungen gewährt, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="56514-143">When you run the **Grant-CsOuPermission** cmdlet for Computer objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-computer-objects"></a><span data-ttu-id="56514-144">Für Computer Objekte gewährte Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="56514-144">Permissions Granted for Computer Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="56514-145">Gruppe</span><span class="sxs-lookup"><span data-stu-id="56514-145">Group</span></span></th>
<th><span data-ttu-id="56514-146">Berechtigungs</span><span class="sxs-lookup"><span data-stu-id="56514-146">Permission</span></span></th>
<th><span data-ttu-id="56514-147">Gilt für</span><span class="sxs-lookup"><span data-stu-id="56514-147">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56514-148">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="56514-148">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="56514-149">Replizieren von Verzeichnisänderungen</span><span class="sxs-lookup"><span data-stu-id="56514-149">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="56514-150">Nur dieses Objekt</span><span class="sxs-lookup"><span data-stu-id="56514-150">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56514-151">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="56514-151">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="56514-152">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="56514-152">List contents</span></span></p>
<p><span data-ttu-id="56514-153">Alle Eigenschaften lesen</span><span class="sxs-lookup"><span data-stu-id="56514-153">Read all properties</span></span></p>
<p><span data-ttu-id="56514-154">Leseberechtigungen</span><span class="sxs-lookup"><span data-stu-id="56514-154">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="56514-155">Nur dieses Objekt</span><span class="sxs-lookup"><span data-stu-id="56514-155">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56514-156">RTCUniversalUserReadOnlyGroup hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="56514-156">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="56514-157">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="56514-157">List contents</span></span></p>
<p><span data-ttu-id="56514-158">Alle Eigenschaften lesen</span><span class="sxs-lookup"><span data-stu-id="56514-158">Read all properties</span></span></p>
<p><span data-ttu-id="56514-159">Leseberechtigungen</span><span class="sxs-lookup"><span data-stu-id="56514-159">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="56514-160">Nur dieses Objekt</span><span class="sxs-lookup"><span data-stu-id="56514-160">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56514-161">RTCUniversalUserReadOnlyGroup hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="56514-161">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="56514-162">Lesen Public-Information</span><span class="sxs-lookup"><span data-stu-id="56514-162">Read Public-Information</span></span></p>
<p><span data-ttu-id="56514-163">Read validiert-DNS-Host-Name</span><span class="sxs-lookup"><span data-stu-id="56514-163">Read Validated-DNS-Host-Name</span></span></p></td>
<td><p><span data-ttu-id="56514-164">Nachfolger Computer Objekte</span><span class="sxs-lookup"><span data-stu-id="56514-164">Descendant Computer objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56514-165">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="56514-165">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="56514-166">Lesen Public-Information</span><span class="sxs-lookup"><span data-stu-id="56514-166">Read Public-Information</span></span></p>
<p><span data-ttu-id="56514-167">Read validiert-DNS-Host-Name</span><span class="sxs-lookup"><span data-stu-id="56514-167">Read Validated-DNS-Host-Name</span></span></p></td>
<td><p><span data-ttu-id="56514-168">Nachfolger Computer Objekte</span><span class="sxs-lookup"><span data-stu-id="56514-168">Descendant Computer objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-contact-or-appcontact-objects"></a><span data-ttu-id="56514-169">Erteilen der Berechtigung für Kontakt-oder AppContact-Objekte</span><span class="sxs-lookup"><span data-stu-id="56514-169">Granting Permission for Contact or AppContact Objects</span></span>

<span data-ttu-id="56514-170">Wenn Sie das **Grant-CsOuPermission-** Cmdlet für Contact-Objekte oder AppContact-Objekte in einer OU ausführen, werden Gruppen Berechtigungen gewährt, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="56514-170">When you run the **Grant-CsOuPermission** cmdlet for Contact objects or AppContact objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-contact-or-appcontact-objects"></a><span data-ttu-id="56514-171">Für Contact-oder AppContact-Objekte gewährte Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="56514-171">Permissions Granted for Contact or AppContact Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="56514-172">Gruppe</span><span class="sxs-lookup"><span data-stu-id="56514-172">Group</span></span></th>
<th><span data-ttu-id="56514-173">Berechtigungs</span><span class="sxs-lookup"><span data-stu-id="56514-173">Permission</span></span></th>
<th><span data-ttu-id="56514-174">Gilt für</span><span class="sxs-lookup"><span data-stu-id="56514-174">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56514-175">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="56514-175">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="56514-176">Replizieren von Verzeichnisänderungen</span><span class="sxs-lookup"><span data-stu-id="56514-176">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="56514-177">Nur dieses Objekt</span><span class="sxs-lookup"><span data-stu-id="56514-177">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56514-178">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="56514-178">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="56514-179">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="56514-179">List contents</span></span></p>
<p><span data-ttu-id="56514-180">Alle Eigenschaften lesen</span><span class="sxs-lookup"><span data-stu-id="56514-180">Read all properties</span></span></p>
<p><span data-ttu-id="56514-181">Leseberechtigungen</span><span class="sxs-lookup"><span data-stu-id="56514-181">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="56514-182">Nur dieses Objekt</span><span class="sxs-lookup"><span data-stu-id="56514-182">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56514-183">RTCUniversalUserReadOnlyGroup hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="56514-183">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="56514-184">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="56514-184">List contents</span></span></p>
<p><span data-ttu-id="56514-185">Alle Eigenschaften lesen</span><span class="sxs-lookup"><span data-stu-id="56514-185">Read all properties</span></span></p>
<p><span data-ttu-id="56514-186">Leseberechtigungen</span><span class="sxs-lookup"><span data-stu-id="56514-186">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="56514-187">Nur dieses Objekt</span><span class="sxs-lookup"><span data-stu-id="56514-187">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56514-188">RTCUniversalUserReadOnlyGroup hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="56514-188">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="56514-189">Lesen von RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-189">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="56514-190">Lesen von RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-190">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="56514-191">Lesen von RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-191">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="56514-192">Lesen Public-Information</span><span class="sxs-lookup"><span data-stu-id="56514-192">Read Public-Information</span></span></p>
<p><span data-ttu-id="56514-193">Lesen General-Information</span><span class="sxs-lookup"><span data-stu-id="56514-193">Read General-Information</span></span></p>
<p><span data-ttu-id="56514-194">Lesen Personal-Information</span><span class="sxs-lookup"><span data-stu-id="56514-194">Read Personal-Information</span></span></p>
<p><span data-ttu-id="56514-195">Lesen von Benutzerkonto Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="56514-195">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="56514-196">Nachfolger-Kontaktobjekte</span><span class="sxs-lookup"><span data-stu-id="56514-196">Descendant Contact objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56514-197">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="56514-197">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="56514-198">Schreiben von RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-198">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="56514-199">Schreiben von otherIpPhone</span><span class="sxs-lookup"><span data-stu-id="56514-199">Write otherIpPhone</span></span></p>
<p><span data-ttu-id="56514-200">Schreiben von DisplayName</span><span class="sxs-lookup"><span data-stu-id="56514-200">Write displayName</span></span></p>
<p><span data-ttu-id="56514-201">Beschreibung schreiben</span><span class="sxs-lookup"><span data-stu-id="56514-201">Write description</span></span></p>
<p><span data-ttu-id="56514-202">Schreiben von telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="56514-202">Write telephoneNumber</span></span></p>
<p><span data-ttu-id="56514-203">Schreiben von msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="56514-203">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="56514-204">Schreiben von RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-204">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="56514-205">Schreiben von RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-205">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="56514-206">Schreiben von proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="56514-206">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="56514-207">Nachfolger-Kontaktobjekte</span><span class="sxs-lookup"><span data-stu-id="56514-207">Descendant Contact objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-device-objects"></a><span data-ttu-id="56514-208">Erteilen der Berechtigung für Geräteobjekte</span><span class="sxs-lookup"><span data-stu-id="56514-208">Granting Permission for Device Objects</span></span>

<span data-ttu-id="56514-209">Wenn Sie das **Grant-CsOuPermission-** Cmdlet für Geräteobjekte in einer OU ausführen, werden Gruppen Berechtigungen gewährt, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="56514-209">When you run the **Grant-CsOuPermission** cmdlet for Device objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-device-objects"></a><span data-ttu-id="56514-210">Für Geräteobjekte gewährte Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="56514-210">Permissions Granted for Device Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="56514-211">Gruppe</span><span class="sxs-lookup"><span data-stu-id="56514-211">Group</span></span></th>
<th><span data-ttu-id="56514-212">Berechtigungs</span><span class="sxs-lookup"><span data-stu-id="56514-212">Permission</span></span></th>
<th><span data-ttu-id="56514-213">Gilt für</span><span class="sxs-lookup"><span data-stu-id="56514-213">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56514-214">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="56514-214">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="56514-215">Replizieren von Verzeichnisänderungen</span><span class="sxs-lookup"><span data-stu-id="56514-215">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="56514-216">Nur dieses Objekt</span><span class="sxs-lookup"><span data-stu-id="56514-216">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56514-217">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="56514-217">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="56514-218">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="56514-218">List contents</span></span></p>
<p><span data-ttu-id="56514-219">Alle Eigenschaften lesen</span><span class="sxs-lookup"><span data-stu-id="56514-219">Read all properties</span></span></p>
<p><span data-ttu-id="56514-220">Leseberechtigungen</span><span class="sxs-lookup"><span data-stu-id="56514-220">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="56514-221">Nur dieses Objekt</span><span class="sxs-lookup"><span data-stu-id="56514-221">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56514-222">RTCUniversalUserReadOnlyGroup hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="56514-222">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="56514-223">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="56514-223">List contents</span></span></p>
<p><span data-ttu-id="56514-224">Alle Eigenschaften lesen</span><span class="sxs-lookup"><span data-stu-id="56514-224">Read all properties</span></span></p>
<p><span data-ttu-id="56514-225">Leseberechtigungen</span><span class="sxs-lookup"><span data-stu-id="56514-225">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="56514-226">Nur dieses Objekt</span><span class="sxs-lookup"><span data-stu-id="56514-226">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56514-227">RTCUniversalUserReadOnlyGroup hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="56514-227">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="56514-228">Lesen von RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-228">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="56514-229">Lesen von RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-229">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="56514-230">Lesen von RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-230">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="56514-231">Lesen Public-Information</span><span class="sxs-lookup"><span data-stu-id="56514-231">Read Public-Information</span></span></p>
<p><span data-ttu-id="56514-232">Lesen Personal-Information</span><span class="sxs-lookup"><span data-stu-id="56514-232">Read Personal-Information</span></span></p>
<p><span data-ttu-id="56514-233">Lesen General-Information</span><span class="sxs-lookup"><span data-stu-id="56514-233">Read General-Information</span></span></p>
<p><span data-ttu-id="56514-234">Lesen von Benutzerkonto Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="56514-234">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="56514-235">Nachfolger-Kontaktobjekte</span><span class="sxs-lookup"><span data-stu-id="56514-235">Descendant Contact objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56514-236">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="56514-236">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="56514-237">Erstellen eines untergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="56514-237">Create child</span></span></p>
<p><span data-ttu-id="56514-238">Untergeordnetes Element löschen</span><span class="sxs-lookup"><span data-stu-id="56514-238">Delete child</span></span></p>
<p><span data-ttu-id="56514-239">Struktur löschen</span><span class="sxs-lookup"><span data-stu-id="56514-239">Delete tree</span></span></p></td>
<td><p><span data-ttu-id="56514-240">Kontakt</span><span class="sxs-lookup"><span data-stu-id="56514-240">Contact</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56514-241">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="56514-241">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="56514-242">Schreiben von DisplayName</span><span class="sxs-lookup"><span data-stu-id="56514-242">Write displayName</span></span></p>
<p><span data-ttu-id="56514-243">Beschreibung schreiben</span><span class="sxs-lookup"><span data-stu-id="56514-243">Write description</span></span></p>
<p><span data-ttu-id="56514-244">Schreiben von telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="56514-244">Write telephoneNumber</span></span></p></td>
<td><p><span data-ttu-id="56514-245">Nachfolger Benutzerobjekte</span><span class="sxs-lookup"><span data-stu-id="56514-245">Descendant User objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56514-246">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="56514-246">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="56514-247">Schreiben von RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-247">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="56514-248">Schreiben von otherIpPhone</span><span class="sxs-lookup"><span data-stu-id="56514-248">Write otherIpPhone</span></span></p>
<p><span data-ttu-id="56514-249">Schreiben von DisplayName</span><span class="sxs-lookup"><span data-stu-id="56514-249">Write displayName</span></span></p>
<p><span data-ttu-id="56514-250">Beschreibung schreiben</span><span class="sxs-lookup"><span data-stu-id="56514-250">Write description</span></span></p>
<p><span data-ttu-id="56514-251">Schreiben von telephoneNumber</span><span class="sxs-lookup"><span data-stu-id="56514-251">Write telephoneNumber</span></span></p>
<p><span data-ttu-id="56514-252">Schreiben von msExchUCVoiceMailSettings</span><span class="sxs-lookup"><span data-stu-id="56514-252">Write msExchUCVoiceMailSettings</span></span></p>
<p><span data-ttu-id="56514-253">Schreiben von RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-253">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="56514-254">Schreiben von RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-254">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="56514-255">Schreiben von proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="56514-255">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="56514-256">Nachfolger-Kontaktobjekte</span><span class="sxs-lookup"><span data-stu-id="56514-256">Descendant Contact objects</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="granting-permission-for-inetorgperson-objects"></a><span data-ttu-id="56514-257">Erteilen der Berechtigung für InetOrgPerson-Objekte</span><span class="sxs-lookup"><span data-stu-id="56514-257">Granting Permission for InetOrgPerson Objects</span></span>

<span data-ttu-id="56514-258">Wenn Sie das **Grant-CsOuPermission-** Cmdlet für InetOrgPerson-Objekte in einer OU ausführen, werden Gruppen Berechtigungen gewährt, wie in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="56514-258">When you run the **Grant-CsOuPermission** cmdlet for InetOrgPerson objects on an OU, groups are granted permissions as shown in the following table.</span></span>

### <a name="permissions-granted-for-inetorgperson-objects"></a><span data-ttu-id="56514-259">Für InetOrgPerson-Objekte gewährte Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="56514-259">Permissions Granted for InetOrgPerson Objects</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="56514-260">Gruppe</span><span class="sxs-lookup"><span data-stu-id="56514-260">Group</span></span></th>
<th><span data-ttu-id="56514-261">Berechtigungs</span><span class="sxs-lookup"><span data-stu-id="56514-261">Permission</span></span></th>
<th><span data-ttu-id="56514-262">Gilt für</span><span class="sxs-lookup"><span data-stu-id="56514-262">Applies to</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56514-263">RTCHSUniversalServices</span><span class="sxs-lookup"><span data-stu-id="56514-263">RTCHSUniversalServices</span></span></p></td>
<td><p><span data-ttu-id="56514-264">Replizieren von Verzeichnisänderungen</span><span class="sxs-lookup"><span data-stu-id="56514-264">Replicating directory changes</span></span></p></td>
<td><p><span data-ttu-id="56514-265">Nur dieses Objekt</span><span class="sxs-lookup"><span data-stu-id="56514-265">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56514-266">RTCUniversalServerReadOnlyGroup</span><span class="sxs-lookup"><span data-stu-id="56514-266">RTCUniversalServerReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="56514-267">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="56514-267">List contents</span></span></p>
<p><span data-ttu-id="56514-268">Alle Eigenschaften lesen</span><span class="sxs-lookup"><span data-stu-id="56514-268">Read all properties</span></span></p>
<p><span data-ttu-id="56514-269">Leseberechtigungen</span><span class="sxs-lookup"><span data-stu-id="56514-269">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="56514-270">Nur dieses Objekt</span><span class="sxs-lookup"><span data-stu-id="56514-270">This object only</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56514-271">RTCUniversalUserReadOnlyGroup hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="56514-271">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="56514-272">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="56514-272">List contents</span></span></p>
<p><span data-ttu-id="56514-273">Alle Eigenschaften lesen</span><span class="sxs-lookup"><span data-stu-id="56514-273">Read all properties</span></span></p>
<p><span data-ttu-id="56514-274">Leseberechtigungen</span><span class="sxs-lookup"><span data-stu-id="56514-274">Read permissions</span></span></p></td>
<td><p><span data-ttu-id="56514-275">Nur dieses Objekt</span><span class="sxs-lookup"><span data-stu-id="56514-275">This object only</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56514-276">RTCUniversalUserReadOnlyGroup hinzugefügt</span><span class="sxs-lookup"><span data-stu-id="56514-276">RTCUniversalUserReadOnlyGroup</span></span></p></td>
<td><p><span data-ttu-id="56514-277">Lesen von RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-277">Read RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="56514-278">Lesen von RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-278">Read RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="56514-279">Lesen von RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-279">Read RTCPropertySet</span></span></p>
<p><span data-ttu-id="56514-280">Lesen Personal-Information</span><span class="sxs-lookup"><span data-stu-id="56514-280">Read Personal-Information</span></span></p>
<p><span data-ttu-id="56514-281">Lesen Public-Information</span><span class="sxs-lookup"><span data-stu-id="56514-281">Read Public-Information</span></span></p>
<p><span data-ttu-id="56514-282">Lesen General-Information</span><span class="sxs-lookup"><span data-stu-id="56514-282">Read General-Information</span></span></p>
<p><span data-ttu-id="56514-283">Lesen von Benutzerkonto Einschränkungen</span><span class="sxs-lookup"><span data-stu-id="56514-283">Read User-Account-Restrictions</span></span></p></td>
<td><p><span data-ttu-id="56514-284">Nachgeordnete InetOrgPerson-Objekte</span><span class="sxs-lookup"><span data-stu-id="56514-284">Descendant inetOrgPerson objects</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56514-285">RTCUniversalUserAdmins</span><span class="sxs-lookup"><span data-stu-id="56514-285">RTCUniversalUserAdmins</span></span></p></td>
<td><p><span data-ttu-id="56514-286">Schreiben von RTCUserSearchPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-286">Write RTCUserSearchPropertySet</span></span></p>
<p><span data-ttu-id="56514-287">Schreiben von RTCUserProvisioningPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-287">Write RTCUserProvisioningPropertySet</span></span></p>
<p><span data-ttu-id="56514-288">Schreiben von RTCPropertySet</span><span class="sxs-lookup"><span data-stu-id="56514-288">Write RTCPropertySet</span></span></p>
<p><span data-ttu-id="56514-289">Schreiben von proxyAddresses</span><span class="sxs-lookup"><span data-stu-id="56514-289">Write proxyAddresses</span></span></p></td>
<td><p><span data-ttu-id="56514-290">Nachgeordnete InetOrgPerson-Objekte</span><span class="sxs-lookup"><span data-stu-id="56514-290">Descendant inetOrgPerson objects</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="56514-291">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="56514-291">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

