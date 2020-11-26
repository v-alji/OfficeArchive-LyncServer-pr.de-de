---
title: 'Lync Server 2013: Definieren und Konfigurieren der Topologie'
description: 'Lync Server 2013: definieren und Konfigurieren der Topologie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining and configuring the topology
ms:assetid: 51d1601e-4f83-48d4-ad08-3b4d5e2003aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398339(v=OCS.15)
ms:contentKeyID: 48184146
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec444a1ddf434c5a80fdc2d56bdba27573da14ab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431001"
---
# <a name="defining-and-configuring-the-topology-in-lync-server-2013"></a><span data-ttu-id="32af5-103">Definieren und Konfigurieren der Topologie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32af5-103">Defining and configuring the topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="32af5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="32af5-104">

<span> </span></span></span>

<span data-ttu-id="32af5-105">_**Letztes Änderungsdatum des Themas:** 2012-09-14_</span><span class="sxs-lookup"><span data-stu-id="32af5-105">_**Topic Last Modified:** 2012-09-14_</span></span>

<span data-ttu-id="32af5-106">Sie definieren und konfigurieren Ihre Topologie mithilfe des Topologie-Generators.</span><span class="sxs-lookup"><span data-stu-id="32af5-106">You define and configure your topology by using Topology Builder.</span></span> <span data-ttu-id="32af5-107">Für den Topologie-Generator ist es nicht erforderlich, dass Sie Mitglied der lokalen Gruppe Administratoren oder einer privilegierten Domänengruppe (beispielsweise Domänenadministratoren) sind.</span><span class="sxs-lookup"><span data-stu-id="32af5-107">Topology Builder does not require you to be a member of the local Administrators group or a privileged domain group (such as Domain Admins).</span></span> <span data-ttu-id="32af5-108">Sie können Ihre Topologie als Standardbenutzer definieren.</span><span class="sxs-lookup"><span data-stu-id="32af5-108">You can define your topology as a standard user.</span></span> <span data-ttu-id="32af5-109">Wenn Sie den Topologie-Generator bei der ersten Verwendung und nachfolgenden Bearbeitungssitzungen starten, werden Sie aufgefordert, den Speicherort anzugeben, an dem der Topologie-Generator das aktuelle Konfigurationsdokument laden soll.</span><span class="sxs-lookup"><span data-stu-id="32af5-109">When you start Topology Builder on first use and subsequent edit sessions, you are prompted for the location where you want Topology Builder to load the current configuration document.</span></span> <span data-ttu-id="32af5-110">Folgende Optionen stehen zur Auswahl:</span><span class="sxs-lookup"><span data-stu-id="32af5-110">The choices are the following:</span></span>

  - <span data-ttu-id="32af5-111">Herunterladen der Topologie aus einer vorhandenen Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="32af5-111">Download topology from existing deployment</span></span>

  - <span data-ttu-id="32af5-112">Öffnen der Topologie aus einer lokalen Datei</span><span class="sxs-lookup"><span data-stu-id="32af5-112">Open topology from a local file</span></span>

  - <span data-ttu-id="32af5-113">Neue Topologie</span><span class="sxs-lookup"><span data-stu-id="32af5-113">New topology</span></span>

<span data-ttu-id="32af5-114">Wenn Sie bereits eine Topologie definiert haben und den zentralen Verwaltungsspeicher eingerichtet haben, sollten Sie eine Topologie aus einer vorhandenen Bereitstellung herunterladen.</span><span class="sxs-lookup"><span data-stu-id="32af5-114">If you have already defined a topology and have established the Central Management store, you should choose to download a topology from an existing deployment.</span></span> <span data-ttu-id="32af5-115">Der Topologie-Generator liest die Datenbank und ruft die aktuelle Definition ab.</span><span class="sxs-lookup"><span data-stu-id="32af5-115">Topology Builder will read the database and retrieve the current definition.</span></span> <span data-ttu-id="32af5-116">Wenn Sie über einen vorhandenen zentralen Verwaltungsspeicher verfügen, sollten Sie immer diese Option auswählen.</span><span class="sxs-lookup"><span data-stu-id="32af5-116">If you have an existing Central Management store, you should always choose this option.</span></span>

