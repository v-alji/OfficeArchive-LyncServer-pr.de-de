---
title: 'Lync Server 2013: Bereitstellen von Front-End-Poolpaaren für die Notfallwiederherstellung'
description: 'Lync Server 2013: Bereitstellen gekoppelter Front-End-Pools für die Notfallwiederherstellung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying paired Front End pools for disaster recovery
ms:assetid: 2f12467c-8b90-43e6-831b-a0b096427f17
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204773(v=OCS.15)
ms:contentKeyID: 48183727
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4846121f301d2bc7be1af9b58f0a0fef3f88e6d6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429828"
---
# <a name="deploying-paired-front-end-pools-for-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="0253f-103">Bereitstellen von Front-End-Poolpaaren für die Notfallwiederherstellung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0253f-103">Deploying paired Front End pools for disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0253f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0253f-104">

<span> </span></span></span>

<span data-ttu-id="0253f-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="0253f-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="0253f-106">Sie können die Disaster Recovery-Topologie von gekoppelten Front-End-Pools auf einfache Weise mithilfe von Topology Builder bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="0253f-106">You can easily deploy the disaster recovery topology of paired Front End pools using Topology Builder.</span></span>

<div>

## <a name="to-deploy-a-pair-of-front-end-pools"></a><span data-ttu-id="0253f-107">So stellen Sie ein Front-End-Poolpaar bereit</span><span class="sxs-lookup"><span data-stu-id="0253f-107">To deploy a pair of Front End pools</span></span>

1.  <span data-ttu-id="0253f-108">Wenn die Pools neu sind und noch nicht definiert sind, verwenden Sie den Topologie-Generator zum Erstellen der Pools.</span><span class="sxs-lookup"><span data-stu-id="0253f-108">If the pools are new and not yet defined, use Topology Builder to create the pools.</span></span>

2.  <span data-ttu-id="0253f-109">Klicken Sie im Topologie-Generator mit der rechten Maustaste auf einen der beiden Pools, und klicken Sie dann auf **Eigenschaften bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="0253f-109">In Topology Builder, right-click one of the two pools, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="0253f-110">Klicken Sie im linken Bereich auf **Flexibilität**, und wählen Sie dann im rechten Bereich die Option **Zugeordneter Sicherungspool** aus.</span><span class="sxs-lookup"><span data-stu-id="0253f-110">Click **Resiliency** in the left pane, and then select **Associated Backup Pool** in the right pane.</span></span>

4.  <span data-ttu-id="0253f-p101">Wählen Sie im Feld unter **Zugeordneter Sicherungspool** den Pool aus, mit dem dieser Pool ein Paar bilden soll. Zur Auswahl stehen nur vorhandene Pools, die noch nicht mit einem anderen Pool ein Paar bilden.</span><span class="sxs-lookup"><span data-stu-id="0253f-p101">In the box below **Associated Backup Pool**, select the pool that you want to pair with this pool. Only existing pools that are not already paired with another pool will be available to select from.</span></span>
    
    <span data-ttu-id="0253f-113">![36080581-DB76-497d-bf9e-f02b39574d0e](images/JJ204773.36080581-db76-497d-bf9e-f02b39574d0e(OCS.15).png "36080581-DB76-497d-bf9e-f02b39574d0e")</span><span class="sxs-lookup"><span data-stu-id="0253f-113">![36080581-db76-497d-bf9e-f02b39574d0e](images/JJ204773.36080581-db76-497d-bf9e-f02b39574d0e(OCS.15).png "36080581-db76-497d-bf9e-f02b39574d0e")</span></span>  

5.  <span data-ttu-id="0253f-114">Wählen Sie **Automatisches Failover und Failback für Sprachdienste** aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="0253f-114">Select **Automatic failover and failback for Voice**, and then click **OK**.</span></span>
    
    <span data-ttu-id="0253f-115">Wenn Sie die Details zu diesem Pool anzeigen, erscheint der zugeordnete Pool jetzt im rechten Bereich unter **Flexibilität**. </span><span class="sxs-lookup"><span data-stu-id="0253f-115">When you view the details about this pool, the associated pool now appears in the right pane under **Resiliency**.</span></span>

6.  <span data-ttu-id="0253f-116">Verwenden Sie den Topologie-Generator zum Veröffentlichen der Topologie.</span><span class="sxs-lookup"><span data-stu-id="0253f-116">Use Topology Builder to publish the topology.</span></span>

