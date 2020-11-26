---
title: 'Lync Server 2013: Hinzufügen von benutzerdefiniertem Text zu Chatnachrichten'
description: 'Lync Server 2013: Hinzufügen von benutzerdefiniertem Text zu Sofortnachrichten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Adding custom text to instant messages
ms:assetid: cabcc3ec-9d35-42ac-a403-e21b7d538c2c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398847(v=OCS.15)
ms:contentKeyID: 48185458
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 54f5cf031da0ba4d5bd0b6dbaa7f5ebc9d0b3a6c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439233"
---
# <a name="adding-custom-text-to-instant-messages-in-lync-server-2013"></a>Hinzufügen von benutzerdefiniertem Text zu Chatnachrichten in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-02-20_

Fügen Sie am Anfang jeder lync 2013-Sofortnachrichtenunterhaltung (im) mithilfe der Cmdlets " **New-CSClientPolicy** " oder " **CSClientPolicy** " der lync Server-Verwaltungsshell mit dem Parameter "unwarning" eine Verzichtserklärung oder eine Warnung hinzu.

Mit dem Befehl im folgenden Beispiel wird eine Sicherheits Erinnerung am Anfang des Unterhaltungsfensters hinzugefügt, wenn eine neue Chat Unterhaltung beginnt:

    New-CsClientPolicy -Identity IMSecurityNotice -IMWarning 
    "Remember, security is everyone's responsibility. Keep it confidential."

Verwenden Sie **Grant-CSClientPolicy** , um diese neue Richtlinie Benutzern zuzuweisen. Ausführliche Informationen finden Sie unter **New-CSClientPolicy** und **Grant-CSClientPolicy** in der Dokumentation zur lync Server-Verwaltungsshell.

</div>

<span> </span>

</div>

</div>

</div>

