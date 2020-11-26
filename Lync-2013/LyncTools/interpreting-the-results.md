---
title: Interpretieren der Ergebnisse
description: Interpretieren der Ergebnisse
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Interpreting the Results
ms:assetid: dd7f199f-7075-4d88-bb84-49a7e05eb593
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945608(v=OCS.15)
ms:contentKeyID: 51541433
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b8342a1ec1e15e42852fc5293f87342e98587a60
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49443174"
---
# <a name="interpreting-the-results"></a><span data-ttu-id="bf089-103">Interpretieren der Ergebnisse</span><span class="sxs-lookup"><span data-stu-id="bf089-103">Interpreting the Results</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bf089-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bf089-104">

<span> </span></span></span>

<span data-ttu-id="bf089-105">_**Letztes Änderungsdatum des Themas:** 2013-02-24_</span><span class="sxs-lookup"><span data-stu-id="bf089-105">_**Topic Last Modified:** 2013-02-24_</span></span>

<span data-ttu-id="bf089-106">Das lync Server 2013-Stress-und-Leistungs Tool (LyncPerfTool.exe) bietet zahlreiche Leistungsindikatoren, mit denen Sie verstehen können, was der Client tut und ob Probleme auftreten.</span><span class="sxs-lookup"><span data-stu-id="bf089-106">The Lync Server 2013 Stress and Performance Tool (LyncPerfTool.exe) has many counters that you can use to understand what the client is doing and whether it is encountering issues.</span></span>

<div>

## <a name="client-counters"></a><span data-ttu-id="bf089-107">Client-Leistungsindikatoren</span><span class="sxs-lookup"><span data-stu-id="bf089-107">Client Counters</span></span>

<span data-ttu-id="bf089-108">Jede Instanz von LyncPerfTool.exe, die ausgeführt wird, verfügt über eine separate Instanz der Leistungsindikatoren.</span><span class="sxs-lookup"><span data-stu-id="bf089-108">Each instance of LyncPerfTool.exe that is running has a separate instance of the counters.</span></span> <span data-ttu-id="bf089-109">Jede Instanz wird durch ihre Prozess-ID benannt.</span><span class="sxs-lookup"><span data-stu-id="bf089-109">Each instance is named by its process ID.</span></span>

<span data-ttu-id="bf089-110">Wenn die Clients überladen sind, können Probleme auftreten.</span><span class="sxs-lookup"><span data-stu-id="bf089-110">If the clients are overloaded, issues can occur.</span></span> <span data-ttu-id="bf089-111">Gehen Sie wie folgt vor, um diese Probleme zu vermeiden:</span><span class="sxs-lookup"><span data-stu-id="bf089-111">To prevent these issues, do the following:</span></span>

1.  <span data-ttu-id="bf089-112">Überwachen Sie die CPU und die Speicherauslastung auf den Clientcomputern.</span><span class="sxs-lookup"><span data-stu-id="bf089-112">Monitor the CPU and the memory usage on the client computers.</span></span> <span data-ttu-id="bf089-113">Wenn die CPU konstant über 90 Prozent liegt, verringern Sie die Anzahl der Benutzer.</span><span class="sxs-lookup"><span data-stu-id="bf089-113">If the CPU is consistently above 90 percent, reduce the number of users.</span></span>

2.  <span data-ttu-id="bf089-114">Bei einem hohen Speicherbedarf können Probleme auftreten, wenn die Auslagerungsdatei nicht groß genug ist.</span><span class="sxs-lookup"><span data-stu-id="bf089-114">If the memory footprint is high, you could run into issues if the page file is not big enough.</span></span> <span data-ttu-id="bf089-115">Überprüfen Sie, ob die Commit-Belastung auf dem Computer nicht auf das Limit trifft.</span><span class="sxs-lookup"><span data-stu-id="bf089-115">Verify that the Commit Charge is not hitting the limit on the computer.</span></span> <span data-ttu-id="bf089-116">Wenn Sie Speichergrenzwerte verwenden, können Sie die Größe der Auslagerungsdatei erhöhen oder die Anzahl der Benutzer reduzieren.</span><span class="sxs-lookup"><span data-stu-id="bf089-116">If you are running into memory limits, consider increasing the page file size or reducing the number of users</span></span>

