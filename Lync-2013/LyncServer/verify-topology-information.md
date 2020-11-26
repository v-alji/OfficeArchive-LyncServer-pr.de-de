---
title: Überprüfen von Topologieinformationen
description: Überprüfen der Topologieinformationen
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify topology information
ms:assetid: aa4c424e-f87c-4be6-8df6-a0cd193b11fc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205151(v=OCS.15)
ms:contentKeyID: 48185046
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2ed41cd95fffdca629e710dcf443631d0c74c69e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440118"
---
# <a name="verify-topology-information"></a><span data-ttu-id="ccdfc-103">Überprüfen von Topologieinformationen</span><span class="sxs-lookup"><span data-stu-id="ccdfc-103">Verify topology information</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ccdfc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ccdfc-104">

<span> </span></span></span>

<span data-ttu-id="ccdfc-105">_**Letztes Änderungsdatum des Themas:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="ccdfc-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="ccdfc-106">Der erste Schritt beim erfolgreichen Überprüfen des Seriendrucks besteht darin, die Office Communications Server 2007 R2-Topologieinformationen anzuzeigen, die Sie mit lync Server 2013 zusammengeführt haben.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-106">The first step in verifying the merge completed successfully is to view the Office Communications Server 2007 R2 topology information that you merged with Lync Server 2013.</span></span> <span data-ttu-id="ccdfc-107">Im Topologie-Generator zeigt der **BackCompatSite** -Knoten den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) jedes Office Communications Server 2007 R2-Pools und-Servers an, den Sie zusammengeführt haben.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-107">In Topology Builder, the **BackCompatSite** node displays the fully qualified domain name (FQDN) of each Office Communications Server 2007 R2 pool and server that you merged.</span></span>

<div>

## <a name="to-view-backcompatsite-in-topology-builder"></a><span data-ttu-id="ccdfc-108">So zeigen Sie BackCompatSite im Topologie-Generator an</span><span class="sxs-lookup"><span data-stu-id="ccdfc-108">To view BackCompatSite in Topology Builder</span></span>

1.  <span data-ttu-id="ccdfc-109">Öffnen Sie in Ihrer Office Communications Server 2007 R2-Umgebung das Office Communications Server 2007 R2-Verwaltungstool, und notieren Sie sich die FQDNs der Legacy Pools und-Server.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-109">In your Office Communications Server 2007 R2 environment, open the Office Communications Server 2007 R2 administrative tool and note the FQDNs of the legacy pools and servers.</span></span>

2.  <span data-ttu-id="ccdfc-110">Öffnen Sie in ihrer lync Server 2013-Umgebung den Topologie-Generator, und erweitern Sie dann den **BackCompatSite** -Knoten.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-110">In your Lync Server 2013 environment, open Topology Builder and then expand the **BackCompatSite** node.</span></span>

3.  <span data-ttu-id="ccdfc-111">Überprüfen Sie, ob die FQDNs für die Pools und Server, die Sie zusammenführen, angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-111">Verify that the FQDNs for the pools and servers that you merge are displayed.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ccdfc-112">Es werden keine Informationen in <STRONG>BackCompatSite</STRONG> für Serverrollen angezeigt, die sich auf einem Front-End-Server oder einem Standard Edition-Server befinden.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-112">You do not see any information in <STRONG>BackCompatSite</STRONG> for server roles that are collocated on a Front End Server or Standard Edition server.</span></span> <span data-ttu-id="ccdfc-113">Es werden nur Serverrollen angezeigt, die für die Interoperabilität zwischen Office Communications Server 2007 R2 und lync Server 2013 erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-113">Only server roles that are required for interoperability between Office Communications Server 2007 R2 and Lync Server 2013 are shown.</span></span>

    
    </div>

<span data-ttu-id="ccdfc-114">![Dialogfeld ' BackCompatSite '](images/JJ205243.62751c76-f018-4c6d-bb48-c61ef8974d31(OCS.15).jpg "Dialogfeld ' BackCompatSite '")</span><span class="sxs-lookup"><span data-stu-id="ccdfc-114">![Topology Builder BackCompatSite dialog box](images/JJ205243.62751c76-f018-4c6d-bb48-c61ef8974d31(OCS.15).jpg "Topology Builder BackCompatSite dialog box")</span></span>

<span data-ttu-id="ccdfc-115">Sie können auch die lync Server 2013-Systemsteuerung verwenden, um Ihre zusammengeführte Topologie anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-115">You can also use Lync Server 2013 Control Panel to view your merged topology.</span></span> <span data-ttu-id="ccdfc-116">In der lync Server 2013-Systemsteuerung können Sie jeden Server-FQDN, Pool-FQDN und Websitenamen für Ihre zusammengeführte Topologie sehen.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-116">In Lync Server 2013 Control Panel, you can see each server FQDN, pool FQDN, and site name for your merged topology.</span></span> <span data-ttu-id="ccdfc-117">Verbundene Server verfügen über den **Website** Namen **BackCompatSite**.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-117">Merged servers have a **Site** name of **BackCompatSite**.</span></span>

</div>

<div>

