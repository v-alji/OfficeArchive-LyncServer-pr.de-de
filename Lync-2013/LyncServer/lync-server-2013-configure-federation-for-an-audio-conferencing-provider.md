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
# <a name="configure-federation-for-an-audio-conferencing-provider-in-lync-server-2013"></a><span data-ttu-id="f97dd-103">Konfigurieren des Verbunds für einen Audiokonferenz-Anbieter in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="f97dd-103">Configure federation for an audio conferencing provider in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="f97dd-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="f97dd-104">

<span> </span></span></span>

<span data-ttu-id="f97dd-105">_**Letztes Änderungsdatum des Themas:** 2014-07-24_</span><span class="sxs-lookup"><span data-stu-id="f97dd-105">_**Topic Last Modified:** 2014-07-24_</span></span>

<span data-ttu-id="f97dd-106">Wenn Sie einen Audiokonferenz-Anbieter (ACP) in ihrer hybridbereitstellung (lync Server lokal mit lync Online) verwenden möchten, müssen Sie den Verbund zwischen Ihrer lokalen lync-Bereitstellung und dem AKP-Partner als zugelassenen Partner Server konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="f97dd-106">If you want to use an Audio Conferencing Provider (ACP) in your hybrid deployment (Lync Server on-premises with Lync Online), you need to configure federation between your on-premises Lync deployment and the ACP partner as an Allowed Partner Server.</span></span> <span data-ttu-id="f97dd-107">Sie können den Verbund konfigurieren, indem Sie die AKP-Partnerdomäne und den Edgeserver (Dies kann auch als Zugriffs Proxy bezeichnet werden) zur Liste der Föderationsdomänen für Ihre lokale Bereitstellung hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="f97dd-107">You can configure federation by adding the ACP partner domain and Edge server (this may also be called the Access Proxy) to the Federated Domains list for your on-premises deployment.</span></span> <span data-ttu-id="f97dd-108">Ihr AKP-Partner muss dann den FQDN Ihres lokalen Edge-Server Pools in die Liste der zulässigen Föderationsdomänen aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="f97dd-108">Your ACP partner then needs to add the FQDN of your on-premises Edge Server pool to their allowed federated domains list.</span></span> <span data-ttu-id="f97dd-109">Wenden Sie sich an ihren AKP-Anbieter für zusätzlichen detailsYour ACP-Partner muss dann den FQDN Ihres lokalen Edge-Server Pools in die Liste der zulässigen Föderationsdomänen aufnehmen.</span><span class="sxs-lookup"><span data-stu-id="f97dd-109">Contact your ACP provider for additional detailsYour ACP partner then needs to add the FQDN of your on-premises Edge Server pool to their allowed federated domains list.</span></span>

  - <span data-ttu-id="f97dd-110">**Hinzufügen der ACP-Domäne und des Edgeservers als zugelassene Partnerverbunddomäne**</span><span class="sxs-lookup"><span data-stu-id="f97dd-110">**Adding the ACP Domain and Edge Server as an Allowed Federated Domain**</span></span>
    
    <span data-ttu-id="f97dd-111">Wenn Sie die ACP-Domäne als zugelassenen Partner Server (zugelassene Verbunddomäne) hinzufügen möchten, führen Sie die Schritte unter [Konfigurieren der Unterstützung für zugelassene externe Domänen in lync Server 2013](lync-server-2013-configure-support-for-allowed-external-domains.md)aus.</span><span class="sxs-lookup"><span data-stu-id="f97dd-111">To add the ACP domain as an Allowed Partner Server (allowed Federated Domain), follow the steps in [Configure support for allowed external domains in Lync Server 2013](lync-server-2013-configure-support-for-allowed-external-domains.md).</span></span> <span data-ttu-id="f97dd-112">Fügen Sie für den Edgeserver den FQDN des Edgeservers des ACP-Partners hinzu.</span><span class="sxs-lookup"><span data-stu-id="f97dd-112">For the Edge Server, add the FQDN of the ACP partner’s Edge Server.</span></span> <span data-ttu-id="f97dd-113">Sie müssen sich möglicherweise an Ihren ACP-Partner wenden, um den FQDN für seinen Edgeserver zu erhalten, der von Ihrem ACP möglicherweise auch als Zugriffsproxy bezeichnet wird.</span><span class="sxs-lookup"><span data-stu-id="f97dd-113">You may need to contact your ACP partner to obtain the FQDN for their Edge Server, which may also be referred to by your ACP as their Access Proxy.</span></span>

  - <span data-ttu-id="f97dd-114">**Bereitstellen des FQDN Ihres Edgeserverpools für den ACP-Partner**</span><span class="sxs-lookup"><span data-stu-id="f97dd-114">**Provide the FQDN of your Edge Server Pool to the ACP partner**</span></span>
    
    <span data-ttu-id="f97dd-115">Der ACP-Partner muss einen Partnerverbund konfigurieren, um Ihre lokale Domäne als einen zulässigen Partnerserver hinzuzufügen, indem der FQDN Ihres Edgeserverpools als eine zugelassene Partnerverbunddomäne hinzugefügt wird.</span><span class="sxs-lookup"><span data-stu-id="f97dd-115">The ACP partner needs to configure federation to add your on-premises domain as an Allowed Partner Server by adding the FQDN of your Edge Server pool as an allowed Federated domain.</span></span>

<span data-ttu-id="f97dd-116"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="f97dd-116"></div>

<span> </span>

</div>

</div>

</span></span></div>

