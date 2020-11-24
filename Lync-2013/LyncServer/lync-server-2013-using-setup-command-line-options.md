---
title: 'Lync Server 2013: Verwenden von Setup-Befehlszeilenoptionen'
description: 'Lync Server 2013: Verwenden der Befehlszeilenoptionen für Setup.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Setup command-line options
ms:assetid: 99878c3c-ff31-48e2-8424-580d7b07a7bf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205129(v=OCS.15)
ms:contentKeyID: 48184957
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 15c3490ead090766462ce83cb13ffe62355032cd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393898"
---
# <a name="using-setup-command-line-options-in-lync-server-2013"></a>Verwenden von Setup-Befehlszeilenoptionen in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-03_

Die Befehlszeile von "Setup.exe" wird nur für wenige Vorgänge des Office-Setups verwendet. Anstelle der Setup-Befehlszeilenoptionen benutzen Sie in der Regel das Office-Anpassungstool und die Datei "Config.xml", um Produkte einzurichten und Funktionen anzupassen.

Die Befehlszeile der Office "Setup.exe" erkennt die in der folgenden Tabelle beschriebenen Befehlzeilenoptionen.

### <a name="office-setup-command-line-options"></a>Optionen der Office Setup-Befehlszeile

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Option der Office Setup-Befehlszeile</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>/admin</p></td>
<td><p>Führt das Office-Anpassungstool aus, um eine Setupanpassungsdatei (.msp-Datei) zu erstellen.</p></td>
</tr>
<tr class="even">
<td><p>/adminfile [Pfad]</p></td>
<td><p>Wendet die angegebene Setupanpassungsdatei auf die Installation an. Sie können einen Pfad zu einer bestimmten Anpassungsdatei (.msp-Datei) oder zu dem Ordner angeben, in dem Sie Anpassungsdateien speichern.</p></td>
</tr>
<tr class="odd">
<td><p>/config [Pfad]</p></td>
<td><p>Gibt die Config.xml Datei an, die von Setup während der Installation verwendet wird. Verwenden Sie die/config-Option, um die Config.xml Datei anzugeben, die Sie für lync 2013-Installationen angepasst haben, beispielsweise: <code>/config \\server\share\Lync15\Lync.WW\Config.xml</code></p></td>
</tr>
<tr class="even">
<td><p>/Modify lync</p></td>
<td><p>Wird mit einer geänderten config.xml-Datei verwendet, um Setup im Wartungsmodus auszuführen und Änderungen an einer vorhandenen Office-Installation durchzuführen. So können Sie beispielsweise die Option/MODIFY verwenden, um lync-Features hinzuzufügen oder zu entfernen.</p></td>
</tr>
<tr class="odd">
<td><p>/Repair lync</p></td>
<td><p>Führt das Setup auf dem Computer des Benutzers aus, um lync zu reparieren.</p></td>
</tr>
<tr class="even">
<td><p>/Uninstall lync</p></td>
<td><p>Führt das Setup aus, um lync vom Computer des Benutzers zu entfernen.</p></td>
</tr>
</tbody>
</table>


Ausführliche Informationen zur Verwendung der Befehlszeilenoptionen für Setup finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=267515> .

</div>

<span> </span>

</div>

</div>

</div>

