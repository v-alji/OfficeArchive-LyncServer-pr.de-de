---
title: Verschieben des zentralen Verwaltungsservers mit lync Server 2010 auf lync Server 2013
description: Verschieben Sie den lync Server 2010 Central-Verwaltungs Server zu lync Server 2013.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Move the Lync Server 2010 Central Management Server to Lync Server 2013
ms:assetid: 30cc98f2-1916-4dbe-99d0-8df5368ed3ec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688013(v=OCS.15)
ms:contentKeyID: 49733602
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 19d53d797375b1eb8fde72f6b999e509b97f85ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443293"
---
# <a name="move-the-lync-server-2010-central-management-server-to-lync-server-2013"></a><span data-ttu-id="76986-103">Verschieben des zentralen Verwaltungsservers mit lync Server 2010 auf lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="76986-103">Move the Lync Server 2010 Central Management Server to Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="76986-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="76986-104">

<span> </span></span></span>

<span data-ttu-id="76986-105">_**Letztes Änderungsdatum des Themas:** 2013-11-25_</span><span class="sxs-lookup"><span data-stu-id="76986-105">_**Topic Last Modified:** 2013-11-25_</span></span>

<span data-ttu-id="76986-106">Nachdem Sie die Migration von lync Server 2010 zu lync Server 2013 durchlaufen haben, müssen Sie den zentralen Verwaltungsserver von lync Server 2010 auf den lync Server 2013-Front-End-Server oder-Pool verschieben, bevor Sie den Legacy-lync Server 2010-Server entfernen können.</span><span class="sxs-lookup"><span data-stu-id="76986-106">After migrating from Lync Server 2010 to Lync Server 2013, you need to move the Lync Server 2010 Central Management Server to the Lync Server 2013 Front End Server or pool, before you can remove the legacy Lync Server 2010 server.</span></span>

<span data-ttu-id="76986-107">Bei dem zentralen Verwaltungsserver handelt es sich um ein einzelnes Master/Multiple-Replikat System, bei dem die Kopie der Datenbank vom Front-End-Server, auf dem sich der zentrale Verwaltungsserver befindet, gelesen/geschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="76986-107">The Central Management Server is a single master/multiple replica system, where the read/write copy of the database is held by the Front End Server that contains the Central Management Server.</span></span> <span data-ttu-id="76986-108">Jeder Computer in der Topologie, einschließlich des Front-End-Servers, der den zentralen Verwaltungsserver enthält, verfügt über eine schreibgeschützte Kopie der zentralen Verwaltungsspeicher Daten in der SQL Server-Datenbank (standardmäßig mit dem Namen RTCLOCAL), die während der Einrichtung und Bereitstellung auf dem Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="76986-108">Each computer in the topology, including the Front End Server that contains the Central Management Server, has a read-only copy of the Central Management store data in the SQL Server database (named RTCLOCAL by default) installed on the computer during setup and deployment.</span></span> <span data-ttu-id="76986-109">Die lokale Datenbank erhält Replikat Updates über den lync Server Replica Replicator-Agent, der auf allen Computern als Dienst ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="76986-109">The local database receives replica updates by way of the Lync Server Replica Replicator Agent that runs as a service on all computers.</span></span> <span data-ttu-id="76986-110">Der Name der tatsächlichen Datenbank auf dem zentralen Verwaltungs Server und das lokale Replikat ist XDS, das aus den Dateien XDS. mdf und XDS. ldf besteht.</span><span class="sxs-lookup"><span data-stu-id="76986-110">The name of the actual database on the Central Management Server and the local replica is XDS, which is made up of the xds.mdf and xds.ldf files.</span></span> <span data-ttu-id="76986-111">Auf den Speicherort der Master Datenbank wird in den Active Directory-Domänendiensten von einem Dienst Kontrollpunkt (Service Control Point, SCP) verwiesen.</span><span class="sxs-lookup"><span data-stu-id="76986-111">The master database location is referenced by a service control point (SCP) in Active Directory Domain Services.</span></span> <span data-ttu-id="76986-112">Alle Tools, die den zentralen Verwaltungs Server zum Verwalten und Konfigurieren von lync Server verwenden, verwenden den SCP, um den zentralen Verwaltungsspeicher zu finden.</span><span class="sxs-lookup"><span data-stu-id="76986-112">All tools that use the Central Management Server to manage and configure Lync Server use the SCP to locate the Central Management store.</span></span>

