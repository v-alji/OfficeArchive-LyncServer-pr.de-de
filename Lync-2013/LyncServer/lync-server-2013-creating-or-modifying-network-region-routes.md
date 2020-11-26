---
title: 'Lync Server 2013: Erstellen oder Ändern von Netzwerkbereichs Routen'
description: 'Lync Server 2013: Erstellen oder Ändern von Netzwerkbereichs Routen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating or modifying network region routes
ms:assetid: 76993daa-76c2-4cec-8363-de8aebef0145
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg521016(v=OCS.15)
ms:contentKeyID: 48184540
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 89106c905419778776ea16341f247027d49f1195
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431428"
---
# <a name="creating-or-modifying-network-region-routes-in-lync-server-2013"></a><span data-ttu-id="943e6-103">Erstellen oder Ändern von Netzwerkbereichs Routen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="943e6-103">Creating or modifying network region routes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="943e6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="943e6-104">

<span> </span></span></span>

<span data-ttu-id="943e6-105">_**Letztes Änderungsdatum des Themas:** 2012-10-08_</span><span class="sxs-lookup"><span data-stu-id="943e6-105">_**Topic Last Modified:** 2012-10-08_</span></span>

<span data-ttu-id="943e6-106">Jede Region innerhalb einer Anruf Steuerungskonfiguration muss über eine Möglichkeit verfügen, auf jede andere Region zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="943e6-106">Every region within a call admission control (CAC) configuration must have some way to access every other region.</span></span> <span data-ttu-id="943e6-107">Während die Region Links die Bandbreiteneinschränkungen für die Verbindungen zwischen Regionen festlegen und auch die physischen Links darstellen, bestimmt eine Route, welchen verknüpften Pfad die Verbindung von einem Bereich zu einer anderen durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="943e6-107">While region links set bandwidth limitations on the connections between regions and also represent the physical links, a route determines which linked path the connection will traverse from one region to another.</span></span> <span data-ttu-id="943e6-108">Sie können die lync Server-Systemsteuerung verwenden, um Netzwerkbereichs Routen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="943e6-108">You can use Lync Server Control Panel to configure network region routes.</span></span> <span data-ttu-id="943e6-109">In der lync Server-Systemsteuerung können Sie eine Netzwerk Regions Route erstellen, ändern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="943e6-109">From Lync Server Control Panel, you can create, modify, or delete a network region route.</span></span> <span data-ttu-id="943e6-110">Verwenden Sie dieses Thema, um eine Netzwerk Regions Route zu erstellen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="943e6-110">Use this topic to create or modify a network region route.</span></span> <span data-ttu-id="943e6-111">Details zum Löschen vorhandener Netzwerkbereichs Routen finden Sie unter [Löschen vorhandener Netzwerkbereichs Routen in lync Server 2013](lync-server-2013-deleting-existing-network-region-routes.md).</span><span class="sxs-lookup"><span data-stu-id="943e6-111">For details about deleting an existing network region routes, see [Deleting existing network region routes in Lync Server 2013](lync-server-2013-deleting-existing-network-region-routes.md).</span></span>

<div>

## <a name="to-create-a-network-region-route"></a><span data-ttu-id="943e6-112">So erstellen Sie eine Netzwerk Regions Route</span><span class="sxs-lookup"><span data-stu-id="943e6-112">To create a network region route</span></span>

1.  <span data-ttu-id="943e6-113">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="943e6-113">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="943e6-114">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="943e6-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="943e6-115">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="943e6-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="943e6-116">Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration** und dann auf **Regions Route**.</span><span class="sxs-lookup"><span data-stu-id="943e6-116">In the left navigation bar, click **Network Configuration** and then click **Region Route**.</span></span>

4.  <span data-ttu-id="943e6-117">Klicken Sie auf der Seite **Region Route** auf **neu**.</span><span class="sxs-lookup"><span data-stu-id="943e6-117">On the **Region Route** page, click **New**.</span></span>

