---
title: 'Lync Server 2013: von Grant-CsSetupPermission vorgenommene Änderungen'
description: 'Lync Server 2013: von Grant-CsSetupPermission vorgenommene Änderungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Changes made by Grant-CsSetupPermission
ms:assetid: c5801f48-14e3-4fdd-8f14-d52e7af07a57
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205250(v=OCS.15)
ms:contentKeyID: 48185360
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d2a9156c977c993dd32e38fc6816bd08d3f65c1f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435068"
---
# <a name="changes-made-by-grant-cssetuppermission-in-lync-server-2013"></a><span data-ttu-id="af281-103">Von Grant-CsSetupPermission in lync Server 2013 vorgenommene Änderungen</span><span class="sxs-lookup"><span data-stu-id="af281-103">Changes made by Grant-CsSetupPermission in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="af281-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="af281-104">

<span> </span></span></span>

<span data-ttu-id="af281-105">_**Letztes Änderungsdatum des Themas:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="af281-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="af281-106">Zum Delegieren von Setup können Sie der universellen RTCUniversalServerAdmins-Gruppe für eine bestimmte Active Directory-Organisationseinheit Berechtigungen erteilen, sodass Mitglieder der RTCUniversalServerAdmins-Gruppe in dieser OU lync Server 2013 in der angegebenen Domäne installieren können, ohne Mitglieder der Gruppe der Domänenadministratoren zu sein.</span><span class="sxs-lookup"><span data-stu-id="af281-106">To delegate setup, you can grant permissions to the RTCUniversalServerAdmins universal group for a specific Active Directory organizational unit (OU), enabling members of the RTCUniversalServerAdmins group in that OU to install Lync Server 2013 in the specified domain without being members of the Domain Admins group.</span></span>

<span data-ttu-id="af281-107">Das Cmdlet **Grant-CsSetupPermission** gewährt der RTCUniversalServerAdmins-Gruppe Berechtigungen für eine OU, wie in der folgenden Tabelle angegeben:</span><span class="sxs-lookup"><span data-stu-id="af281-107">The **Grant-CsSetupPermission** cmdlet grants the RTCUniversalServerAdmins group permissions on an OU, as specified in the following table:</span></span>

