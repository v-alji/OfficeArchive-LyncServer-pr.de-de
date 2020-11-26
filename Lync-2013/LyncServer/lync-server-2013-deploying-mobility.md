---
title: 'Lync Server 2013: Bereitstellen von Mobilität'
description: 'Lync Server 2013: Bereitstellen von Mobilität.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying mobility
ms:assetid: f41e6b25-d2cd-43fd-a17b-22cfda8bcd4f
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690055(v=OCS.15)
ms:contentKeyID: 48185805
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cf927b950f8b94884fb91224a87e196fc815fca1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429874"
---
# <a name="deploying-mobility-in-lync-server-2013"></a><span data-ttu-id="c02fb-103">Bereitstellen von Mobilität in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c02fb-103">Deploying mobility in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c02fb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c02fb-104">

<span> </span></span></span>

<span data-ttu-id="c02fb-105">_**Letztes Änderungsdatum des Themas:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="c02fb-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="c02fb-106">Wenn Sie das Mobilitätsfeature von lync Server 2013 bereitstellen, können mobile Benutzer unterstützte mobile Geräte für lync-Funktionen wie Instant Messaging (im), Anwesenheitsinformationen und Kontakte verwenden.</span><span class="sxs-lookup"><span data-stu-id="c02fb-106">When you deploy the Lync Server 2013 mobility feature, mobile users can use supported mobile devices for Lync functionality such as instant messaging (IM), presence, and contacts.</span></span>

<span data-ttu-id="c02fb-107">Details zu den Anforderungen für die Bereitstellung des Mobilitätsfeatures finden Sie unter [Planen der Mobilität in lync Server 2013](lync-server-2013-planning-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="c02fb-107">For details about requirements for deploying the mobility feature, see [Planning for mobility in Lync Server 2013](lync-server-2013-planning-for-mobility.md).</span></span>

<span data-ttu-id="c02fb-108">Dieser Abschnitt führt Sie durch die Schritte zum Bereitstellen und Überprüfen der Mobilitäts-und automatischen Erkennungs Features.</span><span class="sxs-lookup"><span data-stu-id="c02fb-108">This section guides you through the steps for deploying and verifying the mobility and automatic discovery features.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c02fb-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c02fb-109">In This Section</span></span>

  - [<span data-ttu-id="c02fb-110">Erstellen von DNS-Einträgen für den AutoErmittlungsdienst in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c02fb-110">Creating DNS records for the Autodiscover Service in Lync Server 2013</span></span>](lync-server-2013-creating-dns-records-for-the-autodiscover-service.md)

  - [<span data-ttu-id="c02fb-111">Ändern der Zertifikate für Mobilität in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c02fb-111">Modifying certificates for mobility in Lync Server 2013</span></span>](lync-server-2013-modifying-certificates-for-mobility.md)

  - [<span data-ttu-id="c02fb-112">Konfigurieren des Reverseproxys für Mobilität in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c02fb-112">Configuring the reverse proxy for mobility in Lync Server 2013</span></span>](lync-server-2013-configuring-the-reverse-proxy-for-mobility.md)

  - [<span data-ttu-id="c02fb-113">Konfigurieren der AutoErmittlung in Lync Server 2013 für Mobilität mit hybriden Bereitstellungen</span><span class="sxs-lookup"><span data-stu-id="c02fb-113">Configuring Autodiscover in Lync Server 2013 for mobility with hybrid deployments</span></span>](lync-server-2013-configuring-autodiscover-for-mobility-with-hybrid-deployments.md)

  - [<span data-ttu-id="c02fb-114">Überprüfen der Mobilitätsbereitstellung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c02fb-114">Verifying your mobility deployment in Lync Server 2013</span></span>](lync-server-2013-verifying-your-mobility-deployment.md)

  - [<span data-ttu-id="c02fb-115">Konfigurieren von Pushbenachrichtigungen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c02fb-115">Configuring for push notifications in Lync Server 2013</span></span>](lync-server-2013-configuring-for-push-notifications.md)

  - [<span data-ttu-id="c02fb-116">Konfigurieren der Mobilitätsrichtlinie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c02fb-116">Configuring mobility policy in Lync Server 2013</span></span>](lync-server-2013-configuring-mobility-policy.md)

<span data-ttu-id="c02fb-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c02fb-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

