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
# <a name="testing-service-activation-and-group-permissions-in-lync-server-2013"></a><span data-ttu-id="1e409-103">Testen der Dienstaktivierung und Gruppen Berechtigungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="1e409-103">Testing service activation and group permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1e409-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1e409-104">

<span> </span></span></span>

<span data-ttu-id="1e409-105">_**Letztes Änderungsdatum des Themas:** 2014-06-05_</span><span class="sxs-lookup"><span data-stu-id="1e409-105">_**Topic Last Modified:** 2014-06-05_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="1e409-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="1e409-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="1e409-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="1e409-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="1e409-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="1e409-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="1e409-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="1e409-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="1e409-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="1e409-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="1e409-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein.</span><span class="sxs-lookup"><span data-stu-id="1e409-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group.</span></span></p>
<p><span data-ttu-id="1e409-112">Bei der Ausführung mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des Test-CsTopology-Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="1e409-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the Test-CsTopology cmdlet.</span></span> <span data-ttu-id="1e409-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="1e409-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsTopology&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="1e409-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="1e409-114">Description</span></span>

<span data-ttu-id="1e409-115">Mit dem Test-CsTopology-Cmdlet können Sie überprüfen, ob lync Server 2013 im globalen Bereich ordnungsgemäß funktioniert.</span><span class="sxs-lookup"><span data-stu-id="1e409-115">The Test-CsTopology cmdlet enables you to verify that Lync Server 2013 is functioning correctly at a global scope.</span></span> <span data-ttu-id="1e409-116">Das Cmdlet überprüft standardmäßig Ihre gesamte lync Server-Infrastruktur, überprüft, ob die erforderlichen Dienste ausgeführt werden und dass die entsprechenden Berechtigungen für diese Dienste und für die universellen Sicherheitsgruppen festgesetzt werden, die bei der Installation von lync Server erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="1e409-116">By default, the cmdlet checks your whole Lync Server infrastructure, verifying that the required services are running and that the appropriate permissions are set for these services and for the universal security groups that are created when you install Lync Server.</span></span>

<span data-ttu-id="1e409-117">Zusätzlich zur Überprüfung der Gültigkeit der lync Server-Installation können Sie Test-CsTopology auch die Gültigkeit eines bestimmten Diensts überprüfen.</span><span class="sxs-lookup"><span data-stu-id="1e409-117">In addition to verifying the validity of the Lync Server installation, Test-CsTopology also lets you check the validity of a specific service.</span></span> <span data-ttu-id="1e409-118">Dieser Befehl überprüft beispielsweise den Zustand des A/V-Konferenzservers im Pool ATL-CS-001.litwareinc.com:</span><span class="sxs-lookup"><span data-stu-id="1e409-118">For example, this command checks the state of the A/V Conferencing Server on the pool atl-cs-001.litwareinc.com:</span></span>

    Test-CsTopology -Service "ConferencingServer:atl-cs-001.litwareinc.com"

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="1e409-119">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="1e409-119">Running the test</span></span>

<span data-ttu-id="1e409-120">Standardmäßig werden Test-CsTopology auf dem Bildschirm nur sehr wenig ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="1e409-120">By default, Test-CsTopology displays very little output on-screen.</span></span> <span data-ttu-id="1e409-121">Stattdessen werden vom Cmdlet zurückgegebene Informationen in eine HTML-Datei geschrieben.</span><span class="sxs-lookup"><span data-stu-id="1e409-121">Instead, information returned by the cmdlet is written to an HTML file.</span></span> <span data-ttu-id="1e409-122">Mit dem Parameter Report können Sie einen Dateipfad und einen Dateinamen für die von Test-CsTopology generierte HTML-Datei angeben.</span><span class="sxs-lookup"><span data-stu-id="1e409-122">The Report parameter allows you to specify a file path and file name for the HTML file generated by Test-CsTopology.</span></span> <span data-ttu-id="1e409-123">Wenn Sie den Berichtsparameter nicht angeben, wird die HTML-Datei automatisch in Ihrem Ordner "Benutzer" gespeichert, und Sie erhalten einen ähnlichen Namen wie den folgenden: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span><span class="sxs-lookup"><span data-stu-id="1e409-123">If you do not include the Report parameter the HTML file will automatically be saved to your Users folder and be given a name similar to this: ce84964a-c4da-4622-ad34-c54ff3ed361f.html.</span></span>

