---
title: 'Lync Server 2013: Registrierungs Ansicht'
description: 'Lync Server 2013: Registrierungs Ansicht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Registration view
ms:assetid: 8a42bc7d-3d4f-43c1-9e15-89b2ee419ade
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688120(v=OCS.15)
ms:contentKeyID: 49733718
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: be169cafc324f89cacedda154ca49a8ff1ff39aa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394347"
---
# <a name="registration-view-in-lync-server-2013"></a><span data-ttu-id="90161-103">Registrierungs Ansicht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="90161-103">Registration view in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="90161-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="90161-104">

<span> </span></span></span>

<span data-ttu-id="90161-105">_**Letztes Änderungsdatum des Themas:** 2012-10-01_</span><span class="sxs-lookup"><span data-stu-id="90161-105">_**Topic Last Modified:** 2012-10-01_</span></span>

<span data-ttu-id="90161-106">In der Registrierungs Ansicht werden Informationen zur Benutzerregistrierung gespeichert.</span><span class="sxs-lookup"><span data-stu-id="90161-106">The Registration view stores information about user registration.</span></span> <span data-ttu-id="90161-107">Diese Ansicht wurde in lync Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="90161-107">This view was introduced in Lync Server 2013.</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="90161-108">Spalte</span><span class="sxs-lookup"><span data-stu-id="90161-108">Column</span></span></th>
<th><span data-ttu-id="90161-109">Datentyp</span><span class="sxs-lookup"><span data-stu-id="90161-109">Data Type</span></span></th>
<th><span data-ttu-id="90161-110">Details</span><span class="sxs-lookup"><span data-stu-id="90161-110">Details</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="90161-111"><strong>SessionID</strong></span><span class="sxs-lookup"><span data-stu-id="90161-111"><strong>SessionIdTime</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-112">datetime</span><span class="sxs-lookup"><span data-stu-id="90161-112">datetime</span></span></p></td>
<td><p><span data-ttu-id="90161-113">Uhrzeit der Sitzungsanforderung.</span><span class="sxs-lookup"><span data-stu-id="90161-113">Time of session request.</span></span> <span data-ttu-id="90161-114">Wird in Verbindung mit SessionIdSeq verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="90161-114">Used in conjunction with SessionIdSeq to uniquely identify a session.</span></span> <span data-ttu-id="90161-115">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="90161-115">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90161-116"><strong>SessionIdSeq</strong></span><span class="sxs-lookup"><span data-stu-id="90161-116"><strong>SessionIdSeq</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-117">int</span><span class="sxs-lookup"><span data-stu-id="90161-117">int</span></span></p></td>
<td><p><span data-ttu-id="90161-118">Die ID-Nummer, um die Sitzung zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="90161-118">ID number to identify the session.</span></span> <span data-ttu-id="90161-119">Wird in Verbindung mit SessionID-Mal verwendet, um eine Sitzung eindeutig zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="90161-119">Used in conjunction with SessionIdTime to uniquely identify a session.</span></span> <span data-ttu-id="90161-120">Weitere Informationen finden Sie <a href="lync-server-2013-dialogs-table.md">in der Tabelle Dialogfelder in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="90161-120">See the <a href="lync-server-2013-dialogs-table.md">Dialogs table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90161-121"><strong>Registrierung</strong></span><span class="sxs-lookup"><span data-stu-id="90161-121"><strong>RegisterTime</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-122">datetime</span><span class="sxs-lookup"><span data-stu-id="90161-122">datetime</span></span></p></td>
<td><p><span data-ttu-id="90161-123">Zeitpunkt, zu dem die Registrierung erfolgte.</span><span class="sxs-lookup"><span data-stu-id="90161-123">Time at which registration occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90161-124"><strong>UserUri</strong></span><span class="sxs-lookup"><span data-stu-id="90161-124"><strong>UserUri</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-125">nvarchar (450)</span><span class="sxs-lookup"><span data-stu-id="90161-125">nvarchar(450)</span></span></p></td>
<td><p><span data-ttu-id="90161-126">URI des registrierten Benutzers.</span><span class="sxs-lookup"><span data-stu-id="90161-126">URI of the user who registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90161-127"><strong>UserUriType</strong></span><span class="sxs-lookup"><span data-stu-id="90161-127"><strong>UserUriType</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-128">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="90161-128">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="90161-129">Der Typ des URIs des registrierten Benutzers.</span><span class="sxs-lookup"><span data-stu-id="90161-129">Type of URI of the user who registered.</span></span> <span data-ttu-id="90161-130">Weitere Informationen finden Sie <a href="lync-server-2013-uritypes-table.md">in der UriTypes-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="90161-130">See the <a href="lync-server-2013-uritypes-table.md">UriTypes table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90161-131"><strong>UserTenant</strong></span><span class="sxs-lookup"><span data-stu-id="90161-131"><strong>UserTenant</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-132">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="90161-132">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="90161-133">Der Mandant des registrierten Benutzers.</span><span class="sxs-lookup"><span data-stu-id="90161-133">Tenant of the user who registered.</span></span> <span data-ttu-id="90161-134">Weitere Informationen finden Sie <a href="lync-server-2013-tenants-table.md">in der Tabelle Mandanten in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="90161-134">See the <a href="lync-server-2013-tenants-table.md">Tenants table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90161-135"><strong>EndpointId</strong></span><span class="sxs-lookup"><span data-stu-id="90161-135"><strong>EndpointId</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-136">uniqueidentifier</span><span class="sxs-lookup"><span data-stu-id="90161-136">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="90161-137">Eindeutiger Bezeichner des Endpunkts des Benutzers, bei dem registriert ist.</span><span class="sxs-lookup"><span data-stu-id="90161-137">Unique identifier of the endpoint of the user registered with.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90161-138"><strong>EndpointEra</strong></span><span class="sxs-lookup"><span data-stu-id="90161-138"><strong>EndpointEra</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-139">uniqueidentifier</span><span class="sxs-lookup"><span data-stu-id="90161-139">uniqueidentifier</span></span></p></td>
<td><p><span data-ttu-id="90161-140">Eindeutiger Bezeichner, der zur Unterscheidung von Registrierungen verwendet wird, die denselben Benutzer und denselben Endpunkt einbeziehen.</span><span class="sxs-lookup"><span data-stu-id="90161-140">Unique identifier used to differentiate registrations that involve the same user and the same endpoint.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90161-141"><strong>DeRegisterType</strong></span><span class="sxs-lookup"><span data-stu-id="90161-141"><strong>DeRegisterType</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-142">datetime</span><span class="sxs-lookup"><span data-stu-id="90161-142">datetime</span></span></p></td>
<td><p><span data-ttu-id="90161-143">Zeitpunkt, zu dem die Registrierung erfolgte.</span><span class="sxs-lookup"><span data-stu-id="90161-143">Time at which deregistration occurred.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90161-144"><strong>DeRegisterReason</strong></span><span class="sxs-lookup"><span data-stu-id="90161-144"><strong>DeRegisterReason</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-145">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="90161-145">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="90161-146">Grund für die Deregistrierung.</span><span class="sxs-lookup"><span data-stu-id="90161-146">Reason for deregistration.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90161-147"><strong>ClientVersion</strong></span><span class="sxs-lookup"><span data-stu-id="90161-147"><strong>ClientVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-148">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="90161-148">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="90161-149">Die Version des Clients, die von dem registrierten Benutzer verwendet wurde.</span><span class="sxs-lookup"><span data-stu-id="90161-149">Version of client used by the user who registered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90161-150"><strong>Clienttyp</strong></span><span class="sxs-lookup"><span data-stu-id="90161-150"><strong>ClientType</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-151">int</span><span class="sxs-lookup"><span data-stu-id="90161-151">int</span></span></p></td>
<td><p><span data-ttu-id="90161-152">Der Client, der von dem registrierten Benutzer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="90161-152">Client used by the user who registered.</span></span> <span data-ttu-id="90161-153">Weitere Informationen finden Sie <a href="lync-server-2013-useragentdef-table.md">in der UserAgentDef-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="90161-153">See the <a href="lync-server-2013-useragentdef-table.md">UserAgentDef table in Lync Server 2013</a> for more details.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90161-154"><strong>ClientCategory</strong></span><span class="sxs-lookup"><span data-stu-id="90161-154"><strong>ClientCategory</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-155">nvarchar (64)</span><span class="sxs-lookup"><span data-stu-id="90161-155">nvarchar(64)</span></span></p></td>
<td><p><span data-ttu-id="90161-156">Die Kategorie des Clients, der von dem registrierten Benutzer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="90161-156">Category of the client used by the user who registered.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90161-157"><strong>IPAddress</strong></span><span class="sxs-lookup"><span data-stu-id="90161-157"><strong>IpAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-158">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="90161-158">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="90161-159">Die IP-Adresse, bei der der Benutzer registriert ist.</span><span class="sxs-lookup"><span data-stu-id="90161-159">IP Address the user registered with.</span></span> <span data-ttu-id="90161-160">Dies kann eine IPv4-oder IPv6-Adresse sein.</span><span class="sxs-lookup"><span data-stu-id="90161-160">This may be an IPv4 or IPv6 address.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90161-161"><strong>Dialogfeld-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="90161-161"><strong>DialogId</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-162">varstring (775)</span><span class="sxs-lookup"><span data-stu-id="90161-162">varstring(775)</span></span></p></td>
<td><p><span data-ttu-id="90161-163">SIP-Dialogfeld-ID.</span><span class="sxs-lookup"><span data-stu-id="90161-163">SIP dialog ID.</span></span> <span data-ttu-id="90161-164">Das Format des is:</span><span class="sxs-lookup"><span data-stu-id="90161-164">The format of the is:</span></span></p>
<p><span data-ttu-id="90161-165">Dialogfeld; from-Tag; to-Tag</span><span class="sxs-lookup"><span data-stu-id="90161-165">dialog;from-tag;to-tag</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90161-166"><strong>Response Code</strong></span><span class="sxs-lookup"><span data-stu-id="90161-166"><strong>ResponseCode</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-167">int</span><span class="sxs-lookup"><span data-stu-id="90161-167">int</span></span></p></td>
<td><p><span data-ttu-id="90161-168">SIP-Antwortcode für die Sitzungseinladung</span><span class="sxs-lookup"><span data-stu-id="90161-168">SIP response code to the session invitation.</span></span> <span data-ttu-id="90161-169">Dieses Feld wird in der Regel von Daten ausgefüllt, die aus der anfänglichen Einladungsnachricht in der Sitzung generiert wurden.</span><span class="sxs-lookup"><span data-stu-id="90161-169">This field is typically populated by data generated from the initial INVITE message in the session.</span></span> <span data-ttu-id="90161-170">Wenn keine Einladungsnachricht vorhanden ist, wird das Feld mit dem Datum und der Uhrzeit der ersten relevanten SIP-Nachricht gefüllt (Bye, Cancel, Nachricht oder info).</span><span class="sxs-lookup"><span data-stu-id="90161-170">If there is no INVITE message then the field is populated with the date and time of the first relevant SIP message (BYE, CANCEL, MESSAGE, or INFO).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90161-171"><strong>Diagnose-Nr</strong></span><span class="sxs-lookup"><span data-stu-id="90161-171"><strong>DiagnosticId</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-172">int</span><span class="sxs-lookup"><span data-stu-id="90161-172">int</span></span></p></td>
<td><p><span data-ttu-id="90161-173">Vom SIP-Header erfasste Diagnose-ID.</span><span class="sxs-lookup"><span data-stu-id="90161-173">Diagnostic ID captured from SIP header.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90161-174"><strong>Registrierungsstelle</strong></span><span class="sxs-lookup"><span data-stu-id="90161-174"><strong>Registrar</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-175">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="90161-175">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="90161-176">FQDN der Registrierungsstelle.</span><span class="sxs-lookup"><span data-stu-id="90161-176">FQDN of the Registrar.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90161-177"><strong>Pool</strong></span><span class="sxs-lookup"><span data-stu-id="90161-177"><strong>Pool</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-178">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="90161-178">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="90161-179">Der FQDN des Pools, in dem die Daten für die Sitzung erfasst wurden.</span><span class="sxs-lookup"><span data-stu-id="90161-179">FQDN of the pool that captured the data for the session.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90161-180"><strong>EdgeServer</strong></span><span class="sxs-lookup"><span data-stu-id="90161-180"><strong>EdgeServer</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-181">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="90161-181">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="90161-182">Der FQDN des Edge-Servers, der von dem registrierten Benutzer verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="90161-182">FQDN of the Edge Server used by the user who registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90161-183"><strong>"IsInternal</strong></span><span class="sxs-lookup"><span data-stu-id="90161-183"><strong>IsInternal</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-184">bit</span><span class="sxs-lookup"><span data-stu-id="90161-184">bit</span></span></p></td>
<td><p><span data-ttu-id="90161-185">Gibt an, ob sich der Benutzer vom internen Netzwerk anmeldet.</span><span class="sxs-lookup"><span data-stu-id="90161-185">Indicates whether the user logged on from the internal network.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90161-186"><strong>IsUserServiceAvailable</strong></span><span class="sxs-lookup"><span data-stu-id="90161-186"><strong>IsUserServiceAvailable</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-187">bit</span><span class="sxs-lookup"><span data-stu-id="90161-187">bit</span></span></p></td>
<td><p><span data-ttu-id="90161-188">Gibt an, ob die UserService zur Registrierungszeit verfügbar war.</span><span class="sxs-lookup"><span data-stu-id="90161-188">Indicates whether the UserService was available at registration time.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90161-189"><strong>IsPrimaryRegistrar</strong></span><span class="sxs-lookup"><span data-stu-id="90161-189"><strong>IsPrimaryRegistrar</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-190">bit</span><span class="sxs-lookup"><span data-stu-id="90161-190">bit</span></span></p></td>
<td><p><span data-ttu-id="90161-191">Gibt an, ob die Registrierung bei der primären Registrierungsstelle erfolgte.</span><span class="sxs-lookup"><span data-stu-id="90161-191">Indicates whether registration was with the primary Registrar.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90161-192"><strong>DeviceMacAddress</strong></span><span class="sxs-lookup"><span data-stu-id="90161-192"><strong>DeviceMacAddress</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-193">bigint</span><span class="sxs-lookup"><span data-stu-id="90161-193">bigint</span></span></p></td>
<td><p><span data-ttu-id="90161-194">Mac-Adresse des registrierten Geräts.</span><span class="sxs-lookup"><span data-stu-id="90161-194">MAC Address of device registered.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="90161-195"><strong>DeviceManufacturer</strong></span><span class="sxs-lookup"><span data-stu-id="90161-195"><strong>DeviceManufacturer</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-196">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="90161-196">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="90161-197">Hersteller des registrierten Geräts.</span><span class="sxs-lookup"><span data-stu-id="90161-197">Manufacturer of the device registered.</span></span> <span data-ttu-id="90161-198">Weitere Informationen finden Sie <a href="lync-server-2013-manufacturers-table.md">in der Tabelle "Hersteller" in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="90161-198">See the <a href="lync-server-2013-manufacturers-table.md">Manufacturers table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="90161-199"><strong>DeviceHardwareVersion</strong></span><span class="sxs-lookup"><span data-stu-id="90161-199"><strong>DeviceHardwareVersion</strong></span></span></p></td>
<td><p><span data-ttu-id="90161-200">nvarchar(256)</span><span class="sxs-lookup"><span data-stu-id="90161-200">nvarchar(256)</span></span></p></td>
<td><p><span data-ttu-id="90161-201">Hardware Version des registrierten Geräts.</span><span class="sxs-lookup"><span data-stu-id="90161-201">Hardware version of the device registered.</span></span> <span data-ttu-id="90161-202">Weitere Informationen finden Sie <a href="lync-server-2013-hardwareversions-table.md">in der HardwareVersions-Tabelle in lync Server 2013</a> .</span><span class="sxs-lookup"><span data-stu-id="90161-202">See the <a href="lync-server-2013-hardwareversions-table.md">HardwareVersions table in Lync Server 2013</a> for more information.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="90161-203">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="90161-203">


</div>

<span> </span>

</div>

</div>

</span></span></div>

