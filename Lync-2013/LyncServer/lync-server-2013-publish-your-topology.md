---
title: 'Lync Server 2013: Veröffentlichen der Topologie'
description: 'Lync Server 2013: Veröffentlichen Ihrer Topologie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish your topology
ms:assetid: bfed3829-7a54-4b5c-a7cb-28871acd35e7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412935(v=OCS.15)
ms:contentKeyID: 48185287
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f4d27d2d3644eb1f174e2f3fab47197f2c122a97
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394551"
---
# <a name="publish-your-topology-in-lync-server-2013"></a><span data-ttu-id="23f0d-103">Veröffentlichen der Topologie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="23f0d-103">Publish your topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="23f0d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="23f0d-104">

<span> </span></span></span>

<span data-ttu-id="23f0d-105">_**Letztes Änderungsdatum des Themas:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="23f0d-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="23f0d-106">Jedes Mal, wenn Sie die Topologie mithilfe des Topologie-Generators erstellen, müssen Sie die Topologie in einer Datenbank im zentralen Verwaltungsspeicher veröffentlichen, damit die Daten für die Bereitstellung von lync Server 2013 verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="23f0d-106">Each time you use Topology Builder to build your topology, you must publish the topology to a database in the Central Management store so that the data can be used to deploy Lync Server 2013.</span></span> <span data-ttu-id="23f0d-107">Gehen Sie wie folgt vor, um Ihre Topologie zu veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="23f0d-107">Use the following procedure to publish your topology.</span></span>

<div>

## <a name="to-publish-the-topology"></a><span data-ttu-id="23f0d-108">So veröffentlichen Sie die Topologie</span><span class="sxs-lookup"><span data-stu-id="23f0d-108">To publish the topology</span></span>

1.  <span data-ttu-id="23f0d-109">Starten Sie den Topologie-Generator: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server Topology Builder**.</span><span class="sxs-lookup"><span data-stu-id="23f0d-109">Start Topology Builder: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Topology Builder**.</span></span>

2.  <span data-ttu-id="23f0d-110">Klicken Sie im Topologie-Generator in der Konsolenstruktur mit der rechten Maustaste auf **lync 2013**, und klicken Sie dann auf **Topologie veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="23f0d-110">In Topology Builder, in the console tree, right-click **Lync 2013**, and then click **Publish Topology**.</span></span>

3.  <span data-ttu-id="23f0d-111">Klicken Sie auf der Seite **Willkommen** des Assistenten auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="23f0d-111">On the **Welcome** page of the wizard, click **Next**.</span></span>

4.  <span data-ttu-id="23f0d-112">Klicken Sie auf der Seite " **Topologie-Generator** " auf " **weiter**".</span><span class="sxs-lookup"><span data-stu-id="23f0d-112">On the **Topology Builder found a CMS store** page, click **Next**.</span></span>

5.  <span data-ttu-id="23f0d-113">Klicken Sie auf der Seite **Weitere Datenbanken erstellen** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="23f0d-113">On the **Create other databases** page, click **Next**.</span></span>

6.  <span data-ttu-id="23f0d-114">Wenn der Status angibt, dass die Daten Bank Erstellung erfolgreich war, gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="23f0d-114">When the status indicates that database creation succeeded, do the following:</span></span>
    
      - <span data-ttu-id="23f0d-115">Klicken Sie zum Anzeigen des Protokolls auf **Protokoll anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="23f0d-115">To view the log, click **View log**.</span></span>
    
      - <span data-ttu-id="23f0d-116">Klicken Sie auf **Fertig stellen**, um den Assistenten zu schließen.</span><span class="sxs-lookup"><span data-stu-id="23f0d-116">To close the wizard, click **Finish**.</span></span>
        
        <div>
        

        > [!IMPORTANT]  
        > <span data-ttu-id="23f0d-117">Wenn es sich um eine neue Installation eines Edge-Servers oder eines Edge-Pools handelt, müssen Sie die Edgeserver-Konfiguration von einem vorhandenen Front-End-Server, Front-End-Pool oder Standard Edition-Server exportieren.</span><span class="sxs-lookup"><span data-stu-id="23f0d-117">If this is a new installation of an Edge Server or Edge pool, you must export the Edge Server configuration from an existing Front End Server, Front End pool, or Standard Edition server.</span></span> <span data-ttu-id="23f0d-118">Informationen zum Exportieren der Konfiguration finden Sie unter <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">Exportieren Ihrer lync Server 2013-Topologie und Kopieren der Konfiguration auf externe Medien für die Edge-Installation</A>.</span><span class="sxs-lookup"><span data-stu-id="23f0d-118">To export the configuration, see <A href="lync-server-2013-export-your-topology-and-copy-it-to-external-media-for-edge-installation.md">Export your Lync Server 2013 topology and copy it to external media for edge installation</A>.</span></span> <span data-ttu-id="23f0d-119">Sie importieren die Konfigurationsdatei aus der externen Medien-oder Netzwerkfreigabe während der Setup-und Bereitstellungsphase der Edgeserver über den lync Server-Bereitstellungs-Assistenten.</span><span class="sxs-lookup"><span data-stu-id="23f0d-119">You will import the configuration file from the external media or network share during the setup and deployment phase of the Edge Servers through the Lync Server Deployment Wizard.</span></span><BR><span data-ttu-id="23f0d-120">Sobald die Edgeserver in Betrieb sind und die lokale Configuration Management Store-Datenbank mit der internen Bereitstellung repliziert wird, werden nachfolgende Updates der lync Server 2013-Konfiguration veröffentlicht und auf die Edgeserver repliziert.</span><span class="sxs-lookup"><span data-stu-id="23f0d-120">Once the Edge Servers are operational and the local configuration management store database is replicating with the internal deployment, subsequent updates to the Lync Server 2013 configuration will be published and replicated to the Edge Servers.</span></span>

        
        <span data-ttu-id="23f0d-121"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="23f0d-121"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

