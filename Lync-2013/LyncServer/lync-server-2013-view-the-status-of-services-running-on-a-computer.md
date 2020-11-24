---
title: 'Lync Server 2013: Anzeigen des Status der auf einem Computer ausgeführten Dienste'
description: 'Lync Server 2013: Anzeigen des Status der Dienste, die auf einem Computer ausgeführt werden.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View the status of services running on a computer
ms:assetid: f41918e7-4c02-431e-840a-88a1f36ae499
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182606(v=OCS.15)
ms:contentKeyID: 48185804
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 22aeb13f2beb5d3b0ee5eec8109eceeb14e40213
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394659"
---
# <a name="view-the-status-of-services-running-on-a-computer-in-lync-server-2013"></a><span data-ttu-id="bb7dc-103">Anzeigen des Status der auf einem Computer ausgeführten Dienste in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb7dc-103">View the status of services running on a computer in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bb7dc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bb7dc-104">

<span> </span></span></span>

<span data-ttu-id="bb7dc-105">_**Letztes Änderungsdatum des Themas:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="bb7dc-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="bb7dc-106">Sie können die lync Server 2013-Systemsteuerung verwenden, um alle Dienste anzuzeigen, die auf einem bestimmten Computer in ihrer lync Server-Topologie ausgeführt werden, und den Status jedes Diensts anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="bb7dc-106">You can use Lync Server 2013 Control Panel to view all the services that are running on a specific computer in your Lync Server topology and see the status of each service.</span></span>

<div>

## <a name="to-view-the-status-of-services-running-on-a-computer"></a><span data-ttu-id="bb7dc-107">So zeigen Sie den Status der auf einem Computer ausgeführten Dienste an</span><span class="sxs-lookup"><span data-stu-id="bb7dc-107">To view the status of services running on a computer</span></span>

1.  <span data-ttu-id="bb7dc-108">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="bb7dc-108">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="bb7dc-109">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="bb7dc-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="bb7dc-110">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="bb7dc-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="bb7dc-111">Klicken Sie in der linken Navigationsleiste auf **Topologie**.</span><span class="sxs-lookup"><span data-stu-id="bb7dc-111">In the left navigation bar, click **Topology**.</span></span>

4.  <span data-ttu-id="bb7dc-112">Sortieren oder Durchsuchen Sie auf der **Status** Seite die Liste nach Bedarf, um den Computer zu finden, an dem Sie interessiert sind, und klicken Sie dann auf den Computernamen.</span><span class="sxs-lookup"><span data-stu-id="bb7dc-112">On the **Status** page, sort or search the list, as required, to find the computer you’re interested in, and then click the computer name.</span></span>

5.  <span data-ttu-id="bb7dc-113">Führen Sie einen der folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="bb7dc-113">Do any of the following:</span></span>
    
      - <span data-ttu-id="bb7dc-114">Wenn Sie den aktuellen Status der auf dem Computer ausgeführten Dienste anzeigen möchten, klicken Sie auf **Dienststatus abrufen**.</span><span class="sxs-lookup"><span data-stu-id="bb7dc-114">To see the latest status of services running on the computer, click **Get service status**.</span></span>
    
      - <span data-ttu-id="bb7dc-115">Wenn Sie eine Liste der auf dem Computer ausgeführten Dienste und den Status jedes Diensts anzeigen möchten, klicken Sie auf **Eigenschaften**, und klicken Sie dann auf **Schließen** , um zur Liste zurückzukehren.</span><span class="sxs-lookup"><span data-stu-id="bb7dc-115">To see a list of specific services running on the computer and the status of each service, click **Properties**, and then click **Close** to return to the list.</span></span>

</div>

<div>

## <a name="viewing-service-status-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="bb7dc-116">Anzeigen des Dienst Status mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="bb7dc-116">Viewing Service Status by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="bb7dc-117">Sie können den Dienststatus auch mithilfe von Windows PowerShell und dem Cmdlet **Get-CsWindowsService** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="bb7dc-117">You can also view service status by using Windows PowerShell and the **Get-CsWindowsService** cmdlet.</span></span> <span data-ttu-id="bb7dc-118">Sie können dieses Cmdlet in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="bb7dc-118">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="bb7dc-119">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="bb7dc-119">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-service-status"></a><span data-ttu-id="bb7dc-120">So zeigen Sie den Dienststatus an</span><span class="sxs-lookup"><span data-stu-id="bb7dc-120">To view service status</span></span>

  - <span data-ttu-id="bb7dc-121">Wenn Sie den Dienststatus auf einem Computer anzeigen möchten, geben Sie in der lync Server-Verwaltungsshell einen Befehl ähnlich der folgenden ein, und drücken Sie dann die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="bb7dc-121">To view service status on a computer, type a command similar to the following in the Lync Server Management Shell and then press Enter:</span></span>
    
        Get-CsWindowsService -ComputerName atl-cs-001.litwareinc.com | Select-Object RoleName, Status
    
    <span data-ttu-id="bb7dc-122">Mit diesem Befehl werden Informationen ähnlich der folgenden zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="bb7dc-122">This command returns information similar to the following:</span></span>
    
        RoleName                                  Status
        --------                                  ------
        {W3SVC}                                   Running
        {CentralManagement}                       Running
        {ClsAgent}                                Running
        {Registrar, UserServer, EdgeServer}       Running
        {ApplicationServer}                       Running
        {ConferencingServer}                      Running
        {MediationServer}                         Running

</div>

<span data-ttu-id="bb7dc-123">Ausführliche Informationen finden Sie unter [Get-CsWindowsService](https://docs.microsoft.com/powershell/module/skype/Get-CsWindowsService).</span><span class="sxs-lookup"><span data-stu-id="bb7dc-123">For details, see [Get-CsWindowsService](https://docs.microsoft.com/powershell/module/skype/Get-CsWindowsService).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="bb7dc-124">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bb7dc-124">See Also</span></span>


[<span data-ttu-id="bb7dc-125">Verwalten von Geräten, Telefonen und Clientanwendungen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bb7dc-125">Managing devices, phones, and client applications in Lync Server 2013</span></span>](lync-server-2013-managing-devices-phones-and-client-applications.md)  
  

<span data-ttu-id="bb7dc-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bb7dc-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

