---
title: 'Lync Server 2013: Ändern der Global Hosted Voicemail-Richtlinie'
description: 'Lync Server 2013: Ändern der globalen Richtlinie für gehostete Voicemail.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify the global hosted voice mail policy
ms:assetid: f059b3ce-a7d8-4ea9-b10b-0052222ec2ce
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412994(v=OCS.15)
ms:contentKeyID: 48185757
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9cd5e16c78049ce79abd936a79b2025a14e45943
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445701"
---
# <a name="modify-the-global-hosted-voice-mail-policy-in-lync-server-2013"></a>Ändern der Global Hosted Voicemail-Richtlinie in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-24_

Die *Global* Hosted Voicemail-Richtlinie wird mit lync Server 2013 installiert. Sie können Sie ändern, um Ihre Anforderungen zu erfüllen, aber Sie können Sie nicht umbenennen oder löschen. Zum Ändern der globalen Richtlinie verwenden Sie das Set-CsHostedVoicemailPolicy-Cmdlet, um die Parameter auf die entsprechenden Werte für die jeweilige Bereitstellung zu setzen.

Details zum Cmdlet " [setCsHostedVoicemailPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsHostedVoicemailPolicy) " finden Sie in der Dokumentation zur lync Server-Verwaltungsshell.

<div>

## <a name="to-modify-the-global-hosted-voice-mail-policy"></a>So ändern Sie die Global Hosted Voicemail-Richtlinie

1.  Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.

2.  Führen Sie das Set-CsHostedVoicemailPolicy-Cmdlet aus, um die globalen Richtlinienparameter für Ihre Umgebung einzurichten. Führen Sie beispielsweise den folgenden Befehl aus:
    
        Set-CsHostedVoicemailPolicy -Destination ExUM.fabrikam.com -Organization "corp1.litwareinc.com"
    
    Da dieser Befehl den Identitätsparameter der Richtlinie nicht angibt, legt die Windows PowerShell-Befehlszeilenschnittstelle die folgenden Werte für die Global Hosted Voicemail-Richtlinie fest:
    
      - **Ziel** gibt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des gehosteten Exchange um-Diensts an. Dieser Parameter ist optional, aber wenn Sie versuchen, einen Benutzer für gehostete Voicemail zu aktivieren, und die zugewiesene Richtlinie des Benutzers keinen Zielwert hat, schlägt die Aktivierung fehl.
    
      - **Organisation** gibt eine durch trennzeichengetrennte Liste der Exchange-Mandanten an, die zu den lync Server-Benutzern werden. Jeder Mandant muss als FQDN dieses Mandanten für den gehosteten Exchange um-Dienst angegeben werden.
    
    <div>
    

    > [!NOTE]  
    > Im vorherigen Beispiel-Cmdlet ersetzt der Wert "corp1.litwareinc.com" alle Werte, die möglicherweise bereits im Parameter Organization vorhanden sind. Wenn die Richtlinie beispielsweise bereits eine durch trennzeichengetrennte Liste von Organisationen enthält, wird die vollständige Liste ersetzt. Wenn Sie der Liste eine Organisation hinzufügen möchten, anstatt die gesamte Liste zu ersetzen, führen Sie einen Befehl wie den folgenden aus.

    
    </div>
    
        $a = Get-CsHostedVoicemailPolicy
        $a.Organization += ",corp3.litwareinc.com"
        Set-CsHostedVoicemailPolicy -Organization $a.Organization

</div>

</div>

<span> </span>

</div>

</div>

</div>

