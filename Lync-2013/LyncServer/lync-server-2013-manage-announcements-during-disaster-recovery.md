---
title: 'Lync Server 2013: Verwalten von Ansagen während der Notfallwiederherstellung'
description: 'Lync Server 2013: Verwalten von Ankündigungen während der Notfallwiederherstellung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage announcements during disaster recovery
ms:assetid: c33e51ea-421f-42d2-826b-b73968f6bd5b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721874(v=OCS.15)
ms:contentKeyID: 49733807
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d85dfcd15c9c3650bafafa6fa7702e19ac9c4f7d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426123"
---
# <a name="manage-announcements-during-disaster-recovery-in-lync-server-2013"></a><span data-ttu-id="07f06-103">Verwalten von Ansagen während der Notfallwiederherstellung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="07f06-103">Manage announcements during disaster recovery in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="07f06-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="07f06-104">

<span> </span></span></span>

<span data-ttu-id="07f06-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="07f06-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="07f06-106">Lync Server 2013 unterstützt Ankündigungen für Anrufe an nicht zugewiesene Nummern während Ausfällen.</span><span class="sxs-lookup"><span data-stu-id="07f06-106">Lync Server 2013 supports announcements for calls to unassigned numbers during outages.</span></span> <span data-ttu-id="07f06-107">Das Wiederherstellen der Ankündigungsfunktion während eines Ausfalls ist optional.</span><span class="sxs-lookup"><span data-stu-id="07f06-107">Restoring announcement functionality during an outage is optional.</span></span> <span data-ttu-id="07f06-108">Wenn Sie Ankündigungen während eines Ausfalls wiederherstellen möchten, müssen Sie Ihre Ankündigungs Konfiguration im Sicherungspool erneut erstellen.</span><span class="sxs-lookup"><span data-stu-id="07f06-108">If you choose to restore announcements during an outage, you need recreate your announcement configuration in the backup pool.</span></span> <span data-ttu-id="07f06-109">In diesem Abschnitt wird beschrieben, was Sie tun müssen, wenn Sie Ankündigungen während der Disaster Recovery wiederherstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="07f06-109">This section describes what you need to do if you choose to restore announcements during disaster recovery.</span></span>

<span data-ttu-id="07f06-110">Dieser Abschnitt gilt für nicht zugewiesene Nummernbereiche, in denen die Ankündigungs Anwendung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="07f06-110">This section applies to unassigned number ranges that use the Announcement application.</span></span> <span data-ttu-id="07f06-111">Dieser Abschnitt gilt nicht für nicht zugewiesene Nummernbereiche, die die automatische UM-Telefonzentrale (Exchange Unified Messaging) verwenden.</span><span class="sxs-lookup"><span data-stu-id="07f06-111">This section does not apply to unassigned number ranges that use Exchange Unified Messaging (UM) Auto Attendant.</span></span>

<div>

## <a name="before-an-outage"></a><span data-ttu-id="07f06-112">Vor einem Ausfall</span><span class="sxs-lookup"><span data-stu-id="07f06-112">Before an Outage</span></span>

<span data-ttu-id="07f06-113">Unabhängig davon, ob Sie Ankündigungen während Ausfällen verwenden, sollten Sie separate Sicherungen aller angepassten Audiodateien vornehmen, die Sie für die Ankündigungs Anwendung konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="07f06-113">Regardless of whether you choose to use announcements during outages, you should take separate backups of any customized audio files that you configured for the Announcement application.</span></span> <span data-ttu-id="07f06-114">Angepasste Ankündigungen werden im Rahmen des lync Server Disaster Recovery-Prozesses nicht gesichert.</span><span class="sxs-lookup"><span data-stu-id="07f06-114">Customized announcements are not backed up as part of the Lync Server disaster recovery process.</span></span> <span data-ttu-id="07f06-115">Wenn Sie keine separaten Sicherungen der Dateien vornehmen und die Dateien, die Sie auf den Server oder Pool hochgeladen haben, beschädigt, beschädigt oder gelöscht sind, gehen die Dateien verloren.</span><span class="sxs-lookup"><span data-stu-id="07f06-115">If you do not take separate backups of the files and the files that you uploaded to the server or pool are damaged, corrupted, or erased, the files will be lost.</span></span>

<span data-ttu-id="07f06-116">Wenn Sie keine Sicherungskopien von angepassten Audiodateien haben und die ursprünglichen Audiodateien nicht mehr zur Verfügung stehen, können Sie die Audiodateien finden, die Sie für eine Ankündigungs Anwendung konfiguriert haben, indem Sie im Dateispeicher nach dem Server oder Pool suchen, in dem Sie die Dateien ursprünglich importiert haben.</span><span class="sxs-lookup"><span data-stu-id="07f06-116">If you do not have backup copies of customized audio files, and the original audio files are no longer available, you can find the audio files that you configured for an Announcement application by looking in the File Store for the server or pool where you originally imported the files.</span></span> <span data-ttu-id="07f06-117">Sie können alle Audiodateien kopieren, die Sie für die Ankündigungs Anwendung konfiguriert haben, aus dem Dateispeicher.</span><span class="sxs-lookup"><span data-stu-id="07f06-117">You can copy all the audio files that you configured for the Announcement application from the File Store.</span></span>

