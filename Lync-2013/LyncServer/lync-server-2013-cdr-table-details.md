---
title: 'Lync Server 2013: Ausführliche Informationen zur CDR-Tabelle'
description: 'Lync Server 2013: CdR-Tabellendetails.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: CDR table details
ms:assetid: 896198f5-672b-48ea-852f-0211c0c90857
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398693(v=OCS.15)
ms:contentKeyID: 48184730
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 331a3dfd4ffccac2ac4a442eeb9ad9171defb41c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435481"
---
# <a name="cdr-table-details-in-lync-server-2013"></a><span data-ttu-id="7d284-103">Ausführliche Informationen zur CDR-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-103">CDR table details in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7d284-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7d284-104">

<span> </span></span></span>

<span data-ttu-id="7d284-105">_**Letztes Änderungsdatum des Themas:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="7d284-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="7d284-106">In den folgenden Themen werden die Spalten in den Datenbankschema Tabellen für den Anruf Detaildatensatz (CDR) detailliert beschrieben.</span><span class="sxs-lookup"><span data-stu-id="7d284-106">The following topics detail the columns in each of the call detail records (CDR) database schema tables.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7d284-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="7d284-107">In This Section</span></span>

  - [<span data-ttu-id="7d284-108">Application-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-108">Application table in Lync Server 2013</span></span>](lync-server-2013-application-table.md)

  - [<span data-ttu-id="7d284-109">CallPriorities-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-109">CallPriorities table in Lync Server 2013</span></span>](lync-server-2013-callpriorities-table.md)

  - [<span data-ttu-id="7d284-110">CallType-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-110">CallType table in Lync Server 2013</span></span>](lync-server-2013-calltype-table.md)

  - [<span data-ttu-id="7d284-111">ClientVersions-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-111">ClientVersions table in Lync Server 2013</span></span>](lync-server-2013-clientversions-table.md)

  - [<span data-ttu-id="7d284-112">ConferenceJoinTimeThresholds-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-112">ConferenceJoinTimeThresholds table in Lync Server 2013</span></span>](lync-server-2013-conferencejointimethresholds-table.md)

  - [<span data-ttu-id="7d284-113">ConferenceMessageCount-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-113">ConferenceMessageCount table in Lync Server 2013</span></span>](lync-server-2013-conferencemessagecount-table.md)

  - [<span data-ttu-id="7d284-114">Conferences-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-114">Conferences table in Lync Server 2013</span></span>](lync-server-2013-conferences-table.md)

  - [<span data-ttu-id="7d284-115">ConferenceSessionDetails-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-115">ConferenceSessionDetails table in Lync Server 2013</span></span>](lync-server-2013-conferencesessiondetails-table.md)

  - [<span data-ttu-id="7d284-116">ConferenceUris-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-116">ConferenceUris table in Lync Server 2013</span></span>](lync-server-2013-conferenceuris-table.md)

  - [<span data-ttu-id="7d284-117">ContentTypes-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-117">ContentTypes table in Lync Server 2013</span></span>](lync-server-2013-contenttypes-table.md)

  - [<span data-ttu-id="7d284-118">DeRegisterType-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-118">DeRegisterType table in Lync Server 2013</span></span>](lync-server-2013-deregistertype-table.md)

  - [<span data-ttu-id="7d284-119">Devices-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-119">Devices table in Lync Server 2013</span></span>](lync-server-2013-devices-table.md)

  - [<span data-ttu-id="7d284-120">Dialogs-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-120">Dialogs table in Lync Server 2013</span></span>](lync-server-2013-dialogs-table.md)

  - [<span data-ttu-id="7d284-121">EdgeServers-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-121">EdgeServers table in Lync Server 2013</span></span>](lync-server-2013-edgeservers-table.md)

  - [<span data-ttu-id="7d284-122">ErrorCategory-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-122">ErrorCategory table in Lync Server 2013</span></span>](lync-server-2013-errorcategory-table.md)

  - [<span data-ttu-id="7d284-123">ErrorDef-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-123">ErrorDef table in Lync Server 2013</span></span>](lync-server-2013-errordef-table.md)

  - [<span data-ttu-id="7d284-124">ErrorReport-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-124">ErrorReport table in Lync Server 2013</span></span>](lync-server-2013-errorreport-table.md)

  - [<span data-ttu-id="7d284-125">FileTransfers-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-125">FileTransfers table in Lync Server 2013</span></span>](lync-server-2013-filetransfers-table.md)

  - [<span data-ttu-id="7d284-126">FocusJoinsAndLeaves-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-126">FocusJoinsAndLeaves table in Lync Server 2013</span></span>](lync-server-2013-focusjoinsandleaves-table.md)

  - [<span data-ttu-id="7d284-127">Frontend-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-127">FrontEnd table in Lync Server 2013</span></span>](lync-server-2013-frontend-table.md)

  - [<span data-ttu-id="7d284-128">Gateways-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-128">Gateways table in Lync Server 2013</span></span>](lync-server-2013-gateways-table.md)

  - [<span data-ttu-id="7d284-129">HardwareVersions-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-129">HardwareVersions table in Lync Server 2013</span></span>](lync-server-2013-hardwareversions-table.md)

  - [<span data-ttu-id="7d284-130">IMReportSummary-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-130">IMReportSummary table in Lync Server 2013</span></span>](lync-server-2013-imreportsummary-table.md)

  - [<span data-ttu-id="7d284-131">Locations-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-131">Locations table in Lync Server 2013</span></span>](lync-server-2013-locations-table.md)

  - [<span data-ttu-id="7d284-132">Manufacturers-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-132">Manufacturers table in Lync Server 2013</span></span>](lync-server-2013-manufacturers-table.md)

  - [<span data-ttu-id="7d284-133">McuJoinsAndLeaves-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-133">McuJoinsAndLeaves table in Lync Server 2013</span></span>](lync-server-2013-mcujoinsandleaves-table.md)

  - [<span data-ttu-id="7d284-134">Mcus-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-134">Mcus table in Lync Server 2013</span></span>](lync-server-2013-mcus-table.md)

  - [<span data-ttu-id="7d284-135">Media-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-135">Media table in Lync Server 2013</span></span>](lync-server-2013-media-table.md)

  - [<span data-ttu-id="7d284-136">MediaList-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-136">MediaList table in Lync Server 2013</span></span>](lync-server-2013-medialist-table.md)

  - [<span data-ttu-id="7d284-137">MediationServers-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-137">MediationServers table in Lync Server 2013</span></span>](lync-server-2013-mediationservers-table.md)

  - [<span data-ttu-id="7d284-138">MSMQProcessing-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-138">MSMQProcessing table in Lync Server 2013</span></span>](lync-server-2013-msmqprocessing-table.md)

  - [<span data-ttu-id="7d284-139">Phones-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-139">Phones table in Lync Server 2013</span></span>](lync-server-2013-phones-table.md)

  - [<span data-ttu-id="7d284-140">Pools-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-140">Pools table in Lync Server 2013</span></span>](lync-server-2013-pools-table.md)

  - [<span data-ttu-id="7d284-141">ProgressReport-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-141">ProgressReport table in Lync Server 2013</span></span>](lync-server-2013-progressreport-table.md)

  - [<span data-ttu-id="7d284-142">PurgeSettings-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-142">PurgeSettings table in Lync Server 2013</span></span>](lync-server-2013-purgesettings-table.md)

  - [<span data-ttu-id="7d284-143">Registration-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-143">Registration table in Lync Server 2013</span></span>](lync-server-2013-registration-table.md)

  - [<span data-ttu-id="7d284-144">Roles-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-144">Roles table in Lync Server 2013</span></span>](lync-server-2013-roles-table.md)

  - [<span data-ttu-id="7d284-145">Servers-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-145">Servers table in Lync Server 2013</span></span>](lync-server-2013-servers-table.md)

  - [<span data-ttu-id="7d284-146">SessionDetails-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-146">SessionDetails table in Lync Server 2013</span></span>](lync-server-2013-sessiondetails-table.md)

  - [<span data-ttu-id="7d284-147">SIPResponseMetaData-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-147">SIPResponseMetaData table in Lync Server 2013</span></span>](lync-server-2013-sipresponsemetadata-table.md)

  - [<span data-ttu-id="7d284-148">Tabelle "Syndikator" in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-148">Syndicators table in Lync Server 2013</span></span>](lync-server-2013-syndicators-table.md)

  - [<span data-ttu-id="7d284-149">SyndicatorsTenantMap-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-149">SyndicatorsTenantMap table in Lync Server 2013</span></span>](lync-server-2013-syndicatorstenantmap-table.md)

  - [<span data-ttu-id="7d284-150">Aufgaben Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-150">Task table in Lync Server 2013</span></span>](lync-server-2013-task-table.md)

  - [<span data-ttu-id="7d284-151">Tenants-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-151">Tenants table in Lync Server 2013</span></span>](lync-server-2013-tenants-table.md)

  - [<span data-ttu-id="7d284-152">UriTypes-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-152">UriTypes table in Lync Server 2013</span></span>](lync-server-2013-uritypes-table.md)

  - [<span data-ttu-id="7d284-153">Users-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-153">Users table in Lync Server 2013</span></span>](lync-server-2013-users-table.md)

  - [<span data-ttu-id="7d284-154">UserAgentDef-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-154">UserAgentDef table in Lync Server 2013</span></span>](lync-server-2013-useragentdef-table.md)

  - [<span data-ttu-id="7d284-155">UserStatistics-Tabelle in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-155">UserStatistics table in Lync Server 2013</span></span>](lync-server-2013-userstatistics-table.md)

  - [<span data-ttu-id="7d284-156">VoipDetails-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7d284-156">VoipDetails table in Lync Server 2013</span></span>](lync-server-2013-voipdetails-table.md)

<span data-ttu-id="7d284-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7d284-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

