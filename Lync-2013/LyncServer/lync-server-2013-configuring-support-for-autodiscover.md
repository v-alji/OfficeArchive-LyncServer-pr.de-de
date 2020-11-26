---
title: 'Lync Server 2013: Konfigurieren der Unterstützung für AutoErmittlung'
description: 'Lync Server 2013: Konfigurieren der Unterstützung für AutoErmittlung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring support for Autodiscover
ms:assetid: 3a266456-69a0-4539-ba99-d388b83799a8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945622(v=OCS.15)
ms:contentKeyID: 51541463
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 23991f2f9467035f4ba461ff1b6a84fa8ed1a11d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432611"
---
# <a name="configuring-support-for-autodiscover-in-lync-server-2013"></a><span data-ttu-id="c5d75-103">Konfigurieren der Unterstützung für die AutoErmittlung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c5d75-103">Configuring support for Autodiscover in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c5d75-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c5d75-104">

<span> </span></span></span>

<span data-ttu-id="c5d75-105">_**Letztes Änderungsdatum des Themas:** 2013-01-21_</span><span class="sxs-lookup"><span data-stu-id="c5d75-105">_**Topic Last Modified:** 2013-01-21_</span></span>

<span data-ttu-id="c5d75-106">Der **AutoErmittlungsdienst** für lync Server-Webdienste erschien zunächst im kumulativen Update für lync Server 2010: November 2011.</span><span class="sxs-lookup"><span data-stu-id="c5d75-106">The Lync Server web services **Autodiscover service** first appeared in the Lync Server 2010 Cumulative Update: November 2011.</span></span> <span data-ttu-id="c5d75-107">Dieses Update wurde von der ersten Version von lync Mobile-Clients begleitet.</span><span class="sxs-lookup"><span data-stu-id="c5d75-107">This update was accompanied by the initial release of Lync Mobile clients.</span></span> <span data-ttu-id="c5d75-108">Der AutoErmittlungsdienst hat die Mobilitätsdienste, den so genannten MCX-Dienst, verfügbar gemacht.</span><span class="sxs-lookup"><span data-stu-id="c5d75-108">The autodiscover service exposed the mobility services, known as the Mcx service.</span></span>

<span data-ttu-id="c5d75-109">Der AutoErmittlungsdienst fungiert als einzelner Standort für alle Clients, um Informationen zu den verfügbaren Diensten und Features anzufordern und zu erfahren, wie Sie sich an die Mitarbeiter wenden können – entweder durch einen vollqualifizierten Domänennamen oder einen webuniform Resource Locator-Verweis.</span><span class="sxs-lookup"><span data-stu-id="c5d75-109">The autodiscover service acts as a single location for all clients to request information on what services and features are available, and how to contact the sevices – either by a fully qualified domain name or a web uniform resource locator reference.</span></span> <span data-ttu-id="c5d75-110">Die AutoErmittlung macht eine Reihe von Features verfügbar, und jeder Client stellt Anforderungen basierend auf den Features, die der Client verwenden kann, zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="c5d75-110">Autodiscover exposes a number of features, and each client will make requests based on the features that the client can use.</span></span> <span data-ttu-id="c5d75-111">Beispielsweise wird ein lync 2013-Desktop Client autodiscvoer verwenden, um die externen Webdienste zu ermitteln, verwendet aber nicht die Mobilitätsdienste (MCX).</span><span class="sxs-lookup"><span data-stu-id="c5d75-111">For example, a desktop Lync 2013 client will use autodiscvoer to determine the external web services, but will not use the mobility (Mcx) services.</span></span> <span data-ttu-id="c5d75-112">Damit Ihre Clients die für Sie verfügbaren Features richtig definieren und aktivieren können, sollten die Szenarien definiert werden, die es einem Client ermöglichen, Auto Ermittlungs Einträge effektiv zu finden und zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="c5d75-112">To properly define and enable your clients to use the features available to them, the scenarios that allow a client to effectively find and use autodiscover entries should be defined.</span></span> <span data-ttu-id="c5d75-113">Zur Verwendung von autodoscover erfordert Ihre Bereitstellung, dass ein Reverse Proxy die lync Server-Webdienste veröffentlicht, dass DNS-Einträge für das Auflösen von DNS-Abfragen für den lync Server-AutoErmittlungsdienst und lync Server-Webdienste konfiguriert sind und dass die Zertifikatdienste für Ihr spezifisches Szenario ordnungsgemäß konfiguriert sind.</span><span class="sxs-lookup"><span data-stu-id="c5d75-113">To use autodoscover, your deployment requires that a reverse proxy publishes the Lync Server web services, that DNS records are configured to resolve DNS queries for the Lync Server autodiscover service and Lync Server web services, and that certificate services are properly configured for your specific scenario.</span></span>

