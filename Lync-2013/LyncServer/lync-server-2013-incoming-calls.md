---
title: 'Lync Server 2013: Eingehende Anrufe'
description: 'Lync Server 2013: eingehende Anrufe.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Incoming calls
ms:assetid: 65b9c1b4-6af7-4527-8c33-22c4442bd209
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994038(v=OCS.15)
ms:contentKeyID: 51803948
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a72c7fc378240f9751eae8e6c24e9cc601b08d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427299"
---
# <a name="incoming-calls-in-lync-server-2013"></a>Eingehende Anrufe in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-03-09_

Die Weiterleitung eingehender Anrufe an Benutzer, die für Location-Based Routing aktiviert sind, hängt von der Position des Endpunkts des Benutzers ab. Die Weiterleitung eingehender Anrufe ist auf die folgende Weise betroffen. Wenn ein Benutzer einen eingehenden Anruf an einem Endpunkt hat, der sich in einer Location-Based Routing fähigen Netzwerk Website befindet, und sich der Endpunkt am gleichen Netzwerkstandort wie das PSTN-Gateway befindet, wird der Anruf weitergeleitet. Wenn ein Benutzer einen eingehenden Anruf an einem Endpunkt hat, der sich in einer Location-Based Routing fähigen Netzwerk Website befindet, und sich der Endpunkt an einem anderen Netzwerkstandort als dem PSTN-Gateway befindet, wird der Anruf nicht weitergeleitet. Wenn ein Benutzer keine Endpunkte an derselben Netzwerk Website wie das PSTN-Gateway hat, von dem der eingehende Anruf stammt, wird der eingehende Anruf direkt an die Voicemail des Benutzers weitergeleitet, und eine Benachrichtigung über verpasste Anrufe wird an den angerufenen Teilnehmer gesendet.

Die Einstellungen für die Anrufweiterleitung eines Benutzers, der für Location-Based Routing aktiviert ist, werden weiterhin erzwungen, die weitergeleiteten Anrufe unterliegen jedoch Location-Based Routing Einschränkungen des Benutzers.

Die folgende Tabelle zeigt, wie sich Location-Based Routing auf das Routing von eingehenden Anrufen auswirkt, abhängig von der Position des Endpunkts des aufgerufenen. Die Netzwerk Website des PSTN-Gateways ist für Location-Based Routing aktiviert, und Location-Based Routing ermöglicht nur das Routing von PSTN-Anrufen an Endpunkte innerhalb desselben Netzwerkstandorts.

### <a name="callee-receiving-an-inbound-call-from-the-pstn"></a>Angerufener empfängt einen eingehenden Anruf aus dem Telefonfestnetz (PSTN)

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th>Endgerät des Angerufenen befindet sich am selben Netzwerkstandort wie das PSTN-Gateway</th>
<th>Endgerät des Angerufenen befindet sich nicht am selben Netzwerkstandort wie das PSTN-Gateway</th>
<th>Endgerät des Angerufenen befindet sich an einem unbekannten Netzwerkstandort oder ist nicht für standortbasiertes Routing aktiviert</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Routing eines eingehenden Telefonfestnetzanrufs</p></td>
<td><p>Eingehender Anruf wird an die Endgeräte des Angerufenen weitergeleitet</p></td>
<td><p>Eingehender Anruf wird nicht an die Endgeräte des Angerufenen weitergeleitet</p></td>
<td><p>Eingehender Anruf wird nicht an die Endgeräte des Angerufenen weitergeleitet</p></td>
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

