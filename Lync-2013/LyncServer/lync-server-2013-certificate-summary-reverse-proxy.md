---
title: 'Lync Server 2013: Zertifikatzusammenfassung für Reverseproxy'
description: 'Lync Server 2013: Zertifikatzusammenfassung – Reverse-Proxy.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Certificate summary - Reverse proxy
ms:assetid: f2b9a53f-aead-413d-81e9-4a294a010fbb
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ205381(v=OCS.15)
ms:contentKeyID: 48185820
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0cc250d6de2eb1a0b6c3ad3495c8df62942f9a81
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49435281"
---
# <a name="certificate-summary---reverse-proxy-in-lync-server-2013"></a><span data-ttu-id="3e95c-103">Zertifikatzusammenfassung für Reverseproxy in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="3e95c-103">Certificate summary - Reverse proxy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="3e95c-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="3e95c-104">

<span> </span></span></span>

<span data-ttu-id="3e95c-105">_**Letztes Änderungsdatum des Themas:** 2012-11-14_</span><span class="sxs-lookup"><span data-stu-id="3e95c-105">_**Topic Last Modified:** 2012-11-14_</span></span>

<span data-ttu-id="3e95c-106">Die Zertifikatanforderungen für den Reverse-Proxy sind viel einfacher als die für die Edgeserver.</span><span class="sxs-lookup"><span data-stu-id="3e95c-106">Certificate requirements for the reverse proxy are much simpler than that for the Edge Servers.</span></span> <span data-ttu-id="3e95c-107">Das bereitgestellte Flussdiagramm stellt die erforderlichen Anforderungen dar.</span><span class="sxs-lookup"><span data-stu-id="3e95c-107">The provided flowchart presents the requirements necessary.</span></span> <span data-ttu-id="3e95c-108">In der zugehörigen Tabelle werden typische Namen für Zertifikats Subjekte und andere Alternative Namen in Bezug auf die Szenarien vorgestellt, die in den Edge-Server-Diskussionen besprochen wurden.</span><span class="sxs-lookup"><span data-stu-id="3e95c-108">The accompanying table presents typical certificate subject name and subject alternative names in relation to the scenarios that we have been reviewed in the Edge Server discussions.</span></span> <span data-ttu-id="3e95c-109">Weitere Informationen zu den Edge-Server-Szenarien finden Sie unter [Szenarien für den Zugriff durch externe Benutzer in lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span><span class="sxs-lookup"><span data-stu-id="3e95c-109">For more details on the Edge Server scenarios, see [Scenarios for external user access in Lync Server 2013](lync-server-2013-scenarios-for-external-user-access.md).</span></span>

<span data-ttu-id="3e95c-110">**Flussdiagramm für Zertifikate für den Reverse-Proxy**</span><span class="sxs-lookup"><span data-stu-id="3e95c-110">**Certificates Flow Chart for Reverse Proxy**</span></span>

<span data-ttu-id="3e95c-111">![Flussdiagramm für Zertifikate für Edgeserver](images/JJ205381.026045d7-1b4b-4651-b32f-2d43a7161198(OCS.15).jpg "Flussdiagramm für Zertifikate für Edgeserver")</span><span class="sxs-lookup"><span data-stu-id="3e95c-111">![Certificates Flow Chart for Edge Server](images/JJ205381.026045d7-1b4b-4651-b32f-2d43a7161198(OCS.15).jpg "Certificates Flow Chart for Edge Server")</span></span>

### <a name="reverse-proxy-external-interface"></a><span data-ttu-id="3e95c-112">Reverse Proxy: externe Schnittstelle</span><span class="sxs-lookup"><span data-stu-id="3e95c-112">Reverse Proxy: External Interface</span></span>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="3e95c-113">Komponente</span><span class="sxs-lookup"><span data-stu-id="3e95c-113">Component</span></span></th>
<th><span data-ttu-id="3e95c-114">Name des Antragstellers</span><span class="sxs-lookup"><span data-stu-id="3e95c-114">Subject name</span></span></th>
<th><span data-ttu-id="3e95c-115">Subject Alternative Name (San)/Order</span><span class="sxs-lookup"><span data-stu-id="3e95c-115">Subject alternative name (SAN)/Order</span></span></th>
<th><span data-ttu-id="3e95c-116">Kommentare</span><span class="sxs-lookup"><span data-stu-id="3e95c-116">Comments</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="3e95c-117">Reverseproxy</span><span class="sxs-lookup"><span data-stu-id="3e95c-117">Reverse Proxy</span></span></p></td>
<td><p><span data-ttu-id="3e95c-118">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3e95c-118">webext.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3e95c-119">webext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3e95c-119">webext.contoso.com</span></span></p>
<p><span data-ttu-id="3e95c-120">webdirext.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3e95c-120">webdirext.contoso.com</span></span></p>
<p><span data-ttu-id="3e95c-121">dialin.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3e95c-121">dialin.contoso.com</span></span></p>
<p><span data-ttu-id="3e95c-122">meet.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3e95c-122">meet.contoso.com</span></span></p>
<p><span data-ttu-id="3e95c-123">officewebapps01.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3e95c-123">officewebapps01.contoso.com</span></span></p>
<p><span data-ttu-id="3e95c-124">lyncdiscover.contoso.com</span><span class="sxs-lookup"><span data-stu-id="3e95c-124">lyncdiscover.contoso.com</span></span></p>
<p><span data-ttu-id="3e95c-125">(Optional):\*. contoso.com</span><span class="sxs-lookup"><span data-stu-id="3e95c-125">(Optional):\*.contoso.com</span></span></p></td>
<td><p><span data-ttu-id="3e95c-126">Das Zertifikat muss von einer öffentlichen Zertifizierungsstelle und mit der Server-EKU ausgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="3e95c-126">Certificate must be issued by a public CA and with the server EKU.</span></span> <span data-ttu-id="3e95c-127">Zu den Diensten gehören der Adressbuchdienst, die Expansion der Verteilergruppe in Office Web Apps für Konferenzen und die Veröffentlichungsregeln für lync-IP-Geräte.</span><span class="sxs-lookup"><span data-stu-id="3e95c-127">Services include Address Book Service, distribution group expansion Office Web Apps for conferencing, and Lync IP Device publishing rules.</span></span> <span data-ttu-id="3e95c-128">Der Alternative Antragstellername umfasst:</span><span class="sxs-lookup"><span data-stu-id="3e95c-128">Subject alternative name includes:</span></span></p>
<ul>
<li><p><span data-ttu-id="3e95c-129">FQDN für externe Webdienste für Front-End-Server oder Front-End-Pool</span><span class="sxs-lookup"><span data-stu-id="3e95c-129">External Web Services FQDN for Front End Server or Front End pool</span></span></p></li>
<li><p><span data-ttu-id="3e95c-130">FQDN des externen Webdiensts für Director oder Director-Pool</span><span class="sxs-lookup"><span data-stu-id="3e95c-130">External Web Services FQDN for Director or Director pool</span></span></p></li>
<li><p><span data-ttu-id="3e95c-131">Einwahlkonferenzen</span><span class="sxs-lookup"><span data-stu-id="3e95c-131">Dial-in conferencing</span></span></p></li>
<li><p><span data-ttu-id="3e95c-132">Veröffentlichungsregel für Online Besprechungen</span><span class="sxs-lookup"><span data-stu-id="3e95c-132">Online meeting publishing rule</span></span></p></li>
<li><p><span data-ttu-id="3e95c-133">Office Web Apps für Konferenzen</span><span class="sxs-lookup"><span data-stu-id="3e95c-133">Office Web Apps for conferencing</span></span></p></li>
<li><p><span data-ttu-id="3e95c-134">Lyncdiscover (AutoErmittlung)</span><span class="sxs-lookup"><span data-stu-id="3e95c-134">Lyncdiscover (Autodiscover)</span></span></p></li>
</ul>
<p><span data-ttu-id="3e95c-135">Der optionale Platzhalter ersetzt sowohl Meet als auch Dialin San</span><span class="sxs-lookup"><span data-stu-id="3e95c-135">The optional wildcard replaces both meet and dialin SAN</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="3e95c-136">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="3e95c-136">


</div>

<span> </span>

</div>

</div>

</span></span></div>

