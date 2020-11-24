---
title: 'Lync Server 2013: Verwenden des Überwachungs Dashboards'
description: 'Lync Server 2013: Verwenden des Überwachungs Dashboards'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using the Monitoring Dashboard
ms:assetid: e00e5783-116f-481f-ad17-3af847d6769a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721905(v=OCS.15)
ms:contentKeyID: 49733839
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e8a68fa1e55b7d0b8305c53802ddabaa904fa214
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395278"
---
# <a name="using-the-monitoring-dashboard-in-lync-server-2013"></a><span data-ttu-id="a70fb-103">Verwenden des Überwachungs Dashboards in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a70fb-103">Using the Monitoring Dashboard in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a70fb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a70fb-104">

<span> </span></span></span>

<span data-ttu-id="a70fb-105">_**Letztes Änderungsdatum des Themas:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="a70fb-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="a70fb-106">Das Überwachungs Dashboard bietet Administratoren einen schnellen Überblick über den Systemstatus und die Systemnutzung von Microsoft lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="a70fb-106">The Monitoring Dashboard provides administrators with a quick overview of their Microsoft Lync Server 2013 system health and system usage.</span></span> <span data-ttu-id="a70fb-107">Im Dashboard wird eine Zusammenfassung wichtiger Systemmetriken für folgende Werte angezeigt:</span><span class="sxs-lookup"><span data-stu-id="a70fb-107">The Dashboard is designed to show an aggregate view of key system metrics and to do so by displaying either:</span></span>

  - <span data-ttu-id="a70fb-p102">Gesamtwerte für den aktuellen Tag. Beachten Sie, dass die für den aktuellen Tag angezeigten Werte Daten repräsentieren, die von Mitternacht bis zum aktuellen Zeitpunkt aufgezeichnet wurden (basierend auf der Ortszeit des Berichtsservers). Dies bedeutet, dass Sie in der Regel Daten für einen Teil des Tages und nicht für einen Zeitraum von 24 Stunden sehen. Wenn z. B. die Ortszeit des Servers 08:00 Uhr ist, sehen Sie acht Stunden an Daten, da zwischen Mitternacht und der aktuellen Urzeit 08:00 Uhr acht Stunden verstrichen sind.</span><span class="sxs-lookup"><span data-stu-id="a70fb-p102">Totals for the current day. Note that values shown for the current day represent data that has been recorded from midnight until the current time (based on the local time of the reporting server). That means that you will typically be viewing data for a partial day and not for a 24-hour period. For example, if the local time of the server is 8:00 AM, you see eight hours’ worth of data because there are eight hours between midnight and the current time of 8:00 AM.</span></span>

  - <span data-ttu-id="a70fb-112">Gesamtwerte für die Woche sowie Trendgesamtwerte für die letzten sechs Wochen.</span><span class="sxs-lookup"><span data-stu-id="a70fb-112">Totals for the week, and trend totals for the past six weeks.</span></span>

  - <span data-ttu-id="a70fb-113">Gesamtwerte für den Monat sowie Trendgesamtwerte für die letzten sechs Monate (nur für die Systemauslastung).</span><span class="sxs-lookup"><span data-stu-id="a70fb-113">Totals for the month, and trend totals for the past six months (for system usage only).</span></span>

<span data-ttu-id="a70fb-114">Beachten Sie, dass Sie das Cmdlet [Get-CsReportingConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsReportingConfiguration) verwenden können, um die URL zurückzugeben, die für den Zugriff auf lync Server 2013-Überwachungsberichte verwendet wird:</span><span class="sxs-lookup"><span data-stu-id="a70fb-114">Note that you can use the [Get-CsReportingConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsReportingConfiguration) cmdlet to return the URL used for accessing Lync Server 2013 Monitoring Reports:</span></span>

    Get-CsReportingConfiguration

<span data-ttu-id="a70fb-115">Standardmäßig werden im Monitoring-Dashboard Daten für die folgenden Metriken für die aktuelle Woche angezeigt (und Trendgesamtwerte für die letzten sechs Wochen):</span><span class="sxs-lookup"><span data-stu-id="a70fb-115">By default, the Monitoring Dashboard shows data for the following metrics for the current week (and trend totals for the previous six weeks):</span></span>

