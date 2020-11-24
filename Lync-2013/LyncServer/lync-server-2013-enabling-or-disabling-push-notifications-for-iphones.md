---
title: 'Lync Server 2013: Aktivieren oder Deaktivieren von Push-Benachrichtigungen für iPhones'
description: 'Lync Server 2013: Aktivieren oder Deaktivieren von Push-Benachrichtigungen für iPhones.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enabling or disabling push notifications for iPhones
ms:assetid: 8bbf531a-807f-4a8f-814a-94bfed8f97ef
ms:mtpsurl: https://technet.microsoft.com/en-us/library/JJ688122(v=OCS.15)
ms:contentKeyID: 49733719
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 07a9c5ec442c3628455797b987d8b2f22677e70e
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394702"
---
# <a name="enabling-or-disabling-push-notifications-for-iphones-in-lync-server-2013"></a><span data-ttu-id="ecc08-103">Aktivieren oder Deaktivieren von Push-Benachrichtigungen für iPhones in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ecc08-103">Enabling or disabling push notifications for iPhones in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="ecc08-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="ecc08-104">

<span> </span></span></span>

<span data-ttu-id="ecc08-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="ecc08-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="ecc08-106">Push-Benachrichtigungen in Form von Signalen, Symbolen oder Benachrichtigungen können auch dann an ein iPhone gesendet werden, wenn die Mobile Anwendung inaktiv ist.</span><span class="sxs-lookup"><span data-stu-id="ecc08-106">Push notifications, in the form of badges, icons, or alerts, can be sent to an iPhone even when the mobile application is inactive.</span></span> <span data-ttu-id="ecc08-107">Push-Benachrichtigungen benachrichtigt einen Benutzer über Ereignisse wie eine neue oder verpasste Chat Einladung und Voicemail.</span><span class="sxs-lookup"><span data-stu-id="ecc08-107">Push notifications notify a user of events such as a new or missed IM invitation and voice mail.</span></span> <span data-ttu-id="ecc08-108">Sie können Push-Benachrichtigungen für iPhone aktivieren oder deaktivieren, indem Sie entweder die lync Server 2013-Systemsteuerung oder die lync Server 2013-Verwaltungsshell verwenden.</span><span class="sxs-lookup"><span data-stu-id="ecc08-108">You can enable or disable push notifications for iPhone by using either Lync Server 2013 Control Panel or Lync Server 2013 Management Shell.</span></span>

<div>

## <a name="to-enable-push-notifications-for-iphone-by-using-lync-server-control-panel"></a><span data-ttu-id="ecc08-109">So aktivieren Sie Push-Benachrichtigungen für iPhone mithilfe der lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="ecc08-109">To enable push notifications for iPhone by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="ecc08-110">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="ecc08-110">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ecc08-111">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ecc08-111">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ecc08-112">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ecc08-112">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ecc08-113">Klicken Sie in der linken Navigationsleiste auf **Clients**, und klicken Sie dann auf die Schaltfläche Navigations **Benachrichtigungskonfiguration** .</span><span class="sxs-lookup"><span data-stu-id="ecc08-113">In the left navigation bar, click **Clients**, and then click the **Push Notification Configuration** navigation button.</span></span>

4.  <span data-ttu-id="ecc08-114">Klicken Sie auf der Seite **Konfiguration der Push-Benachrichtigung** auf die Website, die Sie bearbeiten möchten, klicken Sie auf das Menü **Bearbeiten** , und klicken Sie dann auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="ecc08-114">On the **Push Notification Configuration** page, click the site you want to edit, click the **Edit** menu, and then click **Show details**.</span></span>

5.  <span data-ttu-id="ecc08-115">Klicken Sie auf das Kontrollkästchen **Apple-Push-Benachrichtigungen aktivieren** .</span><span class="sxs-lookup"><span data-stu-id="ecc08-115">Click the **Enable Apple push notifications** checkbox.</span></span>

6.  <span data-ttu-id="ecc08-116">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="ecc08-116">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-disable-push-notifications-for-iphone-by-using-lync-server-control-panel"></a><span data-ttu-id="ecc08-117">So deaktivieren Sie Push-Benachrichtigungen für iPhone mithilfe der lync Server-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="ecc08-117">To disable push notifications for iPhone by using Lync Server Control Panel</span></span>

1.  <span data-ttu-id="ecc08-118">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="ecc08-118">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="ecc08-119">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="ecc08-119">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="ecc08-120">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="ecc08-120">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="ecc08-121">Klicken Sie in der linken Navigationsleiste auf **Clients**, und klicken Sie dann auf die Schaltfläche Navigations **Benachrichtigungskonfiguration** .</span><span class="sxs-lookup"><span data-stu-id="ecc08-121">In the left navigation bar, click **Clients**, and then click the **Push Notification Configuration** navigation button.</span></span>

