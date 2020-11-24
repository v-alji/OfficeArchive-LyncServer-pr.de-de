---
title: 'Lync Server 2013: Aktivieren der Anrufdetailaufzeichnung'
description: 'Lync Server 2013: Aktivieren der Anrufdetailaufzeichnung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable call detail recording
ms:assetid: 3b28e432-596f-45a5-a070-577d6fa748d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520980(v=OCS.15)
ms:contentKeyID: 48183865
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8d565c78571e34cead61777381875c9c8d23dae1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394731"
---
# <a name="enable-call-detail-recording-in-lync-server-2013"></a><span data-ttu-id="cde52-103">Aktivieren der Anrufdetailaufzeichnung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cde52-103">Enable call detail recording in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cde52-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cde52-104">

<span> </span></span></span>

<span data-ttu-id="cde52-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="cde52-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="cde52-p101">Bei der Aufzeichnung von Kommunikationsdatensätzen werden Nutzungs- und Diagnoseinformationen über Peer-to-Peer-Aktivitäten aufgezeichnet, z. B. Chat, VoIP-Anrufe (Voice over Internet Protocol), Anwendungsfreigabe, Dateiübertragung und Besprechungen. Anhand der Nutzungsdaten kann die Rendite berechnet werden und die Diagnosedaten können zur Problembehandlung bei Peer-to-Peer-Aktivitäten und Besprechungen eingesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="cde52-p101">Call detail recording (CDR) records usage and diagnostic information about peer-to-peer activities including instance messaging, Voice over Internet Protocol (VoIP) calls, application sharing, file transfer, and meetings. The usage data can be used to calculate return on investment (ROI) and the diagnostic data can be used to troubleshoot peer-to-peer activities and meetings.</span></span>

<span data-ttu-id="cde52-108">Verwenden Sie das folgende Verfahren, um die Aufzeichnung von Kommunikationsdatensätzen (KDS) in der gesamten Organisation oder für jeden Standort in Ihrer Organisation zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cde52-108">Use the following procedure to enable CDR for your whole organization or each site in your organization.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="cde52-109">Zur Aktivierung von KDS müssen Sie die Überwachung und eine Überwachungsdatenbank konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cde52-109">In order to enable CDR you must configure monitoring and a monitoring database.</span></span> <span data-ttu-id="cde52-110">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-deploying-monitoring.md">Bereitstellen der Überwachung in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="cde52-110">For details, see <A href="lync-server-2013-deploying-monitoring.md">Deploying monitoring in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="to-enable-cdr-with-lync-server-control-panel"></a><span data-ttu-id="cde52-111">So aktivieren Sie CDR mit der lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="cde52-111">To enable CDR with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="cde52-112">Melden Sie sich bei einem Benutzerkonto, das ein Mitglied der RTCUniversalServerAdmins-Gruppe ist (oder über entsprechende Benutzerrechte verfügt) oder der CsServerAdministrator-oder CsAdministrator-Rolle zugewiesen ist, bei jedem Computer an, der sich in dem Netzwerk befindet, in dem Sie lync Server 2013 bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="cde52-112">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="cde52-113">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="cde52-113">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="cde52-114">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="cde52-114">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="cde52-115">Klicken Sie in der linken Navigationsleiste auf **Überwachung und Archivierung** und dann auf **Aufzeichnung von Kommunikationsdatensätzen**.</span><span class="sxs-lookup"><span data-stu-id="cde52-115">In the left navigation bar, click **Monitoring and Archiving**, and then click **Call Detail Recording**.</span></span>

4.  <span data-ttu-id="cde52-116">Klicken Sie auf der Seite **Aufzeichnung von Kommunikationsdatensätzen** in der Tabelle auf den geeigneten Standort, klicken Sie auf **Aktion** und anschließend auf **KDS aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="cde52-116">On the **Call Detail Recording** page, click the appropriate site from the table, click **Action**, and then click **Enable CDR**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="cde52-117">KDS ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cde52-117">CDR is enabled by default.</span></span>

    
    </div>

