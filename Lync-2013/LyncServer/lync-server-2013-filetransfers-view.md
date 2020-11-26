---
title: 'Lync Server 2013: Dateiübertragungen (Ansicht)'
description: 'Lync Server 2013: Dateiübertragungen (Ansicht).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FileTransfers view
ms:assetid: e52c3ad0-152e-4a18-af1c-1aff0d205151
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721914(v=OCS.15)
ms:contentKeyID: 49733848
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dd2b084274a4d5daa093f2269617214f703ac03e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428153"
---
# <a name="filetransfers-view-in-lync-server-2013"></a><span data-ttu-id="852bf-103">Dateiübertragungen (Ansicht) in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="852bf-103">FileTransfers view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="852bf-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="852bf-104">

<span> </span></span></span>

<span data-ttu-id="852bf-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="852bf-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="852bf-106">Die Filetransfer-Ansicht speichert Informationen zu Peer-to-Peer-Dateiübertragungssitzungen.</span><span class="sxs-lookup"><span data-stu-id="852bf-106">The FileTransfer view stores information about peer-to-peer file transfer sessions.</span></span> <span data-ttu-id="852bf-107">Diese Ansicht wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="852bf-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="852bf-108">Die Dateiübertragungen-Ansicht enthält alle Spalten in der <A href="lync-server-2013-sessiondetails-view.md">SessionDetails-Ansicht in lync Server 2013</A> sowie die unten aufgeführten Spalten.</span><span class="sxs-lookup"><span data-stu-id="852bf-108">The FileTransfers view contains all of the columns in the <A href="lync-server-2013-sessiondetails-view.md">SessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="852bf-109">Spalte</span><span class="sxs-lookup"><span data-stu-id="852bf-109">Column</span></span></th>
<th><span data-ttu-id="852bf-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="852bf-110">Data Type</span></span></th>
<th><span data-ttu-id="852bf-111">Details</span><span class="sxs-lookup"><span data-stu-id="852bf-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="852bf-112"><strong>FileName</strong></span><span class="sxs-lookup"><span data-stu-id="852bf-112"><strong>FileName</strong></span></span></p></td>
<td><p><span data-ttu-id="852bf-113">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="852bf-113">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="852bf-114">Der Name der übertragenen Datei.</span><span class="sxs-lookup"><span data-stu-id="852bf-114">Name of the file transferred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="852bf-115"><strong>Cookie</strong></span><span class="sxs-lookup"><span data-stu-id="852bf-115"><strong>Cookie</strong></span></span></p></td>
<td><p><span data-ttu-id="852bf-116">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="852bf-116">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="852bf-117">Wird verwendet, um jede nach Verfolgungs Nachricht als zugeordnet zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="852bf-117">Used to identify every follow-up message as being associated with this one.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="852bf-118"><strong>Fileidentity</strong></span><span class="sxs-lookup"><span data-stu-id="852bf-118"><strong>FileIdentity</strong></span></span></p></td>
<td><p><span data-ttu-id="852bf-119">uniqueidentifier</span><span class="sxs-lookup"><span data-stu-id="852bf-119">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="852bf-120">Eindeutiger Bezeichner zur Unterscheidung Zwischendatei Übertragungen mit demselben Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="852bf-120">Unique identifier to distinguish between file transfers involving the same file name.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="852bf-121"><strong>Annehmen</strong></span><span class="sxs-lookup"><span data-stu-id="852bf-121"><strong>Accept</strong></span></span></p></td>
<td><p><span data-ttu-id="852bf-122">bit</span><span class="sxs-lookup"><span data-stu-id="852bf-122">bit</span></span></p></td>
<td><p><span data-ttu-id="852bf-123">Kann "wahr" oder "Null" sein.</span><span class="sxs-lookup"><span data-stu-id="852bf-123">Can be TRUE or NULL.</span></span> <span data-ttu-id="852bf-124">Ist "true", ist "ablehnen" und "Abbrechen" NULL.</span><span class="sxs-lookup"><span data-stu-id="852bf-124">If TRUE, then Reject and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="852bf-125"><strong>Ablehnen</strong></span><span class="sxs-lookup"><span data-stu-id="852bf-125"><strong>Reject</strong></span></span></p></td>
<td><p><span data-ttu-id="852bf-126">bit</span><span class="sxs-lookup"><span data-stu-id="852bf-126">bit</span></span></p></td>
<td><p><span data-ttu-id="852bf-127">Kann "wahr" oder "Null" sein.</span><span class="sxs-lookup"><span data-stu-id="852bf-127">Can be TRUE or NULL.</span></span> <span data-ttu-id="852bf-128">Ist "true", ist "akzeptieren" und "Abbrechen" NULL.</span><span class="sxs-lookup"><span data-stu-id="852bf-128">If TRUE, then Accept and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="852bf-129"><strong>Abbrechen</strong></span><span class="sxs-lookup"><span data-stu-id="852bf-129"><strong>Cancel</strong></span></span></p></td>
<td><p><span data-ttu-id="852bf-130">bit</span><span class="sxs-lookup"><span data-stu-id="852bf-130">bit</span></span></p></td>
<td><p><span data-ttu-id="852bf-131">Kann "wahr" oder "Null" sein.</span><span class="sxs-lookup"><span data-stu-id="852bf-131">Can be TRUE or NULL.</span></span> <span data-ttu-id="852bf-132">Ist "true", ist "annehmen und ablehnen" NULL.</span><span class="sxs-lookup"><span data-stu-id="852bf-132">If TRUE, then Accept and Reject will be NULL.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="852bf-133">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="852bf-133">


</div>

<span> </span>

</div>

</div>

</span></span></div>

