---
title: 'Lync Server 2013: Anzeigen von Netzwerkschnittstelleninformationen'
description: 'Lync Server 2013: Anzeigen von Netzwerkschnittstelleninformationen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Viewing network interface information
ms:assetid: e7dbb1ec-62b3-48be-a419-c493df5740e6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721916(v=OCS.15)
ms:contentKeyID: 49733850
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 12bf844116c048fb8c55e7aac1de46a7dffce4cd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443937"
---
# <a name="viewing-network-interface-information-in-lync-server-2013"></a><span data-ttu-id="87e72-103">Anzeigen von Netzwerkschnittstelleninformationen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="87e72-103">Viewing network interface information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="87e72-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="87e72-104">

<span> </span></span></span>

<span data-ttu-id="87e72-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="87e72-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="87e72-106">Sie können Netzwerkschnittstelleninformationen mithilfe von Windows PowerShell und dem Cmdlet **Get-CsNetworkInterface** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="87e72-106">You can view network interface information by using Windows PowerShell and the **Get-CsNetworkInterface** cmdlet.</span></span> <span data-ttu-id="87e72-107">Sie können dieses Cmdlet in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="87e72-107">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="87e72-108">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="87e72-108">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-network-interface-information"></a><span data-ttu-id="87e72-109">So zeigen Sie Netzwerkschnittstelleninformationen an</span><span class="sxs-lookup"><span data-stu-id="87e72-109">To view network interface information</span></span>

  - <span data-ttu-id="87e72-110">Um Netzwerkschnittstelleninformationen anzuzeigen, geben Sie den folgenden Befehl in der lync Server-Verwaltungsshell ein, und drücken Sie dann die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="87e72-110">To view network interface information, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsNetworkInterface
    
    <span data-ttu-id="87e72-111">Dieser Befehl gibt für jede Netzwerkschnittstelle Informationen ähnlich der folgenden zurück:</span><span class="sxs-lookup"><span data-stu-id="87e72-111">This command returns information similar to the following for each network interface:</span></span>
    
        Identity              : dc.vdomain.com/Primary/1
        ComputerFqdn          : dc.vdomain.com
        IPAddress             : 0.0.0.0
        IPv6Address           :
        Interface             : Primary
        InterfaceNumber       : 1
        ConfiguredFqdn        :
        ConfiguredIPAddress   :
        ConfiguredIPv6Address :
    
    <span data-ttu-id="87e72-112">Ausführliche Informationen finden Sie unter [Get-CsNetworkInterface](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkInterface).</span><span class="sxs-lookup"><span data-stu-id="87e72-112">For details, see [Get-CsNetworkInterface](https://docs.microsoft.com/powershell/module/skype/Get-CsNetworkInterface).</span></span>

<span data-ttu-id="87e72-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="87e72-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

