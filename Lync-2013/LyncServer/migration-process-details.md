---
title: Migrationsprozess – Details
description: Migrationsprozess – Details.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migration process - details
ms:assetid: ca7e352c-9bde-47d9-8273-5cf2fdfdfe7e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205264(v=OCS.15)
ms:contentKeyID: 48185412
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b8ecc5f23a328aef7cc65ad84e28dbb629d44b91
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438603"
---
# <a name="migration-process---details"></a><span data-ttu-id="d50d3-103">Migrationsprozess – Details</span><span class="sxs-lookup"><span data-stu-id="d50d3-103">Migration process - details</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d50d3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d50d3-104">

<span> </span></span></span>

<span data-ttu-id="d50d3-105">_**Letztes Änderungsdatum des Themas:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="d50d3-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="d50d3-106">Verwenden Sie die folgenden Voraussetzungen und detaillierten Schritte zum Migrieren von lync Server 2010, Gruppen-Chat oder Office Communications Server 2007 R2-Gruppen-Chat zu lync Server 2013, beständiger Chat Server.</span><span class="sxs-lookup"><span data-stu-id="d50d3-106">Use the following prerequisites and detailed steps to migrate either Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server.</span></span>

<div>

## <a name="prerequisites-for-migration"></a><span data-ttu-id="d50d3-107">Voraussetzungen für die Migration</span><span class="sxs-lookup"><span data-stu-id="d50d3-107">Prerequisites for Migration</span></span>

<span data-ttu-id="d50d3-108">Stellen Sie sicher, dass Sie die folgenden Voraussetzungen erfüllt haben, bevor Sie entweder lync Server 2010, Gruppen-Chat oder Office Communications Server 2007 R2-Gruppen-Chat zu lync Server 2013, beständiger Chat Server, migrieren.</span><span class="sxs-lookup"><span data-stu-id="d50d3-108">Be sure that you’ve met the following prerequisites before migrating either Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server.</span></span>

1.  <span data-ttu-id="d50d3-109">Bereitstellen von mindestens einem lync Server 2013-Pool</span><span class="sxs-lookup"><span data-stu-id="d50d3-109">Deploy at least one Lync Server 2013 pool.</span></span> <span data-ttu-id="d50d3-110">Wenn Sie über mehrere lync Server 2013-Pools verfügen, entscheiden Sie, welcher lync Server 2013-Pool als privater Pool für den neuen lync Server 2013-Serverpool für beständige Chats festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="d50d3-110">If you have multiple Lync Server 2013 pools, decide which Lync Server 2013 pool will be the home pool for the new Lync Server 2013 Persistent Chat Server pool.</span></span>

2.  <span data-ttu-id="d50d3-111">Installieren Sie den Serverpool des lync Server 2013, beständigen Chats.</span><span class="sxs-lookup"><span data-stu-id="d50d3-111">Install the Lync Server 2013, Persistent Chat Server pool.</span></span> <span data-ttu-id="d50d3-112">Sie ist leer (keine Kategorien, Räume oder Add-Ins).</span><span class="sxs-lookup"><span data-stu-id="d50d3-112">It will be empty (no categories, rooms, or add-ins).</span></span> <span data-ttu-id="d50d3-113">Bevor Sie Ihre Legacy Kategorien,-Räume oder-Add-ins migrieren, können Sie Räume, Kategorien oder Add-Ins in ihrer lync Server 2013-Bereitstellung des beständigen Chats erstellen.</span><span class="sxs-lookup"><span data-stu-id="d50d3-113">Before you migrate your legacy categories, rooms, or add-ins, you can create rooms, categories, or add-ins in your Lync Server 2013, Persistent Chat Server deployment.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="d50d3-114">Beachten Sie, dass diese neu erstellten Elemente Konflikte mit Legacy Elementen verursachen können, die Sie migrieren.</span><span class="sxs-lookup"><span data-stu-id="d50d3-114">Be aware that these newly created items may conflict with legacy items that you migrate.</span></span> <span data-ttu-id="d50d3-115">Vermeiden Sie Namenskonflikte; Andernfalls werden Sie überschrieben, wenn die Legacydaten migriert werden.</span><span class="sxs-lookup"><span data-stu-id="d50d3-115">Avoid any naming conflicts; otherwise, they will be overwritten when the legacy data is migrated.</span></span>

    
    </div>

