---
title: Übersicht über Einwahlkonferenzen in lync Server 2013
description: Übersicht über Einwahlkonferenzen in lync Server 2013
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Dial-in conferencing overview
ms:assetid: 6e581cef-960a-4730-8b22-91b2129d34e3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg398524(v=OCS.15)
ms:contentKeyID: 48184436
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: fa9418c13b56faab747d2c92df3301fe15d722eb
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49429241"
---
# <a name="overview-of-dial-in-conferencing-in-lync-server-2013"></a><span data-ttu-id="15e35-103">Übersicht über Einwahlkonferenzen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="15e35-103">Overview of dial-in conferencing in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="15e35-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="15e35-104">

<span> </span></span></span>

<span data-ttu-id="15e35-105">_**Letztes Änderungsdatum des Themas:** 2012-09-30_</span><span class="sxs-lookup"><span data-stu-id="15e35-105">_**Topic Last Modified:** 2012-09-30_</span></span>

<span data-ttu-id="15e35-106">Wenn in Ihrer Organisation Benutzer vorhanden sind, die an den lokalen Konferenzen von lync Server 2013 teilnehmen müssen, wenn Sie nicht im Büro sind oder keinen Zugriff auf einen Computer haben, können Sie Einwahlkonferenzen bereitstellen, damit Sie mit einem PSTN-Telefon (Public Switched Telephone Network) an der Konferenz teilnehmen können.</span><span class="sxs-lookup"><span data-stu-id="15e35-106">If your organization has users who need to attend Lync Server 2013 on-premises conferences when they are out of the office or do not have access to a computer, you can deploy dial-in conferencing so that they can join the conference by using a public switched telephone network (PSTN) phone.</span></span>

<span data-ttu-id="15e35-107">Einwahlkonferenzen sind ein optionales Feature, das Sie beim Bereitstellen von lync Server 2013-Konferenzen konfigurieren können.</span><span class="sxs-lookup"><span data-stu-id="15e35-107">Dial-in conferencing is an optional feature that you can configure when you deploy Lync Server 2013 conferencing.</span></span> <span data-ttu-id="15e35-108">Obwohl Einwahlkonferenzen einige der gleichen lync Server 2013-Komponenten verwenden, die Enterprise-VoIP verwendet, können Sie Einwahlkonferenzen auch dann bereitstellen, wenn Sie Enterprise-VoIP nicht bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="15e35-108">Although dial-in conferencing uses some of the same Lync Server 2013 components that Enterprise Voice uses, you can deploy dial-in conferencing even if you do not deploy Enterprise Voice.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="15e35-109">Wenn Sie Einwahlkonferenzen bereitstellen, müssen Sie Sie in jedem Pool bereitstellen, in dem Sie die lync Server 2013-Konferenz bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="15e35-109">If you deploy dial-in conferencing, you must deploy it in every pool where you deploy Lync Server 2013 conferencing.</span></span> <span data-ttu-id="15e35-110">Sie müssen keine Zugriffsnummern in jedem Pool zuweisen, aber Sie müssen das Einwahlfeature in jedem Pool bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="15e35-110">You do not need to assign access numbers in every pool, but you must deploy the dial-in feature in every pool.</span></span> <span data-ttu-id="15e35-111">Diese Anforderung unterstützt das Feature "aufgezeichnete Namen", wenn ein Benutzer eine Zugriffsnummer aus einem Pool anruft, um an einer lync Server 2013-Konferenz in einem anderen Pool teilzunehmen.</span><span class="sxs-lookup"><span data-stu-id="15e35-111">This requirement supports the recorded name feature when a user calls an access number from one pool to join a Lync Server 2013 conference in a different pool.</span></span>



</div>

