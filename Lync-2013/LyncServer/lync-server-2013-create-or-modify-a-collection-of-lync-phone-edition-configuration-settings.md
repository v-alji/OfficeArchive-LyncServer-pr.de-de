---
title: Erstellen oder Ändern einer Sammlung von lync Phone Edition-Konfigurationseinstellungen
description: Erstellen oder Ändern einer Sammlung von lync Phone Edition-Konfigurationseinstellungen
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a collection of Lync Phone Edition configuration settings
ms:assetid: 6cf714af-8f57-4a71-89ad-0a776302b2ba
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688086(v=OCS.15)
ms:contentKeyID: 49733683
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 82a4becadf581ec965952e507c3eb2839b622d9f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394754"
---
# <a name="create-or-modify-a-collection-of-lync-phone-edition-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="22b01-103">Erstellen oder Ändern einer Sammlung von lync Phone Edition-Konfigurationseinstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22b01-103">Create or modify a collection of Lync Phone Edition configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="22b01-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="22b01-104">

<span> </span></span></span>

<span data-ttu-id="22b01-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="22b01-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="22b01-106">Wenn Sie lync Server installieren, erhalten Sie eine globale Sammlung von lync Phone Edition-Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="22b01-106">When you install Lync Server, you get a global collection of Lync Phone Edition settings.</span></span> <span data-ttu-id="22b01-107">Diese Einstellungen gelten für alle Geräte, auf denen lync Phone Edition in Ihrer Bereitstellung ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="22b01-107">These settings apply to all devices running Lync Phone Edition in your deployment.</span></span> <span data-ttu-id="22b01-108">Sie können diese Einstellungen jederzeit ändern.</span><span class="sxs-lookup"><span data-stu-id="22b01-108">You can change these settings at any time.</span></span> <span data-ttu-id="22b01-109">Sie können auch eine neue Sammlung von Einstellungen einrichten, die für die Geräte in einer bestimmten Website gelten.</span><span class="sxs-lookup"><span data-stu-id="22b01-109">You can also set up a new collection of settings that apply to the devices in a specific site.</span></span> <span data-ttu-id="22b01-110">Websiteeinstellungen haben Vorrang vor globalen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="22b01-110">Site settings take precedence over global settings.</span></span>

<span data-ttu-id="22b01-111">Die Konfigurationseinstellungen bestehen aus dem Sammlungsnamen, dem Bereich (Global oder Website), der SIP-Sicherheitseinstellung, dem Protokolliergrad, der sprach Dienstleistungsqualität (QoS), der Einstellung für die Telefonsperre und den Details der Telefonsperre, d. h., wie lange die a)-Sperre für persönliche Identifikationsnummer (PIN) und b) im Leerlauf ist, bevor Sie sich</span><span class="sxs-lookup"><span data-stu-id="22b01-111">Configuration settings consist of the collection name, scope (global or site), SIP security setting, logging level, voice quality of service (QoS) level, phone-lock setting, and phone-lock details, that is, how long the a) unlock personal identification number (PIN) must be and b) phone stays idle before locking itself.</span></span>

<div>

## <a name="to-create-a-collection-of-lync-phone-edition-configuration-settings-or-edit-settings-for-an-existing-collection"></a><span data-ttu-id="22b01-112">So erstellen Sie eine Sammlung von lync Phone Edition-Konfigurationseinstellungen oder Bearbeiten von Einstellungen für eine vorhandene Sammlung</span><span class="sxs-lookup"><span data-stu-id="22b01-112">To create a collection of Lync Phone Edition configuration settings or edit settings for an existing collection</span></span>

1.  <span data-ttu-id="22b01-113">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="22b01-113">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="22b01-114">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="22b01-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="22b01-115">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="22b01-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="22b01-116">Klicken Sie in der linken Navigationsleiste auf **Clients**, und klicken Sie dann auf die Navigationsschaltfläche **Gerätekonfiguration** .</span><span class="sxs-lookup"><span data-stu-id="22b01-116">In the left navigation bar, click **Clients**, and then click the **Device Configuration** navigation button.</span></span>

