---
title: 'Lync Server 2013: Verwalten von Richtlinien für den externen Zugriff für Ihre Organisation'
description: 'Lync Server 2013: Verwalten der Richtlinien für den externen Zugriff für Ihre Organisation.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Manage external access policy for your organization
ms:assetid: 5571811e-34c8-443a-b94c-1ab5d4275581
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520995(v=OCS.15)
ms:contentKeyID: 48184160
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8f0bb0e6764f67403065187c62debef13c77fcc3
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49426109"
---
# <a name="manage-external-access-policy-in-lync-server-2013"></a><span data-ttu-id="cb7e7-103">Verwalten von Richtlinien für den externen Zugriff für Ihre Organisation in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cb7e7-103">Manage external access policy in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="cb7e7-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="cb7e7-104">

<span> </span></span></span>

<span data-ttu-id="cb7e7-105">_**Letztes Änderungsdatum des Themas:** 2013-10-07_</span><span class="sxs-lookup"><span data-stu-id="cb7e7-105">_**Topic Last Modified:** 2013-10-07_</span></span>

<span data-ttu-id="cb7e7-106">Nachdem Sie einen oder mehrere Edge-Server bereitgestellt haben, müssen Sie die Typen des externen Zugriffs aktivieren, die für Ihre Organisation unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-106">After deploying one or more Edge Servers, you must enable the types of external access that will be supported for your organization.</span></span>

