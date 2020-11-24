---
title: 'Lync Server 2013: aktivieren Location-Based Routings'
description: 'Lync Server 2013: aktivieren Location-Based Routings'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling Location-Based Routing
ms:assetid: 029ede7e-0c4e-4ad2-af99-909ae674d6fe
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994014(v=OCS.15)
ms:contentKeyID: 51803920
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7844af5792468cd5645b6b42c857c63b943c2df1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394718"
---
# <a name="enabling-location-based-routing-in-lync-server-2013"></a><span data-ttu-id="d1e76-103">Aktivieren von Location-Based-Routing in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d1e76-103">Enabling Location-Based Routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d1e76-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d1e76-104">

<span> </span></span></span>

<span data-ttu-id="d1e76-105">_**Letztes Änderungsdatum des Themas:** 2013-04-26_</span><span class="sxs-lookup"><span data-stu-id="d1e76-105">_**Topic Last Modified:** 2013-04-26_</span></span>

<span data-ttu-id="d1e76-106">Nachdem Enterprise-VoIP bereitgestellt und netzwerkregionen,-Websites und-Subnetze definiert sind, können Sie Location-Based Routing aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d1e76-106">Once Enterprise Voice is deployed and network regions, sites and subnets are defined, you can enable Location-Based Routing.</span></span> <span data-ttu-id="d1e76-107">Location-Based Routing muss für die folgenden Enterprise-VoIP-Elemente aktiviert sein:</span><span class="sxs-lookup"><span data-stu-id="d1e76-107">Location-Based Routing must be enabled for the following Enterprise Voice elements:</span></span>

  - <span data-ttu-id="d1e76-108">Netzwerk Websites</span><span class="sxs-lookup"><span data-stu-id="d1e76-108">Network sites</span></span>

  - <span data-ttu-id="d1e76-109">Trunk-Konfigurationen</span><span class="sxs-lookup"><span data-stu-id="d1e76-109">Trunk configurations</span></span>

  - <span data-ttu-id="d1e76-110">VoIP-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d1e76-110">Voice policies</span></span>

  - <span data-ttu-id="d1e76-111">Routing Konfiguration</span><span class="sxs-lookup"><span data-stu-id="d1e76-111">Routing configuration</span></span>

<div>

## <a name="enable-location-based-routing-to-network-sites"></a><span data-ttu-id="d1e76-112">Aktivieren Location-Based Routings auf Netzwerk Websites</span><span class="sxs-lookup"><span data-stu-id="d1e76-112">Enable Location-Based Routing to Network Sites</span></span>

<span data-ttu-id="d1e76-113">Nachdem Sie Enterprise-VoIP und konfigurierte Netzwerk Websites bereitgestellt haben, können Sie Location-Based Routing konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="d1e76-113">After you have deployed Enterprise Voice, and configured network sites, you are ready to configure Location-Based Routing.</span></span> <span data-ttu-id="d1e76-114">Zuerst erstellen Sie eine VoIP-Routing Richtlinie, um die Netzwerk Website mit den entsprechenden PSTN-Nutzungen zu verknüpfen.</span><span class="sxs-lookup"><span data-stu-id="d1e76-114">First, you create a voice routing policy to associate the network site with the appropriate PSTN usages.</span></span> <span data-ttu-id="d1e76-115">Stellen Sie beim Zuweisen von PSTN-Nutzungen zu einer VoIP-Routing Richtlinie sicher, dass nur PSTN-Nutzungen verwendet werden, die VoIP-Routen zugeordnet sind, die ein lokales PSTN-Gateway für die Website oder ein PSTN-Gateway verwenden, das sich in einem Bereich befindet, in dem Location-Based Routing Einschränkungen nicht erforderlich sind. Verwenden Sie den lync Server Windows PowerShell-Befehl, die CsVoiceRoutingPolicy-oder lync Server-Systemsteuerung, um VoIP-Routing Richtlinien zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d1e76-115">When assigning PSTN usages to a voice routing policy, make sure to only use PSTN usages that are associated to voice routes that use a PSTN gateway local to the site or a PSTN gateway that is located in a region where Location-Based Routing restrictions are not needed.Use the Lync Server Windows PowerShell command, New-CsVoiceRoutingPolicy, or Lync Server Control Panel to create voice routing policies.</span></span>

    New-CsVoiceRoutingPolicy -Identity <voice routing policy ID> -Name <voice routing policy name> -PstnUsages <usages>

