---
title: 'Lync Server 2013: Ändern der Einstellungen für Geräte Aktualisierungsprotokolldateien'
description: 'Lync Server 2013: Ändern Sie die Einstellungen für Geräte Aktualisierungsprotokolldateien.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify settings for Device Update log files
ms:assetid: 9b57f126-1853-43b3-bbd4-06401e6498bd
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182554(v=OCS.15)
ms:contentKeyID: 48184975
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4c2086e11a67207a00ca99773cc818106b16d05c
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445729"
---
# <a name="modify-settings-for-device-update-log-files-in-lync-server-2013"></a><span data-ttu-id="68821-103">Ändern der Einstellungen für Geräte Aktualisierungsprotokolldateien in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="68821-103">Modify settings for Device Update log files in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="68821-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="68821-104">

<span> </span></span></span>

<span data-ttu-id="68821-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="68821-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="68821-106">Mithilfe der lync Server-Systemsteuerung oder der lync Server-Verwaltungsshell können Sie die Einstellungen für die Protokollierung von Geräte Aktualisierungsinformationen in Ihrer Organisation ändern.</span><span class="sxs-lookup"><span data-stu-id="68821-106">You can change settings for how device update information is logged in your organization by using Lync Server Control Panel or Lync Server Management Shell.</span></span> <span data-ttu-id="68821-107">In der folgenden Tabelle wird aufgezeigt, welche Einstellungen änderbar sind und welches Tool (e) Sie verwenden, um die Einstellungen zu ändern.</span><span class="sxs-lookup"><span data-stu-id="68821-107">The following table shows which settings are modifiable, and which tool(s) you use to modify the settings.</span></span>

<span data-ttu-id="68821-108">Protokolleinstellungen können global oder pro Website geändert und angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="68821-108">Log settings can be changed and applied globally, or per site.</span></span>


<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="68821-109">Zu ändern</span><span class="sxs-lookup"><span data-stu-id="68821-109">To change</span></span></th>
<th><span data-ttu-id="68821-110">Verwendung</span><span class="sxs-lookup"><span data-stu-id="68821-110">Use</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="68821-111">Die maximale Größe (in Bytes) für eine Protokolldatei</span><span class="sxs-lookup"><span data-stu-id="68821-111">The maximum size (in bytes) for a log file</span></span></p></td>
<td><p><span data-ttu-id="68821-112">Lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="68821-112">Lync Server Control Panel</span></span></p>
<p><span data-ttu-id="68821-113">oder</span><span class="sxs-lookup"><span data-stu-id="68821-113">-or-</span></span></p>
<p><span data-ttu-id="68821-114">Lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="68821-114">Lync Server Management Shell</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68821-115">Die maximale Menge an Informationen (in Bytes), die im Cache gespeichert werden können</span><span class="sxs-lookup"><span data-stu-id="68821-115">The maximum amount of information (in bytes) that can be held in the cache</span></span></p></td>
<td><p><span data-ttu-id="68821-116">Lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="68821-116">Lync Server Control Panel</span></span></p>
<p><span data-ttu-id="68821-117">oder</span><span class="sxs-lookup"><span data-stu-id="68821-117">-or-</span></span></p>
<p><span data-ttu-id="68821-118">Lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="68821-118">Lync Server Management Shell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68821-119">Wie oft (in Minuten), um zwischengespeicherte Informationen in die Protokolldatei zu schreiben</span><span class="sxs-lookup"><span data-stu-id="68821-119">How often (in minutes) to write cached information to the log file</span></span></p></td>
<td><p><span data-ttu-id="68821-120">Lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="68821-120">Lync Server Control Panel</span></span></p>
<p><span data-ttu-id="68821-121">oder</span><span class="sxs-lookup"><span data-stu-id="68821-121">-or-</span></span></p>
<p><span data-ttu-id="68821-122">Lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="68821-122">Lync Server Management Shell</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68821-123">Wie lange (in Tagen) Protokolldateien aufbewahrt werden</span><span class="sxs-lookup"><span data-stu-id="68821-123">How long (in days) to keep log files</span></span></p></td>
<td><p><span data-ttu-id="68821-124">Lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="68821-124">Lync Server Control Panel</span></span></p>
<p><span data-ttu-id="68821-125">oder</span><span class="sxs-lookup"><span data-stu-id="68821-125">-or-</span></span></p>
<p><span data-ttu-id="68821-126">Lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="68821-126">Lync Server Management Shell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68821-127">Zeitpunkt (Tageszeit) zum Überprüfen auf abgelaufene Dateien, die gelöscht werden sollen</span><span class="sxs-lookup"><span data-stu-id="68821-127">When (time of day) to check for expired files that should be deleted</span></span></p></td>
<td><p><span data-ttu-id="68821-128">Lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="68821-128">Lync Server Management Shell</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="68821-129">Welche Protokolldatei Erweiterungen zugelassen werden sollen</span><span class="sxs-lookup"><span data-stu-id="68821-129">What log file extensions to permit</span></span></p></td>
<td><p><span data-ttu-id="68821-130">Lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="68821-130">Lync Server Management Shell</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="68821-131">Welche Protokolldatei Typen beibehalten werden sollen</span><span class="sxs-lookup"><span data-stu-id="68821-131">Which log file types to retain</span></span></p></td>
<td><p><span data-ttu-id="68821-132">Lync Server-Verwaltungsshell</span><span class="sxs-lookup"><span data-stu-id="68821-132">Lync Server Management Shell</span></span></p></td>
</tr>
</tbody>
</table>


