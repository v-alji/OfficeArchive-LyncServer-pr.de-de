---
title: Cmdlets in Skype for Business Online, die eine Benutzeridentität verwenden
description: Cmdlets in Skype for Business Online, die eine Benutzeridentität verwenden.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Cmdlets that use a user identity
ms:assetid: be87409f-6372-4c70-91ac-6ef13dfbe65a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362842(v=OCS.15)
ms:contentKeyID: 56558859
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 29f838317f8b2779de862eb2df82ae1b348871e4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394235"
---
# <a name="cmdlets-in-skype-for-business-online-that-use-a-user-identity"></a>Cmdlets in Skype for Business Online, die eine Benutzeridentität verwenden

 


In Skype for Business Online gibt es eine Reihe von unterschiedlichen Möglichkeiten, auf eine einzelne Benutzeridentität zu verweisen:

  - Verwenden Sie den Anzeigenamen der Active Directory-Domänendienste des Benutzers. Beispiel:
    
        -Identity "Ken Myer"

  - Verwenden Sie die SIP-Adresse des Benutzers. Beispiel:
    
        -Identity "sip:kenmyer@litwareinc.com"

  - Verwenden Sie den UPN des Benutzers. Beispiel:
    
        -Identity " kenmyer@litwareinc.com"

  - Verwenden Sie den Distinguished Name für den Active Directory-Domänendienst des Benutzers. Beispiel:
    
        -Identity "CN=48ebd1ba-95d4-460c-b751-811ebf0c4611,OU=fa8226f5-14fa-46da-8 236-039b25bc7a27,OU=Lync Online Tenants,DC=litwareinc,DC=com"

Die folgenden Cmdlets akzeptieren eine Benutzeridentität:

  - [Disable-CsMeetingRoom](https://technet.microsoft.com/library/jj204723\(v=ocs.15\))

  - [Enable-CsMeetingRoom](https://technet.microsoft.com/library/jj205062\(v=ocs.15\))

  - [Get-CsExUmContact](https://technet.microsoft.com/library/gg412725\(v=ocs.15\))

  - [Get-CsMeetingRoom](https://technet.microsoft.com/library/jj205277\(v=ocs.15\))

  - [Get-CsOnlineUser](https://technet.microsoft.com/library/jj994026\(v=ocs.15\))

  - [Get-CsUserAcp](https://technet.microsoft.com/library/gg398978\(v=ocs.15\))

  - [New-CsExUmContact](https://technet.microsoft.com/library/gg398139\(v=ocs.15\))

  - [Remove-CsExUmContact](https://technet.microsoft.com/library/gg398946\(v=ocs.15\))

  - [Remove-CsUserAcp](https://technet.microsoft.com/library/gg398982\(v=ocs.15\))

  - [Set-CsExUmContact](https://technet.microsoft.com/library/gg412944\(v=ocs.15\))

  - [Set-CsMeetingRoom](https://technet.microsoft.com/library/jj204831\(v=ocs.15\))

  - [Set-CsUserAcp](https://technet.microsoft.com/library/gg413018\(v=ocs.15\))

Beachten Sie, dass Sie beim Aufrufen eines der **Get-CS-** Cmdlets keine Benutzeridentität angeben müssen. In diesem Fall geben die Cmdlets alle Instanzen des angegebenen Elements zurück. Dieser Befehl gibt beispielsweise Informationen zu allen Benutzern zurück, die für Skype for Business Online aktiviert wurden:

    Get-CsOnlineUser

Der Parameter Identity ist nur erforderlich, wenn Sie Informationen für einen bestimmten Benutzer zurückgeben möchten:

    Get-CsOnlineUser -Identity "Ken Myer"

## <a name="see-also"></a>Siehe auch


[Identitäten, Bereiche und Mandanten in Skype for Business Online](identities-scopes-and-tenants-in-skype-for-business-online.md)  
[Die Lync Online-Cmdlets](https://technet.microsoft.com/library/dn362817\(v=ocs.15\))

