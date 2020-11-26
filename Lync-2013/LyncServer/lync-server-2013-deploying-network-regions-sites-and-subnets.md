---
title: 'Lync Server 2013: Bereitstellen von netzwerkregionen,-Websites und-Subnetzen'
description: 'Lync Server 2013: Bereitstellen von netzwerkregionen,-Websites und-Subnetzen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying network regions, sites, and subnets
ms:assetid: c4b75601-3538-4d07-8d23-1ad90459ae48
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994067(v=OCS.15)
ms:contentKeyID: 51803978
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f1c4c08cd9b78b1439000cdb4a7bbe3ffc2f99d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429846"
---
# <a name="deploying-network-regions-sites-and-subnets-in-lync-server-2013"></a><span data-ttu-id="f9ec1-103">Bereitstellen von netzwerkregionen,-Websites und-Subnetzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9ec1-103">Deploying network regions, sites, and subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f9ec1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f9ec1-104">

<span> </span></span></span>

<span data-ttu-id="f9ec1-105">_**Letztes Änderungsdatum des Themas:** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="f9ec1-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="f9ec1-106">Nachdem Enterprise-VoIP bereitgestellt wurde, müssen Sie Folgendes konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="f9ec1-106">Once Enterprise Voice is deployed, you need to configure:</span></span>

  - <span data-ttu-id="f9ec1-107">Netzwerkregionen</span><span class="sxs-lookup"><span data-stu-id="f9ec1-107">Network regions</span></span>

  - <span data-ttu-id="f9ec1-108">Netzwerk Websites</span><span class="sxs-lookup"><span data-stu-id="f9ec1-108">Network sites</span></span>

  - <span data-ttu-id="f9ec1-109">Netzwerk-Subnetze</span><span class="sxs-lookup"><span data-stu-id="f9ec1-109">Network subnets</span></span>

<div>

## <a name="define-network-regions"></a><span data-ttu-id="f9ec1-110">Definieren von netzwerkregionen</span><span class="sxs-lookup"><span data-stu-id="f9ec1-110">Define Network Regions</span></span>

<span data-ttu-id="f9ec1-111">Verwenden Sie den lync Server Windows PowerShell-Befehl, die CsNetworkRegion-oder lync Server-Systemsteuerung, um netzwerkregionen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="f9ec1-111">Use the Lync Server Windows PowerShell command, New-CsNetworkRegion, or Lync Server Control Panel to define network regions.</span></span>

    New-CsNetworkRegion -NetworkRegionID <region ID> -CentralSite <site ID>

<span data-ttu-id="f9ec1-112">Weitere Informationen finden Sie unter [New-CsNetworkRegion](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion).</span><span class="sxs-lookup"><span data-stu-id="f9ec1-112">For more information, see [New-CsNetworkRegion](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion).</span></span>

<span data-ttu-id="f9ec1-113">In diesem Beispiel wird mit dem folgenden Windows PowerShell-Befehl die in diesem Szenario definierte netzwerkregion, Region 1 (Indien), veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="f9ec1-113">For this example, the following Windows PowerShell command illustrates the network region, region 1 (India), defined in this scenario.</span></span>

    New-CsNetworkRegion -NetworkRegionID "India" -CentralSite "India Central Site"

<div>


</div>

</div>

<div>

## <a name="define-network-sites"></a><span data-ttu-id="f9ec1-114">Definieren von Netzwerk Websites</span><span class="sxs-lookup"><span data-stu-id="f9ec1-114">Define Network Sites</span></span>

<span data-ttu-id="f9ec1-115">Verwenden Sie den lync Server Windows PowerShell-Befehl, New-CsNetworkSite oder die lync Server-Systemsteuerung, um Netzwerk Websites zu definieren.</span><span class="sxs-lookup"><span data-stu-id="f9ec1-115">Use the Lync Server Windows PowerShell command, New-CsNetworkSite, or the Lync Server Control Panel to define network sites.</span></span>

    New-CsNetworkSite -NetworkSiteID <site ID> -NetworkRegionID <region ID>

<span data-ttu-id="f9ec1-116">Weitere Informationen finden Sie unter [New-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite).</span><span class="sxs-lookup"><span data-stu-id="f9ec1-116">For more information, see [New-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSite).</span></span>

<span data-ttu-id="f9ec1-117">In diesem Beispiel veranschaulichen die folgende Tabelle und der lync Server-Windows PowerShell-Befehl die in diesem Szenario definierten Netzwerk Websites.</span><span class="sxs-lookup"><span data-stu-id="f9ec1-117">For this example, the following table and Lync Server Windows PowerShell command illustrate the network sites defined in this scenario.</span></span> <span data-ttu-id="f9ec1-118">Nur Einstellungen, die für Location-Based Routing spezifisch sind, werden in der Tabelle zu Illustrationszwecken berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="f9ec1-118">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsNetworkSite -NetworkSiteID "Delhi" -NetworkRegionID "India"
    New-CsNetworkSite -NetworkSiteID "Hyderabad" -NetworkRegionID "India"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f9ec1-119">Website 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="f9ec1-119">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="f9ec1-120">Website 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="f9ec1-120">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9ec1-121">Website-ID</span><span class="sxs-lookup"><span data-stu-id="f9ec1-121">Site ID</span></span></p></td>
