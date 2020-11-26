---
title: 'Lync Server 2013: Löschen eines Chatrooms oder einer Kategorie'
description: 'Lync Server 2013: Löschen eines Chatrooms oder einer Kategorie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting a chat room or category
ms:assetid: adccb869-0015-4eba-ac73-718bac7843b5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215881(v=OCS.15)
ms:contentKeyID: 48706009
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3ef89802171a1eeca7de18ff0a4eb8eb3895f1b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430413"
---
# <a name="deleting-a-chat-room-or-category-in-lync-server-2013"></a>Löschen eines Chatrooms oder einer Kategorie in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-11-01_

Beständige Chatrooms können gelöscht werden. Wenn Sie über einen Chatroom verfügen, der nicht mehr verwendet wird, können Sie ihn deaktivieren. Ausführliche Informationen finden Sie unter [deaktivieren oder Aktivieren eines Chatrooms in lync Server 2013](lync-server-2013-disabling-or-enabling-a-chat-room.md).

Ein Administrator für beständigen Chat kann nach deaktivierten Chatrooms suchen und die Chatrooms in regelmäßigen Abständen mit dem Windows PowerShell **-Cmdlet Remove-CsPersistentChatRoom** löschen und endgültig löschen.

Kategorien können gelöscht werden. Um eine Kategorie zu löschen, müssen Sie jedoch zunächst entweder alle Chatrooms darunter löschen oder die Chatrooms in eine neue Kategorie verschieben, wodurch eine leere Kategorie zum Löschen bleibt. Mit dem Server für beständigen Chat können Sie keine Kategorie löschen, die Chatrooms enthält. Ausführliche Informationen finden Sie unter [Verschieben eines Chatrooms von einer Kategorie in eine andere in lync Server 2013](lync-server-2013-moving-a-chat-room-from-one-category-to-another.md).

Details zum Löschen von leeren Kategorien mithilfe der Windows PowerShell-Befehlszeilenoberfläche finden Sie unter "roomverwaltung" unter [Konfigurieren des beständigen Chat Servers mithilfe von Windows PowerShell-Cmdlets](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).

Details zu Chatrooms und Kategorien finden Sie unter [Konfigurieren von Räumen in lync Server 2013](lync-server-2013-configure-rooms.md) und [Konfigurieren von Kategorien in lync Server 2013](lync-server-2013-configure-categories.md) in der Bereitstellungsdokumentation.

</div>

<span> </span>

</div>

</div>

</div>

