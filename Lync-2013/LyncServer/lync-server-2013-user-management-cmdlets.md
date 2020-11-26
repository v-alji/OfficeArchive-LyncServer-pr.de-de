---
title: 'Lync Server 2013: Cmdlets für die Benutzerverwaltung'
description: 'Lync Server 2013: Cmdlets für die Benutzerverwaltung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User management cmdlets
ms:assetid: 85312f3f-28e8-421c-b94c-e6ead1f5f755
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398677(v=OCS.15)
ms:contentKeyID: 48184702
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b94f2b48017fd29fa7a5a814da8a3c80d8f57968
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440773"
---
# <a name="user-management-cmdlets-in-lync-server-2013"></a><span data-ttu-id="0538b-103">Cmdlets für die Benutzerverwaltung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0538b-103">User management cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0538b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0538b-104">

<span> </span></span></span>

<span data-ttu-id="0538b-105">_**Letztes Änderungsdatum des Themas:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="0538b-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="0538b-106">Die in Microsoft lync Server 2013 enthaltenen Cmdlets für die Benutzerverwaltung ermöglichen es Ihnen, lync Server-Benutzerkonten zu aktivieren, zu deaktivieren und zu ändern.</span><span class="sxs-lookup"><span data-stu-id="0538b-106">The user management cmdlets included in Microsoft Lync Server 2013 allow you to enable, disable, and modify Lync Server user accounts.</span></span>

<div>

## <a name="user-management-cmdlets"></a><span data-ttu-id="0538b-107">Cmdlets für die Benutzerverwaltung</span><span class="sxs-lookup"><span data-stu-id="0538b-107">User Management Cmdlets</span></span>

<span data-ttu-id="0538b-108">Die meisten Verwaltungsaufgaben, die für Benutzer und Benutzerkonten gelten, können über die lync Server-Systemsteuerung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0538b-108">Most management tasks that apply to users and user accounts can be performed from the Lync Server Control Panel.</span></span> <span data-ttu-id="0538b-109">Die wichtigsten Ausnahmen sind die Cmdlets, die sich mit Audiokonferenz-Anbietern befassen.</span><span class="sxs-lookup"><span data-stu-id="0538b-109">The primary exceptions are the cmdlets that deal with audio conferencing providers.</span></span> <span data-ttu-id="0538b-110">Benutzer Verwaltungsaufgaben können mithilfe von Cmdlets aus der lync Server-Verwaltungsshell oder in einem Skript ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="0538b-110">User management tasks can be performed using cmdlets from the Lync Server Management Shell or from within a script.</span></span> <span data-ttu-id="0538b-111">Mithilfe eines Skripts können Sie bestimmte Aufgaben automatisieren.</span><span class="sxs-lookup"><span data-stu-id="0538b-111">By using a script, you can automate certain tasks.</span></span> <span data-ttu-id="0538b-112">Die folgende Liste enthält Cmdlets, die sich direkt auf die Verwaltung von Benutzern und Benutzerkonten beziehen:</span><span class="sxs-lookup"><span data-stu-id="0538b-112">The following is a list of cmdlets that relate directly to managing users and user accounts:</span></span>

  - <span></span>  
    [<span data-ttu-id="0538b-113">Get-CsAdContact</span><span class="sxs-lookup"><span data-stu-id="0538b-113">Get-CsAdContact</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAdContact)

<!-- end list -->

  - <span></span>  
    [<span data-ttu-id="0538b-114">Get-CsAdUser</span><span class="sxs-lookup"><span data-stu-id="0538b-114">Get-CsAdUser</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsAdUser)

<!-- end list -->

  - [<span data-ttu-id="0538b-115">Get-CsClientAccessLicense</span><span class="sxs-lookup"><span data-stu-id="0538b-115">Get-CsClientAccessLicense</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsClientAccessLicense)

<!-- end list -->

  - [<span data-ttu-id="0538b-116">Get-CsEffectivePolicy</span><span class="sxs-lookup"><span data-stu-id="0538b-116">Get-CsEffectivePolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsEffectivePolicy)