4.  <span data-ttu-id="22b01-117">Führen Sie auf der Seite **Device Configuration** eine der folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="22b01-117">On the **Device Configuration** page, do one of the following:</span></span>
    
      - <span data-ttu-id="22b01-118">Wenn Sie eine neue Sammlung von lync Phone Edition-Konfigurationseinstellungen erstellen möchten, klicken Sie auf **neu**, wählen Sie eine Website aus, klicken Sie auf **OK**, überprüfen Sie die Standardeinstellungen, und nehmen Sie bei Bedarf Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="22b01-118">To create a new collection of Lync Phone Edition configuration settings, click **New**, select a site, click **OK**, review the default settings, and, if you want to, make any changes.</span></span>
    
      - <span data-ttu-id="22b01-119">Wenn Sie eine der Einstellungen in einer vorhandenen Sammlung bearbeiten möchten, klicken Sie auf die Sammlung, klicken Sie auf das Menü **Bearbeiten** , klicken Sie auf **Details anzeigen**, und nehmen Sie dann die gewünschten Änderungen vor.</span><span class="sxs-lookup"><span data-stu-id="22b01-119">To edit any of the settings in an existing collection, click the collection, click the **Edit** menu, click **Show details**, and then make your changes.</span></span>
        
        <div>
        

        > [!TIP]
        > <span data-ttu-id="22b01-120">Wenn Sie zur Verwendung der Standardeinstellungen für die globale Sammlung zurückkehren möchten, klicken Sie auf die globale Sammlung, klicken Sie auf das Menü <STRONG>Bearbeiten</STRONG> , klicken Sie auf <STRONG>Löschen</STRONG>, und klicken Sie dann auf <STRONG>OK</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="22b01-120">To go back to using the default settings for the global collection, click the global collection, click the <STRONG>Edit</STRONG> menu, click <STRONG>Delete</STRONG>, and then click <STRONG>OK</STRONG>.</span></span> <span data-ttu-id="22b01-121">Dadurch wird die globale Sammlung nicht gelöscht; die Einstellungen werden nur auf die Standardeinstellungen zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="22b01-121">This will not delete the global collection; it just resets the settings to the defaults.</span></span>

        
        </div>

5.  <span data-ttu-id="22b01-122">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="22b01-122">Click **Commit**.</span></span>

</div>

<div>

## <a name="creating-new-lync-phone-edition-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="22b01-123">Erstellen neuer lync Phone Edition-Konfigurationseinstellungen mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="22b01-123">Creating New Lync Phone Edition Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="22b01-124">Sie können die Konfigurationseinstellungen für lync Phone Edition (nur im Website Bereich) mithilfe von Windows PowerShell und dem Cmdlet **New-CsUCPhoneConfiguration** erstellen.</span><span class="sxs-lookup"><span data-stu-id="22b01-124">You can create Lync Phone Edition configuration settings can (at the site scope only) by using Windows PowerShell and the **New-CsUCPhoneConfiguration** cmdlet.</span></span> <span data-ttu-id="22b01-125">Sie können dieses Cmdlet in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="22b01-125">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="22b01-126">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="22b01-126">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-create-new-lync-phone-edition-configuration-settings-that-use-the-default-values"></a><span data-ttu-id="22b01-127">So erstellen Sie neue lync Phone Edition-Konfigurationseinstellungen, die die Standardwerte verwenden</span><span class="sxs-lookup"><span data-stu-id="22b01-127">To create new Lync Phone Edition configuration settings that use the default values</span></span>

  - <span data-ttu-id="22b01-128">Dieser Befehl erstellt einen neuen Satz von UC-Telefon Konfigurationseinstellungen für die Website "Redmond":</span><span class="sxs-lookup"><span data-stu-id="22b01-128">This command creates a new set of UC phone configuration settings for the Redmond site:</span></span>
    
        New-CsUCPhoneConfiguration -Identity "site:Redmond"
    
    <span data-ttu-id="22b01-129">Da im vorherigen Befehl keine weiteren Parameter (außer dem obligatorischen Identity-Parameter) angegeben wurden, werden in der neuen Auflistung von Konfigurationseinstellungen für alle Eigenschaften die Standardwerte verwendet.</span><span class="sxs-lookup"><span data-stu-id="22b01-129">Because no parameters (other than the mandatory Identity parameter) were specified in the preceding command, the new collection of configuration settings will use the default values for all its properties.</span></span>

