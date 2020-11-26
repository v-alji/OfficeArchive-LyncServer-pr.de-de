---
title: 'Lync Server 2013: UCWA-Ereignisse'
description: 'Lync Server 2013: UCWA-Ereignisse.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: UCWA events
ms:assetid: 26cb409d-f4e4-43c7-873f-b694702d491d
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ945621(v=OCS.15)
ms:contentKeyID: 51541461
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8104ce9c7533350f40ce194e1cde205bc3692792
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49440465"
---
# <a name="ucwa-events-in-lync-server-2013"></a><span data-ttu-id="44d8a-103">UCWA-Ereignisse in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="44d8a-103">UCWA events in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="44d8a-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="44d8a-104">

<span> </span></span></span>

<span data-ttu-id="44d8a-105">_**Letztes Änderungsdatum des Themas:** 2013-02-15_</span><span class="sxs-lookup"><span data-stu-id="44d8a-105">_**Topic Last Modified:** 2013-02-15_</span></span>

    The information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="44d8a-106">Lync Server 2013 verwendet die Unified Communications Web-API (UCWA) für eine Reihe von Zwecken, vom Zugriff auf Microsoft Exchange für Kontakt suchen bis zur Aktualisierung der Anwesenheitsinformationen für mobile Clients.</span><span class="sxs-lookup"><span data-stu-id="44d8a-106">Lync Server 2013 uses the Unified Communications Web API (UCWA) for a number of purposes, from accessing Microsoft Exchange for contact searches to updating presence for mobile clients.</span></span>