<span data-ttu-id="bf089-117">In den folgenden Tabellen sind die wichtigsten LyncPerfTool-Leistungsindikatoren aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="bf089-117">The following tables list the key LyncPerfTool performance counters.</span></span>

<span data-ttu-id="bf089-118">**Allgemeine Informationen**</span><span class="sxs-lookup"><span data-stu-id="bf089-118">**General Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf089-119"><strong>Leistungsindikator</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-119"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bf089-120"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-120"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf089-121">In Minuten verbrachte Zeit</span><span class="sxs-lookup"><span data-stu-id="bf089-121">Time Spent in Minutes</span></span></p></td>
<td><p><span data-ttu-id="bf089-122">Die Zeit, die seit dem Start des Prozesses aufgewendet wurde.</span><span class="sxs-lookup"><span data-stu-id="bf089-122">Time spent since the process was started.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-123">Aktive Endpunkte</span><span class="sxs-lookup"><span data-stu-id="bf089-123">Active Endpoints</span></span></p></td>
<td><p><span data-ttu-id="bf089-124">Die Anzahl der Endpunkte, die derzeit mit dem Server verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="bf089-124">Number of endpoints currently connected to the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf089-125">Fehlgeschlagene Anmeldungen</span><span class="sxs-lookup"><span data-stu-id="bf089-125">Failed Logons</span></span></p></td>
<td><p><span data-ttu-id="bf089-126">Die Gesamtzahl der Endpunkt Anmeldungsfehler.</span><span class="sxs-lookup"><span data-stu-id="bf089-126">Total number of endpoint sign-in failures.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-127">Anmeldeversuche</span><span class="sxs-lookup"><span data-stu-id="bf089-127">Logon Attempts</span></span></p></td>
<td><p><span data-ttu-id="bf089-128">Die Gesamtzahl der Endpunkt Anmeldeversuche.</span><span class="sxs-lookup"><span data-stu-id="bf089-128">Total number of endpoint sign-in attempts.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf089-129">Endpunkte getrennt</span><span class="sxs-lookup"><span data-stu-id="bf089-129">Endpoints Disconnected</span></span></p></td>
<td><p><span data-ttu-id="bf089-130">Die Gesamtzahl der Endpunkte, die getrennt wurden.</span><span class="sxs-lookup"><span data-stu-id="bf089-130">Total number of endpoints that have been disconnected.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf089-131">**Anwesenheitsinformationen**</span><span class="sxs-lookup"><span data-stu-id="bf089-131">**Presence Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf089-132"><strong>Leistungsindikator</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-132"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bf089-133"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-133"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf089-134">SetPresence-Anrufe</span><span class="sxs-lookup"><span data-stu-id="bf089-134">SetPresence Calls</span></span></p></td>
<td><p><span data-ttu-id="bf089-135">Die Gesamtzahl der Anwesenheits Änderungsversuche.</span><span class="sxs-lookup"><span data-stu-id="bf089-135">Total number of presence change attempts.</span></span> <span data-ttu-id="bf089-136">Informationen zu unterschiedlichen Arten von Anwesenheitsänderungen finden Sie im Leistungsindikator SetPresence (Presence Type) Calls.</span><span class="sxs-lookup"><span data-stu-id="bf089-136">For different types of presence changes, see the SetPresence (Presence Type) Calls Performance Counter.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-137">NNN-Antworten für SetPresence</span><span class="sxs-lookup"><span data-stu-id="bf089-137">NNN Responses for SetPresence</span></span></p></td>
<td><p><span data-ttu-id="bf089-138">Die Gesamtzahl der vom Server empfangenen nnn-Antwortcodes.</span><span class="sxs-lookup"><span data-stu-id="bf089-138">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf089-139">GetPresence-Anrufe</span><span class="sxs-lookup"><span data-stu-id="bf089-139">GetPresence Calls</span></span></p></td>
<td><p><span data-ttu-id="bf089-140">Die Gesamtzahl der Versuche, Anwesenheits Anfragen abzurufen.</span><span class="sxs-lookup"><span data-stu-id="bf089-140">Total number of get presence request attempts.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-141">NNN-Antworten für GetPresence</span><span class="sxs-lookup"><span data-stu-id="bf089-141">NNN Responses for GetPresence</span></span></p></td>
<td><p><span data-ttu-id="bf089-142">Die Gesamtzahl der vom Server empfangenen nnn-Antwortcodes.</span><span class="sxs-lookup"><span data-stu-id="bf089-142">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf089-143">**Informationen zum Adressbuchdienst**</span><span class="sxs-lookup"><span data-stu-id="bf089-143">**Address Book service Information**</span></span>

