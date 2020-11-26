---
title: 'Lync Server 2013: Entscheiden, wie Microsoft Lync bereitgestellt werden soll'
description: 'Lync Server 2013: entscheiden, wie Microsoft lync bereitgestellt wird.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deciding how to deploy Microsoft Lync
ms:assetid: 6ca677d3-745d-4935-8f05-19274a8bccf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204979(v=OCS.15)
ms:contentKeyID: 48184423
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a800b51dfddc6f2c99e42c8f117056ed4091b6a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431232"
---
# <a name="deciding-how-to-deploy-lync-server-2013"></a>Entscheiden, wie Lync Server 2013 bereitgestellt werden soll

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-03_

Bei der Planung für lync ist die erste wichtige Entscheidung, wie Microsoft lync bereitgestellt wird: als lync Server 2013 lokal oder lync online mit Microsoft 365 oder Office 365 in der Cloud.

  - **Lync Server 2013 lokal** : Diese Auswahl bietet den vollständigen lync-Funktionssatz und bietet höchste Flexibilität bei der Konfiguration, dem anpassen und dem Betrieb Ihrer Bereitstellung. Alle Server werden vor Ort installiert und von Ihrer Organisation verwaltet. Eine lokale Bereitstellung bietet die gesamte Palette der lync Server-Funktionen.

  - **Lync Online in der Cloud** Lync Online ist für Organisationen konzipiert, die den Kosten-und Agilitäts Vorteil von Cloud-basiertem Instant Messaging, Anwesenheitsinformationen und Besprechungen benötigen, ohne die Business-Class-Funktionen von lync Server zu beeinträchtigen. Mit lync Online stellt Microsoft die erforderliche Serverinfrastruktur bereit und verwaltet Sie und verarbeitet laufende Wartung, Patches und Upgrades. Einige Features, die in einer lokalen Bereitstellung verfügbar sind, stehen in lync Online nicht zur Verfügung.

Welche Art der Bereitstellung für Sie am besten geeignet ist, hängt von den Arbeitsauslastungen, die Sie bereitstellen möchten, und dem geografischen und geschäftlichen Status Ihrer Organisation ab.

<div>

## <a name="lync-server"></a>Lync Server

Eine lokale lync Server-Bereitstellung eignet sich am besten für die folgenden Szenarien:

  - **Vollständige Enterprise-VoIP-Funktionen**   Wenn Sie beabsichtigen, eine vollständige Enterprise-VoIP-Lösung bereitzustellen, um Ihre Telefonanlage zu ersetzen oder erweiterte Anruffunktionen verwendet, ist eine lokale lync Server-Bereitstellung erforderlich. Lokale Unterstützung bietet direkte Konnektivität mit PBX-Systemen und-Stämmen sowie erweiterte Telefonfunktionen wie Reaktionsgruppen und Parken von anrufen. Lync Online unterstützt diese Features zurzeit nicht.

  - **Media Quality-Steuerelemente**   Wenn Sie die gesamte Bandbreite der Medien Qualitätssicherungs-Features wie Anrufannahme Steuerung (CAC) und QoS-Features (Quality of Service) nutzen möchten, benötigen Sie eine lokale Bereitstellung.

  - **Beständiger Chat**   Wenn Sie den beständigen Chat für Ihre Organisation bereitstellen müssen, müssen Sie eine lokale Bereitstellung auswählen.

  - **Server Anwendungen von Drittanbietern**   Nur lokale Bereitstellungen können mit vertrauenswürdigen Drittanbieteranwendungen funktionieren, die die Microsoft Unified Communications Managed API (UCMA) verwenden.

  - **Multi-National/Multi-Regional-Unternehmen, die regionale Unterstützung benötigen**   Wenn Sie über Rechenzentren in mehreren Ländern oder Regionen verfügen und Server auf regionaler Basis bereitgestellt und verwaltet werden müssen, ist eine lokale Bereitstellung am besten geeignet, da diese Art von regionalen Verwaltungsfunktionen zur Verfügung steht.

  - **Vollständige Kontrolle über Richtlinien, Berichte und Upgrades**   Mit einer lokalen lync Server-Bereitstellung haben Sie Zugriff auf den vollständigen Satz von Server-und Clientrichtlinien, Überwachungs-und anderen Berichten sowie die Anzeigedauer von Upgrades. Lync Online bietet eine Teilmenge der Richtlinieneinstellungen und-Berichte und bietet ein limitiertes, wenn auch erhebliches Fenster für das akzeptieren von Upgrades.

</div>

<div>

## <a name="lync-online"></a>Lync Online

Wenn keiner der Faktoren in der vorstehenden Liste für Sie von entscheidender Bedeutung ist, sollten Sie lync online zur einfacheren Bereitstellung und Verwaltbarkeit auswählen. Lync Online bietet eine robuste Chat-, Anwesenheits-und Konferenz Funktionsgruppe und ermöglicht auch sprach-und Videoanrufe über IP zwischen Benutzern in Ihrer Organisation.

</div>

</div>

<span> </span>

</div>

</div>

</div>
