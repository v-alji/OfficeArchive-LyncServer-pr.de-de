---
title: 'Lync Server 2013: Testen der Dienstaktivierung und Gruppen Berechtigungen'
description: 'Lync Server 2013: Testen der Dienstaktivierung und Gruppen Berechtigungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing service activation and group permissions
ms:assetid: 2c59e603-ba85-40ba-91a7-51c6fd39472e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn743833(v=OCS.15)
ms:contentKeyID: 63969594
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 116cf939f3110616ce395eb14c7945890bdb89b7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440983"
---
# <a name="testing-service-activation-and-group-permissions-in-lync-server-2013"></a>Testen der Dienstaktivierung und Gruppen Berechtigungen in lync Server 2013

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
<td><p>Überprüfungszeitplan</p></td>
<td><p>Täglich</p></td>
</tr>
<tr class="even">
<td><p>Test Tool</p></td>
<td><p>Windows PowerShell</p></td>
</tr>
<tr class="odd">
<td><p>Erforderliche Berechtigungen</p></td>
<td><p>Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</p>
<p>Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsTopology-Cmdlets verfügt. Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsTopology&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Beschreibung

Mit dem Test-CsTopology-Cmdlet können Sie überprüfen, ob lync Server 2013 im globalen Bereich ordnungsgemäß funktioniert. Das Cmdlet überprüft standardmäßig Ihre gesamte lync Server-Infrastruktur, überprüft, ob die erforderlichen Dienste ausgeführt werden und dass die entsprechenden Berechtigungen für diese Dienste und für die universellen Sicherheitsgruppen festgesetzt werden, die bei der Installation von lync Server erstellt werden.

Zusätzlich zur Überprüfung der Gültigkeit der lync Server-Installation können Sie Test-CsTopology auch die Gültigkeit eines bestimmten Diensts überprüfen. Dieser Befehl überprüft beispielsweise den Zustand des A/V-Konferenzservers im Pool ATL-CS-001.litwareinc.com:

    Test-CsTopology -Service "ConferencingServer:atl-cs-001.litwareinc.com"

</div>

<div>

## <a name="running-the-test"></a>Ausführen des Tests

Standardmäßig werden Test-CsTopology auf dem Bildschirm nur sehr wenig ausgegeben. Stattdessen werden vom Cmdlet zurückgegebene Informationen in eine HTML-Datei geschrieben. Mit dem Parameter Report können Sie einen Dateipfad und einen Dateinamen für die von Test-CsTopology generierte HTML-Datei angeben. Wenn Sie den Berichtsparameter nicht angeben, wird die HTML-Datei automatisch in Ihrem Ordner "Benutzer" gespeichert, und Sie erhalten einen ähnlichen Namen wie den folgenden: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.

Der folgende Beispielbefehl führt Test-CsTopology aus und speichert die Ausgabe in einer Datei mit dem Namen C: \\ Logs \\ComputerTest.html:

    Test-CsTopology -Report "C:\Logs\ComputerTest.html" -Verbose

Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsTopology](https://docs.microsoft.com/powershell/module/skype/Test-CsTopology) .

</div>

<div>

## <a name="determining-success-or-failure"></a>Ermitteln von Erfolg oder Misserfolg

Im Gegensatz zu den meisten Test-Cmdlets meldet Test-CsTopology Erfolg oder Misserfolg zurück. Dies ist teilweise auf die große Anzahl von Verifizierungs Prüfungen zurückzuführen, die das Cmdlet bei jeder Ausführung vornehmen muss. Stattdessen werden Daten in einem HTML-Bericht gespeichert, der dann mithilfe von Internet Explorer angezeigt werden kann.

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Gründe, warum der Test fehlgeschlagen ist

Im folgenden finden Sie einige häufige Gründe, warum Test-CsTopology fehlschlagen kann:

  - Die Replikation ist auf dem Testcomputer möglicherweise nicht auf dem neuesten Stand. Sie können den aktuellen Replikationsstatus für einen Computer überprüfen, indem Sie das Get-CsManagementStoreReplicationStatus-Cmdlet ausführen:
    
        Get-CsManagementStoreReplicationStatus -ReplicaFqdn "atl-cs-001.litwareinc.com"
    
    Wenn der Replikationsstatus nicht auf dem neuesten Stand ist, können Sie die Replikation manuell erzwingen, indem Sie einen ähnlichen Befehl wie den folgenden verwenden:
    
        Invoke-CsManagementStoreReplication -ReplicaFqdn "atl-cs-001.litwareinc.com"

  - Möglicherweise muss die Topologie aktiviert sein. Wenn Sie die lync Server-Topologie ändern (Änderungen, die sich auf den lokalen Computer auswirken könnten), müssen Sie die neue Topologie aktivieren. Sie können die Topologie jederzeit aktivieren, indem Sie den folgenden Befehl ausführen:
    
        Enable-CsTopology

</div>

</div>

<span> </span>

</div>

</div>

</div>

