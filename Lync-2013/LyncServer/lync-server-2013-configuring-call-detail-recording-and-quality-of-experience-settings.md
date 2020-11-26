---
title: Konfigurieren von KDS- (Aufzeichnung von Kommunikationsdatensätzen) und QoE-Einstellungen
description: Konfigurieren der Aufzeichnung von Anrufdetails und Einstellungen für die Qualität der Benutzerfreundlichkeit
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring call detail recording and Quality of Experience settings
ms:assetid: 009a0499-4f8c-450d-9c72-a565a08e9f7a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204621(v=OCS.15)
ms:contentKeyID: 48183223
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be0238701f561e6694786faec7fc914dcc9cda40
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433255"
---
# <a name="configuring-call-detail-recording-and-quality-of-experience-settings-in-lync-server-2013"></a><span data-ttu-id="3e7fb-103">Konfigurieren der Einstellungen für die Anrufdetailaufzeichnung und die Qualität der Benutzerfreundlichkeit in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e7fb-103">Configuring call detail recording and Quality of Experience settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3e7fb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3e7fb-104">

<span> </span></span></span>

<span data-ttu-id="3e7fb-105">_**Letztes Änderungsdatum des Themas:** 2012-10-17_</span><span class="sxs-lookup"><span data-stu-id="3e7fb-105">_**Topic Last Modified:** 2012-10-17_</span></span>

<span data-ttu-id="3e7fb-106">Nachdem Sie einen Überwachungsspeicher mit einem Front-End-Pool verknüpft, den Überwachungsspeicher eingerichtet und dann SQL Server Reporting Services-und Überwachungsberichte installiert und konfiguriert haben, können Sie die Datenaufzeichnung (CDR) und die Quality of Experience (QoE)-Überwachung mithilfe der lync Server-Verwaltungsshell verwalten.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-106">After you have associated a monitoring store with a Front End pool, set up the monitoring store, and then installed and configured SQL Server Reporting Services and Monitoring Reports you can manage Call Detail Recording (CDR) and Quality of Experience (QoE) monitoring by using Lync Server Management Shell.</span></span> <span data-ttu-id="3e7fb-107">Cmdlets der lync Server-Verwaltungsshell ermöglichen es Ihnen, die CDR-und/oder QoE-Überwachung für eine bestimmte Website oder für die gesamte lync Server-Bereitstellung zu aktivieren und zu deaktivieren. Dies kann mit einem einfachen Befehl erfolgen:</span><span class="sxs-lookup"><span data-stu-id="3e7fb-107">Lync Server Management Shell cmdlets allow you to enable and disable CDR and/or QoE monitoring for a particular site or for your entire Lync Server deployment; that can be done with a command as simple as this:</span></span>

    Set-CsQoEConfiguration -Identity "global" -EnableQoE $False

