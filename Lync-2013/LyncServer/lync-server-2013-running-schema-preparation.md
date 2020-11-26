---
title: 'Lync Server 2013: Ausführen der Schemavorbereitung'
description: 'Lync Server 2013: Ausführen der Schemavorbereitung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Running schema preparation
ms:assetid: 9d02bdb1-ff29-417a-bcce-b068b31207d8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412729(v=OCS.15)
ms:contentKeyID: 48184911
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0991bbff7f54f8b8b9eb01fc87f752e00f3dcbfd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442194"
---
# <a name="running-active-directory-schema-preparation-in-lync-server-2013"></a><span data-ttu-id="2a221-103">Ausführen der Active Directory-Schemavorbereitung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2a221-103">Running Active Directory schema preparation in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2a221-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2a221-104">

<span> </span></span></span>

<span data-ttu-id="2a221-105">_**Letztes Änderungsdatum des Themas:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="2a221-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="2a221-106">Sie können das Active Directory-Schema mithilfe von Setup-oder lync Server-Verwaltungsshell-Cmdlets vorbereiten.</span><span class="sxs-lookup"><span data-stu-id="2a221-106">You can use Setup or Lync Server Management Shell cmdlets to prepare the Active Directory schema.</span></span> <span data-ttu-id="2a221-107">Das Cmdlet, das das Active Directory-Schema erweitert, ist **install-CsAdServerSchema**.</span><span class="sxs-lookup"><span data-stu-id="2a221-107">The cmdlet that extends the Active Directory schema is **Install-CsAdServerSchema**.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2a221-108">Das Schema Vorbereitungs-Cmdlet (<STRONG>install-CsAdServerSchema</STRONG>) muss auf den Schemamaster zugreifen, der erfordert, dass der Remoteregistrierungsdienst ausgeführt wird und dass der Remote Registrierungsschlüssel aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="2a221-108">The schema preparation cmdlet (<STRONG>Install-CsAdServerSchema</STRONG>) must access the schema master, which requires that the remote registry service is running and that the remote registry key is enabled.</span></span> <span data-ttu-id="2a221-109">Wenn der Remoteregistrierungsdienst auf dem Schemamaster nicht aktiviert werden kann, können Sie das Cmdlet lokal auf dem Schemamaster ausführen.</span><span class="sxs-lookup"><span data-stu-id="2a221-109">If the remote registry service cannot be enabled on the schema master, you can run the cmdlet locally on the schema master.</span></span> <span data-ttu-id="2a221-110">Details zum Remotezugriff auf die Registrierung finden Sie im Microsoft Knowledge Base-Artikel 314837, "Verwalten des Remotezugriffs auf die Registrierung" unter <A href="https://go.microsoft.com/fwlink/p/?linkid=125769">https://go.microsoft.com/fwlink/p/?linkId=125769</A> .</span><span class="sxs-lookup"><span data-stu-id="2a221-110">For details about registry remote access, see Microsoft Knowledge Base article 314837, "How to Manage Remote Access to the Registry," at <A href="https://go.microsoft.com/fwlink/p/?linkid=125769">https://go.microsoft.com/fwlink/p/?linkId=125769</A>.</span></span>



</div>

