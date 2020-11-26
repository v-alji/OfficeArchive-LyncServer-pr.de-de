---
title: 'Lync Server 2013: Testen der Datenbankkonfiguration'
description: 'Lync Server 2013: Testen der Datenbankkonfiguration.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Testing database configuration
ms:assetid: 60f7fcd2-5efe-4791-b159-b0f9bf39a41b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn727307(v=OCS.15)
ms:contentKeyID: 63969606
ms.date: 07/07/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2b9f88eee99c4a2d523cc84df401dcc1d7b9fe59
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441039"
---
# <a name="testing-database-configuration-in-lync-server-2013"></a><span data-ttu-id="c073b-103">Testen der Datenbankkonfiguration in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c073b-103">Testing database configuration in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c073b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c073b-104">

<span> </span></span></span>

<span data-ttu-id="c073b-105">_**Letztes Änderungsdatum des Themas:** 2016-07-07_</span><span class="sxs-lookup"><span data-stu-id="c073b-105">_**Topic Last Modified:** 2016-07-07_</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c073b-106">Überprüfungszeitplan</span><span class="sxs-lookup"><span data-stu-id="c073b-106">Verification schedule</span></span></p></td>
<td><p><span data-ttu-id="c073b-107">Täglich</span><span class="sxs-lookup"><span data-stu-id="c073b-107">Daily</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c073b-108">Test Tool</span><span class="sxs-lookup"><span data-stu-id="c073b-108">Testing tool</span></span></p></td>
<td><p><span data-ttu-id="c073b-109">Windows PowerShell</span><span class="sxs-lookup"><span data-stu-id="c073b-109">Windows PowerShell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c073b-110">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="c073b-110">Permissions required</span></span></p></td>
<td><p><span data-ttu-id="c073b-111">Wenn Benutzer lokal mit der lync Server-Verwaltungsshell ausgeführt werden, müssen Sie Mitglied der RTCUniversalServerAdmins-Sicherheitsgruppe sein und über Administrator Rechte für SQL Server verfügen.</span><span class="sxs-lookup"><span data-stu-id="c073b-111">When run locally using the Lync Server Management Shell, users must be members of the RTCUniversalServerAdmins security group, and need to have Administrator privileges on the SQL server.</span></span></p>
<p><span data-ttu-id="c073b-112">Beim Ausführen mithilfe einer Remoteinstanz von Windows PowerShell muss Benutzern eine RBAC-Rolle zugewiesen werden, die über die Berechtigung zum Ausführen des <strong>Test-CsDatabase-</strong> Cmdlets verfügt.</span><span class="sxs-lookup"><span data-stu-id="c073b-112">When run using a remote instance of Windows PowerShell, users must be assigned an RBAC role that has permission to run the <strong>Test-CsDatabase</strong> cmdlet.</span></span> <span data-ttu-id="c073b-113">Führen Sie den folgenden Befehl in der Windows PowerShell-Eingabeaufforderung aus, um eine Liste aller RBAC-Rollen anzuzeigen, die dieses Cmdlet verwenden können:</span><span class="sxs-lookup"><span data-stu-id="c073b-113">To see a list of all RBAC roles that can use this cmdlet, run the following command from the Windows PowerShell prompt:</span></span></p>
<pre><code>Get-CsAdminRole | Where-Object {$_.Cmdlets -match &quot;Test-CsDatabase&quot;}</code></pre></td>
</tr>
</tbody>
</table>


<div>

## <a name="description"></a><span data-ttu-id="c073b-114">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="c073b-114">Description</span></span>

<span data-ttu-id="c073b-115">Das Cmdlet **Test-CsDatabase** überprüft die Konnektivität mit einer oder mehreren lync Server 2013-Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="c073b-115">The **Test-CsDatabase** cmdlet verifies connectivity to one or more Lync Server 2013 databases.</span></span> <span data-ttu-id="c073b-116">Beim Ausführen liest das Cmdlet **Test-CsDatabase** die lync Server-Topologie, versucht, eine Verbindung mit relevanten Datenbankenherzustellen, und gibt dann den Erfolg oder Misserfolg jedes einzelnen Versuchs zurück.</span><span class="sxs-lookup"><span data-stu-id="c073b-116">When run, the **Test-CsDatabase** cmdlet reads the Lync Server topology, attempts to connect to relevant databases, and then reports back the success or failure of each try.</span></span> <span data-ttu-id="c073b-117">Wenn eine Verbindung hergestellt werden kann, meldet das Cmdlet auch Informationen wie den Datenbanknamen, die SQL Server-Versionsinformationen und den Speicherort aller installierten Spiegeldatenbanken zurück.</span><span class="sxs-lookup"><span data-stu-id="c073b-117">If a connection can be made, the cmdlet will also report back such information as the database name, SQL Server version information, and the location of any installed mirror databases.</span></span>

