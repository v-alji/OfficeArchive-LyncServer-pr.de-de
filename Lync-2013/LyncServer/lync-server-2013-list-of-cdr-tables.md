---
title: 'Lync Server 2013: Liste der CDR-Tabellen'
description: 'Lync Server 2013: Liste der CDR-Tabellen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: List of CDR tables
ms:assetid: 031843fd-c7ff-4534-9b02-8847aad70807
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398084(v=OCS.15)
ms:contentKeyID: 48183254
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 21d0f683ffeb0f5f1cbba5db4c45d248aa14e8e4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426613"
---
# <a name="list-of-cdr-tables-in-lync-server-2013"></a><span data-ttu-id="daf50-103">Liste der CDR-Tabellen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="daf50-103">List of CDR tables in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="daf50-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="daf50-104">

<span> </span></span></span>

<span data-ttu-id="daf50-105">_**Letztes Änderungsdatum des Themas:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="daf50-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="daf50-106">Das Datenbankschema für die Anrufdetailaufzeichnung (CDR) besteht aus den folgenden Tabellen.</span><span class="sxs-lookup"><span data-stu-id="daf50-106">The call detail recording (CDR) database schema consists of the following tables.</span></span>

<div>

## <a name="static-tables"></a><span data-ttu-id="daf50-107">Statische Tabellen</span><span class="sxs-lookup"><span data-stu-id="daf50-107">Static Tables</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="daf50-108">Tabelle</span><span class="sxs-lookup"><span data-stu-id="daf50-108">Table</span></span></th>
<th><span data-ttu-id="daf50-109">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="daf50-109">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="daf50-110"><a href="lync-server-2013-callpriorities-table.md">CallPriorities-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-110"><a href="lync-server-2013-callpriorities-table.md">CallPriorities table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-111">Speichert die Liste möglicher Anruf Prioritäten wie Notfall, dringend, normal, nicht dringend und mehr.</span><span class="sxs-lookup"><span data-stu-id="daf50-111">Stores the list of possible call priorities, such as emergency, urgent, normal, non-urgent, and more.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-112"><a href="lync-server-2013-conferencejointimethresholds-table.md">ConferenceJoinTimeThresholds-Tabelle in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-112"><a href="lync-server-2013-conferencejointimethresholds-table.md">ConferenceJoinTimeThresholds table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-113">Speichert die Klassifizierungs Grenzen, die vom Zusammenfassungsbericht zur Konferenzteilnahme verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="daf50-113">Stores the classification boundaries used by the Conference Join Time Summary Report.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-114"><a href="lync-server-2013-deregistertype-table.md">DeRegisterType-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-114"><a href="lync-server-2013-deregistertype-table.md">DeRegisterType table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-115">Speichert die Liste der möglichen Benutzer Deregistrierungs Gründe, wie &quot; Client initiiert, &quot; &quot; Registrierung abgelaufen, &quot; &quot; Client Absturz &quot; und vieles mehr.</span><span class="sxs-lookup"><span data-stu-id="daf50-115">Stores the list of possible user de-register reasons, such as &quot;client initiated,&quot; &quot;registration expired,&quot; &quot;client crash,&quot; and more.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-116"><a href="lync-server-2013-medialist-table.md">MediaList-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-116"><a href="lync-server-2013-medialist-table.md">MediaList table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-117">Speichert die Liste der Medientypen, die Einträge in der Datenbank generieren können (beispielsweise Chat, Audio, Video und Dateiübertragung).</span><span class="sxs-lookup"><span data-stu-id="daf50-117">Stores the list of media types that can generate entries in the database (for example, IM, audio, video, and file transfer).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-118"><a href="lync-server-2013-purgesettings-table.md">PurgeSettings-Tabelle in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-118"><a href="lync-server-2013-purgesettings-table.md">PurgeSettings table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-119">Speichert Informationen, die angeben, ob (und wann) veraltete Anruf Detaildatensätze automatisch aus der CDR-Datenbank gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="daf50-119">Stores information that specifies if (and when) outdated call detail records will automatically be deleted from the CDR database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-120"><a href="lync-server-2013-roles-table.md">Roles-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-120"><a href="lync-server-2013-roles-table.md">Roles table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-121">Speichert die Liste möglicher Konferenz Rollen (beispielsweise Teilnehmer und Referenten).</span><span class="sxs-lookup"><span data-stu-id="daf50-121">Stores the list of possible conference roles (for example, attendee and presenter).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-122"><a href="lync-server-2013-sipresponsemetadata-table.md">SIPResponseMetaData-Tabelle in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-122"><a href="lync-server-2013-sipresponsemetadata-table.md">SIPResponseMetaData table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-123">Speichert eine Liste der SIP-Antwortcodes sowie die Klassifizierung und Definition der einzelnen Codes.</span><span class="sxs-lookup"><span data-stu-id="daf50-123">Stores a list of SIP response codes and the classification and definition of each of those codes.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="supporting-tables"></a><span data-ttu-id="daf50-124">Unterstützende Tabellen</span><span class="sxs-lookup"><span data-stu-id="daf50-124">Supporting Tables</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="daf50-125">Tabelle</span><span class="sxs-lookup"><span data-stu-id="daf50-125">Table</span></span></th>
<th><span data-ttu-id="daf50-126">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="daf50-126">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="daf50-127"><a href="lync-server-2013-clientversions-table.md">ClientVersions-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-127"><a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-128">Speichert die Clients (Clienttyp und Versionsnummer) jedes an einem Anruf beteiligten Clients mit Informationen, die in dieser Datenbank erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="daf50-128">Stores the clients (both client type and version number) of each client involved in a call with information captured in this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-129"><a href="lync-server-2013-conferenceuris-table.md">ConferenceUris-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-129"><a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-130">Speichert eine Liste der ConferenceURIs, die in konferenzbezogenen Anrufen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="daf50-130">Stores a list of ConferenceURIs that are used in conference related calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-131"><a href="lync-server-2013-contenttypes-table.md">ContentTypes-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-131"><a href="lync-server-2013-contenttypes-table.md">ContentTypes table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-132">Speichert eine Liste von SIP-Inhaltstypen (Session Initiation Protocol), die sowohl in Peer-to-Peer-Anrufen als auch in Konferenzgesprächen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="daf50-132">Stores a list of Session Initiation Protocol (SIP) content types that are used in both peer-to-peer calls and conference calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-133"><a href="lync-server-2013-devices-table.md">Devices-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-133"><a href="lync-server-2013-devices-table.md">Devices table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-134">Speichert eine Liste von Geräten, einschließlich deren Hersteller, Hardware Version und Mac-Adresse.</span><span class="sxs-lookup"><span data-stu-id="daf50-134">Stores a list of devices, including their manufacturer, hardware version, and MAC address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-135"><a href="lync-server-2013-dialogs-table.md">Dialogs-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-135"><a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-136">Speichert Informationen über die Dialog Feld-ID für jede Sitzung in der Datenbank.</span><span class="sxs-lookup"><span data-stu-id="daf50-136">Stores information about the Dialog ID for each session in the database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-137"><a href="lync-server-2013-edgeservers-table.md">EdgeServers-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-137"><a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-138">Speichert eine Liste der Edgeserver, die für externe Anrufe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="daf50-138">Stores a list of Edge Servers that are used for external calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-139"><a href="lync-server-2013-gateways-table.md">Gateways-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-139"><a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-140">Speichert eine Liste der Gateways, die für VoIP-Anrufe (Voice over Internet Protocol) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="daf50-140">Stores a list of Gateways that are used for Voice over Internet Protocol (VoIP) calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-141"><a href="lync-server-2013-hardwareversions-table.md">HardwareVersions-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-141"><a href="lync-server-2013-hardwareversions-table.md">HardwareVersions table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-142">Speichert eine Liste der Hardware Versionen von Geräten (Tischtelefon).</span><span class="sxs-lookup"><span data-stu-id="daf50-142">Stores a list of hardware versions of devices (desk phone).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-143"><a href="lync-server-2013-manufacturers-table.md">Manufacturers-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-143"><a href="lync-server-2013-manufacturers-table.md">Manufacturers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-144">Speichert eine Liste der Hersteller von Geräten (Tischtelefon).</span><span class="sxs-lookup"><span data-stu-id="daf50-144">Stores a list of manufacturers of devices (desk phone).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-145"><a href="lync-server-2013-mcus-table.md">Mcus-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-145"><a href="lync-server-2013-mcus-table.md">Mcus table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-146">Speichert Informationen zu den verschiedenen A/V-Konferenzservern und deren URIs.</span><span class="sxs-lookup"><span data-stu-id="daf50-146">Stores information about the various A/V Conferencing Servers and their URIs.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-147"><a href="lync-server-2013-mediationservers-table.md">MediationServers-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-147"><a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-148">Speichert eine Liste der Vermittlungsserver, die für VoIP-Anrufe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="daf50-148">Stores a list of Mediation Servers that are used for VoIP calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-149"><a href="lync-server-2013-phones-table.md">Phones-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-149"><a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-150">Speichert alle Telefonnummern, die in VoIP-Anrufen verwendet werden, die archiviert wurden oder deren Anrufdetails aufgezeichnet wurden.</span><span class="sxs-lookup"><span data-stu-id="daf50-150">Stores all the phone numbers used in VoIP calls that were archived or whose call details were recorded.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-151"><a href="lync-server-2013-pools-table.md">Pools-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-151"><a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-152">Speichert die Namen des Pools, in dem Chatnachrichten erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="daf50-152">Stores the names of the pool on which IM messages are captured.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-153"><a href="lync-server-2013-servers-table.md">Servers-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-153"><a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-154">Speichert den Namen der an den anrufen beteiligten Server.</span><span class="sxs-lookup"><span data-stu-id="daf50-154">Stores the name of servers involved in calls.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-155"><a href="lync-server-2013-tenants-table.md">Tenants-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-155"><a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-156">Speichert die Mandanten, die von der aktuellen Bereitstellung unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="daf50-156">Stores the tenants supported by current deployment.</span></span> <span data-ttu-id="daf50-157">Es gibt einige integrierte Mandanten für Enterprise-Benutzer, Federated-Benutzer, öffentliche Chat-Konnektivitäts-Benutzer und anonyme Benutzer.</span><span class="sxs-lookup"><span data-stu-id="daf50-157">There some build-in tenants for Enterprise user, Federated User, public IM connectivity user, and Anonymous users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-158"><a href="lync-server-2013-useragentdef-table.md">UserAgentDef-Tabelle in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-158"><a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-159">Ordnet die Bezeichner des Benutzer-Agents den beschreibenden Namen des Agents zu.</span><span class="sxs-lookup"><span data-stu-id="daf50-159">Maps user agent identifiers to the agent’s descriptive names.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-160"><a href="lync-server-2013-users-table.md">Users-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-160"><a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-161">Speichert die Benutzer-URIs von Benutzern, die an Sitzungen teilgenommen haben, die in dieser Datenbank aufgezeichnet oder archiviert wurden.</span><span class="sxs-lookup"><span data-stu-id="daf50-161">Stores the user URIs of users who have participated in sessions recorded or archived in this database.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-162"><a href="lync-server-2013-userstatistics-table.md">UserStatistics-Tabelle in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-162"><a href="lync-server-2013-userstatistics-table.md">UserStatistics table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-163">Speichert Informationen zur Verwendung des Systems durch einen einzelnen Benutzer.</span><span class="sxs-lookup"><span data-stu-id="daf50-163">Stores information about an individual user’s usage of the system.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="tables-specific-to-conference-cdr-records"></a><span data-ttu-id="daf50-164">Für Konferenz CdR-Datensätze spezifische Tabellen</span><span class="sxs-lookup"><span data-stu-id="daf50-164">Tables Specific to Conference CDR Records</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="daf50-165">Tabelle</span><span class="sxs-lookup"><span data-stu-id="daf50-165">Table</span></span></th>
<th><span data-ttu-id="daf50-166">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="daf50-166">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="daf50-167"><a href="lync-server-2013-conferences-table.md">Conferences-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-167"><a href="lync-server-2013-conferences-table.md">Conferences table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-168">Speichert Informationen zu allen Konferenzen, die archiviert wurden oder deren Details aufgezeichnet wurden, einschließlich ConferenceURI sowie Start-und Endzeit.</span><span class="sxs-lookup"><span data-stu-id="daf50-168">Stores information about all conferences that were archived or whose details were recorded, including ConferenceURI, and start and end time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-169"><a href="lync-server-2013-conferencesessiondetails-table.md">ConferenceSessionDetails-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-169"><a href="lync-server-2013-conferencesessiondetails-table.md">ConferenceSessionDetails table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-170">Speichert Informationen zu jeder SIP-basierten Konferenzsitzung, einschließlich Start-und Endzeit, Benutzer-ID, Antwortcode und Diagnose-ID für jede Sitzung.</span><span class="sxs-lookup"><span data-stu-id="daf50-170">Stores information about every SIP-based conference session, including start and end time, user ID, response code, and diagnostic ID for each session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-171"><a href="lync-server-2013-focusjoinsandleaves-table.md">FocusJoinsAndLeaves-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-171"><a href="lync-server-2013-focusjoinsandleaves-table.md">FocusJoinsAndLeaves table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-172">Speichert Informationen zu Konferenz Verknüpfungen und-Blättern, einschließlich der Rolle des Benutzers und der Client Version.</span><span class="sxs-lookup"><span data-stu-id="daf50-172">Stores information about conference joins and leaves, including users’ role and client version.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-173"><a href="lync-server-2013-mcujoinsandleaves-table.md">McuJoinsAndLeaves-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-173"><a href="lync-server-2013-mcujoinsandleaves-table.md">McuJoinsAndLeaves table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-174">Speichert Informationen zu den a/V-Konferenzservern, die an einer Konferenz beteiligt sind, und die Benutzer an-und Abreisezeiten.</span><span class="sxs-lookup"><span data-stu-id="daf50-174">Stores information about the A/V Conferencing Servers that are involved in a conference and the user join and leave times.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="tables-for-messages-in-im-conferences"></a><span data-ttu-id="daf50-175">Tabellen für Nachrichten in Chat Konferenzen</span><span class="sxs-lookup"><span data-stu-id="daf50-175">Tables for Messages in IM Conferences</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="daf50-176">Tabelle</span><span class="sxs-lookup"><span data-stu-id="daf50-176">Table</span></span></th>
<th><span data-ttu-id="daf50-177">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="daf50-177">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="daf50-178"><a href="lync-server-2013-conferencemessagecount-table.md">ConferenceMessageCount-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-178"><a href="lync-server-2013-conferencemessagecount-table.md">ConferenceMessageCount table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-179">Speichert für jede Chat Konferenz die Anzahl der Nachrichten, die von jedem Benutzer gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="daf50-179">For each IM conference, stores the number of messages that were sent by each user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-180"><a href="lync-server-2013-imreportsummary-table.md">IMReportSummary-Tabelle in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-180"><a href="lync-server-2013-imreportsummary-table.md">IMReportSummary table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-181">Bietet einen Gesamtbericht zu den Chat-Sitzungen, die in einer Organisation abgehalten werden.</span><span class="sxs-lookup"><span data-stu-id="daf50-181">Provides an overall report on the instant messaging sessions held in an organization.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="tables-for-peer-to-peer-sessions"></a><span data-ttu-id="daf50-182">Tabellen für Peer-to-Peer-Sitzungen</span><span class="sxs-lookup"><span data-stu-id="daf50-182">Tables for Peer-to-Peer Sessions</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="daf50-183">Tabelle</span><span class="sxs-lookup"><span data-stu-id="daf50-183">Table</span></span></th>
<th><span data-ttu-id="daf50-184">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="daf50-184">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="daf50-185"><a href="lync-server-2013-sessiondetails-table.md">SessionDetails-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-185"><a href="lync-server-2013-sessiondetails-table.md">SessionDetails table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-186">Speichert Informationen zu jeder Peer-to-Peer-Sitzung, einschließlich Start-und Endzeit, Benutzer-ID, Antwortcode und Nachrichtenanzahl für jeden Benutzer.</span><span class="sxs-lookup"><span data-stu-id="daf50-186">Stores information about every peer-to-peer session, including start and end time, user ID, response code, and message count for each user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-187"><a href="lync-server-2013-filetransfers-table.md">FileTransfers-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-187"><a href="lync-server-2013-filetransfers-table.md">FileTransfers table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-188">Speichert Informationen zu Dateiübertragungssitzungen, einschließlich Dateinamen und Ergebnis (akzeptiert, abgelehnt oder storniert).</span><span class="sxs-lookup"><span data-stu-id="daf50-188">Stores information about file transfer sessions, including file name and result (accepted, rejected, or canceled).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-189"><a href="lync-server-2013-media-table.md">Media-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-189"><a href="lync-server-2013-media-table.md">Media table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-190">Speichert Informationen zu den verschiedenen Medientypen, die an Peer-zu-Peer-Sitzungen beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="daf50-190">Stores information about the different media types involved in peer-to-peer sessions.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="table-for-voip-call-details"></a><span data-ttu-id="daf50-191">Tabelle für VoIP-Anruf Details</span><span class="sxs-lookup"><span data-stu-id="daf50-191">Table for VoIP Call Details</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="daf50-192">Tabelle</span><span class="sxs-lookup"><span data-stu-id="daf50-192">Table</span></span></th>
<th><span data-ttu-id="daf50-193">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="daf50-193">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="daf50-194"><a href="lync-server-2013-voipdetails-table.md">VoipDetails-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-194"><a href="lync-server-2013-voipdetails-table.md">VoipDetails table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-195">Speichert für jeden zwei-Parteien-VoIP/PSTN-Anrufinformationen zu dem Anruf, wie etwa die Telefon-ID des VoIP-Telefons, das verwendete Gateway und welche Partei getrennt wurde.</span><span class="sxs-lookup"><span data-stu-id="daf50-195">For each two-party VoIP/PSTN call, stores information about the call, such as the phone ID of VoIP phone, gateway used, and which party disconnected.</span></span> <span data-ttu-id="daf50-196">Bezieht sich auf die <a href="lync-server-2013-sessiondetails-table.md">SessionDetails-Tabelle in lync Server 2013</a> für die Start-und Endzeit des Anrufs und den Antwortcode.</span><span class="sxs-lookup"><span data-stu-id="daf50-196">Refers to the <a href="lync-server-2013-sessiondetails-table.md">SessionDetails table in Lync Server 2013</a> for call start/end times and response code.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="daf50-197">Wenn eine Partei bei einem Anruf ein VoIP-Nutzer ist oder wenn ein Vermittlungs Server an dem Anruf beteiligt war, wird in dieser Tabelle ein Datensatz erstellt.</span><span class="sxs-lookup"><span data-stu-id="daf50-197">If one party on a call is a VoIP user or if a Mediation Server was involved in the call, a record will be created in this table.</span></span> <span data-ttu-id="daf50-198">Informationen zu VoIP-und VoIP-Anrufen, die kein PSTN-Telefon (Public Switched Telephone Network) betreffen, werden in der <A href="lync-server-2013-sessiondetails-table.md">SessionDetails-Tabelle in lync Server 2013</A>erfasst.</span><span class="sxs-lookup"><span data-stu-id="daf50-198">Information about VoIP/VoIP calls not involving a public switched telephone network (PSTN) phone is captured in the <A href="lync-server-2013-sessiondetails-table.md">SessionDetails table in Lync Server 2013</A>.</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="table-for-e9-1-1-call-auditing"></a><span data-ttu-id="daf50-199">Tabelle für die E9-1-1-Anrufüberwachung</span><span class="sxs-lookup"><span data-stu-id="daf50-199">Table for E9-1-1 Call Auditing</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="daf50-200">Tabelle</span><span class="sxs-lookup"><span data-stu-id="daf50-200">Table</span></span></th>
<th><span data-ttu-id="daf50-201">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="daf50-201">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="daf50-202"><a href="lync-server-2013-locations-table.md">Locations-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-202"><a href="lync-server-2013-locations-table.md">Locations table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-203">Speichert für jeden Notruf, beispielsweise einen erweiterten 9-1-1 (E9-1-1)-Anruf, Standortinformationen zu dem Anruf.</span><span class="sxs-lookup"><span data-stu-id="daf50-203">For each emergency call, such as an Enhanced 9-1-1 (E9-1-1) call, stores location information about the call.</span></span> <span data-ttu-id="daf50-204">Bezieht sich auf die <a href="lync-server-2013-sessiondetails-table.md">SessionDetails-Tabelle in lync Server 2013</a> für die Start-und Endzeit des Anrufs und den Antwortcode.</span><span class="sxs-lookup"><span data-stu-id="daf50-204">Refers to the <a href="lync-server-2013-sessiondetails-table.md">SessionDetails table in Lync Server 2013</a> for call start/end times and response code.</span></span></p>
<div>

