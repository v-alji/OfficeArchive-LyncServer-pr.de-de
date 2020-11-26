---
title: 'Lync Server 2013: Ausführen eines Failovers für einen Pool'
description: 'Lync Server 2013: Failover eines Pools.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over a pool
ms:assetid: 10b13732-bc80-4cb2-a71c-56b1d6cb5bbb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204678(v=OCS.15)
ms:contentKeyID: 48183432
ms.date: 10/10/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 819137c1277c5058f4e5d36ef5dbe71e672e8641
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428265"
---
# <a name="failing-over-a-pool-in-lync-server-2013"></a><span data-ttu-id="3fa6e-103">Ausführen eines Failovers für einen Pool in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3fa6e-103">Failing over a pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3fa6e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3fa6e-104">

<span> </span></span></span>

<span data-ttu-id="3fa6e-105">_**Letztes Änderungsdatum des Themas:** 2014-10-10_</span><span class="sxs-lookup"><span data-stu-id="3fa6e-105">_**Topic Last Modified:** 2014-10-10_</span></span>

<span data-ttu-id="3fa6e-106">Wenn ein einzelner Front-End-Pool ausgefallen ist und ein Failover durchgeführt werden muss, gehen Sie wie folgt vor:</span><span class="sxs-lookup"><span data-stu-id="3fa6e-106">If a single Front End pool has failed and needs to be failed over, use the following procedure.</span></span> <span data-ttu-id="3fa6e-107">In diesem Verfahren enthält Datacenter1 pool1, und pool1 ist fehlgeschlagen.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-107">In this procedure, Datacenter1 contains Pool1, and Pool1 has failed.</span></span> <span data-ttu-id="3fa6e-108">Sie haben einen Failover zu Pool2 befindet sich in Datacenter2.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-108">You are failing over to Pool2 located in Datacenter2.</span></span>

<span data-ttu-id="3fa6e-109">Der größte Teil der Arbeit für das Pool-Failover umfasst einen Failover des zentralen Verwaltungsspeichers, falls dies erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-109">Most of the work for the pool failover involves failing over the Central Management store, if it is required.</span></span> <span data-ttu-id="3fa6e-110">Dies ist wichtig, da der zentrale Verwaltungsspeicher funktionsfähig sein muss, wenn die Benutzer des Pools fehlerhaft sind.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-110">This is important because the Central Management store must be functional when the pool’s users are failed over.</span></span>

<span data-ttu-id="3fa6e-111">Wenn ein Front-End-Pool fehlschlägt, der Edge-Pool an dieser Website jedoch weiterhin ausgeführt wird, müssen Sie wissen, ob der Edge-Pool den fehlerhaften Pool als nächsten Hop-Pool verwendet.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-111">Additionally, if a Front End pool fails but the Edge pool at that site is still running, you must know whether the Edge pool uses the failed pool as a next hop pool.</span></span> <span data-ttu-id="3fa6e-112">Wenn dies der Fall ist, müssen Sie den Edge-Pool so ändern, dass ein anderer Front-End-Pool verwendet wird, bevor der fehlerhafte Front-End-Pool fehlschlägt.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-112">If it does, you must change the Edge pool to use a different Front End pool before failing over the failed Front End pool.</span></span> <span data-ttu-id="3fa6e-113">Wie Sie die Einstellung für den nächsten Hop ändern, hängt davon ab, ob der Edge-Pool am gleichen Standort wie der Edge-Pool oder auf einer anderen Website verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-113">How you change the next hop setting depends on whether the Edge will use a pool at the same site as the Edge pool, or a different site.</span></span>

<span data-ttu-id="3fa6e-114">**So stellen Sie einen Edge-Pool für die Verwendung eines Next Hop-Pools auf derselben Website ein**</span><span class="sxs-lookup"><span data-stu-id="3fa6e-114">**To Set an Edge Pool to Use a Next Hop Pool at the Same Site**</span></span>

