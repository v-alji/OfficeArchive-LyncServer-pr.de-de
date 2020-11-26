---
title: 'Lync Server 2013: Clientinteroperabilität in Lync 2013'
description: 'Lync Server 2013: Client Interoperabilität in lync 2013.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Client interoperability in Lync 2013
ms:assetid: 0f126571-91a2-45d5-855c-1e4ddb45fc04
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ204672(v=OCS.15)
ms:contentKeyID: 48183417
ms.date: 03/04/2016
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8ea6e90d9479f03dd6d946787e70a2b3cc078699
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49434921"
---
# <a name="client-interoperability-in-lync-2013"></a><span data-ttu-id="ad2ad-103">Clientinteroperabilität in Lync 2013</span><span class="sxs-lookup"><span data-stu-id="ad2ad-103">Client interoperability in Lync 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ad2ad-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ad2ad-104">

<span> </span></span></span>

<span data-ttu-id="ad2ad-105">_**Letztes Änderungsdatum des Themas:** 2016-03-04_</span><span class="sxs-lookup"><span data-stu-id="ad2ad-105">_**Topic Last Modified:** 2016-03-04_</span></span>

<span data-ttu-id="ad2ad-106">In diesem Thema wird erläutert, wie Microsoft lync Server 2013-Clients mit Clients aus früheren Versionen von lync Server und Office Communications Server koexistieren und mit ihnen interagieren können.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-106">This topic discusses the ability of Microsoft Lync Server 2013 clients to coexist and interact with clients from earlier versions of Lync Server and Office Communications Server.</span></span>

<div>

## <a name="server-and-client-compatibility"></a><span data-ttu-id="ad2ad-107">Server-und Client Kompatibilität</span><span class="sxs-lookup"><span data-stu-id="ad2ad-107">Server and Client Compatibility</span></span>

<span data-ttu-id="ad2ad-108">In der folgenden Tabelle sind die unterstützten Kombinationen von Clientversionen und Server Versionen aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-108">The following table shows the supported combinations of client versions and server versions.</span></span> <span data-ttu-id="ad2ad-109">Diese Tabelle gibt an, ob die Anmeldung unterstützt wird, wenn der Client versucht, eine Verbindung mit dem angegebenen Server herzustellen.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-109">This table indicates whether sign-in is supported when the client attempts to connect to the server indicated.</span></span> <span data-ttu-id="ad2ad-110">Lync Server 2013 unterstützt die vorherige Client Version.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-110">Lync Server 2013 supports the previous client version.</span></span> <span data-ttu-id="ad2ad-111">Im Gegensatz zu früheren Versionen unterstützt lync Server 2010 die neuen lync 2013-Clients.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-111">Also, unlike previous releases, Lync Server 2010 supports the new Lync 2013 clients.</span></span> <span data-ttu-id="ad2ad-112">Dadurch können Organisationen, die von lync Server 2010 upgraden, neue Clients unabhängig von lync Server-Upgrades bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-112">This allows organizations who are upgrading from Lync Server 2010 to roll out new clients independent of Lync Server upgrades.</span></span>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ad2ad-113">Client</span><span class="sxs-lookup"><span data-stu-id="ad2ad-113">Client</span></span></th>
<th><span data-ttu-id="ad2ad-114">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ad2ad-114">Lync Server 2013</span></span></th>
<th><span data-ttu-id="ad2ad-115">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="ad2ad-115">Lync Server 2010</span></span></th>
<th><span data-ttu-id="ad2ad-116">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="ad2ad-116">Office Communications Server 2007 R2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad2ad-117">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="ad2ad-117">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-118">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-118">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-119">Supported5</span><span class="sxs-lookup"><span data-stu-id="ad2ad-119">Supported5</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-120">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-120">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad2ad-121">Lync 2013 Basic</span><span class="sxs-lookup"><span data-stu-id="ad2ad-121">Lync 2013 Basic</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-122">Unterstützt </span><span class="sxs-lookup"><span data-stu-id="ad2ad-122">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-123">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-123">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-124">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-124">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad2ad-125">Lync Web App 2013</span><span class="sxs-lookup"><span data-stu-id="ad2ad-125">Lync Web App 2013</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-126">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-126">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-127">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-127">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-128">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-128">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad2ad-129">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="ad2ad-129">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-130">Unterstützt </span><span class="sxs-lookup"><span data-stu-id="ad2ad-130">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-131">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-131">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-132">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-132">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad2ad-133">Lync 2010 Attendant</span><span class="sxs-lookup"><span data-stu-id="ad2ad-133">Lync 2010 Attendant</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-134">Unterstützt </span><span class="sxs-lookup"><span data-stu-id="ad2ad-134">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-135">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-135">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-136">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-136">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad2ad-137">Lync 2010-Gruppenchat</span><span class="sxs-lookup"><span data-stu-id="ad2ad-137">Lync 2010 Group Chat</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-138">Supported1</span><span class="sxs-lookup"><span data-stu-id="ad2ad-138">Supported1</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-139">Supported2</span><span class="sxs-lookup"><span data-stu-id="ad2ad-139">Supported2</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-140">Nicht zutreffend</span><span class="sxs-lookup"><span data-stu-id="ad2ad-140">Not Applicable</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad2ad-141">Lync Web App 2010</span><span class="sxs-lookup"><span data-stu-id="ad2ad-141">Lync Web App 2010</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-142">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-142">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-143">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-143">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-144">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-144">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad2ad-145">Lync 2010-Teilnehmer</span><span class="sxs-lookup"><span data-stu-id="ad2ad-145">Lync 2010 Attendee</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-146">Nicht Supported3</span><span class="sxs-lookup"><span data-stu-id="ad2ad-146">Not Supported3</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-147">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-147">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-148">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-148">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad2ad-149">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="ad2ad-149">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-150">Interoperable4</span><span class="sxs-lookup"><span data-stu-id="ad2ad-150">Interoperable4</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-151">Unterstützt </span><span class="sxs-lookup"><span data-stu-id="ad2ad-151">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-152">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-152">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad2ad-153">Microsoft Office Communications Server 2007 R2-Vermittlung</span><span class="sxs-lookup"><span data-stu-id="ad2ad-153">Microsoft Office Communications Server 2007 R2 Attendant</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-154">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-154">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-155">Unterstützt </span><span class="sxs-lookup"><span data-stu-id="ad2ad-155">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-156">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-156">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad2ad-157">Office Communicator 2007</span><span class="sxs-lookup"><span data-stu-id="ad2ad-157">Office Communicator 2007</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-158">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-158">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-159">Unterstützt </span><span class="sxs-lookup"><span data-stu-id="ad2ad-159">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-160">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-160">Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad2ad-161">Office Live Meeting 2007</span><span class="sxs-lookup"><span data-stu-id="ad2ad-161">Office Live Meeting 2007</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-162">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-162">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-163">Unterstützt </span><span class="sxs-lookup"><span data-stu-id="ad2ad-163">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-164">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-164">Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad2ad-165">Windows Store-App für Lync</span><span class="sxs-lookup"><span data-stu-id="ad2ad-165">Lync Windows Store app</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-166">Unterstützt </span><span class="sxs-lookup"><span data-stu-id="ad2ad-166">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-167">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-167">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-168">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-168">Not Supported</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ad2ad-169">Informationen zu 1Für finden Sie unter [Migration von lync Server 2010, Gruppen-Chat oder Office Communications Server 2007 R2-Gruppenchat zu lync Server 2013, beständiger Chat Server](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md).</span><span class="sxs-lookup"><span data-stu-id="ad2ad-169">1For details, see [Migration from Lync Server 2010, Group Chat or Office Communications Server 2007 R2 Group Chat to Lync Server 2013, Persistent Chat Server](migration-from-lync-server-2010-group-chat-or-office-communications-server-2007-r2-group-chat-to-lync-server-2013-persistent-chat-server.md).</span></span>

