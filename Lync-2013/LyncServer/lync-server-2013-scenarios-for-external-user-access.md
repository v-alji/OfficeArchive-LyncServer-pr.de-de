---
title: 'Lync Server 2013: Szenarien für den Zugriff durch externe Benutzer'
description: 'Lync Server 2013: Szenarien für den Zugriff durch externe Benutzer.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scenarios for external user access
ms:assetid: 25697446-b045-4d12-9b1c-47f694b4f224
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425727(v=OCS.15)
ms:contentKeyID: 48183640
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b212d371d5a87470fc3d849f185bb5c8659ce05
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442036"
---
# <a name="scenarios-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="6ecf6-103">Szenarien für den Zugriff durch externe Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6ecf6-103">Scenarios for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6ecf6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6ecf6-104">

<span> </span></span></span>

<span data-ttu-id="6ecf6-105">_**Letztes Änderungsdatum des Themas:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="6ecf6-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="6ecf6-106">Das Bereitstellen des Zugriffs externer Benutzer für lync Server 2013 setzt voraus, dass Sie mindestens einen Edgeserver und einen Reverse-Proxy in Ihrem Umkreisnetzwerk bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-106">Providing external user access for Lync Server 2013 requires that you deploy at least one Edge Server and one reverse proxy in your perimeter network.</span></span> <span data-ttu-id="6ecf6-107">Optional können Sie einen Director-oder Director-Pool in Ihrem internen Netzwerk bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-107">Optionally, you may deploy a Director or Director pool in your internal network.</span></span>

<span data-ttu-id="6ecf6-108">Wenn Sie eine größere Kapazität benötigen, als ein einzelner Edgeserver bereitstellen kann, oder wenn Sie eine hohe Verfügbarkeit für Ihre Edge-Server Bereitstellung benötigen, können Sie den Lastenausgleich konfigurieren und mehrere Edgeserver in einem Lastenausgleichspool bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-108">If you need greater capacity than a single Edge Server can provide, or if you need high availability for your Edge Server deployment, you can configure load balancing and deploy multiple Edge Servers in a load balanced pool.</span></span> <span data-ttu-id="6ecf6-109">Wenn Ihre Organisation über mehrere Rechenzentren verfügt, können Sie Edge-Server-oder Edge-Pool-Bereitstellungen an mehr als einem Standort haben.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-109">If your organization has multiple data centers, you can have Edge Server or Edge pool deployments at more than one location.</span></span> <span data-ttu-id="6ecf6-110">Allerdings kann nur eine der Edge-Server-Bereitstellungen als Verbund Route festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-110">However, only one of the Edge Server deployments can be designated as the federation route.</span></span>

<span data-ttu-id="6ecf6-111">In diesem Abschnitt werden die Szenarien für die Bereitstellung von Edge-Servern definiert und die Planungsabschnitte den möglichen Szenarien zugeordnet.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-111">This section defines the scenarios for Edge Server deployments and maps the planning sections to the possible scenarios.</span></span> <span data-ttu-id="6ecf6-112">Wenn Ihre Bereitstellung beispielsweise eine höhere Verfügbarkeit erfordert, Föderation mit den Funktionen für erweiterbare Messaging und Anwesenheitsinformationen (XMPP) und lync Mobility, wählen Sie die übereinstimmenden Einträge in der folgenden Tabelle aus, die diese Anforderungen erfüllen, und verwenden Sie die referenzierten Planungsabschnitte, um Ihre Bereitstellung zu definieren, wie im folgenden Flussdiagramm dargestellt.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-112">For example, if your deployment requires high availability, federation with extensible messaging and presence (XMPP) contacts, and Lync mobility, you would select the matching entries in the following table that would satisfy these requirements and use the referenced planning sections to define your deployment, as illustrated in the following flowchart.</span></span>

<span data-ttu-id="6ecf6-113">**Auswahlverfahren für Edge-Server-Bereitstellungsszenarien**</span><span class="sxs-lookup"><span data-stu-id="6ecf6-113">**Edge Server deployment scenario selection process**</span></span>

