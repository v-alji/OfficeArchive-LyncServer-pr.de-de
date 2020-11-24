---
title: 'Lync Server 2013: Konfiguration von standortbasiertem Routing für Konferenzen'
description: 'Lync Server 2013: Konfiguration von Location-Based Routing für Konferenzen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuration of Location-Based Routing for conferencing
ms:assetid: d8c708cc-a1b1-48b1-808c-a64df15f7701
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362846(v=OCS.15)
ms:contentKeyID: 56335088
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a87f9c799e565f64b0dd30ce025a4e7a3174625
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395159"
---
# <a name="configuration-of-location-based-routing-for-conferencing-in-lync-server-2013"></a><span data-ttu-id="6eb97-103">Konfiguration von standortbasiertem Routing für Konferenzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6eb97-103">Configuration of Location-Based Routing for conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6eb97-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6eb97-104">

<span> </span></span></span>

<span data-ttu-id="6eb97-105">_**Letztes Änderungsdatum des Themas:** 2013-09-11_</span><span class="sxs-lookup"><span data-stu-id="6eb97-105">_**Topic Last Modified:** 2013-09-11_</span></span>

<span data-ttu-id="6eb97-106">Die Location-Based Routing Konferenz Anwendung basiert auf der Konfiguration von lync Server 2013 Location-Based-Routing.</span><span class="sxs-lookup"><span data-stu-id="6eb97-106">The Location-Based Routing Conferencing application relies on the configuration of Lync Server 2013 Location-Based Routing.</span></span> <span data-ttu-id="6eb97-107">Die wichtigsten Konfigurationen sind die folgenden:</span><span class="sxs-lookup"><span data-stu-id="6eb97-107">The main configurations are the following:</span></span>

  - <span data-ttu-id="6eb97-108">Die Position der Teilnehmer, die an einer Besprechung teilnehmen, wird basierend auf Ihrer Netzwerk Website festgelegt.</span><span class="sxs-lookup"><span data-stu-id="6eb97-108">The location of participants joining a meeting is determined based on their network site.</span></span> <span data-ttu-id="6eb97-109">Eine Netzwerk Website und die zugehörigen Netzwerk-Subnetze müssen in lync Server definiert werden, um Location-Based Routing durchzusetzen.</span><span class="sxs-lookup"><span data-stu-id="6eb97-109">A network site and its associated network subnets must be defined in Lync Server in order to enforce Location-Based Routing.</span></span>

  - <span data-ttu-id="6eb97-110">Um Location-Based Routing von Besprechungen durchzusetzen, müssen lync-Teilnehmer für Location-Based Routing aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="6eb97-110">To enforce Location-Based Routing of meetings, Lync participants must be enabled for Location-Based Routing.</span></span>

  - <span data-ttu-id="6eb97-111">Um Location-Based Routing von PSTN-Endpunkten durchzusetzen, die an Besprechungen teilnehmen, muss der für die Verbindung der PSTN-Endpunkte verwendete SIP-Trunk für Location-Based Routing konfiguriert sein</span><span class="sxs-lookup"><span data-stu-id="6eb97-111">To enforce Location-Based Routing of PSTN endpoints joining meetings, the SIP trunk used to connect the PSTN endpoints must be configured for Location-Based Routing.</span></span>

