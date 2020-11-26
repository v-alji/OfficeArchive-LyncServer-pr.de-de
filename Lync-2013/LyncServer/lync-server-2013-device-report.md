---
title: 'Lync Server 2013: gerätebericht'
description: 'Lync Server 2013: gerätebericht.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Device Report
ms:assetid: f42e4d60-699b-4870-8bb5-13b51bb6eb2b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg615049(v=OCS.15)
ms:contentKeyID: 48185807
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: a8bff8e973d5c3e2d96c18992a2a2d917d4deb1c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429426"
---
# <a name="device-report-in-lync-server-2013"></a><span data-ttu-id="2324f-103">Gerätebericht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="2324f-103">Device Report in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="2324f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="2324f-104">

<span> </span></span></span>

<span data-ttu-id="2324f-105">_**Letztes Änderungsdatum des Themas:** 2013-11-12_</span><span class="sxs-lookup"><span data-stu-id="2324f-105">_**Topic Last Modified:** 2013-11-12_</span></span>

<span data-ttu-id="2324f-106">Der Gerätebericht wäre mit „Mikrofon- und Lautsprecherbericht“ treffender betitelt, denn er ruft anrufbezogene Metriken ab (z. B. Prozentsatz der Anrufe schlechter Qualität, Echo und Sprachumschaltzeit) und gruppiert sie nach den im Anruf verwendeten Mikrofonen und Lautsprechern.</span><span class="sxs-lookup"><span data-stu-id="2324f-106">The Device Report might be better titled the Microphone and Speakers Report; that's because the Device Report retrieves call-related metrics (such as poor call percentage, echo, and voice switch time) grouped by the microphones and speakers used in the call.</span></span> <span data-ttu-id="2324f-107">Wenn Sie an IP-Telefonen (auch gemeinhin als "Geräte" bezeichnet) interessiert sind, verwenden Sie stattdessen den [Bericht IP Phone Inventory in lync Server 2013](lync-server-2013-ip-phone-inventory-report.md) .</span><span class="sxs-lookup"><span data-stu-id="2324f-107">If you are interested in IP phones (also commonly referred to as "devices"), use the [IP Phone Inventory Report in Lync Server 2013](lync-server-2013-ip-phone-inventory-report.md) instead.</span></span>

<span data-ttu-id="2324f-p102">Der Gerätebericht ist für Administratoren von großem Nutzen, wenn herausgefunden werden soll, ob bei einem bestimmten Gerätetyp mehr Anrufe schlechter Qualität auftreten als bei anderen Typen. Das kann wiederum Kaufentscheidungen beeinflussen, wenn neue Geräte angeschafft oder vorhandene ausgetauscht werden müssen.</span><span class="sxs-lookup"><span data-stu-id="2324f-p102">The Device Report is extremely useful for administrators in determining if a specific type of device is experiencing high volumes of poor quality calls than others. In turn, this could influence any decisions you must make when it comes time to buy new devices or to replace existing devices.</span></span>

<span data-ttu-id="2324f-p103">Standardmäßig beruhen die Werte im Gerätebericht auch auf dem Mikrofon (dem Aufnahmegerät) und den Lautsprechern bzw. dem Kopfhörer (dem Darstellungsgerät), die bei dem Anruf verwendet werden. Angenommen, Sie haben mehrere Benutzer, die das folgende Aufnahme- bzw. Darstellungsgerät verwenden: Standardmäßig basieren die Informationen im Gerätebericht ebenfalls auf dem Mikrofon (Aufnahmegerät) und den Lautsprechern bzw. dem Kopfhörer (Darstellungsgerät), die für den Anruf verwendet wurden. Nehmen Sie beispielsweise an, dass Sie verschiedene Benutzer haben, die das folgende Aufnahmegerät und das folgende Darstellungsgerät verwenden:</span><span class="sxs-lookup"><span data-stu-id="2324f-p103">By default, the information displayed in the Device Report is also based on the microphone (the capture device) and speakers/headset (the render device) used in the call. For example, suppose you have several users who use the following capture device and the following render device: By default, the information displayed in the Device Report is also based on the microphone (the capture device) and speakers/headset (the render device) used in the call. For example, suppose you have several users who use the following capture device and the following render device:</span></span>

  - <span data-ttu-id="2324f-113">Aufnahmegerät -- Mikrofon (SoundMAX Integrated Digital HD Audio)</span><span class="sxs-lookup"><span data-stu-id="2324f-113">Capture device -- Microphone (SoundMAX Integrated Digital HD Audio)</span></span>

  - <span data-ttu-id="2324f-114">Darstellungsgerät -- Headset-Kopfhörer (Microsoft LifeChat LX-3000)</span><span class="sxs-lookup"><span data-stu-id="2324f-114">Render device -- Headset Earphone (Microsoft LifeChat LX-3000)</span></span>