<span data-ttu-id="ad2ad-170">2in Microsoft lync Server 2010, die Gruppen-Chatfunktionalität war mit dem Gruppen-Chat Server, einer vertrauenswürdigen Drittanbieteranwendung für lync Server 2010, verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-170">2In Microsoft Lync Server 2010, group chat functionality was available with Group Chat Server, a third-party trusted application for Lync Server 2010.</span></span> <span data-ttu-id="ad2ad-171">Lync 2013-Clients sind nicht mit lync Server 2010, Gruppen-Chat, kompatibel.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-171">Lync 2013 clients are not compatible with Lync Server 2010, Group Chat.</span></span>

<span data-ttu-id="ad2ad-172">3Lync Web App 2013 bietet nun eine vollständige Besprechungs Erfahrung, einschließlich Computer Audio und-Video, und gilt als Ersatz für lync 2010 Attendee.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-172">3Lync Web App 2013 now provides a full in-meeting experience, including computer audio and video, and is considered the replacement for Lync 2010 Attendee.</span></span> <span data-ttu-id="ad2ad-173">Lync 2010 Attendee stellt nur dann eine Verbindung mit lync Server 2013 her, wenn Sie einen nicht unterstützten Browser verwenden (Internet Explorer 6 oder Internet Explorer 7) und Windows XP.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-173">Lync 2010 Attendee will connect to Lync Server 2013 only when you are using an unsupported browser (Internet Explorer 6 or Internet Explorer 7) and Windows XP.</span></span>

<span data-ttu-id="ad2ad-174">4Die-Anwesenheits-und Chat Features in Office Communicator 2007 R2 sind mit lync Server 2013 kompatibel, die Konferenzfeatures jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-174">4The presence and IM features in Office Communicator 2007 R2 are compatible with Lync Server 2013, but conferencing features are not.</span></span> <span data-ttu-id="ad2ad-175">Während der Migration von Office Communications Server 2007 R2 eignet sich Office Communicator 2007 R2 für Anwesenheits-und Chat Interoperabilität, doch Benutzer sollten lync Web App 2013 verwenden, um an lync Server 2013-Besprechungen teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-175">During migration from Office Communications Server 2007 R2, Office Communicator 2007 R2 is suitable for presence and IM interoperability, but users should use Lync Web App 2013 to join Lync Server 2013 meetings.</span></span>

<span data-ttu-id="ad2ad-176">5 Einschränkungen finden Sie unter "Konferenz Feature-Unterstützung für lync 2013-Clients in lync Server 2010-Besprechungen" weiter unten in diesem Thema.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-176">5 For limitations, see "Conferencing Feature Support for Lync 2013 Clients in Lync Server 2010 Meetings" later in this topic.</span></span>