<div>

## <a name="system-usage-metrics"></a><span data-ttu-id="a70fb-116">Metriken für die Systemauslastung</span><span class="sxs-lookup"><span data-stu-id="a70fb-116">System Usage Metrics</span></span>

<span data-ttu-id="a70fb-117">**Registrierung**</span><span class="sxs-lookup"><span data-stu-id="a70fb-117">**Registration**</span></span>

  - <span data-ttu-id="a70fb-118">Eindeutige Benutzeranmeldungen</span><span class="sxs-lookup"><span data-stu-id="a70fb-118">Unique user logons</span></span>

<span data-ttu-id="a70fb-119">**Peer-to-Peer**</span><span class="sxs-lookup"><span data-stu-id="a70fb-119">**Peer-to-peer**</span></span>

  - <span data-ttu-id="a70fb-120">Sitzungen insgesamt</span><span class="sxs-lookup"><span data-stu-id="a70fb-120">Total sessions</span></span>

  - <span data-ttu-id="a70fb-121">Chatsitzungen</span><span class="sxs-lookup"><span data-stu-id="a70fb-121">IM sessions</span></span>

  - <span data-ttu-id="a70fb-122">Audiositzungen</span><span class="sxs-lookup"><span data-stu-id="a70fb-122">Audio sessions</span></span>

  - <span data-ttu-id="a70fb-123">Videositzungen</span><span class="sxs-lookup"><span data-stu-id="a70fb-123">Video sessions</span></span>

  - <span data-ttu-id="a70fb-124">Anwendungsfreigabe</span><span class="sxs-lookup"><span data-stu-id="a70fb-124">Application sharing</span></span>

  - <span data-ttu-id="a70fb-125">Gesamtdauer der Audiositzungen in Minuten</span><span class="sxs-lookup"><span data-stu-id="a70fb-125">Total audio session minutes</span></span>

  - <span data-ttu-id="a70fb-126">Durchschn. Dauer der Audiositzungen in Minuten</span><span class="sxs-lookup"><span data-stu-id="a70fb-126">Avg. audio session minutes</span></span>

<span data-ttu-id="a70fb-127">**Konferenz**</span><span class="sxs-lookup"><span data-stu-id="a70fb-127">**Conference**</span></span>

  - <span data-ttu-id="a70fb-128">Konferenzen insgesamt</span><span class="sxs-lookup"><span data-stu-id="a70fb-128">Total conferences</span></span>

  - <span data-ttu-id="a70fb-129">Chatkonferenzen</span><span class="sxs-lookup"><span data-stu-id="a70fb-129">IM conferences</span></span>

  - <span data-ttu-id="a70fb-130">A/V-Konferenzen</span><span class="sxs-lookup"><span data-stu-id="a70fb-130">A/V conferences</span></span>

  - <span data-ttu-id="a70fb-131">Anwendungsfreigabekonferenzen</span><span class="sxs-lookup"><span data-stu-id="a70fb-131">Application sharing conferences</span></span>

  - <span data-ttu-id="a70fb-132">Webkonferenzen</span><span class="sxs-lookup"><span data-stu-id="a70fb-132">Web conferences</span></span>

  - <span data-ttu-id="a70fb-133">Organisatoren insgesamt</span><span class="sxs-lookup"><span data-stu-id="a70fb-133">Total organizers</span></span>

  - <span data-ttu-id="a70fb-134">Gesamtdauer der A/V-Konferenzen in Minuten</span><span class="sxs-lookup"><span data-stu-id="a70fb-134">Total A/V conference minutes</span></span>

  - <span data-ttu-id="a70fb-135">Durchschn. Dauer der A/V-Konferenzen in Minuten</span><span class="sxs-lookup"><span data-stu-id="a70fb-135">Avg. A/V conference minutes</span></span>

  - <span data-ttu-id="a70fb-136">PSTN-Konferenzen insgesamt</span><span class="sxs-lookup"><span data-stu-id="a70fb-136">Total PSTN conferences</span></span>

  - <span data-ttu-id="a70fb-137">PSTN-Teilnehmer insgesamt</span><span class="sxs-lookup"><span data-stu-id="a70fb-137">Total PSTN participants</span></span>

  - <span data-ttu-id="a70fb-138">PSTN-Teilnehmerminuten insgesamt</span><span class="sxs-lookup"><span data-stu-id="a70fb-138">Total PSTN participant minutes</span></span>

