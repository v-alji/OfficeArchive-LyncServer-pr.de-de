---
title: 'Lync Server 2013: anzeigen und Analysieren von Monitoring Server-Berichten'
description: 'Lync Server 2013: anzeigen und Analysieren von Monitoring Server-Berichten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing and analyzing monitoring server reports
ms:assetid: 4dd448f1-01d2-49b2-b109-0728f36566b7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720332(v=OCS.15)
ms:contentKeyID: 63969599
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3f2a1812d76a49d487bea35acae3e22ea403f105
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444007"
---
# <a name="viewing-and-analyzing-monitoring-server-reports-in-lync-server-2013"></a><span data-ttu-id="fc24b-103">Anzeigen und Analysieren von Monitoring Server-Berichten in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc24b-103">Viewing and analyzing monitoring server reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fc24b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fc24b-104">

<span> </span></span></span>

<span data-ttu-id="fc24b-105">_**Letztes Änderungsdatum des Themas:** 2014-05-19_</span><span class="sxs-lookup"><span data-stu-id="fc24b-105">_**Topic Last Modified:** 2014-05-19_</span></span>

<span data-ttu-id="fc24b-106">Monitoring Server-Berichte bieten verschiedene Maßnahmen zur Sprachqualität, um die QoE zu überwachen, die an Endbenutzer übermittelt wird.</span><span class="sxs-lookup"><span data-stu-id="fc24b-106">Monitoring Server reports provides several different measures of voice quality to monitor the QoE that is being delivered to end-users.</span></span> <span data-ttu-id="fc24b-107">Darüber hinaus enthält Monitoring Server mehrere integrierte Berichte, die Ihre Organisation verwenden kann, um die Trends zur Verwendung und Medienqualität im Netzwerk Ihrer Organisation zu beobachten und Probleme mit der Medienqualität zu beheben.</span><span class="sxs-lookup"><span data-stu-id="fc24b-107">Additionally, Monitoring Server includes several built-in reports that your organization can use to watch usage and media quality trends on your organization's network and troubleshoot media quality issues that arise.</span></span>

<span data-ttu-id="fc24b-108">Ein primärer Bestandteil des Haltens von Monitoring Server-Berichten, die für tägliche und wöchentliche Vorgänge interessant sind, ist das Anzeigen und Analysieren von Berichten zur Medienqualität, insbesondere:</span><span class="sxs-lookup"><span data-stu-id="fc24b-108">A primary part of keeping Monitoring Server Reports interesting for daily and weekly operations is viewing and analyzing Media Quality Reports, in particular:</span></span>

  - <span data-ttu-id="fc24b-109">QoE-Zusammenfassung/Trend Berichte</span><span class="sxs-lookup"><span data-stu-id="fc24b-109">QoE Summary/Trend Reports</span></span>

  - <span data-ttu-id="fc24b-110">QoE-Leistungsberichte</span><span class="sxs-lookup"><span data-stu-id="fc24b-110">QoE Performance Reports</span></span>

<div>

## <a name="view-reports-from-the-monitoring-server"></a><span data-ttu-id="fc24b-111">Anzeigen von Berichten vom Monitoring Server</span><span class="sxs-lookup"><span data-stu-id="fc24b-111">View reports from the monitoring server</span></span>

1.  <span data-ttu-id="fc24b-112">Suchen Sie in einem Webbrowser nach den Servern, die die SQL Reporting Services hosten.</span><span class="sxs-lookup"><span data-stu-id="fc24b-112">From a web browser, locate your servers hosting the SQL reporting services.</span></span>

2.  <span data-ttu-id="fc24b-113">Zeigen Sie die erforderlichen Berichte über den Browser-Bildschirm an.</span><span class="sxs-lookup"><span data-stu-id="fc24b-113">View the required reports from the browser screen.</span></span>

3.  <span data-ttu-id="fc24b-114">Optional Exportieren eines Berichts durch Auswählen der Exportoption und des erforderlichen Ausgabeformats</span><span class="sxs-lookup"><span data-stu-id="fc24b-114">(Optional) Export a report by selecting the export option and the required output format.</span></span>

</div>

<div>

## <a name="configure-call-detail-recording-cdr"></a><span data-ttu-id="fc24b-115">Konfigurieren der Anrufdetailaufzeichnung (CDR)</span><span class="sxs-lookup"><span data-stu-id="fc24b-115">Configure call detail recording (CDR)</span></span>

