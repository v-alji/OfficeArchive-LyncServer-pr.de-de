---
title: 'Lync Server 2013: Veröffentlichen der aktualisierten Topologie'
description: 'Lync Server 2013: Veröffentlichen der aktualisierten Topologie'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish the updated topology
ms:assetid: 59455dd1-6a9e-433f-a714-d3636c068100
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204910(v=OCS.15)
ms:contentKeyID: 48184203
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c27cca2eae86eadaf1ff37e2c3520eaec3f86c98
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394559"
---
# <a name="publish-the-updated-topology-in-lync-server-2013"></a>Veröffentlichen der aktualisierten Topologie in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-01_

Nachdem Sie Ihre Topologie im Topologie-Generator aktualisiert haben, müssen Sie die Topologie im zentralen Verwaltungsspeicher veröffentlichen, bevor Sie den Server für beständigen Chat Konfigurieren und verwenden können. Schreibgeschützte Kopien der Daten werden auf alle Server in der Topologie repliziert, sodass diese Server mit der Topologie und anderen Konfigurationsänderungen synchronisiert sind.

<div>

## <a name="to-publish-an-updated-topology"></a>So veröffentlichen Sie eine aktualisierte Topologie

Bevor Sie Ihre Topologie veröffentlichen, installieren Sie die Datenbanken für beständigen Chat Server. Mithilfe des Topologie-Generators können Sie Datenbanken installieren, indem Sie **Aktion** und **Datenbank installieren** auswählen.

1.  Melden Sie sich auf einem Computer, auf dem lync Server 2013 ausgeführt wird oder auf dem die lync Server-Verwaltungstools installiert sind, mit einem Konto an, das Mitglied sowohl der Gruppe der **Domänenadministratoren** als auch der **RTCUniversalServerAdmins** -Gruppe ist. und die über die Berechtigung "Vollzugriff" (also lesen, schreiben und ändern) im Dateispeicher für den Dateispeicher für beständigen Chat Server verfügt (damit der Topologie-Generator die erforderlichen DACLs (Discretionary Access Control Lists) oder ein Konto mit entsprechenden Benutzerrechten konfigurieren kann.

2.  Starten Sie den Topologie-Generator. Wählen Sie **Topologie aus vorhandener Bereitstellung herunterladen** aus, oder **Öffnen Sie die Topologie aus einer lokalen Datei** , wenn Sie Sie lokal gespeichert haben.

3.  Klicken Sie in der Konsolenstruktur mit der rechten Maustaste auf **lync Server 2013**, und klicken Sie dann auf **Topologie veröffentlichen**.

4.  Klicken Sie auf der Seite **Topologie veröffentlichen** auf **Weiter**.

5.  Vergewissern Sie sich auf der Seite **Veröffentlichungs-Assistent abgeschlossen**, dass die Topologie erfolgreich veröffentlicht wurde, und klicken Sie anschließend auf **Fertig stellen**.
    
    <div>
    

    > [!IMPORTANT]  
    > Nachdem Sie die Topologie veröffentlicht haben, müssen Sie die Unterstützung für beständigen Chat Server konfigurieren, bevor Inhalte archiviert werden können.

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

