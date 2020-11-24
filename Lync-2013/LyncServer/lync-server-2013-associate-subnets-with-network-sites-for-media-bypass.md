---
title: 'Lync Server 2013: Zuordnen von Subnetzen zu Netzwerk Websites für die medienumgehung'
description: 'Lync Server 2013: Zuordnen von Subnetzen zu Netzwerk Websites für die medienumgehung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Associate subnets with network sites for media bypass
ms:assetid: 5bc632b7-1446-470f-b332-48ea0ca4d1fd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398401(v=OCS.15)
ms:contentKeyID: 48184244
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ee03b51d29a88ff634cb87385c5889c35acd8884
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395163"
---
# <a name="associate-subnets-with-network-sites-for-media-bypass-in-lync-server-2013"></a>Zuordnen von Subnetzen zu Netzwerk Websites zur medienumgehung in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-12_

<div>


> [!NOTE]  
> In diesem Thema wird davon ausgegangen, dass Sie die globalen Einstellungen für die medienumgehung konfiguriert haben und dass Sie die netzwerkregion und Netzwerk Websites für die medienumgehung konfiguriert haben.



</div>

Jedes Subnetz in Ihrem Netzwerk muss einer bestimmten Netzwerk Website zugeordnet sein. Dies liegt daran, dass die Netzwerk Website, auf der sich ein Endpunkt befindet, mithilfe von Subnetinformationen ermittelt wird. Wenn die Speicherorte beider Parteien in einer Sitzung bekannt sind, kann die medienumgehung bestimmen, wohin Medien zur Verarbeitung gesendet werden sollen.

Die medienumgehung hat keine besonderen Anforderungen für das Zuordnen von Subnetzen zu Netzwerkstandorten. Wenn Sie eine Zuordnung zwischen den Subnetzen und Netzwerkstandorten in Ihrer Topologie erstellen möchten, führen Sie die Verfahren unter Zuordnen eines Subnetzes [zu einer Netzwerk Website in lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md)aus.

<div>

## <a name="next-steps-create-bandwidth-policy-profiles"></a>Nächste Schritte: Erstellen von Bandbreitenrichtlinien Profilen

Nachdem Sie Subnetze mit Netzwerk Websites für die medienumgehung verknüpft haben, müssen Sie mindestens ein bandbreitenrichtlinienprofil erstellen, mit dem Subnetze in Personen mit guter Konnektivität und ohne zum Zweck der medienumgehung partitioniert werden. Alle Subnetze in einem Netzwerkbereich mit Netzwerk Websites, die keine Bandbreiteneinschränkungen aufweisen, verfügen über eine gute Konnektivität, und daher können diese Subnetze die medienumgehung verwenden.

Verfahren zum Konfigurieren von Profilen für Bandbreitenrichtlinien finden Sie unter [Erstellen von Bandbreitenrichtlinien Profilen in lync Server 2013](lync-server-2013-create-bandwidth-policy-profiles.md).

</div>

</div>

<span> </span>

</div>

</div>

</div>

