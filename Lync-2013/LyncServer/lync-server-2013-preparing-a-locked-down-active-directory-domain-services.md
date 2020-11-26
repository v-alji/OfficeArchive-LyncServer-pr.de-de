---
title: 'Lync Server 2013: Vorbereiten gesperrter Active Directory-Domänendienste'
description: 'Lync Server 2013: Vorbereiten einer gesperrten Active Directory-Domänendienste'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing a locked-down Active Directory Domain Services
ms:assetid: 68bde963-3fa3-4102-88d6-ac931c1dd2d7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398492(v=OCS.15)
ms:contentKeyID: 48184377
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4aea04b138de2630935713eda7cbef9e4d21572a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424226"
---
# <a name="preparing-a-locked-down-active-directory-domain-services-in-lync-server-2013"></a>Vorbereiten gesperrter Active Directory-Domänendienste in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-05-14_

Organisationen Sperren häufig Active Directory-Domänendienste, um Sicherheitsrisiken zu minimieren. Eine gesperrte Active Directory-Umgebung kann jedoch die von lync Server 2013 erforderlichen Berechtigungen einschränken. Das ordnungsgemäße Vorbereiten einer gesperrten Active Directory-Umgebung für lync Server 2013 umfasst einige zusätzliche Überlegungen und Schritte.

Es gibt zwei gängige Methoden, mit denen Berechtigungen in einer gesperrten Active Directory-Umgebung eingeschränkt sind:

  - Zugriffssteuerungseinträge (ACEs) für authentifizierte Benutzer werden aus Containern entfernt.

  - Die Vererbung von Berechtigungen ist für Container von Benutzer-, Kontakt-, InetOrgPerson-oder Computer Objekten deaktiviert.

<div>

## <a name="in-this-section"></a>In diesem Abschnitt

  - [Entfernte Berechtigungen für authentifizierte Benutzer in Lync Server 2013](lync-server-2013-authenticated-user-permissions-are-removed.md)

  - [Vererbung von Berechtigungen ist für Computer-, Benutzer- oder InetOrgPerson-Container deaktiviert in Lync Server 2013](lync-server-2013-permissions-inheritance-is-disabled-on-computers-users-or-inetorgperson-containers.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

