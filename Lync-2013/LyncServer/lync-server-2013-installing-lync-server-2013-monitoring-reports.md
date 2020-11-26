---
title: 'Lync Server 2013: Installieren von lync Server 2013-Überwachungsberichten'
description: 'Lync Server 2013: Installieren von lync Server 2013-Überwachungsberichten'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Installing Lync Server 2013 Monitoring Reports
ms:assetid: 6f417569-b100-442c-ad48-fdd794626cf7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204989(v=OCS.15)
ms:contentKeyID: 48184445
ms.date: 02/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12405f786cbaf095e97f526fae2e1c2d3cb45c32
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427040"
---
# <a name="installing-lync-server-2013-monitoring-reports"></a><span data-ttu-id="b1376-103">Installieren von lync Server 2013-Überwachungsberichten</span><span class="sxs-lookup"><span data-stu-id="b1376-103">Installing Lync Server 2013 Monitoring Reports</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b1376-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b1376-104">

<span> </span></span></span>

<span data-ttu-id="b1376-105">_**Letztes Änderungsdatum des Themas:** 2015-02-27_</span><span class="sxs-lookup"><span data-stu-id="b1376-105">_**Topic Last Modified:** 2015-02-27_</span></span>

<span data-ttu-id="b1376-106">Microsoft lync Server 2013-Überwachungsberichte bieten Ihnen eine Fülle von Informationen über die Qualität und Quantität der Kommunikationssitzungen, die in Ihrer Organisation stattfinden.</span><span class="sxs-lookup"><span data-stu-id="b1376-106">Microsoft Lync Server 2013 Monitoring Reports provide you with a wealth of information about the quality and quantity of the communication sessions that take place in your organization.</span></span> <span data-ttu-id="b1376-107">Überwachungsberichte werden jedoch nicht automatisch installiert, wenn Sie lync Server 2013 installieren. Stattdessen müssen Sie die Überwachungsberichte separat und erst nach der Installation von lync Server auf dem Computer installieren.</span><span class="sxs-lookup"><span data-stu-id="b1376-107">However, Monitoring Reports are not automatically installed when you install Lync Server 2013; instead, you must install Monitoring Reports separately, and only after Lync Server has been installed on the computer.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b1376-p102">Es empfiehlt sich, die Überwachungsberichte auf demselben Computer zu installieren, auf dem auch die Überwachungsdatenbank installiert ist. Somit wird die Zuweisung von Zugriffsberechtigungen für die Berichte vereinfacht: wenn die Überwachungsberichte auf dem Computer installiert sind, der auch als Host für den Überwachungsspeicher fungiert, müssen Sie keine Berechtigungen zuweisen, die einer Datenbank auf dem Computer gestatten, mit Reporting Services zu interagieren, wenn diese auf einem zweiten Computer ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="b1376-p102">It is recommended that you install Monitoring Reports on the same computer where the monitoring database is installed. This simplifies the process of assigning permissions for accessing the reports: installing Monitoring Reports on the computer that hosts the monitoring store means that you will not have to configure permissions that allow a database on one computer to interact with Reporting Services running on a second computer.</span></span>



</div>

