---
title: 'Lync Server 2013: DNS-Anforderungen für Standard Edition-Server'
description: 'Lync Server 2013: DNS-Anforderungen für Standard Edition-Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Standard Edition servers
ms:assetid: 3d6bbe65-e7ce-491b-a0bd-d2f7197f240d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425900(v=OCS.15)
ms:contentKeyID: 48183920
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cc93549e07fb82304ad76b051730eab972530764
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393983"
---
# <a name="dns-requirements-for-standard-edition-servers-in-lync-server-2013"></a>DNS-Anforderungen für Standard -Edition-Server in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Zuletzt geändertes Thema:** 19.06.2012_

In diesem Abschnitt werden die DNS (Domain Name System)-Einträge beschrieben, die für die Bereitstellung von Standard -Edition-Servern erforderlich sind.

<div>

## <a name="dns-records-for-standard-edition-servers"></a>DNS Records for Standard Edition Servers

In der folgenden Tabelle sind die DNS-Anforderungen für die Serverbereitstellung von Lync Server 2013 Standard Edition aufgeführt.

### <a name="dns-requirements-for-a-standard-edition-server"></a>DNS-Anforderungen für einen Standard Edition Server

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
<td><p>Automatische Client anmeldung</p></td>
<td><p>Für jede unterstützte SIP-Domäne: ein SRV-Eintrag für _sipinternaltls._tcp. &lt; domäne über Port 5061, der dem FQDN des Standard Edition-Servers, der Clientanforderungen für die Anmeldung authentifiziert und &gt; umleitigt, zu ordnet. Details finden Sie unter <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">den DNS-Anforderungen für die automatische Client anmeldung bei Lync Server 2013.</a></p></td>
</tr>
<tr class="odd">
<td><p>Device Update Web Service Discovery by Unified Communications (UC)-Geräte</p></td>
<td><p>Ein interner A-Datensatz mit dem Namen "ucupdates-r2". &lt; &gt; SIP-Domäne, die in die IP-Adresse des Serverupdatewebdiensts für das Hosten von Standard Edition aufgelöst wird. Wenn ein UC-Gerät aktiviert ist, sich ein Benutzer aber noch nie beim Gerät angemeldet hat, ermöglicht der A-Eintrag dem Gerät, den Serverhostingwebdienst für Geräteaktualisierungen zu ermitteln und Updates zu erhalten. Andernfalls rufen Geräte die Serverinformationen über die In-Band-Bereitstellung ab, wenn sich der Benutzer das erste Mal anmeldet.</p></td>
</tr>
<tr class="even">
<td><p>Ein Reverseproxy zur Unterstützung von HTTP-Datenverkehr</p></td>
<td><p>Ein externer A-Eintrag, der den FQDN der externen Webfarm in die externe IP-Adresse des Reverseproxys aufhebt. Clients und UC-Geräte verwenden diesen Eintrag, um eine Verbindung mit dem Reverseproxy herzustellen. Ausführliche Informationen finden Sie in der Dokumentation zur Planung unter "Ermitteln der DNS-Anforderungen für <a href="lync-server-2013-determine-dns-requirements.md">Lync Server 2013".</a></p></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</div>

