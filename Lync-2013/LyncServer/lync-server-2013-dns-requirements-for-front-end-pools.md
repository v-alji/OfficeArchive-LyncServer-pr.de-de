---
title: 'Lync Server 2013: DNS-Anforderungen für Front -End-Pools'
description: 'Lync Server 2013: DNS-Anforderungen für Front -End-Pools.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Front End pools
ms:assetid: ba28919c-fbbe-4c54-8bf9-2b0cd3fa39c7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412910(v=OCS.15)
ms:contentKeyID: 48185228
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8c0369e82bd8ed2ea63e2156728b41f9942b0148
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429070"
---
# <a name="dns-requirements-for-front-end-pools-in-lync-server-2013"></a>DNS-Anforderungen für Front -End-Pools in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Thema Letzte Änderung:** 11.11.2012_

In diesem Abschnitt werden die DNS-Einträge (Domain Name System) beschrieben, die für die Bereitstellung von Front -End-Pools erforderlich sind.

<div>

## <a name="dns-records-for-front-end-pools"></a>DNS-Einträge für Front -End-Pools

In der folgenden Tabelle sind die DNS-Anforderungen für eine Lync Server 2013-Front-End-Poolbereitstellung angegeben.

### <a name="dns-requirements-for-a-front-end-pool"></a>DNS-Anforderungen für einen Front -End-Pool

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
<td><p>Front -End-Pool mit mehreren Front -End-Servern und einem Hardwareladeausgleich (unabhängig davon, ob der DNS-Lastenausgleich auch in diesem Pool bereitgestellt wird)</p></td>
<td><p>Wenn Sie sowohl den DNS-Lastenausgleich als auch einen Hardwareladeausgleich verwenden, müssen Sie A-Einträge hosten. Erstellen Sie einen internen A-Eintrag, der den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Front -End-Pools für den DNS-Lastenausgleich aufhebt. Erstellen Sie einen internen Hostdatensatz (A) für die internen Webdienste an die virtuelle IP-Adresse (VIP) des Load Balancers. Sie müssen den internen Webdienstnamen wie im Topologie-Generator definiert verwenden.</p>
<p>Wenn Sie z. B. sowohl den DNS-Lastenausgleich als auch den Hardwarelastausgleich verwenden, verfügen Sie über einen A-Eintrag für jeden Front End Server in einem Pool für den DNS-Lastenausgleich und einen A-Eintrag für die internen Webdienste, der auf die virtuelle IP des Hardwareladeausgleichs zeigt:</p>
<ul>
<li><p>DNS-Lastenausgleich: Pool01.contoso.net -IP-Adresse des Pools 10.10.10.5</p>
<div>

> [!WARNING]  
> Jeder Front End Server verfügt auch über einen eindeutigen A-Eintrag:


