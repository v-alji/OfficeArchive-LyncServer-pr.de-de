---
title: 'Lync Server 2013: Genehmigen einer geräteaktualisierungsregel'
description: 'Lync Server 2013: Genehmigen einer geräteaktualisierungsregel'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Approve a Device Update rule
ms:assetid: 9dbb1c9a-be0f-4e13-9234-05501ab43ac5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994053(v=OCS.15)
ms:contentKeyID: 51803964
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 127d16dad6329e952b9033db07ac2f4a4fe9112c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440563"
---
# <a name="approve-a-device-update-rule-in-lync-server-2013"></a><span data-ttu-id="8ba46-103">Genehmigen einer geräteaktualisierungsregel in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8ba46-103">Approve a Device Update rule in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8ba46-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8ba46-104">

<span> </span></span></span>

<span data-ttu-id="8ba46-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="8ba46-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="8ba46-106">Nachdem Sie eine geräteaktualisierungsregel importiert haben, ist Sie auf Ihren Testgeräten installiert.</span><span class="sxs-lookup"><span data-stu-id="8ba46-106">After you import a device update rule, it’s installed on your test devices.</span></span> <span data-ttu-id="8ba46-107">Wenn die Tests erfolgreich sind und Sie das Update für Ihre Organisation bereitzustellen möchten, genehmigen Sie es entweder mithilfe der lync Server-Systemsteuerung oder Windows PowerShell.</span><span class="sxs-lookup"><span data-stu-id="8ba46-107">If your testing is successful, and you want to roll out the update to your organization, approve it by using either Lync Server Control Panel or Windows PowerShell.</span></span>

<div>

## <a name="to-approve-a-device-update-rule-by-using-lync-server-control-panel"></a><span data-ttu-id="8ba46-108">So genehmigen Sie eine geräteaktualisierungsregel mithilfe der lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="8ba46-108">To approve a device update rule by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="8ba46-109">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="8ba46-109">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="8ba46-110">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8ba46-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="8ba46-111">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="8ba46-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="8ba46-112">Führen Sie auf der Seite **Device Update** eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="8ba46-112">On the **Device Update** page, do one of the following:</span></span>
    
      - <span data-ttu-id="8ba46-113">Wenn Sie eine Regel genehmigen möchten, wählen Sie diese Regel aus.</span><span class="sxs-lookup"><span data-stu-id="8ba46-113">To approve one rule, select that rule.</span></span>
    
      - <span data-ttu-id="8ba46-114">Um alle Regeln zu genehmigen, klicken Sie auf **Bearbeiten** und dann auf **Alle auswählen**.</span><span class="sxs-lookup"><span data-stu-id="8ba46-114">To approve all rules, click **Edit**, and then click **Select All**.</span></span>

4.  <span data-ttu-id="8ba46-115">Klicken Sie auf **Aktion** und dann auf **genehmigen**.</span><span class="sxs-lookup"><span data-stu-id="8ba46-115">Click **Action**, and then click **Approve**.</span></span>

</div>

<div>

## <a name="approving-a-device-update-rule-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="8ba46-116">Genehmigen einer geräteaktualisierungsregel mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8ba46-116">Approving a Device Update Rule by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="8ba46-117">Geräteaktualisierungsregeln können auch mithilfe von Windows PowerShell und dem Cmdlet " **genehmigen-CsDeviceUpdateRule** " genehmigt werden.</span><span class="sxs-lookup"><span data-stu-id="8ba46-117">Device update rules can also be approved by using Windows PowerShell and the **Approve-CsDeviceUpdateRule** cmdlet.</span></span> <span data-ttu-id="8ba46-118">Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="8ba46-118">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="8ba46-119">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="8ba46-119">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>

## <a name="to-approve-a-single-device-update-rule"></a><span data-ttu-id="8ba46-120">So genehmigen Sie eine einzelne geräteaktualisierungsregel</span><span class="sxs-lookup"><span data-stu-id="8ba46-120">To approve a single device update rule</span></span>

  - <span data-ttu-id="8ba46-121">Der folgende Befehl genehmigt die geräteaktualisierungsregel d5ce3c10-2588-420A-82ac-dc2d9b1222ff9, die auf dem Webserver ATL-CS-001.litwareinc.com gefunden wurde:</span><span class="sxs-lookup"><span data-stu-id="8ba46-121">The following command approves the device update rule d5ce3c10-2588-420a-82ac-dc2d9b1222ff9 found on the Web server atl-cs-001.litwareinc.com:</span></span>
    
        Approve-CsDeviceUpdateRule -Identity service:WebServer:atl-cs-001.litwareinc.com/d5ce3c10-2588-420a-82ac-dc2d9b1222ff9

</div>

<div>

## <a name="to-approve-multiple-device-update-rules"></a><span data-ttu-id="8ba46-122">So genehmigen Sie mehrere geräteaktualisierungsregeln</span><span class="sxs-lookup"><span data-stu-id="8ba46-122">To approve multiple device update rules</span></span>

  - <span data-ttu-id="8ba46-123">Dieser Befehl genehmigt alle geräteaktualisierungsregeln für Geräte mit Microsoft-Branding:</span><span class="sxs-lookup"><span data-stu-id="8ba46-123">This command approves all the device update rules for Microsoft-branded devices:</span></span>
    
        Get-CsDeviceUpdateRule | Where-Object {$_.Brand -eq "Microsoft"} | Approve-CsDeviceUpdateRule

</div>

<span data-ttu-id="8ba46-124">Ausführliche Informationen finden Sie im Hilfethema zum Cmdlet " [genehmigen-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Approve-CsDeviceUpdateRule) ".</span><span class="sxs-lookup"><span data-stu-id="8ba46-124">For details, see the Help topic for the [Approve-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Approve-CsDeviceUpdateRule) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8ba46-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8ba46-125">See Also</span></span>


[<span data-ttu-id="8ba46-126">Importieren von geräteaktualisierungsregeln in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8ba46-126">Import Device Update rules in Lync Server 2013</span></span>](lync-server-2013-import-device-update-rules.md)  
[<span data-ttu-id="8ba46-127">Wiederherstellen einer geräteaktualisierungsregel in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8ba46-127">Restore a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-restore-a-device-update-rule.md)  
  

<span data-ttu-id="8ba46-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8ba46-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