<span data-ttu-id="76986-113">Nachdem Sie den zentralen Verwaltungsserver erfolgreich verschoben haben, sollten Sie die zentralen Verwaltungsserver Datenbanken vom ursprünglichen Front-End-Server entfernen.</span><span class="sxs-lookup"><span data-stu-id="76986-113">After you have successfully moved the Central Management Server, you should remove the Central Management Server databases from the original Front End Server.</span></span> <span data-ttu-id="76986-114">Informationen zum Entfernen der zentralen Verwaltungs Server-Datenbanken finden Sie unter [Entfernen der SQL Server-Datenbank für einen Front-End-Pool](remove-the-sql-server-database-for-a-front-end-pool.md).</span><span class="sxs-lookup"><span data-stu-id="76986-114">For information on removing the Central Management Server databases, see [Remove the SQL Server database for a Front End pool](remove-the-sql-server-database-for-a-front-end-pool.md).</span></span>

<span data-ttu-id="76986-115">Sie verwenden das Windows PowerShell **-Cmdlet Move-CsManagementServer** in der lync Server-Verwaltungsshell, um die Datenbank aus der lync Server 2010 SQL Server-Datenbank in die lync Server 2013 SQL Server-Datenbank zu verschieben und dann den SCP so zu aktualisieren, dass er auf den Standort des zentralen Verwaltungsservers von lync Server 2013 verweist.</span><span class="sxs-lookup"><span data-stu-id="76986-115">You use the Windows PowerShell cmdlet **Move-CsManagementServer** in the Lync Server Management Shell to move the database from the Lync Server 2010 SQL Server database to the Lync Server 2013 SQL Server database, and then update the SCP to point to the Lync Server 2013 Central Management Server location.</span></span>

<div>

## <a name="preparing-lync-server-2013-front-end-servers-before-moving-the-central-management-server"></a><span data-ttu-id="76986-116">Vorbereiten der lync Server 2013-Front-End-Server vor dem Verschieben des zentralen Verwaltungsservers</span><span class="sxs-lookup"><span data-stu-id="76986-116">Preparing Lync Server 2013 Front End Servers before moving the Central Management Server</span></span>

<span data-ttu-id="76986-117">Führen Sie die Verfahren in diesem Abschnitt aus, um die lync Server 2013-Front-End-Server vorzubereiten, bevor Sie den zentralen Verwaltungs Server für lync Server 2010 verschieben.</span><span class="sxs-lookup"><span data-stu-id="76986-117">Use the procedures in this section to prepare the Lync Server 2013 Front End Servers before you move the Lync Server 2010 Central Management Server.</span></span>

<div>

## <a name="to-prepare-an-enterprise-edition-front-end-pool"></a><span data-ttu-id="76986-118">Vorbereiten eines Enterprise Edition-Front-End-Pools</span><span class="sxs-lookup"><span data-stu-id="76986-118">To prepare an Enterprise Edition Front End pool</span></span>

1.  <span data-ttu-id="76986-119">Klicken Sie im Front-End-Pool von lync Server 2013 Enterprise Edition, in dem Sie den zentralen Verwaltungs Server umsiedeln möchten: Melden Sie sich bei dem Computer an, auf dem die lync Server-Verwaltungsshell als Mitglied der **RTCUniversalServerAdmins** -Gruppe installiert ist.</span><span class="sxs-lookup"><span data-stu-id="76986-119">On the Lync Server 2013 Enterprise Edition Front End pool where you want to relocate the Central Management Server: Log on to the computer where the Lync Server Management Shell is installed as a member of the **RTCUniversalServerAdmins** group.</span></span> <span data-ttu-id="76986-120">Sie müssen auch über die SQL Server-Datenbank sysadmin-Benutzerrechte und-Berechtigungen für die Datenbank verfügen, in der Sie den zentralen Verwaltungsspeicher installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="76986-120">You must also have SQL Server database sysadmin user rights and permissions on the database where you want to install the Central Management store.</span></span>

