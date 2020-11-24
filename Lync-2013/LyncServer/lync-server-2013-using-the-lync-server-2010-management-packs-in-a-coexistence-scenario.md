---
title: Verwenden der lync Server 2010-Verwaltungspakete in einem Koexistenz-Szenario
description: Verwenden der lync Server 2010-Verwaltungspakete in einem Koexistenz-Szenario
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Using the Lync Server 2010 management packs in a coexistence scenario
ms:assetid: 8b792503-bd88-47fe-9d97-b071e8d429a5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205078(v=OCS.15)
ms:contentKeyID: 48184772
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f5f6e76f49b74badd0f40d115101abb38aa35172
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395279"
---
# <a name="using-the-lync-server-2010-management-packs-in-a-coexistence-scenario"></a><span data-ttu-id="d5b27-103">Verwenden der lync Server 2010-Verwaltungspakete in einem Koexistenz-Szenario</span><span class="sxs-lookup"><span data-stu-id="d5b27-103">Using the Lync Server 2010 management packs in a coexistence scenario</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d5b27-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d5b27-104">

<span> </span></span></span>

<span data-ttu-id="d5b27-105">_**Letztes Änderungsdatum des Themas:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="d5b27-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="d5b27-106">Viele Kunden nehmen ein Rollout-Programm innerhalb ihrer Unternehmen an, in dem Benutzer schrittweise von Microsoft lync Server 2010 zu lync Server 2013 migriert werden.</span><span class="sxs-lookup"><span data-stu-id="d5b27-106">Many customers adopt a rollout program inside of their enterprises in which users are progressively migrated from Microsoft Lync Server 2010 to Lync Server 2013.</span></span> <span data-ttu-id="d5b27-107">Die Administratoren in diesen Unternehmen kümmern sich um die Überwachung beider lync Server-Versionen, um sicherzustellen, dass alle Endbenutzer die bestmögliche Kommunikationserfahrung erhalten.</span><span class="sxs-lookup"><span data-stu-id="d5b27-107">The administrators at these companies will care about monitoring both versions of Lync Server to help ensure that all of their end users are getting the best possible communication experience.</span></span> <span data-ttu-id="d5b27-108">In diesem Szenario unterstützt das lync Server 2013-Management Pack einen parallelen Migrationspfad mit dem lync Server 2010-Management Pack.</span><span class="sxs-lookup"><span data-stu-id="d5b27-108">For this scenario, the Lync Server 2013 Management Pack supports a side-by-side migration path with the Lync Server 2010 Management Pack.</span></span>

<span data-ttu-id="d5b27-109">In lync Server 2010 wurden lync Server-Computer über das Topologie-Dokument ermittelt, das mit dem zentralen Verwaltungsspeicher gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="d5b27-109">In the Lync Server 2010, Lync Server computers were discovered through the topology document stored with the Central Management store.</span></span> <span data-ttu-id="d5b27-110">In dieser Konfiguration meldet ein einzelner Computer das vorhanden sein aller anderen lync Server-Computer.</span><span class="sxs-lookup"><span data-stu-id="d5b27-110">In this configuration, a single computer would report the existence of all the other Lync Server computers.</span></span>

<span data-ttu-id="d5b27-111">Die Management Packs für lync Server 2013 verwenden jetzt die Ermittlung auf Computerebene anstelle des zentralen Ermittlungsmechanismus, der in lync Server 2010 verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="d5b27-111">The management packs for Lync Server 2013 now use machine-level discovery instead of the central discovery mechanism that was used in Lync Server 2010.</span></span> <span data-ttu-id="d5b27-112">Dies bedeutet, dass sich jeder System Center-Agent im wesentlichen selbst erkennt und seine Existenz an System Center Operations Manager meldet.</span><span class="sxs-lookup"><span data-stu-id="d5b27-112">This means that each System Center agent essentially discovers itself and reports its existence to System Center Operations Manager.</span></span> <span data-ttu-id="d5b27-113">Die Verwendung der Ermittlung auf Computerebene vereinfacht die Verwaltung ihrer System Center-Infrastruktur und ermöglicht auch die unterschiedlichen Versionen der lync Server-Management Packs (beispielsweise Management Packs für lync Server 2010 und Management Packs für lync Server 2013), um einfacher koexistieren zu können.</span><span class="sxs-lookup"><span data-stu-id="d5b27-113">Using machine-level discovery simplifies administration of your System Center infrastructure and also enables different versions of the Lync Server management packs (for example, management packs for Lync Server 2010 and management packs for Lync Server 2013) to coexist more easily.</span></span>

