---
title: 'Lync Server 2013: Erstellen oder Ändern von netzwerkregionen'
description: 'Lync Server 2013: Erstellen oder Ändern von netzwerkregionen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Creating or modifying network regions
ms:assetid: bd08bb66-5976-4ece-b45c-7de19569f814
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182579(v=OCS.15)
ms:contentKeyID: 48185266
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b02a041272f0df27d2133ca26096caeb01816c7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431414"
---
# <a name="creating-or-modifying-network-regions-in-lync-server-2013"></a><span data-ttu-id="ddeec-103">Erstellen oder Ändern von netzwerkregionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ddeec-103">Creating or modifying network regions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ddeec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ddeec-104">

<span> </span></span></span>

<span data-ttu-id="ddeec-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="ddeec-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="ddeec-106">Ein Netzwerkbereich verbindet verschiedene Teile eines Netzwerks über mehrere geographische Bereiche hinweg.</span><span class="sxs-lookup"><span data-stu-id="ddeec-106">A network region interconnects various parts of a network across multiple geographic areas.</span></span> <span data-ttu-id="ddeec-107">Jeder Netzwerkbereich muss einem zentralen Standort zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="ddeec-107">Every network region must be associated with a central site.</span></span> <span data-ttu-id="ddeec-108">Der zentrale Standort ist die Datencenter-Website, auf der der bandbreitenrichtliniendienst für die Anrufannahme Steuerung (CAC) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="ddeec-108">The central site is the data center site on which the call admission control (CAC) bandwidth policy service is running.</span></span> <span data-ttu-id="ddeec-109">Sie können die lync Server-Systemsteuerung verwenden, um netzwerkregionen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="ddeec-109">You can use Lync Server Control Panel to configure network regions.</span></span> <span data-ttu-id="ddeec-110">Zu den netzwerkregionen gehören Einstellungen, die bestimmen, ob für Audio-und Videoverbindungen alternative Pfade über das Internet zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="ddeec-110">Network regions include settings that determine whether alternate paths through the Internet are allowed for audio and video connections.</span></span> <span data-ttu-id="ddeec-111">In der lync Server-Systemsteuerung können Sie einen Netzwerkbereich erstellen, ändern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="ddeec-111">From the Lync Server Control Panel, you can create, modify, or delete a network region.</span></span> <span data-ttu-id="ddeec-112">Verwenden Sie dieses Thema, um netzwerkregionen zu erstellen und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="ddeec-112">Use this topic to create and modify network regions.</span></span> <span data-ttu-id="ddeec-113">Details zum Löschen vorhandener netzwerkregionen finden Sie unter [Löschen vorhandener netzwerkregionen in lync Server 2013](lync-server-2013-deleting-existing-network-regions.md).</span><span class="sxs-lookup"><span data-stu-id="ddeec-113">For details about deleting existing network regions, see [Deleting existing network regions in Lync Server 2013](lync-server-2013-deleting-existing-network-regions.md).</span></span>

<div>

## <a name="to-create-a-network-region"></a><span data-ttu-id="ddeec-114">So erstellen Sie einen Netzwerkbereich</span><span class="sxs-lookup"><span data-stu-id="ddeec-114">To create a network region</span></span>

1.  <span data-ttu-id="ddeec-115">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="ddeec-115">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ddeec-116">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ddeec-116">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ddeec-117">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ddeec-117">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ddeec-118">Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration** und dann auf **Region**.</span><span class="sxs-lookup"><span data-stu-id="ddeec-118">In the left navigation bar, click **Network Configuration** and then click **Region**.</span></span>

4.  <span data-ttu-id="ddeec-119">Klicken Sie auf der Seite **Region** auf **neu**.</span><span class="sxs-lookup"><span data-stu-id="ddeec-119">On the **Region** page, click **New**.</span></span>

