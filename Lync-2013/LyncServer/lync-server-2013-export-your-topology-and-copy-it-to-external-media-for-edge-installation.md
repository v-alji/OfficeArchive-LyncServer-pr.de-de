---
title: Exportieren der Topologie und Kopieren auf externe Medien zur Edgeinstallation
description: Exportieren Sie Ihre Topologie, und kopieren Sie Sie für die Edge-Installation auf externe Medien.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Export your topology and copy it to external media for edge installation
ms:assetid: def9f416-c519-4a72-b242-7d3057d9c1fd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398983(v=OCS.15)
ms:contentKeyID: 48185615
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 47fcee032b4c0e667455ae7f35afe8b99c2d12cc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393782"
---
# <a name="export-your-lync-server-2013-topology-and-copy-it-to-external-media-for-edge-installation"></a>Exportieren der Lync Server 2013-Topologie und Kopieren auf externe Medien zur Edgeinstallation

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-08_

Nachdem Sie Ihre Topologie veröffentlicht haben, benötigt der lync Server-Bereitstellungs-Assistent Zugriff auf die Daten des zentralen Verwaltungsspeichers, um den Bereitstellungsprozess auf dem Server zu starten. Im internen Netzwerk stehen die Daten direkt von den Servern zur Verfügung, aber Edgeserver, die nicht zur internen Domäne gehören, können nicht auf die Daten zugreifen. Damit die Topologie-Konfigurationsdaten für eine Edge-Server-Bereitstellung zur Verfügung stehen, müssen Sie die Topologiedaten in eine Datei exportieren und auf externe Medien (beispielsweise ein USB-Laufwerk oder eine Netzwerkfreigabe, die vom Edgeserver verfügbar ist) kopieren, bevor Sie den lync Server-Bereitstellungs-Assistenten auf dem Edgeserver ausführen. Gehen Sie wie folgt vor, um Ihre Topologie-Konfigurationsdaten auf dem von Ihnen bereitgestellten Edgeserver zur Verfügung zu stellen.

<div>


> [!NOTE]
> Nachdem Sie lync Server 2013 auf einem Edgeserver installiert haben, können Sie den Edgeserver mithilfe der Verwaltungstools im internen Netzwerk verwalten, die die Konfiguration automatisch auf alle Edgeserver in Ihrer Bereitstellung replizieren. Die einzige Ausnahme ist das zuweisen und Installieren von Zertifikaten sowie das Beenden und starten von Diensten, die beide auf dem Edgeserver ausgeführt werden müssen.



</div>

<div>

## <a name="to-make-your-topology-data-available-on-an-edge-server-by-using-lync-server-management-shell"></a>So stellen Sie Ihre Topologiedaten mithilfe der lync Server-Verwaltungsshell auf einem Edgeserver zur Verfügung

1.  Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.

2.  Führen Sie in der lync Server-Verwaltungsshell das folgende Cmdlet aus:
    
        Export-CsConfiguration -FileName <ConfigurationFilePath.zip>

3.  Kopieren Sie die exportierte Datei auf externe Medien (beispielsweise ein USB-Laufwerk oder eine Netzwerkfreigabe, die während der Bereitstellung vom Edgeserver verfügbar ist).

</div>

</div>

<span> </span>

</div>

</div>

</div>

