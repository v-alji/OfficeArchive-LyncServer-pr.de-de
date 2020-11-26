---
title: 'Lync Server 2013: Zuweisen von Richtlinien für einzelne Benutzer'
description: 'Lync Server 2013: Zuweisen von Richtlinien für einzelne Benutzer.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Assigning per-user policies
ms:assetid: a4ed0120-d9e5-4eb2-acfd-8de2cb503652
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182561(v=OCS.15)
ms:contentKeyID: 48184971
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6a99156f9413926251c27dfee40677976b80b7ea
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438295"
---
# <a name="assigning-per-user-policies-in-lync-server-2013"></a><span data-ttu-id="de55b-103">Zuweisen von Richtlinien für einzelne Benutzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de55b-103">Assigning per-user policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="de55b-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="de55b-104">

<span> </span></span></span>

<span data-ttu-id="de55b-105">_**Letztes Änderungsdatum des Themas:** 2012-10-14_</span><span class="sxs-lookup"><span data-stu-id="de55b-105">_**Topic Last Modified:** 2012-10-14_</span></span>

<span data-ttu-id="de55b-106">Sie können einem Benutzer oder einer Gruppe von Benutzern bestimmte Richtlinien zuweisen, um bestimmte Einstellungen anzugeben, die von den Einstellungen abweichen, die in Richtlinien definiert sind, die anderen Benutzern zugewiesen sind, beispielsweise globale Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="de55b-106">You can assign certain policies to a user or a group of users in order to specify particular settings that deviate from the settings defined in policies assigned to other users, such as global policies.</span></span> <span data-ttu-id="de55b-107">Diese Richtlinien werden als Richtlinien für einzelne Benutzer bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="de55b-107">These policies are called per-user policies.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="de55b-108">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="de55b-108">In This Section</span></span>

  - [<span data-ttu-id="de55b-109">Zuweisen einer pro-Benutzer-konferenzrichtlinie in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de55b-109">Assign a per-user conferencing policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-conferencing-policy.md)

  - [<span data-ttu-id="de55b-110">Zuweisen einer clientversionsrichtlinie pro Benutzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de55b-110">Assign a per-user client version policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-client-version-policy.md)

  - [<span data-ttu-id="de55b-111">Zuweisen einer pro-Benutzer-PIN-Richtlinie in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de55b-111">Assign a per-user PIN policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-pin-policy.md)

  - [<span data-ttu-id="de55b-112">Zuweisen einer Richtlinie für den Zugriff durch externe Benutzer zu einem für Lync aktivierten Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de55b-112">Assign an external user access policy to a Lync enabled user in Lync Server 2013</span></span>](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md)

  - [<span data-ttu-id="de55b-113">Zuweisen einer pro-Benutzer-Archivierungsrichtlinie in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de55b-113">Assign a per-user archiving policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-archiving-policy.md)

  - [<span data-ttu-id="de55b-114">Zuweisen einer Standortrichtlinie für einzelne Benutzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de55b-114">Assign a per-user location policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-location-policy.md)

  - [<span data-ttu-id="de55b-115">Zuweisen einer Mobilitätsrichtlinie für einzelne Benutzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de55b-115">Assign a per-user mobility policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-mobility-policy.md)

  - [<span data-ttu-id="de55b-116">Zuweisen einer beständigen Chat Richtlinie für einzelne Benutzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de55b-116">Assign a per-user Persistent Chat policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-persistent-chat-policy.md)

  - [<span data-ttu-id="de55b-117">Zuweisen einer benutzerseitigen Wähl Plan Richtlinie in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de55b-117">Assign a per-user dial plan policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-dial-plan-policy.md)

  - [<span data-ttu-id="de55b-118">Zuweisen einer VoIP-Richtlinie für einzelne Benutzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de55b-118">Assign a per-user voice policy in Lync Server 2013</span></span>](lync-server-2013-assign-a-per-user-voice-policy.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="de55b-119">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de55b-119">See Also</span></span>


[<span data-ttu-id="de55b-120">Verwalten von Benutzern in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de55b-120">Managing users in Lync Server 2013</span></span>](lync-server-2013-managing-users-in-lync-server.md)  
  

<span data-ttu-id="de55b-121"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="de55b-121"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

