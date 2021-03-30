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

_**Thema Zuletzt geändert:** 27.03.2014_

Wenn Sie Sie bereits edgeserver oder -server bereitgestellt haben, wird das Hinzufügen der Features für Verbundszenarien sofort ausgeführt. Wenn Sie keine Edgeserver eingerichtet haben, müssen Sie dies zuerst tun. Ausführliche Informationen finden Sie unter Planen des Externen [Benutzerzugriffs in Lync Server 2013](lync-server-2013-planning-for-external-user-access.md) in der Planungsdokumentation und Bereitstellen des externen Benutzerzugriffs in Lync Server [2013](lync-server-2013-deploying-external-user-access.md) in der Bereitstellungsdokumentation.

<div>


> [!NOTE]  
> Wenn Sie eine beliebige Kombination aus XMPP-Verbund, Lync-Verbund oder öffentlicher Chatverbindung einrichten möchten, können Sie diese gleichzeitig oder gleichzeitig bereitstellen. Wenn Sie die Optionen über den Topologie-Generator und die Lync Server-Verwaltungsshell konfigurieren und dann den Bereitstellungs-Assistenten auf dem Edgeserver ausführen, nachdem Sie die Optionen für einen, zwei oder alle drei Verbundtypen konfiguriert haben, können Sie die Anzahl der erforderlichen Schritte verringern.



</div>

<div>

## <a name="setting-up-lync-federation-in-topology-builder-and-the-deployment-wizard"></a>Einrichten des Lync-Verbunds im Topologie-Generator und im Bereitstellungs-Assistenten

1.  Öffnen Sie auf einem Front -End-Server den Topologie-Generator. Erweitern Sie Edgepools, und klicken Sie dann mit der rechten Maustaste auf Ihren Edgeserver oder Edgeserverpool. Wählen Sie Eigenschaften bearbeiten aus.

2.  Wählen Sie unter Eigenschaften bearbeiten unter Allgemein die Option Verbund für diesen Edgepool aktivieren (Port 5061) aus. Klicken Sie auf OK.

3.  Klicken Sie auf Aktion, wählen Sie Topologie und dann Veröffentlichen aus. Wenn Sie unter Topologie veröffentlichen aufgefordert werden, klicken Sie auf Weiter. Wenn die Veröffentlichung abgeschlossen ist, klicken Sie auf Fertig stellen.

4.  Öffnen Sie auf dem Edgeserver den Lync Server-Bereitstellungs-Assistenten. Klicken Sie auf Installieren oder Aktualisieren von Lync Server System, und klicken Sie dann auf Einrichten oder Entfernen von Lync Server-Komponenten. Klicken Sie auf Erneut ausführen.

5.  Klicken Sie bei Setup von Lync Server-Komponenten auf Weiter. Im Zusammenfassungsbildschirm werden Aktionen angezeigt, während sie ausgeführt werden. Nachdem die Bereitstellung erfolgt ist, klicken Sie auf Protokoll anzeigen, um die verfügbaren Protokolldateien anzeigen zu können. Klicken Sie auf Fertig stellen, um die Bereitstellung zu beenden.
    
    <div>
    

    > [!IMPORTANT]  
    > Sie können diese Option auswählen, aber nur ein Edgepool oder Edgeserver in Ihrer Organisation kann extern für den Verbund veröffentlicht werden. Alle Zugriffe von Verbundbenutzern, einschließlich Der Benutzer von öffentlichen Chatnachrichten, werden über denselben Edgepool oder einen einzelnen Edgeserver ausgeführt. Wenn Ihre Bereitstellung z. B. einen Edgepool oder einen einzelnen Edgeserver enthält, der in New York bereitgestellt wurde, und ein in London bereitgestellter Server und Sie die Verbundunterstützung für den New York Edge-Pool oder einen einzelnen Edgeserver aktivieren, wird der Signalverkehr für Verbundbenutzer über den New York Edge-Pool oder einen einzelnen Edgeserver ausgeführt. Dies gilt auch für die Kommunikation mit Benutzern in London, wenngleich ein interner Benutzer in London, der einen Partnerbenutzer in London anruft, für den A/V-Datenverkehr den Pool oder Edgeserver in London verwendet.

    
    </div>

</div>

<div>

## <a name="configuring-federation-with-partners"></a>Konfigurieren des Verbunds mit Partnern

