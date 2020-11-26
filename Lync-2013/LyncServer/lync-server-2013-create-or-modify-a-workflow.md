---
title: 'Lync Server 2013: Erstellen oder Ändern eines Workflows'
description: 'Lync Server 2013: Erstellen oder Ändern eines Workflows'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create or modify a workflow
ms:assetid: 5ac1c0f3-e82f-40ca-b972-91950e38c05b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520997(v=OCS.15)
ms:contentKeyID: 48184225
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 053b80e313e497313e613a5f8b16bd5beeabf7ac
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431729"
---
# <a name="create-or-modify-a-workflow-in-lync-server-2013"></a><span data-ttu-id="ba178-103">Erstellen oder Ändern eines Workflows in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba178-103">Create or modify a workflow in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ba178-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ba178-104">

<span> </span></span></span>

<span data-ttu-id="ba178-105">_**Letztes Änderungsdatum des Themas:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="ba178-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="ba178-106">Lync Server 2013 unterstützt zwei Arten von Workflows: Hunt Group und Interactive Voice Response (IVR).</span><span class="sxs-lookup"><span data-stu-id="ba178-106">Lync Server 2013 supports two types of workflows: hunt group and interactive voice response (IVR).</span></span> <span data-ttu-id="ba178-107">Wenn Sie einen Workflow erstellen, verwenden Sie das Reaktionsgruppen-Konfigurations Tool, um die zu verwendende Warteschlange und andere Einstellungen anzugeben, wie etwa eine Willkommensnachricht, Musik in Wartestellung, Geschäftszeiten und Fragen, die die Antwortgruppen Anwendung vom Anrufer fordert.</span><span class="sxs-lookup"><span data-stu-id="ba178-107">When you create a workflow, you use the Response Group Configuration Tool to specify the queue to use and other settings, such as a welcome message, music on hold, business hours, and questions that the Response Group application asks the caller.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ba178-108">Vor dem Erstellen eines Workflows müssen Sie zuerst Agent-Gruppen und Warteschleifen erstellen, die vom Workflow verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="ba178-108">You must create agent groups and queues before you create a workflow that uses them.</span></span> <span data-ttu-id="ba178-109">Wenn Sie vordefinierte Geschäftszeiten und Feiertage erstellen möchten, die Sie für mehrere Workflows verwenden können, müssen Sie auch diese Stunden und Feiertage definieren, bevor Sie einen Workflow erstellen, der Sie verwendet.</span><span class="sxs-lookup"><span data-stu-id="ba178-109">If you want to create predefined business hours and holidays that you can use for multiple workflows, you must also define these hours and holidays before you create a workflow that uses them.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="ba178-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="ba178-110">In This Section</span></span>

  - [<span data-ttu-id="ba178-111">Erstellen oder Ändern eines Sammel Ansuchen-Workflows in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba178-111">Create or modify a hunt group workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-hunt-group-workflow.md)

  - [<span data-ttu-id="ba178-112">Erstellen oder Ändern eines interaktiven Workflows in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba178-112">Create or modify an interactive workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-interactive-workflow.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ba178-113">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ba178-113">See Also</span></span>


[<span data-ttu-id="ba178-114">Erstellen oder Ändern einer Agentengruppe in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba178-114">Create or modify an agent group in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-agent-group.md)  
[<span data-ttu-id="ba178-115">Erstellen oder Ändern einer Warteschlange in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba178-115">Create or modify a queue in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-queue.md)  
[<span data-ttu-id="ba178-116">Optional Definieren von Feiertagssätzen für Reaktionsgruppen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba178-116">(Optional) Define Response Group holiday sets in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-holiday-sets.md)  


[<span data-ttu-id="ba178-117">Optional Definieren der Geschäftszeiten der Reaktionsgruppe in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ba178-117">(Optional) Define Response Group business hours in Lync Server 2013</span></span>](lync-server-2013-optional-define-response-group-business-hours.md)  
  

<span data-ttu-id="ba178-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ba178-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

