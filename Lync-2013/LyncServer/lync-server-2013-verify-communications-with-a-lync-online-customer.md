---
title: 'Lync Server 2013: Überprüfen der Kommunikation mit einem lync Online-Kunden'
description: 'Lync Server 2013: Überprüfen Sie die Kommunikation mit einem lync Online-Kunden.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify communications with a Lync Online customer
ms:assetid: c8287b15-e1bb-4b26-8354-0ec90b2fcfe7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202189(v=OCS.15)
ms:contentKeyID: 48185378
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 867b0f7ffffd563c869b9bcd5443a3cb91b156af
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395062"
---
# <a name="verify-communications-with-a-lync-online-customer-in-lync-server-2013"></a>Überprüfen der Kommunikation mit einem lync Online-Kunden in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-08_

Damit lync-Benutzer in Ihrer Organisation mit Benutzern eines Microsoft lync Online 2010-Kunden kommunizieren können, müssen Sie die folgenden Schritte ausgeführt haben:

  - Alle Voraussetzungen erfüllt. Dies umfasst die Bereitstellung von internen und Edge-Servern, das Aktivieren der Föderations Unterstützung für Ihre Organisation und das Einrichten von Benutzerkonten. Ausführliche Informationen finden Sie unter [Voraussetzungen für die Föderation mit einem lync Online-Kunden in lync Server 2013](lync-server-2013-prerequisites-for-federating-with-a-lync-online-customer.md).

  - Konfigurierte Unterstützung für den Domänenzugriff in ihrer internen Bereitstellung. Dies umfasst das Erstellen eines Hostanbieter Eintrags und das Konfigurieren Ihrer Bereitstellung, um den Zugriff aus der Domäne des lync Online-Kunden zu ermöglichen. Ausführliche Informationen finden Sie unter [Konfigurieren der Verbundunterstützung für eine lync Online-Domäne in lync Server 2013](lync-server-2013-configure-federation-support-for-a-lync-online-domain.md).

  - Ihre Benutzerkonten wurden für die Unterstützung der Föderation konfiguriert. Ausführliche Informationen finden Sie unter [Konfigurieren des Benutzerzugriffs für den Verbund mit einem lync Online-Kunden in lync Server 2013](lync-server-2013-configure-user-access-for-federation-with-a-lync-online-customer.md).

Nachdem Sie alle diese Schritte ausgeführt haben und der Administrator des lync Online 2010-Kunden die gesamte Konfiguration seiner Onlinedienste abgeschlossen hat, um den Verbund mit Ihrer Organisation zu unterstützen, überprüfen Sie die Kommunikation, indem Sie die Kommunikation zwischen einem internen Benutzer in Ihrer Organisation und einem Benutzer des lync Online-Kunden testen. Wenn die Kommunikation nicht erfolgreich ist, können Sie mithilfe des Protokollierungstools Ihres Edge-Servers Protokoll-und Ablaufverfolgungsdateien aufzeichnen, um das Problem zu beheben. Ausführliche Informationen zur Verwendung des Protokollierungstools finden Sie unter [Öffnen der lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md) in der Betriebsdokumentation. Details zum Protokollierungstool finden Sie in der Dokumentation zum Protokollierungstool für lync Server 2010 in der TechNet-Bibliothek unter [https://go.microsoft.com/fwlink/p/?linkId=199265](https://go.microsoft.com/fwlink/p/?linkid=199265) .

</div>

<span> </span>

</div>

</div>

</div>