<span data-ttu-id="a70fb-139">Neben den Metriken für die Systemauslastung werden für die folgenden Metriken Gesamtwerte für den aktuellen Tag und die letzten sechs Tage (wenn Sie **Wöchentliche Ansicht** auswählen) bzw. für die aktuelle Woche und die letzten sechs Wochen (wenn Sie **Monatliche Ansicht** auswählen) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a70fb-139">In addition to the System Usage metrics, the following metrics displays total for the current day and the previous six days (if you select **Weekly View**) or for the current week and the past six weeks if you select **Monthly View**.</span></span>

</div>

<div>

## <a name="per-user-call-diagnostics"></a><span data-ttu-id="a70fb-140">Anrufdiagnose pro Benutzer</span><span class="sxs-lookup"><span data-stu-id="a70fb-140">Per-User Call Diagnostics</span></span>

<span data-ttu-id="a70fb-141">**Benutzer mit Anruffehlern**</span><span class="sxs-lookup"><span data-stu-id="a70fb-141">**Users with call failures**</span></span>

  - <span data-ttu-id="a70fb-142">Benutzer insgesamt mit Anruffehlern</span><span class="sxs-lookup"><span data-stu-id="a70fb-142">Total users with call failures</span></span>

  - <span data-ttu-id="a70fb-143">Konferenzorganisatoren mit Anruffehlern</span><span class="sxs-lookup"><span data-stu-id="a70fb-143">Conference organizers with call failures</span></span>

<span data-ttu-id="a70fb-144">**Benutzer mit Anrufen schlechter Qualität**</span><span class="sxs-lookup"><span data-stu-id="a70fb-144">**Users with poor quality calls**</span></span>

  - <span data-ttu-id="a70fb-145">Benutzer insgesamt mit Anrufen schlechter Qualität</span><span class="sxs-lookup"><span data-stu-id="a70fb-145">Total users with poor quality calls</span></span>

</div>

<div>

## <a name="call-diagnostics"></a><span data-ttu-id="a70fb-146">Anrufdiagnose</span><span class="sxs-lookup"><span data-stu-id="a70fb-146">Call Diagnostics</span></span>

<span data-ttu-id="a70fb-147">Peer-to-Peer</span><span class="sxs-lookup"><span data-stu-id="a70fb-147">Peer-to-peer</span></span>

  - <span data-ttu-id="a70fb-148">Fehler insgesamt</span><span class="sxs-lookup"><span data-stu-id="a70fb-148">Total failures</span></span>

  - <span data-ttu-id="a70fb-149">Fehlerrate insgesamt</span><span class="sxs-lookup"><span data-stu-id="a70fb-149">Overall failure rate</span></span>

  - <span data-ttu-id="a70fb-150">Chatfehlerrate</span><span class="sxs-lookup"><span data-stu-id="a70fb-150">IM failure rate</span></span>

  - <span data-ttu-id="a70fb-151">Audio-Fehlerrate</span><span class="sxs-lookup"><span data-stu-id="a70fb-151">Audio failure rate</span></span>

  - <span data-ttu-id="a70fb-152">Anwendungsfreigabe-Fehlerrate</span><span class="sxs-lookup"><span data-stu-id="a70fb-152">Application sharing failure rate</span></span>

