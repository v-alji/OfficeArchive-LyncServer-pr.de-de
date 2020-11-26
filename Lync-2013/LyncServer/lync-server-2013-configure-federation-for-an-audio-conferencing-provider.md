---
title: 'Lync Server 2013: Konfigurieren der Föderation für einen Audiokonferenz-Anbieter'
description: 'Lync Server 2013: Konfigurieren der Föderation für einen Audiokonferenz-Anbieter.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configure federation for an audio conferencing provider
ms:assetid: 08dedcce-0d3f-45da-8282-cf2634a41665
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn510996(v=OCS.15)
ms:contentKeyID: 60595883
ms.date: 07/24/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: c74654224c42618768d881a95031d58be4d55df5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434053"
---
# <a name="configure-federation-for-an-audio-conferencing-provider-in-lync-server-2013"></a>Konfigurieren des Verbunds für einen Audiokonferenz-Anbieter in lync Server 2013

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody">

<span> </span>

_**Letztes Änderungsdatum des Themas:** 2014-07-24_

Wenn Sie einen Audiokonferenz-Anbieter (ACP) in ihrer hybridbereitstellung (lync Server lokal mit lync Online) verwenden möchten, müssen Sie den Verbund zwischen Ihrer lokalen lync-Bereitstellung und dem AKP-Partner als zugelassenen Partner Server konfigurieren. Sie können den Verbund konfigurieren, indem Sie die AKP-Partnerdomäne und den Edgeserver (Dies kann auch als Zugriffs Proxy bezeichnet werden) zur Liste der Föderationsdomänen für Ihre lokale Bereitstellung hinzufügen. Ihr AKP-Partner muss dann den FQDN Ihres lokalen Edge-Server Pools in die Liste der zulässigen Föderationsdomänen aufnehmen. Wenden Sie sich an ihren AKP-Anbieter für zusätzlichen detailsYour ACP-Partner muss dann den FQDN Ihres lokalen Edge-Server Pools in die Liste der zulässigen Föderationsdomänen aufnehmen.

  - **Hinzufügen der ACP-Domäne und des Edgeservers als zugelassene Partnerverbunddomäne**
    
    Wenn Sie die ACP-Domäne als zugelassenen Partner Server (zugelassene Verbunddomäne) hinzufügen möchten, führen Sie die Schritte unter [Konfigurieren der Unterstützung für zugelassene externe Domänen in lync Server 2013](lync-server-2013-configure-support-for-allowed-external-domains.md)aus. Fügen Sie für den Edgeserver den FQDN des Edgeservers des ACP-Partners hinzu. Sie müssen sich möglicherweise an Ihren ACP-Partner wenden, um den FQDN für seinen Edgeserver zu erhalten, der von Ihrem ACP möglicherweise auch als Zugriffsproxy bezeichnet wird.

  - **Bereitstellen des FQDN Ihres Edgeserverpools für den ACP-Partner**
    
    Der ACP-Partner muss einen Partnerverbund konfigurieren, um Ihre lokale Domäne als einen zulässigen Partnerserver hinzuzufügen, indem der FQDN Ihres Edgeserverpools als eine zugelassene Partnerverbunddomäne hinzugefügt wird.

</div>

<span> </span>

</div>

</div>

</div>

