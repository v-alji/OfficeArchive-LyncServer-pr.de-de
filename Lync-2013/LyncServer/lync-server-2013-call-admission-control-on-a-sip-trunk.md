---
title: 'Lync Server 2013: Anrufsteuerung für einen SIP-Trunk'
description: 'Lync Server 2013: Rufen Sie die Zulassungs Steuerung auf einem SIP-Stamm auf.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call admission control on a SIP trunk
ms:assetid: 7eada098-3d47-4be2-839f-8f87d582efe8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398632(v=OCS.15)
ms:contentKeyID: 48184623
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3667ef4608b221a1607b6bbe0d89d390cb1dd402
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435862"
---
# <a name="call-admission-control-on-a-sip-trunk-in-lync-server-2013"></a><span data-ttu-id="4e5f0-103">Anrufsteuerung für einen SIP-Trunk in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4e5f0-103">Call admission control on a SIP trunk in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4e5f0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4e5f0-104">

<span> </span></span></span>

<span data-ttu-id="4e5f0-105">_**Letztes Änderungsdatum des Themas:** 2012-09-22_</span><span class="sxs-lookup"><span data-stu-id="4e5f0-105">_**Topic Last Modified:** 2012-09-22_</span></span>

<span data-ttu-id="4e5f0-p101">Zur Bereitstellung der Anrufsteuerung für einen SIP-Trunk erstellen Sie einen Netzwerkstandort, der den Anbieter von Internettelefoniediensten repräsentiert. Um Bandbreitenrichtlinienwerte auf den SIP-Trunk anzuwenden, erstellen Sie eine standortübergreifende Richtlinie zwischen dem Netzwerkstandort in Ihrem Unternehmen und dem Netzwerkstandort, der für den Anbieter von Internettelefoniediensten erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="4e5f0-p101">To deploy call admission control (CAC) on a SIP trunk, you create a network site to represent the Internet telephony service provider (ITSP). To apply bandwidth policy values on the SIP trunk, you create an inter-site policy between the network site in your enterprise and the network site that you create to represent the ITSP.</span></span>

<span data-ttu-id="4e5f0-108">Die folgende Abbildung zeigt ein Beispiel für die Bereitstellung der Anrufsteuerung für einen SIP-Trunk.</span><span class="sxs-lookup"><span data-stu-id="4e5f0-108">The following figure shows an example CAC deployment on a SIP trunk.</span></span>

<span data-ttu-id="4e5f0-109">**Konfiguration der Anrufsteuerung für einen SIP-Trunk**</span><span class="sxs-lookup"><span data-stu-id="4e5f0-109">**CAC configuration on a SIP trunk**</span></span>

<span data-ttu-id="4e5f0-110">![Anrufsteuerung – SIP-Trunking (Diagramm)](images/Gg398632.276c0d8f-1dd5-4883-8499-c202399ddbe9(OCS.15).jpg "Anrufsteuerung – SIP-Trunking (Diagramm)")</span><span class="sxs-lookup"><span data-stu-id="4e5f0-110">![Call Admission Control SIP Trunking diagram](images/Gg398632.276c0d8f-1dd5-4883-8499-c202399ddbe9(OCS.15).jpg "Call Admission Control SIP Trunking diagram")</span></span>

<span data-ttu-id="4e5f0-111">Zur Konfiguration der Anrufsteuerung für einen SIP-Trunk müssen Sie während der Bereitstellung der Anrufsteuerung die folgenden Aufgaben ausführen:</span><span class="sxs-lookup"><span data-stu-id="4e5f0-111">To configure CAC on a SIP trunk, you will have to perform the following tasks during CAC deployment:</span></span>

