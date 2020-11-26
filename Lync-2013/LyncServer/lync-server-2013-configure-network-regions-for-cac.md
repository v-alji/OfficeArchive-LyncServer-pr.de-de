---
title: 'Lync Server 2013: Konfigurieren von netzwerkregionen für CAC'
description: 'Lync Server 2013: Konfigurieren von netzwerkregionen für CAC.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure network regions for CAC
ms:assetid: ea3ff988-dd5a-4bc4-bec5-39a0fb09793a
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399051(v=OCS.15)
ms:contentKeyID: 48185906
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f016e0c943963ea4ce9739bd486c6996da502e73
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433871"
---
# <a name="configure-network-regions-for-cac-in-lync-server-2013"></a>Konfigurieren von netzwerkregionen für CAC in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-21_

<div>


> [!IMPORTANT]  
> Wenn Sie bereits netzwerkregionen für E9-1-1 oder Media Bypass erstellt haben, können Sie die vorhandenen netzwerkregionen ändern, indem Sie mithilfe des Cmdlets " <STRONG>festlegen-CsNetworkRegion</STRONG> " spezifische Einstellungen für die Anrufannahme Steuerung (CAC) hinzufügen. Ein Beispiel für das Ändern eines Netzwerkbereichs finden Sie unter <A href="lync-server-2013-create-or-modify-a-network-region.md">erstellen oder Ändern eines Netzwerkbereichs in lync Server 2013</A>.



</div>

*Netzwerkregionen* sind die Netzwerkhubs oder Backbones, die bei der Konfiguration von CAC, E9-1-1 und medienumgehung verwendet werden. Gehen Sie wie folgt vor, um netzwerkregionen zu erstellen, die in der Beispiel Netzwerktopologie für CAC an netzwerkregionen ausgerichtet sind. Informationen zum Anzeigen der Beispiel Netzwerktopologie finden Sie unter [Beispiel: Sammeln Ihrer Anforderungen für die Anrufsteuerung in lync Server 2013](lync-server-2013-example-of-gathering-your-requirements-for-call-admission-control.md) in der Planungsdokumentation.

Die Beispiel Netzwerktopologie für CAC umfasst drei Regionen: Nordamerika, EMEA und APAC. Jede Region hat eine angegebene zentrale Website. Für die Region Nordamerika hat der designierte zentrale Standort den Namen Chicago. Das folgende Verfahren zeigt ein Beispiel dafür, wie Sie das Cmdlet **New-CsNetworkRegion** zum Erstellen der Region Nordamerika verwenden können.

<div>


> [!NOTE]  
> Im folgenden Verfahren wird die lync Server-Verwaltungsshell zum Erstellen eines Netzwerkbereichs verwendet. Details zur Verwendung der lync Server-Systemsteuerung zum Erstellen eines Netzwerkbereichs finden Sie unter <A href="lync-server-2013-create-or-modify-a-network-region.md">erstellen oder Ändern eines Netzwerkbereichs in lync Server 2013</A>.



</div>

<div>

## <a name="to-create-a-network-region-for-call-admission-control"></a>So erstellen Sie einen Netzwerkbereich für die Anrufsteuerung

1.  Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.

2.  Führen Sie für jede Region, die Sie erstellen müssen, das Cmdlet **New-CsNetworkRegion** aus. Wenn Sie beispielsweise die Region Nordamerika erstellen möchten, führen Sie Folgendes aus:
    
        New-CsNetworkRegion -Identity NorthAmerica -CentralSite CHICAGO -Description "All North America Locations"

3.  Wiederholen Sie Schritt 2, um die netzwerkregionen EMEA und APAC zu erstellen.

</div>

</div>

<span> </span>

</div>

</div>

</div>

