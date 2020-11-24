---
title: 'Lync Server 2013: Testen von Exchange auf lync-Benachrichtigungen'
description: 'Lync Server 2013: Testen von Exchange auf lync-Benachrichtigungen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing Exchange to Lync notifications
ms:assetid: ed2d6325-3cf5-4450-9951-03092bcb0a7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727315(v=OCS.15)
ms:contentKeyID: 63969665
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bdf453bfdaab7e7b6bdaae8b67ac7759c0d55af4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394507"
---
# <a name="testing-exchange-to-lync-notifications-in-lync-server-2013"></a><span data-ttu-id="4b694-103">Testen von Exchange auf lync-Benachrichtigungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4b694-103">Testing Exchange to Lync notifications in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4b694-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4b694-104">

<span> </span></span></span>

<span data-ttu-id="4b694-105">_**Letztes Änderungsdatum des Themas:** 2014-11-01_</span><span class="sxs-lookup"><span data-stu-id="4b694-105">_**Topic Last Modified:** 2014-11-01_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4b694-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="4b694-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="4b694-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="4b694-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4b694-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="4b694-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="4b694-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="4b694-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4b694-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="4b694-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="4b694-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="4b694-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="4b694-112">Beim Ausführen mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des <strong>Test-CsExStorageNotification-</strong> Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="4b694-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsExStorageNotification</strong> cmdlet.</span></span> <span data-ttu-id="4b694-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="4b694-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsExStorageNotification&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="4b694-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="4b694-114">Description</span></span>

<span data-ttu-id="4b694-115">Das Cmdlet **Test-CsExStorageNotification** wird verwendet, um zu überprüfen, ob der Microsoft Exchange Server 2013-Benachrichtigungsdienst lync Server 2013 benachrichtigen kann, wenn Aktualisierungen an der Kontaktliste eines Benutzers vorgenommen werden.</span><span class="sxs-lookup"><span data-stu-id="4b694-115">The **Test-CsExStorageNotification** cmdlet is used to verify that the Microsoft Exchange Server 2013 notification service can notify Lync Server 2013 any time updates are made to a user's Contact List.</span></span> <span data-ttu-id="4b694-116">Dieses Cmdlet ist nur gültig, wenn Sie den Unified Contact Store verwenden.</span><span class="sxs-lookup"><span data-stu-id="4b694-116">This cmdlet is valid only if you are using the unified contact store.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="4b694-117">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="4b694-117">Running the test</span></span>

<span data-ttu-id="4b694-118">Der in Beispiel 1 gezeigte Befehl überprüft, ob der lync Server-Speicherdienst eine Verbindung mit dem Microsoft Exchange Server-Post Fach Benachrichtigungsdienst für den Benutzer SIP:kenmyer@litwareinc.com herstellen kann.</span><span class="sxs-lookup"><span data-stu-id="4b694-118">The command shown in Example 1 tests to see whether the Lync Server Storage Service can connect to the Microsoft Exchange Server mailbox notification service for the user sip:kenmyer@litwareinc.com.</span></span> <span data-ttu-id="4b694-119">In diesem Beispiel wird NetNamedPipe als WCF-Bindung verwendet.</span><span class="sxs-lookup"><span data-stu-id="4b694-119">In this example, NetNamedPipe is used as the WCF binding.</span></span>

    Test-CsExStorageNotification -SipUri "sip:kenmyer@litwareinc.com" -Binding "NetNamedPipe"

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="4b694-120">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="4b694-120">Determining success or failure</span></span>

<span data-ttu-id="4b694-121">Wenn die Exchange-Integration ordnungsgemäß konfiguriert ist, erhalten Sie eine ähnliche Ausgabe, wobei die Eigenschaft Ergebnis als **erfolgreich** markiert ist:</span><span class="sxs-lookup"><span data-stu-id="4b694-121">If Exchange integration is configured correctly , you'll receive output similar to this, with the Result property marked as **Success**:</span></span>

<span data-ttu-id="4b694-122">Ziel-FQDN: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="4b694-122">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="4b694-123">Ergebnis: Erfolg</span><span class="sxs-lookup"><span data-stu-id="4b694-123">Result : Success</span></span>

<span data-ttu-id="4b694-124">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4b694-124">Latency : 00:00:00</span></span>

<span data-ttu-id="4b694-125">Fehlermeldung:</span><span class="sxs-lookup"><span data-stu-id="4b694-125">Error Message :</span></span>

