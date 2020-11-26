---
title: 'Lync Server 2013: Ändern vorhandener Webdienst-Konfigurationseinstellungen'
description: 'Lync Server 2013: Ändern vorhandener Webdienst-Konfigurationseinstellungen'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Modify existing Web Service configuration settings
ms:assetid: bd9c7aa5-d31c-4fab-b31d-8baae26b1296
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182580(v=OCS.15)
ms:contentKeyID: 48185272
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 455ddf60d171fe584115d646b16f63595285a906
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/26/2020
ms.locfileid: "49445757"
---
# <a name="modify-existing-web-service-configuration-settings-in-lync-server-2013"></a><span data-ttu-id="eee97-103">Ändern vorhandener Konfigurationseinstellungen für den Webdienst in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="eee97-103">Modify existing Web Service configuration settings in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="eee97-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="eee97-104">

<span> </span></span></span>

<span data-ttu-id="eee97-105">_**Letztes Änderungsdatum des Themas:** 2012-11-01_</span><span class="sxs-lookup"><span data-stu-id="eee97-105">_**Topic Last Modified:** 2012-11-01_</span></span>

<span data-ttu-id="eee97-106">Sie können die **Webdienst** Seite verwenden, um die Authentifizierungsmethoden für den Zugriff auf lync Server 2013-Verwandte Webserver und Webdienste zu konfigurieren.</span><span class="sxs-lookup"><span data-stu-id="eee97-106">You can use the **Web Service** page to configure the authentication methods for accessing Lync Server 2013 related web servers and Web Services.</span></span>

<span data-ttu-id="eee97-107">Führen Sie die folgenden Schritte aus, um eine vorhandene Webdienstrichtlinie zu ändern.</span><span class="sxs-lookup"><span data-stu-id="eee97-107">Follow these steps to modify an existing Web Service policy.</span></span>

<div>

## <a name="to-modify-existing-web-service-configuration-settings"></a><span data-ttu-id="eee97-108">So ändern Sie vorhandene Webdienst-Konfigurationseinstellungen</span><span class="sxs-lookup"><span data-stu-id="eee97-108">To modify existing Web service configuration settings</span></span>

1.  <span data-ttu-id="eee97-109">Melden Sie sich bei einem Benutzerkonto, das ein Mitglied der RTCUniversalServerAdmins-Gruppe ist (oder über entsprechende Benutzerrechte verfügt) oder der CsServerAdministrator-oder CsAdministrator-Rolle zugewiesen ist, bei jedem Computer an, der sich in dem Netzwerk befindet, in dem Sie lync Server 2013 bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="eee97-109">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="eee97-110">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="eee97-110">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="eee97-111">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="eee97-111">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="eee97-112">Klicken Sie in der linken Navigationsleiste auf **Sicherheit** und dann auf **Webdienst**.</span><span class="sxs-lookup"><span data-stu-id="eee97-112">In the left navigation bar, click **Security** and then click **Web Service**.</span></span>

4.  <span data-ttu-id="eee97-113">Klicken Sie auf der Seite **Webdienst** auf eine Konfiguration, klicken Sie auf **Bearbeiten** und dann auf **Details einblenden**.</span><span class="sxs-lookup"><span data-stu-id="eee97-113">On the **Web Service** page, click a configuration, click **Edit**, and then click **Show details**.</span></span>

5.  <span data-ttu-id="eee97-114">Wählen Sie im Abschnitt **Webdiensteinstellung bearbeiten** unter **Integrierte Windows-Authentifizierung** die Option **Aushandeln**, **Integrierte Windows-Authentifizierung** oder **Keine** aus.</span><span class="sxs-lookup"><span data-stu-id="eee97-114">In **Edit Web Service Setting**, in **Integrated Windows authentication**, select **Negotiate**, **Integrated Windows authentication**, or **None**.</span></span>

6.  <span data-ttu-id="eee97-115">Wählen Sie je nach Funktionen der Clients und der Unterstützung in Ihrer Umgebung eine oder mehrere der folgenden Optionen aus:</span><span class="sxs-lookup"><span data-stu-id="eee97-115">Select one or more of the following depending on the capabilities of the clients and support in your environment:</span></span>
    
      - <span data-ttu-id="eee97-116">**PIN-Authentifizierung aktivieren**: Clients werden über eine PIN authentifiziert.</span><span class="sxs-lookup"><span data-stu-id="eee97-116">**Enable PIN Authentication** to enable clients to be authenticated using PIN numbers.</span></span>
    
      - <span data-ttu-id="eee97-117">**Zertifikatauthentifizierung aktivieren**: Die Server im Pool stellen Zertifikate an Clients aus.</span><span class="sxs-lookup"><span data-stu-id="eee97-117">**Enable certificate authentication** to have the servers in the pool issue certificates to clients.</span></span>
    
      - <span data-ttu-id="eee97-118">**Download einer Zertifikatkette aktivieren**: Server können die Zertifikatkette für das jeweilige Zertifikat herunterladen.</span><span class="sxs-lookup"><span data-stu-id="eee97-118">**Enable certificate chain download** to have servers presented with an authentication certificate download the certificate chain for that certificate.</span></span>

7.  <span data-ttu-id="eee97-119">Klicken Sie auf **Commit ausführen**.</span><span class="sxs-lookup"><span data-stu-id="eee97-119">Click **Commit**.</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="eee97-120">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="eee97-120">See Also</span></span>


[<span data-ttu-id="eee97-121">Konfigurieren der Authentifizierung in der lync Server 2013-Systemsteuerung</span><span class="sxs-lookup"><span data-stu-id="eee97-121">Configuring authentication in the Lync Server 2013 Control Panel</span></span>](lync-server-2013-configuring-authentication-in-the-lync-server-control-panel.md)  
  

<span data-ttu-id="eee97-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="eee97-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

