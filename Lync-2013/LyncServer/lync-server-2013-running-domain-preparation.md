---
title: 'Lync Server 2013: Ausführen der Domänenvorbereitung'
description: 'Lync Server 2013: Ausführen der Domänenvorbereitung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running domain preparation
ms:assetid: 95dab800-1f2c-4506-b36c-99986643b149
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398761(v=OCS.15)
ms:contentKeyID: 48184847
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2f2c4ebe94d07ed2d1fd9be013cd8e88204312f8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442257"
---
# <a name="running-domain-preparation-for-lync-server-2013"></a><span data-ttu-id="dbbb1-103">Ausführen der Domänenvorbereitung für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dbbb1-103">Running domain preparation for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="dbbb1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="dbbb1-104">

<span> </span></span></span>

<span data-ttu-id="dbbb1-105">_**Letztes Änderungsdatum des Themas:** 2013-04-16_</span><span class="sxs-lookup"><span data-stu-id="dbbb1-105">_**Topic Last Modified:** 2013-04-16_</span></span>

<span data-ttu-id="dbbb1-106">Sie können die Setup-oder lync Server-Verwaltungsshell-Cmdlets verwenden, um Domänen vorzubereiten.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-106">You can use Setup or Lync Server Management Shell cmdlets to prepare domains.</span></span> <span data-ttu-id="dbbb1-107">Das Cmdlet, das eine Domäne vorbereitet, ist **enable-CsAdDomain**.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-107">The cmdlet that prepares a domain is **Enable-CsAdDomain**.</span></span>

<span data-ttu-id="dbbb1-108">Die Domänenvorbereitung ist der letzte Schritt beim Vorbereiten der Active Directory-Domänendienste für lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-108">Domain preparation is the final step in preparing Active Directory Domain Services for Lync Server 2013.</span></span>

<div>

## <a name="to-use-setup-to-prepare-domains"></a><span data-ttu-id="dbbb1-109">So verwenden Sie das Setup zum Vorbereiten von Domänen</span><span class="sxs-lookup"><span data-stu-id="dbbb1-109">To use Setup to prepare domains</span></span>

1.  <span data-ttu-id="dbbb1-110">Melden Sie sich bei einem beliebigen Server in der Domäne als Mitglied der Gruppe der Domänenadministratoren an.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-110">Log on to any server in the domain as a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="dbbb1-111">Führen Sie im lync Server 2013-Installationsordner oder-Medium Setup.exe aus, um den lync Server-Bereitstellungs-Assistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-111">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Lync Server Deployment Wizard.</span></span>

3.  <span data-ttu-id="dbbb1-112">Klicken Sie auf **Active Directory vorbereiten** und warten Sie das Bestimmen des Bereitstellungsstatus ab.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-112">Click **Prepare Active Directory**, and then wait for the deployment state to be determined.</span></span>

4.  <span data-ttu-id="dbbb1-113">Klicken Sie unter **Schritt 5: Aktuelle Domäne vorbereiten** auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-113">At **Step 5: Prepare Current Domain**, click **Run**.</span></span>

5.  <span data-ttu-id="dbbb1-114">Klicken Sie auf der Seite **Domäne vorbereiten** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-114">On the **Prepare Domain** page, click **Next**.</span></span>

6.  <span data-ttu-id="dbbb1-115">Suchen Sie auf der Seite **Befehle ausführen** nach **Aufgabenstatus: Abgeschlossen** und klicken Sie dann auf **Protokoll anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-115">On the **Executing Commands** page, look for **Task status: Completed**, and then click **View Log**.</span></span>

7.  <span data-ttu-id="dbbb1-116">Erweitern Sie in der Spalte " **Aktion** " die **Domäne prep**, suchen Sie nach einem **\<Success\>** Ausführungsergebnis am Ende jeder Aufgabe, um zu überprüfen, ob die Domänenvorbereitung erfolgreich abgeschlossen wurde, schließen Sie das Protokoll, und klicken Sie dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-116">Under the **Action** column, expand **Domain Prep**, look for a **\<Success\>** Execution Result at the end of each task to verify that domain preparation completed successfully, close the log, and then click **Finish**.</span></span>

8.  <span data-ttu-id="dbbb1-117">Warten Sie, bis die Active Directory-Replikation abgeschlossen ist, oder erzwingen Sie die Replikation auf alle Domänencontroller, die im Snap-in Active Directory-Standorte und-Dienste für den Gesamtstruktur-Stammdomänencontroller aufgeführt sind.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-117">Wait for Active Directory replication to complete or force replication to all the domain controllers listed in the Active Directory Sites and Services snap-in for the forest root domain controller.</span></span>

</div>

<div>

## <a name="to-use-cmdlets-to-prepare-the-domain"></a><span data-ttu-id="dbbb1-118">So verwenden Sie Cmdlets zum Vorbereiten der Domäne</span><span class="sxs-lookup"><span data-stu-id="dbbb1-118">To use cmdlets to prepare the domain</span></span>

1.  <span data-ttu-id="dbbb1-119">Melden Sie sich bei einem beliebigen Server in der Domäne als Mitglied der Gruppe der Domänenadministratoren an.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-119">Log on to any server in the domain as a member of the Domain Admins group.</span></span>

