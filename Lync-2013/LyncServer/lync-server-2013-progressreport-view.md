---
title: 'Lync Server 2013: ProgressReport-Ansicht'
description: 'Lync Server 2013: ProgressReport-Ansicht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ProgressReport view
ms:assetid: b49f3fc7-0e2f-498f-8505-aaaf54e435f9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721857(v=OCS.15)
ms:contentKeyID: 49733790
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b95086012f254499644e778e43cafdf70ffc8f9c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436853"
---
# <a name="progressreport-view-in-lync-server-2013"></a><span data-ttu-id="afaf4-103">ProgressReport-Ansicht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="afaf4-103">ProgressReport view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="afaf4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="afaf4-104">

<span> </span></span></span>

<span data-ttu-id="afaf4-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="afaf4-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="afaf4-106">In der ProgressReport-Ansicht werden Informationen zu abgeschlossenen Sitzungen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="afaf4-106">The ProgressReport view stores information about completed sessions.</span></span> <span data-ttu-id="afaf4-107">Fortschrittsberichte werden nur für Anrufe und Sitzungen geschrieben, die von lync Server 2013 für diagnostische Zwecke nützlich sein können.</span><span class="sxs-lookup"><span data-stu-id="afaf4-107">Progress reports will be written only for calls and sessions that Lync Server 2013 determines might be useful for diagnostic purposes.</span></span> <span data-ttu-id="afaf4-108">Diese Ansicht wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="afaf4-108">This view was introduced in Microsoft Lync Server 2013.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="afaf4-109">Die Felder "Fehler", "ErrorReportSeq" und "ProgressReportSeq" beziehen sich nicht unbedingt auf Fehler, sondern auf Nachrichten, die den Status von anrufen oder Nachrichten angeben.</span><span class="sxs-lookup"><span data-stu-id="afaf4-109">The ErrorTime, ErrorReportSeq and ProgressReportSeq fields don’t necessarily refer to errors but to messages that indicate the status of calls or messages.</span></span>



