---
title: 'Lync Server 2013: Unterstützte Serverkollokation für Edgekomponenten'
description: 'Lync Server 2013: unterstützte Server Zusammenstellung für Edge-Komponenten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Supported server collocation for edge components
ms:assetid: 435c4dd8-36af-4b71-9b88-3ffcf0fc5c65
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425934(v=OCS.15)
ms:contentKeyID: 48183978
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 7bf253e5210e077ca62b3d00f7f130d54d8392a5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49423638"
---
# <a name="supported-server-collocation-for-edge-components-in-lync-server-2013"></a>Unterstützte Serverkollokation für Edgekomponenten in Lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2012-09-08_

Der Zugriffs-Edgedienst, der Webkonferenz-Edgedienst, der A/V-Edgedienst und der XMPP-Proxy Dienst sind auf den Edgeserver verfügbar. Die folgenden Server stellen Funktionen bereit, die für den Zugriff durch externe Benutzer erforderlich sind, und müssen als dedizierte Server bereitgestellt werden:

  - Edgeserver

  - Director (optional)

  - Reverseproxy

<div>


> [!IMPORTANT]  
> Der Reverse-Proxy muss nicht nur für die Bereitstellung von lync Server 2013 dediziert sein. So können Sie beispielsweise Dienste bereitstellen, um die lync Server-Webdienste zu veröffentlichen, und gleichzeitig eine veröffentlichte Website für eine andere Website bereitstellen, die überhaupt keine Auswirkungen auf lync Server hat. Wenn Sie bereits über einen Reverse Proxy-Server im Umkreisnetzwerk verfügen, um andere Dienste zu unterstützen, können Sie ihn für lync Server 2013 verwenden.



</div>

</div>

<span> </span>

</div>

</div>

</div>

