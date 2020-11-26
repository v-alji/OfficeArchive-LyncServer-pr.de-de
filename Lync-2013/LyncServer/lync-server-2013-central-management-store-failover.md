---
title: 'Lync Server 2013: Failover des zentralen Verwaltungsspeichers'
description: Failover des zentralen Verwaltungsspeichers für lync Server 2013
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Central Management store failover
ms:assetid: f464d715-68a4-462c-9584-00f41ab10db0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205376(v=OCS.15)
ms:contentKeyID: 48185809
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d2960a55d6bdc49e00bf22997bc53946d4770fde
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435467"
---
# <a name="central-management-store-failover-in-lync-server-2013"></a><span data-ttu-id="0759b-103">Failover des zentralen Verwaltungsspeichers in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0759b-103">Central Management store failover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0759b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0759b-104">

<span> </span></span></span>

<span data-ttu-id="0759b-105">_**Letztes Änderungsdatum des Themas:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="0759b-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="0759b-106">Der zentrale Verwaltungsspeicher enthält Konfigurationsdaten zu Servern und Diensten in ihrer lync 2013-Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="0759b-106">The Central Management store contains configuration data about servers and services in your Lync 2013 deployment.</span></span> <span data-ttu-id="0759b-107">Sie bietet eine robuste, schematisierten Speicherung der Daten, die zum definieren, einrichten, warten, verwalten, beschreiben und betreiben einer lync 2013-Bereitstellung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="0759b-107">It provides a robust, schematized storage of the data needed to define, set up, maintain, administer, describe, and operate a Lync 2013 deployment.</span></span> <span data-ttu-id="0759b-108">Darüber hinaus überprüft er die Daten, um eine konsistente Konfiguration zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="0759b-108">It also validates the data to ensure configuration consistency.</span></span>

<span data-ttu-id="0759b-109">Jede lync-Bereitstellung umfasst einen zentralen Verwaltungsspeicher, der vom Back-End-Server eines Front-End-Pools gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="0759b-109">Each Lync deployment includes one Central Management store, which is hosted by the Back End Server of one Front End pool.</span></span>

<span data-ttu-id="0759b-110">Wenn Sie eine Pool Kopplung einrichten, die den Pool hostet, in dem der zentrale Verwaltungsspeicher gehostet wird, wird im Sicherungspool eine Datenbank des zentralen Verwaltungsspeichers eingerichtet, und die zentralen Verwaltungsspeicher Dienste werden in beiden Pools installiert.</span><span class="sxs-lookup"><span data-stu-id="0759b-110">When you establish a pool pairing that includes the pool hosting the Central Management store, a backup Central Management store database is set up in the backup pool, and Central Management store services are installed in both pools.</span></span> <span data-ttu-id="0759b-111">Eine der beiden zentralen Verwaltungsspeicher Datenbanken ist zu einem beliebigen Zeitpunkt der aktive Master und der andere ein Standbymodus.</span><span class="sxs-lookup"><span data-stu-id="0759b-111">At any point in time, one of the two Central Management store databases is the active master, and the other is a standby.</span></span> <span data-ttu-id="0759b-112">Der Inhalt wird vom Sicherungsdienst vom aktiven Master in den Standbymodus repliziert.</span><span class="sxs-lookup"><span data-stu-id="0759b-112">The content is replicated by the Backup Service from the active master to the standby.</span></span>

<span data-ttu-id="0759b-113">Bei einem Pool-Failover, das die Pools umfasst, die den zentralen Verwaltungsspeicher hosten, muss der Administrator vor dem Failover des Front-End-Pools einen Failover für den zentralen Verwaltungsspeicher durchführen.</span><span class="sxs-lookup"><span data-stu-id="0759b-113">During a pool failover that involves the pools hosting the Central Management store, the administrator must fail over the Central Management store before failing over the Front End pool.</span></span>

<span data-ttu-id="0759b-114">Nach der Behebung des Notfalls ist es nicht erforderlich, einen Failback des zentralen Verwaltungsspeichers durchzuführen.</span><span class="sxs-lookup"><span data-stu-id="0759b-114">After the disaster is repaired, it is not necessary to fail back the Central Management store.</span></span> <span data-ttu-id="0759b-115">Nach der Reparatur kann der zentrale Verwaltungsspeicher im ursprünglichen Sicherungspool als aktiver MasterVerb leiben.</span><span class="sxs-lookup"><span data-stu-id="0759b-115">After repair, the Central Management store in the original backup pool can remain as the active master.</span></span>

<span data-ttu-id="0759b-116">Die Entwicklungsziele für den zentralen Verwaltungsspeicher sind 5 Minuten für die Wiederherstellungsdauer (Recovery Time Objective, RTO) und 5 Minuten für den Wiederherstellungspunkt (Recovery Point Objective, RPO).</span><span class="sxs-lookup"><span data-stu-id="0759b-116">The engineering targets for Central Management store failover are 5 minutes for recovery time objective (RTO) and 5 minutes for recovery point objective (RPO).</span></span>

<span data-ttu-id="0759b-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0759b-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

