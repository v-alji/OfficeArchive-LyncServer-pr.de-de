---
title: 'Lync Server 2013: bewährte Methoden für Sicherung und Wiederherstellung'
description: 'Lync Server 2013: bewährte Methoden für Sicherung und Wiederherstellung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Best practices for backup and restoration
ms:assetid: abbce0e4-973a-4624-a0c1-e0f22e1d348b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh202184(v=OCS.15)
ms:contentKeyID: 51541500
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3e8875f03a7b4445af8274ef059f3abad4d21ff8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437889"
---
# <a name="best-practices-for-backup-and-restoration-for-lync-server-2013"></a><span data-ttu-id="565e3-103">Bewährte Methoden für die Sicherung und Wiederherstellung für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="565e3-103">Best practices for backup and restoration for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="565e3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="565e3-104">

<span> </span></span></span>

<span data-ttu-id="565e3-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="565e3-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="565e3-106">Dieser Abschnitt enthält zwei Arten von bewährten Methoden:</span><span class="sxs-lookup"><span data-stu-id="565e3-106">This section includes two types of best practices:</span></span>

  - <span data-ttu-id="565e3-107">Bewährte Methoden für Sicherung und Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="565e3-107">Best practices for backup and restoration.</span></span>

  - <span data-ttu-id="565e3-108">Bewährte Methoden zum Minimieren der Auswirkungen eines Notfalls</span><span class="sxs-lookup"><span data-stu-id="565e3-108">Best practices for minimizing the impact of a disaster.</span></span>

<div>

## <a name="best-practices-for-backup-and-restoration"></a><span data-ttu-id="565e3-109">Bewährte Methoden für Sicherung und Wiederherstellung</span><span class="sxs-lookup"><span data-stu-id="565e3-109">Best Practices for Backup and Restoration</span></span>

<span data-ttu-id="565e3-110">Wenden Sie beim Sichern oder Wiederherstellen Ihrer Daten die folgenden bewährten Methoden an, um den Sicherungs-und Wiederherstellungsprozess zu vereinfachen:</span><span class="sxs-lookup"><span data-stu-id="565e3-110">To facilitate your backup and restoration process, apply the following best practices when you back up or restore your data:</span></span>

  - <span data-ttu-id="565e3-111">Führen Sie regelmäßige Sicherungen in angemessenen Abständen aus.</span><span class="sxs-lookup"><span data-stu-id="565e3-111">Perform regular backups at appropriate intervals.</span></span> <span data-ttu-id="565e3-112">Der einfachste und am häufigsten verwendete Backup-Typ und-Rotations Zeitplan ist eine vollständige, nächtliche Sicherung der gesamten SQL Server-Datenbank.</span><span class="sxs-lookup"><span data-stu-id="565e3-112">The simplest and most commonly used backup type and rotation schedule is a full, nightly backup of the entire SQL Server database.</span></span> <span data-ttu-id="565e3-113">Wenn die Wiederherstellung erforderlich ist, erfordert der Wiederherstellungsprozess nur eine Sicherung, und es sollten nicht mehr als die Daten eines Tages verloren gehen.</span><span class="sxs-lookup"><span data-stu-id="565e3-113">Then, if restoration is necessary, the restoration process requires only one backup, and no more than a day’s data should be lost.</span></span>

  - <span data-ttu-id="565e3-114">Wenn Sie mithilfe von Cmdlets oder der lync Server-Systemsteuerung Konfigurationsänderungen vornehmen, verwenden Sie das Cmdlet **Export-CsConfiguration** , um eine Snapshot-Sicherung der Topologie-Konfigurationsdatei (XDS. mdf) zu erstellen, nachdem Sie die Änderungen vorgenommen haben, damit die Änderungen nicht verloren gehen, wenn Sie die Datenbanken wiederherstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="565e3-114">If you use cmdlets or the Lync Server Control Panel to make configuration changes, use the **Export-CsConfiguration** cmdlet to take a snapshot backup of the topology configuration file (Xds.mdf) after you make the changes, so that you won't lose the changes if you need to restore your databases.</span></span> <span data-ttu-id="565e3-115">Beachten Sie, dass diese Konfiguration im XML-Format gesichert und als ZIP-Datei komprimiert wird.</span><span class="sxs-lookup"><span data-stu-id="565e3-115">Note that this configuration is backed up in XML format and compressed as a ZIP file.</span></span>

  - <span data-ttu-id="565e3-116">Stellen Sie sicher, dass der freigegebene Ordner, den Sie zum Sichern von lync Server verwenden möchten, über genügend Speicherplatz verfügt, um alle gesicherten Daten zu speichern.</span><span class="sxs-lookup"><span data-stu-id="565e3-116">Make sure that the shared folder you plan to use for backing up Lync Server has sufficient disk space to hold all the backed up data.</span></span>

  - <span data-ttu-id="565e3-117">Planen Sie Sicherungen, wenn die lync Server-Auslastung in der Regel gering ist, um die Serverleistung und die Benutzerfreundlichkeit zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="565e3-117">Schedule backups when Lync Server usage is typically low, to improve server performance and user experience.</span></span>

  - <span data-ttu-id="565e3-118">Stellen Sie sicher, dass der Speicherort, an dem Sie Daten sichern, sicher ist (Wir empfehlen einen Remotestandort).</span><span class="sxs-lookup"><span data-stu-id="565e3-118">Make sure that the location where you back up data is secure (we recommend a remote location).</span></span>

  - <span data-ttu-id="565e3-119">Bewahren Sie die Sicherungsdateien auf, wo Sie verfügbar sein werden, falls Sie die Daten wiederherstellen müssen.</span><span class="sxs-lookup"><span data-stu-id="565e3-119">Keep the backup files where they will be available, in case you need to restore the data.</span></span>

  - <span data-ttu-id="565e3-120">Planen und planen Sie regelmäßige Tests der Wiederherstellungsprozesse, die von Ihrer Organisation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="565e3-120">Plan for and schedule periodic testing of the restoration processes that are supported by your organization.</span></span>

  - <span data-ttu-id="565e3-121">Überprüfen Sie Ihre Sicherungs-und Wiederherstellungsprozesse im voraus, um sicherzustellen, dass Sie wie erwartet funktionieren.</span><span class="sxs-lookup"><span data-stu-id="565e3-121">Validate your backup and restoration processes in advance to make sure that they work as expected.</span></span>

