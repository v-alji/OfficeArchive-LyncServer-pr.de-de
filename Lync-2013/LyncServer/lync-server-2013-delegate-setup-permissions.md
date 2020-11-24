---
title: 'Lync Server 2013: Delegieren von Setupberechtigungen'
description: 'Lync Server 2013: Delegieren von Setup Berechtigungen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delegate setup permissions
ms:assetid: 9dca1683-4c69-4534-8ebe-6bd635cbae49
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412735(v=OCS.15)
ms:contentKeyID: 48184997
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a7038cf729bad459dbcd2a84a308b14aa56b68dd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394015"
---
# <a name="delegate-setup-permissions-in-lync-server-2013"></a><span data-ttu-id="f0db7-103">Delegieren von Setupberechtigungen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f0db7-103">Delegate setup permissions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f0db7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f0db7-104">

<span> </span></span></span>

<span data-ttu-id="f0db7-105">_**Letztes Änderungsdatum des Themas:** 2014-02-05_</span><span class="sxs-lookup"><span data-stu-id="f0db7-105">_**Topic Last Modified:** 2014-02-05_</span></span>

<span data-ttu-id="f0db7-106">Wenn Sie Benutzern oder Gruppen, die lync Server 2013 bereitstellen, keine Mitgliedschaft in der Gruppe der Domänenadministratoren gewähren möchten, können Sie Mitgliedern der RTCUniversalServerAdmins-Gruppe das Ausführen des Windows PowerShell **-Cmdlets Enable-CsTopology** auf Servern mit lync Server 2013 ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f0db7-106">If you do not want to grant membership in the Domain Admins group to users or groups who are deploying Lync Server 2013, you can enable members of the RTCUniversalServerAdmins group to run the **Enable-CsTopology** Windows PowerShell cmdlet on servers running Lync Server 2013.</span></span> <span data-ttu-id="f0db7-107">Standardmäßig verfügen Mitglieder der RTCUniversalServerAdmins-Gruppe nicht über die Möglichkeit zum Ausführen dieses Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="f0db7-107">By default, members of the RTCUniversalServerAdmins group do not have the ability to run this cmdlet.</span></span> <span data-ttu-id="f0db7-108">Sie erteilen Administratorrechte und Berechtigungen zum Ausführen von **enable-CsTopology** auf Servern mit lync Server mithilfe des Cmdlets **Grant-CsSetupPermission** und Angeben einer Organisationseinheit, in der Computerobjekte für den Server mit lync Server 2013 gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="f0db7-108">You grant administrator rights and permissions to run **Enable-CsTopology** on servers running Lync Server by using the **Grant-CsSetupPermission** cmdlet and specifying an organizational unit (OU) where computer objects for the server running Lync Server 2013 are located.</span></span>

<span data-ttu-id="f0db7-109">Bei der Domänenvorbereitung, die bei der Installation von lync Server erfolgt, werden nicht automatisch die Berechtigungen hinzugefügt, die Mitgliedern der RTCUniversalServerAdmins-Gruppe das Ausführen des Enable-CsTopology-Cmdlets ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="f0db7-109">The domain preparation that takes place when you install Lync Server does not automatically add the permissions that enable members of the RTCUniversalServerAdmins group to run the Enable-CsTopology cmdlet.</span></span> <span data-ttu-id="f0db7-110">Das bedeutet, dass Sie standardmäßig ein Domänenadministrator sein müssen, um eine Topologie zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="f0db7-110">That means that, by default, you must be a domain administrator in order to enable a topology.</span></span> <span data-ttu-id="f0db7-111">Um Mitgliedern der RTCUniversalServerAdmins-Gruppe das Recht zu geben, eine Topologie zu aktivieren, müssen Sie das Grant-CsSetupPermissions-Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="f0db7-111">To give members of the RTCUniversalServerAdmins group the right to enable a topology you must run the Grant-CsSetupPermissions cmdlet.</span></span> <span data-ttu-id="f0db7-112">Darüber hinaus müssen Sie dieses Cmdlet für jeden Active Directory-Container ausführen, auf dem Computer mit lync Server ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="f0db7-112">In addition, you will need to run this cmdlet against each Active Directory container that houses computers running Lync Server.</span></span>

