---
title: 'Lync Server 2013: Ändern eines Trunks im Topologie-Generator'
description: 'Lync Server 2013: Ändern eines Trunks im Topologie-Generator'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify a trunk in Topology Builder
ms:assetid: 81055a82-c6f8-47b2-9779-223b1d842f36
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688110(v=OCS.15)
ms:contentKeyID: 49733709
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5f453997664dbe3048a7aa915732b4d95a932dd9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425542"
---
# <a name="modify-a-trunk-in-topology-builder-in-lync-server-2013"></a><span data-ttu-id="4d152-103">Ändern eines Trunks im Topologie-Generator in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4d152-103">Modify a trunk in Topology Builder in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4d152-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4d152-104">

<span> </span></span></span>

<span data-ttu-id="4d152-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="4d152-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="4d152-106">Führen Sie die folgenden Schritte aus, um die IP-Adresse des alternativen Mediums und den alternativen Bypass-Bezeichner eines Trunks zu ändern.</span><span class="sxs-lookup"><span data-stu-id="4d152-106">Follow these steps to modify the alternate media IP address and alternate bypass identifier of a trunk.</span></span>

<div>

## <a name="to-modify-the-alternate-media-ip-address-of-a-trunk"></a><span data-ttu-id="4d152-107">So ändern Sie die Alternative Medien-IP-Adresse eines Trunks</span><span class="sxs-lookup"><span data-stu-id="4d152-107">To Modify the Alternate Media IP Address of a Trunk</span></span>

1.  <span data-ttu-id="4d152-108">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="4d152-108">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="4d152-109">Führen Sie das Set-CsPstnGateway-Cmdlet aus, und ändern Sie das AlternateBypassId-Feld in der lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="4d152-109">Run the Set-CsPstnGateway cmdlet and modify the AlternateBypassId field in the Lync Server Management Shell.</span></span>
    
        Set-CsPstnGateway -Identity "PstnGateway:<peer FQDN> -RepresentativeMediaIP <IP address>

</div>

<div>

## <a name="to-modify-the-alternate-bypassid-of-a-trunk"></a><span data-ttu-id="4d152-110">So ändern Sie die Alternative Bypass-Nr eines Trunks</span><span class="sxs-lookup"><span data-stu-id="4d152-110">To Modify the Alternate BypassID of a Trunk</span></span>

1.  <span data-ttu-id="4d152-111">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="4d152-111">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="4d152-112">Führen Sie das Set-CsPstnGateway-Cmdlet aus, und ändern Sie das AlternateBypassId-Feld in der lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="4d152-112">Run the Set-CsPstnGateway cmdlet and modify the AlternateBypassId field in the Lync Server Management Shell.</span></span>
    
        Set-CsPstnGateway -Identity "PstnGateway:<peer FQDN> -AlternateBypassID <identifier>

<span data-ttu-id="4d152-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4d152-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

