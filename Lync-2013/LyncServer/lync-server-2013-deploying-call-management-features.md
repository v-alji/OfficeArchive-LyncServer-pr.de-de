---
title: 'Lync Server 2013: Bereitstellen von Funktionen zur Anrufverwaltung'
description: 'Lync Server 2013: Bereitstellen von Funktionen zur Anrufverwaltung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying call management features
ms:assetid: 1667cfe4-76fa-4e10-91bb-b3efbedbf759
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204706(v=OCS.15)
ms:contentKeyID: 48183504
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aa89b75dbcae9de1069daf99986076b66e0411cc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430070"
---
# <a name="deploying-call-management-features-in-lync-server-2013"></a><span data-ttu-id="7cdb9-103">Bereitstellen von Anruf Verwaltungsfeatures in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7cdb9-103">Deploying call management features in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7cdb9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7cdb9-104">

<span> </span></span></span>

<span data-ttu-id="7cdb9-105">_**Letztes Änderungsdatum des Themas:** 2012-12-18_</span><span class="sxs-lookup"><span data-stu-id="7cdb9-105">_**Topic Last Modified:** 2012-12-18_</span></span>

<span data-ttu-id="7cdb9-106">Enterprise-VoIP-anrufverwaltungsfunktionen steuern, wie eingehende Anrufe weitergeleitet und beantwortet werden.</span><span class="sxs-lookup"><span data-stu-id="7cdb9-106">Enterprise Voice call management features control how incoming calls are routed and answered.</span></span> <span data-ttu-id="7cdb9-107">Lync Server 2013 bietet die folgenden anrufverwaltungsfunktionen:</span><span class="sxs-lookup"><span data-stu-id="7cdb9-107">Lync Server 2013 provides the following call management features:</span></span>

  - <span data-ttu-id="7cdb9-108">**Park anrufen:** Ermöglicht es sprach Benutzern, einen Anruf vorübergehend zu parken und ihn dann vom gleichen Telefon oder einem anderen Telefon aus abzuwählen.</span><span class="sxs-lookup"><span data-stu-id="7cdb9-108">**Call Park:** Enables voice users to temporarily park a call and then pick it up from the same phone or another phone.</span></span>

  - <span data-ttu-id="7cdb9-109">**Gruppen Abholung:** Ermöglicht Benutzern das annehmen von Anrufen an einen anderen Benutzer, der einer Pickup-Gruppe zugewiesen ist, indem Sie die Nummer für die Anruf-Abhol Gruppe wählen.</span><span class="sxs-lookup"><span data-stu-id="7cdb9-109">**Group Pickup:** Enables users to answer calls made to another user who is assigned to a pickup group by dialing the call pickup group number.</span></span>

  - <span data-ttu-id="7cdb9-110">**Reaktionsgruppe:** Leitet eingehende Anrufe an Gruppen von Agents weiter, indem Sie Sammelanschlüsse oder Fragen und Antworten zu Interaktionen (Interactive Voice Response) verwenden.</span><span class="sxs-lookup"><span data-stu-id="7cdb9-110">**Response Group:** Routes incoming calls to groups of agents by using hunt groups or interactive voice response (IVR) questions and answers.</span></span>

  - <span data-ttu-id="7cdb9-111">**Ankündigung:** Wiedergabe einer Nachricht für Anrufe an eine nicht zugewiesene Nummer oder Weiterleiten des Anrufs an einem anderen Ort oder in beiden Fällen.</span><span class="sxs-lookup"><span data-stu-id="7cdb9-111">**Announcement:** Plays a message for calls made to an unassigned number, or routes the call elsewhere, or both.</span></span>

<span data-ttu-id="7cdb9-112">In diesem Abschnitt wird beschrieben, wie Sie diese anrufverwaltungsfunktionen während einer Enterprise-VoIP-Bereitstellung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="7cdb9-112">This section describes how to configure these call management features during an Enterprise Voice deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7cdb9-113">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="7cdb9-113">In This Section</span></span>

  - [<span data-ttu-id="7cdb9-114">Konfigurieren des Parkens von Anrufen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7cdb9-114">Configuring Call Park in Lync Server 2013</span></span>](lync-server-2013-configuring-call-park.md)

  - [<span data-ttu-id="7cdb9-115">Konfigurieren der Gruppenanruf Abholung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7cdb9-115">Configuring Group Call Pickup in Lync Server 2013</span></span>](lync-server-2013-configuring-group-call-pickup.md)

  - [<span data-ttu-id="7cdb9-116">Konfigurieren von Reaktionsgruppen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7cdb9-116">Configuring Response Group in Lync Server 2013</span></span>](lync-server-2013-configuring-response-group.md)

  - [<span data-ttu-id="7cdb9-117">Konfigurieren von Ansagen für nicht zugewiesene Nummern in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7cdb9-117">Configuring announcements for unassigned numbers in Lync Server 2013</span></span>](lync-server-2013-configuring-announcements-for-unassigned-numbers.md)

<span data-ttu-id="7cdb9-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7cdb9-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

