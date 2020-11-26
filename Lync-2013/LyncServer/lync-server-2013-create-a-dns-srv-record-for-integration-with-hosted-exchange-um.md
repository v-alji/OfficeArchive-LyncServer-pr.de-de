---
title: Erstellen eines DNS-SRV-Eintrags für die Integration in gehostete Exchange UM-Dienste
description: Erstellen Sie einen DNS-SRV-Eintrag für die Integration in gehostete Exchange um.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create a DNS SRV record for integration with hosted Exchange UM
ms:assetid: 8ea590ae-58ea-4ca5-9853-e0708b3ea760
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh500728(v=OCS.15)
ms:contentKeyID: 48184770
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 694a595977abe33bebbb5fbcf2a508c9bb4e35a4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432233"
---
# <a name="create-a-dns-srv-record-for-integration-with-hosted-exchange-um"></a>Erstellen eines DNS-SRV-Eintrags für die Integration in gehostete Exchange UM-Dienste

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-02-20_

In diesem Thema wird beschrieben, wie Sie den DNS-SRV-Eintrag (Domain Name System) konfigurieren, der für einen lync Server 2013-Edgeserver zur Weiterleitung an einen gehosteten Exchange-Dienst wie Microsoft Exchange Online erforderlich ist.

<div>

## <a name="to-create-an-external-dns-srv-record-for-the-hosted-exchange-service"></a>So erstellen Sie einen externen DNS-SRV-Eintrag für den gehosteten Exchange-Dienst

1.  Melden Sie sich beim externen DNS-Server als Mitglied der DnsAdmins-Gruppe an.

2.  Klicken Sie auf **Start**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **DNS**.

3.  Erweitern Sie in der Konsolenstruktur ihrer SIP-Domäne **Forward-Lookupzonen**, und wählen Sie die SIP-Domäne aus, in der lync Server 2013 installiert werden soll.
    
    <div>
    

    > [!IMPORTANT]
    > Sie müssen den DNS-SRV-Eintrag in der SIP-Domäne erstellen, in der lync Server installiert ist oder installiert wird. Wenn Sie den SRV-Eintrag erstellen, muss der für den Host mit diesem Dienst Feld verwendete FQDN der externe FQDN des Edge-Pools sein. Wenn beispielsweise der externe FQDN Ihres Edge-Pools Edge01.contoso.net lautet, geben Sie diesen Wert ein. Dieser muss sich ebenfalls in der gleichen Domäne wie der DNS-Hosteintrag (A) befinden.

    
    </div>

4.  Klicken Sie mit der rechten Maustaste auf die ausgewählte Domäne, und klicken Sie dann auf **Weitere neue Einträge**.

5.  Klicken Sie unter **Ressourceneintragstyp** auf **Dienststandort (SRV)**, und klicken Sie dann auf **Datensatz erstellen**.

6.  Klicken Sie im **neuen Ressourceneintrag** auf **Dienst**, und geben Sie **\_ sipfederationtls** ein.

7.  Klicken Sie auf **Protokoll**, und geben Sie dann **\_ TCP** ein.

8.  Klicken Sie auf **Portnummer** und geben Sie **5061** ein.

9.  Klicken Sie auf **Host mit diesem Dienst**, und geben Sie dann den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des lync Server 2013-Edge-Pools ein, der Zugriff auf Ihr lync Server 2013-System für vertrauenswürdige externe Clients bietet.
    
    <div>
    

    > [!NOTE]
    > Die Domäne muss auch als autorisierende, akzeptierte Domäne in Ihren Exchange Online-Einstellungen eingerichtet werden. Ausführliche Informationen finden Sie unter Erstellen von akzeptierten Domänen unter <A href="https://go.microsoft.com/fwlink/p/?linkid=229762">https://go.microsoft.com/fwlink/p/?linkId=229762</A> .

    
    </div>

10. Klicken Sie auf **OK** und dann auf **Fertig**.

</div>

<div>

## <a name="to-verify-that-the-dns-srv-record-was-created-successfully"></a>So überprüfen Sie, ob der DNS-SRV-Eintrag erfolgreich erstellt wurde

1.  Melden Sie sich bei einem Clientcomputer in der Domäne an.

2.  Klicken Sie auf  **Start** und dann auf  **Ausführen**.

3.  Führen Sie an der Eingabeaufforderung den folgenden Befehl aus:
    
        nslookup <FQDN Lync Edge Pool>

4.  Überprüfen Sie, ob Sie eine Antwort erhalten, die in die entsprechende IP-Adresse für den FQDN aufgelöst wird.

</div>

<div>

## <a name="see-also"></a>Siehe auch


[Erstellen von DNS-Einträgen für Reverseproxyserver in Lync Server 2013](lync-server-2013-create-dns-records-for-reverse-proxy-servers.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

