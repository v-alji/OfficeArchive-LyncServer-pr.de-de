---
title: 'Lync Server 2013: Zurücksetzen einer geräteaktualisierungsregel'
description: 'Lync Server 2013: Zurücksetzen einer geräteaktualisierungsregel'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Reset a Device Update rule
ms:assetid: d1f597e7-dffd-4756-af07-10613a5d8729
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994069(v=OCS.15)
ms:contentKeyID: 51803980
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8a4d42b6aee8f4cb3fd93839b4a8575059ba71cb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49436370"
---
# <a name="reset-a-device-update-rule-in-lync-server-2013"></a><span data-ttu-id="25a9e-103">Zurücksetzen einer geräteaktualisierungsregel in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25a9e-103">Reset a Device Update rule in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="25a9e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="25a9e-104">

<span> </span></span></span>

<span data-ttu-id="25a9e-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="25a9e-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="25a9e-106">Wenn Ihnen die Funktionsweise eines Updates auf Ihren Testgeräten nicht gefällt, können Sie die geräteaktualisierungsregel zurücksetzen, wodurch der Status der Regel ausstehend entfernt und das Update von den Testgeräten deinstalliert wird.</span><span class="sxs-lookup"><span data-stu-id="25a9e-106">If you don’t like the way that an update works on your test devices, you can reset the device update rule, which removes the rule’s pending status and uninstalls the update from the test devices.</span></span>

<span data-ttu-id="25a9e-107">Sie können eine geräteaktualisierungsregel entweder mithilfe der lync Server-Systemsteuerung oder mit Windows PowerShell entfernen.</span><span class="sxs-lookup"><span data-stu-id="25a9e-107">You can remove a device update rule by using either Lync Server Control Panel or Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="25a9e-108">Wenn Sie eine Regel deinstallieren möchten, die Sie bereits genehmigt haben (also ein Rollup durchgeführt haben), stellen Sie Sie wieder her.</span><span class="sxs-lookup"><span data-stu-id="25a9e-108">To uninstall a rule that you’ve already approved (that is, rolled out), restore it.</span></span> <span data-ttu-id="25a9e-109">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-restore-a-device-update-rule.md">Wiederherstellen einer geräteaktualisierungsregel in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="25a9e-109">For details, see <A href="lync-server-2013-restore-a-device-update-rule.md">Restore a Device Update rule in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-reset-a-device-update-rule-by-using-lync-server-control-panel"></a><span data-ttu-id="25a9e-110">So setzen Sie eine geräteaktualisierungsregel mithilfe der lync Server-Systemsteuerung zurück</span><span class="sxs-lookup"><span data-stu-id="25a9e-110">To reset a device update rule by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="25a9e-111">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="25a9e-111">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="25a9e-112">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="25a9e-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="25a9e-113">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="25a9e-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="25a9e-114">Klicken Sie in der linken Navigationsleiste auf **Clients**, und klicken Sie dann auf die Schaltfläche **Geräte Update** -Navigation.</span><span class="sxs-lookup"><span data-stu-id="25a9e-114">In the left navigation bar, click **Clients**, and then click the **Device Update** navigation button.</span></span>

4.  <span data-ttu-id="25a9e-115">Führen Sie auf der Seite **Device Update** eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="25a9e-115">On the **Device Update** page, do one of the following:</span></span>
    
      - <span data-ttu-id="25a9e-116">Um eine Regel zurückzusetzen, wählen Sie die Regel aus, die Sie zurücksetzen möchten.</span><span class="sxs-lookup"><span data-stu-id="25a9e-116">To reset one rule, select the rule you want to reset.</span></span>
    
      - <span data-ttu-id="25a9e-117">Wenn Sie alle Regeln zurücksetzen möchten, klicken Sie im Menü **Bearbeiten** auf **Alles markieren**.</span><span class="sxs-lookup"><span data-stu-id="25a9e-117">To reset all rules, on the **Edit** menu, click **Select All**.</span></span>
    
      - <span data-ttu-id="25a9e-118">Wenn Sie alle Regeln für eine Marke zurücksetzen möchten, verwenden Sie das Menü **Marken** Spalte.</span><span class="sxs-lookup"><span data-stu-id="25a9e-118">To reset all rules for one brand, use the **Brand** column menu.</span></span>

