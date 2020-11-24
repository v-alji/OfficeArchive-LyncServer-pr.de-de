---
title: 'Lync Server 2013: Konfigurieren von Clients für die Verwendung mit Office Web Apps Server'
description: 'Lync Server 2013: Konfigurieren von Clients für die Verwendung mit Office Web Apps Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring clients for use with Office Web Apps Server
ms:assetid: e5eaead7-0b32-42fb-97eb-ca203af59a9d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205339(v=OCS.15)
ms:contentKeyID: 48185668
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b9bd7cf1e76c481c40381234ba1a84cda5500dc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395110"
---
# <a name="configuring-clients-of-lync-server-2013-for-use-with-office-web-apps-server"></a>Konfigurieren von Clients von lync Server 2013 zur Verwendung mit Office Web Apps Server

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-02-25_

Wenn Sie möchten, dass Benutzer die vollständigen Funktionen von Office Web App Server erfahren, sollten Sie diese Benutzer auf Microsoft lync 2013 aktualisieren. nur Benutzer von lync 2013 sind in der Lage, in PowerPoint-Folien unabhängig von der tatsächlichen PowerPoint-Präsentation zu scrollen. (Dies bedeutet, dass diese Benutzer jederzeit auf jede Folie in der Präsentation zugreifen können, ohne die tatsächliche Präsentation in irgendeiner Weise zu beeinträchtigen.) Benutzer, die nicht lync 2013 verwenden, können weiterhin an Online Konferenzen teilnehmen und die PowerPoint-Präsentation anzeigen. Sie können jedoch nicht unabhängig voneinander durch die Folien scrollen, und Sie können auch keine Folienübergänge sehen oder eingebettete Videos anzeigen.

Beachten Sie, dass diese Funktionen den Benutzern von lync 2013 immer zur Verfügung stehen. Dies gilt auch, wenn der PowerPoint-Referent Microsoft lync 2010 ausführt. Wenn eine PowerPoint-Präsentation von einem Benutzer gehostet wird, der lync 2010 ausführt, wird lync Server 2013 mit Office Web Apps Server koordiniert, um sicherzustellen, dass lync 2013-Benutzer die Office Web Apps-Server Version dieser Präsentation anzeigen. Office Web Apps Server bietet keine PowerPoint-Dienste für Benutzer mit anderen Clients als lync 2013. Stattdessen stellen diese Benutzer eine Verbindung mit dem Konferenzserver Dienst her und zeigen PowerPoint-Präsentationen auf die gleiche Weise an wie in Microsoft lync Server 2010. Dies bedeutet auch, dass diese Benutzer nur Zugriff auf die mehr-begrenzte Funktionen haben, die von lync Server 2010 angeboten werden.

Obwohl für Office Web Apps Server keine Clientkonfiguration erforderlich ist (außer beim Upgrade von Benutzern auf lync 2013), sollten Konferenzteilnehmer auf Internet Explorer 9 aktualisieren. Obwohl auf Konferenzen über Internet Explorer 8 zugegriffen werden kann, gibt es einige Einschränkungen bei der Verwendung dieses Webbrowsers. Beispielsweise können Benutzer von Internet Explorer 8 die Größe der PowerPoint-Phase nicht auf eine benutzerdefinierte Größe ändern. Stattdessen sind Sie auf die Verwendung einer von drei vordefinierten Phasen Größen limitiert. Ebenso können Internet Explorer 8-Benutzer keine Mediendateien wiedergeben.

</div>

<span> </span>

</div>

</div>

</div>

