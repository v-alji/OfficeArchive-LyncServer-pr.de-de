---
title: 'Lync Server 2013: Konfigurieren der Videobandbreite'
description: 'Lync Server 2013: Konfigurieren der Videobandbreite'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring video bandwidth in Lync Server
ms:assetid: 446bed91-b26f-4ab2-b2f5-36e6810b405b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204842(v=OCS.15)
ms:contentKeyID: 48183984
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 85fedbe2fb856696236e79c3bbcece34d5af4a34
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49432415"
---
# <a name="configuring-video-bandwidth-in-lync-server-2013"></a><span data-ttu-id="79576-103">Konfigurieren der Videobandbreite in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="79576-103">Configuring video bandwidth in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="79576-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="79576-104">

<span> </span></span></span>

<span data-ttu-id="79576-105">_**Letztes Änderungsdatum des Themas:** 2012-10-02_</span><span class="sxs-lookup"><span data-stu-id="79576-105">_**Topic Last Modified:** 2012-10-02_</span></span>

<span data-ttu-id="79576-106">Lync Server 2013 umfasst verschiedene Einstellungen für die Verwaltung von Video für zwei-Parteien-Anrufe und Mehrparteienkonferenzen.</span><span class="sxs-lookup"><span data-stu-id="79576-106">Lync Server 2013 includes several settings for managing video for two-party calls and multiparty conferences.</span></span> <span data-ttu-id="79576-107">Wenn Sie lync Server 2013 bereitstellen, sollten Sie überprüfen, ob die Standardeinstellungen für Ihre Organisation geeignet sind, und Sie bei Bedarf ändern.</span><span class="sxs-lookup"><span data-stu-id="79576-107">When you deploy Lync Server 2013, you should evaluate whether the default settings are appropriate for your organization, and modify them as necessary.</span></span>

<span data-ttu-id="79576-108">Die in diesem Abschnitt beschriebenen Parameter gelten sowohl für zwei-Parteien-Anrufe als auch für mehr Parteien-Konferenzen.</span><span class="sxs-lookup"><span data-stu-id="79576-108">The parameters described in this section apply to both two-party calls and multiparty conferencing.</span></span> <span data-ttu-id="79576-109">Sie können diese Einstellungen mithilfe eines der folgenden Cmdlets anzeigen oder ändern:</span><span class="sxs-lookup"><span data-stu-id="79576-109">View or modify these settings by using one of the following cmdlets:</span></span>

  - <span data-ttu-id="79576-110">**Get-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="79576-110">**Get-CsConferencingPolicy**</span></span>

  - <span data-ttu-id="79576-111">**Set-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="79576-111">**Set-CsConferencingPolicy**</span></span>

  - <span data-ttu-id="79576-112">**New-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="79576-112">**New-CsConferencingPolicy**</span></span>

