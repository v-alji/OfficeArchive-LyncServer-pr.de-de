---
title: 'Lync Server 2013: Einrichten von Benutzerrichtlinien für die Archivierung in lync Server'
description: 'Lync Server 2013: Einrichten von Benutzerrichtlinien für die Archivierung in lync Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up user policies for Archiving in Lync Server
ms:assetid: 22d6cc76-6b5c-4a8c-bb8a-7996450ec085
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204742(v=OCS.15)
ms:contentKeyID: 48183626
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9e33abf6cf16c9c1367162aa8beee91874f4c725
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49441627"
---
# <a name="setting-up-user-policies-for-archiving-in-lync-server-2013"></a><span data-ttu-id="5f76c-103">Einrichten von Benutzerrichtlinien für die Archivierung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f76c-103">Setting up user policies for Archiving in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5f76c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5f76c-104">

<span> </span></span></span>

<span data-ttu-id="5f76c-105">_**Letztes Änderungsdatum des Themas:** 2012-10-10_</span><span class="sxs-lookup"><span data-stu-id="5f76c-105">_**Topic Last Modified:** 2012-10-10_</span></span>

<span data-ttu-id="5f76c-106">Das Aktivieren oder Deaktivieren der Archivierung für bestimmte Benutzer, die in lync Server 2013 verwaltet werden, erfordert das Erstellen und Konfigurieren einer oder mehrerer Benutzerrichtlinien und das anschließende Anwenden der entsprechenden Richtlinie auf bestimmte Benutzer oder Benutzergruppen.</span><span class="sxs-lookup"><span data-stu-id="5f76c-106">Enabling or disabling Archiving for specific users homed on Lync Server 2013 requires creating and configuring one or more user policies, and then applying the appropriate policy to specific users or user groups.</span></span> <span data-ttu-id="5f76c-107">Benutzerrichtlinien setzen Website-und globale Richtlinien außer Kraft, allerdings nur für Benutzer, die in lync Server 2013 verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="5f76c-107">User policies override site and global policies, but only for users homed on Lync Server 2013.</span></span>

<span data-ttu-id="5f76c-108">Benutzer sind immer in lync Server beheimatet.</span><span class="sxs-lookup"><span data-stu-id="5f76c-108">Users are always homed in Lync Server.</span></span> <span data-ttu-id="5f76c-109">Wenn die Microsoft Exchange-Integration aktiviert ist, müssen Benutzer, deren Postfächer in Microsoft Exchange Server 2013 enthalten sind, ihre Archivierungsrichtlinien nicht in lync Server verwalten.</span><span class="sxs-lookup"><span data-stu-id="5f76c-109">If Microsoft Exchange integration is enabled, users whose mailboxes are in Microsoft Exchange Server 2013 don’t need to have their Archiving policies in Lync Server managed.</span></span> <span data-ttu-id="5f76c-110">Diese Benutzer mit Archivierung werden von Exchange In-Place halten verwaltet.</span><span class="sxs-lookup"><span data-stu-id="5f76c-110">These users with Archiving will be managed by Exchange In-Place Hold.</span></span>

<span data-ttu-id="5f76c-111">Ausführliche Informationen zur Funktionsweise von Archivierungsrichtlinien, einschließlich der Hierarchie für Global-, Website-und Benutzerrichtlinien, finden Sie unter [Funktionsweise der Archivierung in lync Server 2013](lync-server-2013-how-archiving-works.md) in der Planungsdokumentation, Bereitstellungsdokumentation oder in der Betriebsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="5f76c-111">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) in the Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="5f76c-112">Wenn Sie die Microsoft Exchange-Integration für Ihre Bereitstellung aktiviert haben, Steuern Exchange In-Place Speicherrichtlinien, ob die Archivierung für die Benutzer aktiviert ist, die sich in Exchange 2013 befinden.</span><span class="sxs-lookup"><span data-stu-id="5f76c-112">If you enabled Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013.</span></span> <span data-ttu-id="5f76c-113">Die Archivierung für diese Benutzer setzt voraus, dass ihre Postfächer In-Place halten.</span><span class="sxs-lookup"><span data-stu-id="5f76c-113">Archiving for these users requires that they have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="5f76c-114">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Einrichten von Richtlinien für die Archivierung in lync Server 2013 bei Verwendung der Exchange Server-Integration</A> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="5f76c-114">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="5f76c-115">Sie sollten alle geeigneten Optionen in den Archivierungs Konfigurationen angeben, bevor Sie die Archivierung aktivieren.</span><span class="sxs-lookup"><span data-stu-id="5f76c-115">You should specify all appropriate options in the Archiving configurations before enabling Archiving.</span></span> <span data-ttu-id="5f76c-116">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-configuring-archiving-options.md">Konfigurieren von Archivierungsoptionen in lync Server 2013</A> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="5f76c-116">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="5f76c-117">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="5f76c-117">In This Section</span></span>

  - [<span data-ttu-id="5f76c-118">Erstellen und Konfigurieren von Benutzerrichtlinien für die Archivierung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f76c-118">Creating and configuring user policies for Archiving in Lync Server 2013</span></span>](lync-server-2013-creating-and-configuring-user-policies-for-archiving-in-lync-server.md)

  - [<span data-ttu-id="5f76c-119">Anwenden einer lync Server-Archivierungsrichtlinie auf einen Benutzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f76c-119">Applying a Lync Server Archiving policy to a user in Lync Server 2013</span></span>](lync-server-2013-applying-a-lync-server-archiving-policy-to-a-user.md)

<span data-ttu-id="5f76c-120"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5f76c-120"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

