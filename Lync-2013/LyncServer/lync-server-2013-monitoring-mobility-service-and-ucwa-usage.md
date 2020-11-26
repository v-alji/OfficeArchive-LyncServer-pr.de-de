---
title: 'Lync Server 2013: Überwachen des mobilitätsdiensts und der UCWA-Verwendung'
description: 'Lync Server 2013: Überwachen des mobilitätsdiensts und der UCWA-Verwendung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Monitoring Mobility Service and UCWA usage
ms:assetid: 8389b37a-ca3e-4047-8b51-85bc07da87e8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690025(v=OCS.15)
ms:contentKeyID: 48184683
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6575941faf904e46cd1f66d7226a16c88e8cbaa3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425395"
---
# <a name="monitoring-mobility-service-and-ucwa-usage-in-lync-server-2013"></a>Überwachen des mobilitätsdiensts und der UCWA-Verwendung in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-02-14_

Auf einer kontinuierlichen Basis sollten Sie die CPU und den Arbeitsspeicher überwachen, die vom lync Server Mobility Service (MCX) und der Unified Communications Web-API (UCWA) verwendet werden. Zum Überwachen der Auslastung können Sie Folgendes verwenden:

**Für die Unified Communications-Web-API (UCWA):**

  - Der **LyncUcwa** -Workerprozess im Internet Informationsdienste (IIS)-Manager. Sehen Sie sich im Bereich **Arbeitsprozesse** die Spalten **CPU %** und **Private Bytes (KB)** an.

  - Die Leistungsindikatoren **CPU** und **Prozessor**.

Bei den meisten Bereitstellungen sollte die UCWA-CPU-Auslastung im Durchschnitt unter 15 Prozent liegen. Die Speicherauslastung sollte innerhalb der Grenzwerte liegen, die unter [Überwachen der Speicher Kapazitätsgrenzwerte von Servern in lync Server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)beschrieben werden.

Neben den Leistungsindikatoren für die CPU- und Speicherauslastung können Sie anhand der folgenden Leistungsindikatoren feststellen, ob ein Server mit Anforderungen überlastet ist:

  - **Ls: Web – Drosselung und Authentifizierung \\ Web – Gesamtanforderungen in der Verarbeitung**, die die Anzahl der ausstehenden Webanforderungen auf dem Server angeben. Wenn dieser Leistungsindikator 10.000 erreicht, schlagen nachfolgende Anforderungen mit der Fehlermeldung „503 - Dienst nicht verfügbar“ fehl.

  - **ASP.net \\ Anforderungen in der Warteschlange** (sollten immer 0 sein).

<div>


> [!NOTE]  
> Wenn Sie diese Werte erfüllen oder übertreffen, sollten Sie Ihre Kapazitätsplanung erneut überarbeiten und neu berechnen, um die korrekte Größe der CPU, die Anzahl der Kerne und den Arbeitsspeicher für die Computer zu ermitteln, die die Webdienste hosten.



</div>

**Für den Mobilitätsdienst (Mcx):**

  - Die **CSIntMcxAppPool** -und **CSExtMcxAppPool** -Arbeitsprozesse im Internet Informationsdienste (IIS)-Manager. Sehen Sie sich im Bereich **Arbeitsprozesse** die Spalten **CPU %** und **Private Bytes (KB)** an.

  - Die Leistungsindikatoren **CPU** und **Prozessor**.

Bei den meisten Bereitstellungen sollte die Mobilitätsdienst-CPU-Auslastung im Durchschnitt unter 15 Prozent liegen. Die Speicherauslastung sollte innerhalb der Grenzwerte liegen, die unter [Überwachen der Speicher Kapazitätsgrenzwerte von Servern in lync Server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)beschrieben werden.

Neben den Leistungsindikatoren für die CPU- und Speicherauslastung können Sie anhand der folgenden ASP.NET-Leistungsindikatoren feststellen, ob ein Server mit Anforderungen überlastet ist:

  - **ASP.NET v 2.0.50727 \\ Aktuelle Anforderungen**, die die Anzahl der ausstehenden Webanforderungen auf dem Server angeben. Wenn dieser Leistungsindikator 5.000 erreicht, schlagen nachfolgende Anforderungen mit der Fehlermeldung „503 - Dienst nicht verfügbar“ fehl.

  - **ASP.net \\ Anforderungen in der Warteschlange** (sollten immer 0 sein).

<div>


> [!NOTE]  
> Wenn Sie diese Werte erfüllen oder übertreffen, sollten Sie Ihre Kapazitätsplanung erneut überarbeiten und neu berechnen, um die richtige Größe der CPU, der Anzahl der Kerne und des Arbeitsspeichers für die Computer zu finden, die die Webdienste hosten.



</div>

<div>

## <a name="see-also"></a>Siehe auch


[Überwachen der Speicher Kapazitätsgrenzwerte von Servern in lync Server 2013](lync-server-2013-monitoring-for-server-memory-capacity-limits.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

