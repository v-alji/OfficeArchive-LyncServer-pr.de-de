---
title: 'Lync Server 2013: tblChat'
description: 'Lync Server 2013: tblChat.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: tblChat
ms:assetid: b7fcf1b4-7a3f-4585-a6d9-95e7f030c7dc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615031(v=OCS.15)
ms:contentKeyID: 48185203
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e68d4f0d1ca7ae227c78c95d02e02ffc81656feb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423547"
---
# <a name="tblchat-in-lync-server-2013"></a>tblChat in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-12_

tblChat enthält alle Chatnachrichten.

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
<td><p>Kanal-Nr</p></td>
<td><p>int, nicht NULL</p></td>
<td><p>Knoten-ID.</p></td>
</tr>
<tr class="even">
<td><p>Chat-Funktion</p></td>
<td><p>bigint, nicht NULL</p></td>
<td><p>Eindeutige sequenzielle Nummer (pro Knoten-ID), die die von der tblLastChatId-Tabelle generierte Chatroom-Reihenfolge definiert.</p></td>
</tr>
<tr class="odd">
<td><p>chatDate</p></td>
<td><p>bigint, nicht NULL</p></td>
<td><p>Zeitstempel für die Chatnachricht.</p></td>
</tr>
<tr class="even">
<td><p>UserID</p></td>
<td><p>int, nicht NULL</p></td>
<td><p>Prinzipal-ID des Plakats.</p></td>
</tr>
<tr class="odd">
<td><p>isalert</p></td>
<td><p>Bit, nicht NULL</p></td>
<td><p>"True", wenn es sich bei der Nachricht um eine Warnmeldung handelt. False, wenn dies nicht der Fall ist.</p></td>
</tr>
<tr class="even">
<td><p>Inhalts</p></td>
<td><p>nvarchar (max), nicht NULL</p></td>
<td><p>Chat-Inhalt (die nur-Text-Version). Der Inhalt befindet sich normalerweise im nur-Text-Stil mit den folgenden Ausnahmen:</p>
<ul>
<li><p>Dateien werden als MA-FileLink: Links dargestellt.</p></li>
<li><p>Links werden als HTML-Element dargestellt (auch wenn der Inhaltstyp nicht als HTML betrachtet werden kann).</p></li>
<li><p>Stories werden als "[Story]...."-ähnliches Format codiert.</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>RTF</p></td>
<td><p>varchar (max)</p></td>
<td><p>Chat-Inhalt (die RTF-Version). Kann NULL sein, wenn der Client Sie nicht bereitstellt.</p></td>
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
<td><p>&lt;Kanal-Nr, Chat&gt;</p></td>
<td><p>Primärschlüssel</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

