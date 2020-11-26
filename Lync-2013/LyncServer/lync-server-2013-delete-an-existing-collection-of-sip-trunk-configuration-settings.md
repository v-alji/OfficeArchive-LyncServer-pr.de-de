---
title: Löschen einer vorhandenen Auflistung von SIP-Trunkkonfigurationseinstellungen
description: Löschen Sie eine vorhandene Sammlung von SIP-Trunk-Konfigurationseinstellungen.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete an existing collection of SIP trunk configuration settings
ms:assetid: 3b25f14d-884b-42dd-a866-460d276d3e43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688024(v=OCS.15)
ms:contentKeyID: 49733614
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 98acede458d34eb30202d898414b2e17076d32d2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430518"
---
# <a name="delete-an-existing-collection-of-sip-trunk-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="698f8-103">Löschen einer vorhandenen Sammlung von SIP-Trunk-Konfigurationseinstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="698f8-103">Delete an existing collection of SIP trunk configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="698f8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="698f8-104">

<span> </span></span></span>

<span data-ttu-id="698f8-105">_**Letztes Änderungsdatum des Themas:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="698f8-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="698f8-106">SIP Trunk-Konfigurationseinstellungen definieren die Beziehungen und Funktionen zwischen einem Vermittlungs Server und dem PSTN-Gateway (Public Switched Telephone Network), einer IP-Public Branch Exchange (PBX) oder einem Session Border Controller (SBC) beim Dienstanbieter.</span><span class="sxs-lookup"><span data-stu-id="698f8-106">SIP trunk configuration settings define the relationship and capabilities between a Mediation Server and the public switched telephone network (PSTN) gateway, an IP-public branch exchange (PBX), or a Session Border Controller (SBC) at the service provider.</span></span> <span data-ttu-id="698f8-107">Diese Einstellungen geben unter anderem Folgendes an:</span><span class="sxs-lookup"><span data-stu-id="698f8-107">These settings do such things as specify:</span></span>

  - <span data-ttu-id="698f8-108">Ob Medienumgehung für die Trunks aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="698f8-108">Whether media bypass should be enabled on the trunks.</span></span>

  - <span data-ttu-id="698f8-109">Die Bedingungen, unter denen RTCP-Pakete (Real-Time Transport Control Protocol) gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="698f8-109">The conditions under which real-time transport control protocol (RTCP) packets are sent.</span></span>

  - <span data-ttu-id="698f8-110">Ob die SRTP-Verschlüsselung (Secure Real-Time Protocol) für jeden trunk erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="698f8-110">Whether or not secure real-time protocol (SRTP) encryption is required on each trunk.</span></span>

<span data-ttu-id="698f8-111">Wenn Sie Microsoft lync Server 2013 installieren, wird eine globale Sammlung von SIP-Trunk-Konfigurationseinstellungen für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="698f8-111">When you install Microsoft Lync Server 2013, a global collection of SIP trunk configuration settings is created for you.</span></span> <span data-ttu-id="698f8-112">Diese globale Auflistung von Einstellungen kann nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="698f8-112">This global collection of settings cannot be deleted.</span></span> <span data-ttu-id="698f8-113">Sie können jedoch die lync Server-Systemsteuerung oder das Cmdlet [Remove-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg425943(v=OCS.15)) verwenden, um die Eigenschaften in der globalen Sammlung auf ihre Standardwerte zurückzusetzen.</span><span class="sxs-lookup"><span data-stu-id="698f8-113">However, you can use the Lync Server Control Panel or the [Remove-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg425943(v=OCS.15)) cmdlet to "reset" the properties in the global collection to their default values.</span></span> <span data-ttu-id="698f8-114">Wenn Sie beispielsweise die Eigenschaft „Enable3pccRefer“ auf „True“ setzen, wird diese Eigenschaft beim Zurücksetzen der globalen Auflistung auf den Standardwert „False“ zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="698f8-114">For example, if you have set the Enable3pccRefer property to True, when you reset the global collection the Enable3pccRefer property will revert to its default value of False.</span></span>

