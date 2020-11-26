---
title: 'Lync Server 2013: Löschen einer vorhandenen Sammlung von CDR-Konfigurationseinstellungen'
description: 'Lync Server 2013: Löschen einer vorhandenen Sammlung von CDR-Konfigurationseinstellungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of CDR configuration settings
ms:assetid: 8ebf5da8-c0fc-498c-8d85-527d3be8479a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688128(v=OCS.15)
ms:contentKeyID: 49733726
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e80f6d9e9d878dad258e494095b10c402029932b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430560"
---
# <a name="delete-an-existing-collection-of-cdr-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="dc941-103">Löschen einer vorhandenen Sammlung von CDR-Konfigurationseinstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dc941-103">Delete an existing collection of CDR configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dc941-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dc941-104">

<span> </span></span></span>

<span data-ttu-id="dc941-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="dc941-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="dc941-p101">Die Funktion zum Aufzeichnen von Kommunikationsdatensätzen (KDS) ermöglicht das Nachverfolgen von Peer-to-Peer-, VoIP- und Konferenzanrufen. Diese Nutzungsdaten umfassen Informationen wie z. B. Anrufer, Angerufener, Anrufzeitpunkt und Anrufdauer.</span><span class="sxs-lookup"><span data-stu-id="dc941-p101">Call Detail Recording (CDR) enables you to track usage of such things as peer-to-peer instant messaging sessions, Voice over Internet Protocol (VoIP) phone calls, and conferencing calls. This usage data includes information about who called whom, when they called, and how long they talked.</span></span>

<span data-ttu-id="dc941-108">Wenn Sie Microsoft lync Server 2013 installieren, wird eine einzige globale Sammlung von CDR-Konfigurationseinstellungen für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="dc941-108">When you install Microsoft Lync Server 2013, a single, global collection of CDR configuration settings is created for you.</span></span> <span data-ttu-id="dc941-109">Administratoren haben außerdem die Möglichkeit, benutzerdefinierte Auflistungen von Einstellungen zu erstellen, die auf einzelne Standorte angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="dc941-109">Administrators also have the option of creating custom setting collections that can be applied to individual sites.</span></span> <span data-ttu-id="dc941-110">Prinzipiell haben Einstellungen auf Standortebene Vorrang vor globalen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="dc941-110">By design, settings configured at the site scope take precedence over settings configured at the global scope.</span></span> <span data-ttu-id="dc941-111">Wenn Sie die Einstellungen auf Standortebene entfernen, werden die KDS-Daten (Kommunikationsdatensätze) an diesem Standort mithilfe von globalen Einstellungen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="dc941-111">If you delete site-scoped settings, then CDR will be managed in that site by using the global settings.</span></span>

<span data-ttu-id="dc941-p103">Beachten Sie, dass Sie auch die globalen Einstellungen löschen können. Diese globalen Einstellungen werden jedoch tatsächlich nicht entfernt. Stattdessen werden alle Eigenschaften in dieser Auflistung auf die Standardwerte zurückgesetzt. Beispielsweise ist in der Auflistung von KDS-Konfigurationseinstellungen standardmäßig die Löschung aktiviert. Angenommen, Sie ändern die globalen Einstellungen, sodass die Löschung deaktiviert wurde. Wenn Sie später die globalen Einstellungen löschen, werden alle Eigenschaften auf ihre Standardwerte zurückgesetzt. Das bedeutet in diesem Fall, dass die Löschung wieder aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="dc941-p103">Note that you can also “delete” the global settings. However, the global settings will not actually be removed. Instead, all the properties in that collection will be reset to their default values. For example, by default purging is enabled in a collection of CDR configuration settings. Suppose you modify the global collection so that purging is disabled. If you later delete the global settings, all the properties will be reset to their default values. In this case, that means that purging will once again be enabled.</span></span>

<span data-ttu-id="dc941-119">Sie können die CDR-Konfigurationseinstellungen mithilfe der lync Server-Systemsteuerung oder des Cmdlets [Remove-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsCdrConfiguration) entfernen.</span><span class="sxs-lookup"><span data-stu-id="dc941-119">You can remove CDR configuration settings by using the Lync Server Control Panel or the [Remove-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsCdrConfiguration) cmdlet.</span></span>

<div>

## <a name="to-remove-cdr-configuration-settings-with-lync-server-control-panel"></a><span data-ttu-id="dc941-120">So entfernen Sie CDR-Konfigurationseinstellungen mit der lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="dc941-120">To remove CDR configuration settings with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="dc941-121">Klicken Sie in der lync Server-Systemsteuerung auf **Überwachung und Archivierung**.</span><span class="sxs-lookup"><span data-stu-id="dc941-121">In Lync Server Control Panel, click **Monitoring and Archiving**.</span></span>

