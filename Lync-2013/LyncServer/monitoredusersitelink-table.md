---
title: MonitoredUserSiteLink-Tabelle
description: MonitoredUserSiteLink-Tabelle.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: MonitoredUserSiteLink table
ms:assetid: 16edc24a-2718-4bb4-b05c-bc7aafa97963
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398233(v=OCS.15)
ms:contentKeyID: 48183508
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07c0ae8fba03f3720cbc293657d2fb08f6a98a7e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443762"
---
# <a name="monitoredusersitelink-table"></a>MonitoredUserSiteLink-Tabelle

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-02_

Die Tabelle MonitoredUserSiteLink ist eine unterstützende Tabelle. Jeder Datensatz steht für einen Link zwischen zwei Benutzer Websites.


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
<td><p><strong>UserSite1Key</strong></p></td>
<td><p>int</p></td>
<td><p>Primär, fremd</p></td>
<td><p>Wird in der <a href="lync-server-2013-usersite-table.md">UserSite-Tabelle in lync Server 2013</a>referenziert.</p></td>
</tr>
<tr class="even">
<td><p><strong>UserSite2Key</strong></p></td>
<td><p>int</p></td>
<td><p>Primär, fremd</p></td>
<td><p>Verweis aus der <a href="lync-server-2013-usersite-table.md">Tabelle "UserSite" in lync Server 2013</a>.</p></td>
</tr>
</tbody>
</table>


</div>

<span> </span>

</div>

</div>

</div>

