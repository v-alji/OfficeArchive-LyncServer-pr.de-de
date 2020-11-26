---
title: 'Lync Server 2013: Neue Funktionen für die Archivierung'
description: 'Lync Server 2013: neue Archivierungs Features'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: New Archiving features
ms:assetid: c002e367-41ad-498d-9d23-8b117ac435b2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205225(v=OCS.15)
ms:contentKeyID: 48185288
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b5b69c90e62914284f178ae328375c6e350f5b3e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425163"
---
# <a name="new-archiving-features-in-lync-server-2013"></a>Neue Funktionen für die Archivierung in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-09_

Bei der Archivierung in lync Server 2013 können die folgenden Arten von Inhalten archiviert werden:

  - Peer-zu-Peer-Chatnachrichten

  - Konferenzen (Besprechungen), die mehr Parteien-Sofortnachrichten sind

  - Konferenzinhalte, einschließlich hochgeladener Inhalte (z. B. Handzettel) sowie ereignisbezogener Inhalte (z. B. Beitritt zu/Verlassen einer Konferenz, Hochladen/Freigeben von Inhalten oder Änderungen in der Sichtbarkeit)

Darüber hinaus bietet die Archivierung in lync Server 2013 neue Funktionen, die die Bereitstellung und die Effizienz des Betriebs verbessern. Diese neuen Features bestehen aus:

  - **Übersetzung der Archivierung auf Front-End-Servern.**   Lync Server 2013 verfügt nicht über eine separate Archivierungs Server Rolle. Die Archivierung ist ein optionales Feature, das auf allen Front-End-Servern in einer Enterprise Edition-Bereitstellung und auf Standard Edition-Servern zur Verfügung steht, die für einen Pool oder eine Website konfiguriert werden können.

  - **Integration von Microsoft Exchange.**   Wenn Sie die Archivierung bereitstellen, können Sie den Datenspeicher für die Archivierung mit Ihrem vorhandenen Exchange 2013-Speicher für alle Benutzer integrieren, die sich in Exchange 2013 befinden und deren Postfächer In-Place halten, sodass Sie keine separaten SQL Server-Datenbanken zum Archivieren von lync-Daten bereitstellen müssen. Wenn Sie keine Exchange 2013-Bereitstellung haben, oder wenn Sie es vorziehen, Sie nicht zu integrieren, oder wenn Sie lync 2013-Benutzer haben, die sich nicht in Exchange 2013 befinden und ihre Postfächer in In-Place halten, können Sie separate Archivierungsdatenbanken bereitstellen, indem Sie SQL Server verwenden, um archivierte Daten aus lync Communications zu speichern. Sie können sowohl die Microsoft Exchange-Integration als auch die lync Server 2013-Archivierungsdatenbanken verwenden, wenn Sie die Microsoft Exchange-Integration für einige, aber nicht für alle Benutzer in Ihrer Bereitstellung verwenden möchten. Details zu In-Place Haltebereich finden Sie unter "in-situ-Speicher" unter [https://go.microsoft.com/fwlink/p/?LinkId=267500](https://go.microsoft.com/fwlink/p/?linkid=267500) .

  - **SQL Store-Spiegelung.**   Wenn Sie die Archivierung bereitstellen, können Sie die SQL Server-Datenbankspiegelung für Ihre Archivierungsdatenbank aktivieren.

  - **Archivierung von Whiteboards und Umfragen.**   Archivierte Konferenzinhalte enthalten nun Whiteboards und Umfragen, die während der Besprechung freigegeben werden.

Die folgenden Inhaltstypen werden nicht archiviert:

  - Peer-to-Peer-Dateiübertragungen

  - Audio-/Videoinhalte für Peer-zu-Peer-Chatnachrichten und -konferenzen

  - Anwendungsfreigabe für Peer-to-Peer-Sofortnachrichten und-Konferenzen

<div>

## <a name="see-also"></a>Siehe auch


[Planen der Archivierung in Lync Server 2013](lync-server-2013-planning-for-archiving.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

