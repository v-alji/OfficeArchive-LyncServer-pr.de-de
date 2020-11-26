---
title: 'Lync Server 2013: ConferenceSessionDetails-Tabelle'
description: 'Lync Server 2013: ConferenceSessionDetails-Tabelle.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceSessionDetails table
ms:assetid: 9eae6a54-69fd-4966-aa17-7ecee1297ad8
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412741(v=OCS.15)
ms:contentKeyID: 48184925
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 0d101eb1607e366ab814e60acaeee80820fe87c5
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434417"
---
# <a name="conferencesessiondetails-table-in-lync-server-2013"></a><span data-ttu-id="78da1-103">ConferenceSessionDetails-Tabelle in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="78da1-103">ConferenceSessionDetails table in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="78da1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="78da1-104">

<span> </span></span></span>

<span data-ttu-id="78da1-105">_**Letztes Änderungsdatum des Themas:** 2012-09-28_</span><span class="sxs-lookup"><span data-stu-id="78da1-105">_**Topic Last Modified:** 2012-09-28_</span></span>

<span data-ttu-id="78da1-106">Jeder Datensatz stellt eine Konferenzsitzung dar, bei der es sich entweder um die Sitzung mit dem Fokus oder um die Sitzung mit einem bestimmten Konferenzserver handeln kann.</span><span class="sxs-lookup"><span data-stu-id="78da1-106">Each record represents one conference session, which could be either the session with Focus or the session with a specific conferencing server.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="78da1-107">Spalte</span><span class="sxs-lookup"><span data-stu-id="78da1-107">Column</span></span></th>
<th><span data-ttu-id="78da1-108">Datentyp</span><span class="sxs-lookup"><span data-stu-id="78da1-108">Data Type</span></span></th>
<th><span data-ttu-id="78da1-109">Schlüssel/Index</span><span class="sxs-lookup"><span data-stu-id="78da1-109">Key/Index</span></span></th>
<th><span data-ttu-id="78da1-110">Details</span><span class="sxs-lookup"><span data-stu-id="78da1-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="78da1-111"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-112">DateTime</span><span class="sxs-lookup"><span data-stu-id="78da1-112">Datetime</span></span></p></td>
<td><p><span data-ttu-id="78da1-113">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="78da1-113">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="78da1-114">Uhrzeit der Sitzungsanforderung; wird in Verbindung mit <strong>SessionIdSeq</strong> verwendet, um eine Konferenzsitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="78da1-114">Time of session request; used in conjunction with <strong>SessionIdSeq</strong> to uniquely identify a conference session.</span></span> <span data-ttu-id="78da1-115">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78da1-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78da1-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-117">int</span><span class="sxs-lookup"><span data-stu-id="78da1-117">int</span></span></p></td>
<td><p><span data-ttu-id="78da1-118">Primär, fremd</span><span class="sxs-lookup"><span data-stu-id="78da1-118">Primary, Foreign</span></span></p></td>
<td><p><span data-ttu-id="78da1-119">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="78da1-119">ID number to identify the session.</span></span> <span data-ttu-id="78da1-120">Wird in Verbindung mit <strong>SessionID</strong> -Mal verwendet, um eine Konferenzsitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="78da1-120">Used in conjunction with <strong>SessionIdTime</strong> to uniquely identify a conference session.</span></span> <span data-ttu-id="78da1-121">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78da1-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span> *</p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78da1-122"><strong>ConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-122"><strong>ConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-123">int</span><span class="sxs-lookup"><span data-stu-id="78da1-123">int</span></span></p></td>
<td><p><span data-ttu-id="78da1-124">Fremd</span><span class="sxs-lookup"><span data-stu-id="78da1-124">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78da1-125">Fokus Konferenz-URI, der sich auf diese Sitzung bezieht.</span><span class="sxs-lookup"><span data-stu-id="78da1-125">Focus conference URI related to this session.</span></span> <span data-ttu-id="78da1-126">Weitere Informationen finden Sie <a href="lync-server-2013-conferenceuris-table.md">in der ConferenceUris-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78da1-126">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="78da1-127">Dieser URI ist ein Fokus basierter Konferenz-URI.</span><span class="sxs-lookup"><span data-stu-id="78da1-127">This URI is a Focus-based conference URI.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78da1-128"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-128"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-129">uniqueIdentifier</span><span class="sxs-lookup"><span data-stu-id="78da1-129">uniqueIdentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78da1-130">Bezeichner, der zwischen Instanzen von wiederkehrenden Konferenzen unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="78da1-130">Identifier that differentiates between instances of recurring conferences.</span></span> <span data-ttu-id="78da1-131">Jede wiederkehrende Konferenz Instanz hat dieselbe ConferenceURI, aber einen anderen ConfInstance-Wert.</span><span class="sxs-lookup"><span data-stu-id="78da1-131">Each recurring conference instance has the same ConferenceURI but a different ConfInstance value.</span></span></p>
<p><span data-ttu-id="78da1-132">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="78da1-132">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78da1-133"><strong>McuConferenceUriId</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-133"><strong>McuConferenceUriId</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-134">int</span><span class="sxs-lookup"><span data-stu-id="78da1-134">int</span></span></p></td>
<td><p><span data-ttu-id="78da1-135">Fremd</span><span class="sxs-lookup"><span data-stu-id="78da1-135">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78da1-136">Konferenzserver-Konferenz-URI, der sich auf diese Sitzung bezieht.</span><span class="sxs-lookup"><span data-stu-id="78da1-136">Conferencing server conference URI related to this session.</span></span> <span data-ttu-id="78da1-137">Weitere Informationen finden Sie <a href="lync-server-2013-conferenceuris-table.md">in der ConferenceUris-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78da1-137">See the <a href="lync-server-2013-conferenceuris-table.md">ConferenceUris table in Lync Server 2013</a> for more information.</span></span> <span data-ttu-id="78da1-138">Dieser URI ist der Konferenz-serverbasierte Konferenz-URI.</span><span class="sxs-lookup"><span data-stu-id="78da1-138">This URI is the conferencing server-based conference URI.</span></span> <span data-ttu-id="78da1-139">Für Konferenzsitzungen mit Fokus ist diese Spalte NULL.</span><span class="sxs-lookup"><span data-stu-id="78da1-139">For Focus conference sessions, this column will be null.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78da1-140"><strong>UserID</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-140"><strong>UserId</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-141">int</span><span class="sxs-lookup"><span data-stu-id="78da1-141">int</span></span></p></td>
<td><p><span data-ttu-id="78da1-142">Fremd</span><span class="sxs-lookup"><span data-stu-id="78da1-142">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78da1-143">Die ID eines Benutzers in der Konferenzsitzung.</span><span class="sxs-lookup"><span data-stu-id="78da1-143">ID of one user in the conference session.</span></span> <span data-ttu-id="78da1-144">Weitere Informationen finden Sie <a href="lync-server-2013-users-table.md">in der Tabelle Benutzer in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78da1-144">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78da1-145"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-145"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-146">uniqueidentifier</span><span class="sxs-lookup"><span data-stu-id="78da1-146">uniqueidentifier</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78da1-147">Eine GUID zum Identifizieren der Instanz des Endpunkts.</span><span class="sxs-lookup"><span data-stu-id="78da1-147">A GUID to identify the instance of endpoint.</span></span> <span data-ttu-id="78da1-148">Wenn sich ein Benutzer beispielsweise an verschiedenen Computern mit demselben Konto anmeldet, verfügt jeder Computer über eine andere Endpunkt-ID.</span><span class="sxs-lookup"><span data-stu-id="78da1-148">For example, if one user logs on to different machines with the same account, then each machine will have a different endpoint ID.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78da1-149"><strong>OnBehalfOfId</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-149"><strong>OnBehalfOfId</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-150">int</span><span class="sxs-lookup"><span data-stu-id="78da1-150">int</span></span></p></td>
<td><p><span data-ttu-id="78da1-151">Fremd</span><span class="sxs-lookup"><span data-stu-id="78da1-151">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78da1-152">Gibt die ID des Benutzers an, der der Anrufer im Auftrag ist.</span><span class="sxs-lookup"><span data-stu-id="78da1-152">Indicates the ID of the user of who the caller is on behalf.</span></span> <span data-ttu-id="78da1-153">Weitere Informationen finden Sie <a href="lync-server-2013-users-table.md">in der Tabelle Benutzer in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78da1-153">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78da1-154"><strong>ReferredById</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-154"><strong>ReferredById</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-155">int</span><span class="sxs-lookup"><span data-stu-id="78da1-155">int</span></span></p></td>
<td><p><span data-ttu-id="78da1-156">Fremd</span><span class="sxs-lookup"><span data-stu-id="78da1-156">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78da1-157">Die ID des Benutzers, auf den der Anruf verweist.</span><span class="sxs-lookup"><span data-stu-id="78da1-157">ID of the user by who the call is referred.</span></span> <span data-ttu-id="78da1-158">Weitere Informationen finden Sie <a href="lync-server-2013-users-table.md">in der Tabelle Benutzer in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78da1-158">See the <a href="lync-server-2013-users-table.md">Users table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78da1-159"><strong>UserClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-159"><strong>UserClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-160">int</span><span class="sxs-lookup"><span data-stu-id="78da1-160">int</span></span></p></td>
<td><p><span data-ttu-id="78da1-161">Fremd</span><span class="sxs-lookup"><span data-stu-id="78da1-161">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78da1-162">Vom Konferenzbenutzer verwendete Client Version.</span><span class="sxs-lookup"><span data-stu-id="78da1-162">Client version used by the conference user.</span></span> <span data-ttu-id="78da1-163">Weitere Informationen finden Sie <a href="lync-server-2013-clientversions-table.md">in der ClientVersions-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78da1-163">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78da1-164"><strong>ConfClientVersionId</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-164"><strong>ConfClientVersionId</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-165">int</span><span class="sxs-lookup"><span data-stu-id="78da1-165">int</span></span></p></td>
<td><p><span data-ttu-id="78da1-166">Fremd</span><span class="sxs-lookup"><span data-stu-id="78da1-166">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78da1-167">Client Version, die vom Konferenzserver verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="78da1-167">Client version used by the conference server.</span></span> <span data-ttu-id="78da1-168">Weitere Informationen finden Sie <a href="lync-server-2013-clientversions-table.md">in der ClientVersions-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78da1-168">See the <a href="lync-server-2013-clientversions-table.md">ClientVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78da1-169"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-169"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-170">datetime</span><span class="sxs-lookup"><span data-stu-id="78da1-170">datetime</span></span></p></td>
<td><p><span data-ttu-id="78da1-171">Fremd</span><span class="sxs-lookup"><span data-stu-id="78da1-171">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78da1-172">Die ID-Nummer, die das Dialogfeld identifiziert, das durch die aktuelle Sitzung ersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="78da1-172">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="78da1-173">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78da1-173">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78da1-174"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-174"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-175">int</span><span class="sxs-lookup"><span data-stu-id="78da1-175">int</span></span></p></td>
<td><p><span data-ttu-id="78da1-176">Fremd</span><span class="sxs-lookup"><span data-stu-id="78da1-176">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78da1-177">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="78da1-177">ID number to identify the session.</span></span> <span data-ttu-id="78da1-178">Wird in Verbindung mit <strong>ReplacesDialogIdTime</strong> verwendet, um eine Sitzung, die durch diese Sitzung ersetzt wird, eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="78da1-178">Used in conjunction with <strong>ReplacesDialogIdTime</strong> to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="78da1-179">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78da1-179">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78da1-180"><strong>IsStartedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-180"><strong>IsStartedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-181">bit</span><span class="sxs-lookup"><span data-stu-id="78da1-181">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78da1-182">Gibt an, ob die Sitzung vom Konferenz Server gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="78da1-182">Indicates if the session started by the conferencing Server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78da1-183"><strong>IsEndedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-183"><strong>IsEndedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-184">bit</span><span class="sxs-lookup"><span data-stu-id="78da1-184">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78da1-185">Gibt an, ob die Sitzung vom Konferenzserver beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="78da1-185">Indicates if the session ended by the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78da1-186"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-186"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-187">bit</span><span class="sxs-lookup"><span data-stu-id="78da1-187">bit</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78da1-188">Ob der Benutzer intern angemeldet ist oder nicht.</span><span class="sxs-lookup"><span data-stu-id="78da1-188">Whether user is logged on from internal or not.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78da1-189"><strong>Response Code</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-189"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-190">int</span><span class="sxs-lookup"><span data-stu-id="78da1-190">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78da1-191">SIP-Antwortcode (Session Initiation Protocol) für die Sitzungseinladung</span><span class="sxs-lookup"><span data-stu-id="78da1-191">Session Initiation Protocol (SIP) response code to the session invitation.</span></span> <span data-ttu-id="78da1-192">Dieses Feld wird in der Regel von Daten ausgefüllt, die aus der anfänglichen Einladungsnachricht in der Sitzung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="78da1-192">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="78da1-193">Wenn keine Einladungsnachricht vorhanden ist, wird das Feld mit dem Datum und der Uhrzeit der ersten relevanten SIP-Nachricht gefüllt (Bye, Cancel, Nachricht oder info).</span><span class="sxs-lookup"><span data-stu-id="78da1-193">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78da1-194"><strong>Diagnose-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-194"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-195">int</span><span class="sxs-lookup"><span data-stu-id="78da1-195">int</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78da1-196">Vom SIP-Header erfasste Diagnose-ID.</span><span class="sxs-lookup"><span data-stu-id="78da1-196">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78da1-197"><strong>ServerID</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-197"><strong>ServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-198">int</span><span class="sxs-lookup"><span data-stu-id="78da1-198">int</span></span></p></td>
<td><p><span data-ttu-id="78da1-199">Fremd</span><span class="sxs-lookup"><span data-stu-id="78da1-199">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78da1-200">Die ID des für diese Sitzung verwendeten Front-End-Servers.</span><span class="sxs-lookup"><span data-stu-id="78da1-200">ID of the front-end server used for this session.</span></span> <span data-ttu-id="78da1-201">Weitere Informationen finden Sie <a href="lync-server-2013-servers-table.md">in der Tabelle Server in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78da1-201">See the <a href="lync-server-2013-servers-table.md">Servers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78da1-202"><strong>Pool-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-202"><strong>PoolId</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-203">int</span><span class="sxs-lookup"><span data-stu-id="78da1-203">int</span></span></p></td>
<td><p><span data-ttu-id="78da1-204">Fremd</span><span class="sxs-lookup"><span data-stu-id="78da1-204">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78da1-205">Die ID des Pools, in dem die Sitzung erfasst wurde.</span><span class="sxs-lookup"><span data-stu-id="78da1-205">ID of the pool in which the session was captured.</span></span> <span data-ttu-id="78da1-206">Weitere Informationen finden Sie <a href="lync-server-2013-pools-table.md">in der Tabelle Pools in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78da1-206">See the <a href="lync-server-2013-pools-table.md">Pools table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78da1-207"><strong>MediationServerId</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-207"><strong>MediationServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-208">int</span><span class="sxs-lookup"><span data-stu-id="78da1-208">int</span></span></p></td>
<td><p><span data-ttu-id="78da1-209">Fremd</span><span class="sxs-lookup"><span data-stu-id="78da1-209">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78da1-210">Der Vermittlungs Server, den der Anruf verwendet.</span><span class="sxs-lookup"><span data-stu-id="78da1-210">The Mediation Server the call is using.</span></span> <span data-ttu-id="78da1-211">Weitere Informationen finden Sie <a href="lync-server-2013-mediationservers-table.md">in der MediationServers-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78da1-211">See the <a href="lync-server-2013-mediationservers-table.md">MediationServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78da1-212"><strong>Gatewayserver</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-212"><strong>GatewayId</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-213">int</span><span class="sxs-lookup"><span data-stu-id="78da1-213">int</span></span></p></td>
<td><p><span data-ttu-id="78da1-214">Fremd</span><span class="sxs-lookup"><span data-stu-id="78da1-214">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78da1-215">Das Gateway, das der Anruf verwendet.</span><span class="sxs-lookup"><span data-stu-id="78da1-215">The gateway the call is using.</span></span> <span data-ttu-id="78da1-216">Weitere Informationen finden Sie <a href="lync-server-2013-gateways-table.md">in der Tabelle Gateways in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78da1-216">See the <a href="lync-server-2013-gateways-table.md">Gateways table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78da1-217"><strong>EdgeServerId</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-217"><strong>EdgeServerId</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-218">int</span><span class="sxs-lookup"><span data-stu-id="78da1-218">int</span></span></p></td>
<td><p><span data-ttu-id="78da1-219">Fremd</span><span class="sxs-lookup"><span data-stu-id="78da1-219">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78da1-220">Der Edge-Server, den der Anruf verwendet.</span><span class="sxs-lookup"><span data-stu-id="78da1-220">The Edge Server the call is using.</span></span> <span data-ttu-id="78da1-221">Weitere Informationen finden Sie <a href="lync-server-2013-edgeservers-table.md">in der EdgeServers-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78da1-221">See the <a href="lync-server-2013-edgeservers-table.md">EdgeServers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78da1-222"><strong>ContentTypeID</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-222"><strong>ContentTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-223">int</span><span class="sxs-lookup"><span data-stu-id="78da1-223">int</span></span></p></td>
<td><p><span data-ttu-id="78da1-224">Fremd</span><span class="sxs-lookup"><span data-stu-id="78da1-224">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78da1-225">Inhaltstyp, der in der Sitzung verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="78da1-225">Content type used in the session.</span></span> <span data-ttu-id="78da1-226">Weitere Informationen finden Sie <a href="lync-server-2013-contenttypes-table.md">in der Tabelle "ContentTypes" in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="78da1-226">See the <a href="lync-server-2013-contenttypes-table.md">ContentTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78da1-227"><strong>Einladen</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-227"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-228">datetime</span><span class="sxs-lookup"><span data-stu-id="78da1-228">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78da1-229">Der Zeitpunkt der ersten INVITE-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="78da1-229">The time of the first INVITE request.</span></span> <span data-ttu-id="78da1-230">Dieses Feld wird in der Regel von Daten ausgefüllt, die aus der anfänglichen Einladungsnachricht in der Sitzung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="78da1-230">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="78da1-231">Wenn keine Einladungsnachricht vorhanden ist, wird das Feld mit dem Datum und der Uhrzeit der ersten relevanten SIP-Nachricht gefüllt (Bye, Cancel, Nachricht oder info).</span><span class="sxs-lookup"><span data-stu-id="78da1-231">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78da1-232"><strong>Webantworten</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-232"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-233">datetime</span><span class="sxs-lookup"><span data-stu-id="78da1-233">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78da1-234">Zeitpunkt der ersten SIP-Antwort.</span><span class="sxs-lookup"><span data-stu-id="78da1-234">Time of the first SIP RESPONSE.</span></span> <span data-ttu-id="78da1-235">Dieses Feld wird in der Regel von Daten ausgefüllt, die aus der anfänglichen Einladungsnachricht in der Sitzung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="78da1-235">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="78da1-236">Wenn keine Einladungsnachricht vorhanden ist, wird das Feld mit dem Datum und der Uhrzeit der ersten relevanten SIP-Nachricht gefüllt (Bye, Cancel, Nachricht oder info).</span><span class="sxs-lookup"><span data-stu-id="78da1-236">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78da1-237"><strong>SessionEndTime</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-237"><strong>SessionEndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-238">datetime</span><span class="sxs-lookup"><span data-stu-id="78da1-238">datetime</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78da1-239">Der Zeitpunkt, zu dem die Sitzung beendet wird.</span><span class="sxs-lookup"><span data-stu-id="78da1-239">The time when the session is ended.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78da1-240"><strong>UriTypeId</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-240"><strong>UriTypeId</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-241">tinyint</span><span class="sxs-lookup"><span data-stu-id="78da1-241">tinyint</span></span></p></td>
<td><p><span data-ttu-id="78da1-242">Fremd</span><span class="sxs-lookup"><span data-stu-id="78da1-242">Foreign</span></span></p></td>
<td><p><span data-ttu-id="78da1-243">Enthält den Wert des MCU-URI-Typs aus der <a href="lync-server-2013-uritypes-table.md">UriTypes-Tabelle in lync Server 2013</a>.</span><span class="sxs-lookup"><span data-stu-id="78da1-243">Contains the MCU URI type value from the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a>.</span></span> <span data-ttu-id="78da1-244">Dieses Feld wird verwendet, um die Abfrageleistung zu verbessern.</span><span class="sxs-lookup"><span data-stu-id="78da1-244">This field is used for improving query performance.</span></span></p>
<p><span data-ttu-id="78da1-245">Dieses Feld wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="78da1-245">This field was introduced in Microsoft Lync Server 2013.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="78da1-246"><strong>UserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-246"><strong>UserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-247">smallint</span><span class="sxs-lookup"><span data-stu-id="78da1-247">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78da1-248">Ein Bit-Satz, der die Benutzerattribute angibt.</span><span class="sxs-lookup"><span data-stu-id="78da1-248">A bit set that indicates the user attributes.</span></span> <span data-ttu-id="78da1-249">Die folgenden Attributdefinitionen werden aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="78da1-249">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="78da1-250">Integriert mit dem Desktop-Telefon-1</span><span class="sxs-lookup"><span data-stu-id="78da1-250">Integrated with desktop phone - 1</span></span></p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="78da1-251"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="78da1-251"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="78da1-252">smallint</span><span class="sxs-lookup"><span data-stu-id="78da1-252">smallint</span></span></p></td>
<td></td>
<td><p><span data-ttu-id="78da1-253">Ein Bit-Satz, der die anrufattribute angibt.</span><span class="sxs-lookup"><span data-stu-id="78da1-253">A bit set that indicates the call attributes.</span></span> <span data-ttu-id="78da1-254">Die folgenden Attributdefinitionen werden aufgelistet:</span><span class="sxs-lookup"><span data-stu-id="78da1-254">The following attribute definitions are listed:</span></span></p>
<ul>
<li><p><span data-ttu-id="78da1-255">Wiederholte Sitzung – 1</span><span class="sxs-lookup"><span data-stu-id="78da1-255">Retried Session - 1</span></span></p></li>
</ul></td>
</tr>
</tbody>
</table>


<span data-ttu-id="78da1-256">\* Bei den meisten Sitzungen erhält SessionIdSeq den Wert 1.</span><span class="sxs-lookup"><span data-stu-id="78da1-256">\* For most sessions, SessionIdSeq will have the value of 1.</span></span> <span data-ttu-id="78da1-257">Wenn mehrere Sitzungen genau zur gleichen Zeit beginnen, ist der SessionIdSeq für einen 1, für einen anderen wird 2 usw.</span><span class="sxs-lookup"><span data-stu-id="78da1-257">If multiple sessions start at exactly the same time, the SessionIdSeq for one will be 1, for another will be 2, and so on.</span></span>

<span data-ttu-id="78da1-258"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="78da1-258"></div>

<span> </span>

</div>

</div>

</span></span></div>

