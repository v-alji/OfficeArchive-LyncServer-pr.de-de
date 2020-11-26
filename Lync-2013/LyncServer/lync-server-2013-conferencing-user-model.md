---
title: Lync Server 2013 Conferencing-Benutzermodell
description: Lync Server 2013-Konferenzbenutzer Modell.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: The conferencing user model
ms:assetid: ba4bbba9-f2e3-4cab-8eba-b51f12133cab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205199(v=OCS.15)
ms:contentKeyID: 48185229
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 699f41303b82f4d8fd2864cbf1b29a1c601b826e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434279"
---
# <a name="the-conferencing-user-model-in-lync-server-2013"></a>Das Konferenzbenutzer Modell in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-22_

Ein wichtiger Bestandteil des Benutzermodells von lync Server Conferencing ist die Besprechungsgröße. Nach dem Sammeln von Daten aus mehreren Datenpunkten (wie im vorherigen Abschnitt beschrieben) haben wir Folgendes festgelegt:

  - Bei den meisten Besprechungen handelt es sich tatsächlich um kleine Besprechungs Besprechungen mit durchschnittlich vier bis sechs Teilnehmern.

  - Ungefähr 80 Prozent der Besprechungen haben weniger als 20 Teilnehmer.

  - 99,98% der Besprechungen haben weniger als 100 Teilnehmer.

Neben der Größe der Besprechung berücksichtigt das Konferenzbenutzer Modell auch eine Reihe von Faktoren, wie beispielsweise:

  - **Gleichzeitige Besprechungen**   Wie viele Benutzer werden in Besprechungen gleichzeitig erwartet?

  - **Medienmischung**   Welche Medientypen stehen zur Verfügung und werden von Benutzern in Besprechungen erwartet?

  - **Benutzertypen**   Sind Benutzer interne Benutzer, Remotebenutzer, Verbundbenutzer oder anonyme Benutzer?

  - **Besprechungszeit**   Wie lange dauert es, bis alle Benutzer einer Besprechung an einer Besprechung teilnehmen?

Details zum Benutzermodell finden Sie unter [Benutzermodelle in lync Server 2013](lync-server-2013-user-models.md).

Zum Ermitteln der Anzahl von Besprechungen und Benutzern, die für Tests verwendet werden sollen, haben wir die folgenden Schritte durchführen:

  - Nahm die Gesamtzahl der Benutzer in einer Organisation (beispielsweise 80.000-Benutzer) an und multipliziert Sie mit der Parallelitätsrate der Besprechung (beispielsweise 5% aller Benutzer), um die Gesamtzahl der Benutzer zu ermitteln, die gleichzeitig in Besprechungen erwartet werden (in diesem Beispiel 4000-Benutzer).

  - Dividiert die Gesamtzahl der Benutzer durch die Anzahl der lync Server 2013-Front-End-Server in der Bereitstellung (beispielsweise 8 Server), um die geschätzte Anzahl der Besprechungsteilnehmer pro Front-End-Server (in diesem Beispiel 500-Benutzer pro Front-End-Server) zu ermitteln.

  - Die Anzahl der Benutzer pro Front-End-Server wurde durch die durchschnittliche Besprechungsgröße (beispielsweise 4 Benutzer) dividiert, um die geschätzte durchschnittliche Anzahl der Besprechungen pro Front-End-Server (in diesem Beispiel 125-Besprechungen pro Front-End-Server) zu ermitteln.

  - Um die pro-Medien-Auslastung auf jedem Front-End-Server zu erhalten, schätzten wir den Media Mix. Wenn Sie beispielsweise davon ausgehen, dass 75% der Besprechungen mehr als nur Audio-Unterstützung erfordern und 50% dieser Besprechungen Anwendungsfreigabe erfordern, verbinden sich im Durchschnitt 47 Besprechungen und 188-Benutzer gleichzeitig mit jedem Front-End-Server für die Anwendungsfreigabe.

  - Eine Vielzahl von Besprechungs Größen getestet (basierend auf unserem Benutzermodell mit bis zu 250 Benutzern in einem gemeinsamen Pool), um die Serverskalierbarkeit zu gewährleisten.

</div>

<span> </span>

</div>

</div>

</div>

