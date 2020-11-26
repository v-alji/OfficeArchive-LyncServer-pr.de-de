---
title: 'Lync Server 2013: Serverhardwareplattformen'
description: Lync Server 2013 Server-Hardwareplattformen.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Server hardware platforms
ms:assetid: c964c1c0-0153-472b-88ad-a38866e0df0c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398835(v=OCS.15)
ms:contentKeyID: 48185395
ms.date: 07/28/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d55deec50994d70cf305b794662a630c16c3af14
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441872"
---
# <a name="server-hardware-platforms-for-lync-server-2013"></a><span data-ttu-id="55d08-103">Serverhardwareplattformen für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="55d08-103">Server hardware platforms for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="55d08-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="55d08-104">

<span> </span></span></span>

<span data-ttu-id="55d08-105">_**Letztes Änderungsdatum des Themas:** 2016-07-28_</span><span class="sxs-lookup"><span data-stu-id="55d08-105">_**Topic Last Modified:** 2016-07-28_</span></span>

<span data-ttu-id="55d08-106">Serverfunktionen von lync Server 2013 und Computern, auf denen lync Server-Verwaltungstools ausgeführt werden, erfordern 64-Bit-Hardware.</span><span class="sxs-lookup"><span data-stu-id="55d08-106">Lync Server 2013 server roles and computers running Lync Server administrative tools require 64-bit hardware.</span></span>

<span data-ttu-id="55d08-107">Die spezifische Hardware, die für die lync Server 2013-Bereitstellung verwendet wird, kann abhängig von der Größe und den Verwendungsanforderungen variieren.</span><span class="sxs-lookup"><span data-stu-id="55d08-107">The specific hardware used for Lync Server 2013 deployment can vary, depending on size and usage requirements.</span></span> <span data-ttu-id="55d08-108">In diesem Abschnitt wird die empfohlene Hardware beschrieben.</span><span class="sxs-lookup"><span data-stu-id="55d08-108">This section describes the recommended hardware.</span></span> <span data-ttu-id="55d08-109">Wenngleich es sich hier nicht um Anforderungen, sondern um Empfehlungen handelt, kann der Einsatz von Hardware, die diesen Empfehlungen nicht entspricht, zu erheblichen Leistungsproblemen und sonstigen Problemen führen.</span><span class="sxs-lookup"><span data-stu-id="55d08-109">Although these are recommendations, not requirements, using hardware that does not meet these recommendations may result in significant performance issues and other issues.</span></span>

<div>

## <a name="recommended-hardware-platform"></a><span data-ttu-id="55d08-110">Empfohlene Hardwareplattform</span><span class="sxs-lookup"><span data-stu-id="55d08-110">Recommended Hardware Platform</span></span>

<span data-ttu-id="55d08-111">Für eine optimale Leistung empfehlen wir, dass Sie lync Server auf Servern mit Hardware ausführen, die die Anforderungen in der folgenden Tabelle erfüllt.</span><span class="sxs-lookup"><span data-stu-id="55d08-111">For best performance, we recommend that you run Lync Server on servers with hardware that meets the requirements in the following table.</span></span> <span data-ttu-id="55d08-112">Wenn Sie weniger leistungsfähige Hardware verwenden, treten möglicherweise Funktionsprobleme oder eine schlechte Leistung auf.</span><span class="sxs-lookup"><span data-stu-id="55d08-112">If you use less powerful hardware, you may experience functionality problems or poor performance.</span></span> <span data-ttu-id="55d08-113">Beachten Sie, dass diese Hardwareanforderungen höher als in früheren Versionen von lync Server sind, hauptsächlich deshalb, weil in lync Server 2013 alle Front-End-Server SQL Server ausführen.</span><span class="sxs-lookup"><span data-stu-id="55d08-113">Note that these hardware requirements are higher than those of previous versions of Lync Server, primarily because in Lync Server 2013, all Front End Servers run SQL Server.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="55d08-114">NIC-Teaming wird unterstützt und sollte für lync Server transparent sein.</span><span class="sxs-lookup"><span data-stu-id="55d08-114">NIC teaming is supported and should be transparent to Lync Server.</span></span> <span data-ttu-id="55d08-115">Ausführliche Informationen finden Sie unter <A href="https://go.microsoft.com/fwlink/p/?linkid=389910">Communications Server-oder lync Server-und Netzwerkadapter-Teaming</A>.</span><span class="sxs-lookup"><span data-stu-id="55d08-115">For details, see <A href="https://go.microsoft.com/fwlink/p/?linkid=389910">Communications Server or Lync Server and network adapter teaming</A>.</span></span>



