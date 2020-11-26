---
title: 'Lync Server 2013: System Nutzungsberichte'
description: 'Lync Server 2013: System Nutzungsberichte'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: System usage reports
ms:assetid: 187d316d-2456-417e-b636-05527a18ef06
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558618(v=OCS.15)
ms:contentKeyID: 48183529
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6fffaf22dacbc68958e64090fd4c7d44e32f8ade
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423554"
---
# <a name="system-usage-reports-in-lync-server-2013"></a><span data-ttu-id="d04b6-103">Berichte zur System Nutzung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d04b6-103">System usage reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d04b6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d04b6-104">

<span> </span></span></span>

<span data-ttu-id="d04b6-105">_**Letztes Änderungsdatum des Themas:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="d04b6-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="d04b6-106">Die System Nutzungsberichte liefern Informationen zur Systemnutzung auf der Grundlage von CDR-Daten (Call Detail Recording), die vom lync-Server erfasst werden.</span><span class="sxs-lookup"><span data-stu-id="d04b6-106">The System Usage Reports provide system usage information based on call detail recording (CDR) data collected by the Lync Server.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="d04b6-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="d04b6-107">In This Section</span></span>

  - [<span data-ttu-id="d04b6-108">Bericht zur Benutzerregistrierung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d04b6-108">User Registration Report in Lync Server 2013</span></span>](lync-server-2013-user-registration-report.md)
    
    <span data-ttu-id="d04b6-109">Bietet eine Zusammenfassung der Benutzerkonnektivität zur lync Server 2013-Bereitstellung auf der Grundlage von Registrierungs Ereignissen wie Benutzeranmeldungen.</span><span class="sxs-lookup"><span data-stu-id="d04b6-109">Provides a summary of user connectivity to the Lync Server 2013 deployment based on registration events such as user logons.</span></span> <span data-ttu-id="d04b6-110">Der Bericht bietet eine Möglichkeit zum Anzeigen interner und externer Anmeldungen sowie zum Vergleichen der Anzahl der Benutzer, die sich bei lync Server 2013 angemeldet haben, mit der Anzahl der Benutzer, die den Dienst tatsächlich verwendet haben, während Sie angemeldet waren.</span><span class="sxs-lookup"><span data-stu-id="d04b6-110">The report provides a way to view both internal and external logons, and to compare the number of users who logged on to Lync Server 2013 with the number of users who actually used the service while they were logged on.</span></span>

  - [<span data-ttu-id="d04b6-111">Zusammenfassungsbericht zur Peer-zu-Peer-Aktivität in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d04b6-111">Peer-to-Peer Activity Summary Report in Lync Server 2013</span></span>](lync-server-2013-peer-to-peer-activity-summary-report.md)
    
    <span data-ttu-id="d04b6-p102">Enthält eine Zusammenfassung der Peer-to-Peer-Sofortnachrichten-, Audio-, Video-, Dateiübertragungs- und Anwendungsfreigabesitzungen. An Peer-to-Peer-Sitzungen sind nur zwei Benutzer beteiligt.</span><span class="sxs-lookup"><span data-stu-id="d04b6-p102">Provides a summary of peer-to-peer instant messaging (IM), audio, video, file transfer, and application sharing sessions. Peer-to-peer sessions are sessions involving just two users.</span></span>

  - [<span data-ttu-id="d04b6-114">Bericht zur Konferenz Zusammenfassung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d04b6-114">Conference Summary Report in Lync Server 2013</span></span>](lync-server-2013-conference-summary-report.md)
    
    <span data-ttu-id="d04b6-115">Bietet eine Übersicht über alle Konferenzaktivitäten.</span><span class="sxs-lookup"><span data-stu-id="d04b6-115">Provides a summary of all conference activities.</span></span> <span data-ttu-id="d04b6-116">Eine Konferenz ist eine Sitzung mit mindestens drei Teilnehmern.</span><span class="sxs-lookup"><span data-stu-id="d04b6-116">Conferences are sessions involving three or more people.</span></span>

  - [<span data-ttu-id="d04b6-117">Bericht zur PSTN-Konferenz Zusammenfassung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d04b6-117">PSTN Conference Summary Report in Lync Server 2013</span></span>](lync-server-2013-pstn-conference-summary-report.md)
    
    <span data-ttu-id="d04b6-p104">Bietet eine Übersicht über alle PSTN-Konferenzen. Dies sind Konferenzen, bei denen sich mindestens ein Benutzer über das Festnetz (Public Switched Telephone Network, PSTN) einwählt. Sie werden auch als *Einwahlkonferenzen* bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="d04b6-p104">Provides a summary of all PSTN conferences. These are conferences where at least one user dials in using the public switched telephone network (PSTN), which is also referred to as *dial-in conferencing*.</span></span>

  - [<span data-ttu-id="d04b6-120">Bericht zur Antwortgruppen Nutzung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d04b6-120">Response Group Usage Report in Lync Server 2013</span></span>](lync-server-2013-response-group-usage-report.md)
    
    <span data-ttu-id="d04b6-121">Enthält eine Zusammenfassung der Verwendung der Reaktionsgruppe.</span><span class="sxs-lookup"><span data-stu-id="d04b6-121">Provides a summary of Response Group usage.</span></span> <span data-ttu-id="d04b6-122">Mit der Anwendung Reaktionsgruppe können Sie Telefonanrufe automatisch an Entitäten wie einen Helpdesk oder eine Kundendienstleitung weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="d04b6-122">The Response Group application provides a way for you to automatically route phone calls to entities such as a help desk or customer support line.</span></span>

  - [<span data-ttu-id="d04b6-123">Bericht zum IP Phone-Inventar in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d04b6-123">IP Phone Inventory Report in Lync Server 2013</span></span>](lync-server-2013-ip-phone-inventory-report.md)
    
    <span data-ttu-id="d04b6-124">Enthält Informationen zu den derzeit in der Organisation verwendeten IP-Telefonen.</span><span class="sxs-lookup"><span data-stu-id="d04b6-124">Provides information about the IP phones currently in use in the organization.</span></span> <span data-ttu-id="d04b6-125">Der Bericht basiert auf Telefon Registrierungen und Anmeldungen.</span><span class="sxs-lookup"><span data-stu-id="d04b6-125">The report is based on phone registrations and logons.</span></span> <span data-ttu-id="d04b6-126">Sie sollte nicht als vollständige Inventur angesehen werden.</span><span class="sxs-lookup"><span data-stu-id="d04b6-126">It should not be considered a complete inventory.</span></span> <span data-ttu-id="d04b6-127">Beispielsweise haben Sie möglicherweise Telefone entfernt, die noch im Bericht aufgeführt sind, weil Sie sich mindestens einmal angemeldet haben.</span><span class="sxs-lookup"><span data-stu-id="d04b6-127">For example, you might have removed phones that are still listed in the report because they logged on at least once.</span></span> <span data-ttu-id="d04b6-128">Ebenso können Sie auch neue Telefone haben, die nicht im Bericht angezeigt werden, nur weil sich die Benutzer noch nicht bei lync Server mit ihren neuen Telefonen angemeldet haben.</span><span class="sxs-lookup"><span data-stu-id="d04b6-128">Likewise, you might also have new phones that do not show up in the report simply because users have not logged on to Lync Server with their new phones yet.</span></span>

  - [<span data-ttu-id="d04b6-129">Bericht zur Anruf Zulassungs Steuerung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d04b6-129">Call Admission Control Report in Lync Server 2013</span></span>](lync-server-2013-call-admission-control-report.md)
    
    <span data-ttu-id="d04b6-p107">Enthält eine Liste der Peer-to-Peer- und Konferenzaktivitäten, für die Anrufsteuerung (Call Admission Control, CAC) verwendet wird. Mithilfe der Anrufsteuerung können Sie feststellen, ob ausgehend von etwaigen Bandbreiteneinschränkungen Echtzeitkommunikationssitzungen (z. B. Sprach- oder Videoanrufe) hergestellt werden können sollen.</span><span class="sxs-lookup"><span data-stu-id="d04b6-p107">Provides a list of peer-to-peer and conference activities that use call admission control. Call admission control (CAC) is a way of determining whether you should allow real-time communications sessions, such as voice or video calls, based on bandwidth constraints.</span></span>

<span data-ttu-id="d04b6-132"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d04b6-132"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

