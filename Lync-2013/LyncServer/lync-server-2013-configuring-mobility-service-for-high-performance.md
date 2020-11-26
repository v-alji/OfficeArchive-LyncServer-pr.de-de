---
title: 'Lync Server 2013: Konfigurieren des mobilitätsdiensts für eine höhere Leistung'
description: 'Lync Server 2013: Konfigurieren des mobilitätsdiensts für eine höhere Leistung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Mobility Service for high performance
ms:assetid: c2b8aadb-cffb-49f0-ba7a-e8541a1ff475
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690042(v=OCS.15)
ms:contentKeyID: 48185332
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4732d9f6a92c383a105a6f0d7162c9b6c798de24
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432884"
---
# <a name="configuring-mobility-service-for-high-performance-in-lync-server-2013"></a><span data-ttu-id="854da-103">Konfigurieren des mobilitätsdiensts für die Höchstleistung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="854da-103">Configuring Mobility Service for high performance in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="854da-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="854da-104">

<span> </span></span></span>

<span data-ttu-id="854da-105">_**Letztes Änderungsdatum des Themas:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="854da-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="854da-106">Dieses Thema bezieht sich nur auf den lync Server 2013 Mobility Service (MCX) und gilt nicht für Unified Communications Web API (UCWA), wie Sie in den kumulativen Updates für lync Server 2013: Februar 2013 bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="854da-106">This topic applies only to the Lync Server 2013 Mobility Service (Mcx), and does not apply to Unified Communications Web API (UCWA), as delivered in the Cumulative Updates for Lync Server 2013: February 2013.</span></span>



</div>

<span data-ttu-id="854da-107">Wenn Sie den Mobilitätsdienst (MCX) auf Internet Informationsdienste (IIS) 7,5 installieren, konfiguriert das Mobilitätsdienst-Installationsprogramm einige Leistungseinstellungen auf dem Front-End-Server.</span><span class="sxs-lookup"><span data-stu-id="854da-107">When you install the Mobility Service (Mcx) on Internet Information Services (IIS) 7.5, the Mobility Service installer configures some performance settings on the Front End Server.</span></span> <span data-ttu-id="854da-108">Es wird empfohlen, IIS 7.5 für die Mobilität zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="854da-108">We recommend that you use IIS 7.5 for mobility.</span></span> <span data-ttu-id="854da-109">Diese Einstellungen wirken sich auf die maximale Anzahl gleichzeitiger Benutzeranforderungen und die maximale Anzahl von Threads aus, die für den Mobilitätsdienst zulässig sind.</span><span class="sxs-lookup"><span data-stu-id="854da-109">The settings affect the maximum number of concurrent user requests and the maximum number of threads that are allowed for the Mobility Service.</span></span>

<span data-ttu-id="854da-110">Die Leistungseinstellungen lauten wie folgt:</span><span class="sxs-lookup"><span data-stu-id="854da-110">Here are the performance settings:</span></span>

<div>

## <a name="settings-for-mcx-on-iis-75"></a><span data-ttu-id="854da-111">Einstellungen für Mcx auf IIS 7.5</span><span class="sxs-lookup"><span data-stu-id="854da-111">Settings for Mcx on IIS 7.5</span></span>

1.  <span data-ttu-id="854da-112">**maxConcurrentThreadsPerCPU** ist auf null (0) gesetzt.</span><span class="sxs-lookup"><span data-stu-id="854da-112">**maxConcurrentThreadsPerCPU** is set to zero (0).</span></span>

2.  <span data-ttu-id="854da-113">**maxConcurrentRequestsPerCPU** ist auf null (0) gesetzt.</span><span class="sxs-lookup"><span data-stu-id="854da-113">**maxConcurrentRequestsPerCPU** is set to zero (0).</span></span>

3.  <span data-ttu-id="854da-114">Das ASP.NET-Prozessmodell ist auf AutoConfig (nur für IIS 7.5) gesetzt.</span><span class="sxs-lookup"><span data-stu-id="854da-114">ASP.NET process model is set to AutoConfig (for IIS 7.5 only).</span></span>

4.  <span data-ttu-id="854da-115">Das Limit für die HTTP.SYS-Warteschlange ist standardmäßig auf 1.000 gesetzt.</span><span class="sxs-lookup"><span data-stu-id="854da-115">HTTP.sys queue limit is set to 1,000 (by default).</span></span>

<span data-ttu-id="854da-116"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="854da-116"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

