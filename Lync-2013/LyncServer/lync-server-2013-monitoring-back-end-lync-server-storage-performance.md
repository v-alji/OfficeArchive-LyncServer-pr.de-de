---
title: 'Lync Server 2013: Überwachen der Back-End-Speicherleistung von lync Server'
description: 'Lync Server 2013: Überwachen der Back-End-Speicherleistung von lync Server'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring back end Lync Server 2013 storage performance
ms:assetid: 71627c70-1953-4ac2-afbe-f3ad85be0f44
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720917(v=OCS.15)
ms:contentKeyID: 63969619
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e7501418d3589b941b7e92d2b414492c1d27a3ee
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394171"
---
# <a name="monitoring-back-end-lync-server-2013-storage-performance"></a>Überwachen der Back-End-Speicherleistung von lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2014-05-02_

Die lync Server 2013-Back-End-Datenbanken sind ein sehr wichtiger Bestandteil der lync Server 2013-Bereitstellung. Wir empfehlen, die Datenbanken und die jeweiligen Transaktionsprotokolle ständig zu überwachen, um sicherzustellen, dass das lync Server 2013-Back-End optimal ausgeführt wird.

In der folgenden Tabelle sind Leistungsindikatoren aufgeführt, die überwacht werden sollten, um Informationen zur Speicherleistung zu erhalten. Die Baselinewerte für diese Leistungsindikatoren müssen zuerst bestimmt werden (wenn das System die normale, erwartete Auslastung hat), um die Leistungsänderungen zu verstehen, wenn System beansprucht wird.

### <a name="performance-counters-to-be-monitored"></a>Zu überwachenden Leistungsindikatoren

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Leistungsindikator</th>
<th>Baseline-Schwellenwerte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Transaktionen/SEK (RTC)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Transaktionen/SEK (RTCDyn)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Transaktionen/SEK (tempdb)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Protokollleerungen/SEK (RTC)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Protokollleerungen/Sek. (RTCDyn)</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Protokollleerungen/SEK (tempdb)</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Datenträgerübertragungen/SEK (Read + Write)-RTC DB</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Datenträgerübertragungen/SEK-RTC-Protokoll</p></td>
<td></td>
</tr>
<tr class="odd">
<td><p>Datenträgerübertragungen/SEK-RTCDyn DB</p></td>
<td></td>
</tr>
<tr class="even">
<td><p>Datenträgerübertragungen/SEK-RTCdyn-Protokoll</p></td>
<td></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