<span data-ttu-id="6ecf6-114">![Beispielbereitstellung (Flussdiagramm)](images/Gg425727.007100b5-6923-4909-bfd7-897d8867205f(OCS.15).jpg "Beispielbereitstellung (Flussdiagramm)")</span><span class="sxs-lookup"><span data-stu-id="6ecf6-114">![Sample deployment flowchart](images/Gg425727.007100b5-6923-4909-bfd7-897d8867205f(OCS.15).jpg "Sample deployment flowchart")</span></span>

<span data-ttu-id="6ecf6-115">Mithilfe dieses Vorgangs können Sie die Konfiguration aller potenziellen Features planen und dokumentieren, die Sie für Ihre Benutzer bereitstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-115">By using this process, you can plan for and document the configuration of all potential features that you intend to deploy for your users.</span></span> <span data-ttu-id="6ecf6-116">Sie können jedoch Föderations-und Mobilitätsdienste hinzufügen, nachdem Sie den Edgeserver bereitgestellt und den richtigen Vorgang bestätigt haben, bevor Sie weitere Features hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-116">However, you can add federation and mobility services after you have deployed the Edge Server and have confirmed the correct operation before adding other features.</span></span> <span data-ttu-id="6ecf6-117">Der Vorgang zum Hinzufügen von Features zu einer vorhandenen Edge-Server-Bereitstellung wird im Abschnitt Bereitstellung behandelt.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-117">The process of adding features to an existing Edge Server deployment is covered in the Deployment section.</span></span> <span data-ttu-id="6ecf6-118">Details zur Bereitstellung finden Sie unter [Bereitstellen des Zugriffs auf externe Benutzer in lync Server 2013](lync-server-2013-deploying-external-user-access.md) durch einschließen der Planung für diese Features während des anfänglichen Planungsprozesses können Sie die DNS-, Firewall-und Zertifikatanforderungen für die hinzugefügten Features vorbereiten, wodurch Sie die Zertifikate erwerben und die DNS-und Port/Protocol-Anforderungen im Voraus konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-118">For details on deployment, see [Deploying external user access in Lync Server 2013](lync-server-2013-deploying-external-user-access.md) By including planning for these features during the initial planning process, you can prepare for the DNS, firewall, and certificate requirements for the added features, which enables you to acquire the certificates and configure DNS and port/protocol requirements in advance.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="6ecf6-119">Wenn Sie beabsichtigen, die Edgeserver und Reverse Proxy zu installieren und später Features hinzuzufügen (beispielsweise Föderation und Mobilität), legen Sie fest, welche Zertifikate für alle Dienste nach der Bereitstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-119">If you are planning to install the Edge Servers and reverse proxy and then add features later (for example, federation and mobility), determine what certificates you will require for all services after deployment.</span></span> <span data-ttu-id="6ecf6-120">Wenn Sie die Zertifikate für alle Features im Voraus planen und erwerben, zunächst bereitgestellt oder nicht, müssen Sie keine neuen Zertifikate mehr anfordern, um die Anforderungen des Verbandes (also auf den Edgeserver) oder des Reverse-Proxys (also für Mobilitätsdienste) zu erfüllen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-120">Planning for and acquiring the certificates for all features in advance, initially deployed or not, saves you from having to order new certificates to satisfy the requirements of federation (that is, on the Edge Servers) or the reverse proxy (that is, for mobility services).</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="6ecf6-121">Alle Edge-Dienste werden auf jedem Edgeserver ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-121">All edge services run on each Edge Server.</span></span> <span data-ttu-id="6ecf6-122">Dienste können nicht zwischen zwei verschiedenen Edge-Servern aufgeteilt werden.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-122">Services cannot be split between two different Edge Servers.</span></span> <span data-ttu-id="6ecf6-123">Wenn Sie einen Edge-Pool für Skalierbarkeit bereitstellen, werden alle Edge-Dienste auf jedem Edgeserver im Pool bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-123">If you deploy an Edge pool for scalability, all edge services are deployed on each Edge Server in the pool.</span></span> <span data-ttu-id="6ecf6-124">XMPP Federation, Office Communications Server und lync Server Federation, öffentliche Chat Verbindungen und Clientmobilität sind zusätzliche Dienste, die bereitgestellt werden können, nachdem Sie Ihren First Edge-Server oder Edge-Pool bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-124">XMPP federation, Office Communications Server, and Lync Server federation, public IM connectivity and client mobility are additional services that can be deployed after you have deployed your first Edge Server or Edge pool.</span></span> <span data-ttu-id="6ecf6-125">Mobility Services ist ein Feature, das den Reverse-Proxy verwendet.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-125">Mobility services is a feature that uses the reverse proxy.</span></span> <span data-ttu-id="6ecf6-126">Die Installation von Mobility Services fügt Ihren Edge-Servern keine Features hinzu, erfordert aber eine Neukonfiguration Ihres Reverse-Proxys.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-126">Installation of mobility services will not add features to your Edge Servers, but will require reconfiguration of your reverse proxy.</span></span> <span data-ttu-id="6ecf6-127">In der Spalte " <STRONG>Installationsziel</STRONG> ", in der diese Features aufgelistet sind, finden Sie Planungsanleitungen in der zugehörigen Spalte unter <STRONG>Edge-Server-Planung (Abschnitt) oder in Abschnitten</STRONG> für die gleichzeitige Planung dieser Features, die bei der Installation und Konfiguration der Edgeserver bereitgestellt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-127">The <STRONG>Installation goal</STRONG> column that lists these features provides planning guidance in the associated column under <STRONG>Edge Server planning section or sections</STRONG> for concurrently planning these features to be deployed when the Edge Servers are installed and configured.</span></span>



