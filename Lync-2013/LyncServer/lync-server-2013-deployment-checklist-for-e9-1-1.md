---
title: 'Lync Server 2013: Bereitstellungscheckliste für E9-1-1'
description: 'Lync Server 2013: Bereitstellungscheckliste für E9-1-1.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for E9-1-1
ms:assetid: cc6a656a-6043-4b9b-85c2-5708b9bb1c06
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398864(v=OCS.15)
ms:contentKeyID: 48185655
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0c93762e2acef5e065249ced17bfa0eab2f159e4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429713"
---
# <a name="deployment-checklist-for-e9-1-1-in-lync-server-2013"></a><span data-ttu-id="23179-103">Bereitstellungscheckliste für E9-1-1 in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="23179-103">Deployment checklist for E9-1-1 in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="23179-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="23179-104">

<span> </span></span></span>

<span data-ttu-id="23179-105">_**Letztes Änderungsdatum des Themas:** 2012-10-03_</span><span class="sxs-lookup"><span data-stu-id="23179-105">_**Topic Last Modified:** 2012-10-03_</span></span>

<span data-ttu-id="23179-106">Um effektiv für Enhanced 9-1-1 (E9-1-1) zu planen, müssen Sie unbedingt die folgenden Bereitstellungsanforderungen berücksichtigen:</span><span class="sxs-lookup"><span data-stu-id="23179-106">To plan effectively for Enhanced 9-1-1 (E9-1-1), be sure to include the following deployment requirements:</span></span>

  - <span data-ttu-id="23179-107">Voraussetzungen für die Bereitstellung von E9-1-1.</span><span class="sxs-lookup"><span data-stu-id="23179-107">Prerequisites for deploying E9-1-1.</span></span>

  - <span data-ttu-id="23179-108">Schritte, die für die Bereitstellung von E9-1-1 erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="23179-108">Steps that are required to deploy E9-1-1.</span></span>

<div>

## <a name="deployment-prerequisites-for-e9-1-1"></a><span data-ttu-id="23179-109">Voraussetzungen für die Bereitstellung von E9-1-1</span><span class="sxs-lookup"><span data-stu-id="23179-109">Deployment Prerequisites for E9-1-1</span></span>

<span data-ttu-id="23179-110">Bevor Sie E9-1-1 bereitstellen, müssen Sie bereits die internen lync Server-Server bereitgestellt haben, einschließlich eines zentralen Verwaltungsspeichers, eines Front-End-Pools oder eines Standard Edition-Servers, eines oder mehrerer Vermittlungsserver oder Mediation Server-Pools und lync Server-Clients.</span><span class="sxs-lookup"><span data-stu-id="23179-110">Before you deploy E9-1-1, you must already have deployed your Lync Server internal servers, including a Central Management store, a Front End pool or a Standard Edition server, one or more Mediation Servers or Mediation Server pools, and Lync Server clients.</span></span> <span data-ttu-id="23179-111">Darüber hinaus benötigen Sie für eine E9-1-1-Bereitstellung einen SIP-Trunk zu einem qualifizierten E9-1-1-Dienstanbieter oder ein ELIN-Gateway (Emergency Location Identification Number) zu Ihrem Telefonfestnetz (Public Switched Telephone Network, PSTN).</span><span class="sxs-lookup"><span data-stu-id="23179-111">In addition, an E9-1-1 deployment requires a SIP trunk to a qualified E9-1-1 service provider or an Emergency Location Identification Number (ELIN) gateway to your public switched telephone network (PSTN).</span></span> <span data-ttu-id="23179-112">Lync Server unterstützt die Verwendung von E9-1-1-Dienstanbietern nur innerhalb der Vereinigten Staaten.</span><span class="sxs-lookup"><span data-stu-id="23179-112">Lync Server supports using E9-1-1 service providers only inside the United States.</span></span>

</div>

<div>

## <a name="deployment-process"></a><span data-ttu-id="23179-113">Bereitstellungsprozess</span><span class="sxs-lookup"><span data-stu-id="23179-113">Deployment Process</span></span>