<span data-ttu-id="a70fb-153">Konferenz</span><span class="sxs-lookup"><span data-stu-id="a70fb-153">Conference</span></span>

  - <span data-ttu-id="a70fb-154">Fehler insgesamt</span><span class="sxs-lookup"><span data-stu-id="a70fb-154">Total failures</span></span>

  - <span data-ttu-id="a70fb-155">Fehlerrate insgesamt</span><span class="sxs-lookup"><span data-stu-id="a70fb-155">Overall failure rate</span></span>

  - <span data-ttu-id="a70fb-156">Chatfehlerrate</span><span class="sxs-lookup"><span data-stu-id="a70fb-156">IM failure rate</span></span>

  - <span data-ttu-id="a70fb-157">A/V-Fehlerrate</span><span class="sxs-lookup"><span data-stu-id="a70fb-157">A/V failure rate</span></span>

  - <span data-ttu-id="a70fb-158">Anwendungsfreigabe-Fehlerrate</span><span class="sxs-lookup"><span data-stu-id="a70fb-158">Application sharing failure rate</span></span>

<span data-ttu-id="a70fb-159">Fünf Server mit den meisten fehlerhaften Sitzungen</span><span class="sxs-lookup"><span data-stu-id="a70fb-159">Top five servers by failed sessions</span></span>

</div>

<div>

## <a name="media-quality-diagnostics"></a><span data-ttu-id="a70fb-160">Medienqualitätsdiagnose</span><span class="sxs-lookup"><span data-stu-id="a70fb-160">Media Quality Diagnostics</span></span>

<span data-ttu-id="a70fb-161">Peer-to-Peer</span><span class="sxs-lookup"><span data-stu-id="a70fb-161">Peer-to-peer</span></span>

  - <span data-ttu-id="a70fb-162">Gesamtzahl der Anrufe schlechter Qualität</span><span class="sxs-lookup"><span data-stu-id="a70fb-162">Total poor quality calls</span></span>

  - <span data-ttu-id="a70fb-163">Prozentsatz der Anrufe schlechter Qualität</span><span class="sxs-lookup"><span data-stu-id="a70fb-163">Poor quality call percentage</span></span>

  - <span data-ttu-id="a70fb-164">PSTN-Anrufe schlechter Qualität</span><span class="sxs-lookup"><span data-stu-id="a70fb-164">PSTN calls with poor quality</span></span>

<span data-ttu-id="a70fb-165">Konferenz</span><span class="sxs-lookup"><span data-stu-id="a70fb-165">Conference</span></span>

  - <span data-ttu-id="a70fb-166">Gesamtzahl der Anrufe schlechter Qualität</span><span class="sxs-lookup"><span data-stu-id="a70fb-166">Total poor quality calls</span></span>

  - <span data-ttu-id="a70fb-167">Prozentsatz der Anrufe schlechter Qualität</span><span class="sxs-lookup"><span data-stu-id="a70fb-167">Poor quality call percentage</span></span>

  - <span data-ttu-id="a70fb-168">PSTN-Anrufe schlechter Qualität</span><span class="sxs-lookup"><span data-stu-id="a70fb-168">PSTN calls with poor quality</span></span>

<span data-ttu-id="a70fb-169">Server mit dem höchsten Prozentsatz von Anrufen schlechter Qualität</span><span class="sxs-lookup"><span data-stu-id="a70fb-169">Top worst servers by poor quality call percentage</span></span>

</div>

<div>

## <a name="working-with-the-monitoring-dashboard"></a><span data-ttu-id="a70fb-170">Arbeiten mit dem Monitoring-Dashboard</span><span class="sxs-lookup"><span data-stu-id="a70fb-170">Working with the Monitoring Dashboard</span></span>

