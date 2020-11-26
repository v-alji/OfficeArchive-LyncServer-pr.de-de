---
title: 'Lync Server 2013: Paralleles Anrufen'
description: 'Lync Server 2013: Gleichzeitiges Klingeln.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Simultaneous ringing
ms:assetid: df02f919-4d50-4832-9300-6c51f8b4fc56
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994079(v=OCS.15)
ms:contentKeyID: 51803990
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 595c8c1d4ce105e2189002f18733ffae92cff8bf
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423820"
---
# <a name="simultaneous-ringing-in-lync-server-2013"></a><span data-ttu-id="1f56a-103">Paralleles Anrufen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1f56a-103">Simultaneous ringing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1f56a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1f56a-104">

<span> </span></span></span>

<span data-ttu-id="1f56a-105">_**Letztes Änderungsdatum des Themas:** 2013-03-09_</span><span class="sxs-lookup"><span data-stu-id="1f56a-105">_**Topic Last Modified:** 2013-03-09_</span></span>

<span data-ttu-id="1f56a-106">Wenn der angerufene Teilnehmer das gleichzeitige Klingeln aktiviert hat, analysiert Location-Based Routing den Standort des anrufenden und die Endpunkte der angerufenen Parteien, um zu ermitteln, ob der Anruf weitergeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f56a-106">When the called party has simultaneous ringing enabled, Location-Based Routing analyzes the location of the calling party and the endpoints of the called parties to determine whether the call should be routed.</span></span>

<span data-ttu-id="1f56a-107">Die folgende Tabelle zeigt einen Benutzer, für den paralleles Anrufen konfiguriert ist, und das Ziel des parallelen Anrufs ist ein Benutzer am gleichen oder einem unbekannten Netzwerkstandort.</span><span class="sxs-lookup"><span data-stu-id="1f56a-107">The following table illustrates a user configured with simultaneous ringing, and the simultaneous ringing target is a user in the same network site, in a different network site, or in an unknown network site.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f56a-108">Eingehender Anruf aus dem öffentlichen Telefonnetz für</span><span class="sxs-lookup"><span data-stu-id="1f56a-108">Incoming PSTN call for</span></span></th>
<th><span data-ttu-id="1f56a-109">Am gleichen Netzwerkstandort wie der Angerufene</span><span class="sxs-lookup"><span data-stu-id="1f56a-109">Located in the same network site as callee</span></span></th>
<th><span data-ttu-id="1f56a-110">An einem anderen Netzwerkstandort als der Angerufene</span><span class="sxs-lookup"><span data-stu-id="1f56a-110">Located in different network site than callee</span></span></th>
<th><span data-ttu-id="1f56a-111">Befindet sich auf der unbekannten Netzwerk Website oder ist für Location-Based Routing nicht aktiviert</span><span class="sxs-lookup"><span data-stu-id="1f56a-111">Located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f56a-112">Lync-Benutzer</span><span class="sxs-lookup"><span data-stu-id="1f56a-112">Lync user</span></span></p></td>
<td><p><span data-ttu-id="1f56a-113">Paralleles Anrufen zugelassen</span><span class="sxs-lookup"><span data-stu-id="1f56a-113">Simultaneous ring allowed</span></span></p></td>
<td><p><span data-ttu-id="1f56a-114">Paralleles Anrufen nicht zugelassen</span><span class="sxs-lookup"><span data-stu-id="1f56a-114">Simultaneous ring not allowed</span></span></p></td>
<td><p><span data-ttu-id="1f56a-115">Paralleles Anrufen nicht zugelassen</span><span class="sxs-lookup"><span data-stu-id="1f56a-115">Simultaneous ring not allowed</span></span></p></td>
</tr>
</tbody>
</table>

  
<span data-ttu-id="1f56a-116">In der folgenden Tabelle wird ein Anruf eines lync-Benutzers (also lync-Anrufers) auf derselben Netzwerk Website, in einer anderen Netzwerk Website oder auf einer unbekannten Netzwerk Website veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="1f56a-116">The following table illustrates a call from a Lync user (i.e. Lync caller) in the same network site, in a different network site, or from an unknown network site.</span></span> <span data-ttu-id="1f56a-117">Der Angerufene hat einen Endpunkt im öffentlichen Telefonfestnetz (z. B. ein Mobiltelefon), der als Ziel für paralleles Anrufen konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="1f56a-117">The callee has a PSTN endpoint (i.e. cellphone) configured as a simultaneous ring target.</span></span> <span data-ttu-id="1f56a-118">In diesem Szenario wird Location-Based-Routing feststellen, ob der Anruf an das Ziel für das gleichzeitige Klingeln (also das Mobiltelefon) des angerufenen weitergeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="1f56a-118">In this scenario, Location-Based Routing will determine whether the call should be routed to the simultaneous ring target (i.e. cellphone) of the callee or not.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="1f56a-119">Ziel für paralleles Anrufen</span><span class="sxs-lookup"><span data-stu-id="1f56a-119">Simultaneous ring target</span></span></th>
<th><span data-ttu-id="1f56a-120">Am gleichen Netzwerkstandort wie der Angerufene</span><span class="sxs-lookup"><span data-stu-id="1f56a-120">Located in the same network site as callee</span></span></th>
<th><span data-ttu-id="1f56a-121">An einem anderen Netzwerkstandort als der Angerufene</span><span class="sxs-lookup"><span data-stu-id="1f56a-121">Located in different network site than callee</span></span></th>
<th><span data-ttu-id="1f56a-122">Befindet sich auf der unbekannten Netzwerk Website oder ist für Location-Based Routing nicht aktiviert</span><span class="sxs-lookup"><span data-stu-id="1f56a-122">Located in unknown network site or not enabled for Location-Based Routing</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1f56a-123">Endpunkt im öffentlichen Telefonnetz</span><span class="sxs-lookup"><span data-stu-id="1f56a-123">PSTN endpoint</span></span></p></td>
<td><p><span data-ttu-id="1f56a-124">Paralleles Anrufen durch die VoIP-Weiterleitungsrichtline am Standort des Anrufers zugelassen</span><span class="sxs-lookup"><span data-stu-id="1f56a-124">Simultaneous ring allowed through the caller’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="1f56a-125">Paralleles Anrufen durch die VoIP-Weiterleitungsrichtline am Standort des Anrufers zugelassen</span><span class="sxs-lookup"><span data-stu-id="1f56a-125">Simultaneous ring allowed through the caller’s site voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="1f56a-126">Paralleles Anrufen durch die VoIP-Weiterleitungsrichtlinie an Trunks, die nicht für standortbasiertes Routing aktiviert sind, zugelassen</span><span class="sxs-lookup"><span data-stu-id="1f56a-126">Simultaneous ring allowed through the caller’s voice policy to trunks not enabled for Location-Based Routing</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a><span data-ttu-id="1f56a-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1f56a-127">See Also</span></span>


[<span data-ttu-id="1f56a-128">Szenarien für das standortbasierte Routing in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1f56a-128">Scenarios for Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-scenarios-for-location-based-routing.md)  
  

<span data-ttu-id="1f56a-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1f56a-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

