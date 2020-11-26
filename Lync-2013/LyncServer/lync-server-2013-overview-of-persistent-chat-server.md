---
title: 'Lync Server 2013: Übersicht über den Server für beständigen Chat'
description: 'Lync Server 2013: Übersicht über den Server für beständigen Chat.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Overview of Persistent Chat Server
ms:assetid: 23f7c886-304d-495a-ae70-3cbb44241acd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425717(v=OCS.15)
ms:contentKeyID: 48183622
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: bbcb396522611aca52bd2093f2fd49f376341356
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424758"
---
# <a name="overview-of-persistent-chat-server-in-lync-server-2013"></a><span data-ttu-id="8b0bd-103">Übersicht über den Server für beständigen Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8b0bd-103">Overview of Persistent Chat Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8b0bd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8b0bd-104">

<span> </span></span></span>

<span data-ttu-id="8b0bd-105">_**Letztes Änderungsdatum des Themas:** 2012-10-29_</span><span class="sxs-lookup"><span data-stu-id="8b0bd-105">_**Topic Last Modified:** 2012-10-29_</span></span>

<span data-ttu-id="8b0bd-106">Lync Server 2013, beständiger Chat Server ermöglicht Benutzern die Teilnahme an mehrteiligen, themenbasierten Konversationen, die im Laufe der Zeit fortbestehen.</span><span class="sxs-lookup"><span data-stu-id="8b0bd-106">Lync Server 2013, Persistent Chat Server enables users to participate in multiparty, topic-based conversations that persist over time.</span></span> <span data-ttu-id="8b0bd-107">Der beständige Chat Server kann Ihrer Organisation helfen, Folgendes zu tun:</span><span class="sxs-lookup"><span data-stu-id="8b0bd-107">Persistent Chat Server can help your organization do the following:</span></span>

  - <span data-ttu-id="8b0bd-108">Verbessern der Kommunikation zwischen geografisch verteilten und funktionsübergreifenden Teams</span><span class="sxs-lookup"><span data-stu-id="8b0bd-108">Improve communication between geographically dispersed and cross-functional teams.</span></span> <span data-ttu-id="8b0bd-109">Mithilfe des beständigen Chats können Teams Informationen, Ideen und Entscheidungen effizient miteinander austauschen.</span><span class="sxs-lookup"><span data-stu-id="8b0bd-109">By using Persistent Chat, teams can efficiently share information, ideas, and decisions with one another.</span></span> <span data-ttu-id="8b0bd-110">Die Nachrichten, die in Chatrooms (Diskussionsforen) gepostet wurden, können beibehalten werden (das heißt, Sie können im Laufe der Zeit verfügbar sein), damit Personen an verschiedenen Standorten und Abteilungen teilnehmen können, selbst wenn Sie nicht gleichzeitig online sind.</span><span class="sxs-lookup"><span data-stu-id="8b0bd-110">The messages posted to chat rooms (discussion forums) can persist (that is, can be available over time), so that people from different locations and departments can participate, even when they are not simultaneously online.</span></span> <span data-ttu-id="8b0bd-111">Wenn ein Benutzer eine Verbindung mit einem Chatroom herstellt, wird im Chatroom automatisch Backchat (eine konfigurierbare Anzahl von Chat-Verlaufs Nachrichten) geladen, damit der Benutzer einen Kontext für die Unterhaltung erhält.</span><span class="sxs-lookup"><span data-stu-id="8b0bd-111">When a user connects to a chat room, backchat (a configurable number of chat-history messages) is automatically loaded in the chat room to give the user a context for the conversation.</span></span>

  - <span data-ttu-id="8b0bd-112">Verbessern des Informations Bewusstseins</span><span class="sxs-lookup"><span data-stu-id="8b0bd-112">Improve information awareness.</span></span> <span data-ttu-id="8b0bd-113">Mithilfe von clientseitigen filtern können Benutzerbedingungen definieren, wie beispielsweise Schlüsselwörter im Nachrichteninhalt oder den Wert des Felds "von" in einer Nachricht, um eine Benachrichtigung zu erhalten, wenn diese Bedingungen in Sofortnachrichten oder Chatroom-Nachrichten im beständigen Chat erfüllt werden.</span><span class="sxs-lookup"><span data-stu-id="8b0bd-113">By using client-side filters, users can define conditions—such as keywords in message content, or the value of the "from" field in a message—to receive notification when those conditions are met in Persistent Chat instant messages or chat room messages.</span></span> <span data-ttu-id="8b0bd-114">Auf diese Weise können Benutzer mit den Inhalten, die Sie am meisten interessieren, auf dem neuesten Stand bleiben.</span><span class="sxs-lookup"><span data-stu-id="8b0bd-114">This way, users can stay up-to-date with the content that interests them most.</span></span>

  - <span data-ttu-id="8b0bd-115">Verbessern der Kommunikation mit der erweiterten Organisation</span><span class="sxs-lookup"><span data-stu-id="8b0bd-115">Improve communication with their extended organization.</span></span> <span data-ttu-id="8b0bd-116">Durch die einfache Zusammenarbeit über lang andauernde Themen mit anderen Personen in der Organisation und durch die Bereitstellungeines permanenten Informationsaustauschs hilft der beständige Chat, die Kommunikation zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="8b0bd-116">By making it easy to collaborate over long-running topics with others in the organization, and by providing a persistent place to share information, Persistent Chat helps improve communication.</span></span>

  - <span data-ttu-id="8b0bd-117">Reduzieren Sie die Informationsüberlastung.</span><span class="sxs-lookup"><span data-stu-id="8b0bd-117">Reduce information overload.</span></span> <span data-ttu-id="8b0bd-118">Benutzer können Chatrooms und Nachrichten von größtem Interesse mithilfe von clientseitigen Filtern verfolgen und Chatrooms, denen Sie folgen möchten, zu Ihrer Kontaktliste hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="8b0bd-118">Users can follow chat rooms and messages of most interest by using client-side filters, and can add chat rooms they want to follow to their contact list.</span></span>

  - <span data-ttu-id="8b0bd-119">Verbessern Sie die Verbreitung wichtiger Kenntnisse und Informationen.</span><span class="sxs-lookup"><span data-stu-id="8b0bd-119">Increase dispersion of important knowledge and information.</span></span> <span data-ttu-id="8b0bd-120">Dokumente und Links können in Unterhaltungen für den Zugriff durch das gesamte Team integriert werden.</span><span class="sxs-lookup"><span data-stu-id="8b0bd-120">Documents and links can be included within conversations for access by all the team.</span></span> <span data-ttu-id="8b0bd-121">Wenn Sie Fragen an ein umfassenderes Team senden, können die Benutzer von den Antworten von Sachverständigen profitieren.</span><span class="sxs-lookup"><span data-stu-id="8b0bd-121">By posting questions to a broader team, users can benefit from responses by subject matter experts.</span></span> <span data-ttu-id="8b0bd-122">Durch die Integration in andere Informationssysteme können wichtige organisatorische Daten problemlos an große Gruppen kommuniziert werden.</span><span class="sxs-lookup"><span data-stu-id="8b0bd-122">Integration with other information systems enables important organizational data to be easily communicated to large groups.</span></span>

