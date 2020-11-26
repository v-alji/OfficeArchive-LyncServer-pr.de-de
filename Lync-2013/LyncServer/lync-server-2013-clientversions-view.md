---
title: 'Lync Server 2013: ClientVersions-Ansicht'
description: 'Lync Server 2013: ClientVersions-Ansicht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ClientVersions view
ms:assetid: caf7678f-83a0-46c8-83cc-fee4c3991f52
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721891(v=OCS.15)
ms:contentKeyID: 49733825
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 42ede7107a59db3162ac7f5344e47e81a80d57df
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434732"
---
# <a name="clientversions-view-in-lync-server-2013"></a><span data-ttu-id="498d6-103">ClientVersions-Ansicht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="498d6-103">ClientVersions view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="498d6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="498d6-104">

<span> </span></span></span>

<span data-ttu-id="498d6-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="498d6-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="498d6-106">In der ClientVersions-Ansicht werden Informationen zu den verschiedenen Clienttypen und-Versionen gespeichert, die an Sitzungen teilgenommen haben, die in der Datenbank aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="498d6-106">The ClientVersions view stores information about the various client types and versions that have participated in sessions recorded in the database.</span></span> <span data-ttu-id="498d6-107">Jeder Datensatz in der Ansicht stellt eine Client Version dar.</span><span class="sxs-lookup"><span data-stu-id="498d6-107">Each record in the view represents one client version.</span></span> <span data-ttu-id="498d6-108">Diese Ansicht wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="498d6-108">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="498d6-109">Für bestimmte Spalten können mehrere Datensätze vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="498d6-109">There may be multiple records for certain columns.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="498d6-110">Spalte</span><span class="sxs-lookup"><span data-stu-id="498d6-110">Column</span></span></th>
<th><span data-ttu-id="498d6-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="498d6-111">Data Type</span></span></th>
<th><span data-ttu-id="498d6-112">Details</span><span class="sxs-lookup"><span data-stu-id="498d6-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="498d6-113"><strong>VersionID</strong></span><span class="sxs-lookup"><span data-stu-id="498d6-113"><strong>VersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="498d6-114">int</span><span class="sxs-lookup"><span data-stu-id="498d6-114">int</span></span></p></td>
<td><p><span data-ttu-id="498d6-115">Eindeutige Nummer, die diesen Clienttyp und die Version identifiziert.</span><span class="sxs-lookup"><span data-stu-id="498d6-115">Unique number identifying this client type and version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="498d6-116"><strong>Version</strong></span><span class="sxs-lookup"><span data-stu-id="498d6-116"><strong>Version</strong></span></span></p></td>
<td><p><span data-ttu-id="498d6-117">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="498d6-117">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="498d6-118">Stellt den Benutzer-Agent dar.</span><span class="sxs-lookup"><span data-stu-id="498d6-118">Represents the user agent.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="498d6-119"><strong>Clienttyp</strong></span><span class="sxs-lookup"><span data-stu-id="498d6-119"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="498d6-120">int</span><span class="sxs-lookup"><span data-stu-id="498d6-120">int</span></span></p></td>
<td><p><span data-ttu-id="498d6-121">Der Typ des Clients.</span><span class="sxs-lookup"><span data-stu-id="498d6-121">Type of client.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="498d6-122"><strong>ClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="498d6-122"><strong>ClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="498d6-123">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="498d6-123">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="498d6-124">Die Kategorie, zu der der Client gehört.</span><span class="sxs-lookup"><span data-stu-id="498d6-124">Category that the client belongs to.</span></span> <span data-ttu-id="498d6-125">Beispielsweise gehört der Client Conferencing_Attendant_1 .0 zu ClientCategory CAA.</span><span class="sxs-lookup"><span data-stu-id="498d6-125">For example, the client Conferencing_Attendant_1.0 belongs to the ClientCategory CAA.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="498d6-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="498d6-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