<span data-ttu-id="d1e76-116">Weitere Informationen finden Sie unter [New-CsVoiceRoutingPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoiceRoutingPolicy).</span><span class="sxs-lookup"><span data-stu-id="d1e76-116">For more information, see [New-CsVoiceRoutingPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoiceRoutingPolicy).</span></span>

<span data-ttu-id="d1e76-117">In diesem Beispiel veranschaulichen die folgenden Tabellen-und Windows PowerShell-Befehle zwei VoIP-Routing Richtlinien und die zugehörigen PSTN-Nutzungen, die in diesem Szenario definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d1e76-117">For this example, the following table and Windows PowerShell commands illustrate two voice routing policies and their associated PSTN usages defined in this scenario.</span></span> <span data-ttu-id="d1e76-118">Nur Einstellungen, die für Location-Based Routing spezifisch sind, werden in der Tabelle zu Illustrationszwecken berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="d1e76-118">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    New-CsVoiceRoutingPolicy -Identity "DelhiVoiceRoutingPolicy" -Name "Delhi voice routing policy" -PstnUsages @{add="Delhi usage", "PBX Del usage", "PBX Hyd usage"}
    New-CsVoiceRoutingPolicy -Identity "HyderabadVoiceRoutingPolicy" -Name " Hyderabad voice routing policy" -PstnUsages @{add="Hyderabad usage", "PBX Del usage", "PBX Hyd usage"}


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d1e76-119">VoIP-Routing Richtlinie 1</span><span class="sxs-lookup"><span data-stu-id="d1e76-119">Voice routing policy 1</span></span></th>
<th><span data-ttu-id="d1e76-120">VoIP-Routing Richtlinie 2</span><span class="sxs-lookup"><span data-stu-id="d1e76-120">Voice routing policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1e76-121">VoIP-Richtlinienkennung</span><span class="sxs-lookup"><span data-stu-id="d1e76-121">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="d1e76-122">Delhi-VoIP-Routing Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d1e76-122">Delhi voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="d1e76-123">Hyderabad-VoIP-Routing Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d1e76-123">Hyderabad voice routing policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1e76-124">PSTN-Nutzungen</span><span class="sxs-lookup"><span data-stu-id="d1e76-124">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="d1e76-125">Nutzung von Delhi, Nutzung von Telefonanlagen, Telefonanlagen Hyd</span><span class="sxs-lookup"><span data-stu-id="d1e76-125">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="d1e76-126">Hyderabad-Nutzung, Nutzung von Telefonanlagen Hyd, Telefonanlagen Nutzung</span><span class="sxs-lookup"><span data-stu-id="d1e76-126">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
</tbody>
</table>

  

<span data-ttu-id="d1e76-127">Konfigurieren Sie als nächstes Location-Based Routing für die entsprechenden Netzwerk Websites, und ordnen Sie Ihre VoIP-Routing Richtlinien zu.</span><span class="sxs-lookup"><span data-stu-id="d1e76-127">Next, configure Location-Based Routing for the applicable network sites and associate your voice routing policies to them.</span></span> <span data-ttu-id="d1e76-128">Verwenden Sie den Windows PowerShell-Befehl von lync Server, New-CsNetworkSite, um Location-Based Routing zu aktivieren und Ihren Netzwerk Websites VoIP-Routing Richtlinien zuzuordnen, die Routing Einschränkungen erzwingen müssen.</span><span class="sxs-lookup"><span data-stu-id="d1e76-128">Use the Lync Server Windows PowerShell command, New-CsNetworkSite, to enable Location-Based Routing and associate voice routing policies to your network sites that must enforce routing restrictions.</span></span>

    Set-CsNetworkSite -Identity <site ID> -EnableLocationBasedRouting <$true|$false> -VoiceRoutingPolicy <voice routing policy ID>

