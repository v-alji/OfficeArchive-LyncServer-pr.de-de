---
title: 'Lync Server 2013: Ausführen eines Failbacks für einen Pool'
description: 'Lync Server 2013: Fehler beim Zurücksetzen eines Pools.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing back a pool
ms:assetid: 6232b644-ef57-4c9c-abec-14ff8ffc9fe7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204945(v=OCS.15)
ms:contentKeyID: 48184289
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1c1fc0ea4514d2f951dd936521590d47b809db38
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428328"
---
# <a name="failing-back-a-pool-in-lync-server-2013"></a>Ausführen eines Failbacks für einen Pool in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-11-01_

Nachdem der Pool, der das Desaster erlebt hat, wieder online ist (also pool1 in diesem Beispiel), führen Sie die folgenden Schritte aus, um die Bereitstellung auf normalen Arbeitsstatus wiederherzustellen.

Beachten Sie, dass der Failback-Vorgang mehrere Minuten in Anspruch nimmt.  Zur Orientierung: Erwartungsgemäß dauert dies bei einem Pool mit 20.000 Benutzern bis zu 60 Minuten.

1.  Führen Sie einen Failback für die Benutzer durch, die sich ursprünglich in pool1 begeben haben, und Sie haben ein Failover auf Pool2 durchgeführt, indem Sie das folgende Cmdlet eingegeben haben:
    
        Invoke-CsPoolFailback -PoolFQDN <Pool1 FQDN> -Verbose

Es sind keine weiteren Schritte erforderlich. Wenn Sie einen Fehler über den zentralen Verwaltungs Server ausgeführt haben, können Sie ihn in Pool2 belassen.

</div>

<span> </span>

</div>

</div>

</div>