</div>

<div>

## <a name="preparing-the-source-data-for-migration"></a><span data-ttu-id="d50d3-116">Vorbereiten der Quelldaten für die Migration</span><span class="sxs-lookup"><span data-stu-id="d50d3-116">Preparing the Source Data for Migration</span></span>

<span data-ttu-id="d50d3-117">Führen Sie die folgenden Schritte aus, um die Quelldaten für die Migration richtig vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="d50d3-117">Perform the following steps to properly prepare your source data for migration.</span></span>

1.  <span data-ttu-id="d50d3-118">Sichern Sie die Quelldatenbanken für lync Server 2010, Gruppen-Chat oder Office Communications Server 2007 R2-Gruppen-Chat.</span><span class="sxs-lookup"><span data-stu-id="d50d3-118">Back up the source databases for either Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat.</span></span> <span data-ttu-id="d50d3-119">Details zum Sichern von SQL Server finden Sie unter "Übersicht über Sicherungen (SQL Server)" unter <https://go.microsoft.com/fwlink/p/?linkid=254851> .</span><span class="sxs-lookup"><span data-stu-id="d50d3-119">For details about backing up SQL Server, see "Backup Overview (SQL Server)" at <https://go.microsoft.com/fwlink/p/?linkid=254851>.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="d50d3-120">Die Active Directory-Domänendienste sollten identisch sein.</span><span class="sxs-lookup"><span data-stu-id="d50d3-120">Active Directory Domain Services should be the same.</span></span> <span data-ttu-id="d50d3-121">Als Bedingung für die Migration können Sie nicht zu einem Pool in einer anderen Bereitstellung (insbesondere in einer anderen Active Directory-Gesamtstruktur) migrieren.</span><span class="sxs-lookup"><span data-stu-id="d50d3-121">As a condition for migration, you cannot migrate to a pool in a different deployment (specifically, in a different Active Directory forest).</span></span>

    
    </div>

