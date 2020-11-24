---
title: Erstellen oder Ändern einer Sammlung von a/V-Edgeserver-Konfigurationseinstellungen
description: Erstellen oder ändern Sie eine Sammlung von a/V-Edgeserver-Konfigurationseinstellungen.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a collection of A/V Edge Server configuration settings
ms:assetid: 43899518-59c6-4be4-8892-d6f6207bfaab
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688039(v=OCS.15)
ms:contentKeyID: 49733630
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3cdf7dca19446f4eac584564eed776f7fde47bfe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394763"
---
# <a name="create-or-modify-a-collection-of-av-edge-server-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="fb4fd-103">Erstellen oder Ändern einer Sammlung von a/V-Edgeserver-Konfigurationseinstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fb4fd-103">Create or modify a collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fb4fd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fb4fd-104">

<span> </span></span></span>

<span data-ttu-id="fb4fd-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="fb4fd-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="fb4fd-106">Der a/V-Edgedienst bietet internen Benutzern (Benutzern, die bei Ihrem Unternehmensnetzwerk angemeldet sind) die Möglichkeit, Audio und Video für externe Benutzer freizugeben (Benutzer, die nicht bei Ihrem Organisationsnetzwerk angemeldet sind).</span><span class="sxs-lookup"><span data-stu-id="fb4fd-106">The A/V Edge service provide a way for your internal users (users who are logged on to your organizational network) to share audio and video with external users (users who are not logged on to your organizational network).</span></span> <span data-ttu-id="fb4fd-107">Der a/v-Edgedienst wird in erster Linie mithilfe von a/v-Edge-Konfigurationseinstellungen verwaltet, die für den Website Bereich oder den Dienstbereich konfiguriert werden können (d. h., Sie können für einen einzelnen a/v-Edgeserver konfiguriert werden).</span><span class="sxs-lookup"><span data-stu-id="fb4fd-107">The A/V Edge service is primarily managed by using A/V Edge configuration settings, setting that can be configured at the site scope or at the service scope (that is, can be configured for an individual A/V Edge server).</span></span>

<span data-ttu-id="fb4fd-108">Wenn Sie lync Server installieren, wird eine globale Sammlung von a/V-Edge-Konfigurationseinstellungen für Sie erstellt.</span><span class="sxs-lookup"><span data-stu-id="fb4fd-108">When you install Lync Server, a global collection of A/V Edge configuration settings is created for you.</span></span> <span data-ttu-id="fb4fd-109">Darüber hinaus können Sie die Windows PowerShell und das New-CsAVEdgeConfiguration-Cmdlet verwenden, um neue Einstellungen für den Website Bereich oder den Dienstbereich (also für einen einzelnen A/V-Edgeserver) zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fb4fd-109">In addition to that, you can use the Windows PowerShell and the New-CsAVEdgeConfiguration cmdlet to create new settings at the site scope or the service scope (that is, for an individual A/V Edge server).</span></span> <span data-ttu-id="fb4fd-110">Beachten Sie beim Erstellen neuer Einstellungen Folgendes:</span><span class="sxs-lookup"><span data-stu-id="fb4fd-110">If you create new settings keep in mind that:</span></span>

  - <span data-ttu-id="fb4fd-111">Im Dienstbereich konfigurierte Einstellungen (also auf einem einzelnen Server) haben Vorrang vor allem.</span><span class="sxs-lookup"><span data-stu-id="fb4fd-111">Settings configured at the service scope (that is, on an individual server) take priority over everything.</span></span>

  - <span data-ttu-id="fb4fd-112">Die für den Website Bereich konfigurierten Einstellungen haben Vorrang vor den im globalen Bereich konfigurierten Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="fb4fd-112">Settings configured at the site scope take priority over settings configured at the global scope.</span></span> <span data-ttu-id="fb4fd-113">Dienstbereichs Einstellungen ersetzen jedoch auch die Einstellungen für den Website Bereich.</span><span class="sxs-lookup"><span data-stu-id="fb4fd-113">However, service scope settings will also supersede site-scope settings.</span></span>

  - <span data-ttu-id="fb4fd-114">Einstellungen im globalen Bereich werden nur verwendet, wenn auf dem einzelnen Server keine Diensteinstellungen konfiguriert sind und keine Websiteeinstellungen für die Website vorhanden sind, auf der sich der Server befindet.</span><span class="sxs-lookup"><span data-stu-id="fb4fd-114">Settings at the global scope will be used only if there are no service settings configured on the individual server and if there are no site settings for the site where that server is located.</span></span>

<span data-ttu-id="fb4fd-115">Alle Einstellungen können dann mithilfe des Set-CsAVEdgeConfiguration-Cmdlets geändert werden.</span><span class="sxs-lookup"><span data-stu-id="fb4fd-115">Any of your settings can then be modified by using the Set-CsAVEdgeConfiguration cmdlet.</span></span> <span data-ttu-id="fb4fd-116">Weitere Informationen finden Sie in den Hilfethemen zu den Cmdlets [New-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412884(v=OCS.15)) und Cmdlets für [festgelegte CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412869(v=OCS.15)) .</span><span class="sxs-lookup"><span data-stu-id="fb4fd-116">For more information, see the help topics for the [New-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412884(v=OCS.15)) and the [Set-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412869(v=OCS.15)) cmdlets.</span></span>

<div>

