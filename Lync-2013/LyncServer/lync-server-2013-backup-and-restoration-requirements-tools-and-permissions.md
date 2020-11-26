---
title: 'Lync Server 2013: Sicherungs-und Wiederherstellungsanforderungen: Tools und Berechtigungen'
description: 'Lync Server 2013: Sicherungs-und Wiederherstellungsanforderungen: Tools und Berechtigungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Backup and restoration requirements: tools and permissions'
ms:assetid: 35ec2e33-f33e-4f84-9e64-6550fd78aa52
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202171(v=OCS.15)
ms:contentKeyID: 51541465
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 36327d1214854586b44024f126bbd87acad6c4b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437980"
---
# <a name="backup-and-restoration-requirements-in-lync-server-2013-tools-and-permissions"></a><span data-ttu-id="03934-103">Sicherungs-und Wiederherstellungsanforderungen in lync Server 2013: Tools und Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="03934-103">Backup and restoration requirements in Lync Server 2013: tools and permissions</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="03934-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="03934-104">

<span> </span></span></span>

<span data-ttu-id="03934-105">_**Letztes Änderungsdatum des Themas:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="03934-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="03934-106">In diesem Thema werden die Tools aufgeführt, die Sie zum Sichern und Wiederherstellen von lync Server 2013, den erforderlichen Berechtigungen und zum Remote-oder lokalen Ausführen von Befehlen verwenden können.</span><span class="sxs-lookup"><span data-stu-id="03934-106">This topic identifies the tools that you can use to back up and restore Lync Server 2013, the permissions that you need, and whether you can run commands remotely or locally.</span></span> <span data-ttu-id="03934-107">Insbesondere konzentriert sich dieses Thema auf Tools, die mit lync Server für Sicherung und Wiederherstellung bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="03934-107">Specifically, this topic focuses on tools that are provided with Lync Server for backup and restoration.</span></span>

<div>

## <a name="backups"></a><span data-ttu-id="03934-108">Sicherungen</span><span class="sxs-lookup"><span data-stu-id="03934-108">Backups</span></span>

<span data-ttu-id="03934-109">Zum Sichern von lync Server verwenden Sie die in der folgenden Tabelle angegebenen Tools.</span><span class="sxs-lookup"><span data-stu-id="03934-109">To back up Lync Server, use the tools identified in the following table.</span></span> <span data-ttu-id="03934-110">Alle Befehle, die Sie zum Sichern von lync Server benötigen, können skriptiert werden und können Remote ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="03934-110">All the commands that you need to back up Lync Server can be scripted and can be run remotely.</span></span>

