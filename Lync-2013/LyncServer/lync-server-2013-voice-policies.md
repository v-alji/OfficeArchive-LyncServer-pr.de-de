---
title: 'Lync Server 2013: VoIP-Richtlinien'
description: 'Lync Server 2013: VoIP-Richtlinien.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Voice policies
ms:assetid: b7433c62-9d8c-48af-89a0-19f0d34806ec
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg412891(v=OCS.15)
ms:contentKeyID: 48185223
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: b85e69c83a8f964d9114a83abe6978f040f044d1
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49438638"
---
# <a name="voice-policies-in-lync-server-2013"></a><span data-ttu-id="d6936-103">VoIP-Richtlinien in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d6936-103">Voice policies in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d6936-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d6936-104">

<span> </span></span></span>

<span data-ttu-id="d6936-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="d6936-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="d6936-106">Lync Server- *VoIP-Richtlinien* definieren für jeden Benutzer, jede Website oder jede Organisation, der die Richtlinie zugewiesen ist, die folgenden Punkte:</span><span class="sxs-lookup"><span data-stu-id="d6936-106">Lync Server *voice policies* define the following for each user, site, or organization that is assigned the policy:</span></span>

  - <span data-ttu-id="d6936-107">Eine Reihe von Anruffeatures, die aktiviert oder deaktiviert werden können, um die für Benutzer verfügbare Enterprise-VoIP-Funktionalität zu ermitteln.</span><span class="sxs-lookup"><span data-stu-id="d6936-107">A set of calling features that can be enabled or disabled to determine the Enterprise Voice functionality available to users.</span></span>

  - <span data-ttu-id="d6936-108">Einer Gruppe von Telefonfestnetz-Verwendungseinträgen, die festlegen, welche Arten von Anrufen erlaubt sind.</span><span class="sxs-lookup"><span data-stu-id="d6936-108">A set of public switched telephone network (PSTN) usage records that define what types of calls are authorized.</span></span>

<div>

## <a name="planning-for-voice-policies"></a><span data-ttu-id="d6936-109">Planen von VoIP-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d6936-109">Planning for Voice Policies</span></span>

<span data-ttu-id="d6936-110">Mit den folgenden Schritten können Sie die VoIP-Richtlinien planen, die Sie für Ihre Enterprise-VoIP-Bereitstellung benötigen:</span><span class="sxs-lookup"><span data-stu-id="d6936-110">The following steps will help you plan the voice policies that you will need for your Enterprise Voice deployment:</span></span>

  - <span data-ttu-id="d6936-111">Legen Sie fest, wie die globale VoIP-Richtlinie (die Standard-VoIP-Richtlinie, die mit dem Produkt installiert wird) konfiguriert werden soll.</span><span class="sxs-lookup"><span data-stu-id="d6936-111">Determine how you will configure your global voice policy (the default voice policy that is installed with the product).</span></span> <span data-ttu-id="d6936-112">Diese Richtlinie gilt für alle Enterprise-VoIP-Benutzer, denen nicht explizit eine Richtlinie auf Website-oder Benutzerebene zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="d6936-112">This policy will apply to all Enterprise Voice users who are not explicitly assigned a site-level or per-user policy.</span></span>

  - <span data-ttu-id="d6936-113">Bestimmen der ggf. erforderlichen VoIP-Richtlinien auf Standortebene.</span><span class="sxs-lookup"><span data-stu-id="d6936-113">Identify any site-level voice policies that you might need.</span></span>

  - <span data-ttu-id="d6936-114">Bestimmen der ggf. erforderlichen benutzerbezogenen VoIP-Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="d6936-114">Identify any per-user voice policies that you might need.</span></span>

  - <span data-ttu-id="d6936-115">Entscheiden, welche Anruffunktionen für jede VoIP-Richtlinie aktiviert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d6936-115">Decide which call features to enable for each voice policy.</span></span>

  - <span data-ttu-id="d6936-116">Bestimmen, welche PSTN-Verwendungseinträge für jede VoIP-Richtlinie konfiguriert werden sollen.</span><span class="sxs-lookup"><span data-stu-id="d6936-116">Determine what PSTN usage records to configure for each voice policy.</span></span>

<div>

## <a name="voice-policy-scope"></a><span data-ttu-id="d6936-117">Gültigkeitsbereich von VoIP-Richtlinien</span><span class="sxs-lookup"><span data-stu-id="d6936-117">Voice Policy Scope</span></span>

