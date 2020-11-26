---
title: 'Lync Server 2013: Definieren der Anforderungen für Notrufe'
description: 'Lync Server 2013: Definieren Ihrer Anforderungen für Notrufe.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining your requirements for emergency calls
ms:assetid: 5c12b517-9be6-41d0-83e2-11c78793620c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398404(v=OCS.15)
ms:contentKeyID: 48184276
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8d3c9908dcb4008a1442af86971e42eb4096a98b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430833"
---
# <a name="defining-your-requirements-for-emergency-calls-in-lync-server-2013"></a><span data-ttu-id="4492c-103">Definieren der Anforderungen für Notrufe in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4492c-103">Defining your requirements for emergency calls in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4492c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4492c-104">

<span> </span></span></span>

<span data-ttu-id="4492c-105">_**Letztes Änderungsdatum des Themas:** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="4492c-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="4492c-106">Bevor Sie eine Microsoft lync Server 2013 E9-1-1-Bereitstellung beginnen, sollten Sie zunächst in der Lage sein, die in den folgenden Abschnitten aufgeführten Fragen zu beantworten.</span><span class="sxs-lookup"><span data-stu-id="4492c-106">Before you begin a Microsoft Lync Server 2013 E9-1-1 deployment, you should first be able to answer the questions detailed in the following sections.</span></span> <span data-ttu-id="4492c-107">Welche Planungsmaßnahmen erforderlich sind, ist abhängig von der E9-1-1-Lösung, die Sie bereitstellen möchten: einen SIP-Trunk-E9-1-1-Dienstanbieter oder ein ELIN-Gateway (Emergency Location Identification Number).</span><span class="sxs-lookup"><span data-stu-id="4492c-107">The planning you need to do depends on the type of E9-1-1 solution that you choose to deploy—a SIP trunk E9-1-1 service provider or an Emergency Location Identification Number (ELIN) gateway.</span></span> <span data-ttu-id="4492c-108">In der folgenden Tabelle sind die Abschnitte in dieser Planungsmappe aufgeführt, die Sie für die jeweilige Lösung berücksichtigen müssen.</span><span class="sxs-lookup"><span data-stu-id="4492c-108">The following table identifies the sections in this planning workbook that you’ll need to review for each of those solutions.</span></span>

### <a name="planning-steps-by-type-of-e9-1-1-solution"></a><span data-ttu-id="4492c-109">Planungsschritte nach Art der E9-1-1-Lösung</span><span class="sxs-lookup"><span data-stu-id="4492c-109">Planning Steps by Type of E9-1-1 Solution</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="4492c-110">SIP-Trunk-Dienstanbieter</span><span class="sxs-lookup"><span data-stu-id="4492c-110">SIP trunk service provider</span></span></th>
<th><span data-ttu-id="4492c-111">ELIN-Gateway</span><span class="sxs-lookup"><span data-stu-id="4492c-111">ELIN gateway</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="4492c-112"><a href="lync-server-2013-defining-the-scope-of-the-e9-1-1-deployment.md">Definieren des Bereichs der E9-1-1-Bereitstellung in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4492c-112"><a href="lync-server-2013-defining-the-scope-of-the-e9-1-1-deployment.md">Defining the scope of the E9-1-1 deployment in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="4492c-113"><a href="lync-server-2013-defining-the-scope-of-the-e9-1-1-deployment.md">Definieren des Bereichs der E9-1-1-Bereitstellung in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4492c-113"><a href="lync-server-2013-defining-the-scope-of-the-e9-1-1-deployment.md">Defining the scope of the E9-1-1 deployment in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4492c-114"><a href="lync-server-2013-defining-the-network-elements-used-to-determine-location.md">Definieren der Netzwerkelemente, die zum Ermitteln des Standorts in lync Server 2013 verwendet werden</a></span><span class="sxs-lookup"><span data-stu-id="4492c-114"><a href="lync-server-2013-defining-the-network-elements-used-to-determine-location.md">Defining the network elements used to determine location in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="4492c-115"><a href="lync-server-2013-defining-the-network-elements-used-to-determine-location.md">Definieren der Netzwerkelemente, die zum Ermitteln des Standorts in lync Server 2013 verwendet werden</a></span><span class="sxs-lookup"><span data-stu-id="4492c-115"><a href="lync-server-2013-defining-the-network-elements-used-to-determine-location.md">Defining the network elements used to determine location in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4492c-116"><a href="lync-server-2013-enabling-users-for-e9-1-1.md">Aktivieren von Benutzern für E9-1-1 in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4492c-116"><a href="lync-server-2013-enabling-users-for-e9-1-1.md">Enabling users for E9-1-1 in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="4492c-117"><a href="lync-server-2013-enabling-users-for-e9-1-1.md">Aktivieren von Benutzern für E9-1-1 in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4492c-117"><a href="lync-server-2013-enabling-users-for-e9-1-1.md">Enabling users for E9-1-1 in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4492c-118"><a href="lync-server-2013-managing-locations-for-sip-trunk-service-providers.md">Verwalten von Speicherorten für SIP Trunk-Dienstanbieter in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4492c-118"><a href="lync-server-2013-managing-locations-for-sip-trunk-service-providers.md">Managing locations for SIP trunk service providers in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="4492c-119"><a href="lync-server-2013-managing-locations-for-elin-gateways.md">Verwalten von Speicherorten für Elin-Gateways in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4492c-119"><a href="lync-server-2013-managing-locations-for-elin-gateways.md">Managing locations for ELIN gateways in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4492c-120"><a href="lync-server-2013-defining-the-user-experience-for-manually-acquiring-a-location.md">Definieren der Benutzeroberfläche für den manuellen Erwerb eines Speicherorts in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4492c-120"><a href="lync-server-2013-defining-the-user-experience-for-manually-acquiring-a-location.md">Defining the user experience for manually acquiring a location in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="4492c-121"><a href="lync-server-2013-defining-the-user-experience-for-manually-acquiring-a-location.md">Definieren der Benutzeroberfläche für den manuellen Erwerb eines Speicherorts in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4492c-121"><a href="lync-server-2013-defining-the-user-experience-for-manually-acquiring-a-location.md">Defining the user experience for manually acquiring a location in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4492c-122"><a href="lync-server-2013-designing-the-sip-trunk-for-e9-1-1.md">Entwerfen des SIP-Trunks für E9-1-1 in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4492c-122"><a href="lync-server-2013-designing-the-sip-trunk-for-e9-1-1.md">Designing the SIP trunk for E9-1-1 in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="4492c-123"><a href="lync-server-2013-including-the-security-desk.md">Einschließen des Security Desks in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4492c-123"><a href="lync-server-2013-including-the-security-desk.md">Including the security desk in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4492c-124"><a href="lync-server-2013-including-the-security-desk.md">Einschließen des Security Desks in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4492c-124"><a href="lync-server-2013-including-the-security-desk.md">Including the security desk in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="4492c-125"><a href="lync-server-2013-defining-the-location-policy.md">Definieren der Standortrichtlinie für lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4492c-125"><a href="lync-server-2013-defining-the-location-policy.md">Defining the location policy for Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4492c-126"><a href="lync-server-2013-choosing-an-e9-1-1-service-provider.md">Auswählen eines E9-1-1-Dienstanbieters für lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4492c-126"><a href="lync-server-2013-choosing-an-e9-1-1-service-provider.md">Choosing an E9-1-1 service provider for Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="4492c-127"><a href="lync-server-2013-assigning-location-policy-scope.md">Zuweisen von Standortrichtlinien Bereich in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4492c-127"><a href="lync-server-2013-assigning-location-policy-scope.md">Assigning location policy scope in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="4492c-128"><a href="lync-server-2013-defining-the-location-policy.md">Definieren der Standortrichtlinie für lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4492c-128"><a href="lync-server-2013-defining-the-location-policy.md">Defining the location policy for Lync Server 2013</a></span></span></p></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="4492c-129"><a href="lync-server-2013-assigning-location-policy-scope.md">Zuweisen von Standortrichtlinien Bereich in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="4492c-129"><a href="lync-server-2013-assigning-location-policy-scope.md">Assigning location policy scope in Lync Server 2013</a></span></span></p></td>
<td></td>
</tr>
</tbody>
</table>