### <a name="tools-for-backing-up-lync-server"></a><span data-ttu-id="03934-111">Tools zum Sichern von lync Server</span><span class="sxs-lookup"><span data-stu-id="03934-111">Tools for Backing Up Lync Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03934-112">So sichern Sie Folgendes:</span><span class="sxs-lookup"><span data-stu-id="03934-112">To back up this:</span></span></th>
<th><span data-ttu-id="03934-113">Verwenden Sie dieses Tool oder Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="03934-113">Use this tool or cmdlet:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03934-114">Topologie-Konfigurationsdaten (XDS. mdf)</span><span class="sxs-lookup"><span data-stu-id="03934-114">Topology configuration data (Xds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="03934-115">Export-CsConfiguration</span><span class="sxs-lookup"><span data-stu-id="03934-115">Export-CsConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03934-116">Standortinformationsdienst (E9-1-1)-Daten (LIS. mdf)</span><span class="sxs-lookup"><span data-stu-id="03934-116">Location information service (E9-1-1) data (Lis.mdf)</span></span></p></td>
<td><p><span data-ttu-id="03934-117">Export-CsLisConfiguration</span><span class="sxs-lookup"><span data-stu-id="03934-117">Export-CsLisConfiguration</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03934-118">Konfigurationsdaten der Reaktionsgruppe (RgsConfig. mdf)</span><span class="sxs-lookup"><span data-stu-id="03934-118">Response Group configuration data (RgsConfig.mdf)</span></span></p></td>
<td><p><span data-ttu-id="03934-119">Export-CsRgsConfiguration</span><span class="sxs-lookup"><span data-stu-id="03934-119">Export-CsRgsConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03934-120">Beständige Benutzerdaten (Rtcxds. mdf-Datenbank)</span><span class="sxs-lookup"><span data-stu-id="03934-120">Persistent user data (Rtcxds.mdf database)</span></span></p>
<p><span data-ttu-id="03934-121">Konferenz-IDs</span><span class="sxs-lookup"><span data-stu-id="03934-121">Conference IDs</span></span></p></td>
<td><p><span data-ttu-id="03934-122">Export-CsUserData</span><span class="sxs-lookup"><span data-stu-id="03934-122">Export-CsUserData</span></span></p></td>
</tr>
<tr class="odd">
<td><ul>
<li><p><span data-ttu-id="03934-123">Archivierungsdatenbank (LcsLog. mdf)</span><span class="sxs-lookup"><span data-stu-id="03934-123">Archiving database (LcsLog.mdf)</span></span></p></li>
<li><p><span data-ttu-id="03934-124">Überwachungsdatenbank für Anruf Detaildatensätze (LcsCDR. mdf)</span><span class="sxs-lookup"><span data-stu-id="03934-124">Monitoring call detail record database (LcsCDR.mdf)</span></span></p></li>
<li><p><span data-ttu-id="03934-125">Überwachen der QoE-Datenbank (Datenbank QoEMetrics werden. mdf)</span><span class="sxs-lookup"><span data-stu-id="03934-125">Monitoring QoE database (QoEMetrics.mdf)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="03934-126">SQL Server-Datenbanktool wie SQL Server Management Studio</span><span class="sxs-lookup"><span data-stu-id="03934-126">SQL Server database tool, such as SQL Server Management Studio</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03934-127">Datenbank für beständigen Chat (MGC. mdf)</span><span class="sxs-lookup"><span data-stu-id="03934-127">Persistent Chat database (Mgc.mdf)</span></span></p></td>
<td><p><span data-ttu-id="03934-128">SQL Server-Sicherungsverfahren oder Export-CsPersistentChatData.</span><span class="sxs-lookup"><span data-stu-id="03934-128">SQL Server backup procedures or Export-CsPersistentChatData.</span></span> <span data-ttu-id="03934-129">Export-CsPersistentChatData exportiert persistente Chat-Daten als Datei.</span><span class="sxs-lookup"><span data-stu-id="03934-129">Export-CsPersistentChatData exports Persistent Chat data as a file.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03934-130">Alle Dateispeicher: lync Server-Dateispeicher, Archivierungsdatei Speicher</span><span class="sxs-lookup"><span data-stu-id="03934-130">All file stores: Lync Server file store, Archiving file store</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="03934-131">Dateien mit dem Namen " <STRONG>Meeting. Active</STRONG> " sollten nicht gesichert werden.</span><span class="sxs-lookup"><span data-stu-id="03934-131">Files named <STRONG>Meeting.Active</STRONG> should not be backed up.</span></span> <span data-ttu-id="03934-132">Diese Dateien werden während einer Besprechung verwendet und gesperrt.</span><span class="sxs-lookup"><span data-stu-id="03934-132">These files are in use and locked while a meeting takes place.</span></span>


</div></td>
<td><p><span data-ttu-id="03934-133">Standard mäßiges Dateisystem-Verwaltungstool, beispielsweise Robocopy.</span><span class="sxs-lookup"><span data-stu-id="03934-133">Standard file system management tool, such as Robocopy.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="restoration"></a><span data-ttu-id="03934-134">Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="03934-134">Restoration</span></span>

