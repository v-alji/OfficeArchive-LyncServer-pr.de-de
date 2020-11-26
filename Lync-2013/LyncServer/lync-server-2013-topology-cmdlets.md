---
title: 'Lync Server 2013: Topologie-Cmdlets'
description: 'Lync Server 2013: Topologie-Cmdlets.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Topology cmdlets
ms:assetid: 3ed739a7-d58d-475d-8240-fa8d2c6dc7e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg415648(v=OCS.15)
ms:contentKeyID: 48183942
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7f77febaa3beb4acc25bc5bc54dd0d5585fe18fc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444140"
---
# <a name="topology-cmdlets-jn-lync-server-2013"></a><span data-ttu-id="85bce-103">Topologie-Cmdlets Jn lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="85bce-103">Topology cmdlets jn Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="85bce-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="85bce-104">

<span> </span></span></span>

<span data-ttu-id="85bce-105">_**Letztes Änderungsdatum des Themas:** 2012-06-20_</span><span class="sxs-lookup"><span data-stu-id="85bce-105">_**Topic Last Modified:** 2012-06-20_</span></span>

<span data-ttu-id="85bce-106">Viele der in Microsoft lync Server 2013 enthaltenen Topologie-Cmdlets sind für die Verwendung mit dem Setup-und Topologie-Generator konzipiert. aus diesem Grund gibt es eine Reihe von Topologie-Cmdlets, die von Administratoren nur selten direkt aufgerufen werden.</span><span class="sxs-lookup"><span data-stu-id="85bce-106">Many of the topology cmdlets included in Microsoft Lync Server 2013 are designed for use with Setup and Topology Builder; because of that, there are a number of topology cmdlets that administrators will rarely call directly.</span></span> <span data-ttu-id="85bce-107">Es gibt jedoch Situationen, in denen Administratoren verpflichtet werden, diese Cmdlets zu verwenden. Nachdem Sie beispielsweise neue Kerberos-Konten erstellt haben, müssen Sie das Cmdlet [enable-CsTopology](https://technet.microsoft.com/library/Gg398398(v=OCS.15)) ausführen, damit die Änderungen wirksam werden.</span><span class="sxs-lookup"><span data-stu-id="85bce-107">However, there will be times when administrators will be required to use these cmdlets; for example, after creating new Kerberos accounts you must run the [Enable-CsTopology](https://technet.microsoft.com/library/Gg398398(v=OCS.15)) cmdlet to cause the changes to take effect.</span></span> <span data-ttu-id="85bce-108">Darüber hinaus werden Administratoren wahrscheinlich Cmdlets wie [Test-CsTopology](https://technet.microsoft.com/library/Gg398127(v=OCS.15)) und [Test-CsComputer](https://technet.microsoft.com/library/Gg398162(v=OCS.15)) ausführen, um sicherzustellen, dass lync Server 2013 ordnungsgemäß installiert wurde und wie erwartet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="85bce-108">In addition, administrators will likely run cmdlets such as [Test-CsTopology](https://technet.microsoft.com/library/Gg398127(v=OCS.15)) and [Test-CsComputer](https://technet.microsoft.com/library/Gg398162(v=OCS.15)) to help ensure that Lync Server 2013 has been correctly installed and is working as expected.</span></span>

<div>

## <a name="topology-cmdlets"></a><span data-ttu-id="85bce-109">Topologie-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="85bce-109">Topology Cmdlets</span></span>

<span data-ttu-id="85bce-110">Die folgende Liste enthält Cmdlets, die sich direkt auf die Verwaltung Ihrer lync Server-Topologie beziehen:</span><span class="sxs-lookup"><span data-stu-id="85bce-110">The following is a list of cmdlets that relate directly managing your Lync Server topology:</span></span>

<span data-ttu-id="85bce-111">**Topologie**</span><span class="sxs-lookup"><span data-stu-id="85bce-111">**Topology**</span></span>

  - <span></span>  
    <span data-ttu-id="85bce-112">[Get-CsPool](https://technet.microsoft.com/library/Gg398992(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85bce-112">[Get-CsPool](https://technet.microsoft.com/library/Gg398992(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="85bce-113">[Get-CsSite](https://technet.microsoft.com/library/Gg398185(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85bce-113">[Get-CsSite](https://technet.microsoft.com/library/Gg398185(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="85bce-114">[Satz-CsSite](https://technet.microsoft.com/library/Gg413023(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85bce-114">[Set-CsSite](https://technet.microsoft.com/library/Gg413023(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="85bce-115">[Enable-CsTopology](https://technet.microsoft.com/library/Gg398398(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85bce-115">[Enable-CsTopology](https://technet.microsoft.com/library/Gg398398(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="85bce-116">[Get-CsTopology](https://technet.microsoft.com/library/Gg412824(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85bce-116">[Get-CsTopology](https://technet.microsoft.com/library/Gg412824(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="85bce-117">[Publish-CsTopology](https://technet.microsoft.com/library/Gg398953(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85bce-117">[Publish-CsTopology](https://technet.microsoft.com/library/Gg398953(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="85bce-118">[Test-CsTopology](https://technet.microsoft.com/library/Gg398127(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85bce-118">[Test-CsTopology](https://technet.microsoft.com/library/Gg398127(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="85bce-119">[Export-CsConfiguration](https://technet.microsoft.com/library/Gg398627(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85bce-119">[Export-CsConfiguration](https://technet.microsoft.com/library/Gg398627(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="85bce-120">[Importieren-CsConfiguration](https://technet.microsoft.com/library/Gg398800(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85bce-120">[Import-CsConfiguration](https://technet.microsoft.com/library/Gg398800(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="85bce-121">[Get-CsServerVersion](https://technet.microsoft.com/library/Gg398470(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85bce-121">[Get-CsServerVersion](https://technet.microsoft.com/library/Gg398470(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="85bce-122">[Deaktivieren-CsComputer](https://technet.microsoft.com/library/Gg399023(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85bce-122">[Disable-CsComputer](https://technet.microsoft.com/library/Gg399023(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="85bce-123">[Enable-CsComputer](https://technet.microsoft.com/library/Gg412815(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85bce-123">[Enable-CsComputer](https://technet.microsoft.com/library/Gg412815(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="85bce-124">[Get-CsComputer](https://technet.microsoft.com/library/Gg425959(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85bce-124">[Get-CsComputer](https://technet.microsoft.com/library/Gg425959(v=OCS.15))</span></span>

  - <span></span>  
    <span data-ttu-id="85bce-125">[Test-CsComputer](https://technet.microsoft.com/library/Gg398162(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85bce-125">[Test-CsComputer](https://technet.microsoft.com/library/Gg398162(v=OCS.15))</span></span>

<!-- end list -->

  - <span></span>  
    <span data-ttu-id="85bce-126">[Get-CsNetworkInterface](https://technet.microsoft.com/library/Gg398121(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="85bce-126">[Get-CsNetworkInterface](https://technet.microsoft.com/library/Gg398121(v=OCS.15))</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="85bce-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85bce-127">See Also</span></span>


[<span data-ttu-id="85bce-128">Lync Server PowerShell-Blog</span><span class="sxs-lookup"><span data-stu-id="85bce-128">Lync Server PowerShell Blog</span></span>](https://go.microsoft.com/fwlink/p/?linkid=203150)  
  

<span data-ttu-id="85bce-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="85bce-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

