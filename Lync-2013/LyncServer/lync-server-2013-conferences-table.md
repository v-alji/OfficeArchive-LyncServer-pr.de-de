---
title: 'Lync Server 2013: Conferences-Tabelle'
description: 'Lync Server 2013: Konferenz Tabelle'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferences table
ms:assetid: c3da6271-b3c6-4898-894f-10456ec794d0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412964(v=OCS.15)
ms:contentKeyID: 48185340
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e0d8c61e795dc0c8f9843b871d7e4efd1bec571
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394782"
---
# <a name="conferences-table-in-lync-server-2013"></a><span data-ttu-id="5c72e-103">Conferences-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5c72e-103">Conferences table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5c72e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5c72e-104">

<span> </span></span></span>

<span data-ttu-id="5c72e-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="5c72e-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="5c72e-106">Jeder Datensatz in dieser Tabelle enthält Anrufdetails zu einer Konferenz.</span><span class="sxs-lookup"><span data-stu-id="5c72e-106">Each record in this table contains call details about one conference.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="5c72e-107">Spalte</span><span class="sxs-lookup"><span data-stu-id="5c72e-107">Column</span></span></th>
<th><span data-ttu-id="5c72e-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="5c72e-108">Data Type</span></span></th>
<th><span data-ttu-id="5c72e-109">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="5c72e-109">Key/Index</span></span></th>
<th><span data-ttu-id="5c72e-110">Details</span><span class="sxs-lookup"><span data-stu-id="5c72e-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="5c72e-111"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="5c72e-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5c72e-112">datetime</span><span class="sxs-lookup"><span data-stu-id="5c72e-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="5c72e-113">Primary</span><span class="sxs-lookup"><span data-stu-id="5c72e-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="5c72e-114">Uhrzeit, zu der die Konferenzanforderung vom CdR-Agenten erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="5c72e-114">Time that the conference request was captured by the CDR agent.</span></span> <span data-ttu-id="5c72e-115">Wird nur als Primärschlüssel verwendet, um eine Konferenz Instanz eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5c72e-115">Used only as a primary key to uniquely identify a conference instance.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c72e-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="5c72e-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="5c72e-117">int</span><span class="sxs-lookup"><span data-stu-id="5c72e-117">int</span></span></p></td>
<td><p><span data-ttu-id="5c72e-118">Primary</span><span class="sxs-lookup"><span data-stu-id="5c72e-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="5c72e-119">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5c72e-119">ID number to identify the session.</span></span> <span data-ttu-id="5c72e-120">Wird in Verbindung mit <strong>SessionID</strong> -Mal verwendet, um eine Konferenz Instanz eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="5c72e-120">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference instance.</span></span> *</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c72e-121"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="5c72e-121"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="5c72e-122">int</span><span class="sxs-lookup"><span data-stu-id="5c72e-122">int</span></span></p></td>
<td><p><span data-ttu-id="5c72e-123">Fremd</span><span class="sxs-lookup"><span data-stu-id="5c72e-123">Foreign</span></span></p></td>
<td><p><span data-ttu-id="5c72e-124">Konferenz-URI</span><span class="sxs-lookup"><span data-stu-id="5c72e-124">Conference URI.</span></span> <span data-ttu-id="5c72e-125">Weitere Informationen finden Sie <a href="lync-server-2013-conferenceuris-table.md">in der ConferenceUris-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5c72e-125">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c72e-126"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="5c72e-126"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="5c72e-127">uniqueidentifier</span><span class="sxs-lookup"><span data-stu-id="5c72e-127">uniqueidentifier</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5c72e-128">Nützlich für wiederkehrende Konferenzen; jede Instanz einer Besprechungsserie hat dieselbe <strong>ConferenceUri</strong>, hat aber eine andere <strong>ConfInstance</strong>.</span><span class="sxs-lookup"><span data-stu-id="5c72e-128">Useful for recurring conferences; each instance of a recurring conference has the same <strong>ConferenceUri</strong>, but will have a different <strong>ConfInstance</strong>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c72e-129"><strong>ConferenceStartTime</strong></span><span class="sxs-lookup"><span data-stu-id="5c72e-129"><strong>ConferenceStartTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5c72e-130">datetime</span><span class="sxs-lookup"><span data-stu-id="5c72e-130">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5c72e-131">Startzeit der Konferenz</span><span class="sxs-lookup"><span data-stu-id="5c72e-131">Conference start time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c72e-132"><strong>ConferenceEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="5c72e-132"><strong>ConferenceEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="5c72e-133">datetime</span><span class="sxs-lookup"><span data-stu-id="5c72e-133">datetime</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="5c72e-134">Startzeit der Konferenz</span><span class="sxs-lookup"><span data-stu-id="5c72e-134">Conference start time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c72e-135"><strong>Pool-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="5c72e-135"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="5c72e-136">int</span><span class="sxs-lookup"><span data-stu-id="5c72e-136">int</span></span></p></td>
<td><p><span data-ttu-id="5c72e-137">Fremd</span><span class="sxs-lookup"><span data-stu-id="5c72e-137">Foreign</span></span></p></td>
<td><p><span data-ttu-id="5c72e-138">Die ID-Nummer zur Identifizierung des Pools, in dem die Konferenz aufgenommen wurde.</span><span class="sxs-lookup"><span data-stu-id="5c72e-138">ID number to identify the pool in which the conference was captured.</span></span> <span data-ttu-id="5c72e-139">Weitere Informationen finden Sie <a href="lync-server-2013-pools-table.md">in der Tabelle Pools in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5c72e-139">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c72e-140"><strong>Organizer-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="5c72e-140"><strong>OrganizerId</strong></span></span></p></td>
<td><p><span data-ttu-id="5c72e-141">Int</span><span class="sxs-lookup"><span data-stu-id="5c72e-141">Int</span></span></p></td>
<td><p><span data-ttu-id="5c72e-142">Fremd</span><span class="sxs-lookup"><span data-stu-id="5c72e-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="5c72e-143">Die ID-Nummer zum Identifizieren des Organisator-URIs dieser Konferenz.</span><span class="sxs-lookup"><span data-stu-id="5c72e-143">ID number to identify the organizer URI of this conference.</span></span> <span data-ttu-id="5c72e-144">Weitere Informationen finden Sie <a href="lync-server-2013-users-table.md">in der Tabelle Benutzer in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="5c72e-144">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="5c72e-145"><strong>Kennzeichnen</strong></span><span class="sxs-lookup"><span data-stu-id="5c72e-145"><strong>Flag</strong></span></span></p></td>
<td><p><span data-ttu-id="5c72e-146">smallint</span><span class="sxs-lookup"><span data-stu-id="5c72e-146">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5c72e-147">Eine Bitmaske, die Konferenz Attribute enthält.</span><span class="sxs-lookup"><span data-stu-id="5c72e-147">A bit mask that contains Conference Attributes.</span></span> <span data-ttu-id="5c72e-148">Mögliche Werte:</span><span class="sxs-lookup"><span data-stu-id="5c72e-148">Possible values are:</span></span></p>
<ul>
<li><p><span data-ttu-id="5c72e-149">0X01</span><span class="sxs-lookup"><span data-stu-id="5c72e-149">0X01</span></span></p></li>
<li><p><span data-ttu-id="5c72e-150">Synthetischen</span><span class="sxs-lookup"><span data-stu-id="5c72e-150">Synthetic</span></span></p></li>
<li><p><span data-ttu-id="5c72e-151">Transaktion</span><span class="sxs-lookup"><span data-stu-id="5c72e-151">Transaction</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="5c72e-152"><strong>Verarbeitet</strong></span><span class="sxs-lookup"><span data-stu-id="5c72e-152"><strong>Processed</strong></span></span></p></td>
<td><p><span data-ttu-id="5c72e-153">bit</span><span class="sxs-lookup"><span data-stu-id="5c72e-153">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="5c72e-154">Internes Feld, das vom Überwachungsdienst verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5c72e-154">Internal field used by the Monitoring service.</span></span></p>
<p><span data-ttu-id="5c72e-155">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="5c72e-155">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="5c72e-156">\* Bei den meisten Sitzungen erhält SessionIdSeq den Wert 1.</span><span class="sxs-lookup"><span data-stu-id="5c72e-156">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="5c72e-157">Wenn zwei Sitzungen genau zur gleichen Zeit beginnen, ist der SessionIdSeq für einen 1, und für den anderen wird 2 usw.</span><span class="sxs-lookup"><span data-stu-id="5c72e-157">If two sessions start at exactly the same time, the SessionIdSeq for one will be 1, and for the other will be 2, and so on.</span></span>

<span data-ttu-id="5c72e-158"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5c72e-158"></div>

<span> </span>

</div>

</div>

</span></span></div>

