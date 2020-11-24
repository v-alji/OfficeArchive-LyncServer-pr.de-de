---
title: 'Lync Server 2013: Überprüfen der Konnektivität für externe Benutzer'
description: 'Lync Server 2013: Überprüfen der Konnektivität für externe Benutzer'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Verify connectivity for external users
ms:assetid: 5c02bd6e-1c96-448a-a21d-58c9961c6640
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398402(v=OCS.15)
ms:contentKeyID: 48184249
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 50ef728157d01b93e7d0b8420442ce083a42b5b2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395046"
---
# <a name="verify-connectivity-for-external-users-in-lync-server-2013"></a><span data-ttu-id="24e26-103">Überprüfen der Konnektivität für externe Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="24e26-103">Verify connectivity for external users in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="24e26-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="24e26-104">

<span> </span></span></span>

<span data-ttu-id="24e26-105">_**Letztes Änderungsdatum des Themas:** 2012-10-19_</span><span class="sxs-lookup"><span data-stu-id="24e26-105">_**Topic Last Modified:** 2012-10-19_</span></span>

<span data-ttu-id="24e26-106">Zum Überprüfen der Konnektivität für externe Benutzer muss die Konnektivität zwischen Benutzern und dem Server und Port für den Access Edge-Dienst sichergestellt werden.</span><span class="sxs-lookup"><span data-stu-id="24e26-106">Validating connectivity for external users requires ensuring connectivity from users to the server and port for the Access Edge service.</span></span>

<span data-ttu-id="24e26-107">Eine wertvolle Ressource für die Bestätigung Ihrer Konfiguration und die Möglichkeit zum Verbinden, senden und empfangen der richtigen Nachrichten für die Szenarien, für die der Zugriff durch externe Benutzer erforderlich ist, ist die Remote Connectivity Analyzer-Website ( <http://www.testocsconnectivity.com> ).</span><span class="sxs-lookup"><span data-stu-id="24e26-107">A valuable resource for confirming your configuration and the ability to connect, send and receive the correct messages for the scenarios that external user access requires is the Remote Connectivity Analyzer site (<http://www.testocsconnectivity.com>).</span></span> <span data-ttu-id="24e26-108">Die Website wird vom Microsoft-Support verwaltet und verwaltet.</span><span class="sxs-lookup"><span data-stu-id="24e26-108">The site is managed and maintained by Microsoft Support.</span></span> <span data-ttu-id="24e26-109">Zum Erreichen des Remote Connectivity Analyzer öffnen Sie die Website in einem Browser, und folgen Sie den Anweisungen, um das Szenario auszuwählen.</span><span class="sxs-lookup"><span data-stu-id="24e26-109">To reach the Remote Connectivity Analyzer, open the Web site in a browser and follow the instructions to select the scenario.</span></span>

<div>

## <a name="test-connectivity-of-external-users-and-external-access"></a><span data-ttu-id="24e26-110">Testen der Konnektivität externer Benutzer und des externen Zugriffs</span><span class="sxs-lookup"><span data-stu-id="24e26-110">Test Connectivity of External Users and External access</span></span>

<span data-ttu-id="24e26-111">Tests für den Zugriff durch externe Benutzer sollten alle externen Benutzertypen enthalten, die von Ihrer Organisation unterstützt werden, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="24e26-111">Tests for external user access should include each type of external user that your organization supports, including any or all of the following:</span></span>

  - <span data-ttu-id="24e26-112">Benutzer aus mindestens einer Föderationsdomäne und Test-Chat, Anwesenheit, A/V und Desktopfreigabe.</span><span class="sxs-lookup"><span data-stu-id="24e26-112">Users from at least one federated domain, and test IM, presence, A/V and desktop sharing.</span></span>

  - <span data-ttu-id="24e26-113">Benutzer jedes öffentlichen Chat Dienstanbieters, den Ihre Organisation unterstützt (und für die die Bereitstellung abgeschlossen wurde).</span><span class="sxs-lookup"><span data-stu-id="24e26-113">Users of each public IM service provider that your organization supports (and for which provisioning has been completed).</span></span>

  - <span data-ttu-id="24e26-114">Anonyme Benutzer.</span><span class="sxs-lookup"><span data-stu-id="24e26-114">Anonymous users.</span></span>

  - <span data-ttu-id="24e26-115">Benutzer in Ihrer Organisation, die bei lync Remote angemeldet sind, aber keine VPN-Verbindung verwenden.</span><span class="sxs-lookup"><span data-stu-id="24e26-115">Users within your organization who are logged into Lync remotely, but not using VPN.</span></span>

<span data-ttu-id="24e26-116">Diese Tests bestimmen, ob der Edgeserver wie folgt lautet:</span><span class="sxs-lookup"><span data-stu-id="24e26-116">These tests determine whether your Edge Server is:</span></span>

  - <span data-ttu-id="24e26-117">Überwachen der erforderlichen Ports durch Verwendung eines telnet-Clients außerhalb Ihres Netzwerks.</span><span class="sxs-lookup"><span data-stu-id="24e26-117">Listening on the necessary ports by using a telnet client from outside your network.</span></span>
    
      - <span data-ttu-id="24e26-118">Beispiel: Telnet SIP.contoso.com 443</span><span class="sxs-lookup"><span data-stu-id="24e26-118">Example: telnet sip.contoso.com 443</span></span>
    
      - <span data-ttu-id="24e26-119">Führen Sie den vorhergehenden Test für Ports aus, die Sie je nach Bereitstellung auf dem Edgeserver oder Edgeserver-Pool verwenden.</span><span class="sxs-lookup"><span data-stu-id="24e26-119">Perform the preceding test on ports you are using on the Edge Server or Edge Server pool depending on your deployment.</span></span>

  - <span data-ttu-id="24e26-120">Ausführen einer präzisen externen DNS-Auflösung.</span><span class="sxs-lookup"><span data-stu-id="24e26-120">Performing accurate external DNS resolution.</span></span>
    
      - <span data-ttu-id="24e26-121">Pingen Sie von außerhalb Ihres Netzwerks jeden der externen FQDN des Edge-oder Edge-Pools.</span><span class="sxs-lookup"><span data-stu-id="24e26-121">From outside your network ping each of the external FQDN’s of your Edge or Edge pool.</span></span> <span data-ttu-id="24e26-122">Auch wenn der ping fehlschlägt, werden die IP-Adressen angezeigt, die Sie mit den zugewiesenen vergleichen können.</span><span class="sxs-lookup"><span data-stu-id="24e26-122">Even if the ping fails you will see the IP addresses, which you can compare to the ones you have assigned.</span></span>

<span data-ttu-id="24e26-123"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="24e26-123"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