<span data-ttu-id="cb7e7-107">Standardmäßig sind keine Richtlinien zur Unterstützung des Zugriffs externer Benutzer, einschließlich des Remotebenutzerzugriffs, des Zugriffs auf den Verbundbenutzer konfiguriert, auch wenn Sie die Unterstützung für den externen Benutzer Zugriff für Ihre Organisation bereits aktiviert haben.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-107">By default, there are no policies configured to support external user access, including remote user access, federated user access, even if you have already enabled external user access support for your organization.</span></span> <span data-ttu-id="cb7e7-108">Um die Verwendung des Zugriffs auf externe Benutzer zu steuern, müssen Sie eine oder mehrere Richtlinien konfigurieren und den Typ des für jede Richtlinie unterstützten externen Benutzerzugriffs angeben.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-108">To control the use of external user access, you must configure one or more policies, specifying the type of external user access supported for each policy.</span></span> <span data-ttu-id="cb7e7-109">Die folgenden Richtlinienbereiche stehen für die Erstellung und Konfiguration zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-109">The following policy scopes are available for creation and configuration.</span></span> <span data-ttu-id="cb7e7-110">Standardmäßig wird die globale Richtlinie erstellt, kann aber nicht gelöscht werden.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-110">By default, the Global policy is created, but cannot be deleted.</span></span>

  - <span data-ttu-id="cb7e7-111">**Globale Richtlinie**   Die globale Richtlinie wird erstellt, wenn Sie Ihre Edgeserver bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-111">**Global policy**   The global policy is created when you deploy your Edge Servers.</span></span> <span data-ttu-id="cb7e7-112">Standardmäßig sind keine Optionen für den externen Benutzer Zugriff in der globalen Richtlinie aktiviert.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-112">By default, no external user access options are enabled in the global policy.</span></span> <span data-ttu-id="cb7e7-113">Zur Unterstützung des Zugriffs externer Benutzer auf globaler Ebene konfigurieren Sie die globale Richtlinie so, dass eine oder mehrere Arten von Zugriffsoptionen für externe Benutzer unterstützt werden.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-113">To support external user access at the global level, you configure the global policy to support one or more types of external user access options.</span></span> <span data-ttu-id="cb7e7-114">Die globale Richtlinie gilt für alle Benutzer in Ihrer Organisation, aber Website Richtlinien und Benutzerrichtlinien überschreiben die globale Richtlinie.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-114">The global policy applies to all users in your organization, but site policies and user policies override the global policy.</span></span> <span data-ttu-id="cb7e7-115">Wenn Sie die globale Richtlinie löschen, werden Sie nicht entfernt.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-115">If you delete the global policy, you do not remove it.</span></span> <span data-ttu-id="cb7e7-116">Stattdessen setzen Sie Sie auf die Standardeinstellung zurück.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-116">Instead, you reset it to the default setting.</span></span>

  - <span data-ttu-id="cb7e7-117">**Website Richtlinie**   Sie können eine oder mehrere Website Richtlinien erstellen und konfigurieren, um die Unterstützung für den Zugriff externer Benutzer auf bestimmte Websites zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-117">**Site policy**   You can create and configure one or more site policies to limit support for external user access to specific sites.</span></span> <span data-ttu-id="cb7e7-118">Die Konfiguration in der Standortrichtlinie setzt die globale Richtlinie außer Kraft, jedoch nur für den durch die Standortrichtlinie abgedeckten Standort.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-118">The configuration in the site policy overrides the global policy, but only for the specific site covered by the site policy.</span></span> <span data-ttu-id="cb7e7-119">Wenn Sie beispielsweise den Remotebenutzerzugriff in der globalen Richtlinie aktivieren, geben Sie möglicherweise eine Website Richtlinie an, die den Remotebenutzerzugriff für eine bestimmte Website deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-119">For example, if you enable remote user access in the global policy, you might specify a site policy that disables remote user access for a specific site.</span></span> <span data-ttu-id="cb7e7-120">Standardmäßig wird eine Website Richtlinie auf alle Benutzer dieser Website angewendet, aber Sie können einem Benutzer eine Benutzerrichtlinie zuweisen, um die Website Richtlinieneinstellung zu überschreiben.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-120">By default, a site policy is applied to all users of that site, but you can assign a user policy to a user to override the site policy setting.</span></span>

  - <span data-ttu-id="cb7e7-121">**Benutzerrichtlinien**   Sie können eine oder mehrere Benutzerrichtlinien erstellen und konfigurieren, um die Unterstützung für den Zugriff durch Remotebenutzer auf bestimmte Benutzer zu begrenzen.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-121">**User policy**   You can create and configure one or more user policies to limit support for remote user access to specific users.</span></span> <span data-ttu-id="cb7e7-122">Die Konfiguration in der Benutzerrichtlinie überschreibt die globale und die Website Richtlinie, jedoch nur für bestimmte Benutzer, denen die Benutzerrichtlinie zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-122">The configuration in the user policy overrides the global and site policy, but only for the specific users to whom the user policy is assigned.</span></span> <span data-ttu-id="cb7e7-123">Wenn Sie beispielsweise den Remotebenutzerzugriff in der globalen Richtlinie und der Website Richtlinie aktivieren, geben Sie möglicherweise eine Benutzerrichtlinie an, die den Zugriff durch Remotebenutzer deaktiviert und diese Benutzerrichtlinie dann bestimmten Benutzern zuweist.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-123">For example, if you enable remote user access in the global policy and site policy, you might specify a user policy that disables remote user access and then assign that user policy to specific users.</span></span> <span data-ttu-id="cb7e7-124">Wenn Sie eine Benutzerrichtlinie erstellen, müssen Sie Sie auf einen oder mehrere Benutzer anwenden, bevor Sie wirksam wird.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-124">If you create a user policy, you must apply it to one or more users before it takes effect.</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="cb7e7-125">Lync Server-Richtlinieneinstellungen, die auf einer Richtlinienebene angewendet werden, können Einstellungen außer Kraft setzen, die auf einer anderen Richtlinienebene angewendet werden.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-125">Lync Server policy settings that are applied at one policy level can override settings that are applied at another policy level.</span></span> <span data-ttu-id="cb7e7-126">Die Priorität der lync Server-Richtlinie lautet: Benutzerrichtlinien (der meiste Einfluss) überschreibt eine Website Richtlinie, und eine Website Richtlinie überschreibt eine globale Richtlinie (geringster Einfluss).</span><span class="sxs-lookup"><span data-stu-id="cb7e7-126">Lync Server policy precedence is: User policy (most influence) overrides a Site policy, and then a Site policy overrides a Global policy (least influence).</span></span> <span data-ttu-id="cb7e7-127">Mit anderen Worten: Je geringer der Abstand zwischen Richtlinieneinstellung und betroffenem Objekt, desto stärker der Einfluss auf das Objekt.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-127">This means that the closer the policy setting is to the object that the policy is affecting, the more influence it has on the object.</span></span>