<span data-ttu-id="03934-135">Verwenden Sie zum Wiederherstellen von lync Server die Tools in der folgenden Tabelle.</span><span class="sxs-lookup"><span data-stu-id="03934-135">To restore Lync Server, use the tools in the following table.</span></span> <span data-ttu-id="03934-136">Für alle Befehle, die Sie zum Wiederherstellen von lync Server benötigen, kann ein Skript erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="03934-136">All the commands that you need to restore Lync Server can be scripted.</span></span> <span data-ttu-id="03934-137">Einige können Remote ausgeführt werden, andere müssen jedoch lokal ausgeführt werden, wie in der folgenden Tabelle angegeben.</span><span class="sxs-lookup"><span data-stu-id="03934-137">Some can be run remotely, but others need to be run locally, as specified in the following table.</span></span>

### <a name="tools-for-restoring-lync-server"></a><span data-ttu-id="03934-138">Tools zum Wiederherstellen von lync Server</span><span class="sxs-lookup"><span data-stu-id="03934-138">Tools for Restoring Lync Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="03934-139">Gehen Sie dazu so vor:</span><span class="sxs-lookup"><span data-stu-id="03934-139">To do this:</span></span></th>
<th><span data-ttu-id="03934-140">Verwenden Sie dieses Tool oder Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="03934-140">Use this tool or cmdlet:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="03934-141">Erstellen eines neuen oder sauberen Computers</span><span class="sxs-lookup"><span data-stu-id="03934-141">Build a new or clean computer</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="03934-142">Installationssoftware für Windows-Betriebssysteme</span><span class="sxs-lookup"><span data-stu-id="03934-142">Windows operating system installation software</span></span></p></li>
<li><p><span data-ttu-id="03934-143">SQL Server-Installationssoftware</span><span class="sxs-lookup"><span data-stu-id="03934-143">SQL Server installation software</span></span></p></li>
<li><p><span data-ttu-id="03934-144">Zertifikate Microsoft Management Console (MMC)-Snap-in, wenn Zertifikate mit einem exportierbaren privaten Schlüssel wiederhergestellt werden</span><span class="sxs-lookup"><span data-stu-id="03934-144">Certificates Microsoft Management Console (MMC) snap-in, if restoring certificates with an exportable private key</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03934-145">Wiederherstellen von dateispeicherdaten</span><span class="sxs-lookup"><span data-stu-id="03934-145">Restore file store data</span></span></p></td>
<td><p><span data-ttu-id="03934-146">Standard mäßiges Dateisystem-Verwaltungstool wie Robocopy</span><span class="sxs-lookup"><span data-stu-id="03934-146">Standard file system management tool, such as Robocopy</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03934-147">Erstellen Sie leere Datenbanken neu, und legen Sie Berechtigungen für Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="03934-147">Recreate empty databases and set permissions for the following:</span></span></p>
<ul>
<li><p><span data-ttu-id="03934-148">zentraler Verwaltungsspeicher</span><span class="sxs-lookup"><span data-stu-id="03934-148">Central Management store</span></span></p></li>
<li><p><span data-ttu-id="03934-149">Back-End-Server</span><span class="sxs-lookup"><span data-stu-id="03934-149">Back End Server</span></span></p></li>
<li><p><span data-ttu-id="03934-150">Überwachungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="03934-150">Monitoring database</span></span></p></li>
<li><p><span data-ttu-id="03934-151">Archivierungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="03934-151">Archiving database</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="03934-152">Install-CsDatabase</span><span class="sxs-lookup"><span data-stu-id="03934-152">Install-CsDatabase</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03934-153">Wiederherstellen des Zeigers der Active Directory-Domänendienste auf den zentralen Verwaltungsspeicher</span><span class="sxs-lookup"><span data-stu-id="03934-153">Restore the Active Directory Domain Services pointer to the Central Management store</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="03934-154">Wenn Sie den Dienstverbindungspunkt zu einem beliebigen Zeitpunkt verloren haben, können Sie dieses Cmdlet erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="03934-154">If you lose the service connection point at any time, you can rerun this cmdlet.</span></span>


