---
title: 'Lync Server 2013: Löschen der Konfigurationseinstellungen für die Qualität der Benutzeroberfläche'
description: 'Lync Server 2013: Löschen der Konfigurationseinstellungen für die Qualität der Benutzeroberfläche'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete Quality of Experience configuration settings
ms:assetid: fd0c4c2f-3bfb-42cb-9b6a-f0f8d5aa9e81
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182613(v=OCS.15)
ms:contentKeyID: 48185954
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1894877fe3dbbc758ba02b0e4e5b81c8b7edc4fb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430427"
---
# <a name="delete-quality-of-experience-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="65c7c-103">Löschen der Konfigurationseinstellungen für die Qualität der Benutzeroberfläche in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="65c7c-103">Delete Quality of Experience configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="65c7c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="65c7c-104">

<span> </span></span></span>

<span data-ttu-id="65c7c-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="65c7c-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="65c7c-p101">QoE (Quality of Experience)-Metriken dienen der Überwachung der Qualität von Audio- und Videoanrufen in Ihrer Organisation, z. B. der Anzahl der verloren gegangenen Netzwerkpakete, von Hintergrundgeräuschen und der Unterschiede bei Paketverzögerung (Jitter). Diese Metriken werden in einer Datenbank getrennt von anderen Daten (z. B. den Kommunikationsdatensätzen) gespeichert, sodass QoE unabhängig von anderen Datenaufzeichnungen aktiviert und deaktiviert werden kann.</span><span class="sxs-lookup"><span data-stu-id="65c7c-p101">Quality of Experience (QoE) metrics track the quality of audio and video calls made in your organization, including such things as the number of network packets lost, background noise, and the amount of "jitter" (differences in packet delay). These metrics are stored in a database apart from other data (such as call detail records), which allows you to enable and disable QoE independent of other data recording.</span></span>

<span data-ttu-id="65c7c-108">Wenn Sie Microsoft lync Server 2013 installieren, wird eine einzelne globale Sammlung von QoE-Konfigurationseinstellungen für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="65c7c-108">When you install Microsoft Lync Server 2013, a single, global collection of QoE configuration settings is created for you.</span></span> <span data-ttu-id="65c7c-109">Administratoren haben außerdem die Möglichkeit, benutzerdefinierte Auflistungen von Einstellungen zu erstellen, die auf einzelne Standorte angewendet werden können.</span><span class="sxs-lookup"><span data-stu-id="65c7c-109">Administrators also have the option of creating custom setting collections that can be applied to individual sites.</span></span> <span data-ttu-id="65c7c-110">Prinzipiell gilt, dass auf Standortebene konfigurierte Einstellungen Vorrang vor auf globaler Ebene konfigurierten Einstellungen haben.</span><span class="sxs-lookup"><span data-stu-id="65c7c-110">By design, settings configured at the site scope take precedence over settings configured at the global scope.</span></span> <span data-ttu-id="65c7c-111">Wenn Sie Einstellungen auf Standortebene löschen, wird QoE an diesem Standort unter Verwendung der globalen Einstellungen gesteuert.</span><span class="sxs-lookup"><span data-stu-id="65c7c-111">If you delete site-scoped settings, then QoE will be managed in that site by using the global settings.</span></span>

<span data-ttu-id="65c7c-p103">Beachten Sie, dass Sie die globalen Einstellungen auch „löschen“ können. Allerdings werden die globalen Einstellungen dabei nicht entfernt. Vielmehr werden alle Eigenschaften in dieser Auflistung auf ihre Standardwerte zurückgesetzt. Ein Beispiel: Angenommen, in einer Auflistung von QoE-Konfigurationseinstellungen ist standardmäßig die Bereinigung aktiviert. Sie ändern nun die globale Auflistung dahin gehend, dass Bereinigung deaktiviert ist. Wenn Sie später die globalen Einstellungen löschen, werden alle Eigenschaften auf ihre Standardwerte zurückgesetzt. In diesem Fall bedeutet das, dass die Bereinigung wieder aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="65c7c-p103">Note that you can also “delete” the global settings. However, the global settings will not actually be removed. Instead, all the properties in that collection will be reset to their default values. For example, by default purging is enabled in a collection of QoE configuration settings. Suppose you modify the global collection so that purging is disabled. If you later delete the global settings, all the properties will be reset to their default values. In this case, that means that purging will once again be enabled.</span></span>

<span data-ttu-id="65c7c-119">Sie können QoE-Konfigurationseinstellungen mithilfe der lync Server-Systemsteuerung oder mithilfe des Cmdlets [Remove-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsQoEConfiguration) entfernen.</span><span class="sxs-lookup"><span data-stu-id="65c7c-119">You can remove QoE configuration settings by using the Lync Server Control Panel or by using the [Remove-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsQoEConfiguration) cmdlet.</span></span>

<div>

