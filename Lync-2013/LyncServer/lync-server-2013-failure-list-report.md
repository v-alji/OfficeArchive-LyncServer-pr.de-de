---
title: 'Lync Server 2013: fehlerlistenbericht'
description: 'Lync Server 2013: fehlerlistenbericht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failure List Report
ms:assetid: b6f3a605-e0c6-461e-b17a-41d8039ace9d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615446(v=OCS.15)
ms:contentKeyID: 48185194
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7467144fe207ab61fd086cd35aac74779fd4f771
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393979"
---
# <a name="failure-list-report-in-lync-server-2013"></a><span data-ttu-id="6d6e6-103">Bericht zur Fehlerliste in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6d6e6-103">Failure List Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6d6e6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6d6e6-104">

<span> </span></span></span>

<span data-ttu-id="6d6e6-105">_**Letztes Änderungsdatum des Themas:** 2012-07-02_</span><span class="sxs-lookup"><span data-stu-id="6d6e6-105">_**Topic Last Modified:** 2012-07-02_</span></span>

<span data-ttu-id="6d6e6-p101">Der Fehlerlistenbericht enthält ausführliche Informationen über die einzelnen Teilnehmer, die an einer fehlerhaften Peer-to-Peer-Sitzung oder Konferenzsitzung beteiligt waren. Diese Informationen umfassen den URI des Benutzers, bei dem das Problem aufgetreten ist, sowie den SIP-Antwortcode und die Diagnose-ID, die dem Fehler zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-p101">The Failure List report provides information about the individual participants who took part in a failed peer-to-peer or conferencing session. This information includes the URI of the user who experienced the problem, as well as the SIP Response code and Diagnostic ID associated with the failure.</span></span>

<div>

## <a name="accessing-the-failure-list-report"></a><span data-ttu-id="6d6e6-108">Zugriff auf den Fehlerlistenbericht</span><span class="sxs-lookup"><span data-stu-id="6d6e6-108">Accessing the Failure List Report</span></span>

<span data-ttu-id="6d6e6-109">Auf den Bericht Fehlerliste wird zugegriffen, indem Sie auf eine der folgenden Metriken im [Fehler Verteilungs Bericht in lync Server 2013](lync-server-2013-failure-distribution-report.md)klicken:</span><span class="sxs-lookup"><span data-stu-id="6d6e6-109">The Failure List Report is accessed by clicking any of the following metrics on the [Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md):</span></span>

  - <span data-ttu-id="6d6e6-110">Wichtigste Diagnosegründe (Sitzungen)</span><span class="sxs-lookup"><span data-stu-id="6d6e6-110">Top diagnostic reasons (sessions)</span></span>

  - <span data-ttu-id="6d6e6-111">Wichtigste Modalitäten (Sitzungen)</span><span class="sxs-lookup"><span data-stu-id="6d6e6-111">Top modalities (sessions)</span></span>

  - <span data-ttu-id="6d6e6-112">Wichtigste Pools (Sitzungen)</span><span class="sxs-lookup"><span data-stu-id="6d6e6-112">Top pools (sessions)</span></span>

  - <span data-ttu-id="6d6e6-113">Wichtigste Quellen (Sitzungen)</span><span class="sxs-lookup"><span data-stu-id="6d6e6-113">Top sources (sessions)</span></span>

  - <span data-ttu-id="6d6e6-114">Wichtigste Komponenten (Sitzungen)</span><span class="sxs-lookup"><span data-stu-id="6d6e6-114">Top components (sessions)</span></span>

  - <span data-ttu-id="6d6e6-115">Wichtigste Absenderbenutzer (Sitzungen)</span><span class="sxs-lookup"><span data-stu-id="6d6e6-115">Top from users (sessions)</span></span>

  - <span data-ttu-id="6d6e6-116">Wichtigste Empfängerbenutzer (Sitzungen)</span><span class="sxs-lookup"><span data-stu-id="6d6e6-116">Top to users (sessions)</span></span>

  - <span data-ttu-id="6d6e6-117">Wichtigste Absenderbenutzer-Agenten (Sitzungen)</span><span class="sxs-lookup"><span data-stu-id="6d6e6-117">Top from user agents (sessions)</span></span>

