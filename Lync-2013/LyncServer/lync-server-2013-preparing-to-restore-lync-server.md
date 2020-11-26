---
title: 'Lync Server 2013: Vorbereiten der Wiederherstellung von lync Server'
description: 'Lync Server 2013: Vorbereiten der Wiederherstellung von lync Server'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing to restore Lync Server
ms:assetid: 857e4e02-908e-433a-96c6-be1795a9cb61
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202179(v=OCS.15)
ms:contentKeyID: 51541490
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1875a691cfb70a6a824ab19bfde3dee4d699e48a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424093"
---
# <a name="preparing-to-restore-lync-server-2013"></a><span data-ttu-id="8481b-103">Vorbereiten der Wiederherstellung von lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8481b-103">Preparing to restore Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8481b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8481b-104">

<span> </span></span></span>

<span data-ttu-id="8481b-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="8481b-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="8481b-106">Bevor Sie mit dem Wiederherstellen von Servern und Datenbankennach einem Fehler beginnen, müssen Sie Folgendes ermitteln:</span><span class="sxs-lookup"><span data-stu-id="8481b-106">Before you begin restoring servers and databases after a failure, you need to determine the following:</span></span>

  - <span data-ttu-id="8481b-107">Was muss wiederhergestellt werden?</span><span class="sxs-lookup"><span data-stu-id="8481b-107">What needs to be restored.</span></span>

  - <span data-ttu-id="8481b-108">Die Hardware, Software, Daten und Tools, die Sie für die Wiederherstellung benötigen.</span><span class="sxs-lookup"><span data-stu-id="8481b-108">The hardware, software, data, and tools you need for restoration.</span></span>

<div>

## <a name="determining-what-to-restore"></a><span data-ttu-id="8481b-109">Bestimmen, was wiederhergestellt werden soll</span><span class="sxs-lookup"><span data-stu-id="8481b-109">Determining What to Restore</span></span>

<span data-ttu-id="8481b-110">In diesem Thema wird beschrieben, wie lync Server-Ausfälle wiederhergestellt werden, die auf der Ebene des Servers, Pools oder zentralen Verwaltungsspeichers auftreten.</span><span class="sxs-lookup"><span data-stu-id="8481b-110">This topic describes how to restore Lync Server outages that occur at the server, pool, or Central Management store level.</span></span> <span data-ttu-id="8481b-111">Wenn der zentrale Verwaltungsspeicher fehlschlägt, funktioniert Ihre lync Server-Bereitstellung weiterhin, aber Sie können keine Konfigurationsänderungen vornehmen.</span><span class="sxs-lookup"><span data-stu-id="8481b-111">If the Central Management store fails, your Lync Server deployment continues to function, but you cannot make any configuration changes.</span></span> <span data-ttu-id="8481b-112">Wenn ein Back-End-Server oder Standard Edition-Server ausfällt, funktioniert der Benutzerpool nicht mehr.</span><span class="sxs-lookup"><span data-stu-id="8481b-112">If a Back End Server or Standard Edition server fails, the user pool stops functioning.</span></span> <span data-ttu-id="8481b-113">Wenn ein anderer Server ausfällt, hängt die Größe des Fehlers von der Serverrolle ab, die der Server ausführt, und davon, ob der Server mindestens eine Datenbank hostet.</span><span class="sxs-lookup"><span data-stu-id="8481b-113">If any other server fails, the magnitude of the failure depends on the server role the server is running and whether the server hosts one or more databases.</span></span>

