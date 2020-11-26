---
title: Zurücksetzen der Anrufsteuerung
description: Anrufsteuerung zurücksetzen.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Reset call admission control
ms:assetid: 5873f56c-f3d6-4d73-beea-c9f37d5077f6
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688064(v=OCS.15)
ms:contentKeyID: 49733658
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c4539cda453de6249be3a9b9b61521ecf478cb70
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443622"
---
# <a name="reset-call-admission-control"></a><span data-ttu-id="e10dc-103">Zurücksetzen der Anrufsteuerung</span><span class="sxs-lookup"><span data-stu-id="e10dc-103">Reset call admission control</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e10dc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e10dc-104">

<span> </span></span></span>

<span data-ttu-id="e10dc-105">_**Letztes Änderungsdatum des Themas:** 2012-10-11_</span><span class="sxs-lookup"><span data-stu-id="e10dc-105">_**Topic Last Modified:** 2012-10-11_</span></span>

<span data-ttu-id="e10dc-106">Wenn ein lync Server 2010-Front-End-Pool Anrufannahme Steuerung (CAC) hostet, müssen Sie das CAC-Hosting in einen lync Server 2013-Pool verschieben, bevor Sie den lync Server 2010-Front-End-Pool entfernen können.</span><span class="sxs-lookup"><span data-stu-id="e10dc-106">If a Lync Server 2010 Front End pool is hosting call admission control (CAC), you must move CAC hosting to a Lync Server 2013 pool before you can remove the Lync Server 2010 Front End pool.</span></span>

<div>

## <a name="to-reset-cac"></a><span data-ttu-id="e10dc-107">So setzen Sie CAC zurück</span><span class="sxs-lookup"><span data-stu-id="e10dc-107">To reset CAC</span></span>

1.  <span data-ttu-id="e10dc-108">Öffnen Sie den Topologie-Generator.</span><span class="sxs-lookup"><span data-stu-id="e10dc-108">Open Topology Builder.</span></span>

2.  <span data-ttu-id="e10dc-109">Klicken Sie mit der rechten Maustaste auf den Websiteknoten, und klicken Sie dann auf **Eigenschaften bearbeiten**.</span><span class="sxs-lookup"><span data-stu-id="e10dc-109">Right-click the site node, and then click **Edit Properties**.</span></span>

3.  <span data-ttu-id="e10dc-110">Vergewissern Sie sich, dass unter Einstellungen für die **Anrufsteuerung** die Option **Anrufsteuerung aktivieren** aktiviert ist.</span><span class="sxs-lookup"><span data-stu-id="e10dc-110">Under **Call Admission Control setting**, make sure **Enable Call Admission Control** is selected.</span></span>

4.  <span data-ttu-id="e10dc-111">Wählen Sie unter **Front-End-Pool zum Ausführen der Anrufannahme Steuerung (CAC)** den lync Server 2013-Pool aus, der CAC hosten soll, und klicken Sie dann auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="e10dc-111">Under **Front End pool to run call admission control (CAC)**, select the Lync Server 2013 pool that is to host CAC, and then click **OK**.</span></span>

5.  <span data-ttu-id="e10dc-112">Veröffentlichen Sie die Topologie.</span><span class="sxs-lookup"><span data-stu-id="e10dc-112">Publish the topology.</span></span>

<span data-ttu-id="e10dc-113"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e10dc-113"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