2.  <span data-ttu-id="76986-121">Öffnen Sie die lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="76986-121">Open the Lync Server Management Shell.</span></span>

3.  <span data-ttu-id="76986-122">Zum Erstellen des neuen zentralen Verwaltungsspeichers in der lync Server 2013 SQL Server-Datenbank geben Sie in der lync Server-Verwaltungsshell Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="76986-122">To create the new Central Management store in the Lync Server 2013 SQL Server database, in the Lync Server Management Shell, type:</span></span>
    
        Install-CsDatabase -CentralManagementDatabase -SQLServerFQDN <FQDN of your SQL Server> -SQLInstanceName <name of instance>

4.  <span data-ttu-id="76986-123">Vergewissern Sie sich, dass der Status des **lync Server-Front-End-** Diensts **gestartet** wurde.</span><span class="sxs-lookup"><span data-stu-id="76986-123">Confirm that the status of the **Lync Server Front-End** service is **Started**.</span></span>

</div>

<div>

## <a name="to-prepare-a-standard-edition-front-end-server"></a><span data-ttu-id="76986-124">Vorbereiten eines Standard Edition-Front-End-Servers</span><span class="sxs-lookup"><span data-stu-id="76986-124">To prepare a Standard Edition Front End Server</span></span>

1.  <span data-ttu-id="76986-125">Auf dem lync Server 2013 Standard Edition-Front-End-Server, auf dem Sie den zentralen Verwaltungsserver verschieben möchten: Melden Sie sich bei dem Computer an, auf dem die lync Server-Verwaltungsshell als Mitglied der **RTCUniversalServerAdmins** -Gruppe installiert ist.</span><span class="sxs-lookup"><span data-stu-id="76986-125">On the Lync Server 2013 Standard Edition Front End Server where you want to relocate the Central Management Server: Log on to the computer where the Lync Server Management Shell is installed as a member of the **RTCUniversalServerAdmins** group.</span></span>

2.  <span data-ttu-id="76986-126">Öffnen Sie den lync Server-Bereitstellungs-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="76986-126">Open the Lync Server Deployment Wizard.</span></span>

3.  <span data-ttu-id="76986-127">Klicken Sie im lync Server-Bereitstellungs-Assistenten auf **First Standard Edition-Server vorbereiten**.</span><span class="sxs-lookup"><span data-stu-id="76986-127">In the Lync Server Deployment Wizard, click **Prepare first Standard Edition server**.</span></span>

4.  <span data-ttu-id="76986-128">Auf der Seite **Ausführungsbefehle** wird SQL Server Express als zentraler Verwaltungs Server installiert.</span><span class="sxs-lookup"><span data-stu-id="76986-128">On the **Executing Commands** page, SQL Server Express is installed as the Central Management Server.</span></span> <span data-ttu-id="76986-129">Es werden erforderliche Firewallregeln erstellt.</span><span class="sxs-lookup"><span data-stu-id="76986-129">Necessary firewall rules are created.</span></span> <span data-ttu-id="76986-130">Wenn die Installation der Datenbank und der erforderlichen Software abgeschlossen ist, klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="76986-130">When the installation of the database and prerequisite software is completed, click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="76986-131">Die anfängliche Installation kann einige Zeit in Anspruch nehmen, ohne dass die Anzeige des Befehlsausgabe Zusammenfassungsbildschirms sichtbar wird.</span><span class="sxs-lookup"><span data-stu-id="76986-131">The initial installation may take some time with no visible updates to the command output summary screen.</span></span> <span data-ttu-id="76986-132">Dies ist auf die Installation von SQL Server Express zurückzuführen.</span><span class="sxs-lookup"><span data-stu-id="76986-132">This is due to the installation of the SQL Server Express.</span></span> <span data-ttu-id="76986-133">Wenn Sie die Installation der Datenbank überwachen müssen, verwenden Sie den Task-Manager, um das Setup zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="76986-133">If you need to monitor the installation of the database, use Task Manager to monitor the setup.</span></span>

    
    </div>