1.  <span data-ttu-id="3fa6e-115">Öffnen Sie den Topologie-Generator, klicken Sie mit der rechten Maustaste auf den zu ändernden Edge-Pool, und klicken Sie auf **Eigenschaften bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-115">Open Topology Builder, right-click the Edge pool that needs to be changed, and click **Edit Properties**.</span></span>

2.  <span data-ttu-id="3fa6e-116">Klicken Sie auf **Nächster Hop**.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-116">Click **Next Hop**.</span></span> <span data-ttu-id="3fa6e-117">Wählen Sie in der Liste **Nächster Hop-Pool:** den Pool aus, der nun als nächster Hop-Pool fungieren soll.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-117">From the **Next hop pool:** list, select the pool which will now serve as the next hop pool.</span></span>

3.  <span data-ttu-id="3fa6e-118">Klicken Sie auf **OK**, und veröffentlichen Sie die Änderungen.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-118">Click **OK**, and then publish the changes.</span></span>

<span data-ttu-id="3fa6e-119">**So stellen Sie einen Edge-Pool für die Verwendung eines Next Hop-Pools an einer anderen Website ein**</span><span class="sxs-lookup"><span data-stu-id="3fa6e-119">**To Set an Edge Pool to Use a Next Hop Pool at a Different Site**</span></span>

1.  <span data-ttu-id="3fa6e-120">Öffnen Sie ein lync Server-Verwaltungsshell-Fenster, und geben Sie das folgende Cmdlet ein:</span><span class="sxs-lookup"><span data-stu-id="3fa6e-120">Open a Lync Server Management Shell window and type the following cmdlet:</span></span>
    
        Set-CsEdgeServer -Identity EdgeServer:<Edge Server pool FQDN> -Registrar Registrar:<NextHopPoolFQDN>

<span data-ttu-id="3fa6e-121">**So führen Sie einen Failover eines Pools in einem Notfall durch**</span><span class="sxs-lookup"><span data-stu-id="3fa6e-121">**To Fail Over a Pool in a Disaster**</span></span>

1.  <span data-ttu-id="3fa6e-122">Ermitteln Sie, welcher Pool der Host für den zentralen Verwaltungsserver ist, indem Sie das folgende Cmdlet auf einem Front-End-Server in Pool2 eingeben:</span><span class="sxs-lookup"><span data-stu-id="3fa6e-122">Find which pool is the host for the Central Management Server by typing the following cmdlet on a Front End server in Pool2:</span></span>
    
        Invoke-CsManagementServerFailover -Whatif
    
    <span data-ttu-id="3fa6e-123">Die Ergebnisse dieses Cmdlets zeigen, in welchem Pool zurzeit der zentrale Verwaltungs Server gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-123">The results of this cmdlet show which pool currently hosts the Central Management Server.</span></span> <span data-ttu-id="3fa6e-124">Im weiteren Verlauf dieses Verfahrens wird dieser Pool als "CMS \_ -Pool" bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-124">In the rest of this procedure, this pool is known as CMS\_Pool.</span></span>

2.  <span data-ttu-id="3fa6e-125">Verwenden Sie den Topologie-Generator, um die Version von lync Server zu finden, die im CMS \_ -Pool ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-125">Use Topology Builder to find the version of Lync Server running on the CMS\_Pool.</span></span> <span data-ttu-id="3fa6e-126">Wenn Sie lync Server 2013 ausführen, verwenden Sie das folgende Cmdlet, um den Sicherungspool von Pool 1 zu finden.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-126">If it is running Lync Server 2013, use the following cmdlet to find the backup pool of Pool 1.</span></span>
    
        Get-CsPoolBackupRelationship -PoolFQDN <CMS_Pool FQDN>
    
    <span data-ttu-id="3fa6e-127">Lassen Sie \_ den Backup-Pool zum Backup-Pool werden.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-127">Let Backup\_Pool be the backup pool.</span></span>