7.  <span data-ttu-id="0253f-p102">Wenn die beiden Pools noch nicht bereitgestellt wurden, führen Sie die Bereitstellung jetzt durch, um die Konfiguration abzuschließen. Die letzten beiden Schritte in diesem Verfahren können Sie überspringen.</span><span class="sxs-lookup"><span data-stu-id="0253f-p102">If the two pools were not yet deployed, deploy them now and the configuration will be complete. You can skip the final two steps in this procedure.</span></span>
    
    <span data-ttu-id="0253f-119">Wenn die Pools jedoch bereits bereitgestellt waren, bevor Sie die Paarbeziehung definiert haben, müssen Sie die beiden folgenden abschließenden Schritte ausführen.</span><span class="sxs-lookup"><span data-stu-id="0253f-119">However, if the pools were already deployed before you defined the paired relationship, you must complete the following two final steps.</span></span>

8.  <span data-ttu-id="0253f-120">Führen Sie auf jedem Front-End-Server in beiden Pools Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="0253f-120">On every Front End Server in both pools, run the following:</span></span>
    ```console
    <system drive>\Program Files\Microsoft Lync Server 2013\Deployment\Bootstrapper.exe 
    ```
    <span data-ttu-id="0253f-121">Hierdurch werden die anderen Dienste konfiguriert, die erforderlich sind, damit die Sicherung des Poolpaars korrekt funktioniert.</span><span class="sxs-lookup"><span data-stu-id="0253f-121">This configures other services required for backup pairing to work correctly.</span></span>

9.  <span data-ttu-id="0253f-122">Führen Sie an einer Eingabeaufforderung der lync Server-Verwaltungsshell die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="0253f-122">From a Lync Server Management Shell command prompt, run the following:</span></span>
    ```powershell
    Start-CsWindowsService -Name LYNCBACKUP
    ```
10. <span data-ttu-id="0253f-123">Verwenden Sie die folgenden Cmdlets, um zu erzwingen, dass die Benutzer- und Konferenzdaten beider Pools miteinander synchronisiert werden:</span><span class="sxs-lookup"><span data-stu-id="0253f-123">Force the user and conference data of both pools to be synchronized with each other, with the following cmdlets:</span></span>
    
       ```powershell
        Invoke-CsBackupServiceSync -PoolFqdn <Pool1 FQDN>
       ```
    
       ```powershell
        Invoke-CsBackupServiceSync -PoolFqdn <Pool2 FQDN>
       ```
    
    <span data-ttu-id="0253f-p103">Das Synchronisieren der Daten kann einige Zeit in Anspruch nehmen. Sie können die folgenden Cmdlets verwenden, um den Status zu überprüfen. Stellen Sie sicher, dass der Status für beide Richtungen stabil ist.</span><span class="sxs-lookup"><span data-stu-id="0253f-p103">Synchronizing the data may take some time. You can use the following cmdlets to check the status. Make sure that the status in both directions is in steady state.</span></span>
    
       ```powershell
        Get-CsBackupServiceStatus -PoolFqdn <Pool1 FQDN>
       ```
    
       ```powershell
        Get-CsBackupServiceStatus -PoolFqdn <Pool2 FQDN>
       ```

<div class="">


> [!NOTE]  
> <span data-ttu-id="0253f-127">Die Option <STRONG>Automatisches Failover und Failback für VoIP</STRONG> und die zugehörigen Zeitintervalle im Topologie-Generator gelten nur für die Features der VoIP-Resilienz, die in lync Server 2010 eingeführt wurden.</span><span class="sxs-lookup"><span data-stu-id="0253f-127">The <STRONG>Automatic failover and failback for Voice</STRONG> option and the associated time intervals in Topology Builder apply only to the voice resiliency features that were introduced in Lync Server 2010.</span></span> <span data-ttu-id="0253f-128">Wenn Sie diese Option auswählen, bedeutet dies nicht, dass das in diesem Dokument beschriebene Pool-Failover automatisch erfolgt.</span><span class="sxs-lookup"><span data-stu-id="0253f-128">Selecting this option does not imply that the pool failover discussed in this document is automatic.</span></span> <span data-ttu-id="0253f-129">Für Pool-Failover und Failback muss ein Administrator immer manuell die Failover-und Failback-Cmdlets aufrufen.</span><span class="sxs-lookup"><span data-stu-id="0253f-129">Pool failover and failback always require an administrator to manually invoke the failover and failback cmdlets, respectively.</span></span>



<span data-ttu-id="0253f-130"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0253f-130"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

