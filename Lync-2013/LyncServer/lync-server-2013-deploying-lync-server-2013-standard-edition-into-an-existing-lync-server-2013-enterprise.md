---
title: 'Lync Server 2013: Bereitstellen von Lync Server 2013 Standard Edition in einer vorhandenen Lync Server 2013 Enterprise-Bereitstellung'
description: 'Lync Server 2013: Bereitstellen von lync Server 2013 Standard Edition in einem vorhandenen lync Server 2013 Enterprise.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying Lync Server 2013 Standard Edition into an existing Lync Server 2013 Enterprise
ms:assetid: 05ea128d-6c94-49b3-b28b-477367196425
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398112(v=OCS.15)
ms:contentKeyID: 48183297
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b233d4e782e716904fca0a2a146b2459e906aa57
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429951"
---
# <a name="deploying-lync-server-2013-standard-edition-into-an-existing-lync-server-2013-enterprise"></a>Bereitstellen von Lync Server 2013 Standard Edition in einer vorhandenen Lync Server 2013 Enterprise-Bereitstellung

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-01_

Die Bereitstellungeines Standard Edition-Servers in einer vorhandenen Enterprise Edition-Bereitstellung ähnelt der Bereitstellung zusätzlicher Serverrollen. Ein Standard Edition-Server kann auf einer anderen Website bereitgestellt werden, sodass die Benutzer auf dieser Website auf dem Standard Edition-Server statt im Front-End-Pool über ein WAN (Wide Area Network) verwaltet werden können. Die Verfahren zum Installieren der neuen Website und der neuen Server auf dieser Website sind bereits in anderen Abschnitten der [Bereitstellung von lync Server 2013](lync-server-2013-deploying-lync-server.md) -Dokumentation definiert.

<div id="sectionSection0" class="section">

**So definieren Sie eine neue Website**

1.  Starten Sie den Topologie-Generator: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server Topology Builder**.

2.  Klicken Sie in der Konsolenstruktur mit der rechten Maustaste auf **lync Server 2013**, und klicken Sie dann auf **neue zentrale Website**.

3.  Geben Sie auf der Seite **Website identifizieren** einen Namen für die Website ein, und geben Sie optional eine Beschreibung ein.

4.  Befolgen Sie die Verfahren zum Definieren der restlichen Website Topologie. Ausführliche Informationen finden Sie unter [definieren und Konfigurieren der Topologie in lync Server 2013](lync-server-2013-defining-and-configuring-the-topology.md).

5.  Veröffentlichen der aktualisierten Topologie Ausführliche Informationen finden Sie unter [Veröffentlichen der Topologie in lync Server 2013](lync-server-2013-publish-the-topology.md).

6.  Einrichten und Installieren eines Standard Edition-Servers
    
    <div>
    

    > [!Caution]  
    > Wenn Sie eine Umgebung mit nur einem Standard Edition-Server bereitgestellt haben, hätten Sie den Setup-Vorgang mit dem lync Server-Bereitstellungs-Assistenten begonnen, indem Sie den Link <STRONG>First Standard Edition-Server vorbereiten</STRONG> verwenden, um die anfänglichen Datenbankdateien auf dem neuen Standard Edition-Server zu installieren. Führen Sie diesen Vorgang <STRONG>nicht</STRONG> aus, wenn Sie einen Standard Edition-Server in einer vorhandenen lync Server 2013-Bereitstellung installieren.

    
    </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

