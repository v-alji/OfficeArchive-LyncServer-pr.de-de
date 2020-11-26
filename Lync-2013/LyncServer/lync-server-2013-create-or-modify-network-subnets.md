---
title: 'Lync Server 2013: Erstellen oder Ändern von Netzwerk-Subnetzen'
description: 'Lync Server 2013: Erstellen oder Ändern von Netzwerk-Subnetzen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify network subnets
ms:assetid: 1ba8c4e3-fbc7-4758-88ac-d651fef17bed
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520957(v=OCS.15)
ms:contentKeyID: 48183548
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 37695707bf39b10c351a4990b132c9799406f9c4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431652"
---
# <a name="create-or-modify-network-subnets-in-lync-server-2013"></a><span data-ttu-id="5201d-103">Erstellen oder Ändern von Netzwerk-Subnetzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5201d-103">Create or modify network subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5201d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5201d-104">

<span> </span></span></span>

<span data-ttu-id="5201d-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="5201d-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="5201d-106">Ein Netzwerk-Subnetz muss einer Netzwerk Website zugeordnet sein, um den geografischen Standort des Hosts zu ermitteln, der zu diesem Subnetz gehört.</span><span class="sxs-lookup"><span data-stu-id="5201d-106">A network subnet must be associated with a network site for the purposes of determining the geographic location of the host belonging to this subnet.</span></span> <span data-ttu-id="5201d-107">Sie können die lync Server-Systemsteuerung zum Konfigurieren von Subnetzen verwenden.</span><span class="sxs-lookup"><span data-stu-id="5201d-107">You can use Lync Server Control Panel to configure subnets.</span></span> <span data-ttu-id="5201d-108">In der lync Server-Systemsteuerung können Sie ein Netzwerk-Subnetz erstellen, ändern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="5201d-108">From the Lync Server Control Panel, you can create, modify, or delete a network subnet.</span></span> <span data-ttu-id="5201d-109">Details zum Löschen von Netzwerk-Subnetzen finden Sie unter Löschen von Netzwerk-Subnetzen [in lync Server 2013](lync-server-2013-deleting-network-subnets.md).</span><span class="sxs-lookup"><span data-stu-id="5201d-109">For details about deleting network subnets, see [Deleting network subnets in Lync Server 2013](lync-server-2013-deleting-network-subnets.md).</span></span>

<span data-ttu-id="5201d-110">In den meisten Bereitstellungen von Microsoft lync Server 2013, bei denen die Anrufannahme Steuerung (Call Admission Control, CAC) implementiert ist, gibt es in der Regel eine große Anzahl von Subnetzen.</span><span class="sxs-lookup"><span data-stu-id="5201d-110">In most deployments of Microsoft Lync Server 2013 where call admission control (CAC) is implemented, there will typically be a large number of subnets.</span></span> <span data-ttu-id="5201d-111">Aus diesem Grund ist es am besten, Subnets aus der lync Server-Verwaltungsshell zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="5201d-111">Because of this, it is often best to configure subnets from the Lync Server Management Shell.</span></span> <span data-ttu-id="5201d-112">Von dort aus können Sie **New-CsNetworkSubnet** in Verbindung mit dem Windows PowerShell **-Cmdlet Import-CSV** aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5201d-112">From there you can call **New-CsNetworkSubnet** in conjunction with the Windows PowerShell cmdlet **Import-CSV**.</span></span> <span data-ttu-id="5201d-113">Wenn Sie diese Cmdlets zusammen verwenden, können Sie die subneteinstellungen aus einer CSV-Datei (Comma-Separated Values) lesen und gleichzeitig mehrere Subnetze erstellen.</span><span class="sxs-lookup"><span data-stu-id="5201d-113">By using these cmdlets together, you can read in subnet settings from a comma-separated values (.csv) file and create multiple subnets at the same time.</span></span> <span data-ttu-id="5201d-114">Beispiele zum Erstellen von Subnetzen aus einer CSV-Datei finden Sie unter [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span><span class="sxs-lookup"><span data-stu-id="5201d-114">For examples of how to create subnets from a .csv file, see [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span></span>

<div>

## <a name="to-create-a-network-subnet"></a><span data-ttu-id="5201d-115">So erstellen Sie ein Netzwerk-Subnetz</span><span class="sxs-lookup"><span data-stu-id="5201d-115">To create a network subnet</span></span>

1.  <span data-ttu-id="5201d-116">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="5201d-116">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="5201d-117">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5201d-117">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="5201d-118">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="5201d-118">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="5201d-119">Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration** und dann auf **Subnetz**.</span><span class="sxs-lookup"><span data-stu-id="5201d-119">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="5201d-120">Klicken Sie auf der Seite **Subnetz** auf **neu**.</span><span class="sxs-lookup"><span data-stu-id="5201d-120">On the **Subnet** page, click **New**.</span></span>

