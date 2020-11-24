---
title: 'Lync Server 2013: PSTN-Verwendungsdatensätze'
description: 'Lync Server 2013: PSTN-Verwendungsdaten Sätze.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN usage records
ms:assetid: b5f624aa-abe8-455b-a8e3-c228be230463
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412878(v=OCS.15)
ms:contentKeyID: 48185188
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0f8ff428dc2fa5cf8cf0f10e37f0f79c38d70d70
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394578"
---
# <a name="pstn-usage-records-in-lync-server-2013"></a>PSTN-Verwendungsdatensätze in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-23_

Die Planung von PSTN-Nutzungsdaten Sätzen besteht hauptsächlich darin, alle Anrufberechtigungen aufzulisten, die derzeit in Ihrer Organisation gelten, vom CEO bis hin zu Leiharbeitern, Beratern und Kontingenten Mitarbeitern. Dieser Prozess bietet auch die Möglichkeit, vorhandene Anrufberechtigungen erneut zu überprüfen und zu überarbeiten. Sie können PSTN-Verwendungsdaten Sätze nur für diese Anrufberechtigungen erstellen, die für Ihre erwarteten Enterprise-VoIP-Benutzer gelten, doch eine bessere Lösung mit langer Reichweite könnte darin liegen, PSTN-Verwendungsdaten Sätze für alle Anrufberechtigungen zu erstellen, und zwar unabhängig davon, ob einige derzeit nicht für die Gruppe von Benutzern gelten, die für Enterprise-VoIP aktiviert werden sollen. Wenn sich die Anrufberechtigungen ändern oder neue Benutzer mit unterschiedlichen Anrufberechtigungen hinzugefügt werden, haben Sie bereits die erforderlichen PSTN-Nutzungsdatensätze erstellt.

Im Folgenden sehen Sie eine typische PSTN-Verwendungstabelle.

### <a name="pstn-usage-records"></a>PSTN-Verwendungseinträge

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Telefonattribut</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Local</p></td>
<td><p>Ortsgespräche</p></td>
</tr>
<tr class="even">
<td><p>Long-Distance</p></td>
<td><p>Ferngespräche</p></td>
</tr>
<tr class="odd">
<td><p>International</p></td>
<td><p>Auslandsgespräche</p></td>
</tr>
<tr class="even">
<td><p>Delhi</p></td>
<td><p>Vollzeitmitarbeiter in Delhi</p></td>
</tr>
<tr class="odd">
<td><p>Redmond</p></td>
<td><p>Vollzeitmitarbeiter in Redmond</p></td>
</tr>
<tr class="even">
<td><p>RedmondTemps</p></td>
<td><p>Zeitarbeiter in Redmond</p></td>
</tr>
<tr class="odd">
<td><p>Zurich</p></td>
<td><p>Vollzeitmitarbeiter in Zürich</p></td>
</tr>
</tbody>
</table>


PSTN-Verwendungseinträge alleine führen keine Aktionen aus. Um sie verwenden zu können, müssen Sie sie mit Folgendem verknüpfen:

  - VoIP-Richtlinien, die Benutzern zugewiesen sind

  - Routen, die Rufnummern zugewiesen sind

Details zu VoIP-Richtlinien und-Routen finden Sie unter [VoIP-Richtlinien in lync Server 2013](lync-server-2013-voice-policies.md) und [VoIP-Routen in lync Server 2013](lync-server-2013-voice-routes.md). Ausführliche Informationen zum Erstellen und Konfigurieren von [VoIP-Routen für ausgehende Anrufe finden Sie in lync Server 2013](lync-server-2013-configuring-voice-routes-for-outbound-calls.md).

</div>

<span> </span>

</div>

</div>

</div>

