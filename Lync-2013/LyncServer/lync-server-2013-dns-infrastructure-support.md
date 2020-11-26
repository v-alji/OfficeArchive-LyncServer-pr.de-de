---
title: 'Lync Server 2013: DNS-Infrastrukturunterstützung'
description: 'Lync Server 2013: Unterstützung für DNS-Infrastruktur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Domain Name System (DNS) infrastructure support
ms:assetid: 37777c16-94ce-436d-b517-bcf53a564513
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425850(v=OCS.15)
ms:contentKeyID: 48183878
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea65907eba13367fd92e546d62994d10907bf89
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429077"
---
# <a name="dns-infrastructure-support-in-lync-server-2013"></a>DNS-Infrastrukturunterstützung in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-03-08_

Lync Server 2013 erfordert DNS (Domain Name System) und verwendet es wie folgt:

  - Ermitteln interner Server oder Pools für die Server-zu-Server-Kommunikation.

  - Damit Clients den Front-End-Pool oder Standard Edition-Server ermitteln können, der für verschiedene SIP-Transaktionen verwendet wird.

  - Zuordnen der einfachen URLs für Konferenzen zu den Servern, die diese Konferenzen hosten

  - So aktivieren Sie externe Server und Clients zum Herstellen einer Verbindung mit Edgeserver oder dem HTTP-Reverseproxy für Instant Messaging (im) oder Konferenzen

  - Wenn Sie Unified Communications (UC)-Geräte aktivieren möchten, die nicht angemeldet sind, um den Front-End-Pool oder den Standard Edition-Server mit dem Geräte Update-Webdienst zu entdecken, beziehen Sie Updates, und senden Sie Protokolle.

  - Damit Mobile Clients automatisch Webdienste-Ressourcen ermitteln können, ohne dass die Benutzer URLs in den Geräteeinstellungen manuell eingeben müssen.

  - Für den DNS-Lastenausgleich.

<div>


> [!NOTE]  
> Lync Server 2013 unterstützt keine Internationalisierungs Domänennamen (IDNs).



</div>

<div>


> [!IMPORTANT]  
> Der angegebene Name muss mit dem auf dem Server konfigurierten Computernamen übereinstimmen. Der Name eines Computers, der nicht Mitglied einer Domäne ist, ist standardmäßig kein FQDN, sondern ein Kurzname. Der Topologie-Generator verwendet keine Kurznamen, sondern FQDNs. Daher müssen Sie ein DNS-Suffix für den Namen des Computers konfigurieren, der als Edgeserver bereitgestellt werden soll und nicht Mitglied einer Domäne ist. <STRONG>Verwenden Sie nur Standardzeichen</STRONG> (also A – Z, a – z, 0 – 9 und Bindestriche) beim Zuweisen von FQDNs der Server mit Lync Server, Edgeserver und Pools. Verwenden Sie keine Unicode-Zeichen oder Unterstriche. Andere als die genannten Zeichen in einem FQDN werden von externen DNS und öffentlichen Zertifizierungsstellen (wenn der FQDN dem SN im Zertifikat zugewiesen werden muss) häufig nicht unterstützt.



</div>

</div>

<span> </span>

</div>

</div>

</div>

