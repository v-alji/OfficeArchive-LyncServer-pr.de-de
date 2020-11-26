---
title: Ändern der Standardaktion für nicht explizit unterstützte oder eingeschränkte Clients
description: Ändern Sie die Standardaktion für Clients, die nicht explizit unterstützt oder eingeschränkt sind.
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify the default action for clients not explicitly supported or restricted
ms:assetid: 548dd0f5-62fe-4c3f-8952-2b9fd4c5fff3
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg520994(v=OCS.15)
ms:contentKeyID: 48184137
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 2c28ad4d357953c22f889309323ccbb95c6840e2
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445736"
---
# <a name="modify-the-default-action-for-clients-not-explicitly-supported-or-restricted-in-lync-server-2013"></a><span data-ttu-id="e63d1-103">Ändern der Standardaktion für Clients, die in lync Server 2013 nicht explizit unterstützt oder eingeschränkt werden</span><span class="sxs-lookup"><span data-stu-id="e63d1-103">Modify the default action for clients not explicitly supported or restricted in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="e63d1-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="e63d1-104">

<span> </span></span></span>

<span data-ttu-id="e63d1-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="e63d1-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="e63d1-106">Sie können nicht nur die Version der Clients angeben, die Sie in ihrer lync Server 2013-Umgebung unterstützen möchten, sondern auch eine Standardaktion für Clients angeben, für die noch keine Versionsrichtlinie definiert ist.</span><span class="sxs-lookup"><span data-stu-id="e63d1-106">In addition to specifying the version of clients that you want to support in your Lync Server 2013 environment, you can also specify a default action for clients that do not already have a version policy defined.</span></span> <span data-ttu-id="e63d1-107">Auf diese Weise können Sie einschränken, welche Clientversionen in ihrer lync Server-Umgebung verwendet werden, was Ihnen helfen kann, die Kosten zu kontrollieren, die mit der Unterstützung mehrerer Clientversionen verbunden sind.</span><span class="sxs-lookup"><span data-stu-id="e63d1-107">This enables you to restrict which client versions are used in your Lync Server environment, which can help you control the costs associated with supporting multiple client versions.</span></span>

<div>

## <a name="to-modify-the-default-action-for-clients-not-explicitly-supported-or-restricted"></a><span data-ttu-id="e63d1-108">So ändern Sie die Standardaktion für nicht explizit unterstützte oder eingeschränkte Clients</span><span class="sxs-lookup"><span data-stu-id="e63d1-108">To modify the default action for clients not explicitly supported or restricted</span></span>

1.  <span data-ttu-id="e63d1-109">Melden Sie sich mit einem Benutzerkonto, dem die Rolle "CsUserAdministrator" oder "CsAdministrator" zugewiesen ist, auf einem beliebigen Computer in Ihrer internen Bereitstellung an.</span><span class="sxs-lookup"><span data-stu-id="e63d1-109">From a user account that is assigned to the CsUserAdministrator role or the CsAdministrator role, log on to any computer in your internal deployment.</span></span>

2.  <span data-ttu-id="e63d1-110">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="e63d1-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="e63d1-111">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="e63d1-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="e63d1-112">Klicken Sie in der linken Navigationsleiste auf **Clients**, und klicken Sie dann auf **Client Versions Konfiguration**.</span><span class="sxs-lookup"><span data-stu-id="e63d1-112">In the left navigation bar, click **Clients**, and then click **Client Version Configuration**.</span></span>

4.  <span data-ttu-id="e63d1-113">Doppelklicken Sie auf der Seite **Client Versions Konfiguration** auf die **globale** Konfiguration in der Liste.</span><span class="sxs-lookup"><span data-stu-id="e63d1-113">On the **Client Version Configuration** page, double-click the **Global** configuration in the list.</span></span>

5.  <span data-ttu-id="e63d1-114">Überprüfen Sie im Dialogfeld **Client-Versions Konfiguration bearbeiten** , ob das Kontrollkästchen **Versionskontrolle aktivieren** aktiviert ist, und wählen Sie dann unter **Standardaktion** eine der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="e63d1-114">In the **Edit Client Version Configuration** dialog box, verify that the **Enable version control** check box is selected and then, under **Default action**, select one of the following:</span></span>
    
      - <span data-ttu-id="e63d1-115">**Zulassen**   Ermöglicht es dem Client, sich anzumelden, wenn die Client Version keinem Filter in der Liste der **clientversionsrichtlinien** entspricht.</span><span class="sxs-lookup"><span data-stu-id="e63d1-115">**Allow**   Allows the client to log on if the client version does not match any filter in the **Client version policies** list.</span></span>
    
      - <span data-ttu-id="e63d1-116">**Blockieren**   Verhindert, dass der Client sich anmeldet, wenn die Client Version keinem Filter in der Liste der **clientversionsrichtlinien** entspricht.</span><span class="sxs-lookup"><span data-stu-id="e63d1-116">**Block**   Prevents the client from logging on if the client version does not match any filter in the **Client version policies** list.</span></span>
    
      - <span data-ttu-id="e63d1-117">**Block mit URL**   Verhindert, dass der Client sich anmeldet, wenn die Client Version keinem Filter in der Liste der **clientversionsrichtlinien** entspricht und eine Fehlermeldung mit einer URL enthält, in der ein neuerer Client heruntergeladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="e63d1-117">**Block with URL**   Prevents the client from logging on if the client version does not match any filter in the **Client version policies** list, and include an error message containing a URL where a newer client can be downloaded.</span></span>
    
      - <span data-ttu-id="e63d1-118">**Mit URL zulassen**   Ermöglicht es dem Client, sich anzumelden, wenn die Client Version nicht mit einem Filter in der Liste der **clientversionsrichtlinien** übereinstimmt, und eine Fehlermeldung mit einer URL einfügen, in der ein neuerer Client heruntergeladen werden kann.</span><span class="sxs-lookup"><span data-stu-id="e63d1-118">**Allow with URL**   Allows the client to log on if the client version does not match any filter in the **Client version policies** list, and include an error message containing a URL where a newer client can be downloaded.</span></span>

