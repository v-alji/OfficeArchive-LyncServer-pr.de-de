---
title: 'Lync Server 2013: Erstellen von Workflows für Reaktionsgruppen'
description: 'Lync Server 2013: Erstellen von Reaktionsgruppen-Workflows'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create Response Group workflows
ms:assetid: 41272258-728d-42bd-b4d4-2a499734c720
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425918(v=OCS.15)
ms:contentKeyID: 48183954
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7082295eeca45c4dac76d68ef54b5c32fafb25d7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431589"
---
# <a name="create-response-group-workflows-in-lync-server-2013"></a><span data-ttu-id="2ad16-103">Erstellen von Workflows für Reaktionsgruppen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ad16-103">Create Response Group workflows in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2ad16-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2ad16-104">

<span> </span></span></span>

<span data-ttu-id="2ad16-105">_**Letztes Änderungsdatum des Themas:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="2ad16-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="2ad16-p101">Ein Workflow definiert, wie mit einem Anruf ab dem Läuten des Telefons bis zur Annahme des Anrufs verfahren wird. Der Workflow gibt die Warteschleife zum Halten des Anrufs an und legt die Routingmethode für Sammelanschlüsse oder die Fragen und Antworten für interaktive Reaktionsgruppen fest. Ein Workflow definiert außerdem Einstellungen wie die Willkommensnachricht, Wartemusik, Geschäftszeiten und Feiertage.</span><span class="sxs-lookup"><span data-stu-id="2ad16-p101">A workflow defines the behavior of a call from the time that the phone rings to the time that someone answers the call. The workflow specifies the queue to use for holding the call, and specifies the routing method to use for hunt groups or the questions and answers to use for interactive response groups. A workflow also defines settings such as a welcome message, music on hold, business hours, and holidays.</span></span>

<span data-ttu-id="2ad16-109">Sie verwenden das Reaktionsgruppen-Konfigurations Tool zum Erstellen von Workflows.</span><span class="sxs-lookup"><span data-stu-id="2ad16-109">You use the Response Group Configuration Tool to create workflows.</span></span> <span data-ttu-id="2ad16-110">Sie können auf der Seite Reaktionsgruppe der lync Server-Systemsteuerung auf das Tool für die Reaktionsgruppen Konfiguration zugreifen.</span><span class="sxs-lookup"><span data-stu-id="2ad16-110">You can access the Response Group Configuration Tool from the Response Group page of Lync Server Control Panel.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2ad16-111">Vor dem Erstellen eines Workflows müssen Sie zuerst Agent-Gruppen und Warteschleifen erstellen, die vom Workflow verwendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="2ad16-111">You must create agent groups and queues before you create a workflow that uses them.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="2ad16-112">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="2ad16-112">In This Section</span></span>

  - [<span data-ttu-id="2ad16-113">Erstellen oder Ändern eines Sammel Ansuchen-Workflows in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ad16-113">Create or modify a hunt group workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-hunt-group-workflow.md)

  - [<span data-ttu-id="2ad16-114">Entwerfen von Anrufflüssen für interaktive Sprachantwort in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ad16-114">Design interactive voice response call flows in Lync Server 2013</span></span>](lync-server-2013-design-interactive-voice-response-call-flows.md)

  - [<span data-ttu-id="2ad16-115">Erstellen oder Ändern eines interaktiven Workflows in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ad16-115">Create or modify an interactive workflow in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-interactive-workflow.md)

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="2ad16-116">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="2ad16-116">Related Sections</span></span>

  - [<span data-ttu-id="2ad16-117">Erstellen von Agent-Gruppen für Reaktionsgruppen Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ad16-117">Create Response Group agent groups Lync Server 2013</span></span>](lync-server-2013-create-response-group-agent-groups.md)

  - [<span data-ttu-id="2ad16-118">Erstellen von Warteschleifen für Reaktionsgruppen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2ad16-118">Create Response Group queues in Lync Server 2013</span></span>](lync-server-2013-create-response-group-queues.md)

<span data-ttu-id="2ad16-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2ad16-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