<span data-ttu-id="3e7fb-108">Wenn Sie Microsoft lync Server 2013 installieren, können Sie auch eine vordefinierte Sammlung globaler Konfigurationseinstellungen für CDR und QoE installieren.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-108">When you install Microsoft Lync Server 2013, you will also install a predefined collection of global configuration settings for both CDR and QoE.</span></span> <span data-ttu-id="3e7fb-109">In der folgenden Tabelle sind Standardwerte für einige gängige Einstellungen für die Aufzeichnung von Kommunikationsdatensätzen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="3e7fb-109">Default values for some of the more commonly-used settings used by Call Detail Recording are shown in the following table:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e7fb-110">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3e7fb-110">Property</span></span></th>
<th><span data-ttu-id="3e7fb-111">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e7fb-111">Description</span></span></th>
<th><span data-ttu-id="3e7fb-112">Standardwert</span><span class="sxs-lookup"><span data-stu-id="3e7fb-112">Default Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e7fb-113">EnableCDR</span><span class="sxs-lookup"><span data-stu-id="3e7fb-113">EnableCDR</span></span></p></td>
<td><p><span data-ttu-id="3e7fb-p103">Gibt an, ob KDS aktiviert ist. Bei „True“ werden alle KDS-Datensätze gesammelt und in die Überwachungsdatenbank geschrieben.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-p103">Indicates whether or not CDR is enabled. If True, all CDR records will be collected and written to the monitoring database.</span></span></p></td>
<td><p><span data-ttu-id="3e7fb-116">True</span><span class="sxs-lookup"><span data-stu-id="3e7fb-116">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e7fb-117">EnablePurging</span><span class="sxs-lookup"><span data-stu-id="3e7fb-117">EnablePurging</span></span></p></td>
<td><p><span data-ttu-id="3e7fb-p104">Gibt an, ob KDS-Datensätze regelmäßig aus der Datenbank gelöscht werden. Bei Festlegung auf „True“ werden Einträge nach dem Zeitraum gelöscht, der in den Eigenschaften „KeepCallDetailForDays“ (KDS-Datensätze) und „KeepErrorReportForDays“ (KDS-Fehler) angegeben ist. Bei Festlegung des Parameters auf „False“ werden KDS-Einträge nie gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-p104">Indicates whether or not CDR records will periodically be deleted from the database. If True, records will be deleted after the time period specified by the properties KeepCallDetailForDays (for CDR records) and KeepErrorReportForDays (for CDR errors). If False, CDR records will be maintained indefinitely.</span></span></p></td>
<td><p><span data-ttu-id="3e7fb-121">True</span><span class="sxs-lookup"><span data-stu-id="3e7fb-121">True</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e7fb-122">KeepCallDetailForDays</span><span class="sxs-lookup"><span data-stu-id="3e7fb-122">KeepCallDetailForDays</span></span></p></td>
<td><p><span data-ttu-id="3e7fb-p105">Gibt die Anzahl von Tagen an, die KDS-Datensätze in der Datenbank gespeichert werden. Einträge, die älter sind als angegeben, werden automatisch gelöscht. Dies erfolgt jedoch nur, wenn der Löschvorgang aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-p105">Indicates the number of days that CDR records will be kept in the database; any records older than the specified number of days will automatically be deleted. However, this will occur only if purging has been enabled.</span></span></p>
<p><span data-ttu-id="3e7fb-125">„KeepCallDetailForDays“ kann auf einen beliebigen ganzzahligen Wert zwischen 1 und 2562 Tage (ungefähr 7 Jahre) festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-125">KeepCallDetailForDays can be set to any integer value between 1 and 2562 days (approximately 7 years).</span></span></p></td>
<td><p><span data-ttu-id="3e7fb-126">60 Tage</span><span class="sxs-lookup"><span data-stu-id="3e7fb-126">60 days</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e7fb-127">KeepErrorReportForDays</span><span class="sxs-lookup"><span data-stu-id="3e7fb-127">KeepErrorReportForDays</span></span></p></td>
<td><p><span data-ttu-id="3e7fb-128">Gibt an, wie viele Tage CdR-Fehlerberichte aufbewahrt werden. Alle Berichte, die älter als die angegebene Anzahl von Tagen sind, werden automatisch gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-128">Indicates the number of days that CDR error reports are kept; any reports older than the specified number of days will automatically be deleted.</span></span> <span data-ttu-id="3e7fb-129">CdR-Fehlerberichte sind Diagnoseberichte, die von Clientanwendungen wie Microsoft lync 2013 hochgeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-129">CDR error reports are diagnostic reports uploaded by client applications such as Microsoft Lync 2013.</span></span></p>
<p><span data-ttu-id="3e7fb-130">Sie können diese Eigenschaft auf einen beliebigen ganzzahligen Wert zwischen 1 und 2562 Tage (etwa 7 Jahre) festlegen.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-130">You can set this property to any integer value between 1 and 2562 days.</span></span></p></td>
<td><p><span data-ttu-id="3e7fb-131">60 Tage</span><span class="sxs-lookup"><span data-stu-id="3e7fb-131">60 days</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3e7fb-132">Entsprechend werden in dieser Tabelle Standardwerte für ausgewählte QoE-Einstellungen aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="3e7fb-132">Similarly, default values for selected QoE settings are shown in this table:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e7fb-133">Eigenschaft</span><span class="sxs-lookup"><span data-stu-id="3e7fb-133">Property</span></span></th>
<th><span data-ttu-id="3e7fb-134">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="3e7fb-134">Description</span></span></th>
<th><span data-ttu-id="3e7fb-135">Standardwert</span><span class="sxs-lookup"><span data-stu-id="3e7fb-135">Default Value</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e7fb-136">EnableQoE</span><span class="sxs-lookup"><span data-stu-id="3e7fb-136">EnableQoE</span></span></p></td>
<td><p><span data-ttu-id="3e7fb-p107">Gibt an, ob die QoE-Überwachung aktiviert ist. Bei Festlegung auf „True“ werden alle QoE-Datensätze gesammelt und in die Überwachungsdatenbank geschrieben.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-p107">Indicates whether or not QoE monitoring is enabled. If True, all QoE records will be collected and written to the monitoring database.</span></span></p></td>
<td><p><span data-ttu-id="3e7fb-139">True</span><span class="sxs-lookup"><span data-stu-id="3e7fb-139">True</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="3e7fb-140">EnablePurging</span><span class="sxs-lookup"><span data-stu-id="3e7fb-140">EnablePurging</span></span></p></td>
<td><p><span data-ttu-id="3e7fb-p108">Gibt an, ob QoE-Datensätze regelmäßig aus der Datenbank gelöscht werden oder nicht. Wenn dieser Parameter auf „True“ festgelegt ist, werden die Einträge nach der über die Eigenschaft „KeepQoEDataForDays“ angegebenen Zeitdauer gelöscht. Bei Festlegung des Parameters auf „False“ werden QoE-Datensätze nie gelöscht.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-p108">Indicates whether or not QoE records will periodically be deleted from the database. If True, records will be deleted after the time period specified by the KeepQoEDataForDays property. If False, QoE records will be maintained indefinitely.</span></span></p></td>
<td><p><span data-ttu-id="3e7fb-144">True</span><span class="sxs-lookup"><span data-stu-id="3e7fb-144">True</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="3e7fb-145">KeepQoEDataForDays</span><span class="sxs-lookup"><span data-stu-id="3e7fb-145">KeepQoEDataForDays</span></span></p></td>
<td><p><span data-ttu-id="3e7fb-p109">Gibt die Anzahl von Tagen an, die QoE-Datensätze in der Datenbank gespeichert werden. Einträge, die älter sind als angegeben, werden automatisch gelöscht. Dies erfolgt jedoch nur, wenn der Löschvorgang aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-p109">Indicates the number of days that QoE records will be kept in the database; any records older than the specified number of days will automatically be deleted. However, this will occur only if purging has been enabled.</span></span></p>
<p><span data-ttu-id="3e7fb-148">„KeepCallDetailForDays“ kann auf einen beliebigen Ganzzahlwert zwischen einschließlich 1 und 2562 Tage gesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-148">KeepCallDetailForDays can be set to any integer value between 1 and 2562 days.</span></span></p></td>
<td><p><span data-ttu-id="3e7fb-149">60 Tage</span><span class="sxs-lookup"><span data-stu-id="3e7fb-149">60 days</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="3e7fb-150">Wenn Sie diese globalen Einstellungen ändern müssen, können Sie dazu die Cmdlets „Set-CsCdrConfiguration“ und „Set-CsQoEConfiguration“ verwenden.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-150">If you need to modify these global settings you can do so by using the Set-CsCdrConfiguration and the Set-CsQoEConfiguration cmdlets.</span></span> <span data-ttu-id="3e7fb-151">Mit diesem Befehl (der in der lync Server-Verwaltungsshell ausgeführt wird) wird beispielsweise die CDR-Überwachung im globalen Bereich deaktiviert. Dies erfolgt durch Festlegen der EnableCDR-Eigenschaft auf "false" ($false):</span><span class="sxs-lookup"><span data-stu-id="3e7fb-151">For example, this command (run from within the Lync Server Management Shell) disables CDR monitoring at the global scope; that's done by setting the EnableCDR property to False ($False):</span></span>

    Set-CsCdrConfiguration -Identity "global" -EnableCDR $False

