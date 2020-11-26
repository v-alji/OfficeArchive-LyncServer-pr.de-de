---
title: Übersicht über lync Server 2013 A/V-Konferenzen
description: Übersicht über lync Server 2013 A/V-Konferenzen.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: A/V conferencing overview
ms:assetid: 9583de87-4618-4a99-a47a-45e8cc4cc221
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ619186(v=OCS.15)
ms:contentKeyID: 49733747
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 76ef4f76a4df0187a7c36394b2c95e99876df9be
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49439550"
---
# <a name="overview-of-av-conferencing-in-lync-server-2013"></a><span data-ttu-id="a79a3-103">Übersicht über A/V-Konferenzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="a79a3-103">Overview of A/V conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="a79a3-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="a79a3-104">

<span> </span></span></span>

<span data-ttu-id="a79a3-105">_**Letztes Änderungsdatum des Themas:** 2012-10-13_</span><span class="sxs-lookup"><span data-stu-id="a79a3-105">_**Topic Last Modified:** 2012-10-13_</span></span>

<span data-ttu-id="a79a3-106">A/V-Konferenzen ermöglichen Audio-und Videokommunikation in Echtzeit zwischen Ihren Benutzern.</span><span class="sxs-lookup"><span data-stu-id="a79a3-106">A/V conferencing enables real-time audio and video communications between your users.</span></span> <span data-ttu-id="a79a3-107">Wenn Sie Konferenzen bereitstellen, können Sie auswählen, ob Sie Webkonferenzen und A/V-Konferenzen oder nur Webkonferenzen aktivieren und verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="a79a3-107">When you deploy conferencing, you can choose to enable and use both web conferencing and A/V conferencing, or just web conferencing.</span></span>

<span data-ttu-id="a79a3-108">Zum Planen von A/V-Konferenzen müssen Sie die erforderliche Netzwerkbandbreite für den Typ der Konferenzmedien kennen, die in Ihrer Organisation verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a79a3-108">To plan for A/V conferencing, you need to understand the network bandwidth required by the type of conferencing media that your organization requires.</span></span> <span data-ttu-id="a79a3-109">Dies könnten z. B. Audio, Video und Panoramavideo sein.</span><span class="sxs-lookup"><span data-stu-id="a79a3-109">This could include audio, video, and panoramic video.</span></span>

<span data-ttu-id="a79a3-110">Bevor Sie Benutzer für A/V-Konferenzen aktivieren, stellen Sie sicher, dass Ihr Netzwerk die resultierende Last verarbeiten kann.</span><span class="sxs-lookup"><span data-stu-id="a79a3-110">Before you enable users for A/V conferencing, ensure that your network can handle the resulting load.</span></span> <span data-ttu-id="a79a3-111">Eine zu geringe Netzwerkbandbreite kann zu einem stark beeinträchtigten Benutzererlebnis führen.</span><span class="sxs-lookup"><span data-stu-id="a79a3-111">Without sufficient network bandwidth, the user experience may be severely degraded.</span></span> <span data-ttu-id="a79a3-112">Sie können die Anrufsteuerung (Call Admission Control, CAC) verwenden, um die von A/V-Konferenzen verwendete Netzwerkbandbreite zu verwalten.</span><span class="sxs-lookup"><span data-stu-id="a79a3-112">You can use call admission control (CAC) to manage the network bandwidth used by A/V Conferencing.</span></span> <span data-ttu-id="a79a3-113">Dies ist für eingeschränkte Netzwerke wichtig, beispielsweise bei Verbindungen mit beschränkter Bandbreite zwischen Zentrale und Niederlassungen.</span><span class="sxs-lookup"><span data-stu-id="a79a3-113">This is important for restricted networks, such as limited bandwidth links between central and branch sites.</span></span> <span data-ttu-id="a79a3-114">Ausführliche Informationen finden Sie unter Übersicht über die [Anrufsteuerung in lync Server 2013](lync-server-2013-overview-of-call-admission-control.md).</span><span class="sxs-lookup"><span data-stu-id="a79a3-114">For details, see [Overview of call admission control in Lync Server 2013](lync-server-2013-overview-of-call-admission-control.md).</span></span> <span data-ttu-id="a79a3-115">Details zu den Anforderungen an die Medien Bandbreite finden Sie unter Anforderungen an die [Netzwerkbandbreite für Mediendatenverkehr in lync Server 2013](lync-server-2013-network-bandwidth-requirements-for-media-traffic.md).</span><span class="sxs-lookup"><span data-stu-id="a79a3-115">For details about media bandwidth requirements, see [Network bandwidth requirements for media traffic in Lync Server 2013](lync-server-2013-network-bandwidth-requirements-for-media-traffic.md).</span></span>