<span data-ttu-id="d6936-118">Der *Gültigkeitsbereich von VoIP-Richtlinien* bestimmt die Hierarchieebene, auf der die Richtlinie gelten soll.</span><span class="sxs-lookup"><span data-stu-id="d6936-118">*Voice policy scope* determines the hierarchical level at which the policy can be applied.</span></span> <span data-ttu-id="d6936-119">In lync Server können Sie VoIP-Richtlinien mit den folgenden Bereichsebenen konfigurieren (in der Liste der am häufigsten vorgestellten).</span><span class="sxs-lookup"><span data-stu-id="d6936-119">In Lync Server, you can configure voice policies with the following scope levels (listed from the most specific to the most general).</span></span>

  - <span data-ttu-id="d6936-p103">Die **VoIP-Benutzerrichtlinie** kann einzelnen Benutzern, Gruppen oder Kontaktobjekten zugewiesen werden. Dies ist die niedrigste Richtlinienebene. VoIP-Benutzerrichtlinien können bereitgestellt werden, um Funktionen nur für bestimmte Benutzer oder Gruppen an einem Standort zu aktivieren. Sie können damit z. B. bei bestimmten Mitarbeitern Ferngespräche deaktivieren. Damit eine VoIP-Richtlinie zugewiesen werden kann, wird ein Kontaktobjekt wie ein Einzelbenutzer behandelt.</span><span class="sxs-lookup"><span data-stu-id="d6936-p103">**User voice policy** can be assigned to individual users, groups, or contact objects. This is the lowest level policy. User voice policies can be deployed to enable features for certain users or groups at a site, but not for others in the same site. For example, you may want to disable long distance dialing for some employees. For the purpose of assigning a voice policy, a contact object is treated as an individual user.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="d6936-125">Wir empfehlen, dass Sie eine Benutzer VoIP-Richtlinie für Branch Site Enterprise-VoIP-Benutzer bereitstellen, die bei der zentralen Website Bereitstellung registriert sind, oder für Benutzer, die auf einer Survivable Branch-Appliance registriert sind.</span><span class="sxs-lookup"><span data-stu-id="d6936-125">We recommend that you deploy a user voice policy for branch site Enterprise Voice users who are registered with the central site deployment, or users who are registered on a Survivable Branch Appliance.</span></span>

    
    </div>

  - <span data-ttu-id="d6936-p104">Eine **VoIP-Standortrichtlinie** gilt für einen gesamten Standort. Ausgenommen sind Benutzer, Gruppen oder Kontaktobjekte, denen eine Benutzerrichtlinie zugeordnet wurde. Zum Definieren einer VoIP-Standortrichtlinie müssen Sie den Standort angeben, für den die Richtlinie gelten soll. Wenn keine VoIP-Benutzerrichtlinie zugewiesen ist, wird die VoIP-Standortrichtlinie verwendet.</span><span class="sxs-lookup"><span data-stu-id="d6936-p104">**Site voice policy** applies to an entire site, except for any users, groups, or contact objects that are assigned a user voice policy. To define a site voice policy, you must specify the site to which the policy applies. If a user voice policy is not assigned, the site voice policy is used.</span></span>

  - <span data-ttu-id="d6936-129">Bei der **globalen VoIP-Richtlinie** handelt es sich um die Standard VoIP-Richtlinie, die mit dem Produkt installiert wird.</span><span class="sxs-lookup"><span data-stu-id="d6936-129">**Global voice policy** is the default voice policy that is installed with the product.</span></span> <span data-ttu-id="d6936-130">Sie können die globale VoIP-Richtlinie bearbeiten, um die spezifischen Anforderungen Ihrer Organisation zu erfüllen, Sie können Sie jedoch nicht umbenennen oder löschen.</span><span class="sxs-lookup"><span data-stu-id="d6936-130">You can edit the global voice policy to meet the specific needs of your organization, but you cannot rename or delete it.</span></span> <span data-ttu-id="d6936-131">Diese VoIP-Richtlinie gilt für alle Enterprise-VoIP-Benutzer, Gruppen und Kontaktobjekte in Ihrer Bereitstellung, es sei denn, Sie konfigurieren und weisen eine VoIP-Richtlinie mit einem spezifischeren Bereich zu.</span><span class="sxs-lookup"><span data-stu-id="d6936-131">This voice policy applies to all Enterprise Voice users, groups, and contact objects in your deployment unless you configure and assign a voice policy with more specific scope.</span></span> <span data-ttu-id="d6936-132">Wenn Sie diese Richtlinie vollständig deaktivieren möchten, stellen Sie sicher, dass allen Websites und Benutzern benutzerdefinierte Richtlinien zugewiesen sind.</span><span class="sxs-lookup"><span data-stu-id="d6936-132">If you want to disable this policy entirely, be sure that all sites and users have custom policies assigned to them.</span></span>