## <a name="to-delete-qoe-configuration-settings-by-using-lync-server-control-panel"></a><span data-ttu-id="65c7c-120">So löschen Sie QoE-Konfigurationseinstellungen mithilfe der lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="65c7c-120">To delete QoE configuration settings by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="65c7c-121">Melden Sie sich auf dem Computer als Mitglied der Gruppe "RTCUniversalServerAdmins" oder als Benutzer mit der Rolle "CsVoiceAdministrator", "CsServerAdministrator" oder "CsAdministrator" an.</span><span class="sxs-lookup"><span data-stu-id="65c7c-121">Log on to the computer as a member of the RTCUniversalServerAdmins group, or as a member of the CsVoiceAdministrator, CsServerAdministrator, or CsAdministrator role.</span></span> <span data-ttu-id="65c7c-122">Ausführliche Informationen finden Sie unter [Delegieren von Setup Berechtigungen in lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="65c7c-122">For details, see [Delegate setup permissions in Lync Server 2013](lync-server-2013-delegate-setup-permissions.md).</span></span>

2.  <span data-ttu-id="65c7c-123">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="65c7c-123">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="65c7c-124">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="65c7c-124">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="65c7c-125">Klicken Sie in der linken Navigationsleiste auf **Überwachung und Archivierung** und dann auf **QoE-Daten**.</span><span class="sxs-lookup"><span data-stu-id="65c7c-125">In the left navigation bar, click **Monitoring and Archiving**, and then click **Quality of Experience Data**.</span></span>

4.  <span data-ttu-id="65c7c-126">Klicken Sie auf der Seite **QoE-Daten** auf die gewünschte Richtlinie, dann auf **Bearbeiten** und anschließend auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="65c7c-126">On the **Quality of Experience Data** page, click the policy that you want, click **Edit**, and then click **Delete**.</span></span>

5.  <span data-ttu-id="65c7c-127">Klicken Sie anschließend auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="65c7c-127">Click **OK**.</span></span>

</div>

<div>

## <a name="removing-qoe-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="65c7c-128">Entfernen von QoE-Konfigurationseinstellungen mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="65c7c-128">Removing QoE Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="65c7c-129">Sie können QoE-Konfigurationseinstellungen mithilfe von Windows PowerShell und dem Cmdlet **Remove-CsQoEConfiguration** löschen.</span><span class="sxs-lookup"><span data-stu-id="65c7c-129">You can delete QoE configuration settings by using Windows PowerShell and the **Remove-CsQoEConfiguration** cmdlet.</span></span> <span data-ttu-id="65c7c-130">Sie können dieses Cmdlet entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="65c7c-130">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="65c7c-131">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="65c7c-131">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-qoe-configuration-settings"></a><span data-ttu-id="65c7c-132">So entfernen Sie eine angegebene Auflistung von QoE-Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="65c7c-132">To remove a specified collection of QoE configuration settings</span></span>

  - <span data-ttu-id="65c7c-133">Mit diesem Befehl werden die QoE-Konfigurationseinstellungen entfernt, die auf den Standort Redmond angewendet wurden:</span><span class="sxs-lookup"><span data-stu-id="65c7c-133">This command removes the QoE configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsQoEConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-remove-all-of-the-qoe-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="65c7c-134">So entfernen Sie alle QoE-Konfigurationseinstellungen, die auf Standortebene angewendet wurden</span><span class="sxs-lookup"><span data-stu-id="65c7c-134">To remove all of the QoE configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="65c7c-135">Mit diesem Befehl werden alle QoE-Konfigurationseinstellungen entfernt, die auf Standortebene angewendet wurden:</span><span class="sxs-lookup"><span data-stu-id="65c7c-135">This command removes all the QoE configuration settings applied to the site scope:</span></span>
    
        Get-CsQoEConfiguration -Filter "site:*" | Remove-CsQoEConfiguration

</div>

<div>

## <a name="to-remove-all-of-the-qoe-configuration-settings-where-qoe-monitoring-is-disabled"></a><span data-ttu-id="65c7c-136">So entfernen Sie alle QoE-Konfigurationseinstellungen, in denen QoE-Überwachung deaktiviert ist</span><span class="sxs-lookup"><span data-stu-id="65c7c-136">To remove all of the QoE configuration settings where QoE monitoring is disabled</span></span>

  - <span data-ttu-id="65c7c-137">Mit diesem Befehl werden alle QoE-Konfigurationseinstellungen entfernt, in denen die QoE-Überwachung deaktiviert wurde:</span><span class="sxs-lookup"><span data-stu-id="65c7c-137">This command removes all the QoE configuration settings where QoE monitoring has been disabled:</span></span>
    
        Get-CsQoEConfiguration | Where-Object {$_.EnableQoE -eq $False} | Remove-CsQoEConfiguration

</div>

<span data-ttu-id="65c7c-138">Ausführliche Informationen finden Sie unter [Remove-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsQoEConfiguration).</span><span class="sxs-lookup"><span data-stu-id="65c7c-138">For details, see [Remove-CsQoEConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsQoEConfiguration).</span></span>

<span data-ttu-id="65c7c-139"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="65c7c-139"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

