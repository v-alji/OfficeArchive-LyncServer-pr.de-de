---
title: 'Lync Server 2013: FocusJoinsAndLeaves-Tabelle'
description: 'Lync Server 2013: FocusJoinsAndLeaves-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FocusJoinsAndLeaves table
ms:assetid: e6f0212c-67e9-4061-8720-d0296e855991
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399026(v=OCS.15)
ms:contentKeyID: 48185690
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5796de16ed204ce4f33935d937cbaa425d63a67f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428107"
---
# <a name="focusjoinsandleaves-table-in-lync-server-2013"></a><span data-ttu-id="bfd0f-103">FocusJoinsAndLeaves-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bfd0f-103">FocusJoinsAndLeaves table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bfd0f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bfd0f-104">

<span> </span></span></span>

<span data-ttu-id="bfd0f-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="bfd0f-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="bfd0f-106">Jeder Datensatz in dieser Tabelle enthält die CDR-Informationen zu den Join-und Leave-Informationen eines Benutzers für eine Konferenz.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-106">Each record in this table contains the CDR information about one user’s join and leave information for one conference.</span></span> <span data-ttu-id="bfd0f-107">Jede Konferenz wird in dieser Tabelle für jedes Mal, wenn ein Benutzer mit der Konferenz verbunden ist, mit einem Datensatz dargestellt.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-107">Each conference is represented in this table by one record for each time a user joins and leaves the conference.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bfd0f-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="bfd0f-108">Column</span></span></th>
<th><span data-ttu-id="bfd0f-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bfd0f-109">Data Type</span></span></th>
<th><span data-ttu-id="bfd0f-110">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="bfd0f-110">Key/Index</span></span></th>
<th><span data-ttu-id="bfd0f-111">Details</span><span class="sxs-lookup"><span data-stu-id="bfd0f-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bfd0f-112"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="bfd0f-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="bfd0f-113">datetime</span><span class="sxs-lookup"><span data-stu-id="bfd0f-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="bfd0f-114">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="bfd0f-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="bfd0f-115">Uhrzeit der Konferenz Instanz.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-115">Time of conference instance.</span></span> <span data-ttu-id="bfd0f-116">Wird in Verbindung mit <strong>SessionIdSeq</strong> verwendet, um eine Konferenz Instanz eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="bfd0f-117">Weitere Informationen finden Sie <a href="lync-server-2013-conferences-table.md">in der Tabelle "Konferenzen" in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="bfd0f-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfd0f-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="bfd0f-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="bfd0f-119">int</span><span class="sxs-lookup"><span data-stu-id="bfd0f-119">int</span></span></p></td>
<td><p><span data-ttu-id="bfd0f-120">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="bfd0f-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="bfd0f-121">Die ID-Nummer zum Identifizieren der Konferenz Instanz.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="bfd0f-122">Wird in Verbindung mit <strong>SessionID</strong> -Mal verwendet, um eine Konferenz Instanz eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="bfd0f-123">Weitere Informationen finden Sie <a href="lync-server-2013-conferences-table.md">in der Tabelle "Konferenzen" in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="bfd0f-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfd0f-124"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="bfd0f-124"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="bfd0f-125">datetime</span><span class="sxs-lookup"><span data-stu-id="bfd0f-125">datetime</span></span></p></td>
<td><p><span data-ttu-id="bfd0f-126">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="bfd0f-126">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="bfd0f-127">Uhrzeit der Sitzungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-127">Time of session request.</span></span> <span data-ttu-id="bfd0f-128">Wird in Verbindung mit <strong>SessionIdSeq</strong> verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-128">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="bfd0f-129">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="bfd0f-129">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfd0f-130"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="bfd0f-130"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="bfd0f-131">int</span><span class="sxs-lookup"><span data-stu-id="bfd0f-131">int</span></span></p></td>
<td><p><span data-ttu-id="bfd0f-132">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="bfd0f-132">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="bfd0f-133">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-133">ID number to identify the session.</span></span> <span data-ttu-id="bfd0f-134">Wird in Verbindung mit <strong>SessionID</strong> -Mal verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-134">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="bfd0f-135">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="bfd0f-135">see the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfd0f-136"><strong>UserID</strong></span><span class="sxs-lookup"><span data-stu-id="bfd0f-136"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="bfd0f-137">int</span><span class="sxs-lookup"><span data-stu-id="bfd0f-137">int</span></span></p></td>
<td><p><span data-ttu-id="bfd0f-138">Fremd</span><span class="sxs-lookup"><span data-stu-id="bfd0f-138">Foreign</span></span></p></td>
<td><p><span data-ttu-id="bfd0f-139">Eindeutige Nummer, die diesen Benutzer identifiziert, auf die <a href="lync-server-2013-users-table.md">in der Tabelle "Benutzer" in lync Server 2013</a>verwiesen wird.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-139">Unique number identifying this user, referenced from the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfd0f-140"><strong>FocusUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="bfd0f-140"><strong>FocusUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="bfd0f-141">int</span><span class="sxs-lookup"><span data-stu-id="bfd0f-141">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="bfd0f-142">Wenn ein Benutzer gleichzeitig an mehreren Computern oder Geräten angemeldet ist, wird <strong>UserInstance</strong> verwendet, um die Kombination aus Benutzer und Gerät eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-142">If a user is logged on at multiple computers or devices at the same time, <strong>UserInstance</strong> is used to uniquely identify the user/device combination.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfd0f-143"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="bfd0f-143"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="bfd0f-144">bit</span><span class="sxs-lookup"><span data-stu-id="bfd0f-144">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="bfd0f-145">Ob sich der Benutzer intern angemeldet hat oder nicht.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-145">Whether the user logged on from internal or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfd0f-146"><strong>UserRole</strong></span><span class="sxs-lookup"><span data-stu-id="bfd0f-146"><strong>UserRole</strong></span></span></p></td>
<td><p><span data-ttu-id="bfd0f-147">int</span><span class="sxs-lookup"><span data-stu-id="bfd0f-147">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="bfd0f-148">Die Rolle dieses Benutzers in der Konferenz, beispielsweise Referent oder Teilnehmer.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-148">This user’s role in the conference, such as Presenter or Attendee.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfd0f-149"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="bfd0f-149"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="bfd0f-150">datetime</span><span class="sxs-lookup"><span data-stu-id="bfd0f-150">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="bfd0f-151">Der Zeitpunkt, zu dem dieser Benutzer der Konferenz Beitritt.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-151">The time this user joins the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfd0f-152"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="bfd0f-152"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="bfd0f-153">datetime</span><span class="sxs-lookup"><span data-stu-id="bfd0f-153">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="bfd0f-154">Der Zeitpunkt, zu dem dieser Benutzer die Konferenz verlässt.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-154">The time this user leaves the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bfd0f-155"><strong>ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="bfd0f-155"><strong>ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="bfd0f-156">int</span><span class="sxs-lookup"><span data-stu-id="bfd0f-156">int</span></span></p></td>
<td><p><span data-ttu-id="bfd0f-157">Fremd</span><span class="sxs-lookup"><span data-stu-id="bfd0f-157">Foreign</span></span></p></td>
<td><p><span data-ttu-id="bfd0f-158">Die Version der Client Software des Benutzers, auf die die <a href="lync-server-2013-clientversions-table.md">ClientVersions-Tabelle in lync Server 2013</a>verweist.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-158">Version of the user’s client software, referenced to the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bfd0f-159"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="bfd0f-159"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="bfd0f-160">uniqueIdentifier</span><span class="sxs-lookup"><span data-stu-id="bfd0f-160">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="bfd0f-161">GUID (Globally Unique Identifier) des in der Konferenz verwendeten Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-161">Globally unique identifier (GUID) of the endpoint used in the conference.</span></span></p>
<p><span data-ttu-id="bfd0f-162">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="bfd0f-162">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="bfd0f-163">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bfd0f-163">


</div>

<span> </span>

</div>

</div>

</span></span></div>

