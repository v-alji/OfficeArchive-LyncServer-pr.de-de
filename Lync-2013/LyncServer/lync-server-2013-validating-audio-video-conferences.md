---
title: 'Lync Server 2013: Überprüfen von Audio-und Videokonferenzen'
description: 'Lync Server 2013: Überprüfen von Audio-und Videokonferenzen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating audio/video conferences
ms:assetid: 6c8c422a-d501-42cb-820b-b002f9b2250b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720915(v=OCS.15)
ms:contentKeyID: 63969615
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad12611e928a64b934252ec21c18b98366e0912b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443489"
---
# <a name="validating-audiovideo-conferences-in-lync-server-2013"></a>Überprüfen von Audio-und Videokonferenzen in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2014-06-05_


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p>Überprüfungszeitplan</p></td>
<td><p>Täglich</p></td>
</tr>
<tr class="odd">
<td><p>Test Tool</p></td>
<td><p>Windows PowerShell</p></td>
</tr>
<tr class="even">
<td><p>Erforderliche Berechtigungen</p></td>
<td><p>Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</p>
<p>Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsAVConference-Cmdlets verfügt. Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsAVConference&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Beschreibung

Das Test-CsAVConference-Cmdlet überprüft, ob zwei Testbenutzer an einer Audio/Video-Konferenz (A/V) teilnehmen können. Wenn das Cmdlet ausgeführt wird, sind die beiden Benutzer am System angemeldet. Nachdem Sie sich erfolgreich angemeldet haben, erstellt der erste Benutzer eine A/V-Konferenz und wartet dann auf die Teilnahme des zweiten Benutzers an dieser Konferenz. Nach einem kurzen Datenaustausch wird die Konferenz gelöscht, und die beiden Testbenutzer werden abgemeldet.

Beachten Sie, dass Test-CsAVConference keine eigentliche A/V-Konferenz zwischen den beiden Testbenutzern durchführt. Stattdessen überprüft das Cmdlet, ob die beiden Benutzer alle erforderlichen Verbindungen zum Durchführen einer solchen Konferenz vornehmen können.

Weitere Beispiele für diesen Befehl finden Sie unter [Test-CsAVConference](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference).

</div>

<div>

## <a name="running-the-test"></a>Ausführen des Tests

Das Test-CsAVConference-Cmdlet kann entweder mit einem Paar vorkonfigurierter Testkonten ausgeführt werden (siehe Einrichten von Testkonten zum Ausführen von lync Server-Tests) oder der Konten von zwei Benutzern, die für lync Server aktiviert sind. Um diese Prüfung mit Testkonten auszuführen, müssen Sie lediglich den FQDN des zu testenden lync-Server Pools angeben. Beispiel:

    Test-CsAVConference -TargetFqdn "atl-cs-001.litwareinc.com"

