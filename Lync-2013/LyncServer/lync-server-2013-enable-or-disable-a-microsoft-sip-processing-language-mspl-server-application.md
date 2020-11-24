---
title: 'Lync Server 2013: Aktivieren oder Deaktivieren einer Microsoft SIP Processing Language (MSPL)-Server Anwendung'
description: 'Lync Server 2013: Aktivieren oder Deaktivieren einer Microsoft SIP Processing Language (MSPL)-Server Anwendung.'
ms.reviewer: ''
ms.author: v-lanac
author: lanachin
f1.keywords:
- NOCSH
TOCTitle: Enable or disable a Microsoft SIP Processing Language (MSPL) server application
ms:assetid: b20af38d-224a-4459-991d-0b7eabb3ca7c
ms:mtpsurl: https://technet.microsoft.com/en-us/library/Gg182573(v=OCS.15)
ms:contentKeyID: 48185145
ms.date: 07/23/2014
manager: serdars
mtps_version: v=OCS.15
ms.openlocfilehash: 8f919599d6c6a39fea73424f4e287f00636c0982
ms.sourcegitcommit: 36fee89bb887bea4f18b19f17a8c69daf5bc423d
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 11/24/2020
ms.locfileid: "49394183"
---
# <a name="enable-or-disable-a-microsoft-sip-processing-language-mspl-server-application-in-lync-server-2013"></a><span data-ttu-id="d11b0-103">Aktivieren oder Deaktivieren einer Microsoft SIP Processing Language (MSPL)-Serveranwendung in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d11b0-103">Enable or disable a Microsoft SIP Processing Language (MSPL) server application in Lync Server 2013</span></span>

<div data-xmlns="http://www.w3.org/1999/xhtml">

<div class="topic" data-xmlns="http://www.w3.org/1999/xhtml" data-msxsl="urn:schemas-microsoft-com:xslt" data-cs="https://msdn.microsoft.com/">

<div data-asp="https://msdn2.microsoft.com/asp">



</div>

<div id="mainSection">

<div id="mainBody"><span data-ttu-id="d11b0-104">

<span> </span></span><span class="sxs-lookup"><span data-stu-id="d11b0-104">

<span> </span></span></span>

<span data-ttu-id="d11b0-105">_**Letztes Änderungsdatum des Themas:** 2012-09-21_</span><span class="sxs-lookup"><span data-stu-id="d11b0-105">_**Topic Last Modified:** 2012-09-21_</span></span>

<span data-ttu-id="d11b0-106">Sie können die lync Server-Systemsteuerung verwenden, um MSPL-Serveranwendungen (Microsoft SIP Processing Language) zu aktivieren oder zu deaktivieren, die in ihrer lync Server 2013-Umgebung ausgeführt werden.</span><span class="sxs-lookup"><span data-stu-id="d11b0-106">You can use Lync Server Control Panel to enable or disable Microsoft SIP Processing Language (MSPL) server applications that run in your Lync Server 2013 environment.</span></span> <span data-ttu-id="d11b0-107">Bei diesen Anwendungen handelt es sich um nur-Skript-Anwendungen, die eine Skriptsprache anstelle der Microsoft lync 2013 Preview-API verwenden.</span><span class="sxs-lookup"><span data-stu-id="d11b0-107">These applications are script-only applications that use a scripting language instead of the Microsoft Lync 2013 Preview API.</span></span>

<span data-ttu-id="d11b0-108">Nicht alle Skripts können aktiviert oder deaktiviert werden.</span><span class="sxs-lookup"><span data-stu-id="d11b0-108">Not all scripts can be enabled or disabled.</span></span> <span data-ttu-id="d11b0-109">Beispielsweise ist das DefaultRouting-Skript aktiviert, und diese Option kann für DefaultRouting nicht geändert werden.</span><span class="sxs-lookup"><span data-stu-id="d11b0-109">For instance, the DefaultRouting script is enabled and this option cannot be changed for DefaultRouting.</span></span>

<div>

## <a name="to-enable-or-disable-an-mspl-server-application"></a><span data-ttu-id="d11b0-110">So aktivieren oder deaktivieren Sie eine MSPL-Serveranwendung</span><span class="sxs-lookup"><span data-stu-id="d11b0-110">To enable or disable an MSPL server application</span></span>