<span data-ttu-id="d5b27-114">Um diese Migration zu unterstützen, müssen Sie zunächst Ihre vorhandene lync Server 2010-Überwachung aktualisieren, um Lücken in der Berichterstattung zu vermeiden.</span><span class="sxs-lookup"><span data-stu-id="d5b27-114">To support this migration, you will first need to upgrade your existing Lync Server 2010 monitoring to avoid gaps in coverage.</span></span> <span data-ttu-id="d5b27-115">Wählen Sie dazu einen vorhandenen lync Server 2010-Computer aus, um das zentrale Ermittlungsskript für den lync Server 2010 zu warten, bevor Sie den zentralen Verwaltungsspeicher auf lync Server 2013 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d5b27-115">To do this, elect an existing Lync Server 2010 computer to service the Central Discovery script for the Lync Server 2010 before upgrading your Central Management store to Lync Server 2013.</span></span> <span data-ttu-id="d5b27-116">Hierbei handelt es sich um einen vierstufigen Prozess:</span><span class="sxs-lookup"><span data-stu-id="d5b27-116">This is a four-step process:</span></span>

1.  <span data-ttu-id="d5b27-117">Aktualisieren Sie die lync Server 2010-Verwaltungspakete auf Kumulatives Update 7.</span><span class="sxs-lookup"><span data-stu-id="d5b27-117">Upgrade the Lync Server 2010 Management Packs to Cumulative Update 7.</span></span>

2.  <span data-ttu-id="d5b27-118">Weisen Sie einen lync Server 2010-Computer an, das zentrale Ermittlungsskript auszuführen.</span><span class="sxs-lookup"><span data-stu-id="d5b27-118">Instruct a Lync Server 2010 computer to run the Central Discovery script.</span></span>

3.  <span data-ttu-id="d5b27-119">Überschreiben Sie den zentralen Ermittlungs Kandidaten im Microsoft lync Server 2010-Management Pack.</span><span class="sxs-lookup"><span data-stu-id="d5b27-119">Override the Central Discovery Candidate in the Microsoft Lync Server 2010 Management Pack.</span></span>

4.  <span data-ttu-id="d5b27-120">Überprüfen Sie, ob der neue Central Discovery-Kandidat gefunden wurde.</span><span class="sxs-lookup"><span data-stu-id="d5b27-120">Verify that the new Central Discovery Candidate has been discovered.</span></span>

<div>

## <a name="instructing-a-lync-server-2010-computer-to-run-the-central-discovery-script"></a><span data-ttu-id="d5b27-121">Anweisen eines lync Server 2010-Computers zum Ausführen des zentralen Ermittlungsskripts</span><span class="sxs-lookup"><span data-stu-id="d5b27-121">Instructing a Lync Server 2010 Computer to Run the Central Discovery script</span></span>

<span data-ttu-id="d5b27-122">Wenn Sie einen nicht zentralen Verwaltungsspeicher Computer benennen möchten (beispielsweise einen lync Server-Front-End-Server), der die zentrale Ermittlung behandeln soll, müssen Sie den folgenden Registrierungsschlüssel auf dem nicht zentralen Verwaltungsspeicher Server erstellen:</span><span class="sxs-lookup"><span data-stu-id="d5b27-122">To nominate a non-Central Management store computer (for example, a Lync Server Front End) server to handle central discovery, you will need to create the following registry key on the non-Central Management store server:</span></span>

<span data-ttu-id="d5b27-123">HKLM \\ Software \\ Microsoft \\ Real-Time Communications \\ Health \\ CentralDiscoveryCandidate</span><span class="sxs-lookup"><span data-stu-id="d5b27-123">HKLM\\Software\\Microsoft\\Real-Time Communications\\Health\\CentralDiscoveryCandidate</span></span>

<span data-ttu-id="d5b27-124">Sie können diesen Registrierungsschlüssel erstellen, indem Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="d5b27-124">You can create this registry key by completing the following procedure:</span></span>

1.  <span data-ttu-id="d5b27-125">Klicken Sie auf **Start** und dann auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="d5b27-125">Click **Start** and then click **Run**.</span></span>

2.  <span data-ttu-id="d5b27-126">Geben Sie im Dialogfeld **Ausführen** den **Befehl regedit** ein, und drücken Sie dann die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="d5b27-126">In the **Run** dialog box, type **regedit** and then press ENTER.</span></span>