<span data-ttu-id="bf089-144">Diese Kategorie enthält Leistungsindikatoren, die zum Überwachen von Dateidownloads für den Adressbuchdienst (ABS) und für Adressbuch-Webabfrage Dienstanforderungen verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="bf089-144">This category includes counters used to monitor Address Book service (ABS) file downloads and Address Book Web Query service requests.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf089-145"><strong>Leistungsindikator</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-145"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bf089-146"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-146"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf089-147">Vollständige/Delta-Datei Downloads versucht</span><span class="sxs-lookup"><span data-stu-id="bf089-147">ABS Full/Delta File Downloads Attempted</span></span></p></td>
<td><p><span data-ttu-id="bf089-148">Die Gesamtzahl der vollständigen oder Deltadatei Downloadanforderungen wurde versucht.</span><span class="sxs-lookup"><span data-stu-id="bf089-148">Total number of full or delta file download requests attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-149">Vollständige/Delta-Datei Downloads erfolgreich</span><span class="sxs-lookup"><span data-stu-id="bf089-149">ABS Full/Delta File Downloads Succeeded</span></span></p></td>
<td><p><span data-ttu-id="bf089-150">Die Gesamtzahl der vollständigen oder Deltadatei Downloadanforderungen wurde versucht.</span><span class="sxs-lookup"><span data-stu-id="bf089-150">Total number of full or delta file download requests attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf089-151">Verwandte Leistungsindikatoren des Adressbuch-Webabfrage Diensts</span><span class="sxs-lookup"><span data-stu-id="bf089-151">Address Book Web Query service related counters</span></span></p></td>
<td><p><span data-ttu-id="bf089-152">Verwandte Leistungsindikatoren für Adressbuchdateien herunterladen.</span><span class="sxs-lookup"><span data-stu-id="bf089-152">Address book file download related counters.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-153">Versuchter ABS WS-Anruf</span><span class="sxs-lookup"><span data-stu-id="bf089-153">ABS WS Calls attempted</span></span></p></td>
<td><p><span data-ttu-id="bf089-154">Die Gesamtzahl der versuchten Adressbuch-Webabfrage Dienstanforderungen.</span><span class="sxs-lookup"><span data-stu-id="bf089-154">Total number of Address Book Web Query service requests attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf089-155">ABS WS-Aufrufe erfolgreich</span><span class="sxs-lookup"><span data-stu-id="bf089-155">ABS WS Calls Succeeded</span></span></p></td>
<td><p><span data-ttu-id="bf089-156">Die Gesamtzahl der Adressbuch-Webabfrage Dienstanforderungen, die einen erfolgreichen Antwortcode zurückgegeben haben.</span><span class="sxs-lookup"><span data-stu-id="bf089-156">Total number of Address Book Web Query service requests that returned a successful response code.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-157">ABS WS-Anrufe nicht möglich</span><span class="sxs-lookup"><span data-stu-id="bf089-157">ABS WS Calls Failed</span></span></p></td>
<td><p><span data-ttu-id="bf089-158">Die Gesamtzahl der Adressbuch-Webabfrage Dienstanforderungen, die einen Fehlerantwort Code zurückgegeben haben.</span><span class="sxs-lookup"><span data-stu-id="bf089-158">Total number of Address Book Web Query service requests that returned an error response code.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf089-159">**Informationen zur Verteilerliste (DL)**</span><span class="sxs-lookup"><span data-stu-id="bf089-159">**Distribution List (DL) Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf089-160"><strong>Leistungsindikator</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-160"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bf089-161"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-161"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf089-162">Anrufversuche</span><span class="sxs-lookup"><span data-stu-id="bf089-162">Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="bf089-163">Gesamtzahl der versuchten Webdienstanforderungen für die Verteilerlistenerweiterung (dlx).</span><span class="sxs-lookup"><span data-stu-id="bf089-163">Total number of distribution list expansion (DLX) web service requests attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-164">Anrufe erfolgreich</span><span class="sxs-lookup"><span data-stu-id="bf089-164">Calls Succeeded</span></span></p></td>
<td><p><span data-ttu-id="bf089-165">Die Gesamtzahl der dlx-Webdienstanforderungen, die einen erfolgreichen Antwortcode zurückgegeben haben.</span><span class="sxs-lookup"><span data-stu-id="bf089-165">Total number of DLX web service requests that returned a successful response code.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf089-166">Anruf fehlgeschlagen</span><span class="sxs-lookup"><span data-stu-id="bf089-166">Calls Failed</span></span></p></td>
<td><p><span data-ttu-id="bf089-167">Die Gesamtzahl der dlx-Webdienstanforderungen, die einen Fehlerantwort Code zurückgegeben haben.</span><span class="sxs-lookup"><span data-stu-id="bf089-167">Total number of DLX web service requests that returned an error response code.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf089-168">**VoIP-Grundinformationen**</span><span class="sxs-lookup"><span data-stu-id="bf089-168">**VoIP Basic Information**</span></span>

