---
title: 'Lync Server 2013: Planen von Details für Besprechungen'
description: 'Lync Server 2013: Planen von Details für Besprechungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Scheduling details
ms:assetid: 39ca6fff-2c15-4347-9f1f-6c8687a39a49
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204823(v=OCS.15)
ms:contentKeyID: 48183910
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ef7a6907aedbc880731b3fb474c9294c1c111b80
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442022"
---
# <a name="scheduling-details-for-meetings-in-lync-server-2013"></a><span data-ttu-id="bff6a-103">Planen von Details für Besprechungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bff6a-103">Scheduling details for meetings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bff6a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bff6a-104">

<span> </span></span></span>

<span data-ttu-id="bff6a-105">_**Letztes Änderungsdatum des Themas:** 2012-10-04_</span><span class="sxs-lookup"><span data-stu-id="bff6a-105">_**Topic Last Modified:** 2012-10-04_</span></span>

<span data-ttu-id="bff6a-106">Nachdem sichergestellt wurde, dass zum angefragten Zeitpunkt keine weitere Besprechung anberaumt ist, planen die zuständigen Supportmitarbeiter die Besprechung im Pool für große Besprechungen ein.</span><span class="sxs-lookup"><span data-stu-id="bff6a-106">After checking to ensure that no other meeting is scheduled at the requested time, the large meeting support staff that handles the request schedules the meeting on the large-meeting pool.</span></span> <span data-ttu-id="bff6a-107">Verwenden Sie das Online Besprechungs-Add-in für lync, das mit dem lync Server 2013-Client installiert ist, um diese Aufgabe mithilfe der Anmeldeinformationen eines für lync Server aktivierten Benutzers im dedizierten groß Besprechungs Pool auszuführen.</span><span class="sxs-lookup"><span data-stu-id="bff6a-107">Use the Online Meeting Add-in for Lync that is installed with the Lync Server 2013 client to perform this task, using the credentials of a user enabled for Lync Server in the dedicated large-meeting pool.</span></span>