6.  <span data-ttu-id="e63d1-119">Wenn Sie **Block with URL** ausgewählt haben, geben Sie die Client Download-URL ein, die in die Fehlermeldung im Feld **URL** eingeschlossen werden soll.</span><span class="sxs-lookup"><span data-stu-id="e63d1-119">If you selected **Block with URL**, type the client download URL to include in the error message in the **URL** box.</span></span>

7.  <span data-ttu-id="e63d1-120">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="e63d1-120">Click **Commit**.</span></span>

</div>

<div>

## <a name="to-disable-client-version-control"></a><span data-ttu-id="e63d1-121">So deaktivieren Sie die Client Versionskontrolle</span><span class="sxs-lookup"><span data-stu-id="e63d1-121">To disable client version control</span></span>

  - <span data-ttu-id="e63d1-122">Wenn Sie die Versionskontrolle deaktivieren möchten, damit sich alle Clients unabhängig von der Client Version anmelden können, deaktivieren Sie das Kontrollkästchen **Versionskontrolle aktivieren** , und klicken Sie dann auf **Commit**.</span><span class="sxs-lookup"><span data-stu-id="e63d1-122">To disable version control to allow all clients to log on regardless of the client version, clear the **Enable version control** check box, and then click **Commit**.</span></span>

</div>

<div>

## <a name="modifying-the-default-action-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="e63d1-123">Ändern der Standardaktion mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="e63d1-123">Modifying the Default Action by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="e63d1-124">Die Standardaktion, die ausgeführt werden soll, wenn Benutzer versuchen, sich mithilfe von Clients anzuschließen, die nicht explizit unterstützt werden oder durch eine clientversionsrichtlinie eingeschränkt sind, können mithilfe der Windows PowerShell-Befehlszeilenschnittstelle und des Cmdlets " **CsClientVersionPolicy** " verwaltet werden.</span><span class="sxs-lookup"><span data-stu-id="e63d1-124">The default action to be taken when users try to sign on using clients that are not explicitly supported or restricted by a client version policy can be managed by using Windows PowerShell command-line interface and the **Set-CsClientVersionPolicy** cmdlet.</span></span> <span data-ttu-id="e63d1-125">Dieses Cmdlet kann entweder in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="e63d1-125">This cmdlet can be run either from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="e63d1-126">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="e63d1-126">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-configure-the-default-action-to-block-access"></a><span data-ttu-id="e63d1-127">So konfigurieren Sie die Standardaktion zum Blockieren des Zugriffs</span><span class="sxs-lookup"><span data-stu-id="e63d1-127">To configure the default action to block access</span></span>

  - <span data-ttu-id="e63d1-128">Mit dem folgenden Befehl wird die Standardaktion für den Redmond-Website Block festgelegt.</span><span class="sxs-lookup"><span data-stu-id="e63d1-128">The following command sets the default action for the Redmond site Block.</span></span> <span data-ttu-id="e63d1-129">Dadurch wird die Registrierung für jeden Client blockiert, für den keine Client-Versions Konfigurationsregel vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e63d1-129">This will block registration for any client for which no client version configuration rule exists.</span></span>
    
        Set-CsClientVersionConfiguration -Identity "site:Redmond" -DefaultAction Block

</div>

<div>

## <a name="to-configure-the-default-action-to-allow-access"></a><span data-ttu-id="e63d1-130">So konfigurieren Sie die Standardaktion zum Zulassen des Zugriffs</span><span class="sxs-lookup"><span data-stu-id="e63d1-130">To configure the default action to allow access</span></span>

  - <span data-ttu-id="e63d1-131">In diesem Beispiel ist die Standardaktion für die Website "Redmond" auf "zulassen" eingestellt.</span><span class="sxs-lookup"><span data-stu-id="e63d1-131">In this example, the default action for the Redmond site is set to Allow.</span></span> <span data-ttu-id="e63d1-132">Dies ermöglicht die Registrierung für jeden Client, für den keine Client-Versions Konfigurationsregel vorhanden ist.</span><span class="sxs-lookup"><span data-stu-id="e63d1-132">This will allow registration for any client for which no client version configuration rule exists.</span></span>
    
        Set-CsClientVersionConfiguration -Identity "site:Redmond" -DefaultAction Allow

</div>

<span data-ttu-id="e63d1-133">Ausführliche Informationen finden Sie im Hilfethema zum Cmdlet " [Satz-CsClientVersionPolicy](https://technet.microsoft.com/library/Gg398876(v=OCS.15)) ".</span><span class="sxs-lookup"><span data-stu-id="e63d1-133">For details, see the Help topic for the [Set-CsClientVersionPolicy](https://technet.microsoft.com/library/Gg398876(v=OCS.15)) cmdlet.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="e63d1-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e63d1-134">See Also</span></span>


[<span data-ttu-id="e63d1-135">Verwalten von Geräten, Telefonen und Clientanwendungen in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="e63d1-135">Managing devices, phones, and client applications in Lync Server 2013</span></span>](lync-server-2013-managing-devices-phones-and-client-applications.md)  
  

<span data-ttu-id="e63d1-136"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="e63d1-136"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