5.  <span data-ttu-id="ddeec-120">Geben Sie auf der Seite **neuer Bereich** einen Wert in das Feld **Name** ein.</span><span class="sxs-lookup"><span data-stu-id="ddeec-120">In the **New Region** page, type a value in the **Name** field.</span></span> <span data-ttu-id="ddeec-121">Dieser Wert muss innerhalb Ihrer Microsoft lync Server 2013-Bereitstellung eindeutig sein.</span><span class="sxs-lookup"><span data-stu-id="ddeec-121">This value must be unique within your Microsoft Lync Server 2013 deployment.</span></span>

6.  <span data-ttu-id="ddeec-122">Wählen Sie in der Dropdownliste **Central Site** die zentrale Website für diesen Netzwerkbereich aus.</span><span class="sxs-lookup"><span data-stu-id="ddeec-122">From the **Central site** drop-down list, select the central site for this network region.</span></span>

7.  <span data-ttu-id="ddeec-123">Das Kontrollkästchen **audioalternativen Pfad aktivieren** ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ddeec-123">The **Enable audio alternate path** check box is checked by default.</span></span> <span data-ttu-id="ddeec-124">Dieses Feld bestimmt, ob Audioanrufe durch einen alternativen Pfad weitergeleitet werden, wenn im primären Pfad keine ausreichende Bandbreite vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ddeec-124">This field determines whether audio calls will be routed through an alternate path if adequate bandwidth does not exist in the primary path.</span></span> <span data-ttu-id="ddeec-125">Deaktivieren Sie dieses Kontrollkästchen nur, wenn Sie die Verschiebung zum Internet deaktivieren müssen.</span><span class="sxs-lookup"><span data-stu-id="ddeec-125">Clear this check box only if you need to turn off the offload to the Internet.</span></span> <span data-ttu-id="ddeec-126">Wenn es sich bei ihren anrufen um Internet Anrufe handelt, muss dieses Kontrollkästchen unabhängig von den Bandbreiteneinstellungen aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="ddeec-126">If any of your calls will be Internet calls, this check box must be checked, regardless of bandwidth settings.</span></span>

8.  <span data-ttu-id="ddeec-127">Das Kontrollkästchen **Video alternativen Pfad aktivieren** ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="ddeec-127">The **Enable video alternate path** check box is checked by default.</span></span> <span data-ttu-id="ddeec-128">Dieses Feld bestimmt, ob Videoanrufe über einen alternativen Pfad weitergeleitet werden, wenn im primären Pfad keine ausreichende Bandbreite vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="ddeec-128">This field determines whether video calls will be routed through an alternate path if adequate bandwidth does not exist in the primary path.</span></span> <span data-ttu-id="ddeec-129">Deaktivieren Sie dieses Kontrollkästchen nur, wenn Sie die Verschiebung zum Internet deaktivieren müssen.</span><span class="sxs-lookup"><span data-stu-id="ddeec-129">Clear this check box only if you need to turn off the offload to the Internet.</span></span> <span data-ttu-id="ddeec-130">Wenn es sich bei ihren anrufen um Internet Anrufe handelt, muss dieses Kontrollkästchen unabhängig von den Bandbreiteneinstellungen aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="ddeec-130">If any of your calls will be Internet calls, this check box must be checked, regardless of bandwidth settings.</span></span>

9.  <span data-ttu-id="ddeec-131">Optional Geben Sie im Feld **Beschreibung** einen Wert ein, um weitere Informationen zu dieser Region bereitzustellen, die nicht allein durch den Namen ausgedrückt werden können.</span><span class="sxs-lookup"><span data-stu-id="ddeec-131">(Optional) Type a value in the **Description** field to provide more information about this region that cannot be expressed by the name alone.</span></span>

10. <span data-ttu-id="ddeec-132">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="ddeec-132">Click **Commit**.</span></span>