<span data-ttu-id="bff6a-108">Um die bestmögliche Benutzerfreundlichkeit zu erzielen, ist es wichtig, die große Besprechung mit den richtigen Zugriffsebenen und Besprechungseinstellungen zu planen, die den Bedürfnissen des Besprechungsorganisators entsprechen.</span><span class="sxs-lookup"><span data-stu-id="bff6a-108">To ensure the best user experience, it is important to schedule the large meeting with the right access levels and meeting settings that are appropriate to the meeting organizer’s needs.</span></span> <span data-ttu-id="bff6a-109">Wir empfehlen die folgenden Planungseinstellungen, die in den lync-Besprechungsoptionen konfiguriert sind:</span><span class="sxs-lookup"><span data-stu-id="bff6a-109">We recommend the following scheduling settings configured in Lync Meeting options:</span></span>

  - <span data-ttu-id="bff6a-110">Verwenden Sie einen neuen Besprechungsraum für jede große Besprechung, anstatt den dedizierten Besprechungsraum erneut zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bff6a-110">Use a new meeting space for each large meeting instead of reusing the dedicated meeting space.</span></span>

  - <span data-ttu-id="bff6a-111">Geben Sie die Zugriffsebene für die Besprechung wie folgt an:</span><span class="sxs-lookup"><span data-stu-id="bff6a-111">Specify the meeting access level as follows:</span></span>
    
      - <span data-ttu-id="bff6a-112">Wenn mindestens eine Einladung außerhalb der Organisation ist, setzen Sie den Besprechungs Zugriffstyp auf " **jeder" (keine Einschränkungen**.</span><span class="sxs-lookup"><span data-stu-id="bff6a-112">If at least one invitee is external to the organization, set the meeting access type to **Anyone (no restrictions**.</span></span> <span data-ttu-id="bff6a-113">Dadurch vermeiden Sie, dass Sie während der laufenden Besprechung einen möglicherweise großen Wartebereich verwalten müssen.</span><span class="sxs-lookup"><span data-stu-id="bff6a-113">This enables you to avoid having to manage a potentially large lobby when the meeting is in progress.</span></span>
    
      - <span data-ttu-id="bff6a-114">Wenn die Besprechung nur intern ist, legen Sie den Zugriffstyp für die Besprechung auf **Jeder innerhalb meiner Organisation** fest.</span><span class="sxs-lookup"><span data-stu-id="bff6a-114">If the meeting is an internal-only meeting, set the meeting access type to **Anyone from my organization**.</span></span>
        
        <div>
        

        > [!NOTE]  
        > <span data-ttu-id="bff6a-115">Vermeiden Sie die Festlegung des Besprechungszugriffs Typs für Personen, die <STRONG>ich aus meinem Unternehmen einlade</STRONG> , denn wenn Sie diese Einstellung verwenden, müssen Organisatoren alle Benutzer-e-Mail-Adressen zur Liste der eingeladenen hinzufügen, und Sie können keine Verteilergruppe einladen.</span><span class="sxs-lookup"><span data-stu-id="bff6a-115">Avoid setting the meeting access type to <STRONG>People I invite from my company</STRONG> because when you use this setting, organizers must add all user email addresses to the invitee list and you cannot invite a distribution group.</span></span><BR><span data-ttu-id="bff6a-116">Vermeiden Sie es, den Besprechungs Zugriffstyp <STRONG>nur auf ich, den Organisator der Besprechung</STRONG> , festzulegen, da für diese Einstellung erforderlich ist, dass jeder Besprechungsteilnehmer, einschließlich Referenten, zur Besprechungs Laufzeit in die Lobby gestellt wird.</span><span class="sxs-lookup"><span data-stu-id="bff6a-116">Avoid setting the meeting access type to <STRONG>Only me, the meeting organizer</STRONG> because this setting requires that every meeting participant, including presenters, must be put in the lobby at meeting run time.</span></span> <span data-ttu-id="bff6a-117">Die Person, die für die Ausführung der umfangreichen Besprechung verantwortlich ist, muss die Lobby Liste ständig überwachen und neue Benutzer in der Lobby aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="bff6a-117">The person responsible for running the large meeting must then constantly monitor the lobby roster and admit new users who are in the lobby.</span></span>

        
        </div>

  - <span data-ttu-id="bff6a-118">Wenn Sie die Option **Anrufer erhalten direkten Zugang** aktivieren, können Benutzer, die sich per Telefon einwählen, automatisch der Besprechung beitreten.</span><span class="sxs-lookup"><span data-stu-id="bff6a-118">Allow users who dial-in from phones to enter the meeting automatically by checking the **Callers get in directly** setting.</span></span>

  - <span data-ttu-id="bff6a-119">Laden Sie folgende Benutzer explizit ein:</span><span class="sxs-lookup"><span data-stu-id="bff6a-119">Explicitly invite the following users:</span></span>
    
      - <span data-ttu-id="bff6a-120">Besprechungsorganisator und Delegat (anfordernde Person)</span><span class="sxs-lookup"><span data-stu-id="bff6a-120">Meeting organizer and delegate (requester)</span></span>
    
      - <span data-ttu-id="bff6a-121">Die von der eine Besprechung anfordernden Person vorgelegte Liste mit Referenten</span><span class="sxs-lookup"><span data-stu-id="bff6a-121">The list of presenters provided by a meeting requester</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="bff6a-122">Wenn der Zugriffstyp der Besprechung auf <STRONG>Von mir ausgewählte Personen</STRONG> festgelegt ist, müssen Sie jeden Teilnehmer einer großen Besprechung explizit als eingeladenen Benutzer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="bff6a-122">If the meeting access type is set to <STRONG>People I choose</STRONG>, you need to explicitly add each participant of a large meeting as an invitee of the meeting.</span></span>

    
    </div>

  - <span data-ttu-id="bff6a-p105">Verwalten Sie die Referenten explizit, anstatt die Referenten-Option auf einen der Werte für automatische Hochstufung festzulegen. Stellen Sie sicher, dass folgende Benutzer als Referenten hinzugefügt werden:</span><span class="sxs-lookup"><span data-stu-id="bff6a-p105">Explicitly manage presenters, instead of setting the presenter option to one of the auto-promote values. Be sure to add the following users as presenters:</span></span>
    
      - <span data-ttu-id="bff6a-125">Besprechungsorganisator und Delegat (anfordernde Person)</span><span class="sxs-lookup"><span data-stu-id="bff6a-125">Meeting organizer and delegate (requester)</span></span>
    
      - <span data-ttu-id="bff6a-126">Die von eine große Besprechung anfordernden Personen vorgelegte Liste mit Referenten</span><span class="sxs-lookup"><span data-stu-id="bff6a-126">The list of presenters provided by large meeting requesters</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="bff6a-127">Indem Sie Referenten explizit verwalten, können Sie die Anzahl der Referenten steuern, sodass Sie die Referenten auf eine klein genug Zahl begrenzen können, um eine effektive große Besprechung zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="bff6a-127">By explicitly managing presenters, you can control the number of presenters, so that you can limit presenters to a small enough number to make it possible to have an effective large meeting.</span></span> <span data-ttu-id="bff6a-128">Wenn die Mehrheit der Besprechungsteilnehmer über die Rolle "Teilnehmer" verfügt, kann dadurch die Wahrscheinlichkeit verringert werden, dass Personen versehentlich die Steuerung der Präsentation übernehmen, eine PowerPoint-Präsentation löschen, Referenten stumm schalten/stumm schalten und andere Unterbrechungen der Besprechung durchführen.</span><span class="sxs-lookup"><span data-stu-id="bff6a-128">If the majority of meeting participants have the attendee role, it helps reduce the chance of people accidentally taking control of the presentation, deleting a PowerPoint presentation, muting/unmuting presenters, and other disruptions to the meeting.</span></span>

    
    </div>

  - <span data-ttu-id="bff6a-129">Aktivieren Sie die Option **Alle Teilnehmer stummschalten**, um sicherzustellen, dass nur Referenten Audioinhalte in die Besprechung übertragen können.</span><span class="sxs-lookup"><span data-stu-id="bff6a-129">Check the **Mute all attendees** setting to make sure that only presenters can broadcast audio into the meeting.</span></span>

  - <span data-ttu-id="bff6a-130">Aktivieren Sie die Option **Video von Teilnehmern blockieren**, um sicherzustellen, dass nur Referenten Videoinhalte in die Besprechung übertragen können.</span><span class="sxs-lookup"><span data-stu-id="bff6a-130">Check the **Block attendees’ video** setting to make sure only presenters can broadcast video into the meeting.</span></span>

<span data-ttu-id="bff6a-131">Die folgende Abbildung zeigt die empfohlenen Einstellungen für das Online Besprechungs-Add-in für lync.</span><span class="sxs-lookup"><span data-stu-id="bff6a-131">The following figure shows the recommended settings for the Online Meeting Add-in for Lync.</span></span>

<span data-ttu-id="bff6a-132">![54e4e70d-06b0-45cd-8d94-bab649cd5dc0](images/JJ204823.54e4e70d-06b0-45cd-8d94-bab649cd5dc0(OCS.15).jpg "54e4e70d-06b0-45cd-8d94-bab649cd5dc0")</span><span class="sxs-lookup"><span data-stu-id="bff6a-132">![54e4e70d-06b0-45cd-8d94-bab649cd5dc0](images/JJ204823.54e4e70d-06b0-45cd-8d94-bab649cd5dc0(OCS.15).jpg "54e4e70d-06b0-45cd-8d94-bab649cd5dc0")</span></span>

<span data-ttu-id="bff6a-133"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bff6a-133"></div>

<span> </span>

</div>

</div>

</span></span></div>

