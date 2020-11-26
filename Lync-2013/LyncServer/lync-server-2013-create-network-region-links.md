---
title: 'Lync Server 2013: Erstellen von Netzwerk Regions Verknüpfungen'
description: 'Lync Server 2013: Erstellen von Netzwerk Regions Verknüpfungen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create network region links
ms:assetid: f8163910-8935-475d-88a2-3aa44feb9dbe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg413047(v=OCS.15)
ms:contentKeyID: 48185873
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6510d252ac1534a3a8e9f14d56acc8d0d8b60a6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431897"
---
# <a name="create-network-region-links-in-lync-server-2013"></a><span data-ttu-id="16563-103">Erstellen von Netzwerkbereichs Links in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="16563-103">Create network region links in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="16563-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="16563-104">

<span> </span></span></span>

<span data-ttu-id="16563-105">_**Letztes Änderungsdatum des Themas:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="16563-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="16563-106">Regionen in einem Netzwerk sind über physische WAN-Verbindungen miteinander verbunden.</span><span class="sxs-lookup"><span data-stu-id="16563-106">Regions within a network are linked through physical WAN connectivity.</span></span> <span data-ttu-id="16563-107">Eine *Netzwerk Regions Verknüpfung* erstellt eine Verknüpfung zwischen zwei Regionen, die für die Anrufannahme Steuerung konfiguriert sind, und legt die Bandbreiteneinschränkungen für den Audio-und Videoverkehr zwischen diesen Regionen fest.</span><span class="sxs-lookup"><span data-stu-id="16563-107">A *network region link* creates a link between two regions configured for call admission control (CAC) and sets the bandwidth limitations on audio and video traffic between these regions.</span></span>

<span data-ttu-id="16563-108">Details zum Arbeiten mit Netzwerk Regions Verknüpfungen finden Sie in der Dokumentation zur lync Server-Verwaltungsshell für die folgenden Cmdlets:</span><span class="sxs-lookup"><span data-stu-id="16563-108">For details about working with network region links, see the Lync Server Management Shell documentation for the following cmdlets:</span></span>

  - [<span data-ttu-id="16563-109">New-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="16563-109">New-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegionLink)

  - [<span data-ttu-id="16563-110">Get-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="16563-110">Get-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink)

  - [<span data-ttu-id="16563-111">Set-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="16563-111">Set-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkRegionLink)

  - [<span data-ttu-id="16563-112">Remove-CsNetworkRegionLink</span><span class="sxs-lookup"><span data-stu-id="16563-112">Remove-CsNetworkRegionLink</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkRegionLink)

<span data-ttu-id="16563-113">Die Beispieltopologie weist eine Verbindung zwischen den Regionen „North America“ und „APAC“ sowie zwischen den Regionen „EMEA“ und „APAC“ auf.</span><span class="sxs-lookup"><span data-stu-id="16563-113">The example topology has a link between the North America and APAC regions, and a link between the EMEA and APAC regions.</span></span> <span data-ttu-id="16563-114">Jede dieser Regions Verknüpfungen wird durch die WAN-Bandbreite beschränkt, wie in der Tabelle Regions Link-bandbreiteninformationen im [Beispiel beschrieben: Sammeln Ihrer Anforderungen für die Anrufsteuerung im Abschnitt lync Server 2013](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md) der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="16563-114">Each of these region links is constrained by WAN bandwidth, as described in Region Link Bandwidth Information table in the [Example: Gathering your requirements for call admission control in Lync Server 2013](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md) section of the Planning documentation.</span></span>

<div>

## <a name="to-create-network-region-links-by-using-lync-server-management-shell"></a><span data-ttu-id="16563-115">So erstellen Sie Netzwerk Regions Verknüpfungen mithilfe der lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="16563-115">To create network region links by using Lync Server Management Shell</span></span>

