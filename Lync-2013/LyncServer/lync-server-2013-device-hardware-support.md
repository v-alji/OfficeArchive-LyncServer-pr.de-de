---
title: 'Lync Server 2013: Unterstützte Gerätehardware'
description: Unterstützung für lync Server 2013-Gerätehardware.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device hardware support
ms:assetid: ba07ca91-32b4-49cf-801c-47a2d1d96e18
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412908(v=OCS.15)
ms:contentKeyID: 48185222
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cd03936d35fbc3a639a3ba4596a4357e8e379719
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429451"
---
# <a name="device-hardware-support-in-lync-server-2013"></a><span data-ttu-id="6833d-103">Unterstützte Gerätehardware in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="6833d-103">Device hardware support in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="6833d-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="6833d-104">

<span> </span></span></span>

<span data-ttu-id="6833d-105">_**Letztes Änderungsdatum des Themas:** 2012-12-14_</span><span class="sxs-lookup"><span data-stu-id="6833d-105">_**Topic Last Modified:** 2012-12-14_</span></span>

<span data-ttu-id="6833d-106">Bevor Sie IP-Telefone und analoge Geräte bereitstellen, müssen bestimmte Hardwarekonfigurationen vorhanden sein.</span><span class="sxs-lookup"><span data-stu-id="6833d-106">Specific hardware configurations must be in place before you deploy IP phones and analog devices.</span></span>

<span data-ttu-id="6833d-107">IP-Telefone mit lync Phone Edition-Unterstützung für die Verbindungsschicht Erkennung Protocol-Media Endpunkt Ermittlung (LLDP-MED) und Power over Ethernet (PoE).</span><span class="sxs-lookup"><span data-stu-id="6833d-107">IP phones running Lync Phone Edition support Link Layer Discovery Protocol-Media Endpoint Discovery (LLDP-MED) and Power over Ethernet (PoE).</span></span> <span data-ttu-id="6833d-108">Um die Vorteile von LLDP-MED zu nutzen, muss der Switch IEEE 802.1 ab und ANSI/TIA-1057 unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6833d-108">To take advantage of LLDP-MED, the switch must support IEEE802.1AB and ANSI/TIA-1057.</span></span> <span data-ttu-id="6833d-109">Um Poe nutzen zu können, muss der Switch Poe 802.3 AF oder 802.3 at unterstützen.</span><span class="sxs-lookup"><span data-stu-id="6833d-109">To take advantage of PoE, the switch must support PoE802.3AF or 802.3at.</span></span>

<span data-ttu-id="6833d-110">Um LLDP-MED zu aktivieren, muss der Administrator LLDP über das Console-Fenster Switch aktivieren und die LLDP-MED-Netzwerkrichtlinie mit der korrekten sprach-VLAN-ID festlegen.</span><span class="sxs-lookup"><span data-stu-id="6833d-110">To enable LLDP-MED, the administrator must enable LLDP by using the switch console window and set the LLDP-MED network policy with the correct voice VLAN ID.</span></span>

<span data-ttu-id="6833d-111">Wenn Ihre Bereitstellung analoge Geräte umfasst, müssen Sie außerdem das analoge Gateway für die Verwendung von lync Server konfigurieren, und das Gateway muss eine der folgenden sein:</span><span class="sxs-lookup"><span data-stu-id="6833d-111">In addition, if your deployment includes analog devices, you must configure the analog gateway to use Lync Server, and the gateway must be one of the following:</span></span>

  - <span data-ttu-id="6833d-112">Einen analogen Telefonadapter (ATA)</span><span class="sxs-lookup"><span data-stu-id="6833d-112">An analog telephone adapter (ATA)</span></span>

  - <span data-ttu-id="6833d-113">Ein analoges PSTN-Gateway</span><span class="sxs-lookup"><span data-stu-id="6833d-113">A PSTN analog gateway</span></span>

  - <span data-ttu-id="6833d-114">Eine Survivable-Branch-Appliance mit einem analogen PSTN-Gateway</span><span class="sxs-lookup"><span data-stu-id="6833d-114">A Survivable Branch Appliance that includes a PSTN analog gateway</span></span>

  - <span data-ttu-id="6833d-115">Eine Survivable-Branch-Appliance, die ein PSTN-Gateway enthält, das mit einem ATA kommuniziert</span><span class="sxs-lookup"><span data-stu-id="6833d-115">A Survivable Branch Appliance that includes a PSTN gateway that communicates with an ATA</span></span>

<span data-ttu-id="6833d-116">Informationen zum Konfigurieren eines analogen Gateways finden Sie unter "Planen der Bereitstellung von analogen Geräten" [https://go.microsoft.com/fwlink/p/?LinkId=268537](https://go.microsoft.com/fwlink/p/?linkid=268537) in der lync Server 2010 TechNet-Bibliothek.</span><span class="sxs-lookup"><span data-stu-id="6833d-116">To learn how to configure an analog gateway, see "Planning to Deploy Analog Devices" at [https://go.microsoft.com/fwlink/p/?LinkId=268537](https://go.microsoft.com/fwlink/p/?linkid=268537) in the Lync Server 2010 TechNet Library.</span></span> <span data-ttu-id="6833d-117">(Analoge Geräte funktionieren auf die gleiche Weise in lync Server 2013 wie in lync Server 2010.)</span><span class="sxs-lookup"><span data-stu-id="6833d-117">(Analog devices work the same way in Lync Server 2013 as they do in Lync Server 2010.)</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="6833d-118">Sie können den Schalter für Enhanced 9-1-1 (E9-1-1) konfigurieren, wenn dies vom Switch unterstützt wird.</span><span class="sxs-lookup"><span data-stu-id="6833d-118">You can configure the switch for Enhanced 9-1-1 (E9-1-1), if the switch supports this.</span></span>



<span data-ttu-id="6833d-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="6833d-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

