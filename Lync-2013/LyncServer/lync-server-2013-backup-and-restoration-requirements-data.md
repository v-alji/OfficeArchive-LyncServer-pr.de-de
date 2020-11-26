---
title: 'Lync Server 2013: Sicherungs-und Wiederherstellungsanforderungen: Daten'
description: 'Lync Server 2013: Sicherungs-und Wiederherstellungsanforderungen: Daten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: 'Backup and restoration requirements: data'
ms:assetid: ecfb8e4d-cb4f-476d-9772-4486bd683c04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202194(v=OCS.15)
ms:contentKeyID: 51541526
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7e135f09706d31ff3f0efa54c8687546de9fab78
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437987"
---
# <a name="backup-and-restoration-requirements-in-lync-server-2013-data"></a><span data-ttu-id="fc0f1-103">Sicherungs-und Wiederherstellungsanforderungen in lync Server 2013: Daten</span><span class="sxs-lookup"><span data-stu-id="fc0f1-103">Backup and restoration requirements in Lync Server 2013: data</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fc0f1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fc0f1-104">

<span> </span></span></span>

<span data-ttu-id="fc0f1-105">_**Letztes Änderungsdatum des Themas:** 2013-03-26_</span><span class="sxs-lookup"><span data-stu-id="fc0f1-105">_**Topic Last Modified:** 2013-03-26_</span></span>

<span data-ttu-id="fc0f1-106">Lync Server verwendet Einstellungen und Konfigurationsinformationen, die in Datenbanken gespeichert sind, und Daten, die in Datenbanken und Datei speichern gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-106">Lync Server uses settings and configuration information that are stored in databases, and data that is stored in databases and file stores.</span></span> <span data-ttu-id="fc0f1-107">In diesem Thema werden die Daten beschrieben, die Sie sichern müssen, damit der Dienst wiederhergestellt werden kann, wenn in Ihrer Organisation ein Fehler oder ein Ausfall auftritt, und außerdem die von lync Server verwendeten Daten und Komponenten identifiziert werden, die separat gesichert werden müssen.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-107">This topic describes the data that you need to back up to be able to restore service if your organization experiences a failure or outage, and also identifies the data and components used by Lync Server that you need to back up separately.</span></span>

<div>

## <a name="settings-and-configuration-requirements"></a><span data-ttu-id="fc0f1-108">Einstellungen und Konfigurationsanforderungen</span><span class="sxs-lookup"><span data-stu-id="fc0f1-108">Settings and Configuration Requirements</span></span>

<span data-ttu-id="fc0f1-109">Dieses Thema enthält Verfahren zum Sichern und Wiederherstellen der Einstellungen und Konfigurationsinformationen, die für die Wiederherstellung des lync Server-Diensts erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-109">This topic includes procedures for backing up and restoring the settings and configuration information that is required for recovery of Lync Server service.</span></span> <span data-ttu-id="fc0f1-110">Die Konfigurationsinformationen befinden sich im zentralen Verwaltungsspeicher oder in einer anderen Back-End-Datenbank oder auf dem Standard Edition-Server.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-110">The configuration information is located in the Central Management store or on another back-end database or on Standard Edition server.</span></span>

<span data-ttu-id="fc0f1-111">In der folgenden Tabelle sind die Einstellungen und Konfigurationsinformationen aufgeführt, die Sie sichern und wiederherstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-111">The following table identifies the settings and configuration information that you need to back up and restore.</span></span>