> [!NOTE]  
> <span data-ttu-id="daf50-205">Diese Tabelle enthält nur den Standort-BLOB für den E9-1-1-Anruf.</span><span class="sxs-lookup"><span data-stu-id="daf50-205">This table only contains the location blob for the E9-1-1 call.</span></span> <span data-ttu-id="daf50-206">Bezieht sich auf die Tabelle "SessionDetails", um weitere detaillierte Informationen zu dem Anruf zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="daf50-206">Refers to the SessionDetails table for other detailed information about the call.</span></span>


</div></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="tables-for-troubleshooting"></a><span data-ttu-id="daf50-207">Tabellen zur Problembehandlung</span><span class="sxs-lookup"><span data-stu-id="daf50-207">Tables for Troubleshooting</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="daf50-208">Tabelle</span><span class="sxs-lookup"><span data-stu-id="daf50-208">Table</span></span></th>
<th><span data-ttu-id="daf50-209">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="daf50-209">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="daf50-210"><a href="lync-server-2013-application-table.md">Application-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-210"><a href="lync-server-2013-application-table.md">Application table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-211">Speichert Informationen zu verschiedenen Prozessen in lync Server 2013, die an Routing und Verbindungen beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="daf50-211">Stores information about various processes within Lync Server 2013 that are involved in routing and connections.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-212"><a href="lync-server-2013-calltype-table.md">CallType-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-212"><a href="lync-server-2013-calltype-table.md">CallType table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-213">Speichert Informationen zu Typen des Anrufs, beispielsweise "Audio", "Sofortnachrichten", "Audio und Video" und "Anwendungsfreigabe".</span><span class="sxs-lookup"><span data-stu-id="daf50-213">Stores information about types of the call, such as, “audio”, “Instant Messaging”, “audio and video” and “application sharing”.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-214"><a href="lync-server-2013-errorcategory-table.md">ErrorCategory-Tabelle in lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-214"><a href="lync-server-2013-errorcategory-table.md">ErrorCategory table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-215">Speichert den Anzeigenamen für jede Microsoft lync Server 2013-Diagnose Klassifizierung.</span><span class="sxs-lookup"><span data-stu-id="daf50-215">Stores the friendly name for each Microsoft Lync Server 2013 diagnostic classification.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-216"><a href="lync-server-2013-errordef-table.md">ErrorDef-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-216"><a href="lync-server-2013-errordef-table.md">ErrorDef table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-217">Speichert Informationen zu Fehlertypen und deren Definitionen.</span><span class="sxs-lookup"><span data-stu-id="daf50-217">Stores information about types of errors and their definitions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-218"><a href="lync-server-2013-errorreport-table.md">ErrorReport-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-218"><a href="lync-server-2013-errorreport-table.md">ErrorReport table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-219">Speichert Informationen zu Fehlern, die aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="daf50-219">Stores information about errors that have occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-220"><a href="lync-server-2013-progressreport-table.md">ProgressReport-Tabelle in Lync Server 2013</a></span><span class="sxs-lookup"><span data-stu-id="daf50-220"><a href="lync-server-2013-progressreport-table.md">ProgressReport table in Lync Server 2013</a></span></span></p></td>
<td><p><span data-ttu-id="daf50-221">Speichert Informationen zu den Fortschrittsberichten verschiedener Schritte, die in lync Server 2013-Prozessen involviert sind.</span><span class="sxs-lookup"><span data-stu-id="daf50-221">Stores information about the progress reports of various steps involved in Lync Server 2013 processes.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="daf50-222">Die Tabellen in der folgenden Liste werden intern von lync Server verwendet.</span><span class="sxs-lookup"><span data-stu-id="daf50-222">The tables in the following list are used internally by Lync Server.</span></span> <span data-ttu-id="daf50-223">Deren Details werden in diesem Dokument nicht beschrieben.</span><span class="sxs-lookup"><span data-stu-id="daf50-223">Their details are not described in this document.</span></span>

