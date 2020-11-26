---
title: 'Lync Server 2013: Hinzufügen eines Server für beständigen Chat zu einer Topologie'
description: 'Lync Server 2013: Hinzufügen eines beständigen Chat Servers zur Topologie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Add Persistent Chat Server to the topology
ms:assetid: 8389b307-8c17-4e45-b3b5-5dc9fcfc2ffb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205049(v=OCS.15)
ms:contentKeyID: 48184682
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0321978ce4a0c7381cf2915030267645931f572b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439268"
---
# <a name="add-persistent-chat-server-to-the-topology-in-lync-server-2013"></a><span data-ttu-id="c70f0-103">Hinzufügen eines Server für beständigen Chat zu einer Topologie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c70f0-103">Add Persistent Chat Server to the topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c70f0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c70f0-104">

<span> </span></span></span>

<span data-ttu-id="c70f0-105">_**Letztes Änderungsdatum des Themas:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="c70f0-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="c70f0-106">Sie müssen lync Server 2013 und die Unterstützung für beständigen Chat Server in Ihre Topologie einbeziehen, bevor Sie Ihre Bereitstellung für die Unterstützung des beständigen Chat Servers konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="c70f0-106">You must incorporate Lync Server 2013, Persistent Chat Server support in your topology before you can configure your deployment to support Persistent Chat Server.</span></span> <span data-ttu-id="c70f0-107">Die Informationen in diesem Thema beschreiben, wie Sie mithilfe des Topologie-Generators Ihrer vorhandenen Topologie Unterstützung für beständigen Chat Server hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="c70f0-107">The information in this topic describes how to use Topology Builder to add Persistent Chat Server support to your existing topology.</span></span>

<div>

## <a name="to-add-persistent-chat-server-to-a-topology"></a><span data-ttu-id="c70f0-108">So fügen Sie einen beständigen Chat Server zu einer Topologie hinzu</span><span class="sxs-lookup"><span data-stu-id="c70f0-108">To add Persistent Chat Server to a topology</span></span>

