---
title: 'Lync Server 2013: QoE-Berichte'
description: 'Lync Server 2013: QoE-Berichte.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: QoE reports
ms:assetid: 49c827af-b8dd-4c6e-b0dc-b4bc6d60e9a3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720913(v=OCS.15)
ms:contentKeyID: 63969601
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 55965d246b7f0ddd71eaeeec99d218eaf8819c2e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394526"
---
# <a name="qoe-reports-in-lync-server-2013"></a>QoE-Berichte in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2014-05-01_

<div>

## <a name="qoe-summarytrend-reports"></a>QoE-Zusammenfassung/Trendberichte

Die Berichte QoE-Zusammenfassung/Trends sind hilfreich, um die Spitzenzeiten für die Nutzung zu ermitteln und die Medienqualität in diesen Zeiten zu untersuchen, um sicherzustellen, dass die Netzwerkressourcen Ihrer Organisation ausreichend sind. Ihre Organisation kann auch die zahlreichen im Bericht verfügbaren Filter verwenden, um Leistungsnummern für bestimmte Speicherorte, Client-und Gerätetypen und Server zu isolieren.

QoE-Zusammenfassung/Trendberichte bestehen aus:

  - UC-zu-UC-Zusammenfassung/Trend Bericht

  - PSTN-Zusammenfassung/Trend Bericht

  - Konferenz Zusammenfassung/Trend Bericht

</div>

<div>

## <a name="qoe-performance-reports"></a>QoE-Leistungsberichte

QoE-Leistungsberichte bieten Details zu den drei Berichten, die sich auf die QoE-Leistung von Mediations Servern, A/V-Konferenzservern und Endpunkt Speicherorten konzentrieren.

</div>

<div>

## <a name="mediation-server-performance-report"></a>Bericht zur Vermittlungsserver Leistung

Im Bericht "Vermittlungs Server Leistung" werden die Metriken aufgelistet, die von einer oder mehreren Mediation während des angegebenen Zeitraums erreicht wurden. Die Metriken für das Unified Communications (UC)-to-Mediation-Server Bein und das Vermittlungsserver-zu-Gateway-Bein jedes Anrufs werden separat gemeldet. Mit diesem Bericht können Sie die Lautstärke und Leistung der verschiedenen Vermittlungsserver Ihrer Organisation vergleichen.

Für jeden Vermittlungs Server (und für jedes Anruf Bein) wird im Bericht Folgendes angezeigt:

  - Anzahl der Anrufe

  - Paketverlust

  - Round-Trip-Zeit

  - Jitter

  - Conversational Mean Opinion Score (MOS)

  - Senden von MOS

  - Anhören von MOS

  - Netzwerk-Mos

  - Netzwerk-Mos-Verschlechterung

  - Echo-Rückgabe

  - Signal Pegel

</div>

<div>

## <a name="av-conferencing-server-performance-report"></a>A/V-Konferenzserver-Leistungsbericht

Der Leistungsbericht a/v Conferencing Server bietet Listen mit Metriken, die von einem oder mehreren a/v-Konferenzservern während des angegebenen Zeitraums erreicht wurden. Dieser Bericht kann verwendet werden, um die Lautstärke und Leistung der verschiedenen A/V-Konferenzserver Ihrer Organisation zu vergleichen. Ihre Organisation kann den Bericht auch isolieren, um nur die Benutzeroberfläche für bestimmte Clienttypen wie lync-Clients oder PSTN-Clients anzuzeigen.

Für jeden A/V-Konferenz Server wird im Bericht Folgendes angezeigt:

  - Anzahl von Konferenzen

  - Paketverlust

  - Round-Trip-Zeit

  - Jitter

  - Conversational Mean Opinion Score (MOS)

  - Senden von MOS

  - Anhören von MOS

  - Netzwerk-Mos

  - Netzwerk-Mos-Verschlechterung

  - Echo-Rückgabe

  - Signal Pegel

</div>

<div>

## <a name="location-based-performance-report"></a>Bericht zur standortbasierten Leistung

Der Location-Based Leistungsbericht enthält eine Liste der Netzwerkspeicherorte, und für jeden Standort wird die Anzahl der Anrufe in jedem zuvor festgelegten Qualitätsbereich angezeigt. Ziel dieses Berichts ist es, Einblicke in die Medienqualität des Großteils der Telefonanrufe Ihrer Organisation an verschiedenen Standorten zu geben, damit Sie schlecht darstellende Standorte erkennen und die unterschiedlichen Grade der Medienqualität in den verschiedenen Speicherorten Ihrer Organisation sehen können.

Beim Anzeigen des Berichts werden unterschiedliche Tabellen mit Metriken angezeigt – eine Tabelle für jede Metrik, über die Ihre Organisation berichten möchte. Sie können aus den folgenden Metriken für diesen Bericht wählen:

  - Conversational Mean Opinion Score (MOS)

  - Netzwerk-Mos

  - Netzwerk-Mos-Verschlechterung

  - Senden von MOS

  - Anhören von MOS

  - Paketverlust

  - Jitter

  - Latenz

</div>

</div>

<span> </span>

</div>

</div>

</div>

