---
title: 'Lync Server 2013: Überprüfen der Konfiguration von Office Web Apps Server'
description: 'Lync Server 2013: Überprüfen der Konfiguration von Office Web Apps Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Validating the configuration of Office Web Apps Server
ms:assetid: f6e8ecbf-305d-4a13-92d0-b61dbd82b0ea
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205393(v=OCS.15)
ms:contentKeyID: 48185859
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 80c3160dd9a76c129fbb0289929a868b897beb2c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440444"
---
# <a name="validating-the-configuration-of-office-web-apps-server-in-lync-server-2013"></a><span data-ttu-id="25831-103">Überprüfen der Konfiguration von Office Web Apps Server in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="25831-103">Validating the configuration of Office Web Apps Server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="25831-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="25831-104">

<span> </span></span></span>

<span data-ttu-id="25831-105">_**Letztes Änderungsdatum des Themas:** 2014-04-22_</span><span class="sxs-lookup"><span data-stu-id="25831-105">_**Topic Last Modified:** 2014-04-22_</span></span>

<span data-ttu-id="25831-106">Nachdem Office Web Apps Server zur Topologie hinzugefügt wurde und die Topologie veröffentlicht wurde, sollten im lync Server-Ereignisprotokoll zwei neue Ereignisprotokoll Ereignisse angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="25831-106">After Office Web Apps Server has been added to the topology, and after that topology has been published, you should see two new event log events in the Lync Server event log.</span></span> <span data-ttu-id="25831-107">Zunächst sollte ein ls-Daten MCU-Ereignis (Ereignis-ID 41034) hinzugefügt werden. Dieses Ereignis meldet, dass der Office Web Apps-Server erkannt wurde:</span><span class="sxs-lookup"><span data-stu-id="25831-107">First, an LS Data MCU event (event ID 41034) should be added; this event will report that the Office Web Apps Server has been discovered:</span></span>

<span data-ttu-id="25831-108">**Der Webkonferenzserver Office Web Apps-Server wurde ermittelt, PowerPoint-Inhalte sind aktiviert.**</span><span class="sxs-lookup"><span data-stu-id="25831-108">**Web Conferencing Server Office Web Apps Server is discovered, PowerPoint content is enabled.**</span></span>

<span data-ttu-id="25831-p102">Außerdem sollte ein weiteres "LS Data MCU"-Ereignis angezeigt werden (Ereignis-ID 41032), das Office Web Apps Server-URLs zurückmeldet. Beispielsweise sollten Meldungen wie etwa folgende angezeigt werden:</span><span class="sxs-lookup"><span data-stu-id="25831-p102">In addition to that you should see another LS Data MCU event (event ID 41032) that reports back Office Web Apps Server URLs. For example, you should see something similar to this:</span></span>

<span data-ttu-id="25831-111">**Die Ermittlung des Webkonferenzservers Office Web Apps-Server war erfolgreich.**</span><span class="sxs-lookup"><span data-stu-id="25831-111">**Web Conferencing Server Office Web Apps Server discovery has succeeded.**</span></span>

<span data-ttu-id="25831-112">**Office Web Apps Server-interne Referenten Seite: https://atl-officewebapps-001.litwareinc.com/m/Presenter.aspx?a=0\&embed=**</span><span class="sxs-lookup"><span data-stu-id="25831-112">**Office Web Apps Server internal presenter page: https://atl-officewebapps-001.litwareinc.com/m/Presenter.aspx?a=0\&embed=**</span></span>

<span data-ttu-id="25831-113">**Office Web Apps Server-Seite für interne Teilnehmer: https://atl-officewebapps-001.litwareinc.com/m/ParticipantFrame.aspx?a=0\&embed=true&=**</span><span class="sxs-lookup"><span data-stu-id="25831-113">**Office Web Apps Server internal attendee page: https://atl-officewebapps-001.litwareinc.com/m/ParticipantFrame.aspx?a=0\&embed=true&=**</span></span>

<span data-ttu-id="25831-114">**Office Web Apps Server-externe Referenten Seite: https://atl-officewebapps-001.litwareinc.com/m/Presenter.aspx?a=0\&embed**</span><span class="sxs-lookup"><span data-stu-id="25831-114">**Office Web Apps Server external presenter page: https://atl-officewebapps-001.litwareinc.com/m/Presenter.aspx?a=0\&embed**</span></span>

