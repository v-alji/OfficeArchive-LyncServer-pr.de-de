---
title: 'Lync Server 2013: Anzeigen von Verbindungsinformationen zu netzwerkregionen'
description: 'Lync Server 2013: Anzeigen von Verbindungsinformationen zu netzwerkregionen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network region link information
ms:assetid: 7b6b2ea2-83d8-4376-afb2-70e5d2cf6444
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688102(v=OCS.15)
ms:contentKeyID: 49733701
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0134ded9942ebda91050c1f7b0bbcfef018451a3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446205"
---
# <a name="viewing-network-region-link-information-in-lync-server-2013"></a><span data-ttu-id="74340-103">Anzeigen von Link Informationen zu netzwerkregionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74340-103">Viewing network region link information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="74340-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="74340-104">

<span> </span></span></span>

<span data-ttu-id="74340-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="74340-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="74340-106">Sie können die Verknüpfungen zwischen zwei netzwerkregionen im Rahmen der Anrufsteuerung (Call Admission Control, CAC) anzeigen.</span><span class="sxs-lookup"><span data-stu-id="74340-106">You can view links between two network regions as part of call admission control (CAC).</span></span> <span data-ttu-id="74340-107">Regionen in einem Netzwerk sind über die physische WAN-Konnektivität (Wide Area Network) verbunden.</span><span class="sxs-lookup"><span data-stu-id="74340-107">Regions within a network are linked through physical wide area network (WAN) connectivity.</span></span> <span data-ttu-id="74340-108">Sie können die lync Server-Systemsteuerung verwenden, um eine vorhandene Verknüpfung zwischen zwei netzwerkregionen anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="74340-108">You can use the Lync Server Control Panel to view an existing link between two network regions.</span></span> <span data-ttu-id="74340-109">Details zum Erstellen oder Ändern von Netzwerk Regions Verknüpfungen finden Sie unter [Konfigurieren von Netzwerkbereichs Links in lync Server 2013](lync-server-2013-configuring-network-region-links.md).</span><span class="sxs-lookup"><span data-stu-id="74340-109">For details about creating or modifying network region link, see [Configuring network region links in Lync Server 2013](lync-server-2013-configuring-network-region-links.md).</span></span>

<div>

## <a name="to-view-a-network-region-link-in-lync-server-control-panel"></a><span data-ttu-id="74340-110">So zeigen Sie einen Link zum Netzwerkbereich in der lync Server-Systemsteuerung an</span><span class="sxs-lookup"><span data-stu-id="74340-110">To view a network region link in Lync Server Control Panel</span></span>

1.  <span data-ttu-id="74340-111">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="74340-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="74340-112">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="74340-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="74340-113">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="74340-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="74340-114">Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration** und dann auf **Regions Link**.</span><span class="sxs-lookup"><span data-stu-id="74340-114">In the left navigation bar, click **Network Configuration** and then click **Region Link**.</span></span>

4.  <span data-ttu-id="74340-115">Klicken Sie auf der Seite **Regions Link** auf den Link Region, den Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="74340-115">On the **Region Link** page, click the region link that you want to view.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="74340-116">Sie können nur Informationen zu einem Regions Link gleichzeitig anzeigen.</span><span class="sxs-lookup"><span data-stu-id="74340-116">You can only view information about one region link at a time.</span></span>

    
    </div>

5.  <span data-ttu-id="74340-117">Wählen Sie im Menü **Bearbeiten** die Option **Details anzeigen** aus.</span><span class="sxs-lookup"><span data-stu-id="74340-117">From the **Edit** menu, select **Show details**.</span></span>

</div>

<div>

## <a name="viewing-network-region-link-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="74340-118">Anzeigen von Link Informationen zu netzwerkregionen mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="74340-118">Viewing Network Region Link Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="74340-119">Sie können Netzwerk Regions Verknüpfungen mithilfe von Windows PowerShell und dem Cmdlet **Get-CsNetworkRegionLink** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="74340-119">You can view network region links by using Windows PowerShell and the **Get-CsNetworkRegionLink** cmdlet.</span></span> <span data-ttu-id="74340-120">Sie können dieses Cmdlet in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="74340-120">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="74340-121">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="74340-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-network-region-link-information"></a><span data-ttu-id="74340-122">So zeigen Sie netzwerkregion-Verknüpfungsinformationen an</span><span class="sxs-lookup"><span data-stu-id="74340-122">To view network region link information</span></span>

  - <span data-ttu-id="74340-123">Wenn Sie Informationen zu allen ihren netzwerkregion-Links anzeigen möchten, geben Sie den folgenden Befehl in der lync Server-Verwaltungsshell ein, und drücken Sie dann die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="74340-123">To view information about all your network region links, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsNetworkRegionLink
    
    <span data-ttu-id="74340-124">Mit diesem Befehl werden Informationen ähnlich der folgenden zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="74340-124">This command returns information similar to the following:</span></span>
    
        Identity            : NorthwestToCalifornia
        BWPolicyProfileID   :
        NetworkRegionLinkID : NorthwestToCalifornia
        NetworkRegionID1    : Pacific Northwest
        NetworkRegionID2    : California

</div>

<span data-ttu-id="74340-125">Ausführliche Informationen finden Sie unter [Get-CsNetworkRegionLink](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink).</span><span class="sxs-lookup"><span data-stu-id="74340-125">For details, see [Get-CsNetworkRegionLink](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="74340-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="74340-126">See Also</span></span>


[<span data-ttu-id="74340-127">Konfigurieren von Netzwerkstandort Links in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="74340-127">Configuring network site links in Lync Server 2013</span></span>](lync-server-2013-configuring-network-site-links.md)  
  

<span data-ttu-id="74340-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="74340-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

