---
title: 'Lync Server 2013: Ausführen eines Failovers für den Edgepool, der für den Lync Server-Partnerverbund verwendet wird'
description: 'Lync Server 2013: Failover des für den lync Server-Verbund verwendeten Edge-Pools.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing over the Edge pool used for Lync Server federation
ms:assetid: 5c9da0f2-7429-40bb-bb3c-5cc4ecb5a13d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688071(v=OCS.15)
ms:contentKeyID: 49733665
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1e7e13ccd35a653d38174f55ace9dc6637ded04
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394174"
---
# <a name="failing-over-the-edge-pool-used-for-lync-server-federation-in-lync-server-2013"></a><span data-ttu-id="8f1e4-103">Ausführen eines Failovers für den Edgepool in Lync Server 2013, der für den Lync Server-Partnerverbund verwendet wird</span><span class="sxs-lookup"><span data-stu-id="8f1e4-103">Failing over the Edge pool used for Lync Server federation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8f1e4-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8f1e4-104">

<span> </span></span></span>

<span data-ttu-id="8f1e4-105">_**Letztes Änderungsdatum des Themas:** 2012-09-17_</span><span class="sxs-lookup"><span data-stu-id="8f1e4-105">_**Topic Last Modified:** 2012-09-17_</span></span>

<span data-ttu-id="8f1e4-106">Wenn der Edge-Pool, in dem Sie den lync Server-Verbund konfiguriert haben, ausfällt, müssen Sie die Föderation so ändern, dass ein anderer Edge-Pool für den Verbund verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-106">If the Edge pool where you have Lync Server federation configured goes down, you must change federation to use a different Edge pool for federation to work.</span></span>

<div>

## <a name="failing-over-the-edge-pool-used-for-lync-server-federation"></a><span data-ttu-id="8f1e4-107">Failover des für den lync Server-Verbund verwendeten Edge-Pools</span><span class="sxs-lookup"><span data-stu-id="8f1e4-107">Failing Over the Edge Pool Used for Lync Server Federation</span></span>

1.  <span data-ttu-id="8f1e4-108">Öffnen Sie auf einem Front-End-Server den Topologie-Generator.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-108">On a Front End server, open Topology Builder.</span></span> <span data-ttu-id="8f1e4-109">Erweitern Sie **Edge-Pools**, und klicken Sie dann mit der rechten Maustaste auf den Edgeserver oder den Edgeserver-Pool, der derzeit für den Verbund konfiguriert ist.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-109">Expand **Edge pools**, then right click the Edge server or Edge server pool that is currently configured for Federation.</span></span> <span data-ttu-id="8f1e4-110">Wählen Sie **Eigenschaften bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-110">Select **Edit properties**.</span></span>

2.  <span data-ttu-id="8f1e4-111">Deaktivieren Sie in **Eigenschaften bearbeiten** unter **Allgemein** **die Option Föderation für diesen Edge-Pool aktivieren (Port 5061)**.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-111">In **Edit Properties** under **General**, clear **Enable federation for this Edge pool (Port 5061)**.</span></span> <span data-ttu-id="8f1e4-112">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-112">Click **OK**.</span></span>

3.  <span data-ttu-id="8f1e4-113">Erweitern Sie **Edge-Pools**, und klicken Sie dann mit der rechten Maustaste auf den Edge-Server oder den Edgeserver-Pool, den Sie jetzt für den Verbund verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-113">Expand **Edge pools**, then right click the Edge server or Edge server pool that you now want to use for Federation.</span></span> <span data-ttu-id="8f1e4-114">Wählen Sie **Eigenschaften bearbeiten** aus.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-114">Select **Edit properties**.</span></span>

4.  <span data-ttu-id="8f1e4-115">Wählen Sie in **Eigenschaften bearbeiten** unter **Allgemein** **die Option Föderation für diesen Edge-Pool aktivieren (Port 5061)** aus.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-115">In **Edit Properties** under **General**, select **Enable federation for this Edge pool (Port 5061)**.</span></span> <span data-ttu-id="8f1e4-116">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-116">Click **OK**.</span></span>

