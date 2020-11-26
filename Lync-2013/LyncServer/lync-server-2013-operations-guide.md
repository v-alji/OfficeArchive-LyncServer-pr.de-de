---
title: 'Lync Server 2013: Betriebshandbuch'
description: 'Lync Server 2013: Betriebshandbuch'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Operations Guide
ms:assetid: dcb9ddff-6fe3-4077-a2e3-0ba64f65e264
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn720467(v=OCS.15)
ms:contentKeyID: 63969658
ms.date: 01/27/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 85e562b96e87f54529a9e2ce077a0a82574020c1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445278"
---
# <a name="operations-guide-for-lync-server-2013"></a><span data-ttu-id="2b978-103">Operations Guide for Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b978-103">Operations Guide for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2b978-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2b978-104">

<span> </span></span></span>

<span data-ttu-id="2b978-105">_**Letztes Änderungsdatum des Themas:** 2014-08-18_</span><span class="sxs-lookup"><span data-stu-id="2b978-105">_**Topic Last Modified:** 2014-08-18_</span></span>

<span data-ttu-id="2b978-106">In diesem Dokument werden die operativen Prozesse, Aufgaben und Tools beschrieben, die für die Verwaltung einer Microsoft lync Server 2013-Kommunikationssoftware Umgebung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="2b978-106">This document describes the operational processes, tasks, and tools that are required for you to maintain a Microsoft Lync Server 2013 communications software environment.</span></span> <span data-ttu-id="2b978-107">Es wird erläutert, wie lync Server 2013 entsprechend dem Microsoft Operations Framework (MOF)-Modell verwaltet wird, und es wird Ihnen beim Entwerfen einer effizienten Betriebsverwaltungsumgebung helfen, die das Implementieren von Zeitplänen, Prozessen und Verfahren zum aufrecht erhalten einer effizienten Arbeitsumgebung umfasst.</span><span class="sxs-lookup"><span data-stu-id="2b978-107">It explains how to manage Lync Server 2013 according to the Microsoft Operations Framework (MOF) model and it will help you design an efficient operational management environment, which includes implementing schedules, processes and procedures to maintain an efficient working environment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2b978-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="2b978-108">In This Section</span></span>

<span data-ttu-id="2b978-109">Die folgenden Abschnitte sind enthalten:</span><span class="sxs-lookup"><span data-stu-id="2b978-109">The following sections are included:</span></span>

  - [<span data-ttu-id="2b978-110">Bewährte Methoden für lync Server 2013-Umgebungen</span><span class="sxs-lookup"><span data-stu-id="2b978-110">Best practices for Lync Server 2013 environments</span></span>](lync-server-2013-best-practices-for-lync-server-environments.md)

  - [<span data-ttu-id="2b978-111">Tägliche Aufgaben in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b978-111">Daily tasks in Lync Server 2013</span></span>](lync-server-2013-daily-tasks.md)

  - [<span data-ttu-id="2b978-112">Wöchentliche Aufgaben in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b978-112">Weekly tasks in Lync Server 2013</span></span>](lync-server-2013-weekly-tasks.md)

  - [<span data-ttu-id="2b978-113">Monatliche Aufgaben in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b978-113">Monthly tasks in Lync Server 2013</span></span>](lync-server-2013-monthly-tasks.md)

  - [<span data-ttu-id="2b978-114">Erforderliche Aufgaben in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b978-114">As-needed tasks in Lync Server 2013</span></span>](lync-server-2013-as-needed-tasks.md)

  - [<span data-ttu-id="2b978-115">Vorgangs Checklisten für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b978-115">Operations checklists for Lync Server 2013</span></span>](lync-server-2013-operations-checklists.md)

  - [<span data-ttu-id="2b978-116">Überwachen von lync Server 2013 mit System Center Operations Manager</span><span class="sxs-lookup"><span data-stu-id="2b978-116">Monitoring Lync Server 2013 with System Center Operations Manager</span></span>](lync-server-2013-monitoring-lync-server-with-system-center-operations-manager.md)

  - [<span data-ttu-id="2b978-117">Betriebs Abhängigkeiten in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b978-117">Operational dependencies in Lync Server 2013</span></span>](lync-server-2013-operational-dependencies.md)

  - [<span data-ttu-id="2b978-118">Problembehandlung und wichtige Integritätsindikatoren in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b978-118">Troubleshooting and Key Health Indicators in Lync Server 2013</span></span>](lync-server-2013-troubleshooting-and-key-health-indicators.md)

<span data-ttu-id="2b978-119">Es wird davon ausgegangen, dass Ihre Microsoft lync Server 2013-Bereitstellung abgeschlossen ist.</span><span class="sxs-lookup"><span data-stu-id="2b978-119">It is assumed that your Microsoft Lync Server 2013 deployment is completed.</span></span> <span data-ttu-id="2b978-120">Wenn dies nicht der Fall ist, lesen Sie den Planungs-und Bereitstellungs Inhalt für Microsoft lync Server 2013, bevor Sie fortfahren.</span><span class="sxs-lookup"><span data-stu-id="2b978-120">If this is not the case, refer to the planning and deployment content for Microsoft Lync Server 2013 before you continue.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="2b978-121">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="2b978-121">See Also</span></span>


[<span data-ttu-id="2b978-122">Erste Schritte in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b978-122">Getting started with Lync Server 2013</span></span>](lync-server-2013-getting-started.md)  
[<span data-ttu-id="2b978-123">Planen von lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b978-123">Planning for Lync Server 2013</span></span>](lync-server-2013-planning.md)  
[<span data-ttu-id="2b978-124">Bereitstellung von lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b978-124">Deployment of Lync Server 2013</span></span>](lync-server-2013-deployment.md)  
[<span data-ttu-id="2b978-125">Verwaltungsshell für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2b978-125">Lync Server 2013 Management Shell</span></span>](lync-server-2013-lync-server-management-shell.md)  
  

<span data-ttu-id="2b978-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2b978-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