### <a name="settings-and-configuration-data"></a><span data-ttu-id="fc0f1-112">Einstellungen und Konfigurationsdaten</span><span class="sxs-lookup"><span data-stu-id="fc0f1-112">Settings and Configuration Data</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc0f1-113">Art der Daten</span><span class="sxs-lookup"><span data-stu-id="fc0f1-113">Type of data</span></span></th>
<th><span data-ttu-id="fc0f1-114">Wo gespeichert</span><span class="sxs-lookup"><span data-stu-id="fc0f1-114">Where stored</span></span></th>
<th><span data-ttu-id="fc0f1-115">Beschreibung/wann sichern</span><span class="sxs-lookup"><span data-stu-id="fc0f1-115">Description / When to back up</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc0f1-116">Informationen zur Topologie-Konfiguration</span><span class="sxs-lookup"><span data-stu-id="fc0f1-116">Topology configuration information</span></span></p></td>
<td><p><span data-ttu-id="fc0f1-117">Zentraler Verwaltungsspeicher (Datenbank: XDS. mdf)</span><span class="sxs-lookup"><span data-stu-id="fc0f1-117">Central Management store (database: Xds.mdf)</span></span></p></td>
<td><p><span data-ttu-id="fc0f1-118">Topologie-, Richtlinien-und Konfigurationseinstellungen.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-118">Topology, policy, and configuration settings.</span></span></p>
<p><span data-ttu-id="fc0f1-119">Sichern Sie Ihre regelmäßigen Sicherungen und nachdem Sie die lync Server-Systemsteuerung oder Cmdlets verwendet haben, um Ihre Konfiguration oder Richtlinien zu ändern.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-119">Back up with your regular backups and after you use Lync Server Control Panel or cmdlets to modify your configuration or policies.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc0f1-120">Standortinformationen</span><span class="sxs-lookup"><span data-stu-id="fc0f1-120">Location information</span></span></p></td>
<td><p><span data-ttu-id="fc0f1-121">Zentraler Verwaltungsspeicher (Datenbank: Lis. mdf)</span><span class="sxs-lookup"><span data-stu-id="fc0f1-121">Central Management store (database: Lis.mdf)</span></span></p></td>
<td><p><span data-ttu-id="fc0f1-122">Enterprise Voice Enhanced 9-1-1 (E9-1-1)-Konfigurationsinformationen.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-122">Enterprise Voice Enhanced 9-1-1 (E9-1-1) configuration information.</span></span> <span data-ttu-id="fc0f1-123">Diese Informationen sind in der Regel statisch.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-123">This information is generally static.</span></span></p>
<p><span data-ttu-id="fc0f1-124">Sichern Sie Ihre normalen Backups.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-124">Back up with your regular backups.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc0f1-125">Konfigurationsinformationen zur Reaktionsgruppe</span><span class="sxs-lookup"><span data-stu-id="fc0f1-125">Response Group configuration information</span></span></p></td>
<td><p><span data-ttu-id="fc0f1-126">Back-End-Server oder Standard Edition-Server (Datenbank: RgsConfig. mdf)</span><span class="sxs-lookup"><span data-stu-id="fc0f1-126">Back End Server or Standard Edition server (database: RgsConfig.mdf)</span></span></p></td>
<td><p><span data-ttu-id="fc0f1-127">Gruppen, Warteschlangen und Workflows für Reaktionsgruppen-Agents</span><span class="sxs-lookup"><span data-stu-id="fc0f1-127">Response Group agent groups, queues, and workflows.</span></span></p>
<p><span data-ttu-id="fc0f1-128">Sichern Sie mit ihren regulären Sicherungen und nach dem Hinzufügen oder Ändern von Agentengruppen, Warteschlangen oder Workflows.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-128">Back up with your regular backups and after you add or change agent groups, queues, or workflows.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="data-requirements"></a><span data-ttu-id="fc0f1-129">Datenanforderungen</span><span class="sxs-lookup"><span data-stu-id="fc0f1-129">Data Requirements</span></span>

<span data-ttu-id="fc0f1-130">Nachfolgend finden Sie eine Liste der lync Server-Daten, die Sie sichern müssen, damit Sie den lync Server-Dienst im Fall eines Fehlers wiederherstellen können.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-130">Here is a list of the Lync Server data that you need to back up so that you can restore Lync Server service in the event of a failure.</span></span>

<span data-ttu-id="fc0f1-131">Beachten Sie, dass für die Wiederherstellung einige Datentypen nicht erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-131">Note that some types of data are not required for recovery.</span></span> <span data-ttu-id="fc0f1-132">Dieses Thema enthält keine Verfahren zum Sichern dieser Datentypen, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="fc0f1-132">This topic does not contain procedures for backing up these types of data, which include the following:</span></span>

  - <span data-ttu-id="fc0f1-133">Vorübergehende Benutzerdaten wie Endpunkte und Abonnements, aktive Konferenzserver und transiente Konferenz Zustände (Datenbank: RtcDyn. mdf)</span><span class="sxs-lookup"><span data-stu-id="fc0f1-133">Transient user data, such as endpoints and subscriptions, active conferencing servers, and transient conferencing states (database: RtcDyn.mdf)</span></span>

  - <span data-ttu-id="fc0f1-134">Adressbuchdaten (Datenbanken: RTCAb. mdf und Rtcab1. mdf).</span><span class="sxs-lookup"><span data-stu-id="fc0f1-134">Address Book data (databases: Rtcab.mdf and Rtcab1.mdf).</span></span> <span data-ttu-id="fc0f1-135">Die Adressbuchdatenbank wird automatisch aus den Active Directory-Domänendiensten neu erstellt.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-135">The Address Book database is regenerated automatically from Active Directory Domain Services.</span></span>

  - <span data-ttu-id="fc0f1-136">Dynamische Informationen für die Anwendung des Anruf Parks (Datenbank: CpsDyn. mdf)</span><span class="sxs-lookup"><span data-stu-id="fc0f1-136">Dynamic information for the Call Park application (database: CpsDyn.mdf)</span></span>

  - <span data-ttu-id="fc0f1-137">Flüchtige Antwortgruppen Daten wie Agenten-Anmeldestatus und warte Informationen für Anrufe (Datenbank: RgsDyn. mdf)</span><span class="sxs-lookup"><span data-stu-id="fc0f1-137">Transient Response Group data, such as agent sign-in state and call waiting information (database: RgsDyn.mdf)</span></span>

  - <span data-ttu-id="fc0f1-138">Die Kompatibilitätsdatenbank für beständigen Chat (Datenbank: MgcComp. mdf).</span><span class="sxs-lookup"><span data-stu-id="fc0f1-138">The compliance database for Persistent Chat (database: MgcComp.mdf).</span></span> <span data-ttu-id="fc0f1-139">Wenn die Compliance für beständigen Chat aktiviert ist, sind die Informationen in der beständigen Chat-Kompatibilitätsdatenbank vorübergehend, solange Sie über einen Adapter verfügen, der zum Lesen von Informationen aus der Datenbank konfiguriert ist und in ein anderes Format konvertiert werden kann.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-139">If you have Persistent Chat compliance enabled, the information in the Persistent Chat Compliance database is transient as long as you have an adapter configured to read information from the database and convert it to an alternate format.</span></span> <span data-ttu-id="fc0f1-140">Daher gilt die Compliance-Datenbank für beständigen Chat als vorübergehend.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-140">Hence the compliance database for Persistent Chat is considered transient.</span></span>
    
    <span data-ttu-id="fc0f1-141">Lync Server 2013 beständiger Chat Server wird mit einem XML-Adapter ausgeliefert.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-141">Lync Server 2013 Persistent Chat Server ships with an XML adapter.</span></span> <span data-ttu-id="fc0f1-142">Sie können auch benutzerdefinierte Adapter installieren, die diese Daten übernehmen und in andere Quellen, wie etwa Exchange Hosted Archives, verschieben.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-142">You can also install custom adapters that take this data and move it to other sources, such as Exchange Hosted Archives.</span></span>

