---
title: 'Lync Server 2013: Erstellen von Agent-Gruppen für Reaktionsgruppen'
description: 'Lync Server 2013: Erstellen von Reaktionsgruppen-Agentgruppen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Create Response Group agent groups
ms:assetid: 2a80de17-ead0-46e8-8a27-7a4e233dbde0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520969(v=OCS.15)
ms:contentKeyID: 48183688
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a9420ee5f6fbd4b995c8542b848ef30f53e46fc4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49431617"
---
# <a name="create-response-group-agent-groups-lync-server-2013"></a><span data-ttu-id="d97ec-103">Erstellen von Agent-Gruppen für Reaktionsgruppen Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d97ec-103">Create Response Group agent groups Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d97ec-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d97ec-104">

<span> </span></span></span>

<span data-ttu-id="d97ec-105">_**Letztes Änderungsdatum des Themas:** 2012-09-12_</span><span class="sxs-lookup"><span data-stu-id="d97ec-105">_**Topic Last Modified:** 2012-09-12_</span></span>

<span data-ttu-id="d97ec-106">Beim Erstellen einer Agentgruppe wählen Sie die Agents aus, die der Gruppe zugewiesen werden. Außerdem geben Sie zusätzliche Gruppeneinstellungen (beispielsweise die Routingmethode) an und legen fest, ob sich ein Agent bei der Gruppe an- und abmelden muss.</span><span class="sxs-lookup"><span data-stu-id="d97ec-106">When you create an agent group, you select the agents that are assigned to the group and specify additional group settings, such as the routing method and whether an agent can sign in to and out of the group.</span></span>

<span data-ttu-id="d97ec-107">Ein Agent, der sich bei der Gruppe an-und abmelden muss, die sich von der Anmeldung bei lync Server unterscheidet, wird als *formeller Agent* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d97ec-107">An agent who must sign in and out of the group, which is different from signing in or out of Lync Server, is called a *formal agent*.</span></span> <span data-ttu-id="d97ec-108">Formelle Agents müssen sich bei der Gruppe anmelden, um an die Gruppe weitergeleitete Anrufe empfangen zu können.</span><span class="sxs-lookup"><span data-stu-id="d97ec-108">Formal agents must be signed in to the group before they can receive calls routed to the group.</span></span> <span data-ttu-id="d97ec-109">Dies kann für Agents nützlich sein, die Anrufe der Gruppe nur zeitweise annehmen.</span><span class="sxs-lookup"><span data-stu-id="d97ec-109">This can be useful for agents who answer calls from the group on a part-time basis.</span></span> <span data-ttu-id="d97ec-110">Formelle Agents melden sich bei ihren Gruppen an und aus, indem Sie in lync 2013 auf ein Menüelement klicken, um den Internet Browser von Windows Internet Explorer zu öffnen und eine Webseite-Konsole anzuzeigen.</span><span class="sxs-lookup"><span data-stu-id="d97ec-110">Formal agents sign in and out of their groups by clicking a menu item in Lync 2013 to open the Windows Internet Explorer Internet browser and display a webpage console.</span></span>

<span data-ttu-id="d97ec-111">Ein Agent, der sich nicht bei der Gruppe anmeldet, wird als *informeller Agent* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d97ec-111">An agent who does not sign in or out of the group is called an *informal agent*.</span></span> <span data-ttu-id="d97ec-112">Informelle Agents werden bei der Anmeldung bei lync Server automatisch bei der Gruppe angemeldet, und Sie können sich nicht von der Gruppe abmelden.</span><span class="sxs-lookup"><span data-stu-id="d97ec-112">Informal agents are automatically signed in to the group when they sign in to Lync Server, and they cannot sign out of the group.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d97ec-113">Nur lokale Benutzer können Agents sein.</span><span class="sxs-lookup"><span data-stu-id="d97ec-113">Only on-premises users can be agents.</span></span> <span data-ttu-id="d97ec-114">Wenn ein Agent von lokal in Online verschoben wird, werden keine Antwortgruppen Aufrufe an diesen Agenten weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="d97ec-114">If an agent is moved from on-premises to online, Response Group calls will not be routed to that agent.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d97ec-115">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d97ec-115">In This Section</span></span>

[<span data-ttu-id="d97ec-116">Erstellen oder Ändern einer Agentengruppe in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d97ec-116">Create or modify an agent group in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-an-agent-group.md)

<span data-ttu-id="d97ec-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d97ec-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

