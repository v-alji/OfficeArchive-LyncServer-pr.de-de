---
title: 'Lync Server 2013: Konfigurieren von Enterprise-VoIP'
description: 'Lync Server 2013: Konfigurieren von Enterprise-VoIP'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Enterprise Voice
ms:assetid: 7df179fa-d3a2-4b23-a433-b750aedf980b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ994041(v=OCS.15)
ms:contentKeyID: 51803952
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 49a231b92bf7b04aa3466927a79258f0cbad4e3f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433122"
---
# <a name="configuring-enterprise-voice-in-lync-server-2013"></a><span data-ttu-id="e9ca8-103">Konfigurieren von Enterprise-VoIP in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e9ca8-103">Configuring Enterprise Voice in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e9ca8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e9ca8-104">

<span> </span></span></span>

<span data-ttu-id="e9ca8-105">_**Letztes Änderungsdatum des Themas:** 2013-03-12_</span><span class="sxs-lookup"><span data-stu-id="e9ca8-105">_**Topic Last Modified:** 2013-03-12_</span></span>

<span data-ttu-id="e9ca8-106">Zur Bereitstellung von Enterprise-VoIP müssen Sie Folgendes konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="e9ca8-106">To deploy Enterprise Voice, you’ll need to configure the following:</span></span>

  - <span data-ttu-id="e9ca8-107">Erstellen eines Stamms</span><span class="sxs-lookup"><span data-stu-id="e9ca8-107">Create a Trunk</span></span>

  - <span data-ttu-id="e9ca8-108">Definieren einer VoIP-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="e9ca8-108">Define a Voice Policy</span></span>

  - <span data-ttu-id="e9ca8-109">Definieren einer VoIP-Route</span><span class="sxs-lookup"><span data-stu-id="e9ca8-109">Define a Voice Route</span></span>

  - <span data-ttu-id="e9ca8-110">Enable Users for Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="e9ca8-110">Enable Users for Enterprise Voice</span></span>

<div>

## <a name="create-a-trunk"></a><span data-ttu-id="e9ca8-111">Erstellen eines Stamms</span><span class="sxs-lookup"><span data-stu-id="e9ca8-111">Create a Trunk</span></span>

<span data-ttu-id="e9ca8-112">Sie müssen Trunks in Ihrer Enterprise-VoIP-Bereitstellung definieren.</span><span class="sxs-lookup"><span data-stu-id="e9ca8-112">You must define trunks in your Enterprise Voice deployment.</span></span> <span data-ttu-id="e9ca8-113">Für Location-Based Routing müssen Sie eine trunk-Konfiguration pro trunk erstellen.</span><span class="sxs-lookup"><span data-stu-id="e9ca8-113">For Location-Based Routing, you must create a trunk configuration per trunk.</span></span> <span data-ttu-id="e9ca8-114">Verwenden Sie den lync Server Topology Builder, um Ihre Trunks zu definieren, und verwenden Sie den lync Server Windows PowerShell-Befehl, New-CsTrunkConfiguration oder die lync Server-Systemsteuerung, um die entsprechenden Trunk-Konfigurationen zu definieren.</span><span class="sxs-lookup"><span data-stu-id="e9ca8-114">Use the Lync Server Topology Builder to define your trunks, and use the Lync Server Windows PowerShell command, New-CsTrunkConfiguration, or the Lync Server Control Panel to define the corresponding trunk configurations.</span></span> <span data-ttu-id="e9ca8-115">Weitere Informationen dazu, wie Sie Location-Based Routing auf Trunk-Konfigurationen aktivieren können, finden Sie im Abschnitt Aktivieren von Location-Based Routing zu Trunks, in dem Thema Aktivieren von [Location-Based Routing in lync Server 2013](lync-server-2013-enabling-location-based-routing.md).</span><span class="sxs-lookup"><span data-stu-id="e9ca8-115">More information on how to enable Location-Based Routing on trunk configurations can be found in the section, Enable Location-Based Routing to Trunks, in the topic, [Enabling Location-Based Routing in Lync Server 2013](lync-server-2013-enabling-location-based-routing.md).</span></span> <span data-ttu-id="e9ca8-116">In diesem Beispiel werden in der folgenden Tabelle die in diesem Szenario verwendeten Trunks veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e9ca8-116">For this example, the following table illustrates the trunks used in this scenario.</span></span>

