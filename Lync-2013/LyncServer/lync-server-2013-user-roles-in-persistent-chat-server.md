---
title: 'Lync Server 2013: Benutzerrollen im beständigen Chat Server'
description: 'Lync Server 2013: Benutzerrollen im Server für beständigen Chat.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: User roles in Persistent Chat Server
ms:assetid: 343a0563-9ca5-4ad0-b4f3-a72f1d7f1a81
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ676774(v=OCS.15)
ms:contentKeyID: 49361095
ms.date: 03/19/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: aed64aaa9129e6667cd138bc4365acfb2a64d52c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439158"
---
# <a name="user-roles-in-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="9e881-103">Benutzerrollen im Server für beständigen Chat in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="9e881-103">User roles in Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="9e881-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="9e881-104">

<span> </span></span></span>

<span data-ttu-id="9e881-105">_**Letztes Änderungsdatum des Themas:** 2015-03-19_</span><span class="sxs-lookup"><span data-stu-id="9e881-105">_**Topic Last Modified:** 2015-03-19_</span></span>

<span data-ttu-id="9e881-106">Der Server für beständigen Chat bietet das Konzept der zugelassenen/abgelehnten Mitglieder, das auf beständige Chatkategorien und Steuerelemente angewendet wird, die auf Räume in einer bestimmten Kategorie zugreifen können.</span><span class="sxs-lookup"><span data-stu-id="9e881-106">Persistent Chat Server provides the concept of Allowed/Denied members, which applies to Persistent Chat categories and controls who can access rooms in a particular category.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="9e881-107">Zulässige/abgelehnte Mitglieder in einer Kategorie ist nicht mit einer <STRONG>Mitglieds</STRONG> Rolle identisch, die für einen beständigen Chatroom gilt.</span><span class="sxs-lookup"><span data-stu-id="9e881-107">Allowed/Denied members in a Category is not the same as a <STRONG>Member</STRONG> role, which applies to a Persistent Chat room.</span></span><BR><span data-ttu-id="9e881-108">In suchen werden alle geöffneten und geschlossenen Chatrooms angezeigt, für die der Benutzer, der die Suche ausführt, in der Liste zugelassene/abgelehnte Mitglieder aufgeführt ist.</span><span class="sxs-lookup"><span data-stu-id="9e881-108">Searches display all open and closed chat rooms for which the user performing the search is in the Allowed/Denied member list.</span></span> <span data-ttu-id="9e881-109">Geheime Chatrooms werden nur angezeigt, wenn der Benutzer, der die Suche durchführt, Mitglied des geheimen Chatrooms ist.</span><span class="sxs-lookup"><span data-stu-id="9e881-109">Secret rooms are not displayed unless the user who performs the search is a member of the secret room.</span></span> <span data-ttu-id="9e881-110">Der Benutzer kann nur nach Chatrooms suchen, bei denen er bereits Mitglied ist oder für die er eine Mitgliedschaft anfordern kann.</span><span class="sxs-lookup"><span data-stu-id="9e881-110">The user can search only for rooms that he or she is already a member of, or those for which they can request membership.</span></span>



</div>

<span data-ttu-id="9e881-111">Das primäre Argument für das Konzept der zugelassenen/verweigerten Mitglieder sind ethische Mauern.</span><span class="sxs-lookup"><span data-stu-id="9e881-111">The primary rationale for the concept of Allowed/Denied Members is ethical walls.</span></span> <span data-ttu-id="9e881-112">Beispielsweise ist es bei Banken und Finanzinstitutionen üblich, dass beim Implementieren von Richtlinien und Konventionen Chinesische Mauern definiert werden, die verhindern, dass Händler und Analysten Mitteilungen und Informationen austauschen.</span><span class="sxs-lookup"><span data-stu-id="9e881-112">For example, it is common in banking and financial institutions to have ethical boundaries that prevent traders and analysts from sharing communications while implementing policies and conventions.</span></span> <span data-ttu-id="9e881-113">Um dieser Anforderung nachzukommen, kann ein Administrator Kategorien erstellen, sodass in einer Kategorie Chatrooms von Händlern und in einer anderen Kategorie Chatrooms von Analysten erstellt und verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="9e881-113">To address this requirement, an administrator can create categories so that one category allows rooms to be created and used by traders, and another category allows rooms to be created and used by analysts.</span></span> <span data-ttu-id="9e881-114">Wenn diese Einschränkung in das System vorgesehen ist, ist es nicht möglich, einen Benutzer als Mitglied des Chatrooms hinzuzufügen, wenn die übergeordnete Kategorie Dies verhindert.</span><span class="sxs-lookup"><span data-stu-id="9e881-114">With this constraint is designed into the system prohibits adding a user as a member of the room if the parent category prevents it.</span></span>

