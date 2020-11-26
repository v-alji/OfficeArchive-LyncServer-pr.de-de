---
title: 'Lync Server 2013: Planen des VoIP-Routings für ausgehende Anrufe'
description: 'Lync Server 2013: Planen des ausgehenden VoIP-Routings'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Planning outbound voice routing
ms:assetid: 37c55fa4-175a-4190-b9e4-c2e5ac7b9261
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg425853(v=OCS.15)
ms:contentKeyID: 48183835
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 057f81b995e231c2025a9fcb07e675086a662efe
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49442852"
---
# <a name="planning-outbound-voice-routing-in-lync-server-2013"></a><span data-ttu-id="289e5-103">Planen des VoIP-Routings für ausgehende Anrufe in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="289e5-103">Planning outbound voice routing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="289e5-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="289e5-104">

<span> </span></span></span>

<span data-ttu-id="289e5-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="289e5-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="289e5-106">Das Routing für ausgehende Anrufe bezieht sich auf Anrufe, die für ein öffentliches Switched Telephone Network (PSTN) Gateway, trunk oder Private Branch Exchange (PBX) bestimmt sind.</span><span class="sxs-lookup"><span data-stu-id="289e5-106">Outbound call routing applies to calls that are destined for a public switched telephone network (PSTN) gateway, trunk, or private branch exchange (PBX).</span></span> <span data-ttu-id="289e5-107">Wenn ein Benutzer einen Anruf eingibt, normalisiert der Server die Telefonnummer bei Bedarf in das E. 164-Format und versucht, ihn mit einem SIP-URI zu vergleichen.</span><span class="sxs-lookup"><span data-stu-id="289e5-107">When a user places a call, the server normalizes the phone number to E.164 format, if necessary, and attempts to match it to a SIP URI.</span></span> <span data-ttu-id="289e5-108">Ermittelt der Server keine Übereinstimmung, wird die Routinglogik für ausgehende Anrufe basierend auf der bereitgestellten Wählzeichenfolge angewendet.</span><span class="sxs-lookup"><span data-stu-id="289e5-108">If the server cannot make the match, it applies outbound call routing logic based on the supplied dial string.</span></span> <span data-ttu-id="289e5-109">Sie können diese Logik durch Konfigurieren der Servereinstellungen definieren, die in der folgenden Tabelle beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="289e5-109">You define that logic by configuring the server settings that are described in the following table.</span></span>

