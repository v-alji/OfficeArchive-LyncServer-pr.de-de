---
title: Identitäten, Bereiche und Mandanten in Skype for Business Online
description: Identitäten, Bereiche und Mandanten in Skype for Business Online.
ms.reviewer: ''
ms.author: serdars
author: serdarsoysal
f1.keywords:
- NOCSH
TOCTitle: Identities, scopes, and tenants
ms:assetid: 7cfa194a-2d01-4370-9b48-ee13ff597fa5
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Dn362819(v=OCS.15)
ms:contentKeyID: 56558817
ms.date: 05/04/2015
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 00ab84c3ca83dea2e328315ae7e616ad7830c227
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394966"
---
# <a name="identities-scopes-and-tenants-in-skype-for-business-online"></a><span data-ttu-id="830fe-103">Identitäten, Bereiche und Mandanten in Skype for Business Online</span><span class="sxs-lookup"><span data-stu-id="830fe-103">Identities, scopes, and tenants in Skype for Business Online</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="830fe-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="830fe-104">

<span> </span></span></span>

<span data-ttu-id="830fe-105">_**Letztes Änderungsdatum des Themas:** 2015-03-09_</span><span class="sxs-lookup"><span data-stu-id="830fe-105">_**Topic Last Modified:** 2015-03-09_</span></span>

