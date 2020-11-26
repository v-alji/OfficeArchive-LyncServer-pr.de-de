---
title: 'Lync Server 2013: Anzeigen von Netzwerk-Subnetz-Informationen'
description: 'Lync Server 2013: Anzeigen von Netzwerk-Subnetz-Informationen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network subnet information
ms:assetid: 46f165f2-efe3-4cc1-9fee-a78b7f2ed41e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688044(v=OCS.15)
ms:contentKeyID: 49733636
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 313135c43318817391d54f2fa3e73dd318f7a11f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438855"
---
# <a name="viewing-network-subnet-information-in-lync-server-2013"></a><span data-ttu-id="ad91b-103">Anzeigen von Netzwerk-Subnetz-Informationen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ad91b-103">Viewing network subnet information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ad91b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ad91b-104">

<span> </span></span></span>

<span data-ttu-id="ad91b-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="ad91b-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="ad91b-106">Sie können das folgende Verfahren verwenden, um ein Netzwerk-Subnetz anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="ad91b-106">You can use the following procedure to view a network subnet.</span></span> <span data-ttu-id="ad91b-107">In der lync Server-Systemsteuerung können Sie ein Netzwerk-Subnetz erstellen, ändern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="ad91b-107">From the Lync Server Control Panel, you can create, modify, or delete a network subnet.</span></span> <span data-ttu-id="ad91b-108">Details zum Erstellen oder Ändern von Netzwerk-Subnetzen finden Sie unter Erstellen oder Ändern von Netzwerk-Subnetzen [in lync Server 2013](lync-server-2013-create-or-modify-network-subnets.md).</span><span class="sxs-lookup"><span data-stu-id="ad91b-108">For details about creating or modifying network subnets, see [Create or modify network subnets in Lync Server 2013](lync-server-2013-create-or-modify-network-subnets.md).</span></span>

<div>

## <a name="to-view-a-network-subnet"></a><span data-ttu-id="ad91b-109">So zeigen Sie ein Netzwerk-Subnetz an</span><span class="sxs-lookup"><span data-stu-id="ad91b-109">To view a network subnet</span></span>

1.  <span data-ttu-id="ad91b-110">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="ad91b-110">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ad91b-111">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ad91b-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ad91b-112">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ad91b-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ad91b-113">Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration** und dann auf **Subnetz**.</span><span class="sxs-lookup"><span data-stu-id="ad91b-113">In the left navigation bar, click **Network Configuration** and then click **Subnet**.</span></span>

4.  <span data-ttu-id="ad91b-114">Klicken Sie auf der Seite **Subnetz** auf das Subnetz, das Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="ad91b-114">On the **Subnet** page, click the subnet that you want to view.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="ad91b-115">Sie können jeweils nur ein Subnetz anzeigen.</span><span class="sxs-lookup"><span data-stu-id="ad91b-115">You can only view one subnet at a time.</span></span>

    
    </div>

5.  <span data-ttu-id="ad91b-116">Klicken Sie im Menü **Bearbeiten** auf **Details anzeigen**....</span><span class="sxs-lookup"><span data-stu-id="ad91b-116">On the **Edit** menu, click **Show details…**.</span></span>

</div>

<div>

## <a name="viewing-network-subnet-configuration-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="ad91b-117">Anzeigen von Netzwerk-Subnet-Konfigurationsinformationen mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ad91b-117">Viewing Network Subnet Configuration Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="ad91b-118">Netzwerk-Subnetz-Informationen können mithilfe von Windows PowerShell und dem Cmdlet Get-CsNetworkSubnet angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ad91b-118">Network subnet information can be viewed by using Windows PowerShell and the Get-CsNetworkSubnet cmdlet.</span></span> <span data-ttu-id="ad91b-119">Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="ad91b-119">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="ad91b-120">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="ad91b-120">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-network-subnet-information"></a><span data-ttu-id="ad91b-121">So zeigen Sie Netzwerk-Subnetz-Informationen an</span><span class="sxs-lookup"><span data-stu-id="ad91b-121">To view network subnet information</span></span>

  - <span data-ttu-id="ad91b-122">Wenn Sie Informationen zu allen Netzwerk-Subnetzen anzeigen möchten, geben Sie den folgenden Befehl in der lync Server-Verwaltungsshell ein, und drücken Sie dann die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="ad91b-122">To view information about all your network subnets, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsNetworkSubnet
    
    <span data-ttu-id="ad91b-123">Es werden etwa folgende Informationen zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="ad91b-123">That will return information similar to this:</span></span>
    
        Identity      : 172.11.15.0
        MaskBits      : 28
        Description   :
        NetworkSiteID : Redmond
        SubnetID      : 172.11.15.0

</div>

<span data-ttu-id="ad91b-124">Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Get-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSubnet) .</span><span class="sxs-lookup"><span data-stu-id="ad91b-124">For more information, see the help topic for the [Get-CsNetworkSubnet](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSubnet) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ad91b-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad91b-125">See Also</span></span>


[<span data-ttu-id="ad91b-126">Erstellen oder Ändern von Netzwerk-Subnetzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ad91b-126">Create or modify network subnets in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-network-subnets.md)  
[<span data-ttu-id="ad91b-127">Löschen von Netzwerk-Subnetzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ad91b-127">Deleting network subnets in Lync Server 2013</span></span>](lync-server-2013-deleting-network-subnets.md)  
  

<span data-ttu-id="ad91b-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ad91b-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

