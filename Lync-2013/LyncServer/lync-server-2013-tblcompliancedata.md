---
title: 'Lync Server 2013: tblComplianceData'
description: 'Lync Server 2013: tblComplianceData.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblComplianceData
ms:assetid: 05b28f9b-4aba-4b69-ba8d-2ceeb6cbfaac
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558606(v=OCS.15)
ms:contentKeyID: 48183308
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3c597d67054303de2753182b37419f68051d3af8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444476"
---
# <a name="tblcompliancedata-in-lync-server-2013"></a>tblComplianceData in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-12_

tblComplianceData enthält die Konformitätsereignisse, die noch nicht vom Kompatibilitätsadapter verarbeitet wurden.

### <a name="columns"></a>Spalten

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Spalte</th>
<th>Typ</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>cmplEventID</p></td>
<td><p>bigint, nicht NULL</p></td>
<td><p>Ereignis-ID.</p></td>
</tr>
<tr class="even">
<td><p>entryDate</p></td>
<td><p>smalldatetime, nicht NULL</p></td>
<td><p>Zeitpunkt der Einfügung (kann für cmplType = 9 weit in der Zukunft liegen, da der Eintrag nur ein Platzhalter in diesem Fall ist).</p></td>
</tr>
<tr class="odd">
<td><p>cmplType</p></td>
<td><p>int, nicht NULL</p></td>
<td><p>Art des Konformitäts Ereignisses:</p>
<ul>
<li><p>1: Chat</p></li>
<li><p>2: Backchat</p></li>
<li><p>3: Herunterladen von Dateien</p></li>
<li><p>4: Hochladen von Dateien</p></li>
<li><p>9: provisorische Dateiübertragung</p></li>
<li><p>10: Löschen des Chats (mit Replace)</p></li>
<li><p>11: Chat-Bereinigung</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>cmplTime</p></td>
<td><p>bigint, nicht NULL</p></td>
<td><p>Zeitstempel für das Ereignis.</p></td>
</tr>
<tr class="odd">
<td><p>cmplChannelUri</p></td>
<td><p>nvarchar (255); nicht NULL</p></td>
<td><p>Kanal Uniform Resource Identifier (URI).</p></td>
</tr>
<tr class="even">
<td><p>cmplChatID</p></td>
<td><p>bigint</p></td>
<td><p>Chat-ID (entsprechend der tblChat. Chat-Tabelle).</p></td>
</tr>
<tr class="odd">
<td><p>cmplUserID</p></td>
<td><p>int, nicht NULL</p></td>
<td><p>Prinzipal-ID des Plakats (entsprechend der tblPrincipal. prinID-Tabelle).</p></td>
</tr>
<tr class="even">
<td><p>cmplUserUri</p></td>
<td><p>nvarchar (255); nicht NULL</p></td>
<td><p>Benutzer-URI.</p></td>
</tr>
<tr class="odd">
<td><p>cmplMessage</p></td>
<td><p>nvarchar (max)</p></td>
<td><p>Nachricht (Codierung hängt von cmplType ab).</p></td>
</tr>
</tbody>
</table>


### <a name="key"></a>Key

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Spalte</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>cmplEventID</p></td>
<td><p>Primärschlüssel</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