<div>

## <a name="to-change-logging-settings-by-using-lync-server-control-panel"></a><span data-ttu-id="68821-133">So ändern Sie die Protokollierungseinstellungen mithilfe der lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="68821-133">To change logging settings by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="68821-134">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="68821-134">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="68821-135">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="68821-135">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

2.  <span data-ttu-id="68821-136">Klicken Sie in der linken Navigationsleiste auf **Clients**, und klicken Sie dann auf **geräteprotokoll Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="68821-136">In the left navigation bar, click **Clients**, and then click **Device Log Configuration**.</span></span>

3.  <span data-ttu-id="68821-137">Doppelklicken Sie auf der Seite **Device Log-Konfiguration** auf die Konfiguration, die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="68821-137">On the **Device Log Configuration** page, double-click the configuration that you want to change.</span></span>

4.  <span data-ttu-id="68821-138">Ändern Sie im Dialogfeld **Protokolleinstellung bearbeiten** eine der folgenden Einstellungen:</span><span class="sxs-lookup"><span data-stu-id="68821-138">In the **Edit Log Setting** dialog box, change any of the following settings:</span></span>
    
      - <span data-ttu-id="68821-139">**Maximale Dateigröße (Bytes)**   Gibt die maximale Größe an, die eine Protokolldatei erhalten kann, bevor Sie bereinigt wird.</span><span class="sxs-lookup"><span data-stu-id="68821-139">**Maximum file size (bytes)**   Specifies the maximum size a log file can become before it is purged.</span></span> <span data-ttu-id="68821-140">Der Standardwert ist 1.024.000 Bytes (1 MB).</span><span class="sxs-lookup"><span data-stu-id="68821-140">The default is 1,024,000 bytes (1 MB).</span></span>
    
      - <span data-ttu-id="68821-141">**Maximale Cachegröße (Bytes)**   Gibt die maximale Menge an Informationen (in Byte) an, die im Protokolldatei Cache gespeichert werden können, bevor dieser Cache gelöscht werden muss und die Daten in eine Protokolldatei geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="68821-141">**Maximum cache size (bytes)**   Specifies the maximum amount of information (in bytes) that can be held in the log file cache before that cache must be cleared and the data is written to a log file.</span></span> <span data-ttu-id="68821-142">Der Standardwert ist 512.000 Bytes (0,5 MB).</span><span class="sxs-lookup"><span data-stu-id="68821-142">The default is 512,000 bytes (0.5 MB).</span></span>
    
      - <span data-ttu-id="68821-143">**Anzahl der Minuten zum Leeren des Caches (1-60)**   Gibt an, wie oft im Protokolldatei Cache gespeicherte Informationen in die eigentliche Protokolldatei geschrieben werden.</span><span class="sxs-lookup"><span data-stu-id="68821-143">**Number of minutes to flush cache (1-60)**   Indicates how often information stored in the log file cache is written to the actual log file.</span></span> <span data-ttu-id="68821-144">Nachdem die Daten protokolliert wurden, wird der Cache gelöscht.</span><span class="sxs-lookup"><span data-stu-id="68821-144">After the data is logged, the cache is cleared.</span></span> <span data-ttu-id="68821-145">Der Standardwert ist fünf Minuten.</span><span class="sxs-lookup"><span data-stu-id="68821-145">The default is five minutes.</span></span>
    
      - <span data-ttu-id="68821-146">**Anzahl der Tage, an denen Protokolldateien gespeichert werden sollen (1-365)**   Gibt an, wie viele Tage die Protokolldateien aufbewahrt werden, bevor Sie gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="68821-146">**Number of days to keep log files (1-365)**   Specifies the number of days the log files are kept before they are purged.</span></span> <span data-ttu-id="68821-147">Der Standardwert ist 10 Tage.</span><span class="sxs-lookup"><span data-stu-id="68821-147">The default is 10 days.</span></span>

