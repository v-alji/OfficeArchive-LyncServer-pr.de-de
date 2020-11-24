---
title: 'Lync Server 2013: Diagnoseberichte für Medienqualität'
description: 'Lync Server 2013: Diagnoseberichte für Medienqualität.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Media Quality Diagnostic Reports
ms:assetid: ea61428e-a1d5-4189-aae6-3db19ddc5cf2
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615044(v=OCS.15)
ms:contentKeyID: 48185935
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2e346d0f9b8997158cb926ad830d5477950e846d
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395203"
---
# <a name="media-quality-diagnostic-reports-in-lync-server-2013"></a><span data-ttu-id="0e9eb-103">Berichte zur Medien Qualitäts Diagnose in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0e9eb-103">Media Quality Diagnostic Reports in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0e9eb-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0e9eb-104">

<span> </span></span></span>

<span data-ttu-id="0e9eb-105">_**Letztes Änderungsdatum des Themas:** 2013-02-22_</span><span class="sxs-lookup"><span data-stu-id="0e9eb-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="0e9eb-106">Die Medienqualitäts-Diagnoseberichte bieten Informationen über die Anrufqualität sowie Diagnosedaten und Hinweise zur Problembehandlung für Anrufe, bei denen Fehler aufgetreten sind.</span><span class="sxs-lookup"><span data-stu-id="0e9eb-106">The Media Quality Diagnostic Reports provide information about call quality, and diagnostic and troubleshooting information for failed calls.</span></span>

<div>