<span data-ttu-id="79576-113">Überprüfen Sie die folgenden Einstellungen in ihrer konferenzrichtlinie:</span><span class="sxs-lookup"><span data-stu-id="79576-113">Verify the following settings in your conferencing policy:</span></span>

  - <span data-ttu-id="79576-114">**VideoBitRateKb**   Diese Einstellung gibt die maximale Video Bitrate in Kbit/s für Video an, die von einem Benutzer gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="79576-114">**VideoBitRateKb**   This setting specifies the maximum video bit rate in kilobits per second (kbps) used for video sent by a user.</span></span> <span data-ttu-id="79576-115">Der Standardwert ist 50000 Kbit/s.</span><span class="sxs-lookup"><span data-stu-id="79576-115">The default value is 50000 kbps.</span></span> <span data-ttu-id="79576-116">Gültige Werte sind 0 bis 50000.</span><span class="sxs-lookup"><span data-stu-id="79576-116">Valid values are 0 to 50000.</span></span>
    
    <span data-ttu-id="79576-117">Diese Einstellung gilt separat für Haupt-und Panorama Video.</span><span class="sxs-lookup"><span data-stu-id="79576-117">This setting applies separately to main video and panoramic video.</span></span>
    
    <span data-ttu-id="79576-118">Beispiel: Wenn Sie 2000 Kbit/s angeben, kann lync Server 2000 Kbit/s für den Haupt Videostream und 2000 Kbit/s für den Panorama-Videostream senden.</span><span class="sxs-lookup"><span data-stu-id="79576-118">Example: if you specify 2000 kbps, then Lync Server can send 2000 kbps for the main video stream and 2000 kbps for the panoramic video stream.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="79576-119">Die maximale Video Netzwerkbandbreite für einen lync 2013-Endpunkt beträgt 8000 kBit/s für das Hauptvideo und 2500 Kbit/s für Panorama Video.</span><span class="sxs-lookup"><span data-stu-id="79576-119">The maximum video network bandwidth for a Lync 2013 endpoint is 8000 kbps for the main video and 2500 kbps for panoramic video.</span></span> <span data-ttu-id="79576-120">Diese Höchstwerte werden nur erreicht, wenn mehrere Videos empfangen oder gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="79576-120">These maximum values are reached only if multiple videos are received or sent.</span></span> <span data-ttu-id="79576-121">Ausführliche Informationen finden Sie im Abschnitt "Verwendung des Medien Verkehrs Netzwerks" unter <A href="lync-server-2013-network-bandwidth-requirements-for-media-traffic.md">Netzwerkbandbreite für den Mediendatenverkehr in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="79576-121">For details, see the "Media Traffic Network Usage" section in <A href="lync-server-2013-network-bandwidth-requirements-for-media-traffic.md">Network bandwidth requirements for media traffic in Lync Server 2013</A>.</span></span> <span data-ttu-id="79576-122">In diesem Abschnitt werden die maximale und typische Videodatenstrom Bandbreite für alle unterstützten Auflösungen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="79576-122">This section lists the maximum and typical video stream bandwidth for all supported resolutions.</span></span>

    
    </div>

  - <span data-ttu-id="79576-123">**TotalReceiveVideoBitRateKb**   Diese Einstellung, die in lync Server 2013 neu ist, gibt die maximal zulässige Bitrate (in Kbit/s) für alle Videodatenströme an, die von einem Client empfangen werden.</span><span class="sxs-lookup"><span data-stu-id="79576-123">**TotalReceiveVideoBitRateKb**   This setting, which is new in Lync Server 2013, specifies the maximum allowed bitrate (in kilobits per second) for all the video streams received by a client.</span></span> <span data-ttu-id="79576-124">Das bedeutet, dass die kombinierte Gesamtsumme für alle Videostreams, mit Ausnahme von Panorama-Videostreams, angegeben wird, die ein Client empfangen kann.</span><span class="sxs-lookup"><span data-stu-id="79576-124">That is, it specifies the combined total for all the video streams, except for panoramic video streams, that a client can receive.</span></span> <span data-ttu-id="79576-125">Wenn Sie beispielsweise 1500 kBit/s angeben, kann ein Client bis zu 1500 kBit/s des Videos empfangen, das aus mehreren Videoströmen oder einem einzelnen Videostream bestehen kann.</span><span class="sxs-lookup"><span data-stu-id="79576-125">For example, if you specify 1500 kbps, then a client can receive up to 1500 kbps of video, which may consist of multiple video streams or a single video stream.</span></span> <span data-ttu-id="79576-126">Diese Einstellung gilt nur für lync Server 2013-Clients.</span><span class="sxs-lookup"><span data-stu-id="79576-126">This setting applies only to Lync Server 2013 clients.</span></span>
    
    <span data-ttu-id="79576-127">Der Standardwert für **TotalReceiveVideoBitRateKb** ist 50000 Kbit/s.</span><span class="sxs-lookup"><span data-stu-id="79576-127">The default value for **TotalReceiveVideoBitRateKb** is 50000 kbps.</span></span> <span data-ttu-id="79576-128">Wenn die **EnableMultiviewJoin** -Einstellung für die Katalogansicht auf "true" festgelegt ist, darf **TotalReceiveVideoBitRateKb** nicht unter 420 Kbit/s festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="79576-128">If the **EnableMultiviewJoin** setting for Gallery View is set to True, **TotalReceiveVideoBitRateKb** must not be set below 420 kbps.</span></span> <span data-ttu-id="79576-129">Wenn die **EnableMultiviewJoin** -Einstellung für die Katalogansicht auf "false" festgelegt ist, darf **TotalReceiveVideoBitRateKb** nicht unter 100 kbit/s festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="79576-129">If the **EnableMultiviewJoin** setting for Gallery View is set to False, **TotalReceiveVideoBitRateKb** must not be set below 100 kbps.</span></span> <span data-ttu-id="79576-130">Wenn **EnableMultiviewJoin** auf "true" festgelegt ist und Sie den Wert unter 420 Kbit/s festlegen, werden die Werte standardmäßig auf den Schwellenwert festgelegt.</span><span class="sxs-lookup"><span data-stu-id="79576-130">If **EnableMultiviewJoin** is set to True and you set the value below 420 kbps, the values will default to the threshold value.</span></span> <span data-ttu-id="79576-131">Dieser Grenzwert hilft bei der Vermeidung versehentlicher Fehlkonfiguration, die zu einer schlechten Benutzererfahrung führen kann.</span><span class="sxs-lookup"><span data-stu-id="79576-131">This threshold helps prevent accidental misconfiguration that might result in poor user experience.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="79576-132">Details zur <STRONG>EnableMultiviewJoin</STRONG> -Einstellung finden Sie unter <A href="lync-server-2013-configuring-gallery-view.md">Konfigurieren der Katalogansicht in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="79576-132">For details about the <STRONG>EnableMultiviewJoin</STRONG> setting, see <A href="lync-server-2013-configuring-gallery-view.md">Configuring Gallery View in Lync Server 2013</A>.</span></span>

    
    </div>

  - <span data-ttu-id="79576-133">**MaxVideoConferencingResolution**   Dieser Parameter wird für lync Server 2013-Clients in lync Server 2013-Konferenzen nicht mehr verwendet.</span><span class="sxs-lookup"><span data-stu-id="79576-133">**MaxVideoConferencingResolution**   This parameter is no longer used for Lync Server 2013 clients in Lync Server 2013 conferences.</span></span> <span data-ttu-id="79576-134">Lync Server 2013-Konferenzen verwenden die Bitraten Steuerelemente, die weiter oben in diesem Abschnitt beschrieben wurden.</span><span class="sxs-lookup"><span data-stu-id="79576-134">Lync Server 2013 conferences use the bit rate controls described earlier in this section.</span></span> <span data-ttu-id="79576-135">Diese Einstellung wird weiterhin für Legacy-Clients verwendet, die einer lync Server 2013-Konferenz beitreten.</span><span class="sxs-lookup"><span data-stu-id="79576-135">This setting is still used for legacy clients joining a Lync Server 2013 conference.</span></span> <span data-ttu-id="79576-136">Dieser Parameter bestimmt die maximale Auflösung, die für Legacyclients in Konferenzen zulässig ist, die von Benutzern organisiert werden, die in lync Server 2013 verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="79576-136">This parameter determines the maximum resolution allowed for legacy clients in conferences organized by users who are homed on Lync Server 2013.</span></span> <span data-ttu-id="79576-137">Legacy-Clients werden also genauso behandelt wie in früheren Versionen von lync Server oder Office Communications Server.</span><span class="sxs-lookup"><span data-stu-id="79576-137">That is, legacy clients are treated the same as they were in previous versions of Lync Server or Office Communications Server.</span></span>