5.  <span data-ttu-id="76986-134">Zum Erstellen des neuen zentralen Verwaltungsspeichers auf dem lync Server 2013 Standard Edition-Front-End-Server geben Sie in der lync Server-Verwaltungsshell Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="76986-134">To create the new Central Management store on the Lync Server 2013 Standard Edition Front End Server, in the Lync Server Management Shell, type:</span></span>
    
        Install-CsDatabase -CentralManagementDatabase -SQLServerFQDN <FQDN of your Standard Edition Server> -SQLInstanceName <name of instance - RTC by default>

6.  <span data-ttu-id="76986-135">Vergewissern Sie sich, dass der Status des **lync Server-Front-End-** Diensts **gestartet** wurde.</span><span class="sxs-lookup"><span data-stu-id="76986-135">Confirm that the status of the **Lync Server Front-End** service is **Started**.</span></span>

</div>

</div>

<div>

## <a name="to-move-the-lync-server-2010-central-management-server-to-lync-server-2013"></a><span data-ttu-id="76986-136">So verschieben Sie den lync Server 2010 Central-Verwaltungs Server nach lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="76986-136">To move the Lync Server 2010 Central Management Server to Lync Server 2013</span></span>

1.  <span data-ttu-id="76986-137">Auf dem lync Server 2013-Server, der der zentrale Verwaltungsserver sein soll: Melden Sie sich bei dem Computer an, auf dem die lync Server-Verwaltungsshell als Mitglied der **RTCUniversalServerAdmins** -Gruppe installiert ist.</span><span class="sxs-lookup"><span data-stu-id="76986-137">On the Lync Server 2013 server that will be the Central Management Server: Log on to the computer where the Lync Server Management Shell is installed as a member of the **RTCUniversalServerAdmins** group.</span></span> <span data-ttu-id="76986-138">Sie müssen auch über die Benutzerrechte und-Berechtigungen des SQL Server-Datenbankadministrators verfügen.</span><span class="sxs-lookup"><span data-stu-id="76986-138">You must also have the SQL Server database administrator user rights and permissions.</span></span>

2.  <span data-ttu-id="76986-139">Öffnen Sie die Lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="76986-139">Open Lync Server Management Shell.</span></span>

3.  <span data-ttu-id="76986-140">Geben Sie in der lync Server-Verwaltungsshell Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="76986-140">In the Lync Server Management Shell, type:</span></span>
    
        Enable-CsTopology
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="76986-141">Wenn <CODE>Enable-CsTopology</CODE> dies nicht der Fall ist, beheben Sie das Problem, das verhindert, dass der Befehl abgeschlossen wird, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="76986-141">If <CODE>Enable-CsTopology</CODE> is not successful, resolve the problem preventing the command from completing before continuing.</span></span> <span data-ttu-id="76986-142">Wenn <STRONG>enable-CsTopology</STRONG> nicht erfolgreich ist, schlägt die Verschiebung fehl, und Sie verlässt Ihre Topologie möglicherweise in einem Zustand, in dem kein zentraler Verwaltungsspeicher vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="76986-142">If <STRONG>Enable-CsTopology</STRONG> is not successful, the move will fail and it may leave your topology in a state where there is no Central Management store.</span></span>

    
    </div>

4.  <span data-ttu-id="76986-143">Geben Sie auf dem lync Server 2013-Front-End-Server oder-Front-End-Pool in der lync Server-Verwaltungsshell Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="76986-143">On the Lync Server 2013 Front End Server or Front End pool, in the Lync Server Management Shell, type:</span></span>
    
        Move-CsManagementServer

