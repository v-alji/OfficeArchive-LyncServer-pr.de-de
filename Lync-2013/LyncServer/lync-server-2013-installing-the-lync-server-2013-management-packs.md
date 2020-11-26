---
title: 'Lync Server 2013: Installieren der lync Server 2013-Verwaltungspakete'
description: 'Lync Server 2013: Installieren der lync Server 2013-Verwaltungspakete'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: nstalling the Lync Server 2013 management packs
ms:assetid: b800d4ab-fdc8-4c72-a76a-b78932779fe3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205202(v=OCS.15)
ms:contentKeyID: 48185233
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cbb50146474211c12dbd95801ed2b20f6bbfd8c9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426928"
---
# <a name="installing-the-lync-server-2013-management-packs"></a>Installieren der lync Server 2013-Verwaltungspakete

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-22_

System Center Operations Manager kann nur einen kleinen Teil des Windows-Betriebssystems überwachen. Sie können die Funktionen von System Center Operations Manager jedoch erweitern, indem Sie Management Packs installieren, Software, die festlegt, welche Elemente von System Center Operations Manager überwacht werden können, einschließlich der Art und Weise, wie diese Elemente überwacht werden sollen und wie Benachrichtigungen ausgelöst und gemeldet werden sollen. Microsoft lync Server 2013 umfasst zwei System Center Operations Manager-Verwaltungspakete, die die folgenden Funktionen bieten:

  - Das Komponenten-und Benutzer Verwaltungspaket (Microsoft.ls.2013.Monitoring.ComponentAndUser.MP) verfolgt lync-Server Probleme, die in Ereignisprotokollen aufgezeichnet, von Leistungsindikatoren registriert oder in den Anruf Detaildatensätzen (CDR) oder den QoE-Datenbanken (Quality of Experience) protokolliert wurden. Bei kritischen Problemen kann System Center Operations Manager so konfiguriert werden, dass Administratoren sofort per e-Mail, Sofortnachricht oder SMS-Messaging benachrichtigt werden. SMS ist die Technologie, die verwendet wird, um Textnachrichten von einem mobilen Gerät an ein anderes zu senden.
    
    <div>
    

    > [!NOTE]  
    > Weitere Informationen zum Konfigurieren der Operations Manager-Benachrichtigung finden Sie unter Konfigurieren der Benachrichtigung in der TechNet-Bibliothek unter <A class=uri href="https://go.microsoft.com/fwlink/p/?linkid=268785">https://go.microsoft.com/fwlink/p/?linkid=268785</A> .

    
    </div>

  - Das aktive Überwachungspaket (Microsoft.ls.2013.Monitoring.ActiveMonitoring.MP) testet proaktiv wichtige lync Server-Komponenten wie die Anmeldung am System, den Austausch von Sofortnachrichten oder das tätigen von Anrufen an ein Telefon, das sich im öffentlichen Telefonnetz (PSTN) befindet. Diese Tests werden mithilfe der Cmdlets für synthetische lync Server-Transaktionen durchgeführt. Zum Beispiel wird das **Test-CsIM**-Cmdlet verwendet, um eine Sofortnachrichtenunterhaltung zwischen zwei Testbenutzern zu simulieren. Wenn diese simulierte Nachrichten Unterhaltung fehlschlägt, wird eine Benachrichtigung generiert.

Zu den beiden in lync Server 2013 enthaltenen Management Packs gehören eine große Anzahl von Verbesserungen hinsichtlich der Management Packs, die mit Microsoft lync Server 2010 verwendet werden. Das lync Server 2013-Komponenten-Management Pack ist beispielsweise nicht darauf limitiert, lync Server selbst zu überwachen. Neben dem Überwachen von Ereignisprotokollen und Leistungsindikatoren für lync Server kann das Komponenten-Management Pack auch die Leistung von wichtigen Elementen wie:

  - **Internet Informationsdienste (IIS)**   Benachrichtigungen werden ausgegeben, wenn Internet-Informationsdienste offline geschaltet werden. Dies ist wichtig, da die lync Server-Webdienste von IIS abhängig sind.

  - **Prozessnutzung**   Benachrichtigungen werden ausgegeben, wenn Systemressourcen (wie verfügbarer Arbeitsspeicher) langsam ablaufen. Diese Benachrichtigungen werden selbst dann ausgestellt, wenn lync Server nicht für die Verwendung des Systems mit großem Nutzen verantwortlich ist.

  - **Computer Fehlerereignisse**   Benachrichtigungen werden im Fall eines Hardware-oder Softwareproblems ausgestellt, das die Lebensfähigkeit eines Servers gefährdet. Lync Server-Administratoren werden beispielsweise benachrichtigt, wenn ein Server den Eindruck hat, dass ein Festplattenfehler auftritt.

Die neuen Management Packs verfügen auch über eine verbesserte Berichterstellung. Zu den neuen Berichten für lync Server 2013 gehören:

  - **Bericht "End-to-End-Szenario-Verfügbarkeit**   "   Dieser Bericht enthält Informationen zur Verfügbarkeit/Uptime für wichtige lync Server-Dienste wie Registrierung oder Anwesenheit.

  - **Kapazitäts Bericht**   In diesem Bericht werden mithilfe von Leistungsindikatorinformationen Trends für Systemkomponenten wie Speicherverfügbarkeit und Prozessorauslastung veranschaulicht.

  - **Komponentenbericht**   Dieser Bericht listet die obersten Warnungs Generatoren auf, die nach lync Server-Komponente gruppiert sind.

Zusätzlich zu diesen vordefinierten Berichten melden die Management Packs für lync Server 2013 automatisch Warnungen für die Zuverlässigkeit von Anrufen (Metriken, die mit der Anruf Detail Aufzeichnung gemessen werden) und QoE-Zustände (Metriken, die nach der Qualität der Erfahrung gemessen werden). Wenn Sie die Anruf Detail Aufzeichnung aktiviert haben, können Sie die Zuverlässigkeits Benachrichtigungen für Anrufe überprüfen, indem Sie die folgenden Schritte in der System Center Operations Manager-Konsole ausführen:

  - Erweitern Sie **Überwachung**, erweitern Sie **Microsoft lync Server 2013 Health**, erweitern Sie die **Anruf Zuverlässigkeit und die Medienqualität**, und klicken Sie dann auf **Anruf Zuverlässigkeit**.

Führen Sie die folgenden Schritte über die System Center Operations Manager-Konsole aus, um die Benachrichtigung über die Qualität der Erfahrung anzuzeigen:

  - Erweitern Sie **Überwachung**, erweitern Sie **Microsoft lync Server 2013 Health**, erweitern Sie die **Anruf Zuverlässigkeit und Medienqualität**, und erweitern Sie dann **Medienqualität**.

Die Management Packs für lync Server 2013 verwenden jetzt die Ermittlung auf Computerebene anstelle des zentralen Ermittlungsmechanismus, der in Microsoft lync Server 2010 verwendet wird. Dies bedeutet, dass sich jeder System Center-Agent im wesentlichen selbst erkennt und seine Existenz dem zentralen Verwaltungs Server meldet. Die Verwendung der Ermittlung auf Computerebene vereinfacht die Verwaltung ihrer System Center-Infrastruktur und ermöglicht auch die Koexistenz unterschiedlicher Versionen der lync Server-Management Packs (beispielsweise Management Packs für lync Server 2010 und Management Packs für lync Server 2013).

</div>

<span> </span>

</div>

</div>

</div>

