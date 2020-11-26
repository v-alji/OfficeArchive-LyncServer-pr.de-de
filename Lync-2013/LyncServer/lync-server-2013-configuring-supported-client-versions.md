---
title: 'Lync Server 2013: Konfigurieren unterstützter Clientversionen'
description: 'Lync Server 2013: Konfigurieren unterstützter Clientversionen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring supported client versions
ms:assetid: aebf7b48-9aa2-4a06-adc5-0c9d11b6358d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412832(v=OCS.15)
ms:contentKeyID: 48185137
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 74396314cae864fae134531b71375c750be8d3da
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432597"
---
# <a name="configuring-supported-client-versions-in-lync-server-2013"></a>Konfigurieren von unterstützten Clientversionen in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-12-14_

In lync Server 2013 können Sie clientversionsrichtlinien einrichten, um die Versionen der Clients anzugeben, die in Ihrer Umgebung unterstützt werden. Darüber hinaus können Sie die globale Client Versions Konfiguration verwenden, um eine Standardaktion für Clients anzugeben, für die noch keine Versionsrichtlinie definiert ist und daher nicht explizit unterstützt oder eingeschränkt wird.

Sie können auch clientversionsrichtlinien verwenden, um Clientupdates zu verwalten. Wenn Sie eine clientversionsrichtlinie festlegen und die Optionen **zulassen und aktualisieren** sowie **blockieren und aktualisieren** verwenden, erhalten Clients aktualisierte Software vom Windows Server Update-Dienst (wenn Sie diesen Dienst verwenden) oder von Microsoft Update.

<div>

## <a name="client-version-policy-settings"></a>Client Versionsrichtlinien Einstellungen

Die standardmäßige clientversionsrichtlinie setzt voraus, dass alle Clients lync ausführen. Wenn Clients in Ihrer Umgebung frühere Versionen von Communicator ausführen, müssen Sie möglicherweise die Client Versionsregeln neu konfigurieren, um zu verhindern, dass Clients und Geräte beim Herstellen einer Verbindung mit lync Server 2013 unerwartet blockiert oder aktualisiert werden. Sie können die Standardregel ändern, oder Sie können eine höhere Regel in der Liste der Client Versionsrichtlinien hinzufügen, um die Standardregel zu überschreiben. Darüber hinaus sollten Sie die Client Versionsrichtlinie so konfigurieren, dass die neuesten Updates erforderlich sind, da kumulative Updates (CUS) freigegeben werden. Ausführliche Informationen finden Sie unter [angeben der Clientanwendungen, die für die Anmeldung bei lync Server 2013](lync-server-2013-specifying-the-client-applications-that-can-be-used-to-log-on-to-lync-server-2013.md) in der Betriebsdokumentation verwendet werden können.

</div>

</div>

<span> </span>

</div>

</div>

</div>