<span data-ttu-id="1e409-124">Der folgende Beispielbefehl führt Test-CsTopology aus und speichert die Ausgabe in einer Datei mit dem Namen C: \\ Logs \\ComputerTest.html:</span><span class="sxs-lookup"><span data-stu-id="1e409-124">The following sample command runs Test-CsTopology and saves the output to a file that is named C:\\Logs\\ComputerTest.html:</span></span>

    Test-CsTopology -Report "C:\Logs\ComputerTest.html" -Verbose

<span data-ttu-id="1e409-125">Weitere Informationen finden Sie in der Hilfedokumentation zum Cmdlet [Test-CsTopology](https://docs.microsoft.com/powershell/module/skype/Test-CsTopology) .</span><span class="sxs-lookup"><span data-stu-id="1e409-125">For more information, see the Help documentation for the [Test-CsTopology](https://docs.microsoft.com/powershell/module/skype/Test-CsTopology) cmdlet.</span></span>

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="1e409-126">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="1e409-126">Determining success or failure</span></span>

<span data-ttu-id="1e409-127">Im Gegensatz zu den meisten Test-Cmdlets meldet Test-CsTopology Erfolg oder Misserfolg zurück.</span><span class="sxs-lookup"><span data-stu-id="1e409-127">Unlike most of the test cmdlets, Test-CsTopology does report back Success or Failure.</span></span> <span data-ttu-id="1e409-128">Dies ist teilweise auf die große Anzahl von Verifizierungs Prüfungen zurückzuführen, die das Cmdlet bei jeder Ausführung vornehmen muss.</span><span class="sxs-lookup"><span data-stu-id="1e409-128">In part, that’s due to the large number of verification checks that the cmdlet must make every time that it runs.</span></span> <span data-ttu-id="1e409-129">Stattdessen werden Daten in einem HTML-Bericht gespeichert, der dann mithilfe von Internet Explorer angezeigt werden kann.</span><span class="sxs-lookup"><span data-stu-id="1e409-129">Instead, data is saved to an HTML report that can then be viewed by using Internet Explorer.</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="1e409-130">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="1e409-130">Reasons why the test might have failed</span></span>

<span data-ttu-id="1e409-131">Im folgenden finden Sie einige häufige Gründe, warum Test-CsTopology fehlschlagen kann:</span><span class="sxs-lookup"><span data-stu-id="1e409-131">Here are some common reasons why Test-CsTopology might fail:</span></span>

  - <span data-ttu-id="1e409-132">Die Replikation ist auf dem Testcomputer möglicherweise nicht auf dem neuesten Stand.</span><span class="sxs-lookup"><span data-stu-id="1e409-132">Replication might not be up-to-date on the test computer.</span></span> <span data-ttu-id="1e409-133">Sie können den aktuellen Replikationsstatus für einen Computer überprüfen, indem Sie das Get-CsManagementStoreReplicationStatus-Cmdlet ausführen:</span><span class="sxs-lookup"><span data-stu-id="1e409-133">You can check the current replication status for a computer by running the Get-CsManagementStoreReplicationStatus cmdlet:</span></span>
    
        Get-CsManagementStoreReplicationStatus -ReplicaFqdn "atl-cs-001.litwareinc.com"
    
    <span data-ttu-id="1e409-134">Wenn der Replikationsstatus nicht auf dem neuesten Stand ist, können Sie die Replikation manuell erzwingen, indem Sie einen ähnlichen Befehl wie den folgenden verwenden:</span><span class="sxs-lookup"><span data-stu-id="1e409-134">If the replication status is not up-to-date, you can manually force replication to occur by using a command similar to this:</span></span>
    
        Invoke-CsManagementStoreReplication -ReplicaFqdn "atl-cs-001.litwareinc.com"

  - <span data-ttu-id="1e409-135">Möglicherweise muss die Topologie aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="1e409-135">The topology might have to be enabled.</span></span> <span data-ttu-id="1e409-136">Wenn Sie die lync Server-Topologie ändern (Änderungen, die sich auf den lokalen Computer auswirken könnten), müssen Sie die neue Topologie aktivieren.</span><span class="sxs-lookup"><span data-stu-id="1e409-136">If you change the Lync Server topology (changes that might affect the local computer), then you must enable the new topology.</span></span> <span data-ttu-id="1e409-137">Sie können die Topologie jederzeit aktivieren, indem Sie den folgenden Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="1e409-137">You can enable the topology at any time by running this command:</span></span>
    
        Enable-CsTopology

<span data-ttu-id="1e409-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1e409-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