1.  <span data-ttu-id="16563-116">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="16563-116">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="16563-117">Führen Sie das Cmdlet „New-CsNetworkRegionLink“ aus, um die Regionenverbindungen zu erstellen und geeignete Bandbreitenrichtlinienprofile anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="16563-117">Run the New-CsNetworkRegionLink cmdlet to create the region links and apply appropriate bandwidth policy profiles.</span></span> <span data-ttu-id="16563-118">Führen Sie beispielsweise den folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="16563-118">For example, run:</span></span>
    
      ```powershell
        New-CsNetworkRegionLink -NetworkRegionLinkID NA-EMEA-LINK -NetworkRegionID1 NorthAmerica -NetworkRegionID2 EMEA -BWPolicyProfileID 50Mb_Link
      ```
    
      ```powershell
        New-CsNetworkRegionLink -NetworkRegionLinkID EMEA-APAC-LINK -NetworkRegionID1 EMEA -NetworkRegionID2 APAC -BWPolicyProfileID 25Mb_Link
      ```

</div>

<div>

## <a name="to-create-network-region-links-by-using-lync-server-control-panel"></a><span data-ttu-id="16563-119">So erstellen Sie Netzwerk Regions Verknüpfungen mithilfe der lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="16563-119">To create network region links by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="16563-120">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="16563-120">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="16563-121">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="16563-121">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="16563-122">Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="16563-122">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="16563-123">Klicken Sie auf die Navigationsschaltfläche **Regionenverbindung**.</span><span class="sxs-lookup"><span data-stu-id="16563-123">Click the **Region Link** navigation button.</span></span>

4.  <span data-ttu-id="16563-124">Klicken Sie auf **Neu**.</span><span class="sxs-lookup"><span data-stu-id="16563-124">Click **New**.</span></span>

5.  <span data-ttu-id="16563-125">Klicken Sie auf der Seite **Neue Netzwerkregionenverbindung** auf **Name** und geben Sie einen Namen für die Netzwerkregionenverbindung ein.</span><span class="sxs-lookup"><span data-stu-id="16563-125">On the **New Region Link** page, click **Name** and then type a name for the network region link.</span></span>

6.  <span data-ttu-id="16563-126">Klicken Sie auf **netzwerkregion \# 1**, und klicken Sie dann in der Liste, die Sie mit netzwerkregion 2 verknüpfen möchten, auf den Bereich Netzwerk \# .</span><span class="sxs-lookup"><span data-stu-id="16563-126">Click **Network Region \#1**, and then click the network region in the list that you want to link to Network Region \#2.</span></span>

7.  <span data-ttu-id="16563-127">Klicken Sie auf **netzwerkregion \# 2**, und klicken Sie dann in der Liste auf einen Netzwerkbereich, den Sie mit netzwerkregion 1 verknüpfen möchten \# .</span><span class="sxs-lookup"><span data-stu-id="16563-127">Click **Network Region \#2**, and then click a network region in the list that you want to link to Network Region \#1.</span></span>

8.  <span data-ttu-id="16563-128">Klicken Sie optional auf **Bandbreitenrichtlinie** und wählen Sie das Bandbreitenrichtlinienprofil aus, das Sie auf die Netzwerkregionenverbindung anwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="16563-128">Optionally, click **Bandwidth policy**, and then select the bandwidth policy profile that you want to apply to the network region link.</span></span>
    
    <div class=" ">
    

    > [!NOTE]  
    > <span data-ttu-id="16563-129">Wenden Sie nur dann eine Bandbreitenrichtlinie an, wenn die Netzwerkregionenverbindung eine Bandbreiteneinschränkung aufweist und Sie die Anrufsteuerung verwenden möchten, um den Mediendatenverkehr in dieser Verbindung zu steuern.</span><span class="sxs-lookup"><span data-stu-id="16563-129">Apply a bandwidth policy only if the network region link is bandwidth-constrained and you want to use CAC to control media traffic on that link.</span></span>

    
    </div>

9.  <span data-ttu-id="16563-130">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="16563-130">Click **Commit**.</span></span>

10. <span data-ttu-id="16563-131">Zum Abschließen der Erstellung von Netzwerkregionenverbindungen für Ihre Topologie wiederholen Sie die Schritte 4 bis 9 mit Einstellungen für weitere Regionen.</span><span class="sxs-lookup"><span data-stu-id="16563-131">To finish creating network region links for your topology, repeat steps 4 through 9 with settings for other regions.</span></span>

<span data-ttu-id="16563-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="16563-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>
