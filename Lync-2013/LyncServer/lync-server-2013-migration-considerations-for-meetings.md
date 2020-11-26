---
title: 'Lync Server 2013: Migrationsüberlegungen für Besprechungen'
description: 'Lync Server 2013: Migrationsüberlegungen für Besprechungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Migration considerations for meetings
ms:assetid: a9807d58-99a3-4cff-b4c6-74950d106a2b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412800(v=OCS.15)
ms:contentKeyID: 61097556
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: e238405acf7bc2a96fd2efd4cca761c1f1f258fd
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49425584"
---
# <a name="migration-considerations-for-meetings-in-lync-server-2013"></a><span data-ttu-id="7352f-103">Migrationsüberlegungen für Besprechungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7352f-103">Migration considerations for meetings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="7352f-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="7352f-104">

<span> </span></span></span>

<span data-ttu-id="7352f-105">_**Letztes Änderungsdatum des Themas:** 2014-02-10_</span><span class="sxs-lookup"><span data-stu-id="7352f-105">_**Topic Last Modified:** 2014-02-10_</span></span>

<span data-ttu-id="7352f-106">In diesem Abschnitt werden die folgenden Themen behandelt:</span><span class="sxs-lookup"><span data-stu-id="7352f-106">The following topics are discussed in this section:</span></span>

  - <span data-ttu-id="7352f-107">Änderungen an Besprechungen in Microsoft lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7352f-107">Changes to meetings in Microsoft Lync Server 2013</span></span>

  - <span data-ttu-id="7352f-108">Migrieren von Benutzern basierend auf Ihren Konferenz Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7352f-108">Migrating users based on their conferencing needs</span></span>

  - <span data-ttu-id="7352f-109">Migrieren vorhandener Besprechungen und Besprechungsinhalte</span><span class="sxs-lookup"><span data-stu-id="7352f-109">Migrating existing meetings and meeting content</span></span>

  - <span data-ttu-id="7352f-110">Benutzerfreundlichkeit während der Migration von lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="7352f-110">User experience during Lync Server 2010 migration</span></span>

  - <span data-ttu-id="7352f-111">Benutzerfreundlichkeit während der Migration von Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="7352f-111">User Experience during Office Communications Server 2007 R2 migration</span></span>

  - <span data-ttu-id="7352f-112">Microsoft lync 2013-Kompatibilität mit Besprechungen mit früheren Server Versionen</span><span class="sxs-lookup"><span data-stu-id="7352f-112">Microsoft Lync 2013 compatibility with meetings on earlier server versions</span></span>

<div>

## <a name="changes-to-meetings-in-lync-server-2013"></a><span data-ttu-id="7352f-113">Änderungen an Besprechungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="7352f-113">Changes to Meetings in Lync Server 2013</span></span>

<span data-ttu-id="7352f-114">**Lync Server 2013-Features.**</span><span class="sxs-lookup"><span data-stu-id="7352f-114">**Lync Server 2013 features.**</span></span>   <span data-ttu-id="7352f-115">Lync Server 2013 bietet neue Konferenzfeatures, die Benutzern zur Verfügung stehen, nachdem Ihre Konten nach lync Server 2013 verschoben wurden und sich mit dem lync 2013-Client anmelden.</span><span class="sxs-lookup"><span data-stu-id="7352f-115">Lync Server 2013 provides new conferencing features that become available to users after their accounts are moved to Lync Server 2013 and they sign in with the Lync 2013 client.</span></span> <span data-ttu-id="7352f-116">Neue Features werden in den [neuen Konferenzfeatures in lync Server 2013](lync-server-2013-new-conferencing-features.md) und Neuerungen [für Clients in lync Server 2013](lync-server-2013-what-s-new-for-clients.md)erläutert.</span><span class="sxs-lookup"><span data-stu-id="7352f-116">New features are outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

