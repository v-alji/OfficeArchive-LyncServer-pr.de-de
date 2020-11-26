---
title: 'Lync Server 2013: Verwenden von Config.xml zum Ausführen von Installationsaufgaben'
description: 'Lync Server 2013: Verwenden von Config.xml, um Installationsaufgaben auszuführen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using Config.xml to perform installation tasks
ms:assetid: 0813184a-ab40-417c-b3a3-c2090766b831
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204651(v=OCS.15)
ms:contentKeyID: 48183332
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22fff14e21a120c3a0ee2cd6432fd1eba2bbee5f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438953"
---
# <a name="using-configxml-to-perform-installation-tasks-in-lync-server-2013"></a>Verwenden von Config.xml zum Ausführen von Installationsaufgaben in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-02_

Das Office-Anpassungstool (OAT) ist zwar das primäre Tool für die angepasste Installation, Administratoren können jedoch mit der Datei "Config.xml" zusätzliche, im OAT nicht verfügbare Installationsanweisungen angeben. Die folgenden Anpassungen können nur mithilfe der Datei Config.xml vorgenommen werden:

  - Angeben des Netzwerkinstallationspfads

  - Auswählen der zu installierenden Produkte

  - Konfigurieren der Protokollierung und des Speicherorts der Setupanpassungsdatei und Softwareupdates

  - Angeben von Installationsoptionen, z. B. Benutzername

  - Kopieren der lokalen Installationsquelle (Local Installation Source, LIS) auf den Benutzercomputer ohne Installation von Office

  - Hinzufügen oder Entfernen von Sprachen in der Installation

Wir empfehlen, dass Sie die Config.xml-Datei verwenden, um die unbeaufsichtigte lync 2013-Installation zu konfigurieren.

Standardmäßig wird die Config.xml-Datei, die im Kernproduktordner gespeichert ist (beispielsweise \\ Product. WW) weist Setup an, dieses Produkt zu installieren. Beispielsweise wird in der Config.xml-Datei im folgenden Ordner lync 2013 installiert:

  - \\\\Server \\ Freigabe \\ Lync15 \\ lync. WW \\Config.xml

Die Config.xml Elemente, die am häufigsten für die lync 2013-Installation verwendet werden, sind in der folgenden Tabelle aufgelistet.

### <a name="configxml-elements"></a>Config.xml-Elemente

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Element</th>
<th>Beschreibung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Konfiguration</p></td>
<td><p>Element der obersten Ebene (erforderlich). Enthält das Product-Attribut, beispielsweise: product = lync</p></td>
</tr>
<tr class="even">
<td><p>OptionState</p></td>
<td><p>Gibt an, wie bestimmte Produktfeatures während der Installation behandelt werden. Verwenden Sie die folgenden Attribute, um die Installation von Business Connectivity Services zu verhindern, die freigegebene Komponenten umfasst, die Outlook 2010 stören:</p>
<ul>
<li><p>ID = &quot; LOBiMain&quot;</p></li>
<li><p>Zustand = &quot; abwesend&quot;</p></li>
<li><p>Kinder = &quot; Kraft&quot;</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>Anzeige</p></td>
<td><p>Die Ebene der Benutzeroberfläche, die dem Benutzer angezeigt wird. Zu den typischen Attributen zählen Folgende:</p>
<ul>
<li><p>CompletionNotice = &quot; Ja &quot;  |  &quot; Nein &quot; (Standard)</p></li>
<li><p>AcceptEULA = &quot; Ja &quot;  |  &quot; Nein &quot; (Standard)</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>Protokollierung</p></td>
<td><p>Optionen für den vom Setup ausgeführten Protokollierungstyp. Zu den typischen Attributen zählen Folgende:</p>
<ul>
<li><p>Type = &quot; Off &quot;  |  &quot; Standard &quot; (Standard) | &quot; Ausführliche&quot;</p></li>
<li><p>Template=”filename.txt” (Name der Protokolldatei)</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>Einstellung</p></td>
<td><p>Gibt Werte für Windows Installer-Eigenschaften an. Zu den typischen Attributen zählen Folgende:</p>
<ul>
<li><p>Festlegen von ID = &quot; Name &quot; (der Name der Windows Installer-Eigenschaft)</p></li>
<li><p>Value = &quot; Wert &quot; (der Wert, der der Eigenschaft zugewiesen werden soll)</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>DistributionPoint</p></td>
<td><p>Der vollqualifizierte Pfad des Netzwerkinstallationspfads, von dem die Installation ausgeführt werden soll. Enthält das Standortattribut:</p>
<ul>
<li><p>Location=”path”</p></li>
</ul></td>
</tr>
</tbody>
</table>


Das folgende Beispiel zeigt eine Config.xml-Datei für eine typische unbeaufsichtigte Installation von lync 2013.

    <Configuration Product="Lync">
      <OptionState Id="LOBiMain" State="Absent" Children="Force" />
      <Display Level="None" CompletionNotice="No" AcceptEula="Yes" />
      <Logging Type="verbose" Path="%temp%" Template="LyncSetupVerbose(*).log" />
      <Setting Id="SETUP_REBOOT" Value="Never" />
      <DistributionPoint Location="\\server\share\Lync15" />
    </Configuration>

Detaillierte Informationen zur Verwendung der Config.xml-Datei zum Ausführen von Office-Installations-und-Wartungsaufgaben finden Sie unter <https://go.microsoft.com/fwlink/p/?linkid=267514> .

<div>

## <a name="to-customize-the-configxml-file"></a>So passen Sie die Datei "Config.xml" an

1.  Öffnen Sie die Datei "Config.xml" in einem Text-Editor wie Editor.

2.  Suchen Sie die Zeilen, die die zu ändernden Elemente enthalten.

3.  Ändern Sie den Elementeintrag mit den gewünschten Optionen für eine automatische Installation. Stellen Sie sicher, dass Sie die Kommentartrennzeichen "" entfernen \<\!--" and "--\> . Verwenden Sie z. B. die folgende Syntax:
    
        < DistributionPoint Location="\\server\share\Lync15" />

4.  Speichern Sie die Datei Config.xml.

</div>

</div>

<span> </span>

</div>

</div>

</div>