3.  <span data-ttu-id="d5b27-127">Erweitern Sie im Registrierungs- **Editor \_ HKEY lokaler \_ Computer**, erweitern Sie **Software**, erweitern Sie **Microsoft**, und erweitern Sie dann die **Echtzeitkommunikation**.</span><span class="sxs-lookup"><span data-stu-id="d5b27-127">In Registry Editor, expand **HKEY\_LOCAL\_MACHINE**, expand **SOFTWARE**, expand **Microsoft**, and then expand **Real-Time Communications**.</span></span>

4.  <span data-ttu-id="d5b27-128">Klicken Sie mit der rechten Maustaste auf **Status**, klicken Sie auf **neu**, und klicken Sie dann auf **Taste**.</span><span class="sxs-lookup"><span data-stu-id="d5b27-128">Right-click **Health**, click **New**, and then click **Key**.</span></span> <span data-ttu-id="d5b27-129">Wenn der **Integritäts** Schlüssel nicht vorhanden ist, klicken Sie mit der rechten Maustaste auf **Echtzeitkommunikation**, zeigen Sie auf **neu**, und klicken Sie dann auf **Taste**.</span><span class="sxs-lookup"><span data-stu-id="d5b27-129">If the **Health** key does not exist, then right-click **Real-Time Communications**, point to **New**, and then click **Key**.</span></span> <span data-ttu-id="d5b27-130">Wenn Sie den neuen Schlüssel erstellen, geben Sie Gesundheit ein, und drücken Sie dann die EINGABETASTE.</span><span class="sxs-lookup"><span data-stu-id="d5b27-130">When the new key is created, type Health, and then press ENTER.</span></span>
    
    <span data-ttu-id="d5b27-131">Nachdem der neue Schlüssel erstellt wurde, geben Sie **CentralDiscoveryCandidate** ein, und drücken Sie dann die EINGABETASTE, um den Schlüssel umzubenennen.</span><span class="sxs-lookup"><span data-stu-id="d5b27-131">After the new key has been created, type **CentralDiscoveryCandidate** and then press ENTER to rename the key.</span></span>

<span data-ttu-id="d5b27-132">Es kann den Computer mehrere Stunden dauern, bis diese Änderung abgeholt wird.</span><span class="sxs-lookup"><span data-stu-id="d5b27-132">It may take the computer several hours to pick up this change.</span></span> <span data-ttu-id="d5b27-133">Damit die Änderung sofort wirksam wird, beenden Sie den Integritäts-Agent-Dienst, und starten Sie ihn dann erneut.</span><span class="sxs-lookup"><span data-stu-id="d5b27-133">To make the change take effect immediately, stop and then restart the Health Agent service.</span></span> <span data-ttu-id="d5b27-134">Führen Sie die folgenden Schritte auf dem lync Server 2010-Computer aus, um den Integritäts-Agent-Dienst erneut zu starten:</span><span class="sxs-lookup"><span data-stu-id="d5b27-134">To restart the Health Agent service, complete the following procedure on the Lync Server 2010 computer:</span></span>

1.  <span data-ttu-id="d5b27-135">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Zubehör**, klicken Sie mit der rechten Maustaste auf **Eingabeaufforderung**, und klicken Sie dann auf **als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="d5b27-135">Click **Start**, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

2.  <span data-ttu-id="d5b27-136">Geben Sie im Konsolenfenster den folgenden Befehl ein, und drücken Sie dann die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="d5b27-136">In the console window, type the following command and then press ENTER:</span></span>
    
        Net stop HealthService

3.  <span data-ttu-id="d5b27-137">Es wird eine Meldung angezeigt, die besagt, dass "der System Center-Verwaltungsdienst beendet wird", gefolgt von einer zweiten Meldung, die besagt, dass der Dienst angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="d5b27-137">You will see a message that states "The System Center Management service is stopping," followed by a second message that tells you that the service has been stopped.</span></span> <span data-ttu-id="d5b27-138">Nachdem der Dienst beendet wurde, können Sie ihn erneut starten, indem Sie den folgenden Befehl eingeben und die EINGABETASTE drücken:</span><span class="sxs-lookup"><span data-stu-id="d5b27-138">After the service has stopped, you can restart it by typing the following command and pressing ENTER:</span></span>
    
        Net start HealthService

</div>

<div>

