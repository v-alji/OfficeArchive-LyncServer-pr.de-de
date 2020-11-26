---
title: 'Lync Server 2013: Topologien für IP-Telefone'
description: 'Lync Server 2013: Topologien für IP-Telefone.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Topologies for IP phones
ms:assetid: 26ebffcf-43ff-4e70-847d-0fbc90e94e57
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425740(v=OCS.15)
ms:contentKeyID: 48183662
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7a151a83a69e1f7e14dcbed8d8ab1038157fa839
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439663"
---
# <a name="topologies-for-ip-phones-in-lync-server-2013"></a><span data-ttu-id="40b0a-103">Topologien für IP-Telefone in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="40b0a-103">Topologies for IP phones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="40b0a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="40b0a-104">

<span> </span></span></span>

<span data-ttu-id="40b0a-105">_**Letztes Änderungsdatum des Themas:** 2012-06-21_</span><span class="sxs-lookup"><span data-stu-id="40b0a-105">_**Topic Last Modified:** 2012-06-21_</span></span>

<span data-ttu-id="40b0a-106">Dieser Abschnitt bietet einen Überblick über den Verbindungsprozess und erläutert die Unterschiede zwischen der Verbindung eines IP-Telefons in einem internen und einem externen Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="40b0a-106">This section provides an overview of the connectivity process and explains the differences between how an IP phone connects in an internal and external network.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="40b0a-107">Lync Server bietet Unterstützung für die folgenden IP-Telefone: das Aastra 6721ip-Telefon, das Aastra 6725ip-Tischtelefon, das HP 4110-IP-Telefon (Common Area Phone), das HP 4120 IP-Telefon (Tischtelefon), das Polycom CX600 IP-Tischtelefon, das Polycom CX700 IP-Tischtelefon, das Polycom CX500 IP-Konferenztelefon sowie das Polycom IP-Konferenztelefon</span><span class="sxs-lookup"><span data-stu-id="40b0a-107">Lync Server provides support for the following IP phones: the Aastra 6721ip common area phone, Aastra 6725ip desk phone, HP 4110 IP Phone (common area phone), HP 4120 IP Phone (desk phone), Polycom CX600 IP desk phone, Polycom CX700 IP desk phone, Polycom CX500 IP common area phone, and Polycom CX3000 IP conference phone.</span></span> <span data-ttu-id="40b0a-108">Von diesen Telefonen kann nur die Polycom CX700 lync Phone Edition ausführen.</span><span class="sxs-lookup"><span data-stu-id="40b0a-108">Of those phones, all but the Polycom CX700 can run Lync Phone Edition.</span></span>



</div>

<span data-ttu-id="40b0a-109">Das folgende Diagramm beschreibt alle Komponenten, die für die Gerätekonnektivität innerhalb der Unternehmensumgebung erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="40b0a-109">The following diagram describes all the components involved in device connectivity within the corporate environment.</span></span>

<span data-ttu-id="40b0a-110">**Interne Topologie**</span><span class="sxs-lookup"><span data-stu-id="40b0a-110">**Internal Topology**</span></span>

<span data-ttu-id="40b0a-111">![3d88893e-df57-46e3-855a-a1d24589030a](images/Gg425740.3d88893e-df57-46e3-855a-a1d24589030a(OCS.15).jpg "3d88893e-df57-46e3-855a-a1d24589030a")</span><span class="sxs-lookup"><span data-stu-id="40b0a-111">![3d88893e-df57-46e3-855a-a1d24589030a](images/Gg425740.3d88893e-df57-46e3-855a-a1d24589030a(OCS.15).jpg "3d88893e-df57-46e3-855a-a1d24589030a")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="40b0a-112">Bei der vorherigen Abbildung handelt es sich um eine logische Darstellung, keine physische Übersicht.</span><span class="sxs-lookup"><span data-stu-id="40b0a-112">The previous figure is a logical representation, not a physical overview.</span></span> <span data-ttu-id="40b0a-113">Beispielsweise befindet sich die Active Directory-Domänendienste (AD DS) selten auf demselben Computer wie alle lync Server-Komponenten.</span><span class="sxs-lookup"><span data-stu-id="40b0a-113">For example, Active Directory Domain Services (AD DS) is rarely located on the same machine as any Lync Server components.</span></span> <span data-ttu-id="40b0a-114">Der Benutzerspeicher kann sich auf dem Back-End-Server oder auf den Archivierungs-und Überwachungs Servern befinden.</span><span class="sxs-lookup"><span data-stu-id="40b0a-114">The user store can be located on the Back End Server or on the Archiving and Monitoring Servers.</span></span> <span data-ttu-id="40b0a-115">Die lync Server-Verwaltungsshell, Webserver und Updatedienste sind Teil der Front-End-Serverrolle.</span><span class="sxs-lookup"><span data-stu-id="40b0a-115">The Lync Server Management Shell, web server, and update services are all part of the Front End Server role.</span></span>



</div>

<span data-ttu-id="40b0a-116">Das folgende Diagramm bietet eine Übersicht über die beteiligten Komponenten, wenn sich das Gerät außerhalb des Unternehmensnetzwerks befindet.</span><span class="sxs-lookup"><span data-stu-id="40b0a-116">The following diagram provides an overview of the components involved when the device is located outside the corporate network.</span></span>

<span data-ttu-id="40b0a-117">**Externe Topologie**</span><span class="sxs-lookup"><span data-stu-id="40b0a-117">**External Topology**</span></span>

<span data-ttu-id="40b0a-118">![8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3](images/Gg425740.8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3(OCS.15).jpg "8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3")</span><span class="sxs-lookup"><span data-stu-id="40b0a-118">![8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3](images/Gg425740.8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3(OCS.15).jpg "8ce6bb8e-b89c-4c4e-ac6d-41ac6c68f6f3")</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="40b0a-119">Der Geräte Update-Webdienst bietet eine externe und interne Website, aber nur die externe Website wird hier angezeigt.</span><span class="sxs-lookup"><span data-stu-id="40b0a-119">The Device Update Web service provides an external and internal website, but only the external one is shown here.</span></span><BR><span data-ttu-id="40b0a-120">Der Speicherort der Registrierungsstelle und die URL des Geräte Update-Webdiensts für die Organisation müssen in DNS veröffentlicht werden, wenn externer Zugriff aktiviert werden soll.</span><span class="sxs-lookup"><span data-stu-id="40b0a-120">The location of the Registrar and the URL of the Device Update Web service for the organization must be published in DNS if external access is to be enabled.</span></span> <span data-ttu-id="40b0a-121">Darüber hinaus muss der Edgeserver bereitgestellt und ordnungsgemäß konfiguriert werden, um die externe Kommunikation vom Gerät zur Unternehmensumgebung und zurück zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="40b0a-121">Additionally, the Edge Server must be deployed and correctly configured to allow external communications from the device to the corporate environment and back.</span></span> <span data-ttu-id="40b0a-122">Dies wird im vorherigen Diagramm ausgelassen, da die Edge-Bereitstellung nicht für die Gerätekonnektivität spezifisch ist.</span><span class="sxs-lookup"><span data-stu-id="40b0a-122">This is omitted from the previous diagram because Edge deployment is not specific to device connectivity.</span></span>



<span data-ttu-id="40b0a-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="40b0a-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

