---
title: 'Lync Server 2013: Vorbereiten gesperrter Active Directory-Domänendienste'
description: 'Lync Server 2013: Vorbereiten einer gesperrten Active Directory-Domänendienste'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Preparing a locked-down Active Directory Domain Services
ms:assetid: 68bde963-3fa3-4102-88d6-ac931c1dd2d7
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398492(v=OCS.15)
ms:contentKeyID: 48184377
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4aea04b138de2630935713eda7cbef9e4d21572a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49424226"
---
# <a name="preparing-a-locked-down-active-directory-domain-services-in-lync-server-2013"></a><span data-ttu-id="739a1-103">Vorbereiten gesperrter Active Directory-Domänendienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="739a1-103">Preparing a locked-down Active Directory Domain Services in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="739a1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="739a1-104">

<span> </span></span></span>

<span data-ttu-id="739a1-105">_**Letztes Änderungsdatum des Themas:** 2012-05-14_</span><span class="sxs-lookup"><span data-stu-id="739a1-105">_**Topic Last Modified:** 2012-05-14_</span></span>

<span data-ttu-id="739a1-106">Organisationen Sperren häufig Active Directory-Domänendienste, um Sicherheitsrisiken zu minimieren.</span><span class="sxs-lookup"><span data-stu-id="739a1-106">Organizations often lock down Active Directory Domain Services to help mitigate security risks.</span></span> <span data-ttu-id="739a1-107">Eine gesperrte Active Directory-Umgebung kann jedoch die von lync Server 2013 erforderlichen Berechtigungen einschränken.</span><span class="sxs-lookup"><span data-stu-id="739a1-107">However, a locked-down Active Directory environment can limit the permissions that Lync Server 2013 requires.</span></span> <span data-ttu-id="739a1-108">Das ordnungsgemäße Vorbereiten einer gesperrten Active Directory-Umgebung für lync Server 2013 umfasst einige zusätzliche Überlegungen und Schritte.</span><span class="sxs-lookup"><span data-stu-id="739a1-108">Properly preparing a locked-down Active Directory environment for Lync Server 2013 involves some additional considerations and steps.</span></span>

<span data-ttu-id="739a1-109">Es gibt zwei gängige Methoden, mit denen Berechtigungen in einer gesperrten Active Directory-Umgebung eingeschränkt sind:</span><span class="sxs-lookup"><span data-stu-id="739a1-109">Two common ways in which permissions are limited in a locked-down Active Directory environment are as follows:</span></span>

  - <span data-ttu-id="739a1-110">Zugriffssteuerungseinträge (ACEs) für authentifizierte Benutzer werden aus Containern entfernt.</span><span class="sxs-lookup"><span data-stu-id="739a1-110">Authenticated user access control entries (ACEs) are removed from containers.</span></span>

  - <span data-ttu-id="739a1-111">Die Vererbung von Berechtigungen ist für Container von Benutzer-, Kontakt-, InetOrgPerson-oder Computer Objekten deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="739a1-111">Permissions inheritance is disabled on containers of User, Contact, InetOrgPerson, or Computer objects.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="739a1-112">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="739a1-112">In This Section</span></span>

  - [<span data-ttu-id="739a1-113">Entfernte Berechtigungen für authentifizierte Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="739a1-113">Authenticated user permissions are removed in Lync Server 2013</span></span>](lync-server-2013-authenticated-user-permissions-are-removed.md)

  - [<span data-ttu-id="739a1-114">Vererbung von Berechtigungen ist für Computer-, Benutzer- oder InetOrgPerson-Container deaktiviert in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="739a1-114">Permissions inheritance Is disabled on computers, users, or InetOrgPerson containers in Lync Server 2013</span></span>](lync-server-2013-permissions-inheritance-is-disabled-on-computers-users-or-inetorgperson-containers.md)

<span data-ttu-id="739a1-115"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="739a1-115"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