</div>

<span data-ttu-id="cb7e7-128">Zu diesen Optionen gehören die folgenden Typen von externem Zugriff:</span><span class="sxs-lookup"><span data-stu-id="cb7e7-128">These options include the following types of external access:</span></span>

  - <span data-ttu-id="cb7e7-129">**Aktivieren der Kommunikation mit Verbundbenutzern**   Aktivieren Sie diese Option, wenn Sie den Benutzer Zugriff auf Partnerdomänen für Föderationen unterstützen möchten.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-129">**Enable communications with federated users**   Enable this if you want to support user access to federated partner domains.</span></span> <span data-ttu-id="cb7e7-130">Diese Einstellung konfiguriert die Möglichkeit für Benutzer, mit anderen SIP-Verbunddomänen sowie gehosteten Anbietern wie Microsoft 365 zu kommunizieren.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-130">This setting configures the ability for users to communicate with other SIP federated domains, as well as Hosted providers like Microsoft 365.</span></span> <span data-ttu-id="cb7e7-131">Wenn Sie diese Einstellung auswählen, können Sie die Option zum Zulassen der Kommunikation mit XMPP-Verbunddomänen auswählen.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-131">Selecting this setting allows you to select the option to allow communication with XMPP federated domains.</span></span>
    
    <span data-ttu-id="cb7e7-132">Optional können Sie die Option **Kommunikation mit XMPP-Verbundpartnern aktivieren** auswählen, wenn Sie zuerst **Kommunikation mit Verbundbenutzern aktivieren** auswählen.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-132">As an option, you can select **Enable communications with XMPP federated partners** if you first select **Enable communications with federated users**.</span></span> <span data-ttu-id="cb7e7-133">Die XMPP-Föderation ist eine Föderation mit Organisationen, die das Extensible Messaging and Presence Protocol (XMPP) verwenden.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-133">XMPP federation is a federation with organizations that use extensible messaging and presence protocol (XMPP).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="cb7e7-134">Wenn Sie die XMPP-Föderation aktivieren, müssen Sie auch den <STRONG>XMPP-Verbund</STRONG> im Bereich "Edge-Pools-Konfiguration" des Topologie-Generators bereitstellen.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-134">If you enable XMPP federation, you must also select to deploy <STRONG>XMPP federation</STRONG> in the Edge pools configuration section of Topology Builder.</span></span> <span data-ttu-id="cb7e7-135">Bei der Konfiguration für XMPP Federation wird ein XMPP-Proxy auf dem Edgeserver und ein XMPP-Gateway auf dem Front-End-Server bereitgestellt.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-135">Configuring for XMPP federation deploys an XMPP Proxy on the Edge Server and an XMPP gateway on the Front End Server.</span></span>

    
    </div>

  - <span data-ttu-id="cb7e7-136">**Aktivieren der Kommunikation mit Remotebenutzern**   Aktivieren Sie diese Option, wenn Sie möchten, dass Benutzer in Ihrer Organisation, die sich außerhalb Ihrer Firewall befinden, wie Telecommuter und Benutzer, die unterwegs sind, eine Verbindung mit lync Server über das Internet herstellen können.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-136">**Enable communications with remote users**   Enable this option if you want users in your organization who are outside your firewall, such as telecommuters and users who are traveling, to be able to connect to Lync Server over the Internet.</span></span>

  - <span data-ttu-id="cb7e7-137">**Aktivieren der Kommunikation mit öffentlichen Benutzern**   Aktivieren Sie diese Option, wenn interne Benutzer in der Lage sein sollen, mit Kontakten des öffentlichen Chat-Anbieters zu kommunizieren, wie Sie von Windows Live, Yahoo \! und America Online (AOL) bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-137">**Enable communications with public users**   Enable this option if you want internal users to be able to communicate with public IM provider contacts, such as those provided by Windows Live, Yahoo\!, and America Online (AOL).</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <UL>
    > <LI>
    > <P><span data-ttu-id="cb7e7-138">Ab dem 1. September, 2012, ist die Microsoft lync Public im Connectivity-Benutzerabonnementlizenz ("PIC USL") nicht mehr für den Kauf von neuen oder erneuernden Vereinbarungen verfügbar.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-138">As of September 1st, 2012, the Microsoft Lync Public IM Connectivity User Subscription License (“PIC USL”) is no longer available for purchase for new or renewing agreements.</span></span> <span data-ttu-id="cb7e7-139">Kunden mit aktiven Lizenzen sind in der Lage, weiterhin mit Yahoo! zu verbünden</span><span class="sxs-lookup"><span data-stu-id="cb7e7-139">Customers with active licenses will be able to continue to federate with Yahoo!</span></span> <span data-ttu-id="cb7e7-140">Messenger, bis der Dienst das Datum beendet hat.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-140">Messenger until the service shut down date.</span></span> <span data-ttu-id="cb7e7-141">Datum des Endes des Lebenszyklus von Juni 2014 für AOL und Yahoo!</span><span class="sxs-lookup"><span data-stu-id="cb7e7-141">An end of life date of June 2014 for AOL and Yahoo!</span></span> <span data-ttu-id="cb7e7-142">wurde angekündigt.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-142">has been announced.</span></span> <span data-ttu-id="cb7e7-143">Ausführliche Informationen finden Sie <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">unter Unterstützung für öffentliche Instant Messenger-Konnektivität in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-143">For details, see <A href="lync-server-2013-support-for-public-instant-messenger-connectivity.md">Support for public instant messenger connectivity in Lync Server 2013</A>.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="cb7e7-144">Bei der PIC-USL handelt es sich um eine Abonnementlizenz pro Benutzer pro Monat, die für die Föderation von lync Server oder Office Communications Server mit Yahoo! erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-144">The PIC USL is a per-user per-month subscription license that is required for Lync Server or Office Communications Server to federate with Yahoo!</span></span> <span data-ttu-id="cb7e7-145">Messenger.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-145">Messenger.</span></span> <span data-ttu-id="cb7e7-146">Die Möglichkeit von Microsoft, diesen Dienst bereitzustellen, war von der Unterstützung durch Yahoo! abhängig, deren zugrunde liegende Vereinbarung abgewickelt wird.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-146">Microsoft’s ability to provide this service has been contingent upon support from Yahoo!, the underlying agreement for which is winding down.</span></span></P>
    > <LI>
    > <P><span data-ttu-id="cb7e7-147">Lync ist mehr denn je ein leistungsfähiges Tool für die Verbindung zwischen Organisationen und Personen in der ganzen Welt.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-147">More than ever, Lync is a powerful tool for connecting across organizations and with individuals around the world.</span></span> <span data-ttu-id="cb7e7-148">Für den Verbund mit Windows Live Messenger sind keine zusätzlichen Benutzer-und Gerätelizenzen außerhalb der lync-Standard CAL erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-148">Federation with Windows Live Messenger requires no additional user/device licenses beyond the Lync Standard CAL.</span></span> <span data-ttu-id="cb7e7-149">Skype Federation wird dieser Liste hinzugefügt und ermöglicht es lync-Benutzern, Hunderte von Millionen von Personen mit Chat und Sprache zu erreichen.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-149">Skype federation will be added to this list, enabling Lync users to reach hundreds of millions of people with IM and voice.</span></span></P></LI></UL>

    
    </div>

