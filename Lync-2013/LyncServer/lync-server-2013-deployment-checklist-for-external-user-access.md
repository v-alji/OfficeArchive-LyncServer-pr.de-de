---
title: 'Lync Server 2013: Prüfliste zur Bereitstellung für den Zugriff durch externe Benutzer'
description: 'Lync Server 2013: Bereitstellungscheckliste für den Zugriff durch externe Benutzer.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deployment checklist for external user access
ms:assetid: 3f55f502-88a0-4315-8783-45a32a0b78ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425910(v=OCS.15)
ms:contentKeyID: 48183947
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a31534d1dcf3ba4dd0bb222de682d247c9683f94
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394634"
---
# <a name="deployment-checklist-for-external-user-access-in-lync-server-2013"></a><span data-ttu-id="9d057-103">Prüfliste zur Bereitstellung für den Zugriff durch externe Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9d057-103">Deployment checklist for external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9d057-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9d057-104">

<span> </span></span></span>

<span data-ttu-id="9d057-105">_**Letztes Änderungsdatum des Themas:** 2014-02-04_</span><span class="sxs-lookup"><span data-stu-id="9d057-105">_**Topic Last Modified:** 2014-02-04_</span></span>

<span data-ttu-id="9d057-106">Bevor Sie Ihr Umkreisnetzwerk bereitstellen und die Unterstützung für externe Benutzer implementieren, müssen Sie Ihre Microsoft lync Server 2013-internen Server bereits bereitgestellt haben, einschließlich eines Front-End-Pools oder eines Standard Edition-Servers.</span><span class="sxs-lookup"><span data-stu-id="9d057-106">Before you deploy your perimeter network and implement support for external users, you must already have deployed your Microsoft Lync Server 2013 internal servers, including a Front End pool or a Standard Edition server.</span></span> <span data-ttu-id="9d057-107">Wenn Sie beabsichtigen, die optionalen Directors in Ihrem internen Netzwerk bereitzustellen, sollten Sie diese vor der Bereitstellung von Edgeserver auch bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9d057-107">If you plan to deploy the optional Directors in your internal network, you should also deploy them prior to deploying Edge Servers.</span></span> <span data-ttu-id="9d057-108">Details zum Director-Bereitstellungsprozess finden Sie unter [Szenarien für den Director in lync Server 2013](lync-server-2013-scenarios-for-the-director.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="9d057-108">For details about the Director deployment process, see [Scenarios for the Director in Lync Server 2013](lync-server-2013-scenarios-for-the-director.md) in the Planning documentation.</span></span>

