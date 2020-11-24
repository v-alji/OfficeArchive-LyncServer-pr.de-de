---
title: 'Lync Server 2013: Locations-Tabelle'
description: 'Lync Server 2013: Tabelle "Orte".'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Locations table
ms:assetid: 78dc1b14-5394-4f8e-89d3-4ba593272a04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398596(v=OCS.15)
ms:contentKeyID: 48184579
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9d07b6d3d3820f4efb3310adf0734a7e10c53e6d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395082"
---
# <a name="locations-table-in-lync-server-2013"></a><span data-ttu-id="f747c-103">Locations-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f747c-103">Locations table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f747c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f747c-104">

<span> </span></span></span>

<span data-ttu-id="f747c-105">_**Letztes Änderungsdatum des Themas:** 2012-05-25_</span><span class="sxs-lookup"><span data-stu-id="f747c-105">_**Topic Last Modified:** 2012-05-25_</span></span>

<span data-ttu-id="f747c-106">Jeder Datensatz steht in einem Notruf wie ein E9-1-1-Anruf für einen standortbezug.</span><span class="sxs-lookup"><span data-stu-id="f747c-106">Each record represents one location reference in an emergency call, like an E9-1-1 call.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="f747c-107">Spalte</span><span class="sxs-lookup"><span data-stu-id="f747c-107">Column</span></span></th>
<th><span data-ttu-id="f747c-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="f747c-108">Data Type</span></span></th>
<th><span data-ttu-id="f747c-109">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="f747c-109">Key/Index</span></span></th>
<th><span data-ttu-id="f747c-110">Details</span><span class="sxs-lookup"><span data-stu-id="f747c-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f747c-111"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="f747c-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="f747c-112">datetime</span><span class="sxs-lookup"><span data-stu-id="f747c-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="f747c-113">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="f747c-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="f747c-114">Uhrzeit der Sitzungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="f747c-114">Time of session request.</span></span> <span data-ttu-id="f747c-115">Wird in Verbindung mit <strong>SessionIdSeq</strong> verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f747c-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="f747c-116">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f747c-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f747c-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="f747c-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="f747c-118">int</span><span class="sxs-lookup"><span data-stu-id="f747c-118">int</span></span></p></td>
<td><p><span data-ttu-id="f747c-119">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="f747c-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="f747c-120">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f747c-120">ID number to identify the session.</span></span> <span data-ttu-id="f747c-121">Wird in Verbindung mit <strong>SessionID</strong> -Mal verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f747c-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="f747c-122">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="f747c-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f747c-123"><strong>Standort</strong></span><span class="sxs-lookup"><span data-stu-id="f747c-123"><strong>Location</strong></span></span></p></td>
<td><p><span data-ttu-id="f747c-124">nvarchar (max)</span><span class="sxs-lookup"><span data-stu-id="f747c-124">nvarchar(max)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="f747c-125">Ort des Notrufs.</span><span class="sxs-lookup"><span data-stu-id="f747c-125">Location of emergency call.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="f747c-126">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f747c-126">


</div>

<span> </span>

</div>

</div>

</span></span></div>

