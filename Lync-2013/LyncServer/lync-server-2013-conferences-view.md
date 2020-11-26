---
title: 'Lync Server 2013: Konferenz Ansicht'
description: 'Lync Server 2013: Konferenz Ansicht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferences view
ms:assetid: c0e5c4db-c135-401f-9296-e9a49f6499a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721871(v=OCS.15)
ms:contentKeyID: 49733803
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dee7fbb7c839c351fc9c81716a5800a678980549
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434424"
---
# <a name="conferences-view-in-lync-server-2013"></a><span data-ttu-id="43f92-103">Konferenz Ansicht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="43f92-103">Conferences view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="43f92-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="43f92-104">

<span> </span></span></span>

<span data-ttu-id="43f92-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="43f92-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="43f92-106">In der Ansicht "Konferenzen" werden Informationen zu den Konferenzen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="43f92-106">The Conferences View stores information about the conferences.</span></span> <span data-ttu-id="43f92-107">Diese Ansicht wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="43f92-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="43f92-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="43f92-108">Column</span></span></th>
<th><span data-ttu-id="43f92-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="43f92-109">Data Type</span></span></th>
<th><span data-ttu-id="43f92-110">Details</span><span class="sxs-lookup"><span data-stu-id="43f92-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="43f92-111"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="43f92-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="43f92-112">datetime</span><span class="sxs-lookup"><span data-stu-id="43f92-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="43f92-113">Uhrzeit der Sitzungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="43f92-113">Time of session request.</span></span> <span data-ttu-id="43f92-114">Wird in Verbindung mit SessionIdSeq verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="43f92-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="43f92-115">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="43f92-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43f92-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="43f92-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="43f92-117">int</span><span class="sxs-lookup"><span data-stu-id="43f92-117">int</span></span></p></td>
<td><p><span data-ttu-id="43f92-118">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="43f92-118">ID number to identify the session.</span></span> <span data-ttu-id="43f92-119">Wird in Verbindung mit SessionID-Mal verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="43f92-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="43f92-120">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="43f92-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43f92-121"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="43f92-121"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="43f92-122">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="43f92-122">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="43f92-123">URI für die Konferenz.</span><span class="sxs-lookup"><span data-stu-id="43f92-123">URI for the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43f92-124"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="43f92-124"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="43f92-125">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="43f92-125">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="43f92-126">Der Typ des Konferenz-URIs.</span><span class="sxs-lookup"><span data-stu-id="43f92-126">Type of the conference URI.</span></span> <span data-ttu-id="43f92-127">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="43f92-127">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43f92-128"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="43f92-128"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="43f92-129">uniqueidentifier</span><span class="sxs-lookup"><span data-stu-id="43f92-129">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="43f92-130">Wird für wiederkehrende Konferenzen verwendet.</span><span class="sxs-lookup"><span data-stu-id="43f92-130">Used for recurring conferences.</span></span> <span data-ttu-id="43f92-131">Jede Instanz einer Besprechungsserie hat dieselbe ConferenceUri, aber eine andere ConfInstance.</span><span class="sxs-lookup"><span data-stu-id="43f92-131">Each instance of a recurring conference has the same ConferenceUri but a different ConfInstance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43f92-132"><strong>ConferenceStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="43f92-132"><strong>ConferenceStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="43f92-133">datetime</span><span class="sxs-lookup"><span data-stu-id="43f92-133">datetime</span></span></p></td>
<td><p><span data-ttu-id="43f92-134">Startzeit für die Konferenz.</span><span class="sxs-lookup"><span data-stu-id="43f92-134">Starting time for the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43f92-135"><strong>ConferenceEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="43f92-135"><strong>ConferenceEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="43f92-136">datetime</span><span class="sxs-lookup"><span data-stu-id="43f92-136">datetime</span></span></p></td>
<td><p><span data-ttu-id="43f92-137">Endzeit für die Konferenz.</span><span class="sxs-lookup"><span data-stu-id="43f92-137">Ending time for the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43f92-138"><strong>OrganizerUri</strong></span><span class="sxs-lookup"><span data-stu-id="43f92-138"><strong>OrganizerUri</strong></span></span></p></td>
<td><p><span data-ttu-id="43f92-139">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="43f92-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="43f92-140">Der URI des Benutzers, der die Konferenz organisiert hat.</span><span class="sxs-lookup"><span data-stu-id="43f92-140">URI of the user who organized the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43f92-141"><strong>Organizer</strong></span><span class="sxs-lookup"><span data-stu-id="43f92-141"><strong>OrganizerType</strong></span></span></p></td>
<td><p><span data-ttu-id="43f92-142">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="43f92-142">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="43f92-143">Der Typ des URIs des Benutzers, der die Konferenz organisiert hat.</span><span class="sxs-lookup"><span data-stu-id="43f92-143">Type of URI of the user who organized the conference.</span></span> <span data-ttu-id="43f92-144">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="43f92-144">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43f92-145"><strong>OrganizerTenant</strong></span><span class="sxs-lookup"><span data-stu-id="43f92-145"><strong>OrganizerTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="43f92-146">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="43f92-146">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="43f92-147">Der Mandant des Benutzers, der die Konferenz organisiert hat.</span><span class="sxs-lookup"><span data-stu-id="43f92-147">Tenant of the user who organized the conference.</span></span> <span data-ttu-id="43f92-148">Weitere Informationen finden Sie <a href="lync-server-2013-tenants-table.md">in der Tabelle Mandanten in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="43f92-148">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="43f92-149"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="43f92-149"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="43f92-150">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="43f92-150">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="43f92-151">Vollständig qualifizierter Domänenname des Pools, in dem die Konferenz gehostet wurde.</span><span class="sxs-lookup"><span data-stu-id="43f92-151">Fully qualified domain name of the pool that hosted the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="43f92-152"><strong>Kennzeichnen</strong></span><span class="sxs-lookup"><span data-stu-id="43f92-152"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="43f92-153">smallint</span><span class="sxs-lookup"><span data-stu-id="43f92-153">smallint</span></span></p></td>
<td><p><span data-ttu-id="43f92-154">Bitmaske, die Konferenz Attribute enthält.</span><span class="sxs-lookup"><span data-stu-id="43f92-154">Bit mask that contains Conference Attributes.</span></span> <span data-ttu-id="43f92-155">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="43f92-155">Possible values are:</span></span></p>
<p><span data-ttu-id="43f92-156">0X01 – synthetische Transaktion</span><span class="sxs-lookup"><span data-stu-id="43f92-156">0X01 – Synthetic Transaction</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="43f92-157">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="43f92-157">


</div>

<span> </span>

</div>

</div>

</span></span></div>

