---
title: 'Lync Server 2013: Planen für den Server für beständigen Chat'
description: 'Lync Server 2013: Planen des beständigen Chat Servers'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning for Persistent Chat Server
ms:assetid: 57b2f574-234e-4a5a-bb78-8823369ba79e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398381(v=OCS.15)
ms:contentKeyID: 48184190
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6944437492a1eee718a614369201c3548c95864a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424452"
---
# <a name="planning-for-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="a459c-103">Planen für den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a459c-103">Planning for Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a459c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a459c-104">

<span> </span></span></span>

<span data-ttu-id="a459c-105">_**Letztes Änderungsdatum des Themas:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="a459c-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="a459c-106">Sie können lync Server 2013, beständiger Chat Server verwenden, um mehreren Benutzern die Teilnahme an Unterhaltungen zu ermöglichen, in denen Sie Inhalte zu bestimmten Themen, einschließlich Text, Links und Dateien, Posten und darauf zugreifen.</span><span class="sxs-lookup"><span data-stu-id="a459c-106">You can use Lync Server 2013, Persistent Chat Server to enable multiple users to participate in conversations in which they post and access content about specific topics, including text, links, and files.</span></span> <span data-ttu-id="a459c-107">Benutzer können zwar während einer Sitzung in Echtzeit kommunizieren, der Inhalt der einzelnen Sitzungen ist jedoch dauerhaft, was bedeutet, dass er auch nach Beendigung einer Sitzung weiterhin verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="a459c-107">Although users can communicate in real time during a session, the content of each session is persistent, which means it continues to be available after a session ends.</span></span>

<span data-ttu-id="a459c-108">In diesem Abschnitt werden Planungsüberlegungen in einer lync Server 2013-Bereitstellung des beständigen Chats beschrieben, einschließlich definieren von Anforderungen, Identifizieren von Komponenten und unterstützten Topologien sowie Empfehlungen zur Bereitstellung.</span><span class="sxs-lookup"><span data-stu-id="a459c-108">This section describes planning considerations in a Lync Server 2013, Persistent Chat Server deployment, including defining requirements, identifying components and supported topologies, and deployment recommendations.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a459c-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a459c-109">In This Section</span></span>

  - [<span data-ttu-id="a459c-110">Übersicht über den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a459c-110">Overview of Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-overview-of-persistent-chat-server.md)

  - [<span data-ttu-id="a459c-111">Funktionsweise des beständigen Chat Servers in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a459c-111">How Persistent Chat Server works in Lync Server 2013</span></span>](lync-server-2013-how-persistent-chat-server-works.md)

  - [<span data-ttu-id="a459c-112">Definieren der Anforderungen Ihrer Organisation an den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a459c-112">Defining your organization's requirements for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-defining-your-requirements-for-persistent-chat-server.md)

  - [<span data-ttu-id="a459c-113">Komponenten und Topologien für den Server für beständigen Chat in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a459c-113">Components and topologies for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-components-and-topologies-for-persistent-chat-server.md)

  - [<span data-ttu-id="a459c-114">Technische Anforderungen für den Server für beständigen Chat in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a459c-114">Technical requirements for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-persistent-chat-server.md)

  - [<span data-ttu-id="a459c-115">Einrichten der Systeme und Infrastruktur für den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a459c-115">Setting up systems and infrastructure for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-setting-up-systems-and-infrastructure-for-persistent-chat-server.md)

  - [<span data-ttu-id="a459c-116">Prüfliste zur Bereitstellung für den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a459c-116">Deployment checklist for Persistent Chat Server in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-persistent-chat-server.md)

<span data-ttu-id="a459c-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a459c-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