</div>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="afaf4-110">Spalte</span><span class="sxs-lookup"><span data-stu-id="afaf4-110">Column</span></span></th>
<th><span data-ttu-id="afaf4-111">Datentyp</span><span class="sxs-lookup"><span data-stu-id="afaf4-111">Data Type</span></span></th>
<th><span data-ttu-id="afaf4-112">Details</span><span class="sxs-lookup"><span data-stu-id="afaf4-112">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="afaf4-113"><strong>Fehlerzeit</strong></span><span class="sxs-lookup"><span data-stu-id="afaf4-113"><strong>ErrorTime</strong></span></span></p></td>
<td><p><span data-ttu-id="afaf4-114">datetime</span><span class="sxs-lookup"><span data-stu-id="afaf4-114">datetime</span></span></p></td>
<td><p><span data-ttu-id="afaf4-115">Zeitpunkt des Fehlers.</span><span class="sxs-lookup"><span data-stu-id="afaf4-115">Time of error occurred.</span></span> <span data-ttu-id="afaf4-116">Wird in Verbindung mit ErrorReportSeq verwendet, um einen Fehler eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="afaf4-116">Used in conjunction with ErrorReportSeq to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afaf4-117"><strong>ErrorReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="afaf4-117"><strong>ErrorReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="afaf4-118">int</span><span class="sxs-lookup"><span data-stu-id="afaf4-118">int</span></span></p></td>
<td><p><span data-ttu-id="afaf4-119">Die ID-Nummer, um den Fehler zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="afaf4-119">ID number to identify the error.</span></span> <span data-ttu-id="afaf4-120">Wird in Verbindung mit Fehlerzeit verwendet, um einen Fehler eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="afaf4-120">Used in conjunction with ErrorTime to uniquely identify an error.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afaf4-121"><strong>ProgressReportSeq</strong></span><span class="sxs-lookup"><span data-stu-id="afaf4-121"><strong>ProgressReportSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="afaf4-122">int</span><span class="sxs-lookup"><span data-stu-id="afaf4-122">int</span></span></p></td>
<td><p><span data-ttu-id="afaf4-123">ID zum Identifizieren des Statusberichts</span><span class="sxs-lookup"><span data-stu-id="afaf4-123">ID to identify the progress report.</span></span> <span data-ttu-id="afaf4-124">Wird verwendet, um Fortschrittsberichte desselben Fehlerberichts zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="afaf4-124">Used to distinguish progress reports of the same error report.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afaf4-125"><strong>MsDiagId</strong></span><span class="sxs-lookup"><span data-stu-id="afaf4-125"><strong>MsDiagId</strong></span></span></p></td>
<td><p><span data-ttu-id="afaf4-126">int</span><span class="sxs-lookup"><span data-stu-id="afaf4-126">int</span></span></p></td>
<td><p><span data-ttu-id="afaf4-127">Diagnose-ID für den Fehlerbericht.</span><span class="sxs-lookup"><span data-stu-id="afaf4-127">Diagnostic ID for the error report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afaf4-128"><strong>Quelle</strong></span><span class="sxs-lookup"><span data-stu-id="afaf4-128"><strong>Source</strong></span></span></p></td>
<td><p><span data-ttu-id="afaf4-129">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="afaf4-129">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="afaf4-130">Name des Servers, der den Fehler verursacht hat (wenn der Bericht von einer Serverkomponente gesendet wurde).</span><span class="sxs-lookup"><span data-stu-id="afaf4-130">Name of server that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afaf4-131"><strong>Anwendung</strong></span><span class="sxs-lookup"><span data-stu-id="afaf4-131"><strong>Application</strong></span></span></p></td>
<td><p><span data-ttu-id="afaf4-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="afaf4-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="afaf4-133">Der Name der Anwendung, die den Fehler verursacht hat (wenn der Bericht von einer Serverkomponente gesendet wurde).</span><span class="sxs-lookup"><span data-stu-id="afaf4-133">Name of application that originated the error (if report was sent from a server component).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afaf4-134"><strong>Telemetrie</strong></span><span class="sxs-lookup"><span data-stu-id="afaf4-134"><strong>TelemetryId</strong></span></span></p></td>
<td><p><span data-ttu-id="afaf4-135">uniqueidentifier</span><span class="sxs-lookup"><span data-stu-id="afaf4-135">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="afaf4-136">Eindeutiger Bezeichner, in dem die Verknüpfungszeit Informationen für die verschiedenen an einer Konferenz beteiligten Komponenten korreliert werden.</span><span class="sxs-lookup"><span data-stu-id="afaf4-136">Unique identifier correlating join time information for the different components involved in a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="afaf4-137"><strong>SessionSetupTime</strong></span><span class="sxs-lookup"><span data-stu-id="afaf4-137"><strong>SessionSetupTime</strong></span></span></p></td>
<td><p><span data-ttu-id="afaf4-138">int</span><span class="sxs-lookup"><span data-stu-id="afaf4-138">int</span></span></p></td>
<td><p><span data-ttu-id="afaf4-139">Zeit (in Millisekunden), die für eine bestimmte Komponente erforderlich ist, um an einer Konferenz teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="afaf4-139">Time (in milliseconds) required for a specific component to join a conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="afaf4-140"><strong>MsDiagHeader</strong></span><span class="sxs-lookup"><span data-stu-id="afaf4-140"><strong>MsDiagHeader</strong></span></span></p></td>
<td><p><span data-ttu-id="afaf4-141">varchar (max)</span><span class="sxs-lookup"><span data-stu-id="afaf4-141">varchar(max)</span></span></p></td>
<td><p><span data-ttu-id="afaf4-142">Weitere Fehlerinformationen.</span><span class="sxs-lookup"><span data-stu-id="afaf4-142">Additional error information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="afaf4-143">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="afaf4-143">


</div>

<span> </span>

</div>

</div>

</span></span></div>