<span data-ttu-id="9d057-109">Microsoft lync Server 2013 umfasst Tools zur Vereinfachung der Planung und Bereitstellung von internen Servern und Edgeserver.</span><span class="sxs-lookup"><span data-stu-id="9d057-109">Microsoft Lync Server 2013 includes tools to facilitate planning and deployment of both internal servers and Edge Servers.</span></span> <span data-ttu-id="9d057-110">Veröffentlichen Sie nach Abschluss der Topologie die resultierende Topologie-Definition in Ihrer Produktionsumgebung.</span><span class="sxs-lookup"><span data-stu-id="9d057-110">After the topology is completed, publish the resulting topology definition to your production environment.</span></span> <span data-ttu-id="9d057-111">Zu diesem Zweck müssen Sie Mitglied der Gruppe "Domänen- **Admins** " und der Gruppe " **RTCUniversalServerAdmins** " sein.</span><span class="sxs-lookup"><span data-stu-id="9d057-111">To do this, you must be a member of the **Domain Admins** group and the **RTCUniversalServerAdmins** group.</span></span>

  - <span data-ttu-id="9d057-112">**Planungs Tool**   Office Communications Server 2007 R2 enthielt ein Planungstool und ein Edge-Planning-Tool, mit dem Sie die Topologie entwerfen können.</span><span class="sxs-lookup"><span data-stu-id="9d057-112">**Planning Tool**   Office Communications Server 2007 R2 included a Planning Tool and an Edge Planning Tool that you could use to help guide topology design.</span></span> <span data-ttu-id="9d057-113">In lync Server 2010 wurden diese beiden Tools zu einem einzigen Planungs Tool kombiniert, das zusätzliche Features und Funktionen aufweist, wie etwa das Sammeln geplanter Benutzeranzahl, Sprachanforderungen, Zugriffstypen für externe Benutzer und Verbund Optionen.</span><span class="sxs-lookup"><span data-stu-id="9d057-113">In Lync Server 2010, these two tools were combined into a single Planning Tool that has additional features and functionality, such as collecting planned user count, voice requirements, external user access types, and federation options.</span></span> <span data-ttu-id="9d057-114">Darüber hinaus können Sie die Netzwerkparameter Ihrer Infrastruktur wie IP-Adressen, Lastenausgleichsmodul Typen und andere Aspekte des Umkreisnetzwerks planen.</span><span class="sxs-lookup"><span data-stu-id="9d057-114">Additionally, you can plan your infrastructure’s network parameters, such as IP addresses, load balancer types and other perimeter network considerations.</span></span>

  - <span data-ttu-id="9d057-115">**Topologie-Generator**   Der lync Server 2013-Topologie-Generator hilft Ihnen beim Definieren Ihrer Topologie und Komponenten.</span><span class="sxs-lookup"><span data-stu-id="9d057-115">**Topology Builder**   Lync Server 2013 Topology Builder helps you define your topology and components.</span></span> <span data-ttu-id="9d057-116">Der Topologie-Generator ist für die Bereitstellung von Servern mit lync Server 2013 unerlässlich.</span><span class="sxs-lookup"><span data-stu-id="9d057-116">Topology Builder is essential to deploying servers running Lync Server 2013.</span></span> <span data-ttu-id="9d057-117">Der Topologie-Generator veröffentlicht die Ergebnisse in einem zentralen Verwaltungsspeicher, der zum Konfigurieren aller Server mit lync Server 2013 in Ihrer Organisation verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="9d057-117">Topology Builder publishes the results to a Central Management store that is used to configure all of the servers running Lync Server 2013 in your organization.</span></span> <span data-ttu-id="9d057-118">Sie können lync Server 2013 nicht auf Servern installieren, ohne den Topology Builder verwenden zu müssen.</span><span class="sxs-lookup"><span data-stu-id="9d057-118">You cannot install Lync Server 2013 on servers without using Topology Builder.</span></span>