<span data-ttu-id="698f8-p103">Administratoren können auch benutzerdefinierte Trunkkonfigurationseinstellungen für den Standort- oder Dienstbereich (für ein einzelnes PSTN-Gateway) erstellen. Diese benutzerdefinierten Einstellungen können entfernt werden. Beachten Sie beim Entfernen dieser benutzerdefinierten Einstellungen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="698f8-p103">Administrators can also create custom trunk configuration settings at the site scope or at the service scope (for an individual PSTN gateway); these custom settings can be removed. When removing these custom settings keep the following in mind:</span></span>

  - <span data-ttu-id="698f8-p104">Wenn Sie Einstellungen für den Dienstbereich entfernen, wird der mit diesen Einstellungen verwaltete SIP-Trunk mit den Einstellungen verwaltet, die für den entsprechenden Standort gelten, sofern vorhanden. Wenn keine Standorteinstellungen vorhanden sind, werden diese Trunks mit der globalen Auflistung der Trunkkonfigurationseinstellungen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="698f8-p104">If you remove service scope settings, then the SIP trunk managed by those settings will be managed by the settings applied to their site, if they exist. If site settings do not exist, those trunks will then be managed by the global collection of trunk configuration settings.</span></span>

  - <span data-ttu-id="698f8-119">Wenn Sie Einstellungen für den Standortbereich entfernen, werden alle mit diesen Einstellungen verwalteten SIP-Trunks jetzt mit der globalen Auflistung der Trunkkonfigurationseinstellungen verwaltet.</span><span class="sxs-lookup"><span data-stu-id="698f8-119">If you remove site-scoped settings then any SIP trunks managed by those settings will now be managed by the global collection of trunk configuration settings.</span></span>

<div>

## <a name="to-remove-trunk-configuration-settings-with-lync-server-control-panel"></a><span data-ttu-id="698f8-120">So entfernen Sie trunk-Konfigurationseinstellungen mit der lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="698f8-120">To remove trunk configuration settings with Lync Server Control Panel</span></span>

1.  <span data-ttu-id="698f8-121">Klicken Sie in der lync Server-Systemsteuerung auf **VoIP-Routing** , und klicken Sie dann auf **trunk-Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="698f8-121">In Lync Server Control Panel, click **Voice Routing** and then click **Trunk Configuration**.</span></span>

2.  <span data-ttu-id="698f8-p105">Wählen Sie auf der Registerkarte **Trunkkonfiguration** die Auflistung der zu löschenden SIP-Trunkkonfigurationseinstellungen aus, klicken Sie auf **Bearbeiten** und dann auf **Löschen**. Klicken Sie zum Löschen mehrerer Auflistungen auf die erste zu löschende Auflistung, halten Sie die STRG-TASTE gedrückt und klicken Sie dann auf die weiteren Auflistungen, die Sie entfernen möchten.</span><span class="sxs-lookup"><span data-stu-id="698f8-p105">On the **Trunk Configuration** tab, select the collection of SIP trunk configuration settings to be deleted, click **Edit** and then click **Delete**. To delete multiple collections in the same operation, click the first collection to be deleted, then hold down the Ctrl key and click any additional collections that you want to remove.</span></span>

3.  <span data-ttu-id="698f8-p106">Die Eigenschaft **State** für die Sammlung wird als **Commit nicht ausgeführt** angezeigt. Um die Änderungen zu übernehmen und die Sammlung zu löschen, klicken Sie auf **Commit ausführen** und anschließend auf **Commit für alle Elemente ausführen**.</span><span class="sxs-lookup"><span data-stu-id="698f8-p106">The **State** property for the collection will be updated to **Uncommitted**. To commit the changes, and to delete the collection, click **Commit** and then click **Commit All**.</span></span>

4.  <span data-ttu-id="698f8-126">Klicken Sie im Dialogfeld **VoIP-Konfigurationseinstellungen, für die kein Commit ausgeführt wurde** auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="698f8-126">In the **Uncommitted Voice Configuration Settings** dialog box, click **OK**.</span></span>

5.  <span data-ttu-id="698f8-127">Klicken Sie im Dialogfeld **Microsoft lync Server 2013-System** Steuerung auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="698f8-127">In the **Microsoft Lync Server 2013 Control Panel** dialog box click **OK**.</span></span>

