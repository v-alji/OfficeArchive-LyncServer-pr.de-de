---
title: 'Lync Server 2013: netzwerkregionen'
description: 'Lync Server 2013: netzwerkregionen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Network regions
ms:assetid: 1818e9d2-bbb7-420a-93ea-4c3da3a55ad3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ687979(v=OCS.15)
ms:contentKeyID: 49733567
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3506f3c543c0728f27bd091b9cd63991c4633da7
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425159"
---
# <a name="network-regions-in-lync-server-2013"></a><span data-ttu-id="a0925-103">Netzwerkregionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0925-103">Network regions in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a0925-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a0925-104">

<span> </span></span></span>

<span data-ttu-id="a0925-105">_**Letztes Änderungsdatum des Themas:** 2013-02-21_</span><span class="sxs-lookup"><span data-stu-id="a0925-105">_**Topic Last Modified:** 2013-02-21_</span></span>

<span data-ttu-id="a0925-106">*Netzwerkregionen* sind die Netzwerkhubs oder Backbones, die in der Konfiguration der Anruf Zulassungs Steuerung, E9-1-1 und medienumgehung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a0925-106">*Network regions* are the network hubs or backbones used in the configuration of call admission control, E9-1-1, and media bypass.</span></span> <span data-ttu-id="a0925-107">Gehen Sie wie folgt vor, um netzwerkregionen anzuzeigen, zu erstellen oder zu ändern.</span><span class="sxs-lookup"><span data-stu-id="a0925-107">Use the following procedures to view, create, or modify network regions.</span></span> <span data-ttu-id="a0925-108">Wenn Sie beispielsweise bereits netzwerkregionen für ein Sprachfeature erstellt haben, müssen Sie keine neuen netzwerkregionen erstellen. für andere erweiterte Enterprise-VoIP-Features werden dieselben netzwerkregionen verwendet.</span><span class="sxs-lookup"><span data-stu-id="a0925-108">For example, if you have already created network regions for one Voice feature, you do not need to create new network regions; other advanced Enterprise Voice features will use those same network regions.</span></span> <span data-ttu-id="a0925-109">Sie müssen jedoch möglicherweise eine vorhandene Definition einer Netzwerkregion ändern, um funktionsspezifische Einstellungen anzuwenden.</span><span class="sxs-lookup"><span data-stu-id="a0925-109">You may, however, need to modify an existing network region definition to apply feature-specific settings.</span></span> <span data-ttu-id="a0925-110">Wenn Sie z. B. Netzwerkregionen für E9-1-1 erstellt haben (denen kein zentraler Standort zugeordnet werden muss) und Sie zu einem späteren Zeitpunkt die Anrufsteuerung bereitstellen, müssen Sie die Definitionen der Netzwerkregionen ändern und einen zentralen Standort angeben.</span><span class="sxs-lookup"><span data-stu-id="a0925-110">For example, if you have created network regions for E9-1-1 (which do not require an associated central site) and you then deploy call admission control, you need to modify the network region definitions to specify a central site.</span></span> <span data-ttu-id="a0925-111">Ausführliche Informationen finden Sie unter [Konfigurieren von netzwerkregionen für CAC in lync Server 2013](lync-server-2013-configure-network-regions-for-cac.md).</span><span class="sxs-lookup"><span data-stu-id="a0925-111">For details, see [Configure network regions for CAC in Lync Server 2013](lync-server-2013-configure-network-regions-for-cac.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="a0925-112">Alle funktionsspezifischen Anforderungen für Netzwerkbereichs Definitionen sind in den Bereitstellungsthemen für das Feature dokumentiert.</span><span class="sxs-lookup"><span data-stu-id="a0925-112">Any feature-specific requirements for network region definitions are documented in the Deployment topics for the feature.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a0925-113">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a0925-113">In This Section</span></span>

  - [<span data-ttu-id="a0925-114">Anzeigen von Netzwerk Regionsinformationen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0925-114">Viewing network region information in Lync Server 2013</span></span>](lync-server-2013-viewing-network-region-information.md)

  - [<span data-ttu-id="a0925-115">Erstellen oder Ändern von netzwerkregionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0925-115">Creating or modifying network regions in Lync Server 2013</span></span>](lync-server-2013-creating-or-modifying-network-regions.md)

  - [<span data-ttu-id="a0925-116">Löschen vorhandener netzwerkregionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0925-116">Deleting existing network regions in Lync Server 2013</span></span>](lync-server-2013-deleting-existing-network-regions.md)

</div>

<div>

## <a name="reference"></a><span data-ttu-id="a0925-117">Referenz</span><span class="sxs-lookup"><span data-stu-id="a0925-117">Reference</span></span>

[<span data-ttu-id="a0925-118">Bereitstellen von erweiterten Enterprise-VoIP-Features in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a0925-118">Deploying advanced Enterprise Voice features in Lync Server 2013</span></span>](lync-server-2013-deploying-advanced-enterprise-voice-features.md)

<span data-ttu-id="a0925-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a0925-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

