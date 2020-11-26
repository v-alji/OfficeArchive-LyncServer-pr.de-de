---
title: Verwalten der Konfigurationseinstellungen für den zentralisierten Protokollierungsdienst
description: Verwalten der Konfigurationseinstellungen für den zentralisierten Protokollierungsdienst
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing the Centralized Logging Service configuration settings
ms:assetid: f455c3aa-0061-413d-bdfb-a3e78f82723d
ms:mtpsurl: https://technet.microsoft.com/library/JJ721938(v=OCS.15)
ms:contentKeyID: 49733875
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e25294e096b8368aa06a11e4ad851fe5d1a84c0f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425899"
---
# <a name="managing-the-centralized-logging-service-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="21e3f-103">Verwalten der Konfigurationseinstellungen für den zentralisierten Protokollierungsdienst in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="21e3f-103">Managing the Centralized Logging Service configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="21e3f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="21e3f-104">

<span> </span></span></span>

<span data-ttu-id="21e3f-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="21e3f-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="21e3f-106">Der zentralisierte Protokollierungsdienst wird von Einstellungen und Parametern gesteuert und konfiguriert, die vom zentralen Protokollierungsdienst Controller (CLSController) erstellt und verwendet werden, um Befehle an den zentralen Protokollierungsdienst-Agent (CLSAgent) des jeweiligen Computers zu senden.</span><span class="sxs-lookup"><span data-stu-id="21e3f-106">The Centralized Logging Service is controlled and configured by settings and parameters that are created and used by the Centralized Logging Service Controller (CLSController) to send commands to the individual computer’s Centralized Logging Service Agent (CLSAgent).</span></span> <span data-ttu-id="21e3f-107">Der Agent verarbeitet die an ihn gesendeten Befehle und verwendet (im Fall eines Start Befehls) die Konfiguration der Szenarien, Anbieter, Protokollgröße, Ablauf Verfolgungs Dauer und Flags, um mit dem Sammeln von Ablaufverfolgungsprotokollen entsprechend den bereitgestellten Konfigurationsinformationen zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="21e3f-107">The agent processes the commands that are sent to it and (in the case of a Start command) uses the configuration of the scenarios, providers, log size, trace duration, and flags to begin collecting trace logs according to the configuration information provided.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="21e3f-108">Nicht alle Windows PowerShell-Cmdlets, die für den zentralisierten Protokollierungsdienst aufgelistet sind, sind für die Verwendung in lokalen Bereitstellungen von lync Server 2013 vorgesehen.</span><span class="sxs-lookup"><span data-stu-id="21e3f-108">Not all Windows PowerShell cmdlets listed for the Centralized Logging Service are intended for use with Lync Server 2013 on-premises deployments.</span></span> <span data-ttu-id="21e3f-109">Obwohl Sie anscheinend funktionieren, sind die folgenden Cmdlets nicht für die Funktion mit lync Server 2013-lokalen Bereitstellungen vorgesehen:</span><span class="sxs-lookup"><span data-stu-id="21e3f-109">Although they may appear to work, the following cmdlets are not designed to function with Lync Server 2013 on-premises deployments:</span></span> 
> <UL>
> <LI>
> <P><span data-ttu-id="21e3f-110"><STRONG>CsClsRegion-Cmdlets:</STRONG> <A href="https://technet.microsoft.com/library/JJ204879(v=OCS.15)">Get-CsClsRegion</A>, <A href="https://technet.microsoft.com/library/JJ204746(v=OCS.15)">Sets-CsClsRegion</A>, <A href="https://technet.microsoft.com/library/JJ204658(v=OCS.15)">New-CsClsRegion</A>und <A href="https://technet.microsoft.com/library/JJ204971(v=OCS.15)">Remove-CsClsRegion</A>.</span><span class="sxs-lookup"><span data-stu-id="21e3f-110"><STRONG>CsClsRegion cmdlets:</STRONG> <A href="https://technet.microsoft.com/library/JJ204879(v=OCS.15)">Get-CsClsRegion</A>, <A href="https://technet.microsoft.com/library/JJ204746(v=OCS.15)">Set-CsClsRegion</A>, <A href="https://technet.microsoft.com/library/JJ204658(v=OCS.15)">New-CsClsRegion</A>, and <A href="https://technet.microsoft.com/library/JJ204971(v=OCS.15)">Remove-CsClsRegion</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="21e3f-111"><STRONG>CsClsSearchTerm-Cmdlets:</STRONG> <A href="https://technet.microsoft.com/library/JJ205061(v=OCS.15)">Get-CsClsSearchTerm</A> und <A href="https://technet.microsoft.com/library/JJ204911(v=OCS.15)">setCsClsSearchTerm</A>.</span><span class="sxs-lookup"><span data-stu-id="21e3f-111"><STRONG>CsClsSearchTerm cmdlets:</STRONG> <A href="https://technet.microsoft.com/library/JJ205061(v=OCS.15)">Get-CsClsSearchTerm</A> and <A href="https://technet.microsoft.com/library/JJ204911(v=OCS.15)">Set-CsClsSearchTerm</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="21e3f-112"><STRONG>CsClsSecurityGroup-Cmdlets:</STRONG> <A href="https://technet.microsoft.com/library/JJ205285(v=OCS.15)">Get-CsClsSecurityGroup</A>, <A href="https://technet.microsoft.com/library/JJ204700(v=OCS.15)">Sets-CsClsSecurityGroup</A>, <A href="https://technet.microsoft.com/library/JJ205359(v=OCS.15)">New-CsClsSecurityGroup</A>und <A href="https://technet.microsoft.com/library/JJ204958(v=OCS.15)">Remove-CsClsSecurityGroup</A>.</span><span class="sxs-lookup"><span data-stu-id="21e3f-112"><STRONG>CsClsSecurityGroup cmdlets:</STRONG> <A href="https://technet.microsoft.com/library/JJ205285(v=OCS.15)">Get-CsClsSecurityGroup</A>, <A href="https://technet.microsoft.com/library/JJ204700(v=OCS.15)">Set-CsClsSecurityGroup</A>, <A href="https://technet.microsoft.com/library/JJ205359(v=OCS.15)">New-CsClsSecurityGroup</A>, and <A href="https://technet.microsoft.com/library/JJ204958(v=OCS.15)">Remove-CsClsSecurityGroup</A>.</span></span></P></LI></UL><span data-ttu-id="21e3f-113">Die in diesen Cmdlets definierten Einstellungen behindern nicht oder führen zu unerwünschtem Verhalten, sind aber für die Verwendung mit Microsoft 365 konzipiert und liefern in lokalen Bereitstellungen keine erwarteten Ergebnisse.</span><span class="sxs-lookup"><span data-stu-id="21e3f-113">The settings defined in these cmdlets will not hinder or cause any adverse behavior, but they are designed for use with Microsoft 365 and will not yield the expected results in on-premises deployments.</span></span> <span data-ttu-id="21e3f-114">Das bedeutet nicht, dass diese Cmdlets in lokalen Bereitstellungen nicht von Nutzen sind, ihre Verwendung ist aber ein komplexes Thema, dessen Beschreibung den Rahmen dieser Dokumentation sprengen würde.</span><span class="sxs-lookup"><span data-stu-id="21e3f-114">This is not to say that there is no use for these cmdlets in on-premises deployments, but their use is a more advanced topic that is not covered in this documentation.</span></span>