</div>

<div>

## <a name="interoperability-among-clients"></a><span data-ttu-id="ad2ad-177">Interoperabilität zwischen Clients</span><span class="sxs-lookup"><span data-stu-id="ad2ad-177">Interoperability among Clients</span></span>

<span data-ttu-id="ad2ad-178">Mit der Version lync Server 2013 können verschiedene Clientversionen nahtlos in Peer-zu-Peer-und Konferenzszenarien interagieren.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-178">With the Lync Server 2013 release, various client versions can interact seamlessly in both peer-to-peer and conferencing scenarios.</span></span> <span data-ttu-id="ad2ad-179">In diesem Abschnitt wird die Verfügbarkeit von Features erläutert, wenn Benutzer mit anderen Benutzern interagieren, die unterschiedliche Versionen von Clients und Servern verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-179">This section discusses feature availability when users interact with other users who are using different versions of clients and servers.</span></span>

<div>

## <a name="peer-to-peer-feature-support"></a><span data-ttu-id="ad2ad-180">Unterstützung von Peer-zu-Peer-Features</span><span class="sxs-lookup"><span data-stu-id="ad2ad-180">Peer-to-Peer Feature Support</span></span>

<span data-ttu-id="ad2ad-181">Peer-zu-Peer-Features werden für Benutzer unterstützt, die in unterschiedlichen Versionen des Servers unterschiedliche Clientversionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-181">Peer-to-peer features are supported for users who are homed on different versions of the server and who are using different client versions.</span></span> <span data-ttu-id="ad2ad-182">Die Benutzeroberfläche und die verfügbaren Features stehen im Einklang mit den Funktionen des Benutzer Clients und der Version des Servers, bei dem der Benutzer angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-182">The end-user experience and available features are consistent with the capabilities of the user’s client and the version of the server the user is signed in to.</span></span> <span data-ttu-id="ad2ad-183">Anders ausgedrückt:</span><span class="sxs-lookup"><span data-stu-id="ad2ad-183">In other words:</span></span>

  - <span data-ttu-id="ad2ad-184">Wenn ein Benutzer bei lync Server 2013 mit einem älteren Client angemeldet ist, verfügt der Benutzer über die gleiche Erfahrung, die er verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-184">If a user is signed in to Lync Server 2013 with an older client, the user will have the same experience he or she is used to.</span></span> <span data-ttu-id="ad2ad-185">Keines der neuen Features, die in lync Server 2013 eingeführt wurden, wird verfügbar sein, bis der Client des Benutzers aktualisiert wird.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-185">None of the new features introduced in Lync Server 2013 will be available until the user’s client is upgraded.</span></span> <span data-ttu-id="ad2ad-186">Beispiele sind Video Katalogansicht, HD-Video, aktualisierte PowerPoint-Freigabe und die Option zum stumm schalten aller Teilnehmer-Audio-und-Videoanrufe nach dem Besprechungseintrag.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-186">Examples include video gallery view, HD video, updated PowerPoint sharing, and the option to mute all attendee audio and video upon meeting entry.</span></span> <span data-ttu-id="ad2ad-187">Die neuen Features werden in den [neuen Konferenzfeatures in lync Server 2013](lync-server-2013-new-conferencing-features.md) und Neuerungen [für Clients in lync Server 2013](lync-server-2013-what-s-new-for-clients.md)erläutert.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-187">The new features are outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

  - <span data-ttu-id="ad2ad-188">Wenn ein Benutzer bei lync Server 2010 mit einem lync 2013-Client angemeldet ist, stehen alle neuen Features, die nicht von lync Server 2010 unterstützt werden, erst zur Verfügung, wenn der Benutzer zu lync Server 2013 verschoben wird.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-188">If a user is signed in to Lync Server 2010 with a Lync 2013 client, any new features not supported by Lync Server 2010 will be unavailable until the user is moved to Lync Server 2013.</span></span>

<span data-ttu-id="ad2ad-189">In der folgenden Tabelle wird die Verfügbarkeit von Features in Peer-to-Peer-Sitzungen verglichen, bei denen der Client entweder bei lync Server 2013 oder lync Server 2010 angemeldet ist.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-189">The following table compares feature availability in peer-to-peer sessions where the client is signed in to either Lync Server 2013 or Lync Server 2010.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ad2ad-190">Lync Web App und lync 2010 Attendee sind Besprechungs reine Clients, die nicht in dieser Tabelle enthalten sind.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-190">Lync Web App and Lync 2010 Attendee are meeting-only clients and aren’t included in this table.</span></span>



</div>


