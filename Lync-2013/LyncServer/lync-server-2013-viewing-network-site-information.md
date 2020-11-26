---
title: 'Lync Server 2013: Anzeigen von Netzwerk Website Informationen'
description: 'Lync Server 2013: Anzeigen von Informationen zur Netzwerk Website.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network site information
ms:assetid: 24a97d98-b168-4016-81bf-c2c478092b87
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687996(v=OCS.15)
ms:contentKeyID: 49733586
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b46dc91510cb5ff737977871470033374573ba8c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440402"
---
# <a name="viewing-network-site-information-in-lync-server-2013"></a><span data-ttu-id="bfdb1-103">Anzeigen von Netzwerk Website Informationen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bfdb1-103">Viewing network site information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bfdb1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bfdb1-104">

<span> </span></span></span>

<span data-ttu-id="bfdb1-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="bfdb1-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="bfdb1-106">Netzwerk Websites sind die Büros oder Standorte, die in den einzelnen Regionen einer Anrufannahme Steuerung oder erweiterten 9-1-1-Bereitstellung konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="bfdb1-106">Network sites are the offices or locations configured within each region of a call admission control (CAC) or Enhanced 9-1-1 deployment.</span></span> <span data-ttu-id="bfdb1-107">Sie können Netzwerk Website Informationen entweder in der lync Server 2013-Systemsteuerung oder in der lync Server-Verwaltungsshell anzeigen.</span><span class="sxs-lookup"><span data-stu-id="bfdb1-107">You can view network site information in either Lync Server 2013 Control Panel or Lync Server Management Shell .</span></span> <span data-ttu-id="bfdb1-108">Details zum Erstellen oder Ändern von Netzwerk Websites finden Sie unter [erstellen oder Ändern von Netzwerk Websites in lync Server 2013](lync-server-2013-creating-or-modifying-network-sites.md).</span><span class="sxs-lookup"><span data-stu-id="bfdb1-108">For details about creating or modifying network sites, see [Creating or modifying network sites in Lync Server 2013](lync-server-2013-creating-or-modifying-network-sites.md).</span></span>

<div>

## <a name="to-view-network-site-information-in-lync-server-control-panel"></a><span data-ttu-id="bfdb1-109">So zeigen Sie Netzwerk Website Informationen in der lync Server-Systemsteuerung an</span><span class="sxs-lookup"><span data-stu-id="bfdb1-109">To view network site information in Lync Server Control Panel</span></span>

1.  <span data-ttu-id="bfdb1-110">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="bfdb1-110">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="bfdb1-111">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bfdb1-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="bfdb1-112">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="bfdb1-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="bfdb1-113">Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration** , und klicken Sie dann auf **Website**.</span><span class="sxs-lookup"><span data-stu-id="bfdb1-113">In the left navigation bar, click **Network Configuration** and then click **Site**.</span></span>

4.  <span data-ttu-id="bfdb1-114">Klicken Sie auf der Seite **Website** auf die Website, die Sie anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="bfdb1-114">On the **Site** page, click the site that you want to view.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="bfdb1-115">Sie können nur Informationen für eine Website gleichzeitig anzeigen.</span><span class="sxs-lookup"><span data-stu-id="bfdb1-115">You can only view information for one site at a time.</span></span>

    
    </div>

5.  <span data-ttu-id="bfdb1-116">Klicken Sie im Menü **Bearbeiten** auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="bfdb1-116">On the **Edit** menu, click **Show details**.</span></span>

</div>

<div>

## <a name="viewing-network-site-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="bfdb1-117">Anzeigen von Netzwerk Website Informationen mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bfdb1-117">Viewing Network Site Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="bfdb1-118">Sie können Netzwerk Website Informationen mithilfe von Windows PowerShell und dem Get-CsNetworkSite-Cmdlet anzeigen.</span><span class="sxs-lookup"><span data-stu-id="bfdb1-118">You can view network site information by using Windows PowerShell and the Get-CsNetworkSite cmdlet.</span></span> <span data-ttu-id="bfdb1-119">Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bfdb1-119">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="bfdb1-120">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="bfdb1-120">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-network-site-information"></a><span data-ttu-id="bfdb1-121">So zeigen Sie Netzwerk Website Informationen an</span><span class="sxs-lookup"><span data-stu-id="bfdb1-121">To view network site information</span></span>

  - <span data-ttu-id="bfdb1-122">Wenn Sie Informationen zu allen Ihren Netzwerk Websites anzeigen möchten, geben Sie den folgenden Befehl in der lync Server-Verwaltungsshell ein, und drücken Sie dann die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="bfdb1-122">To view information about all your network sites, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsNetworkSite
    
    <span data-ttu-id="bfdb1-123">Es werden etwa folgende Informationen zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="bfdb1-123">That will return information similar to this:</span></span>
    
        Identity          : Redmond
        NetworkSiteID     : Redmond
        Description       :
        NetworkRegionID   : Pacific Northwest
        BypassID          : 3b232b84-2c1d-4da2-8181-e9330bafebe9
        BWPolicyProfileID :
        LocationPolicy    :

</div>

<span data-ttu-id="bfdb1-124">Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Get-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSite) .</span><span class="sxs-lookup"><span data-stu-id="bfdb1-124">For more information, see the help topic for the [Get-CsNetworkSite](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkSite) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="bfdb1-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bfdb1-125">See Also</span></span>


[<span data-ttu-id="bfdb1-126">Erstellen oder Ändern von Netzwerk Websites in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bfdb1-126">Creating or modifying network sites in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-sites.md)  
[<span data-ttu-id="bfdb1-127">Löschen einer vorhandenen Netzwerk Website in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bfdb1-127">Deleting an existing network site in Lync Server 2013</span></span>](lync-server-2013-deleting-an-existing-network-site.md)  
  

<span data-ttu-id="bfdb1-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bfdb1-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