</div>

<div>

## <a name="running-the-test"></a><span data-ttu-id="c073b-118">Ausführen des Tests</span><span class="sxs-lookup"><span data-stu-id="c073b-118">Running the test</span></span>

<span data-ttu-id="c073b-119">Der in Beispiel 1 gezeigte Befehl überprüft die Konfiguration der zentralen Verwaltungsdatenbank.</span><span class="sxs-lookup"><span data-stu-id="c073b-119">The command shown in Example 1 verifies the configuration of the Central Management database.</span></span>

    Test-CsDatabase -CentralManagementDatabase

<span data-ttu-id="c073b-120">Beispiel 2 überprüft alle lync Server-Datenbanken, die auf dem Computer ATL-SQL-001.litwareinc.com installiert sind.</span><span class="sxs-lookup"><span data-stu-id="c073b-120">Example 2 verifies all the Lync Server databases installed on the computer atl-sql-001.litwareinc.com.</span></span>

    Test-CsDatabase -ConfiguredDatabases -SqlServerFqdn "atl-sql-001.litwareinc.com"

<span data-ttu-id="c073b-121">In Beispiel 3 wird die Überprüfung nur für die auf dem Computer ATL-SQL-001.litwareinc.com installierte Archivierungsdatenbank durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="c073b-121">In Example 3, verification is performed only for the Archiving database installed on the computer atl-sql-001.litwareinc.com.</span></span> <span data-ttu-id="c073b-122">Beachten Sie, dass der SqlInstanceName-Parameter enthalten ist, um die SQL Server-Instanz (Archinst) anzugeben, in der sich die Archivierungsdatenbank befindet.</span><span class="sxs-lookup"><span data-stu-id="c073b-122">Note that the SqlInstanceName parameter is included to specify the SQL Server instance (Archinst) where the Archiving database is located.</span></span>

    Test-CsDatabase -DatabaseType "Archiving" -SqlServerFqdn "atl-sql-001.litwareinc.com" -SqlInstanceName "archinst"

<span data-ttu-id="c073b-123">Der in Beispiel 4 angezeigte Befehl überprüft die auf dem lokalen Computer installierten Datenbanken.</span><span class="sxs-lookup"><span data-stu-id="c073b-123">The command shown in Example 4 verifies the databases installed on the local computer.</span></span>

    Test-CsDatabase -LocalService

</div>

<div>

## <a name="determining-success-or-failure"></a><span data-ttu-id="c073b-124">Ermitteln von Erfolg oder Misserfolg</span><span class="sxs-lookup"><span data-stu-id="c073b-124">Determining success or failure</span></span>

<span data-ttu-id="c073b-125">Wenn die Datenbankverbindung ordnungsgemäß konfiguriert ist, erhalten Sie eine ähnliche Ausgabe, wobei die Eigenschaft erfolgreich als **wahr** markiert ist:</span><span class="sxs-lookup"><span data-stu-id="c073b-125">If database connectivity is configured correctly, you'll receive output similar to this, with the Succeed property marked as **True**:</span></span>

<span data-ttu-id="c073b-126">SqlServerFqdn: ATL-SQL-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c073b-126">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="c073b-127">SqlInstanceName: RTC</span><span class="sxs-lookup"><span data-stu-id="c073b-127">SqlInstanceName : rtc</span></span>

<span data-ttu-id="c073b-128">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="c073b-128">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="c073b-129">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="c073b-129">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="c073b-130">DatabaseName: XDS</span><span class="sxs-lookup"><span data-stu-id="c073b-130">DatabaseName : xds</span></span>

<span data-ttu-id="c073b-131">DataSource</span><span class="sxs-lookup"><span data-stu-id="c073b-131">DataSource :</span></span>

<span data-ttu-id="c073b-132">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="c073b-132">SQLServerVersion :</span></span>

<span data-ttu-id="c073b-133">ExpectedVersion : 10.13.2</span><span class="sxs-lookup"><span data-stu-id="c073b-133">ExpectedVersion : 10.13.2</span></span>

<span data-ttu-id="c073b-134">InstalledVersion</span><span class="sxs-lookup"><span data-stu-id="c073b-134">InstalledVersion :</span></span>

<span data-ttu-id="c073b-135">Erfolgreich: true</span><span class="sxs-lookup"><span data-stu-id="c073b-135">Succeed : True</span></span>