<div>


> [!TIP]  
> <span data-ttu-id="c5d75-114">Technische Informationen dazu, welche Elemente in der Auto Ermittlungsanforderung/-Antwort ausgeführt werden, finden Sie unter <A href="lync-server-2013-understanding-autodiscover.md">Grundlegendes zu AutoErmittlung in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="c5d75-114">For technical details on what the elements within the autodiscover request/response do, see <A href="lync-server-2013-understanding-autodiscover.md">Understanding Autodiscover in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="c5d75-115">Die folgenden Informationen und Tabellen definieren pro Szenario, welche Konfigurationen (sofern vorhanden) Sie implementieren müssen, um die vollständige und effektive Verwendung des AutoErmittlungsdiensts bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="c5d75-115">The following information and tables define, per scenario, what configurations (if any) you need to implement to provide the full and effective use of the autodiscover service.</span></span> <span data-ttu-id="c5d75-116">Die Informationen in den folgenden Themen sind spezifisch für Microsoft lync Server 2013.</span><span class="sxs-lookup"><span data-stu-id="c5d75-116">The information in the following topics is specific to Microsoft Lync Server 2013.</span></span> <span data-ttu-id="c5d75-117">Wenn Sie nach Anleitungen zum Planen der Mobilität für lync Server 2010 suchen, lesen Sie [https://go.microsoft.com/fwlink/?LinkId=275113](https://go.microsoft.com/fwlink/?linkid=275113) .</span><span class="sxs-lookup"><span data-stu-id="c5d75-117">If you are looking for guidance on how to plan Mobility for Lync Server 2010, see [https://go.microsoft.com/fwlink/?LinkId=275113](https://go.microsoft.com/fwlink/?linkid=275113).</span></span> <span data-ttu-id="c5d75-118">Informationen zum Bereitstellen von Mobility für lync Server 2010 finden Sie unter [https://go.microsoft.com/fwlink/?LinkId=275114](https://go.microsoft.com/fwlink/?linkid=275114)</span><span class="sxs-lookup"><span data-stu-id="c5d75-118">To deploy Mobility for Lync Server 2010, see [https://go.microsoft.com/fwlink/?LinkId=275114](https://go.microsoft.com/fwlink/?linkid=275114)</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c5d75-119">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c5d75-119">In This Section</span></span>

  - [<span data-ttu-id="c5d75-120">Konfigurieren von DNS für die AutoErmittlung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c5d75-120">Configuring DNS for Autodiscover in Lync Server 2013</span></span>](lync-server-2013-configuring-dns-for-autodiscover.md)

  - [<span data-ttu-id="c5d75-121">Konfigurieren von Zertifikaten für die AutoErmittlung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c5d75-121">Configuring certificates for Autodiscover in Lync Server 2013</span></span>](lync-server-2013-configuring-certificates-for-autodiscover.md)

  - [<span data-ttu-id="c5d75-122">Konfigurieren eines Reverse-Proxys für die AutoErmittlung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c5d75-122">Configuring a reverse proxy for Autodiscover in Lync Server 2013</span></span>](lync-server-2013-configuring-a-reverse-proxy-for-autodiscover.md)

  - [<span data-ttu-id="c5d75-123">Konfigurieren der AutoErmittlung in lync Server 2013 für hybridbereitstellungen</span><span class="sxs-lookup"><span data-stu-id="c5d75-123">Configuring Autodiscover in Lync Server 2013 for hybrid deployments</span></span>](lync-server-2013-configuring-autodiscover-for-hybrid-deployments.md)

<span data-ttu-id="c5d75-124"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c5d75-124"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