<span data-ttu-id="6d6e6-118">Im Bericht Fehlerliste können Sie auf den [Bericht Peer-to-Peer-Sitzungsdetails in lync Server 2013](lync-server-2013-peer-to-peer-session-detail-report.md) zugreifen, indem Sie auf die Sitzungs Detail Metrik für eine Peer-to-Peer-Sitzung klicken.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-118">From the Failure List Report you can access the [Peer-to-Peer Session Detail Report in Lync Server 2013](lync-server-2013-peer-to-peer-session-detail-report.md) by clicking the Session detail metric for a peer-to-peer session.</span></span> <span data-ttu-id="6d6e6-119">Sie können ebenfalls auf den detaillierten Konferenzbericht zugreifen, indem Sie auf die Konferenzmetrik für eine Konferenz klicken.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-119">You can also access the Conference Detail Report by clicking the Conference metric for a conference.</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-failure-list-report"></a><span data-ttu-id="6d6e6-120">Bestmögliche Verwendung des Fehlerlistenberichts</span><span class="sxs-lookup"><span data-stu-id="6d6e6-120">Making the Best Use of the Failure List Report</span></span>

<span data-ttu-id="6d6e6-p103">Im Fehlerlistenbericht können Sie eine Beschreibung für jeden Antwortcode bzw. jede Diagnose-ID sehen, indem Sie einfach den Mauszeiger über diesen Wert halten. Wenn Sie zum Beispiel Ihre Maus über die Diagnose-ID 7025 halten, wird in einer QuickInfo folgender Text angezeigt:</span><span class="sxs-lookup"><span data-stu-id="6d6e6-p103">In the Failure List Report, you can view a description for each Response code or each Diagnostic ID simply by holding your mouse over that value. For example, if you hold your mouse over Diagnostic ID 7025 you'll see the following displayed in a tooltip:</span></span>

<span data-ttu-id="6d6e6-123">Interner Serverfehler erstellt Medien für Benutzer.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-123">Internal server error creating media for user.</span></span>

<span data-ttu-id="6d6e6-124">Dabei muss beachtet werden, dass der Fehlerlistenbericht weder eine einfache Methode zum direkten Abrufen einer Liste aller Benutzer, die an mindestens einer fehlerhaften Sitzung beteiligt waren, noch eine Methode zur Ermittlung der Benutzer, die am häufigsten an einer fehlerhaften Sitzung beteiligt waren, darstellt.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-124">It's important to note that the Failure List Report does not provide a straightforward way to directly retrieve a list of all the users who participated in at least one failed session, nor does it provide a way to determine which users were most-often involved in a failed session.</span></span> <span data-ttu-id="6d6e6-125">(Zum einen hat der fehlerlistenbericht keine Filterfunktionen.) Wenn Sie die Daten exportieren und dann in eine Datei mit Komma getrennten Werten konvertieren, können Sie Windows PowerShell verwenden, um Antworten auf Fragen wie diese zu finden.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-125">(For one thing, the Failure List Report has no filtering capabilities.) However, if you export the data and then convert it to a comma-separated values file, you can use Windows PowerShell to find the answers to questions like those.</span></span> <span data-ttu-id="6d6e6-126">Nehmen Sie beispielsweise an, dass Sie die Daten in a speichern. CSV-Datei mit dem Namen C: \\ Daten \\ Fehler \_List.csv.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-126">For example, suppose you save the data to a .CSV file named C:\\Data\\Failure\_List.csv.</span></span> <span data-ttu-id="6d6e6-127">Auf Basis der in dieser Datei gespeicherten Daten können mithilfe dieses Befehls alle Benutzer aufgelistet werden, die an mindestens einer fehlerhaften Sitzung beteiligt waren:</span><span class="sxs-lookup"><span data-stu-id="6d6e6-127">Based on the data saved in that file, this command lists all the users who were involved in at least one failed session:</span></span>

    $failures = Import-Csv -Path " C:\Data\Failure_List.csv"
    $failure |Sort-Object "From user" | Select-Object "From user" -Unique

