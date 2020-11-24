---
title: 'Lync Server 2013: Überlegungen zu Migration und Koexistenz für IPv6'
description: 'Lync Server 2013: Überlegungen zur Migration und Koexistenz für IPv6.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration and coexistence considerations for IPv6
ms:assetid: 8c769c4f-c8a9-4cbf-9080-beee3be9848a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205068(v=OCS.15)
ms:contentKeyID: 48184751
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e8618cc14ff3c2467ea41df34e39f5094d1206dc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394986"
---
# <a name="migration-and-coexistence-considerations-for-ipv6-in-lync-server-2013"></a>Überlegungen zu Migration und Koexistenz für IPv6 in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-06-14_

IP Version 6 (IPv6) wird in lync Server 2010 oder Office Communications Server nicht unterstützt. Für Pilot Zwecke können Sie die Koexistenz von lync Server 2010 und lync Server 2013 mit zwei Stapeln testen. Es wird empfohlen, alle Pools für einen bestimmten zentralen Standort auf lync Server 2013 zu aktualisieren, bevor Sie IPv6 (Dual-Stack-Netzwerk) für einen der Pools aktivieren. Wenn Sie einen Pool nur für IPv6 konfigurieren müssen, wird empfohlen, dass Sie einen Nur-IPv6-Pool in Ihrer Testumgebung zum Testen einrichten.

Die folgenden Szenarien werden bei der Migration und Koexistenz unterstützt:

  - Lync Server 2013, lync Server 2010 und Office Communications Server 2007 R2-Pools im IPv4-Modus, die mit lync Server 2013 im Dual-Stack-Modus nebeneinander vorhanden sind.

  - Lync Server 2013-Pool im reinen IPv6-Modus, wenn der nur-IPv6-Pool isoliert ist.

</div>

<span> </span>

</div>

</div>

</div>