2.  <span data-ttu-id="d50d3-122">Überprüfen Sie Ihre lync Server 2010, Gruppen-Chat oder Office Communications Server 2007 R2-Gruppen-Chatrooms und die Kategorie-Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="d50d3-122">Inspect your Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat chat rooms and category configuration.</span></span> <span data-ttu-id="d50d3-123">Alle Änderungen an Kategorien, Räumen oder Add-Ins in Ihrer vorhandenen Legacy Bereitstellung werden vom Gruppen-Chat-Verwaltungs Tool ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d50d3-123">Any changes to categories, rooms, or add-ins in your existing legacy deployment will be done by the Group Chat Admin Tool.</span></span>
    
    <div>
    

    > [!TIP]  
    > <span data-ttu-id="d50d3-124">Alle Änderungen an Kategorien, Räumen oder Add-Ins in ihrer lync Server 2013-Bereitstellung des beständigen Chats werden von der lync Server Control Panel-oder Windows PowerShell-Cmdlets ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="d50d3-124">Any changes to categories, rooms, or add-ins in your Lync Server 2013, Persistent Chat Server deployment are performed by the Lync Server Control Panel or Windows PowerShell cmdlets.</span></span>

    
    </div>
    
    <span data-ttu-id="d50d3-125">Führen Sie die folgenden Schritte aus, um Ihr Legacy System für die Migration vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="d50d3-125">Follow these steps to prepare your legacy system for migration.</span></span>
    
    1.  <span data-ttu-id="d50d3-126">Der beständige Chat Server unterstützt eine einzelne Ebene von Kategorien, anders als eine Tiefe hierarchische Gruppe von Kategorien.</span><span class="sxs-lookup"><span data-stu-id="d50d3-126">Persistent Chat Server supports a single level of categories, unlike a deep hierarchical set of categories.</span></span> <span data-ttu-id="d50d3-127">Nach der Migration werden den Unterkategorien vollständige übergeordnete Kategorienamen vorangestellt.</span><span class="sxs-lookup"><span data-stu-id="d50d3-127">After migration, the subcategories are prefixed with full parent category names.</span></span> <span data-ttu-id="d50d3-128">Möglicherweise möchten Sie die vorhandene Kategorienstruktur vereinfachen und glätten, damit die resultierende Struktur Ihren Anforderungen entspricht.</span><span class="sxs-lookup"><span data-stu-id="d50d3-128">You might want to simplify and flatten your existing category structure so that the resulting structure meets your requirements.</span></span>
    
    2.  <span data-ttu-id="d50d3-129">Überprüfen Sie die **Manager** in der Stammkategorie.</span><span class="sxs-lookup"><span data-stu-id="d50d3-129">Verify the **Managers** at the root Category.</span></span> <span data-ttu-id="d50d3-130">Wenn Manager auf dieser Ebene vorhanden sind, werden diese Benutzer nach der Migration als **Manager zu allen Chatrooms** hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="d50d3-130">If any Managers exist at this level, these users will be added as **Managers to all rooms** after migration.</span></span> <span data-ttu-id="d50d3-131">Wenn dies für Ihre Organisation nicht erforderlich ist, müssen Sie diese Manager aus der Stammkategorie entfernen.</span><span class="sxs-lookup"><span data-stu-id="d50d3-131">If this is not a requirement for your organization, you need to remove these Managers from the root Category.</span></span>
    
    3.  <span data-ttu-id="d50d3-132">Überprüfen Sie die Länge von Raumnamen.</span><span class="sxs-lookup"><span data-stu-id="d50d3-132">Verify the length of room names.</span></span> <span data-ttu-id="d50d3-133">Wenn die Räume unter einer untergeordneten Kategorie vorhanden sind, werden Sie nach der Migration aufgrund vereinfachter Kategorie-Strukturen mit den vollständigen übergeordneten Kategorienamen belegt.</span><span class="sxs-lookup"><span data-stu-id="d50d3-133">After migration, due to simplified category structures, if the rooms exist under a child category, they are prefixed with full parent category names.</span></span> <span data-ttu-id="d50d3-134">Die Benennungs Grenze ist 256 Zeichen, einschließlich übergeordneter Kategorienamen.</span><span class="sxs-lookup"><span data-stu-id="d50d3-134">The naming limit is 256 characters, including parent category names.</span></span> <span data-ttu-id="d50d3-135">Sie müssen die Länge der Raumnamen überprüfen und möglicherweise die Länge verkürzen, wenn Sie zu lang sind.</span><span class="sxs-lookup"><span data-stu-id="d50d3-135">You must verify the length of the room names and possibly shorten the length, if they are too long.</span></span>
    
    4.  <span data-ttu-id="d50d3-136">Wenn in lync Server 2013 die Einstellungen für die Kategorie- **Einladungen** auf "true" festgelegt sind, können Sie für Einladungen zu Räumen unter dieser Kategorie "wahr" oder "falsch" auswählen.</span><span class="sxs-lookup"><span data-stu-id="d50d3-136">In Lync Server 2013, if the category **invitations** settings are set to true, you can choose true or false for invitations to rooms under that category.</span></span> <span data-ttu-id="d50d3-137">Wenn die Einstellungen für die Kategorie-Einladungen aber auf "falsch" festgelegt sind, werden in Räumen unter dieser Kategorie Einladungen deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d50d3-137">However if the category invitations settings are set to false, rooms under that category have invitations turned off.</span></span> <span data-ttu-id="d50d3-138">Vor der Migration müssen Sie die Einladungseinstellungen in ihrer älteren lync Server-Gruppen-Chat Server Version zurücksetzen, wenn Sie möchten, dass Raum (e) unter einer bestimmten Kategorie vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="d50d3-138">Before migration, you must reset the invitation settings in your legacy Lync Server Group Chat Server version, if you want room(s) to exist under a specific category.</span></span> <span data-ttu-id="d50d3-139">Andernfalls zeigt lync Server 2013 während der Migration Warnungen an und legt Räume auf den Standardwert false fest.</span><span class="sxs-lookup"><span data-stu-id="d50d3-139">Otherwise, during migration, Lync Server 2013 displays warnings and sets rooms to the default value of false.</span></span>
    
    5.  <span data-ttu-id="d50d3-140">Wenn Sie Dateien in Chatrooms verwendet haben, müssen Sie die Dateien nach der Migration manuell in den neuen beständigen Chat-Dateispeicher herunterladen.</span><span class="sxs-lookup"><span data-stu-id="d50d3-140">If you used files in chat rooms, you must XCOPY the files manually to the new Persistent Chat file store after migration.</span></span> <span data-ttu-id="d50d3-141">Die Tools tun dies nicht.</span><span class="sxs-lookup"><span data-stu-id="d50d3-141">The tools don’t do this.</span></span>
    
    6.  <span data-ttu-id="d50d3-142">Wenn Sie Verbundbenutzer und Chatrooms mit Verbundbenutzern hatten, beachten Sie, dass der Server für beständigen Chat keine Föderation unterstützt.</span><span class="sxs-lookup"><span data-stu-id="d50d3-142">If you had federated users and rooms with federated users, be aware that Persistent Chat Server does not support federation.</span></span> <span data-ttu-id="d50d3-143">Räume mit Verbundbenutzern werden migriert. die Benutzer können jedoch nicht auf die Inhalte zugreifen, da der Verbundzugriff nicht unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d50d3-143">Rooms with federated users will be migrated; however, the users themselves won’t be able to access the content, because federated access is not supported.</span></span>
    
    7.  <span data-ttu-id="d50d3-144">Identifizieren Sie die Chatrooms, die Sie nicht migrieren möchten, und markieren Sie Sie als deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d50d3-144">Identify those rooms that you do not want to migrate, and mark them as disabled.</span></span>
    
    8.  <span data-ttu-id="d50d3-145">Ermitteln Sie das Datum, über das Sie den Chatroom-Inhalt migrieren möchten.</span><span class="sxs-lookup"><span data-stu-id="d50d3-145">Identify the date beyond which you want to migrate the chat room content.</span></span> <span data-ttu-id="d50d3-146">So möchten Sie beispielsweise Nachrichten nicht vor dem 1. Januar 2010 migrieren, da diese Nachrichten möglicherweise veraltet oder für die Migration nicht relevant sind.</span><span class="sxs-lookup"><span data-stu-id="d50d3-146">For example, you may not want to migrate messages earlier than January 1, 2010, because these messages may be obsolete or not relevant for migration.</span></span>

