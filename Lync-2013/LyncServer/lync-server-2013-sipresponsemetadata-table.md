---
title: 'Lync Server 2013: SIPResponseMetaData-Tabelle'
description: 'Lync Server 2013: SIPResponseMetaData-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: SIPResponseMetaData table
ms:assetid: cf723737-4a75-4352-829b-f4954aa59716
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205294(v=OCS.15)
ms:contentKeyID: 48185510
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 402cff331f81a9b46028d76de69deeaace8d5ae1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444623"
---
# <a name="sipresponsemetadata-table-in-lync-server-2013"></a><span data-ttu-id="e338f-103">SIPResponseMetaData-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e338f-103">SIPResponseMetaData table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e338f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e338f-104">

<span> </span></span></span>

<span data-ttu-id="e338f-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="e338f-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="e338f-106">Das SIPResponseMetaDataTable enthält eine Liste der SIP-Antwortcodes sowie die Klassifizierung und Definition der einzelnen Codes.</span><span class="sxs-lookup"><span data-stu-id="e338f-106">The SIPResponseMetaDataTable contains a list of SIP response codes and the classification and definition of each of those codes.</span></span> <span data-ttu-id="e338f-107">Diese Codes werden als Reaktion auf Ereignisse generiert, die sich auf SIP-Geräte und SIP-Kommunikationssitzungen auswirken. So wird beispielsweise der Antwortcode 403 generiert, wenn ein SIP-Gerät eine Anforderung stellt, aber der Server lehnt die Anerkennung dieser Anforderung ab.</span><span class="sxs-lookup"><span data-stu-id="e338f-107">These codes are generated in response to events affecting SIP devices and SIP communication sessions; for example, the response code 403 is generated when a SIP device makes a request, but the server declines to honor that request.</span></span>

<span data-ttu-id="e338f-108">Diese Tabelle wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="e338f-108">This table was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e338f-109">Spalte</span><span class="sxs-lookup"><span data-stu-id="e338f-109">Column</span></span></th>
<th><span data-ttu-id="e338f-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="e338f-110">Data Type</span></span></th>
<th><span data-ttu-id="e338f-111">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="e338f-111">Key/Index</span></span></th>
<th><span data-ttu-id="e338f-112">Details</span><span class="sxs-lookup"><span data-stu-id="e338f-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e338f-113"><strong>Response Code</strong></span><span class="sxs-lookup"><span data-stu-id="e338f-113"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="e338f-114">int</span><span class="sxs-lookup"><span data-stu-id="e338f-114">int</span></span></p></td>
<td><p><span data-ttu-id="e338f-115">Primary</span><span class="sxs-lookup"><span data-stu-id="e338f-115">Primary</span></span></p></td>
<td><p><span data-ttu-id="e338f-116">Numerischer Wert, der den SIP-Antwortcode darstellt.</span><span class="sxs-lookup"><span data-stu-id="e338f-116">Numeric value that represents the SIP response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e338f-117"><strong>Klasse</strong></span><span class="sxs-lookup"><span data-stu-id="e338f-117"><strong>Class</strong></span></span></p></td>
<td><p><span data-ttu-id="e338f-118">int</span><span class="sxs-lookup"><span data-stu-id="e338f-118">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e338f-119">Allgemeine Klassifizierung für den Antwortcode.</span><span class="sxs-lookup"><span data-stu-id="e338f-119">General classification for the response code.</span></span> <span data-ttu-id="e338f-120">Zu den Klassifizierungen gehören:</span><span class="sxs-lookup"><span data-stu-id="e338f-120">Classifications include:</span></span></p>
<ul>
<li><p><span data-ttu-id="e338f-121">1 – Informations Antworten</span><span class="sxs-lookup"><span data-stu-id="e338f-121">1 – Informational Responses</span></span></p></li>
<li><p><span data-ttu-id="e338f-122">2 – erfolgreiche Antworten</span><span class="sxs-lookup"><span data-stu-id="e338f-122">2 – Successful Responses</span></span></p></li>
<li><p><span data-ttu-id="e338f-123">3 – Umleitungsantworten</span><span class="sxs-lookup"><span data-stu-id="e338f-123">3 – Redirection Responses</span></span></p></li>
<li><p><span data-ttu-id="e338f-124">4 – Antworten auf Client Fehler</span><span class="sxs-lookup"><span data-stu-id="e338f-124">4 – Client Failure Responses</span></span></p></li>
<li><p><span data-ttu-id="e338f-125">5 – Server Fehlerantworten</span><span class="sxs-lookup"><span data-stu-id="e338f-125">5 -- Server Failure Responses</span></span></p></li>
<li><p><span data-ttu-id="e338f-126">6 – globale Fehlerantwort</span><span class="sxs-lookup"><span data-stu-id="e338f-126">6 – Global Failure Response</span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e338f-127"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="e338f-127"><strong>Description</strong></span></span></p></td>
<td><p><span data-ttu-id="e338f-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="e338f-128">nvarchar(256)</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="e338f-129">Beschreibung des SIP-Antwortcodes.</span><span class="sxs-lookup"><span data-stu-id="e338f-129">Description of the SIP response code.</span></span> <span data-ttu-id="e338f-130">Antwortcode 181 weist beispielsweise die folgende Beschreibung auf:</span><span class="sxs-lookup"><span data-stu-id="e338f-130">For example, response code 181 has the following description:</span></span></p>
<p><span data-ttu-id="e338f-131">Anruf wird weitergeleitet</span><span class="sxs-lookup"><span data-stu-id="e338f-131">Call Is Being Forwarded</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e338f-132">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e338f-132">


</div>

<span> </span>

</div>

</div>

</span></span></div>

