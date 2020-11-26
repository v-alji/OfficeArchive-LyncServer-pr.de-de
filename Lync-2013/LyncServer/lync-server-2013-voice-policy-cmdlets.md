---
title: 'Lync Server 2013: VoIP-Richtlinien-Cmdlets'
description: 'Lync Server 2013: VoIP-Richtlinien-Cmdlets.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Voice policy cmdlets
ms:assetid: 92744ec6-754d-498b-b430-dcd5c985ce10
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415663(v=OCS.15)
ms:contentKeyID: 48184800
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 88f87f232ab9922a3e204f11e5231457a867426a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443342"
---
# <a name="voice-policy-cmdlets-in-lync-server-2013"></a><span data-ttu-id="853c5-103">VoIP-Richtlinien-Cmdlets in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="853c5-103">Voice policy cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="853c5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="853c5-104">

<span> </span></span></span>

<span data-ttu-id="853c5-105">_**Letztes Änderungsdatum des Themas:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="853c5-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="853c5-106">Das Verwalten von Enterprise-VoIP umfasst die Konfiguration von VoIP-Richtlinien und Wählplänen sowie das Zuordnen von VoIP-Richtlinien zu VoIP-Routen.</span><span class="sxs-lookup"><span data-stu-id="853c5-106">Managing Enterprise Voice includes configuring such things as voice policies and dial plans, and associating voice policies with voice routes.</span></span> <span data-ttu-id="853c5-107">Cmdlets zum Verwalten von VoIP-Richtlinien können verwendet werden, um Features wie das gleichzeitige Klingeln festzulegen (die Möglichkeit, jedes Mal, wenn jemand Ihr Office-Telefon anruft, ein zweites Telefon klingeln zu lassen), die Anrufweiterleitung und die Wähl Anforderung.</span><span class="sxs-lookup"><span data-stu-id="853c5-107">Cmdlets related to managing voice policies can be used to set features such as simultaneous ringing (the ability to have a second phone ring each time someone calls your office phone), call forwarding, and dialing requirement.</span></span>

<div>

## <a name="voice-policy-cmdlets"></a><span data-ttu-id="853c5-108">VoIP-Richtlinien-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="853c5-108">Voice Policy Cmdlets</span></span>

<span data-ttu-id="853c5-109">Die folgenden Cmdlets können zum Verwalten von VoIP-Richtlinien und Wählplänen für Enterprise-VoIP verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="853c5-109">The following cmdlets can be used to manage voice policies and dial plans for Enterprise Voice.</span></span>

<span data-ttu-id="853c5-110">**VoIP-Richtlinie**</span><span class="sxs-lookup"><span data-stu-id="853c5-110">**Voice Policy**</span></span>

  - <span></span>  
    <span data-ttu-id="853c5-111">[Get-CsDialPlan](https://technet.microsoft.com/library/Gg413043(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="853c5-111">[Get-CsDialPlan](https://technet.microsoft.com/library/Gg413043(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="853c5-112">[Grant-CsDialPlan](https://technet.microsoft.com/library/Gg398547(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="853c5-112">[Grant-CsDialPlan](https://technet.microsoft.com/library/Gg398547(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="853c5-113">[New-CsDialPlan](https://technet.microsoft.com/library/Gg425860(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="853c5-113">[New-CsDialPlan](https://technet.microsoft.com/library/Gg425860(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="853c5-114">[Remove-CsDialPlan](https://technet.microsoft.com/library/Gg398791(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="853c5-114">[Remove-CsDialPlan](https://technet.microsoft.com/library/Gg398791(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="853c5-115">[Set-CsDialPlan](https://technet.microsoft.com/library/Gg398644(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="853c5-115">[Set-CsDialPlan](https://technet.microsoft.com/library/Gg398644(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="853c5-116">[Test-CsDialPlan](https://technet.microsoft.com/library/Gg399024(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="853c5-116">[Test-CsDialPlan](https://technet.microsoft.com/library/Gg399024(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="853c5-117">[Get-CsPstnUsage](https://technet.microsoft.com/library/Gg412734(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="853c5-117">[Get-CsPstnUsage](https://technet.microsoft.com/library/Gg412734(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="853c5-118">[Set-CsPstnUsage](https://technet.microsoft.com/library/Gg399069(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="853c5-118">[Set-CsPstnUsage](https://technet.microsoft.com/library/Gg399069(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="853c5-119">[Get-CsVoicePolicy](https://technet.microsoft.com/library/Gg398101(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="853c5-119">[Get-CsVoicePolicy](https://technet.microsoft.com/library/Gg398101(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="853c5-120">[Grant-CsVoicePolicy](https://technet.microsoft.com/library/Gg398828(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="853c5-120">[Grant-CsVoicePolicy](https://technet.microsoft.com/library/Gg398828(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="853c5-121">[Neu – CsVoicePolicy](https://technet.microsoft.com/library/Gg425856(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="853c5-121">[New-CsVoicePolicy](https://technet.microsoft.com/library/Gg425856(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="853c5-122">[Remove-CsVoicePolicy](https://technet.microsoft.com/library/Gg398309(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="853c5-122">[Remove-CsVoicePolicy](https://technet.microsoft.com/library/Gg398309(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="853c5-123">[Satz-CsVoicePolicy](https://technet.microsoft.com/library/Gg399021(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="853c5-123">[Set-CsVoicePolicy](https://technet.microsoft.com/library/Gg399021(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="853c5-124">[Test-CsVoicePolicy](https://technet.microsoft.com/library/Gg398310(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="853c5-124">[Test-CsVoicePolicy](https://technet.microsoft.com/library/Gg398310(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="853c5-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="853c5-125">See Also</span></span>


[<span data-ttu-id="853c5-126">Enterprise-VoIP-Cmdlets in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="853c5-126">Enterprise Voice cmdlets in Lync Server 2013</span></span>](lync-server-2013-enterprise-voice-cmdlets.md)  


[<span data-ttu-id="853c5-127">Lync Server PowerShell-Blog</span><span class="sxs-lookup"><span data-stu-id="853c5-127">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="853c5-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="853c5-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

