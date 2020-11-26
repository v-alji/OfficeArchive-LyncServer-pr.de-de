---
title: 'Lync Server 2013: Importieren der lync Server 2013-Verwaltungspakete'
description: 'Lync Server 2013: Importieren der lync Server 2013-Verwaltungspakete'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Importing the Lync Server 2013 management packs
ms:assetid: 846287e1-660f-453f-bdba-b2137b5f0ea1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205052(v=OCS.15)
ms:contentKeyID: 48184690
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c9615e559baf2f1c8b99015f1e407230559ff770
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427327"
---
# <a name="importing-the-lync-server-2013-management-packs"></a><span data-ttu-id="1b102-103">Importieren der lync Server 2013-Verwaltungspakete</span><span class="sxs-lookup"><span data-stu-id="1b102-103">Importing the Lync Server 2013 management packs</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="1b102-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="1b102-104">

<span> </span></span></span>

<span data-ttu-id="1b102-105">_**Letztes Änderungsdatum des Themas:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="1b102-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="1b102-106">Sie können die Funktionen von System Center Operations Manager erweitern, indem Sie Management Packs installieren – Software, die festlegt, welche Elemente System Center Operations Manager überwachen kann, und wie diese Elemente überwacht werden sollen und wie Benachrichtigungen ausgelöst und gemeldet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="1b102-106">You can extend the capabilities of System Center Operations Manager by installing management packs—software that dictates which items System Center Operations Manager can monitor, and how those items should be monitored and how alerts should be triggered and reported.</span></span> <span data-ttu-id="1b102-107">Lync Server 2013 umfasst zwei System Center Operations Manager-Verwaltungspakete, die die folgenden Funktionen bieten:</span><span class="sxs-lookup"><span data-stu-id="1b102-107">Lync Server 2013 includes two System Center Operations Manager management packs that provide the following capabilities:</span></span>

  - <span data-ttu-id="1b102-108">Das Komponenten-und Benutzer Verwaltungspaket (Microsoft.ls.2013.Monitoring.ComponentAndUser.MP) verfolgt lync-Server Probleme, die in Ereignisprotokollen aufgezeichnet, von Leistungsindikatoren registriert oder in den Anruf Detaildatensätzen (CDR) oder den QoE-Datenbanken (Quality of Experience) protokolliert wurden.</span><span class="sxs-lookup"><span data-stu-id="1b102-108">The Component and User Management Pack (Microsoft.LS.2013.Monitoring.ComponentAndUser.mp) tracks Lync Server issues recorded in event logs, registered by performance counters, or logged in the call detail records (CDR) or the Quality of Experience (QoE) databases.</span></span> <span data-ttu-id="1b102-109">Bei kritischen Problemen kann System Center Operations Manager so konfiguriert werden, dass Administratoren sofort per e-Mail, Sofortnachricht oder SMS-Messaging benachrichtigt werden.</span><span class="sxs-lookup"><span data-stu-id="1b102-109">For critical problems, System Center Operations Manager can be configured to immediately notify administrators via email, instant message, or Short Message Service (SMS) messaging.</span></span> <span data-ttu-id="1b102-110">SMS ist die Technologie, die verwendet wird, um Textnachrichten von einem mobilen Gerät an einen anderen zu senden.)</span><span class="sxs-lookup"><span data-stu-id="1b102-110">SMS is the technology used to send text messages from one mobile device to another.)</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="1b102-111">Details zum Konfigurieren der Operations Manager-Benachrichtigung finden Sie unter Konfigurieren der Benachrichtigung in der TechNet-Bibliothek unter <A href="https://go.microsoft.com/fwlink/p/?linkid=268785">https://go.microsoft.com/fwlink/p/?LinkId=268785</A> .</span><span class="sxs-lookup"><span data-stu-id="1b102-111">For details about configuring Operations Manager notification, see the Configuring Notification in the TechNet Library at <A href="https://go.microsoft.com/fwlink/p/?linkid=268785">https://go.microsoft.com/fwlink/p/?LinkId=268785</A>.</span></span>

    
    </div>

  - <span data-ttu-id="1b102-112">Das Active Monitoring Management Pack (Microsoft.ls.2013.Monitoring.ActiveMonitoring.MP) testet proaktiv wichtige lync Server-Komponenten wie das Anmelden beim System, den Austausch von Sofortnachrichten oder das tätigen von Anrufen an ein Telefon, das sich im öffentlichen Telefonnetz (PSTN) befindet.</span><span class="sxs-lookup"><span data-stu-id="1b102-112">The Active Monitoring Management Pack (Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp) proactively tests key Lync Server components such as signing into to the system, exchanging instant messages, or making calls to a phone located on the public switched telephone network (PSTN).</span></span> <span data-ttu-id="1b102-113">Diese Tests werden mithilfe der Cmdlets für synthetische lync Server-Transaktionen durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="1b102-113">These tests are conducted using the Lync Server synthetic transaction cmdlets.</span></span> <span data-ttu-id="1b102-114">So können Sie beispielsweise das Cmdlet **Test-CsIM** verwenden, um eine Chat Unterhaltung zwischen zwei Testbenutzern zu simulieren.</span><span class="sxs-lookup"><span data-stu-id="1b102-114">For example, you can use the **Test-CsIM** cmdlet to simulate an instant messaging (IM) conversation between a pair of test users.</span></span> <span data-ttu-id="1b102-115">Wenn diese simulierte Nachrichten Unterhaltung fehlschlägt, wird eine Benachrichtigung generiert.</span><span class="sxs-lookup"><span data-stu-id="1b102-115">If this simulated messaging conversation fails an alert is generated.</span></span>

