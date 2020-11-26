---
title: 'Lync Server 2013: Verwalten von Kategorien, Chatrooms und Add-Ins'
description: 'Lync Server 2013: Verwalten von Kategorien, Räumen und Add-Ins.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing categories, rooms, and add-ins
ms:assetid: a9807031-7369-4a51-9369-6f09bec24141
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412799(v=OCS.15)
ms:contentKeyID: 48185100
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: ba09ed3e021ba24f424d28bbb2c5c379ab975741
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425955"
---
# <a name="managing-categories-rooms-and-add-ins-in-lync-server-2013"></a><span data-ttu-id="77995-103">Verwalten von Kategorien, Chatrooms und Add-Ins in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="77995-103">Managing categories, rooms, and add-ins in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="77995-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="77995-104">

<span> </span></span></span>

<span data-ttu-id="77995-105">_**Letztes Änderungsdatum des Themas:** 2012-10-06_</span><span class="sxs-lookup"><span data-stu-id="77995-105">_**Topic Last Modified:** 2012-10-06_</span></span>

<span data-ttu-id="77995-106">In der lync Server 2013-Systemsteuerung oder mithilfe von Windows PowerShell-Cmdlets können beständige chatadministratoren mithilfe der **beständigen Chat** Seite Kategorien und Add-Ins erstellen. Zum Verwalten beständiger Chatrooms können Administratoren Windows PowerShell-Cmdlets verwenden.</span><span class="sxs-lookup"><span data-stu-id="77995-106">In Lync Server 2013 Control Panel, or by using Windows PowerShell cmdlets, Persistent Chat Administrators can use the **Persistent Chat** page to create categories and add-ins. For managing Persistent Chat rooms, Administrators can use Windows PowerShell cmdlets.</span></span> <span data-ttu-id="77995-107">Wenn der Administrator für beständigen Chat auch SIP-fähig ist, können Sie alternativ den lync-Client verwenden, um eine Webseite zum Erstellen und Verwalten von Chatrooms zu starten.</span><span class="sxs-lookup"><span data-stu-id="77995-107">Alternatively, if the Persistent Chat administrator is also SIP-enabled, they can use the Lync client to launch a web page to create and manage chat rooms.</span></span>

<span data-ttu-id="77995-108">In den folgenden Themen wird beschrieben, wie Sie Kategorien und Chatrooms erstellen und verwenden.</span><span class="sxs-lookup"><span data-stu-id="77995-108">The following topics describe how to create and work with categories and chat rooms.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="77995-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="77995-109">In This Section</span></span>

  - [<span data-ttu-id="77995-110">Erstellen oder Bearbeiten einer neuen Kategorie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="77995-110">Creating or editing a new category in Lync Server 2013</span></span>](lync-server-2013-creating-or-editing-a-new-category.md)

  - [<span data-ttu-id="77995-111">Erstellen oder Bearbeiten eines neuen Chatrooms in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="77995-111">Creating or editing a new room in Lync Server 2013</span></span>](lync-server-2013-creating-or-editing-a-new-room.md)

  - [<span data-ttu-id="77995-112">Erstellen von neuen Add-Ins für Chatrooms in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="77995-112">Creating new add-ins for rooms in Lync Server 2013</span></span>](lync-server-2013-creating-new-add-ins-for-rooms.md)

  - [<span data-ttu-id="77995-113">Festlegen der Benutzer in Lync Server 2013, die in einem Auditoriumchatroom Nachrichten veröffentlichen können</span><span class="sxs-lookup"><span data-stu-id="77995-113">Setting who can post messages in an auditorium chat room in Lync Server 2013</span></span>](lync-server-2013-setting-who-can-post-messages-in-an-auditorium-chat-room.md)

  - [<span data-ttu-id="77995-114">Deaktivieren oder Aktivieren eines Chatrooms in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="77995-114">Disabling or enabling a chat room in Lync Server 2013</span></span>](lync-server-2013-disabling-or-enabling-a-chat-room.md)

  - [<span data-ttu-id="77995-115">Verschieben eines Chatrooms von einer Kategorie in eine andere in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="77995-115">Moving a chat room from one category to another in Lync Server 2013</span></span>](lync-server-2013-moving-a-chat-room-from-one-category-to-another.md)

  - [<span data-ttu-id="77995-116">Löschen eines Chatrooms oder einer Kategorie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="77995-116">Deleting a chat room or category in Lync Server 2013</span></span>](lync-server-2013-deleting-a-chat-room-or-category.md)

  - [<span data-ttu-id="77995-117">Löschen einer Nachricht oder Löschen von veralteten Nachrichten in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="77995-117">Deleting a message or purging obsolete messages in Lync Server 2013</span></span>](lync-server-2013-deleting-a-message-or-purging-obsolete-messages.md)

<span data-ttu-id="77995-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="77995-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

