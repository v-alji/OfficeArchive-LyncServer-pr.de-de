---
title: 'Lync Server 2013: Entwerfen der Topologie mithilfe des Planungstools'
description: 'Lync Server 2013: Entwerfen der Topologie mithilfe des Planungstools'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Designing the topology by using the Planning Tool
ms:assetid: 2a352f62-c5cb-4ef1-9aa9-7f0c1ab47455
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558631(v=OCS.15)
ms:contentKeyID: 51541454
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fcc10d09d7b8b815e2b4924d06c10de23c14236b
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429531"
---
# <a name="designing-the-topology-for-lync-server-2013-by-using-the-planning-tool"></a><span data-ttu-id="24820-103">Entwerfen der Topologie für lync Server 2013 mithilfe des Planungstools</span><span class="sxs-lookup"><span data-stu-id="24820-103">Designing the topology for Lync Server 2013 by using the Planning Tool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="24820-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="24820-104">

<span> </span></span></span>

<span data-ttu-id="24820-105">_**Letztes Änderungsdatum des Themas:** 2013-03-04_</span><span class="sxs-lookup"><span data-stu-id="24820-105">_**Topic Last Modified:** 2013-03-04_</span></span>

<span data-ttu-id="24820-106">Das Planungstool für Microsoft lync Server 2013 ist ein Assistenten gesteuertes, Interview ähnliches Tool, in dem Fragen zur lync Server 2013-Topologie gestellt werden, die Sie entwerfen.</span><span class="sxs-lookup"><span data-stu-id="24820-106">The Microsoft Lync Server 2013, Planning Tool is a wizard driven, interview-like tool that asks questions about the Lync Server 2013 topology that you are designing.</span></span> <span data-ttu-id="24820-107">Das Planungs Tool verwendet die bereitgestellten Informationen in Verbindung mit den bevorzugten Methoden für Topologie-Design und-Kapazität, um eine empfohlene Topologie basierend auf den bereitgestellten Antworten darzustellen.</span><span class="sxs-lookup"><span data-stu-id="24820-107">The Planning Tool uses the information supplied, coupled with preferred practices for topology design and capacity, to present a recommended topology based on the answers supplied.</span></span> <span data-ttu-id="24820-108">Sie können das Planungs Tool aus dem Microsoft Downloads Center () herunterladen [https://go.microsoft.com/fwlink/?LinkID=282725](https://go.microsoft.com/fwlink/?linkid=282725) .</span><span class="sxs-lookup"><span data-stu-id="24820-108">You can download the Planning Tool from the Microsoft Downloads Center ([https://go.microsoft.com/fwlink/?LinkID=282725](https://go.microsoft.com/fwlink/?linkid=282725)).</span></span>

<span data-ttu-id="24820-109">Das Ziel des Planungstools besteht letztendlich darin, die potenzielle Komplexität beim Entwerfen einer vollständigen lync Server 2013-Topologie zu verringern.</span><span class="sxs-lookup"><span data-stu-id="24820-109">Ultimately, the goal of the Planning Tool is to ease the potential complexity of designing a complete Lync Server 2013 topology.</span></span> <span data-ttu-id="24820-110">Das Tool stellt außerdem kontextbezogene Verweise auf die im Tool enthaltene Planungs- und Bereitstellungsdokumentation bereit, sofern eine Internetverbindung zur Microsoft TechNet-Website verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="24820-110">The tool also provides contextual references to planning and deployment documentation inside the tool, provided that an Internet connection is available to connect to the Microsoft TechNet website.</span></span>

<span data-ttu-id="24820-111">Nach dem Anpassen der Topologie mit den TCP/IP-Adressen der Infrastruktur und den vollqualifizierten Domänennamen (FQDNs) stellt das Planungs Tool eine Reihe von Berichten zur Verfügung, die DNS-Benennung (Domain Name System), Firewallregeln, Zertifikate und vieles mehr beinhalten.</span><span class="sxs-lookup"><span data-stu-id="24820-111">After customizing the topology with the infrastructure’s TCP/IP addresses and fully qualified domain names (FQDNs), the Planning Tool makes available a series of reports that cover Domain Name System (DNS) naming, firewall rules, certificates, and more.</span></span>

<span data-ttu-id="24820-112">Das Planungs Tool bietet auch die Möglichkeit, Informationen in zwei Formaten zu exportieren:</span><span class="sxs-lookup"><span data-stu-id="24820-112">The Planning Tool also provides the ability to export information in two formats:</span></span>

  - <span data-ttu-id="24820-113">Microsoft Excel</span><span class="sxs-lookup"><span data-stu-id="24820-113">Microsoft Excel</span></span>

  - <span data-ttu-id="24820-114">Microsoft Visio</span><span class="sxs-lookup"><span data-stu-id="24820-114">Microsoft Visio</span></span>

<span data-ttu-id="24820-115">In den folgenden Themen wird das Planungs Tool vorgestellt und detailliert beschrieben.</span><span class="sxs-lookup"><span data-stu-id="24820-115">The following topics introduce and detail the Planning Tool.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="24820-116">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="24820-116">In This Section</span></span>

  - [<span data-ttu-id="24820-117">Installieren des Planungstools in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="24820-117">Installing the Planning Tool in Lync Server 2013</span></span>](lync-server-2013-installing-the-planning-tool.md)

  - [<span data-ttu-id="24820-118">Installieren von optionaler Software in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="24820-118">Installing optional software in Lync Server 2013</span></span>](lync-server-2013-installing-optional-software.md)

  - [<span data-ttu-id="24820-119">Navigieren im Planungs Tool in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="24820-119">Navigating the Planning Tool in Lync Server 2013</span></span>](lync-server-2013-navigating-the-planning-tool.md)

  - [<span data-ttu-id="24820-120">Erstellen des anfänglichen Topologie-Designs für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="24820-120">Create the initial topology design for Lync Server 2013</span></span>](lync-server-2013-create-the-initial-topology-design.md)

  - [<span data-ttu-id="24820-121">Überprüfen der Administratorberichte in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="24820-121">Reviewing the Administrator Reports in Lync Server 2013</span></span>](lync-server-2013-reviewing-the-administrator-reports.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="24820-122">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="24820-122">See Also</span></span>


[<span data-ttu-id="24820-123">Bereitstellen von Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="24820-123">Deploying Lync Server 2013</span></span>](lync-server-2013-deploying-lync-server.md)  
[<span data-ttu-id="24820-124">Planen für Front-End-Server, Chat und Anwesenheit in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="24820-124">Planning for Front End Servers, instant messaging, and presence in Lync Server 2013</span></span>](lync-server-2013-planning-for-front-end-servers-instant-messaging-and-presence.md)  
  

<span data-ttu-id="24820-125"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="24820-125"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

