---
title: 'Lync Server 2013: Einrichten des SQL Server-Protokollversands zwischen der primären Spiegeldatenbank und der sekundären Datenbank des Protokollversands'
description: 'Lync Server 2013: Einrichten des SQL Server-Protokollversands zwischen der primären Spiegelung und der sekundären Protokollversanddatenbank'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up SQL Server Log Shipping between the primary mirror and the Log Shipping secondary database
ms:assetid: 4e8e9ce9-4301-47f2-a0c3-669afeb53295
ms:mtpsurl: https://technet.microsoft.com/library/JJ204887(v=OCS.15)
ms:contentKeyID: 48184119
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b1655721410da23d569af4df7aa656f3be69e383
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423960"
---
# <a name="setting-up-sql-server-log-shipping-between-the-primary-mirror-and-the-log-shipping-secondary-database-in-lync-server-2013"></a><span data-ttu-id="c002a-103">Einrichten des SQL Server-Protokollversands zwischen der primären Spiegeldatenbank und der sekundären Datenbank des Protokollversands in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c002a-103">Setting up SQL Server Log Shipping between the primary mirror and the Log Shipping secondary database in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c002a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c002a-104">

<span> </span></span></span>

<span data-ttu-id="c002a-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="c002a-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="c002a-106">Führen Sie die folgenden Schritte aus, damit der Protokollversand fortgesetzt wird, wenn die primäre Datenbank für beständige Chats auf die Spiegeldatenbank übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="c002a-106">Perform the following steps for log shipping to continue if the primary Persistent Chat database is failed over to its mirror database.</span></span>

1.  <span data-ttu-id="c002a-107">Manuelles Failover der primären persistent-Chat-Datenbank auf die Spiegelung.</span><span class="sxs-lookup"><span data-stu-id="c002a-107">Manually fail over the primary Persistent Chat database to the mirror.</span></span> <span data-ttu-id="c002a-108">Dies erfolgt mithilfe der lync Server-Verwaltungsshell und des **Invoke-CsDatabaseFailover-** Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="c002a-108">This is done by using the Lync Server Management Shell and the **Invoke-CsDatabaseFailover** cmdlet.</span></span> <span data-ttu-id="c002a-109">Ausführliche Informationen finden Sie unter "Verwenden von Cmdlets für die lync Server-Verwaltungsshell" unter [Bereitstellen der SQL-Spiegelung für den Back-End-Server mit einer höheren Verfügbarkeit in lync Server 2013](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md).</span><span class="sxs-lookup"><span data-stu-id="c002a-109">For details, see "Using Lync Server Management Shell Cmdlets" in [Deploying SQL mirroring for Back End Server high availability in Lync Server 2013](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md).</span></span>

2.  <span data-ttu-id="c002a-110">Stellen Sie mithilfe von SQL Server Management Studio eine Verbindung mit der primären persistent Chat Server-Spiegelungs Instanz her.</span><span class="sxs-lookup"><span data-stu-id="c002a-110">Using the SQL Server Management Studio, connect to the primary Persistent Chat Server mirror instance.</span></span>

3.  <span data-ttu-id="c002a-111">Stellen Sie sicher, dass der SQL Server-Agent ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="c002a-111">Be sure that the SQL Server Agent is running.</span></span>

4.  <span data-ttu-id="c002a-112">Klicken Sie mit der rechten Maustaste auf die mgc-Datenbank und klicken Sie auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="c002a-112">Right-click the mgc database, and then click **Properties**.</span></span>

5.  <span data-ttu-id="c002a-113">Klicken Sie unter **Seite auswählen** auf **Transaktionsprotokollversand**.</span><span class="sxs-lookup"><span data-stu-id="c002a-113">Under **Select a page**, click **Transaction Log Shipping**.</span></span>

6.  <span data-ttu-id="c002a-114">Aktivieren Sie das Kontrollkästchen **Diese Datenbank als primäre Datenbank in einer Protokollversandkonfiguration aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="c002a-114">Select the **Enable this as a primary database in a log shipping configuration** check box.</span></span>

7.  <span data-ttu-id="c002a-115">Klicken Sie unter **Transaktionsprotokollsicherungen** auf **Sicherungseinstellungen**.</span><span class="sxs-lookup"><span data-stu-id="c002a-115">Under **Transaction log backups**, click **Backup Settings**.</span></span>