<span data-ttu-id="1b102-116">Sie müssen die Management Packs importieren.</span><span class="sxs-lookup"><span data-stu-id="1b102-116">You need to import the management packs.</span></span> <span data-ttu-id="1b102-117">Wenn Sie die Management Packs nicht importieren, können Sie Operations Manager nicht verwenden, um lync Server-Ereignisse zu überwachen oder synthetische lync Server-Transaktionen auszuführen.</span><span class="sxs-lookup"><span data-stu-id="1b102-117">If you do not import the management packs, you cannot use Operations Manager to monitor Lync Server events or run Lync Server synthetic transactions.</span></span>

<span data-ttu-id="1b102-118">Das Komponenten-und Benutzer Verwaltungspaket wird nur zum Überwachen von lync Server 2013 verwendet.</span><span class="sxs-lookup"><span data-stu-id="1b102-118">The Component and User Management Pack is only used to monitor Lync Server 2013.</span></span> <span data-ttu-id="1b102-119">Wenn Sie sich in einem Koexistenz-Szenario befinden, in dem sowohl lync Server 2013 als auch lync Server 2010 installiert sind, sollten Sie weiterhin die lync Server 2010-Verwaltungspakete für Ihre lync Server 2010-Computer verwenden.</span><span class="sxs-lookup"><span data-stu-id="1b102-119">If you are in a coexistence scenario, where you have both Lync Server 2013 and Lync Server 2010 installed, you should continue to use the Lync Server 2010 management packs for your Lync Server 2010 computers.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="1b102-120">Zu den Management Packs für lync Server 2010 gehören das lync Server 2010-Überwachungs Management Pack und das lync Server 2010-Überwachungs Management Pack für Gruppenchats.</span><span class="sxs-lookup"><span data-stu-id="1b102-120">Management packs for Lync Server 2010 include the Lync Server 2010 Monitoring Management Pack and the Lync Server 2010 Group Chat Monitoring Management Pack.</span></span>



</div>

