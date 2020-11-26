---
title: Überprüfen des Partnerverbunds und des Remotezugriffs für externe Benutzer
description: Überprüfen Sie den Verbund und den Remotezugriff für externe Benutzer.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify federation and remote access for external users
ms:assetid: a383fefb-c428-4462-93fd-15ba540fa867
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688163(v=OCS.15)
ms:contentKeyID: 49733768
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ac36f2e1b6c5ddfd889810ba2a3ab4d82b7ae33
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446472"
---
# <a name="verify-federation-and-remote-access-for-external-users"></a>Überprüfen des Partnerverbunds und des Remotezugriffs für externe Benutzer

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-18_

Nach dem Übergang der Föderations Route zum lync Server 2013-Edgeserver sollten Sie einige Funktionstests durchführen, um zu überprüfen, ob der Verbund wie erwartet funktioniert. Tests für den Zugriff durch externe Benutzer sollten alle externen Benutzertypen enthalten, die von Ihrer Organisation unterstützt werden, einschließlich der folgenden:

<div>

## <a name="test-connectivity-of-external-users-and-external-access"></a>Testen der Konnektivität externer Benutzer und des externen Zugriffs

  - Benutzer aus mindestens einer Verbunddomäne, einem internen Benutzer in lync Server 2013 und einem Benutzer in lync Server 2010 Testen Sie Instant Messaging (im), Anwesenheitsinformationen, Audio/Video (A/V) und Desktopfreigabe.

  - Benutzer jedes öffentlichen Chat Dienstanbieters, die von Ihrer Organisation unterstützt werden (und für die Bereitstellung abgeschlossen wurde), die mit einem Benutzer in lync Server 2013 und einem Benutzer in lync Server 2010 kommunizieren.

  - Überprüfen Sie, ob anonyme Benutzer an Konferenzen teilnehmen können.

  - Ein Benutzer, der auf lync Server 2010 mithilfe des Remotebenutzerzugriffs (Anmeldung bei lync Server 2010 von außerhalb des Intranets, aber ohne VPN) mit einem Benutzer in lync Server 2013 und einem Benutzer in lync Server 2010 gehostet wird. Testen Sie Chat, Anwesenheit, A/V und Desktopfreigabe.

  - Ein Benutzer, der auf lync Server 2013 mithilfe des Remotebenutzerzugriffs (Anmeldung bei lync Server 2013 von außerhalb des Intranets, aber ohne VPN) mit einem Benutzer in lync Server 2013 und einem Benutzer in lync Server 2010 gehostet wird. Testen Sie Chat, Anwesenheit, A/V und Desktopfreigabe.

</div>

</div>

<span> </span>

</div>

</div>

</div>

