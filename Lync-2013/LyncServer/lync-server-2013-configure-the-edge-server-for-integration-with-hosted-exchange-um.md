---
title: Konfigurieren des Edgeservers für die Integration in gehostete Exchange UM-Dienste
description: Konfigurieren Sie den Edgeserver für die Integration in gehostete Exchange UM.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure the Edge Server for integration with hosted Exchange UM
ms:assetid: ede3f2f9-f412-418e-a705-8d8ec98176c5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399075(v=OCS.15)
ms:contentKeyID: 48185745
ms.date: 01/24/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d1a2eb55df172e6df0bacef0c468a235cb00c3f3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433647"
---
# <a name="configure-the-edge-server-for-integration-with-hosted-exchange-um"></a>Konfigurieren des Edgeservers für die Integration in gehostete Exchange UM-Dienste

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Thema Zuletzt geändert:** 23.01.2015_

Wenn Sie Ihren Lync Server 2013-Benutzern Voicemailfunktionen für gehostete Exchange Unified Messaging (UM) bereitstellen möchten, müssen Sie die folgenden Konfigurationsaufgaben auf dem Edgeserver ausführen:

  - Konfigurieren Sie den Edgeserver für einen Partnerverbund.

  - Replizieren Sie Daten aus dem Zentralen Verwaltungsspeicher auf den Edgeserver, und überprüfen Sie die Replikation.

  - Erstellen Sie auf dem Edgeserver einen Hostinganbieter.