<span data-ttu-id="a70fb-p103">Wie bereits erwähnt, werden standardmäßig Gesamtwerte für die aktuelle Woche sowie Trendwerte für die letzten sechs Wochen angezeigt. Wenn Sie Gesamtwerte für den aktuellen Monat (sowie Trendwerte für die letzten sechs Monate) vorziehen, klicken Sie in der oberen rechten Ecke des Dashboards auf den Link **Monatliche Ansicht**. Wenn Sie monatliche Gesamtwerte anzeigen, wird der Text des Links in **Wöchentliche Ansicht** geändert. Durch Klicken auf diesen Link wechseln Sie wieder zur wöchentlichen Ansicht.</span><span class="sxs-lookup"><span data-stu-id="a70fb-p103">As noted, by default totals are shown for the current week and trend values are shown for the past six weeks. If you would prefer to see totals for the current month (as well as trend values for the past six months), click the **Monthly View** link in the upper right corner of the dashboard. If you decide to view monthly totals, the link text will change to **Weekly View**. You can switch back to the weekly view by clicking that link.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="a70fb-p104">Im Monitoring-Dashboard werden Gesamtwerte für die aktuelle Woche (oder den aktuellen Monat) sowie Trendwerte für die letzten sechs Wochen (oder Monate) angezeigt. Diese Zeiträume können nicht geändert werden. Beispielsweise können Sie mit dem Dashboard keine Berichtgesamtwerte für die letzten neun Monate anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a70fb-p104">The Monitoring Dashboard restricts you to looking at totals for the current week (or month) and trend values for the past six weeks (or months). You cannot change these dates and times. For example, you cannot use the Dashboard to view report totals for the time period beginning nine months ago.</span></span>



</div>

<span data-ttu-id="a70fb-p105">Mit den Werten in den Spalten **Diese Woche**, **Dieser Monat** oder **Heute** sind jeweils ausführlichere Informationen verknüpft. Bedenken Sie, dass der Spaltenname und die darin angezeigten Werte oft voneinander abweichen, je nachdem, welche Metrik Sie auswählen und ob Sie die wöchentliche Ansicht oder die monatliche Ansicht ausgewählt haben. Wenn Sie z. B. auf die angezeigten Gesamtwerte für die Metrik **Eindeutige Benutzeranmeldungen** klicken, wird der **Bericht über Benutzerregistrierung** für den angegebenen Zeitraum angezeigt. Durch Klicken auf **Dashboard** können Sie jederzeit wieder zum Monitoring-Dashboard wechseln.</span><span class="sxs-lookup"><span data-stu-id="a70fb-p105">The values shown in the **This week**, **This month**, or **Today** columns link you to more detailed information about the item. Keep in mind that the column name and the values displayed in that column will often differ depending on the metric chosen and depending on whether you have selected weekly view or monthly view. For example, if you click the totals shown for the **Unique user logons** metric you will see the **User Registration Report** for the specified time period. You can return to the Monitoring Dashboard at any time by clicking **Dashboard**.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="a70fb-182">Sie können auch auf die Startseite der Monitoring Server-Berichte zugreifen, indem Sie in der oberen rechten Ecke des Dashboards auf den Link <STRONG>Berichte</STRONG> klicken.</span><span class="sxs-lookup"><span data-stu-id="a70fb-182">You can also access the Monitoring Server Reports home page by clicking the <STRONG>Reports</STRONG> link in the upper right corner of the Dashboard.</span></span>



</div>

<span data-ttu-id="a70fb-183">In der Spalte **Trend** wird ein einfaches Liniendiagramm mit den Gesamtwerten für die letzten sechs Wochen (oder in Abhängigkeit von der Metrik und dem Zeitintervall für die letzten sechs Tage oder die letzten sechs Monate) angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a70fb-183">The **Trend** column displays a simple line graph that shows totals for the past six weeks (or, depending on the metric and the time interval, the past six days or the past six months).</span></span> <span data-ttu-id="a70fb-184">Diese einfachen Liniendiagramme enthalten einen unbeschrifteten Datenpunkt für jeden Zeitraum (z. B. einen unbeschrifteten Datenpunkt für jede der letzten sechs Wochen).</span><span class="sxs-lookup"><span data-stu-id="a70fb-184">These simple line graphs display one unlabeled data point for each time period (for example, one unlabeled data point for each of the past six weeks).</span></span> <span data-ttu-id="a70fb-185">Sie können jedoch tatsächliche Werte für diese Diagramme abrufen, indem Sie mit dem Mauszeiger über das Diagramm fahren.</span><span class="sxs-lookup"><span data-stu-id="a70fb-185">However, you can retrieve actual values for these graphs by holding your mouse pointer over the graph.</span></span> <span data-ttu-id="a70fb-186">In diesem Fall werden in einer QuickInfo die maximalen und niedrigsten Werte im Diagramm angezeigt.</span><span class="sxs-lookup"><span data-stu-id="a70fb-186">In that case, a tooltip shows you the maximum and minimum values in the graph.</span></span>

