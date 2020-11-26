---
title: 'Lync Server 2013: Bereitstellen des Zugriffs durch externe Benutzer'
description: 'Lync Server 2013: Bereitstellen des Zugriffs externer Benutzer.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Deploying external user access
ms:assetid: d40c9574-c16b-4fe6-b848-21ae0b7e4f0e
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398918(v=OCS.15)
ms:contentKeyID: 48185495
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: af41a169fe3a72e440e95cfa370a16117fb828a6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430007"
---
# <a name="deploying-external-user-access-in-lync-server-2013"></a><span data-ttu-id="7404f-103">Bereitstellen des Zugriffs durch externe Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7404f-103">Deploying external user access in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7404f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7404f-104">

<span> </span></span></span>

<span data-ttu-id="7404f-105">_**Letztes Änderungsdatum des Themas:** 2013-09-23_</span><span class="sxs-lookup"><span data-stu-id="7404f-105">_**Topic Last Modified:** 2013-09-23_</span></span>

<span data-ttu-id="7404f-106">Das Bereitstellen von Edge-Komponenten für Microsoft lync Server 2013 ermöglicht externen Benutzern, die nicht am internen Netzwerk Ihrer Organisation angemeldet sind, einschließlich authentifizierter und anonymer Remotebenutzer, Partner (einschließlich XMPP-Partnern), mobilen Clients und Benutzern von öffentlichen Instant Messaging-Diensten (im), um mit anderen Benutzern in Ihrer Organisation mithilfe von lync Server zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="7404f-106">Deploying edge components for Microsoft Lync Server 2013 makes it possible for external users who are not logged into your organization’s internal network, including authenticated and anonymous remote users, federated partners (including XMPP partners), mobile clients and users of public instant messaging (IM) services, to communicate with other users in your organization using Lync Server.</span></span> <span data-ttu-id="7404f-107">Die Bereitstellungs-und Konfigurationsprozesse für lync Server 2013 unterscheiden sich nicht wesentlich von lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="7404f-107">The deployment and configuration processes for Lync Server 2013 are not significantly different from Lync Server 2010.</span></span> <span data-ttu-id="7404f-108">Die Tools für die Installation und Verwaltung sind ähnlich wie in lync Server 2010.</span><span class="sxs-lookup"><span data-stu-id="7404f-108">The tools for installation and administration are much the same as in Lync Server 2010.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="7404f-109">Die &nbsp; Installation und Konfiguration von Microsoft lync Server 2013 Edge Server kann ein komplexer Prozess sein, der eine potenziell beträchtliche Planung und Koordination mit ihren internen Teams erfordert, einschließlich – aber nicht nur – Sicherheit, Netzwerk, Firewall, DNS (Domain Name System), Load Balancer und Public Key Infrastructure (PKI)-Überlegungen.</span><span class="sxs-lookup"><span data-stu-id="7404f-109">Microsoft Lync Server 2013&nbsp;Edge Server installation and configuration can be a complex process requiring a potentially significant amount of planning and coordination with your internal teams, including – but not limited to – security, networking, firewall, domain name system (DNS), load balancer, and public key infrastructure (PKI) considerations.</span></span> <span data-ttu-id="7404f-110">Es wird dringend empfohlen, den Planungsprozess und die Dokumentation zu überprüfen und zu verwenden, die vor der Bereitstellung Ihrer externen Access-Komponenten bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="7404f-110">It is strongly recommended that you review and use the planning process and documentation provided before deploying your external access components.</span></span> <span data-ttu-id="7404f-111">Auf diese Weise können Sie die Anzahl und Häufigkeit unerwünschter Änderungen und Probleme begrenzen, während Sie den Bereitstellungsprozess durchlaufen.</span><span class="sxs-lookup"><span data-stu-id="7404f-111">This will assist in limiting the number and frequency of undesired changes and problems as you proceed through the deployment process.</span></span> <span data-ttu-id="7404f-112">Informationen zum Planen des Zugriffs externer Benutzer finden Sie unter <A href="lync-server-2013-planning-for-external-user-access.md">Planen des Zugriffs externer Benutzer in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="7404f-112">For information on planning you external user access, see <A href="lync-server-2013-planning-for-external-user-access.md">Planning for external user access in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="in-this-section"></a><span data-ttu-id="7404f-113">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="7404f-113">In This Section</span></span>

  - [<span data-ttu-id="7404f-114">Prüfliste zur Bereitstellung für den Zugriff durch externe Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7404f-114">Deployment checklist for external user access in Lync Server 2013</span></span>](lync-server-2013-deployment-checklist-for-external-user-access.md)

  - [<span data-ttu-id="7404f-115">Systemanforderungen für Komponenten für den Zugriff durch externe Benutzer für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7404f-115">System requirements for external user access components for Lync Server 2013</span></span>](lync-server-2013-system-requirements-for-external-user-access-components.md)

  - [<span data-ttu-id="7404f-116">Vorbereiten der Installation von Servern im Umkreisnetzwerk für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7404f-116">Preparing for installation of servers in the perimeter network for Lync Server 2013</span></span>](lync-server-2013-preparing-for-installation-of-servers-in-the-perimeter-network.md)

  - [<span data-ttu-id="7404f-117">Erstellen einer Edge- und Director-Topologie in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7404f-117">Building an edge and Director topology in Lync Server 2013</span></span>](lync-server-2013-building-an-edge-and-director-topology.md)

  - <span data-ttu-id="7404f-118">[Einrichten des Directors in lync Server 2013](lync-server-2013-setting-up-the-director.md) (optional)</span><span class="sxs-lookup"><span data-stu-id="7404f-118">[Setting up the Director in Lync Server 2013](lync-server-2013-setting-up-the-director.md) (optional)</span></span>

  - [<span data-ttu-id="7404f-119">Einrichten von Edgeservern in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7404f-119">Setting up Edge Servers in Lync Server 2013</span></span>](lync-server-2013-setting-up-edge-servers.md)

  - [<span data-ttu-id="7404f-120">Einrichten von Reverseproxyservern für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7404f-120">Setting up reverse proxy servers for Lync Server 2013</span></span>](lync-server-2013-setting-up-reverse-proxy-servers.md)

  - [<span data-ttu-id="7404f-121">Konfigurieren der Unterstützung für den externen Benutzerzugriff in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7404f-121">Configuring support for external user access in Lync Server 2013</span></span>](lync-server-2013-configuring-support-for-external-user-access.md)

  - [<span data-ttu-id="7404f-122">Leitfaden für die Bereitstellung der Lync-Skype-Konnektivität in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7404f-122">Provisioning guide for Lync-Skype connectivity in Lync Server 2013</span></span>](lync-server-2013-provisioning-guide-for-lync-skype-connectivity.md)

  - [<span data-ttu-id="7404f-123">Konfigurieren von SIP-Partnerverbünden, XMPP-Partnerverbünden und öffentlichem Chat in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7404f-123">Configuring SIP federation, XMPP federation and public instant messaging in Lync Server 2013</span></span>](lync-server-2013-configuring-sip-federation-xmpp-federation-and-public-instant-messaging.md)

  - [<span data-ttu-id="7404f-124">Bereitstellen von Mobilität in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7404f-124">Deploying mobility in Lync Server 2013</span></span>](lync-server-2013-deploying-mobility.md)

  - [<span data-ttu-id="7404f-125">Überprüfen der Edgebereitstellung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7404f-125">Verifying your edge deployment in Lync Server 2013</span></span>](lync-server-2013-verifying-your-edge-deployment.md)

<span data-ttu-id="7404f-126"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7404f-126"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