### <a name="what-to-restore"></a><span data-ttu-id="8481b-114">Was wiederhergestellt werden soll</span><span class="sxs-lookup"><span data-stu-id="8481b-114">What to Restore</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8481b-115">Wenn dies nicht möglich ist</span><span class="sxs-lookup"><span data-stu-id="8481b-115">If this failed</span></span></th>
<th><span data-ttu-id="8481b-116">Lesen Sie diesen Abschnitt:</span><span class="sxs-lookup"><span data-stu-id="8481b-116">See this section:</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8481b-117">Standard Edition-Server</span><span class="sxs-lookup"><span data-stu-id="8481b-117">Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="8481b-118"><a href="lync-server-2013-restoring-a-standard-edition-server.md">Wiederherstellen eines Standard Edition-Servers in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8481b-118"><a href="lync-server-2013-restoring-a-standard-edition-server.md">Restoring a Standard Edition server in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8481b-119">zentraler Verwaltungsspeicher</span><span class="sxs-lookup"><span data-stu-id="8481b-119">Central Management store</span></span></p></td>
<td><p><span data-ttu-id="8481b-120"><a href="lync-server-2013-restoring-the-server-hosting-the-central-management-store.md">Wiederherstellen des Servers, auf dem der zentrale Verwaltungsspeicher in lync Server 2013 gehostet wird</a></span><span class="sxs-lookup"><span data-stu-id="8481b-120"><a href="lync-server-2013-restoring-the-server-hosting-the-central-management-store.md">Restoring the server hosting the Central Management store in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8481b-121">Enterprise Edition-Back-End</span><span class="sxs-lookup"><span data-stu-id="8481b-121">Enterprise Edition Back End</span></span></p></td>
<td><p><span data-ttu-id="8481b-122"><a href="lync-server-2013-restoring-an-enterprise-edition-back-end-server.md">Wiederherstellen eines Enterprise Edition-Back-End-Servers in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8481b-122"><a href="lync-server-2013-restoring-an-enterprise-edition-back-end-server.md">Restoring an Enterprise Edition Back End Server in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8481b-123">Enterprise Edition, gespiegelt, primärer Back-End-Server</span><span class="sxs-lookup"><span data-stu-id="8481b-123">Enterprise Edition Mirrored Back End Primary Server</span></span></p></td>
<td><p><span data-ttu-id="8481b-124"><a href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-primary.md">Wiederherstellen eines gespiegelten Enterprise Edition-Back-End-Servers in lync Server 2013 – primär</a></span><span class="sxs-lookup"><span data-stu-id="8481b-124"><a href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-primary.md">Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - primary</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8481b-125">Enterprise Edition, gespiegelt, sekundärer Back-End-Server</span><span class="sxs-lookup"><span data-stu-id="8481b-125">Enterprise Edition Mirrored Back End Secondary Server</span></span></p></td>
<td><p><span data-ttu-id="8481b-126"><a href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-mirror.md">Wiederherstellen eines gespiegelten Enterprise Edition-Back-End-Servers in lync Server 2013 – Spiegelung</a></span><span class="sxs-lookup"><span data-stu-id="8481b-126"><a href="lync-server-2013-restoring-a-mirrored-enterprise-edition-back-end-server-mirror.md">Restoring a mirrored Enterprise Edition Back End Server in Lync Server 2013 - mirror</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8481b-127">Jeder Enterprise Edition-Server, auf dem eine Serverrolle ausgeführt wird, beispielsweise ein Front-End-Server, ein Edgeserver, Director, Mediation Server oder beständiger Chat Server.</span><span class="sxs-lookup"><span data-stu-id="8481b-127">Any Enterprise Edition server running a server role, such as a Front End Server, Edge Server, Director, Mediation Server,.or Persistent Chat Server.</span></span></p></td>
<td><p><span data-ttu-id="8481b-128"><a href="lync-server-2013-restoring-an-enterprise-edition-member-server.md">Wiederherstellen eines Enterprise Edition-Mitgliedsservers in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8481b-128"><a href="lync-server-2013-restoring-an-enterprise-edition-member-server.md">Restoring an Enterprise Edition member server in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8481b-129">Ein ganzer lync Server-Pool</span><span class="sxs-lookup"><span data-stu-id="8481b-129">An entire Lync Server pool</span></span></p></td>
<td><p><span data-ttu-id="8481b-130"><a href="lync-server-2013-restoring-a-lync-server-pool.md">Wiederherstellen eines lync Server-Pools in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8481b-130"><a href="lync-server-2013-restoring-a-lync-server-pool.md">Restoring a Lync Server pool in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8481b-131">Enterprise Edition-Dateispeicher</span><span class="sxs-lookup"><span data-stu-id="8481b-131">Enterprise Edition File Store</span></span></p></td>
<td><p><span data-ttu-id="8481b-132"><a href="lync-server-2013-restoring-a-file-store.md">Wiederherstellen eines Dateispeichers in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8481b-132"><a href="lync-server-2013-restoring-a-file-store.md">Restoring a file store in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8481b-133">Eine eigenständige Überwachungsdatenbank oder eine Archivierungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="8481b-133">A standalone Monitoring database or Archiving database</span></span></p></td>
<td><p><span data-ttu-id="8481b-134"><a href="lync-server-2013-restoring-monitoring-or-archiving-data.md">Wiederherstellen von Überwachungs-oder Archivierungsdaten in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8481b-134"><a href="lync-server-2013-restoring-monitoring-or-archiving-data.md">Restoring monitoring or archiving data in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8481b-135">Eine eigenständige Datenbank für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="8481b-135">A stand-alone Persistent Chat database</span></span></p></td>
<td><p><span data-ttu-id="8481b-136"><a href="lync-server-2013-restoring-persistent-chat-data.md">Wiederherstellen beständiger Chat-Daten in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="8481b-136"><a href="lync-server-2013-restoring-persistent-chat-data.md">Restoring Persistent Chat data in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="gathering-hardware-software-and-tools"></a><span data-ttu-id="8481b-137">Sammeln von Hardware, Software und Tools</span><span class="sxs-lookup"><span data-stu-id="8481b-137">Gathering Hardware, Software, and Tools</span></span>