<span data-ttu-id="3e7fb-152">Durch das Deaktivieren der Überwachung wird weder die Zuordnung des Überwachungsspeichers zum Front-End-Pool aufgehoben, noch wird die Back-End-Überwachungsdatenbank deinstalliert oder anderweitig geändert.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-152">Note that disabling monitoring does not dissociate the monitoring store from the Front End pool, nor does it uninstall or otherwise affect the backend monitoring database.</span></span> <span data-ttu-id="3e7fb-153">Wenn Sie die lync Server-Verwaltungsshell zum Deaktivieren der CDR-oder QoE-Überwachung verwenden, müssen Sie lync Server vorübergehend nicht mehr für das Sammeln und Archivieren von Überwachungsdaten verwenden.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-153">When you use Lync Server Management Shell to disable either CDR or QoE monitoring all you really do is temporarily stop Lync Server from collecting and archiving monitoring data.</span></span> <span data-ttu-id="3e7fb-154">Wenn Sie in diesem Fall das Sammeln und Archivieren von KDS-Daten fortsetzen möchten, müssen Sie nur die Eigenschaft „EnableCDR“ wieder auf „True“ ($True) festlegen:</span><span class="sxs-lookup"><span data-stu-id="3e7fb-154">If you want to resume, in this case, the collection and archiving of CDR data, all you need to do is set the EnableCDR property back to True ($True):</span></span>

    Set-CsCdrConfiguration -Identity "global" -EnableCDR $True