<span data-ttu-id="2324f-115">Wenn diese Benutzer insgesamt 254 Anrufe getätigt haben, enthält der Bericht den folgenden Eintrag:</span><span class="sxs-lookup"><span data-stu-id="2324f-115">If those users made a total of 254 calls you'll see an entry like this in the report:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2324f-116">Aufnahmegerät</span><span class="sxs-lookup"><span data-stu-id="2324f-116">Capture device</span></span></th>
<th><span data-ttu-id="2324f-117">Darstellungsgerät</span><span class="sxs-lookup"><span data-stu-id="2324f-117">Render device</span></span></th>
<th><span data-ttu-id="2324f-118">Anruflautstärke</span><span class="sxs-lookup"><span data-stu-id="2324f-118">Call volume</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2324f-119">Mikrofon (SoundMAX Integrated Digital HD Audio)</span><span class="sxs-lookup"><span data-stu-id="2324f-119">Microphone (SoundMAX Integrated Digital HD Audio)</span></span></p></td>
<td><p><span data-ttu-id="2324f-120">Headset-Kopfhörer (Microsoft LifeChat LX-3000)</span><span class="sxs-lookup"><span data-stu-id="2324f-120">Headset Earphone (Microsoft LifeChat LX-3000)</span></span></p></td>
<td><p><span data-ttu-id="2324f-121">254</span><span class="sxs-lookup"><span data-stu-id="2324f-121">254</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2324f-p104">Nehmen wir jetzt an, Sie haben eine Reihe von Benutzern, die das gleiche Aufnahmegerät, aber ein anderes Darstellungsgerät verwenden. In diesem Fall enthält der Bericht eine zweite Zeile, und zwar für diese spezielle Kombination aus Aufnahme- und Darstellungsgerät:</span><span class="sxs-lookup"><span data-stu-id="2324f-p104">Now, suppose you have a number of users who use that same capture device but a different render device. In that case, you'll have a second line entry in the report, one for that unique combination of capture device and render device:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2324f-124">Aufnahmegerät</span><span class="sxs-lookup"><span data-stu-id="2324f-124">Capture device</span></span></th>
<th><span data-ttu-id="2324f-125">Darstellungsgerät</span><span class="sxs-lookup"><span data-stu-id="2324f-125">Render device</span></span></th>
<th><span data-ttu-id="2324f-126">Anruflautstärke</span><span class="sxs-lookup"><span data-stu-id="2324f-126">Call volume</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2324f-127">Mikrofon (SoundMAX Integrated Digital HD Audio)</span><span class="sxs-lookup"><span data-stu-id="2324f-127">Microphone (SoundMAX Integrated Digital HD Audio)</span></span></p></td>
<td><p><span data-ttu-id="2324f-128">Headset-Kopfhörer (Microsoft LifeChat LX-3000)</span><span class="sxs-lookup"><span data-stu-id="2324f-128">Headset Earphone (Microsoft LifeChat LX-3000)</span></span></p></td>
<td><p><span data-ttu-id="2324f-129">254</span><span class="sxs-lookup"><span data-stu-id="2324f-129">254</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-130">Mikrofon (SoundMAX Integrated Digital HD Audio)</span><span class="sxs-lookup"><span data-stu-id="2324f-130">Microphone (SoundMAX Integrated Digital HD Audio)</span></span></p></td>
<td><p><span data-ttu-id="2324f-131">Lautsprecher (SoundMAX Integrated Digital HD Audio)</span><span class="sxs-lookup"><span data-stu-id="2324f-131">Speakers (SoundMAX Integrated Digital HD Audio)</span></span></p></td>
<td><p><span data-ttu-id="2324f-132">319</span><span class="sxs-lookup"><span data-stu-id="2324f-132">319</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="2324f-p105">Wenn Sie lieber die Gesamtsumme für ein bestimmtes Gerät angezeigt bekommen möchten (z. B. für das SoundMAX-Aufnahmegerät, unabhängig vom verwendeten Darstellungsgerät), wählen Sie die entsprechende Option in der Dropdownliste „Gerätetyp“ aus (entweder „Aufnahmegerät“ oder „Darstellungsgerät“). Wenn Sie im aktuellen Beispiel „Aufnahmegerät“ wählen, sieht die Ausgabe etwa so aus:</span><span class="sxs-lookup"><span data-stu-id="2324f-p105">If you would rather see combined totals for a given device (for example, for the SoundMAX capture device, regardless of the render device used), select the appropriate option from the Device type dropdown list (either Capture device or Render device). If you select Capture device in this example, that will give you output similar to this:</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2324f-135">Aufnahmegerät</span><span class="sxs-lookup"><span data-stu-id="2324f-135">Capture device</span></span></th>
<th><span data-ttu-id="2324f-136">Anruflautstärke</span><span class="sxs-lookup"><span data-stu-id="2324f-136">Call volume</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2324f-137">Mikrofon (SoundMAX Integrated Digital HD Audio)</span><span class="sxs-lookup"><span data-stu-id="2324f-137">Microphone (SoundMAX Integrated Digital HD Audio)</span></span></p></td>
<td><p><span data-ttu-id="2324f-138">573</span><span class="sxs-lookup"><span data-stu-id="2324f-138">573</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="accessing-the-device-report"></a><span data-ttu-id="2324f-139">Öffnen des Geräteberichts</span><span class="sxs-lookup"><span data-stu-id="2324f-139">Accessing the Device Report</span></span>