<span data-ttu-id="15e35-112">Konferenzen müssen für Einwahlzugriff in Besprechungsrichtlinien aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="15e35-112">Conferences must be enabled for dial-in access in meeting policy.</span></span> <span data-ttu-id="15e35-113">In der Standardeinstellung umfassen Konferenzen, die für den Zugriff per Einwahl aktiviert sind, die folgenden Informationen in der Konferenzeinladung:</span><span class="sxs-lookup"><span data-stu-id="15e35-113">By default, conferences that are enabled for dial-in access include the following information in the conference invitation:</span></span>

  - <span data-ttu-id="15e35-114">Eine numerische Konferenz-ID, die die Konferenz kennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="15e35-114">A numeric conference ID that identifies the conference.</span></span>

  - <span data-ttu-id="15e35-115">Eine oder mehrere PSTN-Zugriffsnummern.</span><span class="sxs-lookup"><span data-stu-id="15e35-115">One or more PSTN access numbers.</span></span>

  - <span data-ttu-id="15e35-116">Einen Link zu einer Seite mit Einstellungen für Einwahlkonferenzen, die eine vollständige Liste der Zugriffsnummern mit den zugehörigen Sprachen enthält; ein Ort zum Erstellen, zurücksetzen oder entsperren persönlicher Identifikationsnummern (Pins); und weitere Informationen, wie etwa DTMF-Steuerelemente (Dual Tone Multi-Frequency).</span><span class="sxs-lookup"><span data-stu-id="15e35-116">A link to a Dial-in Conferencing Settings page, which contains a complete list of access numbers with their associated languages; a place to create, reset, or unblock personal identification numbers (PINs); and other information, such as dual-tone multi-frequency (DTMF) controls.</span></span>

<span data-ttu-id="15e35-117">Einwahlkonferenzen können sowohl für Unternehmensbenutzer als auch für anonyme Benutzer eingesetzt werden.</span><span class="sxs-lookup"><span data-stu-id="15e35-117">Dial-in conferencing supports both enterprise and anonymous users.</span></span> <span data-ttu-id="15e35-118">Unternehmensbenutzer verfügen über die Anmeldeinformationen für Active Directory-Domänendienste und lync Server 2013-Konten innerhalb Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="15e35-118">Enterprise users have Active Directory Domain Services credentials and Lync Server 2013 accounts within their organization.</span></span> <span data-ttu-id="15e35-119">Anonyme Benutzer verfügen über keine Anmeldeinformationen innerhalb Ihrer Organisation.</span><span class="sxs-lookup"><span data-stu-id="15e35-119">Anonymous users do not have enterprise credentials within your organization.</span></span> <span data-ttu-id="15e35-120">Im Zusammenhang mit Einwahlkonferenzen wird ein Benutzer in einer Organisation eines Verbundpartners, der über PSTN eine Verbindung mit einer Konferenz herstellt, als anonymer Benutzer betrachtet.</span><span class="sxs-lookup"><span data-stu-id="15e35-120">In the dial-in conferencing context, a user in a federated partner’s organization who uses the PSTN to connect to a conference is treated like an anonymous user.</span></span> <span data-ttu-id="15e35-121">Im Gegensatz zu anderen Kontexten werden Partnerbenutzer bei Einwahlkonferenzen nicht authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="15e35-121">For dial-in conferencing, unlike other contexts, federated users are not authenticated.</span></span>

