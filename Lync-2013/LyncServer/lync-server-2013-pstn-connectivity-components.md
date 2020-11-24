---
title: 'Lync Server 2013: PSTN-Verbindungskomponenten'
description: 'Lync Server 2013: PSTN-Verbindungskomponenten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: PSTN connectivity components
ms:assetid: 6b2a3f7d-760f-4f09-8432-312c98a7e6b7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398504(v=OCS.15)
ms:contentKeyID: 48184408
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c2ae5a6a7bc5db1cd7a23c44719d7123a624317d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394603"
---
# <a name="pstn-connectivity-components-in-lync-server-2013"></a><span data-ttu-id="0e83e-103">Komponenten für PSTN-Konnektivität in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0e83e-103">PSTN connectivity components in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0e83e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0e83e-104">

<span> </span></span></span>

<span data-ttu-id="0e83e-105">_**Letztes Änderungsdatum des Themas:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="0e83e-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="0e83e-106">Eine VoIP-Lösung für Unternehmen muss ein- und ausgehende PSTN-Anrufe (Public Switched Telephone Network, Telefonfestnetz) ermöglichen, ohne dass die Dienstqualität (Quality of Service, QoS) in irgendeiner Weise beeinträchtigt wird.</span><span class="sxs-lookup"><span data-stu-id="0e83e-106">An enterprise-grade VoIP solution must provide for calls to and from the public switched telephone network (PSTN) without any decline in Quality of Service (QoS).</span></span> <span data-ttu-id="0e83e-107">Außerdem sollte die zugrunde liegende Technologie für Benutzer, die Anrufe tätigen und empfangen, unbemerkt im Hintergrund arbeiten.</span><span class="sxs-lookup"><span data-stu-id="0e83e-107">In addition, users should not be aware of the underlying technology when they place and receive calls.</span></span> <span data-ttu-id="0e83e-108">Aus Sicht des Benutzers sollte ein Anruf zwischen der Enterprise-VoIP-Infrastruktur und dem PSTN wie nur eine weitere SIP-Sitzung aussehen.</span><span class="sxs-lookup"><span data-stu-id="0e83e-108">From the user's perspective, a call between the Enterprise Voice infrastructure and the PSTN should seem like just another SIP session.</span></span>

<span data-ttu-id="0e83e-109">Für PSTN-Verbindungen können Sie entweder einen SIP-Trunk oder ein PSTN-Gateway bereitstellen – mit Nebenstellenanlage (was auch als direkte SIP-Verbindung bezeichnet wird) oder ohne Nebenstellenanlage.</span><span class="sxs-lookup"><span data-stu-id="0e83e-109">For PSTN connections, you can either deploy a SIP trunk or a PSTN gateway (with a PBX, also known as a Direct SIP link, or without a PBX).</span></span>

<div>

## <a name="sip-trunking"></a><span data-ttu-id="0e83e-110">SIP-Trunking</span><span class="sxs-lookup"><span data-stu-id="0e83e-110">SIP Trunking</span></span>

<span data-ttu-id="0e83e-111">Als Alternative zur Verwendung von PSTN-Gateways können Sie Ihre Enterprise-VoIP-Lösung mithilfe von SIP-Trunking mit dem PSTN verbinden.</span><span class="sxs-lookup"><span data-stu-id="0e83e-111">As an alternative to using PSTN gateways, you can connect your Enterprise Voice solution to the PSTN by using SIP trunking.</span></span> <span data-ttu-id="0e83e-112">Mit SIP-Trunking sind folgende Szenarien möglich:</span><span class="sxs-lookup"><span data-stu-id="0e83e-112">SIP trunking enables the following scenarios:</span></span>

  - <span data-ttu-id="0e83e-113">Ein Benutzer eines Unternehmens innerhalb oder außerhalb der Unternehmensfirewall kann ein Orts- oder Ferngespräch über eine E.164-kompatible Nummer führen, das im Telefonfestnetz als Dienst des entsprechenden Dienstanbieters beendet wird.</span><span class="sxs-lookup"><span data-stu-id="0e83e-113">An enterprise user inside or outside the corporate firewall can make a local or long-distance call specified by an E.164-compliant number that is terminated on the PSTN as a service of the corresponding service provider.</span></span>

  - <span data-ttu-id="0e83e-114">Jeder PSTN-Teilnehmer (Public Switched Telephone Network, Telefonfestnetz) kann einen Unternehmensbenutzer innerhalb oder außerhalb der Unternehmensfirewall erreichen, indem er eine DID-Nummer (Direct Inward Dialing) wählt, die dem Unternehmensbenutzer zugeordnet ist.</span><span class="sxs-lookup"><span data-stu-id="0e83e-114">Any PSTN subscriber can contact an enterprise user inside or outside the corporate firewall by dialing a Direct Inward Dialing (DID) number associated with that enterprise user.</span></span>

