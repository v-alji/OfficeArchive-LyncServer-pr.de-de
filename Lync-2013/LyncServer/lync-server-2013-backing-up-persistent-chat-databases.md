---
title: 'Lync Server 2013: Sichern von persistenten Chat Datenbanken'
description: 'Lync Server 2013: sichern beständiger Chat Datenbanken.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Backing up Persistent Chat databases
ms:assetid: b99ebdc0-a025-44d7-9d74-37a7365f330d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945646(v=OCS.15)
ms:contentKeyID: 51541507
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9885eaf0065f5b558922c056fb1f669a5b821460
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438022"
---
# <a name="backing-up-persistent-chat-databases-in-lync-server-2013"></a><span data-ttu-id="d3d34-103">Sichern von persistenten Chat Datenbanken in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d3d34-103">Backing up Persistent Chat databases in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d3d34-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d3d34-104">

<span> </span></span></span>

<span data-ttu-id="d3d34-105">_**Letztes Änderungsdatum des Themas:** 2013-02-17_</span><span class="sxs-lookup"><span data-stu-id="d3d34-105">_**Topic Last Modified:** 2013-02-17_</span></span>

<span data-ttu-id="d3d34-106">Beständiger Chatroom-Inhalt wird in der persistent Chat-Datenbank (MGC. mdf) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="d3d34-106">Persistent Chat room content is stored in the Persistent Chat database (Mgc.mdf).</span></span> <span data-ttu-id="d3d34-107">Es handelt sich hierbei um unternehmenswichtige Daten, die regelmäßig gesichert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="d3d34-107">This is business-critical data that should be backed up regularly.</span></span> <span data-ttu-id="d3d34-108">Zusätzlich zu den Chatroom-Inhalten speichert die persistente Chat-Datenbank auch Informationen zu den Prinzipalen (wie Benutzer und Benutzergruppen) sowie zu den Rollen und dem Zugriff, die Sie für Chatrooms und Chatrooms haben.</span><span class="sxs-lookup"><span data-stu-id="d3d34-108">In addition to the chat room content, the Persistent Chat database also stores information about the principals (such as users and user groups), and the roles and access that they have to chat rooms and chat room.</span></span>

<span data-ttu-id="d3d34-109">Es gibt zwei Möglichkeiten, persistente Chat-Daten zu sichern.</span><span class="sxs-lookup"><span data-stu-id="d3d34-109">There are two ways of backing up Persistent Chat data.</span></span>

  - <span data-ttu-id="d3d34-110">Die SQL Server-Sicherung</span><span class="sxs-lookup"><span data-stu-id="d3d34-110">SQL Server Backup</span></span>

  - <span data-ttu-id="d3d34-111">Das `Export-CsPersistentChatData` Cmdlet, das persistente Chat-Daten als Datei exportiert</span><span class="sxs-lookup"><span data-stu-id="d3d34-111">The `Export-CsPersistentChatData` cmdlet, which exports Persistent Chat data as a file</span></span>

<span data-ttu-id="d3d34-112">Daten, die mit der SQL Server-Sicherung erstellt werden, erfordern erheblich mehr Speicherplatz – möglicherweise 20 mal mehr – als die von Ihnen erstellten `Export-CsPersistentChatData` , aber die SQL Server-Sicherung ist wahrscheinlicher eine Prozedur, mit der Administratoren vertraut sind.</span><span class="sxs-lookup"><span data-stu-id="d3d34-112">Data that is created by using SQL Server backup requires significantly more disk space—possibly 20 times more—than that created by `Export-CsPersistentChatData`, but SQL Server backup is more likely to be a procedure that administrators are familiar with.</span></span>

<span data-ttu-id="d3d34-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d3d34-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

