---
title: 'Lync Server 2013: Löschen vorhandener Webdienst-Konfigurationseinstellungen'
description: 'Lync Server 2013: Löschen vorhandener Webdienst-Konfigurationseinstellungen.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Delete existing Web Service configuration settings
ms:assetid: c2b96f4c-4b07-48e6-9ca6-55bc0e0cf5a1
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182582(v=OCS.15)
ms:contentKeyID: 48185333
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 5a28197f26a447112e29b6e4a831585dd49a9854
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49430441"
---
# <a name="delete-existing-web-service-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="0abdc-103">Löschen vorhandener Webdienst-Konfigurationseinstellungen in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="0abdc-103">Delete existing Web Service configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="0abdc-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="0abdc-104">

<span> </span></span></span>

<span data-ttu-id="0abdc-105">_**Letztes Änderungsdatum des Themas:** 2013-02-23_</span><span class="sxs-lookup"><span data-stu-id="0abdc-105">_**Topic Last Modified:** 2013-02-23_</span></span>

<span data-ttu-id="0abdc-106">Führen Sie die folgenden Schritte aus, um Webdienst-Konfigurationseinstellungen zu löschen.</span><span class="sxs-lookup"><span data-stu-id="0abdc-106">Follow these steps to delete web service configuration settings.</span></span>

<div>

## <a name="to-delete-web-service-configuration-settings"></a><span data-ttu-id="0abdc-107">So löschen Sie vorhandene Webdienst-Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="0abdc-107">To delete web service configuration settings</span></span>

1.  <span data-ttu-id="0abdc-108">Melden Sie sich bei einem Benutzerkonto, das ein Mitglied der RTCUniversalServerAdmins-Gruppe ist (oder über entsprechende Benutzerrechte verfügt) oder der CsServerAdministrator-oder CsAdministrator-Rolle zugewiesen ist, bei jedem Computer an, der sich in dem Netzwerk befindet, in dem Sie lync Server 2013 bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="0abdc-108">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="0abdc-109">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="0abdc-109">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="0abdc-110">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="0abdc-110">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="0abdc-111">Klicken Sie in der linken Navigationsleiste auf **Sicherheit** und dann auf **Webdienst**.</span><span class="sxs-lookup"><span data-stu-id="0abdc-111">In the left navigation bar, click **Security** and then click **Web Service**.</span></span>

4.  <span data-ttu-id="0abdc-112">Geben Sie auf der Seite **Webdienst** in das Suchfeld den vollständigen oder teilweisen Namen der Richtlinie ein, die Sie löschen möchten.</span><span class="sxs-lookup"><span data-stu-id="0abdc-112">On the **Web Service** page, and in the search field, type all or part of the name of the policy you want to delete.</span></span>

5.  <span data-ttu-id="0abdc-113">Klicken Sie in der Richtlinienliste auf die gewünschte Richtlinie, dann auf **Bearbeiten** und anschließend auf **Löschen**.</span><span class="sxs-lookup"><span data-stu-id="0abdc-113">In the list of policies, click the policy that you want, click **Edit**, and then click **Delete**.</span></span>

6.  <span data-ttu-id="0abdc-114">Klicken Sie anschließend auf **OK**.</span><span class="sxs-lookup"><span data-stu-id="0abdc-114">Click **OK**.</span></span>

</div>

<div>

## <a name="deleting-web-service-configuration-settings-by-using-windows-powershell-cmdlets"></a><span data-ttu-id="0abdc-115">Löschen von Webdienst-Konfigurationseinstellungen mithilfe von Windows PowerShell-Cmdlets</span><span class="sxs-lookup"><span data-stu-id="0abdc-115">Deleting Web Service Configuration Settings by Using Windows PowerShell Cmdlets</span></span>