<span data-ttu-id="8481b-138">Wenn Sie einen Server wiederherstellen, müssen Sie mit einem neuen oder sauberen Computer beginnen.</span><span class="sxs-lookup"><span data-stu-id="8481b-138">When you restore a server, you need to start with a new or clean computer.</span></span> <span data-ttu-id="8481b-139">Darüber hinaus müssen Sie die folgende Hardware und Software zur Verfügung haben:</span><span class="sxs-lookup"><span data-stu-id="8481b-139">Additionally, you must have the following hardware and software available:</span></span>

  - <span data-ttu-id="8481b-140">Ein sauberer oder neuer Server mit dem gleichen vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) wie der fehlerhafte Server.</span><span class="sxs-lookup"><span data-stu-id="8481b-140">A clean or new server with the same fully qualified domain name (FQDN) as the server that failed.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="8481b-141">Wenn Sie das Betriebssystem installieren, stellen Sie sicher, dass Sie das Computerkonto nicht in den Active Directory-Domänendiensten löschen, und überprüfen Sie, ob die Gruppen Berechtigungen für das Konto beibehalten werden.</span><span class="sxs-lookup"><span data-stu-id="8481b-141">When you install the operating system, make sure that you do not delete the computer account in Active Directory Domain Services, and verify that the group permissions for the account are retained.</span></span>

    
    </div>

  - <span data-ttu-id="8481b-142">Installationssoftware für das Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="8481b-142">Installation software for the operating system.</span></span> <span data-ttu-id="8481b-143">Verwenden Sie zum Installieren des Betriebssystems die Server Bereitstellungsverfahren und-Konfigurationen, die von Ihrer Organisation eingerichtet wurden.</span><span class="sxs-lookup"><span data-stu-id="8481b-143">To install the operating system, use the server deployment procedures and configurations established by your organization.</span></span> <span data-ttu-id="8481b-144">Wenn Sie den Dienst wiederherstellen, sollten diese Verfahren und Konfigurationsanforderungen zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="8481b-144">You should have these procedures and configuration requirements available when you restore service.</span></span>

  - <span data-ttu-id="8481b-145">Installationssoftware für SQL Server 2012 oder SQL Server 2008 R2</span><span class="sxs-lookup"><span data-stu-id="8481b-145">Installation software for SQL Server 2012 or SQL Server 2008 R2.</span></span> <span data-ttu-id="8481b-146">Wenn Sie einen Datenbankserver installieren möchten, verwenden Sie die entsprechende Version von SQL Server und die von Ihrer Organisation eingerichteten Datenbankserver Bereitstellungsverfahren und-Konfigurationen.</span><span class="sxs-lookup"><span data-stu-id="8481b-146">To install a database server, use the appropriate version of SQL Server and the database server deployment procedures and configurations established by your organization.</span></span> <span data-ttu-id="8481b-147">Wenn Sie den Dienst wiederherstellen, sollten diese Verfahren und Konfigurationsanforderungen zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="8481b-147">You should have these procedures and configuration requirements available when you restore service.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="8481b-148">Der lync Server-Bereitstellungs-Assistent installiert SQL Server 2012 Express auf jedem Standard Edition-Server und auf jedem anderen lync Server-Server automatisch, wenn ein lokaler Konfigurationsspeicher installiert ist, es sei denn, Sie haben SQL Server 2012 oder SQL Server 2008 R2 auf dem Server vorinstalliert.</span><span class="sxs-lookup"><span data-stu-id="8481b-148">The Lync Server Deployment Wizard automatically installs SQL Server 2012 Express on each Standard Edition server and on any other Lync Server server when a local configuration store is installed, unless you have preinstalled SQL Server 2012 or SQL Server 2008 R2 on the server.</span></span>

    
    </div>

  - <span data-ttu-id="8481b-149">Software zum Aufnehmen von System Bildern.</span><span class="sxs-lookup"><span data-stu-id="8481b-149">Software for taking system images.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="8481b-150">Wir empfehlen, dass Sie nach der Installation des Betriebssystems und SQL Server und vor dem Starten der Wiederherstellung eine Image-Kopie des Systems erstellen, damit Sie dieses Bild als Rollback-Point verwenden können, falls während der Wiederherstellung etwas schief geht.</span><span class="sxs-lookup"><span data-stu-id="8481b-150">We recommend that you take an image copy of the system after you install the operating system and SQL Server, and before you start restoration, so that you can use this image as a rollback point in case something goes wrong during restoration.</span></span>

    
    </div>

  - <span data-ttu-id="8481b-151">Lync Server 2013-Installationssoftware.</span><span class="sxs-lookup"><span data-stu-id="8481b-151">Lync Server 2013 installation software.</span></span> <span data-ttu-id="8481b-152">Der lync Server-Bereitstellungs-Assistent befindet sich im lync Server-Installationsordner oder auf den Medien unter \\ Setup \\ amd64 \\Setup.exe.</span><span class="sxs-lookup"><span data-stu-id="8481b-152">The Lync Server Deployment Wizard is located in the Lync Server installation folder or media at \\setup\\amd64\\Setup.exe.</span></span>

