---
title: 'Lync Server 2013: Konfigurieren des Parkens von Anrufen'
description: 'Lync Server 2013: Konfigurieren des Anruf Parks'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Call Park
ms:assetid: e4c5da53-7f6c-4535-bc9b-9da2026caec8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399014(v=OCS.15)
ms:contentKeyID: 48185732
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1d2708f26fae5706afc31aa195b9fdb82536247b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433248"
---
# <a name="configuring-call-park-in-lync-server-2013"></a><span data-ttu-id="5f1e6-103">Konfigurieren des Parkens von Anrufen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f1e6-103">Configuring Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5f1e6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5f1e6-104">

<span> </span></span></span>

<span data-ttu-id="5f1e6-105">_**Letztes Änderungsdatum des Themas:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="5f1e6-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="5f1e6-106">Der Anruf Park ermöglicht es einem Enterprise-VoIP-Nutzer, einen Anruf von einem Telefon aus zu halten und den Anruf später abzurufen, indem er von einem beliebigen Telefon aus eine interne Rufnummer (sog. Call Park *Orbit*) wählt.</span><span class="sxs-lookup"><span data-stu-id="5f1e6-106">Call Park enables an Enterprise Voice user to put a call on hold from one telephone and then retrieve the call later by dialing an internal number (known as a Call Park *orbit*) from any telephone.</span></span>

<span data-ttu-id="5f1e6-107">Die Komponenten, die von Park verwendet werden, werden beim Bereitstellen von Enterprise-VoIP automatisch auf dem Front-End-Server oder Standard Edition-Server installiert und aktiviert.</span><span class="sxs-lookup"><span data-stu-id="5f1e6-107">The components that Call Park uses are automatically installed and enabled on the Front End Server or Standard Edition server when you deploy Enterprise Voice.</span></span> <span data-ttu-id="5f1e6-108">Sie müssen jedoch den Anruf Park konfigurieren, bevor er für die Benutzer verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="5f1e6-108">However, you must configure Call Park before it is available to users.</span></span>

<span data-ttu-id="5f1e6-109">Dieser Abschnitt führt Sie durch die Konfiguration des Anruf Parks.</span><span class="sxs-lookup"><span data-stu-id="5f1e6-109">This section guides you through the configuration of Call Park.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5f1e6-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="5f1e6-110">In This Section</span></span>

  - [<span data-ttu-id="5f1e6-111">Anforderungen und Benutzerrechte für die Konfiguration zum Parken von Anrufen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f1e6-111">Call Park configuration prerequisites and user rights in Lync Server 2013</span></span>](lync-server-2013-call-park-configuration-prerequisites-and-user-rights.md)

  - [<span data-ttu-id="5f1e6-112">Bereitstellungsprozess für den Parken von Anrufen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f1e6-112">Deployment process for Call Park in Lync Server 2013</span></span>](lync-server-2013-deployment-process-for-call-park.md)

  - [<span data-ttu-id="5f1e6-113">Konfigurieren der Orbittabelle für das Parken von Anrufen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f1e6-113">Configure the Call Park orbit table in Lync Server 2013</span></span>](lync-server-2013-configure-the-call-park-orbit-table.md)

  - [<span data-ttu-id="5f1e6-114">Konfigurieren von Einstellungen für den Anruf Park in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f1e6-114">Configure Call Park settings in Lync Server 2013</span></span>](lync-server-2013-configure-call-park-settings.md)

  - [<span data-ttu-id="5f1e6-115">Anpassen der Musik zum Parken von Anrufen im Wartebereich in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f1e6-115">Customize Call Park music on hold in Lync Server 2013</span></span>](lync-server-2013-customize-call-park-music-on-hold.md)

  - [<span data-ttu-id="5f1e6-116">Aktivieren des Anruf Parks für Benutzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f1e6-116">Enable Call Park for users in Lync Server 2013</span></span>](lync-server-2013-enable-call-park-for-users.md)

  - [<span data-ttu-id="5f1e6-117">Überprüfen von Normalisierungsregeln für den Parken von Anrufen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f1e6-117">Verify normalization rules for Call Park in Lync Server 2013</span></span>](lync-server-2013-verify-normalization-rules-for-call-park.md)

  - [<span data-ttu-id="5f1e6-118">Optional Überprüfen der Bereitstellung des Anruf Parks in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f1e6-118">(Optional) Verify Call Park deployment in Lync Server 2013</span></span>](lync-server-2013-optional-verify-call-park-deployment.md)

<span data-ttu-id="5f1e6-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5f1e6-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

