---
title: 'Lync Server 2013: Definieren der Mobilitätsanforderungen'
description: 'Lync Server 2013: Definieren Ihrer Mobilitätsanforderungen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Defining your mobility requirements
ms:assetid: b7608335-cdeb-4aae-8e4b-d80c55f0d62b
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690039(v=OCS.15)
ms:contentKeyID: 48185226
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 4fbc1a443946f0c879397f41628cfe788b428ff6
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430896"
---
# <a name="defining-your-mobility-requirements-for-lync-server-2013"></a><span data-ttu-id="bf4fa-103">Definieren der Mobilitätsanforderungen für Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf4fa-103">Defining your mobility requirements for Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bf4fa-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bf4fa-104">

<span> </span></span></span>

<span data-ttu-id="bf4fa-105">_**Letztes Änderungsdatum des Themas:** 2013-02-14_</span><span class="sxs-lookup"><span data-stu-id="bf4fa-105">_**Topic Last Modified:** 2013-02-14_</span></span>

    Some information in this topic pertains to Cumulative Updates for Lync Server 2013: February 2013.

<span data-ttu-id="bf4fa-106">Während der Planungsphase für das lync Server 2013 Mobility-Feature treffen Sie bei der Verwendung von lync 2010 Mobile-und lync 2013-mobilen Clients Entscheidungen, die ihre Bereitstellungsschritte bestimmen.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-106">During the planning phase for the Lync Server 2013 mobility feature, when you are using Lync 2010 Mobile and Lync 2013 Mobile clients, you make decisions that determine your deployment steps.</span></span>