5.  <span data-ttu-id="943e6-118">Geben **Sie in das** Feld Name einen Wert in das Feld **Name** ein.</span><span class="sxs-lookup"><span data-stu-id="943e6-118">In **New Region Route**, type a value in the **Name** field.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="943e6-119">Dieser Wert muss innerhalb Ihrer Microsoft lync Server 2013-Bereitstellung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="943e6-119">This value must be unique within your Microsoft Lync Server 2013 deployment.</span></span>

    
    </div>

6.  <span data-ttu-id="943e6-120">Wählen Sie in der Dropdownliste **netzwerkregion \# 1** einen der beiden Regionen aus, die mit dieser Route verbunden werden sollen.</span><span class="sxs-lookup"><span data-stu-id="943e6-120">From the **Network region \#1** drop-down list, select one of the two regions to be connected by this route.</span></span>

7.  <span data-ttu-id="943e6-121">Wählen Sie in der Dropdownliste **netzwerkregion \# 2** den anderen Bereich für diese Route aus.</span><span class="sxs-lookup"><span data-stu-id="943e6-121">From the **Network region \#2** drop-down list, select the other region for this route.</span></span> <span data-ttu-id="943e6-122">Diese Region muss sich von der für netzwerkregion 1 ausgewählten Region unterscheiden \# .</span><span class="sxs-lookup"><span data-stu-id="943e6-122">This region must be different from the region selected for Network region \#1.</span></span>

8.  <span data-ttu-id="943e6-123">Verwenden Sie das Listenfeld **Netzwerk Gebiets Links** , um der Route Bereichs Links hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="943e6-123">Use the **Network region links** list box to add region links to the route.</span></span> <span data-ttu-id="943e6-124">Klicken Sie auf die Schaltfläche **Hinzufügen** , um die Seite **Regions Link** anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="943e6-124">Click the **Add** button to display the **Region Link** page.</span></span> <span data-ttu-id="943e6-125">Klicken Sie auf einen Regions Link, der zu dieser Route hinzugefügt werden soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="943e6-125">Click a region link to add to this route, and then click **OK**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="943e6-126">Klicken Sie weiter auf die Schaltfläche <STRONG>Hinzufügen</STRONG> , um weitere Links hinzuzufügen, oder wählen Sie einen Link aus, und klicken Sie auf <STRONG>Entfernen</STRONG> , um einen Link zu entfernen.</span><span class="sxs-lookup"><span data-stu-id="943e6-126">Continue to click the <STRONG>Add</STRONG> button to add more links, or select a link and click <STRONG>Remove</STRONG> to remove a link.</span></span>

    
    </div>

9.  <span data-ttu-id="943e6-127">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="943e6-127">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-a-network-region-route"></a><span data-ttu-id="943e6-128">So ändern Sie eine Route des Netzwerkbereichs</span><span class="sxs-lookup"><span data-stu-id="943e6-128">To modify a network region route</span></span>

1.  <span data-ttu-id="943e6-129">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="943e6-129">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="943e6-130">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="943e6-130">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="943e6-131">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="943e6-131">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="943e6-132">Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration** und dann auf **Regions Route**.</span><span class="sxs-lookup"><span data-stu-id="943e6-132">In the left navigation bar, click **Network Configuration** and then click **Region Route**.</span></span>

4.  <span data-ttu-id="943e6-133">Klicken Sie auf der Seite **Region Route** auf die Route, die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="943e6-133">On the **Region Route** page, click the region route that you want to modify.</span></span>

5.  <span data-ttu-id="943e6-134">Klicken Sie im Menü **Bearbeiten** auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="943e6-134">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="943e6-135">In der **Route "Region bearbeiten**" können Sie die Regionen ändern, die mit dieser Route verbunden sind, und die der Route zugeordneten Regions Verknüpfungen.</span><span class="sxs-lookup"><span data-stu-id="943e6-135">In **Edit Region Route**, you can modify the regions joined by this route and the region links associated with the route.</span></span>

7.  <span data-ttu-id="943e6-136">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="943e6-136">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="943e6-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="943e6-137">See Also</span></span>


[<span data-ttu-id="943e6-138">Löschen vorhandener Netzwerkbereichs Routen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="943e6-138">Deleting existing network region routes in Lync Server 2013</span></span>](lync-server-2013-deleting-existing-network-region-routes.md)  
  

<span data-ttu-id="943e6-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="943e6-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