<span data-ttu-id="0abdc-116">Sie können Webdienst-Konfigurationseinstellungen mithilfe von Windows PowerShell und dem Cmdlet **Remove-CsWebServiceConfiguration** löschen.</span><span class="sxs-lookup"><span data-stu-id="0abdc-116">You can delete web service configuration settings by using Windows PowerShell and the **Remove-CsWebServiceConfiguration** cmdlet.</span></span> <span data-ttu-id="0abdc-117">Sie können dieses Cmdlet in der lync Server 2013-Verwaltungsshell oder in einer Remotesitzung von Windows PowerShell ausführen.</span><span class="sxs-lookup"><span data-stu-id="0abdc-117">You can run this cmdlet from the Lync Server 2013 Management Shell or from a remote session of Windows PowerShell.</span></span> <span data-ttu-id="0abdc-118">Details zum Verwenden der Remote-Windows PowerShell zum Herstellen einer Verbindung mit lync Server finden Sie im Windows PowerShell-Blog Artikel "schnell Start: Verwalten von Microsoft lync Server 2010 mithilfe von Remote-PowerShell" unter [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876) .</span><span class="sxs-lookup"><span data-stu-id="0abdc-118">For details about using remote Windows PowerShell to connect to Lync Server, see the Lync Server Windows PowerShell blog article "Quick Start: Managing Microsoft Lync Server 2010 Using Remote PowerShell" at [https://go.microsoft.com/fwlink/p/?linkId=255876](https://go.microsoft.com/fwlink/p/?linkid=255876).</span></span>

<div>

## <a name="to-delete-a-specific-collection-of-web-service-configuration-settings"></a><span data-ttu-id="0abdc-119">So löschen Sie bestimmte Konfigurationseinstellungen für Webdienste</span><span class="sxs-lookup"><span data-stu-id="0abdc-119">To delete a specific collection of web service configuration settings</span></span>

  - <span data-ttu-id="0abdc-120">Mit dem folgenden Befehl werden die Webdienstsicherheitseinstellungen für den Standort „Redmond“ entfernt:</span><span class="sxs-lookup"><span data-stu-id="0abdc-120">The following command removes the Web Service security settings applied to the Redmond site:</span></span>
    
        Remove-CsWebServiceConfiguration -Identity "site:Redmond"

</div>

<div>

## <a name="to-delete-all-of-the-web-service-configuration-settings-applied-to-the-site-scope"></a><span data-ttu-id="0abdc-121">So löschen Sie alle auf den Standortbereich angewendeten Konfigurationseinstellungen für Webdienste</span><span class="sxs-lookup"><span data-stu-id="0abdc-121">To delete all of the web service configuration settings applied to the site scope</span></span>

  - <span data-ttu-id="0abdc-122">Mit dem folgenden Befehl werden alle auf den Dienstbereich angewendeten Webdienstsicherheitseinstellungen entfernt:</span><span class="sxs-lookup"><span data-stu-id="0abdc-122">The following command removes all of the Web Service security settings applied to the service scope:</span></span>
    
        Get-CsWebServiceConfiguration -Filter "service:*" | Remove-CsWebServiceConfiguration

</div>

<div>

## <a name="to-delete-all-of-the-web-service-configuration-settings-that-allow-certificate-authentication"></a><span data-ttu-id="0abdc-123">So löschen Sie alle Konfigurationseinstellungen für Webdienste, die eine Zertifikatauthentifizierung zulassen</span><span class="sxs-lookup"><span data-stu-id="0abdc-123">To delete all of the web service configuration settings that allow certificate authentication</span></span>

  - <span data-ttu-id="0abdc-124">Mit dem folgenden Befehl werden alle Webdienstsicherheitseinstellungen entfernt, die die Verwendung der Zertifikatauthentifizierung zulassen:</span><span class="sxs-lookup"><span data-stu-id="0abdc-124">The following command removes all the Web Service security settings that allow the use of certificate authentication:</span></span>
    
        Get-CsWebServiceConfiguration | Where-Object {$_.UseCertificateAuth -eq $True} | Remove-CsWebServiceConfiguration

</div>

<span data-ttu-id="0abdc-125">Ausführliche Informationen finden Sie unter [Remove-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsWebServiceConfiguration).</span><span class="sxs-lookup"><span data-stu-id="0abdc-125">For details, see [Remove-CsWebServiceConfiguration](https://docs.microsoft.com/powershell/module/skype/Remove-CsWebServiceConfiguration).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="0abdc-126">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0abdc-126">See Also</span></span>


[<span data-ttu-id="0abdc-127">Konfigurieren der Authentifizierung in der lync Server 2013-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="0abdc-127">Configuring authentication in the Lync Server 2013 Control Panel</span></span>](lync-server-2013-configuring-authentication-in-the-lync-server-control-panel.md)  
  

<span data-ttu-id="0abdc-128"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="0abdc-128"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

