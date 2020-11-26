---
title: Bewährte Methoden für den Server für beständigen Chat
description: Bewährte Methoden für beständigen Chat Server.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Persistent Chat Server best practices
ms:assetid: dc18e7f7-599b-4d32-abf7-cd9e691426a2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398970(v=OCS.15)
ms:contentKeyID: 48185612
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5c575c0afa0366e88748eadfcf4c04fccb20b375
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438785"
---
# <a name="persistent-chat-server-best-practices"></a>Bewährte Methoden für den Server für beständigen Chat

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-06_

Wenn Sie Ihre Kategorien und beständige Chatrooms erstellen und Ihr Scoping und Ihre Mitgliedschaft entwerfen, können Ihnen die folgenden Tipps bei der Planung helfen:

  - Wenn in Ihrem Unternehmen keine ethische Mauer erforderlich ist, schränken Sie den Bereich in der Kategoriestruktur nicht ein. Fügen Sie alle Ihre Benutzer in den Bereich einer Kategorie ein, und erstellen Sie alle Chatrooms in dieser Kategorie. Verwenden Sie anschließend nur Mitgliedschaftslisten, um den Zugriff auf jeden Chatroom zu gewähren oder einzuschränken.

  - In den meisten Fällen sollten Sie es Benutzern ermöglichen, neue Chatrooms zu erstellen, damit Diskussionen zu neuen Themen zu einem beliebigen Zeitpunkt gestartet werden können. Machen Sie dies, indem Sie die Liste der **Ersteller** auf die gleiche Weise wie die **AllowedMembers** -Liste erstellen. Wenn Sie jedoch nur einem zentralen Support Team oder bestimmten Benutzern das Erstellen von Räumen gestatten möchten, stellen Sie die Liste der **Ersteller** als geeignete Teilmenge dar.

  - Geben Sie jedem Chatroom einen vollständigen Namen und eine Beschreibungs Zusammenfassung, die beschreibt, wo er in Ihre Organisation passt. Da Benutzer den Kategorienamen nicht sehen können, wenn Sie den Chatroom verwenden, können Sie sich nicht darauf verlassen, dass der Kategorienname Benutzern hilft, das vorgesehene Diskussionsforum für den Chatroom zu ermitteln.

  - Möglicherweise möchten Sie einen benutzerdefinierten Raum Erstellungs Workflow haben, wenn bestimmte Benennungskonventionen oder andere Zugriffssteuerungen oder Validierungen implementiert werden. Mit der Konfiguration für beständigen Chat können Sie die **RoomManagementUrl** auf einen Host anpassen. Wenn Benutzer beispielsweise auf **einen Chatroom** in Ihrem lync-Client erstellen klicken, können Sie an Ihre benutzerdefinierte Lösung umgeleitet werden.

  - Erstellen Sie eine Vielzahl von Add-Ins, mit denen Sie die Erfahrung von Chatrooms verbessern können, indem Sie andere Geschäftsdaten in Chatrooms einbringen. Administratoren müssen die Add-Ins registrieren, die im System zugelassen werden sollen. Chatroom-Manager und-Entwickler können aus der Liste der zulässigen Add-Ins für diejenigen auswählen, die für die jeweiligen Chatrooms am relevantesten sind.

<div>

## <a name="see-also"></a>Siehe auch


[Verwalten von Kategorien, Chatrooms und Add-Ins in Lync Server 2013](lync-server-2013-managing-categories-rooms-and-add-ins.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