8.  <span data-ttu-id="c002a-116">Geben Sie im Feld **Netzwerkpfad zum Sicherungsordner** den Netzwerkpfad zu der Freigabe ein, die Sie für den Transaktionsprotokoll-Sicherungsordner erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="c002a-116">In the **Network path to the backup folder** box, type the network path to the share you created for the transaction log backup folder.</span></span>

9.  <span data-ttu-id="c002a-p102">Wenn sich der Sicherungsordner auf dem primären Server befindet, geben Sie den lokalen Pfad zum Sicherungsordner im Feld **Wenn sich der Sicherungsordner auf dem primären Server befindet, geben Sie den lokalen Pfad zum Ordner ein** ein. (Wenn sich der Sicherungsordner nicht auf dem primären Server befindet, können Sie dieses Feld leer lassen.)</span><span class="sxs-lookup"><span data-stu-id="c002a-p102">If the backup folder is located on the primary server, type the local path to the backup folder in the **If the backup folder is located on the primary server, type a local path to the folder** box. (If the backup folder is not on the primary server, you can leave this box empty.)</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="c002a-119">Wenn das SQL Server-Dienstkonto auf dem primären Server unter dem lokalen Systemkonto ausgeführt wird, müssen Sie den Sicherungsordner auf dem primären Server erstellen und einen lokalen Pfad zu diesem Ordner angeben.</span><span class="sxs-lookup"><span data-stu-id="c002a-119">If the SQL Server service account on your primary server runs under the local system account, you must create your backup folder on the primary server and specify a local path to that folder.</span></span>

    
    </div>

10. <span data-ttu-id="c002a-120">Konfigurieren Sie den Parameter **Dateien löschen, die älter sind als** und den Parameter **Warnen, wenn keine Sicherung erfolgt in**.</span><span class="sxs-lookup"><span data-stu-id="c002a-120">Configure the **Delete files older than** and **Alert if no backup occurs within** parameters.</span></span>

11. <span data-ttu-id="c002a-121">Schauen Sie sich den Sicherungszeitplan im Feld **Zeitplan** unter **Sicherungsauftrag** an.</span><span class="sxs-lookup"><span data-stu-id="c002a-121">Look at the backup schedule listed in the **Schedule** box under **Backup job**.</span></span> <span data-ttu-id="c002a-122">Wenn Sie den Zeitplan für Ihre Installation anpassen möchten, klicken Sie auf **Planen**, und passen Sie den Zeitplan des SQL Server-Agents nach Bedarf an.</span><span class="sxs-lookup"><span data-stu-id="c002a-122">To customize the schedule for your installation, click **Schedule**, and adjust the SQL Server Agent schedule, as required.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="c002a-123">Verwenden Sie die gleichen Einstellungen, die Sie auch für die primäre Datenbank verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="c002a-123">Use the same settings that you used for the primary database.</span></span>

    
    </div>

12. <span data-ttu-id="c002a-124">Wählen Sie unter **Komprimierung** den Eintrag **Standardservereinstellung verwenden** aus und klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="c002a-124">Under **Compression**, select **Use the default server setting**, and click **OK**.</span></span>

13. <span data-ttu-id="c002a-125">Klicken Sie unter **Sekundäre Serverinstanzen und Datenbanken** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="c002a-125">Under **Secondary server instances and databases**, click **Add**.</span></span>

14. <span data-ttu-id="c002a-126">Klicken Sie auf **Verbinden** und stellen Sie eine Verbindung mit der Instanz von SQL Server her, die Sie als sekundären Server konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="c002a-126">Click **Connect**, and connect to the instance of SQL Server that you have configured as your secondary server.</span></span>

15. <span data-ttu-id="c002a-127">Wählen Sie im Feld **Sekundäre Datenbank** die Datenbank **mgc** aus der Liste aus.</span><span class="sxs-lookup"><span data-stu-id="c002a-127">In the **Secondary Database** box, select the **mgc** database from the list.</span></span>

16. <span data-ttu-id="c002a-128">Wählen Sie auf der Registerkarte **Sekundäre Datenbank initialisieren** die Option **Nein, die sekundäre Datenbank ist initialisiert** aus.</span><span class="sxs-lookup"><span data-stu-id="c002a-128">On the **Initialize Secondary database** tab, select the option **No, the secondary database is initialized**.</span></span>