<span data-ttu-id="8481b-153">Während der Wiederherstellung verwenden Sie die folgenden Tools:</span><span class="sxs-lookup"><span data-stu-id="8481b-153">During restoration, you use the following tools:</span></span>

  - <span data-ttu-id="8481b-154">Cmdlets der lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="8481b-154">Lync Server Management Shell cmdlets</span></span>

  - <span data-ttu-id="8481b-155">Import-CsUserData</span><span class="sxs-lookup"><span data-stu-id="8481b-155">Import-CsUserData</span></span>

  - <span data-ttu-id="8481b-156">Tools zum Wiederherstellen von Windows-Ordnern</span><span class="sxs-lookup"><span data-stu-id="8481b-156">Tools for restoring Windows folders</span></span>

  - <span data-ttu-id="8481b-157">Topologie-Generator</span><span class="sxs-lookup"><span data-stu-id="8481b-157">Topology Builder</span></span>

  - <span data-ttu-id="8481b-158">SQL Server-Datenbankdienstprogramme wie SQL Server Management Studio</span><span class="sxs-lookup"><span data-stu-id="8481b-158">SQL Server database utilities, such as SQL Server Management Studio</span></span>

</div>

<div>

## <a name="preparing-to-restore-a-server"></a><span data-ttu-id="8481b-159">Vorbereiten der Wiederherstellung eines Servers</span><span class="sxs-lookup"><span data-stu-id="8481b-159">Preparing to Restore a Server</span></span>

