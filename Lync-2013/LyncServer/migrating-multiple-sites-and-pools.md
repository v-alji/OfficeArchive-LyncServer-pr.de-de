---
title: Migrieren von mehreren Standorten und Pools
description: Migrieren mehrerer Websites und Pools
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrating multiple sites and pools
ms:assetid: a6d726d2-564d-4b39-a97c-5656a673292a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205165(v=OCS.15)
ms:contentKeyID: 48185079
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7efaa6f038286ff9138e631f23da88bb445e20f1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440374"
---
# <a name="migrating-multiple-sites-and-pools"></a>Migrieren von mehreren Standorten und Pools

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-17_

Lync Server 2013 unterstützt die Bereitstellung mehrerer Standorte und mehrerer Pools. Der Vorgang zum Migrieren mehrerer Pools von lync Server 2010 zu lync Server 2013 erfordert die folgenden Überlegungen:

1.  Nach der Bereitstellungeines lync Server 2013-pilotpools müssen Sie eine Teilmenge der Pilotbenutzer definieren, die in den lync Server 2013-Pool verschoben werden, und eine Methode zum Überprüfen der Funktionalität der Benutzer. Wenn Sie beispielsweise einen Benutzer in den Pilot Pool verschieben, überprüfen Sie, ob die konferenzrichtlinie des Benutzers nach lync Server 2013 verschoben wurde.

2.  Nachdem Sie einen Edgeserver im Pilot Pool bereitgestellt haben, müssen Sie überprüfen, ob externe Benutzer mit dem lync Server 2013-Pool kommunizieren können.

3.  Nachdem Sie die Verbund Routen von lync Server 2010-Edgeserver auf die Pilot-Edgeserver von lync Server 2013 umgestellt haben, müssen Sie überprüfen, ob Verbundbenutzer mit dem lync Server 2013-Pool kommunizieren können.

4.  Nachdem Sie alle Benutzer und nicht-Benutzer-Kontaktobjekte verschoben haben, müssen Sie überprüfen, ob der lync Server 2010-Pool leer ist.

5.  Nachdem Sie überprüft haben, dass der lync Server 2010-Pool leer ist, können Sie den Pool deaktivieren.
    
    Details zum Deaktivieren des Legacy-lync Server 2010-Pools und-Servers finden Sie unter [Phase 8: Legacy-Pools der decommission-Version](phase-8-decommission-legacy-pools.md).

</div>

<span> </span>

</div>

</div>

</div>

