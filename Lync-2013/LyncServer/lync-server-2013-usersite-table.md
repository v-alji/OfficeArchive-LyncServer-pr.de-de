---
title: 'Lync Server 2013: UserSite-Tabelle'
description: 'Lync Server 2013: UserSite-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UserSite table
ms:assetid: 1c2a3cf2-dc05-472e-8097-a31f3a1aafcb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398256(v=OCS.15)
ms:contentKeyID: 48183552
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4e0fb3149b9378bbfd3f14da8176eed226e4f57f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436111"
---
# <a name="usersite-table-in-lync-server-2013"></a>UserSite-Tabelle in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2010-11-09_

Die Tabelle UserSite ist eine unterstützende Tabelle. Jeder Datensatz steht für eine Benutzer Website, die in der Netzwerk Konfigurationseinstellung definiert ist.


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><strong>Spalte</strong></th>
<th><strong>Datentyp</strong></th>
<th><strong>Schlüssel/Index</strong></th>
<th><strong>Details</strong></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>UserSiteKey</strong></p></td>
<td><p>int</p></td>
<td><p>Primary</p></td>
<td><p>Eindeutige Nummer, die die Benutzer Website kennzeichnet.</p></td>
</tr>
<tr class="even">
<td><p><strong>UserSiteName</strong></p></td>
<td><p>nvarchar (128)</p></td>
<td><p>Eindeutigen</p></td>
<td><p>Name der Benutzer Website.</p></td>
</tr>
<tr class="odd">
<td><p><strong>RegionKey</strong></p></td>
<td><p>int</p></td>
<td><p>Fremd</p></td>
<td><p>Referenziert aus der <a href="lync-server-2013-region-table.md">Regions Tabelle in lync Server 2013</a></p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

