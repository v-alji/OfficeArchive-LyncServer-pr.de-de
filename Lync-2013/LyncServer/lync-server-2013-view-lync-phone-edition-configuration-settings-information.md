---
title: 'Lync Server 2013: Anzeigen von Informationen zur Konfiguration der lync Phone Edition-Einstellungen'
description: 'Lync Server 2013: Anzeigen von Informationen zur Konfiguration der lync Phone Edition-Einstellungen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: View Lync Phone Edition configuration settings information
ms:assetid: 15f94478-651f-4063-9918-6a059f98df16
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687976(v=OCS.15)
ms:contentKeyID: 49733564
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 62719b24920ee72a92b2f80498d5ea2a59288c2e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440416"
---
# <a name="view-lync-phone-edition-configuration-settings-information-in-lync-server-2013"></a><span data-ttu-id="8c450-103">Anzeigen von Informationen zu den lync Phone Edition-Konfigurationseinstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c450-103">View Lync Phone Edition configuration settings information in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8c450-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8c450-104">

<span> </span></span></span>

<span data-ttu-id="8c450-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="8c450-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="8c450-106">Sie können Konfigurationsinformationen zu Geräten, auf denen lync Phone Edition ausgeführt wird, anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8c450-106">You can view configuration information about devices running Lync Phone Edition.</span></span> <span data-ttu-id="8c450-107">Die Informationen sind in Sammlungen gegliedert.</span><span class="sxs-lookup"><span data-stu-id="8c450-107">The information is organized into collections.</span></span> <span data-ttu-id="8c450-108">Wenn Sie lync Server installieren, erhalten Sie eine Sammlung von lync Phone Edition-Einstellungen, die für alle Geräte gelten, die lync Phone Edition in Ihrer Bereitstellung ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c450-108">When you install Lync Server, you get a collection of Lync Phone Edition settings that apply to all the devices running Lync Phone Edition in your deployment.</span></span> <span data-ttu-id="8c450-109">Sie können auch neue Sammlungen von Einstellungen für eine bestimmte Website erstellen.</span><span class="sxs-lookup"><span data-stu-id="8c450-109">You can also create new collections of settings for a specific site.</span></span> <span data-ttu-id="8c450-110">Websiteeinstellungen haben Vorrang vor globalen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="8c450-110">Site settings take precedence over global settings.</span></span> <span data-ttu-id="8c450-111">Jede Sammlung von Einstellungen besteht aus einem Namen, dem Bereich (Global oder Website), SIP-Sicherheitseinstellung, Protokollierungsstufe, Sprachdienst Qualität (QoS)-Ebene, Festlegung der Telefonsperre und Details zur Telefonsperre, also der Mindestlänge der PIN (persönliche Identifikationsnummer entsperren) und der Zeit, bevor sich das Telefon selbst sperrt.</span><span class="sxs-lookup"><span data-stu-id="8c450-111">Each collection of settings consists of a name, the scope (global or site), SIP security setting, logging level, voice quality of service (QoS) level, phone-lock setting, and phone-lock details, that is, the minimum length of the unlock personal identification number (PIN) and time before the phone locks itself.</span></span>

<div>

## <a name="to-view-configuration-information-about-devices-running-lync-phone-edition"></a><span data-ttu-id="8c450-112">So zeigen Sie Konfigurationsinformationen zu Geräten mit lync Phone Edition an</span><span class="sxs-lookup"><span data-stu-id="8c450-112">To view configuration information about devices running Lync Phone Edition</span></span>

1.  <span data-ttu-id="8c450-113">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="8c450-113">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="8c450-114">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="8c450-114">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="8c450-115">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="8c450-115">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="8c450-116">Klicken Sie in der linken Navigationsleiste auf **Clients**, und klicken Sie dann auf die Navigationsschaltfläche **Gerätekonfiguration** .</span><span class="sxs-lookup"><span data-stu-id="8c450-116">In the left navigation bar, click **Clients**, and then click the **Device Configuration** navigation button.</span></span>

