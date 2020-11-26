---
title: 'Lync Server 2013: Users-Tabelle'
description: 'Lync Server 2013: Benutzertabelle'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Users table
ms:assetid: a8d71373-4b57-4245-9f02-f7fc0d9fcd3c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412791(v=OCS.15)
ms:contentKeyID: 48185032
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9b1418e162a04e46ee0dfeca082aa66b0665fc77
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436181"
---
# <a name="users-table-in-lync-server-2013"></a>Users-Tabelle in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-28_

Die Tabelle Benutzer ist eine unterstützende Tabelle. Jeder Datensatz in der Tabelle speichert Informationen zu einem Benutzer an anrufen oder Sitzungen mit Datensätzen in der Datenbank.


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th>Spalte</th>
<th>Datentyp</th>
<th>Schlüssel/Index</th>
<th>Details</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>NextUpdateTS</strong></p></td>
<td><p>datetime</p></td>
<td></td>
<td><p>Zeitstempel für die interne Verwendung.</p></td>
</tr>
<tr class="even">
<td><p><strong>UserID</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>Eindeutige Nummer, die diesen Benutzer kennzeichnet.</p></td>
</tr>
<tr class="odd">
<td><p><strong>UserUri</strong></p></td>
<td><p>nvarchar (450)</p></td>
<td><p> </p></td>
<td><p>Benutzer-URI.</p></td>
</tr>
<tr class="even">
<td><p><strong>Mandanten</strong></p></td>
<td><p>int</p></td>
<td><p>Fremd</p></td>
<td><p>Die Mandanten-ID des Benutzers. Weitere Informationen finden Sie <a href="lync-server-2013-tenants-table.md">in der Tabelle Mandanten in lync Server 2013</a> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>UriTypeId</strong></p></td>
<td><p>int</p></td>
<td><p>Fremd</p></td>
<td><p>Der URI-Typ des Benutzers. Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