<span data-ttu-id="6d6e6-128">Die Ausgabe für den Befehl ist eine Liste, die der folgenden Liste ähnelt:</span><span class="sxs-lookup"><span data-stu-id="6d6e6-128">That command will return a list similar to this:</span></span>

    From user
    ----
    Pilar.Ackerman@litwareinc.com
    Henrik.Jensen@litwareinc.com
    Gilead.Amosnino@litwareinc.com
    David.Ahs@litwareinc.com
    Ken.Myer@litwareinc.com

<span data-ttu-id="6d6e6-129">Diese beiden Befehle melden die Gesamtzahl der fehlerhaften Sitzungen zurück, an denen Benutzer beteiligt waren:</span><span class="sxs-lookup"><span data-stu-id="6d6e6-129">These two commands report back the total number of failed sessions that each user was involved in:</span></span>

    $failures = Import-Csv -Path "C:\Data\Failure_List.csv"
    $failures | Group-Object "From user" | Select-Object Count, Name | Sort-Object -Property Count -Descending

<span data-ttu-id="6d6e6-130">Die zurückgegebenen Daten sehen so ähnlich aus, wie diese:</span><span class="sxs-lookup"><span data-stu-id="6d6e6-130">That will return data similar to this:</span></span>

    Count    Name
     -----    ----
        20    Pilar.Ackerman@litwareinc.com
        20    David.Ahs@litwareinc.com
        16    Gilead.Amosnino@litwareinc.com
        16    Ken.Myero@litwareinc.com
        14    Henrik.Jensen@litwareinc.com

</div>

<div>

## <a name="filters"></a><span data-ttu-id="6d6e6-131">Filter</span><span class="sxs-lookup"><span data-stu-id="6d6e6-131">Filters</span></span>

<span data-ttu-id="6d6e6-p105">Keine. Sie können den Fehlerlistenbericht nicht filtern.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-p105">None. You cannot filter the Failure List Report.</span></span>

</div>

<div>

## <a name="metrics"></a><span data-ttu-id="6d6e6-134">Metriken</span><span class="sxs-lookup"><span data-stu-id="6d6e6-134">Metrics</span></span>

<span data-ttu-id="6d6e6-135">In der folgenden Tabelle sind die im Fehlerlistenbericht enthaltenen Informationen für jeden fehlerhaften Anruf aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-135">The following table lists the information provided in the Failure List Report for each failed call.</span></span>