<span data-ttu-id="fc0f1-143">In der folgenden Tabelle sind die Daten aufgeführt, die Sie sichern und wiederherstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-143">The following table identifies the data that you need to back up and restore.</span></span>

### <a name="data-stored-in-databases"></a><span data-ttu-id="fc0f1-144">In Datenbanken gespeicherte Daten</span><span class="sxs-lookup"><span data-stu-id="fc0f1-144">Data Stored in Databases</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc0f1-145">Art der Daten</span><span class="sxs-lookup"><span data-stu-id="fc0f1-145">Type of data</span></span></th>
<th><span data-ttu-id="fc0f1-146">Wo gespeichert</span><span class="sxs-lookup"><span data-stu-id="fc0f1-146">Where stored</span></span></th>
<th><span data-ttu-id="fc0f1-147">Beschreibung/wann sichern</span><span class="sxs-lookup"><span data-stu-id="fc0f1-147">Description / When to back up</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc0f1-148">Beständige Benutzerdaten</span><span class="sxs-lookup"><span data-stu-id="fc0f1-148">Persistent user data</span></span></p></td>
<td><p><span data-ttu-id="fc0f1-149">Back-End-Server oder Standard Edition-Server (Datenbank: RTCXDS. mdf)</span><span class="sxs-lookup"><span data-stu-id="fc0f1-149">Back End Server or Standard Edition server (database: RTCXDS.mdf)</span></span></p></td>
<td><p><span data-ttu-id="fc0f1-150">Benutzerrechte, Benutzer Kontaktlisten, Server-oder Pooldaten, geplante Konferenzen usw.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-150">User rights, user Contacts lists, server or pool data, scheduled conferences, and so on.</span></span> <span data-ttu-id="fc0f1-151">Diese Benutzerdaten beinhalten keine Inhalte, die in eine Konferenz hochgeladen wurden.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-151">This user data does not include content uploaded to a conference.</span></span></p>
<p><span data-ttu-id="fc0f1-152">Sichern Sie Ihre normalen Backups.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-152">Back up with your regular backups.</span></span> <span data-ttu-id="fc0f1-153">Diese Informationen sind dynamisch, doch der Verlust von Updates ist für lync Server nicht katastrophal, wenn Sie die letzte reguläre Sicherung wiederherstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-153">This information is dynamic, but the loss of updates is not catastrophic to Lync Server if you need to restore to your last regular backup.</span></span> <span data-ttu-id="fc0f1-154">Wenn Kontaktlisten für Ihre Organisation wichtig sind, können Sie diese Daten häufiger sichern.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-154">If Contacts lists are critical to your organization, you can back up this data more frequently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc0f1-155">Archivieren von Daten</span><span class="sxs-lookup"><span data-stu-id="fc0f1-155">Archiving data</span></span></p></td>
<td><p><span data-ttu-id="fc0f1-156">Archivierungsdatenbank (Datenbank: LcsLog. mdf)</span><span class="sxs-lookup"><span data-stu-id="fc0f1-156">Archiving database (database: LcsLog.mdf)</span></span></p>
<p><span data-ttu-id="fc0f1-157">Diese Daten werden möglicherweise auf Exchange 2013 gespeichert, wenn Sie die Microsoft Exchange-Integrations Option aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-157">This data may be stored on Exchange 2013, if you have enabled the Microsoft Exchange integration option.</span></span> <span data-ttu-id="fc0f1-158">Andernfalls werden diese Daten in einer lync Server-Archivierungsdatenbank aufbewahrt, die sich möglicherweise mit einer anderen lync Server-Datenbank oder eigenständigen auf einem separaten Datenbankserver befindet.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-158">Otherwise, this data is kept in a Lync Server Archiving database, which may be collocated with another Lync Server database, or stand-alone on a separate database server.</span></span></p></td>
<td><p><span data-ttu-id="fc0f1-159">Instant Messaging (im) und Besprechungsinhalte.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-159">Instant messaging (IM) and meeting content.</span></span></p>
<p><span data-ttu-id="fc0f1-160">Diese Daten sind für lync Server nicht wichtig, können aber für Ihre Organisation für regulatorische Zwecke wichtig sein.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-160">This data is not critical to Lync Server, but it may be critical to your organization for regulatory purposes.</span></span> <span data-ttu-id="fc0f1-161">Legen Sie den Sicherungszeitplan entsprechend fest.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-161">Determine your back up schedule accordingly.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fc0f1-162">Überwachen von Daten</span><span class="sxs-lookup"><span data-stu-id="fc0f1-162">Monitoring data</span></span></p></td>
<td><p><span data-ttu-id="fc0f1-163">Überwachungsdatenbanken (LcsCDR. mdf und Datenbank QoEMetrics werden. mdf)</span><span class="sxs-lookup"><span data-stu-id="fc0f1-163">Monitoring databases (LcsCDR.mdf and QoeMetrics.mdf)</span></span></p>
<p><span data-ttu-id="fc0f1-164">Diese Datenbankenkönnen mit einer anderen lync Server-Datenbank oder eigenständigen auf einem separaten Datenbankserver bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-164">These databases may be collocated with another Lync Server database, or stand-alone on a separate database server.</span></span></p></td>
<td><p><span data-ttu-id="fc0f1-165">Anruf Detaildatensätze (LcsCDR. mdf) und QoE-Metrik (Quality of Experience) (Datenbank QoEMetrics werden. mdf).</span><span class="sxs-lookup"><span data-stu-id="fc0f1-165">Call detail records (LcsCDR.mdf) and Quality of Experience (QoE) metrics (QoeMetrics.mdf).</span></span></p>
<p><span data-ttu-id="fc0f1-166">Anruf Detaildatensätze sind dynamisch und können für Ihr Unternehmen von entscheidender Bedeutung sein.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-166">Call detail records are dynamic and may be critical to your business.</span></span> <span data-ttu-id="fc0f1-167">Ermitteln Sie den Sicherungszeitplan, indem Sie erwägen, ob Sie diese Einträge aus regulatorischen Gründen benötigen.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-167">Determine your back up schedule by considering whether you need these records for regulatory reasons.</span></span></p>
<p><span data-ttu-id="fc0f1-168">Die Qualität der Erfahrungs Informationen ist dynamisch.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-168">Quality of experience information is dynamic.</span></span> <span data-ttu-id="fc0f1-169">Der Verlust von QoE-Daten ist für den Betrieb von lync Server nicht entscheidend, kann aber für Ihr Unternehmen von entscheidender Bedeutung sein.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-169">Loss of QoE data is not critical for the operation of Lync Server, but it may be critical to your business.</span></span> <span data-ttu-id="fc0f1-170">Ermitteln Sie den Sicherungszeitplan basierend auf der Wichtigkeit dieser Informationen für Ihre Organisation.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-170">Determine your back up schedule based on how critical this information is to your organization.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fc0f1-171">Persistente Chat-Daten</span><span class="sxs-lookup"><span data-stu-id="fc0f1-171">Persistent Chat data</span></span></p></td>
<td><p><span data-ttu-id="fc0f1-172">Persistent Chat-Datenbank (MGD. mdf).</span><span class="sxs-lookup"><span data-stu-id="fc0f1-172">Persistent Chat database (mgd.mdf).</span></span></p>
<p><span data-ttu-id="fc0f1-173">Diese Datenbank kann mit einer anderen lync Server-Datenbank oder eigenständigen auf einem separaten Datenbankserver bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-173">This database may be collocated with another Lync Server database, or stand-alone on a separate database server.</span></span></p></td>
<td><p><span data-ttu-id="fc0f1-174">Beständige Chat-Daten sind tatsächliche Chatinhalte, die in Chatrooms gepostet werden.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-174">Persistent Chat Data is actual chat content being posted in chat rooms.</span></span> <span data-ttu-id="fc0f1-175">Diese Daten sind häufig geschäftskritisch.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-175">This data is often business critical.</span></span></p>
<p><span data-ttu-id="fc0f1-176">Sie können die SQL Server-Sicherung verwenden oder die Datenbank mithilfe des Cmdlets <strong>Export-CsPersistentChatData</strong> exportieren, das in lync Server bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-176">You can choose to use SQL Server backup, or export the database by using the <strong>Export-CsPersistentChatData</strong> cmdlet that is provided in Lync Server.</span></span> <span data-ttu-id="fc0f1-177">Zur Wiederherstellung der Daten können Sie die Datenbank bis zum Zeitpunkt der letzten vollständigen Sicherung importieren und wiederherstellen, was bedeutet, dass Sie die Datenbank nicht bis zum Zeitpunkt des Fehlers wiederherstellen können.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-177">For recovery of the data, you can import and restore the database to the point of the last full backup, which means you cannot restore the database to the point of failure.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="file-store-data-requirements"></a><span data-ttu-id="fc0f1-178">Dateispeicher-Datenanforderungen</span><span class="sxs-lookup"><span data-stu-id="fc0f1-178">File Store Data Requirements</span></span>

