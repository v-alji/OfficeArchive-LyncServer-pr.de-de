---
title: 'Lync Server 2013: Durchstellung und Weiterleitung von Anrufen'
description: 'Lync Server 2013: Anruf Übertragungen und Anrufweiterleitung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call transfers and call forwarding
ms:assetid: 978610ec-63c7-4cf6-ad7a-9ef91559bf12
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994051(v=OCS.15)
ms:contentKeyID: 51803962
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9359cb64b386d022eab33e4523dfaccf784075b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435684"
---
# <a name="call-transfers-and-call-forwarding-in-lync-server-2013"></a>Durchstellung und Weiterleitung von Anrufen in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-03-09_

Wenn es sich um einen PSTN-Endpunkt handelt, analysiert Location-Based Routing die Position des Endpunkts der Calle und des Endpunkts, an dem der Anruf übertragen oder weitergeleitet wird (d. h. Übertragung/Forward-Ziel). Location-Based-Routing bestimmt, ob der Anruf je nach Position beider Endpunkte übertragen oder weitergeleitet werden soll.

In der folgenden Tabelle wird das Szenario eines lync-Benutzers in einem Anruf mit einem PSTN-Endpunkt veranschaulicht, und der lync-Benutzer übergibt den Anruf an einen anderen lync-Benutzer. Je nach dem Standort des Netzwerkstandorts des Endpunkts des Empfängers wirkt sich Location-Based Routing auf das Routing der Anrufweiterleitung oder Weiterleitung aus.

### <a name="initiating-call-transfer-or-forward"></a>Einleitung der Anrufdurchstellung oder -weiterleitung

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Benutzer, der die Durchstellung oder Weiterleitung des Anrufs einleitet</th>
<th>Der Zielendpunkt befindet sich am gleichen Netzwerkstandort wie der Benutzer, der die Anrufdurchstellung oder -weiterleitung einleitet</th>
<th>Der Zielendpunkt befindet sich an einem anderen Netzwerkstandort als der Benutzer, der die Anrufdurchstellung oder -weiterleitung einleitet</th>
<th>Der Zielendpunkt befindet sich auf der unbekannten Netzwerk Website oder-Netzwerk Website für Location-Based Routing nicht aktiviert</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Lync-Benutzer</p></td>
<td><p>Anrufweiterleitung oder -durchstellung ist erlaubt</p></td>
<td><p>Anrufweiterleitung oder -durchstellung ist nicht erlaubt</p></td>
<td><p>Anrufweiterleitung oder -durchstellung ist nicht erlaubt</p></td>
</tr>
</tbody>
</table>

  

Beispiel: ein lync-Benutzer in einem Anruf mit einem PSTN-Endpunkt übergibt den Anruf an einen anderen lync-Benutzer, der sich am gleichen Netzwerkstandort befindet. In diesem Fall ist die Durchstellung des Anrufs erlaubt.

In der folgenden Tabelle wird das Szenario eines lync-Benutzers in einem Anruf mit einem anderen lync-Benutzer veranschaulicht, und einer der Benutzer übergibt den Anruf an einen PSTN-Endpunkt. Die Tabelle zeigt im Detail, wie sich das standortbasierte Routing abhängig vom Standort des Benutzers, an den der Anruf durchgestellt werden soll, auf den Anruf auswirkt.

### <a name="call-transfer-or-forward-to-pstn-endpoint"></a>Anrufdurchstellung oder -weiterleitung an einen Endpunkt im öffentlichen Telefonnetz

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Zielendpunkt für die Anrufdurchstellung oder -weiterleitung</th>
<th>Lync-Benutzer auf derselben Netzwerk Website</th>
<th>Lync-Benutzer an verschiedenen Netzwerkstandorten</th>
<th>Ein oder beide lync-Benutzer in einer unbekannten Netzwerk Website oder Netzwerk Website sind für Location-Based Routing nicht aktiviert</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Endpunkt im öffentlichen Telefonnetz</p></td>
<td><p>Anrufweiterleitung oder -durchstellung wird von der VoIP-Routingrichtlinie am Standort des durchgestellten Benutzers zugelassen</p></td>
<td><p>Anrufweiterleitung oder -durchstellung wird von der VoIP-Routingrichtlinie am Standort des durchgestellten Benutzers zugelassen</p></td>
<td><p>Anrufweiterleitung oder -durchstellung wird von der VoIP-Richtlinie des durchgestellten Benutzers nur durch Trunks zugelassen, die nicht für standortbasiertes Routing aktiviert sind</p></td>
</tr>
</tbody>
</table>

  
Beispiel: ein lync-Benutzer in einem Anruf mit einem anderen lync-Benutzer, der sich am gleichen Netzwerkstandort befindet, übernimmt den Anruf an einen PSTN-Endpunkt, und die Anrufübertragung ist zulässig.

<div>

## <a name="see-also"></a>Siehe auch


[Szenarien für das standortbasierte Routing in Lync Server 2013](lync-server-2013-scenarios-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