5.  <span data-ttu-id="68821-148">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="68821-148">Click **Commit**.</span></span>

</div>

<div>

## <a name="changing-logging-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="68821-149">Ändern der Protokollierungseinstellungen mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="68821-149">Changing Logging Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="68821-150">Einstellungen für die Geräteupdate Protokolldatei können mithilfe von Windows PowerShell und dem Cmdlet " **Satz-CsDeviceUpdateConfiguration** " geändert werden.</span><span class="sxs-lookup"><span data-stu-id="68821-150">Device update log file settings can be modified by using Windows PowerShell and the **Set-CsDeviceUpdateConfiguration** cmdlet.</span></span> <span data-ttu-id="68821-151">Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="68821-151">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="68821-152">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A> .</span><span class="sxs-lookup"><span data-stu-id="68821-152">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at <A href="https://go.microsoft.com/fwlink/p/?linkid=255876">https://go.microsoft.com/fwlink/p/?linkId=255876</A>.</span></span>



</div>

<span data-ttu-id="68821-153">Die folgenden Beispiele zeigen eine Reihe von Möglichkeiten, wie Sie mit " **CsDeviceUpdateConfiguration** " Einstellungen ändern können.</span><span class="sxs-lookup"><span data-stu-id="68821-153">The following examples show a couple of the ways that you can use **Set-CsDeviceUpdateConfiguration** to modify settings.</span></span>

<div>

## <a name="to-modify-the-maximum-log-file-size-and-the-log-cleanup-interval"></a><span data-ttu-id="68821-154">So ändern Sie die maximale Protokolldateigröße und das Protokoll Bereinigungsintervall</span><span class="sxs-lookup"><span data-stu-id="68821-154">To modify the maximum log file size and the log cleanup interval</span></span>

  - <span data-ttu-id="68821-155">Mit dem folgenden Befehl werden die Einstellungen für das Geräteupdate Protokoll geändert, die auf die Redmond-Website angewendet wurden.</span><span class="sxs-lookup"><span data-stu-id="68821-155">The following command modifies the device update log settings applied to the Redmond site.</span></span> <span data-ttu-id="68821-156">In diesem Beispiel ist die maximale Protokolldateigröße auf 204800 Bytes und das Protokoll Bereinigungsintervall auf 14 Tage eingestellt.</span><span class="sxs-lookup"><span data-stu-id="68821-156">In this example, the maximum log file size is set to 204800 bytes and the log cleanup interval is set to 14 days.</span></span>
    
        Set-CsDeviceUpdateConfiguration -Identity "site:Redmond" -MaxLogFileSize 204800 -LogCleanUpInterval 14.00:00:00

</div>

<div>

## <a name="to-modify-the-log-cleanup-time-of-day"></a><span data-ttu-id="68821-157">So ändern Sie die Zeit für die Protokoll Bereinigung</span><span class="sxs-lookup"><span data-stu-id="68821-157">To modify the log cleanup time of day</span></span>

  - <span data-ttu-id="68821-158">Mit diesem Befehl wird die Protokoll Bereinigungszeit für die Website "Redmond" auf 3:00 Uhr festgelegt.</span><span class="sxs-lookup"><span data-stu-id="68821-158">This command sets the log cleanup time for the Redmond site to 3:00 AM.</span></span>
    
        Set-CsDeviceUpdateConfiguration -Identity "site:Redmond" -LogCleanupTimeOfDay 03:00

</div>

<span data-ttu-id="68821-159">Ausführliche Informationen finden Sie im Hilfethema zum Cmdlet " [Satz-CsDeviceUpdateConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsDeviceUpdateConfiguration) ".</span><span class="sxs-lookup"><span data-stu-id="68821-159">For details, see the Help topic for the [Set-CsDeviceUpdateConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsDeviceUpdateConfiguration) cmdlet.</span></span>

<span data-ttu-id="68821-160"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="68821-160"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

