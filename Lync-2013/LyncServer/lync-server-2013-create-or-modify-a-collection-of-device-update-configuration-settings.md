---
title: Erstellen oder Ändern einer Sammlung von Konfigurationseinstellungen für Geräte Updates
description: Erstellen oder ändern Sie eine Sammlung von Konfigurationseinstellungen für Geräte Updates.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a collection of Device Update configuration settings
ms:assetid: 3e8ce95f-a8c8-417c-b1f7-0f759a567aff
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994029(v=OCS.15)
ms:contentKeyID: 51803938
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 593a1a0cb0f68254748ee48440cda18c78989780
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394379"
---
# <a name="create-or-modify-a-collection-of-device-update-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="99611-103">Erstellen oder Ändern einer Sammlung von Konfigurationseinstellungen für Geräte Updates in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="99611-103">Create or modify a collection of Device Update configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="99611-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="99611-104">

<span> </span></span></span>

<span data-ttu-id="99611-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="99611-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="99611-106">Konfigurationseinstellungen für Geräte Updates können (nur im Website Bereich) mithilfe von Windows PowerShell und dem Cmdlet **New-CsDeviceUpdateConfiguration** erstellt und mithilfe des Cmdlets " **Satz-CsDeviceUpdateConfiguration** " geändert werden.</span><span class="sxs-lookup"><span data-stu-id="99611-106">Device update configuration settings can be created (at the site scope only) by using Windows PowerShell and the **New-CsDeviceUpdateConfiguration** cmdlet and modified by using the **Set-CsDeviceUpdateConfiguration** cmdlet.</span></span> <span data-ttu-id="99611-107">Diese Cmdlets können entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="99611-107">These cmdlets can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]
> <span data-ttu-id="99611-108">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="99611-108">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<div>


<div>

## <a name="to-create-device-update-configuration-settings-that-use-the-default-values"></a><span data-ttu-id="99611-109">So erstellen Sie Konfigurationseinstellungen für Geräte Updates, die die Standardwerte verwenden</span><span class="sxs-lookup"><span data-stu-id="99611-109">To create device update configuration settings that use the default values</span></span>

  - <span data-ttu-id="99611-110">Mit diesem Befehl wird ein neuer Satz von Geräteupdate-Konfigurationseinstellungen für die Website "Redmond" erstellt:</span><span class="sxs-lookup"><span data-stu-id="99611-110">This command creates a new set of device update configuration settings for the Redmond site:</span></span>
    
        New-CsDeviceUpdateConfiguration -Identity "site:Redmond"
    
    <span data-ttu-id="99611-111">Da im vorhergehenden Befehl keine anderen Parameter als der Parameter für die obligatorische Identität angegeben wurden, werden in der neuen Sammlung der Konfigurationseinstellungen die Standardwerte für alle zugehörigen Eigenschaften verwendet.</span><span class="sxs-lookup"><span data-stu-id="99611-111">Because no parameters other than the mandatory Identity parameter were specified in the preceding command, the new collection of configuration settings will use the default values for all its properties.</span></span>

</div>

<div>

## <a name="to-change-a-single-property-value-when-creating-device-update-configuration-settings"></a><span data-ttu-id="99611-112">So ändern Sie einen einzelnen Eigenschaftswert beim Erstellen von Geräteupdate-Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="99611-112">To change a single property value when creating device update configuration settings</span></span>

  - <span data-ttu-id="99611-113">Um Einstellungen zu erstellen, die andere Eigenschaftswerte verwenden, geben Sie einfach den entsprechenden Parameter und Parameterwert ein.</span><span class="sxs-lookup"><span data-stu-id="99611-113">To create settings that use different property values, simply include the appropriate parameter and parameter value.</span></span> <span data-ttu-id="99611-114">Wenn Sie beispielsweise eine Sammlung von Konfigurationseinstellungen für Geräte Updates erstellen möchten, die standardmäßig alle 21 Tage alte Protokolldateien löscht, verwenden Sie einen Befehl wie den folgenden:</span><span class="sxs-lookup"><span data-stu-id="99611-114">For example, to create a collection of device update configuration settings that, by default, deletes old log files every 21 days, use a command like this one:</span></span>
    
        New-CsDeviceUpdateConfiguration -Identity "site:Redmond" -LogCleanupInterval "21.00:00:00"

</div>

<div>

## <a name="to-change-multiple-property-values-when-creating-device-update-configuration-settings"></a><span data-ttu-id="99611-115">So ändern Sie beim Erstellen von Geräteupdate-Konfigurationseinstellungen mehrere Eigenschaftswerte</span><span class="sxs-lookup"><span data-stu-id="99611-115">To change multiple property values when creating device update configuration settings</span></span>

  - <span data-ttu-id="99611-116">Mehrere Eigenschaftswerte können geändert werden, indem Sie mehrere Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="99611-116">Multiple property values can be modified by including multiple parameters.</span></span> <span data-ttu-id="99611-117">Mit diesem Befehl wird beispielsweise das Protokoll Bereinigungsintervall auf 21 Tage und das Protokoll leer Intervall auf 30 Minuten festgelegt:</span><span class="sxs-lookup"><span data-stu-id="99611-117">For example, this command sets the log cleanup interval to 21 days and the log flush interval to 30 minutes:</span></span>
    
        New-CsDeviceUpdateConfiguration -Identity "site:Redmond" -LogCleanupInterval "21.00:00:00" -LogFlushInterval "00:30:00"

</div>

<span data-ttu-id="99611-118">Details zum Ändern vorhandener Geräte Konfigurationseinstellungen finden Sie im Hilfethema zum Cmdlet " [setCsDeviceUpdateConfiguration](https://technet.microsoft.com/library/Gg398320(v=OCS.15)) ".</span><span class="sxs-lookup"><span data-stu-id="99611-118">For details about modifying existing device configuration settings, see the Help topic for the [Set-CsDeviceUpdateConfiguration](https://technet.microsoft.com/library/Gg398320(v=OCS.15)) cmdlet.</span></span> <span data-ttu-id="99611-119">Details zum Erstellen von Sammlungen von Konfigurationseinstellungen finden Sie im Hilfethema zum Cmdlet [New-CsDeviceUpdateConfiguration](https://technet.microsoft.com/library/Gg425761(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="99611-119">For details about creating collections of configuration settings, see the Help topic for the [New-CsDeviceUpdateConfiguration](https://technet.microsoft.com/library/Gg425761(v=OCS.15)) cmdlet.</span></span>

<span data-ttu-id="99611-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="99611-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