<span data-ttu-id="0e83e-115">Für diese Bereitstellungslösung ist ein SIP-Trunking-Dienstanbieter erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0e83e-115">The use of this deployment solution requires a SIP trunking service provider.</span></span>

</div>

<div>

## <a name="pstn-gateways"></a><span data-ttu-id="0e83e-116">PSTN-Gateways</span><span class="sxs-lookup"><span data-stu-id="0e83e-116">PSTN gateways</span></span>

<span data-ttu-id="0e83e-117">PSTN-Gateways sind Geräte von Drittanbietern, die Signal-und Medienübertragung zwischen der Enterprise-VoIP-Infrastruktur und einem PSTN oder einer Telefonanlage übersetzen.</span><span class="sxs-lookup"><span data-stu-id="0e83e-117">PSTN gateways are third-party devices that translate signaling and media between the Enterprise Voice infrastructure and a PSTN or a PBX.</span></span> <span data-ttu-id="0e83e-118">PSTN-Gateways arbeiten mit dem Vermittlungs Server zusammen, um einem Enterprise-VoIP-Client einen PSTN-oder PBX-Anruf zu präsentieren.</span><span class="sxs-lookup"><span data-stu-id="0e83e-118">PSTN gateways work with the Mediation Server to present a PSTN or PBX call to an Enterprise Voice client.</span></span> <span data-ttu-id="0e83e-119">Der Vermittlungs Server stellt auch Anrufe von Enterprise-VoIP-Clients an das PSTN-Gateway zum Weiterleiten an das PSTN oder die Telefonanlage vor.</span><span class="sxs-lookup"><span data-stu-id="0e83e-119">The Mediation Server also presents calls from Enterprise Voice clients to the PSTN gateway for routing to the PSTN or PBX.</span></span> <span data-ttu-id="0e83e-120">Eine Liste der Partner, die mit Microsoft zusammenarbeiten, um Geräte bereitzustellen, die mit lync Server funktionieren, finden Sie auf der Microsoft Unified Communications Partners-Website unter [https://go.microsoft.com/fwlink/p/?linkId=202836](https://go.microsoft.com/fwlink/p/?linkid=202836) .</span><span class="sxs-lookup"><span data-stu-id="0e83e-120">For a list of partners who work with Microsoft to provide devices that work with Lync Server, see the Microsoft Unified Communications Partners website at [https://go.microsoft.com/fwlink/p/?linkId=202836](https://go.microsoft.com/fwlink/p/?linkid=202836).</span></span>

</div>

<div>

## <a name="private-branch-exchanges"></a><span data-ttu-id="0e83e-121">Nebenstellenanlagen</span><span class="sxs-lookup"><span data-stu-id="0e83e-121">Private Branch Exchanges</span></span>

<span data-ttu-id="0e83e-122">Wenn Sie über eine vorhandene VoIP-Infrastruktur verfügen, die eine PBX (Private Branch Exchange) verwendet, können Sie Ihre Telefonanlage mit lync Server Enterprise-VoIP verwenden.</span><span class="sxs-lookup"><span data-stu-id="0e83e-122">If you have an existing voice infrastructure that uses a private branch exchange (PBX), you can use your PBX with Lync Server Enterprise Voice.</span></span>

<span data-ttu-id="0e83e-123">Die unterstützten Enterprise-VoIP-Integrationsszenarien sind wie folgt:</span><span class="sxs-lookup"><span data-stu-id="0e83e-123">The supported Enterprise Voice-PBX integration scenarios are as follows:</span></span>

  - <span data-ttu-id="0e83e-124">IP-Telefonanlage, die die medienumgehung mit einem Vermittlungs Server unterstützt.</span><span class="sxs-lookup"><span data-stu-id="0e83e-124">IP-PBX that supports media bypass, with a Mediation Server.</span></span>

  - <span data-ttu-id="0e83e-125">IP-Nebenstellenanlage, die ein eigenständiges PSTN-Gateway erfordert.</span><span class="sxs-lookup"><span data-stu-id="0e83e-125">IP-PBX that requires a stand-alone PSTN gateway.</span></span>

  - <span data-ttu-id="0e83e-126">TDM-Nebenstellenanlage (Time Division Multiplexing) mit eigenständigem PSTN-Gateway.</span><span class="sxs-lookup"><span data-stu-id="0e83e-126">Time division multiplexing (TDM) PBX, with a stand-alone PSTN gateway.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="0e83e-127">Die Medienumgehung funktioniert nicht mit allen PSTN-Gateways, IP-Nebenstellenanlagen oder SBCs.</span><span class="sxs-lookup"><span data-stu-id="0e83e-127">Media bypass will not interoperate with every PSTN gateway, IP-PBX, and SBC.</span></span> <span data-ttu-id="0e83e-128">Microsoft hat eine Reihe von PSTN-Gateways und SBCs mit zertifizierten Partnern getestet und einige Tests mit IP-Nebenstellenanlagen von Cisco durchgeführt.</span><span class="sxs-lookup"><span data-stu-id="0e83e-128">Microsoft has tested a set of PSTN gateways and SBCs with certified partners and has done some testing with Cisco IP-PBXs.</span></span> <span data-ttu-id="0e83e-129">Die medienumgehung wird nur mit Produkten und Versionen unterstützt, die unter Unified Communications Open Interoperability Program – lync Server unter aufgeführt sind <A href="https://go.microsoft.com/fwlink/p/?linkid=214406">https://go.microsoft.com/fwlink/p/?linkId=214406</A> .</span><span class="sxs-lookup"><span data-stu-id="0e83e-129">Media bypass is supported only with products and versions listed on Unified Communications Open Interoperability Program – Lync Server at <A href="https://go.microsoft.com/fwlink/p/?linkid=214406">https://go.microsoft.com/fwlink/p/?linkId=214406</A>.</span></span>



</div>

<span data-ttu-id="0e83e-130">Details zu Partnern, die Enterprise-VoIP-Lösungen anbieten, finden Sie auf der Microsoft Unified Communications Partners-Website unter [https://go.microsoft.com/fwlink/p/?linkId=202836](https://go.microsoft.com/fwlink/p/?linkid=202836) .</span><span class="sxs-lookup"><span data-stu-id="0e83e-130">For details about partners who offer Enterprise Voice solutions, see the Microsoft Unified Communications Partners website at [https://go.microsoft.com/fwlink/p/?linkId=202836](https://go.microsoft.com/fwlink/p/?linkid=202836).</span></span>

<span data-ttu-id="0e83e-131">Details zu Partnern, die Enterprise-VoIP-Hardwarelösungen anbieten, einschließlich PSTN-Gateways, finden Sie auf der Microsoft Unified Communications Partners-Website [https://go.microsoft.com/fwlink/p/?linkId=202836](https://go.microsoft.com/fwlink/p/?linkid=202836) .</span><span class="sxs-lookup"><span data-stu-id="0e83e-131">For details about partners who offer Enterprise Voice hardware solutions, including PSTN gateways, see the Microsoft Unified Communications Partners website [https://go.microsoft.com/fwlink/p/?linkId=202836](https://go.microsoft.com/fwlink/p/?linkid=202836).</span></span>

<span data-ttu-id="0e83e-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0e83e-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

