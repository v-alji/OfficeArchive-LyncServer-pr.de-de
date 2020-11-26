---
title: Überprüfen des Partnerverbunds und des Remotezugriffs für externe Benutzer
description: Überprüfen Sie den Verbund und den Remotezugriff für externe Benutzer.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Verify federation and remote access for external users
ms:assetid: a383fefb-c428-4462-93fd-15ba540fa867
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688163(v=OCS.15)
ms:contentKeyID: 49733768
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1ac36f2e1b6c5ddfd889810ba2a3ab4d82b7ae33
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49446472"
---
# <a name="verify-federation-and-remote-access-for-external-users"></a><span data-ttu-id="14a75-103">Überprüfen des Partnerverbunds und des Remotezugriffs für externe Benutzer</span><span class="sxs-lookup"><span data-stu-id="14a75-103">Verify federation and remote access for external users</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="14a75-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="14a75-104">

<span> </span></span></span>

<span data-ttu-id="14a75-105">_**Letztes Änderungsdatum des Themas:** 2012-09-18_</span><span class="sxs-lookup"><span data-stu-id="14a75-105">_**Topic Last Modified:** 2012-09-18_</span></span>

<span data-ttu-id="14a75-106">Nach dem Übergang der Föderations Route zum lync Server 2013-Edgeserver sollten Sie einige Funktionstests durchführen, um zu überprüfen, ob der Verbund wie erwartet funktioniert.</span><span class="sxs-lookup"><span data-stu-id="14a75-106">After transitioning the federation route to the Lync Server 2013 Edge Server, you should perform some functional tests to verify that federation performs as expected.</span></span> <span data-ttu-id="14a75-107">Tests für den Zugriff durch externe Benutzer sollten alle externen Benutzertypen enthalten, die von Ihrer Organisation unterstützt werden, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="14a75-107">Tests for external user access should include each type of external user that your organization supports, including any or all of the following.</span></span>

<div>

## <a name="test-connectivity-of-external-users-and-external-access"></a><span data-ttu-id="14a75-108">Testen der Konnektivität externer Benutzer und des externen Zugriffs</span><span class="sxs-lookup"><span data-stu-id="14a75-108">Test Connectivity of External Users and External access</span></span>

  - <span data-ttu-id="14a75-109">Benutzer aus mindestens einer Verbunddomäne, einem internen Benutzer in lync Server 2013 und einem Benutzer in lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="14a75-109">Users from at least one federated domain, an internal user on Lync Server 2013, and a user on Lync Server 2010.</span></span> <span data-ttu-id="14a75-110">Testen Sie Instant Messaging (im), Anwesenheitsinformationen, Audio/Video (A/V) und Desktopfreigabe.</span><span class="sxs-lookup"><span data-stu-id="14a75-110">Test instant messaging (IM), presence, audio/video (A/V), and desktop sharing.</span></span>

  - <span data-ttu-id="14a75-111">Benutzer jedes öffentlichen Chat Dienstanbieters, die von Ihrer Organisation unterstützt werden (und für die Bereitstellung abgeschlossen wurde), die mit einem Benutzer in lync Server 2013 und einem Benutzer in lync Server 2010 kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="14a75-111">Users of each public IM service provider that your organization supports (and for which provisioning has been completed) communicating with a user on Lync Server 2013 and a user on Lync Server 2010.</span></span>

  - <span data-ttu-id="14a75-112">Überprüfen Sie, ob anonyme Benutzer an Konferenzen teilnehmen können.</span><span class="sxs-lookup"><span data-stu-id="14a75-112">Verify that anonymous users are able to join conferences.</span></span>

  - <span data-ttu-id="14a75-113">Ein Benutzer, der auf lync Server 2010 mithilfe des Remotebenutzerzugriffs (Anmeldung bei lync Server 2010 von außerhalb des Intranets, aber ohne VPN) mit einem Benutzer in lync Server 2013 und einem Benutzer in lync Server 2010 gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="14a75-113">A user hosted on Lync Server 2010 using remote user access (logging into Lync Server 2010 from outside the intranet but without VPN) with a user on Lync Server 2013, and a user on Lync Server 2010.</span></span> <span data-ttu-id="14a75-114">Testen Sie Chat, Anwesenheit, A/V und Desktopfreigabe.</span><span class="sxs-lookup"><span data-stu-id="14a75-114">Test IM, presence, A/V, and desktop sharing.</span></span>

  - <span data-ttu-id="14a75-115">Ein Benutzer, der auf lync Server 2013 mithilfe des Remotebenutzerzugriffs (Anmeldung bei lync Server 2013 von außerhalb des Intranets, aber ohne VPN) mit einem Benutzer in lync Server 2013 und einem Benutzer in lync Server 2010 gehostet wird.</span><span class="sxs-lookup"><span data-stu-id="14a75-115">A user hosted on Lync Server 2013 using remote user access (logging into Lync Server 2013 from outside the intranet but without VPN) with a user on Lync Server 2013, and a user on Lync Server 2010.</span></span> <span data-ttu-id="14a75-116">Testen Sie Chat, Anwesenheit, A/V und Desktopfreigabe.</span><span class="sxs-lookup"><span data-stu-id="14a75-116">Test IM, presence, A/V, and desktop sharing.</span></span>

<span data-ttu-id="14a75-117"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="14a75-117"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