## <a name="overriding-the-central-discovery-candidate-in-the-lync-server-2010-management-pack"></a><span data-ttu-id="d5b27-139">Überschreiben des zentralen Ermittlungs Kandidaten im lync Server 2010-Management Pack</span><span class="sxs-lookup"><span data-stu-id="d5b27-139">Overriding the Central Discovery Candidate in the Lync Server 2010 Management Pack</span></span>

<span data-ttu-id="d5b27-140">Nachdem Sie einen lync Server 2010-Computer angewiesen haben, auf lync Server 2010-Computern zu berichten, müssen Sie das lync Server 2010-Management Pack auch über diese Änderung informieren.</span><span class="sxs-lookup"><span data-stu-id="d5b27-140">After instructing a Lync Server 2010 computer to report on Lync Server 2010 computers, you will need to inform the Lync Server 2010 Management Pack about this change as well.</span></span> <span data-ttu-id="d5b27-141">Dazu müssen Sie im Management Pack eine Außerkraftsetzung erstellen.</span><span class="sxs-lookup"><span data-stu-id="d5b27-141">To do this, you will need to create an override in the Management Pack.</span></span> <span data-ttu-id="d5b27-142">Dazu können Sie die folgenden Schritte ausführen:</span><span class="sxs-lookup"><span data-stu-id="d5b27-142">That can be done by completing the following procedure:</span></span>

1.  <span data-ttu-id="d5b27-143">Klicken Sie in der Operations Manager-Konsole auf **Dokumenterstellung**.</span><span class="sxs-lookup"><span data-stu-id="d5b27-143">In the Operations Manager console, click **Authoring**.</span></span>

2.  <span data-ttu-id="d5b27-144">Erweitern Sie auf der Registerkarte Dokumenterstellung den Knoten **Management Pack-Objekte**, klicken Sie auf **Objektermittlungen**, und klicken Sie dann auf **Bereich**.</span><span class="sxs-lookup"><span data-stu-id="d5b27-144">On the Authoring tab, expand **Management Pack Objects**, click **Object Discoveries**, and then click **Scope**.</span></span>

3.  <span data-ttu-id="d5b27-145">Wählen Sie im Dialogfeld **Scope Management Pack-Objekte** das Element mit dem Ziel **ls Discovery Candidate** aus, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d5b27-145">In the **Scope Management Pack Objects** dialog box, select the item with the Target **LS Discovery Candidate** and then click **OK**.</span></span> <span data-ttu-id="d5b27-146">Beachten Sie, dass der ls-Ermittlungs Kandidat nur angezeigt wird, wenn Sie das lync Server 2010-Management Pack installiert haben.</span><span class="sxs-lookup"><span data-stu-id="d5b27-146">Note that LS Discovery Candidate will appear only if you have installed the Lync Server 2010 Management Pack.</span></span>

4.  <span data-ttu-id="d5b27-147">Klicken Sie in der Operations Manager-Konsole mit der rechten Maustaste auf **ls Discovery Candidate**, zeigen Sie auf **Außerkraftsetzungen**, zeigen Sie auf **Objektermittlung außer Kraft setzen**, und klicken Sie dann auf **für alle Objekte der Klasse: ls Discovery Candidate**.</span><span class="sxs-lookup"><span data-stu-id="d5b27-147">In the Operations Manager console, right-click **LS Discovery Candidate**, point to **Overrides**, point to **Override the Object Discovery**, and then click **For all objects of class: LS Discovery Candidate**.</span></span>

5.  <span data-ttu-id="d5b27-148">Aktivieren Sie im Dialogfeld **Eigenschaften außer Kraft setzen** das Kontrollkästchen **außer Kraft setzen** neben dem FQDN des Parameters **Central Discovery WatcherNode**.</span><span class="sxs-lookup"><span data-stu-id="d5b27-148">In the **Override Properties** dialog box, select the **Override** check box next to the parameter **Central Discovery WatcherNode Fqdn**.</span></span> <span data-ttu-id="d5b27-149">Geben Sie den vollqualifizierten Domänennamen des lync Server 2010-Computers in die Felder **Außerkraftsetzungswert** und **effektiver Wert** ein.</span><span class="sxs-lookup"><span data-stu-id="d5b27-149">Type the fully qualified domain name of the Lync Server 2010 computer in the **Override Value** and **Effective Value** boxes.</span></span> <span data-ttu-id="d5b27-150">Aktivieren Sie das Kontrollkästchen **erzwungen** , und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d5b27-150">Select the **Enforced** check box and click **OK**.</span></span>

