---
title: 'Lync Server 2013: UserStatistics-Tabelle'
description: 'Lync Server 2013: UserStatistics-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserStatistics table
ms:assetid: cfaf803b-1679-4169-92d3-533fad3e56ed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721893(v=OCS.15)
ms:contentKeyID: 49733827
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 75b34fa3c34af4cc9cf2cacc6ae7feb4d217114c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436097"
---
# <a name="userstatistics-table-in-lync-server-2013"></a><span data-ttu-id="adc12-103">UserStatistics-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="adc12-103">UserStatistics table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="adc12-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="adc12-104">

<span> </span></span></span>

<span data-ttu-id="adc12-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="adc12-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="adc12-106">Die Tabelle UserStatistics ist eine unterstützende Tabelle.</span><span class="sxs-lookup"><span data-stu-id="adc12-106">The UserStatistics table is a supporting table.</span></span> <span data-ttu-id="adc12-107">Jeder Datensatz in der Tabelle speichert Informationen zur Verwendung des Systems durch einen einzelnen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="adc12-107">Each record in the table stores information about an individual user’s usage of the system.</span></span> <span data-ttu-id="adc12-108">Diese Tabelle wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="adc12-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="adc12-109">Spalte</span><span class="sxs-lookup"><span data-stu-id="adc12-109">Column</span></span></th>
<th><span data-ttu-id="adc12-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="adc12-110">Data Type</span></span></th>
<th><span data-ttu-id="adc12-111">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="adc12-111">Key/Index</span></span></th>
<th><span data-ttu-id="adc12-112">Details</span><span class="sxs-lookup"><span data-stu-id="adc12-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="adc12-113"><strong>UserID</strong></span><span class="sxs-lookup"><span data-stu-id="adc12-113"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="adc12-114">int</span><span class="sxs-lookup"><span data-stu-id="adc12-114">int</span></span></p></td>
<td><p><span data-ttu-id="adc12-115">Primary</span><span class="sxs-lookup"><span data-stu-id="adc12-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="adc12-116">Eindeutige Nummer, die diesen Benutzer kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="adc12-116">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adc12-117"><strong>LastLogInTime</strong></span><span class="sxs-lookup"><span data-stu-id="adc12-117"><strong>LastLogInTime</strong></span></span></p></td>
<td><p><span data-ttu-id="adc12-118">datetime</span><span class="sxs-lookup"><span data-stu-id="adc12-118">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="adc12-119">Zeitpunkt, zu dem sich der Benutzer zuletzt angemeldet hat.</span><span class="sxs-lookup"><span data-stu-id="adc12-119">Last time the user logged in.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adc12-120"><strong>LastConfOrganizedTime</strong></span><span class="sxs-lookup"><span data-stu-id="adc12-120"><strong>LastConfOrganizedTime</strong></span></span></p></td>
<td><p><span data-ttu-id="adc12-121">datetime</span><span class="sxs-lookup"><span data-stu-id="adc12-121">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="adc12-122">Der letzte Zeitpunkt, zu dem der Benutzer eine Konferenz organisiert hat.</span><span class="sxs-lookup"><span data-stu-id="adc12-122">Last time the user organized a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="adc12-123"><strong>LastCallOrganizerCallFailureTime</strong></span><span class="sxs-lookup"><span data-stu-id="adc12-123"><strong>LastCallOrganizerCallFailureTime</strong></span></span></p></td>
<td><p><span data-ttu-id="adc12-124">datetime</span><span class="sxs-lookup"><span data-stu-id="adc12-124">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="adc12-125">Der letzte Zeitpunkt, zu dem der Benutzer einen Anruf Fehler erlebt hat.</span><span class="sxs-lookup"><span data-stu-id="adc12-125">Last time the user experienced a call failure.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="adc12-126"><strong>LastConfOrganizerCallFailureTime</strong></span><span class="sxs-lookup"><span data-stu-id="adc12-126"><strong>LastConfOrganizerCallFailureTime</strong></span></span></p></td>
<td><p><span data-ttu-id="adc12-127">datetime</span><span class="sxs-lookup"><span data-stu-id="adc12-127">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="adc12-128">Der letzte Zeitpunkt, zu dem der Benutzer einen Anruf Fehler als Konferenzorganisator erlebt hat.</span><span class="sxs-lookup"><span data-stu-id="adc12-128">Last time the user experienced a call failure as a conference organizer.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="adc12-129">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="adc12-129">


</div>

<span> </span>

</div>

</div>

</span></span></div>

