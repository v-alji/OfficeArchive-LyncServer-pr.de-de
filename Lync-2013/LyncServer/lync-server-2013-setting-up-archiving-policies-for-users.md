---
title: 'Lync Server 2013: Einrichten von Archivierungsrichtlinien für Benutzer'
description: 'Lync Server 2013: Einrichten von Archivierungsrichtlinien für Benutzer.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Setting up Archiving policies for users
ms:assetid: 1bbb45df-0590-4c66-9d65-d25526f57790
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204722(v=OCS.15)
ms:contentKeyID: 48183549
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9c18a15c1a0611f49a6fd9a4983f3ce87104332e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49444763"
---
# <a name="setting-up-archiving-policies-for-users-in-lync-server-2013"></a><span data-ttu-id="de853-103">Einrichten von Archivierungsrichtlinien für Benutzer in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de853-103">Setting up Archiving policies for users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="de853-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="de853-104">

<span> </span></span></span>

<span data-ttu-id="de853-105">_**Letztes Änderungsdatum des Themas:** 2012-10-09_</span><span class="sxs-lookup"><span data-stu-id="de853-105">_**Topic Last Modified:** 2012-10-09_</span></span>

<span data-ttu-id="de853-106">Sie können die Archivierung für bestimmte Benutzer aktivieren oder deaktivieren, indem Sie eine Archivierungsrichtlinie für Benutzer erstellen und konfigurieren und dann die Richtlinie auf bestimmte Benutzer oder Benutzergruppen anwenden.</span><span class="sxs-lookup"><span data-stu-id="de853-106">You can enable or disable Archiving for specific users by creating and configuring an Archiving policy for users, and then applying the policy to specific users or user groups.</span></span> <span data-ttu-id="de853-107">Benutzerrichtlinien überschreiben alle globalen Richtlinien oder Website Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="de853-107">User policies override any global policy or site policies.</span></span> <span data-ttu-id="de853-108">Archivierungsrichtlinien gelten nur, wenn Sie die Microsoft Exchange-Integration nicht verwenden, oder wenn Sie die Microsoft Exchange-Integration verwenden, aber einige Benutzer haben, die sich nicht in Exchange 2013 befinden und deren Postfächer In-Place halten.</span><span class="sxs-lookup"><span data-stu-id="de853-108">Archiving policies only apply if you do not use Microsoft Exchange integration or, if you do use Microsoft Exchange integration, but have some users who are not homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span>

<span data-ttu-id="de853-109">Ausführliche Informationen zur Funktionsweise von Archivierungsrichtlinien, einschließlich der Hierarchie für Global-, Website-und Benutzerrichtlinien, finden Sie unter [Funktionsweise der Archivierung in der lync Server 2013](lync-server-2013-how-archiving-works.md) -Planungsdokumentation, Bereitstellungsdokumentation oder Betriebsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="de853-109">For details about how Archiving policies work, including the hierarchy for global, site, and user policies, see [How Archiving works in Lync Server 2013](lync-server-2013-how-archiving-works.md) Planning documentation, Deployment documentation, or Operations documentation.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="de853-110">Wenn Sie die Microsoft Exchange-Integration für Ihre Bereitstellung aktivieren, Steuern Exchange-In-Place Speicherrichtlinien, ob die Archivierung für die Benutzer aktiviert ist, die sich in Exchange 2013 befinden, und die Postfächer In-Place halten.</span><span class="sxs-lookup"><span data-stu-id="de853-110">If you enable Microsoft Exchange integration for your deployment, Exchange In-Place Hold policies control whether archiving is enabled for the users who are homed on Exchange 2013 and have their mailboxes put on In-Place Hold.</span></span> <span data-ttu-id="de853-111">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Einrichten von Richtlinien für die Archivierung in lync Server 2013 bei Verwendung der Exchange Server-Integration</A> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="de853-111">For details, see <A href="lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</A> in the Deployment documentation.</span></span><BR><span data-ttu-id="de853-112">Konfigurieren Sie in der Archivierungskonfiguration erst alle erforderlichen Optionen, bevor Sie in den Archivierungsrichtlinien die Archivierung der internen oder externen Kommunikation aktivieren.</span><span class="sxs-lookup"><span data-stu-id="de853-112">You should specify all appropriate options in the Archiving configurations before enabling Archiving of internal or external communications in the Archiving policies.</span></span> <span data-ttu-id="de853-113">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-configuring-archiving-options.md">Konfigurieren von Archivierungsoptionen in lync Server 2013</A> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="de853-113">For details, see <A href="lync-server-2013-configuring-archiving-options.md">Configuring Archiving options in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="de853-114">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="de853-114">In This Section</span></span>

  - [<span data-ttu-id="de853-115">Einrichten von Benutzerrichtlinien für die Archivierung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="de853-115">Setting up user policies for Archiving in Lync Server 2013</span></span>](lync-server-2013-setting-up-user-policies-for-archiving-in-lync-server.md)

  - [<span data-ttu-id="de853-116">Einrichten von Richtlinien für die Archivierung in lync Server 2013 bei Verwendung der Exchange Server-Integration</span><span class="sxs-lookup"><span data-stu-id="de853-116">Setting up policies for Archiving in Lync Server 2013 when using Exchange Server integration</span></span>](lync-server-2013-setting-up-policies-for-archiving-when-using-exchange-server-integration.md)

<span data-ttu-id="de853-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="de853-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

