---
title: Konfigurieren der hohen Verfügbarkeit und der Notfallwiederherstellung für den Server für beständigen Chat
description: Konfigurieren des beständigen Chat Servers für höhere Verfügbarkeit und Disaster Recovery
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Persistent Chat Server for high availability and disaster recovery
ms:assetid: eebc581c-e3a0-4b69-8a43-80b607b4d8f2
ms:mtpsurl: https://technet.microsoft.com/library/JJ205364(v=OCS.15)
ms:contentKeyID: 48185760
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 13935f2ec690deb7f896c13d185680ce1122a892
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432786"
---
# <a name="configuring-persistent-chat-server-for-high-availability-and-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="7a0a3-103">Konfigurieren der hohen Verfügbarkeit und der Notfallwiederherstellung für den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7a0a3-103">Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7a0a3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7a0a3-104">

<span> </span></span></span>

<span data-ttu-id="7a0a3-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="7a0a3-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="7a0a3-106">Lync Server 2013, persistent Chat Server Services verwenden eine *ausgestreckte Pool* Konfiguration für die Notfallwiederherstellung.</span><span class="sxs-lookup"><span data-stu-id="7a0a3-106">The Lync Server 2013, Persistent Chat Server services use a *stretched pool* configuration for disaster recovery.</span></span> <span data-ttu-id="7a0a3-107">Bei einem gedehnten Pool handelt es sich um einen Pool mit Computern, die zwischen zwei physikalischen Rechenzentren verteilt sind, sich aber auf einer einzelnen logischen lync Server-Website befinden.</span><span class="sxs-lookup"><span data-stu-id="7a0a3-107">A stretched pool is a pool that has computers that are distributed between two physical data centers, but are within a single logical Lync Server site.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7a0a3-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="7a0a3-108">In This Section</span></span>

  - [<span data-ttu-id="7a0a3-109">Erforderliche Ressourcen für den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7a0a3-109">Required resources for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-required-resources-for-persistent-chat-server.md)

  - [<span data-ttu-id="7a0a3-110">Konfigurieren von hoher Verfügbarkeit und Notfallwiederherstellung mithilfe des Topologie-Generators in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7a0a3-110">Using Topology Builder to configure high availability and disaster recovery in Lync Server 2013</span></span>](lync-server-2013-using-topology-builder-to-configure-high-availability-and-disaster-recovery.md)

  - [<span data-ttu-id="7a0a3-111">Verwenden eines ausgedehnten Pools für den Server für beständigen Chat für die Notfallwiederherstellung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7a0a3-111">Using a stretched Persistent Chat Server pool for disaster recovery in Lync Server 2013</span></span>](lync-server-2013-using-a-stretched-persistent-chat-server-pool-for-disaster-recovery.md)

  - [<span data-ttu-id="7a0a3-112">SQL Server-Spiegelung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7a0a3-112">SQL Server mirroring in Lync Server 2013</span></span>](lync-server-2013-sql-server-mirroring.md)

  - [<span data-ttu-id="7a0a3-113">Einrichten des SQL Server-Protokollversands für die primäre Datenbank des Servers für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7a0a3-113">Setting up SQL Server Log Shipping in Lync Server 2013 for the Persistent Chat Server primary database</span></span>](lync-server-2013-setting-up-sql-server-log-shipping-for-the-persistent-chat-server-primary-database.md)

  - [<span data-ttu-id="7a0a3-114">Einrichten des SQL Server-Protokollversands zwischen der primären Spiegeldatenbank und der sekundären Datenbank des Protokollversands in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7a0a3-114">Setting up SQL Server Log Shipping between the primary mirror and the Log Shipping secondary database in Lync Server 2013</span></span>](lync-server-2013-set-up-log-shipping-secondary-database.md)

<span data-ttu-id="7a0a3-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7a0a3-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