<td><p><span data-ttu-id="f9ec1-122">Website 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="f9ec1-122">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="f9ec1-123">Website 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="f9ec1-123">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9ec1-124">Regions-ID</span><span class="sxs-lookup"><span data-stu-id="f9ec1-124">Region ID</span></span></p></td>
<td><p><span data-ttu-id="f9ec1-125">Region 1 (Indien)</span><span class="sxs-lookup"><span data-stu-id="f9ec1-125">Region 1 (India)</span></span></p></td>
<td><p><span data-ttu-id="f9ec1-126">Region 1 (Indien)</span><span class="sxs-lookup"><span data-stu-id="f9ec1-126">Region 1 (India)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="define-network-subnets"></a><span data-ttu-id="f9ec1-127">Definieren von Netzwerk-Subnetzen</span><span class="sxs-lookup"><span data-stu-id="f9ec1-127">Define Network Subnets</span></span>

<span data-ttu-id="f9ec1-128">Verwenden Sie den lync Server Windows PowerShell-Befehl, New-CsNetworkSubnet oder die lync Server-Systemsteuerung, um Netzwerk-Subnetze zu definieren und Sie den Netzwerkstandorten zuzuweisen.</span><span class="sxs-lookup"><span data-stu-id="f9ec1-128">Use the Lync Server Windows PowerShell command, New-CsNetworkSubnet, or the Lync Server Control Panel to define network subnets and assign them to network sites.</span></span>

    New-CsNetworkSubnet -SubnetID <Subnet IP address> -MaskBits <Subnet bitmask> -NetworkSiteID <site ID>

<span data-ttu-id="f9ec1-129">Weitere Informationen finden Sie unter [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span><span class="sxs-lookup"><span data-stu-id="f9ec1-129">For more information, see [New-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkSubnet).</span></span>

<span data-ttu-id="f9ec1-130">In diesem Beispiel veranschaulichen die folgenden Tabellen-und Windows PowerShell-Befehle die Zuweisung von Netzwerk-Subnetzen zu den Netzwerkstandorten Delhi und Hyderabad, die in diesem Szenario definiert sind.</span><span class="sxs-lookup"><span data-stu-id="f9ec1-130">For this example, the following table and Windows PowerShell commands illustrate the assignment of network subnets to the network sites, Delhi and Hyderabad, defined in this scenario.</span></span> <span data-ttu-id="f9ec1-131">Nur Einstellungen, die für Location-Based Routing spezifisch sind, werden in der Tabelle zu Illustrationszwecken berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="f9ec1-131">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsNetworkSubnet -SubnetID "192.168.0.0" -MaskBits "24" -NetworkSiteID "Delhi"
    New-CsNetworkSubnet -SubnetID "192.168.1.0" -MaskBits "24" -NetworkSiteID "Hyderabad"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="f9ec1-132">Website 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="f9ec1-132">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="f9ec1-133">Website 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="f9ec1-133">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="f9ec1-134">Subnet-ID</span><span class="sxs-lookup"><span data-stu-id="f9ec1-134">Subnet ID</span></span></p></td>
<td><p><span data-ttu-id="f9ec1-135">192.168.0.0</span><span class="sxs-lookup"><span data-stu-id="f9ec1-135">192.168.0.0</span></span></p></td>
<td><p><span data-ttu-id="f9ec1-136">192.168.1.0</span><span class="sxs-lookup"><span data-stu-id="f9ec1-136">192.168.1.0</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="f9ec1-137">Format</span><span class="sxs-lookup"><span data-stu-id="f9ec1-137">Mask</span></span></p></td>
<td><p><span data-ttu-id="f9ec1-138">24</span><span class="sxs-lookup"><span data-stu-id="f9ec1-138">24</span></span></p></td>
<td><p><span data-ttu-id="f9ec1-139">24</span><span class="sxs-lookup"><span data-stu-id="f9ec1-139">24</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="f9ec1-140">Website-ID</span><span class="sxs-lookup"><span data-stu-id="f9ec1-140">Site ID</span></span></p></td>
<td><p><span data-ttu-id="f9ec1-141">Website 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="f9ec1-141">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="f9ec1-142">Website 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="f9ec1-142">Site 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="f9ec1-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f9ec1-143">See Also</span></span>


[<span data-ttu-id="f9ec1-144">Konfigurieren von standortbasiertem Routing in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f9ec1-144">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="f9ec1-145"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f9ec1-145"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