</div>

<div>

## <a name="performing-the-migration"></a><span data-ttu-id="d50d3-147">Durchführen der Migration</span><span class="sxs-lookup"><span data-stu-id="d50d3-147">Performing the Migration</span></span>

<span data-ttu-id="d50d3-148">Führen Sie die folgenden Schritte aus, um Ihren Legacy-Gruppen-Chat Server zu migrieren.</span><span class="sxs-lookup"><span data-stu-id="d50d3-148">Perform the following steps to migrate your legacy Group Chat Server.</span></span>

1.  <span data-ttu-id="d50d3-149">Beenden Sie lync Server 2010, Gruppen-Chat, Office Communications Server 2007 R2-Gruppenchat oder lync Server 2013, beständige Chat Server Dienste.</span><span class="sxs-lookup"><span data-stu-id="d50d3-149">Shut down the Lync Server 2010, Group Chat, Office Communications Server 2007 R2 Group Chat or Lync Server 2013, Persistent Chat Server services.</span></span> <span data-ttu-id="d50d3-150">Damit alle Dienste gestoppt werden können, sollten Sie dies zu einem Zeitpunkt planen, zu dem genügend Ausfallzeiten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d50d3-150">All services must be stopped, so plan to do this at a time when there is enough downtime.</span></span> <span data-ttu-id="d50d3-151">Vergewissern Sie sich wie zuvor beschrieben, dass Sie Ihre aktuelle Gruppen-Chat-Datenbank sichern.</span><span class="sxs-lookup"><span data-stu-id="d50d3-151">As previously described, make sure to back up your current Group Chat database.</span></span>

