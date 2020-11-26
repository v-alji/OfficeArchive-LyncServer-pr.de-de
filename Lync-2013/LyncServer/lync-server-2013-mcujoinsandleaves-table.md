---
title: 'Lync Server 2013: McuJoinsAndLeaves-Tabelle'
description: 'Lync Server 2013: McuJoinsAndLeaves-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: McuJoinsAndLeaves table
ms:assetid: 4e073366-0b5d-45b4-a3f6-d63dd5fd9f25
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398316(v=OCS.15)
ms:contentKeyID: 48184115
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee7d9473892ac357dcefd80b0d52382c5dd7d930
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425752"
---
# <a name="mcujoinsandleaves-table-in-lync-server-2013"></a><span data-ttu-id="11f2b-103">McuJoinsAndLeaves-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="11f2b-103">McuJoinsAndLeaves table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="11f2b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="11f2b-104">

<span> </span></span></span>

<span data-ttu-id="11f2b-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="11f2b-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="11f2b-106">Jeder Datensatz in dieser Tabelle enthält Anrufdetails zu einer Kombination aus einem Benutzer-Join oder Leave-und Konferenzserver.</span><span class="sxs-lookup"><span data-stu-id="11f2b-106">Each record in this table contains call details about one combination of a user join or leave and conferencing server.</span></span> <span data-ttu-id="11f2b-107">Wenn ein Benutzer beispielsweise an einer Konferenz teilnimmt, die Webkonferenzen und Audio/Video-Elemente umfasst, wird ein Datensatz für die Webkonferenz Verknüpfung dieses Benutzers erstellt, und es wird ein anderer Eintrag für die Audio-und Videokonferenz Teilnahme des Benutzers erstellt.</span><span class="sxs-lookup"><span data-stu-id="11f2b-107">For example, if a user joins a conference that includes web conferencing and audio/video elements, one record would be created for that user’s web conferencing join, and another record would be created for the user’s audio/video conferencing join.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="11f2b-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="11f2b-108">Column</span></span></th>
<th><span data-ttu-id="11f2b-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="11f2b-109">Data Type</span></span></th>
<th><span data-ttu-id="11f2b-110">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="11f2b-110">Key/Index</span></span></th>
<th><span data-ttu-id="11f2b-111">Details</span><span class="sxs-lookup"><span data-stu-id="11f2b-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="11f2b-112"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="11f2b-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="11f2b-113">datetime</span><span class="sxs-lookup"><span data-stu-id="11f2b-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="11f2b-114">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="11f2b-114">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="11f2b-115">Uhrzeit der Konferenz Instanz.</span><span class="sxs-lookup"><span data-stu-id="11f2b-115">Time of conference instance.</span></span> <span data-ttu-id="11f2b-116">Wird in Verbindung mit <strong>SessionIdSeq</strong> verwendet, um eine Konferenz Instanz eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="11f2b-116">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="11f2b-117">Weitere Informationen finden Sie <a href="lync-server-2013-conferences-table.md">in der Tabelle "Konferenzen" in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="11f2b-117">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11f2b-118"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="11f2b-118"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="11f2b-119">int</span><span class="sxs-lookup"><span data-stu-id="11f2b-119">int</span></span></p></td>
<td><p><span data-ttu-id="11f2b-120">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="11f2b-120">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="11f2b-121">Die ID-Nummer zum Identifizieren der Konferenz Instanz.</span><span class="sxs-lookup"><span data-stu-id="11f2b-121">ID number to identify the conference instance.</span></span> <span data-ttu-id="11f2b-122">Wird in Verbindung mit <strong>SessionID</strong> -Mal verwendet, um eine Konferenz Instanz eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="11f2b-122">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> <span data-ttu-id="11f2b-123">Weitere Informationen finden Sie <a href="lync-server-2013-conferences-table.md">in der Tabelle "Konferenzen" in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="11f2b-123">See the <a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11f2b-124"><strong>UserID</strong></span><span class="sxs-lookup"><span data-stu-id="11f2b-124"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="11f2b-125">int</span><span class="sxs-lookup"><span data-stu-id="11f2b-125">int</span></span></p></td>
<td><p><span data-ttu-id="11f2b-126">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="11f2b-126">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="11f2b-127">Eindeutige Nummer, die diesen Benutzer kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="11f2b-127">Unique number identifying this user.</span></span> <span data-ttu-id="11f2b-128">Weitere Informationen finden Sie <a href="lync-server-2013-users-table.md">in der Tabelle Benutzer in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="11f2b-128">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11f2b-129"><strong>McuUserInstance</strong></span><span class="sxs-lookup"><span data-stu-id="11f2b-129"><strong>McuUserInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="11f2b-130">int</span><span class="sxs-lookup"><span data-stu-id="11f2b-130">int</span></span></p></td>
<td><p><span data-ttu-id="11f2b-131">Primary</span><span class="sxs-lookup"><span data-stu-id="11f2b-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="11f2b-132">Wenn ein Benutzer auf mehreren Computern oder Geräten gleichzeitig angemeldet ist, identifiziert McuUserInstance die Kombination aus Benutzer und Gerät eindeutig.</span><span class="sxs-lookup"><span data-stu-id="11f2b-132">If a user is logged on at multiple computers or devices at once, McuUserInstance uniquely identifies the user/device combination.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11f2b-133"><strong>IsFromPstn</strong></span><span class="sxs-lookup"><span data-stu-id="11f2b-133"><strong>IsFromPstn</strong></span></span></p></td>
<td><p><span data-ttu-id="11f2b-134">bit</span><span class="sxs-lookup"><span data-stu-id="11f2b-134">bit</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="11f2b-135">Gibt an, ob der Benutzer ein PSTN hat oder nicht.</span><span class="sxs-lookup"><span data-stu-id="11f2b-135">Whether the user is joining from a PSTN or not.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11f2b-136"><strong>McuId</strong></span><span class="sxs-lookup"><span data-stu-id="11f2b-136"><strong>McuId</strong></span></span></p></td>
<td><p><span data-ttu-id="11f2b-137">int</span><span class="sxs-lookup"><span data-stu-id="11f2b-137">int</span></span></p></td>
<td><p><span data-ttu-id="11f2b-138">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="11f2b-138">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="11f2b-139">Eindeutige Nummer, die diesen Konferenzserver identifiziert.</span><span class="sxs-lookup"><span data-stu-id="11f2b-139">Unique number identifying this conferencing server.</span></span> <span data-ttu-id="11f2b-140">Weitere Informationen finden Sie <a href="lync-server-2013-mcus-table.md">in der Tabelle "Tabelle" in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="11f2b-140">See the <a href="lync-server-2013-mcus-table.md">Mcus table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11f2b-141"><strong>DialogSessionIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="11f2b-141"><strong>DialogSessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="11f2b-142">datetime</span><span class="sxs-lookup"><span data-stu-id="11f2b-142">datetime</span></span></p></td>
<td><p><span data-ttu-id="11f2b-143">Fremd</span><span class="sxs-lookup"><span data-stu-id="11f2b-143">Foreign</span></span></p></td>
<td><p><span data-ttu-id="11f2b-144">Uhrzeit der Sitzungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="11f2b-144">Time of session request.</span></span> <span data-ttu-id="11f2b-145">Wird in Verbindung mit <strong>SessionIdSeq</strong> verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="11f2b-145">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="11f2b-146">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="11f2b-146">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11f2b-147"><strong>DialogSessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="11f2b-147"><strong>DialogSessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="11f2b-148">int</span><span class="sxs-lookup"><span data-stu-id="11f2b-148">int</span></span></p></td>
<td><p><span data-ttu-id="11f2b-149">Fremd</span><span class="sxs-lookup"><span data-stu-id="11f2b-149">Foreign</span></span></p></td>
<td><p><span data-ttu-id="11f2b-150">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="11f2b-150">ID number to identify the session.</span></span> <span data-ttu-id="11f2b-151">Wird in Verbindung mit <strong>SessionID</strong> -Mal verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="11f2b-151">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="11f2b-152">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="11f2b-152">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11f2b-153"><strong>UserJoinTime</strong></span><span class="sxs-lookup"><span data-stu-id="11f2b-153"><strong>UserJoinTime</strong></span></span></p></td>
<td><p><span data-ttu-id="11f2b-154">datetime</span><span class="sxs-lookup"><span data-stu-id="11f2b-154">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="11f2b-155">Der Zeitpunkt, zu dem dieser Benutzer diesem Konferenzserver Beitritt.</span><span class="sxs-lookup"><span data-stu-id="11f2b-155">The time this user joins this conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="11f2b-156"><strong>UserLeaveTime</strong></span><span class="sxs-lookup"><span data-stu-id="11f2b-156"><strong>UserLeaveTime</strong></span></span></p></td>
<td><p><span data-ttu-id="11f2b-157">datetime</span><span class="sxs-lookup"><span data-stu-id="11f2b-157">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="11f2b-158">Der Zeitpunkt, zu dem dieser Benutzer diesen Konferenzserver verlässt.</span><span class="sxs-lookup"><span data-stu-id="11f2b-158">The time this user leaves this conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="11f2b-159"><strong>ClientVerId</strong></span><span class="sxs-lookup"><span data-stu-id="11f2b-159"><strong>ClientVerId</strong></span></span></p></td>
<td><p><span data-ttu-id="11f2b-160">int</span><span class="sxs-lookup"><span data-stu-id="11f2b-160">int</span></span></p></td>
<td><p><span data-ttu-id="11f2b-161">Fremd</span><span class="sxs-lookup"><span data-stu-id="11f2b-161">Foreign</span></span></p></td>
<td><p><span data-ttu-id="11f2b-162">Bezeichner, der die Versionsnummer der Client Software in der Konferenz angibt.</span><span class="sxs-lookup"><span data-stu-id="11f2b-162">Identifier that specifies the version number of the client software use in the conference.</span></span> <span data-ttu-id="11f2b-163">Weitere Informationen finden Sie <a href="lync-server-2013-clientversions-table.md">in der ClientVersions-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="11f2b-163">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p>
<p><span data-ttu-id="11f2b-164">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="11f2b-164">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="11f2b-165">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="11f2b-165">


</div>

<span> </span>

</div>

</div>

</span></span></div>

