---
title: 'Lync Server 2013: Einrichten eines Lync-Partnerverbunds'
description: 'Lync Server 2013: Einrichten des Lync-Verbunds.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Lync federation
ms:assetid: 374ddc43-26f9-499d-be68-a5158adfa49c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204800(v=OCS.15)
ms:contentKeyID: 48183822
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 382def41635f05525e5b047e97febffdb069da2a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395067"
---
# <a name="setting-up-lync-federation-in-lync-server-2013"></a>Einrichten eines Lync-Partnerverbunds in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Zuletzt geändertes Thema:** 27.03.2014_

Wenn Sie Ihre Edgeserver bereits bereitgestellt haben, können Sie die Features für Verbundszenarien direkt hinzufügen. Wenn Sie noch keine Edgeserver eingerichtet haben, müssen Sie dies zuerst tun. Ausführliche Informationen finden Sie unter: Planen des Zugriffs für externe Benutzer [in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in der Dokumentation zur Planung und Bereitstellen des Zugriffs externer Benutzer [in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) in der Bereitstellungsdokumentation.

<div>


> [!NOTE]  
> Wenn Sie eine beliebige Kombination aus XMPP-Verbund, Lync-Verbund oder öffentlicher Chatkonnektivität einrichten möchten, können Sie diese gleichzeitig oder gleichzeitig bereitstellen. Wenn Sie die Optionen über den Topologie-Generator und die Lync Server-Verwaltungsshell konfigurieren und dann den Bereitstellungsassistenten auf dem Edgeserver ausführen, nachdem Sie die Optionen für einen, zwei oder alle drei Verbundtypen konfiguriert haben, können Sie die Anzahl der erforderlichen Schritte verringern.



</div>

<div>

## <a name="setting-up-lync-federation-in-topology-builder-and-the-deployment-wizard"></a>Einrichten des Lync-Verbunds im Topologie-Generator und im Bereitstellungsassistenten

1.  Öffnen Sie den Topology Builder auf einem Front-End-Server. Erweitern Sie Edgepools, und klicken Sie dann mit der rechten Maustaste auf Den Edgeserver oder Edgeserverpool. Wählen Sie "Eigenschaften bearbeiten" aus.

2.  Wählen Sie in "Eigenschaften bearbeiten" unter "Allgemein" die Option "Verbund für diesen Edgepool aktivieren" (Port 5061) aus. Klicken Sie auf OK.

3.  Klicken Sie auf "Aktion", wählen Sie "Topologie" und dann "Veröffentlichen" aus. Wenn Sie zum Veröffentlichen der Topologie aufgefordert werden, klicken Sie auf "Weiter". Wenn die Veröffentlichung abgeschlossen ist, klicken Sie auf "Fertig stellen".

4.  Öffnen Sie auf dem Edgeserver den Lync Server-Bereitstellungs-Assistenten. Klicken Sie auf "Lync Server System installieren oder aktualisieren", und klicken Sie dann auf "Lync Server-Komponenten einrichten" oder "Entfernen". Klicken Sie auf "Erneut ausführen".

5.  Klicken Sie beim Einrichten von Lync Server-Komponenten auf "Weiter". Im Zusammenfassungsbildschirm werden Aktionen angezeigt, während sie ausgeführt werden. Nachdem die Bereitstellung erfolgt ist, klicken Sie auf "Protokoll anzeigen", um die verfügbaren Protokolldateien anzeigen. Klicken Sie auf "Fertig stellen", um die Bereitstellung fertig zu stellen.
    
    <div>
    

    > [!IMPORTANT]  
    > Sie können diese Option auswählen, aber nur ein Edgepool oder Edgeserver in Ihrer Organisation kann extern für den Verbund veröffentlicht werden. Der zugriff durch Partnerbenutzer, einschließlich der Benutzer öffentlicher Chats, durch denselben Edgepool oder einen einzelnen Edgeserver. Wenn Ihre Bereitstellung z. B. einen Edgepool oder einen einzelnen Edgeserver umfasst, der in New York bereitgestellt wurde, und ein in London bereitgestellter Server, und Sie Verbundunterstützung für den New YorkEr Edge pool oder einen einzelnen Edgeserver aktivieren, wird der Signaldatenverkehr für Partnerbenutzer durch den New YorkEr Edgepool oder einen einzelnen Edgeserver durchgehen. Dies gilt auch für die Kommunikation mit Benutzern in London, wenngleich ein interner Benutzer in London, der einen Partnerbenutzer in London anruft, für den A/V-Datenverkehr den Pool oder Edgeserver in London verwendet.

    
    </div>

</div>

<div>

## <a name="configuring-federation-with-partners"></a>Konfigurieren des Partnerverbunds

1.  Zum Einrichten eines erfolgreichen Verbunds mit einem anderen Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2 oder Office Communicator 2007 wählen Sie den Typ des Verbunds aus der folgenden Tabelle aus, definieren DNS SRV-Einträge, den DNS-Host (A oder AAAA für IPv6) und konfigurieren Richtlinien für den Verbundtyp:
    
    
    <table>
    <colgroup>
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    <col style="width: 25%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th>Verbundtyp</th>
    <th>DNS Records</th>
    <th>Richtliniendefinition</th>
    <th>Hinweise</th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p>Ermittelte Partnerdomäne</p></td>
    <td><p>Konfigurieren Sie den SRV-Eintrag des Formats _sipfederationtls._tcp. &lt; Name der externen Domäne, wobei der Portwert für den SrV-Eintrag TCP 5061 ist und der Host, der diesen Dienst &gt; bietet, als sip definiert ist. <strong></strong> &lt;Externer Domänenname &gt; – der FQDN Ihres Access Edge-Diensts. Details zum Erstellen des SrV-Eintrags finden Sie unter "Konfigurieren von DNS für die Edgeunterstützung <a href="lync-server-2013-configure-dns-for-edge-support.md">in Lync Server 2013".</a></p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Aktivieren oder Deaktivieren des Partnerverbunds und der Konnektivität mit öffentlichen Chatdiensten in Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Aktivieren oder Deaktivieren der Suche von Verbundpartnern in Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>In früheren Versionen wurde dieser Verbundtyp als <strong>"Erweiterter Verbund öffnen" bezeichnet.</strong> Die Erstellung des SrV-Eintrags ist für diesen Verbundtyp erforderlich und soll es anderen Partnern ermöglichen, Ihren Partnerverbund zu ermitteln.</p></td>
    </tr>
    <tr class="even">
    <td><p>Zulässige Partnerdomäne</p></td>
    <td><p>Konfigurieren Sie den SRV-Eintrag des Formats _sipfederationtls._tcp. &lt; Name der externen Domäne, wobei der Portwert für den SrV-Eintrag TCP 5061 ist und der Host, der diesen Dienst &gt; bietet, als sip definiert ist. <strong></strong> &lt;Externer Domänenname &gt; – der FQDN Ihres Access Edge-Diensts. Details zum Erstellen des SrV-Eintrags finden Sie unter "Konfigurieren von DNS für die Edgeunterstützung <a href="lync-server-2013-configure-dns-for-edge-support.md">in Lync Server 2013".</a></p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Aktivieren oder Deaktivieren des Partnerverbunds und der Konnektivität mit öffentlichen Chatdiensten in Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>In früheren Versionen wurde dieser Verbundtyp als erweiterter <strong>Verbund bezeichnet.</strong> Die Erstellung des SrV-Eintrags ist für diesen Verbundtyp optional und soll es anderen Partnern ermöglichen, Ihren Partnerverbund zu ermitteln. Dies ist natürlich eine Open <strong>Enhanced Federation-Domäne</strong>oder eine <strong>ermittelte Partnerdomäne.</strong></p></td>
    </tr>
    <tr class="odd">
    <td><p>Zugelassener Partnerserver</p></td>
    <td><p>Konfigurieren Des SIP-Domänennamens und des FQDNs des Edgeserverpartners als Verbundpartner in Richtlinien</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Aktivieren oder Deaktivieren des Partnerverbunds und der Konnektivität mit öffentlichen Chatdiensten in Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Konfigurieren der Unterstützung für zulässige externe Domänen in Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Konfigurieren der Unterstützung für blockierte externe Domänen in Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>Bei diesem Verbundtyp handelt es sich um die Definition einer 1:1-Beziehung, bei der keine anderen Partnerverbundpartner entdeckt werden können. Jeder Verbundpartner ist explizit konfiguriert. In früheren Versionen wurde dies als direkter <strong>Verbund bekannt.</strong></p></td>
    </tr>
    <tr class="even">
    <td><p>Hostinganbieter und öffentlicher Imitanbieter</p></td>
    <td><p>Für diesen Verbundtyp sind keine spezifischen DNS-Anforderungen definiert.</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Aktivieren oder Deaktivieren des Partnerverbunds und der Konnektivität mit öffentlichen Chatdiensten in Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Erstellen oder Bearbeiten von öffentlichen SIP-Partnerverbundanbietern in Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Erstellen oder Bearbeiten von gehosteten SIP-Verbundanbietern in Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>Dieser Verbundtyp definiert Dienste und Hostinganbieter, die Sie für Ihre Benutzer konfigurieren möchten. Typische Verwendungsmöglichkeiten sind Konfigurationen für öffentliche Nachrichtenanbieter wie Windows Live Messenger, Yahoo! und AOL sowie Hostinganbieter wie Lync Online und Microsoft 365</p>
    <div>

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P>Seit dem 1. September 2012 steht die Microsoft Lync Public Im Connectivity User Subscription License ("PIC USL") für neue oder verlängerte Verträge nicht mehr zum Kauf zur Verfügung. Kunden mit aktiven Lizenzen können weiterhin mit Yahoo! Messenger bis zum Datum des Herunterfahrens des Diensts. Ende des Lebenszyklus von Juni 2014 für AOL und Yahoo! wurde angekündigt. Details finden Sie unter <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support für Verbindungen mit öffentlichen Chatnachrichten in Lync Server 2013.</A></P>
    > <LI>
    > <P>Bei der PIC USL handelt es sich um eine Monatsabonnementlizenz pro Benutzer, die erforderlich ist, damit Lync Server oder Office Communications Server mit Yahoo! Messenger. Die Fähigkeit von Microsoft, diesen Dienst zur Verfügung zu stellen, wurde nach dem Support von Yahoo!, der zugrunde liegenden Vereinbarung, nach unten geparkt.</P>
    > <LI>
    > <P>Mehr als je zuvor ist Lync ein leistungsfähiges Tool für die Verbindung zwischen Organisationen und Personen auf der ganzen Welt. Für einen Verbund mit Windows Live Messenger sind über die Lync Standard CAL hinaus keine weiteren Benutzer-/Gerätelizenzen erforderlich. Der Skype-Verbund wird dieser Liste hinzugefügt, sodass die Benutzer von Lync hunderte Millionen von Personen mit Chat und Sprache erreichen können.</P></LI></UL>


    </div></td>
    </tr>
    </tbody>
    </table>


2.  Definieren und Konfigurieren der erforderlichen DNS-Host- (A oder AAAA für IPv6) und DNS -SRV-Einträge

3.  Definieren und konfigurieren Sie alle Richtlinien mithilfe der Lync Server-Systemsteuerung oder mithilfe der Lync Server-Verwaltungsshell und der entsprechenden Cmdlets. Details zu den Lync Server-Verwaltungsshell-Cmdlets finden Sie in den Cmdlets für Verbund und externen Zugriff [in Lync Server 2013.](https://docs.microsoft.com/powershell/module/skype/)
    
    <div>
    

    > [!NOTE]  
    > Lync Room System (LRS) zeigt keine Schaltfläche "Teilnehmen" für Besprechungen an, die von Organisatoren in Partnerpartnern von Lync gesendet wurden. Damit ein Link zum Teilnehmen an einer Besprechung in LRS angezeigt wird, muss die sendende Organisation TNEF mithilfe des folgenden Cmdlets aktivieren:<BR><BR><CODE>New-RemoteDomain -DomainName Contoso.com -Name Contoso</CODE><BR><CODE>Set-RemoteDomain -Identity Contoso -TNEFEnabled $true</CODE><BR>Beachten Sie, dass dies nicht LRS-spezifisch ist. Outlook und Lync würden in diesem Fall ebenfalls keine Teilnahmelinks anzeigen, da die EIGENSCHAFTEN von MAPI nicht umverteilt werden, aber im Fall von Outlook kann der Benutzer die Besprechungs-Einladung öffnen und auf die Besprechungs-URL klicken. Wenn TNEFEnabled auf "True Exchange 2013" festgelegt ist, werden die MAPI-Eigenschaften, einschließlich OnlineMeetingExternalLink, nicht entfernt, und die Schaltfläche "Beitreten" wird in der Erinnerung angezeigt.

    
    </div>

</div>

<div>

## <a name="see-also"></a>Siehe auch


[Planen für SIP, XMPP-Verbund und öffentliche Chatnachrichten in Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md)  
[Verwalten von Partnerverbünden und externem Zugriff auf Lync Server 2013](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