<span data-ttu-id="23179-114">Die folgende Tabelle zeigt eine Übersicht über den E9-1-1-Bereitstellungsprozess.</span><span class="sxs-lookup"><span data-stu-id="23179-114">The following table provides an overview of the E9-1-1 deployment process.</span></span> <span data-ttu-id="23179-115">Ausführliche Informationen zu Bereitstellungsschritten finden Sie unter [Konfigurieren von erweitertem 9-1-1 in lync Server 2013](lync-server-2013-configure-enhanced-9-1-1.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="23179-115">For details about deployment steps, see [Configure Enhanced 9-1-1 in Lync Server 2013](lync-server-2013-configure-enhanced-9-1-1.md) in the Deployment documentation.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="23179-116">Phase</span><span class="sxs-lookup"><span data-stu-id="23179-116">Phase</span></span></th>
<th><span data-ttu-id="23179-117">Schritte</span><span class="sxs-lookup"><span data-stu-id="23179-117">Steps</span></span></th>
<th><span data-ttu-id="23179-118">Rollen</span><span class="sxs-lookup"><span data-stu-id="23179-118">Roles</span></span></th>
<th><span data-ttu-id="23179-119">Bereitstellungsdokumentation</span><span class="sxs-lookup"><span data-stu-id="23179-119">Deployment documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="23179-120">Konfigurieren von VoIP-Nutzungen, Routen und Trunks</span><span class="sxs-lookup"><span data-stu-id="23179-120">Configure voice usages, routes, and trunk configurations</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="23179-p103">Erstellen Sie einen neuen PSTN-Verwendungseintrag. Hierbei handelt es sich um den gleichen Namen, der in der Standortrichtlinie für die Einstellung <strong>PSTN-Verwendung</strong> verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="23179-p103">Create a new PSTN usage record. This is the same name that is used for the <strong>PSTN Usage</strong> setting in the location policy.</span></span></p></li>
<li><p><span data-ttu-id="23179-123">Erstellen Sie eine VoIP-Route oder weisen Sie dem im vorherigen Schritt erstellten PSTN-Verwendungseintrag eine solche zu und lassen Sie das Gatewayattribut auf den E9-1-1-SIP-Trunk oder das ELIN-Gateway verweisen. </span><span class="sxs-lookup"><span data-stu-id="23179-123">Create or assign a voice route to the PSTN usage record created in the previous step and then point the gateway attribute to the E9-1-1 SIP trunk or ELIN gateway.</span></span></p></li>
<li><p><span data-ttu-id="23179-124">Stellen Sie für SIP-Trunk-E9-1-1-Dienstanbieter den Trunk, der E9-1-1-Anrufe über SIP verarbeiten soll, so ein, dass PIDF-LO-Daten weitergegeben werden. Verwenden Sie dazu das Cmdlet <strong>Set-CsTrunkConfiguration –EnablePIDFLOSupport</strong>.</span><span class="sxs-lookup"><span data-stu-id="23179-124">For a SIP trunk E9-1-1 service provider, set the trunk that will be handling E9-1-1 calls over the SIP to pass PIDF-LO data by using the <strong>Set-CsTrunkConfiguration –EnablePIDFLOSupport</strong> cmdlet.</span></span></p></li>
<li><p><span data-ttu-id="23179-p104">Optional können Sie für SIP-Trunk-E9-1-1-Dienstanbieter eine lokale PSTN-Route für Anrufe erstellen oder zuweisen, die nicht vom SIP-Trunk des E9-1-1-Dienstanbieters verwaltet werden. Diese Route wird verwendet, wenn keine Verbindung zum E9-1-1-Dienstanbieter besteht. Wenn dies von Ihrem E9-1-1-Dienstanbieter unterstützt wird, weisen Sie dem Gateway eine Trunkkonfigurationsregel zu, die die Notrufzeichenfolge in die DID (Direct Inward Dialing)-Nummer des nationalen/regionalen Telefoncenters für Notrufe (Emergency Call Response Center, ECRC) übersetzt.</span><span class="sxs-lookup"><span data-stu-id="23179-p104">Optionally, for a SIP trunk E9-1-1 service provider, create or assign a local PSTN route for calls that are not handled by the E9-1-1 service provider’s SIP trunk. This route will be used if the connection to the E9-1-1 service provider is not available. If supported by your E9-1-1 service provider, assign a trunk configuration rule to the gateway that translates the 911 dial string into the direct inward dialing (DID) number of the national/regional Emergency Call Response Center (ECRC).</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="23179-128">CSVoiceAdmin</span><span class="sxs-lookup"><span data-stu-id="23179-128">CSVoiceAdmin</span></span></p></td>
<td><p><span data-ttu-id="23179-129"><a href="lync-server-2013-configure-an-e9-1-1-voice-route.md">Konfigurieren einer E9-1-1-VoIP-Route in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="23179-129"><a href="lync-server-2013-configure-an-e9-1-1-voice-route.md">Configure an E9-1-1 voice route in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23179-130">Erstellen von Standortrichtlinien und Zuweisen dieser Standortrichtlinien zu Benutzern und Subnetzen</span><span class="sxs-lookup"><span data-stu-id="23179-130">Create location policies and assign them to users and subnets</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="23179-131">Überprüfen Sie die globale Standortrichtlinie.</span><span class="sxs-lookup"><span data-stu-id="23179-131">Review the global location policy.</span></span></p></li>
<li><p><span data-ttu-id="23179-132">Erstellen Sie eine Standortrichtlinie auf Benutzerebene oder erstellen Sie, wenn die Organisation über mehr als einen Standort mit verschiedenen Notfallverwendungen verfügt, eine Standortrichtlinie auf Netzwerkebene.</span><span class="sxs-lookup"><span data-stu-id="23179-132">Create a location policy with a user-level scope; or, if the organization has more than one site with different emergency usages, create a location policy with a network-level scope.</span></span></p></li>
<li><p><span data-ttu-id="23179-133">Weisen Sie die Standortrichtlinie Netzwerkstandorten zu.</span><span class="sxs-lookup"><span data-stu-id="23179-133">Assign the location policy to network sites.</span></span></p></li>
<li><p><span data-ttu-id="23179-134">Fügen Sie dem Netzwerkstandort geeignete Subnetze hinzu.</span><span class="sxs-lookup"><span data-stu-id="23179-134">Add the appropriate subnets to the network site.</span></span></p></li>
<li><p><span data-ttu-id="23179-135">(Optional) Weisen Sie die Standortrichtlinie Benutzerrichtlinien zu.</span><span class="sxs-lookup"><span data-stu-id="23179-135">(Optional) Assign the location policy to user policies.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="23179-136">CSVoiceAdmin</span><span class="sxs-lookup"><span data-stu-id="23179-136">CSVoiceAdmin</span></span></p>
<p><span data-ttu-id="23179-137">CSLocationAdmin (außer bei Erstellung von Standortrichtlinien)</span><span class="sxs-lookup"><span data-stu-id="23179-137">CSLocationAdmin (except for creating Location Policies)</span></span></p></td>
<td><p><span data-ttu-id="23179-138"><a href="lync-server-2013-create-location-policies.md">Erstellen von Standortrichtlinien in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="23179-138"><a href="lync-server-2013-create-location-policies.md">Create location policies in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="23179-139"><a href="lync-server-2013-add-a-location-policy-to-a-network-site.md">Hinzufügen einer Standortrichtlinie zu einer Netzwerk Website in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="23179-139"><a href="lync-server-2013-add-a-location-policy-to-a-network-site.md">Add a location policy to a network site in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="23179-140"><a href="lync-server-2013-associate-subnets-with-network-sites-for-e9-1-1.md">Zuordnen von Subnetzen zu Netzwerkstandorten für E9-1-1 in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="23179-140"><a href="lync-server-2013-associate-subnets-with-network-sites-for-e9-1-1.md">Associate subnets with network sites for E9-1-1 in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="23179-141">Konfigurieren der Standortdatenbank</span><span class="sxs-lookup"><span data-stu-id="23179-141">Configure the location database</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="23179-142">Füllen Sie die Datenbank mit einer Zuordnung von Netzwerkelementen zu Standorten auf.</span><span class="sxs-lookup"><span data-stu-id="23179-142">Populate the database with a mapping of network elements to locations.</span></span></p></li>
<li><p><span data-ttu-id="23179-143">Für Elin-Gateways fügen Sie die Elins zur &lt; Spalte CompanyName hinzu &gt; .</span><span class="sxs-lookup"><span data-stu-id="23179-143">For ELIN gateways, add the ELINs to the &lt;CompanyName&gt; column.</span></span></p></li>
<li><p><span data-ttu-id="23179-144">Konfigurieren Sie für die Verbindung zum E9-1-1-Dienstanbieter die Überprüfung der Adressen.</span><span class="sxs-lookup"><span data-stu-id="23179-144">Configure the connection to the E9-1-1 service provider for validating addresses.</span></span></p></li>
<li><p><span data-ttu-id="23179-145">Gleichen Sie die Adressen mit dem E9-1-1-Dienstanbieter ab.</span><span class="sxs-lookup"><span data-stu-id="23179-145">Validate the addresses with the E9-1-1 service provider.</span></span></p></li>
<li><p><span data-ttu-id="23179-146">Veröffentlichen Sie die aktualisierte Datenbank.</span><span class="sxs-lookup"><span data-stu-id="23179-146">Publish the updated database.</span></span></p></li>
<li><p><span data-ttu-id="23179-147">Laden Sie für ELIN-Gateways die ELINs in die ALI (Automatic Location Identification)-Datenbank Ihres PSTN-Betreibers hoch.</span><span class="sxs-lookup"><span data-stu-id="23179-147">For ELIN gateways, upload the ELINs to your PSTN carrier's Automatic Location Identification (ALI) database.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="23179-148">CSVoiceAdmin</span><span class="sxs-lookup"><span data-stu-id="23179-148">CSVoiceAdmin</span></span></p>
<p><span data-ttu-id="23179-149">CSLocationAdmin</span><span class="sxs-lookup"><span data-stu-id="23179-149">CSLocationAdmin</span></span></p></td>
<td><p><span data-ttu-id="23179-150"><a href="lync-server-2013-configure-the-location-database.md">Configure the location database in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="23179-150"><a href="lync-server-2013-configure-the-location-database.md">Configure the location database in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="23179-151">Konfigurieren von erweiterten Funktionen (optional)</span><span class="sxs-lookup"><span data-stu-id="23179-151">Configure Advanced Features (optional)</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="23179-152">Konfigurieren Sie die URL für die SNMP-Anwendung.</span><span class="sxs-lookup"><span data-stu-id="23179-152">Configure the URL for the SNMP application.</span></span></p></li>
<li><p><span data-ttu-id="23179-153">Konfigurieren Sie die URL für den Speicherort des Informationsdiensts für sekundären Standort.</span><span class="sxs-lookup"><span data-stu-id="23179-153">Configure the URL for the location of the Secondary Location Information service.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="23179-154">CSVoiceAdmin</span><span class="sxs-lookup"><span data-stu-id="23179-154">CSVoiceAdmin</span></span></p></td>
<td><p><span data-ttu-id="23179-155"><a href="lync-server-2013-configure-an-snmp-application.md">Konfigurieren einer SNMP-Anwendung in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="23179-155"><a href="lync-server-2013-configure-an-snmp-application.md">Configure an SNMP application in Lync Server 2013</a></span></span></p>
<p><span data-ttu-id="23179-156"><a href="lync-server-2013-configure-a-secondary-location-information-service.md">Konfigurieren eines sekundären Standort Informationsdiensts in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="23179-156"><a href="lync-server-2013-configure-a-secondary-location-information-service.md">Configure a secondary Location Information service in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="23179-157">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="23179-157">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

