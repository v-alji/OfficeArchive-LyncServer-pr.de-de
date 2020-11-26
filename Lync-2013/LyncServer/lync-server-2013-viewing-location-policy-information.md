---
title: 'Lync Server 2013: Anzeigen von Positions Richtlinieninformationen'
description: 'Lync Server 2013: Anzeigen von Informationen zu Standortrichtlinien.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing location policy information
ms:assetid: 14e41bcb-ea0a-49c2-99b3-1f61fc34416d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520954(v=OCS.15)
ms:contentKeyID: 48183489
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2fecc5de5fb71014a1641038e9e09afba0e90cdb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443958"
---
# <a name="viewing-location-policy-information-in-lync-server-2013"></a><span data-ttu-id="aab41-103">Anzeigen von Standortrichtlinien Informationen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aab41-103">Viewing location policy information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="aab41-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="aab41-104">

<span> </span></span></span>

<span data-ttu-id="aab41-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="aab41-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="aab41-106">In lync Server 2013 können Sie mithilfe der ortungsrichtlinie Einstellungen anwenden, die sich auf die erweiterte 9-1-1 (E9-1-1)-Funktionalität und auf die Standorteinstellungen für Benutzer oder Kontakte beziehen.</span><span class="sxs-lookup"><span data-stu-id="aab41-106">In Lync Server 2013, you can use the location policy to apply settings that relate to Enhanced 9-1-1 (E9-1-1) functionality and to location settings for users or contacts.</span></span> <span data-ttu-id="aab41-107">Die ortungsrichtlinie bestimmt, ob ein Benutzer für E9-1-1 aktiviert ist, und wenn ja, was das Verhalten eines Notrufs ist.</span><span class="sxs-lookup"><span data-stu-id="aab41-107">The location policy determines whether a user is enabled for E9-1-1, and if so what the behavior is of an emergency call.</span></span> <span data-ttu-id="aab41-108">So können Sie beispielsweise mithilfe der ortungsrichtlinie definieren, welche Nummer ein Notruf ist (beispielsweise 911 in den USA), ob die Unternehmenssicherheit automatisch benachrichtigt werden soll und wie der Anruf weitergeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="aab41-108">For example, you can use the location policy to define what number constitutes an emergency call (for example, 911 in the United States), whether corporate security should be automatically notified, and how the call should be routed.</span></span>

<span data-ttu-id="aab41-109">Sie können Standortrichtlinien über die Gruppe **Netzwerkkonfiguration** in der lync Server 2013-Systemsteuerung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="aab41-109">You can configure location policies from the **Network Configuration** group in Lync Server 2013 Control Panel.</span></span> <span data-ttu-id="aab41-110">In der lync Server-Systemsteuerung können Sie Positions Richtlinien anzeigen, erstellen, ändern oder löschen.</span><span class="sxs-lookup"><span data-stu-id="aab41-110">From Lync Server Control Panel you can view, create, modify, or delete location policies.</span></span> <span data-ttu-id="aab41-111">Gehen Sie wie folgt vor, um Informationen zu Standortrichtlinien anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="aab41-111">Use the following procedure to view information about location policies.</span></span> <span data-ttu-id="aab41-112">Details zum Erstellen oder Ändern von Standortrichtlinien finden Sie unter [erstellen oder Ändern einer Standortrichtlinie in lync Server 2013](lync-server-2013-creating-or-modifying-a-location-policy.md).</span><span class="sxs-lookup"><span data-stu-id="aab41-112">For details on creating or modifying location policies, see [Creating or modifying a location policy in Lync Server 2013](lync-server-2013-creating-or-modifying-a-location-policy.md).</span></span>

<div>

## <a name="to-view-information-about-a-location-policy"></a><span data-ttu-id="aab41-113">So zeigen Sie Informationen zu einer Standortrichtlinie an</span><span class="sxs-lookup"><span data-stu-id="aab41-113">To view information about a location policy</span></span>

1.  <span data-ttu-id="aab41-114">Melden Sie sich mit einem Benutzerkonto, das Mitglied der Gruppe "RTCUniversalServerAdmins" ist (oder über gleichwertige Benutzerrechte verfügt) oder dem die Rolle "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="aab41-114">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or is assigned to the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="aab41-115">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="aab41-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="aab41-116">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="aab41-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="aab41-117">Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration** , und klicken Sie dann auf **ortungsrichtlinie**.</span><span class="sxs-lookup"><span data-stu-id="aab41-117">In the left navigation bar, click **Network Configuration** and then click **Location Policy**.</span></span>

4.  <span data-ttu-id="aab41-118">Wählen Sie auf der Seite **Standortrichtlinie** die zu ändernde Standortrichtlinie aus.</span><span class="sxs-lookup"><span data-stu-id="aab41-118">On the **Location Policy** page, select the location policy that you want to modify.</span></span>

5.  <span data-ttu-id="aab41-119">Klicken Sie im Menü **Bearbeiten** auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="aab41-119">On the **Edit** menu, click **Show details**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="aab41-120">Sie können nur Informationen zu einer Standortrichtlinie gleichzeitig anzeigen.</span><span class="sxs-lookup"><span data-stu-id="aab41-120">You can only view information about one location policy at a time.</span></span>

    
    </div>

<span data-ttu-id="aab41-121">Eine einzelne Richtlinie namens "Global" ist standardmäßig vorhanden und kann nicht gelöscht oder umbenannt werden.</span><span class="sxs-lookup"><span data-stu-id="aab41-121">A single policy, called Global, exists by default and cannot be deleted or renamed.</span></span> <span data-ttu-id="aab41-122">Sie können jedoch die globale Richtlinie ändern.</span><span class="sxs-lookup"><span data-stu-id="aab41-122">However, you can modify the Global policy.</span></span> <span data-ttu-id="aab41-123">Diese Richtlinie gilt für alle Benutzer und Kontakte, es sei denn, Sie erstellen Website Richtlinien oder Richtlinien für einzelne Benutzer.</span><span class="sxs-lookup"><span data-stu-id="aab41-123">This policy will apply to all users and contacts, unless you create site policies or per-user policies.</span></span> <span data-ttu-id="aab41-124">Richtlinien für einzelne Benutzer müssen auf bestimmte Benutzer angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="aab41-124">Per-user policies must be applied to specific users.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="aab41-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aab41-125">See Also</span></span>


[<span data-ttu-id="aab41-126">Erstellen oder Ändern einer Standortrichtlinie in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aab41-126">Creating or modifying a location policy in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-a-location-policy.md)  
[<span data-ttu-id="aab41-127">Erstellen von Standortrichtlinien in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aab41-127">Create location policies in Lync Server 2013</span></span>](lync-server-2013-create-location-policies.md)  
[<span data-ttu-id="aab41-128">Erstellen oder Ändern eines Netzwerkstandorts in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="aab41-128">Create or modify a network site in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-site.md)  


[<span data-ttu-id="aab41-129">Neu – CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="aab41-129">New-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsLocationPolicy)  
[<span data-ttu-id="aab41-130">Satz-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="aab41-130">Set-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsLocationPolicy)  
[<span data-ttu-id="aab41-131">Remove-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="aab41-131">Remove-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsLocationPolicy)  
[<span data-ttu-id="aab41-132">Get-CsLocationPolicy</span><span class="sxs-lookup"><span data-stu-id="aab41-132">Get-CsLocationPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsLocationPolicy)  
  

<span data-ttu-id="aab41-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="aab41-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