</div>

### <a name="recommended-hardware-for-front-end-servers-back-end-servers-standard-edition-servers-persistent-chat-servers-and-persistent-chat-store-and-persistent-chat-compliance-store-back-end-server-roles-for-persistent-chat-server"></a><span data-ttu-id="55d08-116">Empfohlene Hardware für Front-End-Server, Back-End-Server, Standard Edition-Server, Server für beständigen Chat, Speicher für beständigen Chat und Compliance-Speicher für beständigen Chat (Back-End-Serverrollen für Server für beständigen Chat)</span><span class="sxs-lookup"><span data-stu-id="55d08-116">Recommended Hardware for Front End Servers, Back End Servers, Standard Edition Servers, Persistent Chat Servers, and Persistent Chat Store and Persistent Chat Compliance Store (Back End Server Roles for Persistent Chat Server)</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55d08-117">Hardwarekomponente</span><span class="sxs-lookup"><span data-stu-id="55d08-117">Hardware component</span></span></th>
<th><span data-ttu-id="55d08-118">Empfohlen</span><span class="sxs-lookup"><span data-stu-id="55d08-118">Recommended</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55d08-119">CPU</span><span class="sxs-lookup"><span data-stu-id="55d08-119">CPU</span></span></p></td>
<td><p><span data-ttu-id="55d08-120">64-Bit-Dualprozessor, Sechskern, mindestens 2,26 GHz.</span><span class="sxs-lookup"><span data-stu-id="55d08-120">64-bit dual processor, hex-core, 2.26 gigahertz (GHz) or higher.</span></span></p>
<p><span data-ttu-id="55d08-121">Intel Itanium-Prozessoren werden für lync Server-Serverrollen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="55d08-121">Intel Itanium processors are not supported for Lync Server server roles.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55d08-122">Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="55d08-122">Memory</span></span></p></td>
<td><p><span data-ttu-id="55d08-123">32 GB.</span><span class="sxs-lookup"><span data-stu-id="55d08-123">32 gigabytes (GB).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55d08-124">Festplatte</span><span class="sxs-lookup"><span data-stu-id="55d08-124">Disk</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="55d08-125">Mindestens 8 Festplattenlaufwerke mit 10.000 U/min und mindestens 72 GB freiem Speicherplatz</span><span class="sxs-lookup"><span data-stu-id="55d08-125">8 or more 10,000 RPM hard disk drives with at least 72 GB free disk space.</span></span></p>
<p><span data-ttu-id="55d08-126">Zwei Festplatten sollten RAID 1 verwenden und sechs Festplatten sollten RAID 10 verwenden.</span><span class="sxs-lookup"><span data-stu-id="55d08-126">Two of the disks should use RAID 1, and six should use RAID 10.</span></span></p>
<p><span data-ttu-id="55d08-127">- Oder</span><span class="sxs-lookup"><span data-stu-id="55d08-127">- OR -</span></span></p></li>
<li><p><span data-ttu-id="55d08-128">Festkörperlaufwerke (SSDs) mit einer ähnlichen Leistung wie 8 mechanische Festplattenlaufwerke mit 10.000 U/min.</span><span class="sxs-lookup"><span data-stu-id="55d08-128">Solid state drives (SSDs) which provide performance similar to 8 10,000-RPM mechanical disk drives.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55d08-129">Netzwerk</span><span class="sxs-lookup"><span data-stu-id="55d08-129">Network</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="55d08-130">1 Dual-Port-Netzwerkadapter, mindestens 1 GBit/s (2 werden empfohlen, wofür ein Teamvorgang mit einer einzelnen MAC-Adresse und einer einzelnen IP-Adresse erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="55d08-130">1 dual-port network adapter, 1 Gbps or higher (2 recommended, which requires teaming with a single MAC address and single IP address).</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="55d08-131">Dualkonfigurationen oder mehrfach vernetzte Konfigurationen werden für Front-End-Server, Back-End-Server, Standard Edition-Server und Server für beständigen Chat nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="55d08-131">Dual or multi-homed configurations are not supported for Front End Servers, Back End Servers, Standard Edition servers, and Persistent Chat Servers.</span></span><BR><span data-ttu-id="55d08-132">ILO/DRAC/usw. Verbindungen, die nicht dem Betriebs System ausgesetzt sind und zur Überwachung und Verwaltung der Server Hardware verwendet werden, stellen keinen mehrfach vernetzten Server dar und werden daher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="55d08-132">ILO/DRAC/etc. connections not exposed to the Operating System and used to monitor and manage the server hardware do not constitute a multi-homed server and thus are supported.</span></span>


