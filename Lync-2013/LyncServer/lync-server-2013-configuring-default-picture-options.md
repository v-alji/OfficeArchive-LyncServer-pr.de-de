---
title: 'Lync Server 2013: Konfigurieren von Standardbild Optionen'
description: 'Lync Server 2013: Konfigurieren von Standardbild Optionen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring default picture options
ms:assetid: b1c986f0-6400-447a-9e36-78c1c3a4f793
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn205074(v=OCS.15)
ms:contentKeyID: 56280893
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6261aca82b4c71eb8e0573e8d2adbfc008e743fc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433213"
---
# <a name="configuring-default-picture-options-in-lync-server-2013"></a>Konfigurieren von Standardbild Optionen in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-03-22_

Standardmäßig werden die Bilder der Benutzer automatisch angezeigt. Wenn Benutzer Ihre Bilder ausblenden möchten, können Sie die Option " **mein Bild ausblenden** " im lync-Client auswählen. Diese Einstellung wird jedoch von einigen anderen Office-Anwendungen ignoriert.

Wenn die Möglichkeit zum Anzeigen von Bildern, auch wenn Sie vom Benutzer deaktiviert werden, problematisch ist, können Sie die Einstellungen für die lync-Bildanzeige Global oder für eine Website oder einen Dienst ändern, damit die Bilder der Benutzer nicht standardmäßig angezeigt werden. Verwenden Sie das folgende Cmdlet der lync Server-Verwaltungsshell, damit die Bilder des Benutzers nur angezeigt werden, wenn Sie die Option " **mein Bild anzeigen** " im Client explizit auswählen:

    Set-CsPrivacyConfiguration -DisplayPublishedPhotoDefault $False

Weitere Informationen zu diesem Cmdlet finden Sie in der Dokumentation zur lync Server-Verwaltungsshell unter [CsPrivacyConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsPrivacyConfiguration) .

</div>

<span> </span>

</div>

</div>

</div>