<span data-ttu-id="3e7fb-155">Entsprechend deaktiviert dieser Befehl den Löschvorgang für QoE-Datensätze auf globaler Ebene:</span><span class="sxs-lookup"><span data-stu-id="3e7fb-155">Similarly, this command disables the purging of QoE records at the global scope:</span></span>

    Set-CsQoEConfiguration -Identity "global" -EnablePurging $False

<span data-ttu-id="3e7fb-p112">Neben den globalen Einstellungen können KDS- und QoE-Konfigurationseinstellungen auch auf Standortebene zugewiesen werden. Dadurch wird die Verwaltung bei der Überwachung flexibler gestaltet; ein Administrator kann beispielsweise die KDS-Überwachung für den Standort Redmond aktivieren, für den Standort Dublin jedoch deaktivieren. Verwenden Sie einen Befehl wie den folgenden, um neue KDS-Konfigurationseinstellungen auf Standortebene zu erstellen:</span><span class="sxs-lookup"><span data-stu-id="3e7fb-p112">In addition to the global settings, CDR and QoE configurations settings can be assigned to the site scope. This provides additional management flexibility when it comes to monitoring; for example, an administrator can enable CDR monitoring for the Redmond site but disable CDR monitoring for the Dublin site. To create new CDR configuration settings at the site scope, use a command similar to this:</span></span>

    New-CsCdrConfiguration -Identity "site:Redmond" -EnableCDR $False

<span data-ttu-id="3e7fb-p113">Beachten Sie, dass Einstellungen auf Standortebene Vorrang vor globalen Einstellungen haben. Angenommen, die KDS-Überwachung ist auf globaler Ebene aktiviert, auf Standortebene (für den Standort Redmond) jedoch deaktiviert. Das bedeutet, dass für Benutzer am Standort Redmond keine Kommunikationsdatensätze aufgezeichnet werden. Für Benutzer an anderen Standorten (die von den globalen Einstellungen statt den Einstellungen für den Standort Redmond verwaltet werden), werden jedoch Kommunikationsdatensätze archiviert.</span><span class="sxs-lookup"><span data-stu-id="3e7fb-p113">Keep in mind that settings configured at the site scope take precedence over settings configured at the global scope. For example, suppose CDR monitoring is enabled at the global scope, but disabled at the site scope (for the Redmond site). That means that call detail recording information will not be archived for users in the Redmond site. However, users in other sites (that is, users managed by the global settings instead of the Redmond site settings) will have their call detail recording information archived.</span></span>

<span data-ttu-id="3e7fb-163">Neue QoE-Konfigurationseinstellungen auf Standortebene können mit einem Befehl wie dem folgenden erstellt werden:</span><span class="sxs-lookup"><span data-stu-id="3e7fb-163">New QoE configuration settings can be created at the site scope by using a command like this one:</span></span>

    New-CsQoEConfiguration -Identity "site:Redmond" -KeepQoEDataForDays 15

<span data-ttu-id="3e7fb-164">Wenn Sie weitere Informationen wünschen, geben Sie in der lync Server-Verwaltungsshell die folgenden Befehle ein:</span><span class="sxs-lookup"><span data-stu-id="3e7fb-164">For more information, type the following commands from within the Lync Server Management Shell:</span></span>

    Get-Help New-CsCdrConfiguration | more
    Get-Help Set-CsCdrConfiguration | more
    Get-Help New-CsQoEConfiguration | more
    Get-Help Set-CsQoEConfiguration | more

<span data-ttu-id="3e7fb-165"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3e7fb-165"></div>

<span> </span>

</div>

</div>

</span></span></div>

