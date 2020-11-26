---
title: Voraussetzungen für Gruppenanruf-Pickup-Konfiguration und Benutzerrechte
description: Voraussetzungen für Gruppenanruf-Abholung und Benutzerrechte
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Group Call Pickup configuration prerequisites and user rights
ms:assetid: 8757b1d3-751d-49c3-b1b8-b678f663f18e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945641(v=OCS.15)
ms:contentKeyID: 51541495
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 74d2a758b7199634e14ee387d2554b30bf2ae8d3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427873"
---
# <a name="group-call-pickup-configuration-prerequisites-and-user-rights-in-lync-server-2013"></a>Voraussetzungen für Gruppenanruf-Pickup-Konfiguration und Benutzerrechte in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-01-30_

Bei der Gruppenanruf Abholung handelt es sich um ein Anruf Verwaltungsfeature, das standardmäßig bei der Bereitstellung von Enterprise-VoIP installiert wird. In diesem Thema wird beschrieben, was Sie benötigen, bevor Sie die Gruppenanruf Abholung und die Benutzerrechte konfigurieren können, die Sie zum Ausführen von Konfigurationsaufgaben benötigen.

In diesem Abschnitt wird davon ausgegangen, dass Sie die Planungsdokumentation gelesen haben, die sich auf die Gruppenanruf Abholung bezieht (siehe [Planen der Gruppenanruf Abholung in lync Server 2013](lync-server-2013-planning-for-group-call-pickup.md)).

<div>

## <a name="group-call-pickup-configuration-prerequisites"></a>Voraussetzungen für Gruppenanruf-Pickup-Konfiguration

Für die Gruppenanruf Abholung sind die folgenden Komponenten erforderlich:

  - Anwendungsdienst

  - Anwendung zum Parken von Anrufen

Diese Komponenten werden automatisch installiert, wenn Sie Enterprise-VoIP bereitstellen.

</div>

<div>

## <a name="group-call-pickup-configuration-user-rights"></a>Benutzerrechte für Gruppenanruf-Pickup-Konfiguration

Sie verwenden die folgenden Verwaltungstools, um die Gruppenanruf Abholung zu konfigurieren:

  - Lync Server-Verwaltungsshell

  - SEFAUtil Resource Kit-Tool

Verwenden Sie die lync Server-Verwaltungsshell zum Erstellen und Verwalten von Anruf-Abhol Gruppen in der Orbit-Tabelle des Anruf Parks. Verwenden Sie das SEFAUtil Resource Kit-Tool, um eine Anruf Abhol Gruppe zuzuweisen und die Gruppenanruf Abholung für Benutzer zu aktivieren oder die Gruppenanruf Abholung für Benutzer zu deaktivieren.

Die Konfiguration der Gruppenanruf Abholung erfordert je nach Aufgabe eine der folgenden Administratorrollen:

  - **CsVoiceAdministrator:** Diese Administratorrolle kann alle sprachbezogenen Einstellungen und Richtlinien erstellen, konfigurieren und verwalten.

  - **CsUserAdministrator:** Mit dieser Administratorrolle kann die Gruppenanruf Abholung für Benutzer aktiviert werden. Diese Administratorrolle verfügt auch über die schreibgeschützte Ansicht Zugriff auf alle Sprachkonfigurationen.

  - **CsServerAdministrator:** Diese Administratorrolle kann Server und Dienste verwalten, überwachen und Problembehandlung durchführen.

  - **CsAdministrator:** Diese Administratorrolle kann alle Aufgaben von CsVoiceAdministrator, CsServerAdministrator und CsUserAdministrator ausführen.

<div>


> [!NOTE]
> Details zu Administratorrechten finden Sie unter <A href="lync-server-2013-planning-for-role-based-access-control.md">Planen der rollenbasierten Zugriffssteuerung in lync Server 2013</A> in der Planungsdokumentation.



</div>

</div>

<div>

## <a name="see-also"></a>Siehe auch


[Bereitstellen von Enterprise-VoIP in lync Server 2013](lync-server-2013-deploying-enterprise-voice.md)  


[Planen der Anruf Verwaltungsfeatures in lync Server 2013](lync-server-2013-planning-for-call-management-features.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

