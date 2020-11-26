---
title: Testen von Civic addresses mit dem Master Street Address Guide
description: Testen von bürgerlichen Adressen mit dem Leitfaden zur Master Street-Adresse.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing civic addresses against the master street address guide
ms:assetid: dc680de9-2a0f-4fd3-a99e-9bab0bc30ae5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn690132(v=OCS.15)
ms:contentKeyID: 63969657
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 16e0d721b70e3db175b2d23ddee6f59d13a13c4e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439828"
---
# <a name="testing-civic-addresses-against-the-master-street-address-guide-in-lync-server-2013"></a>Testen von bürgerlichen Adressen mit dem Leitfaden zur Master Street-Adresse in lync Server 2013

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
<p>Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsRegistration-Cmdlets verfügt. Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsLisCivicAddress &quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a>Beschreibung

Das Test-CsLisCivicAddress-Cmdlet wird verwendet, um die Speicherorte zu überprüfen, die Ihrer Datenbank für den standortinformationsdienst (LIS) hinzugefügt wurden. Das Cmdlet vergleicht Speicherorte mit den Speicherorten im Master Street Address Guide (MSAG), die zu Ihrem E9-1-1-Netzwerk Routing Anbieter gehören. Wenn Sie nicht über einen Netzwerkrouting Anbieter verfügen oder der Anbieter nicht erreicht werden kann, treten bei den Tests Fehler auf.

Wenn Sie den optionalen Schalterparameter UpdateValidationStatus zu Ihrem Befehl hinzufügen, wird die entsprechende MSAGValid-Datenbankeigenschaft für jede Adresse, die den Test übergibt, auf true festgelegt.

</div>

<div>

## <a name="running-the-test"></a>Ausführen des Tests

Das Test-CsLisCivicAddress-Cmdlet kann zum Testen einzelner Adressen oder zum Testen mehrerer Adressen verwendet werden. Dieser Befehl testet beispielsweise eine einzelne Adresse, die sich in Redmond, WA befindet:

    Test-CsLisCivicAddress -HouseNumber 1234 -HouseNumberSuffix "" -PreDirectional "" -StreetName Main -StreetSuffix St -PostDirectional "" -City Redmond -State WA -PostalCode 98052 -Country US -UpdateValidationStatus

Im Vergleich dazu testet dieser Befehl alle Adressen, die sich derzeit in ihrer LIS-Datenbank befinden:

    Get-CsLisCivicAddress | Test-CsLisCivicAddress -UpdateValidationStatus

Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsRegistration](https://technet.microsoft.com/library/Gg412737(v=OCS.15)) .

</div>

<div>

## <a name="determining-success-or-failure"></a>Ermitteln von Erfolg oder Misserfolg

Test-CsLisCivicAddress meldet den Erfolg oder Misserfolg der angegebenen Adressen zurück. Bei einem Adress Test tritt ein Fehler auf, wenn die Adresse nicht gefunden werden kann oder wenn der Dienstanbieter nicht kontaktiert werden kann.

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a>Gründe, warum der Test fehlgeschlagen ist

Im folgenden finden Sie einige häufige Gründe, warum Test-CsLisCivicAddress fehlschlagen kann:

  - Der LIS-Dienstanbieter steht möglicherweise nicht zur Verfügung. Sie können die URL Ihres LIS-Dienstanbieters abrufen, indem Sie das Get-CsLisConfiguration-Cmdlet ausführen:
    
        Get-CsLisConfiguration 
    
    Anschließend können Sie die URL anpingen, um zu überprüfen, ob der Dienstanbieter verfügbar ist.

</div>

</div>

<span> </span>

</div>

</div>

</div>

