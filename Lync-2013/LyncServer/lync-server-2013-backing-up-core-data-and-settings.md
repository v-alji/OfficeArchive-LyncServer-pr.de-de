---
title: 'Lync Server 2013: Sichern von Core-Daten und-Einstellungen'
description: 'Lync Server 2013: Sichern von Core-Daten und-Einstellungen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up core data and settings
ms:assetid: 278bc95a-7b8d-4e01-a872-a844830459de
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202170(v=OCS.15)
ms:contentKeyID: 51541452
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 637eeb950a3b8380f6e756f46a5083f51b5d7e1f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438099"
---
# <a name="backing-up-core-data-and-settings-in-lync-server-2013"></a><span data-ttu-id="dff61-103">Sichern von Kern Daten und-Einstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dff61-103">Backing up core data and settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dff61-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dff61-104">

<span> </span></span></span>

<span data-ttu-id="dff61-105">_**Letztes Änderungsdatum des Themas:** 2014-04-23_</span><span class="sxs-lookup"><span data-stu-id="dff61-105">_**Topic Last Modified:** 2014-04-23_</span></span>

<span data-ttu-id="dff61-106">Die folgenden Verfahren verwenden Cmdlets der lync Server-Verwaltungsshell zum Erstellen von Sicherungsdateien für Einstellungen und Daten für Kerndienste.</span><span class="sxs-lookup"><span data-stu-id="dff61-106">The following procedures use Lync Server Management Shell cmdlets to create backup files for settings and data for core services.</span></span> <span data-ttu-id="dff61-107">Details zu den in diesem Abschnitt verwendeten Tools, einschließlich ihrer Position, finden Sie unter [Sicherungs-und Wiederherstellungsanforderungen in lync Server 2013: Tools und Berechtigungen](lync-server-2013-backup-and-restoration-requirements-tools-and-permissions.md).</span><span class="sxs-lookup"><span data-stu-id="dff61-107">For details about the tools used in this section, including where they are located, see [Backup and restoration requirements in Lync Server 2013: tools and permissions](lync-server-2013-backup-and-restoration-requirements-tools-and-permissions.md).</span></span> <span data-ttu-id="dff61-108">Details zum Sichern von Archivierungs-und Überwachungsdaten finden Sie unter [Sichern von Archivierungs-und Überwachungsdatenbanken in lync Server 2013](lync-server-2013-backing-up-archiving-and-monitoring-databases.md).</span><span class="sxs-lookup"><span data-stu-id="dff61-108">For details about backing up Archiving and Monitoring data, see [Backing up Archiving and Monitoring databases in Lync Server 2013](lync-server-2013-backing-up-archiving-and-monitoring-databases.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="dff61-109">Der Schritt in diesem Abschnitt zum Sichern des zentralen Verwaltungsspeichers umfasst die Einstellungen und die Konfiguration für die Archivierung und Überwachung.</span><span class="sxs-lookup"><span data-stu-id="dff61-109">The step in this section to back up the Central Management store includes the settings and configuration for Archiving and Monitoring.</span></span>



</div>

<span data-ttu-id="dff61-110">Sie können die in diesem Abschnitt beschriebenen Cmdlets lokal oder Remote ausführen.</span><span class="sxs-lookup"><span data-stu-id="dff61-110">You can run the cmdlets described in this section locally or remotely.</span></span>

<div>

## <a name="to-back-up-core-data-and-settings"></a><span data-ttu-id="dff61-111">So sichern Sie Core-Daten und-Einstellungen</span><span class="sxs-lookup"><span data-stu-id="dff61-111">To back up core data and settings</span></span>

1.  <span data-ttu-id="dff61-112">Melden Sie sich von einem Benutzerkonto, das ein Mitglied der RTCUniversalServerAdmins-Gruppe ist, bei einem beliebigen Computer in ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="dff61-112">From a user account that is a member of the RTCUniversalServerAdmins group, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="dff61-113">Wenn Sie die in den folgenden Schritten erstellten Sicherungen speichern möchten, erstellen Sie einen neuen freigegebenen Ordner, und aktualisieren Sie den Pfad, auf den **$Backup** verweist, auf den neuen freigegebenen Ordner.</span><span class="sxs-lookup"><span data-stu-id="dff61-113">To store the backups you create in the following steps, create a new shared folder and update the path referenced by **$Backup** to the new shared folder.</span></span>

3.  <span data-ttu-id="dff61-114">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="dff61-114">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="dff61-115">Sichern Sie die Konfigurationsdatei des zentralen Verwaltungsspeichers.</span><span class="sxs-lookup"><span data-stu-id="dff61-115">Back up the Central Management store configuration file.</span></span> <span data-ttu-id="dff61-116">Geben Sie an der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="dff61-116">At the command line, type the following:</span></span>
    
        Export-CsConfiguration -FileName <path and file name for backup>
    
    <span data-ttu-id="dff61-117">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="dff61-117">For example:</span></span>
    
        Export-CsConfiguration -FileName "C:\Config.zip"
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="dff61-118">Mit diesem Schritt werden Ihre lync Server-Topologie,-Richtlinien und-Konfigurationseinstellungen in eine Datei exportiert.</span><span class="sxs-lookup"><span data-stu-id="dff61-118">This step exports your Lync Server topology, policies, and configuration settings to a file.</span></span> <span data-ttu-id="dff61-119">Zum Sichern von Topologiedaten ist kein anderer Schritt erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dff61-119">No other step is required to backup topology data.</span></span>

    
    </div>

5.  <span data-ttu-id="dff61-120">Kopieren Sie die gesicherte Konfigurationsdatei des zentralen Verwaltungsspeichers in $Backup \\ .</span><span class="sxs-lookup"><span data-stu-id="dff61-120">Copy the backed-up Central Management store configuration file to $Backup\\.</span></span>

6.  <span data-ttu-id="dff61-121">Sichern Sie die Daten des Standort Informationsdiensts.</span><span class="sxs-lookup"><span data-stu-id="dff61-121">Back up Location Information service data.</span></span> <span data-ttu-id="dff61-122">Geben Sie an der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="dff61-122">At the command line, type the following:</span></span>
    
        Export-CsLisConfiguration -FileName <path and file name for backup>
    
    <span data-ttu-id="dff61-123">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="dff61-123">For example:</span></span>
    
        Export-CsLisConfiguration -FileName "C:\E911Config.zip"

7.  <span data-ttu-id="dff61-124">Kopieren Sie die Konfigurationsdatei des gesicherten Standort Informationsdiensts in $Backup \\ .</span><span class="sxs-lookup"><span data-stu-id="dff61-124">Copy the backed-up Location Information service configuration file to $Backup\\.</span></span>

8.  <span data-ttu-id="dff61-125">Sichern Sie die Benutzerdaten in jeder Back-End-Datenbank eines Front-End-Pools und jedes Standard Edition-Servers.</span><span class="sxs-lookup"><span data-stu-id="dff61-125">Back up user data on every back-end database of a Front End pool and every Standard Edition server.</span></span> <span data-ttu-id="dff61-126">Geben Sie an der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="dff61-126">At the command line, type the following:</span></span>
    
        Export-CsUserData -PoolFQDN <Fqdn> -FileName <String>
    
    <span data-ttu-id="dff61-127">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="dff61-127">For example:</span></span>
    
        Export-CsUserData -PoolFQDN "atl-cs-001.litwareinc.com" -FileName "C:\Logs\ExportedUserData.zip"

9.  <span data-ttu-id="dff61-128">Kopieren Sie die gesicherte Benutzerdatei in $Backup \\ .</span><span class="sxs-lookup"><span data-stu-id="dff61-128">Copy the backed up user file to $Backup\\.</span></span>

10. <span data-ttu-id="dff61-129">Sichern Sie in jedem Pool, auf dem die reaktionsgruppenanwendung ausgeführt wird, die Konfiguration der Reaktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="dff61-129">On every pool that runs the Response Group application, back up the Response Group configuration.</span></span> <span data-ttu-id="dff61-130">Gehen Sie folgendermaßen vor:</span><span class="sxs-lookup"><span data-stu-id="dff61-130">Do the following:</span></span>
    
    1.  <span data-ttu-id="dff61-131">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="dff61-131">At the command line, type:</span></span>
        
            Export-CsRgsConfiguration -Source "service:ApplicationServer:<pool FQDN>" -FileName <path and file name for backup>
        
        <span data-ttu-id="dff61-132">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="dff61-132">For example:</span></span>
        
            Export-CsRgsConfiguration -Source ApplicationServer:pool01.contoso.com -FileName C:\RgsConfiguration.zip

11. <span data-ttu-id="dff61-133">Kopieren Sie die gesicherte Antwortgruppen-Konfigurationsdatei in $Backup \\ .</span><span class="sxs-lookup"><span data-stu-id="dff61-133">Copy the backed up Response Group configuration file to $Backup\\.</span></span>

<span data-ttu-id="dff61-134"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dff61-134"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

