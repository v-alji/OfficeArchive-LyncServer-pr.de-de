---
title: 'Lync Server 2013: Anruf Diagnoseberichte'
description: 'Lync Server 2013: Anruf Diagnoseberichte.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Call Diagnostic Reports
ms:assetid: 8d362dd9-a119-4601-a3b4-3e7ed0aaa92e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615013(v=OCS.15)
ms:contentKeyID: 48184794
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 6acc41585414e134eebde1635729b470c7f3472c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394799"
---
# <a name="call-diagnostic-reports-in-lync-server-2013"></a><span data-ttu-id="275b3-103">Anruf Diagnoseberichte in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="275b3-103">Call Diagnostic Reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="275b3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="275b3-104">

<span> </span></span></span>

<span data-ttu-id="275b3-105">_**Letztes Änderungsdatum des Themas:** 2012-10-21_</span><span class="sxs-lookup"><span data-stu-id="275b3-105">_**Topic Last Modified:** 2012-10-21_</span></span>

<span data-ttu-id="275b3-106">Die Anrufdiagnoseberichte enthalten zusammenfassende Informationen und Diagnosedaten für nicht erfolgreich ausgeführte Peer-to-Peer-Sitzungen und Konferenzsitzungen.</span><span class="sxs-lookup"><span data-stu-id="275b3-106">The Call Diagnostic Reports provide summary information and diagnostic data for failed peer-to-peer and conferencing sessions.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="275b3-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="275b3-107">In This Section</span></span>

  - <span data-ttu-id="275b3-108">[Anruf Diagnose Zusammenfassungsbericht in lync Server 2013](lync-server-2013-call-diagnostic-summary-report.md)   Bietet eine Gesamtübersicht über fehlgeschlagene Peer-to-Peer-Sitzungen und Konferenzsitzungen.</span><span class="sxs-lookup"><span data-stu-id="275b3-108">[Call Diagnostic Summary Report in Lync Server 2013](lync-server-2013-call-diagnostic-summary-report.md)   Provides an overall summary of failed peer-to-peer sessions and conference sessions.</span></span> <span data-ttu-id="275b3-109">Peer-to-Peer-Sitzungen sind Sitzungen mit nur zwei Teilnehmern.</span><span class="sxs-lookup"><span data-stu-id="275b3-109">Peer-to-peer sessions are sessions that involve just two participants.</span></span> <span data-ttu-id="275b3-110">Bei Konferenzsitzungen nehmen mindestens drei Teilnehmer teil.</span><span class="sxs-lookup"><span data-stu-id="275b3-110">Conferencing sessions involve three or more participants.</span></span>

  - <span data-ttu-id="275b3-111">[Diagnosebericht zur Peer-to-Peer-Aktivität in lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md)   Bietet eine allgemeine trendansicht für fehlerhafte Peer-to-Peer-Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="275b3-111">[Peer-to-Peer Activity Diagnostic Report in Lync Server 2013](lync-server-2013-peer-to-peer-activity-diagnostic-report.md)   Provides an overall trend view of failed peer-to-peer sessions.</span></span> <span data-ttu-id="275b3-112">Bei einer Peer-to-Peer-Sitzung sind nur zwei Teilnehmer beteiligt.</span><span class="sxs-lookup"><span data-stu-id="275b3-112">A peer-to-peer session involves just two participants.</span></span>

  - <span data-ttu-id="275b3-113">[Konferenz Diagnosebericht in lync Server 2013](lync-server-2013-conference-diagnostic-report.md)   Bietet eine allgemeine trendansicht von fehlgeschlagenen Konferenzsitzungen und Trend Ansichten für die einzelnen Konferenz Modalitäten.</span><span class="sxs-lookup"><span data-stu-id="275b3-113">[Conference Diagnostic Report in Lync Server 2013](lync-server-2013-conference-diagnostic-report.md)   Provides an overall trend view of failed conferencing sessions and trend views for each conference modality.</span></span> <span data-ttu-id="275b3-114">Bei Konferenzsitzungen sind mindestens drei Teilnehmer beteiligt.</span><span class="sxs-lookup"><span data-stu-id="275b3-114">Conferencing sessions involve at least three participants.</span></span>

  - <span data-ttu-id="275b3-115">[Bericht "Top-Fehler" in lync Server 2013](lync-server-2013-top-failures-report.md)   Enthält eine Liste der häufigsten Fehler und deren Trends im Laufe der Zeit.</span><span class="sxs-lookup"><span data-stu-id="275b3-115">[Top Failures Report in Lync Server 2013](lync-server-2013-top-failures-report.md)   Provides a list of the most frequent failures and their trends over time.</span></span>

  - <span data-ttu-id="275b3-116">[Bericht zur Fehlerverteilung in lync Server 2013](lync-server-2013-failure-distribution-report.md)   Bietet eine Analyse fehlerhafter Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="275b3-116">[Failure Distribution Report in Lync Server 2013](lync-server-2013-failure-distribution-report.md)   Provides an analysis of failed sessions.</span></span>

  - <span data-ttu-id="275b3-117">[Bericht zur Fehlerliste in lync Server 2013](lync-server-2013-failure-list-report.md)   Enthält detaillierte Informationen zu den einzelnen Teilnehmern, die an einer fehlgeschlagenen Konferenz beteiligt sind.</span><span class="sxs-lookup"><span data-stu-id="275b3-117">[Failure List Report in Lync Server 2013](lync-server-2013-failure-list-report.md)   Provides detailed information about the individual participants involved in a failed conference.</span></span>

  - <span data-ttu-id="275b3-118">[Diagnosebericht in lync Server 2013](lync-server-2013-diagnostic-report.md)   Bietet Diagnose-und Problembehandlungsinformationen (einschließlich SIP-Antwortcodes und Diagnose Kopfzeilen und-IDs) für fehlerhafte Sitzungen.</span><span class="sxs-lookup"><span data-stu-id="275b3-118">[Diagnostic Report in Lync Server 2013](lync-server-2013-diagnostic-report.md)   Provides diagnostic and troubleshooting information (including SIP response codes and diagnostic headers and IDs) for failed sessions.</span></span>

<span data-ttu-id="275b3-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="275b3-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

