---
title: 'Lync Server 2013: Testen des Zugriffs auf mobile Benutzer'
description: 'Lync Server 2013: Testen des Zugriffs auf mobile Benutzer'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test mobile user access
ms:assetid: 81d97420-428b-41b7-91ef-185d572d3456
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767947(v=OCS.15)
ms:contentKeyID: 63969624
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e99a05e6ef9fe925126026452823e5edcc100ede
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441242"
---
# <a name="test-mobile-user-access-in-lync-server-2013"></a>Testen des Zugriffs von mobilen Benutzern in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2014-06-07_


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Überprüfungszeitplan</p></td>
<td><p>Monatlich</p></td>
</tr>
<tr class="even">
<td><p>Test Tool</p></td>
<td><p>Windows PowerShell</p></td>
</tr>
<tr class="odd">
<td><p>Erforderliche Berechtigungen</p></td>
<td><p>Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</p>
<p>Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsMcxConference-Cmdlets verfügt. Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsMcxConference&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Beschreibung

Mit dem Mobilitätsdienst können Benutzer mobiler Geräte wie folgt vorgehen:

1.  Tauschen Sie Sofortnachrichten und Anwesenheitsinformationen aus.

2.  Speichern und Abrufen von Voicemail intern und nicht mit Ihrem WLAN-Anbieter.

3.  Nutzen Sie die Vorteile von lync-Server Funktionen wie Anruf über Arbeit und Einwahlkonferenzen. Das Test-CsMcxConference-Cmdlet bietet eine schnelle und einfache Möglichkeit, um zu überprüfen, ob Benutzer teilnehmen und an lync Server-Konferenzen teilnehmen können, indem Sie ein mobiles Gerät verwenden.

</div>

<div>

## <a name="running-the-test"></a>Ausführen des Tests

Zum Ausführen dieser Prüfung müssen Sie für jedes Konto drei Windows PowerShell-Anmeldeinformationsobjekte (Objekte, die den Kontonamen und das Kennwort enthalten) erstellen. Sie müssen dann diese Anmeldeinformationsobjekte und die SIP-Adressen der beiden Konten einbeziehen, wenn Sie Test-CsMcxConference aufrufen, wie im folgenden Beispiel gezeigt:

    $organizerCred = Get-Credential "litwareinc\kenmyer"
    $user1Cred = Get-Credential "litwareinc\packerman"
    $user2Cred = Get-Credential "litwareinc\adelaney"
    
    Test-CsMcxConference -TargetFqdn "atl-cs-001.litwareinc.com" -Authentication Negotiate -OrganizerSipAddress "sip:kenmyer@litwareinc.com" -OrganizerCredential $organizerCred -UserSipAddress "sip:pilar@litwareinc.com" -UserCredential $user1Cred -User2SipAddress "sip:adelaney@litwareinc.com" -User2Credential $user2Cred

Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Test-CsMcxConference](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxConference) .

</div>

<div>

## <a name="determining-success-or-failure"></a>Ermitteln von Erfolg oder Misserfolg

Wenn die Überprüfung erfolgreich ist, meldet Test-CsMcxConference ein Testergebnis, das erfolgreich ist:

Ziel-FQDN: ATL-CS-001.litwareinc.com

Ziel-URI: http://atl-cs-001.litwareinc.com:443/mcx

Ergebnis: Erfolg

Latenz: 00:00:00

Fehlermeldung:

Diagnose

Wenn die Überprüfung nicht erfolgreich ist Test-CsMcxConference wird ein Testergebnis des Fehlers gemeldet. Dieses Testergebnis wird in der Regel von einer detaillierten Fehlermeldung und Diagnose begleitet. Beispiel:

Ziel-FQDN: ATL-CS-001.litwareinc.com

Ziel-URI: https://atl-cs-001.litwareinc.com:443/mcx

Ergebnis: Fehler

Latenz: 00:00:00

