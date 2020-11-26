---
title: Migrieren von Telefonen für gemeinsame Bereiche
description: Migrieren von Telefonen im allgemeinen Bereich
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate Common Area Phones
ms:assetid: 31bd26fc-861b-45c6-8221-18df16e575de
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688015(v=OCS.15)
ms:contentKeyID: 49733604
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b8df4d94a3db3274df7e4e82ed2185c3626de12
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443825"
---
# <a name="migrate-common-area-phones"></a><span data-ttu-id="e9a2f-103">Migrieren von Telefonen für gemeinsame Bereiche</span><span class="sxs-lookup"><span data-stu-id="e9a2f-103">Migrate Common Area Phones</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e9a2f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e9a2f-104">

<span> </span></span></span>

<span data-ttu-id="e9a2f-105">_**Letztes Änderungsdatum des Themas:** 2012-09-29_</span><span class="sxs-lookup"><span data-stu-id="e9a2f-105">_**Topic Last Modified:** 2012-09-29_</span></span>

<span data-ttu-id="e9a2f-106">Telefone im öffentlichen Bereich sind IP-Telefone, die sich am häufigsten in einem freigegebenen Arbeitsbereich oder in einem gemeinsamen Bereich befinden, beispielsweise in einer Lobby, einer Küche oder einem Factory-Stockwerk.</span><span class="sxs-lookup"><span data-stu-id="e9a2f-106">Common Area Phones are IP phones that most often reside in a shared workspace or common area, like a lobby, kitchen, or factory floor.</span></span> <span data-ttu-id="e9a2f-107">Telefone im öffentlichen Bereich müssen nicht mit einem Computer verbunden sein, um die lync Server UC-Funktionalität bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="e9a2f-107">Common Area Phones do not need to be connected to a computer to provide Lync Server UC functionality.</span></span> <span data-ttu-id="e9a2f-108">Nachdem Sie eine lync Server 2010-Bereitstellung zu lync Server 2013 migriert haben, müssen Sie auch die Kontaktobjekte migrieren, die mit dem Legacy-Telefon des öffentlichen Bereichs verknüpft sind.</span><span class="sxs-lookup"><span data-stu-id="e9a2f-108">After migrating an Lync Server 2010 deployment to Lync Server 2013, you must also migrate the contact objects associated with the legacy Common Area Phone.</span></span> <span data-ttu-id="e9a2f-109">Mithilfe der lync Server-Verwaltungsshell rufen Sie zunächst alle Kontaktobjekte ab, die mit den Telefonen des lync Server 2010-common areas verknüpft sind, und verschieben diese Objekte dann in den lync Server 2013-Pool.</span><span class="sxs-lookup"><span data-stu-id="e9a2f-109">Using Lync Server Management Shell you will first retrieve all contact objects associated with the Lync Server 2010 Common Area Phones, and then move those objects to the Lync Server 2013 pool.</span></span>

<span data-ttu-id="e9a2f-110">**Migrieren von Telefonen für gemeinsame Bereiche**</span><span class="sxs-lookup"><span data-stu-id="e9a2f-110">**Migrate Common Area Phones**</span></span>

1.  <span data-ttu-id="e9a2f-111">Öffnen Sie auf dem lync Server 2013-Front-End-Server die lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="e9a2f-111">From the Lync Server 2013 Front End server, open Lync Server Management Shell.</span></span>

2.  <span data-ttu-id="e9a2f-112">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="e9a2f-112">From the command line, type the following:</span></span>
    
        Get-CsCommonAreaPhone -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsCommonAreaPhone -Target pool02.contoso.net

3.  <span data-ttu-id="e9a2f-113">Um zu überprüfen, ob alle Kontaktobjekte in den lync Server 2013-Pool verschoben wurden, geben Sie aus der lync Server-Verwaltungsshell Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="e9a2f-113">To verify all contact objects have been moved to the Lync Server 2013 pool, from the Lync Server Management Shell type the following:</span></span>
    
        Get-CsCommonAreaPhone -Filter {RegistrarPool -eq "pool02.contoso.net"}
    
    <span data-ttu-id="e9a2f-114">Überprüfen Sie, ob alle Kontaktobjekte jetzt dem lync Server 2013-Pool zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="e9a2f-114">Verify all contact objects are now associated with the Lync Server 2013 pool.</span></span>

<span data-ttu-id="e9a2f-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e9a2f-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