1.  <span data-ttu-id="d11b0-111">Melden Sie sich bei einem Benutzerkonto, das ein Mitglied der RTCUniversalServerAdmins-Gruppe ist (oder über entsprechende Benutzerrechte verfügt) oder der CsServerAdministrator-oder CsAdministrator-Rolle zugewiesen ist, bei jedem Computer an, der sich in dem Netzwerk befindet, in dem Sie lync Server 2013 bereitgestellt haben.</span><span class="sxs-lookup"><span data-stu-id="d11b0-111">From a user account that is a member of the RTCUniversalServerAdmins group (or has equivalent user rights), or assigned to the CsServerAdministrator or CsAdministrator role, log on to any computer that is in the network in which you deployed Lync Server 2013.</span></span>

2.  <span data-ttu-id="d11b0-112">Öffnen Sie ein Browserfenster, und geben Sie dann die Administrator-URL ein, um die lync Server-Systemsteuerung zu öffnen.</span><span class="sxs-lookup"><span data-stu-id="d11b0-112">Open a browser window, and then enter the Admin URL to open the Lync Server Control Panel.</span></span> <span data-ttu-id="d11b0-113">Details zu den verschiedenen Methoden, die Sie zum Starten der lync Server-Systemsteuerung verwenden können, finden Sie unter [Öffnen von lync Server 2013-Verwaltungstools](lync-server-2013-open-lync-server-administrative-tools.md).</span><span class="sxs-lookup"><span data-stu-id="d11b0-113">For details about the different methods you can use to start Lync Server Control Panel, see [Open Lync Server 2013 administrative tools](lync-server-2013-open-lync-server-administrative-tools.md).</span></span>

3.  <span data-ttu-id="d11b0-114">Klicken Sie in der linken Navigationsleiste auf **Topologie** , und klicken Sie dann auf **Server Anwendung**.</span><span class="sxs-lookup"><span data-stu-id="d11b0-114">In the left navigation bar, click **Topology** and then click **Server Application**.</span></span>

4.  <span data-ttu-id="d11b0-115">Klicken Sie auf der Seite **Serveranwendung** auf eine Spaltenüberschrift, um die Anwendungen bei Bedarf zu sortieren, und klicken Sie dann auf die Serveranwendung, die Sie ändern möchten.</span><span class="sxs-lookup"><span data-stu-id="d11b0-115">On the **Server Application** page, click a column heading to sort the applications, if needed, and then click the server application that you want to modify.</span></span>

5.  <span data-ttu-id="d11b0-116">Klicken Sie auf **Aktion**.</span><span class="sxs-lookup"><span data-stu-id="d11b0-116">Click **Action**.</span></span>

6.  <span data-ttu-id="d11b0-117">Klicken Sie auf Anwendung **aktivieren** oder **Anwendung deaktivieren** (das heißt, wenn das Skript diese Option unterstützt).</span><span class="sxs-lookup"><span data-stu-id="d11b0-117">Click **Enable application** or **Disable application** (that is, if the script supports this option).</span></span>

</div>

<div>

## <a name="see-also"></a><span data-ttu-id="d11b0-118">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d11b0-118">See Also</span></span>


[<span data-ttu-id="d11b0-119">Kennzeichnen einer MSPL-Anwendung (Microsoft SIP Processing Language) als kritisch oder nicht kritisch in lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d11b0-119">Mark a Microsoft SIP Processing Language (MSPL) application as critical or not critical in Lync Server 2013</span></span>](lync-server-2013-mark-a-microsoft-sip-processing-language-mspl-application-as-critical-or-not-critical.md)  


[<span data-ttu-id="d11b0-120">Anzeigen von MSPL-Serveranwendungen (Microsoft SIP Processing Language) in Lync Server 2013</span><span class="sxs-lookup"><span data-stu-id="d11b0-120">View Microsoft SIP Processing Language (MSPL) server applications in Lync Server 2013</span></span>](lync-server-2013-view-microsoft-sip-processing-language-mspl-server-applications.md)  


[<span data-ttu-id="d11b0-121">Verwalten der Lync Server 2013-Topologie</span><span class="sxs-lookup"><span data-stu-id="d11b0-121">Managing the Lync Server 2013 topology</span></span>](lync-server-2013-managing-the-lync-server-topology.md)  
  

<span data-ttu-id="d11b0-122"></div>

</div>

<span> </span>

</div>

</div>

</span><span class="sxs-lookup"><span data-stu-id="d11b0-122"></div>

</div>

<span> </span>

</div>

</div>

</span></span></div>