2.  <span data-ttu-id="d50d3-152">Führen Sie das Cmdlet "Windows PowerShell **Export-CsPersistentChatData** " als Mitglied der Administratorrolle "beständiger Chat" (CsPersistentChatAdministrator) aus.</span><span class="sxs-lookup"><span data-stu-id="d50d3-152">Run the Windows PowerShell **Export-CsPersistentChatData** cmdlet as a member of the Persistent Chat administrator RBAC role (CsPersistentChatAdministrator).</span></span> <span data-ttu-id="d50d3-153">Details zu den Export/Import-Cmdlets finden Sie unter [Problembehandlung bei der Server Konfiguration für beständigen Chat mit Windows PowerShell-Cmdlets in lync Server 2013](lync-server-2013-troubleshooting-persistent-chat-server-configuration-using-windows-powershell-cmdlets.md).</span><span class="sxs-lookup"><span data-stu-id="d50d3-153">For details about the export/import cmdlets, see [Troubleshooting Persistent Chat Server configuration using Windows PowerShell cmdlets in Lync Server 2013](lync-server-2013-troubleshooting-persistent-chat-server-configuration-using-windows-powershell-cmdlets.md).</span></span>
    
    <span data-ttu-id="d50d3-154">Überprüfen Sie die exportierten Inhalte.</span><span class="sxs-lookup"><span data-stu-id="d50d3-154">Inspect the exported contents.</span></span>

3.  <span data-ttu-id="d50d3-155">Bevor Sie zum Importieren bereit sind, beenden Sie lync Server 2013, Server Dienste für beständigen Chat.</span><span class="sxs-lookup"><span data-stu-id="d50d3-155">Before you’re ready to import, shut down Lync Server 2013, Persistent Chat Server services.</span></span> <span data-ttu-id="d50d3-156">Damit alle Dienste gestoppt werden können, sollten Sie dies zu einem Zeitpunkt planen, zu dem genügend Ausfallzeiten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="d50d3-156">All services need to be stopped, so plan to do this at a time when there is enough downtime.</span></span>

4.  <span data-ttu-id="d50d3-157">Führen Sie eine Sicherungskopie der persistenten Chat-Datenbank aus, wenn Sie vor der Migration Kategorien, Räume oder Add-Ins in ihrer lync Server 2013-Bereitstellung erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="d50d3-157">Perform a backup of the Persistent Chat database if you had created any categories, rooms, or add-ins in your Lync Server 2013 deployment before the migration.</span></span> <span data-ttu-id="d50d3-158">Der Export/Import-Prozess kann die Legacydaten in die lync Server 2013-Bereitstellung zusammenführen, doch Sie möchten die Datenbank sichern, falls dieser Inhalt versehentlich überschrieben wird (beispielsweise, wenn Benennungskonflikte weiterhin vorhanden sind).</span><span class="sxs-lookup"><span data-stu-id="d50d3-158">The export/import process will be able to merge the legacy data into the Lync Server 2013 deployment, but you’ll want to back up the database in case that content is inadvertently overwritten (for example, if naming conflicts still exist).</span></span>