2.  <span data-ttu-id="dbbb1-120">Installieren Sie die lync Server Core-Komponenten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="dbbb1-120">Install Lync Server Core components as follows:</span></span>
    
    1.  <span data-ttu-id="dbbb1-121">Führen Sie im lync Server 2013-Installationsordner oder-Medium Setup.exe aus, um den lync Server-Bereitstellungs-Assistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-121">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Lync Server Deployment Wizard.</span></span>
    
    2.  <span data-ttu-id="dbbb1-122">Wenn Sie aufgefordert werden, die Microsoft Visual C++-Installation zu installieren, klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-122">If you are prompted to install the Microsoft Visual C++ Redistributable, click **Yes**.</span></span>
    
    3.  <span data-ttu-id="dbbb1-123">Im Dialogfeld "lync Server 2013-Setup" werden Sie aufgefordert, einen Speicherort zum Installieren der lync Server-Dateien anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-123">The Lync Server 2013 Setup dialog box prompts you for a location to install the Lync Server files.</span></span> <span data-ttu-id="dbbb1-124">Wählen Sie den Standardspeicherort aus, oder **Navigieren** Sie zu einem Speicherort Ihrer Wahl, und klicken Sie dann auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-124">Choose the default location or **Browse** to a location of your choice, and then click **Install**.</span></span>
    
    4.  <span data-ttu-id="dbbb1-125">Aktivieren Sie auf der Seite Lizenzvertrag **die Kontrollkästchen Ich akzeptiere die Bedingungen des Lizenzvertrags**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-125">On the License Agreement page, check **I accept the terms in the license agreement**, and then click **OK**.</span></span> <span data-ttu-id="dbbb1-126">Das Installationsprogramm installiert die lync Server 2013-Core-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-126">The installer installs the Lync Server 2013 Core Components.</span></span>

3.  <span data-ttu-id="dbbb1-127">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-127">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="dbbb1-128">Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="dbbb1-128">Run:</span></span>
    
        Enable-CsAdDomain [-Domain <DomainFQDN>] 
    
    <span data-ttu-id="dbbb1-129">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="dbbb1-129">For example:</span></span>
    
        Enable-CsAdDomain -Domain domain1.contoso.net 
    
    <span data-ttu-id="dbbb1-130">Wenn Sie den Parameter Domain nicht angeben, ist der Standardwert die lokale Domäne.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-130">If you do not specify the Domain parameter, the default is the local domain.</span></span>

5.  <span data-ttu-id="dbbb1-131">Überprüfen Sie, ob die Domänenvorbereitung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-131">Verify that domain preparation was successful.</span></span> <span data-ttu-id="dbbb1-132">Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="dbbb1-132">Run:</span></span>
    
        Get-CsAdDomain [-Domain <Domain FQDN>] [-DomainController <Domain controller FQDN>] [-GlobalCatalog <Global catalog server FQDN>] [-GlobalSettingsDomainController <Domain controller FQDN where global settings are stored>] 
    
    <span data-ttu-id="dbbb1-133">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="dbbb1-133">For example:</span></span>
    
        Get-CsAdDomain -Domain domain1.contoso.net -GlobalSettingsDomainController dc01.domain1.contoso.com
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="dbbb1-134">Mit dem Parameter GlobalSettingsDomainController können Sie angeben, wo die globalen Einstellungen gespeichert werden.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-134">The parameter GlobalSettingsDomainController allows you to indicate where global settings are stored.</span></span> <span data-ttu-id="dbbb1-135">Wenn Ihre Einstellungen im System Container gespeichert sind (typisch für Upgrade-Bereitstellungen, bei denen die globalen Einstellungen nicht in den Konfigurationscontainer migriert wurden), definieren Sie einen Domänencontroller im Stammverzeichnis Ihrer Active Directory-Gesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-135">If your settings are stored in the System container (which is typical with upgrade deployments that have not had the global settings migrated to the Configuration container), you define a domain controller in the root of your Active Directory forest.</span></span> <span data-ttu-id="dbbb1-136">Wenn sich die globalen Einstellungen im Konfigurationscontainer befinden (dies ist bei neuen Bereitstellungen oder Upgradebereitstellungen typisch, bei denen die Einstellungen zum Konfigurationscontainer migriert wurden), definieren Sie einen beliebigen Domänencontroller in der Gesamtstruktur.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-136">If the global settings are in the Configuration container (which is typical with new deployments or upgrade deployments where the settings have been migrated to the Configuration container), you define any domain controller in the forest.</span></span> <span data-ttu-id="dbbb1-137">Wenn Sie diesen Parameter nicht angeben, geht das Cmdlet davon aus, dass die Einstellungen im Konfigurationscontainer gespeichert sind und auf einen beliebigen Domänencontroller in AD &nbsp; DS verweisen.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-137">If you do not specify this parameter, the cmdlet assumes that the settings are stored in the Configuration container and refers to any domain controller in AD&nbsp;DS.</span></span>

    
    </div>
    
    <span data-ttu-id="dbbb1-138">Wenn Sie den Parameter **Domain** nicht angeben, ist der Standardwert die lokale Domäne.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-138">If you do not specify the **Domain** parameter, the default is the local domain.</span></span>
    
    <span data-ttu-id="dbbb1-139">Dieses Cmdlet gibt den Wert des **LC- \_ DOMAINSETTINGS- \_ Status \_ bereit** zurück, wenn die Domänenvorbereitung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="dbbb1-139">This cmdlet returns a value of **LC\_DOMAINSETTINGS\_STATE\_READY** if domain preparation was successful.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="dbbb1-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbbb1-140">See Also</span></span>


[<span data-ttu-id="dbbb1-141">Verwenden von Cmdlets zum Rückgängigmachen der Domänenvorbereitung für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dbbb1-141">Using cmdlets to reverse domain preparation for Lync Server 2013</span></span>](lync-server-2013-using-cmdlets-to-reverse-domain-preparation.md)  


[<span data-ttu-id="dbbb1-142">Vorbereiten von Domänen für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="dbbb1-142">Preparing domains for Lync Server 2013</span></span>](lync-server-2013-preparing-domains.md)  
  

<span data-ttu-id="dbbb1-143"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="dbbb1-143"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

