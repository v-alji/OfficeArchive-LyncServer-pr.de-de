---
title: 'Lync Server 2013: ErrorDef-Tabelle'
description: 'Lync Server 2013: ErrorDef-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ErrorDef table
ms:assetid: 6acf3b86-da61-4923-9812-300db6f66dec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398503(v=OCS.15)
ms:contentKeyID: 48184403
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e58980a671b54007012bbbf6780e24c162aebe00
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428538"
---
# <a name="errordef-table-in-lync-server-2013"></a><span data-ttu-id="22e92-103">ErrorDef-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22e92-103">ErrorDef table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="22e92-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="22e92-104">

<span> </span></span></span>

<span data-ttu-id="22e92-105">_**Letztes Änderungsdatum des Themas:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="22e92-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="22e92-106">In der ErrorDef-Tabelle werden Informationen zu den einzelnen Fehlertypen gespeichert, die auftreten können.</span><span class="sxs-lookup"><span data-stu-id="22e92-106">The ErrorDef table stores information about each type of error that may occur.</span></span> <span data-ttu-id="22e92-107">Jeder Datensatz ist eine Art von Fehler.</span><span class="sxs-lookup"><span data-stu-id="22e92-107">Each record is one type of error.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="22e92-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="22e92-108">Column</span></span></th>
<th><span data-ttu-id="22e92-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="22e92-109">Data Type</span></span></th>
<th><span data-ttu-id="22e92-110">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="22e92-110">Key/Index</span></span></th>
<th><span data-ttu-id="22e92-111">Details</span><span class="sxs-lookup"><span data-stu-id="22e92-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="22e92-112"><strong>ErrorID</strong></span><span class="sxs-lookup"><span data-stu-id="22e92-112"><strong>ErrorId</strong></span></span></p></td>
<td><p><span data-ttu-id="22e92-113">int</span><span class="sxs-lookup"><span data-stu-id="22e92-113">int</span></span></p></td>
<td><p><span data-ttu-id="22e92-114">Primary</span><span class="sxs-lookup"><span data-stu-id="22e92-114">Primary</span></span></p></td>
<td><p><span data-ttu-id="22e92-115">Eindeutige ID-Nummer, die diese Art von Fehler kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="22e92-115">Unique ID number identifying this type of error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22e92-116"><strong>Response Code</strong></span><span class="sxs-lookup"><span data-stu-id="22e92-116"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="22e92-117">int</span><span class="sxs-lookup"><span data-stu-id="22e92-117">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="22e92-118">Standard mäßiger SIP-Antwortcode, der diesem Fehler zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="22e92-118">Standard SIP response code associated with this error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22e92-119"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="22e92-119"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="22e92-120">int</span><span class="sxs-lookup"><span data-stu-id="22e92-120">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="22e92-121">Microsoft-Diagnose-ID.</span><span class="sxs-lookup"><span data-stu-id="22e92-121">Microsoft Diagnostic ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22e92-122"><strong>CallTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="22e92-122"><strong>CallTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="22e92-123">Int</span><span class="sxs-lookup"><span data-stu-id="22e92-123">Int</span></span></p></td>
<td><p><span data-ttu-id="22e92-124">Fremd</span><span class="sxs-lookup"><span data-stu-id="22e92-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="22e92-125">Der Typ des Anrufs.</span><span class="sxs-lookup"><span data-stu-id="22e92-125">Type of the call.</span></span> <span data-ttu-id="22e92-126">Weitere Informationen finden Sie <a href="lync-server-2013-calltype-table.md">in der Tabelle "CallType" in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="22e92-126">See the <a href="lync-server-2013-calltype-table.md">CallType table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="22e92-127"><strong>RequestType</strong></span><span class="sxs-lookup"><span data-stu-id="22e92-127"><strong>RequestType</strong></span></span></p></td>
<td><p><span data-ttu-id="22e92-128">varbinary (33)</span><span class="sxs-lookup"><span data-stu-id="22e92-128">varbinary(33)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="22e92-129">Der Typ der fehlgeschlagenen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="22e92-129">Type of request that failed.</span></span></p>
<p><span data-ttu-id="22e92-130">Diese Daten können mithilfe der folgenden Syntax in das Text Format konvertiert werden:</span><span class="sxs-lookup"><span data-stu-id="22e92-130">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(RequestType as varbinary(max)) as varchar(max))</code></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="22e92-131"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="22e92-131"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="22e92-132">varbinary (257)</span><span class="sxs-lookup"><span data-stu-id="22e92-132">varbinary(257)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="22e92-133">Inhaltstyp der fehlgeschlagenen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="22e92-133">Content type of the request that failed.</span></span></p>
<p><span data-ttu-id="22e92-134">Diese Daten können mithilfe dieser Syntax in das Text Format konvertiert werden:</span><span class="sxs-lookup"><span data-stu-id="22e92-134">This data can be converted to text format by using this syntaxt:</span></span></p>
<p><code>cast(cast(ContentType as varbinary(max)) as varchar(max))</code></p></td>
</tr>
</tbody>
</table><span data-ttu-id="22e92-135">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="22e92-135">


</div>

<span> </span>

</div>

</div>

</span></span></div>