<span data-ttu-id="b1376-110">Zu den lync Server-Überwachungsberichten gehören mehr als 30 Berichte, die detaillierte Informationen zu Konferenzen, Peer-to-Peer-Chatsitzungen, Benutzerregistrierungen, der reaktionsgruppenanwendung und vielem mehr bieten.</span><span class="sxs-lookup"><span data-stu-id="b1376-110">Lync Server Monitoring Reports include over 30 reports designed to provide detailed information about conferences, peer-to-peer IM sessions, user registrations, the Response Group application, and much more.</span></span> <span data-ttu-id="b1376-111">Für die 2013-Version umfassen lync Server-Überwachungsberichte eine Reihe von Verbesserungen:</span><span class="sxs-lookup"><span data-stu-id="b1376-111">For the 2013 version, Lync Server Monitoring Reports include a number of enhancements:</span></span>

  - <span data-ttu-id="b1376-112">**Neue Berichte zur Sprachqualität**.</span><span class="sxs-lookup"><span data-stu-id="b1376-112">**New voice quality reports**.</span></span> <span data-ttu-id="b1376-113">Diese neuen Berichte umfassen den [Bericht "Medien Qualitätsvergleich" in lync Server 2013, in](lync-server-2013-media-quality-comparison-report.md)dem die Qualität zwischen verschiedenen Anrufarten verglichen wird (beispielsweise zwischen kabelgebundenen anrufen und drahtlosen anrufen). und den [Bericht zur Teilnahme an der Konferenz in lync Server 2013, in](lync-server-2013-conference-join-time-report.md)dem Informationen zur Zeitdauer bereitgestellt werden, die für Benutzer für die Teilnahme an einer Konferenz erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="b1376-113">These new reports include the [Media Quality Comparison Report in Lync Server 2013](lync-server-2013-media-quality-comparison-report.md), which compares quality between different types of calls (for example, between wired calls and wireless calls); and the [Conference Join Time Report in Lync Server 2013](lync-server-2013-conference-join-time-report.md), which provides information regarding the amount of time requires for users to join a conference.</span></span>

  - <span data-ttu-id="b1376-114">**Verbesserte Berichte zur Analyse und Problembehandlung bei Video- und Anwendungsfreigabesitzungen.**</span><span class="sxs-lookup"><span data-stu-id="b1376-114">**Improved reports for analyzing and troubleshooting both video and application sharing sessions.**</span></span> <span data-ttu-id="b1376-115">Der [Bericht zur Zusammenfassung der Medienqualität in lync Server 2013](lync-server-2013-media-quality-summary-report.md) bietet eine Möglichkeit, Video-und Anwendungsfreigabe Aufrufe zu analysieren, während der [Server Leistungsbericht in lync Server 2013](lync-server-2013-server-performance-report.md) die Leistung der Server beschreibt, die diese Anrufe generieren.</span><span class="sxs-lookup"><span data-stu-id="b1376-115">The [Media Quality Summary Report in Lync Server 2013](lync-server-2013-media-quality-summary-report.md) provides a way to analyze video and application sharing calls, while the [Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md) details the performance of servers generating these calls.</span></span> <span data-ttu-id="b1376-116">Video-und Anwendungsfreigabe Metriken werden jetzt auch vom [Peer-zu-Peer-Sitzungs Detailbericht in lync Server 2013](lync-server-2013-peer-to-peer-session-detail-report.md) und dem [Konferenz Detailbericht in lync Server 2013](lync-server-2013-conference-detail-report.md)gemeldet.</span><span class="sxs-lookup"><span data-stu-id="b1376-116">Video and application sharing metrics are also now reported by the [Peer-to-Peer Session Detail Report in Lync Server 2013](lync-server-2013-peer-to-peer-session-detail-report.md) and the [Conference Detail Report in Lync Server 2013](lync-server-2013-conference-detail-report.md).</span></span>

  - <span data-ttu-id="b1376-p106">**Verbesserte Berichtsleistung**. Dazu gehören kürzere Reaktions- und Datenabrufzeiten sowie eine schnellere und einfachere Navigation durch die Berichte.</span><span class="sxs-lookup"><span data-stu-id="b1376-p106">**Improved report performance**. This includes faster response and data retrieval time, as well as faster and easier navigation through the reports.</span></span>

<span data-ttu-id="b1376-119">Weitere Informationen erhalten Sie in der Dokumentation zu den Überwachungsberichten.</span><span class="sxs-lookup"><span data-stu-id="b1376-119">More information on the individual reports can be found in the Monitoring Reports documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="b1376-120">Ein weiterer neuer Bericht – QoE-Anruf Detail-Unterbericht – ist in lync Server 2013 enthalten.</span><span class="sxs-lookup"><span data-stu-id="b1376-120">There is another new report – QoE Call Detail Subreport – included in Lync Server 2013.</span></span> <span data-ttu-id="b1376-121">Dieser Bericht dient jedoch in erster Linie internen Zwecken und soll nicht direkt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="b1376-121">However, this report is primarily for internal use, and is not intended to be directly accessed.</span></span>



</div>