</div>

<div>

## <a name="enabling-cdr-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="cde52-118">Aktivieren von CDR mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="cde52-118">Enabling CDR by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="cde52-119">Sie können CdR mithilfe von Windows PowerShell und dem Cmdlet " **Satz-CsCdrConfiguration** " aktivieren.</span><span class="sxs-lookup"><span data-stu-id="cde52-119">You can enable CDR by using Windows PowerShell and the **Set-CsCdrConfiguration** cmdlet.</span></span> <span data-ttu-id="cde52-120">Sie können dieses Cmdlet entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="cde52-120">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="cde52-121">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="cde52-121">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-cdr-for-a-single-location"></a><span data-ttu-id="cde52-122">So aktivieren Sie KDS für einen einzelnen Standort</span><span class="sxs-lookup"><span data-stu-id="cde52-122">To enable CDR for a single location</span></span>

  - <span data-ttu-id="cde52-123">Sie können KDS aktivieren, indem Sie den Parameter „EnableCDR“ auf „True“ ($True) setzen.</span><span class="sxs-lookup"><span data-stu-id="cde52-123">To disable CDR, set the EnableCDR parameter to True ($True).</span></span>
    
        Set-CsCdrConfiguration -Identity "site:Redmond" -EnableCDR $True

</div>

<div>

## <a name="to-disable-cdr-for-a-single-location"></a><span data-ttu-id="cde52-124">So deaktivieren Sie KDS für einen einzelnen Standort</span><span class="sxs-lookup"><span data-stu-id="cde52-124">To disable CDR for a single location</span></span>

  - <span data-ttu-id="cde52-p105">Sie können KDS deaktivieren, indem Sie den Parameter „EnableCDR“ auf „False“ ($False) setzen. Durch die Deaktivierung von KDS wird die Überwachung nicht deinstalliert, sondern die Sammlung und Speicherung von KDS-Daten angehalten.</span><span class="sxs-lookup"><span data-stu-id="cde52-p105">To disable CDR, set the EnableCDR parameter to False ($False). Disabling CDR does not uninstall monitoring. It pauses the collection and storage of CDR data.</span></span>
    
        Set-CsCdrConfiguration -Identity "site:Redmond" -EnableCDR $False

</div>

<div>

## <a name="to-use-a-single-command-to-enable-cdr-in-multiple-locations"></a><span data-ttu-id="cde52-128">So verwenden Sie einen einzelnen Befehl zum Aktivieren von KDS an mehreren Standorten</span><span class="sxs-lookup"><span data-stu-id="cde52-128">To use a single command to enable CDR in multiple locations</span></span>

  - <span data-ttu-id="cde52-129">Mit diesem Befehl wird KDS für alle derzeit in der Organisation verwendeten KDS-Einstellungen aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cde52-129">This command enables CDR for all the CDR configuration settings currently in use in your organization.</span></span>
    
        Get-CsCdrConfiguration | Set-CsCdrConfiguration "site:Redmond" -EnableCDR $True

</div>

<span data-ttu-id="cde52-130">Weitere Informationen finden Sie im Hilfethema zum Cmdlet " [Satz-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) ".</span><span class="sxs-lookup"><span data-stu-id="cde52-130">For more information, see the help topic for the [Set-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsCdrConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="cde52-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cde52-131">See Also</span></span>


[<span data-ttu-id="cde52-132">Planen der Überwachung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cde52-132">Planning for monitoring in Lync Server 2013</span></span>](lync-server-2013-planning-for-monitoring.md)  
[<span data-ttu-id="cde52-133">Bereitstellen der Überwachung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cde52-133">Deploying monitoring in Lync Server 2013</span></span>](lync-server-2013-deploying-monitoring.md)  
  

<span data-ttu-id="cde52-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cde52-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