<span data-ttu-id="bf4fa-107">Hier sind die Entscheidungen, die Sie beachten müssen:</span><span class="sxs-lookup"><span data-stu-id="bf4fa-107">Here are the decisions that you must consider:</span></span>

  - <span data-ttu-id="bf4fa-108">**Möchten Sie die automatische Ermittlung für Mobile lync-Clients verwenden?**</span><span class="sxs-lookup"><span data-stu-id="bf4fa-108">**Do you want to use automatic discovery for Lync mobile clients?**</span></span>
    
    <span data-ttu-id="bf4fa-109">Wenn Sie die automatische Ermittlung unterstützen möchten, müssen Sie neue interne und externe DNS-Einträge (Domain Name System) erstellen, Zertifikate auf den Front-End-Servern, Directors und Reverse-Proxys Subjekt-Alternative Namen hinzufügen und die vorhandenen Veröffentlichungsregeln auf dem Reverse-Proxy ändern.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-109">If you want to support automatic discovery, you need to create new internal and external Domain Name System (DNS) records, add subject alternative names to certificates on the Front End Servers, Directors, and reverse proxy, and modify the existing publishing rules on the reverse proxy.</span></span> <span data-ttu-id="bf4fa-110">Ausführliche Informationen finden Sie unter [Technische Voraussetzungen für Mobilität in lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="bf4fa-110">For details, see [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span></span> <span data-ttu-id="bf4fa-111">Mit der automatischen Ermittlung können Benutzer die lync Server 2013-Webdienste automatisch von einer beliebigen Stelle innerhalb oder außerhalb des Unternehmensnetzwerks finden, ohne die URLs in die Einstellungen Ihres mobilen Geräts einzugeben.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-111">With automatic discovery, users can automatically locate Lync Server 2013 Web Services from anywhere inside or outside the corporate network, without entering URLs in their mobile device settings.</span></span>
    
    <span data-ttu-id="bf4fa-112">Wenn Sie anstelle der automatischen Ermittlung manuelle Einstellungen verwenden, müssen Mobile Benutzer die folgenden URLs manuell auf Ihren mobilen Geräten eingeben:</span><span class="sxs-lookup"><span data-stu-id="bf4fa-112">If you use manual settings instead of automatic discovery, mobile users need to manually enter the following URLs in their mobile devices:</span></span>
    
      - <span data-ttu-id="bf4fa-113"> https://- \<ExtPoolFQDN\> /autodiscover/autodiscoverservice.svc/root für externen Zugriff</span><span class="sxs-lookup"><span data-stu-id="bf4fa-113">https://\<ExtPoolFQDN\>/Autodiscover/autodiscoverservice.svc/Root for external access</span></span>
    
      - <span data-ttu-id="bf4fa-114"> https:// \<IntPoolFQDN\> /autodiscover/autodiscoverservice. svc/root für internen Zugriff</span><span class="sxs-lookup"><span data-stu-id="bf4fa-114">https://\<IntPoolFQDN\>/AutoDiscover/ autodiscoverservice.svc/Root for internal access</span></span>
    
    <span data-ttu-id="bf4fa-115">Wir empfehlen dringend die Verwendung der automatischen Erkennung.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-115">We strongly recommend using automatic discovery.</span></span> <span data-ttu-id="bf4fa-116">Die primäre Verwendung von manuellen Einstellungen dient zur Problembehandlung.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-116">The primary use of manual settings is for troubleshooting.</span></span>

  - <span data-ttu-id="bf4fa-117">**Wenn Sie sich entschließen, die automatische Ermittlung zu unterstützen, sind Sie bereit, Zertifikate auf dem Reverse-Proxy mit alternativen Subjektnamen für die einzelnen SIP-Domänen zu aktualisieren?**</span><span class="sxs-lookup"><span data-stu-id="bf4fa-117">**If you decide to support automatic discovery, are you willing to update certificates on the reverse proxy with subject alternative names for each SIP domain?**</span></span>
    
    <span data-ttu-id="bf4fa-118">Wenn Sie über viele SIP-Domänen verfügen, kann das Aktualisieren öffentlicher Zertifikate auf dem Reverse-Proxy sehr teuer werden.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-118">If you have many SIP domains, updating public certificates on the reverse proxy can become very expensive.</span></span> <span data-ttu-id="bf4fa-119">Wenn dies der Fall ist, können Sie die automatische Ermittlung so implementieren, dass die anfängliche AutoErmittlungsdienst Anforderung http auf Port 80 verwendet, anstatt HTTPS auf Port 443 zu verwenden.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-119">If this is the case, you can choose to implement automatic discovery so that the initial Autodiscover Service request uses HTTP on port 80, instead of using HTTPS on port 443.</span></span> <span data-ttu-id="bf4fa-120">Dies ist jedoch nicht die empfohlene Vorgehensweise.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-120">However, this is not the recommended approach.</span></span> <span data-ttu-id="bf4fa-121">Wenn Sie sich entscheiden, diese Alternative zu wählen, müssen Sie die Zertifikate auf dem Reverseproxy nicht aktualisieren, Sie müssen jedoch eine Webveröffentlichungsregel für http auf Port 80 erstellen.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-121">If you decide to choose this alternative, you do not need to update the certificates on the reverse proxy, but you need to create a web publishing rule for HTTP on port 80.</span></span> <span data-ttu-id="bf4fa-122">Weitere Informationen finden Sie unter [Technische Voraussetzungen für Mobilität in lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span><span class="sxs-lookup"><span data-stu-id="bf4fa-122">For more details, see [Technical requirements for mobility in Lync Server 2013](lync-server-2013-technical-requirements-for-mobility.md).</span></span>

  - <span data-ttu-id="bf4fa-123">**Möchten Sie lync Mobile-Clients sowohl intern als auch extern für das Unternehmensnetzwerk unterstützen oder Clients nur innerhalb des Unternehmensnetzwerks unterstützen?**</span><span class="sxs-lookup"><span data-stu-id="bf4fa-123">**Do you want to support Lync mobile clients both internal and external to the corporate network, or support clients only inside the corporate network?**</span></span>
    
    <span data-ttu-id="bf4fa-124">Wenn Sie Mobile Clients innerhalb und außerhalb Ihres Netzwerks unterstützen möchten, können mobile Geräte von jedem beliebigen Standort aus auf Mobilitätsfeatures zugreifen.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-124">If you want to support mobile clients internal and external to your network, mobile devices can access mobility features from any location.</span></span> <span data-ttu-id="bf4fa-125">Die Standardkonfiguration ist die Unterstützung von internen und externen Clients im Unternehmensnetzwerk.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-125">The default configuration is to support clients both internal and external to the corporate network.</span></span>
    
    <span data-ttu-id="bf4fa-126">Zwar kann die Standardkonfiguration den mobilen Client Datenverkehr auf der externen Website durchlaufen, doch können Sie den mobilen Client Datenverkehr auf das interne Unternehmensnetzwerk einschränken.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-126">Although the default configuration enables mobile client traffic to go through the external site, you can restrict mobile client traffic to the internal corporate network.</span></span> <span data-ttu-id="bf4fa-127">Wenn Sie den Datenverkehr auf das interne Netzwerk einschränken, können Benutzer lync Mobile-Anwendungen nur auf Ihren mobilen Geräten verwenden, wenn Sie sich im Netzwerk befinden.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-127">When you restrict the traffic to the internal network, users can use Lync mobile applications on their mobile devices only when they are inside the network.</span></span>
    
    <span data-ttu-id="bf4fa-128">Für Bereitstellungen, die Mobilität mithilfe des MCX-mobilitätsdiensts und lync 2010 Mobile unterstützen, führen Sie das Cmdlet " **setCsMcxConfiguration** " aus.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-128">For deployments that support mobility using the Mcx mobility service and Lync 2010 Mobile, you run the **Set-CsMcxConfiguration** cmdlet.</span></span> <span data-ttu-id="bf4fa-129">Wenn Sie die Mobilität nur für die interne Verwendung einstellen möchten, verwenden Sie einen Befehl ähnlich der folgenden:</span><span class="sxs-lookup"><span data-stu-id="bf4fa-129">To set mobility for internal use only, you would use a command similar to the following:</span></span>
    
        Set-CsMcxConfiguration -Identity site:Redmond -ExposedWebURL Internal
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="bf4fa-130">Für UCWA sind keine zusätzlichen Konfigurationen erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-130">There are no additional configurations required for UCWA.</span></span> <span data-ttu-id="bf4fa-131">UCWA hat keine äquivalente interne Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-131">UCWA does not have an equivalent internal-only configuration.</span></span>

    
    </div>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="bf4fa-132">Wenn Sie einen lync Server 2013- &nbsp; Front-End-Server oder Front-End <STRONG>you do not have</STRONG> -Pools verwenden und keine lync Server 2010- &nbsp; Front-End-Server oder Front-End-Pools vorhanden sind, <STRONG>gibt es keine Anforderung für die Cookie-basierte Persistenz</STRONG>.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-132">If you are using a Lync Server 2013&nbsp;Front End Server or Front End pools and <STRONG>you do not have</STRONG> any Lync Server 2010&nbsp;Front End Servers or Front End pools, <STRONG>there is no requirement for cookie-based persistence</STRONG>.</span></span> <span data-ttu-id="bf4fa-133">Wenn Sie alle lync Server 2010 &nbsp; -Front-End-Server oder Front-End-Pools beibehalten müssen, gelten die gleichen Regeln wie in lync Server 2010 für Cookie-basierte Persistenz.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-133">If you need to retain any Lync Server 2010&nbsp;Front End Servers or Front End pools, the same rules still apply as in Lync Server 2010 for cookie-based persistence.</span></span>

    
    </div>

  - <span data-ttu-id="bf4fa-134">**Möchten Sie Push-Benachrichtigungen für Apple IOS-Geräte und Windows phones unterstützen?**</span><span class="sxs-lookup"><span data-stu-id="bf4fa-134">**Do you want to support push notifications for Apple iOS devices and Windows Phones?**</span></span>
    
    <span data-ttu-id="bf4fa-135">Wenn Sie Push-Benachrichtigungen unterstützen, erhalten unterstützte Apple IOS-Geräte und Windows phones eine Benachrichtigung über Ereignisse, die auftreten, wenn die Mobile Anwendung inaktiv ist.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-135">If you support push notifications, supported Apple iOS devices and Windows Phones receive a notification of events that occur when the mobile application is inactive.</span></span> <span data-ttu-id="bf4fa-136">Sie müssen den Edgeserver so konfigurieren, dass er über eine Verbundbeziehung mit dem cloudbasierten lync Server-Push-Benachrichtigungsdienst verfügt, der sich im lync Online-Rechenzentrum befindet, und ein Cmdlet ausführen, um Push-Benachrichtigungen zu aktivieren.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-136">You must configure your Edge Server to have a federation relationship with the cloud-based Lync Server Push Notification Service, which is located in the Lync Online datacenter, and run a cmdlet to enable push notifications.</span></span>
    
    <span data-ttu-id="bf4fa-137">Wenn Sie Push-Benachrichtigungen über Ihr Wi-Fi-Netzwerk unterstützen möchten, müssen Sie zusätzlich zur Unterstützung von Push-Benachrichtigungen über die 3G-oder Datennetzwerke des Mobilfunkanbieters Port 5223 in Ihrem Enterprise-Wi-Fi-Netzwerk öffnen.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-137">If you want to support push notifications over your Wi-Fi network, in addition to supporting push notifications over the mobile device providers' 3G or data networks, you must open port 5223 outbound on your enterprise Wi-Fi network.</span></span> <span data-ttu-id="bf4fa-138">Das unterstützen von Push-Benachrichtigungen über das Wi-Fi-Netzwerk unterstützt mobile Geräte, die nur Wi-Fi-und Mobilgeräte verwenden, die einen schlechten Empfang in der Halle aufweisen.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-138">Supporting push notifications over the Wi-Fi network supports mobile devices that use only Wi-Fi and mobile devices that have poor indoor reception.</span></span>
    
    <div>
    

    > [!IMPORTANT]  
    > <span data-ttu-id="bf4fa-139">Das Öffnen von Port TCP 5223 ist nur erforderlich, wenn Apple-Geräte unterstützt werden, auf denen der Mobile lync 2010-Client ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-139">Opening port TCP 5223 is required only when supporting Apple devices running the Lync 2010 Mobile client.</span></span>

    
    </div>
    
    <span data-ttu-id="bf4fa-140">Wenn Sie keine Push-Benachrichtigungen unterstützen, finden Benutzer von mobilen Apple-Geräten und Windows-Smartphones keine Informationen zu Ereignissen wie Sofortnachrichten-Einladungen oder verpassten Nachrichten, die auftreten, wenn die Mobile Anwendung inaktiv ist.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-140">If you do not support push notifications, users of Apple mobile devices and Windows Phones will not find out about events—such as instant message invitations or missed messages—that occur when the mobile application is inactive.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="bf4fa-141">Für lync 2013 Mobile-Clients auf Apple-Geräten ist keine Push-Benachrichtigung erforderlich.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-141">Lync 2013 Mobile clients on Apple devices do not require push notification.</span></span> <span data-ttu-id="bf4fa-142">Die mobilen lync 2013-Clients auf Windows Phone verwenden eine Push-Benachrichtigung.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-142">The Lync 2013 Mobile clients on Windows Phone use push notification.</span></span> <span data-ttu-id="bf4fa-143">Die Planung für die Push-Benachrichtigung und das Clearing House für die Push-Benachrichtigung bleiben für lync Mobile auf Windows Phone-und Apple-Geräten gleich, die nicht in der Lage sind, den mobilen lync 2013-Client auszuführen.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-143">Planning for push notification and the push notification clearinghouse remain the same for Lync Mobile on Windows Phone and Apple devices that are not able to run the Lync 2013 Mobile client.</span></span>

    
    </div>

  - <span data-ttu-id="bf4fa-144">**Möchten Sie, dass alle Benutzer Zugriff auf Mobilitätsfeatures haben, oder möchten Sie in der Lage sein, anzugeben, welche Benutzer Zugriff auf diese Features haben?**</span><span class="sxs-lookup"><span data-stu-id="bf4fa-144">**Do you want all users to have access to mobility features, or do you want to be able to specify which users have access to these features?**</span></span>
    
    <span data-ttu-id="bf4fa-145">In der Tabelle werden die Features beschrieben, die Benutzern in lync Server 2013 zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-145">The table describes features available to users in Lync Server 2013.</span></span> <span data-ttu-id="bf4fa-146">Die Standardeinstellungen ermöglichen Anruf über Arbeit, VoIP (Voice over IP) und ermöglichen Mobilität.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-146">The defaults allow Call via Work, allow Voice over IP (VoIP), and enable Mobility.</span></span> <span data-ttu-id="bf4fa-147">Hier finden Sie die vollständige Auswahl der verfügbaren Optionen:</span><span class="sxs-lookup"><span data-stu-id="bf4fa-147">Here is the full set of available options:</span></span>
    
    
    <table>
    <colgroup>
    <col style="width: 33%" />
    <col style="width: 33%" />
    <col style="width: 33%" />
    </colgroup>
    <thead>
    <tr class="header">
    <th><span data-ttu-id="bf4fa-148">Feature/Parameter Name/Bereich (Richtlinien Parameter Namen sind möglicherweise nicht identisch)</span><span class="sxs-lookup"><span data-stu-id="bf4fa-148">Feature/Parameter Name/Scope (Policy parameter names may not be the same)</span></span></th>
    <th><span data-ttu-id="bf4fa-149">Beschreibung</span><span class="sxs-lookup"><span data-stu-id="bf4fa-149">Description</span></span></th>
    <th><span data-ttu-id="bf4fa-150">Eingeführt</span><span class="sxs-lookup"><span data-stu-id="bf4fa-150">Introduced</span></span></th>
    </tr>
    </thead>
    <tbody>
    <tr class="odd">
    <td><p><span data-ttu-id="bf4fa-151">Mobilität aktivieren</span><span class="sxs-lookup"><span data-stu-id="bf4fa-151">Enable Mobility</span></span></p>
    <p><span data-ttu-id="bf4fa-152">Parameter Name: <code>EnableMobility</code></span><span class="sxs-lookup"><span data-stu-id="bf4fa-152">Parameter Name : <code>EnableMobility</code></span></span></p>
    <p><span data-ttu-id="bf4fa-153">Bereich: Global/Website/Benutzer</span><span class="sxs-lookup"><span data-stu-id="bf4fa-153">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="bf4fa-154">Administrative Einstellung Wenn die Richtlinie auf "false" festgelegt ist, kann der Benutzer sich nicht beim Client anmelden, um die Benutzer in einem bestimmten Bereich zu steuern, auf dem die lync Mobile-Anwendung installiert ist.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-154">Administrative setting to control users in a given scope that have the Lync Mobile installed, If the policy is set to False, the user would not be able to sign into the client.</span></span></p>
    <p><span data-ttu-id="bf4fa-155">Die Standardeinstellung ist wahr.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-155">The default setting is True.</span></span></p></td>
    <td><p><span data-ttu-id="bf4fa-156">Kumulatives Update für lync Server 2010: November 2011</span><span class="sxs-lookup"><span data-stu-id="bf4fa-156">Cumulative Update for Lync Server 2010: November 2011</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="bf4fa-157">Aktivieren von Fremdsprache</span><span class="sxs-lookup"><span data-stu-id="bf4fa-157">Enable Outside Voice</span></span></p>
    <p><span data-ttu-id="bf4fa-158">Parameter Name: <code>EnableOutsideVoice</code></span><span class="sxs-lookup"><span data-stu-id="bf4fa-158">Parameter Name : <code>EnableOutsideVoice</code></span></span></p>
    <p><span data-ttu-id="bf4fa-159">Bereich: Global/Website/Benutzer</span><span class="sxs-lookup"><span data-stu-id="bf4fa-159">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="bf4fa-160">Steuert die Möglichkeit des Benutzers, Anrufe über Arbeit zu verwenden, eine Funktion, mit der Benutzer Anrufe tätigen und entgegennehmen können, indem Sie Ihre geschäftliche Nummer anstelle Ihrer Mobiltelefonnummer verwenden.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-160">Controls a user’s ability to use Call Via Work, a feature that enables users to make and receive calls by using their work number instead of their mobile number.</span></span> <span data-ttu-id="bf4fa-161">Wenn Sie auf "false" festgelegt ist, kann der Benutzer keine Anrufe tätigen oder entgegennehmen, indem er seine geschäftliche Nummer auf seinem mobilen Gerät verwendet.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-161">If set to False, the user will not be able to make or receive calls by using their work number from their mobile device.</span></span></p>
    <p><span data-ttu-id="bf4fa-162">Die Standardeinstellung ist wahr.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-162">The default setting is True</span></span></p></td>
    <td><p><span data-ttu-id="bf4fa-163">Kumulatives Update für lync Server 2010: November 2011</span><span class="sxs-lookup"><span data-stu-id="bf4fa-163">Cumulative Update for Lync Server 2010: November 2011</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="bf4fa-164">IP-Audio und -Video aktivieren</span><span class="sxs-lookup"><span data-stu-id="bf4fa-164">Enable IP Audio and Video</span></span></p>
    <p><span data-ttu-id="bf4fa-165">Parameter Name: <code>EnableIPAudioVideo</code></span><span class="sxs-lookup"><span data-stu-id="bf4fa-165">Parameter Name : <code>EnableIPAudioVideo</code></span></span></p>
    <p><span data-ttu-id="bf4fa-166">Bereich: Global/Website/Benutzer</span><span class="sxs-lookup"><span data-stu-id="bf4fa-166">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="bf4fa-167">Steuert, ob ein Benutzer VoIP verwenden kann, um Sprach-oder Videoanrufe auf seinem mobilen Gerät zu tätigen oder zu empfangen.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-167">Controls whether a user can use VoIP to make or receive voice or video calls on their mobile device.</span></span> <span data-ttu-id="bf4fa-168">Wenn Sie auf "false" festgelegt ist, kann der Benutzer keine VoIP-oder Videoanrufe auf seinem Gerät tätigen oder empfangen.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-168">If set to False, the user will not be able to make or receive VoIP or video calls on their device.</span></span></p>
    <p><span data-ttu-id="bf4fa-169">Die Standardeinstellung ist wahr.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-169">The default setting is True.</span></span></p></td>
    <td><p><span data-ttu-id="bf4fa-170">Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf4fa-170">Microsoft Lync Server 2013</span></span></p></td>
    </tr>
    <tr class="even">
    <td><p><span data-ttu-id="bf4fa-171">Wi-Fi für IP-Audio erforderlich</span><span class="sxs-lookup"><span data-stu-id="bf4fa-171">Require WiFi for IP Audio</span></span></p>
    <p><span data-ttu-id="bf4fa-172">Parameter Name: <code>RequireWiFiForIPAudio</code></span><span class="sxs-lookup"><span data-stu-id="bf4fa-172">Parameter Name : <code>RequireWiFiForIPAudio</code></span></span></p>
    <p><span data-ttu-id="bf4fa-173">Bereich: Global/Website/Benutzer</span><span class="sxs-lookup"><span data-stu-id="bf4fa-173">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="bf4fa-174">Mit dieser Einstellung wird festgelegt, ob der Client Anrufe über VoIP über WLAN statt über das Mobilfunknetz führen und empfangen muss.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-174">This setting defines whether the client will be required to make and receive calls over VoIP on WiFi instead of the cellular data network.</span></span> <span data-ttu-id="bf4fa-175">Wenn der Benutzer auf "true" festgelegt ist, kann er nur dann VoIP-Anrufe tätigen und empfangen, wenn er mit einem WLAN-Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-175">If set to True, the user can make and receive VoIP calls only when connected to a WiFi network.</span></span></p>
    <p><span data-ttu-id="bf4fa-176">Die Standardeinstellung ist "false".</span><span class="sxs-lookup"><span data-stu-id="bf4fa-176">The default setting is False.</span></span></p></td>
    <td><p><span data-ttu-id="bf4fa-177">Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf4fa-177">Microsoft Lync Server 2013</span></span></p></td>
    </tr>
    <tr class="odd">
    <td><p><span data-ttu-id="bf4fa-178">Wi-Fi für IP-Video erforderlich</span><span class="sxs-lookup"><span data-stu-id="bf4fa-178">Require WiFi for IP Video</span></span></p>
    <p><span data-ttu-id="bf4fa-179">Parameter Name: <code>RequireWiFiForIPVideo</code></span><span class="sxs-lookup"><span data-stu-id="bf4fa-179">Parameter Name : <code>RequireWiFiForIPVideo</code></span></span></p>
    <p><span data-ttu-id="bf4fa-180">Bereich: Global/Website/Benutzer</span><span class="sxs-lookup"><span data-stu-id="bf4fa-180">Scope: Global/Site/User</span></span></p></td>
    <td><p><span data-ttu-id="bf4fa-181">Mit dieser Einstellung wird festgelegt, ob der Client Videoanrufe auf Wi-Fi statt im zellularen Datennetzwerk tätigen und empfangen muss.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-181">This setting defines whether the client will be required to make and receive video calls on Wi-Fi instead of on the cellular data network.</span></span> <span data-ttu-id="bf4fa-182">Wenn der Benutzer auf "true" festgelegt ist, kann er nur dann Videoanrufe tätigen und empfangen, wenn er mit einem Wi-Fi Netzwerk verbunden ist.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-182">If set to True, the user can make and receive video calls only when connected to a Wi-Fi network.</span></span></p>
    <p><span data-ttu-id="bf4fa-183">Die Standardeinstellung ist "false".</span><span class="sxs-lookup"><span data-stu-id="bf4fa-183">The default setting is False.</span></span></p></td>
    <td><p><span data-ttu-id="bf4fa-184">Microsoft Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf4fa-184">Microsoft Lync Server 2013</span></span></p></td>
    </tr>
    </tbody>
    </table>
    
    <span data-ttu-id="bf4fa-185">Eine Beschreibung der Richtlinieneinstellungen, die Sie konfigurieren können, und Informationen zum Verwalten der Richtlinien finden Sie unter [New-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy), [CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsMobilityPolicy), [Get-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Get-CsMobilityPolicy), [Grant-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsMobilityPolicy) und [Remove-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsMobilityPolicy).</span><span class="sxs-lookup"><span data-stu-id="bf4fa-185">For a description of the policy settings that you can configure, and how to manage the policies, see [New-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/New-CsMobilityPolicy), [Set-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Set-CsMobilityPolicy), [Get-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Get-CsMobilityPolicy), [Grant-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Grant-CsMobilityPolicy) and [Remove-CsMobilityPolicy](https://docs.microsoft.com/powershell/module/skype/Remove-CsMobilityPolicy).</span></span>

  - <span data-ttu-id="bf4fa-186">**Möchten Sie, dass Benutzer, die nicht für Enterprise-VoIP aktiviert sind, in der Lage sein, Click-to-Join zu verwenden, um an Konferenzen teilzunehmen?**</span><span class="sxs-lookup"><span data-stu-id="bf4fa-186">**Do you want users who are not enabled for Enterprise Voice to be able to use Click to Join to join conferences?**</span></span>
    
    <span data-ttu-id="bf4fa-187">Damit Benutzer Zugriff auf Mobilitätsfunktionen haben und über die Arbeit anrufen können, müssen Sie für Enterprise-VoIP aktiviert sein.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-187">For users to have access to mobility features and Call via Work, they must be enabled for Enterprise Voice.</span></span> <span data-ttu-id="bf4fa-188">Benutzer, die nicht für Enterprise-VoIP aktiviert sind, können jedoch an Konferenzen teilnehmen, indem Sie auf dem mobilen Gerät auf den Link klicken, wenn Ihnen eine entsprechende VoIP-Richtlinie zugewiesen ist.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-188">However, users who are not enabled for Enterprise Voice can join conferences by clicking the link on their mobile device, if they have an appropriate voice policy assigned to them.</span></span> <span data-ttu-id="bf4fa-189">Sie können diesen Benutzern entweder eine bestimmte VoIP-Richtlinie zuweisen oder sicherstellen, dass eine globale Richtlinie oder eine Richtlinie auf Websiteebene vorhanden ist, die für diese Benutzer gilt.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-189">You can either assign a specific voice policy to these users or make sure that a global policy or site-level policy exists that applies to them.</span></span> <span data-ttu-id="bf4fa-190">Die VoIP-Richtlinie, die Sie zuweisen, muss über öffentliche PSTN-Nutzungsdatensätze und-Routen verfügen, die die Bereiche definieren, in die die Benutzer zum teilnehmen an einer Konferenz wählen können.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-190">The voice policy that you assign must have public switched telephone network (PSTN) usage records and routes that define the areas to which users can dial out to join a conference.</span></span> <span data-ttu-id="bf4fa-191">Details zum Festlegen von VoIP-Richtlinien, PSTN-Verwendungsdatensätzen und Routen finden Sie unter [Konfigurieren von VoIP-Richtlinien, PSTN-Verwendungsdatensätzen und VoIP-Routen in lync Server 2013](lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md).</span><span class="sxs-lookup"><span data-stu-id="bf4fa-191">For details about setting voice policy, PSTN usage records, and routes, see [Configuring voice policies, PSTN usage records, and voice routes in Lync Server 2013](lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md).</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="bf4fa-192">Für mobile Benutzer, die Click-to-Join verwenden möchten, ist eine VoIP-Richtlinie zusammen mit den zugehörigen PSTN-Nutzungsdaten Sätzen und VoIP-Routen erforderlich, da durch Klicken auf den Link auf dem mobilen Gerät ein ausgehender Anruf von lync Server 2013 entsteht.</span><span class="sxs-lookup"><span data-stu-id="bf4fa-192">Mobile users who want to use Click to Join require a voice policy, along with the related PSTN usage records and voice routes, because clicking the link on the mobile device results in an outbound call from Lync Server 2013.</span></span>

    
    </div>

<div>

## <a name="see-also"></a><span data-ttu-id="bf4fa-193">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bf4fa-193">See Also</span></span>


[<span data-ttu-id="bf4fa-194">Technische Anforderungen für die Mobilität in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf4fa-194">Technical requirements for mobility in Lync Server 2013</span></span>](lync-server-2013-technical-requirements-for-mobility.md)  


[<span data-ttu-id="bf4fa-195">Konfigurieren von VoIP-Richtlinien, PSTN-Verwendungsdatensätzen und VoIP-Routen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bf4fa-195">Configuring voice policies, PSTN usage records, and voice routes in Lync Server 2013</span></span>](lync-server-2013-configuring-voice-policies-pstn-usage-records-and-voice-routes.md)  
  

<span data-ttu-id="bf4fa-196"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bf4fa-196"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

