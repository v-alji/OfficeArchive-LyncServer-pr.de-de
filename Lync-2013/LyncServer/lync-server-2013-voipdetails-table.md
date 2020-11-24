---
title: 'Lync Server 2013: VoipDetails-Tabelle'
description: 'Lync Server 2013: VoipDetails-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: VoipDetails table
ms:assetid: 74ffbb71-569b-4018-be1f-4db2bbafcf36
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398566(v=OCS.15)
ms:contentKeyID: 48184522
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: f23d991c1d577a15717de2572d744e1b65ba6bab
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49393786"
---
# <a name="voipdetails-table-in-lync-server-2013"></a><span data-ttu-id="fee6f-103">VoipDetails-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="fee6f-103">VoipDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="fee6f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="fee6f-104">

<span> </span></span></span>

<span data-ttu-id="fee6f-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="fee6f-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="fee6f-106">Jeder Datensatz steht für 1 2-Party-Anrufe, bei denen mindestens ein Nutzer ein VoIP-Nutzer ist.</span><span class="sxs-lookup"><span data-stu-id="fee6f-106">Each record represents one two-party call in which at least one user is a VoIP user.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="fee6f-107">Spalte</span><span class="sxs-lookup"><span data-stu-id="fee6f-107">Column</span></span></th>
<th><span data-ttu-id="fee6f-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="fee6f-108">Data Type</span></span></th>
<th><span data-ttu-id="fee6f-109">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="fee6f-109">Key/Index</span></span></th>
<th><span data-ttu-id="fee6f-110">Details</span><span class="sxs-lookup"><span data-stu-id="fee6f-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="fee6f-111"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="fee6f-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="fee6f-112">datetime</span><span class="sxs-lookup"><span data-stu-id="fee6f-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="fee6f-113">Primary</span><span class="sxs-lookup"><span data-stu-id="fee6f-113">Primary</span></span></p></td>
<td><p><span data-ttu-id="fee6f-114">Uhrzeit der Sitzungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="fee6f-114">Time of session request.</span></span> <span data-ttu-id="fee6f-115">Wird in Verbindung mit <strong>SessionIdSeq</strong> verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fee6f-115">Used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a session.</span></span> <span data-ttu-id="fee6f-116">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="fee6f-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fee6f-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="fee6f-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="fee6f-118">int</span><span class="sxs-lookup"><span data-stu-id="fee6f-118">int</span></span></p></td>
<td><p><span data-ttu-id="fee6f-119">Primary</span><span class="sxs-lookup"><span data-stu-id="fee6f-119">Primary</span></span></p></td>
<td><p><span data-ttu-id="fee6f-120">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fee6f-120">ID number to identify the session.</span></span> <span data-ttu-id="fee6f-121">Wird in Verbindung mit <strong>SessionID</strong> -Mal verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fee6f-121">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a session.</span></span> <span data-ttu-id="fee6f-122">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="fee6f-122">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fee6f-123"><strong>FromNumberId</strong></span><span class="sxs-lookup"><span data-stu-id="fee6f-123"><strong>FromNumberId</strong></span></span></p></td>
<td><p><span data-ttu-id="fee6f-124">int</span><span class="sxs-lookup"><span data-stu-id="fee6f-124">int</span></span></p></td>
<td><p><span data-ttu-id="fee6f-125">Fremd</span><span class="sxs-lookup"><span data-stu-id="fee6f-125">Foreign</span></span></p></td>
<td><p><span data-ttu-id="fee6f-126"><strong>Telefonnummer</strong> des Anrufers.</span><span class="sxs-lookup"><span data-stu-id="fee6f-126"><strong>PhoneId</strong> of the caller.</span></span> <span data-ttu-id="fee6f-127">Weitere Informationen finden Sie <a href="lync-server-2013-phones-table.md">in der Tabelle Telefone in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="fee6f-127">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="fee6f-128">Wenn nicht NULL und <strong>FromGatewayId</strong> nicht NULL ist, war der Aufrufer ein PSTN-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="fee6f-128">If not NULL and <strong>FromGatewayId</strong> is not NULL, then the caller was a PSTN user.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fee6f-129"><strong>ConnectedNumberId</strong></span><span class="sxs-lookup"><span data-stu-id="fee6f-129"><strong>ConnectedNumberId</strong></span></span></p></td>
<td><p><span data-ttu-id="fee6f-130">int</span><span class="sxs-lookup"><span data-stu-id="fee6f-130">int</span></span></p></td>
<td><p><span data-ttu-id="fee6f-131">Fremd</span><span class="sxs-lookup"><span data-stu-id="fee6f-131">Foreign</span></span></p></td>
<td><p><span data-ttu-id="fee6f-132"><strong>Telefonnummer</strong> des anrufempfängers.</span><span class="sxs-lookup"><span data-stu-id="fee6f-132"><strong>PhoneId</strong> of the call receiver.</span></span> <span data-ttu-id="fee6f-133">Weitere Informationen finden Sie <a href="lync-server-2013-phones-table.md">in der Tabelle Telefone in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="fee6f-133">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="fee6f-134">Wenn nicht NULL und <strong>togateway</strong> -Nr NULL ist, war der Anrufempfänger ein PSTN-Benutzer.</span><span class="sxs-lookup"><span data-stu-id="fee6f-134">If not NULL and <strong>ToGatewayId</strong> is not NULL, then the call receiver was a PSTN user.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fee6f-135"><strong>FromMediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="fee6f-135"><strong>FromMediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="fee6f-136">int</span><span class="sxs-lookup"><span data-stu-id="fee6f-136">int</span></span></p></td>
<td><p><span data-ttu-id="fee6f-137">Fremd</span><span class="sxs-lookup"><span data-stu-id="fee6f-137">Foreign</span></span></p></td>
<td><p><span data-ttu-id="fee6f-138">Der Vermittlungs Server, aus dem der Anruf kommt.</span><span class="sxs-lookup"><span data-stu-id="fee6f-138">The Mediation Server the call is coming from.</span></span> <span data-ttu-id="fee6f-139">Weitere Informationen finden Sie <a href="lync-server-2013-mediationservers-table.md">in der MediationServers-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="fee6f-139">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fee6f-140"><strong>ToMediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="fee6f-140"><strong>ToMediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="fee6f-141">int</span><span class="sxs-lookup"><span data-stu-id="fee6f-141">int</span></span></p></td>
<td><p><span data-ttu-id="fee6f-142">Fremd</span><span class="sxs-lookup"><span data-stu-id="fee6f-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="fee6f-143">Der Vermittlungs Server wird aufgerufen.</span><span class="sxs-lookup"><span data-stu-id="fee6f-143">The Mediation Server called is going to.</span></span> <span data-ttu-id="fee6f-144">Weitere Informationen finden Sie <a href="lync-server-2013-mediationservers-table.md">in der MediationServers-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="fee6f-144">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fee6f-145"><strong>FromGatewayId</strong></span><span class="sxs-lookup"><span data-stu-id="fee6f-145"><strong>FromGatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="fee6f-146">int</span><span class="sxs-lookup"><span data-stu-id="fee6f-146">int</span></span></p></td>
<td><p><span data-ttu-id="fee6f-147">Fremd</span><span class="sxs-lookup"><span data-stu-id="fee6f-147">Foreign</span></span></p></td>
<td><p><span data-ttu-id="fee6f-148">Gateway, aus dem der Anruf kommt.</span><span class="sxs-lookup"><span data-stu-id="fee6f-148">Gateway the call is coming from.</span></span> <span data-ttu-id="fee6f-149">Weitere Informationen finden Sie <a href="lync-server-2013-gateways-table.md">in der Tabelle Gateways in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="fee6f-149">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fee6f-150"><strong>Togatewayservernummer</strong></span><span class="sxs-lookup"><span data-stu-id="fee6f-150"><strong>ToGatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="fee6f-151">int</span><span class="sxs-lookup"><span data-stu-id="fee6f-151">int</span></span></p></td>
<td><p><span data-ttu-id="fee6f-152">Fremd</span><span class="sxs-lookup"><span data-stu-id="fee6f-152">Foreign</span></span></p></td>
<td><p><span data-ttu-id="fee6f-153">Gateway, an das der Anruf geht.</span><span class="sxs-lookup"><span data-stu-id="fee6f-153">Gateway the call is going to.</span></span> <span data-ttu-id="fee6f-154">Weitere Informationen finden Sie <a href="lync-server-2013-gateways-table.md">in der Tabelle Gateways in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="fee6f-154">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="fee6f-155"><strong>DisconnectedbyURIId</strong></span><span class="sxs-lookup"><span data-stu-id="fee6f-155"><strong>DisconnectedbyURIId</strong></span></span></p></td>
<td><p><span data-ttu-id="fee6f-156">int</span><span class="sxs-lookup"><span data-stu-id="fee6f-156">int</span></span></p></td>
<td><p><span data-ttu-id="fee6f-157">Fremd</span><span class="sxs-lookup"><span data-stu-id="fee6f-157">Foreign</span></span></p></td>
<td><p><span data-ttu-id="fee6f-158">Der URI des Benutzers, der den Anruf getrennt hat, wenn der Benutzer über einen URI verfügt.</span><span class="sxs-lookup"><span data-stu-id="fee6f-158">URI of the user who disconnected the call, if the user has a URI.</span></span> <span data-ttu-id="fee6f-159">Weitere Informationen finden Sie <a href="lync-server-2013-users-table.md">in der Tabelle Benutzer in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="fee6f-159">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="fee6f-160"><strong>DisconnectedbyPhoneId</strong></span><span class="sxs-lookup"><span data-stu-id="fee6f-160"><strong>DisconnectedbyPhoneId</strong></span></span></p></td>
<td><p><span data-ttu-id="fee6f-161">int</span><span class="sxs-lookup"><span data-stu-id="fee6f-161">int</span></span></p></td>
<td><p><span data-ttu-id="fee6f-162">Fremd</span><span class="sxs-lookup"><span data-stu-id="fee6f-162">Foreign</span></span></p></td>
<td><p><span data-ttu-id="fee6f-163">Die ID des Telefons, das den Anruf getrennt hat, wurde von einem Telefon getrennt.</span><span class="sxs-lookup"><span data-stu-id="fee6f-163">ID of the phone that disconnected the call was disconnected from a phone.</span></span> <span data-ttu-id="fee6f-164">Weitere Informationen finden Sie <a href="lync-server-2013-phones-table.md">in der Tabelle Telefone in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="fee6f-164">See the <a href="lync-server-2013-phones-table.md">Phones table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="fee6f-165">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="fee6f-165">


</div>

<span> </span>

</div>

</div>

</span></span></div>