<div>

## <a name="in-this-section"></a><span data-ttu-id="4492c-130">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="4492c-130">In This Section</span></span>

  - [<span data-ttu-id="4492c-131">Definieren des Bereichs der E9-1-1-Bereitstellung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4492c-131">Defining the scope of the E9-1-1 deployment in Lync Server 2013</span></span>](lync-server-2013-defining-the-scope-of-the-e9-1-1-deployment.md)

  - [<span data-ttu-id="4492c-132">Definieren der Netzwerkelemente, die zum Ermitteln des Standorts in lync Server 2013 verwendet werden</span><span class="sxs-lookup"><span data-stu-id="4492c-132">Defining the network elements used to determine location in Lync Server 2013</span></span>](lync-server-2013-defining-the-network-elements-used-to-determine-location.md)

  - [<span data-ttu-id="4492c-133">Aktivieren von Benutzern für E9-1-1 in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4492c-133">Enabling users for E9-1-1 in Lync Server 2013</span></span>](lync-server-2013-enabling-users-for-e9-1-1.md)

  - [<span data-ttu-id="4492c-134">Verwalten von Speicherorten für SIP Trunk-Dienstanbieter in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4492c-134">Managing locations for SIP trunk service providers in Lync Server 2013</span></span>](lync-server-2013-managing-locations-for-sip-trunk-service-providers.md)

  - [<span data-ttu-id="4492c-135">Verwalten von Speicherorten für Elin-Gateways in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4492c-135">Managing locations for ELIN gateways in Lync Server 2013</span></span>](lync-server-2013-managing-locations-for-elin-gateways.md)

  - [<span data-ttu-id="4492c-136">Definieren der Benutzeroberfläche für den manuellen Erwerb eines Speicherorts in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4492c-136">Defining the user experience for manually acquiring a location in Lync Server 2013</span></span>](lync-server-2013-defining-the-user-experience-for-manually-acquiring-a-location.md)

  - [<span data-ttu-id="4492c-137">Entwerfen des SIP-Trunks für E9-1-1 in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4492c-137">Designing the SIP trunk for E9-1-1 in Lync Server 2013</span></span>](lync-server-2013-designing-the-sip-trunk-for-e9-1-1.md)

  - [<span data-ttu-id="4492c-138">Einschließen des Security Desks in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4492c-138">Including the security desk in Lync Server 2013</span></span>](lync-server-2013-including-the-security-desk.md)

  - [<span data-ttu-id="4492c-139">Auswählen eines E9-1-1-Dienstanbieters für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4492c-139">Choosing an E9-1-1 service provider for Lync Server 2013</span></span>](lync-server-2013-choosing-an-e9-1-1-service-provider.md)

  - [<span data-ttu-id="4492c-140">Definieren der Standortrichtlinie für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4492c-140">Defining the location policy for Lync Server 2013</span></span>](lync-server-2013-defining-the-location-policy.md)

  - [<span data-ttu-id="4492c-141">Zuweisen von Standortrichtlinien Bereich in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4492c-141">Assigning location policy scope in Lync Server 2013</span></span>](lync-server-2013-assigning-location-policy-scope.md)

<span data-ttu-id="4492c-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4492c-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

