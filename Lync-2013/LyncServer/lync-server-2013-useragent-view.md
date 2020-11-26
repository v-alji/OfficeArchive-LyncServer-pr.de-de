---
title: 'Lync Server 2013: UserAgent-Ansicht'
description: 'Lync Server 2013: UserAgent-Ansicht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserAgent view
ms:assetid: b986f76f-f16e-4e5e-96cb-6e8f7f9b42ee
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721862(v=OCS.15)
ms:contentKeyID: 49733795
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9fc5ef2ec01b50f3714dca3690d0844286baaef5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439051"
---
# <a name="useragent-view-in-lync-server-2013"></a><span data-ttu-id="924d2-103">UserAgent-Ansicht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="924d2-103">UserAgent view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="924d2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="924d2-104">

<span> </span></span></span>

<span data-ttu-id="924d2-105">_**Letztes Änderungsdatum des Themas:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="924d2-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="924d2-106">Die UserAgent-Ansicht speichert Informationen zu den Benutzer-Agents, die an Sitzungen teilgenommen haben, die Datensätze in der Datenbank aufweisen.</span><span class="sxs-lookup"><span data-stu-id="924d2-106">The UserAgent View stores information about the user agents that have been involved in sessions that have records in the database.</span></span> <span data-ttu-id="924d2-107">Diese Ansicht wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="924d2-107">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="924d2-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="924d2-108">Column</span></span></th>
<th><span data-ttu-id="924d2-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="924d2-109">Data Type</span></span></th>
<th><span data-ttu-id="924d2-110">Details</span><span class="sxs-lookup"><span data-stu-id="924d2-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="924d2-111">UserAgentKey</span><span class="sxs-lookup"><span data-stu-id="924d2-111">UserAgentKey</span></span></p></td>
<td><p><span data-ttu-id="924d2-112">int</span><span class="sxs-lookup"><span data-stu-id="924d2-112">int</span></span></p></td>
<td><p><span data-ttu-id="924d2-113">Eindeutige Nummer, die diesen Benutzer-Agent kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="924d2-113">Unique number identifying this user agent.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="924d2-114">UserAgent</span><span class="sxs-lookup"><span data-stu-id="924d2-114">UserAgent</span></span></p></td>
<td><p><span data-ttu-id="924d2-115">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="924d2-115">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="924d2-116">Benutzer-Agent-Zeichenfolge.</span><span class="sxs-lookup"><span data-stu-id="924d2-116">User agent string.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="924d2-117">UAType</span><span class="sxs-lookup"><span data-stu-id="924d2-117">UAType</span></span></p></td>
<td><p><span data-ttu-id="924d2-118">smallint</span><span class="sxs-lookup"><span data-stu-id="924d2-118">smallint</span></span></p></td>
<td><p><span data-ttu-id="924d2-119">Der Typ des Benutzer-Agents.</span><span class="sxs-lookup"><span data-stu-id="924d2-119">Type of user agent.</span></span> <span data-ttu-id="924d2-120">Weitere Informationen finden Sie <a href="lync-server-2013-useragent-table.md">in der UserAgent-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="924d2-120">See the <a href="lync-server-2013-useragent-table.md">UserAgent table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="924d2-121">UACategory</span><span class="sxs-lookup"><span data-stu-id="924d2-121">UACategory</span></span></p></td>
<td><p><span data-ttu-id="924d2-122">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="924d2-122">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="924d2-123">Die Kategorie, zu der der Benutzer-Agent gehört.</span><span class="sxs-lookup"><span data-stu-id="924d2-123">Category that the user agent belongs to.</span></span> <span data-ttu-id="924d2-124">Beispielsweise gehört der Benutzer-Agent Conferencing_Attendant_1 .0 zu UACategory CAA.</span><span class="sxs-lookup"><span data-stu-id="924d2-124">For example, the user agent Conferencing_Attendant_1.0 belongs to the UACategory CAA.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="924d2-125">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="924d2-125">


</div>

<span> </span>

</div>

</div>

</span></span></div>