</div>

<div>

## <a name="exporting-data-from-the-monitoring-dashboard"></a><span data-ttu-id="a70fb-187">Exportieren von Daten aus dem Monitoring-Dashboard</span><span class="sxs-lookup"><span data-stu-id="a70fb-187">Exporting Data from the Monitoring Dashboard</span></span>

<span data-ttu-id="a70fb-p107">Im Monitoring-Dashboard gibt es eine Reihe von Möglichkeiten zum Exportieren der aktuellen Dashboardansicht. In der Symbolleiste des Dashboards wird ein Symbol für eine Diskette mit einem grünen Pfeil angezeigt. Durch Klicken auf dieses Symbol wird eine Dropdownliste mit den folgenden Datenexportformaten angezeigt:</span><span class="sxs-lookup"><span data-stu-id="a70fb-p107">The Monitoring Dashboard provides a number of ways to export the current dashboard view. On the Dashboard toolbar, you'll see an icon that looks like a floppy disk with a green arrow attached to it. If you click this icon, a dropdown list will appear giving you the following data export formats:</span></span>

  - <span data-ttu-id="a70fb-191">XML-Datei mit Berichtsdaten</span><span class="sxs-lookup"><span data-stu-id="a70fb-191">XML file with report data</span></span>

  - <span data-ttu-id="a70fb-192">CSV (Komma als Trennzeichen)</span><span class="sxs-lookup"><span data-stu-id="a70fb-192">CSV (comma delimited)</span></span>

  - <span data-ttu-id="a70fb-193">PDF</span><span class="sxs-lookup"><span data-stu-id="a70fb-193">PDF</span></span>

  - <span data-ttu-id="a70fb-194">MHTML (Webarchiv)</span><span class="sxs-lookup"><span data-stu-id="a70fb-194">MHTML (web archive)</span></span>

  - <span data-ttu-id="a70fb-195">Excel</span><span class="sxs-lookup"><span data-stu-id="a70fb-195">Excel</span></span>

  - <span data-ttu-id="a70fb-196">TIFF-Datei</span><span class="sxs-lookup"><span data-stu-id="a70fb-196">TIFF file</span></span>

  - <span data-ttu-id="a70fb-197">Word</span><span class="sxs-lookup"><span data-stu-id="a70fb-197">Word</span></span>

<span data-ttu-id="a70fb-198">Zum Exportieren der aktuellen Dashboardansicht (und der zugehörigen Werte), klicken Sie auf die gewünschte Exportoption.</span><span class="sxs-lookup"><span data-stu-id="a70fb-198">To export the current dashboard view (and its values), click the desired export option.</span></span> <span data-ttu-id="a70fb-199">Lync Server 2013 generiert einen Bericht im angegebenen Format und gibt Ihnen dann die Möglichkeit, diesen Bericht zu öffnen oder zu speichern.</span><span class="sxs-lookup"><span data-stu-id="a70fb-199">Lync Server 2013 generates a report in the specified format and then give you the option of opening that report or saving it.</span></span> <span data-ttu-id="a70fb-200">Beachten Sie, dass lync Server standardmäßig das Dashboard für die Berichts **Überwachung** Überschriften und im Ordner "Downloads" speichert.</span><span class="sxs-lookup"><span data-stu-id="a70fb-200">Note that, by default, Lync Server titles the report **Monitoring Dashboard** and saves it to your Downloads folder.</span></span> <span data-ttu-id="a70fb-201">Wenn Sie den Bericht anders benennen oder in einem anderen Ordner speichern möchten, klicken Sie auf den Pfeil neben der Schaltfläche **Speichern** und klicken Sie dann auf **Speichern unter**.</span><span class="sxs-lookup"><span data-stu-id="a70fb-201">To give the report a different name or to store it in a different folder, click the arrow next to the **Save** button and then click **Save As**.</span></span> <span data-ttu-id="a70fb-202">Wenn Sie den Namen **Monitoring-Dashboard** übernehmen und den Bericht im Ordner „Downloads“ speichern möchten, können Sie einfach auf die Schaltfläche **Speichern** klicken.</span><span class="sxs-lookup"><span data-stu-id="a70fb-202">If you are fine with name **Monitoring Dashboard** and with having the report saved in the Downloads folder you can just click the **Save** button.</span></span>

