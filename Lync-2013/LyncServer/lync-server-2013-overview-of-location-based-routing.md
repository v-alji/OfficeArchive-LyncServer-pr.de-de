---
title: 'Lync Server 2013: Übersicht über Location-Based Routing'
description: 'Lync Server 2013: Übersicht über Location-Based-Routing.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Location-Based Routing
ms:assetid: 4aa494bd-0d66-4335-b9e8-f758d44a7202
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994032(v=OCS.15)
ms:contentKeyID: 51803941
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0b1e026791a8562629231b91b58d7e7eff569ffa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394979"
---
# <a name="overview-of-location-based-routing-in-lync-server-2013"></a>Übersicht über Location-Based-Routing in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-02-21_

Das standortbasierte Routing stellt einen neuen Regelsatz zur Verfügung, mit dem das Routing nationaler und internationaler PSTN-Anrufe modifiziert werden kann, um eine Gebührenumgehung zu verhindern. Beim standortbasierten Routing lassen sich die Regeln flexibel auf bestimmte Regionen und Gateways und sogar auf bestimmte Benutzergruppen beschränken.

Die folgenden Szenarien veranschaulichen die wichtigsten Arten von Einschränkungen, die Location-Based Routing erzwingen kann:

  - Ausstiegs Anrufe – Location-Based Routing kann ausgehende Aufrufe von einem PSTN-Gateway erzwingen, das sich in der gleichen Region befindet wie der Aufrufer, um die PSTN-Maut Umgehung zu verhindern, wodurch Anrufe von einem PSTN-Gateway in einer anderen Region als der Aufrufer verhindert werden.

  - Ingress-Anrufe – Location-Based Routing kann verhindern, dass eingehende PSTN-Anrufe lync-Endpunkte anrufen, wenn sich das PSTN-Gateway, in dem sich der eingehende Anruf befindet, nicht in derselben Region wie der angerufene lync-Benutzer befindet.

  - Unbekannte Regionen – Location-Based Routing schränkt eingehende und ausgehende PSTN-Anrufe von und zu Benutzern ein, die sich an unbestimmten Speicherorten befinden (also Remotebenutzer, die eine Verbindung mit dem Internet herstellen oder sich in unbekannten Regionen befinden).

  - Internationale Regionen – Location-Based Routing erzwingt die Weiterleitung von ausgehenden Anrufen über internationale PSTN-Gateways, wenn ein Gateway lokal zum Standort des Benutzers nicht gefunden werden kann.

<div>

## <a name="see-also"></a>Siehe auch


[Planung des standortbasierten Routings in Lync Server 2013](lync-server-2013-planning-for-location-based-routing.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