### <a name="failure-list-report-metrics"></a><span data-ttu-id="6d6e6-136">Metriken des Fehlerlistenberichts</span><span class="sxs-lookup"><span data-stu-id="6d6e6-136">Failure List Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6d6e6-137">Name</span><span class="sxs-lookup"><span data-stu-id="6d6e6-137">Name</span></span></th>
<th><span data-ttu-id="6d6e6-138">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="6d6e6-138">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="6d6e6-139">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="6d6e6-139">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6d6e6-140"><strong>Gemeldeter Zeitpunkt</strong></span><span class="sxs-lookup"><span data-stu-id="6d6e6-140"><strong>Reported time</strong></span></span></p></td>
<td><p><span data-ttu-id="6d6e6-141">Nein</span><span class="sxs-lookup"><span data-stu-id="6d6e6-141">No</span></span></p></td>
<td><p><span data-ttu-id="6d6e6-142">Datum und Uhrzeit der Aufzeichnung des Berichts.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-142">Date and time the report was recorded.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d6e6-143"><strong>Anforderung</strong></span><span class="sxs-lookup"><span data-stu-id="6d6e6-143"><strong>Request</strong></span></span></p></td>
<td><p><span data-ttu-id="6d6e6-144">Nein</span><span class="sxs-lookup"><span data-stu-id="6d6e6-144">No</span></span></p></td>
<td><p><span data-ttu-id="6d6e6-p106">Typ der fehlerhaften SIP-Anforderung. Beispiel: INVITE oder BYE.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-p106">SIP request type that failed. For example, INVITE or BYE.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d6e6-147"><strong>Antwortcode</strong></span><span class="sxs-lookup"><span data-stu-id="6d6e6-147"><strong>Response code</strong></span></span></p></td>
<td><p><span data-ttu-id="6d6e6-148">Nein</span><span class="sxs-lookup"><span data-stu-id="6d6e6-148">No</span></span></p></td>
<td><p><span data-ttu-id="6d6e6-149">SIP-Antwortcode, der bei einem Konferenzfehler gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-149">SIP response code sent when the conference failed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d6e6-150"><strong>Diagnose-ID</strong></span><span class="sxs-lookup"><span data-stu-id="6d6e6-150"><strong>Diagnostic ID</strong></span></span></p></td>
<td><p><span data-ttu-id="6d6e6-151">Nein</span><span class="sxs-lookup"><span data-stu-id="6d6e6-151">No</span></span></p></td>
<td><p><span data-ttu-id="6d6e6-152">Eindeutige ID (in der Form eines Headers vom Typ „ms-diagnostics“), die an eine SIP-Nachricht angehängt wird und oft nützliche Informationen für die Fehlerbehebung bereitstellt.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-152">Unique identifier (in the form of an ms-diagnostics header) attached to a SIP message that often provides information useful in troubleshooting errors.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d6e6-153"><strong>Beitrittszeitraum (ms)</strong></span><span class="sxs-lookup"><span data-stu-id="6d6e6-153"><strong>Join cost time (ms)</strong></span></span></p></td>
<td><p><span data-ttu-id="6d6e6-154">Nein</span><span class="sxs-lookup"><span data-stu-id="6d6e6-154">No</span></span></p></td>
<td><p><span data-ttu-id="6d6e6-155">Zeitraum (in Millisekunden), der erforderlich ist, damit der Benutzer der Konferenz beitreten kann.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-155">Amount of time (in milliseconds) required for the user to join the conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d6e6-156"><strong>Absenderbenutzer</strong></span><span class="sxs-lookup"><span data-stu-id="6d6e6-156"><strong>From user</strong></span></span></p></td>
<td><p><span data-ttu-id="6d6e6-157">Nein</span><span class="sxs-lookup"><span data-stu-id="6d6e6-157">No</span></span></p></td>
<td><p><span data-ttu-id="6d6e6-158">Die SIP-Adresse des Benutzers, der den Anruf initiiert hat.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-158">SIP address of the user who initiated the call.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6d6e6-159"><strong>Von Benutzeragent</strong></span><span class="sxs-lookup"><span data-stu-id="6d6e6-159"><strong>From user agent</strong></span></span></p></td>
<td><p><span data-ttu-id="6d6e6-160">Nein</span><span class="sxs-lookup"><span data-stu-id="6d6e6-160">No</span></span></p></td>
<td><p><span data-ttu-id="6d6e6-161">Software, die vom Endpunkt des Benutzers, der den Anruf initiiert hat, verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-161">Software used by the endpoint of the user who initiated the call.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6d6e6-162"><strong>An Benutzer</strong></span><span class="sxs-lookup"><span data-stu-id="6d6e6-162"><strong>To user</strong></span></span></p></td>
<td><p><span data-ttu-id="6d6e6-163">Nein</span><span class="sxs-lookup"><span data-stu-id="6d6e6-163">No</span></span></p></td>
<td><p><span data-ttu-id="6d6e6-164">SIP-Adresse des Benutzers, der angerufen wurde.</span><span class="sxs-lookup"><span data-stu-id="6d6e6-164">SIP address of the user who was being called.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="6d6e6-165">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6d6e6-165">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

