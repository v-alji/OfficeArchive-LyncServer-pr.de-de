---
title: 'Lync Server 2013: Zuweisen von Standortrichtlinien Bereich'
description: 'Lync Server 2013: Zuweisen des Bereichs für Standortrichtlinien.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assigning location policy scope
ms:assetid: e4c66517-c593-4253-b900-7b4dd8bddf2f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205360(v=OCS.15)
ms:contentKeyID: 48185734
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9f6c46150241b0b224e8005556c0f2f594d8bce5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438302"
---
# <a name="assigning-location-policy-scope-in-lync-server-2013"></a><span data-ttu-id="345da-103">Zuweisen von Standortrichtlinien Bereich in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="345da-103">Assigning location policy scope in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="345da-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="345da-104">

<span> </span></span></span>

<span data-ttu-id="345da-105">_**Letztes Änderungsdatum des Themas:** 2012-06-06_</span><span class="sxs-lookup"><span data-stu-id="345da-105">_**Topic Last Modified:** 2012-06-06_</span></span>

<span data-ttu-id="345da-106">Wie bei anderen lync-Server Richtlinien können Standortrichtlinien auf mehreren Bereichsebenen zugewiesen werden: Global, Website und Benutzer.</span><span class="sxs-lookup"><span data-stu-id="345da-106">As with other Lync Server policies, location policies can be assigned at multiple scope levels: global, site, and user.</span></span> <span data-ttu-id="345da-107">Der Bereich der Standortrichtlinien auf Benutzerebene verhält sich jedoch etwas anders als bei anderen lync-Server Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="345da-107">However, the scope of user-level location policies behaves a bit differently than with other Lync Server policies.</span></span> <span data-ttu-id="345da-108">Auf Endpunkt Objekte (wie Benutzer und Telefon Kontaktobjekte im öffentlichen Bereich) können nicht nur Orts Richtlinien für einzelne Benutzer angewendet werden, sondern auch auf lync Server-Netzwerk Websites angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="345da-108">Not only can per-user location policies be applied to endpoint objects (such as Users and Common Area Phone contact objects), they can also be applied to Lync Server network sites.</span></span> <span data-ttu-id="345da-109">Netzwerkstandorte sind Gruppierungen von Client-Subnetzen, die einem geografischen Standort zugeordnet sind (jedoch muss es sich nicht zwingend um alle Subnetze an einem zentralen Standort oder in einer Zweigniederlassung handeln).</span><span class="sxs-lookup"><span data-stu-id="345da-109">Network sites are groupings of client subnets associated with a geographical location (but may not necessarily be all subnets in an entire central site or branch site).</span></span> <span data-ttu-id="345da-110">Alle Clients, die mit den Subnetzen an einem Netzwerkstandort verbunden sind, übernehmen automatisch die Standortrichtlinie, die dem jeweiligen Netzwerkstandort zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="345da-110">Any clients connected to the subnets in a network site automatically pick up the location policy assigned to that network site.</span></span> <span data-ttu-id="345da-111">Wenn eine Standortrichtlinie auf Benutzerebene sowohl einem Benutzer als auch einem Netzwerkstandort zugewiesen ist, hat die auf dem Netzwerkstandort basierende Standortrichtlinie Vorrang vor allen benutzerspezifischen Richtlinieneinstellungen.</span><span class="sxs-lookup"><span data-stu-id="345da-111">In cases where a user-level location policy is assigned both to a user and to a network site, the network site-based location policy overrides any per-user policy setting.</span></span>

<span data-ttu-id="345da-112">Jedem Netzwerkstandort ist eine Standortrichtlinie zugewiesen und jeder Richtlinie sind andere Werte für PSTN-Verwendungen, Benachrichtigungs-URIs und Konferenz-URIs zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="345da-112">Each network site has a location policy assigned to it, and each policy will have different PSTN Usages, Notification URIs, and Conference URIs values assigned to it.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="345da-113">Dieses spezielle Richtlinienverhalten hat folgenden Grund: Wenn ein Benutzer, der einem Pool an einem Bürostandort angehört, einen anderen Standort besucht und einen Notruf tätigen muss, gelten die Einstellungen für die E9-1-1-Anrufumleitung für diesen Netzwerkstandort unabhängig davon, welchem Pool oder welchem Standort der Benutzer zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="345da-113">The reason for this special policy scoping behavior is so that when a user homed on a pool at one office site visits another site and has to make an emergency call, the E9-1-1 call routing settings appropriate to that network site will apply no matter what pool or site the user is assigned to.</span></span>



<span data-ttu-id="345da-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="345da-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

