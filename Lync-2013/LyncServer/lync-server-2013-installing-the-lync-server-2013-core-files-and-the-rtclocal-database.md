---
title: Installieren der lync Server 2013-Core-Dateien und der RTCLocal-Datenbank
description: Installieren der lync Server 2013-Core-Dateien und der RTCLocal-Datenbank
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing the Lync Server 2013 core files and the RTCLocal database
ms:assetid: 206f0c1d-40f7-45b6-aa62-88aaef6cf7f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204734(v=OCS.15)
ms:contentKeyID: 48183591
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 68964f8b80f6377afd859d113783d61e33afbebd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426998"
---
# <a name="installing-the-lync-server-2013-core-files-and-the-rtclocal-database"></a>Installieren der lync Server 2013-Core-Dateien und der RTCLocal-Datenbank

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-20_

Führen Sie die folgenden Schritte aus, um die Core-Dateien von lync Server 2013 auf einem Computer zu installieren. Die RTCLocal-Datenbank wird automatisch installiert, wenn Sie die Core-Dateien installieren. Beachten Sie, dass Sie SQL Server nicht auf den Watcher-Knoten installieren müssen. Stattdessen wird SQL Server Express automatisch für Sie installiert.

So installieren Sie die lync Server 2013-Core-Dateien und die RTCLocal-Datenbank:

1.  Klicken Sie auf dem Watcher-Knoten Computer auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Zubehör**, klicken Sie mit der rechten Maustaste auf **Eingabeaufforderung**, und klicken Sie dann auf **als Administrator ausführen**.

2.  Geben Sie im Konsolenfenster den folgenden Befehl ein, und drücken Sie dann die EINGABETASTE, und verwenden Sie den entsprechenden Pfad zu ihren lync Server-Setupdateien:
    
        D:\Setup.exe /BootstrapLocalMgmt

Um zu überprüfen, ob die zentralen lync Server-Komponenten erfolgreich installiert wurden, klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**. Geben Sie in der lync Server 2013-Verwaltungsshell den folgenden Windows PowerShell-Befehl ein, und drücken Sie dann die EINGABETASTE:

    Get-CsWatcherNodeConfiguration

Wenn Sie diesen Befehl zum ersten Mal ausführen, werden keine Daten zurückgegeben, da Sie noch keine Watcher-Knoten Computer konfiguriert haben. Solange der Befehl ausgeführt wird, ohne einen Fehler zurückzugeben, können Sie davon ausgehen, dass das lync Server-Setup erfolgreich abgeschlossen wurde.

Wenn sich Ihr Watcher-Knoten Computer in Ihrem Umkreisnetzwerk befindet, können Sie den folgenden Befehl ausführen, um die Installation von lync Server 2013 zu überprüfen:

    Get-CsPinPolicy

Je nach der Anzahl der für die Verwendung in Ihrer Organisation konfigurierten Richtlinien für die persönliche Identifikationsnummer (PIN) erhalten Sie Informationen ähnlich wie die folgenden:

    Identity             : Global
    Description          :
    MinPasswordLength    : 5
    PINHistoryCount      : 0
    AllowCommonPatterns  : False
    PINLifetime          : 0
    MaximumLogonAttempts :

Wenn Sie Informationen zu Ihren PIN-Richtlinien sehen, bedeutet dies, dass Sie die Kernkomponenten erfolgreich installiert haben.

</div>

<span> </span>

</div>

</div>

</div>