<table style="width:100%;">
<colgroup>
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
<col style="width: 14%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ad2ad-191">Client</span><span class="sxs-lookup"><span data-stu-id="ad2ad-191">Client</span></span></th>
<th><span data-ttu-id="ad2ad-192">Instant Messaging</span><span class="sxs-lookup"><span data-stu-id="ad2ad-192">Instant Messaging</span></span></th>
<th><span data-ttu-id="ad2ad-193">Anwesenheit</span><span class="sxs-lookup"><span data-stu-id="ad2ad-193">Presence</span></span></th>
<th><span data-ttu-id="ad2ad-194">VoIP</span><span class="sxs-lookup"><span data-stu-id="ad2ad-194">Voice</span></span></th>
<th><span data-ttu-id="ad2ad-195">Video</span><span class="sxs-lookup"><span data-stu-id="ad2ad-195">Video</span></span></th>
<th><span data-ttu-id="ad2ad-196">Anwendungsfreigabe</span><span class="sxs-lookup"><span data-stu-id="ad2ad-196">Application Sharing</span></span></th>
<th><span data-ttu-id="ad2ad-197">Dateiübertragung</span><span class="sxs-lookup"><span data-stu-id="ad2ad-197">File Transfer</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad2ad-198">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="ad2ad-198">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-199">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-199">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-200">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-200">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-201">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-201">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-202">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-202">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-203">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-203">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-204">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-204">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad2ad-205">Lync 2013 Basic</span><span class="sxs-lookup"><span data-stu-id="ad2ad-205">Lync 2013 Basic</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-206">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-206">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-207">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-207">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-208">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-208">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-209">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-209">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-210">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-210">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-211">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-211">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad2ad-212">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="ad2ad-212">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-213">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-213">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-214">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-214">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-215">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-215">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-216">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-216">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-217">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-217">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-218">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-218">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad2ad-219">Lync 2010 Attendant</span><span class="sxs-lookup"><span data-stu-id="ad2ad-219">Lync 2010 Attendant</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-220">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-220">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-221">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-221">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-222">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-222">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad2ad-223">Lync 2010 Mobile</span><span class="sxs-lookup"><span data-stu-id="ad2ad-223">Lync 2010 Mobile</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-224">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-224">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-225">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-225">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad2ad-226">Lync Phone Edition</span><span class="sxs-lookup"><span data-stu-id="ad2ad-226">Lync Phone Edition</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-227">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-227">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-228">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-228">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-229">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-229">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad2ad-230">Office Communicator 2007 R2</span><span class="sxs-lookup"><span data-stu-id="ad2ad-230">Office Communicator 2007 R2</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-231">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-231">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-232">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-232">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-233">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-233">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-234">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-234">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-235">Ja1</span><span class="sxs-lookup"><span data-stu-id="ad2ad-235">Yes1</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-236">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-236">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad2ad-237">Öffentlicher Chat (AOL, Yahoo!)</span><span class="sxs-lookup"><span data-stu-id="ad2ad-237">Public IM (AOL, Yahoo!)</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-238">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-238">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-239">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-239">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad2ad-240">Öffentlicher Chat (MSN, Windows Live Messenger)</span><span class="sxs-lookup"><span data-stu-id="ad2ad-240">Public IM (MSN, Windows Live Messenger)</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-241">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-241">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-242">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-242">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-243">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-243">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-244">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-244">Yes</span></span></p></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<div>


> [!IMPORTANT]  
> <UL>
> <LI>
> <P><span data-ttu-id="ad2ad-245">Ab dem 1. September, 2012, ist die Microsoft lync Public Chat-Benutzerabonnementlizenz (PIC USL) nicht mehr für den Kauf für neue oder erneuernde Vereinbarungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-245">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (PIC USL) is no longer available for the purchase for new or renewing agreements.</span></span> <span data-ttu-id="ad2ad-246">Kunden mit aktiven Lizenzen sind in der Lage, weiterhin mit Yahoo! zu verbünden</span><span class="sxs-lookup"><span data-stu-id="ad2ad-246">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="ad2ad-247">Messenger bis zum Shutdown-Datum des Diensts.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-247">Messenger until the service shutdown date.</span></span> <span data-ttu-id="ad2ad-248">Datum des Endes des Lebenszyklus von Juni 2014 für AOL und Yahoo!</span><span class="sxs-lookup"><span data-stu-id="ad2ad-248">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="ad2ad-249">wurde angekündigt.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-249">has been announced.</span></span> <span data-ttu-id="ad2ad-250">Ausführliche Informationen finden Sie <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">unter Unterstützung für die öffentliche Instant Messenger-Konnektivität in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-250">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>..</span></span></P>
> <LI>
> <P><span data-ttu-id="ad2ad-251">Bei der PIC-USL handelt es sich um eine pro Benutzer/Monat-Abonnementlizenz, die für lync Server oder Office Communications Server für die Föderation mit Yahoo! erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-251">The PIC USL is a per-user, per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="ad2ad-252">Messenger.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-252">Messenger.</span></span> <span data-ttu-id="ad2ad-253">Die Möglichkeit von Microsoft, diesen Dienst bereitzustellen, war von der Unterstützung durch Yahoo! abhängig, deren zugrunde liegende Vereinbarung nicht verlängert werden sollte.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-253">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which will not be renewed.</span></span></P>
> <LI>
> <P><span data-ttu-id="ad2ad-254">Lync ist mehr denn je ein leistungsfähiges Tool für die Verbindung zwischen Organisationen und Personen in der ganzen Welt.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-254">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="ad2ad-255">Für den Verbund mit Windows Live Messenger sind keine zusätzlichen Benutzer-und Gerätelizenzen außerhalb der lync-Standard CAL erforderlich.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-255">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="ad2ad-256">Skype Federation wird dieser Liste hinzugefügt und ermöglicht es lync-Benutzern, Hunderte von Millionen von Personen über Chat und Sprache zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-256">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people through IM and voice.</span></span></P></LI></UL>



