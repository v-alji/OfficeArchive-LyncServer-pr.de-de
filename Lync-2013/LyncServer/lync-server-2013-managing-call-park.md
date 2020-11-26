---
title: 'Lync Server 2013: Verwalten des Anruf Parks'
description: 'Lync Server 2013: Verwalten des Anruf Parks'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Managing Call Park
ms:assetid: 9554cdf6-8e7c-48c8-94dd-f28e2befefdc
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688140(v=OCS.15)
ms:contentKeyID: 49733740
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6540cc6d4df06b3eaadd78dce8fe01990928045a
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425969"
---
# <a name="managing-call-park-in-lync-server-2013"></a><span data-ttu-id="656a1-103">Verwalten des Anruf Parks in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="656a1-103">Managing Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="656a1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="656a1-104">

<span> </span></span></span>

<span data-ttu-id="656a1-105">_**Letztes Änderungsdatum des Themas:** 2012-09-10_</span><span class="sxs-lookup"><span data-stu-id="656a1-105">_**Topic Last Modified:** 2012-09-10_</span></span>

<span data-ttu-id="656a1-106">Mit der Anwendung "Anruf parken" kann ein Enterprise-VoIP-Benutzer einen Anruf von einem Telefon aus halten und den Anruf später von einem beliebigen Telefon aus abrufen.</span><span class="sxs-lookup"><span data-stu-id="656a1-106">The Call Park application enables an Enterprise Voice user to put a call on hold from one telephone and then retrieve the call later from any telephone.</span></span> <span data-ttu-id="656a1-107">Wenn der Benutzer einen Anruf parkt, überträgt lync Server den Anruf an eine temporäre Nummer, die so genannte *Orbit*, in der der Anruf gehalten wird, bis er von einem anderen abgerufen wird, oder es wird ein Timeout festgestellt.</span><span class="sxs-lookup"><span data-stu-id="656a1-107">When the user parks a call, Lync Server transfers the call to a temporary number, called an *orbit*, where the call is held until someone retrieves it or it times out.</span></span>

<span data-ttu-id="656a1-108">Die Themen in diesem Abschnitt enthalten Schritt-für-Schritt-Verfahren für Aufgaben, die Sie ausführen können, um die Anwendung Parken in Ihrer Bereitstellung anzupassen und zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="656a1-108">Topics in this section provide step-by-step procedures for tasks that you can perform to customize and maintain the Call Park application in your deployment.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="656a1-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="656a1-109">In This Section</span></span>

  - [<span data-ttu-id="656a1-110">Konfigurieren von Telefonnummern Erweiterungen für Parken von Anrufen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="656a1-110">Configure phone number extensions for parking calls in Lync Server 2013</span></span>](lync-server-2013-configure-phone-number-extensions-for-parking-calls.md)

  - [<span data-ttu-id="656a1-111">Konfigurieren von Einstellungen für den Anruf Park in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="656a1-111">Configure Call Park settings in Lync Server 2013</span></span>](lync-server-2013-configure-call-park-settings.md)

  - [<span data-ttu-id="656a1-112">Anpassen der Musik zum Parken von Anrufen im Wartebereich in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="656a1-112">Customize Call Park music on hold in Lync Server 2013</span></span>](lync-server-2013-customize-call-park-music-on-hold.md)

  - [<span data-ttu-id="656a1-113">Verwalten des Parkens von Anrufen während der Notfallwiederherstellung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="656a1-113">Manage Call Park during disaster recovery in Lync Server 2013</span></span>](lync-server-2013-manage-call-park-during-disaster-recovery.md)

<span data-ttu-id="656a1-114"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="656a1-114"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