## <a name="to-view-the-merged-topology-in-lync-server-2013-control-panel"></a><span data-ttu-id="ccdfc-118">So zeigen Sie die zusammengeführte Topologie in der lync Server 2013-Systemsteuerung an</span><span class="sxs-lookup"><span data-stu-id="ccdfc-118">To view the merged topology in Lync Server 2013 Control Panel</span></span>

1.  <span data-ttu-id="ccdfc-119">Öffnen Sie die lync Server 2013-Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-119">Open Lync Server 2013 Control Panel.</span></span>

2.  <span data-ttu-id="ccdfc-120">Klicken Sie auf **Topologie**.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-120">Click **Topology**.</span></span>

3.  <span data-ttu-id="ccdfc-121">Überprüfen Sie auf der Registerkarte **Status** , ob die zusammengeführten Server und Pools angezeigt werden, indem Sie in der Spalte **Websites** nach **BackCompatSite** suchen.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-121">On the **Status** tab, verify that servers and pools you merged appear by looking for **BackCompatSite** in the **Site** column.</span></span>

<span data-ttu-id="ccdfc-122">![Lync Server-Systemsteuerung mit zusammengeführter Topologie](images/JJ205151.f986ddd4-2040-454d-9389-7f6154b59cc9(OCS.15).jpg "Lync Server-Systemsteuerung mit zusammengeführter Topologie")</span><span class="sxs-lookup"><span data-stu-id="ccdfc-122">![Lync Server Control Panel showing merged topology](images/JJ205151.f986ddd4-2040-454d-9389-7f6154b59cc9(OCS.15).jpg "Lync Server Control Panel showing merged topology")</span></span>

<span data-ttu-id="ccdfc-123">Wenn Sie weitere Details zu einem zusammengeführten Pool anzeigen möchten, verwenden Sie das Cmdlet **Get-CsPool** .</span><span class="sxs-lookup"><span data-stu-id="ccdfc-123">To see more detail about a merged pool, use the **Get-CsPool** cmdlet.</span></span> <span data-ttu-id="ccdfc-124">Zusätzlich zu den Informationen, die im Topologie-Generator und in der lync Server 2013-Systemsteuerung zur Verfügung stehen, zeigt dieses Cmdlet die Dienste an, die im lync Server 2013-Pool ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-124">In addition to the information that is available in Topology Builder and Lync Server 2013 Control Panel, this cmdlet displays the services that run on the Lync Server 2013 pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ccdfc-125">Wenn Sie die Topologie nach dem Ausführen des Zusammenführungs-Assistenten im Topologie-Generator veröffentlichen, werden Konferenzverzeichnisse mit lync Server 2013 zusammengeführt.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-125">When you publish the topology after running the Merge wizard in Topology Builder, conference directories are merged to Lync Server 2013.</span></span> <span data-ttu-id="ccdfc-126">Konferenzverzeichnisse können überprüft werden, indem Sie das Cmdlet " <STRONG>Get-CsConferenceDirectory</STRONG> " ausführen.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-126">Conference directories can be verified by running the <STRONG>Get-CsConferenceDirectory</STRONG> cmdlet.</span></span>



</div>

</div>

<div>

## <a name="to-view-services-on-a-merged-pool"></a><span data-ttu-id="ccdfc-127">So zeigen Sie Dienste in einem zusammengeführten Pool an</span><span class="sxs-lookup"><span data-stu-id="ccdfc-127">To view services on a merged pool</span></span>

1.  <span data-ttu-id="ccdfc-128">Öffnen Sie die lync Server 2013-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-128">Open the Lync Server 2013 Management Shell.</span></span>

2.  <span data-ttu-id="ccdfc-129">Geben Sie an der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="ccdfc-129">At the command line, type the following:</span></span>
    
        Get-CsPool [-Identity <FQDN of the pool>]
    
    <span data-ttu-id="ccdfc-130">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ccdfc-130">For example:</span></span>
    
        Get-CsPool -Identity pool02.contoso.net

</div>

<div>

## <a name="to-verify-conference-directories-merged"></a><span data-ttu-id="ccdfc-131">So überprüfen Sie die Zusammenführung von Konferenz Verzeichnissen</span><span class="sxs-lookup"><span data-stu-id="ccdfc-131">To verify conference directories merged</span></span>

1.  <span data-ttu-id="ccdfc-132">Öffnen Sie die lync Server 2013-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-132">Open the Lync Server 2013 Management Shell.</span></span>

2.  <span data-ttu-id="ccdfc-133">Geben Sie an der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="ccdfc-133">At the command line, type the following:</span></span>
    
        Get-CsConferenceDirectory

3.  <span data-ttu-id="ccdfc-134">Stellen Sie sicher, dass sich alle Konferenzverzeichnisse für den Pool oder Server, den Sie zusammenführen, jetzt in lync Server 2013 befinden.</span><span class="sxs-lookup"><span data-stu-id="ccdfc-134">Verify that all the conference directories for the pool or server you are merging are now in Lync Server 2013.</span></span>

<span data-ttu-id="ccdfc-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ccdfc-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

