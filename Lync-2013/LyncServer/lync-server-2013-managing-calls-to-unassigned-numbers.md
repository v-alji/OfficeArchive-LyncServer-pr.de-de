---
title: 'Lync Server 2013: Verwalten von Anrufen an nicht zugewiesene Nummern'
description: 'Lync Server 2013: Verwalten von Anrufen an nicht zugewiesene Nummern.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing calls to unassigned numbers
ms:assetid: a45a7546-5ee6-4c1e-ab13-20a71a058f80
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688167(v=OCS.15)
ms:contentKeyID: 49733772
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a91c1ec30ea1e942fa3ea27fbcd369572884a52a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394607"
---
# <a name="managing-calls-to-unassigned-numbers-in-lync-server-2013"></a><span data-ttu-id="eaba3-103">Verwalten von Anrufen an nicht zugewiesene Nummern in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eaba3-103">Managing calls to unassigned numbers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eaba3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eaba3-104">

<span> </span></span></span>

<span data-ttu-id="eaba3-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="eaba3-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="eaba3-106">Mit lync Server können Sie die Behandlung von eingehenden Telefon anrufen konfigurieren, wenn die gewählte Nummer für Ihre Organisation gültig ist, aber keinem Benutzer oder Telefon zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="eaba3-106">Lync Server lets you configure the handling of incoming phone calls when the dialed number is valid for your organization, but is not assigned to a user or phone.</span></span> <span data-ttu-id="eaba3-107">Sie können die Ankündigungs Anwendung verwenden, um diese Anrufe an ein festgelegtes Ziel (Telefonnummer, SIP-URI oder Voicemail) zu übertragen oder eine Audio-Ansage oder beides wiederzugeben.</span><span class="sxs-lookup"><span data-stu-id="eaba3-107">You can use the Announcement application to transfer these calls to a predetermined destination (phone number, SIP URI, or voice mail), or play an audio announcement, or both.</span></span> <span data-ttu-id="eaba3-108">Sie können diese Anrufe auch an die Telefonnummer einer automatischen Exchange UM-Telefonzentrale übertragen.</span><span class="sxs-lookup"><span data-stu-id="eaba3-108">You can also transfer these calls to an Exchange UM Auto Attendant phone number.</span></span> <span data-ttu-id="eaba3-109">Die Behandlung von Anrufen an nicht zugewiesene Nummern auf eine der folgenden Arten hilft Ihnen, die Situationen zu vermeiden, in denen sich ein Anrufer verwählt und dann einen besetzt Ton hört oder der SIP-Client eine Fehlermeldung erhält.</span><span class="sxs-lookup"><span data-stu-id="eaba3-109">Handling calls to unassigned numbers in one of these ways helps you avoid the situations in which a caller misdials and then hears a busy tone, or the SIP client receives an error message.</span></span>

<span data-ttu-id="eaba3-110">In diesem Abschnitt wird beschrieben, wie nicht zugewiesene Nummernbereiche verwaltet werden, um Anrufe an nicht zugewiesene Telefonnummern zu verarbeiten.</span><span class="sxs-lookup"><span data-stu-id="eaba3-110">This section describes how to manage unassigned number ranges to handle calls to unassigned phone numbers.</span></span> <span data-ttu-id="eaba3-111">Im Abschnitt wird auch beschrieben, wie Sie Ankündigungen während einer Disaster Recovery verwalten, wenn Sie diese Funktion während eines Ausfalls nutzen möchten.</span><span class="sxs-lookup"><span data-stu-id="eaba3-111">The section also describes how to manage Announcements during disaster recovery if you want this functionality during an outage.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="eaba3-112">Die Verwendung einer nicht zugewiesenen Nummern Behandlung während eines Ausfalls ist optional.</span><span class="sxs-lookup"><span data-stu-id="eaba3-112">Using unassigned number handling during an outage is optional.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="eaba3-113">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="eaba3-113">In This Section</span></span>

  - [<span data-ttu-id="eaba3-114">Erstellen einer Ankündigung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eaba3-114">Create an announcement in Lync Server 2013</span></span>](lync-server-2013-create-an-announcement.md)

  - [<span data-ttu-id="eaba3-115">Konfigurieren von nicht zugewiesenen Telefonnummern in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eaba3-115">Configure unassigned phone numbers in Lync Server 2013</span></span>](lync-server-2013-configure-unassigned-phone-numbers.md)

  - [<span data-ttu-id="eaba3-116">Verwalten von Ansagen während der Notfallwiederherstellung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eaba3-116">Manage announcements during disaster recovery in Lync Server 2013</span></span>](lync-server-2013-manage-announcements-during-disaster-recovery.md)

<span data-ttu-id="eaba3-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eaba3-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

