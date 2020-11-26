---
title: 'Lync Server 2013: Dialogs-Tabelle'
description: 'Lync Server 2013: Dialogfelder (Tabelle).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dialogs table
ms:assetid: 487a430b-af66-4ea6-b28e-4e33cfdb7f9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425954(v=OCS.15)
ms:contentKeyID: 48184001
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c2c9cf9ec59fc48f7f5ffc6232980e3f8aa68c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429182"
---
# <a name="dialogs-table-in-lync-server-2013"></a><span data-ttu-id="58033-103">Dialogs-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="58033-103">Dialogs table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="58033-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="58033-104">

<span> </span></span></span>

<span data-ttu-id="58033-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="58033-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="58033-106">Die Tabelle Dialogfelder ist eine unterstützende Tabelle, in der die Informationen zu DialogIDs für Peer-to-Peer-Sitzungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="58033-106">The Dialogs table is a supporting table that stores the information about DialogIDs for peer-to-peer sessions.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="58033-107">Spalte</span><span class="sxs-lookup"><span data-stu-id="58033-107">Column</span></span></th>
<th><span data-ttu-id="58033-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="58033-108">Data Type</span></span></th>
<th><span data-ttu-id="58033-109">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="58033-109">Key/Index</span></span></th>
<th><span data-ttu-id="58033-110">Details</span><span class="sxs-lookup"><span data-stu-id="58033-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="58033-111"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="58033-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="58033-112">datetime</span><span class="sxs-lookup"><span data-stu-id="58033-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="58033-113">Primary</span><span class="sxs-lookup"><span data-stu-id="58033-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="58033-114">Uhrzeit der Sitzungsanforderung; wird in Verbindung mit SessionIDSeq verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="58033-114">Time of session request; used in conjunction with SessionIDSeq to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58033-115"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="58033-115"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="58033-116">int</span><span class="sxs-lookup"><span data-stu-id="58033-116">int</span></span></p></td>
<td><p><span data-ttu-id="58033-117">Primary</span><span class="sxs-lookup"><span data-stu-id="58033-117">Primary</span></span></p></td>
<td><p><span data-ttu-id="58033-118">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="58033-118">ID number to identify the session.</span></span> <span data-ttu-id="58033-119">Wird in Verbindung mit SessionID-Mal verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="58033-119">Used in conjunction with SessionIDTime to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="58033-120"><strong>ExternalChecksum</strong></span><span class="sxs-lookup"><span data-stu-id="58033-120"><strong>ExternalChecksum</strong></span></span></p></td>
<td><p><span data-ttu-id="58033-121">int</span><span class="sxs-lookup"><span data-stu-id="58033-121">int</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="58033-122">Prüfsumme der externen-Nr.</span><span class="sxs-lookup"><span data-stu-id="58033-122">Checksum of the ExternalID.</span></span> <span data-ttu-id="58033-123">Dieses Feld wird verwendet, um die Geschwindigkeit von Datenbanksuchen zu erhöhen.</span><span class="sxs-lookup"><span data-stu-id="58033-123">This field is used to increase the speed of database searches.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="58033-124"><strong>ExternalId</strong></span><span class="sxs-lookup"><span data-stu-id="58033-124"><strong>ExternalId</strong></span></span></p></td>
<td><p><span data-ttu-id="58033-125">varbinary (775)</span><span class="sxs-lookup"><span data-stu-id="58033-125">varbinary(775)</span></span></p></td>
<td><p> </p></td>
<td><p><span data-ttu-id="58033-126">SIP-Dialogfeld-ID, als Binärdatei gespeichert.</span><span class="sxs-lookup"><span data-stu-id="58033-126">SIP dialog ID, stored as a binary.</span></span> <span data-ttu-id="58033-127">Das Format der Binärdatei lautet wie folgt:</span><span class="sxs-lookup"><span data-stu-id="58033-127">The format of the binary is:</span></span></p>
<p><span data-ttu-id="58033-128">Dialogfeld; from-Tag; to-Tag</span><span class="sxs-lookup"><span data-stu-id="58033-128">dialog;from-tag;to-tag</span></span></p>
<p><span data-ttu-id="58033-129">Diese Daten können mithilfe der folgenden Syntax in das Text Format konvertiert werden:</span><span class="sxs-lookup"><span data-stu-id="58033-129">This data can be converted to text format by using this syntax:</span></span></p>
<p><code>cast(cast(ExternalId as varbinary(max)) as varchar(max))</code></p></td>
</tr>
</tbody>
</table><span data-ttu-id="58033-130">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="58033-130">


</div>

<span> </span>

</div>

</div>

</span></span></div>

