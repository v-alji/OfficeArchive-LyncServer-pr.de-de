---
title: 'Lync Server 2013: Ausführen der Gesamtstrukturvorbereitung'
description: 'Lync Server 2013: Ausführen der Gesamtstrukturvorbereitung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running forest preparation
ms:assetid: 9d62f7be-bcfe-421d-8d8a-225567102a35
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412732(v=OCS.15)
ms:contentKeyID: 48184991
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ad3ef2d7583d541701d6606946ca1df1bbd8cf23
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442215"
---
# <a name="running-forest-preparation-for-lync-server-2013"></a><span data-ttu-id="9f324-103">Ausführen der Gesamtstrukturvorbereitung für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f324-103">Running forest preparation for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9f324-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9f324-104">

<span> </span></span></span>

<span data-ttu-id="9f324-105">_**Letztes Änderungsdatum des Themas:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="9f324-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="9f324-106">Sie können mit den Setup-oder lync Server-Verwaltungsshell-Cmdlets die Gesamtstruktur vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="9f324-106">You can use Setup or Lync Server Management Shell cmdlets to prepare the forest.</span></span> <span data-ttu-id="9f324-107">Das Cmdlet, das die Gesamtstruktur vorbereitet, ist **enable-CsAdForest**.</span><span class="sxs-lookup"><span data-stu-id="9f324-107">The cmdlet that prepares the forest is **Enable-CsAdForest**.</span></span>

<span data-ttu-id="9f324-108">Nachdem Sie die Gesamtstruktur vorbereitet haben, müssen Sie überprüfen, ob die globalen Einstellungen repliziert wurden, bevor Sie die Domänenvorbereitung ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f324-108">After you prepare the forest, you must verify that global settings have been replicated before running domain preparation.</span></span>

<div>

## <a name="to-use-setup-to-prepare-the-forest"></a><span data-ttu-id="9f324-109">So verwenden Sie Setup zum Vorbereiten der Gesamtstruktur</span><span class="sxs-lookup"><span data-stu-id="9f324-109">To use Setup to prepare the forest</span></span>

1.  <span data-ttu-id="9f324-110">Melden Sie sich bei einem Computer an, der einer Domäne als Mitglied der Gruppe "Organisations-Admins" für die Stammdomäne der Gesamtstruktur beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="9f324-110">Log on to a computer that is joined to a domain as a member of the Enterprise Admins group for the forest root domain.</span></span>

2.  <span data-ttu-id="9f324-111">Führen Sie im lync Server 2013-Installationsordner oder-Medium Setup.exe aus, um den Bereitstellungs-Assistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="9f324-111">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Deployment Wizard.</span></span>

3.  <span data-ttu-id="9f324-112">Klicken Sie auf **Active Directory vorbereiten** und warten Sie das Bestimmen des Bereitstellungsstatus ab.</span><span class="sxs-lookup"><span data-stu-id="9f324-112">Click **Prepare Active Directory**, and then wait for the deployment state to be determined.</span></span>

4.  <span data-ttu-id="9f324-113">Klicken Sie in **Schritt 3: aktuelle Gesamtstruktur vorbereiten** auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="9f324-113">At **Step 3: Prepare Current Forest**, click **Run**.</span></span>

5.  <span data-ttu-id="9f324-114">Klicken Sie auf der Seite **Forest vorbereiten** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="9f324-114">On the **Prepare Forest** page, click **Next**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9f324-115">Mit der Gesamtstrukturvorbereitung können Sie auswählen, wo die universellen Gruppen für lync Server 2013 platziert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="9f324-115">Forest Preparation allows you to choose where to place the Universal Groups for Lync Server 2013.</span></span> <span data-ttu-id="9f324-116">Wählen Sie einen Speicherort entsprechend den Anforderungen Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="9f324-116">Choose a location that is consistent with the requirements of your organization.</span></span>

    
    </div>

6.  <span data-ttu-id="9f324-117">Suchen Sie auf der Seite **Befehle ausführen** nach **Aufgabenstatus: Abgeschlossen** und klicken Sie dann auf **Protokoll anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="9f324-117">On the **Executing Commands** page, look for **Task status: Completed**, and then click **View Log**.</span></span>

7.  <span data-ttu-id="9f324-118">Erweitern Sie in der Spalte **Aktion** den Knoten **Gesamtstruktur prep**, suchen Sie **\<Success\>** am Ende jeder Aufgabe nach einem Ausführungsergebnis, um zu überprüfen, ob die Gesamtstrukturvorbereitung erfolgreich abgeschlossen wurde, schließen Sie das Protokoll, und klicken Sie dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="9f324-118">Under the **Action** column, expand **Forest Prep**, look for a **\<Success\>** Execution Result at the end of each task to verify that forest preparation completed successfully, close the log, and then click **Finish**.</span></span>

8.  <span data-ttu-id="9f324-119">Warten Sie, bis die Active Directory-Replikation abgeschlossen ist, oder erzwingen Sie die Replikation auf alle Domänencontroller, die im Snap-in **Active Directory-Standorte und-Dienste** für den Gesamtstruktur-Stammdomänencontroller aufgelistet sind, bevor Sie die Domänenvorbereitung ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f324-119">Wait for Active Directory replication to complete, or force replication to all domain controllers listed in the **Active Directory Sites and Services** snap-in for the forest root domain controller, before running domain preparation.</span></span> <span data-ttu-id="9f324-120">Erzwingen Sie die Replikation zwischen den Domänencontrollern an allen Active Directory-Standorten, damit die Replikation innerhalb der Websites innerhalb weniger Minuten erfolgen kann.</span><span class="sxs-lookup"><span data-stu-id="9f324-120">Force replication between the domain controllers in all Active Directory sites to cause replication within the sites to occur within minutes.</span></span>

