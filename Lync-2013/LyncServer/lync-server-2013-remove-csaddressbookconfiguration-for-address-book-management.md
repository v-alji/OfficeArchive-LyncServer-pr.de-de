---
title: Remove-CsAddressBookConfiguration für die Verwaltung von Adressbüchern
description: Remove-CsAddressBookConfiguration für die Verwaltung von Adressbüchern.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove-CsAddressBookConfiguration for Address Book management
ms:assetid: 5d173ebe-ec4d-4640-8432-a25071ea9cc5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429705(v=OCS.15)
ms:contentKeyID: 48184258
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d513c128dfe87c5a6e92b66a6ba4e1dbdfbfb651
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436440"
---
# <a name="remove-csaddressbookconfiguration-for-address-book-management-in-lync-server-2013"></a>Remove-CsAddressBookConfiguration für die Verwaltung von Adressbüchern in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-11-01_

Wer dieses Cmdlet ausführen kann: Standardmäßig sind Mitglieder der folgenden Gruppen autorisiert, das Remove-CsAddressBookConfiguration-Cmdlet lokal auszuführen: RTCUniversalServerAdmins. Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller rollenbasierten zugriffssteuerungsrollen zurückzugeben, denen dieses Cmdlet zugewiesen wurde (einschließlich aller benutzerdefinierten RBAC-Rollen, die Sie selbst erstellt haben):

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Remove-CsAddressBookConfiguration"}

Wie der Name andeutet, entfernt Remove-CsAddressBookConfiguration die Konfiguration basierend auf der definierten Websiteidentität.

Beispiel:

    Remove-CsAddressBookConfiguration -Identity site:Redmond

<div>

## <a name="see-also"></a>Siehe auch


[Remove-CsAddressBookConfiguration](https://technet.microsoft.com/library/Gg398934(v=OCS.15))  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

