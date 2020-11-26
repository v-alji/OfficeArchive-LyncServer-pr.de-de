---
title: 'Phase 8: Außerbetriebsetzen der Legacypools'
description: 'Phase 8: decommission Legacy-Pools.'
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: 'Phase 8: Decommission legacy pools'
ms:assetid: 1c68e5d8-fb5f-45e6-b6e3-27f5e830c966
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204724(v=OCS.15)
ms:contentKeyID: 48183557
ms.date: 12/29/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a6414fe97b54ed1b487ff722c6b02d4904443841
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446086"
---
# <a name="phase-8-decommission-legacy-pools"></a><span data-ttu-id="f3f61-103">Phase 8: Außerbetriebsetzen der Legacypools</span><span class="sxs-lookup"><span data-stu-id="f3f61-103">Phase 8: Decommission legacy pools</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f3f61-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f3f61-104">

<span> </span></span></span>

<span data-ttu-id="f3f61-105">_**Letztes Änderungsdatum des Themas:** 2016-12-08_</span><span class="sxs-lookup"><span data-stu-id="f3f61-105">_**Topic Last Modified:** 2016-12-08_</span></span>

<span data-ttu-id="f3f61-106">Das folgende Thema enthält Anleitungen zum Aktualisieren von DNS-Einträgen, zum Verschieben des Inhalts Verwaltungsservers, zur Außerbetriebnahme von Pools sowie zum Deaktivieren und Entfernen von Servern und Pools aus einer Legacy Bereitstellung von lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="f3f61-106">The following topic provides guidance in updating DNS entries, moving the Content Management Server, decommissioning pools, and deactivating and removing servers and pools from a legacy deployment of Lync Server 2010.</span></span> <span data-ttu-id="f3f61-107">Nicht alle in diesem Abschnitt aufgelisteten Verfahren sind erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f3f61-107">Not all of the procedures listed in this section are required.</span></span> <span data-ttu-id="f3f61-108">Lesen Sie die Dokumentation, und legen Sie fest, welches Verfahren für die Außerbetriebnahme verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="f3f61-108">Read the documentation and determine which decommissioning procedure to use.</span></span>

<span data-ttu-id="f3f61-109">Umfassende Informationen zum Entfernen von lync Server 2010-Servern und-Serverrollen sowie eine Schritt-für-Schritt-Anleitung zur Außerbetriebnahme einer lync Server 2010-Bereitstellung finden Sie unter "Deinstallieren von Microsoft lync Server 2010 und Entfernen von Serverrollen", die unter heruntergeladen werden können [https://go.microsoft.com/fwlink/p/?linkId=246227](https://go.microsoft.com/fwlink/p/?linkid=246227) .</span><span class="sxs-lookup"><span data-stu-id="f3f61-109">For exhaustive coverage of removing Lync Server 2010 servers and server roles, and a step-by-step guide to decommissioning a Lync Server 2010 deployment, see "Uninstalling Microsoft Lync Server 2010 and Removing Server Roles," which can be downloaded at [https://go.microsoft.com/fwlink/p/?linkId=246227](https://go.microsoft.com/fwlink/p/?linkid=246227).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="f3f61-110">Informationen zum Migrieren und Aktualisieren von Microsoft Unified Communications Managed API-Anwendungen (UCMA) vor der Außerbetriebnahme ihrer Legacyumgebung finden Sie unter <A href="https://go.microsoft.com/fwlink/p/?linkid=269555">https://go.microsoft.com/fwlink/p/?LinkId=269555</A></span><span class="sxs-lookup"><span data-stu-id="f3f61-110">For information on migrating and upgrading Microsoft Unified Communications Managed API (UCMA) applications, prior to decommissioning your legacy environment, see <A href="https://go.microsoft.com/fwlink/p/?linkid=269555">https://go.microsoft.com/fwlink/p/?LinkId=269555</A></span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="f3f61-111">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="f3f61-111">In This Section</span></span>

  - <span></span>  
    [<span data-ttu-id="f3f61-112">Aktualisieren von DNS SRV-Einträgen</span><span class="sxs-lookup"><span data-stu-id="f3f61-112">Update DNS SRV records</span></span>](update-dns-srv-records.md)

  - <span></span>  
    [<span data-ttu-id="f3f61-113">Verschieben des zentralen Verwaltungsservers mit lync Server 2010 auf lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f3f61-113">Move the Lync Server 2010 Central Management Server to Lync Server 2013</span></span>](move-the-lync-server-2010-central-management-server-to-lync-server-2013.md)

  - <span></span>  
    [<span data-ttu-id="f3f61-114">Verschieben von Konferenzverzeichnissen</span><span class="sxs-lookup"><span data-stu-id="f3f61-114">Move Conference Directories</span></span>](move-lync-server-2010-conference-directories-to-lync-server-2013.md)

  - <span></span>  
    [<span data-ttu-id="f3f61-115">Entfernen der Zuordnung des Archivierungsservers</span><span class="sxs-lookup"><span data-stu-id="f3f61-115">Remove the Archiving server association</span></span>](remove-the-archiving-server-association.md)

  - <span></span>  
    [<span data-ttu-id="f3f61-116">Entfernen der Zuordnung der Monitoring Server</span><span class="sxs-lookup"><span data-stu-id="f3f61-116">Remove the Monitoring server association</span></span>](remove-the-monitoring-server-association.md)

  - <span></span>  
    [<span data-ttu-id="f3f61-117">Entfernen des Enterprise Edition-Front-End-Servers oder des Standard Edition-Front-End-Servers</span><span class="sxs-lookup"><span data-stu-id="f3f61-117">Remove the Enterprise Edition Front End Server or Standard Edition Front End Server</span></span>](remove-the-enterprise-edition-front-end-server-or-standard-edition-front-end-server.md)

  - <span></span>  
    [<span data-ttu-id="f3f61-118">Entfernen von SQL Server-Instanzen und -Datenbanken auf dem Back-End-Server</span><span class="sxs-lookup"><span data-stu-id="f3f61-118">Remove SQL Server instances and databases on the Back End Server</span></span>](remove-sql-server-instances-and-databases-on-the-back-end-server.md)

<span data-ttu-id="f3f61-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f3f61-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

