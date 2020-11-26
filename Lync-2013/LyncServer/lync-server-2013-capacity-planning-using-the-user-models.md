---
title: Lync Server 2013-Kapazitätsplanung mit den Benutzermodellen
description: Lync Server 2013-Kapazitätsplanung mit den Benutzermodellen
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Capacity planning using the user models
ms:assetid: 902ab23e-94d6-482a-9d6e-c0b28dc3e03d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615015(v=OCS.15)
ms:contentKeyID: 49733733
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b710f7ec88dd75c872d704f2169fa2f161fc186
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435509"
---
# <a name="capacity-planning-for-lync-server-2013-using-the-user-models"></a><span data-ttu-id="a6116-103">Kapazitätsplanung für lync Server 2013 mit den Benutzermodellen</span><span class="sxs-lookup"><span data-stu-id="a6116-103">Capacity planning for Lync Server 2013 using the user models</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a6116-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a6116-104">

<span> </span></span></span>

<span data-ttu-id="a6116-105">_**Letztes Änderungsdatum des Themas:** 2014-01-14_</span><span class="sxs-lookup"><span data-stu-id="a6116-105">_**Topic Last Modified:** 2014-01-14_</span></span>

<span data-ttu-id="a6116-106">Dieser Abschnitt enthält Anleitungen dazu, wie viele Server Sie auf einer Website benötigen, um die Anzahl der Benutzer auf dieser Website entsprechend der in den [Benutzermodellen in lync Server 2013](lync-server-2013-user-models.md)beschriebenen Verwendung zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6116-106">This section provides guidance on how many servers you need at a site for the number of users at that site, according to the usage described in [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>

<div>

## <a name="tested-hardware-platform"></a><span data-ttu-id="a6116-107">Getestete Hardwareplattform</span><span class="sxs-lookup"><span data-stu-id="a6116-107">Tested Hardware Platform</span></span>

<span data-ttu-id="a6116-108">Alle Leistungsergebnisse und Bereitstellungsempfehlungen in diesem Abschnitt basieren auf Leistungstests auf Servern, auf denen die in der folgenden Tabelle beschriebene Hardware ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="a6116-108">All the performance results and deployment recommendations in this section are based on performance testing on servers running the hardware described in the following table.</span></span> <span data-ttu-id="a6116-109">Wir empfehlen, ähnliche Hardware zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6116-109">We recommend that you use similar hardware.</span></span> <span data-ttu-id="a6116-110">Wenn Sie weniger leistungsfähige Hardware verwenden, treten möglicherweise Funktionsprobleme oder eine schlechte Leistung auf.</span><span class="sxs-lookup"><span data-stu-id="a6116-110">If you use less powerful hardware, you may experience functionality problems or poor performance.</span></span> <span data-ttu-id="a6116-111">Beachten Sie, dass diese Hardwareempfehlungen höher als in früheren Versionen von lync Server sind.</span><span class="sxs-lookup"><span data-stu-id="a6116-111">Note that these hardware recommendations are higher than those of previous versions of Lync Server.</span></span>

### <a name="hardware-used-in-performance-testing"></a><span data-ttu-id="a6116-112">Bei Leistungstests eingesetzte Hardware</span><span class="sxs-lookup"><span data-stu-id="a6116-112">Hardware Used in Performance Testing</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6116-113">Hardwarekomponente</span><span class="sxs-lookup"><span data-stu-id="a6116-113">Hardware component</span></span></th>
<th><span data-ttu-id="a6116-114">Empfohlen</span><span class="sxs-lookup"><span data-stu-id="a6116-114">Recommended</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6116-115">CPU</span><span class="sxs-lookup"><span data-stu-id="a6116-115">CPU</span></span></p></td>
<td><p><span data-ttu-id="a6116-116">64-Bit-Dualprozessor, Sechskern, mindestens 2,26 GHz</span><span class="sxs-lookup"><span data-stu-id="a6116-116">64-bit dual processor, hex-core, 2.26 gigahertz (GHz) or higher</span></span></p>
<p><span data-ttu-id="a6116-117">Intel Itanium-Prozessoren werden für lync Server-Serverrollen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a6116-117">Intel Itanium processors are not supported for Lync Server server roles.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6116-118">Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="a6116-118">Memory</span></span></p></td>
<td><p><span data-ttu-id="a6116-119">32 GB</span><span class="sxs-lookup"><span data-stu-id="a6116-119">32 gigabytes (GB)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6116-120">Festplatte</span><span class="sxs-lookup"><span data-stu-id="a6116-120">Disk</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="a6116-121">8 oder mehr Festplatten mit 10.000 U/Min mit mindestens 72 GB freiem Speicher.</span><span class="sxs-lookup"><span data-stu-id="a6116-121">8 or more 10,000-RPM hard disk drives with at least 72 GB free disk space.</span></span></p>
<p><span data-ttu-id="a6116-122">Zwei Festplatten sollten RAID 1 verwenden und sechs Festplatten sollten RAID 10 verwenden.</span><span class="sxs-lookup"><span data-stu-id="a6116-122">Two of the disks should use RAID 1, and six should use RAID 10.</span></span></p>
<p><span data-ttu-id="a6116-123">- Oder</span><span class="sxs-lookup"><span data-stu-id="a6116-123">- OR -</span></span></p></li>
<li><p><span data-ttu-id="a6116-124">Festkörperlaufwerke (SSDs) mit einer ähnlichen Leistung wie 8 mechanische Festplattenlaufwerke mit 10.000 U/min.</span><span class="sxs-lookup"><span data-stu-id="a6116-124">Solid state drives (SSDs) which provide performance similar to 8 10,000-RPM mechanical disk drives.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6116-125">Netzwerk</span><span class="sxs-lookup"><span data-stu-id="a6116-125">Network</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="a6116-126">1 Dual-Port-Netzwerkadapter, mindestens 1 GBit/s (2 werden empfohlen, wofür die Verknüpfung mit einer einzelnen MAC-Adresse und einer einzelnen IP-Adresse erforderlich ist)</span><span class="sxs-lookup"><span data-stu-id="a6116-126">1 dual-port network adapter, 1 Gbps or higher (2 recommended, which requires teaming with a single MAC address and single IP address)</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="summary-of-results"></a><span data-ttu-id="a6116-127">Zusammenfassung der Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="a6116-127">Summary of Results</span></span>