<span data-ttu-id="7352f-117">**Besprechungs-URL.**</span><span class="sxs-lookup"><span data-stu-id="7352f-117">**Meeting URL.**</span></span>   <span data-ttu-id="7352f-118">Wie in lync Server 2010 verfügen alle neu geplanten Besprechungen in lync Server 2013 über ein URL-Präfix für https://, und vorhandene Besprechungen werden zusammen mit Benutzerkonten migriert.</span><span class="sxs-lookup"><span data-stu-id="7352f-118">As in Lync Server 2010, all newly scheduled meetings in Lync Server 2013 have a URL prefix of https:// and existing meetings migrate along with user accounts.</span></span> <span data-ttu-id="7352f-119">Lync Server 2013 unterstützt jedoch nicht den Office Communications Server 2007 R2-Konferenzanruf (conf://url prefix) oder die Webkonferenz (Meet://-URL-Präfix).</span><span class="sxs-lookup"><span data-stu-id="7352f-119">However, Lync Server 2013 does not support the Office Communications Server 2007 R2 conference call (conf:// URL prefix) or web conference (meet:// URL prefix).</span></span> <span data-ttu-id="7352f-120">Weitere Informationen finden Sie unter "Migrieren von Besprechungen von Office Communications Server 2007 R2" weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="7352f-120">See “Migrating Meetings from Office Communications Server 2007 R2” later in this topic for more information.</span></span>

<span data-ttu-id="7352f-121">**Kundendienst.**</span><span class="sxs-lookup"><span data-stu-id="7352f-121">**Client support.**</span></span>   <span data-ttu-id="7352f-122">Im Gegensatz zu lync Server 2010 unterstützt lync Server 2013 keine Office Communicator-Clients für Konferenzen.</span><span class="sxs-lookup"><span data-stu-id="7352f-122">Unlike Lync Server 2010, Lync Server 2013 does not support Office Communicator clients for conferencing.</span></span> <span data-ttu-id="7352f-123">Sie können die folgenden Clients nicht zum teilnehmen an Besprechungen verwenden, die über das Online Besprechungs-Add-in für lync 2013 geplant sind:</span><span class="sxs-lookup"><span data-stu-id="7352f-123">You cannot use the following clients to join meetings scheduled through the Online Meeting Add-in for Lync 2013:</span></span>

  - <span data-ttu-id="7352f-124">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="7352f-124">Office Communicator 2007 R2</span></span>

  - <span data-ttu-id="7352f-125">Microsoft Office Communications Server 2007 R2-Vermittlung</span><span class="sxs-lookup"><span data-stu-id="7352f-125">Microsoft Office Communications Server 2007 R2 Attendant</span></span>

  - <span data-ttu-id="7352f-126">Office Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="7352f-126">Office Communicator 2007</span></span>

  - <span data-ttu-id="7352f-127">Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="7352f-127">Office Live Meeting 2007</span></span>

<span data-ttu-id="7352f-128">Während der Migration sollten Office Communicator 2007 R2-Benutzer lync Web App 2013 verwenden, um an lync Server 2013-Besprechungen teilzunehmen, bis Ihre Clients aktualisiert wurden.</span><span class="sxs-lookup"><span data-stu-id="7352f-128">During migration, Office Communicator 2007 R2 users should use Lync Web App 2013 to join Lync Server 2013 meetings until their clients are upgraded.</span></span> <span data-ttu-id="7352f-129">Beachten Sie, dass Benutzer von Office Communicator 2007 R2 weiterhin ihren vorhandenen Client gegen lync Server 2013 für Anwesenheits-und Chat Features verwenden können, Konferenzfeatures aber nicht unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="7352f-129">Note that Office Communicator 2007 R2 users can continue to use their existing client against Lync Server 2013 for presence and IM features, but conferencing features are not supported.</span></span>

<div>


</div>

</div>

<div>

## <a name="migrating-users-based-on-their-conferencing-needs"></a><span data-ttu-id="7352f-130">Migrieren von Benutzern basierend auf Ihren Konferenz Anforderungen</span><span class="sxs-lookup"><span data-stu-id="7352f-130">Migrating Users Based on Their Conferencing Needs</span></span>

<span data-ttu-id="7352f-131">**Häufige Besprechungsorganisatoren**</span><span class="sxs-lookup"><span data-stu-id="7352f-131">**Frequent meeting organizers.**</span></span>   <span data-ttu-id="7352f-132">Ziehen Sie es vor, häufige Besprechungsorganisatoren frühzeitig zu migrieren, damit Sie die neuen lync Server 2013-und lync 2013-Features nutzen können, die in den [neuen Konferenzfeatures in lync Server 2013](lync-server-2013-new-conferencing-features.md) und Neuerungen [für Clients in lync Server 2013](lync-server-2013-what-s-new-for-clients.md)beschrieben sind.</span><span class="sxs-lookup"><span data-stu-id="7352f-132">Consider migrating frequent meeting organizers early in the process so that they can take advantage of the new Lync Server 2013 and Lync 2013 features outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