## <a name="to-create-new-av-edge-configuration-settings-at-the-site-scope"></a><span data-ttu-id="fb4fd-117">So erstellen Sie neue A/V-Edge-Konfigurationseinstellungen im Website Bereich</span><span class="sxs-lookup"><span data-stu-id="fb4fd-117">To create new A/V Edge configuration settings at the site scope</span></span>

  - <span data-ttu-id="fb4fd-118">Mit dem folgenden Befehl wird eine neue Sammlung von a/V-Edge-Konfigurationseinstellungen für die Website "Redmond" erstellt:</span><span class="sxs-lookup"><span data-stu-id="fb4fd-118">The following command creates a new collection of A/V Edge configuration settings for the Redmond site:</span></span>
    
        New-CsAVEdgeConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-create-custom-av-edge-configuration-settings-at-the-site-scope"></a><span data-ttu-id="fb4fd-119">So erstellen Sie benutzerdefinierte A/V-Edge-Konfigurationseinstellungen im Website Bereich</span><span class="sxs-lookup"><span data-stu-id="fb4fd-119">To create custom A/V Edge configuration settings at the site scope</span></span>

  - <span data-ttu-id="fb4fd-120">Da keine zusätzlichen Parameter enthalten sind, verwenden diese neuen Einstellungen die Standardwerte für den A/V-Edgedienst.</span><span class="sxs-lookup"><span data-stu-id="fb4fd-120">Because no additional parameters were included, these new settings will use the default values for the A/V Edge service.</span></span> <span data-ttu-id="fb4fd-121">Alternativ können Sie zusätzliche Parameter und Parameterwerte hinzufügen, um eine benutzerdefinierte Sammlung zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="fb4fd-121">Alternatively, you can add additional parameters and parameter values to create a custom collection.</span></span> <span data-ttu-id="fb4fd-122">Mit diesem Befehl wird beispielsweise die MaxTokenLifetime-Eigenschaft auf 4 Stunden (04 Stunden: 00 Minuten: 00 Sekunden) festgelegt:</span><span class="sxs-lookup"><span data-stu-id="fb4fd-122">For example, this command sets the MaxTokenLifetime property to 4 hours (04 hours : 00 minutes : 00 seconds):</span></span>
    
        New-CsAVEdgeConfiguration -Identity "site:Redmond" -MaxTokenLifetime "04:00:00"

</div>

<div>

## <a name="to-create-custom-av-edge-configuration-settings-at-the-service-scope"></a><span data-ttu-id="fb4fd-123">So erstellen Sie benutzerdefinierte A/V-Edge-Konfigurationseinstellungen im Dienstbereich</span><span class="sxs-lookup"><span data-stu-id="fb4fd-123">To create custom A/V Edge configuration settings at the service scope</span></span>

  - <span data-ttu-id="fb4fd-124">Mit diesem Befehl wird eine ähnliche Sammlung erstellt, die auf die a/V-Edgeserver-ATL-Edge-001.litwareinc.com angewendet wurde:</span><span class="sxs-lookup"><span data-stu-id="fb4fd-124">This command creates a similar collection applied to the A/V Edge server atl-edge-001.litwareinc.com:</span></span>
    
        New-CsAVEdgeConfiguration -Identity "service:EdgeServer:atl-edge-001.litwareinc.com" -MaxTokenLifetime "04:00:00"

</div>

<div>

## <a name="to-modify-existing-av-edge-configuration-settings"></a><span data-ttu-id="fb4fd-125">So ändern Sie vorhandene A/V-Edge-Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="fb4fd-125">To modify existing A/V Edge configuration settings</span></span>

  - <span data-ttu-id="fb4fd-126">In diesem Beispiel wird das Set-CsAVEdgeConfiguration-Cmdlet verwendet, um die maximale Token-Lebensdauer für den Standort Redmond auf 12 Stunden zu ändern:</span><span class="sxs-lookup"><span data-stu-id="fb4fd-126">In this example, the Set-CsAVEdgeConfiguration cmdlet is used to change the maximum token lifetime for the Redmond site to 12 hours:</span></span>
    
        Set-CsAVEdgeConfiguration -Identity "site:Redmond" -MaxTokenLifetime "12:00:00"

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="fb4fd-127">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fb4fd-127">See Also</span></span>


[<span data-ttu-id="fb4fd-128">Zurückgeben von A/V-Edgeserver-Konfigurationsinformationen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fb4fd-128">Return A/V Edge Server configuration information in Lync Server 2013</span></span>](lync-server-2013-return-a-v-edge-server-configuration-information.md)  
[<span data-ttu-id="fb4fd-129">Löschen einer vorhandenen Sammlung von A/V-Edgeserver-Konfigurationseinstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fb4fd-129">Delete an existing collection of A/V Edge Server configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-a-v-edge-server-configuration-settings.md)  


[<span data-ttu-id="fb4fd-130">Audio/Video-Edgeserver (A/V) in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fb4fd-130">Audio/Video (A/V) Edge Servers in Lync Server 2013</span></span>](lync-server-2013-audio-video-a-v-edge-servers.md)  
<span data-ttu-id="fb4fd-131">[Neu – CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412884(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="fb4fd-131">[New-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412884(v=OCS.15))</span></span>  
<span data-ttu-id="fb4fd-132">[Satz-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412869(v=OCS.15))</span><span class="sxs-lookup"><span data-stu-id="fb4fd-132">[Set-CsAVEdgeConfiguration](https://technet.microsoft.com/library/Gg412869(v=OCS.15))</span></span>  
  

<span data-ttu-id="fb4fd-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fb4fd-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

