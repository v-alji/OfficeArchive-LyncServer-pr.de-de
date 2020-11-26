---
title: 'Lync Server 2013: Angeben der Beibehaltung von CDR-Daten'
description: 'Lync Server 2013: Angeben der Beibehaltung von CDR-Daten'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Specifying retention of CDR data
ms:assetid: c0fd6056-87bc-4136-902a-f1b37cd3a1ca
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182581(v=OCS.15)
ms:contentKeyID: 48185299
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d9367721a2390ad701702818590ac14e69da0df9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423785"
---
# <a name="specifying-retention-of-cdr-data-in-lync-server-2013"></a><span data-ttu-id="4f0a7-103">Angeben der Beibehaltung von CDR-Daten in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4f0a7-103">Specifying retention of CDR data in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4f0a7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4f0a7-104">

<span> </span></span></span>

<span data-ttu-id="4f0a7-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="4f0a7-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="4f0a7-p101">In der Standardeinstellung werden Daten zur Aufzeichnung von Kommunikationsdatensätzen (KDS) nach 60 Tagen gelöscht. Sie können die Einstellungen auf der Seite **Aufzeichnung von Kommunikationsdatensätzen** verwenden, um die Daten für einen längeren oder kürzeren Zeitraum zu speichern. Wenn Sie KDS deaktivieren, werden auch Daten gelöscht, die bei aktivierter KDS-Datenerfassung aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="4f0a7-p101">By default, call detail recording (CDR) data is purged after 60 days. You can use the settings on the **Call Detail Recording** page to retain the data for a longer or shorter period of time. If you disable CDR, data that was captured before CDR was enabled will also be subject to purging.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="4f0a7-p102">Sie sollten die Aufzeichnung von Kommunikationsdatensätzen (KDS) und QoE-Daten (Quality of Experience) so konfigurieren, dass Daten für die gleiche Anzahl von Tagen gespeichert werden. Die Berichte zu den aufgezeichneten Kommunikationsdatensätzen (KDS), verfügbar auf der Webseite für Monitoring Server-Berichte, umfassen KDS- und QoE-Informationen zu jedem Anruf. Wenn die Zeit bis zum Löschen für KDS und QoE abweicht, umfassen einige Anrufe möglicherweise nur KDS-Daten, während andere ausschließlich QoE-Daten aufweisen.</span><span class="sxs-lookup"><span data-stu-id="4f0a7-p102">You should configure CDR and Quality of Experience (QoE) to retain data for the same number of days. Each call in the call detail reports (CDRs), available from the Monitoring Server Reports webpage, includes CDR and QoE information. If the purging duration for CDR and QoE is different, some calls might only include CDR data, while other may only include QoE data.</span></span>



</div>

<span data-ttu-id="4f0a7-112">Verwenden Sie die folgenden Verfahren, um Bereinigungseinstellungen für KDS-Daten zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="4f0a7-112">Use the following procedures to configure purge settings for CDR data.</span></span>

<div>

## <a name="to-specify-retention-of-cdr-data"></a><span data-ttu-id="4f0a7-113">So geben Sie die Beibehaltungsdauer für KDS-Daten an</span><span class="sxs-lookup"><span data-stu-id="4f0a7-113">To specify retention of CDR data</span></span>

1.  <span data-ttu-id="4f0a7-114">Melden Sie sich bei einem Benutzerkonto, das ein Mitglied der RTCUniversalServerAdmins-Gruppe ist (oder über entsprechende Benutzerrechte verfügt) oder der CsServerAdministrator-oder CsAdministrator-Rolle zugewiesen ist, bei jedem Computer an, der sich in dem Netzwerk befindet, in dem Sie lync Server 2013 bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="4f0a7-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="4f0a7-115">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="4f0a7-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="4f0a7-116">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="4f0a7-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="4f0a7-117">Klicken Sie in der linken Navigationsleiste auf **Überwachung und Archivierung** und dann auf **Aufzeichnung von Kommunikationsdatensätzen**.</span><span class="sxs-lookup"><span data-stu-id="4f0a7-117">In the left navigation bar, click **Monitoring and Archiving**, and then click **Call Detail Recording**.</span></span>

4.  <span data-ttu-id="4f0a7-118">Klicken Sie auf der Seite **Aufzeichnung von Kommunikationsdatensätzen** in der Tabelle auf den geeigneten Standort, klicken Sie auf **Bearbeiten** und anschließend auf **Details einblenden**.</span><span class="sxs-lookup"><span data-stu-id="4f0a7-118">On the **Call Detail Recording** page, click the appropriate site in the table, click **Edit**, and then click **Show Details**.</span></span>

