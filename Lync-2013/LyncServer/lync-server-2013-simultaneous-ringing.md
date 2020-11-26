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
# <a name="simultaneous-ringing-in-lync-server-2013"></a>Paralleles Anrufen in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-03-09_

Wenn der angerufene Teilnehmer das gleichzeitige Klingeln aktiviert hat, analysiert Location-Based Routing den Standort des anrufenden und die Endpunkte der angerufenen Parteien, um zu ermitteln, ob der Anruf weitergeleitet werden soll.

Die folgende Tabelle zeigt einen Benutzer, für den paralleles Anrufen konfiguriert ist, und das Ziel des parallelen Anrufs ist ein Benutzer am gleichen oder einem unbekannten Netzwerkstandort.


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Eingehender Anruf aus dem öffentlichen Telefonnetz für</th>
<th>Am gleichen Netzwerkstandort wie der Angerufene</th>
<th>An einem anderen Netzwerkstandort als der Angerufene</th>
<th>Befindet sich auf der unbekannten Netzwerk Website oder ist für Location-Based Routing nicht aktiviert</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Lync-Benutzer</p></td>
<td><p>Paralleles Anrufen zugelassen</p></td>
<td><p>Paralleles Anrufen nicht zugelassen</p></td>
<td><p>Paralleles Anrufen nicht zugelassen</p></td>
</tr>
</tbody>
</table>

  
In der folgenden Tabelle wird ein Anruf eines lync-Benutzers (also lync-Anrufers) auf derselben Netzwerk Website, in einer anderen Netzwerk Website oder auf einer unbekannten Netzwerk Website veranschaulicht. Der Angerufene hat einen Endpunkt im öffentlichen Telefonfestnetz (z. B. ein Mobiltelefon), der als Ziel für paralleles Anrufen konfiguriert ist. In diesem Szenario wird Location-Based-Routing feststellen, ob der Anruf an das Ziel für das gleichzeitige Klingeln (also das Mobiltelefon) des angerufenen weitergeleitet werden soll.


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Ziel für paralleles Anrufen</th>
<th>Am gleichen Netzwerkstandort wie der Angerufene</th>
<th>An einem anderen Netzwerkstandort als der Angerufene</th>
<th>Befindet sich auf der unbekannten Netzwerk Website oder ist für Location-Based Routing nicht aktiviert</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Endpunkt im öffentlichen Telefonnetz</p></td>
<td><p>Paralleles Anrufen durch die VoIP-Weiterleitungsrichtline am Standort des Anrufers zugelassen</p></td>
<td><p>Paralleles Anrufen durch die VoIP-Weiterleitungsrichtline am Standort des Anrufers zugelassen</p></td>
<td><p>Paralleles Anrufen durch die VoIP-Weiterleitungsrichtlinie an Trunks, die nicht für standortbasiertes Routing aktiviert sind, zugelassen</p></td>
</tr>
</tbody>
</table>


<div>

## <a name="see-also"></a>Siehe auch


[Szenarien für das standortbasierte Routing in Lync Server 2013](lync-server-2013-scenarios-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