<span data-ttu-id="8b0bd-123">Um Chatrooms in lync Server 2013 zu aktivieren, stellen Sie den lync Server 2013-beständigen Chat bereit.</span><span class="sxs-lookup"><span data-stu-id="8b0bd-123">To enable chat rooms in Lync Server 2013, deploy Lync Server 2013 Persistent Chat.</span></span> <span data-ttu-id="8b0bd-124">Informationen zum Aktivieren von Chatrooms finden Sie in der Hilfe zum beständigen Chat unter <https://go.microsoft.com/fwlink/p/?linkid=270945> .</span><span class="sxs-lookup"><span data-stu-id="8b0bd-124">For information about enabling chat rooms, see the Persistent Chat Help at <https://go.microsoft.com/fwlink/p/?linkid=270945>.</span></span> <span data-ttu-id="8b0bd-125">Wenn Benutzer für lync Server aktiviert sind und die lync Server-Unterstützung bereitgestellt wird, können Benutzer lync 2013-beständigen Chat installieren und verwenden, um Chatroom-Unterstützung bereitzustellen.</span><span class="sxs-lookup"><span data-stu-id="8b0bd-125">If users are enabled for Lync Server, and Lync Server support is deployed, users can install and use Lync 2013 Persistent Chat to provide chat room support.</span></span>

<span data-ttu-id="8b0bd-126">Wenn Ihre Organisation Konformitätsrichtlinien beachten muss, können Sie optional den Compliance-Service für beständigen Chat bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="8b0bd-126">If your organization is required to follow compliance regulations, you can optionally deploy Persistent Chat Compliance service.</span></span>

<span data-ttu-id="8b0bd-127"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8b0bd-127"></div>

<span> </span>

</div>

</div>

</span></span></div>