<span data-ttu-id="a6116-128">In der folgenden Tabelle werden diese Empfehlungen zusammengefasst.</span><span class="sxs-lookup"><span data-stu-id="a6116-128">The following table summarizes these recommendations.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6116-129">Serverrolle</span><span class="sxs-lookup"><span data-stu-id="a6116-129">Server role</span></span></th>
<th><span data-ttu-id="a6116-130">Maximale Anzahl von unterstützten Benutzern</span><span class="sxs-lookup"><span data-stu-id="a6116-130">Maximum number of users supported</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6116-131">Front-End-Pool mit zwölf Front-End-Servern und einem Back-End-Server oder einem gespiegelten Paar von Back-End-Servern.</span><span class="sxs-lookup"><span data-stu-id="a6116-131">Front End pool with twelve Front End Servers and one Back End Server or a mirrored pair of Back End Servers.</span></span></p></td>
<td><p><span data-ttu-id="a6116-132">80.000 eindeutige Benutzer, plus 50 % Anmeldungen auf mehreren Geräten (Multiple Point Of Presence, MPOP), die keine mobilen Instanzen sind, plus 40 % Benutzer, die für Mobilität aktiviert sind, für insgesamt 152.000 Endpunkte.</span><span class="sxs-lookup"><span data-stu-id="a6116-132">80,000 unique users simultaneously logged in, plus 50% multiple points of presence (MPOP) representing non-mobile instances, plus 40% of users enabled for Mobility for a total of 152,000 endpoints.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6116-133">A/V-Konferenzen</span><span class="sxs-lookup"><span data-stu-id="a6116-133">A/V Conferencing</span></span></p></td>
<td><p><span data-ttu-id="a6116-134">Der a/V-Konferenzdienst, der von einem Front-End-Pool bereitgestellt wird, unterstützt die Konferenzen des Pools, vorausgesetzt, es wird eine maximale Konferenzgröße von 250-Benutzern und nur eine solche große Konferenz gleichzeitig ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6116-134">The A/V Conferencing service provided by a Front End pool supports the pool’s conferences assuming a maximum conference size of 250 users, and only one such large conference running at a time.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="a6116-135">Darüber hinaus können Sie große Konferenzen zwischen 250-und 1000-Benutzern unterstützen, indem Sie einen separaten Front-End-Pool mit zwei Front-End-Servern bereitstellen, um die umfangreichen Konferenzen zu hosten.</span><span class="sxs-lookup"><span data-stu-id="a6116-135">Additionally, you can support large conferences of between 250 and 1000 users by deploying a separate Front End pool with two Front End Servers to host the large conferences.</span></span> <span data-ttu-id="a6116-136">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-supporting-large-meetings.md">unterstützen von umfangreichen Besprechungen mit lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="a6116-136">For details, see <A href="lync-server-2013-supporting-large-meetings.md">Supporting large meetings using Lync Server 2013</A>.</span></span>


</div></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6116-137">Ein Edgeserver</span><span class="sxs-lookup"><span data-stu-id="a6116-137">One Edge Server</span></span></p></td>
<td><p><span data-ttu-id="a6116-138">12.000 Concurrent Remote-Benutzer</span><span class="sxs-lookup"><span data-stu-id="a6116-138">12,000 concurrent remote users</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6116-139">Ein Direktor</span><span class="sxs-lookup"><span data-stu-id="a6116-139">One Director</span></span></p></td>
<td><p><span data-ttu-id="a6116-140">12.000 Concurrent Remote-Benutzer</span><span class="sxs-lookup"><span data-stu-id="a6116-140">12,000 concurrent remote users</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6116-141">Überwachen und Archivieren</span><span class="sxs-lookup"><span data-stu-id="a6116-141">Monitoring and Archiving</span></span></p></td>
<td><p><span data-ttu-id="a6116-142">In lync Server 2013 werden die Front-End-Dienste für die Überwachung und Archivierung nun auf jedem Front-End-Server und nicht auf separaten Server Rollen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6116-142">In Lync Server 2013, the Monitoring and Archiving front end services now run on each Front End Server, instead of on separate server roles.</span></span></p>
<p><span data-ttu-id="a6116-143">Für das Überwachen und Archivieren sind weiterhin eigene Datenbankspeicher erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a6116-143">Monitoring and Archiving each still require their own database stores.</span></span> <span data-ttu-id="a6116-144">Wenn Sie auch Exchange 2013 ausführen, können Sie Ihre Archivierungsdaten in Exchange und nicht in einer dedizierten SQL-Datenbank speichern.</span><span class="sxs-lookup"><span data-stu-id="a6116-144">If you also run Exchange 2013, you can keep your Archiving data in Exchange, rather than in a dedicated SQL database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6116-145">Ein Vermittlungs Server</span><span class="sxs-lookup"><span data-stu-id="a6116-145">One Mediation Server</span></span></p></td>
<td><p><span data-ttu-id="a6116-146">Der mit dem Front-End-Server zusammenhängende Vermittlungsserver wird auf jedem Front-End-Server in einem Pool ausgeführt und sollte genügend Kapazität für die Benutzer im Pool bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a6116-146">Mediation Server collocated with Front End Server runs on every Front End Server in a pool, and should provide enough capacity for the users in the pool.</span></span> <span data-ttu-id="a6116-147">Informationen zum eigenständigen Vermittlungsserver finden Sie im Abschnitt "Mediation Server" weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="a6116-147">For stand-alone Mediation Server, see the “Mediation Server” section later in this topic.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6116-148">Ein Standard Edition-Server</span><span class="sxs-lookup"><span data-stu-id="a6116-148">One Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="a6116-149">Wir empfehlen dringend, dass Sie bei der Verwendung von Standard Edition-Servern zum Hosten von Benutzern immer zwei Server verwenden, die mit den Empfehlungen <a href="lync-server-2013-planning-for-high-availability-and-disaster-recovery.md">für die Planung von höchst Verfügbarkeit und Disaster Recovery in lync Server 2013</a>kombiniert werden.</span><span class="sxs-lookup"><span data-stu-id="a6116-149">We strongly recommend that if you use Standard Edition servers to host users, you always use two servers, paired using the recommendations in <a href="lync-server-2013-planning-for-high-availability-and-disaster-recovery.md">Planning for high availability and disaster recovery in Lync Server 2013</a>.</span></span> <span data-ttu-id="a6116-150">Jeder Server der Kombination kann bis zu 2.500 Benutzer hosten und wenn ein Server ausfällt, kann der verbleibende Server in einem Failoverszenario 5.000 Benutzer unterstützen.</span><span class="sxs-lookup"><span data-stu-id="a6116-150">Each server in the pair can host up to 2,500 users, and if one server fails the remaining server can support 5,000 users in a failover scenario.</span></span></p>
<p><span data-ttu-id="a6116-151">Wenn in Ihrer Bereitstellung Audio- oder Videodatenverkehr im großen Umfang anfällt, wird die Serverleistung u. U. auch bei mehr als 2.500 Benutzern pro Server beeinträchtigt.</span><span class="sxs-lookup"><span data-stu-id="a6116-151">If your deployment includes a significant amount of audio or video traffic, server performance may suffer with more than 2,500 users per server.</span></span> <span data-ttu-id="a6116-152">In diesem Fall sollten Sie das Hinzufügen weiterer Standard Edition-Server oder die Umstellung auf lync Server Enterprise Edition in Frage stellen.</span><span class="sxs-lookup"><span data-stu-id="a6116-152">In this case, you should consider adding more Standard Edition servers or moving to Lync Server Enterprise Edition.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="front-end-server"></a><span data-ttu-id="a6116-153">Front-End-Server</span><span class="sxs-lookup"><span data-stu-id="a6116-153">Front End Server</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a6116-154">Gestreckte Pools werden für diese Serverrolle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a6116-154">Stretched pools are not supported for this server role.</span></span>



</div>

