---
title: 'Lync Server 2013: Benutzerverwaltung für gehostete Exchange-Dienste'
description: 'Lync Server 2013: Hosted Exchange-Benutzerverwaltung'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Hosted Exchange user management
ms:assetid: e8723af5-0604-4d7d-bad2-463a9832efb4
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg399037(v=OCS.15)
ms:contentKeyID: 48185887
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 9ceda9352fc627fc7b762b5995d788ffafa159ae
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49427523"
---
# <a name="hosted-exchange-user-management-in-lync-server-2013"></a><span data-ttu-id="c58d6-103">Benutzerverwaltung für gehostete Exchange-Dienste in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="c58d6-103">Hosted Exchange user management in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="c58d6-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="c58d6-104">

<span> </span></span></span>

<span data-ttu-id="c58d6-105">_**Letztes Änderungsdatum des Themas:** 2012-10-18_</span><span class="sxs-lookup"><span data-stu-id="c58d6-105">_**Topic Last Modified:** 2012-10-18_</span></span>

<span data-ttu-id="c58d6-106">Wenn Sie Voicemail-Dienste für lync Server 2013-Benutzer bereitstellen möchten, deren Postfächer sich in einem gehosteten Exchange-Dienst befinden, müssen Sie deren Benutzerkonten für gehostete Voicemail aktivieren.</span><span class="sxs-lookup"><span data-stu-id="c58d6-106">To provide voice mail services for Lync Server 2013 users whose mailboxes are located on a hosted Exchange service, you must enable their user accounts for hosted voice mail.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="c58d6-107">Bevor ein lync Server 2013-Benutzer für gehostete Voicemail aktiviert werden kann, muss eine gehostete Voicemail-Richtlinie bereitgestellt werden, die für das entsprechende Benutzerkonto gilt.</span><span class="sxs-lookup"><span data-stu-id="c58d6-107">Before a Lync Server 2013 user can be enabled for hosted voice mail, a hosted voice mail policy that applies to the corresponding user account must be deployed.</span></span> <span data-ttu-id="c58d6-108">Die Richtlinie kann global, Site oder pro Benutzer im Umfang sein, sofern Sie für den Benutzer gilt, den Sie aktivieren möchten.</span><span class="sxs-lookup"><span data-stu-id="c58d6-108">The policy can be global, site, or per-user in scope, as long as it applies to the user whom you want to enable.</span></span> <span data-ttu-id="c58d6-109">Ausführliche Informationen finden Sie unter <A href="lync-server-2013-hosted-voice-mail-policies.md">Richtlinien für gehostete Voicemail in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="c58d6-109">For details, see <A href="lync-server-2013-hosted-voice-mail-policies.md">Hosted voice mail policies in Lync Server 2013</A>.</span></span>



</div>

<div>

## <a name="the-msexchucvoicemailsettings-attribute"></a><span data-ttu-id="c58d6-110">Das msExchUCVoiceMailSettings-Attribut</span><span class="sxs-lookup"><span data-stu-id="c58d6-110">The msExchUCVoiceMailSettings Attribute</span></span>

<span data-ttu-id="c58d6-111">Lync Server 2013 führt ein neues Benutzerattribut mit dem Namen **msExchUCVoiceMailSettings** ein, das im Rahmen der Active Directory-Schemavorbereitung von lync Server 2013 erstellt wird.</span><span class="sxs-lookup"><span data-stu-id="c58d6-111">Lync Server 2013 introduces a new user attribute named **msExchUCVoiceMailSettings**, which is created as part of the Lync Server 2013 Active Directory schema preparation.</span></span> <span data-ttu-id="c58d6-112">Dieses mehrwertige Attribut enthält Einstellungen für Voicemail, die von lync Server 2013 und dem gehosteten Exchange-Dienst freigegeben werden.</span><span class="sxs-lookup"><span data-stu-id="c58d6-112">This multivalued attribute holds voice mail settings that are shared by Lync Server 2013 and the hosted Exchange service.</span></span>

<span data-ttu-id="c58d6-113">Der gehostete Exchange-Dienst kann in einigen Fällen den Wert des Attributs msExchUCVoiceMailSettings beim Aktivieren von Exchange um oder während des Prozesses der Übertragung von Postfächern auf einen gehosteten Exchange-Server einstellen.</span><span class="sxs-lookup"><span data-stu-id="c58d6-113">The hosted Exchange service may in some cases set the value of the msExchUCVoiceMailSettings attribute in the process of enabling Exchange UM, or during the process of transferring mailboxes to a hosted Exchange Server.</span></span> <span data-ttu-id="c58d6-114">Wenn dieses Attribut nicht von Exchange gesetzt wird, muss der lync Server 2013-Administrator es durch Ausführen des Set-CsUser-Cmdlets einrichten, wie weiter oben in diesem Thema beschrieben.</span><span class="sxs-lookup"><span data-stu-id="c58d6-114">If this attribute is not set by Exchange, the Lync Server 2013 administrator must set it by running the Set-CsUser cmdlet, as described earlier in this topic.</span></span>

