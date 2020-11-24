---
title: 'Lync Server 2013: Konfigurieren von IIS'
description: 'Lync Server 2013: Konfigurieren von IIS.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure IIS
ms:assetid: bc4ae8cc-ec0c-42f1-9034-058930e530d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412918(v=OCS.15)
ms:contentKeyID: 48185248
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cdd08e47d05f2e32f14178eaaa3a100f8c445dda
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394771"
---
# <a name="configure-iis-for-lync-server-2013"></a><span data-ttu-id="43a0e-103">Konfigurieren von IIS für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="43a0e-103">Configure IIS for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="43a0e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="43a0e-104">

<span> </span></span></span>

<span data-ttu-id="43a0e-105">_**Letztes Änderungsdatum des Themas:** 2011-12-16_</span><span class="sxs-lookup"><span data-stu-id="43a0e-105">_**Topic Last Modified:** 2011-12-16_</span></span>

<span data-ttu-id="43a0e-106">Zum Konfigurieren der Internetinformationsdienste (IIS) für lync Server 2013 müssen die richtigen Komponenten installiert werden, um die von lync Server 2013 benötigten Webdienste zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="43a0e-106">Configuring Internet Information Services (IIS) for Lync Server 2013 involves installing the correct components to support the Web Services needed by Lync Server 2013.</span></span> <span data-ttu-id="43a0e-107">Details zur Installation von IIS finden Sie unter [IIS-Konfiguration in lync Server 2013](lync-server-2013-iis-configuration.md).</span><span class="sxs-lookup"><span data-stu-id="43a0e-107">For details about installing IIS, see [IIS configuration in Lync Server 2013](lync-server-2013-iis-configuration.md).</span></span> <span data-ttu-id="43a0e-108">Wenn Sie über eine Richtlinie verfügen, mit der der Sicherheitskonfigurations-Assistent auf Servern ausgeführt werden kann, bevor Sie Sie in Betrieb nehmen, oder als typischer Bestandteil ihrer Wartung, lesen Sie [erneutes Aktivieren des Servers, nachdem der Sicherheitskonfigurations-Assistent Ports in IIS geschlossen](lync-server-2013-re-activate-server-after-security-configuration-wizard-closes-ports-in-iis.md) hat, um Informationen zu einem Nebeneffekt der Ausführung des Assistenten zu erhalten, der Ports in einer lync Server 2013 IIS-Konfiguration schließt</span><span class="sxs-lookup"><span data-stu-id="43a0e-108">If you have a policy to run the Security Configuration Wizard on servers before putting them into service or as a typical part of your maintenance, see [Re-activate server after Security Configuration Wizard closes ports in IIS](lync-server-2013-re-activate-server-after-security-configuration-wizard-closes-ports-in-iis.md) for information about a side effect of running the wizard that will close ports on a Lync Server 2013 IIS configuration.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="43a0e-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="43a0e-109">In This Section</span></span>

  - [<span data-ttu-id="43a0e-110">IIS-Konfiguration in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="43a0e-110">IIS configuration in Lync Server 2013</span></span>](lync-server-2013-iis-configuration.md)

  - [<span data-ttu-id="43a0e-111">Erneutes Aktivieren eines Servers, nachdem der Sicherheitskonfigurations-Assistent Ports in IIS schließt</span><span class="sxs-lookup"><span data-stu-id="43a0e-111">Re-activate server after Security Configuration Wizard closes ports in IIS</span></span>](lync-server-2013-re-activate-server-after-security-configuration-wizard-closes-ports-in-iis.md)

<span data-ttu-id="43a0e-112"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="43a0e-112"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

