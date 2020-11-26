---
title: 'Lync Server 2013: Wiederherstellen beständiger Chat-Daten'
description: 'Lync Server 2013: Wiederherstellen beständiger Chat-Daten'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Restoring Persistent Chat data
ms:assetid: c251a7fa-50da-434b-b39a-17f5978ce736
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945649(v=OCS.15)
ms:contentKeyID: 51541516
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7c75683e151daaadab8374ed5b41886da9a3aea3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442509"
---
# <a name="restoring-persistent-chat-data-in-lync-server-2013"></a><span data-ttu-id="58ad7-103">Wiederherstellen beständiger Chat-Daten in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="58ad7-103">Restoring Persistent Chat data in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="58ad7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="58ad7-104">

<span> </span></span></span>

<span data-ttu-id="58ad7-105">_**Letztes Änderungsdatum des Themas:** 2013-02-18_</span><span class="sxs-lookup"><span data-stu-id="58ad7-105">_**Topic Last Modified:** 2013-02-18_</span></span>

<span data-ttu-id="58ad7-106">Beständiger Chatroom-Inhalt wird in der persistent Chat-Datenbank (MGC. mdf) gespeichert.</span><span class="sxs-lookup"><span data-stu-id="58ad7-106">Persistent Chat room content is stored in the Persistent Chat database (mgc.mdf).</span></span> <span data-ttu-id="58ad7-107">Es handelt sich hierbei um unternehmenswichtige Daten, die regelmäßig gesichert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="58ad7-107">This is business-critical data that should be backed up regularly.</span></span> <span data-ttu-id="58ad7-108">Zusätzlich zu den Chatroom-Inhalten werden Prinzipale (wie Benutzer und Gruppen) und die Rollen und der Zugriff, die Sie für Chatrooms und Chatroom-Inhalte haben, auch in der persistenten Chat-Datenbank gespeichert.</span><span class="sxs-lookup"><span data-stu-id="58ad7-108">In addition to the chat room content, principals (such as users and groups) and the roles and access that they have to chat rooms and chat room content, is also stored in the Persistent Chat database.</span></span>

<span data-ttu-id="58ad7-109">Wie Sie Ihre beständigen Chat-Daten wiederherstellen, hängt von der Methode ab, die Sie zum Sichern verwendet haben.</span><span class="sxs-lookup"><span data-stu-id="58ad7-109">How you restore your Persistent Chat data depends on the method that you used to back it up.</span></span>

  - <span data-ttu-id="58ad7-110">Wenn Sie SQL Server-Sicherungsverfahren verwendet haben, müssen Sie SQL Server-Wiederherstellungsverfahren verwenden.</span><span class="sxs-lookup"><span data-stu-id="58ad7-110">If you used SQL Server backup procedures, you must use SQL Server restore procedures.</span></span>

  - <span data-ttu-id="58ad7-111">Wenn Sie das Cmdlet **Export-CsPersistentChatData** zum Sichern beständiger Chat-Daten verwendet haben, müssen Sie die Daten mithilfe des Cmdlets **Import-CsPersistentChatData** wiederherstellen.</span><span class="sxs-lookup"><span data-stu-id="58ad7-111">If you used the **Export-CsPersistentChatData** cmdlet to back up Persistent Chat data, then you must use the **Import-CsPersistentChatData** cmdlet to restore the data.</span></span>

<span data-ttu-id="58ad7-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="58ad7-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