5.  <span data-ttu-id="8f1e4-117">Klicken Sie auf **Aktion**, wählen Sie **Topologie** aus, und wählen Sie **veröffentlichen** aus.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-117">Click **Action**, select **Topology**, select **Publish**.</span></span> <span data-ttu-id="8f1e4-118">Wenn Sie dazu aufgefordert werden, **die Topologie zu veröffentlichen**, klicken Sie auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-118">When prompted on **Publish the topology**, click **Next**.</span></span> <span data-ttu-id="8f1e4-119">Wenn der Veröffentlichungsvorgang abgeschlossen ist, klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-119">When the Publish is finished, click **Finish**.</span></span>

6.  <span data-ttu-id="8f1e4-120">Öffnen Sie auf dem Edgeserver den lync Server-Bereitstellungs-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-120">On the Edge server, open the Lync Server Deployment wizard.</span></span> <span data-ttu-id="8f1e4-121">Klicken Sie auf **lync Server System installieren oder aktualisieren** und dann auf **lync Server-Komponenten einrichten oder entfernen**.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-121">Click **Install or Update Lync Server System**, then click **Setup or Remove Lync Server Components**.</span></span> <span data-ttu-id="8f1e4-122">Klicken Sie **erneut auf Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-122">Click **Run Again**.</span></span>

7.  <span data-ttu-id="8f1e4-123">Klicken Sie bei der Installation von lync Server-Komponenten auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-123">At Setup Lync Server components, click **Next**.</span></span> <span data-ttu-id="8f1e4-124">Auf dem Zusammenfassungsbildschirm werden die Aktionen während der Ausführung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-124">The summary screen will show actions as they are executed.</span></span> <span data-ttu-id="8f1e4-125">Nachdem die Bereitstellung abgeschlossen ist, klicken Sie auf **Protokoll anzeigen** , um die verfügbaren Protokolldateien anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-125">Once the deployment is done, click **View Log** to view available log files.</span></span> <span data-ttu-id="8f1e4-126">Klicken Sie auf **Fertig stellen** , um die Bereitstellung abzuschließen.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-126">Click **Finish** to complete the deployment.</span></span>
    
    <span data-ttu-id="8f1e4-127">Wenn die Website mit dem fehlerhaften Edge-Pool Front-End-Server enthält, die noch ausgeführt werden, müssen Sie den Webkonferenzdienst und den A/V-Konferenzdienst in diesen Front-End-Pools aktualisieren, um einen Edge-Pool in einer noch ausgeführten Remotewebsite zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-127">If the site containing the failed Edge pool contains Front End Servers that are still running, you must update the Web Conferencing Service and A/V Conferencing Service on these Front End pools to use an Edge pool in a remote site that is still running.</span></span> <span data-ttu-id="8f1e4-128">Weitere Informationen finden Sie unter [Ändern des Edge-Pools, der einem Front-End-Pool in lync Server 2013 zugeordnet](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md)ist.</span><span class="sxs-lookup"><span data-stu-id="8f1e4-128">For more information, see [Changing the Edge pool associated with a Front End pool in Lync Server 2013](lync-server-2013-changing-the-edge-pool-associated-with-a-front-end-pool.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8f1e4-129">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f1e4-129">See Also</span></span>


[<span data-ttu-id="8f1e4-130">Ausführen eines Failovers für den Edgepool in Lync Server 2013, der für den XMPP-Partnerverbund verwendet wird</span><span class="sxs-lookup"><span data-stu-id="8f1e4-130">Failing over the Edge pool used for XMPP federation in Lync Server 2013</span></span>](lync-server-2013-failing-over-the-edge-pool-used-for-xmpp-federation.md)  
[<span data-ttu-id="8f1e4-131">Ausführen eines Failbacks für den Edgepool in Lync Server 2013, der für den Lync Server-Partnerverbund verwendet wird</span><span class="sxs-lookup"><span data-stu-id="8f1e4-131">Failing back the Edge pool used for Lync Server federation or XMPP federation in Lync Server 2013</span></span>](lync-server-2013-failing-back-the-edge-pool-used-for-lync-server-federation-or-xmpp-federation.md)  


[<span data-ttu-id="8f1e4-132">Notfallwiederherstellung für Edgeserver in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8f1e4-132">Edge Server disaster recovery in Lync Server 2013</span></span>](lync-server-2013-edge-server-disaster-recovery.md)  
  

<span data-ttu-id="8f1e4-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8f1e4-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

