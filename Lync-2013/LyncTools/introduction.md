---
title: Einführung
description: Einführung in.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Introduction
ms:assetid: 276395be-93df-4a16-97e2-cb468cd0f2e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945588(v=OCS.15)
ms:contentKeyID: 51541414
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8eb847c499bde077ccaf2aa050de801ceeedcc6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438743"
---
# <a name="introduction"></a><span data-ttu-id="cf13d-103">Einführung</span><span class="sxs-lookup"><span data-stu-id="cf13d-103">Introduction</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cf13d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cf13d-104">

<span> </span></span></span>

<span data-ttu-id="cf13d-105">_**Letztes Änderungsdatum des Themas:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="cf13d-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="cf13d-106">Das lync Server 2013-Tool Stress und Leistung (als LyncPerfTool bezeichnet) kann die Benutzerauslastung der folgenden Typen simulieren:</span><span class="sxs-lookup"><span data-stu-id="cf13d-106">The Lync Server 2013 Stress and Performance Tool (referred to as LyncPerfTool) can simulate user load of the following types:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf13d-107">Instant Messaging (im) und Anwesenheitsinformationen</span><span class="sxs-lookup"><span data-stu-id="cf13d-107">Instant messaging (IM) and presence</span></span></p></td>
<td><p><span data-ttu-id="cf13d-108">Audiokonferenz</span><span class="sxs-lookup"><span data-stu-id="cf13d-108">Audio conferencing</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf13d-109">Anwendungsfreigabe</span><span class="sxs-lookup"><span data-stu-id="cf13d-109">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="cf13d-110">VoIP (Voice over IP), einschließlich der PSTN-Simulation (Public Switched Telephone Network)</span><span class="sxs-lookup"><span data-stu-id="cf13d-110">Voice over IP (VoIP), including public switched telephone network (PSTN) simulation</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf13d-111">Web Access-Client Konferenzen</span><span class="sxs-lookup"><span data-stu-id="cf13d-111">Web Access Client conferencing</span></span></p></td>
<td><p><span data-ttu-id="cf13d-112">Microsoft lync 2013 Attendant</span><span class="sxs-lookup"><span data-stu-id="cf13d-112">Microsoft Lync 2013 Attendant</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf13d-113">Reaktionsgruppen</span><span class="sxs-lookup"><span data-stu-id="cf13d-113">Response Groups</span></span></p></td>
<td><p><span data-ttu-id="cf13d-114">Erweiterung der Verteilerliste</span><span class="sxs-lookup"><span data-stu-id="cf13d-114">Distribution list expansion</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf13d-115">Adressbuch Download und Adressbuch Abfrage</span><span class="sxs-lookup"><span data-stu-id="cf13d-115">Address book download and address book query</span></span></p></td>
<td><p><span data-ttu-id="cf13d-116">Erweiterte 9-1-1 (E9-1-1)-Anrufe und Standortprofil (Wählplan)</span><span class="sxs-lookup"><span data-stu-id="cf13d-116">Enhanced 9-1-1 (E9-1-1) calls and location profile (dial plan)</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf13d-117">MultiView</span><span class="sxs-lookup"><span data-stu-id="cf13d-117">MultiView</span></span></p></td>
<td><p><span data-ttu-id="cf13d-118">Anzeigen mehrerer Datenströme aus einer Konferenz</span><span class="sxs-lookup"><span data-stu-id="cf13d-118">Viewing multiple streams from a conference</span></span></p></td>
</tr>
<tr class="odd">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="cf13d-119">Das Stress-und Leistungs Tool von lync Server 2013 unterstützt die Generierung und Föderations übergreifendes Laden von Datenpools über erweiterte Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="cf13d-119">The Lync Server 2013 Stress and Performance Tool supports cross-pool load generation and federation through advanced configuration only.</span></span>

<span data-ttu-id="cf13d-120">Das Tool simuliert auch keine Benutzerauslastung für die folgenden Clients:</span><span class="sxs-lookup"><span data-stu-id="cf13d-120">The tool also does not simulate user load for the following clients:</span></span>

  - <span data-ttu-id="cf13d-121">Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="cf13d-121">Office Live Meeting 2007</span></span>

  - <span data-ttu-id="cf13d-122">Lync 2013-beständiger Chat</span><span class="sxs-lookup"><span data-stu-id="cf13d-122">Lync 2013 Persistent Chat</span></span>

