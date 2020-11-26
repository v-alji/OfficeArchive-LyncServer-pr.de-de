---
title: 'Lync Server 2013: Installieren der Standard Edition-Serverdatenbank'
description: 'Lync Server 2013: Installieren der Standard Edition-Server Datenbank.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Install Standard Edition server database
ms:assetid: 0bd3a804-aad6-48cb-981b-54725af032db
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398167(v=OCS.15)
ms:contentKeyID: 48183385
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0a20d2c01de94ad88960555db78c57c6b79d92f7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427152"
---
# <a name="install-standard-edition-server-database-for-lync-server-2013"></a><span data-ttu-id="b1035-103">Installieren der Standard Edition-Serverdatenbank für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="b1035-103">Install Standard Edition server database for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b1035-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b1035-104">

<span> </span></span></span>

<span data-ttu-id="b1035-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="b1035-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="b1035-106">Wenn Sie einen Standard Edition-Server als einzigen Server in Ihrer Infrastruktur einrichten, der sich von anderen Server Installationen unterscheidet, gibt es im **Bereitstellungs-Assistenten** eine Auswahl, die speziell für das Einrichten des ursprünglichen Servers vorgesehen ist.</span><span class="sxs-lookup"><span data-stu-id="b1035-106">Setting up a Standard Edition server as the only server in your infrastructure that homes users differs from other server installations in that there is a selection in the **Deployment Wizard** specifically for setting up the initial server.</span></span>

<div>

## <a name="to-install-a-standard-edition-server"></a><span data-ttu-id="b1035-107">So installieren Sie einen Standard Edition-Server</span><span class="sxs-lookup"><span data-stu-id="b1035-107">To install a Standard Edition server</span></span>

1.  <span data-ttu-id="b1035-108">Melden Sie sich bei dem Server an, auf dem Sie den Standard Edition-Server als lokalen Administrator oder als Domänen Entsprechung installieren möchten.</span><span class="sxs-lookup"><span data-stu-id="b1035-108">Log on to the server where you are going to install Standard Edition server as a local administrator or a domain equivalent.</span></span>

2.  <span data-ttu-id="b1035-109">Wenn Sie die Active Directory-Domänendienste nicht vorbereitet haben, führen Sie zuerst diese Verfahren aus.</span><span class="sxs-lookup"><span data-stu-id="b1035-109">If you have not prepared Active Directory Domain Services, then first perform those procedures.</span></span> <span data-ttu-id="b1035-110">Ausführliche Informationen finden Sie unter [Vorbereiten von Active Directory-Domänendiensten für lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md).</span><span class="sxs-lookup"><span data-stu-id="b1035-110">For details, see [Preparing Active Directory Domain Services for Lync Server 2013](lync-server-2013-preparing-active-directory-domain-services.md).</span></span>

3.  <span data-ttu-id="b1035-111">Klicken Sie im lync Server-Bereitstellungs-Assistenten auf **First Standard Edition-Server vorbereiten**.</span><span class="sxs-lookup"><span data-stu-id="b1035-111">In the Lync Server Deployment Wizard, click **Prepare first Standard Edition server**.</span></span>

4.  <span data-ttu-id="b1035-112">Klicken Sie auf der Seite **Single Standard Edition-Server vorbereiten** auf **weiter**.</span><span class="sxs-lookup"><span data-stu-id="b1035-112">On the **Prepare single Standard Edition Server** page, click **Next**.</span></span>

5.  <span data-ttu-id="b1035-113">Auf der Seite **Ausführungsbefehle** wird SQL Server 2012 Express als zentraler Verwaltungsspeicher installiert.</span><span class="sxs-lookup"><span data-stu-id="b1035-113">On the **Executing Commands** page, the SQL Server 2012 Express is installed as the Central Management store.</span></span> <span data-ttu-id="b1035-114">Es werden erforderliche Firewallregeln erstellt.</span><span class="sxs-lookup"><span data-stu-id="b1035-114">Necessary firewall rules are created.</span></span> <span data-ttu-id="b1035-115">Wenn die Installation der Datenbank und der erforderlichen Software abgeschlossen ist, klicken Sie auf **Fertig stellen**.</span><span class="sxs-lookup"><span data-stu-id="b1035-115">When the installation of the database and prerequisite software is completed, click **Finish**.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="b1035-116">Die anfängliche Installation kann einige Zeit in Anspruch nehmen, ohne dass die Anzeige des Befehlsausgabe Zusammenfassungsbildschirms sichtbar wird.</span><span class="sxs-lookup"><span data-stu-id="b1035-116">The initial installation may take some time with no visible updates to the command output summary screen.</span></span> <span data-ttu-id="b1035-117">Dies ist auf die Installation von SQL Server Express zurückzuführen.</span><span class="sxs-lookup"><span data-stu-id="b1035-117">This is due to the installation of the SQL Server Express.</span></span> <span data-ttu-id="b1035-118">Wenn Sie die Installation der Datenbank überwachen müssen, verwenden Sie den Task-Manager, um das Setup zu überwachen.</span><span class="sxs-lookup"><span data-stu-id="b1035-118">If you need to monitor the installation of the database, use Task Manager to monitor the setup.</span></span>

    
    </div>

6.  <span data-ttu-id="b1035-119">Klicken Sie auf der Seite mit dem lync Server-Bereitstellungs-Assistenten auf **Topologie-Generator installieren** , wenn Sie die Verwaltungstools zuvor noch nicht installiert haben.</span><span class="sxs-lookup"><span data-stu-id="b1035-119">On the Lync Server Deployment Wizard page, click **Install Topology Builder** if you have not previously installed the administrative tools.</span></span> <span data-ttu-id="b1035-120">Ausführliche Informationen finden Sie unter [Installieren von lync Server 2013-Verwaltungstools](lync-server-2013-install-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="b1035-120">For details, see [Install Lync Server 2013 administrative tools](lync-server-2013-install-lync-server-administrative-tools.md).</span></span>

7.  <span data-ttu-id="b1035-121">Vergewissern Sie sich, dass neben "Active Directory vorbereiten", "Vorbereiten des ersten Standard Edition-Servers" und "Installieren des Topologie-Generators" grüne Häkchen vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="b1035-121">Confirm that there are green check marks next to “Prepare Active Directory,” “Prepare first Standard Edition server,” and “Install Topology Builder.”</span></span>

<span data-ttu-id="b1035-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b1035-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