<span data-ttu-id="fc0f1-179">In einer Enterprise Edition-Bereitstellung befindet sich der lync Server-Dateispeicher normalerweise auf einem Datei Server.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-179">In an Enterprise Edition deployment, the Lync Server file store is typically located on a file server.</span></span> <span data-ttu-id="fc0f1-180">Bei einer Standard Edition-Bereitstellung befindet sich der lync Server-Dateispeicher standardmäßig auf dem Standard Edition-Server.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-180">In a Standard Edition deployment, the Lync Server file store is located by default on the Standard Edition server.</span></span> <span data-ttu-id="fc0f1-181">In der Regel gibt es einen lync Server-Dateispeicher, der für eine Website freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-181">Typically, there is one Lync Server file store that is shared for a site.</span></span> <span data-ttu-id="fc0f1-182">Der Dateispeicher für beständigen Chat verwendet dieselbe Dateifreigabe wie der lync Server-Dateispeicher.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-182">The Persistent Chat file store uses the same file share as the Lync Server file store.</span></span>

<span data-ttu-id="fc0f1-183">Dateispeicherorte werden als \\ \\ Server \\ Freigabename identifiziert.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-183">File store locations are identified as \\\\server\\share name.</span></span> <span data-ttu-id="fc0f1-184">Wenn Sie die spezifischen Speicherorte ihrer Dateispeicher finden möchten, öffnen Sie den Topologie-Generator, und schauen Sie im Knoten **Dateispeicher** nach.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-184">To find the specific locations of your file stores, open Topology Builder and look in the **File stores** node.</span></span>