<span data-ttu-id="2324f-140">Auf den Gerätebericht greifen Sie über die Startseite für Überwachungsberichte zu.</span><span class="sxs-lookup"><span data-stu-id="2324f-140">The Device Report is typically accessed from the Monitoring Reports home page.</span></span> <span data-ttu-id="2324f-141">Wenn Sie jedoch den [Anruf Detail Bericht in lync Server 2013](lync-server-2013-call-detail-report.md) anzeigen, können Sie einen Drilldown zum gerätebericht für ein bestimmtes Gerät durchführen, indem Sie auf eine der folgenden Metriken klicken:</span><span class="sxs-lookup"><span data-stu-id="2324f-141">However, if you are viewing the [Call Detail Report in Lync Server 2013](lync-server-2013-call-detail-report.md) you can drill down to the Device Report for a specific device by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="2324f-142">Aufnahmegerät</span><span class="sxs-lookup"><span data-stu-id="2324f-142">Capture Device</span></span>

  - <span data-ttu-id="2324f-143">Darstellungsgerät</span><span class="sxs-lookup"><span data-stu-id="2324f-143">Render Device</span></span>

<span data-ttu-id="2324f-144">Im gerätebericht können Sie einen Drilldown zum [Anruflistenbericht in lync Server 2013](lync-server-2013-call-list-report.md) durchführen, indem Sie auf eine der folgenden Metriken klicken:</span><span class="sxs-lookup"><span data-stu-id="2324f-144">From the Device Report you can drill down to the [Call List Report in Lync Server 2013](lync-server-2013-call-list-report.md) by clicking either of the following metrics:</span></span>

  - <span data-ttu-id="2324f-145">Anruflautstärke</span><span class="sxs-lookup"><span data-stu-id="2324f-145">Call volume</span></span>

  - <span data-ttu-id="2324f-146">Prozentsatz der Anrufe schlechter Qualität</span><span class="sxs-lookup"><span data-stu-id="2324f-146">Poor call percentage</span></span>

</div>

<div>

## <a name="making-the-best-use-of-the-device-report"></a><span data-ttu-id="2324f-147">Optimales Nutzen des Geräteberichts</span><span class="sxs-lookup"><span data-stu-id="2324f-147">Making the Best Use of the Device Report</span></span>

