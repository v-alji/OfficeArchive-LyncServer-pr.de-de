---
title: 'Lync Server 2013: DNS-Anforderungen für einen Standard Edition-Server'
description: 'Lync Server 2013: DNS-Anforderungen für einen Standard Edition-Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for a Standard Edition server
ms:assetid: 5d1daf54-6e60-4ce0-9254-7d57a0835fa4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204936(v=OCS.15)
ms:contentKeyID: 48184259
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea0c7219563d62a9d99bd85655b3d3fcb0c551f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395027"
---
# <a name="dns-requirements-for-a-standard-edition-server-in-lync-server-2013"></a>DNS-Anforderungen für einen Standard Edition-Server in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Thema Zuletzt geändert:** 22.02.2013_

In diesem Abschnitt werden die DNS-Einträge (Domain Name System) beschrieben, die für die Bereitstellung von Standard Edition-Servern erforderlich sind.

<div>

## <a name="dns-records-for-standard-edition-servers"></a>DNS Records für Standard Edition Servers

In der folgenden Tabelle sind die DNS-Anforderungen für die Serverbereitstellung von Lync Server 2013 Standard Edition angegeben.


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Bereitstellungsszenario</th>
<th>DNS-Anforderung</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Standard Edition-Server</p></td>
<td><p>Ein interner A-Eintrag, mit dem der vollqualifizierte Domänenname (Fully Qualified Domain Name, FQDN) des Servers in die zugehörige IP-Adresse aufgelöst wird.</p></td>
</tr>
<tr class="even">
<td><p>Automatische Client-Anmeldung</p></td>
<td><p>Für jede unterstützte SIP-Domäne einen SRV-Eintrag für _sipinternaltls._tcp. &lt; Domäne über Port 5061, der dem FQDN des Standard Edition-Servers zu ordnet, der Clientanforderungen zur Anmeldung authentifiziert und &gt; umleitt. Details finden Sie unter <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS-Anforderungen für die automatische Client-Anmeldung in Lync Server 2013.</a></p></td>
</tr>
<tr class="odd">
<td><p>Device Update Web Service Discovery by Unified Communications (UC)-Geräte</p></td>
<td><p>Ein interner A-Eintrag mit dem Namen ucupdates-r2. &lt; &gt; SIP-Domäne, die auf die IP-Adresse des Standard Edition-Serverhosting-Geräteupdatewebdiensts aufgelöst wird. In der Situation, in der ein UC-Gerät aktiviert ist, sich ein Benutzer aber noch nie beim Gerät angemeldet hat, ermöglicht der A-Eintrag dem Gerät, den Serverhosting-Geräteupdatewebdienst zu ermitteln und Updates zu erhalten. Andernfalls rufen Geräte die Serverinformationen über die In-Band-Bereitstellung ab, wenn sich der Benutzer das erste Mal anmeldet. Ausführliche Informationen finden Sie unter <a href="lync-server-2013-device-update-web-service.md">Geräteupdatewebdienst in Lync Server 2013</a> in der Dokumentation "Vorgänge".</p></td>
</tr>
<tr class="even">
<td><p>Ein Reverseproxy zur Unterstützung von HTTP-Datenverkehr</p></td>
<td><p>Ein externer A-Eintrag, der den FQDN der externen Webfarm in die externe IP-Adresse des Reverseproxys aufhebt. Clients und UC-Geräte verwenden diesen Eintrag, um eine Verbindung mit dem Reverseproxy herzustellen. Ausführliche Informationen finden Sie <a href="lync-server-2013-determine-dns-requirements.md">unter Ermitteln der DNS-Anforderungen für Lync Server 2013</a> in der Dokumentation "Planung".</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a>Siehe auch


[DNS-Anforderungen für die automatische Client-Anmeldung in Lync Server 2013](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md)  
[Ermitteln von DNS-Anforderungen für Lync Server 2013](lync-server-2013-determine-dns-requirements.md)  


[Geräteaktualisierungs-Webdienst in Lync Server 2013](lync-server-2013-device-update-web-service.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

