---
title: 'Lync Server 2013: Konfigurieren von Clients für die Verwendung mit Office Web Apps Server'
description: 'Lync Server 2013: Konfigurieren von Clients für die Verwendung mit Office Web Apps Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring clients for use with Office Web Apps Server
ms:assetid: e5eaead7-0b32-42fb-97eb-ca203af59a9d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205339(v=OCS.15)
ms:contentKeyID: 48185668
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 1b9bd7cf1e76c481c40381234ba1a84cda5500dc
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395110"
---
# <a name="configuring-clients-of-lync-server-2013-for-use-with-office-web-apps-server"></a><span data-ttu-id="c7ba2-103">Konfigurieren von Clients von lync Server 2013 zur Verwendung mit Office Web Apps Server</span><span class="sxs-lookup"><span data-stu-id="c7ba2-103">Configuring clients of Lync Server 2013 for use with Office Web Apps Server</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c7ba2-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c7ba2-104">

<span> </span></span></span>

<span data-ttu-id="c7ba2-105">_**Letztes Änderungsdatum des Themas:** 2013-02-25_</span><span class="sxs-lookup"><span data-stu-id="c7ba2-105">_**Topic Last Modified:** 2013-02-25_</span></span>

<span data-ttu-id="c7ba2-106">Wenn Sie möchten, dass Benutzer die vollständigen Funktionen von Office Web App Server erfahren, sollten Sie diese Benutzer auf Microsoft lync 2013 aktualisieren. nur Benutzer von lync 2013 sind in der Lage, in PowerPoint-Folien unabhängig von der tatsächlichen PowerPoint-Präsentation zu scrollen.</span><span class="sxs-lookup"><span data-stu-id="c7ba2-106">If you want users to experience the full capabilities of Office Web App Server then you should upgrade those users to Microsoft Lync 2013; only users of Lync 2013 will be able to do such things as scroll through PowerPoint slides independent of the actual PowerPoint presentation.</span></span> <span data-ttu-id="c7ba2-107">(Dies bedeutet, dass diese Benutzer jederzeit auf jede Folie in der Präsentation zugreifen können, ohne die tatsächliche Präsentation in irgendeiner Weise zu beeinträchtigen.) Benutzer, die nicht lync 2013 verwenden, können weiterhin an Online Konferenzen teilnehmen und die PowerPoint-Präsentation anzeigen. Sie können jedoch nicht unabhängig voneinander durch die Folien scrollen, und Sie können auch keine Folienübergänge sehen oder eingebettete Videos anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c7ba2-107">(That is, these users can look at any slide in the presentation at any time, without interfering in any way with the actual presentation.) Users who are not using Lync 2013 will still be able to join online conferences and view the PowerPoint presentation; however, they will not be able to independently scroll through the slides, nor will they be able to see slide transitions or view embedded videos.</span></span>

<span data-ttu-id="c7ba2-108">Beachten Sie, dass diese Funktionen den Benutzern von lync 2013 immer zur Verfügung stehen. Dies gilt auch, wenn der PowerPoint-Referent Microsoft lync 2010 ausführt.</span><span class="sxs-lookup"><span data-stu-id="c7ba2-108">Note that these capabilities will always be available to users of Lync 2013; this is true even if the PowerPoint presenter is running Microsoft Lync 2010.</span></span> <span data-ttu-id="c7ba2-109">Wenn eine PowerPoint-Präsentation von einem Benutzer gehostet wird, der lync 2010 ausführt, wird lync Server 2013 mit Office Web Apps Server koordiniert, um sicherzustellen, dass lync 2013-Benutzer die Office Web Apps-Server Version dieser Präsentation anzeigen.</span><span class="sxs-lookup"><span data-stu-id="c7ba2-109">If a PowerPoint presentation is being hosted by a user running Lync 2010, Lync Server 2013 will coordinate with Office Web Apps Server to make sure that Lync 2013 users will view the Office Web Apps Server version of that presentation.</span></span> <span data-ttu-id="c7ba2-110">Office Web Apps Server bietet keine PowerPoint-Dienste für Benutzer mit anderen Clients als lync 2013.</span><span class="sxs-lookup"><span data-stu-id="c7ba2-110">Office Web Apps Server does not provide PowerPoint services for users running clients other than Lync 2013.</span></span> <span data-ttu-id="c7ba2-111">Stattdessen stellen diese Benutzer eine Verbindung mit dem Konferenzserver Dienst her und zeigen PowerPoint-Präsentationen auf die gleiche Weise an wie in Microsoft lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="c7ba2-111">Instead, those users connect to the Conferencing server service and view PowerPoint presentations the same way they did in Microsoft Lync Server 2010.</span></span> <span data-ttu-id="c7ba2-112">Dies bedeutet auch, dass diese Benutzer nur Zugriff auf die mehr-begrenzte Funktionen haben, die von lync Server 2010 angeboten werden.</span><span class="sxs-lookup"><span data-stu-id="c7ba2-112">This also means that these users will only have access to the more-limited capabilities offered by Lync Server 2010.</span></span>

<span data-ttu-id="c7ba2-113">Obwohl für Office Web Apps Server keine Clientkonfiguration erforderlich ist (außer beim Upgrade von Benutzern auf lync 2013), sollten Konferenzteilnehmer auf Internet Explorer 9 aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="c7ba2-113">Although no client configuration is required for Office Web Apps Server (other than upgrading users to Lync 2013), it is recommended that conference attendees be upgrade to Internet Explorer 9.</span></span> <span data-ttu-id="c7ba2-114">Obwohl auf Konferenzen über Internet Explorer 8 zugegriffen werden kann, gibt es einige Einschränkungen bei der Verwendung dieses Webbrowsers.</span><span class="sxs-lookup"><span data-stu-id="c7ba2-114">Although conferences can be accessed using Internet Explorer 8, there are some limitations to using that Web browser.</span></span> <span data-ttu-id="c7ba2-115">Beispielsweise können Benutzer von Internet Explorer 8 die Größe der PowerPoint-Phase nicht auf eine benutzerdefinierte Größe ändern. Stattdessen sind Sie auf die Verwendung einer von drei vordefinierten Phasen Größen limitiert.</span><span class="sxs-lookup"><span data-stu-id="c7ba2-115">For example, users of Internet Explorer 8 will not be able to resize the PowerPoint stage to a custom size; instead, they will be limited to using one of three predefined stage sizes.</span></span> <span data-ttu-id="c7ba2-116">Ebenso können Internet Explorer 8-Benutzer keine Mediendateien wiedergeben.</span><span class="sxs-lookup"><span data-stu-id="c7ba2-116">Likewise, Internet Explorer 8 users will not be able to play media files.</span></span>

<span data-ttu-id="c7ba2-117"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c7ba2-117"></div>

<span> </span>

</div>

</div>

</span></span></div>