</div>

<div>

## <a name="best-practices-for-minimizing-the-impact-of-a-disaster"></a><span data-ttu-id="565e3-122">Bewährte Methoden zum Minimieren der Auswirkungen eines Notfalls</span><span class="sxs-lookup"><span data-stu-id="565e3-122">Best Practices for Minimizing the Impact of a Disaster</span></span>

<span data-ttu-id="565e3-123">Die beste Strategie für den Umgang mit katastrophalen Dienstunterbrechungen (verursacht durch nicht verwaltbare Ereignisse wie Stromausfälle oder plötzliche Hardwareausfälle) besteht darin, davon auszugehen, dass dies geschieht, und entsprechend zu planen.</span><span class="sxs-lookup"><span data-stu-id="565e3-123">The best strategy for dealing with disastrous service interruptions (caused by unmanageable events such as power outages or sudden hardware failures) is to assume they will happen, and to plan accordingly.</span></span>

<span data-ttu-id="565e3-124">Wenn die lync-Dienste mit einem mindestunterbrechungs-und Ausfallrisiko für Ihre Organisation unternehmenskritisch sind, sollten Sie in der Lage sein, gekoppelte Pools von Front-End-Servern zu implementieren, wie unter [Planen von hoher Verfügbarkeit und Disaster Recovery in lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md)beschrieben.</span><span class="sxs-lookup"><span data-stu-id="565e3-124">If Lync services, with a minimum of disruption and outage, are business-critical for your organization, you should consider implementing paired pools of Front End Servers, as described in [Planning for high availability and disaster recovery in Lync Server 2013](lync-server-2013-planning-for-high-availability-and-disaster-recovery.md).</span></span> <span data-ttu-id="565e3-125">Wenn eines dieser Pools einen Notfall hat, kann ein Administrator die Benutzer des Pools so umschalten, dass Sie mit einem mindestausfall von einem anderen Pool bedient werden.</span><span class="sxs-lookup"><span data-stu-id="565e3-125">Then, if one of these pools has a disaster, an administrator can switch the users of that pool to be served by the other pool, with a minimum of downtime.</span></span>

<span data-ttu-id="565e3-126">Die Notfall Verwaltungspläne, die Sie im Rahmen ihrer Sicherungs-und Wiederherstellungsstrategie entwickeln, sollten Folgendes umfassen:</span><span class="sxs-lookup"><span data-stu-id="565e3-126">The disaster management plans that you develop as part of your backup and restoration strategy should include the following:</span></span>

  - <span data-ttu-id="565e3-127">Sie können Ihr Software-Medium sowie Ihre Software-und Firmware-Updates bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="565e3-127">Keeping your software media, and your software and firmware updates, readily available.</span></span>

  - <span data-ttu-id="565e3-128">Verwalten von Hardware-und Software Datensätzen</span><span class="sxs-lookup"><span data-stu-id="565e3-128">Maintaining hardware and software records.</span></span>

  - <span data-ttu-id="565e3-129">Regelmäßiges Sichern Ihrer Daten und Überwachen der Integrität Ihrer Sicherungen</span><span class="sxs-lookup"><span data-stu-id="565e3-129">Backing up your data regularly and monitoring the integrity of your backups.</span></span>

  - <span data-ttu-id="565e3-130">Schulung Ihrer Mitarbeiter in Disaster Recovery, Dokumentation von Verfahren und Implementierung von Disaster Recovery-Simulationsübungen.</span><span class="sxs-lookup"><span data-stu-id="565e3-130">Training your staff in disaster recovery, documenting procedures, and implementing disaster recovery simulation drills.</span></span>

  - <span data-ttu-id="565e3-131">Wenn Sie Ersatzhardware zur Verfügung haben oder wenn Sie über einen Service Level Agreement (SLA) verfügen, können Sie sich mit Hardwareanbietern und Lieferanten für den sofortigen Austausch beauftragen.</span><span class="sxs-lookup"><span data-stu-id="565e3-131">Keeping spare hardware available, or, if you have a service level agreement (SLA), contracting with hardware vendors and suppliers for prompt replacements.</span></span>

  - <span data-ttu-id="565e3-132">Trennen des Speicherorts ihrer Transaktionsprotokolldateien (LDF-Dateien) und Datenbankdateien (MDF-Dateien)</span><span class="sxs-lookup"><span data-stu-id="565e3-132">Separating the location of your transaction log files (.ldf files) and database files (.mdf files).</span></span>

<span data-ttu-id="565e3-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="565e3-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

