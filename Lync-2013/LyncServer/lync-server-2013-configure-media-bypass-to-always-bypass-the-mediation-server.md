---
title: 'Lync Server 2013: Konfigurieren der medienumgehung, um den Vermittlungsserver immer zu umgehen'
description: 'Lync Server 2013: Konfigurieren Sie die medienumgehung so, dass der Vermittlungsserver immer umgangen wird.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure media bypass to always bypass the Mediation Server
ms:assetid: 370c4f54-e520-4d77-96a3-84c5e84a9996
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425846(v=OCS.15)
ms:contentKeyID: 48183819
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6b4981c7b12700d2f0bbf0bf05c8a51623bb8ba9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433913"
---
# <a name="configure-media-bypass-in-lync-server-2013-to-always-bypass-the-mediation-server"></a><span data-ttu-id="3ecbb-103">Configure media bypass in Lync Server 2013 to always bypass the Mediation Server</span><span class="sxs-lookup"><span data-stu-id="3ecbb-103">Configure media bypass in Lync Server 2013 to always bypass the Mediation Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3ecbb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3ecbb-104">

<span> </span></span></span>

<span data-ttu-id="3ecbb-105">_**Letztes Änderungsdatum des Themas:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="3ecbb-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="3ecbb-106">In diesem Thema wird davon ausgegangen, dass Sie die medienumgehung für alle trunk-Verbindungen mit einem Peer (einem öffentlichen Switched Telephone Network (PSTN)-Gateway, einer IP-Telefonanlage oder einem Session Border Controller (SBC) bei einem Internet-Telefoniedienstanbieter (ITSP)) für eine bestimmte Website oder einen bestimmten Dienst konfiguriert haben, für die Medien den Vermittlungs Server umgehen sollen.</span><span class="sxs-lookup"><span data-stu-id="3ecbb-106">This topic assumes that you have already configured media bypass for any trunk connections to a peer (a public switched telephone network (PSTN) gateway, an IP-PBX, or a Session Border Controller (SBC) at an Internet Telephony Service Provider (ITSP)) for a specific site or service for which you want media to bypass the Mediation Server.</span></span><BR><span data-ttu-id="3ecbb-107">Sie können Medien nicht so konfigurieren, dass der Vermittlungs Server immer umgangen wird, während die Anrufsteuerung ebenfalls aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="3ecbb-107">You cannot configure media to always bypass the Mediation Server while also enabling call admission control.</span></span> <span data-ttu-id="3ecbb-108">Diese Einstellungen sind nicht kompatibel und sind daher gegenseitig ausschließende Einstellungen in der Benutzeroberfläche der lync Server-Systemsteuerung.</span><span class="sxs-lookup"><span data-stu-id="3ecbb-108">These settings are incompatible and are therefore mutually exclusive settings in the Lync Server Control Panel user interface.</span></span>



</div>

<span data-ttu-id="3ecbb-109">Zusätzlich zum Aktivieren der medienumgehung für einzelne trunk-Verbindungen, die einem Peer zum Vermittlungs Server zugeordnet sind, müssen Sie auch die globalen Einstellungen für die medienumgehung konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="3ecbb-109">In addition to enabling media bypass for individual trunk connections associated with a peer to the Mediation Server, you must also configure global settings for media bypass.</span></span> <span data-ttu-id="3ecbb-110">Wenn Sie die Schritte in diesem Thema zum Konfigurieren globaler Einstellungen für die medienumgehung verwenden, wird davon ausgegangen, dass Sie über eine gute Konnektivität zwischen lync-Endpunkten und allen Peers verfügen, für die Sie die medienumgehung für die trunk-Verbindung konfiguriert haben.</span><span class="sxs-lookup"><span data-stu-id="3ecbb-110">If you use the steps in this topic to configure global settings for media bypass, the assumption is that you have good connectivity between Lync endpoints and any peer for which you configured media bypass on the trunk connection.</span></span>

