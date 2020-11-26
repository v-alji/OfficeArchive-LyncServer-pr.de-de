---
title: 'Lync Server 2013: Technische Anforderungen für die Medienumgehung'
description: 'Lync Server 2013: Technische Voraussetzungen für die medienumgehung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Technical requirements for media bypass
ms:assetid: 6162a204-0e7c-460a-8eb2-e592c6590a8a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398435(v=OCS.15)
ms:contentKeyID: 48184321
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: dee594139031966342fcec2bc1296a603055b4cc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423435"
---
# <a name="technical-requirements-for-media-bypass-in-lync-server-2013"></a>Technische Anforderungen für die Medienumgehung in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-21_

Für jeden Anruf an das PSTN ermittelt der Vermittlungsserver, ob Medien vom lync-Endpunkt des Ursprungs direkt an einen Vermittlungsserver-Peer gesendet werden können, ohne den Vermittlungsserver zu durchlaufen. Der Peer kann ein PSTN-Gateway, eine IP-Nebenstellenanlage oder ein SBC (Session Border Controller) bei einem Anbieter von Internettelefoniediensten sein, der zu der Leitung zwischen dem Vermittlungsserver gehört, bei dem der Anruf weitergeleitet wird.

Die Medienumgehung kann implementiert werden, wenn die folgenden Voraussetzungen erfüllt sind:

  - Ein Vermittlungs Server-Peer muss die erforderlichen Funktionen für die medienumgehung unterstützen, wobei das wichtigste die Möglichkeit ist, mehrere gegabelte Antworten (so genannte "frühe Dialogfelder") zu verarbeiten. Wenden Sie sich an den Hersteller Ihres Gateways oder Ihrer Telefonanlage oder Ihres ITSP, um den Wert für die maximale Anzahl der frühen Dialogfelder abzurufen, die das Gateway, die Telefonanlage oder SBC akzeptieren können.

  - Der Vermittlungs Server-Peer muss Mediendatenverkehr direkt von lync-Endpunkten akzeptieren. Mit vielen ITSPs können Ihre SBC nur Datenverkehr vom Vermittlungs Server empfangen. Wenden Sie sich an Ihren ITSP, um festzustellen, ob der SBC Mediendatenverkehr direkt von lync-Endpunkten akzeptiert.

  - Lync-Clients und ein Vermittlungs Server-Peer müssen gut verbunden sein, d. h., Sie befinden sich entweder im gleichen Netzwerkbereich oder auf Netzwerkstandorten, die eine Verbindung mit der Region über WAN-Links herstellen, die keine Bandbreiteneinschränkungen aufweisen.

<div>

## <a name="see-also"></a>Siehe auch


[Modi für die Medienumgehung in Lync Server 2013](lync-server-2013-media-bypass-modes.md)  
[Medienumgehung und Anrufsteuerung in Lync Server 2013](lync-server-2013-media-bypass-and-call-admission-control.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