<span data-ttu-id="07f06-118">**So kopieren Sie Audiodateien aus dem Dateispeicher**</span><span class="sxs-lookup"><span data-stu-id="07f06-118">**To copy audio files from the file store**</span></span>

1.  <span data-ttu-id="07f06-119">Führen Sie an der Eingabeaufforderung folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="07f06-119">At the command line, run:</span></span>
    
        Xcopy <Source: Pool Announcement Service File Store path> <Destination>
    
    <span data-ttu-id="07f06-120">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="07f06-120">For example:</span></span>
    
        Xcopy "<Pool File Store Path>\X-ApplicationServer-X\AppServerFiles\RGS\AS" "<Destination: Backup location>"
    
    <span data-ttu-id="07f06-121">Wobei x-ApplicationServer-x auf die Dienst-ID des Anwendungsservers des Pools verweist (beispielsweise 1-ApplicationServer-1 ")</span><span class="sxs-lookup"><span data-stu-id="07f06-121">Where X-ApplicationServer-X refers to the service ID of the Application Server of the pool (for example, 1-ApplicationServer-1")</span></span>


</div>

<div>

## <a name="during-an-outage"></a><span data-ttu-id="07f06-122">Bei einem Ausfall</span><span class="sxs-lookup"><span data-stu-id="07f06-122">During an Outage</span></span>

<span data-ttu-id="07f06-123">Wenn Sie die Ankündigungs Anwendung während eines Ausfalls verwenden möchten, müssen Sie die Ankündigungs Konfiguration im Sicherungspool neu erstellen, indem Sie die in diesem Abschnitt beschriebenen Aufgaben ausführen.</span><span class="sxs-lookup"><span data-stu-id="07f06-123">To use the Announcement application during an outage, you need to recreate the announcement configuration in the backup pool by performing the tasks described in this section.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="07f06-124">Wir empfehlen, dass Sie diese Aufgaben ausführen, nachdem Sie das Failover für den Sicherungspool durchgeführt haben, denn sobald Sie Schritt 2 ausführen, übernimmt der Sicherungspool den Besitz der nicht zugewiesenen Nummernbereiche.</span><span class="sxs-lookup"><span data-stu-id="07f06-124">We recommend that you perform these tasks after you fail over to the backup pool, because as soon as you perform step 2, the backup pool takes ownership of the unassigned number ranges.</span></span>



</div>

<div>


> [!NOTE]  
> <span data-ttu-id="07f06-125">Diese Schritte sind für Nummernbereiche, die eine Telefonnummer der automatischen Exchange UM-Telefonzentrale verwenden, nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="07f06-125">These steps are not required for number ranges that use an Exchange UM Auto Attendant phone number.</span></span>



</div>

<span data-ttu-id="07f06-126">**So erstellen Sie die Ankündigungs Konfiguration im Sicherungspool erneut**</span><span class="sxs-lookup"><span data-stu-id="07f06-126">**To recreate the announcement configuration in the backup pool**</span></span>

1.  <span data-ttu-id="07f06-127">Erstellen Sie die Ankündigungen, die Sie im primären Pool im Sicherungspool bereitgestellt haben, wie folgt neu:</span><span class="sxs-lookup"><span data-stu-id="07f06-127">Recreate the announcements that you deployed in the primary pool in the backup pool by doing the following:</span></span>
    
    1.  <span data-ttu-id="07f06-128">Importieren Sie alle im primären Pool verwendeten Audiodateien in den Sicherungspool mithilfe des Cmdlets " **Import-CsAnnouncementFile** ", und geben Sie den Sicherungspool für den übergeordneten Parameter an.</span><span class="sxs-lookup"><span data-stu-id="07f06-128">Import any audio files used in the primary pool to the backup pool by using the **Import-CsAnnouncementFile** cmdlet and specifying the backup pool for the Parent parameter.</span></span>
    
    2.  <span data-ttu-id="07f06-129">Erstellen Sie die einzelnen Ankündigungen neu, indem Sie das Cmdlet **New-CsAnnouncement** verwenden und den Sicherungspool für den übergeordneten Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="07f06-129">Recreate each announcement by using the **New-CsAnnouncement** cmdlet and specifying the backup pool for the Parent parameter.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="07f06-130">Details zur Verwendung dieser Parameter zum Erstellen von Ankündigungen im Sicherungspool finden Sie unter <A href="lync-server-2013-create-an-announcement.md">Erstellen einer Ankündigung in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="07f06-130">For details about using these parameters to create announcements in the backup pool, see <A href="lync-server-2013-create-an-announcement.md">Create an announcement in Lync Server 2013</A>.</span></span>

    
    </div>

