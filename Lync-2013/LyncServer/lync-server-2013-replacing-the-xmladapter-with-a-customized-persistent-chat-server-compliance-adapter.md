---
title: 'Lync Server 2013: Ersetzen des xmladapters durch einen angepassten beständigen Chat Server-Kompatibilitätsadapter'
description: 'Lync Server 2013: Ersetzen des xmladapters durch einen angepassten beständigen Chat Server-Kompatibilitätsadapter.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Replacing the XmlAdapter with a customized Persistent Chat Server Compliance adapter
ms:assetid: 2cb70db2-663f-40a6-abcf-89ea7d4a8b65
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ680106(v=OCS.15)
ms:contentKeyID: 49558152
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 3a90b4df7df42ffdc6c55e9b551b0eb53d07ab1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394511"
---
# <a name="replacing-the-xmladapter-with-a-customized-persistent-chat-server-compliance-adapter-in-lync-server-2013"></a>Ersetzen des xmladapters durch einen angepassten beständigen Chat Server-Kompatibilitätsadapter in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-11-01_

Sie können einen benutzerdefinierten Adapter schreiben, anstatt den XMLAdapter zu verwenden, der mit dem Server für beständigen Chat installiert ist. Hierzu müssen Sie eine .NET Framework-Assembly bereitstellen, die eine öffentliche Klasse enthält, die die **IComplianceAdapter**-Schnittstelle implementiert. Sie müssen diese Assembly im beständigen Chat Server-Installationsordner für jeden Server im beständigen Chat Serverpool platzieren. Jeder der Konformitätsserver kann Konformitätsdaten für Ihren Adapter bereitstellen, aber die Konformitätsserver stellen keine doppelten Konformitätsdaten für mehrere Instanzen des Adapters bereit.

<div>

## <a name="implementing-the-icomplianceadapter-interface"></a>Implementieren der IComplianceAdapter-Schnittstelle

Die Schnittstelle ist in der Compliance.dll Assembly im Namespace definiert `Microsoft.Rtc.Internal.Chat.Server.Compliance` . Die Schnittstelle definiert zwei Methoden, die Ihr benutzerdefinierter Adapter implementieren muss.

    void SetConfig(AdapterConfig config)

Der beständige Chat-Kompatibilitätsserver ruft diese Methode auf, wenn der Adapter zuerst geladen wird. Die `AdapterConfig` Kompatibilitäts Konfiguration für beständigen Chat enthält, die für den Kompatibilitätsadapter relevant ist.

    void Translate(ConversationCollection conversations)

Der beständige Chat-Kompatibilitätsserver ruft diese Methode in regelmäßigen Intervallen auf, solange neue zu übersetzende Daten vorhanden sind. Dieses Zeitintervall entspricht dem `RunInterval` in der Compliance-Konfiguration für beständigen Chat angegebenen Satz.

Die `ConversationCollection` enthält die Konversations Informationen, die beim letzten Aufrufen dieser Methode erfasst wurden.

</div>

</div>

<span> </span>

</div>

</div>

</div>