5.  <span data-ttu-id="d50d3-159">Führen Sie das Windows PowerShell **-Import-CsPersistentChatData-** Cmdlet (Import Tool) mit einem **WhatIf** -Befehl aus, um den Back-End-Server des beständigen Chat Server Pools mit migrierten Daten zu füllen.</span><span class="sxs-lookup"><span data-stu-id="d50d3-159">Run the Windows PowerShell **Import-CsPersistentChatData** cmdlet (import tool), with a **WhatIf** command to populate the Back End Server of the Persistent Chat Server pool with migrated data.</span></span> <span data-ttu-id="d50d3-160">Einige Konvertierungen erfolgen im Prozess, um dem vereinfachten Verwaltungsmodell gerecht zu werden.</span><span class="sxs-lookup"><span data-stu-id="d50d3-160">Some conversions happen in the process to accommodate the simplified administration model.</span></span> <span data-ttu-id="d50d3-161">Beheben Sie alle angezeigten Fehler oder Warnungen.</span><span class="sxs-lookup"><span data-stu-id="d50d3-161">Fix any errors or warnings that appear.</span></span>

6.  <span data-ttu-id="d50d3-162">Führen Sie das Cmdlet "beständiger Chat Server Windows PowerShell **-Import-CsPersistentChatData** " als Mitglied der Administratorrolle "beständiger Chat" (CsPersistentChatAdministrator) aus.</span><span class="sxs-lookup"><span data-stu-id="d50d3-162">Run the Persistent Chat Server Windows PowerShell **Import-CsPersistentChatData** cmdlet as a member of the Persistent Chat administrator RBAC role (CsPersistentChatAdministrator).</span></span> <span data-ttu-id="d50d3-163">Details zu den Export/Import-Cmdlets finden Sie unter [Problembehandlung bei der Server Konfiguration für beständigen Chat mit Windows PowerShell-Cmdlets in lync Server 2013](lync-server-2013-troubleshooting-persistent-chat-server-configuration-using-windows-powershell-cmdlets.md).</span><span class="sxs-lookup"><span data-stu-id="d50d3-163">For details about the export/import cmdlets, see [Troubleshooting Persistent Chat Server configuration using Windows PowerShell cmdlets in Lync Server 2013](lync-server-2013-troubleshooting-persistent-chat-server-configuration-using-windows-powershell-cmdlets.md).</span></span>

7.  <span data-ttu-id="d50d3-164">Sie müssen alle hochgeladenen Dateien (den gesamten Ordner) in den neuen lync Server 2013-Dateispeicher für persistente Chats übertragen.</span><span class="sxs-lookup"><span data-stu-id="d50d3-164">You must XCOPY all uploaded files (the entire folder) to the new Lync Server 2013, Persistent Chat file store.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="d50d3-165">Lync 2013 (Client) unterstützt das Hochladen oder Anzeigen von Dateien in Chatrooms nicht.</span><span class="sxs-lookup"><span data-stu-id="d50d3-165">The Lync 2013 (client) does not support uploading or viewing files in chat rooms.</span></span> <span data-ttu-id="d50d3-166">Sie können den Legacyclient weiterhin verwenden, um Dateien im Chatroom zu Posten und anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d50d3-166">You can still use the legacy client to post and view files in the room.</span></span>

    
    </div>

