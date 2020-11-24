---
title: 'Lync Server 2013: Standort eines PSTN-Gateways'
description: 'Lync Server 2013: Standort des PSTN-Gateways.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN gateway's location
ms:assetid: 49693a35-fad3-49ee-a71e-c7e4537b79aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994031(v=OCS.15)
ms:contentKeyID: 51803940
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4f793249908bd1f064f9038ddd90c7f5b01a61d5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394590"
---
# <a name="pstn-gateways-location-in-lync-server-2013"></a>Standort eines PSTN-Gateways in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-03-09_

Für Anrufe, die über PSTN-Gateways und PBX-Anlagen weitergeleitet werden, sind möglicherweise abhängig vom Standort solcher Systeme Location-Based Routing Einschränkungen erforderlich. Location-Based-Routing kann pro trunk basierend auf Granularität aktiviert werden.

Location-Based Routing führt die folgenden Regeln ein, wenn Sie in einem Trunk aktiviert sind:

  - Wenn Location-Based Routing pro trunk aktiviert ist, werden die Regeln, die für diesen Trunk definiert sind, nur auf die durch diesen Trunk weitergeleiteten Anrufe angewendet.

  - Um zu verhindern, dass PSTN-Mautgebühren für Anrufe von einer Netzwerk Website, die sich von der Netzwerk Website, auf der sich das PSTN-Gateway befindet, abweichen, wird Location-Based Routing die Zuordnung einer Netzwerk Website zu einem bestimmten trunk eingeführt. Dadurch wird die Netzwerk Website definiert, die das Weiterleiten von Anrufen an einen bestimmten trunk ermöglicht.

Trunks können für Location-Based Routing auf zwei Arten aktiviert werden:

  - Der Trunk ist für ein PSTN-Gateway definiert, das Anrufe an das Telefonfestnetz weiterleitet. Eingehende Anrufe, die von einem Trunk dieses Typs weitergeleitet werden, werden nur an Endgeräte weitergeleitet, die sich am selben Netzwerkstandort befinden wie der Trunk.

  - Der trunk ist für einen Vermittlungs Server-Peer definiert, der keine Anrufe an das PSTN abgibt und Dienste für Benutzer mit älteren Telefonen an statischen Speicherorten (also Telefonanlagen) abruft. Für diese spezielle Konfiguration wird für alle eingehenden Anrufe, die von einem Trunk dieses Typs weitergeleitet werden, angenommen, dass sie vom selben Netzwerkstandort kommen wie der Trunk. Anrufe von PBX-Benutzern haben dieselbe Location-Based Routing Erzwingung wie lync-Benutzer, die sich am gleichen Netzwerkstandort wie der Stamm befinden. Wenn zwei PBX-Systeme, die sich auf separaten Netzwerkstandorten befinden, über lync Server verbunden sind, ermöglicht Location-Based Routing die Weiterleitung von einem PBX-Endpunkt in einer Netzwerk Website an einen anderen PBX-Endpunkt auf der anderen Netzwerk Website. Dieses Szenario wird durch Location-Based Routing nicht blockiert. Zusätzlich zu diesem Szenario und auf ähnliche Weise wie ein lync-Benutzer am gleichen Speicherort können Endpunkte, die mit einem Vermittlungsserver-Peer mit dieser Konfiguration verbunden sind, Anrufe an und von einem anderen Vermittlungsserver-Peer durchführen oder empfangen, die keine Anrufe an das PSTN (also einen mit einer anderen Telefonanlage verbundenen Endpunkt) weiterleiten, und zwar unabhängig von der Netzwerk Website, der Alle eingehenden Anrufe, ausgehenden Anrufe, Anruf Übertragungen und Anrufweiterleitung mit PSTN-Endpunkten unterliegen dem standortbasierten Routing, um nur PSTN-Gateways zu verwenden, die als lokal für diesen Vermittlungs Server-Peer definiert sind.

<div>

## <a name="see-also"></a>Siehe auch


[Anleitungen für das standortbasierte Routing in Lync Server 2013](lync-server-2013-guidance-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