1.  <span data-ttu-id="4e5f0-112">Erstellen eines Netzwerkstandorts, der den Anbieter von Internettelefoniediensten repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="4e5f0-112">Create a network site to represent the ITSP.</span></span> <span data-ttu-id="4e5f0-113">Zuordnen des Netzwerkstandorts zu einer geeigneten Netzwerkregion und Zuweisen eines Bandbreitenwerts von Null für Audio und Video an diesem Netzwerkstandort.</span><span class="sxs-lookup"><span data-stu-id="4e5f0-113">Associate the network site to an appropriate network region, and allocate bandwidth of zero for audio and video for this network site.</span></span> <span data-ttu-id="4e5f0-114">Ausführliche Informationen finden Sie unter [Konfigurieren von Netzwerk Websites für CAC in lync Server 2013](lync-server-2013-configure-network-sites-for-cac.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="4e5f0-114">For details, see [Configure network sites for CAC in Lync Server 2013](lync-server-2013-configure-network-sites-for-cac.md) in the Deployment documentation.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="4e5f0-115">Für den Anbieter von Internettelefoniediensten ist diese Netzwerkstandortkonfiguration nicht funktionsfähig.</span><span class="sxs-lookup"><span data-stu-id="4e5f0-115">For the ITSP, this network site configuration is not functional.</span></span> <span data-ttu-id="4e5f0-116">Die Bandbreitenrichtlinienwerte werden tatsächlich in Schritt 2 angewendet.</span><span class="sxs-lookup"><span data-stu-id="4e5f0-116">Bandwidth policy values are actually applied in step 2.</span></span>

    
    </div>

2.  <span data-ttu-id="4e5f0-117">Erstellen Sie einen Inter-Site-Link für den SIP-Trunk unter Verwendung der relevanten Parameterwerte für die Website, die Sie in Schritt 1 erstellt haben.</span><span class="sxs-lookup"><span data-stu-id="4e5f0-117">Create an inter-site link for the SIP trunk using the relevant parameter values for the site you created in step 1.</span></span> <span data-ttu-id="4e5f0-118">Verwenden Sie beispielsweise den Namen der Netzwerk Website in Ihrem Unternehmen als Wert des NetworkSiteID1-Parameters und die ITSP-Netzwerk Website als Wert des NetworkSiteID2-Parameters.</span><span class="sxs-lookup"><span data-stu-id="4e5f0-118">For example, use the name of the network site in your enterprise as the value of the NetworkSiteID1 parameter, and the ITSP network site as the value of the NetworkSiteID2 parameter.</span></span> <span data-ttu-id="4e5f0-119">Ausführliche Informationen finden Sie unter [Erstellen von Netzwerk-Standortrichtlinien in lync Server 2013](lync-server-2013-create-network-intersite-policies.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="4e5f0-119">For details, see [Create network intersite policies in Lync Server 2013](lync-server-2013-create-network-intersite-policies.md) in the Deployment documentation.</span></span> <span data-ttu-id="4e5f0-120">Weitere Informationen finden Sie auch in der Dokumentation zur lync Server-Verwaltungsshell für das New-CsNetworkInterSitePolicy-Cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4e5f0-120">Also see the Lync Server Management Shell documentation for the New-CsNetworkInterSitePolicy cmdlet.</span></span>

3.  <span data-ttu-id="4e5f0-121">Lassen Sie sich vom Anbieter der Internettelefoniedienste die IP-Adresse des SBC-Medienendpunkts (Session Border Controller) geben.</span><span class="sxs-lookup"><span data-stu-id="4e5f0-121">Get the IP address of the Session Border Controller’s (SCB) Media Termination Point from your ITSP.</span></span> <span data-ttu-id="4e5f0-122">Fügen Sie diese IP-Adresse mit der Subnetzmaske 32 zu dem Netzwerkstandort hinzu, der den Anbieter von Internettelefoniediensten repräsentiert.</span><span class="sxs-lookup"><span data-stu-id="4e5f0-122">Add that IP address with a subnet mask of 32 to the network site that represents the ITSP.</span></span> <span data-ttu-id="4e5f0-123">Ausführliche Informationen finden Sie unter [Zuordnen eines Subnetzes zu einer Netzwerk Website in lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md).</span><span class="sxs-lookup"><span data-stu-id="4e5f0-123">For details, see [Associate a subnet with a network site in Lync Server 2013](lync-server-2013-associate-a-subnet-with-a-network-site.md).</span></span>

<span data-ttu-id="4e5f0-124"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4e5f0-124"></div>

<span> </span>

</div>

</div>

</span></span></div>

