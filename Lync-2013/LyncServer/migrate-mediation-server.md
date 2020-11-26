---
title: Migrieren des Vermittlungsservers
description: Migrieren Sie den Vermittlungs Server.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate Mediation Server
ms:assetid: b0b77121-2c8f-413e-b276-dbf1038361d3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205173(v=OCS.15)
ms:contentKeyID: 48185117
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 31cc4c95f0e9c86b48594238218db22f3ec1a387
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446871"
---
# <a name="migrate-mediation-server"></a><span data-ttu-id="b2269-103">Migrieren des Vermittlungsservers</span><span class="sxs-lookup"><span data-stu-id="b2269-103">Migrate Mediation Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="b2269-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="b2269-104">

<span> </span></span></span>

<span data-ttu-id="b2269-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="b2269-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="b2269-106">Wenn Sie den Zusammenführungs-Assistenten ausführen, wird Ihr Vermittlungsserver mit ihrer lync Server 2013-Pilot Topologie verbunden.</span><span class="sxs-lookup"><span data-stu-id="b2269-106">Your Mediation Server is merged into your Lync Server 2013 pilot topology when you run the Merge wizard.</span></span> <span data-ttu-id="b2269-107">Sie konfigurieren den lync Server 2013-Vermittlungsserver allerdings, nachdem alle Benutzer migriert wurden, weil ein Office Communications Server 2007 R2-Pool nicht mit einem lync Server 2013-Vermittlungsserver kommunizieren kann.</span><span class="sxs-lookup"><span data-stu-id="b2269-107">You configure the Lync Server 2013 Mediation Server, however, after all users are migrated because an Office Communications Server 2007 R2 pool cannot communicate with a Lync Server 2013 Mediation Server.</span></span> <span data-ttu-id="b2269-108">Während der parallelen Migration kommuniziert der lync Server 2013-Pool mit dem Office Communications Server 2007 R2-Vermittlungsserver.</span><span class="sxs-lookup"><span data-stu-id="b2269-108">During the side-by-side migration, the Lync Server 2013 pool communicates with the Office Communications Server 2007 R2 Mediation Server.</span></span>

<span data-ttu-id="b2269-109">Wenn Sie Ihren lync Server 2013-Vermittlungsserver konfigurieren, müssen Sie auch Ihre Office Communications Server 2007 R2-Gateways aktualisieren oder ersetzen.</span><span class="sxs-lookup"><span data-stu-id="b2269-109">When you configure your Lync Server 2013 Mediation Server, you must also upgrade or replace your Office Communications Server 2007 R2 gateways.</span></span> <span data-ttu-id="b2269-110">Office Communications Server 2007 R2-Gateways unterstützen keinen lync Server 2013-Vermittlungsserver.</span><span class="sxs-lookup"><span data-stu-id="b2269-110">Office Communications Server 2007 R2 gateways do not support Lync Server 2013 Mediation Server.</span></span> <span data-ttu-id="b2269-111">Sie müssen Gateways bereitstellen, die für lync Server 2013 zertifiziert sind, und Sie dem lync Server 2013-Vermittlungsserver zuordnen.</span><span class="sxs-lookup"><span data-stu-id="b2269-111">You need to deploy gateways that are certified for Lync Server 2013 and associate them with the Lync Server 2013 Mediation Server.</span></span> <span data-ttu-id="b2269-112">Dieser Schritt ist erforderlich, bevor Sie Ihre Office Communications Server 2007 R2-Bereitstellung vollständig außer Dienststellen können.</span><span class="sxs-lookup"><span data-stu-id="b2269-112">This step is required before you can completely decommission your Office Communications Server 2007 R2 deployment.</span></span>

<span data-ttu-id="b2269-113">Die Themen in diesem Abschnitt beschreiben Konfigurationsaufgaben, die Sie ausführen müssen, nachdem Sie die Migration von lync Server 2013-Vermittlungsserver abgeschlossen haben.</span><span class="sxs-lookup"><span data-stu-id="b2269-113">The topics in this section describe configuration tasks that you need to perform after you have completed your migration of Lync Server 2013 Mediation Server.</span></span> <span data-ttu-id="b2269-114">Der Übergang des beiliegenden Vermittlungsservers zu einem eigenständigen Vermittlungsserver ist eine optionale Aufgabe.</span><span class="sxs-lookup"><span data-stu-id="b2269-114">Transitioning the collocated Mediation Server to a stand-alone Mediation Server is an optional task.</span></span>

  - [<span data-ttu-id="b2269-115">Konfigurieren des Vermittlungsservers</span><span class="sxs-lookup"><span data-stu-id="b2269-115">Configure Mediation Server</span></span>](configure-mediation-server.md)

  - [<span data-ttu-id="b2269-116">Ändern von VoIP-Routen zur Verwendung des neuen lync Server 2013-Vermittlungsservers</span><span class="sxs-lookup"><span data-stu-id="b2269-116">Change voice routes to use the new Lync Server 2013 Mediation Server</span></span>](change-voice-routes-to-use-the-new-lync-server-2013-mediation-server.md)

  - [<span data-ttu-id="b2269-117">Umstieg auf einen bereitstehenden Vermittlungsserver zu einem eigenständigen Vermittlungsserver (optional)</span><span class="sxs-lookup"><span data-stu-id="b2269-117">Transition a collocated Mediation Server to a stand-alone Mediation Server (optional)</span></span>](transition-a-collocated-mediation-server-to-a-stand-alone-mediation-server-optional.md)

<span data-ttu-id="b2269-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="b2269-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

