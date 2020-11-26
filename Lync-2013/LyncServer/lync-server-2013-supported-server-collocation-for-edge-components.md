---
title: 'Lync Server 2013: Unterstützte Serverkollokation für Edgekomponenten'
description: 'Lync Server 2013: unterstützte Server Zusammenstellung für Edge-Komponenten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported server collocation for edge components
ms:assetid: 435c4dd8-36af-4b71-9b88-3ffcf0fc5c65
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425934(v=OCS.15)
ms:contentKeyID: 48183978
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7bf253e5210e077ca62b3d00f7f130d54d8392a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423638"
---
# <a name="supported-server-collocation-for-edge-components-in-lync-server-2013"></a><span data-ttu-id="5d9b0-103">Unterstützte Serverkollokation für Edgekomponenten in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5d9b0-103">Supported server collocation for edge components in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5d9b0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5d9b0-104">

<span> </span></span></span>

<span data-ttu-id="5d9b0-105">_**Letztes Änderungsdatum des Themas:** 2012-09-08_</span><span class="sxs-lookup"><span data-stu-id="5d9b0-105">_**Topic Last Modified:** 2012-09-08_</span></span>

<span data-ttu-id="5d9b0-106">Der Zugriffs-Edgedienst, der Webkonferenz-Edgedienst, der A/V-Edgedienst und der XMPP-Proxy Dienst sind auf den Edgeserver verfügbar.</span><span class="sxs-lookup"><span data-stu-id="5d9b0-106">The Access Edge service, Web Conferencing Edge service, A/V Edge service and XMPP Proxy service are collocated on the Edge Servers.</span></span> <span data-ttu-id="5d9b0-107">Die folgenden Server stellen Funktionen bereit, die für den Zugriff durch externe Benutzer erforderlich sind, und müssen als dedizierte Server bereitgestellt werden:</span><span class="sxs-lookup"><span data-stu-id="5d9b0-107">The following servers provide functions needed for external user access and must be deployed as dedicated servers:</span></span>

  - <span data-ttu-id="5d9b0-108">Edgeserver</span><span class="sxs-lookup"><span data-stu-id="5d9b0-108">Edge Server</span></span>

  - <span data-ttu-id="5d9b0-109">Director (optional)</span><span class="sxs-lookup"><span data-stu-id="5d9b0-109">Director (Optional)</span></span>

  - <span data-ttu-id="5d9b0-110">Reverseproxy</span><span class="sxs-lookup"><span data-stu-id="5d9b0-110">Reverse proxy</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="5d9b0-111">Der Reverse-Proxy muss nicht nur für die Bereitstellung von lync Server 2013 dediziert sein.</span><span class="sxs-lookup"><span data-stu-id="5d9b0-111">The reverse proxy does not need to be dedicated to serving only Lync Server 2013.</span></span> <span data-ttu-id="5d9b0-112">So können Sie beispielsweise Dienste bereitstellen, um die lync Server-Webdienste zu veröffentlichen, und gleichzeitig eine veröffentlichte Website für eine andere Website bereitstellen, die überhaupt keine Auswirkungen auf lync Server hat.</span><span class="sxs-lookup"><span data-stu-id="5d9b0-112">For example, you can provide services to publish the Lync Server Web services, and concurrently provide a published Web site for another Web site that has no bearing on Lync Server at all.</span></span> <span data-ttu-id="5d9b0-113">Wenn Sie bereits über einen Reverse Proxy-Server im Umkreisnetzwerk verfügen, um andere Dienste zu unterstützen, können Sie ihn für lync Server 2013 verwenden.</span><span class="sxs-lookup"><span data-stu-id="5d9b0-113">If you already have a reverse proxy server in the perimeter network to support other services, you can use it for Lync Server 2013.</span></span>



<span data-ttu-id="5d9b0-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5d9b0-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