<span data-ttu-id="d1e76-129">In diesem Beispiel wird in der folgenden Tabelle Location-Based Routing für zwei verschiedene Netzwerkstandorte, Delhi und Hyderabad, veranschaulicht, die in diesem Szenario mithilfe der lync Server Windows PowerShell definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d1e76-129">In this example, the following table illustrates Location-Based Routing for two different network sites, Delhi and Hyderabad, defined in this scenario using the Lync Server Windows PowerShell.</span></span> <span data-ttu-id="d1e76-130">Nur Einstellungen, die für Location-Based Routing spezifisch sind, werden in der Tabelle zu Illustrationszwecken berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="d1e76-130">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    Set-CsNetworkSite -Identity "Delhi" -EnableLocationBasedRouting $true -VoiceRoutingPolicy "DelhiVoiceRoutingPolicy"
    Set-CsNetworkSite -Identity "Hyderabad" -EnableLocationBasedRouting $true -VoiceRoutingPolicy "HyderabadVoiceRoutingPolicy"


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d1e76-131">Website 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="d1e76-131">Site 1 (Delhi)</span></span></th>
<th><span data-ttu-id="d1e76-132">Website 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="d1e76-132">Site 2 (Hyderabad)</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1e76-133">Websitename</span><span class="sxs-lookup"><span data-stu-id="d1e76-133">Site Name</span></span></p></td>
<td><p><span data-ttu-id="d1e76-134">Website 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="d1e76-134">Site 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="d1e76-135">Website 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="d1e76-135">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1e76-136">EnableLocationBasedRouting</span><span class="sxs-lookup"><span data-stu-id="d1e76-136">EnableLocationBasedRouting</span></span></p></td>
<td><p><span data-ttu-id="d1e76-137">Wahr</span><span class="sxs-lookup"><span data-stu-id="d1e76-137">True</span></span></p></td>
<td><p><span data-ttu-id="d1e76-138">Wahr</span><span class="sxs-lookup"><span data-stu-id="d1e76-138">True</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1e76-139">VoIP-Routing Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d1e76-139">Voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="d1e76-140">Delhi-VoIP-Routing Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d1e76-140">Delhi voice routing policy</span></span></p></td>
<td><p><span data-ttu-id="d1e76-141">Hyderabad-VoIP-Routing Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d1e76-141">Hyderabad voice routing policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1e76-142">Subnetze</span><span class="sxs-lookup"><span data-stu-id="d1e76-142">Subnets</span></span></p></td>
<td><p><span data-ttu-id="d1e76-143">Subnetz 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="d1e76-143">Subnet 1 (Delhi)</span></span></p></td>
<td><p><span data-ttu-id="d1e76-144">Subnetz 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="d1e76-144">Subnet 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-to-trunks"></a><span data-ttu-id="d1e76-145">Aktivieren von Location-Based Routing zu Trunks</span><span class="sxs-lookup"><span data-stu-id="d1e76-145">Enable Location-Based Routing to Trunks</span></span>

<span data-ttu-id="d1e76-146">Bevor eine trunk-Konfiguration für Location-Based Routing aktiviert werden kann, müssen Sie für jeden trunk oder jede Netzwerk Website eine trunk-Konfiguration erstellen.</span><span class="sxs-lookup"><span data-stu-id="d1e76-146">Before a trunk configuration can be enabled for Location-Based Routing, you need to create a trunk configuration for each trunk or each network site.</span></span> <span data-ttu-id="d1e76-147">Verwenden Sie den Windows PowerShell-Befehl von lync Server, New-CsTrunkConfiguration, um eine trunk-Konfiguration zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="d1e76-147">Use the Lync Server Windows PowerShell command, New-CsTrunkConfiguration, to create a trunk configuration.</span></span> <span data-ttu-id="d1e76-148">Wenn mehrere Trunks einem bestimmten System (also Gateway oder PBX) zugeordnet sind, muss jede trunk-Konfiguration so geändert werden, dass Location-Based Routing Einschränkungen aktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="d1e76-148">If multiple trunks are associated with a given system (i.e. Gateway or PBX), each trunk configuration must be modified to enable Location-Based Routing restrictions.</span></span>

    New-CsTrunkConfiguration -Identity < trunk configuration ID>

