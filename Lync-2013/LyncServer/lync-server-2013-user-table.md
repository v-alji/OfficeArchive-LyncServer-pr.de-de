---
title: 'Lync Server 2013: User-Tabelle'
description: 'Lync Server 2013: Benutzertabelle'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User table
ms:assetid: 6b52047e-286d-47ab-b7bc-a9b266f62d82
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398505(v=OCS.15)
ms:contentKeyID: 48184437
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 15d1ac08a229f4afea35a2727ef1105a5f24b826
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444168"
---
# <a name="user-table-in-lync-server-2013"></a><span data-ttu-id="3b840-103">User-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3b840-103">User table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3b840-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3b840-104">

<span> </span></span></span>

<span data-ttu-id="3b840-105">_**Letztes Änderungsdatum des Themas:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="3b840-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="3b840-106">Die Tabelle Benutzer ist eine unterstützende Tabelle, in der eine Liste der verschiedenen Benutzer gespeichert ist, die an Sitzungen teilgenommen haben, die in der Datenbank aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="3b840-106">The User table is a supporting table that stores a list of the various users who have participated in sessions recorded in the database.</span></span> <span data-ttu-id="3b840-107">Jeder Datensatz in der Tabelle steht für einen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="3b840-107">Each record in the table represents one user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3b840-108"><strong>Spalte</strong></span><span class="sxs-lookup"><span data-stu-id="3b840-108"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="3b840-109"><strong>Datentyp</strong></span><span class="sxs-lookup"><span data-stu-id="3b840-109"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="3b840-110"><strong>Schlüssel/Index</strong></span><span class="sxs-lookup"><span data-stu-id="3b840-110"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="3b840-111"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="3b840-111"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3b840-112"><strong>UserKey</strong></span><span class="sxs-lookup"><span data-stu-id="3b840-112"><strong>UserKey</strong></span></span></p></td>
<td><p><span data-ttu-id="3b840-113">int</span><span class="sxs-lookup"><span data-stu-id="3b840-113">int</span></span></p></td>
<td><p><span data-ttu-id="3b840-114">Primary</span><span class="sxs-lookup"><span data-stu-id="3b840-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="3b840-115">Eindeutige Nummer, die diesen Benutzer kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="3b840-115">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b840-116"><strong>URI</strong></span><span class="sxs-lookup"><span data-stu-id="3b840-116"><strong>URI</strong></span></span></p></td>
<td><p><span data-ttu-id="3b840-117">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="3b840-117">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="3b840-118">Eindeutigen</span><span class="sxs-lookup"><span data-stu-id="3b840-118">Unique</span></span></p></td>
<td><p><span data-ttu-id="3b840-119">URI-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="3b840-119">URI string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b840-120"><strong>URIType</strong></span><span class="sxs-lookup"><span data-stu-id="3b840-120"><strong>URIType</strong></span></span></p></td>
<td><p><span data-ttu-id="3b840-121">int</span><span class="sxs-lookup"><span data-stu-id="3b840-121">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3b840-122">1 ist ein Unbekannter URI-Typ.</span><span class="sxs-lookup"><span data-stu-id="3b840-122">1 is unknown URI type.</span></span></p>
<p><span data-ttu-id="3b840-123">2 ist ein Benutzer-URI.</span><span class="sxs-lookup"><span data-stu-id="3b840-123">2 is user URI.</span></span></p>
<p><span data-ttu-id="3b840-124">4 ist Konferenz-URI.</span><span class="sxs-lookup"><span data-stu-id="3b840-124">4 is conference URI.</span></span></p>
<p><span data-ttu-id="3b840-125">8 ist ein Telefon-URI.</span><span class="sxs-lookup"><span data-stu-id="3b840-125">8 is phone URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b840-126"><strong>TenantKey</strong></span><span class="sxs-lookup"><span data-stu-id="3b840-126"><strong>TenantKey</strong></span></span></p></td>
<td><p><span data-ttu-id="3b840-127">int</span><span class="sxs-lookup"><span data-stu-id="3b840-127">int</span></span></p></td>
<td><p><span data-ttu-id="3b840-128">Fremd</span><span class="sxs-lookup"><span data-stu-id="3b840-128">Foreign</span></span></p></td>
<td><p><span data-ttu-id="3b840-129">Der Mandant des Benutzers, auf den die Mandantentabelle verweist.</span><span class="sxs-lookup"><span data-stu-id="3b840-129">Tenant of the user, referenced from tenant table.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3b840-130"><strong>LastPoorCallTime</strong></span><span class="sxs-lookup"><span data-stu-id="3b840-130"><strong>LastPoorCallTime</strong></span></span></p></td>
<td><p><span data-ttu-id="3b840-131">datetime</span><span class="sxs-lookup"><span data-stu-id="3b840-131">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3b840-132">Letzter Zeitstempel, wenn der Benutzer einen schlechten Audioanruf hatte.</span><span class="sxs-lookup"><span data-stu-id="3b840-132">Latest time stamp when the user had a poor audio call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3b840-133"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="3b840-133"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="3b840-134">datetime</span><span class="sxs-lookup"><span data-stu-id="3b840-134">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="3b840-135">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="3b840-135">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3b840-136">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3b840-136">


</div>

<span> </span>

</div>

</div>

</span></span></div>