Fehlermeldung: für Web-Ticket Dienst wurde keine Antwort empfangen.

Innere Ausnahme: die HHTP-Anforderung ist mit dem Client nicht autorisiert

Aushandlungs Schema "NTLM". Der empfangene Authentifizierungsheader

vom Server war "Negotiate".

Innere Ausnahme: der Remoteserver hat einen Fehler zurückgegeben: (401)

Unbefugte.

Diagnose

Innere Diagnose: X-MS-Server-Fqdb: ATL-CS-001.litwareinc.com

Cache-Control: privat

Content-Type: Text/HTML; charset = UTF-8.

Server: Microsoft-IIS/8.5

WWW-Authenticate: Negotiate, NTLM

X-powered-by: ASP.net

X-Content-Type-Optionen: nosniff

Datum: Wed, 28 May 2014 19:22:19 GMT

Content-length: 6305

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Gründe, warum der Test fehlgeschlagen ist

Wenn Test-CsMcxConference fehlschlägt, sollten Sie zunächst überprüfen, ob der Mobilitätsdienst ausgeführt wird und auf den Sie zugreifen können. Dies kann mithilfe eines Webbrowsers erfolgen, um zu überprüfen, ob auf die Mobilitätsdienst-URL für Ihren lync Server-Pool zugegriffen werden kann. Mit diesem Befehl wird beispielsweise die URL für den Pool ATL-CS-001.litwareinc.com überprüft:

`https://atl-cs-001.litwareinc.com/mcx/mcxservice.svc`

Wenn Sie auf den Mobilitätsdienst zugreifen können, sollten Sie sicherstellen, dass die Testbenutzer über gültige lync Server-Konten verfügen. Sie können Kontoinformationen abrufen, indem Sie einen Befehl wie den folgenden verwenden:

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object Enabled

Wenn die Enabled-Eigenschaft nicht gleich true ist oder der Befehl fehlschlägt, bedeutet dies, dass der Benutzer kein gültiges lync Server-Konto hat. Sie sollten auch sicherstellen, dass jedes Benutzerkonto für Mobilität aktiviert ist. Ermitteln Sie dazu zunächst die Mobilitätsrichtlinie, die dem Konto zugewiesen ist:

    Get-CsUser -Identity "sip:kenmyer@litwareinc.com" | Select-Object MobilityPolicy

Nachdem Sie den Richtliniennamen bekannt haben, verwenden Sie das Get-CsMobilityPolicy-Cmdlet, um zu überprüfen, ob die EnableMobility-Eigenschaft auf die betreffende Richtlinie (beispielsweise RedmondMobilityPolicy) auf true festgelegt ist:

    Get-CsMobilityPolicy -Identity "RedmondMobilityPolicy"

Wenn Sie eine Fehlermeldung "Authentifizierungsheader" erhalten, wenn Sie Test-CsMcxConference ausführen, die häufig bedeutet, dass Sie kein gültiges Benutzerkonto angegeben haben, überprüfen Sie den Benutzernamen und das Kennwort, und versuchen Sie dann erneut, den Test zu testen. Wenn Sie davon überzeugt sind, dass das Benutzerkonto gültig ist, verwenden Sie das Get-CsWebServiceConfiguration-Cmdlet, und überprüfen Sie den Wert der UseWindowsAuth-Eigenschaft. Damit erfahren Sie, welche Authentifizierungsmethoden in Ihrer Organisation aktiviert sind.

Weitere Tipps zur Problembehandlung beim Mobilitätsdienst finden Sie im Blogbeitrag zur [Problembehandlung von externen lync-Mobilitäts Verbindungsproblemen Schritt-für-Schritt](https://blogs.technet.com/b/nexthop/archive/2012/02/21/troubleshooting-external-lync-mobility-connectivity-issues-step-by-step.aspx).

</div>

</div>

<span> </span>

</div>

</div>

</div>