</div>

<div>

## <a name="to-use-cmdlets-to-prepare-the-forest"></a><span data-ttu-id="9f324-121">So verwenden Sie Cmdlets zum Vorbereiten der Gesamtstruktur</span><span class="sxs-lookup"><span data-stu-id="9f324-121">To use cmdlets to prepare the forest</span></span>

1.  <span data-ttu-id="9f324-122">Melden Sie sich bei einem Computer an, der einer Domäne als Mitglied der Gruppe der Domänenadministratoren in der Stammdomäne der Gesamtstruktur beigetreten ist.</span><span class="sxs-lookup"><span data-stu-id="9f324-122">Log on to a computer that is joined to a domain as a member of the Domain Admins group in the forest root domain.</span></span>

2.  <span data-ttu-id="9f324-123">Installieren Sie die lync Server Core-Komponenten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="9f324-123">Install Lync Server Core components as follows:</span></span>
    
    1.  <span data-ttu-id="9f324-124">Führen Sie im lync Server 2013-Installationsordner oder-Medium Setup.exe aus, um den lync Server-Bereitstellungs-Assistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="9f324-124">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Lync Server Deployment Wizard.</span></span>
    
    2.  <span data-ttu-id="9f324-125">Wenn Sie aufgefordert werden, die Microsoft Visual C++-Installation zu installieren, klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="9f324-125">If you are prompted to install the Microsoft Visual C++ Redistributable, click **Yes**.</span></span>
    
    3.  <span data-ttu-id="9f324-126">Im Dialogfeld "lync Server 2013-Setup" werden Sie aufgefordert, einen Speicherort zum Installieren der lync Server-Dateien anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="9f324-126">The Lync Server 2013 Setup dialog box prompts you for a location to install the Lync Server files.</span></span> <span data-ttu-id="9f324-127">Wählen Sie den Standardspeicherort aus, oder **Navigieren** Sie zu einem Speicherort Ihrer Wahl, und klicken Sie dann auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="9f324-127">Choose the default location or **Browse** to a location of your choice, and then click **Install**.</span></span>
    
    4.  <span data-ttu-id="9f324-128">Aktivieren Sie auf der Seite Lizenzvertrag **die Kontrollkästchen Ich akzeptiere die Bedingungen des Lizenzvertrags**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="9f324-128">On the License Agreement page, check **I accept the terms in the license agreement**, and then click **OK**.</span></span> <span data-ttu-id="9f324-129">Das Installationsprogramm installiert die lync Server 2013-Core-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="9f324-129">The installer installs the Lync Server 2013 Core Components.</span></span>

3.  <span data-ttu-id="9f324-130">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="9f324-130">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="9f324-131">Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="9f324-131">Run:</span></span>
    
        Enable-CsAdForest [-GroupDomain <FQDN of the domain in which to create the universal groups>]
    
    <span data-ttu-id="9f324-132">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="9f324-132">For example:</span></span>
    
        Enable-CsAdForest -GroupDomain domain1.contoso.com 
    
    <span data-ttu-id="9f324-133">Wenn Sie den GroupDomain-Parameter nicht angeben, ist der Standardwert die lokale Domäne.</span><span class="sxs-lookup"><span data-stu-id="9f324-133">If you do not specify the GroupDomain parameter, the default value is the local domain.</span></span> <span data-ttu-id="9f324-134">Wenn universelle Gruppen zuvor in einer Domäne erstellt wurden, die nicht die Standarddomäne ist, müssen Sie den GroupDomain-Parameter explizit angeben.</span><span class="sxs-lookup"><span data-stu-id="9f324-134">If universal groups were created previously in a domain that is not the default domain, you must specify the GroupDomain parameter explicitly.</span></span>

5.  <span data-ttu-id="9f324-135">Warten Sie, bis die Active Directory-Replikation abgeschlossen ist, oder erzwingen Sie die Replikation auf alle Domänencontroller, die im Snap-in **Active Directory-Standorte und-Dienste** für den Gesamtstruktur-Stammdomänencontroller aufgelistet sind, bevor Sie die Domänenvorbereitung ausführen.</span><span class="sxs-lookup"><span data-stu-id="9f324-135">Wait for Active Directory replication to complete, or force replication to all domain controllers listed in the **Active Directory Sites and Services** snap-in for the forest root domain controller, before running domain preparation.</span></span>

6.  <span data-ttu-id="9f324-136">Überprüfen Sie, ob die Gesamtstrukturvorbereitung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="9f324-136">Verify that forest preparation was successful.</span></span> <span data-ttu-id="9f324-137">Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="9f324-137">Run:</span></span>
    
        Get-CsAdForest 
    
    <span data-ttu-id="9f324-138">Dieses Cmdlet gibt den Wert des **LC- \_ FORESTSETTINGS- \_ Zustands \_ bereit** zurück, wenn die Gesamtstrukturvorbereitung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="9f324-138">This cmdlet returns a value of **LC\_FORESTSETTINGS\_STATE\_READY** if forest preparation was successful.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="9f324-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9f324-139">See Also</span></span>


[<span data-ttu-id="9f324-140">Verwenden von Cmdlets zum Rückgängigmachen der Gesamtstrukturvorbereitung für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f324-140">Using cmdlets to reverse forest preparation for Lync Server 2013</span></span>](lync-server-2013-using-cmdlets-to-reverse-forest-preparation.md)  


[<span data-ttu-id="9f324-141">Vorbereiten der Gesamtstruktur für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9f324-141">Preparing the forest for Lync Server 2013</span></span>](lync-server-2013-preparing-the-forest.md)  
  

<span data-ttu-id="9f324-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9f324-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