</div>

<span data-ttu-id="ad2ad-257">1 in Office Communicator 2007 R2 steht nur die Desktopfreigabe (und nicht die Programmfreigabe) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-257">1 In Office Communicator 2007 R2, only desktop sharing (and not program sharing) is available.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="ad2ad-258">Die Desktop Freigabe zwischen Office Communicator 2007 R2 und Skype for Business 2015 kann nicht vom neueren Client initiiert werden, wenn die Benutzeroberfläche des Skype for Business 2015-Clients erzwungen wird.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-258">Desktop sharing between Office Communicator 2007 R2 and Skype for Business 2015 cannot be initiated from the newer client when the Skype for Business 2015 client user interface is enforced.</span></span>



</div>

</div>

<div>

## <a name="conferencing-feature-support-for-lync-2013-clients-in-lync-server-2010-meetings"></a><span data-ttu-id="ad2ad-259">Unterstützung von Konferenzfeatures für lync 2013-Clients in lync Server 2010-Besprechungen</span><span class="sxs-lookup"><span data-stu-id="ad2ad-259">Conferencing Feature Support for Lync 2013 Clients in Lync Server 2010 Meetings</span></span>

<span data-ttu-id="ad2ad-260">Wenn Benutzer mit einem lync 2013-Client an lync Server 2010-Besprechungen teilnehmen, können Sie mit den folgenden Ausnahmen auf lync 2013-Clientfeatures zugreifen:</span><span class="sxs-lookup"><span data-stu-id="ad2ad-260">When users join Lync Server 2010 meetings with a Lync 2013 client, they have access to Lync 2013 client features with the following exceptions:</span></span>

  - <span data-ttu-id="ad2ad-261">In den Verwaltungsoptionen für **Teilnehmer** , auf die durch zeigen auf das Symbol "Personen" im Besprechungsfenster zugegriffen werden kann, funktioniert die Option **keine Besprechung im Chat** .</span><span class="sxs-lookup"><span data-stu-id="ad2ad-261">In the **Participants** management options, which are accessible by pointing to the people icon in the meeting window, the **No Meeting IM** option does not function.</span></span>

  - <span data-ttu-id="ad2ad-262">Die Katalogansicht funktioniert in Videokonferenzen nicht.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-262">Gallery View does not function in video conferences.</span></span> <span data-ttu-id="ad2ad-263">Der Benutzer sieht nur den aktiven Lautsprecher und nicht alle Lautsprecher.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-263">The user sees only the active speaker instead of all speakers.</span></span> <span data-ttu-id="ad2ad-264">In der Liste der Optionen zum **Wählen eines Layouts** steht die **Katalogansicht** nicht zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-264">In the list of **Pick a Layout** options, **Gallery View** is unavailable</span></span>

  - <span data-ttu-id="ad2ad-265">Die Teilnehmerliste wird standardmäßig in Videokonferenzen angezeigt.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-265">The participant list displays by default in video conferences.</span></span>

  - <span data-ttu-id="ad2ad-266">Wenn Sie mit der rechten Maustaste auf einen Benutzer in der Teilnehmerliste klicken, sind die Optionen für das **Video Spotlight** und die **PIN-zu-Katalog** -Teilnehmer-Verwaltung Sperren nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-266">When right-clicking a user in the participants list, the **Lock the Video Spotlight** and **Pin to Gallery** participant management options are unavailable.</span></span>

</div>

<div>

## <a name="conferencing-feature-support-in-lync-server-2013-meetings"></a><span data-ttu-id="ad2ad-267">Unterstützung von Konferenzfeatures in lync Server 2013-Besprechungen</span><span class="sxs-lookup"><span data-stu-id="ad2ad-267">Conferencing Feature Support in Lync Server 2013 Meetings</span></span>

<span data-ttu-id="ad2ad-268">Lync Server 2013 bietet neue Konferenzfeatures, die Benutzern zur Verfügung stehen, nachdem Ihre Konten nach lync Server 2013 verschoben wurden und sich mit dem lync 2013-Client anmelden.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-268">Lync Server 2013 provides new conferencing features that become available to users after their accounts are moved to Lync Server 2013 and they sign in with the Lync 2013 client.</span></span> <span data-ttu-id="ad2ad-269">Beispiele sind Video Katalogansicht, HD-Video, PowerPoint-Freigabe und die Option zum stumm schalten aller Teilnehmer-Audio-und-Videoanrufe nach dem Besprechungseintrag.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-269">Examples include video gallery view, HD video, PowerPoint sharing, and the option to mute all attendee audio and video upon meeting entry.</span></span> <span data-ttu-id="ad2ad-270">Die neuen Features werden in den [neuen Konferenzfeatures in lync Server 2013](lync-server-2013-new-conferencing-features.md) und Neuerungen [für Clients in lync Server 2013](lync-server-2013-what-s-new-for-clients.md)erläutert.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-270">The new features are outlined in [New conferencing features in Lync Server 2013](lync-server-2013-new-conferencing-features.md) and [What's new for clients in Lync Server 2013](lync-server-2013-what-s-new-for-clients.md).</span></span>

