---
title: 'Lync Server 2013: Installieren von Lync Server-Serverkomponenten'
description: 'Lync Server 2013: Installieren der lync Server-Server Komponenten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Lync Server server components
ms:assetid: 186aed6e-7adf-4a92-9f2e-f9a4de5ff202
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398239(v=OCS.15)
ms:contentKeyID: 48183528
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1930926f3a46be868d838abf646eb8702c9713a8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427166"
---
# <a name="install-server-components-for-lync-server-2013"></a>Installieren von Serverkomponenten für Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2014-05-05_

Bevor Sie diese Schritte ausführen, stellen Sie sicher, dass Sie bei dem Server mit einem Domänenbenutzerkonto angemeldet sind, das sowohl ein lokaler Administrator als auch ein Mitglied der RTCUniversalReadOnlyAdmins-Gruppe in Active Directory ist.

Der lync Server-Bereitstellungs-Assistent wird verwendet, um die erforderlichen Komponenten für jede lync-Serverrolle zu installieren und den Server zu aktivieren. Dieser Artikel führt Sie durch die Schritte zum Bereitstellen eines Standard Edition-Servers oder eines Front-End-Servers in ihrer lync-Infrastruktur.

<div>

## <a name="to-install-lync-server-components"></a>So installieren Sie lync Server-Komponenten

1.  Wenn der lync Server-Bereitstellungs-Assistent nicht ausgeführt wird, starten Sie ihn auf dem Server, auf dem Sie lync installieren möchten.

2.  Klicken Sie auf **lync Server System installieren oder aktualisieren**.

3.  Bestätigen Sie im Bereitstellungs-Assistenten, dass **Schritt 1: Installieren des lokalen Konfigurationsspeichers** ein grünes Häkchen aufweist, was bedeutet, dass dieser Server eine lokale Kopie des Stores erfolgreich installiert hat. Wenn das Kontrollkästchen nicht aktiviert ist, müssen Sie den lokalen Konfigurationsspeicher auf dem Server installieren. Führen Sie die Schritte unter [Installieren des lokalen Konfigurationsspeichers in lync Server 2013](lync-server-2013-install-the-local-configuration-store.md) aus, und kehren Sie dann zurück.

4.  Wenn Sie bereit sind, die lync Server 2013-Komponenten auf dem Server zu installieren, klicken Sie auf **Ausführen** neben **Schritt 2: Einrichten oder Entfernen von lync Server-Komponenten**.

5.  Klicken Sie auf der Seite **lync Server-Komponenten einrichten** auf **weiter** , um Komponenten gemäß der Definition in der veröffentlichten Topologie einzurichten.

6.  Auf der Seite " **Befehle ausführen** " wird eine Zusammenfassung der Befehle und Installationsinformationen angezeigt, wenn die Einrichtung erfolgt. Nach Abschluss des Vorgangs können Sie in der angezeigten Liste ein Protokoll auswählen und auf **Protokoll anzeigen** klicken.

7.  Wenn das Setup von lync Server 2013-Komponenten abgeschlossen ist und Sie die Protokolle nach Bedarf überprüft haben, klicken Sie auf **Fertig stellen** , um diesen Schritt in der Installation abzuschließen.
    
    <div>
    

    > [!NOTE]  
    > Wenn Sie aufgefordert werden, den Server neu zu starten (was möglicherweise der Fall ist, wenn die Windows-Desktop Umgebung installiert werden muss), tun Sie dies unbedingt. Wenn der Computer wieder in Betrieb ist, müssen Sie diese Schritte wiederholen, beginnend mit Schritt 3, der oben aufgeführt ist (im Grunde Schritt 2 im Bereitstellungs-Assistenten ausführen).

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