</div></td>
<td><p><span data-ttu-id="03934-155">Set-CsConfigurationStoreLocation</span><span class="sxs-lookup"><span data-stu-id="03934-155">Set-CsConfigurationStoreLocation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03934-156">Importieren der Topologie, Richtlinien und Konfigurationseinstellungen in den zentralen Verwaltungsspeicher (XDS. mdf)</span><span class="sxs-lookup"><span data-stu-id="03934-156">Import the topology, policies, and configuration settings to the Central Management store (Xds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="03934-157">Import-CsConfiguration</span><span class="sxs-lookup"><span data-stu-id="03934-157">Import-CsConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03934-158">Veröffentlichen und Aktivieren der Topologie</span><span class="sxs-lookup"><span data-stu-id="03934-158">Publish and enable the topology</span></span></p></td>
<td><p><span data-ttu-id="03934-159">Topologie-Generator</span><span class="sxs-lookup"><span data-stu-id="03934-159">Topology Builder</span></span></p>
<p><span data-ttu-id="03934-160">oder</span><span class="sxs-lookup"><span data-stu-id="03934-160">-or-</span></span></p>
<p><span data-ttu-id="03934-161">Publish-CsTopology und Enable-CsTopology</span><span class="sxs-lookup"><span data-stu-id="03934-161">Publish-CsTopology and Enable-CsTopology</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03934-162">Aktivieren der letzten veröffentlichten Topologie</span><span class="sxs-lookup"><span data-stu-id="03934-162">Enable the last published topology</span></span></p></td>
<td><p><span data-ttu-id="03934-163">Enable-CsTopology</span><span class="sxs-lookup"><span data-stu-id="03934-163">Enable-CsTopology</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03934-164">Erneutes Installieren von lync Server-Komponenten</span><span class="sxs-lookup"><span data-stu-id="03934-164">Reinstall Lync Server components</span></span></p></td>
<td><p><span data-ttu-id="03934-165">Lync Server-Setup</span><span class="sxs-lookup"><span data-stu-id="03934-165">Lync Server Setup</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="03934-166">Befindet sich im lync Server-Installationsordner oder auf den Medien unter \setup\amd64\Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="03934-166">Located in the Lync Server installation folder or media at \setup\amd64\Setup.exe.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03934-167">Wiederherstellen von Standortinformationen (E9-1-1)-Daten (LIS. mdf)</span><span class="sxs-lookup"><span data-stu-id="03934-167">Restore location information (E9-1-1) data (Lis.mdf)</span></span></p></td>
<td><p><span data-ttu-id="03934-168">Import-CsLisConfiguration</span><span class="sxs-lookup"><span data-stu-id="03934-168">Import-CsLisConfiguration</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03934-169">Wiederherstellen beständiger Benutzerdaten (Rtcxds. mdf)</span><span class="sxs-lookup"><span data-stu-id="03934-169">Restore persistent user data (Rtcxds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="03934-170">Import-CsUserData</span><span class="sxs-lookup"><span data-stu-id="03934-170">Import-CsUserData</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03934-171">Wiederherstellen der Konfigurationsdaten der Reaktionsgruppe (RgsConfig. mdf)</span><span class="sxs-lookup"><span data-stu-id="03934-171">Restore Response Group configuration data (RgsConfig.mdf)</span></span></p></td>
<td><p><span data-ttu-id="03934-172">Import-CsRgsConfiguration</span><span class="sxs-lookup"><span data-stu-id="03934-172">Import-CsRgsConfiguration</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="03934-173">Wenn die Konfiguration in einem neu bereitgestellten Pool wiederhergestellt wird, in dem keine Antwortgruppen Daten in der Datenbank enthalten sind, sollten Sie die Option – OverwriteOwner verwenden.</span><span class="sxs-lookup"><span data-stu-id="03934-173">If the configuration is being restored in a newly deployed pool that has no Response Group data in the database, then you should use the –OverwriteOwner option.</span></span> <span data-ttu-id="03934-174">Verwenden Sie diese Option, selbst wenn sich die wiederhergestellten Daten in einem Pool mit dem gleichen vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) befinden.</span><span class="sxs-lookup"><span data-stu-id="03934-174">Use this option even if the data being restored is in a pool with the same fully qualified domain name (FQDN).</span></span> <span data-ttu-id="03934-175">Andernfalls ist der Import aufgrund der Kontaktobjekte zu den bereits in Active Directory vorhandenen Antwortgruppen nicht erfolgreich.</span><span class="sxs-lookup"><span data-stu-id="03934-175">Otherwise, the import will not succeed, due to the contact objects to the Response Groups already existing in Active Directory.</span></span>