<span data-ttu-id="8481b-160">Bevor Sie den Server wiederherstellen, müssen Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="8481b-160">Before you restore the server, you must perform the following steps:</span></span>

1.  <span data-ttu-id="8481b-161">Installieren Sie das Betriebssystem.</span><span class="sxs-lookup"><span data-stu-id="8481b-161">Install the operating system.</span></span>

2.  <span data-ttu-id="8481b-162">Wenn es sich bei dem Server um einen Back-End-Server handelt, installieren Sie SQL Server 2012 oder SQL Server 2008 R2.</span><span class="sxs-lookup"><span data-stu-id="8481b-162">If the server is a Back End Server, install SQL Server 2012 or SQL Server 2008 R2.</span></span>

3.  <span data-ttu-id="8481b-163">Wiederherstellen oder Erneutes Registrieren Ihrer Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="8481b-163">Restore or reenroll your certificates.</span></span> <span data-ttu-id="8481b-164">Ausführliche Informationen zu Zertifikaten finden Sie unter "zusätzliche Sicherungsanforderungen" in den [Sicherungs-und Wiederherstellungsanforderungen in lync Server 2013: Data](lync-server-2013-backup-and-restoration-requirements-data.md).</span><span class="sxs-lookup"><span data-stu-id="8481b-164">For details about certificates, see "Additional Backup Requirements" in [Backup and restoration requirements in Lync Server 2013: data](lync-server-2013-backup-and-restoration-requirements-data.md).</span></span>

4.  <span data-ttu-id="8481b-165">Erstellen Sie ein Abbild des Systems, bevor Sie die Wiederherstellung starten, um es als Rollback-Punkt zu verwenden, falls während der Wiederherstellung etwas schief geht.</span><span class="sxs-lookup"><span data-stu-id="8481b-165">Take an image of the system before starting restoration to use as a rollback point, in case something goes wrong during restoration.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8481b-166">Den lync Server-Bereitstellungs-Assistenten und Cmdlets, die in den Vorgehensweisen in diesem Thema beschrieben sind, und Verwandte Themen, legen Sie alle erforderlichen Zugriffssteuerungslisten (ACLs) an.</span><span class="sxs-lookup"><span data-stu-id="8481b-166">The Lync Server Deployment Wizard and cmdlets described in the procedures in this topic, and related topics, set all required access control lists (ACLs).</span></span>



</div>

<span data-ttu-id="8481b-167">Überprüfen Sie, ob die Hardware und die Software, die Sie für die Komponenten benötigen, die Sie wiederherstellen möchten, verfügbar sind, bevor Sie die Wiederherstellung starten.</span><span class="sxs-lookup"><span data-stu-id="8481b-167">Verify that the hardware and the software that you need for the components that you plan to restore are available before you start restoration.</span></span> <span data-ttu-id="8481b-168">Nachdem Sie das Betriebssystem und SQL Server installiert haben, können die meisten Schritte in den folgenden Wiederherstellungsverfahren Remote ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8481b-168">After you install the operating system and SQL Server, most of the steps in the following restoration procedures can be run remotely.</span></span> <span data-ttu-id="8481b-169">Die Ausnahmen sind in den Verfahren angegeben.</span><span class="sxs-lookup"><span data-stu-id="8481b-169">The exceptions are noted in the procedures.</span></span>

<span data-ttu-id="8481b-170">Darüber hinaus sollten Sie den Sicherungs-und Wiederherstellungsplan Ihrer Organisation und die Informationen aus ihrer letzten Sicherung, wie etwa die Informationen in den Arbeitsblättern in diesem Dokument (Details finden Sie unter [Sicherungs-und Wiederherstellungs Arbeitsblätter für lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md)), verfügbar sein, bevor Sie mit der Wiederherstellung beginnen.</span><span class="sxs-lookup"><span data-stu-id="8481b-170">You should also have your organization's backup and restoration plan and the information from your last backup, such as the information in the worksheets in this document (for details, see [Backup and restoration worksheets for Lync Server 2013](lync-server-2013-backup-and-restoration-worksheets.md)), available before you begin restoration.</span></span>

<span data-ttu-id="8481b-171"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8481b-171"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