<span data-ttu-id="ad2ad-271">In lync Server 2013-Besprechungen werden bestimmte Konferenzfeatures für Benutzer unterstützt, die in unterschiedlichen Versionen des Servers verwaltet werden und unterschiedliche Clients und Clientversionen verwenden.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-271">In Lync Server 2013 meetings, certain conferencing features are supported for users who are homed on different versions of the server and who are using different clients and client versions.</span></span> <span data-ttu-id="ad2ad-272">Wenn Clients an einer lync Server 2013-Besprechung teilnehmen, haben Benutzer Zugriff auf die Features und Funktionen, die in dieser Tabelle gezeigt werden.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-272">When clients join a Lync Server 2013 meeting, users have access to the features and capabilities shown in this table.</span></span>


<table style="width:100%;">
<colgroup>
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
<col style="width: 11%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ad2ad-273">Client</span><span class="sxs-lookup"><span data-stu-id="ad2ad-273">Client</span></span></th>
<th><span data-ttu-id="ad2ad-274">Peer-zu-Peer-Chat</span><span class="sxs-lookup"><span data-stu-id="ad2ad-274">Peer-to-peer IM</span></span></th>
<th><span data-ttu-id="ad2ad-275">VoIP</span><span class="sxs-lookup"><span data-stu-id="ad2ad-275">Voice</span></span></th>
<th><span data-ttu-id="ad2ad-276">Video</span><span class="sxs-lookup"><span data-stu-id="ad2ad-276">Video</span></span></th>
<th><span data-ttu-id="ad2ad-277">Anwendungsfreigabe</span><span class="sxs-lookup"><span data-stu-id="ad2ad-277">Application Sharing</span></span></th>
<th><span data-ttu-id="ad2ad-278">PowerPoint</span><span class="sxs-lookup"><span data-stu-id="ad2ad-278">PowerPoint</span></span></th>
<th><span data-ttu-id="ad2ad-279">Dateiübertragung</span><span class="sxs-lookup"><span data-stu-id="ad2ad-279">File Transfer</span></span></th>
<th><span data-ttu-id="ad2ad-280">Whiteboard</span><span class="sxs-lookup"><span data-stu-id="ad2ad-280">Whiteboard</span></span></th>
<th><span data-ttu-id="ad2ad-281">Abruf</span><span class="sxs-lookup"><span data-stu-id="ad2ad-281">Polling</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad2ad-282">Lync 2013</span><span class="sxs-lookup"><span data-stu-id="ad2ad-282">Lync 2013</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-283">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-283">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-284">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-284">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-285">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-285">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-286">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-286">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-287">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-287">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-288">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-288">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-289">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-289">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-290">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-290">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad2ad-291">Lync 2013 Basic</span><span class="sxs-lookup"><span data-stu-id="ad2ad-291">Lync 2013 Basic</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-292">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-292">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-293">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-293">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-294">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-294">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-295">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-295">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-296">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-296">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-297">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-297">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-298">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-298">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-299">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-299">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad2ad-300">Lync Web App</span><span class="sxs-lookup"><span data-stu-id="ad2ad-300">Lync Web App</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-301">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-301">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-302">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-302">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-303">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-303">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-304">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-304">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-305">Ja2</span><span class="sxs-lookup"><span data-stu-id="ad2ad-305">Yes2</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-306">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-306">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-307">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-307">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-308">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-308">Yes</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad2ad-309">Lync 2010</span><span class="sxs-lookup"><span data-stu-id="ad2ad-309">Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-310">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-310">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-311">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-311">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-312">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-312">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-313">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-313">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-314">Ja3</span><span class="sxs-lookup"><span data-stu-id="ad2ad-314">Yes3</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-315">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-315">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-316">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-316">Yes</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-317">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-317">Yes</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad2ad-318">Office Communicator 2007 R2 4</span><span class="sxs-lookup"><span data-stu-id="ad2ad-318">Office Communicator 2007 R2 4</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-319">Ja</span><span class="sxs-lookup"><span data-stu-id="ad2ad-319">Yes</span></span></p></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
<td></td>
</tr>
</tbody>
</table>


<span data-ttu-id="ad2ad-320">1 in Office Communicator 2007 R2 steht nur die Desktopfreigabe (und nicht die Programmfreigabe) zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-320">1 In Office Communicator 2007 R2, only desktop sharing (and not program sharing) is available.</span></span>

<span data-ttu-id="ad2ad-321">2 lync Server 2013 verwendet einen aktualisierten Mechanismus zum Hochladen von PowerPoint-Dateien.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-321">2 Lync Server 2013 uses an updated mechanism for uploading PowerPoint files.</span></span> <span data-ttu-id="ad2ad-322">Lync Web App-Benutzer, die an einer Besprechung teilnehmen, die ursprünglich auf lync Server 2010 geplant war, können PowerPoint-Präsentationen anzeigen und darin navigieren, jedoch keine PowerPoint-Dateien hochladen.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-322">Lync Web App users who join a meeting that was originally scheduled on Lync Server 2010 can view and navigate PowerPoint presentations, but cannot upload PowerPoint files.</span></span>