<span data-ttu-id="79576-138">Überprüfen Sie zusätzlich zu den Einstellungen für Konferenzrichtlinien, die für Benutzer gelten, die Einstellungen für die Medienkonfiguration.</span><span class="sxs-lookup"><span data-stu-id="79576-138">In addition to conferencing policy settings that apply to users, evaluate media configuration settings.</span></span> <span data-ttu-id="79576-139">Sie können diese Einstellungen mithilfe eines der folgenden Cmdlets anzeigen oder ändern:</span><span class="sxs-lookup"><span data-stu-id="79576-139">View or modify these settings by using one of the following cmdlets:</span></span>

  - <span data-ttu-id="79576-140">**Get-CsMediaConfiguration**</span><span class="sxs-lookup"><span data-stu-id="79576-140">**Get-CsMediaConfiguration**</span></span>

  - <span data-ttu-id="79576-141">**Satz-CsMediaConfiguration**</span><span class="sxs-lookup"><span data-stu-id="79576-141">**Set- CsMediaConfiguration**</span></span>

  - <span data-ttu-id="79576-142">**Neu – CsMediaConfiguration**</span><span class="sxs-lookup"><span data-stu-id="79576-142">**New- CsMediaConfiguration**</span></span>

<span data-ttu-id="79576-143">Überprüfen Sie die folgende Einstellung:</span><span class="sxs-lookup"><span data-stu-id="79576-143">Verify the following setting:</span></span>

  - <span data-ttu-id="79576-144">**MaxVideoRateAllowed**   Diese Einstellung pro Pool gibt die maximale Rate an, mit der Videosignale an den Clientendpunkten übertragen werden.</span><span class="sxs-lookup"><span data-stu-id="79576-144">**MaxVideoRateAllowed**   This per-pool setting specifies the maximum rate at which video signals will be transferred at the client endpoints.</span></span> <span data-ttu-id="79576-145">Sie gilt nur für frühere Versionen von lync Server-Clients.</span><span class="sxs-lookup"><span data-stu-id="79576-145">It applies only to previous versions of Lync Server clients.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="79576-146">Lync Server 2013-Clients ignorieren diese Einstellung und verwenden stattdessen die TotalReceiveVideoBitRateKb-Einstellung in Konferenzrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="79576-146">Lync Server 2013 clients ignore this setting and use the TotalReceiveVideoBitRateKb setting in conferencing policy instead.</span></span>

    
    </div>
    
    <span data-ttu-id="79576-147">Der Standardwert ist 720p.</span><span class="sxs-lookup"><span data-stu-id="79576-147">The default value is HD720P.</span></span> <span data-ttu-id="79576-148">Gültige Werte sind HD720p15M, VGA600K und CIF250K.</span><span class="sxs-lookup"><span data-stu-id="79576-148">Valid values are HD720p15M, VGA600K, and CIF250K.</span></span>
    
    <span data-ttu-id="79576-149">Beispiel: Wenn Sie 1500 kBit/s angeben, können alle Legacyclients im Pool bis zu 1500 kBit/s Video in zwei-oder Mehrparteienkonferenzen empfangen.</span><span class="sxs-lookup"><span data-stu-id="79576-149">Example: If you specify 1500 kbps, then all the legacy clients in the pool can receive up to 1500 kbps of video in two-party or multiparty conferences.</span></span>