<span data-ttu-id="d1e76-149">Weitere Informationen finden Sie unter [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span><span class="sxs-lookup"><span data-stu-id="d1e76-149">For more information, see [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span></span>

<span data-ttu-id="d1e76-150">In diesem Beispiel veranschaulichen die folgenden Windows PowerShell-Befehle das Erstellen einer trunk-Konfiguration für jeden trunk in der Bereitstellung, die in diesem Szenario definiert ist.</span><span class="sxs-lookup"><span data-stu-id="d1e76-150">For this example, the following Windows PowerShell commands illustrate creating one trunk configuration for each trunk in the deployment defined in this scenario.</span></span>

    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 1 DEL-GW>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 2 HYD-GW>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 3 DEL-PBX>"
    New-CsTrunkConfiguration -Identity Service:PstnGateway:"<Trunk 4 HYD-PBX>"

<span data-ttu-id="d1e76-151">Nachdem eine trunk-Konfiguration pro trunk konfiguriert wurde, können Sie den lync Server Windows PowerShell-Befehl, CsTrunkConfiguration, verwenden, um Location-Based Routing an Ihre Trunks zu aktivieren, die Routing Einschränkungen erzwingen müssen.</span><span class="sxs-lookup"><span data-stu-id="d1e76-151">Once a trunk configuration is configured per trunk, you can use the Lync Server Windows PowerShell command, Set-CsTrunkConfiguration, to enable Location-Based Routing to your trunks that must enforce routing restrictions.</span></span> <span data-ttu-id="d1e76-152">Aktivieren Sie Location-Based Routing an Trunks, die Anrufe an PSTN-Gateways weiterleiten, die Anrufe an das PSTN weiterleiten, und ordnen Sie die Netzwerk Website zu, auf der sich das Gateway befindet.</span><span class="sxs-lookup"><span data-stu-id="d1e76-152">Enable Location-Based Routing to trunks that route calls to PSTN gateways that route calls to the PSTN, and associate the network site where the gateway is located.</span></span>

    Set-CsTrunkConfiguration -Identity <trunk configuration ID> -EnableLocationRestriction $true -NetworkSiteID <site ID>

<span data-ttu-id="d1e76-153">Weitere Informationen finden Sie unter [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span><span class="sxs-lookup"><span data-stu-id="d1e76-153">For more information, see [New-CsTrunkConfiguration](https://docs.microsoft.com/powershell/module/skype/New-CsTrunkConfiguration).</span></span>

<span data-ttu-id="d1e76-154">In diesem Beispiel ist Location-Based Routing für jeden trunk aktiviert, der PSTN-Gateways in Delhi und Hyderabad zugeordnet ist:</span><span class="sxs-lookup"><span data-stu-id="d1e76-154">In this example, Location-Based Routing is enabled for each trunk that is associated to PSTN gateways in Delhi and Hyderabad:</span></span>

    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 1 DEL-GW -EnableLocationRestriction $true -NetworkSiteID "Delhi"
    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 2 HYD-GW -EnableLocationRestriction $true -NetworkSiteID "Hyderabad"

  

<span data-ttu-id="d1e76-155">Aktivieren Sie Location-Based Routing für Trunks, die keine Anrufe an das PSTN weiterleiten. Sie müssen den trunk jedoch weiterhin der Netzwerk Website zuordnen, auf der sich das System befindet, da Location-Based Routing Einschränkungen für PSTN-Anrufe, die über diesen Trunk verbunden sind, erzwungen werden müssen.</span><span class="sxs-lookup"><span data-stu-id="d1e76-155">Do not enable Location-Based Routing for trunks that do not route calls to the PSTN; however, you must still associate the trunk to the network site where the system is located as Location-Based Routing restrictions need to be enforced for PSTN calls reaching endpoints connected via this trunk.</span></span> <span data-ttu-id="d1e76-156">In diesem Beispiel ist Location-Based Routing für jeden trunk, der PBX-Systemen in Delhi und Hyderabad zugeordnet ist, nicht aktiviert:</span><span class="sxs-lookup"><span data-stu-id="d1e76-156">For this example, Location-Based Routing is not enabled for each trunk that is associated to PBX systems in Delhi and Hyderabad:</span></span>

    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 3 DEL-PBX -EnableLocationRestriction $false -NetworkSiteID "Delhi"
    Set-CsTrunkConfiguration -Identity Service:PstnGateway:Trunk 4 HYD-PBX -EnableLocationRestriction $false -NetworkSiteID "Hyderabad"

  
<span data-ttu-id="d1e76-157">Endpunkte, die mit Systemen verbunden sind, die keine Anrufe an das PSTN (also eine Telefonanlage) weiterleiten, weisen ähnliche Einschränkungen wie lync-Endpunkte von Benutzern auf, die für Location-Based Routing aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="d1e76-157">Endpoints that are connected to systems that do not route calls to the PSTN (i.e. a PBX) will have similar restrictions as Lync endpoints of users enabled for Location-Based Routing.</span></span> <span data-ttu-id="d1e76-158">Dies bedeutet, dass diese Benutzer unabhängig vom Standort des Benutzers Anrufe an und von lync-Benutzern tätigen und empfangen können.</span><span class="sxs-lookup"><span data-stu-id="d1e76-158">This means that these users will be able to place and receive calls to and from Lync user regardless of the user’s location.</span></span> <span data-ttu-id="d1e76-159">Sie können auch Anrufe von und zu anderen Systemen tätigen, die keine Anrufe an das PSTN-Netzwerk (also einen mit einer anderen Telefonanlage verbundenen Endpunkt) weiterleiten, und zwar unabhängig von der Netzwerk Website, der das System zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="d1e76-159">They will also be able to place an receive calls to and from other systems that do not route calls to the PSTN network (i.e. an endpoint connected to a different PBX) regardless of the network site to which the system is associated.</span></span> <span data-ttu-id="d1e76-160">Alle eingehenden Anrufe, ausgehenden Anrufe, Anruf Übertragungen und Anrufweiterleitung, die PSTN-Endpunkte betreffen, unterliegen Location-Based Routing-Erzwingung.</span><span class="sxs-lookup"><span data-stu-id="d1e76-160">All inbound calls, outbound calls, call transfers and call forwarding involving PSTN endpoints will be subject to Location-Based Routing enforcements.</span></span> <span data-ttu-id="d1e76-161">Bei solchen anrufen müssen nur PSTN-Gateways verwendet werden, die für solche Systeme als lokal definiert sind.</span><span class="sxs-lookup"><span data-stu-id="d1e76-161">Such calls must use only PSTN gateways that are defined as local to such systems.</span></span>

<span data-ttu-id="d1e76-162">In der folgenden Tabelle wird die trunk-Konfiguration von vier Trunks auf zwei verschiedenen Netzwerkstandorten veranschaulicht: zwei mit PSTN-Gateways verbunden und zwei mit PBX-Systemen verbunden.</span><span class="sxs-lookup"><span data-stu-id="d1e76-162">The following table illustrates the trunk configuration of four trunks in two different network sites: two connected to PSTN gateways and two connected to PBX systems.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="d1e76-163">Name</span><span class="sxs-lookup"><span data-stu-id="d1e76-163">Name</span></span></th>
<th><span data-ttu-id="d1e76-164">EnableLocationRestriction</span><span class="sxs-lookup"><span data-stu-id="d1e76-164">EnableLocationRestriction</span></span></th>
<th><span data-ttu-id="d1e76-165">NetworkSiteID</span><span class="sxs-lookup"><span data-stu-id="d1e76-165">NetworkSiteID</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1e76-166">PstnGateway: trunk 1 del-GW</span><span class="sxs-lookup"><span data-stu-id="d1e76-166">PstnGateway:Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="d1e76-167">Wahr</span><span class="sxs-lookup"><span data-stu-id="d1e76-167">True</span></span></p></td>
<td><p><span data-ttu-id="d1e76-168">Website 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="d1e76-168">Site 1 (Delhi)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1e76-169">PstnGateway: trunk 2 Hyd-GW</span><span class="sxs-lookup"><span data-stu-id="d1e76-169">PstnGateway:Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="d1e76-170">Wahr</span><span class="sxs-lookup"><span data-stu-id="d1e76-170">True</span></span></p></td>
<td><p><span data-ttu-id="d1e76-171">Website 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="d1e76-171">Site 2 (Hyderabad)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1e76-172">PstnGateway: trunk 3 del-PBX</span><span class="sxs-lookup"><span data-stu-id="d1e76-172">PstnGateway:Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="d1e76-173">Falsch</span><span class="sxs-lookup"><span data-stu-id="d1e76-173">False</span></span></p></td>
<td><p><span data-ttu-id="d1e76-174">Website 1 (Delhi)</span><span class="sxs-lookup"><span data-stu-id="d1e76-174">Site 1 (Delhi)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1e76-175">PstnGateway: trunk 4 Hyd-PBX</span><span class="sxs-lookup"><span data-stu-id="d1e76-175">PstnGateway:Trunk 4 HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="d1e76-176">Falsch</span><span class="sxs-lookup"><span data-stu-id="d1e76-176">False</span></span></p></td>
<td><p><span data-ttu-id="d1e76-177">Website 2 (Hyderabad)</span><span class="sxs-lookup"><span data-stu-id="d1e76-177">Site 2 (Hyderabad)</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-to-voice-policies"></a><span data-ttu-id="d1e76-178">Aktivieren von Location-Based Routing zu VoIP-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d1e76-178">Enable Location-Based Routing to Voice Policies</span></span>

<span data-ttu-id="d1e76-179">Wenn Sie Location-Based Routing für bestimmte Benutzer erzwingen möchten, konfigurieren Sie die VoIP-Richtlinie dieser Benutzer, um die PSTN-Maut Umgehung zu verhindern.</span><span class="sxs-lookup"><span data-stu-id="d1e76-179">To enforce Location-Based Routing to specific users, configure those users’ voice policy to prevent PSTN toll bypass.</span></span> <span data-ttu-id="d1e76-180">Verwenden Sie den Windows PowerShell-Befehl von lync Server, New-CsVoicePolicy, zum Erstellen einer neuen VoIP-Richtlinie oder eines CsVoicePolicy, wenn Sie eine vorhandene Richtlinie verwenden, um Location-Based Routing zu aktivieren, indem Sie die PSTN-Maut Umgehung verhindern.</span><span class="sxs-lookup"><span data-stu-id="d1e76-180">Use the Lync Server Windows PowerShell command, New-CsVoicePolicy, to create a new voice policy or Set-CsVoicePolicy, if using an existing policy, to enable Location-Based Routing by preventing PSTN toll bypass.</span></span>

    Set-CsVoicePolicy -Identity <voice policy ID> -PreventPSTNTollBypass <$true|$false>

<span data-ttu-id="d1e76-181">Weitere Informationen finden Sie unter [New-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoicePolicy).</span><span class="sxs-lookup"><span data-stu-id="d1e76-181">For more information, see [New-CsVoicePolicy](https://docs.microsoft.com/powershell/module/skype/New-CsVoicePolicy).</span></span>

<span data-ttu-id="d1e76-182">In diesem Beispiel veranschaulichen die folgenden Tabellen-und Windows PowerShell-Befehle die Verhinderung von PSTN-Maut Umgehung für die in diesem Szenario definierten VoIP-Richtlinien in Delhi und Hyderabad.</span><span class="sxs-lookup"><span data-stu-id="d1e76-182">For this example, the following table and Windows PowerShell commands illustrate enabling the prevention of PSTN toll bypass to the Delhi and Hyderabad voice policies defined in this scenario.</span></span> <span data-ttu-id="d1e76-183">Nur Einstellungen, die für Location-Based Routing spezifisch sind, werden in der Tabelle zu Illustrationszwecken berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="d1e76-183">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

    Set-CsVoicePolicy -Identity "Delhi voice policy" -PreventPSTNTollBypass $true
    Set-CsVoicePolicy -Identity "Hyderabad voice policy" -PreventPSTNTollBypass $true


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="d1e76-184">VoIP-Richtlinie 1</span><span class="sxs-lookup"><span data-stu-id="d1e76-184">Voice policy 1</span></span></th>
<th><span data-ttu-id="d1e76-185">VoIP-Richtlinie 2</span><span class="sxs-lookup"><span data-stu-id="d1e76-185">Voice policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="d1e76-186">VoIP-Richtlinienkennung</span><span class="sxs-lookup"><span data-stu-id="d1e76-186">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="d1e76-187">VoIP-Richtlinie für Delhi</span><span class="sxs-lookup"><span data-stu-id="d1e76-187">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="d1e76-188">Hyderabad-VoIP-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="d1e76-188">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="d1e76-189">PSTN-Nutzungen</span><span class="sxs-lookup"><span data-stu-id="d1e76-189">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="d1e76-190">Nutzung von Delhi, Nutzung von Telefonanlagen, Telefonanlagen Hyd</span><span class="sxs-lookup"><span data-stu-id="d1e76-190">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="d1e76-191">Hyderabad-Nutzung, Nutzung von Telefonanlagen Hyd, Telefonanlagen Nutzung</span><span class="sxs-lookup"><span data-stu-id="d1e76-191">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="d1e76-192">PreventPSTNTollBypass</span><span class="sxs-lookup"><span data-stu-id="d1e76-192">PreventPSTNTollBypass</span></span></p></td>
<td><p><span data-ttu-id="d1e76-193">Wahr</span><span class="sxs-lookup"><span data-stu-id="d1e76-193">True</span></span></p></td>
<td><p><span data-ttu-id="d1e76-194">Wahr</span><span class="sxs-lookup"><span data-stu-id="d1e76-194">True</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-location-based-routing-in-the-routing-configuration"></a><span data-ttu-id="d1e76-195">Aktivieren des Location-Based-Routings in der Routingkonfiguration</span><span class="sxs-lookup"><span data-stu-id="d1e76-195">Enable Location-Based Routing in the routing configuration</span></span>

<span data-ttu-id="d1e76-196">Schließlich können Sie Location-Based Routing an Ihre Routingkonfiguration Global aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d1e76-196">Finally, globally enable Location-Based Routing to your routing configuration.</span></span> <span data-ttu-id="d1e76-197">Verwenden Sie den Windows PowerShell-Befehl von lync Server, New-CsRoutingConfiguration, um Location-Based Routing zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d1e76-197">Use the Lync Server Windows PowerShell command, New-CsRoutingConfiguration, to enable Location-Based Routing.</span></span>

    Set-CsRoutingConfiguration -EnableLocationBasedRouting $true

<span data-ttu-id="d1e76-198">Weitere Informationen finden Sie unter [Satz-CsRoutingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsRoutingConfiguration).</span><span class="sxs-lookup"><span data-stu-id="d1e76-198">For more information, see [Set-CsRoutingConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsRoutingConfiguration).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d1e76-199">während Location-Based-Routing über eine globale Konfiguration aktiviert werden muss, wird die anzuwendende Regel nur für die Websites, Benutzer und Trunks erzwungen, für die Sie konfiguriert wurde, wie in dieser Dokumentation angegeben.</span><span class="sxs-lookup"><span data-stu-id="d1e76-199">while Location-Based Routing must be enabled via a global configuration, the set of rules to be applied will only be enforced for the sites, users and trunks for which it has been configured as specified in this documentation.</span></span>



</div>

<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d1e76-200">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1e76-200">See Also</span></span>


[<span data-ttu-id="d1e76-201">Konfigurieren von standortbasiertem Routing in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d1e76-201">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="d1e76-202"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d1e76-202"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