1.  <span data-ttu-id="fc24b-116">Melden Sie sich bei einem Benutzerkonto, das ein Mitglied der RTCUniversalServerAdmins-Gruppe ist (oder über entsprechende Berechtigungen verfügt) oder der CsServerAdministrator-oder CsAdministrator-Rolle zugewiesen ist, bei jedem Computer an, der sich in dem Netzwerk befindet, in dem Sie lync Server 2013 bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="fc24b-116">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent permissions), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="fc24b-117">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fc24b-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="fc24b-118">Klicken Sie in der linken Navigationsleiste auf **Überwachung und Archivierung** und dann auf **Aufzeichnung von Kommunikationsdatensätzen**.</span><span class="sxs-lookup"><span data-stu-id="fc24b-118">In the left navigation bar, click **Monitoring and Archiving**, and then click **Call Detail Recording**.</span></span>

4.  <span data-ttu-id="fc24b-119">Klicken Sie auf der Seite **Aufzeichnung von Kommunikationsdatensätzen** in der Tabelle auf den geeigneten Standort, klicken Sie auf **Bearbeiten** und anschließend auf **Details einblenden**.</span><span class="sxs-lookup"><span data-stu-id="fc24b-119">On the **Call Detail Recording** page, click the appropriate site in the table, click **Edit**, and then click **Show Details**.</span></span>

5.  <span data-ttu-id="fc24b-120">Wenn Sie die Bereinigung aktivieren möchten, wählen Sie die Option **zum Entfernen von Überwachungs Servern aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="fc24b-120">To turn on purging, select **Enable Purging for Monitoring Servers**.</span></span>

6.  <span data-ttu-id="fc24b-121">Unter " **Anrufdetails aufzeichnen" für maximale Dauer (Tage):** wählen Sie die maximale Anzahl von Tagen aus, für die Anruf Detail Aufzeichnungen aufbewahrt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fc24b-121">In **Keep call detail recordings for maximum duration (days):** select the maximum number of days that call detail recordings should be retained.</span></span>

7.  <span data-ttu-id="fc24b-122">Wählen Sie unter **Maximale Aufbewahrungsdauer von Fehlerberichtsdaten (in Tagen):** die maximale Anzahl von Tagen, für die Fehlerberichte gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fc24b-122">In **Keep error report data for maximum duration (days):** select the maximum number of days that error reports should be retained.</span></span>

8.  <span data-ttu-id="fc24b-123">Klicken Sie auf **Commit**.</span><span class="sxs-lookup"><span data-stu-id="fc24b-123">Click **Commit**.</span></span>

</div>

<div>

## <a name="configure-qoe"></a><span data-ttu-id="fc24b-124">Konfigurieren von QoE</span><span class="sxs-lookup"><span data-stu-id="fc24b-124">Configure QoE</span></span>

1.  <span data-ttu-id="fc24b-125">Melden Sie sich auf dem Computer als Mitglied der Gruppe "RTCUniversalServerAdmins" oder als Benutzer mit der Rolle "CsVoiceAdministrator", "CsServerAdministrator" oder "CsAdministrator" an.</span><span class="sxs-lookup"><span data-stu-id="fc24b-125">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="fc24b-126">Ausführliche Informationen finden Sie unter Delegate Setup Permissions.</span><span class="sxs-lookup"><span data-stu-id="fc24b-126">For details, see Delegate Setup Permissions.</span></span>

2.  <span data-ttu-id="fc24b-127">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fc24b-127">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="fc24b-128">Klicken Sie in der linken Navigationsleiste auf **Überwachung und Archivierung** und dann auf **QoE-Daten**.</span><span class="sxs-lookup"><span data-stu-id="fc24b-128">In the left navigation bar, click **Monitoring and Archiving**, and then click **Quality of Experience Data**.</span></span>

4.  <span data-ttu-id="fc24b-129">Klicken Sie auf der Seite **QoE-Daten** in der Tabelle auf den geeigneten Standort, klicken Sie auf **Bearbeiten** und anschließend auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="fc24b-129">On the **Quality of Experience Data** page, click the appropriate site from the table, click **Edit**, and then click **Show Details**.</span></span>

5.  <span data-ttu-id="fc24b-130">Wenn Sie die Bereinigung aktivieren möchten, wählen Sie die Option **zum Entfernen von Überwachungs Servern aktivieren** aus.</span><span class="sxs-lookup"><span data-stu-id="fc24b-130">To turn on purging, select **Enable Purging for Monitoring Servers**.</span></span>

6.  <span data-ttu-id="fc24b-131">In " **Anrufdetails aufzeichnen" für maximale Dauer (Tage):** wählen Sie die maximale Anzahl von Tagen aus, die QoE-Daten beibehalten werden sollen.</span><span class="sxs-lookup"><span data-stu-id="fc24b-131">In **Keep call detail recordings for maximum duration (days):** select the maximum number of days that QoE data should be retained.</span></span>