## <a name="in-this-section"></a><span data-ttu-id="0e9eb-107">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="0e9eb-107">In This Section</span></span>

  - <span data-ttu-id="0e9eb-108">[Zusammenfassungsbericht für Medienqualität in lync Server 2013](lync-server-2013-media-quality-summary-report.md)   Bietet allgemeine Qualitätsdaten für unterschiedliche Endpunkttypen, darunter Enterprise-VoIP-Peer-to-Peer-Anrufe, Enterprise-VoIP-Konferenzanrufe und Anrufe, die zumindest teilweise auf dem öffentlichen Telefonnetz (PSTN) beruhen.</span><span class="sxs-lookup"><span data-stu-id="0e9eb-108">[Media Quality Summary Report in Lync Server 2013](lync-server-2013-media-quality-summary-report.md)   Provides overall quality data for different endpoint types, including Enterprise Voice peer-to-peer calls, Enterprise Voice conference calls, and calls that rely, at least in part, on the public switched telephone network (PSTN).</span></span>

  - <span data-ttu-id="0e9eb-109">[Bericht zum Vergleich der Medienqualität in lync Server 2013](lync-server-2013-media-quality-comparison-report.md)   Bietet einen Vergleich der Werte für die Anrufqualität für verschiedene Arten von Audioanrufen (beispielsweise Anrufe, die über ein Drahtlosnetzwerk getätigt wurden, und Anrufe, die über eine Kabelverbindung erfolgen).</span><span class="sxs-lookup"><span data-stu-id="0e9eb-109">[Media Quality Comparison Report in Lync Server 2013](lync-server-2013-media-quality-comparison-report.md)   Provides a comparison of call quality values for different types of audio calls (for example, calls made over a wireless network vs. calls made across a wired connection).</span></span>

  - <span data-ttu-id="0e9eb-110">[Bericht zur Server Leistung in lync Server 2013](lync-server-2013-server-performance-report.md)   Listet die Server auf, bei denen die meisten Probleme aufgetreten sind, basierend auf der Messung solcher wichtigen Qualitäts Metriken wie Degradation, Paketverlust und Jitter.</span><span class="sxs-lookup"><span data-stu-id="0e9eb-110">[Server Performance Report in Lync Server 2013](lync-server-2013-server-performance-report.md)   Lists the servers that have experienced the most problems, based on measurements of such key quality metrics as degradation, packet loss, and jitter.</span></span>

  - <span data-ttu-id="0e9eb-111">[Standortbericht in lync Server 2013](lync-server-2013-location-report.md)   Enthält eine Liste der Netzwerkspeicherorte und eine Zusammenfassung der Medienqualität der Anrufe, die an jedem Standort erfolgen.</span><span class="sxs-lookup"><span data-stu-id="0e9eb-111">[Location Report in Lync Server 2013](lync-server-2013-location-report.md)   Provides a list of network locations and a summary of the media quality of the calls that occur at each location.</span></span> <span data-ttu-id="0e9eb-112">Für die Zwecke dieses Berichts basieren Speicherorte auf IP-Subnetzen.</span><span class="sxs-lookup"><span data-stu-id="0e9eb-112">For purposes of this report, locations are based on IP subnets.</span></span>

  - <span data-ttu-id="0e9eb-113">[Gerätebericht in lync Server 2013](lync-server-2013-device-report.md)   Enthält eine Zusammenfassung der Geräte, die für Enterprise-VoIP-Anrufe verwendet werden, und umfasst die durchschnittliche Medienqualität der Anrufe nach Gerät.</span><span class="sxs-lookup"><span data-stu-id="0e9eb-113">[Device Report in Lync Server 2013](lync-server-2013-device-report.md)   Provides a summary of devices that are used for Enterprise Voice calls and it includes the average media quality of the calls by device.</span></span>

  - <span data-ttu-id="0e9eb-114">[Bericht zur Anrufliste in lync Server 2013](lync-server-2013-call-list-report.md)   Enthält detaillierte Informationen zu Telefon anrufen, die in Ihrer Organisation getätigt oder empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="0e9eb-114">[Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md)   Provides detailed information about phone calls made or received within your organization.</span></span>

  - <span data-ttu-id="0e9eb-115">[Anruf Detail Bericht in lync Server 2013](lync-server-2013-call-detail-report.md)   Enthält detaillierte Informationen zu Telefon anrufen, die in Ihrer Organisation getätigt oder empfangen wurden.</span><span class="sxs-lookup"><span data-stu-id="0e9eb-115">[Call Detail Report in Lync Server 2013](lync-server-2013-call-detail-report.md)   Provides detailed information about phone calls made from or received within your organization.</span></span>

  - <span data-ttu-id="0e9eb-116">[Trend Bericht zur Server Medienqualität in lync Server 2013](lync-server-2013-server-media-quality-trend-report.md)   Bietet eine Möglichkeit, bis zu 5 Server auf der Grundlage der Qualität von Erfahrungswerten wie Anruflautstärke, schlechtem Anruf Prozentsatz, Paketverlust und Jitter grafisch zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="0e9eb-116">[Server Media Quality Trend Report in Lync Server 2013](lync-server-2013-server-media-quality-trend-report.md)   Provides a way for you to graphically compare up to 5 servers on Quality of Experience metrics such as call volume, poor call percentage, packet loss, and jitter.</span></span>

  - <span data-ttu-id="0e9eb-117">[Der Verteilungs Bericht zur Medien Qualitätsmetrik in lync Server 2013](lync-server-2013-media-quality-metrics-distribution-report.md)   Stellt ein Diagramm bereit, in dem die Verteilungswerte für eine Qualität der Erfahrungs Metrik wie Jitter oder Paketverlust angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="0e9eb-117">[The Media Quality Metrics Distribution Report in Lync Server 2013](lync-server-2013-media-quality-metrics-distribution-report.md)   Provides a graph that shows the distribution values for a Quality of Experience metric such as jitter or packet loss.</span></span>

  - <span data-ttu-id="0e9eb-118">[Standort Trend Bericht in lync Server 2013](lync-server-2013-location-trend-report.md)   Bietet Trendinformationen zur Anrufqualität für Netzwerkspeicherorte.</span><span class="sxs-lookup"><span data-stu-id="0e9eb-118">[Location Trend Report in Lync Server 2013](lync-server-2013-location-trend-report.md)   Provides call quality trend information for network locations.</span></span>

<span data-ttu-id="0e9eb-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0e9eb-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

