---
title: Verwenden von Kategorien zur Verwaltung des Servers für beständigen Chat
description: Verwenden von Kategorien zum Verwalten des beständigen Chat Servers
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Using categories to administer Persistent Chat Server
ms:assetid: dfcb3ad1-da90-467e-b08c-f4e68673b7b5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398988(v=OCS.15)
ms:contentKeyID: 48185628
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 181ecba944a042e3598b2964ad233590cf63349e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443167"
---
# <a name="using-categories-to-administer-persistent-chat-server"></a><span data-ttu-id="f7771-103">Verwenden von Kategorien zur Verwaltung des Servers für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="f7771-103">Using categories to administer Persistent Chat Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f7771-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f7771-104">

<span> </span></span></span>

<span data-ttu-id="f7771-105">_**Letztes Änderungsdatum des Themas:** 2013-10-01_</span><span class="sxs-lookup"><span data-stu-id="f7771-105">_**Topic Last Modified:** 2013-10-01_</span></span>

<span data-ttu-id="f7771-106">Ihre beständige Chat Server-Bereitstellung kann viele gleichzeitig beständige Chatrooms hosten.</span><span class="sxs-lookup"><span data-stu-id="f7771-106">Your Persistent Chat Server deployment can host many concurrent Persistent Chat rooms.</span></span> <span data-ttu-id="f7771-107">Chatrooms können in Kategoriegruppen auf dem Server angeordnet werden.</span><span class="sxs-lookup"><span data-stu-id="f7771-107">Chat rooms can be organized into a set of categories on the server.</span></span> <span data-ttu-id="f7771-108">Jeder Chatroom gehört einer Kategorie an und übernimmt die Einstellungen dieser Kategorie.</span><span class="sxs-lookup"><span data-stu-id="f7771-108">Each chat room belongs to one category, and inherits some settings from that category.</span></span> <span data-ttu-id="f7771-109">Diese Anordnung ergibt eine hilfreiche Struktur zur Identifikation von Konversationen basierend auf ihrem geschäftlichen Anlass und ermöglicht die delegierte Administration und eine einfachere Verwaltung.</span><span class="sxs-lookup"><span data-stu-id="f7771-109">This organization creates a useful structure for identifying conversations, based on their business purpose, and facilitates delegated administration and simplified management.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f7771-110">Obwohl viele Verwaltungsfeatures von Chatrooms in Computern, auf denen persistenter Chat (lync-Client) ausgeführt wird, für den Benutzer verfügbar sind, müssen beständige chatadministratoren (in der Rolle <STRONG>cspersistentchatadministrator</STRONG> ) die lync Server-Systemsteuerung oder Windows PowerShell-Cmdlets verwenden, um Kategorien zu erstellen oder zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="f7771-110">Although many of the management features of chat rooms are available in computers running Persistent Chat (Lync client) for the user, Persistent Chat Administrators (in the <STRONG>cspersistentchatadministrator</STRONG> role) must use the Lync Server Control Panel or Windows PowerShell cmdlets to create or manage categories.</span></span>



</div>

<span data-ttu-id="f7771-111">Beständige Chat Administratoren verwenden die lync Server Control Panel-oder Windows PowerShell-Cmdlets zum Erstellen und Verwalten von Kategorien sowie zum Entwerfen des Zugriffs für Chatrooms für die Benutzer in Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="f7771-111">Persistent Chat administrators use Lync Server Control Panel or Windows PowerShell cmdlets to create and manage categories, and to design access for chat rooms for the users in their organization.</span></span>

<span data-ttu-id="f7771-112">Beständige Chatroom-Manager, die in der Lage sind, einen oder mehrere Chatrooms zu verwalten, können mithilfe des lync-Clients eine Webanwendung für die Raumverwaltung starten, um Räume zu erstellen und zu verwalten (oder Kunden können benutzerdefinierte Lösungen und Workflows erstellen, die aufgerufen werden sollen).</span><span class="sxs-lookup"><span data-stu-id="f7771-112">Persistent Chat room managers, who have the ability to manage one or more chat rooms, can use the Lync client to launch a room management Web application to create and manage rooms (or customers can create custom solutions and workflows to be invoked).</span></span> <span data-ttu-id="f7771-113">Administratoren für beständigen Chat können auch die lync Server Control Panel-oder Windows PowerShell-Cmdlets verwenden, um Räume zu erstellen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="f7771-113">Persistent Chat administrators can also use Lync Server Control Panel or Windows PowerShell cmdlets to create and manage rooms.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="f7771-114">Ein beständiger Chatroom kann nicht den gleichen Namen wie die Kategorie "beständiger Chat" haben.</span><span class="sxs-lookup"><span data-stu-id="f7771-114">A Persistent Chat room cannot have the same name as a Persistent Chat category.</span></span>



</div>

