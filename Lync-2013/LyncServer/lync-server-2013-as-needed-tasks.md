---
title: 'Lync Server 2013: erforderliche Aufgaben'
description: 'Lync Server 2013: erforderliche Aufgaben.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: As-needed tasks
ms:assetid: b66bc6fe-f138-4cf4-ba7f-aee9a3e0497e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn722431(v=OCS.15)
ms:contentKeyID: 63969643
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 91fe249d9615bb619426c58b22606c3ef182f9a7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440549"
---
# <a name="as-needed-tasks-in-lync-server-2013"></a><span data-ttu-id="573f3-103">Erforderliche Aufgaben in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="573f3-103">As-needed tasks in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="573f3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="573f3-104">

<span> </span></span></span>

<span data-ttu-id="573f3-105">_**Letztes Änderungsdatum des Themas:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="573f3-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="573f3-106">Führen Sie die folgenden Aufgaben nach Bedarf aus.</span><span class="sxs-lookup"><span data-stu-id="573f3-106">Perform the following tasks as necessary.</span></span> <span data-ttu-id="573f3-107">Sie werden häufig auch durch Standardverfahren abgedeckt:</span><span class="sxs-lookup"><span data-stu-id="573f3-107">They are frequently also covered by standard procedures:</span></span>

  - <span data-ttu-id="573f3-108">\* \* Vollständige Sicherheitsüberprüfung \* \* Sie können diese Überprüfung regelmäßig als Antwort auf ein Upgrade oder eine Neugestaltung des Messagingsystems oder als Antwort auf eine versuchte (oder erfolgreiche) Sicherheitsverletzung durchführen.</span><span class="sxs-lookup"><span data-stu-id="573f3-108">\*\*Full Security Auditing   \*\*You can perform this audit regularly, in response to an upgrade or redesign of the messaging system, or in response to an attempted (or successful) security breach.</span></span> <span data-ttu-id="573f3-109">Das Verfahren kann Port-Scans auf Servern und Firewalls, Audits von Sicherheitsfixes und Penetrationstests von Drittanbietern beinhalten.</span><span class="sxs-lookup"><span data-stu-id="573f3-109">The procedure may involve port scans on servers and firewalls, audits of security fixes, and third-party penetration tests.</span></span>

  - <span data-ttu-id="573f3-110">**Ersetzen von Zertifikaten zum ablaufen**   Das Überprüfen von lync Server-Zertifikaten erfolgt in regelmäßigen wöchentlichen Aufgaben, und im Rahmen der Vorgehensweisesollte ein Administrator eine Aufzeichnung aller Ablaufdaten aller Zertifikate aufweisen.</span><span class="sxs-lookup"><span data-stu-id="573f3-110">**Replace Certificates about to Expire**   Checking Lync Server Certificates is one of regular weekly tasks, and as part of the procedure an administrator should have a record of all certificates’ expiry dates.</span></span> <span data-ttu-id="573f3-111">Dieser Eintrag ermöglicht es einem Administrator, eine Benachrichtigung zu erstellen, wenn ein bestimmtes Zertifikat demnächst abgelaufen und nach Bedarf ersetzt werden soll.</span><span class="sxs-lookup"><span data-stu-id="573f3-111">This record enables an administrator to create a notification when a particular certificate is about to be expired and replaced as needed.</span></span>

  - <span data-ttu-id="573f3-112">**Aktualisieren von Leistungsbasis Plänen**   Aktualisieren Sie die Leistungsbasis Pläne nach einem Upgrade oder einer Konfigurationsänderung.</span><span class="sxs-lookup"><span data-stu-id="573f3-112">**Updating Performance Baselines**   Update performance baselines after an upgrade or configuration change.</span></span> <span data-ttu-id="573f3-113">Ihre Organisation kann Basispläne verwenden, um Leistungsänderungen zu messen und Probleme zu erkennen, die sich auf die Systemleistung auswirken.</span><span class="sxs-lookup"><span data-stu-id="573f3-113">Your organization can use baselines to measure performance changes and to detect issues that affect system performance.</span></span>

  - <span data-ttu-id="573f3-114">**Verwalten des Enterprise-Pools**   Die anfängliche Konfiguration von Enterprise-Pools, Standard Edition-Servern und anderen Servern in der Umgebung Ihrer Organisation erfolgte während der Bereitstellung der einzelnen Server.</span><span class="sxs-lookup"><span data-stu-id="573f3-114">**Managing Enterprise Pool**   Initial configuration of Enterprise pools, Standard Edition servers, and any other servers in your organization's environment were done during deployment of the individual servers.</span></span> <span data-ttu-id="573f3-115">Die Verwaltung nach der Bereitstellung von Servern und Pools für Standard Edition-Server und Enterprise-Pools umfasst die folgenden Aufgaben:</span><span class="sxs-lookup"><span data-stu-id="573f3-115">Post-deployment management of servers and pools for Standard Edition servers and Enterprise pools includes the following tasks:</span></span>
    
      - <span data-ttu-id="573f3-116">Verwalten von Front-End-Servern</span><span class="sxs-lookup"><span data-stu-id="573f3-116">Managing Front End Servers</span></span>
    
      - <span data-ttu-id="573f3-117">Verwalten von Webkonferenzen</span><span class="sxs-lookup"><span data-stu-id="573f3-117">Managing Web Conferencing</span></span>
    
      - <span data-ttu-id="573f3-118">Verwalten von Konferenzen</span><span class="sxs-lookup"><span data-stu-id="573f3-118">Managing Conferencing</span></span>
    
      - <span data-ttu-id="573f3-119">Ändern der Anmeldeinformationen für das Dienstkonto</span><span class="sxs-lookup"><span data-stu-id="573f3-119">Changing Service Account Credentials</span></span>
    
      - <span data-ttu-id="573f3-120">Verwalten von Datenbanken</span><span class="sxs-lookup"><span data-stu-id="573f3-120">Managing Databases</span></span>
    
      - <span data-ttu-id="573f3-121">Starten und Beenden von Diensten und Deaktivieren von Server Rollen</span><span class="sxs-lookup"><span data-stu-id="573f3-121">Starting and Stopping Services and Deactivating Server Roles</span></span>
    
      - <span data-ttu-id="573f3-122">Entfernen von Servern und Serverrollen, Entfernen von Pools und Außerbetriebnahme von Servern und Pools</span><span class="sxs-lookup"><span data-stu-id="573f3-122">Removing Servers and Server Roles, Removing Pools, and Decommissioning Servers and Pools</span></span>

  - <span data-ttu-id="573f3-123">**Verwalten der Nutzung**   Sie können lync Server 2013 so konfigurieren, dass die Features und Funktionen bereitgestellt werden, die für Ihre Organisation am besten geeignet sind.</span><span class="sxs-lookup"><span data-stu-id="573f3-123">**Managing Usage**   You can configure Lync Server 2013 to provide the features and functionality that are most appropriate for your organization.</span></span> <span data-ttu-id="573f3-124">Dazu gehört Folgendes:</span><span class="sxs-lookup"><span data-stu-id="573f3-124">This includes the following:</span></span>
    
      - <span data-ttu-id="573f3-125">Verwalten der Unterstützung für lokale Webkonferenzbesprechungen</span><span class="sxs-lookup"><span data-stu-id="573f3-125">Managing Support for On-Premise Web Conferencing Meetings</span></span>
    
      - <span data-ttu-id="573f3-126">Verwalten der Verwendung von Verteilergruppen zum Senden von Sofortnachrichten</span><span class="sxs-lookup"><span data-stu-id="573f3-126">Managing the Use of Distribution Groups to Send Instant Messages</span></span>
    
      - <span data-ttu-id="573f3-127">Verwalten von Kontakten, Anwesenheitsinformationen und Abfragen</span><span class="sxs-lookup"><span data-stu-id="573f3-127">Managing Contacts, Presence, and Queries</span></span>
    
      - <span data-ttu-id="573f3-128">Konfigurieren der Client Versions Filterung</span><span class="sxs-lookup"><span data-stu-id="573f3-128">Configuring Client Version Filtering</span></span>
    
      - <span data-ttu-id="573f3-129">Konfigurieren intelligenter Chat Filterung</span><span class="sxs-lookup"><span data-stu-id="573f3-129">Configuring Intelligent IM Filtering</span></span>
    
      - <span data-ttu-id="573f3-130">Konfigurieren von Archivierungs-, Anruf Detail Aufzeichnung und Besprechungs Konformität</span><span class="sxs-lookup"><span data-stu-id="573f3-130">Configuring Archiving, Call Detail Recording, and Meeting Compliance</span></span>

  - <span data-ttu-id="573f3-131">**Verwalten der Edge-Server-Konnektivität**   Die laufende Verwaltung der Server und Einstellungen, die für die Bereitstellung externer Konnektivität erforderlich sind, umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="573f3-131">**Managing Edge Server Connectivity**   Ongoing management of the servers and settings required to provide external connectivity includes the following:</span></span>
    
      - <span data-ttu-id="573f3-132">Verwalten der Konnektivität zwischen internen Servern und Edgeserver</span><span class="sxs-lookup"><span data-stu-id="573f3-132">Managing Connectivity between Internal Servers and Edge Servers</span></span>
    
      - <span data-ttu-id="573f3-133">Konfigurieren interner und externer Schnittstellen und Zertifikate für Edgeserver</span><span class="sxs-lookup"><span data-stu-id="573f3-133">Configuring Internal and External Interfaces and Certificates for Edge Servers</span></span>
    
      - <span data-ttu-id="573f3-134">Verwalten des Zugriffs von Verbundpartnern</span><span class="sxs-lookup"><span data-stu-id="573f3-134">Managing Federated Partner Access</span></span>

  - <span data-ttu-id="573f3-135">**Verwalten des Adressbuchs**   Die Verwaltung von Adressbuch Servern umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="573f3-135">**Administering the Address Book**   Administering Address Book Servers includes the following:</span></span>
    
      - <span data-ttu-id="573f3-136">Konfigurieren der Adressbuch Server-Telefon Normalisierung</span><span class="sxs-lookup"><span data-stu-id="573f3-136">Configuring Address Book Server phone normalization</span></span>
    
      - <span data-ttu-id="573f3-137">Verwalten des Adressbuchservers über die Befehlszeile</span><span class="sxs-lookup"><span data-stu-id="573f3-137">Managing the Address Book Server from the command line</span></span>

  - <span data-ttu-id="573f3-138">**Verwalten von Benutzerkonten**   Die Verwaltung von Benutzerkonten umfasst Folgendes:</span><span class="sxs-lookup"><span data-stu-id="573f3-138">**Managing User Accounts**   Management of user accounts includes the following:</span></span>
    
      - <span data-ttu-id="573f3-139">Aktivieren von Benutzerkonten für lync Server</span><span class="sxs-lookup"><span data-stu-id="573f3-139">Enabling User Accounts for Lync Server</span></span>
    
      - <span data-ttu-id="573f3-140">Konfigurieren von lync Server-Benutzern mit dem Assistenten</span><span class="sxs-lookup"><span data-stu-id="573f3-140">Configuring Lync Server Users using the Wizard</span></span>
    
      - <span data-ttu-id="573f3-141">Konfigurieren der Eigenschaften einzelner lync Server-Benutzerkonten</span><span class="sxs-lookup"><span data-stu-id="573f3-141">Configuring Individual Lync Server User Account Properties</span></span>
    
      - <span data-ttu-id="573f3-142">Suchen nach lync Server-Benutzern</span><span class="sxs-lookup"><span data-stu-id="573f3-142">Searching for Lync Server Users</span></span>
    
      - <span data-ttu-id="573f3-143">Verschieben von lync Server-Benutzern</span><span class="sxs-lookup"><span data-stu-id="573f3-143">Moving Lync Server Users</span></span>
    
      - <span data-ttu-id="573f3-144">Löschen von lync Server-Benutzern</span><span class="sxs-lookup"><span data-stu-id="573f3-144">Deleting Lync Server Users</span></span>

  - <span data-ttu-id="573f3-145">**Analysieren von lync Server 2013-Protokolldateien**   Ein sehr hilfreiches Tool, das in der Regel für die Problembehandlung verwendet wird, ist das lync Server 2013-Protokollierungstool, das ausführlich unter [Verwenden des lync Server 2013-Protokollierungstools](https://technet.microsoft.com/library/gg558599.aspx)beschrieben wird.</span><span class="sxs-lookup"><span data-stu-id="573f3-145">**Analyzing Lync Server 2013 Log Files**   One very helpful tool, generally used for troubleshooting, is the Lync Server 2013 Logging Tool described in detail in [Using Lync Server 2013 Logging Tool](https://technet.microsoft.com/library/gg558599.aspx).</span></span>

<span data-ttu-id="573f3-146">Da das Protokollierungstool Protokolldateien (pro Server) generiert, können diese Protokolldateien mithilfe des Snooper-Tools angezeigt und analysiert werden, wenn die Microsoft Office Server 12 Resource Kit-Tools auf dem Computer installiert sind.</span><span class="sxs-lookup"><span data-stu-id="573f3-146">Because the Logging Tool generates log files (on a per-server basis), these log files can be viewed and analyzed by using the Snooper tool, if the Microsoft Office Server 12 Resource Kit Tools are installed on the computer.</span></span> <span data-ttu-id="573f3-147">Andernfalls können Protokolle auch mithilfe eines Text-Editors analysiert werden, der weitaus weniger transparent und komplexer als die Verwendung des Snooper-Dienstprogramms ist.</span><span class="sxs-lookup"><span data-stu-id="573f3-147">Otherwise, logs can also be analyzed by using a text editor, which is much less transparent and more complex than using the Snooper utility.</span></span>

<span data-ttu-id="573f3-148">So zeigen Sie Protokollnachrichten an und analysieren Sie</span><span class="sxs-lookup"><span data-stu-id="573f3-148">To View and Analyze Protocol Messages</span></span>

<span data-ttu-id="573f3-149">Wenn Sie im Protokollierungstool die Debugsitzung beendet haben, klicken Sie auf Protokolldateien analysieren, um die Protokolldateien mit dem Snooper-Tool anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="573f3-149">In the Logging Tool, when you have ended the debug session, click Analyze Log Files to view the log files by using the Snooper tool.</span></span> <span data-ttu-id="573f3-150">Sie können Protokoll Protokolle für die folgenden Komponenten analysieren:</span><span class="sxs-lookup"><span data-stu-id="573f3-150">You can analyze protocol logs for the following components:</span></span>

  - <span data-ttu-id="573f3-151">Lync Server SipStack (SIP)</span><span class="sxs-lookup"><span data-stu-id="573f3-151">Lync Server SipStack (SIP)</span></span>

  - <span data-ttu-id="573f3-152">Lync Server S4 (SIP)</span><span class="sxs-lookup"><span data-stu-id="573f3-152">Lync Server S4 (SIP)</span></span>

  - <span data-ttu-id="573f3-153">Lync Server Conferencing Signalisierungs Datenverkehr (C3P), einschließlich MCU Infra C3P und Fokus C3P</span><span class="sxs-lookup"><span data-stu-id="573f3-153">Lync Server Conferencing signaling traffic (C3P), including MCU Infra C3P and Focus C3P</span></span>

  - <span data-ttu-id="573f3-154">Lync Server Web Conferencing Traffic (PSOM)</span><span class="sxs-lookup"><span data-stu-id="573f3-154">Lync Server Web conferencing traffic (PSOM)</span></span>

  - <span data-ttu-id="573f3-155">Lync Server Unified Communications Client Platform-Client (uccp)</span><span class="sxs-lookup"><span data-stu-id="573f3-155">Lync Server Unified Communications Client Platform client (UCCP)</span></span>

  - <span data-ttu-id="573f3-156">Fehlerberichte aus der Archivierungsdatenbank</span><span class="sxs-lookup"><span data-stu-id="573f3-156">Error reports from the archiving database</span></span>

<span data-ttu-id="573f3-157">Informationen dazu, wie Sie die Leistung von erforderlichen Aufgaben organisieren können, finden Sie unter Checkliste für As-Needed Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="573f3-157">To help organize the performance of as-needed tasks, see As-Needed Operations Checklist.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="573f3-158">Detaillierte Verwaltungs-und Verwaltungsverfahren finden Sie im Microsoft lync Server 2013-Administratorhandbuch.</span><span class="sxs-lookup"><span data-stu-id="573f3-158">For detailed administration and management procedures, see the Microsoft Lync Server 2013 Administration Guide.</span></span>



</div>

<div>

## <a name="backup-and-restore-policies-or-configuration-settings"></a><span data-ttu-id="573f3-159">Sicherungs-und Wiederherstellungsrichtlinien oder Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="573f3-159">Backup (and restore) policies or configuration settings</span></span>

<span data-ttu-id="573f3-160">Mit lync Server 2013 können Sie das gesamte System sichern und wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="573f3-160">Lync Server 2013 lets you back up and restore the whole system.</span></span> <span data-ttu-id="573f3-161">Wenn Sie eine einzelne Richtlinie oder eine einzelne Sammlung von Konfigurationseinstellungen sichern (und dann möglicherweise irgendwann wiederherstellen) möchten, rufen Sie die entsprechende Richtlinie ab, und leiten Sie dieses Objekt dann an das Export-Clixml-Cmdlet weiter, wodurch die Richtlinieninformationen als XML-Datei gespeichert werden:</span><span class="sxs-lookup"><span data-stu-id="573f3-161">Iif you want to back up (and then maybe someday restore) a single policy or a single collection of configuration settings, retrieve the appropriate policy, and then pipe that object to the Export-Clixml cmdlet, which saves the policy information as an XML file:</span></span>

`Get-CsClientPolicy -Identity "RedmondClientPolicy" | Export-Clixml -Path C:\Backup\RedmondClientPolicy.xml`

<span data-ttu-id="573f3-162">Sie können jetzt mit RedmondClientPolicy experimentieren und viele Einstellungen ändern.</span><span class="sxs-lookup"><span data-stu-id="573f3-162">You may now experiment with RedmondClientPolicy and change lots of the settings.</span></span> <span data-ttu-id="573f3-163">Wenn Sie stattdessen die alte Richtlinie wiederherstellen möchten, geben Sie Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="573f3-163">If you decide instead to restore the old policy, enter:</span></span>

`$x = Import-Clixml -Path C:\Backup\RedmondClientPolicy.xml`

`Set-CsClientPolicy -Instance $x`

<span data-ttu-id="573f3-164">Beachten Sie, dass diese Vorgehensweise für die meisten Richtlinien und Einstellungen geeignet ist, aber nicht mit einigen der komplexeren Elemente (Elemente, die mehrere untergeordnete Objekte enthalten (wie Routing Konfigurationseinstellungen, die viele getrennte VoIP-Routen enthalten) funktionieren.</span><span class="sxs-lookup"><span data-stu-id="573f3-164">Note that this approach will work for most policies and settings but it won't work with some of the more complex items—items that contain multiple sub-objects (like routing configuration settings, which contain many separate voice routes).</span></span>

<span data-ttu-id="573f3-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="573f3-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

