---
title: 'Lync Server 2013: Konfigurieren von DNS-Hosteinträgen'
description: 'Lync Server 2013: Konfigurieren von DNS-Host Einträgen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS Host records
ms:assetid: 78a1afcf-41c8-4da5-8740-c6570c19078c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398593(v=OCS.15)
ms:contentKeyID: 48184577
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7fd403402d0d2f089d7fc92a62296a56df0cf2e6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434039"
---
# <a name="configure-dns-host-records-for-lync-server-2013"></a><span data-ttu-id="4eb4a-103">Konfigurieren von DNS-Hosteinträgen für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4eb4a-103">Configure DNS Host records for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4eb4a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4eb4a-104">

<span> </span></span></span>

<span data-ttu-id="4eb4a-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="4eb4a-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="4eb4a-106">Um dieses Verfahren erfolgreich durchführen zu können, sollten Sie mindestens als Mitglied der Gruppe Domänen-Admins oder als Mitglied der DnsAdmins-Gruppe bei dem Server oder der Domäne angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="4eb4a-106">To successfully complete this procedure, you should be logged on to the server or domain at minimum as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<div>

## <a name="to-configure-dns-host-a-records"></a><span data-ttu-id="4eb4a-107">So konfigurieren Sie DNS-Host A-Einträge</span><span class="sxs-lookup"><span data-stu-id="4eb4a-107">To configure DNS Host A records</span></span>

1.  <span data-ttu-id="4eb4a-108">Klicken Sie auf dem DNS-Server (Domain Name System) auf **Start**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **DNS**.</span><span class="sxs-lookup"><span data-stu-id="4eb4a-108">On the Domain Name System (DNS) server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="4eb4a-109">Erweitern Sie in der Konsolenstruktur für Ihre Domäne **Forward-Lookupzonen**, und klicken Sie dann mit der rechten Maustaste auf die Domäne, in der lync Server 2013 installiert wird.</span><span class="sxs-lookup"><span data-stu-id="4eb4a-109">In the console tree for your domain, expand **Forward Lookup Zones**, and then right-click the domain in which Lync Server 2013 will be installed.</span></span>

3.  <span data-ttu-id="4eb4a-110">Klicken Sie auf **neuer Host (A oder AAAA)**.</span><span class="sxs-lookup"><span data-stu-id="4eb4a-110">Click **New Host (A or AAAA)**.</span></span>

4.  <span data-ttu-id="4eb4a-111">Klicken Sie auf **Name**, geben Sie den Hostnamen für den Pool ein (der Domänen Name wird aus der Zone übernommen, in der der Datensatz definiert ist, und muss nicht als Teil des A-Eintrags eingegeben werden).</span><span class="sxs-lookup"><span data-stu-id="4eb4a-111">Click **Name**, type the host name for the pool (the domain name is assumed from the zone that the record is defined in and does not need to be entered as part of the A record).</span></span>

5.  <span data-ttu-id="4eb4a-112">Klicken Sie auf **IP-Adresse**, und geben Sie die virtuelle IP (VIP) des Load Balancer für den Front-End-Pool ein.</span><span class="sxs-lookup"><span data-stu-id="4eb4a-112">Click **IP Address**, type the virtual IP (VIP) of the load balancer for the Front End pool.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="4eb4a-113">In Bereitstellungen, die einen Director-Pool verwenden, sollten die Host (a)-Einträge für die einfachen URLs auf den VIP des Director Load Balancer verweisen.</span><span class="sxs-lookup"><span data-stu-id="4eb4a-113">In deployments that use a Director pool, the host (A) records for the simple URLs should point to the VIP of the Director load balancer.</span></span>

    
    </div>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4eb4a-114">Wenn Sie nur einen Enterprise Edition-Server oder-Director bereitstellen, der mit der Topologie ohne Load Balancer verbunden ist, oder wenn Sie einen Standard Edition-Server bereitstellen, geben Sie die IP-Adresse des Enterprise Edition-Servers, Standard Edition-Servers oder Directors ein.</span><span class="sxs-lookup"><span data-stu-id="4eb4a-114">If you deploy only one Enterprise Edition server or Director that is connected to the topology without a load balancer, or if you deploy a Standard Edition server, type the IP address of the Enterprise Edition server, Standard Edition server, or Director.</span></span> <span data-ttu-id="4eb4a-115">Ein Lastenausgleichsmodul ist erforderlich, wenn Sie mehr als einen Enterprise Edition-Server oder-Director in einem Pool bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4eb4a-115">A load balancer is required if you deploy more than one Enterprise Edition server or Director in a pool.</span></span> <span data-ttu-id="4eb4a-116">Load-Balancer werden nicht mit Standard Edition-Servern verwendet.</span><span class="sxs-lookup"><span data-stu-id="4eb4a-116">Load balancers are not used with Standard Edition servers.</span></span>

    
    </div>

6.  <span data-ttu-id="4eb4a-117">Klicken Sie auf **Host hinzufügen**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="4eb4a-117">Click **Add Host**, and then click **OK**.</span></span>

7.  <span data-ttu-id="4eb4a-118">Wiederholen Sie die Schritte 4 und 5, um einen zusätzlichen A-Eintrag zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="4eb4a-118">To create an additional A record, repeat steps 4 and 5.</span></span>

8.  <span data-ttu-id="4eb4a-119">Wenn Sie alle benötigten A-Einträge erstellt haben, klicken Sie auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="4eb4a-119">When you are finished creating all the A records that you need, click **Done**.</span></span>

<span data-ttu-id="4eb4a-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4eb4a-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

