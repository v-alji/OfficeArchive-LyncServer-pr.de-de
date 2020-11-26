---
title: 'Lync Server 2013: VoIPDetails-Ansicht'
description: 'Lync Server 2013: VoIPDetails-Ansicht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VoIPDetails view
ms:assetid: 14c44736-71ba-4fc5-82c7-1df65bf6261c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687973(v=OCS.15)
ms:contentKeyID: 49733561
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5ecd34be0c8568eef29d773f088e8503a8065743
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446184"
---
# <a name="voipdetails-view-in-lync-server-2013"></a><span data-ttu-id="b158f-103">VoIPDetails-Ansicht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b158f-103">VoIPDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b158f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b158f-104">

<span> </span></span></span>

<span data-ttu-id="b158f-105">_**Letztes Änderungsdatum des Themas:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="b158f-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="b158f-106">In der VoIPDetails-Ansicht werden Informationen zu Peer-to-Peer-Sitzungen gespeichert, wobei mindestens ein Benutzer ein VoIP-Benutzer ist.</span><span class="sxs-lookup"><span data-stu-id="b158f-106">The VoIPDetails view stores information about peer-to-peer sessions, where at least one user is a VoIP user.</span></span> <span data-ttu-id="b158f-107">Diese Ansicht wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b158f-107">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b158f-108">Die VoIPDetails-Ansicht enthält alle Spalten in der <A href="lync-server-2013-sessiondetails-view.md">SessionDetails-Ansicht in lync Server 2013</A> sowie die unten aufgeführten Spalten.</span><span class="sxs-lookup"><span data-stu-id="b158f-108">The VoIPDetails view contains all of the columns in the <A href="lync-server-2013-sessiondetails-view.md">SessionDetails view in Lync Server 2013</A> in addition the columns listed below.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b158f-109">Spalte</span><span class="sxs-lookup"><span data-stu-id="b158f-109">Column</span></span></th>
<th><span data-ttu-id="b158f-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="b158f-110">Data Type</span></span></th>
<th><span data-ttu-id="b158f-111">Details</span><span class="sxs-lookup"><span data-stu-id="b158f-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b158f-112"><strong>Vom Telefon</strong></span><span class="sxs-lookup"><span data-stu-id="b158f-112"><strong>FromPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="b158f-113">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="b158f-113">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="b158f-114">Telefon-URI des Benutzers, der die Sitzung gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="b158f-114">Phone URI of the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b158f-115"><strong>Tophone</strong></span><span class="sxs-lookup"><span data-stu-id="b158f-115"><strong>ToPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="b158f-116">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="b158f-116">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="b158f-117">Telefon-URI des Benutzers, der der Sitzung beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b158f-117">Phone URI of the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b158f-118"><strong>DisconnectedByUri</strong></span><span class="sxs-lookup"><span data-stu-id="b158f-118"><strong>DisconnectedByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="b158f-119">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="b158f-119">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="b158f-120">Der URI des Benutzers, der die Sitzung getrennt hat.</span><span class="sxs-lookup"><span data-stu-id="b158f-120">URI of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b158f-121"><strong>DisconnectedByUriType</strong></span><span class="sxs-lookup"><span data-stu-id="b158f-121"><strong>DisconnectedByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="b158f-122">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b158f-122">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b158f-123">Der Typ des URIs des Benutzers, der die Sitzung getrennt hat.</span><span class="sxs-lookup"><span data-stu-id="b158f-123">Type of URI of the user who disconnected the session.</span></span> <span data-ttu-id="b158f-124">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="b158f-124">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b158f-125"><strong>DisconnectedByTenant</strong></span><span class="sxs-lookup"><span data-stu-id="b158f-125"><strong>DisconnectedByTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="b158f-126">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b158f-126">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b158f-127">Der Mandant des Benutzers, der die Sitzung getrennt hat.</span><span class="sxs-lookup"><span data-stu-id="b158f-127">Tenant of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b158f-128"><strong>DisconnectedByPhone</strong></span><span class="sxs-lookup"><span data-stu-id="b158f-128"><strong>DisconnectedByPhone</strong></span></span></p></td>
<td><p><span data-ttu-id="b158f-129">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="b158f-129">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="b158f-130">Telefon-URI des Benutzers, der die Sitzung getrennt hat.</span><span class="sxs-lookup"><span data-stu-id="b158f-130">Phone URI of the user who disconnected the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b158f-131"><strong>FromMediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="b158f-131"><strong>FromMediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="b158f-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b158f-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b158f-133">Der von dem Benutzer, der die Sitzung gestartet hat, verwendete Vermittlungs Server.</span><span class="sxs-lookup"><span data-stu-id="b158f-133">Mediation Server used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b158f-134"><strong>ToMediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="b158f-134"><strong>ToMediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="b158f-135">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b158f-135">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b158f-136">Vermittlungs Server, der von dem Benutzer verwendet wird, der der Sitzung beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b158f-136">Mediation Server used by the user who joined the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b158f-137"><strong>FromGateway</strong></span><span class="sxs-lookup"><span data-stu-id="b158f-137"><strong>FromGateway</strong></span></span></p></td>
<td><p><span data-ttu-id="b158f-138">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b158f-138">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b158f-139">Gateway, das vom Benutzer verwendet wird, der die Sitzung gestartet hat.</span><span class="sxs-lookup"><span data-stu-id="b158f-139">Gateway used by the user who started the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b158f-140"><strong>Togateway</strong></span><span class="sxs-lookup"><span data-stu-id="b158f-140"><strong>ToGateway</strong></span></span></p></td>
<td><p><span data-ttu-id="b158f-141">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="b158f-141">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="b158f-142">Gateway, das vom Benutzer verwendet wird, der der Sitzung beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="b158f-142">Gateway used by the user who joined the session.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="b158f-143">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b158f-143">


</div>

<span> </span>

</div>

</div>

</span></span></div>