</div>

<div>

## <a name="call-features"></a><span data-ttu-id="d6936-133">Anruffunktionen</span><span class="sxs-lookup"><span data-stu-id="d6936-133">Call Features</span></span>

<span data-ttu-id="d6936-134">Für jede Richtlinie können Sie die folgenden Anruffunktionen aktivieren oder deaktivieren:</span><span class="sxs-lookup"><span data-stu-id="d6936-134">You can enable or disable the following call features for each voice policy:</span></span>

  - <span data-ttu-id="d6936-p106">**Anrufweiterleitung** ermöglicht Benutzern das Weiterleiten von Anrufen an andere Telefone und Clientgeräte. Diese Option ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d6936-p106">**Call forwarding** enables users to forward calls to other phones and client devices. Enabled by default.</span></span>

  - <span data-ttu-id="d6936-p107">**Delegierung** ermöglicht Benutzern die Angabe anderer Benutzer, die in ihrem Namen Anrufe tätigen und empfangen können. Diese Option ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d6936-p107">**Delegation** enables users to specify other users to send and receive calls on their behalf. Enabled by default.</span></span>

  - <span data-ttu-id="d6936-p108">**Anrufdurchstellung** ermöglicht Benutzern, Anrufe an andere Benutzer durchzustellen. Diese Option ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d6936-p108">**Call transfer** enables users to transfer calls to other users. Enabled by default.</span></span>

  - <span data-ttu-id="d6936-p109">**Anruf parken** ermöglicht Benutzern, Anrufe in der Warteschleife zu parken und mit einem anderen Telefon oder Clientgerät wiederaufzunehmen. Diese Option ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d6936-p109">**Call park** enables users to park calls and then pick up the call from a different phone or client. Disabled by default.</span></span>

  - <span data-ttu-id="d6936-p110">**Gleichzeitiges Klingeln** ermöglicht bei eingehenden Anrufen das gleichzeitige Läuten auf zusätzlichen Telefonen (z. B. einem Mobiltelefon) oder anderen Endpunktgeräten. Diese Option ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d6936-p110">**Simultaneous ringing** enables incoming calls to ring on an additional phone (for example, a mobile phone) or other endpoint devices. Enabled by default.</span></span>

  - <span data-ttu-id="d6936-p111">**Teamanruf** ermöglicht Benutzern in einem definierten Team die Annahme von Anrufen für andere Teammitglieder. Diese Option ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d6936-p111">**Team call** enables users on a defined team to answer calls for other members of the team. Enabled by default.</span></span>

  - <span data-ttu-id="d6936-p112">**PSTN-Umleitung** ermöglicht das Umleiten von Anrufen von Benutzern, denen diese Richtlinie zugewiesen wurde, an andere Benutzer im Unternehmen über das Festnetz, wenn das WAN überlastet oder nicht verfügbar ist. Diese Option ist standardmäßig aktiviert.</span><span class="sxs-lookup"><span data-stu-id="d6936-p112">**PSTN reroute** enables calls made by users who are assigned this policy to other enterprise users to be rerouted on the public switched telephone network (PSTN) if the WAN is congested or unavailable. Enabled by default.</span></span>

  - <span data-ttu-id="d6936-p113">**Außerkraftsetzung der Bandbreitenrichtlinie** ermöglicht Administratoren, Richtlinienentscheidungen im Rahmen der Anrufsteuerung für einen bestimmten Benutzer außer Kraft zu setzen. Diese Option ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d6936-p113">**Bandwidth policy override** enables administrators to override call admission control policy decisions for a particular user. Disabled by default.</span></span>

  - <span data-ttu-id="d6936-151">Durch eine **böswillige Anrufprotokollierung** können Benutzer böswillige Anrufe über den lync-Client melden und diese dann in den Anruf Detaildatensätzen kennzeichnen.</span><span class="sxs-lookup"><span data-stu-id="d6936-151">**Malicious call tracing** enables users to report malicious calls by using the Lync client, and then flags such calls in the call detail records.</span></span> <span data-ttu-id="d6936-152">Diese Option ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d6936-152">Disabled by default.</span></span>

  - <span data-ttu-id="d6936-153">**Voicemail-Ausweg** verhindert, dass Anrufe sofort an das Voicemail-System des Mobiltelefons des Benutzers weitergeleitet werden, wenn gleichzeitiges Klingeln konfiguriert und das Telefon abgeschaltet, ohne Strom oder außer Reichweite ist und auf einem Timer-Wert basiert.</span><span class="sxs-lookup"><span data-stu-id="d6936-153">**Voicemail escape** prevents calls from being immediately routed to the user’s mobile phone voicemail system when simultaneous ringing is configured and the phone is turned off, out of battery, or out of range, and is based on a timer value.</span></span> <span data-ttu-id="d6936-154">Mit dieser Einstellung wird der Timer aktiviert und deaktiviert sowie der Wert des Timers eingestellt.</span><span class="sxs-lookup"><span data-stu-id="d6936-154">This setting enables and disables the timer and sets the value of the timer.</span></span> <span data-ttu-id="d6936-155">Sie kann nur mithilfe der lync Server-Verwaltungsshell konfiguriert werden.</span><span class="sxs-lookup"><span data-stu-id="d6936-155">It can be configured only by using the Lync Server Management Shell.</span></span> <span data-ttu-id="d6936-156">Diese ist standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="d6936-156">Disabled by default.</span></span>

  - <span data-ttu-id="d6936-157">**Anrufweiterleitung und gleichzeitiges anrufen PSTN-Nutzungen** können Administratoren die gleiche PSTN-Verwendung wie die VoIP-Richtlinie für die Anrufweiterleitung und gleichzeitiges Klingeln angeben, die Anrufweiterleitung und das gleichzeitige Klingeln nur für interne lync-Benutzer einschränken oder eine benutzerdefinierte PSTN-Nutzung angeben, die sich von der PSTN-Nutzung der VoIP-Richtlinie unterscheidet.</span><span class="sxs-lookup"><span data-stu-id="d6936-157">**Call forwarding and simultaneous ringing PSTN usages** enables administrators to specify the same PSTN usage as the voice policy for call forwarding and simultaneous ringing, restrict call forwarding and simultaneous ringing to internal Lync users only, or specify a custom PSTN usage that is different from the voice policy’s PSTN usage.</span></span> <span data-ttu-id="d6936-158">Standardmäßig wird für Anrufweiterleitung und gleichzeitiges Klingeln die gleiche PSTN-Verwendung verwendet wie bei der VoIP-Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="d6936-158">The default is to use the same PSTN usage as the voice policy for call forwarding and simultaneous ringing.</span></span>