<span data-ttu-id="9d057-119">Wenn Sie Ihre Edge-Topologie während des Planungsprozesses entworfen haben, einschließlich der Ausführung des Topologie-Generators zum Definieren Ihrer Edge-Topologie, können Sie diese Ergebnisse verwenden, um die Edge-Server-Bereitstellung zu starten.</span><span class="sxs-lookup"><span data-stu-id="9d057-119">If you designed your edge topology during your planning process, including running Topology Builder to define your edge topology, you can use those results to start your Edge Server deployment.</span></span> <span data-ttu-id="9d057-120">Wenn Sie die Erstellung Ihrer Edge-Topologie zuvor nicht abgeschlossen haben oder die zuvor angegebenen Informationen ändern möchten, müssen Sie die Ausführung des Topologie-Generators beenden, bevor Sie mit anderen Bereitstellungsschritten fortfahren.</span><span class="sxs-lookup"><span data-stu-id="9d057-120">If you did not finish building your edge topology earlier or you want to change the information you previously specified, you must finish running Topology Builder before proceeding with other deployment steps.</span></span> <span data-ttu-id="9d057-121">Ausführliche Informationen zum Erstellen Ihrer Topologie finden Sie unter [Szenarien für den Zugriff durch externe Benutzer in lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="9d057-121">For details about how to build your topology, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span></span>

<span data-ttu-id="9d057-122">Details zum Planungs Tool und zum Topologie-Generator finden Sie unter [Starten des Planungsprozesses für lync Server 2013](lync-server-2013-beginning-the-planning-process.md) in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="9d057-122">For details about the Planning Tool and Topology Builder, see [Beginning the planning process for Lync Server 2013](lync-server-2013-beginning-the-planning-process.md) in the Planning documentation.</span></span>

<span data-ttu-id="9d057-123">Die folgende Tabelle enthält eine Übersicht über den Edge Server-Bereitstellungsprozess.</span><span class="sxs-lookup"><span data-stu-id="9d057-123">The following table provides an overview of the Edge Server deployment process.</span></span> <span data-ttu-id="9d057-124">Informationen zu den Planungsentscheidungen, die vor der Bereitstellung des Zugriffs auf externe Benutzer getroffen werden müssen, finden Sie unter [Szenarien für den Zugriff durch externe Benutzer in lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="9d057-124">To review the planning decisions that must be made before deploying external user access, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="9d057-125">Die Informationen in der folgenden Tabelle konzentrieren sich auf eine neue Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="9d057-125">The information in the following table focuses on a new deployment.</span></span> <span data-ttu-id="9d057-126">Wenn Sie Edgeserver in einer lync Server 2010, Office Communications Server 2007 R2 oder Office Communications Server 2007-Umgebung bereitgestellt haben, finden Sie Informationen zum Migrieren zu lync Server 2013 in der <A href="migration.md">Migration</A> .</span><span class="sxs-lookup"><span data-stu-id="9d057-126">If you have deployed Edge Servers in a Lync Server 2010, Office Communications Server 2007 R2 or Office Communications Server 2007 environment, see the <A href="migration.md">Migration</A> for details about migrating to Lync Server 2013.</span></span> <span data-ttu-id="9d057-127">Die Migration wird von keiner Version vor Office Communications Server 2007 R2 unterstützt, einschließlich Office Communications Server 2007, Live Communications Server 2005 und Live Communications Server 2003.</span><span class="sxs-lookup"><span data-stu-id="9d057-127">Migration is not supported from any version prior to Office Communications Server 2007 R2, including Office Communications Server 2007, Live Communications Server 2005, and Live Communications Server 2003.</span></span>



</div>

<span data-ttu-id="9d057-128">Zum Verbessern der Leistung und Sicherheit von Edge-Servern und zur Vereinfachung der Bereitstellung wenden Sie die folgenden bewährten Methoden an, wenn Sie das Umkreisnetzwerk und die Edgeserver bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="9d057-128">To enhance Edge Server performance and security, and to facilitate deployment, apply the following best practices when you deploy your perimeter network and Edge Servers:</span></span>

  - <span data-ttu-id="9d057-129">Stellen Sie Edgeserver erst bereit, nachdem Sie den Betrieb von lync Server 2013 in Ihrer Organisation getestet und überprüft haben.</span><span class="sxs-lookup"><span data-stu-id="9d057-129">Deploy Edge Servers only after you have tested and verified operation of Lync Server 2013 inside your organization.</span></span>

  - <span data-ttu-id="9d057-130">Es wird empfohlen, Edgeserver in einer Arbeitsgruppe statt in einer Domäne bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="9d057-130">We recommend that you deploy Edge Servers in a workgroup rather than a domain.</span></span> <span data-ttu-id="9d057-131">Dadurch wird die Installation vereinfacht, und Active Directory-Domänendienste (AD DS) sind außerhalb des Umkreisnetzwerks.</span><span class="sxs-lookup"><span data-stu-id="9d057-131">Doing so simplifies installation and keeps Active Directory Domain Services (AD DS) out of the perimeter network.</span></span> <span data-ttu-id="9d057-132">Das Auffinden von AD DS im Umkreisnetzwerk kann ein erhebliches Sicherheitsrisiko darstellen.</span><span class="sxs-lookup"><span data-stu-id="9d057-132">Locating AD DS in the perimeter network can present a significant security risk.</span></span>

  - <span data-ttu-id="9d057-133">Das beitreten zu einem Edgeserver zu einer Domäne, die sich vollständig im Umkreisnetzwerk befindet, wird unterstützt, aber nicht empfohlen.</span><span class="sxs-lookup"><span data-stu-id="9d057-133">Joining an Edge Server to a domain located entirely in the perimeter network is supported but not recommended.</span></span> <span data-ttu-id="9d057-134">Ein Edgeserver als Teil der internen Domäne verletzt vertrauenswürdige Netzwerkgrenzen, bei denen das Internet am wenigsten vertraut ist, Umkreisnetzwerk ist vertrauenswürdiger als das Internet, und das interne Netzwerk ist am vertrauenswürdigsten.</span><span class="sxs-lookup"><span data-stu-id="9d057-134">An Edge Server as part of the internal domain violates trusted network boundaries, where the Internet is least trusted, perimeter network is more trusted than the Internet, and the internal network is most trusted.</span></span> <span data-ttu-id="9d057-135">Ein Edgeserver als Mitglied der Domäne ist automatisch Teil des vertrauenswürdigsten Netzwerks, befindet sich aber in einem vertrauenswürdigen Netzwerk (dem Umkreis).</span><span class="sxs-lookup"><span data-stu-id="9d057-135">An Edge server as a member of the domain is automatically a part of the most trusted network, but resides in a less trusted network (the perimeter).</span></span>

<div>

## <a name="deployment-process-for-edge-servers"></a><span data-ttu-id="9d057-136">Bereitstellungsprozess für Edgeserver</span><span class="sxs-lookup"><span data-stu-id="9d057-136">Deployment Process for Edge Servers</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="9d057-137">Phase</span><span class="sxs-lookup"><span data-stu-id="9d057-137">Phase</span></span></th>
<th><span data-ttu-id="9d057-138">Schritte</span><span class="sxs-lookup"><span data-stu-id="9d057-138">Steps</span></span></th>
<th><span data-ttu-id="9d057-139">Berechtigungen</span><span class="sxs-lookup"><span data-stu-id="9d057-139">Permissions</span></span></th>
<th><span data-ttu-id="9d057-140">Dokumentation</span><span class="sxs-lookup"><span data-stu-id="9d057-140">Documentation</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="9d057-141">Erstellen Sie die geeignete Edge-Topologie, und ermitteln Sie die geeigneten Komponenten.</span><span class="sxs-lookup"><span data-stu-id="9d057-141">Create the appropriate edge topology and determine the appropriate components.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="9d057-142">Führen Sie den Topologie-Generator aus, um Edge-Servereinstellungen zu konfigurieren und die Topologie zu erstellen und zu veröffentlichen, und verwenden Sie dann die lync Server-Verwaltungsshell zum Exportieren der Topologie-Konfigurationsdatei.</span><span class="sxs-lookup"><span data-stu-id="9d057-142">Run Topology Builder to configure Edge Server settings and create and publish the topology, and then use Lync Server Management Shell to export the topology configuration file.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d057-143">Gruppe " <strong>Domänen-Admins</strong> " und " <strong>RTCUniversalServerAdmins</strong> " oder " <strong>CsAdmins</strong> "</span><span class="sxs-lookup"><span data-stu-id="9d057-143"><strong>Domain Admins</strong> group and <strong>RTCUniversalServerAdmins</strong> or <strong>CsAdmins</strong> group</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="9d057-144">Sie können eine Topologie mithilfe eines Kontos definieren, das ein Mitglied der lokalen Benutzergruppe ist, aber das Veröffentlichen einer Topologie erfordert ein Konto, das ein Mitglied der Gruppe der <STRONG>Domänenadministratoren</STRONG> und der <STRONG>RTCUniversalServerAdmins</STRONG> -Gruppe ist.</span><span class="sxs-lookup"><span data-stu-id="9d057-144">You can define a topology using an account that is a member of the local users group, but publishing a topology requires an account that is a member of the <STRONG>Domain Admins</STRONG> group and the <STRONG>RTCUniversalServerAdmins</STRONG> group.</span></span>


</div></td>
<td><p><span data-ttu-id="9d057-145"><a href="lync-server-2013-building-an-edge-and-director-topology.md">Erstellen einer Edge-und Director-Topologie in lync Server 2013</a> in der Bereitstellungsdokumentation</span><span class="sxs-lookup"><span data-stu-id="9d057-145"><a href="lync-server-2013-building-an-edge-and-director-topology.md">Building an edge and Director topology in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d057-146">Vorbereiten des Setups</span><span class="sxs-lookup"><span data-stu-id="9d057-146">Prepare for setup.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="9d057-147">Stellen Sie sicher, dass die Systemvoraussetzungen erfüllt sind.</span><span class="sxs-lookup"><span data-stu-id="9d057-147">Ensure that system prerequisites are met.</span></span></p></li>
<li><p><span data-ttu-id="9d057-148">Konfigurieren Sie IP-Adressen (bei Verwendung von IPv4 und IPv6) sowohl für interne als auch für öffentlich zugängliche Netzwerkschnittstellen auf jedem Edgeserver.</span><span class="sxs-lookup"><span data-stu-id="9d057-148">Configure IP addresses (IPv4 and IPv6, if used) for both internal and public facing network interfaces on each Edge Server.</span></span></p></li>
<li><p><span data-ttu-id="9d057-149">Konfigurieren Sie interne und externe DNS-Einträge (Host A und AAAA für IPv4 und IPv6), einschließlich der Konfiguration des DNS-Suffixes auf dem Computer, der als Edgeserver bereitgestellt werden soll.</span><span class="sxs-lookup"><span data-stu-id="9d057-149">Configure internal and external DNS records (host A and AAAA for IPv4 and IPv6), including configuring the DNS suffix on the computer to be deployed as an Edge Server.</span></span></p></li>
<li><p><span data-ttu-id="9d057-150">Optional Erstellen und installieren Sie öffentliche Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="9d057-150">(Optional) Create and install public certificates.</span></span> <span data-ttu-id="9d057-151">Die zum Abrufen von Zertifikaten erforderliche Zeit hängt davon ab, welche Zertifizierungsstelle das Zertifikat ausgibt.</span><span class="sxs-lookup"><span data-stu-id="9d057-151">The time required to obtain certificates depends on which certification authority (CA) issues the certificate.</span></span> <span data-ttu-id="9d057-152">Wenn Sie diesen Schritt an diesem Punkt nicht ausführen, müssen Sie dies während der Installation des Edge-Servers tun.</span><span class="sxs-lookup"><span data-stu-id="9d057-152">If you do not perform this step at this point, you must do it during Edge Server installation.</span></span> <span data-ttu-id="9d057-153">Die Edge-Server Dienste können erst gestartet werden, nachdem Zertifikate abgerufen und installiert wurden.</span><span class="sxs-lookup"><span data-stu-id="9d057-153">The Edge Server services cannot be started until certificates are obtained and installed.</span></span></p></li>
<li><p><span data-ttu-id="9d057-154">Bereitstellen von Unterstützung für öffentliche Chat Verbindungen, wenn Ihre Bereitstellung die Kommunikation mit Windows Live, AOL oder Yahoo! unterstützt</span><span class="sxs-lookup"><span data-stu-id="9d057-154">Provision support for public IM connectivity, if your deployment is to support communications with Windows Live, AOL, or Yahoo!</span></span> <span data-ttu-id="9d057-155">Benutzer.</span><span class="sxs-lookup"><span data-stu-id="9d057-155">users.</span></span></p>
<div>

> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="9d057-156">Ab dem 1. September, 2012, ist die Microsoft lync Public im Connectivity-Benutzerabonnementlizenz ("PIC USL") nicht mehr für den Kauf von neuen oder erneuernden Vereinbarungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="9d057-156">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="9d057-157">Kunden mit aktiven Lizenzen sind in der Lage, weiterhin mit Yahoo! zu verbünden</span><span class="sxs-lookup"><span data-stu-id="9d057-157">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="9d057-158">Messenger, bis der Dienst das Datum beendet hat.</span><span class="sxs-lookup"><span data-stu-id="9d057-158">Messenger until the service shut down date.</span></span> <span data-ttu-id="9d057-159">Datum des Endes des Lebenszyklus von Juni 2014 für AOL und Yahoo!</span><span class="sxs-lookup"><span data-stu-id="9d057-159">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="9d057-160">wurde angekündigt.</span><span class="sxs-lookup"><span data-stu-id="9d057-160">has been announced.</span></span> <span data-ttu-id="9d057-161">Ausführliche Informationen finden Sie <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">unter Unterstützung für öffentliche Instant Messenger-Konnektivität in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="9d057-161">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
> <LI>
> <P><span data-ttu-id="9d057-162">Bei der PIC-USL handelt es sich um eine Abonnementlizenz pro Benutzer pro Monat, die für die Föderation von lync Server oder Office Communications Server mit Yahoo! erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="9d057-162">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="9d057-163">Messenger.</span><span class="sxs-lookup"><span data-stu-id="9d057-163">Messenger.</span></span> <span data-ttu-id="9d057-164">Die Möglichkeit von Microsoft, diesen Dienst bereitzustellen, war von der Unterstützung durch Yahoo! abhängig, deren zugrunde liegende Vereinbarung abgewickelt wird.</span><span class="sxs-lookup"><span data-stu-id="9d057-164">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
> <LI>
> <P><span data-ttu-id="9d057-165">Lync ist mehr denn je ein leistungsfähiges Tool für die Verbindung zwischen Organisationen und Personen in der ganzen Welt.</span><span class="sxs-lookup"><span data-stu-id="9d057-165">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="9d057-166">Für den Verbund mit Windows Live Messenger sind keine zusätzlichen Benutzer-und Gerätelizenzen außerhalb der lync-Standard CAL erforderlich.</span><span class="sxs-lookup"><span data-stu-id="9d057-166">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="9d057-167">Skype Federation wird dieser Liste hinzugefügt und ermöglicht es lync-Benutzern, Hunderte von Millionen von Personen mit Chat und Sprache zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="9d057-167">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>


</div></li>
<li><p><span data-ttu-id="9d057-168">Bereitstellen von Unterstützung für die Unterstützung von XMPP und Verbund für Office Communications Server 2007, Office Communications Server 2007 R2, lync Server 2010-Partner, wenn diese von der Bereitstellung verwendet werden</span><span class="sxs-lookup"><span data-stu-id="9d057-168">Provision support for XMPP and federation support for Office Communications Server 2007, Office Communications Server 2007 R2, Lync Server 2010 partners, if your deployment will use these</span></span></p></li>
<li><p><span data-ttu-id="9d057-169">Konfigurieren Sie Firewalls.</span><span class="sxs-lookup"><span data-stu-id="9d057-169">Configure firewalls.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="9d057-170">Entsprechend Ihrer Organisation</span><span class="sxs-lookup"><span data-stu-id="9d057-170">As appropriate to your organization</span></span></p></td>
<td><p><span data-ttu-id="9d057-171"><a href="lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md">Vorbereiten der Installation von Servern im Umkreisnetzwerk für lync Server 2013</a> in der Bereitstellungsdokumentation</span><span class="sxs-lookup"><span data-stu-id="9d057-171"><a href="lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md">Preparing for installation of servers in the perimeter network for Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d057-172">Einrichten eines Reverse-Proxys</span><span class="sxs-lookup"><span data-stu-id="9d057-172">Set up reverse proxy.</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="9d057-173">Einrichten des Reverse Proxys (beispielsweise für Microsoft Forefront Threat Management Gateway 2010 oder Microsoft Internet Security and Acceleration (ISA) Server mit Service Pack 1) im Umkreisnetzwerk, besorgen Sie sich die erforderlichen öffentlichen Zertifikate, und konfigurieren Sie die Webveröffentlichungsregeln auf dem Reverse-Proxy Server.</span><span class="sxs-lookup"><span data-stu-id="9d057-173">Set up the reverse proxy (for example, for Microsoft Forefront Threat Management Gateway 2010 or Microsoft Internet Security and Acceleration (ISA) Server with Service Pack 1) in the perimeter network, obtain the necessary public certificates, and configure the web publishing rules on the reverse proxy server.</span></span></p>
<p><span data-ttu-id="9d057-174">Bereiten Sie den Reverseproxy für Mobilitätsdienste vor, wenn Sie für Mobilität geplant haben und die Mobilitätsdienste im Front-End-Pool oder Standard Edition-Server bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="9d057-174">Prepare the reverse proxy for Mobility services if you have planned for Mobility and are deploying the Mobility services on the Front End pool or Standard Edition server.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d057-175">Gruppe " <strong>Administratoren</strong> " oder Reverse-Proxy-Administrator</span><span class="sxs-lookup"><span data-stu-id="9d057-175"><strong>Administrators</strong> group or Reverse Proxy administrator</span></span></p></td>
<td><p><span data-ttu-id="9d057-176"><a href="lync-server-2013-setting-up-reverse-proxy-servers.md">Einrichten von Reverse-Proxyservern für lync Server 2013</a> in der Bereitstellungsdokumentation</span><span class="sxs-lookup"><span data-stu-id="9d057-176"><a href="lync-server-2013-setting-up-reverse-proxy-servers.md">Setting up reverse proxy servers for Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d057-177">Einrichten eines Directors (optional)</span><span class="sxs-lookup"><span data-stu-id="9d057-177">Setup a Director (optional).</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="9d057-178">Optional Installieren und konfigurieren Sie einen oder mehrere Directors im internen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="9d057-178">(Optional) Install and configure one or more Directors in the internal network.</span></span></p></li>
</ul></td>
<td><p><span data-ttu-id="9d057-179">Gruppe " <strong>Administratoren</strong> "</span><span class="sxs-lookup"><span data-stu-id="9d057-179"><strong>Administrators</strong> group</span></span></p></td>
<td><p><span data-ttu-id="9d057-180"><a href="lync-server-2013-setting-up-the-director.md">Einrichten des Directors in lync Server 2013</a> in der Bereitstellungsdokumentation</span><span class="sxs-lookup"><span data-stu-id="9d057-180"><a href="lync-server-2013-setting-up-the-director.md">Setting up the Director in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d057-181">Einrichten von Edgeserver</span><span class="sxs-lookup"><span data-stu-id="9d057-181">Set up Edge Servers.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="9d057-182">Installieren Sie die erforderliche Software.</span><span class="sxs-lookup"><span data-stu-id="9d057-182">Install prerequisite software.</span></span></p></li>
<li><p><span data-ttu-id="9d057-183">Transportieren Sie die exportierte Topologie-Konfigurationsdatei auf jeden Edgeserver.</span><span class="sxs-lookup"><span data-stu-id="9d057-183">Transport the exported topology configuration file to each Edge Server.</span></span></p></li>
<li><p><span data-ttu-id="9d057-184">Installieren Sie die lync Server 2013-Software auf jedem Edgeserver.</span><span class="sxs-lookup"><span data-stu-id="9d057-184">Install the Lync Server 2013 software on each Edge Server.</span></span></p></li>
<li><p><span data-ttu-id="9d057-185">Konfigurieren Sie die Edgeserver.</span><span class="sxs-lookup"><span data-stu-id="9d057-185">Configure the Edge Servers.</span></span></p></li>
<li><p><span data-ttu-id="9d057-186">Fordern Sie Zertifikate für jeden Edgeserver an, und installieren Sie Sie.</span><span class="sxs-lookup"><span data-stu-id="9d057-186">Request and install certificates for each Edge Server.</span></span></p></li>
<li><p><span data-ttu-id="9d057-187">Starten Sie die Edgeserver-Dienste.</span><span class="sxs-lookup"><span data-stu-id="9d057-187">Start the Edge Server services.</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="9d057-188">Gruppe " <strong>Administratoren</strong> "</span><span class="sxs-lookup"><span data-stu-id="9d057-188"><strong>Administrators</strong> group</span></span></p></td>
<td><p><span data-ttu-id="9d057-189"><a href="lync-server-2013-setting-up-edge-servers.md">Einrichten von Edgeserver in lync Server 2013</a> in der Bereitstellungsdokumentation</span><span class="sxs-lookup"><span data-stu-id="9d057-189"><a href="lync-server-2013-setting-up-edge-servers.md">Setting up Edge Servers in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="9d057-190">Konfigurieren Sie die Bereitstellung für den Zugriff durch externe Benutzer.</span><span class="sxs-lookup"><span data-stu-id="9d057-190">Configure deployment for external user access.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="9d057-191">Verwenden Sie die lync Server-Systemsteuerung, um die Unterstützung für jede der folgenden Optionen zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="9d057-191">Use the Lync Server Control Panel to configure support for each of the following (as applicable):</span></span></p>
<ul>
<li><p><span data-ttu-id="9d057-192">Medien Relay</span><span class="sxs-lookup"><span data-stu-id="9d057-192">Media relay</span></span></p></li>
<li><p><span data-ttu-id="9d057-193">Föderations Route</span><span class="sxs-lookup"><span data-stu-id="9d057-193">Federation route</span></span></p></li>
<li><p><span data-ttu-id="9d057-194">Zugriff durch Remote Benutzer</span><span class="sxs-lookup"><span data-stu-id="9d057-194">Remote user access</span></span></p></li>
<li><p><span data-ttu-id="9d057-195">Föderation mit lync Server, Office Communications Server und Live Communications Server</span><span class="sxs-lookup"><span data-stu-id="9d057-195">Federation with Lync Server, Office Communications Server and Live Communications Server</span></span></p></li>
<li><p><span data-ttu-id="9d057-196">Verbindung mit öffentlichen Chatdiensten</span><span class="sxs-lookup"><span data-stu-id="9d057-196">Public IM connectivity</span></span></p></li>
<li><p><span data-ttu-id="9d057-197">XMPP-Föderation</span><span class="sxs-lookup"><span data-stu-id="9d057-197">XMPP federation</span></span></p></li>
<li><p><span data-ttu-id="9d057-198">Anonyme Nutzer</span><span class="sxs-lookup"><span data-stu-id="9d057-198">Anonymous users</span></span></p></li>
</ul></li>
<li><p><span data-ttu-id="9d057-199">Konfigurieren von Benutzerkonten für Remotebenutzerzugriff, Föderation, öffentliche Chat Verbindungen, XMPP und anonyme Benutzerunterstützung (sofern zutreffend)</span><span class="sxs-lookup"><span data-stu-id="9d057-199">Configure user accounts for remote user access, federation, public IM connectivity, XMPP and anonymous user support (as applicable)</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="9d057-200"><strong>RTCUniversalServerAdmins</strong> -Gruppe oder ein Benutzerkonto, das der <strong>CSAdministrator</strong> -Rolle zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="9d057-200"><strong>RTCUniversalServerAdmins</strong> group or user account that is assigned to the <strong>CSAdministrator</strong> role</span></span></p></td>
<td><p><span data-ttu-id="9d057-201"><a href="lync-server-2013-configuring-support-for-external-user-access.md">Konfigurieren der Unterstützung für den Zugriff durch externe Benutzer in lync Server 2013</a> in der Bereitstellungsdokumentation</span><span class="sxs-lookup"><span data-stu-id="9d057-201"><a href="lync-server-2013-configuring-support-for-external-user-access.md">Configuring support for external user access in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="9d057-202">Überprüfen Sie Ihre Edge-Server-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="9d057-202">Verify your Edge Server configuration.</span></span></p></td>
<td><ol>
<li><p><span data-ttu-id="9d057-203">Überprüfen Sie die Serverkonnektivität und die Replikation von Konfigurationsdaten von internen Servern.</span><span class="sxs-lookup"><span data-stu-id="9d057-203">Verify server connectivity and replication of configuration data from internal servers.</span></span></p></li>
<li><p><span data-ttu-id="9d057-204">Stellen Sie sicher, dass externe Benutzer eine Verbindung herstellen können, einschließlich Remotebenutzern, Benutzern in Verbunddomänen, öffentlichen Chat Benutzern und anonymen Benutzern entsprechend Ihrer Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="9d057-204">Verify that external users can connect, including remote users, users in federated domains, public IM users, and anonymous users, as appropriate to your deployment.</span></span></p></li>
<li><p><span data-ttu-id="9d057-205">Überprüfen der Konfiguration und Kommunikation mithilfe der lync Server-Remote Verbindungsanalyse <a href="https://www.testocsconnectivity.com" class="uri">https://www.testocsconnectivity.com</a></span><span class="sxs-lookup"><span data-stu-id="9d057-205">Verify configuration and communication using the Lync Server Remote Connectivity Analyzer <a href="https://www.testocsconnectivity.com" class="uri">https://www.testocsconnectivity.com</a></span></span></p></li>
<li><p><span data-ttu-id="9d057-206">Problembehandlung bei Konfigurations-und Kommunikationsproblemen</span><span class="sxs-lookup"><span data-stu-id="9d057-206">Troubleshoot configuration and communication difficulties</span></span></p></li>
</ol></td>
<td><p><span data-ttu-id="9d057-207">Zur Überprüfung der Replikation, der <strong>RTCUniversalServerAdmins</strong> -Gruppe oder des Benutzerkontos, das der <strong>CSAdministrator</strong> -Rolle zugewiesen ist</span><span class="sxs-lookup"><span data-stu-id="9d057-207">For verification of replication, <strong>RTCUniversalServerAdmins</strong> group or user account that is assigned to the <strong>CSAdministrator</strong> role</span></span></p>
<p><span data-ttu-id="9d057-208">Zur Überprüfung der Benutzerkonnektivität wird ein Benutzer für jeden von Ihnen unterstützten Typ von Zugriff auf externe Benutzer</span><span class="sxs-lookup"><span data-stu-id="9d057-208">For verification of user connectivity, a user for each type of external user access that you support</span></span></p>
<p><span data-ttu-id="9d057-209">Remote Benutzer</span><span class="sxs-lookup"><span data-stu-id="9d057-209">Remote users</span></span></p></td>
<td><p><span data-ttu-id="9d057-210"><a href="lync-server-2013-verifying-your-edge-deployment.md">Überprüfen der Edge-Bereitstellung in lync Server 2013</a> in der Bereitstellungsdokumentation</span><span class="sxs-lookup"><span data-stu-id="9d057-210"><a href="lync-server-2013-verifying-your-edge-deployment.md">Verifying your edge deployment in Lync Server 2013</a> in the Deployment documentation</span></span></p></td>
</tr><span data-ttu-id="9d057-211">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9d057-211">
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