1.  Wenn Sie einen erfolgreichen Verbund mit einem anderen Microsoft Lync Server 2013, Lync Server 2010, Office Communications Server 2007 R2 oder Office Communicator 2007 einrichten möchten, wählen Sie den Typ des Verbunds aus der folgenden Tabelle aus, definieren DNS SRV-Einträge, DNS-Host (A oder AAAA für IPv6) und konfigurieren Richtlinien, die für den Typ des Verbunds gelten:
    
    
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
    <td><p>Konfigurieren Sie den SRV-Eintrag des Formats _sipfederationtls._tcp. &lt; Name der externen Domäne Wenn der Portwert für den SRV-Eintrag TCP 5061 ist und der Host, der diesen Dienst &gt; bietet, als sip definiert ist. <strong></strong> &lt;Name der externen &gt; Domäne – der FQDN Ihres Access Edge-Diensts. Details zum Erstellen des SRV-Eintrags finden Sie unter Konfigurieren von DNS für Edgeunterstützung <a href="lync-server-2013-configure-dns-for-edge-support.md">in Lync Server 2013.</a></p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Aktivieren oder Deaktivieren des Partnerverbunds und der Konnektivität mit öffentlichen Chatdiensten in Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-enable-or-disable-discovery-of-federation-partners.md">Aktivieren oder Deaktivieren der Suche von Verbundpartnern in Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>Frühere Versionen haben diesen Verbundtyp als <strong>Erweiterter Verbund öffnen bezeichnet.</strong> Die Erstellung des SRV-Eintrags ist für diesen Verbundtyp erforderlich und soll es anderen Partnern ermöglichen, Ihren Verbund zu entdecken.</p></td>
    </tr>
    <tr class="even">
    <td><p>Zulässige Partnerdomäne</p></td>
    <td><p>Konfigurieren Sie den SRV-Eintrag des Formats _sipfederationtls._tcp. &lt; Name der externen Domäne Wenn der Portwert für den SRV-Eintrag TCP 5061 ist und der Host, der diesen Dienst &gt; bietet, als sip definiert ist. <strong></strong> &lt;Name der externen &gt; Domäne – der FQDN Ihres Access Edge-Diensts. Details zum Erstellen des SRV-Eintrags finden Sie unter Konfigurieren von DNS für Edgeunterstützung <a href="lync-server-2013-configure-dns-for-edge-support.md">in Lync Server 2013.</a></p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Aktivieren oder Deaktivieren des Partnerverbunds und der Konnektivität mit öffentlichen Chatdiensten in Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>Frühere Versionen bezeichneten diesen Verbundtyp als <strong>Erweiterter Verbund</strong>. Die Erstellung des SRV-Eintrags ist für diese Art von Verbund optional und soll es anderen Partnern ermöglichen, Ihren Verbund zu entdecken. Natürlich handelt es sich dann um einen <strong>erweiterten Open Federation</strong>oder <strong>eine "Discovered Partner Domain".</strong></p></td>
    </tr>
    <tr class="odd">
    <td><p>Zulässiger Partnerserver</p></td>
    <td><p>Konfigurieren des SIP-Domänennamens und des Partner Edge Server FQDNs als Verbundpartner in Richtlinien</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Aktivieren oder Deaktivieren des Partnerverbunds und der Konnektivität mit öffentlichen Chatdiensten in Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-configure-support-for-allowed-external-domains.md">Konfigurieren der Unterstützung für zulässige externe Domänen in Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-configure-support-for-blocked-external-domains.md">Konfigurieren der Unterstützung für blockierte externe Domänen in Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>Dieser Verbundtyp ist die Definition einer 1:1-Beziehung und ermöglicht keine Suche nach anderen Partnerverbundpartnern. Jeder Partnerverbund ist explizit konfiguriert. In früheren Versionen wurde dies als <strong>"Direkter Verbund"</strong></p></td>
    </tr>
    <tr class="even">
    <td><p>Hostinganbieter und öffentlicher IM-Anbieter</p></td>
    <td><p>Für diesen Verbundtyp sind keine speziellen DNS-Anforderungen definiert.</p></td>
    <td><ul>
    <li><p><a href="lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md">Aktivieren oder Deaktivieren des Partnerverbunds und der Konnektivität mit öffentlichen Chatdiensten in Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-create-or-edit-public-sip-federated-providers.md">Erstellen oder Bearbeiten von öffentlichen SIP-Partnerverbundanbietern in Lync Server 2013</a></p></li>
    <li><p><a href="lync-server-2013-create-or-edit-hosted-sip-federated-providers.md">Erstellen oder Bearbeiten von gehosteten SIP-Verbundanbietern in Lync Server 2013</a></p></li>
    </ul></td>
    <td><p>Dieser Verbundtyp definiert Dienste und Hostinganbieter, die Sie für Ihre Benutzer konfigurieren möchten. Typische Verwendungsmöglichkeiten sind die Konfiguration für öffentliche Windows Live Messenger, Yahoo! und AOL sowie Hostinganbieter wie Lync Online und Microsoft 365</p>
    <div>

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P>Seit dem 1. September 2012 steht die Microsoft Lync Public IM Connectivity User Subscription License ("PIC USL") für neue oder verlängernde Verträge nicht mehr zum Kauf zur Verfügung. Kunden mit aktiven Lizenzen können weiterhin eine Zusammenarbeit mit Yahoo! Messenger bis zum Herunterfahren des Diensts. Ende des Lebenszyklus von Juni 2014 für AOL und Yahoo! wurde angekündigt. Details finden Sie unter <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support für die Konnektivität mit öffentlichen Chatnachrichten in Lync Server 2013.</A></P>
    > <LI>
    > <P>Die PIC USL ist eine Abonnementlizenz pro Benutzer pro Monat, die erforderlich ist, damit Lync Server oder Office Communications Server mit Yahoo! zusammenarbeiten können. Messenger. Die Fähigkeit von Microsoft, diesen Dienst zur Verfügung zu stellen, hängt von der Unterstützung von Yahoo! ab, der zugrunde liegenden Vereinbarung, für die der Vertrag geschlossen wird.</P>
    > <LI>
    > <P>Lync ist mehr denn je ein leistungsfähiges Tool für die Verbindung zwischen Organisationen und Einzelpersonen auf der ganzen Welt. Der Verbund mit Windows Live Messenger erfordert keine zusätzlichen Benutzer-/Gerätelizenzen über die Lync Standard CAL hinaus. Der Skype-Verbund wird dieser Liste hinzugefügt, sodass Lync-Benutzer Hunderte von Millionen von Personen mit Chat und Sprache erreichen können.</P></LI></UL>


    </div></td>
    </tr>
    </tbody>
    </table>