<div>


> [!NOTE]  
> <span data-ttu-id="cb7e7-150">Neben der Unterstützung für den Zugriff durch externe Benutzer müssen Sie auch Richtlinien konfigurieren, um die Verwendung des Zugriffs externer Benutzer in Ihrer Organisation zu steuern, bevor Benutzer Zugriff auf externe Benutzer erhalten.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-150">In addition to enabling external user access support, you must also configure policies to control the use of external user access in your organization before any type of external user access is available to users.</span></span> <span data-ttu-id="cb7e7-151">Details zum Erstellen, konfigurieren und Anwenden von Richtlinien für den Zugriff durch externe Benutzer finden Sie unter <A href="lync-server-2013-enable-or-disable-remote-user-access.md">Aktivieren oder Deaktivieren des Remotebenutzerzugriffs in lync Server 2013</A>.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-151">For details about creating, configuring, and applying policies for external user access see <A href="lync-server-2013-enable-or-disable-remote-user-access.md">Enable or disable remote user access in Lync Server 2013</A>.</span></span>



</div>

<span data-ttu-id="cb7e7-152">**So zeigen Sie die Richtlinien für den externen Zugriff mithilfe von Windows PowerShell-Cmdlets an**</span><span class="sxs-lookup"><span data-stu-id="cb7e7-152">**To view external access policies by using Windows PowerShell cmdlets**</span></span>

  - <span data-ttu-id="cb7e7-153">Sie können die Richtlinien für den externen Zugriff mit der lync Server-Verwaltungsshell und dem Cmdlet **Get-CsExternalAccessPolicy** anzeigen.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-153">You can view external access policies by using Lync Server Management Shell and the **Get-CsExternalAccessPolicy** cmdlet.</span></span> <span data-ttu-id="cb7e7-154">Sie können dieses Cmdlet in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="cb7e7-154">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="cb7e7-155">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="cb7e7-155">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>
    
    <span data-ttu-id="cb7e7-156">Wenn Sie Informationen zu allen Ihren externen Zugriffsrichtlinien anzeigen möchten, geben Sie den folgenden Befehl in der lync Server-Verwaltungsshell ein, und drücken Sie dann die EINGABETASTE:</span><span class="sxs-lookup"><span data-stu-id="cb7e7-156">To view information about all your external access policies, type the following command in the Lync Server Management Shell and then press ENTER:</span></span>
    
        Get-CsExternalAccessPolicy
    
    <span data-ttu-id="cb7e7-157">Mit diesem Befehl werden Informationen ähnlich der folgenden zurückgegeben:</span><span class="sxs-lookup"><span data-stu-id="cb7e7-157">This command returns information similar to the following:</span></span>
    
        Identity                          : Global
        Description                       :
        EnableFederationAccess            : False
        EnableXmppAccess                  : False
        EnablePublicCloudAccess           : False
        EnablePublicCloudAudioVideoAccess : False
        EnableOutsideAccess               : False