<span data-ttu-id="ad2ad-323">3 Wenn die Besprechung auf lync Server 2013 geplant war und PowerPoint-Folien von einem lync 2013-Client hochgeladen wurden, haben lync 2010-Benutzer nur Zugriff auf die Folien.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-323">3 If the meeting was scheduled on Lync Server 2013 and PowerPoint slides were uploaded by a Lync 2013 client, Lync 2010 users have view-only access to the slides.</span></span> <span data-ttu-id="ad2ad-324">Wenn umgekehrt die PowerPoint-Folien von einem lync 2010-Benutzer hochgeladen wurden, können lync Server 2013-Benutzer die Ansicht und Folien anzeigen und, wenn der Office Web Apps-Server konfiguriert ist, auf neue Funktionen zugreifen, wie Anzeige, Animationen, Folienübergänge und eingebettete Videos mit höherer Auflösung.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-324">Conversely, if the PowerPoint slides were uploaded by a Lync 2010 user, Lync Server 2013 users will be able to view and slides and, if Office Web Apps Server is configured, access new capabilities such as higher resolution display, animations, slide transitions, and embedded video.</span></span> <span data-ttu-id="ad2ad-325">Weitere Informationen finden Sie unter [Konfigurieren der Integration in Office Web Apps Server und lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span><span class="sxs-lookup"><span data-stu-id="ad2ad-325">For more information, see [Configuring integration with Office Web Apps Server and Lync Server 2013](lync-server-2013-enabling-office-web-apps-server-and-lync-server-2013.md).</span></span>

<span data-ttu-id="ad2ad-326">4Die-Anwesenheits-und Chat Features in Office Communicator 2007 R2 sind mit lync Server 2013 kompatibel, die Konferenzfeatures jedoch nicht.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-326">4The presence and IM features in Office Communicator 2007 R2 are compatible with Lync Server 2013, but conferencing features are not.</span></span> <span data-ttu-id="ad2ad-327">Während der Migration von Office Communications Server 2007 R2 eignet sich Office Communicator 2007 R2 für Anwesenheits-und Chat Interoperabilität, doch Benutzer sollten lync Web App 2013 verwenden, um an lync Server 2013-Besprechungen teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-327">During migration from Office Communications Server 2007 R2, Office Communicator 2007 R2 is suitable for presence and IM interoperability, but users should use Lync Web App 2013 to join Lync Server 2013 meetings.</span></span>

</div>

</div>

<div>

## <a name="scheduling-add-in-support"></a><span data-ttu-id="ad2ad-328">Planen der Add-in-Unterstützung</span><span class="sxs-lookup"><span data-stu-id="ad2ad-328">Scheduling Add-in Support</span></span>

<span data-ttu-id="ad2ad-329">Die Server Unterstützung für die verschiedenen Terminplan-Add-Ins ist mit der Kompatibilität zwischen Server-und Clientversionen konsistent.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-329">Server support for the various scheduling add-ins is consistent with server and client version compatibility.</span></span> <span data-ttu-id="ad2ad-330">Im Allgemeinen werden die folgenden Planungs-Add-Ins in lync Server 2013 unterstützt.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-330">In general, the following scheduling add-ins are supported on Lync Server 2013.</span></span> <span data-ttu-id="ad2ad-331">In früheren Versionen von Add-Ins werden jedoch keine neuen lync 2013-Add-in-Features bereitgestellt, wie beispielsweise die Option zum stumm schalten aller Teilnehmer-Audio-und-Videoanrufe nach dem Besprechungseintrag.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-331">However, previous versions of add-ins do not provide new Lync 2013 add-in features, such as the option to mute all attendee audio and video upon meeting entry.</span></span>

  - <span data-ttu-id="ad2ad-332">**Online Besprechungs-Add-in für lync 2013**   Bietet die gleichen Funktionen wie das Online Besprechungs-Add-in für lync 2010 mit dem Hinzufügen von Steuerelementen für Teilnehmer-stumm Schaltungen, mit denen Besprechungsorganisatoren Konferenzen planen können, bei denen die Teilnehmer Audio und Videostandard mäßig stumm geschaltet sind.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-332">**Online Meeting Add-in for Lync 2013**   Provides the same features as the Online Meeting Add-in for Lync 2010, with the addition of attendee mute controls, which allow meeting organizers to schedule conferences that have attendee audio and video muted by default.</span></span> <span data-ttu-id="ad2ad-333">Administratoren können die Besprechungseinladungen des Unternehmens auch anpassen, indem Sie ein benutzerdefiniertes Logo, eine Support-URL, eine URL zur rechtlichen Verzichtserklärung oder einen benutzerdefinierten Fußzeilentext hinzufügen.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-333">Administrators can also customize the organization’s meeting invitations by adding a custom logo, a support URL, a legal disclaimer URL, or custom footer text.</span></span>

  - <span data-ttu-id="ad2ad-334">**Online Besprechungs-Add-in für lync 2010**   Bietet Planung für lync-Besprechungen und entfernt die Möglichkeit zum Planen von Office Live Meeting-Konferenzen.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-334">**Online Meeting Add-in for Lync 2010**   Provides scheduling for Lync meetings and removes the capability to schedule Office Live Meeting conferences.</span></span>

  - <span data-ttu-id="ad2ad-335">**Office Communicator 2007 R2-Konferenz-Add-in**   Bietet Terminplanung für Office Live Meeting-Konferenzen und Office Communicator 2007 R2-Konferenzen.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-335">**Office Communicator 2007 R2 Conferencing Add-in**   Provides scheduling for both Office Live Meeting conferences and Office Communicator 2007 R2 conferences.</span></span> 

<div>


> [!NOTE]  
> <span data-ttu-id="ad2ad-336">Live Meeting-Konferenzen können auf lync Server 2013 nicht geplant werden.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-336">Live Meeting conferences cannot be scheduled on Lync Server 2013.</span></span>



</div>


<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="ad2ad-337">Terminplanungs-Client</span><span class="sxs-lookup"><span data-stu-id="ad2ad-337">Scheduling Client</span></span></th>
<th><span data-ttu-id="ad2ad-338">Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ad2ad-338">Lync Server 2013</span></span></th>
<th><span data-ttu-id="ad2ad-339">Lync Server 2010</span><span class="sxs-lookup"><span data-stu-id="ad2ad-339">Lync Server 2010</span></span></th>
<th><span data-ttu-id="ad2ad-340">Office Communications Server 2007 R2</span><span class="sxs-lookup"><span data-stu-id="ad2ad-340">Office Communications Server 2007 R2</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="ad2ad-341">Online Besprechungs-Add-in für lync 2013 (kann mit Office 2013, Outlook 2010 und Outlook 2007 verwendet werden)</span><span class="sxs-lookup"><span data-stu-id="ad2ad-341">Online Meeting Add-in for Lync 2013 (can be used with Office 2013, Outlook 2010, and Outlook 2007)</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-342">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-342">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-343">Unterstützt (neue Add-in-Features sind nicht verfügbar)</span><span class="sxs-lookup"><span data-stu-id="ad2ad-343">Supported (new add-in features not available)</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-344">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-344">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad2ad-345">Lync 2013 Web Scheduler</span><span class="sxs-lookup"><span data-stu-id="ad2ad-345">Lync 2013 Web Scheduler</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-346">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-346">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-347">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-347">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-348">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-348">Not Supported</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="ad2ad-349">Onlinebesprechungs-Add-In für Lync 2010</span><span class="sxs-lookup"><span data-stu-id="ad2ad-349">Online Meeting Add-in for Lync 2010</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-350">Unterstützt </span><span class="sxs-lookup"><span data-stu-id="ad2ad-350">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-351">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-351">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-352">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-352">Not Supported</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="ad2ad-353">Office Communicator 2007 R2-Konferenz-Add-in</span><span class="sxs-lookup"><span data-stu-id="ad2ad-353">Office Communicator 2007 R2 Conferencing Add-in</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-354">Nicht unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-354">Not Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-355">Unterstützt </span><span class="sxs-lookup"><span data-stu-id="ad2ad-355">Supported</span></span></p></td>
<td><p><span data-ttu-id="ad2ad-356">Unterstützt</span><span class="sxs-lookup"><span data-stu-id="ad2ad-356">Supported</span></span></p></td>
</tr>
</tbody>
</table>


</div>

<div>

## <a name="support-for-joining-meetings"></a><span data-ttu-id="ad2ad-357">Unterstützung für die Teilnahme an Besprechungen</span><span class="sxs-lookup"><span data-stu-id="ad2ad-357">Support for Joining Meetings</span></span>

<span data-ttu-id="ad2ad-358">Alle Clients, die von lync Server 2013 unterstützt werden, dürfen an lync 2013-Besprechungen teilnehmen.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-358">All of the clients that Lync Server 2013 supports are allowed to join Lync 2013 meetings.</span></span> <span data-ttu-id="ad2ad-359">Da es sich bei lync Web App um eine Webkomponente des Servers handelt, wird in den Fällen, in denen lync Web App für die Teilnahme an einer lync Server 2013-Besprechung verwendet wird, immer die neuere Version von lync Web App verwendet.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-359">Because Lync Web App is a web component of the server, in cases where Lync Web App is used to join a Lync Server 2013 meeting, the newer version of Lync Web App is always used.</span></span>

<span data-ttu-id="ad2ad-360">Lync 2013-Clients können an Besprechungen teilnehmen, die in lync 2010 und Office Communications Server 2007 R2 mit skalierten Funktionen gehostet werden.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-360">Lync 2013 clients can join meetings hosted on Lync 2010 and Office Communications Server 2007 R2 with scaled-down functionality.</span></span> <span data-ttu-id="ad2ad-361">In-Meeting-Features sind durch die Version des Servers, auf dem die Besprechung gehostet wird, limitiert.</span><span class="sxs-lookup"><span data-stu-id="ad2ad-361">In-meeting features are limited by the version of the server on which the meeting is hosted.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ad2ad-362">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ad2ad-362">See Also</span></span>


[<span data-ttu-id="ad2ad-363">Lync Windows Store-App-Anforderungen für lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ad2ad-363">Lync Windows Store app requirements for Lync Server 2013</span></span>](lync-server-2013-lync-windows-store-app-requirements.md)  
[<span data-ttu-id="ad2ad-364">Neue Konferenzfunktionen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ad2ad-364">New conferencing features in Lync Server 2013</span></span>](lync-server-2013-new-conferencing-features.md)  
[<span data-ttu-id="ad2ad-365">Neue Funktionen für Clients in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ad2ad-365">What's new for clients in Lync Server 2013</span></span>](lync-server-2013-what-s-new-for-clients.md)  
  

<span data-ttu-id="ad2ad-366"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ad2ad-366"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

