---
title: 'Lync Server 2013: Bereitstellen der Remoteanrufsteuerung'
description: 'Lync Server 2013: Bereitstellen der Remoteanrufsteuerung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying remote call control
ms:assetid: 763037f7-7a2a-49ae-acc3-9781b0bff7e0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg558664(v=OCS.15)
ms:contentKeyID: 48184536
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4cc5e79f3ee44c354baf435585d304574d6a980c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429783"
---
# <a name="deploying-remote-call-control-in-lync-server-2013"></a><span data-ttu-id="09849-103">Bereitstellen der Remoteanrufsteuerung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09849-103">Deploying remote call control in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="09849-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="09849-104">

<span> </span></span></span>

<span data-ttu-id="09849-105">_**Letztes Änderungsdatum des Themas:** 2012-10-20_</span><span class="sxs-lookup"><span data-stu-id="09849-105">_**Topic Last Modified:** 2012-10-20_</span></span>

<span data-ttu-id="09849-106">Dieser Abschnitt führt Sie durch den Prozess der Bereitstellung von Funktionen für die Remoteanrufsteuerung für Benutzer in Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="09849-106">This section guides you through the process of deploying remote call control functionality to users in your organization.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="09849-107">Obwohl Remote-Anrufsteuerungsfeatures für Remotebenutzer verfügbar sind, während Sie sich außerhalb der Firewall Ihrer Organisation befinden, gehen Details zum Bereitstellen von externen Zugriffsszenarien nicht in diesen Dokumentationsbereich ein.</span><span class="sxs-lookup"><span data-stu-id="09849-107">Although remote call control features are available to remote users while they are outside of your organization’s firewall, details about deploying external access scenarios are beyond the scope of this documentation.</span></span> <span data-ttu-id="09849-108">Details zum Bereitstellen des Zugriffs externer Benutzer finden Sie unter <A href="lync-server-2013-deploying-external-user-access.md">Bereitstellen des Zugriffs auf externe Benutzer in lync Server 2013</A> in der Bereitstellungsdokumentation.</span><span class="sxs-lookup"><span data-stu-id="09849-108">For details about deploying external user access, see <A href="lync-server-2013-deploying-external-user-access.md">Deploying external user access in Lync Server 2013</A> in the Deployment documentation.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="09849-109">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="09849-109">In This Section</span></span>

  - [<span data-ttu-id="09849-110">Konfigurieren von Lync Server 2013 für das Routing an ein SIP/CSTA-Gateway</span><span class="sxs-lookup"><span data-stu-id="09849-110">Configuring Lync Server 2013 to route to a SIP/CSTA gateway</span></span>](lync-server-2013-configuring-lync-server-to-route-to-a-sip-csta-gateway.md)

  - [<span data-ttu-id="09849-111">Konfigurieren einer statischen Route für die Remoteanrufsteuerung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09849-111">Configure a static route for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-static-route-for-remote-call-control.md)

  - [<span data-ttu-id="09849-112">Konfigurieren eines Eintrags einer vertrauenswürdigen Anwendung für die Remoteanrufsteuerung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09849-112">Configure a trusted application entry for remote call control in Lync Server 2013</span></span>](lync-server-2013-configure-a-trusted-application-entry-for-remote-call-control.md)

  - <span data-ttu-id="09849-113">[Definieren einer SIP/CSTA-Gateway-IP-Adresse in lync Server 2013](lync-server-2013-define-a-sip-csta-gateway-ip-address.md) (nur, wenn das Gateway für die Verwendung von TCP konfiguriert ist)</span><span class="sxs-lookup"><span data-stu-id="09849-113">[Define a SIP/CSTA gateway IP address in Lync Server 2013](lync-server-2013-define-a-sip-csta-gateway-ip-address.md) (only if the gateway is configured to use TCP)</span></span>

  - [<span data-ttu-id="09849-114">Aktivieren von Lync-Benutzern für die Remoteanrufsteuerung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09849-114">Enable Lync users for remote call control in Lync Server 2013</span></span>](lync-server-2013-enable-lync-users-for-remote-call-control.md)

  - [<span data-ttu-id="09849-115">Remoteanrufsteuerung und Normalisieren von Rufnummern in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09849-115">Remote call control and phone number normalization in Lync Server 2013</span></span>](lync-server-2013-remote-call-control-and-phone-number-normalization.md)

  - <span data-ttu-id="09849-116">[Entfernen eines autorisierten Legacyhosts in lync Server 2013 (optional)](lync-server-2013-remove-a-legacy-authorized-host-optional.md) (nur, wenn Sie Benutzer migrieren, die zuvor für die Remoteanrufsteuerung aktiviert wurden)</span><span class="sxs-lookup"><span data-stu-id="09849-116">[Remove a legacy authorized host in Lync Server 2013 (optional)](lync-server-2013-remove-a-legacy-authorized-host-optional.md) (only if you are migrating users previously enabled for remote call control)</span></span>

</div>

<div>

## <a name="related-sections"></a><span data-ttu-id="09849-117">Verwandte Abschnitte</span><span class="sxs-lookup"><span data-stu-id="09849-117">Related Sections</span></span>

[<span data-ttu-id="09849-118">Planen der Remoteanrufsteuerung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="09849-118">Planning for remote call control in Lync Server 2013</span></span>](lync-server-2013-planning-for-remote-call-control.md)

<span data-ttu-id="09849-119"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="09849-119"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

