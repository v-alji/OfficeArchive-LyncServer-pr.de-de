---
title: 'Lync Server 2013: Abläufe für das Parken von Anrufen während des Ausfalls eines Pools'
description: 'Lync Server 2013: Anruf parken während eines Pool Fehlers.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Park experience during pool failure
ms:assetid: f6303e69-8771-492a-9e8b-c3d7ba231309
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205383(v=OCS.15)
ms:contentKeyID: 48185831
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b97a0af13d378b0753979c32b6d5ffe7a525cf0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435698"
---
# <a name="call-park-experience-in-lync-server-2013-during-pool-failure"></a>Abläufe für das Parken von Anrufen in Lync Server 2013 während des Ausfalls eines Pools

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-10_

Wenn ein Front-End-Pool aufgrund eines ungeplanten Vorfalls nicht mehr zur Verfügung steht, werden Anrufe, die geparkt, aber noch nicht abgerufen wurden, getrennt. Beim Failover zu einem Sicherungspool werden die Benutzer in den Sicherungspool umgeleitet und befinden sich im Widerstands Modus. Im Resilienz-Modus können Benutzer keine Anrufe parken, aber Sie können Anrufe in Wartestellung setzen und übertragen. Nach Abschluss des Failovers können Anrufe wieder wie gewohnt abgestellt und abgerufen werden. Während des Failback können Benutzer Anrufe erst dann Parken, wenn Sie den Stabilitäts Modus verlassen.

Während der Disaster Recovery verwenden Benutzer, die im Rahmen des Failovers an den Backup-Pool umgeleitet wurden, die Anwendung Parken, die im Backup-Pool bereitgestellt wird. Daher verwenden Benutzer, die an den Sicherungspool umgeleitet werden, die Einstellungen für den Anruf Park, die für die Anwendung "Parken" im Sicherungspool konfiguriert sind.

In der folgenden Tabelle sind die Erfahrungen des Anruf Parks in den Phasen der Disaster Recovery zusammengefasst.

### <a name="user-experience-during-disaster-recovery"></a>Benutzererfahrung bei der Disaster Recovery

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Anruf Zustand</th>
<th>Wenn ein Ausfall eintritt</th>
<th>Während des Failovers</th>
<th>Während des Failbacks</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Noch nicht geparkter Anruf</p></td>
<td><p>Der Anruf bleibt verbunden, kann aber nicht abgestellt werden.</p></td>
<td><ul>
<li><p>Während des Failovers kann der Anruf nicht abgestellt werden, während sich die Benutzer im Resilienz-Modus befinden, können aber in Wartestellung gesetzt und übertragen werden.</p></li>
<li><p>Nach Abschluss des Failovers kann der Anruf abgestellt und abgerufen werden.</p></li>
</ul></td>
<td><ul>
<li><p>Während des Failback kann der Anruf nicht abgestellt werden, während sich die Benutzer im Resilienz-Modus befinden, können aber in Wartestellung gesetzt und übertragen werden.</p></li>
<li><p>Nach Abschluss des Failback kann der Anruf abgestellt und abgerufen werden.</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>Anruf abgestellt, aber noch nicht abgerufen</p></td>
<td><p>Der Anruf wird getrennt.</p></td>
<td><p>Keine Anrufe in diesem Zustand.</p></td>
<td><p>Der Anruf bleibt geparkt.</p></td>
</tr>
<tr class="odd">
<td><p>Geparkten Anruf bereits abgerufen</p></td>
<td><p>Der Anruf bleibt verbunden.</p></td>
<td><p>Der Anruf bleibt verbunden.</p></td>
<td><p>Der Anruf bleibt verbunden.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