8.  <span data-ttu-id="d50d3-167">Portieren Sie lync Server 2010, Gruppen-Chat oder Office Communications Server 2007 R2-Gruppen-Chat-Nachschlage Server-URI zum lync Server 2013-Kontaktobjekt für beständigen Chat Server.</span><span class="sxs-lookup"><span data-stu-id="d50d3-167">Port the Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat Lookup Server URI to the Lync Server 2013, Persistent Chat Server contact object.</span></span> <span data-ttu-id="d50d3-168">Die folgenden Schritte sind erforderlich, wenn sich entweder Ihr lync 2010-Gruppen-Chat oder die Office Communicator 2007 R2-Gruppen-Chat-Clients nach der Migration ohne clientseitige Konfigurationsänderungen mit dem neuesten lync 2013, beständigen Chat (Client) verbinden müssen:</span><span class="sxs-lookup"><span data-stu-id="d50d3-168">The following steps are required if either your Lync 2010 Group Chat or Office Communicator 2007 R2 Group Chat clients need to connect to the latest Lync 2013, Persistent Chat (client) after migration without any client-side configuration changes:</span></span>
    
      - <span data-ttu-id="d50d3-169">Löschen Sie das OCSChat@ \<domainName\> . com Lookup Server-Benutzerkonto.</span><span class="sxs-lookup"><span data-stu-id="d50d3-169">Delete the ocschat@\<domainName\>.com Lookup Server user account.</span></span> <span data-ttu-id="d50d3-170">Dies wurde verwendet, um auf den Nachschlage Dienst in lync Server 2010, Gruppen-Chat, zu verweisen.</span><span class="sxs-lookup"><span data-stu-id="d50d3-170">This was used to point to the Lookup Service in Lync Server 2010, Group Chat.</span></span> <span data-ttu-id="d50d3-171">Sie können den Pool deinstallieren und vertrauenswürdige Einträge später entfernen.</span><span class="sxs-lookup"><span data-stu-id="d50d3-171">You can uninstall the pool and remove trusted entries later.</span></span>
    
      - <span data-ttu-id="d50d3-172">Erstellen Sie einen Legacy Endpunkt (Kontaktobjekt für beständigen Chat Server), indem Sie das Windows PowerShell **-Cmdlet New-CsPersistentChatEndpoint** mit dem identischen SIP-URI ausführen, damit der Legacyclient effektiv funktioniert, wenn der Dienst neu gestartet wird.</span><span class="sxs-lookup"><span data-stu-id="d50d3-172">Create a legacy endpoint (Persistent Chat Server contact object) by running the Windows PowerShell cmdlet, **New-CsPersistentChatEndpoint**, with the identical SIP URI so that the legacy client will work effectively when the service is restarted.</span></span>
    
    <span data-ttu-id="d50d3-173">Der obligatorische Migrationsprozess ist an diesem Punkt abgeschlossen.</span><span class="sxs-lookup"><span data-stu-id="d50d3-173">The mandatory migration process is complete at this point.</span></span> <span data-ttu-id="d50d3-174">Lync 2010-Gruppen-Chats (Clients) oder Office Communicator 2007 R2-Gruppen-Chat (Clients) können jetzt transparent eine Verbindung mit dem neuen beständigen Chat Server Pool herstellen.</span><span class="sxs-lookup"><span data-stu-id="d50d3-174">Lync 2010 Group Chat (clients) or Office Communicator 2007 R2 Group Chat (clients) can connect to the new Persistent Chat Server pool now, transparently.</span></span>
    
    <span data-ttu-id="d50d3-175">Befolgen Sie diese zusätzlichen Schritte zur Außerbetriebnahme für lync Server 2010, Gruppen-Chat oder Office Communications Server 2007 R2-Gruppen-Chat.</span><span class="sxs-lookup"><span data-stu-id="d50d3-175">Follow these additional decommissioning steps for Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat.</span></span>

9.  <span data-ttu-id="d50d3-176">Starten Sie die Server Dienste für beständigen Chat, indem Sie alle Computer im neuen beständigen Chat Serverpool aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d50d3-176">Start the Persistent Chat Server services by turning on all computers in the new Persistent Chat Server pool.</span></span>

