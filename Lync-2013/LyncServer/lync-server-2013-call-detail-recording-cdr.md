---
title: 'Lync Server 2013: Anrufdetailaufzeichnung (CDR)'
description: 'Lync Server 2013: Anrufdetailaufzeichnung (CDR).'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call detail recording (CDR)
ms:assetid: 67726075-c77c-4191-a64f-a1cf5c7bcbb2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688079(v=OCS.15)
ms:contentKeyID: 49733675
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 590f99fd0b8649ffb3c4df039488dc54a8f3b7b4
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435775"
---
# <a name="call-detail-recording-cdr-in-lync-server-2013"></a><span data-ttu-id="c2a43-103">Anrufdetailaufzeichnung (CDR) in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2a43-103">Call detail recording (CDR) in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c2a43-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c2a43-104">

<span> </span></span></span>

<span data-ttu-id="c2a43-105">_**Letztes Änderungsdatum des Themas:** 2012-10-22_</span><span class="sxs-lookup"><span data-stu-id="c2a43-105">_**Topic Last Modified:** 2012-10-22_</span></span>

<span data-ttu-id="c2a43-106">Bei der KDS (Aufzeichnung von Kommunikationsdatensätzen) werden Nutzungs- und Diagnoseinformationen über Peer-to-Peer-Aktivitäten wie Chats, VoIP-Anrufe, Anwendungsfreigaben, Dateiübertragungen und Besprechungen aufgezeichnet.</span><span class="sxs-lookup"><span data-stu-id="c2a43-106">Call detail recording (CDR) records usage and diagnostic information about peer-to-peer activities, including instance messaging, Voice over Internet Protocol (VoIP) calls, application sharing, file transfer, and meetings.</span></span> <span data-ttu-id="c2a43-107">Anhand der Nutzungsdaten kann die Rendite berechnet werden und die Diagnosedaten können zur Problembehandlung bei Peer-to-Peer-Aktivitäten und Besprechungen genutzt werden.</span><span class="sxs-lookup"><span data-stu-id="c2a43-107">The usage data can be used to calculate return on investment (ROI) and the diagnostic data can be used to troubleshoot peer-to-peer activities and meetings.</span></span> <span data-ttu-id="c2a43-108">Wenn Sie lync Server 2013 installieren, können Sie auch eine vordefinierte Sammlung globaler Konfigurationseinstellungen für CdR installieren.</span><span class="sxs-lookup"><span data-stu-id="c2a43-108">When you install Lync Server 2013, you will also install a predefined collection of global configuration settings for CDR.</span></span> <span data-ttu-id="c2a43-109">In den Themen in diesem Abschnitt wird beschrieben, wie KDS konfiguriert wird.</span><span class="sxs-lookup"><span data-stu-id="c2a43-109">Use the topics in this section to configure CDR.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="c2a43-110">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="c2a43-110">In This Section</span></span>

  - [<span data-ttu-id="c2a43-111">Anzeigen der CDR-Konfigurationsinformationen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2a43-111">View CDR configuration information in Lync Server 2013</span></span>](lync-server-2013-view-cdr-configuration-information.md)

  - [<span data-ttu-id="c2a43-112">Aktivieren der Anrufdetailaufzeichnung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2a43-112">Enable call detail recording in Lync Server 2013</span></span>](lync-server-2013-enable-call-detail-recording.md)

  - [<span data-ttu-id="c2a43-113">Erstellen oder Ändern einer Sammlung von CDR-Konfigurationseinstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2a43-113">Create or modify a collection of CDR configuration settings in Lync Server 2013</span></span>](lync-server-2013-create-or-modify-a-collection-of-cdr-configuration-settings.md)

  - [<span data-ttu-id="c2a43-114">Löschen einer vorhandenen Sammlung von CDR-Konfigurationseinstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2a43-114">Delete an existing collection of CDR configuration settings in Lync Server 2013</span></span>](lync-server-2013-delete-an-existing-collection-of-cdr-configuration-settings.md)

  - [<span data-ttu-id="c2a43-115">Manuelles Bereinigen der Datenbanken für die Anrufdetailaufzeichnung und die Qualität von Erfahrungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2a43-115">Manually purging the call detail recording and Quality of Experience databases in Lync Server 2013</span></span>](lync-server-2013-manually-purging-the-call-detail-recording-and-quality-of-experience-databases.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="c2a43-116">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c2a43-116">See Also</span></span>


[<span data-ttu-id="c2a43-117">Konfigurieren der Einstellungen für die Anrufdetailaufzeichnung und die Qualität der Benutzerfreundlichkeit in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c2a43-117">Configuring call detail recording and Quality of Experience settings in Lync Server 2013</span></span>](lync-server-2013-configuring-call-detail-recording-and-quality-of-experience-settings.md)  
  

<span data-ttu-id="c2a43-118"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c2a43-118"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