</div>

<div>

## <a name="to-change-a-single-property-value-when-creating-new-lync-phone-edition-configuration-settings"></a><span data-ttu-id="22b01-130">So ändern Sie einen einzelnen Eigenschaftswert beim Erstellen neuer lync Phone Edition-Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="22b01-130">To change a single property value when creating new Lync Phone Edition configuration settings</span></span>

  - <span data-ttu-id="22b01-131">Um Einstellungen zu erstellen, die andere Eigenschaftswerte verwenden, geben Sie einfach den entsprechenden Parameter und Parameterwert ein.</span><span class="sxs-lookup"><span data-stu-id="22b01-131">To create settings that use different property values, simply include the appropriate parameter and parameter value.</span></span> <span data-ttu-id="22b01-132">Wenn Sie beispielsweise eine Sammlung von UC-Telefon Konfigurationseinstellungen erstellen möchten, die standardmäßig Telefon sperren erfordern, verwenden Sie einen Befehl wie den folgenden:</span><span class="sxs-lookup"><span data-stu-id="22b01-132">For example, to create a collection of UC phone configuration settings that, by default, require phone locking, use a command like this:</span></span>
    
        New-CsUCPhoneConfiguration -Identity "site:Redmond" -EnforcePhoneLock $True

</div>

<div>

## <a name="to-change-multiple-property-values-when-creating-new-lync-phone-edition-configuration-settings"></a><span data-ttu-id="22b01-133">So ändern Sie beim Erstellen neuer lync Phone Edition-Konfigurationseinstellungen mehrere Eigenschaftswerte</span><span class="sxs-lookup"><span data-stu-id="22b01-133">To change multiple property values when creating new Lync Phone Edition configuration settings</span></span>

  - <span data-ttu-id="22b01-134">Mehrere Eigenschaftswerte können geändert werden, indem Sie mehrere Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="22b01-134">Multiple property values can be modified by including multiple parameters.</span></span> <span data-ttu-id="22b01-135">Mit diesem Befehl wird beispielsweise die Telefon Verriegelung erzwungen und die minimale PIN-Länge auf 8 Ziffern festgelegt:</span><span class="sxs-lookup"><span data-stu-id="22b01-135">For example, this command enforces phone locking and also sets the minimum PIN length to 8 digits:</span></span>
    
        New-CsUCPhoneConfiguration -Identity "site:Redmond" -EnforcePhoneLock $True -MinPhonePinLength 8

</div>

<span data-ttu-id="22b01-136">Ausführliche Informationen finden Sie unter [New-CsUCPhoneConfiguration](https://technet.microsoft.com/library/Gg398445(v=OCS.15)).</span><span class="sxs-lookup"><span data-stu-id="22b01-136">For details, see [New-CsUCPhoneConfiguration](https://technet.microsoft.com/library/Gg398445(v=OCS.15)).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="22b01-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="22b01-137">See Also</span></span>


[<span data-ttu-id="22b01-138">Löschen einer vorhandenen Sammlung von lync Phone Edition-Konfigurationseinstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22b01-138">Delete an existing collection of Lync Phone Edition configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-lync-phone-edition-configuration-settings.md)  
[<span data-ttu-id="22b01-139">Konfigurieren von Sicherheitseinstellungen für lync Phone Edition in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22b01-139">Configure security settings for Lync Phone Edition in Lync Server 2013</span></span>](lync-server-2013-configure-security-settings-for-lync-phone-edition.md)  
[<span data-ttu-id="22b01-140">Erzwingen der Telefon Sperrung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="22b01-140">Enforce phone locking in Lync Server 2013</span></span>](lync-server-2013-enforce-phone-locking.md)  
  

<span data-ttu-id="22b01-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="22b01-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

