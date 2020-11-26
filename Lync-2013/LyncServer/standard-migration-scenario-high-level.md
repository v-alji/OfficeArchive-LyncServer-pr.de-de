---
title: Standardmigrationsszenario – Übersicht
description: Standard Migrationsszenario – auf höherer Ebene.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Standard migration scenario - high-level
ms:assetid: e768a7ca-44e3-4969-a6d9-7ed3e7029c5c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205354(v=OCS.15)
ms:contentKeyID: 48185709
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a931b76e528b7e6468f6b7e7b9a718724d27501f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438757"
---
# <a name="standard-migration-scenario---high-level"></a>Standardmigrationsszenario – Übersicht

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-01-30_

Verwenden Sie die folgenden Elemente als Ausgangspunkt für die Migration von lync Server 2010, Gruppen-Chat oder Office Communications Server 2007 R2-Gruppenchat zu lync Server 2013, beständiger Chat Server. Der Standard-Migrationspfad für lync Server 2013 lautet wie folgt:

  - Ihre Organisation hat zuvor lync Server 2010, Gruppen-Chat oder Office Communications Server 2007 R2-Gruppen-Chat bereitgestellt, und Sie möchten lync Server 2013, beständiger Chat Server bereitstellen.

  - Stellen Sie lync Server 2013 bereit, und stellen Sie dann den Server Pool für beständigen Chat bereit.

  - Vorbereiten und planen Sie die Migration Ihrer beständigen Chatrooms, und bestimmen Sie einen geeigneten Zeitpunkt für das Herunterfahren des Systems für die Migration.

  - Führen Sie die Windows PowerShell-Cmdlets für die Migration aus (**Export-CsPersistentChatData** und **Import-CsPersistentChatData**), um Inhalte in den beständigen Chat Server zu verschieben.

  - Überprüfen Sie, ob die Migration erfolgreich war.

  - Außerbetriebnahme Ihrer Legacy Bereitstellung

  - Konfigurieren Sie den Server für beständigen Chat, damit Legacyclients eine Verbindung mit lync Server 2013, persistent Chat Server herstellen können. Dies ist erforderlich, da es Zeit braucht, um neue Clients bereitzustellen, und Sie möchten, dass vorhandene Benutzer mit älteren Clients so schnell wie möglich auf Ihre Chatrooms zugreifen können.

  - Stellen Sie neue Clients bereit, während Sie weiterhin sicherstellen, dass Mitarbeiter mit Legacy-Gruppen-Chats (Clients) in Ihre Chatrooms gelangen können.

</div>

<span> </span>

</div>

</div>

</div>