<span data-ttu-id="a70fb-p109">Beim Exportieren von Dashboarddaten wird möglicherweise ein **Sicherheitshinweis** angezeigt, dass Ihre aktuellen Einstellungen das Herunterladen dieser Datei nicht zulassen. Führen Sie in diesem Fall die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="a70fb-p109">It's possible that, when you try to export dashboard data, a **Security Alert** dialog box will appear along with the message "Your current settings do not allow this file to be downloaded." If that occurs, do the following:</span></span>

  - <span data-ttu-id="a70fb-205">Wählen Sie in Internet Explorer die Option **Internetoptionen** aus.</span><span class="sxs-lookup"><span data-stu-id="a70fb-205">In Internet Explorer, select **Internet Options**.</span></span>

  - <span data-ttu-id="a70fb-206">Klicken Sie im Dialogfeld **Internetoptionen** auf der Registerkarte **Sicherheit** auf **Vertrauenswürdige Sites** und dann auf **Sites**.</span><span class="sxs-lookup"><span data-stu-id="a70fb-206">In the **Internet Options** dialog box, on the **Security** tab, click **Trusted sites** and then click **Sites**.</span></span>

  - <span data-ttu-id="a70fb-207">Klicken Sie im Dialogfeld **vertrauenswürdige Websites** auf **Hinzufügen** , um den lync Server 2013, der lync Server 2013-Berichte ausführt, den Sammlungen vertrauenswürdiger Websites hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="a70fb-207">In the **Trusted sites** dialog box, click **Add** to add the Lync Server 2013 that is running Lync Server 2013 Reports to the collections of trusted websites.</span></span>

  - <span data-ttu-id="a70fb-208">Klicken Sie auf **Schließen** und dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="a70fb-208">Click **Close** and then click **OK**.</span></span>

<span data-ttu-id="a70fb-p110">Anschließend müssen Sie das Monitoring-Dashboard aktualisieren, damit die Änderungen wirksam werden. Drücken Sie dazu entweder F5 oder klicken in der Symbolleiste des Dashboards auf das Symbol **Aktualisieren**. (Das Symbol **Aktualisieren** ist ein Kreis, in dem sich ein grünes Pfeilpaar befindet.)</span><span class="sxs-lookup"><span data-stu-id="a70fb-p110">You will then need to refresh the Monitoring Dashboard before the changes take effect. To do that, either press F5 or click the **Refresh** icon in the Dashboard toolbar. (The **Refresh** icon is a circle with a pair of green arrows in it.)</span></span>

<span data-ttu-id="a70fb-p111">Sie können auch ein Excel-Arbeitsblatt mit Livedatenfeeds erstellen, das Links zu den neuesten Monitoring-Dashboard-Daten enthält. Zum Erstellen einer Livedatenfeed-Datei klicken Sie in der Symbolleiste auf das orangefarbene Symbol **In Datenfeed exportieren**.</span><span class="sxs-lookup"><span data-stu-id="a70fb-p111">You can also create an Excel spreadsheet that includes live data feeds, which includes links to the latest Monitoring Dashboard data. To create a live data feed file, click the orange **Export to Data Feed** icon in the toolbar.</span></span>

<span data-ttu-id="a70fb-214">Wenn Sie das aktuelle Dashboard drucken möchten, klicken Sie in der Symbolleiste auf das Druckersymbol.</span><span class="sxs-lookup"><span data-stu-id="a70fb-214">If you would prefer to print the current Dashboard then click the printer icon in the toolbar.</span></span>

<span data-ttu-id="a70fb-215"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a70fb-215"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

