---
title: Manuelles Bereinigen der Datenbanken für die Anrufdetailaufzeichnung und-Qualität
description: Manuelles Bereinigen der Datenbanken für die Anrufdetailaufzeichnung und-Qualität
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manually purging the call detail recording and Quality of Experience databases
ms:assetid: 3a3a965b-b861-41a4-b9a8-27184d622c17
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204812(v=OCS.15)
ms:contentKeyID: 48183859
ms.date: 07/07/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c7903431d28bf1a829991ce35c2ee7351168b4a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425822"
---
# <a name="manually-purging-the-call-detail-recording-and-quality-of-experience-databases-in-lync-server-2013"></a><span data-ttu-id="39559-103">Manuelles Bereinigen der Datenbanken für die Anrufdetailaufzeichnung und die Qualität von Erfahrungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="39559-103">Manually purging the call detail recording and Quality of Experience databases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="39559-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="39559-104">

<span> </span></span></span>

<span data-ttu-id="39559-105">_**Letztes Änderungsdatum des Themas:** 2014-07-07_</span><span class="sxs-lookup"><span data-stu-id="39559-105">_**Topic Last Modified:** 2014-07-07_</span></span>

<span data-ttu-id="39559-p101">Administratoren können die Datenbank für die Aufzeichnung von Kommunikationsdatensätzen (KDS) und/oder die QoE-Datenbanken (Quality of Experience) so konfigurieren, dass alte Datensätze automatisch aus der Datenbank gelöscht werden. Dies ist der Fall, wenn der Löschvorgang für die angegebene Datenbank (KDS oder QoE) aktiviert wurde und wenn Datensätze vorhanden sind, die länger als der angegebene Zeitraum in der Datenbank vorhanden waren. Administratoren können das System beispielsweise so konfigurieren, dass täglich um 1:00 Uhr QoE-Datensätze, die älter als 60 Tage sind, aus der QoE-Datenbank gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="39559-p101">Administrators can configure the Call Detail Recording (CDR) and/or the Quality of Experience (QoE) databases to automatically purge old records from the database; this occurs if purging has been enabled for the specified database (CDR or QoE) and if there are any records that have been in the database longer than the specified amount of time. For example, every day at 1:00 AM administrators might configure the system so that QoE records more than 60 days old will be deleted from the QoE database.</span></span>

<span data-ttu-id="39559-108">Zusätzlich zu dieser automatischen Bereinigung wurden zwei neue Cmdlets, Invoke-CsCdrDatabasePurge und Invoke-CsQoEDatbasePurge, zu Microsoft lync Server 2013 hinzugefügt. Mithilfe dieser Cmdlets können Administratoren Datensätze aus der CDR und den QoE-Datenbanken jederzeit manuell bereinigen.</span><span class="sxs-lookup"><span data-stu-id="39559-108">In addition to that automatic purging, two new cmdlets -- Invoke-CsCdrDatabasePurge and Invoke-CsQoEDatbasePurge -- have been added to Microsoft Lync Server 2013; these cmdlets allow administrators to manually purge records from the CDR and the QoE databases at any time.</span></span> <span data-ttu-id="39559-109">Wenn Sie beispielsweise alle Datensätze, die älter als 10 Tage sind, aus der CDR-Datenbank manuell löschen möchten, können Sie einen Befehl wie den folgenden verwenden:</span><span class="sxs-lookup"><span data-stu-id="39559-109">For example, to manually purge all the records more than 10 days old from the CDR database you can use a command similar to this:</span></span>

    Invoke-CsCdrDatabasePurge -Identity service:MonitoringDatabase:atl-sql-001.litwareinc.com -PurgeCallDetailDataOlderThanDays 10 -PurgeDiagnosticDataOlderThanDays 10

<span data-ttu-id="39559-110">Im vorherigen Befehl werden sowohl Anrufdetaildatensätze als auch Diagnosedatensätze, die älter als 10 Tage sind, aus der Überwachungsdatenbank unter atl-sql-001.litwareinc.com entfernt.</span><span class="sxs-lookup"><span data-stu-id="39559-110">In the preceding command both call detail records and diagnostic data records older than 10 days are deleted from the monitoring database on atl-sql-001.litwareinc.com.</span></span> <span data-ttu-id="39559-111">(Anrufdetaildatensätze sind Benutzer-/Sitzungsberichte.</span><span class="sxs-lookup"><span data-stu-id="39559-111">(Call detail records are user/session reports.</span></span> <span data-ttu-id="39559-112">Diagnostische Datensätze sind Diagnoseprotokolle, die von Clientanwendungen wie lync 2013 hochgeladen wurden.)</span><span class="sxs-lookup"><span data-stu-id="39559-112">Diagnostic data records are diagnostic logs uploaded by client applications such as Lync 2013.)</span></span>