10. <span data-ttu-id="d50d3-177">Verwenden Sie die lync Server-Systemsteuerung und die Windows PowerShell-Cmdlets, um zu überprüfen, ob die Daten erfolgreich migriert wurden.</span><span class="sxs-lookup"><span data-stu-id="d50d3-177">Use the Lync Server Control Panel and Windows PowerShell cmdlets to verify that the data has migrated successfully.</span></span>

11. <span data-ttu-id="d50d3-178">Deinstallieren Sie den lync 2010-Gruppen-Chat oder den Office Communicator 2007 R2-Gruppen-Chat von den Computern im Gruppen-Chat-Server Pool.</span><span class="sxs-lookup"><span data-stu-id="d50d3-178">Uninstall Lync 2010 Group Chat or Office Communicator 2007 R2 Group Chat from the computers in the Group Chat Server pool.</span></span>

12. <span data-ttu-id="d50d3-179">Löschen Sie die vertrauenswürdige Anwendung und den vertrauenswürdigen Anwendungspool mithilfe von Windows PowerShell-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="d50d3-179">Delete the trusted application and trusted application pool using Windows PowerShell cmdlets.</span></span> <span data-ttu-id="d50d3-180">Dadurch werden diese Elemente aus dem zentralen Verwaltungsspeicher und den zugehörigen TSE (Trusted Service Entries) aus dem Active Directory gelöscht.</span><span class="sxs-lookup"><span data-stu-id="d50d3-180">This deletes these items from the Central Management store and the associated Trusted Service Entries (TSEs) from the Active Directory.</span></span> <span data-ttu-id="d50d3-181">Alternativ funktioniert dieser Schritt mithilfe des Topologie-Generators (die vertrauenswürdigen Anwendungen/Pools verfügen ebenfalls über einen dedizierten Knoten).</span><span class="sxs-lookup"><span data-stu-id="d50d3-181">Alternatively, this step works by using the Topology Builder (the trusted applications/pools have a dedicated node there, also).</span></span>

13. <span data-ttu-id="d50d3-182">Sie können jetzt beginnen, die Funktion des beständigen Chat Servers über die neuen Clients zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="d50d3-182">You can now begin to enable Persistent Chat Server functionality through the new clients.</span></span> <span data-ttu-id="d50d3-183">Ausführliche Informationen zum Aktivieren des Servers für beständigen Chat finden Sie unter [Bereitstellen eines persistenten Chat Servers in lync Server 2013](lync-server-2013-deploying-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="d50d3-183">For details about enabling Persistent Chat Server, see [Deploying Persistent Chat Server in Lync Server 2013](lync-server-2013-deploying-persistent-chat-server.md).</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="d50d3-184">Lync Server 2013 unterstützt mehrere Server Pools für beständigen Chat.</span><span class="sxs-lookup"><span data-stu-id="d50d3-184">Lync Server 2013 supports multiple Persistent Chat Server pools.</span></span> <span data-ttu-id="d50d3-185">Wir unterstützen allerdings die Migration eines lync 2010-Gruppen-oder Office Communications Server 2007 R2 &nbsp; -Gruppen-Chat Pools zu einem einzelnen lync Server 2013, beständigen Chat Serverpool.</span><span class="sxs-lookup"><span data-stu-id="d50d3-185">However, we support migrating a Lync 2010 Group Chat or Office Communications Server 2007 R2&nbsp;Group Chat pool to a single Lync Server 2013, Persistent Chat Server pool.</span></span> <span data-ttu-id="d50d3-186">Sie können weitere neue Server Pools für beständigen Chat in Ihrer Bereitstellung hinzufügen, um die regulatorischen Anforderungen zu erfüllen (beispielsweise das Beibehalten von Daten in einer bestimmten geografischen Region).</span><span class="sxs-lookup"><span data-stu-id="d50d3-186">You can add additional new Persistent Chat Server pools in your deployment to meet the regulatory needs (for example, keeping data within a given geography).</span></span>

    
    <span data-ttu-id="d50d3-187"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d50d3-187"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

