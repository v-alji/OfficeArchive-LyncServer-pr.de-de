---
title: 'Lync Server 2013: Schema Klassen und Beschreibungen'
description: 'Lync Server 2013: Schema Klassen und Beschreibungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Schema classes and descriptions
ms:assetid: 7d43b920-ac37-40cc-adfe-be289bda6e9e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398625(v=OCS.15)
ms:contentKeyID: 48184612
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ec27c2e00a7f969dbc13c91b06313c8045894a9e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441970"
---
# <a name="schema-classes-and-descriptions-in-lync-server-2013"></a><span data-ttu-id="0c83e-103">Schema Klassen und Beschreibungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0c83e-103">Schema classes and descriptions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0c83e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0c83e-104">

<span> </span></span></span>

<span data-ttu-id="0c83e-105">_**Letztes Änderungsdatum des Themas:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="0c83e-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="0c83e-106">In diesem Abschnitt werden alle von lync Server 2013 verwendeten Schemaklassen beschrieben.</span><span class="sxs-lookup"><span data-stu-id="0c83e-106">This section describes all the schema classes used by Lync Server 2013.</span></span>

<div>

## <a name="schema-classes-and-descriptions"></a><span data-ttu-id="0c83e-107">Schema Klassen und Beschreibungen</span><span class="sxs-lookup"><span data-stu-id="0c83e-107">Schema Classes and Descriptions</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="0c83e-108">Klasse</span><span class="sxs-lookup"><span data-stu-id="0c83e-108">Class</span></span></th>
<th><span data-ttu-id="0c83e-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="0c83e-109">Description</span></span></th>
<th><span data-ttu-id="0c83e-110">Kommentare</span><span class="sxs-lookup"><span data-stu-id="0c83e-110">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-111">Mail-Recipient</span><span class="sxs-lookup"><span data-stu-id="0c83e-111">Mail-Recipient</span></span></p></td>
<td><p><span data-ttu-id="0c83e-112">Exchange Unified Messaging (um)-e-Mail-Empfänger.</span><span class="sxs-lookup"><span data-stu-id="0c83e-112">Exchange Unified Messaging (UM) email recipient.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-113">Diese Auxiliary-Klasse wird für Exchange um freigegeben.</span><span class="sxs-lookup"><span data-stu-id="0c83e-113">This auxiliary class is shared with Exchange UM.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-114">Attribut msRTCSIP-ApplicationContacts</span><span class="sxs-lookup"><span data-stu-id="0c83e-114">msRTCSIP-ApplicationContacts</span></span></p></td>
<td><p><span data-ttu-id="0c83e-115">Diese Klasse ist ein Container für mehrere Anwendungskontakte und enthält keine Attribute selbst.</span><span class="sxs-lookup"><span data-stu-id="0c83e-115">This class is a container for multiple application contacts and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-116">Neu in Microsoft Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="0c83e-116">New in Microsoft Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-117">Attribut msRTCSIP-ApplicationServer</span><span class="sxs-lookup"><span data-stu-id="0c83e-117">msRTCSIP-ApplicationServer</span></span></p></td>
<td><p><span data-ttu-id="0c83e-118">Diese Klasse enthält den Eintrag für den Dienst Kontrollpunkt für eine Instanz von Unified Communications Application Services (UCAS).</span><span class="sxs-lookup"><span data-stu-id="0c83e-118">This class holds the entry for the service control point for an instance of Unified Communications Application Services (UCAS).</span></span></p></td>
<td><p><span data-ttu-id="0c83e-119">Neu in Office Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="0c83e-119">New in Office Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-120">Attribut msRTCSIP-ApplicationServerService</span><span class="sxs-lookup"><span data-stu-id="0c83e-120">msRTCSIP-ApplicationServerService</span></span></p></td>
<td><p><span data-ttu-id="0c83e-121">Diese Klasse stellt eine Zuordnung von einem bestimmten Pool zu seinem Anwendungsdienst bereit.</span><span class="sxs-lookup"><span data-stu-id="0c83e-121">This class provides an association from a specific pool to its Application service.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-122">Neu in Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="0c83e-122">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-123">Attribut msRTCSIP-ApplicationServerSettings</span><span class="sxs-lookup"><span data-stu-id="0c83e-123">msRTCSIP-ApplicationServerSettings</span></span></p></td>
<td><p><span data-ttu-id="0c83e-124">Diese Auxiliary-Klasse für Attribut msRTCSIP-ApplicationServer enthält Attribute, die Einstellungen für Instanzen des Anwendungsdiensts darstellen.</span><span class="sxs-lookup"><span data-stu-id="0c83e-124">This auxiliary class to msRTCSIP-ApplicationServer holds attributes representing settings for instances of the Application service.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-125">Neu in Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="0c83e-125">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-126">Attribut msRTCSIP-Archiv (veraltet)</span><span class="sxs-lookup"><span data-stu-id="0c83e-126">msRTCSIP-Archive (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="0c83e-127">Diese Auxiliary-Klasse für Attribut msRTCSIP-Global Container enthält alle Einstellungen im Zusammenhang mit der Archivierung.</span><span class="sxs-lookup"><span data-stu-id="0c83e-127">This auxiliary class to msRTCSIP-GlobalContainer holds all settings related to archiving.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-128">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="0c83e-128">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-129">Attribut msRTCSIP-ArchivingServer (veraltet)</span><span class="sxs-lookup"><span data-stu-id="0c83e-129">msRTCSIP-ArchivingServer (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="0c83e-130">Diese Klasse stellt einen einzelnen Instant Messaging-Archivierungs Server dar.</span><span class="sxs-lookup"><span data-stu-id="0c83e-130">This class represents a single instant messaging Archiving Server.</span></span> <span data-ttu-id="0c83e-131">Eine Instanz dieser Klasse wird erstellt, wenn ein Computer als Instant Messaging-Archivierungs Server aktiviert wird, beispielsweise einen Computer, auf dem der Instant Messaging-Archivierungsdienst installiert ist.</span><span class="sxs-lookup"><span data-stu-id="0c83e-131">An instance of this class is created when a computer is activated as an instant messaging Archiving Server, such as a computer with the Instant Messaging Archiving service installed.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-132">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="0c83e-132">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-133">Attribut msRTCSIP-ConferenceDirectories</span><span class="sxs-lookup"><span data-stu-id="0c83e-133">msRTCSIP-ConferenceDirectories</span></span></p></td>
<td><p><span data-ttu-id="0c83e-134">Diese Klasse ist ein Container für mehrere Instanzen von Konferenz Verzeichnissen und enthält keine Attribute selbst.</span><span class="sxs-lookup"><span data-stu-id="0c83e-134">This class is a container for multiple instances of conference directories and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-135">Neu in Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="0c83e-135">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-136">Attribut msRTCSIP-ConferenceDirectory</span><span class="sxs-lookup"><span data-stu-id="0c83e-136">msRTCSIP-ConferenceDirectory</span></span></p></td>
<td><p><span data-ttu-id="0c83e-137">Diese Klasse enthält Attribute, die Einstellungen für ein bestimmtes Konferenzverzeichnis darstellen.</span><span class="sxs-lookup"><span data-stu-id="0c83e-137">This class holds attributes representing settings for a specific conference directory.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-138">Neu in Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="0c83e-138">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-139">Attribut msRTCSIP-ConnectionPoint</span><span class="sxs-lookup"><span data-stu-id="0c83e-139">msRTCSIP-ConnectionPoint</span></span></p></td>
<td><p><span data-ttu-id="0c83e-140">Generic Service Control Point (SCP), um den Computer als einen Server mit lync Server festzulegen.</span><span class="sxs-lookup"><span data-stu-id="0c83e-140">Generic service control point (SCP) to specify the computer as a server running Lync Server.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-141">Neu in lync 2010.</span><span class="sxs-lookup"><span data-stu-id="0c83e-141">New in Lync 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-142">Attribut msRTCSIP-DefaultCWABank</span><span class="sxs-lookup"><span data-stu-id="0c83e-142">msRTCSIP-DefaultCWABank</span></span></p></td>
<td><p><span data-ttu-id="0c83e-143">Diese Auxiliary-Klasse enthält die Einstellungen für eine Microsoft lync Web App-Bank.</span><span class="sxs-lookup"><span data-stu-id="0c83e-143">This auxiliary class holds the settings for a Microsoft Lync Web App bank.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-144">Neu in Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="0c83e-144">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-145">Attribut msRTCSIP-Domäne</span><span class="sxs-lookup"><span data-stu-id="0c83e-145">msRTCSIP-Domain</span></span></p></td>
<td><p><span data-ttu-id="0c83e-146">Diese Klasse enthält Attribute, die die konfigurierten Domänen der SIP-Registrierungsstelle definieren.</span><span class="sxs-lookup"><span data-stu-id="0c83e-146">This class holds attributes that define the configured domains of the SIP Registrar.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-147">Attribut msRTCSIP-EdgeProxy</span><span class="sxs-lookup"><span data-stu-id="0c83e-147">msRTCSIP-EdgeProxy</span></span></p></td>
<td><p><span data-ttu-id="0c83e-148">Dieser Klassencontainer stellt einen einzelnen Access-Edgedienst dar.</span><span class="sxs-lookup"><span data-stu-id="0c83e-148">This class container represents a single Access Edge service.</span></span> <span data-ttu-id="0c83e-149">Da ein Access-Edgedienst im Umkreisnetzwerk bereitgestellt wird und Kunden in der Regel keinen Zugriff auf Active Directory-Domänendienste aus dem Umkreisnetzwerk zulassen, sind Instanzen des Access-Edgedienst nicht dem Active Directory-Netzwerk des Intranets beigetreten.</span><span class="sxs-lookup"><span data-stu-id="0c83e-149">Because an Access Edge service is deployed in the perimeter network and customers usually do not allow Active Directory Domain Services access from the perimeter network, instances of Access Edge service are not joined to the intranet’s Active Directory network.</span></span> <span data-ttu-id="0c83e-150">Daher werden Zugriffsproxys nicht automatisch in AD DS registriert.</span><span class="sxs-lookup"><span data-stu-id="0c83e-150">Therefore, Access Proxies are not automatically registered in AD DS.</span></span> <span data-ttu-id="0c83e-151">Der Administrator muss das vorhanden sein jeder Instanz von Access Edge Service in AD DS manuell konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="0c83e-151">The administrator must manually configure the existence of each instance of Access Edge service in AD DS.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-152">Attribut msRTCSIP-EnterpriseMCUSettings</span><span class="sxs-lookup"><span data-stu-id="0c83e-152">msRTCSIP-EnterpriseMCUSettings</span></span></p></td>
<td><p><span data-ttu-id="0c83e-153">Diese Erweiterungsklasse für Attribut msRTCSIP-MCU enthält Attribute, die Einstellungen für Konferenzserver darstellen.</span><span class="sxs-lookup"><span data-stu-id="0c83e-153">This auxiliary class to msRTCSIP-MCU holds attributes representing settings for Conferencing servers.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-154">Neu in Microsoft Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0c83e-154">New in Microsoft Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-155">Attribut msRTCSIP-EnterpriseMediationServerSettings</span><span class="sxs-lookup"><span data-stu-id="0c83e-155">msRTCSIP-EnterpriseMediationServerSettings</span></span></p></td>
<td><p><span data-ttu-id="0c83e-156">Diese Auxiliary-Klasse für Attribut msRTCSIP-MediationServer enthält Attribute, die Einstellungen für Vermittlungsserver darstellen.</span><span class="sxs-lookup"><span data-stu-id="0c83e-156">This auxiliary class to msRTCSIP-MediationServer holds attributes representing settings for Mediation Servers.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-157">Neu in Office Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0c83e-157">New in Office Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-158">Attribut msRTCSIP-EnterpriseServerSettings</span><span class="sxs-lookup"><span data-stu-id="0c83e-158">msRTCSIP-EnterpriseServerSettings</span></span></p></td>
<td><p><span data-ttu-id="0c83e-159">Diese Auxiliary-Klasse für Attribut msRTCSIP-Server enthält Attribute, die Einstellungen für SIP-Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="0c83e-159">This auxiliary class to msRTCSIP-Server holds attributes representing settings for SIP servers.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-160">Attribut msRTCSIP-Federation</span><span class="sxs-lookup"><span data-stu-id="0c83e-160">msRTCSIP-Federation</span></span></p></td>
<td><p><span data-ttu-id="0c83e-161">Diese Auxiliary-Klasse für Attribut msRTCSIP-Global Container enthält alle Einstellungen, die sich auf den Verbund beziehen.</span><span class="sxs-lookup"><span data-stu-id="0c83e-161">This auxiliary class to msRTCSIP-GlobalContainer holds all settings related to federation.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-162">Attribut msRTCSIP-Global Container</span><span class="sxs-lookup"><span data-stu-id="0c83e-162">msRTCSIP-GlobalContainer</span></span></p></td>
<td><p><span data-ttu-id="0c83e-163">Diese Klasse enthält alle Einstellungen, die in einer lync Server-Bereitstellung gelten.</span><span class="sxs-lookup"><span data-stu-id="0c83e-163">This class holds all settings that apply throughout a Lync Server deployment.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-164">Attribut msRTCSIP-GlobalUserPolicy (veraltet)</span><span class="sxs-lookup"><span data-stu-id="0c83e-164">msRTCSIP-GlobalUserPolicy (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="0c83e-165">Diese Klasse stellt eine einzelne Office Communications Server-Besprechungsrichtlinie dar.</span><span class="sxs-lookup"><span data-stu-id="0c83e-165">This class represents a single Office Communications Server meeting policy.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-166">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="0c83e-166">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-167">Attribut msRTCSIP-GlobalTopologySetting</span><span class="sxs-lookup"><span data-stu-id="0c83e-167">msRTCSIP-GlobalTopologySetting</span></span></p></td>
<td><p><span data-ttu-id="0c83e-168">Das Setting-Objekt der lokalen globalen Topologie.</span><span class="sxs-lookup"><span data-stu-id="0c83e-168">The local global topology setting object.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-169">Neu in lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="0c83e-169">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-170">Attribut msRTCSIP-GlobalTopologySettings</span><span class="sxs-lookup"><span data-stu-id="0c83e-170">msRTCSIP-GlobalTopologySettings</span></span></p></td>
<td><p><span data-ttu-id="0c83e-171">Container, in dem globale Topologie-Einstellungsobjekte enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="0c83e-171">Container to hold global topology setting objects.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-172">Neu in lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="0c83e-172">New in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-173">Attribut msRTCSIP-LocalNormalization</span><span class="sxs-lookup"><span data-stu-id="0c83e-173">msRTCSIP-LocalNormalization</span></span></p></td>
<td><p><span data-ttu-id="0c83e-174">Diese Klasse ist ein Container, der eine Instanz einer Standort Normalisierungsregel darstellt.</span><span class="sxs-lookup"><span data-stu-id="0c83e-174">This class is a container that represents an instance of a location normalization rule.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-175">Attribut msRTCSIP-LocationContactMapping</span><span class="sxs-lookup"><span data-stu-id="0c83e-175">msRTCSIP-LocationContactMapping</span></span></p></td>
<td><p><span data-ttu-id="0c83e-176">Diese Klasse wird von der Conferencing Attendant-Anwendung erstellt und enthält Attribute, mit denen Konferenz Telefonnummern nach Regionen kategorisiert werden.</span><span class="sxs-lookup"><span data-stu-id="0c83e-176">This class is created by the Conferencing Attendant application and holds attributes used to categorize conference telephone numbers by region.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-177">Neu in Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="0c83e-177">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-178">Attribut msRTCSIP-LocationContactMappings</span><span class="sxs-lookup"><span data-stu-id="0c83e-178">msRTCSIP-LocationContactMappings</span></span></p></td>
<td><p><span data-ttu-id="0c83e-179">Diese Klasse ist ein Container für mehrere Instanzen von Standortkontaktzuordnungen und enthält keine Attribute selbst.</span><span class="sxs-lookup"><span data-stu-id="0c83e-179">This class is a container for multiple instances of location contact mappings and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-180">Neu in Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="0c83e-180">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-181">Attribut msRTCSIP-LocationProfile</span><span class="sxs-lookup"><span data-stu-id="0c83e-181">msRTCSIP-LocationProfile</span></span></p></td>
<td><p><span data-ttu-id="0c83e-182">Diese Klasse ist ein Container, der ein bestimmtes Standortprofil darstellt.</span><span class="sxs-lookup"><span data-stu-id="0c83e-182">This class is a container that represents a specific location profile.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-183">Attribut msRTCSIP-LocationProfiles (veraltet)</span><span class="sxs-lookup"><span data-stu-id="0c83e-183">msRTCSIP-LocationProfiles (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="0c83e-184">Diese Klasse ist ein Container für mehrere Standortprofile und enthält keine Attribute selbst.</span><span class="sxs-lookup"><span data-stu-id="0c83e-184">This class is a container for multiple location profiles and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-185">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="0c83e-185">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-186">Attribut msRTCSIP-LocalNormalizations (veraltet)</span><span class="sxs-lookup"><span data-stu-id="0c83e-186">msRTCSIP-LocalNormalizations (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="0c83e-187">Diese Klasse ist ein Container für mehrere lokale Normalisierungsregeln und enthält keine Attribute selbst.</span><span class="sxs-lookup"><span data-stu-id="0c83e-187">This class is a container for multiple local normalization rules and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-188">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="0c83e-188">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-189">Attribut msRTCSIP-MCU</span><span class="sxs-lookup"><span data-stu-id="0c83e-189">msRTCSIP-MCU</span></span></p></td>
<td><p><span data-ttu-id="0c83e-190">Diese Klasse stellt einen einzelnen Konferenzserver dar.</span><span class="sxs-lookup"><span data-stu-id="0c83e-190">This class represents a single Conferencing server.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-191">Neu in Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0c83e-191">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-192">Attribut msRTCSIP-MCUFactories</span><span class="sxs-lookup"><span data-stu-id="0c83e-192">msRTCSIP-MCUFactories</span></span></p></td>
<td><p><span data-ttu-id="0c83e-193">Diese Klasse enthält mehrere Attribut msRTCSIP-MCUFactory-Klassen und besitzt keine Attribute selbst.</span><span class="sxs-lookup"><span data-stu-id="0c83e-193">This class holds multiple msRTCSIP-MCUFactory classes and does not have attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-194">Neu in Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0c83e-194">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-195">Attribut msRTCSIP-MCUFactory</span><span class="sxs-lookup"><span data-stu-id="0c83e-195">msRTCSIP-MCUFactory</span></span></p></td>
<td><p><span data-ttu-id="0c83e-196">Bei dieser Klasse handelt es sich um einen Container, der eine Konferenz Server Factory für einen einzelnen Medientyp darstellt.</span><span class="sxs-lookup"><span data-stu-id="0c83e-196">This class is a container representing a Conferencing Server Factory for a single medium type.</span></span> <span data-ttu-id="0c83e-197">Eine Instanz dieser Klasse wird erstellt, wenn der erste Konferenzserver für diesen bestimmten Typ und Lieferanten aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="0c83e-197">An instance of this class is created when the first Conferencing server for this particular type and vendor is activated.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-198">Neu in Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0c83e-198">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-199">Attribut msRTCSIP-MCUFactoryService</span><span class="sxs-lookup"><span data-stu-id="0c83e-199">msRTCSIP-MCUFactoryService</span></span></p></td>
<td><p><span data-ttu-id="0c83e-200">Diese Klasse stellt eine Zuordnung von einem bestimmten Pool zu seiner Konferenz Server Factory bereit.</span><span class="sxs-lookup"><span data-stu-id="0c83e-200">This class provides an association from a specific pool to its Conferencing Server Factory.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-201">Neu in Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0c83e-201">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-202">Attribut msRTCSIP-MediationServer</span><span class="sxs-lookup"><span data-stu-id="0c83e-202">msRTCSIP-MediationServer</span></span></p></td>
<td><p><span data-ttu-id="0c83e-203">Diese Klasse enthält den Eintrag für den Dienst Kontrollpunkt für einen Vermittlungs Server.</span><span class="sxs-lookup"><span data-stu-id="0c83e-203">This class holds the entry for the service control point for a Mediation Server.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-204">Neu in Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0c83e-204">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-205">Attribut msRTCSIP-Besprechung (veraltet)</span><span class="sxs-lookup"><span data-stu-id="0c83e-205">msRTCSIP-Meeting (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="0c83e-206">Diese Auxiliary-Klasse für Attribut msRTCSIP-Global Container enthält Attribute, die konfigurierbare Besprechungseinstellungen darstellen.</span><span class="sxs-lookup"><span data-stu-id="0c83e-206">This auxiliary class to msRTCSIP-GlobalContainer holds attributes representing configurable meeting settings.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-207">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="0c83e-207">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-208">Attribut msRTCSIP – Mobilität</span><span class="sxs-lookup"><span data-stu-id="0c83e-208">msRTCSIP-Mobility</span></span></p></td>
<td><p><span data-ttu-id="0c83e-209">Container, in dem die globalen Mobilitätseinstellungen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="0c83e-209">Container that stores the global mobility settings.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-210">Attribut msRTCSIP-MonitoringServer</span><span class="sxs-lookup"><span data-stu-id="0c83e-210">msRTCSIP-MonitoringServer</span></span></p></td>
<td><p><span data-ttu-id="0c83e-211">Diese Klasse enthält Attribute, die Einstellungen für einen einzelnen Überwachungs Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="0c83e-211">This class holds attributes that represent settings for a single Monitoring Server.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-212">Neu in Communications Server 2007 R2.</span><span class="sxs-lookup"><span data-stu-id="0c83e-212">New in Communications Server 2007 R2.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-213">Attribut msRTCSIP-PhoneRoute (veraltet)</span><span class="sxs-lookup"><span data-stu-id="0c83e-213">msRTCSIP-PhoneRoute (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="0c83e-214">Bei dieser Klasse handelt es sich um einen Container, der eine Instanz einer Least Cost-Route zu einem Gateway oder einer Gruppe von Gateways darstellt.</span><span class="sxs-lookup"><span data-stu-id="0c83e-214">This class is a container representing an instance of a least cost route to a gateway or set of gateways.</span></span> <span data-ttu-id="0c83e-215">Diese Informationen werden von allen Enterprise-Pools oder Servern mit Standard Edition verwendet, um ausgehende Anrufe auf die kostengünstigste Weise an das öffentlich geschaltete Telefonnetz (PSTN) weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="0c83e-215">This information is used by all Enterprise pools or servers running Standard Edition to route outgoing calls to the public switched telephone network (PSTN) in the most cost effective way.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-216">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="0c83e-216">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-217">Attribut msRTCSIP-PhoneRoutes (veraltet)</span><span class="sxs-lookup"><span data-stu-id="0c83e-217">msRTCSIP-PhoneRoutes (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="0c83e-218">Diese Klasse ist ein Container für mehrere, kostengünstigste Routen und enthält keine Attribute selbst.</span><span class="sxs-lookup"><span data-stu-id="0c83e-218">This class is a container for multiple, least cost routes and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-219">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="0c83e-219">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-220">Attribut msRTCSIP-Richtlinien (veraltet)</span><span class="sxs-lookup"><span data-stu-id="0c83e-220">msRTCSIP-Policies (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="0c83e-221">Diese Klasse enthält mehrere lync Server-Richtlinien Klassen und hat keine Attribute selbst.</span><span class="sxs-lookup"><span data-stu-id="0c83e-221">This class holds multiple Lync Server policy classes and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-222">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="0c83e-222">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-223">Attribut msRTCSIP-Pool</span><span class="sxs-lookup"><span data-stu-id="0c83e-223">msRTCSIP-Pool</span></span></p></td>
<td><p><span data-ttu-id="0c83e-224">Diese Klasse stellt einen einzelnen lync Server-Pool dar.</span><span class="sxs-lookup"><span data-stu-id="0c83e-224">This class represents a single Lync Server pool.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-225">Attribut msRTCSIP-Pools</span><span class="sxs-lookup"><span data-stu-id="0c83e-225">msRTCSIP-Pools</span></span></p></td>
<td><p><span data-ttu-id="0c83e-226">Diese Klasse enthält mehrere lync Server-Pools und hat keine Attribute selbst.</span><span class="sxs-lookup"><span data-stu-id="0c83e-226">This class holds multiple Lync Server pools and does not have any attributes itself.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-227">Attribut msRTCSIP-PoolService</span><span class="sxs-lookup"><span data-stu-id="0c83e-227">msRTCSIP-PoolService</span></span></p></td>
<td><p><span data-ttu-id="0c83e-228">Diese Klasse stellt den Kontrollpunkt des Dienst Steuerelements pointservice eines Pools dar.</span><span class="sxs-lookup"><span data-stu-id="0c83e-228">This class represents the service control pointservice control point of a pool.</span></span> <span data-ttu-id="0c83e-229">Für Benutzer, die in einem Pool gehostet werden, wird Ihr Attribut msRTCSIP-PrimaryHomeServer-Attribut auf eine Instanz dieser Klasse verweisen.</span><span class="sxs-lookup"><span data-stu-id="0c83e-229">Users hosted on a pool have their msRTCSIP-PrimaryHomeServer attribute point to an instance of this class.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-230">Attribut msRTCSIP-Anwesenheitsinformationen</span><span class="sxs-lookup"><span data-stu-id="0c83e-230">msRTCSIP-Presence</span></span></p></td>
<td><p><span data-ttu-id="0c83e-231">Container, in dem die globalen Anwesenheitseinstellungen gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="0c83e-231">Container that stores the global presence settings.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-232">Attribut msRTCSIP-Registrar</span><span class="sxs-lookup"><span data-stu-id="0c83e-232">msRTCSIP-Registrar</span></span></p></td>
<td><p><span data-ttu-id="0c83e-233">Diese Hilfsklasse für Attribut msRTCSIP-Global Container enthält Attribute, die Benutzereinstellungen darstellen, die von den SIP-Registrierungs Servern verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="0c83e-233">This auxiliary class to msRTCSIP-GlobalContainer holds attributes representing user settings maintained by the SIP Registrar servers.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-234">Attribut msRTCSIP-RouteUsage (veraltet)</span><span class="sxs-lookup"><span data-stu-id="0c83e-234">msRTCSIP-RouteUsage (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="0c83e-235">Bei dieser Klasse handelt es sich um einen Container, der eine Instanz einer Telefonrouten Verwendung darstellt.</span><span class="sxs-lookup"><span data-stu-id="0c83e-235">This class is a container representing an instance of a phone route usage.</span></span> <span data-ttu-id="0c83e-236">Eine Telefonroute-Nutzungsklasse besteht aus einem Attributfeld und einem Beschreibungsfeld.</span><span class="sxs-lookup"><span data-stu-id="0c83e-236">A phone route usage class consists of an attribute field and a description field.</span></span> <span data-ttu-id="0c83e-237">Das Attributfeld definiert einen Verwendungstyp.</span><span class="sxs-lookup"><span data-stu-id="0c83e-237">The attribute field defines a usage type.</span></span> <span data-ttu-id="0c83e-238">Im Feld Beschreibung können Administratoren die Verwendung dieses Attributs auf der Telefonroute beschreiben.</span><span class="sxs-lookup"><span data-stu-id="0c83e-238">The description field allows administrators to describe the usage for this attribute in the phone route.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-239">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="0c83e-239">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-240">Attribut msRTCSIP-RouteUsages (veraltet)</span><span class="sxs-lookup"><span data-stu-id="0c83e-240">msRTCSIP-RouteUsages (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="0c83e-241">Diese Klasse enthält mehrere Instanzen der Attribut msRTCSIP-RouteUsage-Klasse und hat keine Attribute selbst.</span><span class="sxs-lookup"><span data-stu-id="0c83e-241">This class holds multiple instances of the msRTCSIP-RouteUsage class and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-242">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="0c83e-242">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-243">Attribut msRTCSIP-Suche</span><span class="sxs-lookup"><span data-stu-id="0c83e-243">msRTCSIP-Search</span></span></p></td>
<td><p><span data-ttu-id="0c83e-244">Diese Auxiliary-Klasse für Attribut msRTCSIP-Global Container enthält Attribute, die den Umfang der Suchergebnisse einschränken und steuern.</span><span class="sxs-lookup"><span data-stu-id="0c83e-244">This auxiliary class to msRTCSIP-GlobalContainer holds attributes that limit and control the scope of search results.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-245">Attribut msRTCSIP-Server</span><span class="sxs-lookup"><span data-stu-id="0c83e-245">msRTCSIP-Server</span></span></p></td>
<td><p><span data-ttu-id="0c83e-246">Diese Klasse steht für einen einzelnen Server, auf dem lync Server ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="0c83e-246">This class represents a single server running Lync Server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-247">Attribut msRTCSIP-Service</span><span class="sxs-lookup"><span data-stu-id="0c83e-247">msRTCSIP-Service</span></span></p></td>
<td><p><span data-ttu-id="0c83e-248">Diese Klasse enthält den Container für globale Einstellungen und Attribut msRTCSIP-Domänenobjekte.</span><span class="sxs-lookup"><span data-stu-id="0c83e-248">This class holds the global settings container and msRTCSIP-Domain objects.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-249">Attribut msRTCSIP-TrustedMCU</span><span class="sxs-lookup"><span data-stu-id="0c83e-249">msRTCSIP-TrustedMCU</span></span></p></td>
<td><p><span data-ttu-id="0c83e-250">Diese Klasse enthält Attribute, die Einstellungen für einen vertrauenswürdigen Konferenzserver darstellen.</span><span class="sxs-lookup"><span data-stu-id="0c83e-250">This class holds attributes that represent settings for a trusted Conferencing server.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-251">Neu in Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0c83e-251">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-252">Attribut msRTCSIP-TrustedMCUs</span><span class="sxs-lookup"><span data-stu-id="0c83e-252">msRTCSIP-TrustedMCUs</span></span></p></td>
<td><p><span data-ttu-id="0c83e-253">Diese Klasse enthält mehrere Instanzen der Attribut msRTCSIP-TrustedMCU-Klasse und hat keine Attribute selbst.</span><span class="sxs-lookup"><span data-stu-id="0c83e-253">This class holds multiple instances of the msRTCSIP-TrustedMCU class and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-254">Neu in Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0c83e-254">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-255">Attribut msRTCSIP-TrustedProxies</span><span class="sxs-lookup"><span data-stu-id="0c83e-255">msRTCSIP-TrustedProxies</span></span></p></td>
<td><p><span data-ttu-id="0c83e-256">Diese Klasse enthält mehrere Attribut msRTCSIP-TrustedProxy-Klassen und enthält keine Attribute selbst.</span><span class="sxs-lookup"><span data-stu-id="0c83e-256">This class holds multiple msRTCSIP-TrustedProxy classes and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-257">Neu in Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0c83e-257">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-258">Attribut msRTCSIP-TrustedProxy</span><span class="sxs-lookup"><span data-stu-id="0c83e-258">msRTCSIP-TrustedProxy</span></span></p></td>
<td><p><span data-ttu-id="0c83e-259">Diese Klasse ist ein Container, der einen Server mit Proxy Server darstellt.</span><span class="sxs-lookup"><span data-stu-id="0c83e-259">This class is a container representing a server running Proxy Server.</span></span> <span data-ttu-id="0c83e-260">Eine Instanz dieser Klasse wird erstellt, wenn ein neuer Proxy Server auf einem Computer aktiviert wird, der mit AD DS verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="0c83e-260">An instance of this class is created when activating a new Proxy Server on a computer joined to AD DS.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-261">Neu in Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0c83e-261">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-262">Attribut msRTCSIP-TrustedServer</span><span class="sxs-lookup"><span data-stu-id="0c83e-262">msRTCSIP-TrustedServer</span></span></p></td>
<td><p><span data-ttu-id="0c83e-263">Diese Klasse enthält Attribute, die Einstellungen für einen vertrauenswürdigen Server darstellen.</span><span class="sxs-lookup"><span data-stu-id="0c83e-263">This class holds attributes that represent settings for a trusted server.</span></span></p></td>
<td><p>-</p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-264">Attribut msRTCSIP-TrustedService</span><span class="sxs-lookup"><span data-stu-id="0c83e-264">msRTCSIP-TrustedService</span></span></p></td>
<td><p><span data-ttu-id="0c83e-265">Diese Klasse ist ein Container, der einen vertrauenswürdigen Dienst darstellt, der mithilfe einer Global routingfähigen Benutzer-Agent-URI-Adresse (GRUU) geroutet werden kann.</span><span class="sxs-lookup"><span data-stu-id="0c83e-265">This class is a container representing a trusted service that is routable using a Globally Routable User Agent URI (GRUU) address.</span></span> <span data-ttu-id="0c83e-266">Eine Instanz dieser Klasse wird erstellt, wenn ein neuer Server aktiviert wird, der von lync Server als vertrauenswürdig eingestuft wird.</span><span class="sxs-lookup"><span data-stu-id="0c83e-266">An instance of this class is created when a new server that is trusted by Lync Server is activated.</span></span> <span data-ttu-id="0c83e-267">Dieser vertrauenswürdige Server muss einer Active Directory-Domäne angehören.</span><span class="sxs-lookup"><span data-stu-id="0c83e-267">This trusted server must be joined to an Active Directory domain.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-268">Neu in Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0c83e-268">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-269">Attribut msRTCSIP-TrustedServices</span><span class="sxs-lookup"><span data-stu-id="0c83e-269">msRTCSIP-TrustedServices</span></span></p></td>
<td><p><span data-ttu-id="0c83e-270">Diese Klasse ist ein Container für mehrere GRUU-Server und enthält keine Attribute selbst.</span><span class="sxs-lookup"><span data-stu-id="0c83e-270">This class is a container for multiple GRUU servers and does not contain any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-271">Neu in Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0c83e-271">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-272">Attribut msRTCSIP-TrustedWebComponentsServer</span><span class="sxs-lookup"><span data-stu-id="0c83e-272">msRTCSIP-TrustedWebComponentsServer</span></span></p></td>
<td><p><span data-ttu-id="0c83e-273">Diese Klasse enthält Attribute, die die Einstellungen für eine vertrauenswürdige Webkomponente darstellen.</span><span class="sxs-lookup"><span data-stu-id="0c83e-273">This class holds attributes that represent the settings for a trusted web component.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-274">Neu in Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0c83e-274">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-275">Attribut msRTCSIP-TrustedWebComponentsServers</span><span class="sxs-lookup"><span data-stu-id="0c83e-275">msRTCSIP-TrustedWebComponentsServers</span></span></p></td>
<td><p><span data-ttu-id="0c83e-276">Diese Klasse enthält mehrere Instanzen der Attribut msRTCSIP-TrustedWebComponentServer-Klasse und hat keine Attribute selbst.</span><span class="sxs-lookup"><span data-stu-id="0c83e-276">This class holds multiple instances of the msRTCSIP-TrustedWebComponentServer class and does not have any attributes itself.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-277">Neu in Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0c83e-277">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-278">Attribut msRTCSIP-UnifiedCommunications (veraltet)</span><span class="sxs-lookup"><span data-stu-id="0c83e-278">msRTCSIP-UnifiedCommunications (obsolete)</span></span></p></td>
<td><p><span data-ttu-id="0c83e-279">Diese Auxiliary-Klasse für Attribut msRTCSIP-Global Container enthält Attribute, die sich auf Unified Communications beziehen.</span><span class="sxs-lookup"><span data-stu-id="0c83e-279">This auxiliary class to msRTCSIP-GlobalContainer holds attributes related to unified communications.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-280">In lync Server 2010 veraltet.</span><span class="sxs-lookup"><span data-stu-id="0c83e-280">Obsolete in Lync Server 2010.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-281">Attribut msRTCSIP-Webkomponenten</span><span class="sxs-lookup"><span data-stu-id="0c83e-281">msRTCSIP-WebComponents</span></span></p></td>
<td><p><span data-ttu-id="0c83e-282">Diese Klasse enthält den pointservice-Kontrollpunkt für Dienst Steuerelemente für Internet Information Server (IIS).</span><span class="sxs-lookup"><span data-stu-id="0c83e-282">This class holds the service control pointservice control point for Internet Information Server (IIS).</span></span> <span data-ttu-id="0c83e-283">Es identifiziert einen Server als Web Components-Server.</span><span class="sxs-lookup"><span data-stu-id="0c83e-283">It identifies a server as a web components server.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-284">Neu in Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0c83e-284">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="0c83e-285">Attribut msRTCSIP-WebComponentsService</span><span class="sxs-lookup"><span data-stu-id="0c83e-285">msRTCSIP-WebComponentsService</span></span></p></td>
<td><p><span data-ttu-id="0c83e-286">Diese Klasse stellt eine Zuordnung von einem bestimmten Pool zu den Webkomponenten bereit, die vom Pool verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="0c83e-286">This class provides an association from a specific pool to the web components that the pool will use.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-287">Neu in Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0c83e-287">New in Communications Server 2007.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="0c83e-288">Attribut msRTCSIP-WebComponentSettings</span><span class="sxs-lookup"><span data-stu-id="0c83e-288">msRTCSIP-WebComponentSettings</span></span></p></td>
<td><p><span data-ttu-id="0c83e-289">Diese zusätzliche Klasse für Attribut msRTCSIP-Webkomponenten enthält Attribute, die Einstellungen für Webkomponenten darstellen.</span><span class="sxs-lookup"><span data-stu-id="0c83e-289">This auxiliary class to msRTCSIP-WebComponents holds attributes representing settings for web components.</span></span></p></td>
<td><p><span data-ttu-id="0c83e-290">Neu in Communications Server 2007.</span><span class="sxs-lookup"><span data-stu-id="0c83e-290">New in Communications Server 2007.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="0c83e-291">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0c83e-291">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

