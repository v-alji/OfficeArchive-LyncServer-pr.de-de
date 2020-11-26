---
title: 'Lync Server 2013: Failover des zentralen Verwaltungsspeichers'
description: Failover des zentralen Verwaltungsspeichers für lync Server 2013
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Central Management store failover
ms:assetid: f464d715-68a4-462c-9584-00f41ab10db0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205376(v=OCS.15)
ms:contentKeyID: 48185809
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d2960a55d6bdc49e00bf22997bc53946d4770fde
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435467"
---
# <a name="central-management-store-failover-in-lync-server-2013"></a>Failover des zentralen Verwaltungsspeichers in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-18_

Der zentrale Verwaltungsspeicher enthält Konfigurationsdaten zu Servern und Diensten in ihrer lync 2013-Bereitstellung. Sie bietet eine robuste, schematisierten Speicherung der Daten, die zum definieren, einrichten, warten, verwalten, beschreiben und betreiben einer lync 2013-Bereitstellung erforderlich sind. Darüber hinaus überprüft er die Daten, um eine konsistente Konfiguration zu gewährleisten.

Jede lync-Bereitstellung umfasst einen zentralen Verwaltungsspeicher, der vom Back-End-Server eines Front-End-Pools gehostet wird.

Wenn Sie eine Pool Kopplung einrichten, die den Pool hostet, in dem der zentrale Verwaltungsspeicher gehostet wird, wird im Sicherungspool eine Datenbank des zentralen Verwaltungsspeichers eingerichtet, und die zentralen Verwaltungsspeicher Dienste werden in beiden Pools installiert. Eine der beiden zentralen Verwaltungsspeicher Datenbanken ist zu einem beliebigen Zeitpunkt der aktive Master und der andere ein Standbymodus. Der Inhalt wird vom Sicherungsdienst vom aktiven Master in den Standbymodus repliziert.

Bei einem Pool-Failover, das die Pools umfasst, die den zentralen Verwaltungsspeicher hosten, muss der Administrator vor dem Failover des Front-End-Pools einen Failover für den zentralen Verwaltungsspeicher durchführen.

Nach der Behebung des Notfalls ist es nicht erforderlich, einen Failback des zentralen Verwaltungsspeichers durchzuführen. Nach der Reparatur kann der zentrale Verwaltungsspeicher im ursprünglichen Sicherungspool als aktiver MasterVerb leiben.

Die Entwicklungsziele für den zentralen Verwaltungsspeicher sind 5 Minuten für die Wiederherstellungsdauer (Recovery Time Objective, RTO) und 5 Minuten für den Wiederherstellungspunkt (Recovery Point Objective, RPO).

</div>

<span> </span>

</div>

</div>

</div>