3.  <span data-ttu-id="3fa6e-128">Überprüfen Sie den Status des zentralen Verwaltungsspeichers mit dem folgenden Cmdlet:</span><span class="sxs-lookup"><span data-stu-id="3fa6e-128">Check the status of the Central Management store with the following cmdlet:</span></span>
    
        Get-CsManagementStoreReplicationStatus -CentralManagementStoreStatus 
    
    <span data-ttu-id="3fa6e-129">Dieses Cmdlet sollte anzeigen, dass sowohl ActiveMasterFQDN als auch ActiveFileTransferAgents auf den FQDN des CMS- \_ Pools verweisen.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-129">This cmdlet should show that both ActiveMasterFQDN and ActiveFileTransferAgents are pointing to the FQDN of CMS\_Pool.</span></span> <span data-ttu-id="3fa6e-130">Wenn Sie leer sind, steht der zentrale Verwaltungs Server nicht zur Verfügung, und Sie müssen einen Failover durchführen.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-130">If they are empty, the Central Management Server is not available and you must fail it over.</span></span>

4.  <span data-ttu-id="3fa6e-131">Wenn der zentrale Verwaltungsspeicher nicht verfügbar ist oder wenn der zentrale Verwaltungsspeicher auf pool1 ausgeführt wurde (also der Pool, bei dem ein Fehler aufgetreten ist), müssen Sie vor dem Failover des Pools einen Failover für den zentralen Verwaltungs Server durchführen.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-131">If the Central Management store is not available or if the Central Management store was running on Pool1 (that is, the pool that has failed), you must fail over the Central Management Server before failing over the pool.</span></span> <span data-ttu-id="3fa6e-132">Wenn Sie einen Failover für den zentralen Verwaltungs Server durchführen müssen, der in einem Pool mit lync Server 2013 gehostet wurde, verwenden Sie das Cmdlet in Schritt 5 dieses Verfahrens.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-132">If you need to fail over the Central Management Server that was hosted on a pool running Lync Server 2013, use the cmdlet in step 5 of this procedure.</span></span> <span data-ttu-id="3fa6e-133">Wenn Sie einen Failover für den zentralen Verwaltungs Server durchführen müssen, der in einem Pool mit lync Server 2010 gehostet wurde, verwenden Sie das Cmdlet in Schritt 6 dieses Verfahrens.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-133">If you need to fail over the Central Management Server that was hosted on a pool running Lync Server 2010, use the cmdlet in step 6 of this procedure.</span></span> <span data-ttu-id="3fa6e-134">Wenn Sie keinen Failover für den zentralen Verwaltungs Server benötigen, fahren Sie mit Schritt 7 dieses Verfahrens fort.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-134">If you do not need to fail over the Central Management Server, skip to step 7 of this procedure.</span></span>

