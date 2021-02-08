---
title: 'Lync Server 2013: DNS-Anforderungen für Standard Edition-Server'
description: 'Lync Server 2013: DNS-Anforderungen für Standard Edition-Server.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: DNS requirements for Standard Edition servers
ms:assetid: 3d6bbe65-e7ce-491b-a0bd-d2f7197f240d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425900(v=OCS.15)
ms:contentKeyID: 48183920
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: cc93549e07fb82304ad76b051730eab972530764
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393983"
---
# <a name="dns-requirements-for-standard-edition-servers-in-lync-server-2013"></a><span data-ttu-id="7ec51-103">DNS-Anforderungen für Standard -Edition-Server in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7ec51-103">DNS requirements for Standard Edition servers in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7ec51-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7ec51-104">

<span> </span></span></span>

<span data-ttu-id="7ec51-105">_**Zuletzt geändertes Thema:** 19.06.2012_</span><span class="sxs-lookup"><span data-stu-id="7ec51-105">_**Topic Last Modified:** 2012-06-19_</span></span>

<span data-ttu-id="7ec51-106">In diesem Abschnitt werden die DNS (Domain Name System)-Einträge beschrieben, die für die Bereitstellung von Standard -Edition-Servern erforderlich sind.</span><span class="sxs-lookup"><span data-stu-id="7ec51-106">This section describes the Domain Name System (DNS) records that are required for deployment of Standard Edition servers.</span></span>

<div>

## <a name="dns-records-for-standard-edition-servers"></a><span data-ttu-id="7ec51-107">DNS Records for Standard Edition Servers</span><span class="sxs-lookup"><span data-stu-id="7ec51-107">DNS Records for Standard Edition Servers</span></span>

<span data-ttu-id="7ec51-108">In der folgenden Tabelle sind die DNS-Anforderungen für die Serverbereitstellung von Lync Server 2013 Standard Edition aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="7ec51-108">The following table specifies DNS requirements for Lync Server 2013 Standard Edition server deployment.</span></span>

### <a name="dns-requirements-for-a-standard-edition-server"></a><span data-ttu-id="7ec51-109">DNS-Anforderungen für einen Standard Edition Server</span><span class="sxs-lookup"><span data-stu-id="7ec51-109">DNS Requirements for a Standard Edition Server</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="7ec51-110">Bereitstellungsszenario</span><span class="sxs-lookup"><span data-stu-id="7ec51-110">Deployment scenario</span></span></th>
<th><span data-ttu-id="7ec51-111">DNS-Anforderung</span><span class="sxs-lookup"><span data-stu-id="7ec51-111">DNS requirement</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="7ec51-112">Standard Edition-Server</span><span class="sxs-lookup"><span data-stu-id="7ec51-112">Standard Edition server</span></span></p></td>
<td><p><span data-ttu-id="7ec51-113">Ein interner A-Eintrag, mit dem der vollqualifizierte Domänenname (Fully Qualified Domain Name, FQDN) des Servers in die zugehörige IP-Adresse aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="7ec51-113">An internal A record that resolves the fully qualified domain name (FQDN) of the server to its IP address.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec51-114">Automatische Client anmeldung</span><span class="sxs-lookup"><span data-stu-id="7ec51-114">Automatic client sign-in</span></span></p></td>
<td><p><span data-ttu-id="7ec51-115">Für jede unterstützte SIP-Domäne: ein SRV-Eintrag für _sipinternaltls._tcp. &lt; domäne über Port 5061, der dem FQDN des Standard Edition-Servers, der Clientanforderungen für die Anmeldung authentifiziert und &gt; umleitigt, zu ordnet.</span><span class="sxs-lookup"><span data-stu-id="7ec51-115">For each supported SIP domain, an SRV record for _sipinternaltls._tcp.&lt;domain&gt; over port 5061 that maps to the FQDN of the Standard Edition server that authenticates and redirects client requests for sign-in.</span></span> <span data-ttu-id="7ec51-116">Details finden Sie unter <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">den DNS-Anforderungen für die automatische Client anmeldung bei Lync Server 2013.</a></span><span class="sxs-lookup"><span data-stu-id="7ec51-116">For details, see <a href="lync-server-2013-dns-requirements-for-automatic-client-sign-in.md">DNS requirements for automatic client sign-in in Lync Server 2013</a>.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="7ec51-117">Device Update Web Service Discovery by Unified Communications (UC)-Geräte</span><span class="sxs-lookup"><span data-stu-id="7ec51-117">Device Update Web service discovery by unified communications (UC) devices</span></span></p></td>
<td><p><span data-ttu-id="7ec51-118">Ein interner A-Datensatz mit dem Namen "ucupdates-r2". &lt; &gt; SIP-Domäne, die in die IP-Adresse des Serverupdatewebdiensts für das Hosten von Standard Edition aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="7ec51-118">An internal A record with the name ucupdates-r2.&lt;SIP domain&gt; that resolves to the IP address of the Standard Edition server hosting Device Update Web service.</span></span> <span data-ttu-id="7ec51-119">Wenn ein UC-Gerät aktiviert ist, sich ein Benutzer aber noch nie beim Gerät angemeldet hat, ermöglicht der A-Eintrag dem Gerät, den Serverhostingwebdienst für Geräteaktualisierungen zu ermitteln und Updates zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="7ec51-119">In the situation where a UC device is turned on, but a user has never logged into the device, the A record allows the device to discover the server hosting Device Update Web service and obtain updates.</span></span> <span data-ttu-id="7ec51-120">Andernfalls rufen Geräte die Serverinformationen über die In-Band-Bereitstellung ab, wenn sich der Benutzer das erste Mal anmeldet.</span><span class="sxs-lookup"><span data-stu-id="7ec51-120">Otherwise, devices obtain the server information though in-band provisioning the first time a user logs in.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="7ec51-121">Ein Reverseproxy zur Unterstützung von HTTP-Datenverkehr</span><span class="sxs-lookup"><span data-stu-id="7ec51-121">A reverse proxy to support HTTP traffic</span></span></p></td>
<td><p><span data-ttu-id="7ec51-122">Ein externer A-Eintrag, der den FQDN der externen Webfarm in die externe IP-Adresse des Reverseproxys aufhebt.</span><span class="sxs-lookup"><span data-stu-id="7ec51-122">An external A record that resolves the external web farm FQDN to the external IP address of the reverse proxy.</span></span> <span data-ttu-id="7ec51-123">Clients und UC-Geräte verwenden diesen Eintrag, um eine Verbindung mit dem Reverseproxy herzustellen.</span><span class="sxs-lookup"><span data-stu-id="7ec51-123">Clients and UC devices use this record to connect to the reverse proxy.</span></span> <span data-ttu-id="7ec51-124">Ausführliche Informationen finden Sie in der Dokumentation zur Planung unter "Ermitteln der DNS-Anforderungen für <a href="lync-server-2013-determine-dns-requirements.md">Lync Server 2013".</a></span><span class="sxs-lookup"><span data-stu-id="7ec51-124">For details, see <a href="lync-server-2013-determine-dns-requirements.md">Determine DNS requirements for Lync Server 2013</a> in the Planning documentation.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="7ec51-125">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7ec51-125">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

