---
title: Lync Server 2013-Konferenz Lastverteilung
description: Lync Server 2013-Konferenz Lastverteilung.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Conferencing load distribution
ms:assetid: 5901a076-1b6f-4720-8837-95fc7f3c37f3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204922(v=OCS.15)
ms:contentKeyID: 48184233
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 28897b26d7351bf0ea577e2678d916aec6d15647
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434326"
---
# <a name="conferencing-load-distribution-in-lync-server-2013"></a><span data-ttu-id="ca92e-103">Verteilung von Konferenz Lasten in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ca92e-103">Conferencing load distribution in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ca92e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ca92e-104">

<span> </span></span></span>

<span data-ttu-id="ca92e-105">_**Letztes Änderungsdatum des Themas:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="ca92e-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="ca92e-106">Im Gegensatz zu einigen anderen dedizierten Konferenzlösungen handelt es sich bei der lync Server-Architektur um ein freigegebenes Hardwaremodell.</span><span class="sxs-lookup"><span data-stu-id="ca92e-106">Unlike some other dedicated conferencing solutions, Lync Server architecture is a shared-hardware model.</span></span> <span data-ttu-id="ca92e-107">Das bedeutet, dass die gleiche Hardware von vielen Softwarekomponenten freigegeben wird, die jeweils unterschiedliche Echtzeitkommunikationen unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ca92e-107">This means that the same hardware is shared by many software components, each of which supports different real-time communications.</span></span> <span data-ttu-id="ca92e-108">Jede Art von Echtzeitkommunikation platziert bestimmte Lasten auf den Servern.</span><span class="sxs-lookup"><span data-stu-id="ca92e-108">Each type of real-time communications places specific loads on the servers.</span></span> <span data-ttu-id="ca92e-109">So kann beispielsweise der Front-End-Server die SIP-Routingkomponenten (Session Initiation Protocol), Webanwendungen (wie Adressbuchsuche), Webkonferenzdienst, A/V-Konferenzdienst, Enterprise-VoIP-Anwendungen (beispielsweise die Anwendungs-und reaktionsgruppenanwendung der Konferenzzentrale) und den Vermittlungsserver ausführen.</span><span class="sxs-lookup"><span data-stu-id="ca92e-109">For example, the Front End Server can run the Session Initiation Protocol (SIP) routing components, web applications (such as Address Book search), Web Conferencing service, A/V Conferencing service, Enterprise Voice applications (for example, Conferencing Attendant application and Response Group application), and Mediation Server.</span></span> <span data-ttu-id="ca92e-110">Eine Gruppe von Datenbanken auf dem Front-End-Server bietet auch Speicher und Verarbeitung für Benutzer-, Kontakt-, Anwesenheits-, Konferenz-und VoIP-Routingdaten.</span><span class="sxs-lookup"><span data-stu-id="ca92e-110">A set of databases on the Front End Server also provide storage and processing for user, contact, presence, conferencing, and voice routing data.</span></span> <span data-ttu-id="ca92e-111">Wenn diese Hardware Freigabe, Komponenten, Dienste und Prozesse für CPU-und Arbeitsspeicherressourcen konkurrieren, wirken sich nicht-Konferenz Arbeitslasten direkt auf die Server Skalierung aus.</span><span class="sxs-lookup"><span data-stu-id="ca92e-111">With this hardware sharing, components, services, and processes compete for CPU and memory resources, so non-conferencing workloads have a direct impact on server scaling.</span></span>

<span data-ttu-id="ca92e-112">Im Vergleich zu anderen Hardware-portbasierten Konferenzlösungen ist die lync Server-Konferenz Architektur kein Reservierungs Modell.</span><span class="sxs-lookup"><span data-stu-id="ca92e-112">Compared to other hardware port-based conferencing solutions, Lync Server conferencing architecture is a no-reservation model.</span></span> <span data-ttu-id="ca92e-113">Wenn ein Benutzer eine Besprechung plant, erstellt lync Server einen Eintrag in der Konferenzdatenbank, in dem Konferenzdaten gespeichert werden, reserviert aber keine Hardwareressourcen für die geplante Besprechung im voraus.</span><span class="sxs-lookup"><span data-stu-id="ca92e-113">When a user schedules a meeting, Lync Server creates a record in the conferencing database, which stores conferencing data, but does not reserve any hardware resources for the scheduled meeting ahead of time.</span></span> <span data-ttu-id="ca92e-114">Stattdessen verfügt lync Server über integrierte Lastenausgleichs Logik, um Konferenzressourcen auf Front-End-Servern so dynamisch zuzuweisen, dass Lasten gleichmäßig über alle Front-End-Server im Pool verteilt werden.</span><span class="sxs-lookup"><span data-stu-id="ca92e-114">Instead, Lync Server has built-in load balancing logic to dynamically allocate conferencing resources on Front End Servers in a way that distributes loads equally across all Front End Servers in the pool.</span></span> <span data-ttu-id="ca92e-115">Diese Bestimmungen und nutzt Hardwareressourcen, macht es aber schwierig, sehr große Besprechungen zu unterstützen (insbesondere ohne angemessene Planung).</span><span class="sxs-lookup"><span data-stu-id="ca92e-115">This effectively provisions and utilizes hardware resources, but makes it challenging to support very large meetings (especially without appropriate planning).</span></span> <span data-ttu-id="ca92e-116">Wenn beispielsweise ein lync Server 2013-Pool nahezu an seiner obersten Kapazität ausgeführt wird, kann jeder Front-End-Server ungefähr 125 Besprechungen mit durchschnittlicher Größe hosten.</span><span class="sxs-lookup"><span data-stu-id="ca92e-116">For example, when a Lync Server 2013 pool is running close to its top capacity, each Front End Server might host approximately 125 average-size meetings.</span></span> <span data-ttu-id="ca92e-117">Das Hinzufügen einer weiteren kleinen Besprechung wäre kein Problem, doch das Hinzufügen einer Besprechung für 1000-Benutzer wäre ein Problem, da die Front-End-Server wahrscheinlich nicht in der Lage sind, eine so große Besprechung zur gleichen Zeit wie die anderen 125-Besprechungen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="ca92e-117">Adding another small meeting would not be a problem, but adding a meeting for 1000 users would be a problem because the Front End Servers would probably not be able to support such a large meeting at the same time as the other 125 meetings.</span></span>

<span data-ttu-id="ca92e-118"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ca92e-118"></div>

<span> </span>

</div>

</div>

</span></span></div>

