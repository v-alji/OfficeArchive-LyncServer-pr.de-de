---
title: 'Lync Server 2013: Users-Tabelle'
description: 'Lync Server 2013: Benutzertabelle'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Users table
ms:assetid: a8d71373-4b57-4245-9f02-f7fc0d9fcd3c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412791(v=OCS.15)
ms:contentKeyID: 48185032
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b1418e162a04e46ee0dfeca082aa66b0665fc77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436181"
---
# <a name="users-table-in-lync-server-2013"></a><span data-ttu-id="bd001-103">Users-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bd001-103">Users table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bd001-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bd001-104">

<span> </span></span></span>

<span data-ttu-id="bd001-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="bd001-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="bd001-106">Die Tabelle Benutzer ist eine unterstützende Tabelle.</span><span class="sxs-lookup"><span data-stu-id="bd001-106">The Users table is a supporting table.</span></span> <span data-ttu-id="bd001-107">Jeder Datensatz in der Tabelle speichert Informationen zu einem Benutzer an anrufen oder Sitzungen mit Datensätzen in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="bd001-107">Each record in the table stores information about one user involved in calls or sessions that have records in the database.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bd001-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="bd001-108">Column</span></span></th>
<th><span data-ttu-id="bd001-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="bd001-109">Data Type</span></span></th>
<th><span data-ttu-id="bd001-110">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="bd001-110">Key/Index</span></span></th>
<th><span data-ttu-id="bd001-111">Details</span><span class="sxs-lookup"><span data-stu-id="bd001-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bd001-112"><strong>NextUpdateTS</strong></span><span class="sxs-lookup"><span data-stu-id="bd001-112"><strong>NextUpdateTS</strong></span></span></p></td>
<td><p><span data-ttu-id="bd001-113">datetime</span><span class="sxs-lookup"><span data-stu-id="bd001-113">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="bd001-114">Zeitstempel für die interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="bd001-114">Time stamp for internal use.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd001-115"><strong>UserID</strong></span><span class="sxs-lookup"><span data-stu-id="bd001-115"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="bd001-116">int</span><span class="sxs-lookup"><span data-stu-id="bd001-116">int</span></span></p></td>
<td><p><span data-ttu-id="bd001-117">Primary</span><span class="sxs-lookup"><span data-stu-id="bd001-117">Primary</span></span></p></td>
<td><p><span data-ttu-id="bd001-118">Eindeutige Nummer, die diesen Benutzer kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="bd001-118">Unique number identifying this user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd001-119"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="bd001-119"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="bd001-120">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="bd001-120">nvarchar(450)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="bd001-121">Benutzer-URI.</span><span class="sxs-lookup"><span data-stu-id="bd001-121">User URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bd001-122"><strong>Mandanten</strong></span><span class="sxs-lookup"><span data-stu-id="bd001-122"><strong>TenantId</strong></span></span></p></td>
<td><p><span data-ttu-id="bd001-123">int</span><span class="sxs-lookup"><span data-stu-id="bd001-123">int</span></span></p></td>
<td><p><span data-ttu-id="bd001-124">Fremd</span><span class="sxs-lookup"><span data-stu-id="bd001-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="bd001-125">Die Mandanten-ID des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="bd001-125">This user’s Tenant ID.</span></span> <span data-ttu-id="bd001-126">Weitere Informationen finden Sie <a href="lync-server-2013-tenants-table.md">in der Tabelle Mandanten in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="bd001-126">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bd001-127"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="bd001-127"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="bd001-128">int</span><span class="sxs-lookup"><span data-stu-id="bd001-128">int</span></span></p></td>
<td><p><span data-ttu-id="bd001-129">Fremd</span><span class="sxs-lookup"><span data-stu-id="bd001-129">Foreign</span></span></p></td>
<td><p><span data-ttu-id="bd001-130">Der URI-Typ des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="bd001-130">This user’s URI type.</span></span> <span data-ttu-id="bd001-131">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="bd001-131">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="bd001-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bd001-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