<span data-ttu-id="a6116-155">In einem Front-End-Pool sollten Sie über einen Front-End-Server für alle 6.660-Benutzer verfügen, die im Pool verwaltet werden, vorausgesetzt, dass Hyper-Threading auf allen Servern im Pool aktiviert ist und dass die Server Hardware die Empfehlungen in [Server Hardwareplattformen für lync Server 2013](lync-server-2013-server-hardware-platforms.md)erfüllt.</span><span class="sxs-lookup"><span data-stu-id="a6116-155">In a Front End pool, you should have one Front End Server for every 6,660 users homed in the pool, assuming that hyper-threading is enabled on all servers in the pool, and that the server hardware meets the recommendations in [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span></span> <span data-ttu-id="a6116-156">Die maximale Anzahl von Benutzern in einem Front-End-Pool ist 80.000, vorausgesetzt, Hyper-Threading ist auf allen Servern im Pool aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a6116-156">The maximum number of users in one Front End pool is 80,000, assuming that hyper-threading is enabled on all the servers in the pool.</span></span> <span data-ttu-id="a6116-157">Wenn Sie über mehr als 80.000 Benutzer an einer Website verfügen, können Sie mehr als einen Front-End-Pool bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a6116-157">If you have more than 80,000 users at a site, you can deploy more than one Front End pool.</span></span>

<span data-ttu-id="a6116-158">Wenn Sie die Anzahl der Benutzer in einem Front-End-Pool berücksichtigen, schließen Sie die Benutzer, die sich auf überlebensfähigen Zweig-Appliances und überlebensfähigen Verzweigungs Servern befinden, in Zweigniederlassungen ein, die diesem Front-End-Pool zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a6116-158">When you account for the number of users in a Front End pool, include the users homed on Survivable Branch Appliances and Survivable Branch Servers at branch offices that are associated with this Front End pool.</span></span>

<span data-ttu-id="a6116-159">Wenn ein aktiver Server nicht mehr verfügbar ist, werden seine Verbindungen automatisch an die anderen Server innerhalb des Pools übertragen.</span><span class="sxs-lookup"><span data-stu-id="a6116-159">When an active server is unavailable, its connections are transferred automatically to the other servers in the pool.</span></span> <span data-ttu-id="a6116-160">Wenn Sie beispielsweise 30.000-Benutzer und fünf Front-End-Server haben, müssen die Verbindungen von 6000-Benutzern auf die anderen vier Server übertragen werden, wenn ein Server nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a6116-160">For example, if you have 30,000 users and five Front End Servers, then if one server is unavailable, the connections of 6000 users need to be transferred to the other four servers.</span></span> <span data-ttu-id="a6116-161">Die restlichen vier Server verfügen jeweils über 7500-Benutzer, was eine größere Zahl als empfohlen ist.</span><span class="sxs-lookup"><span data-stu-id="a6116-161">The remaining four servers will each have 7500 users, which is a larger number than recommended.</span></span>

<span data-ttu-id="a6116-162">Wenn Sie stattdessen mit sechs Front-End-Servern für ihre 30.000-Benutzer begonnen haben und diese dann nicht mehr zur Verfügung stehen, werden insgesamt 5000-Benutzer auf die restlichen fünf Server verschoben.</span><span class="sxs-lookup"><span data-stu-id="a6116-162">If instead you had started with six Front End Servers for your 30,000 users and subsequently one became unavailable, a total of 5000 users will be moved to the remaining five servers.</span></span> <span data-ttu-id="a6116-163">Diese fünf Server sind für jeden Host 6000-Benutzer, der sich im empfohlenen Bereich befindet.</span><span class="sxs-lookup"><span data-stu-id="a6116-163">These five servers will each host 6000 users, which is in the recommended range.</span></span>

<span data-ttu-id="a6116-164">Die maximale Anzahl von Benutzern in einem Front-End-Pool ist 80.000.</span><span class="sxs-lookup"><span data-stu-id="a6116-164">The maximum number of users in a Front End pool is 80,000.</span></span> <span data-ttu-id="a6116-165">Die maximale Anzahl der Front-End-Server in einem Pool beträgt 12.</span><span class="sxs-lookup"><span data-stu-id="a6116-165">The maximum number of Front End Servers in a pool is 12.</span></span>

<span data-ttu-id="a6116-166">Bei einem Front-End-Pool mit 80.000-Benutzern genügen zwölf Front-End-Server für die Leistung in typischen Bereitstellungen, die den [Benutzermodellen in lync Server 2013](lync-server-2013-user-models.md)entsprechen.</span><span class="sxs-lookup"><span data-stu-id="a6116-166">For a Front End pool with 80,000 users, twelve Front End Servers is sufficient for performance, in typical deployments that follow the [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span> <span data-ttu-id="a6116-167">Für Bereitstellungen zur Unterstützung von Disaster Recovery-Failover wird davon ausgegangen, dass maximal 40.000-Benutzer in jedem von zwei gekoppelten Front-End-Pools gehostet werden können, in denen jeder Pool über genügend Front-End-Server verfügt, um die Benutzer in beiden Pools aufnehmen zu können, wenn ein Pool Failover auf den anderen durchgeführt werden muss.</span><span class="sxs-lookup"><span data-stu-id="a6116-167">Deployments designed to support disaster recovery failover assume that a maximum of 40,000 users can be hosted in each of two paired Front End pools, in which each pool has enough Front End Servers to accommodate the users in both pools should one pool need to be failed over to the other.</span></span>

<span data-ttu-id="a6116-168">Die Anzahl der Benutzer, die mit einer guten Leistung von einem bestimmten Front-End-Pool unterstützt werden, kann aus folgenden Gründen von diesen Zahlen abweichen:</span><span class="sxs-lookup"><span data-stu-id="a6116-168">The number of users supported with good performance by a particular Front End pool may differ from these numbers for the following reasons:</span></span>

  - <span data-ttu-id="a6116-169">Die Hardware für Ihre Front-End-Server entspricht nicht den Empfehlungen in [Server Hardwareplattformen für lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span><span class="sxs-lookup"><span data-stu-id="a6116-169">The hardware for your Front End Servers does not meet the recommendations in [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span></span>

  - <span data-ttu-id="a6116-170">Die Nutzung Ihrer Organisation weicht erheblich von den Benutzermodellen ab, wie etwa erheblich mehr Konferenzdatenverkehr.</span><span class="sxs-lookup"><span data-stu-id="a6116-170">Your organization’s usage differs significantly from the user models, such as significantly more conferencing traffic.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="a6116-171">In lync Server 2013 werden die Anwesenheits Datenbanken nun auf Front-End-Servern gehostet, anders als in lync Server 2010, auf dem Sie auf dem Back-End-Server gehostet wurden.</span><span class="sxs-lookup"><span data-stu-id="a6116-171">In Lync Server 2013, the presence databases are now hosted on Front End Servers, unlike in Lync Server 2010 where they were hosted on the Back End Server.</span></span> <span data-ttu-id="a6116-172">Das bedeutet, dass die Datenträgerleistung und-Kapazität Ihrer Front-End-Server nicht von den weiter oben in diesem Abschnitt und auf <A href="lync-server-2013-server-hardware-platforms.md">Server Hardwareplattformen für lync Server 2013</A>aufgeführten Empfehlungen beeinträchtigt werden sollten, unabhängig von der Anzahl der Benutzer, die von ihren Front-End-Servern gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="a6116-172">This means that the disk performance and capacity of your Front End Servers should not be compromised from the recommendations listed earlier in this section and in <A href="lync-server-2013-server-hardware-platforms.md">Server hardware platforms for Lync Server 2013</A>, regardless of the number of users hosted by your Front End Servers.</span></span>



</div>

<span data-ttu-id="a6116-173">In der folgenden Tabelle ist die durchschnittliche Bandbreite für Chat und Anwesenheitsinformationen anhand des Benutzermodells dargestellt, wie es in [Benutzermodellen in lync Server 2013](lync-server-2013-user-models.md)definiert ist.</span><span class="sxs-lookup"><span data-stu-id="a6116-173">The following table shows the average bandwidth for IM and presence, given the user model, as defined in [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6116-174">Durchschnittliche Bandbreite pro Benutzer</span><span class="sxs-lookup"><span data-stu-id="a6116-174">Average bandwidth per user</span></span></th>
<th><span data-ttu-id="a6116-175">Bandbreitenanforderungen pro Front-End-Server mit 6.660-Benutzern</span><span class="sxs-lookup"><span data-stu-id="a6116-175">Bandwidth requirements per Front End Server with 6,660 users</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6116-176">1,3 KBit/s</span><span class="sxs-lookup"><span data-stu-id="a6116-176">1.3 Kpbs</span></span></p></td>
<td><p><span data-ttu-id="a6116-177">13 MBit/s</span><span class="sxs-lookup"><span data-stu-id="a6116-177">13 Mbps</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="a6116-178">Wenn Sie die Medien Leistung der co-located A/V-Konferenz-und Vermittlungs Server Funktionalität auf Ihren Front-End-Servern verbessern möchten, sollten Sie auf den Netzwerkadaptern auf Ihren Front-End-Servern die Receive-Side-Skalierung (RSS) aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6116-178">To improve the media performance of the co-located A/V Conferencing and Mediation Server functionality on your Front End Servers, you should enable receive-side scaling (RSS) on the network adapters on your Front End Servers.</span></span> <span data-ttu-id="a6116-179">Mit RSS können eingehende Pakete gleichzeitig von mehreren Prozessoren auf dem Server verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a6116-179">RSS enables incoming packets to be handled in parallel by multiple processors on the server.</span></span> <span data-ttu-id="a6116-180">Ausführliche Informationen finden Sie unter "Verbesserungen bei der Empfangs seitigen Skalierung in Windows Server 2008" <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?linkId=268731</A> .</span><span class="sxs-lookup"><span data-stu-id="a6116-180">For details, see "Receive-Side Scaling Enhancements in Windows Server 2008" at <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?linkId=268731</A>.</span></span> <span data-ttu-id="a6116-181">Weitere Informationen zum Aktivieren von RSS finden Sie in der Dokumentation zu Ihrem Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="a6116-181">For details about how to enable RSS, see your network adapter documentation.</span></span>



</div>

</div>

<div>

## <a name="conferencing-maximums"></a><span data-ttu-id="a6116-182">Maximale Anzahl von Benutzern für Konferenzen</span><span class="sxs-lookup"><span data-stu-id="a6116-182">Conferencing Maximums</span></span>

<span data-ttu-id="a6116-183">Angesichts des Benutzermodells, dass sich 5% der Benutzer in einem Pool zu einem beliebigen Zeitpunkt in einer Konferenz befinden können, kann ein Pool von 80.000-Benutzern gleichzeitig über 4.000-Benutzer in Konferenzen verfügen.</span><span class="sxs-lookup"><span data-stu-id="a6116-183">Given the user model that 5% of users in a pool may be in a conference at any one time, a pool of 80,000 users could have about 4,000 users in conferences at one time.</span></span> <span data-ttu-id="a6116-184">Bei diesen Konferenzen wird davon ausgegangen, dass eine Kombination aus Mediendatenverkehr (z. B. nur Chatnachrichten, Chatnachrichten mit Audio, Audio/Video-Konferenzen) verarbeitet werden muss und eine unterschiedliche Anzahl von Benutzern teilnimmt.</span><span class="sxs-lookup"><span data-stu-id="a6116-184">These conferences are expected to be a mix of media (some IM-only, some IM with audio, some audio/video, for example) and number of participants.</span></span> <span data-ttu-id="a6116-185">Es gibt keine harte Grenze für die tatsächliche Anzahl der zulässigen Konferenzen, und die tatsächliche Nutzung bestimmt die tatsächliche Leistung.</span><span class="sxs-lookup"><span data-stu-id="a6116-185">There is no hard limit for the actual number of conferences allowed, and actual usage determines the actual performance.</span></span> <span data-ttu-id="a6116-186">Wenn Ihre Organisation beispielsweise über viele weitere Konferenzen im gemischten Modus verfügt, als im Benutzermodell angenommen wird, müssen Sie möglicherweise mehr Front-End-Server oder A/V-Konferenzserver bereitstellen als die Empfehlungen in diesem Dokument.</span><span class="sxs-lookup"><span data-stu-id="a6116-186">For example, if your organization has many more mixed-mode conferences than are assumed in the user model, you might need to deploy more Front End Servers or A/V Conferencing Servers than the recommendations in this document.</span></span> <span data-ttu-id="a6116-187">Details zu den Annahmen im Benutzermodell finden Sie unter [Benutzermodelle in lync Server 2013](lync-server-2013-user-models.md).</span><span class="sxs-lookup"><span data-stu-id="a6116-187">For details about the assumptions in the user model, see [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>

<span data-ttu-id="a6116-188">Die maximale unterstützte Konferenzgröße, die von einem regulären lync Server 2013-Front-End-Pool gehostet wird, der auch Benutzer hostet, ist 250 Teilnehmer.</span><span class="sxs-lookup"><span data-stu-id="a6116-188">The maximum supported conference size hosted by a regular Lync Server 2013 Front End pool which also hosts users is 250 participants.</span></span> <span data-ttu-id="a6116-189">Während eine 250-Benutzer Konferenz stattfindet, unterstützt der Pool weiterhin auch andere Konferenzen, sodass sich insgesamt 5% der Pool Benutzer in parallelen Konferenzen befinden.</span><span class="sxs-lookup"><span data-stu-id="a6116-189">While a 250-user conference is happening, the pool still supports other conferences as well, such that a total of 5% of pool users are in concurrent conferences.</span></span> <span data-ttu-id="a6116-190">Beispielsweise unterstützt lync Server in einem Pool von zwölf Front-End-Servern und 80.000-Benutzern, während die 250-Benutzer Konferenz stattfindet, 3.750 anderen Benutzern, die an kleineren Konferenzen teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="a6116-190">For example, in a pool of twelve Front End Servers and 80,000 users, while the 250-user conference is happening, Lync Server supports 3,750 other users participating in smaller conferences.</span></span>

<span data-ttu-id="a6116-191">Unabhängig von der Anzahl der Benutzer, die sich auf dem Front-End-Pool oder dem Standard Edition-Server befinden, unterstützt lync Server mindestens 125 anderen Benutzern, die an kleineren Konferenzen am gleichen Pool oder Server teilnehmen, der eine Konferenz mit 250-Benutzern hostet.</span><span class="sxs-lookup"><span data-stu-id="a6116-191">Regardless of the number of users homed on the Front End pool or Standard Edition server, Lync Server supports a minimum of 125 other users participating in smaller conferences on the same pool or server which is hosting a 250-user conference.</span></span>

<span data-ttu-id="a6116-192">Zum Aktivieren von Konferenzen mit zwischen 250-und 1000-Benutzern können Sie einen separaten Front-End-Pool einrichten, um diese Konferenzen zu hosten.</span><span class="sxs-lookup"><span data-stu-id="a6116-192">To enable conferences with between 250 and 1000 users, you can set up a separate Front End pool just to host those conferences.</span></span> <span data-ttu-id="a6116-193">In diesem Front-End-Pool werden keine Benutzer gehostet.</span><span class="sxs-lookup"><span data-stu-id="a6116-193">This Front End pool will not host any users.</span></span> <span data-ttu-id="a6116-194">Ausführliche Informationen finden Sie unter [unterstützen von umfangreichen Besprechungen mit lync Server 2013](lync-server-2013-supporting-large-meetings.md).</span><span class="sxs-lookup"><span data-stu-id="a6116-194">For details, see [Supporting large meetings using Lync Server 2013](lync-server-2013-supporting-large-meetings.md).</span></span>

<span data-ttu-id="a6116-195">Wenn in Ihrer Organisation viele weitere Konferenzen im gemischten Modus stattfinden, die im Benutzermodell angenommen werden, müssen Sie möglicherweise mehr Front-End-Server als die Empfehlungen in diesem Dokument bereitstellen (bis zu einem Grenzwert von 12 Fes).</span><span class="sxs-lookup"><span data-stu-id="a6116-195">If your organization has many more mixed-mode conferences than are assumed in the user model, you might need to deploy more Front End Servers than the recommendations in this document (up to a limit of 12 FEs).</span></span> <span data-ttu-id="a6116-196">Details zu den Annahmen im Benutzermodell finden Sie unter [Benutzermodelle in lync Server 2013](lync-server-2013-user-models.md).</span><span class="sxs-lookup"><span data-stu-id="a6116-196">For details about the assumptions in the user model, see [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>

</div>

<div>

## <a name="edge-server"></a><span data-ttu-id="a6116-197">Edgeserver</span><span class="sxs-lookup"><span data-stu-id="a6116-197">Edge Server</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a6116-198">Gestreckte Pools werden für diese Serverrolle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a6116-198">Stretched pools are not supported for this server role.</span></span>



</div>

<span data-ttu-id="a6116-199">Sie sollten einen Edgeserver für alle 12.000-Remotebenutzer bereitstellen, die gleichzeitig auf eine Website zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a6116-199">You should deploy one Edge Server for every 12,000 remote users who will access a site concurrently.</span></span> <span data-ttu-id="a6116-200">Wir empfehlen mindestens zwei Edge-Server für eine höhere Verfügbarkeit.</span><span class="sxs-lookup"><span data-stu-id="a6116-200">At a minimum we recommend two Edge Servers for high availability.</span></span> <span data-ttu-id="a6116-201">Bei diesen Empfehlungen wird davon ausgegangen, dass die Hardware für Ihre Edgeserver die Empfehlungen in [Server Hardwareplattformen für lync Server 2013](lync-server-2013-server-hardware-platforms.md)erfüllt.</span><span class="sxs-lookup"><span data-stu-id="a6116-201">These recommendations assume that the hardware for your Edge Servers meets the recommendations in [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span></span>

<span data-ttu-id="a6116-202">Wenn Sie die Anzahl der Benutzer für die Edgeserver berücksichtigen, schließen Sie die Benutzer, die sich auf Survivable Branch Appliances und überlebensfähige Verzweigungs Server befinden, in Zweigniederlassungen ein, die einem Front-End-Pool an diesem Standort zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a6116-202">When you account for the number of users for the Edge Servers, include the users homed on Survivable Branch Appliances and Survivable Branch Servers at branch offices that are associated with a Front End pool at this site.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a6116-203">Wenn Sie die Leistung des A/V-Konferenz-Edgedienst auf Ihren Edge-Servern verbessern möchten, sollten Sie auf den Netzwerkadaptern auf Ihren Edge-Servern die Receive-Side-Skalierung (RSS) aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6116-203">To improve the performance of the A/V Conferencing Edge service on your Edge Servers, you should enable receive-side scaling (RSS) on the network adapters on your Edge Servers.</span></span> <span data-ttu-id="a6116-204">Mit RSS können eingehende Pakete gleichzeitig von mehreren Prozessoren auf dem Server verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a6116-204">RSS enables incoming packets to be handled in parallel by multiple processors on the server.</span></span> <span data-ttu-id="a6116-205">Ausführliche Informationen finden Sie unter "Verbesserungen bei der Empfangs seitigen Skalierung in Windows Server 2008" <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?linkId=268731</A> .</span><span class="sxs-lookup"><span data-stu-id="a6116-205">For details, see "Receive-Side Scaling Enhancements in Windows Server 2008" at <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?linkId=268731</A>.</span></span> <span data-ttu-id="a6116-206">Weitere Informationen zum Aktivieren von RSS finden Sie in der Dokumentation zu Ihrem Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="a6116-206">For details about how to enable RSS, see your network adapter documentation.</span></span>



</div>

</div>

<div>

## <a name="director"></a><span data-ttu-id="a6116-207">Director</span><span class="sxs-lookup"><span data-stu-id="a6116-207">Director</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a6116-208">Gestreckte Pools werden für diese Serverrolle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a6116-208">Stretched pools are not supported for this server role.</span></span>



</div>

<span data-ttu-id="a6116-209">Wenn Sie die Director-Serverrolle bereitstellen, empfehlen wir, dass Sie einen Director für alle 12.000-Remotebenutzer bereitstellen, die gleichzeitig auf eine Website zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a6116-209">If you deploy the Director server role we recommend that you deploy one Director for every 12,000 remote users who will access a site concurrently.</span></span> <span data-ttu-id="a6116-210">Wir empfehlen mindestens zwei Directors für höchste Verfügbarkeit.</span><span class="sxs-lookup"><span data-stu-id="a6116-210">At a minimum we recommend two Directors for high availability.</span></span> <span data-ttu-id="a6116-211">Bei diesen Empfehlungen wird davon ausgegangen, dass die Hardware für Ihre Edgeserver die Empfehlungen in [Server Hardwareplattformen für lync Server 2013](lync-server-2013-server-hardware-platforms.md)erfüllt.</span><span class="sxs-lookup"><span data-stu-id="a6116-211">These recommendations assume that the hardware for your Edge Servers meets the recommendations in [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span></span>

<span data-ttu-id="a6116-212">Wenn Sie die Anzahl der Benutzer für die Directors berücksichtigen, fügen Sie die Benutzer, die sich auf Survival Branch-Appliances und überlebensfähige Branch-Server befinden, in Zweigniederlassungen ein, die einem Front-End-Pool an diesem Standort zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="a6116-212">When you account for the number of users for the Directors, include the users homed on Survivable Branch Appliances and Survivable Branch Servers at branch offices that are associated with a Front End pool at this site.</span></span>

</div>

<div>

## <a name="mediation-server"></a><span data-ttu-id="a6116-213">Vermittlungsserver</span><span class="sxs-lookup"><span data-stu-id="a6116-213">Mediation Server</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a6116-214">Gestreckte Pools werden für diese Serverrolle nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="a6116-214">Stretched pools are not supported for this server role.</span></span>



</div>

<span data-ttu-id="a6116-215">Wenn Sie den Vermittlungsserver mit dem Front-End-Server collocate, wird der Mediation Server auf jedem Front-End-Server im Pool ausgeführt und sollte genügend Kapazität für die Benutzer im Pool bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="a6116-215">If you collocate Mediation Server with Front End Server, Mediation Server runs on every Front End Server in the pool, and should provide enough capacity for the users in the pool.</span></span>

<span data-ttu-id="a6116-216">Wenn Sie einen eigenständigen vermittlungsserverpool bereitstellen, hängt die Anzahl der bereitzustellenden Vermittlungsserver von vielen Faktoren ab, einschließlich der für den Vermittlungsserver verwendeten Hardware, der Anzahl der VoIP-Benutzer, der Anzahl der Gateway-Peers, die von jedem vermittlungsserverpool gesteuert werden, vom auslastungsstunden-Datenverkehr über diese Gateways und dem Prozentsatz der Anrufe mit</span><span class="sxs-lookup"><span data-stu-id="a6116-216">If you deploy a stand-alone Mediation Server pool, then how many Mediation Servers to deploy depends on many factors, including the hardware used for Mediation Server, the number of VoIP users you have, the number of gateway peers that each Mediation Server pool controls, the busy hour traffic through those gateways, and the percentage of calls with media that bypasses the Mediation Server.</span></span>

<span data-ttu-id="a6116-217">Die folgenden Tabellen stellen eine Richtlinie für die Anzahl von gleichzeitigen anrufen dar, die von einem Vermittlungsserver verarbeitet werden können, vorausgesetzt, die Hardware für die Vermittlungsserver erfüllt die Anforderungen in [Server Hardwareplattformen für lync Server 2013](lync-server-2013-server-hardware-platforms.md) und das Hyper-Threading ist aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a6116-217">The following tables provide a guideline for how many concurrent calls a Mediation Server can handle, assuming that the hardware for the Mediation Servers meets the requirements in [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md) and that hyper-threading is enabled.</span></span> <span data-ttu-id="a6116-218">Details zur Vermittlungsserver-Skalierbarkeit finden Sie unter [schätzen der Sprachverwendung und des Datenverkehrs für lync Server 2013](lync-server-2013-estimating-voice-usage-and-traffic.md) und [Bereitstellungsrichtlinien für den Vermittlungsserver in lync Server 2013](lync-server-2013-deployment-guidelines-for-mediation-server.md).</span><span class="sxs-lookup"><span data-stu-id="a6116-218">For details about Mediation Server scalability, see [Estimating voice usage and traffic for Lync Server 2013](lync-server-2013-estimating-voice-usage-and-traffic.md) and [Deployment guidelines for Mediation Server in Lync Server 2013](lync-server-2013-deployment-guidelines-for-mediation-server.md).</span></span>

<span data-ttu-id="a6116-219">Alle folgenden Tabellen gehen davon aus, dass die Verwendung in [Benutzermodellen in lync Server 2013](lync-server-2013-user-models.md)zusammengefasst ist.</span><span class="sxs-lookup"><span data-stu-id="a6116-219">All the following tables assume usage as summarized in [User models in Lync Server 2013](lync-server-2013-user-models.md).</span></span>

### <a name="stand-alone-mediation-server-capacity-70-internal-users-30-external-users-with-non-bypass-call-capacity-media-transcoding-performed-by-mediation-server"></a><span data-ttu-id="a6116-220">Eigenständige Vermittlungs Server Kapazität: 70% interne Benutzer, 30% externe Benutzer mit nicht-Bypass-Anrufkapazität (vom Vermittlungsserver durchgeführte Medienumwandlung)</span><span class="sxs-lookup"><span data-stu-id="a6116-220">Stand-alone Mediation Server Capacity: 70% Internal Users, 30% External users with non-bypass call capacity (media transcoding performed by Mediation Server)</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6116-221">Serverhardware</span><span class="sxs-lookup"><span data-stu-id="a6116-221">Server hardware</span></span></th>
<th><span data-ttu-id="a6116-222">Maximale Anzahl von Anrufen</span><span class="sxs-lookup"><span data-stu-id="a6116-222">Maximum number of calls</span></span></th>
<th><span data-ttu-id="a6116-223">Maximale Anzahl von T1-Leitungen</span><span class="sxs-lookup"><span data-stu-id="a6116-223">Maximum number of T1 lines</span></span></th>
<th><span data-ttu-id="a6116-224">Maximale Anzahl von E1-Leitungen</span><span class="sxs-lookup"><span data-stu-id="a6116-224">Maximum number of E1 lines</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6116-225">Dualprozessor, Vierkern, Hyperthreading-CPU mit 2,26 GHz  <strong>und deaktiviertem Hyperthreading </strong>, 32 GB Arbeitsspeicher und einem Dualport-Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="a6116-225">Dual processor, hex core, 2.26 GHz hyper-threaded CPU <strong>with hyper-threading disabled</strong>, with 32 GB memory and one dual-port network adapter card.</span></span></p></td>
<td><p><span data-ttu-id="a6116-226">1100</span><span class="sxs-lookup"><span data-stu-id="a6116-226">1100</span></span></p></td>
<td><p><span data-ttu-id="a6116-227">46</span><span class="sxs-lookup"><span data-stu-id="a6116-227">46</span></span></p></td>
<td><p><span data-ttu-id="a6116-228">35</span><span class="sxs-lookup"><span data-stu-id="a6116-228">35</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6116-229">Dualprozessor, Sechskern, Hyperthreading-CPU mit 2,26 GHz, 32 GB Arbeitsspeicher und ein Dualport-Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="a6116-229">Dual processor, hex core, 2.26 GHz hyper-threaded CPU, with 32 GB memory and one dual-port network adapter card.</span></span></p></td>
<td><p><span data-ttu-id="a6116-230">1500</span><span class="sxs-lookup"><span data-stu-id="a6116-230">1500</span></span></p></td>
<td><p><span data-ttu-id="a6116-231">63</span><span class="sxs-lookup"><span data-stu-id="a6116-231">63</span></span></p></td>
<td><p><span data-ttu-id="a6116-232">47</span><span class="sxs-lookup"><span data-stu-id="a6116-232">47</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="a6116-233">Obwohl Server mit 32 GB Arbeitsspeicher für Leistungstests verwendet wurden, werden Server mit 16 GB Arbeitsspeicher für eigenständigen Vermittlungs Server unterstützt und genügen, um die in dieser Tabelle gezeigte Leistung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="a6116-233">Although servers with 32 GB of memory were used for performance testing, servers with 16 GB of memory are supported for stand-alone Mediation Server, and are sufficient to provide the performance shown in this table.</span></span>



</div>

### <a name="mediation-server-capacity-mediation-server-collocated-with-front-end-server-70-internal-users-30-external-users-non-bypass-call-capacity-media-processing-performed-by-mediation-server"></a><span data-ttu-id="a6116-234">Vermittlungsserver Kapazität (Mediationsserver mit Front-End-Server) 70% interne Benutzer, 30% externe Benutzer, nicht-Bypass-Anrufkapazität (Medienverarbeitung vom Vermittlungsserver ausgeführt)</span><span class="sxs-lookup"><span data-stu-id="a6116-234">Mediation Server Capacity (Mediation Server Collocated with Front End Server) 70% Internal Users, 30% External Users, Non-Bypass Call Capacity (Media Processing Performed by Mediation Server)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6116-235">Serverhardware</span><span class="sxs-lookup"><span data-stu-id="a6116-235">Server hardware</span></span></th>
<th><span data-ttu-id="a6116-236">Maximale Anzahl von Anrufen</span><span class="sxs-lookup"><span data-stu-id="a6116-236">Maximum number of calls</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6116-237">Dualprozessor, Sechskern, Hyperthreading-CPU mit 2,26 GHz und deaktiviertem Hyperthreading, 32 GB Arbeitsspeicher und zwei Netzwerkadapter mit 1 GB.</span><span class="sxs-lookup"><span data-stu-id="a6116-237">Dual processor, hex core, 2.26 GHz hyper-threaded CPU, with 32 GB memory and 2 1GB network adapter cards.</span></span></p></td>
<td><p><span data-ttu-id="a6116-238">150</span><span class="sxs-lookup"><span data-stu-id="a6116-238">150</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="a6116-239">Diese Zahl ist viel kleiner als die Zahlen für den eigenständigen Vermittlungsserver, da der Front-End-Server andere Features und Funktionen für die 6600-Benutzer, die sich auf diesem Server befinden, sowie die für Sprachanrufe benötigte Transcodierung verarbeiten muss.</span><span class="sxs-lookup"><span data-stu-id="a6116-239">This number is much smaller than the numbers for the stand-alone Mediation Server because the Front End Server has to handle other features and functions for the 6600 users homed on it, in addition to the transcoding needed for voice calls.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="a6116-240">Um die Leistung des Vermittlungsservers zu verbessern, sollten Sie auf den Netzwerkadaptern auf Ihren Vermittlungsservern die Receive-Side-Skalierung (RSS) aktivieren.</span><span class="sxs-lookup"><span data-stu-id="a6116-240">To improve the performance of the Mediation Server, you should enable receive-side scaling (RSS) on the network adapters on your Mediation Servers.</span></span> <span data-ttu-id="a6116-241">Mit RSS können eingehende Pakete gleichzeitig von mehreren Prozessoren auf dem Server verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="a6116-241">RSS enables incoming packets to be handled in parallel by multiple processors on the server.</span></span> <span data-ttu-id="a6116-242">Ausführliche Informationen finden Sie unter "Verbesserungen bei der Empfangs seitigen Skalierung in Windows Server 2008" <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?linkId=268731</A> .</span><span class="sxs-lookup"><span data-stu-id="a6116-242">For details, see "Receive-Side Scaling Enhancements in Windows Server 2008" at <A href="https://go.microsoft.com/fwlink/p/?linkid=268731">https://go.microsoft.com/fwlink/p/?linkId=268731</A>.</span></span> <span data-ttu-id="a6116-243">Weitere Informationen zum Aktivieren von RSS finden Sie in der Dokumentation zu Ihrem Netzwerkadapter.</span><span class="sxs-lookup"><span data-stu-id="a6116-243">For details about how to enable RSS, see your network adapter documentation.</span></span>



</div>

</div>

<div>

## <a name="back-end-server"></a><span data-ttu-id="a6116-244">Back-End-Server</span><span class="sxs-lookup"><span data-stu-id="a6116-244">Back End Server</span></span>

<span data-ttu-id="a6116-245">In lync Server 2013 befinden sich die Anwesenheits Datenbanken auf den Front-End-Servern statt auf dem Back-End-Server.</span><span class="sxs-lookup"><span data-stu-id="a6116-245">In Lync Server 2013, the presence databases are located on the Front End Servers instead of the Back End Server.</span></span> <span data-ttu-id="a6116-246">Dies hat zu einer wesentlich einfacheren Anforderung für jeden Back-End-Server in lync Server 2013 geführt, der der Hardwareanforderung für den Front-End-Server entspricht.</span><span class="sxs-lookup"><span data-stu-id="a6116-246">This has resulted in a much simpler requirement for each Back End Server in Lync Server 2013, equivalent to the hardware requirement for the Front End Server.</span></span> <span data-ttu-id="a6116-247">Vergleichen Sie dies mit lync Server 2010, bei dem der Back-End-Server ein viel höherwertiger Server mit 25 Datenträgern sein muss.</span><span class="sxs-lookup"><span data-stu-id="a6116-247">Contrast this to Lync Server 2010, where the Back End Server was required to be a much higher grade server with 25 disks.</span></span> <span data-ttu-id="a6116-248">Die Arbeitsauslastung von Back-End-Servern ist jedoch weiterhin so, dass Sie die Hardwareempfehlungen, die weiter oben in diesem Abschnitt und auf [Server Hardwareplattformen für lync Server 2013](lync-server-2013-server-hardware-platforms.md)aufgeführt sind, nicht versäumen sollten.</span><span class="sxs-lookup"><span data-stu-id="a6116-248">However, the workload of Back End Servers is still such that you should not fail to meet the hardware recommendations listed earlier in this section and in [Server hardware platforms for Lync Server 2013](lync-server-2013-server-hardware-platforms.md).</span></span>

<span data-ttu-id="a6116-249">Zur Bereitstellung einer großen Verfügbarkeit Ihres Back-End-Servers empfehlen wir die Bereitstellung der Server Spiegelung.</span><span class="sxs-lookup"><span data-stu-id="a6116-249">To provide high availability of your Back End Server, we recommend deploying server mirroring.</span></span> <span data-ttu-id="a6116-250">Weitere Informationen finden Sie unter [Back-End-Server-Höchstverfügbarkeit in lync Server 2013](lync-server-2013-back-end-server-high-availability.md).</span><span class="sxs-lookup"><span data-stu-id="a6116-250">For more information, see [Back End Server high availability in Lync Server 2013](lync-server-2013-back-end-server-high-availability.md).</span></span>

</div>

<div>

## <a name="monitoring-and-archiving"></a><span data-ttu-id="a6116-251">Überwachen und Archivieren</span><span class="sxs-lookup"><span data-stu-id="a6116-251">Monitoring and Archiving</span></span>

<span data-ttu-id="a6116-252">Wenn Sie in lync Server 2013 die Überwachung oder Archivierung bereitstellen, wird die Front-End-Funktionalität dieser Dienste auf den Front-End-Servern statt auf separaten Server Rollen ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="a6116-252">In Lync Server 2013, if you deploy Monitoring or Archiving, the front end functionality of these services runs on the Front End Servers, instead of on separate server roles.</span></span> <span data-ttu-id="a6116-253">Für die Überwachung und Archivierung wird jeweils weiterhin ein eigener Datenbankspeicher separat vom Back-End-Speicher verwendet.</span><span class="sxs-lookup"><span data-stu-id="a6116-253">Monitoring and Archiving each still use their own database store, separate from the Back End store.</span></span> <span data-ttu-id="a6116-254">Wenn Sie jedoch Exchange 2013 bereitgestellt haben, können Sie Sofortnachrichten-Archivierungsdaten in Exchange anstatt in einem dedizierten SQL Store speichern.</span><span class="sxs-lookup"><span data-stu-id="a6116-254">Alternatively, if you have Exchange 2013 deployed, you can store instant message Archiving data in Exchange instead of in a dedicated SQL store.</span></span>

<span data-ttu-id="a6116-255">Die folgende Tabelle zeigt, wie viele Datenbankspeicher pro Benutzer und Tag für die Daten aus der Überwachung und Archivierung in etwa benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="a6116-255">The following table indicates approximately how much database storage is required per user per day for Monitoring and Archiving data.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<tbody>
<tr class="odd">
<td></td>
<td><p><span data-ttu-id="a6116-256"><strong>KDS (Überwachung)</strong></span><span class="sxs-lookup"><span data-stu-id="a6116-256"><strong>CDR (Monitoring)</strong></span></span></p></td>
<td><p><span data-ttu-id="a6116-257"><strong>QoE (Überwachung)</strong></span><span class="sxs-lookup"><span data-stu-id="a6116-257"><strong>QoE (Monitoring)</strong></span></span></p></td>
<td><p><span data-ttu-id="a6116-258"><strong>Archiving</strong></span><span class="sxs-lookup"><span data-stu-id="a6116-258"><strong>Archiving</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6116-259">Pro Benutzer und Tag benötigter Festplattenspeicher</span><span class="sxs-lookup"><span data-stu-id="a6116-259">Disk space required per user per day</span></span></p></td>
<td><p><span data-ttu-id="a6116-260">49 KB</span><span class="sxs-lookup"><span data-stu-id="a6116-260">49 KB</span></span></p></td>
<td><p><span data-ttu-id="a6116-261">28 KB</span><span class="sxs-lookup"><span data-stu-id="a6116-261">28 KB</span></span></p></td>
<td><p><span data-ttu-id="a6116-262">57 KB</span><span class="sxs-lookup"><span data-stu-id="a6116-262">57 KB</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="a6116-263">Microsoft hat bei den Leistungstests für den Datenbankserver die in der folgenden Tabelle aufgeführte Hardware für die Überwachung und Archivierung eingesetzt.</span><span class="sxs-lookup"><span data-stu-id="a6116-263">Microsoft used the hardware in the following table for the database server for Monitoring and Archiving during its performance testing.</span></span> <span data-ttu-id="a6116-264">Die Tests sammelten die Daten von zwei Front-End-Pools, die jeweils 80.000-Benutzer enthielten.</span><span class="sxs-lookup"><span data-stu-id="a6116-264">The testing collected the data of two Front End pools, each of which contained 80,000 users.</span></span>

### <a name="hardware-used-in-monitoring-and-archiving-performance-testing"></a><span data-ttu-id="a6116-265">Beim Leistungstest der Überwachung und Archivierung eingesetzte Hardware</span><span class="sxs-lookup"><span data-stu-id="a6116-265">Hardware Used in Monitoring and Archiving Performance Testing</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="a6116-266">Hardwarekomponente</span><span class="sxs-lookup"><span data-stu-id="a6116-266">Hardware component</span></span></th>
<th><span data-ttu-id="a6116-267">Empfohlen</span><span class="sxs-lookup"><span data-stu-id="a6116-267">Recommended</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6116-268">CPU</span><span class="sxs-lookup"><span data-stu-id="a6116-268">CPU</span></span></p></td>
<td><p><span data-ttu-id="a6116-269">64-Bit-Dualprozessor, Sechskern, mindestens 2,26 GHz</span><span class="sxs-lookup"><span data-stu-id="a6116-269">64-bit dual processor, hex-core, 2.26 gigahertz (GHz) or higher</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6116-270">Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="a6116-270">Memory</span></span></p></td>
<td><p><span data-ttu-id="a6116-271">48 GB</span><span class="sxs-lookup"><span data-stu-id="a6116-271">48 gigabytes (GB)</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6116-272">Festplatte</span><span class="sxs-lookup"><span data-stu-id="a6116-272">Disk</span></span></p></td>
<td><p><span data-ttu-id="a6116-273">25 Festplatten mit 10.000 U/Min mit jeweils 300 GB und der folgenden Konfiguration</span><span class="sxs-lookup"><span data-stu-id="a6116-273">25 10,000-RPM hard disk drives with 300 GB on each disk, with the following configuration</span></span></p>
<h3 id="section-3"> </h3>
<div>
<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="a6116-274"><strong>Laufwerk</strong></span><span class="sxs-lookup"><span data-stu-id="a6116-274"><strong>Drive</strong></span></span></p></td>
<td><p><span data-ttu-id="a6116-275"><strong>RAID-Konfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="a6116-275"><strong>RAID Configuration</strong></span></span></p></td>
<td><p><span data-ttu-id="a6116-276"><strong>Anzahl Festplatten</strong></span><span class="sxs-lookup"><span data-stu-id="a6116-276"><strong>Number of disks</strong></span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6116-277">KDS-, QoE- und Archivdatenbankdateien auf einem einzigen Laufwerk</span><span class="sxs-lookup"><span data-stu-id="a6116-277">CDR, QoE, and Archiving database data files, on a single drive</span></span></p></td>
<td><p><span data-ttu-id="a6116-278">1+0</span><span class="sxs-lookup"><span data-stu-id="a6116-278">1+0</span></span></p></td>
<td><p><span data-ttu-id="a6116-279">16</span><span class="sxs-lookup"><span data-stu-id="a6116-279">16</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6116-280">KDS-Datenbankprotokolldatei</span><span class="sxs-lookup"><span data-stu-id="a6116-280">CDR database log file</span></span></p></td>
<td><p><span data-ttu-id="a6116-281">1</span><span class="sxs-lookup"><span data-stu-id="a6116-281">1</span></span></p></td>
<td><p><span data-ttu-id="a6116-282">2</span><span class="sxs-lookup"><span data-stu-id="a6116-282">2</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6116-283">QoE-Datenbankprotokolldatei</span><span class="sxs-lookup"><span data-stu-id="a6116-283">QoE database log file</span></span></p></td>
<td><p><span data-ttu-id="a6116-284">1</span><span class="sxs-lookup"><span data-stu-id="a6116-284">1</span></span></p></td>
<td><p><span data-ttu-id="a6116-285">2</span><span class="sxs-lookup"><span data-stu-id="a6116-285">2</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="a6116-286">Archiv-Datenbankprotokolldatei</span><span class="sxs-lookup"><span data-stu-id="a6116-286">Archiving database log file</span></span></p></td>
<td><p><span data-ttu-id="a6116-287">1</span><span class="sxs-lookup"><span data-stu-id="a6116-287">1</span></span></p></td>
<td><p><span data-ttu-id="a6116-288">2</span><span class="sxs-lookup"><span data-stu-id="a6116-288">2</span></span></p></td>
</tr>
</tbody>
</table>

</div></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="a6116-289">Netzwerk</span><span class="sxs-lookup"><span data-stu-id="a6116-289">Network</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="a6116-290">1 Dual-Port-Netzwerkadapter, mindestens 1 GBit/s (2 werden empfohlen, wofür die Verknüpfung mit einer einzelnen MAC-Adresse und einer einzelnen IP-Adresse erforderlich ist)</span><span class="sxs-lookup"><span data-stu-id="a6116-290">1 dual-port network adapter, 1 Gbps or higher (2 recommended, which requires teaming with a single MAC address and single IP address)</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a6116-291">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a6116-291">In This Section</span></span>

  - [<span data-ttu-id="a6116-292">Schätzen von VoIP-Nutzung und -Datenverkehr für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6116-292">Estimating voice usage and traffic for Lync Server 2013</span></span>](lync-server-2013-estimating-voice-usage-and-traffic.md)

  - [<span data-ttu-id="a6116-293">Bereitstellungsrichtlinien für den Vermittlungsserver in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a6116-293">Deployment guidelines for Mediation Server in Lync Server 2013</span></span>](lync-server-2013-deployment-guidelines-for-mediation-server.md)

<span data-ttu-id="a6116-294"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a6116-294"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