5.  <span data-ttu-id="4f0a7-119">Wählen Sie **Bereinigung von KDS-Aufzeichnungen aktivieren** aus, um die Bereinigung zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="4f0a7-119">To turn on purging, select **Enable purging of CDRs**.</span></span>

6.  <span data-ttu-id="4f0a7-120">Wählen Sie unter **Maximale Aufbewahrungsdauer für KDS-Aufzeichnungen (in Tagen):** die maximale Anzahl von Tagen aus, für die KDS-Aufzeichnungen gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4f0a7-120">In **Keep CDRs for maximum duration (days):** select the maximum number of days that call detail recordings should be retained.</span></span>

7.  <span data-ttu-id="4f0a7-121">Wählen Sie unter **Maximale Aufbewahrungsdauer von Fehlerberichtsdaten (in Tagen):** die maximale Anzahl von Tagen, für die Fehlerberichte gespeichert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="4f0a7-121">In **Keep error report data for maximum duration (days):** select the maximum number of days that error reports should be retained.</span></span>

8.  <span data-ttu-id="4f0a7-122">Klicken Sie auf **Commit**.</span><span class="sxs-lookup"><span data-stu-id="4f0a7-122">Click **Commit**.</span></span>

</div>

<div>

## <a name="specifying-cdr-retention-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="4f0a7-123">Angeben der CDR-Aufbewahrung mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="4f0a7-123">Specifying CDR Retention by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="4f0a7-124">Sie können CdR-Aufbewahrungseinstellungen mithilfe von Windows PowerShell und dem Set-CsCdrConfiguration-Cmdlet erstellen.</span><span class="sxs-lookup"><span data-stu-id="4f0a7-124">You can create CDR retention settings by using Windows PowerShell and the Set-CsCdrConfiguration cmdlet.</span></span> <span data-ttu-id="4f0a7-125">Sie können dieses Cmdlet entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="4f0a7-125">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="4f0a7-126">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="4f0a7-126">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-specify-cdr-retention-for-a-specific-location"></a><span data-ttu-id="4f0a7-127">So geben Sie die Beibehaltungsdauer für KDS-Daten für einen bestimmten Standort an</span><span class="sxs-lookup"><span data-stu-id="4f0a7-127">To specify CDR retention for a specific location</span></span>

  - <span data-ttu-id="4f0a7-128">Mit diesem Befehl werden KDS-Daten für den Standort „Redmond“ bereinigt und außerdem wird für den Standort konfiguriert, dass sowohl KDS-Daten als auch Fehlerberichtdaten 20 Tage lang aufbewahrt werden.</span><span class="sxs-lookup"><span data-stu-id="4f0a7-128">This command enables purging of CDR data for the Redmond site, and configures the site to maintain both CDR data and error reports data for 20 days.</span></span>
    
        Set-CsCdrConfiguration -Identity "site:Redmond" -EnablePurging -KeepCallDetailForDays 20 -KeepErrorReportForDays 20

</div>

<div>

## <a name="to-specify-cdr-retention-for-multiple-locations"></a><span data-ttu-id="4f0a7-129">So geben Sie die Beibehaltungsdauer für KDS-Daten für mehrere Standorte an</span><span class="sxs-lookup"><span data-stu-id="4f0a7-129">To specify CDR retention for multiple locations</span></span>

  - <span data-ttu-id="4f0a7-130">Mit diesem Befehl wird die Beibehaltung von KDS-Daten für alle in einer Organisation verwendeten KDS-Konfigurationseinstellungen konfiguriert.</span><span class="sxs-lookup"><span data-stu-id="4f0a7-130">This command configures CDR retention for all the CDR configuration settings in use in an organization.</span></span>
    
        Get-CsCdrConfiguration | Set-CsCdrConfiguration-EnablePurging -KeepCallDetailForDays 20 -KeepErrorReportForDays 20

</div>

<span data-ttu-id="4f0a7-131">Weitere Informationen finden Sie im Hilfethema zum Cmdlet " [Satz-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) ".</span><span class="sxs-lookup"><span data-stu-id="4f0a7-131">For more information, see the help topic for the [Set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="4f0a7-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4f0a7-132">See Also</span></span>


[<span data-ttu-id="4f0a7-133">Anrufdetailaufzeichnung (CDR) in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4f0a7-133">Call detail recording (CDR) in Lync Server 2013</span></span>](lync-server-2013-call-detail-recording-cdr.md)  
  

<span data-ttu-id="4f0a7-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4f0a7-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

