---
title: 'Lync Server 2013: Konfigurieren von Portbereichen für Ihre Edgeserver'
description: 'Lync Server 2013: Konfigurieren von Portbereichen für Ihre Edgeserver'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring port ranges for your Edge Servers
ms:assetid: 6f0ae442-6624-4e3f-849a-5b9e387fb8cf
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204996(v=OCS.15)
ms:contentKeyID: 48184469
ms.date: 07/24/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c085a5dbc32bbf56842984eae2ef8896ab895c65
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432744"
---
# <a name="configuring-port-ranges-for-your-edge-servers-in-lync-server-2013"></a><span data-ttu-id="37573-103">Konfigurieren von Portbereichen für Ihre Edgeserver in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="37573-103">Configuring port ranges for your Edge Servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="37573-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="37573-104">

<span> </span></span></span>

<span data-ttu-id="37573-105">_**Letztes Änderungsdatum des Themas:** 2015-07-24_</span><span class="sxs-lookup"><span data-stu-id="37573-105">_**Topic Last Modified:** 2015-07-24_</span></span>

<span data-ttu-id="37573-106">Bei Edge-Servern müssen Sie keine separaten Portbereiche für Audio-, Video-und Anwendungsfreigaben konfigurieren. Ebenso müssen die für Edgeserver verwendeten Portbereiche nicht den Portbereichen entsprechen, die mit ihren Konferenz-, Anwendungs-und Vermittlungsservern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="37573-106">With Edge servers you do not have to configure separate port ranges for audio, video, and application sharing; likewise, the port ranges used for Edge servers do not have to match the port ranges used with your Conferencing, Application, and Mediation servers.</span></span> <span data-ttu-id="37573-107">Bevor wir mit unserem Beispiel fortfahren, ist es wichtig zu betonen, dass diese Option zwar vorhanden ist, aber wir empfehlen, die Portbereiche nicht zu ändern, da sich dies negativ auf einige Szenarien auswirken kann, wenn Sie den 50000-Portbereich verschieben.</span><span class="sxs-lookup"><span data-stu-id="37573-107">Before we proceed with our example, it's important to stress that while this option exists, we do recommend you not change the port ranges, as this may adversely affect some scenarios if you move out of the 50000 port range.</span></span>

<span data-ttu-id="37573-108">Angenommen, Sie haben Ihre Konferenz-, Anwendungs-und Vermittlungsserver so konfiguriert, dass Sie diese Portbereiche verwenden:</span><span class="sxs-lookup"><span data-stu-id="37573-108">For example, suppose you have configured your Conferencing, Application, and Mediation servers to use these port ranges:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="37573-109">Pakettyp</span><span class="sxs-lookup"><span data-stu-id="37573-109">Packet Type</span></span></th>
<th><span data-ttu-id="37573-110">Port wird gestartet</span><span class="sxs-lookup"><span data-stu-id="37573-110">Starting Port</span></span></th>
<th><span data-ttu-id="37573-111">Anzahl der reservierten Ports</span><span class="sxs-lookup"><span data-stu-id="37573-111">Number of Ports Reserved</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="37573-112">Anwendungsfreigabe</span><span class="sxs-lookup"><span data-stu-id="37573-112">Application sharing</span></span></p></td>
<td><p><span data-ttu-id="37573-113">40803</span><span class="sxs-lookup"><span data-stu-id="37573-113">40803</span></span></p></td>
<td><p><span data-ttu-id="37573-114">8348</span><span class="sxs-lookup"><span data-stu-id="37573-114">8348</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37573-115">Audio</span><span class="sxs-lookup"><span data-stu-id="37573-115">Audio</span></span></p></td>
<td><p><span data-ttu-id="37573-116">49152</span><span class="sxs-lookup"><span data-stu-id="37573-116">49152</span></span></p></td>
<td><p><span data-ttu-id="37573-117">8348</span><span class="sxs-lookup"><span data-stu-id="37573-117">8348</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="37573-118">Video</span><span class="sxs-lookup"><span data-stu-id="37573-118">Video</span></span></p></td>
<td><p><span data-ttu-id="37573-119">57500</span><span class="sxs-lookup"><span data-stu-id="37573-119">57500</span></span></p></td>
<td><p><span data-ttu-id="37573-120">8034</span><span class="sxs-lookup"><span data-stu-id="37573-120">8034</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="37573-121"><strong>Summen</strong></span><span class="sxs-lookup"><span data-stu-id="37573-121"><strong>Totals</strong></span></span></p></td>
<td><p>--</p></td>
<td><p><span data-ttu-id="37573-122">24730</span><span class="sxs-lookup"><span data-stu-id="37573-122">24730</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="37573-123">Wie Sie sehen können, beginnen Ihre Portbereiche für Audio-, Video-und Anwendungsfreigabe bei Port 40803 und umfassen insgesamt 24732-Ports.</span><span class="sxs-lookup"><span data-stu-id="37573-123">As you can see, your port ranges for audio, video, and application sharing start at port 40803 and encompass a total of 24732 ports.</span></span> <span data-ttu-id="37573-124">Wenn Sie möchten, können Sie einen bestimmten Edgeserver so konfigurieren, dass diese Gesamt Port Werte verwendet werden, indem Sie in der lync Server-Verwaltungsshell einen ähnlichen Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="37573-124">If you prefer, you can configure a given Edge Server to use these overall port values by running a command similar to this one from within the Lync Server Management Shell:</span></span>

    Set-CsEdgeServer -Identity EdgeServer:atl-edge-001.litwareinc.com -MediaCommunicationPortStart 40803 -MediaCommunicationPortCount 24730

<span data-ttu-id="37573-125">Oder verwenden Sie den folgenden Befehl, um alle Edgeserver in Ihrer Organisation gleichzeitig zu konfigurieren:</span><span class="sxs-lookup"><span data-stu-id="37573-125">Or, use the following command to simultaneously configure all the Edge Servers in your organization:</span></span>

    Get-CsService -EdgeServer | ForEach-Object {Set-CsEdgeServer -Identity $_.Identity -MediaCommunicationPortStart 40803 -MediaCommunicationPortCount 24730}

<span data-ttu-id="37573-126">Sie können die aktuellen Porteinstellungen für Ihre Edgeserver mithilfe dieses Befehls der lync Server-Verwaltungsshell überprüfen:</span><span class="sxs-lookup"><span data-stu-id="37573-126">You can verify the current port settings for your Edge Servers by using this Lync Server Management Shell command:</span></span>

    Get-CsService -EdgeServer | Select-Object Identity, MediaCommunicationPortStart, MediaCommunicationPortCount

<span data-ttu-id="37573-127">Auch wenn wir diese Optionen zur Verfügung stellen, empfehlen wir Ihnen dringend, die Einstellungen für die Port-Konfiguration zu belassen.</span><span class="sxs-lookup"><span data-stu-id="37573-127">Again, while we do provide these options, we strongly recommend you leave things as they are for the port configuration.</span></span>

<span data-ttu-id="37573-128"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="37573-128"></div>

<span> </span>

</div>

</div>

</span></span></div>