<span data-ttu-id="1b102-121">Zum Importieren der Management Packs können folgende Tools verwendet werden:</span><span class="sxs-lookup"><span data-stu-id="1b102-121">You can use one of the following tools to import management packs:</span></span>

  - <span data-ttu-id="1b102-122">**System Center Operations Manager**   Mit dieser Methode verwenden Sie den Operations Manager, um die Überwachung für lync Server hinzuzufügen.</span><span class="sxs-lookup"><span data-stu-id="1b102-122">**System Center Operations Manager**   With this method, you use the Operations Manager to add monitoring for Lync Server.</span></span>

  - <span data-ttu-id="1b102-123">**Operations Manager-Shell**   Sie können die Operations Manager-Shell verwenden, um direkt zu importieren oder Probleme zu beheben, die beim Importieren von Management Packs mithilfe der System Center Operations Manager-Konsole auftreten.</span><span class="sxs-lookup"><span data-stu-id="1b102-123">**Operations Manager Shell**   You can use the Operations Manager Shell to import directly or to troubleshoot any issues you encounter when you import management packs by using the System Center Operations Manager console.</span></span>

<div>

## <a name="importing-the-management-packs-by-using-system-center-operations-manager"></a><span data-ttu-id="1b102-124">Importieren der Management Packs mit System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="1b102-124">Importing the Management Packs by Using System Center Operations Manager</span></span>

1.  <span data-ttu-id="1b102-125">Laden Sie die Dateien Microsoft.ls.2013.Monitoring.ActiveMonitoring.MP und Microsoft.ls.2013.Monitoring.ComponentAndUser.MP.</span><span class="sxs-lookup"><span data-stu-id="1b102-125">Download the files Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp and Microsoft.LS.2013.Monitoring.ComponentAndUser.mp.</span></span>

2.  <span data-ttu-id="1b102-126">Klicken Sie in System Center Operations Manager auf **Verwaltung**.</span><span class="sxs-lookup"><span data-stu-id="1b102-126">In System Center Operations Manager, click **Administration**.</span></span>

3.  <span data-ttu-id="1b102-127">Klicken Sie im **Verwaltungs** Bereich mit der rechten Maustaste auf **Management Packs**, und klicken Sie dann auf **Management Packs importieren**.</span><span class="sxs-lookup"><span data-stu-id="1b102-127">In the **Administration** pane, right-click **Management Packs**, and then click **Import Management Packs**.</span></span>

4.  <span data-ttu-id="1b102-128">Klicken Sie im Dialogfeld **Management Packs auswählen** auf **Hinzufügen** und anschließend auf **Von Datenträger hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="1b102-128">In the **Select Management Packs** dialog box, click **Add**, and then click **Add from disk**.</span></span>

5.  <span data-ttu-id="1b102-129">Klicken Sie im Dialogfeld **Online Katalogverbindung** auf **Abbrechen** , um zu verhindern, dass Operations Manager Online geht, um festzustellen, ob für die lync Server-Management Packs Abhängigkeiten vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="1b102-129">In the **Online Catalog Connection** dialog box, click **Cancel** to prevent Operations Manager from going online to see if any dependencies exist for the Lync Server management packs.</span></span> <span data-ttu-id="1b102-130">Wenn Sie System Center Operations Manager 2012 verwenden, klicken Sie auf **Nein**.</span><span class="sxs-lookup"><span data-stu-id="1b102-130">If you are using System Center Operations Manager 2012, click **No**.</span></span>

6.  <span data-ttu-id="1b102-131">Suchen Sie im Dialogfeld **zu importierende Management Packs auswählen nach** den Dateien **Microsoft.ls.2013.Monitoring.ActiveMonitoring.MP** und **Microsoft.ls.2013.Monitoring.ComponentAndUser.MP** , und klicken Sie dann auf **Öffnen**.</span><span class="sxs-lookup"><span data-stu-id="1b102-131">In the **Select Management Packs to import** dialog box, locate and select the files **Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp** and **Microsoft.LS.2013.Monitoring.ComponentAndUser.mp** and then click **Open**.</span></span> <span data-ttu-id="1b102-132">Wenn Sie mehrere Dateien im Dialogfeld auswählen möchten, klicken Sie auf die erste Datei, halten Sie die STRG-Taste gedrückt, und klicken Sie dann auf die zweite Datei.</span><span class="sxs-lookup"><span data-stu-id="1b102-132">To select multiple files in the dialog box, click the first file, hold down the Ctrl key and then click the second file.</span></span>