</div></li>
</ul></td>
</tr>
</tbody>
</table>


### <a name="recommended-hardware-for-edge-servers-standalone-mediation-servers-and-directors"></a><span data-ttu-id="55d08-133">Empfohlene Hardware für Edgeserver, eigenständige Vermittlungsserver und Directors</span><span class="sxs-lookup"><span data-stu-id="55d08-133">Recommended Hardware for Edge Servers, Standalone Mediation Servers, and Directors</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="55d08-134">Hardwarekomponente</span><span class="sxs-lookup"><span data-stu-id="55d08-134">Hardware component</span></span></th>
<th><span data-ttu-id="55d08-135">Empfohlen</span><span class="sxs-lookup"><span data-stu-id="55d08-135">Recommended</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="55d08-136">CPU</span><span class="sxs-lookup"><span data-stu-id="55d08-136">CPU</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="55d08-137">64-Bit-Dualprozessor, Quad-Core, 2,0 Gigahertz (GHz) oder höher</span><span class="sxs-lookup"><span data-stu-id="55d08-137">64-bit dual processor, quad-core, 2.0 gigahertz (GHz) or higher.</span></span></p>
<p><span data-ttu-id="55d08-138">- Oder</span><span class="sxs-lookup"><span data-stu-id="55d08-138">- OR -</span></span></p></li>
<li><p><span data-ttu-id="55d08-139">64-Bit-4-Wege-Prozessor, Dual-Core, 2,0 GHz oder höher</span><span class="sxs-lookup"><span data-stu-id="55d08-139">64-bit 4-way processor, dual-core, 2.0 GHz or higher.</span></span></p></li>
</ul>
<p><span data-ttu-id="55d08-140">Intel Itanium-Prozessoren werden für lync Server-Serverrollen nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="55d08-140">Intel Itanium processors are not supported for Lync Server server roles.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55d08-141">Arbeitsspeicher</span><span class="sxs-lookup"><span data-stu-id="55d08-141">Memory</span></span></p></td>
<td><p><span data-ttu-id="55d08-142">16 Gigabyte (GB).</span><span class="sxs-lookup"><span data-stu-id="55d08-142">16 gigabytes (GB).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="55d08-143">Festplattenspeicher</span><span class="sxs-lookup"><span data-stu-id="55d08-143">Disk</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="55d08-144">4 oder mehr 10.000-rpm-Festplattenlaufwerke mit mindestens 72 GB freiem Speicherplatz.</span><span class="sxs-lookup"><span data-stu-id="55d08-144">4 or more 10,000 RPM hard disk drives with at least 72 GB free disk space.</span></span></p>
<p><span data-ttu-id="55d08-145">Die Festplatten sollten in einer 2x-RAID-1-Konfiguration sein.</span><span class="sxs-lookup"><span data-stu-id="55d08-145">The disks should be in a 2x RAID 1 configuration.</span></span></p>
<p><span data-ttu-id="55d08-146">- Oder</span><span class="sxs-lookup"><span data-stu-id="55d08-146">- OR -</span></span></p></li>
<li><p><span data-ttu-id="55d08-147">Festkörperlaufwerke (SSDs) mit einer ähnlichen Leistung wie 4 mechanische Festplattenlaufwerke mit 10.000 U/min.</span><span class="sxs-lookup"><span data-stu-id="55d08-147">Solid state drives (SSDs) which provide performance similar to 4 10,000-RPM mechanical disk drives.</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="55d08-148">Netzwerk</span><span class="sxs-lookup"><span data-stu-id="55d08-148">Network</span></span></p></td>
<td><ul>
<li><p><span data-ttu-id="55d08-149">1 Dual-Port-Netzwerkadapter, mindestens 1 GBit/s (2 werden empfohlen, wofür ein Teamvorgang mit einer einzelnen MAC-Adresse und einer einzelnen IP-Adresse erforderlich ist).</span><span class="sxs-lookup"><span data-stu-id="55d08-149">1 dual-port network adapter, 1 Gbps or higher (2 recommended, which requires teaming with a single MAC address and single IP address).</span></span> <span data-ttu-id="55d08-150">zwei Netzwerkschnittstellen sind auf Edge-Servern erforderlich und werden auf eigenständigen Vermittlungsservern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="55d08-150">2 network interfaces are required on Edge Servers, and are supported on standalone Mediation Servers.</span></span></p></li>
</ul>
<div>

