---
title: Verbinden des Pilotpools mit Edgeservern der Vorversion
description: Verbinden Sie den Pilot Pool mit Legacy-Edgeserver.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Connect pilot pool to legacy Edge Servers
ms:assetid: c3b67220-5705-47f6-852e-415204f3626c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721875(v=OCS.15)
ms:contentKeyID: 49733808
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ede2256efabf561be6b3f99543437087cb5c3890
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394414"
---
# <a name="connect-pilot-pool-to-legacy-edge-servers"></a><span data-ttu-id="e12db-103">Verbinden des Pilotpools mit Edgeservern der Vorversion</span><span class="sxs-lookup"><span data-stu-id="e12db-103">Connect pilot pool to legacy Edge Servers</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e12db-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e12db-104">

<span> </span></span></span>

<span data-ttu-id="e12db-105">_**Letztes Änderungsdatum des Themas:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="e12db-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="e12db-106">Nach der Bereitstellung von lync Server 2013 müssen Sie eine Verbund Route für Ihre Website konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="e12db-106">After deploying Lync Server 2013, you need to configure a federation route for your site.</span></span> <span data-ttu-id="e12db-107">Um die von lync Server 2010 verwendete Föderations Route verwenden zu können, muss lync Server 2013 für die Verwendung dieser Route konfiguriert sein.</span><span class="sxs-lookup"><span data-stu-id="e12db-107">In order to use the federated route that is being used by Lync Server 2010, Lync Server 2013 must be configured to use this route.</span></span>

<span data-ttu-id="e12db-108">Damit die lync Server 2013-Website den Director und den Edgeserver der lync Server 2010-Bereitstellung verwenden kann, verwenden Sie den Topologie-Generator, um den Legacy-Edge-Pool zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="e12db-108">To enable the Lync Server 2013 site to use the Director and Edge Server of the Lync Server 2010 deployment, use Topology Builder to associate the legacy Edge pool.</span></span>

<div>

## <a name="to-associate-the-legacy-edge-pool-by-using-topology-builder"></a><span data-ttu-id="e12db-109">So ordnen Sie den Legacy-Edge-Pool mithilfe des Topologie-Generators zu</span><span class="sxs-lookup"><span data-stu-id="e12db-109">To associate the legacy Edge pool by using Topology Builder</span></span>

1.  <span data-ttu-id="e12db-110">Öffnen Sie den **Topologie-Generator**.</span><span class="sxs-lookup"><span data-stu-id="e12db-110">Open **Topology Builder**.</span></span>

2.  <span data-ttu-id="e12db-111">Wählen Sie Ihre Website aus, die sich direkt unter dem **lync-Server** Knoten befindet.</span><span class="sxs-lookup"><span data-stu-id="e12db-111">Select your site, which is directly below the **Lync Server** node.</span></span>

3.  <span data-ttu-id="e12db-112">Klicken Sie im Menü **Aktionen** auf **Eigenschaften bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="e12db-112">On the **Actions** menu, click **Edit Properties**.</span></span>

4.  <span data-ttu-id="e12db-113">Wählen Sie im linken Bereich **Föderations Route** aus.</span><span class="sxs-lookup"><span data-stu-id="e12db-113">In the left pane, select **Federation route**.</span></span>

5.  <span data-ttu-id="e12db-114">Wählen Sie unter **Website Verbund-Routenzuordnung** die Option **SIP-Verbund aktivieren** aus, und wählen Sie dann den lync Server 2010 Director oder den lync Server 2010-Edgeserver aus, wenn kein Director aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="e12db-114">Under **Site federation route assignment**, select **Enable SIP federation**, and then select the Lync Server 2010 Director, or the Lync Server 2010 Edge Server if no Director is listed.</span></span>
    
    <span data-ttu-id="e12db-115">![Eigenschaften bearbeiten, Seite "Verbund Route"](images/JJ721875.5f1d04c3-c724-426d-b27d-3fe89c6c5cfb(OCS.15).jpg "Eigenschaften bearbeiten, Seite "Verbund Route"")</span><span class="sxs-lookup"><span data-stu-id="e12db-115">![Edit Properties, Federation route page](images/JJ721875.5f1d04c3-c724-426d-b27d-3fe89c6c5cfb(OCS.15).jpg "Edit Properties, Federation route page")</span></span>  

6.  <span data-ttu-id="e12db-116">Klicken Sie auf **OK** , um die Seite **Eigenschaften bearbeiten** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e12db-116">Click **OK** to close the **Edit Properties** page.</span></span>

7.  <span data-ttu-id="e12db-117">Navigieren Sie im Topologie-Generator unter dem lync Server 2013-Knoten zu den Front-End-Pools **Standard Edition Server** oder **Enterprise Edition**, klicken Sie mit der rechten Maustaste auf den Pool, und klicken Sie dann auf **Eigenschaften bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="e12db-117">In Topology Builder, under the Lync Server 2013 node, navigate to the **Standard Edition server** or **Enterprise Edition Front End pools**, right-click the pool, and then click **Edit Properties**.</span></span>

8.  <span data-ttu-id="e12db-118">Aktivieren Sie unter **Zuordnungen** das Kontrollkästchen neben **Edge-Pool zuordnen (für Medienkomponenten)**.</span><span class="sxs-lookup"><span data-stu-id="e12db-118">Under **Associations**, select the check box next to **Associate Edge pool (for media components)**.</span></span>

9.  <span data-ttu-id="e12db-119">Wählen Sie in der Liste den Legacy-Edgeserver aus.</span><span class="sxs-lookup"><span data-stu-id="e12db-119">From the list, select the legacy Edge Server.</span></span>
    
    <span data-ttu-id="e12db-120">![Dialogfeld "Eigenschaften bearbeiten", "Legacy Edge" auswählen](images/JJ721875.feae8156-540e-4804-bb0a-2b5736ec2900(OCS.15).jpg "Dialogfeld "Eigenschaften bearbeiten", "Legacy Edge" auswählen")</span><span class="sxs-lookup"><span data-stu-id="e12db-120">![Edit Properties dialog, selecting the legacy Edge](images/JJ721875.feae8156-540e-4804-bb0a-2b5736ec2900(OCS.15).jpg "Edit Properties dialog, selecting the legacy Edge")</span></span>  

10. <span data-ttu-id="e12db-121">Klicken Sie auf **OK** , um die Seite **Eigenschaften bearbeiten** zu schließen.</span><span class="sxs-lookup"><span data-stu-id="e12db-121">Click **OK** to close the **Edit Properties** page.</span></span>

11. <span data-ttu-id="e12db-122">Wählen Sie im **Topologie-Generator** den obersten Knoten, **lync Server**, aus.</span><span class="sxs-lookup"><span data-stu-id="e12db-122">In **Topology Builder**, select the top-most node, **Lync Server**.</span></span>

12. <span data-ttu-id="e12db-123">Klicken Sie im Menü **Aktion** auf **Topologie veröffentlichen**, und klicken Sie dann auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="e12db-123">From the **Action** menu, click **Publish Topology**, and then click **Next**.</span></span>

13. <span data-ttu-id="e12db-124">Klicken Sie nach Abschluss des **Veröffentlichungs-Assistenten** auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="e12db-124">When the **Publishing wizard** completes, click **Finish**.</span></span>

<span data-ttu-id="e12db-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e12db-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

