---
title: 'Lync Server 2013: Testen der Rechte der Administrator Topologie'
description: 'Lync Server 2013: Testen der Rechte der Administrator Topologie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Test admin topology rights
ms:assetid: 0c03b7fd-449a-47ad-8263-ce811164cbce
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn767943(v=OCS.15)
ms:contentKeyID: 63969575
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22d713297d0e944c7acbc5efcb11b21ea1b26639
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441277"
---
# <a name="test-admin-topology-rights-in-lync-server-2013"></a>Testen der Rechte der Administrator Topologie in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2016-12-08_


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p>Überprüfungszeitplan</p></td>
<td><p>Nach der ersten lync Server-Bereitstellung. Bei Bedarf, wenn berechtigungsbezogene Probleme auftreten.</p></td>
</tr>
<tr class="even">
<td><p>Test Tool</p></td>
<td><p>Windows PowerShell</p></td>
</tr>
<tr class="odd">
<td><p>Erforderliche Berechtigungen</p></td>
<td><p>Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</p>
<p>Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsSetupPermission-Cmdlets verfügt. Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsSetupPermission&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Beschreibung

Standardmäßig können nur Domänenadministratoren eine lync Server-Topologie aktivieren und große Änderungen an der lync Server-Infrastruktur vornehmen. Dies ist kein Problem, solange Ihre Domänenadministratoren und ihre lync Server-Administratoren identisch sind. In vielen Organisationen verfügen lync Server-Administratoren nicht über Administratorrechte für die gesamte Domäne. Standardmäßig bedeutet dies, dass diese Administratoren (als Mitglieder der RTCUniversalServerAdmins-Gruppe definiert) keine Änderungen an der lync Server-Topologie vornehmen können. Um Mitgliedern der RTCUniversalServerAdmins-Gruppe das Recht zu geben, Topologie-Änderungen vorzunehmen, müssen Sie mithilfe des Cmdlets [Grant-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Grant-CsSetupPermission) die erforderlichen Active Directory-Berechtigungen zuweisen.

Das Test-CsSetupPermission-Cmdlet überprüft, ob die erforderlichen Berechtigungen zum Installieren von lync Server oder einer seiner Komponenten für den angegebenen Active Directory-Container konfiguriert sind. Wenn die Berechtigungen nicht zugewiesen sind, können Sie das Grant-CsSetupPermission-Cmdlet ausführen, um Mitgliedern der RTCUniversalServerAdmins-Gruppe das Recht zu gewähren, lync Server zu installieren und zu aktivieren.

<div>


> [!NOTE]  
> Eine detaillierte Liste der von Grant-CsSetupPermission zugewiesenen Berechtigungen finden Sie im Blogbeitrag <A href="https://blogs.technet.com/b/jenstr/archive/2011/02/07/grant-cssetuppermission-and-grant-csoupermission.aspx">Grant-CsSetupPermission und Grant-CsOUPermission</A>.



</div>

</div>

<div>

## <a name="running-the-test"></a>Ausführen des Tests

Rufen Sie das Test-CsSetupPermission-Cmdlet auf, um zu ermitteln, ob Setup Berechtigungen für einen Active Directory-Container zugewiesen sind. Geben Sie den Distinguished Name des Containers an, der überprüft werden soll. Dieser Befehl überprüft beispielsweise die Setup Berechtigungen für den Container ou = CsServers, DC = "litwareinc, DC = com:

    Test-CsSetupPermission -ComputerOU "ou=CsServers,dc=litwareinc,dc=com"

Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Test-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsSetupPermission) .

</div>

<div>

## <a name="determining-success-or-failure"></a>Ermitteln von Erfolg oder Misserfolg

Wenn Test-CsSetupPermission feststellt, dass die erforderlichen Berechtigungen bereits für einen Active Directory-Container festgelegt wurden, gibt das Cmdlet den Wert "true" zurück:

Wahr

Wenn Berechtigungen nicht festgelegt werden, gibt Test-CsSetupPermission den Wert false zurück. Beachten Sie, dass dieser Wert in der Regel in viele Warnmeldungen eingeschlossen ist. Beispiel:

Warnung: Zugriffssteuerungseintrag (ACE) ATL-CS-001 \\ RTCUniversalServerAdmins; Ermöglichen ExtendedRight; Keine Keine 1131f6aa-9c07-11d1-f79f-00c04fc2dcd2

Warnung: die Zugriffssteuerungseinträge (ACEs) für das Objekt "CN = Computers, DC =" litwareinc, DC = com "sind nicht bereit.

Falsch

Warnung: die Verarbeitung von "Test-CsSetupPermission" wurde mit Warnungen abgeschlossen. "2"-Warnungen wurden während dieser Ausführung aufgezeichnet.

Warnung: detaillierte Ergebnisse finden Sie unter "C: \\ Benutzer \\ Administrator \\ AppData \\ local \\ Temp \\Test-CsSetupPermission-1da99ba6-abe2-45e4-8b16-dfd244763118.html".

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Gründe, warum der Test fehlgeschlagen ist

Es gibt zwar seltene Ausnahmen, wenn Test-CsSetupPermission fehlschlägt, bedeutet dies in der Regel, dass dem angegebenen Active Directory-Container keine Setup Berechtigungen zugewiesen sind. Diese Berechtigungen können mithilfe des Grant-CsSetupPermission-Cmdlets zugewiesen werden. Beispielsweise gewährt dieser Befehl dem Container "Computer" im Domänen litwareinc.com Setup Berechtigungen:

    Grant-CsSetupPermission -ComputerOU "cn=Computers,dc=litwareinc,dc=com"

Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Test-CsSetupPermission](https://docs.microsoft.com/powershell/module/skype/Test-CsSetupPermission) .

</div>

</div>

<span> </span>

</div>

</div>

</div>