</div>

<div>

## <a name="pstn-usage-records"></a><span data-ttu-id="d6936-159">PSTN-Verwendungseinträge</span><span class="sxs-lookup"><span data-stu-id="d6936-159">PSTN Usage Records</span></span>

<span data-ttu-id="d6936-160">Jeder VoIP-Richtlinie muss mindestens ein PSTN-Verwendungseintrag zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="d6936-160">Each voice policy should have one or more associated PSTN usage records.</span></span> <span data-ttu-id="d6936-161">PSTN-Verwendungen können nur zum Zweck von Anrufweiterleitung und gleichzeitigem Klingeln einer VoIP-Richtlinie zugeordnet sein.</span><span class="sxs-lookup"><span data-stu-id="d6936-161">PSTN usages can be associated with a voice policy for the purpose of simultaneous ringing and call forwarding only.</span></span> <span data-ttu-id="d6936-162">Details zum Planen von PSTN-Verwendungsdatensätzen finden Sie unter [PSTN-Verwendungsdaten Sätze in lync Server 2013](lync-server-2013-pstn-usage-records.md).</span><span class="sxs-lookup"><span data-stu-id="d6936-162">For details about planning PSTN usage records, see [PSTN usage records in Lync Server 2013](lync-server-2013-pstn-usage-records.md).</span></span>

<div>


> [!NOTE]  
> <span data-ttu-id="d6936-p118">Die Reihenfolge der PSTN-Verwendungseinträge ist wichtig, da die Ausgangsroutingfunktion beim Zuordnen von Benutzern zu Routen die PSTN-Verwendungseinträge von oben nach unten vergleicht. Wenn der erste Eintrag mit der Anrufroute übereinstimmt, wird diese Route verwendet. Falls nicht, unterstützt die Ausgangsroutingfunktion den nächsten PSTN-Verwendungseintrag in der Liste und fährt damit fort, bis eine Übereinstimmung gefunden wird. Die nachfolgenden PSTN-Verwendungseinträge dienen zur zusätzlichen Absicherung, wenn der erste Datensatz in der Liste nicht verfügbar ist.</span><span class="sxs-lookup"><span data-stu-id="d6936-p118">PSTN usage order is critical because in matching users to routes, the outbound routing functionality compares PSTN usages from top to bottom. If the first usage matches the call route, that route is used. If not, the outbound routing functionality looks at the next PSTN usage on the list and continues until a match is found. In effect, the subsequent PSTN usages provide backup if the first one on the list is unavailable.</span></span>



<span data-ttu-id="d6936-167"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d6936-167"></div>

</div>

</div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