5.  <span data-ttu-id="25a9e-119">Klicken Sie auf **Aktion** und dann auf **ausstehende Updates Abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="25a9e-119">Click **Action**, and then click **Cancel pending updates**.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="25a9e-120">Wenn Sie sicher sind, dass Sie die von Ihnen stornierten geräteaktualisierungsregeln nie aufrollen möchten, sollten Sie Sie möglicherweise löschen.</span><span class="sxs-lookup"><span data-stu-id="25a9e-120">If you’re sure you’ll never want to roll out the device update rule(s) that you cancelled, you might want to delete them.</span></span> <span data-ttu-id="25a9e-121">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-remove-a-device-update-rule.md">Entfernen einer geräteaktualisierungsregel in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="25a9e-121">For details, see <A href="lync-server-2013-remove-a-device-update-rule.md">Remove a Device Update rule in Lync Server 2013</A>.</span></span>

    
    </div>

</div>

<div>

## <a name="resetting-a-device-update-rule-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="25a9e-122">Zurücksetzen einer geräteaktualisierungsregel mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="25a9e-122">Resetting a Device Update Rule by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="25a9e-123">Geräteaktualisierungsregeln können auch mithilfe von Windows PowerShell und dem Cmdlet **Reset-CsDeviceUpdateRule** zurückgesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="25a9e-123">Device update rules can also be reset by using Windows PowerShell and the **Reset-CsDeviceUpdateRule** cmdlet.</span></span> <span data-ttu-id="25a9e-124">Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="25a9e-124">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="25a9e-125">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="25a9e-125">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>

## <a name="to-reset-a-specific-device-update-rule-on-a-server"></a><span data-ttu-id="25a9e-126">So setzen Sie eine bestimmte geräteaktualisierungsregel auf einem Server zurück</span><span class="sxs-lookup"><span data-stu-id="25a9e-126">To reset a specific device update rule on a server</span></span>

  - <span data-ttu-id="25a9e-127">Mit dem folgenden Befehl wird die geräteaktualisierungsregel d5ce3c10-2588-420A-82ac-dc2d9b1222ff9 auf dem Webserver ATL-CS-001.litwareinc.com zurückgesetzt:</span><span class="sxs-lookup"><span data-stu-id="25a9e-127">The following command resets the device update rule d5ce3c10-2588-420a-82ac-dc2d9b1222ff9 on the Web server atl-cs-001.litwareinc.com:</span></span>
    
        Reset-CsDeviceUpdateRule -Identity "service:WebServer:atl-cs-001.litwareinc.com/d5ce3c10-2588-420a-82ac-dc2d9b1222ff9"

</div>

<div>

## <a name="to-reset-all-the-device-update-rules-on-a-server"></a><span data-ttu-id="25a9e-128">So setzen Sie alle geräteaktualisierungsregeln auf einem Server zurück</span><span class="sxs-lookup"><span data-stu-id="25a9e-128">To reset all the device update rules on a server</span></span>

  - <span data-ttu-id="25a9e-129">Mit diesem Befehl werden alle geräteaktualisierungsregeln auf dem Webserver ATL-CS-001.litwareinc.com zurückgesetzt:</span><span class="sxs-lookup"><span data-stu-id="25a9e-129">This command resets all the device update rules on the Web server atl-cs-001.litwareinc.com:</span></span>
    
        Get-CsDeviceUpdateRule -Filter "service:WebServer:atl-cs-001.litwareinc.com*"  | Reset-CsDeviceUpdateRule

</div>

<div>

## <a name="to-reset-all-the-device-updates-rules-that-have-a-specific-brand"></a><span data-ttu-id="25a9e-130">So setzen Sie alle Geräteupdate Regeln mit einer bestimmten Marke zurück</span><span class="sxs-lookup"><span data-stu-id="25a9e-130">To reset all the device updates rules that have a specific brand</span></span>

  - <span data-ttu-id="25a9e-131">In diesem Beispiel werden alle Geräte Updates in der gesamten Organisation, die eine Marke von Microsoft aufweisen, zurückgesetzt:</span><span class="sxs-lookup"><span data-stu-id="25a9e-131">In this example, all the device updates throughout the organization that have a Brand equal to Microsoft are reset:</span></span>
    
        Get-CsDeviceUpdateRule | Where-Object {$_.Brand -eq "Microsoft"} | Reset-CsDeviceUpdateRule

</div>

<span data-ttu-id="25a9e-132">Ausführliche Informationen finden Sie im Hilfethema zum Cmdlet [Reset-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Reset-CsDeviceUpdateRule) .</span><span class="sxs-lookup"><span data-stu-id="25a9e-132">For details, see the Help topic for the [Reset-CsDeviceUpdateRule](https://docs.microsoft.com/powershell/module/skype/Reset-CsDeviceUpdateRule) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="25a9e-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25a9e-133">See Also</span></span>


[<span data-ttu-id="25a9e-134">Genehmigen einer geräteaktualisierungsregel in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25a9e-134">Approve a Device Update rule in Lync Server 2013</span></span>](lync-server-2013-approve-a-device-update-rule.md)  
  

<span data-ttu-id="25a9e-135"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="25a9e-135"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