<span data-ttu-id="39559-113">Wie oben gezeigt, müssen Sie beim Ausführen des Cmdlets Invoke-CsCdrDatabasePurge sowohl den Parameter PurgeCallDetaiDataOlderThanDays als auch den Parameter PurgeDiagnosticDataOlderThanDays einfügen.</span><span class="sxs-lookup"><span data-stu-id="39559-113">As shown above, when you run the Invoke-CsCdrDatabasePurge cmdlet you must include both the PurgeCallDetaiDataOlderThanDays and the PurgeDiagnosticDataOlderThanDays parameters.</span></span> <span data-ttu-id="39559-114">Diese Parameter müssen jedoch nicht auf denselben Wert festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="39559-114">However, these parameters do not have to be set to the same value.</span></span> <span data-ttu-id="39559-115">Sie können beispielsweise festlegen, dass Anrufdetaildatensätze, die älter sind als 10 Tage, gelöscht werden und konfigurieren, dass alle Diagnosedatensätze in der Datenbank bleiben.</span><span class="sxs-lookup"><span data-stu-id="39559-115">For example, it's possible to purge call detail records more than 10 days old and yet, at the same time, leave all the diagnostic data records in the database.</span></span> <span data-ttu-id="39559-116">Setzen Sie dazu PurgeCallDetailDataOlderThanDays auf 10 und PurgeDiagnosticDataOlderThanDays auf 0.</span><span class="sxs-lookup"><span data-stu-id="39559-116">To do that, set PurgeCallDetailDataOlderThanDays to 10 and PurgeDiagnosticDataOlderThanDays to 0.</span></span> <span data-ttu-id="39559-117">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="39559-117">For example:</span></span>

    Invoke-CsCdrDatabasePurge -Identity service:MonitoringDatabase:atl-sql-001.litwareinc.com -PurgeCallDetailDataOlderThanDays 10 -PurgeDiagnosticDataOlderThanDays 0

<span data-ttu-id="39559-118">Wenn Sie das Cmdlet Invoke-CsCdrDatabasePurge ausführen, sehen Sie standardmäßig für jede Datenbanktabelle, die gelöscht werden muss, eine Eingabeaufforderung ähnlich wie die folgende:</span><span class="sxs-lookup"><span data-stu-id="39559-118">By default, any time you run Invoke-CsCdrDatabasePurge you will see a prompt similar to this one for each database table that must be purged:</span></span>

    Confirm
    Are you sure you want to perform this action?
    Performing operation "Stored procedure: RtcCleanupDiag" on Target "Target SQL Server:atl-sql-001.litwareinc.com\archinst Database: lcscdr".
    [Y] Yes  [A] Yes to All  [N] No  [L] No to All [S] Suspend  [?] Help (default is "Y"):

<span data-ttu-id="39559-p105">Sie müssen entweder J (für Ja) oder A (für Ja zu allen Optionen) eingeben, bevor der Löschvorgang in der Datenbank tatsächlich beginnt. Wenn Sie diese Bestätigungsaufforderungen lieber unterdrücken möchten, fügen Sie am Ende des Aufrufs von Invoke-CsCdrDatabasePurge die folgenden Parameter hinzu:</span><span class="sxs-lookup"><span data-stu-id="39559-p105">You must type either Y (for Yes) or A (for Yes to All) before the database purging will actually take place. If you would prefer to suppress these confirmation prompts, add the following parameter to the end of your call to Invoke-CsCdrDatabasePurge:</span></span>

    -Confirm:$False

<span data-ttu-id="39559-121">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="39559-121">For example:</span></span>

    Invoke-CsCdrDatabasePurge -Identity service:MonitoringDatabase:atl-sql-001.litwareinc.com -PurgeCallDetailDataOlderThanDays 10 -PurgeDiagnosticDataOlderThanDays 10 -Confirm:$False

<span data-ttu-id="39559-122">Dies bewirkt, dass keine Bestätigungsaufforderungen angezeigt werden und der Löschvorgang in der Datenbank sofort durchgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="39559-122">If you do that, confirmation prompts will not be displayed, and database purging will immediately be performed.</span></span>

<span data-ttu-id="39559-123">Verwenden Sie das Cmdlet Invoke-CsQoEDatabasePurge, um Datensätze in der QoE-Datenbank zu löschen und geben Sie das Alter der zu löschenden Datensätze (in Tagen) an:</span><span class="sxs-lookup"><span data-stu-id="39559-123">To purge the QoE database, use the Invoke-CsQoEDatabasePurge cmdlet and specify the age (in days) of the records to be deleted:</span></span>

    Invoke-CsQoEDatabasePurge -Identity service:MonitoringDatabase:atl-sql-001.litwareinc.com -PurgeQoEDataOlderThanDays 10

<span data-ttu-id="39559-124"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="39559-124"></div>

<span> </span>

</div>

</div>

</span></span></div>

