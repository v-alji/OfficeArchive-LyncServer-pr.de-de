---
title: 'Lync Server 2013: Von der Ankündigungsanwendung verwendete Komponenten'
description: 'Lync Server 2013: von der Ankündigungs Anwendung verwendete Komponenten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by the Announcement application
ms:assetid: 7b1a0281-cf31-459d-a734-5f10a129089c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398608(v=OCS.15)
ms:contentKeyID: 48184595
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e5338ad097c814d5c6435bd89dbf7cfa8680feb8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394207"
---
# <a name="components-used-by-the-announcement-application-in-lync-server-2013"></a>Von der Ankündigungsanwendung in Lync Server 2013 verwendete Komponenten

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-13_

In lync Server 2013 ist die Ankündigungs Anwendung eine Komponente der reaktionsgruppenanwendung. Wenn Sie Enterprise-VoIP bereitstellen, wird die Ankündigungs Anwendung zusammen mit der reaktionsgruppenanwendung automatisch installiert und aktiviert. In diesem Abschnitt werden die Komponenten beschrieben, die die Ankündigungs Anwendung unterstützen.

<div>

## <a name="announcement-application-components"></a>Ankündigungs Anwendungskomponenten

Die folgenden lync Server-Komponenten unterstützen die Ankündigungs Anwendung:

  - **Anwendungsdienst**   Der Anwendungsdienst bietet eine Plattform zum Bereitstellen, hosten und Verwalten von Unified Communications-Anwendungen. Der Anwendungsdienst wird auf jedem Front-End-Server in einem Front-End-Pool und auf jedem Standard Edition-Server automatisch installiert.

  - **Reaktionsgruppenanwendung**   Die Antwortgruppen Anwendung ist eine der Unified Communications-Anwendungen, die vom Anwendungsdienst gehostet werden. Wenn ein nicht zugewiesener Telefonnummern Bereich so konfiguriert ist, dass er zu einer Ankündigung weitergeleitet wird, ist die reaktionsgruppenanwendung erforderlich, um die an die Telefonnummer vorgenommenen Anrufe weiterzuleiten. (Antwortgruppen Anwendung ist nicht erforderlich, wenn alle Bereiche für die Weiterleitung an Exchange Unified Messaging (um) konfiguriert sind.)

  - **Audiodateien**   Audiodateien werden für Ankündigungen verwendet.

  - **Dateispeicher**   Die Ankündigungs Anwendung verwendet den Dateispeicher zum Speichern der Audiodateien.

  - **Lync Server-System**   Steuerung   Sie können die lync Server-Systemsteuerung verwenden, um die Tabelle nicht zugewiesene Nummern zu konfigurieren.

  - **Lync Server-Verwaltungsshell**   Sie können Cmdlets der lync Server-Verwaltungsshell verwenden, um Ankündigungseinstellungen und die Tabelle nicht zugewiesene Nummern zu konfigurieren.

</div>

</div>

<span> </span>

</div>

</div>

</div>