<span data-ttu-id="4b694-126">Diagnose</span><span class="sxs-lookup"><span data-stu-id="4b694-126">Diagnosis :</span></span>

<span data-ttu-id="4b694-127">Wenn der angegebene Benutzer keine Benachrichtigungen empfangen kann, wird das Ergebnis als Fehler angezeigt, und weitere Informationen werden in den Eigenschaften Fehler und Diagnose aufgezeichnet:</span><span class="sxs-lookup"><span data-stu-id="4b694-127">If the specified user can't receive notifications, the Result will be shown as Failure, and additional information will be recorded in the Error and Diagnosis properties:</span></span>

<span data-ttu-id="4b694-128">Ziel-FQDN: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="4b694-128">Target Fqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="4b694-129">Ergebnis: Fehler</span><span class="sxs-lookup"><span data-stu-id="4b694-129">Result : Failure</span></span>

<span data-ttu-id="4b694-130">Latenz: 00:00:00</span><span class="sxs-lookup"><span data-stu-id="4b694-130">Latency : 00:00:00</span></span>

<span data-ttu-id="4b694-131">Fehlermeldung: 10060, Fehler bei einem Verbindungsversuch, weil die verbundene Partei</span><span class="sxs-lookup"><span data-stu-id="4b694-131">Error Message : 10060, A connection attempt failed because the connected party</span></span>

<span data-ttu-id="4b694-132">hat nach einer bestimmten Zeit nicht richtig reagiert, oder</span><span class="sxs-lookup"><span data-stu-id="4b694-132">did not properly respond after a period of time, or</span></span>

<span data-ttu-id="4b694-133">Fehler beim Herstellen einer Verbindung, weil der verbundene Host</span><span class="sxs-lookup"><span data-stu-id="4b694-133">established connection failed because connected host has</span></span>

<span data-ttu-id="4b694-134">Fehler beim Antworten 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="4b694-134">failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="4b694-135">Innere Ausnahme: ein Verbindungsversuch ist fehlgeschlagen, da die</span><span class="sxs-lookup"><span data-stu-id="4b694-135">Inner Exception:A connection attempt failed because the</span></span>

<span data-ttu-id="4b694-136">die verbundene Partei hat nach einer gewissen Zeit nicht richtig reagiert</span><span class="sxs-lookup"><span data-stu-id="4b694-136">connected party did not properly respond after a period of</span></span>

<span data-ttu-id="4b694-137">Zeit, oder die Verbindung konnte nicht hergestellt werden, weil der verbundene Host</span><span class="sxs-lookup"><span data-stu-id="4b694-137">time, or established connection failed because connected host</span></span>

<span data-ttu-id="4b694-138">Fehler beim Antworten 10.188.116.96:5061</span><span class="sxs-lookup"><span data-stu-id="4b694-138">has failed to respond 10.188.116.96:5061</span></span>

<span data-ttu-id="4b694-139">Diagnose</span><span class="sxs-lookup"><span data-stu-id="4b694-139">Diagnosis :</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="4b694-140">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="4b694-140">Reasons why the test might have failed</span></span>

<span data-ttu-id="4b694-141">Nachfolgend finden Sie einige häufige Gründe, warum **Test-CsExStorageNotification** möglicherweise fehlschlägt:</span><span class="sxs-lookup"><span data-stu-id="4b694-141">Here are some common reasons why **Test-CsExStorageNotification** might fail:</span></span>

  - <span data-ttu-id="4b694-142">Es wurde ein falscher Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="4b694-142">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="4b694-143">Wenn die optionalen Parameter verwendet werden, müssen Sie ordnungsgemäß konfiguriert sein, oder der Test schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="4b694-143">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="4b694-144">Führen Sie den Befehl ohne die optionalen Parameter erneut aus, und überprüfen Sie, ob dies erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="4b694-144">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="4b694-145">Dieser Befehl schlägt fehl, wenn der Microsoft Exchange-Server falsch konfiguriert oder noch nicht bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="4b694-145">This command will fail if the Microsoft Exchange Server is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4b694-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4b694-146">See Also</span></span>


[<span data-ttu-id="4b694-147">Test-CsExStorageConnectivity</span><span class="sxs-lookup"><span data-stu-id="4b694-147">Test-CsExStorageConnectivity</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsExStorageConnectivity)  
  

<span data-ttu-id="4b694-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4b694-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

