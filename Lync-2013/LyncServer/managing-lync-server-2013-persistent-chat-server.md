---
title: Verwalten von Lync Server 2013 Persistent Chat Server
description: Verwalten von lync Server 2013, beständiger Chat Server
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Lync Server 2013, Persistent Chat Server
ms:assetid: 82befdc6-5d32-45f1-bfd7-aaedffed1ab8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398657(v=OCS.15)
ms:contentKeyID: 48184672
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fe5306c79c738d61b70c3dd079fb55650e6fdae9
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446906"
---
# <a name="managing-lync-server-2013-persistent-chat-server"></a><span data-ttu-id="e6bb9-103">Verwalten von Lync Server 2013 Persistent Chat Server</span><span class="sxs-lookup"><span data-stu-id="e6bb9-103">Managing Lync Server 2013, Persistent Chat Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e6bb9-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e6bb9-104">

<span> </span></span></span>

<span data-ttu-id="e6bb9-105">_**Letztes Änderungsdatum des Themas:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="e6bb9-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="e6bb9-106">Sie können lync Server 2013, beständiger Chat Server verwenden, um mehreren Benutzern die Teilnahme an Unterhaltungen zu ermöglichen, in denen Sie Inhalte zu bestimmten Themen, einschließlich Text, Links und Dateien, Posten und darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e6bb9-106">You can use Lync Server 2013, Persistent Chat Server to enable multiple users to participate in conversations in which they post and access content about specific topics, including text, links, and files.</span></span> <span data-ttu-id="e6bb9-107">Obwohl Benutzer während einer Sitzung in Echtzeit kommunizieren können, ist der Inhalt jeder Sitzung persistent, was bedeutet, dass Sie nach dem Ende einer Sitzung weiterhin zur Verfügung steht.</span><span class="sxs-lookup"><span data-stu-id="e6bb9-107">Although users can communicate in real time during a session, the content of each session is persistent, which means that it continues to be available after a session ends.</span></span>

<span data-ttu-id="e6bb9-108">Der Inhalt beständiger Chatrooms besteht in erster Linie aus kurzen Textnachrichten, kann aber auch längere Nachrichten, die als Text *Abschnitte* bezeichnet werden, sowie Links, Emoticons und hochgeladene Dokumente umfassen.</span><span class="sxs-lookup"><span data-stu-id="e6bb9-108">The content of Persistent Chat rooms consists primarily of short text messages, although it can include longer messages, referred to as *stories*, and also hyperlinks, emoticons, and uploaded documents.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="e6bb9-109">Dateiupload und-Download wird vom lync 2013-Client nicht unterstützt. Sie wird jedoch weiterhin von lync Server 2013, beständiger Chat Server, unterstützt.</span><span class="sxs-lookup"><span data-stu-id="e6bb9-109">File upload and download is not supported by the Lync 2013 client; however, it is still supported by Lync Server 2013, Persistent Chat Server.</span></span> <span data-ttu-id="e6bb9-110">Der Legacy-Gruppen-Chat-Client kann Dateien Posten und anzeigen, aber wenn auf den gleichen Chatroom über den lync 2013-Client zugegriffen wird, kann er nicht auf die Dateien zugreifen.</span><span class="sxs-lookup"><span data-stu-id="e6bb9-110">The legacy Group Chat client can post and view files, but if the same chat room is accessed via the Lync 2013 client, it will not be able to access the files.</span></span>



</div>