<span data-ttu-id="7352f-133">**Live Meeting-Benutzer.**</span><span class="sxs-lookup"><span data-stu-id="7352f-133">**Live Meeting users.**</span></span>   <span data-ttu-id="7352f-134">Wenn Sie von Office Communications Server 2007 R2 migrieren, und Sie über Benutzer verfügen, die für Live Meeting spezifische Webkonferenz Features benötigen – insbesondere Unterstützung für große Besprechungen und Break-out-Räume – haben Sie die folgenden Optionen:</span><span class="sxs-lookup"><span data-stu-id="7352f-134">If you are migrating from Office Communications Server 2007 R2 and you have users who need web conferencing features specific to Live Meeting—particularly support for large meetings and break-out rooms—you have the following options:</span></span>

  - <span data-ttu-id="7352f-135">Empfehlen Sie die Organisatoren, den Live Meeting-Dienst zu verwenden, sofern Sie in Ihrer Organisation verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="7352f-135">Advise organizers to use the Live Meeting service, if available in your organization.</span></span>

  - <span data-ttu-id="7352f-136">Lassen Sie die Organisatoren in der früheren Version von Office Communications Server verwaltet, damit Sie weiterhin Server basierte Live Meeting-Webkonferenzen planen können.</span><span class="sxs-lookup"><span data-stu-id="7352f-136">Leave the organizers homed on the earlier version of Office Communications Server, so they can continue to schedule server-based Live Meeting web conferences.</span></span>

</div>

<div>

## <a name="migrating-existing-meetings-and-meeting-content"></a><span data-ttu-id="7352f-137">Migrieren vorhandener Besprechungen und Besprechungsinhalte</span><span class="sxs-lookup"><span data-stu-id="7352f-137">Migrating Existing Meetings and Meeting Content</span></span>

<div>

## <a name="migrating-meetings-from-lync-server-2010"></a><span data-ttu-id="7352f-138">Migrieren von Besprechungen von lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="7352f-138">Migrating Meetings from Lync Server 2010</span></span>

<span data-ttu-id="7352f-139">Wenn Sie einen Benutzer von lync Server 2010 auf lync Server 2013 verschieben, werden die folgenden Informationen mit dem Konto des Benutzers verschoben:</span><span class="sxs-lookup"><span data-stu-id="7352f-139">When you move a user from Lync Server 2010 to Lync Server 2013, the following information moves with the user’s account:</span></span>

  - <span data-ttu-id="7352f-140">Besprechungen, die der Benutzer bereits geplant hat.</span><span class="sxs-lookup"><span data-stu-id="7352f-140">Meetings already scheduled by the user.</span></span> <span data-ttu-id="7352f-141">Dazu gehören Konferenzverzeichnisse und Konferenzdaten.</span><span class="sxs-lookup"><span data-stu-id="7352f-141">This includes conferencing directories and conferencing data.</span></span>

  - <span data-ttu-id="7352f-142">Die persönliche Identifikationsnummer (PIN) des Benutzers.</span><span class="sxs-lookup"><span data-stu-id="7352f-142">The user’s personal identification number (PIN).</span></span> <span data-ttu-id="7352f-143">Die aktuelle PIN des Benutzers funktioniert weiterhin, bis er abläuft oder der Benutzer eine neue PIN anfordert.</span><span class="sxs-lookup"><span data-stu-id="7352f-143">The user’s current PIN continues to work until it expires or the user requests a new PIN.</span></span>

<span data-ttu-id="7352f-144">Die folgenden Benutzerkontoinformationen werden jedoch nicht auf den neuen Server verschoben:</span><span class="sxs-lookup"><span data-stu-id="7352f-144">However, the following user account information does not move to the new server:</span></span>

  - <span data-ttu-id="7352f-145">Besprechungsinhalte, beispielsweise PowerPoint-Präsentationen, Whiteboard-Inhalte und Umfragedaten</span><span class="sxs-lookup"><span data-stu-id="7352f-145">Meeting content, for example PowerPoint presentations, whiteboard content, and poll data</span></span>

