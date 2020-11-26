---
title: 'Lync Server 2013: Unterstützte Gerätehardware'
description: Unterstützung für lync Server 2013-Gerätehardware.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device hardware support
ms:assetid: ba07ca91-32b4-49cf-801c-47a2d1d96e18
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412908(v=OCS.15)
ms:contentKeyID: 48185222
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cd03936d35fbc3a639a3ba4596a4357e8e379719
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429451"
---
# <a name="device-hardware-support-in-lync-server-2013"></a>Unterstützte Gerätehardware in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-12-14_

Bevor Sie IP-Telefone und analoge Geräte bereitstellen, müssen bestimmte Hardwarekonfigurationen vorhanden sein.

IP-Telefone mit lync Phone Edition-Unterstützung für die Verbindungsschicht Erkennung Protocol-Media Endpunkt Ermittlung (LLDP-MED) und Power over Ethernet (PoE). Um die Vorteile von LLDP-MED zu nutzen, muss der Switch IEEE 802.1 ab und ANSI/TIA-1057 unterstützen. Um Poe nutzen zu können, muss der Switch Poe 802.3 AF oder 802.3 at unterstützen.

Um LLDP-MED zu aktivieren, muss der Administrator LLDP über das Console-Fenster Switch aktivieren und die LLDP-MED-Netzwerkrichtlinie mit der korrekten sprach-VLAN-ID festlegen.

Wenn Ihre Bereitstellung analoge Geräte umfasst, müssen Sie außerdem das analoge Gateway für die Verwendung von lync Server konfigurieren, und das Gateway muss eine der folgenden sein:

  - Einen analogen Telefonadapter (ATA)

  - Ein analoges PSTN-Gateway

  - Eine Survivable-Branch-Appliance mit einem analogen PSTN-Gateway

  - Eine Survivable-Branch-Appliance, die ein PSTN-Gateway enthält, das mit einem ATA kommuniziert

Informationen zum Konfigurieren eines analogen Gateways finden Sie unter "Planen der Bereitstellung von analogen Geräten" [https://go.microsoft.com/fwlink/p/?LinkId=268537](https://go.microsoft.com/fwlink/p/?linkid=268537) in der lync Server 2010 TechNet-Bibliothek. (Analoge Geräte funktionieren auf die gleiche Weise in lync Server 2013 wie in lync Server 2010.)

<div>


> [!IMPORTANT]  
> Sie können den Schalter für Enhanced 9-1-1 (E9-1-1) konfigurieren, wenn dies vom Switch unterstützt wird.



</div>

</div>

<span> </span>

</div>

</div>

</div>