<span data-ttu-id="b1376-122">Es gibt zwei Möglichkeiten, lync Server-Überwachungsberichte zu installieren: Sie können den lync Server-Bereitstellungs-Assistenten verwenden, oder Sie können ein Windows PowerShell-Skript verwenden, das in den lync Server 2013-Installationsdateien enthalten ist.</span><span class="sxs-lookup"><span data-stu-id="b1376-122">There are two ways to install Lync Server Monitoring Reports: you can use the Lync Server Deployment Wizard or you can use a Windows PowerShell script included with the Lync Server 2013 installation files.</span></span> <span data-ttu-id="b1376-123">Unabhängig von der Installationsmethode, für die Sie sich entscheiden, müssen Sie zunächst Folgendes sicherstellen:</span><span class="sxs-lookup"><span data-stu-id="b1376-123">Regardless of the method you use to install the reports you must first make sure that you:</span></span>

  - <span data-ttu-id="b1376-124">Sie sind dazu berechtigt, einem Benutzerkonto in der Überwachungsdatenbank eine Datenbankrolle hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="b1376-124">Have the right to add a database role to a user account in the monitoring database.</span></span>

  - <span data-ttu-id="b1376-p109">Sie haben die Rolle „Content Manager“ in SQL Server Reporting Services. Diese Rolle berechtigt Sie dazu, Berichte in SQL Server Reporting Services bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="b1376-p109">Hold the Content Manager role in SQL Server Reporting Services. This role gives you the right to deploy reports to SQL Server Reporting Services.</span></span>

<span data-ttu-id="b1376-127">Führen Sie folgende Schritte durch, um die Überwachungsberichte mithilfe des Bereitstellungs-Assistenten zu installieren:</span><span class="sxs-lookup"><span data-stu-id="b1376-127">To install the Monitoring Reports by using the Deployment Wizard, complete the following steps:</span></span>

1.  <span data-ttu-id="b1376-128">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Bereitstellungs-Assistent**.</span><span class="sxs-lookup"><span data-stu-id="b1376-128">Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Deployment Wizard**.</span></span>

2.  <span data-ttu-id="b1376-129">Klicken Sie im Bereitstellungs-Assistenten auf **Überwachungsberichte bereitstellen**, um den Assistenten für die Bereitstellung der Überwachungsberichte zu starten.</span><span class="sxs-lookup"><span data-stu-id="b1376-129">In the Deployment Wizard, click **Deploy Monitoring Reports** in order to start the Deploy Monitoring Reports wizard.</span></span>

3.  <span data-ttu-id="b1376-p110">Stellen Sie im Assistenten für die Bereitstellung der Überwachungsberichte auf der Seite **Überwachungsdatenbank angeben** sicher, dass der vollqualifizierte Domänenname des als Host für Ihren Überwachungsspeicher fungierenden Computers in der Dropdownliste **Überwachungsdatenbank** angezeigt wird. (Sollten Sie über mehrere Überwachungsspeicher verfügen, müssen Sie den entsprechenden Server in der Dropdownliste auswählen.) Stellen Sie sicher, dass die richtige SQL-Serverinstanz im Feld **SQL Server Reporting Services-Instanz (SSRS)** angezeigt wird (z. B. **atl-sql-001.litwareinc.com/archinst**) und klicken Sie anschließend auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="b1376-p110">In the Deploy Monitoring Reports wizard, on the **Specify Monitoring Database** page, make sure that the fully qualified domain name of the computer hosting your monitoring store appears in the **Monitoring database** dropdown list. (If you have multiple monitoring stores you will need to select the appropriate server from the dropdown list.) Verify that the correct SQL Server instance appears in the **SQL Server Reporting Services (SSRS) instance** box (for example, **atl-sql-001.litwareinc.com/archinst**) and then click **Next**.</span></span>

