---
title: 'Lync Server 2013: Anrufsteuerung für einen SIP-Trunk'
description: 'Lync Server 2013: Rufen Sie die Zulassungs Steuerung auf einem SIP-Stamm auf.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call admission control on a SIP trunk
ms:assetid: 7eada098-3d47-4be2-839f-8f87d582efe8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398632(v=OCS.15)
ms:contentKeyID: 48184623
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3667ef4608b221a1607b6bbe0d89d390cb1dd402
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435862"
---
# <a name="call-admission-control-on-a-sip-trunk-in-lync-server-2013"></a>Anrufsteuerung für einen SIP-Trunk in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-22_

Zur Bereitstellung der Anrufsteuerung für einen SIP-Trunk erstellen Sie einen Netzwerkstandort, der den Anbieter von Internettelefoniediensten repräsentiert. Um Bandbreitenrichtlinienwerte auf den SIP-Trunk anzuwenden, erstellen Sie eine standortübergreifende Richtlinie zwischen dem Netzwerkstandort in Ihrem Unternehmen und dem Netzwerkstandort, der für den Anbieter von Internettelefoniediensten erstellt wird.

Die folgende Abbildung zeigt ein Beispiel für die Bereitstellung der Anrufsteuerung für einen SIP-Trunk.

**Konfiguration der Anrufsteuerung für einen SIP-Trunk**

![Anrufsteuerung – SIP-Trunking (Diagramm)](images/Gg398632.276c0d8f-1dd5-4883-8499-c202399ddbe9(OCS.15).jpg "Anrufsteuerung – SIP-Trunking (Diagramm)")

Zur Konfiguration der Anrufsteuerung für einen SIP-Trunk müssen Sie während der Bereitstellung der Anrufsteuerung die folgenden Aufgaben ausführen:

1.  Erstellen eines Netzwerkstandorts, der den Anbieter von Internettelefoniediensten repräsentiert. Zuordnen des Netzwerkstandorts zu einer geeigneten Netzwerkregion und Zuweisen eines Bandbreitenwerts von Null für Audio und Video an diesem Netzwerkstandort. Ausführliche Informationen finden Sie unter [Konfigurieren von Netzwerk Websites für CAC in lync Server 2013](lync-server-2013-configure-network-sites-for-cac.md) in der Bereitstellungsdokumentation.
    
    <div>
    

    > [!NOTE]  
    > Für den Anbieter von Internettelefoniediensten ist diese Netzwerkstandortkonfiguration nicht funktionsfähig. Die Bandbreitenrichtlinienwerte werden tatsächlich in Schritt 2 angewendet.

    
    </div>

2.  Erstellen Sie einen Inter-Site-Link für den SIP-Trunk unter Verwendung der relevanten Parameterwerte für die Website, die Sie in Schritt 1 erstellt haben. Verwenden Sie beispielsweise den Namen der Netzwerk Website in Ihrem Unternehmen als Wert des NetworkSiteID1-Parameters und die ITSP-Netzwerk Website als Wert des NetworkSiteID2-Parameters. Ausführliche Informationen finden Sie unter [Erstellen von Netzwerk-Standortrichtlinien in lync Server 2013](lync-server-2013-create-network-intersite-policies.md) in der Bereitstellungsdokumentation. Weitere Informationen finden Sie auch in der Dokumentation zur lync Server-Verwaltungsshell für das New-CsNetworkInterSitePolicy-Cmdlet.

3.  Lassen Sie sich vom Anbieter der Internettelefoniedienste die IP-Adresse des SBC-Medienendpunkts (Session Border Controller) geben. Fügen Sie diese IP-Adresse mit der Subnetzmaske 32 zu dem Netzwerkstandort hinzu, der den Anbieter von Internettelefoniediensten repräsentiert. Ausführliche Informationen finden Sie unter [Zuordnen eines Subnetzes zu einer Netzwerk Website in lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md).

</div>

<span> </span>

</div>

</div>

</div>

