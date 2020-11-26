---
title: 'Lync Server 2013: Übersicht über den Director'
description: 'Lync Server 2013: Übersicht über den Director.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of the Director
ms:assetid: cf9919b3-e16b-47c5-be1d-2c4bc64f44ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398879(v=OCS.15)
ms:contentKeyID: 48185393
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6686534e22bab5b02a2663789298e4cf7ea582c2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424709"
---
# <a name="overview-of-the-director-in-lync-server-2013"></a><span data-ttu-id="16236-103">Übersicht über den Director in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="16236-103">Overview of the Director in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="16236-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="16236-104">

<span> </span></span></span>

<span data-ttu-id="16236-105">_**Letztes Änderungsdatum des Themas:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="16236-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="16236-106">Bei einem Director handelt es sich um einen Server mit lync Server 2013, der Benutzeranforderungen authentifiziert, jedoch keine Benutzerkonten enthält.</span><span class="sxs-lookup"><span data-stu-id="16236-106">A Director is a server running Lync Server 2013 that authenticates user requests, but does not home any user accounts.</span></span> <span data-ttu-id="16236-107">Optional können Sie einen Director in den beiden folgenden Szenarien bereitstellen:</span><span class="sxs-lookup"><span data-stu-id="16236-107">You optionally can deploy a Director in the following two scenarios:</span></span>

  - <span data-ttu-id="16236-108">Wenn Sie den Zugriff von externen Benutzern durch die Bereitstellung von Edge-Servern aktivieren, sollten Sie auch einen Director bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="16236-108">If you enable access by external users by deploying Edge Servers, you should also deploy a Director.</span></span> <span data-ttu-id="16236-109">In diesem Szenario authentifiziert der Director die externen Benutzer und übergibt dann den Datenverkehr an interne Server.</span><span class="sxs-lookup"><span data-stu-id="16236-109">In this scenario, the Director authenticates the external users, and then passes their traffic on to internal servers.</span></span> <span data-ttu-id="16236-110">Wenn ein Director zur Authentifizierung externer Benutzer verwendet wird, entlastet es Front-End-Pool Server vor dem mehr Aufwand bei der Authentifizierung dieser Benutzer.</span><span class="sxs-lookup"><span data-stu-id="16236-110">When a Director is used to authenticate external users, it relieves Front End pool servers from the overhead of performing authentication of these users.</span></span> <span data-ttu-id="16236-111">Darüber hinaus können Sie interne Front-End-Pools vor böswilligem Datenverkehr wie Denial-of-Service-Angriffen isolieren.</span><span class="sxs-lookup"><span data-stu-id="16236-111">It also helps insulate internal Front End pools from malicious traffic such as denial-of-service attacks.</span></span> <span data-ttu-id="16236-112">Wenn das Netzwerk bei einem solchen Angriff mit einem ungültigen externen Datenverkehr überflutet wird, endet dieser Datenverkehr beim Director.</span><span class="sxs-lookup"><span data-stu-id="16236-112">If the network is flooded with invalid external traffic in such an attack, this traffic ends at the Director.</span></span>

  - <span data-ttu-id="16236-113">Wenn Sie mehrere Front-End-Pools an einem zentralen Standort bereitstellen, indem Sie dieser Website einen Director hinzufügen, können Sie Authentifizierungsanforderungen rationalisieren und die Leistung verbessern.</span><span class="sxs-lookup"><span data-stu-id="16236-113">If you deploy multiple Front End pools at a central site, by adding a Director to that site you can streamline authentication requests and improve performance.</span></span> <span data-ttu-id="16236-114">In diesem Szenario gehen alle Anforderungen zuerst an den Director, der Sie dann an den richtigen Front-End-Pool weiterleitet.</span><span class="sxs-lookup"><span data-stu-id="16236-114">In this scenario, all requests go first to the Director, which then routes them to the correct Front End pool.</span></span>

<span data-ttu-id="16236-115"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="16236-115"></div>

<span> </span>

</div>

</div>

</span></span></div>