<div>

## <a name="in-this-section"></a><span data-ttu-id="cb7e7-158">In diesem Abschnitt</span><span class="sxs-lookup"><span data-stu-id="cb7e7-158">In This Section</span></span>

  - [<span data-ttu-id="cb7e7-159">Konfigurieren von Richtlinien zur Steuerung des Partnerbenutzerzugriffs in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cb7e7-159">Configure policies to control federated user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-federated-user-access.md)

  - [<span data-ttu-id="cb7e7-160">Konfigurieren von Richtlinien zur Steuerung des Zugriffs durch XMPP-Partnerbenutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cb7e7-160">Configure policies to control XMPP federated user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-xmpp-federated-user-access.md)

  - [<span data-ttu-id="cb7e7-161">Konfigurieren von Richtlinien zur Steuerung des Zugriffs durch Remotebenutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cb7e7-161">Configure policies to control remote user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-remote-user-access.md)

  - [<span data-ttu-id="cb7e7-162">Konfigurieren von Richtlinien zur Steuerung des öffentlichen Benutzerzugriffs in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cb7e7-162">Configure policies to control public user access in Lync Server 2013</span></span>](lync-server-2013-configure-policies-to-control-public-user-access.md)

  - [<span data-ttu-id="cb7e7-163">Zuweisen einer Richtlinie für den Zugriff durch externe Benutzer zu einem für Lync aktivierten Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cb7e7-163">Assign an external user access policy to a Lync enabled user in Lync Server 2013</span></span>](lync-server-2013-assign-an-external-user-access-policy-to-a-lync-enabled-user.md)

  - [<span data-ttu-id="cb7e7-164">Zurücksetzen oder Löschen von Richtlinien für den Zugriff durch externe Benutzer in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="cb7e7-164">Resetting or deleting external user access policies in Lync Server 2013</span></span>](lync-server-2013-resetting-or-deleting-external-user-access-policies.md)

<span data-ttu-id="cb7e7-165"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="cb7e7-165"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