<span data-ttu-id="79576-150">Die folgenden Verfahren sind Beispiele für die Verwendung der lync Server-Verwaltungsshell zum Ändern der in diesem Abschnitt beschriebenen Einstellungen.</span><span class="sxs-lookup"><span data-stu-id="79576-150">The following procedures are examples of using Lync Server Management Shell to modify the settings described in this section.</span></span>

<div>

## <a name="to-modify-conferencing-policy-for-video-settings"></a><span data-ttu-id="79576-151">So ändern Sie die konferenzrichtlinie für Videoeinstellungen</span><span class="sxs-lookup"><span data-stu-id="79576-151">To modify conferencing policy for video settings</span></span>

1.  <span data-ttu-id="79576-152">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="79576-152">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="79576-153">Führen Sie in der Befehlszeile das folgende Cmdlet aus, um die konferenzrichtlinie zu bearbeiten:</span><span class="sxs-lookup"><span data-stu-id="79576-153">At the command line, run the following cmdlet to edit conferencing policy:</span></span>
    
        Set-CsConferencingPolicy -Identity Pool01ConferencingPolicy -VideoBitRateKb 2000 -TotalReceiveVideoBitRateKb 2000 

</div>

<div>

## <a name="to-modify-media-configuration-for-legacy-clients"></a><span data-ttu-id="79576-154">So ändern Sie die Medienkonfiguration für Legacy-Clients</span><span class="sxs-lookup"><span data-stu-id="79576-154">To modify media configuration for legacy clients</span></span>

1.  <span data-ttu-id="79576-155">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="79576-155">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="79576-156">Führen Sie in der Befehlszeile das folgende Cmdlet aus, um die Medienkonfiguration zu bearbeiten:</span><span class="sxs-lookup"><span data-stu-id="79576-156">At the command line, run the following cmdlet to edit the media configuration:</span></span>
    
        Set-CsMediaConfiguration -Identity site:Redmond01 -MaxVideoRateAllowed CIF250K

<span data-ttu-id="79576-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="79576-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