<span data-ttu-id="2324f-148">Im Hinblick auf Gerätenamen ist der Gerätebericht besonders detailliert. Beispielsweise könnten die folgenden Aufnahmegeräte vorhanden sein:</span><span class="sxs-lookup"><span data-stu-id="2324f-148">When it comes to device names, the Device Report is extremely detailed; for example, suppose you have the following capture devices:</span></span>

  - <span data-ttu-id="2324f-149">Aastra 3002-Mikrofon (2- Aastra 3002)</span><span class="sxs-lookup"><span data-stu-id="2324f-149">Aastra 3002 Microphone (2- Aastra 3002)</span></span>

  - <span data-ttu-id="2324f-150">Aastra 3002-Mikrofon (3- Aastra 3002)</span><span class="sxs-lookup"><span data-stu-id="2324f-150">Aastra 3002 Microphone (3- Aastra 3002)</span></span>

  - <span data-ttu-id="2324f-151">Aastra 3002-Mikrofon (Aastra 3002)</span><span class="sxs-lookup"><span data-stu-id="2324f-151">Aastra 3002 Microphone (Aastra 3002)</span></span>

  - <span data-ttu-id="2324f-152">Aastra 6725ip</span><span class="sxs-lookup"><span data-stu-id="2324f-152">Aastra 6725ip</span></span>

  - <span data-ttu-id="2324f-153">Aastra 6725ip-Mikrofon (10- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="2324f-153">Aastra 6725ip Microphone (10- Aastra 6725ip)</span></span>

  - <span data-ttu-id="2324f-154">Aastra 6725ip-Mikrofon (10- Aastra 6725ip)-V0</span><span class="sxs-lookup"><span data-stu-id="2324f-154">Aastra 6725ip Microphone (10- Aastra 6725ip)-V0</span></span>

  - <span data-ttu-id="2324f-155">Aastra 6725ip-Mikrofon (2- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="2324f-155">Aastra 6725ip Microphone (2- Aastra 6725ip)</span></span>

  - <span data-ttu-id="2324f-156">Aastra 6725ip-Mikrofon (3- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="2324f-156">Aastra 6725ip Microphone (3- Aastra 6725ip)</span></span>

  - <span data-ttu-id="2324f-157">Aastra 6725ip-Mikrofon (4- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="2324f-157">Aastra 6725ip Microphone (4- Aastra 6725ip)</span></span>

  - <span data-ttu-id="2324f-158">Aastra 6725ip-Mikrofon (5- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="2324f-158">Aastra 6725ip Microphone (5- Aastra 6725ip)</span></span>

  - <span data-ttu-id="2324f-159">Aastra 6725ip-Mikrofon (6- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="2324f-159">Aastra 6725ip Microphone (6- Aastra 6725ip)</span></span>

  - <span data-ttu-id="2324f-160">Aastra 6725ip-Mikrofon (7- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="2324f-160">Aastra 6725ip Microphone (7- Aastra 6725ip)</span></span>

  - <span data-ttu-id="2324f-161">Aastra 6725ip-Mikrofon (9- Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="2324f-161">Aastra 6725ip Microphone (9- Aastra 6725ip)</span></span>

  - <span data-ttu-id="2324f-162">Aastra 6725ip-Mikrofon (9- Aastra 6725ip)-V0</span><span class="sxs-lookup"><span data-stu-id="2324f-162">Aastra 6725ip Microphone (9- Aastra 6725ip)-V0</span></span>

  - <span data-ttu-id="2324f-163">Aastra 6725ip-Mikrofon (Aastra 6725ip)</span><span class="sxs-lookup"><span data-stu-id="2324f-163">Aastra 6725ip Microphone (Aastra 6725ip)</span></span>

  - <span data-ttu-id="2324f-164">Aastra 6725ip-Mikrofon (Aastra 6725ip)-V0</span><span class="sxs-lookup"><span data-stu-id="2324f-164">Aastra 6725ip Microphone (Aastra 6725ip)-V0</span></span>

  - <span data-ttu-id="2324f-165">Aastra 6725ip-Mikrofon (USB-Audiogerät)</span><span class="sxs-lookup"><span data-stu-id="2324f-165">Aastra 6725ip Microphone (USB Audio Device)</span></span>

  - <span data-ttu-id="2324f-166">Aastra 6725ip-Mikrofon (USB-Audiogerät)-V0</span><span class="sxs-lookup"><span data-stu-id="2324f-166">Aastra 6725ip Microphone (USB Audio Device)-V0</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="2324f-167">Beachten Sie, dass die Namen von Aufnahmegeräten möglicherweise nicht identisch sind, wenn Sie lokalisierte Versionen von lync Server 2013 ausführen.</span><span class="sxs-lookup"><span data-stu-id="2324f-167">Keep in mind that capture device names might not be the same if you are running localized versions of Lync Server 2013.</span></span> <span data-ttu-id="2324f-168">Ein Gerät namens Aastra 6725ip-Mikrofon (Aastra 6725ip)-V0 hat wahrscheinlich auf Französisch oder Spanisch eine andere Bezeichnung.</span><span class="sxs-lookup"><span data-stu-id="2324f-168">A device named Aastra 6725ip Microphone (Aastra 6725ip)-V0 in US English could have a different name in French or Spanish.</span></span>



</div>

<span data-ttu-id="2324f-169">Oft benötigen Sie diese Detailebene; zu anderen Zeiten können Sie jedoch nur daran interessiert sein, wie viele Anrufe ein Aastra-Mikrofon verwenden, unabhängig von der Modellnummer.</span><span class="sxs-lookup"><span data-stu-id="2324f-169">Often times you'll want that level of detail; at other times, however, you might only be interested in how many calls use any Aastra microphone, regardless of model number.</span></span> <span data-ttu-id="2324f-170">Eine Möglichkeit zum Abrufen von Informationen wie der besteht darin, die Geräte Berichtsdaten nach Microsoft Excel zu exportieren und diese Daten dann in einer Datei mit durch Kommas getrennten Werten (beispielsweise C: \\ Daten \\ Geräte \_Report.csv) zu speichern.</span><span class="sxs-lookup"><span data-stu-id="2324f-170">One way to get information like that is to export the Device Report data to Microsoft Excel and then save that data to a comma-separated values file (for example, C:\\Data\\Devices\_Report.csv).</span></span> <span data-ttu-id="2324f-171">Sie können dann eine Reihe ähnlicher Befehle verwenden, um das zu importieren. CSV-Datei in Windows PowerShell und Berichterstattung über die Gesamtzahl der Anrufe, die mit einem Aastra-Aufnahmegerät durchgeführt wurden:</span><span class="sxs-lookup"><span data-stu-id="2324f-171">You can then use a set of commands similar to these to import the .CSV file into Windows PowerShell and report back the total number of calls made using an Aastra capture device:</span></span>

    $devices = Import-Csv "C:\Data\Device_Report.csv
    $sum = $devices | Where-Object {$_."Capture device" -match "Aastra"}
    $sum | foreach-object {[Int]$x = [Int]$x + [Int]$_."call volume"}
    $x

<span data-ttu-id="2324f-p109">Damit wird ein einzelner Wert zurückgegeben, der die Gesamtzahl der Anrufe angibt, die mit einem Aastra-Aufnahmegerät ausgeführt wurden. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2324f-p109">That will return a single value representing the total number of calls made using an Aastra capture device. For example:</span></span>

    384

</div>

<div>

## <a name="filters"></a><span data-ttu-id="2324f-174">Filter</span><span class="sxs-lookup"><span data-stu-id="2324f-174">Filters</span></span>

<span data-ttu-id="2324f-p110">Mithilfe von Filtern können Sie eine gezieltere Datenauswahl zurückgeben oder die zurückgegebenen Daten auf unterschiedliche Weise anzeigen. Beispielsweise können Sie im Gerätebericht nach dem Anruftyp filtern (d. h., ob der Anruf ein Clientanruf, eine Telefonkonferenz oder ein PSTN-Anruf ist). Sie können außerdem festlegen, wie Daten gruppiert werden sollen. In diesem Fall werden die Geräte nach Stunde, Tag, Woche oder Monat gruppiert.</span><span class="sxs-lookup"><span data-stu-id="2324f-p110">Filters provide a way for you to return a more finely-targeted set of data or to view the returned data in different ways. For example, the Device Report enables you to filter on such things as call type (that is, was the call a client call), a conference call, or a public switched telephone network (PSTN) call. You can also choose how data should be grouped. In this case, devices are grouped by hour, day, week, or month.</span></span>

<span data-ttu-id="2324f-179">In der folgenden Tabelle werden die Filter aufgelistet, die Sie im Gerätebericht verwenden können.</span><span class="sxs-lookup"><span data-stu-id="2324f-179">The following table lists the filters that you can use with the Device Report.</span></span>

### <a name="device-report-filters"></a><span data-ttu-id="2324f-180">Geräteberichtfilter</span><span class="sxs-lookup"><span data-stu-id="2324f-180">Device Report Filters</span></span>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2324f-181">Name</span><span class="sxs-lookup"><span data-stu-id="2324f-181">Name</span></span></th>
<th><span data-ttu-id="2324f-182">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2324f-182">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2324f-183"><strong>Von</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-183"><strong>From</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-p111">Anfangsdatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Anfangsdatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="2324f-p111">Start date/time for the time range. To view data by hours, enter both the start date and time as follows:</span></span></p>
<p><span data-ttu-id="2324f-186">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="2324f-186">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="2324f-p112">Wenn Sie keinen Anfangszeitpunkt eingeben, beginnt der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="2324f-p112">If you do not enter a start time, the report automatically begins at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="2324f-189">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="2324f-189">7/7/2012</span></span></p>
<p><span data-ttu-id="2324f-190">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="2324f-190">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="2324f-191">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="2324f-191">7/3/2012</span></span></p>
<p><span data-ttu-id="2324f-192">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="2324f-192">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-193"><strong>Bis</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-193"><strong>To</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-p113">Enddatum und -uhrzeit für den Zeitraum. Wenn die Daten nach Stunden angezeigt werden sollen, geben Sie Enddatum und -uhrzeit wie folgt ein:</span><span class="sxs-lookup"><span data-stu-id="2324f-p113">End date/time for the time range. To view data by hours, enter both the end date and time as follows:</span></span></p>
<p><span data-ttu-id="2324f-196">7/7/2012 1:00 Uhr</span><span class="sxs-lookup"><span data-stu-id="2324f-196">7/7/2012 1:00 PM</span></span></p>
<p><span data-ttu-id="2324f-p114">Wenn Sie keinen Endzeitpunkt eingeben, endet der Bericht automatisch am angegebenen Tag um 12:00 Uhr. Zum Anzeigen der Daten nach Tag geben Sie nur das Datum ein:</span><span class="sxs-lookup"><span data-stu-id="2324f-p114">If you do not enter an end time, the report automatically ends at 12:00 AM on the specified day. To view data by day, enter just the date:</span></span></p>
<p><span data-ttu-id="2324f-199">7/7/2012</span><span class="sxs-lookup"><span data-stu-id="2324f-199">7/7/2012</span></span></p>
<p><span data-ttu-id="2324f-200">Sollen die Daten nach Woche oder Monat angezeigt werden, geben Sie irgendein Datum ein, das in die anzuzeigende Woche oder den anzuzeigenden Monat fällt (Sie müssen nicht den ersten Tag der Woche oder des Monats eingeben):</span><span class="sxs-lookup"><span data-stu-id="2324f-200">To view by week or by month, enter a date that falls anywhere within the week or month that you want to view (you do not have to enter the first day of the week or month):</span></span></p>
<p><span data-ttu-id="2324f-201">7/3/2012</span><span class="sxs-lookup"><span data-stu-id="2324f-201">7/3/2012</span></span></p>
<p><span data-ttu-id="2324f-202">Eine Woche läuft immer von Sonntag bis einschließlich Samstag.</span><span class="sxs-lookup"><span data-stu-id="2324f-202">Weeks always run from Sunday through Saturday.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2324f-203"><strong>Ursache für die Sprachumschaltung</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-203"><strong>Voice switch cause</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-p115">Der Grund, weshalb der Halbduplex-Modus für einen Anruf verwendet werden musste, um Echo zu verhindern. Im Halbduplex-Modus ist die Kommunikation jeweils nur in eine Richtung möglich, ähnlich wie bei Funksprechgeräten, bei denen auch abwechselnd gesprochen wird. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="2324f-p115">Reason why a call had to be placed into half duplex mode in order to prevent echo. In half duplex mode, communication can travel in only one direction at a time, similar to the way users take turns when communicating with a walkie-talkie. Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-207">[Alle]</span><span class="sxs-lookup"><span data-stu-id="2324f-207">[All]</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-208">Keine</span><span class="sxs-lookup"><span data-stu-id="2324f-208">None</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-209">Ungültiger Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="2324f-209">Bad timestamp</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-210">Echo</span><span class="sxs-lookup"><span data-stu-id="2324f-210">Echo</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-211">DNLP (Dynamic Nonlinear Processor)</span><span class="sxs-lookup"><span data-stu-id="2324f-211">DNLP (dynamic nonlinear processor)</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-212">Geringe Komplexität</span><span class="sxs-lookup"><span data-stu-id="2324f-212">Low complexity</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-213">Ungültiger Gerätestatus</span><span class="sxs-lookup"><span data-stu-id="2324f-213">Bad device state</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-214">Echo nach AEC (Acoustic Echo Cancellation, Echounterdrückung)</span><span class="sxs-lookup"><span data-stu-id="2324f-214">Post-AEC echo (acoustic echo cancellation)</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-215"><strong>Ursache für Echo</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-215"><strong>Echo cause</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-p116">Der Grund, weshalb bei einem Anruf Echo über dem akzeptablen Niveau festgestellt wurde. (In der Telekommunikation handelt es sich bei Echo um eine Schallreflexion; dasselbe Phänomen tritt auf, wenn Sie in einen Brunnen rufen). Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="2324f-p116">Reason why echo above the accepted level was detected in a call. (In telecommunications, echo is a reflection of sound, the same phenomenon you will hear if you yell down to the bottom of a well.) Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-218">[Alle]</span><span class="sxs-lookup"><span data-stu-id="2324f-218">[All]</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-219">Keine</span><span class="sxs-lookup"><span data-stu-id="2324f-219">None</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-220">Ungültiger Zeitstempel</span><span class="sxs-lookup"><span data-stu-id="2324f-220">Bad timestamp</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-221">Echo nach AEC (Acoustic Echo Cancellation, Echounterdrückung)</span><span class="sxs-lookup"><span data-stu-id="2324f-221">Post-AEC echo (acoustic echo cancellation)</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-222">ANLP (Adaptive Nonlinear Processor)</span><span class="sxs-lookup"><span data-stu-id="2324f-222">ANLP (adaptive nonlinear processor)</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-223">DNLP (Dynamic Nonlinear Processor)</span><span class="sxs-lookup"><span data-stu-id="2324f-223">DNLP (dynamic nonlinear processor)</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-224">Mikrofon übersteuert</span><span class="sxs-lookup"><span data-stu-id="2324f-224">Microphone clipping</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2324f-225"><strong>Anruftyp</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-225"><strong>Call type</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-p117">Gibt an, welcher Typ von Anruf getätigt wurde. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="2324f-p117">Indicates the type of call that was made. Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-228">[Alle]</span><span class="sxs-lookup"><span data-stu-id="2324f-228">[All]</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-229">Clientanruf</span><span class="sxs-lookup"><span data-stu-id="2324f-229">Client call</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-230">PSTN-Anruf</span><span class="sxs-lookup"><span data-stu-id="2324f-230">PSTN call</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-231">Telefonkonferenz</span><span class="sxs-lookup"><span data-stu-id="2324f-231">Conference call</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-232"><strong>Zugriffstyp</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-232"><strong>Access type</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-p118">Gibt an, ob der Client am internen oder am externen Netzwerk angemeldet wurde, als der Anruf getätigt wurde. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="2324f-p118">Indicates whether the client was logged on to the internal network or the external network when the call was placed. Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-235">[Alle]</span><span class="sxs-lookup"><span data-stu-id="2324f-235">[All]</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-236">Intern</span><span class="sxs-lookup"><span data-stu-id="2324f-236">Internal</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-237">Extern</span><span class="sxs-lookup"><span data-stu-id="2324f-237">External</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2324f-238"><strong>Netzwerktyp</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-238"><strong>Network type</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-p119">Gibt den Typ des Netzwerks an, mit dem der Client verbunden wurde, als der Anruf erfolgte. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="2324f-p119">Indicates the type of network the client was connected to when the call was placed. Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-241">[Alle]</span><span class="sxs-lookup"><span data-stu-id="2324f-241">[All]</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-242">Verkabelt</span><span class="sxs-lookup"><span data-stu-id="2324f-242">Wired</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-243">Funk</span><span class="sxs-lookup"><span data-stu-id="2324f-243">Wireless</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-244"><strong>VPN</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-244"><strong>VPN</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-p120">Gibt an, ob ein externer Client eine VPN-Verbindung (Virtual Private Network) verwendete, als der Anruf getätigt wurde. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="2324f-p120">Indicates whether an external client was using a virtual private network (VPN) connection when the call was placed. Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-247">[Alle]</span><span class="sxs-lookup"><span data-stu-id="2324f-247">[All]</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-248">VPN</span><span class="sxs-lookup"><span data-stu-id="2324f-248">VPN</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-249">Nicht-VPN</span><span class="sxs-lookup"><span data-stu-id="2324f-249">Non-VPN</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2324f-250"><strong>Gerätetyp</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-250"><strong>Device type</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-p121">Gibt den Typ des Geräts an. Wählen Sie eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="2324f-p121">Indicates the type of device. Select one of the following:</span></span></p>
<dl>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-253">Aufnahmegerät</span><span class="sxs-lookup"><span data-stu-id="2324f-253">Capture device</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-254">Darstellungsgerät</span><span class="sxs-lookup"><span data-stu-id="2324f-254">Render device</span></span></p>
</dd>
<dt><span></span></dt>
<dd><p><span data-ttu-id="2324f-255">Aufnahme-/Darstellungsgerätepaar</span><span class="sxs-lookup"><span data-stu-id="2324f-255">Capture/Render device pair</span></span></p>
</dd>
</dl></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-256"><strong>Gerätename</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-256"><strong>Device name</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-p122">Der Name des Aufnahme- oder Darstellungsgeräts. Sie können den vollständigen Gerätenamen oder einen Teil davon eingeben. Geben Sie beispielsweise wie folgt den vollständigen Gerätenamen ein, um nach dem Gerät „Mikrofon (Microsoft LifeCam VX-1000)“ zu suchen:</span><span class="sxs-lookup"><span data-stu-id="2324f-p122">Name of the capture or render device. You can enter the complete device name or any portion of the device name. For example, to find the device Microphone (Microsoft LifeCam VX-1000.), you can enter the complete device name as follows:</span></span></p>
<p><span data-ttu-id="2324f-260">Mikrofon (Microsoft LifeCam VX-1000)</span><span class="sxs-lookup"><span data-stu-id="2324f-260">Microphone (Microsoft LifeCam VX-1000.)</span></span></p>
<p><span data-ttu-id="2324f-p123">Sie können aber auch nur einen Teil des Namens eingeben. Beispiel:</span><span class="sxs-lookup"><span data-stu-id="2324f-p123">Or, you can enter just a portion of the name. For example:</span></span></p>
<p><span data-ttu-id="2324f-263">LifeCam</span><span class="sxs-lookup"><span data-stu-id="2324f-263">LifeCam</span></span></p>
<p><span data-ttu-id="2324f-264">Beachten Sie, dass der vorhergehende Filter jedes Gerät zurückgibt, das die Zeichenfolge &quot; LifeCam &quot; an einer beliebigen Stelle im Namen enthält.</span><span class="sxs-lookup"><span data-stu-id="2324f-264">Note that the preceding filter returns any device that contains the string &quot;LifeCam&quot; anywhere in its name.</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="metrics"></a><span data-ttu-id="2324f-265">Metriken</span><span class="sxs-lookup"><span data-stu-id="2324f-265">Metrics</span></span>

<span data-ttu-id="2324f-266">In der folgenden Tabelle werden Metriken aufgelistet, die im Gerätebericht angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="2324f-266">The following table lists the information provided in the Device Report.</span></span>

### <a name="device-report-metrics"></a><span data-ttu-id="2324f-267">Geräteberichtmetriken</span><span class="sxs-lookup"><span data-stu-id="2324f-267">Device Report Metrics</span></span>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="2324f-268">Name</span><span class="sxs-lookup"><span data-stu-id="2324f-268">Name</span></span></th>
<th><span data-ttu-id="2324f-269">Kann nach dieser Metrik sortiert werden?</span><span class="sxs-lookup"><span data-stu-id="2324f-269">Can you sort on this item?</span></span></th>
<th><span data-ttu-id="2324f-270">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="2324f-270">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="2324f-271"><strong>Aufnahmegerät</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-271"><strong>Capture device</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-272">Ja</span><span class="sxs-lookup"><span data-stu-id="2324f-272">Yes</span></span></p></td>
<td><p><span data-ttu-id="2324f-273">Ein Gerät (z. B. ein Mikrofon oder eine Webcam), das für die Übertragung von Audio verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2324f-273">Device (for example, a microphone or webcam) used for transmitting audio.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-274"><strong>Darstellungsgerät</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-274"><strong>Render device</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-275">Ja</span><span class="sxs-lookup"><span data-stu-id="2324f-275">Yes</span></span></p></td>
<td><p><span data-ttu-id="2324f-276">Ein Gerät (z. B. ein Headset oder Lautsprecher), das für den Empfang von Audio verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="2324f-276">Device (for example, a headset or speakers) used for receiving audio.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2324f-277"><strong>Anruflautstärke</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-277"><strong>Call volume</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-278">Ja</span><span class="sxs-lookup"><span data-stu-id="2324f-278">Yes</span></span></p></td>
<td><p><span data-ttu-id="2324f-279">Die Gesamtzahl der getätigten Anrufe.</span><span class="sxs-lookup"><span data-stu-id="2324f-279">Total number of calls placed.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-280"><strong>Prozentsatz der Anrufe schlechter Qualität</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-280"><strong>Poor call percentage</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-281">Ja</span><span class="sxs-lookup"><span data-stu-id="2324f-281">Yes</span></span></p></td>
<td><p><span data-ttu-id="2324f-282">Prozentsatz der Anrufe, die als "schlecht" klassifiziert wurden &quot; . &quot; Bei einem schlechten Anruf handelt es sich um einen Anruf, bei dem mindestens eine der gemessenen Metriken den zulässigen Wert überschritten hat (beispielsweise ein Anruf, bei dem übermäßiger Jitter zu sehen ist).</span><span class="sxs-lookup"><span data-stu-id="2324f-282">Percentage of calls that were classified as &quot;poor.&quot; A poor call is any call which at least one of the measured metrics exceeded the allowed value (for example, a call that experienced excessive jitter).</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2324f-283"><strong>Eindeutige Benutzer</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-283"><strong>Unique users</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-284">Ja</span><span class="sxs-lookup"><span data-stu-id="2324f-284">Yes</span></span></p></td>
<td><p><span data-ttu-id="2324f-p124">Die eindeutigen Benutzer, die das Gerät verwendet haben. Wenn ein Benutzer das Gerät 13 Mal verwendet hat, zählt er als ein eindeutiger Benutzer. Dasselbe gilt für einen Benutzer, der das Gerät nur ein einziges Mal verwendet hat.</span><span class="sxs-lookup"><span data-stu-id="2324f-p124">Unique users who used the device. If a user used the device 13 times he or she would count as one unique user, the same as a user who only used the device a single time.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-287"><strong>Anteil Sprachumschaltzeit</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-287"><strong>Ratio of voice switch time</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-288">Ja</span><span class="sxs-lookup"><span data-stu-id="2324f-288">Yes</span></span></p></td>
<td><p><span data-ttu-id="2324f-p125">Der Prozentsatz des Anrufs, der im Halbduplex-Modus getätigt werden musste, um Echo zu verhindern. Im Halbduplex-Modus ist die Kommunikation jeweils nur in eine Richtung möglich, ähnlich wie bei Funksprechgeräten, bei denen auch abwechselnd gesprochen wird.</span><span class="sxs-lookup"><span data-stu-id="2324f-p125">Percentage of the call that had to be conducted in half duplex mode in order to prevent echo. In half duplex mode, communication can travel in only one direction at a time, similar to the way users take turns when communicating with a walkie-talkie.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2324f-291"><strong>Anteil nicht funktionierendes Mikrofon</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-291"><strong>Ratio of microphone not functioning</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-292">Ja</span><span class="sxs-lookup"><span data-stu-id="2324f-292">Yes</span></span></p></td>
<td><p><span data-ttu-id="2324f-p126">Der Prozentsatz des Anrufs, bei dem das Aufnahmegerät nicht ordnungsgemäß funktionierte. Ein hoher Wert ist ein Hinweis, dass Qualitätsprobleme beim Anruf in erster Linie darauf zurückzuführen sind, dass das Aufnahmegerät nicht erwartungsgemäß funktionierte.</span><span class="sxs-lookup"><span data-stu-id="2324f-p126">Percentage of the call in which the capture device was not functioning at an acceptable level. A high values suggests that quality issues with the call were primarily due to the capture device not working as expected.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-295"><strong>Anteil nicht funktionierender Lautsprecher</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-295"><strong>Ratio of speaker not functioning</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-296">Ja</span><span class="sxs-lookup"><span data-stu-id="2324f-296">Yes</span></span></p></td>
<td><p><span data-ttu-id="2324f-p127">Der Prozentsatz des Anrufs, bei dem das Darstellungsgerät nicht ordnungsgemäß funktionierte. Ein hoher Wert ist ein Hinweis, dass Qualitätsprobleme beim Anruf in erster Linie darauf zurückzuführen sind, dass das Darstellungsgerät nicht erwartungsgemäß funktionierte.</span><span class="sxs-lookup"><span data-stu-id="2324f-p127">Percentage of the call in which the render device was not functioning at an acceptable level. A high values suggests that quality issues with the call were primarily due to the render device not working as expected.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2324f-299"><strong>Anrufe mit Sprachumschaltung (%)</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-299"><strong>Calls with voice switch (%)</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-300">Ja</span><span class="sxs-lookup"><span data-stu-id="2324f-300">Yes</span></span></p></td>
<td><p><span data-ttu-id="2324f-p128">Der Prozentsatz der Gesamtanrufe, die im Halbduplex-Modus getätigt werden mussten. Im Halbduplex-Modus ist die Kommunikation jeweils nur in eine Richtung möglich, ähnlich wie bei Funksprechgeräten, bei denen auch abwechselnd gesprochen wird.</span><span class="sxs-lookup"><span data-stu-id="2324f-p128">Percentage of the total calls which had to be placed into half duplex mode. In half duplex mode, communication can travel in only one direction at a time, similar to the way users take turns when communicating with a walkie-talkie.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-303"><strong>Echo in Mikrofon (%)</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-303"><strong>Echo microphone in (%)</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-304">Ja</span><span class="sxs-lookup"><span data-stu-id="2324f-304">Yes</span></span></p></td>
<td><p><span data-ttu-id="2324f-p129">Prozentsatz der Zeit, in der im Mikrofonaufnahme-Datenstrom Echo festgestellt wurde. In der Regel weisen Headsets oder Hörer niedrige Werte und Freisprechvorrichtungen oder eigenständige Lautsprecher höhere Werte auf. Bei Geräten, die eine integrierte akustische Echounterdrückung unterstützen, weisen hohe Werte auf eine Echoausbreitung hin. Für andere Geräte sollte diese Metrik nicht verwendet werden, um die Gerätequalität zu evaluieren.</span><span class="sxs-lookup"><span data-stu-id="2324f-p129">Percentage of time when echo was detected in the microphone capture stream. Typically, values are low for headsets or handsets, and higher for speaker phones or stand-alone speakers. For devices that support on-board acoustic echo cancellation, high values indicate echo leak. For other devices, this metric should not be used to evaluate device quality.</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="2324f-309"><strong>Echo-Übertragung (%)</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-309"><strong>Echo send (%)</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-310">Ja</span><span class="sxs-lookup"><span data-stu-id="2324f-310">Yes</span></span></p></td>
<td><p><span data-ttu-id="2324f-311">Der Prozentsatz an Echo, das an andere Benutzer übertragen wird.</span><span class="sxs-lookup"><span data-stu-id="2324f-311">Percentage of echo transmitted to other users.</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="2324f-312"><strong>Anrufe mit Echo (%)</strong></span><span class="sxs-lookup"><span data-stu-id="2324f-312"><strong>Calls with echo (%)</strong></span></span></p></td>
<td><p><span data-ttu-id="2324f-313">Ja</span><span class="sxs-lookup"><span data-stu-id="2324f-313">Yes</span></span></p></td>
<td><p><span data-ttu-id="2324f-314">Der Prozentsatz der Gesamtanrufe mit Echo über dem akzeptablen Niveau.</span><span class="sxs-lookup"><span data-stu-id="2324f-314">Percentage of the total calls that had echo exceeding the acceptable level.</span></span></p></td>
</tr>
</tbody>
</table><span data-ttu-id="2324f-315">


</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="2324f-315">


</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

