---
title: Migration von Lync Server 2010-Gruppenchat oder Office Communications Server 2007 R2-Gruppenchat zu Lync Server 2013 Persistent Chat Server
description: Migration von lync Server 2010, Gruppen-Chat oder Office Communications Server 2007 R2-Gruppen-Chat zu lync Server 2013, beständiger Chat Server.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server
ms:assetid: 5b4d3db1-6eba-4932-b49c-f60bcf9488f9
ms:mtpsurl: https://technet.microsoft.com/library/Gg615442(v=OCS.15)
ms:contentKeyID: 48184240
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6090d5924a203a960444d9a10700fd178d038887
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446857"
---
# <a name="migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server"></a>Migration von Lync Server 2010-Gruppenchat oder Office Communications Server 2007 R2-Gruppenchat zu Lync Server 2013 Persistent Chat Server

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-06_

Die Themen in diesem Abschnitt führen Sie durch den Vorgang zum Migrieren von lync Server 2010, Gruppen-Chat oder Office Communications Server 2007 R2-Gruppenchat zu lync Server 2013, beständiger Chat Server. Wenn Sie beabsichtigen, dass die Bereitstellung 2013 des beständigen Chat Servers mit einer lync Server 2010-, Gruppen-Chat-oder Office Communications Server 2007 R2-Gruppen-Chat-Bereitstellung koexistieren soll, enthält dieser Leitfaden auch einige wichtige Informationen zum Betrieb in dieser gemischten Umgebung. Dieser Leitfaden befasst sich in erster Linie mit der Datenmigration für beständigen Chat Server. Informationen zu Benutzern, die von älteren Versionen von lync Server zu lync Server 2013 migrieren, finden Sie unter [Migration von lync Server 2010 zu lync Server 2013](migration-from-lync-server-2010-to-lync-server-2013.md) und [Migration von Office Communications Server 2007 R2 zu lync Server 2013](migration-from-office-communications-server-2007-r2-to-lync-server-2013.md).

<div>


> [!IMPORTANT]  
> In diesem Thema wird davon ausgegangen, dass Sie lync Server 2013 bereits in Koexistenz mit lync Server 2010 oder Office Communications Server 2007 R2 installiert haben.



</div>

<div>


> [!IMPORTANT]  
> In diesem Leitfaden werden die Schritte beschrieben, die in der Regel für die einzelnen Migrationsphasen erforderlich sind. Sie bezieht sich nicht auf jede mögliche Legacy Bereitstellungstopologie oder alle möglichen Migrationsszenarien. Daher müssen Sie möglicherweise nicht alle beschriebenen Schritte ausführen, oder Sie müssen abhängig von Ihrer Bereitstellung möglicherweise zusätzliche Schritte ausführen. Der Leitfaden enthält auch Beispiele für Überprüfungsschritte. Diese Überprüfungsschritte werden bereitgestellt, um Ihnen zu verdeutlichen, was Sie suchen müssen, um sicherzustellen, dass jede Phase erfolgreich abgeschlossen wird, während Sie Ihre Migration fortführen. Sie können diese Überprüfungsschritte für Ihren spezifischen Migrationsprozess ändern.



</div>

Dieses Handbuch enthält Informationen, die speziell für das Upgrade Ihrer vorhandenen Bereitstellung gelten. Es wird nicht erläutert, wie Sie Ihre vorhandene Topologie ändern. In diesem Leitfaden wird die Implementierung neuer Features nicht behandelt. Wenn eine detaillierte Prozedur an anderer Stelle dokumentiert wird, werden Sie in diesem Leitfaden zu dem entsprechenden Dokument-oder Dokumentabschnitt weitergeleitet.

In diesem Dokument werden die in der folgenden Liste angegebenen Ausdrücke definiert.

  - *Migrations*  
    Verschieben der Bereitstellung aus einer früheren Version des beständigen Chat Servers (vormals als Gruppen-Chat Server bezeichnet) zu lync Server 2013, beständiger Chat Server

<!-- end list -->

  - *Upgrade*  
    Installieren einer neueren Software Version auf einem Server oder Clientcomputer

<!-- end list -->

  - *Koexistenz*  
    Die temporäre Umgebung, die während der Migration vorhanden ist, wenn einige Funktionen zu lync Server 2013, beständiger Chat Server migriert wurden und andere Funktionen weiterhin auf einer früheren Version des Gruppen Chat Servers verbleiben.

Der beständige Chat Server ist eine Erweiterung der lync Server 2013-Infrastruktur. Je nach Topologie können Sie lync Server 2010, Gruppen-Chat oder Office Communications Server 2007 R2-Gruppen-Chat zu lync Server 2013-beständigen Chat Server migrieren. Details zu verfügbaren Topologien und den technischen und Softwareanforderungen für die Migration des Gruppen-Chat Servers finden Sie unter [Planen des beständigen Chat Servers in lync Server 2013](lync-server-2013-planning-for-persistent-chat-server.md) in der Planungsdokumentation.

Wenn Ihre Organisation Compliance-Unterstützung erfordert, wird Sie jetzt automatisch mit jedem beständigen Chat Server installiert. Für die Compliance wird kein separater Server mehr benötigt.

<div>


> [!IMPORTANT]  
> Der Server für beständigen Chat muss auf einem NTFS-Dateisystem installiert sein, um die Dateisystemsicherheit zu erzwingen. FAT32 ist kein unterstütztes Dateisystem für beständigen Chat Server.<BR>Wenn Ihre Organisation Compliance-Unterstützung erfordert, wird Sie jetzt automatisch mit jedem beständigen Chat Server installiert. Für die Compliance wird kein separater Server mehr benötigt. Weitere Informationen zu Änderungen in lync Server 2013 &nbsp; -Server für beständigen Chat finden Sie unter <A href="lync-server-2013-new-persistent-chat-server-features.md">neue beständige Chat Server Features in lync Server 2013</A> in der Dokumentation "erste Schritte".



</div>

<div>

## <a name="in-this-section"></a>In diesem Abschnitt

  - [Standardmigrationsszenario – Übersicht](standard-migration-scenario-high-level.md)

  - [Migrationsprozess – Details](migration-process-details.md)

  - [Überlegungen zur Koexistenz](coexistence-considerations.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

