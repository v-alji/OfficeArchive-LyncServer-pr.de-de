---
title: 'Lync Server 2013: Löschen eines Chatrooms oder einer Kategorie'
description: 'Lync Server 2013: Löschen eines Chatrooms oder einer Kategorie.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deleting a chat room or category
ms:assetid: adccb869-0015-4eba-ac73-718bac7843b5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ215881(v=OCS.15)
ms:contentKeyID: 48706009
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3ef89802171a1eeca7de18ff0a4eb8eb3895f1b9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430413"
---
# <a name="deleting-a-chat-room-or-category-in-lync-server-2013"></a><span data-ttu-id="21e2e-103">Löschen eines Chatrooms oder einer Kategorie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="21e2e-103">Deleting a chat room or category in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="21e2e-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="21e2e-104">

<span> </span></span></span>

<span data-ttu-id="21e2e-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="21e2e-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="21e2e-106">Beständige Chatrooms können gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="21e2e-106">Persistent Chat rooms can be deleted.</span></span> <span data-ttu-id="21e2e-107">Wenn Sie über einen Chatroom verfügen, der nicht mehr verwendet wird, können Sie ihn deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="21e2e-107">If you have a chat room that is no longer being used, you can disable it.</span></span> <span data-ttu-id="21e2e-108">Ausführliche Informationen finden Sie unter [deaktivieren oder Aktivieren eines Chatrooms in lync Server 2013](lync-server-2013-disabling-or-enabling-a-chat-room.md).</span><span class="sxs-lookup"><span data-stu-id="21e2e-108">For details, see [Disabling or enabling a chat room in Lync Server 2013](lync-server-2013-disabling-or-enabling-a-chat-room.md).</span></span>

<span data-ttu-id="21e2e-109">Ein Administrator für beständigen Chat kann nach deaktivierten Chatrooms suchen und die Chatrooms in regelmäßigen Abständen mit dem Windows PowerShell **-Cmdlet Remove-CsPersistentChatRoom** löschen und endgültig löschen.</span><span class="sxs-lookup"><span data-stu-id="21e2e-109">A Persistent Chat administrator can query for disabled chat rooms, and can periodically purge and permanently delete the chat rooms, by using the Windows PowerShell cmdlet, **Remove-CsPersistentChatRoom**.</span></span>

<span data-ttu-id="21e2e-110">Kategorien können gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="21e2e-110">Categories can be deleted.</span></span> <span data-ttu-id="21e2e-111">Um eine Kategorie zu löschen, müssen Sie jedoch zunächst entweder alle Chatrooms darunter löschen oder die Chatrooms in eine neue Kategorie verschieben, wodurch eine leere Kategorie zum Löschen bleibt.</span><span class="sxs-lookup"><span data-stu-id="21e2e-111">However, to delete a category, you must first either delete all chat rooms under it or move the chat rooms to a new category, leaving an empty category for deletion.</span></span> <span data-ttu-id="21e2e-112">Mit dem Server für beständigen Chat können Sie keine Kategorie löschen, die Chatrooms enthält.</span><span class="sxs-lookup"><span data-stu-id="21e2e-112">Persistent Chat Server does not allow you to delete a category that contains chat rooms.</span></span> <span data-ttu-id="21e2e-113">Ausführliche Informationen finden Sie unter [Verschieben eines Chatrooms von einer Kategorie in eine andere in lync Server 2013](lync-server-2013-moving-a-chat-room-from-one-category-to-another.md).</span><span class="sxs-lookup"><span data-stu-id="21e2e-113">For details, see [Moving a chat room from one category to another in Lync Server 2013](lync-server-2013-moving-a-chat-room-from-one-category-to-another.md).</span></span>

<span data-ttu-id="21e2e-114">Details zum Löschen von leeren Kategorien mithilfe der Windows PowerShell-Befehlszeilenoberfläche finden Sie unter "roomverwaltung" unter [Konfigurieren des beständigen Chat Servers mithilfe von Windows PowerShell-Cmdlets](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span><span class="sxs-lookup"><span data-stu-id="21e2e-114">For details about deleting empty categories by using the Windows PowerShell command-line interface, see "Room Management" in [Configuring Persistent Chat Server by using Windows PowerShell cmdlets](configuring-persistent-chat-server-by-using-windows-powershell-cmdlets.md).</span></span>

<span data-ttu-id="21e2e-115">Details zu Chatrooms und Kategorien finden Sie unter [Konfigurieren von Räumen in lync Server 2013](lync-server-2013-configure-rooms.md) und [Konfigurieren von Kategorien in lync Server 2013](lync-server-2013-configure-categories.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="21e2e-115">For details about chat rooms and categories, see [Configure rooms in Lync Server 2013](lync-server-2013-configure-rooms.md) and [Configure categories in Lync Server 2013](lync-server-2013-configure-categories.md) in the Deployment documentation.</span></span>

<span data-ttu-id="21e2e-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="21e2e-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