<span data-ttu-id="e9ca8-117">Weitere Informationen finden Sie unter [Definieren zusätzlicher Trunks im Topologie-Generator in lync Server 2013](lync-server-2013-define-additional-trunks-in-topology-builder.md).</span><span class="sxs-lookup"><span data-stu-id="e9ca8-117">For more information, see [Define additional trunks in Topology Builder in Lync Server 2013](lync-server-2013-define-additional-trunks-in-topology-builder.md).</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="e9ca8-118">Trunk-Name</span><span class="sxs-lookup"><span data-stu-id="e9ca8-118">Trunk name</span></span></th>
<th><span data-ttu-id="e9ca8-119">Systemtyp</span><span class="sxs-lookup"><span data-stu-id="e9ca8-119">System type</span></span></th>
<th><span data-ttu-id="e9ca8-120">Name</span><span class="sxs-lookup"><span data-stu-id="e9ca8-120">Name</span></span></th>
<th><span data-ttu-id="e9ca8-121">Ort</span><span class="sxs-lookup"><span data-stu-id="e9ca8-121">Location</span></span></th>
<th><span data-ttu-id="e9ca8-122">Vermittlungsserver</span><span class="sxs-lookup"><span data-stu-id="e9ca8-122">Mediation Server</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9ca8-123">Trunk 1 del-GW</span><span class="sxs-lookup"><span data-stu-id="e9ca8-123">Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-124">PSTN-Gateway</span><span class="sxs-lookup"><span data-stu-id="e9ca8-124">PSTN gateway</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-125">DEL-GW</span><span class="sxs-lookup"><span data-stu-id="e9ca8-125">DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-126">Delhi</span><span class="sxs-lookup"><span data-stu-id="e9ca8-126">Delhi</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-127">MS1</span><span class="sxs-lookup"><span data-stu-id="e9ca8-127">MS1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9ca8-128">Trunk 2 Hyd-GW</span><span class="sxs-lookup"><span data-stu-id="e9ca8-128">Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-129">PSTN-Gateway</span><span class="sxs-lookup"><span data-stu-id="e9ca8-129">PSTN gateway</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-130">Hyd-GW</span><span class="sxs-lookup"><span data-stu-id="e9ca8-130">HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-131">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="e9ca8-131">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-132">MS1</span><span class="sxs-lookup"><span data-stu-id="e9ca8-132">MS1</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9ca8-133">Trunk 3 del-PBX</span><span class="sxs-lookup"><span data-stu-id="e9ca8-133">Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-134">PBX</span><span class="sxs-lookup"><span data-stu-id="e9ca8-134">PBX</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-135">DEL-PBX</span><span class="sxs-lookup"><span data-stu-id="e9ca8-135">DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-136">Delhi</span><span class="sxs-lookup"><span data-stu-id="e9ca8-136">Delhi</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-137">MS1</span><span class="sxs-lookup"><span data-stu-id="e9ca8-137">MS1</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9ca8-138">Trunk 4 Hyd-PBX</span><span class="sxs-lookup"><span data-stu-id="e9ca8-138">Trunk 4 HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-139">PBX</span><span class="sxs-lookup"><span data-stu-id="e9ca8-139">PBX</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-140">Hyd-PBX</span><span class="sxs-lookup"><span data-stu-id="e9ca8-140">HYD-PBX</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-141">Hyderabad</span><span class="sxs-lookup"><span data-stu-id="e9ca8-141">Hyderabad</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-142">MS1</span><span class="sxs-lookup"><span data-stu-id="e9ca8-142">MS1</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="defines-voice-policies"></a><span data-ttu-id="e9ca8-143">Definiert VoIP-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="e9ca8-143">Defines Voice Policies</span></span>