</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="03934-176">Stellen Sie die folgenden Datenbanken wieder her:</span><span class="sxs-lookup"><span data-stu-id="03934-176">Restore the following databases:</span></span></p>
<ul>
<li><p><span data-ttu-id="03934-177">Archivierungsdatenbank (LcsLog. mdf)</span><span class="sxs-lookup"><span data-stu-id="03934-177">Archiving database (LcsLog.mdf)</span></span></p></li>
<li><p><span data-ttu-id="03934-178">Überwachungsdatenbanken: Anruf Detaildatensatz Datenbank (LcsCDR. mdf) und QoE-Datenbank (Datenbank QoEMetrics werden. mdf)</span><span class="sxs-lookup"><span data-stu-id="03934-178">Monitoring databases: call detail record database (LcsCDR.mdf) and QoE database (QoEMetrics.mdf)</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="03934-179">SQL Server-Datenbankverwaltungstools</span><span class="sxs-lookup"><span data-stu-id="03934-179">SQL Server database management tools</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="03934-180">Datenbank für beständigen Chat (MGS. mdf)</span><span class="sxs-lookup"><span data-stu-id="03934-180">Persistent Chat database (Mgs.mdf)</span></span></p></td>
<td><p><span data-ttu-id="03934-181">SQL Server-Wiederherstellungsverfahren oder Import-CsPersistentChatData.</span><span class="sxs-lookup"><span data-stu-id="03934-181">SQL Server restore procedures or Import-CsPersistentChatData.</span></span> <span data-ttu-id="03934-182">Sie können Import-CsPersistentChatData mit einer Datei verwenden, die von Export-CsPersistentChatData erstellt wurde, und die Daten werden in die persistente Chat Datenbank importiert.</span><span class="sxs-lookup"><span data-stu-id="03934-182">You can use Import-CsPersistentChatData with a file created by Export-CsPersistentChatData, and the data will be imported into the Persistent Chat database.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="required-permissions"></a><span data-ttu-id="03934-183">Erforderliche Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="03934-183">Required Permissions</span></span>

<span data-ttu-id="03934-184">Benutzer müssen ein Mitglied der **RTCUniversalServerAdmins** -Gruppe sein, um alle in diesem Thema beschriebenen Befehle ausführen zu können.</span><span class="sxs-lookup"><span data-stu-id="03934-184">Users must be a member of the **RTCUniversalServerAdmins** group to perform all the commands described in this topic.</span></span> <span data-ttu-id="03934-185">Die meisten Befehle für die Sicherung und Wiederherstellung unterstützen keine rollenbasierte Zugriffssteuerung.</span><span class="sxs-lookup"><span data-stu-id="03934-185">Most backup and restore commands do not support role-based access control (RBAC).</span></span> <span data-ttu-id="03934-186">Zwei Ausnahmen sind die beständigen Chat-Cmdlets Export-CsPersistentChatData und Import-CsPersistentChatData, die von einem Benutzer ausgeführt werden müssen, der ein Mitglied der CsPersistentChatAdministrator-Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="03934-186">Two exceptions are the Persistent Chat cmdlets Export-CsPersistentChatData and Import-CsPersistentChatData, which must be run by a user who is a member of the CsPersistentChatAdministrator group.</span></span> <span data-ttu-id="03934-187">Damit Sie den lync Server-Bereitstellungs-Assistenten ausführen können, muss ein Benutzer auch ein Mitglied der lokalen Administratoren-Gruppe sein.</span><span class="sxs-lookup"><span data-stu-id="03934-187">To run Lync Server Deployment Wizard, a user must also be a member of the Local Adminstrators group.</span></span>

<span data-ttu-id="03934-188"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="03934-188"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

