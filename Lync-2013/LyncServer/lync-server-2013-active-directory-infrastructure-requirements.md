---
title: 'Lync Server 2013: Active Directory-Infrastrukturanforderungen'
description: 'Lync Server 2013: Anforderungen an die Active Directory-Infrastruktur.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Active Directory infrastructure requirements
ms:assetid: c2086f7b-662f-4179-ab99-2c0311ebd903
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412955(v=OCS.15)
ms:contentKeyID: 48185318
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 62218605c9b3fac20743d0b6bb475515c9498f9a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439415"
---
# <a name="active-directory-infrastructure-requirements-for-lync-server-2013"></a>Active Directory-Infrastrukturanforderungen für Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-11-07_

Bevor Sie mit dem Vorbereiten der Active Directory-Domänendienste für lync Server 2013 beginnen, stellen Sie sicher, dass Ihre Active Directory-Infrastruktur die folgenden Voraussetzungen erfüllt:

  - Alle Domänencontroller (einschließlich aller globalen Katalogserver) in der Gesamtstruktur, in der Sie lync Server bereitstellen, führen eines der folgenden Betriebssysteme aus:
    
      - Windows Server 2012 R2-Betriebssystem
    
      - Betriebssystem Windows Server 2012
    
      - Windows Server 2008 R2-Betriebssystem
    
      - Windows Server 2008-Betriebssystem
    
      - Windows Server 2008 Enterprise 32-Bit
    
      - 32-Bit-oder 64-Bit-Versionen des Windows Server 2003 R2-Betriebssystems
    
      - 32-Bit-oder 64-Bit-Versionen des Windows Server 2003-Betriebssystems

  - Alle Domänen, in denen Sie lync Server bereitstellen, werden auf eine Domänenfunktionsebene von Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 oder mindestens Windows Server 2003 heraufgestuft.

  - Die Gesamtstruktur, in der Sie lync Server bereitstellen, wird auf eine Gesamtstrukturfunktionsebene von Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 oder mindestens Windows Server 2003 heraufgestuft.
    
    <div>
    

    > [!NOTE]  
    > Informationen zum Ändern ihrer Domänen-oder Gesamtstrukturfunktionsebene finden Sie unter "Heraufstufen von Domänen-und Gesamtstrukturfunktionsebenen" in der TechNet-Bibliothek unter <A href="https://go.microsoft.com/fwlink/p/?linkid=263775">https://go.microsoft.com/fwlink/p/?LinkId=263775</A> .

    
    </div>

  - Ein globaler Katalog wird in jeder Domäne bereitgestellt, in der Sie lync Server-Computer oder-Benutzer bereitstellen.

Lync Server 2013 unterstützt die universellen Gruppen in den Betriebssystemen Windows Server 2012 R2, Windows Server 2012, Windows Server 2008 R2, Windows Server 2008 und Windows Server 2003. Mitglieder universeller Gruppen können andere Gruppen und Konten aus beliebigen Domänen in der Domänen- oder Gesamtstruktur umfassen und über Berechtigungen für beliebige Domänen in der Domänen- oder Gesamtstruktur verfügen. Die Unterstützung für universelle Gruppen in Verbindung mit der Administrator Delegierung vereinfacht die Verwaltung einer lync Server-Bereitstellung. Beispielsweise ist es nicht erforderlich, eine Domäne einer anderen hinzuzufügen, um einem Administrator die Verwaltung beider Domänen zu ermöglichen.

</div>

<span> </span>

</div>

</div>

</div>

