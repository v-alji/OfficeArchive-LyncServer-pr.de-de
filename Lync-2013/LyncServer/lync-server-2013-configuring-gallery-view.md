---
title: 'Lync Server 2013: Konfigurieren der Katalogansicht'
description: 'Lync Server 2013: Konfigurieren der Katalogansicht'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring Gallery View
ms:assetid: 4a609178-47d8-4682-ac8d-29f882801924
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204871(v=OCS.15)
ms:contentKeyID: 48184069
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2aec2f1e3c7bff9a3736f40584a29880978b9daa
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433094"
---
# <a name="configuring-gallery-view-in-lync-server-2013"></a><span data-ttu-id="4f369-103">Konfigurieren der Katalogansicht in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="4f369-103">Configuring Gallery View in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="4f369-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="4f369-104">

<span> </span></span></span>

<span data-ttu-id="4f369-105">_**Letztes Änderungsdatum des Themas:** 2012-10-30_</span><span class="sxs-lookup"><span data-stu-id="4f369-105">_**Topic Last Modified:** 2012-10-30_</span></span>

<span data-ttu-id="4f369-106">In lync Server 2013 konfigurieren Sie Videokonferenzen in der Katalogansicht in Konferenzrichtlinien.</span><span class="sxs-lookup"><span data-stu-id="4f369-106">In Lync Server 2013, you configure Gallery View video conferencing in conferencing policy.</span></span> <span data-ttu-id="4f369-107">Die Katalogansicht ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="4f369-107">Gallery View is turned on by default.</span></span> <span data-ttu-id="4f369-108">Wenn Sie die Katalogansicht nicht zulassen oder nur für einige Benutzer zulassen möchten, müssen Sie das Feature in Konferenzrichtlinien deaktivieren.</span><span class="sxs-lookup"><span data-stu-id="4f369-108">If you do not want to allow Gallery View, or want to allow it for only some users, you need to turn off the feature in conferencing policy.</span></span>

<span data-ttu-id="4f369-109">Wenn das Video eines Konferenzteilnehmers nicht zur Verfügung steht, kann die Benutzeroberfläche für die Galerieansicht verbessert werden, wenn Sie Fotos mit hoher Auflösung, ein neues Feature in lync Server 2013, bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="4f369-109">When a conference participant's video is not available, the users' Gallery View experience can be enhanced if you deploy high-resolution photos, a new feature in Lync Server 2013.</span></span> <span data-ttu-id="4f369-110">Fotos mit hoher Auflösung bieten eine Alternative zu den kleineren, in den Active Directory-Domänendiensten gespeicherten Kontaktfotos mit begrenzter Auflösung.</span><span class="sxs-lookup"><span data-stu-id="4f369-110">High-resolution photos provide an alternative to the smaller, limited resolution contact photos stored in Active Directory Domain Services.</span></span> <span data-ttu-id="4f369-111">Fotos mit hoher Auflösung werden im Exchange 2013-Postfach eines Benutzers gespeichert, und daher müssen Sie lync Server 2013 in Exchange 2013 integrieren.</span><span class="sxs-lookup"><span data-stu-id="4f369-111">High-resolution photos are stored in a user's Exchange 2013 mailbox, and, therefore, require you to integrate Lync Server 2013 with Exchange 2013.</span></span> <span data-ttu-id="4f369-112">Ausführliche Informationen finden Sie im NextHop-Blog Artikel "Integration von Exchange 2013 und lync Server 2013" unter [https://go.microsoft.com/fwlink/p/?LinkId=260987](https://go.microsoft.com/fwlink/p/?linkid=260987) .</span><span class="sxs-lookup"><span data-stu-id="4f369-112">For details, see the NextHop blog article, "Integrating Exchange 2013 and Lync Server 2013," at [https://go.microsoft.com/fwlink/p/?LinkId=260987](https://go.microsoft.com/fwlink/p/?linkid=260987).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="4f369-113">Die Inhalte der Blogs und die zugehörige URL können ohne vorherige Ankündigung geändert werden.</span><span class="sxs-lookup"><span data-stu-id="4f369-113">The content of each blog and its URL are subject to change without notice.</span></span>