</div>
<ol>
<li><p>FE01.contoso.net 10.10.10.1</p></li>
<li><p>FE02.contoso.net 10.10.10.2</p></li>
<li><p>FE03.contoso.net 10.10.10.3</p></li>
<li><p>FE04.contoso.net 10.10.10.4</p></li>
</ol></li>
<li><p>Hardwarelastausgleich: WebInternal.contoso.net #A0 von HLB VIP 192.168.10.5</p></li>
</ul>
<p>Für den ganzen Datenverkehr mit Ausnahme von HTTP/HTTPS-Datenverkehr wird der Pool01.contoso.net verwendet. FÜR HTTP/HTTPS-Datenverkehr wird die definierte interne Webdienstadresse von 192.168.10.5 verwendet.</p></td>
</tr>
<tr class="even">
<td><p>Front -End-Pool mit bereitgestellter DNS-Lastenverteilung</p></td>
<td><p>Eine Gruppe interner A-Datensätze, die den FQDN des Pools auf die IP-Adresse jedes Servers im Pool auflösen. Für jeden Server im Pool muss ein A-Eintrag vorhanden sein.</p></td>
</tr>
<tr class="odd">
<td><p>Front -End-Pool mit bereitgestellter DNS-Lastenverteilung</p></td>
<td><p>Eine Reihe interner A-Einträge, die den FQDN jedes Servers im Pool an die IP-Adresse des Servers auflösen. Ausführliche Informationen finden Sie unter <a href="lync-server-2013-dns-load-balancing.md">DNS-Lastenausgleich in Lync Server 2013</a> in der Dokumentation zur Planung.</p></td>
</tr>
<tr class="even">
<td><p>Front -End-Pool mit einem einzelnen Front End Server und einer dedizierten Back-End-Datenbank, aber ohne Lastenausgleich</p></td>
<td><p>Ein interner A-Eintrag, der den FQDN des Front -End-Pools auf die IP-Adresse des einzelnen Enterprise Edition Front End Servers aufhebt.</p></td>
</tr>
<tr class="odd">
<td><p>Automatische Client-Anmeldung</p></td>
<td><p>Für jede unterstützte SIP-Domäne einen SRV-Eintrag für _sipinternaltls._tcp. &lt; Domäne &gt; über Port 5061, der dem FQDN des Front -End-Pools zu ordnet, der Clientanforderungen für die Anmeldung authentifiziert und umleitt. Details finden Sie unter <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS-Anforderungen für die automatische Client-Anmeldung in Lync Server 2013.</a></p></td>
</tr>
<tr class="even">
<td><p>Device Update Web Service Discovery by Unified Communications (UC)-Geräte</p></td>
<td><p>Ein interner A-Eintrag mit dem Namen ucupdates-r2. &lt; SIP-Domäne, die auf die IP-Adresse des &gt; Front -End-Pools aufgelöst wird, der den Geräteupdatewebdienst hostet. In der Situation, in der ein UC-Gerät aktiviert ist, sich ein Benutzer aber noch nie beim Gerät angemeldet hat, ermöglicht der A-Eintrag dem Gerät, den Front -End-Pool-Hostinggeräteupdate-Webdienst zu ermitteln und Updates zu erhalten. Andernfalls erhalten Geräte diese Informationen, obwohl sie bei der ersten Benutzeranmeldezeit in der Bandbereitstellung bereitgestellt werden.</p>
<div>

> [!IMPORTANT]  
> Wenn Sie in Lync Server 2010 über eine Bereitstellung des Geräteupdatewebdiensts verfügen, haben Sie bereits einen internen A-Eintrag mit dem Namen ucupdates erstellt. &lt; SIP-Domäne &gt; . Für Microsoft Office Communications Server 2007 R2 müssen Sie einen zusätzlichen DNS A-Eintrag mit dem Namen ucupdates-r2 erstellen. &lt; SIP-Domäne &gt; .


</div></td>
</tr>
<tr class="odd">
<td><p>Ein Reverseproxy zur Unterstützung von HTTP-Datenverkehr</p></td>
<td><p>Ein externer A-Eintrag, der den FQDN der externen Webfarm in die externe IP-Adresse des Reverseproxys aufhebt. Clients und UC-Geräte verwenden diesen Eintrag, um eine Verbindung mit dem Reverseproxy herzustellen. Ausführliche Informationen finden Sie <a href="lync-server-2013-determine-dns-requirements.md">unter Ermitteln der DNS-Anforderungen für Lync Server 2013</a> in der Dokumentation "Planung".</p></td>
</tr>
</tbody>
</table>


Die folgende Tabelle zeigt ein Beispiel für die dns-Einträge, die für die interne Webfarm FQDN erforderlich sind.

### <a name="example-dns-records-for-internal-web-farm-fqdn"></a>Beispiel-DNS-Einträge für FQDN der internen Webfarm

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th>FQDN für interne Webfarmen</th>
<th>Pool-FQDN</th>
<th>DNS A-Einträge</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>webcon.contoso.com</p></td>
<td><p>ee-pool.contoso.com</p></td>
<td><p>DNS Ein Eintrag für die ee-pool.contoso.com, der in die VIP-Adresse des Load Balancers aufgelöst wird, der von den Front -End-Servern verwendet wird.</p>
<p>DNS Ein Eintrag für webcon.contoso.com, der in die VIP-Adresse des Load Balancers aufgelöst wird, der von den Front -End-Servern verwendet wird.</p></td>
</tr>
<tr class="even">
<td><p>ee-pool.contoso.com</p></td>
<td><p>ee-pool.contoso.com</p></td>
<td><p>DNS Ein Eintrag für ee-pool.contoso.com, der in die virtuelle IP-Adresse (VIP) des Load Balancers aufgelöst wird, der von den Enterprise Edition Front End-Servern im Front -End-Pool verwendet wird.</p>
<p>Beachten Sie, dass ihr Front -End-Pool und die interne Webfarm nicht über denselben FQDN verfügen können, wenn Sie den DNS-Lastenausgleich für diesen Pool verwenden.</p></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</div>

