---
title: 'Lync Server 2013: Von Reaktionsgruppen verwendete Komponenten'
description: 'Lync Server 2013: von der Reaktionsgruppe verwendete Komponenten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Response Group
ms:assetid: 2b058785-47ca-43b7-b3de-6928a60dc685
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425768(v=OCS.15)
ms:contentKeyID: 48183693
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2a1e916d9e4bf986bf0337a6f1f1dd918ff2772e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434557"
---
# <a name="components-used-by-response-group-in-lync-server-2013"></a>Von Reaktionsgruppen verwendete Komponenten in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-11_

Die reaktionsgruppenanwendung wird automatisch aktiviert, wenn Sie Enterprise-VoIP bereitstellen. In diesem Abschnitt werden die Komponenten beschrieben, die die reaktionsgruppenanwendung unterstützen.

<div>

## <a name="response-group-components"></a>Komponenten der Reaktionsgruppe

Die folgenden Microsoft lync Server 2013-Komponenten unterstützen die reaktionsgruppenanwendung:

  - **Anwendungsdienst**   Der Anwendungsdienst bietet eine Plattform zum Bereitstellen, hosten und Verwalten von Unified Communications-Anwendungen wie der Reaktionsgruppe. Der Anwendungsdienst wird automatisch auf jedem Front-End-Server in einem Front-End-Pool und auf jedem Standard Edition-Server installiert.

  - **Reaktionsgruppenanwendung**   Die Antwortgruppen Anwendung ist eine der Unified Communications-Anwendungen, die vom Anwendungsdienst gehostet werden. Sie wird automatisch einbezogen, wenn Sie die Reaktionsgruppe bereitstellen. Die Antwortgruppen Anwendung leitet eingehende Anrufe an Gruppen von Agents weiter und Warteschlangen.

  - **Sprachpaket**   Für die Unterstützung von Text-zu-Sprache-und Spracherkennung ist ein Sprachpaket erforderlich. Diese Sprachtechnologien werden zum Konfigurieren von Nachrichten verwendet, beispielsweise für die Willkommensnachricht oder für andere Ansagen sowie für Fragen und Antworten der interaktiven Sprachantwort (Interactive Voice Response, IVR). Standardmäßig werden die 26 unterstützten Sprachpakete installiert, wenn Sie lync Server 2013 bereitstellen.

  - **Audiodateien**   Audiodateien werden für Nachrichten und Musik im Wartebereich verwendet.

  - **Dateispeicher**   Die Reaktionsgruppe verwendet den Dateispeicher zum Speichern von Audiodateien. Mehrere Antwortgruppen Pools können dieselbe Instanz des Dateispeichers verwenden.

  - **Reaktionsgruppen-Konfigurations Tool**   Das Tool für die Reaktionsgruppen-Konfiguration ist ein webbasiertes Tool, das zum Erstellen und Konfigurieren von Reaktionsgruppen verwendet wird. Beim Installieren von Webdiensten ist das Tool für die Reaktionsgruppen Konfiguration enthalten.

  - **Microsoft lync Server 2013-System**   Steuerung   Mit der lync Server-Systemsteuerung können Sie Agentengruppen und-Warteschlangen für Reaktionsgruppen einrichten und konfigurieren.

  - **Lync Server-Verwaltungsshell**   Alle Einstellungen der Reaktionsgruppe können mithilfe der lync Server-Verwaltungsshell-Cmdlets konfiguriert werden.

  - **Microsoft lync 2013**   Formelle Agents (Agents, die sich bei der Gruppe anmelden müssen, bevor Sie Anrufe für die Gruppe annehmen können) verwenden Sie lync 2013, um sich bei der Gruppe anzumelden und sich abzumelden. Wenn eine Agentengruppe für formelle Agents konfiguriert ist, klicken die Agents auf ein Menüelement in lync 2013, um Internet Explorer zu öffnen und eine Webseite-Konsole für die Anmeldung bei der Gruppe anzuzeigen.

  - **Web Services**   Webdienste sind für das Reaktionsgruppen-Konfigurations Tool, die Anmelde-und Abmelde Konsole des Agents, die lync Server-Systemsteuerung und den Client-Webdienst der Reaktionsgruppe erforderlich.

  - **Client-Webdienst für Reaktionsgruppen**   Die Antwortgruppen Anwendung bietet einen Client-Webdienst, der von Drittanbieteranwendungen verwendet werden kann, um Informationen zu Agents, Agentengruppen Mitgliedschaft, Agent-Anmeldestatus, Anrufstatus für Gruppen und die Gruppen abzurufen, die anonyme Anrufe unterstützen. Lync 2013 und lync 2010 Attendant verwenden den Client-Webdienst der Reaktionsgruppe, um die Liste der Antwortgruppen abzurufen, die von Agents für anonyme Anrufe verwendet werden können. Der Client-Webdienst ist bei der Installation von Webdiensten enthalten.

</div>

</div>

<span> </span>

</div>

</div>

</div>

