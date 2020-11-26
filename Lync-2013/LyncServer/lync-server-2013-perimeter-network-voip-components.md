---
title: 'Lync Server 2013: VoIP-Komponenten für das Umkreisnetzwerk'
description: 'Lync Server 2013: Umkreisnetzwerk VoIP-Komponenten.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Perimeter network VoIP components
ms:assetid: 74230008-695d-436a-90b9-9cd060c70f7b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398559(v=OCS.15)
ms:contentKeyID: 48184514
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 20a416838b2ccec969e2990d492029486b6f2c72
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49437140"
---
# <a name="perimeter-network-voip-components-for-lync-server-2013"></a><span data-ttu-id="5f34a-103">VoIP-Komponenten für das Umkreisnetzwerk für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="5f34a-103">Perimeter network VoIP components for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="5f34a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="5f34a-104">

<span> </span></span></span>

<span data-ttu-id="5f34a-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="5f34a-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="5f34a-106">Externe Anrufer, die Unified Communications-Clients für Einzel-oder Konferenzgespräche verwenden, setzen auf Edge-Server für die Sprachkommunikation mit Kollegen.</span><span class="sxs-lookup"><span data-stu-id="5f34a-106">Outside callers who use unified communications clients for individual or conference calls rely on Edge Server for voice communication with coworkers.</span></span>

<span data-ttu-id="5f34a-107">Auf einem Edgeserver bietet der Access Edge-Dienst SIP-Signale für Anrufe von lync-Benutzern, die sich außerhalb der Firewall Ihrer Organisation befinden.</span><span class="sxs-lookup"><span data-stu-id="5f34a-107">On an Edge Server, the Access Edge service provides SIP signaling for calls from Lync users who are outside your organization’s firewall.</span></span> <span data-ttu-id="5f34a-108">Der A/V-Edgedienst ermöglicht es Medien, Firewalls und NAT zu passieren.</span><span class="sxs-lookup"><span data-stu-id="5f34a-108">The A/V Edge service enables media traversal of NAT and firewalls.</span></span> <span data-ttu-id="5f34a-109">Anrufer, die einen Unified Communications-Client (UC) außerhalb der Unternehmensfirewall verwenden, benötigen den A/V-Edgedienst für Einzelgespräche und Telefonkonferenzen.</span><span class="sxs-lookup"><span data-stu-id="5f34a-109">A caller who uses a unified communications (UC) client from outside the corporate firewall relies on the A/V Edge service for both individual and conference calls.</span></span>

<span data-ttu-id="5f34a-p102">Der A/V-Authentifizierungsdienst ist mit dem A/V-Edgedienst verknüpft und stellt Authentifizierungsdienste für diesen bereit. Externe Benutzer, die versuchen, eine Verbindung mit dem A/V-Edgedienst herzustellen, benötigen ein vom A/V-Authentifizierungsdienst bereitgestelltes Authentifizierungstoken, damit ihre Anrufe durchgestellt werden können.</span><span class="sxs-lookup"><span data-stu-id="5f34a-p102">The A/V Authentication service is collocated with, and provides authentication services for, the A/V Edge service. Outside users who attempt to connect to the A/V Edge service require an authentication token that is provided by the A/V Authentication Service before their calls can go through.</span></span>

<span data-ttu-id="5f34a-112"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="5f34a-112"></div>

<span> </span>

</div>

</div>

</span></span></div>

