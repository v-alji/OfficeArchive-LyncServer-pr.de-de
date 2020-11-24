---
title: 'Lync Server 2013: tblADCookie'
description: 'Lync Server 2013: tblADCookie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblADCookie
ms:assetid: 0a9102c4-47aa-40ea-8a0d-20e72ab09848
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558610(v=OCS.15)
ms:contentKeyID: 48183366
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 41c3dde3730ede07b204a473c7fe0a5ab68054d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394346"
---
# <a name="tbladcookie-in-lync-server-2013"></a><span data-ttu-id="e44a2-103">tblADCookie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e44a2-103">tblADCookie in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e44a2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e44a2-104">

<span> </span></span></span>

<span data-ttu-id="e44a2-105">_**Letztes Änderungsdatum des Themas:** 2012-06-25_</span><span class="sxs-lookup"><span data-stu-id="e44a2-105">_**Topic Last Modified:** 2012-06-25_</span></span>

<span data-ttu-id="e44a2-106">tblADCookie enthält die aktuellen LDAP-Synchronisierungs Cookies (Lightweight Directory Access Protocol).</span><span class="sxs-lookup"><span data-stu-id="e44a2-106">tblADCookie contains the current Lightweight Directory Access Protocol (LDAP) Sync cookies.</span></span>

### <a name="columns"></a><span data-ttu-id="e44a2-107">Spalten</span><span class="sxs-lookup"><span data-stu-id="e44a2-107">Columns</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e44a2-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="e44a2-108">Column</span></span></th>
<th><span data-ttu-id="e44a2-109">Typ</span><span class="sxs-lookup"><span data-stu-id="e44a2-109">Type</span></span></th>
<th><span data-ttu-id="e44a2-110">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e44a2-110">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e44a2-111">prinGuid</span><span class="sxs-lookup"><span data-stu-id="e44a2-111">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="e44a2-112">GUID, nicht NULL</span><span class="sxs-lookup"><span data-stu-id="e44a2-112">GUID, not null</span></span></p></td>
<td><p><span data-ttu-id="e44a2-113">Prinzipal-GUID der zu überwachenden Domäne.</span><span class="sxs-lookup"><span data-stu-id="e44a2-113">Principal GUID of the domain being monitored.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e44a2-114">prinDCHost</span><span class="sxs-lookup"><span data-stu-id="e44a2-114">prinDCHost</span></span></p></td>
<td><p><span data-ttu-id="e44a2-115">nvarchar (255)</span><span class="sxs-lookup"><span data-stu-id="e44a2-115">nvarchar (255)</span></span></p></td>
<td><p><span data-ttu-id="e44a2-116">Vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des aktuellen Domänencontrollers, der für die Synchronisierung von Active Directory-Domänendiensten verwendet wird. Hat einen Informationswert.</span><span class="sxs-lookup"><span data-stu-id="e44a2-116">Fully qualified domain name (FQDN) of the current domain controller used for Active Directory Domain Services Sync. Has informational value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e44a2-117">adcContent</span><span class="sxs-lookup"><span data-stu-id="e44a2-117">adcContent</span></span></p></td>
<td><p><span data-ttu-id="e44a2-118">Bild (binär)</span><span class="sxs-lookup"><span data-stu-id="e44a2-118">image (binary)</span></span></p></td>
<td><p><span data-ttu-id="e44a2-119">Active Directory-Synchronisierungs Cookie</span><span class="sxs-lookup"><span data-stu-id="e44a2-119">Active Directory Sync cookie.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e44a2-120">lastUpdated</span><span class="sxs-lookup"><span data-stu-id="e44a2-120">lastUpdated</span></span></p></td>
<td><p><span data-ttu-id="e44a2-121">datetime</span><span class="sxs-lookup"><span data-stu-id="e44a2-121">datetime</span></span></p></td>
<td><p><span data-ttu-id="e44a2-122">Zeitstempel mit der Zeilen Aktualisierungszeit.</span><span class="sxs-lookup"><span data-stu-id="e44a2-122">Time stamp with the row update time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e44a2-123">lockedUntil</span><span class="sxs-lookup"><span data-stu-id="e44a2-123">lockedUntil</span></span></p></td>
<td><p><span data-ttu-id="e44a2-124">datetime</span><span class="sxs-lookup"><span data-stu-id="e44a2-124">datetime</span></span></p></td>
<td><p><span data-ttu-id="e44a2-125">Zeit, bis die Zeile für Änderungen gesperrt ist.</span><span class="sxs-lookup"><span data-stu-id="e44a2-125">Time until the row is locked for changes.</span></span> <span data-ttu-id="e44a2-126">Dies ist Teil eines Software-Interlock-Mechanismus, der sicherstellt, dass nur einer der Chat Dienste die Active Directory-Synchronisierung gleichzeitig durchführt.</span><span class="sxs-lookup"><span data-stu-id="e44a2-126">This is part of a software interlock mechanism that ensures that only one of the chat services does the Active Directory Sync at a time.</span></span></p></td>
</tr>
</tbody>
</table>


### <a name="keys"></a><span data-ttu-id="e44a2-127">Schlüssel</span><span class="sxs-lookup"><span data-stu-id="e44a2-127">Keys</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e44a2-128">Spalte (n)</span><span class="sxs-lookup"><span data-stu-id="e44a2-128">Column(s)</span></span></th>
<th><span data-ttu-id="e44a2-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="e44a2-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e44a2-130">prinGuid</span><span class="sxs-lookup"><span data-stu-id="e44a2-130">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="e44a2-131">Primärschlüssel</span><span class="sxs-lookup"><span data-stu-id="e44a2-131">Primary key.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e44a2-132">prinGuid</span><span class="sxs-lookup"><span data-stu-id="e44a2-132">prinGuid</span></span></p></td>
<td><p><span data-ttu-id="e44a2-133">Fremdschlüssel mit Lookup in der Principal. prinGuid-Tabelle.</span><span class="sxs-lookup"><span data-stu-id="e44a2-133">Foreign key with lookup in Principal.prinGuid table.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="e44a2-134">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e44a2-134">


</div>

<span> </span>

</div>

</div>

</span></span></div>