4.  <span data-ttu-id="b1376-132">Geben Sie auf der Seite **Anmeldeinformationen angeben** im Feld **Benutzername** den Domänennamen und den Benutzernamen des Kontos ein, das beim Zugriff auf die Überwachungsberichte verwendet werden soll (beispielsweise **"litwareinc \\ kenmyer**).</span><span class="sxs-lookup"><span data-stu-id="b1376-132">On the **Specify Credentials** page, in the **User name** box, type the domain name and user name of the account to be used when accessing the Monitoring Reports (for example, **litwareinc\\kenmyer**).</span></span> <span data-ttu-id="b1376-133">Wenn Sie dieses Format (Domänen \\ Benutzername) nicht verwenden, tritt ein Fehler auf.</span><span class="sxs-lookup"><span data-stu-id="b1376-133">If you do not use this format (domain\\user name) an error will occur.</span></span>
    
    <span data-ttu-id="b1376-p112">Geben Sie das Kennwort des Benutzerkontos in das Feld **Kennwort** ein und klicken Sie auf **Weiter**. Für dieses Konto sind keine speziellen Rechte erforderlich. Dem Konto werden die erforderlichen Anmelde- und Datenbankberechtigungen automatisch erteilt, wenn die Einrichtung abgeschlossen wird.</span><span class="sxs-lookup"><span data-stu-id="b1376-p112">Type the user account password in the **Password** box, and then click **Next**. Note that no special rights are required for this account. The account will automatically be granted the required logon and database permissions when setup completes.</span></span>

5.  <span data-ttu-id="b1376-p113">Geben Sie auf der Seite **Gruppe mit Lesezugriff angeben** den Namen einer Sicherheitsgruppe an, der der Lesezugriff auf die SQL Server Reporting Services im Benutzergruppenfeld gewährt wird. Wenn Sie beispielsweise einen Lesezugriff auf die Berichte für Administratoren erteilen möchten, geben Sie **RTCUniversalReadOnlyAdmins** ein. Klicken Sie auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="b1376-p113">On the **Specify Read-Only Group** page enter the name of a security group that will be granted read-only access to the SQL Server Reporting Services in the User group box. For example, to give read-only administrators access to the reports enter **RTCUniversalReadOnlyAdmins**. Click **Next**.</span></span>

6.  <span data-ttu-id="b1376-140">Klicken Sie auf der Seite **Befehle ausführen** auf **Fertigstellen**.</span><span class="sxs-lookup"><span data-stu-id="b1376-140">On the **Executing Commands** page, click **Finish**.</span></span>

<span data-ttu-id="b1376-141">Überwachungsberichte können auch über die lync Server-Verwaltungsshell installiert werden, indem Sie das Skript DeployReports.ps1 ausführen. Dieses Windows PowerShell-Skript befindet sich auf den lync Server-Installationsmedien im \\ \\ Ordner Setup ReportingSetup.</span><span class="sxs-lookup"><span data-stu-id="b1376-141">Monitoring Reports can also be installed from the Lync Server Management Shell by running the script DeployReports.ps1; this Windows PowerShell script can be found on the Lync Server installation media in the \\Setup\\ReportingSetup folder.</span></span> <span data-ttu-id="b1376-142">Wenn Sie Überwachungsberichte mit DeployReports.ps1 installieren möchten, geben Sie an der Eingabeaufforderung der Verwaltungsshell einen Befehl ähnlich der folgenden ein:</span><span class="sxs-lookup"><span data-stu-id="b1376-142">To install Monitoring Reports using DeployReports.ps1, type a command similar to the following at the Management Shell prompt:</span></span>

    C:\Program Files\Microsoft Lync Server 2013\Deployment\Setup\DeployReports.ps1 -storedUserName "litwareinc\kenmyer" -storedPassword "p@ssw0rd" -readOnlyGroupName "RTCUniversalReadOnlyAdmins" -reportServerSqlInstance "atl-sql-001.litwareinc.com" -monitoringDatabaseId "MonitoringDatabase:atl-sql-001.litwareinc.com"

<span data-ttu-id="b1376-143">Die im vorstehenden Befehl verwendeten Parameter werden in der folgenden Tabelle beschrieben:</span><span class="sxs-lookup"><span data-stu-id="b1376-143">The parameters used in the preceding command are described in the following table:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="b1376-144">Parametername</span><span class="sxs-lookup"><span data-stu-id="b1376-144">Parameter Name</span></span></th>
<th><span data-ttu-id="b1376-145">Erforderlich</span><span class="sxs-lookup"><span data-stu-id="b1376-145">Required</span></span></th>
<th><span data-ttu-id="b1376-146">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="b1376-146">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="b1376-147">storedUserName</span><span class="sxs-lookup"><span data-stu-id="b1376-147">storedUserName</span></span></p></td>
<td><p><span data-ttu-id="b1376-148">Ja</span><span class="sxs-lookup"><span data-stu-id="b1376-148">Yes</span></span></p></td>
<td><p><span data-ttu-id="b1376-149">Benutzerkonto, das für den Zugriff auf den Überwachungsspeicher verwendet wird. Zum Beispiel</span><span class="sxs-lookup"><span data-stu-id="b1376-149">User account (in the format domain\username) used to access the monitoring store; for example:</span></span></p>
<pre><code>-storedUserName &quot;litwareinc\kenmyer&quot;</code></pre>
<p><span data-ttu-id="b1376-150">Dieses Konto muss über die zuvor angegebenen Berechtigungen für SQL Server und SQL Server Reporting Services verfügen, damit das Skript nicht fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="b1376-150">This account must have the previously-specified SQL Server and SQL Server Reporting Services permissions or the script will fail.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1376-151">storedPassword</span><span class="sxs-lookup"><span data-stu-id="b1376-151">storedPassword</span></span></p></td>
<td><p><span data-ttu-id="b1376-152">Ja</span><span class="sxs-lookup"><span data-stu-id="b1376-152">Yes</span></span></p></td>
<td><p><span data-ttu-id="b1376-153">Kennwort für das Benutzerkonto, das für den Zugriff auf den Überwachungsspeicher verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="b1376-153">Password for the user account used to access the monitoring store.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1376-154">readOnlyGroupName</span><span class="sxs-lookup"><span data-stu-id="b1376-154">readOnlyGroupName</span></span></p></td>
<td><p><span data-ttu-id="b1376-155">Nein</span><span class="sxs-lookup"><span data-stu-id="b1376-155">No</span></span></p></td>
<td><p><span data-ttu-id="b1376-p115">Domäne oder lokale Sicherheitsgruppe, deren Mitglieder den Lesezugriff für die Überwachungsberichte erhalten. Beachten Sie, dass das Skript fehlschlägt, wenn die angegebene Gruppe nicht vorhanden ist. Falls Sie diese Berechtigungen später wieder entziehen möchten oder sich dafür entscheiden, anderen Benutzern oder Gruppen Zugriffsberechtigungen zu erteilen, können Sie dies mithilfe des Berichts-Managers der SQL Service Reporting Services tun.</span><span class="sxs-lookup"><span data-stu-id="b1376-p115">Domain or local security group whose members will be granted read-only access to the Monitoring Reports. Note that the script will fail if the specified group does not exist. If you later decide to revoke these permissions, or if you decide to grant other users or other groups access permissions, you can do so using the SQL Service Reporting Services Report Manager.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="b1376-159">reportSqlServerInstance</span><span class="sxs-lookup"><span data-stu-id="b1376-159">reportSqlServerInstance</span></span></p></td>
<td><p><span data-ttu-id="b1376-160">Nein</span><span class="sxs-lookup"><span data-stu-id="b1376-160">No</span></span></p></td>
<td><p><span data-ttu-id="b1376-p116">SQL Server-Instanz, die als Host für den Berichtsdienst fungiert. Die Berichtsinstanz muss unter Verwendung des vollqualifizierten Domänennamens des Berichtsservers angegeben werden. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="b1376-p116">SQL Server instance that hosts the Reporting Service. The Reporting instance must be specified using the fully qualified domain name of the Report Server; for example:</span></span></p>
<pre><code>-reportServerSqlInstance atl-sql-001.litwareinc.com</code></pre>
<p><span data-ttu-id="b1376-163">Falls dieser Parameter nicht enthalten ist, nimmt das Skript an, dass die Berichtsdienste von derselben SQL Server-Instanz gehostet werden, die auch als Host für die Überwachungsdatenbank dient.</span><span class="sxs-lookup"><span data-stu-id="b1376-163">If this parameter is not included the script will assume that the reporting services are hosted by the same SQL Server instance that hosts the monitoring database.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="b1376-164">monitoringDatabaseId</span><span class="sxs-lookup"><span data-stu-id="b1376-164">monitoringDatabaseId</span></span></p></td>
<td><p><span data-ttu-id="b1376-165">Nein</span><span class="sxs-lookup"><span data-stu-id="b1376-165">No</span></span></p></td>
<td><p><span data-ttu-id="b1376-p117">Dienstidentität für die Überwachungsdatenbank. Sie können die Identitäten für Ihre Überwachungsdatenbanken durch Ausführung des folgenden Befehls zurückgeben:</span><span class="sxs-lookup"><span data-stu-id="b1376-p117">Service Identity for the monitoring database. You can return the Identities for your monitoring databases by running this command:</span></span></p>
<pre><code>Get-CsService -MonitoringDatabase</code></pre></td>
</tr>
</tbody>
</table>


<span data-ttu-id="b1376-168">Nachdem die Überwachungsberichte installiert wurden, müssen Sie das Set-CsReportingConfiguration-Cmdlet verwenden, um die URL für den Zugriff auf diese Berichte zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="b1376-168">After the Monitoring Reports have been installed you must then use the Set-CsReportingConfiguration cmdlet to configure the URL used to access these reports.</span></span> <span data-ttu-id="b1376-169">Diese Aufgabe kann über die lync Server-Verwaltungsshell ausgeführt werden, indem Sie den folgenden Windows PowerShell-Befehl ausführen.</span><span class="sxs-lookup"><span data-stu-id="b1376-169">This task can be carried out from the Lync Server Management Shell by running the following Windows PowerShell command.</span></span> <span data-ttu-id="b1376-170">Beachten Sie, dass es zwar ratsam, aber nicht erforderlich ist, das HTTPS-Protokoll für die Konfiguration der Berichts-URL zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="b1376-170">Note that it is recommended, but not required, that you use the HTTPS protocol when configuring the reporting URL:</span></span>

    Set-CsReportingConfiguration -Identity "MonitoringDatabase:atl-sql-001.litwareinc.com" -ReportingURL "https://atl-sql-001.litwareinc.com:443/Reports_ARCHINST"

<span data-ttu-id="b1376-p119">Im vorangehenden Befehl sollte die ReportingUrl-Eigenschaft auf die von SQL Server 2008 R2 Reporting Services verwendete Berichts-Manager-URL festgelegt sein. Führen Sie zur Ermittlung der Berichts-Manager-URL folgende Schritte auf dem Computer durch, auf dem SQL Server Reporting Services installiert wurde:</span><span class="sxs-lookup"><span data-stu-id="b1376-p119">In the preceding command, the ReportingUrl property should be set to the Report Manager URL used by SQL Server 2008 R2 Reporting Services. You can determine the Report Manager URL by completing the following steps on the computer where SQL Server Reporting Services has been installed:</span></span>

1.  <span data-ttu-id="b1376-173">Klicken Sie auf „Start“, „Alle Programme“, „Microsoft SQL Server 2008 R2“, „Konfigurationstools“ und dann auf „Konfigurations-Manager für Reporting Services“.</span><span class="sxs-lookup"><span data-stu-id="b1376-173">Click Start, click All Programs, click Microsoft SQL Server 2008 R2, click Configuration Tools, and then click Reporting Services Configuration Manager.</span></span>

2.  <span data-ttu-id="b1376-p120">Vergewissern Sie sich, dass im Dialogfeld „Konfigurationsverbindung für Reporting Services“ der Name des Reporting Services-Computers im Feld „Servername“ angezeigt wird. Wählen Sie die SQL Server-Instanz in der Dropdownliste „Berichtsserverinstanz“ aus und klicken Sie dann auf „Verbinden“.</span><span class="sxs-lookup"><span data-stu-id="b1376-p120">In the Reporting Services Configuration Connection dialog box, make sure that the name of the Reporting Services computer appears in the Server Name box. Select the SQL Server instance from the Report Server Instance dropdown list and then click Connect.</span></span>

3.  <span data-ttu-id="b1376-p121">Klicken Sie unter „Konfigurations-Manager für Reporting Services“ auf „Berichts-Manager-URL“. Im Bereich „Berichts-Manager-URL“ sollten mehrere URLs angezeigt werden. Sie können jede dieser URLs als URL für die Berichtsfunktion verwenden. Es sei jedoch nochmals darauf hingewiesen, dass für die ReportingUrl das HTTPS-Protokoll empfohlen wird.</span><span class="sxs-lookup"><span data-stu-id="b1376-p121">In Reporting Services Configuration Manager, click Report Manager URL. One or more URLs should appear in the Report Manager URL pane. Any of these URLs can be used as the Reporting URL although, again, it is recommended that the ReportingUrl use the HTTPS protocol.</span></span>

<span data-ttu-id="b1376-179">Wenn Sie eine Spiegeldatenbank für Ihre Überwachungsdatenbank eingerichtet haben, müssen Sie auch die Überwachungsberichte mit der Spiegeldatenbank verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="b1376-179">If you have set up a mirror database for your monitoring database then you must also associate the Monitoring Reports with the mirror database.</span></span> <span data-ttu-id="b1376-180">Details finden Sie im Artikel [Zuordnen von Überwachungsberichten zu einer Spiegeldatenbank in lync Server 2013](lync-server-2013-associating-monitoring-reports-with-a-mirror-database.md) .</span><span class="sxs-lookup"><span data-stu-id="b1376-180">See the article [Associating Monitoring Reports with a mirror database in Lync Server 2013](lync-server-2013-associating-monitoring-reports-with-a-mirror-database.md) for details.</span></span>

<span data-ttu-id="b1376-181"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b1376-181"></div>

<span> </span>

</div>

</div>

</span></span></div>

