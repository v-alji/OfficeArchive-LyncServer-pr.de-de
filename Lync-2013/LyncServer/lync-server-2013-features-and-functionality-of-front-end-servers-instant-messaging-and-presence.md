---
title: 'Lync Server 2013: Features und Funktionen für Front-End-Server, Chat und Anwesenheit'
description: 'Lync Server 2013: Features und Funktionen von Front-End-Servern, Instant Messaging und Anwesenheitsinformationen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Features and functionality of Front End Servers, instant messaging, and presence
ms:assetid: 05b29536-dcd7-49b5-934a-2ebf20ddc45c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398109(v=OCS.15)
ms:contentKeyID: 48183294
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b5c8bc3db255228da3366eb5aa142cd5adc233d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393978"
---
# <a name="features-and-functionality-of-front-end-servers-instant-messaging-and-presence-in-lync-server-2013"></a><span data-ttu-id="70858-103">Features und Funktionen für Front-End-Server, Chat und Anwesenheit in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="70858-103">Features and functionality of Front End Servers, instant messaging, and presence in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="70858-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="70858-104">

<span> </span></span></span>

<span data-ttu-id="70858-105">_**Letztes Änderungsdatum des Themas:** 2013-03-17_</span><span class="sxs-lookup"><span data-stu-id="70858-105">_**Topic Last Modified:** 2013-03-17_</span></span>

<span data-ttu-id="70858-106">Front-End-Server bieten die meisten lync Server-Funktionen.</span><span class="sxs-lookup"><span data-stu-id="70858-106">Front End Servers provide most Lync Server functionality.</span></span> <span data-ttu-id="70858-107">Es stehen zwei Versionen zur Verfügung: lync Server Enterprise Edition, die in erster Linie für größere Organisationen konzipiert ist, und lync Server Standard Edition, die in erster Linie für kleinere Organisationen konzipiert ist, die eine kleinere Hardware-Investition benötigen und keine höhere Verfügbarkeit erfordern.</span><span class="sxs-lookup"><span data-stu-id="70858-107">There are two editions available: Lync Server Enterprise Edition, which is designed primarily for larger organizations, and Lync Server Standard Edition, which is designed primarily for smaller organizations which want a smaller hardware investement and do not require high availability.</span></span> <span data-ttu-id="70858-108">Beide Editionen unterstützen alle lync Server-Arbeitsauslastungen, einschließlich Chat, Anwesenheit, Konferenz und Enterprise-VoIP.</span><span class="sxs-lookup"><span data-stu-id="70858-108">Both editions support all Lync Server workloads including IM, presence, conferencing, and Enterprise Voice.</span></span>

<span data-ttu-id="70858-109">Mit der Chatfunktion können Benutzer auf ihren Computern in Echtzeit über textbasierte Nachrichten miteinander kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="70858-109">Instant messaging (IM) enables your users to communicate with each other in real time on their computers using text-based messages.</span></span> <span data-ttu-id="70858-110">Es werden sowohl Chatsitzungen mit zwei Teilnehmern als auch Sitzungen mit mehreren Teilnehmern unterstützt.</span><span class="sxs-lookup"><span data-stu-id="70858-110">Both two-party and multiparty IM sessions are supported.</span></span> <span data-ttu-id="70858-111">Ein Teilnehmer an einer Chatsitzung mit zwei Teilnehmern kann der Unterhaltung jederzeit einen dritten Teilnehmer hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="70858-111">A participant in a two-party IM conversation can add a third participant to the conversation at any time.</span></span> <span data-ttu-id="70858-112">Wenn dies geschieht, ändert sich das Unterhaltungsfenster, um Konferenzfunktionen zu unterstützen.</span><span class="sxs-lookup"><span data-stu-id="70858-112">When this happens, the Conversation window changes to support conferencing features.</span></span>

<div>


