---
title: 'Lync Server 2013: Anzeigen der CDR-Konfigurationsinformationen'
description: 'Lync Server 2013: Anzeigen der CDR-Konfigurationsinformationen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View CDR configuration information
ms:assetid: 77bd553f-da89-4c84-a5d0-2f7e91d04383
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688096(v=OCS.15)
ms:contentKeyID: 49733695
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 687ee05701c022e1d7ecfe2cd8be5190949c51d0
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443405"
---
# <a name="view-cdr-configuration-information-in-lync-server-2013"></a><span data-ttu-id="beb59-103">Anzeigen der CDR-Konfigurationsinformationen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="beb59-103">View CDR configuration information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="beb59-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="beb59-104">

<span> </span></span></span>

<span data-ttu-id="beb59-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="beb59-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="beb59-p101">Die Funktion zum Aufzeichnen von Kommunikationsdatensätzen (KDS) ermöglicht das Nachverfolgen von Peer-to-Peer-, VoIP- und Konferenzanrufen. Diese Nutzungsdaten umfassen Informationen wie z. B. Anrufer, Angerufener, Anrufzeitpunkt und Anrufdauer.</span><span class="sxs-lookup"><span data-stu-id="beb59-p101">Call Detail Recording (CDR) enables you to track usage of such things as peer-to-peer instant messaging sessions, Voice over Internet Protocol (VoIP) phone calls, and conferencing calls. This usage data includes information about who called whom, when they called, and how long they talked.</span></span>

<span data-ttu-id="beb59-108">Wenn Sie Microsoft lync Server 2013 installieren, wird eine einzige globale Sammlung von CDR-Konfigurationseinstellungen für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="beb59-108">When you install Microsoft Lync Server 2013, a single, global collection of CDR configuration settings is created for you.</span></span> <span data-ttu-id="beb59-109">Administratoren haben außerdem die Möglichkeit, benutzerdefinierte Auflistungen von Einstellungen zu erstellen, die auf einzelne Standorte angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="beb59-109">Administrators also have the option of creating custom setting collections that can be applied to individual sites.</span></span> <span data-ttu-id="beb59-110">Sie können die in Ihrer Organisation verwendeten CdR-Konfigurationseinstellungen mithilfe der lync Server-Systemsteuerung oder mit dem Cmdlet [Get-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsCdrConfiguration) anzeigen.</span><span class="sxs-lookup"><span data-stu-id="beb59-110">You can view the CDR configuration settings in use in your organization by using Lync Server Control Panel or the [Get-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsCdrConfiguration) cmdlet.</span></span>

<div>

## <a name="to-view-cdr-configuration-information-by-using-lync-server-control-panel"></a><span data-ttu-id="beb59-111">So zeigen Sie CDR-Konfigurationsinformationen mithilfe der lync Server-Systemsteuerung an</span><span class="sxs-lookup"><span data-stu-id="beb59-111">To view CDR configuration information by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="beb59-112">Klicken Sie in der lync Server-Systemsteuerung auf **Überwachung und Archivierung**.</span><span class="sxs-lookup"><span data-stu-id="beb59-112">In Lync Server Control Panel click **Monitoring and Archiving**.</span></span>

2.  <span data-ttu-id="beb59-p103">Auf der Registerkarte **Aufzeichnung von Kommunikationsdatensätzen** wird eine Liste mit allen KDS-Konfigurationseinstellungen angezeigt; für jede Einstellungsauflistung wird der **Name** der Auflistung angezeigt; ob KDS aktiviert wurde oder nicht (die Eigenschaft **KDS**); und ob der Löschvorgang (die Eigenschaft **KDS-Löschvorgang**) aktiviert wurde oder nicht. Sie können detaillierte Informationen zu einer Auflistung anzeigen, indem Sie doppelt auf diese Auflistung klicken. Alternativ können Sie die gewünschte Auflistung auswählen und auf **Bearbeiten** und **Details anzeigen** klicken. Beachten Sie Folgendes: Es können jeweils nur detaillierte Informationen zu einer Auflistung mit KDS-Konfigurationseinstellungen angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="beb59-p103">A list of all your CDR configuration settings will be displayed in the **Call Detail Recording** tab; for each collection of settings you will see the collection **Name**; whether or not CDR has been enabled (the **CDR** property); and whether or not purging has been enabled (the **CDR purging** property). To see detailed information about a collection, double-click the collection, or select the appropriate collection, click **Edit**, and then click **Show Details**. Note that you can only view detailed information for a single collection of CDR configuration settings at a time.</span></span>

</div>

<div>

## <a name="viewing-cdr-configuration-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="beb59-116">Anzeigen von CDR-Konfigurationsinformationen mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="beb59-116">Viewing CDR Configuration Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="beb59-117">Sie können die CDR-Konfigurationseinstellungen mithilfe von Windows PowerShell und dem Get-CsCdrConfiguration-Cmdlet anzeigen.</span><span class="sxs-lookup"><span data-stu-id="beb59-117">You can view CDR configuration settings by using Windows PowerShell and the Get-CsCdrConfiguration cmdlet.</span></span> <span data-ttu-id="beb59-118">Sie können dieses Cmdlet entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="beb59-118">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="beb59-119">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="beb59-119">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-cdr-configuration-information"></a><span data-ttu-id="beb59-120">So zeigen Sie KDS-Konfigurationsinformationen an</span><span class="sxs-lookup"><span data-stu-id="beb59-120">To view CDR configuration information</span></span>

  - <span data-ttu-id="beb59-121">Wenn Sie Informationen zu allen CdR-Konfigurationseinstellungen anzeigen möchten, geben Sie den folgenden Befehl in der lync Server-Verwaltungsshell ein, und drücken Sie dann die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="beb59-121">To view information about all your CDR configuration settings, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsCdrConfiguration
    
    <span data-ttu-id="beb59-122">Es werden etwa folgende Informationen zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="beb59-122">That will return information similar to this:</span></span>
    
        Identity               : Global
        EnableCDR              : True
        EnablePurging          : True
        KeepCallDetailForDays  : 90
        KeepErrorReportForDays : 60
        PurgeHourOfDay         : 2

</div>

<span data-ttu-id="beb59-123">Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Get-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsCdrConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="beb59-123">For more information, see the help topic for the [Get-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsCdrConfiguration) cmdlet.</span></span>

<span data-ttu-id="beb59-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="beb59-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

