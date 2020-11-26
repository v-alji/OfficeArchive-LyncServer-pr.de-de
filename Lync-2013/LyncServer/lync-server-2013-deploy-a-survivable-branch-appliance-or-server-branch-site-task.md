---
title: Bereitstellen einer Survivable Branch Appliance oder eines Survivable Branch Servers – Aufgaben am Zweigstellenstandort
description: Bereitstelleneiner überlebensfähigen Branch Appliance-oder Server Verzweigungs Website Aufgabe
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploy a Survivable Branch Appliance or Server - branch site task
ms:assetid: 7989ba29-0419-46dd-892c-4ad3238afd56
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398599(v=OCS.15)
ms:contentKeyID: 48184586
ms.date: 10/29/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b84f603f185bd507111d4767a22e9009fc0e8b3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430252"
---
# <a name="deploy-a-survivable-branch-appliance-or-server-with-lync-server-2013---branch-site-task"></a><span data-ttu-id="b7a3b-103">Bereitstellen einer Survivable Branch Appliance oder eines Survivable Branch Servers mit Lync Server 2013 – Aufgaben am Zweigstellenstandort</span><span class="sxs-lookup"><span data-stu-id="b7a3b-103">Deploy a Survivable Branch Appliance or Server with Lync Server 2013 - branch site task</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b7a3b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b7a3b-104">

<span> </span></span></span>

<span data-ttu-id="b7a3b-105">_**Letztes Änderungsdatum des Themas:** 2014-10-28_</span><span class="sxs-lookup"><span data-stu-id="b7a3b-105">_**Topic Last Modified:** 2014-10-28_</span></span>

<span data-ttu-id="b7a3b-106">Führen Sie eines der beiden in diesem Thema beschriebenen Verfahren auf der Zweigstelle aus, nachdem Sie die Aufgaben beim [Bereitstelleneiner Survivable Branch-Appliance oder eines Servers mit lync Server 2013-Central-Websiteaufgaben](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md)erfolgreich abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="b7a3b-106">Perform one of the two procedures described in this topic at the branch site, after successfully completing the tasks in [Deploying a Survivable Branch Appliance or Server with Lync Server 2013 - central site tasks](lync-server-2013-deploying-a-survivable-branch-appliance-or-server-central-site-tasks.md).</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="b7a3b-107">Um diese Schritte ausführen zu können, müssen Sie ein Mitglied der RTCUniversalSBATechnicians-Gruppe sein.</span><span class="sxs-lookup"><span data-stu-id="b7a3b-107">To perform this procedure, you must be a member of the RTCUniversalSBATechnicians group.</span></span>



</div>

<div>

## <a name="to-deploy-the-survivable-branch-appliance"></a><span data-ttu-id="b7a3b-108">So stellen Sie die Survivable Branch-Appliance bereit</span><span class="sxs-lookup"><span data-stu-id="b7a3b-108">To deploy the Survivable Branch Appliance</span></span>

  - <span data-ttu-id="b7a3b-109">Die überlebensfähige Branch Appliance-Bereitstellung wird über eine Web-Benutzeroberfläche (User Interface, UI) vom Hersteller der Survivable Branch Appliance aktiviert.</span><span class="sxs-lookup"><span data-stu-id="b7a3b-109">Survivable Branch Appliance deployment is enabled by the Survivable Branch Appliance vendor through a web user interface (UI).</span></span> <span data-ttu-id="b7a3b-110">Informationen zum Bereitstellen der Survivable Branch-Appliance finden Sie in der Dokumentation Ihres Überlebenden Branch Appliance-Anbieters.</span><span class="sxs-lookup"><span data-stu-id="b7a3b-110">For information about deploying the Survivable Branch Appliance, see your Survivable Branch Appliance vendor documentation.</span></span>

</div>

<div>

## <a name="to-deploy-the-survivable-branch-server"></a><span data-ttu-id="b7a3b-111">So stellen Sie den Überlebenden Verzweigungs Server bereit</span><span class="sxs-lookup"><span data-stu-id="b7a3b-111">To deploy the Survivable Branch Server</span></span>

  - <span data-ttu-id="b7a3b-112">Installieren Sie lync Server 2013 auf einem Computer unter Windows Server 2008 R2, Windows Server 2012 oder Windows Server 2012 R2, genauso wie Sie eine andere lync Server 2013-Serverrolle installieren würden.</span><span class="sxs-lookup"><span data-stu-id="b7a3b-112">Install Lync Server 2013 on a computer running Windows Server 2008 R2, Windows Server 2012, or Windows Server 2012 R2, just as you would install any other Lync Server 2013 server role.</span></span>
    
    <div>
    

    > [!NOTE]
    > <span data-ttu-id="b7a3b-113">Informationen zum Installieren von lync Server finden Sie unter <A href="lync-server-2013-deploying-lync-server.md">Bereitstellen von lync Server 2013</A> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="b7a3b-113">For information about installing Lync Server, see <A href="lync-server-2013-deploying-lync-server.md">Deploying Lync Server 2013</A> in the Deployment documentation.</span></span>

    
    </div>

<span data-ttu-id="b7a3b-114">**Nächster Schritt**: [Konfigurieren von Benutzern für die Stabilität des Zweigstellen Standorts in lync Server 2013](lync-server-2013-configuring-users-for-branch-site-resiliency.md)</span><span class="sxs-lookup"><span data-stu-id="b7a3b-114">**Next step**: [Configuring users for branch site resiliency in Lync Server 2013](lync-server-2013-configuring-users-for-branch-site-resiliency.md)</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="b7a3b-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b7a3b-115">See Also</span></span>


[<span data-ttu-id="b7a3b-116">Anhang A: Verwenden von Cmdlets zur Bereitstellung einer Survivable Branch Appliance in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b7a3b-116">Appendix A: Using cmdlets to deploy a Survivable Branch Appliance in Lync Server 2013</span></span>](lync-server-2013-appendix-a-using-cmdlets-to-deploy-a-survivable-branch-appliance.md)  
  

<span data-ttu-id="b7a3b-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b7a3b-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

