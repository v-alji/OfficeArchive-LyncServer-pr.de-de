---
title: 'Lync Server 2013: von der Gruppenanruf Abholung verwendete Komponenten'
description: 'Lync Server 2013: von der Gruppenanruf Abholung verwendete Komponenten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Group Call Pickup
ms:assetid: 45db2f23-d486-4b20-a8cf-7b48a1f9fd3a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945625(v=OCS.15)
ms:contentKeyID: 51541470
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 517f75dcbac8bfed0e749c061a9696b7667e10ed
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394210"
---
# <a name="components-used-by-group-call-pickup-in-lync-server-2013"></a>Von der Gruppenanruf Abholung in lync Server 2013 verwendete Komponenten

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-01-30_

Die Gruppenanruf Abholung wird automatisch bereitgestellt, wenn Sie Enterprise-VoIP und die Anwendung für den Anruf Park bereitstellen. Sie aktivieren die Abholung von Gruppen anrufen, indem Sie die Umlaufbahn Tabelle des Anruf Parks mit getrennten Nummernbereichen konfigurieren, die als Gruppennummern für die Anruf Abholung bestimmt sind, und dann durch Zuweisen von Benutzern zum Anrufen von Abhol Gruppen und zum Aktivieren der Gruppenanruf Abholung. Die folgenden lync Server-Komponenten unterstützen die Gruppenanruf Abholung:

  - **Anwendungsdienst**   Der Anwendungsdienst stellt eine Plattform zum Bereitstellen, hosten und Verwalten von Unified Communications-Anwendungen bereit, beispielsweise die Anwendung für den Parken von anrufen. Der Anwendungsdienst wird auf jedem Front-End-Server in einem Front-End-Pool und auf jedem Standard Edition-Server automatisch installiert.

  - **Anruf parken-Anwendung**   Die Anwendung "Parken" ist eine der Unified Communications-Anwendungen, die vom Anwendungsdienst gehostet werden. Die Abholung von Gruppen anrufen basiert auf der Anwendung "Parken".

  - **Lync Server-Verwaltungsshell**   Sie verwenden die lync Server-Verwaltungsshell zum Verwalten von Gruppenanruf-pickupgruppen.

  - **SEFAUtil Resource Kit-Tool**   Sie verwenden das Feature-Aktivierungs Dienstprogramm für sekundäre Erweiterungen (SEFAUtil), um Benutzer einer Anruf Abhol Gruppe zuzuweisen und die Anruf Abholung für Benutzer zu aktivieren oder zu deaktivieren.

</div>

<span> </span>

</div>

</div>

</div>