<span data-ttu-id="9e881-115">Im folgenden werden die vier Benutzerrollen beständiger Chat Server:</span><span class="sxs-lookup"><span data-stu-id="9e881-115">Following are the four user roles Persistent Chat Server:</span></span>

  - <span data-ttu-id="9e881-116">**Creator:** Benutzer, die über die Berechtigung zum Erstellen von Chatrooms verfügen.</span><span class="sxs-lookup"><span data-stu-id="9e881-116">**Creator:** Users who have permissions to create chat rooms.</span></span> <span data-ttu-id="9e881-117">Diese Benutzer befinden sich in der Liste der Ersteller bestimmter Kategorien: Sie können Chatrooms in dieser Kategorie erstellen, und Sie können auch Mitgliedschaften entsprechend der Kategorie zuweisen und Managern zuweisen, dass Sie den Chatroom verwalten möchten.</span><span class="sxs-lookup"><span data-stu-id="9e881-117">These users are in the Creators list of certain categories: they can create chat rooms in that category, and they can also assign membership according to the category, and assign managers to manage the chat room.</span></span> <span data-ttu-id="9e881-118">Der Benutzer, der einen Chatroom erstellt, wird automatisch als Manager des Chatrooms hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="9e881-118">The user who creates a chat room is automatically added as a manager of the room.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="9e881-p104">Als Ersteller besitzt ein Benutzer lediglich die Rechte zum Erstellen von Chatrooms. Durch die automatische Heraufstufung zum Manager erhält der Ersteller die Berechtigung, Mitgliedschaften, Manager usw. für die erstellten Chatdienste zu verfeinern.</span><span class="sxs-lookup"><span data-stu-id="9e881-p104">Being a Creator simply provides rights for creating chat rooms. It is the automatic promotion to Manager that enables the Creator to further refine memberships, managers, and so on, on the created chat services.</span></span>

    
    </div>
    
    <span data-ttu-id="9e881-121">Mit dieser Rolle können Sie steuern, wer die Chatrooms in Ihrer Organisation erstellt. Dies ist insbesondere praktisch, wenn Sie das Erstellen von Chatrooms zentral verwalten möchten, um Richtlinien und Konventionen zu erzwingen und anschließend die Chatroomverwaltung an andere Benutzer in der Organisation delegieren möchten.</span><span class="sxs-lookup"><span data-stu-id="9e881-121">This role exists to give you the option of controlling who creates chat rooms in your organization, particularly if you want to centrally manage creating chat rooms to enforce policies and conventions, and subsequently delegate the chat room management to other users in the organization.</span></span>

  - <span data-ttu-id="9e881-122">**Manager:** Benutzer, die die Eigenschaften eines Chatrooms verwalten.</span><span class="sxs-lookup"><span data-stu-id="9e881-122">**Manager:** Users who manage properties of a chat room.</span></span> <span data-ttu-id="9e881-123">Chatroommanager können die Mitgliederliste ändern (Mitglieder hinzufügen und entfernen) und die Chatroommanager-Liste ändern (Manager hinzufügen und entfernen).</span><span class="sxs-lookup"><span data-stu-id="9e881-123">Chat room managers can modify the member list (add and remove members), and modify the chat room managers list (add and remove managers).</span></span> <span data-ttu-id="9e881-124">Chatroommanager können sich selbst der Mitglieder- oder Referentenliste (für ein Auditorium) hinzufügen, damit sie am Chatroom teilnehmen können.</span><span class="sxs-lookup"><span data-stu-id="9e881-124">Chat room managers can add themselves to the members or presenters list (for auditorium rooms) so they can participate in the chat room.</span></span> <span data-ttu-id="9e881-125">Chatroommanager können Chatrooms auch deaktivieren (Administratoren können deaktivierte Chatrooms abfragen und dauerhaft löschen).</span><span class="sxs-lookup"><span data-stu-id="9e881-125">Chat room managers can also disable chat rooms (administrators can query for disabled chat rooms and can permanently delete them).</span></span> <span data-ttu-id="9e881-126">Manager können bis auf die Chatroomkategorie alle Eigenschaften eines Chatrooms ändern.</span><span class="sxs-lookup"><span data-stu-id="9e881-126">Managers can change all the properties of a chat room, except the category of the chat room.</span></span> <span data-ttu-id="9e881-127">Nur der Administrator des beständigen Chats kann die Kategorie nach dem Erstellen des Chatrooms ändern.</span><span class="sxs-lookup"><span data-stu-id="9e881-127">Only the Persistent Chat Administrator can change the category after the chat room has been created.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="9e881-128">Wenn der Manager in einer anderen Kategorie auch der Ersteller ist, kann der Manager die Kategorie in eine Kategorie ändern, für die eine Berechtigung zum Erstellen von Chatrooms besitzt.</span><span class="sxs-lookup"><span data-stu-id="9e881-128">If the manager is also a Creator in another category, he or she can change the category to one where they are authorized to create rooms.</span></span>

    
    </div>

  - <span data-ttu-id="9e881-129">**Mitglied:** Benutzer, die Mitglieder eines Chatrooms sind.</span><span class="sxs-lookup"><span data-stu-id="9e881-129">**Member:** Users who are members of a chat room.</span></span> <span data-ttu-id="9e881-130">Diese Benutzer können die Chatrooms im Verzeichnis anzeigen (auch wenn der Chatroom geheim ist) sowie den Chatroom abonnieren (einschließlich metadateneinstellungen wie ungelesene Nachrichten, Ego-Filter und Keyword-Filter) und am Chatroom teilnehmen (kann Posten, es sei denn, der Raum ist ein Auditorium, in dem nur Referenten Beiträge Posten, Inhalte abrufen und suchen können).</span><span class="sxs-lookup"><span data-stu-id="9e881-130">These users can see the chat rooms in the directory (even if the chat room is secret), as well as subscribe to the chat room (including metadata options such as unread messages, ego filters, and keyword filters), and participate in the chat room (can post, unless the room is an auditorium room where only presenters can post, get content, and search).</span></span> <span data-ttu-id="9e881-131">Benutzer, die keine Mitglieder des Chatrooms sind, können nach dem Chatroom suchen, wenn Sie sich in der Liste der zulässigen Mitglieder der Kategorie befinden, müssen aber Zugriff auf die Teilnahme an diesen Chatrooms anfordern, um auf Inhalte zugreifen zu können.</span><span class="sxs-lookup"><span data-stu-id="9e881-131">Users who aren’t members of the chat room can search for the chat room if they are in the Allowed Members list of the category, but need to request access to join these chat rooms to access content.</span></span> <span data-ttu-id="9e881-132">(Es sind keine Zugriffs-oder Genehmigungsanfragen in das System integriert; diese werden extern per e-Mail, Telefon oder anderen Kontaktarten durchgeführt.)</span><span class="sxs-lookup"><span data-stu-id="9e881-132">(There is no request access or approvals built into the system; these are done externally by email, phone, or other forms of contact.)</span></span>

  - <span data-ttu-id="9e881-133">**Referent:** Benutzer, die in einem Auditorium-Chatroom Posten können</span><span class="sxs-lookup"><span data-stu-id="9e881-133">**Presenter:** Users who can post to an auditorium room.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="9e881-134">Der beständige Chat Server ermöglicht Benutzern, Chatrooms für eine bestimmte Website zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="9e881-134">Persistent Chat Server lets users create and manage chat room for a specific site.</span></span> <span data-ttu-id="9e881-135">Benutzer können Chatrooms jedoch nicht auf anderen Websites innerhalb derselben Topologie erstellen oder verwalten.</span><span class="sxs-lookup"><span data-stu-id="9e881-135">Users cannot, however, create or manage chat rooms on other sites within the same topology.</span></span> <span data-ttu-id="9e881-136">Stellen Sie sicher, dass Sie für alle Websites in Ihrer Organisation Chatroom-Ersteller und-Manager angeben.</span><span class="sxs-lookup"><span data-stu-id="9e881-136">Be sure to specify chat room Creators and Managers for all the sites in your organization.</span></span>



