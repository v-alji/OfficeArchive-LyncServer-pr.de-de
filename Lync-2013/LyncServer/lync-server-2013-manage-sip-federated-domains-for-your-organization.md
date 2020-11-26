---
title: 'Lync Server 2013: Verwalten von SIP-Partnerdomänen für eine Organisation'
description: 'Lync Server 2013: Verwalten von SIP-Verbunddomänen für Ihre Organisation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage SIP federated domains for your organization
ms:assetid: abc48829-e5cf-4651-bc38-899192f5c3bc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ552454(v=OCS.15)
ms:contentKeyID: 48679565
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6fcb8851af7e623251e5c0b635e67e524355fd4c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426032"
---
# <a name="manage-sip-federated-domains-for-your-organization-in-lync-server-2013"></a><span data-ttu-id="a272f-103">Verwalten von SIP-Partnerdomänen für eine Organisation in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a272f-103">Manage SIP federated domains for your organization in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a272f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a272f-104">

<span> </span></span></span>

<span data-ttu-id="a272f-105">_**Letztes Änderungsdatum des Themas:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="a272f-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="a272f-106">Diese Dokumentation ist vorläufig und kann geändert werden.</span><span class="sxs-lookup"><span data-stu-id="a272f-106">This is preliminary documentation and is subject to change.</span></span> <span data-ttu-id="a272f-107">Leere Themen sind als Platzhalter enthalten.</span><span class="sxs-lookup"><span data-stu-id="a272f-107">Blank topics are included as placeholders.</span></span>

<span data-ttu-id="a272f-108">Zum Verwalten und Konfigurieren von SIP-Domänen, mit denen Sie eine Föderation führen können, können Sie die folgenden Aktionen ausführen:</span><span class="sxs-lookup"><span data-stu-id="a272f-108">To manage and configure SIP domains that you can federate with, you can do the following:</span></span>

  - <span data-ttu-id="a272f-109">Erstellen oder bearbeiten Sie eine Liste der zulässigen Domänen der SIP-Partnerdomänen.</span><span class="sxs-lookup"><span data-stu-id="a272f-109">Create or edit an allowed domain list of SIP federated partner domains.</span></span>

  - <span data-ttu-id="a272f-110">Erstellen oder Bearbeiten einer Liste blockierter Domänen mit SIP-Verbunddomänen</span><span class="sxs-lookup"><span data-stu-id="a272f-110">Create or edit a blocked domain list of SIP federated domains.</span></span>

<span data-ttu-id="a272f-111">Führen Sie die Verfahren in diesem Abschnitt aus, um diese Aufgaben auszuführen.</span><span class="sxs-lookup"><span data-stu-id="a272f-111">To perform these tasks, use the procedures in this section.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="a272f-112">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="a272f-112">In This Section</span></span>

  - [<span data-ttu-id="a272f-113">Konfigurieren der Unterstützung für zulässige externe Domänen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a272f-113">Configure support for allowed external domains in Lync Server 2013</span></span>](lync-server-2013-configure-support-for-allowed-external-domains.md)

  - [<span data-ttu-id="a272f-114">Konfigurieren der Unterstützung für blockierte externe Domänen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a272f-114">Configure support for blocked external domains in Lync Server 2013</span></span>](lync-server-2013-configure-support-for-blocked-external-domains.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="a272f-115">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a272f-115">See Also</span></span>


[<span data-ttu-id="a272f-116">Konfigurieren von Richtlinien zur Steuerung des Partnerbenutzerzugriffs in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a272f-116">Configure policies to control federated user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-federated-user-access.md)  
[<span data-ttu-id="a272f-117">Aktivieren oder Deaktivieren des Partnerverbunds und der Konnektivität mit öffentlichen Chatdiensten in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a272f-117">Enable or disable federation and public IM connectivity in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-federation-and-public-im-connectivity.md)  
[<span data-ttu-id="a272f-118">Aktivieren oder Deaktivieren der Suche von Verbundpartnern in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a272f-118">Enable or disable discovery of federation partners in Lync Server 2013</span></span>](lync-server-2013-enable-or-disable-discovery-of-federation-partners.md)  
  

<span data-ttu-id="a272f-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a272f-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