<span data-ttu-id="6eb97-112">Weitere Informationen zum Bereitstellen und Konfigurieren von lync Server 2013 Location-Based-Routing finden Sie unter Konfigurieren des [standortbasierten Routings](lync-server-2013-configuring-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="6eb97-112">For additional information on deploying and configuring Lync Server 2013 Location-Based Routing, please refer Configuring [Location-Based Routing](lync-server-2013-configuring-location-based-routing.md).</span></span>

<div>

## <a name="enabling-the-location-based-routing-conferencing-application"></a><span data-ttu-id="6eb97-113">Aktivieren der Location-Based Routing Konferenz Anwendung</span><span class="sxs-lookup"><span data-stu-id="6eb97-113">Enabling the Location-Based Routing Conferencing Application</span></span>

<span data-ttu-id="6eb97-114">Die Location-Based-Routing Konferenz Anwendung ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="6eb97-114">The Location-Based Routing Conferencing application is disabled by default.</span></span> <span data-ttu-id="6eb97-115">Bevor Sie diese Anwendung aktivieren, müssen Sie die richtige Priorität ermitteln, die für die Anwendung zugewiesen werden soll.</span><span class="sxs-lookup"><span data-stu-id="6eb97-115">Before enabling this application, you need to determine the right priority to assign for the application.</span></span> <span data-ttu-id="6eb97-116">Führen Sie das folgende Cmdlet in der lync Server-Verwaltungsshell aus, um diese Priorität zu ermitteln:</span><span class="sxs-lookup"><span data-stu-id="6eb97-116">To determine this priority, run the following cmdlet in Lync Server Management Shell:</span></span>

```powershell
Get-CsServerApplication -Identity Service:Registrar:<Pool FQDN>
```

<span data-ttu-id="6eb97-117">In diesem Cmdlet \<Pool FQDN\> ist der Pool, in dem die Location-Based Routing Konferenz Anwendung aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="6eb97-117">In this cmdlet, \<Pool FQDN\> is the pool in which the Location-Based Routing Conferencing application is to be enabled.</span></span>

<span data-ttu-id="6eb97-118">Dieses Cmdlet gibt die Liste der von lync Server gehosteten Anwendungen zurück, und der Prioritätswert für jeden von Ihnen.</span><span class="sxs-lookup"><span data-stu-id="6eb97-118">This cmdlet will return the list of the applications hosted by Lync Server and the priority value for each of them.</span></span> <span data-ttu-id="6eb97-119">Der Location-Based Routing Konferenz Anwendung muss ein Prioritätswert zugewiesen werden, der größer als die Anwendung "UdcAgent" und kleiner als die Anwendungen "DefaultRouting", "ExumRouting" und "OutboundRouting" ist.</span><span class="sxs-lookup"><span data-stu-id="6eb97-119">The Location-Based Routing Conferencing application needs to be assigned a priority value larger than the “UdcAgent” application and smaller than the “DefaultRouting”, “ExumRouting” and “OutboundRouting” applications.</span></span> <span data-ttu-id="6eb97-120">Wir empfehlen, dass Sie der Location-Based Routing Konferenz Anwendung einen Prioritätswert zuweisen, der einen Punkt höher als der Prioritätswert der Anwendung "UdcAgent" ist.</span><span class="sxs-lookup"><span data-stu-id="6eb97-120">We recommend that you assign the Location-Based Routing Conferencing application a priority value that is one point higher than the priority value of the “UdcAgent” application.</span></span>

<span data-ttu-id="6eb97-121">Wenn beispielsweise die Anwendung "UdcAgent" einen Prioritätswert von "2" aufweist, hat die Anwendung "DefaultRouting" den Prioritätswert "8", die "ExumRouting"-Anwendung einen Prioritätswert von "9" und die "OutboundRouting"-Anwendung einen Prioritätswert von "10", und Sie sollten der Location-Based Routing Konferenz Anwendung einen Prioritätswert von "3" zuweisen.</span><span class="sxs-lookup"><span data-stu-id="6eb97-121">For example, if the “UdcAgent” application has a priority value of “2”, the “DefaultRouting” application has a priority value of “8”, the “ExumRouting” application has a priority value of “9” and the “OutboundRouting” application has a priority value of “10” then you should assign the Location-Based Routing Conferencing application a priority value of “3”.</span></span> <span data-ttu-id="6eb97-122">Auf diese Weise würde die Priorität der Anwendungen in der folgenden Reihenfolge platziert: andere Anwendungen (Prioritäten: 0 bis 1), "UdcAgent" (Priorität: 2), Location-Based Routing Konferenz Anwendung (Priorität: 3), andere Anwendungen (Prioritäten: 4 bis 8), "DefaultRouting" (Priorität: 9), "ExumRouting" (Priorität: 10) und "OutboundRouting" (Priorität: 11).</span><span class="sxs-lookup"><span data-stu-id="6eb97-122">Doing so would place the priority of the applications in the following order: Other applications (Priorities: 0 to 1), “UdcAgent” (Priority: 2), Location-Based Routing Conferencing application (Priority: 3), other applications (Priorities: 4 to 8), “DefaultRouting” (Priority: 9), “ExumRouting” (Priority: 10) and “OutboundRouting” (Priority: 11).</span></span>

<span data-ttu-id="6eb97-123">Nachdem Sie den richtigen Prioritätswert für die Location-Based Routing Konferenz Anwendung gefunden haben, geben Sie das folgende Cmdlet für jeden Front-End Pool oder Standard Edition-Server ein, auf dem Benutzer für Location-Based Routing aktiviert sind:</span><span class="sxs-lookup"><span data-stu-id="6eb97-123">After you find the correct priority value for the Location-Based Routing Conferencing application, type the following cmdlet for each Front-End pool or Standard Edition Server that homes users enabled for Location-Based Routing:</span></span>

```powershell
New-CsServerApplication -Identity Service:Registrar:<Pool FQDN>/LBRouting -Priority <Application Priority> -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

<span data-ttu-id="6eb97-124">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="6eb97-124">For example:</span></span>

```powershell
New-CsServerApplication -Identity Service:Registrar:LS2013CU2LBRPool.contoso.com/LBRouting -Priority 3 -Enabled $true -Critical $true -Uri http://www.microsoft.com/LCS/LBRouting
```

<span data-ttu-id="6eb97-125">Nachdem Sie dieses Cmdlet verwendet haben, starten Sie alle Front-End-Server im Pool oder die Standard Edition-Server neu, auf denen die Location-Based Routing Konferenz Anwendung aktiviert wurde.</span><span class="sxs-lookup"><span data-stu-id="6eb97-125">After using this cmdlet, restart all Front End servers in the pool or the Standard Edition Servers where the Location-Based Routing Conferencing application has been enabled.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="6eb97-126">Location-Based-Routing-Erzwingung von Konferenzen oder beratenden Übertragungen wird erst erzwungen, wenn alle Front-End-Server in den entsprechenden Pools oder den Standard Edition-Servern neu gestartet werden.</span><span class="sxs-lookup"><span data-stu-id="6eb97-126">Location-Based Routing enforcements to conferences or consultative transfers won’t be enforced until all the Front End Servers in the applicable pools or the Standard Edition Servers are restarted.</span></span>



</div>

<span data-ttu-id="6eb97-127">Nachdem die Location-Based Routing Konferenz Anwendung erfolgreich aktiviert wurde und alle anwendbaren lync-Server neu gestartet wurden, werden alle Konferenzen, die von lync-Benutzern für Location-Based Routing aktiviert wurden, überwacht, um eine PSTN-Maut Umgehung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="6eb97-127">Once the Location-Based Routing Conferencing application has been successfully enabled and all applicable Lync servers have been restarted, all conferences organized by Lync users enabled for Location-Based Routing will be monitored to prevent PSTN toll bypass</span></span>

<span data-ttu-id="6eb97-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6eb97-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