<span data-ttu-id="44d8a-p101">UCWA zeichnet Einträge zum Betriebsverhalten als die Ereignistypen „Information“, „Warnung“ und „Fehler“ auf. In der folgenden Tabelle sind die Ereignisse beschrieben, die von den UCWA-Komponenten geschrieben werden können.</span><span class="sxs-lookup"><span data-stu-id="44d8a-p101">UCWA will write records of operational behavior as event types Informational, Warning, and Error. The following table describes the events that can be written by the UCWA components.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="44d8a-109">Ereigniskennung</span><span class="sxs-lookup"><span data-stu-id="44d8a-109">Event ID</span></span></th>
<th><span data-ttu-id="44d8a-110">Ereignistyp</span><span class="sxs-lookup"><span data-stu-id="44d8a-110">Event Type</span></span></th>
<th><span data-ttu-id="44d8a-111">Zusammenfassung</span><span class="sxs-lookup"><span data-stu-id="44d8a-111">Summary</span></span></th>
<th><span data-ttu-id="44d8a-112">Ursache und Lösung</span><span class="sxs-lookup"><span data-stu-id="44d8a-112">Cause and Resolution</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="44d8a-113">20001</span><span class="sxs-lookup"><span data-stu-id="44d8a-113">20001</span></span></p></td>
<td><p><span data-ttu-id="44d8a-114">Information</span><span class="sxs-lookup"><span data-stu-id="44d8a-114">Informational</span></span></p></td>
<td><p><span data-ttu-id="44d8a-115">UCWA initialisiert</span><span class="sxs-lookup"><span data-stu-id="44d8a-115">UCWA initialized</span></span></p></td>
<td><p><span data-ttu-id="44d8a-116">-</span><span class="sxs-lookup"><span data-stu-id="44d8a-116">N/A</span></span></p>
<p><span data-ttu-id="44d8a-117">-</span><span class="sxs-lookup"><span data-stu-id="44d8a-117">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44d8a-118">20002</span><span class="sxs-lookup"><span data-stu-id="44d8a-118">20002</span></span></p></td>
<td><p><span data-ttu-id="44d8a-119">Fehler</span><span class="sxs-lookup"><span data-stu-id="44d8a-119">Error</span></span></p></td>
<td><p><span data-ttu-id="44d8a-120">Unerwartete Ausnahme während der Initialisierung von UCWA</span><span class="sxs-lookup"><span data-stu-id="44d8a-120">UCWA encountered an unexpected exception during initialization</span></span></p></td>
<td><p><span data-ttu-id="44d8a-121">Während der Initialisierung ist ein unerwarteter Fehler aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="44d8a-121">An unexpected error has occurred during initialization</span></span></p>
<p><span data-ttu-id="44d8a-122">Überprüfen Sie die Ausnahmedetails im zugehörigen Ereignisprotokolleintrag, um die mögliche Ursache zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="44d8a-122">Examine the exception details in the associated event log entry to determine the possible cause</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44d8a-123">20003</span><span class="sxs-lookup"><span data-stu-id="44d8a-123">20003</span></span></p></td>
<td><p><span data-ttu-id="44d8a-124">Fehler</span><span class="sxs-lookup"><span data-stu-id="44d8a-124">Error</span></span></p></td>
<td><p><span data-ttu-id="44d8a-125">In der UCWA ist eine nicht behandelte Ausnahme aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="44d8a-125">UCWA encountered an unhandled exception</span></span></p></td>
<td><p><span data-ttu-id="44d8a-126">Eine nicht behandelte Ausnahme ist aufgetreten.</span><span class="sxs-lookup"><span data-stu-id="44d8a-126">An unhandled exception happened</span></span></p>
<p><span data-ttu-id="44d8a-p102">Starten Sie den Server neu. Falls das Problem weiterhin besteht, wenden Sie sich an den Produktsupport.</span><span class="sxs-lookup"><span data-stu-id="44d8a-p102">Restart the server. If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44d8a-129">20004</span><span class="sxs-lookup"><span data-stu-id="44d8a-129">20004</span></span></p></td>
<td><p><span data-ttu-id="44d8a-130">Fehler</span><span class="sxs-lookup"><span data-stu-id="44d8a-130">Error</span></span></p></td>
<td><p><span data-ttu-id="44d8a-131">Kein Zugriff auf Exchange zum Abrufen des HD-Fotos</span><span class="sxs-lookup"><span data-stu-id="44d8a-131">Cannot access Exchange for HD photo</span></span></p></td>
<td><p><span data-ttu-id="44d8a-132">Keine Verbindung mit Exchange verfügbar</span><span class="sxs-lookup"><span data-stu-id="44d8a-132">Connection to Exchange is not available</span></span></p>
<p><span data-ttu-id="44d8a-133">Sicherstellen, dass eine Verbindung mit Exchange verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="44d8a-133">Make sure the connection to Exchange is available</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44d8a-134">20005</span><span class="sxs-lookup"><span data-stu-id="44d8a-134">20005</span></span></p></td>
<td><p><span data-ttu-id="44d8a-135">Information</span><span class="sxs-lookup"><span data-stu-id="44d8a-135">Informational</span></span></p></td>
<td><p><span data-ttu-id="44d8a-136">Wiederherstellung nach dem Fehler beim Zugriff auf Exchange zum Abrufen des HD-Fotos ausgeführt</span><span class="sxs-lookup"><span data-stu-id="44d8a-136">Recovered from failing to access Exchange for HD photo</span></span></p></td>
<td><p><span data-ttu-id="44d8a-137">-</span><span class="sxs-lookup"><span data-stu-id="44d8a-137">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44d8a-138">20006</span><span class="sxs-lookup"><span data-stu-id="44d8a-138">20006</span></span></p></td>
<td><p><span data-ttu-id="44d8a-139">Fehler</span><span class="sxs-lookup"><span data-stu-id="44d8a-139">Error</span></span></p></td>
<td><p><span data-ttu-id="44d8a-140">Kein Zugriff auf Exchange zum Suchen von Kontakten</span><span class="sxs-lookup"><span data-stu-id="44d8a-140">Cannot access Exchange for contact search</span></span></p></td>
<td><p><span data-ttu-id="44d8a-141">Keine Verbindung mit Exchange verfügbar</span><span class="sxs-lookup"><span data-stu-id="44d8a-141">Connection to Exchange is not available</span></span></p>
<p><span data-ttu-id="44d8a-142">Sicherstellen, dass eine Verbindung mit Exchange verfügbar ist</span><span class="sxs-lookup"><span data-stu-id="44d8a-142">Make sure the connection to Exchange is available</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44d8a-143">20007</span><span class="sxs-lookup"><span data-stu-id="44d8a-143">20007</span></span></p></td>
<td><p><span data-ttu-id="44d8a-144">Information</span><span class="sxs-lookup"><span data-stu-id="44d8a-144">Informational</span></span></p></td>
<td><p><span data-ttu-id="44d8a-145">Wiederherstellung nach dem Fehler beim Suchen von Kontakten in Exchange ausgeführt</span><span class="sxs-lookup"><span data-stu-id="44d8a-145">Recovered from failing to search contact in Exchange</span></span></p></td>
<td><p><span data-ttu-id="44d8a-146">-</span><span class="sxs-lookup"><span data-stu-id="44d8a-146">N/A</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44d8a-147">20008</span><span class="sxs-lookup"><span data-stu-id="44d8a-147">20008</span></span></p></td>
<td><p><span data-ttu-id="44d8a-148">Warnung</span><span class="sxs-lookup"><span data-stu-id="44d8a-148">Warning</span></span></p></td>
<td><p><span data-ttu-id="44d8a-149">Versuchen, mehr Anwesenheitsabonnements pro Anwendung als zulässig abzuschließen</span><span class="sxs-lookup"><span data-stu-id="44d8a-149">Attempt to subscribe more than the allowed presence subscriptions per application</span></span></p></td>
<td><p><span data-ttu-id="44d8a-150">Versuchen, mehr Anwesenheitsabonnements pro Anwendung als zulässig abzuschließen</span><span class="sxs-lookup"><span data-stu-id="44d8a-150">Attempt to subscribe more than the allowed presence subscriptions per application</span></span></p>
<p><span data-ttu-id="44d8a-151">Clients auf unnötige Abonnements überprüfen</span><span class="sxs-lookup"><span data-stu-id="44d8a-151">Check the clients for unnecessary subscriptions</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44d8a-152">20009</span><span class="sxs-lookup"><span data-stu-id="44d8a-152">20009</span></span></p></td>
<td><p><span data-ttu-id="44d8a-153">Warnung</span><span class="sxs-lookup"><span data-stu-id="44d8a-153">Warning</span></span></p></td>
<td><p><span data-ttu-id="44d8a-154">Versuchen, mehr Anwesenheitsabonnements pro Batch als zulässig abzuschließen</span><span class="sxs-lookup"><span data-stu-id="44d8a-154">Attempt to subscribe more than the allowed presence subscriptions per batch</span></span></p></td>
<td><p><span data-ttu-id="44d8a-155">Versuchen, mehr Anwesenheitsabonnements pro Batch als zulässig abzuschließen</span><span class="sxs-lookup"><span data-stu-id="44d8a-155">Attempt to subscribe more than the allowed presence subscriptions per batch</span></span></p>
<p><span data-ttu-id="44d8a-156">Clients auf unnötige Abonnements überprüfen</span><span class="sxs-lookup"><span data-stu-id="44d8a-156">Check the clients for unnecessary subscriptions</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44d8a-157">20010</span><span class="sxs-lookup"><span data-stu-id="44d8a-157">20010</span></span></p></td>
<td><p><span data-ttu-id="44d8a-158">Fehler</span><span class="sxs-lookup"><span data-stu-id="44d8a-158">Error</span></span></p></td>
<td><p><span data-ttu-id="44d8a-159">In-Band-Daten können nicht abgerufen werden</span><span class="sxs-lookup"><span data-stu-id="44d8a-159">Cannot retrieve inband data</span></span></p></td>
<td><p><span data-ttu-id="44d8a-160">In-Band-Daten können nicht abgerufen werden</span><span class="sxs-lookup"><span data-stu-id="44d8a-160">Cannot retrieve inband data</span></span></p>
<p><span data-ttu-id="44d8a-161">Falls das Problem weiterhin besteht, wenden Sie sich an den Produktsupport.</span><span class="sxs-lookup"><span data-stu-id="44d8a-161">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44d8a-162">20011</span><span class="sxs-lookup"><span data-stu-id="44d8a-162">20011</span></span></p></td>
<td><p><span data-ttu-id="44d8a-163">Fehler</span><span class="sxs-lookup"><span data-stu-id="44d8a-163">Error</span></span></p></td>
<td><p><span data-ttu-id="44d8a-164">Anwesenheit kann nicht abonniert werden</span><span class="sxs-lookup"><span data-stu-id="44d8a-164">Cannot subscribe presence</span></span></p></td>
<td><p><span data-ttu-id="44d8a-165">Anwesenheit kann nicht abonniert werden</span><span class="sxs-lookup"><span data-stu-id="44d8a-165">Cannot subscribe presence</span></span></p>
<p><span data-ttu-id="44d8a-166">Falls das Problem weiterhin besteht, wenden Sie sich an den Produktsupport.</span><span class="sxs-lookup"><span data-stu-id="44d8a-166">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44d8a-167">20012</span><span class="sxs-lookup"><span data-stu-id="44d8a-167">20012</span></span></p></td>
<td><p><span data-ttu-id="44d8a-168">Fehler</span><span class="sxs-lookup"><span data-stu-id="44d8a-168">Error</span></span></p></td>
<td><p><span data-ttu-id="44d8a-169">Fehler beim Registrieren des Endpunkts</span><span class="sxs-lookup"><span data-stu-id="44d8a-169">Failed to register endpoint</span></span></p></td>
<td><p><span data-ttu-id="44d8a-170">Fehler beim Registrieren des Endpunkts</span><span class="sxs-lookup"><span data-stu-id="44d8a-170">Failed to register endpoint</span></span></p>
<p><span data-ttu-id="44d8a-171">Falls das Problem weiterhin besteht, wenden Sie sich an den Produktsupport.</span><span class="sxs-lookup"><span data-stu-id="44d8a-171">If the problem persists contact product support</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44d8a-172">20013</span><span class="sxs-lookup"><span data-stu-id="44d8a-172">20013</span></span></p></td>
<td><p><span data-ttu-id="44d8a-173">Fehler</span><span class="sxs-lookup"><span data-stu-id="44d8a-173">Error</span></span></p></td>
<td><p><span data-ttu-id="44d8a-174">IM MCU ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="44d8a-174">IM MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="44d8a-175">IM MCU ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="44d8a-175">IM MCU is unavailable</span></span></p>
<p><span data-ttu-id="44d8a-176">Prüfen, ob IM MCU ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44d8a-176">See whether IM MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44d8a-177">20014</span><span class="sxs-lookup"><span data-stu-id="44d8a-177">20014</span></span></p></td>
<td><p><span data-ttu-id="44d8a-178">Information</span><span class="sxs-lookup"><span data-stu-id="44d8a-178">Informational</span></span></p></td>
<td><p><span data-ttu-id="44d8a-179">Wiederherstellung nach dem Fehler bei der Herstellung der Verbindung mit IM MCU ausgeführt</span><span class="sxs-lookup"><span data-stu-id="44d8a-179">Recovered from failing to connect to IM MCU</span></span></p></td>
<td><p><span data-ttu-id="44d8a-180">-</span><span class="sxs-lookup"><span data-stu-id="44d8a-180">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44d8a-181">20015</span><span class="sxs-lookup"><span data-stu-id="44d8a-181">20015</span></span></p></td>
<td><p><span data-ttu-id="44d8a-182">Fehler</span><span class="sxs-lookup"><span data-stu-id="44d8a-182">Error</span></span></p></td>
<td><p><span data-ttu-id="44d8a-183">AV MCU ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="44d8a-183">AV MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="44d8a-184">AV MCU ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="44d8a-184">AV MCU is unavailable</span></span></p>
<p><span data-ttu-id="44d8a-185">Prüfen, ob AV MCU ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44d8a-185">See whether AV MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44d8a-186">20016</span><span class="sxs-lookup"><span data-stu-id="44d8a-186">20016</span></span></p></td>
<td><p><span data-ttu-id="44d8a-187">Information</span><span class="sxs-lookup"><span data-stu-id="44d8a-187">Informational</span></span></p></td>
<td><p><span data-ttu-id="44d8a-188">Wiederherstellung nach dem Fehler bei der Herstellung der Verbindung mit AV MCU ausgeführt</span><span class="sxs-lookup"><span data-stu-id="44d8a-188">Recovered from failing to connect to AV MCU</span></span></p></td>
<td><p><span data-ttu-id="44d8a-189">-</span><span class="sxs-lookup"><span data-stu-id="44d8a-189">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44d8a-190">20017</span><span class="sxs-lookup"><span data-stu-id="44d8a-190">20017</span></span></p></td>
<td><p><span data-ttu-id="44d8a-191">Fehler</span><span class="sxs-lookup"><span data-stu-id="44d8a-191">Error</span></span></p></td>
<td><p><span data-ttu-id="44d8a-192">AS MCU ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="44d8a-192">AS MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="44d8a-193">AS MCU ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="44d8a-193">AS MCU is unavailable</span></span></p>
<p><span data-ttu-id="44d8a-194">Prüfen, ob AS MCU ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44d8a-194">See whether AS MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44d8a-195">20018</span><span class="sxs-lookup"><span data-stu-id="44d8a-195">20018</span></span></p></td>
<td><p><span data-ttu-id="44d8a-196">Information</span><span class="sxs-lookup"><span data-stu-id="44d8a-196">Informational</span></span></p></td>
<td><p><span data-ttu-id="44d8a-197">Wiederherstellung nach dem Fehler bei der Herstellung der Verbindung mit AS MCU ausgeführt</span><span class="sxs-lookup"><span data-stu-id="44d8a-197">Recovered from failing to connect to AS MCU</span></span></p></td>
<td><p><span data-ttu-id="44d8a-198">-</span><span class="sxs-lookup"><span data-stu-id="44d8a-198">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44d8a-199">20019</span><span class="sxs-lookup"><span data-stu-id="44d8a-199">20019</span></span></p></td>
<td><p><span data-ttu-id="44d8a-200">Fehler</span><span class="sxs-lookup"><span data-stu-id="44d8a-200">Error</span></span></p></td>
<td><p><span data-ttu-id="44d8a-201">Data MCU ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="44d8a-201">Data MCU is unavailable</span></span></p></td>
<td><p><span data-ttu-id="44d8a-202">Data MCU ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="44d8a-202">Data MCU is unavailable</span></span></p>
<p><span data-ttu-id="44d8a-203">Prüfen, ob Data MCU ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44d8a-203">See whether Data MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44d8a-204">20020</span><span class="sxs-lookup"><span data-stu-id="44d8a-204">20020</span></span></p></td>
<td><p><span data-ttu-id="44d8a-205">Information</span><span class="sxs-lookup"><span data-stu-id="44d8a-205">Informational</span></span></p></td>
<td><p><span data-ttu-id="44d8a-206">Wiederherstellung nach dem Fehler bei der Herstellung der Verbindung mit Date MCU ausgeführt</span><span class="sxs-lookup"><span data-stu-id="44d8a-206">Recovered from failing to connect to Data MCU</span></span></p></td>
<td><p><span data-ttu-id="44d8a-207">-</span><span class="sxs-lookup"><span data-stu-id="44d8a-207">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44d8a-208">20021</span><span class="sxs-lookup"><span data-stu-id="44d8a-208">20021</span></span></p></td>
<td><p><span data-ttu-id="44d8a-209">Fehler</span><span class="sxs-lookup"><span data-stu-id="44d8a-209">Error</span></span></p></td>
<td><p><span data-ttu-id="44d8a-210">Teilnahme an IM MCU nicht möglich</span><span class="sxs-lookup"><span data-stu-id="44d8a-210">Cannot join IM MCU</span></span></p></td>
<td><p><span data-ttu-id="44d8a-211">Teilnahme an IM MCU nicht möglich</span><span class="sxs-lookup"><span data-stu-id="44d8a-211">Cannot join IM MCU</span></span></p>
<p><span data-ttu-id="44d8a-212">Prüfen, ob IM MCU ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44d8a-212">See whether IM MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44d8a-213">20022</span><span class="sxs-lookup"><span data-stu-id="44d8a-213">20022</span></span></p></td>
<td><p><span data-ttu-id="44d8a-214">Fehler</span><span class="sxs-lookup"><span data-stu-id="44d8a-214">Error</span></span></p></td>
<td><p><span data-ttu-id="44d8a-215">Teilnahme an AV MCU nicht möglich</span><span class="sxs-lookup"><span data-stu-id="44d8a-215">Cannot join AV MCU</span></span></p></td>
<td><p><span data-ttu-id="44d8a-216">Teilnahme an AV MCU nicht möglich</span><span class="sxs-lookup"><span data-stu-id="44d8a-216">Cannot join AV MCU</span></span></p>
<p><span data-ttu-id="44d8a-217">Prüfen, ob AV MCU ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44d8a-217">See whether AV MCU is running</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44d8a-218">20023</span><span class="sxs-lookup"><span data-stu-id="44d8a-218">20023</span></span></p></td>
<td><p><span data-ttu-id="44d8a-219">Fehler</span><span class="sxs-lookup"><span data-stu-id="44d8a-219">Error</span></span></p></td>
<td><p><span data-ttu-id="44d8a-220">Teilnahme an AS MCU nicht möglich</span><span class="sxs-lookup"><span data-stu-id="44d8a-220">Cannot join AS MCU</span></span></p></td>
<td><p><span data-ttu-id="44d8a-221">Teilnahme an AS MCU nicht möglich</span><span class="sxs-lookup"><span data-stu-id="44d8a-221">Cannot join AS MCU</span></span></p>
<p><span data-ttu-id="44d8a-222">Prüfen, ob AS MCU ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44d8a-222">See whether AS MCU is running</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44d8a-223">20024</span><span class="sxs-lookup"><span data-stu-id="44d8a-223">20024</span></span></p></td>
<td><p><span data-ttu-id="44d8a-224">Fehler</span><span class="sxs-lookup"><span data-stu-id="44d8a-224">Error</span></span></p></td>
<td><p><span data-ttu-id="44d8a-225">Teilnahme an Data MCU nicht möglich</span><span class="sxs-lookup"><span data-stu-id="44d8a-225">Cannot join Data MCU</span></span></p></td>
<td><p><span data-ttu-id="44d8a-226">Teilnahme an Data MCU nicht möglich</span><span class="sxs-lookup"><span data-stu-id="44d8a-226">Cannot join Data MCU</span></span></p>
<p><span data-ttu-id="44d8a-227">Prüfen, ob Data MCU ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="44d8a-227">See whether Data MCU is running</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44d8a-228">20025</span><span class="sxs-lookup"><span data-stu-id="44d8a-228">20025</span></span></p></td>
<td><p><span data-ttu-id="44d8a-229">Fehler</span><span class="sxs-lookup"><span data-stu-id="44d8a-229">Error</span></span></p></td>
<td><p><span data-ttu-id="44d8a-230">Kein Zugriff auf Active Directory zum Abrufen des Fotos</span><span class="sxs-lookup"><span data-stu-id="44d8a-230">Cannot access active directory for photo</span></span></p></td>
<td><p><span data-ttu-id="44d8a-231">Die Verbindung mit Active Directory ist nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="44d8a-231">Connection to active directory is not available</span></span></p>
<p><span data-ttu-id="44d8a-232">Stellen Sie sicher, dass die Verbindung mit Active Directory verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="44d8a-232">Make sure the connection to active directory is available</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="44d8a-233">20026</span><span class="sxs-lookup"><span data-stu-id="44d8a-233">20026</span></span></p></td>
<td><p><span data-ttu-id="44d8a-234">Information</span><span class="sxs-lookup"><span data-stu-id="44d8a-234">Informational</span></span></p></td>
<td><p><span data-ttu-id="44d8a-235">Wiederherstellung nach dem Fehler beim Zugriff auf Active Directory zum Abrufen des Fotos ausgeführt</span><span class="sxs-lookup"><span data-stu-id="44d8a-235">Recovered from failing to access active directory for photo</span></span></p></td>
<td><p><span data-ttu-id="44d8a-236">-</span><span class="sxs-lookup"><span data-stu-id="44d8a-236">N/A</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="44d8a-237">20027</span><span class="sxs-lookup"><span data-stu-id="44d8a-237">20027</span></span></p></td>
<td><p><span data-ttu-id="44d8a-238">Warnung</span><span class="sxs-lookup"><span data-stu-id="44d8a-238">Warning</span></span></p></td>
<td><p><span data-ttu-id="44d8a-239">Deserialisierung nicht möglich</span><span class="sxs-lookup"><span data-stu-id="44d8a-239">Cannot deserialize</span></span></p></td>
<td><p><span data-ttu-id="44d8a-240">Deserialisierung nicht möglich</span><span class="sxs-lookup"><span data-stu-id="44d8a-240">Cannot deserialize</span></span></p>
<p><span data-ttu-id="44d8a-241">Falls das Problem weiterhin besteht, wenden Sie sich an den Produktsupport.</span><span class="sxs-lookup"><span data-stu-id="44d8a-241">If the problem persists contact product support</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="44d8a-242">


</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="44d8a-242">


</div>

<span> </span>

</div>

</div>

</span></span></div>