### <a name="lync-server-outbound-call-routing-settings"></a><span data-ttu-id="289e5-110">Ausgehende Anruf Routing Einstellungen für lync Server</span><span class="sxs-lookup"><span data-stu-id="289e5-110">Lync Server Outbound Call Routing Settings</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="289e5-111">Objekt</span><span class="sxs-lookup"><span data-stu-id="289e5-111">Object</span></span></th>
<th><span data-ttu-id="289e5-112">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="289e5-112">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="289e5-113">Wählplan</span><span class="sxs-lookup"><span data-stu-id="289e5-113">Dial Plan</span></span></p></td>
<td><p><span data-ttu-id="289e5-114">Ein Wählplan ist ein benannter Satz von Normalisierungsregeln, mit deren Hilfe Telefonnummern als Bestandteil der Telefonautorisierung und Anrufweiterleitung für einen benannten Standort, für einzelne Benutzer oder für Kontaktobjekte in ein einzelnes Standardformat (E.164) übersetzt werden.</span><span class="sxs-lookup"><span data-stu-id="289e5-114">A dial plan is a named set of normalization rules that translates phone numbers for a named location, individual user, or contact object into a single standard (E.164) format for purposes of phone authorization and call routing.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289e5-115">Normalisierungsregel</span><span class="sxs-lookup"><span data-stu-id="289e5-115">Normalization rule</span></span></p></td>
<td><p><span data-ttu-id="289e5-p102">Normalisierungsregeln definieren das Routing von Rufnummern in unterschiedlichen Formaten für benannte Standorte, Benutzer oder Kontaktobjekte. Ein und dieselbe Wählzeichenfolge kann je nach dem Standort, an dem sie gewählt wurde, und je nach der anrufenden Person bzw. dem anrufenden Kontaktobjekt unterschiedlich interpretiert und übersetzt werden. Eine Gruppe von Normalisierungsregeln, die einem bestimmten Standort zugeordnet sind, bildet einen Wählplan.</span><span class="sxs-lookup"><span data-stu-id="289e5-p102">Normalization rules define how phone numbers expressed in various formats are to be routed for each specified location, user, or contact object. The same dial string may be interpreted and translated differently, depending on the location from which it is dialed and the person or contact object that makes the call. A set of normalization rules associated with a particular location constitutes a dial plan.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289e5-119">VoIP-Richtlinie</span><span class="sxs-lookup"><span data-stu-id="289e5-119">Voice policy</span></span></p></td>
<td><p><span data-ttu-id="289e5-p103">Eine VoIP-Richtlinie ordnet einem Benutzer oder einer Benutzergruppe mindestens einen PSTN-Verwendungseintrag zu. Außerdem enthält eine VoIP-Richtlinie immer eine Liste der Anruffunktionen, die Sie aktivieren oder deaktivieren können.</span><span class="sxs-lookup"><span data-stu-id="289e5-p103">A voice policy associates one or more PSTN usage records with one user or a group of users. A voice policy also provides a list of calling features that you can enable or disable.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="289e5-122">PSTN-Verwendungseintrag</span><span class="sxs-lookup"><span data-stu-id="289e5-122">PSTN usage record</span></span></p></td>
<td><p><span data-ttu-id="289e5-123">Ein PSTN-Verwendungseintrag gibt eine Klasse von Anrufen an (z. B. interne Anrufe, Ortsgespräche oder Ferngespräche), die von bestimmten Benutzern oder Benutzergruppen in einer Organisation getätigt werden dürfen.</span><span class="sxs-lookup"><span data-stu-id="289e5-123">A PSTN usage record specifies a class of call (such as internal, local, or long distance) that can be made by various users, or groups of users, in an organization.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="289e5-124">Anrufroute</span><span class="sxs-lookup"><span data-stu-id="289e5-124">Call Route</span></span></p></td>
<td><p><span data-ttu-id="289e5-p104">Eine Anrufroute ordnet Zielrufnummern bestimmte Trunks und PSTN-Verwendungseinträge zu. Ein PSTN-Gateway wird als Trunk angesehen.</span><span class="sxs-lookup"><span data-stu-id="289e5-p104">A call route associates destination phone numbers with particular trunks and PSTN usage records. A PSTN gateway is considered a trunk.</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="in-this-section"></a><span data-ttu-id="289e5-127">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="289e5-127">In This Section</span></span>

<span data-ttu-id="289e5-128">In diesem Abschnitt finden Sie Richtlinien für die Konfiguration der folgenden Routingserver Einstellungen für ausgehende Anrufe:</span><span class="sxs-lookup"><span data-stu-id="289e5-128">This section provides guidelines for configuring the following outbound call routing server settings:</span></span>

  - <span></span>  
    [<span data-ttu-id="289e5-129">Wählpläne und Normalisierungsregeln in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="289e5-129">Dial plans and normalization rules in Lync Server 2013</span></span>](lync-server-2013-dial-plans-and-normalization-rules.md)

  - <span></span>  
    [<span data-ttu-id="289e5-130">VoIP-Richtlinien in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="289e5-130">Voice policies in Lync Server 2013</span></span>](lync-server-2013-voice-policies.md)

  - <span></span>  
    [<span data-ttu-id="289e5-131">PSTN-Verwendungsdatensätze in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="289e5-131">PSTN usage records in Lync Server 2013</span></span>](lync-server-2013-pstn-usage-records.md)

  - <span></span>  
    [<span data-ttu-id="289e5-132">VoIP-Routen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="289e5-132">Voice routes in Lync Server 2013</span></span>](lync-server-2013-voice-routes.md)

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="289e5-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="289e5-133">See Also</span></span>


[<span data-ttu-id="289e5-134">SIP-Trunking in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="289e5-134">SIP trunking in Lync Server 2013</span></span>](lync-server-2013-sip-trunking.md)  
[<span data-ttu-id="289e5-135">Direkte SIP-Verbindungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="289e5-135">Direct SIP connections in Lync Server 2013</span></span>](lync-server-2013-direct-sip-connections.md)  
  

<span data-ttu-id="289e5-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="289e5-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

