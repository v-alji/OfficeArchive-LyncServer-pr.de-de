---
title: 'Lync Server 2013: Informationen zu Netzwerkregionen, Standorten und Subnetzen'
description: 'Lync Server 2013: Informationen zu netzwerkregionen,-Websites und-Subnetzen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: About network regions, sites, and subnets
ms:assetid: 6662123a-d011-408c-a290-92b2a8589943
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398467(v=OCS.15)
ms:contentKeyID: 48184335
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a3c7f660f3c72003527e0721c3f9702865e9b9b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439520"
---
# <a name="about-network-regions-sites-and-subnets-in-lync-server-2013"></a><span data-ttu-id="25f1a-103">Informationen zu Netzwerkregionen, Standorten und Subnetzen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25f1a-103">About network regions, sites, and subnets in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="25f1a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="25f1a-104">

<span> </span></span></span>

<span data-ttu-id="25f1a-105">_**Letztes Änderungsdatum des Themas:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="25f1a-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="25f1a-106">Die in diesem Abschnitt beschriebenen erweiterten Enterprise-VoIP-Features geben bestimmte Konfigurationsanforderungen für netzwerkregionen, Netzwerk Websites und Subnetze frei.</span><span class="sxs-lookup"><span data-stu-id="25f1a-106">The advanced Enterprise Voice features described in this section share certain configuration requirements for network regions, network sites, and subnets.</span></span> <span data-ttu-id="25f1a-107">Für alle drei erweiterten Features ist es beispielsweise erforderlich, dass jedes Subnetz in Ihrer Topologie einer bestimmten *Netzwerk Website* zugeordnet ist, und jede Netzwerk Website muss einem *Netzwerkbereich* zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="25f1a-107">For example, all three advanced features require that each subnet in your topology be associated with a specific *network site*, and each network site must be associated with a *network region*.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="25f1a-108">Bevor Sie mit der Netzwerkkonfiguration für die Anrufsteuerung, E9-1-1 oder Media Bypass beginnen, stellen Sie sicher, dass Sie weitere Informationen zu den Netzwerkeinstellungen in den <A href="lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md">Netzwerkeinstellungen für das erweiterte Enterprise Voice-Feature in lync Server 2013</A> in der Planungsdokumentation überprüft haben.</span><span class="sxs-lookup"><span data-stu-id="25f1a-108">Before you begin network configuration for call admission control, E9-1-1, or media bypass, make sure that you reviewed additional information about network settings in the <A href="lync-server-2013-network-settings-for-the-advanced-enterprise-voice-features.md">Network settings for the advanced Enterprise Voice features in Lync Server 2013</A> topic in the Planning documentation.</span></span> <span data-ttu-id="25f1a-109">Details zur Netzwerkkonfiguration in erster Linie zur Anrufsteuerung finden Sie auch unter <A href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Definieren Ihrer Anforderungen für die Anrufsteuerung in lync Server 2013</A> in der Planungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="25f1a-109">For details about network configuration primarily about call admission control, also see <A href="lync-server-2013-defining-your-requirements-for-call-admission-control.md">Defining your requirements for call admission control in Lync Server 2013</A> in the Planning documentation.</span></span>



</div>

<span data-ttu-id="25f1a-110">Für die Anrufsteuerung und E9-1-1 gelten bei den Netzwerkstandorten zusätzliche Konfigurationsanforderungen:</span><span class="sxs-lookup"><span data-stu-id="25f1a-110">Call admission control and E9-1-1 have additional configuration requirements for network sites:</span></span>

  - <span data-ttu-id="25f1a-111">Die Anrufsteuerung erfordert, dass ein *Bandbreitenrichtlinienprofil* für jeden Standort angegeben wird, für den WAN-Bandbreiteneinschränkungen gelten.</span><span class="sxs-lookup"><span data-stu-id="25f1a-111">Call admission control requires that a *bandwidth policy profile* be specified for each site that is constrained by WAN bandwidth limitations.</span></span> <span data-ttu-id="25f1a-112">Wenn Sie beabsichtigen, die Anrufsteuerung bereitzustellen, müssen Sie die [bandbreitenrichtlinienprofile in lync Server 2013 erstellen](lync-server-2013-create-bandwidth-policy-profiles.md) , bevor Sie Ihre Netzwerk Websites konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="25f1a-112">If you plan to deploy call admission control, you must [Create bandwidth policy profiles in Lync Server 2013](lync-server-2013-create-bandwidth-policy-profiles.md) before you configure your network sites.</span></span>

  - <span data-ttu-id="25f1a-113">Für E9-1-1 ist es erforderlich, dass für jeden Standort eine *Standortrichtlinie* angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="25f1a-113">E9-1-1 requires that a *location policy* be specified for each site.</span></span> <span data-ttu-id="25f1a-114">Wenn Sie die Bereitstellung von E9-1-1 planen, müssen Sie [in lync Server 2013 Standortrichtlinien erstellen](lync-server-2013-create-location-policies.md) , bevor Sie Ihre Netzwerk Websites konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="25f1a-114">If you plan to deploy E9-1-1, you must [Create location policies in Lync Server 2013](lync-server-2013-create-location-policies.md) before you configure your network sites.</span></span>

<div>

## <a name="create-or-modify-network-regions-network-sites-and-subnets"></a><span data-ttu-id="25f1a-115">Erstellen oder Ändern von netzwerkregionen, Netzwerk Websites und Subnetzen</span><span class="sxs-lookup"><span data-stu-id="25f1a-115">Create or Modify Network Regions, Network Sites, and Subnets</span></span>

<span data-ttu-id="25f1a-116">Die folgenden Themen enthalten Schritte zum Erstellen oder Ändern von netzwerkregionen und Netzwerk Websites sowie zum Zuordnen von Subnetzen zu Netzwerkstandorten.</span><span class="sxs-lookup"><span data-stu-id="25f1a-116">The following topics provide steps to create or modify network regions and network sites, and to associate subnets with network sites.</span></span> <span data-ttu-id="25f1a-117">Diese Themen sind für keine spezielle erweiterte Enterprise-VoIP-Funktion spezifisch.</span><span class="sxs-lookup"><span data-stu-id="25f1a-117">These topics are not specific to any particular advanced Enterprise Voice feature.</span></span>

  - [<span data-ttu-id="25f1a-118">Erstellen oder Ändern eines Netzwerkbereichs in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25f1a-118">Create or modify a network region in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-region.md)

  - [<span data-ttu-id="25f1a-119">Erstellen oder Ändern eines Netzwerkstandorts in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25f1a-119">Create or modify a network site in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-network-site.md)

  - [<span data-ttu-id="25f1a-120">Zuordnen eines Subnetzes zu einem Netzwerkstandort in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25f1a-120">Associate a subnet with a network site in Lync Server 2013</span></span>](lync-server-2013-associate-a-subnet-with-a-network-site.md)

<span data-ttu-id="25f1a-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="25f1a-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