4.  <span data-ttu-id="ecc08-122">Klicken Sie auf der Seite **Konfiguration der Push-Benachrichtigung** auf die Website, die Sie bearbeiten möchten, klicken Sie auf das Menü **Bearbeiten** , und klicken Sie dann auf **Details anzeigen**.</span><span class="sxs-lookup"><span data-stu-id="ecc08-122">On the **Push Notification Configuration** page, click the site you want to edit, click the **Edit** menu, and then click **Show details**.</span></span>

5.  <span data-ttu-id="ecc08-123">Deaktivieren Sie das Kontrollkästchen **Apple-Push-Benachrichtigungen aktivieren** .</span><span class="sxs-lookup"><span data-stu-id="ecc08-123">Clear the **Enable Apple push notifications** checkbox.</span></span>

6.  <span data-ttu-id="ecc08-124">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="ecc08-124">Click **Commit**.</span></span>

</div>

<div>

## <a name="enabling-or-disabling-push-notifications-to-iphone-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="ecc08-125">Aktivieren oder Deaktivieren von Push-Benachrichtigungen auf dem iPhone mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="ecc08-125">Enabling or Disabling Push Notifications to iPhone by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="ecc08-126">Push-Benachrichtigungen an Apple iPhone können mithilfe des Cmdlets " **CsPushNotificationConfiguration** " aktiviert oder deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="ecc08-126">Push notifications to Apple iPhone can be enabled or disabled by using the **Set-CsPushNotificationConfiguration** cmdlet.</span></span> <span data-ttu-id="ecc08-127">Sie können dieses Cmdlet entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="ecc08-127">You can run this cmdlet either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="ecc08-128">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="ecc08-128">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-enable-push-notifications-for-iphone"></a><span data-ttu-id="ecc08-129">So aktivieren Sie Push-Benachrichtigungen für iPhone</span><span class="sxs-lookup"><span data-stu-id="ecc08-129">To enable push notifications for iPhone</span></span>

  - <span data-ttu-id="ecc08-130">So aktivieren Sie die Push-Benachrichtigungen für iPhone legen Sie den Wert der EnableApplePushNotificationService-Eigenschaft auf true ($true) fest.</span><span class="sxs-lookup"><span data-stu-id="ecc08-130">To enable push notifications for iPhone set the value of the EnableApplePushNotificationService property to True ($True).</span></span> <span data-ttu-id="ecc08-131">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ecc08-131">For example:</span></span>
    
        Set-CsPushNotificationConfiguration -Identity "site:Redmond" -EnableApplePushNotificationService $True

</div>

<div>

## <a name="to-disable-push-notifications-for-iphone"></a><span data-ttu-id="ecc08-132">So deaktivieren Sie Push-Benachrichtigungen für iPhone</span><span class="sxs-lookup"><span data-stu-id="ecc08-132">To disable push notifications for iPhone</span></span>

  - <span data-ttu-id="ecc08-133">So deaktivieren Sie Push-Benachrichtigungen für iPhone legen Sie den Wert der EnableApplePushNotificationService-Eigenschaft auf false ($false) fest.</span><span class="sxs-lookup"><span data-stu-id="ecc08-133">To disable push notifications for iPhone set the value of the EnableApplePushNotificationService property to False ($False).</span></span> <span data-ttu-id="ecc08-134">Beispiel:</span><span class="sxs-lookup"><span data-stu-id="ecc08-134">For example:</span></span>
    
        Set-CsPushNotificationConfiguration -Identity "site:Redmond" -EnableApplePushNotificationService $False

</div>

<span data-ttu-id="ecc08-135">Weitere Informationen finden Sie im Hilfethema zum Cmdlet " [Satz-CsPushNotificationConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsPushNotificationConfiguration) ".</span><span class="sxs-lookup"><span data-stu-id="ecc08-135">For more information, see the help topic for the [Set-CsPushNotificationConfiguration](https://docs.microsoft.com/powershell/module/skype/Set-CsPushNotificationConfiguration) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="ecc08-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ecc08-136">See Also</span></span>


[<span data-ttu-id="ecc08-137">Konfigurieren von Pushbenachrichtigungen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="ecc08-137">Configuring for push notifications in Lync Server 2013</span></span>](lync-server-2013-configuring-for-push-notifications.md)  
  

<span data-ttu-id="ecc08-138"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="ecc08-138"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