</div>

<span data-ttu-id="4f369-114">Sie können die Parameter für die Katalogansicht mithilfe der lync Server 2013-Systemsteuerung oder mithilfe eines der folgenden Cmdlets anzeigen oder ändern:</span><span class="sxs-lookup"><span data-stu-id="4f369-114">You can view or modify the Gallery View parameters by using Lync Server 2013 Control Panel or by using one of the following cmdlets:</span></span>

  - <span data-ttu-id="4f369-115">**Get-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="4f369-115">**Get-CsConferencingPolicy**</span></span>

  - <span data-ttu-id="4f369-116">**Set-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="4f369-116">**Set-CsConferencingPolicy**</span></span>

  - <span data-ttu-id="4f369-117">**New-CsConferencingPolicy**</span><span class="sxs-lookup"><span data-stu-id="4f369-117">**New-CsConferencingPolicy**</span></span>

<span data-ttu-id="4f369-118">Konfigurieren Sie die Katalogansicht mit den folgenden konferenzrichtlinieneinstellungen:</span><span class="sxs-lookup"><span data-stu-id="4f369-118">Configure Gallery View with the following conferencing policy settings:</span></span>

  - <span data-ttu-id="4f369-119">**AllowMultiview**   Dieser Parameter steuert, ob ein Benutzer die Möglichkeit hat, Katalogansicht-Videokonferenzen zu organisieren.</span><span class="sxs-lookup"><span data-stu-id="4f369-119">**AllowMultiview**   This parameter controls whether a user is allowed to organize Gallery View video conferences.</span></span> <span data-ttu-id="4f369-120">Dieser Parameter gilt für geplante und Ad-hoc-Besprechungen, die vom Benutzer erstellt wurden.</span><span class="sxs-lookup"><span data-stu-id="4f369-120">This parameter applies to scheduled and ad-hoc meetings created by the user.</span></span>
    
    <span data-ttu-id="4f369-121">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f369-121">Examples:</span></span>
    
      - <span data-ttu-id="4f369-122">Dieser Parameter ist für Benutzer A auf true festgelegt, der in einem lync Server 2013-Pool verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="4f369-122">This parameter is set to True for User A, who is homed on a Lync Server 2013 pool.</span></span> <span data-ttu-id="4f369-123">Besprechungen, die von einem Benutzer organisiert werden, ermöglichen es Benutzern, mehreren Videostreams beizutreten und zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="4f369-123">Meetings organized by User A enable users to join and receive multiple video streams.</span></span>
    
      - <span data-ttu-id="4f369-124">Dieser Parameter wird für Benutzer B auf "false" festgelegt, der sich in einem lync Server 2013-Pool befindet.</span><span class="sxs-lookup"><span data-stu-id="4f369-124">This parameter is set to False for User B, who is homed on a Lync Server 2013 pool.</span></span> <span data-ttu-id="4f369-125">Besprechungen, die von Benutzer B organisiert werden, sind mit einem einzelnen Videostream vergleichbar mit der Videokonferenz, die von lync Server 2010 bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4f369-125">Meetings organized by User B have a single video stream that is similar to the video conference experience provided by Lync Server 2010.</span></span>
    
    <span data-ttu-id="4f369-126">Dieser Parameter bestimmt, wer Besprechungen organisieren kann, die mehrere Videostreams zulassen.</span><span class="sxs-lookup"><span data-stu-id="4f369-126">This parameter determines who can organize meetings that allow multiple video streams.</span></span> <span data-ttu-id="4f369-127">Teilnehmern an Besprechungen, die mehrere Videostreams zulassen, ist es möglich, auf der Grundlage ihrer individuellen Berechtigungen mehrere Videostreams zu empfangen (siehe Beschreibung des EnableMultiviewJoin-Parameters).</span><span class="sxs-lookup"><span data-stu-id="4f369-127">Participants in meetings that allow multiple video streams may or may not be allowed to receive multiple video streams, based on their individual permissions (see the description for the EnableMultiviewJoin parameter).</span></span>

  - <span data-ttu-id="4f369-128">**EnableMultiviewJoin**   Dieser Parameter steuert, ob ein Teilnehmer an einer Besprechung in Besprechungen, die ihn zulassen, die videoerfahrung in der Galerieansicht erhält.</span><span class="sxs-lookup"><span data-stu-id="4f369-128">**EnableMultiviewJoin**   This parameter controls whether a participant in a meeting receives the Gallery View video experience in meetings that allow it.</span></span> <span data-ttu-id="4f369-129">Dieser Parameter steuert die Benutzererfahrung in jeder Besprechung, an der Sie teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="4f369-129">This parameter controls the user's experience in any meeting in which he or she participates.</span></span>
    
    <span data-ttu-id="4f369-130">Beispiele</span><span class="sxs-lookup"><span data-stu-id="4f369-130">Examples:</span></span>
    
      - <span data-ttu-id="4f369-131">Dieser Parameter wird für Benutzer c auf "true" festgelegt, um mehrere Videodatenströme empfangen zu können, wenn Sie an einer Besprechung teilnehmen, die von Benutzer a organisiert oder gestartet wurde. Benutzer c erhält einen einzelnen Videostream, der der Videokonferenz ähnelt, die von lync Server 2010 bei der Teilnahme an einer von Benutzer B organisierten oder gestarteten Besprechung bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4f369-131">This parameter is set to True for User C. User C can receive multiple video streams when participating in a meeting organized or started by User A. User C receives a single video stream that is similar to the video conference experience provided by Lync Server 2010 when participating in a meeting organized or started by User B.</span></span>
    
      - <span data-ttu-id="4f369-132">Dieser Parameter wird für Benutzer d auf "false" festgelegt und erhält einen einzelnen Videostream, der der Videokonferenz ähnelt, die von lync Server 2010 bei der Teilnahme an einer Besprechung, die von Benutzer a oder Benutzer B organisiert wurde, bereitgestellt wird.</span><span class="sxs-lookup"><span data-stu-id="4f369-132">This parameter is set to False for User D. User D receives single video stream that is similar to the video conference experience provided by Lync Server 2010 when participating in any meeting organized by User A or User B.</span></span>