<span data-ttu-id="c70f0-109">Führen Sie die folgenden Schritte aus, um einen einzelnen beständigen Chat Server Pool ohne Disaster Recovery-Konfiguration zu installieren.</span><span class="sxs-lookup"><span data-stu-id="c70f0-109">Perform the following steps for installing a single Persistent Chat Server pool without a disaster recovery configuration.</span></span> <span data-ttu-id="c70f0-110">Informationen zum Konfigurieren eines gestreckten beständigen Chat-Server Pools für Hochverfügbarkeits-und Disaster Recovery finden Sie unter [Konfigurieren des beständigen Chat Servers für Hochverfügbarkeits-und Disaster Recovery in lync Server 2013](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="c70f0-110">For configuring a stretched Persistent Chat Server pool for high availability and disaster recovery, see [Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013](lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md) in the Deployment documentation.</span></span>

<span data-ttu-id="c70f0-111">Zum Bereitstellen mehrerer beständiger Chat Server-Pools wiederholen Sie diesen Vorgang für jeden Pool.</span><span class="sxs-lookup"><span data-stu-id="c70f0-111">To deploy multiple Persistent Chat Server pools, repeat the same process for each pool.</span></span>

1.  <span data-ttu-id="c70f0-112">Melden Sie sich auf einem Computer, auf dem lync Server 2013 ausgeführt wird oder auf dem die lync Server-Verwaltungstools installiert sind, mit einem Konto an, das Mitglied der lokalen Gruppe "Benutzer" (oder einem Konto mit entsprechenden Benutzerrechten) ist.</span><span class="sxs-lookup"><span data-stu-id="c70f0-112">On a computer that is running Lync Server 2013 or on which the Lync Server administrative tools are installed, log on using an account that is a member of the local Users group (or an account with equivalent user rights).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c70f0-113">Sie können eine Topologie definieren, indem Sie ein Konto verwenden, das ein Mitglied der lokalen Benutzergruppe ist, aber zum Veröffentlichen einer Topologie, die erforderlich ist, um einen lync Server 2013-Server zu installieren. Sie müssen ein Konto verwenden, das ein Mitglied der Gruppe " <STRONG>Domänen-Admins</STRONG> " und der Gruppe " <STRONG>RTCUniversalServerAdmins</STRONG> " ist und über Vollzugriffsberechtigungen (also lesen, schreiben und ändern) für den Dateispeicher verfügt, den Sie für den Dateispeicher des beständigen Chat Servers verwenden möchten (d...</span><span class="sxs-lookup"><span data-stu-id="c70f0-113">You can define a topology by using an account that is a member of the local Users group, but to publish a topology, which is required to install a Lync Server 2013 server, you must use an account that is a member of the <STRONG>Domain Admins</STRONG> group and the <STRONG>RTCUniversalServerAdmins</STRONG> group, and that has full control permissions (that is, read, write, and modify) on the file store that you are going to use for the Persistent Chat Server file store (that is, so that Topology Builder can configure the required DACLs), or an account with equivalent rights.</span></span>

    
    </div>

2.  <span data-ttu-id="c70f0-114">Starten Sie den Topologie-Generator.</span><span class="sxs-lookup"><span data-stu-id="c70f0-114">Start Topology Builder.</span></span>

3.  <span data-ttu-id="c70f0-115">Navigieren Sie in der Konsolenstruktur zum Knoten **beständiger Chat Pools** , und erweitern Sie ihn, um einen Server Pool für beständigen Chat auszuwählen, oder klicken Sie mit der rechten Maustaste auf den Knoten, und wählen Sie **neuer beständiger Chat Pool** aus.</span><span class="sxs-lookup"><span data-stu-id="c70f0-115">In the console tree, navigate to the **Persistent Chat Pools** node and expand it to select a Persistent Chat Server pool, or right-click the node and select **New Persistent Chat Pool**.</span></span> <span data-ttu-id="c70f0-116">Sie müssen den vollqualifizierten Domänennamen (Fully Qualified Domain Name, FQDN) des Pools definieren und angeben, ob es sich bei dem Pool um eine Einzelserver Pool-oder um die Bereitstellung mehrerer Server Pools handelt.</span><span class="sxs-lookup"><span data-stu-id="c70f0-116">You must define the pool’s fully qualified domain name (FQDN), and indicate whether the pool will be a single-server pool or multiple-server pool deployment.</span></span>
    
    <span data-ttu-id="c70f0-117">Wählen Sie **Pool mit mehreren Computern** oder **Pool mit einem Computer** aus.</span><span class="sxs-lookup"><span data-stu-id="c70f0-117">You can choose a **Multiple Computer Pool** or a **Single Computer Pool**.</span></span> <span data-ttu-id="c70f0-118">Wählen Sie die erste Option aus, wenn Sie beabsichtigen, mehr als einen beständigen Chat Server-Front-End-Server in Ihrem beständigen Chat-Serverpool zu haben.</span><span class="sxs-lookup"><span data-stu-id="c70f0-118">Choose the former if you are planning to have more than one Persistent Chat Server Front End Server in your Persistent Chat Server pool.</span></span> <span data-ttu-id="c70f0-119">Wählen Sie diese Option jetzt oder zu einem späteren Zeitpunkt, da Sie einem Pool mit einem Computer später keine zusätzlichen Server hinzufügen können.</span><span class="sxs-lookup"><span data-stu-id="c70f0-119">Make this choice now, or at a later point, because after you create a single computer pool, you cannot add additional servers to it later.</span></span> <span data-ttu-id="c70f0-120">Wenn Sie einen Pool mit mehreren Computern auswählen, geben Sie die Namen der einzelnen beständigen Chat Server-Front-End-Server ein, aus denen sich der Pool zusammensetzt.</span><span class="sxs-lookup"><span data-stu-id="c70f0-120">If you choose a multiple computer pool, enter the names of the individual Persistent Chat Server Front End Servers that comprise the pool.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="c70f0-121">Wenn die Serverrolle "beständiger Chat" auf einem lync Server 2013 &nbsp; Standard Edition-Server installiert wird, muss der FQDN dem FQDN des Standard Edition-Servers entsprechen.</span><span class="sxs-lookup"><span data-stu-id="c70f0-121">If the Persistent Chat Server role is being installed on a Lync Server 2013&nbsp;Standard Edition server, the FQDN needs to match the FQDN of the Standard Edition server.</span></span>

    
    </div>

4.  <span data-ttu-id="c70f0-122">Definieren Sie einen einfachen **Anzeige Namen** für den Server Pool des beständigen Chats.</span><span class="sxs-lookup"><span data-stu-id="c70f0-122">Define a simple **Display Name** for the Persistent Chat Server pool.</span></span> <span data-ttu-id="c70f0-123">Der Anzeigename kann von benutzerdefinierten Clients verwendet werden, insbesondere dann, wenn mehrere beständige Chat Server Pools vorhanden sind, um Räume zu unterscheiden.</span><span class="sxs-lookup"><span data-stu-id="c70f0-123">The display name can be used by custom clients, particularly when there are multiple Persistent Chat Server pools, to differentiate rooms.</span></span>

5.  <span data-ttu-id="c70f0-124">Definieren Sie den Port, der vom beständigen Chat Server für die Kommunikation mit lync Server-Front-End-Servern verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="c70f0-124">Define the port used by the Persistent Chat Server to communicate with Lync Server Front End Servers.</span></span> <span data-ttu-id="c70f0-125">Der Standardport lautet 5041.</span><span class="sxs-lookup"><span data-stu-id="c70f0-125">The default port is 5041.</span></span>

6.  <span data-ttu-id="c70f0-126">Falls in Ihrer Organisation Kompatibilitätsunterstützung erforderlich ist, aktivieren Sie das Kontrollkästchen **Kompatibilität aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="c70f0-126">If your organization requires compliance support, select the **Enable compliance** check box.</span></span> <span data-ttu-id="c70f0-127">Falls ausgewählt, wird der beständige Chat Server-Kompatibilitätsdienst auf demselben Computer wie der Front-End-Server des beständigen Chats installiert.</span><span class="sxs-lookup"><span data-stu-id="c70f0-127">If chosen, the Persistent Chat Server Compliance service is installed on the same computer as the Persistent Chat Server Front End Server.</span></span> <span data-ttu-id="c70f0-128">Sie werden aufgefordert, einen SQL Server-Back-End-Server für die beständige Chat Server-Kompatibilität zu einem späteren Zeitpunkt auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="c70f0-128">You are prompted to select a SQL Server Back End Server for Persistent Chat Server Compliance later.</span></span>

7.  <span data-ttu-id="c70f0-129">Zuweisen einer Website Affinität für den Server Pool für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="c70f0-129">Assign site affinity for the Persistent Chat Server pool.</span></span> <span data-ttu-id="c70f0-130">Aktivieren Sie das Kontrollkästchen **diesen Pool als Standard \<SiteName\> für Website verwenden** , oder **verwenden Sie diesen Pool als Standard für alle Websites** , um diesen Server Pool für beständigen Chat als Standardpool für die aktuelle Website oder alle Websites festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c70f0-130">Select the **Use this pool as default for site \<SiteName\>** check box or **Use this pool as default for all sites** to designate this Persistent Chat Server pool as the default pool for the current site or all sites.</span></span> <span data-ttu-id="c70f0-131">Wenn der lync 2013-Client zum Erstellen und Verwalten von Räumen verwendet wird, wird der Standardpool, der der Website des Benutzers zugeordnet ist, von der raumerstellung und-Verwaltung verwendet, um Raum Erstellungs-und Verwaltungsvorgänge an diesen Pool weiterleiten zu können.</span><span class="sxs-lookup"><span data-stu-id="c70f0-131">When the Lync 2013 client is used to create and manage rooms, the default pool associated with the user’s site is used by the room creation and management experience so that it can route room creation and management operations to that pool.</span></span> <span data-ttu-id="c70f0-132">Dies gilt nur, wenn Sie mehrere beständige Chat Server Pools bereitgestellt haben und die Funktionen zur raumerstellung und-Verwaltung des beständigen Chat Servers verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="c70f0-132">This only applies when you have multiple Persistent Chat Server pools deployed, and want to use the room creation and management features of Persistent Chat Server.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="c70f0-133">Sie können die Funktionen zur raumerstellung und-Verwaltung mithilfe des beständigen Chat-Servers Software Development Kit (SDK) anpassen.</span><span class="sxs-lookup"><span data-stu-id="c70f0-133">You can customize the room creation and management features using the Persistent Chat Server Software Development Kit (SDK).</span></span><BR><span data-ttu-id="c70f0-134">Ausführliche Informationen zum Konfigurieren von SQL Server-Sicherungsdatenbanken für die Disaster Recovery finden Sie unter <A href="lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md">Konfigurieren des beständigen Chat Servers für Hochverfügbarkeits-und Disaster Recovery in lync Server 2013</A> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="c70f0-134">For details about how to configure SQL Server backup databases for disaster recovery, see <A href="lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md">Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013</A> in the Deployment documentation.</span></span>

    
    </div>

8.  <span data-ttu-id="c70f0-135">Definieren Sie den **SQL Store für den beständigen Chat Server-Back-End (wobei Chatroom-Inhalte gespeichert werden)** , indem Sie eine der folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="c70f0-135">Define the **SQL store for the Persistent Chat Server Back End (where chat room content is stored)** by doing one of the following:</span></span>
    
      - <span data-ttu-id="c70f0-136">Wenn Sie eine vorhandene SQL Server-Datenbank verwenden möchten, klicken Sie in der Dropdownliste auf den Namen der SQL Server-Datenbank, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="c70f0-136">To use an existing SQL Server database, in the drop-down list, click the name of the SQL Server database that you want to use.</span></span>
    
      - <span data-ttu-id="c70f0-137">Wenn Sie eine neue SQL Server-Datenbank angeben möchten, klicken Sie auf **neu**, und führen Sie im **neuen SQL Store definieren** die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="c70f0-137">To specify a new SQL Server database, click **New**, and in **Define New SQL Store**, perform the following:</span></span>
    
    <!-- end list -->
    
      - <span data-ttu-id="c70f0-138">Geben Sie im **SQL Server-FQDN** den FQDN des SQL Server an, auf dem Sie die neue SQL Server-Datenbank erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="c70f0-138">In **SQL Server FQDN**, specify the FQDN of the SQL Server on which you want to create the new SQL Server database.</span></span>
    
      - <span data-ttu-id="c70f0-139">Wählen Sie entweder **Standardinstanz** aus, um die Standardinstanz zu verwenden, oder wählen Sie **Benannte Instanz** aus, um eine andere Instanz anzugeben, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="c70f0-139">Either select **Default Instance** to use the default instance or, to specify a different instance, select **Named Instance**, and specify the instance that you want to use.</span></span>

9.  <span data-ttu-id="c70f0-140">Definieren Sie die SQL Server-Kompatibilitätsdatenbank, wenn Sie die Kompatibilität aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="c70f0-140">Define the SQL Server compliance database if you enabled Compliance.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="c70f0-141">Weitere Informationen zum Konfigurieren von SQL Server-Spiegelungen für die Hochverfügbarkeits-Datenbank für die persistente Chat Server-Datenbank und die Datenbank für beständigen Chat Server finden Sie unter <A href="lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md">Konfigurieren des beständigen Chat Servers für die Hochverfügbarkeits-und Disaster Recovery in lync Server 2013</A> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="c70f0-141">For details about how to configure SQL Server mirrors for high availability for the Persistent Chat Server database and the Persistent Chat Server compliance database, see <A href="lync-server-2013-configuring-persistent-chat-server-for-high-availability-and-disaster-recovery.md">Configuring Persistent Chat Server for high availability and disaster recovery in Lync Server 2013</A> in the Deployment documentation.</span></span>

    
    </div>

10. <span data-ttu-id="c70f0-142">Definieren Sie den Dateispeicher.</span><span class="sxs-lookup"><span data-stu-id="c70f0-142">Define the file store.</span></span> <span data-ttu-id="c70f0-143">Bei einem Dateispeicher handelt es sich um einen Ordner, in dem eine Kopie einer Datei, die in das Datei-Repository hochgeladen wurde, gespeichert wird (beispielsweise das Speichern von Dateianlagen, die in einem Chatroom gepostet wurden).</span><span class="sxs-lookup"><span data-stu-id="c70f0-143">A file store is a folder where a copy of any file uploaded to the file repository is stored (for example, storing file attachments posted to a chat room).</span></span> <span data-ttu-id="c70f0-144">Bei einer persistenten Chat Server Topologie mit mehreren Servern muss es sich um einen UNC-Pfad (Universal Naming Convention) handeln. und bei einer Server Topologie mit einem Server für beständigen Chat kann es sich um einen lokalen Dateipfad handeln.</span><span class="sxs-lookup"><span data-stu-id="c70f0-144">In the case of a multiple-server Persistent Chat Server topology, this must be a Universal Naming Convention (UNC) path; and for a single-server Persistent Chat Server topology, it can be a local file path.</span></span>
    
    <span data-ttu-id="c70f0-145">Führen Sie die folgenden Schritte aus, um einen vorhandenen Dateispeicher zu verwenden:</span><span class="sxs-lookup"><span data-stu-id="c70f0-145">To use an existing file store, perform the following steps:</span></span>
    
      - <span data-ttu-id="c70f0-146">Geben Sie im **FQDN des Dateiservers** den FQDN des Dateispeichers an, für den Sie den neuen Dateispeicher erstellen möchten.</span><span class="sxs-lookup"><span data-stu-id="c70f0-146">In **File Server FQDN**, specify the FQDN of the file store on which you want to create the new file store.</span></span>
    
      - <span data-ttu-id="c70f0-147">Geben Sie in **Dateifreigabe** den Dateispeicher an, den Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="c70f0-147">In **File Share**, specify the file store that you want to use.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="c70f0-148">Sie können den Dateispeicher in Topology Builder definieren, bevor Sie den Dateispeicher erstellen, aber Sie müssen den Dateispeicher am definierten Speicherort erstellen, den Sie definieren, bevor Sie die Topologie veröffentlichen.</span><span class="sxs-lookup"><span data-stu-id="c70f0-148">You can define the file store in Topology Builder before you create the file store, but you must create the file store in the defined location you define before you publish the topology.</span></span>

    
    </div>

11. <span data-ttu-id="c70f0-149">Wählen Sie den Front-End-Serverpool aus, der als nächster Hop für diesen beständigen Chat Serverpool verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="c70f0-149">Select the Front End Server pool to be used as a next hop for this Persistent Chat Server pool.</span></span> <span data-ttu-id="c70f0-150">Dies ist der Front-End-Serverpool, der beständige Chat Server Anforderungen an diesen Pool weiterleiten kann.</span><span class="sxs-lookup"><span data-stu-id="c70f0-150">This is the Front End Server pool that will be able to route Persistent Chat Server requests to this pool.</span></span>

12. <span data-ttu-id="c70f0-151">Klicken Sie auf **Fertig stellen**, um die Konfiguration zu speichern.</span><span class="sxs-lookup"><span data-stu-id="c70f0-151">To save the configuration, click **Finish**.</span></span> <span data-ttu-id="c70f0-152">Der Server Pool für beständigen Chat wird im Topologie-Generator mit ihren spezifischen Pooleinstellungen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="c70f0-152">The Persistent Chat Server pool appears in Topology Builder accompanied by your specific pool settings.</span></span>
    
    <span data-ttu-id="c70f0-153">Wenn Sie jetzt Ihre aktualisierte Topologie veröffentlichen möchten, auf der Sie den persistenten Chat Server haben, lesen Sie [Veröffentlichen der aktualisierten Topologie in lync Server 2013](lync-server-2013-publish-the-updated-topology.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="c70f0-153">To now publish your updated topology to which you’ve Persistent Chat Server, see [Publish the updated topology in Lync Server 2013](lync-server-2013-publish-the-updated-topology.md) in the Deployment documentation.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="c70f0-154">Wenn der Topologie-Generator bereits geöffnet ist, können Sie mit Schritt 3 in <A href="lync-server-2013-publish-the-updated-topology.md">Veröffentlichen der aktualisierten Topologie in lync Server 2013</A> fortfahren, um mit der Veröffentlichung ihrer aktualisierten Topologie zu beginnen.</span><span class="sxs-lookup"><span data-stu-id="c70f0-154">With Topology Builder already open, you can proceed to step 3 in <A href="lync-server-2013-publish-the-updated-topology.md">Publish the updated topology in Lync Server 2013</A> to begin publishing your updated topology.</span></span>

    
    <span data-ttu-id="c70f0-155"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c70f0-155"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