4.  <span data-ttu-id="8c450-117">Klicken Sie auf der Seite **Device Configuration** auf die Sammlung von Einstellungen, über die Sie Informationen anzeigen möchten.</span><span class="sxs-lookup"><span data-stu-id="8c450-117">On the **Device Configuration** page, click the collection of settings you want to view information about.</span></span> <span data-ttu-id="8c450-118">Der Name, der Bereich, die SIP-Sicherheitseinstellung, die sprach Qualitätsstufe und die Einstellung der Telefonsperre sind auf der Hauptseite aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="8c450-118">The name, scope, SIP security setting, voice quality level, and phone lock setting are listed on the main page.</span></span> <span data-ttu-id="8c450-119">Klicken Sie auf das Menü **Bearbeiten** , und klicken Sie dann auf **Details anzeigen**, um die Details für Protokollierungsstufe und Telefonsperre anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="8c450-119">To view the logging level and phone lock details, click the **Edit** menu, and then click **Show details**.</span></span>

</div>

<div>

## <a name="viewing-lync-phone-edition-configuration-information-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="8c450-120">Anzeigen von Informationen zur lync Phone Edition-Konfiguration mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="8c450-120">Viewing Lync Phone Edition Configuration Information by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="8c450-121">Sie können die lync Phone Edition-Konfigurationseinstellungen mithilfe der lync Server-Verwaltungsshell und dem Cmdlet **Get-CsUCPhoneConfiguration** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="8c450-121">You can view Lync Phone Edition configuration settings by using Lync Server Management Shell and the **Get-CsUCPhoneConfiguration** cmdlet.</span></span> <span data-ttu-id="8c450-122">Sie können dieses Cmdlet in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="8c450-122">You can run this cmdlet can from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="8c450-123">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="8c450-123">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-view-lync-phone-edition-configuration-information"></a><span data-ttu-id="8c450-124">So zeigen Sie die lync Phone Edition-Konfigurationsinformationen an</span><span class="sxs-lookup"><span data-stu-id="8c450-124">To view Lync Phone Edition configuration information</span></span>

  - <span data-ttu-id="8c450-125">Wenn Sie Informationen zu allen ihren lync Phone Edition-Konfigurationseinstellungen anzeigen möchten, geben Sie den folgenden Befehl in der lync Server-Verwaltungsshell ein, und drücken Sie dann die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="8c450-125">To view information about all your Lync Phone Edition configuration settings, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsUCPhoneConfiguration
    
    <span data-ttu-id="8c450-126">Der Befehl gibt Informationen ähnlich der folgenden zurück:</span><span class="sxs-lookup"><span data-stu-id="8c450-126">The command returns information similar to the following:</span></span>
    
        Identity             : Global
        CalendarPollInterval : 00:03:00
        EnforcePhoneLock     : True
        PhoneLockTimeout     : 00:10:00
        MinPhonePinLength    : 6
        SIPSecurityMode      : High
        VoiceDiffServTag     : 40
        Voice8021p           : 0
        LoggingLevel         : Off

</div>

<span data-ttu-id="8c450-127">Ausführliche Informationen finden Sie unter [Get-CsUCPhoneConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsUCPhoneConfiguration).</span><span class="sxs-lookup"><span data-stu-id="8c450-127">For details, see [Get-CsUCPhoneConfiguration](https://docs.microsoft.com/powershell/module/skype/Get-CsUCPhoneConfiguration).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8c450-128">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8c450-128">See Also</span></span>


[<span data-ttu-id="8c450-129">Erstellen oder Ändern einer Sammlung von lync Phone Edition-Konfigurationseinstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c450-129">Create or modify a collection of Lync Phone Edition configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-collection-of-lync-phone-edition-configuration-settings.md)  
[<span data-ttu-id="8c450-130">Löschen einer vorhandenen Sammlung von lync Phone Edition-Konfigurationseinstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c450-130">Delete an existing collection of Lync Phone Edition configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-lync-phone-edition-configuration-settings.md)  
[<span data-ttu-id="8c450-131">Konfigurieren von Sicherheitseinstellungen für lync Phone Edition in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c450-131">Configure security settings for Lync Phone Edition in Lync Server 2013</span></span>](lync-server-2013-configure-security-settings-for-lync-phone-edition.md)  
[<span data-ttu-id="8c450-132">Erzwingen der Telefon Sperrung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8c450-132">Enforce phone locking in Lync Server 2013</span></span>](lync-server-2013-enforce-phone-locking.md)  
  

<span data-ttu-id="8c450-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8c450-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