<span data-ttu-id="bf089-169">Die nachstehend aufgeführten Leistungsindikatoren melden Nummern für alle VoIP-Anrufe (Voice over IP), einschließlich Anrufe an den Vermittlungsserver, A/V-Konferenzserver, den Edgeserver, die Antwortgruppen Anwendung und die automatische Konferenzzentrale, wenn diese Szenarien aktiviert sind.</span><span class="sxs-lookup"><span data-stu-id="bf089-169">The performance counters listed below report numbers for all Voice over IP (VoIP) calls, including calls to Mediation Server, A/V Conferencing Server, Edge Server, Response Group application, and Conference Auto Attendant, when these scenarios are enabled.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf089-170"><strong>Leistungsindikator</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-170"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bf089-171"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-171"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf089-172">Aktive Anrufe</span><span class="sxs-lookup"><span data-stu-id="bf089-172">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="bf089-173">Die Gesamtzahl der eingehenden/ausgehenden Sprachanrufe, die derzeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bf089-173">Total number of incoming/outgoing voice calls ongoing currently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-174">Anrufe beendet</span><span class="sxs-lookup"><span data-stu-id="bf089-174">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="bf089-175">Die Gesamtzahl der eingehenden/ausgehenden Sprachanrufe wurde bereits beendet.</span><span class="sxs-lookup"><span data-stu-id="bf089-175">Total number of incoming/outgoing voice calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf089-176">Anrufe abgelehnt</span><span class="sxs-lookup"><span data-stu-id="bf089-176">Calls Declined</span></span></p></td>
<td><p><span data-ttu-id="bf089-177">Die Gesamtzahl der eingehenden Sprachanrufe wurde abgelehnt.</span><span class="sxs-lookup"><span data-stu-id="bf089-177">Total number of incoming voice calls declined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-178">Ein-und ausgehende Anrufe wurden versucht</span><span class="sxs-lookup"><span data-stu-id="bf089-178">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="bf089-179">Die Gesamtzahl der eingehenden/ausgehenden Sprachanrufe wurde versucht.</span><span class="sxs-lookup"><span data-stu-id="bf089-179">Total number of incoming/outgoing voice calls attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf089-180">Eingehende/ausgehende Anrufe eingerichtet</span><span class="sxs-lookup"><span data-stu-id="bf089-180">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="bf089-181">Gesamtzahl der festgelegten eingehenden/ausgehenden Sprachanrufe.</span><span class="sxs-lookup"><span data-stu-id="bf089-181">Total number of incoming/outgoing voice calls established.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-182">Empfangene Anrufe nnn</span><span class="sxs-lookup"><span data-stu-id="bf089-182">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="bf089-183">Die Gesamtzahl der vom Server empfangenen nnn-Antwortcodes.</span><span class="sxs-lookup"><span data-stu-id="bf089-183">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf089-184">VoIP-Durchlauf Rate (%)</span><span class="sxs-lookup"><span data-stu-id="bf089-184">VoIP Pass Rate (%)</span></span></p></td>
<td><p><span data-ttu-id="bf089-185">Gesamtzahl der eingestellten Anrufe/Gesamtzahl der Anrufe.</span><span class="sxs-lookup"><span data-stu-id="bf089-185">Total calls established/Total calls attempted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf089-186">**Informationen zum Reaktionsgruppendienst**</span><span class="sxs-lookup"><span data-stu-id="bf089-186">**Response Group service Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf089-187"><strong>Leistungsindikator</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-187"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bf089-188"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-188"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf089-189">Aktive Anrufe</span><span class="sxs-lookup"><span data-stu-id="bf089-189">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="bf089-190">Die Gesamtzahl aktiver Anrufe an die reaktionsgruppenanwendung.</span><span class="sxs-lookup"><span data-stu-id="bf089-190">Total number of active calls to the Response Group application.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-191">Anrufversuche</span><span class="sxs-lookup"><span data-stu-id="bf089-191">Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="bf089-192">Gesamtzahl der versuchten Anrufe.</span><span class="sxs-lookup"><span data-stu-id="bf089-192">Total number of calls attempted.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf089-193">**Sofortnachrichten (im)-Anrufinformationen**</span><span class="sxs-lookup"><span data-stu-id="bf089-193">**Instant Messaging (IM) Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf089-194"><strong>Leistungsindikator</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-194"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bf089-195"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-195"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf089-196">Aktive Anrufe</span><span class="sxs-lookup"><span data-stu-id="bf089-196">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="bf089-197">Gesamtzahl der laufenden eingehenden/ausgehenden Sofortnachrichten.</span><span class="sxs-lookup"><span data-stu-id="bf089-197">Total number of ongoing incoming/outgoing instant messaging calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-198">Anrufe beendet</span><span class="sxs-lookup"><span data-stu-id="bf089-198">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="bf089-199">Die Gesamtzahl der eingehenden/ausgehenden Instant Messaging-Anrufe wurde bereits beendet.</span><span class="sxs-lookup"><span data-stu-id="bf089-199">Total number of incoming/outgoing instant messaging calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf089-200">Empfangene Anrufe nnn</span><span class="sxs-lookup"><span data-stu-id="bf089-200">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="bf089-201">Die Gesamtzahl der vom Server empfangenen nnn-Antwortcodes.</span><span class="sxs-lookup"><span data-stu-id="bf089-201">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-202">Empfangene/Gesendete Chatnachrichten</span><span class="sxs-lookup"><span data-stu-id="bf089-202">IM Messages Received/Sent</span></span></p></td>
<td><p><span data-ttu-id="bf089-203">Die Gesamtzahl der Nachrichten, die für alle Sitzungen empfangen oder gesendet wurden.</span><span class="sxs-lookup"><span data-stu-id="bf089-203">Total number of messages received or sent for all sessions.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf089-204">Ein-und ausgehende Anrufe wurden versucht</span><span class="sxs-lookup"><span data-stu-id="bf089-204">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="bf089-205">Die Gesamtzahl der eingehenden/ausgehenden Sofortnachrichten Anrufe wurde versucht.</span><span class="sxs-lookup"><span data-stu-id="bf089-205">Total number of incoming/outgoing instant messaging calls attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-206">Eingehende/ausgehende Anrufe eingerichtet</span><span class="sxs-lookup"><span data-stu-id="bf089-206">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="bf089-207">Die Gesamtzahl der eingehenden/ausgehenden Sofortnachrichten Anrufe wurde eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="bf089-207">Total number of incoming/outgoing instant message calls established.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf089-208">**App-Freigabe-Anrufinformationen**</span><span class="sxs-lookup"><span data-stu-id="bf089-208">**App Sharing Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf089-209"><strong>Leistungsindikator</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-209"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bf089-210"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-210"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf089-211">Aktive Anrufe</span><span class="sxs-lookup"><span data-stu-id="bf089-211">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="bf089-212">Gesamtzahl der laufenden eingehenden/ausgehenden Anwendungsfreigabe Anrufe.</span><span class="sxs-lookup"><span data-stu-id="bf089-212">Total number of ongoing incoming/outgoing application sharing calls.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-213">Anrufe beendet</span><span class="sxs-lookup"><span data-stu-id="bf089-213">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="bf089-214">Die Gesamtzahl der eingehenden/ausgehenden Anwendungsfreigabe Anrufe wurde bereits beendet.</span><span class="sxs-lookup"><span data-stu-id="bf089-214">Total number of incoming/outgoing application sharing calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf089-215">Empfangene Anrufe nnn</span><span class="sxs-lookup"><span data-stu-id="bf089-215">Calls Received NNN</span></span></p></td>
<td><p><span data-ttu-id="bf089-216">Die Gesamtzahl der vom Server empfangenen nnn-Antwortcodes.</span><span class="sxs-lookup"><span data-stu-id="bf089-216">Total number of nnn response codes received from the server.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-217">Ein-und ausgehende Anrufe wurden versucht</span><span class="sxs-lookup"><span data-stu-id="bf089-217">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="bf089-218">Die Gesamtzahl der eingehenden/ausgehenden Anwendungsfreigabe Aufrufe wurde versucht.</span><span class="sxs-lookup"><span data-stu-id="bf089-218">Total number of incoming/outgoing application sharing calls attempted.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf089-219">Eingehende/ausgehende Anrufe eingerichtet</span><span class="sxs-lookup"><span data-stu-id="bf089-219">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="bf089-220">Die Gesamtzahl der eingehenden/ausgehenden Anwendungsfreigabe Anrufe wurde eingerichtet.</span><span class="sxs-lookup"><span data-stu-id="bf089-220">Total number of incoming/outgoing application sharing calls established.</span></span></p></td>
</tr>
<tr class="even">
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf089-221">**CAA-Anrufinformationen**</span><span class="sxs-lookup"><span data-stu-id="bf089-221">**CAA Call Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf089-222"><strong>Leistungsindikator</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-222"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bf089-223"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-223"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf089-224">Aktive Anrufe</span><span class="sxs-lookup"><span data-stu-id="bf089-224">Calls Active</span></span></p></td>
<td><p><span data-ttu-id="bf089-225">Die Gesamtzahl der eingehenden/ausgehenden PSTN-Anrufe (Public Switched Telephone Network), die derzeit ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="bf089-225">Total number of incoming/outgoing public switched telephone network (PSTN) calls ongoing currently.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-226">Anrufe beendet</span><span class="sxs-lookup"><span data-stu-id="bf089-226">Calls Terminated</span></span></p></td>
<td><p><span data-ttu-id="bf089-227">Die Gesamtzahl der eingehenden/ausgehenden PSTN-Anrufe wurde bereits beendet.</span><span class="sxs-lookup"><span data-stu-id="bf089-227">Total number of incoming/outgoing PSTN calls already terminated.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf089-228">Ein-und ausgehende Anrufe wurden versucht</span><span class="sxs-lookup"><span data-stu-id="bf089-228">Incoming/Outgoing Calls Attempted</span></span></p></td>
<td><p><span data-ttu-id="bf089-229">Die Gesamtzahl der eingehenden/ausgehenden PSTN-Anrufe wurde versucht.</span><span class="sxs-lookup"><span data-stu-id="bf089-229">Total number of incoming/outgoing PSTN calls attempted.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-230">Eingehende/ausgehende Anrufe eingerichtet</span><span class="sxs-lookup"><span data-stu-id="bf089-230">Incoming/Outgoing Calls Established</span></span></p></td>
<td><p><span data-ttu-id="bf089-231">Gesamtzahl der festgelegten eingehenden/ausgehenden PSTN-Anrufe.</span><span class="sxs-lookup"><span data-stu-id="bf089-231">Total number of incoming/outgoing PSTN calls established.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf089-232">**Konferenz Informationen**</span><span class="sxs-lookup"><span data-stu-id="bf089-232">**Conference Information**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf089-233"><strong>Leistungsindikator</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-233"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bf089-234"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-234"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf089-235">Aktive Instant Messaging-Konferenzen</span><span class="sxs-lookup"><span data-stu-id="bf089-235">Active Instant Messaging Conferences</span></span></p></td>
<td><p><span data-ttu-id="bf089-236">Gesamtzahl der laufenden Instant Messaging-Konferenzen.</span><span class="sxs-lookup"><span data-stu-id="bf089-236">Total number of ongoing instant messaging conferences.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-237">Aktive Audio/Video Konferenzen</span><span class="sxs-lookup"><span data-stu-id="bf089-237">Active Audio/Video Conferences</span></span></p></td>
<td><p><span data-ttu-id="bf089-238">Gesamtzahl der laufenden Audio/Video-Konferenzen (A/V).</span><span class="sxs-lookup"><span data-stu-id="bf089-238">Total number of ongoing audio/video (A/V) conferences.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf089-239">Aktive Anwendungsfreigabe Konferenzen</span><span class="sxs-lookup"><span data-stu-id="bf089-239">Active Application Sharing Conferences</span></span></p></td>
<td><p><span data-ttu-id="bf089-240">Gesamtzahl der laufenden Konferenz zur Anwendungsfreigabe.</span><span class="sxs-lookup"><span data-stu-id="bf089-240">Total number of ongoing application sharing conferences.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-241">Anzahl der Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="bf089-241">Number of Participants</span></span></p></td>
<td><p><span data-ttu-id="bf089-242">Die Gesamtzahl der Teilnehmer, die derzeit mit Konferenzen verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="bf089-242">Total number of participants currently connected to conferences.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="bf089-243">Konferenzplan Fehler</span><span class="sxs-lookup"><span data-stu-id="bf089-243">Conference Schedule Failure</span></span></p></td>
<td><p><span data-ttu-id="bf089-244">Die Gesamtzahl der Fehler bei dem Versuch, eine Konferenz zu planen.</span><span class="sxs-lookup"><span data-stu-id="bf089-244">Total number of failures while trying to schedule a conference.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-245">Konferenz Fehler teilnehmen</span><span class="sxs-lookup"><span data-stu-id="bf089-245">Join Conference Failure</span></span></p></td>
<td><p><span data-ttu-id="bf089-246">Die Gesamtzahl der Fehler bei dem Versuch, eine Verbindung mit einer Konferenz herzustellen.</span><span class="sxs-lookup"><span data-stu-id="bf089-246">Total number of failures while trying to connect to a conference.</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="bf089-247">**UCWA-Client-Leistungsindikatoren**</span><span class="sxs-lookup"><span data-stu-id="bf089-247">**UCWA Client Counters**</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="bf089-248"><strong>Leistungsindikator</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-248"><strong>Performance Counter</strong></span></span></th>
<th><span data-ttu-id="bf089-249"><strong>Beschreibung</strong></span><span class="sxs-lookup"><span data-stu-id="bf089-249"><strong>Description</strong></span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="bf089-250">Gesamtzahl der IMMCU-Joins erfolgreich</span><span class="sxs-lookup"><span data-stu-id="bf089-250">Total Number of IMMCU Joins Succeeded</span></span></p></td>
<td><p><span data-ttu-id="bf089-251">Die Gesamtzahl der Teilnahmen an Instant Messaging-Konferenzen.</span><span class="sxs-lookup"><span data-stu-id="bf089-251">Total number of instant messaging conferences joined.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="bf089-252">Gesamtzahl der DMCU-Joins erfolgreich</span><span class="sxs-lookup"><span data-stu-id="bf089-252">Total Number of DMCU Joins Succeeded</span></span></p></td>
<td><p><span data-ttu-id="bf089-253">Die Gesamtzahl der A/V-Konferenzen, die beigetreten sind.</span><span class="sxs-lookup"><span data-stu-id="bf089-253">Total number of A/V conferences joined.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="bf089-254">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bf089-254">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

