---
title: 'Lync Server 2013: Unterstützte Virtualisierungstechnologien und bekannte Einschränkungen'
description: 'Lync Server 2013: Unterstützte Virtualisierungs-Technologien und bekannte Einschränkungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported virtualization technologies and known limitations
ms:assetid: 6d3d749d-e840-4c05-afae-d6e69e7616aa
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204982(v=OCS.15)
ms:contentKeyID: 48184428
ms.date: 02/07/2017
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 745fa535462d29342f4c0a58674ee6487db42a6f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423561"
---
# <a name="supported-virtualization-technologies-and-known-limitations-in-lync-server-2013"></a><span data-ttu-id="91780-103">Unterstützte Virtualisierungstechnologien und bekannte Einschränkungen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="91780-103">Supported virtualization technologies and known limitations in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="91780-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="91780-104">

<span> </span></span></span>

<span data-ttu-id="91780-105">_**Letztes Änderungsdatum des Themas:** 2017-02-06_</span><span class="sxs-lookup"><span data-stu-id="91780-105">_**Topic Last Modified:** 2017-02-06_</span></span>

<span data-ttu-id="91780-106">Das lync VDI-Plug-in ermöglicht Audio-und Videoanrufe nach unterstützten Virtualisierungstechnologien.</span><span class="sxs-lookup"><span data-stu-id="91780-106">The Lync VDI plug-in allows audio and video calling for supported virtualization technologies.</span></span> <span data-ttu-id="91780-107">Dadurch wird die für Microsoft lync Server 2010 in der [Client-Virtualisierung in Microsoft lync 2010](https://go.microsoft.com/fwlink/?linkid=330447) -Whitepaper skizzierte Funktionalität erweitert.</span><span class="sxs-lookup"><span data-stu-id="91780-107">This extends the functionality outlined for Microsoft Lync Server 2010 in the [Client Virtualization in Microsoft Lync 2010](https://go.microsoft.com/fwlink/?linkid=330447) white paper.</span></span> <span data-ttu-id="91780-108">Gemäß Standardtelefonvorschriften ist auch Unterstützung für E911 enthalten.</span><span class="sxs-lookup"><span data-stu-id="91780-108">In compliance with standard telephone regulations, support for E911 is also included.</span></span> <span data-ttu-id="91780-109">In den folgenden Abschnitten werden die Virtualisierungstechnologien beschrieben, die vom lync-VDI-Plug-in und den bekannten Funktionseinschränkungen unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="91780-109">The following sections describe the virtualization technologies that are supported by the Lync VDI plug-in and the known feature limitations.</span></span>

<div>

## <a name="support-for-virtualization-technologies"></a><span data-ttu-id="91780-110">Unterstützung für Virtualisierungstechnologien</span><span class="sxs-lookup"><span data-stu-id="91780-110">Support for Virtualization Technologies</span></span>

<span data-ttu-id="91780-111">Das lync-VDI-Plug-in unterstützt das vollständige Desktop-Remoting im Szenario des persönlichen virtuellen Desktops, aber nicht im Szenario der Remotedesktopsitzung.</span><span class="sxs-lookup"><span data-stu-id="91780-111">The Lync VDI plug-in supports full desktop remoting in the personal virtual desktop scenario, but not in the remote desktop session scenario.</span></span> <span data-ttu-id="91780-112">Diese Szenarien können wie folgt beschrieben werden:</span><span class="sxs-lookup"><span data-stu-id="91780-112">These scenarios can be described as follows:</span></span>

  - <span data-ttu-id="91780-113">**Unterstützt: Personalisierte virtuelle Desktops oder virtuelle Desktopinfrastruktur (Virtual Desktop Infrastructure, VDI).**</span><span class="sxs-lookup"><span data-stu-id="91780-113">**Supported: Personalized Virtual Desktops or Virtual Desktop Infrastructure (VDI).**</span></span>   <span data-ttu-id="91780-114">In diesem Szenario melden sich die einzelnen Benutzer bei einem anpassbaren virtuellen Desktop an und können Dateien auf dem Desktop speichern, die sitzungsübergreifend bestehen bleiben.</span><span class="sxs-lookup"><span data-stu-id="91780-114">In this scenario, each user logs on to a customizable virtual desktop and is able to save files on the desktop that persist across sessions.</span></span> <span data-ttu-id="91780-115">Microsoft Remote Desktop Dienste, VMware Horizon View und Citrix XenDesktop sind Implementierungen, die für die Verwendung mit lync getestet wurden.</span><span class="sxs-lookup"><span data-stu-id="91780-115">Microsoft Remote Desktop Services, VMware Horizon View, and Citrix XenDesktop are implementations that have been tested for use with Lync.</span></span> <span data-ttu-id="91780-116">Informationen zu herstellerspezifischen VDI-Umgebungen und Clienthardware, die von Microsoft getestet wurden, finden Sie unter [für Microsoft lync qualifizierte Infrastruktur](https://go.microsoft.com/fwlink/?linkid=313435).</span><span class="sxs-lookup"><span data-stu-id="91780-116">For information about vendor-specific VDI environments and client hardware that have been tested by Microsoft, see [Infrastructure qualified for Microsoft Lync](https://go.microsoft.com/fwlink/?linkid=313435).</span></span>

  - <span data-ttu-id="91780-117">**Nicht unterstützt: Remotedesktopsitzungen.**</span><span class="sxs-lookup"><span data-stu-id="91780-117">**Not supported: Remote Desktop Sessions.**</span></span>   <span data-ttu-id="91780-118">In diesem Szenario meldet sich jeder Benutzer bei einer allgemeinen virtuellen Desktopsitzung an, die nicht angepasst werden kann.</span><span class="sxs-lookup"><span data-stu-id="91780-118">In this scenario, each user logs on to a generic virtual desktop session that cannot be customized.</span></span> <span data-ttu-id="91780-119">Zu den Beispielimplementierungen gehören Microsoft-Remotedesktopsitzungen (RDSH) und Citrix XenApp in Kombination mit Citrix Receiver.</span><span class="sxs-lookup"><span data-stu-id="91780-119">Example implementations include Microsoft Remote Desktop Sessions (RDSH) and Citrix XenApp combined with Citrix Receiver.</span></span>

<span data-ttu-id="91780-120">Das lync-VDI-Plug-in unterstützt keine anderen Virtualisierungstechnologien wie Application Virtualization, was die Verwendung einer Anwendung ermöglicht, ohne dass die vollständige Anwendung lokal installiert werden muss.</span><span class="sxs-lookup"><span data-stu-id="91780-120">The Lync VDI plug-in does not support other virtualization technologies, such as application virtualization, which allows the use of an application without requiring installation of the full application locally.</span></span> <span data-ttu-id="91780-121">Zu den Beispielimplementierungen gehören Citrix XenApp und Microsoft Application Virtualization (App-V).</span><span class="sxs-lookup"><span data-stu-id="91780-121">Example implementations include Citrix XenApp and Microsoft Application Virtualization (App-V).</span></span> <span data-ttu-id="91780-122">Anwendungsstreaming, Anwendungsremoting und gemischte Virtualisierungsmodi (zum Beispiel Anwendungsremoting in vollem Desktopremoting) werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91780-122">Application streaming, application remoting, and mixed virtualization modes (for example, application remoting in full desktop remoting) are not supported.</span></span>

<span data-ttu-id="91780-123">Um die Erweiterbarkeit zu ermöglichen, wurde das lync VDI-Plug-in für die Verwendung von plattformunabhängigen APIs mit dem Namen Dynamic Virtual Channels (DVCs) entwickelt.</span><span class="sxs-lookup"><span data-stu-id="91780-123">To allow extensibility, the Lync VDI plug-in was designed to use platform-independent APIs called Dynamic Virtual Channels (DVCs).</span></span> <span data-ttu-id="91780-124">Informationen zu Szenarien, die nicht explizit von lync unterstützt werden, finden Sie unter Support-Statements des VDI-Lösungsanbieters.</span><span class="sxs-lookup"><span data-stu-id="91780-124">For scenarios that are not explicitly supported by Lync, refer to support statements from the VDI solution provider.</span></span>

</div>

<div>

## <a name="known-feature-limitations"></a><span data-ttu-id="91780-125">Bekannte Funktionseinschränkungen</span><span class="sxs-lookup"><span data-stu-id="91780-125">Known Feature Limitations</span></span>

<span data-ttu-id="91780-126">Im folgenden sind bekannte Einschränkungen bei der Verwendung von lync 2013 in einer VDI-Umgebung bekannt:</span><span class="sxs-lookup"><span data-stu-id="91780-126">The following are known limitations when you use Lync 2013 in a VDI environment:</span></span>

  - <span data-ttu-id="91780-127">Es gibt nur begrenzte Unterstützung für die Anonymisierungs Funktionen für Anruf Delegierungen und Reaktionsgruppen-Agents.</span><span class="sxs-lookup"><span data-stu-id="91780-127">There is limited support for Call Delegation and Response Group Agent Anonymization features.</span></span>

  - <span data-ttu-id="91780-128">Folgende Features werden nicht unterstützt:</span><span class="sxs-lookup"><span data-stu-id="91780-128">There is no support for the following features:</span></span>
    
      - <span data-ttu-id="91780-129">Integrierte Optimierungsseiten für Audio- und Videogeräte</span><span class="sxs-lookup"><span data-stu-id="91780-129">Integrated Audio Device and Video Device tuning pages.</span></span>
    
      - <span data-ttu-id="91780-130">Mehransicht für Video</span><span class="sxs-lookup"><span data-stu-id="91780-130">Multiple-view video.</span></span>
    
      - <span data-ttu-id="91780-131">Aufzeichnen von Konversationen</span><span class="sxs-lookup"><span data-stu-id="91780-131">Recording of conversations.</span></span>
    
      - <span data-ttu-id="91780-132">Remote Desktop Dienste (RDS).</span><span class="sxs-lookup"><span data-stu-id="91780-132">Remote Desktop Services (RDS).</span></span>
    
      - <span data-ttu-id="91780-133">Anonyme Teilnahme an Besprechungen (also an lync-Besprechungen, die von einer Organisation gehostet werden, die nicht mit Ihrer Organisation in Verbindung steht).</span><span class="sxs-lookup"><span data-stu-id="91780-133">Joining meetings anonymously (that is, joining Lync meetings hosted by an organization that does not federate with your organization).</span></span>
    
      - <span data-ttu-id="91780-134">Verwenden des lync-VDI-Plug-ins zusammen mit einem lync Phone Edition-Gerät.</span><span class="sxs-lookup"><span data-stu-id="91780-134">Using the Lync VDI plug-in along with a Lync Phone Edition device.</span></span>
    
      - <span data-ttu-id="91780-135">Anrufkontinuität im Fall eines Netzwerkausfalls</span><span class="sxs-lookup"><span data-stu-id="91780-135">Call continuity in case of a network outage.</span></span>
    
      - <span data-ttu-id="91780-136">Features für benutzerdefinierte Klingeltöne und Wartemusik</span><span class="sxs-lookup"><span data-stu-id="91780-136">Customized ringtones and music-on-hold features.</span></span>

  - <span data-ttu-id="91780-137">Das lync-VDI-Plug-in wird in einer Microsoft 365-oder Office 365-Umgebung nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="91780-137">The Lync VDI plug-in is not supported in a Microsoft 365 or Office 365 environment.</span></span>

<span data-ttu-id="91780-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="91780-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