<span data-ttu-id="a79a3-116">Bei Bereitstellung der Audiokonferenzfunktion in Ihrem Netzwerk benötigen Ihre Benutzer Audiogeräte (z. B. Headsets), um an einer Audiokonferenz teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="a79a3-116">If you deploy audio conferencing in your network, your users will need audio devices such as headsets to participate in an audio conference.</span></span> <span data-ttu-id="a79a3-117">Wenn Sie Videokonferenzen bereitstellen, benötigen die Benutzer Videogeräte, wie Webcams.</span><span class="sxs-lookup"><span data-stu-id="a79a3-117">If you deploy video conferencing, you need to deploy video devices, such as webcams for users.</span></span> <span data-ttu-id="a79a3-118">Wir empfehlen die Verwendung von UC-Geräten (Unified Communications), die von Microsoft für alle Gerätetypen zertifiziert sind, um eine optimale Benutzererfahrung zu gewährleisten.</span><span class="sxs-lookup"><span data-stu-id="a79a3-118">We recommend that you use unified communications (UC) devices that are certified by Microsoft for all device types, to ensure an optimal user experience.</span></span> <span data-ttu-id="a79a3-119">Details zu UC-zertifizierten Geräten finden Sie unter "Telefone und Geräte für lync" unter [https://go.microsoft.com/fwlink/p/?LinkId=263861](https://go.microsoft.com/fwlink/p/?linkid=263861) .</span><span class="sxs-lookup"><span data-stu-id="a79a3-119">For details about UC-certified devices, see "Phones and Devices for Lync" at [https://go.microsoft.com/fwlink/p/?LinkId=263861](https://go.microsoft.com/fwlink/p/?linkid=263861).</span></span> <span data-ttu-id="a79a3-120">Für Audio-oder Videogeräte, die Gerätebereitstellung und die Benutzerschulung sind wichtige Schritte, die Sie beachten und planen können.</span><span class="sxs-lookup"><span data-stu-id="a79a3-120">For either audio or video devices, device deployment, and user training are important steps for you to consider and plan for.</span></span>

<span data-ttu-id="a79a3-121">In den folgenden Abschnitten werden die Features für Audio-und Videokonferenzen beschrieben, einschließlich Informationen zum Verwalten der Bandbreite und zum Auswählen der entsprechenden Clients.</span><span class="sxs-lookup"><span data-stu-id="a79a3-121">The following sections describe the features for audio and video conferencing, including information about managing bandwidth and selecting the appropriate clients.</span></span>

<div>

## <a name="audio-conferencing-features"></a><span data-ttu-id="a79a3-122">Audiokonferenz-Features</span><span class="sxs-lookup"><span data-stu-id="a79a3-122">Audio Conferencing Features</span></span>

<span data-ttu-id="a79a3-123">Lync Server 2013 bietet verschiedene Features, die Sie zum Konfigurieren der Audiokonferenz-Oberfläche für den Benutzer verwenden können, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="a79a3-123">Lync Server 2013 provides several features that you can use to configure the audio conferencing experience for the user, including the following:</span></span>

  - <span data-ttu-id="a79a3-124">**Publikums Stummschaltung**   Der Referent kann diese Einstellung verwenden, um alle Audio-Teilnehmer in der Konferenz stummzuschalten und die Konferenz in einen Zustand zu versetzen, in dem nicht Referenten die Stummschaltung selbst aufheben können.</span><span class="sxs-lookup"><span data-stu-id="a79a3-124">**Audience mute**   The presenter can use this setting to mute all the audio participants in the conference and put the conference in a state where non-presenters cannot unmute themselves.</span></span>

  - <span data-ttu-id="a79a3-125">**Conferencing Entry/Exit-Ankündigungen**   Wenn Sie Einwahlkonferenzen aktiviert haben, können Referenten diese Einstellung verwenden, um ein-und ausgehende Ankündigungen zu aktivieren oder zu deaktivieren, um Ablenkungen zu minimieren, während eine Konferenz läuft.</span><span class="sxs-lookup"><span data-stu-id="a79a3-125">**Conferencing Entry/Exit Announcements**   If you have enabled dial-in conferencing, presenters can use this setting to turn entry and exit announcements on or off to minimize distractions while a conference is in progress.</span></span>

  - <span data-ttu-id="a79a3-126">**Hinzufügen eines Benutzers durch anrufen**   Referenten und Teilnehmer, denen die Berechtigung erteilt wurde, können den Konferenzen PSTN-Nummern hinzufügen und die Konferenz an diese Nummern abwählen.</span><span class="sxs-lookup"><span data-stu-id="a79a3-126">**Adding a user by dialing out**   Presenters and attendees that have been given permission, can add PSTN numbers to the conferences and have the conference dial-out to those numbers.</span></span>

</div>

<div>

## <a name="video-conferencing-features"></a><span data-ttu-id="a79a3-127">Video Konferenz Features</span><span class="sxs-lookup"><span data-stu-id="a79a3-127">Video Conferencing Features</span></span>

<span data-ttu-id="a79a3-128">Lync Server 2013 bietet verschiedene Features, mit denen Sie die Videokonferenzfunktionalität für den Benutzer konfigurieren können, einschließlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="a79a3-128">Lync Server 2013 provides several features that you can use to configure the video conferencing experience for the user, including the following:</span></span>

  - <span data-ttu-id="a79a3-129">**Katalogansicht**   In Videokonferenzen, die mehr als zwei Personen aufweisen, sehen Benutzer automatisch alle Teilnehmer der Konferenz.</span><span class="sxs-lookup"><span data-stu-id="a79a3-129">**Gallery View**   In video conferences that have more than two people, users automatically see everyone in the conference.</span></span> <span data-ttu-id="a79a3-130">Wenn die Konferenz mehr als fünf Teilnehmer hat, werden in der ersten Zeile die Videos der aktivsten Teilnehmer angezeigt und für die übrigen Teilnehmer Fotos.</span><span class="sxs-lookup"><span data-stu-id="a79a3-130">If the conference has more than five participants, the video of the most active participants appear in the top row and only the photo appears for the other participants.</span></span> <span data-ttu-id="a79a3-131">Die Videoaushandlung ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="a79a3-131">Multiparty video is turned on by default.</span></span> <span data-ttu-id="a79a3-132">Details zum Konfigurieren oder Deaktivieren von mehrteiligen Videos finden Sie unter [Konfigurieren der Videobandbreite in lync Server 2013](lync-server-2013-configuring-video-bandwidth.md).</span><span class="sxs-lookup"><span data-stu-id="a79a3-132">For details about configuring or turning off multiparty video, see [Configuring video bandwidth in Lync Server 2013](lync-server-2013-configuring-video-bandwidth.md).</span></span>

  - <span data-ttu-id="a79a3-133">**Panorama Video**   Wenn ein RoundTable-Videokonferenz Gerät im Konferenzraum installiert ist, bietet dieses Feature eine vollständige 360-Grad-Ansicht des Konferenzraums.</span><span class="sxs-lookup"><span data-stu-id="a79a3-133">**Panoramic Video**   If a RoundTable video conferencing device is installed in the conferencing room, this feature provides a full 360 degree view of the conference room.</span></span> <span data-ttu-id="a79a3-134">Panoramavideo ist nur mit Round Table verfügbar.</span><span class="sxs-lookup"><span data-stu-id="a79a3-134">The panoramic video strip is only available with RoundTable devices.</span></span>

  - <span data-ttu-id="a79a3-135">**Nur Referenten Videomodus**   Referenten können die Besprechung so konfigurieren, dass nur das Video des Referenten angezeigt wird.</span><span class="sxs-lookup"><span data-stu-id="a79a3-135">**Presenter only video mode**   Presenters can configure the meeting so that only the video from the presenter is shown.</span></span> <span data-ttu-id="a79a3-136">Dies verhindert bei großen Besprechungen Ablenkungen, wenn mehrere Videostreams verfügbar und mit verschiedenen Quellen verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="a79a3-136">This prevents distractions in large meetings when multiple video streams are available and locking to different sources.</span></span> <span data-ttu-id="a79a3-137">Dieser Modus wird auch auf Videos angewendet, die mit Round Table-Geräte aufgenommen und bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a79a3-137">This mode also applies to video captured and provided by RoundTable devices.</span></span>

  - <span data-ttu-id="a79a3-138">**HD-Video**   Die Benutzer können Auflösungen bis zu HD 1080p in zwei-Parteien-anrufen und Mehrparteienkonferenzen erleben.</span><span class="sxs-lookup"><span data-stu-id="a79a3-138">**HD video**   Users can experience resolutions up to HD 1080P in two-party calls and multiparty conferences.</span></span>

  - <span data-ttu-id="a79a3-139">**Video-Spotlight**   Referenten können die Besprechung so konfigurieren, dass nur die Videos von einem ausgewählten Teilnehmer, der eine Videoquelle ist, von den anderen Teilnehmern der Konferenz angezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="a79a3-139">**Video Spotlight**   Presenters can configure the meeting so that only the video from a selected participant who is a video source is seen by the other participants in the conference.</span></span> <span data-ttu-id="a79a3-140">Dieser Modus wird auch auf Videos angewendet, die mit Round Table-Geräten aufgenommen und bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="a79a3-140">This mode also applies to video captured and provided by RoundTable devices for panoramic video.</span></span>

<span data-ttu-id="a79a3-141"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="a79a3-141"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