<span data-ttu-id="c073b-136">SqlServerFqdn: ATL-SQL-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c073b-136">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="c073b-137">SqlInstanceName: RTC</span><span class="sxs-lookup"><span data-stu-id="c073b-137">SqlInstanceName : rtc</span></span>

<span data-ttu-id="c073b-138">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="c073b-138">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="c073b-139">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="c073b-139">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="c073b-140">DatabaseName: Lis</span><span class="sxs-lookup"><span data-stu-id="c073b-140">DatabaseName : lis</span></span>

<span data-ttu-id="c073b-141">DataSource</span><span class="sxs-lookup"><span data-stu-id="c073b-141">DataSource :</span></span>

<span data-ttu-id="c073b-142">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="c073b-142">SQLServerVersion :</span></span>

<span data-ttu-id="c073b-143">ExpectedVersion: 3.1.1</span><span class="sxs-lookup"><span data-stu-id="c073b-143">ExpectedVersion : 3.1.1</span></span>

<span data-ttu-id="c073b-144">InstalledVersion</span><span class="sxs-lookup"><span data-stu-id="c073b-144">InstalledVersion :</span></span>

<span data-ttu-id="c073b-145">Erfolgreich: true</span><span class="sxs-lookup"><span data-stu-id="c073b-145">Succeed : True</span></span>

<span data-ttu-id="c073b-146">Wenn die Datenbank richtig konfiguriert ist, aber weiterhin verfügbar ist, wird das Feld erfolgreich als **falsch** angezeigt, und es werden weitere Warnungen und Informationen bereitgestellt:</span><span class="sxs-lookup"><span data-stu-id="c073b-146">If the database is configured correctly but still available, the Succeed field will be shown as **False**, and additional warnings and information will be provided:</span></span>

<span data-ttu-id="c073b-147">SqlServerFqdn: ATL-SQL-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c073b-147">SqlServerFqdn : atl-sql-001.litwareinc.com</span></span>

<span data-ttu-id="c073b-148">SqlInstanceName: RTC</span><span class="sxs-lookup"><span data-stu-id="c073b-148">SqlInstanceName : rtc</span></span>

<span data-ttu-id="c073b-149">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="c073b-149">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="c073b-150">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="c073b-150">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="c073b-151">DatabaseName: XDS</span><span class="sxs-lookup"><span data-stu-id="c073b-151">DatabaseName : xds</span></span>

<span data-ttu-id="c073b-152">DataSource</span><span class="sxs-lookup"><span data-stu-id="c073b-152">DataSource :</span></span>

<span data-ttu-id="c073b-153">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="c073b-153">SQLServerVersion :</span></span>

<span data-ttu-id="c073b-154">ExpectedVersion : 10.13.2</span><span class="sxs-lookup"><span data-stu-id="c073b-154">ExpectedVersion : 10.13.2</span></span>

<span data-ttu-id="c073b-155">InstalledVersion</span><span class="sxs-lookup"><span data-stu-id="c073b-155">InstalledVersion :</span></span>

<span data-ttu-id="c073b-156">Erfolgreich: falsch</span><span class="sxs-lookup"><span data-stu-id="c073b-156">Succeed : False</span></span>

<span data-ttu-id="c073b-157">SqlServerFqdn: ATL-CS-001.litwareinc.com</span><span class="sxs-lookup"><span data-stu-id="c073b-157">SqlServerFqdn : atl-cs-001.litwareinc.com</span></span>

<span data-ttu-id="c073b-158">SqlInstanceName: RTC</span><span class="sxs-lookup"><span data-stu-id="c073b-158">SqlInstanceName : rtc</span></span>

<span data-ttu-id="c073b-159">MirrorSqlServerFqdn :</span><span class="sxs-lookup"><span data-stu-id="c073b-159">MirrorSqlServerFqdn :</span></span>

<span data-ttu-id="c073b-160">MirrorSqlInstanceName :</span><span class="sxs-lookup"><span data-stu-id="c073b-160">MirrorSqlInstanceName :</span></span>

<span data-ttu-id="c073b-161">DatabaseName: Lis</span><span class="sxs-lookup"><span data-stu-id="c073b-161">DatabaseName : lis</span></span>

<span data-ttu-id="c073b-162">DataSource</span><span class="sxs-lookup"><span data-stu-id="c073b-162">DataSource :</span></span>

<span data-ttu-id="c073b-163">SQLServerVersion :</span><span class="sxs-lookup"><span data-stu-id="c073b-163">SQLServerVersion :</span></span>