Damit diese Überprüfung mit tatsächlichen Benutzerkonten ausgeführt werden kann, müssen Sie für jedes Konto zwei Windows PowerShell-Anmeldeinformationsobjekte (Objekte, die den Kontonamen und das Kennwort enthalten) erstellen. Sie müssen dann diese Anmeldeinformationsobjekte und die SIP-Adressen der beiden Konten einbeziehen, wenn Sie Test-CsAVConference aufrufen:

    $credential1 = Get-Credential "litwareinc\kenmyer"
    $credential2 = Get-Credential "litwareinc\davidlongmire"
    Test-CsAVConference -TargetFqdn "atl-cs-001.litwareinc.com" -SenderSipAddress "sip:kenmyer@litwareinc.com" -SenderCredential $credential1 -ReceiverSipAddress "sip:davidlongmire@litwareinc.com" -ReceiverCredential $credential2

Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsAVConference](https://docs.microsoft.com/powershell/module/skype/Test-CsAVConference) .

</div>

<div>

## <a name="determining-success-or-failure"></a>Ermitteln von Erfolg oder Misserfolg

Wenn die angegebenen Benutzer eine A/V-Konferenz erfolgreich abschließen können, erhalten Sie eine ähnliche Ausgabe, wobei die Eigenschaft Ergebnis als erfolgreich markiert ist **:**

TargetFqdn: ATL-CS-001.litwareinc.com

Ergebnis: Erfolg

Latenz: 00:00:02.6841765

Fehler

Diagnose

Wenn die Benutzer die Konferenz nicht abschließen können, wird das Ergebnis als Fehler angezeigt, und weitere Informationen werden in den Eigenschaften Fehler und Diagnose aufgezeichnet:

TargetFqdn: ATL-CS-001.litwareinc.com

Ergebnis: Fehler

Latenz: 00:00:00

Fehler: 404, nicht gefunden

Diagnose: errorCode = 4005, Source = ATL-CS-001.litwareinc.com,

Reason = Ziel-URI ist entweder für SIP nicht aktiviert oder nicht

existieren.

Microsoft. RTC. Signalisierungs-DiagnosticHeader

In der vorherigen Ausgabe wird beispielsweise festgestellt, dass der Test fehlgeschlagen ist, weil mindestens eines der beiden Benutzerkonten ungültig war, weil das Konto nicht vorhanden ist oder weil das Konto für lync Server nicht aktiviert wurde. Sie können überprüfen, ob die beiden Testkonten vorhanden sind und ob Sie für lync Server aktiviert wurden, indem Sie einen Befehl wie den folgenden ausführen:

    "sip:kenmyer@litwareinc.com","sip:davidlongmire@litwareinc.com" | Get-CsUser | Select-Object SipAddress, enabled

Wenn Test-CsAVConference fehlschlägt, möchten Sie möglicherweise den Test erneut ausführen, wobei dieser Zeitpunkt einschließlich des Verbose-Parameters lautet:

    Test-CsAVConference -TargetFqdn "atl-cs-001.litwareinc.com" -Verbose

Wenn der Verbose-Parameter enthalten ist Test-CsAVConference gibt eine Schritt-für-Schritt-Konto für jede Aktion zurück, die versucht wurde, als die Möglichkeit der angegebenen Benutzer zur Teilnahme an einer AV-Konferenz geprüft wurde. Nehmen wir beispielsweise an, dass Ihr Test fehlschlägt und Sie die folgende Diagnose erhalten:

ErrorCode = 1008, Source = accessproxy. "litwareinc. com; Reason = DNS-SRV-Eintrag konnte nicht aufgelöst werden

Wenn Sie den Test mit dem Verbose-Parameter erneut ausführen, beinhalten die zurückgegebenen schrittweisen Informationen eine Ausgabe, die der folgenden ähnelt:

Ausführlich: die Aktivität "registrieren" wurde gestartet.

Registrierungsanfrage wird gesendet:

Ziel-FQDN = ATL-CS-001.litwareinc.com

SIP-Adresse des Benutzers = SIP:davidlongmire@litwareinc.com

Registrar Port = 5061.

Auth-Typ "vertrauenswürdig" ist ausgewählt.

Die Aktivität "registrieren" wurde gestartet.

Registrierungsanfrage wird gesendet:

Ziel-FQDN = ATL-CS-001.litwareinc.com

SIP-Adresse des Benutzers = SIP:kenmyer@litwareinc.com

Registrar Port = 5061.

Auth-Typ "vertrauenswürdig" ist ausgewählt.

Eine Ausnahme "der Endpunkt konnte nicht registriert werden. Lesen Sie den ErrorCode aus bestimmten Gründen. während des Workflows aufgetreten

Die letzte Zeile in dieser Ausgabe gibt an, dass der Benutzer SIP:kenmyer@litwareinc.com sich nicht bei lync Server registrieren konnte. Das bedeutet, dass Sie überprüfen sollten, ob die SIP-Adresse SIP:kenmyer@litwareinc.com gültig ist und dass der zugeordnete Benutzer für lync Server aktiviert ist.

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Gründe, warum der Test fehlgeschlagen ist

Im folgenden finden Sie einige häufige Gründe, warum Test-CsAVConference fehlschlagen kann:

  - Sie haben ein ungültiges Benutzerkonto angegeben. Sie können überprüfen, ob ein Benutzerkonto vorhanden ist, indem Sie einen Befehl wie den folgenden ausführen:
    
        Get-CsUser "sip:kenmyer@litwareinc.com"

  - Das Benutzerkonto ist gültig, das Konto ist derzeit aber für lync Server nicht aktiviert. Führen Sie einen Befehl ähnlich der folgenden aus, um zu überprüfen, ob ein Benutzerkonto für lync Server aktiviert ist:
    
        Get-CsUser "sip:kenmyer@litwareinc.com" | Select-Object Enabled
    
    Wenn die Enabled-Eigenschaft auf false festgelegt ist, bedeutet dies, dass der Benutzer zurzeit nicht für lync Server aktiviert ist.

</div>

</div>

<span> </span>

</div>

</div>

</div>