<span data-ttu-id="15e35-p105">Unternehmensbenutzer oder Konferenzleiter, die einer für den Zugriff per Einwahl aktivierten Konferenz beitreten, wählen eine der Zugriffsnummern für die Konferenz und werden anschließend zur Eingabe der Konferenz-ID aufgefordert. Wenn der Konferenzleiter der Besprechung noch nicht beigetreten ist, können Benutzer entweder ihre Unified Communications-Durchwahl (UC) (oder die vollständige Telefonnummer) und PIN eingeben oder warten, bis der Konferenzleiter bestätigt, dass sie zur Konferenz zugelassen werden. Besprechungsorganisatoren können der Besprechung als Konferenzleiter beitreten, indem sie lediglich ihre PIN eingeben. Der Front-End-Server verwendet die Kombination aus der vollständigen Telefonnummer oder Durchwahl und der PIN, um Unternehmensbenutzer eindeutig ihren Active-Anmeldeinformationen zuzuordnen. So werden Unternehmensbenutzer anhand ihres Namens in der Konferenz authentifiziert und identifiziert. Unternehmensbenutzer können auch eine Konferenzrolle übernehmen, die vom Organisator vorgegeben ist.</span><span class="sxs-lookup"><span data-stu-id="15e35-p105">Enterprise users or conference leaders who join a conference that is enabled for dial-in access dial one of the conference access numbers and then are prompted to enter the conference ID. If a leader has not yet joined the meeting, users can either enter their unified communications (UC) extension (or full phone number) and PIN or wait to be admitted by a leader. The Meeting organizer can join the meeting as a leader by entering just their PIN. The Front End Server uses the combination of full phone number or extension, and PIN, to uniquely map enterprise users to their Active Directory credentials. As a result, enterprise users are authenticated and identified by name in the conference. Enterprise users can also assume a conference role predefined by the organizer.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="15e35-128">Enterprise-Benutzer, die sich über ein Office-IP-Telefon oder über lync Server 2013 oder lync 2010 Attendant einwählen, werden nicht zur Eingabe Ihrer Telefonnummer aufgefordert, da Sie bereits authentifiziert sind.</span><span class="sxs-lookup"><span data-stu-id="15e35-128">Enterprise users who dial in from an office IP phone or from Lync Server 2013 or Lync 2010 Attendant are not prompted for their phone number because they are already authenticated.</span></span>



</div>

<span data-ttu-id="15e35-p106">Anonyme Benutzer, die einer Einwahlkonferenz beitreten möchten, wählen eine der Zugriffsnummern für die Konferenz und werden zur Eingabe der Konferenz-ID aufgefordert. Nicht authentifizierte anonyme Benutzer werden zudem zur Aufzeichnung ihres Namens aufgefordert. Der aufgezeichnete Name identifiziert nicht authentifizierte Benutzer in der Konferenz. Anonyme Benutzer werden erst zur Konferenz zugelassen, wenn mindestens ein Konferenzleiter oder authentifizierter Benutzer beigetreten ist. Das Zuweisen einer vordefinierten Rolle zu anonymen Benutzern ist nicht möglich.</span><span class="sxs-lookup"><span data-stu-id="15e35-p106">Anonymous users who want to join a dial-in conference dial one of the conference access numbers and then they are prompted to enter the conference ID. Unauthenticated anonymous users are also prompted to record their name. The recorded name identifies unauthenticated users in the conference. Anonymous users are not admitted to the conference until at least one leader or authenticated user has joined, and they cannot be assigned a predefined role.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="15e35-p107">Unternehmensbenutzer, die ihre Telefonnummer und PIN nicht eingeben, werden nicht authentifiziert. Diese Benutzer werden zur Aufzeichnung ihres Namens aufgefordert und in der Konferenz als anonyme Benutzer behandelt.</span><span class="sxs-lookup"><span data-stu-id="15e35-p107">Enterprise users who choose not to enter their phone number and PIN are not authenticated. They are prompted to record their name and are treated as anonymous users in the conference.</span></span>



</div>

