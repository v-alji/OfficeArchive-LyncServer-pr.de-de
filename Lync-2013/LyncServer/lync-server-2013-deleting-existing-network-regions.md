---
title: 'Lync Server 2013: Löschen vorhandener netzwerkregionen'
description: 'Lync Server 2013: Löschen vorhandener netzwerkregionen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting existing network regions
ms:assetid: c7293a2f-2b49-4c4a-903f-f7edcea2bc5f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721882(v=OCS.15)
ms:contentKeyID: 49733815
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b148f0bd92ad398ab7057a5a291bf3245df3e47e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430322"
---
# <a name="deleting-existing-network-regions-in-lync-server-2013"></a><span data-ttu-id="02381-103">Löschen vorhandener netzwerkregionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="02381-103">Deleting existing network regions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="02381-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="02381-104">

<span> </span></span></span>

<span data-ttu-id="02381-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="02381-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="02381-106">Ein Netzwerkbereich verbindet verschiedene Teile eines Netzwerks über mehrere geographische Bereiche hinweg.</span><span class="sxs-lookup"><span data-stu-id="02381-106">A network region interconnects various parts of a network across multiple geographic areas.</span></span> <span data-ttu-id="02381-107">Jeder Netzwerkbereich muss einem zentralen Standort zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="02381-107">Every network region must be associated with a central site.</span></span> <span data-ttu-id="02381-108">Der zentrale Standort ist die Datencenter-Website, auf der der bandbreitenrichtliniendienst für die Anrufannahme Steuerung (CAC) ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="02381-108">The central site is the data center site on which the call admission control (CAC) bandwidth policy service is running.</span></span> <span data-ttu-id="02381-109">Sie können die lync Server-Systemsteuerung verwenden, um netzwerkregionen zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="02381-109">You can use Lync Server Control Panel to configure network regions.</span></span> <span data-ttu-id="02381-110">Zu den netzwerkregionen gehören Einstellungen, die bestimmen, ob für Audio-und Videoverbindungen alternative Pfade über das Internet zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="02381-110">Network regions include settings that determine whether alternate paths through the Internet are allowed for audio and video connections.</span></span> <span data-ttu-id="02381-111">In der lync Server-Systemsteuerung können Sie einen Netzwerkbereich erstellen, ändern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="02381-111">From the Lync Server Control Panel, you can create, modify, or delete a network region.</span></span> <span data-ttu-id="02381-112">Verwenden Sie dieses Thema, um vorhandene netzwerkregionen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="02381-112">Use this topic to delete existing network regions.</span></span> <span data-ttu-id="02381-113">Details zum Erstellen oder Ändern vorhandener netzwerkregionen finden Sie unter [erstellen oder Ändern von netzwerkregionen in lync Server 2013](lync-server-2013-creating-or-modifying-network-regions.md).</span><span class="sxs-lookup"><span data-stu-id="02381-113">For details about creating or modifying existing network regions, see [Creating or modifying network regions in Lync Server 2013](lync-server-2013-creating-or-modifying-network-regions.md).</span></span>

<div>

## <a name="to-delete-a-network-region"></a><span data-ttu-id="02381-114">So löschen Sie einen Netzwerkbereich</span><span class="sxs-lookup"><span data-stu-id="02381-114">To delete a network region</span></span>

1.  <span data-ttu-id="02381-115">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="02381-115">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="02381-116">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="02381-116">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="02381-117">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="02381-117">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="02381-118">Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration** und dann auf **Region**.</span><span class="sxs-lookup"><span data-stu-id="02381-118">In the left navigation bar, click **Network Configuration** and then click **Region**.</span></span>

4.  <span data-ttu-id="02381-119">Klicken Sie auf der Seite **Region** auf den Bereich, den Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="02381-119">On the **Region** page, click the region you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="02381-120">Sie können mehr als einen Bereich gleichzeitig löschen.</span><span class="sxs-lookup"><span data-stu-id="02381-120">You can delete more than one region at a time.</span></span> <span data-ttu-id="02381-121">Drücken Sie dazu STRG, und wählen Sie mehrere Bereiche aus, während Sie die STRG-Taste gedrückt halten.</span><span class="sxs-lookup"><span data-stu-id="02381-121">To do this, press CTRL and select multiple regions while holding down the CTRL key.</span></span> <span data-ttu-id="02381-122">Wenn Sie alle Bereiche auswählen möchten, klicken Sie im Menü <STRONG>Bearbeiten</STRONG> auf <STRONG>Alle auswählen</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="02381-122">Or, to select all regions, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="02381-123">Klicken Sie im Menü **Bearbeiten** auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="02381-123">On the **Edit** menu, click **Delete**.</span></span>

6.  <span data-ttu-id="02381-124">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="02381-124">Click **OK**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="02381-125">Eine netzwerkregion kann nicht entfernt werden, wenn Sie einer Netzwerk Website zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="02381-125">A network region cannot be removed if it is associated with a network site.</span></span> <span data-ttu-id="02381-126">Wenn Sie versuchen, einen Bereich zu entfernen, der einer Website zugeordnet ist, wird eine Fehlermeldung angezeigt.</span><span class="sxs-lookup"><span data-stu-id="02381-126">If you attempt to remove a region associated with a site you will receive an error message.</span></span> <span data-ttu-id="02381-127">Wenn Sie feststellen möchten, ob ein Bereich Websites zugeordnet ist, wählen Sie den Bereich aus, und klicken Sie dann im Menü <STRONG>Bearbeiten</STRONG> auf <STRONG>Details anzeigen</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="02381-127">To see if a region is associated with any sites, select the region and then click <STRONG>Show details</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="02381-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="02381-128">See Also</span></span>


[<span data-ttu-id="02381-129">Erstellen oder Ändern von netzwerkregionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="02381-129">Creating or modifying network regions in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-regions.md)  
  

<span data-ttu-id="02381-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="02381-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

