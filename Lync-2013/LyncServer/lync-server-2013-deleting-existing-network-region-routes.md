---
title: 'Lync Server 2013: Löschen vorhandener Netzwerkbereichs Routen'
description: 'Lync Server 2013: Löschen vorhandener Netzwerkbereichs Routen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting existing network region routes
ms:assetid: 6256ff80-5f1e-48b4-928b-24aeb3c1a0e7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688074(v=OCS.15)
ms:contentKeyID: 49733669
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c2501dc3f4ed88a56e9f591e3af11a673046280a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430336"
---
# <a name="deleting-existing-network-region-routes-in-lync-server-2013"></a><span data-ttu-id="dea40-103">Löschen vorhandener Netzwerkbereichs Routen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dea40-103">Deleting existing network region routes in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dea40-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dea40-104">

<span> </span></span></span>

<span data-ttu-id="dea40-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="dea40-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="dea40-106">Jede Region innerhalb einer Anruf Steuerungskonfiguration muss über eine Möglichkeit verfügen, auf jede andere Region zuzugreifen.</span><span class="sxs-lookup"><span data-stu-id="dea40-106">Every region within a call admission control (CAC) configuration must have some way to access every other region.</span></span> <span data-ttu-id="dea40-107">Während die Region Links die Bandbreiteneinschränkungen für die Verbindungen zwischen Regionen festlegen und auch die physischen Links darstellen, bestimmt eine Route, welchen verknüpften Pfad die Verbindung von einem Bereich zu einer anderen durchlaufen wird.</span><span class="sxs-lookup"><span data-stu-id="dea40-107">While region links set bandwidth limitations on the connections between regions and also represent the physical links, a route determines which linked path the connection will traverse from one region to another.</span></span> <span data-ttu-id="dea40-108">Sie können die lync Server-Systemsteuerung verwenden, um Netzwerkbereichs Routen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="dea40-108">You can use Lync Server Control Panel to configure network region routes.</span></span> <span data-ttu-id="dea40-109">In der lync Server-Systemsteuerung können Sie eine Netzwerk Regions Route erstellen, ändern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="dea40-109">From Lync Server Control Panel, you can create, modify, or delete a network region route.</span></span> <span data-ttu-id="dea40-110">Verwenden Sie dieses Thema, um vorhandene Netzwerkbereichs Routen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="dea40-110">Use this topic to delete existing network region routes.</span></span> <span data-ttu-id="dea40-111">Details zum Erstellen oder Ändern von Netzwerkbereichs Routen finden Sie unter [erstellen oder Ändern von Netzwerkbereichs Routen in lync Server 2013](lync-server-2013-creating-or-modifying-network-region-routes.md).</span><span class="sxs-lookup"><span data-stu-id="dea40-111">For details about creating or modifying network region routes, see [Creating or modifying network region routes in Lync Server 2013](lync-server-2013-creating-or-modifying-network-region-routes.md).</span></span>

<div>

## <a name="to-delete-a-network-region-route"></a><span data-ttu-id="dea40-112">So löschen Sie eine Route des Netzwerkbereichs</span><span class="sxs-lookup"><span data-stu-id="dea40-112">To delete a network region route</span></span>

1.  <span data-ttu-id="dea40-113">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="dea40-113">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="dea40-114">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="dea40-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="dea40-115">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="dea40-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="dea40-116">Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration** und dann auf **Regions Route**.</span><span class="sxs-lookup"><span data-stu-id="dea40-116">In the left navigation bar, click **Network Configuration** and then click **Region Route**.</span></span>

4.  <span data-ttu-id="dea40-117">Klicken Sie auf der Seite **Region Route** auf die Route, die Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="dea40-117">On the **Region Route** page, click the region route that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="dea40-118">Sie können mehr als eine Regions Route gleichzeitig löschen.</span><span class="sxs-lookup"><span data-stu-id="dea40-118">You can delete more than one region route at a time.</span></span> <span data-ttu-id="dea40-119">Drücken Sie dazu STRG, und wählen Sie mehrere Bereichs Routen aus, während Sie die STRG-Taste gedrückt halten.</span><span class="sxs-lookup"><span data-stu-id="dea40-119">To do this, press CTRL and select multiple region routes while holding down the CTRL key.</span></span> <span data-ttu-id="dea40-120">Wenn Sie alle Regions Routen auswählen möchten, klicken Sie im Menü <STRONG>Bearbeiten</STRONG> auf <STRONG>Alle auswählen</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="dea40-120">Or, to select all region routes, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="dea40-121">Klicken Sie im Menü **Bearbeiten** auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="dea40-121">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="dea40-122">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="dea40-122">Click **OK**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="dea40-123">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dea40-123">See Also</span></span>


[<span data-ttu-id="dea40-124">Erstellen oder Ändern von Netzwerkbereichs Routen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dea40-124">Creating or modifying network region routes in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-region-routes.md)  


<span data-ttu-id="dea40-125">[Konfigurieren einer Netzwerkregionenroute](https://technet.microsoft.com/library/gg133706\(v=ocs.15\))</span><span class="sxs-lookup"><span data-stu-id="dea40-125">[Configure a Network Region Route](https://technet.microsoft.com/library/gg133706\(v=ocs.15\))</span></span>  


[<span data-ttu-id="dea40-126">New-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="dea40-126">New-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkInterRegionRoute)  
[<span data-ttu-id="dea40-127">Set-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="dea40-127">Set-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkInterRegionRoute)  
[<span data-ttu-id="dea40-128">Remove-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="dea40-128">Remove-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkInterRegionRoute)  
[<span data-ttu-id="dea40-129">Get-CsNetworkInterRegionRoute</span><span class="sxs-lookup"><span data-stu-id="dea40-129">Get-CsNetworkInterRegionRoute</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkInterRegionRoute)  
  

<span data-ttu-id="dea40-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dea40-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