6.  <span data-ttu-id="698f8-128">Wenn Sie es sich anders überlegen und die Sammlung nicht löschen möchten, klicken Sie auf **Commit** , und klicken Sie dann auf **alle nicht übernommenen Änderungen abbrechen**.</span><span class="sxs-lookup"><span data-stu-id="698f8-128">If you change your mind and decide not to delete the collection, click **Commit** and then click **Cancel All Uncommitted Changes**.</span></span> <span data-ttu-id="698f8-129">Wenn das Dialogfeld **Microsoft lync Server 2013-System** Steuerung angezeigt wird, klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="698f8-129">When the **Microsoft Lync Server 2013 Control Panel** dialog box appears, click **OK**.</span></span>

</div>

<div>

## <a name="removing-trunk-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="698f8-130">Entfernen von trunk-Konfigurationseinstellungen mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="698f8-130">Removing Trunk Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="698f8-131">Sie können trunk-Konfigurationseinstellungen mithilfe von Windows PowerShell und dem Cmdlet **Remove-CsTrunkConfiguration** löschen.</span><span class="sxs-lookup"><span data-stu-id="698f8-131">You can delete trunk configuration settings by using Windows PowerShell and the **Remove-CsTrunkConfiguration** cmdlet.</span></span> <span data-ttu-id="698f8-132">Sie können dieses Cmdlet entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="698f8-132">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="698f8-133">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="698f8-133">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-remove-a-specified-collection-of-settings"></a><span data-ttu-id="698f8-134">So entfernen Sie eine angegebene Auflistung von Einstellungen</span><span class="sxs-lookup"><span data-stu-id="698f8-134">To remove a specified collection of settings</span></span>

  - <span data-ttu-id="698f8-135">Mit dem folgenden Befehl werden die Trunkkonfigurationseinstellungen gelöscht, die auf den Standort „Redmond“ angewendet wurden:</span><span class="sxs-lookup"><span data-stu-id="698f8-135">The following command removes the trunk configuration settings applied to the Redmond site:</span></span>
    
        Remove-CsTrunkConfiguration -Identity site:Redmond

</div>

<div>

## <a name="to-remove-all-the-collections-applied-to-the-site-scope"></a><span data-ttu-id="698f8-136">So entfernen Sie alle Auflistungen, die im Standortbereich angewendet wurden</span><span class="sxs-lookup"><span data-stu-id="698f8-136">To remove all the collections applied to the site scope</span></span>

  - <span data-ttu-id="698f8-137">Mit dem folgenden Befehl werden alle Trunkkonfigurationseinstellungen entfernt, die auf den Dienstbereich angewendet wurden:</span><span class="sxs-lookup"><span data-stu-id="698f8-137">This command removes all the trunk configuration settings applied to the service scope:</span></span>
    
        Get-CsTrunkConfiguration -Filter "service:*" | Remove-CsTrunkConfiguration

</div>

<div>

## <a name="to-remove-all-the-collections-where-media-bypass-is-enabled"></a><span data-ttu-id="698f8-138">So entfernen Sie alle Auflistungen, bei denen die Medienumgehung aktiviert ist</span><span class="sxs-lookup"><span data-stu-id="698f8-138">To remove all the collections where media bypass is enabled</span></span>

  - <span data-ttu-id="698f8-139">Mit dem folgenden Befehl werden alle Trunkkonfigurationseinstellungen entfernt, bei denen die Medienumgehung aktiviert ist:</span><span class="sxs-lookup"><span data-stu-id="698f8-139">The following command removes all the trunk configuration settings where media bypass has been enabled:</span></span>
    
        Get-CsTrunkConfiguration | Where-Object {$_.EnableBypass -eq $True} | Remove-CsTrunkConfiguration

</div>

<span data-ttu-id="698f8-140">Weitere Informationen finden Sie im Hilfethema zum Cmdlet [Remove-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg425943(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="698f8-140">For more information, see the help topic for the [Remove-CsTrunkConfiguration](https://technet.microsoft.com/library/Gg425943(v=OCS.15)) cmdlet.</span></span>

<span data-ttu-id="698f8-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="698f8-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

