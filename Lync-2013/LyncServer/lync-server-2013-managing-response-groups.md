---
title: 'Lync Server 2013: Verwalten von Reaktionsgruppen'
description: 'Lync Server 2013: Verwalten von Reaktionsgruppen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing response groups
ms:assetid: 5a804d7d-3c1a-4647-a0e0-d5c4c8c23b73
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520996(v=OCS.15)
ms:contentKeyID: 48184222
ms.date: 02/01/2018
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 138ece386d55895893402e5a1fdead58790504f5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437210"
---
# <a name="managing-response-groups-in-lync-server-2013"></a><span data-ttu-id="6597a-103">Verwalten von Reaktionsgruppen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6597a-103">Managing response groups in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6597a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6597a-104">

<span> </span></span></span>

<span data-ttu-id="6597a-105">_**Letztes Änderungsdatum des Themas:** 2018-02-01_</span><span class="sxs-lookup"><span data-stu-id="6597a-105">_**Topic Last Modified:** 2018-02-01_</span></span>

<span data-ttu-id="6597a-106">Reaktionsgruppen sind eine anrufverwaltungsfunktion, mit der Sie Anrufe an einen bestimmten Bereich, beispielsweise einen Helpdesk, in die Warteschlange stellen und die Anrufe an eine bestimmte Gruppe von Personen weiterleiten können, die so genannten *Agenten* sind.</span><span class="sxs-lookup"><span data-stu-id="6597a-106">Response groups are a call management feature that enables you to queue calls that are made to a specific area, such as a Help Desk, and then route the calls to a designated group of people, called *agents*.</span></span>

<span data-ttu-id="6597a-107">Zum Verwalten von Reaktionsgruppen konfigurieren Sie Agentengruppen,-Warteschlangen und-Workflows, die definieren, was mit einem Anruf ab dem Zeitpunkt erfolgt, zu dem er gespeichert wird, bis ein Agent ihn beantwortet.</span><span class="sxs-lookup"><span data-stu-id="6597a-107">To manage response groups, you configure agent groups, queues, and workflows, which define what happens to a call from the time it is placed until an agent answers it.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="6597a-108">Wenn in der Bereitstellung von Reaktionsgruppen mehr als 300-Workflows in einem einzigen Pool vorhanden sind, empfiehlt es sich, die Cmdlets der lync Server-Verwaltungsshell zum Erstellen der Workflows zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="6597a-108">If you have more than 300 workflows in a single pool in your Response Group deployment, it is better to use Lync Server Management Shell cmdlets to create the workflows.</span></span> <span data-ttu-id="6597a-109">Wenn Sie das Tool für die Reaktionsgruppen Konfiguration verwenden, um Workflows für einen Pool mit mehr als 300-Workflows zu erstellen, dauert die Ladezeit der Webseite sehr lange.</span><span class="sxs-lookup"><span data-stu-id="6597a-109">If you use the Response Group Configuration Tool to create workflows for a pool that has more than 300 workflows, the webpage takes a long time to load.</span></span> <span data-ttu-id="6597a-110">Die Anzahl der Agents, die indirekt Workflows über die Warteschlangen zugeordnet sind, wirkt sich auch proportional auf das Laden der Seite aus.</span><span class="sxs-lookup"><span data-stu-id="6597a-110">The number of agents that are indirectly associated with workflows through the queues also has a proportional effect on page loading.</span></span>



</div>

<span data-ttu-id="6597a-111">Die Themen in diesem Abschnitt enthalten Schritt-für-Schritt-Verfahren für Aufgaben, die Sie ausführen können, um die reaktionsgruppenanwendung in Ihrer Bereitstellung anzupassen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="6597a-111">Topics in this section provide step-by-step procedures for tasks that you can perform to customize and maintain the Response Group application in your deployment</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="6597a-112">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="6597a-112">In This Section</span></span>

  - [<span data-ttu-id="6597a-113">Verwalten von Reaktionsgruppen-Agentgruppen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6597a-113">Managing Response Group agent groups in Lync Server 2013</span></span>](lync-server-2013-managing-response-group-agent-groups.md)

  - [<span data-ttu-id="6597a-114">Verwalten von warte Gruppen Warteschlangen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6597a-114">Managing Response Group queues in Lync Server 2013</span></span>](lync-server-2013-managing-response-group-queues.md)

  - [<span data-ttu-id="6597a-115">Verwalten von reaktionsgruppenworkflows in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6597a-115">Managing Response Group workflows in Lync Server 2013</span></span>](lync-server-2013-managing-response-group-workflows.md)

  - [<span data-ttu-id="6597a-116">Verwalten von Reaktionsgruppeneinstellungen auf Anwendungsebene in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6597a-116">Managing application-level Response Group settings in Lync Server 2013</span></span>](lync-server-2013-managing-application-level-response-group-settings.md)

  - [<span data-ttu-id="6597a-117">Verschieben von Reaktionsgruppen in einen neuen Pool in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6597a-117">Moving response groups to a new pool in Lync Server 2013</span></span>](lync-server-2013-moving-response-groups-to-a-new-pool.md)

  - [<span data-ttu-id="6597a-118">Verwalten von Reaktionsgruppen in Lync Server 2013 während eines Notfalls</span><span class="sxs-lookup"><span data-stu-id="6597a-118">Managing response groups in Lync Server 2013 during a disaster</span></span>](lync-server-2013-managing-response-groups-during-a-disaster.md)

<span data-ttu-id="6597a-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6597a-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

