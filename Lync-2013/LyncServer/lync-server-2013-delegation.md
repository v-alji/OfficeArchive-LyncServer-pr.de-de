---
title: 'Lync Server 2013: Stellvertretung'
description: 'Lync Server 2013: Delegierung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delegation
ms:assetid: 89e76e5c-3cfb-4504-8d0d-7509c8ba9815
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994045(v=OCS.15)
ms:contentKeyID: 51803956
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6dc25d0ea3dfd64ee1b71677e6bac55c1cb1ca32
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430742"
---
# <a name="delegation-in-lync-server-2013"></a>Stellvertretung in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-03-09_

Die Delegierungsfunktionen in lync sind von Location-Based Routing auf die folgende Weise betroffen:

  - Wenn eine für Location-Based Routing aktivierte Stellvertretung einen Anruf im Auftrag eines Managers anbietet, wird die VoIP-Richtlinie des Stellvertreters verwendet, um den Anruf zu genehmigen, und die VoIP-Routing Richtlinie des Stellvertreters wird zum Weiterleiten des Anrufs verwendet.

  - Für eingehende Anrufe aus dem öffentlichen Telefonnetz für einen Vorgesetzten gelten die gleichen Regeln wie für Anrufweiterleitung oder paralleles Anrufen, wie in den Themen zur Anrufweiterleitung und -durchstellung bzw. zum parallelen Anrufen beschrieben.

  - Wenn eine Stellvertretung einen Endpunkt im öffentlichen Telefonnetz als Ziel für paralleles Anrufen festlegt, wird bei einem für den Vorgesetzten eingehenden Anruf die VoIP-Routingrichtlinie des Standorts, der dem eingehenden Trunk zugeordnet ist, für das Routen des Anrufs an den Endpunkt der Stellvertretung im öffentlichen Telefonnetz verwendet.

  - Für Stellvertretungen empfiehlt es sich, dass der Vorgesetzte und die ihm zugeordneten Stellvertretungen sich normalerweise am gleichen Netzwerkstandort befinden.

<div>

## <a name="see-also"></a>Siehe auch


[Szenarien für das standortbasierte Routing in Lync Server 2013](lync-server-2013-scenarios-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

