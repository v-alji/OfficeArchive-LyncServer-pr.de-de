---
title: 'Lync Server 2013: Ausführen eines Failbacks für einen Pool'
description: 'Lync Server 2013: Fehler beim Zurücksetzen eines Pools.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Failing back a pool
ms:assetid: 6232b644-ef57-4c9c-abec-14ff8ffc9fe7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204945(v=OCS.15)
ms:contentKeyID: 48184289
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1c1fc0ea4514d2f951dd936521590d47b809db38
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49428328"
---
# <a name="failing-back-a-pool-in-lync-server-2013"></a><span data-ttu-id="475ae-103">Ausführen eines Failbacks für einen Pool in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="475ae-103">Failing back a pool in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="475ae-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="475ae-104">

<span> </span></span></span>

<span data-ttu-id="475ae-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="475ae-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="475ae-106">Nachdem der Pool, der das Desaster erlebt hat, wieder online ist (also pool1 in diesem Beispiel), führen Sie die folgenden Schritte aus, um die Bereitstellung auf normalen Arbeitsstatus wiederherzustellen.</span><span class="sxs-lookup"><span data-stu-id="475ae-106">After the pool that experienced the disaster is back online (that is, Pool1 in this example), take the following steps to restore your deployment to regular working status.</span></span>

<span data-ttu-id="475ae-107">Beachten Sie, dass der Failback-Vorgang mehrere Minuten in Anspruch nimmt.</span><span class="sxs-lookup"><span data-stu-id="475ae-107">Note that the failback process takes several minute to complete.</span></span>  <span data-ttu-id="475ae-108">Zur Orientierung: Erwartungsgemäß dauert dies bei einem Pool mit 20.000 Benutzern bis zu 60 Minuten.</span><span class="sxs-lookup"><span data-stu-id="475ae-108">For reference, it is expected to take up to 60 minutes for a pool of 20,000 users.</span></span>

1.  <span data-ttu-id="475ae-109">Führen Sie einen Failback für die Benutzer durch, die sich ursprünglich in pool1 begeben haben, und Sie haben ein Failover auf Pool2 durchgeführt, indem Sie das folgende Cmdlet eingegeben haben:</span><span class="sxs-lookup"><span data-stu-id="475ae-109">Fail back the users who were originally homed in Pool1 and have been failed over to Pool2 by typing the following cmdlet:</span></span>
    
        Invoke-CsPoolFailback -PoolFQDN <Pool1 FQDN> -Verbose

<span data-ttu-id="475ae-110">Es sind keine weiteren Schritte erforderlich.</span><span class="sxs-lookup"><span data-stu-id="475ae-110">No other steps are necessary.</span></span> <span data-ttu-id="475ae-111">Wenn Sie einen Fehler über den zentralen Verwaltungs Server ausgeführt haben, können Sie ihn in Pool2 belassen.</span><span class="sxs-lookup"><span data-stu-id="475ae-111">If you failed over the Central Management Server, you can leave it in Pool2.</span></span>

<span data-ttu-id="475ae-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="475ae-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