<span data-ttu-id="fc0f1-185">In der folgenden Tabelle sind die Dateispeicher aufgeführt, die Sie sichern und wiederherstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-185">The following table identifies the file stores you need to back up and restore.</span></span>

### <a name="file-stores"></a><span data-ttu-id="fc0f1-186">Dateispeicher</span><span class="sxs-lookup"><span data-stu-id="fc0f1-186">File Stores</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fc0f1-187">Art der Daten</span><span class="sxs-lookup"><span data-stu-id="fc0f1-187">Type of data</span></span></th>
<th><span data-ttu-id="fc0f1-188">Wo gespeichert</span><span class="sxs-lookup"><span data-stu-id="fc0f1-188">Where stored</span></span></th>
<th><span data-ttu-id="fc0f1-189">Beschreibung/wann sichern</span><span class="sxs-lookup"><span data-stu-id="fc0f1-189">Description / when to back up</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fc0f1-190">Lync Server-Dateispeicher</span><span class="sxs-lookup"><span data-stu-id="fc0f1-190">Lync Server file store</span></span></p></td>
<td><p><span data-ttu-id="fc0f1-191">In der Regel auf einem Dateiserver, einem Dateicluster oder einem Standard Edition-Server</span><span class="sxs-lookup"><span data-stu-id="fc0f1-191">Typically on a file server, file cluster, or a Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="fc0f1-192">Besprechungsinhalte, Metadaten für Besprechungsinhalte, Konformitäts Protokolle für Anwendungen, Anwendungsdatendateien, Updatedateien für Geräte Updates, Audiodateien für die Reaktionsgruppe, Anruf Park-und Ankündigungs Anwendungen sowie Dateien, die in beständigen Chatrooms gepostet wurden.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-192">Meeting content, meeting content metadata, meeting compliance logs, application data files, update files for device updates, audio files for Response Group, Call Park, and Announcement applications, and files posted into Persistent Chat rooms.</span></span></p>
<p><span data-ttu-id="fc0f1-193">Sichern Sie Ihre normalen Backups.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-193">Back up with your regular backups.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="additional-backup-requirements"></a><span data-ttu-id="fc0f1-194">Zusätzliche Sicherungsanforderungen</span><span class="sxs-lookup"><span data-stu-id="fc0f1-194">Additional Backup Requirements</span></span>