<span data-ttu-id="3ecbb-111">Wenn Sie keine gute Verbindung zwischen lync Server-Endpunkten und allen Peers mit dem Vermittlungsserver haben, deren jeweilige trunk-Verbindungen für die medienumgehung aktiviert wurden, müssen Sie die globalen Einstellungen für die medienumgehung so konfigurieren, dass Sie bei Verwendung der medienumgehung Website-und Regionsinformationen verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ecbb-111">If you do not have good connectivity between Lync Server endpoints and all peers to the Mediation Server whose respective trunk connections have been enabled for media bypass, you must configure global media bypass settings to use site and region information when employing media bypass.</span></span> <span data-ttu-id="3ecbb-112">Auf diese Weise können Sie festlegen, wann Medien den Vermittlungs Server umgeht.</span><span class="sxs-lookup"><span data-stu-id="3ecbb-112">This allows for more control in determining when media bypasses the Mediation Server.</span></span> <span data-ttu-id="3ecbb-113">Führen Sie dazu die Schritte unter Konfigurieren der [globalen Einstellungen für medienumgehung in lync Server 2013 aus, um Website-und Regionsinformationen zu verwenden](lync-server-2013-configure-media-bypass-global-settings-to-use-site-and-region-information.md) und stattdessen [ein Subnetz mit einer Netzwerk Website in lync Server 2013 zu verknüpfen](lync-server-2013-associate-a-subnet-with-a-network-site.md) .</span><span class="sxs-lookup"><span data-stu-id="3ecbb-113">To do this, use the steps in [Configure media bypass global settings in Lync Server 2013 to use site and region information](lync-server-2013-configure-media-bypass-global-settings-to-use-site-and-region-information.md) and [Associate a subnet with a network site in Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md) instead.</span></span>

<div>

## <a name="to-enable-media-bypass-globally-to-always-bypass-the-mediation-server"></a><span data-ttu-id="3ecbb-114">So aktivieren Sie die Medienumgehung global zur dauerhaften Umgehung des Vermittlungsservers</span><span class="sxs-lookup"><span data-stu-id="3ecbb-114">To Enable Media Bypass Globally to Always Bypass the Mediation Server</span></span>

1.  <span data-ttu-id="3ecbb-115">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="3ecbb-115">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="3ecbb-116">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="3ecbb-116">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="3ecbb-117">Klicken Sie in der linken Navigationsleiste auf **Netzwerkkonfiguration**.</span><span class="sxs-lookup"><span data-stu-id="3ecbb-117">In the left navigation bar, click **Network Configuration**.</span></span>

3.  <span data-ttu-id="3ecbb-118">Doppelklicken Sie in der Liste auf die Konfiguration **Global**.</span><span class="sxs-lookup"><span data-stu-id="3ecbb-118">Double-click the **Global** configuration in the list.</span></span>

4.  <span data-ttu-id="3ecbb-119">Aktivieren Sie auf der Seite **Globale Einstellungen bearbeiten** das Kontrollkästchen **Medienumgehung aktivieren**.</span><span class="sxs-lookup"><span data-stu-id="3ecbb-119">On the **Edit Global Setting** page, select the **Enable media bypass** check box.</span></span>

5.  <span data-ttu-id="3ecbb-120">Klicken Sie auf **Immer umgehen**.</span><span class="sxs-lookup"><span data-stu-id="3ecbb-120">Click **Always bypass**.</span></span>

6.  <span data-ttu-id="3ecbb-121">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="3ecbb-121">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="3ecbb-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ecbb-122">See Also</span></span>


[<span data-ttu-id="3ecbb-123">Konfigurieren der Medienumgehung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3ecbb-123">Configure media bypass in Lync Server 2013</span></span>](lync-server-2013-configure-media-bypass.md)  
[<span data-ttu-id="3ecbb-124">Globale Medien Umgehungs Optionen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3ecbb-124">Global media bypass options in Lync Server 2013</span></span>](lync-server-2013-global-media-bypass-options.md)  
[<span data-ttu-id="3ecbb-125">Medienumgehung und Vermittlungsserver in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3ecbb-125">Media bypass and Mediation Server in Lync Server 2013</span></span>](lync-server-2013-media-bypass-and-mediation-server.md)  


[<span data-ttu-id="3ecbb-126">Planung der Medienumgehung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3ecbb-126">Planning for media bypass in Lync Server 2013</span></span>](lync-server-2013-planning-for-media-bypass.md)  
  

<span data-ttu-id="3ecbb-127"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3ecbb-127"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