</div>

<span data-ttu-id="9e881-137">Die folgenden Rollen sind Administratorrollen für den Server für beständigen Chat:</span><span class="sxs-lookup"><span data-stu-id="9e881-137">The following roles are administrator roles for Persistent Chat Server:</span></span>

  - <span data-ttu-id="9e881-138">**Administrator für beständigen Chat (CsPersistentChatAdministrator):** Hierbei handelt es sich um eine neue Role-Based zugriffssteuerungsrolle, um den Server für beständigen Chat zu verwalten und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="9e881-138">**Persistent Chat Administrator (CsPersistentChatAdministrator):** This is a new Role-Based Access Control (RBAC) role to administer and manage Persistent Chat Server.</span></span> <span data-ttu-id="9e881-139">Benutzer oder Sicherheitsgruppen, die als CsPersistentChatAdministrator bezeichnet werden, können beständigen Chat Server mithilfe von Windows PowerShell-Cmdlets remote verwalten (also von einem anderen Computer als dem beständigen Chat Server).</span><span class="sxs-lookup"><span data-stu-id="9e881-139">Users or security groups designated as CsPersistentChatAdministrator are able administer Persistent Chat Server by using Windows PowerShell cmdlets remotely (that is, from a computer other than the Persistent Chat Server).</span></span> <span data-ttu-id="9e881-140">Der beständige Chat Server überprüft, ob der Administrator des beständigen Chats Mitglied der lokalen Gruppe RTC Local Administrator auf dem Front-End-Server des beständigen Chats ist.</span><span class="sxs-lookup"><span data-stu-id="9e881-140">Persistent Chat Server checks that the Persistent Chat Administrator is member of the RTC Local administrator local group on the Persistent Chat Server Front End Server.</span></span>
    
    <span data-ttu-id="9e881-141">Die CsPersistentChatAdministrator-Rolle kann Chatrooms verwalten (alle Eigenschaften wie Mitgliedschaft, Manager, Kategorien, als deaktiviert kennzeichnen) sowie Chatrooms erstellen und verwalten, die definieren, wer Chatrooms erstellen und darauf zugreifen kann.</span><span class="sxs-lookup"><span data-stu-id="9e881-141">The CsPersistentChatAdministrator role can manage chat rooms (modify all properties including membership, managers, categories, mark rooms as disabled), as well as create and manage chat room categories that define who can create and access chat rooms.</span></span> <span data-ttu-id="9e881-142">Administratoren können Chatrooms auch als deaktiviert kennzeichnen und Chatrooms bereinigen, die nicht mehr aktiv sind.</span><span class="sxs-lookup"><span data-stu-id="9e881-142">Administrators can also mark chat rooms as disabled and clean up chat rooms that are no longer active.</span></span> <span data-ttu-id="9e881-143">Administratoren unterliegen nicht den Einschränkungen des Erstellers oder der zulässigen Mitglieder.</span><span class="sxs-lookup"><span data-stu-id="9e881-143">Administrators are not subject to the Creators or Allowed Members restrictions.</span></span> <span data-ttu-id="9e881-144">Administratoren können jede Art von Chatroom erstellen und sich selbst als Mitglied zu einem Chatroom hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="9e881-144">Administrators can create any kind of chat room and add themselves as a member to any chat room.</span></span> <span data-ttu-id="9e881-145">Administratoren können auch die Konfiguration beständiger Chats (Pooleigenschaften, globale Einstellungen und Kompatibilitäts Konfiguration) ändern und verwalten sowie die Migration von einer älteren Gruppen-Chat Server Bereitstellung auf den lync Server 2013-persistent-Chat Server planen und implementieren.</span><span class="sxs-lookup"><span data-stu-id="9e881-145">Administrators can also modify and manage Persistent Chat configuration (pool properties, global settings, and compliance configuration) and can also plan and implement migration from an older Group Chat Server deployment to Lync Server 2013 Persistent Chat Server.</span></span>

  - <span data-ttu-id="9e881-146">**Lync-Administrator:** Gesamtunternehmens Administrator für lync Server 2013, der für die Bereitstellung verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="9e881-146">**Lync Administrator:** Overall enterprise administrator for Lync Server 2013 responsible for deployment.</span></span>

  - <span data-ttu-id="9e881-147">**Operations Manager:** Der Benutzer, der für die Verwaltung von alltäglichen Vorgängen verantwortlich ist.</span><span class="sxs-lookup"><span data-stu-id="9e881-147">**Operations Manager:** User responsible for managing day-to-day operations.</span></span>

  - <span data-ttu-id="9e881-148">**Drittanbieter-Entwickler und-Partner:** Entwickler von Drittanbietern erweitern das System, insbesondere die Bereitstellung einer ethischen Wandlösung für Gruppenunterhaltungen, Compliance-Unterstützung und Tools, Web/Mobile-Clients und ein Framework für die bot-Entwicklung.</span><span class="sxs-lookup"><span data-stu-id="9e881-148">**Third-party developers and partners:** Third-party developers extend the system, in particular providing an ethical wall solution for group conversations, compliance support and tools, web/mobile clients, and a framework for Bot development.</span></span>

<span data-ttu-id="9e881-149"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="9e881-149"></div>

<span> </span>

</div>

</div>

</span></span></div>