<span data-ttu-id="25831-115">**Office Web Apps Server-Seite für interne Teilnehmer: https://atl-officewebapps-001.litwareinc.com/m/ParticipantFrame.aspx?a=0\&embed=true&**</span><span class="sxs-lookup"><span data-stu-id="25831-115">**Office Web Apps Server internal attendee page: https://atl-officewebapps-001.litwareinc.com/m/ParticipantFrame.aspx?a=0\&embed=true&**</span></span>

<span data-ttu-id="25831-116">Wenn ein ls-Daten MCU-Ereignis mit der Ereignis-ID von 41033 angezeigt wird, bedeutet dies, dass die Server Ermittlung von Office Web Apps fehlgeschlagen ist.</span><span class="sxs-lookup"><span data-stu-id="25831-116">If you see an LS Data MCU event with the event ID of 41033 that means that Office Web Apps Server discovery has failed.</span></span> <span data-ttu-id="25831-117">In diesem Fall wird Microsoft lync Server 2013 so oft wie erforderlich versuchen, um den neu konfigurierten Office Web Apps-Server zu entdecken.</span><span class="sxs-lookup"><span data-stu-id="25831-117">In that case, Microsoft Lync Server 2013 will try as many times as needed to discover the newly-configured Office Web Apps Server.</span></span> <span data-ttu-id="25831-118">Wenn der Ermittlungsvorgang wiederholt fehlschlägt, sollten Sie Office Web Apps Server aus Ihrem Topologie-Dokument entfernen, die aktualisierte Topologie veröffentlichen und dann versuchen, Office Web Apps Server wieder zur Topologie hinzuzufügen, nachdem die Verbindungsprobleme behoben wurden.</span><span class="sxs-lookup"><span data-stu-id="25831-118">If the discovery process fails repeatedly you should remove Office Web Apps Server from your topology document, publish the updated topology, and then try adding Office Web Apps Server back to the topology after the connectivity issues have been resolved.</span></span>

<span data-ttu-id="25831-119">Wenn Office Web Apps Server anscheinend ordnungsgemäß konfiguriert wurde und vom Ermittlungsprozess erkannt wurde, können Sie überprüfen, ob der Office Web Apps-Server wie erwartet funktioniert, indem Sie eine PowerPoint-Präsentation zwischen zwei Microsoft lync 2013-Clients freigeben.</span><span class="sxs-lookup"><span data-stu-id="25831-119">If Office Web Apps Server appears to be configured correctly and has been recognized by the discovery process you can verify that Office Web Apps Server is working as expected by sharing a PowerPoint presentation between a pair of Microsoft Lync 2013 clients.</span></span> <span data-ttu-id="25831-120">Wenn Benutzer a die PowerPoint-Präsentation laden und anzeigen kann und wenn Benutzer B dann an der Besprechung teilnehmen und diese Präsentation sehen kann, funktioniert der Office Web Apps-Server.</span><span class="sxs-lookup"><span data-stu-id="25831-120">If User A can load and display the PowerPoint presentation and if User B can then join the meeting and see that presentation then Office Web Apps Server is working.</span></span>

<span data-ttu-id="25831-121">Auch wenn Office Web Apps Server anscheinend richtig konfiguriert ist, können Sie möglicherweise die Fehlermeldung "einige Freigabefeatures sind aufgrund von Server Verbindungsproblemen nicht verfügbar" erhalten, wenn Sie versuchen, eine PowerPoint-Präsentation freizugeben.</span><span class="sxs-lookup"><span data-stu-id="25831-121">Even if Office Web Apps Server appears to be configured correctly, you could potentially receive the error message “Some sharing features are unavailable due to server connectivity issues” when you try sharing a PowerPoint presentation.</span></span> <span data-ttu-id="25831-122">Wenn diese Fehlermeldung angezeigt wird, sollten Sie den Front-End-Server (oder die Server) neu starten, die dem neuen Office Web Apps-Server zugeordnet sind.</span><span class="sxs-lookup"><span data-stu-id="25831-122">If you receive that error message you should restart the Front End server (or servers) associated with the new Office Web Apps Server.</span></span>

<span data-ttu-id="25831-123"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="25831-123"></div>

<span> </span>

</div>

</div>

</span></span></div>