<span data-ttu-id="830fe-106">Für viele der Windows PowerShell-Cmdlets, die für die Verwaltung von Skype for Business Online verwendet werden, müssen Sie sehr genau über das Element verfügen, das Sie verwalten möchten.</span><span class="sxs-lookup"><span data-stu-id="830fe-106">Many of the Windows PowerShell cmdlets used to manage Skype for Business Online require you to be very specific about the item that you are trying to manage.</span></span> <span data-ttu-id="830fe-107">Wenn Sie beispielsweise das Cmdlet " [Satz-CsUserAcp](https://docs.microsoft.com/powershell/module/skype/Set-CsUserAcp) " ausführen, müssen Sie angeben, welchen Benutzer Sie verwalten möchten.</span><span class="sxs-lookup"><span data-stu-id="830fe-107">For example, when you run the [Set-CsUserAcp](https://docs.microsoft.com/powershell/module/skype/Set-CsUserAcp) cmdlet, you must indicate which user you are trying to manage.</span></span> <span data-ttu-id="830fe-108">Das macht Sinn.</span><span class="sxs-lookup"><span data-stu-id="830fe-108">This makes sense.</span></span> <span data-ttu-id="830fe-109">Wenn Sie dem Cmdlet nicht ausdrücklich mitteilen, welches Benutzerkonto verwaltet werden soll, hat das Cmdlet " **Satz-CsUserAcp** " keine Ahnung, welche Audio-Konferenz Informationen des Benutzers geändert werden sollten.</span><span class="sxs-lookup"><span data-stu-id="830fe-109">Unless you specifically tell the cmdlet which user account to manage, the **Set-CsUserAcp** cmdlet has no idea which user’s audio conferencing information should be modified.</span></span> <span data-ttu-id="830fe-110">Aus diesem Grund müssen Sie jedes Mal, wenn Sie das Cmdlet " **Satz-CsUserAcp** " ausführen, den Parameter Identity und dann die Identität des zu ändernden Benutzerkontos einbeziehen:</span><span class="sxs-lookup"><span data-stu-id="830fe-110">For this reason, each time you run the **Set-CsUserAcp** cmdlet, you’ll need to include the Identity parameter, followed by the Identity of the user account to be modified:</span></span>

    Set-CsUserAcp -Identity "Ken Myer" -TollNumber "14255551298" -ParticipantPassCode 13761 -Domain "fabrikam.com" -Name "Fabrikam ACP"

<span data-ttu-id="830fe-111">Wenn der Ausdruck *Identity* immer auf die Identität eines Benutzerkontos Bezug genommen hat, gibt es nur wenige Ursachen für Verwirrung.</span><span class="sxs-lookup"><span data-stu-id="830fe-111">If the term *Identity* always referred to the Identity of a user account, there would be little cause for confusion.</span></span> <span data-ttu-id="830fe-112">Wenn Sie mit Personen (Benutzern, Kontakten usw.) zu tun haben, verweisen Identitäten auf die einzelnen Benutzer selbst.</span><span class="sxs-lookup"><span data-stu-id="830fe-112">When you are dealing with people (users, contacts, and so on), Identities refer to the individual users themselves.</span></span> <span data-ttu-id="830fe-113">Elemente, die keine Benutzerkonten sind, weisen aber auch Identitäten auf.</span><span class="sxs-lookup"><span data-stu-id="830fe-113">However, items other than user accounts also have Identities.</span></span> <span data-ttu-id="830fe-114">Wenn es sich um Komponenten des Skype for Business Online-Diensts (Richtlinien, Konfigurationseinstellungen usw.) handelt, bedeutet der Ausdruck Identität etwas anderes.</span><span class="sxs-lookup"><span data-stu-id="830fe-114">When you are dealing with components of the Skype for Business Online service—policies, configuration settings, and so on—the term Identity means something slightly different.</span></span> <span data-ttu-id="830fe-115">Sehen Sie sich beispielsweise diesen Befehl an:</span><span class="sxs-lookup"><span data-stu-id="830fe-115">For example, consider this command:</span></span>

    Get-CsMeetingConfiguration -Identity "global"

<span data-ttu-id="830fe-116">In diesem Fall bezieht sich die Identität "Global" auf den Bereich der Konfigurationseinstellungen für Besprechungen.</span><span class="sxs-lookup"><span data-stu-id="830fe-116">In this case, the Identity "global" refers to the scope of the meeting configuration settings.</span></span> <span data-ttu-id="830fe-117">*Scope* ist ein Ausdruck, der in Skype for Business Online (und in lync Server) verwendet wird, um die Bereiche der Verwaltung festzulegen.</span><span class="sxs-lookup"><span data-stu-id="830fe-117">*Scope* is a term used in Skype for Business Online (and in Lync Server) to designate spheres of management.</span></span> <span data-ttu-id="830fe-118">Standardmäßig verfügen Richtlinien und Einstellungen immer über einen globalen Bereich.</span><span class="sxs-lookup"><span data-stu-id="830fe-118">By default, policies and settings always have a global scope.</span></span> <span data-ttu-id="830fe-119">Wenn Sie Ihr Skype for Business Online-Konto zum ersten Mal einrichten, verfügen Sie standardmäßig über eine Sammlung globaler Richtlinien und Einstellungen – globale Besprechungs Konfigurationseinstellungen, eine globale Richtlinie für den externen Zugriff, einen globalen Wählplan usw.</span><span class="sxs-lookup"><span data-stu-id="830fe-119">When you first set up your Skype for Business Online account you'll have, by default, a collection of global policies and settings—global meeting configuration settings, a global external access policy, a global dial plan, and so on.</span></span>

<span data-ttu-id="830fe-120">Diese globalen Richtlinien und Einstellungen wurden in Microsoft lync Server 2010 eingeführt, um sicherzustellen, dass alle Benutzer und alle Komponenten immer in irgendeiner Weise verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="830fe-120">These global policies and settings were introduced in Microsoft Lync Server 2010 to help ensure that all users and all components would always, in some way, be managed.</span></span> <span data-ttu-id="830fe-121">Dies war in Microsoft Office Communicator 2007 R2 nicht unbedingt der Fall.</span><span class="sxs-lookup"><span data-stu-id="830fe-121">This was not necessarily true in Microsoft Office Communicator 2007 R2.</span></span> <span data-ttu-id="830fe-122">Je nachdem, wie Sie auf das System zugegriffen haben, könnten Sie möglicherweise in einem weitgehend unverwalteten Zustand enden (in der Regel, weil Gruppenrichtlinien nicht auf Ihr Benutzerkonto angewendet werden konnten).</span><span class="sxs-lookup"><span data-stu-id="830fe-122">Depending on how you accessed the system, you could potentially end up in a largely unmanaged state (typically, because Group Policy could not be applied to your user account).</span></span> <span data-ttu-id="830fe-123">Im Gegensatz dazu wird in lync Server und in Skype for Business Online nichts jemals unverwaltet gelassen.</span><span class="sxs-lookup"><span data-stu-id="830fe-123">In contrast, in Lync Server and in Skype for Business Online, nothing is ever left unmanaged.</span></span> <span data-ttu-id="830fe-124">Der Grund dafür ist, dass globale Richtlinien und Einstellungen immer erzwungen werden, anstatt irgendetwas anderes zu tun.</span><span class="sxs-lookup"><span data-stu-id="830fe-124">This is because, in lieu of anything else, global policies and settings will always be enforced.</span></span>

<span data-ttu-id="830fe-125">Was meinen wir mit "anstelle von irgendetwas anderem"?</span><span class="sxs-lookup"><span data-stu-id="830fe-125">What do we mean by "in lieu of anything else"?</span></span> <span data-ttu-id="830fe-126">Nun, im Fall von Skype for Business Online ist es möglich, Richtlinien im *Bereich "Tag*" oder "Bereich der Verwaltung" zu erstellen.</span><span class="sxs-lookup"><span data-stu-id="830fe-126">Well, in the case of Skype for Business Online, it’s possible to create policies at the *tag scope*, or sphere of management.</span></span> <span data-ttu-id="830fe-127">Richtlinien, die mit dem Tag-Bereich (auch als benutzerspezifischer *Bereich* bezeichnet) erstellt wurden, haben Vorrang vor im globalen Bereich erstellten Richtlinien.</span><span class="sxs-lookup"><span data-stu-id="830fe-127">Policies created at the tag scope (also known as *the per-user scope*) take priority over policies created at the global scope.</span></span> <span data-ttu-id="830fe-128">Anders ausgedrückt: eine benutzerspezifische Richtlinie hat immer Vorrang vor einer globalen Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="830fe-128">In other words, a per-user policy will always take precedence over a global policy.</span></span> <span data-ttu-id="830fe-129">So können Sie beispielsweise zwei Richtlinien für den externen Benutzer Zugriff haben.</span><span class="sxs-lookup"><span data-stu-id="830fe-129">For example, you might have two external user access policies.</span></span> <span data-ttu-id="830fe-130">Die globale Richtlinie verbietet Benutzern, mit Personen zu kommunizieren, die über Konten für öffentliche Instant Messaging-Anbieter (im) wie Windows Live verfügen.</span><span class="sxs-lookup"><span data-stu-id="830fe-130">The global policy prohibits users from communicating with people who have accounts on public instant messaging (IM) providers, such as Windows Live.</span></span> <span data-ttu-id="830fe-131">Die benutzerspezifische Richtlinie AllowPublicIMCommunication ermöglicht die Kommunikation mit öffentlichen Chat Anbietern.</span><span class="sxs-lookup"><span data-stu-id="830fe-131">The per-user policy, AllowPublicIMCommunication, allows communication with public IM providers.</span></span>

<span data-ttu-id="830fe-132">Sie haben möglicherweise auch zwei Benutzer: Ken Myers und Pilar Ackerman.</span><span class="sxs-lookup"><span data-stu-id="830fe-132">You might also have two users: Ken Myer and Pilar Ackerman.</span></span> <span data-ttu-id="830fe-133">Ken Myers wurde die Richtlinie pro Benutzer zugewiesen.</span><span class="sxs-lookup"><span data-stu-id="830fe-133">Ken Myer has been assigned the per-user policy.</span></span> <span data-ttu-id="830fe-134">Pilar Ackerman wurde keine Richtlinie pro Benutzer zugewiesen; Das heißt, dass Sie von der globalen Richtlinie für den externen Zugriff verwaltet wird.</span><span class="sxs-lookup"><span data-stu-id="830fe-134">Pilar Ackerman has not been assigned a per-user policy; that is, she is managed by the global external access policy.</span></span> <span data-ttu-id="830fe-135">Die folgende Tabelle zeigt, welche Benutzer (falls vorhanden) mit öffentlichen Chat Anbietern kommunizieren können:</span><span class="sxs-lookup"><span data-stu-id="830fe-135">The following table shows which user (if any) can communicate with public IM providers:</span></span>


<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><span data-ttu-id="830fe-136">Richtlinieneinstellungen</span><span class="sxs-lookup"><span data-stu-id="830fe-136">Policy Settings</span></span></th>
<th><span data-ttu-id="830fe-137">Ken Myer</span><span class="sxs-lookup"><span data-stu-id="830fe-137">Ken Myer</span></span></th>
<th><span data-ttu-id="830fe-138">Pilar Ackerman</span><span class="sxs-lookup"><span data-stu-id="830fe-138">Pilar Ackerman</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><span data-ttu-id="830fe-139">Globale Richtlinieneinstellung für öffentliche Chat Anbieter</span><span class="sxs-lookup"><span data-stu-id="830fe-139">Global policy setting for public IM providers</span></span></p></td>
<td><p><span data-ttu-id="830fe-140">Nein</span><span class="sxs-lookup"><span data-stu-id="830fe-140">No</span></span></p></td>
<td><p><span data-ttu-id="830fe-141">Nein</span><span class="sxs-lookup"><span data-stu-id="830fe-141">No</span></span></p></td>
</tr>
<tr class="even">
<td><p><span data-ttu-id="830fe-142">Benutzerspezifische Richtlinieneinstellung für öffentliche Chat Anbieter</span><span class="sxs-lookup"><span data-stu-id="830fe-142">Per-user policy setting for public IM providers</span></span></p></td>
<td><p><span data-ttu-id="830fe-143">Ja</span><span class="sxs-lookup"><span data-stu-id="830fe-143">Yes</span></span></p></td>
<td><p><span data-ttu-id="830fe-144">Nein</span><span class="sxs-lookup"><span data-stu-id="830fe-144">No</span></span></p></td>
</tr>
<tr class="odd">
<td><p><span data-ttu-id="830fe-145">Der Benutzer kann mit öffentlichen Chat Anbietern kommunizieren</span><span class="sxs-lookup"><span data-stu-id="830fe-145">User can communicate with public IM providers</span></span></p></td>
<td><p><span data-ttu-id="830fe-146">Ja</span><span class="sxs-lookup"><span data-stu-id="830fe-146">Yes</span></span></p></td>
<td><p><span data-ttu-id="830fe-147">Nein</span><span class="sxs-lookup"><span data-stu-id="830fe-147">No</span></span></p></td>
</tr>
</tbody>
</table>


<span data-ttu-id="830fe-148">Wie Sie sehen können, ist es Ken Myers gestattet, mit öffentlichen Chat Dienstanbietern zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="830fe-148">As you can see, Ken Myer is allowed to communicate with public IM providers.</span></span> <span data-ttu-id="830fe-149">Der Grund hierfür ist, dass die Einstellungen in der ihm zugewiesenen Benutzerrichtlinie die Einstellungen in der globalen Richtlinie außer Kraft setzen.</span><span class="sxs-lookup"><span data-stu-id="830fe-149">This is because the settings in the per-user policy assigned to him override the settings in the global policy.</span></span> <span data-ttu-id="830fe-150">Pilar Ackerman kann nicht mit öffentlichen Chat Anbietern kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="830fe-150">Pilar Ackerman cannot communicate with public IM providers.</span></span> <span data-ttu-id="830fe-151">Dies liegt daran, dass Sie von der globalen Richtlinie verwaltet wird und die globale Richtlinie diese Kommunikation untersagt.</span><span class="sxs-lookup"><span data-stu-id="830fe-151">This is because she is managed by the global policy, and the global policy prohibits such communications.</span></span>

<span data-ttu-id="830fe-152">Richtlinien für einzelne Benutzer müssen vom Microsoft-Support für Sie erstellt werden.</span><span class="sxs-lookup"><span data-stu-id="830fe-152">Per-user policies must be created for you by Microsoft Support.</span></span> <span data-ttu-id="830fe-153">Nachdem die Richtlinien erstellt wurden, können Sie Sie den Benutzern mithilfe des entsprechenden **Grant-CS-** Cmdlets zuweisen (beispielsweise [Grant-CsExternalAccessPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsExternalAccessPolicy)).</span><span class="sxs-lookup"><span data-stu-id="830fe-153">After the policies are created, you can then assign them to users by using the appropriate **Grant-Cs** cmdlet (for example, [Grant-CsExternalAccessPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsExternalAccessPolicy)).</span></span> <span data-ttu-id="830fe-154">Richtlinien für einzelne Benutzer sind einfach zu erkennen, da die Richtlinien Identität immer mit dem **Tagpräfix beginnt.**</span><span class="sxs-lookup"><span data-stu-id="830fe-154">Per-user policies are easy to identify because the policy Identity always begins with the tag **prefix**.</span></span> <span data-ttu-id="830fe-155">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="830fe-155">For example:</span></span>

    Identity : tag:AllowPublicIMCommunication

<div>


> [!NOTE]  
> <span data-ttu-id="830fe-156">Das Tagpräfix <STRONG>geht auf</STRONG> die frühen Entwicklungstage von lync Server 2010 zurück.</span><span class="sxs-lookup"><span data-stu-id="830fe-156">The tag <STRONG>prefix</STRONG> dates back to the early development days of Lync Server 2010.</span></span> <span data-ttu-id="830fe-157">In diesen Tagen wurden Richtlinien für einzelne Benutzer als <EM>Transponder Richtlinien</EM> bezeichnet und durch <STRONG>das Tagpräfix identifiziert.</STRONG></span><span class="sxs-lookup"><span data-stu-id="830fe-157">In those days, per-user policies were referred to as <EM>tag policies</EM> and were identified by the tag <STRONG>prefix</STRONG>.</span></span> <span data-ttu-id="830fe-158">Diese Richtlinien werden jetzt genauer als benutzerspezifische <EM>Richtlinien</EM>bezeichnet, und der Transponder Bereich wird genauer als benutzerspezifischer <EM>Bereich</EM>bezeichnet.</span><span class="sxs-lookup"><span data-stu-id="830fe-158">These policies are now more accurately referred to as <EM>per-user policies</EM>, and the tag scope is more accurately referred to as the <EM>per-user scope</EM>.</span></span> <span data-ttu-id="830fe-159">Aus technischen <STRONG>Gründen wurde das Tagpräfix jedoch</STRONG> nie geändert.</span><span class="sxs-lookup"><span data-stu-id="830fe-159">However, for technical reasons, the tag <STRONG>prefix</STRONG> was never changed.</span></span>



</div>

<span data-ttu-id="830fe-160">Ein weiterer wichtiger Ausdruck, der bei der Arbeit mit Skype for Business Online und Windows PowerShell verwendet wird, ist *Mandant*.</span><span class="sxs-lookup"><span data-stu-id="830fe-160">Another key term used when working with Skype for Business Online and Windows PowerShell is *tenant*.</span></span> <span data-ttu-id="830fe-161">Wenn Sie ein Skype for Business Online-Konto einrichten, wird Ihrer neuen Bereitstellung eine Mandanten-ID zugewiesen, bei der es sich um eine GUID (Globally Unique Identifier) handelt, die der folgenden ähnelt:</span><span class="sxs-lookup"><span data-stu-id="830fe-161">When you set up a Skype for Business Online account, your new deployment is assigned a tenant ID number, which is a globally unique identifier (GUID) similar to this:</span></span>

    bf19b7db-6960-41e5-a139-2aa373474354

<span data-ttu-id="830fe-162">Bei einigen der Skype for Business Online-Cmdlets müssen Sie die Mandanten-ID eingeben, wenn Sie das Cmdlet ausführen.</span><span class="sxs-lookup"><span data-stu-id="830fe-162">A few of the Skype for Business Online cmdlets require you to enter the tenant ID whenever you run the cmdlet.</span></span> <span data-ttu-id="830fe-163">Sie müssen die Mandanten-ID eingeben, selbst wenn Sie sich angemeldet haben und nur einen Mandanten haben.</span><span class="sxs-lookup"><span data-stu-id="830fe-163">You must enter the tenant ID even if you have logged on to, and only have, one tenant.</span></span> <span data-ttu-id="830fe-164">Glücklicherweise müssen Sie die Mandanten-ID nicht auswendig lernen.</span><span class="sxs-lookup"><span data-stu-id="830fe-164">Fortunately, you do not have to memorize the tenant ID.</span></span> <span data-ttu-id="830fe-165">Sie können Ihre Mandanten-ID jederzeit abrufen, indem Sie den folgenden Windows PowerShell-Befehl ausführen:</span><span class="sxs-lookup"><span data-stu-id="830fe-165">You can retrieve your tenant ID at any time by running the following Windows PowerShell command:</span></span>

    Get-CsTenant | Select-Object TenantId

<span data-ttu-id="830fe-166">Das Erkennen von Dingen wie dem Unterschied zwischen dem globalen Bereich und dem Bereich pro Benutzer (oder dem Tag-Bereich) ist natürlich nur die halbe Schlacht.</span><span class="sxs-lookup"><span data-stu-id="830fe-166">Of course, knowing things such as the difference between the global scope and the per-user scope (or the tag scope) is only half the battle.</span></span> <span data-ttu-id="830fe-167">Darüber hinaus ist es wichtig zu wissen, wann (oder sogar ob) Sie diese Bereiche verwenden können.</span><span class="sxs-lookup"><span data-stu-id="830fe-167">It’s also important to know when (or even if) you can use these scopes.</span></span> <span data-ttu-id="830fe-168">Das gleiche gilt für Identitäten und den Mandanten Parameter.</span><span class="sxs-lookup"><span data-stu-id="830fe-168">The same is true for Identities and the tenant parameter.</span></span> <span data-ttu-id="830fe-169">In den folgenden Themen wird beschrieben, wie die verschiedenen Skype for Business Online-Cmdlets Identitäten, Bereiche und den Mandanten Parameter verwenden:</span><span class="sxs-lookup"><span data-stu-id="830fe-169">The following topics describe how the different Skype for Business Online cmdlets use Identities, scopes, and the tenant parameter:</span></span>

  - [<span data-ttu-id="830fe-170">Cmdlets in Skype for Business Online, die nur den globalen Bereich verwenden</span><span class="sxs-lookup"><span data-stu-id="830fe-170">Cmdlets in Skype for Business Online that use only the global scope</span></span>](cmdlets-in-skype-for-business-online-that-use-only-the-global-scope.md)

  - [<span data-ttu-id="830fe-171">Cmdlets in Skype for Business Online, die den globalen Bereich und den Transponder Bereich verwenden</span><span class="sxs-lookup"><span data-stu-id="830fe-171">Cmdlets in Skype for Business Online that use the global scope and the tag scope</span></span>](cmdlets-in-skype-for-business-online-that-use-the-global-scope-and-the-tag-scope.md)

  - [<span data-ttu-id="830fe-172">Cmdlets in Skype for Business Online, die eine Benutzeridentität verwenden</span><span class="sxs-lookup"><span data-stu-id="830fe-172">Cmdlets in Skype for Business Online that use a user identity</span></span>](cmdlets-in-skype-for-business-online-that-use-a-user-identity.md)

  - [<span data-ttu-id="830fe-173">Cmdlets in Skype for Business Online, die eine Benutzeridentität und den Transponder Bereich verwenden</span><span class="sxs-lookup"><span data-stu-id="830fe-173">Cmdlets in Skype for Business Online that use a user identity and the tag scope</span></span>](cmdlets-in-skype-for-business-online-that-use-a-user-identity-and-the-tag-scope.md)

  - [<span data-ttu-id="830fe-174">Cmdlets in Skype for Business Online, die den Mandanten Parameter verwenden</span><span class="sxs-lookup"><span data-stu-id="830fe-174">Cmdlets in Skype for Business Online that use the Tenant parameter</span></span>](cmdlets-in-skype-for-business-online-that-use-the-tenant-parameter.md)

  - [<span data-ttu-id="830fe-175">Cmdlets in Skype for Business Online, die eine Konferenzanbieter Identität verwenden</span><span class="sxs-lookup"><span data-stu-id="830fe-175">Cmdlets in Skype for Business Online that use a conferencing provider identity</span></span>](cmdlets-in-skype-for-business-online-that-use-a-conferencing-provider-identity.md)

  - [<span data-ttu-id="830fe-176">Cmdlets in Skype for Business Online, die keinen Bereich oder keine Identität verwenden</span><span class="sxs-lookup"><span data-stu-id="830fe-176">Cmdlets in Skype for Business Online that do not use a scope or an identity</span></span>](cmdlets-in-skype-for-business-online-that-do-not-use-a-scope-or-an-identity.md)

<span data-ttu-id="830fe-177"></div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="830fe-177"></div>

<span> </span>

</div>

</div>

</span></span></div>

