---
title: 'Lync Server 2013: Einrichten der Zertifikate für den Reverseproxy'
description: 'Lync Server 2013: richten Sie Zertifikate für den Reverse-Proxy ein.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Set up certificates for the reverse proxy
ms:assetid: c03a08ec-a67b-4f11-b0d7-6677461beaaa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412938(v=OCS.15)
ms:contentKeyID: 48185291
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4b84241775bb3594840b68551048c01ff5faba2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441746"
---
# <a name="set-up-certificates-for-the-reverse-proxy-in-lync-server-2013"></a>Einrichten der Zertifikate für den Reverseproxy in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-08_

Für jeden Reverse-Proxy Server ist ein Webserverzertifikat zur Verwendung durch den Überwachungsdienst erforderlich. Das Webserverzertifikat muss von einer öffentlichen Zertifizierungsstelle (Certification Authority, ca) ausgestellt werden.

Ausführliche Informationen zu diesen und anderen Zertifikatanforderungen finden Sie unter [Zertifikatanforderungen für den Zugriff durch externe Benutzer in lync Server 2013](lync-server-2013-certificate-requirements-for-external-user-access.md).

<div>

## <a name="to-set-up-a-web-services-certificate-for-the-reverse-proxy"></a>So richten Sie ein Webdienste-Zertifikat für den Reverse-Proxy ein

  - Sie sollten ihren Reverse-Proxy bereits eingerichtet haben, einschließlich der Einrichtung des Webdienste-Zertifikats. Wenn Sie dies nicht getan haben, bevor Sie die Bereitstellung Ihrer Edgeserver gestartet haben, verwenden Sie die Verfahren zum [Einrichten von Reverse-Proxyservern für lync Server 2013](lync-server-2013-setting-up-reverse-proxy-servers.md) , um die Anforderung zu erstellen und das Webdienst Zertifikat zu installieren, und erstellen Sie dann jede Webveröffentlichungsregel, und konfigurieren Sie Sie für die Verwendung des Zertifikats.

</div>

</div>

<span> </span>

</div>

</div>

</div>

