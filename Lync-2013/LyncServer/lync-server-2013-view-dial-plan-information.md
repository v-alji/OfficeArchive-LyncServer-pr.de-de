---
title: 'Lync Server 2013: Anzeigen von Wähl Planinformationen'
description: 'Lync Server 2013: Anzeigen von Wähl Planinformationen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View dial plan information
ms:assetid: 25ed0112-a8a7-418a-8c2c-580081be692a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687997(v=OCS.15)
ms:contentKeyID: 49733587
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b4473302b182b8de4ea6aad12d7993cb5d442b7e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423393"
---
# <a name="view-dial-plan-information-in-lync-server-2013"></a><span data-ttu-id="a2139-103">Anzeigen von Wähl Planinformationen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a2139-103">View dial plan information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a2139-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a2139-104">

<span> </span></span></span>

<span data-ttu-id="a2139-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="a2139-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="a2139-106">Führen Sie die Schritte im folgenden Verfahren aus, um Informationen zu einem vorhandenen Wählplan anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="a2139-106">To view information for an existing dial plan, perform the steps in the following procedure.</span></span> <span data-ttu-id="a2139-107">Wenn Sie einen neuen Wählplan erstellen möchten, lesen Sie [Erstellen eines Wähl Plans in lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span><span class="sxs-lookup"><span data-stu-id="a2139-107">If you want to create a new dial plan, see [Create a dial plan in Lync Server 2013](lync-server-2013-create-a-dial-plan.md).</span></span>

<div>

## <a name="to-view-information-about-a-dial-plan-from-lync-server-control-panel"></a><span data-ttu-id="a2139-108">So zeigen Sie Informationen zu einem Wählplan in der lync Server-Systemsteuerung an</span><span class="sxs-lookup"><span data-stu-id="a2139-108">To view information about a dial plan from Lync Server Control Panel</span></span>

1.  <span data-ttu-id="a2139-109">Melden Sie sich auf dem Computer als Mitglied der Gruppe "RTCUniversalServerAdmins" oder als Benutzer mit der Rolle "CsVoiceAdministrator", "CsServerAdministrator" oder "CsAdministrator" an.</span><span class="sxs-lookup"><span data-stu-id="a2139-109">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="a2139-110">Ausführliche Informationen finden Sie unter [Delegieren von Setup Berechtigungen in lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="a2139-110">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="a2139-111">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="a2139-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="a2139-112">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="a2139-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="a2139-113">Klicken Sie in der linken Navigationsleiste auf **VoIP-Routing** und dann auf **Wählplan**.</span><span class="sxs-lookup"><span data-stu-id="a2139-113">In the left navigation bar, click **Voice Routing** and then click **Dial Plan**.</span></span>

4.  <span data-ttu-id="a2139-114">Doppelklicken Sie auf der Seite **Wähleinstellungen** auf einen Satz mit Wähleinstellungen.</span><span class="sxs-lookup"><span data-stu-id="a2139-114">On the **Dial Plan** page, double-click a dial plan name.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="a2139-115">Sie können Informationen nur für einen Wählplan gleichzeitig anzeigen.</span><span class="sxs-lookup"><span data-stu-id="a2139-115">You can view information for only one dial plan at a time.</span></span>

    
    </div>

</div>

<div>

## <a name="to-view-dial-plans-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="a2139-116">So zeigen Sie Wählpläne mithilfe von Windows PowerShell-Cmdlets an</span><span class="sxs-lookup"><span data-stu-id="a2139-116">To view dial plans by using Windows PowerShell cmdlets</span></span>

  - <span data-ttu-id="a2139-117">Wählpläne können mithilfe der Windows PowerShell-Befehlszeilenschnittstelle und dem Cmdlet **Get-CsDialPlan** angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a2139-117">Dial plans can be viewed by using the Windows PowerShell command-line interface and the **Get-CsDialPlan** cmdlet.</span></span> <span data-ttu-id="a2139-118">Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="a2139-118">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="a2139-119">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="a2139-119">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>
    
    <span data-ttu-id="a2139-120">Wenn Sie Informationen zu allen ihren Wählplänen anzeigen möchten, geben Sie den folgenden Befehl in der lync Server-Verwaltungsshell ein, und drücken Sie dann die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="a2139-120">To view information about all your dial plans, type the following command in the Lync Server Management Shell, and then press ENTER:</span></span>
    
        Get-CsDialPlan
    
    <span data-ttu-id="a2139-121">Dieser Befehl gibt ähnliche Informationen zurück:</span><span class="sxs-lookup"><span data-stu-id="a2139-121">That command will return information similar to this:</span></span>
    
        Identity                 : Global
        Description              :
        DialinConferencingRegion :
        NormalizationRules       : {Description=;
                                   Pattern=^(\d+)$;Translation=$1;Name=
                                   KeepAll;IsInternalExtension=False}
        CountryCode              :
        State                    :
        City                     :
        ExternalAccessPrefix     :
        SimpleName               : DefaultProfile
        OptimizeDeviceDialing    : False

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a2139-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a2139-122">See Also</span></span>


[<span data-ttu-id="a2139-123">Erstellen eines Wählplans in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a2139-123">Create a dial plan in Lync Server 2013</span></span>](lync-server-2013-create-a-dial-plan.md)  
[<span data-ttu-id="a2139-124">Ändern eines Wählplans in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a2139-124">Modify a dial plan in Lync Server 2013</span></span>](lync-server-2013-modify-a-dial-plan.md)  
  

<span data-ttu-id="a2139-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a2139-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