<span data-ttu-id="c58d6-115">Die Schlüssel-Wert-Paare des Attributs und deren Autoren sind in der folgenden Tabelle dargestellt.</span><span class="sxs-lookup"><span data-stu-id="c58d6-115">The attribute’s key/value pairs and their authors are shown in the following table.</span></span>

### <a name="the-msexchucvoicemailsettings-attribute-keyvalue-pairs"></a><span data-ttu-id="c58d6-116">Schlüssel-Wert-Paare des msExchUCVoiceMailSettings-Attributs</span><span class="sxs-lookup"><span data-stu-id="c58d6-116">The msExchUCVoiceMailSettings Attribute Key/Value Pairs</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="c58d6-117">Wert</span><span class="sxs-lookup"><span data-stu-id="c58d6-117">Value</span></span></th>
<th><span data-ttu-id="c58d6-118">Autor</span><span class="sxs-lookup"><span data-stu-id="c58d6-118">Author</span></span></th>
<th><span data-ttu-id="c58d6-119">Bedeutung</span><span class="sxs-lookup"><span data-stu-id="c58d6-119">Meaning</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="c58d6-120">ExchangeHostedVoiceMail = 1</span><span class="sxs-lookup"><span data-stu-id="c58d6-120">ExchangeHostedVoiceMail=1</span></span></p></td>
<td><p><span data-ttu-id="c58d6-121">Exchange</span><span class="sxs-lookup"><span data-stu-id="c58d6-121">Exchange</span></span></p></td>
<td><p><span data-ttu-id="c58d6-122">Der Benutzer wurde für den gehosteten um-Zugriff durch Exchange Server aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c58d6-122">User has been enabled for hosted UM access by Exchange Server.</span></span> <span data-ttu-id="c58d6-123">Die Exchange um-Routing Anwendung überprüft die Richtlinie des Benutzers für gehostete Voicemail auf Routing Details.</span><span class="sxs-lookup"><span data-stu-id="c58d6-123">The Exchange UM Routing application will check the user’s hosted voice mail policy for routing details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c58d6-124">ExchangeHostedVoiceMail = 0</span><span class="sxs-lookup"><span data-stu-id="c58d6-124">ExchangeHostedVoiceMail=0</span></span></p></td>
<td><p><span data-ttu-id="c58d6-125">Exchange</span><span class="sxs-lookup"><span data-stu-id="c58d6-125">Exchange</span></span></p></td>
<td><p><span data-ttu-id="c58d6-126">Der Benutzer wurde für den gehosteten um-Zugriff durch Exchange Server deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c58d6-126">User has been disabled for hosted UM access by Exchange Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="c58d6-127">CsHostedVoiceMail = 1</span><span class="sxs-lookup"><span data-stu-id="c58d6-127">CsHostedVoiceMail=1</span></span></p></td>
<td><p><span data-ttu-id="c58d6-128">Lync Server</span><span class="sxs-lookup"><span data-stu-id="c58d6-128">Lync Server</span></span></p></td>
<td><p><span data-ttu-id="c58d6-129">Der Benutzer wurde für den gehosteten um-Zugriff von lync Server 2013 aktiviert.</span><span class="sxs-lookup"><span data-stu-id="c58d6-129">User has been enabled for hosted UM access by Lync Server 2013.</span></span> <span data-ttu-id="c58d6-130">Die lync Server 2013 ExUM-Routing Anwendung überprüft die Richtlinie des Benutzers für gehostete Voicemail auf Routing Details.</span><span class="sxs-lookup"><span data-stu-id="c58d6-130">The Lync Server 2013 ExUM Routing application will check the user’s hosted voice mail policy for routing details.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="c58d6-131">CsHostedVoiceMail = 0</span><span class="sxs-lookup"><span data-stu-id="c58d6-131">CsHostedVoiceMail=0</span></span></p></td>
<td><p><span data-ttu-id="c58d6-132">Lync Server</span><span class="sxs-lookup"><span data-stu-id="c58d6-132">Lync Server</span></span></p></td>
<td><p><span data-ttu-id="c58d6-133">Der Benutzer wurde für den gehosteten um-Zugriff von lync Server 2013 deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="c58d6-133">User has been disabled for hosted UM access by Lync Server 2013.</span></span></p></td>
</tr>
</tbody>
</table>


<div>