2.  <span data-ttu-id="dc941-p104">Wählen Sie auf der Registerkarte **Aufzeichnung von Kommunikationsdatensätzen** die Auflistung (oder Auflistungen) der zu entfernenden KDS-Einstellungen aus. Zum Auswählen mehrerer Auflistungen klicken Sie auf die erste Auflistung, halten Sie die Strg-Taste gedrückt und klicken Sie dann auf weitere Auflistungen.</span><span class="sxs-lookup"><span data-stu-id="dc941-p104">On the **Call Detail Recording** tab, select the collection (or collections) of CDR settings to be removed. To select multiple collections, click the first collection, hold down the Ctrl key, and click additional collections.</span></span>

3.  <span data-ttu-id="dc941-124">Klicken Sie auf **Bearbeiten** und anschließend auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="dc941-124">Click **Edit**, and then click **Delete**.</span></span>

4.  <span data-ttu-id="dc941-125">Klicken Sie im Dialogfeld lync Server-Systemsteuerung auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="dc941-125">In the Lync Server Control Panel dialog box, click **OK**.</span></span>

</div>

<div>

## <a name="removing-cdr-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="dc941-126">Entfernen von CDR-Konfigurationseinstellungen mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="dc941-126">Removing CDR Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="dc941-127">Sie können die Konfigurationseinstellungen für die Anrufdetailaufzeichnung mithilfe von Windows PowerShell und dem Cmdlet **Remove-CsCdrConfiguration** löschen.</span><span class="sxs-lookup"><span data-stu-id="dc941-127">You can delete call detail recording configuration settings by using Windows PowerShell and the **Remove-CsCdrConfiguration** cmdlet.</span></span> <span data-ttu-id="dc941-128">Sie können dieses Cmdlet entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="dc941-128">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="dc941-129">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="dc941-129">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-cdr-configuration-settings"></a><span data-ttu-id="dc941-130">So entfernen Sie eine angegebene Auflistung von KDS-Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="dc941-130">To remove a specified collection of CDR configuration settings</span></span>

  - <span data-ttu-id="dc941-131">Mit diesem Befehl werden die KDS-Konfigurationseinstellungen entfernt, die auf den Standort „Redmond“ angewendet wurden:</span><span class="sxs-lookup"><span data-stu-id="dc941-131">This command removes the CDR configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsCdrConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-the-cdr-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="dc941-132">So entfernen Sie alle KDS-Konfigurationseinstellungen, die auf Standortebene angewendet wurden</span><span class="sxs-lookup"><span data-stu-id="dc941-132">To remove all the CDR configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="dc941-133">Mit diesem Befehl werden alle KDS-Konfigurationseinstellungen entfernt, die auf Standortebene angewendet wurden:</span><span class="sxs-lookup"><span data-stu-id="dc941-133">This command removes all the CDR configuration settings applied to the site scope:</span></span>
    
        Get-CsCdrConfiguration -Filter "site:*" | Remove-CsCdrConfiguration

</div>

<div>

## <a name="to-remove-all-the-cdr-configuration-settings-that-disable-call-detail-recording"></a><span data-ttu-id="dc941-134">So entfernen Sie alle KDS-Konfigurationseinstellungen, die die Aufzeichnung von Kommunikationsdatensätzen deaktivieren</span><span class="sxs-lookup"><span data-stu-id="dc941-134">To remove all the CDR configuration settings that disable call detail recording</span></span>

  - <span data-ttu-id="dc941-135">Mit diesem Befehl werden alle KDS-Konfigurationseinstellungen entfernt, bei denen die Aufzeichnung von Kommunikationsdatensätzen deaktiviert wurde:</span><span class="sxs-lookup"><span data-stu-id="dc941-135">This command removes all the CDR configuration settings where Call Detail recording has been disabled:</span></span>
    
        Get-CsCdrConfiguration | Where-Object {$_.EnableCDR -eq $False} | Remove-CsCdrConfiguration

</div>

<span data-ttu-id="dc941-136">Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Remove-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsCdrConfiguration) .</span><span class="sxs-lookup"><span data-stu-id="dc941-136">For more information, see the help topic for the [Remove-CsCdrConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsCdrConfiguration) cmdlet.</span></span>

<span data-ttu-id="dc941-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dc941-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

