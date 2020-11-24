---
title: 'Lync Server 2013: Planen von Funktionen zur Anrufverwaltung'
description: 'Lync Server 2013: Planen von Anruf Verwaltungsfeatures'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for call management features
ms:assetid: 5f557345-5a04-45d6-b274-c02dbfe41b33
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398421(v=OCS.15)
ms:contentKeyID: 48184298
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ec990aad40baf33365e92e78ee8071216a2add1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393779"
---
# <a name="planning-for-call-management-features-in-lync-server-2013"></a><span data-ttu-id="45c1d-103">Planen der Anruf Verwaltungsfeatures in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="45c1d-103">Planning for call management features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="45c1d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="45c1d-104">

<span> </span></span></span>

<span data-ttu-id="45c1d-105">_**Letztes Änderungsdatum des Themas:** 2012-12-17_</span><span class="sxs-lookup"><span data-stu-id="45c1d-105">_**Topic Last Modified:** 2012-12-17_</span></span>

<span data-ttu-id="45c1d-106">Enterprise-VoIP-anrufverwaltungsfunktionen steuern, wie eingehende Anrufe weitergeleitet und beantwortet werden.</span><span class="sxs-lookup"><span data-stu-id="45c1d-106">Enterprise Voice call management features control how incoming calls are routed and answered.</span></span> <span data-ttu-id="45c1d-107">Lync Server 2013 bietet die folgenden anrufverwaltungsfunktionen:</span><span class="sxs-lookup"><span data-stu-id="45c1d-107">Lync Server 2013 provides the following call management features:</span></span>

  - <span data-ttu-id="45c1d-108">**Parken von Anrufen**: Ermöglicht VoIP-Benutzern, Anrufe vorübergehend zu parken und anschließend am gleichen oder an einem anderen Telefon entgegenzunehmen.</span><span class="sxs-lookup"><span data-stu-id="45c1d-108">**Call Park**:   Enables voice users to temporarily park a call and then pick it up from the same or another phone.</span></span>

  - <span data-ttu-id="45c1d-109">**Gruppenannahme**: Ermöglicht VoIP-Benutzern das Annehmen von Anrufen, die an andere VoIP-Benutzer eingehen, die Annahmegruppen zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="45c1d-109">**Group Pickup**:   Enables voice users to pick up calls that are ringing for other voice users who are assigned to call pickup groups.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="45c1d-110">Die Gruppen Abholung ist neu mit kumulativen Updates für lync Server 2013: Februar 2013.</span><span class="sxs-lookup"><span data-stu-id="45c1d-110">Group Pickup is new with Cumulative Updates for Lync Server 2013: February 2013.</span></span>

    
    </div>

  - <span data-ttu-id="45c1d-111">**Reaktionsgruppe**: Leitet eingehende Anrufe mithilfe von Sammelanschlüssen oder interaktiven Sprachantworten an Agentgruppen weiter.</span><span class="sxs-lookup"><span data-stu-id="45c1d-111">**Response Group**:   Routes incoming calls to groups of agents by using hunt groups or interactive voice response (IVR) questions and answers.</span></span>

  - <span data-ttu-id="45c1d-112">**Ankündigung:**    Wiedergabe einer Nachricht für Anrufe an eine nicht zugewiesene Nummer oder Weiterleiten des Anrufs an einem anderen Ort oder in beiden Fällen.</span><span class="sxs-lookup"><span data-stu-id="45c1d-112">**Announcement:**    Plays a message for calls made to an unassigned number, or routes the call elsewhere, or both.</span></span>

<span data-ttu-id="45c1d-113">Wenn Sie die Bereitstellung von Enterprise-VoIP planen, können Sie einige oder alle dieser Anrufverwaltungsfunktionen implementieren.</span><span class="sxs-lookup"><span data-stu-id="45c1d-113">If you plan to deploy Enterprise Voice, you can choose to implement any or all of these call management features.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="45c1d-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="45c1d-114">In This Section</span></span>

  - [<span data-ttu-id="45c1d-115">Planen des Parkens von Anrufen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="45c1d-115">Planning for Call Park in Lync Server 2013</span></span>](lync-server-2013-planning-for-call-park.md)

  - [<span data-ttu-id="45c1d-116">Planen der Abholung von Gruppen anrufen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="45c1d-116">Planning for Group Call Pickup in Lync Server 2013</span></span>](lync-server-2013-planning-for-group-call-pickup.md)

  - [<span data-ttu-id="45c1d-117">Planen von Reaktionsgruppen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="45c1d-117">Planning for response groups in Lync Server 2013</span></span>](lync-server-2013-planning-for-response-groups.md)

  - [<span data-ttu-id="45c1d-118">Planen von Ansagen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="45c1d-118">Planning for announcements in Lync Server 2013</span></span>](lync-server-2013-planning-for-announcements.md)

<span data-ttu-id="45c1d-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="45c1d-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