7.  <span data-ttu-id="fc24b-132">Klicken Sie auf Commit ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc24b-132">Click Commit.</span></span>

</div>

<div>

## <a name="change-the-archiving-policy"></a><span data-ttu-id="fc24b-133">Ändern der Archivierungsrichtlinie</span><span class="sxs-lookup"><span data-stu-id="fc24b-133">Change the archiving policy</span></span>

1.  <span data-ttu-id="fc24b-134">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsArchivingAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="fc24b-134">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="fc24b-135">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fc24b-135">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="fc24b-136">Klicken Sie auf der linken Navigationsleiste auf **Überwachung und Archivierung** und anschließend auf **Archivierungsrichtlinie**.</span><span class="sxs-lookup"><span data-stu-id="fc24b-136">In the left navigation bar, click **Monitoring and Archiving**, and then click **Archiving Policy**.</span></span>

4.  <span data-ttu-id="fc24b-137">Klicken Sie in der Liste der Richtlinien auf **Global**, dann auf **Bearbeiten** und anschließend auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="fc24b-137">Click **Global** in the list of policies, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="fc24b-138">Führen Sie im Abschnitt **Bearbeiten der Archivierungsrichtlinie – Global** folgende Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="fc24b-138">In **Edit Archiving Policy - Global**, do the following:</span></span>

6.  <span data-ttu-id="fc24b-139">Aktivieren oder deaktivieren Sie das Kontrollkästchen **interne Kommunikation archivieren** , um die interne Archivierung für die Bereitstellung zu aktivieren oder zu deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="fc24b-139">To enable or disable internal archiving for the deployment, select or clear the **Archive internal communications** check box.</span></span>

7.  <span data-ttu-id="fc24b-140">Wenn Sie die externe Archivierung für die Bereitstellung aktivieren oder deaktivieren möchten, aktivieren oder deaktivieren Sie das Kontrollkästchen **externe Kommunikation archivieren** .</span><span class="sxs-lookup"><span data-stu-id="fc24b-140">To enable or disable external archiving for the deployment, select or clear the **Archive external communications** check box.</span></span>

8.  <span data-ttu-id="fc24b-141">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="fc24b-141">Click **Commit**.</span></span>

</div>

<div>

## <a name="apply-an-archiving-policy-to-a-user"></a><span data-ttu-id="fc24b-142">Anwenden einer Archivierungsrichtlinie auf einen Benutzer</span><span class="sxs-lookup"><span data-stu-id="fc24b-142">Apply an archiving policy to a user</span></span>

1.  <span data-ttu-id="fc24b-143">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsArchivingAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="fc24b-143">From a user account that is assigned to the CsArchivingAdministrator or CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="fc24b-144">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="fc24b-144">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span>

3.  <span data-ttu-id="fc24b-145">Klicken Sie in der linken Navigationsleiste auf **Benutzer** und suchen Sie anschließend nach dem Benutzerkonto, das Sie konfigurieren möchten.</span><span class="sxs-lookup"><span data-stu-id="fc24b-145">In the left navigation bar, click **Users**, and then search on the user account that you want to configure.</span></span>

4.  <span data-ttu-id="fc24b-146">Klicken Sie in der Tabelle mit den Suchergebnissen auf das Benutzerkonto, klicken Sie auf **Bearbeiten** und dann auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="fc24b-146">In the table that lists the search results, click the user account, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="fc24b-147">Wählen Sie in **lync Server-Benutzer bearbeiten** unter **Archivierungsrichtlinie** die Archivierungs Benutzerrichtlinie aus, die Sie anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="fc24b-147">In **Edit Lync Server User** under **Archiving policy**, select the archiving user policy that you want to apply.</span></span>

6.  <span data-ttu-id="fc24b-148">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="fc24b-148">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fc24b-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc24b-149">See Also</span></span>


[<span data-ttu-id="fc24b-150">Verwenden von Überwachungsberichten in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc24b-150">Using Monitoring Reports in Lync Server 2013</span></span>](lync-server-2013-using-monitoring-reports.md)  
[<span data-ttu-id="fc24b-151">Bericht zur Server Leistung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc24b-151">Server Performance Report in Lync Server 2013</span></span>](lync-server-2013-server-performance-report.md)  
[<span data-ttu-id="fc24b-152">Bericht zum Vergleich der Medienqualität in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fc24b-152">Media Quality Comparison Report in Lync Server 2013</span></span>](lync-server-2013-media-quality-comparison-report.md)  
  

<span data-ttu-id="fc24b-153"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fc24b-153"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