5.  <span data-ttu-id="5201d-121">Geben Sie im **neuen Subnetz** einen Wert in das Feld **Subnet-ID** ein.</span><span class="sxs-lookup"><span data-stu-id="5201d-121">In **New Subnet**, enter a value in the **Subnet ID** field.</span></span> <span data-ttu-id="5201d-122">Hierbei muss es sich um eine IP-Adresse (beispielsweise 174.11.12.0) handeln, die die erste Adresse im vom Subnetz definierten IP-Adressbereich sein muss.</span><span class="sxs-lookup"><span data-stu-id="5201d-122">This must be an IP address (for example, 174.11.12.0), and it must be the first address in the IP address range defined by the subnet.</span></span>

6.  <span data-ttu-id="5201d-123">Geben Sie im Feld **Maske** einen numerischen Wert von 1 bis 32 ein.</span><span class="sxs-lookup"><span data-stu-id="5201d-123">In the **Mask** field, enter a numeric value from 1 through 32.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="5201d-124">Dieser Wert ist die Bitmaske, die auf das erstellte Subnetz angewendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="5201d-124">This value is the bitmask that is to be applied to the subnet being created.</span></span>

    
    </div>

7.  <span data-ttu-id="5201d-125">Wählen Sie unter **Netzwerk Website-ID** die Website aus, zu der dieses Subnetz gehört.</span><span class="sxs-lookup"><span data-stu-id="5201d-125">In **Network site ID**, select the site to which this subnet belongs.</span></span>

8.  <span data-ttu-id="5201d-126">Optional Geben Sie im Feld **Beschreibung** einen Wert ein, um weitere Informationen zu diesem Subnetz bereitzustellen, die nicht allein durch den Namen ausgedrückt werden können.</span><span class="sxs-lookup"><span data-stu-id="5201d-126">(Optional) Type a value in the **Description** field to provide more information about this subnet that cannot be expressed by the name alone.</span></span>

9.  <span data-ttu-id="5201d-127">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="5201d-127">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-modify-a-network-subnet"></a><span data-ttu-id="5201d-128">So ändern Sie ein Netzwerk-Subnetz</span><span class="sxs-lookup"><span data-stu-id="5201d-128">To modify a network subnet</span></span>

1.  <span data-ttu-id="5201d-129">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="5201d-129">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="5201d-130">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="5201d-130">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="5201d-131">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="5201d-131">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="5201d-132">Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration** und dann auf **Subnetz**.</span><span class="sxs-lookup"><span data-stu-id="5201d-132">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="5201d-133">Klicken Sie auf der Seite **Subnetz** auf das Subnetz, das Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="5201d-133">On the **Subnet** page, click the subnet that you want to modify.</span></span>

5.  <span data-ttu-id="5201d-134">Klicken Sie im Menü **Bearbeiten** auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="5201d-134">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="5201d-135">Auf der Seite " **Subnetz bearbeiten** " können Sie die Bitmaske, die zugeordnete Netzwerk Website oder die Beschreibung ändern.</span><span class="sxs-lookup"><span data-stu-id="5201d-135">On the **Edit Subnet** page, you can modify the bitmask, associated network site, or description.</span></span> <span data-ttu-id="5201d-136">Beachten Sie beim Ändern der Bitmaske, dass die Subnetz-ID immer noch die erste Adresse im IP-Adressbereich sein muss, die vom Subnetz definiert ist.</span><span class="sxs-lookup"><span data-stu-id="5201d-136">If you modify the bitmask, keep in mind that the Subnet ID must still be the first address in the IP address range defined by the subnet.</span></span>

7.  <span data-ttu-id="5201d-137">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="5201d-137">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="5201d-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5201d-138">See Also</span></span>


[<span data-ttu-id="5201d-139">Löschen von Netzwerk-Subnetzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5201d-139">Deleting network subnets in Lync Server 2013</span></span>](lync-server-2013-deleting-network-subnets.md)  


[<span data-ttu-id="5201d-140">Informationen zu Netzwerkregionen, Standorten und Subnetzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5201d-140">About network regions, sites, and subnets in Lync Server 2013</span></span>](lync-server-2013-about-network-regions-sites-and-subnets.md)  


[<span data-ttu-id="5201d-141">New-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="5201d-141">New-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet)  
[<span data-ttu-id="5201d-142">Set-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="5201d-142">Set-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkSubnet)  
[<span data-ttu-id="5201d-143">Remove-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="5201d-143">Remove-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkSubnet)  
[<span data-ttu-id="5201d-144">Get-CsNetworkSubnet</span><span class="sxs-lookup"><span data-stu-id="5201d-144">Get-CsNetworkSubnet</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSubnet)  
  

<span data-ttu-id="5201d-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5201d-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