<span data-ttu-id="32af5-117">Wenn Sie keinen zentralen Verwaltungsspeicher eingerichtet haben und eine zuvor gespeicherte Konfiguration bearbeiten möchten, sollten Sie die Topologie aus einer lokalen Datei öffnen.</span><span class="sxs-lookup"><span data-stu-id="32af5-117">If you have not established a Central Management store and want to edit a previously saved configuration, you should choose to open the topology from a local file.</span></span> <span data-ttu-id="32af5-118">Die Datei, die Sie öffnen, ist die Konfigurationsdatei, die in einer vorherigen Sitzung gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="32af5-118">The file that you will open would be the configuration file that was saved in a previous session.</span></span> <span data-ttu-id="32af5-119">Sie können diese Option verwenden, um die zuvor gespeicherte Topologie zu bearbeiten.</span><span class="sxs-lookup"><span data-stu-id="32af5-119">You can use this option to edit the previously saved topology.</span></span>

<div>


> [!WARNING]  
> <span data-ttu-id="32af5-120">Wenn Sie bereits über eine veröffentlichte Topologie verfügen, sollten Sie keine lokale Konfigurationsdatei laden.</span><span class="sxs-lookup"><span data-stu-id="32af5-120">If you already have a published topology, you should not load a local configuration file.</span></span> <span data-ttu-id="32af5-121">Sie sollten die Topologie aus einer vorhandenen Bereitstellung herunterladen.</span><span class="sxs-lookup"><span data-stu-id="32af5-121">You should choose to download the topology from an existing deployment.</span></span>



</div>

<span data-ttu-id="32af5-122">Wählen Sie aus, um eine neue Topologie zu erstellen, wenn Sie eine neue Topologie-Generator-Konfiguration erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="32af5-122">Choose to create a new topology, if you want to create a new Topology Builder configuration.</span></span> <span data-ttu-id="32af5-123">Ein zuvor gespeichertes Design wird nur dann überschrieben, wenn Sie es als die Datei speichern, die Sie in einer früheren Entwurfssitzung erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="32af5-123">A previously saved design is not overwritten unless you choose to save it as the same file that you created in an earlier design session.</span></span>

<span data-ttu-id="32af5-124">In jeder dieser Optionen werden Sie aufgefordert, einen Speicherort für die Konfigurationsdatei des Topology Builder zu speichern.</span><span class="sxs-lookup"><span data-stu-id="32af5-124">In each of these options, you will be prompted for a location to store the Topology Builder configuration file.</span></span> <span data-ttu-id="32af5-125">Der Speicherort für die Datei kann ein lokaler Speicherort, ein freigegebener Speicherort auf einer festgelegten Dateifreigabe oder ein Wechselmedium sein.</span><span class="sxs-lookup"><span data-stu-id="32af5-125">The location for the file could be a local location, a shared location on an established file share, or removable media.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="32af5-126">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="32af5-126">In This Section</span></span>

  - [<span data-ttu-id="32af5-127">Definieren und Konfigurieren einer Topologie für Lync Server 2013 im Topologie-Generator</span><span class="sxs-lookup"><span data-stu-id="32af5-127">Define and configure a topology in Topology Builder for Lync Server 2013</span></span>](lync-server-2013-define-and-configure-a-topology-in-topology-builder.md)

  - [<span data-ttu-id="32af5-128">Definieren und Konfigurieren eines Front-End-Pools oder Standard Edition-Servers in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32af5-128">Define and configure a Front End pool or Standard Edition server in Lync Server 2013</span></span>](lync-server-2013-define-and-configure-a-front-end-pool-or-standard-edition-server.md)

  - [<span data-ttu-id="32af5-129">Bereitstellen von Front-End-Poolpaaren für die Notfallwiederherstellung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32af5-129">Deploying paired Front End pools for disaster recovery in Lync Server 2013</span></span>](lync-server-2013-deploying-paired-front-end-pools-for-disaster-recovery.md)

  - [<span data-ttu-id="32af5-130">Bereitstellen der SQL-Spiegelung für eine hohe Verfügbarkeit von Back-End-Servern in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32af5-130">Deploying SQL mirroring for Back End Server high availability in Lync Server 2013</span></span>](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md)

  - [<span data-ttu-id="32af5-131">Bearbeiten oder Konfigurieren einfacher URLs in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32af5-131">Edit or configure simple URLs in Lync Server 2013</span></span>](lync-server-2013-edit-or-configure-simple-urls.md)

  - [<span data-ttu-id="32af5-132">Auswählen des zentralen Verwaltungsservers in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="32af5-132">Select the Central Management Server in Lync Server 2013</span></span>](lync-server-2013-select-the-central-management-server.md)

<span data-ttu-id="32af5-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="32af5-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