<span data-ttu-id="4f369-133">Das folgende Verfahren ist ein Beispiel für die Verwendung der lync Server-Verwaltungsshell zum Aktivieren von Videokonferenzen in der Katalogansicht.</span><span class="sxs-lookup"><span data-stu-id="4f369-133">The following procedure is an example of using Lync Server Management Shell to enable Gallery View video conferencing.</span></span>

<div>

## <a name="to-modify-conferencing-policy-for-gallery-view-video-conferencing"></a><span data-ttu-id="4f369-134">So ändern Sie die konferenzrichtlinie für Videokonferenzen in der Katalogansicht</span><span class="sxs-lookup"><span data-stu-id="4f369-134">To modify conferencing policy for Gallery View video conferencing</span></span>

1.  <span data-ttu-id="4f369-135">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="4f369-135">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

2.  <span data-ttu-id="4f369-136">Führen Sie in der Befehlszeile das folgende Cmdlet aus, um die konferenzrichtlinie zu bearbeiten:</span><span class="sxs-lookup"><span data-stu-id="4f369-136">At the command line, run the following cmdlet to edit conferencing policy:</span></span>
    
        Set-CsConferencingPolicy -Identity Pool01ConferencingPolicy -AllowMultiview $true -EnableMultiviewJoin $true 

<span data-ttu-id="4f369-137"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="4f369-137"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

