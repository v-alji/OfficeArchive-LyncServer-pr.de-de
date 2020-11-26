---
title: 'Lync Server 2013: Löschen einer Nachricht oder Löschen von veralteten Nachrichten'
description: 'Lync Server 2013: Löschen einer Nachricht oder bereinigen veralteter Nachrichten'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting a message or purging obsolete messages
ms:assetid: 3f0c612d-6dfd-41a4-a5fe-5ff3448eb0ce
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215874(v=OCS.15)
ms:contentKeyID: 48706000
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 928e34d2ab52b02155568c7da96e4ac1d8154b7a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430406"
---
# <a name="deleting-a-message-or-purging-obsolete-messages-in-lync-server-2013"></a>Löschen einer Nachricht oder Löschen von veralteten Nachrichten in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2014-02-05_

Ein beständiger Chat-Administrator kann eine Nachricht aus einem beständigen Chatroom löschen (optional kann Sie durch eine andere Nachricht ersetzt werden). Administratoren können auch veraltete Nachrichten im Rahmen der laufenden Wartung bereinigen, um das Wachstum der Datenbank zu minimieren. Mit diesem Windows PowerShell-Befehl werden beispielsweise alle Nachrichten aus dem ITChatRoom-Chatroom entfernt, die vom Benutzer kenmyer@litwareinc.com gepostet wurden:

    Remove-CsPersistentChatMessage -Identity "atl-persistentchat-001.litwareinc.com\ITChatRoom" -UserUri "sip:kenmyer@litwareinc.com"

In diesem Beispiel werden alle entfernten Nachrichten durch den Hinweis ersetzt, dass die Nachricht nicht mehr verfügbar ist:

    Remove-CsPersistentChatMessage -Identity "atl-persistentchat-001.litwareinc.com\ITChatRoom" -UserUri "sip:kenmyer@litwareinc.com" -ReplaceMessage "This message is no longer available."

Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Remove-CsPersistentChatMessage](https://docs.microsoft.com/powershell/module/skype/Remove-CsPersistentChatMessage) .

</div>

<span> </span>

</div>

</div>

</div>