> [!NOTE]  
> <span data-ttu-id="c58d6-134">Wenn das Attribut bereits Werte enthält, die nicht zu den Schlüssel-Wert-Paaren von lync Server 2013 (CSHostedVoiceMail = 0 oder CSHostedVoiceMail = 1) führen, wird eine Warnung angezeigt, die besagt, dass das Attribut von einer anderen Anwendung verwaltet werden kann.</span><span class="sxs-lookup"><span data-stu-id="c58d6-134">If the attribute already has values other than one of the Lync Server 2013 key/value pairs (CSHostedVoiceMail=0 or CSHostedVoiceMail=1), a warning will indicate that the attribute may be managed by a different application.</span></span> <span data-ttu-id="c58d6-135">Beispielsweise wird eine Warnung angezeigt, wenn das Schlüssel-Wert-Paar ExchangeHostedVoiceMail = 0 oder ExchangeHostedVoiceMail = 1 bereits vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="c58d6-135">For example, a warning is displayed if the key/value pair ExchangeHostedVoiceMail=0 or ExchangeHostedVoiceMail=1 is already present.</span></span> <span data-ttu-id="c58d6-136">In diesem Fall können Sie den Wert ändern, indem Sie ihn in Active Directory bearbeiten, oder führen Sie das folgende Cmdlet aus, um den Wert auf NULL festzulegen:</span><span class="sxs-lookup"><span data-stu-id="c58d6-136">In that case, you can change the value by editing it the Active Directory, or run the following cmdlet to set the value to null:</span></span><BR><span data-ttu-id="c58d6-137">Set-CsUser – Identity User – HostedVoicemail $NULL</span><span class="sxs-lookup"><span data-stu-id="c58d6-137">Set-CsUser –identity user –HostedVoicemail $null</span></span>



</div>

</div>

<div>

## <a name="enabling-users-for-hosted-voice-mail"></a><span data-ttu-id="c58d6-138">Aktivieren von Benutzern für gehostete Voicemails</span><span class="sxs-lookup"><span data-stu-id="c58d6-138">Enabling Users for Hosted Voice Mail</span></span>

<span data-ttu-id="c58d6-139">Damit die Voicemail-Anrufe eines Benutzers an gehostete Exchange um weitergeleitet werden können, müssen Sie das Set-CsUser-Cmdlet ausführen, um den Wert des *HostedVoiceMail* -Parameters festzulegen.</span><span class="sxs-lookup"><span data-stu-id="c58d6-139">To enable a user’s voice mail calls to be routed to hosted Exchange UM, you must run the Set-CsUser cmdlet to set the value of the *HostedVoiceMail* parameter.</span></span> <span data-ttu-id="c58d6-140">Dieser Parameter signalisiert auch, dass lync Server 2013 den Indikator "Voicemail anrufen" aufleuchtet.</span><span class="sxs-lookup"><span data-stu-id="c58d6-140">This parameter also signals Lync Server 2013 to light up the “call voice mail” indicator.</span></span>

  - <span data-ttu-id="c58d6-141">Im folgenden Beispiel wird das Benutzerkonto von Pilar Ackerman für gehostete Voicemail aktiviert:</span><span class="sxs-lookup"><span data-stu-id="c58d6-141">The following example enables Pilar Ackerman’s user account for hosted voice mail:</span></span>
    
        Set-CsUser -Identity "Pilar Ackerman" -HostedVoiceMail $True
    
    <span data-ttu-id="c58d6-142">Das Cmdlet überprüft, ob eine gehostete Voicemail-Richtlinie (Global, Websiteebene oder pro Benutzer) für diesen Benutzer gilt.</span><span class="sxs-lookup"><span data-stu-id="c58d6-142">The cmdlet verifies that a hosted voice mail policy (global, site-level or per-user) applies to this user.</span></span> <span data-ttu-id="c58d6-143">Wenn keine Richtlinie zutrifft, schlägt das Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="c58d6-143">If no policy applies, the cmdlet fails.</span></span>

  - <span data-ttu-id="c58d6-144">Im folgenden Beispiel wird das Benutzerkonto von Pilar Ackerman für gehostete Voicemail deaktiviert:</span><span class="sxs-lookup"><span data-stu-id="c58d6-144">The following example disables Pilar Ackerman’s user account for hosted voice mail:</span></span>
    
        Set-CsUser -Identity "Pilar Ackerman" -HostedVoiceMail $False
    
    <span data-ttu-id="c58d6-145">Das Cmdlet überprüft, ob für diesen Benutzer keine gehostete Voicemail-Richtlinie (Global, Website-Ebene oder pro Benutzer) gilt.</span><span class="sxs-lookup"><span data-stu-id="c58d6-145">The cmdlet verifies that no hosted voice mail policy (global, site-level or per-user) applies to this user.</span></span> <span data-ttu-id="c58d6-146">Wenn eine Richtlinie angewendet wird, schlägt das Cmdlet fehl.</span><span class="sxs-lookup"><span data-stu-id="c58d6-146">If a policy does apply, the cmdlet fails.</span></span>

<span data-ttu-id="c58d6-147">Details zur Verwendung des Set-CsUser-Cmdlets finden Sie in der Dokumentation zur lync Server-Verwaltungsshell.</span><span class="sxs-lookup"><span data-stu-id="c58d6-147">For details about using the Set-CsUser cmdlet, see the Lync Server Management Shell documentation.</span></span>

<span data-ttu-id="c58d6-148"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="c58d6-148"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