<!-- end list -->

  - [<span data-ttu-id="0538b-117">Invoke-CsUcsRollback</span><span class="sxs-lookup"><span data-stu-id="0538b-117">Invoke-CsUcsRollback</span></span>](https://docs.microsoft.com/powershell/module/skype/Invoke-CsUcsRollback)

<!-- end list -->

  - [<span data-ttu-id="0538b-118">Debug-CsUnifiedContactStore</span><span class="sxs-lookup"><span data-stu-id="0538b-118">Debug-CsUnifiedContactStore</span></span>](https://docs.microsoft.com/powershell/module/skype/Debug-CsUnifiedContactStore)

  - [<span data-ttu-id="0538b-119">Test-CsUnifiedContactStore</span><span class="sxs-lookup"><span data-stu-id="0538b-119">Test-CsUnifiedContactStore</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsUnifiedContactStore)

<!-- end list -->

  - <span></span>  
    [<span data-ttu-id="0538b-120">Deaktivieren-CsUser</span><span class="sxs-lookup"><span data-stu-id="0538b-120">Disable-CsUser</span></span>](https://docs.microsoft.com/powershell/module/skype/Disable-CsUser)

  - <span></span>  
    [<span data-ttu-id="0538b-121">Enable-CsUser</span><span class="sxs-lookup"><span data-stu-id="0538b-121">Enable-CsUser</span></span>](https://docs.microsoft.com/powershell/module/skype/Enable-CsUser)

  - <span></span>  
    [<span data-ttu-id="0538b-122">Get-CsUser</span><span class="sxs-lookup"><span data-stu-id="0538b-122">Get-CsUser</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUser)

  - <span></span>  
    [<span data-ttu-id="0538b-123">Verschieben-CsUser</span><span class="sxs-lookup"><span data-stu-id="0538b-123">Move-CsUser</span></span>](https://docs.microsoft.com/powershell/module/skype/Move-CsUser)

  - <span></span>  
    [<span data-ttu-id="0538b-124">Satz-CsUser</span><span class="sxs-lookup"><span data-stu-id="0538b-124">Set-CsUser</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsUser)

<!-- end list -->

  - <span></span>  
    [<span data-ttu-id="0538b-125">Get-CsUserAcp</span><span class="sxs-lookup"><span data-stu-id="0538b-125">Get-CsUserAcp</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUserAcp)

  - <span></span>  
    [<span data-ttu-id="0538b-126">Remove-CsUserAcp</span><span class="sxs-lookup"><span data-stu-id="0538b-126">Remove-CsUserAcp</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsUserAcp)

  - <span></span>  
    [<span data-ttu-id="0538b-127">Set-CsUserAcp</span><span class="sxs-lookup"><span data-stu-id="0538b-127">Set-CsUserAcp</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsUserAcp)

  - <span></span>  
    [<span data-ttu-id="0538b-128">Test-CsAudioConferencingProvider</span><span class="sxs-lookup"><span data-stu-id="0538b-128">Test-CsAudioConferencingProvider</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsAudioConferencingProvider)

<!-- end list -->

  - <span></span>  
    [<span data-ttu-id="0538b-129">Get-CsUserPoolInfo</span><span class="sxs-lookup"><span data-stu-id="0538b-129">Get-CsUserPoolInfo</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUserPoolInfo)

<!-- end list -->

  - [<span data-ttu-id="0538b-130">Get-CsUserServicesPolicy</span><span class="sxs-lookup"><span data-stu-id="0538b-130">Get-CsUserServicesPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Get-CsUserServicesPolicy)

  - [<span data-ttu-id="0538b-131">Grant-CsUserServicesPolicy</span><span class="sxs-lookup"><span data-stu-id="0538b-131">Grant-CsUserServicesPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Grant-CsUserServicesPolicy)

  - [<span data-ttu-id="0538b-132">New-CsUserServicesPolicy</span><span class="sxs-lookup"><span data-stu-id="0538b-132">New-CsUserServicesPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/New-CsUserServicesPolicy)

  - [<span data-ttu-id="0538b-133">Remove-CsUserServicesPolicy</span><span class="sxs-lookup"><span data-stu-id="0538b-133">Remove-CsUserServicesPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Remove-CsUserServicesPolicy)

  - [<span data-ttu-id="0538b-134">Set-CsUserServicesPolicy</span><span class="sxs-lookup"><span data-stu-id="0538b-134">Set-CsUserServicesPolicy</span></span>](https://docs.microsoft.com/powershell/module/skype/Set-CsUserServicesPolicy)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0538b-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0538b-135">See Also</span></span>


[<span data-ttu-id="0538b-136">Lync Server PowerShell-Blog</span><span class="sxs-lookup"><span data-stu-id="0538b-136">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="0538b-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0538b-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

