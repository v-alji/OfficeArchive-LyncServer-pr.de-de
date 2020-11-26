---
title: 'Lync Server 2013: FileTransfers-Tabelle'
description: 'Lync Server 2013: Filetransfers-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: FileTransfers table
ms:assetid: 5368e67c-d8a9-43a1-9472-a839950dedb3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398353(v=OCS.15)
ms:contentKeyID: 48184118
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ccde45fa3743a809499273676d567846ef292ecc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428167"
---
# <a name="filetransfers-table-in-lync-server-2013"></a><span data-ttu-id="8bcfe-103">FileTransfers-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8bcfe-103">FileTransfers table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8bcfe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8bcfe-104">

<span> </span></span></span>

<span data-ttu-id="8bcfe-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="8bcfe-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="8bcfe-106">Jeder Datensatz stellt eine Dateiübertragungssitzung dar.</span><span class="sxs-lookup"><span data-stu-id="8bcfe-106">Each record represents one file transfer session.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8bcfe-107">Spalte</span><span class="sxs-lookup"><span data-stu-id="8bcfe-107">Column</span></span></th>
<th><span data-ttu-id="8bcfe-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="8bcfe-108">Data Type</span></span></th>
<th><span data-ttu-id="8bcfe-109">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="8bcfe-109">Key/Index</span></span></th>
<th><span data-ttu-id="8bcfe-110">Details</span><span class="sxs-lookup"><span data-stu-id="8bcfe-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8bcfe-111"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="8bcfe-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="8bcfe-112">datetime</span><span class="sxs-lookup"><span data-stu-id="8bcfe-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="8bcfe-113">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="8bcfe-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="8bcfe-114">Uhrzeit der Sitzungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="8bcfe-114">Time of session request.</span></span> <span data-ttu-id="8bcfe-115">Wird in Verbindung mit <strong>SessionIdSeq</strong> verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8bcfe-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="8bcfe-116">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8bcfe-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bcfe-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="8bcfe-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="8bcfe-118">int</span><span class="sxs-lookup"><span data-stu-id="8bcfe-118">int</span></span></p></td>
<td><p><span data-ttu-id="8bcfe-119">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="8bcfe-119">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="8bcfe-120">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8bcfe-120">ID number to identify the session.</span></span> <span data-ttu-id="8bcfe-121">Wird in Verbindung mit <strong>SessionID</strong> -Mal verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="8bcfe-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="8bcfe-122">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="8bcfe-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bcfe-123"><strong>Dateiname</strong></span><span class="sxs-lookup"><span data-stu-id="8bcfe-123"><strong>File Name</strong></span></span></p></td>
<td><p><span data-ttu-id="8bcfe-124">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="8bcfe-124">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8bcfe-125">Der Name der Datei.</span><span class="sxs-lookup"><span data-stu-id="8bcfe-125">Name of the file.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bcfe-126"><strong>Fileidentity</strong></span><span class="sxs-lookup"><span data-stu-id="8bcfe-126"><strong>FileIdentity</strong></span></span></p></td>
<td><p><span data-ttu-id="8bcfe-127">uniqueidentifier</span><span class="sxs-lookup"><span data-stu-id="8bcfe-127">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8bcfe-128">Eindeutiger Bezeichner zur Unterscheidung Zwischendatei Übertragungen mit demselben Dateinamen.</span><span class="sxs-lookup"><span data-stu-id="8bcfe-128">Unique identifier to distinguish between file transfers involving the same file name.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bcfe-129"><strong>Cookie</strong></span><span class="sxs-lookup"><span data-stu-id="8bcfe-129"><strong>Cookie</strong></span></span></p></td>
<td><p><span data-ttu-id="8bcfe-130">nvarchar (128)</span><span class="sxs-lookup"><span data-stu-id="8bcfe-130">nvarchar(128)</span></span></p></td>
<td><p><span data-ttu-id="8bcfe-131">Primary</span><span class="sxs-lookup"><span data-stu-id="8bcfe-131">Primary</span></span></p></td>
<td><p><span data-ttu-id="8bcfe-132">Wird verwendet, um jede nach Verfolgungs Nachricht als zugeordnet zu kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="8bcfe-132">Used to identify every follow-up message as being associated with this one.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bcfe-133"><strong>Annehmen</strong></span><span class="sxs-lookup"><span data-stu-id="8bcfe-133"><strong>Accept</strong></span></span></p></td>
<td><p><span data-ttu-id="8bcfe-134">bit</span><span class="sxs-lookup"><span data-stu-id="8bcfe-134">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8bcfe-135">Kann "wahr" oder "Null" sein.</span><span class="sxs-lookup"><span data-stu-id="8bcfe-135">Can be TRUE or NULL.</span></span> <span data-ttu-id="8bcfe-136">Ist "true", ist "ablehnen" und "Abbrechen" NULL.</span><span class="sxs-lookup"><span data-stu-id="8bcfe-136">If TRUE, then Reject and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8bcfe-137"><strong>Ablehnen</strong></span><span class="sxs-lookup"><span data-stu-id="8bcfe-137"><strong>Reject</strong></span></span></p></td>
<td><p><span data-ttu-id="8bcfe-138">bit</span><span class="sxs-lookup"><span data-stu-id="8bcfe-138">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8bcfe-139">Kann "wahr" oder "Null" sein.</span><span class="sxs-lookup"><span data-stu-id="8bcfe-139">Can be TRUE or NULL.</span></span> <span data-ttu-id="8bcfe-140">Ist "true", ist "akzeptieren" und "Abbrechen" NULL.</span><span class="sxs-lookup"><span data-stu-id="8bcfe-140">If TRUE, then Accept and Cancel will be NULL.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8bcfe-141"><strong>Abbrechen</strong></span><span class="sxs-lookup"><span data-stu-id="8bcfe-141"><strong>Cancel</strong></span></span></p></td>
<td><p><span data-ttu-id="8bcfe-142">bit</span><span class="sxs-lookup"><span data-stu-id="8bcfe-142">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="8bcfe-143">Kann "wahr" oder "Null" sein.</span><span class="sxs-lookup"><span data-stu-id="8bcfe-143">Can be TRUE or NULL.</span></span> <span data-ttu-id="8bcfe-144">Ist "true", ist "annehmen und ablehnen" NULL.</span><span class="sxs-lookup"><span data-stu-id="8bcfe-144">If TRUE, then Accept and Reject will be NULL.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="8bcfe-145">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8bcfe-145">


</div>

<span> </span>

</div>

</div>

</span></span></div>

