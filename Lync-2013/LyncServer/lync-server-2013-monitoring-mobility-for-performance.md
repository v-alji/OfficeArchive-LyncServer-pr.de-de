---
title: 'Lync Server 2013: Überwachen der Mobilität für die Leistung'
description: 'Lync Server 2013: Überwachen der Mobilität für die Leistung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring mobility for performance
ms:assetid: 9c831c63-9a7d-48ec-9118-f8a7e80ddd04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690033(v=OCS.15)
ms:contentKeyID: 48184908
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d6c366542e88406df043ba1a782ee12cd64bd804
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425402"
---
# <a name="monitoring-mobility-for-performance-in-lync-server-2013"></a>Überwachen der Mobilität für die Leistung in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-02-14_

Der lync Server Mobility Service (MCX) und die Unified Communications Web-API (UCWA) erhöhen die Auslastung von Front-End-Servern und Front-End-Pools. Mobile Geräte, die eine Verbindung mit dem Server beibehalten, auch wenn die Mobile Anwendung minimiert ist, wie etwa Android-und Nokia-Geräte mit lync 2010 Mobile sowie Android-und Apple-Geräte, auf denen lync 2013 Mobile ausgeführt wird, stellen eine größere Belastung als Geräte dar, die Ihre Verbindung mit dem Server kündigen, wenn die Mobile Anwendung minimiert wird. Nimmt die Nutzung der Mobilitätsdienste zu, müssen Sie die Mobilitätsleistung überwachen, um festzustellen, ob die Kapazität erhöht werden muss.

Die Mobilitätsleistung wird durch mehrere Limits beeinflusst:

  - Verfügbarer Speicher

  - Anforderungswarteschlangenlimit

  - Gleichzeitige Verbindungen

  - IIS-Warteschlangenlänge

Andere Grenzwerte für Server, die die Mobilitätsleistung beeinflussen können, sind maximal zwölf gleichzeitige Anmeldungen, Authentifizierungen, Sitzungs Verlängerungen und Kündigungen. Diese Höchstwerte müssen für die meisten Bereitstellungen nicht geändert werden.

<div>

## <a name="in-this-section"></a>In diesem Abschnitt

  - [Überwachen der Speicher Kapazitätsgrenzwerte von Servern in lync Server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)

  - [Überwachen des mobilitätsdiensts und der UCWA-Verwendung in lync Server 2013](lync-server-2013-monitoring-mobility-service-and-ucwa-usage.md)

  - [Konfigurieren des mobilitätsdiensts für die Höchstleistung in lync Server 2013](lync-server-2013-configuring-mobility-service-for-high-performance.md)

  - [Überwachen von IIS-Anforderungs Protokollierungs Protokolldateien in lync Server 2013](lync-server-2013-monitoring-iis-request-tracing-log-files.md)

  - [Mobilitäts Leistungsindikatoren in lync Server 2013](lync-server-2013-mobility-performance-counters.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