<span data-ttu-id="d5b27-151">Nachdem Sie die Außerkraftsetzung erstellt haben, müssen Sie den Integritätsdienst auf dem Stamm Verwaltungs Server erneut starten.</span><span class="sxs-lookup"><span data-stu-id="d5b27-151">After you have created the override, you need to restart the health service on the Root Management Server.</span></span> <span data-ttu-id="d5b27-152">Führen Sie den folgenden Vorgang auf dem Stamm Verwaltungs Server aus, um den Integritätsdienst erneut zu starten:</span><span class="sxs-lookup"><span data-stu-id="d5b27-152">To restart the health service, complete the following procedure on the Root Management Server:</span></span>

1.  <span data-ttu-id="d5b27-153">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Zubehör**, klicken Sie mit der rechten Maustaste auf **Eingabeaufforderung**, und klicken Sie dann auf **als Administrator ausführen**.</span><span class="sxs-lookup"><span data-stu-id="d5b27-153">Click **Start**, click **All Programs**, click **Accessories**, right-click **Command Prompt**, and then click **Run as administrator**.</span></span>

2.  <span data-ttu-id="d5b27-154">Geben Sie im Konsolenfenster den folgenden Befehl ein, und drücken Sie dann die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="d5b27-154">In the console window, type the following command, and then press ENTER:</span></span>
    
        Net stop HealthService

3.  <span data-ttu-id="d5b27-155">Es wird eine Meldung angezeigt, die besagt, dass "der System Center-Verwaltungsdienst beendet wird", gefolgt von einer zweiten Meldung, die besagt, dass der Dienst angehalten wurde.</span><span class="sxs-lookup"><span data-stu-id="d5b27-155">You will see a message stating that "The System Center Management service is stopping," followed by a second message that tells you that the service has been stopped.</span></span> <span data-ttu-id="d5b27-156">Nachdem der Dienst beendet wurde, können Sie ihn erneut starten, indem Sie den folgenden Befehl eingeben und die EINGABETASTE drücken:</span><span class="sxs-lookup"><span data-stu-id="d5b27-156">After the service has stopped, you can then restart it by typing the following command and pressing ENTER:</span></span>
    
        Net start HealthService

</div>

<div>

## <a name="verifying-that-the-new-central-discovery-candidate-was-discovered"></a><span data-ttu-id="d5b27-157">Überprüfen, ob der neue zentrale Discovery Candidate erkannt wurde</span><span class="sxs-lookup"><span data-stu-id="d5b27-157">Verifying that the New Central Discovery Candidate Was Discovered</span></span>

<span data-ttu-id="d5b27-158">Der letzte Schritt vor dem Upgrade des zentralen Verwaltungsspeichers besteht darin, sicherzustellen, dass der neue zentrale Discovery-Kandidat vom lync Server 2010-Management Pack erkannt wurde.</span><span class="sxs-lookup"><span data-stu-id="d5b27-158">The final step before upgrading Central Management store is to make sure that the new central discovery candidate was discovered by the Lync Server 2010 Management Pack.</span></span> <span data-ttu-id="d5b27-159">Öffnen Sie dazu die Operations Manager-Konsole, und klicken Sie dann auf Überwachung.</span><span class="sxs-lookup"><span data-stu-id="d5b27-159">To do this, open the Operations Manager console and then click Monitoring.</span></span> <span data-ttu-id="d5b27-160">Erweitern Sie auf der Registerkarte Überwachung den **Status Microsoft lync Server 2010**, erweitern Sie **Topologie Discovery**, und klicken Sie dann auf **Ermittlungsstatus Ansicht**.</span><span class="sxs-lookup"><span data-stu-id="d5b27-160">On the Monitoring tab, expand **Microsoft Lync Server 2010 Health**, expand **Topology Discovery**, and then click **Discovery State View**.</span></span> <span data-ttu-id="d5b27-161">Überprüfen Sie, ob eine Zeile in der Anzeige einen **Pfad** enthält, in dem der vollqualifizierte Domänenname des zentralen Ermittlungs Kandidaten aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="d5b27-161">Verify that a row in the display has a **Path** that lists the fully qualified domain name of the central discovery candidate.</span></span> <span data-ttu-id="d5b27-162">Sie sollten auch sicherstellen, dass der Computerzustand als **Fehler** freigemeldet wird.</span><span class="sxs-lookup"><span data-stu-id="d5b27-162">You should also verify that the computer state is reported as **Healthy**.</span></span>

<span data-ttu-id="d5b27-163"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d5b27-163"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