2.  Definieren und Konfigurieren der erforderlichen DNS-Host-Einträge (A oder AAAA für IPv6) und DNS SRV-Einträge

3.  Definieren und konfigurieren Sie alle Richtlinien mithilfe der Lync Server-Systemsteuerung oder mithilfe der Lync Server-Verwaltungsshell und der entsprechenden Cmdlets. Details zu den Lync Server Management Shell-Cmdlets finden Sie unter Verbund- und externe [Zugriffs-Cmdlets in Lync Server 2013.](https://docs.microsoft.com/powershell/module/skype/)
    
    <div>
    

    > [!NOTE]  
    > Lync Room System (LRS) zeigt keine Teilnahmeschaltfläche für Besprechungen an, die von Organisatoren in Partnerpartnern von Lync gesendet wurden. Damit ein Besprechungsverknüpfungslink auf LRS angezeigt wird, muss die sendende Organisation TNEF mithilfe des folgenden Cmdlets aktivieren:<BR><BR><CODE>New-RemoteDomain -DomainName Contoso.com -Name Contoso</CODE><BR><CODE>Set-RemoteDomain -Identity Contoso -TNEFEnabled $true</CODE><BR>Beachten Sie, dass dies nicht LRS-spezifisch ist. Outlook und Lync würden in diesem Fall auch keine Verknüpfungen für die Teilnahme anzeigen, da die MAPI-Eigenschaften nicht transportiert werden, aber im Fall von Outlook kann der Benutzer die Besprechungs-Einladung öffnen und auf die Besprechungs-URL klicken. Wenn TNEFEnabled auf true festgelegt ist Exchange 2013 entfernt keine MAPI-Eigenschaften, einschließlich OnlineMeetingExternalLink, und die Schaltfläche Beitreten wird in der Erinnerung angezeigt.

    
    </div>

</div>

<div>

## <a name="see-also"></a>Siehe auch


[Planen von SIP, XMPP-Verbund und öffentlichem Chat in Lync Server 2013](lync-server-2013-planning-for-sip-xmpp-federation-and-public-instant-messaging.md)  
[Verwalten von Partnerverbünden und externem Zugriff auf Lync Server 2013](lync-server-2013-managing-federation-and-external-access-to-lync-server-2013.md)  
  

</div>

</div>

<span> </span>

</div>

</div>

</div>

