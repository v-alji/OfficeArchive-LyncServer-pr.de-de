---
title: 'Lync Server 2013: Remove-CsWebServiceConfiguration für die Verwaltung von Adressbüchern'
description: 'Lync Server 2013: Remove-CsWebServiceConfiguration für die Verwaltung von Adressbüchern.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Remove-CsWebServiceConfiguration for Address Book management
ms:assetid: 91947cad-5cdd-41b9-83e1-650703c55879
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg429713(v=OCS.15)
ms:contentKeyID: 48184848
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 145cb1cb98bcb4c988a8fdaea74a4eae86d5fc4f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436426"
---
# <a name="remove-cswebserviceconfiguration-for-address-book-management-in-lync-server-2013"></a>Remove-CsWebServiceConfiguration für die Verwaltung von Adressbüchern in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-11-01_

Wer dieses Cmdlet ausführen kann: Standardmäßig sind Mitglieder der folgenden Gruppen autorisiert, das Remove-CsWebServiceConfiguration-Cmdlet lokal auszuführen: RTCUniversalServerAdmins. Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller rollenbasierten zugriffssteuerungsrollen zurückzugeben, denen dieses Cmdlet zugewiesen wurde (einschließlich aller benutzerdefinierten RBAC-Rollen, die Sie selbst erstellt haben):

    Get-CsAdminRole | Where-Object {$_.Cmdlets -match "Remove-CsWebServiceConfiguration"}

Das Remove-CsWebServiceConfiguration-Cmdlet ermöglicht es einem Administrator, eine zuvor erstellte Webdienste-Konfiguration zu entfernen. Das Cmdlet kann die globale Webdienste-Konfiguration nicht entfernen.

Beispiel:

    Remove-CsWebServiceConfiguration -Identity site:Redmond

<div>

## <a name="see-also"></a>Siehe auch


[Remove-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsWebServiceConfiguration)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