<span data-ttu-id="c073b-164">ExpectedVersion: 3.1.1</span><span class="sxs-lookup"><span data-stu-id="c073b-164">ExpectedVersion : 3.1.1</span></span>

<span data-ttu-id="c073b-165">InstalledVersion</span><span class="sxs-lookup"><span data-stu-id="c073b-165">InstalledVersion :</span></span>

<span data-ttu-id="c073b-166">Erfolgreich: falsch</span><span class="sxs-lookup"><span data-stu-id="c073b-166">Succeed : False</span></span>

<span data-ttu-id="c073b-167">Warnung: Test-CsDatabase Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="c073b-167">WARNING: Test-CsDatabase encountered errors.</span></span> <span data-ttu-id="c073b-168">Konsultieren Sie die Protokolldatei für eine</span><span class="sxs-lookup"><span data-stu-id="c073b-168">Consult the log file for a</span></span>

<span data-ttu-id="c073b-169">detaillierte Analyse und um sicherzustellen, dass alle Fehler (2) und Warnungen (0) behandelt werden</span><span class="sxs-lookup"><span data-stu-id="c073b-169">detailed analysis, and to make sure that all errors (2) and warnings (0) are addressed</span></span>

<span data-ttu-id="c073b-170">bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="c073b-170">before continuing.</span></span>

<span data-ttu-id="c073b-171">Warnung: detaillierte Ergebnisse finden Sie unter</span><span class="sxs-lookup"><span data-stu-id="c073b-171">WARNING: Detailed results can be found at</span></span>

<span data-ttu-id="c073b-172">"C: \\ Benutzer \\ Testen \\ AppData \\ local \\ Temp \\ 2 \\ Test-CsDatabase-b18d488a-8044-4679-bbf2-</span><span class="sxs-lookup"><span data-stu-id="c073b-172">"C:\\Users\\Testing\\AppData\\Local\\Temp\\2\\Test-CsDatabase-b18d488a-8044-4679-bbf2-</span></span>

<span data-ttu-id="c073b-173">04d593cce8e6.html ".</span><span class="sxs-lookup"><span data-stu-id="c073b-173">04d593cce8e6.html".</span></span>

</div>

<div>

## <a name="reasons-why-the-test-might-have-failed"></a><span data-ttu-id="c073b-174">Gründe, warum der Test fehlgeschlagen ist</span><span class="sxs-lookup"><span data-stu-id="c073b-174">Reasons why the test might have failed</span></span>

<span data-ttu-id="c073b-175">Nachfolgend finden Sie einige häufige Gründe, warum **Test-CsDatabase** möglicherweise fehlschlägt:</span><span class="sxs-lookup"><span data-stu-id="c073b-175">Here are some common reasons why **Test-CsDatabase** might fail:</span></span>

  - <span data-ttu-id="c073b-176">Es wurde ein falscher Parameterwert angegeben.</span><span class="sxs-lookup"><span data-stu-id="c073b-176">An incorrect parameter value was supplied.</span></span> <span data-ttu-id="c073b-177">Wenn die optionalen Parameter verwendet werden, müssen Sie ordnungsgemäß konfiguriert sein, oder der Test schlägt fehl.</span><span class="sxs-lookup"><span data-stu-id="c073b-177">If used, the optional parameters must be configured correctly or the test will fail.</span></span> <span data-ttu-id="c073b-178">Führen Sie den Befehl ohne die optionalen Parameter erneut aus, und überprüfen Sie, ob dies erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="c073b-178">Rerun the command without the optional parameters and see whether that succeeds.</span></span>

  - <span data-ttu-id="c073b-179">Dieser Befehl schlägt fehl, wenn die Datenbank falsch konfiguriert oder noch nicht bereitgestellt wurde.</span><span class="sxs-lookup"><span data-stu-id="c073b-179">This command will fail if the database is misconfigured or not yet deployed.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c073b-180">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c073b-180">See Also</span></span>


[<span data-ttu-id="c073b-181">Get-CsDatabaseMirrorState</span><span class="sxs-lookup"><span data-stu-id="c073b-181">Get-CsDatabaseMirrorState</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsDatabaseMirrorState)  
[<span data-ttu-id="c073b-182">Get-CsService</span><span class="sxs-lookup"><span data-stu-id="c073b-182">Get-CsService</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsService)  
[<span data-ttu-id="c073b-183">Get-CsUserDatabaseState</span><span class="sxs-lookup"><span data-stu-id="c073b-183">Get-CsUserDatabaseState</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUserDatabaseState)  
  

<span data-ttu-id="c073b-184"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c073b-184"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