</div>

<div>

## <a name="tables-for-internal-use-by-lync-server"></a><span data-ttu-id="daf50-224">Tabellen für die interne Verwendung durch lync Server</span><span class="sxs-lookup"><span data-stu-id="daf50-224">Tables for Internal Use by Lync Server</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="daf50-225">Tabelle</span><span class="sxs-lookup"><span data-stu-id="daf50-225">Table</span></span></th>
<th><span data-ttu-id="daf50-226">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="daf50-226">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="daf50-227"><strong>DbConfigDateTime</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-227"><strong>DbConfigDateTime</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-228">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-228">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-229"><strong>DbConfigInt</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-229"><strong>DbConfigInt</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-230">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-230">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-231"><strong>Dberrormessage</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-231"><strong>DbErrorMessage</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-232">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-232">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-233"><strong>Frontend-Tabelle</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-233"><strong>FrontEnd Table</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-234">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-234">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-235"><strong>MSMQProcessing-Tabelle</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-235"><strong>MSMQProcessing Table</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-236">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-236">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-237"><strong>SummaryTableConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-237"><strong>SummaryTableConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-238">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-238">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-239"><strong>Tabelle "Syndikator"</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-239"><strong>Syndicators Table</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-240">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-240">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-241"><strong>SyndicatorsTenantMap-Tabelle</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-241"><strong>SyndicatorsTenantMap Table</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-242">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-242">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-243"><strong>Aufgaben Tabelle</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-243"><strong>Task Table</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-244">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-244">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-245"><strong>UserStatistics</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-245"><strong>UserStatistics</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-246">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-246">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-247"><strong>UsageSummary_UQ</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-247"><strong>UsageSummary_UQ</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-248">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-248">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-249"><strong>UsageSummary</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-249"><strong>UsageSummary</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-250">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-250">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-251"><strong>DaylightSavingYears</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-251"><strong>DaylightSavingYears</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-252">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-252">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-253"><strong>TimeZoneConfiguration</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-253"><strong>TimeZoneConfiguration</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-254">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-254">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-255"><strong>Zeitzonen</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-255"><strong>TimeZones</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-256">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-256">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-257"><strong>FailureSummary_UQ</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-257"><strong>FailureSummary_UQ</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-258">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-258">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-259"><strong>FailureSummary</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-259"><strong>FailureSummary</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-260">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-260">For internal use only.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="daf50-261"><strong>ServerSummary</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-261"><strong>ServerSummary</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-262">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-262">For internal use only.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="daf50-263"><strong>MsDiagMetaData</strong></span><span class="sxs-lookup"><span data-stu-id="daf50-263"><strong>MsDiagMetaData</strong></span></span></p></td>
<td><p><span data-ttu-id="daf50-264">Nur für interne Verwendung.</span><span class="sxs-lookup"><span data-stu-id="daf50-264">For internal use only.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="daf50-265">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="daf50-265">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

