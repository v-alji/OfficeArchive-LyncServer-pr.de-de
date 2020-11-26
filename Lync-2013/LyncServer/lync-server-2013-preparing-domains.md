---
title: 'Lync Server 2013: Vorbereiten von Domänen'
description: 'Lync Server 2013: Vorbereiten von Domänen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing domains
ms:assetid: 8eea541c-5f9d-4afc-92a8-a31d6f742544
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398721(v=OCS.15)
ms:contentKeyID: 48184816
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7700bbdd10a96949f892858ae03da8de60d86a3a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424163"
---
# <a name="preparing-domains-for-lync-server-2013"></a>Vorbereiten von Domänen für Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-10-29_

Die Domänenvorbereitung ist der letzte Schritt beim Vorbereiten der Active Directory-Domänendienste für lync Server 2013. Beim Schritt zur Domänenvorbereitung werden universellen Gruppen die erforderlichen ACEs (Access Control Entries, Zugriffssteuerungseinträge) hinzugefügt, über die Berechtigungen zum Hosten und Verwalten von Benutzern in der Domäne gewährt werden. Bei der Domänenvorbereitung werden ACEs im Domänenstamm und in drei integrierten Containern erstellt: für Benutzer, Computer und Domänencontroller.

Sie können die Domänenvorbereitung auf jedem Computer in der Domäne ausführen, in der Sie lync Server bereitstellen. Sie müssen jede Domäne vorbereiten, die lync Server oder Benutzer hosten soll.

Wenn die Vererbung von Berechtigungen deaktiviert ist oder die Berechtigungen für authentifizierte Benutzer in Ihrer Organisation deaktiviert sind, müssen Sie während der Domänenvorbereitung weitere Schritte ausführen. Ausführliche Informationen finden Sie unter [Vorbereiten einer gesperrten Active Directory-Domänendienste in lync Server 2013](lync-server-2013-preparing-a-locked-down-active-directory-domain-services.md).

Wenn Ihre Organisation Organisationseinheiten (OU) anstelle der drei integrierten Container (also Benutzer, Computer und Domänencontroller) verwendet, müssen Sie den Organisationseinheiten Lesezugriff für die Gruppe Authentifizierte Benutzer erteilen. Für die Domänenvorbereitung ist Lesezugriff auf die Container erforderlich. Wenn die Gruppe der authentifizierten Benutzer keinen Lesezugriff auf die Organisationseinheit hat, führen Sie das Cmdlet **Grant-CsOuPermission** aus, wie in den folgenden Codebeispielen veranschaulicht, um Leseberechtigungen für jede OU zu erteilen.

   ```PowerShell
    Grant-CsOuPermission -ObjectType <User | Computer | InetOrgPerson | Contact | AppContact | Device> -OU <DN of the OU > 
   ```

   ```PowerShell
    Grant-CsOuPermission -ObjectType "user","contact",inetOrgPerson" -OU "ou=Redmond,dc=contoso,dc=net"
   ```

Details zum Cmdlet **Grant-CsOuPermission** finden Sie in der Dokumentation zur lync Server-Verwaltungsshell.

<div class="">


> [!TIP]  
> Details zu den ACEs, die im Domänenstamm und in den Containern Benutzer, Computer und Domänencontroller erstellt wurden, finden Sie unter Änderungen, die <A href="lync-server-2013-changes-made-by-domain-preparation.md">von der Domänenvorbereitung in lync Server 2013 vorgenommen</A>wurden.



</div>

<div>

## <a name="in-this-section"></a>In diesem Abschnitt

  - [Ausführen der Domänenvorbereitung für Lync Server 2013](lync-server-2013-running-domain-preparation.md)

  - [Verwenden von Cmdlets zum Rückgängigmachen der Domänenvorbereitung für Lync Server 2013](lync-server-2013-using-cmdlets-to-reverse-domain-preparation.md)

</div>

</div>

<span> </span>

</div>

</div>

</div>

