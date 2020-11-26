---
title: 'Lync Server 2013: Voraussetzungen zur Aktivierung der Kerberos-Authentifizierung'
description: 'Lync Server 2013: Voraussetzungen für die Aktivierung der Kerberos-Authentifizierung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Prerequisites for enabling Kerberos authentication
ms:assetid: 3f276a21-7476-4bc0-9fd1-59e844d2e9c1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425909(v=OCS.15)
ms:contentKeyID: 48183945
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 65a45bad0eb249fdbc717fe05f080ce737c87c6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436972"
---
# <a name="prerequisites-for-enabling-kerberos-authentication-in-lync-server-2013"></a>Voraussetzungen zur Aktivierung der Kerberos-Authentifizierung in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-02-21_

Bevor Sie die Kerberos-Authentifizierung aktivieren, stellen Sie sicher, dass Sie alle erforderlichen Konfigurations-und Infrastruktur Vorbereitungen durchführen:

  - Das Active Directory-Schema wird für lync Server 2013 erweitert.

  - Die Active Directory-Gesamtstrukturvorbereitung ist für lync Server 2013 abgeschlossen.

  - Die Active Directory-Domänenvorbereitung ist für lync Server 2013 abgeschlossen.

  - Der zentrale Verwaltungsspeicher wurde erfolgreich installiert und verfügbar.

  - Die Topologie wurde mithilfe des Topologie-Generators erstellt und veröffentlicht.

  - Server und Rollen, die Webdienste erfordern, wurden definiert und bereitgestellt, einschließlich der Front-End-Server, der Standard Edition-Server und der Directors.

  - Internet Informationsdienste (IIS) wird mit den empfohlenen Rollendiensten für die Unterstützung von Webdiensten in lync Server 2013 konfiguriert und bereitgestellt.

Nachdem die Voraussetzungen erfüllt wurden, sollten Sie bereit sein, mindestens ein Konto für Webdienste zu erstellen, das für die Kerberos-Authentifizierung für Ihre Bereitstellung verwendet werden soll. Sie müssen mindestens ein Kerberos-Authentifizierungs Konto für jede Bereitstellung erstellen. Sie können jedoch für jede Website ein Konto erstellen, um die lokale Kerberos-Authentifizierung auf der Website bereitzustellen. Sie können nur ein Kerberos-Authentifizierungs Konto pro Website angeben.

</div>

<span> </span>

</div>

</div>

</div>