<span data-ttu-id="fc0f1-195">Wenn Sie sicherstellen möchten, dass Sie die lync Server-Dienste bei einem Fehler wiederherstellen können, müssen Sie einige erforderliche Komponenten sichern, die nicht Teil von lync Server selbst sind.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-195">To help ensure your ability to restore Lync Server services in the event of a failure, you must back up some necessary components that are not part of Lync Server itself.</span></span> <span data-ttu-id="fc0f1-196">Die folgenden Komponenten werden nicht im Rahmen des in diesem Dokument beschriebenen lync Server-Sicherungs-und Wiederherstellungsprozesses gesichert oder wiederhergestellt:</span><span class="sxs-lookup"><span data-stu-id="fc0f1-196">The following components are not backed up or restored as part of the Lync Server backup and restoration process described in this document:</span></span>

  - <span data-ttu-id="fc0f1-197">**Active Directory-Domänendienste**   Sie müssen AD DS mithilfe von Active Directory-Tools zur gleichen Zeit sichern, wie Sie lync Server sichern.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-197">**Active Directory Domain Services**   You need to back up AD DS by using Active Directory tools at the same time that you back up Lync Server.</span></span> <span data-ttu-id="fc0f1-198">Es ist wichtig, dass AD DS mit lync Server synchronisiert bleibt, um Probleme zu vermeiden, die auftreten können, wenn lync Server Kontaktobjekte erwartet, die nicht mit denen in AD DS übereinstimmen.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-198">It is important to keep AD DS synchronized with Lync Server, to avoid problems that can occur when Lync Server expects contact objects that do not match those in AD DS.</span></span> <span data-ttu-id="fc0f1-199">In AD DS werden die folgenden von lync Server verwendeten Einstellungen gespeichert:</span><span class="sxs-lookup"><span data-stu-id="fc0f1-199">AD DS stores the following settings which are used by Lync Server:</span></span>
    
      - <span data-ttu-id="fc0f1-200">SIP-URI des Benutzers und andere Benutzereinstellungen.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-200">User SIP URI and other user settings.</span></span>
    
      - <span data-ttu-id="fc0f1-201">Kontaktobjekte für Anwendungen wie Reaktionsgruppe und Konferenzzentrale.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-201">Contact objects for applications such as Response Group and Conferencing Attendant.</span></span>
    
      - <span data-ttu-id="fc0f1-202">Ein Zeiger auf den zentralen Verwaltungsspeicher.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-202">A pointer to the Central Management Store.</span></span>
    
      - <span data-ttu-id="fc0f1-203">Kerberos-Authentifizierungs Konto (ein optionales Computerobjekt) und lync Server-Sicherheitsgruppen.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-203">Kerberos Authentication Account (an optional computer object) and Lync Server security groups.</span></span>
    
    <span data-ttu-id="fc0f1-204">Details zum Sichern und Wiederherstellen von AD DS in Windows Server 2008 finden Sie unter schrittweise Anleitung zur AD DS-Sicherung und-Wiederherstellung unter [https://go.microsoft.com/fwlink/p/?linkId=209105](https://go.microsoft.com/fwlink/p/?linkid=209105) .</span><span class="sxs-lookup"><span data-stu-id="fc0f1-204">For details about backing up and restoring AD DS in Windows Server 2008, see "AD DS Backup and Recovery Step-by-Step Guide" at [https://go.microsoft.com/fwlink/p/?linkId=209105](https://go.microsoft.com/fwlink/p/?linkid=209105).</span></span>

  - <span data-ttu-id="fc0f1-205">**Zertifizierungsstelle und Zertifikate**   Verwenden Sie die Richtlinie Ihres Unternehmens zum Sichern Ihrer Zertifizierungsstelle (Certification Authority, ca) und Zertifikate.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-205">**Certification authority and certificates**   Use your organization's policy for backing up your certification authority (CA) and certificates.</span></span> <span data-ttu-id="fc0f1-206">Wenn Sie exportierbare private Schlüssel verwenden, können Sie das Zertifikat und den privaten Schlüssel sichern und dann exportieren, wenn Sie die in diesem Dokument beschriebenen Verfahren zum Wiederherstellen von lync Server verwenden.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-206">If you use exportable private keys, you can back up the certificate and the private key, and then export them if you use the procedures in this document to restore Lync Server.</span></span> <span data-ttu-id="fc0f1-207">Wenn Sie eine interne Zertifizierungsstelle verwenden, können Sie die Registrierung erneut registrieren, wenn Sie lync Server wiederherstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-207">If you use an internal CA, you can re-enroll if you need to restore Lync Server.</span></span> <span data-ttu-id="fc0f1-208">Es ist wichtig, dass Sie den privaten Schlüssel an einem sicheren Ort aufbewahren, wo er verfügbar ist, wenn ein Computer ausfällt.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-208">It is important that you retain the private key in a secure location where it will be available if a computer fails.</span></span>

  - <span data-ttu-id="fc0f1-209">**System Center Operations Manager**   Wenn Sie Microsoft System Center Operations Manager (vormals Microsoft Operations Manager) zum Überwachen Ihrer lync Server-Bereitstellung verwenden, können Sie optional die Daten sichern, die beim Überwachen von lync Server erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-209">**System Center Operations Manager**   If you use Microsoft System Center Operations Manager (formerly Microsoft Operations Manager) to monitor your Lync Server deployment, you can optionally back up the data it creates while it is monitoring Lync Server.</span></span> <span data-ttu-id="fc0f1-210">Verwenden Sie den standardmäßigen SQL Server-Sicherungsvorgang zum Sichern von System Center Operations Manager-Dateien.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-210">Use your standard SQL Server backup process to back up System Center Operations Manager files.</span></span> <span data-ttu-id="fc0f1-211">Diese Dateien werden während der Wiederherstellung nicht wiederhergestellt.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-211">These files are not restored during recovery.</span></span>

  - <span data-ttu-id="fc0f1-212">**PSTN-Gateway-Konfiguration (Public Switched Telephone Network)**   Wenn Sie Enterprise-VoIP oder Survival Branch-Appliances verwenden, müssen Sie die Konfiguration des PSTN-Gateways sichern.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-212">**Public switched telephone network (PSTN) gateway configuration**   If you use Enterprise Voice or Survivable Branch Appliances, you need to back up the PSTN gateway configuration.</span></span> <span data-ttu-id="fc0f1-213">Informationen zum Sichern und Wiederherstellen von Konfigurationen für PSTN-Gateways finden Sie in Ihrem Anbieter.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-213">See your vendor for details about backing up and restoring PSTN gateway configurations.</span></span>

  - <span data-ttu-id="fc0f1-214">Nebeneinander **vorhandene Versionen von lync Server oder Office Communications Server**   Wenn Ihre lync Server 2013-Bereitstellung mit lync Server 2010 oder einer früheren Version von Office Communications Server koexistiert, können Sie die in diesem Dokument beschriebenen Verfahren nicht zum Sichern oder Wiederherstellen der vorherigen Version verwenden.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-214">**Coexisting versions of Lync Server or Office Communications Server**   If your Lync Server 2013 deployment coexists with Lync Server 2010 or an earlier version of Office Communications Server, you can’t use the procedures in this document for backing up or restoring the earlier version.</span></span> <span data-ttu-id="fc0f1-215">Stattdessen müssen Sie die Sicherungs-und Wiederherstellungsverfahren verwenden, die speziell für ihre frühere Version dokumentiert sind.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-215">Instead, you must use the backup and restoration procedures documented specifically for your earlier version.</span></span> <span data-ttu-id="fc0f1-216">Weitere Informationen zum Sichern und Wiederherstellen von lync Server 2010 finden Sie unter [https://go.microsoft.com/fwlink/p/?linkId=265417](https://go.microsoft.com/fwlink/p/?linkid=265417) .</span><span class="sxs-lookup"><span data-stu-id="fc0f1-216">For details about backing up and restoring Lync Server 2010, see [https://go.microsoft.com/fwlink/p/?linkId=265417](https://go.microsoft.com/fwlink/p/?linkid=265417) .</span></span> <span data-ttu-id="fc0f1-217">Weitere Informationen zum Sichern und Wiederherstellen von Microsoft Office Communications Server 2007 R2 finden Sie unter [https://go.microsoft.com/fwlink/p/?linkId=168162](https://go.microsoft.com/fwlink/p/?linkid=168162) .</span><span class="sxs-lookup"><span data-stu-id="fc0f1-217">For details about backing up and restoring Microsoft Office Communications Server 2007 R2, see [https://go.microsoft.com/fwlink/p/?linkId=168162](https://go.microsoft.com/fwlink/p/?linkid=168162).</span></span>

  - <span data-ttu-id="fc0f1-218">**Infrastruktur Informationen**   Sie müssen Informationen zu Ihrer Infrastruktur sichern, beispielsweise Ihre Firewall-Konfiguration, die Konfiguration des Lastenausgleichs, die Konfiguration der Internet Informationsdienste (IIS), DNS-Einträge (Domain Name System) und IP-Adressen sowie die DHCP-Konfiguration (Dynamic Host Configuration Protocol).</span><span class="sxs-lookup"><span data-stu-id="fc0f1-218">**Infrastructure information**   You need to back up information about your infrastructure, such as your firewall configuration, load balancing configuration, Internet Information Services (IIS) configuration, Domain Name System (DNS) records and IP addresses, and Dynamic Host Configuration Protocol (DHCP) configuration.</span></span> <span data-ttu-id="fc0f1-219">Informationen zum Sichern dieser Komponenten finden Sie bei den jeweiligen Anbietern.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-219">For details about backing up these components, check with their respective vendors.</span></span>

  - <span data-ttu-id="fc0f1-220">**Microsoft Exchange und Exchange Unified Messaging (um)**   Sichern und Wiederherstellen von Microsoft Exchange und Exchange um, wie in der Microsoft Exchange-Dokumentation beschrieben.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-220">**Microsoft Exchange and Exchange Unified Messaging (UM)**   Backup and restore Microsoft Exchange and Exchange UM as described in the Microsoft Exchange documentation.</span></span> <span data-ttu-id="fc0f1-221">Weitere Informationen zum Sichern und Wiederherstellen von Exchange Server 2013 finden Sie unter [https://go.microsoft.com/fwlink/?LinkId=285384](https://go.microsoft.com/fwlink/?linkid=285384) .</span><span class="sxs-lookup"><span data-stu-id="fc0f1-221">For details about backing up and restoring Exchange Server 2013, see [https://go.microsoft.com/fwlink/?LinkId=285384](https://go.microsoft.com/fwlink/?linkid=285384).</span></span> <span data-ttu-id="fc0f1-222">Weitere Informationen zum Sichern und Wiederherstellen von Exchange Server 2010 finden Sie unter [https://go.microsoft.com/fwlink/p/?linkId=209179](https://go.microsoft.com/fwlink/p/?linkid=209179) .</span><span class="sxs-lookup"><span data-stu-id="fc0f1-222">For details about backing up and restoring Exchange Server 2010, see [https://go.microsoft.com/fwlink/p/?linkId=209179](https://go.microsoft.com/fwlink/p/?linkid=209179).</span></span>
    
    <span data-ttu-id="fc0f1-223">Beachten Sie, dass lync Server 2013 die Möglichkeit bietet, Benutzer Kontaktlisten, HD-Benutzer Fotos und Archivierungsdaten in Exchange 2013 zu speichern.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-223">Note that Lync Server 2013 introduces the ability to have user contact lists, high definition user photos, and archiving data stored in Exchange 2013.</span></span> <span data-ttu-id="fc0f1-224">Sehen Sie sich die folgende Liste an, um zu erfahren, wie Sie diese Datentypen sichern:</span><span class="sxs-lookup"><span data-stu-id="fc0f1-224">See the following list to see how to back up these types of data:</span></span>
    
      - <span data-ttu-id="fc0f1-225">**Fotos mit höherer Auflösung** werden im Rahmen der Exchange Server-Sicherung gesichert.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-225">**High definition photos** are backed up as part of the Exchange Server backup.</span></span>
    
      - <span data-ttu-id="fc0f1-226">Der **Unified Contact Store** wird in lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-226">**Unified contact store** is introduced in Lync Server 2013.</span></span> <span data-ttu-id="fc0f1-227">Mit dem Unified Contact Store können Benutzer alle Ihre Kontaktinformationen in Exchange 2013 behalten.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-227">Unified contact store enables users to keep all their contact information in Exchange 2013.</span></span>
        
        <span data-ttu-id="fc0f1-228">Stellen Sie sicher, dass die Sicherungen für Benutzer auf dem neuesten Stand sind, indem Sie angeben, ob Ihre Benutzer Kontakte im Unified Contact Store oder auf dem lync-Back-End-Server gespeichert sind.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-228">You should make sure that backups are up-to-date for users in terms of whether their user contacts are stored in the unified contact store or on the Lync Back End Server.</span></span> <span data-ttu-id="fc0f1-229">Die folgenden Szenarien veranschaulichen, wo die Migration von Benutzerkontakten in den Unified Contact Store zu Problemen beim Sicherungs-und Wiederherstellungsprozess führen kann.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-229">The following scenarios illustrate where migrating user contacts to the unified contact store can cause issues for the backup and restore process.</span></span>
        
        <span data-ttu-id="fc0f1-230">**Szenario 1:** Benutzer Kontakte werden in den einheitlichen Kontaktspeicher migriert, und eine Wiederherstellung erfolgt über eine lync Server-Sicherung, die vor der Migration von Benutzerkontakten ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-230">**Scenario 1:** User contacts are migrated to the unified contact store, and a restore is performed from a Lync Server backup taken prior to the migration of user contacts.</span></span> <span data-ttu-id="fc0f1-231">In diesem Szenario hat der Benutzer einen Status veralteter Kontakte bis zu einem Tag, bis der lync Server-Migrations Task die Migration von Benutzerkontakten zu Exchange beginnt.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-231">In this scenario, the user will have a state of outdated contacts for up to one day until Lync Server Migration Task begins migrating user contacts to Exchange.</span></span> <span data-ttu-id="fc0f1-232">(Beachten Sie, dass die Exchange-Kontaktinformationen verwendet werden, da die Benutzer Kontakte zuvor in den Unified Contact Store migriert wurden).</span><span class="sxs-lookup"><span data-stu-id="fc0f1-232">(Note that because the user contacts were previously migrated to the unified contact store, the Exchange contact information will be used).</span></span> <span data-ttu-id="fc0f1-233">In diesem Szenario ist kein Administratoreingriff erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-233">No administrator intervention is needed in this scenario.</span></span>
        
        <span data-ttu-id="fc0f1-234">**Szenario 2:** Benutzer Kontakte wurden zuvor im Unified Contact Store gespeichert, anschließend aber zurückgesetzt.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-234">**Scenario 2:** User contacts were previously stored in the unified contact store, but then rolled back.</span></span> <span data-ttu-id="fc0f1-235">Eine Wiederherstellung erfolgt über eine lync Server-Sicherung, die durchgeführt wurde, wenn die Benutzer Kontakte im Unified Contact Store gespeichert wurden.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-235">A restore is performed from a Lync Server backup taken when the user contacts were stored in the unified contact store.</span></span> <span data-ttu-id="fc0f1-236">In diesem Szenario zeigt eine Fehlermeldung `Error: Incorrect Exchange Version` in den Serverprotokollen des Clients oder Lyss möglicherweise ein Problem an.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-236">In this scenario, an error message of `Error: Incorrect Exchange Version` in the client or Lyss server logs may indicate this as an issue.</span></span> <span data-ttu-id="fc0f1-237">Der Benutzer kann direkt von Exchange aus auf seine Kontaktliste in lync 2013 zugreifen, der Zustand des Clients entspricht aber nicht dem lync-Server Zustand.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-237">The user will be able to access their contact list in Lync 2013 directly from Exchange, but client’s state will not match the Lync Server state.</span></span> <span data-ttu-id="fc0f1-238">Um dies zu beheben, muss ein Administrator die **Invoke-CsUCSRollback-** Cmdlets für die betroffenen Benutzer ausführen.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-238">To fix this, an administrator will need to run the **Invoke-CsUCSRollback** cmdlets for the affected users.</span></span>
    
      - <span data-ttu-id="fc0f1-239">**Archivierungsdaten** können in Exchange 2013 gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-239">**Archiving Data** can be stored in Exchange 2013.</span></span> <span data-ttu-id="fc0f1-240">Diese Daten sind für lync Server nicht wichtig, können aber für Ihre Organisation für regulatorische Zwecke wichtig sein.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-240">This data is not critical to Lync Server, but it may be critical to your organization for regulatory purposes.</span></span> <span data-ttu-id="fc0f1-241">Wenn Archivierungsdaten in Exchange gespeichert sind und für Ihre Organisation wichtig sind, folgen Sie den Exchange-Sicherungs-und Wiederherstellungsverfahren.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-241">If archiving data is stored in Exchange and is critical to your organization, then follow Exchange backup and restore procedures.</span></span> <span data-ttu-id="fc0f1-242">Beachten Sie, dass Archivierungsdaten, die in Exchange gespeichert sind, nicht zurück zu lync Server verschoben werden können.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-242">Note that archiving data stored in Exchange cannot be moved back to Lync Server.</span></span> <span data-ttu-id="fc0f1-243">Darüber hinaus gibt es keine Möglichkeit, Daten, die bereits in der lync-Archivierungsdatenbank gespeichert sind, in Exchange zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="fc0f1-243">Additionally, there is no way to move data already stored in the Lync archiving database to Exchange.</span></span>

<span data-ttu-id="fc0f1-244"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fc0f1-244"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