<span data-ttu-id="f7771-p103">Chatroommanager können Änderungen an allen Chatroomeigenschaften vornehmen. Die Kategorie des Chatrooms können Sie jedoch nicht ändern. Sie können nicht am Ausführen der folgenden Aktionen gehindert werden:</span><span class="sxs-lookup"><span data-stu-id="f7771-p103">Chat room managers can make changes to all chat room properties, except for changing the category of the room. They cannot be restricted from performing the following actions:</span></span>

  - <span data-ttu-id="f7771-117">Deaktivieren eines Chatrooms</span><span class="sxs-lookup"><span data-stu-id="f7771-117">Disabling a chat room</span></span>

  - <span data-ttu-id="f7771-118">Ändern des Namens eines Chatrooms</span><span class="sxs-lookup"><span data-stu-id="f7771-118">Changing a chat room name</span></span>

  - <span data-ttu-id="f7771-119">Ändern der Beschreibung eines Chatrooms</span><span class="sxs-lookup"><span data-stu-id="f7771-119">Changing a chat room description</span></span>

  - <span data-ttu-id="f7771-120">Ändern des Chatroomtyps („Auditorium“ bzw. „Normal“)</span><span class="sxs-lookup"><span data-stu-id="f7771-120">Changing a chat room type (Auditorium versus Normal)</span></span>

  - <span data-ttu-id="f7771-121">Ändern des Datenschutzes eines Chatrooms (offen, geschlossen bzw. geheim)</span><span class="sxs-lookup"><span data-stu-id="f7771-121">Changing the privacy of a room (open versus closed versus secret)</span></span>

  - <span data-ttu-id="f7771-122">Hinzufügen oder Entfernen von Mitgliedern</span><span class="sxs-lookup"><span data-stu-id="f7771-122">Adding or removing members</span></span>

  - <span data-ttu-id="f7771-123">Hinzufügen oder Entfernen von Chatroommanagern</span><span class="sxs-lookup"><span data-stu-id="f7771-123">Adding or removing chat room managers</span></span>

  - <span data-ttu-id="f7771-124">Hinzufügen oder Entfernen eines Add-Ins</span><span class="sxs-lookup"><span data-stu-id="f7771-124">Adding or removing an add-in</span></span>

  - <span data-ttu-id="f7771-125">Ändern von Einstellungen wie z. B. Einladungen (je nachdem, was durch die Kategorie zulässig ist)</span><span class="sxs-lookup"><span data-stu-id="f7771-125">Changing settings such as invitations (according to what’s permitted by the category)</span></span>

<div>

## <a name="delegated-administration"></a><span data-ttu-id="f7771-126">Delegierte Administration</span><span class="sxs-lookup"><span data-stu-id="f7771-126">Delegated Administration</span></span>

<span data-ttu-id="f7771-127">Das Erstellen und verwalten beständiger Chatrooms ist mit der korrekten Verwendung von Kategorien viel einfacher.</span><span class="sxs-lookup"><span data-stu-id="f7771-127">Creating and managing Persistent Chat rooms is much easier with the correct use of categories.</span></span> <span data-ttu-id="f7771-128">Ein beständiger Chat-Administrator kann **AllowedMembers** und **Creators** für jede Kategorie definieren und auch die Standardeinstellungen und-Verhaltensweisen für Chatrooms definieren, die auf alle Chatrooms angewendet werden, die in der Kategorie erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="f7771-128">A Persistent Chat Administrator can define **AllowedMembers** and **Creators** for each category, and can also define the default chat room settings and behaviors that will be applied to all chat rooms created in the category.</span></span> <span data-ttu-id="f7771-129">Beständige Chat Administratoren erstellen und verwalten Kategorien mithilfe der lync Server Control Panel-oder Windows PowerShell-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="f7771-129">Persistent Chat administrators create and manage categories by using Lync Server Control Panel or Windows PowerShell cmdlets.</span></span>

<span data-ttu-id="f7771-p105">Benutzer, Organisationseinheiten (Organizational Units, OUs) und Benutzergruppen, die als Ersteller einer Kategorie definiert werden, sind die einzigen Personen und Benutzergruppen, die Chatrooms in dieser Kategorie erstellen dürfen. Nachdem die Kategorie erstellt wurde, können sie Benutzer, Organisationseinheiten und Benutzergruppen in der Liste **Zugelassene Mitglieder** der Kategorie als Chatroommanager und Mitglieder auswählen, die den Chatroom verwalten und an diesem teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="f7771-p105">Users, Organizational Units (OUs), and user groups that are identified as Creators of the category are the only individuals and groups that are allowed to create rooms in the category. After the category is created, they can choose users, OUs, and user groups from the category’s **AllowedMembers** list as chat room managers and members to manage and participate in the room.</span></span>

<span data-ttu-id="f7771-132">Chatrooms, die in einer Kategorie erstellt wurden, befolgen die Richtlinien und Einstellungen, die von der Kategorie erzwungen werden (beispielsweise wer in der Mitgliedschaft des Chatrooms sein kann, wer den Chatroom verwalten kann, ob Dateiuploads zulässig sind, ob Einladungen gesendet werden usw.).</span><span class="sxs-lookup"><span data-stu-id="f7771-132">Chat rooms that are created in a category adhere to the policies and settings enforced by the category (such as who can be in the room’s membership, who can manage the room, whether file uploads are allowed, whether invitations are sent, and so on).</span></span>

<span data-ttu-id="f7771-133"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f7771-133"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

