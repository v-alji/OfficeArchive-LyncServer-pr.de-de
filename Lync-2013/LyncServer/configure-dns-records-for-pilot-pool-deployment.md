---
title: Konfigurieren von DNS-Einträgen für die Pilotpoolbereitstellung
description: Konfigurieren von DNS-Einträgen für die Bereitstellung von pilotpools
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
audience: Admin
f1.keywords:
- NOCSH
TOCTitle: Configure DNS records for pilot pool deployment
ms:assetid: eb421bad-4bf1-4837-a077-7795094692d9
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721921(v=OCS.15)
ms:contentKeyID: 49733855
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1e41e163432ba910f6d083cc508e8ad8c9f2006d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394442"
---
# <a name="configure-dns-records-for-pilot-pool-deployment"></a><span data-ttu-id="d8bef-103">Konfigurieren von DNS-Einträgen für die Pilotpoolbereitstellung</span><span class="sxs-lookup"><span data-stu-id="d8bef-103">Configure DNS records for pilot pool deployment</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d8bef-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d8bef-104">

<span> </span></span></span>

<span data-ttu-id="d8bef-105">_**Letztes Änderungsdatum des Themas:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="d8bef-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="d8bef-106">Vor der Bereitstellung des lync Server 2013-pilotpools müssen Sie den DNS-Host einen Eintrag für den Pilot Pool aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="d8bef-106">Prior to deploying the Lync Server 2013 pilot pool, you must update the DNS Host A entries for the pilot pool.</span></span> <span data-ttu-id="d8bef-107">Um dieses Verfahren erfolgreich durchführen zu können, sollten Sie als Mitglied der Gruppe Domänenadministratoren oder als Mitglied der DnsAdmins-Gruppe am Server oder in der Domäne angemeldet sein.</span><span class="sxs-lookup"><span data-stu-id="d8bef-107">To successfully complete this procedure, you should be logged on to the server or domain as a member of the Domain Admins group or a member of the DnsAdmins group.</span></span>

<span data-ttu-id="d8bef-108">**So konfigurieren Sie DNS-Host A-Einträge**</span><span class="sxs-lookup"><span data-stu-id="d8bef-108">**To configure DNS Host A records**</span></span>

1.  <span data-ttu-id="d8bef-109">Klicken Sie auf dem DNS-Server (Domain Name System) auf **Start**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **DNS**.</span><span class="sxs-lookup"><span data-stu-id="d8bef-109">On the Domain Name System (DNS) server, click **Start**, click **Administrative Tools**, and then click **DNS**.</span></span>

2.  <span data-ttu-id="d8bef-110">Erweitern Sie in der Konsolenstruktur für Ihre Domäne **Forward-Lookupzonen**, und klicken Sie dann mit der rechten Maustaste auf die Domäne, in der lync Server 2013 installiert wird.</span><span class="sxs-lookup"><span data-stu-id="d8bef-110">In the console tree for your domain, expand **Forward Lookup Zones**, and then right-click the domain in which Lync Server 2013 will be installed.</span></span>

3.  <span data-ttu-id="d8bef-111">Klicken Sie auf **neuer Host (A oder AAAA)**.</span><span class="sxs-lookup"><span data-stu-id="d8bef-111">Click **New Host (A or AAAA)**.</span></span>

4.  <span data-ttu-id="d8bef-112">Klicken Sie auf **Name**, geben Sie den Hostnamen für den lync Server 2013-Pool ein (der Domänen Name wird aus der Zone übernommen, in der der Datensatz definiert ist, und muss nicht als Teil des A-Eintrags eingegeben werden).</span><span class="sxs-lookup"><span data-stu-id="d8bef-112">Click **Name**, type the host name for the Lync Server 2013 pool (the domain name is assumed from the zone that the record is defined in and does not need to be entered as part of the A record).</span></span>

5.  <span data-ttu-id="d8bef-113">Klicken Sie auf **IP-Adresse**, und geben Sie die IP-Adresse für den Front-End-Pool ein.</span><span class="sxs-lookup"><span data-stu-id="d8bef-113">Click **IP Address**, type the IP address for the Front End pool.</span></span>

6.  <span data-ttu-id="d8bef-114">Klicken Sie auf **Host hinzufügen**, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="d8bef-114">Click **Add Host**, and then click **OK**.</span></span>

7.  <span data-ttu-id="d8bef-115">Wenn Sie fertig sind, klicken Sie auf **Fertig**.</span><span class="sxs-lookup"><span data-stu-id="d8bef-115">When you are finished, click **Done**.</span></span>

<span data-ttu-id="d8bef-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d8bef-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

