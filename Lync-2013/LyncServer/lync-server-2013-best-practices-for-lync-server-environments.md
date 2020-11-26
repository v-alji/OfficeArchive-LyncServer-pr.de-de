---
title: 'Lync Server 2013: bewährte Methoden für lync Server-Umgebungen'
description: 'Lync Server 2013: bewährte Methoden für lync Server-Umgebungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for Lync Server environments
ms:assetid: b0e45d84-09c8-4d3e-aad0-bc6f34ce233b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720348(v=OCS.15)
ms:contentKeyID: 63969642
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ae6c02621bd6506d2a1d379aeaf92b20ce3f7ae1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436062"
---
# <a name="best-practices-for-lync-server-2013-environments"></a>Bewährte Methoden für lync Server 2013-Umgebungen

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2014-08-04_

Die folgenden allgemeinen Grundsätze sollten auf den laufenden Betrieb Ihres Systems angewendet werden:

  - **Verstehen und Verwenden von MOF**   MOF ist eine Sammlung von bewährten Methoden, Prinzipien und Modellen, die Unternehmen technische Anleitungen zur Verwaltung von IT-Ressourcen bereitstellen, beispielsweise tägliche lync Server 2013-Vorgänge. Die folgenden MOF-Richtlinien können Ihnen dabei helfen, unternehmenskritische Produktionssystem Zuverlässigkeit, Verfügbarkeit, Unterstützung und Verwaltbarkeit für Microsoft-Produkte zu erreichen. Weitere Informationen finden Sie unter [Microsoft Operations Framework 4,0](https://go.microsoft.com/fwlink/p/?linkid=40939).

  - Informationen **zu bewährten Methoden für lync Server 2013**   Wir empfehlen, praktische und bewährte Verfahren zum Verwalten von lync Server 2013 zu implementieren. Durch die Verwendung von erprobten, getesteten und dokumentierten Methoden zur Verwaltung von Vorgängen ist es möglicherweise effizienter als die Entwicklung eigener Methoden.

  - **Getrennte Vorgänge in tägliche, wöchentliche und monatliche Prozesse**   Dokumentieren Sie die erforderlichen operativen Aufgaben, die Sie regelmäßig ausführen werden. Wenn Sie dokumentieren, wie Sie Aufgaben durchführen, können Sie sicherstellen, dass Ihre Informationen beibehalten werden, wenn sich Ihre Betriebsumgebung ändert, beispielsweise wenn neue Technologien bereitgestellt werden oder Mitarbeiter Änderungen auftreten. Wir empfehlen, dass operative Aufgaben in verwaltbare Arbeitslasten aufgeteilt werden, bei denen Aufgaben täglich, wöchentlich und monatlich durchgeführt werden. Tägliche Aufgaben konzentrieren sich auf die Funktionsweise eines Systems, während sich die monatlichen Aufgaben mehr auf die Gewährleistung der langfristigen Gesundheit eines Systems konzentrieren.
    
    Dieses Dokument kann in Umgebungen verwendet werden, in denen nur Instant Messaging/Anwesenheits Komponenten (im/p) bereitgestellt werden, oder im/p mit Enterprise-VoIP. Wenn Aufgaben oder Checklisten Elemente für Enterprise-VoIP spezifisch sind, wird dies erwähnt, und wenn Ihre Umgebung keine Enterprise-VoIP umfasst, kann der Teil übersprungen werden.

  - **Bereitstellen der für den Betrieb von lync Server 2013 erforderlichen Tools**   Es stehen viele Tools zur Verfügung, mit denen Sie Probleme behandeln, Aufgaben automatisieren und die lync Server 2013-Umgebung überwachen und verwalten können. Definieren Sie einen Standardsatz von Tools für Ihre Organisation, damit die Aufgaben, die vom Operations Team ausgeführt werden, genau, effizient, konsistent und auf kontrollierte Weise ausgeführt werden. Darüber hinaus sollten Sie Prozesse implementieren, um Vorfälle und wichtige Konfigurationsänderungen nachverfolgen zu können.

<div>

## <a name="reference"></a>Referenz

Zugunsten der Leser, die nicht bereits mit den Grundlagen der Serververwaltung im allgemeinen vertraut sind, bieten wir eine Übersicht über Server Verwaltungsmethoden. Leser, die bereits mit der Serververwaltung vertraut sind, können diesen Abschnitt überspringen.

Bewährte Methoden sind Empfehlungen, die auf dem Wissen und der Erfahrung basieren, die IT-Experten in vielen Umgebungen erworben haben. Sie bieten Standardverfahren für typische Aufgaben, die von ihren lync Server-Administratoren täglich ausgeführt werden müssen, und listet die Tools auf, die Sie zum Verwalten einer lync Server-Umgebung verwenden sollten.

Zu den typischen Aufgaben für lync-Administratoren gehören die folgenden:

  - **Kapazitäts-und Verfügbarkeitsverwaltung**   Definieren Sie, wie und was gemessen werden soll, um zukünftige Kapazitätsanforderungen vorherzusagen und über die Kapazität, Zuverlässigkeit und Verfügbarkeit Ihrer Systeme zu berichten. Sie müssen sicherstellen, dass die Server, auf denen lync Server ausgeführt wird, für die Verarbeitung der Auslastung des Systems ausgelegt sind und dass ungeplante Ausfallzeiten unter den in der Vereinbarung zum Service Level (SLA) definierten Ebenen aufbewahrt werden. Darüber hinaus müssen Sie Hardware aktualisieren, um die definierten Anforderungen weiterhin erfüllen zu können.

  - **Change Management und Konfigurationsverwaltung**   Steuern Sie, wie Änderungen an IT-Systemen vorgenommen werden. Dies sollte Tests, Anwendungs Feedback und Notfallpläne, die Dokumentation aller Änderungen und die Genehmigung der Verwaltung umfassen, wenn Probleme auftreten. Speichern Sie Ihre Software-und Hardwareressourcen sowie deren Konfigurationen.

  - **System Verwaltung**   Gliedern Sie die Standardmethoden für administrative Aufgaben wie Datenbankverwaltung und Websiteverwaltung.

  - **Sicherheitsverwaltung**   Sie verfügen über eine detaillierte Richtlinie und einen Plan, mit dem Datenvertraulichkeit, Datenintegrität und Datenverfügbarkeit der IT-Infrastruktur geschützt werden. Dazu gehören alltägliche Aktivitäten und Aufgaben im Zusammenhang mit der Verwaltung und Anpassung der IT-Sicherheitsinfrastruktur.

  - **System Problembehandlung**   Gliedern von Methoden zum Umgang mit unerwarteten Problemen, einschließlich der Schritte zum verhindern ähnlicher Probleme in der Zukunft.

  - **Service Level Agreements**   Verwalten Sie eine Reihe von Zielen für die Leistung der IT-Systeme, und Messen Sie die Leistung regelmäßig mit diesen Zielen.

  - **Dokumentation**   Dokumentieren Sie Standardverfahren wie Konfigurationsinformationen und gelernte Lektionen, und stellen Sie Sie den Mitarbeitern zur Verfügung, die Sie benötigen. Wenn Änderungen an der Konfiguration vorgenommen wurden, aktualisieren Sie die Dokumentation entsprechend.

</div>

<div>

## <a name="related-sections"></a>Verwandte Abschnitte

Lesen Sie die folgenden Themen zu Systemvorgängen, bevor Sie fortfahren:

  - [Kapazitäts-und Verfügbarkeitsverwaltung in lync Server 2013](lync-server-2013-capacity-and-availability-management.md)

  - [Änderungsverwaltung in lync Server 2013](lync-server-2013-change-management.md)

  - [Konfigurationsverwaltung in lync Server 2013](lync-server-2013-configuration-management.md)

  - [System Verwaltung in lync Server 2013](lync-server-2013-system-administration.md)

  - [Service Level Agreements in lync Server 2013](lync-server-2013-service-level-agreements.md)

  - [Dokumentation in lync Server 2013](lync-server-2013-documentation.md)

  - [Standard Verfahren in lync Server 2013](lync-server-2013-standard-procedures.md)

  - [Notfallverfahren in lync Server 2013](lync-server-2013-emergency-procedures.md)

</div>

<div>

## <a name="see-also"></a>Siehe auch


[Microsoft Operations Framework 4,0](https://go.microsoft.com/fwlink/p/?linkid=40939)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