<span data-ttu-id="7352f-146">Verwenden Sie den MoveMeetingContent-Parameter des Move-CsUser-Cmdlets, um den Inhalt zu verschieben, der in Besprechungen freigegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="7352f-146">To move the content that has been shared in meetings, use the MoveMeetingContent parameter of the Move-CsUser cmdlet.</span></span> <span data-ttu-id="7352f-147">Detaillierte Informationen zur Verwendung dieses Cmdlets finden Sie unter [Move-CsUser](https://docs.microsoft.com/powershell/module/skype/Move-CsUser) in der Dokumentation zu lync Server 2013-Cmdlets.</span><span class="sxs-lookup"><span data-stu-id="7352f-147">For details about using this cmdlet, see [Move-CsUser](https://docs.microsoft.com/powershell/module/skype/Move-CsUser) in the Lync Server 2013 cmdlets documentation.</span></span>

</div>

<div>

## <a name="migrating-meetings-from-office-communications-server-2007-r2"></a><span data-ttu-id="7352f-148">Migrieren von Besprechungen von Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="7352f-148">Migrating Meetings from Office Communications Server 2007 R2</span></span>

<span data-ttu-id="7352f-149">Office Communications Server 2007 R2-Besprechungen sind entweder Konferenzgespräche (conf://url prefix) oder Webkonferenzen (Meet://url prefix).</span><span class="sxs-lookup"><span data-stu-id="7352f-149">Office Communications Server 2007 R2 meetings are either conference calls (conf:// URL prefix) or web conferences (meet:// URL prefix).</span></span> <span data-ttu-id="7352f-150">Lync Server 2013 unterstützt diese früheren conf://-und Meet://-Konferenzen nicht, und Sie werden nicht zusammen mit dem Benutzerkonto migriert.</span><span class="sxs-lookup"><span data-stu-id="7352f-150">Lync Server 2013 does not support these earlier conf:// and meet:// conferences, and they are not migrated along with the user account.</span></span> <span data-ttu-id="7352f-151">Nach der Migration sollten Sie die Benutzer anweisen, die Links für alle geplanten Onlinebesprechungen zu aktualisieren.</span><span class="sxs-lookup"><span data-stu-id="7352f-151">After migration, you should instruct users to update the links for any online meetings they have scheduled.</span></span> <span data-ttu-id="7352f-152">Sie können dies nach der Installation des lync 2013-Clients tun, indem Sie eine geplante Besprechungseinladung öffnen, die die Besprechungs-URL aktualisiert, und die Einladung an die Teilnehmer erneut senden.</span><span class="sxs-lookup"><span data-stu-id="7352f-152">They can do this after installing the Lync 2013 client by opening a scheduled meeting invitation—which updates the meeting URL—and resending the invitation to participants.</span></span>

</div>

</div>

<div>

## <a name="user-experience-during-lync-server-2010-migration"></a><span data-ttu-id="7352f-153">Benutzerfreundlichkeit während der Migration von lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="7352f-153">User Experience during Lync Server 2010 Migration</span></span>

<span data-ttu-id="7352f-154">Dieser Abschnitt enthält eine Zusammenfassung der Benutzer Konferenzfunktionen bei der Migration von lync 2010.</span><span class="sxs-lookup"><span data-stu-id="7352f-154">This section provides a summary of users’ conferencing experience when migrating from Lync 2010.</span></span> <span data-ttu-id="7352f-155">Weitere Informationen dazu, wie lync Server 2013-Clients koexistieren und mit früheren Client-und Server Versionen interagieren können, finden Sie unter [Client Interoperabilität in lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span><span class="sxs-lookup"><span data-stu-id="7352f-155">For more details about how Lync Server 2013 clients can coexist and interact with previous client and server versions, see [Client interoperability in Lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span></span>

<div>

## <a name="joining-lync-server-2010-meetings-with-a-lync-2013-client"></a><span data-ttu-id="7352f-156">Beitreten zu lync Server 2010-Besprechungen mit einem lync 2013-Client</span><span class="sxs-lookup"><span data-stu-id="7352f-156">Joining Lync Server 2010 Meetings with a Lync 2013 Client</span></span>

<span data-ttu-id="7352f-157">Während der Migration von lync Server 2010 kann es einen Zeitraum der Koexistenz geben, wenn Benutzer mit einem lync 2013-Client an lync Server 2010-Besprechungen teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="7352f-157">During migration from Lync Server 2010, there may be a period of coexistence when users join Lync Server 2010 meetings with a Lync 2013 client.</span></span> <span data-ttu-id="7352f-158">Diese Benutzer können mit den folgenden Ausnahmen auf lync 2013-Clientfeatures zugreifen:</span><span class="sxs-lookup"><span data-stu-id="7352f-158">These users have access to Lync 2013 client features with the following exceptions:</span></span>

  - <span data-ttu-id="7352f-159">In den Verwaltungsoptionen für **Teilnehmer** , auf die durch zeigen auf das Symbol "Personen" im Besprechungsfenster zugegriffen werden kann, funktioniert die Option **keine Besprechung im Chat** .</span><span class="sxs-lookup"><span data-stu-id="7352f-159">In the **Participants** management options, which are accessible by pointing to the people icon in the meeting window, the **No Meeting IM** option does not function.</span></span>

  - <span data-ttu-id="7352f-160">Die Katalogansicht funktioniert in Videokonferenzen nicht.</span><span class="sxs-lookup"><span data-stu-id="7352f-160">Gallery View does not function in video conferences.</span></span> <span data-ttu-id="7352f-161">Der Benutzer sieht nur den aktiven Lautsprecher und nicht alle Lautsprecher.</span><span class="sxs-lookup"><span data-stu-id="7352f-161">The user sees only the active speaker instead of all speakers.</span></span> <span data-ttu-id="7352f-162">In der Liste der Optionen zum **Wählen eines Layouts** steht die **Katalogansicht** nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="7352f-162">In the list of **Pick a Layout** options, **Gallery View** is unavailable</span></span>

  - <span data-ttu-id="7352f-163">Die Teilnehmerliste wird standardmäßig in Videokonferenzen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="7352f-163">The participant list displays by default in video conferences.</span></span>

  - <span data-ttu-id="7352f-164">Wenn Sie mit der rechten Maustaste auf einen Benutzer in der Teilnehmerliste klicken, sind die Optionen für das **Video Spotlight** und die **PIN-zu-Katalog** -Teilnehmer-Verwaltung Sperren nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="7352f-164">When right-clicking a user in the participants list, the **Lock the Video Spotlight** and **Pin to Gallery** participant management options are unavailable.</span></span>

</div>

</div>

<div>

## <a name="user-experience-during-office-communications-server-2007-r2-migration"></a><span data-ttu-id="7352f-165">Benutzerfreundlichkeit während der Migration von Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="7352f-165">User Experience during Office Communications Server 2007 R2 Migration</span></span>

<span data-ttu-id="7352f-166">Dieser Abschnitt enthält eine Zusammenfassung der Benutzer Konferenz Erfahrung bei der Migration von Office Communications Server 2007 R2, sowohl vor als auch nach der Installation von lync 2013.</span><span class="sxs-lookup"><span data-stu-id="7352f-166">This section provides a summary of users’ conferencing experience when migrating from Office Communications Server 2007 R2, both before and after Lync 2013 is installed.</span></span> <span data-ttu-id="7352f-167">Weitere Informationen dazu, wie lync Server 2013-Clients koexistieren und mit früheren Client-und Server Versionen interagieren können, finden Sie unter [Client Interoperabilität in lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span><span class="sxs-lookup"><span data-stu-id="7352f-167">For more details about how Lync Server 2013 clients can coexist and interact with previous client and server versions, see [Client interoperability in Lync 2013](lync-server-2013-client-interoperability-in-lync-2013.md).</span></span>

<div>

## <a name="after-user-account-is-migrated-before-lync-2013-is-installed"></a><span data-ttu-id="7352f-168">Nach dem Migrieren des Benutzerkontos vor der Installation von lync 2013</span><span class="sxs-lookup"><span data-stu-id="7352f-168">After User Account is Migrated, Before Lync 2013 Is Installed</span></span>

<span data-ttu-id="7352f-169">Nachdem ein Benutzer zum lync Server 2013-Server migriert wurde, aber bevor neue Clients installiert werden, können Benutzer von Office Communicator 2007 R2 weiterhin ihren vorhandenen Client für Anwesenheits-und Chat Features mit lync Server 2013 verwenden, aber Konferenzfeatures werden nicht unterstützt.</span><span class="sxs-lookup"><span data-stu-id="7352f-169">After a user is migrated to the Lync Server 2013 server, but before new clients are installed, Office Communicator 2007 R2 users can continue to use their existing client against Lync Server 2013 for presence and IM features, but conferencing features are not supported.</span></span>

</div>

<div>

## <a name="after-user-account-is-migrated-after-lync-2013-is-installed"></a><span data-ttu-id="7352f-170">Nach dem Migrieren des Benutzerkontos nach der Installation von lync 2013</span><span class="sxs-lookup"><span data-stu-id="7352f-170">After User Account is Migrated, After Lync 2013 Is Installed</span></span>

<span data-ttu-id="7352f-171">Wenn ein migrierter Benutzer lync 2013 installiert, wird auch das Online Besprechungs-Add-in für lync 2013 installiert.</span><span class="sxs-lookup"><span data-stu-id="7352f-171">When a migrated user installs Lync 2013, the Online Meeting Add-in for Lync 2013 is installed too.</span></span> <span data-ttu-id="7352f-172">Dies hat die folgenden Auswirkungen:</span><span class="sxs-lookup"><span data-stu-id="7352f-172">This has the following effects:</span></span>

  - <span data-ttu-id="7352f-173">Alle nachfolgend geplanten Besprechungen verwenden das neue Besprechungs Format, das eine https://-Adresse anstelle der Legacy-Meet://-Live Besprechungs Adresse verwendet.</span><span class="sxs-lookup"><span data-stu-id="7352f-173">All subsequently scheduled meetings use the new meeting format, which uses an https:// address instead of the legacy meet:// Live Meeting address.</span></span>

  - <span data-ttu-id="7352f-174">Bei einer IT-verwalteten Bereitstellung von lync 2013 hat der Administrator die Möglichkeit, das Konferenz-Add-in für Microsoft Office Outlook zu deinstallieren, das zum Planen von Live Meeting-Servern und dienstbasierten Besprechungen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="7352f-174">In an IT-managed deployment of Lync 2013, the administrator has the option of uninstalling the Conferencing Add-in for Microsoft Office Outlook, which is used to schedule Live Meeting server and service-based meetings.</span></span> <span data-ttu-id="7352f-175">Möglicherweise verfügen Sie jedoch über Benutzer, die weiterhin Live Meeting-Service Besprechungen planen müssen.</span><span class="sxs-lookup"><span data-stu-id="7352f-175">However, you may have users who need to continue to schedule Live Meeting service meetings.</span></span> <span data-ttu-id="7352f-176">In diesem Fall können Sie zulassen, dass beide Add-ins koexistieren.</span><span class="sxs-lookup"><span data-stu-id="7352f-176">In this case, you can allow both add-ins to coexist.</span></span>

</div>

<div>

## <a name="meetings-with-federated-organizations-that-use-previous-clients"></a><span data-ttu-id="7352f-177">Besprechungen mit Verbundorganisationen, die frühere Clients verwenden</span><span class="sxs-lookup"><span data-stu-id="7352f-177">Meetings with Federated Organizations that Use Previous Clients</span></span>

<span data-ttu-id="7352f-178">Benutzer in Verbundorganisationen, die Microsoft Office Communicator 2007 verwenden, können in Ihrer Organisation nicht an lync Server 2013-Besprechungen teilnehmen, wenn diese Besprechungen vom Organisator gesperrt sind.</span><span class="sxs-lookup"><span data-stu-id="7352f-178">Users in federated organizations who are using Microsoft Office Communicator 2007 cannot join Lync Server 2013 meetings in your organization if those meetings are locked by the organizer.</span></span> <span data-ttu-id="7352f-179">Sie müssen diese Besprechungen in lync Server 2013 neu planen, sodass Sie, wenn Teilnehmer an der Besprechung teilnehmen, mithilfe der neuen https://-Besprechungs-URL, lync Web App verwenden können.</span><span class="sxs-lookup"><span data-stu-id="7352f-179">You have to reschedule these meetings in Lync Server 2013 so when federated participants join the meeting by using the new https:// meeting URL, they can use Lync Web App.</span></span>

<span data-ttu-id="7352f-180"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="7352f-180"></div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

