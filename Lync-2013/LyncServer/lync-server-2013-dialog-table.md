---
title: 'Lync Server 2013: Dialog-Tabelle'
description: 'Lync Server 2013: Dialog Tabelle'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dialog table
ms:assetid: 4d93424f-9072-43f5-83c2-3d539e3e9ca6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398313(v=OCS.15)
ms:contentKeyID: 48184068
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7ae93b8ca9f1146b7dc164803f27cbeeadc66777
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429203"
---
# <a name="dialog-table-in-lync-server-2013"></a><span data-ttu-id="2ef52-103">Dialog-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ef52-103">Dialog table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2ef52-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2ef52-104">

<span> </span></span></span>

<span data-ttu-id="2ef52-105">_**Letztes Änderungsdatum des Themas:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="2ef52-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="2ef52-106">Die Dialog Tabelle ist eine unterstützende Tabelle; Jeder Datensatz steht für ein SIP-Dialogfeld (Session Initiation Protocol).</span><span class="sxs-lookup"><span data-stu-id="2ef52-106">The Dialog table is a supporting table; each record represents one Session Initiation Protocol (SIP) dialog.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2ef52-107"><strong>Spalte</strong></span><span class="sxs-lookup"><span data-stu-id="2ef52-107"><strong>Column</strong></span></span></th>
<th><span data-ttu-id="2ef52-108"><strong>Datentyp</strong></span><span class="sxs-lookup"><span data-stu-id="2ef52-108"><strong>Data Type</strong></span></span></th>
<th><span data-ttu-id="2ef52-109"><strong>Schlüssel/Index</strong></span><span class="sxs-lookup"><span data-stu-id="2ef52-109"><strong>Key/Index</strong></span></span></th>
<th><span data-ttu-id="2ef52-110"><strong>Details</strong></span><span class="sxs-lookup"><span data-stu-id="2ef52-110"><strong>Details</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2ef52-111"><strong>ConferenceDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="2ef52-111"><strong>ConferenceDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="2ef52-112">datetime</span><span class="sxs-lookup"><span data-stu-id="2ef52-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="2ef52-113">Primary</span><span class="sxs-lookup"><span data-stu-id="2ef52-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="2ef52-114">Zeitpunkt, zu dem der Quality of Excellence (QoE)-Agent den ersten Bericht von einem Anrufer oder angerufenen erhält.</span><span class="sxs-lookup"><span data-stu-id="2ef52-114">Time when the Quality of Excellence (QoE) agent receives the first report from either caller or callee.</span></span> <span data-ttu-id="2ef52-115">Wird in Verbindung mit SessionSeq verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="2ef52-115">Used in conjunction with SessionSeq to uniquely identify a session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ef52-116"><strong>SessionSeq</strong></span><span class="sxs-lookup"><span data-stu-id="2ef52-116"><strong>SessionSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="2ef52-117">int</span><span class="sxs-lookup"><span data-stu-id="2ef52-117">int</span></span></p></td>
<td><p><span data-ttu-id="2ef52-118">Primary</span><span class="sxs-lookup"><span data-stu-id="2ef52-118">Primary</span></span></p></td>
<td><p><span data-ttu-id="2ef52-119">Sequenznummer, um Sitzungen zu unterscheiden, wenn Sie dieselbe ConferenceDateTime haben.</span><span class="sxs-lookup"><span data-stu-id="2ef52-119">Sequence number to differentiate sessions when they have the same ConferenceDateTime.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2ef52-120"><strong>Dialogfeld-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="2ef52-120"><strong>DialogID</strong></span></span></p></td>
<td><p><span data-ttu-id="2ef52-121">varchar (256)</span><span class="sxs-lookup"><span data-stu-id="2ef52-121">varchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="2ef52-122">Dialog Feld-ID, die global eindeutig ist.</span><span class="sxs-lookup"><span data-stu-id="2ef52-122">Dialog ID which is globally unique.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2ef52-123"><strong>DialogIDChecksum</strong></span><span class="sxs-lookup"><span data-stu-id="2ef52-123"><strong>DialogIDChecksum</strong></span></span></p></td>
<td><p><span data-ttu-id="2ef52-124">int</span><span class="sxs-lookup"><span data-stu-id="2ef52-124">int</span></span></p></td>
<td><p><span data-ttu-id="2ef52-125">Index</span><span class="sxs-lookup"><span data-stu-id="2ef52-125">index</span></span></p></td>
<td><p><span data-ttu-id="2ef52-126">Die Prüfsumme der Dialog Feld-ID.</span><span class="sxs-lookup"><span data-stu-id="2ef52-126">Checksum of the Dialog ID.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="2ef52-127">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2ef52-127">


</div>

<span> </span>

</div>

</div>

</span></span></div>