<span data-ttu-id="f0db7-113">Beachten Sie, dass dieses Cmdlet nur der RTCUniversalServerAdmins-Gruppe Berechtigungen gewährt. das Cmdlet kann nicht verwendet werden, um anderen Sicherheitsgruppen oder einzelnen Benutzern Berechtigungen zu gewähren.</span><span class="sxs-lookup"><span data-stu-id="f0db7-113">Keep in mind that this cmdlet only grants permissions to the RTCUniversalServerAdmins group; the cmdlet cannot be used to grant permissions to other security groups or to individual users.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f0db7-114"><STRONG>Enable-CsTopology</STRONG> ist das Schlüssel-Cmdlet, das es den RTCUniversalServerAdmins-Gruppenmitgliedern ermöglicht, lync Server 2013 einzurichten und bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="f0db7-114"><STRONG>Enable-CsTopology</STRONG> is the key cmdlet to allow the RTCUniversalServerAdmins group members to set up and deploy Lync Server 2013.</span></span>



</div>

<div>

## <a name="to-add-the-ability-to-run-enable-cstopology-to-the-rtcuniversalserveradmins-group"></a><span data-ttu-id="f0db7-115">So fügen Sie die Möglichkeit hinzu, Enable-CsTopology zur RTCUniversalServerAdmins-Gruppe zu führen</span><span class="sxs-lookup"><span data-stu-id="f0db7-115">To add the ability to run Enable-CsTopology to the RTCUniversalServerAdmins group</span></span>

1.  <span data-ttu-id="f0db7-116">Melden Sie sich bei einem Server als Mitglied der Gruppe der Domänenadministratoren für die Domäne an, auf der der Delegierte Benutzer **enable-CsTopology** ausführen soll.</span><span class="sxs-lookup"><span data-stu-id="f0db7-116">Log on to a server as a member of the Domain Admins group for the domain on which the delegated user will run **Enable-CsTopology**.</span></span>

2.  <span data-ttu-id="f0db7-117">Öffnen Sie die lync Server 2013-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="f0db7-117">Open the Lync Server 2013 Management Shell.</span></span> <span data-ttu-id="f0db7-118">Die lync Server 2013-Verwaltungsshell wird automatisch auf jedem Front-End-Server oder auf jedem Computer installiert, auf dem die lync Server 2013-Verwaltungstools installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="f0db7-118">The Lync Server 2013 Management Shell is automatically installed on each Front End Server or any computer where the Lync Server 2013 administrative tools have been installed.</span></span> <span data-ttu-id="f0db7-119">Details zur lync Server 2013-Verwaltungsshell finden Sie unter [lync Server 2013-Verwaltungsshell](lync-server-2013-lync-server-management-shell.md) in der Betriebsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="f0db7-119">For details about the Lync Server 2013 Management Shell, see [Lync Server 2013 Management Shell](lync-server-2013-lync-server-management-shell.md) in the Operations documentation.</span></span>

3.  <span data-ttu-id="f0db7-120">Führen Sie das folgende Cmdlet aus der lync Server 2013-Verwaltungsshell aus:</span><span class="sxs-lookup"><span data-stu-id="f0db7-120">Run the following cmdlet from the Lync Server 2013 Management Shell:</span></span>
    
        Grant-CsSetupPermission -ComputerOU <DN of the OU> -Domain <Domain FQDN>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="f0db7-121">Wenn die Organisationseinheit nicht oberste Ebene ist, müssen Sie den vollständigen Domänennamen angeben.</span><span class="sxs-lookup"><span data-stu-id="f0db7-121">If the OU is not top level, you must provide the full domain name.</span></span>

    
    </div>
    
    <span data-ttu-id="f0db7-122">Im folgenden Beispiel ist die OU "lync Servers", die sich in der contoso.com-Domäne befindet.</span><span class="sxs-lookup"><span data-stu-id="f0db7-122">In the following example, the OU is “Lync Servers,” which is in the contoso.com domain.</span></span>
    
        Grant-CsSetupPermission -ComputerOU "OU=Lync Servers" -Domain contoso.com

<span data-ttu-id="f0db7-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f0db7-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

