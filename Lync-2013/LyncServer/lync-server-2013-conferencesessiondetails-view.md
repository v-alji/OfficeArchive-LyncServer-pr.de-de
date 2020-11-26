---
title: 'Lync Server 2013: ConferenceSessionDetails-Ansicht'
description: 'Lync Server 2013: ConferenceSessionDetails-Ansicht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: ConferenceSessionDetails view
ms:assetid: 5858c84d-baed-421d-ad1d-3726e150e256
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688066(v=OCS.15)
ms:contentKeyID: 49733660
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: d1c62f020413efecdbc0f909618256ccc7308d4f
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434396"
---
# <a name="conferencesessiondetails-view-in-lync-server-2013"></a><span data-ttu-id="56904-103">ConferenceSessionDetails-Ansicht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="56904-103">ConferenceSessionDetails view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="56904-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="56904-104">

<span> </span></span></span>

<span data-ttu-id="56904-105">_**Letztes Änderungsdatum des Themas:** 2012-11-12_</span><span class="sxs-lookup"><span data-stu-id="56904-105">_**Topic Last Modified:** 2012-11-12_</span></span>

<span data-ttu-id="56904-106">In der ConferenceSessionDetails-Ansicht werden Informationen zu mehrteiligen Sitzungen gespeichert.</span><span class="sxs-lookup"><span data-stu-id="56904-106">The ConferenceSessionDetails view stores information about multiparty sessions.</span></span> <span data-ttu-id="56904-107">Jeder Datensatz stellt eine Konferenzsitzung dar, bei der es sich entweder um die Sitzung mit dem Fokus oder um die Sitzung mit einem bestimmten Konferenzserver handeln kann.</span><span class="sxs-lookup"><span data-stu-id="56904-107">Each record represents one conference session, which could be either the session with Focus or the session with a specific conferencing server.</span></span> <span data-ttu-id="56904-108">Diese Ansicht wurde in Microsoft lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="56904-108">This view was introduced in Microsoft Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="56904-109">Spalte</span><span class="sxs-lookup"><span data-stu-id="56904-109">Column</span></span></th>
<th><span data-ttu-id="56904-110">Datentyp</span><span class="sxs-lookup"><span data-stu-id="56904-110">Data Type</span></span></th>
<th><span data-ttu-id="56904-111">Details</span><span class="sxs-lookup"><span data-stu-id="56904-111">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="56904-112"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="56904-112"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-113">datetime</span><span class="sxs-lookup"><span data-stu-id="56904-113">datetime</span></span></p></td>
<td><p><span data-ttu-id="56904-114">Uhrzeit der Sitzungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="56904-114">Time of session request.</span></span> <span data-ttu-id="56904-115">Wird in Verbindung mit SessionIdSeq verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="56904-115">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="56904-116">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="56904-116">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-117"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="56904-117"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-118">int</span><span class="sxs-lookup"><span data-stu-id="56904-118">int</span></span></p></td>
<td><p><span data-ttu-id="56904-119">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="56904-119">ID number to identify the session.</span></span> <span data-ttu-id="56904-120">Wird in Verbindung mit SessionID-Mal verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="56904-120">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="56904-121">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="56904-121">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-122"><strong>Einladen</strong></span><span class="sxs-lookup"><span data-stu-id="56904-122"><strong>InviteTime</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-123">datetime</span><span class="sxs-lookup"><span data-stu-id="56904-123">datetime</span></span></p></td>
<td><p><span data-ttu-id="56904-124">Uhrzeit der ersten INVITE-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="56904-124">Time of the first INVITE request.</span></span> <span data-ttu-id="56904-125">Dieses Feld wird in der Regel von Daten ausgefüllt, die aus der anfänglichen Einladungsnachricht in der Sitzung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="56904-125">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="56904-126">Wenn keine Einladungsnachricht vorhanden ist, wird das Feld mit dem Datum und der Uhrzeit der ersten relevanten SIP-Nachricht gefüllt (Bye, Cancel, Nachricht oder info).</span><span class="sxs-lookup"><span data-stu-id="56904-126">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-127"><strong>ConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="56904-127"><strong>ConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-128">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="56904-128">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="56904-129">URI der Konferenz.</span><span class="sxs-lookup"><span data-stu-id="56904-129">URI of the conference.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-130"><strong>ConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="56904-130"><strong>ConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-131">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="56904-131">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="56904-132">Typ des Konferenz-URI.</span><span class="sxs-lookup"><span data-stu-id="56904-132">Type of conference URI.</span></span> <span data-ttu-id="56904-133">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="56904-133">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-134"><strong>ConfInstance</strong></span><span class="sxs-lookup"><span data-stu-id="56904-134"><strong>ConfInstance</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-135">uniqueidentifier</span><span class="sxs-lookup"><span data-stu-id="56904-135">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="56904-136">Bezeichner, der zwischen Instanzen von wiederkehrenden Konferenzen unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="56904-136">Identifier that differentiates between instances of recurring conferences.</span></span> <span data-ttu-id="56904-137">Jede wiederkehrende Konferenz Instanz hat dieselbe ConferenceURI, aber einen anderen ConfInstance-Wert.</span><span class="sxs-lookup"><span data-stu-id="56904-137">Each recurring conference instance has the same ConferenceURI but a different ConfInstance value.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-138"><strong>McuConferenceUri</strong></span><span class="sxs-lookup"><span data-stu-id="56904-138"><strong>McuConferenceUri</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-139">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="56904-139">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="56904-140">URI des Konferenzservers</span><span class="sxs-lookup"><span data-stu-id="56904-140">URI of the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-141"><strong>McuConferenceUriType</strong></span><span class="sxs-lookup"><span data-stu-id="56904-141"><strong>McuConferenceUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-142">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="56904-142">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="56904-143">Der Typ des Konferenzserver-URIs.</span><span class="sxs-lookup"><span data-stu-id="56904-143">Type of conferencing server URI.</span></span> <span data-ttu-id="56904-144">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="56904-144">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-145"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="56904-145"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-146">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="56904-146">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="56904-147">Der URI des an der Sitzung beteiligten Benutzers.</span><span class="sxs-lookup"><span data-stu-id="56904-147">URI of the user involved in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-148"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="56904-148"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-149">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="56904-149">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="56904-150">Der Typ des URIs des Benutzers, dessen Teil der Sitzung war.</span><span class="sxs-lookup"><span data-stu-id="56904-150">Type of URI of the user whose was part of the session.</span></span> <span data-ttu-id="56904-151">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="56904-151">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-152"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="56904-152"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-153">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="56904-153">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="56904-154">Der Mandant des Benutzers, dessen Teil der Sitzung war.</span><span class="sxs-lookup"><span data-stu-id="56904-154">Tenant of the user whose was part of the session.</span></span> <span data-ttu-id="56904-155">Weitere Informationen finden Sie <a href="lync-server-2013-tenants-table.md">in der Tabelle Mandanten in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="56904-155">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-156"><strong>UserEndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="56904-156"><strong>UserEndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-157">uniqueidentifier</span><span class="sxs-lookup"><span data-stu-id="56904-157">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="56904-158">Eindeutiger Bezeichner des Benutzers, dessen Teil der Sitzung war.</span><span class="sxs-lookup"><span data-stu-id="56904-158">Unique identifier of the user whose was part of the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-159"><strong>EndTime</strong></span><span class="sxs-lookup"><span data-stu-id="56904-159"><strong>EndTime</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-160">datetime</span><span class="sxs-lookup"><span data-stu-id="56904-160">datetime</span></span></p></td>
<td><p><span data-ttu-id="56904-161">Endzeit der Sitzung.</span><span class="sxs-lookup"><span data-stu-id="56904-161">End time of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-162"><strong>ConferenceClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="56904-162"><strong>ConferenceClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-163">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="56904-163">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="56904-164">Version des Konferenzservers</span><span class="sxs-lookup"><span data-stu-id="56904-164">Version of conference server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-165"><strong>ConferenceClientType</strong></span><span class="sxs-lookup"><span data-stu-id="56904-165"><strong>ConferenceClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-166">int</span><span class="sxs-lookup"><span data-stu-id="56904-166">int</span></span></p></td>
<td><p><span data-ttu-id="56904-167">Der Typ des Konferenzservers.</span><span class="sxs-lookup"><span data-stu-id="56904-167">Type of conference server.</span></span> <span data-ttu-id="56904-168">Weitere Informationen finden Sie <a href="lync-server-2013-useragentdef-table.md">in der UserAgentDef-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="56904-168">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-169"><strong>ConferenceCategory</strong></span><span class="sxs-lookup"><span data-stu-id="56904-169"><strong>ConferenceCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-170">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="56904-170">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="56904-171">Konferenzserver Kategorie.</span><span class="sxs-lookup"><span data-stu-id="56904-171">Conference server category.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-172"><strong>UserClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="56904-172"><strong>UserClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-173">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="56904-173">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="56904-174">Die Version des Clients, die von dem Benutzer verwendet wird, der an der Sitzung teilgenommen hat.</span><span class="sxs-lookup"><span data-stu-id="56904-174">Version of client used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-175"><strong>UserClientType</strong></span><span class="sxs-lookup"><span data-stu-id="56904-175"><strong>UserClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-176">int</span><span class="sxs-lookup"><span data-stu-id="56904-176">int</span></span></p></td>
<td><p><span data-ttu-id="56904-177">Der Client, der von dem Benutzer verwendet wird, der an der Sitzung teilgenommen hat.</span><span class="sxs-lookup"><span data-stu-id="56904-177">Client used by the user who participated in the session.</span></span> <span data-ttu-id="56904-178">Weitere Informationen finden Sie <a href="lync-server-2013-useragentdef-table.md">in der UserAgentDef-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="56904-178">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-179"><strong>UserClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="56904-179"><strong>UserClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-180">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="56904-180">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="56904-181">Der Name der Kategorie des Clients, der von dem Benutzer verwendet wurde, der Teil der Sitzung war.</span><span class="sxs-lookup"><span data-stu-id="56904-181">Name of the category of the client used by the user who was part of the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-182"><strong>OnBehalfOfUri</strong></span><span class="sxs-lookup"><span data-stu-id="56904-182"><strong>OnBehalfOfUri</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-183">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="56904-183">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="56904-184">Der URI des Benutzers, in dessen Auftrag die Sitzung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="56904-184">URI of the user on whose behalf the session was started.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-185"><strong>OnBehalfOfUriType</strong></span><span class="sxs-lookup"><span data-stu-id="56904-185"><strong>OnBehalfOfUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-186">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="56904-186">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="56904-187">Der Typ des URIs des Benutzers, in dessen Auftrag die Sitzung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="56904-187">Type of URI of the user on whose behalf the session was started.</span></span> <span data-ttu-id="56904-188">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="56904-188">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-189"><strong>OnBehalfOfTenant</strong></span><span class="sxs-lookup"><span data-stu-id="56904-189"><strong>OnBehalfOfTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-190">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="56904-190">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="56904-191">Der Mandant des Benutzers, dessen Namen für die Sitzung gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="56904-191">Tenant of the user whose on behalf the session was started.</span></span> <span data-ttu-id="56904-192">Weitere Informationen finden Sie <a href="lync-server-2013-tenants-table.md">in der Tabelle Mandanten in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="56904-192">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-193"><strong>ReferredByUri</strong></span><span class="sxs-lookup"><span data-stu-id="56904-193"><strong>ReferredByUri</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-194">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="56904-194">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="56904-195">Der URI des Benutzers, der die Sitzung angewiesen hat.</span><span class="sxs-lookup"><span data-stu-id="56904-195">URI of the user who referred the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-196"><strong>ReferredByUriType</strong></span><span class="sxs-lookup"><span data-stu-id="56904-196"><strong>ReferredByUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-197">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="56904-197">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="56904-198">Der Typ des URIs des Benutzers, der die Sitzung angewiesen hat.</span><span class="sxs-lookup"><span data-stu-id="56904-198">Type of URI of the user who referred the session.</span></span> <span data-ttu-id="56904-199">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="56904-199">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-200"><strong>ReferredByUriTenant</strong></span><span class="sxs-lookup"><span data-stu-id="56904-200"><strong>ReferredByUriTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-201">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="56904-201">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="56904-202">Der Mandant des Benutzers, der die Sitzung angewiesen hat.</span><span class="sxs-lookup"><span data-stu-id="56904-202">Tenant of the user who referred the session.</span></span> <span data-ttu-id="56904-203">Weitere Informationen finden Sie <a href="lync-server-2013-tenants-table.md">in der Tabelle Mandanten in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="56904-203">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-204"><strong>Dialogfeld-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="56904-204"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-205">varstring (775)</span><span class="sxs-lookup"><span data-stu-id="56904-205">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="56904-206">SIP-Dialogfeld-ID.</span><span class="sxs-lookup"><span data-stu-id="56904-206">SIP dialog ID.</span></span> <span data-ttu-id="56904-207">Das Format ist</span><span class="sxs-lookup"><span data-stu-id="56904-207">The format is</span></span></p>
<p><span data-ttu-id="56904-208">:d ialog; from-Tag; to-Tag</span><span class="sxs-lookup"><span data-stu-id="56904-208">:dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-209"><strong>ReplaceDialogIdTime</strong></span><span class="sxs-lookup"><span data-stu-id="56904-209"><strong>ReplaceDialogIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-210">datetime</span><span class="sxs-lookup"><span data-stu-id="56904-210">datetime</span></span></p></td>
<td><p><span data-ttu-id="56904-211">Die ID-Nummer, die das Dialogfeld identifiziert, das durch die aktuelle Sitzung ersetzt wurde.</span><span class="sxs-lookup"><span data-stu-id="56904-211">ID number to identify the dialog which was replaced by current session.</span></span> <span data-ttu-id="56904-212">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="56904-212">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-213"><strong>ReplaceDialogIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="56904-213"><strong>ReplaceDialogIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-214">int</span><span class="sxs-lookup"><span data-stu-id="56904-214">int</span></span></p></td>
<td><p><span data-ttu-id="56904-215">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="56904-215">ID number to identify the session.</span></span> <span data-ttu-id="56904-216">Wird in Verbindung mit ReplaceDialogIdTime verwendet, um eine Sitzung, die durch diese Sitzung ersetzt wird, eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="56904-216">Used in conjunction with ReplaceDialogIdTime to uniquely identify a session that is replaced by this session.</span></span> <span data-ttu-id="56904-217">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="56904-217">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-218"><strong>ReplacesDialogId</strong></span><span class="sxs-lookup"><span data-stu-id="56904-218"><strong>ReplacesDialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-219">varchar (775)</span><span class="sxs-lookup"><span data-stu-id="56904-219">varchar(775)</span></span></p></td>
<td><p><span data-ttu-id="56904-220">SIP-Dialog-ID, die die Sitzung ersetzt.</span><span class="sxs-lookup"><span data-stu-id="56904-220">SIP dialog ID the session replaces.</span></span> <span data-ttu-id="56904-221">Das Format des is:</span><span class="sxs-lookup"><span data-stu-id="56904-221">The format of the is:</span></span></p>
<p><span data-ttu-id="56904-222">Dialogfeld; from-Tag; to-Tag</span><span class="sxs-lookup"><span data-stu-id="56904-222">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-223"><strong>IsStartedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="56904-223"><strong>IsStartedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-224">bit</span><span class="sxs-lookup"><span data-stu-id="56904-224">bit</span></span></p></td>
<td><p><span data-ttu-id="56904-225">Gibt an, ob die Sitzung vom Konferenzserver gestartet wurde.</span><span class="sxs-lookup"><span data-stu-id="56904-225">Indicates whether the session was started by the conferencing server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-226"><strong>IsEndedByConfServer</strong></span><span class="sxs-lookup"><span data-stu-id="56904-226"><strong>IsEndedByConfServer</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-227">bit</span><span class="sxs-lookup"><span data-stu-id="56904-227">bit</span></span></p></td>
<td><p><span data-ttu-id="56904-228">Gibt an, ob die Sitzung vom Konferenzserver beendet wurde.</span><span class="sxs-lookup"><span data-stu-id="56904-228">Indicates whether the session was ended by the conferencing server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-229"><strong>IsUserInternal</strong></span><span class="sxs-lookup"><span data-stu-id="56904-229"><strong>IsUserInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-230">bit</span><span class="sxs-lookup"><span data-stu-id="56904-230">bit</span></span></p></td>
<td><p><span data-ttu-id="56904-231">Gibt an, ob sich der Benutzer vom internen Netzwerk anmeldet.</span><span class="sxs-lookup"><span data-stu-id="56904-231">Indicates whether the user logged on from the internal network.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-232"><strong>Webantworten</strong></span><span class="sxs-lookup"><span data-stu-id="56904-232"><strong>ResponseTime</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-233">datetime</span><span class="sxs-lookup"><span data-stu-id="56904-233">datetime</span></span></p></td>
<td><p><span data-ttu-id="56904-234">Zeitpunkt der Antwort auf die erste Einladungsnachricht.</span><span class="sxs-lookup"><span data-stu-id="56904-234">Time of the response to the first INVITE message.</span></span> <span data-ttu-id="56904-235">Dieses Feld wird in der Regel von Daten ausgefüllt, die aus der anfänglichen Einladungsnachricht in der Sitzung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="56904-235">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="56904-236">Wenn keine Einladungsnachricht vorhanden ist, wird das Feld mit dem Datum und der Uhrzeit der ersten relevanten SIP-Nachricht gefüllt (Bye, Cancel, Nachricht oder info).</span><span class="sxs-lookup"><span data-stu-id="56904-236">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-237"><strong>Response Code</strong></span><span class="sxs-lookup"><span data-stu-id="56904-237"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-238">int</span><span class="sxs-lookup"><span data-stu-id="56904-238">int</span></span></p></td>
<td><p><span data-ttu-id="56904-239">SIP-Antwortcode für die Sitzungseinladung</span><span class="sxs-lookup"><span data-stu-id="56904-239">SIP response code to the session invitation.</span></span> <span data-ttu-id="56904-240">Dieses Feld wird in der Regel von Daten ausgefüllt, die aus der anfänglichen Einladungsnachricht in der Sitzung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="56904-240">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="56904-241">Wenn keine Einladungsnachricht vorhanden ist, wird das Feld mit dem Datum und der Uhrzeit der ersten relevanten SIP-Nachricht gefüllt (Bye, Cancel, Nachricht oder info).</span><span class="sxs-lookup"><span data-stu-id="56904-241">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-242"><strong>Diagnose-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="56904-242"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-243">int</span><span class="sxs-lookup"><span data-stu-id="56904-243">int</span></span></p></td>
<td><p><span data-ttu-id="56904-244">Diagnose-ID, die aus Sitzungs-SIP-Headern erfasst wird.</span><span class="sxs-lookup"><span data-stu-id="56904-244">Diagnostic ID captured from session SIP headers.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-245"><strong>ContentType</strong></span><span class="sxs-lookup"><span data-stu-id="56904-245"><strong>ContentType</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-246">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="56904-246">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="56904-247">Inhaltstyp für die Sitzung.</span><span class="sxs-lookup"><span data-stu-id="56904-247">Content type for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-248"><strong>FrontEnd</strong></span><span class="sxs-lookup"><span data-stu-id="56904-248"><strong>FrontEnd</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-249">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="56904-249">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="56904-250">FQDN des Front-End-Servers, der die Daten für die Sitzung erfasst hat.</span><span class="sxs-lookup"><span data-stu-id="56904-250">FQDN of the Front End server that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-251"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="56904-251"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-252">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="56904-252">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="56904-253">Der FQDN des Pools, in dem die Daten für die Sitzung erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="56904-253">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-254"><strong>MediationServer</strong></span><span class="sxs-lookup"><span data-stu-id="56904-254"><strong>MediationServer</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-255">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="56904-255">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="56904-256">Vermittlungs Server, der von dem Benutzer verwendet wird, der an der Sitzung teilgenommen hat.</span><span class="sxs-lookup"><span data-stu-id="56904-256">Mediation Server used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-257"><strong>Gateway</strong></span><span class="sxs-lookup"><span data-stu-id="56904-257"><strong>Gateway</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-258">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="56904-258">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="56904-259">Gateway, das vom Benutzer verwendet wird, der an der Sitzung teilgenommen hat.</span><span class="sxs-lookup"><span data-stu-id="56904-259">Gateway used by the user who participated the session.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-260"><strong>EdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="56904-260"><strong>EdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-261">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="56904-261">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="56904-262">Der FQDN des Edge-Servers, der von dem Benutzer verwendet wird, der an der Sitzung teilgenommen hat.</span><span class="sxs-lookup"><span data-stu-id="56904-262">FQDN of the Edge server used by the user who participated in the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="56904-263"><strong>UserFlag</strong></span><span class="sxs-lookup"><span data-stu-id="56904-263"><strong>UserFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-264">smallint</span><span class="sxs-lookup"><span data-stu-id="56904-264">smallint</span></span></p></td>
<td><p><span data-ttu-id="56904-265">Gibt die Attribute des Benutzers an, der an der Sitzung teilgenommen hat.</span><span class="sxs-lookup"><span data-stu-id="56904-265">Indicates the attributes of the user who participated in the session.</span></span> <span data-ttu-id="56904-266">Die folgenden Attributdefinitionen sind zulässig:</span><span class="sxs-lookup"><span data-stu-id="56904-266">The following attribute definitions allowed:</span></span></p>
<p><span data-ttu-id="56904-267">0x01-integriert mit dem Desktoptelefon</span><span class="sxs-lookup"><span data-stu-id="56904-267">0x01 - Integrated with desktop phone</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="56904-268"><strong>CallFlag</strong></span><span class="sxs-lookup"><span data-stu-id="56904-268"><strong>CallFlag</strong></span></span></p></td>
<td><p><span data-ttu-id="56904-269">smallint</span><span class="sxs-lookup"><span data-stu-id="56904-269">smallint</span></span></p></td>
<td><p><span data-ttu-id="56904-270">Gibt die anrufattribute an.</span><span class="sxs-lookup"><span data-stu-id="56904-270">Indicates the call attributes.</span></span> <span data-ttu-id="56904-271">Die folgenden Attributdefinitionen sind zulässig:</span><span class="sxs-lookup"><span data-stu-id="56904-271">The following attribute definitions are allowed:</span></span></p>
<p><span data-ttu-id="56904-272">0x01 – wiederholte Session0</span><span class="sxs-lookup"><span data-stu-id="56904-272">0x01 - Retried Session0</span></span></p>
<p><span data-ttu-id="56904-273">x02 – ein Anruf, der von einem Agenten im Auftrag einer Reaktionsgruppe durchgeführt wurde</span><span class="sxs-lookup"><span data-stu-id="56904-273">x02 - A call made by agent on behalf of a Response Group</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="56904-274">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="56904-274">


</div>

<span> </span>

</div>

</div>

</span></span></div>

