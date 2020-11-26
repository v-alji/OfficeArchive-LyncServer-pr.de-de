---
title: 'Lync Server 2013: Konfigurieren eines Watcher-Knotens zum Ausführen synthetischer Transaktionen'
description: 'Lync Server 2013: Konfigurieren eines Watcher-Knotens zum Ausführen synthetischer Transaktionen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring a watcher node to run synthetic transactions
ms:assetid: cedda508-8881-4079-88d5-49798f342ddf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205314(v=OCS.15)
ms:contentKeyID: 48185578
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bd5fdb3d1a1499a6ef79e962a41d9eb3ee174c33
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433468"
---
# <a name="configuring-a-watcher-node-to-run-synthetic-transactions-in-lync-server-2013"></a>Konfigurieren eines Watcher-Knotens zum Ausführen synthetischer Transaktionen in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2014-02-07_

Nachdem Sie die System Center-Agent-Dateien installiert haben, müssen Sie den Watcher-Knoten als Nächstes konfigurieren. Die Schritte zum Konfigurieren eines Watcher-Knotens variieren je nachdem, ob sich der Watcher-Knoten Computer in Ihrem Umkreisnetzwerk oder außerhalb Ihres Umkreisnetzwerks befindet.

Beim Konfigurieren eines Monitorknotens müssen Sie außerdem die Authentifizierungsmethode auswählen, die von diesem Knoten verwendet werden soll. Mit lync Server 2013 können Sie eine von zwei Authentifizierungsmethoden auswählen: vertrauenswürdige Server-oder Anmelde Informations Authentifizierung. Die Unterschiede zwischen diesen beiden Methoden sind in der folgenden Tabelle beschrieben:


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>Konfiguration</th>
<th>Beschreibung</th>
<th>Unterstützte Speicherorte</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Vertrauenswürdiger Server</p></td>
<td><p>Ein Zertifikat wird verwendet, um die Identität eines internen Servers anzunehmen und die Authentifizierungsaufforderungen zu umgehen.</p>
<p>Dies ist hilfreich für Administratoren, die ein einzelnes Zertifikat anstelle von vielen Benutzerkennwörtern für jeden Watcher-Knoten verwalten möchten.</p></td>
<td><p>Innerhalb des Unternehmens.</p>
<p>Beachten Sie, dass sich der Watcher-Knoten bei dieser Methode in der gleichen Domäne wie die zu überwachenden Pools befinden muss. Wenn sich der Watcher-Knoten und die überwachten Pools in verschiedenen Domänen befinden, verwenden Sie stattdessen die Anmelde Informations Authentifizierung.</p></td>
</tr>
<tr class="even">
<td><p>Authentifizierung von Anmeldeinformationen</p></td>
<td><p>Benutzernamen und Kennwörter werden auf sichere Weise in der Windows-Anmeldeinformationsverwaltung auf jedem Monitorknoten gespeichert.</p>
<p>Dieser Modus erfordert mehr Kennwortverwaltung, ist aber die einzige Option für Watcher-Knoten, die sich außerhalb des Unternehmens befinden. Diese Monitorknoten können nicht als vertrauenswürdiger Endpunkt für die Authentifizierung betrachtet werden.</p></td>
<td><p>Außerhalb des Unternehmens.</p>
<p>Innerhalb des Unternehmens.</p></td>
</tr>
</tbody>
</table>


Sie sollten auch sicherstellen, dass Ihre Firewall eingehende Regeln für MonitoringHost.exe und PowerShell.exe enthält. Wenn diese Prozesse von der Firewall blockiert werden, schlagen Ihre synthetischen Transaktionen mit einem 504-Fehler (Servertimeout) fehl.

</div>

<span> </span>

</div>

</div>

</div>

