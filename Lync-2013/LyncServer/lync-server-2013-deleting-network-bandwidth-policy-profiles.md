---
title: 'Lync Server 2013: Löschen von Netzwerkbandbreite-Richtlinienprofilen'
description: 'Lync Server 2013: Löschen von Netzwerkbandbreite-Richtlinienprofilen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting network bandwidth policy profiles
ms:assetid: 4d6beda8-6aa5-4d5e-8a07-363598f0e0c8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688050(v=OCS.15)
ms:contentKeyID: 49733643
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 69f460d9620158d1857dae41e0033f6d36078868
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430301"
---
# <a name="deleting-network-bandwidth-policy-profiles-in-lync-server-2013"></a><span data-ttu-id="0655d-103">Löschen von Netzwerkbandbreite-Richtlinienprofilen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0655d-103">Deleting network bandwidth policy profiles in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0655d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0655d-104">

<span> </span></span></span>

<span data-ttu-id="0655d-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="0655d-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="0655d-106">Im Rahmen der Anrufannahme Steuerung (CAC) wird eine bandbreitenrichtlinie verwendet, um Bandbreiteneinschränkungen für bestimmte Modalitäten festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0655d-106">As part of call admission control (CAC), a bandwidth policy is used to define bandwidth limitations for certain modalities.</span></span> <span data-ttu-id="0655d-107">In Microsoft lync Server 2013 können nur den Audio-und Video-Modalitäten Bandbreiteneinschränkungen zugewiesen werden.</span><span class="sxs-lookup"><span data-stu-id="0655d-107">In Microsoft Lync Server 2013, only audio and video modalities can be assigned bandwidth limitations.</span></span> <span data-ttu-id="0655d-108">Sie können allgemeine Bandbreiteneinschränkungen und Sitzungs Einschränkungen einstellen.</span><span class="sxs-lookup"><span data-stu-id="0655d-108">You can set overall bandwidth limitations and session limitations.</span></span> <span data-ttu-id="0655d-109">Sie können die lync Server-Systemsteuerung verwenden, um ein Container Profil für diese Richtlinien zu erstellen, zu ändern oder zu löschen.</span><span class="sxs-lookup"><span data-stu-id="0655d-109">You can use the Lync Server Control Panel to create, modify, or delete a container profile for these policies.</span></span> <span data-ttu-id="0655d-110">Gehen Sie wie folgt vor, um ein Netzwerkband breiten Richtlinienprofil zu löschen.</span><span class="sxs-lookup"><span data-stu-id="0655d-110">Use the following procedures to delete a network bandwidth policy profiles.</span></span> <span data-ttu-id="0655d-111">Details zum Erstellen oder Ändern eines Richtlinienprofils für die Netzwerkbandbreite finden Sie unter [erstellen oder Ändern von Bandbreitenrichtlinien Profilen in lync Server 2013](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md).</span><span class="sxs-lookup"><span data-stu-id="0655d-111">For details on creating or modifying a network bandwidth policy profile, see [Creating or modifying bandwidth policy profiles in Lync Server 2013](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md).</span></span>

<div>

## <a name="to-delete-a-bandwidth-policy-profile"></a><span data-ttu-id="0655d-112">So löschen Sie ein bandbreitenrichtlinienprofil</span><span class="sxs-lookup"><span data-stu-id="0655d-112">To delete a bandwidth policy profile</span></span>

1.  <span data-ttu-id="0655d-113">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="0655d-113">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="0655d-114">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0655d-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="0655d-115">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="0655d-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="0655d-116">Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration** , und klicken Sie dann auf **bandbreitenrichtlinie**.</span><span class="sxs-lookup"><span data-stu-id="0655d-116">In the left navigation bar, click **Network Configuration** and then click **Bandwidth Policy**.</span></span>

4.  <span data-ttu-id="0655d-117">Klicken Sie auf der Seite **bandbreitenrichtlinie** auf das bandbreitenrichtlinienprofil, das Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="0655d-117">On the **Bandwidth Policy** page, click the bandwidth policy profile that you want to delete.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="0655d-118">Sie können mehr als ein Profil gleichzeitig löschen.</span><span class="sxs-lookup"><span data-stu-id="0655d-118">You can delete more than one profile at a time.</span></span> <span data-ttu-id="0655d-119">Drücken Sie dazu STRG, und wählen Sie mehrere Profile aus, während Sie die STRG-Taste gedrückt halten.</span><span class="sxs-lookup"><span data-stu-id="0655d-119">To do this, press CTRL and select multiple profiles while holding down the CTRL key.</span></span> <span data-ttu-id="0655d-120">Wenn Sie alle Profile auswählen möchten, klicken Sie im Menü <STRONG>Bearbeiten</STRONG> auf <STRONG>Alles auswählen</STRONG> .</span><span class="sxs-lookup"><span data-stu-id="0655d-120">Or, to select all profiles, click <STRONG>Select all</STRONG> on the <STRONG>Edit</STRONG> menu.</span></span>

    
    </div>

5.  <span data-ttu-id="0655d-121">Klicken Sie im Menü **Bearbeiten** auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="0655d-121">On the **Edit** menu, click **Delete**.</span></span>
    
    <div>
    

    > [!WARNING]  
    > <span data-ttu-id="0655d-122">Sie können ein bandbreitenrichtlinienprofil, das einer Netzwerk Website zugeordnet ist, nicht löschen.</span><span class="sxs-lookup"><span data-stu-id="0655d-122">You cannot delete a bandwidth policy profile that is associated with a network site.</span></span> <span data-ttu-id="0655d-123">Sie müssen zuerst die Zuordnung zur Netzwerk Website entfernen, bevor Sie das Profil löschen können.</span><span class="sxs-lookup"><span data-stu-id="0655d-123">You must first remove the association with the network site before you can delete the profile.</span></span> <span data-ttu-id="0655d-124">Details zum Ändern der Netzwerk Website finden Sie unter <A href="lync-server-2013-creating-or-modifying-network-sites.md">erstellen oder Ändern von Netzwerk Websites in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="0655d-124">For details about how to modify the network site, see <A href="lync-server-2013-creating-or-modifying-network-sites.md">Creating or modifying network sites in Lync Server 2013</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0655d-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0655d-125">See Also</span></span>


[<span data-ttu-id="0655d-126">Erstellen oder Ändern von Bandbreitenrichtlinien Profilen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0655d-126">Creating or modifying bandwidth policy profiles in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-bandwidth-policy-profiles.md)  
[<span data-ttu-id="0655d-127">Anzeigen von Profilinformationen zu Netzwerkbandbreiten in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0655d-127">Viewing network bandwidth policy profile information in Lync Server 2013</span></span>](lync-server-2013-viewing-network-bandwidth-policy-profile-information.md)  


[<span data-ttu-id="0655d-128">Konfigurieren der Anrufsteuerung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0655d-128">Configure call admission control in Lync Server 2013</span></span>](lync-server-2013-configure-call-admission-control.md)  
[<span data-ttu-id="0655d-129">Remove-CsNetworkBandwidthPolicyProfile</span><span class="sxs-lookup"><span data-stu-id="0655d-129">Remove-CsNetworkBandwidthPolicyProfile</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsNetworkBandwidthPolicyProfile)  
  

<span data-ttu-id="0655d-130"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0655d-130"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