17. <span data-ttu-id="c002a-p104">Geben Sie auf der Registerkarte **Dateien kopieren** unter **Zielordner für kopierte Dateien** den Pfad des Ordners ein, in den die Transaktionsprotokollsicherungen kopiert werden sollen, und klicken Sie auf **OK**. Dieser Ordner befindet sich in der Regel auf dem sekundären Server.</span><span class="sxs-lookup"><span data-stu-id="c002a-p104">On the **Copy Files** tab, in **Destination folder for copied files**, type the path of the folder into which the transaction logs backups should be copied, and click **OK**. This folder is often located on the secondary server.</span></span>

18. <span data-ttu-id="c002a-131">Öffnen Sie die Dropdownliste **Skript für Konfiguration erstellen** und wählen Sie **Skript für Konfiguration in Fenster 'Neue Abfrage' schreiben** aus.</span><span class="sxs-lookup"><span data-stu-id="c002a-131">Open the **Script Configuration** drop-down list, and select **Script Configuration to New Query Window**.</span></span>

19. <span data-ttu-id="c002a-132">Klicken Sie im neuen Abfragefenster unter **Datenbankeigenschaften** auf **OK**, um mit der Konfiguration zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="c002a-132">In the new query window, in **Database Properties**, click **OK** to begin the configuration process.</span></span>

20. <span data-ttu-id="c002a-133">Wählen Sie die erste Hälfte der Abfrage aus, und führen Sie Sie aus (siehe Schritt 18) bis zur Zeile:-- \* \* \* \* \* \* Ende: Skript, das bei primär ausgeführt werden soll: \* \* \* \* \* \* .</span><span class="sxs-lookup"><span data-stu-id="c002a-133">Select and run the first half of the query (see step 18) up to the line: -- \*\*\*\*\*\* End: Script to be run at Primary: \*\*\*\*\*\*.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="c002a-134">Das manuelle Ausführen dieses Skripts ist erforderlich, da SQL Server Management Studio mehrere primäre Datenbanken in einer SQL Server-Protokollversandkonfiguration nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="c002a-134">Manually running this script is necessary because SQL Server Management Studio does not support multiple primary databases in a SQL Server Log Shipping configuration.</span></span>

    
    </div>

21. <span data-ttu-id="c002a-135">Wählen Sie **Abbrechen** aus, um das Konfigurationsfenster für den Protokolldateiversand zu schließen und ein funktionierendes Setup zu erstellen, das den Protokolldateiversand für die primäre und für die gespiegelte Datenbank (bei einem Failover) ordnungsgemäß implementiert. </span><span class="sxs-lookup"><span data-stu-id="c002a-135">Select **Cancel** to close the Log File shipping configuration panel and to establish a working setup that correctly implements the log file shipping for both the primary and mirrored database (in case of failover).</span></span>

22. <span data-ttu-id="c002a-136">Manuelles Zurücksetzen der primären beständigen Chat Datenbank auf das primäre.</span><span class="sxs-lookup"><span data-stu-id="c002a-136">Manually fail back the primary Persistent Chat database to the primary.</span></span> <span data-ttu-id="c002a-137">Dies erfolgt mithilfe der lync Server-Verwaltungsshell und des Cmdlets **Invoke-CsDatabaseFailover** .</span><span class="sxs-lookup"><span data-stu-id="c002a-137">This is done by using the Lync Server Management Shell, and the **Invoke-CsDatabaseFailover** cmdlet.</span></span> <span data-ttu-id="c002a-138">Ausführliche Informationen finden Sie unter "Verwenden von Cmdlets für die lync Server-Verwaltungsshell" unter [Bereitstellen der SQL-Spiegelung für den Back-End-Server mit einer höheren Verfügbarkeit in lync Server 2013](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md).</span><span class="sxs-lookup"><span data-stu-id="c002a-138">For details, see "Using Lync Server Management Shell Cmdlets" in [Deploying SQL mirroring for Back End Server high availability in Lync Server 2013](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md).</span></span>

<div>

## <a name="see-also"></a><span data-ttu-id="c002a-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c002a-139">See Also</span></span>


[<span data-ttu-id="c002a-140">Bereitstellen der SQL-Spiegelung für eine hohe Verfügbarkeit von Back-End-Servern in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c002a-140">Deploying SQL mirroring for Back End Server high availability in Lync Server 2013</span></span>](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md)  
[<span data-ttu-id="c002a-141">Bereitstellen der SQL-Spiegelung für eine hohe Verfügbarkeit von Back-End-Servern in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c002a-141">Deploying SQL mirroring for Back End Server high availability in Lync Server 2013</span></span>](lync-server-2013-deploying-sql-mirroring-for-back-end-server-high-availability.md)  
  

<span data-ttu-id="c002a-142"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c002a-142"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