### <a name="permissions-granted-to-objects-in-the-ou"></a><span data-ttu-id="af281-108">Berechtigungen, die Objekten in der Organisationseinheit gewährt werden</span><span class="sxs-lookup"><span data-stu-id="af281-108">Permissions granted to Objects in the OU</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="af281-109">Berechtigungen gelten für:</span><span class="sxs-lookup"><span data-stu-id="af281-109">Permissions apply to:</span></span></th>
<th><span data-ttu-id="af281-110">Gewährte Berechtigungen sind:</span><span class="sxs-lookup"><span data-stu-id="af281-110">Permissions granted are:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="af281-111">RTCUniversalServerAdmins</span><span class="sxs-lookup"><span data-stu-id="af281-111">RTCUniversalServerAdmins</span></span></p></td>
<td><p><span data-ttu-id="af281-112">Spezieller Zugriff:</span><span class="sxs-lookup"><span data-stu-id="af281-112">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="af281-113">Lesen von servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="af281-113">Read servicePrincipalName</span></span></p></li>
<li><p><span data-ttu-id="af281-114">Schreiben von servicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="af281-114">Write servicePrincipalName</span></span></p></li>
<li><p><span data-ttu-id="af281-115">Struktur löschen</span><span class="sxs-lookup"><span data-stu-id="af281-115">Delete tree</span></span></p></li>
<li><p><span data-ttu-id="af281-116">Replizieren von Verzeichnisänderungen</span><span class="sxs-lookup"><span data-stu-id="af281-116">Replicating directory changes</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af281-117">Nachfolger serviceConnectionPoint-Objekte</span><span class="sxs-lookup"><span data-stu-id="af281-117">Descendant serviceConnectionPoint objects</span></span></p></td>
<td><p><span data-ttu-id="af281-118">Spezieller Zugriff:</span><span class="sxs-lookup"><span data-stu-id="af281-118">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="af281-119">Leseberechtigungen</span><span class="sxs-lookup"><span data-stu-id="af281-119">Read permissions</span></span></p></li>
<li><p><span data-ttu-id="af281-120">Schreibberechtigungen</span><span class="sxs-lookup"><span data-stu-id="af281-120">Write permissions</span></span></p></li>
<li><p><span data-ttu-id="af281-121">Erstellen eines untergeordneten Elements</span><span class="sxs-lookup"><span data-stu-id="af281-121">Create child</span></span></p></li>
<li><p><span data-ttu-id="af281-122">Untergeordnetes Element löschen</span><span class="sxs-lookup"><span data-stu-id="af281-122">Delete child</span></span></p></li>
<li><p><span data-ttu-id="af281-123">Listeninhalt</span><span class="sxs-lookup"><span data-stu-id="af281-123">List contents</span></span></p></li>
<li><p><span data-ttu-id="af281-124">Write-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af281-124">Write property</span></span></p></li>
<li><p><span data-ttu-id="af281-125">Read-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af281-125">Read property</span></span></p></li>
<li><p><span data-ttu-id="af281-126">Struktur löschen</span><span class="sxs-lookup"><span data-stu-id="af281-126">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af281-127">NachfolgerAttribut msRTCSIP-Server Objekte</span><span class="sxs-lookup"><span data-stu-id="af281-127">Descendant msRTCSIP-Server objects</span></span></p></td>
<td><p><span data-ttu-id="af281-128">Spezieller Zugriff:</span><span class="sxs-lookup"><span data-stu-id="af281-128">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="af281-129">Write-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af281-129">Write property</span></span></p></li>
<li><p><span data-ttu-id="af281-130">Read-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af281-130">Read property</span></span></p></li>
<li><p><span data-ttu-id="af281-131">Struktur löschen</span><span class="sxs-lookup"><span data-stu-id="af281-131">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af281-132">NachfolgerAttribut msRTCSIP – Webkomponenten Objekte</span><span class="sxs-lookup"><span data-stu-id="af281-132">Descendant msRTCSIP-WebComponents objects</span></span></p></td>
<td><p><span data-ttu-id="af281-133">Spezieller Zugriff:</span><span class="sxs-lookup"><span data-stu-id="af281-133">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="af281-134">Write-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af281-134">Write property</span></span></p></li>
<li><p><span data-ttu-id="af281-135">Read-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af281-135">Read property</span></span></p></li>
<li><p><span data-ttu-id="af281-136">Struktur löschen</span><span class="sxs-lookup"><span data-stu-id="af281-136">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af281-137">NachfolgerAttribut msRTCSIP-MCU-Objekte</span><span class="sxs-lookup"><span data-stu-id="af281-137">Descendant msRTCSIP-MCU objects</span></span></p></td>
<td><p><span data-ttu-id="af281-138">Spezieller Zugriff:</span><span class="sxs-lookup"><span data-stu-id="af281-138">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="af281-139">Write-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af281-139">Write property</span></span></p></li>
<li><p><span data-ttu-id="af281-140">Read-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af281-140">Read property</span></span></p></li>
<li><p><span data-ttu-id="af281-141">Struktur löschen</span><span class="sxs-lookup"><span data-stu-id="af281-141">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af281-142">NachfolgerAttribut msRTCSIP-MediationServer-Objekte</span><span class="sxs-lookup"><span data-stu-id="af281-142">Descendant msRTCSIP-MediationServer objects</span></span></p></td>
<td><p><span data-ttu-id="af281-143">Spezieller Zugriff:</span><span class="sxs-lookup"><span data-stu-id="af281-143">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="af281-144">Write-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af281-144">Write property</span></span></p></li>
<li><p><span data-ttu-id="af281-145">Read-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af281-145">Read property</span></span></p></li>
<li><p><span data-ttu-id="af281-146">Struktur löschen</span><span class="sxs-lookup"><span data-stu-id="af281-146">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af281-147">NachfolgerAttribut msRTCSIP-ApplicationServer-Objekte</span><span class="sxs-lookup"><span data-stu-id="af281-147">Descendant msRTCSIP-ApplicationServer objects</span></span></p></td>
<td><p><span data-ttu-id="af281-148">Spezieller Zugriff:</span><span class="sxs-lookup"><span data-stu-id="af281-148">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="af281-149">Write-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af281-149">Write property</span></span></p></li>
<li><p><span data-ttu-id="af281-150">Read-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af281-150">Read property</span></span></p></li>
<li><p><span data-ttu-id="af281-151">Struktur löschen</span><span class="sxs-lookup"><span data-stu-id="af281-151">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="af281-152">NachfolgerAttribut msRTCSIP-ConnectionPoint-Objekte</span><span class="sxs-lookup"><span data-stu-id="af281-152">Descendant msRTCSIP-ConnectionPoint objects</span></span></p></td>
<td><p><span data-ttu-id="af281-153">Spezieller Zugriff:</span><span class="sxs-lookup"><span data-stu-id="af281-153">Special access:</span></span></p>
<ul>
<li><p><span data-ttu-id="af281-154">Write-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af281-154">Write property</span></span></p></li>
<li><p><span data-ttu-id="af281-155">Read-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af281-155">Read property</span></span></p></li>
<li><p><span data-ttu-id="af281-156">Struktur löschen</span><span class="sxs-lookup"><span data-stu-id="af281-156">Delete tree</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="af281-157">Nachfolger Computer Objekte</span><span class="sxs-lookup"><span data-stu-id="af281-157">Descendant Computer objects</span></span></p></td>
<td><p><span data-ttu-id="af281-158">Spezieller Zugriff für serviceConnectionPoint:</span><span class="sxs-lookup"><span data-stu-id="af281-158">Special access for serviceConnectionPoint:</span></span></p>
<ul>
<li><p><span data-ttu-id="af281-159">Erstellen von untergeordneten Objekten</span><span class="sxs-lookup"><span data-stu-id="af281-159">Create child objects</span></span></p></li>
<li><p><span data-ttu-id="af281-160">Löschen von untergeordneten Objekten</span><span class="sxs-lookup"><span data-stu-id="af281-160">Delete child objects</span></span></p></li>
<li><p><span data-ttu-id="af281-161">Struktur löschen</span><span class="sxs-lookup"><span data-stu-id="af281-161">Delete tree</span></span></p></li>
</ul>
<p><span data-ttu-id="af281-162">Spezieller Zugriff für öffentliche Informationen:</span><span class="sxs-lookup"><span data-stu-id="af281-162">Special access for public information:</span></span></p>
<ul>
<li><p><span data-ttu-id="af281-163">Read-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af281-163">Read property</span></span></p></li>
</ul>
<p><span data-ttu-id="af281-164">Spezieller Zugriff auf den DNS-Hostname:</span><span class="sxs-lookup"><span data-stu-id="af281-164">Special access for DNS host name:</span></span></p>
<ul>
<li><p><span data-ttu-id="af281-165">Read-Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="af281-165">Read property</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table><span data-ttu-id="af281-166">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="af281-166">


</div>

<span> </span>

</div>

</div>

</span></span></div>

