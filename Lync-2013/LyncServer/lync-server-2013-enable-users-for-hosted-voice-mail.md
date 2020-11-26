---
title: 'Lync Server 2013: Aktivieren von Benutzern für gehostete Voicemail'
description: 'Lync Server 2013: Aktivieren von Benutzern für gehostete Voicemail.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable users for hosted voice mail
ms:assetid: fa559f8f-ef99-43a1-b580-9e998b95efb8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413062(v=OCS.15)
ms:contentKeyID: 48185919
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3853a70d433c09029a02f2ca6256b5988defdcb2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437469"
---
# <a name="enable-users-for-hosted-voice-mail-in-lync-server-2013"></a>Aktivieren von Benutzern für gehostete Voicemail in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-24_

Führen Sie das Verfahren zum Aktivieren von lync Server 2013-Benutzern für Voicemail in einem gehosteten Exchange Unified Messaging (um)-Dienst aus.

Ausführliche Informationen finden Sie unter [gehostete Exchange-Benutzerverwaltung in lync Server 2013](lync-server-2013-hosted-exchange-user-management.md) in der Planungsdokumentation.

Details zum Cmdlet " [setCsUser](https://docs.microsoft.com/powershell/module/skype/Set-CsUser) " finden Sie in der Dokumentation zur lync Server-Verwaltungsshell.

<div>


> [!IMPORTANT]  
> Bevor ein lync Server 2013-Benutzer für gehostete Voicemail aktiviert werden kann, muss eine gehostete Voicemail-Richtlinie bereitgestellt werden, die für Ihr Benutzerkonto gilt. Ausführliche Informationen finden Sie unter <A href="lync-server-2013-hosted-voice-mail-policies.md">Richtlinien für gehostete Voicemail in lync Server 2013</A>.



</div>

<div>

## <a name="to-enable-users-for-hosted-voice-mail"></a>So aktivieren Sie Benutzer für gehostete Voicemails

1.  Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.

2.  Führen Sie das Set-CsUser-Cmdlet aus, um das Benutzerkonto für gehostete Voicemail zu konfigurieren. Führen Sie beispielsweise den folgenden Befehl aus:
    
        Set-CsUser -HostedVoiceMail $True -Identity "contoso\kenmyer"
    
    Im oben stehenden Beispiel werden folgende Parameter festgelegt:
    
      - **HostedVoiceMail** ermöglicht es, dass die Voicemail-Anrufe eines Benutzers an den Hosted Exchange um weitergeleitet werden. Außerdem signalisiert Microsoft lync 2013, dass die Anzeige "Voicemail anrufen" leuchtet.
    
      - **Identity** gibt das zu ändernde Benutzerkonto an. Der Identity-Wert kann mit einem der folgenden Formate angegeben werden:
        
          - Die SIP-Adresse des Benutzers
        
          - Name des Active Directory-Benutzerprinzipals des Benutzers
        
          - Der Domänen \\ Anmeldename des Benutzers (beispielsweise contoso \\ kenmyer)
        
          - Die Active Directory-Domänendienste des Benutzers Display-Name (beispielsweise Ken Myers). Wenn Sie die Display-Name als Identitätswert verwenden, können Sie das \* Platzhalterzeichen Sternchen () verwenden. Die Identität " \* Smith" gibt beispielsweise alle Benutzer zurück, die eine Display-Name haben, die mit dem Zeichenfolgenwert "Smith" endet.
        
        <div>
        

        > [!NOTE]  
        > Der Name des Active Directory-SAM-Kontos des Benutzers kann nicht als Identitätswert verwendet werden, da der Name des SAM-Kontos in der Gesamtstruktur nicht unbedingt eindeutig ist.

        
        </div>

</div>

</div>

<span> </span>

</div>

</div>

</div>

