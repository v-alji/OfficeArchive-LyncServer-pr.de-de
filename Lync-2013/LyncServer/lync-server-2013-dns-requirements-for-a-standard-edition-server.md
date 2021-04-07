---
title: 'Lync Server 2013: DNS-Anforderungen für einen Standard Edition-Server'
description: 'Lync Server 2013: DNS-Anforderungen für einen Standard Edition-Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for a Standard Edition server
ms:assetid: 5d1daf54-6e60-4ce0-9254-7d57a0835fa4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204936(v=OCS.15)
ms:contentKeyID: 48184259
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea0c7219563d62a9d99bd85655b3d3fcb0c551f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49395027"
---
# <a name="dns-requirements-for-a-standard-edition-server-in-lync-server-2013"></a><span data-ttu-id="8f2b6-103">DNS-Anforderungen für einen Standard Edition-Server in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8f2b6-103">DNS requirements for a Standard Edition server in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="8f2b6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="8f2b6-104">

<span> </span></span></span>

<span data-ttu-id="8f2b6-105">_**Thema Zuletzt geändert:** 22.02.2013_</span><span class="sxs-lookup"><span data-stu-id="8f2b6-105">_**Topic Last Modified:** 2013-02-22_</span></span>

<span data-ttu-id="8f2b6-106">In diesem Abschnitt werden die DNS-Einträge (Domain Name System) beschrieben, die für die Bereitstellung von Standard Edition-Servern erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-106">This section describes the Domain Name System (DNS) records that are required for deployment of Standard Edition servers.</span></span>

<div>

## <a name="dns-records-for-standard-edition-servers"></a><span data-ttu-id="8f2b6-107">DNS Records für Standard Edition Servers</span><span class="sxs-lookup"><span data-stu-id="8f2b6-107">DNS Records for Standard Edition Servers</span></span>

<span data-ttu-id="8f2b6-108">In der folgenden Tabelle sind die DNS-Anforderungen für die Serverbereitstellung von Lync Server 2013 Standard Edition angegeben.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-108">The following table specifies DNS requirements for Lync Server 2013 Standard Edition server deployment.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="8f2b6-109">Bereitstellungsszenario</span><span class="sxs-lookup"><span data-stu-id="8f2b6-109">Deployment scenario</span></span></th>
<th><span data-ttu-id="8f2b6-110">DNS-Anforderung</span><span class="sxs-lookup"><span data-stu-id="8f2b6-110">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="8f2b6-111">Standard Edition-Server</span><span class="sxs-lookup"><span data-stu-id="8f2b6-111">Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="8f2b6-112">Ein interner A-Eintrag, mit dem der vollqualifizierte Domänenname (Fully Qualified Domain Name, FQDN) des Servers in die zugehörige IP-Adresse aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-112">An internal A record that resolves the fully qualified domain name (FQDN) of the server to its IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f2b6-113">Automatische Client-Anmeldung</span><span class="sxs-lookup"><span data-stu-id="8f2b6-113">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="8f2b6-114">Für jede unterstützte SIP-Domäne einen SRV-Eintrag für _sipinternaltls._tcp. &lt; Domäne über Port 5061, der dem FQDN des Standard Edition-Servers zu ordnet, der Clientanforderungen zur Anmeldung authentifiziert und &gt; umleitt.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-114">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Standard Edition server that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="8f2b6-115">Details finden Sie unter <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS-Anforderungen für die automatische Client-Anmeldung in Lync Server 2013.</a></span><span class="sxs-lookup"><span data-stu-id="8f2b6-115">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="8f2b6-116">Device Update Web Service Discovery by Unified Communications (UC)-Geräte</span><span class="sxs-lookup"><span data-stu-id="8f2b6-116">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="8f2b6-117">Ein interner A-Eintrag mit dem Namen ucupdates-r2. &lt; &gt; SIP-Domäne, die auf die IP-Adresse des Standard Edition-Serverhosting-Geräteupdatewebdiensts aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-117">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Standard Edition server hosting Device Update Web service.</span></span> <span data-ttu-id="8f2b6-118">In der Situation, in der ein UC-Gerät aktiviert ist, sich ein Benutzer aber noch nie beim Gerät angemeldet hat, ermöglicht der A-Eintrag dem Gerät, den Serverhosting-Geräteupdatewebdienst zu ermitteln und Updates zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-118">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the server hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="8f2b6-119">Andernfalls rufen Geräte die Serverinformationen über die In-Band-Bereitstellung ab, wenn sich der Benutzer das erste Mal anmeldet.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-119">Otherwise, devices obtain the server information though in-band provisioning the first time a user logs in.</span></span> <span data-ttu-id="8f2b6-120">Ausführliche Informationen finden Sie unter <a href="lync-server-2013-device-update-web-service.md">Geräteupdatewebdienst in Lync Server 2013</a> in der Dokumentation "Vorgänge".</span><span class="sxs-lookup"><span data-stu-id="8f2b6-120">For details, see <a href="lync-server-2013-device-update-web-service.md">Device Update Web service in Lync Server 2013</a> in the Operations documentation.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="8f2b6-121">Ein Reverseproxy zur Unterstützung von HTTP-Datenverkehr</span><span class="sxs-lookup"><span data-stu-id="8f2b6-121">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="8f2b6-122">Ein externer A-Eintrag, der den FQDN der externen Webfarm in die externe IP-Adresse des Reverseproxys aufhebt.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-122">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="8f2b6-123">Clients und UC-Geräte verwenden diesen Eintrag, um eine Verbindung mit dem Reverseproxy herzustellen.</span><span class="sxs-lookup"><span data-stu-id="8f2b6-123">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="8f2b6-124">Ausführliche Informationen finden Sie <a href="lync-server-2013-determine-dns-requirements.md">unter Ermitteln der DNS-Anforderungen für Lync Server 2013</a> in der Dokumentation "Planung".</span><span class="sxs-lookup"><span data-stu-id="8f2b6-124">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="see-also"></a><span data-ttu-id="8f2b6-125">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8f2b6-125">See Also</span></span>


[<span data-ttu-id="8f2b6-126">DNS-Anforderungen für die automatische Client-Anmeldung in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8f2b6-126">DNS requirements for automatic client sign-in in Lync Server 2013</span></span>](lync-server-2013-dns-requirements-for-automatic-client-sign-in.md)  
[<span data-ttu-id="8f2b6-127">Ermitteln von DNS-Anforderungen für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8f2b6-127">Determine DNS requirements for Lync Server 2013</span></span>](lync-server-2013-determine-dns-requirements.md)  


[<span data-ttu-id="8f2b6-128">Geräteaktualisierungs-Webdienst in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="8f2b6-128">Device Update Web service in Lync Server 2013</span></span>](lync-server-2013-device-update-web-service.md)  
  

<span data-ttu-id="8f2b6-129"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="8f2b6-129"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