<span data-ttu-id="15e35-135">Zur Zeitplanung kann der Besprechungsorganisator den Zugriff auf die Besprechung einschränken, indem die Besprechung geschlossen oder gesperrt wird.</span><span class="sxs-lookup"><span data-stu-id="15e35-135">At schedule time, the meeting organizer can choose to restrict access to the meeting by making the meeting closed or locked.</span></span> <span data-ttu-id="15e35-136">In diesem Fall müssen sich die Benutzer bei der Einwahl authentifizieren.</span><span class="sxs-lookup"><span data-stu-id="15e35-136">In this case, dial-in users are requested to authenticate.</span></span> <span data-ttu-id="15e35-137">Wenn Benutzer von Einwahl Fehlern Versagen oder sich nicht authentifizieren möchten, werden Sie in die Lobby übertragen.</span><span class="sxs-lookup"><span data-stu-id="15e35-137">If dial-in users fail or choose not to authenticate, they are transferred to the lobby.</span></span> <span data-ttu-id="15e35-138">Sie warten in der Wartehalle, bis eine Führungslinie Sie annimmt oder ablehnt, oder Sie verfallen und werden getrennt.</span><span class="sxs-lookup"><span data-stu-id="15e35-138">They wait in the lobby until a leader accepts or rejects them, or they time out and are disconnected.</span></span> <span data-ttu-id="15e35-139">Einwahlbenutzer hören Musik, wenn Sie darauf warten, zur Konferenz zugelassen zu werden.</span><span class="sxs-lookup"><span data-stu-id="15e35-139">Dial-in users hear music if they are waiting to be admitted to the conference.</span></span> <span data-ttu-id="15e35-140">Sobald Einwahlbenutzer zu einer Konferenz zugelassen wurden, können sie am Audioteil der Konferenz teilnehmen und über das Tastenfeld ihres Telefons DTMF-Befehle (Dual-Tone Multi-Frequency, Mehrfrequenzverfahren) eingeben.</span><span class="sxs-lookup"><span data-stu-id="15e35-140">After they are admitted to a conference, dial-in users can participate in the audio portion of the conference and can exercise dual-tone multi-frequency (DTMF) commands by using the phone keypad.</span></span> <span data-ttu-id="15e35-141">Der Leiter einer Einwahlkonferenz kann mithilfe von DTMF-Befehlen die Möglichkeit der Teilnehmer zur Stummschaltung ein- oder ausschalten, die Konferenz sperren oder entsperren, Personen aus der Lobby aufnehmen sowie Ankündigungen bei Zu- und Abgang ein- bzw. ausschalten.</span><span class="sxs-lookup"><span data-stu-id="15e35-141">Dial-in leaders can exercise DTMF commands to turn participants' ability to unmute on or off, lock or unlock the conference, admit people from the lobby, and turn entry and exit announcements on or off.</span></span> <span data-ttu-id="15e35-142">Konferenzleiter können mithilfe von DTMF-Befehlen zudem alle Teilnehmer aus der Lobby zulassen. Durch diese Aktion werden die Berechtigungen für die Besprechung so geändert, dass anschließend sämtliche Benutzer zugelassen werden, die der Besprechung beitreten.</span><span class="sxs-lookup"><span data-stu-id="15e35-142">Leaders can also use a DTMF command to admit everyone from the lobby, which changes the permissions of the meeting to allow anyone who subsequently joins.</span></span> <span data-ttu-id="15e35-143">Alle eingewählten Teilnehmer können DTMF-Befehle ausführen, um Hilfeinformationen abzuhören, die Namen der Teilnehmer wiederzugeben und sich selbst stumm zu schalten.</span><span class="sxs-lookup"><span data-stu-id="15e35-143">All dial-in participants can exercise DTMF commands to hear Help, listen to the conference roster, and mute themselves.</span></span>

<span data-ttu-id="15e35-144">Einwahl Teilnehmer (das heißt, ob Sie aus dem PSTN wählen), während der Konferenz persönliche Ankündigungen hören, beispielsweise ob Sie stumm geschaltet oder nicht stumm geschaltet wurden, die Besprechung aufgezeichnet wird oder jemand in der Lobby wartet.</span><span class="sxs-lookup"><span data-stu-id="15e35-144">Dial-in participants (that is, whether or not they dial from the PSTN), hear personal announcements during the conference, such as whether they have been muted or unmuted, the meeting is being recorded, or someone is waiting in the lobby.</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="15e35-145">Für Teilnehmer, die sich nicht einwählen, sondern der Besprechung über einen Link beitreten, werden keine persönlichen Ansagen wiedergegeben.</span><span class="sxs-lookup"><span data-stu-id="15e35-145">Participants who join the conference by clicking a link instead of dialing in do not hear personal announcements.</span></span>



<span data-ttu-id="15e35-146"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="15e35-146"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

