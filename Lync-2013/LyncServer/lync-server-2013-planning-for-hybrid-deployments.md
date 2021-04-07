---
title: 'Lync Server 2013: Planen von Hybridbereitstellungen'
description: 'Lync Server 2013: Planen von Hybridbereitstellungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for hybrid deployments
ms:assetid: f8b3d240-bc2e-42c9-acf8-d532d641a14c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205403(v=OCS.15)
ms:contentKeyID: 48185910
ms.date: 05/25/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 919f6058059fc9bfcb6bcb4f4c38140e53be6274
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424548"
---
# <a name="planning-for-lync-server-2013-hybrid-deployments"></a>Planen von Lync Server 2013-Hybridbereitstellungen

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Thema Zuletzt geändert:** 25.05.2016_

Bei der Planung einer Hybridbereitstellung sollten Sie die folgenden Anforderungen für Benutzer und Ihre Netzwerkinfrastruktur berücksichtigen.

<div>

## <a name="infrastructure-requirements"></a>Infrastrukturanforderungen

Sie müssen folgendes in Ihrer Umgebung konfiguriert haben, um eine Hybridbereitstellung implementieren und bereitstellen zu können.

  - Eine Microsoft 365- oder Office 365-Organisation mit aktivierter Skype for Business Online-Funktion. Beachten Sie, dass Sie bei ihrer lokalen Bereitstellung nur einen einzigen Mandanten für eine Hybridkonfiguration verwenden können.

  - Eine einzelne lokale Bereitstellung (Infrastruktur) von Skype for Business Server oder Lync Server, die in einer unterstützten Topologie bereitgestellt wird. Siehe Topologieanforderungen.
    
    Informationen zum Konfigurieren Ihrer Lync Server 2013- oder Lync Server 2010-Bereitstellung für hybride Bereitstellungen finden Sie unter Konfigurieren von [Lync Server 2013-Hybridbereitstellungen.](lync-server-2013-configuring-hybrid-deployments.md)

  - Skype for Business Server 2015-Verwaltungstools. Wenn Sie Lync Server 2013 oder Lync Server 2010 verwenden, können Sie die Lync Server 2013-Verwaltungstools verwenden.

  - Wenn Sie einmaliges Anmelden mit Microsoft 365 oder Office 365 unterstützen möchten, damit Benutzer dieselben Anmeldeinformationen für die Anmeldung bei Office verwenden können wie lokal, können Sie die Kennwortsynchronisierungsfunktionen von Azure Active Directory (AAD) Connect verwenden. Sie können Active Directory Federation Services (AD FS) auch zum einmaligen Anmelden mit Microsoft 365 oder Office 365 verwenden.
    
    Weitere Informationen finden Sie unter [Integrieren Ihrer lokalen Identitäten in Azure Active Directory.](https://go.microsoft.com/fwlink/p/?linkid=619754)

  - Eine Lösung für die Verzeichnissynchronisierung, um ihre lokalen und Online-Active Directory-Objekte zu synchronisieren. Details zur Verzeichnissynchronisierung finden Sie unter [Verzeichnisintegrationstools](https://go.microsoft.com/fwlink/p/?linkid=530320).

</div>

<div>

## <a name="lync-client-support"></a>Lync-Clientsupport

Es gibt einige Unterschiede bei den features, die in Lync-Clients unterstützt werden, sowie bei den Features, die in lokalen und Onlineumgebungen verfügbar sind. Bevor Sie entscheiden, wo Benutzer in Ihrer Organisation zu Hause sein möchten, können Sie den Clientsupport für die verschiedenen Konfigurationen von Lync Server anzeigen. Die folgenden Clients werden von Skype for Business Online in einer Lync-Hybridbereitstellung unterstützt:

  - Lync 2010

  - Lync 2013

  - Windows Store-App für Lync

  - Lync Web App

  - Lync Mobile

  - Lync für Mac 2011

  - Lync Room System

  - Lync Basic 2013

Details zum Clientsupport finden Sie in den folgenden Themen:

  - [Clients für Lync Online](https://go.microsoft.com/fwlink/?linkid=281902)

  - [Clientvergleichstabellen für Lync Server 2013](lync-server-2013-desktop-client-comparison-tables.md)

  - [Vergleichstabellen für mobile Clients für Lync Server 2013](lync-server-2013-mobile-client-comparison-tables.md)

</div>

<span id="BKMK_Topology"></span>

<div>

## <a name="topology-requirements"></a>Anforderungen im Hinblick auf die Topologie

Um Ihre Bereitstellung für die Hybridbereitstellung mit Skype for Business Online zu konfigurieren, benötigen Sie eine der folgenden unterstützten Topologien:

  - Eine Skype for Business Server 2015-Bereitstellung mit allen Servern, auf denen Skype for Business Server 2015 ausgeführt wird.

  - Eine Lync Server 2013-Bereitstellung mit allen Servern, auf denen Lync Server 2013 ausgeführt wird.

  - Eine Lync Server 2010-Bereitstellung mit allen Servern, auf denen Lync Server 2010 ausgeführt wird, mit den neuesten kumulativen Updates.
    
      - Der Edgeserver des Verbunds und der Server des nächsten Hops vom Edgeserver des Verbunds müssen Lync Server 2010 mit den neuesten kumulativen Updates ausführen.
    
      - Die Verwaltungstools für Skype for Business Server 2015 oder Lync Server 2013 müssen auf mindestens einem Server oder einer Verwaltungsarbeitsstation installiert sein.

  - Eine gemischte Bereitstellung von Lync Server 2013 und Skype for Business Server 2015 mit den folgenden Serverrollen auf mindestens einer Website, auf der Skype for Business Server 2015 ausgeführt wird:
    
      - Mindestens ein Enterprise-Pool- oder Standard Edition-Server 
    
      - Der dem SIP-Partnerverbund zugeordnete Director-Pool, falls vorhanden
    
      - Der dem SIP-Partnerverbund zugeordnete Edgepool

  - Eine gemischte Bereitstellung von Lync Server 2010 und Skype for Business Server 2015 mit den folgenden Serverrollen auf mindestens einer Website, auf der Skype for Business Server 2015 ausgeführt wird:
    
      - Mindestens ein Enterprise-Pool- oder Standard Edition-Server 
    
      - Der dem SIP-Partnerverbund zugeordnete Director-Pool, falls vorhanden
    
      - Der dem SIP-Partnerverbund zugeordnete Edgepool für den Standort

  - Eine gemischte Lync Server 2010- und Lync Server 2013-Bereitstellung mit den folgenden Serverrollen auf mindestens einer Website, auf der Lync Server 2013 ausgeführt wird:
    
      - Mindestens ein Enterprise-Pool- oder Standard Edition-Server am Standort
    
      - Der dem SIP-Partnerverbund zugeordnete Director-Pool, falls am Standort vorhanden
    
      - Der dem SIP-Partnerverbund zugeordnete Edgepool für den Standort

<div>


> [!IMPORTANT]  
> Alle Benutzerverwaltungen, einschließlich der Benutzerbewegungen zwischen lokal und UNRESOLVED_TOKEN_VAL(skypeforbusiness) Online, müssen mit der neuesten installierten Version der Verwaltungstools durchgeführt werden. Die Verwaltungstools müssen auf einem separaten Server installiert sein, der den Zugriff auf die vorhandene lokale Bereitstellung und das Internet verbindet. Das <A href="https://docs.microsoft.com/powershell/module/skype/Move-CsUser">Cmdlet "Move-CsUser",</A> um Benutzer von Ihrer lokalen Bereitstellung in UNRESOLVED_TOKEN_VAL(skype16_online) zu verschieben, muss über die verwaltungstechnischen Tools ausgeführt werden, die mit Ihrer lokalen Bereitstellung verbunden sind.



</div>

Weitere Informationen zu unterstützten Topologien finden Sie unter Unterstützte [Topologien in Lync Server 2013](lync-server-2013-supported-topologies.md)und [Lync Server 2013 Referenztopologien für Hybridbereitstellungen](https://go.microsoft.com/fwlink/p/?linkid=398709)in Unternehmen.

Informationen zur Problembehandlung zu Hybridbereitstellungen und zum Verbinden von PowerShell mit Lync Online finden Sie unter [Lync Online: Lync PowerShell und Hybrid troubleshooting](https://go.microsoft.com/fwlink/p/?linkid=306718).

</div>

<div>

## <a name="requirements-for-federation-allowedblocked-lists"></a>Anforderungen für "Verbund zugelassene/blockierte Listen"

Die Liste der zugelassenen Domänen enthält Domänen, für die ein Partner-Edge-FQDN (vollqualifizierter Domänenname) konfiguriert ist. Diese werden mitunter als *zulässige Partnerserver* oder *direkte Verbundpartner* bezeichnet. Sie sollten mit dem Unterschied zwischen einem öffentlichen Partnerverbund und einem geschlossenen Partnerverbund vertraut sein, der in lokalen Bereitstellungen als *Partnerermittlung* bzw. *Liste der zulässigen Partnerdomänen* bezeichnet wird.

Die folgenden Anforderungen müssen erfüllt sein, um eine Hybridbereitstellung erfolgreich zu konfigurieren:

  - Der Domänenabgleich muss für Ihre lokale Bereitstellung und Ihre Microsoft 365- oder Office 365-Organisation identisch konfiguriert sein. Wenn die Partnerermittlung für die lokale Bereitstellung aktiviert ist, muss der öffentliche Partnerverbund für den Onlinemandaten konfiguriert sein. Wenn die Partnerermittlung nicht aktiviert ist, muss für den Onlinemandanten der geschlossene Partnerverbund konfiguriert sein.

  - Die Liste der blockierten Domänen in der lokalen Bereitstellung muss genau mit der Liste der blockierten Domänen für den Onlinemandanten übereinstimmen.

  - Die Liste der zugelassenen Domänen in der lokalen Bereitstellung muss genau mit der Liste der zugelassenen Domänen für den Onlinemandanten übereinstimmen.

  - Der Verbund muss für die externe Kommunikation für den Online-Mandanten aktiviert sein, die mithilfe der Lync Online-Systemsteuerung konfiguriert wird.

</div>

<div>

## <a name="dns-settings"></a>DNS-Einstellungen

Beim Erstellen von DNS-Einträgen für Hybridbereitstellungen sollten alle externen Lync-DNS-Einträge auf die lokale Infrastruktur verweisen. Details zu den erforderlichen DNS-Einträgen finden Sie unter [Domänennamensystemanforderungen für Lync Server 2013](lync-server-2013-domain-name-system-dns-requirements.md).

Darüber hinaus müssen Sie sicherstellen, dass die in der folgenden Tabelle erläuterte DNS-Auflösung in Ihrer lokalen Bereitstellung funktioniert:


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>DNS-Eintrag</p></td>
<td><p>Aufzulösen durch</p></td>
<td><p>DNS-Anforderung</p></td>
</tr>
<tr class="even">
<td><p>DNS SRV-Eintrag für _sipfederationtls._tcp. &lt; sipdomain.com &gt; für alle unterstützten SIP-Domänen, die auf externe ACCESS Edge-IP(n) aufgelöst werden</p></td>
<td><p>Edgeserver</p></td>
<td><p>Aktivieren Sie Partnerverbundkommunikation in einer Hybridkonfiguration. Der Edgeserver muss wissen, wohin der Datenverkehr im Partnerverbund für die zwischen lokal und online aufgeteilte SIP-Domäne geleitet werden soll.</p></td>
</tr>
<tr class="odd">
<td><p>DNS-A-Eintrag/Einträge für den Edge-Webkonferenzdienst-FQDN, zum Beispiel „webcon.contoso.com“, aufgelöst zu der externen IP/den IPs des Webkonferenzdienst-Edgeservers</p></td>
<td><p>Über internes Unternehmensnetzwerk verbundene Benutzercomputer</p></td>
<td><p>Versetzen Sie Onlinebenutzer in die Lage, in lokal gehosteten Besprechungen Inhalte zu präsentieren oder zu betrachten. Entsprechende Inhalte sind unter anderem PowerPoint-Dateien, Whiteboards, Umfragen und freigegebene Notizen. </p></td>
</tr>
</tbody>
</table>


Je nachdem, wie DNS in Ihrer Organisation konfiguriert ist, müssen Sie möglicherweise der intern gehosteten DNS-Zone für die entsprechenden SIP-Domäne(n) diese Einträge hinzufügen, um die interne DNS-Auflösung dieser Datensätze zu gewährleisten.

</div>

<div>

## <a name="firewall-considerations"></a>Überlegungen zur Firewall

Die Computer in Ihrem Netzwerk müssen Standard-Internet-DNS-Lookups ausführen können. Wenn diese Computer Standard-Internetwebsites erreichen können, erfüllt Ihr Netzwerk diese Anforderung.

Je nach Standort ihres Microsoft Online Services-Rechenzentrums müssen Sie auch Ihre Netzwerkfirewallgeräte so konfigurieren, dass Verbindungen auf Der Grundlage von Platzhalterdomänennamen (z. B. der datenverkehr von \* .outlook.com) akzeptiert werden. Wenn die Firewalls Ihrer Organisation Konfigurationen mit Platzhalternamen nicht unterstützen, müssen Sie die IP-Adressbereiche, die Sie zulassen möchten, und die angegebenen Ports manuell festlegen.

Lesen Sie das Hilfethema [Office 365-URLs und IP-Adressbereiche.](https://go.microsoft.com/fwlink/p/?linkid=252942)

</div>

<span id="b"></span>

<div>

## <a name="port-and-protocol-requirements"></a>Port- und Protokollanforderungen

Zusätzlich zu den Portanforderungen für die interne Lync Server 2013-Kommunikation müssen Sie auch die folgenden Ports konfigurieren.


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th>Protokoll/Port</th>
<th>Anwendungen</th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>TCP 443</p></td>
<td><p>Eingehendes Öffnen</p>
<ul>
<li><p>Active Directory Federation Services (Verbundserverrolle)</p>
<p>Weitere Informationen finden Sie unter <a href="https://go.microsoft.com/fwlink/p/?linkid=281899">Grundlegendes zu AD FS Role Services</a>.</p></li>
<li><p>Active Directory Federation Services (Proxyserverrolle)</p></li>
<li><p>Microsoft Online Services Portal</p></li>
<li><p>Mein Unternehmensportal</p></li>
<li><p>Outlook Web App</p></li>
<li><p>Lync-Client (Kommunikation mit Lync Online vom lokalen Lync Server)</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p>TCP 80 und 443</p></td>
<td><p>Eingehendes Öffnen</p>
<ul>
<li><p>Microsoft Online Services-Verzeichnissynchronisierungstool</p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p>TCP 5061</p></td>
<td><p>Öffnen von Ein-/Ausgehend auf dem Edgeserver</p></td>
</tr>
<tr class="even">
<td><p>PSOM/TLS 443</p></td>
<td><p>Öffnen von Ein-/Ausgehend für Datenfreigabesitzungen</p></td>
</tr>
<tr class="odd">
<td><p>STUN/TCP 443</p></td>
<td><p>Öffnen von eingehenden/ausgehenden Audio-, Video- und Anwendungsfreigabesitzungen</p></td>
</tr>
<tr class="even">
<td><p>STUN/UDP 3478</p></td>
<td><p>Öffnen von Ein-/Ausgehend für Audio- und Videositzungen</p></td>
</tr>
<tr class="odd">
<td><p>RTP/TCP 50000-59999</p></td>
<td><p>Ausgehendes Öffnen für Audio- und Videositzungen</p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="user-accounts-and-data"></a>Benutzerkonten und Daten

In einer Lync Server 2013-Hybridbereitstellung muss jeder Benutzer, den Sie in Lync Online zu Hause haben möchten, zuerst in der lokalen Bereitstellung erstellt werden, damit das Benutzerkonto in Active Directory Domain Services erstellt wird. Sie können den Benutzer dann zu Skype for Business Online verschieben, wodurch die Kontaktliste des Benutzers bewegt wird.

Wenn Sie Benutzerkonten zwischen Ihren lokalen Lync- und Lync Online-Bereitstellungen mit AD FS und Dirsync synchronisieren, müssen Sie die AD-Konten für alle Lync-Benutzer in Ihrer Organisation zwischen Ihren lokalen und Online-Lync-Bereitstellungen synchronisieren, auch wenn Benutzer nicht nach Lync Online verschoben werden. Wenn Sie nicht alle Benutzer synchronisieren, funktioniert die Kommunikation zwischen lokalen und Onlinebenutzern in Ihrem Unternehmen möglicherweise nicht erwartungsgemäß.

<div>


> [!IMPORTANT]  
> Wenn der Benutzer mithilfe des Onlineportals für Microsoft 365 Admin Center erstellt wird, wird das Benutzerkonto nicht mit lokalem Active Directory synchronisiert, und der Benutzer ist im lokalen Active Directory nicht vorhanden. Wenn Sie bereits Benutzer in Lync Online erstellt haben und eine Hybridlösung mit einem lokalen Lync Server konfigurieren möchten, lesen Sie Verschieben von Benutzern von Lync Online zu Lync lokal <A href="lync-server-2013-moving-users-from-lync-online-to-lync-on-premises.md">in Lync Server 2013</A>.



</div>

Sie sollten bei der Planung einer Hybridbereitstellung auch die folgenden benutzerbezogenen Aspekte berücksichtigen.

  - **Benutzerkontakte**   Der Grenzwert für Kontakte für Lync Online-Benutzer beträgt 250. Alle darüber hinausgehenden Kontakte werden aus der Kontaktliste des Benutzers entfernt, wenn das Konto nach Lync Online verschoben wird.

  - **Chat und Anwesenheit**   Benutzerkontaktlisten, Benutzergruppen und Zugriffssteuerungslisten (ACLs) werden mit dem Benutzerkonto migriert.

  - **Konferenzdaten, Besprechungsinhalte und geplante Besprechungen**   Dieser Inhalt wird nicht mit dem Benutzerkonto migriert. Benutzer müssen Besprechungen neu planen, nachdem ihre Konten zu Lync Online migriert wurden.

</div>

<div>

## <a name="user-policies-and-features"></a>Benutzerrichtlinien und -features

  - In einer Lync Server 2013-Hybridumgebung können Benutzer für Chatnachrichten, Sprachnachrichten und Besprechungen lokal oder online aktiviert werden, jedoch nicht beide gleichzeitig.

  - **Lync-Client**    Einige Benutzer benötigen möglicherweise eine neue Clientversion, wenn sie nach Lync Online verschoben werden. Bei Office Communications Server 2007 R2 müssen Benutzer vor der Migration zu Lync Online in einen Lync Server 2013-Pool verschoben werden.
    
    Weitere Informationen zur Clientunterstützung finden Sie unter [Clients für Lync Online-](https://go.microsoft.com/fwlink/p/?linkid=281902) und [Unterstützte Lync-Clients und Netzwerkportkonfigurationen.](https://go.microsoft.com/fwlink/p/?linkid=281901)

  - **Lokale Richtlinien und Konfiguration (Nichtbenutzer)**   Online- und lokale Richtlinien erfordern eine separate Konfiguration. Sie können keine globalen Richtlinien festlegen, die für beide Umgebungen gelten.

</div>

</div>

<span> </span>

</div>

</div>

</div>
