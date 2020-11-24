---
title: 'Lync Server 2013: Veröffentlichen der aktualisierten Topologie'
description: 'Lync Server 2013: Veröffentlichen der aktualisierten Topologie'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Publish the updated topology
ms:assetid: 59455dd1-6a9e-433f-a714-d3636c068100
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204910(v=OCS.15)
ms:contentKeyID: 48184203
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c27cca2eae86eadaf1ff37e2c3520eaec3f86c98
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394559"
---
# <a name="publish-the-updated-topology-in-lync-server-2013"></a><span data-ttu-id="eb72d-103">Veröffentlichen der aktualisierten Topologie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eb72d-103">Publish the updated topology in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eb72d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eb72d-104">

<span> </span></span></span>

<span data-ttu-id="eb72d-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="eb72d-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="eb72d-106">Nachdem Sie Ihre Topologie im Topologie-Generator aktualisiert haben, müssen Sie die Topologie im zentralen Verwaltungsspeicher veröffentlichen, bevor Sie den Server für beständigen Chat Konfigurieren und verwenden können.</span><span class="sxs-lookup"><span data-stu-id="eb72d-106">After updating your topology in Topology Builder, you must publish the topology to the Central Management store before you can configure and use Persistent Chat Server.</span></span> <span data-ttu-id="eb72d-107">Schreibgeschützte Kopien der Daten werden auf alle Server in der Topologie repliziert, sodass diese Server mit der Topologie und anderen Konfigurationsänderungen synchronisiert sind.</span><span class="sxs-lookup"><span data-stu-id="eb72d-107">Read-only copies of the data are replicated to all servers in the topology to keep all servers in sync with topology and other configuration changes.</span></span>

<div>

## <a name="to-publish-an-updated-topology"></a><span data-ttu-id="eb72d-108">So veröffentlichen Sie eine aktualisierte Topologie</span><span class="sxs-lookup"><span data-stu-id="eb72d-108">To publish an updated topology</span></span>

<span data-ttu-id="eb72d-109">Bevor Sie Ihre Topologie veröffentlichen, installieren Sie die Datenbanken für beständigen Chat Server.</span><span class="sxs-lookup"><span data-stu-id="eb72d-109">Before you publish your topology, install the databases for Persistent Chat Server.</span></span> <span data-ttu-id="eb72d-110">Mithilfe des Topologie-Generators können Sie Datenbanken installieren, indem Sie **Aktion** und **Datenbank installieren** auswählen.</span><span class="sxs-lookup"><span data-stu-id="eb72d-110">Use Topology Builder to install databases by selecting **Action** and **Install Database**.</span></span>

1.  <span data-ttu-id="eb72d-111">Melden Sie sich auf einem Computer, auf dem lync Server 2013 ausgeführt wird oder auf dem die lync Server-Verwaltungstools installiert sind, mit einem Konto an, das Mitglied sowohl der Gruppe der **Domänenadministratoren** als auch der **RTCUniversalServerAdmins** -Gruppe ist. und die über die Berechtigung "Vollzugriff" (also lesen, schreiben und ändern) im Dateispeicher für den Dateispeicher für beständigen Chat Server verfügt (damit der Topologie-Generator die erforderlichen DACLs (Discretionary Access Control Lists) oder ein Konto mit entsprechenden Benutzerrechten konfigurieren kann.</span><span class="sxs-lookup"><span data-stu-id="eb72d-111">On a computer that is running Lync Server 2013 or on which the Lync Server administrative tools are installed, log on using an account that is a member of both the **Domain Admins** group and the **RTCUniversalServerAdmins** group, and that has full control permissions (that is, read, write, and modify) on the file store to be used for the Persistent Chat Server file store (so that Topology Builder can configure the required discretionary access control lists (DACLs)), or an account with equivalent user rights.</span></span>

2.  <span data-ttu-id="eb72d-112">Starten Sie den Topologie-Generator.</span><span class="sxs-lookup"><span data-stu-id="eb72d-112">Start Topology Builder.</span></span> <span data-ttu-id="eb72d-113">Wählen Sie **Topologie aus vorhandener Bereitstellung herunterladen** aus, oder **Öffnen Sie die Topologie aus einer lokalen Datei** , wenn Sie Sie lokal gespeichert haben.</span><span class="sxs-lookup"><span data-stu-id="eb72d-113">Select **Download Topology from existing deployment**, or **Open Topology from a local file** if you saved it locally.</span></span>

3.  <span data-ttu-id="eb72d-114">Klicken Sie in der Konsolenstruktur mit der rechten Maustaste auf **lync Server 2013**, und klicken Sie dann auf **Topologie veröffentlichen**.</span><span class="sxs-lookup"><span data-stu-id="eb72d-114">In the console tree, right-click **Lync Server 2013**, and then click **Publish Topology**.</span></span>

4.  <span data-ttu-id="eb72d-115">Klicken Sie auf der Seite **Topologie veröffentlichen** auf **Weiter**.</span><span class="sxs-lookup"><span data-stu-id="eb72d-115">On the **Publish the topology** page, click **Next**.</span></span>

5.  <span data-ttu-id="eb72d-116">Vergewissern Sie sich auf der Seite **Veröffentlichungs-Assistent abgeschlossen**, dass die Topologie erfolgreich veröffentlicht wurde, und klicken Sie anschließend auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="eb72d-116">On the **Publishing wizard complete** page, verify that the topology was successfully published, and then click **Finish**.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="eb72d-117">Nachdem Sie die Topologie veröffentlicht haben, müssen Sie die Unterstützung für beständigen Chat Server konfigurieren, bevor Inhalte archiviert werden können.</span><span class="sxs-lookup"><span data-stu-id="eb72d-117">After publishing the topology, you must configure support for Persistent Chat Server before any content can be archived.</span></span>

    
    <span data-ttu-id="eb72d-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eb72d-118"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