<span data-ttu-id="e9ca8-144">Sie müssen VoIP-Richtlinien für Ihre Enterprise-VoIP-Bereitstellung definieren.</span><span class="sxs-lookup"><span data-stu-id="e9ca8-144">You must define voice policies for your Enterprise Voice deployment.</span></span> <span data-ttu-id="e9ca8-145">Definieren Sie eine VoIP-Richtlinie, um Location-Based Routing Einschränkungen für eine Teilmenge von Benutzern zu erzwingen, wenn nur eine Teilmenge von Ihnen für die Verwendung von Location-Based Routing erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="e9ca8-145">Define a Voice Policy to enforce Location-Based Routing restrictions to a subset of users if only a subset of them is required to use Location-Based Routing.</span></span> <span data-ttu-id="e9ca8-146">In diesem Beispiel werden in der folgenden Tabelle die in diesem Szenario verwendeten VoIP-Richtlinien veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e9ca8-146">For this example, the following table illustrates the voice policies used in this scenario.</span></span> <span data-ttu-id="e9ca8-147">Nur Einstellungen, die für Location-Based Routing spezifisch sind, werden in der Tabelle zu Illustrationszwecken berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="e9ca8-147">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="e9ca8-148">Weitere Informationen finden Sie unter [Konfigurieren von VoIP-Richtlinien und PSTN-Verwendungsdatensätzen, um die Anruffunktionen und-Berechtigungen in lync Server 2013 zu autorisieren](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md).</span><span class="sxs-lookup"><span data-stu-id="e9ca8-148">For more information, see [Configuring voice policies and PSTN usage records to authorize calling features and privileges in Lync Server 2013](lync-server-2013-configuring-voice-policies-and-pstn-usage-records-to-authorize-calling-features-and-privileges.md).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="e9ca8-149">VoIP-Richtlinie 1</span><span class="sxs-lookup"><span data-stu-id="e9ca8-149">Voice policy 1</span></span></th>
<th><span data-ttu-id="e9ca8-150">VoIP-Richtlinie 2</span><span class="sxs-lookup"><span data-stu-id="e9ca8-150">Voice policy 2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9ca8-151">VoIP-Richtlinienkennung</span><span class="sxs-lookup"><span data-stu-id="e9ca8-151">Voice policy ID</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-152">VoIP-Richtlinie für Delhi</span><span class="sxs-lookup"><span data-stu-id="e9ca8-152">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-153">Hyderabad-VoIP-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="e9ca8-153">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9ca8-154">PSTN-Nutzungen</span><span class="sxs-lookup"><span data-stu-id="e9ca8-154">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-155">Nutzung von Delhi, Nutzung von Telefonanlagen, Telefonanlagen Hyd</span><span class="sxs-lookup"><span data-stu-id="e9ca8-155">Delhi usage, PBX Del usage, PBX Hyd usage</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-156">Hyderabad-Nutzung, Nutzung von Telefonanlagen Hyd, Telefonanlagen Nutzung</span><span class="sxs-lookup"><span data-stu-id="e9ca8-156">Hyderabad usage, PBX Hyd usage, PBX Del usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9ca8-157">PreventPSTNTollBypass</span><span class="sxs-lookup"><span data-stu-id="e9ca8-157">PreventPSTNTollBypass</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-158">Falsch</span><span class="sxs-lookup"><span data-stu-id="e9ca8-158">False</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-159">Falsch</span><span class="sxs-lookup"><span data-stu-id="e9ca8-159">False</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="define-voice-routes"></a><span data-ttu-id="e9ca8-160">Definieren von VoIP-Routen</span><span class="sxs-lookup"><span data-stu-id="e9ca8-160">Define Voice Routes</span></span>

<span data-ttu-id="e9ca8-161">Sie müssen VoIP-Routen für Ihre Enterprise-VoIP-Bereitstellung definieren.</span><span class="sxs-lookup"><span data-stu-id="e9ca8-161">You must define voice routes for your Enterprise Voice deployment.</span></span> <span data-ttu-id="e9ca8-162">In diesem Beispiel werden in der folgenden Tabelle die in diesem Szenario verwendeten VoIP-Routen veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e9ca8-162">For this example, the following table illustrates the voice routes used in this scenario.</span></span> <span data-ttu-id="e9ca8-163">Nur Einstellungen, die für Location-Based Routing spezifisch sind, werden in der Tabelle zu Illustrationszwecken berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="e9ca8-163">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="e9ca8-164">Weitere Informationen finden Sie unter [Konfigurieren von VoIP-Routen für ausgehende Anrufe in lync Server 2013](lync-server-2013-configuring-voice-routes-for-outbound-calls.md).</span><span class="sxs-lookup"><span data-stu-id="e9ca8-164">For more information, see [Configuring voice routes for outbound calls in Lync Server 2013](lync-server-2013-configuring-voice-routes-for-outbound-calls.md).</span></span>


<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="e9ca8-165">VoIP-Route 1</span><span class="sxs-lookup"><span data-stu-id="e9ca8-165">Voice route 1</span></span></th>
<th><span data-ttu-id="e9ca8-166">VoIP-Route 2</span><span class="sxs-lookup"><span data-stu-id="e9ca8-166">Voice route 2</span></span></th>
<th><span data-ttu-id="e9ca8-167">VoIP-Route 3</span><span class="sxs-lookup"><span data-stu-id="e9ca8-167">Voice route 3</span></span></th>
<th><span data-ttu-id="e9ca8-168">VoIP-Route 4</span><span class="sxs-lookup"><span data-stu-id="e9ca8-168">Voice route 4</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9ca8-169">Name</span><span class="sxs-lookup"><span data-stu-id="e9ca8-169">Name</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-170">Delhi-Route</span><span class="sxs-lookup"><span data-stu-id="e9ca8-170">Delhi route</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-171">Hyderabad-Route</span><span class="sxs-lookup"><span data-stu-id="e9ca8-171">Hyderabad route</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-172">PBX del-Route</span><span class="sxs-lookup"><span data-stu-id="e9ca8-172">PBX Del route</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-173">PBX-Hyd-Route</span><span class="sxs-lookup"><span data-stu-id="e9ca8-173">PBX Hyd route</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9ca8-174">PSTN-Nutzungen</span><span class="sxs-lookup"><span data-stu-id="e9ca8-174">PSTN usages</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-175">Delhi-Nutzung</span><span class="sxs-lookup"><span data-stu-id="e9ca8-175">Delhi usage</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-176">Hyderabad-Nutzung</span><span class="sxs-lookup"><span data-stu-id="e9ca8-176">Hyderabad usage</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-177">Telefonanlagen Nutzung</span><span class="sxs-lookup"><span data-stu-id="e9ca8-177">PBX Del usage</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-178">Verwendung von PBX-Hyd</span><span class="sxs-lookup"><span data-stu-id="e9ca8-178">PBX Hyd usage</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="e9ca8-179">Stamm</span><span class="sxs-lookup"><span data-stu-id="e9ca8-179">Trunk</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-180">Trunk 1 del-GW</span><span class="sxs-lookup"><span data-stu-id="e9ca8-180">Trunk 1 DEL-GW</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-181">Trunk 2 Hyd-GW</span><span class="sxs-lookup"><span data-stu-id="e9ca8-181">Trunk 2 HYD-GW</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-182">Trunk 3 del-PBX</span><span class="sxs-lookup"><span data-stu-id="e9ca8-182">Trunk 3 DEL-PBX</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-183">Trunk 4 Hyd-PBX</span><span class="sxs-lookup"><span data-stu-id="e9ca8-183">Trunk 4 HYD-PBX</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="enable-users-for-enterprise-voice"></a><span data-ttu-id="e9ca8-184">Enable Users for Enterprise Voice</span><span class="sxs-lookup"><span data-stu-id="e9ca8-184">Enable Users for Enterprise Voice</span></span>

