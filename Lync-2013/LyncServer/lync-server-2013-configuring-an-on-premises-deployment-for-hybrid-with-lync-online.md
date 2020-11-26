---
title: Konfigurieren einer lokalen Bereitstellung für Hybridumgebungen mit Lync Online
description: Konfigurieren einer lokalen Bereitstellung für Hybrid mit lync Online
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring an on-premises deployment for hybrid with Lync Online
ms:assetid: c26addb0-2936-4eea-9071-3ab95825154b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205237(v=OCS.15)
ms:contentKeyID: 48185321
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 717900389db98fc14513a7d54bd37813757f98ad
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433388"
---
# <a name="configuring-an-on-premises-deployment-for-hybrid-with-lync-online"></a><span data-ttu-id="8a2b5-103">Konfigurieren einer lokalen Bereitstellung für Hybridumgebungen mit Lync Online</span><span class="sxs-lookup"><span data-stu-id="8a2b5-103">Configuring an on-premises deployment for hybrid with Lync Online</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8a2b5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8a2b5-104">

<span> </span></span></span>

<span data-ttu-id="8a2b5-105">_**Letztes Änderungsdatum des Themas:** 2014-05-28_</span><span class="sxs-lookup"><span data-stu-id="8a2b5-105">_**Topic Last Modified:** 2014-05-28_</span></span>

<span data-ttu-id="8a2b5-106">Bei einer hybridbereitstellung handelt es sich um eine Bereitstellung, in der einige Benutzer lokal verwaltet werden und einige Benutzer online sind, aber alle Benutzer dieselbe Domäne verwenden, beispielsweise user@contoso.com.</span><span class="sxs-lookup"><span data-stu-id="8a2b5-106">A hybrid deployment is a deployment in which some users are homed on-premises and some users are homed online, but all users share the same domain, such as user@contoso.com.</span></span> <span data-ttu-id="8a2b5-107">In diesem Abschnitt wird beschrieben, wie Sie die für eine hybridbereitstellung erforderlichen Anwendungen bereitstellen und dann Ihre Bereitstellung so konfigurieren, dass Sie aktiviert wird.</span><span class="sxs-lookup"><span data-stu-id="8a2b5-107">This section guides you through deploying the applications required for a hybrid deployment, and then configuring your deployment to enable it.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="8a2b5-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="8a2b5-108">In This Section</span></span>

  - [<span data-ttu-id="8a2b5-109">Übersicht über die lync Server 2013-Hybridumgebung</span><span class="sxs-lookup"><span data-stu-id="8a2b5-109">Overview of the Lync Server 2013 hybrid environment</span></span>](lync-server-2013-overview-of-the-lync-server-hybrid-environment.md)

  - [<span data-ttu-id="8a2b5-110">Schritte zur Vorbereitung und Bereitstellung einer Lync Server 2013-Hybridumgebung</span><span class="sxs-lookup"><span data-stu-id="8a2b5-110">Steps to prepare and deploy Lync Server 2013 hybrid environment</span></span>](lync-server-2013-steps-to-prepare-and-deploy-lync-server-hybrid-environment.md)

  - [<span data-ttu-id="8a2b5-111">Konfigurieren des Verbunds von lync Server 2013 mit lync Online</span><span class="sxs-lookup"><span data-stu-id="8a2b5-111">Configure federation of Lync Server 2013 with Lync Online</span></span>](lync-server-2013-configure-federation-with-lync-online.md)

  - [<span data-ttu-id="8a2b5-112">Konfigurieren des Verbunds für einen Audiokonferenz-Anbieter in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8a2b5-112">Configure federation for an audio conferencing provider in Lync Server 2013</span></span>](lync-server-2013-configure-federation-for-an-audio-conferencing-provider.md)

  - [<span data-ttu-id="8a2b5-113">Verschieben von Benutzern nach lync Online in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8a2b5-113">Move users to Lync Online in Lync Server 2013</span></span>](lync-server-2013-move-users-to-lync-online.md)

  - [<span data-ttu-id="8a2b5-114">Verwalten von Benutzern in einer hybriden lync Server 2013-Bereitstellung</span><span class="sxs-lookup"><span data-stu-id="8a2b5-114">Administering users in a hybrid Lync Server 2013 deployment</span></span>](lync-server-2013-administering-users-in-a-hybrid-deployment.md)

<span data-ttu-id="8a2b5-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8a2b5-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