Ausführliche Informationen finden Sie in der Dokumentation zur Lync Server-Verwaltungsshell für die folgenden Cmdlets:

  - [Set-CsAccessEdgeConfiguration](https://technet.microsoft.com/library/Gg413017(v=OCS.15))

  - [New-CsHostingProvider](https://technet.microsoft.com/library/Gg398490(v=OCS.15))

<div>


> [!IMPORTANT]
> Vor dem Ausführen dieser Schritte müssen Sie einen externen DNS-SRV-Eintrag zum Hosten des Exchange-Diensts erstellen. Details finden Sie unter <A href="lync-server-2013-create-a-dns-srv-record-for-integration-with-hosted-exchange-um.md">Erstellen eines DNS SRV-Eintrags für die Integration in gehostete Exchange UM.</A>



</div>

<div>

## <a name="to-configure-the-edge-server-for-federation"></a>So konfigurieren Sie den Edgeserver für einen Partnerverbund

1.  Starten Sie die Lync Server-Verwaltungsshell: Klicken Sie auf **Start,** klicken Sie auf **Alle Programme,** klicken Sie auf **Microsoft Lync Server 2013,** und klicken Sie dann **auf Lync Server Management Shell**.

2.  Führen Sie das Cmdlet "Set-CsAccessEdgeConfiguration" aus, um den Server für einen Partnerverbund zu konfigurieren. Führen Sie beispielsweise den folgenden Befehl aus:
    
        Set-CsAccessEdgeConfiguration -UseDnsSrvRouting -AllowFederatedUsers 1 -EnablePartnerDiscovery 0
    
    Im oben stehenden Beispiel werden folgende Parameter festgelegt:
    
      - **UseDnsSrvRouting** gibt an, dass Edgeserver beim Senden und Empfangen von Partnerverbundanforderungen auf DNS-SRV-Einträge zurückgreifen.
    
      - **AllowFederatedUsers** gibt an, ob interne Benutzer mit Benutzern aus Partnerdomänen kommunizieren dürfen. Diese Eigenschaft legt außerdem fest, ob interne Benutzer mit Benutzern in einem Szenario mit getrennten Domänen kommunizieren können.
    
      - **EnablePartnerDiscovery** gibt an, ob Lync Server DNS-Einträge verwendet, um Partnerdomänen zu ermitteln, die nicht in der Liste der zulässigen Active Directory-Domänen aufgeführt sind. Ist False, wird Lync Server 2013 nur mit Domänen in der Liste zulässiger Domänen in Verbindung stehen. Dieser Parameter ist für die Verwendung von DNS-Dienstrouting erforderlich. In den meisten Bereitstellungen ist der Wert auf "False" gesetzt, um einen Partnerverbund mit allen Partnern zu vermeiden.

</div>

<div>

## <a name="to-replicate-data-to-the-edge-server-and-verify-the-replication"></a>So replizieren Sie Daten auf den Edgeserver und überprüfen die Replikation

  - Überprüfen Sie, ob die Replikation auf den Edgeserver vollständig durchgeführt wurde. Das Verfahren finden Sie unter [Überprüfen der Konnektivität zwischen internen Servern und Edgeservern in Lync Server 2013.](lync-server-2013-verify-connectivity-between-internal-servers-and-edge-servers.md)

</div>

<div>

## <a name="to-create-a-hosting-provider-on-the-edge-server"></a>So erstellen Sie auf dem Edgeserver einen Hostinganbieter

1.  Starten Sie die Lync Server-Verwaltungsshell: Klicken Sie auf **Start,** klicken Sie auf **Alle Programme,** klicken Sie auf **Microsoft Lync Server 2013,** und klicken Sie dann **auf Lync Server Management Shell**.

2.  Führen Sie das **New-CsHostingProvider**-Cmdlet aus, um den Hostinganbieter zu konfigurieren. Führen Sie beispielsweise den folgenden Befehl aus:
    
        New-CsHostingProvider -Identity Fabrikam.com -Enabled $True -EnabledSharedAddressSpace $True -HostsOCSUsers $False -ProxyFQDN "proxyserver.fabrikam.com" -IsLocal $False -VerificationLevel UseSourceVerification
    
    Im oben stehenden Beispiel werden folgende Parameter festgelegt:
    
      - **Identity** gibt einen eindeutigen Zeichenfolgenwert für den Hostinganbieter an, den Sie erstellen, in diesem Beispiel **Fabrikam.com**. Beachten Sie, dass der Befehl nicht erfolgreich ist, wenn bereits ein Anbieter mit dieser Identität konfiguriert wurde.
    
      - **Enabled** gibt an, ob die Netzwerkverbindung zwischen Ihrer Domäne und dem Hostinganbieter aktiviert ist. Der Nachrichtenaustausch zwischen zwei Organisationen ist erst möglich, wenn dieser Wert auf **True** festgelegt ist.
    
      - **EnabledSharedAddressSpace** gibt an, ob der Hostinganbieter in einem Szenario mit freigegebenem SIP-Adressraum (getrennte Domäne) verwendet wird.
        
        <div>
        

        > [!NOTE]
        > Versuchen Sie vor <CODE>EnableSharedAddressSpace</CODE> dem Festlegen von True, den SrV-Eintrag des Verbunds intern zu beheben. Wenn dieser Datensatz nicht intern aufgelöst werden kann, müssen Sie die Datensätze erstellen, _sipfederationtls._tcp. &lt; domäne &gt; und _sip._tls. &lt; domäne &gt; im internen DNS. Diese Einträge müssen auf die externe IP-Adresse der Zugriffsschnittstelle des Edgeservers verweisen.

        
        </div>
    
      - **HostsOCSUsers** gibt an, ob der Hostinganbieter zum Hosten von Lync Server 2013-Konten verwendet wird. Der Wert **False** gibt an, dass der Anbieter andere Kontotypen (z. B. Microsoft Exchange-Konten) hostet.
    
      - **ProxyFQDN** gibt den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des vom Hostinganbieter verwendeten Proxyservers an, in diesem Beispiel **proxyserver.fabrikam.com**. Dieser Wert kann nicht geändert werden. Wenn der Hostinganbieter seinen Proxyserver ändert, muss der Eintrag für diesen Anbieter gelöscht und neu erstellt werden.
    
      - **IsLocal** gibt an, ob der vom Hostinganbieter verwendete Proxyserver in Ihrer Lync Server 2013-Topologie enthalten ist.
    
      - **VerificationLevel** gibt die Überprüfungsstufe an, die für Nachrichten zulässig ist, die an den und vom gehosteten Anbieter gesendet werden. Geben Sie den **UseSourceVerification**-Wert an, der von der Überprüfungsstufe in Nachrichten abhängt, die vom Hostinganbieter gesendet werden. Wenn diese Stufe nicht angegeben ist, wird die Nachricht als nicht überprüfbar eingestuft und abgelehnt.

</div>

<div>

## <a name="see-also"></a>Siehe auch


[Exportieren der Lync Server 2013-Topologie und Kopieren auf externe Medien zur Edgeinstallation](lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md)  


[Überprüfen der Konnektivität zwischen internen Servern und Edgeservern in Lync Server 2013](lync-server-2013-verify-connectivity-between-internal-servers-and-edge-servers.md)  


[New-CsHostingProvider](https://technet.microsoft.com/library/Gg398490(v=OCS.15))  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