<span data-ttu-id="2a221-111">Nachdem Sie die Schemavorbereitung abgeschlossen haben, überprüfen Sie manuell, ob die Schemapartition repliziert wurde, bevor Sie mit der Gesamtstrukturvorbereitung fortfahren.</span><span class="sxs-lookup"><span data-stu-id="2a221-111">After you complete schema preparation, manually verify that the schema partition has been replicated before proceeding to forest preparation.</span></span> <span data-ttu-id="2a221-112">Ausführliche Informationen finden Sie unter [Überprüfen der Active Directory-Schemareplikation in lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span><span class="sxs-lookup"><span data-stu-id="2a221-112">For details, see [Verifying Active Directory schema replication in Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span></span>

<div>

## <a name="to-use-setup-to-prepare-the-schema-of-the-current-forest"></a><span data-ttu-id="2a221-113">So verwenden Sie Setup zum Vorbereiten des Schemas der aktuellen Gesamtstruktur</span><span class="sxs-lookup"><span data-stu-id="2a221-113">To use Setup to prepare the schema of the current forest</span></span>

1.  <span data-ttu-id="2a221-114">Melden Sie sich bei einem Server in Ihrer Gesamtstruktur als Mitglied der Gruppe Schemaadministratoren und mit Administratorrechten für den Schemamaster an.</span><span class="sxs-lookup"><span data-stu-id="2a221-114">Log on to a server in your forest as a member of the Schema Admins group and with administrator rights on the schema master.</span></span>

2.  <span data-ttu-id="2a221-115">Führen Sie im lync Server 2013-Installationsordner oder-Medium Setup.exe aus, um den Bereitstellungs-Assistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="2a221-115">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Deployment Wizard.</span></span>

3.  <span data-ttu-id="2a221-116">Wenn Sie aufgefordert werden, die Microsoft Visual C++-Installation zu installieren, klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2a221-116">If you are prompted to install the Microsoft Visual C++ Redistributable, click **Yes**.</span></span>

4.  <span data-ttu-id="2a221-117">Im Dialogfeld "lync Server 2013-Setup" werden Sie aufgefordert, einen Speicherort zum Installieren der lync Server-Dateien anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2a221-117">The Lync Server 2013 Setup dialog box prompts you for a location to install the Lync Server files.</span></span> <span data-ttu-id="2a221-118">Wählen Sie den Standardspeicherort aus, oder **Navigieren** Sie zu einem Speicherort Ihrer Wahl, und klicken Sie dann auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="2a221-118">Choose the default location or **Browse** to a location of your choice, and then click **Install**.</span></span>

5.  <span data-ttu-id="2a221-119">Aktivieren Sie auf der Seite Lizenzvertrag **die Kontrollkästchen Ich akzeptiere die Bedingungen des Lizenzvertrags**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a221-119">On the License Agreement page, check **I accept the terms in the license agreement**, and then click **OK**.</span></span>

6.  <span data-ttu-id="2a221-120">Das Installationsprogramm installiert die lync Server Core-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="2a221-120">The installer installs the Lync Server Core Components.</span></span>

7.  <span data-ttu-id="2a221-121">Wenn der Bereitstellungs-Assistent bereit ist, klicken Sie auf **Active Directory vorbereiten**, und warten Sie, bis der Bereitstellungsstatus ermittelt wurde.</span><span class="sxs-lookup"><span data-stu-id="2a221-121">When the Deployment Wizard is ready, click **Prepare Active Directory**, and then wait for the deployment state to be determined.</span></span>

8.  <span data-ttu-id="2a221-122">Klicken Sie in **Schritt 1: Schema vorbereiten** auf **Ausführen**.</span><span class="sxs-lookup"><span data-stu-id="2a221-122">At **Step 1: Prepare Schema**, click **Run**.</span></span>

9.  <span data-ttu-id="2a221-123">Klicken Sie auf der Seite **Schema vorbereiten** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="2a221-123">On the **Prepare Schema** page, click **Next**.</span></span>

10. <span data-ttu-id="2a221-124">Suchen Sie auf der Seite **Befehle ausführen** nach **Aufgabenstatus: Abgeschlossen** und klicken Sie dann auf **Protokoll anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="2a221-124">On the **Executing Commands** page, look for **Task status: Completed**, and then click **View Log**.</span></span>

11. <span data-ttu-id="2a221-125">Erweitern Sie in der Spalte **Aktion** die **Schema** Vorbereitung, suchen Sie nach dem **\<Success\>** Ausführungsergebnis am Ende jeder Aufgabe, um zu überprüfen, ob die Schemavorbereitung erfolgreich abgeschlossen wurde, schließen Sie das Protokoll, und klicken Sie dann auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="2a221-125">Under the **Action** column, expand **Schema Prep**, look for the **\<Success\>** Execution Result at the end of each task to verify that schema preparation completed successfully, close the log, and then click **Finish**.</span></span>

12. <span data-ttu-id="2a221-126">Warten Sie, bis die Active Directory-Replikation abgeschlossen ist, oder erzwingen Sie die Replikation.</span><span class="sxs-lookup"><span data-stu-id="2a221-126">Wait for Active Directory replication to complete or force replication.</span></span>

13. <span data-ttu-id="2a221-127">Überprüfen Sie manuell, ob die Schemaänderungen auf alle anderen Domänencontroller repliziert wurden.</span><span class="sxs-lookup"><span data-stu-id="2a221-127">Manually verify that the schema changes replicated to all other domain controllers.</span></span> <span data-ttu-id="2a221-128">Ausführliche Informationen finden Sie unter [Überprüfen der Active Directory-Schemareplikation in lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span><span class="sxs-lookup"><span data-stu-id="2a221-128">For details, see [Verifying Active Directory schema replication in Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span></span>

</div>

<div>

## <a name="to-use-cmdlets-to-prepare-the-schema-of-the-current-forest"></a><span data-ttu-id="2a221-129">So verwenden Sie Cmdlets zum Vorbereiten des Schemas der aktuellen Gesamtstruktur</span><span class="sxs-lookup"><span data-stu-id="2a221-129">To use cmdlets to prepare the schema of the current forest</span></span>

1.  <span data-ttu-id="2a221-130">Melden Sie sich bei einem Computer in der Gesamtstruktur als Mitglied der Gruppe Schemaadministratoren und mit Administratorrechten für den Schemamaster an.</span><span class="sxs-lookup"><span data-stu-id="2a221-130">Log on to a computer in the forest as a member of the Schema Admins group and with administrator rights on the schema master.</span></span>

2.  <span data-ttu-id="2a221-131">Installieren Sie die lync Server Core-Komponenten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="2a221-131">Install Lync Server Core components as follows:</span></span>
    
    1.  <span data-ttu-id="2a221-132">Führen Sie im lync Server 2013-Installationsordner oder-Medium Setup.exe aus, um den lync Server-Bereitstellungs-Assistenten zu starten.</span><span class="sxs-lookup"><span data-stu-id="2a221-132">From the Lync Server 2013 installation folder or media, run Setup.exe to start the Lync Server Deployment Wizard.</span></span>
    
    2.  <span data-ttu-id="2a221-133">Wenn Sie aufgefordert werden, die Microsoft Visual C++-Installation zu installieren, klicken Sie auf **Ja**.</span><span class="sxs-lookup"><span data-stu-id="2a221-133">If you are prompted to install the Microsoft Visual C++ Redistributable, click **Yes**.</span></span>
    
    3.  <span data-ttu-id="2a221-134">Im Dialogfeld "lync Server 2013-Setup" werden Sie aufgefordert, einen Speicherort zum Installieren der lync Server-Dateien anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="2a221-134">The Lync Server 2013 Setup dialog box prompts you for a location to install the Lync Server files.</span></span> <span data-ttu-id="2a221-135">Wählen Sie den Standardspeicherort aus, oder **Navigieren** Sie zu einem Speicherort Ihrer Wahl, und klicken Sie dann auf **Installieren**.</span><span class="sxs-lookup"><span data-stu-id="2a221-135">Choose the default location or **Browse** to a location of your choice, and then click **Install**.</span></span>
    
    4.  <span data-ttu-id="2a221-136">Aktivieren Sie auf der Seite Lizenzvertrag **die Kontrollkästchen Ich akzeptiere die Bedingungen des Lizenzvertrags**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="2a221-136">On the License Agreement page, check **I accept the terms in the license agreement**, and then click **OK**.</span></span> <span data-ttu-id="2a221-137">Das Installationsprogramm installiert die lync Server 2013-Core-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="2a221-137">The installer installs the Lync Server 2013 Core Components.</span></span>

3.  <span data-ttu-id="2a221-138">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="2a221-138">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

4.  <span data-ttu-id="2a221-139">Führen Sie folgenden Befehl aus:</span><span class="sxs-lookup"><span data-stu-id="2a221-139">Run:</span></span>
    
        Install-CsAdServerSchema [-Ldf <directory where the .ldf file is located>] 
    
    <span data-ttu-id="2a221-140">Wenn Sie den LDF-Parameter nicht angeben, ist der Standardwert der lync Server 2013-Installationspfad, der aus der Registrierung gelesen wird.</span><span class="sxs-lookup"><span data-stu-id="2a221-140">If you do not specify the Ldf parameter, the default value is the Lync Server 2013 installation path that is read from the registry.</span></span>
    
    <span data-ttu-id="2a221-141">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2a221-141">For example:</span></span>
    
        Install-CsAdServerSchema -Ldf "C:\Program Files\Microsoft Lync Server 2013\Deployment\Setup"

5.  <span data-ttu-id="2a221-142">Verwenden Sie das folgende Cmdlet, um zu überprüfen, ob die Schemavorbereitung bis zum Abschluss ausgeführt wurde.</span><span class="sxs-lookup"><span data-stu-id="2a221-142">Use the following cmdlet to verify that schema preparation ran to completion.</span></span>
    
        Get-CsAdServerSchema 
    
    <span data-ttu-id="2a221-143">Dieses Cmdlet gibt den Wert des **Schema \_ Versions \_ Status \_ Current** zurück, wenn die Schemavorbereitung erfolgreich war.</span><span class="sxs-lookup"><span data-stu-id="2a221-143">This cmdlet returns a value of **SCHEMA\_VERSION\_STATE\_CURRENT** if schema preparation was successful.</span></span>

6.  <span data-ttu-id="2a221-144">Warten Sie, bis die Active Directory-Replikation abgeschlossen ist, oder erzwingen Sie die Replikation.</span><span class="sxs-lookup"><span data-stu-id="2a221-144">Wait for Active Directory replication to complete or force replication.</span></span>

7.  <span data-ttu-id="2a221-145">Überprüfen Sie manuell, ob die Schemaänderungen auf alle anderen Domänencontroller repliziert wurden.</span><span class="sxs-lookup"><span data-stu-id="2a221-145">Manually verify that the schema changes replicated to all other domain controllers.</span></span> <span data-ttu-id="2a221-146">Ausführliche Informationen finden Sie unter [Überprüfen der Active Directory-Schemareplikation in lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span><span class="sxs-lookup"><span data-stu-id="2a221-146">For details, see [Verifying Active Directory schema replication in Lync Server 2013](lync-server-2013-verifying-schema-replication.md).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2a221-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2a221-147">See Also</span></span>


[<span data-ttu-id="2a221-148">Überprüfen der Active Directory-Schemareplikation in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2a221-148">Verifying Active Directory schema replication in Lync Server 2013</span></span>](lync-server-2013-verifying-schema-replication.md)  


[<span data-ttu-id="2a221-149">Vorbereiten des Active Directory-Schemas in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2a221-149">Preparing the Active Directory schema in Lync Server 2013</span></span>](lync-server-2013-preparing-the-active-directory-schema.md)  
  

<span data-ttu-id="2a221-150"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2a221-150"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