<span data-ttu-id="e6bb9-111">Der Zugriff auf einen Chatroom wird durch eine Mitgliedschaftsliste gesteuert.</span><span class="sxs-lookup"><span data-stu-id="e6bb9-111">Access to a chat room is controlled by a membership list.</span></span> <span data-ttu-id="e6bb9-112">Der gesamte Verlauf des Chatrooms steht jedem Mitglied zur chronologischen Überprüfung oder Volltextsuche zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="e6bb9-112">The entire chat room history is available to any member for chronological review or full-text search.</span></span> <span data-ttu-id="e6bb9-113">Details zur Verwendung des beständigen Chat-Clients finden Sie unter [Planen der Clients in lync Server 2013](lync-server-2013-planning-for-clients.md) in der Planungsdokumentation und [Bereitstellen von Clients und Geräten in lync Server 2013](lync-server-2013-deploying-clients-and-devices.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="e6bb9-113">For details about using the Persistent Chat client, see [Planning for clients in Lync Server 2013](lync-server-2013-planning-for-clients.md) in the Planning documentation, and [Deploying clients and devices in Lync Server 2013](lync-server-2013-deploying-clients-and-devices.md) in the Deployment documentation.</span></span>

<span data-ttu-id="e6bb9-114">Wenn Sie den Server für beständigen Chat für Ihre Organisation einrichten, geben Sie die anfängliche Konfiguration während der Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="e6bb9-114">When you set up Persistent Chat Server for your organization, you specify the initial configuration during deployment.</span></span> <span data-ttu-id="e6bb9-115">Es kann jedoch vorkommen, dass Sie ändern möchten, wie Sie die Unterstützung für beständigen Chat Server implementieren.</span><span class="sxs-lookup"><span data-stu-id="e6bb9-115">However, there may be times when you want to change how you implement Persistent Chat Server support.</span></span> <span data-ttu-id="e6bb9-116">So können Sie beispielsweise für ein bestimmtes Team oder eine bestimmte Gruppe in Ihrer Organisation die Unterstützung für beständigen Chat Server und die Steuerelemente anders einrichten.</span><span class="sxs-lookup"><span data-stu-id="e6bb9-116">For example, you may need to set up Persistent Chat Server support and controls differently for a specific team or group within your organization.</span></span> <span data-ttu-id="e6bb9-117">Dieser Abschnitt enthält Informationen und Verfahren, die Ihnen bei der Anpassung ihrer beständigen Chat Server Bereitstellung helfen.</span><span class="sxs-lookup"><span data-stu-id="e6bb9-117">This section provides information and procedures to help you customize your Persistent Chat Server deployment.</span></span> <span data-ttu-id="e6bb9-118">Details zu den Features und Funktionen, die Sie für den Server für beständigen Chat konfigurieren können, finden Sie unter [Definieren der Anforderungen Ihrer Organisation für den beständigen Chat Server in lync Server 2013](lync-server-2013-defining-your-requirements-for-persistent-chat-server.md) in der Planungsdokumentation und [Funktionsweise des beständigen Chat Servers in lync Server 2013](lync-server-2013-how-persistent-chat-server-works.md) in der Planungsdokumentation, Bereitstellungsdokumentation oder in der Betriebsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="e6bb9-118">For details about the features and functionality that you can configure for Persistent Chat Server, see [Defining your organization's requirements for Persistent Chat Server in Lync Server 2013](lync-server-2013-defining-your-requirements-for-persistent-chat-server.md) in the Planning documentation, and [How Persistent Chat Server works in Lync Server 2013](lync-server-2013-how-persistent-chat-server-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span> <span data-ttu-id="e6bb9-119">Details zum Bereitstellen des beständigen Chat Servers für lync Server 2013 finden Sie unter [Bereitstellen eines beständigen Chat Servers in lync Server 2013](lync-server-2013-deploying-persistent-chat-server.md) in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="e6bb9-119">For details about deploying Persistent Chat Server for Lync Server 2013, see [Deploying Persistent Chat Server in Lync Server 2013](lync-server-2013-deploying-persistent-chat-server.md) in the Deployment documentation.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="e6bb9-120">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="e6bb9-120">In This Section</span></span>

  - [<span data-ttu-id="e6bb9-121">Funktionsweise des beständigen Chat Servers in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e6bb9-121">How Persistent Chat Server works in Lync Server 2013</span></span>](lync-server-2013-how-persistent-chat-server-works.md)

  - [<span data-ttu-id="e6bb9-122">Verwenden von Kategorien zur Verwaltung des Servers für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="e6bb9-122">Using categories to administer Persistent Chat Server</span></span>](using-categories-to-administer-persistent-chat-server.md)

  - [<span data-ttu-id="e6bb9-123">Grundlegendes zur dauerhaften Chat Mitgliedschaft</span><span class="sxs-lookup"><span data-stu-id="e6bb9-123">Understanding Persistent Chat membership</span></span>](understanding-persistent-chat-membership.md)

  - [<span data-ttu-id="e6bb9-124">Bewährte Methoden für den Server für beständigen Chat</span><span class="sxs-lookup"><span data-stu-id="e6bb9-124">Persistent Chat Server best practices</span></span>](persistent-chat-server-best-practices.md)

  - [<span data-ttu-id="e6bb9-125">Verwalten von Kategorien, Chatrooms und Add-Ins in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e6bb9-125">Managing categories, rooms, and add-ins in Lync Server 2013</span></span>](lync-server-2013-managing-categories-rooms-and-add-ins.md)

  - [<span data-ttu-id="e6bb9-126">Verwalten des Benutzerzugriffs für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e6bb9-126">Managing Persistent Chat user access in Lync Server 2013</span></span>](lync-server-2013-managing-persistent-chat-user-access.md)

  - [<span data-ttu-id="e6bb9-127">Betreiben und Verwalten des Systems für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e6bb9-127">Operating and maintaining the Persistent Chat system in Lync Server 2013</span></span>](lync-server-2013-operating-and-maintaining-the-persistent-chat-system.md)

<span data-ttu-id="e6bb9-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e6bb9-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

