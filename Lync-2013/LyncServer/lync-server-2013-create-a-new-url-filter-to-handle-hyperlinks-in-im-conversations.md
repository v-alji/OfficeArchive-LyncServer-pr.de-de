---
title: Erstellen eines neuen URL-Filters zur Behandlung von Links in Chat Unterhaltungen
description: Erstellen Sie einen neuen URL-Filter zur Behandlung von Links in Chat Unterhaltungen.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a new URL filter to handle hyperlinks in IM conversations
ms:assetid: d0ee01e5-f039-4a34-ac9d-659fe4e9e879
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182590(v=OCS.15)
ms:contentKeyID: 48185426
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6e583b3e8cbd04279ab7f54b4138a349fa0d1e85
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432121"
---
# <a name="create-a-new-url-filter-in-lync-server-2013-to-handle-hyperlinks-in-im-conversations"></a>Erstellen eines neuen URL-Filters in lync Server 2013 zur Behandlung von Hyperlinks in Chat Unterhaltungen

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-26_

Zusätzlich zum Ändern des globalen URL-Filters können Sie benutzerdefinierte URL-Filter für einzelne Websites in ihrer lync Server 2013-Bereitstellung konfigurieren. Details zur URL-Filterung finden Sie unter [Konfigurieren der Dateiübertragung und der URL-Filterung für Chatnachrichten in lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md).

<div>

## <a name="to-create-a-new-url-filter"></a>So erstellen Sie einen neuen URL-Filter

1.  Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.

2.  Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen. Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).

3.  Klicken Sie in der linken Navigationsleiste auf **Chat und Anwesenheit**, und klicken Sie dann auf **URL-Filter**.

4.  Klicken Sie auf der Seite **URL-Filter** auf **neu**.

5.  Klicken Sie unter **Website auswählen** auf die Website, für die Sie den URL-Filter erstellen möchten, und klicken Sie dann auf **OK**.

6.  Aktivieren Sie im Dialogfeld **neuer URL-Filter** das Kontrollkästchen **URL-Filter aktivieren** , um die URL-Filterung für die Website zu aktivieren.

7.  Aktivieren Sie das Kontrollkästchen **URLs mit Dateierweiterung blockieren** , um alle aktiven URLs zu blockieren, die eine Datei mit einer Erweiterung enthalten, die unter **Dateityperweiterungen zum Blockieren** in **Datei Filter bearbeiten** aufgeführt ist.

8.  Klicken Sie im Dropdown-Listenfeld **Link-Präfix** auf die Option, die dem entspricht, wie URLs in Chat Unterhaltungen behandelt werden sollen.
    
    Im Dialogfeld " **zulassen** " können Sie beim Senden von Links, die gesendet werden dürfen, eine Warnmeldung an den Benutzer senden.

9.  Klicken Sie auf **Commit ausführen**.

</div>

<div>

## <a name="see-also"></a>Siehe auch


[Konfigurieren der Dateiübertragung und der URL-Filterung für Chatnachrichten in lync Server 2013](lync-server-2013-configuring-file-transfer-and-url-filtering-for-instant-messaging-im.md)  
[Erstellen eines neuen dateiübertragungsfilters in lync Server 2013 für eine bestimmte Website](lync-server-2013-create-a-new-file-transfer-filter-for-a-specific-site.md)  
[Ändern des standardmäßigen dateiübertragungsfilters in lync Server 2013](lync-server-2013-modify-the-default-file-transfer-filter.md)  


[Ändern des Standard-URL-Filters in lync Server 2013](lync-server-2013-modify-the-default-url-filter.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