<span data-ttu-id="e9ca8-185">Aktivieren Sie Benutzer für Enterprise-VoIP, und weisen Sie Ihnen eine VoIP-Richtlinie zu, die Sie zuvor definiert haben.</span><span class="sxs-lookup"><span data-stu-id="e9ca8-185">Enable users for Enterprise Voice and assign them a voice policy you’ve previously defined.</span></span> <span data-ttu-id="e9ca8-186">In diesem Beispiel wird in der folgenden Tabelle die in diesem Szenario verwendete Aufgabe veranschaulicht.</span><span class="sxs-lookup"><span data-stu-id="e9ca8-186">For this example, the following table illustrates the assignment used in this scenario.</span></span> <span data-ttu-id="e9ca8-187">Nur Einstellungen, die für Location-Based Routing spezifisch sind, werden in der Tabelle zu Illustrationszwecken berücksichtigt.</span><span class="sxs-lookup"><span data-stu-id="e9ca8-187">Only settings that are specific to Location-Based Routing are included in the table for illustration purposes.</span></span>

<span data-ttu-id="e9ca8-188">Weitere Informationen finden Sie unter [Aktivieren von Benutzern für Enterprise-VoIP in lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span><span class="sxs-lookup"><span data-stu-id="e9ca8-188">For more information, see [Enable users for Enterprise Voice in Lync Server 2013](lync-server-2013-enable-users-for-enterprise-voice.md).</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th></th>
<th><span data-ttu-id="e9ca8-189">Benutzer in Delhi</span><span class="sxs-lookup"><span data-stu-id="e9ca8-189">Users located in Delhi</span></span></th>
<th><span data-ttu-id="e9ca8-190">Benutzer, die sich in Hyderabad befinden</span><span class="sxs-lookup"><span data-stu-id="e9ca8-190">Users located in Hyderabad</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="e9ca8-191">Zugehörige VoIP-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="e9ca8-191">Associated voice policy</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-192">VoIP-Richtlinie für Delhi</span><span class="sxs-lookup"><span data-stu-id="e9ca8-192">Delhi voice policy</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-193">Hyderabad-VoIP-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="e9ca8-193">Hyderabad voice policy</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="e9ca8-194">Beispiel Benutzer</span><span class="sxs-lookup"><span data-stu-id="e9ca8-194">Sample users</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-195">Del-lync-1, del-lync-2, del-lync-3</span><span class="sxs-lookup"><span data-stu-id="e9ca8-195">DEL-LYNC-1,DEL-LYNC-2,DEL-LYNC-3</span></span></p></td>
<td><p><span data-ttu-id="e9ca8-196">Hyd-lync-1, Hyd-lync-2, Hyd-lync-3</span><span class="sxs-lookup"><span data-stu-id="e9ca8-196">HYD-LYNC-1, HYD-LYNC-2, HYD-LYNC-3</span></span></p></td>
</tr>
</tbody>
</table>


<div>


</div>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e9ca8-197">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e9ca8-197">See Also</span></span>


[<span data-ttu-id="e9ca8-198">Konfigurieren von standortbasiertem Routing in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e9ca8-198">Configuring Location-Based Routing in Lync Server 2013</span></span>](lync-server-2013-configuring-location-based-routing.md)  
  

<span data-ttu-id="e9ca8-199"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e9ca8-199"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

