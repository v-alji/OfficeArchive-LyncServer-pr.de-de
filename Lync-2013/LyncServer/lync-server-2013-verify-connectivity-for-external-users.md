---
title: 'Lync Server 2013: Überprüfen der Konnektivität für externe Benutzer'
description: 'Lync Server 2013: Überprüfen der Konnektivität für externe Benutzer'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify connectivity for external users
ms:assetid: 5c02bd6e-1c96-448a-a21d-58c9961c6640
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398402(v=OCS.15)
ms:contentKeyID: 48184249
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 50ef728157d01b93e7d0b8420442ce083a42b5b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395046"
---
# <a name="verify-connectivity-for-external-users-in-lync-server-2013"></a>Überprüfen der Konnektivität für externe Benutzer in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-19_

Zum Überprüfen der Konnektivität für externe Benutzer muss die Konnektivität zwischen Benutzern und dem Server und Port für den Access Edge-Dienst sichergestellt werden.

Eine wertvolle Ressource für die Bestätigung Ihrer Konfiguration und die Möglichkeit zum Verbinden, senden und empfangen der richtigen Nachrichten für die Szenarien, für die der Zugriff durch externe Benutzer erforderlich ist, ist die Remote Connectivity Analyzer-Website ( <http://www.testocsconnectivity.com> ). Die Website wird vom Microsoft-Support verwaltet und verwaltet. Zum Erreichen des Remote Connectivity Analyzer öffnen Sie die Website in einem Browser, und folgen Sie den Anweisungen, um das Szenario auszuwählen.

<div>

## <a name="test-connectivity-of-external-users-and-external-access"></a>Testen der Konnektivität externer Benutzer und des externen Zugriffs

Tests für den Zugriff durch externe Benutzer sollten alle externen Benutzertypen enthalten, die von Ihrer Organisation unterstützt werden, einschließlich der folgenden:

  - Benutzer aus mindestens einer Föderationsdomäne und Test-Chat, Anwesenheit, A/V und Desktopfreigabe.

  - Benutzer jedes öffentlichen Chat Dienstanbieters, den Ihre Organisation unterstützt (und für die die Bereitstellung abgeschlossen wurde).

  - Anonyme Benutzer.

  - Benutzer in Ihrer Organisation, die bei lync Remote angemeldet sind, aber keine VPN-Verbindung verwenden.

Diese Tests bestimmen, ob der Edgeserver wie folgt lautet:

  - Überwachen der erforderlichen Ports durch Verwendung eines telnet-Clients außerhalb Ihres Netzwerks.
    
      - Beispiel: Telnet SIP.contoso.com 443
    
      - Führen Sie den vorhergehenden Test für Ports aus, die Sie je nach Bereitstellung auf dem Edgeserver oder Edgeserver-Pool verwenden.

  - Ausführen einer präzisen externen DNS-Auflösung.
    
      - Pingen Sie von außerhalb Ihres Netzwerks jeden der externen FQDN des Edge-oder Edge-Pools. Auch wenn der ping fehlschlägt, werden die IP-Adressen angezeigt, die Sie mit den zugewiesenen vergleichen können.

</div>

</div>

<span> </span>

</div>

</div>

</div>

