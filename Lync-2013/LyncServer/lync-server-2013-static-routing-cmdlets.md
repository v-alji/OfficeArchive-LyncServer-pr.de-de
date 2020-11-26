---
title: 'Lync Server 2013: statische Routing-Cmdlets'
description: 'Lync Server 2013: statische Routing-Cmdlets.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Static routing cmdlets
ms:assetid: 71d5e0cd-8412-4383-818a-95b851a4da4b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg416492(v=OCS.15)
ms:contentKeyID: 48184496
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 33fd251f63111cebb9297287252e666a7e10f0e1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423687"
---
# <a name="static-routing-cmdlets-in-lync-server-2013"></a><span data-ttu-id="6b422-103">Statische Routing-Cmdlets in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6b422-103">Static routing cmdlets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6b422-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6b422-104">

<span> </span></span></span>

<span data-ttu-id="6b422-105">_**Letztes Änderungsdatum des Themas:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="6b422-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="6b422-106">Bei statischen Routen können Administratoren die von SIP-Nachrichten getroffenen Netzwerkrouten vorbestimmen.</span><span class="sxs-lookup"><span data-stu-id="6b422-106">With static routes, administrators can predetermine the network routes taken by SIP messages.</span></span> <span data-ttu-id="6b422-107">Wenn eine Nachricht von einem Server empfangen wird, überprüft der Server die Nachrichtenadresse und leitet die Nachricht dann an den von einem Administrator vorkonfigurierten Next Hop-Server weiter.</span><span class="sxs-lookup"><span data-stu-id="6b422-107">When a message is received by a server, the server checks the message address and then forwards the message to the next hop server preconfigured by an administrator.</span></span> <span data-ttu-id="6b422-108">Wenn Sie ordnungsgemäß konfiguriert sind, können mithilfe statischer Routen rechtzeitig und genau die Zustellung von Nachrichten gewährleistet werden, und es werden nur minimale belauschte auf Servern bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6b422-108">If configured correctly, static routes help ensure timely, and accurate, delivery of messages, and with minimal overheard placed on servers.</span></span>

<div>

## <a name="static-routing-cmdlets"></a><span data-ttu-id="6b422-109">Statische Routing-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="6b422-109">Static Routing Cmdlets</span></span>

<span data-ttu-id="6b422-110">Sofern nicht anderweitig vom Microsoft-Supportpersonal angewiesen, sollten statische Routen, die für Microsoft lync Server 2013 konfiguriert sind, mithilfe des Cmdlets [New-CsStaticRoute](https://technet.microsoft.com/library/Gg398265(v=OCS.15)) erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="6b422-110">Unless otherwise instructed by Microsoft support personnel, static routes configured for Microsoft Lync Server 2013 should be created using the [New-CsStaticRoute](https://technet.microsoft.com/library/Gg398265(v=OCS.15)) cmdlet.</span></span> <span data-ttu-id="6b422-111">Nachdem eine Route erstellt wurde, können Sie diese Route mithilfe der CsStaticRoutingConfiguration-Cmdlets zu einer statischen Routing Sammlung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6b422-111">After a route has been created, you can then use the CsStaticRoutingConfiguration cmdlets to add that route to a static routing collection.</span></span>

<span data-ttu-id="6b422-112">**Statisches Routing**</span><span class="sxs-lookup"><span data-stu-id="6b422-112">**Static Routing**</span></span>

  - <span></span>  
    <span data-ttu-id="6b422-113">[Get-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg398130(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6b422-113">[Get-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg398130(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="6b422-114">[New-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg413041(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6b422-114">[New-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg413041(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="6b422-115">[Remove-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg412932(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6b422-115">[Remove-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg412932(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="6b422-116">[Set-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg425895(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6b422-116">[Set-CsSipResponseCodeTranslationRule](https://technet.microsoft.com/library/Gg425895(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="6b422-117">[New-CsStaticRoute](https://technet.microsoft.com/library/Gg398265(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6b422-117">[New-CsStaticRoute](https://technet.microsoft.com/library/Gg398265(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="6b422-118">[Get-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398754(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6b422-118">[Get-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398754(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="6b422-119">[Neu – CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg425811(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6b422-119">[New-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg425811(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="6b422-120">[Remove-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398668(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6b422-120">[Remove-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398668(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="6b422-121">[Satz-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398724(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6b422-121">[Set-CsStaticRoutingConfiguration](https://technet.microsoft.com/library/Gg398724(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="6b422-122">[Neu – CsSipProxyCustom](https://technet.microsoft.com/library/Gg425904(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6b422-122">[New-CsSipProxyCustom](https://technet.microsoft.com/library/Gg425904(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="6b422-123">[Neu – CsSipProxyRealm](https://technet.microsoft.com/library/Gg413084(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6b422-123">[New-CsSipProxyRealm](https://technet.microsoft.com/library/Gg413084(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="6b422-124">[Neu – CsSipProxyTCP](https://technet.microsoft.com/library/Gg425745(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6b422-124">[New-CsSipProxyTCP](https://technet.microsoft.com/library/Gg425745(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="6b422-125">[Neu – CsSipProxyTLS](https://technet.microsoft.com/library/Gg398629(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6b422-125">[New-CsSipProxyTLS](https://technet.microsoft.com/library/Gg398629(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="6b422-126">[Neu – CsSipProxyTransport](https://technet.microsoft.com/library/Gg398489(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6b422-126">[New-CsSipProxyTransport](https://technet.microsoft.com/library/Gg398489(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="6b422-127">[Neu – CsSipProxyUseDefault](https://technet.microsoft.com/library/Gg398274(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6b422-127">[New-CsSipProxyUseDefault](https://technet.microsoft.com/library/Gg398274(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="6b422-128">[Neu – CsSipProxyUseDefaultCert](https://technet.microsoft.com/library/Gg425858(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6b422-128">[New-CsSipProxyUseDefaultCert](https://technet.microsoft.com/library/Gg425858(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="6b422-129">[Neu – CsIssuedCertId](https://technet.microsoft.com/library/Gg425814(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="6b422-129">[New-CsIssuedCertId](https://technet.microsoft.com/library/Gg425814(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="6b422-130">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="6b422-130">See Also</span></span>


[<span data-ttu-id="6b422-131">Lync Server PowerShell-Blog</span><span class="sxs-lookup"><span data-stu-id="6b422-131">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="6b422-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6b422-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