2.  <span data-ttu-id="07f06-131">Nachdem alle Ankündigungen im Sicherungspool neu erstellt wurden, leiten Sie alle nicht zugewiesenen Nummernbereiche, die Ankündigungen im primären Pool verwenden, auf die neu erstellten Ankündigungen im Sicherungspool um.</span><span class="sxs-lookup"><span data-stu-id="07f06-131">After all announcements are recreated in the backup pool, redirect all the unassigned number ranges that use announcements in the primary pool to the recreated announcements in the backup pool.</span></span>
    
    <span data-ttu-id="07f06-132">Führen Sie für jeden nicht zugewiesenen Nummernbereich, der eine Ankündigung im primären Pool verwendet, die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="07f06-132">For each unassigned number range that uses an announcement in the primary pool, run the following:</span></span>
    
        Set-CsUnassignedNumber -Identity "<name of number range>" -AnnouncementService "<FQDN of backup pool>" -AnnouncementName "<announcement name in backup pool>"

</div>

<div>

## <a name="after-the-outage"></a><span data-ttu-id="07f06-133">Nach dem Ausfall</span><span class="sxs-lookup"><span data-stu-id="07f06-133">After the Outage</span></span>

<span data-ttu-id="07f06-134">Wenn der primäre Pool verfügbar wird, müssen Sie die nicht zugewiesenen Nummernbereiche, die Sie für den Ausfall geändert haben, wieder in den primären Pool umleiten.</span><span class="sxs-lookup"><span data-stu-id="07f06-134">When the primary pool becomes available, you need to redirect the unassigned number ranges that you changed for the outage back to the primary pool.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="07f06-135">Diese Schritte sind für Nummernbereiche, die eine Telefonnummer der automatischen Exchange UM-Telefonzentrale verwenden, nicht erforderlich.</span><span class="sxs-lookup"><span data-stu-id="07f06-135">These steps are not required for number ranges that use an Exchange UM Auto Attendant phone number.</span></span>



</div>

<span data-ttu-id="07f06-136">**So stellen Sie Ankündigungen im primären Pool wieder her**</span><span class="sxs-lookup"><span data-stu-id="07f06-136">**To restore announcements in the primary pool**</span></span>

1.  <span data-ttu-id="07f06-137">Wenn Sie den primären Pool während der Wiederherstellung wiederherstellen mussten, müssen Sie die Ankündigungen im primären Pool neu erstellen, indem Sie die Audiodateien importieren und Ankündigungen erstellen, genau wie im Sicherungspool, mit der Ausnahme, dass Sie den primären Pool für den übergeordneten Parameter angeben.</span><span class="sxs-lookup"><span data-stu-id="07f06-137">If you had to rebuild the primary pool during the recovery, you need to recreate the announcements in the primary pool by importing the audio files and creating announcements, just as you did in the backup pool, except that you specify the primary pool for the Parent parameter.</span></span> <span data-ttu-id="07f06-138">Ausführliche Informationen finden Sie unter "während eines Ausfalls" weiter oben in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="07f06-138">For details, see "During an Outage" earlier in this topic.</span></span>

2.  <span data-ttu-id="07f06-139">Führen Sie für jeden nicht zugewiesenen Nummernbereich, den Sie für den Ausfall geändert haben, die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="07f06-139">For each unassigned number range that you changed for the outage, run the following:</span></span>
    
        Set-CsUnassignedNumber [-Identity "<name of number range>"] -AnnouncementService "<FQDN of primary pool>" -AnnouncementName "<announcement name in primary pool>"

3.  <span data-ttu-id="07f06-140">Optional können Sie die im Sicherungspool neu erstellten Ankündigungen entfernen.</span><span class="sxs-lookup"><span data-stu-id="07f06-140">Optionally, remove the announcements that you recreated in the backup pool.</span></span> <span data-ttu-id="07f06-141">Rufen Sie eine Liste der Ankündigungen für die APP für die Backup-Pool Ankündigung ab.</span><span class="sxs-lookup"><span data-stu-id="07f06-141">Get a list of announcements for the backup pool Announcement application.</span></span> <span data-ttu-id="07f06-142">Führen Sie an der Eingabeaufforderung folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="07f06-142">At the command line, run:</span></span>
    
        Get-CsAnnouncement -Identity "<Service:service ID>"
    
    <span data-ttu-id="07f06-143">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="07f06-143">For example:</span></span>
    
        Get-CsAnnouncement -Identity "ApplicationServer:redmond.contoso.com
    
    <span data-ttu-id="07f06-144">Suchen Sie in der resultierenden Liste die Ankündigungen, die Sie entfernen möchten, und kopieren Sie die GUIDs.</span><span class="sxs-lookup"><span data-stu-id="07f06-144">In the resulting list, locate the announcements you want to remove and copy the GUIDs.</span></span> <span data-ttu-id="07f06-145">Führen Sie für jede Ankündigung, die Sie entfernen möchten, Folgendes aus:</span><span class="sxs-lookup"><span data-stu-id="07f06-145">For each announcement you want to remove, run:</span></span>
    
        Remove-CsAnnouncement -Identity "<Service:service ID/guid>"
    
    <span data-ttu-id="07f06-146">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="07f06-146">For example:</span></span>
    
        Remove-CsAnnouncement -Identity "ApplicationServer:redmond.contoso.com/1951f734-c80f-4fb2-965d-51807c792b90"


<span data-ttu-id="07f06-147"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="07f06-147"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

