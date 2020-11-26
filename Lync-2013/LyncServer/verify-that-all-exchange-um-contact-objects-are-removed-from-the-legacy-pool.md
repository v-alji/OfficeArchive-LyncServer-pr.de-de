---
title: Überprüfen, ob alle Exchange um-Kontaktobjekte aus dem Legacy Pool entfernt wurden
description: Überprüfen Sie, ob alle Exchange um-Kontaktobjekte aus dem Legacy Pool entfernt wurden.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify that all Exchange UM Contact objects are removed from the legacy pool
ms:assetid: 5a813169-0ed7-4f84-a242-ed2cd4ea5c43
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688068(v=OCS.15)
ms:contentKeyID: 49733664
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8af5dea6cf746c55d8fecf074e132f721c380de1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440136"
---
# <a name="verify-that-all-exchange-um-contact-objects-are-removed-from-the-legacy-pool"></a><span data-ttu-id="c6b1a-103">Überprüfen, ob alle Exchange um-Kontaktobjekte aus dem Legacy Pool entfernt wurden</span><span class="sxs-lookup"><span data-stu-id="c6b1a-103">Verify that all Exchange UM Contact objects are removed from the legacy pool</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c6b1a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c6b1a-104">

<span> </span></span></span>

<span data-ttu-id="c6b1a-105">_**Letztes Änderungsdatum des Themas:** 2012-09-26_</span><span class="sxs-lookup"><span data-stu-id="c6b1a-105">_**Topic Last Modified:** 2012-09-26_</span></span>

<span data-ttu-id="c6b1a-106">Verwenden Sie entweder das **OCSUmUtil** -Tool oder das Cmdlet " **Get-CsExumContact** ", um zu überprüfen, ob Exchange um-Kontaktobjekte aus dem Legacy Office Communications Server 2007 R2-Pool entfernt wurden.</span><span class="sxs-lookup"><span data-stu-id="c6b1a-106">Use either the **OCSUmUtil** tool or the **Get-CsExumContact** cmdlet to verify that Exchange UM contact objects have been removed from the legacy Office Communications Server 2007 R2 pool.</span></span> <span data-ttu-id="c6b1a-107">**OCSUmUtil** befindet sich im folgenden Ordner:</span><span class="sxs-lookup"><span data-stu-id="c6b1a-107">**OCSUmUtil** is located in the following folder:</span></span>

<span data-ttu-id="c6b1a-108">% Program Files% \\ Common Files \\ lync Server 2013 \\ Support \\OcsUMUtil.exe</span><span class="sxs-lookup"><span data-stu-id="c6b1a-108">%Program Files%\\Common Files\\Lync Server 2013\\Support\\OcsUMUtil.exe</span></span>

<span data-ttu-id="c6b1a-109">**OCSUmUtil** muss von einem Benutzerkonto ausgeführt werden, das Folgendes hat:</span><span class="sxs-lookup"><span data-stu-id="c6b1a-109">**OCSUmUtil** must be run from a user account that has:</span></span>

  - <span data-ttu-id="c6b1a-110">Mitgliedschaft in der Gruppe "RTCUniversalServerAdmins" und "RTCUniversalUserAdmins" (die Rechte zum Lesen von Exchange Server Unified Messaging-Einstellungen umfasst)</span><span class="sxs-lookup"><span data-stu-id="c6b1a-110">Membership in the RTCUniversalServerAdmins and RTCUniversalUserAdmins group (which includes rights to read Exchange Server Unified Messaging settings)</span></span>

  - <span data-ttu-id="c6b1a-111">Domänenrechte zum Erstellen von Kontaktobjekten im angegebenen Organisationseinheitscontainer (OU)</span><span class="sxs-lookup"><span data-stu-id="c6b1a-111">Domain rights to create contact objects in the specified organizational unit (OU) container</span></span>

<span data-ttu-id="c6b1a-112">Ausführliche Informationen zur Verwendung des Cmdlets **Get-CsExumContact** finden Sie unter [Get-CsExumContact](https://docs.microsoft.com/powershell/module/skype/Get-CsExUmContact) in der Dokumentation zur lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="c6b1a-112">For details about using the **Get-CsExumContact** cmdlet, see [Get-CsExUmContact](https://docs.microsoft.com/powershell/module/skype/Get-CsExUmContact) in the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="c6b1a-113"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c6b1a-113"></div>

<span> </span>

</div>

</div>

</span></span></div>

