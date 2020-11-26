---
title: 'Lync Server 2013: Bereitstellen von Zweigstellen'
description: 'Lync Server 2013: Bereitstellen von Zweigstellen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying branch sites
ms:assetid: 1475dee0-66ae-4ee5-b6f1-7409b4bbff45
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398217(v=OCS.15)
ms:contentKeyID: 48183483
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d653e3f06de832693d97bfb229f122a67c28640e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430091"
---
# <a name="deploying-branch-sites-in-lync-server-2013"></a>Bereitstellen von Zweigstellen in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-21_

Zweigstellenbenutzer erhalten die meisten ihrer lync Server 2013-Funktionen von dem Server am zentralen Standort, dem die Zweigstelle zugeordnet ist. Jede Verzweigungs Website ist genau einem zentralen Standort zugeordnet. Zum Bereitstellen von Anrufen in das und aus dem PSTN (Public Switched Telephone Network) kann eine Verzweigungs Website eine der folgenden Aktionen enthalten:

  - Ein PSTN-Gateway und möglicherweise ein Meditations Server

  - Ein SIP-Trunk

  - Eine vorhandene VoIP-Infrastruktur mit einer PBX (Private Branch Exchange)

  - Eine Survivable-Branch-Appliance

  - Ein Survivable-Branch-Server

Zweigstellen mit einer überlebensfähigen Branch-Appliance oder einem Survivable Branch-Server sind in Zeiten von Wide-Area-Netzwerk-oder zentralen Standortausfällen widerstandsfähiger als Zweigstellen ohne eine dieser Lösungen. Beispielsweise können Benutzer in einer Website mit einer überlebensfähigen Branch-Appliance oder einem Überlebenden Branch-Server weiterhin PSTN-Anrufe tätigen und empfangen, wenn das Netzwerk, das die Verzweigungs Website mit dem zentralen Standort verbindet, ausgefallen ist. Eine weitere Möglichkeit zum Erreichen einer Ausfallsicherheit für Zweigstellen ist die Verwendung eines PSTN-Gateways oder eines SIP-Trunks mit einer vollständigen lync Server-Bereitstellung auf der Zweigstelle.

Details dazu, welche Verzweigungs Website Bereitstellung für Ihre Organisation richtig ist, einschließlich Voraussetzungen und andere Planungsüberlegungen, finden Sie unter [Planen der PSTN-Konnektivität in lync Server 2013](lync-server-2013-planning-for-pstn-connectivity.md) und [Planen der sprach Stabilität von Branch-Site in lync Server 2013](lync-server-2013-planning-for-branch-site-voice-resiliency.md) in der Planungsdokumentation.

<div>

## <a name="in-this-section"></a>In diesem Abschnitt

  - [Bereitstellen der PSTN-Konnektivität an einem Zweigstellenstandort in Lync Server 2013](lync-server-2013-providing-pstn-connectivity-at-a-branch-site.md)

  - [Bereitstellen einer Survivable Branch Appliance oder eines Survivable Branch Servers mit Lync Server 2013](lync-server-2013-deploying-a-survivable-branch-appliance-or-server.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

