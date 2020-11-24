---
title: 'Lync Server 2013: Komponenten für das Parken von Anrufen'
description: 'Lync Server 2013: von Call Park verwendete Komponenten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Components used by Call Park
ms:assetid: c7ffbee3-0ce1-48c0-bb56-af098b41d6d6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398824(v=OCS.15)
ms:contentKeyID: 48185374
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 285af316fa2d49e8bebf68e11de6d9526e12ae29
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394211"
---
# <a name="components-used-by-call-park-in-lync-server-2013"></a><span data-ttu-id="074c5-103">Komponenten für das Parken von Anrufen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="074c5-103">Components used by Call Park in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="074c5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="074c5-104">

<span> </span></span></span>

<span data-ttu-id="074c5-105">_**Letztes Änderungsdatum des Themas:** 2012-09-13_</span><span class="sxs-lookup"><span data-stu-id="074c5-105">_**Topic Last Modified:** 2012-09-13_</span></span>

<span data-ttu-id="074c5-106">Die Anwendung Parken wird automatisch installiert, wenn Sie Enterprise-VoIP bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="074c5-106">The Call Park application is automatically installed when you deploy Enterprise Voice.</span></span> <span data-ttu-id="074c5-107">Sie aktivieren den Anruf Park durch Konfigurieren der VoIP-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="074c5-107">You enable Call Park by configuring voice policy.</span></span> <span data-ttu-id="074c5-108">Die folgenden lync Server 2013-Komponenten unterstützen die Anwendung für den Parken von anrufen:</span><span class="sxs-lookup"><span data-stu-id="074c5-108">The following Lync Server 2013 components support the Call Park application:</span></span>

  - <span data-ttu-id="074c5-109">**Anwendungsdienst**   Der Anwendungsdienst stellt eine Plattform zum Bereitstellen, hosten und Verwalten von Unified Communications-Anwendungen bereit, beispielsweise die Anwendung für den Parken von anrufen.</span><span class="sxs-lookup"><span data-stu-id="074c5-109">**Application service**   Application service provides a platform for deploying, hosting, and managing unified communications applications, such as the Call Park application.</span></span> <span data-ttu-id="074c5-110">Der Anwendungsdienst wird auf jedem Front-End-Server in einem Front-End-Pool und auf jedem Standard Edition-Server automatisch installiert.</span><span class="sxs-lookup"><span data-stu-id="074c5-110">Application service is automatically installed on every Front End Server in a Front End pool and on every Standard Edition server.</span></span>

  - <span data-ttu-id="074c5-111">**Anruf parken-Anwendung**   Die Anwendung "Parken" ist eine der Unified Communications-Anwendungen, die vom Anwendungsdienst gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="074c5-111">**Call Park application**   The Call Park application is one of the unified communications applications that are hosted by Application service.</span></span> <span data-ttu-id="074c5-112">Sie wird automatisch bei der Bereitstellung von Enterprise-VoIP integriert.</span><span class="sxs-lookup"><span data-stu-id="074c5-112">It is included automatically when you deploy Enterprise Voice.</span></span> <span data-ttu-id="074c5-113">Rufen Sie Parkplätze an, ruft Anrufe ab und verwaltet die Orbits des Anruf Parks.</span><span class="sxs-lookup"><span data-stu-id="074c5-113">Call Park parks and retrieves calls and manages call park orbits.</span></span>

  - <span data-ttu-id="074c5-114">**Music-on-halte-Datei**   Wenn "Musik" aktiviert ist, wird die Musikdatei wiedergegeben, während ein Anruf abgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="074c5-114">**Music-on hold-file**   If music in enabled, the music file is played while a call is parked.</span></span> <span data-ttu-id="074c5-115">Eine Standard-Musikdatei ist enthalten, wenn die Anwendung für den Parken von Anrufen installiert ist.</span><span class="sxs-lookup"><span data-stu-id="074c5-115">A default music file is included when the Call Park application is installed.</span></span>

  - <span data-ttu-id="074c5-116">**Dateispeicher**   Die Anwendung für den Anruf Park verwendet den Dateispeicher, um benutzerdefinierte Audiodateien zu speichern.</span><span class="sxs-lookup"><span data-stu-id="074c5-116">**File Store**   The Call Park application uses File Store to hold custom audio files.</span></span>

  - <span data-ttu-id="074c5-117">**Lync Server-System**   Steuerung   Sie können die lync Server-Systemsteuerung verwenden, um die Orbit-Tabelle des Anruf Parks zu konfigurieren und den Anruf Park für Benutzer zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="074c5-117">**Lync Server Control Panel**   You can use Lync Server Control Panel to configure the call park orbit table and to enable Call Park for users.</span></span>

  - <span data-ttu-id="074c5-118">**Lync Server-Verwaltungsshell**   Die Konfiguration der gesamten Anruf Park-Anwendung kann mithilfe der lync Server-Verwaltungsshell-Cmdlets ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="074c5-118">**Lync Server Management Shell**   All Call Park application configuration can be performed by using Lync Server Management Shell cmdlets.</span></span>

<span data-ttu-id="074c5-119"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="074c5-119"></div>

<span> </span>

</div>

</div>

</span></span></div>