</div>

<div>

## <a name="identifying-and-mapping-your-deployment-goals"></a><span data-ttu-id="6ecf6-128">Identifizieren und Zuordnen von Bereitstellungszielen</span><span class="sxs-lookup"><span data-stu-id="6ecf6-128">Identifying and Mapping Your Deployment Goals</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="6ecf6-129">Installationsziel</span><span class="sxs-lookup"><span data-stu-id="6ecf6-129">Installation goal</span></span></th>
<th><span data-ttu-id="6ecf6-130">Dokumentation zur Edge-Server-Planung</span><span class="sxs-lookup"><span data-stu-id="6ecf6-130">Edge Server planning documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="6ecf6-131">Sie haben entschieden, dass ein einzelner Server für Edge-Dienste in Ihrer Infrastruktur ausreicht.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-131">You have decided that a single server is sufficient for Edge services in your infrastructure.</span></span> <span data-ttu-id="6ecf6-132">Darüber hinaus beabsichtigen Sie, private IP-Adressen für die externen Edge-Server-Schnittstellen mit NAT in das Internet zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-132">You also intend to use private IP addresses for the Edge server external interfaces with NAT to the Internet.</span></span></p>
<p><span data-ttu-id="6ecf6-133">Verwenden Sie diesen Planungsabschnitt, wenn Sie einen einzelnen Edgeserver in Ihrem Umkreis bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-133">Use this planning section if you are deploying a single Edge Server in your perimeter.</span></span> <span data-ttu-id="6ecf6-134">Sie stellen einen Edgeserver mit privaten IP-Adressen bereit, die dem Edgeserver zugewiesen sind, und verwenden NAT, um die öffentlichen IP-Adressen für die externen Benutzer im Internet bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-134">You will deploy an Edge Server with private IP addresses assigned to the Edge Server and will use NAT to provide the public IP addresses for the external users on the Internet.</span></span></p></td>
<td><p><span data-ttu-id="6ecf6-135"><a href="lync-server-2013-single-consolidated-edge-with-private-ip-addresses-and-nat.md">Einzelner konsolidierter Edgeserver mit privaten IP-Adressen und NAT in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="6ecf6-135"><a href="lync-server-2013-single-consolidated-edge-with-private-ip-addresses-and-nat.md">Single consolidated edge with private IP addresses and NAT in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ecf6-136">Sie haben entschieden, dass ein einzelner Server für Edge-Dienste in Ihrer Infrastruktur ausreicht.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-136">You have decided that a single server is sufficient for Edge services in your infrastructure.</span></span> <span data-ttu-id="6ecf6-137">Sie beabsichtigen auch, öffentliche IP-Adressen für die externen Edge-Server-Schnittstellen für das Internet zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-137">You also intend to use public IP addresses for the Edge server external interfaces to the Internet.</span></span></p>
<p><span data-ttu-id="6ecf6-138">Verwenden Sie diesen Planungsabschnitt, wenn Sie einen einzelnen Edgeserver in Ihrem Umkreis bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-138">Use this planning section if you are deploying a single Edge Server in your perimeter.</span></span> <span data-ttu-id="6ecf6-139">Sie stellen einen Edgeserver mit öffentlichen IP-Adressen bereit, die dem Edgeserver zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-139">You will deploy an Edge Server with public IP addresses assigned to the Edge Server.</span></span> <span data-ttu-id="6ecf6-140">Anstelle von NAT verwenden Sie Routing in diesem Szenario.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-140">Instead of NAT, you will use routing in this scenario.</span></span> <span data-ttu-id="6ecf6-141">Die tatsächliche öffentliche IP-Adresse des Edge-Servers wird für externe Benutzer Verbindungen bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-141">The actual public IP address of the Edge Server are made available for external user connections.</span></span></p></td>
<td><p><span data-ttu-id="6ecf6-142"><a href="lync-server-2013-single-consolidated-edge-with-public-ip-addresses.md">Einzelner konsolidierter Edgeserver mit öffentlichen IP-Adressen in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="6ecf6-142"><a href="lync-server-2013-single-consolidated-edge-with-public-ip-addresses.md">Single consolidated edge with public IP addresses in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ecf6-143">Sie haben entschieden, dass eine höhere Verfügbarkeit der Edge-Dienste für Ihre Benutzer wichtig ist, und Sie werden zwei oder mehr Edgeserver in diesem Pool bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-143">You have decided that high availability of the Edge services is important to your users and you will deploy two or more Edge Servers in this pool.</span></span> <span data-ttu-id="6ecf6-144">Darüber hinaus beabsichtigen Sie, private IP-Adressen für die externen Edge-Server-Schnittstellen mit NAT in das Internet zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-144">You also intend to use private IP addresses for the Edge Server external interfaces with NAT to the Internet.</span></span></p>
<p><span data-ttu-id="6ecf6-145">Verwenden Sie diesen Planungsabschnitt, wenn Sie einen Pool von Edgeserver in Ihrem Umkreis bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-145">Use this planning section if you are deploying a pool of Edge Servers in your perimeter.</span></span> <span data-ttu-id="6ecf6-146">Sie stellen die Edgeserver mit privaten IP-Adressen bereit, die dem Edgeserver zugewiesen sind, indem Sie den DNS-Lastenausgleich verwenden, um die Kommunikation über den Pool zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-146">You will deploy the Edge Servers with private IP addresses assigned to the Edge Server, using DNS load balancing to distribute communication across the pool.</span></span> <span data-ttu-id="6ecf6-147">Sie verwenden NAT, um die öffentlichen IP-Adressen für die externen Benutzer im Internet bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-147">You will use NAT to provide the public IP addresses for the external users on the Internet.</span></span></p></td>
<td><p><span data-ttu-id="6ecf6-148"><a href="lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md">Skalierter konsolidierter Edgeserver, DNS-Lastenausgleich mit privaten IP-Adressen und NAT in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="6ecf6-148"><a href="lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-private-ip-addresses-using-nat.md">Scaled consolidated edge, DNS load balancing with private IP addresses using NAT in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ecf6-149">Sie haben entschieden, dass eine höhere Verfügbarkeit der Edge-Dienste für Ihre Benutzer wichtig ist, und Sie werden zwei oder mehr Edgeserver in diesem Pool bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-149">You have decided that high availability of the Edge services is important to your users and you will deploy two or more Edge Servers in this pool.</span></span> <span data-ttu-id="6ecf6-150">Sie beabsichtigen auch, öffentliche IP-Adressen für die externen Edge-Server-Schnittstellen für das Internet zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-150">You also intend to use public IP addresses for the Edge Server external interfaces to the Internet.</span></span></p>
<p><span data-ttu-id="6ecf6-151">Verwenden Sie diesen Planungsabschnitt, wenn Sie einen Pool von Edgeserver in Ihrem Umkreis bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-151">Use this planning section if you are deploying a pool of Edge Servers in your perimeter.</span></span> <span data-ttu-id="6ecf6-152">Sie stellen die Edgeserver mit öffentlichen IP-Adressen bereit, die dem Edgeserver zugewiesen sind, indem Sie den DNS-Lastenausgleich verwenden, um die Kommunikation über den Pool zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-152">You will deploy the Edge Servers with public IP addresses assigned to the Edge Server, using DNS load balancing to distribute communication across the pool.</span></span> <span data-ttu-id="6ecf6-153">Anstelle von NAT verwenden Sie Routing, um die öffentlichen IP-Adressen für die externen Benutzer im Internet bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-153">Instead of NAT, you will use routing to provide the public IP addresses for the external users on the Internet.</span></span></p></td>
<td><p><span data-ttu-id="6ecf6-154"><a href="lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md">Skalierter konsolidierter Edgeserver, DNS-Lastenausgleich mit öffentlichen IP-Adressen in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="6ecf6-154"><a href="lync-server-2013-scaled-consolidated-edge-dns-load-balancing-with-public-ip-addresses.md">Scaled consolidated edge, DNS load balancing with public IP addresses in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ecf6-155">Sie haben entschieden, dass die hohe Verfügbarkeit der Edge-Dienste für Ihre Benutzer wichtig ist, und dass Sie zwei oder mehr Edgeserver in diesem Pool mithilfe eines Hardwarelastenausgleichs bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-155">You have decided that high availability of the Edge services is important to your users and you will deploy two or more Edge Servers in this pool using a hardware load balancer.</span></span></p>
<p><span data-ttu-id="6ecf6-156">Verwenden Sie diesen Planungsabschnitt, wenn Sie einen Pool von Edgeserver in Ihrem Umkreis bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-156">Use this planning section if you are deploying a pool of Edge Servers in your perimeter.</span></span> <span data-ttu-id="6ecf6-157">Sie stellen die Edgeserver mit öffentlichen IP-Adressen bereit, die dem Edgeserver zugewiesen sind, und verwenden Hardwarelastenausgleichs, um die Kommunikation über den Pool zu verteilen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-157">You will deploy the Edge Servers with public IP addresses assigned to the Edge Server, using hardware load balancers to distribute communication across the pool.</span></span> <span data-ttu-id="6ecf6-158">Anstelle von NAT verwenden Sie Routing, um die öffentlichen IP-Adressen für die externen Benutzer im Internet bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-158">Instead of NAT, you will use routing to provide the public IP addresses for the external users on the Internet.</span></span></p></td>
<td><p><span data-ttu-id="6ecf6-159"><a href="lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md">Skalierter konsolidierter Edgeserver mit Hardwarelastenausgleich in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="6ecf6-159"><a href="lync-server-2013-scaled-consolidated-edge-with-hardware-load-balancers.md">Scaled consolidated edge with hardware load balancers in Lync Server 2013</a></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="6ecf6-160">In den Verbundszenarien können Sie das Feature planen, mit dem die Typen von Partnern erweitert werden, mit denen Ihre Benutzer kommunizieren können.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-160">The federation scenarios allow you to plan for the feature that will extend the types of partners that your users can communicate with.</span></span></p>
<ul>
<li><p><span data-ttu-id="6ecf6-161">Lync Server-Verbund</span><span class="sxs-lookup"><span data-stu-id="6ecf6-161">Lync Server federation</span></span></p></li>
<li><p><span data-ttu-id="6ecf6-162">Office Communications Server-Föderation</span><span class="sxs-lookup"><span data-stu-id="6ecf6-162">Office Communications Server federation</span></span></p></li>
<li><p><span data-ttu-id="6ecf6-163">Verbindung mit öffentlichen Chatdiensten</span><span class="sxs-lookup"><span data-stu-id="6ecf6-163">Public IM connectivity</span></span></p></li>
<li><p><span data-ttu-id="6ecf6-164">XMPP-Föderation</span><span class="sxs-lookup"><span data-stu-id="6ecf6-164">XMPP federation</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="6ecf6-165">Planen von Verbundszenarien</span><span class="sxs-lookup"><span data-stu-id="6ecf6-165">Planning for Federation Scenarios</span></span></p>
<ul>
<li><p><span data-ttu-id="6ecf6-166"><a href="lync-server-2013-planning-for-lync-server-and-office-communications-server-federation.md">Planen der lync Server 2013-und Office Communications Server-Föderation</a></span><span class="sxs-lookup"><span data-stu-id="6ecf6-166"><a href="lync-server-2013-planning-for-lync-server-and-office-communications-server-federation.md">Planning for Lync Server 2013 and Office Communications Server federation</a></span></span></p></li>
<li><p><span data-ttu-id="6ecf6-167"><a href="lync-server-2013-planning-for-public-instant-messaging-connectivity.md">Planen der öffentlichen Instant Messaging-Konnektivität in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="6ecf6-167"><a href="lync-server-2013-planning-for-public-instant-messaging-connectivity.md">Planning for public instant messaging connectivity in Lync Server 2013</a></span></span></p></li>
<li><p><span data-ttu-id="6ecf6-168"><a href="lync-server-2013-planning-for-extensible-messaging-and-presence-protocol-xmpp-federation.md">Planen der erweiterbaren Messaging-und Anwesenheits Protokoll (XMPP)-Föderation in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="6ecf6-168"><a href="lync-server-2013-planning-for-extensible-messaging-and-presence-protocol-xmpp-federation.md">Planning for extensible messaging and presence protocol (XMPP) federation in Lync Server 2013</a></span></span></p></li>
</ul></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="6ecf6-169">Mobilitätsdienste werden über den Reverse-Proxy angeboten.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-169">Mobility services are offered through the reverse proxy.</span></span> <span data-ttu-id="6ecf6-170">Dienste, die die Mobilität für externe Benutzer ermöglichen, werden auf dem Front-End-Server oder im Front-End-Pool bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-170">Services that enable mobility for external users are deployed on the Front End Server or Front End pool.</span></span> <span data-ttu-id="6ecf6-171">Sie erstellen oder ändern vorhandene Veröffentlichungsregeln auf dem Reverse-Proxy, um Mobilitätsdienste für Ihre externen Benutzer zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-171">You create or modify existing publishing rules on the reverse proxy to enable mobility services for your external users.</span></span></p></td>
<td><p><span data-ttu-id="6ecf6-172"><a href="lync-server-2013-planning-for-mobility.md">Planen der Mobilität in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="6ecf6-172"><a href="lync-server-2013-planning-for-mobility.md">Planning for mobility in Lync Server 2013</a></span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!TIP]  
> <span data-ttu-id="6ecf6-173">In den folgenden Szenarien sind Abschnitte Referenzarchitekturen, Beispiel-DNS, Port/Protokoll-Definitionen und Zertifikatanforderungen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-173">In the following Scenarios sections are reference architectures, example DNS, port/protocol definitions, and certificate requirements.</span></span> <span data-ttu-id="6ecf6-174">Ebenfalls enthalten sind Diagramme für Ihre DNS-, Port/Protocol-Definitionen und Zertifikatanforderungen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-174">Also included are diagrams for your DNS, port/protocol definitions and certificate needs.</span></span> <span data-ttu-id="6ecf6-175">In den Diagrammen wird eine Vorlage bereitgestellt, die Sie ausfüllen und an andere Teams verteilen können (beispielsweise das Netzwerkteam Ihrer Organisation, das Team für öffentliche Schlüsselinfrastruktur und das Server Bereitstellungsteam).</span><span class="sxs-lookup"><span data-stu-id="6ecf6-175">The diagrams will provide a template for you to fill in and distribute to other teams (for example, your organization’s Network Team, Public Key Infrastructure Team, and Server Deployment Team).</span></span> <span data-ttu-id="6ecf6-176">Das Ziel der Diagramme besteht darin, die Kommunikation zu verbessern und den Erfolg zu gewährleisten, wenn die erforderlichen Edge-Server-Konfigurationselemente den Personen mitgeteilt werden, die die eigentliche Konfigurationsarbeit durchführen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-176">The goal of the diagrams is to enhance communication and to ensure success when communicating the required Edge Server configuration elements to the people who will do the actual configuration work.</span></span> <span data-ttu-id="6ecf6-177">Wir empfehlen, dass Sie die Diagramme und zugehörigen Referenzarchitekturen verwenden, um Ihre Bereitstellung zu planen.</span><span class="sxs-lookup"><span data-stu-id="6ecf6-177">We recommend that you use the diagrams and associated reference architectures to plan your deployment.</span></span>



<span data-ttu-id="6ecf6-178"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6ecf6-178"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

