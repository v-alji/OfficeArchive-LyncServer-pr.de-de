---
title: 'Lync Server 2013: Konfigurieren von Pushbenachrichtigungen'
description: 'Lync Server 2013: Konfigurieren für Push-Benachrichtigungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Configuring for push notifications
ms:assetid: d77f2c06-0fe6-45d5-8f08-808ab871b3e0
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Hh690047(v=OCS.15)
ms:contentKeyID: 48185574
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 24c22ff42f666add9eac4966134c88b9bf680046
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49433082"
---
# <a name="configuring-for-push-notifications-in-lync-server-2013"></a><span data-ttu-id="bc0e8-103">Konfigurieren von Pushbenachrichtigungen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="bc0e8-103">Configuring for push notifications in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="bc0e8-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="bc0e8-104">

<span> </span></span></span>

<span data-ttu-id="bc0e8-105">_**Letztes Änderungsdatum des Themas:** 2013-02-12_</span><span class="sxs-lookup"><span data-stu-id="bc0e8-105">_**Topic Last Modified:** 2013-02-12_</span></span>

<span data-ttu-id="bc0e8-106">Push-Benachrichtigungen in Form von Signalen, Symbolen oder Benachrichtigungen können auch dann an ein mobiles Gerät gesendet werden, wenn die Mobile Anwendung inaktiv ist.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-106">Push notifications, in the form of badges, icons, or alerts, can be sent to a mobile device even when the mobile application is inactive.</span></span> <span data-ttu-id="bc0e8-107">Push-Benachrichtigungen benachrichtigt einen Benutzer über Ereignisse wie eine neue oder verpasste Chat Einladung und Voicemail.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-107">Push notifications notify a user of events such as a new or missed IM invitation and voice mail.</span></span> <span data-ttu-id="bc0e8-108">Der lync Server 2013-Mobilitätsdienst sendet die Benachrichtigungen an den cloudbasierten lync Server-Push-Benachrichtigungsdienst, der dann die Benachrichtigungen an den Apple Push Notification Service (APNS) (für ein Apple-Gerät mit dem lync 2010-Mobilclient) oder den Microsoft Push Notification Service (MPNS) sendet (für ein Windows Phone-Gerät, auf dem lync 2010 Mobile oder der Mobile lync 2013-Client ausgeführt</span><span class="sxs-lookup"><span data-stu-id="bc0e8-108">The Lync Server 2013 Mobility Service sends the notifications to the cloud-based Lync Server Push Notification Service, which then sends the notifications to the Apple Push Notification Service (APNS) (for an Apple device running the Lync 2010 Mobile client) or the Microsoft Push Notification Service (MPNS) (for a Windows Phone device running the Lync 2010 Mobile or the Lync 2013 Mobile client).</span></span>

<div>


> [!IMPORTANT]  
> <span data-ttu-id="bc0e8-109">Wenn Sie Windows Phone mit lync 2010 Mobile-oder lync 2013-Mobilclient verwenden, ist eine Push-Benachrichtigung eine wichtige Überlegung.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-109">If you use Windows Phone with Lync 2010 Mobile or Lync 2013 Mobile client, push notification is an important consideration.</span></span><BR><span data-ttu-id="bc0e8-110">Wenn Sie lync 2010 Mobile auf Apple-Geräten verwenden, ist eine Push-Benachrichtigung eine wichtige Überlegung.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-110">If you use Lync 2010 Mobile on Apple devices, push notification is an important consideration.</span></span><BR><span data-ttu-id="bc0e8-111">Wenn Sie lync 2013 Mobile auf Apple-Geräten verwenden, benötigen Sie keine Push-Benachrichtigung mehr.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-111">If you use Lync 2013 Mobile on Apple devices, you no longer need push notification.</span></span>



</div>

<span data-ttu-id="bc0e8-112">Konfigurieren Sie Ihre Topologie so, dass Push-Benachrichtigungen unterstützt werden, indem Sie wie folgt vorgehen:</span><span class="sxs-lookup"><span data-stu-id="bc0e8-112">Configure your topology to support push notifications by doing the following:</span></span>

  - <span data-ttu-id="bc0e8-113">Wenn Ihre Umgebung über einen lync Server 2010-oder lync Server 2013-Edgeserver verfügt, müssen Sie einen neuen Hostinganbieter, Microsoft lync Online, hinzufügen und dann den Anbieter Verbund für den Hostinganbieter zwischen Ihrer Organisation und lync Online einrichten.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-113">If your environment has a Lync Server 2010 or Lync Server 2013 Edge Server, you need to add a new hosting provider, Microsoft Lync Online, and then set up hosting provider federation between your organization and Lync Online.</span></span>

  - <span data-ttu-id="bc0e8-114">Wenn Ihre Umgebung über einen Office Communications Server 2007 R2 Edge-Server verfügt, müssen Sie Direct SIP Federation mit Push.lync.com einrichten.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-114">If your environment has a Office Communications Server 2007 R2 Edge Server, you need to set up direct SIP federation with push.lync.com.</span></span>
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="bc0e8-115">Push.lync.com ist eine Microsoft Office 365-Domäne für den Push-Benachrichtigungsdienst.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-115">Push.lync.com is a Microsoft Office 365 domain for Push Notification Service.</span></span>

    
    </div>

  - <span data-ttu-id="bc0e8-116">Um Push-Benachrichtigungen zu aktivieren, müssen Sie das Cmdlet " **setCsPushNotificationConfiguration** " ausführen.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-116">To enable push notifications, you need to run the **Set-CsPushNotificationConfiguration** cmdlet.</span></span> <span data-ttu-id="bc0e8-117">Pushbenachrichtigungen sind standardmäßig deaktiviert.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-117">By default, push notifications are turned off.</span></span>

  - <span data-ttu-id="bc0e8-118">Testen Sie die Föderations Konfiguration und die Push-Benachrichtigungen.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-118">Test the federation configuration and push notifications.</span></span>

<div>

## <a name="to-configure-for-push-notifications-with-lync-server-2013-or-lync-server-2010-edge-server"></a><span data-ttu-id="bc0e8-119">So konfigurieren Sie für Push-Benachrichtigungen mit lync Server 2013 oder lync Server 2010 Edge-Server</span><span class="sxs-lookup"><span data-stu-id="bc0e8-119">To configure for push notifications with Lync Server 2013 or Lync Server 2010 Edge Server</span></span>

1.  <span data-ttu-id="bc0e8-120">Melden Sie sich bei einem Computer an, auf dem die lync Server-Verwaltungsshell und OCSCore als Mitglied der RtcUniversalServerAdmins-Gruppe installiert sind.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-120">Log on to a computer where Lync Server Management Shell and Ocscore are installed as a member of the RtcUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="bc0e8-121">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-121">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="bc0e8-122">Hinzufügen eines lync Server Online-Hostinganbieter.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-122">Add a Lync Server online hosting provider.</span></span> <span data-ttu-id="bc0e8-123">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="bc0e8-123">At the command line, type:</span></span>
    
        New-CsHostingProvider -Identity <unique identifier for Lync Online hosting provider> -Enabled $True -ProxyFqdn <FQDN for the Access Server used by the hosting provider> -VerificationLevel UseSourceVerification
    
    <span data-ttu-id="bc0e8-124">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="bc0e8-124">For example:</span></span>
    
        New-CsHostingProvider -Identity "LyncOnline" -Enabled $True -ProxyFqdn "sipfed.online.lync.com" -VerificationLevel UseSourceVerification
    
    <div>
    

    > [!NOTE]  
    > <span data-ttu-id="bc0e8-125">Es ist nicht möglich, mehr als eine Verbundbeziehung mit einem einzelnen Hostinganbieter zu haben.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-125">You cannot have more than one federation relationship with a single hosting provider.</span></span> <span data-ttu-id="bc0e8-126">Wenn Sie bereits einen Hostinganbieter eingerichtet haben, der über eine Verbundbeziehung zu sipfed.online.lync.com verfügt, fügen Sie keinen weiteren Hostinganbieter hinzu, auch wenn die Identität des Hostinganbieter etwas anderes als LyncOnline ist.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-126">That is, if you have already set up a hosting provider that has a federation relationship with sipfed.online.lync.com, do not add another hosting provider for it, even if the identity of the hosting provider is something other than LyncOnline.</span></span>

    
    </div>

4.  <span data-ttu-id="bc0e8-127">Einrichten des Anbieters von Hostinganbieter zwischen Ihrer Organisation und dem Push-Benachrichtigungsdienst bei lync Online</span><span class="sxs-lookup"><span data-stu-id="bc0e8-127">Set up hosting provider federation between your organization and the Push Notification Service at Lync Online.</span></span> <span data-ttu-id="bc0e8-128">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="bc0e8-128">At the command line, type:</span></span>
    
        New-CsAllowedDomain -Identity "push.lync.com"

</div>

<div>

## <a name="to-configure-for-push-notifications-with-office-communications-server-2007-r2-edge-server"></a><span data-ttu-id="bc0e8-129">So konfigurieren Sie für Push-Benachrichtigungen mit Office Communications Server 2007 R2-Edgeserver</span><span class="sxs-lookup"><span data-stu-id="bc0e8-129">To configure for push notifications with Office Communications Server 2007 R2 Edge Server</span></span>

1.  <span data-ttu-id="bc0e8-130">Melden Sie sich beim Edgeserver als Mitglied der RtcUniversalServerAdmins-Gruppe an.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-130">Log on to the Edge Server as a member of the RtcUniversalServerAdmins group.</span></span>

2.  <span data-ttu-id="bc0e8-131">Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Verwaltung**, und klicken Sie dann auf **Computer Verwaltung**.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-131">Click **Start**, click **All Programs**, click **Administrative Tools**, and then click **Computer Management**.</span></span>

3.  <span data-ttu-id="bc0e8-132">Erweitern Sie in der Konsolenstruktur **Dienste und Anwendungen**, klicken Sie mit der rechten Maustaste auf **Microsoft Office Communications Server 2007 R2**, und klicken Sie dann auf **Eigenschaften**.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-132">In the console tree, expand **Services and Applications**, right-click **Microsoft Office Communications Server 2007 R2**, and then click **Properties**.</span></span>

4.  <span data-ttu-id="bc0e8-133">Klicken Sie auf der Registerkarte **zulassen** auf **Hinzufügen**.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-133">On the **Allow** tab, click **Add**.</span></span>

5.  <span data-ttu-id="bc0e8-134">Führen Sie im Dialogfeld **Federated-Partner hinzufügen** die folgenden Aktionen aus:</span><span class="sxs-lookup"><span data-stu-id="bc0e8-134">In the **Add Federated Partner** dialog box, do the following:</span></span>
    
      - <span data-ttu-id="bc0e8-135">Geben Sie im **Domänennamen des Verbundpartners** **Push.lync.com** ein.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-135">In **Federated partner domain name**, type **push.lync.com**.</span></span>
    
      - <span data-ttu-id="bc0e8-136">Geben Sie im **Access-Edgeserver für Federated-Partner** **sipfed.online.lync.com**.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-136">In **Federated partner Access Edge Server**, type **sipfed.online.lync.com**.</span></span>
    
      - <span data-ttu-id="bc0e8-137">Klicken Sie auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-137">Click **OK**.</span></span>

</div>

<div>

## <a name="to-enable-push-notifications"></a><span data-ttu-id="bc0e8-138">So aktivieren Sie Push-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="bc0e8-138">To enable push notifications</span></span>

1.  <span data-ttu-id="bc0e8-139">Melden Sie sich bei einem Computer an, auf dem die lync Server-Verwaltungsshell und OCSCore als Mitglied der CsAdministrator-Rolle installiert sind.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-139">Log on to a computer where Lync Server Management Shell and Ocscore are installed as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="bc0e8-140">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-140">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="bc0e8-141">Aktivieren von Push-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="bc0e8-141">Enable push notifications.</span></span> <span data-ttu-id="bc0e8-142">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="bc0e8-142">At the command line, type:</span></span>
    
        Set-CsPushNotificationConfiguration -EnableApplePushNotificationService $True -EnableMicrosoftPushNotificationService $True

4.  <span data-ttu-id="bc0e8-143">Föderation aktivieren</span><span class="sxs-lookup"><span data-stu-id="bc0e8-143">Enable federation.</span></span> <span data-ttu-id="bc0e8-144">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="bc0e8-144">At the command line, type:</span></span>
    
        Set-CsAccessEdgeConfiguration -AllowFederatedUsers $True

</div>

<div>

## <a name="to-test-federation-and-push-notifications"></a><span data-ttu-id="bc0e8-145">So testen Sie Föderations-und Push-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="bc0e8-145">To test federation and push notifications</span></span>

1.  <span data-ttu-id="bc0e8-146">Melden Sie sich bei einem Computer an, auf dem die lync Server-Verwaltungsshell und OCSCore als Mitglied der CsAdministrator-Rolle installiert sind.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-146">Log on to a computer where Lync Server Management Shell and Ocscore are installed as a member of the CsAdministrator role.</span></span>

2.  <span data-ttu-id="bc0e8-147">Starten Sie die lync Server-Verwaltungsshell: Klicken Sie auf **Start**, klicken Sie auf **Alle Programme**, klicken Sie auf **Microsoft lync Server 2013**, und klicken Sie dann auf **lync Server-Verwaltungsshell**.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-147">Start the Lync Server Management Shell: Click **Start**, click **All Programs**, click **Microsoft Lync Server 2013**, and then click **Lync Server Management Shell**.</span></span>

3.  <span data-ttu-id="bc0e8-148">Testen Sie die Verbund Konfiguration.</span><span class="sxs-lookup"><span data-stu-id="bc0e8-148">Test the federation configuration.</span></span> <span data-ttu-id="bc0e8-149">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="bc0e8-149">At the command line, type:</span></span>
    
        Test-CsFederatedPartner -TargetFqdn <FQDN of Access Edge server used for federated SIP traffic> -Domain <FQDN of federated domain> -ProxyFqdn <FQDN of the Access Edge server used by the federated organization>
    
    <span data-ttu-id="bc0e8-150">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="bc0e8-150">For example:</span></span>
    
        Test-CsFederatedPartner -TargetFqdn accessproxy.contoso.com -Domain push.lync.com -ProxyFqdn sipfed.online.lync.com

4.  <span data-ttu-id="bc0e8-151">Testen von Push-Benachrichtigungen</span><span class="sxs-lookup"><span data-stu-id="bc0e8-151">Test push notifications.</span></span> <span data-ttu-id="bc0e8-152">Geben Sie in der Befehlszeile Folgendes ein:</span><span class="sxs-lookup"><span data-stu-id="bc0e8-152">At the command line, type:</span></span>
    
        Test-CsMcxPushNotification -AccessEdgeFqdn <Access Edge service FQDN>
    
    <span data-ttu-id="bc0e8-153">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="bc0e8-153">For example:</span></span>
    
        Test-CsMcxPushNotification -AccessEdgeFqdn accessproxy.contoso.com

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="bc0e8-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="bc0e8-154">See Also</span></span>


[<span data-ttu-id="bc0e8-155">Test-CsFederatedPartner</span><span class="sxs-lookup"><span data-stu-id="bc0e8-155">Test-CsFederatedPartner</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsFederatedPartner)  
[<span data-ttu-id="bc0e8-156">Test-CsMcxPushNotification</span><span class="sxs-lookup"><span data-stu-id="bc0e8-156">Test-CsMcxPushNotification</span></span>](https://docs.microsoft.com/powershell/module/skype/Test-CsMcxPushNotification)  
  

<span data-ttu-id="bc0e8-157"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="bc0e8-157"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