<span data-ttu-id="ddeec-133">Die Tabelle **zugeordnete Websites** wird nicht zum Erstellen eines Netzwerkbereichs verwendet.</span><span class="sxs-lookup"><span data-stu-id="ddeec-133">The **Associated sites** table is not used for creating a network region.</span></span> <span data-ttu-id="ddeec-134">Sie ordnen eine Website einem Bereich zu, wenn Sie die Website erstellen oder ändern.</span><span class="sxs-lookup"><span data-stu-id="ddeec-134">You associate a site with a region when you create or modify the site.</span></span> <span data-ttu-id="ddeec-135">Ausführliche Informationen finden Sie unter [erstellen oder Ändern von Netzwerk Websites in lync Server 2013](lync-server-2013-creating-or-modifying-network-sites.md).</span><span class="sxs-lookup"><span data-stu-id="ddeec-135">For details, see [Creating or modifying network sites in Lync Server 2013](lync-server-2013-creating-or-modifying-network-sites.md).</span></span>

</div>

<div>

## <a name="to-modify-a-network-region"></a><span data-ttu-id="ddeec-136">So ändern Sie einen Netzwerkbereich</span><span class="sxs-lookup"><span data-stu-id="ddeec-136">To modify a network region</span></span>

1.  <span data-ttu-id="ddeec-137">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="ddeec-137">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ddeec-138">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ddeec-138">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ddeec-139">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ddeec-139">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ddeec-140">Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration** und dann auf **Region**.</span><span class="sxs-lookup"><span data-stu-id="ddeec-140">In the left navigation bar, click **Network Configuration** and then click **Region**.</span></span>

4.  <span data-ttu-id="ddeec-141">Klicken Sie auf der Seite **Region** auf den Bereich, den Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="ddeec-141">On the **Region** page, click the region that you want to modify.</span></span>

5.  <span data-ttu-id="ddeec-142">Klicken Sie im Menü **Bearbeiten** auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="ddeec-142">On the **Edit** menu, click **Show details**.</span></span>

6.  <span data-ttu-id="ddeec-143">Auf der Seite " **Bereich bearbeiten** " können Sie die Einstellungen für die Aktivierung und Deaktivierung von Audio-und Video Alternativen Pfaden ändern und die Beschreibung ändern (Einzelheiten finden Sie im Abschnitt "So erstellen Sie einen Netzwerkbereich" weiter oben in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="ddeec-143">On the **Edit Region** page, you can modify the settings for enabling and disabling audio and video alternate paths, and change the description (for details, see the "To create a network region" section earlier in this topic.</span></span>

7.  <span data-ttu-id="ddeec-144">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="ddeec-144">Click **Commit**.</span></span>

<span data-ttu-id="ddeec-145">Auf dieser Seite können Sie die **zugehörigen Websites** nicht ändern.</span><span class="sxs-lookup"><span data-stu-id="ddeec-145">You cannot modify the **Associated sites** on this page.</span></span> <span data-ttu-id="ddeec-146">Die Liste der zugehörigen Websites wird als Referenz bereitgestellt, damit Sie wissen, welche Websites beeinträchtigt werden, wenn Sie die Regionseinstellungen ändern.</span><span class="sxs-lookup"><span data-stu-id="ddeec-146">The list of associated sites is provided for reference so you are aware of which sites will be affected when you modify the region settings.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ddeec-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ddeec-147">See Also</span></span>


[<span data-ttu-id="ddeec-148">Löschen vorhandener netzwerkregionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ddeec-148">Deleting existing network regions in Lync Server 2013</span></span>](lync-server-2013-deleting-existing-network-regions.md)  
[<span data-ttu-id="ddeec-149">Konfigurieren von netzwerkregionen für CAC in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ddeec-149">Configure network regions for CAC in Lync Server 2013</span></span>](lync-server-2013-configure-network-regions-for-cac.md)  


[<span data-ttu-id="ddeec-150">New-CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="ddeec-150">New-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsNetworkRegion)  
[<span data-ttu-id="ddeec-151">Set-CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="ddeec-151">Set-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsNetworkRegion)  
[<span data-ttu-id="ddeec-152">Remove-CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="ddeec-152">Remove-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkRegion)  
[<span data-ttu-id="ddeec-153">Get-CsNetworkRegion</span><span class="sxs-lookup"><span data-stu-id="ddeec-153">Get-CsNetworkRegion</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkRegionLink)  
  

<span data-ttu-id="ddeec-154"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ddeec-154"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