5.  <span data-ttu-id="76986-144">In der lync Server-Verwaltungsshell werden die Server, Dateispeicher, Datenbankspeicher und die Dienstverbindungspunkte des aktuellen Zustands und des vorgeschlagenen Zustands angezeigt.</span><span class="sxs-lookup"><span data-stu-id="76986-144">Lync Server Management Shell displays the servers, file stores, database stores, and the service connection points of the Current State and the Proposed State.</span></span> <span data-ttu-id="76986-145">Lesen Sie die Informationen sorgfältig durch, und bestätigen Sie, dass dies die beabsichtigte Quelle und das Ziel ist.</span><span class="sxs-lookup"><span data-stu-id="76986-145">Read the information carefully and confirm that this is the intended source and destination.</span></span> <span data-ttu-id="76986-146">Geben Sie **Y** ein, um fortzufahren, oder **N** , um die Verschiebung zu beenden.</span><span class="sxs-lookup"><span data-stu-id="76986-146">Type **Y** to continue, or **N** to stop the move.</span></span>

6.  <span data-ttu-id="76986-147">Überprüfen Sie alle Warnungen oder Fehler, die durch den Befehl **Move-CsManagementServer** generiert wurden, und beheben Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="76986-147">Review any warnings or errors generated by the **Move-CsManagementServer** command and resolve them.</span></span>

7.  <span data-ttu-id="76986-148">Öffnen Sie auf dem lync Server 2013-Server den lync Server-Bereitstellungs-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="76986-148">On the Lync Server 2013 server, open the Lync Server Deployment Wizard.</span></span>

8.  <span data-ttu-id="76986-149">Klicken Sie im lync Server-Bereitstellungs-Assistenten auf **lync Server System installieren oder aktualisieren**, klicken Sie auf **Schritt 2: Einrichten oder Entfernen von lync Server-Komponenten**, klicken Sie auf **weiter**, überprüfen Sie die Zusammenfassung, und klicken Sie dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="76986-149">In Lync Server Deployment Wizard, click **Install or Update Lync Server System**, click **Step 2: Setup or Remove Lync Server Components**, click **Next**, review the summary, and then click **Finish**.</span></span>

9.  <span data-ttu-id="76986-150">Öffnen Sie auf dem lync Server 2010-Server den lync Server-Bereitstellungs-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="76986-150">On the Lync Server 2010 server, open the Lync Server Deployment Wizard.</span></span>

10. <span data-ttu-id="76986-151">Klicken Sie im lync Server-Bereitstellungs-Assistenten auf **lync Server System installieren oder aktualisieren**, klicken Sie auf **Schritt 2: Einrichten oder Entfernen von lync Server-Komponenten**, klicken Sie auf **weiter**, überprüfen Sie die Zusammenfassung, und klicken Sie dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="76986-151">In Lync Server Deployment Wizard, click **Install or Update Lync Server System**, click **Step 2: Setup or Remove Lync Server Components**, click **Next**, review the summary, and then click **Finish**.</span></span>

11. <span data-ttu-id="76986-152">Starten Sie den lync Server 2013-Server neu.</span><span class="sxs-lookup"><span data-stu-id="76986-152">Reboot the Lync Server 2013 server.</span></span> <span data-ttu-id="76986-153">Dies ist aufgrund einer Änderung der Gruppenmitgliedschaft für den Zugriff auf die zentrale Verwaltungs Server-Datenbank erforderlich.</span><span class="sxs-lookup"><span data-stu-id="76986-153">This is required because of a group membership change to access Central Management Server database.</span></span>

12. <span data-ttu-id="76986-154">Um zu bestätigen, dass die Replikation mit dem neuen zentralen Verwaltungsspeicher erfolgt, geben Sie in der lync Server-Verwaltungsshell Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="76986-154">To confirm that replication with the new Central Management store is occurring, in the Lync Server Management Shell, type:</span></span>
    
        Get-CsManagementStoreReplicationStatus
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="76986-155">Die Replikation kann einige Zeit dauern, bis alle aktuellen Replikate aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="76986-155">The replication may take some time to update all current replicas.</span></span>

    
    </div>