> [!NOTE]  
> <span data-ttu-id="55d08-151">Dual-oder Multi-Homed-Konfigurationen werden für Directors nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="55d08-151">Dual or multi-homed configurations are not supported for Directors.</span></span><BR><span data-ttu-id="55d08-152">ILO/DRAC/usw. Verbindungen, die nicht dem Betriebs System ausgesetzt sind und zur Überwachung und Verwaltung der Server Hardware verwendet werden, stellen keinen mehrfach vernetzten Server dar und werden daher unterstützt.</span><span class="sxs-lookup"><span data-stu-id="55d08-152">ILO/DRAC/etc. connections not exposed to the Operating System and used to monitor and manage the server hardware do not constitute a multi-homed server and thus are supported.</span></span>


</div>
<p><span data-ttu-id="55d08-153">Für Edgeserver sind zwei Netzwerkschnittstellen erforderlich, bei denen es sich um Dual-Port-Netzwerkadapter, 1 Gbit/s oder höher (oder zwei gekoppelte Netzwerkadapter, für insgesamt vier) handelt, wobei jedes Paar mit einer einzelnen Mac-Adresse und einer einzelnen IP-Adresse für insgesamt zwei Paare zusammengestellt wird.</span><span class="sxs-lookup"><span data-stu-id="55d08-153">Edge Servers will require two network interfaces that are dual-port network adapters, 1 Gbps or higher (or two paired network adapters, for a total of four, each pair being teamed with a single MAC address and a single IP address, for a total of two pairs).</span></span></p>
<p><span data-ttu-id="55d08-154">Die Installation zusätzlicher Netzwerkschnittstellenkarten (NICs), um die Konfiguration einer bestimmten PSTN-IP-Adresse zu ermöglichen, wird auf eigenständigen Vermittlungsservern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="55d08-154">Installation of additional network interface cards (NICs) to allow the configuration of a specific PSTN IP address is supported on standalone Mediation Servers.</span></span></p><span data-ttu-id="55d08-155"></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="55d08-155"></td>
</tr>
</tbody>
</table>


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