5.  <span data-ttu-id="3fa6e-135">Gehen Sie wie folgt vor, um einen Failover des zentralen Verwaltungsspeichers in einem Pool mit lync Server 2013 auszuführen:</span><span class="sxs-lookup"><span data-stu-id="3fa6e-135">To fail over the Central Management store on a pool running Lync Server 2013, do the following:</span></span>
    
      - <span data-ttu-id="3fa6e-136">Überprüfen Sie zunächst, welcher Back-End-Server im Sicherungs \_ Pool die Prinzipalinstanz des zentralen Verwaltungsspeichers ausführt, indem Sie Folgendes eingeben:</span><span class="sxs-lookup"><span data-stu-id="3fa6e-136">First, check which Back End Server in Backup\_Pool runs the principal instance of the Central Management store by typing the following:</span></span>
        
            Get-CsDatabaseMirrorState -DatabaseType Centralmgmt -PoolFqdn <Backup_Pool Fqdn>
    
      - <span data-ttu-id="3fa6e-137">Wenn der primäre Back-End-Server im Sicherungs \_ Pool der Prinzipal ist, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="3fa6e-137">If the primary Back End Server in Backup\_Pool is the principal, type:</span></span>
        
            Invoke-CSManagementServerFailover -BackupSQLServerFqdn <Backup_Pool Primary BackEnd Server FQDN> -BackupSQLInstanceName <Backup_Pool Primary SQL Instance Name>
        
        <span data-ttu-id="3fa6e-138">Wenn der Spiegelungs-Back-End-Server im Sicherungs \_ Pool der Prinzipal ist, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="3fa6e-138">If the mirror Back End Server in Backup\_Pool is the principal, type:</span></span>
        
            Invoke-CSManagementServerFailover -MirrorSQLServerFqdn <Backup_Pool Mirror BackEnd Server FQDN> -MirrorSQLInstanceName <Backup_Pool Mirror SQL Instance Name>
    
      - <span data-ttu-id="3fa6e-139">Überprüfen Sie, ob der Failover des zentralen Verwaltungsservers abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-139">Validate that the Central Management Server failover is complete.</span></span> <span data-ttu-id="3fa6e-140">Geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="3fa6e-140">Type the following:</span></span>
        
            Get-CsManagementStoreReplicationStatus -CentralManagementStoreStatus 
        
        <span data-ttu-id="3fa6e-141">Überprüfen Sie, ob sowohl ActiveMasterFQDN als auch ActiveFileTransferAgents auf den FQDN des Sicherungs \_ Pools verweisen.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-141">Check that both ActiveMasterFQDN and ActiveFileTransferAgents are pointing to the FQDN of Backup\_Pool.</span></span>
    
      - <span data-ttu-id="3fa6e-142">Überprüfen Sie abschließend den Replikatstatus für alle Front-End-Server, indem Sie Folgendes eingeben:</span><span class="sxs-lookup"><span data-stu-id="3fa6e-142">Finally, check the replica status for all Front End Servers by typing the following:</span></span>
        
            Get-CsManagementStoreReplicationStatus 
        
        <span data-ttu-id="3fa6e-143">Überprüfen Sie, ob alle Replikate den Wert true aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-143">Check that all replicas have a value of True.</span></span>
        
        <span data-ttu-id="3fa6e-144">Fahren Sie mit Schritt 7 in diesem Verfahren fort.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-144">Skip to step 7 in this procedure.</span></span>

6.  <span data-ttu-id="3fa6e-145">Installieren Sie den zentralen Verwaltungsspeicher auf dem Back-End-Server des Sicherungs \_ Pools.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-145">Install the Central Management store on the Back End Server of Backup\_Pool.</span></span>
    
      - <span data-ttu-id="3fa6e-146">Führen Sie zunächst den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="3fa6e-146">First, run the following command:</span></span>
        
        ```PowerShell 
        Install-CsDatabase -CentralManagementDatabase -Clean -SqlServerFqdn <Backup_Pool Back End Server FQDN> -SqlInstanceName rtc  
        ```
    
      - <span data-ttu-id="3fa6e-147">Führen Sie den nächsten Befehl auf einem der Front-End-Server des Sicherungs \_ Pools aus, um den Wechsel des zentralen Verwaltungsspeichers zu erzwingen:</span><span class="sxs-lookup"><span data-stu-id="3fa6e-147">Run the next command on one of the Front End Servers of Backup\_Pool to force the move of the Central Management store:</span></span>
        
            Move-CsManagementServer -ConfigurationFileName c:\CsConfigurationFile.zip -LisConfigurationFileName c:\CsLisConfigurationFile.zip -Force 
    
      - <span data-ttu-id="3fa6e-148">Überprüfen Sie, ob die Verschiebung abgeschlossen ist:</span><span class="sxs-lookup"><span data-stu-id="3fa6e-148">Validate the move is complete:</span></span>
        
            Get-CsManagementStoreReplicationStatus -CentralManagementStoreStatus 
        
        <span data-ttu-id="3fa6e-149">Überprüfen Sie, ob sowohl ActiveMasterFQDN als auch ActiveFileTransferAgents auf den FQDN des Sicherungs \_ Pools verweisen.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-149">Check that both ActiveMasterFQDN and ActiveFileTransferAgents are pointing to the FQDN of Backup\_Pool.</span></span>
    
      - <span data-ttu-id="3fa6e-150">Überprüfen Sie den Replikatstatus für alle Front-End-Server, indem Sie Folgendes eingeben:</span><span class="sxs-lookup"><span data-stu-id="3fa6e-150">Check the replica status for all Front End Servers by typing the following:</span></span>
        
            Get-CsManagementStoreReplicationStatus 
        
        <span data-ttu-id="3fa6e-151">Überprüfen Sie, ob alle Replikate den Wert true aufweisen.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-151">Check that all replicas have a value of True.</span></span>
    
      - <span data-ttu-id="3fa6e-152">Installieren Sie den zentralen Verwaltungs Server Dienst auf den restlichen Front-End-Servern im Sicherungs \_ Pool.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-152">Install the Central Management Server service on the rest of the Front End Servers in Backup\_Pool.</span></span> <span data-ttu-id="3fa6e-153">Führen Sie dazu den folgenden Befehl auf allen Front-End-Servern aus, mit Ausnahme derjenigen, die Sie beim Erzwingen des zentralen Verwaltungsspeichers weiter oben in diesem Verfahren verwendet haben:</span><span class="sxs-lookup"><span data-stu-id="3fa6e-153">To do so, run the following command on all the Front End Servers, except the one you used when forcing the Central Management store move earlier in this procedure:</span></span>
        
            Bootstrapper /Setup 