</div>

<div>

## <a name="to-remove-lync-server-2010-central-management-store-files-after-a-move"></a><span data-ttu-id="76986-156">So entfernen Sie nach einem Umzug lync Server 2010 Central Management Store-Dateien</span><span class="sxs-lookup"><span data-stu-id="76986-156">To remove Lync Server 2010 Central Management store files after a move</span></span>

1.  <span data-ttu-id="76986-157">Auf dem lync Server 2010-Server: Melden Sie sich bei dem Computer an, auf dem die lync Server-Verwaltungsshell als Mitglied der **RTCUniversalServerAdmins** -Gruppe installiert ist.</span><span class="sxs-lookup"><span data-stu-id="76986-157">On the Lync Server 2010 server: Log on to the computer where the Lync Server Management Shell is installed as a member of the **RTCUniversalServerAdmins** group.</span></span> <span data-ttu-id="76986-158">Sie müssen auch über die Benutzerrechte und-Berechtigungen des SQL Server-Datenbankadministrators verfügen.</span><span class="sxs-lookup"><span data-stu-id="76986-158">You must also have the SQL Server database administrator user rights and permissions.</span></span>

2.  <span data-ttu-id="76986-159">Öffnen der lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="76986-159">Open Lync Server Management Shell</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="76986-160">Gehen Sie nicht mit dem Entfernen der vorherigen Datenbankdateien fort, bis die Replikation abgeschlossen und stabil ist.</span><span class="sxs-lookup"><span data-stu-id="76986-160">Do not proceed with the removal of the previous database files until replication is complete and is stable.</span></span> <span data-ttu-id="76986-161">Wenn Sie die Dateien vor dem Abschließen der Replikation entfernen, werden Sie den Replikationsprozess unterbrechen und den neu verschobenen zentralen Verwaltungs Server in einem unbekannten Zustand belässt.</span><span class="sxs-lookup"><span data-stu-id="76986-161">If you remove the files prior to completing replication, you will disrupt the replication process and leave the newly moved Central Management Server in an unknown state.</span></span> <span data-ttu-id="76986-162">Verwenden Sie das Cmdlet <STRONG>Get-CsManagementStoreReplicationStatus</STRONG> , um den Replikationsstatus zu bestätigen.</span><span class="sxs-lookup"><span data-stu-id="76986-162">Use the cmdlet <STRONG>Get-CsManagementStoreReplicationStatus</STRONG> to confirm the replication status.</span></span>

    
    </div>

3.  <span data-ttu-id="76986-163">Wenn Sie die zentralen Verwaltungsspeicher-Datenbankdateien vom lync Server 2010 Central-Verwaltungs Server entfernen möchten, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="76986-163">To remove the Central Management store database files from the Lync Server 2010 Central Management Server, type:</span></span>
    
        Uninstall-CsDatabase -CentralManagementDatabase -SqlServerFqdn <FQDN of SQL Server> -SqlInstanceName <Name of source server>
    
    <span data-ttu-id="76986-164">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="76986-164">For example:</span></span>
    
        Uninstall-CsDatabase -CentralManagementDatabase -SqlServerFqdn sql.contoso.net -SqlInstanceName rtc
    
    <span data-ttu-id="76986-165">Dabei \<FQDN of SQL Server\> handelt es sich entweder um den lync Server 2010-Back-End-Server in einer Enterprise Edition-Bereitstellung oder um den FQDN des Standard Edition-Servers.</span><span class="sxs-lookup"><span data-stu-id="76986-165">Where the \<FQDN of SQL Server\> is either the Lync Server 2010 Back End Server in an Enterprise Edition deployment or the FQDN of the Standard Edition server.</span></span>

<span data-ttu-id="76986-166"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="76986-166"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