7.  <span data-ttu-id="1b102-133">Klicken Sie im Dialogfeld **Management Packs auswählen** auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="1b102-133">In the **Select Management Packs** dialog box, click **Install**.</span></span> <span data-ttu-id="1b102-134">Wenn eine Fehlermeldung angezeigt wird und bei der Installation ein Fehler auftritt, bedeutet das normalerweise, dass sich die Management Pack-Dateien in einem Ordner befinden, der durch die Windows-Benutzerkontensteuerung geschützt ist.</span><span class="sxs-lookup"><span data-stu-id="1b102-134">If you get an error message and installation fails, that typically means that the management pack files are in a folder protected by the Windows User Account Control.</span></span> <span data-ttu-id="1b102-135">Wenn dies der Fall ist, kopieren Sie die Dateien in einen anderen Ordner, und starten Sie den Import-und Installationsvorgang erneut.</span><span class="sxs-lookup"><span data-stu-id="1b102-135">If this occurs, copy the files to a different folder and then restart the import and installation process.</span></span>

8.  <span data-ttu-id="1b102-136">Klicken Sie im Dialogfeld **Management Packs auswählen** auf **Schließen**.</span><span class="sxs-lookup"><span data-stu-id="1b102-136">In the **Select Management Packs** dialog box, click **Close**.</span></span> <span data-ttu-id="1b102-137">Beachten Sie, dass für den Import-und Installationsvorgang möglicherweise mehrere Minuten erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="1b102-137">Note that the import and installation process might require several minutes to complete.</span></span>

</div>

<div>

## <a name="importing-management-packs-by-using-the-operations-manager-shell"></a><span data-ttu-id="1b102-138">Importieren von Management Packs mithilfe der Operations Manager-Shell</span><span class="sxs-lookup"><span data-stu-id="1b102-138">Importing Management Packs by Using the Operations Manager Shell</span></span>

<span data-ttu-id="1b102-139">Im Allgemeinen ist es einfacher, die Management Packs mithilfe von Operations Manager zu importieren. Wenn jedoch ein Fehler auftritt und der Import fehlschlägt, bietet die Konsole nicht immer angemessene Fehlerberichte.</span><span class="sxs-lookup"><span data-stu-id="1b102-139">In general it is easier to import the management packs by using the Operations Manager.However, if an error occurs and the import fails, the console does not always provide adequate error reports.</span></span> <span data-ttu-id="1b102-140">Im Vergleich dazu bietet die Operations Manager-Shell detaillierte Informationen.</span><span class="sxs-lookup"><span data-stu-id="1b102-140">By comparison, the Operations Manager Shell, provides detailed information.</span></span> <span data-ttu-id="1b102-141">Wenn Sie Operations Manager verwenden und beim Importieren eines Management Packs Probleme auftreten, importieren Sie das Pack mithilfe der Operations Manager-Shell.</span><span class="sxs-lookup"><span data-stu-id="1b102-141">If you are using Operations Manager and you run into problems importing a management pack, import the pack by using the Operations Manager Shell .</span></span> <span data-ttu-id="1b102-142">Die Operations Manager-Shell bietet weitere Informationen, die Ihnen bei der Entscheidung helfen können, warum der Import fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="1b102-142">The Operations Manager Shell provides more information that might help you determine why the import failed.</span></span>

<span data-ttu-id="1b102-143">Wenn Sie System Center Operations Manager 2007 R2 verwenden, führen Sie die folgenden Schritte aus:</span><span class="sxs-lookup"><span data-stu-id="1b102-143">If you are using System Center Operations Manager 2007 R2, complete the following procedure:</span></span>