> [!IMPORTANT]
> <span data-ttu-id="70858-113">Lync-und Communicator-Clients werden, wenn Sie an einer 1:1-Kommunikation beteiligt sind, häufig als Peer-to-Peer bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="70858-113">Lync and Communicator clients when involved in a one to one communication, is often referred to as peer-to-peer.</span></span> <span data-ttu-id="70858-114">Technisch gesehen kommunizieren die beiden Clients in einer 1:1-Konversation mit der Instant Messaging-Multipoint-Steuereinheit (IMMCU) in der Mitte.</span><span class="sxs-lookup"><span data-stu-id="70858-114">Technically, the two clients are communicating in a one to one conversation, with the Instant Messaging multipoint control unit (IMMCU) in the middle.</span></span> <span data-ttu-id="70858-115">Die IMMCU ist eine Komponente des Front-End-Servers.</span><span class="sxs-lookup"><span data-stu-id="70858-115">The IMMCU is a component of Front End Server.</span></span> <span data-ttu-id="70858-116">Wenn Sie den IMMCU in den erforderlichen Kommunikations Workflow einfügen, können Sie die Anrufdetailaufzeichnung und andere Features, die der Front-End-Server ermöglicht, aufzeichnen.</span><span class="sxs-lookup"><span data-stu-id="70858-116">Placing the IMMCU in the required communication workflow allows call detail recording and other features that the Front End Server enables.</span></span> <span data-ttu-id="70858-117">Die Kommunikation erfolgt von einem dynamischen Quell Port auf dem Client zum Front-End-Serverport TLS/TCP/5061 (unter der Voraussetzung, dass die empfohlene Transportschichtsicherheit verwendet wird).</span><span class="sxs-lookup"><span data-stu-id="70858-117">Communication is from a dynamic source port on the client to the Front End Server port TLS/TCP/5061 (assuming the use of the recommended transport layer security).</span></span> <span data-ttu-id="70858-118">Die Peer-to-Peer-Kommunikation (ebenso wie die Chat Unterhaltung mit mehreren Teilnehmern) ist im Entwurf nur möglich, wenn lync Server und IMMCU aktiv und verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="70858-118">By design, peer-to-peer communication (as well as multi-party IM) is possible only when Lync Server and the IMMCU is active and available.</span></span>



</div>

<span data-ttu-id="70858-119">*Anwesenheits* Informationen bieten Benutzern Informationen über den Status anderer Personen im Netzwerk.</span><span class="sxs-lookup"><span data-stu-id="70858-119">*Presence* provides information to users about the status of other on the network.</span></span> <span data-ttu-id="70858-120">Der Anwesenheitsstatus eines Benutzers bietet Informationen, um anderen zu helfen, zu entscheiden, ob er versuchen soll, den Benutzer zu kontaktieren, und ob er Sofortnachrichten, Telefone oder e-Mails verwenden soll.</span><span class="sxs-lookup"><span data-stu-id="70858-120">A user’s presence status provides information to help others decide whether they should try to contact the user and whether to use instant messaging, phone, or email.</span></span> <span data-ttu-id="70858-121">Anwesenheitsinformationen unterstützt die sofortige Kommunikation, wenn möglich, bietet aber auch Informationen darüber, ob sich ein Benutzer in einer Besprechung oder außerhalb des Büros befindet, was darauf hinweist, dass eine sofortige Kommunikation nicht möglich ist.</span><span class="sxs-lookup"><span data-stu-id="70858-121">Presence encourages instant communication when possible, but it also provides information about whether a user is in a meeting or out of the office, indicating that instant communication is not possible.</span></span> <span data-ttu-id="70858-122">Dieser Anwesenheitsstatus wird in lync und anderen Anwendungen mit Anwesenheitsanzeige als Anwesenheitssymbol angezeigt, einschließlich des Microsoft Outlook-Messaging-und Zusammenarbeits Clients, Microsoft SharePoint Technologies, Microsoft Word und Microsoft Excel-Tabellenkalkulationssoftware.</span><span class="sxs-lookup"><span data-stu-id="70858-122">This presence status is displayed as a presence icon in Lync and other presence-aware applications, including the Microsoft Outlook messaging and collaboration client, Microsoft SharePoint technologies, Microsoft Word, and Microsoft Excel spreadsheet software.</span></span> <span data-ttu-id="70858-123">Das Anwesenheitssymbol steht für die aktuelle Verfügbarkeit und Kommunikationsbereitschaft des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="70858-123">The presence icon represents the user’s current availability and willingness to communicate.</span></span>

<span data-ttu-id="70858-124"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="70858-124"></div>

<span> </span>

</div>

</div>

</span></span></div>

