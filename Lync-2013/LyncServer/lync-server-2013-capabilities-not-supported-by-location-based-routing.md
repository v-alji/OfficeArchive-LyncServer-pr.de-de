---
title: 'Lync Server 2013: Vom standortbasierten Routing nicht unterstützte Funktionen'
description: 'Lync Server 2013: Funktionen, die von Location-Based Routing nicht unterstützt werden.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capabilities not supported by Location-Based Routing
ms:assetid: c3d54953-a7d6-4465-a6c3-ae411b2d8ea9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994071(v=OCS.15)
ms:contentKeyID: 51803982
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bf9cd03a8cbdd50e136605c4f172598b2ad3f523
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435607"
---
# <a name="capabilities-not-supported-by-location-based-routing-in-lync-server-2013"></a>Vom standortbasierten Routing nicht unterstützte Funktionen in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2014-03-12_

Location-Based Routing gilt nicht für die folgenden Arten von Interaktionen. Location-Based Routing wird nicht erzwungen, wenn lync-Endpunkte mithilfe dieser Funktionen mit PSTN-Endpunkten interagieren.

  - PSTN-Einwahl bei Konferenzen

  - Eingehende und ausgehende PSTN-Anrufe über die Reaktionsgruppe

  - Parken von Anrufen oder Abrufen von PSTN-Anrufen über das Parken von Anrufen

  - Eingehende PSTN-Anrufe an den Ankündigungsdienst

  - Eingehende PSTN-Anrufe, die über die Gruppenanrufannahme abgerufen werden

Wenn Sie Location-Based Routingregeln für die Typen von Interaktionen in der folgenden Liste erzwingen möchten, müssen Sie Location-Based Routing für Konferenzen aktivieren:

  - PSTN-Einwahl von Konferenzen

  - Eskalationen von Peer-zu-Peer-Audiounterhaltungen in Konferenzen unter Beteiligung von PSTN-Endpunkten

  - Anrufdurchstellung nach Rücksprache unter Beteiligung von PSTN-Endpunkten

Informationen zum Aktivieren von Location-Based Routing für Konferenzen finden Sie unter [standortbasiertes Routing für Konferenzen in lync Server 2013](lync-server-2013-location-based-routing-for-conferencing.md).

<div>

## <a name="see-also"></a>Siehe auch


[Planung des standortbasierten Routings in Lync Server 2013](lync-server-2013-planning-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