1.  <span data-ttu-id="1b102-144">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **System Center Operations Manager 2007 R2**, und klicken Sie dann auf **Operations Manager-Shell**.</span><span class="sxs-lookup"><span data-stu-id="1b102-144">Click **Start**, click **All Programs**, click **System Center Operations Manager 2007 R2**, and then click **Operations Manager Shell**.</span></span>

2.  <span data-ttu-id="1b102-145">Geben Sie in der Operations Manager-Shell an der Eingabeaufforderung den folgenden Befehl unter Verwendung des tatsächlichen Pfads zu Ihrer Kopie der Datei Microsoft.ls.2013.Monitoring.ActiveMonitoring.MP ein, und drücken Sie dann die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="1b102-145">In the Operations Manager Shell, type the following command at the command prompt, using the actual path to your copy of the file Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp, and then press ENTER:</span></span>
    
        MPImport.exe D:\MP\Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp

3.  <span data-ttu-id="1b102-146">Nachdem Sie das erste Management Pack importiert haben, wiederholen Sie den Vorgang mit dem Pfad zu Ihrer Kopie der Datei Microsoft.ls.2013.Monitoring.ComponentAndUser.MP:</span><span class="sxs-lookup"><span data-stu-id="1b102-146">After you import the first management pack, repeat the process using the path to your copy of the file Microsoft.LS.2013.Monitoring.ComponentAndUser.mp:</span></span>
    
        MPImport.exe D:\MP\Microsoft.LS.2013.Monitoring.ComponentAndUser.mp

4.  <span data-ttu-id="1b102-147">Schließen Sie die Operations Manager-Shell.</span><span class="sxs-lookup"><span data-stu-id="1b102-147">Close the Operations Manager Shell.</span></span>

<span data-ttu-id="1b102-148">Wenn Sie System Center Operations Manager 2012 verwenden, führen Sie stattdessen dieses Verfahren aus:</span><span class="sxs-lookup"><span data-stu-id="1b102-148">If you are using System Center Operations Manager 2012, complete this procedure instead:</span></span>

1.  <span data-ttu-id="1b102-149">Klicken Sie auf **Start**, klicken Sie dann auf **Alle Programme**, anschließend auf **Microsoft System Center 2012**, dann auf **Operations Manager** und anschließend auf **Operations Manager-Shell**.</span><span class="sxs-lookup"><span data-stu-id="1b102-149">Click **Start**, click **All Programs**, click **Microsoft System Center 2012**, click **Operations Manager**, and then click **Operations Manager Shell**.</span></span>

2.  <span data-ttu-id="1b102-150">Geben Sie in der Operations Manager-Shell an der Eingabeaufforderung den folgenden Befehl unter Verwendung des tatsächlichen Pfads zu Ihrer Kopie der Datei Microsoft.ls.2013.Monitoring.ActiveMonitoring.MP ein, und drücken Sie dann die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="1b102-150">In the Operations Manager Shell, type the following command at the command prompt, using the actual path to your copy of the file Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp, and then press ENTER:</span></span>
    
        Import-SCOMManagementPack -FullName "D:\MP\ Microsoft.LS.2013.Monitoring.ActiveMonitoring.mp"

3.  <span data-ttu-id="1b102-151">Nachdem Sie das erste Management Pack importiert haben, wiederholen Sie den Vorgang mit dem Pfad zu Ihrer Kopie der Datei Microsoft.ls.2013.Monitoring.ComponentAndUser.MP:</span><span class="sxs-lookup"><span data-stu-id="1b102-151">After you have imported the first management pack, repeat the process using the path to your copy of the file Microsoft.LS.2013.Monitoring.ComponentAndUser.mp:</span></span>
    
        Import-SCOMManagementPack -FullName "D:\MP\ Microsoft.LS.2013.Monitoring.ComponentAndUser.mp"

<span data-ttu-id="1b102-152"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="1b102-152"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