</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="21e3f-115">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="21e3f-115">In This Section</span></span>

<span data-ttu-id="21e3f-116">In den Themen in diesem Abschnitt werden die Konfigurationsoptionen, Parameter und Einstellungen für den zentralisierten Protokollierungsdienst definiert.</span><span class="sxs-lookup"><span data-stu-id="21e3f-116">The topics in this section define the configuration options, parameters, and settings for the Centralized Logging Service.</span></span> <span data-ttu-id="21e3f-117">Informationen zum Konfigurieren des zentralen Protokollierungsdiensts, zum Abrufen der Konfigurationseinstellungen, zum Erstellen von Szenarien, zum Verwalten von Sicherheitsgruppen für den zentralisierten Protokollierungsdienst, suchen und mehr finden Sie in den folgenden Themen.</span><span class="sxs-lookup"><span data-stu-id="21e3f-117">Information about how to configure the Centralized Logging Service, how to retrieve the configuration settings, creation of scenarios, management of security groups for Centralized Logging Service, searching, and more is contained in the following topics.</span></span>

  - [<span data-ttu-id="21e3f-118">Verwalten der Konfiguration von Computer, Website und globaler zentralisierter Protokollierungsdienst in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="21e3f-118">Managing computer, site and global Centralized Logging Service configuration in Lync Server 2013</span></span>](lync-server-2013-managing-computer-site-and-global-centralized-logging-service-configuration.md)

  - [<span data-ttu-id="21e3f-119">Konfigurieren von Anbietern für den zentralisierten Protokollierungsdienst in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="21e3f-119">Configuring providers for Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-configuring-providers-for-centralized-logging-service.md)

  - [<span data-ttu-id="21e3f-120">Konfigurieren von Szenarien für den zentralisierten Protokollierungsdienst in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="21e3f-120">Configuring scenarios for the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-configuring-scenarios-for-the-centralized-logging-service.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="21e3f-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="21e3f-121">See Also</span></span>


[<span data-ttu-id="21e3f-122">Übersicht über den zentralisierten Protokollierungsdienst in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="21e3f-122">Overview of the Centralized Logging Service in Lync Server 2013</span></span>](lync-server-2013-overview-of-the-centralized-logging-service.md)  
[<span data-ttu-id="21e3f-123">Cmdlets für die zentralisierte Protokollierung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="21e3f-123">Centralized Logging cmdlets in Lync Server 2013</span></span>](lync-server-2013-centralized-logging-cmdlets.md)  
  

<span data-ttu-id="21e3f-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="21e3f-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