7.  <span data-ttu-id="3fa6e-154">Führen Sie einen Failover der Benutzer von pool1 zu Pool2 durch, indem Sie das folgende Cmdlet in einem Fenster der lync Server-Verwaltungsshell ausführen:</span><span class="sxs-lookup"><span data-stu-id="3fa6e-154">Fail over the users from Pool1 to Pool2 by running the following cmdlet in a Lync Server Management Shell window:</span></span>
    
        Invoke-CsPoolFailover -PoolFQDN <Pool1 FQDN> -DisasterMode -Verbose
    
    <span data-ttu-id="3fa6e-155">Da die Schritte, die in den vorherigen Abschnitten dieses Verfahrens zur Überprüfung des Status des zentralen Verwaltungsspeichers durchgeführt wurden, nicht universell sind, besteht weiterhin die Möglichkeit, dass dieses Cmdlet fehlschlägt, da der zentrale Verwaltungsspeicher noch nicht vollständig fehlerhaft ist.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-155">Because the steps taken in the previous parts of this procedure to check the Central Management store status are not universal, there is still a chance this cmdlet will fail because the Central Management store is not yet fully failed over.</span></span> <span data-ttu-id="3fa6e-156">In diesem Fall müssen Sie den zentralen Verwaltungsspeicher basierend auf den angezeigten Fehlermeldungen korrigieren und dieses Cmdlet dann erneut ausführen.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-156">In this case, you must fix the Central Management store based on the error messages that you see, and then run this cmdlet again.</span></span>
    
    <span data-ttu-id="3fa6e-157">Wenn die folgende Fehlermeldung angezeigt wird, müssen Sie den Edge-Pool auf dieser Website ändern, um einen anderen Pool als nächsten Hop zu verwenden, bevor Sie einen Failover für den Pool durchführen.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-157">If you see the following error message, then you need to change the Edge pool at this site to use a different pool as its next hop before failing over the pool.</span></span> <span data-ttu-id="3fa6e-158">Ausführliche Informationen finden Sie in den Verfahren am Anfang dieses Themas.</span><span class="sxs-lookup"><span data-stu-id="3fa6e-158">For details, see the procedures at the beginning of this topic.</span></span>
    
        Invoke-CsPoolFailOver : This Front-end pool "pool1.contoso.com" is specified in
        topology as the next hop for the Edge server. Failing over this pool may cause External
        access/Federation/Split-domain/XMPP features to stop working. Please use Topology Builder to
        change the Edge internal next hop setting to point to a different Front-end pool,  before you
        proceed.

<span data-ttu-id="3fa6e-159"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3fa6e-159"></div>

<span> </span>

</div>

</div>

</span></span></div>

