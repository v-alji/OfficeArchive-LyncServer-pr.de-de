---
title: 'Lync Server 2013: tblPrincipalType'
description: 'Lync Server 2013: tblPrincipalType.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblPrincipalType
ms:assetid: 32e1c1d6-80f4-4624-bf4e-b4c77d3982fa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558633(v=OCS.15)
ms:contentKeyID: 48183787
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba0f607d4499b54b16d7ecf8a4e7de603e874788
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393910"
---
# <a name="tblprincipaltype-in-lync-server-2013"></a><span data-ttu-id="c3827-103">tblPrincipalType in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c3827-103">tblPrincipalType in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c3827-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c3827-104">

<span> </span></span></span>

<span data-ttu-id="c3827-105">_**Letztes Änderungsdatum des Themas:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="c3827-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="c3827-106">tblPrincipalType enthält Prinzipaltypen, um zu kategorisieren, was in der tblPrincipal-Tabelle enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="c3827-106">tblPrincipalType contains principal types to categorize what is in the tblPrincipal table.</span></span>

### <a name="columns"></a><span data-ttu-id="c3827-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="c3827-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3827-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="c3827-108">Column</span></span></th>
<th><span data-ttu-id="c3827-109">Typ</span><span class="sxs-lookup"><span data-stu-id="c3827-109">Type</span></span></th>
<th><span data-ttu-id="c3827-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3827-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3827-111">ptypeID</span><span class="sxs-lookup"><span data-stu-id="c3827-111">ptypeID</span></span></p></td>
<td><p><span data-ttu-id="c3827-112">smallint, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="c3827-112">smallint, not null</span></span></p></td>
<td><p><span data-ttu-id="c3827-113">Prinzipaltyp-ID.</span><span class="sxs-lookup"><span data-stu-id="c3827-113">Principal type ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3827-114">ptypeDesc</span><span class="sxs-lookup"><span data-stu-id="c3827-114">ptypeDesc</span></span></p></td>
<td><p><span data-ttu-id="c3827-115">nvarchar (256); nicht NULL</span><span class="sxs-lookup"><span data-stu-id="c3827-115">nvarchar (256), not null</span></span></p></td>
<td><p><span data-ttu-id="c3827-116">Beschreibung des Typs.</span><span class="sxs-lookup"><span data-stu-id="c3827-116">Description of the type.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3827-117">ptypeIsSystemUser</span><span class="sxs-lookup"><span data-stu-id="c3827-117">ptypeIsSystemUser</span></span></p></td>
<td><p><span data-ttu-id="c3827-118">Bit, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="c3827-118">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="c3827-119">"True", wenn der Typ den Prinzipalen entspricht, die für interne Zwecke verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="c3827-119">True if the type corresponds to the principals that are used for internal purposes.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3827-120">ptypeIsUser</span><span class="sxs-lookup"><span data-stu-id="c3827-120">ptypeIsUser</span></span></p></td>
<td><p><span data-ttu-id="c3827-121">Bit, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="c3827-121">bit, not null</span></span></p></td>
<td><p><span data-ttu-id="c3827-122">"True", wenn es sich bei dem Typ um einen Benutzertyp handelt.</span><span class="sxs-lookup"><span data-stu-id="c3827-122">True if the type is a user type.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="c3827-123">Key</span><span class="sxs-lookup"><span data-stu-id="c3827-123">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3827-124">Spalte</span><span class="sxs-lookup"><span data-stu-id="c3827-124">Column</span></span></th>
<th><span data-ttu-id="c3827-125">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3827-125">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3827-126">ptypeID</span><span class="sxs-lookup"><span data-stu-id="c3827-126">ptypeID</span></span></p></td>
<td><p><span data-ttu-id="c3827-127">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="c3827-127">Primary key.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="principal-values"></a><span data-ttu-id="c3827-128">Prinzipal Werte</span><span class="sxs-lookup"><span data-stu-id="c3827-128">Principal Values</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c3827-129">ID</span><span class="sxs-lookup"><span data-stu-id="c3827-129">ID</span></span></th>
<th><span data-ttu-id="c3827-130">Rolle</span><span class="sxs-lookup"><span data-stu-id="c3827-130">Role</span></span></th>
<th><span data-ttu-id="c3827-131">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c3827-131">Description</span></span></th>
<th><span data-ttu-id="c3827-132">User</span><span class="sxs-lookup"><span data-stu-id="c3827-132">User</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c3827-133">1</span><span class="sxs-lookup"><span data-stu-id="c3827-133">1</span></span></p></td>
<td><p><span data-ttu-id="c3827-134">Beliebig</span><span class="sxs-lookup"><span data-stu-id="c3827-134">Any</span></span></p></td>
<td><p><span data-ttu-id="c3827-135">Generischer Prinzipal ohne bekannten Typ.</span><span class="sxs-lookup"><span data-stu-id="c3827-135">Generic principal with no known type.</span></span> <span data-ttu-id="c3827-136">Wird in der tblPrincipal-Tabelle nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3827-136">Not used in tblPrincipal table.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3827-137">2</span><span class="sxs-lookup"><span data-stu-id="c3827-137">2</span></span></p></td>
<td><p><span data-ttu-id="c3827-138">AnyUser</span><span class="sxs-lookup"><span data-stu-id="c3827-138">AnyUser</span></span></p></td>
<td><p><span data-ttu-id="c3827-139">Generisches Prinzipal des Benutzertyps.</span><span class="sxs-lookup"><span data-stu-id="c3827-139">Generic principal of user type.</span></span> <span data-ttu-id="c3827-140">Wird in der tblPrincipal-Tabelle nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3827-140">Not used in tblPrincipal table.</span></span></p></td>
<td><p><span data-ttu-id="c3827-141">Ja</span><span class="sxs-lookup"><span data-stu-id="c3827-141">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3827-142">3</span><span class="sxs-lookup"><span data-stu-id="c3827-142">3</span></span></p></td>
<td><p><span data-ttu-id="c3827-143">AnyGroup</span><span class="sxs-lookup"><span data-stu-id="c3827-143">AnyGroup</span></span></p></td>
<td><p><span data-ttu-id="c3827-144">Generischer Prinzipal mit Gruppen Semantik</span><span class="sxs-lookup"><span data-stu-id="c3827-144">Generic principal with group semantic.</span></span> <span data-ttu-id="c3827-145">Wird in der tblPrincipal-Tabelle nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="c3827-145">Not used in tblPrincipal table.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3827-146">4</span><span class="sxs-lookup"><span data-stu-id="c3827-146">4</span></span></p></td>
<td><p><span data-ttu-id="c3827-147">Multiswitch</span><span class="sxs-lookup"><span data-stu-id="c3827-147">SystemUser</span></span></p></td>
<td><p><span data-ttu-id="c3827-148">Prinzipal, der intern vom beständigen Chat Server verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c3827-148">Principal used internally by Persistent Chat Server.</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3827-149">5</span><span class="sxs-lookup"><span data-stu-id="c3827-149">5</span></span></p></td>
<td><p><span data-ttu-id="c3827-150">Benutzer</span><span class="sxs-lookup"><span data-stu-id="c3827-150">User</span></span></p></td>
<td><p><span data-ttu-id="c3827-151">Normaler Benutzer.</span><span class="sxs-lookup"><span data-stu-id="c3827-151">Regular user.</span></span></p></td>
<td><p><span data-ttu-id="c3827-152">Ja</span><span class="sxs-lookup"><span data-stu-id="c3827-152">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3827-153">8</span><span class="sxs-lookup"><span data-stu-id="c3827-153">8</span></span></p></td>
<td><p><span data-ttu-id="c3827-154">DC</span><span class="sxs-lookup"><span data-stu-id="c3827-154">DC</span></span></p></td>
<td><p><span data-ttu-id="c3827-155">Active Directory-Domänendienste-Domänencontroller.</span><span class="sxs-lookup"><span data-stu-id="c3827-155">Active Directory Domain Services domain controller.</span></span></p></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c3827-156">9</span><span class="sxs-lookup"><span data-stu-id="c3827-156">9</span></span></p></td>
<td><p><span data-ttu-id="c3827-157">Gruppe</span><span class="sxs-lookup"><span data-stu-id="c3827-157">Group</span></span></p></td>
<td><p><span data-ttu-id="c3827-158">Active Directory-Sicherheitsgruppe.</span><span class="sxs-lookup"><span data-stu-id="c3827-158">Active Directory security group.</span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c3827-159">10</span><span class="sxs-lookup"><span data-stu-id="c3827-159">10</span></span></p></td>
<td><p><span data-ttu-id="c3827-160">Ordner</span><span class="sxs-lookup"><span data-stu-id="c3827-160">Folder</span></span></p></td>
<td><p><span data-ttu-id="c3827-161">Active Directory-Container oder-Organisationseinheit.</span><span class="sxs-lookup"><span data-stu-id="c3827-161">Active Directory container or organizational unit.</span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="c3827-162">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c3827-162">See Also</span></span>


[<span data-ttu-id="c3827-163">tblPrincipal in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c3827-163">tblPrincipal in Lync Server 2013</span></span>](lync-server-2013-tblprincipal.md)  
  

<span data-ttu-id="c3827-164"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c3827-164"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

