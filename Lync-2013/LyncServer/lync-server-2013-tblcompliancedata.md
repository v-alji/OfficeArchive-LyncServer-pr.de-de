---
title: 'Lync Server 2013: tblComplianceData'
description: 'Lync Server 2013: tblComplianceData.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceData
ms:assetid: 05b28f9b-4aba-4b69-ba8d-2ceeb6cbfaac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558606(v=OCS.15)
ms:contentKeyID: 48183308
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3c597d67054303de2753182b37419f68051d3af8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444476"
---
# <a name="tblcompliancedata-in-lync-server-2013"></a><span data-ttu-id="73640-103">tblComplianceData in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="73640-103">tblComplianceData in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="73640-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="73640-104">

<span> </span></span></span>

<span data-ttu-id="73640-105">_**Letztes Änderungsdatum des Themas:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="73640-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="73640-106">tblComplianceData enthält die Konformitätsereignisse, die noch nicht vom Kompatibilitätsadapter verarbeitet wurden.</span><span class="sxs-lookup"><span data-stu-id="73640-106">tblComplianceData contains the compliance events that have not been processed by the compliance adapter yet.</span></span>

### <a name="columns"></a><span data-ttu-id="73640-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="73640-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="73640-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="73640-108">Column</span></span></th>
<th><span data-ttu-id="73640-109">Typ</span><span class="sxs-lookup"><span data-stu-id="73640-109">Type</span></span></th>
<th><span data-ttu-id="73640-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73640-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73640-111">cmplEventID</span><span class="sxs-lookup"><span data-stu-id="73640-111">cmplEventID</span></span></p></td>
<td><p><span data-ttu-id="73640-112">bigint, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="73640-112">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="73640-113">Ereignis-ID.</span><span class="sxs-lookup"><span data-stu-id="73640-113">Event ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73640-114">entryDate</span><span class="sxs-lookup"><span data-stu-id="73640-114">entryDate</span></span></p></td>
<td><p><span data-ttu-id="73640-115">smalldatetime, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="73640-115">smalldatetime, not null</span></span></p></td>
<td><p><span data-ttu-id="73640-116">Zeitpunkt der Einfügung (kann für cmplType = 9 weit in der Zukunft liegen, da der Eintrag nur ein Platzhalter in diesem Fall ist).</span><span class="sxs-lookup"><span data-stu-id="73640-116">Time of insertion (may be far in the future for cmplType=9 because the entry is just a placeholder in that case).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73640-117">cmplType</span><span class="sxs-lookup"><span data-stu-id="73640-117">cmplType</span></span></p></td>
<td><p><span data-ttu-id="73640-118">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="73640-118">int, not null</span></span></p></td>
<td><p><span data-ttu-id="73640-119">Art des Konformitäts Ereignisses:</span><span class="sxs-lookup"><span data-stu-id="73640-119">Type of compliance event:</span></span></p>
<ul>
<li><p><span data-ttu-id="73640-120">1: Chat</span><span class="sxs-lookup"><span data-stu-id="73640-120">1: Chat</span></span></p></li>
<li><p><span data-ttu-id="73640-121">2: Backchat</span><span class="sxs-lookup"><span data-stu-id="73640-121">2: Backchat</span></span></p></li>
<li><p><span data-ttu-id="73640-122">3: Herunterladen von Dateien</span><span class="sxs-lookup"><span data-stu-id="73640-122">3: File download</span></span></p></li>
<li><p><span data-ttu-id="73640-123">4: Hochladen von Dateien</span><span class="sxs-lookup"><span data-stu-id="73640-123">4: File upload</span></span></p></li>
<li><p><span data-ttu-id="73640-124">9: provisorische Dateiübertragung</span><span class="sxs-lookup"><span data-stu-id="73640-124">9: Provisional file transfer</span></span></p></li>
<li><p><span data-ttu-id="73640-125">10: Löschen des Chats (mit Replace)</span><span class="sxs-lookup"><span data-stu-id="73640-125">10: Chat deletion (with replace)</span></span></p></li>
<li><p><span data-ttu-id="73640-126">11: Chat-Bereinigung</span><span class="sxs-lookup"><span data-stu-id="73640-126">11: Chat purging</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73640-127">cmplTime</span><span class="sxs-lookup"><span data-stu-id="73640-127">cmplTime</span></span></p></td>
<td><p><span data-ttu-id="73640-128">bigint, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="73640-128">bigint, not null</span></span></p></td>
<td><p><span data-ttu-id="73640-129">Zeitstempel für das Ereignis.</span><span class="sxs-lookup"><span data-stu-id="73640-129">Time stamp for the event.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73640-130">cmplChannelUri</span><span class="sxs-lookup"><span data-stu-id="73640-130">cmplChannelUri</span></span></p></td>
<td><p><span data-ttu-id="73640-131">nvarchar (255); nicht NULL</span><span class="sxs-lookup"><span data-stu-id="73640-131">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="73640-132">Kanal Uniform Resource Identifier (URI).</span><span class="sxs-lookup"><span data-stu-id="73640-132">Channel Uniform Resource Identifier (URI).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73640-133">cmplChatID</span><span class="sxs-lookup"><span data-stu-id="73640-133">cmplChatID</span></span></p></td>
<td><p><span data-ttu-id="73640-134">bigint</span><span class="sxs-lookup"><span data-stu-id="73640-134">bigint</span></span></p></td>
<td><p><span data-ttu-id="73640-135">Chat-ID (entsprechend der tblChat. Chat-Tabelle).</span><span class="sxs-lookup"><span data-stu-id="73640-135">Chat ID (corresponding to tblChat.chatId table).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73640-136">cmplUserID</span><span class="sxs-lookup"><span data-stu-id="73640-136">cmplUserID</span></span></p></td>
<td><p><span data-ttu-id="73640-137">int, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="73640-137">int, not null</span></span></p></td>
<td><p><span data-ttu-id="73640-138">Prinzipal-ID des Plakats (entsprechend der tblPrincipal. prinID-Tabelle).</span><span class="sxs-lookup"><span data-stu-id="73640-138">Principal ID of the poster (corresponding to tblPrincipal.prinID table).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="73640-139">cmplUserUri</span><span class="sxs-lookup"><span data-stu-id="73640-139">cmplUserUri</span></span></p></td>
<td><p><span data-ttu-id="73640-140">nvarchar (255); nicht NULL</span><span class="sxs-lookup"><span data-stu-id="73640-140">nvarchar (255), not null</span></span></p></td>
<td><p><span data-ttu-id="73640-141">Benutzer-URI.</span><span class="sxs-lookup"><span data-stu-id="73640-141">User URI.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="73640-142">cmplMessage</span><span class="sxs-lookup"><span data-stu-id="73640-142">cmplMessage</span></span></p></td>
<td><p><span data-ttu-id="73640-143">nvarchar (max)</span><span class="sxs-lookup"><span data-stu-id="73640-143">nvarchar (max)</span></span></p></td>
<td><p><span data-ttu-id="73640-144">Nachricht (Codierung hängt von cmplType ab).</span><span class="sxs-lookup"><span data-stu-id="73640-144">Message (encoding depends on cmplType).</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="key"></a><span data-ttu-id="73640-145">Key</span><span class="sxs-lookup"><span data-stu-id="73640-145">Key</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="73640-146">Spalte</span><span class="sxs-lookup"><span data-stu-id="73640-146">Column</span></span></th>
<th><span data-ttu-id="73640-147">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="73640-147">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="73640-148">cmplEventID</span><span class="sxs-lookup"><span data-stu-id="73640-148">cmplEventID</span></span></p></td>
<td><p><span data-ttu-id="73640-149">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="73640-149">Primary key.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="73640-150">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="73640-150">


</div>

<span> </span>

</div>

</div>

</span></span></div>

