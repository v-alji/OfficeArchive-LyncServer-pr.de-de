---
title: 'Lync Server 2013: Konfigurieren von Netzwerk Regions Verknüpfungen'
description: 'Lync Server 2013: Konfigurieren von Netzwerk Regions Verknüpfungen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring network region links
ms:assetid: 952bc93e-e6aa-4539-85c7-2b15f14eb382
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182551(v=OCS.15)
ms:contentKeyID: 48184829
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b92593f3b8fcd5fe3307a9c193ed7cddcf6dfce0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432926"
---
# <a name="configuring-network-region-links-in-lync-server-2013"></a><span data-ttu-id="acaf5-103">Konfigurieren von Netzwerkbereichs Links in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="acaf5-103">Configuring network region links in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="acaf5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="acaf5-104">

<span> </span></span></span>

<span data-ttu-id="acaf5-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="acaf5-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="acaf5-106">Sie können Verknüpfungen zwischen zwei netzwerkregionen als Teil der Anrufsteuerung (Call Admission Control, CAC) konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="acaf5-106">You can configure links between two network regions as part of call admission control (CAC).</span></span> <span data-ttu-id="acaf5-107">Regionen in einem Netzwerk sind über die physische WAN-Konnektivität (Wide Area Network) verbunden.</span><span class="sxs-lookup"><span data-stu-id="acaf5-107">Regions within a network are linked through physical wide area network (WAN) connectivity.</span></span> <span data-ttu-id="acaf5-108">Sie können die lync Server-Systemsteuerung verwenden, um eine Verknüpfung zwischen zwei netzwerkregionen zu definieren und die Bandbreiteneinschränkungen für Audio-und Videoverbindungen zwischen diesen Regionen festzulegen.</span><span class="sxs-lookup"><span data-stu-id="acaf5-108">You can use the Lync Server Control Panel to define a link between two network regions and set the bandwidth limitations on audio and video connections between these regions.</span></span> <span data-ttu-id="acaf5-109">Details zum Löschen einer vorhandenen Netzwerk Regions Verknüpfung finden Sie unter [Löschen von Netzwerkbereichs Links in lync Server 2013](lync-server-2013-deleting-network-region-links.md).</span><span class="sxs-lookup"><span data-stu-id="acaf5-109">For details about deleting an existing network region link, see [Deleting network region links in Lync Server 2013](lync-server-2013-deleting-network-region-links.md).</span></span>

<div>

## <a name="to-create-a-network-region-link"></a><span data-ttu-id="acaf5-110">So erstellen Sie eine Netzwerk Regions Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="acaf5-110">To create a network region link</span></span>

1.  <span data-ttu-id="acaf5-111">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="acaf5-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="acaf5-112">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="acaf5-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="acaf5-113">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="acaf5-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="acaf5-114">Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration** und dann auf **Regions Link**.</span><span class="sxs-lookup"><span data-stu-id="acaf5-114">In the left navigation bar, click **Network Configuration** and then click **Region Link**.</span></span>

4.  <span data-ttu-id="acaf5-115">Klicken Sie auf der Seite **Regions Link** auf **neu**.</span><span class="sxs-lookup"><span data-stu-id="acaf5-115">On the **Region Link** page, click **New**.</span></span>

5.  <span data-ttu-id="acaf5-116">Geben Sie im Feld **neuer Bereich** einen Wert in das Feld **Name** ein.</span><span class="sxs-lookup"><span data-stu-id="acaf5-116">In **New Region Link**, type a value in the **Name** field.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="acaf5-117">Dieser Wert muss innerhalb ihrer lync Server 2013-Bereitstellung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="acaf5-117">This value must be unique within your Lync Server 2013 deployment.</span></span>

    
    </div>

6.  <span data-ttu-id="acaf5-118">Wählen Sie in der Dropdownliste **netzwerkregion \# 1** einen der beiden zu verknüpfende Regionen aus.</span><span class="sxs-lookup"><span data-stu-id="acaf5-118">From the **Network region \#1** drop-down list, select one of the two regions to be linked.</span></span>

7.  <span data-ttu-id="acaf5-119">Wählen Sie in der Dropdownliste **netzwerkregion \# 2** die andere Region aus, die verknüpft werden soll.</span><span class="sxs-lookup"><span data-stu-id="acaf5-119">From the **Network region \#2** drop-down list, select the other region to be linked.</span></span> <span data-ttu-id="acaf5-120">Diese Region muss sich von der für netzwerkregion 1 ausgewählten Region unterscheiden \# .</span><span class="sxs-lookup"><span data-stu-id="acaf5-120">This region must be different from the region selected for Network region \#1.</span></span>

8.  <span data-ttu-id="acaf5-121">Optional Wenn Sie Bandbreiteneinschränkungen für Audio-oder Videoanrufe zwischen diesen Regionen festlegen möchten, wählen Sie in der Dropdownliste **bandbreitenrichtlinie** ein Profil für Bandbreitenrichtlinien aus.</span><span class="sxs-lookup"><span data-stu-id="acaf5-121">(Optional) If you want to place bandwidth limitations on audio or video calls between these regions, select a bandwidth policy profile from the **Bandwidth policy** drop-down list.</span></span>

9.  <span data-ttu-id="acaf5-122">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="acaf5-122">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-a-network-region-link"></a><span data-ttu-id="acaf5-123">So ändern Sie eine Netzwerk Regions Verknüpfung</span><span class="sxs-lookup"><span data-stu-id="acaf5-123">To modify a network region link</span></span>

1.  <span data-ttu-id="acaf5-124">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="acaf5-124">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="acaf5-125">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="acaf5-125">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="acaf5-126">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="acaf5-126">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="acaf5-127">Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration** und dann auf **Regions Link**.</span><span class="sxs-lookup"><span data-stu-id="acaf5-127">In the left navigation bar, click **Network Configuration** and then click **Region Link**.</span></span>

4.  <span data-ttu-id="acaf5-128">Klicken Sie auf der Seite **Regions Link** auf den zu ändernden Bereichs Link.</span><span class="sxs-lookup"><span data-stu-id="acaf5-128">On the **Region Link** page, click the region link that you want to modify.</span></span>

5.  <span data-ttu-id="acaf5-129">Klicken Sie im Menü **Bearbeiten** auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="acaf5-129">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="acaf5-130">Im **Link "Region bearbeiten**" können Sie die verknüpften Regionen oder das bandbreitenrichtlinienprofil für diesen Link ändern.</span><span class="sxs-lookup"><span data-stu-id="acaf5-130">In **Edit Region Link**, you can modify the regions that are linked or the bandwidth policy profile for this link.</span></span>

7.  <span data-ttu-id="acaf5-131">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="acaf5-131">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="acaf5-132">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="acaf5-132">See Also</span></span>


[<span data-ttu-id="acaf5-133">Löschen von Netzwerkbereichs Links in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="acaf5-133">Deleting network region links in Lync Server 2013</span></span>](lync-server-2013-deleting-network-region-links.md)  


[<span data-ttu-id="acaf5-134">New-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="acaf5-134">New-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegionLink)  
[<span data-ttu-id="acaf5-135">Set-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="acaf5-135">Set-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkRegionLink)  
[<span data-ttu-id="acaf5-136">Remove-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="acaf5-136">Remove-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkRegionLink)  
[<span data-ttu-id="acaf5-137">Get-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="acaf5-137">Get-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink)  
  

<span data-ttu-id="acaf5-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="acaf5-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
