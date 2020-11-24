---
title: 'Lync Server 2013: Konfiguration von standortbasiertem Routing für Konferenzen'
description: 'Lync Server 2013: Konfiguration von Location-Based Routing für Konferenzen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration of Location-Based Routing for conferencing
ms:assetid: d8c708cc-a1b1-48b1-808c-a64df15f7701
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362846(v=OCS.15)
ms:contentKeyID: 56335088
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a87f9c799e565f64b0dd30ce025a4e7a3174625
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395159"
---
# <a name="configuration-of-location-based-routing-for-conferencing-in-lync-server-2013"></a>Konfiguration von standortbasiertem Routing für Konferenzen in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2013-09-11_

Die Location-Based Routing Konferenz Anwendung basiert auf der Konfiguration von lync Server 2013 Location-Based-Routing. Die wichtigsten Konfigurationen sind die folgenden:

  - Die Position der Teilnehmer, die an einer Besprechung teilnehmen, wird basierend auf Ihrer Netzwerk Website festgelegt. Eine Netzwerk Website und die zugehörigen Netzwerk-Subnetze müssen in lync Server definiert werden, um Location-Based Routing durchzusetzen.

  - Um Location-Based Routing von Besprechungen durchzusetzen, müssen lync-Teilnehmer für Location-Based Routing aktiviert sein.

  - Um Location-Based Routing von PSTN-Endpunkten durchzusetzen, die an Besprechungen teilnehmen, muss der für die Verbindung der PSTN-Endpunkte verwendete SIP-Trunk für Location-Based Routing konfiguriert sein

Weitere Informationen zum Bereitstellen und Konfigurieren von lync Server 2013 Location-Based-Routing finden Sie unter Konfigurieren des [standortbasierten Routings](lync-server-2013-configuring-location-based-routing.md).

<div>

## <a name="enabling-the-location-based-routing-conferencing-application"></a>Aktivieren der Location-Based Routing Konferenz Anwendung

Die Location-Based-Routing Konferenz Anwendung ist standardmäßig deaktiviert. Bevor Sie diese Anwendung aktivieren, müssen Sie die richtige Priorität ermitteln, die für die Anwendung zugewiesen werden soll. Führen Sie das folgende Cmdlet in der lync Server-Verwaltungsshell aus, um diese Priorität zu ermitteln:

```powershell
Get-CsServerApplication -Identity Service:Registrar:<Pool FQDN>
```

In diesem Cmdlet \<Pool FQDN\> ist der Pool, in dem die Location-Based Routing Konferenz Anwendung aktiviert werden soll.

Dieses Cmdlet gibt die Liste der von lync Server gehosteten Anwendungen zurück, und der Prioritätswert für jeden von Ihnen. Der Location-Based Routing Konferenz Anwendung muss ein Prioritätswert zugewiesen werden, der größer als die Anwendung "UdcAgent" und kleiner als die Anwendungen "DefaultRouting", "ExumRouting" und "OutboundRouting" ist. Wir empfehlen, dass Sie der Location-Based Routing Konferenz Anwendung einen Prioritätswert zuweisen, der einen Punkt höher als der Prioritätswert der Anwendung "UdcAgent" ist.

Wenn beispielsweise die Anwendung "UdcAgent" einen Prioritätswert von "2" aufweist, hat die Anwendung "DefaultRouting" den Prioritätswert "8", die "ExumRouting"-Anwendung einen Prioritätswert von "9" und die "OutboundRouting"-Anwendung einen Prioritätswert von "10", und Sie sollten der Location-Based Routing Konferenz Anwendung einen Prioritätswert von "3" zuweisen. Auf diese Weise würde die Priorität der Anwendungen in der folgenden Reihenfolge platziert: andere Anwendungen (Prioritäten: 0 bis 1), "UdcAgent" (Priorität: 2), Location-Based Routing Konferenz Anwendung (Priorität: 3), andere Anwendungen (Prioritäten: 4 bis 8), "DefaultRouting" (Priorität: 9), "ExumRouting" (Priorität: 10) und "OutboundRouting" (Priorität: 11).

Nachdem Sie den richtigen Prioritätswert für die Location-Based Routing Konferenz Anwendung gefunden haben, geben Sie das folgende Cmdlet für jeden Front-End Pool oder Standard Edition-Server ein, auf dem Benutzer für Location-Based Routing aktiviert sind:

```powershell
New-CsServerApplication -Identity Service:Registrar:<Pool FQDN>/LBRouting -Priority <Application Priority> -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

Beispiel:

```powershell
New-CsServerApplication -Identity Service:Registrar:LS2013CU2LBRPool.contoso.com/LBRouting -Priority 3 -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

Nachdem Sie dieses Cmdlet verwendet haben, starten Sie alle Front-End-Server im Pool oder die Standard Edition-Server neu, auf denen die Location-Based Routing Konferenz Anwendung aktiviert wurde.

<div>


> [!IMPORTANT]  
> Location-Based-Routing-Erzwingung von Konferenzen oder beratenden Übertragungen wird erst erzwungen, wenn alle Front-End-Server in den entsprechenden Pools oder den Standard Edition-Servern neu gestartet werden.



</div>

Nachdem die Location-Based Routing Konferenz Anwendung erfolgreich aktiviert wurde und alle anwendbaren lync-Server neu gestartet wurden, werden alle Konferenzen, die von lync-Benutzern für Location-Based Routing aktiviert wurden, überwacht, um eine PSTN-Maut Umgehung zu verhindern.

</div>

</div>

<span> </span>

</div>

</div>

</div>