<span data-ttu-id="cf13d-123">Infolgedessen unterstützt das lync Server 2013-Tool Stress und Leistung das Testen der folgenden Komponenten nicht:</span><span class="sxs-lookup"><span data-stu-id="cf13d-123">As a result, the Lync Server 2013 Stress and Performance Tool will not support testing the following components:</span></span>

  - <span data-ttu-id="cf13d-124">Lync 2013-beständiger Chat</span><span class="sxs-lookup"><span data-stu-id="cf13d-124">Lync 2013 Persistent Chat</span></span>

  - <span data-ttu-id="cf13d-125">Exchange-Integrationsszenarien</span><span class="sxs-lookup"><span data-stu-id="cf13d-125">Exchange integration scenarios</span></span>

<div>

## <a name="applications-and-files-included-with-the-lync-server-2013-stress-and-performance-tool"></a><span data-ttu-id="cf13d-126">Im Lieferumfang des lync Server 2013-Tools für Stress und Leistung enthaltene Anwendungen und Dateien</span><span class="sxs-lookup"><span data-stu-id="cf13d-126">Applications and Files Included with the Lync Server 2013 Stress and Performance Tool</span></span>

<span data-ttu-id="cf13d-127">Die folgenden Anwendungen sind im Stress-und Leistungs Tool von lync Server 2013 enthalten:</span><span class="sxs-lookup"><span data-stu-id="cf13d-127">The following applications are included in the Lync Server 2013 Stress and Performance Tool:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="cf13d-128">Tool</span><span class="sxs-lookup"><span data-stu-id="cf13d-128">Tool</span></span></th>
<th><span data-ttu-id="cf13d-129">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="cf13d-129">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="cf13d-130">UserProvisioningTool.exe</span><span class="sxs-lookup"><span data-stu-id="cf13d-130">UserProvisioningTool.exe</span></span></p></td>
<td><p><span data-ttu-id="cf13d-131">Das lync Server 2013-Bereitstellungstool für Benutzer.</span><span class="sxs-lookup"><span data-stu-id="cf13d-131">The Lync Server 2013 User Provisioning tool.</span></span> <span data-ttu-id="cf13d-132">Dieses Tool dient zum Erstellen von Benutzern und Kontakten.</span><span class="sxs-lookup"><span data-stu-id="cf13d-132">This tool is used to create users and contacts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf13d-133">UserProfileGenerator.exe</span><span class="sxs-lookup"><span data-stu-id="cf13d-133">UserProfileGenerator.exe</span></span></p></td>
<td><p><span data-ttu-id="cf13d-134">Das lync Server 2013 Load Configuration Tool.</span><span class="sxs-lookup"><span data-stu-id="cf13d-134">The Lync Server 2013 Load Configuration Tool.</span></span> <span data-ttu-id="cf13d-135">Dieses Tool dient zum Konfigurieren der Eigenschaften der Benutzerauslastung, die simuliert werden soll.</span><span class="sxs-lookup"><span data-stu-id="cf13d-135">This tool is used to configure the characteristics of the user load to simulate.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf13d-136">LyncPerfTool.exe</span><span class="sxs-lookup"><span data-stu-id="cf13d-136">LyncPerfTool.exe</span></span></p></td>
<td><p><span data-ttu-id="cf13d-137">Das lync Server 2013-Tool für Stress und Leistung.</span><span class="sxs-lookup"><span data-stu-id="cf13d-137">The Lync Server 2013 Stress and Performance Tool.</span></span> <span data-ttu-id="cf13d-138">LyncPerfTool ist das Tool, das die Benutzerauslastung simuliert.</span><span class="sxs-lookup"><span data-stu-id="cf13d-138">LyncPerfTool is the tool that simulates the user load.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="cf13d-139">Standard. TMX</span><span class="sxs-lookup"><span data-stu-id="cf13d-139">Default.tmx</span></span></p></td>
<td><p><span data-ttu-id="cf13d-140">Standard. TMX ist erforderlich, um das lync Server 2013-Protokollierungs Tool zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="cf13d-140">Default.tmx is required to use the Lync Server 2013 Logging Tool.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="cf13d-141">Beispiele für Bereitstellungsskripts</span><span class="sxs-lookup"><span data-stu-id="cf13d-141">Example provisioning scripts</span></span></p></td>
<td><p><span data-ttu-id="cf13d-142">Diese Beispiele werden verwendet, um die Topologie für die Ausführung von Auslastungstests basierend auf bestimmten Szenarien zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="cf13d-142">These examples are used to configure the topology for running load tests, based on specific scenarios</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="cf13d-143">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cf13d-143">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

