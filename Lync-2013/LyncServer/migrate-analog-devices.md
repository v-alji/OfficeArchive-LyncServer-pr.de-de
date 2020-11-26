---
title: Migrieren analoger Geräte
description: Migrieren von analogen Geräten.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Migrate analog devices
ms:assetid: ad072916-87ed-4d44-8289-aab87da86250
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ721846(v=OCS.15)
ms:contentKeyID: 49733779
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 63f7f92142fb6a3ced37cded1a223038ec1876d8
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443832"
---
# <a name="migrate-analog-devices"></a><span data-ttu-id="d9518-103">Migrieren analoger Geräte</span><span class="sxs-lookup"><span data-stu-id="d9518-103">Migrate analog devices</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d9518-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d9518-104">

<span> </span></span></span>

<span data-ttu-id="d9518-105">_**Letztes Änderungsdatum des Themas:** 2012-10-16_</span><span class="sxs-lookup"><span data-stu-id="d9518-105">_**Topic Last Modified:** 2012-10-16_</span></span>

<span data-ttu-id="d9518-106">Lync Server bietet Unterstützung für analoge Geräte.</span><span class="sxs-lookup"><span data-stu-id="d9518-106">Lync Server provides support for analog devices.</span></span> <span data-ttu-id="d9518-107">Die unterstützten analogen Geräte sind analoge Audio-Telefone und analoge Faxgeräte.</span><span class="sxs-lookup"><span data-stu-id="d9518-107">Specifically, the supported analog devices are analog audio phones and analog fax machines.</span></span> <span data-ttu-id="d9518-108">Sie können die qualifizierten Gateways so konfigurieren, dass die Verwendung von analogen Geräten in ihrer lync Server-Umgebung unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="d9518-108">You can configure the qualified gateways to support the use of analog devices in your Lync Server environment.</span></span> <span data-ttu-id="d9518-109">Nachdem Sie von lync Server 2010 zu lync Server 2013 migriert haben, müssen Sie auch die Kontaktobjekte migrieren, die den analogen Geräten zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d9518-109">After you migrate from Lync Server 2010 to Lync Server 2013, you must also migrate the contact objects associated with the analog devices.</span></span> <span data-ttu-id="d9518-110">Verwenden Sie die lync Server-Verwaltungsshell, um zuerst alle Kontaktobjekte abzurufen, die mit den analogen Geräten von lync Server 2010 verknüpft sind, und verschieben Sie diese Objekte dann in den lync Server 2013-Pool.</span><span class="sxs-lookup"><span data-stu-id="d9518-110">Use Lync Server Management Shell to first retrieve all contact objects associated with the Lync Server 2010 analog devices, and then move those objects to the Lync Server 2013 pool.</span></span>

<div>

## <a name="to-migrate-analog-devices"></a><span data-ttu-id="d9518-111">So migrieren Sie analoge Geräte</span><span class="sxs-lookup"><span data-stu-id="d9518-111">To migrate analog devices</span></span>

1.  <span data-ttu-id="d9518-112">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="d9518-112">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="d9518-113">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="d9518-113">At the command line, type:</span></span>
    
        Get-CsAnalogDevice -Filter {RegistrarPool -eq "pool01.contoso.net"} | Move-CsAnalogDevice -Target pool02.contoso.net

3.  <span data-ttu-id="d9518-114">Überprüfen Sie, ob alle Kontaktobjekte in den lync Server 2013-Pool verschoben wurden.</span><span class="sxs-lookup"><span data-stu-id="d9518-114">Verify that all contact objects have been moved to the Lync Server 2013 pool.</span></span> <span data-ttu-id="d9518-115">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="d9518-115">At the command line, type:</span></span>
    
        Get-CsAnalogDevice -Filter {RegistrarPool -eq "pool02.contoso.net"}

4.  <span data-ttu-id="d9518-116">Überprüfen Sie, ob alle Kontaktobjekte jetzt dem lync Server 2013-Pool zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="d9518-116">Verify that all the contact objects are now associated with the Lync Server 2013 pool.</span></span>

<span data-ttu-id="d9518-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d9518-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

